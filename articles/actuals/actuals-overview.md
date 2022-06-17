---
title: Doanh thu thực tế
description: Bài viết này cung cấp thông tin về cách làm việc với thực tế trong Microsoft Dynamics 365 Project Operations.
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

Giá trị thực tế đại diện cho tiến độ tài chính và lịch trình đã được xem xét và phê duyệt trên một dự án. Chúng được tạo khi các bút toán sử dụng thời gian, chi phí và nguyên vật liệu, các bút toán nhật ký và hóa đơn được chấp thuận.

> [!IMPORTANT]
> Thực tế không được chỉnh sửa hoặc xóa khỏi hệ thống. Nếu không, tính toàn vẹn tài chính và bất kỳ sự tích hợp nào với các hệ thống tài chính và kế toán khác có thể bị ảnh hưởng bất lợi. Microsoft Dynamics 365 Project Operations cho phép bạn sử dụng đảo ngược và thay thế các thực tế để chỉnh sửa các thực tế tại các điểm khác nhau trong vòng đời quy trình kinh doanh của các dự án của bạn.

## <a name="recording-actuals-based-on-project-events"></a>Ghi lại thực tế dựa trên sự kiện dự án

Hoạt động Dự án ghi lại các giao dịch tài chính xảy ra trong vòng đời tham gia dự án dưới dạng thực tế. Việc tạo ra các thực tế tại các sự kiện khác nhau trong vòng đời khác nhau, tùy thuộc vào việc tham gia vào dự án sử dụng mô hình thanh toán thời gian và vật liệu hay mô hình thanh toán giá cố định và liệu nó đang trong giai đoạn bán hàng trước hay là một dự án nội bộ.

Các bài viết sau giải thích tác động đến bảng Thực tế tại các sự kiện khác nhau cho các biến thể khác nhau:

- [Thực tế tác động trong thời gian và tương tác vật liệu](ActualsonTM.md)
- [Thực tế tác động đến tương tác giá cố định](ActualonFP.md)
- [Thực tế tác động trong giai đoạn trước khi bán hàng của một cam kết](ActualonPreSales.md)
- [Tác động thực tế đối với một dự án nội bộ](ActualonInternal.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
