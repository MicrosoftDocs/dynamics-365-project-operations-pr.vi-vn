---
title: Hành vi trên giao diện người dùng của mục nhập thời gian
description: Chủ đề này cung cấp thông tin về hành vi trên giao diện người dùng của mục nhập thời gian.
author: stsporen
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 8719e2f9ee4867f17ed75142eca2115f61e37999
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124529"
---
# <a name="time-entry-ui-behavior"></a>Hành vi trên giao diện người dùng của mục nhập thời gian

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_


Lưới **Mục nhập thời gian hàng tuần** là kiểm soát tùy chỉnh có thanh công cụ và hai phần chính **Thông số** và **Khoảng thời gian**.

## <a name="dimensions"></a>Chiều
Phần **Thông số** hiển thị các thông số có thể nhập được thời gian vào đó. Các thông số sau đây được hỗ trợ ngay lập tức:

  - Dự án
  - Nhiệm vụ dự án
  - Vai trò
  - Loại
  - Trạng thái Mục nhập

Phần **Thông số** không cho phép chỉnh sửa nội tuyến. Phần này được hỗ trợ bởi một dạng xem cho phép thêm các trường tùy chỉnh vào lưới mục nhập thời gian hàng tuần.

## <a name="duration"></a>Thời lượng
Phần Thời gian hiển thị các ngày trong tuần dưới dạng tiêu đề cột. Phần này cho phép chỉnh sửa nội tuyến. Sau khi hàng mục nhập thời gian được tạo có các thông số phù hợp, người dùng có thể nhanh chóng nhập khoảng thời gian mà họ đã dành cho các thông số đó.

## <a name="create-a-new-time-entry"></a>Tạo mục nhập thời gian mới

1. Trong lưới mục nhập thời gian, hãy chọn **Mới**. 
2. Trong hộp thoại **Tạo nhanh mục nhập thời gian**, hãy chọn ngày nhập thời gian.
3. Nhập dữ liệu cho các thông số **Dự án**, **Nhiệm vụ dự án**, **Vai trò** và **Khoảng thời gian**. Thông tin này sẽ được thêm vào theo phút, giờ hoặc ngày bằng cách nhập **giờ**, **phút** hoặc **ngày** cùng với số. 
4. Nhập mô tả cho mục nhập và mọi nhận xét có thể được chia sẻ bên ngoài về mục nhập thời gian. 

Khi bạn lưu mục nhập, các giá trị đã nhập sẽ xuất hiện trong phần **Thông số**. Thông tin đã nhập trong trường **Khoảng thời gian** sẽ xuất hiện vào ngày tạo mục nhập thời gian.

Trường tìm kiếm được các dạng xem hệ thống hỗ trợ. Ví dụ: sau khi người dùng nhập một dự án, trường **nhiệm vụ dự án** được đặt thành dạng xem **Sao chép** theo mặc định. Để tạo mục nhập thời gian cho các nhiệm vụ không được gán cho người dùng, hãy chọn **Thay đổi dạng xem** trong hộp thoại tra cứu, sau đó chọn dạng xem **Tất cả nhiệm vụ dự án đang hoạt động**.

## <a name="edit-a-time-entry"></a>Chinh sửa mục nhập thời gian 
Thông tin chi tiết từ một số nguồn trên trang mục nhập thời gian, chẳng hạn như **Mô tả** và **Nhận xét bên ngoài**, không được hiển thị trong lưới mục nhập thời gian hàng tuần. Thay vào đó, một chỉ báo hình tham giác nhỏ sẽ xuất hiện trong các ô **Khoảng thời gian** có thông tin chi tiết bổ sung. 

1. Để chỉnh sửa mục nhập thời gian, hãy chọn ô bạn muốn cập nhật trong mục nhập thời gian.
2. Chọn **Chỉnh sửa chi tiết** để cập nhật dữ liệu trong ngăn **Biểu mẫu chính của mục nhập thời gian**. 

## <a name="copy-a-time-entry-row"></a>Sao chép hàng mục nhập thời gian
Sau khi hàng đã được tạo, bạn có thể chọn **Sao chép hàng** để sao chép toàn bộ hàng vào một hàng mới. Khi một hàng được sao chép theo cách này, các thông số và khoảng thời gian cũng được sao chép. Bạn cũng có thể chọn **Chỉnh sửa hàng** để cập nhật các giá trị thông số và khoảng thời gian trong phần **Khoảng thời gian**.

## <a name="open-a-time-entry-behavior"></a>Mở một hành vi mục nhập thời gian
Để hỗ trợ mục nhập tối ưu và nhanh chóng trong các trường nổi bật nhất, lưới mục nhập thời gian hàng tuần hiển thị tập hợp con của các thông số và khoảng thời gian đã chọn. Để xem tất cả thông tin chi tiết của một mục nhập thời gian, trong mục **Chỉnh sửa mục nhập**, hãy chọn **Mở**.

## <a name="submit-a-time-entry"></a>Gửi một mục nhập thời gian
Bạn có thể gửi một mục nhập thời gian duy nhất hoặc một nhóm mục nhập thời gian bằng cách chọn một khối ô hoặc toàn bộ hàng mục nhập thời gian rồi chọn **Gửi**. Các mục nhập thời gian đã gửi xuất hiện dưới dạng các mục nhập đang chờ phê duyệt trên trang **Phê duyệt** của người phê duyệt. Không thể chỉnh sửa các mục nhập thời gian sau khi đã gửi thành công.

## <a name="recall-a-time-entry"></a>Lấy lại mục nhập thời gian
Bạn có thể lấy lại các mục nhập thời gian mà mình đã gửi. Bạn có thể lấy lại một mục nhập thời gian duy nhất, một khối mục nhập thời gian hoặc toàn bộ hàng mục nhập thời gian. Bạn có thể chỉnh sửa các mục nhập thời gian đã thu hồi.

## <a name="time-entry-status"></a>Trạng thái mục nhập thời gian

- **Bản nháp**: Các mục nhập thời gian mới được tự động gán trạng thái **Bản nháp**. Chỉ có thể xóa các mục nhập thời gian có trạng thái **Bản nháp**.
- **Đã gửi**: Khi một mục nhập thời gian được gửi, trạng thái sẽ được cập nhật thành **Đã gửi**. 
- **Đã phê duyệt**: Khi một mục nhập thời gian đã gửi được phê duyệt, trạng thái sẽ được cập nhật thành **Đã phê duyệt**. 
- **Đã trả về**: Nếu một mục nhập thời gian bị từ chối, trạng thái sẽ được cập nhật thành **Đã trả về** và mục nhập này sẽ có sẵn để sửa chữa và gửi lại. 

## <a name="view-rejection-comments"></a>Xem các nhận xét từ chối
Khi người phê duyệt từ chối một mục nhập thời gian, họ có thể thêm nhận xét để nguồn lực hiểu được lý do từ chối. Để xem các nhận xét từ chối cho một mục nhập thời gian, hãy chọn **Mở mục nhập**. Nhận xét từ chối sẽ được hiển thị trong tiến trình thời gian. Người dùng có thể trả lời các nhận xét từ chối trước khi họ gửi lại mục nhập.

## <a name="copy-week"></a>Sao chép tuần
Sau khi tạo một vài mục nhập thời gian, người dùng có thể tạo nhiều mục nhập thời gian cùng một lúc.

1. Trong biểu mẫu **Mục nhập thời gian**, hãy chọn **Sao chép tuần** để tạo hàng loạt các mục nhập thời gian bổ sung. 
2. Trong hộp thoại **Sao chép** trong phần **Từ khoảng thời gian**, hãy sử dụng các trường **Ngày bắt đầu** và **Ngày kết thúc** để xác định phạm vi ngày sẽ sao chép mục nhập thời gian từ đó. 
3. Trong phần **Tới khoảng thời gian**, trong trường **Ngày bắt đầu**, hãy chỉ định ngày để tạo mục nhập thời gian. 
4. Chọn **Sao chép**. Đối với ngày đã chỉ định trong **khoảng thời gian Tới**, một bản sao của các mục nhập thời gian cho ngày tương ứng trong tuần trong **khoảng thời gian Từ** sẽ được tạo ra. Ví dụ: mục nhập thời gian của thứ Hai tuần trước được sao chép vào thứ Hai của tuần được chỉ định là **khoảng thời gian Tới**.

## <a name="import"></a>Nhập
Quá trình cơ bản tương tự được dùng để nhập từ các thông tin đặt trước, nội dung chỉ định và thông tin trao đổi. Bạn có thể chỉ định phạm vi ngày mà mục đặt trước được nhập từ đó, sau đó chọn rõ ràng các mục đặt trước cần được sao chép vào mục nhập thời gian nháp. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]