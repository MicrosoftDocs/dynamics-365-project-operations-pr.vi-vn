---
title: Xác định giá bán cho các ước tính và thực tế của dự án
description: Bài viết này cung cấp thông tin về cách xác định giá bán cho các ước tính và thực tế của dự án.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 6504302578d1eb3d00c717ea93cd4c4212acb4e7
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410170"
---
# <a name="determine-sales-prices-for-project-estimates-and-actuals"></a>Xác định giá bán cho các ước tính và thực tế của dự án

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Để xác định giá bán trên ước tính và thực tế trong Microsoft Dynamics 365 Project Operations, trước tiên hệ thống sử dụng ngày và đơn vị tiền tệ trong ước tính đến hoặc ngữ cảnh thực tế để xác định bảng giá bán hàng. Trong ngữ cảnh thực tế cụ thể, hệ thống sử dụng **Ngày Giao dịch** trường để xác định bảng giá có thể áp dụng. Sau khi bảng giá bán hàng được xác định, hệ thống sẽ xác định tỷ lệ bán hàng hoặc hóa đơn.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-time"></a>Xác định tỷ lệ bán hàng trên các dòng thực tế và ước tính cho Thời gian

Ước tính ngữ cảnh cho **Thời gian** đề cập đến:

- Trích dẫn chi tiết dòng cho **Thời gian**.
- Chi tiết dòng hợp đồng cho **Thời gian**.
- Phân công tài nguyên trong một dự án.

Bối cảnh thực tế cho **Thời gian** đề cập đến:

- Nhập và sửa dòng tạp chí cho **Thời gian**.
- Các dòng nhật ký được tạo khi gửi một mục thời gian.
- Chi tiết dòng hóa đơn cho **Thời gian**. 

Sau khi xác định được bảng giá bán hàng, hệ thống sẽ hoàn tất các bước sau để nhập giá hóa đơn mặc định.

1. Hệ thống phù hợp với sự kết hợp của **Vai diễn** và **Đơn vị cung ứng** các trường trong ngữ cảnh ước tính hoặc thực tế cho **Thời gian** chống lại các đường giá vai trò trên bảng giá. Sự phù hợp này giả định rằng bạn đang sử dụng các thứ nguyên đặt giá ngoài hộp cho giá hóa đơn. Nếu bạn đã định cấu hình giá để nó dựa trên các trường khác ngoài hoặc ngoài **Vai diễn** và **Đơn vị cung ứng**, tổ hợp các trường đó được sử dụng để truy xuất đường giá phù hợp với vai trò.
1. Nếu hệ thống tìm thấy một dòng giá vai trò có tỷ lệ thanh toán cho **Vai diễn** và **Đơn vị cung ứng** kết hợp, tỷ giá hóa đơn đó được sử dụng làm tỷ giá hóa đơn mặc định.
1. Nếu hệ thống không thể khớp với **Vai diễn** và **Đơn vị cung ứng** giá trị, nó truy xuất các đường giá vai trò có các giá trị phù hợp cho **Vai diễn** trường trừ các giá trị rỗng cho **Đơn vị tài nguyên** đồng ruộng. Sau khi hệ thống tìm thấy một bản ghi giá vai trò phù hợp, giá hóa đơn từ bản ghi đó sẽ được sử dụng làm giá hóa đơn mặc định. Sự kết hợp này giả định một cấu hình out-of-box cho mức độ ưu tiên tương đối của **Vai diễn** đấu với **Đơn vị cung ứng** như một thứ nguyên định giá bán hàng.

> [!NOTE]
> Nếu bạn định cấu hình một mức độ ưu tiên khác của **Vai diễn** và **Đơn vị cung ứng** hoặc nếu bạn có các thứ nguyên khác có mức độ ưu tiên cao hơn, hành vi trước đó sẽ thay đổi tương ứng. Hệ thống truy xuất bản ghi giá vai trò có giá trị phù hợp với từng giá trị thứ nguyên đặt giá theo thứ tự ưu tiên. Các hàng có giá trị null cho các thứ nguyên đó đứng cuối cùng.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Xác định tỷ lệ bán hàng trên các dòng thực tế và ước tính Chi phí

Ước tính ngữ cảnh cho **Chi phí** đề cập đến:

- Trích dẫn chi tiết dòng cho **Chi phí**.
- Chi tiết dòng hợp đồng cho **Chi phí**.
- Dòng dự toán chi phí trên một dự án.

Bối cảnh thực tế cho **Chi phí** đề cập đến:

- Nhập và sửa dòng tạp chí cho **Chi phí**.
- Các dòng nhật ký được tạo khi gửi một mục chi phí.
- Chi tiết dòng hóa đơn cho **Chi phí**. 

Sau khi xác định được bảng giá bán hàng, hệ thống hoàn tất các bước sau để nhập đơn giá bán hàng mặc định.

1. Hệ thống phù hợp với sự kết hợp của **Loại** và **Đơn vị** các trường trên dòng ước tính cho **Chi phí** so với các dòng giá thể loại trên bảng giá.
1. Nếu hệ thống tìm thấy dòng giá danh mục có tỷ lệ bán hàng cho **Loại** và **Đơn vị** kết hợp, tỷ lệ bán hàng đó được sử dụng làm tỷ lệ bán hàng mặc định.
1. Nếu hệ thống tìm thấy đường giá danh mục phù hợp, thì phương pháp đặt giá có thể được sử dụng để nhập giá bán mặc định. Bảng sau đây cho thấy hành vi mặc định đối với giá chi phí trong Hoạt động dự án.

    | Ngữ cảnh | Phương pháp định giá | Giá mặc định |
    | --- | --- | --- |
    | Ước tính | Đơn giá | Dựa trên dòng giá danh mục. |
    |        | Tại mức chi phí | 0.00 |
    |        | Tăng cao hơn chi phí | 0.00 |
    | Thực tế | Đơn giá | Dựa trên dòng giá danh mục. |
    |        | Tại mức chi phí | Căn cứ vào chi phí thực tế có liên quan. |
    |        | Tăng cao hơn chi phí | Một đánh dấu được áp dụng, như được xác định bởi đường giá danh mục, cho tỷ lệ chi phí đơn vị của chi phí thực tế có liên quan. |

1. Nếu hệ thống không thể khớp với **Loại** và **Đơn vị** giá trị, tỷ lệ bán hàng được đặt thành **0** (không) theo mặc định.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-material"></a>Xác định tỷ lệ bán hàng trên các dòng thực tế và ước tính cho Vật liệu

Ước tính ngữ cảnh cho **Vật chất** đề cập đến:

- Trích dẫn chi tiết dòng cho **Vật chất**.
- Chi tiết dòng hợp đồng cho **Vật chất**.
- Các đường ước tính vật liệu trên một dự án.

Bối cảnh thực tế cho **Vật chất** đề cập đến:

- Nhập và sửa dòng tạp chí cho **Vật chất**.
- Các dòng nhật ký được tạo khi gửi nhật ký sử dụng Nguyên liệu.
- Chi tiết dòng hóa đơn cho **Vật chất**. 

Sau khi xác định được bảng giá bán hàng, hệ thống hoàn tất các bước sau để nhập đơn giá bán hàng mặc định.

1. Hệ thống phù hợp với sự kết hợp của **Sản phẩm** và **Đơn vị** các trường trên dòng ước tính cho **Vật chất** so với các dòng mục của bảng giá trên bảng giá.
1. Nếu hệ thống tìm thấy một dòng mục trong danh sách giá có tỷ lệ bán hàng cho **Sản phẩm** và **Đơn vị** kết hợp và nếu phương pháp định giá là **Lượng ngoại tệ**, giá bán được chỉ định trên dòng bảng giá được sử dụng. 
1. Nếu **Sản phẩm** và **Đơn vị** các giá trị trường không khớp hoặc nếu phương pháp đặt giá khác với **Lượng ngoại tệ**, tỷ lệ bán hàng được đặt thành **0** (không) theo mặc định. Hành vi này xảy ra bởi vì Hoạt động Dự án chỉ hỗ trợ **Lượng ngoại tệ** phương pháp định giá cho các vật liệu được sử dụng trong một dự án.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
