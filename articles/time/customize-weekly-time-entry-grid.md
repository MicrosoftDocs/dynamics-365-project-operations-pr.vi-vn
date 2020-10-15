---
title: Kéo dài mục nhập thời gian
description: Chủ đề này cung cấp thông tin về cách các nhà phát triển có thể mở rộng kiểm soát mục nhập thời gian.
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 93f411ad7c86beefcc35e7799a03987dacdcd62b
ms.sourcegitcommit: 5a29adce48133e09f051929e8544d6c2c93c025d
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/02/2020
ms.locfileid: "3930906"
---
# <a name="extending-time-entries"></a>Kéo dài mục nhập thời gian

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Dynamics 365 Project Operations bao gồm điều khiển tùy chỉnh mục nhập thời gian có thể mở rộng. Điều khiển này bao gồm những tính năng sau đây:

- Nhập thời gian theo chiều ngang trong một tuần
- Tổng số theo ngày, hàng hoặc tuần
- Sao chép hàng hoặc tuần
- Mục nhập thời gian thông qua HH:mm hoặc HH.hh (tự động chuyển đổi thành HH.hh)
- Nhập từ phân công, đặt chỗ hoặc cuộc hẹn

Có thể kéo dài mục nhập thời gian trong hai lĩnh vực:
- [Thêm các mục nhập thời gian tùy chỉnh để sử dụng cho riêng bạn](#add)
- [Tùy chỉnh điều khiển mục nhập thời gian hằng tuần](#customize)

## <a name="add-custom-time-entries-for-your-own-use"></a><a name="add"></a>Thêm các mục nhập thời gian tùy chỉnh để sử dụng cho riêng bạn.

Mục nhập thời gian là một thực thể cốt lõi được thiết kế để sử dụng cho nhiều tình huống. Trong tháng 4 đợt 1 năm 2020, giải pháp cốt lõi TESA đã được giới thiệu, cung cấp thực thể **Thiết đặt** và một vai trò bảo mật **Người dùng mục nhập thời gian** mới. Các trường mới **msdyn_start** và **msdyn_end** có mối quan hệ trực tiếp với **msdyn_duration** cũng được bao gồm. Thực thể, vai trò bảo mật và các trường mới cho phép một cách tiếp cận thống nhất hơn về thời gian trên nhiều sản phẩm.


### <a name="time-source-entity"></a>Thực thể nguồn thời gian
| Trường | Nội dung mô tả | 
|-------|------------|
| Tên  | Tên của mục nhập Nguồn thời gian được sử dụng làm giá trị lựa chọn trong quá trình tạo mục nhập thời gian. |
| Nguồn thời gian mặc định [Nguồn thời gian: isdefault] | Theo mặc định, chỉ một Nguồn thời gian có thể được đánh dấu tại nguồn thời gian mặc định. Khả năng này cho phép các mục nhập mặc định thành nguồn thời gian nếu nguồn thời gian không được chỉ định. |
|Loại nguồn thời gian [Nguồn thời gian: sourcetype] | Loại nguồn là một tùy chọn (Loại nguồn mục nhập thời gian) cho phép liên kết nguồn thời gian với một ứng dụng. Các giá trị bổ sung sẽ được thêm vào bộ tùy chọn này khi các ứng dụng bổ sung được thêm vào. Lưu ý rằng Microsoft bảo lưu các giá trị lớn hơn 190.000.000.|


### <a name="time-entries-and-the-time-source-entity"></a>Mục nhập thời gian và thực thể nguồn thời gian
Mỗi mục nhập thời gian được liên kết với một bản ghi nguồn thời gian. Bản ghi này xác định cách thức và ứng dụng nào sẽ xử lý mục nhập thời gian.

Các mục nhập thời gian luôn là một khối thời gian liền kề có liên kết bắt đầu, kết thúc và khoảng thời gian.

Logic sẽ tự động cập nhật bản ghi mục nhập thời gian trong các trường hợp sau:

- Nếu hai trong ba trường sau được cung cấp, trường thứ ba được tính toán tự động 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- Các trường **msdyn_start** và **msdyn_end** phân biệt múi giờ.
- Các mục nhập thời gian được tạo với chỉ **msdyn_date** và **msdyn_duration** được chỉ định sẽ bắt đầu lúc nửa đêm và **msdyn_start** và **msdyn_end** sẽ được cập nhật tương ứng.

#### <a name="time-entry-types"></a>Loại mục nhập thời gian

Bản ghi mục nhập thời gian có một kiểu liên kết xác định hành vi trong luồng gửi cho ứng dụng được liên kết.

|Nhãn | Giá_trị|
|-----|-----|
|Trong thời gian nghỉ   |192,355,000|
|Di chuyển | 192,355,001|
|Làm thêm   | 192,354,320|
|Công việc   | 192,350,000|
|Vắng mặt    | 192,350,001|
|Kỳ nghỉ   | 192,350,002|



## <a name="customize-the-weekly-time-entry-control"></a><a name="customize"></a>Tùy chỉnh điều khiển mục nhập thời gian hằng tuần
Các nhà phát triển có thể thêm các trường và tra cứu bổ sung cho các thực thể khác, đồng thời triển khai các quy tắc kinh doanh tùy chỉnh để hỗ trợ các tình huống kinh doanh của họ.

### <a name="add-custom-fields-with-lookups-to-other-entities"></a>Thêm các trường tùy chỉnh có mục tra cứu cho thực thể khác
Có 3 bước chính để thêm trường tùy chỉnh vào lưới mục nhập thời gian hàng tuần.

- Thêm trường tùy chỉnh vào hộp thoại tạo nhanh.
- Cấu hình lưới để hiển thị trường tùy chỉnh.
- Thêm trường tùy chỉnh vào dòng tác vụ chỉnh sửa hàng hoặc dòng tác vụ chỉnh sửa ô.

Ngoài ra, bạn phải đảm bảo rằng trường mới có các xác thực bắt buộc trong hàng hoặc ô chỉnh sửa luồng nhiệm vụ. Trong bước này, bạn phải khóa trường theo trạng thái mục nhập thời gian.

#### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Thêm trường tùy chỉnh vào hộp thoại tạo nhanh
Bạn phải thêm trường tùy chỉnh vào hộp thoại **Tạo nhanh mục nhập thời gian**. Sau đó, người dùng có thể nhập một giá trị khi họ thêm các mục nhập thời gian bằng cách chọn **Mới**.

#### <a name="configure-the-grid-to-show-the-custom-field"></a>Cấu hình lưới để hiển thị trường tùy chỉnh
Có 2 cách để thêm trường tùy chỉnh vào lưới mục nhập thời gian hàng tuần:

  - Tùy chỉnh chế độ xem và thêm trường tùy chỉnh
  - Tạo mục nhập thời gian tùy chỉnh mặc định mới 


**Tùy chỉnh chế độ xem và thêm trường tùy chỉnh**

Bạn có thể tùy chỉnh dạng xem **Mục nhập thời gian hằng tuần của tôi** và thêm trường tùy chỉnh vào đó. Bạn có thể chọn vị trí và kích thước của trường tùy chỉnh trong lưới bằng cách chỉnh sửa các thuộc tính đó trong dạng xem.

**Tạo mục nhập thời gian tùy chỉnh mặc định mới** 

dạng xem này sẽ chứa các trường **Mô tả** và **Nhận xét bên ngoài**, ngoài các cột mà bạn muốn có trong lưới. 

1. Chọn vị trí, kích thước và thứ tự sắp xếp mặc định cho lưới bằng cách chỉnh sửa các thuộc tính đó trong dạng xem. 
2. Cấu hình bộ kiểm soát tùy chỉnh cho dạng xem này để trở thành bộ kiểm soát **Lưới mục nhập thời gian**. 
3. Thêm bộ kiểm soát này vào dạng xem và chọn cho web, điện thoại và máy tính bảng. 
4. Cấu hình các thông số cho lưới mục nhập thời gian hàng tuần. Đặt trường **Ngày bắt đầu** thành **msdyn_date**, đặt trường **Khoảng thời gian** thành **msdyn_duration** và đặt trường **Trạng thái** thành **msdyn_entrystatus**. 
5. Đối với dạng xem mặc định, trường **Danh sách trạng thái chỉ đọc** được đặt thành **192350002,192350003,192350004**, trường **Luồng nhiệm vụ chỉnh sửa hàng** được đặt thành **msdyn_timeentryrowedit** và trường **Luồng nhiệm vụ chỉnh sửa ô** được đặt thành **msdyn_timeentryedit**. 
6. Bạn có thể tùy chỉnh các trường này để thêm hoặc xóa trạng thái chỉ đọc hoặc sử dụng trải nghiệm dựa trên nhiệm vụ khác (TBX) để chỉnh sửa hàng hoặc ô editing. Các trường này sẽ bị ràng buộc với giá trị tĩnh.


> [!NOTE] 
> Cả hai tùy chọn đều loại bỏ một số tính năng lọc sẵn cho các thực thể **Dự án** và **nhiệm vụ dự án**, từ đó tất cả dạng xem tra cứu cho các thực thể này đều hiển thị. Ban đầu, chỉ có dạng xem tra cứu phù hợp mới hiển thị.
Bạn phải xác định luồng nhiệm vụ phù hợp cho trường tùy chỉnh. Nhiều khả năng, nếu bạn đã thêm trường vào lưới, trường đó sẽ chuyển vào luồng nhiệm vụ chỉnh sửa hàng được dùng cho các trường áp dụng cho toàn bộ hàng mục nhập thời gian. Nếu trường tùy chỉnh có giá trị duy nhất mỗi ngày, chẳng hạn như trường tùy chỉnh cho **Thời gian kết thúc**, thì trường đó sẽ chuyển vào luồng nhiệm vụ chỉnh sửa ô.

Để thêm trường tùy chỉnh vào một luồng nhiệm vụ, hãy kéo thành phần **Trường** vào vị trí thích hợp trên trang, sau đó đặt thuộc tính cho trường đó. Đặt thuộc tính **Nguồn** thành **Mục nhập thời gian** và đặt thuộc tính **Trường dữ liệu** thành trường tùy chỉnh. Thuộc tính **Trường** chỉ định tên hiển thị trên trang TBX. Chọn **Áp dụng** để lưu các thay đổi của bạn vào trường, sau đó chọn **Cập nhật** để lưu các thay đổi của bạn vào trang.

Để sử dụng trang TBX tùy chỉnh mới, hãy tạo một quy trình mới. Đặt danh mục thành **Luồng quy trình công việc**, đặt thực thể thành **Mục nhập thời gian** và đặt loại quy trình công việc thành **Chạy quy trình dưới dạng luồng nhiệm vụ**. Trong phần **Thuộc tính**, phải đặt thuộc tính **Tên trang** thành tên hiển thị cho trang. Thêm tất cả các trường liên quan vào trang TBX. Lưu và kích hoạt quy trình, sau đó cập nhật thuộc tính kiểm soát tùy chỉnh cho luồng nhiệm vụ liên quan thành giá trị **Tên** trên quy trình.

### <a name="add-new-option-set-values"></a>Thêm các giá trị bộ tùy chọn mới
Để thêm các giá trị bộ tùy chọn vào một trường sẵn có, hãy mở trang chỉnh sửa cho trường đó, sau đó trong **Loại**, hãy chọn **Chỉnh sửa** bên cạnh bộ tùy chọn. Tiếp theo, thêm tùy chọn mới có nhãn và màu tùy chỉnh. Nếu bạn muốn thêm trạng thái mục nhập thời gian mới, thì trường ban đầu phải được đặt tên là **Trạng thái mục nhập** chứ không phải là **Trạng thái**.

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
Bạn nên sử dụng các quy tắc xác thực bổ trợ đối với mọi quá trình xác thực yêu cầu nhiều ngữ cảnh hơn ngữ cảnh có sẵn trong một bản ghi mục nhập thời gian, hoặc bất kỳ quá trình xác thực nào mà bạn muốn chạy trên các bản cập nhật nội tuyến trong lưới. Để hoàn tất quy trình xác thực, hãy tạo một phần bổ trợ trên thực thể **Mục nhập thời gian**.
