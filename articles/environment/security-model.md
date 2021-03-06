---
title: Mô hình bảo mật
description: Chủ đề này cung cấp thông tin về mô hình bảo mật trong Dynamics 365 Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ffcfa8a9c8e31c5665acd3c3919fa90d36a3f3ca
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896757"
---
# <a name="security-model"></a>Mô hình bảo mật

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Microsoft Dynamics 365 Project Operations chứa một mô hình bảo mật duy nhất cho phép mô hình bảo mật kinh doanh dựa trên vai trò hợp tác với Microsoft Office Groups. 


## <a name="security-roles"></a>Vai trò bảo mật
Các khả năng ngoại vi của Project Operations bao gồm các vai trò sau:

| Vai trò                          | Nội dung mô tả                                                                                                                                                                 | Phạm vi |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|
| Người quản lý thực tiễn              | Hỗ trợ báo cáo dự án chéo.                                                                                                            | Đơn vị kinh doanh              |
| Người phê duyệt dự án              | Phê duyệt thời gian và chi phí cho dự án.                                                                                                                              | Đơn vị kinh doanh |
| Quản trị viên thanh toán dự án | Tạo đề xuất hóa đơn.                                                                                                                                                 | Đơn vị kinh doanh |
| Người quản lý dự án               | Tạo kế hoạch dự án và yêu cầu nguồn lực.                                                                                                                              | Đơn vị kinh doanh |
| Nguồn lực dự án              | Các thành viên trong nhóm có thể được đặt trước và báo cáo thời gian.                                                                                                          | Đơn vị kinh doanh|
| Resource Manager              | Tất cả các chức năng quản lý nguồn lực, chẳng hạn như thực hiện các yêu cầu và đặt chỗ nguồn lực, được tách riêng để hỗ trợ người quản lý Dự án kết hợp + Cấu hình trình quản lý nguồn lực và vai trò người quản lý Tài nguyên tập trung và duy nhất. | Đơn vị kinh doanh |


Microsoft Project cho Web bao gồm các vai trò sau:
| Vai trò                          | Nội dung mô tả                                                                                                          | Phạm vi |                                                       
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----|
| Người dùng dự án | Người dùng cộng tác của Dự án có thể tạo dự án của riêng họ và xem bất kỳ dự án nào được chia sẻ với họ.| Người dùng|
| Hệ thống dự án | Vai trò được sử dụng cho ngữ cảnh ứng dụng. Khách hàng không nên sử dụng vai trò hệ thống này. | Toàn bộ|

## <a name="security-enforcement"></a>Thực thi bảo mật
Các hành động được thực hiện ở cấp độ dự án được thực hiện trong ngữ cảnh của người dùng đã đăng nhập. Điều này có nghĩa là để tạo, mở hoặc xóa một dự án, người dùng bắt buộc phải có quyền truy cập trong CDS. Quyền truy cập trong CDS có thể được cấp thông qua bất kỳ cơ chế nào có thể có trong nền tảng. Ví dụ: người dùng có phạm vi lớn hơn có thể truy cập dự án hoặc nếu hành động chia sẻ dự án rõ ràng đã được thực hiện để cấp quyền truy cập cho người dùng.

Điều quan trọng là phải xem xét việc này khi tạo dự án trong Project Operations.

## <a name="modern-group-collaboration-with-project-operations"></a>Hợp tác nhóm hiện đại với Project Operations
Project for the Web và Project Operations hỗ trợ các nhóm hiện đại cộng tác. Người dùng được thêm vào dự án thông qua một nhóm có thể chỉnh sửa kế hoạch dự án.

Project for the Web tự động thêm người dùng vào nhóm khi được gán.

Groups cho phép các quyền của dự án và các tạo tác hỗ trợ cộng tác được thực hiện một cách hợp tác. Sơ đồ sau đây mô tả các sự kiện và thay đổi trạng thái xảy ra trong quy trình gán nhóm.

Project Operations không tạo ra một nhóm thông qua hành động ngầm và chỉ thực hiện thông qua hành động rõ ràng của các nhóm thúc ép.

Tìm kiếm thành viên nhóm trong **Quản lý nhóm**, được giới hạn cho những người được đặt là một phần của nhóm bảo mật của môi trường. Để biết thêm thông tin, xem [Kiểm soát quyền truy cập người dùng vào môi trường: nhóm bảo mật và giấy phép](https://docs.microsoft.com/power-platform/admin/control-user-access).

1. Dự án được tạo và do thuộc sở hữu của Người dùng tạo.
2. Chủ dự án được cập nhật vào nhóm.
3. Nhóm chủ sở hữu được ánh xạ tới Office Group được chỉ định hoặc đã tạo.
4. Chủ sở hữu ban đầu của Dự án được thêm vào Office Group.

## <a name="deployment-recommendation"></a>Đề xuất triển khai
Khi mô hình cộng tác nhóm Office phát triển, chức năng sẽ được thêm vào để cung cấp khả năng kiểm soát chi tiết hơn theo thời gian. Các khách hàng triển khai Project Operations ngày nay được khuyến khích tập trung vào Mô hình bảo mật Microsoft Dynamics 365.

Để biết thêm thông tin, hãy xem [Bảo mật trong Common Data Service](https://docs.microsoft.com/power-platform/admin/wp-security).

## <a name="project-operations-and-microsoft-dynamics-365-finance-security"></a>Project Operations và bảo mật Microsoft Dynamics 365 Finance
Project Operations bao gồm các vai trò sau:

- Người quản lý dự án
- Kế toán dự án

Để biết thêm thông tin về vai trò bảo mật trong Finance, hãy xem [Bảo mật dựa trên vai trò](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security).


