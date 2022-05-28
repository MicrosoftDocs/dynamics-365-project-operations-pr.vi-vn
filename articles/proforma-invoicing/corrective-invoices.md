---
title: Hóa đơn hiệu chỉnh dựa trên dự án
description: Chủ đề này cung cấp thông tin về cách tạo và xác nhận các hóa đơn hiệu chỉnh dựa trên dự án trong Project Operations.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 71bf10518c22ce2ad6aa43b710c68d0d46f93e77
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8594650"
---
# <a name="corrective-project-based-invoices"></a>Hóa đơn hiệu chỉnh dựa trên dự án

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Hóa đơn dự án đã xác nhận có thể được hiệu chỉnh để xử lý các thay đổi hoặc tín dụng theo như sự thương lượng với khách hàng và người quản lý dự án.

Để chỉnh sửa hóa đơn đã xác nhận, hãy mở hóa đơn đã xác nhận và chọn **Sửa chữa hóa đơn này**. 

> [!NOTE]
> Lựa chọn này không khả dụng trừ khi hóa đơn dự án được xác nhận hoặc hóa đơn dựa trên dự án có các khoản tạm ứng hoặc đặt cọc hoặc các mục đối chiếu các khoản tạm ứng hoặc đặt cọc.

Một hóa đơn nháp mới được tạo từ hóa đơn đã xác nhận. Tất cả các chi tiết mô tả hóa đơn từ hóa đơn đã được xác nhận trước đây sẽ được sao chép vào hóa đơn nháp mới. Sau đây là một số điểm chính mà bạn cần hiểu về chi tiết mô tả trên hóa đơn được hiệu chỉnh mới:

- Tất cả các số lượng được cập nhật thành không. Dynamics 365 Project Operations giả định rằng tất cả các hạng mục đưa vào hóa đơn đều được ghi có đầy đủ. Nếu cần, bạn có thể cập nhật thủ công các số lượng này để phản ánh số lượng được lập hóa đơn chứ không phải số lượng được ghi có. Dựa trên số lượng bạn nhập, ứng dụng sẽ tính số lượng được ghi có. Số lượng này được phản ánh ở các giá trị thực tế sẽ được tạo ra khi hóa đơn hiệu chỉnh được xác nhận. Nếu bạn thay đổi số tiền thuế, thì bạn phải nhập số tiền thuế chính xác chứ không phải số tiền thuế được ghi có.
- Các phần hiệu chỉnh mốc luôn được xử lý dưới dạng tín dụng đầy đủ.


> [!IMPORTANT]
> Đối với chi tiết mô tả hóa đơn là các sửa đổi đối với những khoản phí đã được lập hóa đơn, trường **Điều chỉnh** được đặt thành **Có**. Đối với hóa đơn có các chi tiết mô tả hóa đơn đã được sửa đổi, trường **Có nội dung điều chỉnh** được đặt thành **Có**.

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a>Các giá trị thực tế được tạo khi xác nhận hóa đơn hiệu chỉnh

Bảng sau liệt kê các giá trị thực tế được tạo khi xác nhận hóa đơn hiệu chỉnh.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p>
                    <strong>Kịch bản</strong>
                </p>
            </td>
            <td width="808" valign="top">
                <p>
                    <strong>Giá trị thực tế được tạo khi xác nhận</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Lập hóa đơn toàn bộ tín dụng của giao dịch thời gian đã lập hóa đơn trước đây.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Một khoản đảo ngược doanh số đã lập hóa đơn cho số giờ và số tiền trên chi tiết mô tả hóa đơn gốc cho thời gian.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Một giá trị thực tế đảo ngược doanh số chưa lập hóa đơn mới cho số giờ và số tiền trên chi tiết mô tả hóa đơn gốc cho thời gian.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Lập hóa đơn một phần tín dụng trên một giao dịch thời gian.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Một khoản đảo ngược doanh số đã lập hóa đơn cho số giờ và số tiền được lập hóa đơn trên chi tiết mô tả hóa đơn gốc cho thời gian.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Giá trị thực tế doanh số chưa lập hóa đơn mới, có thể tính phí cho số giờ và số tiền trên chi tiết mô tả hóa đơn đã sửa, khoản đảo ngược của giá trị này và giá trị thực tế doanh số bán hàng đã lập hóa đơn tương đương.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Giá trị thực tế doanh số chưa lập hóa đơn mới, có thể tính phí cho số giờ và số tiền còn lại sau khi khấu trừ các số liệu đã hiệu chỉnh trên chi tiết mô tả hóa đơn.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Lập hóa đơn toàn bộ tín dụng của giao dịch chi phí đã lập hóa đơn trước đây.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Một khoản đảo ngược doanh số đã lập hóa đơn cho số lượng và số tiền trên chi tiết mô tả hóa đơn gốc cho chi phí.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Một giá trị thực tế đảo ngược doanh số chưa lập hóa đơn mới cho số lượng và số tiền trên chi tiết mô tả hóa đơn gốc cho chi phí.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Lập hóa đơn một phần tín dụng của giao dịch chi phí đã lập hóa đơn trước đây.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Một khoản đảo ngược doanh số đã lập hóa đơn cho số lượng và số tiền được lập hóa đơn trên chi tiết mô tả hóa đơn gốc cho một chi phí.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Giá trị thực tế doanh số chưa lập hóa đơn mới, có thể tính phí cho số lượng và số tiền trên chi tiết mô tả hóa đơn đã hiệu chỉnh, khoản đảo ngược của giá trị này và giá trị thực tế doanh số đã lập hóa đơn tương đương.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Giá trị thực tế doanh số chưa lập hóa đơn mới, có thể tính phí cho số lượng và số tiền còn lại sau khi khấu trừ các số liệu đã hiệu chỉnh trên chi tiết mô tả hóa đơn.
                </p>
            </td>
        </tr>
                <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Lập hóa đơn toàn bộ tín dụng của một giao dịch vật tư đã được lập hóa đơn trước đó.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Một khoản đảo ngược doanh số đã được lập hóa đơn cho số lượng và số tiền ghi trên chi tiết mô tả hóa đơn gốc cho vật tư.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Một giá trị thực tế mới của doanh số bán hàng chưa được lập hóa đơn cho số lượng và số tiền ghi trên chi tiết mô tả hóa đơn gốc cho vật tư.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Lập hóa đơn tín dụng từng phần cho một giao dịch về vật tư.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Một khoản đảo ngược doanh số đã được lập hóa đơn cho số lượng và số tiền ghi trên chi tiết mô tả hóa đơn gốc cho vật tư.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Một giá trị thực tế mới của doanh số bán hàng chưa lập hóa đơn. Đây là giá trị phải chịu phí tổn cho số lượng và số tiền ghi trên chi tiết mô tả hóa đơn đã chỉnh sửa, khoản đảo ngược của giá trị này và một giá trị thực tế của doanh số đã lập hóa đơn tương đương.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Giá trị thực tế doanh số chưa lập hóa đơn mới, có thể tính phí cho số lượng và số tiền còn lại sau khi khấu trừ các số liệu đã hiệu chỉnh trên chi tiết mô tả hóa đơn.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Lập hóa đơn toàn bộ tín dụng của giao dịch phí đã lập hóa đơn trước đây.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Một khoản đảo ngược doanh số đã lập hóa đơn cho số lượng và số tiền trên chi tiết mô tả hóa đơn gốc cho phí.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Một giá trị thực tế đảo ngược doanh số chưa lập hóa đơn mới cho số lượng và số tiền trên chi tiết mô tả hóa đơn gốc cho phí.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Lập hóa đơn một phần tín dụng của giao dịch phí đã lập hóa đơn trước đây.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Một khoản đảo ngược doanh số đã lập hóa đơn cho số lượng và số tiền được lập hóa đơn trên chi tiết mô tả hóa đơn gốc cho phí.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Giá trị thực tế doanh số chưa lập hóa đơn mới, có thể tính phí cho số lượng và số tiền trên chi tiết mô tả hóa đơn hiệu chỉnh đã sửa, khoản đảo ngược của giá trị này và giá trị thực tế doanh số đã lập hóa đơn tương đương.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Lập hóa đơn toàn bộ tín dụng của mốc đã lập hóa đơn trước đây.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Một khoản đảo ngược doanh số đã lập hóa đơn cho số giờ và số tiền trên chi tiết mô tả hóa đơn gốc cho mốc.
                </p>
                <p>
Trạng thái hóa đơn của mốc được cập nhật từ <b>Đã đăng hóa đơn khách hàng</b> thành <b>Sẵn sàng lập hóa đơn</b>.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Lập hóa đơn một phần tín dụng của mốc đã lập hóa đơn trước đây.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Kịch bản này không được hỗ trợ.
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
