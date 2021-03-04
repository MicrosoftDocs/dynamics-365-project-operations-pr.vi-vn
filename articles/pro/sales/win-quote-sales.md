---
title: Đóng báo giá - bản đơn giản
description: Chủ đề này cung cấp thông tin về cách đóng báo giá trong Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8d387816f51f63ecd95df6534c7c012b323e6ddc
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764890"
---
# <a name="close-a-quote---lite"></a>Đóng báo giá - bản đơn giản

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Báo giá dự án ở trạng thái Đã giành được hoặc Đã mất. Báo giá nháp có thể bị đóng do các thao tác Kích hoạt và Sủa đổi trên báo giá không được hỗ trợ trong Microsoft Dynamics 365 Project Operations.

## <a name="close-a-quote-as-won"></a>Đóng báo giá dưới dạng Đã giành được

Khi đóng báo giá dưới dạng Giành được, trạng thái sẽ được chuyển sang Đã đóng và lý do dẫn đến trạng thái là Giành được. Việc đóng báo giá làm cho báo giá dự án ở chế độ chỉ đọc và tạo ra bản nháp hợp đồng dự án có chứa thông tin báo giá. Do không thể mở báo giá đã đóng, một hộp thoại sẽ hiện lên để xác nhận các thay đổi của bạn.

Nếu báo giá được đính kèm với một cơ hội, bất kỳ báo giá dự án nào khác về cơ hội sẽ tự động bị đóng dưới dạng Đã mất.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Tác động tài chính của việc đóng báo giá là Đã giành được

Nếu có giá trị thực nào của thời gian trên một dự án trong khi vẫn đính kèm vào báo giá nháp, thì hệ thống sẽ chỉ ghi lại chi phí thời gian hoặc khoản chi tiêu. Sau khi một báo giá được đóng dưới dạng Đã giành được, ứng dụng sẽ cấu trúc lại chi phí bằng cách đảo ngược các giá trị chi phí thực tế cũ hơn và tạo lại giá trị chi phí thực tế mới. Ứng dụng sẽ xử lý các giá trị chi phí thực tế này dựa trên Phương thức thanh toán của mô tả hợp đồng dự án liên quan. Nếu các giá trị thực của chi phí tham chiếu một dòng mô tả về thời gian và nguyên vật liệu trên hợp đồng, các giá trị thực của giao dịch chưa lập hóa đơn sẽ được tạo khi báo giá bị đóng và hợp đồng dự án được tạo. Nếu các giá trị thực của chi phí tham chiếu một dòng mô tả về giá cố định trên hợp đồng, thì ứng dụng sẽ ngừng xử lý lại các giá trị thực của chi phí được dựa trên quy tắc phân tách hóa đơn dành cho khách hàng trong hợp đồng dự án.

## <a name="closing-a-quote-as-lost"></a>Đóng báo giá dưới dạng đã mất:

Khi đóng báo giá dưới dạng Đã mất, trạng thái sẽ được chuyển sang Đã đóng và lý do dẫn đến trạng thái là Đã mất. Việc đóng báo giá làm cho báo giá dự án ở chế độ chỉ đọc. Vì không thể mở lại báo giá đã đóng, vì vậy trước khi bạn đóng báo giá, hộp thoại xác nhận sẽ xác nhận các thay đổi của bạn.

Nếu có báo giá đóng dưới dạng Đã mất tham chiếu một dự án trên dòng bất kỳ, thì dự án đó cũng sẽ được đánh dấu là Đã đóng. Mọi mục đặt trước nguồn lực từ ngày đó trở đi sẽ bị hủy.

> [!NOTE]
> Trong Project Operations, việc đóng báo giá dưới dạng Đã giành được hay Đã mất sẽ không ảnh hưởng đến trạng thái đó của Cơ hội. Cơ hội sẽ vẫn mở cho đến khi được đóng theo cách thủ công.
