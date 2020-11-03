---
title: Thực tế
description: Chủ đề này cung cấp thông tin về cách làm việc với giá trị thực tế trong Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 93a945ffbe9c6dd998456b506b95e717ab8fbab7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087098"
---
# <a name="actuals"></a>Thực tế 

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Thực tế là lượng công việc đã hoàn thành trên một dự án. Chúng được tạo ra do kết quả của mục nhập thời gian và chi phí, bút toán và hóa đơn.

## <a name="journal-lines-and-time-submission"></a>Dòng nhật ký kế toán và thời gian gửi

Để biết thêm thông tin về mục nhập thời gian, hãy xem [Tổng quan về mục nhập thời gian](../time/time-entry-overview.md).

### <a name="time-and-materials"></a>Thời gian và vật tư

Khi một mục nhập thời gian đã gửi được liên kết với một dự án ánh xạ tới mô tả hợp đồng thời gian và vật tư, hệ thống sẽ tạo ra hai dòng nhật ký kế toán, một dòng cho chi phí và một dòng cho doanh số chưa lập hóa đơn.

### <a name="fixed-price"></a>Giá cố định

Khi một mục nhập thời gian được gửi được liên kết với một dự án được ánh xạ tới một mô tả hợp đồng giá cố định, thì hệ thống sẽ tạo ra một mô tả hợp đồng cho chi phí.

### <a name="default-pricing"></a>Giá mặc định

Logic để tạo giá mặc định nằm trên dòng nhật ký kế toán. Các giá trị trường từ mục nhập thời gian được sao chép vào dòng nhật ký kế toán. Các giá trị này bao gồm ngày giao dịch, mô tả hợp đồng mà dự án được ánh xạ và kết quả tiền tệ trong bảng giá phù hợp.

Các trường ảnh hưởng đến giá mặc định, chẳng hạn như **Vai trò** và **Đơn vị tổ chức** được sử dụng để xác định giá thích hợp trên dòng nhật ký kế toán. Bạn có thể thêm trường tùy chỉnh trên mục nhập thời gian. Nếu bạn muốn điền giá trị trường vào giá trị thực tế, hãy tạo trường đó trên thực thể Thực tế và sử dụng ánh xạ trường để sao chép trường từ mục nhập thời gian tới giá trị thực tế.

## <a name="journal-lines-and-basic-expense-submission"></a>Các dòng nhật ký kế toán và nộp chi phí cơ bản

Để biết thêm thông tin về mục nhập chi phí, hãy xem [Tổng quan về chi phí](../expense/expense-overview.md).

### <a name="time-and-materials"></a>Thời gian và vật tư

Khi một mục nhập chi phí cơ bản đã gửi đi được liên kết với một dự án ánh xạ tới mô tả hợp đồng thời gian và vật tư, hệ thống sẽ tạo ra hai dòng nhật ký kế toán, một dòng cho chi phí và một dòng cho doanh số chưa lập hóa đơn.

### <a name="fixed-price"></a>Giá cố định

Khi một mục nhập chi phí cơ bản được gửi được liên kết với một dự án được ánh xạ tới một mô tả hợp đồng giá cố định, thì hệ thống sẽ tạo ra một dòng nhật ký kế toán cho chi phí.

### <a name="default-pricing"></a>Giá mặc định

Logic để nhập giá mặc định cho các chi phí dựa trên danh mục chi phí. Ngày giao dịch, dòng hợp đồng mà dự án được ánh xạ tới và tiền tệ được dùng để xác định bảng giá phù hợp. Tuy nhiên, theo mặc định, số tiền mà người dùng nhập cho giá được đặt trực tiếp trên dòng nhật ký kế toán chi phí liên quan cho chi phí và bán hàng.

Mục nhập dựa trên danh mục của giá mặc định cho mỗi đơn vị trên các mục nhập chi phí không khả dụng.

## <a name="use-entry-journals-to-record-costs"></a>Sử dụng bút toán để ghi lại chi phí

Bạn có thể sử dụng bút toán để ghi lại chi phí hoặc doanh thu trong lớp giao dịch thuế, chi phí, thời gian, phí hoặc vật tư. Có thể sử dụng nhật ký cho các mục đích sau:

- Ghi lại chi phí vật tư thực tế và bán hàng trên một dự án.
- Di chuyển thực tế giao dịch từ một hệ thống khác sang Microsoft Dynamics 365 Project Operations.
- Ghi lại chi phí đã xảy ra trong hệ thống khác. Các chi phí này có thể bao gồm chi phí mua sắm hoặc chi phí thầu phụ.

> [!IMPORTANT]
> Ứng dụng không xác nhận dòng nhật ký kế toán hoặc giá cả liên quan được nhập trên dòng nhật ký kế toán. Do đó, chỉ người dùng có nhận thức đầy đủ về tác động kế toán mà các giá trị thực tế có đối với dự án mới được sử dụng bút toán để tạo các giá trị thực tế. Do tác động của loại nhật ký này, bạn nên cẩn thận chọn người có quyền truy cập để tạo bút toán.
## <a name="record-actuals-based-on-project-events"></a>Ghi lại thực tế dựa trên sự kiện dự án

Project Operations ghi lại các giao dịch tài chính xảy ra trong một dự án. Các giao dịch này được ghi lại là thực tế. Các bảng sau đây hiển thị các loại thực tế khác nhau được tạo, phụ thuộc vào việc dự án là dự án thời gian và vật tư hay giá cố định, ở giai đoạn trước khi bán hàng hay là dự án nội bộ.

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a>Tài nguyên thuộc về cùng một đơn vị tổ chức như đơn vị hợp đồng của dự án

<table>
<thead>
<tr>
<th rowspan="3">Sự kiện</th>
<th colspan="4">Dự án có thể lập hóa đơn hoặc đã bán</th>
<th rowspan="3">Dự án trong giai đoạn trước khi bán</th>
<th rowspan="3">Dự án nội bộ</th>
</tr>
<tr>
<th colspan="2">Thời gian và vật tư</th>
<th colspan="2">Giá cố định</th>
</tr>
<tr>
<th>Thực tế</th>
<th>Loại tiền giao dịch</th>
<th>Giá cố định</th>
<th>Loại tiền giao dịch</th>
</tr>
</thead>
<tbody>
<tr>
<td>Mục nhập thời gian được tạo.</td>
<td colspan="6">Không có hoạt động trong thực thể Thực tế</td>
</tr>
<tr>
<td>Mục nhập thời gian được gửi.</td>
<td colspan="6">Không có hoạt động trong thực thể Thực tế</td>
</tr>
<tr>
<td rowspan="2">Thời gian được phê duyệt và số giờ có thể lập hóa đơn sẽ không thay đổi hay tăng trong quá trình phê duyệt.</td>
<td>Thực tế chi phí</td>
<td>Tiền tệ của đơn vị hợp đồng</td>
<td rowspan="2">Thực tế chi phí</td>
<td rowspan="2">Tiền tệ của đơn vị hợp đồng
<td rowspan="2">Thực tế chi phí</td>
<td rowspan="2">Thực tế chi phí</td>
</tr>
<tr>
<td>Thực tế bán hàng chưa lập hóa đơn – Có thể tính phí</td>
<td>Tiền tệ hợp đồng dự án</td>
</tr>
<tr>
<td rowspan="3">Thời gian được phê duyệt và số giờ có thể lập hóa đơn giảm trong quá trình phê duyệt.</td>
<td>Thực tế chi phí</td>
<td>Tiền tệ của đơn vị hợp đồng</td>
<td rowspan="3">Thực tế chi phí</td>
<td rowspan="3">Tiền tệ của đơn vị hợp đồng</td>
<td rowspan="3">Thực tế chi phí</td>
<td rowspan="3">Thực tế chi phí</td>
</tr>
<tr>
<td>Thực tế bán hàng chưa lập hóa đơn – Có thể tính phí cho số lượng mới</td>
<td>Tiền tệ hợp đồng dự án</td>
</tr>
<tr>
<td>Thực tế bán hàng chưa lập hóa đơn – Không thể tính phí cho phần chênh lệch</td>
<td>Tiền tệ hợp đồng dự án</td>
</tr>
<tr>
<td rowspan="2">Hóa đơn được xác nhận, số giờ có thể lập hóa đơn sẽ không thay đổi hay tăng.</td>
<td>Đảo ngược bán hàng chưa lập hóa đơn</td>
<td>Tiền tệ hợp đồng dự án</td>
<td rowspan="2">Doanh số đã lập hóa đơn cho mốc quan trọng</td>
<td rowspan="2">Tiền tệ hợp đồng dự án</td>
<td rowspan="2">Không áp dụng</td>
<td rowspan="2">Không áp dụng</td>
</tr>
<tr>
<td>Doanh số đã lập hóa đơn</td>
<td>Tiền tệ hợp đồng dự án</td>
</tr>
<tr>
<td rowspan="3">Hóa đơn được xác nhận, số giờ có thể lập hóa đơn giảm.</td>
<td>Đảo ngược bán hàng chưa lập hóa đơn</td>
<td>Tiền tệ hợp đồng dự án</td>
<td rowspan="3">Không áp dụng</td>
<td rowspan="3">Không áp dụng</td>
<td rowspan="3">Không áp dụng</td>
<td rowspan="3">Không áp dụng</td>
</tr>
<tr>
<td>Doanh số chưa lập hóa đơn – Có thể tính phí cho số lượng mới</td>
<td>Tiền tệ hợp đồng dự án</td>
</tr>
<tr>
<td>Doanh số chưa lập hóa đơn – Không thể tính phí cho phần chênh lệch</td>
<td>Tiền tệ hợp đồng dự án</td>
</tr>
<tr>
<td rowspan="2">Hóa đơn được sửa để tăng số lượng có thể tính phí.</td>
<td>Doanh số đã tính phí – Đảo ngược</td>
<td>Tiền tệ hợp đồng dự án</td>
<td rowspan="5">
<ul>
<li>Đảo ngược doanh số đã lập hóa đơn cho mốc quan trọng</li>
<li>Thay đổi trạng thái mốc quan trọng từ <strong>Đã lập hóa đơn</strong> thành <strong>Sẵn sàng lập hóa đơn</strong></li>
</ul>
</td>
<td rowspan="5">Tiền tệ hợp đồng dự án</td>
<td rowspan="5">Không áp dụng</td>
<td rowspan="5">Không áp dụng</td>
</tr>
<tr>
<td>Doanh số đã lập hóa đơn</td>
<td>Tiền tệ hợp đồng dự án</td>
</tr>
<tr>
<td rowspan="3">Hóa đơn được sửa để giảm số lượng có thể tính phí.</td>
<td>Doanh số đã tính phí – Đảo ngược</td>
<td>Tiền tệ hợp đồng dự án</td>
</tr>
<tr>
<td>Doanh số chưa lập hóa đơn cho số lượng mới</td>
<td>Tiền tệ hợp đồng dự án</td>
</tr>
<tr>
<td>Doanh số chưa lập hóa đơn – Có thể tính phí cho phần chênh lệch</td>
<td>Tiền tệ hợp đồng dự án</td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a>Tài nguyên thuộc về một đơn vị tổ chức khác với đơn vị hợp đồng của dự án

<table>
<thead>
<tr>
<th rowspan="3">Sự kiện</th>
<th colspan="4">Dự án có thể lập hóa đơn hoặc đã bán</th>
<th rowspan="3">Dự án trong giai đoạn trước khi bán</th>
<th rowspan="3">Dự án nội bộ</th>
</tr>
<tr>
<th colspan="2">Thời gian và vật tư</th>
<th colspan="2">Giá cố định</th>
</tr>
<tr>
<th>Thực tế</th>
<th>Loại tiền giao dịch</th>
<th>Giá cố định</th>
<th>Loại tiền giao dịch</th>
</tr>
</thead>
<tbody>
<tr>
<td>Mục nhập thời gian được tạo.</td>
<td colspan="6">Không có hoạt động trong thực thể Thực tế</td>
</tr>
<tr>
<td>Mục nhập thời gian được gửi.</td>
<td colspan="6">Không có hoạt động trong thực thể Thực tế</td>
</tr>
<tr>
<td rowspan="4">Thời gian được phê duyệt và số giờ có thể lập hóa đơn sẽ không thay đổi hay tăng trong quá trình phê duyệt.</td>
<td>Thực tế chi phí</td>
<td>Tiền tệ của đơn vị hợp đồng</td>
<td rowspan="4">Thực tế chi phí</td>
<td rowspan="4">Tiền tệ của đơn vị hợp đồng</td>
<td rowspan="4">Thực tế chi phí</td>
<td rowspan="4">Thực tế chi phí</td>
</tr>
<tr>
<td>Thực tế bán hàng chưa lập hóa đơn – Có thể tính phí</td>
<td>Tiền tệ hợp đồng dự án</td>
</tr>
<tr>
<td>Chi phí đơn vị nguồn lực</td>
<td>Tiền tệ đơn vị nguồn lực</td>
</tr>
<tr>
<td>Bán hàng liên tổ chức</td>
<td>Tiền tệ của đơn vị hợp đồng</td>
</tr>
<tr>
<td rowspan="5">Thời gian được phê duyệt và số giờ có thể lập hóa đơn giảm trong quá trình phê duyệt.</td>
<td>Thực tế chi phí</td>
<td>Tiền tệ của đơn vị hợp đồng</td>
<td rowspan="5">Thực tế chi phí</td>
<td rowspan="5">Tiền tệ của đơn vị hợp đồng</td>
<td rowspan="5">Thực tế chi phí</td>
<td rowspan="5">Thực tế chi phí</td>
</tr>
<tr>
<td>Chi phí đơn vị nguồn lực</td>
<td>Tiền tệ đơn vị nguồn lực</td>
</tr>
<tr>
<td>Bán hàng liên tổ chức</td>
<td>Tiền tệ của đơn vị hợp đồng</td>
</tr>
<tr>
<td>Thực tế bán hàng chưa lập hóa đơn – Có thể tính phí cho số lượng mới</td>
<td>Tiền tệ hợp đồng dự án</td>
</tr>
<tr>
<td>Thực tế bán hàng chưa lập hóa đơn – Không thể tính phí cho phần chênh lệch</td>
<td>Tiền tệ hợp đồng dự án</td>
</tr>
<tr>
<td rowspan="2">Hóa đơn được xác nhận, số giờ có thể lập hóa đơn sẽ không thay đổi hay tăng.</td>
<td>Đảo ngược bán hàng chưa lập hóa đơn</td>
<td>Tiền tệ hợp đồng dự án</td>
<td rowspan="2">Doanh số đã lập hóa đơn cho mốc quan trọng</td>
<td rowspan="2">Tiền tệ hợp đồng dự án</td>
<td rowspan="2">Không áp dụng</td>
<td rowspan="2">Không áp dụng</td>
</tr>
<tr>
<td>Doanh số đã lập hóa đơn</td>
<td>Tiền tệ hợp đồng dự án</td>
</tr>
<tr>
<td rowspan="3">Hóa đơn được xác nhận, số giờ có thể lập hóa đơn giảm.</td>
<td>Đảo ngược bán hàng chưa lập hóa đơn</td>
<td>Tiền tệ hợp đồng dự án</td>
<td rowspan="3">Không áp dụng</td>
<td rowspan="3">Không áp dụng</td>
<td rowspan="3">Không áp dụng</td>
<td rowspan="3">Không áp dụng</td>
</tr>
<tr>
<td>Doanh số chưa lập hóa đơn – Có thể tính phí cho số lượng mới</td>
<td>Tiền tệ hợp đồng dự án</td>
</tr>
<tr>
<td>Doanh số chưa lập hóa đơn – Không thể tính phí cho phần chênh lệch</td>
<td>Tiền tệ hợp đồng dự án</td>
</tr>
<tr>
<td rowspan="2">Hóa đơn được sửa để tăng số lượng có thể tính phí.</td>
<td>Doanh số đã tính phí – Đảo ngược</td>
<td>Tiền tệ hợp đồng dự án</td>
<td rowspan="5">
<ul>
<li>Đảo ngược doanh số đã lập hóa đơn cho mốc quan trọng</li>
<li>Thay đổi trạng thái mốc quan trọng từ <strong>Đã lập hóa đơn</strong> thành <strong>Sẵn sàng lập hóa đơn</strong></li>
</ul>
</td>
<td rowspan="5">Tiền tệ hợp đồng dự án</td>
<td rowspan="5">Không áp dụng</td>
<td rowspan="5">Không áp dụng</td>
</tr>
<tr>
<td>Doanh số đã lập hóa đơn</td>
<td>Tiền tệ hợp đồng dự án</td>
</tr>
<tr>
<td rowspan="3">Hóa đơn được sửa để giảm số lượng có thể tính phí.</td>
<td>Doanh số đã tính phí – Đảo ngược</td>
<td>Tiền tệ hợp đồng dự án</td>
</tr>
<tr>
<td>Doanh số chưa lập hóa đơn cho số lượng mới</td>
<td>Tiền tệ hợp đồng dự án</td>
</tr>
<tr>
<td>Doanh số chưa lập hóa đơn – Có thể tính phí cho phần chênh lệch</td>
<td>Tiền tệ hợp đồng dự án</td>
</tr>
</tbody>
</table>
