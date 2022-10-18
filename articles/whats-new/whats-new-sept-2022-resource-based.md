---
title: Có gì mới vào tháng 9 năm 2022 - Hoạt động dự án cho các kịch bản dựa trên tài nguyên / không có kho
description: Bài viết này cung cấp thông tin về các bản cập nhật chất lượng có sẵn trong bản phát hành tháng 9 năm 2022 của Microsoft Dynamics 365 Project Operations cho các kịch bản dựa trên tài nguyên / không có hàng.
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
# <a name="whats-new-september-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Có gì mới vào tháng 9 năm 2022 - Hoạt động dự án cho các kịch bản dựa trên tài nguyên / không có kho

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Bài viết này áp dụng cho các thành phần và phiên bản sau của Microsoft Dynamics 365 Project Operations:

- Hoạt động dự án trong một Dataverse phiên bản môi trường 4.46.0.60
- Quản lý dự án và kế toán trong môi trường Dynamics 365 Finance phiên bản 10.0.29

## <a name="features-included-in-this-release"></a>Các tính năng có trong bản phát hành này

| Lĩnh vực tính năng | Tên tính năng | Thông tin thêm |
| --- | --- | --- |
| Quản lý cơ hội | **Sửa đổi và Kích hoạt Báo giá**<br>Hoạt động Dự án mang lại sự hỗ trợ đầy đủ cho quá trình bán hàng. Báo giá dự án có thể được kích hoạt để thể hiện trạng thái mà báo giá là chỉ đọc và đang được xem xét. Các báo giá đã kích hoạt có thể được sửa lại để tạo các báo giá mới có số sửa đổi tăng dần. Báo giá dự án đã kích hoạt hoặc bản sửa đổi báo giá có thể được đóng lại là thắng hoặc thua. | [Kích hoạt và sửa đổi báo giá dự án](/dynamics365/project-operations/sales/activation-and-revision) |
| Định giá và thanh toán | **Giá mặc định theo múi giờ không xác định**<br>Hoạt động Dự án đã đưa ra khái niệm về một ngày không xác định múi giờ trên tất cả các thực tế của dự án. Một lĩnh vực mới, **Ngày Giao dịch**, hiện có sẵn trên các dòng nhật ký và thực tế, và sẽ được sử dụng để lưu trữ ngày giao dịch xảy ra, nhưng không chuyển đổi ngày đó thành Giờ Phối hợp Quốc tế. Ngày này sẽ được sử dụng cho các quy trình tiếp theo như mặc định giá và tạo hóa đơn. | <p>[Xác định tỷ lệ chi phí cho các ước tính và thực tế dựa trên dự án](/dynamics365/project-operations/pricing-costing/cost-price-resolution)</p><p>[Xác định giá bán cho các ước tính và thực tế dựa trên dự án](/dynamics365/project-operations/pricing-costing/sales-price-resolution)</p> |
| Định giá và thanh toán | **Ghi đè giá có hiệu lực theo ngày trong Hoạt động dự án**<br>Ghi đè giá có hiệu lực theo ngày cung cấp cách ghi đè hoặc thay đổi giá cụ thể trong danh sách giá. | [Ghi đè giá theo ngày có hiệu lực](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Thầu phụ | **Hợp đồng phụ và đối chiếu hóa đơn của nhà cung cấp**<br>Tính năng này cho phép khách hàng tạo hợp đồng phụ để mua thời gian tài nguyên, danh mục chi phí và vật liệu được sử dụng cho công việc của dự án. Nó cũng cho phép khách hàng ghi lại, trong các ứng dụng tài chính và hoạt động, các hóa đơn của nhà cung cấp sẽ có sẵn cho các nhà quản lý dự án trong Dataverse để xác minh. | <p>[Quản lý hợp đồng phụ](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview)</p><p>[Tạo hóa đơn của nhà cung cấp](/dynamics365/project-operations/procurement/vendor-invoicing-concept-and-creation)</p> |
| Thời gian và Chi phí | **Người phê duyệt toàn cầu**<br>Tính năng này cho phép nhà cung cấp phần mềm độc lập (ISV) và phê duyệt tập trung, bất kể trạng thái của dự án hoặc thành viên nhóm trong dự án. | [Bảo mật và phê duyệt](/dynamics365/project-operations/approvals/approvals-security) |
| Quản lý chi phí | **Khả năng đăng trách nhiệm pháp lý chi phí bằng đơn vị tiền tệ của nhà cung cấp**<br>Tính năng này cho phép đăng báo cáo chi phí bằng đơn vị tiền tệ của nhà cung cấp cho phương thức thanh toán bằng tiền mặt. | [Khả năng đăng trách nhiệm pháp lý chi phí bằng đơn vị tiền tệ của nhà cung cấp](/dynamics365/project-operations/expense/posting-expense-reports#enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature) |
| Mua sắm dự án | **Thanh toán khi thanh toán của nhà cung cấp đã thanh toán**<br>Tính năng này cho phép sử dụng tính năng Thanh toán khi được thanh toán (PWP) với các môi trường không phải của Hoạt động dự án. Nó cho phép các khoản thanh toán của nhà cung cấp bị chặn / giữ lại, dựa trên các điều khoản lưu giữ, cho đến khi nhận được khoản thanh toán từ khách hàng. | [Thanh toán khi thanh toán của nhà cung cấp đã thanh toán](/dynamics365/project-operations/procurement/pay-when-paid) |
| Mua sắm dự án | **Yêu cầu mua dự án**<br>Tính năng này cho phép người dùng tạo các đơn đặt hàng liên quan đến dự án trong các pháp nhân nơi Hoạt động dự án trên Dynamics 365 Customer Engagement tích hợp được bật. Đơn đặt hàng mua dự án có thể được sử dụng để ghi lại hoạt động mua sắm vật tư không tồn kho đối với dự án của nhân vật bộ phận Mua sắm. Đơn đặt hàng mua dự án sẽ không được đồng bộ hóa với Dataverse. Tuy nhiên, bạn có thể sử dụng một thực thể ảo để hiển thị các dòng lệnh mua Dự án trong Dataverse để biết thông tin người quản lý dự án. Chi phí hóa đơn nhà cung cấp liên quan đến dự án được tích hợp với thực thể Thực tế dự án trong Dataverse. Chi phí dự án được ghi vào sổ cái phụ của Dự án bằng cách sử dụng tạp chí Tích hợp Hoạt động Dự án. | |
|Hoạch định và theo dõi dự án|**Sử dụng các API lịch trình dự án để thực hiện các hoạt động với các thực thể Lập lịch biểu** </br> </br>API chỉnh sửa đường bao phân công tài nguyên cho phép các nhà phát triển chỉ định theo chương trình nỗ lực của người được giao nhiệm vụ trong bất kỳ phạm vi ngày nào được hỗ trợ để lập kế hoạch nỗ lực theo từng giai đoạn thời gian chi tiết hơn.|[Sử dụng các API lịch trình dự án để thực hiện các hoạt động với các thực thể Lập lịch biểu](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="project-operations-dual-write-maps-updates"></a>Cập nhật về bản đồ ghi kép của Project Operations

Bảng sau đây cho thấy các bản đồ viết kép đã được sửa đổi hoặc bổ sung trong bản phát hành Dự án Hoạt động tháng 9 năm 2022.

| Bản đồ thực thể | Phiên bản đã cập nhật | Bình luận |
| -------------- | ------------------- | ------------|
| Giá trị tích hợp thực tế của Project Operations (msdyn_actuals) | 1.0.0.15 | Bản đồ này hỗ trợ xử lý các thủ tục hợp đồng phụ với Hoạt động Dự án cho các tình huống dựa trên tài nguyên. |
| Thực thể xuất hóa đơn nhà cung cấp của Project Operations (msdyn_projectvendorinvoices) | 1.0.0.2 | Bản đồ này hỗ trợ xử lý các thủ tục hợp đồng phụ với Hoạt động Dự án cho các tình huống dựa trên tài nguyên. |
| Thực thể xuất mô tả hóa đơn nhà cung cấp của Project Operations (msdyn_projectvendorinvoicelines) | 1.0.0.5 | Bản đồ này hỗ trợ xử lý các thủ tục hợp đồng phụ với Hoạt động Dự án cho các tình huống dựa trên tài nguyên. |

Luôn chạy phiên bản bản đồ mới nhất trong môi trường của bạn và bật tất cả các bản đồ bảng liên quan khi bạn cập nhật Hoạt động dự án của mình Dataverse giải pháp và phiên bản giải pháp Tài chính. Một số tính năng và khả năng có thể không hoạt động chính xác nếu phiên bản mới nhất của bản đồ không được kích hoạt. Bạn có thể xem phiên bản hiện hoạt của bản đồ trong cột **Phiên bản** trên trang **Ghi kép**. Để kích hoạt phiên bản mới của bản đồ, hãy chọn **Phiên bản bản đồ bảng**, chọn phiên bản mới nhất rồi lưu phiên bản đã chọn. Nếu bạn đã tùy chỉnh sơ đồ bảng ngoài hộp, hãy áp dụng lại các thay đổi. Để biết thêm thông tin, hãy xem [Quản lý vòng đời áp dụng](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Nếu bạn gặp sự cố khi khởi động bản đồ, hãy làm theo hướng dẫn trong [Vấn đề thiếu cột trong bảng trên bản đồ](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) phần của hướng dẫn khắc phục sự cố ghi kép.

## <a name="quality-updates"></a>Bản cập nhật chất lượng

### <a name="project-operations-on-dataverse"></a>Project Operations trên Dataverse

| Lĩnh vực tính năng | Số tham chiếu | Cập nhật chất lượng |
| --- | --- | --- |
| Định giá và thanh toán | 2754422 | Các ước tính về Vật liệu và Chi phí không chuyển đến Tài chính khi các dự án được sao chép trong Dataverse. |
| Thời gian và Chi phí | 2787409 | Người phê duyệt không hợp lệ có thể phê duyệt mục thời gian phi dự án. |
| Quản lý cơ hội | 2788907 | Đã cập nhật thông báo lỗi về xác thực tính duy nhất cho các dòng đặt hàng có cờ. |
| Thời gian và Chi phí | 2842253 | Xử lý ngoại lệ rỗng để phê duyệt thời gian. |
| Định giá và thanh toán | 2844181 | Việc không nhận được ID tương quan sẽ chặn việc tạo hóa đơn. |
| Định giá và thanh toán | 2876628 | QLD, CLD - Ước tính độ phân giải bảng giá nên sử dụng các trường phạm vi ngày kế thừa của bảng giá. |
| Thầu phụ | 2893222 | Nếu không có vai trò nào được chỉ định cho dòng hợp đồng phụ, thì có thể chọn dòng đó trên một thành viên trong nhóm cho bất kỳ vai trò nào. |

### <a name="project-management-and-accounting-in-finance"></a>Quản lý dự án và kế toán trong lĩnh vực tài chính

Để biết thông tin về các bản sửa lỗi có trong bản cập nhật này, hãy đăng nhập vào Microsoft Dynamics Dịch vụ Vòng đời và xem [KB bài viết](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Các tính năng được bật theo mặc định trong bản phát hành sắp tới

Bảng sau liệt kê các tính năng được bật theo mặc định trong phiên bản 10.0.30. Hầu hết các tính năng đã được bật tự động có thể được tắt trong [Quản lý tính năng](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). Trong tương lai, một số tính năng đã được bật tự động có thể bị xóa khỏi Quản lý tính năng và trở thành tính năng bắt buộc. Thay đổi này đảm bảo rằng khách hàng đang sử dụng chức năng hiện tại, để các cải tiến có thể xây dựng dựa trên chức năng hiện tại khi chúng được thêm vào. Các tính năng sẽ không bao giờ được bật tự động trong vòng chưa đầy một năm, trừ khi chúng được xác định là cần thiết.

| Tên tính năng | Ngày kích hoạt | Đã thêm tính năng | Trạng thái tính năng | Mô-đun |
| --- | --- | --- |--- |--- |
| Bật hoạt động không đồng bộ khi người dùng cần chuyển đổi giữa hoạt động đồng bộ và không đồng bộ | Ngày 21 tháng 10 năm 2022 | 9 tháng 4 năm 2021 | Bật theo mặc định | Quản lý chi phí |
| Đánh giá chính sách chi phí cho các khoản thu được yêu cầu | Ngày 21 tháng 10 năm 2022 | Tháng 20 năm 2021 | Bật theo mặc định | Quản lý chi phí |
| Chế độ xem danh sách các báo cáo chi phí được tạo bởi công nhân ủy nhiệm | Ngày 21 tháng 10 năm 2022 | Tháng 19 năm 2020 | Bật theo mặc định | Quản lý chi phí |
| Tính tổng số dặm theo năm tài chính | Ngày 21 tháng 10 năm 2022 | Ngày 10 tháng 5 năm 2022 | Bật theo mặc định | Quản lý chi phí |
