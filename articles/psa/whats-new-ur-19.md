---
title: Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 19, V3
description: Chủ đề này liệt kê các tính năng và bản sửa lỗi có trong Bản phát hành cập nhật Project Service Automation 19, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: 0137d0241238ff96de406884dd05a5d7f023c318
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949165"
---
# <a name="project-service-automation-update-release-19-v3"></a>Phát hành bản cập nhật Project Service Automation 19, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Chúng tôi vui mừng thông báo bản cập nhật mới nhất dành cho ứng dụng Project Service Automation của Dynamics 365. Bản phát hành này bao gồm một số cải tiến quan trọng về chất lượng, hiệu suất và khả năng sử dụng. Bản phát hành này tương thích với Dynamics 365 9.x. Để cập nhật lên bản phát hành này, hãy truy cập vào Trung tâm quản trị cho trang giải pháp trực tuyến Dynamics 365 để cài đặt bản cập nhật. Để biết thêm thông tin, hãy xem [Cài đặt, cập nhật hoặc xóa giải pháp ưu tiên](/power-platform/admin/install-remove-preferred-solution).

Chủ đề này liệt kê các tính năng và bản sửa lỗi mới hoặc đã thay đổi cho PSA V3, Bản phát hành cập nhật 19. Phiên bản này có số bản dựng là V3.10.30.41 và thường có sẵn thông qua bản tự cập nhật vào tháng 5 năm 2020.

## <a name="update-release-19"></a>Phát hành bản cập nhật 19

### <a name="bug-fixes"></a>Sửa lỗi

**Thời gian và Chi phí**

Các vấn đề sau đã được khắc phục: 

- Lỗi xuất phát từ mục nhập thời gian hiển thị không chính xác.
- Lưới mục nhập thời gian không hỗ trợ hành vi trường **Chỉ ngày**.
- Nguồn lực dự án không thể tạo ra một chi phí với một dự án.

**Quản lý dự án**

Các vấn đề sau đã được khắc phục: 

-  Nhiệm vụ cháu gây ra ước tính nỗ lực không chính xác trong khi Tính toán hoàn thành (EAC).

**Sales**

Các vấn đề sau đã được khắc phục: 

- Hành động **Tính toán lại** không hoạt động với chi tiết mô tả hợp đồng chi phí hoặc chi tiết mô tả báo giá.
- **Cập nhật giá** bị thiếu cho ước tính chi phí.
-  Khách hàng không thể chọn lý do dẫn đến trạng thái hợp đồng tùy chỉnh từ trang **Hợp đồng dự án**.
- Khách hàng trải nghiệm hiệu suất xuống cấp khi tạo một bảng giá tùy chỉnh từ một báo giá.
- Trải nghiệm khách hàng không nhất quán với **đơn vị** mặc định trên các trang **Chi tiết mô tả báo giá** và **Chi tiết mô tả hợp đồng**.
- Việc thêm các mục danh mục giao dịch không thể tính phí vào mô tả hợp đồng có thể tính phí sẽ không tôn trọng loại thanh toán **Không thể tính phí** của danh mục giao dịch.
- Khách hàng không thể sử dụng các vai trò và danh mục mới được thêm trên các hợp đồng được tạo trước đó.
- Khách hàng trải nghiệm hiệu suất bị suy giảm Truy xuất không cần thiết trong PreValidateProjectTeamMemberUpdate.cs
- Vai trò được thiết lập là không thể tính phí trong danh sách **Danh mục nguồn lực** nên được thêm vào tab **Vai trò có thể tính phí** dưới dạng **Không thể tính phí** trên mô tả hợp đồng cho một dự án.
- Khách hàng có thể gặp hiệu suất xuống cấp khi tạo dự án vì **GetBookableResourceIdFromUser** truy xuất tất cả các cột của nguồn lực có thể đặt trước thay vì chỉ truy xuất ID chính.
- Thực thể **Loại giao dịch** thiếu phần bổ trợ cập nhật xác thực trước để ngăn người dùng nhập **Đơn vị** và **Nhóm đơn vị** không hợp lệ cho các loại giao dịch.
- Bước **Loại bỏ** không hoạt động để nhập mục nhập thời gian.


[!INCLUDE[footer-include](../includes/footer-banner.md)]