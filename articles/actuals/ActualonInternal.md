---
title: Tác động thực tế đối với một dự án nội bộ
description: Chủ đề này cung cấp thông tin về tác động trên bảng Thực tế tại các sự kiện khác nhau đối với một dự án nội bộ trong Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: 66a9ac4d2f56ae95313ed6731c3e51926105cff7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579792"
---
# <a name="actuals-impact-for-an-internal-project"></a>Tác động thực tế đối với một dự án nội bộ

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/vật tư không tồn kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Bảng sau liệt kê các thực tế của các loại giao dịch khác nhau được tạo tại các sự kiện khác nhau trong cam kết dự án nội bộ.

| Sự kiện | Thực tế chi phí | Ví dụ: |
|---|---|---|
| Thời gian được tạo ra. | Không áp dụng | <p>Bob Kozack, từ đơn vị tổ chức Fabrikam Hoa Kỳ có chi phí 100 đô la Mỹ (100 USD) mỗi giờ, đang thực hiện một dự án có tên "Lắp đặt cánh tay tại Adatum." Dự án này được ánh xạ đến một phương pháp thanh toán giá cố định trên dòng hợp đồng. Đây là một mục nhập thời gian mẫu từ Bob Kozak:</p><p>Bob Kozack - 8 giờ</p> |
| Thời gian được nộp. | Không áp dụng | Một dòng nhật ký chi phí được tạo cho mục nhập thời gian. Tỷ lệ chi phí mặc định được nhập vào mục nhật ký. |
| Mục nhập thời gian được gọi lại trước khi nó được phê duyệt. | Không áp dụng | |
| Thời gian được chấp thuận. | Một chi phí thực tế được tạo ra. | <p>Thực tế mới được tạo:</p><ul><li>**Chi phí thực tế:** Bob Kozack, 8 giờ, USD 800</li></ul> |
| Việc phê duyệt thời gian bị hủy bỏ. | <p>Trạng thái điều chỉnh của giá gốc thực tế được cập nhật thành **Điều chỉnh**.</p><p>Một khoản hoàn nhập chi phí thực tế được tạo có trạng thái điều chỉnh là **Không thể điều chỉnh**.</p> | <p>Thực tế hiện có được cập nhật:</p><ul><li>**Chi phí thực tế:** Bob Kozack, 8 giờ, USD 800, *Điều chỉnh*</li></ul><p>Thực tế mới được tạo ra để đảo ngược tác động tài chính trước đó:</p><ul><li>**Chi phí thực tế:** Bob Kozack, (8 giờ), (800 USD), *Không thể điều chỉnh*</li></ul> |
| Mục nhập thời gian được gọi lại sau khi nó được phê duyệt. | <p>Trạng thái điều chỉnh của giá gốc thực tế được cập nhật thành **Điều chỉnh**.</p><p>Một khoản hoàn nhập chi phí thực tế được tạo có trạng thái điều chỉnh là **Không thể điều chỉnh**.</p> | <p>Thực tế hiện có được cập nhật:</p><ul><li>**Chi phí thực tế:** Bob Kozack, 8 giờ, USD 800, *Điều chỉnh*</li></ul><p>Thực tế mới được tạo ra để đảo ngược tác động tài chính trước đó:</p><ul><li>**Chi phí thực tế:** Bob Kozack, (8 giờ), (800 USD), *Không thể điều chỉnh*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
