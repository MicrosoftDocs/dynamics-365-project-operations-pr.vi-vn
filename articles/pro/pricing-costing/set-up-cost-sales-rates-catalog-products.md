---
title: Thiết lập chi phí và tỷ lệ bán hàng cho sản phẩm trên danh mục – bản đơn giản
description: Chủ đề này cung cấp thông tin về cách thiết lập chi phí và tỷ lệ bán hàng cho các mặt hàng trong danh mục sản phẩm.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 135b182af73bdab7a3520589431332ad059ec497
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176727"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Thiết lập chi phí và tỷ lệ bán hàng cho sản phẩm trên danh mục – bản đơn giản

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_


Thiết lập giá cho các mặt hàng trong danh mục sản phẩm trong Dynamics 365 Project Operations giống như trong Dynamics 365 Sales.

Vì không thể ước tính hoặc sử dụng sản phẩm cho các dự án trong Project Operations, nên không cần đặt giá danh mục sản phẩm trên bảng giá dự án cho báo giá và hợp đồng.

Giá danh mục sản phẩm nên được thiết lập trong trường **Giá sản phẩm** của báo giá, hợp đồng hoặc tài khoản. Không thiết lập giá danh mục sản phẩm trong bảng giá dự án cho những thực thể này. Bảng giá dự án dành riêng cho Project Operations. Có logic nghiệp vụ dành riêng cho ứng dụng sao chép bảng giá từ báo giá sang hợp đồng. Kết quả là bảng giá dự án theo hợp đồng. Thao tác sao chép có thể trì hoãn quá trình nhận được báo giá nếu bảng giá dự án trên báo giá quá lớn. Bảng giá sản phẩm không được sao chép để tạo bảng giá tùy chỉnh trên hợp đồng. Điều này có nghĩa là bảng giá sản phẩm không ảnh hưởng đến hiệu suất của quá trình nhận được báo giá.
