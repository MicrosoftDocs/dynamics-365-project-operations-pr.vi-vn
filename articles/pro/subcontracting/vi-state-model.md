---
title: Chuyển đổi trạng thái trên hóa đơn của nhà cung cấp
description: Bài viết này giải thích các chuyển tiếp trạng thái trên hóa đơn của nhà cung cấp trong Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e25e4d63d4c9098112a7f40abe60c7184018d582
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261070"
---
# <a name="state-transitions-on-a-vendor-invoice"></a>Chuyển đổi trạng thái trên hóa đơn của nhà cung cấp

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Bài viết này giải thích các chuyển tiếp trạng thái trên hóa đơn của nhà cung cấp trong Microsoft Dynamics 365 Project Operations. Các trạng thái sau được sử dụng: **Bản thảo**, **Đang được xem xét**, **Đã xác nhận**, **Tạm dừng** và **Đã hủy**.

Những hình minh họa sau đây cho thấy các chuyển tiếp trạng thái.

![Mô hình chuyển đổi trạng thái hợp đồng phụ.](../media/VI_State_Model.jpg)

Bảng sau giải thích những gì mỗi trạng thái đại diện trong vòng đời của hóa đơn nhà cung cấp trong Project Operations.

| Bang | Description | Chuyển tiếp được cho phép |
| --- | --- | --- |
| Bản nháp | Trạng thái này là trạng thái ban đầu của hóa đơn nhà cung cấp. Mô tả và giá có thể được sửa đổi. Hóa đơn của nhà cung cấp trong trạng thái này có thể được chỉnh sửa và xóa. | Đang tiến hành |
| Đang được đánh giá | Trạng thái này thể hiện trạng thái xử lý của hóa đơn nhà cung cấp. Ít nhất một mô tả hóa đơn của nhà cung cấp có trạng thái xác minh là **Đang tiến hành**. | Đã xác nhận, Tạm dừng |
| Đã xác nhận | Trạng thái này đại diện cho giai đoạn của một hóa đơn nhà cung cấp trong đó ứng dụng đã tạo chi phí thực tế cho mỗi mô tả hóa đơn của nhà cung cấp. Bất kỳ chi phí thực tế đã liên kết nào được khớp với mô tả hóa đơn của nhà cung cấp đã được đảo ngược và thay thế bằng chi phí thực tế từ mô tả hóa đơn của nhà cung cấp đó. Hóa đơn của nhà cung cấp trong trạng thái này không thể chỉnh sửa hoặc xóa. Bạn có thể dùng nút **Hủy** để hủy hóa đơn của nhà cung cấp đã xác nhận. Hành động Hủy sẽ đảo ngược tác động của hành động Xác nhận. | Đã huỷ |
| Tạm giữ | <p>Trạng thái này đại diện cho một giai đoạn của hóa đơn nhà cung cấp trong đó hóa đơn của nhà cung cấp không thể di chuyển do sự cố với hóa đơn hoặc trạng thái của nhà cung cấp. Hóa đơn của nhà cung cấp trong trạng thái này không thể được xác nhận, hủy, chỉnh sửa hoặc xóa.</p><p>Bạn có thể sử dụng hành động Mở lại để chuyển hóa đơn của nhà cung cấp sang trạng thái **Bản thảo** hoặc **Đang được xem xét**. Nếu ít nhất một dòng trên hóa đơn của nhà cung cấp có trạng thái xác minh là **Đang tiến hành** hoặc **Hoàn thành**, hóa đơn của nhà cung cấp sẽ được mở lại ở trạng thái **Đang được xem xét**. Nếu tất cả các mô tả trên hóa đơn của nhà cung cấp có trạng thái xác minh là **Chưa bắt đầu**, hóa đơn của nhà cung cấp sẽ được mở lại trong trạng thái **Bản thảo**.</p> | Bản thảo, Đang được xem xét |
| Đã huỷ | Trạng thái này đại diện cho giai đoạn của hợp đồng phụ mà việc giao vật tư và/hoặc công việc thực tế bằng các nguồn lực của hợp đồng phụ không còn được yêu cầu nữa. Hợp đồng phụ trong trạng thái này không thể được sử dụng để ước tính và bố trí yêu cầu dự án cho nguồn lực và vật tư, đồng thời không thể được tham chiếu trên thời gian, chi phí và sử dụng vật tư trong dự án. Hợp đồng phụ của nhà cung cấp trong trạng thái này không thể chỉnh sửa hoặc xóa. | Không có |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
