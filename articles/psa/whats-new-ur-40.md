---
title: Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 40, V3
description: Chủ đề này liệt kê các tính năng và bản sửa lỗi có sẵn trong Microsoft Dynamics 365 Project Service Automation Bản phát hành cập nhật 40, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/31/2022
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
ms.openlocfilehash: 25f375ce648eb7d233f6433739832caee351830d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588670"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-40-v3"></a>Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 40, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Chúng tôi vui mừng được công bố bản cập nhật mới nhất cho ứng dụng Microsoft Dynamics 365 Project Service Automation. Bản phát hành này bao gồm một số cải tiến quan trọng về chất lượng, hiệu suất và khả năng sử dụng. Bản này tương thích với Dynamics 365 9.x. Để cập nhật lên bản phát hành này, hãy truy cập trang giải pháp trực tuyến Trung tâm quản trị cho Dynamics 365 và cài đặt bản cập nhật. Để biết thêm thông tin, hãy xem [Cài đặt, cập nhật hoặc xóa giải pháp ưu tiên](/power-platform/admin/install-remove-preferred-solution).

Chủ đề này liệt kê các tính năng và bản sửa lỗi mới hoặc đã thay đổi cho Project Service Automation, Bản phát hành cập nhật 40, V3. Phiên bản này có số bản dựng là V3.10.61.61 và thường có sẵn thông qua bản tự cập nhật vào tháng 2 năm 2022.

## <a name="update-release-40"></a>Phát hành bản cập nhật 40

### <a name="features"></a>Tính năng
Giai đoạn 1 của quá trình nâng cấp từ Tự động hóa dịch vụ dự án lên Vận hành dự án - Lite sẽ được phát hành vào tháng 2 năm 2022 cho tất cả khách hàng. Để kiểm tra tính đủ điều kiện, hãy xem [Nâng cấp từ Tự động hóa dịch vụ dự án lên Vận hành dự án](upgrade-project-operations-non-stocked.md). Nếu ứng dụng không xuất hiện trong phiên bản của bạn trong Power Platform Trung tâm quản trị, liên hệ với bộ phận hỗ trợ và yêu cầu bật chuyến bay cho môi trường của bạn. Yêu cầu của bạn phải bao gồm danh sách ID môi trường mà chuyến bay cần được kích hoạt.

### <a name="bug-fixes"></a>Sửa lỗi

Các vấn đề sau đã được khắc phục.

**Thời gian và Chi phí**
- Mục nhập ghi chú bị thiếu khi mục nhập thời gian bị từ chối hoặc bị hủy. 

**Bán hàng**

- Khi bạn cập nhật ước tính chi phí hoặc doanh số bằng cách sử dụng các trình cắm bổ sung, bạn không được phép gửi các tải trọng JSON không hợp lệ ra bên ngoài giao diện người dùng.
- Khi bạn cập nhật các dòng trích dẫn bằng cách sử dụng chế độ xem nhanh, bạn được phép kích hoạt các báo giá.
