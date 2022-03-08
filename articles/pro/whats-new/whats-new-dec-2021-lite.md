---
title: Có gì mới vào tháng 12 năm 2021 - Triển khai Project Operations Lite
description: Chủ đề này cung cấp thông tin về các bản cập nhật chất lượng có trong bản triển khai Project Operations lite vào tháng 12 năm 2021.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0432e2d4970c352e91cca589987bbdace57c6eaf
ms.sourcegitcommit: 9d20e7738cce195d344f5925a115741a1ce3ca36
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 12/21/2021
ms.locfileid: "7943003"
---
# <a name="whats-new-december-2021---project-operations-lite-deployment"></a>Có gì mới vào tháng 12 năm 2021 - Triển khai Project Operations Lite

_Áp dụng cho: Bản triển khai giản đơn - từ thỏa thuận đến lập hóa đơn ước giá_

Chủ đề này áp dụng cho các thành phần và phiên bản sau của Microsoft Dynamics 365 Project Operations:

- Hoạt động dự án trong một Dataverse phiên bản môi trường 4.27.0.195, 4.27.0.242


## <a name="features-included-in-this-release"></a>Các tính năng có trong bản phát hành này

### <a name="subcontract-management"></a>Quản lý hợp đồng phụ 

- [Hợp đồng phụ các thành viên trong nhóm dự án](../subcontracting/subcontracting-project-team-members.md) : Người quản lý dự án có thể tạo các thành viên nhóm có tên hoặc chung chung với các hợp đồng phụ và các dòng hợp đồng phụ để tác động đến việc lập nhân viên và ước tính.
- [Các tùy chọn hợp đồng phụ cho các thành viên trong nhóm dự án](../subcontracting/subcon-options.md) : Khi đưa ra lựa chọn nhân sự cho các thành viên nhóm dự án có tên hoặc chung chung, người quản lý dự án có thể xem xét các hợp đồng phụ hiện có hoặc tạo các hợp đồng phụ mới cho một hoặc nhiều thành viên trong nhóm dự án. 
- [Ước tính chi phí của các nhiệm vụ tài nguyên được hợp đồng phụ](../subcontracting/costing-subcon-ra.md) : Việc ước tính chi phí dự án sẽ tính đến việc phân công nguồn lực theo hợp đồng phụ và sẽ tính chi phí cho chúng bằng cách sử dụng bảng giá mua liên quan đến các hợp đồng phụ. 
- [Định cấu hình Bảng lịch trình để hiển thị công nhân hợp đồng và năng lực của hợp đồng phụ](../subcontracting/configure-sb-subcon.md) : Bảng lịch trình trong Hoạt động dự án giờ đây có thể được định cấu hình để tìm kiếm và đề xuất loại tài nguyên có thể đặt trước và năng lực được hợp đồng phụ của nhân viên theo hợp đồng cùng với nhân viên. Cấu hình này có thể được áp dụng khi tìm kiếm tài nguyên trong bối cảnh nhân sự cho một yêu cầu dự án cụ thể hoặc khi tìm kiếm bên ngoài ngữ cảnh của một yêu cầu dự án.
- [Nhân sự cho một dự án với công nhân hợp đồng và năng lực của hợp đồng phụ](../subcontracting/staffing-cw.md) : Giờ đây, công nhân hợp đồng có thể được đặt trên các dự án tận dụng kinh nghiệm của bảng tiến độ.
- [Ghi lại thời gian, chi phí và việc sử dụng vật liệu trong các dự án cho các thành phần được thầu phụ](../subcontracting/recording-subcon-actuals.md) : Nhân viên hợp đồng có thể ghi lại thời gian và chi phí, đồng thời các thành viên trong nhóm dự án cũng có thể ghi lại việc sử dụng các vật liệu được mua bằng cách sử dụng hợp đồng phụ trong một dự án. Điều này sẽ dẫn đến việc ghi nhận chi phí chính xác đối với các dự án sử dụng năng lực hoặc vật liệu đã mua.
- [Chuyển đổi trạng thái trên một hợp đồng phụ](../subcontracting/subcon-states.md) : Các hợp đồng phụ có thể được xác nhận để hoàn tất thương lượng với nhà cung cấp, được đóng để cho biết đã hoàn thành giao hàng hoặc bị hủy để cho biết việc chấm dứt hợp đồng với nhà cung cấp trước khi hoàn thành giao hàng.

### <a name="task-planning"></a>Lập kế hoạch Nhiệm vụ
- Cải thiện xử lý sự cố cho quản trị viên hệ thống. Khi người dùng không thể mở dự án, quản trị viên có thể xem lại các lỗi liên quan đến không có giấy phép được tạo từ Dự án cho web trong [Nhật ký lập lịch dự án](../../project-management/schedule-api-logs.md).
- [Sử dụng danh sách kiểm tra tác vụ trong Microsoft Project cho web](https://support.microsoft.com/en-us/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c). Trong Microsoft Project cho web, bạn có thể thêm danh sách kiểm tra vào một công việc để theo dõi các mục cụ thể.

## <a name="quality-updates"></a>Bản cập nhật chất lượng

| **Lĩnh vực tính năng** | **Số tham chiếu** | **Cập nhật chất lượng** |
| --- | --- | --- |
| Hoạch định và theo dõi dự án | 2392596 | Lập lịch API hiện cho phép cập nhật **Nỗ lực còn lại**, **lực đã hoàn thành**, và **% Hoàn chỉnh** lĩnh vực. |
| Hoạch định và theo dõi dự án | 2478497 | Lập lịch các API **Số hoạt động** và **ID công việc** Các trường có thể để trống trên đầu vào vì hệ thống sẽ điền chúng bằng cách đánh số tự động.|
| Thời gian và Chi phí | 2468135 | Số lần thử phê duyệt lại giảm từ năm xuống còn ba. |
| Thời gian và Chi phí | 2468188 | Đã khắc phục sự cố với văn bản nhật ký vượt quá độ dài tối đa trong **notetext** thuộc tính của **chú thích** thực thể. |
