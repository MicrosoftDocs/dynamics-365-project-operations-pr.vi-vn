---
title: Xác nhận hợp đồng dự án
description: Chủ đề này cung cấp thông tin về cách xác nhận hợp đồng trong Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 24da0887c0266d51bddcbbf8efd6f2644b6d0f4f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128313"
---
# <a name="confirm-a-project-contract"></a>Xác nhận hợp đồng dự án

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Hợp đồng dự án trong Dynamics 365 Project Operations có thể ở trạng thái hiện hoạt với lý do **Đã xác nhận** hoặc bị đóng với lý do **Đã mất**. Khi bạn xác nhận hợp đồng dự án, trạng thái sẽ được cập nhật từ **Bản nháp** thành **Hiện hoạt** và lý do dẫn đến trạng thái là **Đã xác nhận**. Bạn không thể chỉnh sửa hoặc mở lại hợp đồng hiện hoạt hoặc đã đóng. 

### <a name="financial-impact-of-confirming-a-project-contract"></a>Tác động tài chính của việc xác nhận hợp đồng dự án

Sau khi hợp đồng dự án được xác nhận, ứng dụng sẽ tính lại chi phí bằng cách đảo ngược các giá trị chi phí thực tế cũ hơn và tạo giá trị chi phí thực tế mới. Sau đó, giá trị chi phí thực tế mới được xử lý dựa trên phương thức thanh toán của mục mô tả hợp đồng dự án được liên kết. Nếu giá trị chi phí thực tế tham chiếu đến mục mô tả hợp đồng Thời gian và vật tư, thì ứng dụng sẽ tự động tạo lại các giá trị thực tế doanh số chưa lập hóa đơn tương ứng. Nếu các giá trị chi phí thực tế tham chiếu đến mục mô tả hợp đồng Giá cố định, thì ứng dụng sẽ ngừng xử lý lại giá trị chi phí thực tế.

Giới hạn không vượt quá, mục thiết lập khả năng tính phí, giá và chi phí trên giá trị thực tế sẽ được đánh giá và sau đó được cập nhật trong quy trình xác nhận.

## <a name="close-a-project-contract-as-lost"></a>Đóng hợp đồng dự án ở dạng đã mất

Khi bạn đóng hợp đồng dự án ở dạng đã mất, trạng thái hợp đồng được cập nhật thành **Đã đóng** và lý do dẫn đến trạng thái là **Đã mất**. Hợp đồng dự án trở thành dạng chỉ đọc. Hộp thoại xác nhận được cung cấp trước khi các thay đổi hoàn tất, vì bạn không thể mở lại hợp đồng dự án đã đóng.

Nếu hợp đồng dự án đã đóng ở dạng bị mất tham chiếu đến một dự án trên các mục mô tả của nó, thì dự án đó cũng được đánh dấu là đã đóng. Mọi mục đặt trước nguồn lực từ ngày đó trở đi sẽ bị hủy. Nếu có giá trị thực tế doanh số chưa lập hóa đơn nào trong hợp đồng dự án chưa được đưa vào hóa đơn, thì mục đó sẽ được đảo ngược.

> [!NOTE]
> Trong Dynamics 365 Project Operations, việc đóng hợp đồng dự án ở dạng bị mất sẽ không ảnh hưởng đến trạng thái của cơ hội được liên kết. Cơ hội sẽ vẫn mở và phải được đóng thủ công.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]