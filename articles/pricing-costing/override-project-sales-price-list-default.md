---
title: Thay thế bảng giá bán hàng của dự án
description: Chủ đề này cung cấp thông tin về cách tạo bảng giá bán hàng tùy chỉnh.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 17a86e89f626cef720fe3c8db0cbd8d6a2a3ddd5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275564"
---
# <a name="override-project-sales-price-lists"></a>Thay thế bảng giá bán hàng của dự án

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

## <a name="customer-specific-project-price-lists"></a>Bảng giá dự án cụ thể cho từng khách hàng

Các thỏa thuận về giá cụ thể cho từng khách hàng có thể được thiết lập dưới dạng bảng giá dự án trên hồ sơ tài khoản trong Dynamics 365 Project Operations.

Để thiết lập bảng giá dự án cụ thể cho từng khách hàng, trong khu vực **Bán hàng**, hãy chuyển đến hồ sơ tài khoản.

1. Mở trang danh sách **Tài khoản**.
2. Tìm và nhấp đúp vào hồ sơ khách hàng để mở trang chi tiết **Tài khoản**.
3. Trên tab **Bảng giá dự án**, hãy chọn **+ Bảng giá dự án mới**.
4. Trên **Bảng giá dự án mới**, hãy chọn một bảng giá từ danh sách thả xuống. Chỉ đưa vào các bảng giá có ngữ cảnh được đặt thành **Bán hàng** và đơn vị tiền tệ của bảng giá đó khớp với đơn vị tiền tệ của tài khoản.
5. Đặt tên cho liên kết rồi chọn **Lưu**. Một bảng giá dự án cụ thể cho từng khách hàng được tạo. Bảng giá này sẽ được dùng để đặt mặc định giá dự án trên báo giá dự án hoặc hợp đồng được tạo cho khách hàng này, trong đó ngày tạo báo giá hoặc hợp đồng dự án nằm trong ngày có hiệu lực của bảng giá.

## <a name="custom-pricing-on-project-quotes"></a>Giá tùy chỉnh trên báo giá dự án

Trên báo giá dự án, bạn có thể có giá dự án bắt đầu với một bảng giá tiêu chuẩn mặc định do khách hàng đặt hoặc từ các tham số dự án.

Khi bạn cần giá tùy chỉnh cho công việc liên quan đến dự án trên một báo giá cụ thể, bạn có thể lấy giá đó từ thực thể liên kết với bảng giá dự án.

Hoàn thành các bước sau để thiết lập giá dự án cụ thể theo báo giá.

1. Mở báo giá dự án rồi chọn tab **Bảng giá dự án**.
2. Trong lưới con, hãy chọn **Tạo giá tùy chỉnh**.

Tất cả bảng giá dự án đính kèm với báo giá đều được sao chép sang bảng giá mới. Tên của các bảng giá mới phản ánh tên của báo giá có dấu ngày giờ cho biết thời điểm tạo các bảng giá này.

Bạn có thể sử dụng từng bảng giá đó và cập nhật giá nhân công (giá vai trò) và giá chi phí (giá thể loại). Các mức giá này sẽ chỉ áp dụng cho báo giá dự án này.

## <a name="price-lists-on-a-project-contract"></a>Bảng giá trên hợp đồng dự án

Trên hợp đồng dự án, giá dự án luôn được đặt mặc định dưới dạng bảng giá tùy chỉnh với tên hợp đồng và dấu ngày giờ tạo được thêm vào tên. Điều này cũng đúng cho dù hợp đồng được tạo khi đã có báo giá hay hợp đồng được tạo từ đầu. Nếu cần, bạn có thể loại bỏ liên kết này khỏi bảng giá tùy chỉnh và liên kết bảng giá chuẩn với hợp đồng dự án.

Khi bạn liên kết một bảng giá chuẩn với bảng giá dự án trên báo giá hoặc hợp đồng, bất kỳ thay đổi nào được thực hiện đối với giá trong bảng giá đó sẽ ảnh hưởng đến tất cả báo giá và hợp đồng sử dụng bảng giá đó.


[!INCLUDE[footer-include](../includes/footer-banner.md)]