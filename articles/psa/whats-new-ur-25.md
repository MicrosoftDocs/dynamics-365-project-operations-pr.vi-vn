---
title: Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 25, V3
description: Chủ đề này liệt kê các tính năng và bản sửa lỗi có trong Bản phát hành cập nhật Project Service Automation 25, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: 9d8ac559be2c23396604c61caae83c8a5328869d76218c6d8b3b6a6a6b32c1eb
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996597"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a>Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 25, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Chúng tôi vui mừng thông báo bản cập nhật mới nhất dành cho ứng dụng Project Service Automation của Dynamics 365. Bản phát hành này bao gồm một số cải tiến quan trọng về chất lượng, hiệu suất và khả năng sử dụng. Bản phát hành này tương thích với Dynamics 365 9.x. Để cập nhật lên bản phát hành này, hãy truy cập vào Trung tâm quản trị cho trang giải pháp trực tuyến Dynamics 365 để cài đặt bản cập nhật. Để biết thêm thông tin, hãy xem [Cài đặt, cập nhật hoặc xóa giải pháp ưu tiên](/power-platform/admin/install-remove-preferred-solution).

Chủ đề này liệt kê các tính năng và bản sửa lỗi mới hoặc đã thay đổi đối với Project Service Automation V3, Bản phát hành cập nhật 25. Phiên bản này có số bản dựng là 3.10.43.76 và thường được cung cấp đại trà thông qua bản tự cập nhật vào tháng 10 năm 2020.

## <a name="update-release-25"></a>Phát hành bản cập nhật 25

### <a name="bug-fixes"></a>Sửa lỗi

**Thời gian và Chi phí**

Sự cố sau đây đã được khắc phục:

- Biểu đồ mục nhập thời gian hiển thị dữ liệu bổ sung dựa trên khoảng thời gian được truy xuất quá lớn.

**Quản lý nguồn lực**

Sự cố sau đây đã được khắc phục:

- Đã thêm mã package deployer để bỏ qua bước nhập bản vá Universal Resource Scheduling nếu bản vá phiên bản cao hơn đã tồn tại.

**Quản lý dự án**

Các vấn đề sau đã được khắc phục:

- Sửa sự chênh lệch về làm tròn và tỷ giá hối đoái dẫn đến chi phí dự kiến không chính xác trong lưới theo dõi dự án.
- Hỗ trợ khả năng hiển thị hai hoặc nhiều lưới phản ứng trên biểu mẫu **Dự án**.
- Cung cấp tính năng xác thực để giải quyết khả năng chỉ định một nhiệm vụ quá ngày kết thúc theo lịch, dẫn đến việc chỉ định nguồn lực không thành công.
- Cải thiện khả năng xử lý lỗi để giải quyết Ngoại lệ tham chiếu null được tạo ra từ các trường hợp sau:

    - Phần bổ trợ **PreValidateProjectTeamMemberCreate**
    - **PreValidateProjectTaskCreate** khi một nhiệm vụ dự án được tạo mà không có một dự án được liên kết
    - Phần bổ trợ **PreProjectTeamMemberCreate**
    - Phần bổ trợ **PostProjectTeamMemberDelete**
    - Phần bổ trợ **PreValidateProjectTaskDelete**

**Sales**

Các vấn đề sau đã được khắc phục:

- Cải thiện khả năng xử lý lỗi để giải quyết các Ngoại lệ tham chiếu null được tạo ra từ **Copy Project: Estimates HelperResource Management**.
- Mục **Chưa sẵn sàng để lập hóa đơn** trên mục **Tồn đọng thanh toán cho thời gian và vật tư** không xóa trạng thái thanh toán.
- Đã sửa nút **Giá** bị gắn nhãn sai trên tab **Giá vai trò** và **Mục trong danh mục**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]