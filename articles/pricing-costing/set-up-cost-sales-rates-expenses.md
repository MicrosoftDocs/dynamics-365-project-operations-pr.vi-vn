---
title: Thiết lập chi phí và tỷ lệ bán hàng cho các chi phí
description: Chủ đề này cung cấp thông tin về cách thiết lập chi phí và tỷ lệ bán hàng cho các danh mục giao dịch và chi phí.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: de7f95f9dcb1dff866d165dba9aaaedb480c1ad5
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598468"
---
# <a name="set-up-cost-and-sales-rates-for-expenses"></a>Thiết lập chi phí và tỷ lệ bán hàng cho các chi phí

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Bạn có thể thiết lập chi phí và giá bán cho các danh mục giao dịch trong Dynamics 365 Project Operations. Bởi vì chi phí và giá bán được thiết kế cho Chi phí, mỗi danh mục giao dịch bao gồm các khoản này, cũng phải được thiết lập như một danh mục chi phí. Thiết lập này đảm bảo tính chính xác trong chức năng xuôi tuyến. Chi phí và giá bán cho các danh mục giao dịch chỉ có thể được liệt kê bằng một đơn vị tiền tệ. Đơn vị tiền tệ này phải là đơn vị tiền tệ trên tiêu đề bảng giá.

Để thiết lập chi phí và tỷ lệ bán hàng cho các danh mục giao dịch, hãy hoàn thành các bước sau. 

1. Đi đến **Bán hàng** > **Khách hàng** > **Bảng giá**.
2. Chọn **Mới** để tạo một bảng giá mới. 
3. Trên **Giá thể loại**, trên menu lưới con, hãy chọn **Giá thể loại mới**. 
4. Trên trang **Tạo nhanh**, hãy nhập danh mục giao dịch và đơn vị mà bạn đang tạo giá mới.

Bảng sau liệt kê các trường trên tab **Tổng quát** và trang **Tạo nhanh** của mô tả giá theo danh mục mà bạn phải lưu ý khi tạo giá theo danh mục trên bảng giá bán hoặc bảng giá vốn.

| Trường | Vị trí | Nội dung mô tả | Tác động xuôi tuyến |
| --- | --- | --- | --- |
| Thể loại giao dịch | Tab **Tổng quát** và trang **Tạo nhanh** | Chọn danh mục giao dịch mà bạn đang tạo giá bán hoặc giá vốn. | Danh mục giao dịch trên giá trị ước tính đến hoặc giá trị thực tế cho Chi phí sẽ được đối chiếu với mô tả này để mặc định chi phí hoặc tỷ lệ bán hàng của danh mục giao dịch. |
| Lịch trình Đơn vị | Tab **Tổng quát** và trang **Tạo nhanh** | Lịch trình đơn vị mặc định từ lịch trình đơn vị của danh mục giao dịch. | Không có tác động xuôi tuyến từ trường này. |
| Đơn vị | Tab **Tổng quát** và trang **Tạo nhanh** | Chọn đơn vị mà giá đang được thiết lập. | Đơn vị trên giá trị dự báo đến hoặc giá trị thực tế được đối chiếu với đơn vị trên mô tả này để mặc định tỷ lệ trên dự toán chi phí hoặc thực tế. |
| Phương pháp định giá | Tab **Tổng quát** và trang **Tạo nhanh** | Các giá trị khả thi của trường **Phương pháp định giá** là **Đơn giả**, **Theo chi phí** và **Tăng cao hơn chi phí**. | Trong khi thiết lập giá, việc chọn **Đơn giá** khóa trường **Phần trăm** trên mô tả giá theo danh mục. Nếu **Theo chi phí** được chọn, các trường **Giá** và **Phần trăm** được khóa trên bảng giá bán hàng. Việc chọn **Tăng cao hơn chi phí** sẽ khóa trường **Giá** trên bảng giá bán hàng. Đối với mô tả giá trị thực tế đến cho chi phí, phương pháp định giá **Theo chi phí** hoặc **Tăng cao hơn chi phí** dẫn đến mô tả bán hàng chưa lập hóa đơn tương ứng được gán một mức giá bằng với giá thực tế hoặc được tính như một khoản chênh lệch so với giá. |
| Giá | Tab **Tổng quát** và trang **Tạo nhanh** | Thiết lập tỷ giá trên mỗi đơn vị cho danh mục giao dịch và kết hợp đơn vị. Ví dụ: chi phí đi lại là 10 USD/dặm và 8 USD/km. | Chi phí đi lại sẽ là tỷ lệ mặc định trên mỗi đơn giá hoặc chi phí của ước tính đến hoặc mô tả thực tế cho một loại giao dịch chi phí.|
| Phần trăm | Tab **Tổng quát** và trang **Tạo nhanh** | Thiết lập tỷ lên phần trăm trên chi phí cho danh mục giao dịch và kết hợp đơn vị. Ví dụ: chi phí vé máy bay nên được đánh dấu lên 10 phần trăm so với chi phí vé máy bay phát sinh. | Tỷ lệ phần trăm chi phí này chỉ áp dụng trên bảng giá bán hàng khi phương thức tính giá đã chọn là **Tăng cao hơn chi phí**. |
| Tiền tệ | Tab **Tổng quát** và trang **Tạo nhanh** | Theo mặc định, giá trị này đến từ đơn vị tiền tệ trên tiêu đề của bảng giá. Đối với định giá danh mục giao dịch, không thể ghi đè đơn vị tiền tệ. | Đơn vị tiền tệ này mặc định dựa trên đơn giá của mô tả thực tế đến cho loại giao dịch chi phí cho chi phí và doanh số. |

## <a name="pricing-methods-for-expenses"></a>Phương thức định giá cho chi phí

Khi bạn thiết lập giá theo danh mục chỉ có liên quan trong bối cảnh định giá chi phí, bạn có thể sử dụng một trong ba phương thức định giá sau:

- **Đơn giá**
- **Tại mức chi phí**
- **Tăng cao hơn chi phí**

### <a name="price-per-unit"></a>Đơn giá
Khi phương thức định giá này được chọn trên mô tả giá theo danh mục được liên kết với bảng giá bán hàng, giá mặc định cho kết hợp danh mục và đơn vị trong cả giá trị ước tính và giá trị thực tế. Ước tính đề cập đến các mô tả ước tính dự án cho các chi phí, chi tiết mô tả báo giá và chi tiết mô tả hợp đồng cho các chi phí.

### <a name="at-cost"></a>Tại mức chi phí
Khi phương thức định giá này được chọn trên mô tả giá theo danh mục được liên kết với bảng giá bán hàng, giá chỉ mặc định cho kết hợp danh mục và đơn vị cho chi phí thực tế. Ví dụ: giá trị bán hàng thực tế chưa lập hóa đơn cho lớp giao dịch chi phí. Đơn giá được đặt trên giá trị bán hàng thực tế chưa lập hóa đơn từ đơn giá trên chi phí thực tế cho khoản chi phí đó. Mặc định giá dựa trên chi phí không được thực hiện trên giá trị ước tính dự án cho các chi phí hoặc mô tả báo giá và chi tiết mô tả hợp đồng cho các chi phí.

### <a name="markup-over-cost"></a>Tăng cao hơn chi phí
Khi phương thức định giá này được chọn trên mô tả giá theo danh mục được liên kết với bảng giá bán hàng, giá chỉ mặc định cho kết hợp danh mục và đơn vị cho chi phí thực tế. Ví dụ: giá trị bán hàng thực tế chưa lập hóa đơn cho lớp giao dịch chi phí. Đơn giá này được đặt trên giá trị bán hàng thực tế chưa lập hóa đơn thành một giá trị được tính toán từ đơn giá trên chi phí thực tế cho khoản chi phí đó sau khi áp dụng tỷ lệ phần trăm tăng. Mặc định giá dựa trên chi phí không được thực hiện trên giá trị ước tính dự án cho các chi phí hoặc mô tả báo giá và chi tiết mô tả hợp đồng cho các chi phí.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
