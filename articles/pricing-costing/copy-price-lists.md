---
title: Sao chép bảng giá
description: Chủ đề này cung cấp thông tin về cách sao chép bảng giá trong Project Operations.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9e4f4eeda019f2af11a0d7a4469c41ee450eb03b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001452"
---
# <a name="copy-price-lists"></a>Sao chép bảng giá

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Bạn có thể tạo bản sao của bảng giá trong Dynamics 365 Project Operations. Chẳng hạn, bạn có thể tạo bảng giá cho năm sắp tới bằng bảng giá của năm hiện tại.  Hoặc, bạn có thể sao chép một bảng giá cho tỷ lệ hóa đơn và giá bán hàng từ bảng giá cho chi phí. 

Để tạo bản sao bảng giá, hãy hoàn thành các bước sau.

1. Mở bảng giá mà bạn muốn sao chép và chọn **Sao chép**.
2. Nhập mọi thông tin cần thiết để sao chép bảng giá. Bảng sau đây trình bày những điểm cần lưu ý khi nhập thông tin.

| Trường | Nội dung mô tả | Tác động xuôi tuyến |
| --- | --- | --- |
| Tên | Tên của bảng giá nguồn kèm theo **- sao chép**. | Bảng giá đưa giá trị này vào tất cả các trang danh sách và tùy chọn thả xuống. |
| Ngữ cảnh | Nhập bối cảnh mà bạn muốn dùng cho danh sách giá mục tiêu. | Bảng giá có bối cảnh được đặt thành **Chi phí** sẽ được dùng để tra cứu giá cho giá trị ước tính chi phí và chi phí thực tế. Bảng giá có bối cảnh được đặt thành **Bán hàng** sẽ được dùng để tra cứu giá cho giá trị ước tính bán hàng và giá trị bán hàng thực tế. Chỉ các bảng giá có bối cảnh được đặt thành **Bán hàng** mới có thể được đính kèm vào bảng giá dự án cho khách hàng, báo giá hoặc hợp đồng. |
| Ngày bắt đầu | Ngày bắt đầu khoảng thời gian có hiệu lực của bảng giá. | Cùng với trường **Ngày kết thúc**, trường này được sử dụng để xác định bảng giá nào được áp dụng cho một dòng ước tính hoặc thực tế nhất định. |
| Ngày kết thúc | Ngày kết thúc khoảng thời gian có hiệu lực của bảng giá. | Cùng với trường **Ngày bắt đầu**, trường này được sử dụng để xác định bảng giá nào được áp dụng cho một dòng ước tính hoặc thực tế nhất định. |
| Tiền tệ | Đơn vị tiền tệ của bảng giá nguồn. Mục này có thể thay đổi. | Khi mục này được thay đổi, tất cả các mục mô tả giá tạo ra cho nhân công, chi phí và hạng mục danh mục sản phẩm sẽ được chuyển đổi sang đơn vị tiền tệ của bảng giá mục tiêu trong quá trình sao chép. |
| Đơn vị Thời gian | Đơn vị tiền tệ của bảng giá nguồn. Mục này có thể thay đổi. | Khi mục này được thay đổi, các mục mô tả giá tạo ra cho nhân công, chi phí và hạng mục danh mục sản phẩm sẽ được chuyển đổi sang đơn vị của bảng giá mục tiêu trong quá trình sao chép. Dữ liệu chuyển đổi từ phần thiết lập đơn vị cho đơn vị thời gian bảng giá nguồn và đơn vị thời gian bảng giá mục tiêu sẽ được sử dụng. |
| Nội dung mô tả | Phần mô tả bảng giá nguồn kèm theo **- sao chép**. Đây là trường văn bản, bạn có thể có nhiều dòng mô tả về bảng giá. | Trường này được hiển thị ở các dạng xem **Được liên kết** trên bảng giá trong nhiều thực thể khác nhau có bảng giá liên quan. |

3. Lưu bảng giá. 

## <a name="update-a-price-list-by-applying-a-mark-up-to-all-the-prices"></a>Cập nhật bảng giá bằng cách áp dụng khoảng tăng cho tất cả các mức giá

1. Trên các tab **Vai trò**, **Thể loại** và **Hạng mục trong bảng giá** của bảng giá, bạn có thể chọn **Cập nhật giá** để áp dụng một mức tăng cho tất cả các mức giá trong lưới con. 
2. Trên trang hộp thoại mở ra, hãy nhập khoảng tăng. Bạn cũng có thể nhập tỷ lệ phần trăm tăng âm để giảm giá theo một tỷ lệ phần trăm nhất định. 
3. Chọn **OK** trên trang hộp thoại, sau đó xác minh rằng các mức giá trong lưới con phản ánh những thay đổi bạn đã thực hiện.


[!INCLUDE[footer-include](../includes/footer-banner.md)]