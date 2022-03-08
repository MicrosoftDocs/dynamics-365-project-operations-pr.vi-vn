---
title: Tại sao tôi không thể xóa bản ghi khỏi thực thể thực tế?
description: Chủ đề này cung cấp thông tin về lý do tại sao bạn không thể xóa các bản ghi khỏi thực thể thực tế.
author: JPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 11/6/2018
ms.topic: article
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
ms.openlocfilehash: d60a3586fd1f0f688bcd2626d039ebc1aa6b0925c90d676f0e716400d8e8d6dd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/06/2021
ms.locfileid: "7002897"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a>Tại sao tôi không thể xóa bản ghi khỏi thực thể Thực tế?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Project Service Automation (PSA) không cho phép bạn xóa thực tế vì chúng đóng vai trò là nguồn của sự thật cho các giao dịch có tác động tài chính đến hệ thống xuôi tuyến, chẳng hạn như sổ cái chung. Nếu có thể xóa thực tế, thì tính toàn vẹn của các giao dịch báo cáo tài chính có thể được hỏi. Để thiết lập lịch sử kiểm tra, khách hàng nên sử dụng nhật ký để tạo các giao dịch bù.



[!INCLUDE[footer-include](../includes/footer-banner.md)]