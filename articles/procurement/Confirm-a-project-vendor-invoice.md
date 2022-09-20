---
title: Xác nhận hóa đơn của nhà cung cấp dự án
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
# <a name="confirm-project-vendor-invoices"></a>Xác nhận hóa đơn của nhà cung cấp dự án

_ **Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho

Khi mà **Cần xác nhận thủ công bởi PM** tham số được bật, hóa đơn của nhà cung cấp được tạo trong Microsoft Dataverse có **Bản thảo** trạng thái. Hóa đơn của nhà cung cấp được tạo theo cách này phải được xem xét và xác nhận theo cách thủ công. Khi mà **Cần xác nhận thủ công bởi PM** tham số bị vô hiệu hóa, hóa đơn của nhà cung cấp được tạo trong Dataverse được xác nhận tự động. Không có thêm hành động được yêu cầu. 

Sau khi bạn đã xác minh tất cả các dòng trên hóa đơn của nhà cung cấp trong Dynamics 365 Project Operations, lựa chọn **Xác nhận** để xác nhận hóa đơn của nhà cung cấp.

Khi bạn chọn **Xác nhận** trên hóa đơn của nhà cung cấp, hành vi sau xảy ra:

1. Trạng thái của hóa đơn nhà cung cấp được cập nhật thành **Đã xác nhận**.
1. Hóa đơn của nhà cung cấp đã xác nhận và các bản ghi liên quan của nó trở thành ở chế độ chỉ đọc và không thể chỉnh sửa hoặc xóa.
1. Nếu bất kỳ thực hành chi phí nào tham chiếu đến dòng hóa đơn của nhà cung cấp như một phần của quy trình đối sánh, tất cả các thực tế về chi phí được liên kết với dòng hóa đơn của nhà cung cấp được tham chiếu sẽ bị đảo ngược.
1. Thực tế chi phí mới được tạo bằng cách sử dụng thông tin trên dòng hóa đơn của nhà cung cấp.
1. Bạn không còn có thể tạo nhật ký sửa chữa, ghi lại quy trình các mục thời gian, hoặc hủy bỏ việc phê duyệt các thủ tục thời gian, chi phí hoặc vật chất ban đầu đã bị đảo ngược.
1. Trong Dynamics 365 Finance, **Chi phí dự án** giá trị được cập nhật bằng cách sử dụng tạp chí Tích hợp dự án và tài khoản tích hợp Mua sắm là *đảo ngược* sau khi tạp chí tích hợp Dự án được đăng.

> [!NOTE]
> Nếu bất kỳ dòng nào trên hóa đơn của nhà cung cấp có trạng thái xác minh khác với **Hoàn thành**, không thể xác nhận hóa đơn của nhà cung cấp.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
