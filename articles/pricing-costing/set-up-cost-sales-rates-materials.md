---
title: Thiết lập chi phí và tỷ lệ doanh số cho vật tư
description: Chủ đề này cung cấp thông tin về cách thiết lập chi phí và tỷ lệ doanh số cho vật tư được dùng cho các dự án.
author: rumant
ms.date: 03/21/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 1b1b679f15662d922804deefb6372adcdf4d4839
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576894"
---
# <a name="set-up-cost-and-sales-rates-for-materials"></a>Thiết lập chi phí và tỷ lệ doanh số cho vật tư

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Bạn có thể thiết lập chi phí và giá bán cho sản phẩm trong Dynamics 365 Project Operations. Giá vốn và giá bán cho sản phẩm chỉ có thể được liệt kê bằng một đơn vị tiền tệ. Đơn vị tiền tệ này phải là đơn vị tiền tệ trên tiêu đề bảng giá.

Để thiết lập chi phí và tỷ lệ doanh số cho sản phẩm, hãy hoàn thành các bước sau. 

1. Đi đến **Bán hàng** > **Khách hàng** > **Bảng giá** rồi chọn **Mới** để tạo một bảng giá mới. 
2. Trên **Các hạng mục trong bảng giá**, trong menu lưới phụ, hãy chọn **Hạng mục trong bảng giá mới**. 
3. Trên trang **Tạo nhanh**, hãy nhập sản phẩm và đơn vị mà bạn đang tạo giá mới.

Để biết thêm thông tin về cách xác định giá cho các mục trong danh mục, hãy xem [Xác định giá sản phẩm bằng bảng giá và các mục trong bảng giá](/dynamics365/sales/create-price-lists-price-list-items-define-pricing-products) và [Độ chính xác thập phân về đơn vị tiền tệ và giá cả](/dynamics365/sales/decimal-precision-currency-pricing).
> [!NOTE]
> Dynamics 365 Project Operations không hỗ trợ tất cả các phương pháp định giá cho các sản phẩm với tư cách là Bán hàng Dynamics 365. Phương pháp định giá duy nhất được hỗ trợ cho các sản phẩm được sử dụng trong các dự án là *Lượng ngoại tệ*.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
