---
title: Đóng báo giá
description: Chủ đề này cung cấp thông tin về cách đóng báo giá trong Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 47804db0144c2b0f9dee2c60518e8aba6fb27473
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124709"
---
# <a name="close-a-quote"></a>Đóng báo giá

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Báo giá dự án ở trạng thái Đã giành được hoặc Đã mất. Các chức năng Kích hoạt và Sửa đổi không được hỗ trợ trên báo giá trong Microsoft Dynamics 365 Project Operations. Do đó, bạn có thể đóng báo giá nháp.

## <a name="close-a-quote-as-won"></a>Đóng báo giá dưới dạng Đã giành được

Việc đóng báo giá dự án dưới dạng Đã giành được sẽ đặt trạng thái báo giá thành **Đã đóng** và lý do dẫn đến trạng thái được đặt thành **Đã giành được**. Việc đóng báo giá làm cho báo giá ở chế độ chỉ đọc và tạo ra bản nháp hợp đồng dự án có chứa tất cả thông tin báo giá. Vì không thể mở lại báo giá đã đóng nên trước khi bạn đóng báo giá, hộp thoại xác nhận sẽ xác nhận các thay đổi của bạn.

Hợp đồng dự án được tạo từ báo giá dự án cũng có sẵn trong mô-đun kế toán và quản lý dự án của Project Operations. Nếu hợp đồng dự án không được ánh xạ tới một dự án trên mọi mô tả hợp đồng, thì hợp đồng dự án này sẽ được cung cấp dưới dạng hợp đồng dự án không hoạt động và có hiệu lực ngay khi dự án được ánh xạ tới ít nhất một trong các mô tả hợp đồng của dự án đó.

Nếu báo giá được đính kèm với một cơ hội, bất kỳ báo giá dự án nào khác về cơ hội sẽ tự động bị đóng dưới dạng Đã mất.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Tác động tài chính của việc đóng báo giá là Đã giành được

Nếu có bất kỳ giá trị thời gian thực tế nào đã ghi lại trên một dự án mà vẫn còn được đính kèm với báo giá nháp, thì chỉ chi phí của thời gian hoặc chi phí được ghi lại. Sau khi một báo giá được đóng dưới dạng Đã giành được, ứng dụng sẽ cấu trúc lại chi phí bằng cách đảo ngược các giá trị chi phí thực tế cũ hơn và tạo lại giá trị chi phí thực tế mới. Ứng dụng sẽ xử lý các giá trị chi phí thực tế này dựa trên Phương thức thanh toán của mô tả hợp đồng dự án liên quan. Nếu các giá trị thực tế chi phí tham chiếu đến mô tả hợp đồng về vật tư và thời gian, hệ thống sẽ tự động tạo các gái trị bán hàng thực tế chưa lập hóa đơn tương ứng cho thời điểm đóng báo giá và thời điểm tạo hợp đồng. Nếu các giá trị chi phí thực tế tham chiếu đến mô tả hợp đồng theo giá cố định, ứng dụng sẽ ngừng xử lý lại các giá trị chi phí thực tế dựa trên các quy tắc thanh toán chia nhỏ cho khách hàng hợp đồng dự án.

Tất cả các giá trị thực tế đã được xử lý lại đều có trong mô-đun kế toán và quản lý dự án để xem xét, cập nhật và đăng lên sổ cái. 

## <a name="close-a-quote-as-lost"></a>Đóng báo giá dưới dạng Đã mất

Việc đóng báo giá dự án dưới dạng **Đã mất** sẽ đặt trạng thái thành Đã đóng và lý do dẫn đến trạng thái thành **Đã mất**. Việc đóng báo giá làm cho báo giá ở chế độ chỉ đọc. Vì không thể mở lại báo giá đã đóng, vì vậy trước khi bạn đóng báo giá, hộp thoại xác nhận sẽ xác nhận các thay đổi của bạn.

Nếu báo giá dự án được đóng dưới dạng Đã mất có một dự án được tham chiếu trên bất kỳ mô tả nào của dự án, thì dự án đó cũng được đánh dấu là Đã đóng và mọi mục đặt trước nguồn lực từ ngày đó trở đi sẽ bị hủy.

> [!NOTE]
> Trong Project Operations, việc đóng báo giá dưới dạng Đã giành được hay Đã mất sẽ không ảnh hưởng đến trạng thái đó của Cơ hội. Cơ hội sẽ vẫn mở cho đến khi được đóng theo cách thủ công.
