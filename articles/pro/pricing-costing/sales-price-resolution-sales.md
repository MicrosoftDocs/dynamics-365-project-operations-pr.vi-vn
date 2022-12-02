---
title: Xác định giá bán hàng cho số liệu thực tế và ước tính của dự án
description: Bài viết này cung cấp thông tin về cách xác định giá bán cho giá trị thực tế và ước tính của dự án.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 1288a571d50604ee400db9c16822719d0649628b
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475211"
---
# <a name="determine-sales-prices-for-project-estimates-and-actuals"></a>Xác định giá bán hàng cho số liệu thực tế và ước tính của dự án

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Để quyết định giá bán trên ước tính và số liệu thực tế được trong Microsoft Dynamics 365 Project Operations, hệ thống trước tiên sử dụng ngày và đơn vị tiền tệ trong ước tính sắp tới hoặc ngữ cảnh thực tế để xác định bảng giá bán hàng trước tiên. Trong ngữ cảnh thực tế cụ thể, hệ thống sử dụng trường **Ngày giao dịch** để xác định bảng giá nào được áp dụng. Giá trị **Ngày giao dịch** của ước tính sắp đến hoặc số liệu thực tế được so sánh với các giá trị **Ngày bắt đầu có hiệu lực (Độc lập về múi giờ)** và **Ngày kết thúc hiệu lực (Độc lập về múi giờ)** trên bảng giá. Sau khi quyết định xong bảng giá bán hàng, hệ thống sẽ quyết định tỷ lệ bán hàng hoặc tỷ lệ hóa đơn.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-time"></a>Quyết định tỷ lệ bán hàng trên mô tả thực tế và ước tính cho Thời gian

Ước tính ngữ cảnh cho **Thời gian** đề cập đến:

- Chi tiết mô tả báo giá cho **Thời gian**.
- Chi tiết mô tả hợp đồng cho **Thời gian**.
- Phân công nguồn lực trên dự án.

Ngữ cảnh thực tế cho **Thời gian** đề cập đến:

- Dòng nhật ký kế toán Mục nhập và Chỉnh sửa cho **Thời gian**.
- Các dòng nhật ký kế toán được tạo khi mục nhập thời gian được gửi.
- Chi tiết mô tả hóa đơn cho **Thời gian**. 

Sau khi quyết định bảng giá bán hàng, hệ thống sẽ hoàn tất các bước sau để nhập tỷ lệ hóa đơn mặc định.

1. Hệ thống khớp các trường **Vai trò**, **Đơn vị nguồn lực** và trong ước tính hoặc ngữ cảnh thực tế cho **Thời gian** dựa trên mô tả giá theo vai trò trên bảng giá. Trùng khớp này giả định rằng bạn đang sử dụng các thông số giá có sẵn cho tỷ lệ hóa đơn. Nếu bạn đã đặt cấu hình giá sao cho nó dựa trên bất kỳ trường nào khác thay vì hoặc ngoài **Vai trò** và **Đơn vị nguồn lực**, thì kết hợp các trường đó sẽ được sử dụng để truy xuất mô tả giá theo vai trò phù hợp.
1. Nếu hệ thống tìm thấy một mô tả giá theo vai trò có tỷ lệ hóa đơn cho kết hợp **Vai trò** và **Đơn vị nguồn lực**, thì tỷ lệ hóa đơn được sử dụng làm tỷ lệ hóa đơn mặc định.
1. Nếu hệ thống không thể khớp với các giá trị trường **Vai trò**, **Đơn vị nguồn lực**, hệ thống sẽ truy xuất các dòng giá vai trò có giá trị khớp cho trường **Vai trò** nhưng giá trị rỗng cho trường **Đơn vị nguồn lực**. Sau khi tìm thấy một bản ghi giá theo vai trò phù hợp, tỷ lệ hóa đơn từ bản ghi đó sẽ được sử dụng làm tỷ lệ hóa đơn mặc định. Giá trị trùng khớp này giả định một cấu hình có sẵn cho mức độ ưu tiên tương đối của **Vai trò** so với **Đơn vị nguồn lực** là thông số giá bán hàng.

> [!NOTE]
> Nếu bạn đặt cấu hình mức độ ưu tiên khác cho các trường **Vai trò** và **Đơn vị nguồn lực** hoặc nếu bạn có các thông số khác có mức độ ưu tiên cao hơn, thì hành vi liền trước này sẽ thay đổi tương ứng. Hệ thống truy xuất các bản ghi giá vai trò có giá trị phù hợp với từng giá trị thứ nguyên về giá theo thứ tự ưu tiên. Các hàng có giá trị rỗng cho các thứ nguyên đó đứng cuối cùng.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Quyết định tỷ lệ bán hàng trên mô tả thực tế và ước tính cho Chi phí

Ước tính ngữ cảnh cho **Chi phí** đề cập đến:

- Chi tiết mô tả báo giá cho **Chi phí**.
- Chi tiết mô tả hợp đồng cho **Chi phí**.
- Mô tả ước tính chi phí trên dự án.

Ngữ cảnh ước tính cho **Chi phí** đề cập đến:

- Dòng nhật ký kế toán Mục nhập và Chỉnh sửa cho **Chi phí**.
- Các dòng nhật ký kế toán được tạo khi mục nhập chi phí được gửi.
- Chi tiết mô tả hóa đơn cho **Chi phí**. 

Sau khi quyết định bảng giá bán hàng, hệ thống sẽ hoàn tất các bước sau để nhập đơn giá bán mặc định.

1. Hệ thống khớp kết hợp giữa các trường **Danh mục** và **Đơn vị** trên mô tả ước tính cho **Chi phí** để đối chiếu với mô tả giá theo danh mục trên bảng giá.
1. Nếu hệ thống tìm thấy một mô tả giá theo danh mục có tỷ lệ bán hàng cho kết hợp trường **Danh mục** và **Đơn vị**, thì tỷ lệ bán hàng được sử dụng làm tỷ lệ bán hàng mặc định.
1. Nếu hệ thống tìm thấy mô tả giá theo danh mục phù hợp, phương pháp định giá có thể được sử dụng để nhập giá bán mặc định. Bảng sau đây cho thấy hành vi mặc định cho giá chi phí trong Project Operations.

    | Ngữ cảnh | Phương pháp định giá | Giá mặc định |
    | --- | --- | --- |
    | Ước tính | Đơn giá | Dựa trên mô tả giá theo danh mục. |
    |        | Tại mức chi phí | 0.00 |
    |        | Tăng cao hơn chi phí | 0.00 |
    | Thực tế | Đơn giá | Dựa trên mô tả giá theo danh mục. |
    |        | Tại mức chi phí | Dựa trên chi phí thực tế liên quan. |
    |        | Tăng cao hơn chi phí | Một mức tăng được áp dụng, như được xác định bởi mô tả giá theo danh mục , vào tỷ lệ chi phí đơn vị của chi phí thực tế liên quan. |

1. Nếu hệ thống không thể đối chiếu các giá trị trường **Danh mục** và **Đơn vị**, thì tỷ lệ bán hàng được đặt về **0** (không) theo mặc định.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-material"></a>Quyết định tỷ lệ doanh số trên dòng giá trị thực tế và giá trị ước tính cho Vật tư

Ước tính ngữ cảnh cho **Vật tư** đề cập đến:

- Chi tiết mô tả báo giá cho **Vật tư**.
- Chi tiết mô tả hợp đồng cho **Vật tư**.
- Mô tả ước tính vật tư trên dự án.

Ngữ cảnh ước tính cho **Vật tư** đề cập đến:

- Dòng nhật ký kế toán Mục nhập và Chỉnh sửa cho **Vật tư**.
- Các dòng nhật ký kế toán được tạo khi Nhật ký sử dụng vật tư được gửi.
- Chi tiết mô tả hóa đơn cho **Vật tư**. 

Sau khi quyết định bảng giá bán hàng, hệ thống sẽ hoàn tất các bước sau để nhập đơn giá bán mặc định.

1. Hệ thống khớp kết hợp các trường **Sản phẩm** và **Đơn vị** trên dòng ước tính cho **Vật tư** để khớp các dòng hạng mục trong bảng giá trong bảng giá.
1. Nếu hệ thống tìm thấy một dòng hạng mục trong bảng giá có tỷ lệ doanh số cho tổ hợp trường **Sản phẩm** và **Đơn vị** và nếu phương pháp định giá là **Số tiền theo loại tiền**, thì giá bán sẽ được nêu rõ trên dòng bảng giá được sử dụng. 
1. Nếu các giá trị trường **Sản phẩm** và **Đơn vị** không khớp, hoặc nếu phương pháp giá khác với **Số tiền theo loại tiền**, tỷ lệ doanh số được đặt thành **0** (không) theo mặc định. Hành vi này xảy ra bởi vì Project Operations chỉ hỗ trợ phương pháp giá **Số tiền theo loại tiền** cho các vật tư được sử dụng trong một dự án.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
