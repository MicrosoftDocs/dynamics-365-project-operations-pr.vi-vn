---
title: Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 27, V3
description: Chủ đề này liệt kê các tính năng và bản sửa lỗi có trong Bản phát hành cập nhật Project Service Automation 27, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 8879229b50ef113d6d6cb8622b707f0c12182a57
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280334"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-27-v3"></a>Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 27, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Chúng tôi vui mừng thông báo bản cập nhật mới nhất dành cho ứng dụng Project Service Automation của Dynamics 365. Bản phát hành này bao gồm một số cải tiến quan trọng về chất lượng, hiệu suất và khả năng sử dụng. Bản phát hành này tương thích với Dynamics 365 9.x. Để cập nhật lên bản phát hành này, hãy truy cập vào Trung tâm quản trị cho trang giải pháp trực tuyến Dynamics 365 để cài đặt bản cập nhật. Để biết thêm thông tin, hãy xem [Cài đặt, cập nhật hoặc xóa giải pháp ưu tiên](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Chủ đề này liệt kê các tính năng và bản sửa lỗi mới hoặc đã thay đổi cho Project Service Automation V3, Bản phát hành cập nhật 27. Phiên bản này có số bản dựng là V3.10.45.98 và thường ra mắt rộng rãi thông qua bản tự cập nhật vào tháng 1 năm 2021.

## <a name="update-release-27"></a>Phát hành bản cập nhật 27

### <a name="bug-fixes"></a>Sửa lỗi

**Sự cố chung**

Các vấn đề sau đã được khắc phục:

- Nhật ký tạo bằng phần bổ trợ trong Project Service Automation chưa được đặt thành tự động xóa.
- Tự động cập nhật thất bại do giải pháp Project Service Automation chứa giá trị rỗng cũ là NavBarArea và thành tố tiêu đề.

**Thời gian và Chi phí**

Các vấn đề sau đã được khắc phục:

- Lưới **Mục nhập thời gian** hiển thị dữ liệu không chính xác cho hành vi dữ liệu **Độc lập múi giờ**.
- Lưới **Mục nhập thời gian** tạo thời gian không chính xác cho hành vi dữ liệu **Độc lập múi giờ**.
- Tra cứu nhiệm vụ không bị giới hạn ở dự án đã chọn trên trang **Chỉnh sửa mục nhập thời gian**.
- Việc phê duyệt thời gian đối với các mục nhập thời gian bị chặn vì hệ thống sẽ tìm kiếm vai trò người phê duyệt dự án.
- Các mục nhập đúng trên tab Thực tế hiển thị thông báo lỗi không chính xác.
- Khi một nhiệm vụ chứa giá trị rỗng đối với chi phí thực tế và tổng dự án được làm mới, thông báo lỗi sau sẽ xuất hiện: "Khóa đã cho không có trong từ điển".
- Trong các bản thể hiện cụ thể, bộ lọc **Nhóm theo** trên tab **Ước tính dự án** không hiển thị ước tính các khoản chi tiêu.
- Khoảng **Giờ mùa hè** không chính xác đối với các mục nhập thời gian.

**Quản lý dự án**

Các vấn đề sau đã được khắc phục:

- Cải thiện bộ đệm, giúp tăng hiệu năng liên quan đến việc tải trang **Dự án**.
- Loại bỏ quy tắc kinh doanh làm cản trợ việc hoàn thành nhiệm vụ dự án.
- Các đường nối Phần bổ trợ Microsoft Project không tuân theo lịch của phần bổ trợ, làm cho các yêu cầu nguồn lực không chính xác.
- Việc tạo dự án bằng mẫu sẽ đặt ngày phân công không chính xác và cản trở khả năng tạo các yêu cầu nguồn lực.
- Người dùng không thể truy cập vào các tùy chọn **Danh mục**, **Mô tả**, **Trạng thái** bằng bàn phím.
- Giá trị bán hàng thực của dự án không bao gồm phí và giá trị bán hàng nguyên vật liệu.
- Cách tính tổng giá trị bán hàng thực và chi phí thực không chính xác do tỷ giá hối đoái khác nhau.
- Mô tả trong **Mẫu giờ làm việc mặc định** gây nhầm lẫn.
- Khi thụt dòng nhiệm vụ, tùy chọn **Danh mục** vẫn tồn tại trong giao diện người dùng cho đến khi làm mới.
- Thiếu sự xác thực để đảm bảo rằng việc di chuyển dự án ra ngoài ngày kết thúc là không được cho phép.

**Sales**

Các vấn đề sau đã được khắc phục:

- Ngoại lệ tham chiếu rỗng được tạo trên dòng báo giá dự án vì tùy chọn **Nhập từ ước tính dự án** không hiển thị sau khi đã chọn dự án.
- Lỗi "Tham chiếu đối tượng chưa được đặt thành một bản thể hiện của đối tượng" xảy ra khi đóng báo giá dưới dạng **Giành được**.
- Trạng thái sửa đổi không được thiết lập trong lần đảo ngược giá trị thực tế trong quá trình hủy liên kết dự án với dòng hợp đồng.
- Khi cài đặt cả Dynamics 365 Field Service và Project Service Automation, các tùy chọn **Khóa giá** và **Dùng giá hiện tại** không hiển thị cùng lúc trên trang **Hóa đơn**.
- Đối với tiếng Nhật, bản dịch không nhất quán với các trang khác dựa trên lịch.
- Tùy chọn **Kích hoạt** và **Hủy kích hoạt** bị xóa khỏi thực thể **Liên kết bảng giá** trong Project Service Automation.


[!INCLUDE[footer-include](../includes/footer-banner.md)]