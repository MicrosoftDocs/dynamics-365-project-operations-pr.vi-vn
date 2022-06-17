---
title: Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 28, V3
description: Bài viết này liệt kê các tính năng và bản sửa lỗi có sẵn trong Bản phát hành bản cập nhật tự động hóa dịch vụ dự án 28, V3.
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 56a87bce55c560e541e20709b10d38b9512ffcee
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930620"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a>Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 28, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Chúng tôi vui mừng thông báo bản cập nhật mới nhất dành cho ứng dụng Project Service Automation của Dynamics 365. Bản phát hành này bao gồm một số cải tiến quan trọng về chất lượng, hiệu suất và khả năng sử dụng. Bản phát hành này tương thích với Dynamics 365 9.x. Để cập nhật lên bản phát hành này, hãy truy cập vào Trung tâm quản trị cho trang giải pháp trực tuyến Dynamics 365 để cài đặt bản cập nhật. Để biết thêm thông tin, hãy xem [Cài đặt, cập nhật hoặc xóa giải pháp ưu tiên](/power-platform/admin/install-remove-preferred-solution).

Bài viết này liệt kê các tính năng và bản sửa lỗi mới hoặc được thay đổi cho Project Service Automation V3, Bản cập nhật 28 Phiên bản này có số bản dựng là V3.10.46.32 và thường có sẵn thông qua bản tự cập nhật vào tháng 1 năm 2021.

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
