---
title: Nâng cấp thông tin cân nhắc cho cấu trúc phân tích công việc
description: Chủ đề này cung cấp thông tin về cách nâng cấp cấu trúc phân tích công việc từ Project Service Automation 2.x lên 3.x.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
author: ruhercul
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
ms.openlocfilehash: a067521410f0fe0d8f5d4c510a35f2a3b018dce3
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281774"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a><span data-ttu-id="f0612-103">Nâng cấp thông tin cân nhắc cho cấu trúc phân tích công việc</span><span class="sxs-lookup"><span data-stu-id="f0612-103">Upgrade considerations for the work breakdown structure</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="f0612-104">Chủ đề này cung cấp thông tin về cách nâng cấp cấu trúc phân tích công việc từ Project Service Automation 2.x lên 3.x.</span><span class="sxs-lookup"><span data-stu-id="f0612-104">This topic provides information about upgrading the work breakdown structure from Project Service Automation 2.x to 3.x.</span></span> <span data-ttu-id="f0612-105">Chủ đề này xác định trạng thái ổn định của một dự án trong Project Service Automation (PSA) được yêu cầu để nâng cấp thành công.</span><span class="sxs-lookup"><span data-stu-id="f0612-105">This topic defines the healthy state of a project in Project Service Automation (PSA) that is required for a successful upgrade.</span></span> <span data-ttu-id="f0612-106">Cũng có thông tin về các điều kiện chặn phổ biến sẽ khiến không nâng cấp được.</span><span class="sxs-lookup"><span data-stu-id="f0612-106">There is also information about the common blocking conditions that will cause upgrade to fail.</span></span> <span data-ttu-id="f0612-107">Để biết thêm thông tin về cách xác định nhiệm vụ dự án và các chức năng trong lịch trình dự án, hãy xem [Lịch biểu dự án](project-creating.md).</span><span class="sxs-lookup"><span data-stu-id="f0612-107">For more information about defining project tasks and their functions within a project schedule, see [Project schedules](project-creating.md).</span></span>

## <a name="key-entities"></a><span data-ttu-id="f0612-108">Các thực thể chính</span><span class="sxs-lookup"><span data-stu-id="f0612-108">Key entities</span></span>
<span data-ttu-id="f0612-109">Đối với một cấu trúc phân tích công việc chính xác đã được tải với các nguồn lực, cần có các thực thể sau:</span><span class="sxs-lookup"><span data-stu-id="f0612-109">For an accurate work breakdown structure that is already loaded with resources, the following entities are required:</span></span>

- [<span data-ttu-id="f0612-110">Dự án</span><span class="sxs-lookup"><span data-stu-id="f0612-110">Project</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [<span data-ttu-id="f0612-111">Nhóm Dự án</span><span class="sxs-lookup"><span data-stu-id="f0612-111">Project Team</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [<span data-ttu-id="f0612-112">Nhiệm vụ Dự án</span><span class="sxs-lookup"><span data-stu-id="f0612-112">Project Task</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [<span data-ttu-id="f0612-113">Gán Nguồn lực</span><span class="sxs-lookup"><span data-stu-id="f0612-113">Resource Assignments</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [<span data-ttu-id="f0612-114">Quan hệ phụ thuộc Nhiệm vụ Dự án</span><span class="sxs-lookup"><span data-stu-id="f0612-114">Project Task Dependency</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [<span data-ttu-id="f0612-115">Nguồn lực có thể đặt trước</span><span class="sxs-lookup"><span data-stu-id="f0612-115">Bookable Resources</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

<span data-ttu-id="f0612-116">Để xác định cấu trúc phân tích công việc tải nguồn lực, bạn phải hoàn thành các bước sau:</span><span class="sxs-lookup"><span data-stu-id="f0612-116">To define a resource loaded work breakdown structure, you must complete the following steps:</span></span>

1. <span data-ttu-id="f0612-117">Tạo dự án mới.</span><span class="sxs-lookup"><span data-stu-id="f0612-117">Create a new project.</span></span> <span data-ttu-id="f0612-118">Để biết thêm thông tin về cách tạo dự án mới, hãy xem [msdyn_project](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).</span><span class="sxs-lookup"><span data-stu-id="f0612-118">For more information about how to create a new project, see [msdyn_project](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).</span></span>
2. <span data-ttu-id="f0612-119">Tạo một hoặc nhiều nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="f0612-119">Create one or more tasks.</span></span> <span data-ttu-id="f0612-120">Để biết thêm thông tin về cách tạo nhiệm vụ, hãy xem [msdyn_projecttask](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).</span><span class="sxs-lookup"><span data-stu-id="f0612-120">For more information about how to create a task, see [msdyn_projecttask](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).</span></span>
3. <span data-ttu-id="f0612-121">Xác định các yếu tố phụ thuộc nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="f0612-121">Define the task dependencies.</span></span> <span data-ttu-id="f0612-122">Để biết thêm thông tin, hãy xem [Quan hệ phụ thuộc nhiệm vụ dự án](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).</span><span class="sxs-lookup"><span data-stu-id="f0612-122">For more information, see [Project Task Dependency](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).</span></span>
4. <span data-ttu-id="f0612-123">Chỉ định thành viên nhóm dự án vào dự án.</span><span class="sxs-lookup"><span data-stu-id="f0612-123">Assign project team members to the project.</span></span> <span data-ttu-id="f0612-124">Để biết thêm thông tin, hãy xem [msdyn_projectteam](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).</span><span class="sxs-lookup"><span data-stu-id="f0612-124">For more information, see [msdyn_projectteam](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).</span></span>
5. <span data-ttu-id="f0612-125">Chỉ định thành viên nhóm dự án vào nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="f0612-125">Assign project team members to the tasks.</span></span> <span data-ttu-id="f0612-126">Để biết thêm thông tin, hãy xem [msdyn_resourceassignment](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).</span><span class="sxs-lookup"><span data-stu-id="f0612-126">For more information, see [msdyn_resourceassignment](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).</span></span>

## <a name="project-team-relationships"></a><span data-ttu-id="f0612-127">Mối quan hệ của nhóm dự án</span><span class="sxs-lookup"><span data-stu-id="f0612-127">Project team relationships</span></span>

<span data-ttu-id="f0612-128">Để đảm bảo nâng cấp thành công, phải duy trì chính xác các mối quan hệ sau:</span><span class="sxs-lookup"><span data-stu-id="f0612-128">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>
- <span data-ttu-id="f0612-129">Tất cả thành viên nhóm dự án phải liên kết với một nguồn lực có thể đặt trước.</span><span class="sxs-lookup"><span data-stu-id="f0612-129">All project team members must be associated with a bookable resource.</span></span>
- <span data-ttu-id="f0612-130">Tất cả thành viên nhóm dự án phải liên kết với cùng một dự án.</span><span class="sxs-lookup"><span data-stu-id="f0612-130">All project team members must be associated with the same project.</span></span> 

## <a name="project-task-relationships"></a><span data-ttu-id="f0612-131">Mối quan hệ của nhiệm vụ dự án</span><span class="sxs-lookup"><span data-stu-id="f0612-131">Project task relationships</span></span>
<span data-ttu-id="f0612-132">Để đảm bảo nâng cấp thành công, phải duy trì chính xác các mối quan hệ sau:</span><span class="sxs-lookup"><span data-stu-id="f0612-132">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="f0612-133">Mọi nhiệm vụ liên quan phải được liên kết với cùng một dự án.</span><span class="sxs-lookup"><span data-stu-id="f0612-133">Any related tasks must be associated with the same project.</span></span>
- <span data-ttu-id="f0612-134">Mọi nhiệm vụ dòng phải có một nhiệm vụ chính.</span><span class="sxs-lookup"><span data-stu-id="f0612-134">Every line task must have a parent task.</span></span>
- <span data-ttu-id="f0612-135">Mọi nhiệm vụ phải có một dự án chính.</span><span class="sxs-lookup"><span data-stu-id="f0612-135">Every task must have a parent project.</span></span>

### <a name="valid-conditions"></a><span data-ttu-id="f0612-136">Điều kiện hợp lệ</span><span class="sxs-lookup"><span data-stu-id="f0612-136">Valid conditions</span></span>

- <span data-ttu-id="f0612-137">Tất cả các khoảng thời gian nhiệm vụ phải lớn hơn hoặc bằng (>=) một giờ và nhỏ hơn 1.800.000 phút (1.250 ngày).\*</span><span class="sxs-lookup"><span data-stu-id="f0612-137">All task durations must be greater than or equal to (>=) one hour and less than 1,800,000 minutes (1,250 days).\*</span></span>
- <span data-ttu-id="f0612-138">Tất cả các nhiệm vụ phải có ngày bắt đầu không sớm hơn 2000/01/01.\*</span><span class="sxs-lookup"><span data-stu-id="f0612-138">All tasks must have a start date no earlier than 2000/01/01.\*</span></span>
- <span data-ttu-id="f0612-139">Tất cả các nhiệm vụ phải có ngày bắt đầu không muộn hơn 17 năm kể từ ngày hiện tại.\*</span><span class="sxs-lookup"><span data-stu-id="f0612-139">All tasks must have a start date no later than 17 years from the present day.\*</span></span>
- <span data-ttu-id="f0612-140">Tất cả các nhiệm vụ phải có ngày bắt đầu sớm hơn hoặc bằng với ngày kết thúc.</span><span class="sxs-lookup"><span data-stu-id="f0612-140">All tasks must have a start date earlier or equal to their finish date.</span></span>
- <span data-ttu-id="f0612-141">Tất cả các loại giao dịch về phân loại (Chi phí, tài liệu, thuế và thời gian) phải có giá trị **Đơn vị mặc định** và **Nhóm đơn vị**.</span><span class="sxs-lookup"><span data-stu-id="f0612-141">All transaction types on classifications (Expense, Material, Tax, and Time) must have values for **Default Unit** and **Unit Group**.</span></span>
- <span data-ttu-id="f0612-142">Phải tránh các định dạng ngày có chữ cái.</span><span class="sxs-lookup"><span data-stu-id="f0612-142">Date formats with letters should be avoided.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="f0612-143">Các bước giảm nhẹ có thể áp dụng</span><span class="sxs-lookup"><span data-stu-id="f0612-143">Potential mitigation steps</span></span>
- <span data-ttu-id="f0612-144">Sử dụng Tìm kiếm nâng cao để xác định các nhiệm vụ Dự án không chứa ID dự án.</span><span class="sxs-lookup"><span data-stu-id="f0612-144">Use Advanced Find to identify Project tasks that do not contain a Project ID.</span></span>
- <span data-ttu-id="f0612-145">Sử dụng Tìm kiếm nâng cao để xác định các nhiệm vụ Dự án trong đó thời lượng dự kiến lớn hơn > 1.800.000.</span><span class="sxs-lookup"><span data-stu-id="f0612-145">Use Advanced Find to identify Project tasks where the scheduled duration is greater than > 1,800,000.</span></span>
- <span data-ttu-id="f0612-146">Trước khi thực hiện bất kỳ thay đổi dữ liệu nào, bạn nên điều tra mọi tùy chỉnh liên quan đến thực thể có thể dẫn đến việc đưa dữ liệu vào trạng thái xấu.</span><span class="sxs-lookup"><span data-stu-id="f0612-146">Prior to making any data changes, you should investigate any customizations associated with the entity that may have led to getting the data into a bad state.</span></span> <span data-ttu-id="f0612-147">Các tùy chỉnh này phải được xử lý trước khi tiến hành bất kỳ cập nhật nào liên quan đến dữ liệu.</span><span class="sxs-lookup"><span data-stu-id="f0612-147">These customizations should be addressed before proceeding with any data-related updates.</span></span>
- <span data-ttu-id="f0612-148">Đối với các nhiệm vụ đã xác định bị bỏ, hãy xem xét xóa các nhiệm vụ này nếu chúng không cần thiết hoặc nếu chúng cần được liên kết với dự án mẹ chính xác.</span><span class="sxs-lookup"><span data-stu-id="f0612-148">For the identified tasks that have been orphaned, consider deleting these tasks if they are not needed or if they should be associated with the correct parent project.</span></span>
- <span data-ttu-id="f0612-149">Đối với bất kỳ nhiệm vụ nào có thời lượng lớn hơn 1.250 ngày, hãy xem xét thêm nhiều nhiệm vụ để thể hiện tổng thời lượng, nếu khả thi.</span><span class="sxs-lookup"><span data-stu-id="f0612-149">For any tasks where the duration is greater than 1,250 days, consider adding multiple tasks to represent the total duration, if feasible.</span></span>

> [!NOTE]
> <span data-ttu-id="f0612-150">Các mục được ghi chú với dấu hoa thị (\*) có giới hạn do thực tế là công cụ quản lý quan hệ khách hàng (CRM) chỉ hỗ trợ mở rộng 7.320 lần xuất hiện lại.</span><span class="sxs-lookup"><span data-stu-id="f0612-150">Items noted with an asterisk (\*) have limits that are due to the fact that customer relationship management (CRM) supports only 7,320 recurrence expansions.</span></span> <span data-ttu-id="f0612-151">Bạn phải ở dưới giới hạn này.</span><span class="sxs-lookup"><span data-stu-id="f0612-151">You must stay below this limit.</span></span>

## <a name="resource-assignment-relationships"></a><span data-ttu-id="f0612-152">Mối quan hệ Gán nguồn lực</span><span class="sxs-lookup"><span data-stu-id="f0612-152">Resource Assignment relationships</span></span>
<span data-ttu-id="f0612-153">Để đảm bảo nâng cấp thành công, phải duy trì chính xác các mối quan hệ sau:</span><span class="sxs-lookup"><span data-stu-id="f0612-153">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="f0612-154">Tất cả Gán nguồn lực trong cấu trúc phân tích công việc phải liên quan đến cùng một dự án.</span><span class="sxs-lookup"><span data-stu-id="f0612-154">All Resource Assignments in a work breakdown structure must be related to the same project.</span></span>
- <span data-ttu-id="f0612-155">Tất cả Gán nguồn lực trong cấu trúc phân tích công việc phải liên quan đến các thành viên nhóm dự án trong cùng một dự án.</span><span class="sxs-lookup"><span data-stu-id="f0612-155">All Resource Assignments in a work breakdown structure must be associated to project team members in the same project.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="f0612-156">Các bước giảm nhẹ có thể áp dụng</span><span class="sxs-lookup"><span data-stu-id="f0612-156">Potential mitigation steps</span></span>
- <span data-ttu-id="f0612-157">Xác định tất cả các nhiệm vụ nằm ngoài các điều kiện được mô tả ở trên.</span><span class="sxs-lookup"><span data-stu-id="f0612-157">Identify all tasks that fall outside the conditions described above.</span></span>  
- <span data-ttu-id="f0612-158">Bất kỳ Gán nguồn lực nào không còn hiệu lực sẽ bị xóa.</span><span class="sxs-lookup"><span data-stu-id="f0612-158">Any Resource Assignments that are no longer valid should be deleted.</span></span>

## <a name="project-task-dependency-relationships"></a><span data-ttu-id="f0612-159">Mối quan hệ phụ thuộc của nhiệm vụ dự án</span><span class="sxs-lookup"><span data-stu-id="f0612-159">Project task dependency relationships</span></span>
<span data-ttu-id="f0612-160">Để đảm bảo nâng cấp thành công, phải duy trì chính xác các mối quan hệ sau:</span><span class="sxs-lookup"><span data-stu-id="f0612-160">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="f0612-161">Tất cả yếu tố phụ thuộc nhiệm vụ dự án phải liên quan đến cùng một dự án.</span><span class="sxs-lookup"><span data-stu-id="f0612-161">All project task dependencies must be related to the same project.</span></span>
- <span data-ttu-id="f0612-162">Trong một nhiệm vụ, không được tham chiếu cùng một yếu tố phụ thuộc nhiều hơn một lần.</span><span class="sxs-lookup"><span data-stu-id="f0612-162">A task can't have the same dependency referenced more than once.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]