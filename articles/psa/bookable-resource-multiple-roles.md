---
title: Ước tính doanh số và chi phí khi một nguồn lực có thể đăng ký đảm nhận nhiều vai trò của dự án
description: Chủ đề này cung cấp thông tin về cách dùng các chiều giá cả để hỗ trợ ước tính giá và chi phí đối với một nguồn lực đảm nhận nhiều vai trò của dự án.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 0f779cf7e247157d6cae2ae7c4c5644201cb7714
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291015"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-for-a-project"></a><span data-ttu-id="87bcb-103">Ước tính doanh số và chi phí khi một nguồn lực có thể đăng ký đảm nhận nhiều vai trò của dự án</span><span class="sxs-lookup"><span data-stu-id="87bcb-103">Estimate project sales and costs when a bookable resource fills multiple roles for a project</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="87bcb-104">Thông thường, các công ty hoạt động theo dự án sẽ cần có một nguồn lực đảm nhận nhiều vai trò trong một dự án.</span><span class="sxs-lookup"><span data-stu-id="87bcb-104">Project-based companies often have the need for one resource to perform multiple roles on a project.</span></span> <span data-ttu-id="87bcb-105">Mỗi vai trò này có thể được định giá và tính chi phí khác nhau, có nghĩa là thời gian của cùng nguồn lực trong dự án có thể nhận được ước tính tài chính khác nhau tùy thuộc vào hóa đơn và chi phí cho mỗi vai trò.</span><span class="sxs-lookup"><span data-stu-id="87bcb-105">Each of these roles could be priced and costed differently, which means the same resource's time on the project could get a different financial estimate depending on the bill and cost rates for each of the roles.</span></span> <span data-ttu-id="87bcb-106">Project Service Automation cho phép thiết lập các giá trị trên bản ghi thành viên nhóm cho tài nguyên được đặt tên và cho phép các nội dung ghi đè khác nhau đối với từng nhiệm vụ mà thành viên nhóm được phân công.</span><span class="sxs-lookup"><span data-stu-id="87bcb-106">Project Service Automation allows the setup of the values on the team member record for the named resource and allows for different overrides on each of the tasks that the team member is assigned to.</span></span>

<span data-ttu-id="87bcb-107">Ví dụ sau giải thích cách ghi đè đơn giản của giá trị này cho phép một nguồn lực có nhiều vai trò trong dự án với các mức chi phí và hóa đơn khác nhau.</span><span class="sxs-lookup"><span data-stu-id="87bcb-107">The following example  explains how the simple override of this value allows a resource to have multiple roles on a project with different cost and bill rates.</span></span>

## <a name="create-tasks"></a><span data-ttu-id="87bcb-108">Tạo nhiệm vụ</span><span class="sxs-lookup"><span data-stu-id="87bcb-108">Create tasks</span></span>
<span data-ttu-id="87bcb-109">Tạo hai nhiệm vụ dự án, mỗi nhiệm vụ 40 giờ, Nhiệm vụ A và Nhiệm vụ B. Chọn Nhiệm vụ A là nhiệm vụ trước Nhiệm vụ B.</span><span class="sxs-lookup"><span data-stu-id="87bcb-109">Create two project tasks for 40 hours each, Task A and Task B. Select Task A as a predecessor to Task B.</span></span>

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a><span data-ttu-id="87bcb-110">Thiết lập vai trò và đơn vị tổ chức cho một thành viên nhóm dự án chung</span><span class="sxs-lookup"><span data-stu-id="87bcb-110">Set up Role and Organization Unit for a generic project team member</span></span>

1. <span data-ttu-id="87bcb-111">Trên trang **Lịch trình**, chọn hàng **Nhiệm vụ** cho Nhiệm vụ A.</span><span class="sxs-lookup"><span data-stu-id="87bcb-111">On the **Schedule** page, select the **Task** row for Task A.</span></span> 
2. <span data-ttu-id="87bcb-112">Trong trường **Nguồn lực**, chọn **Tạo** trong danh sách thả xuống.</span><span class="sxs-lookup"><span data-stu-id="87bcb-112">In the **Resources** field, select **Create** in the drop-down list.</span></span>
3. <span data-ttu-id="87bcb-113">Trên trang **Tạo nhanh thành viên nhóm**, chỉ định thuộc tính của thành viên nhóm chung có thể thực hiện nhiệm vụ này.</span><span class="sxs-lookup"><span data-stu-id="87bcb-113">On the **Team Member Quick Create** page, specify the attributes of the generic team member who can perform this task.</span></span>
4. <span data-ttu-id="87bcb-114">Chọn vai trò và đơn vị tổ chức thích hợp, sau đó chọn **Lưu và đóng**.</span><span class="sxs-lookup"><span data-stu-id="87bcb-114">Select the appropriate role and organizational unit, and then select **Save and Close**.</span></span> <span data-ttu-id="87bcb-115">Một thành viên nhóm chung được tạo và phân công nhiệm vụ này.</span><span class="sxs-lookup"><span data-stu-id="87bcb-115">A generic team member is created and assigned to this task.</span></span> 

<span data-ttu-id="87bcb-116">Lặp lại các bước này cho Nhiệm vụ B và đảm bảo rằng vai trò và đơn vị tổ chức của thành viên nhóm chung được tạo cho Nhiệm vụ B khác với Nhiệm vụ A.</span><span class="sxs-lookup"><span data-stu-id="87bcb-116">Repeat these steps for Task B and make sure that the role and organizational unit on the generic team member created for Task B is different than Task A.</span></span> 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a><span data-ttu-id="87bcb-117">Thiết lập vai trò và đơn vị tổ chức cho nhiệm vụ dự án</span><span class="sxs-lookup"><span data-stu-id="87bcb-117">Set up role and organization unit for a project task</span></span>

1. <span data-ttu-id="87bcb-118">Sau khi bạn tạo Nhiệm vụ A, hãy chọn nhiệm vụ, sau đó chọn **Chỉnh sửa nhiệm vụ**.</span><span class="sxs-lookup"><span data-stu-id="87bcb-118">After you create Task A, select the task, and then select **Edit task**.</span></span>
2. <span data-ttu-id="87bcb-119">Trên trang **Chi tiết nhiệm vụ**, tìm trường **Vai trò** và **Đơn vị tổ chức**, thêm các giá trị bắt buộc của nguồn lực sẽ thực hiện nhiệm vụ này.</span><span class="sxs-lookup"><span data-stu-id="87bcb-119">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="87bcb-120">Nếu bạn đang hoàn thành kịch bản này bằng cách sử dụng dữ liệu demo Project Service Automation, hãy chọn **Trưởng nhóm tư vấn** cho vai trò và **Fabrikam US** là đơn vị tổ chức.</span><span class="sxs-lookup"><span data-stu-id="87bcb-120">If you are completing this scenarios using Project Service Automation demo data, select **Consulting Lead** for the role, and **Fabrikam US** as the organizational unit.</span></span>

3. <span data-ttu-id="87bcb-121">Chọn Nhiệm vụ B và sau đó chọn **Chỉnh sửa nhiệm vụ**.</span><span class="sxs-lookup"><span data-stu-id="87bcb-121">Select Task B and then select **Edit task**.</span></span>
4. <span data-ttu-id="87bcb-122">Trên trang **Chi tiết nhiệm vụ**, tìm trường **Vai trò** và **Đơn vị tổ chức**, thêm các giá trị bắt buộc của nguồn lực sẽ thực hiện nhiệm vụ này.</span><span class="sxs-lookup"><span data-stu-id="87bcb-122">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> <span data-ttu-id="87bcb-123">Đảm bảo rằng các giá trị trong trường **Vai trò** và **Đơn vị tổ chức** của Nhiệm vụ B khác với các giá trị của Nhiệm vụ A.</span><span class="sxs-lookup"><span data-stu-id="87bcb-123">Make sure that the values in the **Role** and **Organizational Unit** fields are different for Task B from the values for Task A.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="87bcb-124">Nếu bạn đang hoàn thành kịch bản này bằng cách sử dụng dữ liệu demo Project Service Automation, hãy chọn **Kỹ thuật viên mạng** cho vai trò và **Fabrikam US** là đơn vị tổ chức.</span><span class="sxs-lookup"><span data-stu-id="87bcb-124">If you are completing this scenarios using Project Service Automation demo data, select **Network Technician** for the role, and **Fabrikam US** as the organizational unit.</span></span>

5. <span data-ttu-id="87bcb-125">Lưu và đóng trang **Chi tiết nhiệm vụ**.</span><span class="sxs-lookup"><span data-stu-id="87bcb-125">Save and close the **Task Details** page.</span></span> 

## <a name="team-member-and-estimates-behavior"></a><span data-ttu-id="87bcb-126">Hành vi thành viên nhóm và giá trị ước tính</span><span class="sxs-lookup"><span data-stu-id="87bcb-126">Team member and estimates behavior</span></span> 

1. <span data-ttu-id="87bcb-127">Trên trang **Chi tiết nhiệm vụ**, trên **Thành viên nhóm**, chọn hai Thành viên nhóm rồi chọn **Tạo yêu cầu**.</span><span class="sxs-lookup"><span data-stu-id="87bcb-127">On the **Task Details** page, on the **Team Member**, select the two generic team Members and then select **Generate Requirements**.</span></span> 
2. <span data-ttu-id="87bcb-128">Chọn hàng thành viên nhóm cho **Trưởng nhóm tư vấn** rồi chọn **Đặt trước**.</span><span class="sxs-lookup"><span data-stu-id="87bcb-128">Select the team member row for **Consulting Lead** and then select **Book**.</span></span> <span data-ttu-id="87bcb-129">Bảng lịch trình mở ra và đặt trước một nguồn lực cho yêu cầu đó.</span><span class="sxs-lookup"><span data-stu-id="87bcb-129">The schedule board opens and books a resource to that requirement.</span></span>
3. <span data-ttu-id="87bcb-130">Chọn hàng thành viên nhóm cho **Kỹ thuật viên mạng** rồi chọn **Đặt trước**.</span><span class="sxs-lookup"><span data-stu-id="87bcb-130">Select the team member row for **Network Technician** and the select **Book**.</span></span> <span data-ttu-id="87bcb-131">Bảng lịch trình mở ra và đặt trước cùng nguồn lực cho yêu cầu đó.</span><span class="sxs-lookup"><span data-stu-id="87bcb-131">The schedule board opens and books the same resource on that requirement.</span></span>

### <a name="team-member-grid"></a><span data-ttu-id="87bcb-132">Lưới Thành viên nhóm</span><span class="sxs-lookup"><span data-stu-id="87bcb-132">Team Member grid</span></span> 
<span data-ttu-id="87bcb-133">Trên lưới **Thành viên nhóm**, hãy lưu ý rằng có 2 bản ghi thành viên nhóm chung bị xóa và được thay thế bằng một nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="87bcb-133">On the **Team Member** grid, notice that the two generic team member records are deleted and have been replaced one resource.</span></span> <span data-ttu-id="87bcb-134">Có một bộ giá trị cho nguồn lực đó cho thấy bộ giá trị mặc định cho **Vai trò** và **Đơn vị tổ chức**.</span><span class="sxs-lookup"><span data-stu-id="87bcb-134">There is one set of values for that resource that shows a default set of values for **Role** and **Organizational Unit**.</span></span>
<span data-ttu-id="87bcb-135">Khi bạn mở rộng hàng của bản ghi Thành viên nhóm đó, bạn có thể thấy các nhiệm vụ riêng biệt trên bản ghi thành viên nhóm cho cả hai nhiệm vụ đó.</span><span class="sxs-lookup"><span data-stu-id="87bcb-135">When you expand the row of that Team Member record, you can see distinct assignments on the team member record for both of those tasks.</span></span> <span data-ttu-id="87bcb-136">Mỗi hàng phân công có các giá trị cụ thể cho nhiệm vụ đối với **Vai trò** và **Đơn vị tổ chức**.</span><span class="sxs-lookup"><span data-stu-id="87bcb-136">Each assignment row has task-specific values for **Role** and **Organizational Unit**.</span></span> 

### <a name="estimates-grid"></a><span data-ttu-id="87bcb-137">Lưới ước tính</span><span class="sxs-lookup"><span data-stu-id="87bcb-137">Estimates grid</span></span> 
<span data-ttu-id="87bcb-138">Khi bạn điều hướng đến lưới **Ước tính**, bạn sẽ nhận thấy rằng cả hai mục phân công cho cùng một nguồn lực có giá khác nhau.</span><span class="sxs-lookup"><span data-stu-id="87bcb-138">When you navigate to the **Estimates** grid, you will notice that both assignments for the same resource are priced differently.</span></span>
<span data-ttu-id="87bcb-139">Việc phân công nguồn lực trong Nhiệm vụ A được định giá bằng giá trị thuộc tính **Vai trò** của **Trưởng nhóm tư vấn**.</span><span class="sxs-lookup"><span data-stu-id="87bcb-139">The assignment for the resource on Task A is priced using the **Role** attribute value of **Consulting Lead**.</span></span> <span data-ttu-id="87bcb-140">Việc phân công nguồn lực đó trong Nhiệm vụ B được định giá bằng giá trị thuộc tính **Vai trò** của **Kỹ thuật viên mạng**.</span><span class="sxs-lookup"><span data-stu-id="87bcb-140">The assignment for the same resource on Task B is priced using the **Role** attribute value of **Network Technician**.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]