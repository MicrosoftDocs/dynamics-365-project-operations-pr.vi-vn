---
title: Tính năng mới kể từ tháng 6 năm 2021 – Project Operations cho các kịch bản dựa trên nguồn lực/hàng không trữ kho
description: Chủ đề này cung cấp thông tin về các bản cập nhật chất lượng có trong bản phát hành tháng 6 năm 2021 của Project Operations cho các kịch bản dựa trên nguồn lực/hàng không trữ kho.
author: sigitac
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 28890238f9debb96786a31f66dd9a219f88a5338
ms.sourcegitcommit: 2f16c2bc7c8350676a6a380c61fffa9958db6a0b
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/22/2021
ms.locfileid: "6293163"
---
# <a name="whats-new-june-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Tính năng mới kể từ tháng 6 năm 2021 – Project Operations cho các kịch bản dựa trên nguồn lực/hàng không trữ kho

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Chủ đề này áp dụng cho các phiên bản và thành phần sau của Dynamics 365 Project Operations:

- Project Operations trên môi trường Dynamics 365 Dataverse phiên bản 4.11.0.156 hoặc 4.11.0.164.
- Quản lý dự án và kế toán trong môi trường ứng dụng Finance and Operations phiên bản 10.0.19.

## <a name="features-included-in-this-release"></a>Các tính năng có trong bản phát hành này

Sau đây là các tính năng có trong bản phát hành này:

- Khả năng xóa [Các dòng đề xuất hóa đơn dự án cho các tình huống điều chỉnh](../invoicing/correct-project-invoice-proposals.md).
- Các dòng chi phí được chia nhỏ phản ánh tên danh mục con trong báo cáo chi phí [Báo cáo chi phí được mô phỏng lại-Tính năng mới](../expense/expense-reports-reimagined.md#new-features).
- Phương thức thanh toán có sẵn trong ngăn chi phí mới khi tạo một khoản chi phí mới.

## <a name="project-operations-dual-write-maps-updates"></a>Cập nhật về bản đồ ghi kép của Project Operations

Không có bản cập nhật nào cho bản đồ ghi kép Project Operations trong bản phát hành này. 

Để biết danh sách hiện tại và các phiên bản của bản đồ ghi kép Project Operations, hãy xem [Phiên bản bản đồ ghi kép Project Operations](../environment/resource-dual-write-maps.md).

Bạn hãy luôn chạy phiên bản mới nhất của bản đồ trong môi trường của bạn và kích hoạt tất cả các bản đồ bảng liên quan trong quá trình cập nhật giải pháp Dataverse của Project Operations và phiên bản giải pháp ứng dụng Finance and Operations. Một số tính năng và chức năng nhất định có thể không hoạt động chính xác nếu phiên bản mới nhất của bản đồ không được kích hoạt. Bạn có thể xem phiên bản đang hoạt động của bản đồ trên trang **Ghi kép** trong cột **Phiên bản**. Kích hoạt phiên bản mới của bản đồ bằng cách chọn **Các phiên bản bản đồ bảng**, chọn phiên bản mới nhất, sau đó lưu phiên bản đã chọn. Nếu đã tùy chỉnh sơ đồ bảng có sẵn, hãy áp dụng lại các thay đổi. Để biết thêm thông tin, hãy xem [Quản lý vòng đời áp dụng](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Nếu bạn gặp sự cố khi khởi động bản đồ, hãy làm theo hướng dẫn trong phần [Vấn đề thiếu cột trong bảng trên bản đồ](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) trong hướng dẫn khắc phục sự cố Ghi kép.

## <a name="quality-updates"></a>Bản cập nhật chất lượng

### <a name="project-operations-on-dataverse"></a>Project Operations trên Dataverse

| **Lĩnh vực tính năng** | **Số tham chiếu** | **Cập nhật chất lượng** |
| --- | --- | --- |
| Định giá và thanh toán | 2281417 | Đã khắc phục sự cố liên quan đến việc không thực hiện được hành động tạo hóa đơn tự động thông qua lịch trình hóa đơn. |
| Định giá và thanh toán | 2287835 | Đã cải thiện hiệu suất xác nhận hóa đơn. |
| Quản lý cơ hội | 2222555 | Khả năng tính phí ước tính vật liệu phải được sao chép chính xác để báo giá chi tiết dòng khi sử dụng **Nhập từ Ước tính dự án**. |
| Quản lý cơ hội | 2223427 | Các tùy chỉnh hiện được phép cho hành động, **GenerateRetainersFromRetainerScheduleOptions**. |
| Quản lý cơ hội | 2277528 | Tính toán giá trị mốc thanh toán cố định cho các mô tả hợp đồng dự án với nhiều khách hàng. |
| Hoạch định và theo dõi dự án | 2226110 | Đã khắc phục sự cố gián đoạn với hàm **Tạo yêu cầu** trong lưới **Nhóm dự án**. |
| Hoạch định và theo dõi dự án | 2208109 | Người dùng không thể tạo dự án bằng một đơn vị tiền tệ với các nhiệm vụ liên quan bằng đơn vị tiền tệ khác. |
| Hoạch định và theo dõi dự án | 2258228 | Danh sách các trường được phép sửa đổi với thực thể **Lập lịch trình** sử dụng API lịch trình đã được cập nhật. |
| Hoạch định và theo dõi dự án | 2293989 | Ngôn ngữ và cài đặt khu vực chính xác phải được chuyển sang lưới **Nhiệm vụ dự án**. |
| Quản lý nguồn lực | 2220493 | Đã sửa lỗi trải nghiệm người dùng trong lưới **Nhiệm vụ** khi nhanh chóng đánh dấu một yêu cầu nguồn lực là hoàn thành. |
| Quản lý nguồn lực | 2330496 | Đã sửa lỗi tải **Bảng lịch trình**. (Bản cập nhật chất lượng có sẵn trong phiên bản 4.11.0.164) |
| Thời gian và Chi phí | 2194431 | Lưới **Mục nhập thời gian** phải tuân thủ đầu tuần như đã thiết lập trong **Cài đặt hệ thống**. |
| Thời gian và Chi phí | 2277311 | Sau khi bạn xóa giá trị trong một ô trong lưới **Mục nhập thời gian**, con trỏ vẫn ở trong lưới. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Quản lý dự án và kế toán trong Dynamics 365 Finance

| Lĩnh vực tính năng | Số tham chiếu | Cập nhật chất lượng |
| --- | --- | --- |
| Quản lý dự án và kế toán | [552976](https://fix.lcs.dynamics.com/Issue/Details/?bugId=552976) | **Ghi chú biểu mẫu** và **Thiết lập biểu mẫu** không hiển thị dưới **Thiết lập quản lý dự án** trong các pháp nhân Tài chính được tích hợp với Project Operations. |
| Quản lý dự án và kế toán | [527970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527970) | Mô tả mặc định cho VAT bị trống khi **Kiểu đăng bài** = **Thuế bán hàng** cho các chứng từ hóa đơn của dự án. |
| Quản lý dự án và kế toán | [565089](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565089) | Các giao dịch kép được đăng khi thanh toán dựa trên nhiệm vụ được sử dụng trong Dataverse với tích hợp Project Operations. |
| Quản lý dự án và kế toán | [566869](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566869) | Phần trăm hoàn thành trong ghi nhận doanh thu không chính xác khi sử dụng tích hợp Project Operations. |
| Quản lý dự án và kế toán | [568107](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568107) | Doanh thu tích lũy được nhân đôi trên một hóa đơn của nhà cung cấp đang chờ xử lý trong một kịch bản tích hợp Project Operations. |
| Quản lý dự án và kế toán | [572370](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572370) | Không thể đăng phần tích hợp khi quy tắc hồ sơ doanh thu được đặt thành thiết lập **Nhóm**. |
| Quản lý dự án và kế toán | [573596](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573596) | Không thể đăng hóa đơn mua hàng cho các đơn đặt hàng dự án có dòng với nhiều đơn vị đo lường. |
| Quản lý dự án và kế toán | [573637](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573637) | Không thể cập nhật thông số tài chính mặc định của một dự án bằng cách sử dụng các thực thể dữ liệu của dự án **V2**. |
| Quản lý dự án và kế toán | [577211](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577211) | Quá trình hàng loạt để tạo ước tính dự án mất quá nhiều thời gian để hoàn thành. |
| Quản lý dự án và kế toán | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | Xóa hợp đồng cũng xóa địa chỉ được liên kết với khách hàng. |
| Đi lại và chi phí | [514930](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514930) | Điều kiện quy trình phê duyệt báo cáo chi phí không được đánh giá chính xác. |
| Đi lại và chi phí | [519304](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519304) | Chính sách báo cáo chi phí không đánh giá đúng ID dự án. |
| Đi lại và chi phí | [522463](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522463) | Hành động, **Chia cho cá nhân cho các giao dịch chi phí liên công ty** không hoạt động chính xác. |
| Đi lại và chi phí | [534702](https://fix.lcs.dynamics.com/Issue/Details/?bugId=534702) | Các biện minh dòng báo cáo chi phí vô tình bị xóa khi một số yêu cầu đi lại nhất định bị xóa. Điều này xảy ra khi recID của báo cáo chi phí và yêu cầu đi lại giống nhau. |
| Đi lại và chi phí | [544368](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544368) | Có một vấn đề trong ứng dụng di động Expense khi trường **ID dự án** là bắt buộc trong chính sách báo cáo chi phí. |
| Đi lại và chi phí | [545331](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545331) | Không thể chỉnh sửa chi phí liên công ty liên quan đến dự án. Thay vào đó, thông báo lỗi sau sẽ hiển thị, "Tham chiếu đối tượng không được đặt thành phiên bản của đối tượng." |
| Đi lại và chi phí | [548659](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548659) | Sau khi báo cáo chi phí được đăng, đơn vị tiền tệ và số tiền sai sẽ được liệt kê trong sổ phụ của ngân hàng. |
| Đi lại và chi phí | [558336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558336) | Các cải tiến đã được thực hiện cho tính năng *Xóa các giao dịch thẻ tín dụng*.  |
| Đi lại và chi phí | [525070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525070) | Thuế bán hàng được bao gồm trong báo cáo chi phí không được tính toán nhất quán khi đơn vị tiền tệ báo cáo khác được chỉ định trong một pháp nhân. |
| Đi lại và chi phí | [527779](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527779) | Hiệu suất bị ảnh hưởng khi thêm một khoản chi phí đi lại bằng tiền mặt mới. |
| Đi lại và chi phí | [537841](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537841) | Các quy tắc về chính sách chi phí không được kích hoạt trên báo cáo chi phí. |
| Đi lại và chi phí | [566386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566386) | Tải lên danh mục được chia sẻ mới bằng cách sử dụng Khung quản lý dữ liệu sẽ xóa tất cả các danh mục con cho tất cả các danh mục được chia sẻ. |
| Đi lại và chi phí | [574131](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574131) | Khi bạn tạo dòng chi phí, sau đó chọn một danh mục, thông báo lỗi sau sẽ hiển thị, "Sự kết hợp giữa DOM nhóm thuế bán hàng và nhóm thuế bán hàng STD không hợp lệ." |
| Đi lại và chi phí | [574900](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574900) | Có vấn đề về đồng bộ hóa trong ứng dụng di động Expense. |
