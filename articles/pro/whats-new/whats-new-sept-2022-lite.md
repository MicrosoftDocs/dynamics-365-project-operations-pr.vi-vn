---
title: Tính năng mới kể từ tháng 9 năm 2022 – triển khai bản đơn giản Project Operations
description: Bài viết này cung cấp thông tin về các bản cập nhật chất lượng có trong lần triển khai bản đơn giản của Microsoft Dynamics 365 Project Operations phát hành vào tháng 9 năm 2022.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: a02ac7a69489bc7974eb0e63c11fa5de74795b78
ms.sourcegitcommit: b3a70bc4f2850cff5c2b7114cff7bd61ec298143
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/06/2022
ms.locfileid: "9634879"
---
# <a name="whats-new-september-2022---project-operations-lite-deployment"></a>Tính năng mới kể từ tháng 9 năm 2022 – triển khai bản đơn giản Project Operations

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Bài viết này áp dụng cho các phiên bản và thành phần sau của Microsoft Dynamics 365 Project Operations:

- Project Operations trong môi trường Dataverse phiên bản 4.46.0.60

## <a name="features-included-in-this-release"></a>Các tính năng có trong bản phát hành này

| Lĩnh vực tính năng | Tên tính năng | Thông tin thêm |
| --- | --- | --- |
| Quản lý cơ hội | **Sửa lại và kích hoạt báo giá**<br>Project Operations mang lại sự hỗ trợ đầy đủ cho quá trình bán hàng. Báo giá dự án có thể được kích hoạt để thể hiện trạng thái báo giá là chỉ đọc và đang được xem xét. Các báo giá đã kích hoạt có thể được sửa lại để tạo các báo giá mới có số lượt sửa đổi tăng dần. Báo giá dự án hoặc bản chỉnh sửa báo giá đã kích hoạt có thể ở trạng thái đã chốt hoặc đã mất. | [Kích hoạt và sửa đổi báo giá dự án](/dynamics365/project-operations/sales/activation-and-revision) |
| Định giá và thanh toán | **Mặc định giá không xác định múi giờ**<br>Project Operations đã đưa ra khái niệm về ngày không xác định múi giờ trên tất cả các số liệu thực tế của dự án. Một trường mới, **Ngày giao dịch**, hiện có sẵn trên các mô tả nhật ký và số liệu thực tế, và sẽ được sử dụng để lưu trữ ngày giao dịch xảy ra, nhưng không chuyển đổi ngày đó thành Giờ Phối hợp Quốc tế. Ngày này sẽ được sử dụng cho các quy trình xuôi tuyến như mặc định giá và tạo hóa đơn. | <p>[Xác định tỷ lệ chi phí cho ước tính và số liệu thực tế theo dự án](/dynamics365/project-operations/pro/pricing-costing/cost-price-resolution-sales)</p><p>[Xác định giá bán cho số liệu thực tế và ước tính theo dự án](/dynamics365/project-operations/pro/pricing-costing/sales-price-resolution-sales)</p> |
| Định giá và thanh toán | **Ngày bắt đầu có hiệu lực thay thế giá trong Project Operations**<br>Ngày bắt đầu có hiệu lực thay thế giá cung cấp cách thay thế hoặc thay đổi các mức giá cụ thể trong bảng giá. | [Ngày bắt đầu có hiệu lực thay thế giá](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Thời gian và Chi phí | **Công cụ phê duyệt toàn cầu**<br>Tính năng này cho phép nhà cung cấp phần mềm độc lập (ISV) và phê duyệt tập trung, bất kể trạng thái của dự án hoặc thành viên nhóm trong dự án. | [Bảo mật và phê duyệt](/dynamics365/project-operations/approvals/approvals-security) |
|Hoạch định và theo dõi dự án|**Sử dụng các API lịch trình dự án để thực hiện các hoạt động với các thực thể Lập lịch biểu** </br> </br>API chỉnh sửa đường viền phân công nguồn lực cho phép các nhà phát triển chỉ định theo lập trình hoạt động của người được giao nhiệm vụ trong bất kỳ phạm vi ngày nào được hỗ trợ để lập kế hoạch nỗ lực theo giai đoạn chi tiết hơn.|[Sử dụng các API lịch trình dự án để thực hiện các hoạt động với các thực thể Lập lịch biểu](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="quality-updates"></a>Bản cập nhật chất lượng

| Lĩnh vực tính năng | Số tham chiếu | Cập nhật chất lượng |
| --- | --- | --- |
| Định giá và thanh toán | 2754422 | Các ước tính Vật tư và Chi phí không chuyển sang Dynamics 365 Finance khi dự án được sao chép trong Dataverse. |
| Thời gian và Chi phí | 2787409 | Người phê duyệt không hợp lệ có thể phê duyệt mục nhập thời gian không dựa trên dự án. |
| Quản lý cơ hội | 2788907 | Đã cập nhật thông báo lỗi về xác thực tính duy nhất cho các mô tả đơn hàng bao gồm cờ. |
| Thời gian và Chi phí | 2842253 | Xử lý ngoại lệ rỗng cho phê duyệt thời gian. |
| Định giá và thanh toán | 2844181 | Việc không nhận được ID tương quan sẽ chặn việc tạo hóa đơn. |
| Định giá và thanh toán | 2876628 | QLD, CLD - Ước tính cách phân giải bảng giá nên sử dụng các trường phạm vi ngày kế thừa của bảng giá. |
| Hợp đồng phụ | 2893222 | Nếu không có vai trò nào được chỉ định cho mô tả hợp đồng phụ, thì có thể chọn mô tả đó trên một thành viên nhóm cho bất kỳ vai trò nào. |
