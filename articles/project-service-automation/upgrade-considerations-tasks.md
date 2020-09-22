---
title: Nâng cấp thông tin cân nhắc cho cấu trúc phân tích công việc
description: Chủ đề này cung cấp thông tin về cách nâng cấp cấu trúc phân tích công việc từ Project Service Automation 2.x lên 3.x.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 2.x
author: ruhercul
ms.assetid: 9e43d5b5-ca5d-41f5-9012-c48f8e3080f9
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 9aa35dd8784bfa55737b0836e653afd0442b80c2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 03/24/2020
ms.locfileid: "3757092"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a><span data-ttu-id="34c8f-103">Nâng cấp thông tin cân nhắc cho cấu trúc phân tích công việc</span><span class="sxs-lookup"><span data-stu-id="34c8f-103">Upgrade considerations for the work breakdown structure</span></span>
<span data-ttu-id="34c8f-104">Chủ đề này cung cấp thông tin về cách nâng cấp cấu trúc phân tích công việc từ Project Service Automation 2.x lên 3.x.</span><span class="sxs-lookup"><span data-stu-id="34c8f-104">This topic provides information about upgrading the work breakdown structure from Project Service Automation 2.x to 3.x.</span></span> <span data-ttu-id="34c8f-105">Chủ đề này xác định trạng thái ổn định của một dự án trong Project Service Automation (PSA) được yêu cầu để nâng cấp thành công.</span><span class="sxs-lookup"><span data-stu-id="34c8f-105">This topic defines the healthy state of a project in Project Service Automation (PSA) that is required for a successful upgrade.</span></span> <span data-ttu-id="34c8f-106">Cũng có thông tin về các điều kiện chặn phổ biến sẽ khiến không nâng cấp được.</span><span class="sxs-lookup"><span data-stu-id="34c8f-106">There is also information about the common blocking conditions that will cause upgrade to fail.</span></span> <span data-ttu-id="34c8f-107">Để biết thêm thông tin về cách xác định nhiệm vụ dự án và các chức năng trong lịch trình dự án, hãy xem [Lịch biểu dự án](project-creating.md).</span><span class="sxs-lookup"><span data-stu-id="34c8f-107">For more information about defining project tasks and their functions within a project schedule, see [Project schedules](project-creating.md).</span></span>

## <a name="key-entities"></a><span data-ttu-id="34c8f-108">Các thực thể chính</span><span class="sxs-lookup"><span data-stu-id="34c8f-108">Key entities</span></span>
<span data-ttu-id="34c8f-109">Đối với một cấu trúc phân tích công việc chính xác đã được tải với các nguồn lực, cần có các thực thể sau:</span><span class="sxs-lookup"><span data-stu-id="34c8f-109">For an accurate work breakdown structure that is already loaded with resources, the following entities are required:</span></span>

- [<span data-ttu-id="34c8f-110">Dự án</span><span class="sxs-lookup"><span data-stu-id="34c8f-110">Project</span></span>](../developer/entities/msdyn_project.md)
- [<span data-ttu-id="34c8f-111">Nhóm Dự án</span><span class="sxs-lookup"><span data-stu-id="34c8f-111">Project Team</span></span>](../developer/entities/msdyn_projectteam.md)
- [<span data-ttu-id="34c8f-112">Nhiệm vụ Dự án</span><span class="sxs-lookup"><span data-stu-id="34c8f-112">Project Task</span></span>](../developer/entities/msdyn_projecttask.md)
- [<span data-ttu-id="34c8f-113">Gán Nguồn lực</span><span class="sxs-lookup"><span data-stu-id="34c8f-113">Resource Assignments</span></span>](../developer/entities/msdyn_resourceassignment.md)
- [<span data-ttu-id="34c8f-114">Quan hệ phụ thuộc Nhiệm vụ Dự án</span><span class="sxs-lookup"><span data-stu-id="34c8f-114">Project Task Dependency</span></span>](../developer/entities/msdyn_projecttaskdependency.md)
- [<span data-ttu-id="34c8f-115">Nguồn lực có thể đặt trước</span><span class="sxs-lookup"><span data-stu-id="34c8f-115">Bookable Resources</span></span>](../developer/entities/bookableresource.md)

<span data-ttu-id="34c8f-116">Để xác định cấu trúc phân tích công việc tải nguồn lực, bạn phải hoàn thành các bước sau:</span><span class="sxs-lookup"><span data-stu-id="34c8f-116">To define a resource loaded work breakdown structure, you must complete the following steps:</span></span>

1. <span data-ttu-id="34c8f-117">Tạo dự án mới.</span><span class="sxs-lookup"><span data-stu-id="34c8f-117">Create a new project.</span></span> <span data-ttu-id="34c8f-118">Để biết thêm thông tin về cách tạo dự án mới, hãy xem [msdyn_project](../developer/entities/msdyn_project.md).</span><span class="sxs-lookup"><span data-stu-id="34c8f-118">For more information about how to create a new project, see [msdyn_project](../developer/entities/msdyn_project.md).</span></span>
2. <span data-ttu-id="34c8f-119">Tạo một hoặc nhiều nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="34c8f-119">Create one or more tasks.</span></span> <span data-ttu-id="34c8f-120">Để biết thêm thông tin về cách tạo nhiệm vụ, hãy xem [msdyn_projecttask](../developer/entities/msdyn_projecttask.md).</span><span class="sxs-lookup"><span data-stu-id="34c8f-120">For more information about how to create a task, see [msdyn_projecttask](../developer/entities/msdyn_projecttask.md).</span></span>
3. <span data-ttu-id="34c8f-121">Xác định các yếu tố phụ thuộc nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="34c8f-121">Define the task dependencies.</span></span> <span data-ttu-id="34c8f-122">Để biết thêm thông tin, hãy xem [Quan hệ phụ thuộc nhiệm vụ dự án](../developer/entities/msdyn_projecttaskdependency.md).</span><span class="sxs-lookup"><span data-stu-id="34c8f-122">For more information, see [Project Task Dependency](../developer/entities/msdyn_projecttaskdependency.md).</span></span>
4. <span data-ttu-id="34c8f-123">Chỉ định thành viên nhóm dự án vào dự án.</span><span class="sxs-lookup"><span data-stu-id="34c8f-123">Assign project team members to the project.</span></span> <span data-ttu-id="34c8f-124">Để biết thêm thông tin, hãy xem [msdyn_projectteam](../developer/entities/msdyn_projectteam.md).</span><span class="sxs-lookup"><span data-stu-id="34c8f-124">For more information, see [msdyn_projectteam](../developer/entities/msdyn_projectteam.md).</span></span>
5. <span data-ttu-id="34c8f-125">Chỉ định thành viên nhóm dự án vào nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="34c8f-125">Assign project team members to the tasks.</span></span> <span data-ttu-id="34c8f-126">Để biết thêm thông tin, hãy xem [msdyn_resourceassignment](../developer/entities/msdyn_resourceassignment.md).</span><span class="sxs-lookup"><span data-stu-id="34c8f-126">For more information, see [msdyn_resourceassignment](../developer/entities/msdyn_resourceassignment.md).</span></span>

## <a name="project-team-relationships"></a><span data-ttu-id="34c8f-127">Mối quan hệ của nhóm dự án</span><span class="sxs-lookup"><span data-stu-id="34c8f-127">Project team relationships</span></span>

<span data-ttu-id="34c8f-128">Để đảm bảo nâng cấp thành công, phải duy trì chính xác các mối quan hệ sau:</span><span class="sxs-lookup"><span data-stu-id="34c8f-128">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>
- <span data-ttu-id="34c8f-129">Tất cả thành viên nhóm dự án phải liên kết với một nguồn lực có thể đặt trước.</span><span class="sxs-lookup"><span data-stu-id="34c8f-129">All project team members must be associated with a bookable resource.</span></span>
- <span data-ttu-id="34c8f-130">Tất cả thành viên nhóm dự án phải liên kết với cùng một dự án.</span><span class="sxs-lookup"><span data-stu-id="34c8f-130">All project team members must be associated with the same project.</span></span> 

## <a name="project-task-relationships"></a><span data-ttu-id="34c8f-131">Mối quan hệ của nhiệm vụ dự án</span><span class="sxs-lookup"><span data-stu-id="34c8f-131">Project task relationships</span></span>
<span data-ttu-id="34c8f-132">Để đảm bảo nâng cấp thành công, phải duy trì chính xác các mối quan hệ sau:</span><span class="sxs-lookup"><span data-stu-id="34c8f-132">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="34c8f-133">Mọi nhiệm vụ liên quan phải được liên kết với cùng một dự án.</span><span class="sxs-lookup"><span data-stu-id="34c8f-133">Any related tasks must be associated with the same project.</span></span>
- <span data-ttu-id="34c8f-134">Mọi nhiệm vụ dòng phải có một nhiệm vụ chính.</span><span class="sxs-lookup"><span data-stu-id="34c8f-134">Every line task must have a parent task.</span></span>
- <span data-ttu-id="34c8f-135">Mọi nhiệm vụ phải có một dự án chính.</span><span class="sxs-lookup"><span data-stu-id="34c8f-135">Every task must have a parent project.</span></span>

### <a name="valid-conditions"></a><span data-ttu-id="34c8f-136">Điều kiện hợp lệ</span><span class="sxs-lookup"><span data-stu-id="34c8f-136">Valid conditions</span></span>

- <span data-ttu-id="34c8f-137">Tất cả các khoảng thời gian nhiệm vụ phải lớn hơn hoặc bằng (>=) một giờ và nhỏ hơn 1.800.000 phút (1.250 ngày).\*</span><span class="sxs-lookup"><span data-stu-id="34c8f-137">All task durations must be greater than or equal to (>=) one hour and less than 1,800,000 minutes (1,250 days).\*</span></span>
- <span data-ttu-id="34c8f-138">Tất cả các nhiệm vụ phải có ngày bắt đầu không sớm hơn 2000/01/01.\*</span><span class="sxs-lookup"><span data-stu-id="34c8f-138">All tasks must have a start date no earlier than 2000/01/01.\*</span></span>
- <span data-ttu-id="34c8f-139">Tất cả các nhiệm vụ phải có ngày bắt đầu không muộn hơn 17 năm kể từ ngày hiện tại.\*</span><span class="sxs-lookup"><span data-stu-id="34c8f-139">All tasks must have a start date no later than 17 years from the present day.\*</span></span>
- <span data-ttu-id="34c8f-140">Tất cả các nhiệm vụ phải có ngày bắt đầu sớm hơn hoặc bằng với ngày kết thúc.</span><span class="sxs-lookup"><span data-stu-id="34c8f-140">All tasks must have a start date earlier or equal to their finish date.</span></span>
- <span data-ttu-id="34c8f-141">Tất cả các loại giao dịch về phân loại (Chi phí, tài liệu, thuế và thời gian) phải có giá trị **Đơn vị mặc định** và **Nhóm đơn vị**.</span><span class="sxs-lookup"><span data-stu-id="34c8f-141">All transaction types on classifications (Expense, Material, Tax, and Time) must have values for **Default Unit** and **Unit Group**.</span></span>
- <span data-ttu-id="34c8f-142">Phải tránh các định dạng ngày có chữ cái.</span><span class="sxs-lookup"><span data-stu-id="34c8f-142">Date formats with letters should be avoided.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="34c8f-143">Các bước giảm nhẹ có thể áp dụng</span><span class="sxs-lookup"><span data-stu-id="34c8f-143">Potential mitigation steps</span></span>
- <span data-ttu-id="34c8f-144">Sử dụng Tìm kiếm nâng cao để xác định các nhiệm vụ Dự án không chứa ID dự án.</span><span class="sxs-lookup"><span data-stu-id="34c8f-144">Use Advanced Find to identify Project tasks that do not contain a Project ID.</span></span>
- <span data-ttu-id="34c8f-145">Sử dụng Tìm kiếm nâng cao để xác định các nhiệm vụ Dự án trong đó thời lượng dự kiến lớn hơn > 1.800.000.</span><span class="sxs-lookup"><span data-stu-id="34c8f-145">Use Advanced Find to identify Project tasks where the scheduled duration is greater than > 1,800,000.</span></span>
- <span data-ttu-id="34c8f-146">Trước khi thực hiện bất kỳ thay đổi dữ liệu nào, bạn nên điều tra mọi tùy chỉnh liên quan đến thực thể có thể dẫn đến việc đưa dữ liệu vào trạng thái xấu.</span><span class="sxs-lookup"><span data-stu-id="34c8f-146">Prior to making any data changes, you should investigate any customizations associated with the entity that may have led to getting the data into a bad state.</span></span> <span data-ttu-id="34c8f-147">Các tùy chỉnh này phải được xử lý trước khi tiến hành bất kỳ cập nhật nào liên quan đến dữ liệu.</span><span class="sxs-lookup"><span data-stu-id="34c8f-147">These customizations should be addressed before proceeding with any data-related updates.</span></span>
- <span data-ttu-id="34c8f-148">Đối với các nhiệm vụ đã xác định bị bỏ, hãy xem xét xóa các nhiệm vụ này nếu chúng không cần thiết hoặc nếu chúng cần được liên kết với dự án mẹ chính xác.</span><span class="sxs-lookup"><span data-stu-id="34c8f-148">For the identified tasks that have been orphaned, consider deleting these tasks if they are not needed or if they should be associated with the correct parent project.</span></span>
- <span data-ttu-id="34c8f-149">Đối với bất kỳ nhiệm vụ nào có thời lượng lớn hơn 1.250 ngày, hãy xem xét thêm nhiều nhiệm vụ để thể hiện tổng thời lượng, nếu khả thi.</span><span class="sxs-lookup"><span data-stu-id="34c8f-149">For any tasks where the duration is greater than 1,250 days, consider adding multiple tasks to represent the total duration, if feasible.</span></span>

> [!NOTE]
> <span data-ttu-id="34c8f-150">Các mục được ghi chú với dấu hoa thị (\*) có giới hạn do thực tế là công cụ quản lý quan hệ khách hàng (CRM) chỉ hỗ trợ mở rộng 7.320 lần xuất hiện lại.</span><span class="sxs-lookup"><span data-stu-id="34c8f-150">Items noted with an asterisk (\*) have limits that are due to the fact that customer relationship management (CRM) supports only 7,320 recurrence expansions.</span></span> <span data-ttu-id="34c8f-151">Bạn phải ở dưới giới hạn này.</span><span class="sxs-lookup"><span data-stu-id="34c8f-151">You must stay below this limit.</span></span>

## <a name="resource-assignment-relationships"></a><span data-ttu-id="34c8f-152">Mối quan hệ Gán nguồn lực</span><span class="sxs-lookup"><span data-stu-id="34c8f-152">Resource Assignment relationships</span></span>
<span data-ttu-id="34c8f-153">Để đảm bảo nâng cấp thành công, phải duy trì chính xác các mối quan hệ sau:</span><span class="sxs-lookup"><span data-stu-id="34c8f-153">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="34c8f-154">Tất cả Gán nguồn lực trong cấu trúc phân tích công việc phải liên quan đến cùng một dự án.</span><span class="sxs-lookup"><span data-stu-id="34c8f-154">All Resource Assignments in a work breakdown structure must be related to the same project.</span></span>
- <span data-ttu-id="34c8f-155">Tất cả Gán nguồn lực trong cấu trúc phân tích công việc phải liên quan đến các thành viên nhóm dự án trong cùng một dự án.</span><span class="sxs-lookup"><span data-stu-id="34c8f-155">All Resource Assignments in a work breakdown structure must be associated to project team members in the same project.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="34c8f-156">Các bước giảm nhẹ có thể áp dụng</span><span class="sxs-lookup"><span data-stu-id="34c8f-156">Potential mitigation steps</span></span>
- <span data-ttu-id="34c8f-157">Xác định tất cả các nhiệm vụ nằm ngoài các điều kiện được mô tả ở trên.</span><span class="sxs-lookup"><span data-stu-id="34c8f-157">Identify all tasks that fall outside the conditions described above.</span></span>  
- <span data-ttu-id="34c8f-158">Bất kỳ Gán nguồn lực nào không còn hiệu lực sẽ bị xóa.</span><span class="sxs-lookup"><span data-stu-id="34c8f-158">Any Resource Assignments that are no longer valid should be deleted.</span></span>

## <a name="project-task-dependency-relationships"></a><span data-ttu-id="34c8f-159">Mối quan hệ phụ thuộc của nhiệm vụ dự án</span><span class="sxs-lookup"><span data-stu-id="34c8f-159">Project task dependency relationships</span></span>
<span data-ttu-id="34c8f-160">Để đảm bảo nâng cấp thành công, phải duy trì chính xác các mối quan hệ sau:</span><span class="sxs-lookup"><span data-stu-id="34c8f-160">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="34c8f-161">Tất cả yếu tố phụ thuộc nhiệm vụ dự án phải liên quan đến cùng một dự án.</span><span class="sxs-lookup"><span data-stu-id="34c8f-161">All project task dependencies must be related to the same project.</span></span>
- <span data-ttu-id="34c8f-162">Trong một nhiệm vụ, không được tham chiếu cùng một yếu tố phụ thuộc nhiều hơn một lần.</span><span class="sxs-lookup"><span data-stu-id="34c8f-162">A task can't have the same dependency referenced more than once.</span></span>
