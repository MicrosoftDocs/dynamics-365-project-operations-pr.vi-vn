---
title: Đặt trước nguồn lực có thể đặt lịch có tên cho nhóm dự án và chỉ định nhiệm vụ
description: Chủ đề này cung cấp thông tin về cách đặt trước nguồn lực được nêu tên cho nhóm dự án và chỉ định nhiệm vụ cho nguồn lực.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
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
ms.openlocfilehash: defc92e701ae6baf9d54f41dca123a09ef834c35
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087227"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a>Đặt trước nguồn lực có thể đặt lịch có tên cho nhóm dự án và chỉ định nhiệm vụ 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Bạn có thể thêm nguồn lực được đặt tên vào nhóm dự án của mình bằng cách đặt lịch trực tiếp họ vào nhóm. Để làm như vậy, hãy hoàn thành các bước sau đây.

1. Trong Project Service Automation, truy cập **Dự án** , sau đó chọn mở dự án mà bạn đặt lịch.
2. Trên trang **Dự án** , trên tab **Nhóm** , nhấp vào **Mới**. 

![Thêm thành viên nhóm từ tab Nhóm](media/RM-how-to-1.png)

3. Trong hộp thoại **Tạo nhanh thành viên nhóm dự án** , chọn nguồn lực có thể đặt lịch. Trường **Vai trò** sẽ điền bằng vai trò mặc định của nguồn lực nếu họ được chỉ định. Bạn có thể thay đổi vai trò này nếu cần. 
4. Chọn ngày bắt đầu và kết thúc mà nguồn lực sẽ cần và chọn phương pháp phân bổ năng lực của nguồn lực. 
5. Nếu bạn muốn thành viên nhóm là người phê duyệt dự án, chọn **Có** trong trường **Người phê duyệt dự án**. Điều này có nghĩa là thành viên nhóm có thể phê duyệt các mục nhập thời gian và chi phí đã gửi cho dự án này. 
6. Bấm vào **Lưu**.

![Thêm thành viên nhóm trên biểu mẫu tạo nhanh](media/RM-how-to-2.png)


Bây giờ bạn có thể gán nguồn lực đã đặt cho các nhiệm vụ dự án. Trên trang **Dự án** , nhấp và tab **Lên lịch** để gán nhiệm vụ cho tài nguyên mới. Bộ chọn nguồn lực được khởi chạy từ trường **Nguồn lực** trong lưới nhiệm vụ sẽ hiển thị các thành viên nhóm mà bạn có thể chọn.

![Chỉ định thành viên nhóm cho nhiệm vụ trên tab lịch trình](media/RM-how-to-3.png)

Trong phiên bản 3 của Project Service Automation (PSA), việc đặt lịch nguồn lực và gán nhiệm vụ không ghép đôi chặt chẽ với nhau. Điều này có nghĩa là khi bạn sử dụng bộ chọn nguồn lực trong lịch trình, bạn có thể gán nhiệm vụ cho các thành viên trong nhóm trong nhiều giờ hơn so với đặt lịch của họ trên dự án.
Bạn có thể thấy sự khác biệt giữa đặt lịch và phân công thành viên nhóm trên tab **Nhóm** hoặc tab **Hợp nhất nguồn lực**. Bạn cũng có thể hợp nhất sự khác biệt giữa các đặt chỗ và phân công cho các nguồn lực ở mức chi tiết hơn.

![Tab hợp nhất nguồn lực](media/RM-how-to-4.png)

Bạn cũng có thể sử dụng bộ chọn nguồn lực trên tab **Lên lịch** để tìm kiếm và chọn các nguồn lực có thể đặt lịch không phải là một phần của nhóm dự án. Chúng được hiển thị trong bộ chọn nguồn lực dưới dạng **Nguồn lực khác**.

![Phân công nhiệm vụ cho một nguồn lực không phải thành viên nhóm](media/RM-how-to-5.png)

Khi bạn thực hiện việc này, nguồn lực đó sẽ được thêm vào nhóm dự án và phân công tác vụ, nhưng không tạo đặt lịch.

![Thành viên nhóm được phân công và không có đặt lịch](media/RM-how-to-6.png)

Bạn có thể sử dụng khả năng đặt lịch mở rộng của tab **Hợp nhất** hoặc **Bảng lịch trình** để đặt lịch năng lực của nguồn lực cho dự án.

![Mở rộng các đặt lịch cho một thành viên nhóm trên tab hợp nhất nguồn lực](media/RM-how-to-7.png)

Sau khi một thành viên nhóm được đặt lịch trên dự án của bạn, bạn có thể sử dụng duy trì đặt phòng hoặc sử dụng Bảng lịch trình để trực tiếp quản lý đặt lịch của họ.
