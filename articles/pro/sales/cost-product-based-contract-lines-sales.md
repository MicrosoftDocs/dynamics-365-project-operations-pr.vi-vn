---
title: Mô tả hợp đồng dựa trên sản phẩm chi phí
description: Chủ đề này cung cấp thông tin về việc tạo
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7dfb9425174dddee52f9ee64f7a963e48a6bca70
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/20/2020
ms.locfileid: "4087339"
---
# <a name="costing-product-based-contract-lines"></a>Mô tả hợp đồng dựa trên sản phẩm chi phí

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_


Các mục mô tả hợp đồng dựa trên sản phẩm trong Dynamics 365 Project Operations có trường **Giá vốn** , đây là trường lưu trữ giá vốn của sản phẩm để tính toán lợi nhuận xuôi tuyến.

Khi mục mô tả hợp đồng dựa trên sản phẩm được tạo cho một sản phẩm trong danh mục, chi phí của mục mô tả hợp đồng dựa trên sản phẩm đó được lấy mặc định từ trường **Chi phí tiêu chuẩn** trong danh mục sản phẩm. Trường **Chi phí tiêu chuẩn** trong danh mục sản phẩm được thiết lập theo đơn vị tiền tệ cơ sở của tổ chức. Khi chi phí đơn vị được lấy mặc định trên mục mô tả hợp đồng, giá trị này được chuyển đổi theo đơn vị tiền tệ bán hàng trên hợp đồng.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Chi phí đơn vị trên mục mô tả hợp đồng dựa trên sản phẩm

Khi có chi phí đơn vị trên mục mô tả hợp đồng dựa trên sản phẩm, mỗi lần bán đơn vị sẽ có một mục chi phí sản phẩm khác nhau. Tuy điều này không phải lúc nào cũng cần thiết, nhưng vẫn có một số trường hợp nhất định mà nhà cung cấp có thể chiết khấu chi phí sản phẩm cho khách hàng. Xem xét kịch bản ví dụ sau đây:

Fabrikam Robotics lắp đặt các cánh tay rô-bốt tại dây chuyền lắp ráp của Adatum Corporation. Fabrikam cung cấp dịch vụ lắp đặt nhưng các cánh tay rô-bốt được mua từ Trey Research. Nếu việc lắp đặt cánh tay rô-bốt tại Adatum Corporation mở ra một ngành mới cho Trey Research, thì công ty này có thể áp dụng chiết khấu đặc biệt cho thỏa thuận này với Fabrikam. Trong trường hợp này, Fabrikam tạo một mục mo tả hợp đồng dựa trên sản phẩm cho Robotic Arms và nhập chi phí trên đơn vị cho hợp đồng này khác với chi phí tiêu chuẩn cho cánh tay rô-bốt của Trey Research.
