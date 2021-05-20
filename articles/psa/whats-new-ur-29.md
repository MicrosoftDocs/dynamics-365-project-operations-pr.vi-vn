---
title: Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 29, V3
description: Chủ đề này liệt kê các tính năng và bản sửa lỗi có trong Bản phát hành cập nhật Project Service Automation 29, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 2ac47974b9cc8386c7446136faf48724de73efce
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948688"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a>Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 29, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Chúng tôi vui mừng thông báo bản cập nhật mới nhất dành cho ứng dụng Project Service Automation của Dynamics 365. Bản phát hành này bao gồm một số cải tiến quan trọng về chất lượng, hiệu suất và khả năng sử dụng. Bản phát hành này tương thích với Dynamics 365 9.x. Để cập nhật lên bản phát hành này, hãy truy cập vào Trung tâm quản trị cho trang giải pháp trực tuyến Dynamics 365 để cài đặt bản cập nhật. Để biết thêm thông tin, hãy xem [Cài đặt, cập nhật hoặc xóa giải pháp ưu tiên](/power-platform/admin/install-remove-preferred-solution).

Chủ đề này liệt kê các tính năng và bản sửa lỗi mới hoặc đã thay đổi cho Project Service Automation V3, Bản phát hành cập nhật 29. Phiên bản này có số bản dựng là V3.10.47.7 và thường ra mắt rộng rãi thông qua bản tự cập nhật vào tháng 2 năm 2021.

## <a name="update-release-29"></a>Phát hành bản cập nhật 29

### <a name="bug-fixes"></a>Sửa lỗi

**Thời gian và Chi phí**

Các vấn đề sau đã được khắc phục:

- Người dùng không thể xem giờ làm việc được ghi vào những ngày không làm việc trong lưới nhập thời gian.
- Các mục chi phí đã được phê duyệt có thể được chỉnh sửa trên lưới.

**Quản lý dự án**

Các vấn đề sau đã được khắc phục:

- Thiếu logic xác thực để đảm bảo giờ nỗ lực phân công tài nguyên không thể bị âm.
- Hành động tùy chỉnh, **AssignResourcesForTask** cập nhật tất cả các trường thay vì chỉ các trường đã thay đổi.
- Khi sao chép một dự án trong một môi trường có phần bổ trợ hoặc quy trình công việc được đăng ký trên sự kiện **CreateProject**, thuộc tính **msdyn_bulkgenerationstatus** không được cập nhật nếu **CopyWBSToProject** lỗi.
- Khi bạn mở rộng lịch dự án, ngày làm việc không được sắp xếp theo thứ tự tăng dần khiến một số cập nhật nhiệm vụ dự án không thành công.
- Việc thay đổi Trình quản lý dự án trên một dự án hiện có sẽ kích hoạt logic mặc định của đơn vị tổ chức.

**Bán hàng**

Các vấn đề sau đã được khắc phục:

- Tab **Thực hiện hợp đồng** trên trang **Hợp đồng** không thành công trong quá trình khởi tạo khi không có dòng hợp đồng nào.