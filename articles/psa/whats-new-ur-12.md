---
title: Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 12, V3
description: Chủ đề này cung cấp thông tin về tính năng mới trong Phát hành bản cập nhật Project Service Automation 12, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: 62c3a0c5cfbecb568faef570da309c20afd86de9
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087069"
---
# <a name="project-service-automation-update-release-12-v3"></a>Phát hành bản cập nhật Project Service Automation 12, V3
Chúng tôi vui mừng thông báo bản cập nhật mới nhất cho ứng dụng Dynamics 365 Project Service Automation (PSA). Bản phát hành này bao gồm một số cải tiến quan trọng về chất lượng, hiệu suất và khả năng sử dụng. Bản phát hành này tương thích với Dynamics 365 9.x. Để cập nhật lên bản phát hành này, hãy truy cập vào Trung tâm quản trị cho Dynamics 365 trực tuyến và truy cập vào trang giải pháp để cài đặt bản cập nhật. Để biết thêm thông tin, hãy xem [Cài đặt, cập nhật hoặc xóa giải pháp ưu tiên](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Chủ đề này liệt kê các tính năng và bản sửa lỗi mới hoặc đã thay đổi cho Project Service Automation V3, Bản phát hành cập nhật 12. Phiên bản này có số bản dựng là V3.10.2.34 và thường có sẵn thông qua bản tự cập nhật vào tháng 10 năm 2019.

## <a name="update-release-12"></a>Phát hành bản cập nhật 12

### <a name="bug-fixes"></a>Sửa lỗi

- Thời gian và Chi phí

    - Đã sửa lỗi: Thông báo lỗi nhập thời gian đã được cập nhật với ngữ cảnh phù hợp hơn.
    - Đã sửa lỗi: Lưới nhập thời gian và lịch trình hiển thị chính xác thanh cuộn dọc khi được yêu cầu.
    - Đã sửa lỗi: Bạn không thể phê duyệt các mục nhập thời gian và chi phí đã gửi.
    - Đã sửa lỗi: Thông báo trên hộp thoại xác nhận hủy phê duyệt đã được sửa để phản ánh trạng thái phê duyệt khi thay đổi từ **Đã phê duyệt** thành **Đã gửi**.
    - Đã sửa lỗi: Trường **Giá** , **Đơn vị** và **Số lượng** hiện đã bị khóa trên bản ghi Chi phí sau khi đã được phê duyệt.

- Quản lý dự án

    - Đã sửa lỗi: Hành động **Mới** trong biểu mẫu chính **Thành viên nhóm** đã bị xóa.
    - Đã sửa lỗi: Việc gán tài nguyên đã được cập nhật để giải thích cho các lỗi làm tròn không chính xác, dẫn đến sự thay đổi trong ngày kết thúc của nhiệm vụ.
    - Đã sửa lỗi: Trong lưới nhiệm vụ, các lỗi phía máy chủ có liên quan sẽ xuất hiện cho người dùng.
    - Đã sửa lỗi: Tên của thành viên trong nhóm hiện hiển thị trong bộ chọn người thực hiện nhiệm vụ thay vì tên vị trí.

- Quản lý nguồn lực

    - Đã sửa lỗi: Chi tiết yêu cầu nguồn lực cho các dự án được tạo từ mẫu hiện sử dụng lịch dự án.
    - Đã sửa lỗi: Các kỹ năng và năng lực hiện được mặc định từ dữ liệu chính của vai trò đến yêu cầu nguồn lực được tạo cho vai trò đó.

- Sales

    - Đã sửa lỗi: Đã tìm thấy ID đối tượng trùng lặp trong biểu mẫu **chính của Hợp động**.
    - Đã sửa lỗi: Logic đã được cập nhật để hiển thị tab **Phân tích báo giá** sao cho tab này hiển thị thiết lập siêu dữ liệu của tab.
    - Đã sửa lỗi: Ngày tháng kế toán trên bản ghi thực bắt nguồn từ ngày nhập thời gian/chi phí và không phải ngày phê duyệt.