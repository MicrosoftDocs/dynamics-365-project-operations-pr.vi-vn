---
title: Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 14, V3
description: Chủ đề này cung cấp thông tin về tính năng mới trong Phát hành bản cập nhật Project Service Automation 14 V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
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
ms.openlocfilehash: 00ce5c68b1141c88671f0534f7500bf0d7eebd8e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087066"
---
# <a name="project-service-automation-update-release-14-v3"></a>Phát hành bản cập nhật Project Service Automation 14, V3
Chúng tôi vui mừng thông báo bản cập nhật mới nhất cho ứng dụng Dynamics 365 Project Service Automation (PSA). Bản phát hành này bao gồm một số cải tiến quan trọng về chất lượng, hiệu suất và khả năng sử dụng. Bản phát hành này tương thích với Dynamics 365 9.x. Để cập nhật lên bản phát hành này, hãy truy cập vào Trung tâm quản trị cho Dynamics 365 trực tuyến và truy cập vào trang giải pháp để cài đặt bản cập nhật. Để biết thêm thông tin, hãy xem [Cài đặt, cập nhật hoặc xóa giải pháp ưu tiên](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Chủ đề này liệt kê các tính năng và bản sửa lỗi mới hoặc đã thay đổi cho PSA V3, Bản phát hành cập nhật 14. Phiên bản này có số bản dựng là V3.10.4.21 và có sẵn theo lịch trình sau:

- **Tính sẵn có chung (tự cập nhật):** Tháng 1 năm 2020
- **Cập nhật tự động:** Tháng 2 năm 2020

## <a name="update-release-14"></a>Phát hành bản cập nhật 14

### <a name="enhancements"></a>Cải tiến

- Sales

     - Các giá trị của trường tùy chỉnh từ **Chi tiết mô tả báo giá** được sao chép sang **Chi tiết mô tả hợp đồng dự án** khi báo giá được cập nhật thành **Đóng dưới dạng thắng**.
     - Có thể **Đóng dưới dạng thua** các dự án đã xác nhận.

- Quản lý nguồn lực

     - Khi gia hạn đặt trước, người dùng sẽ được nhắc với hộp thoại xác nhận để tóm tắt kết quả đặt trước và cung cấp liên kết để Duy trì đặt trước.


### <a name="bug-fixes"></a>Sửa lỗi

- Thời gian và Chi phí

     - Đã sửa lỗi: Cải thiện trải nghiệm người dùng khi người dùng chưa chọn bất kỳ mục nhập nào cần sửa.

- Quản lý nguồn lực

     - Đã sửa lỗi: Đặt trước một nguồn lực nhiều lần vượt quá tên của nguồn lực có thể đặt được.

- Sales

     - Đã sửa lỗi: Tổng giá bán không được tính cho đến khi người dùng cũng nhập giá vốn cho ước tính chi phí cho một dự án.
     - Đã sửa lỗi: Việc đóng một báo giá là **Thắng** không thành công nếu hợp đồng dự án được liên kết không ở trạng thái **Bản nháp**.
