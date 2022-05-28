---
title: Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 15, V3
description: Chủ đề này cung cấp thông tin về tính năng mới trong Phát hành bản cập nhật Project Service Automation 15, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
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
ms.openlocfilehash: 26b9ee0a6ff1ad81d6c77a6a7091733667c493ff
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585174"
---
# <a name="project-service-automation-update-release-15-v3"></a>Phát hành bản cập nhật Project Service Automation 15, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Chúng tôi vui mừng thông báo bản cập nhật mới nhất cho ứng dụng Dynamics 365 Project Service Automation (PSA). Bản phát hành này bao gồm một số cải tiến quan trọng về chất lượng, hiệu suất và khả năng sử dụng. Bản phát hành này tương thích với Dynamics 365 9.x. Để cập nhật lên bản phát hành này, hãy truy cập vào Trung tâm quản trị cho Dynamics 365 trực tuyến và truy cập vào trang giải pháp để cài đặt bản cập nhật. Để biết thêm thông tin, hãy xem [Cài đặt, cập nhật hoặc xóa giải pháp ưu tiên](/power-platform/admin/install-remove-preferred-solution).

Chủ đề này liệt kê các tính năng và bản sửa lỗi mới hoặc đã thay đổi cho PSA V3, Bản phát hành cập nhật 15. Phiên bản này có số bản dựng là V3.10.5.28 và thường có sẵn thông qua bản tự cập nhật vào tháng 1 năm 2020.

## <a name="update-release-15"></a>Phát hành bản cập nhật 15 

### <a name="enhancements"></a>Cải tiến

- Quản lý dự án

### <a name="bug-fixes"></a>Sửa lỗi

- Thời gian và Chi phí

  - Đã sửa lỗi: Thêm xử lý lỗi khi tải trong dạng xem điều hòa.
  - Đã sửa lỗi: Trung tâm nguồn lực dự án: Đổi tên **Số tiền** để giảm sự mơ hồ.
  - Đã sửa lỗi: Điều chỉnh dạng xem **Sao chép cột mục nhập thời gian** để bao gồm loại.
  - Đã sửa lỗi: Việc chỉnh sửa thời lượng nhập thời gian trong chế độ xem lưới bằng số thập phân dẫn đến lỗi không xác định đối với một số số.

- Quản lý dự án

  - Đã sửa lỗi: Menu thả xuống cho **Dùng trong Dạng xem theo dõi** hiện mở rộng dựa vào chiều rộng của các tùy chọn.
  - Đã sửa lỗi: Khi quản lý dự án theo múi giờ +13, tính toán nhiệm vụ có thể hiển thị kết quả không chính xác.
  - Đã sửa lỗi: **Thời gian kết thúc thành viên nhóm** đã được sửa khi dùng lịch 24 giờ.
  - Đã sửa lỗi: Đã kích hoạt lại **BPF** trong biểu mẫu chính **msdyn_project**.
  - Đã sửa lỗi: Tính toán phân bổ không còn bỏ qua một ngày.
  - Đã sửa lỗi: Biểu ngữ thông báo mới đã được thêm vào biểu mẫu dự án khi múi giờ khác nhau giữa người dùng và dự án.

- Sales

  - Đã sửa lỗi: Có thể dùng tra cứu danh mục ước tính chi phí để lọc trùng lặp.
  - Đã sửa lỗi: Mã trong **PluginDomain.ExecuteInTryCatchBlock(..)** không còn ẩn nguồn gốc của ngoại lệ.
  - Đã sửa lỗi: Không còn nhận thông báo lỗi trong **Tra cứu dự án** trong biểu mẫu **Mô tả báo giá** khi có hơn 1000 dự án.
  - Đã sửa lỗi: Lưới **ước tính** cho ước tính lao động và ước tính chi phí hiện hiển thị ký hiệu tiền tệ chính xác.
  - Đã sửa lỗi: Sau khi tổ chức cập nhật PSA từ Bản phát hành cập nhật 14 thành Bản phát hành cập nhật 15, tab **Lịch trình** không còn xuất hiện dưới dạng trống trên biểu mẫu **Dự án**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
