---
title: Nhập ước tính cho dự án vào mô tả báo giá dựa trên dự án
description: Chủ đề này cung cấp thông tin về cách nhập ước tính từ dự án vào mô tả báo giá.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 75511f0d7ef1d2d1b3bf5cc598a8f51d0c553939
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908733"
---
# <a name="import-estimates-for-a-project-to-a-project-based-quote-line"></a>Nhập ước tính cho dự án vào mô tả báo giá dựa trên dự án

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_


Nếu một dự án được tạo trong giai đoạn trước khi bán hàng, bạn có thể chọn nhập ước tính tài chính từ dự án vào mô tả báo giá dựa trên dự án.

1. Đảm bảo rằng mô tả báo giá dựa trên dự án có thông tin dự án trong trường **Dự án**.
2. Trên tab **Chi tiết mô tả báo giá**, chọn **Nhập từ ước tính dự án**.
3. Trên trang hộp thoại mở ra, hãy chọn một trong các tùy chọn tóm tắt sau.

  - **Lớp giao dịch**
  - **Danh mục**
  - **Vai trò** 
  - **Nhiệm vụ dự án**

Dựa trên lựa chọn của bạn, ước tính từ dự án cho tất cả các lớp giao dịch bao gồm trên mô tả báo giá này được sao chép qua. Để kiểm tra những lớp giao dịch nào được bao gồm, hãy chọn tab **Tổng quát** trên mô tả báo giá dựa trên dự án và kiểm tra các giá trị cho **Bao gồm thời gian**, **Bao gồm chi phí** và **Bao gồm phí**.

Khi bạn nhập ước tính, hệ thống sẽ mặc định giá dựa trên bảng giá dự án đính kèm với báo giá và loại thanh toán được thiết lập trên mô tả báo giá dựa trên dự án. Nếu một vai trò hoặc danh mục được thiết lập trên mô tả báo giá dựa trên dự án là không tính phí, thì mô tả ước tính đã nhập sẽ được đặt là không tính phí và sẽ không cộng vào giá trị được báo giá của mô tả báo giá.

Khi mô tả báo giá có chi tiết mô tả, các trường **Giá trị báo giá** và **Thuế ước tính** trên mô tả báo giá được tóm tắt và không thể chỉnh sửa.

Khi nhiều tùy chọn tóm tắt được chọn, chức năng tóm tắt sẽ cố gắng tóm tắt theo tất cả các tùy chọn đã chọn. Điều này có nghĩa là đầu ra của mô tả báo giá đã nhập sẽ nhiều hơn so với việc bạn chỉ chọn một tùy chọn tóm tắt.

Ví dụ: Nếu dự án có các mô tả ước tính chi phí sau đây.

| Tác vụ | Danh mục | Ngày | Số lượng | Đơn giá | Số lượng |
| --- | --- | --- | --- | --- | --- |
| Nhiệm vụ A | Vé máy bay | 10/1/2020 | 4 | 400 | 1600 |
| Nhiệm vụ B | Khách sạn | 10/1/2020 | 4 | 200 | 800 |
| Nhiệm vụ C | Khách sạn | 11/1/2020 | 2 | 200 | 400 |

Khi người dùng chọn tóm tắt theo lớp giao dịch, thông tin sau sẽ được nhập.

| Tác vụ | Danh mục | Ngày | Số lượng | Đơn giá | Số lượng |
| --- | --- | --- | --- | --- | --- |
| | | 10/1/2020 | 3.34 | 840 | 2800 |

Khi người dùng chọn tóm tắt theo lớp giao dịch và danh mục, thông tin sau sẽ được nhập.

| Tác vụ | Danh mục | Ngày | Số lượng | Đơn giá | Số lượng |
| --- | --- | --- | --- | --- | --- |
| Nhiệm vụ A | Vé máy bay | 10/1/2020 | 4 | 400 | 1600 |
| | Khách sạn | 10/1/2020 | 6 | 200 | 1200 |

Khi người dùng chọn tóm tắt theo lớp giao dịch, danh mục và nhiệm vụ nút lá, thông tin sau sẽ được nhập. Lưu ý rằng kết quả này giống với kết quả trong dự án.

| Tác vụ | Danh mục | Ngày | Số lượng | Đơn giá | Số lượng |
| --- | --- | --- | --- | --- | --- |
| Nhiệm vụ A | Vé máy bay | 10/1/2020 | 4 | 400 | 1600 |
| Nhiệm vụ B | Khách sạn | 10/1/2020 | 4 | 200 | 800 |
| Nhiệm vụ C | Khách sạn | 11/1/2020 | 2 | 200 | 400 |