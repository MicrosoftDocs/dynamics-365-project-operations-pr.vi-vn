---
title: Tổng quan về mô tả hợp đồng dựa trên dự án
description: Bài viết này cung cấp thông tin về cách làm việc với các dòng hợp đồng dựa trên dự án.
author: rumant
ms.date: 10/28/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d32edac6537a4b0f51e9d2f72cb4a7342606d2c5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931448"
---
# <a name="project-based-contract-lines-overview"></a>Tổng quan về mô tả hợp đồng dựa trên dự án

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Mô tả hợp đồng theo dự án trong Dynamics 365 Project Operations được thiết kế để ghi lại ước tính và thỏa thuận thanh toán cho các thành phần cụ thể của dự án theo cam kết. Cấu trúc của phần mô tả hợp đồng dựa trên dự án được mở rộng cho các ước tính và kịch bản thanh toán của dự án với các khái niệm sau:

- Phương thức thanh toán
- Ánh xạ dự án và nhiệm vụ
- Các lớp giao dịch được bao gồm
- Giới hạn không vượt quá
- Thiết lập khả năng tính phí
- Các ước tính dựa trên chi tiết mô tả hợp đồng
- Khách hàng trong phần mô tả hợp đồng

Bảng sau bao gồm các trường trên tab **Chung** của phần mô tả hợp đồng dựa trên dự án giúp thiết lập cơ sở cho số liệu ước tính chi tiết, cơ bản và sắp xếp thanh toán cho công việc theo dự án.

| Trường | Nội dung mô tả | Tác động xuôi tuyến |
| --- | --- | --- |
| **Tên** | Tên phần mô tả hợp đồng. Tên này xác định thành phần riêng biệt của hợp đồng đang được ước tính. Đối với hợp đồng dự án tạo từ báo giá, giá trị này sẽ được sao chép từ giá trị tương ứng của phần mô tả báo giá dựa trên dự án. | Tên được sao chép sang phần mô tả hóa đơn dự án được tạo từ phần mô tả hợp đồng này khi tạo hóa đơn. |
| **Phương thức Thanh toán** | Đối với hợp đồng dự án tạo từ báo giá, giá trị này sẽ được sao chép từ trường tương ứng trên phần mô tả báo giá. Dưới đây là bộ tùy chọn đại diện cho 2 mô hình hợp đồng chính được Project Operations hỗ trợ:</br>- **Giá cố định**</br>- **Thời gian và Vật tư** | Dựa trên phương thức thanh toán được tham chiếu trong phần mô tả hợp đồng, giao dịch thực tế sẽ được xử lý. Nếu phần mô tả hợp đồng tham chiếu theo giao dịch thực tế có phương thức thanh toán theo thời gian và vật tư, thì các hồ sơ chi phí và doanh số bán hàng thực tế chưa thanh toán sẽ được tạo. Nếu phần mô tả hợp đồng tham chiếu theo giao dịch thực tế có phương thức thanh toán theo giá cố định, thì chỉ một hồ sơ chi phí thực tế được tạo. |
| **Dự án** | Sử dụng trường này để xác định dự án sẽ dùng để thực hiện công việc theo cam kết này. | Giá trị này sẽ được sử dụng cùng với **Nhiệm vụ được đưa vào** và **Các loại giao dịch được đưa vào** để giải quyết tham chiếu mô tả hợp đồng trên bản ghi dòng giá trị thực tế hoặc ước tính. |
| **Các tác vụ được đưa vào** | Cho biết liệu phần mô tả hợp đồng này có bao gồm tất cả các nhiệm vụ dự án của dự án đã chọn hay chỉ một tập hợp con các nhiệm vụ. Đây là một bộ tùy chọn có các giá trị có thể có sau đây:</br>- **Tất cả Nhiệm vụ Dự án**</br>- **Chỉ các nhiệm vụ dự án đã chọn**. Giá trị trống trong trường này tương đương với việc chọn **Tất cả nhiệm vụ dự án**. | Nếu **Chỉ các nhiệm vụ đã chọn** được lựa chọn, thì bạn có thể chọn các nhiệm vụ cụ thể và liên kết các nhiệm vụ đó với phần mô tả hợp đồng này trên tab **Thiết lập thanh toán theo nhiệm vụ** của trang **Dự án**. Giá trị nói trên sẽ được sử dụng cùng với các **Dự án** và các lớp **Giao dịch được bao gồm** để xử lý việc tham chiếu phần mô tả hợp đồng cho hồ sơ mô tả số liệu ước tính hoặc thực tế. |
| **Bao gồm Thời gian** | Giá trị **Có**/**Không** cho biết liệu các giao dịch thời gian hoặc chi phí nhân công của dự án đã chọn có được đưa vào mục mô tả hợp đồng này hay không. Giá trị **Không** chỉ ra rằng các giao dịch theo thời gian hoặc chi phí lao động sẽ không được đưa vào phần mô tả hợp đồng này. Giá trị **Có** chỉ ra điều ngược lại. | Giá trị này được dùng cùng với dự án để giải quyết tham chiếu mô tả hợp đồng trên bản ghi dòng giá trị thực tế hoặc ước tính. |
| **Bao gồm Chi phí** | Giá trị **Có**/**Không** cho biết liệu các chi phí của dự án đã chọn có được đưa vào mục mô tả hợp đồng này hay không. Giá trị **Không** chỉ ra rằng các chi phí sẽ không được đưa vào phần mô tả hợp đồng này. Giá trị **Có** chỉ ra điều ngược lại. | Giá trị này được dùng cùng với dự án để giải quyết tham chiếu mô tả hợp đồng trên bản ghi dòng giá trị thực tế hoặc ước tính. |
| **Bao gồm vật tư** | Giá trị **Có**/**Không** cho biết liệu các chi phí vật tư của dự án đã chọn có được đưa vào mục mô tả hợp đồng này hay không. Giá trị **Không** cho biết các chi phí vật tư sẽ không được đưa vào mục mô tả hợp đồng này. Giá trị **Có** chỉ ra điều ngược lại. | Giá trị này được dùng cùng với dự án để giải quyết tham chiếu mô tả hợp đồng trên bản ghi dòng giá trị thực tế hoặc ước tính. |
| **Bao gồm Phí** | Giá trị **Có**/**Không** cho biết liệu các khoản phí của dự án đã chọn có được đưa vào mục mô tả hợp đồng này hay không. Giá trị **Không** chỉ ra rằng các khoản phí sẽ không được đưa vào phần mô tả hợp đồng này. Giá trị **Có** chỉ ra điều ngược lại. | Giá trị này được dùng cùng với dự án để giải quyết tham chiếu mô tả hợp đồng trên bản ghi dòng giá trị thực tế hoặc ước tính. |
| **Số tiền Theo hợp đồng** | Đối với phần mô tả hợp đồng có giá cố định, số tiền này là giá trị đã thỏa thuận mà khách hàng sẽ được lập hóa đơn cho tất cả các thành phần công việc liên quan đến phần mô tả hợp đồng này. Đối với phần mô tả hợp đồng vật tư và thời gian, số tiền này là giá trị ước tính của số tiền mà khách hàng sẽ được lập hóa đơn cho tất cả các thành phần công việc liên quan đến phần mô tả hợp đồng này. Đối với hợp đồng dự án tạo từ báo giá, giá trị này sẽ được sao chép từ trường tương ứng trên phần mô tả báo giá. Khi phần mô tả hợp đồng dựa trên dự án có các chi tiết mô tả, bạn sẽ không chỉnh sửa được trường này. Ngoài ra, trường này có nội dung được tóm tắt dựa trên số tiền có trong các chi tiết mô tả hợp đồng. | Khi phần mô tả hợp đồng có các chi tiết mô tả, giá trị này có thể được sửa đổi bằng cách thay đổi số tiền có trong các chi tiết mô tả. Đối với phần mô tả hợp đồng có giá cố định, giá trị này dùng để đưa ra số tiền trước thuế cho các mốc thanh toán định kỳ. |
| **Thuế Ước tính** | Người dùng có thể chỉnh sửa trường này để nhập số tiền thuế ước tính trên phần mô tả hợp đồng. Khi phần mô tả hợp đồng dựa trên dự án có các chi tiết mô tả, bạn sẽ không chỉnh sửa được trường này. Ngoài ra, trường này có nội dung được tóm tắt dựa trên số tiền thuế có trong các chi tiết mô tả hợp đồng. | Khi phần mô tả hợp đồng có các chi tiết mô tả, giá trị này có thể được sửa đổi bằng cách thay đổi số tiền thuế có trong các chi tiết mô tả. Đối với phần mô tả hợp đồng có giá cố định, giá trị này dùng để đưa ra khoản thuế cho các mốc thanh toán định kỳ. |
| **Số tiền sau thuế theo hợp đồng** | Số tiền sau thuế theo phần mô tả hợp đồng. Trường này là trường chỉ đọc và được tính bằng công thức **Số tiền theo hợp đồng + Thuế**. | Đối với phần mô tả hợp đồng có giá cố định, giá trị này dùng để đưa ra các mốc thanh toán định kỳ. |
| **Giới hạn không vượt quá** | Người dùng có thể chỉnh sửa trường này và đây là trường chỉ có trong phần mô tả hợp đồng dựa trên dự án có phương thức thanh toán được đặt là theo thời gian và vật tư. | Người dùng có thể chỉnh sửa trường này. Khi số liệu thực tế về thời gian và vật tư tham chiếu đến phần mô tả hợp đồng theo thời gian và vật tư này, số tiền thực tế được đánh giá theo giới hạn không vượt quá trên phần mô tả hợp đồng. Việc đánh giá này được hoàn thành sau khi các khoản đã chi và đã cam kết được hạch toán. |
| **Ngân sách Khách hàng** | Đây là trường có thể chỉnh sửa và được sao chép từ trường tương ứng trên phần mô tả báo giá nếu hợp đồng được tạo từ một báo giá. | Trường này chỉ dùng để cung cấp thông tin và không có bất kỳ ý nghĩa nào theo đó. |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>Quy tắc xác thực cho các tùy chọn trên tab Chung của phần mô tả hợp đồng dựa trên dự án

Quy tắc 1: Nếu trường **Các nhiệm vụ được đưa vào** bị để trống hoặc được đặt thành **Tất cả nhiệm vụ dự án**, thì tất cả các nhiệm vụ của dự án được bao gồm trong phần mô tả hợp đồng.

Quy tắc 2: Khi trường **Các nhiệm vụ được đưa vào** bị để trống hoặc được đặt rõ ràng thành **Tất cả nhiệm vụ dự án**, thì một dự án và một lớp giao dịch nhất định chỉ có thể được đưa vào một phần mô tả hợp đồng dựa trên dự án của một hợp đồng.

Quy tắc 3: Khi trường **Các nhiệm vụ được đưa vào** được đặt thành **Chỉ các nhiệm vụ dự án đã chọn**, thì một dự án và một lớp giao dịch nhất định có thể được đưa vào nhiều phần mô tả hợp đồng dựa trên dự án của một hợp đồng.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p>
                    <strong>Hợp đồng</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Mô tả hợp đồng</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Dự án</strong>
                </p>
            </td>
            <td width="67" valign="top">
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
                    <strong>Bao gồm vật tư</strong>
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
            <td width="53" valign="top">
                <p>
                    <strong>Hợp lệ/Không hợp lệ</strong>
                </p>
            </td>
            <td width="250" valign="top">
                <p>
                    <strong>Lý do</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
Kỳ 1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Trống </p>
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
            <td width="42" valign="top">
                <p>
Có </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Không hợp lệ </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Vi phạm Quy tắc số 2. Thời gian, Chi phí, Vật tư và Phí cho dự án P1 được thêm vào cả hai mục Mô tả hợp đồng CL1 và CL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
Kỳ 1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Trống </p>
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
            <td width="42" valign="top">
                <p>
Có </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
Kỳ 1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Trống </p>
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
            <td width="42" valign="top">
                <p>
Có </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Không hợp lệ </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Vi phạm Quy tắc số 2. Thời gian, Vật tư và Phí cho dự án P1 được thêm vào cả hai mục Mô tả hợp đồng CL1 và CL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
Kỳ 1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Trống </p>
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
            <td width="42" valign="top">
                <p>
Có </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
Kỳ 1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Trống </p>
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
            <td width="42" valign="top">
                <p>
Có </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Hợp lệ </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Thời gian, Vật tư và Phí cho dự án P1 được thêm vào CL1.
                </p>
                <ul>
                    <li>
Chi phí trên dự án P1 được bao gồm trên CL2.
                    </li>
                </ul>
                <p>
Những nội dung được thêm vào mỗi mục Mô tả hợp đồng là hợp lệ do không bị trùng lặp.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
Kỳ 1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Trống </p>
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
            <td width="42" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
Kỳ 1 </p>
            </td>
            <td width="67" valign="top">
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
            <td width="42" valign="top">
                <p>
Có </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Không hợp lệ </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Vi phạm quy tắc số 2 </p>
                <p>
C1 bao gồm Thời gian, Vật tư, Chi phí và Phí cho một tập hợp con các nhiệm vụ trong dự án P1.
                </p>
                <p>
CL2 bao gồm Thời gian, Vật tư, Chi phí và Phí cho toàn bộ dự án P1 và do đó trùng lặp với những nội dung được thêm vào C1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
Kỳ 1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Trống </p>
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
            <td width="42" valign="top">
                <p>
Có </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
Kỳ 1 </p>
            </td>
            <td width="67" valign="top">
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
            <td width="42" valign="top">
                <p>
Có </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Hợp lệ </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Theo quy tắc số 3 </p>
                <p>
C1 bao gồm Thời gian, Chi phí, Vật tư, Chi phí và Phí cho một tập hợp con các nhiệm vụ trong dự án P1.
                </p>
                <p>
CL2 bao gồm Thời gian, Chi phí, Vật tư, Chi phí và Phí cho một tập hợp con các nhiệm vụ trong dự án P1.
                </p>
                <p>
Bước xác thực bổ sung duy nhất xoay quanh việc tập hợp con các nhiệm vụ trên CL1 khác với tập hợp con các nhiệm vụ trên CL2 để đảm bảo rằng không có sự trùng lặp ở đó. Điều này được hệ thống thực hiện khi các nhiệm vụ được liên kết.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
Kỳ 1 </p>
            </td>
            <td width="67" valign="top">
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
            <td width="42" valign="top">
                <p>
Có </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
