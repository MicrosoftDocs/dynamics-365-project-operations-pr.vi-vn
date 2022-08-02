---
title: Giai đoạn dự án
description: Bài viết này cung cấp thông tin về các giai đoạn của dự án có sẵn trong Microsoft Dynamics Hoạt động Dự án.
author: ruhercul
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: a8c8e63a2d8c238f582b67348f88b7285a0b1e12
ms.sourcegitcommit: 278740b352f1ed9618ee5c79597c8f449984d6f4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 07/19/2022
ms.locfileid: "9177406"
---
# <a name="project-stages"></a>Giai đoạn dự án

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Giai đoạn dự án được thiết kế để phản ánh trạng thái của dự án khi dự án tiến triển. Hệ thống có thể sử dụng các tùy chỉnh để tự động cập nhật các dòng quy trình công việc, Power Automate hoặc tiện ích phần bổ trợ.

Các giai đoạn sau được xác định trong dòng quy trình công việc mặc định:

- Mới
- Báo giá
- Gói
- Chuyển giao
- Hoàn tất
- Đóng 

## <a name="new"></a>Mới

Khi bạn tạo một dự án, giai đoạn dự án sẽ được đặt thành **Mới**. Nếu dự án được tạo ra từ một mẫu, dự án đó có thể có lịch trình, ước tính và nhóm dữ liệu. Nếu không, đó sẽ là một bản phác thảo của dự án và các thành phần còn lại phải được nhập vào.

## <a name="quote"></a>Báo giá

Khi bạn liên kết một dự án với một báo giá hoặc tạo một dự án từ báo giá, giai đoạn dự án được đặt thành **Báo giá** và ngày bắt đầu và ngày kết thúc ước tính được cập nhật. Khi dự án trong giai đoạn **Báo giá**, tab **Bán hàng** trên trang **Thực thể dự án** hiển thị thông tin chi tiết về báo giá.

## <a name="plan"></a>Kế hoạch

Khi bạn thắng báo giá liên kết với dự án, dự án được chuyển đến giai đoạn **Hợp đồng**, giai đoạn dự án được cập nhật thành **Kế hoạch**. Trong khi dự án đang ở **Kế hoạch** sân khấu, **Việc bán hàng** tab trên **Thực thể dự án** trang hiển thị chi tiết của hợp đồng.

## <a name="deliver"></a>Chuyển giao

Khi kế hoạch dự án hoàn tất và bạn đã sẵn sàng để bắt đầu dự án, người quản lý dự án nên cập nhật giai đoạn dự án thành **Chuyển giao** để cho biết dự án đã bắt đầu.

## <a name="complete"></a>Hoàn thành 

Khi công việc cho dự án được hoàn thành, người quản lý dự án có thể cập nhật giai đoạn thành **Hoàn thành**. Bằng cách cập nhật giai đoạn dự án thành **Hoàn thành**, người quản lý dự án chỉ ra rằng công việc được hoàn thành 100% nhưng dự án được giữ ở trạng thái mở để mọi mục nhập thời gian hoặc chi phí đang chờ xử lý có thể được ghi lại.

## <a name="close"></a>Đóng

Khi tất cả giao dịch được ghi lại cho dự án, người quản lý dự án có thể cập nhật giai đoạn thành **Đóng**. Tại thời điểm đó, không thể ghi lại giao dịch nào và dự án được đặt thành chế độ chỉ đọc.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
