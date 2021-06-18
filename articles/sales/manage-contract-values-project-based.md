---
title: Làm việc với phần mô tả hợp đồng dựa trên dự án
description: Chủ đề này cung cấp thông tin về phần mô tả hợp đồng dựa trên dự án.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2072692296308a08756ec3e0f381c792745dd3e2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011532"
---
# <a name="work-with-projectbased-contract-lines"></a>Làm việc với phần mô tả hợp đồng dựa trên dự án

Mô tả hợp đồng theo dự án trong Dynamics 365 Project Operations được thiết kế để ghi lại ước tính và thỏa thuận thanh toán cho các thành phần cụ thể của dự án theo cam kết. Cấu trúc của phần mô tả hợp đồng dựa trên dự án được mở rộng cho các ước tính và kịch bản thanh toán của dự án với các khái niệm sau:

- Phương thức thanh toán
- Ánh xạ dự án và nhiệm vụ
- Các lớp giao dịch được bao gồm
- Giới hạn không vượt quá
- Thiết lập khả năng tính phí
- Các ước tính dựa trên chi tiết mô tả hợp đồng
- Khách hàng trong phần mô tả hợp đồng

Tab **Chung** của phần mô tả hợp đồng dựa trên dự án bao gồm các trường sau. Các trường này giúp thiết lập cơ sở cho số liệu ước tính chi tiết, cơ bản và sắp xếp thanh toán cho công việc theo dự án.

| Trường | Nội dung mô tả | Tác động xuôi tuyến |
| --- | --- | --- |
| **Tên** | Tên của phần mô tả hợp đồng xác định thành phần riêng biệt của hợp đồng đang được ước tính. Đối với hợp đồng dự án tạo từ báo giá, giá trị này sẽ được sao chép từ giá trị tương ứng của phần mô tả báo giá dựa trên dự án. | Giá trị của trường này được sao chép sang phần mô tả hóa đơn dự án được tạo dựa trên phần mô tả hợp đồng này khi tạo hóa đơn. |
| **Phương thức Thanh toán** | Đối với hợp đồng dự án tạo từ báo giá, giá trị này sẽ được sao chép từ trường tương ứng trên phần mô tả báo giá. Dưới đây là bộ tùy chọn đại diện cho 2 mô hình hợp đồng chính được Project Operations hỗ trợ:</br>- **Giá cố định**</br>- **Thời gian và Vật tư** | Dựa trên phương thức thanh toán được tham chiếu trong phần mô tả hợp đồng, giao dịch thực tế sẽ được xử lý. Nếu phần mô tả hợp đồng tham chiếu theo giao dịch thực tế có phương thức thanh toán theo thời gian và vật tư, thì hồ sơ chi phí và doanh số bán hàng thực tế chưa thanh toán sẽ được tạo. Nếu phần mô tả hợp đồng tham chiếu theo giao dịch thực tế có phương thức thanh toán theo giá cố định, thì chỉ một hồ sơ chi phí thực tế được tạo. |
| **Dự án** | Sử dụng trường này để xác định dự án sẽ dùng để thực hiện công việc theo cam kết này. | Giá trị trong trường này sẽ được sử dụng cùng với trường **Các nhiệm vụ được đưa vào** và trường **Các lớp giao dịch được bao gồm** để xử lý việc tham chiếu phần mô tả hợp đồng cho hồ sơ mô tả số liệu ước tính hoặc thực tế. |
| **Bao gồm Thời gian** | Một cờ cho biết liệu các giao dịch theo thời gian hoặc chi phí lao động của dự án đã chọn có được đưa vào phần mô tả hợp đồng này hay không. Giá trị **Không** chỉ ra rằng các giao dịch theo thời gian hoặc chi phí lao động sẽ không được đưa vào phần mô tả hợp đồng này. Giá trị **Có** chỉ ra điều ngược lại. | Giá trị của trường này được sử dụng cùng với dự án để xử lý việc tham chiếu phần mô tả hợp đồng cho hồ sơ mô tả số liệu ước tính hoặc thực tế. |
| **Bao gồm Chi phí** | Một cờ cho biết liệu các chi phí của dự án đã chọn có được đưa vào phần mô tả hợp đồng này hay không. Giá trị **Không** chỉ ra rằng các chi phí sẽ không được đưa vào phần mô tả hợp đồng này. Giá trị **Có** chỉ ra điều ngược lại. | Giá trị của trường này được sử dụng cùng với dự án để xử lý việc tham chiếu phần mô tả hợp đồng cho hồ sơ mô tả số liệu ước tính hoặc thực tế. |
| **Bao gồm Phí** | Một cờ cho biết liệu các khoản phí của dự án đã chọn có được đưa vào phần mô tả hợp đồng này hay không. Giá trị **Không** chỉ ra rằng các khoản phí sẽ không được đưa vào phần mô tả hợp đồng này. Giá trị **Có** chỉ ra điều ngược lại. | Giá trị của trường này được sử dụng cùng với dự án để xử lý việc tham chiếu phần mô tả hợp đồng cho hồ sơ mô tả số liệu ước tính hoặc thực tế. |
| **Số tiền Theo hợp đồng** | Đối với phần mô tả hợp đồng có giá cố định, đây là giá trị đã thỏa thuận mà khách hàng sẽ được lập hóa đơn cho tất cả các thành phần công việc liên quan đến phần mô tả hợp đồng này. Đối với phần mô tả hợp đồng vật tư và thời gian, số tiền này là giá trị ước tính của số tiền mà khách hàng sẽ được lập hóa đơn cho tất cả các thành phần công việc liên quan đến phần mô tả hợp đồng này. Đối với hợp đồng dự án tạo từ báo giá, giá trị này sẽ được sao chép từ trường tương ứng trên phần mô tả báo giá. Khi phần mô tả hợp đồng dựa trên dự án có các chi tiết mô tả, bạn sẽ không chỉnh sửa được trường này. Ngoài ra, trường này có nội dung được tóm tắt dựa trên số tiền có trong các chi tiết mô tả hợp đồng. | Khi phần mô tả hợp đồng có các chi tiết mô tả, giá trị này có thể được sửa đổi bằng cách thay đổi số tiền có trong các chi tiết mô tả. Đối với phần mô tả hợp đồng có giá cố định, giá trị này dùng để đưa ra số tiền trước thuế cho các mốc thanh toán định kỳ. |
| **Thuế Ước tính** | Người dùng có thể chỉnh sửa trường này để nhập số tiền thuế ước tính trên phần mô tả hợp đồng. Khi phần mô tả hợp đồng dựa trên dự án có các chi tiết mô tả, bạn sẽ không chỉnh sửa được trường này. Ngoài ra, trường này có nội dung được tóm tắt dựa trên số tiền thuế có trong các chi tiết mô tả hợp đồng. | Khi phần mô tả hợp đồng có các chi tiết mô tả, giá trị này có thể được sửa đổi bằng cách thay đổi số tiền thuế có trong các chi tiết mô tả. Đối với phần mô tả hợp đồng có giá cố định, giá trị này dùng để đưa ra khoản thuế cho các mốc thanh toán định kỳ. |
| **Số tiền sau thuế theo hợp đồng** | Số tiền sau thuế theo phần mô tả hợp đồng. Trường này là trường chỉ đọc và được tính bằng **Số tiền theo hợp đồng + Thuế**. | Đối với phần mô tả hợp đồng có giá cố định, giá trị này dùng để đưa ra các mốc thanh toán định kỳ. |
| **Giới hạn không vượt quá** | Người dùng có thể chỉnh sửa trường này và đây là trường chỉ có trong phần mô tả hợp đồng dựa trên dự án có phương thức thanh toán theo thời gian và vật tư. | Người dùng có thể chỉnh sửa trường này. Khi số liệu thực tế về thời gian và chi phí tham chiếu đến phần mô tả hợp đồng theo thời gian và vật tư này, số tiền thực tế được đánh giá theo giới hạn không vượt quá trên phần mô tả hợp đồng sau khi tính đến số tiền đã chi và số tiền cam kết. |
| **Ngân sách Khách hàng** | Đây là trường có thể chỉnh sửa và được sao chép từ trường tương ứng trên phần mô tả báo giá, nếu hợp đồng được tạo từ một báo giá. | Trường này chỉ dùng để cung cấp thông tin và không có bất kỳ ý nghĩa nào theo đó. |

## <a name="validation-rule-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>Quy tắc xác thực cho các tùy chọn trên tab Chung của phần mô tả hợp đồng dựa trên dự án

Quy tắc: Một dự án và một lớp giao dịch nhất định chỉ có thể được đưa vào một phần mô tả hợp đồng dựa trên dự án của một hợp đồng.

| Hợp đồng | Mô tả hợp đồng | Dự án | Bao gồm thời gian | Bao gồm chi phí | Bao gồm phí | Hợp lệ/Không hợp lệ | Lý do                                                                                                                                                                                                  |
|----------|---------------|---------|--------------|-----------------|-------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| C1       | CL1           | Kỳ 1      | Có          | Có             | Có         | Không hợp lệ       | Vi phạm quy tắc. Thời gian, chi phí và các khoản phí của dự án P1 được đưa vào cả hai phần mô tả hợp đồng, CL1 và CL2.                                                                                       |
| C1       | CL2           | Kỳ 1      | Có          | Có             | Có         | Không hợp lệ       | Vi phạm quy tắc. Thời gian, chi phí và các khoản phí của dự án P1 được đưa vào cả hai phần mô tả hợp đồng, CL1 và CL2.                                                                                       |
| C1       | CL1           | Kỳ 1      | Có          | No              | Có         | Không hợp lệ       | Vi phạm quy tắc. Thời gian và các khoản phí của dự án P1 được đưa vào cả hai phần mô tả hợp đồng, CL1 và CL2.                                                                                                   |
| C1       | CL2           | Kỳ 1      | Có          | Có             | Có         | Không hợp lệ       | Vi phạm quy tắc. Thời gian và các khoản phí của dự án P1 được đưa vào cả hai phần mô tả hợp đồng, CL1 và CL2.                                                                                                   |
| C1       | CL1           | Kỳ 1      | Có          | No              | Có         | Hợp lệ           | Thời gian và các khoản phí của dự án P1 được đưa vào CL1. Chi phí của dự án P1 được đưa vào CL2. </br>   Những số liệu đưa vào từng mô tả hợp đồng không bị chồng chéo, do đó hợp lệ.  |
| C1       | CL2           | Kỳ 1      | No           | Có             | No          | Hợp lệ           | Thời gian và các khoản phí của dự án P1 được đưa vào CL1. Chi phí của dự án P1 được đưa vào CL2. </br>   Những số liệu đưa vào từng mô tả hợp đồng không bị chồng chéo, do đó hợp lệ.  |
| C1       | CL1           | Kỳ 1      | Có          | Có             | Có         | Không hợp lệ       | Vi phạm quy tắc. Thời gian, chi phí và các khoản phí của dự án P1 được đưa vào phần mô tả của 2 hợp đồng.                                                                                               |
| CL2      | CL2           | Kỳ 1      | Có          | Có             | Có         | Không hợp lệ       | Vi phạm quy tắc. Thời gian, chi phí và các khoản phí của dự án P1 được đưa vào phần mô tả của 2 hợp đồng.                                                                                               |


[!INCLUDE[footer-include](../includes/footer-banner.md)]