---
title: Có gì mới vào tháng 11 năm 2021 - Hoạt động dự án cho các kịch bản dựa trên tài nguyên / không có kho
description: Chủ đề này cung cấp thông tin về các bản cập nhật chất lượng có sẵn trong bản phát hành tháng 11 năm 2021 của Hoạt động dự án cho các kịch bản dựa trên tài nguyên / không có kho.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: fb9dad5b04ef2933ed8a8d8211f888f13df5ba40
ms.sourcegitcommit: 9d20e7738cce195d344f5925a115741a1ce3ca36
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 12/21/2021
ms.locfileid: "7942911"
---
# <a name="whats-new-november-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Có gì mới vào tháng 11 năm 2021 - Hoạt động dự án cho các kịch bản dựa trên tài nguyên / không có kho

*Áp dụng cho: Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho*

Chủ đề này áp dụng cho các thành phần và phiên bản sau của Microsoft Dynamics 365 Project Operations:

- Hoạt động dự án trong một Dataverse phiên bản môi trường 4.26.0.145, 4.26.0.148, 4.26.0.150, 4.26.0.155
- Quản lý dự án và kế toán trong một Dynamics 365 Finance phiên bản môi trường 10.0.22

## <a name="features-included-in-this-release"></a>Các tính năng có trong bản phát hành này

Sau đây là các tính năng có trong bản phát hành này:

- Các giao diện lập trình ứng dụng Lập lịch dự án (API) hiện hỗ trợ khả năng tạo và xóa các nhóm Dự án.

## <a name="project-operations-dual-write-maps-updates"></a>Cập nhật về bản đồ ghi kép của Project Operations

Không có bản cập nhật nào cho bản đồ ghi kép Project Operations trong bản phát hành này. Để biết danh sách hiện tại và các phiên bản của bản đồ ghi kép Project Operations, hãy xem [Phiên bản bản đồ ghi kép Project Operations](/dynamics365/project-operations/environment/resource-dual-write-maps).

Luôn chạy phiên bản mới nhất của bản đồ trong môi trường của bạn và bật tất cả các bản đồ bảng liên quan khi bạn cập nhật Hoạt động dự án của mình Dataverse giải pháp và phiên bản giải pháp Tài chính. Một số tính năng và khả năng có thể không hoạt động chính xác nếu phiên bản mới nhất của bản đồ không được kích hoạt. Bạn có thể xem phiên bản hiện hoạt của bản đồ trong cột **Phiên bản** trên trang **Ghi kép**. Để kích hoạt phiên bản mới của bản đồ, hãy chọn **Phiên bản bản đồ bảng**, chọn phiên bản mới nhất rồi lưu phiên bản đã chọn. Nếu bạn đã tùy chỉnh sơ đồ bảng ngoài hộp, hãy áp dụng lại các thay đổi. Để biết thêm thông tin, hãy xem [Quản lý vòng đời áp dụng](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Nếu bạn gặp sự cố khi khởi động bản đồ, hãy làm theo hướng dẫn trong [Vấn đề thiếu cột trong bảng trên bản đồ](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) phần của hướng dẫn khắc phục sự cố Ghi kép.

## <a name="quality-updates"></a>Bản cập nhật chất lượng

### <a name="project-operations-in-dataverse"></a>Hoạt động dự án trong Dataverse

| Lĩnh vực tính năng | Số tham chiếu | Cập nhật chất lượng |
| --- | --- | --- |
| Định giá và thanh toán | 2240080 | Các **Điều khoản thanh toán** trường không được trùng lặp trên hóa đơn chiếu lệ. |
| Định giá và thanh toán | 2358236 | Chỉnh sửa hóa đơn phải cho phép chỉnh sửa có đường giá bằng không. |
| Quản lý nguồn lực | 2410072 | Cho phép thiết lập tài nguyên được giao cho nhiệm vụ với tư cách là người quản lý dự án. |
| Định giá và thanh toán | 2430234 | Khắc phục sự cố tính toán hiệu suất chi phí. |
| Thời gian và Chi phí | 2436978 | Cho phép nhập thời gian ở định dạng hh: mm. |
| Định giá và thanh toán | 2448623 | Cho phép cập nhật bảng giá sau khi chúng được liên kết với một đơn vị tổ chức. |
| Thời gian và Chi phí | 2460396 | Cho phép xóa mục nhập thời gian bằng cách xóa ô. |
| Định giá và thanh toán | 2467386 | Cho phép xóa một dự án có nhiệm vụ, ngay cả khi nhiệm vụ được liên kết với một câu trích dẫn đã thắng. |
| Thời gian và Chi phí | 2461744 | Các **Sự chấp thuận không thành công của tôi** chế độ xem chỉ chứa các phê duyệt dự án trong **Đã đệ trình** sân khấu. |
| Thời gian và Chi phí | 2464082 | Xóa liên kết từ phê duyệt dự án đến phê duyệt đã đặt khi trạng thái mục tiêu được khớp. |
| Thời gian và Chi phí | 2468108 | Công việc lên lịch không nên đặt một **Xử lý** trạng thái cho tập hợp phê duyệt. |
| Thời gian và Chi phí | 2471503 | Xóa tập hợp phê duyệt đã có bảy ngày. |
| Định giá và thanh toán | 2480687 | Tham chiếu dòng trích dẫn không được xóa khi cột mốc dòng trích dẫn được tạo. |

### <a name="project-management-and-accounting-in-finance"></a>Quản lý dự án và kế toán trong lĩnh vực tài chính

| Lĩnh vực tính năng | Số tham chiếu | Cập nhật chất lượng |
| --- | --- | --- |
| Quản lý dự án và kế toán | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Số tiền nhà cung cấp giữ lại trong các giao dịch chi phí dự án không được hiển thị trong danh sách giao dịch. |
| Quản lý dự án và kế toán | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Hóa đơn nhà cung cấp liên công ty bị hỏng khi tích hợp hóa đơn nhà cung cấp được bật. |
| Quản lý dự án và kế toán | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Các điều khoản thanh toán trên hóa đơn dự án không hoạt động như mong đợi. |
| Quản lý dự án và kế toán | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Khi việc lưu giữ nhà cung cấp được giải phóng, việc đăng phiếu thưởng có các dòng bổ sung không chính xác. |
| Quản lý dự án và kế toán | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Khi tạp chí tích hợp Hoạt động Dự án được đăng, nó không thành công do thiếu thứ nguyên cho một tài khoản không được đăng lên. |
| Quản lý dự án và kế toán | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | Các **Dự định** không thể chỉnh sửa tab trên hóa đơn của nhà cung cấp đang chờ xử lý khi danh mục mua sắm được chỉ định cho mặt hàng. |
| Quản lý dự án và kế toán | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Ngăn điều hướng bị thiếu nếu bạn chưa đăng nhập vào Hoạt động dự án Dataverse. |
| Quản lý dự án và kế toán | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Khi bạn đăng doanh thu từ hóa đơn dự án trong trường hợp lưu giữ áp dụng, một vấn đề xảy ra do các giao dịch trên chứng từ không có số dư. |
| Quản lý dự án và kế toán | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Việc tạo ước tính sau khi bạn đăng đề xuất hóa đơn chặn các dòng sửa chữa khỏi quá trình nhập. |
| Quản lý dự án và kế toán | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Không thể sửa đổi hồ sơ cột mốc đã lập hóa đơn đầy đủ. |
| Đi lại và chi tiêu | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Tất cả các báo cáo chi phí đều hiển thị khi bạn tìm kiếm một danh mục trong ứng dụng Chi phí dành cho thiết bị di động. |
| Đi lại và chi tiêu | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Số tiền không chính xác về giao dịch của nhà cung cấp và giao dịch thuế bán hàng được tính từ một khoản chi phí được tạo ra từ giao dịch thẻ tín dụng. |
| Đi lại và chi tiêu | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Một cảnh báo không liên quan xảy ra khi bạn làm mới **Báo cáo chi tiêu** trang. |
| Đi lại và chi tiêu | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Người phê duyệt tạm thời sai được sử dụng khi bạn xóa người phê duyệt tạm thời và sau đó gửi lại báo cáo chi phí thông qua quy trình làm việc. |
| Đi lại và chi tiêu | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Một lỗi đăng liên quan đến thiết lập số dặm xảy ra. |
