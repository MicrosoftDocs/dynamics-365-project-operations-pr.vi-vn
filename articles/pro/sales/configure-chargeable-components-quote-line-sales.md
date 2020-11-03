---
title: Đặt cấu hình các thành phần có thể tính phí của mục mô tả báo giá
description: Chủ đề này cung cấp thông tin về cách thiết lập các thành phần có thể tính phí và không thể tính phí trên mục mô tả báo giá dựa trên dự án.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e0b64d7edb21df127bf7544f044de7f3c496dfe3
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087229"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a>Đặt cấu hình các thành phần có thể tính phí của mục mô tả báo giá

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Một mục mô tả báo giá dựa trên dự án có các thành phần *bao gồm* và thành phần *có thể tính phí*.

Các thành phần bao gồm phải tuân theo:

  - Phương thức thanh toán và phần tách của khách hàng
  - Giới hạn không vượt quá 
  - Các mục thiết đặt tần suất hóa đơn được xác định trên mục mô tả báo giá dựa trên dự án

Một tập con các thành phần bao gồm có thể được đánh dấu là có thể tính phí bằng trường **Loại thanh toán**. Trường **Loại thanh toán** là một bộ tùy chọn cho phép thiết lập các giá trị sau trong bối cảnh mục mô tả báo giá:

  - Có thể tính phí
  - Không thể tính phí

Các thành phần có thể tính phí có thể được xác định trên nhiệm vụ, vai trò và danh mục giao dịch.

Khả năng tính phí được xác định trên các nhiệm vụ cho một mục mô tả báo giá và áp dụng cho tất cả các lớp giao dịch có trong mục mô tả đó. Nếu trường **Bao gồm nhiệm vụ** được đặt thành **Toàn bộ dự án** hoặc bị để trống, thì tab **Nhiệm vụ có thể tính phí** sẽ không khả dụng.

Khả năng tính phí được xác định trên các vai trò cho một mục mô tả báo giá và chỉ áp dụng cho lớp giao dịch **Thời gian**. Nếu trường **Bao gồm thời gian** được đặt thành **Không** trên một mục mô tả báo giá dự án, thì tab **Vai trò có thể tính phí** sẽ không khả dụng.

Khả năng tính phí được xác định trên các danh mục giao dịch cho một mục mô tả báo giá và chỉ áp dụng cho lớp giao dịch **Chi phí**. Nếu trường **Bao gồm chi phí** được đặt thành **Không** trên một mục mô tả báo giá dự án, thì tab **Danh mục có thể tính phí** sẽ không khả dụng.

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a>Cập nhật nhiệm vụ dự án thành dạng có thể tính phí hoặc không thể tính phí

Một nhiệm vụ dự án có thể là dạng có thể tính phí hoặc không thể tính phí trong bối cảnh một mục mô tả báo giá dựa trên dự án cụ thể, vì vậy, các tổ hợp sau có thể được thiết lập:

Nếu mục mô tả báo giá dựa trên dự án bao gồm **Thời gian** và nhiệm vụ **T1** , thì nhiệm vụ được liên kết với mục mô tả báo giá dưới dạng có thể tính phí. Nếu có mục mô tả báo giá thứ hai bao gồm **Chi phí** , thì bạn có thể liên kết nhiệm vụ **T1** trên mục mô tả báo giá dưới dạng không thể tính phí. Kết quả là toàn bộ thời gian được ghi lại trong nhiệm vụ đều là dạng có thể tính phí và tất cả các chi phí được ghi lại trong nhiệm vụ đều là dạng không thể tính phí.

Bạn có thể đặt cấu hình loại thanh toán của nhiệm vụ trên tab **Nhiệm vụ có thể tính phí** của mục mô tả báo giá dựa trên dự án bằng cách cập nhật trường **Loại thanh toán** trên lưới con **Nhiệm vụ cho mục mô tả báo giá**. Hoặc, bạn có thể cập nhật loại thanh toán cho một nhiệm vụ dự án trong trường **Loại thanh toán** trên lưới con trên nhiệm vụ thiết lập thanh toán của một dự án hiển thị các mục mô tả báo giá được liên kết với một nhiệm vụ.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Cập nhật vai trò thành dạng có thể tính phí hoặc không thể tính phí

Một vai trò có thể là dạng có thể tính phí hoặc không thể tính phí trong bối cảnh một mục mô tả báo giá dựa trên dự án cụ thể.

Bạn có thể đặt cấu hình loại thanh toán của vai trò trên tab **Vai trò có thể tính phí** của mục mô tả báo giá bằng cách cập nhật trường **Loại thanh toán** trên lưới con **Vai trò có thể tính phí**.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Cập nhật danh mục giao dịch thành dạng có thể tính phí hoặc không thể tính phí

Một danh mục giao dịch có thể là dạng có thể tính phí hoặc không thể tính phí trên một mục mô tả báo giá cụ thể.

Bạn có thể đặt cấu hình loại thanh toán của giao dịch trên tab **Danh mục có thể tính phí** của mục mô tả báo giá bằng cách cập nhật trường **Loại thanh toán** trên lưới con **Danh mục có thể tính phí**.

### <a name="resolve-chargeability"></a>Giải quyết khả năng tính phí
Giá trị ước tính hoặc thực tế được tạo cho thời gian sẽ chỉ được coi là có thể tính phí nếu **Thời gian** được bao gồm trên mục mô tả báo giá và nếu **Nhiệm vụ** , **Vai trò** được đặt cấu hình là có thể tính phí trên mục mô tả báo giá.

Giá trị ước tính hoặc thực tế được tạo cho chi phí sẽ chỉ được coi là có thể tính phí nếu **Chi phí** được bao gồm trên mục mô tả báo giá và nếu **Nhiệm vụ** , **Danh mục giao dịch** được đặt cấu hình là có thể tính phí trên mục mô tả báo giá.

| Bao gồm thời gian | Bao gồm chi phí | Các tác vụ được đưa vào | Vai trò | Danh mục | Tác vụ | Thanh toán |
| --- | --- | --- | --- | --- | --- | --- |
| Có | Có | Toàn bộ dự án | Có thể tính phí | Có thể tính phí | Không thể đặt | Thanh toán theo giá trị thời gian thực tế: Có thể tính phí </br>Loại thanh toán theo giá trị chi phí thực tế: Có thể tính phí |
| Có | Có | Chỉ các tác vụ được chọn | Có thể tính phí | Có thể tính phí | Có thể tính phí | Thanh toán theo giá trị thời gian thực tế: Có thể tính phí</br>Loại thanh toán theo giá trị chi phí thực tế: Có thể tính phí |
| Có | Có | Chỉ các tác vụ được chọn | Không thể tính phí | Có thể tính phí | Có thể tính phí | Thanh toán theo giá trị thời gian thực tế: Không thể tính phí</br>Loại thanh toán theo giá trị chi phí thực tế: Có thể tính phí |
| Có | Có | Chỉ các tác vụ được chọn | Có thể tính phí | Có thể tính phí | Không thể tính phí | Thanh toán theo giá trị thời gian thực tế: Không thể tính phí</br> Loại thanh toán theo giá trị chi phí thực tế: Không thể tính phí |
| Có | Có | Chỉ các tác vụ được chọn | Không thể tính phí | Có thể tính phí | Không thể tính phí | Thanh toán theo giá trị thời gian thực tế: Không thể tính phí</br> Loại thanh toán theo giá trị chi phí thực tế: Không thể tính phí |
| Có | Có | Chỉ các tác vụ được chọn | Không thể tính phí | Không thể tính phí | Có thể tính phí | Thanh toán theo giá trị thời gian thực tế: Không thể tính phí</br> Loại thanh toán theo giá trị chi phí thực tế: Không thể tính phí |
| No | Có | Toàn bộ dự án | Không thể đặt | Có thể tính phí | Không thể đặt | Thanh toán theo giá trị thời gian thực tế: Không khả dụng </br>Loại thanh toán theo giá trị chi phí thực tế: Có thể tính phí |
| No | Có | Toàn bộ dự án | Không thể đặt | Không thể tính phí | Không thể đặt | Thanh toán theo giá trị thời gian thực tế: Không khả dụng </br>Loại thanh toán theo giá trị chi phí thực tế: Không thể tính phí |
| Có | No | Toàn bộ dự án | Có thể tính phí | Không thể đặt | Không thể đặt | Thanh toán theo giá trị thời gian thực tế: Có thể tính phí</br>Loại thanh toán theo giá trị chi phí thực tế: Không khả dụng |
| Có | No | Toàn bộ dự án | Không thể tính phí | Không thể đặt | Không thể đặt | Thanh toán theo giá trị thời gian thực tế: Không thể tính phí </br>Loại thanh toán theo giá trị chi phí thực tế: Không khả dụng |
