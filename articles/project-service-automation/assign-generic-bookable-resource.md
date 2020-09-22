---
title: Phân công nhiệm vụ và nhóm dự án cho nguồn lực có thể đặt lịch chung
description: Chủ đề này cung cấp thông tin về cách đặt nguồn lực chung cho nhóm dự án và nhiệm vụ.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: f461fbd3-1fce-4aeb-a896-a6d14453a5a4
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 82478e2cf97ab03e80e9f5fbb662b3603d5905b9
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 03/24/2020
ms.locfileid: "3757151"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a>Phân công nhiệm vụ cho nguồn lực có thể đặt lịch chung và tạo yêu cầu nguồn lực 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Ngoài việc đặt và phân công các nguồn lực có tên hoặc nguồn lực thực tế cho dự án của bạn, bạn có thể phân công nhiệm vụ dự án cho các nguồn lực chung. Các nguồn lực này có thể đóng vai trò như là chỗ dành sẵn cho nguồn lực được đặt tên cho đến khi bạn đã sẵn sàng phân công dự án cho nguồn lực có tên. 

1. Trong Project Service Automation (PSA), mở trang **Dự án** và trên tab **Lịch trình**, nhập tên vị trí của nguồn lực chung trong ô **Nguồn lực** của lịch trình. Hoặc nhấp vào biểu tượng **Nguồn lực** trong ô để mở bộ chọn nguồn lực, sau đó nhập tên của nguồn lực chung mà bạn muốn tạo.

![Tạo và chỉ định một thành viên nhóm chung](media/RM-how-to-9.png)

Điều này sẽ mở bảng điều khiển **Tạo nhanh: Thành viên nhóm dự án**. 

2. Nhập vai trò và đơn vị tổ chức của thành viên nhóm nguồn lực chung, sau đó nhấp vào **Lưu**.

![Tạo nhanh thành viên nhóm chung](media/RM-how-to-10.png)

3. Sau khi bạn đã tạo thành viên nhóm nguồn lực chung mới, thành viên đó sẽ được phân công tác vụ. Bạn có thể tiếp tục phân công nhiệm vụ khác cho nguồn lực chung trong lịch trình nhiệm vụ.

![Phân công nhiệm vụ cho thành viên nhóm chung hiện có](media/RM-how-to-11.png)

4. Sau khi bạn chỉ định nguồn lực chung, bạn có thể tạo yêu cầu nguồn lực và hoàn thành bằng cách trực tiếp đặt hoặc gửi một yêu cầu nguồn lực cho Resource Manager.

![Tạo yêu cầu cho thành viên nhóm chung](media/RM-how-to-12.png)

Trên lưới thành viên nhóm, ngoài việc có thể sử dụng bộ chọn nguồn lực như đã đề cập ở trên, bạn có thể thêm trực tiếp các nguồn lực chung. Các nguồn lực được thêm vào với một yêu cầu nguồn lực dựa trên ngày bắt đầu/kết thúc và phương pháp phân bổ được chỉ định trong bảng điều khiển **Tạo nhanh: Thành viên nhóm dự án**.

Bạn có thể thấy sự khác biệt nếu bạn thêm các thành viên nhóm chung trực tiếp và sau đó gán nhiều nhiệm vụ cho nguồn lực chung hơn là số giờ họ có. Nhấp vào **Tạo yêu cầu** để tạo lại yêu cầu nhằm cân bằng số giờ yêu cầu so với phân công.

Bạn cũng có thể nhấp vào liên kết **Yêu cầu nguồn lực** trong lưới nhóm để mở yêu cầu và thêm kỹ năng, nguồn lực ưu tiên, v.v.

![Yêu cầu nguồn lực](media/RM-how-to-13.png)

