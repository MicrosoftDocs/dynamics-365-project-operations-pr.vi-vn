---
title: Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 36, V3
description: Chủ đề này liệt kê các tính năng và bản sửa lỗi có sẵn trong Microsoft Dynamics 365 Project Service Automation Bản phát hành cập nhật 36, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/06/2021
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
ms.openlocfilehash: 9b85aed79acb7e7784a23f54a2e9af1cc83f5f4d
ms.sourcegitcommit: 6d9fc4dc851814664bf71729904ab4bedd85fe70
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/06/2021
ms.locfileid: "7606839"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-36-v3"></a>Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 36, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Chúng tôi vui mừng được công bố bản cập nhật mới nhất cho ứng dụng Microsoft Dynamics 365 Project Service Automation. Bản phát hành này bao gồm một số cải tiến quan trọng về chất lượng, hiệu suất và khả năng sử dụng. Bản này tương thích với Dynamics 365 9.x. Để cập nhật lên bản phát hành này, hãy truy cập trang giải pháp trực tuyến Trung tâm quản trị cho Dynamics 365 và cài đặt bản cập nhật. Để biết thêm thông tin, hãy xem [Cài đặt, cập nhật hoặc xóa giải pháp ưu tiên](/power-platform/admin/install-remove-preferred-solution).

Chủ đề này liệt kê các tính năng và bản sửa lỗi mới hoặc đã thay đổi cho Project Service Automation, Bản phát hành cập nhật 36, V3. Phiên bản này có số bản dựng là V3.10.57.152 và thường có sẵn thông qua bản tự cập nhật vào tháng 10 năm 2021.

## <a name="update-release-36"></a>Phát hành bản cập nhật 36

### <a name="bug-fixes"></a>Sửa lỗi

Các vấn đề sau đã được khắc phục.

**Chung**
- Tên trường **Mẫu giờ làm việc mặc định** được dịch không chính xác trên trang **Tham số dự án**.
- Các phần bổ trợ không đồng bộ không xử lý chính xác các trường hợp ngoại lệ liên quan đến **SharedVariableService**.

**Thời gian và Chi phí**
- Khi các mô tả nhật ký kế toán bị thiếu hoặc người dùng không có đặc quyền chính xác để đọc các mô tả nhật ký, lỗi không chính xác xảy ra khi phê duyệt dự án bị hủy bỏ.
- Người dùng không thể hủy phê duyệt khi một mục chi phí hoặc thời gian có nhiều hơn một phê duyệt dự án liên quan.
- **Vắng mặt** và **Kỳ nghỉ** được dịch không chính xác cho ngôn ngữ Trung Quốc trong một tra cứu trên trang tạo nhanh **Mục nhập thời gian**.

**Quản lý nguồn lực**
- Người dùng không thể tìm kiếm nguồn lực trong **Trợ lý lịch trình** khi chế độ xem được đặt thành **Ngày**, **Tuần** hoặc **Tháng**.
- Các nguồn lực chung không được phép có tên vị trí trống. 
- Việc đóng hợp đồng nếu bị mất sẽ không hủy bỏ các đăng ký trong tương lai.

**Bán hàng**
- Khi một môi trường có một khối lượng lớn sản phẩm, hiệu suất sẽ giảm trong lưới **Dự toán vật tư**.
- Khi tạo một dự án từ một mẫu, đơn vị tiền tệ của dự án không mặc định cho đơn vị ký hợp đồng của Người quản lý dự án tương ứng.
- Số tiền thực tế không phải lúc nào cũng khớp với những gì được phản ánh trên dự án đến hạn hoặc số tiền trở nên âm trong các tình huống thu hồi cụ thể.
- Lỗi xảy ra khi bạn liên kết một dự án được tạo từ mẫu dự án với một mô tả hợp đồng.
- Người dùng có thể xóa mô tả hợp đồng với các mốc quan trọng: **Sẵn sàng xuất hóa đơn** và **Hóa đơn đã được tạo**. Điều này không được phép.
- Khi dự toán được nhập từ một dự án, khả năng tính phí chi tiết của mô tả báo giá được đặt không chính xác khi tính năng thanh toán dựa trên tác vụ được bật cho mô tả báo giá.
- Khi bạn thêm cột mốc thanh toán giá cố định, cột mốc đó không được phản ánh trong lưới con cột mốc cho đến khi trang được làm mới.
- Một ngoại lệ tham chiếu rỗng được tạo ra khi bạn tạo hợp đồng dự án với tên trích dẫn là null.
- Các tác vụ ở chế độ thủ công trong đó đơn vị tiền tệ của dự án khác với đơn vị tiền tệ của nguồn lực dẫn đến dự toán giá không chính xác.
- Người dùng không thể nhớ lại giao dịch đã được sửa thành công bằng hóa đơn sửa.
- Các danh mục giao dịch đã hủy kích hoạt xuất hiện trong lưới **Dự toán chi phí**.



