---
title: Giải quyết giá vốn cho giá trị ước tính và thực tế
description: Bài viết này cung cấp thông tin về cách giải quyết giá chi phí ước tính và thực tế.
author: rumant
ms.date: 04/09/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: af17712f0aef4fe3e6e758edd976cc377e90631d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919994"
---
# <a name="resolving-cost-prices-for-estimates-and-actuals"></a>Giải quyết giá vốn cho giá trị ước tính và thực tế

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Để giải quyết giá vốn và bảng giá vốn cho các giá trị ước tính và thực tế, hệ thống sử dụng thông tin trong các trường **Ngày**, **Tiền tệ** và **Đơn vị hợp đồng** của dự án liên quan. Sau khi bảng giá vốn được giải quyết, ứng dụng sẽ giải quyết tỷ lệ chi phí.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Giải quyết tỷ lệ chi phí trên các mục mô tả ước tính và thực tế cho Thời gian

Mục mô tả ước tính cho Thời gian đề cập đến các chi tiết mô tả hợp đồng và báo giá cho các mục chỉ định thời gian và nguồn lực trong một dự án.

Sau khi bảng giá vốn được giải quyết, hệ thống sử dụng các trường **Vai trò**, **Công ty cung cấp nguồn lực** và **Đơn vị nguồn lực** trên mục mô tả ước tính cho Thời gian để so khớp với các mục mô tả giá vai trò trong bảng giá. Hoạt động so khớp này giả định rằng bạn sử dụng các thông số định giá có sẵn cho chi phí lao động. Nếu bạn đã đặt cấu hình để hệ thống so khớp trường thay cho **Vai trò**, **Công ty cung cấp nguồn lực** và **Đơn vị cung cấp nguồn lực** hoặc kèm theo các trường đó, thì một tổ hợp khác sẽ được sử dụng để truy xuất mục mô tả giá vai trò phù hợp. Nếu ứng dụng tìm thấy một mục mô tả giá vai trò có tỷ lệ chi phí cho tổ hợp trường **Vai trò**, **Công ty cung cấp nguồn lực** và **Đơn vị nguồn lực**, thì đó sẽ là tỷ lệ chi phí mặc định. Nếu không thể khớp chính xác tổ hợp các giá trị **Vai trò**, **Công ty cung cấp nguồn lực** và **Đơn vị nguồn lực**, ứng dụng sẽ truy xuất các dòng về giá theo vai trò có một giá trị theo vai trò phù hợp, nhưng có giá trị rỗng cho **Đơn vị nguồn lực** và **Công ty cung cấp nguồn lực**. Sau khi tìm thấy một bản ghi giá theo vai trò phù hợp có giá trị giá theo vai trò phù hợp, tỷ lệ chi phí sẽ được đặt mặc định từ bản ghi đó. 

> [!NOTE]
> Nếu bạn đặt cấu hình mức độ ưu tiên khác cho **Vai trò**, **Công ty cung cấp nguồn lực** và **Đơn vị nguồn lực** hoặc nếu bạn có các thông số khác có mức độ ưu tiên cao hơn, thì hành vi này sẽ thay đổi tương ứng. Hệ thống truy xuất các bản ghi giá theo vai trò có các giá trị khớp với từng giá trị của thứ nguyên giá theo thứ tự ưu tiên, trong đó các hàng không có giá trị cho các thứ nguyên đó sẽ nằm cuối cùng trong thứ tự ưu tiên.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Giải quyết tỷ lệ chi phí trên các mục mô tả ước tính và thực tế cho Chi phí

Mục mô tả ước tính cho Chi phí đề cập đến thông tin chi tiết mô tả hợp đồng và báo giá cho các chi phí và mục mô tả ước tính chi phí trên một dự án.

Sau khi bảng giá vốn được giải quyết, hệ thống sử dụng một tổ hợp trường **Danh mục** và **Đơn vị** trên mục mô tả ước tính cho chi phí để so khớp với các mục mô tả **Giá danh mục** trên bảng giá đã giải quyết. Nếu hệ thống tìm thấy một mô tả giá theo danh mục có tỷ lệ chi phí cho tổ hợp trường **Danh mục** và **Đơn vị**, thì tỷ lệ chi phí đó sẽ được lấy mặc định. Nếu hệ thống không thể khớp với các giá trị **Danh mục** và **Đơn vị** hoặc nếu có thể tìm thấy một mục mô tả giá danh mục phù hợp nhưng phương thức định giá không phải là **Đơn giá**, thì tỷ lệ chi phí sẽ được đặt mặc định là không (0).

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a>Giải quyết tỷ lệ chi phí trên dòng giá trị thực tế và giá trị ước tính cho vật tư

Các dòng giá trị ước tính cho vật tư đề cập đến chi tiết mô tả báo giá và hợp đồng cho vật tư và dòng giá trị ước tính cho vật tư trong một dự án.

Sau khi xử lý bảng giá vốn, hệ thống sử dụng kết hợp các trường **Sản phẩm** và **Đơn vị** trên dòng ước tính để có giá trị ước tính cho vật tư khớp với các dòng **Hạng mục trong bảng giá** trên bảng giá đã xử lý. Nếu hệ thống tìm thấy một dòng giá sản phẩm có tỷ lệ chi phí cho tổ hợp trường **Sản phẩm** và **Đơn vị**, tỷ lệ chi phí được đặt thành mặc định. Nếu hệ thống không thể khớp các giá trị **Sản phẩm** và **Đơn vị**, thì chi phí đơn vị mặc định là 0. Giá trị mặc định này cũng sẽ xảy ra nếu có một dòng hạng mục trong bảng giá phù hợp, nhưng phương pháp đặt giá dựa trên chi phí chuẩn hoặc chi phí hiện tại chưa được xác định trong sản phẩm.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
