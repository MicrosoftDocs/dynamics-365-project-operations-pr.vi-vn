---
title: Đặt cấu hình các thành phần có thể tính phí của mục mô tả hợp đồng dựa trên dự án
description: Chủ đề này cung cấp thông tin về các thành phần bao gồm, thành phần có thể tính phí và không thể tính phí trên mục mô tả hợp đồng.
author: rumant
manager: Annbe
ms.date: 10/12/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d6f67d5dc6b94148d437b3399229c1235c702c6a
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128733"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a>Đặt cấu hình các thành phần có thể tính phí của mục mô tả hợp đồng dựa trên dự án

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Một mục mô tả hợp đồng dựa trên dự án có các thành phần bao gồm, thành phần có thể tính phí và không thể tính phí.

Thành phần bao gồm sẽ phụ thuộc vào các mục thiết đặt phương thức thanh toán, phần tách của khách hàng, giới hạn không vượt quá và tần suất hóa đơn được xác định trên mục mô tả hợp đồng dựa trên dự án.

Một tập con các thành phần bao gồm có thể được đánh dấu là có thể tính phí bằng cách cập nhật trường **Loại thanh toán**.

Các thành phần có thể tính phí có thể được xác định trên vai trò và danh mục giao dịch.

Đối với mục mô tả hợp đồng dự án, khả năng tính phí được xác định trên vai trò sẽ chỉ áp dụng được cho lớp giao dịch **Thời gian**. Nếu **Bao gồm thời gian** được đặt thành **Không** trên một mục mô tả hợp đồng dự án, thì tab **Vai trò có thể tính phí** sẽ không khả dụng.

Khả năng tính phí được xác định trên các danh mục giao dịch cho một mục mô tả hợp đồng dự án và chỉ áp dụng cho lớp giao dịch **Chi phí**. Nếu **Bao gồm chi phí** được đặt thành **Không** trên một mục mô tả hợp đồng dự án, thì tab **Danh mục có thể tính phí** sẽ không khả dụng.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Cập nhật vai trò thành dạng có thể tính phí hoặc không thể tính phí

Một vai trò có thể là dạng có thể tính phí hoặc không thể tính phí trên một mục mô tả hợp đồng dựa trên dự án cụ thể.

Ở tab **Các vai trò có thể tính phí** của mô tả hợp đồng dựa trên dự án, trên lưới con **Thể loại có thể tính phí**, trong trường **Loại thanh toán**, hãy cập nhật loại thanh toán cho một vai trò.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Cập nhật danh mục giao dịch thành dạng có thể tính phí hoặc không thể tính phí

Một danh mục giao dịch có thể là dạng có thể tính phí hoặc không thể tính phí trên một mục mô tả hợp đồng dựa trên dự án cụ thể.

Ở tab **Thể loại có thể tính phí** của mô tả hợp đồng dựa trên dự án, trên lưới con **Thể loại có thể tính phí**, trong trường **Loại thanh toán**, hãy cập nhật loại thanh toán cho một giao dịch.

### <a name="resolve-chargeability"></a>Giải quyết khả năng tính phí

Giá trị ước tính hoặc thực tế được tạo cho thời gian sẽ chỉ được coi là có thể tính phí nếu thời gian được bao gồm trên mục mô tả hợp đồng và nếu vai trò được đặt cấu hình là có thể tính phí trên mục mô tả hợp đồng.

Giá trị ước tính hoặc thực tế được tạo cho chi phí sẽ chỉ được coi là có thể tính phí nếu chi phí được bao gồm trên mục mô tả hợp đồng và nếu danh mục giao dịch được đặt cấu hình là có thể tính phí trên mục mô tả hợp đồng.

| Bao gồm thời gian | Bao gồm chi phí | Vai trò | Danh mục | Tác vụ |
| --- | --- | --- | --- | --- |
| Có | Có | Có thể tính phí | Có thể tính phí | Thanh toán theo giá trị thời gian thực tế: Có thể tính phí </br>Loại thanh toán trên giá trị chi phí thực tế: Có thể tính phí |
| Có | Có | Không thể tính phí | Có thể tính phí | Thanh toán theo giá trị thời gian thực tế: Không thể tính phí </br>Loại thanh toán trên giá trị chi phí thực tế: Có thể tính phí |
| Có | Có | Không thể tính phí | Không thể tính phí | Thanh toán theo giá trị thời gian thực tế: Không thể tính phí </br>Loại thanh toán trên giá trị chi phí thực tế: Không thể tính phí |
| No | Có | Không thể đặt | Có thể tính phí | Thanh toán theo giá trị thời gian thực tế: Không khả dụng </br>Loại thanh toán trên giá trị chi phí thực tế: Có thể tính phí |
| No | Có | Không thể đặt | Không thể tính phí | Thanh toán theo giá trị thời gian thực tế: Không khả dụng </br>Loại thanh toán trên giá trị chi phí thực tế: Không thể tính phí |
| Có | No | Có thể tính phí | Không thể đặt | Thanh toán theo giá trị thời gian thực tế: Có thể tính phí </br>Loại thanh toán trên giá trị chi phí thực tế: Không khả dụng |
| Có | No | Không thể tính phí | Không thể đặt | Thanh toán theo giá trị thời gian thực tế: Không thể tính phí </br> Loại thanh toán trên giá trị chi phí thực tế: Không khả dụng |
