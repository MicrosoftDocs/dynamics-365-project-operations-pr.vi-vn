---
title: Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 17, V3
description: Chủ đề này liệt kê các tính năng và bản sửa lỗi có trong Bản phát hành cập nhật Project Service Automation 17, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: 7ba685568692dafe117de42a71bb14d391cd7cc4
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087064"
---
# <a name="project-service-automation-update-release-17-v3"></a>Phát hành bản cập nhật Project Service Automation 17, V3

Chúng tôi vui mừng thông báo bản cập nhật mới nhất dành cho ứng dụng Project Service Automation của Dynamics 365. Bản phát hành này bao gồm một số cải tiến quan trọng về chất lượng, hiệu suất và khả năng sử dụng.  Bản phát hành này tương thích với Dynamics 365 9.x. Để cập nhật lên bản phát hành này, hãy truy cập vào Trung tâm quản trị cho Dynamics 365 trực tuyến, rồi chuyển đến trang giải pháp để cài đặt bản cập nhật. Để biết thêm thông tin, hãy xem [Cài đặt, cập nhật hoặc xóa giải pháp ưu tiên](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Chủ đề này liệt kê các tính năng và bản sửa lỗi mới hoặc đã thay đổi cho PSA V3, Bản phát hành cập nhật 17. Phiên bản này có số bản dựng là V3.10.6.34 và thường có sẵn thông qua bản tự cập nhật vào tháng 3 năm 2020.


## <a name="update-release-17"></a>Phát hành bản cập nhật 17

### <a name="bug-fixes"></a>Sửa lỗi

**Sự cố chung**

- Sửa lỗi: Cập nhật Project Service Automation để thực thi giấy phép Thành viên Nhóm (Trung tâm Nguồn lực Dự án sẽ bao gồm siêu dữ liệu của gói Dịch vụ Thành viên Nhóm 3.x)
 
**Thời gian và Chi phí**

- Sửa lỗi: Không thể thay đổi ước tính chi phí từ giá khác không thành không (0). Thay đổi sẽ bị bỏ qua.

**Quản lý dự án**

- Sửa lỗi: Thêm bước kiểm tra giá trị rỗng cho tên vị trí của thành viên nhóm.
- Sửa lỗi: trường **msdyn_userresourceid** trên thực thể **msdyn_resourceassignment** không dùng được nữa.
- Sửa lỗi: Bản nâng cấp từ 2.x lên 3.x giờ sẽ xử lý các đường cong nỗ lực trống về phân công nhiệm vụ.

**Sales**

- Sửa lỗi: **Invoice.PreValidateInvoiceUpdate** giờ sẽ xử lý kịch bản về quá trình gán lại chủ sở hữu đúng cách.
- Sửa lỗi: Khi lớp giao dịch là **Thời gian** , thì không chỉnh sửa được **UnitGroup** đối với tất cả thực thể, bao gồm **QuoteLineDetails** , **JournalLine** , **InvoiceLineDetail** và **ContractLineDetails**. Tuy nhiên, chỉ không chỉnh sửa được **Đơn vị** đối với **JournalLine** và **InvoiceLineDetails**.


