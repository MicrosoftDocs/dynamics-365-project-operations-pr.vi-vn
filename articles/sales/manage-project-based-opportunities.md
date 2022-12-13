---
title: Quản lý cơ hội dự án
description: Bài viết này cung cấp thông tin về cách làm việc với các cơ hội có liên quan đến dự án.
author: rumant
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 56eba38476dd5b49f0043eee5d411d51f9bf56b8
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825358"
---
# <a name="manage-project-opportunities"></a>Quản lý cơ hội dự án

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Các công ty dựa trên dự án thường sắp xếp các hoạt động giao hàng của mình ở nhiều quốc gia và khu vực địa lý. Chi phí thực hiện dự án và giao hàng có thể thay đổi tùy theo khu vực địa lý hoặc bộ phận quản lý việc giao hàng. Ở chiều ngược lại, điều này cũng có thể ảnh hưởng đến lợi nhuận của thỏa thuận. Việc cung cấp dịch vụ dựa trên dự án thường tiêu tốn một lượng lớn thời gian của nguồn nhân lực, cùng với những khoản chi phí đáng kể cho việc đi lại, chi phí vật liệu và các chi phí khác.

Các cơ hội theo dự án trong Dynamics 365 Project Operations được thiết kế với phần mở rộng cho Dynamics 365 Sales. Bài viết cung cấp thông tin chi tiết về các trường và lô-gic kinh doanh khác nhau có trong chức năng bổ sung được các công ty dựa trên dự án yêu cầu để quản lý các cơ hội dựa trên dự án.

## <a name="view-all-project-based-opportunities"></a>Xem tất cả các cơ hội dựa trên dự án

Bạn có thể thấy một danh sách tất cả các cơ hội dựa trên dự án ở trang danh sách **Cơ hội**. 

1. Chuyển tới **Bán hàng** > **Cơ hội**.
2. Sử dụng **Bộ chuyển dạng xem** để chọn các chế độ đã lọc khác đối với cơ hội. Bạn có thể tạo dạng xem của riêng mình với các tiêu chí bộ lọc tùy chỉnh để đặt cấu hình các dạng xem và tùy chọn điều hướng này.

Cơ hội dự án có thể được tạo hoặc xóa khỏi trang danh sách này hoặc trang chi tiết.

## <a name="business-process-flow-for-project-based-deals"></a>Dòng quy trình công việc cho các thỏa thuận dựa trên dự án

Các dòng quy trình công việc sau được hỗ trợ cho những thỏa thuận dựa trên dự án trong Project Operations:

- Quy trình công việc từ khách hàng tiềm năng thành cơ hội
- Quy trình bán hàng từ cơ hội

### <a name="lead-to-opportunity-business-process"></a>Quy trình công việc từ khách hàng tiềm năng thành cơ hội 
Quy trình công việc từ khách hàng tiềm năng thành cơ hội hỗ trợ các giai đoạn sau:

| Trạng thái | Thực thể được ánh xạ | Chức năng |
| --- | --- | --- |
| Bao gồm | Khách hàng tiềm năng | Định tính khách hàng tiềm năng để tạo tài khoản, người liên hệ và cơ hội. |
| Phát triển | Cơ hội | Tạo cơ hội để bổ sung thêm thông tin về công việc liên quan, các bên liên quan chính và đối thủ cạnh tranh. |
| Đề xuất | Cơ hội | Xây dựng đề xuất và nhận sự phê duyệt của nhóm đánh giá nội bộ. |
| Đóng | Cơ hội | Giành được cơ hội để chốt thỏa thuận. |

### <a name="opportunity-sales-process"></a>Quy trình bán hàng từ cơ hội
Quy trình bán hàng Cơ hội trong Project Operations là phần mở rộng cho dòng quy trình công việc bán hàng Cơ hội trong ứng dụng Sales. Quy trình công việc này được thiết kế sẵn dùng để hỗ trợ các giai đoạn sau trong cơ hội dựa trên dự án.

| Trạng thái | Thực thể được ánh xạ | Chức năng |
| --- | --- | --- |
| Bao gồm | Cơ hội | Định tính khách hàng tiềm năng để tạo tài khoản, người liên hệ và cơ hội. |
| Đề xuất | Báo giá | Xây dựng đề xuất bằng báo giá dự án và nhận sự phê duyệt của nhóm đánh giá nội bộ. |
| Hợp đồng | Hợp đồng dự án | Giành được báo giá để tạo hợp đồng và bắt đầu thực hiện và giao hàng trên dự án. |
| Đóng | Hợp đồng dự án | Kết thúc công việc thành công và chốt hợp đồng dự án. |

> [!NOTE]
> Nếu thỏa thuận dựa trên dự án của bạn bắt đầu với Khách hàng tiềm năng, thì quy trình công việc từ Khách hàng tiềm năng thành cơ hội sẽ được ưu tiên.
>
> Nếu thỏa thuận dựa trên dự án của bạn bắt đầu với Cơ hội, thì quy trình bán hàng Cơ hội sẽ được ưu tiên.

Bạn có thể sửa dòng quy trình công việc cho sản phẩm hoặc tạo dòng quy trình công việc của riêng mình để theo dõi quy trình bán hàng khi cần. Để biết thêm thông tin về dòng quy trình công việc, hãy xem [Tổng quan về dòng quy trình công việc](/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
