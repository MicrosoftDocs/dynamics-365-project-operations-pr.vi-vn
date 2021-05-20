---
title: Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 28, V3
description: Chủ đề này liệt kê các tính năng và bản sửa lỗi có trong Bản phát hành cập nhật Project Service Automation 28, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: 2d5e8c629f8108ed039948ca70842c9d8afebfa6
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948715"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a>Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 28, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Chúng tôi vui mừng thông báo bản cập nhật mới nhất dành cho ứng dụng Project Service Automation của Dynamics 365. Bản phát hành này bao gồm một số cải tiến quan trọng về chất lượng, hiệu suất và khả năng sử dụng. Bản phát hành này tương thích với Dynamics 365 9.x. Để cập nhật lên bản phát hành này, hãy truy cập vào Trung tâm quản trị cho trang giải pháp trực tuyến Dynamics 365 để cài đặt bản cập nhật. Để biết thêm thông tin, hãy xem [Cài đặt, cập nhật hoặc xóa giải pháp ưu tiên](/power-platform/admin/install-remove-preferred-solution).

Chủ đề này liệt kê các tính năng và bản sửa lỗi mới hoặc đã thay đổi đối với bản phát hành cập nhật 28 của Project Service Automation V3. Phiên bản này có số bản dựng là V3.10.46.32 và thường ra mắt rộng rãi thông qua bản tự cập nhật vào tháng 1 năm 2021.

## <a name="update-release-28"></a>Phát hành bản cập nhật 28

### <a name="bug-fixes"></a>Sửa lỗi

**Thời gian và Chi phí**

Các vấn đề sau đã được khắc phục:

- Người dùng có thể sử dụng tính năng **Chỉnh sửa hàng loạt** để cập nhật các mục thời gian đã được phê duyệt hoặc gửi.

**Quản lý dự án**

Các vấn đề sau đã được khắc phục:

- Trong trường hợp nhiệm vụ GUID được diễn giải dưới dạng số, bạn không thể mở các nhiệm vụ để chỉnh sửa bằng tính năng **Chỉnh sửa nhiệm vụ** ở ruy-băng trên trang **Cấu trúc phân tích công việc**.

**Sales**

Các vấn đề sau đã được khắc phục:

- Hệ thống sẽ tạo một ngoại lệ tham chiếu rỗng khi phần bổ trợ **GetEstimatesForProject** được gọi.
- **Đánh dấu là sẵn sàng lập hóa đơn** trên lưới mốc chỉ cập nhật một phần các thuộc tính, ngoại trừ thuộc tính **Trạng thái hóa đơn** đã được cập nhật.



[!INCLUDE[footer-include](../includes/footer-banner.md)]