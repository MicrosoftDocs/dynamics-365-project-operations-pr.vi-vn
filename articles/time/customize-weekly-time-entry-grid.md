---
title: Kéo dài mục nhập thời gian
description: Chủ đề này cung cấp thông tin về cách các nhà phát triển có thể mở rộng kiểm soát mục nhập thời gian.
author: stsporen
ms.date: 10/08/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 02ed62c9ea27429b4b1d95d67d1607a090ab1dd2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996007"
---
# <a name="extending-time-entries"></a>Kéo dài mục nhập thời gian

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Dynamics 365 Project Operations bao gồm một kiểm soát tùy chỉnh nhập giờ có thể mở rộng. Điều khiển này bao gồm những tính năng sau đây:

- Nhập thời gian theo chiều ngang trong một tuần
- Tổng số theo ngày, hàng hoặc tuần
- Sao chép hàng hoặc tuần
- Mục nhập thời gian thông qua HH:mm hoặc HH.hh (tự động chuyển đổi thành HH.hh)
- Nhập từ mục chỉ định, đặt trước hoặc cuộc hẹn

Có thể kéo dài mục nhập thời gian trong hai lĩnh vực:
- [Thêm các mục nhập thời gian tùy chỉnh để sử dụng cho riêng bạn](#add)
- [Tùy chỉnh điều khiển mục nhập thời gian hằng tuần](#customize)

## <a name="add-custom-time-entries-for-your-own-use"></a><a name="add"></a>Thêm mục nhập thời gian tùy chỉnh để chính bạn sử dụng

Mục nhập thời gian là thực thể lõi được sử dụng trong nhiều tình huống. Trong bản phát hành tháng 4 năm 2020 đợt 1, giải pháp lõi TESA đã được giới thiệu. TESA cung cấp một thực thể **Thiết đặt** và một vai trò bảo mật **Người dùng nhập thời gian** mới. Các trường mới, **msdyn_start** và **msdyn_end**, có mối quan hệ trực tiếp với **msdyn_duration** cũng được cung cấp. Thực thể, vai trò bảo mật và các trường mới cho phép một cách tiếp cận thống nhất hơn về thời gian trên nhiều sản phẩm.


### <a name="time-source-entity"></a>Thực thể nguồn thời gian
| Trường | Nội dung mô tả | 
|-------|------------|
| Tên  | Tên của mục nhập Nguồn thời gian được sử dụng làm giá trị lựa chọn khi tạo mục nhập thời gian. |
| Nguồn thời gian mặc định [Nguồn thời gian: isdefault] | Theo mặc định, chỉ một Nguồn thời gian có thể được đánh dấu tại mục mặc định. Điều này cho phép các mục nhập được lấy mặc định theo một nguồn thời gian nếu chưa có nguồn nào được chỉ định. |
|Loại nguồn thời gian [Nguồn thời gian: sourcetype] | Loại nguồn là một tùy chọn (Loại nguồn mục nhập thời gian) cho phép liên kết nguồn thời gian với một ứng dụng. Microsoft bảo lưu các giá trị lớn hơn 190.000.000.|


### <a name="time-entries-and-the-time-source-entity"></a>Mục nhập thời gian và thực thể Nguồn thời gian
Mỗi mục nhập thời gian được liên kết với một bản ghi nguồn thời gian. Bản ghi này xác định cách thức và ứng dụng nào sẽ xử lý mục nhập thời gian.

Các mục nhập thời gian luôn là một khối thời gian liền kề có liên kết bắt đầu, kết thúc và khoảng thời gian.

Logic sẽ tự động cập nhật bản ghi mục nhập thời gian trong các trường hợp sau:

- Nếu hai trong ba trường sau được cung cấp, thì trường thứ ba sẽ được tính toán tự động: 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- Các trường **msdyn_start** và **msdyn_end** phân biệt múi giờ.
- Mục nhập thời gian được tạo chỉ với **msdyn_date** và **msdyn_duration** được chỉ định sẽ bắt đầu lúc nửa đêm. Các trường **msdyn_start** và **msdyn_end** sẽ cập nhật tương ứng.

#### <a name="time-entry-types"></a>Loại mục nhập thời gian

Bản ghi mục nhập thời gian có một loại liên kết xác định hành vi trong luồng gửi cho ứng dụng được liên kết.

|Nhãn | Giá_trị|
|-----|-----|
|Trong thời gian nghỉ   |192,355,000|
|Di chuyển | 192,355,001|
|Làm thêm   | 192,354,320|
|Công việc   | 192,350,000|
|Vắng mặt    | 192,350,001|
|Kỳ nghỉ   | 192,350,002|



## <a name="customize-the-weekly-time-entry-control"></a><a name="customize"></a>Tùy chỉnh bộ điều khiển mục nhập Thời gian hằng tuần
Các nhà phát triển có thể thêm các trường và tra cứu bổ sung cho các thực thể khác, đồng thời triển khai các quy tắc kinh doanh tùy chỉnh để hỗ trợ các tình huống kinh doanh của họ.

### <a name="add-custom-fields-with-lookups-to-other-entities"></a>Thêm các trường tùy chỉnh có mục tra cứu cho thực thể khác
Có 3 bước chính để thêm trường tùy chỉnh vào lưới mục nhập thời gian hàng tuần.

1. Thêm trường tùy chỉnh vào hộp thoại tạo nhanh.
2. Cấu hình lưới để hiển thị trường tùy chỉnh.
3. Thêm trường tùy chỉnh vào dòng tác vụ sửa hàng hoặc dòng tác vụ sửa ô.

Bảo đảm rằng trường mới có các mục xác thực bắt buộc trong dòng tác vụ sửa hàng hoặc ô. Trong bước này, hãy khóa trường dựa trên trạng thái mục nhập thời gian.

### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Thêm trường tùy chỉnh vào hộp thoại tạo nhanh
Thêm trường tùy chỉnh vào hộp thoại **Tạo nhanh mục nhập thời gian**. Sau đó, khi mục nhập thời gian được thêm, người dùng có thể nhập giá trị bằng cách chọn **Mới**.

### <a name="configure-the-grid-to-show-the-custom-field"></a>Cấu hình lưới để hiển thị trường tùy chỉnh
Có 2 cách để thêm trường tùy chỉnh vào lưới mục nhập thời gian hàng tuần:

  - Tùy chỉnh chế độ xem và thêm trường tùy chỉnh
  - Tạo mục nhập thời gian tùy chỉnh mặc định mới 


#### <a name="customize-a-view-and-add-a-custom-field"></a>Tùy chỉnh chế độ xem và thêm trường tùy chỉnh

Tùy chỉnh dạng xem **Mục nhập thời gian hằng tuần của tôi** và thêm trường tùy chỉnh vào đó. Bạn có thể chọn vị trí và kích cỡ của trường tùy chỉnh trong lưới bằng cách sửa các thuộc tính trong dạng xem.

#### <a name="create-a-new-default-custom-time-entry"></a>Tạo mục nhập thời gian tùy chỉnh mặc định mới

dạng xem này sẽ chứa các trường **Mô tả** và **Nhận xét bên ngoài**, ngoài các cột mà bạn muốn có trong lưới. 

1. Chọn vị trí, kích thước và thứ tự sắp xếp mặc định cho lưới bằng cách chỉnh sửa các thuộc tính đó trong dạng xem. 
2. Cấu hình bộ kiểm soát tùy chỉnh cho dạng xem này để trở thành bộ kiểm soát **Lưới mục nhập thời gian**. 
3. Thêm bộ kiểm soát này vào dạng xem và chọn cho web, điện thoại và máy tính bảng. 
4. Cấu hình các thông số cho lưới mục nhập thời gian hàng tuần. 
5. Đặt trường **Ngày bắt đầu** thành **msdyn_date**, đặt trường **Khoảng thời gian** thành **msdyn_duration** và đặt trường **Trạng thái** thành **msdyn_entrystatus**. 
6. Đối với dạng xem mặc định, trường **Danh sách trạng thái chỉ đọc** được đặt thành **192350002,192350003,192350004**. Trường **Dòng tác vụ sửa hàng** được đặt thành **msdyn_timeentryrowedit**. Trường **Dòng tác vụ sửa ô** được đặt thành **msdyn_timeentryedit**. 
7. Bạn có thể tùy chỉnh các trường này để thêm hoặc xóa trạng thái chỉ đọc hoặc sử dụng trải nghiệm dựa trên nhiệm vụ khác (TBX) để chỉnh sửa hàng hoặc ô editing. Các trường này giờ bị ràng buộc với giá trị tĩnh.


> [!NOTE] 
> Cả hai tùy chọn đều sẽ loại bỏ một số bộ lọc dùng ngay cho các thực thể **Dự án** và **Nhiệm vụ dự án**, để tất cả các dạng xem tra cứu cho các thực thể này sẽ được hiển thị. Ban đầu, chỉ có dạng xem tra cứu phù hợp mới hiển thị.

Xác định dòng tác vụ phù hợp cho trường tùy chỉnh. Nếu bạn đã thêm trường vào lưới, thì trường đó sẽ chuyển vào dòng tác vụ sửa hàng được dùng cho các trường áp dụng cho toàn bộ hàng mục nhập thời gian. Nếu trường tùy chỉnh có giá trị duy nhất mỗi ngày, chẳng hạn như trường tùy chỉnh cho **Thời gian kết thúc**, thì trường đó sẽ chuyển vào luồng nhiệm vụ chỉnh sửa ô.

Để thêm trường tùy chỉnh vào một luồng nhiệm vụ, hãy kéo thành phần **Trường** vào vị trí thích hợp trên trang, sau đó đặt thuộc tính cho trường đó. Đặt thuộc tính **Nguồn** thành **Mục nhập thời gian** và đặt thuộc tính **Trường dữ liệu** thành trường tùy chỉnh. Thuộc tính **Trường** chỉ định tên hiển thị trên trang TBX. Chọn **Áp dụng** để lưu các thay đổi của bạn vào trường, sau đó chọn **Cập nhật** để lưu các thay đổi của bạn vào trang.

Để sử dụng trang TBX tùy chỉnh mới, hãy tạo một quy trình mới. Đặt danh mục thành **Luồng quy trình công việc**, đặt thực thể thành **Mục nhập thời gian** và đặt loại quy trình công việc thành **Chạy quy trình dưới dạng luồng nhiệm vụ**. Trong phần **Thuộc tính**, phải đặt thuộc tính **Tên trang** thành tên hiển thị cho trang. Thêm tất cả các trường liên quan vào trang TBX. Lưu và kích hoạt quy trình. Cập nhật thuộc tính điều khiển tùy chỉnh cho dòng tác vụ liên quan thành giá trị **Tên** trên quy trình.

### <a name="add-new-option-set-values"></a>Thêm các giá trị bộ tùy chọn mới
Để thêm các giá trị bộ tùy chọn vào một trường dùng ngay, hãy mở trang sửa cho trường đó và trong **Loại**, hãy chọn **Sửa** bên cạnh bộ tùy chọn. Thêm tùy chọn mới có nhãn và màu tùy chỉnh. Nếu bạn muốn thêm trạng thái mục nhập thời gian mới, thì trường dùng ngay phải được đặt tên là **Trạng thái mục nhập** chứ không phải là **Trạng thái**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Chỉ định trạng thái mục nhập thời gian mới là chỉ đọc
Để chỉ định trạng thái mục nhập thời gian mới thành chỉ đọc, hãy thêm giá trị mục nhập thời gian mới vào thuộc tính **Danh sách trạng thái chỉ đọc**. Phần có thể chỉnh sửa của lưới mục nhập thời gian sẽ bị khóa cho các hàng có trạng thái mới.
Tiếp theo, hãy thêm các quy tắc công việc để khóa tất cả các trường trên trang TBX **Chỉnh sửa hàng mục nhập thời gian** và **Chỉnh sửa mục nhập thời gian**. Bạn có thể truy cập các quy tắc công việc cho những trang này bằng cách mở công cụ biên tập dòng quy trình công việc cho trang rồi chọn **Quy tắc công việcBusiness Rules**. Sau đó, bạn có thể thêm trạng thái mới vào điều kiện trong các quy tắc kinh doanh hiện có hoặc có thể thêm quy tắc công việc mới cho trạng thái mới.

### <a name="add-custom-validation-rules"></a>Thêm quy tắc xác thực tùy chỉnh
Có hai loại quy tắc xác thực mà bạn có thể thêm cho trải nghiệm lưới mục nhập thời gian hằng tuần:

- Các quy tắc công việc phía khách hàng hoạt động trong hộp thoại tạo nhanh và trên các trang TBX.
- Xác thực phần bổ trợ phía máy chủ áp dụng cho tất cả bản cập nhật mục nhập thời gian.

#### <a name="business-rules"></a>Quy tắc kinh doanh
Sử dụng quy tắc công việc để khóa và mở khóa các trường, nhập giá trị mặc định vào trường và xác định các quy tắc xác thực chỉ yêu cầu thông tin từ bản ghi mục nhập thời gian hiện tại. Bạn có thể truy cập các quy tắc công việc cho trang TBX bằng cách mở công cụ biên tập dòng quy trình công việc cho trang rồi chọn **Quy tắc công việc**. Sau đó, bạn có thể chỉnh sửa quy tắc công việc hiện có hoặc thêm quy tắc kinh doanh mới. Để có các quy tắc xác thực mang tính tùy chỉnh hơn, bạn có thể sử dụng quy tắc công việc để chạy JavaScript.

#### <a name="plug-in-validations"></a>Xác thực bổ trợ
Sử dụng các mục xác thực phần bổ trợ đối với mọi mục xác thực yêu cầu có nhiều thông tin bối cảnh hơn mức có sẵn trong một bản ghi mục nhập thời gian hoặc đối với bất kỳ mục xác thực nào mà bạn muốn chạy trên các phần cập nhật nội tuyến trong lưới. Để hoàn tất quy trình xác thực, hãy tạo một phần bổ trợ trên thực thể **Mục nhập thời gian**.

### <a name="copying-time-entries"></a>Sao chép mục nhập thời gian
Sử dụng dạng xem **Sao chép cột mục nhập thời gian** để xác định danh sách các trường sẽ sao chép trong quá trình nhập thời gian. **Ngày** và **Khoảng thời gian** là các trường bắt buộc và không nên bị loại bỏ khỏi dạng xem.


[!INCLUDE[footer-include](../includes/footer-banner.md)]