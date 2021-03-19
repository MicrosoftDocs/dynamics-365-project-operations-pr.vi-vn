---
title: Chỉ định nguồn lực cho nhiệm vụ
description: Chủ đề này cung cấp thông tin về cách gán tài nguyên cho công việc.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
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
ms.openlocfilehash: 486371df2de8b400f200dbf38e66cb5e2dec7ae7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286274"
---
# <a name="assign-a-resource-to-a-task"></a>Gán nguồn lực cho nhiệm vụ

[!include [banner](../includes/psa-now-project-operations.md)]

Có 3 cách để gán nguồn lực cho một nhiệm vụ trong Microsoft Dynamics 365 Project Service Automation.

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Đăng ký một nguồn lực là một thành viên nhóm và sau đó gán nguồn lực cho nhiệm vụ

Bạn có thể thêm nguồn lực vào nhóm dự án và sau đó gán nguồn lực cho nhiệm vụ trong lịch trình dự án.

1. Trên tab **Thành viên nhóm**, thêm một thành viên nhóm bằng cách chọn **Mới**. 

2. Bảng điều khiển **Tạo nhanh Thành viên nhóm** mở ra, ở đây bạn có thể chọn tên nguồn lực có thể đăng ký được và đặt vai trò. 

    Chọn một trong các phương pháp phân bổ sau để đăng ký nguồn lực:

    - **Năng lực đầy đủ** đăng ký năng lực đầy đủ của nguồn lực theo các ngày bắt đầu và kết thúc đã được chỉ định.
    - **Năng lực tỉ lệ phần trăm** đăng ký nguồn lực theo tỉ lệ phần trăm năng lực của nguồn lực theo những ngày bắt đầu và kết thúc.
    - **Phân phối theo giờ đồng đều** sẽ đăng ký nguồn lực cho số giờ được chỉ định, phương pháp này phân phối thời gian mỗi ngày đều nhau cho các ngày đã được chỉ định kể từ khi bắt đầu cho tới khi kết thúc.
    - **Phân phối không đồng đều** đăng ký nguồn lực cho số giờ được chỉ định, phương pháp này phân phối không đồng đều thời gian cho mỗi ngày trong các ngày được chỉ định từ khi bắt đầu cho tới khi kết thúc.
    - Lựa chọn **Không có** sẽ thêm nguồn lực cho nhóm nhưng không tạo bất kỳ đăng kỳ nào mà sử dụng năng lực của nguồn lực.

3. Trên lưới **Lịch trình** cho nhiệm vụ, chọn biểu tượng **Nguồn lực** trong ô nguồn lực, sau đó trong **Thành viên nhóm**, chọn thành viên nhóm bạn vừa mới thêm vào. 

> [!NOTE]
> Trên cả tab **Thành viên Nhóm** và **Hợp nhất**, nguồn lực hiển thị số giờ đã được đăng ký và số giờ được gán. Số giờ nên giống nhau nhưng không bắt buộc vì đặt lịch và phân công không ghép đôi chặt chẽ với nhau. Tab **Hợp nhất** cho bạn chi tiết khi chúng khác nhau, như khi bạn gán cho một nguồn lực số giờ nhiều hơn số giờ mà bạn đã đăng ký. Nếu cần, bạn có sửa thông tin này bằng cách mở rộng đăng ký của nguồn lực hoặc đổi phân công.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Tạo thành viên nhóm chung bằng phân công nhiệm vụ

Khi bạn tạo thành viên nhóm chung thông qua chỉ định nhiệm vụ, bạn tạo một nguồn lực chung hoặc nguồn lực giữ chỗ mà mô tả các đặc điểm của nguồn lực được đặt tên, cuối cùng bạn muốn làm việc với nhiệm vụ bằng cách tạo nhóm sau khi gán vai trò cho nhiệm vụ. Sau đó bạn tạo một yêu cầu (hoặc gửi một yêu cầu bằng cách sử dụng yêu cầu) mà được dùng để tìm và đăng ký nguồn lực được đặt tên.

1. Trên lưới **Lịch trình** cho nhiệm vụ, chọn biểu tượng **Nguồn lực** trong ô nguồn lực.

2. Nhập một tên để làm tên của nguồn lực đặt chỗ. Ví dụ: Người quản lý Chương trình.

3. Chọn **Tạo** và trong trường **Tạo nhanh Thành viên Nhóm Dự án**, đặt vai trò cho nguồn lực chung.

4. Bạn có thể tiếp tục gán nhiệm vụ cho nguồn lực giữ chỗ này bằng cách chọn nguồn lực trên **Bộ chọn nguồn lực** cho nhiệm vụ. Chúng được liệt kê trong phần **Thành viên Nhóm**.

5. Khi bạn hoàn thành việc gán nguồn lực chung, chọn nguồn lực chung trên tab **Nhóm** và sau đó chọn **Tạo yêu cầu** để tạo yêu cầu nguồn lực cho nguồn lực chung.

6. Chọn **Đăng ký** cho nguồn lực chung. Sau đó bạn có thể dùng bảng Lịch trình để tìm và đăng ký nguồn lực thực. Bạn cũng có thể gửi yêu cầu để thực hiện bởi người quản lý nguồn lực.

7. Khi nguồn lực chung được hoàn thành bằng nguồn lực được đặt tên, nguồn lực chung sẽ được loại bỏ khỏi nhóm và các phân công nhiệm vụ cho nguồn lực chung được gán cho nguồn lực được đặt tên mà hoàn thành yêu cầu nguồn lực của nguồn lực.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Gán một nguồn lực được đặt tên từ danh sách tất cả các nguồn lực có thể đăng ký được

Bạn có thể dùng hộp tìm kiếm trong **Bộ chọn nguồn lực** để tìm tất cả các nguồn lực có thể đăng ký và gán nguồn lực cho nhiệm vụ.

Các tài nguyên được chỉ định theo cách này sẽ được thêm vào nhóm mà không có bất kỳ đặt chỗ nào. Điều này tương tự như việc thêm một thành viên trong nhóm và chọn Không có làm phương pháp phân bổ. Nguồn lực được hiển thị trong tab **Nhóm** và tab **Hợp nhất** như là nguồn lực chỉ có phân công còn đặt chỗ bị thâm hụt. Đăng ký chúng nếu bạn muốn sử dụng tính sẵn có của chúng.

1. Trên lưới **Lịch trình** cho nhiệm vụ, chọn biểu tượng **Nguồn lực** trong ô nguồn lực.

2. Bắt đầu gõ vào một tên. Kết quả tìm kiếm cho tên được hiện thị trong **Bộ chọn nguồn lực** trong phần **Các nguồn lực khác**.

3. Chọn tài nguyên mà bạn muốn gán cho tác vụ.



[!INCLUDE[footer-include](../includes/footer-banner.md)]