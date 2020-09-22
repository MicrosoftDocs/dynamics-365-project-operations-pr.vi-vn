---
title: Đặt trước nguồn lực có thể đặt lịch có tên cho nhóm dự án và chỉ định nhiệm vụ
description: Chủ đề này cung cấp thông tin về cách đặt nguồn lực có tên cho nhóm dự án và phân công tác vụ.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: e947986a-e83a-42f4-813e-c82bdfbec33c
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 079ba299f912c75f9ed739d4b6aa3c63189d11d0
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 03/24/2020
ms.locfileid: "3757008"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a><span data-ttu-id="6aa16-103">Đặt trước nguồn lực có thể đặt lịch có tên cho nhóm dự án và chỉ định nhiệm vụ</span><span class="sxs-lookup"><span data-stu-id="6aa16-103">Book named bookable resources to a project team and assign tasks</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="6aa16-104">Bạn có thể thêm nguồn lực được đặt tên vào nhóm dự án của mình bằng cách đặt lịch trực tiếp họ vào nhóm.</span><span class="sxs-lookup"><span data-stu-id="6aa16-104">You can  add a named resource to your project team by booking them directly onto the team.</span></span> <span data-ttu-id="6aa16-105">Để làm như vậy, hãy hoàn thành các bước sau đây.</span><span class="sxs-lookup"><span data-stu-id="6aa16-105">To do this, complete the following steps.</span></span>

1. <span data-ttu-id="6aa16-106">Trong Project Service Automation, truy cập **Dự án**, sau đó chọn mở dự án mà bạn đặt lịch.</span><span class="sxs-lookup"><span data-stu-id="6aa16-106">In  Project Service Automation, go to **Projects**, and select the open the project that you are booking for.</span></span>
2. <span data-ttu-id="6aa16-107">Trên trang **Dự án**, trên tab **Nhóm**, nhấp vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="6aa16-107">On the **Project** page, on the **Team** tab, click **New**.</span></span> 

![Thêm thành viên nhóm từ tab Nhóm](media/RM-how-to-1.png)

3. <span data-ttu-id="6aa16-109">Trong hộp thoại **Tạo nhanh thành viên nhóm dự án**, chọn nguồn lực có thể đặt lịch.</span><span class="sxs-lookup"><span data-stu-id="6aa16-109">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="6aa16-110">Trường **Vai trò** sẽ điền bằng vai trò mặc định của nguồn lực nếu họ được chỉ định.</span><span class="sxs-lookup"><span data-stu-id="6aa16-110">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="6aa16-111">Bạn có thể thay đổi vai trò này nếu cần.</span><span class="sxs-lookup"><span data-stu-id="6aa16-111">You can change the role if needed.</span></span> 
4. <span data-ttu-id="6aa16-112">Chọn ngày bắt đầu và kết thúc mà nguồn lực sẽ cần và chọn phương pháp phân bổ năng lực của nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="6aa16-112">Select the from and to dates that the resource will be needed and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="6aa16-113">Nếu bạn muốn thành viên nhóm là người phê duyệt dự án, chọn **Có** trong trường **Người phê duyệt dự án**.</span><span class="sxs-lookup"><span data-stu-id="6aa16-113">If you want the team member to be a project approver, select **Yes** in the **Project Approver** field.</span></span> <span data-ttu-id="6aa16-114">Điều này có nghĩa là thành viên nhóm có thể phê duyệt các mục nhập thời gian và chi phí đã gửi cho dự án này.</span><span class="sxs-lookup"><span data-stu-id="6aa16-114">This will mean that the team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="6aa16-115">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="6aa16-115">Click **Save**.</span></span>

![Thêm thành viên nhóm trên biểu mẫu tạo nhanh](media/RM-how-to-2.png)


<span data-ttu-id="6aa16-117">Bây giờ bạn có thể gán nguồn lực đã đặt cho các nhiệm vụ dự án.</span><span class="sxs-lookup"><span data-stu-id="6aa16-117">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="6aa16-118">Trên trang **Dự án**, nhấp và tab **Lên lịch** để gán nhiệm vụ cho tài nguyên mới.</span><span class="sxs-lookup"><span data-stu-id="6aa16-118">On the **Project** page, click the **Schedule** tab to assign tasks to the new resource.</span></span> <span data-ttu-id="6aa16-119">Bộ chọn nguồn lực được khởi chạy từ trường **Nguồn lực** trong lưới nhiệm vụ sẽ hiển thị các thành viên nhóm mà bạn có thể chọn.</span><span class="sxs-lookup"><span data-stu-id="6aa16-119">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>

![Chỉ định thành viên nhóm cho nhiệm vụ trên tab lịch trình](media/RM-how-to-3.png)

<span data-ttu-id="6aa16-121">Trong phiên bản 3 của Project Service Automation (PSA), việc đặt lịch nguồn lực và gán nhiệm vụ không ghép đôi chặt chẽ với nhau.</span><span class="sxs-lookup"><span data-stu-id="6aa16-121">In version 3 for Project Service Automation (PSA), resource bookings and task assignments are not tightly coupled.</span></span> <span data-ttu-id="6aa16-122">Điều này có nghĩa là khi bạn sử dụng bộ chọn nguồn lực trong lịch trình, bạn có thể gán nhiệm vụ cho các thành viên trong nhóm trong nhiều giờ hơn so với đặt lịch của họ trên dự án.</span><span class="sxs-lookup"><span data-stu-id="6aa16-122">This means that when you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>
<span data-ttu-id="6aa16-123">Bạn có thể thấy sự khác biệt giữa đặt lịch và phân công thành viên nhóm trên tab **Nhóm** hoặc tab **Hợp nhất nguồn lực**. Bạn cũng có thể hợp nhất sự khác biệt giữa các đặt chỗ và phân công cho các nguồn lực ở mức chi tiết hơn.</span><span class="sxs-lookup"><span data-stu-id="6aa16-123">You can see the differences between team member bookings and assignments on the **Team** tab or on the **Resource Reconciliation** tab. You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

![Tab hợp nhất nguồn lực](media/RM-how-to-4.png)

<span data-ttu-id="6aa16-125">Bạn cũng có thể sử dụng bộ chọn nguồn lực trên tab **Lên lịch** để tìm kiếm và chọn các nguồn lực có thể đặt lịch không phải là một phần của nhóm dự án.</span><span class="sxs-lookup"><span data-stu-id="6aa16-125">You can also use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="6aa16-126">Chúng được hiển thị trong bộ chọn nguồn lực dưới dạng **Nguồn lực khác**.</span><span class="sxs-lookup"><span data-stu-id="6aa16-126">These are shown in the resource picker as **Other Resources**.</span></span>

![Phân công nhiệm vụ cho một nguồn lực không phải thành viên nhóm](media/RM-how-to-5.png)

<span data-ttu-id="6aa16-128">Khi bạn thực hiện việc này, nguồn lực đó sẽ được thêm vào nhóm dự án và phân công tác vụ, nhưng không tạo đặt lịch.</span><span class="sxs-lookup"><span data-stu-id="6aa16-128">When you do this, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

![Thành viên nhóm được phân công và không có đặt lịch](media/RM-how-to-6.png)

<span data-ttu-id="6aa16-130">Bạn có thể sử dụng khả năng đặt lịch mở rộng của tab **Hợp nhất** hoặc **Bảng lịch trình** để đặt lịch năng lực của nguồn lực cho dự án.</span><span class="sxs-lookup"><span data-stu-id="6aa16-130">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

![Mở rộng các đặt lịch cho một thành viên nhóm trên tab hợp nhất nguồn lực](media/RM-how-to-7.png)

<span data-ttu-id="6aa16-132">Sau khi một thành viên nhóm được đặt lịch trên dự án của bạn, bạn có thể sử dụng duy trì đặt phòng hoặc sử dụng Bảng lịch trình để trực tiếp quản lý đặt lịch của họ.</span><span class="sxs-lookup"><span data-stu-id="6aa16-132">After a team member is booked on your project, you can use maintain bookings or use the Schedule Board directly to manage their bookings.</span></span>
