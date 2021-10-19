---
title: Xác định lịch dự án
description: Chủ đề này cung cấp thông tin về cách áp dụng mẫu lịch cho dự án để theo dõi tiến độ dự án.
author: ruhercul
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9c2ea49e008d6cde40f152320face073c7e5f548
ms.sourcegitcommit: bbe484e58a77efe77d28b34709fb6661d5da00f9
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 09/10/2021
ms.locfileid: "7487666"
---
# <a name="define-project-calendars"></a>Xác định lịch dự án

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

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

Bạn hiện có thể liên kết mẫu công việc với mẫu lịch dự án.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

