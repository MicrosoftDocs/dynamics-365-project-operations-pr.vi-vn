---
title: Chuyển đổi trạng thái trên hóa đơn của nhà cung cấp
description: Bài viết này giải thích các chuyển đổi trạng thái trên hóa đơn của nhà cung cấp trong Microsoft Dynamics 365 Project Operations.
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

Bài viết này giải thích các chuyển đổi trạng thái trên hóa đơn của nhà cung cấp trong Microsoft Dynamics 365 Project Operations. Các trạng thái sau được sử dụng: **Bản thảo**, **xem xét**, **xác nhận**, **chờ**, và **Đã hủy**.

Các hình minh họa sau đây cho thấy các chuyển đổi trạng thái.

![Hợp đồng phụ mô hình chuyển đổi trạng thái.](../media/VI_State_Model.jpg)

Bảng sau đây giải thích những gì mỗi trạng thái đại diện trong vòng đời của hóa đơn nhà cung cấp trong Hoạt động dự án.

| Bang | Description | Chuyển đổi được phép |
| --- | --- | --- |
| Bản nháp | Trạng thái này là trạng thái ban đầu của hóa đơn nhà cung cấp. Các dòng và giá cả có thể sửa đổi. Hóa đơn của nhà cung cấp ở trạng thái này có thể được chỉnh sửa và xóa. | Đang tiến hành |
| Đang được đánh giá | Trạng thái này đại diện cho trạng thái xử lý của hóa đơn nhà cung cấp. Ít nhất một dòng hóa đơn của nhà cung cấp có trạng thái xác minh là **Trong tiến trình**. | Đã xác nhận, đang chờ |
| Đã xác nhận | Trạng thái này đại diện cho giai đoạn của một hóa đơn nhà cung cấp trong đó ứng dụng đã tạo các chi phí thực tế cho mỗi dòng hóa đơn của nhà cung cấp. Bất kỳ thực tế chi phí được liên kết nào được khớp với các dòng hóa đơn của nhà cung cấp đã được hoàn nguyên và thay thế bằng các thực tế chi phí từ các dòng hóa đơn của nhà cung cấp đó. Không thể chỉnh sửa hoặc xóa hóa đơn của nhà cung cấp ở trạng thái này. Bạn có thể dùng **Hủy bỏ** nút để hủy hóa đơn của nhà cung cấp đã xác nhận. Hành động Hủy sẽ đảo ngược tác động của hành động Xác nhận. | Đã huỷ |
| Tạm giữ | <p>Trạng thái này đại diện cho một giai đoạn của hóa đơn nhà cung cấp trong đó hóa đơn của nhà cung cấp không thể di chuyển do vấn đề với hóa đơn hoặc trạng thái của nhà cung cấp. Không thể xác nhận, hủy, chỉnh sửa hoặc xóa hóa đơn của nhà cung cấp ở trạng thái này.</p><p>Bạn có thể sử dụng hành động Mở lại để chuyển hóa đơn của nhà cung cấp đến **Bản thảo** hoặc **Đang xem xét** tiểu bang. Nếu ít nhất một dòng trên hóa đơn của nhà cung cấp có trạng thái xác minh là **Trong tiến trình** hoặc **Hoàn thành**, hóa đơn của nhà cung cấp sẽ được mở lại trong **Đang xem xét** tiểu bang. Nếu tất cả các dòng trên hóa đơn của nhà cung cấp có trạng thái xác minh là **Chưa bắt đầu**, hóa đơn của nhà cung cấp sẽ được mở lại trong **Bản thảo** tiểu bang.</p> | Bản nháp, Đang xem xét |
| Đã huỷ | Trạng thái này đại diện cho giai đoạn của hợp đồng phụ mà việc giao vật liệu và / hoặc công việc thực tế bằng các nguồn lực của hợp đồng phụ không còn được yêu cầu nữa. Hợp đồng phụ ở trạng thái này không thể được sử dụng để ước tính và yêu cầu của nhân viên dự án về nguồn lực và vật liệu, đồng thời cũng không thể được tham chiếu về thời gian, chi phí và việc sử dụng vật liệu cho một dự án. Không thể chỉnh sửa hoặc xóa hợp đồng phụ ở trạng thái này. | Không có |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]