---
title: Đơn đặt hàng cho dự án
description: Bài viết này mô tả các phương thức khác nhau mà bạn có thể sử dụng để tạo đơn đặt hàng cho một dự án. Phương thức bạn dùng tùy vào mục đích của đơn đặt hàng và khi mặt hàng đã mua được tiêu dùng và tính phí cho dự án.
author: Yowelle
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd891aec5bcab66c5801a5d9ca8abbbf632d662d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087096"
---
# <a name="purchase-orders-for-a-project"></a>Đơn đặt hàng cho dự án

[!include [banner](../includes/banner.md)]

Bài viết này mô tả các phương thức khác nhau mà bạn có thể sử dụng để tạo đơn đặt hàng cho một dự án. Phương thức bạn dùng tùy vào mục đích của đơn đặt hàng và khi mặt hàng đã mua được tiêu dùng và tính phí cho dự án.

### <a name="methods-for-creating-a-purchase-order"></a>Phương thức tạo đơn đặt hàng

Bạn có thể sử dụng một trong các phương pháp sau để tạo đơn đặt hàng trong Quản lý dự án và kế toán. Mục đích của đơn đặt hàng sẽ xác định thời điểm cần thực hiện đơn đặt hàng và từ đó xác định khi nào tính phí mặt hàng vào dự án.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Phương pháp</th>
<th>Mục đích</th>
<th>Tiêu thụ mặt hàng</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Tạo đơn đặt hàng trực tiếp từ dự án.</td>
<td>Sử dụng phương thức này để mua mặt hàng từ nhà cung cấp bên ngoài để tiêu dùng cho một dự án. Bạn có thể tạo đơn đặt hàng theo hai cách:
<ul>
<li>Từ chính dự án. Trong trường hợp này, dự án đã được xác định cho đơn đặt hàng.</li>
<li>Bằng cách điều hướng đến đơn đặt hàng của dự án. Bạn phải chọn cả nhà cung cấp và dự án để tạo đơn đặt hàng.</li>
</ul></td>
<td>Mặt hàng được tiêu thụ khi hóa đơn của nhà cung cấp được cập nhật.</td>
</tr>
<tr class="even">
<td>Tạo đơn đặt hàng từ đơn bán hàng.</td>
<td>Sử dụng phương thức này để mua mặt hàng khi bạn tạo đơn bán hàng từ dự án.</td>
<td>Mặt hàng được tiêu thụ khi đơn bán hàng được lập hóa đơn cho khách hàng.</td>
</tr>
<tr class="odd">
<td>Tạo đơn đặt hàng từ yêu cầu về mặt hàng.</td>
<td>Sử dụng phương thức này để mua mặt hàng khi bạn tạo yêu cầu mặt hàng từ dự án.</td>
<td>Mặt hàng được tiêu thụ khi phiếu đóng gói cho yêu cầu về mặt hàng được cập nhật.</td>
</tr>
</tbody>
</table>

> [!NOTE] 
> Khi bạn cập nhật hóa đơn của nhà cung cấp hoặc phiếu đóng gói, bạn sẽ được nhắc cập nhật phiếu đóng gói theo yêu cầu mặt hàng.

Để biết thêm thông tin, hãy xem [Nhận các mặt hàng theo đơn đặt hàng từ yêu cầu mặt hàng](tasks/receive-items-purchase-order-item-requirement.md).

