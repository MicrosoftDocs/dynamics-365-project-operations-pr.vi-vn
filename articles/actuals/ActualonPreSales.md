---
title: Tác động của số liệu thực tế trong giai đoạn trước khi bán hàng của một thỏa thuận
description: Bài viết này cung cấp thông tin về tác động đối với bảng Thực tế tại các sự kiện khác nhau trong khi một tương tác đang trong giai đoạn trước bán hàng trong Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: d03d6ac2154806189d0d9d0b232bb317f51071ba
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922386"
---
# <a name="actuals-impact-during-the-pre-sales-stage-of-an-engagement"></a>Tác động của số liệu thực tế trong giai đoạn trước khi bán hàng của một thỏa thuận

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/vật tư không tồn kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Bảng sau liệt kê các số liệu thực tế của các loại giao dịch khác nhau được tạo ra tại các sự kiện khác nhau trong giai đoạn trước bán hàng của tương tác dự án.

| Sự kiện | Thực tế chi phí | Ví dụ: |
|---|---|---|
| Thời gian được tạo. | Không áp dụng | <p>Bob Kozack, đến từ đơn vị tổ chức Fabrikam Hoa Kỳ có mức chi phí là 100 đô-la Mỹ (100 USD) mỗi giờ, đang thực hiện một dự án mang tên "Lắp đặt cánh tay tại Adatum". Dự án này được ánh xạ đến phương pháp thanh toán giá cố định trên mô tả hợp đồng. Sau đây là mục nhập thời gian mẫu từ Bob Kozak:</p><p>Bob Kozack - 8 giờ</p> |
| Thời gian được gửi. | Không áp dụng | Dòng nhật ký kế toán chi phí được tạo cho mục nhập thời gian. Tà tỷ lệ chi phí mặc định được nhập trong bút toán. |
| Mục nhập thời gian được thu hồi lại trước khi được phê duyệt. | Không áp dụng | |
| Thời gian được phê duyệt. | Chi phí thực tế được tạo. | <p>Số liệu thực tế mới được tạo:</p><ul><li>**Chi phí thực tế:** Bob Kozack, 8 giờ, 800 USD</li></ul> |
| Phê duyệt thời gian bị hủy. | <p>Trạng thái điều chỉnh của chi phí thực tế ban đầu được cập nhật thành **Đã điều chỉnh**.</p><p>Một chi phí thực tế đảo ngược được tạo ra có trạng thái điều chỉnh là **Không thể điều chỉnh**.</p> | <p>Số liệu thực tế hiện có được cập nhật:</p><ul><li>**Chi phí thực tế:** Bob Kozack, 8 giờ, 800 USD *Đã điều chỉnh*</li></ul><p>Số liệu thực tế mới được tạo ra để đảo ngược tác động tài chính trước đó:</p><ul><li>**Chi phí thực tế:** Bob Kozack, 8 giờ, 800 USD, *Không thể điều chỉnh*</li></ul> |
| Mục nhập thời gian được thu hồi lại sau khi được phê duyệt. | <p>Trạng thái điều chỉnh của chi phí thực tế ban đầu được cập nhật thành **Đã điều chỉnh**.</p><p>Một chi phí thực tế đảo ngược được tạo ra có trạng thái điều chỉnh là **Không thể điều chỉnh**.</p> | <p>Số liệu thực tế hiện có được cập nhật:</p><ul><li>**Chi phí thực tế:** Bob Kozack, 8 giờ, 800 USD *Đã điều chỉnh*</li></ul><p>Số liệu thực tế mới được tạo ra để đảo ngược tác động tài chính trước đó:</p><ul><li>**Chi phí thực tế:** Bob Kozack, 8 giờ, 800 USD, *Không thể điều chỉnh*</li></ul> |
| Báo giá đã giành được và hợp đồng được tạo. | <p>Trạng thái điều chỉnh của chi phí thực tế cũ được cập nhật thành **Đã điều chỉnh**.</p><p>Chi phí thực tế đảo ngược tạo tạo có trạng thái điều chỉnh là **Không thể điều chỉnh**.</p><p>Chi phí thực tế mới được tạo sau khi quy tắc hợp đồng được đánh giá lại.</p> | <p>Số liệu thực tế hiện có được cập nhật:</p><ul><li>**Chi phí thực tế:** Bob Kozack, 8 giờ, 800 USD *Đã điều chỉnh*</li></ul><p>Số liệu thực tế mới được tạo ra để đảo ngược tác động tài chính trước đó:</p><ul><li>**Chi phí thực tế:** Bob Kozack, 8 giờ, 800 USD, *Không thể điều chỉnh*</li></ul><p>Số liệu thực tế mới được tạo cho tác động tài chính được đánh giá lại khi báo giá được giành hợp đồng được tạo:</p><ul><li>**Chi phí thực tế:** Bob Kozack, 8 giờ, 800 USD</li><li>**Doanh số chưa lập hóa đơn thực tế:** Bob Kozack, 8 giờ, 1.600 USD</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
