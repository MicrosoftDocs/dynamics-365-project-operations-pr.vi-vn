---
title: Thiết lập chi phí và tỷ lệ doanh số cho vật tư
description: Bài viết này cung cấp thông tin về cách thiết lập chi phí và tỷ lệ doanh số cho vật tư được dùng cho các dự án.
author: rumant
ms.date: 03/21/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0a7d84c2dcaa228e06add2f3cb06a530b29e0e35
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911806"
---
# <a name="set-up-cost-and-sales-rates-for-materials"></a>Thiết lập chi phí và tỷ lệ doanh số cho vật tư

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Bạn có thể thiết lập chi phí và giá bán cho sản phẩm trong Dynamics 365 Project Operations. Giá vốn và giá bán cho sản phẩm chỉ có thể được liệt kê bằng một đơn vị tiền tệ. Đơn vị tiền tệ này phải là đơn vị tiền tệ trên tiêu đề bảng giá.

Để thiết lập chi phí và tỷ lệ doanh số cho sản phẩm, hãy hoàn thành các bước sau. 

1. Đi đến **Bán hàng** > **Khách hàng** > **Bảng giá** rồi chọn **Mới** để tạo một bảng giá mới. 
2. Trên **Các hạng mục trong bảng giá**, trong menu lưới phụ, hãy chọn **Hạng mục trong bảng giá mới**. 
3. Trên trang **Tạo nhanh**, hãy nhập sản phẩm và đơn vị mà bạn đang tạo giá mới.

Để biết thêm thông tin về cách xác định giá cho các mục trong danh mục, hãy xem [Định giá sản phẩm bằng bảng giá và mục bảng giá](/dynamics365/sales/create-price-lists-price-list-items-define-pricing-products) và [Độ chính xác thập phân trong đơn vị tiền tệ và giá](/dynamics365/sales/decimal-precision-currency-pricing).
> [!NOTE]
> Dynamics 365 Project Operations không hỗ trợ tất cả các phương pháp định giá cho các sản phẩm dưới dạng Dynamics 365 Sales. Phương pháp định giá duy nhất được hỗ trợ cho các sản phẩm được sử dụng trong các dự án là *Số tiền theo loại tiền*.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
