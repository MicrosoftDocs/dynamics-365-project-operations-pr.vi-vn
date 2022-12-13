---
title: Đặt cấu hình các thành phần phải chịu phí tổn của mô tả hợp đồng dự án
description: Bài viết này cung cấp thông tin về cách thêm các thành phần có thể tính phí vào mục mô tả hợp đồng trong Project Operations.
author: rumant
ms.date: 10/08/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 33296c93964cc88499e7a98d499b99463e59d62a
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825591"
---
# <a name="configure-chargeable-components-of-a-project-contract-line"></a>Đặt cấu hình các thành phần phải chịu phí tổn của mô tả hợp đồng dự án

_**Áp dụng cho:** Triển khai bản đơn giản - từ thỏa thuận đến lập hóa đơn ước giá, Project Operations cho các kịch bản dựa trên tài nguyên/không lưu kho_

Một mô tả hợp đồng dự án có *các thành phần* bao gồm và các thành phần *có thể tính phí* .

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

Một nhiệm vụ dự án có thể là nhiệm vụ phải chịu phí tổn hoặc không phải chịu phí tổn trên một mục mô tả hợp đồng cụ thể, vì vậy, có thể có các cách thiết lập sau đây:

Nếu một mục mô tả hợp đồng dựa trên dự án có **Thời gian** và một nhiệm vụ nhất định, thì **T1** sẽ được liên kết với mục đó dưới dạng có thể tính phí. Nếu có mục mô tả hợp đồng thứ hai bao gồm **Chi phí**, thì bạn có thể liên kết nhiệm vụ T1 trên mục mô tả hợp đồng dưới dạng không thể tính phí. Kết quả là toàn bộ thời gian được ghi lại trong nhiệm vụ đều là dạng có thể tính phí và tất cả các chi phí là dạng không thể tính phí.

Loại thanh toán của nhiệm vụ có thể được đặt cấu hình trên tab **Nhiệm vụ có thể tính phí** của mô tả hợp đồng bằng cách cập nhật trường **Loại thanh toán** trên lưới con nhiệm vụ trong mô tả hợp đồng. Ngoài ra, bạn có thể cập nhật trường **Loại thanh toán** trên lưới con của nhiệm vụ Thiết lập thanh toán trong một dự án hiển thị mô tả hợp đồng được liên kết với một nhiệm vụ.

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a>Cập nhật vai trò thành dạng có thể tính phí hoặc không thể tính phí

Một vai trò có thể là dạng có thể tính phí hoặc không thể tính phí trên một mục mô tả hợp đồng cụ thể.

Bạn có thể đặt cấu hình loại thanh toán của một vai trò trên tab **Vai trò có thể tính phí** của mục mô tả hợp đồng. Để làm điều này, hãy cập nhật trường **Loại thanh toán** trên lưới con **Vai trò có thể tính phí**.

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a>Cập nhật danh mục giao dịch thành dạng có thể tính phí hoặc không thể tính phí

Một danh mục giao dịch có thể là dạng có thể tính phí hoặc không thể tính phí trên một mục mô tả hợp đồng cụ thể.

Bạn có thể đặt cấu hình loại thanh toán của một giao dịch trên tab **Danh mục có thể tính phí** của mục mô tả hợp đồng dựa trên dự án. Để làm điều này, hãy cập nhật trường **Loại thanh toán** trên lưới con **Thể loại có thể tính phí**.

### <a name="resolve-chargeability"></a>Giải quyết khả năng tính phí

Một giá trị ước tính hoặc thực tế được tạo cho thời gian chỉ được coi là phải chịu phí tổn nếu:

   - **Thời gian** được thêm vào mô tả hợp đồng.
   - **Vai trò** được đặt cấu hình là phải chịu phí tổn trên mô tả hợp đồng.
   - **Các nhiệm vụ được đưa vào** được đặt thành **Các nhiệm vụ đã chọn** trên mô tả hợp đồng.
 
 Nếu ba điều này là đúng, thì nhiệm vụ được đặt cấu hình là phải chịu phí tổn. 

Một giá trị ước tính hoặc thực tế được tạo cho chi phí chỉ được coi là phải chịu phí tổn nếu:

   - **Chi phí** được thêm vào mô tả hợp đồng
   - **Thể loại giao dịch** được đặt cấu hình là phải chịu phí tổn trên mô tả hợp đồng
   - **Các nhiệm vụ được đưa vào** được đặt thành **Nhiệm vụ đã chọn** trên mô tả hợp đồng
  
 Nếu ba điều này là đúng, thì **Nhiệm vụ** được đặt cấu hình là phí tổn phải trả. 

Một số liệu ước tính hoặc số liệu thực tế được tạo cho vật tư chỉ được coi là phí tổn phải trả nếu:

   - **Vật tư** được thêm vào mô tả hợp đồng
   - **Các nhiệm vụ được đưa vào** được đặt thành **Các nhiệm vụ đã chọn** trên mô tả hợp đồng

Nếu hai điều này là đúng, thì **Nhiệm vụ** được đặt cấu hình là phí tổn phải trả. 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>Bao gồm thời gian</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>Bao gồm chi phí</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>Bao gồm vật tư</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
                    <strong>Các tác vụ được đưa vào</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Vai trò</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Danh mục</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Tác vụ</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
                    <strong>Tác động đến khả năng phải chịu phí tổn</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Có </p>
            </td>
            <td width="78" valign="top">
                <p>
Có </p>
            </td>
            <td width="63" valign="top">
                <p>
Có </p>
            </td>
            <td width="75" valign="top">
                <p>
Toàn bộ dự án </p>
            </td>
            <td width="65" valign="top">
                <p>
Có thể tính phí </p>
            </td>
            <td width="70" valign="top">
                <p>
Có thể tính phí </p>
            </td>
            <td width="65" valign="top">
                <p>
Không thể đặt </p>
            </td>
            <td width="350" valign="top">
                <p>
Thanh toán theo giá trị thời gian thực tế: <strong>Phải chịu phí tổn</strong>
                </p>
                <p>
Loại thanh toán theo giá trị chi phí thực tế: <strong>Phải chịu phí tổn</strong>
                </p>
                <p>
Loại thanh toán theo giá trị vật tư thực tế: <strong>Phải chịu phí tổn</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Có </p>
            </td>
            <td width="78" valign="top">
                <p>
Có </p>
            </td>
            <td width="63" valign="top">
                <p>
Có </p>
            </td>
            <td width="75" valign="top">
                <p>
Chỉ các tác vụ được chọn </p>
            </td>
            <td width="65" valign="top">
                <p>
Có thể tính phí </p>
            </td>
            <td width="70" valign="top">
                <p>
Có thể tính phí </p>
            </td>
            <td width="65" valign="top">
                <p>
Có thể tính phí </p>
            </td>
            <td width="350" valign="top">
                <p>
Thanh toán theo giá trị thời gian thực tế: <strong>Phải chịu phí tổn</strong>
                </p>
                <p>
Loại thanh toán theo giá trị chi phí thực tế: <strong>Phải chịu phí tổn</strong>
                </p>
                <p>
Loại thanh toán theo giá trị vật tư thực tế: <strong>Phải chịu phí tổn</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Có </p>
            </td>
            <td width="78" valign="top">
                <p>
Có </p>
            </td>
            <td width="63" valign="top">
                <p>
Có </p>
            </td>
            <td width="75" valign="top">
                <p>
Chỉ các tác vụ được chọn </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Không phải chịu phí tổn</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Có thể tính phí </p>
            </td>
            <td width="65" valign="top">
                <p>
Có thể tính phí </p>
            </td>
            <td width="350" valign="top">
                <p>
Thanh toán theo giá trị thời gian thực tế: <strong>Không phải chịu phí tổn</strong>
                </p>
                <p>
Loại thanh toán theo giá trị chi phí thực tế: Có thể tính phí </p>
                <p>
Loại thanh toán theo giá trị vật tư thực tế: Phải chịu phí tổn </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Có </p>
            </td>
            <td width="78" valign="top">
                <p>
Có </p>
            </td>
            <td width="63" valign="top">
                <p>
Có </p>
            </td>
            <td width="75" valign="top">
                <p>
Chỉ các tác vụ được chọn </p>
            </td>
            <td width="65" valign="top">
                <p>
Có thể tính phí </p>
            </td>
            <td width="70" valign="top">
                <p>
Có thể tính phí </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Không phải chịu phí tổn</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
Thanh toán theo giá trị thời gian thực tế: <strong>Không phải chịu phí tổn</strong>
                </p>
                <p>
Loại thanh toán theo giá trị chi phí thực tế: <strong>Không phải chịu phí tổn</strong>
                </p>
                <p>
Loại thanh toán theo giá trị vật tư thực tế: <strong>Không phải chịu phí tổn</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Có </p>
            </td>
            <td width="78" valign="top">
                <p>
Có </p>
            </td>
            <td width="63" valign="top">
                <p>
Có </p>
            </td>
            <td width="75" valign="top">
                <p>
Chỉ các tác vụ được chọn </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Không phải chịu phí tổn</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Có thể tính phí </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Không phải chịu phí tổn</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
Thanh toán theo giá trị thời gian thực tế: <strong>Không phải chịu phí tổn</strong>
                </p>
                <p>
Loại thanh toán theo giá trị chi phí thực tế: <strong>Không phải chịu phí tổn</strong>
                </p>
                <p>
Loại thanh toán theo giá trị vật tư thực tế: <strong>Không phải chịu phí tổn</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Có </p>
            </td>
            <td width="78" valign="top">
                <p>
Có </p>
            </td>
            <td width="63" valign="top">
                <p>
Có </p>
            </td>
            <td width="75" valign="top">
                <p>
Chỉ các tác vụ được chọn </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Không phải chịu phí tổn</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Không phải chịu phí tổn</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Có thể tính phí </p>
            </td>
            <td width="350" valign="top">
                <p>
Thanh toán theo giá trị thời gian thực tế: <strong>Không phải chịu phí tổn</strong>
                </p>
                <p>
Loại thanh toán theo giá trị chi phí thực tế: <strong>Không phải chịu phí tổn</strong>
                </p>
                <p>
Loại thanh toán theo giá trị vật tư thực tế: Phải chịu phí tổn </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
Có </p>
            </td>
            <td width="63" valign="top">
                <p>
Có </p>
            </td>
            <td width="75" valign="top">
                <p>
Toàn bộ dự án </p>
            </td>
            <td width="65" valign="top">
                <p>
Không thể đặt </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Có thể tính phí</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Không thể đặt </p>
            </td>
            <td width="350" valign="top">
                <p>
Thanh toán theo giá trị thời gian thực tế: <strong>Không khả dụng</strong>
                </p>
                <p>
Loại thanh toán theo giá trị chi phí thực tế: Có thể tính phí </p>
                <p>
Loại thanh toán theo giá trị vật tư thực tế: Phải chịu phí tổn </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
Có </p>
            </td>
            <td width="63" valign="top">
                <p>
Có </p>
            </td>
            <td width="75" valign="top">
                <p>
Toàn bộ dự án </p>
            </td>
            <td width="65" valign="top">
                <p>
Không thể đặt </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Không phải chịu phí tổn</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Không thể đặt </p>
            </td>
            <td width="350" valign="top">
                <p>
Thanh toán theo giá trị thời gian thực tế: <strong>Không khả dụng</strong>
                </p>
                <p>
Loại thanh toán theo giá trị chi phí thực tế: <strong>Không phải chịu phí tổn</strong>
                </p>
                <p>
Loại thanh toán theo giá trị vật tư thực tế: Phải chịu phí tổn </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Có </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
Có </p>
            </td>
            <td width="75" valign="top">
                <p>
Toàn bộ dự án </p>
            </td>
            <td width="65" valign="top">
                <p>
Có thể tính phí </p>
            </td>
            <td width="70" valign="top">
                <p>
Không thể đặt </p>
            </td>
            <td width="65" valign="top">
                <p>
Không thể đặt </p>
            </td>
            <td width="350" valign="top">
                <p>
Thanh toán theo giá trị thời gian thực tế: Có thể tính phí </p>
                <p>
Loại thanh toán theo giá trị chi phí thực tế:<strong> Không khả dụng</strong>
                </p>
                <p>
Loại thanh toán theo giá trị vật tư thực tế: Phải chịu phí tổn </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Có </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
Có </p>
            </td>
            <td width="75" valign="top">
                <p>
Toàn bộ dự án </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Không phải chịu phí tổn</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Không thể đặt </p>
            </td>
            <td width="65" valign="top">
                <p>
Không thể đặt </p>
            </td>
            <td width="350" valign="top">
                <p>
Thanh toán theo giá trị thời gian thực tế: <strong>Không phải chịu phí tổn</strong>
                </p>
                <p>
Loại thanh toán theo giá trị chi phí thực tế:<strong> Không khả dụng</strong>
                </p>
                <p>
Loại thanh toán theo giá trị vật tư thực tế: Phải chịu phí tổn </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Có </p>
            </td>
            <td width="78" valign="top">
                <p>
Có </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
Toàn bộ dự án </p>
            </td>
            <td width="65" valign="top">
                <p>
Có thể tính phí </p>
            </td>
            <td width="70" valign="top">
                <p>
Có thể tính phí </p>
            </td>
            <td width="65" valign="top">
                <p>
Không thể đặt </p>
            </td>
            <td width="350" valign="top">
                <p>
Thanh toán theo giá trị thời gian thực tế: Có thể tính phí </p>
                <p>
Loại thanh toán theo giá trị chi phí thực tế: Có thể tính phí </p>
                <p>
Loại thanh toán theo giá trị vật tư thực tế: <strong>Không khả dụng</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Có </p>
            </td>
            <td width="78" valign="top">
                <p>
Có </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
Toàn bộ dự án </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Không phải chịu phí tổn</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Không thể tính phí</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Không thể đặt </p>
            </td>
            <td width="350" valign="top">
                <p>
Thanh toán theo giá trị thời gian thực tế: <strong>Không phải chịu phí tổn</strong>
                </p>
                <p>
Loại thanh toán theo giá trị chi phí thực tế:<strong> Không phải chịu phí tổn</strong>
                </p>
                <p>
Loại thanh toán theo giá trị vật tư thực tế:<strong> Không khả dụng</strong>
                </p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
