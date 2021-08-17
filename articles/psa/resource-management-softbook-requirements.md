---
title: Đăng ký không chắc chắn yêu cầu
description: Chủ đề này cung cấp thông tin về cách đăng ký không chắc chắn yêu cầu.
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
ms.openlocfilehash: 95f064e0f83d2052ac4ae9673b4fcdcd16a2574246d3320e1ed3798cd6ff062b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007037"
---
# <a name="soft-book-requirements"></a>Đăng ký không chắc chắn yêu cầu

[!include [banner](../includes/psa-now-project-operations.md)]

Yêu cầu nguồn lực có thể được đăng ký chắc chắn. Đăng ký chắc chắn tạo ra đề xuất chiếm năng lực của nguồn lực. Sau đó, đề xuất này được gửi lại cho người yêu cầu để phê duyệt. Đăng ký không chắc chắn dự định bổ sung nguồn lực vào nhóm dự án và có trạng thái khác trên Bảng lịch trình nhưng không chiếm năng lực của nguồn lực. Để đăng ký không chắc chắn nguồn lực từ Bảng lịch trình, hãy đặt trường **Trạng thái đăng ký** thành **Không chắc chắn**.

![Trạng thái đăng ký được đặt thành Không chắc chắn.](media/Resource-Management-image77.png)

Khi tab **Nhóm** ở trong dạng xem **Thành viên nhóm có tên**, nguồn lực xuất hiện ở đó. Giờ đăng ký không chắc chắn được báo cáo trong cột **Giờ đăng ký không chắc chắn**.

![Giờ đăng ký không chắc chắn trong dạng xem Thành viên nhóm có tên.](media/Resource-Management-image78.png)

Có thể phân công nhiệm vụ cho các thành viên nhóm được đăng ký không chắc chắn.

![Thành viên nhóm được đăng ký không chắc chắn được phân công nhiệm vụ.](media/Resource-Management-image79.png)

Trên tab **Điều hòa**, không có đăng ký hiển thị cho nguồn lực được đăng ký không chắc chắn do tab **Điều hòa** chỉ xem xét các đăng ký chắc chắn.

![Nguồn lực được đăng ký không chắc chắn không có đăng ký trên tab Điều hòa.](media/Resource-Management-image80.png)

> [!NOTE]
> Bạn không thể đăng ký không chắc chắn nguồn lực từ yêu cầu do thành viên nhóm chung tạo.

Trên Bảng lịch trình, tô màu khác nhau được dùng cho đăng ký chắc chắn cho nguồn lực.

![Đăng ký không chắc chắn trên Bảng lịch trình.](media/Resource-Management-image81.png)

Để chuyển đổi đăng ký không chắc chắn thành đăng ký chắc chắn, trên Bảng lịch trình, hãy bấm chuột phải vào đăng ký chắc chắn rồi chọn **Thay đổi trạng thái** \> **Đăng ký chắc chắn** \> **Chắc chắn**.

![Thay đổi trạng thái đăng ký thành Chắc chắn.](media/Resource-Management-image82.png)

Đăng ký thay đổi và trạng thái được thay đổi trên Bảng lịch trình. Vì trạng thái đăng ký hiện là **Chắc chắn**, nên nguồn lực hiển thị ở trạng thái đã đăng ký và năng lực cũng như trạng thái rảnh/bận của nguồn lực được điều chỉnh.

Bạn có thể dùng cùng một phương pháp để đăng ký chắc chắn hoặc không chắc chắn từ Bảng lịch trình.

Để chuyển đổi nguồn lực được đăng ký không chắc chắn thành đăng ký chắc chắn trên tab **Nhóm**, hãy chọn nguồn lực rồi chọn **Xác nhận**.

![Lệnh xác nhận.](media/Resource-Management-image83.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]