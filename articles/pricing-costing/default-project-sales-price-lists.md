---
title: Bảng giá mặc định
description: Chủ đề này cung cấp thông tin về bảng giá vốn và bảng giá bán hàng mặc định trong Project Operations.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c204a8f0364a4be39974b101e834d4465b99f769
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000507"
---
# <a name="default-price-lists"></a>Bảng giá mặc định

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

## <a name="sales-price-lists"></a>Bảng giá bán hàng

Mọi báo giá dự án và hợp đồng trong Dynamics 365 Project Operations chứa một bảng giá bán hàng mặc định. 

### <a name="price-list-default-on-project-quotes"></a>Bảng giá mặc định trên báo giá dự án
Hệ thống hoàn tất quá trình sau để xác định bảng giá nào được đặt mặc định trên báo giá dự án:

1. Hệ thống xem xét các bảng giá được đính kèm với bảng giá dự án của tài khoản. 
2. Nếu có các bảng giá dự án được đính kèm với bản ghi tài khoản, thì hệ thống sẽ xem xét các bảng giá bán hàng đính kèm với tham số dự án khớp với đơn vị tiền tệ trong báo giá dự án.
3. Tiếp theo, hệ thống kiểm tra khoảng ngày hiệu lực của các bảng giá khớp với phạm vi ngày của báo giá dự án. Cụ thể là ngày tạo báo giá.
4. Nếu có nhiều bảng giá có hiệu lực đối với ngày của báo giá dự án, thì tất cả các bảng giá đó đều được đặt mặc định trên báo giá dự án.
5. Nếu không có bảng giá nào có hiệu lực đối với ngày của báo giá dự án, thì sẽ không có bảng giá dự án mặc định nào trên báo giá dự án. Một thông báo cảnh báo sẽ xuất hiện trên báo giá dự án. Thông báo cho biết các giá trị thực tế và ước tính trên dự án sẽ không được định giá vì không có bảng giá dự án nào được đính kèm.

### <a name="price-list-default-on-project-contracts"></a>Bảng giá mặc định trên hợp đồng dự án 
Hệ thống hoàn tất quá trình sau để xác định bảng giá nào được đặt mặc định trên hợp đồng dự án:

1. Nếu hợp đồng được tạo từ báo giá, thì các bảng giá dự án trên báo giá sẽ được sao chép riêng và được đính kèm với hợp đồng dự án.
2. Nếu hợp đồng được tạo từ đầu, thì hệ thống sẽ xem xét các bảng giá được đính kèm với bảng giá dự án của tài khoản. Nếu không có bảng giá dự án nào được đính kèm với bản ghi tài khoản, thì hệ thống sẽ tìm các bảng giá bán hàng được đính kèm với tham số dự án khớp với đơn vị tiền tệ trong hợp đồng dự án.
4. Tiếp theo, hệ thống kiểm tra khoảng ngày hiệu lực của các bảng giá khớp với phạm vi ngày của hợp đồng dự án. Cụ thể là ngày tạo hợp đồng.
5. Nếu có nhiều bảng giá có hiệu lực đối với ngày của hợp đồng, thì tất cả các bảng giá đó đều được đặt mặc định trên hợp đồng.
6. Nếu không có bảng giá nào có hiệu lực đối với ngày của hợp đồng, thì sẽ không có bảng giá dự án nào được đặt mặc định trên hợp đồng. Một thông báo cảnh báo sẽ xuất hiện trên hợp đồng dự án. Thông báo cho biết các giá trị thực tế và ước tính trên dự án sẽ không được định giá vì không có bảng giá dự án nào được đính kèm.

## <a name="cost-price-lists"></a>Bảng giá vốn

Bảng giá vốn không được đặt mặc định cho bất kỳ thực thể nào trong Project Operations. Bảng giá vốn sẽ dùng cho chi phí dự án luôn được xác định tại thời điểm thực hiện. Hệ thống hoàn tất quá trình sau để xác định bảng giá sẽ dùng cho chi phí dự án:

1. Đầu tiên, hệ thống xem xét các bảng giá được đính kèm với đơn vị tổ chức nhận thầu ký hợp đồng của dự án.
2. Sau đó, hệ thống sẽ xem xét khoảng ngày hiệu lực của các bảng giá khớp với ngày của dòng ước tính hoặc thực tế đến. Trong tình huống này, *dòng ước tính* chỉ cả ba bối cảnh ước tính trong Project Operations:

    - Dòng ước tính dự án
    - Chi tiết mô tả báo giá
    - Chi tiết mô tả hợp đồng
  
3. Nếu có nhiều bảng giá có hiệu lực đối với ngày trên dòng ước tính hoặc thực tế đến, thì bảng giá được tạo gần đây nhất sẽ được chọn.
4. Nếu không có bảng giá nào được đính kèm với đơn vị tổ chức ký hợp đồng của dự án, thì hệ thống sẽ xem xét các bảng giá vốn được đính kèm với tham số dự án khớp với đơn vị tiền tệ của dự án.
5. Tiếp theo, hệ thống sẽ xem xét khoảng ngày hiệu lực của các bảng giá khớp với ngày của dòng ước tính hoặc thực tế đến. 
6. Nếu có nhiều bảng giá có hiệu lực đối với ngày trên dòng ước tính hoặc thực tế đến, thì bảng giá được tạo gần đây nhất sẽ được chọn.
7. Nếu không có bảng giá vốn nào được đính kèm với tham số dự án khớp với đơn vị tiền tệ và ngày có hiệu lực, thì hệ thống sẽ đặt mặc định tỷ lệ chi phí thành không (0) trên dòng ước tính hoặc thực tế đến.


[!INCLUDE[footer-include](../includes/footer-banner.md)]