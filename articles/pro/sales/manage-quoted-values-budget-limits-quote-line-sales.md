---
title: Tổng quan về các mô tả báo giá dựa trên dự án - bản đơn giản
description: Chủ đề này cung cấp thông tin về việc sử dụng các mô tả báo giá dựa trên dự án cho công việc dự án. (Dự án)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: be1663c0d226fa19fe4b9df566e16d215f1fc08e
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181118"
---
# <a name="project-based-quote-lines-overview---lite"></a>Tổng quan về các mô tả báo giá dựa trên dự án - bản đơn giản

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

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
| Tên | Tên của mô tả báo giá sẽ giúp bạn xác định thành phần riêng biệt của báo giá đang được ước tính. | Được sao chép vào mô tả hợp đồng dự án tạo từ mô tả báo giá này khi báo giá được chốt. |
| Phương thức Thanh toán | Trên một báo giá tạo từ một cơ hội, giá trị này được sao chép từ trường tương ứng trên mô tả cơ hội. Trường này bao gồm hai mô hình hợp đồng chính được hỗ trợ bởi Dynamics 365 Project Operations:</br>- Giá cố định</br>- Thời gian và vật tư.| Giá trị trường này được sao chép vào mô tả hợp đồng dự án tạo từ mô tả báo giá này khi báo giá được chốt. |
| Dự án | Sử dụng trường tùy chọn này để xác định dự án sẽ được sử dụng để thực hiện công việc trong cam kết này. Khi một dự án được ánh xạ đến một mô tả báo giá, nó sẽ giúp thiết lập các tác vụ có thể tính phí, đồng thời đưa ước tính dựa trên dự án vào mô tả báo giá dưới dạng chi tiết mô tả báo giá. Khi một dự án không được ánh xạ tới mô tả báo giá dựa trên dự án, ước tính sẽ được tạo theo cách thủ công bằng cách tạo chi tiết từng mô tả báo giá. | Giá trị trường này được sao chép vào mô tả hợp đồng dự án tạo từ mô tả báo giá này khi báo giá được chốt.|
| Các tác vụ được đưa vào | Cho biết mô tả báo giá này được sử dụng cho tất cả hoặc một số tác vụ dự án cho dự án đã chọn. Trường này có các giá trị khả dĩ sau đây:</br>- Tất cả tác vụ dự án</br>- Chỉ các tác vụ dự án đã chọn</br>Giá trị trống trong trường này tương đương với tùy chọn **Tất cả tác vụ dự án**. | Khi **Chỉ các tác vụ dự án được chọn** được chọn, trên trang dự án, tab **Thiết lập thanh toán theo tác vụ** cho phép bạn chọn một số tác vụ cụ thể để liên kết chúng với mô tả báo giá này. Giá trị trường này được sao chép vào mô tả hợp đồng dự án tạo từ mô tả báo giá này khi báo giá được chốt. |
| Bao gồm Thời gian | Cờ **Có**/**Không** cho biết nếu các giao dịch thời gian hoặc chi phí nhân công trên dự án đã chọn sẽ được bao gồm trong ước tính trên mô tả báo giá này. Giá trị **Không** cho biết rằng giao dịch thời gian hoặc chi phí nhân công sẽ không được bao gồm trong ước tính trên mô tả báo giá này. Giá trị **Có** cho biết rằng giao dịch thời gian hoặc chi phí nhân công sẽ được bao gồm trong ước tính trên mô tả báo giá này. | Giá trị trường này được sao chép vào mô tả hợp đồng dự án tạo từ mô tả báo giá này khi báo giá được chốt. |
| Bao gồm Chi phí | Cờ **Có**/**Không** cho biết nếu chi phí phí tổn trên dự án đã chọn sẽ được bao gồm trong ước tính trên mô tả báo giá này. Giá trị **Không** cho biết rằng chi phí phí tổn sẽ không được bao gồm trong ước tính trên mô tả báo giá này. Giá trị **Có** cho biết rằng chi phí phí tổn sẽ được bao gồm trong ước tính trên mô tả báo giá này. | Giá trị trường này được sao chép vào mô tả hợp đồng dự án tạo từ mô tả báo giá này khi báo giá được chốt. |
| Bao gồm Phí | Cờ **Có**/**Không** cho biết nếu các khoản phí trên dự án đã chọn sẽ được bao gồm trong ước tính trên mô tả báo giá này. Giá trị **Không** cho biết rằng các khoản phí sẽ không được bao gồm trong ước tính trên mô tả báo giá này. Giá trị **Có** cho biết rằng các khoản phí sẽ được bao gồm trong ước tính trên mô tả báo giá này. | Giá trị trường này được sao chép vào Mô tả hợp đồng dự án tạo từ mô tả báo giá này khi báo giá được chốt. |
| Số tiền Đã báo giá | Đây là số tiền sẽ được báo giá cho khách hàng đối với tất cả các công việc được dự báo trên mô tả báo giá dựa trên dự án này. Trên một báo giá tạo từ một cơ hội, giá trị này được sao chép từ trường **Ngân sách khách hàng** trên mô tả cơ hội. Khi mô tả báo giá dựa trên dự án có chi tiết mô tả, trường này bị khóa tính năng chỉnh sửa và được tóm tắt từ số tiền trên chi tiết mô tả báo giá. | Giá trị trường này được sao chép vào mô tả hợp đồng dự án tạo từ mô tả báo giá này khi báo giá được chốt. |
| Thuế Ước tính | Đây là trường có thể chỉnh sửa để người dùng thêm số tiền thuế ước tính trên mô tả báo giá. Khi mô tả báo giá dựa trên dự án có chi tiết mô tả, trường này bị khóa tính năng chỉnh sửa và được tóm tắt từ số tiền thuế trên chi tiết mô tả báo giá. | Giá trị trường này được sao chép vào mô tả hợp đồng dự án tạo từ mô tả báo giá này khi báo giá được chốt. |
| Số tiền đã báo giá sau thuế | Trường này là số tiền mô tả báo giá sau thuế và ở dạng chỉ đọc. Số tiền trong trường này được tính là *Số tiền báo giá + Thuế*. | Giá trị trường này được sao chép vào mô tả hợp đồng dự án tạo từ mô tả báo giá này khi báo giá được chốt. |
| Giới hạn không vượt quá | Trường này có thể chỉnh sửa và chỉ có sẵn trên các mô tả báo giá dựa trên dự án có phương thức thanh toán **Thời gian và vật tư**. | Giá trị trường này được sao chép vào mô tả hợp đồng dự án tạo từ mô tả báo giá này khi báo giá được chốt. |
| Ngân sách Khách hàng | Trường này có thể chỉnh sửa và được sao chép từ trường tương ứng trên mô tả cơ hội nếu báo giá được tạo từ một cơ hội. | Giá trị trường này được sao chép vào mô tả hợp đồng dự án tạo từ mô tả báo giá này khi báo giá được chốt. |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Quy tắc xác thực cho các trường trên tab Tổng quát của các mô tả báo giá dựa trên dự án

**Quy tắc 1**: Nếu trường **Các tác vụ được đưa vào** bị trống hoặc nếu nó được đặt thành **Tất cả các tác vụ dự án**, một dự án sẽ được bao gồm trong mô tả báo giá.

**Quy tắc 2**: Nếu trường **Các tác vụ được đưa vào** bị trống hoặc nếu nó được đặt thành **Tất cả các tác vụ dự án**, một dự án và một lớp giao dịch nhất định chỉ có thể được đưa vào một mô tả báo giá dựa trên dự án của báo giá.

**Quy tắc 3**: Nếu trường **Các tác vụ được đưa vào** được đặt thành **Chỉ các tác vụ dự án đã chọn**, một dự án và một lớp giao dịch nhất định có thể được đưa vào nhiều mô tả báo giá dựa trên dự án của báo giá.

**Quy tắc 4**: Nếu một cơ hội có nhiều báo giá, có thể có các mô tả báo giá từ các báo giá khác nhau mà đều tham chiếu đến cùng một dự án và bao gồm cùng một lớp giao dịch.

**Quy tắc 5** : Nếu các báo giá không thuộc cùng một cơ hội, chúng không thể bao gồm cùng một dự án và lớp giao dịch.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p>
                    <strong>Cơ hội</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Báo giá</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Mô tả báo giá</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Dự án</strong>
                </p>
            </td>
            <td width="90" valign="top">
                <p>
                    <strong>Các tác vụ được đưa vào</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Bao gồm Thời gian</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Bao gồm Chi phí</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Bao gồm</strong>
                </p>
                <p>
                    <strong>Phí</strong>
                </p>
            </td>
            <td width="54" valign="top">
                <p>
                    <strong>Hợp lệ/Không hợp lệ</strong>
                </p>
            </td>
            <td width="308" valign="top">
                <p>
                    <strong>Lý do</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
Kỳ 1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Trống </p>
            </td>
            <td width="48" valign="top">
                <p>
Có </p>
            </td>
            <td width="48" valign="top">
                <p>
Có </p>
            </td>
            <td width="42" valign="top">
                <p>
Có </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Không hợp lệ </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Vi phạm Quy tắc số 2. Thời gian, Chi phí và Phí cho dự án P1 được bao gồm trên các mô tả báo giá QL1 và QL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
Kỳ 1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Trống </p>
            </td>
            <td width="48" valign="top">
                <p>
Có </p>
            </td>
            <td width="48" valign="top">
                <p>
Có </p>
            </td>
            <td width="42" valign="top">
                <p>
Có </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
Kỳ 1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Trống </p>
            </td>
            <td width="48" valign="top">
                <p>
Có </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
Có </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Không hợp lệ </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Vi phạm Quy tắc số 2. Thời gian và Phí cho dự án P1 được bao gồm trên các mô tả báo giá QL1 và QL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
Kỳ 1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Trống </p>
            </td>
            <td width="48" valign="top">
                <p>
Có </p>
            </td>
            <td width="48" valign="top">
                <p>
Có </p>
            </td>
            <td width="42" valign="top">
                <p>
Có </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
Kỳ 1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Trống </p>
            </td>
            <td width="48" valign="top">
                <p>
Có </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
Có </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Hợp lệ </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
Thời gian và Phí của dự án P1 được bao gồm trên QL1.
Chi phí trên dự án P1 được bao gồm trên QL2.
Không có sự chồng chéo về những gì được bao gồm trên mỗi mô tả báo giá và hợp lệ.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
Kỳ 1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Trống </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="48" valign="top">
                <p>
Có </p>
            </td>
            <td width="42" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
Kỳ 1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Chỉ các tác vụ được chọn </p>
            </td>
            <td width="48" valign="top">
                <p>
Có </p>
            </td>
            <td width="48" valign="top">
                <p>
Có </p>
            </td>
            <td width="42" valign="top">
                <p>
Có </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Không hợp lệ </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Vi phạm Quy tắc số 2 ở trên </p>
                <p>
Q1 bao gồm Thời gian, Chi phí và Phí cho một tập hợp con các nhiệm vụ trong dự án P1.
                </p>
                <p>
QL2 bao gồm Thời gian, Chi phí và Phí cho toàn bộ dự án P1 và chồng chéo với những gì được bao gồm trong Q1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
Kỳ 1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Trống </p>
            </td>
            <td width="48" valign="top">
                <p>
Có </p>
            </td>
            <td width="48" valign="top">
                <p>
Có </p>
            </td>
            <td width="42" valign="top">
                <p>
Có </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
Kỳ 1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Chỉ các tác vụ được chọn </p>
            </td>
            <td width="48" valign="top">
                <p>
Có </p>
            </td>
            <td width="48" valign="top">
                <p>
Có </p>
            </td>
            <td width="42" valign="top">
                <p>
Có </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Hợp lệ </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Theo Quy tắc số 3 ở trên, </p>
                <p>
Q1 bao gồm Thời gian, Chi phí và Phí cho một tập hợp con các nhiệm vụ trong dự án P1.
                </p>
                <p>
QL2 bao gồm Thời gian, Chi phí và Phí cho một tập hợp con các nhiệm vụ trong dự án P1.
                </p>
                <p>
Xác thực bổ sung duy nhất xoay quan tập hợp con gồm các nhiệm vụ trên QL1, khác với tập hợp con các nhiệm vụ trên QL2. Điều này đảm bảo rằng không có sự chồng chéo. Điều này được hệ thống thực hiện khi các nhiệm vụ được liên kết.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
Kỳ 1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Chỉ các tác vụ được chọn </p>
            </td>
            <td width="48" valign="top">
                <p>
Có </p>
            </td>
            <td width="48" valign="top">
                <p>
Có </p>
            </td>
            <td width="42" valign="top">
                <p>
Có </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
Kỳ 1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Tất cả các tác vụ dự án hoặc để trống </p>
            </td>
            <td width="48" valign="top">
                <p>
Có </p>
            </td>
            <td width="48" valign="top">
                <p>
Có </p>
            </td>
            <td width="42" valign="top">
                <p>
Có </p>
            </td>
            <td width="54" valign="top">
                <p>
Hợp lệ </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Dựa trên Quy tắc số 5, Q1 và Q2 là hai báo giá về cùng một cơ hội, vì vậy cả hai đều có thể ước tính cho các thành phần giống nhau của dự án.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q2 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
Kỳ 1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Tất cả các tác vụ dự án hoặc để trống </p>
            </td>
            <td width="48" valign="top">
                <p>
Có </p>
            </td>
            <td width="48" valign="top">
                <p>
Có </p>
            </td>
            <td width="42" valign="top">
                <p>
Có </p>
            </td>
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
Kỳ 1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Tất cả các tác vụ dự án hoặc để trống </p>
            </td>
            <td width="48" valign="top">
                <p>
Có </p>
            </td>
            <td width="48" valign="top">
                <p>
Có </p>
            </td>
            <td width="42" valign="top">
                <p>
Có </p>
            </td>
            <td width="54" valign="top">
                <p>
Hợp lệ </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Dựa trên Quy tắc số 4, Q1 và Q2 là hai báo giá về các cơ hội khác nhau, vì vậy cả hai không thể ước tính cho các thành phần giống nhau của cùng dự án.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O2 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
Kỳ 1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Tất cả các tác vụ dự án hoặc để trống </p>
            </td>
            <td width="48" valign="top">
                <p>
Có </p>
            </td>
            <td width="48" valign="top">
                <p>
Có </p>
            </td>
            <td width="42" valign="top">
                <p>
Có </p>
            </td>
            <td width="54" valign="top">
                <p>
Không hợp lệ </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]