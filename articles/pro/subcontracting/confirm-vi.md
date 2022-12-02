---
title: Xác nhận hóa đơn của nhà cung cấp trong dự án
description: Bài viết này giải thích cách xác nhận hóa đơn của nhà cung cấp dự án trong Microsoft Dynamics 365 Project Operations và tác động tài chính của việc xác nhận hóa đơn của nhà cung cấp dự án.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4dafbe64e0727957068d68f510202a12871b62aa
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261539"
---
# <a name="confirm-a-project-vendor-invoice"></a>Xác nhận hóa đơn của nhà cung cấp trong dự án

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Sau khi bạn đã xác minh tất cả các dòng trên hóa đơn của nhà cung cấp trong Microsoft Dynamics 365 Project Operations, bạn có thể sử dụng hành động Xác nhận để xác nhận hóa đơn của nhà cung cấp.

Khi bạn chọn **Xác nhận** trên hóa đơn của nhà cung cấp, hành vi sau đây xảy ra:

1. Trạng thái của hóa đơn nhà cung cấp được cập nhật thành **Đã xác nhận**.
2. Hóa đơn của nhà cung cấp đã xác nhận và các bản ghi liên quan của nó trở thành chỉ đọc và không thể chỉnh sửa hoặc xóa.
3. Nếu bất kỳ chi phí thực tế nào tham chiếu đến mô tả hóa đơn của nhà cung cấp như một phần của quá trình khớp, tất cả các chi phí thực tế được liên kết với mô tả hóa đơn của nhà cung cấp đã tham chiếu sẽ được đảo ngược.
4. Chi phí thực tế mới được tạo bằng cách sử dụng thông tin trên mô tả hóa đơn của nhà cung cấp.
5. Sau khi hóa đơn của nhà cung cấp được xác nhận, bạn không thể tạo nhật ký chỉnh sửa, xử lý thu hồi mục nhập thời gian hoặc hủy phê duyệt về thời gian, chi phí hoặc vật tư thực tế ban đầu đã được đảo ngược.

> [!NOTE]
> Nếu bất kỳ mô tả nào trên hóa đơn của nhà cung cấp có trạng thái xác minh không phải là **Hoàn thành**, hóa đơn của nhà cung cấp không thể được xác nhận.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
