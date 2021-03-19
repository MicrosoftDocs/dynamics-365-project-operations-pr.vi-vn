---
title: Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 16, V3
description: Chủ đề này liệt kê các tính năng và bản sửa lỗi có trong Bản phát hành cập nhật Project Service Automation 16, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
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
ms.openlocfilehash: 1f3bb4442ce1d06807f264003c930dbbee19a5c7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280919"
---
# <a name="project-service-automation-update-release-16-v3"></a>Phát hành bản cập nhật Project Service Automation 16, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Chúng tôi vui mừng thông báo bản cập nhật mới nhất dành cho ứng dụng Project Service Automation của Dynamics 365. Bản phát hành này bao gồm một số cải tiến quan trọng về chất lượng, hiệu suất và khả năng sử dụng.  Bản phát hành này tương thích với Dynamics 365 9.x. Để cập nhật lên bản phát hành này, hãy truy cập vào Trung tâm quản trị cho Dynamics 365 trực tuyến, rồi chuyển đến trang giải pháp để cài đặt bản cập nhật. Để biết thêm thông tin, hãy xem phần [Cài đặt, cập nhật giải pháp ưu tiên](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).
Chủ đề này liệt kê các tính năng và bản sửa lỗi mới hoặc đã thay đổi cho PSA V3, Bản phát hành cập nhật 16. Phiên bản này có số bản dựng là V3.10.6.34 và thường có sẵn thông qua bản tự cập nhật vào tháng 1 năm 2020.


## <a name="update-release-16"></a>Phát hành bản cập nhật 16

### <a name="bug-fixes"></a>Sửa lỗi

-   Thời gian và Chi phí

    -   Sửa lỗi: Người dùng cố gửi các mục nhập thời gian và chi phí đã xóa để phê duyệt giờ sẽ nhận được thông báo lỗi có liên quan.

-   Quản lý dự án

    -   Sửa lỗi: Đơn vị cấp nguồn lực đã xác định cho các thành viên nhóm trong mẫu được xem xét với mẫu được áp dụng cho dự án mới.

    -   Sửa lỗi: Cải thiện việc xử lý quá trình gán lại quyền sở hữu bản ghi.

    -   Sửa lỗi: Các dự án đang được sao chép sẽ không được phép sao chép cho đến khi tất cả các thao tác sao chép hoàn tất.

-   Quản lý nguồn lực

    -   Sửa lỗi: Thao tác mở rộng đăng ký giờ sẽ xử lý khoảng thời gian ngắn một cách chính xác và không còn tạo ra 0 giờ cho lượt đăng ký mở rộng.

    -   Sửa lỗi: Dạng xem điều hòa giờ sẽ hiển thị khi múi giờ dự án là +5:30 GMT và múi giờ của người dùng là khác nhau.

-   Sales

    -   Sửa lỗi: Khi một dự án đã ánh xạ đến mô tả hợp đồng bị xóa và một dự án mới được ánh xạ, bản ghi thực tế trên dự án mới không được đánh giá lại dựa trên các quy tắc thanh toán và định giá đã xác định trên mô tả hợp đồng. Lỗi này đã được khắc phục trong bản phát hành này. Bản ghi thực tế và giá trên dự án mới được ánh xạ sẽ bị hủy bỏ và được tạo lại chính xác dựa trên các quy tắc định giá và thanh toán của mô tả hợp đồng. Kết quả là bản ghi thực tế của dự án không được ánh xạ cũng sẽ được đánh giá lại và tạo lại.

    -   Sửa lỗi: Thêm xác thực bổ sung vào trường **Số tiền** của mô tả ước tính để đảm bảo rằng các giá trị rỗng không được giữ tiếp tục.

    -   Sửa lỗi: Khi dữ liệu thực tế đã được cập nhật trên một dự án, một nút làm mới đã được thêm vào biểu mẫu chính của dự án để cho phép người dùng đồng bộ hóa lại dữ liệu thực tế.

    -   Sửa lỗi: Khi người dùng nâng cấp từ 2.X lên 3.X, các dự án có giá trị RỖNG cho tên dự án sẽ được cho phép.



[!INCLUDE[footer-include](../includes/footer-banner.md)]