---
title: Có gì mới tháng 2 năm 2022 - Hoạt động dự án cho các kịch bản dựa trên tài nguyên / không có kho
description: Chủ đề này cung cấp thông tin về các bản cập nhật chất lượng có trong bản phát hành tháng 2 năm 2022 của Hoạt động dự án cho các tình huống dựa trên tài nguyên / không có kho.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 76ae00517c857415c89d7a03f421686dad28da93
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600860"
---
# <a name="whats-new-february-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Có gì mới tháng 2 năm 2022 - Hoạt động dự án cho các kịch bản dựa trên tài nguyên / không có kho

*Áp dụng cho: Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho*

Chủ đề này áp dụng cho các thành phần và phiên bản sau của Microsoft Dynamics 365 Project Operations:

- Hoạt động dự án trong một Dataverse phiên bản môi trường 4.28.0.120
- Quản lý dự án và kế toán trong môi trường Dynamics 365 Finance phiên bản 10.0.24

## <a name="features-included-in-this-release"></a>Các tính năng có trong bản phát hành này

- Kể từ phiên bản này, bạn có thể thêm tối đa 300 thành viên trong nhóm vào một dự án. Trước đây, giới hạn về số lượng thành viên trong nhóm là 150. Để biết thêm thông tin, hãy xem [Các giới hạn của dự án](../project-management/create-wbs.md#project-limitations).

## <a name="project-operations-dual-write-map-updates"></a>Bản cập nhật bản đồ ghi kép Hoạt động Dự án

Danh sách sau đây hiển thị các bản đồ viết kép đã được sửa đổi hoặc bổ sung trong bản phát hành Dự án Hoạt động tháng 2 năm 2022.

| Bản đồ thực thể | Phiên bản đã cập nhật | Bình luận |
| --- | --- | --- |
| Dự án Hoạt động tích hợp chi phí dự án xuất khẩu thực thể (msdyn\_ chi phí) | 1.0.0.3 | Mở rộng để đồng bộ hóa hoạt động dự án sang Dataverse. |

Để biết danh sách hiện tại và các phiên bản của bản đồ viết kép Hoạt động Dự án, hãy xem [Phiên bản bản đồ ghi kép Hoạt động Dự án](../environment/resource-dual-write-maps.md).

Luôn chạy phiên bản bản đồ mới nhất trong môi trường của bạn và bật tất cả các bản đồ bảng liên quan khi bạn cập nhật Hoạt động dự án của mình Dataverse giải pháp và phiên bản giải pháp Tài chính. Một số tính năng và khả năng có thể không hoạt động chính xác nếu phiên bản mới nhất của bản đồ không được kích hoạt. Bạn có thể xem phiên bản hiện hoạt của bản đồ trong cột **Phiên bản** trên trang **Ghi kép**. Để kích hoạt phiên bản mới của bản đồ, hãy chọn **Phiên bản bản đồ bảng**, chọn phiên bản mới nhất rồi lưu phiên bản đã chọn. Nếu bạn đã tùy chỉnh sơ đồ bảng ngoài hộp, hãy áp dụng lại các thay đổi. Để biết thêm thông tin, hãy xem [Quản lý vòng đời áp dụng](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Nếu bạn gặp sự cố khi khởi động bản đồ, hãy làm theo hướng dẫn trong [Vấn đề thiếu cột trong bảng trên bản đồ](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) của hướng dẫn khắc phục sự cố Ghi kép.

## <a name="quality-updates"></a>Bản cập nhật chất lượng

### <a name="project-operations-on-dataverse"></a>Project Operations trên Dataverse

| Lĩnh vực tính năng | Số tham chiếu | Cập nhật chất lượng |
| --- | --- | --- |
| Định giá và thanh toán | 2415109 | Giá trị mặc định trong **Điều khoản thanh toán hoạt động** trường phải là hồ sơ khách hàng hợp đồng dự án và hồ sơ hóa đơn chiếu lệ. |
| Định giá và thanh toán | 2497369 | Hiệu chỉnh vật liệu phải tuân theo giá trị ngày tháng trong **Điều chỉnh** thông số. |
| Định giá và thanh toán | 2498697 | Cải thiện cấu hình bảo mật cho **Thu hồi mục nhập thời gian**. |
| Định giá và thanh toán | 2513824 | Đối với các tình huống dựa trên tài nguyên, ID danh mục giao dịch không được vượt quá 28 ký tự trong Hoạt động dự án. |
| Định giá và thanh toán | 2517455 | Các **Làm mới các giao dịch dòng hóa đơn** không được phép thực hiện hành động nhiều lần đồng thời cho cùng một hóa đơn. |
| Định giá và thanh toán | 2517465 | Các **Hủy kích hoạt chi tiết dòng hóa đơn** hành động bị chặn vì nó không được hỗ trợ. |
| Định giá và thanh toán | 2556660 | Đã sửa lỗi kiểm tra tính hiệu quả ngày được thực hiện trên bảng giá được đính kèm với bản ghi thông số dự án. |
|   Quản lý cơ hội | 2369202 | Đã chỉnh sửa logic nghiệp vụ xác minh rằng các bảng giá có ngày hiệu lực trùng nhau có thể được đính kèm vào cùng một hợp đồng dự án. |
|   Quản lý cơ hội | 2385965 | Đã sửa hành vi trên **Khách hàng** tab của **Hợp đồng dự án** trang khi bạn chọn **Lưu và đóng**. |
| Thời gian và chi phí | 2538503 | Một nhiệm vụ dự án phải có sẵn trong **Thực tế dự án** thực thể sau khi báo cáo chi phí được đăng. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Quản lý dự án và kế toán trên Dynamics 365 Finance

| Lĩnh vực tính năng | Số tham chiếu | Cập nhật chất lượng |
| --- | --- | --- |
| Quản lý dự án và kế toán | [615496](https://fix.lcs.dynamics.com/Issue/Details/?bugId=615496) | Trong quá trình nhập giấy báo có của nhà cung cấp, một lỗi xảy ra. Thông báo lỗi cho biết, "Số tiền sửa lại không được nhiều hơn số tiền thực còn lại." |
| Quản lý dự án và kế toán | [619391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=619391) | Nếu một đề xuất hóa đơn bao gồm bất kỳ giao dịch phí số tiền 0 nào là các thủ tục bán hàng chưa lập hóa đơn, thì việc lập hóa đơn không thể thực hiện được. |
| Quản lý dự án và kế toán | [624423](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624423) | Chi phí đã đăng không chính xác sau khi giá mua được cập nhật và **Kích hoạt quản lý thay đổi** được kích hoạt.|
| Quản lý dự án và kế toán | [628386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=628386) | Ước tính đăng tải cho một dự án giá cố định sử dụng đơn vị tiền tệ và số tiền không chính xác trong chứng từ ước tính, ngay cả khi **Bật đơn vị tiền tệ của hợp đồng dự án để tính toán ước tính** tính năng được kích hoạt. |
| Quản lý dự án và kế toán | [629239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=629239) | **ProjDMFDataPopulation\_ Sự mở rộng** không nên thực hiện cuộc gọi để bật theo dõi thay đổi mà không bắt các ngoại lệ cho các thực thể có khóa cấu hình chưa được bật. |
| Quản lý dự án và kế toán | [623818](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623818) | Công việc hàng loạt được khắc phục khi nhiều tạp chí nâng cao được đăng và lỗi xảy ra. |
| Đi lại và chi tiêu | [616805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616805) | Do một vấn đề quyết toán liên quan đến các khoản tạm ứng tiền mặt trên báo cáo chi phí, nên số thuế không được bao gồm như một phần của khoản tạm ứng tiền mặt. |
| Đi lại và chi tiêu | [616959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616959) | Thông tin thuế bán hàng không được bao gồm trên **Chi phí - Đã đăng giao dịch** báo cáo. |
| Đi lại và chi tiêu | [618943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=618943) | Các **Biên lai bắt buộc** vi phạm chính sách chi phí hiển thị không chính xác cảnh báo trên báo cáo chi phí. |
| Đi lại và chi tiêu | [633470](https://fix.lcs.dynamics.com/Issue/Details/?bugId=633470) | Một giao dịch dự án không bao gồm thuế bán hàng không thu hồi được trong tổng số tiền bán hàng khi giao dịch là kết quả của chi phí dặm bay. |
| Đi lại và chi tiêu | [642979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642979) | Khi một dòng được chia thành từng khoản có thuế, bạn không thể thay đổi ngày của dòng thành khoản và xảy ra lỗi trạng thái tài liệu nguồn. |

## <a name="removed-and-deprecated-features"></a>Các tính năng đã bị xóa và không dùng nữa

Các [Các tính năng bị xóa hoặc không dùng nữa trong Hoạt động dự án](removed-depreciated-features-project.md) chủ đề mô tả các tính năng đã bị xóa hoặc không được dùng nữa đối với Dynamics 365 Project Operations.

- Tính năng đã xóa không còn khả dụng trong sản phẩm.
- Một tính năng không dùng nữa không được phát triển tích cực và có thể bị xóa trong bản cập nhật trong tương lai.

Thông báo ngừng sử dụng sẽ xuất hiện trong [Các tính năng bị xóa hoặc không dùng nữa trong Hoạt động dự án](removed-depreciated-features-project.md) chủ đề 12 tháng trước khi bất kỳ tính năng nào bị xóa khỏi sản phẩm.

Đối với các thay đổi vi phạm chỉ ảnh hưởng đến thời gian biên dịch, nhưng tương thích nhị phân với hộp cát và môi trường sản xuất, thời gian ngừng sử dụng sẽ dưới 12 tháng. Thông thường, những thay đổi này là các cập nhật chức năng phải được thực hiện cho trình biên dịch.
