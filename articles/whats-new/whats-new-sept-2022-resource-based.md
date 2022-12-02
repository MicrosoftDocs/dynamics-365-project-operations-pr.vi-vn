---
title: Có gì mới tháng 9 năm 2022 – Project Operations cho các kịch bản dựa trên nguồn lực/hàng không nhập kho
description: Bài viết này cung cấp thông tin về các bản cập nhật chất lượng có trong bản phát hành triển khai bản đơn giản Microsoft Dynamics 365 Project Operations tháng 9 năm 2022 cho các kịch bản dựa trên nguồn lực/hàng không nhập kho.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 04b5f2f8223cdc80028860dd880dde314be244eb
ms.sourcegitcommit: b3a70bc4f2850cff5c2b7114cff7bd61ec298143
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/06/2022
ms.locfileid: "9634832"
---
# <a name="whats-new-september-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Có gì mới tháng 9 năm 2022 – Project Operations cho các kịch bản dựa trên nguồn lực/hàng không nhập kho

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Bài viết này áp dụng cho các phiên bản và thành phần sau của Microsoft Dynamics 365 Project Operations:

- Project Operations trong môi trường Dataverse phiên bản 4.46.0.60
- Quản lý dự án và kế toán trong môi trường ứng dụng Dynamics 365 Finance phiên bản 10.0.29

## <a name="features-included-in-this-release"></a>Các tính năng có trong bản phát hành này

| Lĩnh vực tính năng | Tên tính năng | Thông tin thêm |
| --- | --- | --- |
| Quản lý cơ hội | **Sửa lại và kích hoạt báo giá**<br>Project Operations mang lại sự hỗ trợ đầy đủ cho quá trình bán hàng. Báo giá dự án có thể được kích hoạt để thể hiện trạng thái báo giá là chỉ đọc và đang được xem xét. Các báo giá đã kích hoạt có thể được sửa lại để tạo các báo giá mới có số lượt sửa đổi tăng dần. Báo giá dự án hoặc bản chỉnh sửa báo giá đã kích hoạt có thể ở trạng thái đã chốt hoặc đã mất. | [Kích hoạt và sửa đổi báo giá dự án](/dynamics365/project-operations/sales/activation-and-revision) |
| Định giá và thanh toán | **Mặc định giá không xác định múi giờ**<br>Project Operations đã đưa ra khái niệm về ngày không xác định múi giờ trên tất cả các số liệu thực tế của dự án. Một trường mới, **Ngày giao dịch**, hiện có sẵn trên các mô tả nhật ký và số liệu thực tế, và sẽ được sử dụng để lưu trữ ngày giao dịch xảy ra, nhưng không chuyển đổi ngày đó thành Giờ Phối hợp Quốc tế. Ngày này sẽ được sử dụng cho các quy trình xuôi tuyến như mặc định giá và tạo hóa đơn. | <p>[Xác định tỷ lệ chi phí cho ước tính và số liệu thực tế theo dự án](/dynamics365/project-operations/pricing-costing/cost-price-resolution)</p><p>[Xác định giá bán cho số liệu thực tế và ước tính theo dự án](/dynamics365/project-operations/pricing-costing/sales-price-resolution)</p> |
| Định giá và thanh toán | **Ngày bắt đầu có hiệu lực thay thế giá trong Project Operations**<br>Ngày bắt đầu có hiệu lực thay thế giá cung cấp cách thay thế hoặc thay đổi các mức giá cụ thể trong bảng giá. | [Ngày bắt đầu có hiệu lực thay thế giá](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Hợp đồng phụ | **Hợp đồng phụ và đối chiếu hóa đơn của nhà cung cấp**<br>Tính năng này cho phép khách hàng tạo hợp đồng phụ cho thời gian nguồn lực được mua, danh mục chi phí và vật tư được sử dụng cho công việc của dự án. Nó cũng cho phép khách hàng ghi lại, trong các ứng dụng tài chính và hoạt động, các hóa đơn của nhà cung cấp sẽ có sẵn để người quản lý dự án trong Dataverse có thể xác minh. | <p>[Quản lý hợp đồng phụ](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview)</p><p>[Tạo hóa đơn của nhà cung cấp](/dynamics365/project-operations/procurement/vendor-invoicing-concept-and-creation)</p> |
| Thời gian và Chi phí | **Công cụ phê duyệt toàn cầu**<br>Tính năng này cho phép nhà cung cấp phần mềm độc lập (ISV) và phê duyệt tập trung, bất kể trạng thái của dự án hoặc thành viên nhóm trong dự án. | [Bảo mật và phê duyệt](/dynamics365/project-operations/approvals/approvals-security) |
| Quản lý chi phí | **Khả năng đăng trách nhiệm chi phí bằng đơn vị tiền tệ của nhà cung cấp**<br>Tính năng này cho phép đăng báo cáo chi phí bằng đơn vị tiền tệ của nhà cung cấp cho phương thức thanh toán bằng tiền mặt. | [Khả năng đăng trách nhiệm chi phí bằng đơn vị tiền tệ của nhà cung cấp](/dynamics365/project-operations/expense/posting-expense-reports#enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature) |
| Mua sắm trong dự án | **Thanh toán khi có khoản thanh toán của nhà cung cấp được trả tiền**<br>Tính năng này cho phép sử dụng tính năng Thanh toán khi được trả tiền (PWP) với các môi trường không trữ kho của Project Operations. Nó cho phép các khoản thanh toán của nhà cung cấp bị chặn/giữ lại, dựa trên các điều khoản lưu giữ, cho đến khi nhận được khoản thanh toán từ khách hàng. | [Thanh toán khi có khoản thanh toán của nhà cung cấp được trả tiền](/dynamics365/project-operations/procurement/pay-when-paid) |
| Mua sắm trong dự án | **Yêu cầu mua hàng cho dự án**<br>Tính năng này cho phép người dùng tạo các đơn mua hàng liên quan đến dự án trong các pháp nhân hợp pháp có bật hoạt động tích hợp Project Operations trên Dynamics 365 Customer Engagement. Đơn đặt hàng dự án có thể được sử dụng để ghi lại hoạt động mua sắm vật tư không tồn kho đối với dự án của nhân sự bộ phận Mua sắm. Đơn đặt hàng dự án sẽ không được đồng bộ hóa với Dataverse. Tuy nhiên, bạn có thể sử dụng một thực thể ảo để hiển thị các mô tả đơn đặt hàng Dự án trong Dataverse cho thông tin của người quản lý dự án. Chi phí hóa đơn nhà cung cấp liên quan đến dự án được tích hợp với thực thể Thực tế dự án trong Dataverse. Chi phí dự án được ghi lại trong sổ phụ Dự án bằng cách sử dụng nhật ký Tích hợp Project Operations. | |
|Hoạch định và theo dõi dự án|**Sử dụng các API lịch trình dự án để thực hiện các hoạt động với các thực thể Lập lịch biểu** </br> </br>API chỉnh sửa đường viền phân công nguồn lực cho phép các nhà phát triển chỉ định theo lập trình hoạt động của người được giao nhiệm vụ trong bất kỳ phạm vi ngày nào được hỗ trợ để lập kế hoạch nỗ lực theo giai đoạn chi tiết hơn.|[Sử dụng các API lịch trình dự án để thực hiện các hoạt động với các thực thể Lập lịch biểu](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="project-operations-dual-write-maps-updates"></a>Cập nhật về bản đồ ghi kép của Project Operations

Bảng sau đây hiển thị các bản đồ ghi kép đã được sửa đổi hoặc bổ sung trong bản phát hành Project Operations vào tháng 9 năm 2022.

| Bản đồ thực thể | Phiên bản đã cập nhật | Bình luận |
| -------------- | ------------------- | ------------|
| Giá trị tích hợp thực tế của Project Operations (msdyn_actuals) | 1.0.0.15 | Bản đồ này hỗ trợ xử lý các số liệu thực tế của hợp đồng phụ với Project Operations cho các trường hợp dựa trên nguồn lực. |
| Thực thể xuất hóa đơn nhà cung cấp của Project Operations (msdyn_projectvendorinvoices) | 1.0.0.2 | Bản đồ này hỗ trợ xử lý các số liệu thực tế của hợp đồng phụ với Project Operations cho các trường hợp dựa trên nguồn lực. |
| Thực thể xuất mô tả hóa đơn nhà cung cấp của Project Operations (msdyn_projectvendorinvoicelines) | 1.0.0.5 | Bản đồ này hỗ trợ xử lý các số liệu thực tế của hợp đồng phụ với Project Operations cho các trường hợp dựa trên nguồn lực. |

Luôn chạy phiên bản bản đồ mới nhất trong môi trường của bạn và bật tất cả các bản đồ bảng liên quan khi bạn cập nhật phiên bản giải pháp Project Operations Dataverse và giải pháp Tài chính. Một số tính năng và chức năng nhất định có thể không hoạt động chính xác nếu phiên bản mới nhất của bản đồ không được kích hoạt. Bạn có thể xem phiên bản hiện hoạt của bản đồ trong cột **Phiên bản** trên trang **Ghi kép**. Để kích hoạt phiên bản mới của bản đồ, hãy chọn **Phiên bản bản đồ bảng**, chọn phiên bản mới nhất rồi lưu phiên bản đã chọn. Nếu đã tùy chỉnh sơ đồ bảng có sẵn, hãy áp dụng lại các thay đổi. Để biết thêm thông tin, hãy xem [Quản lý vòng đời áp dụng](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Nếu bạn gặp sự cố khi khởi động bản đồ, hãy làm theo hướng dẫn trong phần [Vấn đề thiếu cột trong bảng trên bản đồ](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) của hướng dẫn khắc phục sự cố Ghi kép.

## <a name="quality-updates"></a>Bản cập nhật chất lượng

### <a name="project-operations-on-dataverse"></a>Project Operations trên Dataverse

| Lĩnh vực tính năng | Số tham chiếu | Cập nhật chất lượng |
| --- | --- | --- |
| Định giá và thanh toán | 2754422 | Các ước tính Vật tư và Chi phí không chuyển sang Finance dự án được sao chép trong Dataverse. |
| Thời gian và Chi phí | 2787409 | Người phê duyệt không hợp lệ có thể phê duyệt mục nhập thời gian không dựa trên dự án. |
| Quản lý cơ hội | 2788907 | Đã cập nhật thông báo lỗi về xác thực tính duy nhất cho các mô tả đơn hàng bao gồm cờ. |
| Thời gian và Chi phí | 2842253 | Xử lý ngoại lệ rỗng cho phê duyệt thời gian. |
| Định giá và thanh toán | 2844181 | Việc không nhận được ID tương quan sẽ chặn việc tạo hóa đơn. |
| Định giá và thanh toán | 2876628 | QLD, CLD - Ước tính cách phân giải bảng giá nên sử dụng các trường phạm vi ngày kế thừa của bảng giá. |
| Hợp đồng phụ | 2893222 | Nếu không có vai trò nào được chỉ định cho mô tả hợp đồng phụ, thì có thể chọn mô tả đó trên một thành viên nhóm cho bất kỳ vai trò nào. |

### <a name="project-management-and-accounting-in-finance"></a>Quản lý dự án và kế toán trong Tài chính

Để biết thông tin về các bản sửa lỗi có trong bản cập nhật này, hãy đăng nhập vào Microsoft Dynamics Lifecycle Services và xem [Bài viết trên KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Các tính năng được bật theo mặc định trong bản phát hành sắp tới

Bảng sau liệt kê các tính năng được bật theo mặc định trong phiên bản 10.0.30. Hầu hết các tính năng đã được tự động bật có thể được tắt trong [Quản lý tính năng](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). Trong tương lai, một số tính năng đã được bật tự động có thể bị xóa khỏi Quản lý tính năng và trở thành tính năng bắt buộc. Thay đổi này đảm bảo rằng khách hàng đang sử dụng chức năng hiện tại, sao cho các cải tiến có thể xây dựng dựa trên chức năng hiện tại khi chúng được thêm vào. Các tính năng sẽ không bao giờ được bật tự động trong vòng chưa đầy một năm, trừ khi chúng được xác định là cần thiết.

| Tên tính năng | Ngày kích hoạt | Tính năng được thêm | Trạng thái tính năng | Mô-đun |
| --- | --- | --- |--- |--- |
| Bật hoạt động không đồng bộ khi người dùng cần chuyển đổi giữa hoạt động đồng bộ và không đồng bộ | Ngày 21 tháng 10 năm 2022 | 9 tháng 4 năm 2021 | Bật theo mặc định | Quản lý chi phí |
| Đánh giá chính sách chi phí cho biên lai được yêu cầu | Ngày 21 tháng 10 năm 2022 | Tháng 20 năm 2021 | Bật theo mặc định | Quản lý chi phí |
| Dạng xem danh sách về các báo cáo chi phí được tạo bởi nhân viên ủy quyền | Ngày 21 tháng 10 năm 2022 | Tháng 19 năm 2020 | Bật theo mặc định | Quản lý chi phí |
| Tính tổng số dặm theo năm tài chính | Ngày 21 tháng 10 năm 2022 | Ngày 10 tháng 5 năm 2022 | Bật theo mặc định | Quản lý chi phí |
