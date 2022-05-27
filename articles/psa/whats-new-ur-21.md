---
title: Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 21, V3
description: Chủ đề này liệt kê các tính năng và bản sửa lỗi có trong Bản phát hành cập nhật Project Service Automation 21, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: 34d1540639352f635068b849500a104de2509a7f
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8577861"
---
# <a name="project-service-automation-update-release-21-v3"></a>Phát hành bản cập nhật Project Service Automation 21, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Chúng tôi vui mừng thông báo bản cập nhật mới nhất dành cho ứng dụng Project Service Automation của Dynamics 365. Bản phát hành này bao gồm một số cải tiến quan trọng về chất lượng, hiệu suất và khả năng sử dụng. Bản phát hành này tương thích với Dynamics 365 9.x. Để cập nhật lên bản phát hành này, hãy truy cập vào Trung tâm quản trị cho trang giải pháp trực tuyến Dynamics 365 để cài đặt bản cập nhật. Để biết thêm thông tin, hãy xem [Cài đặt, cập nhật hoặc xóa giải pháp ưu tiên](/power-platform/admin/install-remove-preferred-solution).

Chủ đề này liệt kê các tính năng và bản sửa lỗi mới hoặc đã thay đổi cho Project Service Automation V3, Bản phát hành cập nhật 21. Phiên bản này có số bản dựng là V 3.10.32.50 và thường được cung cấp thông qua bản tự cập nhật vào tháng 6 năm 2020.

## <a name="update-release-21"></a>Phát hành bản cập nhật 21

### <a name="bug-fixes"></a>Sửa lỗi

**Thời gian và Chi phí**

Các vấn đề sau đã được khắc phục:

- Khi lưu trữ **Kiểm soát lưới mục nhập thời gian** trong Bảng điều khiển, lưới này không sử dụng toàn bộ chiều rộng của vùng chứa lưới bảng điều khiển.
- Đối với các múi giờ cụ thể, kiểm soát lưới **Mục nhập Thời gian** không hiển thị bản ghi.
- Các mục thời gian sau 21:00 sẽ hiển thị không đúng ngày.
- Người dùng không thể gửi chi phí nếu loại chi phí **Yêu cầu biên nhận chi phí** không có giá trị.

**Quản lý nguồn lực**

Các vấn đề sau đã được khắc phục:

- Các lượt đăng ký không hoạt động hiển thị ở dạng xem **Đối chiếu**.
- Quá trình thực hiện nguồn lực chung thiếu thông tin xác thực để đảm bảo rằng có tồn tại trạng thái đăng ký hợp lệ.

**Quản lý dự án**

Các vấn đề sau đã được khắc phục:

- Lưới biểu mẫu **Dự án** (**Gán Nguồn lực**, **Nhiệm vụ**, dạng xem **Đối chiếu**, **Ước tính Chi phí**) vẫn có thể chỉnh sửa ngay cả khi dự án không hoạt động.
- Không thể hợp nhất các khách hàng trùng lặp với những khách hàng liên kết với hợp đồng dự án đã xác nhận.
- Khi một nguồn lực không có lịch hợp lệ được thêm vào, hệ thống sẽ không trả về thông báo lỗi thân thiện với người dùng.
- Nút **Thêm Nhiệm vụ** trên lưới nhiệm vụ được bật khi dự án liên kết với **Phần bổ trợ Microsoft Project**.
- Nhân công tăng lên một cách không kiểm soát khi một nhiệm vụ có thể loại được giao cho một nguồn lực có vai trò được xác định giá vốn .

**Sales**

Chúng tôi đã thực hiện những cải tiến sau:

- **Tần suất Hóa đơn** và **Bắt đầu Thanh toán** đã được chuyển sang tab **Lập hóa đơn**.

Các vấn đề sau đã được khắc phục:

- **Tổng Giá bán** của **Thể loại** bằng không (0) mặc dù **Vai trò** có tổng giá bán khác 0.
- Khách hàng không thể thay đổi giá trị của trường **Trạng thái Hóa đơn** thành **Đã sẵn sàng để lập hóa đơn** khi một quy trình tùy chỉnh khác đang cập nhật một trường bổ sung.
- Nút **Làm mới Thông tin Hóa đơn** có thể tạo nhiều dòng trùng lặp nếu được chọn nhiều lần.
- Nút **Cập nhật giá** không hoạt động trên lưới con **Giá vai trò** trong biểu mẫu **Xem nhanh**.
- Logic **Giải pháp Bảng giá Bán hàng** xử lý không đúng múi giờ, dẫn đến việc lựa chọn bảng giá không chính xác.
- **Tổng Chi phí Thực tế** của dự án có thể được giảm một phần nhỏ sau khi một mục nhập thời gian được chấp thuận.
- Logic **Giải pháp Giá bán** không trả về thông báo lỗi thân thiện với người dùng nếu **Giá Vai trò Đã truy xuất** không có giá trị trong trường **"Đơn vị Chính"** và **"Giá theo Đơn vị Chính"**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
