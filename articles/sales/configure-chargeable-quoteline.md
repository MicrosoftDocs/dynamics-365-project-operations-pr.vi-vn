---
title: Đặt cấu hình các thành phần có thể tính phí của một dòng mô tả báo giá theo dự án
description: Chủ đề này cung cấp thông tin về các thành phần được bao gồm, có thể tính phí và không thể tính phí trên các dòng mô tả báo giá theo dự án.
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 36765ab3687a8aaf3ae4a631516a1d61c14e981e
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642569"
---
# <a name="configure-the-chargeable-components-of-a-project-based-quote-line"></a>Đặt cấu hình các thành phần có thể tính phí của một dòng mô tả báo giá theo dự án

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Một dòng mô tả báo giá dựa trên dự án có thể chứa thành phần được bao gồm và thành phần có thể tính phí.

Các thành phần được bao gồm sẽ tuân theo phương thức lập hóa đơn, cách phân chia khách hàng, giới hạn không được vượt quá và các tùy chọn cài đặt tần suất hóa đơn trên dòng mô tả báo giá theo dự án.
Bạn có thể đánh dấu một tập con của các thành phần được bao gồm là có thể tính phí bằng cách dùng **Loại thanh toán**. Bạn có thể chọn một trong các tùy chọn sau trong trường **Loại thanh toán** trong phạm vi dòng mô tả báo giá:

   - Có thể tính phí
   - Không thể tính phí

Các thành phần có thể tính phí có thể được xác định trên vai trò và danh mục giao dịch.

Trạng thái tính phí xác định trên các vai trò của dòng mô tả báo giá dự án sẽ chỉ áp dụng cho lớp giao dịch **Thời gian**. Nếu một dòng báo giá dự án có giá trị **Bao gồm thời gian** = **Không**, thì tab **Vai trò có thể tính phí** sẽ không khả dụng.

Trạng thái tính phí xác định trên các danh mục giao dịch của dòng mô tả báo giá dự án sẽ chỉ áp dụng cho lớp giao dịch **Chi phí**. Nếu một dòng báo giá dự án có giá trị **Bao gồm chi phí** = **Không**, thì tab **Danh mục có thể tính phí** sẽ không khả dụng.

## <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Cập nhật vai trò thành dạng có thể tính phí hoặc không thể tính phí
Trên một dòng báo giá theo dự án, một vai trò có thể có trạng thái là có thể tính phí hoặc không thể tính phí. Bạn có thể đặt thông số loại thanh toán trên một vai trò thông qua tab **Vai trò có thể tính phí** của dòng báo giá theo dự án. Để thực hiện việc này, hãy cập nhật **Loại thanh toán** trên lưới con **Vai trò có thể tính phí**. 

## <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Cập nhật danh mục giao dịch thành dạng có thể tính phí hoặc không thể tính phí
Trên một dòng báo giá theo dự án, một danh mục giao dịch có thể có trạng thái là có thể tính phí hoặc không thể tính phí. Bạn có thể đặt thông số loại thanh toán trên một giao dịch thông qua tab **Danh mục có thể tính phí** của dòng báo giá theo dự án. Để làm điều này, hãy cập nhật trường **Loại thanh toán** trên lưới con **Thể loại có thể tính phí**. 

## <a name="resolve-chargeability"></a>Giải quyết khả năng tính phí

Giá trị ước tính hoặc thực tế của thời gian chỉ được xem là có thể tính phí nếu thời gian được bao gồm trên dòng báo giá và nếu vai trò được đặt cấu hình là có thể tính phí.
Giá trị ước tính hoặc thực tế của chi phí chỉ được xem là có thể tính phí nếu chi phí được bao gồm trên dòng báo giá và nếu danh mục giao dịch được đặt cấu hình là có thể tính phí trên báo giá. Bảng sau trình bày giá trị mặc định của trạng thái tính phí trên mỗi trường hợp thực tế. Các thành phần được bao gồm và loại thanh toán mà bạn thiết lập trên dòng báo giá sẽ quyết định giá trị mặc định.

| Bao gồm thời gian | Bao gồm chi phí | Vai trò | Danh mục | Tác vụ |
| --- | --- | --- | --- | --- |
| Có | Có | Có thể tính phí | Có thể tính phí | Thanh toán theo giá trị thời gian thực tế: Có thể tính phí </br>Loại thanh toán trên giá trị chi phí thực tế: Có thể tính phí |
| Có | Có | Không thể tính phí | Có thể tính phí | Thanh toán theo giá trị thời gian thực tế: Không thể tính phí </br>Loại thanh toán trên giá trị chi phí thực tế: Có thể tính phí |
| Có | Có | Không thể tính phí | Không thể tính phí | Thanh toán theo giá trị thời gian thực tế: Không thể tính phí </br>Loại thanh toán trên giá trị chi phí thực tế: Không thể tính phí |
| No | Có | Không thể đặt | Có thể tính phí | Thanh toán theo giá trị thời gian thực tế: Không khả dụng </br>Loại thanh toán trên giá trị chi phí thực tế: Có thể tính phí |
| No | Có | Không thể đặt | Không thể tính phí | Thanh toán theo giá trị thời gian thực tế: Không khả dụng </br>Loại thanh toán trên giá trị chi phí thực tế: Không thể tính phí |
| Có | No | Có thể tính phí | Không thể đặt | Thanh toán theo giá trị thời gian thực tế: Có thể tính phí </br>Loại thanh toán trên giá trị chi phí thực tế: Không khả dụng |
| Có | No | Không thể tính phí | Không thể đặt | Thanh toán theo giá trị thời gian thực tế: Không thể tính phí </br> Loại thanh toán trên giá trị chi phí thực tế: Không khả dụng |


[!INCLUDE[footer-include](../includes/footer-banner.md)]