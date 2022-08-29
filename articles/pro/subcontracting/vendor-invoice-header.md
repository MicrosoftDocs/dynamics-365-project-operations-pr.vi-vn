---
title: Chi tiết tiêu đề cho hóa đơn của nhà cung cấp
description: Bài viết này giải thích chức năng được cung cấp trên tiêu đề hóa đơn của nhà cung cấp trong Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d575ebe44e45411e1009c64e9b575777b741322f
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261709"
---
# <a name="header-details-for-vendor-invoices"></a>Chi tiết tiêu đề cho hóa đơn của nhà cung cấp

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Bài viết này giải thích chức năng được cung cấp trên tiêu đề hóa đơn của nhà cung cấp trong Microsoft Dynamics 365 Project Operations.

Khi người quản lý dự án lập kế hoạch và thực hiện dự án, họ có thể thuê các nhà thầu phụ và mua các sản phẩm và dịch vụ từ các nhà cung cấp. Trong quá trình thực hiện dự án, chi phí phát sinh từ các dịch vụ, vật liệu và các hạng mục chi phí được đấu thầu theo hợp đồng phụ với các nhà cung cấp. Các nhà cung cấp lập hóa đơn các chi phí này cho các dự án bằng cách tạo các hóa đơn của nhà cung cấp.

Bảng sau cung cấp thông tin về các trường trên tiêu đề hóa đơn của nhà cung cấp trong Hoạt động dự án.

| Trường | Description | Tác động chức năng |
| --- | --- | --- |
| Tên | Tên của hóa đơn nhà cung cấp. | Trong tất cả danh sách thả xuống hóa đơn của nhà cung cấp, tên của hóa đơn của nhà cung cấp được liệt kê trong cột đầu tiên để giúp bạn xác định hóa đơn của nhà cung cấp. Theo mặc định, khi hóa đơn của nhà cung cấp được tạo từ hợp đồng phụ, **Tên** trường của hóa đơn nhà cung cấp được đặt thành giá trị bao gồm tên của hợp đồng phụ cộng với ngày hiện tại. |
| Description | Mô tả ngắn gọn về các dịch vụ và sản phẩm đang được lập hóa đơn trên hóa đơn của nhà cung cấp. | Không có |
| Nhà cung cấp | Tên của công ty lập hóa đơn cho các sản phẩm và dịch vụ. Công ty này phải là một bản ghi tài khoản có loại mối quan hệ là **Người bán** hoặc **Nhà cung cấp**. | <p>Dựa trên nhà cung cấp được chọn, các giá trị mặc định được tự động nhập vào các trường sau:</p><ul><li>Tiền tệ</li><li>Bảng giá</li><li>Điều khoản thanh toán</li><li>Địa chỉ thanh toán</li></ul> |
| Hợp đồng phụ | Tham chiếu đến hợp đồng phụ cho hóa đơn của nhà cung cấp. | <p>Dựa trên hợp đồng phụ được chọn, các giá trị mặc định được tự động nhập vào các trường sau:</p><ul><li>Tiền tệ</li><li>Bảng giá</li><li>Điều khoản thanh toán</li><li>Địa chỉ thanh toán</li></ul><p>Hợp đồng phụ được chọn trên tiêu đề hóa đơn của nhà cung cấp được nhập theo mặc định trên các dòng hóa đơn của nhà cung cấp và không thể thay đổi ở đó.</p> |
| Ngày lập hóa đơn | Ngày thực hiện chi phí sẽ được tạo khi hóa đơn của nhà cung cấp được xác nhận. | Ngày lập hóa đơn cũng được sử dụng để chọn danh sách giá mua chính xác từ các danh sách giá được đính kèm với nhà cung cấp liên quan hoặc từ các thông số của dự án. |
| Lý do dẫn đến trạng thái | Trạng thái của hóa đơn nhà cung cấp. | <p>Trạng thái xác định vị trí của hóa đơn nhà cung cấp trong quy trình kinh doanh và liệu nó có thể được chỉnh sửa hay không. Dưới đây là một số giá trị có sẵn:</p><ul><li>**Bản thảo** - Hóa đơn của nhà cung cấp có thể được chỉnh sửa.</li><li>**Đã xác nhận** - Hóa đơn của nhà cung cấp đã được xác minh và xác nhận. Không thể chỉnh sửa hoặc xóa hóa đơn của nhà cung cấp ở trạng thái này.</li><li>**Đang tiến hành** - Hóa đơn của nhà cung cấp đang được xem xét. Hóa đơn của nhà cung cấp ở trạng thái này có thể được chỉnh sửa nhưng không thể xóa được.</li><li>**Đã hủy** - Hóa đơn của nhà cung cấp đã bị hủy. Không thể chỉnh sửa hoặc xóa hóa đơn của nhà cung cấp ở trạng thái này.</li></ul> |
| Tiền tệ | Đơn vị tiền tệ mà nhà cung cấp lập hóa đơn cho các sản phẩm và dịch vụ trên hóa đơn của nhà cung cấp. | Trên hóa đơn của nhà cung cấp tham chiếu đến hợp đồng phụ, đơn vị tiền tệ của hợp đồng phụ được nhập theo mặc định làm đơn vị tiền tệ của hóa đơn nhà cung cấp. Trên hóa đơn của nhà cung cấp không tham chiếu đến hợp đồng phụ, giá trị mặc định được nhập từ bản ghi tài khoản của nhà cung cấp và có thể được thay đổi. Sau khi hóa đơn của nhà cung cấp được lưu, bạn không thể chỉnh sửa đơn vị tiền tệ được nữa. |
| Đơn vị hợp đồng | Bộ phận của công ty chịu trách nhiệm nhận các dịch vụ và / hoặc sản phẩm từ nhà cung cấp. | Không có |
| Điều khoản thanh toán | Các điều khoản thanh toán trên hóa đơn của nhà cung cấp được phát hành. Giá trị mặc định được nhập tự động từ bản ghi tài khoản nhà cung cấp. | Các điều khoản thanh toán từ hợp đồng phụ được sao chép vào tất cả các hóa đơn của nhà cung cấp có liên quan đến hợp đồng phụ. Điều khoản thanh toán có thể được cập nhật nếu hóa đơn của nhà cung cấp có trạng thái **Bản thảo**. |
| Địa chỉ thanh toán | Địa chỉ của nhà cung cấp mà các khoản thanh toán phải được gửi đến. Giá trị mặc định được nhập tự động từ bản ghi tài khoản nhà cung cấp. | Địa chỉ thanh toán từ hợp đồng phụ được sao chép làm địa chỉ thanh toán cho tất cả các hóa đơn của nhà cung cấp được tạo cho hợp đồng phụ đó. Địa chỉ thanh toán có thể được cập nhật nếu hóa đơn của nhà cung cấp có trạng thái **Bản thảo**. |
| Tổng con | Nếu hóa đơn của nhà cung cấp không có dòng, hãy nhập tổng phụ của hóa đơn trước thuế. Nếu hóa đơn của nhà cung cấp có các dòng, trường này chỉ được đọc. Trong trường hợp này, số tiền được hiển thị là tổng phụ từ tất cả các dòng trên hóa đơn của nhà cung cấp. | Không có |
| Tổng số thuế | Nếu hóa đơn của nhà cung cấp không có dòng nào, hãy nhập tổng số thuế trên hợp đồng phụ. Nếu hóa đơn của nhà cung cấp có các dòng, trường này chỉ được đọc. Trong trường hợp này, số tiền được hiển thị là tổng số tiền thuế từ tất cả các dòng trên hóa đơn của nhà cung cấp. | Không có |
| Tổng cộng | Trường được tính toán này hiển thị tổng số tiền trên hóa đơn của nhà cung cấp sau khi đã bao gồm thuế. | Không có |

> [!NOTE]
> Không thể thay đổi các trường sau trên hóa đơn của nhà cung cấp sau khi lưu hóa đơn của nhà cung cấp: **Người bán**, **đồng phụ**, **tệ**, **vị ký kết**, và **Điều khoản thanh toán**. Nếu bất kỳ thay đổi nào được yêu cầu đối với các trường này trên hóa đơn của nhà cung cấp, bạn phải xóa hóa đơn của nhà cung cấp và tạo hóa đơn của nhà cung cấp mới.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
