---
title: Giải quyết giá bán hàng cho ước tính và thực tế – bản đơn giản
description: Chủ đề này cung cấp thông tin về cách giải quyết giá bán hàng cho các ước tính và thực tế.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 25620704570fa702e1e5e09c83005be50f98f20a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274529"
---
# <a name="resolve-sales-prices-for-estimates-and-actuals---lite"></a>Giải quyết giá bán hàng cho ước tính và thực tế – bản đơn giản

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Khi giá bán trên ước tính và thực tế được giải quyết trong Dynamics 365 Project Operations, hệ thống trước tiên sử dụng ngày và đơn vị tiền tệ của báo giá dự án hoặc hợp đồng liên quan để giải quyết bảng giá bán hàng. Sau khi giải quyết xong bảng giá bán hàng, hệ thống sẽ giải quyết tỷ giá bán hàng hoặc hóa đơn.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-time"></a>Giải quyết tỷ lệ bán hàng trên mô tả thực tế và ước tính cho thời gian

Trong Project Operations, các mô tả ước tính cho thời gian được sử dụng để biểu thị chi tiết mô tả báo giá và mô tả hợp đồng cho thời gian và các phân bổ nguồn lực trong dự án.

Sau khi giải quyết bảng giá bán hàng, hệ thống sẽ hoàn tất các bước sau để mặc định tỷ giá hóa đơn.

1. Hệ thống sử dụng các trường **Vai trò** và **Đơn vị nguồn lực** trên mô tả ước tính cho thời gian để đối chiếu với mô tả giá theo vai trò trong bảng giá đã giải quyết. Trùng khớp này giả định rằng các thông số giá có sẵn cho tỷ lệ hóa đơn đang được sử dụng. Nếu bạn đã đặt cấu hình giá dựa trên bất kỳ trường nào khác thay vì hoặc ngoài **Vai trò** và **Đơn vị nguồn lực**, thì đó là kết hợp sẽ được sử dụng để truy xuất mô tả giá theo vai trò phù hợp.
2. Nếu hệ thống tìm thấy một mô tả giá theo vai trò có tỷ lệ hóa đơn cho kết hợp trường **Vai trò** và **Đơn vị nguồn lực**, thì tỷ lệ hóa đơn đó sẽ được đặt mặc định.
3. Nếu không thể đối chiếu các giá trị của trường **Vai trò** và **Đơn vị nguồn lực**, thì hệ thống sẽ truy xuất mô tả giá theo vai trò với vai trò phù hợp nhưng có giá trị null của **Đơn vị nguồn lực**. Sau khi tìm thấy một bản ghi giá theo vai trò phù hợp, hệ thống sẽ mặc định tỷ lệ hóa đơn từ bản ghi đó. Giá trị trùng khớp này giả định một cấu hình có sẵn cho mức độ ưu tiên tương đối của **Vai trò** và **Đơn vị nguồn lực** là thông số giá bán hàng.

> [!NOTE]
> Nếu bạn đã đặt cấu hình mức độ ưu tiên khác của **Vai trò** và **Đơn vị nguồn lực** hoặc nếu bạn có thông số khác có mức độ ưu tiên cao hơn, hành vi này sẽ thay đổi tương ứng. Hệ thống truy xuất các bản ghi giá vai trò với các giá trị phù hợp của từng giá trị thông số giá theo thứ tự ưu tiên với các hàng có giá trị rỗng cho các thông số đến sau cùng.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Giải quyết tỷ lệ bán hàng trên mô tả thực tế và ước tính cho chi phí

Trong Project Operations, các mô tả ước tính cho chi phí được sử dụng để biểu thị chi tiết mô tả báo giá và mô tả hợp đồng cho chi phí và mô tả ước tính chi phí trong dự án.

Sau khi giải quyết bảng giá bán hàng, hệ thống sẽ hoàn tất các bước sau để mặc định đơn giá bán.

1. Hệ thống sử dụng kết hợp trường **Danh mục** và **Đơn vị** trên mô tả ước tính cho chi phí để đối chiếu với mô tả giá theo danh mục trong bảng giá đã giải quyết.
2. Nếu hệ thống tìm thấy một mô tả giá theo danh mục có tỷ lệ bán hàng cho kết hợp trường **Danh mục** và **Đơn vị**, thì tỷ lệ bán hàng đó sẽ được đặt mặc định.
3. Nếu hệ thống tìm thấy mô tả giá theo danh mục phù hợp, phương pháp định giá có thể được sử dụng để đặt mặc định giá bán. Bảng sau đây cho thấy hành vi mặc định giá chi phí trong Project Operations.

    | Ngữ cảnh | Phương pháp định giá | Giá được đặt mặc định |
    | --- | --- | --- |
    | Ước tính | Đơn giá | Dựa trên mô tả giá theo danh mục |
    | &nbsp; | Tại mức chi phí | 0.00 |
    | &nbsp; | Tăng cao hơn chi phí | 0.00 |
    | Thực tế | Đơn giá | Dựa trên mô tả giá theo danh mục |
    | &nbsp; | Tại mức chi phí | Dựa trên chi phí thực tế liên quan |
    | &nbsp; | Tăng cao hơn chi phí | Áp dụng mức tăng như được xác định bởi mô tả giá theo danh mục trên tỷ lệ chi phí đơn vị của chi phí thực tế liên quan |

4. Nếu hệ thống không thể đối chiếu các giá trị trường **Danh mục** và **Đơn vị**, thì tỷ lệ bán hàng được đặt mặc định về không (0).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]