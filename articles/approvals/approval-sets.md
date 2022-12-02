---
title: Các bộ phê duyệt
description: Bài viết này giải thích cách làm việc với các bộ phê duyệt, yêu cầu và tập hợp con các thao tác đó.
author: stsporen
ms.date: 02/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: ca205073edbce2b399aab3ae273d635c8af96765
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524943"
---
# <a name="approval-sets"></a>Các bộ phê duyệt

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Bộ phê duyệt có tác dụng nhóm các yêu cầu phê duyệt lại với nhau thành các tập hợp thao tác nhỏ hơn. Việc nhóm này cho phép xử lý các phê duyệt theo dự án, theo một thứ tự cụ thể đồng thời cho phép thử lại và sắp xếp theo trình tự. Việc nhóm các yêu cầu phê duyệt lại với nhau giúp cải thiện độ tin cậy và khả năng truy xuất nguồn gốc của việc xử lý phê duyệt đối với khối lượng phê duyệt lớn.

Các bộ phê duyệt cho biết trạng thái xử lý tổng thể của các bản ghi liên quan. Khi một bản ghi phê duyệt được xử lý bằng cách sử dụng một bộ phê duyệt, bản ghi sẽ chuyển từ **Đã gửi** sang **Đã phê duyệt** và không còn được liên kết với bộ phê duyệt. Nếu bản ghi đã gửi không được phê duyệt, thì bản ghi đó vẫn ở trạng thái **Đã gửi** và bộ phê duyệt được đánh dấu là không thành công. Bộ phê duyệt ghi lại thông báo lỗi về sự thất bại đó.

## <a name="processing-approvals-and-approval-sets"></a>Xử lý mục phê duyệt và bộ phê duyệt
Các mục phê duyệt được xếp hàng đợi để xử lý sẽ xuất hiện ở dạng xem **Xử lý mục phê duyệt**. Hệ thống xử lý không đồng bộ tất cả các mục nhập nhiều lần, bao gồm cả việc thử lại phê duyệt nếu các lần thử trước không thành công.

Trường **Thời gian tồn tại của bộ phê duyệt** ghi lại số lần thử còn lại để xử lý bộ phê duyệt trước khi mục này được đánh dấu là không thành công.

Bộ phê duyệt được xử lý thông qua việc kích hoạt định kỳ dựa trên **Dòng đám mây** có tên **Project Service - Lập lịch trình định kỳ Bộ phê duyệt dự án**. Điều này được tìm thấy trong **Giải pháp** được đặt tên **Project Operations**. 

Đảm bảo rằng dòng được kích hoạt bằng cách hoàn thành các bước sau.

1. Với tư cách là quản trị viên, hãy đăng nhập vào [flow.microsoft.com](https://powerautomate.microsoft.com).
2. Ở góc trên bên phải, chuyển sang môi trường mà bạn sử dụng cho Dynamics 365 Project Operations.
3. Chọn **Giải pháp** để liệt kê các giải pháp được cài đặt trong môi trường.
4. Trong danh sách giải pháp, hãy chọn **Project Operations**.
5. Thay đổi bộ lọc từ **Tất cả** thành **Dòng đám mây**.
6. Xác minh rằng dòng **Project Service – Lập lịch trình định kỳ Bộ phê duyệt dự án** được đặt thành **Bật**. Nếu không, chọn dòng rồi chọn **Bật**.
7. Xác minh rằng quá trình xử lý diễn ra sau mỗi năm phút bằng cách xem xét danh sách **Công việc hệ thống** trong khu vực **Cài đặt** trong môi trường Project Operations Dataverse của bạn.

## <a name="failed-approvals-and-approval-sets"></a>Mục phê duyệt và bộ phê duyệt không thành công
Dạng xem **Phê duyệt không thành công** liệt kê tất cả các phê duyệt yêu cầu sự can thiệp của người dùng. Hãy mở nhật ký bộ phê duyệt được liên kết để xác định nguyên nhân của sự thất bại.
Thao tác chọn **Thử lại** sẽ tăng số lần trong thời gian tồn tại của bộ phê duyệt, chuyển bộ phê duyệt trở lại trạng thái **Đang xử lý** và cố gắng xử lý các bản ghi còn lại.

## <a name="configure-approval-sets"></a>Đặt cấu hình bộ phê duyệt

### <a name="enable-the-approval-sets-feature"></a>Bật tính năng Bộ phê duyệt
Trước khi bạn bật tính năng Bộ phê duyệt, hãy xác minh rằng không có mục phê duyệt nào hiện đang được xử lý. Sau khi tính năng này được kích hoạt thì sẽ không thể vô hiệu hóa.

- Chuyển đến trang **Thông số dự án** và chọn **Kiểm soát tính năng** > **Bật phê duyệt hiện đại**.

### <a name="configuring-the-asynchronous-threshold"></a>Định cấu hình ngưỡng không đồng bộ 
Khi các bộ phê duyệt được tạo, quá trình xử lý sẽ chuyển sang nền khi số lượng bản ghi đã chọn để phê duyệt vượt quá ngưỡng được chỉ định. Sử dụng trường **Ngưỡng không đồng thời** để đặt cấu hình khi nào hoạt động xử lý phê duyệt nên chạy đồng bộ hoặc không đồng bộ. Chọn một trong các giá trị sau:

  - Không: Tất cả các yêu cầu phải được xử lý không đồng bộ. 
  - Số lớn hơn 0: Các mục phê duyệt chỉ được xử lý không đồng bộ khi số lượng mục phê duyệt đã gửi vượt quá giá trị này.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
