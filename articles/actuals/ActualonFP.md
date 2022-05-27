---
title: Thực tế tác động đến tương tác giá cố định
description: Chủ đề này cung cấp thông tin về tác động trên bảng Thực tế tại các sự kiện khác nhau trong vòng đời của cam kết giá cố định trong Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: 222e7c5eefd7c619e4d7389cdaff2f96176ff275
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579254"
---
# <a name="actuals-impact-in-a-fixed-price-engagement"></a>Thực tế tác động đến tương tác giá cố định

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/vật tư không tồn kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Bảng sau liệt kê các thực tế của các loại giao dịch khác nhau được tạo tại các sự kiện khác nhau trong một cam kết giá cố định.

| Sự kiện | Thực tế chi phí | Doanh số chưa lập hóa đơn thực tế | Doanh số bán hàng được lập hóa đơn thực tế | Ví dụ: |
|---|---|---|---|---|
| Thời gian được tạo ra. | Không áp dụng | Không áp dụng | Không áp dụng | <p>Bob Kozack, từ đơn vị tổ chức Fabrikam Hoa Kỳ có chi phí 100 đô la Mỹ (100 USD) mỗi giờ, đang thực hiện một dự án có tên "Lắp đặt cánh tay tại Adatum." Dự án này được ánh xạ đến một phương pháp thanh toán giá cố định trên dòng hợp đồng. Đây là một mục nhập thời gian mẫu từ Bob Kozak:</p><p>Bob Kozack - 8 giờ</p> |
| Thời gian được nộp. | Không áp dụng | Không áp dụng | Không áp dụng | Một dòng nhật ký chi phí được tạo cho mục nhập thời gian. Tỷ lệ chi phí mặc định được nhập vào mục nhật ký. |
| Mục nhập thời gian được gọi lại trước khi nó được phê duyệt. | Không áp dụng | Không áp dụng | Không áp dụng | |
| Thời gian được chấp thuận. | Một chi phí thực tế được tạo ra. | Không áp dụng | Không áp dụng | <p>Thực tế mới được tạo:</p><ul><li>**Chi phí thực tế:** Bob Kozack, 8 giờ, USD 800</li></ul> |
| Phê duyệt thời gian bị hủy bỏ. | <p>Trạng thái điều chỉnh của giá gốc thực tế được cập nhật thành **Điều chỉnh**.</p><p>Một khoản hoàn nhập chi phí thực tế được tạo có trạng thái điều chỉnh là **Không thể điều chỉnh**.</p> | Không áp dụng | Không áp dụng | <p>Thực tế hiện có được cập nhật:</p><ul><li>**Chi phí thực tế:** Bob Kozack, 8 giờ, USD 800, *Điều chỉnh*</li></ul><p>Thực tế mới được tạo ra để đảo ngược tác động tài chính trước đó:</p><ul><li>**Chi phí thực tế:** Bob Kozack, (8 giờ), (800 USD), *Không thể điều chỉnh*</li></ul> |
| Mục nhập thời gian được gọi lại sau khi nó được phê duyệt. | <p>Trạng thái điều chỉnh của giá gốc thực tế được cập nhật thành **Điều chỉnh**.</p><p>Một khoản hoàn nhập chi phí thực tế được tạo có trạng thái điều chỉnh là **Không thể điều chỉnh**.</p> | Không áp dụng | Không áp dụng | <p>Thực tế hiện có được cập nhật:</p><ul><li>**Chi phí thực tế:** Bob Kozack, 8 giờ, USD 800, *Điều chỉnh*</li></ul><p>Thực tế mới được tạo ra để đảo ngược tác động tài chính trước đó:</p><ul><li>**Chi phí thực tế:** Bob Kozack, (8 giờ), (800 USD), *Không thể điều chỉnh*</li></ul> |
| Hợp đồng được xác nhận. | <p>Trạng thái điều chỉnh của các thực tế chi phí cũ được cập nhật thành **Điều chỉnh**.</p><p>Thực tế chi phí đảo ngược được tạo có trạng thái điều chỉnh là **Không thể điều chỉnh**.</p><p>Thực tế chi phí mới được tạo sau khi các quy tắc hợp đồng được đánh giá lại.</p> | Không áp dụng | Không áp dụng | <p>Thực tế hiện có được cập nhật:</p><ul><li>**Chi phí thực tế:** Bob Kozack, 8 giờ, USD 800, *Điều chỉnh*</li></ul><p>Thực tế mới được tạo ra để đảo ngược tác động tài chính trước đó:</p><ul><li>**Chi phí thực tế:** Bob Kozack, (8 giờ), (800 USD), *Không thể điều chỉnh*</li></ul><p>Thực tế mới được tạo ra để đánh giá lại tác động tài chính:</p><ul><li>**Chi phí thực tế:** Bob Kozack, 8 giờ, USD 800</li></ul> |
| Một hóa đơn được tạo. | Không áp dụng | Không áp dụng | Không áp dụng | |
| Hóa đơn được xác nhận với một mốc quan trọng. | Không áp dụng | Không áp dụng | Các hướng dẫn bán hàng được lập hóa đơn dựa trên cột mốc quan trọng mới được tạo. | <p>Thực tế hiện tại vẫn không thay đổi:</p><ul><li>**Chi phí thực tế:** Bob Kozack, 8 giờ, USD 800</li></ul><p>Thực tế mới được tạo để ghi lại các giá trị bán hàng được lập hóa đơn:</p><ul><li>**Doanh số thực tế được lập hóa đơn:** Milestone, USD 5,000</li></ul> |
| Hóa đơn được sửa lại để ghi có dấu mốc quan trọng. | Không áp dụng | Không áp dụng | Các hướng dẫn bán hàng lập hóa đơn đảo ngược được tạo. | <p>Thực tế hiện tại vẫn không thay đổi:</p><ul><li>**Chi phí thực tế:** Bob Kozack, 8 giờ, 800 USD</li></ul><p>Thực tế hiện có được cập nhật:</p><ul><li>**Doanh số thực tế được lập hóa đơn:** Milestone, USD 5,000, *Điều chỉnh*</li></ul><p>Thực tế mới được tạo để đảo ngược các giá trị bán hàng đã lập hóa đơn trước đó:</p><ul><li>**Doanh số thực tế được lập hóa đơn:** Mốc, (5.000 USD), *Không thể điều chỉnh*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
