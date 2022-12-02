---
title: Chuyển đổi trạng thái trên một hợp đồng phụ
description: Bài viết này giải thích các chuyển tiếp trạng thái trên hợp đồng phụ trong Microsoft Dynamics 365 Project Operations khi hợp đồng phụ được tạo, thực thi và đóng.
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

Bài viết này giải thích các chuyển tiếp trạng thái trên hợp đồng phụ trong Microsoft Dynamics 365 Project Operations. Mỗi trạng thái được thể hiện dưới dạng bản nháp, đã xác nhận, đã đóng hoặc đã hủy. Hình minh họa sau đây cho thấy các chuyển tiếp trạng thái.

![Mô hình trạng thái hợp đồng phụ](../media/SubconStates.png)  

Bảng sau cung cấp mô tả về mỗi trạng thái đại diện trong vòng đời của hợp đồng phụ trong Project Operations.

| Bang | Description | Chuyển tiếp được cho phép |
| --- | --- | --- |
| Bản nháp | Điều này thể hiện trạng thái ban đầu của hợp đồng phụ. Đang tiến hành thương lượng với nhà cung cấp. Mô tả và giá có thể được sửa đổi. Một hợp đồng phụ ở trạng thái này có thể được sử dụng để ước tính và bố trí nhân sự theo yêu cầu của dự án cho nguồn lực và vật tư. Nó cũng có thể được tham chiếu về thời gian, chi phí và việc sử dụng vật tư cho một dự án. Hợp đồng phụ của nhà cung cấp trong trạng thái này không thể chỉnh sửa và xóa. | Đã xác nhận |
| Đã xác nhận | Điều này thể hiện giai đoạn của hợp đồng phụ sau khi thương lượng với nhà cung cấp về giá và mục hàng được mua đã hoàn thành. Tuy nhiên, việc giao vật tư và/hoặc công việc thực tế bằng các nguồn lực trong hợp đồng phụ vẫn đang diễn ra. Một hợp đồng phụ ở trạng thái này có thể được sử dụng để ước tính và bố trí nhân sự theo yêu cầu của dự án cho nguồn lực và vật tư. Nó cũng có thể được tham chiếu về thời gian, chi phí và việc sử dụng vật tư cho một dự án. Hợp đồng phụ của nhà cung cấp trong trạng thái này không thể chỉnh sửa hoặc xóa. Nút **Hủy** cho phép bạn hủy hợp đồng phụ đã xác nhận. Nút **Mở lại** cho phép bạn mở lại hợp đồng phụ để đưa nó trở lại trạng thái **Bản thảo**. Sử dụng nút **Đóng** để đóng một hợp đồng phụ đã xác nhận. | Đã đóng <br> Đã huỷ <br> Bản nháp |
| Đã đóng | Trạng thái này đại diện cho giai đoạn của hợp đồng phụ khi việc giao vật tư và/hoặc công việc thực tế bằng các nguồn lực của hợp đồng phụ được hoàn thành. Một hợp đồng phụ ở trạng thái này không còn được sử dụng để ước tính và bố trí nhân sự theo yêu cầu của dự án cho nguồn lực và vật tư. Ngoài ra, nó cũng không thể được tham chiếu về thời gian, chi phí và việc sử dụng vật tư cho một dự án. Hợp đồng phụ của nhà cung cấp trong trạng thái này không thể chỉnh sửa hoặc xóa. | Không có |
| Đã huỷ | Trạng thái này đại diện cho giai đoạn của hợp đồng phụ khi việc giao vật tư và/hoặc công việc thực tế bằng các nguồn lực của hợp đồng phụ không còn cần thiết nữa. Hợp đồng phụ trong trạng thái này không thể được sử dụng để ước tính và bố trí yêu cầu dự án cho nguồn lực và vật tư, cũng như không thể được tham chiếu trên thời gian, chi phí và sử dụng vật tư trong dự án. Hợp đồng phụ của nhà cung cấp trong trạng thái này không thể chỉnh sửa hoặc xóa. | Không có |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
