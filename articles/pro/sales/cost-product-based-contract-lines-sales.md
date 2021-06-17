---
title: Mô tả hợp đồng dựa trên chi phí sản phẩm - bản đơn giản
description: Chủ đề này cung cấp thông tin về việc tạo
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9458a57863244a68359f57185325c03a46bd6569
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003567"
---
# <a name="cost-product-based-contract-lines---lite"></a>Mô tả hợp đồng dựa trên chi phí sản phẩm - bản đơn giản

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_


Mô tả hợp đồng dựa trên dự án trong Dynamics 365 Project Operations bao gồm trường **Giá vốn**, trường này chỉ giá vốn của sản phẩm để tính toán lợi nhuận xuôi dòng.

Khi mục mô tả hợp đồng dựa trên sản phẩm được tạo cho một sản phẩm trong danh mục, chi phí trong mô tả mặc định từ trường **Chi phí tiêu chuẩn** trong danh mục sản phẩm. Trường **Chi phí tiêu chuẩn** trong danh mục sản phẩm được thiết lập theo đơn vị tiền tệ cơ sở của tổ chức. Khi chi phí đơn vị được lấy mặc định trên mục mô tả hợp đồng, giá trị này được chuyển đổi theo đơn vị tiền tệ bán hàng trên hợp đồng.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Chi phí đơn vị trên mục mô tả hợp đồng dựa trên sản phẩm

Khi có chi phí đơn vị trên mục mô tả hợp đồng dựa trên sản phẩm, mỗi lần bán đơn vị sẽ có một mục chi phí sản phẩm khác nhau. Tuy điều này không phải lúc nào cũng cần thiết, nhưng vẫn có một số trường hợp nhất định mà nhà cung cấp có thể chiết khấu chi phí sản phẩm cho khách hàng. Xem xét kịch bản ví dụ sau đây:

Fabrikam Robotics lắp đặt các cánh tay rô-bốt tại dây chuyền lắp ráp của Adatum Corporation. Tuy Fabrikam cung cấp dịch vụ lắp đặt nhưng cánh tay robot là sản phẩm của Trey Research. Nếu việc lắp đặt cánh tay rô-bốt tại Adatum Corporation mở ra một ngành mới cho Trey Research, thì công ty này có thể áp dụng chiết khấu đặc biệt cho thỏa thuận này với Fabrikam. Trong trường hợp này, Fabrikam tạo một mô tả hợp đồng dựa trên sản phẩm cho Robotic Arms. Chi phí trên đơn vị được nhập cho hợp đồng này. Chi phí này khác với chi phí của các cánh tay robot từ Trey Research.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]