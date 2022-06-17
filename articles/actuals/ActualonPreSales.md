---
title: Thực tế tác động trong giai đoạn trước khi bán hàng của một cam kết
description: Bài viết này cung cấp thông tin về tác động của bảng Thực tế tại các sự kiện khác nhau trong khi tương tác đang ở giai đoạn bán hàng trước trong Microsoft Dynamics 365 Project Operations.
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
# <a name="actuals-impact-during-the-pre-sales-stage-of-an-engagement"></a>Thực tế tác động trong giai đoạn trước khi bán hàng của một cam kết

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/vật tư không tồn kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Bảng sau liệt kê các thực tế của các loại giao dịch khác nhau được tạo tại các sự kiện khác nhau trong giai đoạn trước khi bán hàng của một cam kết dự án.

| Sự kiện | Thực tế chi phí | Ví dụ: |
|---|---|---|
| Thời gian được tạo ra. | Không áp dụng | <p>Bob Kozack, từ đơn vị tổ chức Fabrikam Hoa Kỳ có chi phí 100 đô la Mỹ (100 USD) mỗi giờ, đang thực hiện một dự án có tên "Lắp đặt cánh tay tại Adatum." Dự án này được ánh xạ đến một phương pháp thanh toán giá cố định trên dòng hợp đồng. Đây là một mục nhập thời gian mẫu từ Bob Kozak:</p><p>Bob Kozack - 8 giờ</p> |
| Thời gian được nộp. | Không áp dụng | Một dòng nhật ký chi phí được tạo cho mục nhập thời gian. Tỷ lệ chi phí mặc định được nhập vào mục nhật ký. |
| Mục nhập thời gian được gọi lại trước khi được phê duyệt. | Không áp dụng | |
| Thời gian được chấp thuận. | Một chi phí thực tế được tạo ra. | <p>Thực tế mới được tạo:</p><ul><li>**Chi phí thực tế:** Bob Kozack, 8 giờ, USD 800</li></ul> |
| Phê duyệt thời gian bị hủy bỏ. | <p>Trạng thái điều chỉnh của giá gốc thực tế được cập nhật thành **Điều chỉnh**.</p><p>Chi phí hoàn nhập thực tế được tạo có trạng thái điều chỉnh là **Không thể điều chỉnh**.</p> | <p>Thực tế hiện có được cập nhật:</p><ul><li>**Chi phí thực tế:** Bob Kozack, 8 giờ, USD 800, *Điều chỉnh*</li></ul><p>Thực tế mới được tạo ra để đảo ngược tác động tài chính trước đó:</p><ul><li>**Chi phí thực tế:** Bob Kozack, (8 giờ), (800 USD), *Không thể điều chỉnh*</li></ul> |
| Mục nhập thời gian được gọi lại sau khi nó được phê duyệt. | <p>Trạng thái điều chỉnh của giá gốc thực tế được cập nhật thành **Điều chỉnh**.</p><p>Chi phí hoàn nhập thực tế được tạo có trạng thái điều chỉnh là **Không thể điều chỉnh**.</p> | <p>Thực tế hiện có được cập nhật:</p><ul><li>**Chi phí thực tế:** Bob Kozack, 8 giờ, USD 800, *Điều chỉnh*</li></ul><p>Thực tế mới được tạo ra để đảo ngược tác động tài chính trước đó:</p><ul><li>**Chi phí thực tế:** Bob Kozack, (8 giờ), (800 USD), *Không thể điều chỉnh*</li></ul> |
| Báo giá đã thắng và một hợp đồng được tạo ra. | <p>Trạng thái điều chỉnh của các thực tế chi phí cũ được cập nhật thành **Điều chỉnh**.</p><p>Thực tế chi phí đảo ngược được tạo có trạng thái điều chỉnh là **Không thể điều chỉnh**.</p><p>Thực tế chi phí mới được tạo sau khi các quy tắc hợp đồng được đánh giá lại.</p> | <p>Thực tế hiện có được cập nhật:</p><ul><li>**Chi phí thực tế:** Bob Kozack, 8 giờ, USD 800, *Điều chỉnh*</li></ul><p>Thực tế mới được tạo ra để đảo ngược tác động tài chính trước đó:</p><ul><li>**Chi phí thực tế:** Bob Kozack, (8 giờ), (800 USD), *Không thể điều chỉnh*</li></ul><p>Các hướng dẫn thực tế mới được tạo ra để đánh giá lại tác động tài chính khi báo giá giành được và hợp đồng được tạo:</p><ul><li>**Chi phí thực tế:** Bob Kozack, 8 giờ, USD 800</li><li>**Doanh số bán hàng thực tế chưa lập hóa đơn:** Bob Kozack, 8 giờ, USD 1,600</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
