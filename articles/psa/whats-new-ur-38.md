---
title: Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 38, V3
description: Chủ đề này liệt kê các tính năng và bản sửa lỗi có sẵn trong Microsoft Dynamics 365 Project Service Automation Bản phát hành cập nhật 38, V3.
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
ms.openlocfilehash: 16994535d57dc1d7fefbe6e892c154f52638c7c0
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598744"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-38-v3"></a>Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 38, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Chúng tôi vui mừng được công bố bản cập nhật mới nhất cho ứng dụng Microsoft Dynamics 365 Project Service Automation. Bản phát hành này bao gồm một số cải tiến quan trọng về chất lượng, hiệu suất và khả năng sử dụng. Bản này tương thích với Dynamics 365 9.x. Để cập nhật lên bản phát hành này, hãy truy cập trang giải pháp trực tuyến Trung tâm quản trị cho Dynamics 365 và cài đặt bản cập nhật. Để biết thêm thông tin, hãy xem [Cài đặt, cập nhật hoặc xóa giải pháp ưu tiên](/power-platform/admin/install-remove-preferred-solution).

Chủ đề này liệt kê các tính năng và bản sửa lỗi mới hoặc đã thay đổi cho Project Service Automation, Bản phát hành cập nhật 38, V3. Phiên bản này có số bản dựng là V3.10.59.117 và thường có sẵn thông qua bản tự cập nhật vào tháng 12 năm 2021.

## <a name="update-release-38"></a>Phát hành bản cập nhật 38

### <a name="bug-fixes"></a>Sửa lỗi

Các vấn đề sau đã được khắc phục.

**Thời gian và Chi phí**

- Một ngoại lệ xảy ra khi độ dài của nhật ký tập hợp phê duyệt vượt quá 100.000 bản ghi.
- Người dùng không thể truy cập vào **Thời gian nhập cảnh** lưới từ The **Thời gian nhập cảnh** Trang chính.
- Các **Nhập thời gian** hộp thoại không hiển thị bất kỳ văn bản nào khi không có mục nào đủ điều kiện để nhập.
- Người dùng có thể tạo tập hợp phê duyệt trong đó **Trạng thái mục tiêu** trường được đặt thành **không xác định**.

**Quản lý dự án**

- Các đường bao không được hiển thị chính xác trong chỉ định tài nguyên cho UTC (+09: 30) và UTC (+10: 00) khi thời gian tiết kiệm ánh sáng ban ngày bắt đầu.
- Các **Cột bổ sung** trường cho cấu trúc phân tích công việc bị ẩn trong một số ngôn ngữ.
- Bộ chọn ngày để kiểm soát lịch trong **Nhiệm vụ dự án** lưới không được bản địa hóa chính xác cho tiếng Trung Quốc.

**Bán hàng**

- **Thực hiện hợp đồng** và **Chi phí thực tế của dự án** giá trị không khớp khi các tài nguyên có thể đặt trước có các đơn vị hợp đồng và đơn vị tiền tệ khác nhau gửi các mục thời gian.
- Quy trình làm việc tùy chỉnh để tự động xác nhận hóa đơn không thành công khi hóa đơn được nhập dưới dạng giải pháp được quản lý. Thông báo sau được hiển thị: "Microsoft.Xrm.Sdk.InvalidPluginExecutionException Thông báo: Trạng thái hóa đơn không hợp lệ."
- Khi nào **Nguồn gốc** được chọn làm tùy chọn tóm tắt và dự án có các ước tính từ hỗn hợp các lớp giao dịch (ví dụ: kết hợp ước tính thời gian, chi phí và vật liệu), hệ thống sẽ tóm tắt giữa các lớp giao dịch dưới dạng một dòng phí duy nhất.
- Trong các tình huống mà dòng chi phí được thêm vào trước khi dòng hợp đồng được liên kết với một dự án, giá chính xác không được nhập làm giá trị mặc định trong **Cập nhật giá** đồng ruộng.
- Số tiền bán hàng âm không được phép vào **Dự định** và **Nhiệm vụ** các thực thể.
