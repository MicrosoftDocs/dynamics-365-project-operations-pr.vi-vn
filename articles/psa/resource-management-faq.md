---
title: Câu hỏi thường gặp về quản lý nguồn lực
description: Chủ đề này cung cấp câu trả lời cho các câu hỏi thường gặp về quản lý nguồn lực.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 395aa57d73e5d4a0c9c827c79bf4e7ef229c3981
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087319"
---
# <a name="resource-management-faq"></a>Câu hỏi thường gặp về quản lý nguồn lực

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a>Sự khác biệt giữa một thành viên nhóm và yêu cầu nguồn lực là gì?

Thành viên nhóm dự án có thể được phân công cho các nhiệm vụ, được đăng ký hoặc đăng ký quá mức và đặt làm người phê duyệt. Yêu cầu nguồn lực có thể tồn tại mà không có thành viên nhóm dự án, ở dạng ghi chú nháp về nhu cầu. 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a>Sự khác biệt giữa giờ đề xuất và giờ đăng ký không chắc chắn là gì?

Giờ được đề xuất và giờ đăng ký không chắc chắn khác nhau về khả năng hiển thị. Chỉ có người quản lý nguồn lực và người quản lý dự án bắt đầu nhu cầu bằng yêu cầu nguồn lực mới có thể xem giờ đề xuất. Mọi người có quyền truy cập Bảng lịch trình đều có thể xem giờ đăng ký không chắc chắn.

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a>Làm cách nào để có thể xem giờ đăng ký không chắc chắn cho các nguồn lực trên nhóm?

Khi đăng ký yêu cầu nguồn lực, bạn có thể đăng ký không chắc chắn. Nguồn lực được đăng ký không chắc chắn trên nhóm dự án xuất hiện ở dạng thành viên nhóm có giờ đăng ký không chắc chắn. Họ cũng xuất hiện trên Bảng lịch trình.

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a>Làm cách nào để thay đổi giờ yêu cầu, ngày bắt đầu và ngày kết thúc cho nguồn lực (chung hoặc có tên) mà bạn đã đăng ký?

Sau khi nguồn lực được đăng ký, hãy chọn **Duy trì đăng ký** để thực hiện mọi thay đổi cần thiết.

## <a name="what-resources-types-does-project-service-automation-support"></a>Project Service Automation hỗ trợ những loại nguồn lực nào?

Chỉ có các loại nguồn lực **Người dùng** và **Liên hệ** được hỗ trợ trong Dynamics 365 Project Service Automation. Mặc dù bạn có thể tạo các loại nguồn lực khác (ví dụ: **Thiết bị** và **Nhóm** ), nhưng không có trường hợp sử dụng toàn diện nào được hỗ trợ cho các nguồn lực này.

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a>Sự khác biệt giữa phân công và đăng ký là gì?

Phân công là phân công nguồn lực cho các nhiệm vụ dự án trong lịch trình dự án. Các nguồn lực có thể là các nguồn lực thật hoặc chung. Đăng ký là việc phân bổ nguồn lực cho dự án theo cách chắc chắn hoặc không chắc chắn. Đăng ký chắc chắn chiếm năng lực của nguồn lực. Đối với các nguồn lực thực, tốt nhất là đăng ký và phân công nên nhất quán vì không khác nhau. Tuy nhiên, PSA không thực thi thỏa thuận này. Dạng xem Điều hòa hiển thị cho người quản lý dự án nơi đăng ký và phân công của nguồn lực không nhất quán.