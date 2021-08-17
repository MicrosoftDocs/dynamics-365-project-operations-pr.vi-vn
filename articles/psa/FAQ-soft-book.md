---
title: Đặt lịch một nguồn lực
description: Chủ đề này cung cấp thông tin về cách lên lịch trình dự định hoặc đặt lịch các thành viên thuộc nhóm dự án.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/25/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.app:
- ProjectOperations
ms.openlocfilehash: cf67769fef39f95785320ae38055f0a3359b3a82d996b740bdb5d51e864f3d56
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005372"
---
# <a name="soft-book-a-resource"></a>Đặt lịch một nguồn lực

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Bạn có thể lên lịch trình dự kiến hoặc "đăng ký dự kiến" nguồn lực trên nhóm dự án để hiện nguồn lực bạn lên kế hoặc để gán nguồn lực cho dự án. Đăng ký dự kiến không sử dụng năng lực sẵn có của nguồn lực và bạn có thể gán thành viên nhóm được đăng ký dự kiến cho nhiệm vụ dự án. Tuy nhiên, vì đăng ký dự kiến không sử dụng năng lực của nguồn lực, bạn vẫn có thể "đăng ký xác nhận" nguồn lực cho các nhiệm vụ khác trong cùng khoảng thời gian. Không thể đăng ký dự kiến nguồn lực chung, cũng không thể đáp ứng yêu cầu đăng ký dự kiến cho một nguồn lực chung.

Thành viên nhóm dự án đã đặt dự kiến được liệt kê trên tab **Team** của trang **Dự án** với số giờ đặt lịch dự kiến hiển thị trên cột **Số giờ đặt lịch dự kiến** trong dạng xem **Thành viên nhóm được đặt tên**. Thành viên nhóm được đăng ký dự kiến cũng được liệt kê trên bảng Lịch trình. Vì họ được đăng ký dự kiến, nên Bảng lịch trình không hiện bất kỳ mức sử dụng năng lực nào cho các nguồn lực này. Thời gian được đăng ký dự kiến không hiển thị trên tab **Hợp nhất**, cũng không hiển thị trong trường **Đăng ký Mở rộng** trong tab **Hợp nhất** của bảng Lịch trình. 

Có hai cách để đăng ký dự kiến thành viên nhóm trên dự án: trực tiếp từ bảng Lịch trình hoặc bằng cách thêm thành viên nhóm trên tab **Nhóm**. 

## <a name="soft-book-from-the-schedule-board"></a>Đăng ký dự kiến từ bảng Lịch trình
Hoàn tất các bước sau để đặt lịch dự kiến một tài nguyên từ bảng Lịch trình. 

1. Mở bảng Lịch trình, sau đó trong bảng điều khiển **Yêu cầu đặt lịch**, chọn tab **Dự án**.
2. Tìm dự án bạn muốn đăng ký dự kiến nguồn lực. Nếu có một số lượng lớn các dự án trong danh sách, hãy chọn tiêu đề cột **Dự án** rồi dùng bộ lọc để tìm kiếm một hoặc nhiều dự án.
3. Chọn dự án, sau đó kéo và thả vào lưới thời gian của nguồn lực.
5. Trong bảng điều khiển **Tạo đặt lịch nguồn lực**, hãy điều chỉnh ngày bắt đầu và kết thúc, đặt **Trạng thái đặt lịch** thành **Dự kiến**, sau đó đặt giờ. 
6. Nhấp vào **Đăng ký**. Lúc này, nguồn lực hiển thị trên tab **Nhóm** dưới dạng nguồn lực cho dự án. Trên dạng xem **Thành viên Nhóm được Đặt tên**, bạn sẽ thấy số giờ được đăng ký dự kiến trong cột **Số giờ được Đăng ký Dự kiến**.

> [!NOTE]
> Lúc này, bạn có thể gán đăng ký dự kiến cho nhiệm vụ trên tab **Lịch trình**. Trên tab **Hợp nhất**, nguồn lực hiển thị sự thâm hụt đăng lý liên quan tới sự phân công nhiệm vụ vì tab **Hợp nhất** chỉ xem xét đăng ký đã xác nhận. Bạn có thể dùng tính năng **Đăng ký Mở rộng** để đăng ký xác nhận nhằm loại bỏ sự thâm hụt đăng lý xác nhận đối với phân công nguồn lực. Bạn sẽ phải hủy bỏ thủ công việc đăng ký dự kiến cho nguồn lực bằng cách sử dụng **Đăng ký Duy trì**.

## <a name="soft-book-on-the-team-tab"></a>Đăng ký dự kiến trên tab Nhóm

Bạn có thể thêm thành viên nhóm trực tiếp trên tab **Nhóm**, sau đó đổi trạng thái đăng ký của các thành viên từ **Xác nhận** sang **Dự kiến** bằng **Đăng ký Duy trì**. Khi bạn thêm thành viên nhóm theo cách này, sẽ có kết quả là đăng ký xác nhận trừ khi bạn chọn phương pháp phân bổ là **Không có**.

Để sử dụng phương pháp này, hãy hoàn tất các bước sau.

1. Trên trang **Dự án**, trên tab **Nhóm**, nhấp vào **Mới**.
2. Chọn ngày bắt đầu, kết thúc, vai trò, nguồn lực có thể đăng ký được.
3. Chọn một phương pháp phân bổ khác với **Không có**.
4. Chọn **Lưu**. Bạn sẽ thấy nguồn lực trên lưới và số giờ của họ trong cột **Số giờ được Đăng ký Xác nhận**.
5. Duy trì trạng thái đăng ký của nguồn lực bằng cách chọn **Duy trì Đăng ký**.
6. Khi bảng Lịch trình mở ra, hãy mở rộng nguồn lực để hiển thị các đăng ký. Bạn sẽ thấy đăng ký hiển thị là **Xác nhận**.
7. Nhấp chuột phải vào đăng ký, trong **Thay đổi Trạng thái**, chọn **Đăng ký Dự kiến** \> **Dự kiến**. Trạng thái đăng ký bây giờ là **Dự kiến**.
8. Sau khi đóng bảng Lịch trình, bạn sẽ thấy số giờ cho nguồn lực được di chuyển từ cột **Số giờ được Đăng ký Xác nhận** sang **Số giờ được Đăng ký Dự kiến** trên lưới tab **Nhóm**, khi nhìn vào dạng xem **Thành viên Nhóm được Đặt tên**.

> [!NOTE]
> Khi bạn sử dụng **Duy trì đăng ký** để thay đổi trạng thái từ **Xác nhận** sang **Dự kiến**, nếu bạn đăng ký xác nhận một nguồn lực trên nhóm rồi chỉ định nhiệm vụ cho nguồn lực đó, thì phân công nhiệm vụ cho nguồn lực đó sẽ được duy trì. Tuy nhiên, trên tab **Hợp nhất**, nguồn lực sẽ có sự thâm hụt đăng ký vì chỉ đăng ký xác nhận được xem xét khi hợp nhất đăng ký với phân công. Bạn có thể dùng tính năng **Đăng ký Mở rộng** trên tab **Hợp nhất** để đăng ký xác nhận nguồn lực nhằm loại bỏ sự thâm hụt đăng ký xác nhận so với phân công nguồn lực. Bạn sẽ phải hủy bỏ thủ công việc đăng ký dự kiến cho nguồn lực bằng cách sử dụng **Duy trì đăng ký**.

Khi bạn sẵn sàng đổi nguồn lực thành viên nhóm được đăng ký dự kiến sang thành viên nhóm được đăng ký xác nhận, thực hiện như sau:

1. Trên bảng Lịch trình, mở rộng nguồn lực để hiện các đăng ký. Bạn sẽ thấy đăng ký được hiện là **Dự kiến**.
2. Nhấp chuột phải vào đăng ký, trong **Thay đổi Trạng thái**, chọn **Đăng ký Xác nhận** \> **Xác nhận**. Trạng thái đăng ký bây giờ là **Xác nhận**.
3. Sau khi bạn đóng bảng Lịch trình, hãy quay trở lại dự án và mở tab **Nhóm**, bạn sẽ thấy số giờ cho nguồn lực được di chuyển từ cột **Số giờ được Đăng ký Dự kiến** sang cột **Số giờ được đăng ký Xác nhận** trên tab **Nhóm** khi ở dạng xem **Thành viên Nhóm được Đặt tên**. Nếu nguồn lực đã được gán cho nhiệm vụ, nguồn lực sẽ không còn hiện sự thâm hụt đăng ký trên tab **Hợp nhất** vì các đăng ký hiện đang là xác nhận.



[!INCLUDE[footer-include](../includes/footer-banner.md)]