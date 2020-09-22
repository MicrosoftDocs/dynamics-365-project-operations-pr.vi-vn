---
title: Giai đoạn dự án
description: Chủ đề này cung cấp thông tin về các giai đoạn dự án.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 983c25a0-ed21-4151-a109-b385a88285fa
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 70aa057e127df7ba925e84f5d056a06a4cc8833e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 03/24/2020
ms.locfileid: "3757030"
---
# <a name="project-stages"></a>Giai đoạn dự án 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Giai đoạn dự án được cập nhật để phản ánh trạng thái của dự án khi dự án tiến triển. Dòng quy trình công việc mặc định tự động cập nhật một số giai đoạn của dự án trong khi các giai đoạn khác được người quản lý dự án cập nhật theo cách thủ công. 

Các giai đoạn sau được xác định trong BPF mặc định:

- Mới
- Báo giá
- Kế hoạch
- Chuyển giao
- Hoàn thành
- Đóng 

## <a name="new"></a>Mới

Khi bạn tạo một dự án, giai đoạn dự án sẽ được đặt thành **Mới**. Nếu dự án được tạo ra từ một mẫu, dự án đó có thể có lịch trình, ước tính và nhóm dữ liệu. Nếu không, nó chỉ là một bản phác thảo của dự án và các thành phần còn lại phải được nhập vào.

## <a name="quote"></a>Báo giá

Khi bạn liên kết một dự án với một báo giá hoặc tạo một dự án từ báo giá, giai đoạn dự án được đặt thành **Báo giá** và ngày bắt đầu và ngày kết thúc ước tính được cập nhật. Khi dự án trong giai đoạn **Báo giá**, tab **Bán hàng** trên trang **Thực thể dự án** hiển thị thông tin chi tiết về báo giá.

## <a name="plan"></a>Kế hoạch

Khi bạn thắng báo giá liên kết với dự án, dự án được chuyển đến giai đoạn **Hợp đồng**, giai đoạn dự án được cập nhật thành **Kế hoạch**. Khi dự án ở giai đoạn **Kế hoạch**, trang **Thực thể dự án** hiển thị thông tin chi tiết về hợp đồng.

## <a name="deliver"></a>Chuyển giao

Khi kế hoạch dự án hoàn tất và bạn đã sẵn sàng để bắt đầu dự án, người quản lý dự án nên cập nhật giai đoạn dự án thành **Chuyển giao** để cho biết dự án đã bắt đầu.

## <a name="complete"></a>Hoàn thành 

Khi công việc cho dự án được hoàn thành, người quản lý dự án có thể cập nhật giai đoạn thành **Hoàn thành**. Bằng cách cập nhật giai đoạn dự án thành **Hoàn thành**, người quản lý dự án chỉ ra rằng công việc được hoàn thành 100% nhưng dự án được giữ ở trạng thái mở để mọi mục nhập thời gian hoặc chi phí đang chờ xử lý có thể được ghi lại.

## <a name="close"></a>Đóng

Khi tất cả giao dịch được ghi lại cho dự án, người quản lý dự án có thể cập nhật giai đoạn thành **Đóng**. Tại thời điểm đó, không thể ghi lại giao dịch nào và dự án được đặt thành chế độ chỉ đọc.
