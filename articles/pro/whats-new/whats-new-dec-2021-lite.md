---
title: Tính năng mới kể từ tháng 12 năm 2021 – triển khai bản đơn giản Project Operations
description: Bài viết này cung cấp thông tin về các bản cập nhật chất lượng có trong bản phát hành triển khai bản đơn giản Project Operations vào tháng 12 năm 2021.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 301acc5be76fb0318d6298820b62ae5bb05efac3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914106"
---
# <a name="whats-new-december-2021---project-operations-lite-deployment"></a>Tính năng mới kể từ tháng 12 năm 2021 – triển khai bản đơn giản Project Operations

_Áp dụng cho: Bản triển khai giản đơn - từ thỏa thuận đến lập hóa đơn ước giá_

Bài viết này áp dụng cho các phiên bản và thành phần sau của Microsoft Dynamics 365 Project Operations:

- Project Operations trong môi trường Dataverse phiên bản 4.27.0.195, 4.27.0.242, 4.27.0.244


## <a name="features-included-in-this-release"></a>Các tính năng có trong bản phát hành này

### <a name="subcontract-management"></a>Quản lý hợp đồng phụ 

- [Thực hiện hợp đồng phụ cho thành viên nhóm dự án](../subcontracting/subcontracting-project-team-members.md): Người quản lý dự án có thể tạo thành viên nhóm có tên hoặc chung với các hợp đồng phụ và các mô tả hợp đồng phụ để tác động đến việc bố trí nhân sự và ước tính.
- [Các tùy chọn hợp đồng phụ cho thành viên nhóm dự án](../subcontracting/subcon-options.md): Khi đưa ra lựa chọn bố trị nhân sự cho thành viên nhóm dự án có tên hoặc chung, người quản lý dự án có thể xem xét các hợp đồng phụ hiện có hoặc tạo các hợp đồng phụ mới cho một hoặc nhiều thành viên nhóm dự án. 
- [Ước tính chi phí của các phân công nguồn lực theo hợp đồng phụ](../subcontracting/costing-subcon-ra.md) : Việc ước tính chi phí dự án sẽ tính đến việc phân công nguồn lực theo hợp đồng phụ và sẽ tính chi phí cho chúng bằng cách sử dụng bảng giá mua được liên kết với các hợp đồng phụ. 
- [Định cấu hình Bảng lịch trình để hiển thị nhân viên hợp đồng và năng lực hợp đồng phụ](../subcontracting/configure-sb-subcon.md): Bảng lịch trình trong Project Operations hiện có thể được định cấu hình để tìm kiếm và đề xuất nhân viên hợp đồng thuộc loại nguồn lực có thể đặt và năng lực hợp đồng phụ cùng với nhân viên. Cấu hình này có thể được áp dụng khi tìm kiếm nguồn lực trong bối cảnh bố trị nhân sự cho một yêu cầu dự án cụ thể hoặc khi tìm kiếm bên ngoài bối cảnh của một yêu cầu dự án.
- [Bố trí nhân sự cho một dự án với nhân viên hợp đồng và năng lực của hợp đồng phụ](../subcontracting/staffing-cw.md): Các nhân viên hợp đồng hiện có thể được đặt trên các dự án bằng cách sử dụng trải nghiệm bảng lịch trình.
- [Ghi lại thời gian, chi phí và việc sử dụng vật tư trong các dự án cho các thành phần theo hợp đồng phụ](../subcontracting/recording-subcon-actuals.md): Nhân viên hợp đồng có thể ghi lại thời gian và chi phí, đồng thời các thành viên nhóm dự án cũng có thể ghi lại việc sử dụng các vật liệu được mua bằng cách sử dụng hợp đồng phụ trong một dự án. Điều này sẽ dẫn đến việc ghi nhận chi phí chính xác đối với các dự án sử dụng năng lực hoặc vật tư đã mua.
- [Chuyển tiếp trạng thái trên một hợp đồng phụ](../subcontracting/subcon-states.md): Các hợp đồng phụ có thể được xác nhận để hoàn thành thương lượng với nhà cung cấp, được đóng để cho biết đã hoàn thành bàn giao hoặc bị hủy để cho biết việc chấm dứt hợp đồng với nhà cung cấp trước khi hoàn thành bàn giao.

### <a name="task-planning"></a>Lên kế hoạch nhiệm vụ
- Khắc phục sự cố được cải thiện dành cho quản trị viên hệ thống. Khi người dùng không thể mở một dự án, quản trị viên có thể xem lại các lỗi liên quan đến việc không có giấy phép được tạo từ Project for the web trong [Nhật ký lập lịch dự án](../../project-management/schedule-api-logs.md).
- [Sử dụng danh sách kiểm tra nhiệm vụ trong Microsoft Project for the web](https://support.microsoft.com/en-us/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c). Trong Microsoft Project for the web, bạn có thể thêm danh sách kiểm tra vào một nhiệm vụ để theo dõi các mục cụ thể.

## <a name="quality-updates"></a>Bản cập nhật chất lượng

| **Lĩnh vực tính năng** | **Số tham chiếu** | **Cập nhật chất lượng** |
| --- | --- | --- |
| Hoạch định và theo dõi dự án | 2392596 | API Lịch trình giờ cho phép cập nhật các trường **Nỗ lực còn lại**, **Nỗ lực hoàn thành** và **% Hoàn thành**. |
| Hoạch định và theo dõi dự án | 2478497 | API lịch trình **Số hoạt động** và **ID công việc** có thể để trống trên đầu vào vì hệ thống sẽ điền chúng bằng cách đánh số tự động.|
| Thời gian và Chi phí | 2468135 | Số lần thử lại phê duyệt giảm từ năm xuống còn ba. |
| Thời gian và Chi phí | 2468188 | Đã khắc phục sự cố văn bản nhật ký vượt quá độ dài tối đa trong thuộc tính **notetext** của thực thể **chú thích**. |
