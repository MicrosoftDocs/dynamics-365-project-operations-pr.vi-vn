---
title: Tác động của số liệu thực tế trong một thỏa thuận dựa trên giá cố định
description: Bài viết này cung cấp thông tin về tác động đối với bảng Thực tế tại các sự kiện khác nhau trong vòng đời của thỏa thuận giá cố định trong Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: 50819d77d56935bfe5438d7d9dae99562bcc0b49
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918154"
---
# <a name="actuals-impact-in-a-fixed-price-engagement"></a>Tác động của số liệu thực tế trong một thỏa thuận dựa trên giá cố định

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/vật tư không tồn kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Bảng sau liệt kê các số liệu thực tế của các loại giao dịch khác nhau được tạo ra tại các sự kiện khác nhau trong thỏa thuận giá cố định.

| Sự kiện | Thực tế chi phí | Doanh số chưa lập hóa đơn thực tế | Doanh số lập hóa đơn thực tế | Ví dụ: |
|---|---|---|---|---|
| Thời gian được tạo. | Không áp dụng | Không áp dụng | Không áp dụng | <p>Bob Kozack, đến từ đơn vị tổ chức Fabrikam Hoa Kỳ có mức chi phí là 100 đô-la Mỹ (100 USD) mỗi giờ, đang thực hiện một dự án mang tên "Lắp đặt cánh tay tại Adatum". Dự án này được ánh xạ đến phương pháp thanh toán giá cố định trên mô tả hợp đồng. Sau đây là mục nhập thời gian mẫu từ Bob Kozak:</p><p>Bob Kozack - 8 giờ</p> |
| Thời gian được gửi. | Không áp dụng | Không áp dụng | Không áp dụng | Dòng nhật ký kế toán chi phí được tạo cho mục nhập thời gian. Tà tỷ lệ chi phí mặc định được nhập trong bút toán. |
| Mục nhập thời gian được thu hồi lại trước khi được phê duyệt. | Không áp dụng | Không áp dụng | Không áp dụng | |
| Thời gian được phê duyệt. | Chi phí thực tế được tạo. | Không áp dụng | Không áp dụng | <p>Số liệu thực tế mới được tạo:</p><ul><li>**Chi phí thực tế:** Bob Kozack, 8 giờ, 800 USD</li></ul> |
| Phê duyệt thời gian bị hủy. | <p>Trạng thái điều chỉnh của chi phí thực tế ban đầu được cập nhật thành **Đã điều chỉnh**.</p><p>Một chi phí thực tế đảo ngược được tạo ra có trạng thái điều chỉnh là **Không thể điều chỉnh**.</p> | Không áp dụng | Không áp dụng | <p>Số liệu thực tế hiện có được cập nhật:</p><ul><li>**Chi phí thực tế:** Bob Kozack, 8 giờ, 800 USD *Đã điều chỉnh*</li></ul><p>Số liệu thực tế mới được tạo ra để đảo ngược tác động tài chính trước đó:</p><ul><li>**Chi phí thực tế:** Bob Kozack, 8 giờ, 800 USD, *Không thể điều chỉnh*</li></ul> |
| Mục nhập thời gian được thu hồi lại sau khi được phê duyệt. | <p>Trạng thái điều chỉnh của chi phí thực tế ban đầu được cập nhật thành **Đã điều chỉnh**.</p><p>Một chi phí thực tế đảo ngược được tạo ra có trạng thái điều chỉnh là **Không thể điều chỉnh**.</p> | Không áp dụng | Không áp dụng | <p>Số liệu thực tế hiện có được cập nhật:</p><ul><li>**Chi phí thực tế:** Bob Kozack, 8 giờ, 800 USD *Đã điều chỉnh*</li></ul><p>Số liệu thực tế mới được tạo ra để đảo ngược tác động tài chính trước đó:</p><ul><li>**Chi phí thực tế:** Bob Kozack, 8 giờ, 800 USD, *Không thể điều chỉnh*</li></ul> |
| Hợp đồng được xác nhận. | <p>Trạng thái điều chỉnh của chi phí thực tế cũ được cập nhật thành **Đã điều chỉnh**.</p><p>Chi phí thực tế đảo ngược tạo tạo có trạng thái điều chỉnh là **Không thể điều chỉnh**.</p><p>Chi phí thực tế mới được tạo sau khi quy tắc hợp đồng được đánh giá lại.</p> | Không áp dụng | Không áp dụng | <p>Số liệu thực tế hiện có được cập nhật:</p><ul><li>**Chi phí thực tế:** Bob Kozack, 8 giờ, 800 USD *Đã điều chỉnh*</li></ul><p>Số liệu thực tế mới được tạo ra để đảo ngược tác động tài chính trước đó:</p><ul><li>**Chi phí thực tế:** Bob Kozack, 8 giờ, 800 USD, *Không thể điều chỉnh*</li></ul><p>Số liệu thực tế mới được tạo cho tác động tài chính được đánh giá lại:</p><ul><li>**Chi phí thực tế:** Bob Kozack, 8 giờ, 800 USD</li></ul> |
| Hóa đơn được tạo. | Không áp dụng | Không áp dụng | Không áp dụng | |
| Hóa đơn được xác nhận với một mốc. | Không áp dụng | Không áp dụng | Doanh số đã lập hóa đơn thực tế dựa trên mốc mới được tạo. | <p>Số liệu thực tế hiện tại vẫn không đổi:</p><ul><li>**Chi phí thực tế:** Bob Kozack, 8 giờ, 800 USD</li></ul><p>Số liệu thực tế mới mới được tạo để ghi lại giá trị doanh số đã lập hóa đơn:</p><ul><li>**Doanh số đã lập hóa đơn thực tế:** Mốc, 5.000 USD</li></ul> |
| Hóa đơn được sửa lại để ghi có cho mốc. | Không áp dụng | Không áp dụng | Doanh số đã lập hóa đơn thực tế đảo ngược được tạo. | <p>Số liệu thực tế hiện tại vẫn không đổi:</p><ul><li>**Chi phí thực tế:** Bob Kozack, 8 giờ, 800 USD</li></ul><p>Số liệu thực tế hiện có được cập nhật:</p><ul><li>**Doanh số đã lập hóa đơn thực tế:** Mốc, 5.000 USD, *Đã điều chỉnh*</li></ul><p>Số liệu thực tế mới mới được tạo để đảo ngược doanh số đã lập hóa đơn trước đó:</p><ul><li>**Doanh số đã lập hóa đơn thực tế:** Mốc, (5.000 USD), *Không thể điều chỉnh*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
