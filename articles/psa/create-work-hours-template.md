---
title: Tạo mẫu giờ làm việc
description: Chủ đề này mô tả cách tạo mẫu giờ làm việc trong Project Service.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 5788378c7e015c4b11182aaf427aca7d1da48b40
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598974"
---
# <a name="create-a-work-hours-template-project-service"></a>Tạo mẫu giờ làm việc (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

Để tạo và quản lý dự án, bạn cần phải áp dụng mẫu lịch cho dự án. Mẫu lịch xác định các thuộc tính sau của dự án:

- Giờ làm việc, bao gồm thời gian bắt đầu và kết thúc
- Ngày làm việc
- Trường hợp ngoại lệ của lịch, chẳng hạn như những ngày không làm việc

Mẫu lịch được áp dụng cho dự án là bản sao của mẫu lịch được xác định trong cài đặt tổ chức của bạn.

> [!NOTE]
> Nếu bạn thay đổi mẫu lịch, những thay đổi đó sẽ không ảnh hưởng đến giờ làm việc của dự án. Để thay đổi giờ làm việc của dự án, bạn cần áp dụng mẫu mới.

Để tạo mẫu lịch cho tổ chức của bạn, có hai yêu cầu chính:

- Xác định giờ làm việc mong muốn của mẫu bằng cách sử dụng nguồn lực có thể đặt trước mới hoặc hiện có.
- Tạo mẫu lịch mới và liên kết mẫu với nguồn lực có thể đặt trước.

**Xác định số giờ làm việc của mẫu**

1. Truy cập vào **Nguồn lực** \> **Nguồn lực**.
2. Tạo nguồn lực mới để tham chiếu trong mẫu lịch hoặc chọn một nguồn lực hiện có.
3. Chọn tab **Giờ làm việc** của nguồn lực và hoàn thành các hướng dẫn trong [Đặt giờ làm việc cho một nguồn lực](/dynamics365/field-service/set-work-hours-resource) để định cấu hình các quy tắc lịch.

**Tạo mẫu lịch mới**

1. Chuyển đến phần **Cài đặt** \> **Mẫu lịch**.
2. Chọn **Mới** rồi nhập tên, mô tả và nguồn lực mẫu.


> [!NOTE]
> Khi nguồn lực được tham chiếu trong mẫu lịch, bản sao lịch của nguồn lực được liên kết với mẫu lịch. Nếu giờ làm việc của mẫu đã sao chép thay đổi, những thay đổi đó sẽ không ảnh hưởng đến mẫu lịch.


### <a name="see-also"></a>Xem thêm  
 [Thiết lập nguồn lực](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
