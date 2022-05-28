---
title: Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 22, V3
description: Chủ đề này liệt kê các tính năng và bản sửa lỗi có trong Bản phát hành cập nhật Project Service Automation 22, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: 2718509a21c76c12427ec1d78e287df2274f4d72
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588808"
---
# <a name="project-service-automation-update-release-22-v3"></a>Phát hành bản cập nhật Project Service Automation 22, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Chúng tôi vui mừng thông báo bản cập nhật mới nhất dành cho ứng dụng Project Service Automation của Dynamics 365. Bản phát hành này bao gồm một số cải tiến quan trọng về chất lượng, hiệu suất và khả năng sử dụng. Bản phát hành này tương thích với Dynamics 365 9.x. Để cập nhật lên bản phát hành này, hãy truy cập vào Trung tâm quản trị cho trang giải pháp trực tuyến Dynamics 365 để cài đặt bản cập nhật. Để biết thêm thông tin, hãy xem [Cài đặt, cập nhật hoặc xóa giải pháp ưu tiên](/power-platform/admin/install-remove-preferred-solution).

Chủ đề này liệt kê các tính năng và bản sửa lỗi mới hoặc đã thay đổi cho Project Service Automation V3, Bản phát hành cập nhật 22. Phiên bản này có số bản dựng là V 3.10.33.48 và thường được cung cấp thông qua bản tự cập nhật vào tháng 6 năm 2020.

## <a name="update-release-22"></a>Phát hành bản cập nhật 22

### <a name="bug-fixes"></a>Sửa lỗi



**Thời gian và Chi phí**

Các vấn đề sau đã được khắc phục:

- **Mục nhập thời gian** không được tự động thêm vào Lịch trình thời gian sau khi nhập.
- Bộ chọn ngày dạng lưới **Mục nhập thời gian** không nhận dạng tùy chọn cài đặt theo khu vực của người dùng.

**Quản lý nguồn lực**

Các vấn đề sau đã được khắc phục:

- Ở chế độ thủ công, những thay đổi đối với sự phân phối giờ làm việc **Gán Nguồn lực** không được nhận dạng khi tạo **Yêu cầu về Nguồn lực**.
- **Yêu cầu về Nguồn lực** không hỗ trợ các trạng thái yêu cầu tùy chỉnh.

**Quản lý dự án**

Các vấn đề sau đã được khắc phục:

- Việc nhấp đúp vào EstimateGridControl sẽ không phân tích cú pháp chính xác các định dạng số của Hà Lan.
- Các giờ đã gán không cập nhật chính xác khi nhiệm vụ được thay đổi bằng phần bổ trợ của máy khách Microsoft Project.
- Lưới Theo dõi Dự án và Ước tính hiển thị không chính xác mã đơn vị tiền tệ bán hàng khi đơn vị tiền tệ trong hợp đồng khác với đơn vị tiền tệ của khách hàng và tổ chức được định cấu hình để hiển thị mã đơn vị tiền tệ thay vì ký hiệu tiền tệ.
- Ngày kết thúc của thành viên Nhóm sẽ được bổ sung thêm 1 ngày nếu lịch làm việc là 24 giờ mỗi ngày.
- Trên Lịch trình Dự án, việc thêm Danh mục Giao dịch vào nhiệm vụ không kích hoạt tính năng lưu tự động.
- Lỗi sau sẽ xuất hiện khi thêm một thành viên nhóm vào Mẫu Dự án: "Không thể liên kết các yêu cầu về nguồn lực với mẫu dự án". 
- Tập lệnh quy tắc ruy băng "msdyn.Approval.CanApproveOrReject" hiển thị lỗi hết thời gian chờ.

**Sales**

Các vấn đề sau đã được khắc phục:

- Thông báo lỗi xác thực không hiển thị khi một Hạng mục trong Bảng Giá được chọn khi tra cứu Bảng Giá trên biểu mẫu/thực thể "Bảng Giá Dự án Báo giá Mới".
- Việc đóng báo giá ở trạng thái thành công sẽ không chuyển đến hợp đồng đã tạo nếu BPF đính kèm với báo giá đang ở giai đoạn cuối cùng.
- **Bán hàng Chưa lập hóa đơn** đảo ngược được liên kết với chi phí ban đầu khi mục nhập thời gian được thu hồi.
- Sau khi chọn nút **Xác nhận**, trạng thái hóa đơn chỉ thay đổi thành **Đã xác nhận** khi hóa đơn được làm mới.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
