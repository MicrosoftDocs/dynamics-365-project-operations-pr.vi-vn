---
title: Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 34, V3
description: Bài viết này liệt kê các tính năng và bản sửa lỗi có sẵn trong Bản phát hành bản cập nhật tự động hóa dịch vụ dự án 34, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/05/2021
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
ms.openlocfilehash: e47a5442f285952c165a2d30e337a362a6b065dd
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928688"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-34-v3"></a>Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 34, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Chúng tôi vui mừng được công bố bản cập nhật mới nhất cho ứng dụng Microsoft Dynamics 365 Project Service Automation. Bản phát hành này bao gồm một số cải tiến quan trọng về chất lượng, hiệu suất và khả năng sử dụng. Bản này tương thích với Dynamics 365 9.x. Để cập nhật lên bản phát hành này, hãy truy cập trang giải pháp trực tuyến Trung tâm quản trị cho Dynamics 365 và cài đặt bản cập nhật. Để biết thêm thông tin, hãy xem [Cài đặt, cập nhật hoặc xóa giải pháp ưu tiên](/power-platform/admin/install-remove-preferred-solution).

Bài viết này liệt kê các tính năng và bản sửa lỗi mới hoặc được thay đổi cho Tự động hóa dịch vụ dự án V3, Bản phát hành cập nhật 34. Phiên bản này có số bản dựng là V3.10.55.38 và thường có sẵn thông qua bản tự cập nhật vào tháng 7 năm 2021.

## <a name="update-release-34"></a>Phát hành bản cập nhật 34

### <a name="bug-fixes"></a>Sửa lỗi
Các vấn đề sau đã được khắc phục.

**Chung**

- Các bản cập nhật theo nhà xuất bản không kích hoạt quy trình phê duyệt hiện đại mới.
- Thuộc tính **Trạng thái mục tiêu** và **Loại hành động** bị thiếu trên trang chính **Bộ phê duyệt**.

**Thời gian và Chi phí**

- Không thể phê duyệt yêu cầu thu hồi bằng quy trình phê duyệt hiện đại.
- Việc sao chép các mục nhập thời gian trong một tuần không hoạt động khi sao chép các mục nhập không liên quan đến người dùng đã đăng nhập.

**Lập kế hoạch dự án**

- Đường viền gán nguồn lực bị hỏng khi nhập từ phần bổ trợ Microsoft Project dành cho máy tính để bàn.

**Quản lý nguồn lực**

- Khi bạn xuất bản một dự án từ phần bổ trợ máy khách Microsoft Project dành cho máy tính để bàn, ngày kết thúc của các yêu cầu hiện có sẽ thay đổi.
- Độ chính xác thập phân vượt quá hai chữ số thập phân trong hộp thoại xác nhận đặt trước mở rộng.

**Bán hàng**

- Khi bạn thêm một dòng dựa trên sản phẩm với một sản phẩm hiện có vào hợp đồng dự án, thông báo ngoại lệ **không tìm thấy khóa trong từ điển** sẽ hiển thị.
- Khách hàng tiềm năng không thể đủ điều kiện khi một loại đơn hàng được ánh xạ từ khách hàng tiềm năng thành cơ hội.
