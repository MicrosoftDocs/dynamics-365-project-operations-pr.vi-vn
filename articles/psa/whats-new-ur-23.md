---
title: Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 23, V3
description: Chủ đề này liệt kê các tính năng và bản sửa lỗi có trong Bản phát hành cập nhật Project Service Automation 23, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: cc918f1516d4751b3f8e70a93d8fc66058201f22
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581632"
---
# <a name="project-service-automation-update-release-23-v3"></a>Phát hành bản cập nhật Project Service Automation 23, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Chúng tôi vui mừng thông báo bản cập nhật mới nhất dành cho ứng dụng Project Service Automation của Dynamics 365. Bản phát hành này bao gồm một số cải tiến quan trọng về chất lượng, hiệu suất và khả năng sử dụng. Bản phát hành này tương thích với Dynamics 365 9.x. Để cập nhật lên bản phát hành này, hãy truy cập vào Trung tâm quản trị cho trang giải pháp trực tuyến Dynamics 365 để cài đặt bản cập nhật. Để biết thêm thông tin, hãy xem [Cài đặt, cập nhật hoặc xóa giải pháp ưu tiên](/power-platform/admin/install-remove-preferred-solution).

Chủ đề này liệt kê các tính năng và bản sửa lỗi mới hoặc đã thay đổi cho Project Service Automation V3, Bản phát hành cập nhật 23. Phiên bản này có số bản dựng là V 3.10.34.30 và thường có sẵn thông qua bản tự cập nhật vào tháng 8 năm 2020.

## <a name="update-release-23"></a>Phát hành bản cập nhật 23

### <a name="bug-fixes"></a>Sửa lỗi

**Thời gian và Chi phí**

Các vấn đề sau đã được khắc phục:
- Xử lý trường hợp cạnh trong **Xóa thành viên nhóm dự án** để cung cấp một ngoại lệ có ý nghĩa.
- Kết quả nhập mục phân công trong một màn hình xóa trống.

**Quản lý nguồn lực**

Các vấn đề sau đã được khắc phục:

- **Thẻ tài nguyên lưới thời gian làm việc của nguồn lực** cho thấy dữ liệu không chính xác khi thang thời gian lớn hơn năm ngày.
- Khi khách hàng tạo nguồn lực có thể đặt trước, phần bổ trợ liên tục không thể tự động thêm nguồn lực vào nhóm Microsoft Office 365.
- Dạng xem **điều hòa** hiển thị các đường viền thủ công không chính xác trong dạng xem **Tuần** hoặc **Tháng**.

**Quản lý dự án**

Các vấn đề sau đã được khắc phục:

- Một số lượng thực thể **RetrieveMultiple cho usersettings** quá lớn đang làm giảm hiệu suất cho các mục phê duyệt dự án và các thao tác khác.
- Tính năng tra cứu nguồn lực trong lưới **Lập kế hoạch nhiệm vụ** giới hạn để chỉ hiển thị năm thành viên nhóm từ nhóm dự án. 
- Tính năng tra cứu nguồn lực trong lưới **Lập kế hoạch nhiệm vụ** không lọc nguồn lực không hoạt động.
- Chế độ thủ công không hoạt động như mong đợi trong cấu trúc phân tích công việc lập kế hoạch dự án.
- Lưới **Lập kế hoạch nhiệm vụ** hiển thị **Hạng mục giao dịch không hoạt động**.
- Lưới **Phân công nguồn lực** làm tròn không chính xác khi một nhiệm vụ có nhiều nhiệm vụ.
- Các giá trị làm tròn khác nhau giữa chi phí theo kế hoạch và chi phí thực tế cho một nhiệm vụ.

**Sales**

Các vấn đề sau đã được khắc phục:

- **Tìm nạp tất cả các hạng mục giao dịch** nhấp đúp để tạo nhiều dòng.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
