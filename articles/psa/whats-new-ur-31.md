---
title: Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 31, V3
description: Bài viết này liệt kê các tính năng và bản sửa lỗi có trong Bản phát hành cập nhật Project Service Automation 31, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: 8d62b12a5363637e46b29c2e9edf4e1f17da729f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925054"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a>Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 31, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Chúng tôi vui mừng thông báo bản cập nhật mới nhất dành cho ứng dụng Project Service Automation của Dynamics 365. Bản phát hành này bao gồm một số cải tiến quan trọng về chất lượng, hiệu suất và khả năng sử dụng. Bản phát hành này tương thích với Dynamics 365 9.x. Để cập nhật lên bản phát hành này, hãy truy cập vào Trung tâm quản trị cho trang giải pháp trực tuyến Dynamics 365 để cài đặt bản cập nhật. Để biết thêm thông tin, hãy xem [Cài đặt, cập nhật hoặc xóa giải pháp ưu tiên](/power-platform/admin/install-remove-preferred-solution).

Bài viết này liệt kê các tính năng và bản sửa lỗi mới hoặc đã thay đổi cho Project Service Automation V3, Bản phát hành cập nhật 31. Phiên bản này có số bản dựng là V3.10.52.77 và thường có sẵn thông qua bản tự cập nhật vào tháng 5 năm 2021.

## <a name="update-release-31"></a>Phát hành bản cập nhật 31

### <a name="bug-fixes"></a>Sửa lỗi

**Thời gian và Chi phí**

Các vấn đề sau đã được khắc phục:

- Các nút lệnh điều khiển mục nhập thời gian trên trang **Nguồn lực có thể đặt trước** gây khó hiểu.
- Một ngoại lệ tham chiếu rỗng đã được tạo trong **Project.SetTrackingFields** khi phê duyệt mục nhập thời gian.

**Quản lý nguồn lực**

Các vấn đề sau đã được khắc phục:

- **Tạo thành viên trong nhóm** không hiển thị chính xác cài đặt siêu dữ liệu về thiết lập đăng ký cho **Trạng thái cam kết đăng ký mặc định**.
- Khi nâng cấp từ PSA 1.X lên 3.X, quá trình nâng cấp không thành công tại **UpgradeResourceRequirements**.


**Bán hàng**

Các vấn đề sau đã được khắc phục:

- Doanh thu thực tế chuyển đổi số tiền sang đơn vị tiền tệ của dự án trong bảng theo dõi.
- Đơn vị tiền tệ mặc định không rõ ràng khi tạo dòng nhật ký kế toán, mô tả báo giá và mô tả hợp đồng trong các tình huống mà đơn vị tiền tệ cơ bản của một tổ chức khác với đơn vị tiền tệ của dự án.
- Truy vấn **Đang chờ xác thực nhật ký sửa chữa** không lọc theo dự án.
- Doanh số còn lại được tính không chính xác trên một dự án.
- Báo giá dựa trên liên hệ không thành công khi được tạo mà không có bảng giá.
- Không có vòng xoay xử lý nào được hiển thị khi bạn chọn **Xác nhận hóa đơn**.
- Không có vòng xoay xử lý nào được hiển thị khi bạn chọn **Tạo hóa đơn**.
- Việc đóng một báo giá khi bị mất không hủy bỏ các lượt đăng ký.







