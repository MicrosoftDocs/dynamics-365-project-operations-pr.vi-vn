---
title: Xử lý giá vốn cho các ước tính và thực tế - bản đơn giản
description: Chủ đề này cung cấp thông tin về cách giải quyết giá vốn trên các giá trị ước tính và thực tế.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bbb79fdc5c68d67530b5aa34fe6105211eff1768
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274575"
---
# <a name="resolve-cost-prices-on-estimates-and-actuals---lite"></a>Xử lý giá vốn cho các ước tính và thực tế - bản đơn giản

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Để giải quyết giá vốn và bảng giá vốn cho các giá trị ước tính và thực tế, hệ thống sử dụng thông tin trong các trường **Ngày**, **Tiền tệ** và **Đơn vị hợp đồng** của dự án liên quan. Sau khi bảng giá vốn được giải quyết, ứng dụng sẽ giải quyết tỷ lệ chi phí.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Giải quyết tỷ lệ chi phí trên các mục mô tả ước tính và thực tế cho Thời gian

Mục mô tả ước tính cho Thời gian đề cập đến các chi tiết mô tả hợp đồng và báo giá cho các mục chỉ định thời gian và nguồn lực trong một dự án.

Sau khi bảng giá vốn được giải quyết, các trường **Vai trò** và **Đơn vị Nguồn lực** trên mô tả ước tính cho Thời gian được so khớp với các mô tả giá cả vai trò trong danh sách giá. Việc so khớp này giả định rằng bạn đang sử dụng các thông số định giá tiêu chuẩn cho chi phí nhân công. Nếu bạn đã đặt cấu hình để hệ thống so khớp trường thay cho **Vai trò** và **Đơn vị nguồn lực** hoặc kèm theo các trường đó, thì một tổ hợp khác sẽ được sử dụng để truy xuất mục mô tả giá vai trò phù hợp. Nếu ứng dụng tìm thấy một mục mô tả giá vai trò có tỷ lệ chi phí cho tổ hợp trường **Vai trò** và **Đơn vị nguồn lực**, thì đó sẽ là tỷ lệ chi phí mặc định. Nếu ứng dụng không thể so khớp với các giá trị **Vai trò** và **Đơn vị nguồn lực**, thì hệ thống sẽ truy xuất các mục mô tả giá vai trò có vai trò phù hợp nhưng có giá trị **Đơn vị nguồn lực** là rỗng. Sau khi có bản ghi giá vai trò phù hợp, tỷ lệ chi phí sẽ được lấy mặc định từ bản ghi đó. 

> [!NOTE]
> Nếu bạn đặt cấu hình mức độ ưu tiên khác cho **Vai trò** và **Đơn vị nguồn lực** hoặc nếu bạn có các thông số khác có mức độ ưu tiên cao hơn, thì hành vi này sẽ thay đổi tương ứng. Hệ thống truy xuất các bản ghi giá vai trò có các giá trị khớp với từng giá trị thông số định giá theo thứ tự ưu tiên, với các hàng có giá trị rỗng cho các thông số đó ở cuối cùng.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Giải quyết tỷ lệ chi phí trên các mục mô tả ước tính và thực tế cho Chi phí

Mục mô tả ước tính cho Chi phí đề cập đến thông tin chi tiết mô tả hợp đồng và báo giá cho các chi phí và mục mô tả ước tính chi phí trên một dự án.

Sau khi bảng giá vốn được giải quyết, hệ thống dùng kết hợp các trường **Thể loại** và **Đơn vị** trên mục mô tả ước tính chi phí để so khớp với các dòng **Giá cả Thể loại** trong bảng giá vốn đã giải quyết. Nếu hệ thống tìm thấy một mô tả giá theo danh mục có tỷ lệ chi phí cho tổ hợp trường **Danh mục** và **Đơn vị**, thì tỷ lệ chi phí đó sẽ được lấy mặc định. Nếu hệ thống không thể khớp với giá trị **Thể loại** và **Đơn vị** hoặc nếu có thể tìm thấy dòng giá cả thể loại phù hợp nhưng phương pháp định giá không phải là **Đơn giá**, thì tỷ lệ chi phí mặc định bằng không (0).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]