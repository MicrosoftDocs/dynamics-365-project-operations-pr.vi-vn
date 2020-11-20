---
title: Mô tả hợp đồng dựa trên chi phí sản phẩm - bản đơn giản
description: Chủ đề này cung cấp thông tin về việc tạo
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0e961bcf32a5dd662b7cd27a23eb5f664c45c292
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177268"
---
# <a name="cost-product-based-contract-lines---lite"></a>Mô tả hợp đồng dựa trên chi phí sản phẩm - bản đơn giản

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_


Các mục mô tả hợp đồng dựa trên sản phẩm trong Dynamics 365 Project Operations có trường **Giá vốn**, đây là trường lưu trữ giá vốn của sản phẩm để tính toán lợi nhuận xuôi tuyến.

Khi mục mô tả hợp đồng dựa trên sản phẩm được tạo cho một sản phẩm trong danh mục, chi phí của mục mô tả hợp đồng dựa trên sản phẩm đó được lấy mặc định từ trường **Chi phí tiêu chuẩn** trong danh mục sản phẩm. Trường **Chi phí tiêu chuẩn** trong danh mục sản phẩm được thiết lập theo đơn vị tiền tệ cơ sở của tổ chức. Khi chi phí đơn vị được lấy mặc định trên mục mô tả hợp đồng, giá trị này được chuyển đổi theo đơn vị tiền tệ bán hàng trên hợp đồng.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Chi phí đơn vị trên mục mô tả hợp đồng dựa trên sản phẩm

Khi có chi phí đơn vị trên mục mô tả hợp đồng dựa trên sản phẩm, mỗi lần bán đơn vị sẽ có một mục chi phí sản phẩm khác nhau. Tuy điều này không phải lúc nào cũng cần thiết, nhưng vẫn có một số trường hợp nhất định mà nhà cung cấp có thể chiết khấu chi phí sản phẩm cho khách hàng. Xem xét kịch bản ví dụ sau đây:

Fabrikam Robotics lắp đặt các cánh tay rô-bốt tại dây chuyền lắp ráp của Adatum Corporation. Fabrikam cung cấp dịch vụ lắp đặt nhưng các cánh tay rô-bốt được mua từ Trey Research. Nếu việc lắp đặt cánh tay rô-bốt tại Adatum Corporation mở ra một ngành mới cho Trey Research, thì công ty này có thể áp dụng chiết khấu đặc biệt cho thỏa thuận này với Fabrikam. Trong trường hợp này, Fabrikam tạo một mục mo tả hợp đồng dựa trên sản phẩm cho Robotic Arms và nhập chi phí trên đơn vị cho hợp đồng này khác với chi phí tiêu chuẩn cho cánh tay rô-bốt của Trey Research.
