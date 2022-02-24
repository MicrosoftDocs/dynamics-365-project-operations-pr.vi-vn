---
title: Đặt cấu hình các thành phần có thể tính phí của mục mô tả báo giá
description: Chủ đề này cung cấp thông tin về cách thiết lập các thành phần có thể tính phí và không thể tính phí trên mục mô tả báo giá dựa trên dự án.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1a9e1851bd8c5a4070df2774c945d1f3eabaaa8a
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858319"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a>Đặt cấu hình các thành phần có thể tính phí của một mô tả báo giá 

_**Áp dụng cho:** Triển khai bản đơn giản - từ thỏa thuận đến lập hóa đơn ước giá, Project Operations cho các kịch bản dựa trên tài nguyên/không lưu kho_

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

Một nhiệm vụ dự án có thể là nhiệm vụ phải chịu phí tổn hoặc không phải chịu phí tổn trong bối cảnh một mục mô tả báo giá dựa trên dự án cụ thể, vì vậy, các tổ hợp sau có thể được thiết lập.

Nếu mục mô tả báo giá dựa trên dự án bao gồm **Thời gian** và nhiệm vụ **T1**, thì nhiệm vụ được liên kết với mục mô tả báo giá dưới dạng có thể tính phí. Nếu có mục mô tả báo giá thứ hai bao gồm **Chi phí**, thì bạn có thể liên kết nhiệm vụ **T1** trên mục mô tả báo giá dưới dạng không thể tính phí. Kết quả là toàn bộ thời gian được ghi lại trong nhiệm vụ đều là dạng có thể tính phí và tất cả các chi phí được ghi lại trong nhiệm vụ đều là dạng không thể tính phí.

Loại thanh toán của nhiệm vụ có thể được đặt cấu hình trên tab **Nhiệm vụ có thể tính phí** của mô tả báo giá dựa trên dự án bằng cách cập nhật trường **Loại thanh toán** trên lưới con **Nhiệm vụ trong mô tả báo giá**. Ngoài ra, bạn có thể cập nhật loại thanh toán cho nhiệm vụ dự án trong trường **Loại thanh toán** trên lưới con khi thiết lập thanh toán cho nhiệm vụ của một dự án hiển thị mô tả báo giá được liên kết với một nhiệm vụ.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Cập nhật vai trò thành dạng có thể tính phí hoặc không thể tính phí

Một vai trò có thể là dạng có thể tính phí hoặc không thể tính phí trong bối cảnh một mục mô tả báo giá dựa trên dự án cụ thể.

Loại thanh toán của một vai trò có thể được đặt cấu hình trên tab **Các vai trò có thể tính phí** của mô tả báo giá bằng cách cập nhật trường **Loại thanh toán** trên lưới con **Các vai trò có thể tính phí**.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Cập nhật danh mục giao dịch thành dạng có thể tính phí hoặc không thể tính phí

Một danh mục giao dịch có thể là dạng có thể tính phí hoặc không thể tính phí trên một mục mô tả báo giá cụ thể.

Loại thanh toán của một giao dịch có thể được đặt cấu hình trên tab **Thể loại có thể tính phí** của mô tả báo giá bằng cách cập nhật trường **Loại thanh toán** trên lưới con **Thể loại có thể tính phí**.

### <a name="resolve-chargeability"></a>Giải quyết khả năng tính phí
Một giá trị ước tính hoặc thực tế được tạo cho thời gian sẽ chỉ được coi là phải chịu phí tổn nếu:

   - **Thời gian** được thêm vào mô tả báo giá.
   - **Vai trò** được đặt cấu hình là phải chịu phí tổn trên mô tả báo giá.
   - **Các nhiệm vụ được đưa vào** được đặt thành **Các nhiệm vụ đã chọn** trên mô tả báo giá. 

Nếu ba điều này là đúng, thì **Nhiệm vụ** cũng được đặt cấu hình là phải chịu phí tổn. 

Một giá trị ước tính hoặc thực tế được tạo cho chi phí chỉ được coi là phải chịu phí tổn nếu: 

   - **Chi phí** được thêm vào mô tả báo giá.
   - **Thể loại giao dịch** được đặt cấu hình là phải chịu phí tổn trên mô tả báo giá.
   - **Các nhiệm vụ được đưa vào** được đặt thành **Các nhiệm vụ đã chọn** trên mô tả báo giá.

Nếu ba điều này là đúng, thì **Nhiệm vụ** cũng được đặt cấu hình là phải chịu phí tổn. 

Một số liệu ước tính hoặc số liệu thực tế được tạo cho vật tư sẽ chỉ được coi là phải chịu phí tổn nếu:

   - **Vật tư** được thêm vào mô tả báo giá.
   - **Các nhiệm vụ được đưa vào** được đặt thành **Các nhiệm vụ đã chọn** trên mô tả báo giá.

Nếu hai điều này là đúng, thì **Nhiệm vụ** cũng nên được đặt cấu hình là phải chịu phí tổn. 


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
Thanh toán theo giá trị thời gian thực tế: Có thể tính phí </p>
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
Có thể tính phí </p>
            </td>
            <td width="350" valign="top">
                <p>
Thanh toán theo giá trị thời gian thực tế: Có thể tính phí </p>
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
