---
title: Tổng quan về các mô tả báo giá dựa trên sản phẩm - bản đơn giản
description: Chủ đề này cung cấp thông tin về cách làm việc với mô tả báo giá dựa trên sản phẩm.
author: rumant
manager: Annbe
ms.date: 10/30/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 29d82637c6c8bb5b5cde7707d181d5b3d3b235c4
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272594"
---
# <a name="product-based-quote-lines-overview---lite"></a>Tổng quan về các mô tả báo giá dựa trên sản phẩm - bản đơn giản

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Bạn có thể tạo mô tả báo giá dựa trên sản phẩm trong Dynamics 365 Project Operations. Các mô tả báo giá dựa trên sản phẩm có thể thêm được theo cách thủ công hoặc chúng có thể là các mục từ danh mục sản phẩm.

## <a name="product-catalog"></a>Danh mục sản phẩm

Mỗi sản phẩm trong danh mục sản phẩm đều có đơn vị mặc định và nhóm đơn vị đo. Nếu nhiều sản phẩm có cùng nhóm thuộc tính, bạn có thể tạo dòng sản phẩm cũng có các thuộc tính đó. 

Ví dụ: công ty bán các giấy phép gói đăng ký cho các loại phần mềm khác nhau. Tất cả phần mềm gói đăng ký có 2 thuộc tính sau:

- Số người dùng
- Khoảng thời gian đăng ký được tính theo tháng

Để duy trì loại danh mục này, hãy tạo dòng sản phẩm có tên **Phần mềm đăng ký** và thêm số người dùng cũng như khoảng thời gian đăng ký làm thuộc tính. Tiếp theo, bạn có thể thêm từng sản phẩm vào dòng sản phẩm **Phần mềm đăng ký**.

## <a name="add-product-catalog-items-to-a-project-quote"></a>Thêm các mục trong danh mục sản phẩm vào báo giá dự án

Các trang **Báo giá dự án** và **Hợp đồng dự án** có các phần cho mô tả dựa trên dự án và mô tả dựa trên sản phẩm. Đối với mô tả dựa trên sản phẩm, danh sách thả xuống trên mô tả báo giá hoặc mô tả hợp đồng dự án bao gồm tất cả sản phẩm và đơn vị trong bảng giá sản phẩm. Bạn cũng có thể thêm các sản phẩm không thuộc bảng giá sản phẩm.

Ngoài ra, bạn có thể chọn các sản phẩm từ bảng giá khác hoặc ngay từ danh mục sản phẩm. Khi bạn chọn các sản phẩm trực tiếp từ danh mục sản phẩm, bảng giá mặc định của sản phẩm đó dùng để nhận giá bán hàng của sản phẩm. Nếu một bảng giá mặc định không được đặt, giá sẽ được đặt về không (0).

Khi mô tả báo giá dựa trên danh mục sản phẩm, bạn có thể thay thế giá bán hàng trực tiếp trên mô tả báo giá. Một mô tả báo giá trong trường **Giá** có sẵn hai giá trị:

- **Thay thế giá**
- **Dùng mặc định**

Nếu bạn chọn **Thay thế giá**, giá mặc định sẽ không được đặt. Thay vào đó, bạn phải nhập giá cho sản phẩm trên mô tả báo giá. Nếu bạn chọn **Sử dụng giá mặc định**, giá bán mặc định sẽ được dùng và trường bị khóa không cho chỉnh sửa.

Giá bán mặc định được nhập trên mô tả theo sản phẩm trong báo giá. Sau đó, trường **Giá** được đặt thành **Thay thế giá** để bạn có thể chỉnh sửa giá mặc định trên mô tả báo giá. Đây là một tính năng thay thế dành riêng cho Project Operations đối với các hành vi mô tả dựa trên sản phẩm trong Dynamics 365 Sales.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]