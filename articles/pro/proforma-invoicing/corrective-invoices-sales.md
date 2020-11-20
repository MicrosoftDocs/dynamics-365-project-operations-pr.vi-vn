---
title: Hóa đơn được hiệu chỉnh - bản đơn giản
description: Chủ đề này cung cấp thông tin về hóa đơn được hiệu chỉnh trong Project Operations
author: rumant
manager: Annbe
ms.date: 10/15/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 55bec8ad1d9c2b55cabb453321f13df8b7cd1614
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176457"
---
# <a name="corrected-invoices---lite"></a>Hóa đơn được hiệu chỉnh - bản đơn giản

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Hóa đơn dự án đã xác nhận có thể được hiệu chỉnh để xử lý các thay đổi hoặc tín dụng theo như sự thương lượng với khách hàng và người quản lý dự án.

Để chỉnh sửa hóa đơn đã xác nhận, hãy mở hóa đơn đã xác nhận và chọn **Sửa chữa hóa đơn này**. 

> [!NOTE]
> Mục lựa chọn này sẽ không khả dụng cho đến khi hóa đơn dự án được xác nhận.

Một hóa đơn nháp mới được tạo từ hóa đơn đã xác nhận. Tất cả các chi tiết mô tả hóa đơn từ hóa đơn đã được xác nhận trước đây sẽ được sao chép vào hóa đơn nháp mới. Sau đây là một số điểm chính mà bạn cần hiểu về chi tiết mô tả trên hóa đơn được hiệu chỉnh mới:

- Tất cả các số lượng được cập nhật thành không. Ứng dụng giả định rằng tất cả các mặt hàng được lập hóa đơn đều được ghi có đầy đủ. Nếu cần, bạn có thể cập nhật thủ công các số lượng này để phản ánh số lượng được lập hóa đơn chứ không phải số lượng được ghi có. Dựa trên số lượng bạn nhập, ứng dụng sẽ tính số lượng được ghi có. Số lượng này được phản ánh ở các giá trị thực tế sẽ được tạo ra khi hóa đơn hiệu chỉnh được xác nhận. Nếu bạn thay đổi số tiền thuế, thì bạn phải nhập số tiền thuế chính xác chứ không phải số tiền thuế được ghi có.
- Các mục mô tả hợp đồng dựa trên sản phẩm đã xác nhận trước đây sẽ không được sao chép sang hóa đơn mới. Không hỗ trợ xử lý các phần hiệu chỉnh trên hóa đơn dự án dựa trên sản phẩm.
- Các phần hiệu chỉnh mốc luôn được xử lý dưới dạng tín dụng đầy đủ.
- Số tiền trả trước hoặc tạm ứng có thể được hiệu chỉnh nếu khách hàng được lập hóa đơn một số tiền không chính xác.
- Các mục điều hòa số tiền trả trước và tạm ứng có thể được hiệu chỉnh nếu số tiền không chính xác được sử dụng để điều hòa với các khoản phí trên hóa đơn đã xác nhận trước đây.

> [!IMPORTANT]
> Đối với các chi tiết mô tả hóa đơn là phần hiệu chỉnh cho các khoản phí đã được lập hóa đơn khác, trường **Sửa chữa** tương ứng được đặt thành **Có**. Các hóa đơn được hiệu chỉnh chi tiết mô tả hóa đơn sẽ có một trường **Có nội dung điều chỉnh**, trường đó cũng được đặt thành **Có**.

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a>Các giá trị thực tế sẽ được tạo khi Xác nhận hóa đơn hiệu chỉnh:

Dưới đây là các giá trị thực tế sẽ được ứng dụng tạo ra khi xác nhận một mục hiệu chỉnh dựa trên các thao tác được thực hiện trên hóa đơn hiệu chỉnh nháp trước khi xác nhận.

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
            <td width="216" rowspan="4" valign="top">
                <p>
Xác nhận việc hiệu chỉnh khoản tạm ứng hoặc trả trước đã lập hóa đơn.<strong></strong>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Khoản đảo ngược doanh số chưa lập hóa đơn của số tiền trả trước hoặc tạm ứng đã tạo để điều hòa. Số tiền này là số dương vì nó có tác dụng bù cho giá trị âm được tạo ra khi số tiền trả trước hoặc tạm ứng được lập hóa đơn.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Một giá trị thực tế đảo ngược doanh số đã lập hóa đơn được tạo cho số tiền trả trước hoặc tạm ứng để đảo ngược doanh số đã lập hóa đơn ban đầu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Một giá trị thực tế doanh số được lập hóa đơn mới được tạo cho số tiền đã hiệu chỉnh đối với mục mô tả hóa đơn được hiệu chỉnh dựa trên số tiền trả trước hoặc tạm ứng.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Một giá trị thực tế doanh số chưa lập hóa đơn tương ứng với giá trị âm của mục mô tả hóa đơn được hiệu chỉnh dựa trên số tiền trả trước hoặc tạm ứng, sẽ được sử dụng để điều hòa.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
Một mục xác nhận việc hiệu chỉnh khoản tiền trả trước hoặc tạm ứng đã điều hòa trước đây.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Khoản đảo ngược doanh số chưa lập hóa đơn của số tiền trả trước hoặc tạm ứng đã tạo để điều hòa. Số tiền này là số dương và có tác dụng bù cho giá trị âm được tạo ra khi thực hiện việc điều hòa trước đây.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Một giá trị thực tế đảo ngược doanh số đã lập hóa đơn cho số tiền trên hóa đơn trước đây.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Một giá trị thực tế doanh số đã lập hóa đơn mới được tạo cho số tiền trả trước hiệu chỉnh được áp dụng cho hóa đơn hiệu chỉnh.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Một giá trị thực tế doanh số chưa lập hóa đơn có giá trị âm từ khoản tiền trả trước hoặc tạm ứng còn lại được hiệu chỉnh, sẽ được sử dụng để điều hòa trên các hóa đơn sau này.
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
Hóa đơn mốc hoặc trạng thái thanh toán trên mục mô tả hợp đồng dự án được cập nhật thành **Đã sẵn sàng để lập hóa đơn**.
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
Không Được hỗ trợ </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Các khoản tín dụng và hiệu chỉnh của một mục mô tả hợp đồng dựa trên sản phẩm đã lập hóa đơn trước đây.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Không Được hỗ trợ </p>
            </td>
        </tr>
    </tbody>
</table>
