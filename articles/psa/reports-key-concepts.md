---
title: Khái niệm chính
description: Chủ đề này cung cấp thông tin về các khái niệm chính để quản lý nguồn lực trong Project Service Automation.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 3a0305ab35a28348798f9d9c7452b3bee75412e4
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8601274"
---
# <a name="key-concepts"></a>Khái niệm chính

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Bảng sau đây xác định các khái niệm chính được sử dụng trong ứng dụng Dynamics 365 Project Service Automation.

| Khái niệm                    | Định nghĩa |
|----------------------------|------------|
| Thành viên nhóm dự án        | Là một phần của nhóm dự án, thành viên nhóm dự án có thể là nguồn lực có tên có đăng ký, nguồn lực có tên không có đăng ký hoặc nguồn lực chung. Nguồn lực chung không có đăng ký, là cục bộ cho dự án, và không có rằng buộc năng lực trên các dự án. |
| Nguồn lực chung của dự án   | Chỗ dành sẵn cho nguồn lực cho phép bạn tạo nhóm và bố trí nhân lực cho kế hoạch dự án mà không cần biết nguồn lực có tên. Lịch dự án được sử dụng như lịch của nguồn lực chung. Nguồn lực chung có thể được thêm vào nhóm dự án và phân công cho nhiệm vụ. |
| Số giờ đã đăng ký               | Giờ nguồn lực được đăng ký chắc chắn với dự án giúp đảm bảo công việc dự án được hoàn thành. Giờ đã đăng ký sử dụng năng lực tổng thể của nguồn lực. Đăng ký chỉ dựa trên các nguồn lực có tên, không dựa trên các nguồn lực chung. |
| Giờ đã phân công             | Giờ nguồn lực được phân công cho các nhiệm vụ trong lịch trình dự án. Phân công có thể dựa trên nguồn lực có tên hoặc nguồn lực chung. Phân công có thể độc lập với đăng ký. |
| Giờ yêu cầu             | Năng lực được yêu cầu nhưng chưa được nguồn lực có tên thực hiện. Giờ yêu cầu chỉ liên quan đến các thành viên nhóm chung có yêu cầu nguồn lực được tạo. |
| Nhu cầu                     | Khối lượng công việc hiện tại và sắp tới. Trong Project Service Automation, nhu cầu hiển thị ở dạng yêu cầu nguồn lực. |
| Yêu cầu nguồn lực       | Một thực thể dùng để ghi lại ngày bắt đầu và kết thúc, kỹ năng, địa lý, giờ yêu cầu và tham số giá khác cho nguồn lực yêu cầu. Yêu cầu nguồn lực được tạo từ thành viên nhóm dự án hoặc được tạo riêng. |
| Yêu cầu nguồn lực           | Thực thể được dùng ở dạng "phong bì" để thực hiện yêu cầu nguồn lực phải được người quản lý nguồn lực thực hiện. |
| Vai trò mặc định của nguồn lực      | Vai trò mà nguồn lực được nhóm trong tính toán thời gian làm việc. Nguồn lực được giả định có các kỹ năng cần thiết cho vai trò và để đáp ứng thời gian làm việc mục tiêu cho vai trò đó. |
| Đơn vị tổ chức của nguồn lực | Đơn vị tổ chức mà nguồn lực được phân công đến. |
| Đường cong                    | Nhiệm vụ, yêu cầu hoặc giờ phân công được chia thành phân phối hàng ngày. Ví dụ: nhiệm vụ 5 ngày, 40 giờ có thể được đánh dấu bằng đường mức thành 8 giờ mỗi ngày trong 5 ngày. |
| Dạng xem điều hòa        | Dạng xem cho biết các đăng ký và phân công cho từng thành viên nhóm dự án. Dạng xem cho phép người quản lý dự án tìm mọi điểm không phù hợp giữa đăng ký và nhiệm vụ và thực hiện hành động khắc phục nếu có điểm không phù hợp xảy ra. |
| Giờ làm việc                 | Một thực thể dùng để xác định năng lực nguồn lực, giờ làm việc và không làm việc. Thực thể này cũng được gọi là lịch nguồn lực. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
