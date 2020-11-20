---
title: Tại sao tôi không thể xóa bản ghi khỏi thực thể thực tế?
description: Chủ đề này cung cấp thông tin về lý do tại sao bạn không thể xóa các bản ghi khỏi thực thể thực tế.
author: JPBurrows
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: b9b45e3ae0cd9273af4d2a5cd9cce30502c0aa78
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127184"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="4c5ef-103">Tại sao tôi không thể xóa bản ghi khỏi thực thể Thực tế?</span><span class="sxs-lookup"><span data-stu-id="4c5ef-103">Why can’t I delete records from the Actuals entity?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="4c5ef-104">Project Service Automation (PSA) không cho phép bạn xóa thực tế vì chúng đóng vai trò là nguồn của sự thật cho các giao dịch có tác động tài chính đến hệ thống xuôi tuyến, chẳng hạn như sổ cái chung.</span><span class="sxs-lookup"><span data-stu-id="4c5ef-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="4c5ef-105">Nếu có thể xóa thực tế, thì tính toàn vẹn của các giao dịch báo cáo tài chính có thể được hỏi.</span><span class="sxs-lookup"><span data-stu-id="4c5ef-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="4c5ef-106">Để thiết lập lịch sử kiểm tra, khách hàng nên sử dụng nhật ký để tạo các giao dịch bù.</span><span class="sxs-lookup"><span data-stu-id="4c5ef-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>

