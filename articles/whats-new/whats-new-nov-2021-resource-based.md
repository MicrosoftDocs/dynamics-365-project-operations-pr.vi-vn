---
title: Tính năng mới kể từ tháng 11 năm 2021 – Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho
description: Bài viết này cung cấp thông tin về các bản cập nhật chất lượng có trong bản phát hành triển khai bản đơn giản Project Operations vào tháng 11 năm 2021 cho các kịch bản dựa trên nguồn lực/hàng không nhập kho.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d5b58965f728321cc30d4e476b0dacf621fdec71
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932920"
---
# <a name="whats-new-november-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Tính năng mới kể từ tháng 11 năm 2021 – Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho

*Áp dụng cho: Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho*

Bài viết này áp dụng cho các phiên bản và thành phần sau của Microsoft Dynamics 365 Project Operations:

- Project Operations trong môi trường Dataverse phiên bản 4.26.0.145, 4.26.0.148, 4.26.0.150, 4.26.0.155
- Quản lý dự án và kế toán trong môi trường ứng dụng Dynamics 365 Finance phiên bản 10.0.22

## <a name="features-included-in-this-release"></a>Các tính năng có trong bản phát hành này

Sau đây là các tính năng có trong bản phát hành này:

- Các giao diện lập trình ứng dụng (API) Lập lịch dự án hiện hỗ trợ khả năng tạo và xóa các Bộ chứa dự án.

## <a name="project-operations-dual-write-maps-updates"></a>Cập nhật về bản đồ ghi kép của Project Operations

Không có bản cập nhật nào cho bản đồ ghi kép Project Operations trong bản phát hành này. Để biết danh sách hiện tại và các phiên bản của bản đồ ghi kép Project Operations, hãy xem [Phiên bản bản đồ ghi kép Project Operations](/dynamics365/project-operations/environment/resource-dual-write-maps).

Luôn chạy phiên bản bản đồ mới nhất trong môi trường của bạn và bật tất cả các bản đồ bảng liên quan khi bạn cập nhật phiên bản giải pháp Project Operations Dataverse và giải pháp Tài chính. Một số tính năng và chức năng nhất định có thể không hoạt động chính xác nếu phiên bản mới nhất của bản đồ không được kích hoạt. Bạn có thể xem phiên bản hiện hoạt của bản đồ trong cột **Phiên bản** trên trang **Ghi kép**. Để kích hoạt phiên bản mới của bản đồ, hãy chọn **Phiên bản bản đồ bảng**, chọn phiên bản mới nhất rồi lưu phiên bản đã chọn. Nếu đã tùy chỉnh sơ đồ bảng có sẵn, hãy áp dụng lại các thay đổi. Để biết thêm thông tin, hãy xem [Quản lý vòng đời áp dụng](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Nếu bạn gặp sự cố khi khởi động bản đồ, hãy làm theo hướng dẫn trong phần [Vấn đề thiếu cột trong bảng trên bản đồ](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) của hướng dẫn khắc phục sự cố Ghi kép.

## <a name="quality-updates"></a>Bản cập nhật chất lượng

### <a name="project-operations-in-dataverse"></a>Project Operations trong Dataverse

| Lĩnh vực tính năng | Số tham chiếu | Cập nhật chất lượng |
| --- | --- | --- |
| Định giá và thanh toán | 2240080 | Trường **Điều khoản thanh toán** không được trùng lặp trên hóa đơn ước giá. |
| Định giá và thanh toán | 2358236 | Chỉnh sửa hóa đơn phải cho phép các chỉnh sửa có đường giá bằng không. |
| Quản lý nguồn lực | 2410072 | Cho phép thiết lập nguồn lực được phân công vào nhiệm vụ với tư cách người quản lý dự án. |
| Định giá và thanh toán | 2430234 | Khắc phục sự cố tính toán hiệu suất chi phí. |
| Thời gian và Chi phí | 2436978 | Cho phép nhập thời gian ở định dạng hh:mm. |
| Định giá và thanh toán | 2448623 | Cho phép cập nhật bảng giá sau khi chúng được liên kết với đơn vị tổ chức. |
| Thời gian và Chi phí | 2460396 | Cho phép xóa mục nhập thời gian bằng cách xóa ô. |
| Định giá và thanh toán | 2467386 | Cho phép xóa một dự án có nhiệm vụ, ngay cả khi nhiệm vụ được liên kết với một báo giá đã giành được. |
| Thời gian và Chi phí | 2461744 | Dạng xem **Phê duyệt không thành công của tôi** chỉ chứa các phê duyệt dự án ở giai đoạn **Đã gửi**. |
| Thời gian và Chi phí | 2464082 | Xóa liên kết từ phê duyệt dự án đến bộ phê duyệt khi trạng thái mục tiêu được so khớp. |
| Thời gian và Chi phí | 2468108 | Công việc Lập lịch không được đặt trạng thái **Xử lý** cho bộ phê duyệt. |
| Thời gian và Chi phí | 2471503 | Xóa bộ phê duyệt tồn tại được 7 ngày. |
| Định giá và thanh toán | 2480687 | Không được xóa tham chiếu mô tả báo giá khi mốc mô tả báo giá được tạo. |

### <a name="project-management-and-accounting-in-finance"></a>Quản lý dự án và kế toán trong Tài chính

| Lĩnh vực tính năng | Số tham chiếu | Cập nhật chất lượng |
| --- | --- | --- |
| Quản lý dự án và kế toán | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Số tiền nhà cung cấp giữ lại trong các giao dịch chi phí dự án không được hiển thị trong danh sách giao dịch. |
| Quản lý dự án và kế toán | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Hóa đơn nhà cung cấp liên công ty bị hỏng khi tích hợp hóa đơn nhà cung cấp được bật. |
| Quản lý dự án và kế toán | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Các điều khoản thanh toán trên hóa đơn dự án không hoạt động như mong đợi. |
| Quản lý dự án và kế toán | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Khi khoản trả trước của nhà cung cấp được giải phóng, mục đăng chứng từ có các dòng bổ sung không chính xác. |
| Quản lý dự án và kế toán | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Khi nhật ký tích hợp Project Operations được đăng, nó không thành công vì thiếu thứ nguyên cho một tài khoản không được đăng lên. |
| Quản lý dự án và kế toán | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | Tab **Dự án** không thể chỉnh sửa trên hóa đơn nhà cung cấp đang chờ xử lý khi danh mục mua được chỉ định cho mặt hàng. |
| Quản lý dự án và kế toán | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Ngăn điều hướng không hiển thị nếu bạn chưa đăng nhập vào Project Operations Dataverse. |
| Quản lý dự án và kế toán | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Khi bạn đăng doanh thu từ hóa đơn dự án trong trường hợp trả trước được áp dụng, một sự cố xảy ra vì giao dịch trên chứng từ không được cân bằng. |
| Quản lý dự án và kế toán | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Việc tạo ước tính sau khi bạn đăng đề xuất hóa đơn chặn các dòng chỉnh sửa khỏi quá trình nhập. |
| Quản lý dự án và kế toán | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Không thể sửa đổi bản ghi mốc đã lập hóa đơn đầy đủ. |
| Đi lại và chi tiêu | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Tất cả báo cáo chi phí hiển thị khi bạn tìm kiếm một thể loại trong ứng dụng Chi phí dành cho thiết bị di động. |
| Đi lại và chi tiêu | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Số tiền trên các giao dịch thuế bán hàng và giao dịch nhà cung cấp được tính từ một khoản chi phí được tạo ra từ giao dịch thẻ tín dụng là không chính xác. |
| Đi lại và chi tiêu | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Cảnh báo không liên quan xảy ra khi bạn làm mới trang **Báo cáo chi phí**. |
| Đi lại và chi tiêu | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Sử dụng nhầm người phê duyệt tạm thời khi bạn xóa người phê duyệt tạm thời và sau đó gửi lại báo cáo chi phí thông qua quy trình làm việc. |
| Đi lại và chi tiêu | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Lỗi đăng có liên quan đến việc thiết lập khoảng cách xảy ra. |
