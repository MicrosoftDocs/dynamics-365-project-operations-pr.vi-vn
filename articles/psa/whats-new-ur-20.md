---
title: Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 20, V3
description: Chủ đề này liệt kê các tính năng và bản sửa lỗi có trong Bản phát hành cập nhật Project Service Automation 20, V3
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: db416343ac9ac2591007e83be80493a48f9ae904
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280694"
---
# <a name="project-service-automation-update-release-20-v3"></a>Phát hành bản cập nhật Project Service Automation 20, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Chúng tôi vui mừng thông báo bản cập nhật mới nhất dành cho ứng dụng Project Service Automation của Dynamics 365. Bản phát hành này bao gồm một số cải tiến quan trọng về chất lượng, hiệu suất và khả năng sử dụng. Bản phát hành này tương thích với Dynamics 365 9.x. Để cập nhật lên bản phát hành này, hãy truy cập vào Trung tâm quản trị cho trang giải pháp trực tuyến Dynamics 365 để cài đặt bản cập nhật. Để biết thêm thông tin, hãy xem [Cài đặt, cập nhật hoặc xóa giải pháp ưu tiên](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Chủ đề này liệt kê các tính năng và bản sửa lỗi mới hoặc đã thay đổi cho Project Service Automation V3, Bản phát hành cập nhật 20. Phiên bản này có số bản dựng là V 3.10.31.37 và thường được cung cấp thông qua bản tự cập nhật vào tháng 6 năm 2020.

## <a name="update-release-20"></a>Phát hành bản cập nhật 20

### <a name="bug-fixes"></a>Sửa lỗi

**Quản lý dự án**

Các vấn đề sau đã được khắc phục:

- Việc nhập thành viên nhóm dự án với phương pháp phân bổ yêu cầu số giờ dẫn đến thông báo lỗi không rõ ràng khi số giờ được chỉ định bằng không.
- Người dùng nhận được lỗi không chính xác khi số lượng ký tự tối đa đã được nhập vào trường **Mô tả** cho một nhiệm vụ dự án.
- Trang **tải xuống phần bổ trợ Microsoft Dynamics 365 Project Service Automation** chuyển hướng đến trang tải xuống bằng tiếng Anh khi thiết đặt ngôn ngữ của người dùng là Nhật Bản.
- Khi xảy ra lỗi máy chủ, nhãn đồng bộ hóa trên tab **Lịch trình** của biểu mẫu **Dự án** đôi khi vẫn còn.
- Các bản cập nhật nhiệm vụ dự phòng đang được gửi đến máy chủ khi một nhiệm vụ được sửa đổi.

**Sales**

Các vấn đề sau đã được khắc phục:

- Trên biểu mẫu **Hợp đồng**, nhấp đúp vào **Tạo hóa đơn** tạo ra hai hóa đơn cho một bản ghi thực tế duy nhất.
- Trong Internet Explorer 11, người dùng không thể tạo các mục nhập chi phí.
- Đảo ngược Chi phí và đảo ngược Dữ liệu thực tế về doanh thu bán hàng chưa lập hóa đơn không được liên kết.
- Nút **Làm mới số liệu thực tế** trên biểu mẫu **Dự án** không làm mới **Số giờ thực tế cho nhiệm vụ**.
- Phần bổ trợ **PreValidateProjectTeamMemberCreate** có thể tạo các nguồn lực có thể đặt trước chung khi thuộc tính **msdyn_isgenericresourceprojectscoped** được đặt thành **Sai**.
- **Tính toán lại** xóa chi phí có thể tính phí của chi tiết mô tả báo giá dựa trên sản phẩm và chi tiết mô tả hợp đồng.
- Trong các kịch bản cụ thể, phần bổ trợ **PostEstimateLineUpdate** hiển thị lỗi ngoại lệ tham chiếu null.
- Khoảng thời gian giai đoạn thời gian trên **Biểu đồ phân tích lợi nhuận** không khớp với khoảng thời gian của chi phí trong chi tiết mô tả báo giá với chi phí cố định của báo giá.
- Giá trị đơn vị và nhóm đơn vị không mặc định chính xác cho các danh mục chi phí trên các biểu mẫu **Chi tiết mô tả hợp đồng** và **Chi tiết mô tả báo giá**.
- Danh sách **Giá vốn đơn vị tổ chức** cho phép chồng chéo trong hiệu lực ngày tháng.
- Người dùng không được phép thay đổi **Đơn vị tổ chức** khi loại đơn hàng không dựa trên công việc vì điều này sẽ dẫn đến lỗi ngoại lệ tham chiếu null.
- Khi cố gắng điều hướng từ biểu mẫu **Chi tiết mô tả báo giá**, quay lại tab **Báo giá**, biểu mẫu làm mới và hiển thị tab **Tóm tắt**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]