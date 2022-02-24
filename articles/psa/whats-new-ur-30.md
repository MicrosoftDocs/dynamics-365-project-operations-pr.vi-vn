---
title: Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 30, V3
description: Chủ đề này liệt kê các tính năng và bản sửa lỗi có trong Bản phát hành cập nhật Project Service Automation 30, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 1169ee13c42e982cb30a40d92df660f8933786a9
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852907"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a>Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 30, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Chúng tôi vui mừng thông báo bản cập nhật mới nhất dành cho ứng dụng Project Service Automation của Dynamics 365. Bản phát hành này bao gồm một số cải tiến quan trọng về chất lượng, hiệu suất và khả năng sử dụng. Bản phát hành này tương thích với Dynamics 365 9.x. Để cập nhật lên bản phát hành này, hãy truy cập vào Trung tâm quản trị cho trang giải pháp trực tuyến Dynamics 365 để cài đặt bản cập nhật. Để biết thêm thông tin, hãy xem [Cài đặt, cập nhật hoặc xóa giải pháp ưu tiên](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Chủ đề này liệt kê các tính năng và bản sửa lỗi mới hoặc đã thay đổi cho Project Service Automation V3, Bản phát hành cập nhật 30. Phiên bản này có số bản dựng là V3.10.51.61 và thường có sẵn thông qua bản tự cập nhật vào tháng 4 năm 2021.

## <a name="update-release-30"></a>Phát hành bản cập nhật 30

### <a name="bug-fixes"></a>Sửa lỗi

**Thời gian và Chi phí**

Các vấn đề sau đã được khắc phục:

- Đã xảy ra lỗi khi bạn tạo và lưu mục nhập thời gian trên trang **Tạo nhanh** nếu trường **Vai trò** bị xóa.
- Bộ lọc Mục nhập thời gian áp dụng sai toán tử bộ lọc.
- Bảng chấm công đã sao chép không tự động hiển thị khi bạn chọn **Sao chép tuần** khi kiểm soát mục nhập thời gian.

**Quản lý nguồn lực**

Các vấn đề sau đã được khắc phục:

- Khi bạn gia hạn đặt chỗ, trạng thái đặt chỗ được chỉ định cho loại hình đặt chỗ cứng là không chính xác. Việc gia hạn đặt chỗ dựa trên trạng thái đặt chỗ được xác định là **Đã cam kết** trong siêu dữ liệu thiết lập đặt chỗ.
- Khi bạn không chỉ định trạng thái đặt chỗ hợp lệ, thông báo lỗi sẽ không được bản địa hóa một cách chính xác.

**Quản lý dự án**

Các vấn đề sau đã được khắc phục:

- Không thể tạo dự án bằng một đơn vị tiền tệ và bao gồm các nhiệm vụ có liên quan bằng một đơn vị tiền tệ khác.

**Bán hàng**

Các vấn đề sau đã được khắc phục:

- Khi bảng giá được sao chép, giá sẽ không được cập nhật.
- Việc chốt báo giá là thắng sẽ không thành công khi chi tiết chi phí có giá trị gốc.
- Trên thực thể **Nhiệm vụ dự án**, **Chi phí ước tính** đã được đổi tên thành **Chi phí dự kiến (Cơ sở)**.
- Một ngoại lệ tham chiếu rỗng được tạo ra khi các hóa đơn được tạo hoặc xóa.
