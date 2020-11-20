---
title: Gửi yêu cầu nguồn lực
description: Chủ đề này cung cấp thông tin về việc gửi yêu cầu cho một nguồn lực dự án.
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 50f076b89c5ac7fee4866534cbd47d81f92f3ab3
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131322"
---
# <a name="submitting-a-resource-request"></a><span data-ttu-id="0704a-103">Gửi yêu cầu nguồn lực</span><span class="sxs-lookup"><span data-stu-id="0704a-103">Submitting a resource request</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="0704a-104">Bạn có thể gửi yêu cầu nguồn lực được tạo ra dưới dạng yêu cầu nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="0704a-104">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="0704a-105">Sau đó, yêu cầu này được gửi tới người quản lý nguồn lực để thực hiện.</span><span class="sxs-lookup"><span data-stu-id="0704a-105">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="0704a-106">Trong Project Service Automation (PSA), trên trang **Dự án**, hãy bấm vào tab **Nhóm** để xem danh sách các nguồn lực có thể đặt.</span><span class="sxs-lookup"><span data-stu-id="0704a-106">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab to view a list bookable resources.</span></span> 
2. <span data-ttu-id="0704a-107">Chọn nguồn lực chung có yêu cầu nguồn lực từ danh sách rồi bấm vào **Gửi yêu cầu**.</span><span class="sxs-lookup"><span data-stu-id="0704a-107">Select the generic resource that has a resource requirement from the list and then click **Submit Request**.</span></span>

![Gửi yêu cầu nguồn lực](media/RM-how-to-18.png)

<span data-ttu-id="0704a-109">Trạng thái yêu cầu của thành viên nhóm chung sẽ thay đổi thành **Đã gửi**.</span><span class="sxs-lookup"><span data-stu-id="0704a-109">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="0704a-110">Sau khi người quản lý nguồn lực thực hiện yêu cầu này, nguồn lực chung sẽ được thay thế bằng một nguồn lực được đặt tên nếu người quản lý nguồn lực thực hiện yêu cầu và đặt nguồn lực được đặt tên.</span><span class="sxs-lookup"><span data-stu-id="0704a-110">After the request is fulfilled by the resource manager, the generic resource will be replaced by a named resource if the resource manager fulfills the request with the booking of a named resource.</span></span> <span data-ttu-id="0704a-111">Ngoài ra, nguồn lực chung sẽ vẫn còn trong nhóm và trạng thái yêu cầu sẽ thay đổi thành **Cần đánh giá**, nếu người quản lý nguồn lực đã đề xuất một tài nguyên được đặt tên.</span><span class="sxs-lookup"><span data-stu-id="0704a-111">Otherwise, the generic resource will remain on the team and the request status will change to **Needs Review**, if the resource manager has proposed a named resource.</span></span>
