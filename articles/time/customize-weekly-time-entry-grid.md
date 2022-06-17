---
title: Kéo dài mục nhập thời gian
description: Bài viết này cung cấp thông tin về cách các nhà phát triển có thể mở rộng kiểm soát mục nhập thời gian.
author: stsporen
ms.date: 01/27/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 7ed501af3fb2059ab3c3ab6f6c957fe518595d55
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914796"
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
Mỗi mục nhập thời gian được liên kết với một bản ghi nguồn thời gian. Bản ghi này xác định ứng dụng nào nên xử lý mục nhập thời gian và cách thức.

Các mục nhập thời gian luôn là một khối thời gian liền kề có liên kết bắt đầu, kết thúc và khoảng thời gian.

Logic sẽ tự động cập nhật bản ghi mục nhập thời gian trong các trường hợp sau:

- Nếu hai trong ba trường sau được cung cấp, thì trường thứ ba sẽ được tính toán tự động: 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- Các **msdyn_start** và **msdyn_end** các trường nhận biết múi giờ.
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

1. Thêm trường tùy chỉnh vào **Tạo nhanh** hộp thoại.
2. Cấu hình lưới để hiển thị trường tùy chỉnh.
3. Thêm trường tùy chỉnh vào **Hàng sửa** hoặc **Mục nhập thời gian** trang, nếu thích hợp.

Đảm bảo rằng trường mới có các xác thực bắt buộc trên **Hàng sửa** hoặc **Mục nhập thời gian** trang. Là một phần của nhiệm vụ này, hãy khóa trường, dựa trên trạng thái của mục nhập thời gian.

Khi bạn thêm trường tùy chỉnh vào **Mục nhập thời gian** lưới và sau đó tạo các mục thời gian trực tiếp trong lưới, trường tùy chỉnh cho các mục đó sẽ tự động được đặt sao cho khớp với hàng. 

### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Thêm trường tùy chỉnh vào hộp thoại Tạo nhanh
Thêm trường tùy chỉnh vào **Tạo nhanh: Tạo mục nhập thời gian** hộp thoại. Sau đó, người dùng có thể nhập một giá trị khi họ thêm các mục nhập thời gian bằng cách chọn **Mới**.

### <a name="configure-the-grid-to-show-the-custom-field"></a>Cấu hình lưới để hiển thị trường tùy chỉnh
Có hai cách để thêm trường tùy chỉnh vào **Mục nhập thời gian hàng tuần** lưới điện.

- Tùy chỉnh **Mục thời gian hàng tuần của tôi** xem và thêm trường tùy chỉnh vào đó. Bạn có thể chỉ định vị trí và kích thước của trường tùy chỉnh trong lưới bằng cách chỉnh sửa các thuộc tính trong dạng xem.
- Tạo một dạng xem mục nhập thời gian tùy chỉnh mới và đặt nó làm dạng xem mặc định. Chế độ xem này phải chứa **Sự mô tả** và **Bình luận bên ngoài** ngoài các cột mà bạn muốn lưới bao gồm. Bạn có thể chỉ định vị trí, kích thước và thứ tự sắp xếp mặc định của lưới bằng cách chỉnh sửa các thuộc tính trong dạng xem. Tiếp theo, cấu hình bộ kiểm soát tùy chỉnh cho dạng xem này để trở thành bộ kiểm soát **Lưới mục nhập thời gian**. Thêm điều khiển vào dạng xem và chọn nó cho **Web**, **thoại**, và **Máy tính bảng**. Tiếp theo, định cấu hình các thông số cho **Mục nhập thời gian hàng tuần** lưới điện. Đặt **Ngày bắt đầu** lĩnh vực để **msdyn\_ ngày**, đặt **Khoảng thời gian** lĩnh vực để **msdyn\_ khoảng thời gian** và đặt **Trạng thái** lĩnh vực để **msdyn\_ entrystatus**. Các **Danh sách trạng thái chỉ đọc** trường được đặt thành **192350002 (Được chấp thuận)**, **(đã đệ trình)**, hoặc **192350004 (Đã yêu cầu thu hồi)**.

### <a name="add-the-custom-field-to-the-appropriate-edit-page"></a>Thêm trường tùy chỉnh vào trang chỉnh sửa thích hợp
Bạn có thể tìm thấy các trang được sử dụng để chỉnh sửa mục nhập thời gian hoặc một hàng mục nhập thời gian trong **Các hình thức**. Các **Chỉnh sửa mục nhập** nút trong lưới mở ra **Chỉnh sửa mục nhập** trang và **Chỉnh sửa hàng** nút mở **Hàng sửa** trang. Bạn có thể chỉnh sửa các trang này để chúng bao gồm các trường tùy chỉnh.

Cả hai tùy chọn đều loại bỏ một số tính năng lọc ngoài hộp trên **Dự án** và **Nhiệm vụ dự án** các thực thể, để tất cả các chế độ xem tra cứu cho các thực thể đều có thể nhìn thấy được. Ban đầu, chỉ có dạng xem tra cứu phù hợp mới hiển thị.

Bạn phải xác định trang thích hợp cho trường tùy chỉnh. Rất có thể, nếu bạn đã thêm trường vào lưới, trường đó sẽ chuyển sang **Hàng sửa** trang được sử dụng cho các trường áp dụng cho toàn bộ hàng mục thời gian. Nếu trường tùy chỉnh có một giá trị duy nhất trong hàng mỗi ngày (ví dụ: nếu đó là trường tùy chỉnh cho thời gian kết thúc), thì nó sẽ chuyển sang **Mục nhập thời gian** trang.

Để thêm trường tùy chỉnh vào một trang, hãy kéo **Đồng ruộng** vào vị trí thích hợp trên trang, rồi đặt các thuộc tính của nó.

### <a name="add-new-option-set-values"></a>Thêm các giá trị bộ tùy chọn mới
Để thêm giá trị bộ tùy chọn vào trường bên ngoài, hãy làm theo các bước sau.

1. Mở trang chỉnh sửa cho trường, sau đó, trong **Loại hình**, lựa chọn **Chỉnh sửa** bên cạnh bộ tùy chọn.
2. Thêm tùy chọn mới có nhãn và màu tùy chỉnh. Nếu bạn muốn thêm một trạng thái nhập thời gian mới, trường ngoài hộp được đặt tên **Trạng thái đầu vào**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Chỉ định trạng thái mục nhập thời gian mới là chỉ đọc
Để chỉ định trạng thái mục nhập thời gian mới thành chỉ đọc, hãy thêm giá trị mục nhập thời gian mới vào thuộc tính **Danh sách trạng thái chỉ đọc**. Đảm bảo thêm số chứ không phải nhãn. Giờ đây, phần có thể chỉnh sửa của lưới mục nhập thời gian sẽ bị khóa đối với các hàng có trạng thái mới. Để thiết lập **Danh sách trạng thái chỉ đọc** tài sản khác nhau cho khác nhau **Thời gian nhập cảnh** lượt xem, thêm **Mục nhập thời gian** lưới trong một chế độ xem **Kiểm soát tùy chỉnh** và định cấu hình các thông số sao cho phù hợp.

Tiếp theo, thêm các quy tắc kinh doanh để khóa tất cả các trường trên **Hàng sửa** và **Mục nhập thời gian** các trang. Để truy cập các quy tắc kinh doanh cho các trang này, hãy mở công cụ biên tập biểu mẫu cho mỗi trang, sau đó chọn **Quy tắc kinh doanh**. Sau đó, bạn có thể thêm trạng thái mới vào điều kiện trong các quy tắc kinh doanh hiện có hoặc có thể thêm quy tắc công việc mới cho trạng thái mới.

### <a name="add-custom-validation-rules"></a>Thêm quy tắc xác thực tùy chỉnh
Bạn có thể thêm hai loại quy tắc xác thực cho **Mục nhập thời gian hàng tuần** trải nghiệm lưới:

- Các quy tắc kinh doanh phía khách hàng hoạt động trên các trang
- Xác thực trình cắm phía máy chủ áp dụng cho các bản cập nhật mục nhập mọi lúc

#### <a name="client-side-business-rules"></a>Quy tắc kinh doanh phía khách hàng
Sử dụng quy tắc công việc để khóa và mở khóa các trường, nhập giá trị mặc định vào trường và xác định các quy tắc xác thực chỉ yêu cầu thông tin từ bản ghi mục nhập thời gian hiện tại. Để truy cập các quy tắc kinh doanh cho một trang, hãy mở công cụ biên tập biểu mẫu, sau đó chọn **Nội quy kinh doanh**. Sau đó, bạn có thể chỉnh sửa quy tắc công việc hiện có hoặc thêm quy tắc kinh doanh mới.

#### <a name="server-side-plug-in-validations"></a>Xác thực trình cắm phía máy chủ
Bạn nên sử dụng xác thực trình cắm cho bất kỳ xác thực nào yêu cầu nhiều ngữ cảnh hơn khả dụng trong một bản ghi mục nhập thời gian duy nhất. Bạn cũng nên sử dụng chúng cho bất kỳ xác thực nào mà bạn muốn chạy trên các bản cập nhật nội tuyến trong lưới. Để hoàn tất quá trình xác thực, hãy tạo một trình cắm tùy chỉnh trên **Thời gian nhập cảnh** thực thể.

### <a name="limits"></a>Giới hạn
Hiện tại, **Mục nhập thời gian** lưới có giới hạn kích thước là 500 hàng. Nếu có nhiều hơn 500 hàng, các hàng thừa sẽ không được hiển thị. Không có cách nào để tăng giới hạn kích thước này.

### <a name="copying-time-entries"></a>Sao chép mục nhập thời gian
Sử dụng dạng xem **Sao chép cột mục nhập thời gian** để xác định danh sách các trường sẽ sao chép trong quá trình nhập thời gian. **Ngày** và **Khoảng thời gian** là các trường bắt buộc và không nên bị loại bỏ khỏi dạng xem.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
