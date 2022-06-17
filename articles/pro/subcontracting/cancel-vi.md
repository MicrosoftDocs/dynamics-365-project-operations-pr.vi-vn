---
title: Hủy hóa đơn của nhà cung cấp trong dự án
description: Bài viết này giải thích cách hủy hóa đơn của nhà cung cấp dự án trong Microsoft Dynamics 365 Project Operations và tác động tài chính của việc hủy hóa đơn của nhà cung cấp dự án.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7ddaadc0f6e336a8ba67bb4ad8000f7e894f3eb0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911576"
---
# <a name="cancel-a-project-vendor-invoice"></a>Hủy hóa đơn của nhà cung cấp trong dự án

[!include [banner](../../includes/dataverse-preview.md)]

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Sau khi xác nhận hóa đơn của nhà cung cấp, bạn không thể chỉnh sửa hoặc xóa hóa đơn đó. Nếu có lỗi trên hóa đơn nhà cung cấp đã được xác nhận, bạn có thể sử dụng hành động Hủy để đảo ngược tác động của hóa đơn nhà cung cấp và tạo hóa đơn nhà cung cấp mới.

Khi bạn chọn **Hủy bỏ** trên hóa đơn của nhà cung cấp, hành vi sau đây xảy ra:

1. Trạng thái của hóa đơn nhà cung cấp được cập nhật thành **Đã hủy**.
2. Hóa đơn của nhà cung cấp đã hủy và các bản ghi liên quan của nó trở thành chỉ đọc và không thể chỉnh sửa hoặc xóa.
3. Bất kỳ thực tế chi phí nào được tạo dựa trên các dòng hóa đơn của nhà cung cấp như một phần của xác nhận hóa đơn của nhà cung cấp đều bị hủy bỏ.
4. Nếu bất kỳ thực tế chi phí nào được liên kết với các dòng hóa đơn của nhà cung cấp như một phần của quy trình đối sánh, thì xác nhận hóa đơn ban đầu của nhà cung cấp đã đảo ngược chúng. Trong quá trình hủy hóa đơn của nhà cung cấp, các chỉ số chi phí đó sẽ được tạo lại. Nguồn gốc chỉ ra các mục sử dụng thời gian, chi phí hoặc nguyên vật liệu.
5. Sau khi hóa đơn của nhà cung cấp bị hủy, một lần nữa bạn có thể tạo nhật ký sửa chữa, thu hồi mục nhập thời gian xử lý và hủy bỏ phê duyệt về thời gian, chi phí hoặc thực tế vật liệu ban đầu.

> [!NOTE]
> Chỉ có thể hủy bỏ các hóa đơn của nhà cung cấp dự án đã được xác nhận. Không thể hủy hóa đơn của nhà cung cấp ở các tiểu bang khác.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
