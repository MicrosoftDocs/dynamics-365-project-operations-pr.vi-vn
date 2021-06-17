---
title: Giải quyết giá vốn cho số liệu thực tế và ước tính của dự án
description: Chủ đề này cung cấp thông tin về cách giải quyết giá vốn trên giá trị thực tế và ước tính của dự án.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6b42bc97251aec7259d314fe51b3a012edf597aa
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004422"
---
# <a name="resolve-cost-prices-on-project-estimates-and-actuals"></a>Giải quyết giá vốn cho số liệu thực tế và ước tính của dự án 

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

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a>Giải quyết tỷ lệ chi phí trên dòng giá trị thực tế và giá trị ước tính cho Vật tư

Các dòng giá trị ước tính cho Vật tư đề cập đến chi tiết mô tả báo giá và hợp đồng cho vật tư và dòng giá trị ước tính cho vật tư trong một dự án.

Sau khi xử lý bảng giá vốn, hệ thống sử dụng kết hợp các trường **Sản phẩm** và **Đơn vị** trên dòng ước tính để có giá trị ước tính cho vật tư khớp với các dòng **Hạng mục trong bảng giá** trên bảng giá đã xử lý. Nếu hệ thống tìm thấy một dòng giá sản phẩm có tỷ lệ chi phí cho tổ hợp trường **Sản phẩm** và **Đơn vị**, tỷ lệ chi phí được đặt thành mặc định. Nếu hệ thống không thể khớp các giá trị **Sản phẩm** và **Đơn vị** hoặc nếu có thể tìm thấy một dòng hạng mục trong bảng giá phù hợp nhưng phương pháp đặt giá dựa trên Chi phí chuẩn hoặc Chi phí hiện tại và không dựa trên cả hai chi phí này đều được xác định trên sản phẩm, thì chi phí đơn vị sẽ mặc định bằng 0.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
