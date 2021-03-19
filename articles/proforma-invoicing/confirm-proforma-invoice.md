---
title: Xác nhận hóa đơn ước giá
description: Chủ đề này cung cấp thông tin về việc xác nhận hóa đơn ước giá.
author: rumant
manager: AnnBe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b2ed241509d2643d841ce55777e6e316612f70b8
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287894"
---
# <a name="confirm-a-proforma-invoice"></a>Xác nhận hóa đơn ước giá

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Sau khi hóa đơn ước giá được xác nhận, trạng thái của hóa đơn dự án được cập nhật thành **Đã xác nhận**. Khi hóa đơn được xác nhận, mục đó sẽ trở thành dạng chỉ đọc. Sau này, hóa đơn chỉ có thể được hiệu chỉnh nếu có bất kỳ sự chỉnh sửa hoặc ghi có nào do khách hàng thực hiện hoặc khi hóa đơn được đánh dấu là đã thanh toán.

Bảng sau liệt kê các giá trị thực tế được hệ thống tạo. Các giá trị thực tế này được tạo ra khi một số hoạt động nhất định được thực hiện trên hóa đơn dự án nháp trước khi mục đó được xác nhận.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="416" valign="top">
                <p>
                    <strong>Kịch bản</strong>
                </p>
            </td>
            <td width="608" valign="top">
                <p>
                    <strong>Giá trị thực tế được tạo khi xác nhận</strong>
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
Giá trị thực tế doanh số chưa lập hóa đơn mới, có thể tính phí cho số giờ và số tiền trên chi tiết mô tả hóa đơn đã sửa, khoản đảo ngược của giá trị thực tế doanh số chưa lập hóa đơn và giá trị thực tế doanh số đã lập hóa đơn tương đương.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Giá trị thực tế doanh số chưa lập hóa đơn mới, không thể tính phí cho số giờ và số tiền còn lại sau khi trừ số liệu đã hiệu chỉnh trên chi tiết mô tả hóa đơn đã sửa, khoản đảo ngược của giá trị thực tế doanh số chưa lập hóa đơn và giá trị thực tế doanh số đã lập hóa đơn tương đương.
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
Một giá trị thực tế doanh số đã lập hóa đơn cho số lượng và số tiền khi phê duyệt chi phí ban đầu.
                </p>
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
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]