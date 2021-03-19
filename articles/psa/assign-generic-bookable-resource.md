---
title: Phân công nhiệm vụ và nhóm dự án cho nguồn lực có thể đặt lịch chung
description: Chủ đề này cung cấp thông tin về cách đặt nguồn lực chung cho nhóm dự án và nhiệm vụ.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: 5b4c47513b96310745fd2cdb296988a57df0e966
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291420"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a><span data-ttu-id="5b47f-103">Phân công nhiệm vụ cho nguồn lực có thể đặt lịch chung và tạo yêu cầu nguồn lực</span><span class="sxs-lookup"><span data-stu-id="5b47f-103">Assign generic bookable resources to a task and generate resource requirements</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="5b47f-104">Ngoài việc đặt và phân công các nguồn lực có tên hoặc nguồn lực thực tế cho dự án của bạn, bạn có thể phân công nhiệm vụ dự án cho các nguồn lực chung.</span><span class="sxs-lookup"><span data-stu-id="5b47f-104">In addition to booking and assigning named or real resources to your project, you can assign generic resources to project tasks.</span></span> <span data-ttu-id="5b47f-105">Các nguồn lực này có thể đóng vai trò như là chỗ dành sẵn cho nguồn lực được đặt tên cho đến khi bạn đã sẵn sàng phân công dự án cho nguồn lực có tên.</span><span class="sxs-lookup"><span data-stu-id="5b47f-105">These resources can serve as placeholders for named resources until you are ready to staff your project with named resources.</span></span> 

1. <span data-ttu-id="5b47f-106">Trong Project Service Automation (PSA), mở trang **Dự án** và trên tab **Lịch trình**, nhập tên vị trí của nguồn lực chung trong ô **Nguồn lực** của lịch trình.</span><span class="sxs-lookup"><span data-stu-id="5b47f-106">In Project Service Automation (PSA), open the **Project** page and on the **Schedule** tab, enter the position name of the generic resource in the **Resource** cell of the schedule.</span></span> <span data-ttu-id="5b47f-107">Hoặc nhấp vào biểu tượng **Nguồn lực** trong ô để mở bộ chọn nguồn lực, sau đó nhập tên của nguồn lực chung mà bạn muốn tạo.</span><span class="sxs-lookup"><span data-stu-id="5b47f-107">Or, click the **Resource** icon in the cell to open the resource picker and then enter the name of the generic resource that you want to create.</span></span>

![Tạo và chỉ định một thành viên nhóm chung](media/RM-how-to-9.png)

<span data-ttu-id="5b47f-109">Điều này sẽ mở bảng điều khiển **Tạo nhanh: Thành viên nhóm dự án**.</span><span class="sxs-lookup"><span data-stu-id="5b47f-109">This will open the **Quick Create: Project Team Member** panel.</span></span> 

2. <span data-ttu-id="5b47f-110">Nhập vai trò và đơn vị tổ chức của thành viên nhóm nguồn lực chung, sau đó nhấp vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="5b47f-110">Enter the role and organization unit of the generic resource team member and then click **Save**.</span></span>

![Tạo nhanh thành viên nhóm chung](media/RM-how-to-10.png)

3. <span data-ttu-id="5b47f-112">Sau khi bạn đã tạo thành viên nhóm nguồn lực chung mới, thành viên đó sẽ được phân công tác vụ.</span><span class="sxs-lookup"><span data-stu-id="5b47f-112">After you have created the new generic resource team member, it is assigned to the task.</span></span> <span data-ttu-id="5b47f-113">Bạn có thể tiếp tục phân công nhiệm vụ khác cho nguồn lực chung trong lịch trình nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="5b47f-113">You can continue to assign that generic resource to other tasks in the task schedule.</span></span>

![Phân công nhiệm vụ cho thành viên nhóm chung hiện có](media/RM-how-to-11.png)

4. <span data-ttu-id="5b47f-115">Sau khi bạn chỉ định nguồn lực chung, bạn có thể tạo yêu cầu nguồn lực và hoàn thành bằng cách trực tiếp đặt hoặc gửi một yêu cầu nguồn lực cho Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="5b47f-115">After you have assigned the generic resource, you can generate a resource requirement and fulfill it by directly booking or submitting a resource request to a resource manager.</span></span>

![Tạo yêu cầu cho thành viên nhóm chung](media/RM-how-to-12.png)

<span data-ttu-id="5b47f-117">Trên lưới thành viên nhóm, ngoài việc có thể sử dụng bộ chọn nguồn lực như đã đề cập ở trên, bạn có thể thêm trực tiếp các nguồn lực chung.</span><span class="sxs-lookup"><span data-stu-id="5b47f-117">On the team member grid, in addition to being able to use the resource picker as mentioned above, you can add generic resources directly.</span></span> <span data-ttu-id="5b47f-118">Các nguồn lực được thêm vào với một yêu cầu nguồn lực dựa trên ngày bắt đầu/kết thúc và phương pháp phân bổ được chỉ định trong bảng điều khiển **Tạo nhanh: Thành viên nhóm dự án**.</span><span class="sxs-lookup"><span data-stu-id="5b47f-118">The resources are added with a resource requirement that is based on the start/end dates and allocation method specified in the **Quick Create: Project Team Member** panel.</span></span>

<span data-ttu-id="5b47f-119">Bạn có thể thấy sự khác biệt nếu bạn thêm các thành viên nhóm chung trực tiếp và sau đó gán nhiều nhiệm vụ cho nguồn lực chung hơn là số giờ họ có.</span><span class="sxs-lookup"><span data-stu-id="5b47f-119">You can see a difference if you add the generic team member directly and then assign more tasks to the generic resource than they have required hours to cover.</span></span> <span data-ttu-id="5b47f-120">Nhấp vào **Tạo yêu cầu** để tạo lại yêu cầu nhằm cân bằng số giờ yêu cầu so với phân công.</span><span class="sxs-lookup"><span data-stu-id="5b47f-120">Click **Generate Requirement** to regenerate the requirement to balance the required hours against assignments.</span></span>

<span data-ttu-id="5b47f-121">Bạn cũng có thể nhấp vào liên kết **Yêu cầu nguồn lực** trong lưới nhóm để mở yêu cầu và thêm kỹ năng, nguồn lực ưu tiên, v.v.</span><span class="sxs-lookup"><span data-stu-id="5b47f-121">You can also click the **Resource requirement** link in the team grid to open the requirement and add skills, preferred resources, etc.</span></span>

![Yêu cầu nguồn lực](media/RM-how-to-13.png)



[!INCLUDE[footer-include](../includes/footer-banner.md)]