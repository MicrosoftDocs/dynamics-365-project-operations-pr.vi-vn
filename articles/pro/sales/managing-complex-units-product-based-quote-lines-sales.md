---
title: Quản lý các đơn vị phức tạp như mỗi người dùng, mỗi tháng cho các mô tả báo giá dựa trên sản phẩm - bản đơn giản
description: Chủ đề này cung cấp thông tin về việc quản lý các đơn vị phức tạp cho mô tả báo giá dựa trên sản phẩm.
author: rumant
ms.date: 10/06/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 87f6ef70a328164291f37e42d106649178c8cfbe
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591062"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines---lite"></a>Quản lý các đơn vị phức tạp như mỗi người dùng, mỗi tháng cho các mô tả báo giá dựa trên sản phẩm - bản đơn giản

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Dynamics 365 Project Operations sử dụng các yếu tố số lượng để hỗ trợ bán các sản phẩm dựa trên đăng ký. Đối với các sản phẩm dựa trên đăng ký, số lượng trên báo giá hoặc mô tả hợp đồng dự án được thể hiện ở dạng số tháng người dùng.

Thông thường, giá phần mềm đăng ký được lưu trữ trong danh mục ở dạng giá cho mỗi người dùng mỗi tháng. Trong quá trình bán hàng, giá trên mô tả báo giá thường là giá trên mỗi người dùng, mỗi tháng được đại lý bán hàng CNTT thương lượng và giảm giá. Mỗi thỏa thuận có một số lượng người dùng khác nhau và số lượng tháng đăng ký khác nhau. Số lượng được dùng để tính toán mô tả báo giá là sản phẩm của số lượng người dùng và số lượng tháng đăng ký.

Để hỗ trợ loại bán hàng này, Project Operations giới thiệu khái nhiệm yếu tố số lượng. Yếu tố số lượng dựa vào các thuộc tính sản phẩm trong Dynamics 365. Khi bạn đặt cấu hình các thuộc tính cụ thể cho sản phẩm, Project Operations cho phép bạn gắn cờ một tập con hoặc tất cả thuộc tính ở dạng các yếu tố số lượng.

Project Operations xác thực rằng chỉ có thuộc tính số hoặc các thuộc tính sản phẩm có loại dữ liệu số được gắn cờ ở dạng yếu tố số lượng. Khi bạn thêm một sản phẩm có yếu tố số lượng vào mô tả báo giá, trường **Số lượng** trở thành chỉ đọc. Sau khi bạn nhập giá trị cho các thuộc tính sản phẩm là các yếu tố số lượng, Project Operations sẽ tính số lượng của mô tả báo giá.

Ví dụ: Dynamics 365 Sales có thể có các thuộc tính sau đây:

- **Số người dùng**: Số lượng người dùng
- **Số tháng**: Số lượng tháng đăng ký
- **SKU sản phẩm**

Bạn có thể gắn cờ **Số người dùng** và **Số tháng** có thể được gắn cờ ở dạng yếu tố số lượng bằng cách chỉnh sửa các thuộc tính của mô tả sản phẩm.

Để tạo yếu tố Số lượng từ thuộc tính Sản phẩm, hãy làm theo các bước sau:

1. Trên ngăn điều hướng bên trái Project Operations, hãy đi tới **Bán hàng** > **Sản phẩm**.
2. Mở sản phẩm mà bạn cần đặt cấu hình yếu tố số lượng. Đảm bảo rằng sản phẩm có các thuộc tính đã được đặt cấu hình.
3. Trên trang **Thông tin dự án** cho Sản phẩm, chọn tab **Yếu tố số lượng**.
4. Trong lưới con, chọn **+ Tính toán trường mới**.
5. Nhập tên của yếu tố Số lượng và chọn giá trị thuộc tính ánh xạ đến mục tính toán trường.
6. Lưu và đóng biểu mẫu. Lặp lại các bước này cho tất cả các thuộc tính để tính toán số lượng cho mô tả báo giá dựa trên sản phẩm.

Khi bạn tạo mô tả báo giá dựa trên sản phẩm cho một sản phẩm, số lượng của mô tả báo giá sẽ bị khóa. Số lượng sẽ được tính dưới dạng tích số của các giá trị thuộc tính mà bạn nhập cho mô tả báo giá đó.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]