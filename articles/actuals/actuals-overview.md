---
title: Thực tế
description: Chủ đề này cung cấp thông tin về cách làm việc với giá trị thực tế trong Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 78c7a9486d0338adfd7770447f21d17509e654f7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996637"
---
# <a name="actuals"></a>Thực tế 

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/vật tư không tồn kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Giá trị thực tế đại diện cho tiến độ tài chính và lịch trình đã được xem xét và phê duyệt trên một dự án. Chúng được tạo ra do thời gian, chi phí, các mục nhập mức sử dụng vật tư, bút toán và hóa đơn được phê duyệt.

## <a name="journal-lines-and-time-submission"></a>Dòng nhật ký kế toán và thời gian gửi

Để biết thêm thông tin về mục nhập thời gian, hãy xem [Tổng quan về mục nhập thời gian](../time/time-entry-overview.md).

### <a name="time-and-materials"></a>Thời gian và vật tư

Khi một mục nhập thời gian đã gửi được liên kết với một dự án ánh xạ tới mô tả hợp đồng thời gian và vật tư, hệ thống sẽ tạo ra hai dòng nhật ký kế toán, một dòng cho chi phí và một dòng cho doanh số chưa lập hóa đơn.

### <a name="fixed-price"></a>Giá cố định

Khi một mục nhập thời gian được gửi được liên kết với một dự án được ánh xạ tới một mô tả hợp đồng giá cố định, thì hệ thống sẽ tạo ra một mô tả hợp đồng cho chi phí.

### <a name="default-pricing"></a>Giá mặc định

Logic để tạo giá mặc định nằm trên dòng nhật ký kế toán. Các giá trị trường từ mục nhập thời gian được sao chép vào dòng nhật ký kế toán. Các giá trị này bao gồm ngày giao dịch, mô tả hợp đồng mà dự án được ánh xạ và kết quả tiền tệ trong bảng giá phù hợp.

Các trường ảnh hưởng đến giá mặc định, chẳng hạn như **Vai trò** và **Đơn vị nguồn lực** được dùng để xác định mức giá phù hợp trên dòng nhật ký kế toán. Bạn có thể thêm trường tùy chỉnh trên mục nhập thời gian. Nếu bạn muốn giá trị trường được điền vào giá trị thực tế, hãy tạo trường trong các bảng **Giá trị thực tế** và **Dòng nhật ký kế toán**. Sử dụng mã tùy chỉnh để điền giá trị trường đã chọn từ Mục nhập thời gian vào Giá trị thực tế thông qua dòng nhật ký kế toán bằng cách sử dụng nguồn gốc giao dịch. Để biết thêm thông tin về nguồn gốc và kết nối giao dịch, hãy xem [Liên kết Giá trị thực tế với bản ghi gốc](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="journal-lines-and-basic-expense-submission"></a>Các dòng nhật ký kế toán và nộp chi phí cơ bản

Để biết thêm thông tin về mục nhập chi phí, hãy xem [Tổng quan về chi phí](../expense/expense-overview.md).

### <a name="time-and-materials"></a>Thời gian và vật tư

Khi một mục nhập chi phí cơ bản đã gửi đi được liên kết với một dự án ánh xạ tới mô tả hợp đồng thời gian và vật tư, hệ thống sẽ tạo ra hai dòng nhật ký kế toán, một dòng cho chi phí và một dòng cho doanh số chưa lập hóa đơn.

### <a name="fixed-price"></a>Giá cố định

Khi một mục nhập chi phí cơ bản đã gửi liên kết với một dự án được ánh xạ tới một mô tả hợp đồng giá cố định, thì hệ thống sẽ tạo một dòng nhật ký kế toán cho chi phí.

### <a name="default-pricing"></a>Giá mặc định

Logic để nhập giá mặc định cho các chi phí dựa trên danh mục chi phí. Ngày giao dịch, mô tả hợp đồng mà dự án được ánh xạ tới và tiền tệ đều được dùng để xác định bảng giá phù hợp. Các trường ảnh hưởng đến giá mặc định, chẳng hạn như **Thể loại giao dịch** và **Đơn vị** được dùng để xác định mức giá phù hợp trên dòng nhật ký kế toán. Tuy nhiên, điều này chỉ có tác dụng khi phương pháp định giá trong danh sách giá là **Đơn giá**. Nếu phương pháp định giá là **Theo chi phí** hoặc **Tăng trên chi phí**, thì giá được nhập khi tạo mục nhập chi phí sẽ được dùng cho chi phí và giá trên dòng nhật ký kế toán về doanh số sẽ được tính theo phương pháp định giá. 

Bạn có thể thêm một trường tùy chỉnh vào mục nhập chi phí. Nếu bạn muốn giá trị trường được điền vào giá trị thực tế, hãy tạo trường trong các bảng **Giá trị thực tế** và **Dòng nhật ký kế toán**. Sử dụng mã tùy chỉnh để điền giá trị trường đã chọn từ Mục nhập thời gian vào Giá trị thực tế thông qua dòng nhật ký kế toán bằng cách sử dụng nguồn gốc giao dịch. Để biết thêm thông tin về nguồn gốc và kết nối giao dịch, hãy xem [Liên kết Giá trị thực tế với bản ghi gốc](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="journal-lines-and-material-usage-log-submission"></a>Các dòng nhật ký kế toán và việc gửi nhật ký sử dụng vật tư

Để biết thêm thông tin về mục nhập chi phí, hãy xem [Nhật ký sử dụng vật tư](../material/material-usage-log.md).

### <a name="time-and-materials"></a>Thời gian và vật tư

Khi một mục nhập nhật ký sử dụng vật tư đã gửi liên kết với một dự án được ánh xạ tới mô tả hợp đồng thời gian và vật tư, hệ thống sẽ tạo ra hai dòng nhật ký kế toán, một dòng cho chi phí và một dòng cho doanh số chưa lập hóa đơn.

### <a name="fixed-price"></a>Giá cố định

Khi một mục nhập nhật ký sử dụng vật tư đã gửi liên kết với một dự án được ánh xạ tới một mô tả hợp đồng giá cố định, thì hệ thống sẽ tạo một dòng nhật ký kế toán cho chi phí.

### <a name="default-pricing"></a>Giá mặc định

Logic để nhập giá mặc định cho vật tư dựa trên sự kết hợp giữa sản phẩm và đơn vị. Ngày giao dịch, mô tả hợp đồng mà dự án được ánh xạ tới và tiền tệ đều được dùng để xác định bảng giá phù hợp. Các trường ảnh hưởng đến giá mặc định, chẳng hạn như **ID sản phẩm** và **Đơn vị** được dùng để xác định mức giá phù hợp trên dòng nhật ký kế toán. Tuy nhiên, điều này chỉ áp dụng cho các sản phẩm trong danh mục. Đối với sản phẩm chọn thêm, giá được nhập khi tạo mục nhập nhật ký sử dụng vật tư được dùng cho chi phí và giá bán trên các dòng nhật ký kế toán. 

Bạn có thể thêm một trường tùy chỉnh vào mục nhập **Nhật ký sử dụng vật tư**. Nếu bạn muốn giá trị trường được điền vào giá trị thực tế, hãy tạo trường trong các bảng **Giá trị thực tế** và **Dòng nhật ký kế toán**. Sử dụng mã tùy chỉnh để điền giá trị trường đã chọn từ Mục nhập thời gian vào Giá trị thực tế thông qua dòng nhật ký kế toán bằng cách sử dụng nguồn gốc giao dịch. Để biết thêm thông tin về nguồn gốc và kết nối giao dịch, hãy xem [Liên kết Giá trị thực tế với bản ghi gốc](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="use-entry-journals-to-record-costs"></a>Sử dụng bút toán để ghi lại chi phí

Bạn có thể sử dụng bút toán để ghi lại chi phí hoặc doanh thu trong lớp giao dịch thuế, chi phí, thời gian, phí hoặc vật tư. Có thể sử dụng nhật ký cho các mục đích sau:

- Di chuyển các giá trị thực tế của giao dịch từ một hệ thống khác sang Microsoft Dynamics 365 Project Operations.
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
