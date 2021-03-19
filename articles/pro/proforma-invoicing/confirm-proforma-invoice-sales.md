---
title: Xác nhận hóa đơn ước giá - bản đơn giản
description: Chủ đề này cung cấp thông tin về việc xác nhận hóa đơn ước giá trong Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3b1818f20a0d54848939b689f87986154943c57a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274304"
---
# <a name="confirm-a-proforma-invoice---lite"></a>Xác nhận hóa đơn ước giá - bản đơn giản

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_


Sau khi hóa đơn ước giá được xác nhận, trạng thái của hóa đơn dự án được cập nhật thành **Đã xác nhận**. Khi hóa đơn được xác nhận, mục đó sẽ trở thành dạng chỉ đọc. Từ giờ trở đi, hóa đơn chỉ có thể được hiệu chỉnh nếu có bất kỳ sự chỉnh sửa hoặc ghi có nào do khách hàng thực hiện hoặc nếu hóa đơn được đánh dấu là đã thanh toán.

Bảng sau liệt kê các giá trị thực tế được hệ thống tạo. Các giá trị thực tế này được tạo ra khi một số hoạt động nhất định được thực hiện trên hóa đơn dự án nháp trước khi mục đó được xác nhận.

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
Lập hóa đơn khoản tạm ứng hoặc trả trước </p>
            </td>
            <td width="408" valign="top">
                <p>
Giá trị thực tế doanh số được lập hóa đơn thuộc loại <strong>Khoản trả trước</strong> được tạo ra cho số tiền tạm ứng hoặc trả trước.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Một giá trị thực tế doanh số chưa lập hóa đơn tương ứng với giá trị âm của khoản trả trước hoặc tạm ứng sẽ được sử dụng để điều hòa.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Sau khi điều hòa đầy đủ khoản trả trước hoặc tạm ứng trên hóa đơn.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Khoản đảo ngược doanh số chưa lập hóa đơn của số tiền trả trước hoặc tạm ứng đã tạo để điều hòa. Số tiền này là số dương vì nó có tác dụng bù cho giá trị âm được tạo ra khi khoản trả trước hoặc tạm ứng được lập hóa đơn.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Một giá trị thực tế doanh số đã lập hóa đơn cho số tiền trên hóa đơn này.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Sau khi điều hòa một phần khoản trả trước hoặc tạm ứng trên hóa đơn.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Khoản đảo ngược doanh số chưa lập hóa đơn của số tiền trả trước hoặc tạm ứng đã tạo để điều hòa. Số tiền này là số dương vì nó có tác dụng bù cho giá trị âm được tạo ra khi khoản trả trước hoặc tạm ứng được lập hóa đơn.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Một giá trị thực tế doanh số đã lập hóa đơn cho số tiền trên hóa đơn này.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Một giá trị thực tế doanh số chưa lập hóa đơn, có giá trị âm của số tiền trả trước hoặc tạm ứng sẽ được sử dụng để điều hòa trong các hóa đơn sau này.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Lập hóa đơn cho một giao dịch thời gian mà không có bất kỳ chỉnh sửa nào trên hóa đơn nháp.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Một khoản đảo ngược doanh số chưa lập hóa đơn cho số giờ và số tiền khi phê duyệt thời gian ban đầu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Một giá trị thực tế doanh số đã lập hóa đơn cho số giờ và số tiền khi phê duyệt thời gian ban đầu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Lập hóa đơn cho một giao dịch thời gian đã được sửa để giảm số lượng.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Một khoản đảo ngược doanh số chưa lập hóa đơn cho số giờ và số tiền khi phê duyệt thời gian ban đầu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Giá trị thực tế doanh số chưa lập hóa đơn mới, có thể tính phí cho số giờ và số tiền trên chi tiết mô tả hóa đơn đã sửa, khoản đảo ngược của giá trị thực tế doanh số và giá trị thực tế doanh số đã lập hóa đơn tương đương.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Giá trị thực tế doanh số chưa lập hóa đơn mới, không thể tính phí cho số giờ và số tiền còn lại sau khi trừ số liệu đã hiệu chỉnh trên chi tiết mô tả hóa đơn đã sửa, khoản đảo ngược của giá trị thực tế doanh số và giá trị thực tế doanh số đã lập hóa đơn tương đương.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Lập hóa đơn cho một giao dịch thời gian đã được sửa để tăng số lượng.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Một khoản đảo ngược doanh số chưa lập hóa đơn cho số giờ và số tiền khi phê duyệt thời gian ban đầu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Giá trị thực tế doanh số chưa lập hóa đơn mới, có thể tính phí cho số giờ và số tiền trên chi tiết mô tả hóa đơn đã sửa, khoản đảo ngược của giá trị thực tế doanh số chưa lập hóa đơn và giá trị thực tế doanh số đã lập hóa đơn tương đương.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Lập hóa đơn cho một giao dịch chi phí mà không có bất kỳ chỉnh sửa nào trên hóa đơn nháp.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Một khoản đảo ngược doanh số chưa lập hóa đơn cho số lượng và số tiền khi phê duyệt chi phí ban đầu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Một giá trị thực tế doanh số đã lập hóa đơn cho số lượng và số tiền khi phê duyệt chi phí ban đầu </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Lập hóa đơn cho một giao dịch chi phí đã được sửa để giảm số lượng.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Một khoản đảo ngược doanh số chưa lập hóa đơn cho số lượng và số tiền khi phê duyệt chi phí ban đầu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Giá trị thực tế doanh số chưa lập hóa đơn mới, có thể tính phí cho số lượng và số tiền trên chi tiết mô tả hóa đơn đã sửa, khoản đảo ngược của giá trị thực tế doanh số chưa lập hóa đơn và giá trị thực tế doanh số đã lập hóa đơn tương đương.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Giá trị thực tế doanh số chưa lập hóa đơn mới, không thể tính phí cho số lượng và số tiền còn lại sau khi trừ số liệu đã hiệu chỉnh trên chi tiết mô tả hóa đơn đã sửa, khoản đảo ngược của giá trị thực tế doanh số chưa lập hóa đơn và giá trị thực tế doanh số đã lập hóa đơn tương đương.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Lập hóa đơn cho một giao dịch chi phí đã được sửa để tăng số lượng.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Một khoản đảo ngược doanh số chưa lập hóa đơn cho số lượng và số tiền khi phê duyệt chi phí ban đầu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Giá trị thực tế doanh số chưa lập hóa đơn mới, có thể tính phí cho số lượng và số tiền trên chi tiết mô tả hóa đơn đã sửa, khoản đảo ngược của giá trị thực tế doanh số chưa lập hóa đơn và giá trị thực tế doanh số đã lập hóa đơn tương đương. 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Lập hóa đơn một khoản phí.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Một khoản đảo ngược doanh số chưa lập hóa đơn cho số tiền phí trên dòng nhật ký kế toán ban đầu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Một giá trị thực tế doanh số đã lập hóa đơn cho số lượng và số tiền trên dòng nhật ký kế toán phí ban đầu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Lập hóa đơn cho một mốc.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Giá trị thực tế doanh số đã lập hóa đơn cho số tiền mốc trên mốc ban đầu trên mục mô tả hợp đồng dự án.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Lập hóa đơn cho mục mô tả hợp đồng dựa trên sản phẩm.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Giá trị thực tế doanh số được lập hóa đơn cho mục mô tả sản phẩm có số lượng và số tiền từ mục mô tả hợp đồng dựa trên sản phẩm.
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]