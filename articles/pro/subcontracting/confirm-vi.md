---
title: Xác nhận hóa đơn của nhà cung cấp trong dự án
description: Bài viết này giải thích cách xác nhận hóa đơn của nhà cung cấp dự án trong Microsoft Dynamics 365 Project Operations và tác động tài chính của việc xác nhận hóa đơn của nhà cung cấp dự án.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 092b3cd5981f7d9bb8767c7a2acb2f4952801d06
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932460"
---
# <a name="confirm-a-project-vendor-invoice"></a>Xác nhận hóa đơn của nhà cung cấp trong dự án

[!include [banner](../../includes/dataverse-preview.md)]

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Sau khi bạn đã xác minh tất cả các dòng trên hóa đơn của nhà cung cấp trong Microsoft Dynamics 365 Project Operations, bạn có thể sử dụng hành động Xác nhận để xác nhận hóa đơn của nhà cung cấp.

Khi bạn chọn **Xác nhận** trên hóa đơn của nhà cung cấp, hành vi sau xảy ra:

1. Trạng thái của hóa đơn nhà cung cấp được cập nhật thành **Đã xác nhận**.
2. Hóa đơn của nhà cung cấp đã xác nhận và các bản ghi liên quan của nó trở thành chỉ đọc và không thể chỉnh sửa hoặc xóa.
3. Nếu bất kỳ thực hành chi phí nào tham chiếu đến dòng hóa đơn của nhà cung cấp như một phần của quy trình đối sánh, thì tất cả các thực tế về chi phí được liên kết với dòng hóa đơn của nhà cung cấp được tham chiếu sẽ bị đảo ngược.
4. Thực tế chi phí mới được tạo bằng cách sử dụng thông tin trên dòng hóa đơn của nhà cung cấp.
5. Sau khi hóa đơn của nhà cung cấp được xác nhận, bạn không còn có thể tạo nhật ký sửa chữa, thu hồi mục nhập thời gian xử lý hoặc hủy phê duyệt về thời gian, chi phí hoặc các thủ tục vật chất ban đầu đã được đảo ngược.

> [!NOTE]
> Nếu bất kỳ dòng nào trên hóa đơn của nhà cung cấp có trạng thái xác minh khác với **Hoàn thành**, không thể xác nhận hóa đơn của nhà cung cấp.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
