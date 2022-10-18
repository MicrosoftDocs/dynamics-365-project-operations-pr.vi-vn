---
title: Có gì mới vào tháng 9 năm 2022 - Triển khai Project Operations Lite
description: Bài viết này cung cấp thông tin về các bản cập nhật chất lượng có sẵn trong bản phát hành tháng 9 năm 2022 của Microsoft Dynamics 365 Project Operations triển khai lite.
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
# <a name="whats-new-september-2022---project-operations-lite-deployment"></a>Có gì mới vào tháng 9 năm 2022 - Triển khai Project Operations Lite

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Bài viết này áp dụng cho các thành phần và phiên bản sau của Microsoft Dynamics 365 Project Operations:

- Hoạt động dự án trong một Dataverse phiên bản môi trường 4.46.0.60

## <a name="features-included-in-this-release"></a>Các tính năng có trong bản phát hành này

| Lĩnh vực tính năng | Tên tính năng | Thông tin thêm |
| --- | --- | --- |
| Quản lý cơ hội | **Sửa đổi và Kích hoạt Báo giá**<br>Hoạt động Dự án mang lại sự hỗ trợ đầy đủ cho quá trình bán hàng. Báo giá dự án có thể được kích hoạt để thể hiện trạng thái mà báo giá là chỉ đọc và đang được xem xét. Các báo giá đã kích hoạt có thể được sửa lại để tạo các báo giá mới có số sửa đổi tăng dần. Báo giá dự án đã kích hoạt hoặc bản sửa đổi báo giá có thể được đóng lại là thắng hoặc thua. | [Kích hoạt và sửa đổi báo giá dự án](/dynamics365/project-operations/sales/activation-and-revision) |
| Định giá và thanh toán | **Giá mặc định theo múi giờ không xác định**<br>Hoạt động Dự án đã đưa ra khái niệm về một ngày không xác định múi giờ trên tất cả các thực tế của dự án. Một lĩnh vực mới, **Ngày Giao dịch**, hiện có sẵn trên các dòng nhật ký và thực tế, và sẽ được sử dụng để lưu trữ ngày giao dịch xảy ra, nhưng không chuyển đổi ngày đó thành Giờ Phối hợp Quốc tế. Ngày này sẽ được sử dụng cho các quy trình tiếp theo như mặc định giá và tạo hóa đơn. | <p>[Xác định tỷ lệ chi phí cho các ước tính và thực tế dựa trên dự án](/dynamics365/project-operations/pro/pricing-costing/cost-price-resolution-sales)</p><p>[Xác định giá bán cho các ước tính và thực tế dựa trên dự án](/dynamics365/project-operations/pro/pricing-costing/sales-price-resolution-sales)</p> |
| Định giá và thanh toán | **Ghi đè giá có hiệu lực theo ngày trong Hoạt động dự án**<br>Ghi đè giá có hiệu lực theo ngày cung cấp cách ghi đè hoặc thay đổi giá cụ thể trong danh sách giá. | [Ghi đè giá theo ngày có hiệu lực](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Thời gian và Chi phí | **Người phê duyệt toàn cầu**<br>Tính năng này cho phép nhà cung cấp phần mềm độc lập (ISV) và phê duyệt tập trung, bất kể dự án hoặc trạng thái thành viên nhóm trong dự án. | [Bảo mật và phê duyệt](/dynamics365/project-operations/approvals/approvals-security) |
|Hoạch định và theo dõi dự án|**Sử dụng các API lịch trình dự án để thực hiện các hoạt động với các thực thể Lập lịch biểu** </br> </br>API chỉnh sửa đường bao phân công tài nguyên cho phép các nhà phát triển chỉ định theo chương trình nỗ lực của người được giao nhiệm vụ trong bất kỳ phạm vi ngày nào được hỗ trợ để lập kế hoạch nỗ lực theo từng giai đoạn thời gian chi tiết hơn.|[Sử dụng các API lịch trình dự án để thực hiện các hoạt động với các thực thể Lập lịch biểu](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="quality-updates"></a>Bản cập nhật chất lượng

| Lĩnh vực tính năng | Số tham chiếu | Cập nhật chất lượng |
| --- | --- | --- |
| Định giá và thanh toán | 2754422 | Các ước tính về Vật liệu và Chi phí không chuyển đến Dynamics 365 Finance khi các dự án được sao chép vào Dataverse. |
| Thời gian và Chi phí | 2787409 | Người phê duyệt không hợp lệ có thể phê duyệt mục thời gian phi dự án. |
| Quản lý cơ hội | 2788907 | Đã cập nhật thông báo lỗi về xác thực tính duy nhất cho các dòng đặt hàng có cờ. |
| Thời gian và Chi phí | 2842253 | Xử lý ngoại lệ rỗng để phê duyệt thời gian. |
| Định giá và thanh toán | 2844181 | Việc không nhận được ID tương quan sẽ chặn việc tạo hóa đơn. |
| Định giá và thanh toán | 2876628 | QLD, CLD - Ước tính độ phân giải bảng giá nên sử dụng các trường phạm vi ngày kế thừa của bảng giá. |
| Thầu phụ | 2893222 | Nếu không có vai trò nào được chỉ định cho dòng hợp đồng phụ, thì có thể chọn dòng đó trên một thành viên trong nhóm cho bất kỳ vai trò nào. |
