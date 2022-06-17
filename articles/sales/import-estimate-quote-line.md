---
title: Nhập giá trị ước tính cho một dự án vào mục mô tả báo giá dự án
description: Bài viết này cung cấp thông tin về cách nhập ước tính từ một dự án vào dòng báo giá dự án.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: dc5b6279a2123604291da35c9da2bf63dbe475b7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915072"
---
# <a name="import-estimates-for-a-project-to-a-project-quote-line"></a>Nhập giá trị ước tính cho một dự án vào mục mô tả báo giá dự án

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_


Nếu một dự án được tạo trong giai đoạn trước khi bán hàng, bạn có thể chọn nhập ước tính tài chính từ dự án vào mô tả báo giá dựa trên dự án.

1. Đảm bảo rằng mô tả báo giá dựa trên dự án có thông tin dự án trong trường **Dự án**.
2. Trên tab **Chi tiết mô tả báo giá**, chọn **Nhập từ ước tính dự án**.
3. Trên trang hộp thoại mở ra, hãy chọn một trong các tùy chọn tóm tắt sau:

  - **Lớp giao dịch**
  - **Danh mục**
  - **Vai trò** 
  - **Nhiệm vụ dự án**

Dựa trên lựa chọn của bạn, ước tính từ dự án cho tất cả các lớp giao dịch bao gồm trên mô tả báo giá này được sao chép qua. Để kiểm tra những lớp giao dịch nào được bao gồm, hãy chọn tab **Tổng quát** trên mô tả báo giá dựa trên dự án và kiểm tra các giá trị cho **Bao gồm thời gian**, **Bao gồm chi phí** và **Bao gồm phí**.

Khi bạn nhập giá trị ước tính, hệ thống sẽ lấy mặc định giá dựa trên bảng giá dự án được đính kèm với báo giá và loại thanh toán được thiết lập trên mục mô tả báo giá dựa trên dự án. Nếu một vai trò hoặc danh mục được thiết lập trên mô tả báo giá dựa trên dự án là không tính phí, thì mô tả ước tính đã nhập sẽ được đặt là không tính phí và sẽ không cộng vào giá trị được báo giá của mô tả báo giá.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
