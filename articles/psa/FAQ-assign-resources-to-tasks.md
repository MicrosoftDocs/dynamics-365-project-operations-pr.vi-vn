---
title: Chỉ định nguồn lực cho nhiệm vụ
description: Chủ đề này cung cấp thông tin về cách gán tài nguyên cho công việc.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
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
ms.openlocfilehash: 486371df2de8b400f200dbf38e66cb5e2dec7ae7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286274"
---
# <a name="assign-a-resource-to-a-task"></a><span data-ttu-id="d0697-103">Gán nguồn lực cho nhiệm vụ</span><span class="sxs-lookup"><span data-stu-id="d0697-103">Assign a resource to a task</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="d0697-104">Có 3 cách để gán nguồn lực cho một nhiệm vụ trong Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="d0697-104">There are three ways to assign a resource to a task in Microsoft Dynamics 365 Project Service Automation.</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="d0697-105">Đăng ký một nguồn lực là một thành viên nhóm và sau đó gán nguồn lực cho nhiệm vụ</span><span class="sxs-lookup"><span data-stu-id="d0697-105">Book a resource as a team member, and then assign the resource to a task</span></span>

<span data-ttu-id="d0697-106">Bạn có thể thêm nguồn lực vào nhóm dự án và sau đó gán nguồn lực cho nhiệm vụ trong lịch trình dự án.</span><span class="sxs-lookup"><span data-stu-id="d0697-106">You can add a resource to the project team, and then assign the resource to tasks in the project schedule.</span></span>

1. <span data-ttu-id="d0697-107">Trên tab **Thành viên nhóm**, thêm một thành viên nhóm bằng cách chọn **Mới**.</span><span class="sxs-lookup"><span data-stu-id="d0697-107">On the **Team Member** tab, add a new team member by selecting **New**.</span></span> 

2. <span data-ttu-id="d0697-108">Bảng điều khiển **Tạo nhanh Thành viên nhóm** mở ra, ở đây bạn có thể chọn tên nguồn lực có thể đăng ký được và đặt vai trò.</span><span class="sxs-lookup"><span data-stu-id="d0697-108">The **Team Member Quick Create** panel opens, where you can select the bookable resource name and set a role.</span></span> 

    <span data-ttu-id="d0697-109">Chọn một trong các phương pháp phân bổ sau để đăng ký nguồn lực:</span><span class="sxs-lookup"><span data-stu-id="d0697-109">Select one of the following allocation methods for the resource’s booking:</span></span>

    - <span data-ttu-id="d0697-110">**Năng lực đầy đủ** đăng ký năng lực đầy đủ của nguồn lực theo các ngày bắt đầu và kết thúc đã được chỉ định.</span><span class="sxs-lookup"><span data-stu-id="d0697-110">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="d0697-111">**Năng lực tỉ lệ phần trăm** đăng ký nguồn lực theo tỉ lệ phần trăm năng lực của nguồn lực theo những ngày bắt đầu và kết thúc.</span><span class="sxs-lookup"><span data-stu-id="d0697-111">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="d0697-112">**Phân phối theo giờ đồng đều** sẽ đăng ký nguồn lực cho số giờ được chỉ định, phương pháp này phân phối thời gian mỗi ngày đều nhau cho các ngày đã được chỉ định kể từ khi bắt đầu cho tới khi kết thúc.</span><span class="sxs-lookup"><span data-stu-id="d0697-112">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing them evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="d0697-113">**Phân phối không đồng đều** đăng ký nguồn lực cho số giờ được chỉ định, phương pháp này phân phối không đồng đều thời gian cho mỗi ngày trong các ngày được chỉ định từ khi bắt đầu cho tới khi kết thúc.</span><span class="sxs-lookup"><span data-stu-id="d0697-113">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>
    - <span data-ttu-id="d0697-114">Lựa chọn **Không có** sẽ thêm nguồn lực cho nhóm nhưng không tạo bất kỳ đăng kỳ nào mà sử dụng năng lực của nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="d0697-114">**None** adds the resource to the team but doesn’t create any bookings that absorb their capacity.</span></span>

3. <span data-ttu-id="d0697-115">Trên lưới **Lịch trình** cho nhiệm vụ, chọn biểu tượng **Nguồn lực** trong ô nguồn lực, sau đó trong **Thành viên nhóm**, chọn thành viên nhóm bạn vừa mới thêm vào.</span><span class="sxs-lookup"><span data-stu-id="d0697-115">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell, and then under **Team Members**, select the team member you just added.</span></span> 

> [!NOTE]
> <span data-ttu-id="d0697-116">Trên cả tab **Thành viên Nhóm** và **Hợp nhất**, nguồn lực hiển thị số giờ đã được đăng ký và số giờ được gán.</span><span class="sxs-lookup"><span data-stu-id="d0697-116">On the **Team Member** and **Reconciliation** tabs, the resource shows booked and assigned hours.</span></span> <span data-ttu-id="d0697-117">Số giờ nên giống nhau nhưng không bắt buộc vì đặt lịch và phân công không ghép đôi chặt chẽ với nhau.</span><span class="sxs-lookup"><span data-stu-id="d0697-117">The hours should be the same, but it isn't required as bookings and assignments are not tightly coupled.</span></span> <span data-ttu-id="d0697-118">Tab **Hợp nhất** cho bạn chi tiết khi chúng khác nhau, như khi bạn gán cho một nguồn lực số giờ nhiều hơn số giờ mà bạn đã đăng ký.</span><span class="sxs-lookup"><span data-stu-id="d0697-118">The **Reconciliation** tab gives you details when they are different, such as when you assign a resource more hours than you have booked.</span></span> <span data-ttu-id="d0697-119">Nếu cần, bạn có sửa thông tin này bằng cách mở rộng đăng ký của nguồn lực hoặc đổi phân công.</span><span class="sxs-lookup"><span data-stu-id="d0697-119">If needed, you can correct the information by extending the resource's bookings or changing the assignment.</span></span>

## <a name="create-a-generic-team-member-through-task-assignment"></a><span data-ttu-id="d0697-120">Tạo thành viên nhóm chung bằng phân công nhiệm vụ</span><span class="sxs-lookup"><span data-stu-id="d0697-120">Create a generic team member through task assignment</span></span>

<span data-ttu-id="d0697-121">Khi bạn tạo thành viên nhóm chung thông qua chỉ định nhiệm vụ, bạn tạo một nguồn lực chung hoặc nguồn lực giữ chỗ mà mô tả các đặc điểm của nguồn lực được đặt tên, cuối cùng bạn muốn làm việc với nhiệm vụ bằng cách tạo nhóm sau khi gán vai trò cho nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="d0697-121">When you create a generic team member through task assignment, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks.</span></span> <span data-ttu-id="d0697-122">Sau đó bạn tạo một yêu cầu (hoặc gửi một yêu cầu bằng cách sử dụng yêu cầu) mà được dùng để tìm và đăng ký nguồn lực được đặt tên.</span><span class="sxs-lookup"><span data-stu-id="d0697-122">You then generate a requirement (or submit a request using the requirement) that is used to search for and book the named resource.</span></span>

1. <span data-ttu-id="d0697-123">Trên lưới **Lịch trình** cho nhiệm vụ, chọn biểu tượng **Nguồn lực** trong ô nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="d0697-123">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="d0697-124">Nhập một tên để làm tên của nguồn lực đặt chỗ.</span><span class="sxs-lookup"><span data-stu-id="d0697-124">Type a name to serve as the placeholder resource’s name.</span></span> <span data-ttu-id="d0697-125">Ví dụ: Người quản lý Chương trình.</span><span class="sxs-lookup"><span data-stu-id="d0697-125">For example, Program Manager.</span></span>

3. <span data-ttu-id="d0697-126">Chọn **Tạo** và trong trường **Tạo nhanh Thành viên Nhóm Dự án**, đặt vai trò cho nguồn lực chung.</span><span class="sxs-lookup"><span data-stu-id="d0697-126">Select **Create**, and in the **Quick Create Project Team Member** field, set the role for the generic resource.</span></span>

4. <span data-ttu-id="d0697-127">Bạn có thể tiếp tục gán nhiệm vụ cho nguồn lực giữ chỗ này bằng cách chọn nguồn lực trên **Bộ chọn nguồn lực** cho nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="d0697-127">You can continue to assign tasks to this placeholder resource by selecting the resource on the **Resource Selector** for the task.</span></span> <span data-ttu-id="d0697-128">Chúng được liệt kê trong phần **Thành viên Nhóm**.</span><span class="sxs-lookup"><span data-stu-id="d0697-128">They’re listed under **Team Members**.</span></span>

5. <span data-ttu-id="d0697-129">Khi bạn hoàn thành việc gán nguồn lực chung, chọn nguồn lực chung trên tab **Nhóm** và sau đó chọn **Tạo yêu cầu** để tạo yêu cầu nguồn lực cho nguồn lực chung.</span><span class="sxs-lookup"><span data-stu-id="d0697-129">When you’re done assigning the generic resource, select the generic resource on the **Team** tab, and then select **Generate Requirement** to create a resource requirement for the generic resource.</span></span>

6. <span data-ttu-id="d0697-130">Chọn **Đăng ký** cho nguồn lực chung.</span><span class="sxs-lookup"><span data-stu-id="d0697-130">Select **Book** for the generic resource.</span></span> <span data-ttu-id="d0697-131">Sau đó bạn có thể dùng bảng Lịch trình để tìm và đăng ký nguồn lực thực.</span><span class="sxs-lookup"><span data-stu-id="d0697-131">You can then use the Schedule board to find and book a real resource.</span></span> <span data-ttu-id="d0697-132">Bạn cũng có thể gửi yêu cầu để thực hiện bởi người quản lý nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="d0697-132">You can also submit the requirement for fulfillment by a resource manager.</span></span>

7. <span data-ttu-id="d0697-133">Khi nguồn lực chung được hoàn thành bằng nguồn lực được đặt tên, nguồn lực chung sẽ được loại bỏ khỏi nhóm và các phân công nhiệm vụ cho nguồn lực chung được gán cho nguồn lực được đặt tên mà hoàn thành yêu cầu nguồn lực của nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="d0697-133">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a><span data-ttu-id="d0697-134">Gán một nguồn lực được đặt tên từ danh sách tất cả các nguồn lực có thể đăng ký được</span><span class="sxs-lookup"><span data-stu-id="d0697-134">Assign a named resource from the list of all bookable resources</span></span>

<span data-ttu-id="d0697-135">Bạn có thể dùng hộp tìm kiếm trong **Bộ chọn nguồn lực** để tìm tất cả các nguồn lực có thể đăng ký và gán nguồn lực cho nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="d0697-135">You can use the search box in the **Resource Selector** to search all bookable resources and assign them to a task.</span></span>

<span data-ttu-id="d0697-136">Các tài nguyên được chỉ định theo cách này sẽ được thêm vào nhóm mà không có bất kỳ đặt chỗ nào.</span><span class="sxs-lookup"><span data-stu-id="d0697-136">Resources assigned this way are added to the team without any bookings.</span></span> <span data-ttu-id="d0697-137">Điều này tương tự như việc thêm một thành viên trong nhóm và chọn Không có làm phương pháp phân bổ.</span><span class="sxs-lookup"><span data-stu-id="d0697-137">This is similar to adding a team member and selecting None as the allocation method.</span></span> <span data-ttu-id="d0697-138">Nguồn lực được hiển thị trong tab **Nhóm** và tab **Hợp nhất** như là nguồn lực chỉ có phân công còn đặt chỗ bị thâm hụt.</span><span class="sxs-lookup"><span data-stu-id="d0697-138">The resource is displayed in the **Team** and **Reconciliation** tabs as resources with only assignments and a booking deficit.</span></span> <span data-ttu-id="d0697-139">Đăng ký chúng nếu bạn muốn sử dụng tính sẵn có của chúng.</span><span class="sxs-lookup"><span data-stu-id="d0697-139">Book them if you want to use their availability.</span></span>

1. <span data-ttu-id="d0697-140">Trên lưới **Lịch trình** cho nhiệm vụ, chọn biểu tượng **Nguồn lực** trong ô nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="d0697-140">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="d0697-141">Bắt đầu gõ vào một tên.</span><span class="sxs-lookup"><span data-stu-id="d0697-141">Start typing a name.</span></span> <span data-ttu-id="d0697-142">Kết quả tìm kiếm cho tên được hiện thị trong **Bộ chọn nguồn lực** trong phần **Các nguồn lực khác**.</span><span class="sxs-lookup"><span data-stu-id="d0697-142">The search results for the name are displayed in the **Resource Selector** under **Other Resources**.</span></span>

3. <span data-ttu-id="d0697-143">Chọn tài nguyên mà bạn muốn gán cho tác vụ.</span><span class="sxs-lookup"><span data-stu-id="d0697-143">Select the resource that you want to assign to the task.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]