---
title: Đặt cấu hình các thành phần có thể tính phí của mô tả hợp đồng dựa trên dự án - bản đơn giản
description: Chủ đề này cung cấp thông tin về cách thêm các thành phần có thể tính phí vào mục mô tả hợp đồng trong Hoạt động Dự án.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b881e03a2bb085c6d7cfccb7eec70442e696e62c
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 11/12/2020
ms.locfileid: "4513905"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line---lite"></a>Đặt cấu hình các thành phần có thể tính phí của mô tả hợp đồng dựa trên dự án - bản đơn giản

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Một mục mô tả hợp đồng dựa trên dự án có các thành phần *bao gồm* và thành phần *có thể tính phí*.

Thành phần bao gồm là các thành phần phải tuân theo:

  - Phương thức thanh toán và phần tách của khách hàng
  - Giới hạn không vượt quá 
  - Các mục thiết đặt tần suất hóa đơn được xác định trên mục mô tả hợp đồng dựa trên dự án

Một tập con các thành phần bao gồm có thể được đánh dấu là có thể tính phí bằng trường **Loại thanh toán**. Trường **Loại thanh toán** là một bộ tùy chọn cho phép thiết lập các giá trị sau trong bối cảnh mục mô tả hợp đồng:

  - Có thể tính phí
  - Không thể tính phí

Các thành phần có thể tính phí có thể được xác định trên nhiệm vụ, vai trò và danh mục giao dịch.

Khả năng tính phí được xác định trên các nhiệm vụ cho một mục mô tả hợp đồng dự án và áp dụng cho tất cả các lớp giao dịch có trong mục mô tả này. Nếu trường **Bao gồm nhiệm vụ** trên một mục mô tả hợp đồng bị để trống hoặc được đặt thành **Toàn bộ dự án**, thì tab **Nhiệm vụ có thể tính phí** sẽ không khả dụng.

Khả năng tính phí được xác định trên các vai trò cho một mục mô tả hợp đồng dự án và chỉ áp dụng cho lớp giao dịch **Thời gian**. Nếu trường **Bao gồm thời gian** trên một mục mô tả hợp đồng dự án được đặt thành **Không**, thì tab **Vai trò có thể tính phí** sẽ không khả dụng.

Khả năng tính phí được xác định trên các danh mục giao dịch cho một mục mô tả hợp đồng dự án và chỉ áp dụng cho lớp giao dịch **Chi phí**. Nếu trường **Bao gồm chi phí** được đặt thành **Không**, thì tab **Danh mục có thể tính phí** sẽ không khả dụng.

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a>Cập nhật nhiệm vụ dự án thành dạng có thể tính phí hoặc không thể tính phí

Một nhiệm vụ dự án có thể là dạng có thể tính phí hoặc không thể tính phí trên một mục mô tả hợp đồng cụ thể, vì vậy, có thể có các cách thiết lập sau đây:

Nếu một mục mô tả hợp đồng dựa trên dự án có **Thời gian** và một nhiệm vụ nhất định, thì **T1** sẽ được liên kết với mục đó dưới dạng có thể tính phí. Nếu có mục mô tả hợp đồng thứ hai bao gồm **Chi phí**, thì bạn có thể liên kết nhiệm vụ T1 trên mục mô tả hợp đồng dưới dạng không thể tính phí. Kết quả là toàn bộ thời gian được ghi lại trong nhiệm vụ đều là dạng có thể tính phí và tất cả các chi phí là dạng không thể tính phí.

Loại thanh toán của nhiệm vụ có thể được đặt cấu hình trên tab **Nhiệm vụ có thể tính phí** của mô tả hợp đồng bằng cách cập nhật trường **Loại thanh toán** trên lưới con nhiệm vụ trong mô tả hợp đồng. Ngoài ra, bạn có thể cập nhật trường **Loại thanh toán** trên lưới con của nhiệm vụ Thiết lập thanh toán trong một dự án hiển thị mô tả hợp đồng được liên kết với một nhiệm vụ.

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a>Cập nhật vai trò thành dạng có thể tính phí hoặc không thể tính phí

Một vai trò có thể là dạng có thể tính phí hoặc không thể tính phí trên một mục mô tả hợp đồng cụ thể.

Bạn có thể đặt cấu hình loại thanh toán của một vai trò trên tab **Vai trò có thể tính phí** của mục mô tả hợp đồng. Để làm điều này, hãy cập nhật trường **Loại thanh toán** trên lưới con **Vai trò có thể tính phí**.

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a>Cập nhật danh mục giao dịch thành dạng có thể tính phí hoặc không thể tính phí

Một danh mục giao dịch có thể là dạng có thể tính phí hoặc không thể tính phí trên một mục mô tả hợp đồng cụ thể.

Bạn có thể đặt cấu hình loại thanh toán của một giao dịch trên tab **Danh mục có thể tính phí** của mục mô tả hợp đồng dựa trên dự án. Để làm điều này, hãy cập nhật trường **Loại thanh toán** trên lưới con **Thể loại có thể tính phí**.

### <a name="resolve-chargeability"></a>Giải quyết khả năng tính phí

Giá trị ước tính hoặc thực tế được tạo cho thời gian sẽ chỉ được coi là có thể tính phí nếu **Thời gian** được bao gồm trên mục mô tả hợp đồng và nếu **Nhiệm vụ**, **Vai trò** được đặt cấu hình là có thể tính phí trên mục mô tả hợp đồng.

Giá trị ước tính hoặc thực tế được tạo cho chi phí sẽ chỉ được coi là có thể tính phí nếu **Chi phí** được bao gồm trên mục mô tả hợp đồng và nếu **Nhiệm vụ**, danh mục **Giao dịch** được đặt cấu hình là có thể tính phí trên mục mô tả hợp đồng.


| Bao gồm thời gian | Bao gồm chi phí | Bao gồm nhiệm vụ | Vai trò           | Danh mục       | Tác vụ                                                                                                      |
|---------------|------------------|----------------|----------------|----------------|-----------------------------------------------------------------------------------------------------------|
| Có           | Có              | Toàn bộ dự án | Có thể tính phí     | Có thể tính phí     | Thanh toán theo giá trị Thời gian thực tế: **Có thể tính phí** </br> Loại thanh toán theo giá trị Chi phí thực tế: **Có thể tính phí**           |
| Có           | Có              | Nhiệm vụ được chọn | Có thể tính phí     | Có thể tính phí     | Thanh toán theo giá trị Thời gian thực tế: **Có thể tính phí** </br> Loại thanh toán theo giá trị Chi phí thực tế: **Có thể tính phí**           |
| Có           | Có              | Nhiệm vụ được chọn | Không thể tính phí | Có thể tính phí     | Thanh toán theo giá trị Thời gian thực tế: **Không thể tính phí** </br> Loại thanh toán theo giá trị Chi phí thực tế: **Có thể tính phí**       |
| Có           | Có              | Nhiệm vụ được chọn | Có thể tính phí     | Có thể tính phí     | Thanh toán theo giá trị Thời gian thực tế: **Không thể tính phí** </br> Loại thanh toán theo giá trị Chi phí thực tế: **Không thể tính phí** |
| Có           | Có              | Nhiệm vụ được chọn | Không thể tính phí | Có thể tính phí     | Thanh toán theo giá trị Thời gian thực tế: **Không thể tính phí** </br> Loại thanh toán theo giá trị Chi phí thực tế: **Không thể tính phí** |
| Có           | Có              | Nhiệm vụ được chọn | Không thể tính phí | Không thể tính phí | Thanh toán theo giá trị Thời gian thực tế: **Không thể tính phí** </br> Loại thanh toán theo giá trị Chi phí thực tế: **Không thể tính phí** |
| No            | Có              | Toàn bộ dự án | Không thể đặt   | Có thể tính phí     | Thanh toán theo giá trị Thời gian thực tế: **Không khả dụng**</br>Loại thanh toán theo giá trị Chi phí thực tế: **Có thể tính phí**          |
| No            | Có              | Toàn bộ dự án | Không thể đặt   | Không thể tính phí | Thanh toán theo giá trị Thời gian thực tế: **Không khả dụng**</br> Loại thanh toán theo giá trị Chi phí thực tế: **Không thể tính phí**     |
| Có           | No               | Toàn bộ dự án | Có thể tính phí     | Không thể đặt   | Thanh toán theo giá trị Thời gian thực tế: **Có thể tính phí** </br> Loại thanh toán theo giá trị Chi phí thực tế: **Không khả dụng**        |
| Có           | No               | Toàn bộ dự án | Không thể tính phí | Không thể đặt   | Thanh toán theo giá trị Thời gian thực tế: **Không thể tính phí** </br>Loại thanh toán theo giá trị Chi phí thực tế: **Không khả dụng**   |
