---
title: Xem lại tồn đọng về vấn đề lập hóa đơn đối với các dự án và hợp đồng dự án
description: Chủ đề này cung cấp thông tin về cách xem lại các tồn đọng về thời gian, chi phí và sản phẩm, cũng như cách đánh dấu các mục này là sẵn sàng để lập hóa đơn.
author: rumant
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 51a7ecfefcc20544f5be378a347e3568285cafb3
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600584"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a>Xem lại tồn đọng về vấn đề lập hóa đơn đối với các dự án và hợp đồng dự án

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Khi một giao dịch sẵn sàng tạo và xử lý hóa đơn, thì giao dịch đó sẽ được đánh dấu là **Sẵn sàng lập hóa đơn**. Chủ đề này mô tả các loại giao dịch có thể được tạo.

## <a name="review-the-time-and-material-billing-backlog"></a>Xem lại tồn đọng về lập hóa đơn theo thời gian và tài liệu

Khi một mục nhập thời gian hoặc chi phí được gửi và phê duyệt cho một dự án, PSA sẽ tạo ra một dự án thực tế. Nếu tổ hợp dự án và lớp giao dịch phù hợp với một mô tả hợp đồng cho một dự án thời gian-và-tài liệu, thì hai số liệu thực sẽ được tạo ra khi mục nhập này được phê duyệt:

- Chi phí thực tế 
- Doanh số chưa lập hóa đơn thực tế

Doanh số chưa lập hóa đơn thực tế thể hiện tồn đọng lập hóa đơn, và trạng thái lập hóa đơn phải được đặt thành **Sẵn sàng lập hóa đơn**. Khi một hóa đơn dự án được tạo, doanh số thực tế chưa lập hóa đơn được đánh dấu là **Sẵn sàng lập hóa đơn** sẽ được sao chép thành chi tiết mô tả hóa đơn.

Để xem lại tồn đọng lập hóa đơn cho thời gian và tài liệu, hãy chuyển đến **Doanh số** \> **Lập hóa đơn** \> **Tồn đọng lập hóa đơn thời gian và tài liệu**. Chọn tất cả doanh số thực tế chưa lập hóa đơn đã sẵn sàng được lập hóa đơn rồi chọn **Sẵn sàng lập hóa đơn**. Trạng thái lập hóa đơn của các mục thực tế này được thay đổi thành **Sẵn sàng lập hóa đơn**.

![Tồn đọng Thanh toán Thời gian và Vật liệu.](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a>Đánh giá tồn đọng lập hóa đơn sản phẩm

Trong PSA, khi hợp đồng dự án có mô tả sản phẩm dựa trên hợp đồng, những nội dung mô tả đó được xem xét để lập hóa đơn bất cứ khi nào hóa đơn được tạo cho hợp đồng dự án. Mọi sản phẩm có mô tả hợp đồng được đánh dấu là **Sẵn sàng lập hóa đơn** sẽ được sao chép vào hóa đơn dự án dưới dạng mô tả hóa đơn dự án.

Để đánh giá tồn đọng lập hóa đơn cho sản phẩm, hãy chuyển đến **Doanh số** \> **Lập hóa đơn** \> **Tồn đọng lập hóa đơn sản phẩm**. Chọn tất cả mô tả hợp đồng dựa trên sản phẩm đã sẵn sàng được lập hóa đơn rồi chọn **Sẵn sàng lập hóa đơn**. Trạng thái lập hóa đơn của những nội dung mô tả này được thay đổi thành **Sẵn sàng lập hóa đơn**.

![Tồn đọng Thanh toán Sản phẩm.](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a>Đánh giá các mốc lập hóa đơn đối với hợp đồng cố định giá

Mỗi nội dung mô tả hợp đồng dự án có một phương thức lập hóa đơn giá cố định phải xác định các cột mốc hợp đồng. Những cột mốc hợp đồng này có thể được lập hóa đơn nếu chúng được đánh dấu là **Sẵn sàng lập hóa đơn**. 

Để xem lại các cột mốc lập hóa đơn, hãy chuyển đến **Doanh số** \> **Lập hóa đơn** \> **Mốc giá cố định**. Chọn tất cả doanh số thực tế chưa lập hóa đơn đã sẵn sàng được lập hóa đơn rồi chọn **Sẵn sàng lập hóa đơn**. Trạng thái lập hóa đơn của các mốc này được thay đổi thành **Sẵn sàng lập hóa đơn**.

![Mốc Giá Cố định.](media/FPBacklog.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
