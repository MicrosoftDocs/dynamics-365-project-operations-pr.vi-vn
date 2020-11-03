---
title: Gửi yêu cầu nguồn lực
description: Chủ đề này cung cấp thông tin về việc gửi yêu cầu cho một nguồn lực dự án.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
author: JohnPBurrows
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: bcea3d640d7e9ee2b071c55bff9ade3268edb319
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087201"
---
# <a name="submitting-a-resource-request"></a>Gửi yêu cầu nguồn lực

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Bạn có thể gửi yêu cầu nguồn lực được tạo ra dưới dạng yêu cầu nguồn lực. Sau đó, yêu cầu này được gửi tới người quản lý nguồn lực để thực hiện.

1. Trong Project Service Automation (PSA), trên trang **Dự án** , hãy bấm vào tab **Nhóm** để xem danh sách các nguồn lực có thể đặt. 
2. Chọn nguồn lực chung có yêu cầu nguồn lực từ danh sách rồi bấm vào **Gửi yêu cầu**.

![Gửi yêu cầu nguồn lực](media/RM-how-to-18.png)

Trạng thái yêu cầu của thành viên nhóm chung sẽ thay đổi thành **Đã gửi**.

Sau khi người quản lý nguồn lực thực hiện yêu cầu này, nguồn lực chung sẽ được thay thế bằng một nguồn lực được đặt tên nếu người quản lý nguồn lực thực hiện yêu cầu và đặt nguồn lực được đặt tên. Ngoài ra, nguồn lực chung sẽ vẫn còn trong nhóm và trạng thái yêu cầu sẽ thay đổi thành **Cần đánh giá** , nếu người quản lý nguồn lực đã đề xuất một tài nguyên được đặt tên.
