---
title: Tạo đăng ký dự án từ bảng Lịch trình
description: Chủ đề này cung cấp thông tin về cách tạo đặt chỗ dự án từ bảng lịch trình.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: 57fbc71681015fca73cdda4bc7d392f6be4289f3
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087125"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a>Tạo đăng ký dự án từ bảng Lịch trình

Bạn có thể đăng ký nguồn lực trên dự án bằng cả cách trực tiếp trên tab **Nhóm** của dự án hoặc bằng cách tạo yêu cầu nguồn lực từ phân công thành viên nhóm chung và sau đó thực hiện yêu cầu được tạo với thành viên nhóm dự án.

Bạn cũng có thể đăng ký nguồn lực trên dự án trực tiếp từ bảng Lịch trình. Có ba cách để thực hiện việc này:

- **Đăng ký từ một yêu cầu nguồn lực được tạo:** Bạn có thể tạo một yêu cầu nguồn lực sau khi tạo một tài nguyên chung và gán tác vụ trong một dự án.

- **Đặt lịch từ yêu cầu chính:** Các yêu cầu chính hiển thị trên bảng Lịch trình trên tab **Dự án**. 

- **Đặt lịch từ một yêu cầu nguồn lực mới:** Bạn có thể tạo một yêu cầu nguồn lực từ đầu và liên kết với một dự án. Trên bảng Lịch trình, yêu cầu nguồn lực hiển thị trên tab **Mở yêu cầu**.

## <a name="book-from-a-generated-resource-requirement"></a>Đăng ký từ một yêu cầu nguồn lực được tạo

Bạn có thể tạo nguồn lực chung và gán cho nguồn lực một hoặc nhiều nhiệm vụ ở trong dự án. Sau đó, bạn có thể tạo yêu cầu nguồn lực từ thành viên nhóm chung. 

1.  Trên bảng Lịch trình, nguồn lực này sẽ hiển thị trên tab **Mở yêu cầu**. Bạn sẽ cần dùng các bộ lọc cột trên lưới nếu bạn có nhiều yêu cầu mở. 

    ![Mở tab Yêu cầu trên bảng Lịch trình](media/FAQ-Project-Booking-Schedule-Board-1.png "Ảnh chụp màn hình khi đăng ký và bảng phân công")

2. Chọn yêu cầu. Tab **Tìm khả năng đáp ứng** sẽ xuất hiện ở phía trên dòng được chọn.
 
3. Khi bạn chọn tab này, chế độ Trợ lý Lịch trình trên bảng Lịch trình sẽ mở ra và lọc các nguồn lực sẵn có đáp ứng được yêu cầu nguồn lực. Sau đó, bạn có thể đăng ký nguồn lực.

4. Bạn cũng có thể kéo và thả dòng được chọn ở phía dưới bảng Lịch trình tới ô nguồn lực trong lưới ở trên. Khi bạn thả ra, yêu cầu sẽ mở bảng điều khiển **Tạo đăng ký nguồn lực** ở bên phải.

    Chọn **Đăng ký** để đăng ký nguồn lực trên nhóm dự án.

![Tạo bảng điều khiển Đăng ký Nguồn lực](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a>Đăng ký từ Yêu cầu Chính

Tạo dự án tự động trong Project Service sẽ tự động tạo yêu cầu nguồn lực được gọi là Yêu cầu Chính. Đây là một yêu cầu rỗng được dùng để đăng ký nhanh chóng nguồn lực bằng bảng Lịch trình mà không phải tạo yêu cầu hoặc tạo nguồn lực từ đầu. Bởi vì yêu cầu này rỗng, bạn sẽ cần xác định ngày cũng như phương pháp phân bổ và số giờ nếu áp dụng. 

1. Để đăng ký nguồn lực bằng Yêu cầu Chính, trên bảng Lịch trình, chọn tab **Dự án**. Bạn sẽ cần dùng bộ lọc cột trên cột **Dự án** nếu bạn có nhiều dự án.

   ![Bộ lọc cột trên bảng Lịch trình](media/FAQ-Project-Booking-Schedule-Board-2.png "Ảnh chụp màn hình khi đăng ký và bảng phân công")

2. Chọn yêu cầu mà chỉ có tên dự án có cùng tên đó và có khoảng thời gian là không (0).

3. Chọn tab **Tìm sẵn có** hiện ở trên dòng. Điều này khiến bảng Lịch trình trong chế độ Trợ lý Lịch trình và hiện các nguồn lực sẵn có mà có thể được đăng lý trên dự án.

4. Bởi vì **Yêu cầu Chính** là một yêu cầu rỗng có khoảng thời gian bằng không (0), bạn sẽ cần đặt khoảng thời gian trên bảng điều khiển **Tạo đăng ký nguồn lực** khi chọn và đăng ký nguồn lực.

5. Bạn cũng có thể chọn **Yêu cầu Chính của Dự án** ở cuối bảng Lịch trình và kéo, thả yêu cầu vào nguồn lực để đăng ký.
 
    Bởi vì **Yêu cầu Chính** là một yêu cầu rỗng có khoảng thời gian bằng không (0), bạn sẽ cần đặt khoảng thời gian trên bảng điều khiển **Tạo đăng ký nguồn lực** khi chọn và đăng ký nguồn lực.
 
    Khi bạn đăng ký nguồn lực qua **Yêu cầu Chính** trên bảng Lịch trình, bạn thêm nguồn lực vào nhóm dự án mà không cần phân công.
 
## <a name="book-from-a-new-resource-requirement"></a>Đăng ký từ yêu cầu nguồn lực mới
Hoàn tất các bước sau để đặt lịch từ một yêu cầu nguồn lực mới. 

1. Chuyển tới **Yêu cầu nguồn lực** và chọn **Mới** để tạo yêu cầu nguồn lực mới.

2. Trên tab **Dự án** , chọn một dự án liên kết yêu cầu dự án.
 
    Trên bảng Lịch trình, yêu cầu mới này hiển thị là **Yêu cầu Mở** trên bảng lịch trình mà bạn có thể thực hiện.

3. Đăng ký nguồn lực để thêm nguồn lực vào nhóm dự án.

4. Bây giờ, nguồn lực đã được đăng ký, bạn phải gán nhiệm vụ theo cách thủ công.

