---
title: Nhập số liệu ước tính vào phần mô tả hợp đồng dựa trên dự án - bản đơn giản
description: Bài viết này cung cấp thông tin về việc nhập giá trị ước tính tài chính từ dự án vào mục mô tả hợp đồng.
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d6e3bdfeb1ea9de32d6712ac5671be39c243702a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924226"
---
# <a name="import-an-estimate-to-a-project-based-contract-line---lite"></a>Nhập số liệu ước tính vào phần mô tả hợp đồng dựa trên dự án - bản đơn giản

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Trong Dynamics 365 Project Operations, bạn có thể nhập ước tính từ một dự án vào mô tả hợp đồng theo dự án.

1. Xác minh rằng trường **Dự án** đã được điền trên mục mô tả hợp đồng dựa trên dự án.
2. Trên tab **Chi tiết mô tả hợp đồng**, hãy chọn **Nhập từ ước tính dự án**. Trang hộp thoại với các tùy chọn tóm tắt sẽ mở ra. Các tùy chọn tóm tắt có sẵn là: **Lớp giao dịch**, **Danh mục**, **Vai trò** và **Nhiệm vụ dự án**.
3. Dựa trên sự lựa chọn tóm tắt, giá trị ước tính từ dự án cho tất cả các lớp giao dịch và nhiệm vụ có trong mục mô tả hợp đồng này sẽ được sao chép. Để kiểm tra những lớp giao dịch nào được bao gồm, trên tab **Tổng quát** ở mục mô tả hợp đồng dựa trên dự án, hãy kiểm tra giá trị trong các trường **Bao gồm thời gian**, **Bao gồm chi phí** và **Bao gồm phí**. 
4. Để xem những nhiệm vụ nào được bao gồm, hãy chọn tab **Nhiệm vụ có thể tính phí** trên mục mô tả hợp đồng. Dựa trên các nhiệm vụ được liên kết có trường **Lớp giao dịch được bao gồm** được đặt thành **Có**, tất cả các giá trị ước tính cho những tổ hợp nhiệm vụ và lớp giao dịch đó sẽ được nhập vào mục mô tả hợp đồng.

Khi bạn nhập giá trị ước tính, hệ thống sẽ lấy mặc định giá dựa trên bảng giá dự án được đính kèm với hợp đồng và loại thanh toán được thiết lập trên mục mô tả hợp đồng. Nếu một nhiệm vụ, vai trò hoặc danh mục được thiết lập trên mục mô tả hợp đồng là không thể tính phí, thì mục mô tả ước tính đã nhập sẽ là dạng không thể tính phí và sẽ không cộng vào giá trị theo hợp đồng của mục mô tả hợp đồng.

Khi mục mô tả hợp đồng có chi tiết mô tả, các trường **Giá trị hợp đồng** và **Thuế ước tính** trên mục mô tả hợp đồng được tóm tắt và không thể chỉnh sửa.

Khi có nhiều tùy chọn tóm tắt được chọn, hệ thống sẽ cố gắng tóm tắt theo tất cả các tùy chọn đã chọn. Kết quả tóm tắt sẽ tạo ra nhiều mục mô tả hợp đồng được nhập hơn nếu bạn chỉ chọn một tùy chọn tóm tắt.

Chẳng hạn, nếu dự án có các mục mô tả giá trị ước tính sau đây cho chi phí:

| Tác vụ | Danh mục | Ngày | Số lượng | Đơn giá | Số lượng |
| --- | --- | --- | --- | --- | --- |
| Nhiệm vụ A | Vé máy bay | 10/1/2020 | 4 | 400 | 1600 |
| Nhiệm vụ B | Khách sạn | 10/1/2020 | 4 | 200 | 800 |
| Nhiệm vụ C | Khách sạn | 11/1/2020 | 2 | 200 | 400 |

Khi người dùng chọn tóm tắt theo **Lớp giao dịch**, thông tin sau sẽ được nhập:

| Tác vụ | Danh mục | Ngày | Số lượng | Đơn giá | Số lượng |
| --- | --- | --- | --- | --- | --- |
| &nbsp; | &nbsp; | 10/1/2020 | 3.34 | 840 | 2800 |

Khi người dùng chọn tóm tắt theo **Lớp giao dịch** và **Danh mục**, thông tin sau sẽ được nhập:

| Tác vụ | Danh mục | Ngày | Số lượng | Đơn giá | Số lượng |
| --- | --- | --- | --- | --- | --- |
| Nhiệm vụ A | Vé máy bay | 10/1/2020 | 4 | 400 | 1600 |
| &nbsp;| Khách sạn | 10/1/2020 | 6 | 200 | 1200 |

Khi người dùng chọn tóm tắt theo **Lớp giao dịch**, **Danh mục** và **Nhiệm vụ nút lá**, thông tin sau sẽ được nhập. Xin lưu ý rằng kết quả này giống như những gì có trên dự án:

| Tác vụ | Danh mục | Ngày | Số lượng | Đơn giá | Số lượng |
| --- | --- | --- | --- | --- | --- |
| Nhiệm vụ A | Vé máy bay | 10/1/2020 | 4 | 400 | 1600 |
| Nhiệm vụ B | Khách sạn | 10/1/2020 | 4 | 200 | 800 |
| Nhiệm vụ C | Khách sạn | 11/1/2020 | 2 | 200 | 400 |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]