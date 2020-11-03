---
title: Ước tính nguồn lực
description: Chủ đề này cung cấp thông tin về cách tính ước tính nguồn lực trong Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2ebde2b3c5bcfb5faa02ee476065ac34b1953432
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087028"
---
# <a name="resource-estimates"></a>Ước tính nguồn lực

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Ước tính nguồn lực đến từ nhân công theo từng giai đoạn thời gian được xác định trong cấu trúc phân tích công việc cùng với các thứ nguyên giá áp dụng. Thông thường, phép tính là **tốc độ/giờ cho mỗi vai trò x giờ.** Nhân công theo giai đoạn thời gian cho mỗi nguồn lực được lưu trữ trong bản ghi gán nguồn lực. Giá được lưu trữ trong một bảng giá được xác định trước. Quy đổi đơn vị được áp dụng dựa trên bảng giá áp dụng.

![Ước tính nguồn lực](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Loại tiền tệ chi phí và giá vốn mặc định

Giá vốn được mặc định từ Đơn vị tổ chức.

## <a name="default-bill-rate-and-sales-currency"></a>Loại tiền tệ bán hàng và tỷ lệ thanh toán mặc định

Giá bán hàng được áp dụng một lần cho mỗi thỏa thuận. Hệ thống cấp bậc cho bảng giá ưu đãi mặc định như sau:

1. Tổ chức
2. Khách hàng
3. Báo giá/hợp đồng
