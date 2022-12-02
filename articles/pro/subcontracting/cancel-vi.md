---
title: Hủy hóa đơn của nhà cung cấp trong dự án
description: Bài viết này giải thích cách hủy hóa đơn của nhà cung cấp dự án trong Microsoft Dynamics 365 Project Operations và tác động tài chính của việc hủy hóa đơn của nhà cung cấp dự án.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 79d00a91f9ab2d66eab2f80349d6f1fba1934f94
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261117"
---
# <a name="cancel-a-project-vendor-invoice"></a>Hủy hóa đơn của nhà cung cấp trong dự án

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Sau khi hóa đơn của nhà cung cấp được xác nhận, nó không thể được chỉnh sửa hoặc xóa. Nếu có lỗi trên hóa đơn nhà cung cấp đã được xác nhận, bạn có thể sử dụng hành động Hủy để đảo ngược tác động của hóa đơn nhà cung cấp và tạo hóa đơn nhà cung cấp mới.

Khi bạn chọn **Hủy** trên hóa đơn của nhà cung cấp, hành vi sau đây xảy ra:

1. Trạng thái của hóa đơn nhà cung cấp được cập nhật thành **Đã hủy**.
2. Hóa đơn của nhà cung cấp đã hủy và các bản ghi liên quan của nó trở thành chỉ đọc và không thể chỉnh sửa hoặc xóa.
3. Bất kỳ chi phí thực tế nào đã được tạo dựa trên các mô tả hóa đơn của nhà cung cấp như một phần của xác nhận hóa đơn nhà cung cấp đều bị hủy bỏ.
4. Nếu bất kỳ chi phí thực tế nào được liên kết với các mô tả hóa đơn của nhà cung cấp như một phần của quy trình đối sánh, thì xác nhận hóa đơn nhà cung cấp ban đầu đã đảo ngược chúng. Trong quá trình hủy hóa đơn của nhà cung cấp, các chi phí thực tế được tạo lại. Nguồn gốc chỉ ra các mục sử dụng thời gian, chi phí hoặc vật tư.
5. Sau khi hóa đơn của nhà cung cấp bị hủy, một lần nữa bạn có thể tạo nhật ký chỉnh sửa, thu hồi mục nhập thời gian xử lý và hủy phê duyệt về thời gian, chi phí hoặc vật tư thực tế ban đầu.

> [!NOTE]
> Chỉ có thể hủy các hóa đơn của nhà cung cấp dự án được xác nhận. Không thể hủy hóa đơn nhà cung cấp ở các trạng thái khác.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
