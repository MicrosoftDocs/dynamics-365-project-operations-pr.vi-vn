---
title: Nhập giá trị ước tính vào mục mô tả hợp đồng dựa trên dự án
description: Chủ đề này cung cấp thông tin về cách nhập giá trị ước tính từ dự án vào mục mô tả hợp đồng.
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ea513ca8126eadbf563f3c6cb3e966f81703ae805d12881f865cdc1dd77e191d
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/06/2021
ms.locfileid: "6990117"
---
# <a name="import-an-estimate-to-a-project-based-contract-line"></a>Nhập giá trị ước tính vào mục mô tả hợp đồng dựa trên dự án

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Trong Dynamics 365 Project Operations, bạn có thể nhập ước tính từ một dự án vào mô tả hợp đồng theo dự án.

1. Xác minh rằng trường **Dự án** được điền trên mục mô tả hợp đồng dựa trên dự án.
2. Trên tab **Chi tiết mô tả hợp đồng**, hãy chọn **Nhập từ ước tính dự án**. Trang hộp thoại với các tùy chọn tóm tắt sẽ mở ra. Các tùy chọn tóm tắt có sẵn là: **Lớp giao dịch**, **Danh mục**, **Vai trò** và **Nhiệm vụ dự án**. Dựa trên sự lựa chọn tóm tắt, giá trị ước tính từ dự án cho tất cả các lớp giao dịch có trong mục mô tả hợp đồng này sẽ được sao chép. 
3. Để kiểm tra những lớp giao dịch nào được bao gồm, trên tab **Tổng quát** của mục mô tả hợp đồng dựa trên dự án, hãy kiểm tra giá trị trong các trường **Bao gồm thời gian**, **Bao gồm chi phí** và **Bao gồm phí**.

Khi bạn nhập giá trị ước tính, ứng dụng sẽ lấy mặc định giá dựa trên bảng giá dự án được đính kèm với hợp đồng và loại thanh toán được thiết lập trên mục mô tả hợp đồng. Nếu một vai trò hoặc danh mục được thiết lập trên mục mô tả hợp đồng là không thể tính phí, thì mục mô tả ước tính đã nhập cho vai trò hoặc danh mục đó sẽ là dạng không thể tính phí và sẽ không cộng vào giá trị theo hợp đồng của mục mô tả hợp đồng.

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
| &nbsp;  | &nbsp;  | 10/1/2020 | 3.34 | 840 | 2800 |

Khi người dùng chọn tóm tắt theo **Lớp giao dịch** và **Danh mục**, thông tin sau sẽ được nhập:

| Tác vụ | Danh mục | Ngày | Số lượng | Đơn giá | Số lượng |
| --- | --- | --- | --- | --- | --- |
| Nhiệm vụ A | Vé máy bay | 10/1/2020 | 4 | 400 | 1600 |
| &nbsp;  | Khách sạn | 10/1/2020 | 6 | 200 | 1200 |

Khi người dùng chọn tóm tắt theo **Lớp giao dịch**, **Danh mục** và **Nhiệm vụ nút lá**, thông tin sau sẽ được nhập. Xin lưu ý rằng kết quả này giống như những gì có trên dự án:

| Tác vụ | Danh mục | Ngày | Số lượng | Đơn giá | Số lượng |
| --- | --- | --- | --- | --- | --- |
| Nhiệm vụ A | Vé máy bay | 10/1/2020 | 4 | 400 | 1600 |
| Nhiệm vụ B | Khách sạn | 10/1/2020 | 4 | 200 | 800 |
| Nhiệm vụ C | Khách sạn | 11/1/2020 | 2 | 200 | 400 |


[!INCLUDE[footer-include](../includes/footer-banner.md)]