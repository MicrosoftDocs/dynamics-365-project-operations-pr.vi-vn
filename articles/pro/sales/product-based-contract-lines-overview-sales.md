---
title: Tổng quan về mô tả hợp đồng dựa trên sản phẩm - bản đơn giản
description: Chủ đề này cung cấp thông tin về mô tả hợp đồng dựa trên sản phẩm.
author: rumant
ms.date: 10/07/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8006e90e0d4fdf02042f26b261775a92f87f47ca
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598238"
---
# <a name="product-based-contract-lines-overview---lite"></a>Tổng quan về mô tả hợp đồng dựa trên sản phẩm - bản đơn giản

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Bạn có thể tạo mô tả báo giá dựa trên sản phẩm trong Dynamics 365 Project Operations. Mô tả hợp đồng dựa trên sản phẩm có thể là mô tả được tạo thủ công hoặc các mục từ danh mục sản phẩm.

## <a name="product-catalog"></a>Danh mục sản phẩm

Các sản phẩm trong danh mục sản phẩm có đơn vị mặc định và nhóm đơn vị đo. Nếu một số sản phẩm có cùng nhóm thuộc tính, bạn có thể tạo dòng sản phẩm cũng có các thuộc tính đó. Tất cả sản phẩm trong một dòng sản phẩm thừa kế cùng bộ thuộc tính.

Ví dụ: công ty bán các giấy phép gói đăng ký cho các loại phần mềm khác nhau. Tất cả phần mềm gói đăng ký có 2 thuộc tính sau:

- Số người dùng
- Thời gian đăng ký (trong tháng)

Để duy trì loại danh mục này, hãy tạo một dòng sản phẩm có tên **Phần mềm đăng ký**. Thêm các thuộc tính, **Số lượng người dùng** và **Thời hạn đăng ký** cho dòng sản phẩm. Sau đó, thêm các sản phẩm riêng lẻ vào dòng sản phẩm **Phần mềm đăng ký**.

## <a name="add-product-catalog-items-to-a-project-contract"></a>Thêm các mục danh mục sản phẩm vào hợp đồng dự án

Hợp đồng dự án có các phần cho 2 loại mô tả: mô tả dựa trên dự án và mô tả dựa trên sản phẩm. Mô tả dựa trên sản phẩm bao gồm tất cả các sản phẩm và đơn vị trong bảng giá sản phẩm trên hợp đồng. Có thể thêm các sản phẩm không thuộc bảng giá sản phẩm của hợp đồng.

Bạn có thể chọn sản phẩm từ các bảng giá khác hoặc trực tiếp từ danh mục sản phẩm. Khi bạn chọn các sản phẩm trực tiếp từ danh mục sản phẩm, bảng giá mặc định của sản phẩm đó dùng cho giá bán hàng của sản phẩm. Nếu một bảng giá mặc định không được đặt, giá sẽ được đặt về 0 (không).

Nếu mô tả hợp đồng dựa trên danh mục sản phẩm, bạn có thể thay thế giá bán hàng trực tiếp trên mô tả. Mô tả hợp đồng có trường **Giá** có hai giá trị:

- **Thay thế giá**
- **Dùng mặc định**

Nếu bạn đặt trường **Giá** thành **Ghi đè giá**, giá mặc định không được đặt. Nhập giá cho sản phẩm trên mô tả hợp đồng. Nếu bạn đặt trường thành **Sử dụng mặc định**, giá bán mặc định được sử dụng và không thể chỉnh sửa trường.

Sau khi bạn cài đặt Project Operations, giá bán hàng mặc định được nhập trên mô tả dựa trên sản phẩm trên hợp đồng. Sau đó, trường **Giá** được đặt thành **Thay thế giá** để bạn có thể chỉnh sửa giá mặc định trên mô tả hợp đồng. Đây là giá trị ghi đè dành riêng cho Project Operations đối với hành vi mô tả dựa trên sản phẩm trong Dynamics 365 Sales.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]