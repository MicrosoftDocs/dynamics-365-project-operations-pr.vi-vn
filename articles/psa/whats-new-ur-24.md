---
title: Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 24, V3
description: Chủ đề này liệt kê các tính năng và bản sửa lỗi có trong Bản phát hành cập nhật Project Service Automation 24, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 15fe1c3482de66331dd543ee73391638919b2595
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146734"
---
# <a name="project-service-automation-update-release-24-v3"></a>Phát hành bản cập nhật Project Service Automation 24, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Chúng tôi vui mừng thông báo bản cập nhật mới nhất dành cho ứng dụng Project Service Automation của Dynamics 365. Bản phát hành này bao gồm một số cải tiến quan trọng về chất lượng, hiệu suất và khả năng sử dụng. Bản phát hành này tương thích với Dynamics 365 9.x. Để cập nhật lên bản phát hành này, hãy truy cập vào Trung tâm quản trị cho trang giải pháp trực tuyến Dynamics 365 để cài đặt bản cập nhật. Để biết thêm thông tin, hãy xem [Cài đặt, cập nhật hoặc xóa giải pháp ưu tiên](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Chủ đề này liệt kê các tính năng và bản sửa lỗi mới hoặc đã thay đổi cho Project Service Automation V3, Bản phát hành cập nhật 24. Phiên bản này có số bản dựng là V 3.10.42.43 và thường có sẵn thông qua bản tự cập nhật vào tháng 10 năm 2020.

## <a name="update-release-24"></a>Phát hành bản cập nhật 24

### <a name="bug-fixes"></a>Sửa lỗi

**Sales**

Các vấn đề sau đã được khắc phục:

- Sự cố khi đặt bảng giá mặc định của sản phẩm.
- Hiệu suất giành được báo giá đang chậm do bản sao của bản ghi bảng giá và giá vai trò được nhúng.
- **Hợp đồng dự án/Trung tâm bán hàng** > **Hạng mục sản phẩm/Số lượng mô tả đơn hàng** được tự động làm tròn đến số nguyên gần nhất.
- Nâng cao đặc quyền hệ thống khi đọc bảng giá.
- Sao chép các trường địa chỉ khách hàng **address1_freighttermscode** và **address1_shippingmethodcode** vào Báo giá/Đơn hàng. 


**Thời gian và Chi phí**

Các vấn đề sau đã được khắc phục:

- **Lưới mục nhập thời gian** không hỗ trợ hành vi thời gian **Chỉ ngày**.
- **Mục nhập thời gian** không tự động làm mới. Làm mới thủ công là bắt buộc.
- Không thể nhập các mục nhập thời gian từ mục phân công khi có thời gian giải lao (0 giờ) trong mục phân công của nguồn lực.
- Khi tạo mục nhập thời gian, hãy đặt thời gian bắt đầu giống như **msdyn_date**.
- Bật lại tính năng chỉnh sửa hàng loạt cho mục nhập thời gian.

**Quản lý nguồn lực**

Các vấn đề sau đã được khắc phục:

- Việc cố gắng cập nhật trạng thái đặt trước giữa các ngày mà không có yêu cầu sẽ đưa ra ngoại lệ null-ref.
- Lỗi khi tải **Dạng xem điều hòa**.


**Quản lý dự án**

Các vấn đề sau đã được khắc phục:

- Trong **Lịch trình dự án**, khi chuyển từ **Thủ công** sang **Tự động**, quá trình lưu tự động không hoàn thành.
- Chí phí không được phép tính vào mức chênh lệch trên **Lưới theo dõi dự án**.
- Hành vi không nhất quán đối với cột **Thẻ ước tính** trong khi tải so với thay đổi loại **Thời gian - Giai đoạn**.
- Chi phí thực tế của một dự án có thể không phản ánh tổng số từ **Thực tế**.
- **Ngày kết thúc ước tính** trên tab **Tóm tắt** không khớp với **Lịch trình WBS**.
- **Cập nhật giờ thực tế** trên phần nhô lề không hoạt động chính xác.
- Người quản lý dự án bên ngoài **BU** gốc không thể tạo dự án.
- Các thay đổi đối với nhiệm vụ hoặc thể loại trên **Ước tính chi phí** không tồn tại.
- **Bản sao hợp đồng** sao chép lịch trình hóa đơn và trạng thái chạy.
- Nút **Làm mới giá trị thực tế** tính toán không chính xác các nhiệm vụ tóm tắt.
- Phần bổ trợ Microsoft Project: Khắc phục lỗi tham chiếu rỗng nếu bất kỳ thành viên nào trong nhóm có đơn vị cung ứng nguồn lực trống.



[!INCLUDE[footer-include](../includes/footer-banner.md)]