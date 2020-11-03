---
title: Thiết lập chi phí và tỷ lệ bán hàng cho các sản phẩm danh mục
description: Chủ đề này cung cấp thông tin về cách thiết lập chi phí và tỷ lệ bán hàng cho các mặt hàng trong danh mục sản phẩm.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5178a9143536bf4b2573403125325017861cdd5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087175"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products"></a>Thiết lập chi phí và tỷ lệ bán hàng cho các sản phẩm danh mục

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_


Thiết lập giá cho các mặt hàng trong danh mục sản phẩm trong Dynamics 365 Project Operations giống như trong Dynamics 365 Sales.

Vì không thể ước tính hoặc sử dụng sản phẩm cho các dự án trong Project Operations, nên không cần đặt giá danh mục sản phẩm trên bảng giá dự án cho báo giá và hợp đồng.

Giá danh mục sản phẩm nên được thiết lập trong trường **Giá sản phẩm** của báo giá, hợp đồng hoặc tài khoản. Không thiết lập giá danh mục sản phẩm trong bảng giá dự án cho những thực thể này. Bảng giá dự án dành riêng cho Project Operations. Có logic nghiệp vụ dành riêng cho ứng dụng sao chép bảng giá từ báo giá sang hợp đồng. Kết quả là bảng giá dự án theo hợp đồng. Thao tác sao chép có thể trì hoãn quá trình nhận được báo giá nếu bảng giá dự án trên báo giá quá lớn. Bảng giá sản phẩm không được sao chép để tạo bảng giá tùy chỉnh trên hợp đồng. Điều này có nghĩa là bảng giá sản phẩm không ảnh hưởng đến hiệu suất của quá trình nhận được báo giá.
