---
title: Thiết lập chi phí và tỷ lệ bán hàng cho sản phẩm trên danh mục – bản đơn giản
description: Chủ đề này cung cấp thông tin về cách thiết lập chi phí và tỷ lệ bán hàng cho các mặt hàng trong danh mục sản phẩm.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5e851193df8151821e112e01a9f33df5afee7df7
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764592"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Thiết lập chi phí và tỷ lệ bán hàng cho sản phẩm trên danh mục – bản đơn giản

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_


Cách thiết lập giá cho các mục thuộc danh mục sản phẩm trong Dynamics 365 Project Operations cũng giống như trong Dynamics 365 Sales.

Trong Project Operations, bạn không thể ước tính hoặc sử dụng sản phẩm trên dự án, nên không cần thiết lập giá của danh mục sản phẩm trên bảng giá dự án đối với báo giá và hợp đồng.

Sử dụng trường **Giá sản phẩm** của một báo giá, hợp đồng hoặc tài khoản để thiết lập giá của danh mục sản phẩm. Không nên thiết lập giá của danh mục sản phẩm trong bảng giá dự án. Bảng giá dự án dành riêng cho Project Operations. Logic kinh doanh dành riêng cho ứng dụng sẽ sao chép bảng giá từ báo giá sang hợp đồng. Kết quả là bảng giá dự án theo hợp đồng. Thao tác sao chép có thể trì hoãn quá trình nhận được báo giá nếu bảng giá dự án trên báo giá quá lớn. Bảng giá sản phẩm không được sao chép để tạo bảng giá tùy chỉnh trên hợp đồng. Do không có hoạt động sao chép nào liên quan, nên hiệu quả của quy trình báo giá không bị ảnh hưởng.
