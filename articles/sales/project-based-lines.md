---
title: Mô tả cơ hội dựa trên dự án
description: Chủ đề này cung cấp thông tin về cách làm việc với mô tả cơ hội dựa trên dự án.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0ede474e3d8830b420dc5b183f14327206c10288
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181973"
---
# <a name="project-based-opportunity-lines"></a>Mô tả cơ hội dựa trên dự án

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_


Mô tả cơ hội dựa trên dự án chỉ có sẵn trong các cơ hội dựa trên dự án. Bản ghi cơ hội dựa trên dự án có giá trị trường **Loại** được đặt thành **Dựa trên công việc**.

Mô tả cơ hội dựa trên dự án là các mục mô tả sẽ được phân phối cho khách hàng bằng cách sử dụng một dự án. Tuy nhiên, dự án không thể bị ràng buộc với mô tả cơ hội dựa trên dự án. Các dự án có thể được liên kết với mục mô tả từ giai đoạn **Báo giá** trở đi vì cơ hội thường xảy ra trong giai đoạn đầu của một giao dịch. Việc xác định có bao nhiêu dự án sẽ được sử dụng để giao công việc cho khách hàng là một quyết định được đưa ra sau đó trong giai đoạn bán hàng. Sử dụng giai đoạn cơ hội để xác định các thành phần phân phối riêng biệt cho khách hàng. Các quyết định xoay quanh số lượng dự án thực tế được sử dụng để cung cấp các thành phần này có thể bị gạt ra cho đến khi có thêm thông tin về chính công việc đó.

Dưới đây là các trường trên mô tả cơ hội dựa trên dự án:

| **Trường** | **Vị trí** | **Mô tả** | **Tác động xuôi tuyến** |
| --- | --- | --- | --- |
| Loại Sản phẩm | Tab tổng quát (ẩn) | Đây là trường bộ tùy chọn. Nếu bạn đã cài đặt Dynamics 365 Operations, một trong những tùy chọn khả dụng là **Dịch vụ dựa trên dự án**.  | Giá trị của trường này được đặt thành **Dịch vụ dựa trên dự án** khi bạn tạo mô tả cơ hội dựa trên dự án từ lưới mô tả dựa trên dự án trên mục Cơ hội. <br> Nếu bạn thay đổi hoặc ghi đè giá trị này, chức năng dự án sẽ không được bật trên các mục mô tả dựa trên dự án của bạn. |
| Cơ hội | Tab tổng quát | Trường này ở chế độ chỉ đọc và tham chiếu đến bản ghi Cơ hội chính có chứa mục mô tả này. | Không có tác động xuôi tuyến của trường này. |
| Tên | Tab tổng quát | Đây là trường văn bản có thể chỉnh sửa dùng để cung cấp thông tin nhận dạng ngắn gọn cho mục mô tả này | Giá trị này được đưa sang mô tả báo giá khi bạn tạo báo giá từ cơ hội này |
| Ngân sách Khách hàng | Tab tổng quát | Trường đơn vị tiền tệ có thể chỉnh sửa này dùng để theo dõi số tiền mà khách hàng sẵn sàng chi cho mục mô tả này. | Giá trị này được đưa sang trường tương ứng trên mô tả báo giá khi bạn tạo báo giá từ cơ hội này |
| Phương thức Thanh toán | Tab tổng quát | Trường có thể chỉnh sửa này có các giá trị sau đây:</br>- Thời gian và vật tư</br>- Giá cố định | Giá trị này được đưa sang trường tương ứng trên mô tả báo giá khi bạn tạo báo giá từ cơ hội này. Sau khi mô tả báo giá được tạo, trường bị khóa và không thay đổi được. Gán giá trị trường này càng chính xác càng tốt. Nếu bạn cần thay đổi giá trị của trường này trên mô tả báo giá, hãy xóa và tạo lại mô tả báo giá. |
