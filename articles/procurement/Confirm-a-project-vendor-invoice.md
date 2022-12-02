---
title: Xác nhận các hóa đơn của nhà cung cấp trong dự án
description: Bài viết này giải thích cách xác nhận hóa đơn của nhà cung cấp dự án trong Microsoft Dynamics 365 Project Operations và mô tả tác động tài chính của việc xác nhận hóa đơn của nhà cung cấp dự án.
author: suvaidya
ms.date: 8/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 9739b15753aa34c51a0aa1e6dfeb7f590655ca7a
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475488"
---
# <a name="confirm-project-vendor-invoices"></a>Xác nhận các hóa đơn của nhà cung cấp trong dự án

_ **Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho

Khi tham số **Bắt buộc phải có xác nhận thủ công của PM** được bật, các hóa đơn nhà cung cấp được tạo trong Microsoft Dataverse đều có trạng thái **Bản nháp**. Hóa đơn của nhà cung cấp được tạo theo cách này phải được xem xét và xác nhận theo cách thủ công. Khi tham số **Bắt buộc phải có xác nhận thủ công của PM** được tắt, các hóa đơn nhà cung cấp được tạo trong Dataverse được xác nhận tự động. Không yêu cầu thêm hành động nào. 

Sau khi bạn đã xác minh tất cả các dòng trên hóa đơn của nhà cung cấp trong Dynamics 365 Project Operations, hãy chọn **Xác nhận** để xác nhận hóa đơn của nhà cung cấp.

Khi bạn chọn **Xác nhận** trên hóa đơn của nhà cung cấp, hành vi sau đây xảy ra:

1. Trạng thái của hóa đơn nhà cung cấp được cập nhật thành **Đã xác nhận**.
1. Hóa đơn của nhà cung cấp đã xác nhận và các bản ghi liên quan của nó trở thành chỉ đọc và không thể chỉnh sửa hoặc xóa.
1. Nếu bất kỳ chi phí thực tế nào tham chiếu đến mô tả hóa đơn của nhà cung cấp như một phần của quá trình khớp, tất cả các chi phí thực tế được liên kết với mô tả hóa đơn của nhà cung cấp đã tham chiếu sẽ được đảo ngược.
1. Chi phí thực tế mới được tạo bằng cách sử dụng thông tin trên mô tả hóa đơn của nhà cung cấp.
1. Bạn không thể tạo nhật ký chỉnh sửa, xử lý thu hồi mục nhập thời gian hoặc hủy phê duyệt về thời gian, chi phí hoặc vật tư thực tế ban đầu đã được đảo ngược.
1. Trong Dynamics 365 Finance, giá trị **Chi phí dự án** được cập nhật bằng cách sử dụng nhật ký Tích hợp dự án và Tài khoản tích hợp mua sắm được *đảo ngược* sau khi nhật ký Tích hợp dự án được đăng.

> [!NOTE]
> Nếu bất kỳ mô tả nào trên hóa đơn của nhà cung cấp có trạng thái xác minh không phải là **Hoàn thành**, hóa đơn của nhà cung cấp không thể được xác nhận.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
