---
title: Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 38, V3
description: Bài viết này liệt kê các tính năng và bản sửa lỗi có sẵn trong Microsoft Dynamics 365 Project Service Automation Bản phát hành cập nhật 38, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 12/06/2021
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
ms.openlocfilehash: ccc08cd0bc365bd4761424a4c0ceac91985e7c89
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915211"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-38-v3"></a>Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 38, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Chúng tôi vui mừng được công bố bản cập nhật mới nhất cho ứng dụng Microsoft Dynamics 365 Project Service Automation. Bản phát hành này bao gồm một số cải tiến quan trọng về chất lượng, hiệu suất và khả năng sử dụng. Bản này tương thích với Dynamics 365 9.x. Để cập nhật lên bản phát hành này, hãy truy cập trang giải pháp trực tuyến Trung tâm quản trị cho Dynamics 365 và cài đặt bản cập nhật. Để biết thêm thông tin, hãy xem [Cài đặt, cập nhật hoặc xóa giải pháp ưu tiên](/power-platform/admin/install-remove-preferred-solution).

Bài viết này liệt kê các tính năng và bản sửa lỗi mới hoặc đã thay đổi cho Project Service Automation, Bản phát hành cập nhật 38, V3. Phiên bản này có số bản dựng là V3.10.59.117 và thường có sẵn thông qua bản tự cập nhật vào tháng 12 năm 2021.

## <a name="update-release-38"></a>Phát hành bản cập nhật 38

### <a name="bug-fixes"></a>Sửa lỗi

Các vấn đề sau đã được khắc phục.

**Thời gian và Chi phí**

- Một ngoại lệ xảy ra khi độ dài của nhật ký bộ phê duyệt vượt quá 100.000 bản ghi.
- Người dùng không thể truy cập vào lưới **Mục nhập thời gian** từ trang chính **Mục nhập thời gian**.
- Hộp thoại **Nhập mục nhập thời gian** không hiển thị bất kỳ văn bản nào khi không có mục nào đủ điều kiện để nhập.
- Người dùng có thể tạo bộ phê duyệt trong đó trường **Trạng thái mục tiêu** được đặt thành **Không xác định**.

**Quản lý dự án**

- Các đường viền không được hiển thị chính xác trong phân công nguồn lực cho UTC (+09:30) và UTC (+10:00) khi giờ mùa hè bắt đầu.
- Trường **Cột bổ sung** cho cấu trúc phân tích công việc bị ẩn trong một số ngôn ngữ.
- Bộ chọn ngày để kiểm soát lịch trong lưới **Nhiệm vụ dự án** không được bản địa hóa chính xác cho tiếng Trung Quốc.

**Bán hàng**

- Các giá trị **Hiệu suất hợp đồng** và **Chi phí thực tế của dự án** không khớp khi các nguồn lực có thể đặt có mục nhập thời gian gửi đơn vị hợp đồng và đơn vị tiền tệ khác nhau.
- Quy trình làm việc tùy chỉnh để tự động xác nhận hóa đơn không thành công khi hóa đơn được nhập dưới dạng giải pháp được quản lý. Thông báo sau được hiển thị: "Thông báo Microsoft.Xrm.Sdk.InvalidPluginExecutionException: Trạng thái hóa đơn không hợp lệ."
- Khi **Gốc** được chọn làm tùy chọn tóm tắt và dự án có các ước tính từ kết hợp các lớp giao dịch (ví dụ: kết hợp ước tính thời gian, chi phí và vật liệu), hệ thống tóm tắt giữa các lớp giao dịch dưới dạng một mô tả phí duy nhất.
- Trong các tình huống mà mô tả chi phí được thêm vào trước khi mô tả hợp đồng được liên kết với một dự án, giá chính xác sẽ không được nhập làm giá trị mặc định trong trường **Cập nhật giá**.
- Số tiền doanh số âm không được cho phép trên các thực thể **Dự án** và **Nhiệm vụ**.
