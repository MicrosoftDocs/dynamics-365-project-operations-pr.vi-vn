---
title: Cách phân công một nhiệm vụ cho nguồn lực có thể đặt lịch trong ứng dụng web
description: Tổng quan về các cách bạn có thể phân công nguồn lực có thể đặt lịch.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: b4296837cabd4c6f7e2d2924079658e45ce8b87c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286319"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a><span data-ttu-id="53a61-103">Làm thế nào để tôi gán nguồn lực có thể đăng ký được cho một nhiệm vụ trong ứng dụng web (ứng dụng Project Service v2.x)?</span><span class="sxs-lookup"><span data-stu-id="53a61-103">How do I assign a bookable resource to a task in the web app (Project Service app v2.x)?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="53a61-104">Có hai cách để gán nguồn lực cho một nhiệm vụ trong Project Service.</span><span class="sxs-lookup"><span data-stu-id="53a61-104">There are two ways to assign a resource to a task in Project Service.</span></span> <span data-ttu-id="53a61-105">Bạn có thể đăng ký nguồn lực là thành viên nhóm và gán nguồn lực đó cho nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="53a61-105">You can book a resource as a team member and then assign it to a task.</span></span> <span data-ttu-id="53a61-106">Hoặc bạn có thể tạo thành viên nhóm chung nhờ việc phân công vai trò theo nhiệm vụ, tạo một nhóm và hoàn thành các yêu cầu hỗ trợ bằng nguồn lực được đặt tên.</span><span class="sxs-lookup"><span data-stu-id="53a61-106">Or, you can create a generic team member through role assignment on tasks, generate a team, and then fulfill the backing requirements with a named resource.</span></span>

<span data-ttu-id="53a61-107">Lưu ý rằng nếu bạn muốn gán một nguồn lực có thể đăng ký được cho nhiệm vụ, thành viên nhóm là nguồn lực có thể đăng ký được phải có đủ các đăng ký sẵn có.</span><span class="sxs-lookup"><span data-stu-id="53a61-107">Note that if you’d like to assign a bookable resource to a task, the bookable resource team member must have enough available bookings.</span></span> <span data-ttu-id="53a61-108">Tình trạng của đăng ký phải là Commit Type Hard Book (Đăng ký chắc chắn loại cam kết) và Status Committed (Trạng thái đã được cam kết).</span><span class="sxs-lookup"><span data-stu-id="53a61-108">The status of the booking must be Commit Type Hard Book and Status Committed.</span></span> <span data-ttu-id="53a61-109">Nếu không có đủ số đăng ký cho nguồn lực, Project Service sẽ loại bỏ sự phân công và hiển thị thông báo lỗi như sau:</span><span class="sxs-lookup"><span data-stu-id="53a61-109">If there aren’t enough bookings for the resource, Project Service removes the assignment and displays the following error message:</span></span>

<span data-ttu-id="53a61-110">*Không thể gán nguồn lực cho nhiệm vụ - (Các) Nguồn lực sau không có đủ số giờ được đăng ký cho dự án*</span><span class="sxs-lookup"><span data-stu-id="53a61-110">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project*</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="53a61-111">Đăng ký một nguồn lực là một thành viên nhóm và sau đó gán nguồn lực cho nhiệm vụ</span><span class="sxs-lookup"><span data-stu-id="53a61-111">Book a resource as a team member and then assign the resource to a task</span></span>

<span data-ttu-id="53a61-112">Với phương pháp này bạn có thể thêm nguồn lực cho nhóm dự án và sau đó gán nhiệm vụ cho nguồn lực trong lịch trình dự án.</span><span class="sxs-lookup"><span data-stu-id="53a61-112">With this method you add a resource to the project team and then assign tasks to the resource in the project schedule.</span></span> <span data-ttu-id="53a61-113">Đây là cách làm việc này:</span><span class="sxs-lookup"><span data-stu-id="53a61-113">Here’s how you do this:</span></span>
1.  <span data-ttu-id="53a61-114">Trên lưới thành viên nhóm, thêm một thành viên nhóm bằng cách chọn **Mới**.</span><span class="sxs-lookup"><span data-stu-id="53a61-114">On the team member grid, add a new team member by selecting **New**.</span></span>
2.  <span data-ttu-id="53a61-115">Trên màn hình Team Member Quick Create (Tạo nhanh thành viên nhóm), chọn tên nguồn lực có thể đăng ký được và đặt vai trò.</span><span class="sxs-lookup"><span data-stu-id="53a61-115">On the Team Member Quick Create screen, select the bookable resource name and set a role.</span></span>
3.  <span data-ttu-id="53a61-116">Chọn các ngày **Bắt đầu** và ngày **Kết thúc**.</span><span class="sxs-lookup"><span data-stu-id="53a61-116">Select the **From** and **To** dates.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="53a61-117">![Ảnh chụp màn hình thêm thành viên nhóm](media/FAQ-Resources-to-Tasks2-1.png "Ảnh chụp màn hình thêm thành viên nhóm")</span><span class="sxs-lookup"><span data-stu-id="53a61-117">![Screenshot of adding team member](media/FAQ-Resources-to-Tasks2-1.png "Screenshot of adding team member")</span></span>
 
4.  <span data-ttu-id="53a61-118">Chọn một trong các phương pháp phân bổ sau để đăng ký nguồn lực:</span><span class="sxs-lookup"><span data-stu-id="53a61-118">Select one of the following allocation methods for booking the resource:</span></span>
    - <span data-ttu-id="53a61-119">**Năng lực đầy đủ** đăng ký năng lực đầy đủ của nguồn lực theo các ngày bắt đầu và kết thúc đã được chỉ định.</span><span class="sxs-lookup"><span data-stu-id="53a61-119">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="53a61-120">**Năng lực tỉ lệ phần trăm** đăng ký nguồn lực theo tỉ lệ phần trăm năng lực của nguồn lực theo những ngày bắt đầu và kết thúc.</span><span class="sxs-lookup"><span data-stu-id="53a61-120">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="53a61-121">**Phân phối theo giờ đồng đều** đăng ký nguồn lực cho số giờ được chỉ định, phương pháp này phân phối thời gian mỗi ngày đều nhau cho các ngày đã được chỉ định kể từ khi bắt đầu cho tới khi kết thúc.</span><span class="sxs-lookup"><span data-stu-id="53a61-121">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing it evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="53a61-122">**Phân phối không đồng đều** đăng ký nguồn lực cho số giờ được chỉ định, phương pháp này phân phối không đồng đều thời gian cho mỗi ngày trong các ngày được chỉ định từ khi bắt đầu cho tới khi kết thúc.</span><span class="sxs-lookup"><span data-stu-id="53a61-122">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>

    <span data-ttu-id="53a61-123">Không nên chọn **Không có** vì tính năng này thêm nguồn lực vào nhóm nhưng không tạo bất kỳ đăng ký nào mà sử dụng năng lực của nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="53a61-123">Don’t select **None** because it adds the resource to the team but doesn’t create any bookings that absorb the resource's capacity.</span></span>
5.  <span data-ttu-id="53a61-124">Chọn **Lưu.**</span><span class="sxs-lookup"><span data-stu-id="53a61-124">Select **Save**.</span></span>

    <span data-ttu-id="53a61-125">Lưu ý rằng số giờ của đăng ký phải đủ cho cả số giờ nỗ lực và quãng ngày của nhiệm vụ mà bạn gán nguồn lực này cho.</span><span class="sxs-lookup"><span data-stu-id="53a61-125">Note that the hours of the booking must be enough to cover the effort hours and date ranges of the tasks that you assign this resource to.</span></span> <span data-ttu-id="53a61-126">Nếu chúng không được căn chỉnh, bạn không thể gán nguồn lực cho nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="53a61-126">If they aren’t in alignment, you can’t assign the resource to the task.</span></span>

6.  <span data-ttu-id="53a61-127">Trên Cấu trúc phân tích công việc (WBS) cho nhiệm vụ, bấm vào danh sách thả xuống của ô nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="53a61-127">On the work breakdown structure (WBS) for the task, click the resource cell dropdown.</span></span> <span data-ttu-id="53a61-128">Vậy thì:</span><span class="sxs-lookup"><span data-stu-id="53a61-128">Then:</span></span> 

    1. <span data-ttu-id="53a61-129">Chọn **Thêm**.</span><span class="sxs-lookup"><span data-stu-id="53a61-129">Select **Add**.</span></span>
    2. <span data-ttu-id="53a61-130">Chọn danh sách thả xuống ở dưới **Nguồn lực** và chọn thành viên nhóm bạn đã thêm vào ở trên.</span><span class="sxs-lookup"><span data-stu-id="53a61-130">Select the dropdown under **Resources** and select the team member you added above.</span></span>
    3. <span data-ttu-id="53a61-131">Chọn **OK**.</span><span class="sxs-lookup"><span data-stu-id="53a61-131">Select **OK**.</span></span> <span data-ttu-id="53a61-132">Thành viên nhóm hiện được gán cho nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="53a61-132">The team member is now assigned to the task.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="53a61-133">![Ảnh chụp màn hình thêm tài nguyên với WBS](media/FAQ-Resources-to-Tasks2-2.png "Ảnh chụp màn hình thêm tài nguyên với WBS")</span><span class="sxs-lookup"><span data-stu-id="53a61-133">![Screenshot of adding resources with WBS](media/FAQ-Resources-to-Tasks2-2.png "Screenshot of adding resources with WBS")</span></span>
 
<span data-ttu-id="53a61-134">Trên lưới điện thành viên nhóm, bạn sẽ thấy sự tổng hợp của số giờ đã được gán của nguồn lực dưới phần Số giờ được gán.</span><span class="sxs-lookup"><span data-stu-id="53a61-134">On the team member grid, you’ll see the aggregate of the resource’s assigned hours under Assigned Hours.</span></span> <span data-ttu-id="53a61-135">Số giờ đó sẽ ít hơn hoặc bằng với số giờ đã được đăng ký cho nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="53a61-135">It will be less than or equal to the booked hours for the resource.</span></span> 

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="53a61-136">![Ảnh chụp màn hình số giờ được chỉ định cho một tài nguyên](media/FAQ-Resources-to-Tasks2-3.png "Ảnh chụp màn hình số giờ được chỉ định cho một tài nguyên")</span><span class="sxs-lookup"><span data-stu-id="53a61-136">![Screenshot of assigned hours for a resource](media/FAQ-Resources-to-Tasks2-3.png "Screenshot of assigned hours for a resource")</span></span>
 
<span data-ttu-id="53a61-137">Nếu nhiệm vụ mà bạn đang cố gán cho nguồn lực bắt đầu sau ngày kết thúc của đăng ký nguồn lực, nguồn lực sẽ không hiện lên trong danh sách thả xuống.</span><span class="sxs-lookup"><span data-stu-id="53a61-137">If the task you’re attempting to assign to the resource starts after the end date of the resources bookings, the resource won’t appear in the dropdown.</span></span>

<span data-ttu-id="53a61-138">Lưu ý rằng bạn có thể gán nguồn lực cho số giờ nhiều hơn số giờ đã được đăng ký của nguồn lực nếu nguồn lực còn một số năng lực còn lại mà chưa được gán.</span><span class="sxs-lookup"><span data-stu-id="53a61-138">Note that you can assign a resource to more hours than their booked hours if the resource has some remaining unassigned capacity.</span></span> <span data-ttu-id="53a61-139">Trong trường hợp này, nguồn lực sẽ chỉ được gán từng phần cho đăng ký của nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="53a61-139">In this case the resource will only be partially assigned up to their bookings.</span></span> <span data-ttu-id="53a61-140">Bạn có thể xem số giờ nhiệm vụ chưa được gán bằng cách thêm cột Số giờ trống vào cấu trúc phân tích công việc.</span><span class="sxs-lookup"><span data-stu-id="53a61-140">You can see these remaining unassigned task hours by adding the Unstaffed Hours column to the work breakdown structure.</span></span>

<span data-ttu-id="53a61-141">Nếu nguồn lực được gán cho số giờ được đăng ký cho nguồn lực (số giờ được đăng ký cho nguồn lực bằng số giờ được gán cho nguồn lực), bạn sẽ thấy thông báo lỗi như sau khi bạn cố gán nguồn lực cho các nhiệm vụ sau:</span><span class="sxs-lookup"><span data-stu-id="53a61-141">If resources are assigned to their booked hours (their booked hours equals their assigned hours), you’ll see the following error message when you attempt to assign them further tasks:</span></span>

<span data-ttu-id="53a61-142">*Không thể gán nguồn lực cho nhiệm vụ - (Các) Nguồn lực sau không có đủ số giờ được đăng ký cho dự án.*</span><span class="sxs-lookup"><span data-stu-id="53a61-142">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project.*</span></span>

<span data-ttu-id="53a61-143">Ngoài ra, thành viên nhóm của người quản lý dự án mặc định mà được thêm vào nhóm khi bạn tạo dự án được thêm mà không có bất kỳ đăng ký nào và không thể được đăng ký cho bất kỳ dự án nào.</span><span class="sxs-lookup"><span data-stu-id="53a61-143">Additionally, the default project manager team member that is added to the team when you create the project is added without any bookings and can’t be assigned to any task.</span></span> <span data-ttu-id="53a61-144">Chúng sẽ không được hiển thị trong danh sách nguồn lực thả xuống cho các nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="53a61-144">They won’t show up in the resource dropdown for tasks.</span></span>

<span data-ttu-id="53a61-145">Nếu bạn muốn gán nguồn lực này, bạn cần loại bỏ chúng khỏi nhóm và sau đó thêm chúng lại bằng phương pháp phân bổ chứ không để là Không có.</span><span class="sxs-lookup"><span data-stu-id="53a61-145">If you want to assign this resource, you need to remove them from the team and then re-add them with an allocation method other than None.</span></span> <span data-ttu-id="53a61-146">Lý do chúng được thêm vào nhóm khi dự án được tạo là để dự án có tối thiểu một người phê chuẩn dự án theo mặc định.</span><span class="sxs-lookup"><span data-stu-id="53a61-146">The reason they’re added to the team when the project is created is so that a project has at least one project approver by default.</span></span>

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a><span data-ttu-id="53a61-147">Tạo một thành viên chung bằng cách phân công vai trò cho nhiệm vụ</span><span class="sxs-lookup"><span data-stu-id="53a61-147">Create a generic team member through role assignment on tasks</span></span>

<span data-ttu-id="53a61-148">Phương pháp này đảm bảo nguồn lực có đủ đăng ký cho nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="53a61-148">This method assures that resources have enough bookings for tasks.</span></span> <span data-ttu-id="53a61-149">Đầu tiên, bạn tạo một nguồn lực chung hoặc nguồn lực giữ chỗ mà mô tả các đặc điểm của nguồn lực được đặt tên, cuối cùng bạn muốn làm việc với nhiệm vụ bằng cách tạo nhóm sau khi gán vai trò cho nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="53a61-149">First, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks by generating a team after assigning roles to tasks.</span></span> <span data-ttu-id="53a61-150">Đây là cách làm việc này:</span><span class="sxs-lookup"><span data-stu-id="53a61-150">Here’s how you do this:</span></span>

1. <span data-ttu-id="53a61-151">Trên cấu trúc phân tích công việc, chọn nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="53a61-151">On the work breakdown structure, select a task.</span></span>
2. <span data-ttu-id="53a61-152">Chọn biểu tượng danh sách thả xuống **Vai trò được gán** trong ô nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="53a61-152">Select the **Assigned Role** dropdown icon in the resource cell.</span></span>
3. <span data-ttu-id="53a61-153">Chọn danh sách thả xuống **Vai trò** và chọn vai trò cho nguồn lực chung.</span><span class="sxs-lookup"><span data-stu-id="53a61-153">Select the **Role** dropdown and select the role for the generic resource.</span></span>
4. <span data-ttu-id="53a61-154">Chọn **OK**.</span><span class="sxs-lookup"><span data-stu-id="53a61-154">Select **OK**.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="53a61-155">![Ảnh chụp màn hình dùng WBS để thêm tài nguyên](media/FAQ-Resources-to-Tasks2-4.png "Ảnh chụp màn hình dùng WBS để thêm tài nguyên")</span><span class="sxs-lookup"><span data-stu-id="53a61-155">![Screenshot of using WBS to add resource](media/FAQ-Resources-to-Tasks2-4.png "Screenshot of using WBS to add resource")</span></span>
 
<span data-ttu-id="53a61-156">Khi bạn hoàn thành việc gán vai trò cho nhiệm vụ trong WBS, chọn **Tạo nhóm dự án**.</span><span class="sxs-lookup"><span data-stu-id="53a61-156">Once you’ve completed assigning roles to the tasks in the WBS, select **Generate Project Team**.</span></span> <span data-ttu-id="53a61-157">Project Service tạo số thành viên nhóm chung tối thiểu dựa trên vai trò, tạo nguồn lực đơn vị tổ chức, và lịch dự án bằng cách tập hợp các phân công nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="53a61-157">Project Service creates the minimum number of generic team members based on the roles, resourcing organization units, and project calendar by aggregating the task assignments.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="53a61-158">![Ảnh chụp màn hình tạo nhóm dự án](media/FAQ-Resources-to-Tasks2-5.png "Ảnh chụp màn hình tạo nhóm dự án")</span><span class="sxs-lookup"><span data-stu-id="53a61-158">![Screenshot of generating project team](media/FAQ-Resources-to-Tasks2-5.png "Screenshot of generating project team")</span></span>
 
<span data-ttu-id="53a61-159">Trên lưới Thành viên nhóm, bạn sẽ thấy các nguồn lực của loại Nguồn lực chung với tên vị trí và vai trò.</span><span class="sxs-lookup"><span data-stu-id="53a61-159">On the Team Member grid, you’ll see resources of the Generic Resource type with the role and position name.</span></span> <span data-ttu-id="53a61-160">Nếu hai nguồn lực cần cho vai trò để hoàn thành công việc, tính năng Tạo nhóm sẽ tạo hai thành viên nhóm và dùng tên vị trí để phân biệt.</span><span class="sxs-lookup"><span data-stu-id="53a61-160">If two resources are needed for a role to complete the work, the Generate Team feature creates two team members and uses position name to set them apart.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="53a61-161">![Ảnh chụp màn hình thêm hai tài nguyên chung](media/FAQ-Resources-to-Tasks2-6.png "Ảnh chụp màn hình thêm hai tài nguyên chung")</span><span class="sxs-lookup"><span data-stu-id="53a61-161">![Screenshot of adding two generic resources](media/FAQ-Resources-to-Tasks2-6.png "Screenshot of adding two generic resources")</span></span>
 
<span data-ttu-id="53a61-162">Bạn có thể mở yêu cầu nguồn lực hỗ trợ cho thành viên nhóm chung bằng cách chon liên kết ở dưới Yêu cầu Nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="53a61-162">You can open the backing resource requirement for the generic team member by selecting the link under Resource Requirement.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="53a61-163">![Ảnh chụp màn hình mở yêu cầu nguồn lực hỗ trợ](media/FAQ-Resources-to-Tasks2-7.png "Ảnh chụp màn hình mở yêu cầu nguồn lực hỗ trợ")</span><span class="sxs-lookup"><span data-stu-id="53a61-163">![Screenshot of opening backing resource requirement](media/FAQ-Resources-to-Tasks2-7.png "Screenshot of opening backing resource requirement")</span></span>

<span data-ttu-id="53a61-164">Chọn **Đăng ký** đối với nguồn lực chung và sau đó bạn có thể dùng bảng lịch trình để tìm và đăng ký nguồn lực thực.</span><span class="sxs-lookup"><span data-stu-id="53a61-164">Select **Book** for the generic resource, and then you can use the schedule board to find and book a real resource.</span></span> <span data-ttu-id="53a61-165">Bạn cũng có thể gửi yêu cầu hoàn thành bởi người quản lý nguồn lực bằng cách chọn **Gửi yêu cầu**.</span><span class="sxs-lookup"><span data-stu-id="53a61-165">You can also submit the requirement for fulfillment by a resource manager by selecting **Submit Request**.</span></span>

<span data-ttu-id="53a61-166">Khi nguồn lực chung được hoàn thành bằng nguồn lực được đặt tên, nguồn lực chung sẽ được loại bỏ khỏi nhóm và các phân công nhiệm vụ cho nguồn lực chung được gán cho nguồn lực được đặt tên mà hoàn thành yêu cầu nguồn lực của nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="53a61-166">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>
 



[!INCLUDE[footer-include](../includes/footer-banner.md)]