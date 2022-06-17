---
title: Tổng quan về mô tả báo giá dựa trên dự án
description: Bài viết này cung cấp thông tin về việc sử dụng các dòng trích dẫn dựa trên dự án cho công việc của dự án.
author: rumant
ms.date: 03/30/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 90c5affa25b113476e43f0bbbadd5c9615f9c05c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934484"
---
# <a name="project-based-quote-lines-overview"></a>Tổng quan về mô tả báo giá dựa trên dự án 

_**Áp dụng cho:** Triển khai bản đơn giản - từ thỏa thuận đến lập hóa đơn ước giá, Project Operations cho các kịch bản dựa trên tài nguyên/không lưu kho_

Các mô tả báo giá dựa trên dự án được thiết kế để giúp ước tính công việc dự án trên một cam kết. Cấu trúc của mô tả báo giá dựa trên dự án được mở rộng cho các ước tính dự án với các khái niệm sau:

- Phương thức Thanh toán
- Ánh xạ dự án và tác vụ
- Các lớp giao dịch được bao gồm
- Giới hạn không vượt quá
- Thiết lập khả năng tính phí
- Ước tính bằng cách sử dụng Chi tiết mô tả báo giá
- Khách hàng trên mô tả báo giá

Bảng sau cung cấp thông tin về các trường trên tab **Tổng quát** của mô tả báo giá dựa trên dự án. Các trường này giúp thiết lập cơ sở để ước tính chi tiết, nền tảng cho công việc dự án.

| **Trường** | **Mô tả** | **Tác động xuôi tuyến** |
| --- | --- | --- |
| Tên | Tên của mục mô tả báo giá giúp bạn xác định thành thành phần riêng rẽ của báo giá đang được ước tính. | Được sao chép vào mô tả hợp đồng dự án tạo từ mô tả báo giá này khi báo giá được chốt. |
| Phương thức Thanh toán | Trên một báo giá tạo từ một cơ hội, giá trị này được sao chép từ trường tương ứng trên mô tả cơ hội. Trường này bao gồm 2 mô hình hợp đồng được hỗ trợ bởi Dynamics 365 Project Operations:</br>- Giá cố định</br>- Thời gian và vật tư.| Giá trị này được sao chép vào mục mô tả hợp đồng dự án được tạo từ mục mô tả báo giá này khi có được báo giá. |
| Dự án | Sử dụng trường tùy chọn này để xác định dự án sẽ được sử dụng để thực hiện công việc trong cam kết này. Khi một dự án được ánh xạ đến một mô tả báo giá, nó sẽ giúp thiết lập các tác vụ có thể tính phí, đồng thời đưa ước tính dựa trên dự án vào mô tả báo giá dưới dạng chi tiết mô tả báo giá. Khi một dự án không được ánh xạ tới mô tả báo giá dựa trên dự án, ước tính sẽ được tạo theo cách thủ công bằng cách tạo chi tiết từng mô tả báo giá. | Giá trị này được sao chép vào mục mô tả hợp đồng dự án được tạo từ mục mô tả báo giá này khi có được báo giá.|
| Các tác vụ được đưa vào | Cho biết mô tả báo giá này được sử dụng cho tất cả hoặc một số tác vụ dự án cho dự án đã chọn. Trường này có các giá trị khả dĩ sau đây:</br>- Tất cả tác vụ dự án</br>- Chỉ các tác vụ dự án đã chọn</br>Giá trị trống trong trường này tương đương với tùy chọn **Tất cả tác vụ dự án**. | Khi **Chỉ các nhiệm vụ dự án đã chọn** được chọn trên trang dự án, tab **Thiết lập thanh toán theo nhiệm vụ** cho phép bạn chọn các nhiệm vụ cụ thể để liên kết chúng với mục mô tả báo giá này. Giá trị này được sao chép vào mục mô tả hợp đồng dự án được tạo từ mục mô tả báo giá này khi có được báo giá. |
| Bao gồm Thời gian | Giá trị **Có**/**Không** cho biết liệu các giao dịch thời gian hoặc chi phí nhân công của dự án đã chọn có được đưa vào phần ước tính trên mục mô tả báo giá này hay không. Giá trị **Không** cho biết rằng giao dịch thời gian hoặc chi phí nhân công sẽ không được bao gồm trong ước tính trên mô tả báo giá này. Giá trị **Có** cho biết rằng giao dịch thời gian hoặc chi phí nhân công sẽ được bao gồm trong ước tính trên mô tả báo giá này. | Giá trị này được sao chép vào mục mô tả hợp đồng dự án được tạo từ mục mô tả báo giá này khi có được báo giá. |
| Bao gồm Chi phí | Giá trị **Có**/**Không** cho biết liệu các chi phí của dự án đã chọn có được đưa vào phần ước tính trên mục mô tả báo giá này hay không. Giá trị **Không** cho biết rằng chi phí phí tổn sẽ không được bao gồm trong ước tính trên mô tả báo giá này. Giá trị **Có** cho biết rằng chi phí phí tổn sẽ được bao gồm trong ước tính trên mô tả báo giá này. | Giá trị này được sao chép vào mục mô tả hợp đồng dự án được tạo từ mục mô tả báo giá này khi có được báo giá. |
| Bao gồm vật liệu | Giá trị **Có**/**Không** cho biết liệu các chi phí vật tư của dự án đã chọn có được đưa vào phần ước tính trên mục mô tả báo giá này hay không. Giá trị **Không** cho biết các chi phí vật tư sẽ không được đưa vào phần ước tính trên mục mô tả báo giá này. Giá trị **Có** cho biết các chi phí vật tư sẽ không được đưa vào phần ước tính trên mục mô tả báo giá này. | Giá trị này được sao chép vào mục mô tả hợp đồng dự án được tạo từ mục mô tả báo giá này khi có được báo giá. |
| Bao gồm Phí | Giá trị **Có**/**Không** cho biết liệu các khoản phí của dự án đã chọn có được đưa vào phần ước tính trên mục mô tả báo giá này hay không. Giá trị **Không** cho biết rằng các khoản phí sẽ không được đưa vào phần ước tính trên mục mô tả báo giá này. Giá trị **Có** cho biết rằng các khoản phí sẽ được đưa vào phần ước tính trên mục mô tả báo giá này. | Giá trị này được sao chép vào mục Mô tả hợp đồng dự án được tạo từ mục mô tả báo giá này khi có được báo giá. |
| Số tiền Đã báo giá | Đây là số tiền sẽ được báo giá cho khách hàng đối với tất cả các công việc được dự báo trên mục mô tả báo giá dựa trên dự án này. Trên một báo giá tạo từ một cơ hội, giá trị này được sao chép từ trường **Ngân sách khách hàng** trên mô tả cơ hội. Khi mô tả báo giá dựa trên dự án có chi tiết mô tả, trường này bị khóa tính năng chỉnh sửa và được tóm tắt từ số tiền trên chi tiết mô tả báo giá. | Giá trị này được sao chép vào mục mô tả hợp đồng dự án được tạo từ mục mô tả báo giá này khi có được báo giá. |
| Thuế Ước tính | Đây là trường có thể chỉnh sửa để người dùng thêm số tiền thuế ước tính trên mô tả báo giá. Khi mô tả báo giá dựa trên dự án có chi tiết mô tả, trường này bị khóa tính năng chỉnh sửa và được tóm tắt từ số tiền thuế trên chi tiết mô tả báo giá. | Giá trị này được sao chép vào mục mô tả hợp đồng dự án được tạo từ mục mô tả báo giá này khi có được báo giá. |
| Số tiền đã báo giá sau thuế | Trường này là số tiền mô tả báo giá sau thuế và ở dạng chỉ đọc. Số tiền trong trường này được tính là *Số tiền báo giá + Thuế*. | Giá trị này được sao chép vào mục mô tả hợp đồng dự án được tạo từ mục mô tả báo giá này khi có được báo giá. |
| Giới hạn không vượt quá | Trường này có thể chỉnh sửa và chỉ có sẵn trên các mô tả báo giá dựa trên dự án có phương thức thanh toán **Thời gian và vật tư**. | Giá trị này được sao chép vào mục mô tả hợp đồng dự án được tạo từ mục mô tả báo giá này khi có được báo giá. |
| Ngân sách Khách hàng | Trường này có thể chỉnh sửa và được sao chép từ trường tương ứng trên mô tả cơ hội nếu báo giá được tạo từ một cơ hội. | Giá trị này được sao chép vào mục mô tả hợp đồng dự án được tạo từ mục mô tả báo giá này khi có được báo giá. |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Quy tắc xác thực cho các trường trên tab Tổng quát của các mô tả báo giá dựa trên dự án

**Quy tắc 1**: Nếu trường **Các tác vụ được đưa vào** bị trống hoặc nếu nó được đặt thành **Tất cả các tác vụ dự án**, một dự án sẽ được bao gồm trong mô tả báo giá.

**Quy tắc 2**: Nếu trường **Các tác vụ được đưa vào** bị trống hoặc nếu nó được đặt thành **Tất cả các tác vụ dự án**, một dự án và một lớp giao dịch nhất định chỉ có thể được đưa vào một mô tả báo giá dựa trên dự án của báo giá.

**Quy tắc 3**: Nếu trường **Các tác vụ được đưa vào** được đặt thành **Chỉ các tác vụ dự án đã chọn**, một dự án và một lớp giao dịch nhất định có thể được đưa vào nhiều mô tả báo giá dựa trên dự án của báo giá.

**Quy tắc 4**: Nếu một cơ hội có nhiều báo giá, có thể có các mô tả báo giá từ các báo giá khác nhau mà đều tham chiếu đến cùng một dự án và bao gồm cùng một lớp giao dịch.

**Quy tắc 5** : Nếu các báo giá không thuộc cùng một cơ hội, chúng không thể bao gồm cùng một dự án và lớp giao dịch.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p>
                    <strong>Cơ hội</strong>
                </p>
            </td>
            <td width="39" valign="top">
                <p>
                    <strong>Báo giá</strong>
                </p>
            </td>
            <td width="40" valign="top">
                <p>
                    <strong>Mô tả báo giá</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Dự án</strong>
                </p>
            </td>
            <td width="77" valign="top">
                <p>
                    <strong>Các tác vụ được đưa vào</strong>
                </p>
            </td>
            <td width="45" valign="top">
                <p>
                    <strong>Bao gồm Thời gian</strong>
                </p>
            </td>
            <td width="46" valign="top">
                <p>
                    <strong>Bao gồm Chi phí</strong>
                </p>
            </td>
            <td width="43" valign="top">
                <p>
                    <strong>Bao gồm vật liệu</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Bao gồm</strong>
                </p>
                <p>
                    <strong>Phí</strong>
                </p>
            </td>
            <td width="49" valign="top">
                <p>
                    <strong>Hợp lệ/Không hợp lệ</strong>
                </p>
            </td>
            <td width="200" valign="top">
                <p>
                    <strong>Lý do</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Kỳ 1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Trống </p>
            </td>
            <td width="45" valign="top">
                <p>
Có </p>
            </td>
            <td width="46" valign="top">
                <p>
Có </p>
            </td>
            <td width="43" valign="top">
                <p>
Có </p>
            </td>
            <td width="41" valign="top">
                <p>
Có </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Không hợp lệ </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Vi phạm Quy tắc số 2. Thời gian, Chi phí và Phí cho dự án P1 được đưa vào các mục mô tả báo giá QL1 và QL2 </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
Kỳ 1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Trống </p>
            </td>
            <td width="45" valign="top">
                <p>
Có </p>
            </td>
            <td width="46" valign="top">
                <p>
Có </p>
            </td>
            <td width="43" valign="top">
                <p>
Có </p>
            </td>
            <td width="41" valign="top">
                <p>
Có </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Kỳ 1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Trống </p>
            </td>
            <td width="45" valign="top">
                <p>
Có </p>
            </td>
            <td width="46" valign="top">
                <p>
No </p>
            </td>
            <td width="43" valign="top">
                <p>
Có </p>
            </td>
            <td width="41" valign="top">
                <p>
Có </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Không hợp lệ </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Vi phạm Quy tắc số 2. Thời gian, Vật tư và Phí cho dự án P1 được đưa vào các mục mô tả báo giá QL1 và QL2 </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
Kỳ 1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Trống </p>
            </td>
            <td width="45" valign="top">
                <p>
Có </p>
            </td>
            <td width="46" valign="top">
                <p>
Có </p>
            </td>
            <td width="43" valign="top">
                <p>
Có </p>
            </td>
            <td width="41" valign="top">
                <p>
Có </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Kỳ 1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Trống </p>
            </td>
            <td width="45" valign="top">
                <p>
Có </p>
            </td>
            <td width="46" valign="top">
                <p>
No </p>
            </td>
            <td width="43" valign="top">
                <p>
Có </p>
            </td>
            <td width="41" valign="top">
                <p>
Có </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Hợp lệ </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Thời gian, Vật tư và Phí cho dự án P1 được đưa vào QL1 <br>
Chi phí trên dự án P1 được đưa vào QL2 <br>
Những nội dung được đưa vào mỗi mục mô tả báo giá là hợp lệ do không bị trùng lặp.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
Kỳ 1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Trống </p>
            </td>
            <td width="45" valign="top">
                <p>
No </p>
            </td>
            <td width="46" valign="top">
                <p>
Có </p>
            </td>
            <td width="43" valign="top">
                <p>
No </p>
            </td>
            <td width="41" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Kỳ 1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Chỉ các tác vụ được chọn </p>
            </td>
            <td width="45" valign="top">
                <p>
Có </p>
            </td>
            <td width="46" valign="top">
                <p>
Có </p>
            </td>
            <td width="43" valign="top">
                <p>
Có </p>
            </td>
            <td width="41" valign="top">
                <p>
Có </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Không hợp lệ </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Vi phạm quy tắc số 2 </p>
                <p>
Q1 bao gồm Thời gian, Vật tư, Chi phí và Phí cho một tập hợp con các nhiệm vụ trong dự án P1 </p>
                <p>
QL2 bao gồm Thời gian, Chi phí và Phí của toàn bộ dự án P1, do đó trùng lặp với những số liệu được đưa vào Q1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
Kỳ 1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Trống </p>
            </td>
            <td width="45" valign="top">
                <p>
Có </p>
            </td>
            <td width="46" valign="top">
                <p>
Có </p>
            </td>
            <td width="43" valign="top">
                <p>
Có </p>
            </td>
            <td width="41" valign="top">
                <p>
Có </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Kỳ 1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Chỉ các tác vụ được chọn </p>
            </td>
            <td width="45" valign="top">
                <p>
Có </p>
            </td>
            <td width="46" valign="top">
                <p>
Có </p>
            </td>
            <td width="43" valign="top">
                <p>
Có </p>
            </td>
            <td width="41" valign="top">
                <p>
Có </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Hợp lệ </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Theo quy tắc số 3, </p>
                <p>
Q1 bao gồm Thời gian, Vật tư, Chi phí và Phí cho một tập hợp con các nhiệm vụ trong dự án P1.
                </p>
                <p>
QL2 bao gồm Thời gian, Vật tư, Chi phí và Phí cho một tập hợp con các nhiệm vụ trong dự án P1.
                </p>
                <p>
Bước xác thực bổ sung duy nhất xoay quanh việc tập hợp con các nhiệm vụ trên QL1 khác với tập hợp con các nhiệm vụ trên QL2 để đảm bảo rằng không có sự trùng lặp. Điều này được hệ thống thực hiện khi các nhiệm vụ được liên kết.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
Kỳ 1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Chỉ các tác vụ được chọn </p>
            </td>
            <td width="45" valign="top">
                <p>
Có </p>
            </td>
            <td width="46" valign="top">
                <p>
Có </p>
            </td>
            <td width="43" valign="top">
                <p>
Có </p>
            </td>
            <td width="41" valign="top">
                <p>
Có </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Kỳ 1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tất cả các tác vụ dự án hoặc để trống </p>
            </td>
            <td width="45" valign="top">
                <p>
Có </p>
            </td>
            <td width="46" valign="top">
                <p>
Có </p>
            </td>
            <td width="43" valign="top">
                <p>
Có </p>
            </td>
            <td width="41" valign="top">
                <p>
Có </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Hợp lệ </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Theo Quy tắc số 5, Q1 và Q2 là hai báo giá về cùng một cơ hội, vì vậy cả hai đều có thể ước tính cho các thành phần giống nhau của một dự án.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q2 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Kỳ 1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tất cả các tác vụ dự án hoặc để trống </p>
            </td>
            <td width="45" valign="top">
                <p>
Có </p>
            </td>
            <td width="46" valign="top">
                <p>
Có </p>
            </td>
            <td width="43" valign="top">
                <p>
Có </p>
            </td>
            <td width="41" valign="top">
                <p>
Có </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Kỳ 1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tất cả các tác vụ dự án hoặc để trống </p>
            </td>
            <td width="45" valign="top">
                <p>
Có </p>
            </td>
            <td width="46" valign="top">
                <p>
Có </p>
            </td>
            <td width="43" valign="top">
                <p>
Có </p>
            </td>
            <td width="41" valign="top">
                <p>
Có </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Không hợp lệ </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Theo Quy tắc số 4, Q1 và Q2 là hai báo giá về các cơ hội khác nhau, vì vậy cả hai đều không thể ước tính cho các thành phần giống nhau của cùng một dự án.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O2 </p>
            </td>
            <td width="39" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Kỳ 1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tất cả các tác vụ dự án hoặc để trống </p>
            </td>
            <td width="45" valign="top">
                <p>
Có </p>
            </td>
            <td width="46" valign="top">
                <p>
Có </p>
            </td>
            <td width="43" valign="top">
                <p>
Có </p>
            </td>
            <td width="41" valign="top">
                <p>
Có </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
