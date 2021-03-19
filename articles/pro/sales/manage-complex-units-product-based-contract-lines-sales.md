---
title: Quản lý nhiều đơn vị phức tạp cho các mô tả hợp đồng dựa trên sản phẩm - bản đơn giản
description: Chủ đề này cung cấp thông tin về việc hỗ trợ bán các sản phẩm dựa trên đăng ký.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 029d2aa4fd20fc036a34ae6136fe12454f3b7703
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273359"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a>Quản lý nhiều đơn vị phức tạp cho các mô tả hợp đồng dựa trên sản phẩm - bản đơn giản

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Dynamics 365 Project Operations sử dụng các yếu tố số lượng để hỗ trợ bán các sản phẩm dựa trên đăng ký. Đối với các sản phẩm dựa trên đăng ký, số lượng trên hợp đồng hoặc phần mô tả hợp đồng dự án được thể hiện dưới dạng số tháng làm người dùng.

Giá của phần mềm đăng ký được lưu trữ trong danh mục dưới dạng giá cho mỗi người dùng mỗi tháng. Trong quá trình bán hàng, giá trên phần mô tả hợp đồng thường là giá trên mỗi người dùng, mỗi tháng do đại lý bán hàng thương lượng và giảm giá. Mỗi thỏa thuận có một số lượng người dùng khác nhau và số lượng tháng đăng ký khác nhau. Số lượng dùng để tính số tiền trong phần mô tả hợp đồng là sản phẩm gồm số lượng người dùng và số lượng tháng đăng ký.

Để hỗ trợ loại bán hàng này, Project Operations hỗ trợ khái niệm *hệ số số lượng*. Yếu tố số lượng dựa vào các thuộc tính sản phẩm. Khi bạn đặt cấu hình các thuộc tính cụ thể cho sản phẩm, bạn có thể gắn cờ một tập con của các thuộc tính đó hoặc tất cả thuộc tính ở dạng các yếu tố số lượng.

Project Operations xác thực rằng chỉ có thuộc tính số hoặc các thuộc tính sản phẩm có loại dữ liệu số được gắn cờ ở dạng yếu tố số lượng. Khi một sản phẩm dã đặt cấu hình hệ số số lượng được thêm vào phần mô tả hợp đồng, trường **Số lượng** sẽ trở thành chỉ đọc. Sau khi bạn nhập giá trị cho thuộc tính sản phẩm là hệ số số lượng, Project Operations sẽ tính số lượng có trong phần mô tả hợp đồng.

Ví dụ: Dynamics 365 Sales có thể có các thuộc tính sau đây:

- **Số người dùng**: Số lượng người dùng.
- **Số tháng**: Số lượng tháng đăng ký.
- **SKU sản phẩm**: Đơn vị lưu kho (SKU) của sản phẩm.

Các thuộc tính **Sô người dùng** và **Số tháng** có thể được gắn cờ ở dạng yếu tố số lượng bằng cách chỉnh sửa các thuộc tính của mô tả sản phẩm.

Để tạo các hệ số số lượng từ thuộc tính của sản phẩm, hãy hoàn thành các bước sau.

1. Trên **Project Operations**, hãy chọn **Sản phẩm bán hàng**.
2. Mở sản phẩm mà bạn cần thiết lập hệ số số lượng. Đảm bảo sản phẩm có các thuộc tính đã được thiết lập.
3. Trên trang **Thông tin dự án**, hãy chọn tab **Hệ số số lượng**.
4. Trong lưới con, chọn **+ Tính toán trường mới**.
5. Nhập tên **Hệ số số lượng** rồi chọn giá trị thuộc tính ánh xạ đến mục tính toán của trường.
6. Lưu và đóng biểu mẫu.
7. Lặp lại các bước từ 2 đến 6 cho tất cả các thuộc tính sẽ tạo nên số lượng trong phần mô tả hợp đồng dựa trên sản phẩm.

Nếu hệ số số lượng đã được thiết lập, khi người dùng tạo phần mô tả hợp đồng cho sản phẩm này, số lượng trong phần mô tả hợp đồng sẽ bị khóa. Sau đó, số lượng được tính dưới dạng sản phẩm gồm các giá trị thuộc tính cho phần mô tả hợp đồng đó.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]