---
title: Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 18, V3
description: Chủ đề này liệt kê các tính năng và bản sửa lỗi có trong Bản phát hành cập nhật Project Service Automation 18, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: d6e0bb669513185ca266858ea9b8a89ed6dd4408
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147229"
---
# <a name="project-service-automation-update-release-18-v3"></a>Phát hành bản cập nhật Project Service Automation 18, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Chúng tôi vui mừng thông báo bản cập nhật mới nhất dành cho ứng dụng Project Service Automation của Dynamics 365. Bản phát hành này bao gồm một số cải tiến quan trọng về chất lượng, hiệu suất và khả năng sử dụng. Bản phát hành này tương thích với Dynamics 365 9.x. Để cập nhật lên bản phát hành này, hãy truy cập vào Trung tâm quản trị cho Dynamics 365 trực tuyến, rồi chuyển đến trang giải pháp để cài đặt bản cập nhật. Để biết thêm thông tin, hãy xem [Cài đặt, cập nhật hoặc xóa giải pháp ưu tiên](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Chủ đề này liệt kê các tính năng và bản sửa lỗi mới hoặc đã thay đổi cho Project Service Automation V3, Bản phát hành cập nhật 18. Phiên bản này có số bản dựng là V3.10.8.12 và thường có sẵn thông qua bản tự cập nhật vào tháng 4 năm 2020.

## <a name="update-release-18"></a>Phát hành bản cập nhật 18

### <a name="bug-fixes"></a>Sửa lỗi

**Thời gian và Chi phí**

- Đã sửa: Dòng **Thu hồi**, **Yêu cầu** và **Hủy phê duyệt** trả về ngoại lệ có thông báo lỗi không rõ ràng.
- Đã sửa: Khi **Hủy phê duyệt** không thành công đối với chi phí, một lỗi ngoại lệ có liên quan không được trả về.
- Đã sửa: Lưới Mục nhập thời gian xử lý không chính xác những ngày không làm việc ở Úc sau khi chuyển đổi thời gian tiết kiệm ánh sáng ban ngày (DST) vào tháng 10.
- Đã sửa: Logic mặc định không chính xác ngăn việc gửi chi phí.
- Đã sửa: Khi phê duyệt mục nhập thời gian không thành công, phê duyệt vẫn ở trạng thái **Đang chờ xử lý**.
- Đã sửa: Lỗi SQL trên các phê duyệt hàng loạt (khóa chết/thời gian chờ).
- Đã sửa: Các sự cố hiệu suất đáng kể trong trải nghiệm người dùng gây ra bằng cách cập nhật thành viên trong nhóm trong khi phê duyệt các mục thời gian.

**Quản lý dự án**

- Đã sửa: Thông báo múi giờ được chuyển từ dạng xem **Điều hòa** thành biểu mẫu chính của **Dự án**.
- Đã sửa: Mẫu lịch không được mặc định chính xác khi biểu mẫu của dự án mới mở.
- Đã sửa: Đối với các trình duyệt dựa trên chromium, người dùng không thể dễ dàng chọn các tác vụ trước đó để xóa.
- Đã sửa: Tạo hoặc sao chép **Dự án từ mẫu rỗng** tìm nạp các nhiệm vụ không liên quan.
- Đã sửa: Trong các trường hợp cụ thể, việc tạo một nhiệm vụ mới từ lưới tác vụ dẫn đến các bản ghi trùng lặp được tạo.
- Đã sửa: Trong chế độ thủ công, người dùng không thể cập nhật ngày bắt đầu tác vụ muộn hơn ngày hiện tại được lưu.

**Quản lý nguồn lực**

- Đã sửa: Hàng tổng dạng xem **Điều hòa** tính sai phương sai đặt chỗ sau khi mở rộng đặt chỗ.
- Đã sửa: Dạng xem **Điều hòa** hiển thị không chính xác việc gán nguồn lực khi nguồn lực có thể ghi được có lịch không khớp với lịch dự án.

**Sales**

- Đã sửa: Khi các mục nhập thời gian được phê duyệt lại (**Phê duyệt > Hủy>** phê duyệt lại), giá trị thực tế không tính phí trùng lặp được tạo ra.


[!INCLUDE[footer-include](../includes/footer-banner.md)]