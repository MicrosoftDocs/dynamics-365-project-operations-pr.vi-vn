---
title: Chuyển đổi trạng thái trên một hợp đồng phụ
description: Bài viết này giải thích các chuyển đổi trạng thái trên hợp đồng phụ trong Microsoft Dynamics 365 Project Operations khi hợp đồng phụ được tạo, thực thi và đóng.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2804fc30f8dade42dc1093e5fc0f01fa1db22ca3
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522957"
---
# <a name="state-transitions-on-a-subcontract"></a>Chuyển đổi trạng thái trên một hợp đồng phụ 

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Bài viết này giải thích các chuyển đổi trạng thái trên hợp đồng phụ trong Microsoft Dynamics 365 Project Operations. Mỗi trạng thái được thể hiện dưới dạng bản nháp, được xác nhận, đã đóng hoặc bị hủy. Hình ảnh sau đây đại diện cho các chuyển đổi trạng thái.

![Mô hình trạng thái hợp đồng phụ](../media/SubconStates.png)  

Bảng sau đây cung cấp mô tả về những gì mỗi trạng thái thể hiện trong vòng đời của hợp đồng phụ trong Hoạt động dự án.

| Bang | Description | Chuyển đổi được phép |
| --- | --- | --- |
| Bản nháp | Điều này thể hiện trạng thái ban đầu của hợp đồng phụ. Đang đàm phán với nhà cung cấp. Các dòng và giá cả có thể sửa đổi. Một hợp đồng phụ ở trạng thái này có thể được sử dụng để ước tính và nhân viên dự án yêu cầu về nguồn lực và vật liệu. Nó cũng có thể được tham chiếu về thời gian, chi phí và việc sử dụng vật liệu cho một dự án. Hợp đồng phụ ở trạng thái này có thể được chỉnh sửa và xóa. | Đã xác nhận |
| Đã xác nhận | Điều này thể hiện giai đoạn của hợp đồng phụ sau khi thương lượng với nhà cung cấp về giá cả và mục hàng được mua hoàn tất. Tuy nhiên, việc giao vật liệu và / hoặc công việc thực tế bằng các nguồn lực được thầu phụ vẫn đang diễn ra. Một hợp đồng phụ ở trạng thái này có thể được sử dụng để ước tính và nhân viên dự án yêu cầu về nguồn lực và vật liệu. Nó cũng có thể được tham chiếu về thời gian, chi phí và việc sử dụng vật liệu cho một dự án. Không thể chỉnh sửa hoặc xóa hợp đồng phụ ở trạng thái này. Các **Hủy bỏ** cho phép bạn hủy hợp đồng phụ đã xác nhận. Các **Mở lại** cho phép bạn mở lại hợp đồng phụ để đưa nó trở lại **Bản thảo** trạng thái. Sử dụng **Đóng** để đóng một hợp đồng phụ đã được xác nhận. | Đã đóng <br> Đã huỷ <br> Bản nháp |
| Đã đóng | Điều này thể hiện giai đoạn của hợp đồng phụ khi việc giao vật liệu và / hoặc công việc thực tế bằng các nguồn lực của hợp đồng phụ được hoàn thành. Hợp đồng phụ ở trạng thái này không còn có thể được sử dụng để ước tính và yêu cầu của nhân viên dự án đối với các nguồn lực và vật liệu. Ngoài ra, nó không còn có thể được tham chiếu về thời gian, chi phí và việc sử dụng vật liệu trong một dự án. Không thể chỉnh sửa hoặc xóa hợp đồng phụ ở trạng thái này. | Không có |
| Đã huỷ | Điều này thể hiện giai đoạn của hợp đồng phụ khi việc giao vật liệu và / hoặc công việc thực tế bằng các nguồn lực của hợp đồng phụ không còn cần thiết nữa. Hợp đồng phụ ở trạng thái này không thể được sử dụng để ước tính và yêu cầu của nhân viên dự án đối với các nguồn lực và vật liệu cũng như không thể tham chiếu nó về thời gian, chi phí và việc sử dụng vật liệu cho một dự án. Không thể chỉnh sửa hoặc xóa hợp đồng phụ ở trạng thái này. | Không có |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
