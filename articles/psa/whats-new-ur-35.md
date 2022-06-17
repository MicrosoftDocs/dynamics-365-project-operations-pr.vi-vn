---
title: Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 35, V3
description: Bài viết này liệt kê các tính năng và bản sửa lỗi có sẵn trong Microsoft Dynamics 365 Project Service Automation Cập nhật Bản phát hành 35, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 09/03/2021
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
ms.openlocfilehash: 28b4a5ccbfff83c9b1a18cb0b4062af9cdaf8f6e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912864"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-35-v3"></a>Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 35, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Chúng tôi vui mừng được công bố bản cập nhật mới nhất cho ứng dụng Microsoft Dynamics 365 Project Service Automation. Bản phát hành này bao gồm một số cải tiến quan trọng về chất lượng, hiệu suất và khả năng sử dụng. Bản này tương thích với Dynamics 365 9.x. Để cập nhật lên bản phát hành này, hãy truy cập trang giải pháp trực tuyến Trung tâm quản trị cho Dynamics 365 và cài đặt bản cập nhật. Để biết thêm thông tin, hãy xem [Cài đặt, cập nhật hoặc xóa giải pháp ưu tiên](/power-platform/admin/install-remove-preferred-solution).

Bài viết này liệt kê các tính năng và bản sửa lỗi mới hoặc được thay đổi cho Bản phát hành bản cập nhật tự động hóa dịch vụ dự án 35, V3. Phiên bản này có số bản dựng là V3.10.56.110 và thường có sẵn thông qua bản tự cập nhật vào tháng 9 năm 2021.

## <a name="update-release-35"></a>Bản phát hành cập nhật 35

### <a name="bug-fixes"></a>Sửa lỗi

Các vấn đề sau đã được khắc phục.

**Thời gian và Chi phí**

- Người phê duyệt dự án nhận được lỗi đặc quyền đọc khi họ phê duyệt các mục chi phí với vai trò **Người phê duyệt dự án**.
- Người phê duyệt dự án nhận được lỗi ghi đặc quyền trên **msdyn_projectapproval** khi họ hủy một mục thời gian đã được phê duyệt với vai trò **Người phê duyệt dự án**.
- Khi bạn chọn **Sao chép tuần** trong mục nhập thời gian trong mô-đun ứng dụng Dynamics 365 dành cho điện thoại - Trung tâm nguồn lực dự án, lỗi sau xảy ra: "... \ OfficePcriptivity_RibbonRules.js.map: Lỗi HTTP: mã trạng thái 404, net:: ERR_HTTP_RESPONSE_CODE_FAILURE. "
- Chính sách **Thử lại** tự động phê duyệt các mục nhập đã bị từ chối trước đó.
- Lưới phụ **Bộ phê duyệt** hiển thị các hành động với ruy băng không thể áp dụng.
- Các biểu tượng bị thiếu cho **Nhiệm vụ dự án** và **Vai trò nguồn lực** trên thực thể **Thời gian nhập**.
- Khi bạn nhập các nhiệm vụ nguồn lực, các mục thời gian đã nhập không có thời lượng chính xác cho các nhiệm vụ được tạo thông qua các tác vụ ở chế độ thủ công.
- **Xóa** bị thiếu trên trang **Tìm kiếm Nâng cao cho bản ghi Mục nhập thời gian**.
- **Lưu** bị thiếu trên trang **Thông tin nhập thời gian**. Sự cố này ngăn các thay đổi được lưu khi đóng trang.

**Lập kế hoạch dự án**

- Các lưới **Phân công nguồn lực** và **Đối chiếu nguồn lực** không sắp xếp các thuộc tính được nhóm theo bảng chữ cái.
- Không thể tạo tác vụ nếu hành vi ngày được tùy chỉnh thành **Chỉ ngày**.

**Quản lý nguồn lực**

- Nếu cả Dynamics 365 Field Service và Project Service Automation được cài đặt, các vấn đề về lớp phủ xảy ra khi **Dạng xem Liên kết Yêu cầu Nguồn lực** được liên kết với một trang chính.
- Bấm đúp vào **Lưu** trong hộp thoại **Tạo nhanh Thành viên nhóm** ngăn yêu cầu nguồn lực được tạo.

**Bán hàng**

- Một ngoại lệ được đưa ra nếu bạn xóa một công việc được liên kết với một dấu ngoặc kép có trạng thái **Giành được**.
