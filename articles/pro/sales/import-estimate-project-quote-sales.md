---
title: Nhập số liệu ước tính cho dự án vào phần mô tả báo giá dựa trên dự án - bản đơn giản
description: Chủ đề này cung cấp thông tin về cách nhập giá trị ước tính từ dự án vào mục mô tả báo giá.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 1c676011660cd06e49996c137f7e9dca0ef2e491
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584070"
---
# <a name="import-estimates-for-a-project-to-a-project-based-quote-line"></a>Nhập ước tính cho dự án vào mô tả báo giá dựa trên dự án 

_**Áp dụng cho:** Triển khai bản đơn giản - từ thỏa thuận đến lập hóa đơn ước giá, Project Operations cho các kịch bản dựa trên tài nguyên/không lưu kho_

Nếu một dự án được tạo trong giai đoạn trước khi bán hàng, bạn có thể chọn nhập ước tính tài chính từ dự án vào mô tả báo giá dựa trên dự án.

1. Đảm bảo rằng mô tả báo giá dựa trên dự án có thông tin dự án trong trường **Dự án**.
2. Trên tab **Chi tiết mô tả báo giá**, chọn **Nhập từ ước tính dự án**.
3. Trên trang hộp thoại mở ra, hãy chọn một trong các tùy chọn tóm tắt sau.

  - **Lớp giao dịch**
  - **Danh mục**
  - **Vai trò** 
  - **Nhiệm vụ dự án**

Dựa trên lựa chọn của bạn, ước tính từ dự án cho tất cả các lớp giao dịch bao gồm trên mô tả báo giá này được sao chép qua. Để kiểm tra những loại giao dịch nào được đưa vào, hãy chọn tab **Chung** trên mục mô tả báo giá dựa trên dự án và kiểm tra các giá trị của tùy chọn **Bao gồm thời gian**, **Bao gồm chi phí**, **Bao gồm vật tư**, và **Bao gồm phí**.  Để kiểm tra xem những nhiệm vụ nào được bao gồm, hãy chọn tab **Nhiệm vụ có thể tính phí** trên mục mô tả báo giá.

Tùy theo Nhiệm vụ được liên kết và Lớp giao dịch được bao gồm, các giá trị ước tính cho những tổ hợp nhiệm vụ và lớp giao dịch đó sẽ được nhập vào mục mô tả báo giá.

Khi bạn nhập ước tính, hệ thống sẽ mặc định giá dựa trên bảng giá dự án đính kèm với báo giá và loại thanh toán được thiết lập trên mô tả báo giá dựa trên dự án. Nếu một nhiệm vụ, vai trò hoặc danh mục được thiết lập trên mô tả báo giá dựa trên dự án là không tính phí, thì mục mô tả ước tính đã nhập sẽ được đặt là không tính phí và sẽ không cộng vào giá trị được báo giá của mục mô tả báo giá.

Khi mô tả báo giá có chi tiết mô tả, các trường **Giá trị báo giá** và **Thuế ước tính** trên mô tả báo giá được tóm tắt và không thể chỉnh sửa.

Khi có nhiều tùy chọn tóm tắt được chọn, hệ thống sẽ cố gắng tóm tắt theo tất cả các tùy chọn đã chọn. Kết quả là dữ liệu đầu ra của mục mô tả báo giá đã nhập sẽ nhiều hơn số lượng bạn có khi chỉ chọn một tùy chọn tóm tắt.

Chẳng hạn, nếu dự án có các mục mô tả giá trị ước tính sau đây cho chi phí.

| Tác vụ | Danh mục | Ngày | Số lượng | Đơn giá | Số lượng |
| --- | --- | --- | --- | --- | --- |
| Nhiệm vụ A | Vé máy bay | 10/1/2020 | 4 | 400 | 1600 |
| Nhiệm vụ B | Khách sạn | 10/1/2020 | 4 | 200 | 800 |
| Nhiệm vụ C | Khách sạn | 11/1/2020 | 2 | 200 | 400 |

Khi người dùng chọn tóm tắt theo lớp giao dịch, thông tin sau sẽ được nhập.

| Tác vụ | Danh mục | Ngày | Số lượng | Đơn giá | Số lượng |
| --- | --- | --- | --- | --- | --- |
|||10/1/2020 | 3.34 | 840 | 2800 |

Khi người dùng chọn tóm tắt theo lớp giao dịch và danh mục, thông tin sau sẽ được nhập.

| Tác vụ | Danh mục | Ngày | Số lượng | Đơn giá | Số lượng |
| --- | --- | --- | --- | --- | --- |
| Nhiệm vụ A | Vé máy bay | 10/1/2020 | 4 | 400 | 1600 |
| | Khách sạn | 10/1/2020 | 6 | 200 | 1200 |

Khi người dùng chọn tóm tắt theo Lớp giao dịch, Danh mục và Nhiệm vụ nút lá, thông tin sau sẽ được nhập. Lưu ý rằng kết quả này giống với kết quả trong dự án.

| Tác vụ | Danh mục | Ngày | Số lượng | Đơn giá | Số lượng |
| --- | --- | --- | --- | --- | --- |
| Nhiệm vụ A | Vé máy bay | 10/1/2020 | 4 | 400 | 1600 |
| Nhiệm vụ B | Khách sạn | 10/1/2020 | 4 | 200 | 800 |
| Nhiệm vụ C | Khách sạn | 11/1/2020 | 2 | 200 | 400 |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
