---
title: Thiết lập bảng giá
description: Bài viết này cung cấp thông tin về cách thiết lập bảng giá vốn và giá bán.
author: rumant
ms.date: 10/20/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8a6d96f4a5a8d97e86bbd00413e21f69255a48c5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917694"
---
# <a name="set-up-price-lists"></a>Thiết lập bảng giá

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Bảng giá trong Dynamics 365 Project Operations đại diện cho một danh mục tỷ giá. Các mức giá thể hiện chi phí, doanh số bán hàng và tỷ lệ thanh toán. Tùy thuộc vào việc bảng giá thể hiện tỷ lệ chi phí hay tỷ lệ bán hàng và thanh toán, bối cảnh của bảng giá là **Bán hàng** hoặc **Chi phí**.

Các phần mở rộng sau đây dành riêng cho Project Operations và được áp dụng cho bảng giá từ Dynamics 365 Sales.

- **Bối cảnh**: Trường này có các giá trị được hỗ trợ, **Chi phí** và **Bán hàng**. Giá trị **Mua hàng** không được hỗ trợ. Đặt ngữ cảnh thành **Chi phí** để lập bảng giá vốn hoặc đặt ngữ cảnh thành **Bán hàng** cho bảng giá bán hàng. Bảng giá vốn giải quyết giá cho loại chi phí trên hồ sơ ước tính và thực tế. Bảng giá bán hàng giải quyết giá trên hồ sơ ước tính và thực tế của các loại bán hàng chưa lập hóa đơn và đã lập hóa đơn.
- **Đơn vị thời gian**: Đây là đơn vị thời gian mặc định mà giá được thiết lập trong bảng **Giá theo vai trò** cho bảng giá này.
- **Thực thể bảng giá**: Trường ẩn này là của Project Operations để phân biệt các bảng giá là báo giá hoặc theo hợp đồng cụ thể với các bảng giá tiêu chuẩn và có thể áp dụng trên toàn cầu.

## <a name="price-list-header"></a>Tiêu đề bảng giá

Bảng sau bao gồm các trường trên tab **Tổng quát** của bảng giá dành riêng cho Project Operations hoặc có những thay đổi đáng kể về hành vi từ bảng giá trong Bán hàng.

| Trường | Vị trí | Nội dung mô tả | Tác động xuôi tuyến |
| --- | --- | --- | --- |
| Tên | Tab **Tổng quát** và biểu mẫu **Tạo nhanh** | Danh tính của bảng giá. | Bảng giá được hiển thị với giá trị này trên tất cả các trang danh sách và các tùy chọn thả xuống.|
| Ngữ cảnh | Tab **Tổng quát** và biểu mẫu **Tạo nhanh** | Trường này có thể được đặt thành **Chi phí** hoặc **Bán hàng**. | Bảng giá được đặt thành **Chi phí** dùng để tra cứu giá cho ước tính chi phí và chi phí thực tế. Bảng giá được đặt thành **Bán hàng** dùng để tra cứu giá cho ước tính chi phí bán hàng và chi phí thực tế bán hàng. Chỉ các bảng giá có ngữ cảnh được đặt thành **Bán hàng** có thể đính kèm vào bảng giá dự án cho khách hàng, báo giá dự án và hợp đồng dự án. |
| Ngày bắt đầu | Tab **Tổng quát** và biểu mẫu **Tạo nhanh** | Ngày bắt đầu khoảng thời gian có hiệu lực của bảng giá. | Với trường **Ngày cuối**, trường này được sử dụng để xác định bảng giá áp dụng cho một ước tính hoặc dòng thực tế nhất định. |
| Ngày kết thúc | Tab **Tổng quát** và biểu mẫu **Tạo nhanh** | Ngày kết thúc khoảng thời gian có hiệu lực của bảng giá. | Với trường **Ngày bắt đầu**, trường này được sử dụng để xác định bảng giá áp dụng cho một ước tính hoặc dòng thực tế nhất định. |
| Tiền tệ | Tab **Tổng quát** và biểu mẫu **Tạo nhanh** | Trường này được sử dụng để đặt mặc định đơn vị tiền tệ trên mỗi dòng mục vai trò, danh mục hoặc hạng mục trong bảng giá liên quan đến bảng giá này. | Trên bảng giá **Bán hàng**, không thể tạo vai trò, danh mục hoặc dòng hạng mục trong bảng giá bằng bất kỳ đơn vị tiền tệ nào khác ngoài đơn vị tiền tệ này. Trên bảng giá **Chi phí**, bạn có thể tạo dòng giá theo vai trò bằng bất kỳ đơn vị tiền tệ nào. Đơn vị tiền tệ được xác định ở đây được sử dụng làm mặc định. Thiết lập người dùng là giá theo vai trò có liên quan có thể ghi đè giá trị này để cho phép thiết lập tỷ lệ chi phí nhân công bằng bất kỳ đơn vị tiền tệ nào. Chỉ có thể thiết lập tỷ lệ chi phí danh mục và chi phí hạng mục trong bảng giá bằng đơn vị tiền tệ được xác định tại đây. |
| Đơn vị Thời gian | Tab **Tổng quát** và biểu mẫu **Tạo nhanh** | Trường này được sử dụng để đặt mặc định đơn vị thời gian trên mỗi dòng vai trò liên quan đến bảng giá này. | Giá trị trường này chỉ được sử dụng trên thiết lập giá vai trò liên quan. Trên bảng giá **Chi phí** và **Bán hàng**, bạn có thể tạo dòng giá theo vai trò bằng bất kỳ đơn vị thời gian nào. Đơn vị thời gian được xác định ở đây được dùng làm đơn vị mặc định. Giá theo vai trò liên quan đến thiết lập người dùng có thể ghi đè giá trị này để cho phép thiết lập tỷ lệ chi phí nhân công và tỷ lệ thanh toán bằng bất kỳ đơn vị tiền tệ nào. |
| Nội dung mô tả | Tab **Tổng quát** và biểu mẫu **Tạo nhanh** | Trường văn bản này cho phép bạn cung cấp mô tả nhiều dòng về bảng giá. | Trường này được hiển thị ở các dạng xem **Được liên kết** trên bảng giá trong nhiều thực thể khác nhau có bảng giá liên quan. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]