---
title: Doanh thu thực tế
description: Bài viết này cung cấp thông tin về cách làm việc với giá trị thực tế trong Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: 2551b7d6d20df170c913e302e734583135265529
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924824"
---
# <a name="actuals"></a>Thực tế

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/vật tư không tồn kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Giá trị thực tế đại diện cho tiến độ tài chính và lịch trình đã được xem xét và phê duyệt trên một dự án. Chúng được tạo ra khi mục nhập thời gian, chi phí và sử dụng vật tư, bút toán và hóa đơn được phê duyệt.

> [!IMPORTANT]
> Số liệu thực tế không được chỉnh sửa hoặc xóa khỏi hệ thống. Nếu không, tính toàn vẹn tài chính và bất kỳ sự tích hợp nào với các hệ thống tài chính và kế toán khác có thể chịu ảnh hưởng bất lợi. Microsoft Dynamics 365 Project Operations cho phép bạn sử dụng số liệu thực tế đảo ngược và thay thế để chỉnh sửa các số liệu thực tế tại các điểm khác nhau trong chu kỳ quy trình kinh doanh của các dự án.

## <a name="recording-actuals-based-on-project-events"></a>Ghi lại thực tế dựa trên sự kiện dự án

Project Operations ghi lại các giao dịch tài chính xảy ra trong một chu kỳ thực hiện dự án dưới dạng số liệu thực t ế. Việc tạo các số liệu thực tế tại các sự kiện khác nhau trong chu kỳ sẽ thay đổi, tùy thuộc vào việc thực hiện dự án sử dụng mô hình lập hóa đơn thời gian và vật tư hay mô hình lập hóa đơn giá cố định, và liệu nó ở giai đoạn trước bán hàng hay là dự án nội bộ.

Các bài viết sau giải thích tác động đến bảng Thực tế tại các sự kiện khác nhau cho các biến thể khác nhau:

- [Tác động của số liệu thực tế trong một thỏa thuận dựa trên thời gian và vật liệu](ActualsonTM.md)
- [Tác động của số liệu thực tế trong một thỏa thuận dựa trên giá cố định](ActualonFP.md)
- [Tác động của số liệu thực tế trong giai đoạn trước khi bán hàng của một thỏa thuận](ActualonPreSales.md)
- [Tác động của số liệu thực tế đối với một dự án nội bộ](ActualonInternal.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
