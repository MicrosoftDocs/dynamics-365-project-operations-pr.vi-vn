---
title: Có gì mới tháng 2 năm 2022 – Project Operations cho các kịch bản dựa trên nguồn lực/hàng không nhập kho
description: Bài viết này cung cấp thông tin về các bản cập nhật chất lượng được cung cấp trong lần triển khai bản phát hành Project Operations tháng 2 năm 2022 cho tình huống dựa trên nguồn lực/hàng không trữ kho.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b036c0a3c39c52cb15277293679ef88906cae2c4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933012"
---
# <a name="whats-new-february-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Có gì mới tháng 2 năm 2022 – Project Operations cho các kịch bản dựa trên nguồn lực/hàng không nhập kho

*Áp dụng cho: Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho*

Bài viết này áp dụng cho các phiên bản và thành phần sau của Microsoft Dynamics 365 Project Operations:

- Project Operations trong môi trường Dataverse phiên bản 4.28.0.120
- Quản lý dự án và kế toán trong môi trường ứng dụng Dynamics 365 Finance phiên bản 10.0.24

## <a name="features-included-in-this-release"></a>Các tính năng có trong bản phát hành này

- Kể từ bản phát hành này, bạn có thể thêm tối đa 300 thành viên nhóm vào một dự án. Trước đây, giới hạn về số lượng thành viên nhóm là 150. Để biết thêm thông tin, hãy xem [Giới hạn dự án](../project-management/create-wbs.md#project-limitations).

## <a name="project-operations-dual-write-map-updates"></a>Cập nhật về ánh xạ ghi kép của Project Operations

Danh sách sau đây hiển thị các bản đồ ghi kép đã được sửa đổi hoặc bổ sung trong bản phát hành Project Operations vào tháng 2 năm 2022.

| Bản đồ thực thể | Phiên bản đã cập nhật | Bình luận |
| --- | --- | --- |
| Thực thể xuất chi phí dự án tích hợp của Project Operations (msdyn\_expenses) | 1.0.0.3 | Mở rộng để đồng bộ hóa hoạt động dự án với Dataverse. |

Để biết danh sách hiện tại và các phiên bản của bản đồ ghi kép Project Operations, hãy xem [Phiên bản bản đồ ghi kép Project Operations](../environment/resource-dual-write-maps.md).

Luôn chạy phiên bản bản đồ mới nhất trong môi trường của bạn và bật tất cả các bản đồ bảng liên quan khi bạn cập nhật phiên bản giải pháp Project Operations Dataverse và giải pháp Tài chính. Một số tính năng và chức năng nhất định có thể không hoạt động chính xác nếu phiên bản mới nhất của bản đồ không được kích hoạt. Bạn có thể xem phiên bản hiện hoạt của bản đồ trong cột **Phiên bản** trên trang **Ghi kép**. Để kích hoạt phiên bản mới của bản đồ, hãy chọn **Phiên bản bản đồ bảng**, chọn phiên bản mới nhất rồi lưu phiên bản đã chọn. Nếu đã tùy chỉnh sơ đồ bảng có sẵn, hãy áp dụng lại các thay đổi. Để biết thêm thông tin, hãy xem [Quản lý vòng đời áp dụng](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Nếu bạn gặp sự cố khi khởi động bản đồ, hãy làm theo hướng dẫn trong phần [Vấn đề thiếu cột trong bảng trên bản đồ](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) của hướng dẫn khắc phục sự cố Ghi kép.

## <a name="quality-updates"></a>Bản cập nhật chất lượng

### <a name="project-operations-on-dataverse"></a>Project Operations trên Dataverse

| Lĩnh vực tính năng | Số tham chiếu | Cập nhật chất lượng |
| --- | --- | --- |
| Định giá và thanh toán | 2415109 | Giá trị mặc định trong trường **Điều khoản thanh toán Operations** phải là bản ghi khách hàng hợp đồng dự án và bản ghi hóa đơn ước giá. |
| Định giá và thanh toán | 2497369 | Hiệu chỉnh vật tư phải tuân theo giá trị ngày tháng trong tham số **Điều chỉnh**. |
| Định giá và thanh toán | 2498697 | Cải thiện cấu hình bảo mật cho **Thu hồi mục nhập thời gian**. |
| Định giá và thanh toán | 2513824 | Đối với các tình huống dựa trên nguồn lực, ID danh mục giao dịch không được vượt quá 28 ký tự trong Project Operations. |
| Định giá và thanh toán | 2517455 | Hành động **Làm mới các giao dịch mô tả hóa đơn** không được phép kích hoạt nhiều lần đồng thời cho cùng một hóa đơn. |
| Định giá và thanh toán | 2517465 | Hành động **Hủy kích hoạt chi tiết dòng hóa đơn** bị chặn vì nó không được hỗ trợ. |
| Định giá và thanh toán | 2556660 | Đã sửa lỗi kiểm tra ngày hiệu lực được thực hiện trên bảng giá được đính kèm với bản ghi tham số dự án. |
|   Quản lý cơ hội | 2369202 | Đã sửa logic kinh doanh xác minh rằng các bảng giá có ngày hiệu lực trùng nhau có thể được đính kèm vào cùng một hợp đồng dự án. |
|   Quản lý cơ hội | 2385965 | Đã sửa hành vi trên tab **Khách hàng** của trang **Hợp đồng dự án** khi bạn chọn **Lưu và đóng**. |
| Thời gian và chi phí | 2538503 | Một nhiệm vụ dự án phải có sẵn trong thực thể **Giá trị thực tế của dự án** sau khi báo cáo chi phí được đăng. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Quản lý dự án và kế toán trên Dynamics 365 Finance

| Lĩnh vực tính năng | Số tham chiếu | Cập nhật chất lượng |
| --- | --- | --- |
| Quản lý dự án và kế toán | [615496](https://fix.lcs.dynamics.com/Issue/Details/?bugId=615496) | Trong quá trình nhập chứng từ ghi có của nhà cung cấp, một lỗi xảy ra. Thông báo lỗi cho biết: "Số tiền giữ lại không được nhiều hơn số tiền thực còn lại." |
| Quản lý dự án và kế toán | [619391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=619391) | Nếu một đề xuất hóa đơn bao gồm bất kỳ giao dịch phí bằng 0 là các số liệu thực tế doanh số không lập hóa đơn, thì việc lập hóa đơn không thể xảy ra. |
| Quản lý dự án và kế toán | [624423](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624423) | Chi phí đã đăng không chính xác sau khi giá mua được cập nhật và **Kích hoạt quản lý thay đổi** được kích hoạt.|
| Quản lý dự án và kế toán | [628386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=628386) | Ước tính đăng cho một dự án theo giá cố định sử dụng đơn vị tiền tệ và số tiền không chính xác trong chứng từ ước tính, ngay cả khi tính năng **Bật đơn vị tiền tệ của hợp đồng dự án để dự toán** được kích hoạt. |
| Quản lý dự án và kế toán | [629239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=629239) | **ProjDMFDataPopulation\_Extension** không nên thực hiện cuộc gọi để bật theo dõi thay đổi mà không nắm bắt các ngoại lệ cho các thực thể có khóa cấu hình chưa được bật. |
| Quản lý dự án và kế toán | [623818](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623818) | Công việc theo lô được sửa khi nhiều nhật ký nâng cao được đăng và lỗi xảy ra. |
| Đi lại và chi tiêu | [616805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616805) | Do một vấn đề quyết toán liên quan đến các khoản tạm ứng tiền mặt trên báo cáo chi phí, nên số tiền thuế không được bao gồm như một phần của khoản tạm ứng tiền mặt. |
| Đi lại và chi tiêu | [616959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616959) | Thông tin thuế bán hàng không được bao gồm trên báo cáo **Chi phí - Giao dịch đã đăng**. |
| Đi lại và chi tiêu | [618943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=618943) | Vi phạm chính sách chi phí **Bắt buộc biên lai** hiển thị không chính xác cảnh báo trên báo cáo chi phí. |
| Đi lại và chi tiêu | [633470](https://fix.lcs.dynamics.com/Issue/Details/?bugId=633470) | Một giao dịch dự án không bao gồm thuế bán hàng không thu hồi được trong tổng số tiền doanh số khi giao dịch là kết quả của chi phí số dặm. |
| Đi lại và chi tiêu | [642979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642979) | Khi một dòng được chia thành từng khoản mục có thuế, bạn không thể thay đổi ngày của dòng khoản mục và một lỗi trạng thái tài liệu nguồn xảy ra. |

## <a name="removed-and-deprecated-features"></a>Các tính năng bị xóa và không dùng nữa

Bài viết [Các tính năng bị xóa hoặc không dùng nữa trong Project Operations](removed-depreciated-features-project.md) mô tả các tính năng đã bị xóa hoặc không được dùng nữa đối với Dynamics 365 Project Operations.

- Tính năng đã xóa không còn khả dụng trong sản phẩm.
- Tính năng không dùng nữa không ở trong giai đoạn phát triển và có thể bị xóa khỏi bản cập nhật trong tương lai.

Thông báo không dùng nữa sẽ xuất hiện trong bài viết [Các tính năng bị xóa hoặc không dùng nữa trong Project Operations](removed-depreciated-features-project.md) 12 tháng trước khi bất kỳ tính năng nào bị xóa khỏi sản phẩm.

Đối với các thay đổi mới chỉ ảnh hưởng đến thời gian biên dịch, nhưng tương thích nhị phân với hộp cát và môi trường sản xuất, thời gian không dùng nữa sẽ ít hơn 12 tháng. Thông thường, những thay đổi này là các cập nhật chức năng phải được thực hiện cho công cụ biên soạn.
