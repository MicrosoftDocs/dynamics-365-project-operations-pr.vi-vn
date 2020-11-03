---
title: Giải quyết giá bán cho ước tính và thực tế
description: Chủ đề này cung cấp thông tin về cách giải quyết tỷ lệ bán hàng cho các ước tính và thực tế.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b4ae5b3c4a4378330caed97011f55ca11175e644
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/21/2020
ms.locfileid: "4088167"
---
# <a name="resolve-sales-prices-for-estimates-and-actuals"></a>Giải quyết giá bán cho ước tính và thực tế

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Khi giá bán hàng trên ước tính và thực tế được giải quyết trong Dynamics 365 Project Operations, trước tiên hệ thống sử dụng ngày và đơn vị tiền tệ của báo giá hoặc hợp đồng dự án liên quan để giải quyết bảng giá bán. Sau khi giải quyết xong bảng giá bán hàng, hệ thống sẽ giải quyết tỷ giá bán hàng hoặc hóa đơn.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-time"></a>Giải quyết tỷ lệ bán hàng trên mô tả thực tế và ước tính cho thời gian

Trong Project Operations, các mô tả ước tính cho thời gian được sử dụng để biểu thị chi tiết mô tả báo giá và mô tả hợp đồng cho thời gian và các phân bổ nguồn lực trong dự án.

Sau khi giải quyết bảng giá bán hàng, hệ thống sẽ hoàn tất các bước sau để mặc định tỷ giá hóa đơn.

1. Hệ thống sử dụng các trường **Vai trò** , **Công ty cung cấp nguồn lực** và **Đơn vị cung cấp nguồn lực** trên dòng ước tính cho thời gian, để khớp với các dòng giá vai trò trong bảng giá đã giải quyết. Trùng khớp này giả định rằng các thông số giá có sẵn cho tỷ lệ hóa đơn đang được sử dụng. Nếu bạn đã định cấu hình giá dựa trên bất kỳ trường nào khác thay vì hoặc ngoài **Vai trò** , **Công ty cung cấp nguồn lực** và **Đơn vị cung cấp nguồn lực** , thì đó là sự kết hợp sẽ được sử dụng để truy xuất dòng giá vai trò phù hợp.
2. Nếu hệ thống tìm thấy một dòng giá vai trò có tỷ lệ thanh toán cho kết hợp trường **Vai trò** , **Công ty cung cấp nguồn lực** và **Đơn vị cung cấp nguồn lực** , sau đó tỷ lệ hóa đơn đó được đặt mặc định.
3. Nếu hệ thống không thể khớp với các giá trị trường **Vai trò** , **Công ty cung cấp nguồn lực** và **Đơn vị cung cấp nguồn lực** , sau đó hệ thống truy xuất các dòng giá vai trò có vai trò phù hợp nhưng giá trị null của **Đơn vị nguồn lực**. Sau khi tìm thấy một bản ghi giá theo vai trò phù hợp, hệ thống sẽ mặc định tỷ lệ hóa đơn từ bản ghi đó. Giá trị trùng khớp này giả định một cấu hình có sẵn cho mức độ ưu tiên tương đối của **Vai trò** và **Đơn vị nguồn lực** là thông số giá bán hàng.

> [!NOTE]
> Nếu bạn đã định cấu hình mức độ ưu tiên khác của **Vai trò** , **Công ty cung cấp nguồn lực** và **Đơn vị cung cấp nguồn lực** hoặc nếu bạn có các thông số khác có mức độ ưu tiên cao hơn, hành vi này sẽ thay đổi tương ứng. Hệ thống truy xuất các bản ghi giá vai trò với các giá trị phù hợp của từng giá trị thông số giá theo thứ tự ưu tiên với các hàng có giá trị rỗng cho các thông số đến sau cùng.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Giải quyết tỷ lệ bán hàng trên mô tả thực tế và ước tính cho chi phí

Trong Project Operations, các mô tả ước tính cho chi phí được sử dụng để biểu thị chi tiết mô tả báo giá và mô tả hợp đồng cho chi phí và mô tả ước tính chi phí trong dự án.

Sau khi giải quyết bảng giá bán hàng, hệ thống sẽ hoàn tất các bước sau để mặc định đơn giá bán.

1. Hệ thống sử dụng kết hợp trường **Danh mục** và **Đơn vị** trên mô tả ước tính cho chi phí để đối chiếu với mô tả giá theo danh mục trong bảng giá đã giải quyết.
2. Nếu hệ thống tìm thấy một mô tả giá theo danh mục có tỷ lệ bán hàng cho kết hợp trường **Danh mục** và **Đơn vị** , thì tỷ lệ bán hàng đó sẽ được đặt mặc định.
3. Nếu hệ thống tìm thấy mô tả giá theo danh mục phù hợp, phương pháp định giá có thể được sử dụng để đặt mặc định giá bán. Bảng sau đây cho thấy hành vi mặc định giá chi phí trong Project Operations.

    | Ngữ cảnh | Phương pháp định giá | Giá được đặt mặc định |
    | --- | --- | --- |
    | Ước tính | Đơn giá | Dựa trên mô tả giá theo danh mục |
    | &nbsp; | Tại mức chi phí | 0.00 |
    | &nbsp; | Tăng cao hơn chi phí | 0.00 |
    | Thực tế | Đơn giá | Dựa trên mô tả giá theo danh mục |
    | &nbsp; | Tại mức chi phí | Dựa trên chi phí thực tế liên quan |
    | &nbsp; | Tăng cao hơn chi phí | Bằng cách áp dụng mức tăng như được xác định bởi dòng giá danh mục trên tỷ lệ chi phí đơn vị của chi phí thực tế liên quan |

4. Nếu hệ thống không thể đối chiếu các giá trị trường **Danh mục** và **Đơn vị** , thì tỷ lệ bán hàng được đặt mặc định về không (0).
