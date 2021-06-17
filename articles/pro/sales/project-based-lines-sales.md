---
title: Mô tả cơ hội dựa trên dự án - bản đơn giản
description: Chủ đề này cung cấp thông tin về mô tả cơ hội dựa trên dự án. (Dự án)
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 90b1b078d51c2842f6406c4455188a4433820a77
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994432"
---
# <a name="project-based-opportunity-lines---lite"></a>Mô tả cơ hội dựa trên dự án - bản đơn giản

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Mô tả cơ hội dựa trên dự án chỉ có sẵn trong các cơ hội dựa trên dự án. Bản ghi cơ hội dựa trên dự án có giá trị trường **Loại** được đặt thành **Dựa trên công việc**.

Mô tả cơ hội dựa trên dự án là các mục mô tả sẽ được phân phối cho khách hàng bằng cách sử dụng một dự án. Tuy nhiên, dự án không thể bị ràng buộc với mô tả cơ hội dựa trên dự án. Các dự án có thể được liên kết với mục mô tả từ giai đoạn **Báo giá** trở đi vì cơ hội thường nằm ở giai đoạn đầu của vòng đời hoặc thỏa thuận. Việc xác định có bao nhiêu dự án sẽ được sử dụng để giao công việc cho khách hàng là một quyết định được đưa ra sau đó trong giai đoạn bán hàng. Bạn có thể sử dụng giai đoạn cơ hội để xác định các thành phần phân phối riêng biệt cho khách hàng. Các quyết định xoay quanh số lượng dự án thực tế được sử dụng để cung cấp các thành phần này có thể bị gạt ra cho đến khi có thêm thông tin về chính công việc đó.

Dưới đây là các trường trên mô tả cơ hội dựa trên dự án:

| **Trường** | **Vị trí** | **Mô tả** | **Tác động xuôi tuyến** |
| --- | --- | --- | --- |
| Loại Sản phẩm | Tab tổng quát (ẩn) | Bạn có thể chọn một trong các tùy chọn sau:</br>- Dịch vụ dựa trên dự án (chỉ khả dụng khi Dynamics 365 Project Operations được cài đặt)</br>- Sản phẩm (chỉ khả dụng khi Project Operations và Dynamics 365 Sales được cài đặt) | Giá trị của trường này được đặt thành **Dịch vụ dựa trên dự án** khi bạn tạo mô tả cơ hội dựa trên dự án từ lưới mô tả dựa trên dự án trên mục Cơ hội. <br> Nếu bạn thay đổi hoặc ghi đè giá trị này, chức năng dự án sẽ không được bật trên các mục mô tả dựa trên dự án của bạn. |
| Cơ hội | Tab tổng quát | Trường này ở chế độ chỉ đọc và tham chiếu đến bản ghi Cơ hội chính có chứa mục mô tả này. | Không có tác động xuôi tuyến từ trường này. |
| Tên | Tab tổng quát | Đây là trường văn bản có thể chỉnh sửa dùng để cung cấp thông tin nhận dạng ngắn gọn cho mục mô tả này. | Giá trị này được đưa sang mô tả báo giá khi bạn tạo báo giá từ cơ hội này. |
| Ngân sách Khách hàng | Tab tổng quát | Trường đơn vị tiền tệ có thể chỉnh sửa này dùng để theo dõi số tiền mà khách hàng sẵn sàng chi cho mục mô tả này. | Giá trị này được đưa sang trường tương ứng trên mô tả báo giá khi bạn tạo báo giá từ cơ hội này. |
| Phương thức Thanh toán | Tab tổng quát | Trường có thể chỉnh sửa này có các giá trị sau đây:</br>- Thời gian và vật tư</br>- Giá cố định | Giá trị này được đưa sang trường tương ứng trên mô tả báo giá khi bạn tạo báo giá từ cơ hội này. Sau khi mô tả báo giá được tạo, trường bị khóa và không thay đổi được. Gán giá trị trường này càng chính xác càng tốt. Nếu bạn cần thay đổi giá trị của trường này trên mô tả báo giá, hãy xóa và tạo lại mô tả báo giá. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]