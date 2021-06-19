---
title: Đặt nguồn lực có tên từ yêu cầu nguồn lực
description: Chủ đề này cung cấp thông tin về đặt lịch nguồn lực có tên cho một yêu cầu nguồn lực chung.
author: JohnPBurrows
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
ms.openlocfilehash: c2f97107de938975491770ab4e2ed18a3145d0e3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013422"
---
# <a name="book-named-resources-from-resource-requirements"></a><span data-ttu-id="3dc98-103">Đặt nguồn lực có tên từ yêu cầu nguồn lực</span><span class="sxs-lookup"><span data-stu-id="3dc98-103">Book named resources from resource requirements</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="3dc98-104">Bạn có thể đặt một nguồn lực được đặt tên để thay thế nguồn lực chung có yêu cầu nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="3dc98-104">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="3dc98-105">Trong Project Service Automation (PSA), trên trang **Dự án**, nhấp vào tab **Nhóm**.</span><span class="sxs-lookup"><span data-stu-id="3dc98-105">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab.</span></span>
2. <span data-ttu-id="3dc98-106">Chọn nguồn lực chung có yêu cầu nguồn lực từ danh sách, sau đó nhấp vào **Đặt lịch**.</span><span class="sxs-lookup"><span data-stu-id="3dc98-106">Select the generic resource that has a resource requirement from the list and then click **Book**.</span></span> <span data-ttu-id="3dc98-107">Hoặc mở yêu cầu nguồn lực rồi nhấp vào **Đặt lịch**.</span><span class="sxs-lookup"><span data-stu-id="3dc98-107">Or, open the resource requirement and then click **Book**.</span></span>


![Đặt một thành viên nhóm chung](media/RM-how-to-14.png)


3. <span data-ttu-id="3dc98-109">Trên trang **Trợ lý lịch trình**, chọn nguồn lực có tên để đặt lịch vào nhóm dự án của bạn rồi nhấp vào **Đặt lịch**.</span><span class="sxs-lookup"><span data-stu-id="3dc98-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then click **Book**.</span></span>

![Đặt một thành viên nhóm chung bằng trợ lý lịch trình](media/RM-how-to-15.png)

<span data-ttu-id="3dc98-111">Khi đặt lịch xong và được thực hiện bởi một nguồn lực có tên, thì nguồn lực chung được thay thế bằng nguồn lực có tên đó.</span><span class="sxs-lookup"><span data-stu-id="3dc98-111">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

![Thành viên nhóm có tên thay thế cho thành viên nhóm chung](media/RM-how-to-16.png)

<span data-ttu-id="3dc98-113">Các phân công trên lịch trình cũng được cập nhật bằng nguồn lực có tên.</span><span class="sxs-lookup"><span data-stu-id="3dc98-113">The assignments on the schedule are updated with the named resource as well.</span></span>

![Thành viên nhóm có tên được phân công cho nhiệm vụ dự án](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="3dc98-115">Hoàn thành một nguồn lực chung với nhiều nguồn lực được đặt tên</span><span class="sxs-lookup"><span data-stu-id="3dc98-115">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="3dc98-116">Thực hiện một yêu cầu cho một nguồn lực chung với nhiều nguồn lực có tên sẽ tương tự như việc gán một nguồn lực có tên.</span><span class="sxs-lookup"><span data-stu-id="3dc98-116">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="3dc98-117">Ví dụ: có một nhiệm vụ với thời gian năm ngày và 120 giờ làm việc.</span><span class="sxs-lookup"><span data-stu-id="3dc98-117">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="3dc98-118">Một nguồn lực không thể hoàn thành nhiệm vụ này trong tám giờ trong năm ngày trong tuần.</span><span class="sxs-lookup"><span data-stu-id="3dc98-118">This task can't be completed by one resource that works a typical eight-hour day over a five day week.</span></span> 

![Một nhiệm vụ cần 120 giờ trong năm ngày](media/RM-how-to-21.png)

<span data-ttu-id="3dc98-120">Yêu cầu này là cho 120 giờ kỹ thuật robot trong năm ngày, trong đó mỗi ngày 24 giờ.</span><span class="sxs-lookup"><span data-stu-id="3dc98-120">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

![Yêu cầu theo ngày](media/RM-how-to-22.png)

<span data-ttu-id="3dc98-122">Đây là một ví dụ khi nhiều nguồn lực được đặt tên là cần thiết để hoàn thành một yêu cầu nguồn lực chung.</span><span class="sxs-lookup"><span data-stu-id="3dc98-122">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="3dc98-123">Bạn sẽ cần phải đặt nhiều nguồn lực để hoàn thành yêu cầu.</span><span class="sxs-lookup"><span data-stu-id="3dc98-123">You will need to book multiple resources to fulfill the requirement.</span></span>

![Đặt nhiều nguồn lực để hoàn thành yêu cầu](media/RM-how-to-23.png)

<span data-ttu-id="3dc98-125">Sự khác biệt chính trong trường hợp này là nguồn lực chung vẫn còn trên nhóm được chỉ định nhiệm vụ và các thành viên nhóm nguồn lực được đặt tên không được chỉ định là một phần của vị trí.</span><span class="sxs-lookup"><span data-stu-id="3dc98-125">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="3dc98-126">Người quản lý dự án có thể gán công việc phù hợp với các nguồn lực được đặt tên.</span><span class="sxs-lookup"><span data-stu-id="3dc98-126">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="3dc98-127">Dạng xem **Hợp nhất** có thể hỗ trợ người quản lý dự án trong việc chia các đặt lịch cho nhiều nguồn lực cho phân công nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="3dc98-127">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="3dc98-128">Điều này không được thực hiện tự động bởi vì trong bất kỳ trường hợp nào phức tạp hơn ví dụ đơn giản ở trên, chẳng hạn như nơi bạn có một yêu cầu gồm nhiều nhiệm vụ, ý định về cách thức người quản lý dự án muốn chỉ định, mà hệ thống cần tính đến.</span><span class="sxs-lookup"><span data-stu-id="3dc98-128">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement, the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="3dc98-129">Bởi vì hệ thống không thể hiểu được ý định, nên có khả năng là các giả định sẽ khác với dự kiến và cho một kết quả không chính xác hoặc không thể đoán trước.</span><span class="sxs-lookup"><span data-stu-id="3dc98-129">Because the system can't understand intent, chances are that the assumptions will be different than intended and an incorrect or unpredictable result will happen.</span></span> <span data-ttu-id="3dc98-130">Kết quả dự đoán được đó là nguồn lực chung vẫn được gán cho đến khi ngời quản lý dự án cố ý tạo phân công với sự trợ giúp của dạng xem **Hợp nhất**.</span><span class="sxs-lookup"><span data-stu-id="3dc98-130">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]