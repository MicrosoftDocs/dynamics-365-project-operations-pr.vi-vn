---
title: Tổng quan về giá trị thực tế
description: Bài viết này cung cấp thông tin về thực tế dự án.
author: rumant
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 08/03/2020
ms.topic: overview
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 35282e6c51fff28dbbb0a5a7de760788416ed0e4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929102"
---
# <a name="actuals-overview"></a>Tổng quan về giá trị thực tế

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Thực tế là lượng công việc đã hoàn thành trên một dự án. Có thể truy nguyên thực tế dự án theo tài liệu nguồn. Các tài liệu nguồn đó bao gồm mục nhập thời gian, chi phí và nhật ký cũng như hóa đơn.

![Cách truy nguyên thực tế dự án theo tài liệu nguồn.](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a>Gửi mục nhập thời gian

Trong PSA, khi một mục thời gian được gửi cho một dự án được ánh xạ tới một dòng hợp đồng thời gian và vật tư, hai dòng nhật ký kế toán sẽ được tạo. Một dòng dành cho chi phí và dòng còn lại dành cho bán hàng chưa lập hóa đơn. Khi một mục thời gian được gửi cho một dự án được ánh xạ tới một dòng hợp đồng giá cố định, thì dòng nhật ký kế toán chỉ được tạo cho chi phí. 

Logic để nhập giá mặc định nằm trên dòng nhật ký kế toán. Tất cả các giá trị trường từ một mục nhập thời gian được sao chép vào dòng nhật ký kế toán. Các trường này bao gồm ngày giao dịch, dòng hợp đồng mà dự án được ánh xạ tới và kết quả tiền tệ trong bảng giá phù hợp. 

Các trường ảnh hưởng đến giá mặc định, chẳng hạn như **Vai trò** và **Đơn vị tổ chức** có thể khiến một mức giá phù hợp được nhập vào dòng nhật ký kế toán theo mặc định. Nếu bạn thêm một trường tùy chỉnh vào mục nhập thời gian và bạn muốn điền vào thực tế, hãy tạo trường đó trên thực thể Thực tế và sử dụng ánh xạ trường để sao chép trường từ mục nhập thời gian tới thực tế.

## <a name="submitting-an-expense-entry"></a>Gửi một mục nhập chi phí

Trong PSA, khi một mục nhập chi phí được gửi cho một dự án được ánh xạ tới một dòng hợp đồng thời gian và vật tư, hai dòng nhật ký kế toán sẽ được tạo. Một dòng dành cho chi phí và dòng còn lại dành cho bán hàng chưa lập hóa đơn. Khi một mục nhập chi phí được gửi cho một dự án được ánh xạ tới một dòng hợp đồng giá cố định, thì dòng nhật ký kế toán chỉ được tạo cho chi phí.

Logic để nhập giá mặc định cho chi phí dựa trên loại chi phí được chọn trên trang **Mục nhập chi phí**. Ngày giao dịch, dòng hợp đồng mà dự án được ánh xạ tới và tiền tệ được dùng để xác định bảng giá phù hợp. Tuy nhiên, đối với giá, số tiền mà người dùng nhập được đặt trực tiếp trên dòng nhật ký kế toán chi phí liên quan cho chi phí và bán hàng theo mặc định.

Trong phiên bản hiện tại của PSA, mục nhập dựa trên danh mục của giá mặc định cho mỗi đơn vị các mục nhập chi phí không khả dụng.

## <a name="using-entry-journals-to-record-costs"></a>Sử dụng nhật ký Mục nhập để ghi lại chi phí

Trong PSA, nhật ký Mục nhập cho phép bạn ghi lại chi phí hoặc doanh thu trong lớp giao dịch thuế, chi phí, thời gian, phí hoặc vật tư. Nhật ký kế toán có tiêu đề, các dòng và hành động **Xác nhận**. Dưới đây là một số tình huống mà bạn có thể sử dụng một nhật ký kế toán:

- Bạn phải ghi lại các chi phí vật tư thực tế và bán hàng trên một dự án.
- Bạn phải di chuyển thực tế giao dịch từ một hệ thống khác sang PSA.
- Bạn phải ghi lại chi phí xảy ra trong một hệ thống khác, chẳng hạn như mua sắm hoặc chi phí thầu phụ.

> [!IMPORTANT]
> Chỉ người dùng nhận biết đầy đủ về tác động kế toán của Thực tế đối với dự án mới có thể dùng nhật ký Mục nhập để tạo thực thể Thực tế. Điều này là do ứng dụng không xác nhận loại dòng nhật ký kế toán hoặc giá liên quan được nhập vào dòng nhật ký kế toán. Do tác động của loại nhật ký này, hãy thận trọng đối với người được cấp quyền truy cập để tạo nhật ký Mục nhập.     


## <a name="recording-actuals-based-on-project-events"></a>Ghi lại thực tế dựa trên sự kiện dự án

PSA ghi lại các giao dịch tài chính xảy ra trong một dự án. Các giao dịch này được ghi lại là **thực tế**. Các bảng sau đây hiển thị các loại thực tế khác nhau được tạo, phụ thuộc vào việc dự án là dự án thời gian và vật tư hay giá cố định, ở giai đoạn trước khi bán hàng hay là dự án nội bộ.

**Tài nguyên thuộc về cùng một đơn vị tổ chức như đơn vị hợp đồng của dự án**

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

**Tài nguyên thuộc về một đơn vị tổ chức khác với đơn vị hợp đồng của dự án**

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
