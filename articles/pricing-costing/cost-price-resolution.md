---
title: Giải quyết giá vốn cho giá trị ước tính và thực tế
description: Chủ đề này cung cấp thông tin về cách giải quyết giá vốn cho các giá trị ước tính và thực tế.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c447e725753d738662f33cc9a5f20ec1a72b2e18
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119728"
---
# <a name="resolving-cost-prices-for-estimates-and-actuals"></a>Giải quyết giá vốn cho giá trị ước tính và thực tế

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Để giải quyết giá vốn và bảng giá vốn cho các giá trị ước tính và thực tế, hệ thống sử dụng thông tin trong các trường **Ngày**, **Tiền tệ** và **Đơn vị hợp đồng** của dự án liên quan. Sau khi bảng giá vốn được giải quyết, ứng dụng sẽ giải quyết tỷ lệ chi phí.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Giải quyết tỷ lệ chi phí trên các mục mô tả ước tính và thực tế cho Thời gian

Mục mô tả ước tính cho Thời gian đề cập đến các chi tiết mô tả hợp đồng và báo giá cho các mục chỉ định thời gian và nguồn lực trong một dự án.

Sau khi bảng giá vốn được giải quyết, hệ thống sử dụng các trường **Vai trò**, **Công ty cung cấp nguồn lực** và **Đơn vị nguồn lực** trên mục mô tả ước tính cho Thời gian để so khớp với các mục mô tả giá vai trò trong bảng giá. Hoạt động so khớp này giả định rằng bạn sử dụng các thông số định giá có sẵn cho chi phí lao động. Nếu bạn đã đặt cấu hình để hệ thống so khớp trường thay cho **Vai trò**, **Công ty cung cấp nguồn lực** và **Đơn vị cung cấp nguồn lực** hoặc kèm theo các trường đó, thì một tổ hợp khác sẽ được sử dụng để truy xuất mục mô tả giá vai trò phù hợp. Nếu ứng dụng tìm thấy một mục mô tả giá vai trò có tỷ lệ chi phí cho tổ hợp trường **Vai trò**, **Công ty cung cấp nguồn lực** và **Đơn vị nguồn lực**, thì đó sẽ là tỷ lệ chi phí mặc định. Nếu ứng dụng không thể so khớp với các giá trị **Vai trò**, **Công ty cung cấp nguồn lực** và **Đơn vị nguồn lực**, thì hệ thống sẽ truy xuất các mục mô tả giá vai trò có vai trò phù hợp nhưng có giá trị **Đơn vị nguồn lực** là rỗng. Sau khi có bản ghi giá vai trò phù hợp, tỷ lệ chi phí sẽ được lấy mặc định từ bản ghi đó. 

> [!NOTE]
> Nếu bạn đặt cấu hình mức độ ưu tiên khác cho **Vai trò**, **Công ty cung cấp nguồn lực** và **Đơn vị nguồn lực** hoặc nếu bạn có các thông số khác có mức độ ưu tiên cao hơn, thì hành vi này sẽ thay đổi tương ứng. Hệ thống truy xuất các bản ghi giá vai trò có các giá trị khớp với từng giá trị thông số định giá theo thứ tự ưu tiên, với các hàng có giá trị rỗng cho các thông số đó ở cuối cùng.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Giải quyết tỷ lệ chi phí trên các mục mô tả ước tính và thực tế cho Chi phí

Mục mô tả ước tính cho Chi phí đề cập đến thông tin chi tiết mô tả hợp đồng và báo giá cho các chi phí và mục mô tả ước tính chi phí trên một dự án.

Sau khi bảng giá vốn được giải quyết, hệ thống sử dụng một tổ hợp trường **Danh mục** và **Đơn vị** trên mục mô tả ước tính cho chi phí để so khớp với các mục mô tả **Giá danh mục** trên bảng giá đã giải quyết. Nếu hệ thống tìm thấy một mô tả giá theo danh mục có tỷ lệ chi phí cho tổ hợp trường **Danh mục** và **Đơn vị**, thì tỷ lệ chi phí đó sẽ được lấy mặc định. Nếu hệ thống không thể khớp với các giá trị **Danh mục** và **Đơn vị** hoặc nếu có thể tìm thấy một mục mô tả giá danh mục phù hợp nhưng phương thức định giá không phải là **Đơn giá**, thì tỷ lệ chi phí sẽ được đặt mặc định là không (0).
