---
title: Sử dụng API lịch trình để thực hiện các hoạt động với các thực thể Lập lịch trình
description: Chủ đề này cung cấp thông tin và mẫu để sử dụng API lịch trình.
author: sigitac
manager: Annbe
ms.date: 04/27/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e03f4e6c49a835206b23cade3fabe3fd26693441
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950830"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="e5181-103">Sử dụng API lịch trình để thực hiện các hoạt động với các thực thể Lập lịch trình</span><span class="sxs-lookup"><span data-stu-id="e5181-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="e5181-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="e5181-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="e5181-105">Một số hoặc tất cả chức năng được ghi chú trong chủ đề này khả dụng như một phần của bản phát hành xem trước.</span><span class="sxs-lookup"><span data-stu-id="e5181-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="e5181-106">Nội dung và chức năng có thể thay đổi.</span><span class="sxs-lookup"><span data-stu-id="e5181-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="e5181-107">Thực thể lập lịch trình</span><span class="sxs-lookup"><span data-stu-id="e5181-107">Scheduling entities</span></span>

<span data-ttu-id="e5181-108">API lịch trình cung cấp khả năng thực hiện các thao tác tạo, cập nhật và xóa với **Thực thể lập lịch trình**.</span><span class="sxs-lookup"><span data-stu-id="e5181-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="e5181-109">Các thực thể này được quản lý thông qua công cụ Lập lịch trình trong Dự án cho web.</span><span class="sxs-lookup"><span data-stu-id="e5181-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="e5181-110">Các thao tác tạo, cập nhật và xóa với **Thực thể lập lịch trình** đã bị hạn chế trong các bản phát hành Dynamics 365 Project Operations trước đó.</span><span class="sxs-lookup"><span data-stu-id="e5181-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="e5181-111">Bảng sau cung cấp danh sách đầy đủ các **Thực thể lập lịch trình**.</span><span class="sxs-lookup"><span data-stu-id="e5181-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="e5181-112">Tên thực thể</span><span class="sxs-lookup"><span data-stu-id="e5181-112">Entity name</span></span>  | <span data-ttu-id="e5181-113">Tên logic của thực thể</span><span class="sxs-lookup"><span data-stu-id="e5181-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="e5181-114">Dự án</span><span class="sxs-lookup"><span data-stu-id="e5181-114">Project</span></span> | <span data-ttu-id="e5181-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="e5181-115">msdyn_project</span></span> |
| <span data-ttu-id="e5181-116">Nhiệm vụ dự án</span><span class="sxs-lookup"><span data-stu-id="e5181-116">Project Task</span></span>  | <span data-ttu-id="e5181-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="e5181-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="e5181-118">Quan hệ phụ thuộc Nhiệm vụ Dự án</span><span class="sxs-lookup"><span data-stu-id="e5181-118">Project Task Dependency</span></span>  | <span data-ttu-id="e5181-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="e5181-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="e5181-120">Gán Nguồn lực</span><span class="sxs-lookup"><span data-stu-id="e5181-120">Resource Assignment</span></span> | <span data-ttu-id="e5181-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="e5181-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="e5181-122">Bộ chứa Dự án</span><span class="sxs-lookup"><span data-stu-id="e5181-122">Project Bucket</span></span>  | <span data-ttu-id="e5181-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="e5181-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="e5181-124">Thành viên Nhóm Dự án</span><span class="sxs-lookup"><span data-stu-id="e5181-124">Project Team Member</span></span> | <span data-ttu-id="e5181-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="e5181-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="e5181-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="e5181-126">OperationSet</span></span>

<span data-ttu-id="e5181-127">OperationSet là một mẫu đơn vị công việc có thể được sử dụng khi phải xử lý một số yêu cầu tác động lên lịch trình trong một giao dịch.</span><span class="sxs-lookup"><span data-stu-id="e5181-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="e5181-128">API lịch trình</span><span class="sxs-lookup"><span data-stu-id="e5181-128">Schedule APIs</span></span>

<span data-ttu-id="e5181-129">Sau đây là danh sách các API lịch trình hiện tại.</span><span class="sxs-lookup"><span data-stu-id="e5181-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="e5181-130">**msdyn_CreateProjectV1**: API này có thể được dùng để tạo một dự án.</span><span class="sxs-lookup"><span data-stu-id="e5181-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="e5181-131">Nhóm dự án và dự án mặc định được tạo ngay lập tức.</span><span class="sxs-lookup"><span data-stu-id="e5181-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="e5181-132">**msdyn_CreateTeamMemberV1**: API này có thể được dùng để tạo một thành viên trong nhóm dự án.</span><span class="sxs-lookup"><span data-stu-id="e5181-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="e5181-133">Hồ sơ thành viên trong nhóm được tạo ngay lập tức.</span><span class="sxs-lookup"><span data-stu-id="e5181-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="e5181-134">**msdyn_CreateOperationSetV1**: API này có thể được dùng để lập lịch trình một số yêu cầu phải được thực hiện trong một giao dịch.</span><span class="sxs-lookup"><span data-stu-id="e5181-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="e5181-135">**msdyn_PSSCreateV1**: API này có thể được dùng để tạo một thực thể.</span><span class="sxs-lookup"><span data-stu-id="e5181-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="e5181-136">Thực thể có thể là bất kỳ thực thể Lập lịch trình nào hỗ trợ thao tác tạo.</span><span class="sxs-lookup"><span data-stu-id="e5181-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="e5181-137">**msdyn_PSSUpdateV1**: API này có thể được dùng để cập nhật một thực thể.</span><span class="sxs-lookup"><span data-stu-id="e5181-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="e5181-138">Thực thể có thể là bất kỳ thực thể Lập lịch trình nào hỗ trợ thao tác cập nhật.</span><span class="sxs-lookup"><span data-stu-id="e5181-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="e5181-139">**msdyn_PSSDeleteV1**: API này có thể được dùng để xóa một thực thể.</span><span class="sxs-lookup"><span data-stu-id="e5181-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="e5181-140">Thực thể có thể là bất kỳ thực thể Lập lịch trình nào hỗ trợ thao tác xóa.</span><span class="sxs-lookup"><span data-stu-id="e5181-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="e5181-141">**msdyn_ExecuteOperationSetV1**: API này được dùng để thực thi tất cả các thao tác trong nhóm thao tác nhất định.</span><span class="sxs-lookup"><span data-stu-id="e5181-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="e5181-142">Sử dụng API lịch trình với OperationSet</span><span class="sxs-lookup"><span data-stu-id="e5181-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="e5181-143">Bởi vì bản ghi có cả **CreateProjectV1** và **CreateTeamMemberV1** được tạo ngay lập tức, nên không thể dùng các API này trực tiếp trong **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="e5181-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="e5181-144">Tuy nhiên, bạn có thể sử dụng API để tạo các bản ghi cần thiết, tạo một **OperationSet**, sau đó sử dụng các bản ghi được tạo trước này trong **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="e5181-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="e5181-145">Thao tác được hỗ trợ</span><span class="sxs-lookup"><span data-stu-id="e5181-145">Supported operations</span></span>

| <span data-ttu-id="e5181-146">Thực thể lập lịch trình</span><span class="sxs-lookup"><span data-stu-id="e5181-146">Scheduling entity</span></span> | <span data-ttu-id="e5181-147">Tạo</span><span class="sxs-lookup"><span data-stu-id="e5181-147">Create</span></span> | <span data-ttu-id="e5181-148">Update</span><span class="sxs-lookup"><span data-stu-id="e5181-148">Update</span></span> | <span data-ttu-id="e5181-149">Delete</span><span class="sxs-lookup"><span data-stu-id="e5181-149">Delete</span></span> | <span data-ttu-id="e5181-150">Những điều quan trọng cần cân nhắc</span><span class="sxs-lookup"><span data-stu-id="e5181-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="e5181-151">Nhiệm vụ dự án</span><span class="sxs-lookup"><span data-stu-id="e5181-151">Project task</span></span> | <span data-ttu-id="e5181-152">Có</span><span class="sxs-lookup"><span data-stu-id="e5181-152">Yes</span></span> | <span data-ttu-id="e5181-153">Có</span><span class="sxs-lookup"><span data-stu-id="e5181-153">Yes</span></span> | <span data-ttu-id="e5181-154">Có</span><span class="sxs-lookup"><span data-stu-id="e5181-154">Yes</span></span> | <span data-ttu-id="e5181-155">Không có</span><span class="sxs-lookup"><span data-stu-id="e5181-155">None</span></span> |
| <span data-ttu-id="e5181-156">Quan hệ phụ thuộc nhiệm vụ dự án</span><span class="sxs-lookup"><span data-stu-id="e5181-156">Project task dependency</span></span> | <span data-ttu-id="e5181-157">Có</span><span class="sxs-lookup"><span data-stu-id="e5181-157">Yes</span></span> | <span data-ttu-id="e5181-158">Có</span><span class="sxs-lookup"><span data-stu-id="e5181-158">Yes</span></span> | | <span data-ttu-id="e5181-159">Bản ghi quan hệ phụ thuộc nhiệm vụ dự án không được cập nhật.</span><span class="sxs-lookup"><span data-stu-id="e5181-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="e5181-160">Thay vào đó, một bản ghi cũ có thể bị xóa và một bản ghi mới có thể được tạo.</span><span class="sxs-lookup"><span data-stu-id="e5181-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="e5181-161">Công việc giao cho nguồn lực</span><span class="sxs-lookup"><span data-stu-id="e5181-161">Resource assignment</span></span> | <span data-ttu-id="e5181-162">Có</span><span class="sxs-lookup"><span data-stu-id="e5181-162">Yes</span></span> | <span data-ttu-id="e5181-163">Có</span><span class="sxs-lookup"><span data-stu-id="e5181-163">Yes</span></span> | | <span data-ttu-id="e5181-164">Không hỗ trợ thao tác với các trường sau: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** và **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="e5181-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="e5181-165">Bản ghi việc được giao không được cập nhật.</span><span class="sxs-lookup"><span data-stu-id="e5181-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="e5181-166">Thay vào đó, một bản ghi cũ có thể bị xóa và một bản ghi mới có thể được tạo.</span><span class="sxs-lookup"><span data-stu-id="e5181-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="e5181-167">Nhóm dự án</span><span class="sxs-lookup"><span data-stu-id="e5181-167">Project bucket</span></span> | <span data-ttu-id="e5181-168">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="e5181-168">N/A</span></span> | <span data-ttu-id="e5181-169">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="e5181-169">N/A</span></span> | <span data-ttu-id="e5181-170">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="e5181-170">N/A</span></span> | <span data-ttu-id="e5181-171">Nhóm mặc định được tạo bằng cách sử dụng API **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="e5181-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="e5181-172">Thành viên nhóm dự án</span><span class="sxs-lookup"><span data-stu-id="e5181-172">Project team member</span></span> | <span data-ttu-id="e5181-173">Có</span><span class="sxs-lookup"><span data-stu-id="e5181-173">Yes</span></span> | <span data-ttu-id="e5181-174">Có</span><span class="sxs-lookup"><span data-stu-id="e5181-174">Yes</span></span> | <span data-ttu-id="e5181-175">Có</span><span class="sxs-lookup"><span data-stu-id="e5181-175">Yes</span></span> | <span data-ttu-id="e5181-176">Đối với thao tác tạo, hãy sử dụng API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="e5181-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="e5181-177">Dự án</span><span class="sxs-lookup"><span data-stu-id="e5181-177">Project</span></span> | <span data-ttu-id="e5181-178">Có</span><span class="sxs-lookup"><span data-stu-id="e5181-178">Yes</span></span> | <span data-ttu-id="e5181-179">Có</span><span class="sxs-lookup"><span data-stu-id="e5181-179">Yes</span></span> | <span data-ttu-id="e5181-180">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="e5181-180">N/A</span></span> | <span data-ttu-id="e5181-181">Không hỗ trợ thao tác với các trường sau: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** và **Duration**.</span><span class="sxs-lookup"><span data-stu-id="e5181-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="e5181-182">Các API này có thể được gọi ra với các đối tượng thực thể bao gồm các trường tùy chỉnh.</span><span class="sxs-lookup"><span data-stu-id="e5181-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="e5181-183">Thuộc tính ID là không bắt buộc.</span><span class="sxs-lookup"><span data-stu-id="e5181-183">The ID property is optional.</span></span> <span data-ttu-id="e5181-184">Nếu được cung cấp, hệ thống sẽ cố gắng sử dụng ID thuộc tính và đưa ra một ngoại lệ nếu không thể sử dụng.</span><span class="sxs-lookup"><span data-stu-id="e5181-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="e5181-185">Nếu không được cung cấp, hệ thống sẽ tạo ID thuộc tính.</span><span class="sxs-lookup"><span data-stu-id="e5181-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="e5181-186">Các trường bị hạn chế</span><span class="sxs-lookup"><span data-stu-id="e5181-186">Restricted fields</span></span>

<span data-ttu-id="e5181-187">Các bảng sau xác định các trường bị hạn chế trong **Tạo** và **Chỉnh sửa**.</span><span class="sxs-lookup"><span data-stu-id="e5181-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="e5181-188">Nhiệm vụ dự án</span><span class="sxs-lookup"><span data-stu-id="e5181-188">Project task</span></span>

| <span data-ttu-id="e5181-189">**Tên lô-gic**</span><span class="sxs-lookup"><span data-stu-id="e5181-189">**Logical name**</span></span>                       | <span data-ttu-id="e5181-190">**Có thể tạo**</span><span class="sxs-lookup"><span data-stu-id="e5181-190">**Can create**</span></span> | <span data-ttu-id="e5181-191">**Có thể chỉnh sửa**</span><span class="sxs-lookup"><span data-stu-id="e5181-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="e5181-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="e5181-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="e5181-193">không</span><span class="sxs-lookup"><span data-stu-id="e5181-193">no</span></span>             | <span data-ttu-id="e5181-194">không</span><span class="sxs-lookup"><span data-stu-id="e5181-194">no</span></span>               |
| <span data-ttu-id="e5181-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="e5181-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="e5181-196">không</span><span class="sxs-lookup"><span data-stu-id="e5181-196">no</span></span>             | <span data-ttu-id="e5181-197">không</span><span class="sxs-lookup"><span data-stu-id="e5181-197">no</span></span>               |
| <span data-ttu-id="e5181-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="e5181-198">msdyn_actualend</span></span>                        | <span data-ttu-id="e5181-199">không</span><span class="sxs-lookup"><span data-stu-id="e5181-199">no</span></span>             | <span data-ttu-id="e5181-200">không</span><span class="sxs-lookup"><span data-stu-id="e5181-200">no</span></span>               |
| <span data-ttu-id="e5181-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="e5181-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="e5181-202">không</span><span class="sxs-lookup"><span data-stu-id="e5181-202">no</span></span>             | <span data-ttu-id="e5181-203">không</span><span class="sxs-lookup"><span data-stu-id="e5181-203">no</span></span>               |
| <span data-ttu-id="e5181-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="e5181-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="e5181-205">không</span><span class="sxs-lookup"><span data-stu-id="e5181-205">no</span></span>             | <span data-ttu-id="e5181-206">không</span><span class="sxs-lookup"><span data-stu-id="e5181-206">no</span></span>               |
| <span data-ttu-id="e5181-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="e5181-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="e5181-208">không</span><span class="sxs-lookup"><span data-stu-id="e5181-208">no</span></span>             | <span data-ttu-id="e5181-209">không</span><span class="sxs-lookup"><span data-stu-id="e5181-209">no</span></span>               |
| <span data-ttu-id="e5181-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="e5181-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="e5181-211">không</span><span class="sxs-lookup"><span data-stu-id="e5181-211">no</span></span>             | <span data-ttu-id="e5181-212">không</span><span class="sxs-lookup"><span data-stu-id="e5181-212">no</span></span>               |
| <span data-ttu-id="e5181-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="e5181-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="e5181-214">không</span><span class="sxs-lookup"><span data-stu-id="e5181-214">no</span></span>             | <span data-ttu-id="e5181-215">không</span><span class="sxs-lookup"><span data-stu-id="e5181-215">no</span></span>               |
| <span data-ttu-id="e5181-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="e5181-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="e5181-217">không</span><span class="sxs-lookup"><span data-stu-id="e5181-217">no</span></span>             | <span data-ttu-id="e5181-218">không</span><span class="sxs-lookup"><span data-stu-id="e5181-218">no</span></span>               |
| <span data-ttu-id="e5181-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="e5181-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="e5181-220">không</span><span class="sxs-lookup"><span data-stu-id="e5181-220">no</span></span>             | <span data-ttu-id="e5181-221">không</span><span class="sxs-lookup"><span data-stu-id="e5181-221">no</span></span>               |
| <span data-ttu-id="e5181-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="e5181-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="e5181-223">không</span><span class="sxs-lookup"><span data-stu-id="e5181-223">no</span></span>             | <span data-ttu-id="e5181-224">không</span><span class="sxs-lookup"><span data-stu-id="e5181-224">no</span></span>               |
| <span data-ttu-id="e5181-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="e5181-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="e5181-226">không</span><span class="sxs-lookup"><span data-stu-id="e5181-226">no</span></span>             | <span data-ttu-id="e5181-227">không</span><span class="sxs-lookup"><span data-stu-id="e5181-227">no</span></span>               |
| <span data-ttu-id="e5181-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="e5181-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="e5181-229">không</span><span class="sxs-lookup"><span data-stu-id="e5181-229">no</span></span>             | <span data-ttu-id="e5181-230">không</span><span class="sxs-lookup"><span data-stu-id="e5181-230">no</span></span>               |
| <span data-ttu-id="e5181-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="e5181-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="e5181-232">không</span><span class="sxs-lookup"><span data-stu-id="e5181-232">no</span></span>             | <span data-ttu-id="e5181-233">không</span><span class="sxs-lookup"><span data-stu-id="e5181-233">no</span></span>               |
| <span data-ttu-id="e5181-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="e5181-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="e5181-235">không</span><span class="sxs-lookup"><span data-stu-id="e5181-235">no</span></span>             | <span data-ttu-id="e5181-236">không</span><span class="sxs-lookup"><span data-stu-id="e5181-236">no</span></span>               |
| <span data-ttu-id="e5181-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="e5181-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="e5181-238">không</span><span class="sxs-lookup"><span data-stu-id="e5181-238">no</span></span>             | <span data-ttu-id="e5181-239">không</span><span class="sxs-lookup"><span data-stu-id="e5181-239">no</span></span>               |
| <span data-ttu-id="e5181-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="e5181-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="e5181-241">không</span><span class="sxs-lookup"><span data-stu-id="e5181-241">no</span></span>             | <span data-ttu-id="e5181-242">không</span><span class="sxs-lookup"><span data-stu-id="e5181-242">no</span></span>               |
| <span data-ttu-id="e5181-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="e5181-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="e5181-244">không</span><span class="sxs-lookup"><span data-stu-id="e5181-244">no</span></span>             | <span data-ttu-id="e5181-245">không</span><span class="sxs-lookup"><span data-stu-id="e5181-245">no</span></span>               |
| <span data-ttu-id="e5181-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="e5181-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="e5181-247">không</span><span class="sxs-lookup"><span data-stu-id="e5181-247">no</span></span>             | <span data-ttu-id="e5181-248">không</span><span class="sxs-lookup"><span data-stu-id="e5181-248">no</span></span>               |
| <span data-ttu-id="e5181-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="e5181-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="e5181-250">không</span><span class="sxs-lookup"><span data-stu-id="e5181-250">no</span></span>             | <span data-ttu-id="e5181-251">không</span><span class="sxs-lookup"><span data-stu-id="e5181-251">no</span></span>               |
| <span data-ttu-id="e5181-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="e5181-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="e5181-253">không</span><span class="sxs-lookup"><span data-stu-id="e5181-253">no</span></span>             | <span data-ttu-id="e5181-254">không</span><span class="sxs-lookup"><span data-stu-id="e5181-254">no</span></span>               |
| <span data-ttu-id="e5181-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="e5181-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="e5181-256">không</span><span class="sxs-lookup"><span data-stu-id="e5181-256">no</span></span>             | <span data-ttu-id="e5181-257">không</span><span class="sxs-lookup"><span data-stu-id="e5181-257">no</span></span>               |
| <span data-ttu-id="e5181-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="e5181-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="e5181-259">không</span><span class="sxs-lookup"><span data-stu-id="e5181-259">no</span></span>             | <span data-ttu-id="e5181-260">không</span><span class="sxs-lookup"><span data-stu-id="e5181-260">no</span></span>               |
| <span data-ttu-id="e5181-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="e5181-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="e5181-262">không</span><span class="sxs-lookup"><span data-stu-id="e5181-262">no</span></span>             | <span data-ttu-id="e5181-263">không</span><span class="sxs-lookup"><span data-stu-id="e5181-263">no</span></span>               |
| <span data-ttu-id="e5181-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="e5181-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="e5181-265">không</span><span class="sxs-lookup"><span data-stu-id="e5181-265">no</span></span>             | <span data-ttu-id="e5181-266">không</span><span class="sxs-lookup"><span data-stu-id="e5181-266">no</span></span>               |
| <span data-ttu-id="e5181-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="e5181-267">msdyn_progress</span></span>                         | <span data-ttu-id="e5181-268">không</span><span class="sxs-lookup"><span data-stu-id="e5181-268">no</span></span>             | <span data-ttu-id="e5181-269">không (có cho P4W)</span><span class="sxs-lookup"><span data-stu-id="e5181-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="e5181-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="e5181-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="e5181-271">không</span><span class="sxs-lookup"><span data-stu-id="e5181-271">no</span></span>             | <span data-ttu-id="e5181-272">không</span><span class="sxs-lookup"><span data-stu-id="e5181-272">no</span></span>               |
| <span data-ttu-id="e5181-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="e5181-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="e5181-274">không</span><span class="sxs-lookup"><span data-stu-id="e5181-274">no</span></span>             | <span data-ttu-id="e5181-275">không</span><span class="sxs-lookup"><span data-stu-id="e5181-275">no</span></span>               |
| <span data-ttu-id="e5181-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="e5181-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="e5181-277">không</span><span class="sxs-lookup"><span data-stu-id="e5181-277">no</span></span>             | <span data-ttu-id="e5181-278">không</span><span class="sxs-lookup"><span data-stu-id="e5181-278">no</span></span>               |
| <span data-ttu-id="e5181-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="e5181-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="e5181-280">không</span><span class="sxs-lookup"><span data-stu-id="e5181-280">no</span></span>             | <span data-ttu-id="e5181-281">không</span><span class="sxs-lookup"><span data-stu-id="e5181-281">no</span></span>               |
| <span data-ttu-id="e5181-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="e5181-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="e5181-283">không</span><span class="sxs-lookup"><span data-stu-id="e5181-283">no</span></span>             | <span data-ttu-id="e5181-284">không</span><span class="sxs-lookup"><span data-stu-id="e5181-284">no</span></span>               |
| <span data-ttu-id="e5181-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="e5181-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="e5181-286">không</span><span class="sxs-lookup"><span data-stu-id="e5181-286">no</span></span>             | <span data-ttu-id="e5181-287">không</span><span class="sxs-lookup"><span data-stu-id="e5181-287">no</span></span>               |
| <span data-ttu-id="e5181-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="e5181-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="e5181-289">không</span><span class="sxs-lookup"><span data-stu-id="e5181-289">no</span></span>             | <span data-ttu-id="e5181-290">không</span><span class="sxs-lookup"><span data-stu-id="e5181-290">no</span></span>               |
| <span data-ttu-id="e5181-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="e5181-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="e5181-292">không</span><span class="sxs-lookup"><span data-stu-id="e5181-292">no</span></span>             | <span data-ttu-id="e5181-293">không</span><span class="sxs-lookup"><span data-stu-id="e5181-293">no</span></span>               |
| <span data-ttu-id="e5181-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="e5181-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="e5181-295">không</span><span class="sxs-lookup"><span data-stu-id="e5181-295">no</span></span>             | <span data-ttu-id="e5181-296">không</span><span class="sxs-lookup"><span data-stu-id="e5181-296">no</span></span>               |
| <span data-ttu-id="e5181-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="e5181-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="e5181-298">không</span><span class="sxs-lookup"><span data-stu-id="e5181-298">no</span></span>             | <span data-ttu-id="e5181-299">không</span><span class="sxs-lookup"><span data-stu-id="e5181-299">no</span></span>               |
| <span data-ttu-id="e5181-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="e5181-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="e5181-301">không</span><span class="sxs-lookup"><span data-stu-id="e5181-301">no</span></span>             | <span data-ttu-id="e5181-302">không</span><span class="sxs-lookup"><span data-stu-id="e5181-302">no</span></span>               |
| <span data-ttu-id="e5181-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="e5181-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="e5181-304">không</span><span class="sxs-lookup"><span data-stu-id="e5181-304">no</span></span>             | <span data-ttu-id="e5181-305">không</span><span class="sxs-lookup"><span data-stu-id="e5181-305">no</span></span>               |
| <span data-ttu-id="e5181-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="e5181-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="e5181-307">không</span><span class="sxs-lookup"><span data-stu-id="e5181-307">no</span></span>             | <span data-ttu-id="e5181-308">không</span><span class="sxs-lookup"><span data-stu-id="e5181-308">no</span></span>               |
| <span data-ttu-id="e5181-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="e5181-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="e5181-310">không</span><span class="sxs-lookup"><span data-stu-id="e5181-310">no</span></span>             | <span data-ttu-id="e5181-311">không</span><span class="sxs-lookup"><span data-stu-id="e5181-311">no</span></span>               |
| <span data-ttu-id="e5181-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="e5181-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="e5181-313">không</span><span class="sxs-lookup"><span data-stu-id="e5181-313">no</span></span>             | <span data-ttu-id="e5181-314">không</span><span class="sxs-lookup"><span data-stu-id="e5181-314">no</span></span>               |
| <span data-ttu-id="e5181-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="e5181-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="e5181-316">không</span><span class="sxs-lookup"><span data-stu-id="e5181-316">no</span></span>             | <span data-ttu-id="e5181-317">không</span><span class="sxs-lookup"><span data-stu-id="e5181-317">no</span></span>               |
| <span data-ttu-id="e5181-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="e5181-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="e5181-319">không</span><span class="sxs-lookup"><span data-stu-id="e5181-319">no</span></span>             | <span data-ttu-id="e5181-320">không</span><span class="sxs-lookup"><span data-stu-id="e5181-320">no</span></span>               |
| <span data-ttu-id="e5181-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="e5181-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="e5181-322">không</span><span class="sxs-lookup"><span data-stu-id="e5181-322">no</span></span>             | <span data-ttu-id="e5181-323">không</span><span class="sxs-lookup"><span data-stu-id="e5181-323">no</span></span>               |
| <span data-ttu-id="e5181-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="e5181-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="e5181-325">không</span><span class="sxs-lookup"><span data-stu-id="e5181-325">no</span></span>             | <span data-ttu-id="e5181-326">không</span><span class="sxs-lookup"><span data-stu-id="e5181-326">no</span></span>               |
| <span data-ttu-id="e5181-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="e5181-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="e5181-328">không</span><span class="sxs-lookup"><span data-stu-id="e5181-328">no</span></span>             | <span data-ttu-id="e5181-329">không</span><span class="sxs-lookup"><span data-stu-id="e5181-329">no</span></span>               |
| <span data-ttu-id="e5181-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="e5181-330">msdyn_summary</span></span>                          | <span data-ttu-id="e5181-331">không</span><span class="sxs-lookup"><span data-stu-id="e5181-331">no</span></span>             | <span data-ttu-id="e5181-332">không</span><span class="sxs-lookup"><span data-stu-id="e5181-332">no</span></span>               |
| <span data-ttu-id="e5181-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="e5181-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="e5181-334">không</span><span class="sxs-lookup"><span data-stu-id="e5181-334">no</span></span>             | <span data-ttu-id="e5181-335">không</span><span class="sxs-lookup"><span data-stu-id="e5181-335">no</span></span>               |
| <span data-ttu-id="e5181-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="e5181-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="e5181-337">không</span><span class="sxs-lookup"><span data-stu-id="e5181-337">no</span></span>             | <span data-ttu-id="e5181-338">không</span><span class="sxs-lookup"><span data-stu-id="e5181-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="e5181-339">Quan hệ phụ thuộc nhiệm vụ dự án</span><span class="sxs-lookup"><span data-stu-id="e5181-339">Project task dependency</span></span>

| <span data-ttu-id="e5181-340">**Tên lô-gic**</span><span class="sxs-lookup"><span data-stu-id="e5181-340">**Logical name**</span></span>              | <span data-ttu-id="e5181-341">**Có thể tạo**</span><span class="sxs-lookup"><span data-stu-id="e5181-341">**Can create**</span></span> | <span data-ttu-id="e5181-342">**Có thể chỉnh sửa**</span><span class="sxs-lookup"><span data-stu-id="e5181-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="e5181-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="e5181-343">msdyn_linktype</span></span>                | <span data-ttu-id="e5181-344">không</span><span class="sxs-lookup"><span data-stu-id="e5181-344">no</span></span>             | <span data-ttu-id="e5181-345">không</span><span class="sxs-lookup"><span data-stu-id="e5181-345">no</span></span>           |
| <span data-ttu-id="e5181-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="e5181-346">msdyn_linktypename</span></span>            | <span data-ttu-id="e5181-347">không</span><span class="sxs-lookup"><span data-stu-id="e5181-347">no</span></span>             | <span data-ttu-id="e5181-348">không</span><span class="sxs-lookup"><span data-stu-id="e5181-348">no</span></span>           |
| <span data-ttu-id="e5181-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="e5181-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="e5181-350">có</span><span class="sxs-lookup"><span data-stu-id="e5181-350">yes</span></span>            | <span data-ttu-id="e5181-351">không</span><span class="sxs-lookup"><span data-stu-id="e5181-351">no</span></span>           |
| <span data-ttu-id="e5181-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="e5181-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="e5181-353">có</span><span class="sxs-lookup"><span data-stu-id="e5181-353">yes</span></span>            | <span data-ttu-id="e5181-354">không</span><span class="sxs-lookup"><span data-stu-id="e5181-354">no</span></span>           |
| <span data-ttu-id="e5181-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="e5181-355">msdyn_project</span></span>                 | <span data-ttu-id="e5181-356">có</span><span class="sxs-lookup"><span data-stu-id="e5181-356">yes</span></span>            | <span data-ttu-id="e5181-357">không</span><span class="sxs-lookup"><span data-stu-id="e5181-357">no</span></span>           |
| <span data-ttu-id="e5181-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="e5181-358">msdyn_projectname</span></span>             | <span data-ttu-id="e5181-359">có</span><span class="sxs-lookup"><span data-stu-id="e5181-359">yes</span></span>            | <span data-ttu-id="e5181-360">không</span><span class="sxs-lookup"><span data-stu-id="e5181-360">no</span></span>           |
| <span data-ttu-id="e5181-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="e5181-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="e5181-362">có</span><span class="sxs-lookup"><span data-stu-id="e5181-362">yes</span></span>            | <span data-ttu-id="e5181-363">không</span><span class="sxs-lookup"><span data-stu-id="e5181-363">no</span></span>           |
| <span data-ttu-id="e5181-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="e5181-364">msdyn_successortask</span></span>           | <span data-ttu-id="e5181-365">có</span><span class="sxs-lookup"><span data-stu-id="e5181-365">yes</span></span>            | <span data-ttu-id="e5181-366">không</span><span class="sxs-lookup"><span data-stu-id="e5181-366">no</span></span>           |
| <span data-ttu-id="e5181-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="e5181-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="e5181-368">có</span><span class="sxs-lookup"><span data-stu-id="e5181-368">yes</span></span>            | <span data-ttu-id="e5181-369">không</span><span class="sxs-lookup"><span data-stu-id="e5181-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="e5181-370">Công việc giao cho nguồn lực</span><span class="sxs-lookup"><span data-stu-id="e5181-370">Resource assignment</span></span>

| <span data-ttu-id="e5181-371">**Tên lô-gic**</span><span class="sxs-lookup"><span data-stu-id="e5181-371">**Logical name**</span></span>             | <span data-ttu-id="e5181-372">**Có thể tạo**</span><span class="sxs-lookup"><span data-stu-id="e5181-372">**Can create**</span></span> | <span data-ttu-id="e5181-373">**Có thể chỉnh sửa**</span><span class="sxs-lookup"><span data-stu-id="e5181-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="e5181-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="e5181-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="e5181-375">có</span><span class="sxs-lookup"><span data-stu-id="e5181-375">yes</span></span>            | <span data-ttu-id="e5181-376">không</span><span class="sxs-lookup"><span data-stu-id="e5181-376">no</span></span>           |
| <span data-ttu-id="e5181-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="e5181-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="e5181-378">có</span><span class="sxs-lookup"><span data-stu-id="e5181-378">yes</span></span>            | <span data-ttu-id="e5181-379">không</span><span class="sxs-lookup"><span data-stu-id="e5181-379">no</span></span>           |
| <span data-ttu-id="e5181-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="e5181-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="e5181-381">không</span><span class="sxs-lookup"><span data-stu-id="e5181-381">no</span></span>             | <span data-ttu-id="e5181-382">không</span><span class="sxs-lookup"><span data-stu-id="e5181-382">no</span></span>           |
| <span data-ttu-id="e5181-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="e5181-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="e5181-384">không</span><span class="sxs-lookup"><span data-stu-id="e5181-384">no</span></span>             | <span data-ttu-id="e5181-385">không</span><span class="sxs-lookup"><span data-stu-id="e5181-385">no</span></span>           |
| <span data-ttu-id="e5181-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="e5181-386">msdyn_committype</span></span>             | <span data-ttu-id="e5181-387">không</span><span class="sxs-lookup"><span data-stu-id="e5181-387">no</span></span>             | <span data-ttu-id="e5181-388">không</span><span class="sxs-lookup"><span data-stu-id="e5181-388">no</span></span>           |
| <span data-ttu-id="e5181-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="e5181-389">msdyn_committypename</span></span>         | <span data-ttu-id="e5181-390">không</span><span class="sxs-lookup"><span data-stu-id="e5181-390">no</span></span>             | <span data-ttu-id="e5181-391">không</span><span class="sxs-lookup"><span data-stu-id="e5181-391">no</span></span>           |
| <span data-ttu-id="e5181-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="e5181-392">msdyn_effort</span></span>                 | <span data-ttu-id="e5181-393">không</span><span class="sxs-lookup"><span data-stu-id="e5181-393">no</span></span>             | <span data-ttu-id="e5181-394">không</span><span class="sxs-lookup"><span data-stu-id="e5181-394">no</span></span>           |
| <span data-ttu-id="e5181-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="e5181-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="e5181-396">không</span><span class="sxs-lookup"><span data-stu-id="e5181-396">no</span></span>             | <span data-ttu-id="e5181-397">không</span><span class="sxs-lookup"><span data-stu-id="e5181-397">no</span></span>           |
| <span data-ttu-id="e5181-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="e5181-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="e5181-399">không</span><span class="sxs-lookup"><span data-stu-id="e5181-399">no</span></span>             | <span data-ttu-id="e5181-400">không</span><span class="sxs-lookup"><span data-stu-id="e5181-400">no</span></span>           |
| <span data-ttu-id="e5181-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="e5181-401">msdyn_finish</span></span>                 | <span data-ttu-id="e5181-402">không</span><span class="sxs-lookup"><span data-stu-id="e5181-402">no</span></span>             | <span data-ttu-id="e5181-403">không</span><span class="sxs-lookup"><span data-stu-id="e5181-403">no</span></span>           |
| <span data-ttu-id="e5181-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="e5181-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="e5181-405">không</span><span class="sxs-lookup"><span data-stu-id="e5181-405">no</span></span>             | <span data-ttu-id="e5181-406">không</span><span class="sxs-lookup"><span data-stu-id="e5181-406">no</span></span>           |
| <span data-ttu-id="e5181-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="e5181-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="e5181-408">không</span><span class="sxs-lookup"><span data-stu-id="e5181-408">no</span></span>             | <span data-ttu-id="e5181-409">không</span><span class="sxs-lookup"><span data-stu-id="e5181-409">no</span></span>           |
| <span data-ttu-id="e5181-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="e5181-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="e5181-411">không</span><span class="sxs-lookup"><span data-stu-id="e5181-411">no</span></span>             | <span data-ttu-id="e5181-412">không</span><span class="sxs-lookup"><span data-stu-id="e5181-412">no</span></span>           |
| <span data-ttu-id="e5181-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="e5181-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="e5181-414">không</span><span class="sxs-lookup"><span data-stu-id="e5181-414">no</span></span>             | <span data-ttu-id="e5181-415">không</span><span class="sxs-lookup"><span data-stu-id="e5181-415">no</span></span>           |
| <span data-ttu-id="e5181-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="e5181-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="e5181-417">không</span><span class="sxs-lookup"><span data-stu-id="e5181-417">no</span></span>             | <span data-ttu-id="e5181-418">không</span><span class="sxs-lookup"><span data-stu-id="e5181-418">no</span></span>           |
| <span data-ttu-id="e5181-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="e5181-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="e5181-420">không</span><span class="sxs-lookup"><span data-stu-id="e5181-420">no</span></span>             | <span data-ttu-id="e5181-421">không</span><span class="sxs-lookup"><span data-stu-id="e5181-421">no</span></span>           |
| <span data-ttu-id="e5181-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="e5181-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="e5181-423">không</span><span class="sxs-lookup"><span data-stu-id="e5181-423">no</span></span>             | <span data-ttu-id="e5181-424">không</span><span class="sxs-lookup"><span data-stu-id="e5181-424">no</span></span>           |
| <span data-ttu-id="e5181-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="e5181-425">msdyn_projectid</span></span>              | <span data-ttu-id="e5181-426">có</span><span class="sxs-lookup"><span data-stu-id="e5181-426">yes</span></span>            | <span data-ttu-id="e5181-427">không</span><span class="sxs-lookup"><span data-stu-id="e5181-427">no</span></span>           |
| <span data-ttu-id="e5181-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="e5181-428">msdyn_projectidname</span></span>          | <span data-ttu-id="e5181-429">không</span><span class="sxs-lookup"><span data-stu-id="e5181-429">no</span></span>             | <span data-ttu-id="e5181-430">không</span><span class="sxs-lookup"><span data-stu-id="e5181-430">no</span></span>           |
| <span data-ttu-id="e5181-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="e5181-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="e5181-432">không</span><span class="sxs-lookup"><span data-stu-id="e5181-432">no</span></span>             | <span data-ttu-id="e5181-433">không</span><span class="sxs-lookup"><span data-stu-id="e5181-433">no</span></span>           |
| <span data-ttu-id="e5181-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="e5181-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="e5181-435">không</span><span class="sxs-lookup"><span data-stu-id="e5181-435">no</span></span>             | <span data-ttu-id="e5181-436">không</span><span class="sxs-lookup"><span data-stu-id="e5181-436">no</span></span>           |
| <span data-ttu-id="e5181-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="e5181-437">msdyn_start</span></span>                  | <span data-ttu-id="e5181-438">không</span><span class="sxs-lookup"><span data-stu-id="e5181-438">no</span></span>             | <span data-ttu-id="e5181-439">không</span><span class="sxs-lookup"><span data-stu-id="e5181-439">no</span></span>           |
| <span data-ttu-id="e5181-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="e5181-440">msdyn_taskid</span></span>                 | <span data-ttu-id="e5181-441">không</span><span class="sxs-lookup"><span data-stu-id="e5181-441">no</span></span>             | <span data-ttu-id="e5181-442">không</span><span class="sxs-lookup"><span data-stu-id="e5181-442">no</span></span>           |
| <span data-ttu-id="e5181-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="e5181-443">msdyn_taskidname</span></span>             | <span data-ttu-id="e5181-444">không</span><span class="sxs-lookup"><span data-stu-id="e5181-444">no</span></span>             | <span data-ttu-id="e5181-445">không</span><span class="sxs-lookup"><span data-stu-id="e5181-445">no</span></span>           |
| <span data-ttu-id="e5181-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="e5181-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="e5181-447">không</span><span class="sxs-lookup"><span data-stu-id="e5181-447">no</span></span>             | <span data-ttu-id="e5181-448">không</span><span class="sxs-lookup"><span data-stu-id="e5181-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="e5181-449">Thành viên nhóm dự án</span><span class="sxs-lookup"><span data-stu-id="e5181-449">Project team member</span></span>

| <span data-ttu-id="e5181-450">**Tên lô-gic**</span><span class="sxs-lookup"><span data-stu-id="e5181-450">**Logical name**</span></span>                                 | <span data-ttu-id="e5181-451">**Có thể tạo**</span><span class="sxs-lookup"><span data-stu-id="e5181-451">**Can create**</span></span> | <span data-ttu-id="e5181-452">**Có thể chỉnh sửa**</span><span class="sxs-lookup"><span data-stu-id="e5181-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="e5181-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="e5181-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="e5181-454">không</span><span class="sxs-lookup"><span data-stu-id="e5181-454">no</span></span>             | <span data-ttu-id="e5181-455">không</span><span class="sxs-lookup"><span data-stu-id="e5181-455">no</span></span>           |
| <span data-ttu-id="e5181-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="e5181-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="e5181-457">không</span><span class="sxs-lookup"><span data-stu-id="e5181-457">no</span></span>             | <span data-ttu-id="e5181-458">không</span><span class="sxs-lookup"><span data-stu-id="e5181-458">no</span></span>           |
| <span data-ttu-id="e5181-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="e5181-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="e5181-460">không</span><span class="sxs-lookup"><span data-stu-id="e5181-460">no</span></span>             | <span data-ttu-id="e5181-461">không</span><span class="sxs-lookup"><span data-stu-id="e5181-461">no</span></span>           |
| <span data-ttu-id="e5181-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="e5181-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="e5181-463">không</span><span class="sxs-lookup"><span data-stu-id="e5181-463">no</span></span>             | <span data-ttu-id="e5181-464">không</span><span class="sxs-lookup"><span data-stu-id="e5181-464">no</span></span>           |
| <span data-ttu-id="e5181-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="e5181-465">msdyn_effort</span></span>                                     | <span data-ttu-id="e5181-466">không</span><span class="sxs-lookup"><span data-stu-id="e5181-466">no</span></span>             | <span data-ttu-id="e5181-467">không</span><span class="sxs-lookup"><span data-stu-id="e5181-467">no</span></span>           |
| <span data-ttu-id="e5181-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="e5181-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="e5181-469">không</span><span class="sxs-lookup"><span data-stu-id="e5181-469">no</span></span>             | <span data-ttu-id="e5181-470">không</span><span class="sxs-lookup"><span data-stu-id="e5181-470">no</span></span>           |
| <span data-ttu-id="e5181-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="e5181-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="e5181-472">không</span><span class="sxs-lookup"><span data-stu-id="e5181-472">no</span></span>             | <span data-ttu-id="e5181-473">không</span><span class="sxs-lookup"><span data-stu-id="e5181-473">no</span></span>           |
| <span data-ttu-id="e5181-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="e5181-474">msdyn_finish</span></span>                                     | <span data-ttu-id="e5181-475">không</span><span class="sxs-lookup"><span data-stu-id="e5181-475">no</span></span>             | <span data-ttu-id="e5181-476">không</span><span class="sxs-lookup"><span data-stu-id="e5181-476">no</span></span>           |
| <span data-ttu-id="e5181-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="e5181-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="e5181-478">không</span><span class="sxs-lookup"><span data-stu-id="e5181-478">no</span></span>             | <span data-ttu-id="e5181-479">không</span><span class="sxs-lookup"><span data-stu-id="e5181-479">no</span></span>           |
| <span data-ttu-id="e5181-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="e5181-480">msdyn_hours</span></span>                                      | <span data-ttu-id="e5181-481">không</span><span class="sxs-lookup"><span data-stu-id="e5181-481">no</span></span>             | <span data-ttu-id="e5181-482">không</span><span class="sxs-lookup"><span data-stu-id="e5181-482">no</span></span>           |
| <span data-ttu-id="e5181-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="e5181-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="e5181-484">không</span><span class="sxs-lookup"><span data-stu-id="e5181-484">no</span></span>             | <span data-ttu-id="e5181-485">không</span><span class="sxs-lookup"><span data-stu-id="e5181-485">no</span></span>           |
| <span data-ttu-id="e5181-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="e5181-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="e5181-487">không</span><span class="sxs-lookup"><span data-stu-id="e5181-487">no</span></span>             | <span data-ttu-id="e5181-488">không</span><span class="sxs-lookup"><span data-stu-id="e5181-488">no</span></span>           |
| <span data-ttu-id="e5181-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="e5181-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="e5181-490">không</span><span class="sxs-lookup"><span data-stu-id="e5181-490">no</span></span>             | <span data-ttu-id="e5181-491">không</span><span class="sxs-lookup"><span data-stu-id="e5181-491">no</span></span>           |
| <span data-ttu-id="e5181-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="e5181-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="e5181-493">không</span><span class="sxs-lookup"><span data-stu-id="e5181-493">no</span></span>             | <span data-ttu-id="e5181-494">không</span><span class="sxs-lookup"><span data-stu-id="e5181-494">no</span></span>           |
| <span data-ttu-id="e5181-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="e5181-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="e5181-496">không</span><span class="sxs-lookup"><span data-stu-id="e5181-496">no</span></span>             | <span data-ttu-id="e5181-497">không</span><span class="sxs-lookup"><span data-stu-id="e5181-497">no</span></span>           |
| <span data-ttu-id="e5181-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="e5181-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="e5181-499">không</span><span class="sxs-lookup"><span data-stu-id="e5181-499">no</span></span>             | <span data-ttu-id="e5181-500">không</span><span class="sxs-lookup"><span data-stu-id="e5181-500">no</span></span>           |
| <span data-ttu-id="e5181-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="e5181-501">msdyn_start</span></span>                                      | <span data-ttu-id="e5181-502">không</span><span class="sxs-lookup"><span data-stu-id="e5181-502">no</span></span>             | <span data-ttu-id="e5181-503">không</span><span class="sxs-lookup"><span data-stu-id="e5181-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="e5181-504">Dự án</span><span class="sxs-lookup"><span data-stu-id="e5181-504">Project</span></span>

| <span data-ttu-id="e5181-505">**Tên lô-gic**</span><span class="sxs-lookup"><span data-stu-id="e5181-505">**Logical name**</span></span>                       | <span data-ttu-id="e5181-506">**Có thể tạo**</span><span class="sxs-lookup"><span data-stu-id="e5181-506">**Can create**</span></span> | <span data-ttu-id="e5181-507">**Có thể chỉnh sửa**</span><span class="sxs-lookup"><span data-stu-id="e5181-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="e5181-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="e5181-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="e5181-509">không</span><span class="sxs-lookup"><span data-stu-id="e5181-509">no</span></span>             | <span data-ttu-id="e5181-510">không</span><span class="sxs-lookup"><span data-stu-id="e5181-510">no</span></span>           |
| <span data-ttu-id="e5181-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="e5181-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="e5181-512">không</span><span class="sxs-lookup"><span data-stu-id="e5181-512">no</span></span>             | <span data-ttu-id="e5181-513">không</span><span class="sxs-lookup"><span data-stu-id="e5181-513">no</span></span>           |
| <span data-ttu-id="e5181-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="e5181-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="e5181-515">không</span><span class="sxs-lookup"><span data-stu-id="e5181-515">no</span></span>             | <span data-ttu-id="e5181-516">không</span><span class="sxs-lookup"><span data-stu-id="e5181-516">no</span></span>           |
| <span data-ttu-id="e5181-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="e5181-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="e5181-518">không</span><span class="sxs-lookup"><span data-stu-id="e5181-518">no</span></span>             | <span data-ttu-id="e5181-519">không</span><span class="sxs-lookup"><span data-stu-id="e5181-519">no</span></span>           |
| <span data-ttu-id="e5181-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="e5181-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="e5181-521">không</span><span class="sxs-lookup"><span data-stu-id="e5181-521">no</span></span>             | <span data-ttu-id="e5181-522">không</span><span class="sxs-lookup"><span data-stu-id="e5181-522">no</span></span>           |
| <span data-ttu-id="e5181-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="e5181-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="e5181-524">không</span><span class="sxs-lookup"><span data-stu-id="e5181-524">no</span></span>             | <span data-ttu-id="e5181-525">không</span><span class="sxs-lookup"><span data-stu-id="e5181-525">no</span></span>           |
| <span data-ttu-id="e5181-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="e5181-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="e5181-527">có</span><span class="sxs-lookup"><span data-stu-id="e5181-527">yes</span></span>            | <span data-ttu-id="e5181-528">không</span><span class="sxs-lookup"><span data-stu-id="e5181-528">no</span></span>           |
| <span data-ttu-id="e5181-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="e5181-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="e5181-530">có</span><span class="sxs-lookup"><span data-stu-id="e5181-530">yes</span></span>            | <span data-ttu-id="e5181-531">không</span><span class="sxs-lookup"><span data-stu-id="e5181-531">no</span></span>           |
| <span data-ttu-id="e5181-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="e5181-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="e5181-533">có</span><span class="sxs-lookup"><span data-stu-id="e5181-533">yes</span></span>            | <span data-ttu-id="e5181-534">không</span><span class="sxs-lookup"><span data-stu-id="e5181-534">no</span></span>           |
| <span data-ttu-id="e5181-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="e5181-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="e5181-536">không</span><span class="sxs-lookup"><span data-stu-id="e5181-536">no</span></span>             | <span data-ttu-id="e5181-537">không</span><span class="sxs-lookup"><span data-stu-id="e5181-537">no</span></span>           |
| <span data-ttu-id="e5181-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="e5181-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="e5181-539">không</span><span class="sxs-lookup"><span data-stu-id="e5181-539">no</span></span>             | <span data-ttu-id="e5181-540">không</span><span class="sxs-lookup"><span data-stu-id="e5181-540">no</span></span>           |
| <span data-ttu-id="e5181-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="e5181-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="e5181-542">không</span><span class="sxs-lookup"><span data-stu-id="e5181-542">no</span></span>             | <span data-ttu-id="e5181-543">không</span><span class="sxs-lookup"><span data-stu-id="e5181-543">no</span></span>           |
| <span data-ttu-id="e5181-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="e5181-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="e5181-545">không</span><span class="sxs-lookup"><span data-stu-id="e5181-545">no</span></span>             | <span data-ttu-id="e5181-546">không</span><span class="sxs-lookup"><span data-stu-id="e5181-546">no</span></span>           |
| <span data-ttu-id="e5181-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="e5181-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="e5181-548">không</span><span class="sxs-lookup"><span data-stu-id="e5181-548">no</span></span>             | <span data-ttu-id="e5181-549">không</span><span class="sxs-lookup"><span data-stu-id="e5181-549">no</span></span>           |
| <span data-ttu-id="e5181-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="e5181-550">msdyn_duration</span></span>                         | <span data-ttu-id="e5181-551">không</span><span class="sxs-lookup"><span data-stu-id="e5181-551">no</span></span>             | <span data-ttu-id="e5181-552">không</span><span class="sxs-lookup"><span data-stu-id="e5181-552">no</span></span>           |
| <span data-ttu-id="e5181-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="e5181-553">msdyn_effort</span></span>                           | <span data-ttu-id="e5181-554">không</span><span class="sxs-lookup"><span data-stu-id="e5181-554">no</span></span>             | <span data-ttu-id="e5181-555">không</span><span class="sxs-lookup"><span data-stu-id="e5181-555">no</span></span>           |
| <span data-ttu-id="e5181-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="e5181-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="e5181-557">không</span><span class="sxs-lookup"><span data-stu-id="e5181-557">no</span></span>             | <span data-ttu-id="e5181-558">không</span><span class="sxs-lookup"><span data-stu-id="e5181-558">no</span></span>           |
| <span data-ttu-id="e5181-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="e5181-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="e5181-560">không</span><span class="sxs-lookup"><span data-stu-id="e5181-560">no</span></span>             | <span data-ttu-id="e5181-561">không</span><span class="sxs-lookup"><span data-stu-id="e5181-561">no</span></span>           |
| <span data-ttu-id="e5181-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="e5181-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="e5181-563">không</span><span class="sxs-lookup"><span data-stu-id="e5181-563">no</span></span>             | <span data-ttu-id="e5181-564">không</span><span class="sxs-lookup"><span data-stu-id="e5181-564">no</span></span>           |
| <span data-ttu-id="e5181-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="e5181-565">msdyn_finish</span></span>                           | <span data-ttu-id="e5181-566">có</span><span class="sxs-lookup"><span data-stu-id="e5181-566">yes</span></span>            | <span data-ttu-id="e5181-567">có</span><span class="sxs-lookup"><span data-stu-id="e5181-567">yes</span></span>          |
| <span data-ttu-id="e5181-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="e5181-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="e5181-569">không</span><span class="sxs-lookup"><span data-stu-id="e5181-569">no</span></span>             | <span data-ttu-id="e5181-570">không</span><span class="sxs-lookup"><span data-stu-id="e5181-570">no</span></span>           |
| <span data-ttu-id="e5181-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="e5181-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="e5181-572">không</span><span class="sxs-lookup"><span data-stu-id="e5181-572">no</span></span>             | <span data-ttu-id="e5181-573">không</span><span class="sxs-lookup"><span data-stu-id="e5181-573">no</span></span>           |
| <span data-ttu-id="e5181-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="e5181-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="e5181-575">không</span><span class="sxs-lookup"><span data-stu-id="e5181-575">no</span></span>             | <span data-ttu-id="e5181-576">không</span><span class="sxs-lookup"><span data-stu-id="e5181-576">no</span></span>           |
| <span data-ttu-id="e5181-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="e5181-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="e5181-578">không</span><span class="sxs-lookup"><span data-stu-id="e5181-578">no</span></span>             | <span data-ttu-id="e5181-579">không</span><span class="sxs-lookup"><span data-stu-id="e5181-579">no</span></span>           |
| <span data-ttu-id="e5181-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="e5181-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="e5181-581">không</span><span class="sxs-lookup"><span data-stu-id="e5181-581">no</span></span>             | <span data-ttu-id="e5181-582">không</span><span class="sxs-lookup"><span data-stu-id="e5181-582">no</span></span>           |
| <span data-ttu-id="e5181-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="e5181-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="e5181-584">không</span><span class="sxs-lookup"><span data-stu-id="e5181-584">no</span></span>             | <span data-ttu-id="e5181-585">không</span><span class="sxs-lookup"><span data-stu-id="e5181-585">no</span></span>           |
| <span data-ttu-id="e5181-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="e5181-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="e5181-587">không</span><span class="sxs-lookup"><span data-stu-id="e5181-587">no</span></span>             | <span data-ttu-id="e5181-588">không</span><span class="sxs-lookup"><span data-stu-id="e5181-588">no</span></span>           |
| <span data-ttu-id="e5181-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="e5181-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="e5181-590">không</span><span class="sxs-lookup"><span data-stu-id="e5181-590">no</span></span>             | <span data-ttu-id="e5181-591">không</span><span class="sxs-lookup"><span data-stu-id="e5181-591">no</span></span>           |
| <span data-ttu-id="e5181-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="e5181-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="e5181-593">không</span><span class="sxs-lookup"><span data-stu-id="e5181-593">no</span></span>             | <span data-ttu-id="e5181-594">không</span><span class="sxs-lookup"><span data-stu-id="e5181-594">no</span></span>           |
| <span data-ttu-id="e5181-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="e5181-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="e5181-596">không</span><span class="sxs-lookup"><span data-stu-id="e5181-596">no</span></span>             | <span data-ttu-id="e5181-597">không</span><span class="sxs-lookup"><span data-stu-id="e5181-597">no</span></span>           |
| <span data-ttu-id="e5181-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="e5181-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="e5181-599">không</span><span class="sxs-lookup"><span data-stu-id="e5181-599">no</span></span>             | <span data-ttu-id="e5181-600">không</span><span class="sxs-lookup"><span data-stu-id="e5181-600">no</span></span>           |
| <span data-ttu-id="e5181-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="e5181-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="e5181-602">không</span><span class="sxs-lookup"><span data-stu-id="e5181-602">no</span></span>             | <span data-ttu-id="e5181-603">không</span><span class="sxs-lookup"><span data-stu-id="e5181-603">no</span></span>           |
| <span data-ttu-id="e5181-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="e5181-604">msdyn_progress</span></span>                         | <span data-ttu-id="e5181-605">không</span><span class="sxs-lookup"><span data-stu-id="e5181-605">no</span></span>             | <span data-ttu-id="e5181-606">không</span><span class="sxs-lookup"><span data-stu-id="e5181-606">no</span></span>           |
| <span data-ttu-id="e5181-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="e5181-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="e5181-608">không</span><span class="sxs-lookup"><span data-stu-id="e5181-608">no</span></span>             | <span data-ttu-id="e5181-609">không</span><span class="sxs-lookup"><span data-stu-id="e5181-609">no</span></span>           |
| <span data-ttu-id="e5181-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="e5181-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="e5181-611">không</span><span class="sxs-lookup"><span data-stu-id="e5181-611">no</span></span>             | <span data-ttu-id="e5181-612">không</span><span class="sxs-lookup"><span data-stu-id="e5181-612">no</span></span>           |
| <span data-ttu-id="e5181-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="e5181-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="e5181-614">không</span><span class="sxs-lookup"><span data-stu-id="e5181-614">no</span></span>             | <span data-ttu-id="e5181-615">không</span><span class="sxs-lookup"><span data-stu-id="e5181-615">no</span></span>           |
| <span data-ttu-id="e5181-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="e5181-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="e5181-617">không</span><span class="sxs-lookup"><span data-stu-id="e5181-617">no</span></span>             | <span data-ttu-id="e5181-618">không</span><span class="sxs-lookup"><span data-stu-id="e5181-618">no</span></span>           |
| <span data-ttu-id="e5181-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="e5181-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="e5181-620">không</span><span class="sxs-lookup"><span data-stu-id="e5181-620">no</span></span>             | <span data-ttu-id="e5181-621">không</span><span class="sxs-lookup"><span data-stu-id="e5181-621">no</span></span>           |
| <span data-ttu-id="e5181-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="e5181-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="e5181-623">không</span><span class="sxs-lookup"><span data-stu-id="e5181-623">no</span></span>             | <span data-ttu-id="e5181-624">không</span><span class="sxs-lookup"><span data-stu-id="e5181-624">no</span></span>           |
| <span data-ttu-id="e5181-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="e5181-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="e5181-626">không</span><span class="sxs-lookup"><span data-stu-id="e5181-626">no</span></span>             | <span data-ttu-id="e5181-627">không</span><span class="sxs-lookup"><span data-stu-id="e5181-627">no</span></span>           |
| <span data-ttu-id="e5181-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="e5181-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="e5181-629">không</span><span class="sxs-lookup"><span data-stu-id="e5181-629">no</span></span>             | <span data-ttu-id="e5181-630">không</span><span class="sxs-lookup"><span data-stu-id="e5181-630">no</span></span>           |
| <span data-ttu-id="e5181-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="e5181-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="e5181-632">không</span><span class="sxs-lookup"><span data-stu-id="e5181-632">no</span></span>             | <span data-ttu-id="e5181-633">không</span><span class="sxs-lookup"><span data-stu-id="e5181-633">no</span></span>           |
| <span data-ttu-id="e5181-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="e5181-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="e5181-635">không</span><span class="sxs-lookup"><span data-stu-id="e5181-635">no</span></span>             | <span data-ttu-id="e5181-636">không</span><span class="sxs-lookup"><span data-stu-id="e5181-636">no</span></span>           |
| <span data-ttu-id="e5181-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="e5181-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="e5181-638">không</span><span class="sxs-lookup"><span data-stu-id="e5181-638">no</span></span>             | <span data-ttu-id="e5181-639">không</span><span class="sxs-lookup"><span data-stu-id="e5181-639">no</span></span>           |
| <span data-ttu-id="e5181-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="e5181-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="e5181-641">không</span><span class="sxs-lookup"><span data-stu-id="e5181-641">no</span></span>             | <span data-ttu-id="e5181-642">không</span><span class="sxs-lookup"><span data-stu-id="e5181-642">no</span></span>           |
| <span data-ttu-id="e5181-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="e5181-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="e5181-644">không</span><span class="sxs-lookup"><span data-stu-id="e5181-644">no</span></span>             | <span data-ttu-id="e5181-645">không</span><span class="sxs-lookup"><span data-stu-id="e5181-645">no</span></span>           |
| <span data-ttu-id="e5181-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="e5181-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="e5181-647">không</span><span class="sxs-lookup"><span data-stu-id="e5181-647">no</span></span>             | <span data-ttu-id="e5181-648">không</span><span class="sxs-lookup"><span data-stu-id="e5181-648">no</span></span>           |
| <span data-ttu-id="e5181-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="e5181-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="e5181-650">không</span><span class="sxs-lookup"><span data-stu-id="e5181-650">no</span></span>             | <span data-ttu-id="e5181-651">không</span><span class="sxs-lookup"><span data-stu-id="e5181-651">no</span></span>           |
| <span data-ttu-id="e5181-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="e5181-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="e5181-653">không</span><span class="sxs-lookup"><span data-stu-id="e5181-653">no</span></span>             | <span data-ttu-id="e5181-654">không</span><span class="sxs-lookup"><span data-stu-id="e5181-654">no</span></span>           |
| <span data-ttu-id="e5181-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="e5181-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="e5181-656">không</span><span class="sxs-lookup"><span data-stu-id="e5181-656">no</span></span>             | <span data-ttu-id="e5181-657">không</span><span class="sxs-lookup"><span data-stu-id="e5181-657">no</span></span>           |
| <span data-ttu-id="e5181-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="e5181-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="e5181-659">không</span><span class="sxs-lookup"><span data-stu-id="e5181-659">no</span></span>             | <span data-ttu-id="e5181-660">không</span><span class="sxs-lookup"><span data-stu-id="e5181-660">no</span></span>           |
| <span data-ttu-id="e5181-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="e5181-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="e5181-662">không</span><span class="sxs-lookup"><span data-stu-id="e5181-662">no</span></span>             | <span data-ttu-id="e5181-663">không</span><span class="sxs-lookup"><span data-stu-id="e5181-663">no</span></span>           |
| <span data-ttu-id="e5181-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="e5181-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="e5181-665">không</span><span class="sxs-lookup"><span data-stu-id="e5181-665">no</span></span>             | <span data-ttu-id="e5181-666">không</span><span class="sxs-lookup"><span data-stu-id="e5181-666">no</span></span>           |
| <span data-ttu-id="e5181-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="e5181-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="e5181-668">không</span><span class="sxs-lookup"><span data-stu-id="e5181-668">no</span></span>             | <span data-ttu-id="e5181-669">không</span><span class="sxs-lookup"><span data-stu-id="e5181-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="e5181-670">Các giới hạn và vấn đề đã biết</span><span class="sxs-lookup"><span data-stu-id="e5181-670">Limitations and known issues</span></span>
<span data-ttu-id="e5181-671">Sau đây là danh sách các giới hạn và vấn đề đã biết:</span><span class="sxs-lookup"><span data-stu-id="e5181-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="e5181-672">Chỉ **Người dùng có giấy phép dự án của Microsoft** là có thể sử dụng API lịch trình.</span><span class="sxs-lookup"><span data-stu-id="e5181-672">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="e5181-673">Những đối tượng sau không thể sử dụng API lịch trình:</span><span class="sxs-lookup"><span data-stu-id="e5181-673">They can't be used by:</span></span>
    - <span data-ttu-id="e5181-674">Người dùng ứng dụng</span><span class="sxs-lookup"><span data-stu-id="e5181-674">Application users</span></span>
    - <span data-ttu-id="e5181-675">Người dùng hệ thống</span><span class="sxs-lookup"><span data-stu-id="e5181-675">System users</span></span>
    - <span data-ttu-id="e5181-676">Người dùng tích hợp</span><span class="sxs-lookup"><span data-stu-id="e5181-676">Integration users</span></span>
    - <span data-ttu-id="e5181-677">Những người dùng khác không có giấy phép bắt buộc</span><span class="sxs-lookup"><span data-stu-id="e5181-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="e5181-678">Mỗi **OperationSet** chỉ có thể có tối đa 100 thao tác.</span><span class="sxs-lookup"><span data-stu-id="e5181-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="e5181-679">Mỗi người dùng chỉ có tối đa 10 **OperationSets** đang mở.</span><span class="sxs-lookup"><span data-stu-id="e5181-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="e5181-680">Project Operations hiện hỗ trợ tổng cộng tối đa 500 nhiệm vụ trên một dự án.</span><span class="sxs-lookup"><span data-stu-id="e5181-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="e5181-681">Hiện không có nhật ký lỗi và trạng thái lỗi **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="e5181-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- <span data-ttu-id="e5181-682">API lịch trình ở Bản xem trước công khai.</span><span class="sxs-lookup"><span data-stu-id="e5181-682">Schedule APIs are in Public preview.</span></span> <span data-ttu-id="e5181-683">Microsoft không hỗ trợ sử dụng các API này trong Môi trường sản xuất.</span><span class="sxs-lookup"><span data-stu-id="e5181-683">Using these APIs in a Production environment isn't supported by Microsoft.</span></span>
- [<span data-ttu-id="e5181-684">Giới hạn và ranh giới đối với các dự án và nhiệm vụ</span><span class="sxs-lookup"><span data-stu-id="e5181-684">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="e5181-685">Xử lý lỗi</span><span class="sxs-lookup"><span data-stu-id="e5181-685">Error handling</span></span>

   - <span data-ttu-id="e5181-686">Để xem lại các lỗi được tạo từ Bộ hoạt động, hãy chuyển đến phần **Cài đặt** \> **Tích hợp lịch biểu** \> **Bộ hoạt động**.</span><span class="sxs-lookup"><span data-stu-id="e5181-686">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="e5181-687">Để xem lại các lỗi được tạo từ Dịch vụ lên lịch dự án, hãy chuyển đến phần **Cài đặt** \> **Tích hợp lịch biểu** \> **Nhật ký lỗi PSS**.</span><span class="sxs-lookup"><span data-stu-id="e5181-687">To review errors generated from the Project Scheduling Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="e5181-688">Kịch bản mẫu</span><span class="sxs-lookup"><span data-stu-id="e5181-688">Sample scenario</span></span>

<span data-ttu-id="e5181-689">Trong kịch bản này, bạn sẽ tạo một dự án, một thành viên nhóm, bốn nhiệm vụ và hai công việc giao cho nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="e5181-689">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="e5181-690">Tiếp theo, bạn sẽ cập nhật một nhiệm vụ, cập nhật dự án, xóa một nhiệm vụ, xóa một công việc giao cho nguồn lực và tạo một quan hệ phụ thuộc nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="e5181-690">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```csharp
Entity project = CreateProject();
project.Id = CallCreateProjectAction(project);
var projectReference = project.ToEntityReference();

var teamMember = new Entity("msdyn_projectteam", Guid.NewGuid());
teamMember["msdyn_name"] = $"TM {DateTime.Now.ToShortTimeString()}";
teamMember["msdyn_project"] = projectReference;
var createTeamMemberResponse = CallCreateTeamMemberAction(teamMember);

var description = $"My demo {DateTime.Now.ToShortTimeString()}";
var operationSetId = CallCreateOperationSetAction(project.Id, description);

var task1 = GetTask("1WW", projectReference);
var task2 = GetTask("2XX", projectReference, task1.ToEntityReference());
var task3 = GetTask("3YY", projectReference);
var task4 = GetTask("4ZZ", projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment("R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

var assignment1Response = CallPssCreateAction(assignment1, operationSetId);
var assignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

var assignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="e5181-691">Các mẫu khác</span><span class="sxs-lookup"><span data-stu-id="e5181-691">Additional samples</span></span>

```csharp
#region Call actions --- Sample code ----

/// <summary>
/// Calls the action to create an operationSet
/// </summary>
/// <param name="projectId">project id for the operations to be included in this operationSet</param>
/// <param name="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
private string CallCreateOperationSetAction(Guid projectId, string description)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_CreateOperationSetV1");
    operationSetRequest["ProjectId"] = projectId.ToString();
    operationSetRequest["Description"] = description;
    OrganizationResponse response = organizationService.Execute(operationSetRequest);
    return response["OperationSetId"].ToString();
}

/// <summary>
/// Calls the action to create an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>

private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssUpdateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssUpdateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="recordId">Id of the record to be deleted</param>
/// <param name="entityLogicalName">Entity logical name of the record</param>
/// <param name="operationSetId">OperationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssDeleteAction(string recordId, string entityLogicalName, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssDeleteV1");
    operationSetRequest["RecordId"] = recordId;
    operationSetRequest["EntityLogicalName"] = entityLogicalName;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to execute requests in an operationSet
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallExecuteOperationSetAction(string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_ExecuteOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// This can be used to abandon an operationSet that is no longer needed
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
protected OperationSetResponse CallAbandonOperationSetAction(Guid operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_AbandonOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId.ToString();
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}


/// <summary>
/// Calls the action to create a new project
/// </summary>
/// <param name="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1");
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);
    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <param name="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
private string CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject<OperationSetResponse>((string)orgResponse.Results["OperationSetResponse"]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet("msdyn_project", "msdyn_name");
    var getDefaultBucket = new QueryExpression("msdyn_projectbucket")
    {
        ColumnSet = columnsToFetch,
        Criteria =
        {
            Conditions =
            {
                new ConditionExpression("msdyn_project", ConditionOperator.Equal, projectReference.Id),
                new ConditionExpression("msdyn_name", ConditionOperator.Equal, "Bucket 1")
            }
        }
    };

    return organizationService.RetrieveMultiple(getDefaultBucket);
}

private Entity GetBucket(EntityReference projectReference)
{
    var bucketCollection = GetDefaultBucket(projectReference);
    if (bucketCollection.Entities.Count > 0)
    {
        return bucketCollection[0].ToEntity<Entity>();
    }

    throw new Exception($"Please open project with id {projectReference.Id} in the Dynamics UI and navigate to the Tasks tab");
}

private Entity CreateProject()
{
    var project = new Entity("msdyn_project", Guid.NewGuid());
    project["msdyn_subject"] = $"Proj {DateTime.Now.ToShortTimeString()}";

    return project;
}



private Entity GetTask(string name, EntityReference projectReference, EntityReference parentReference = null)
{
    var task = new Entity("msdyn_projecttask", Guid.NewGuid());
    task["msdyn_project"] = projectReference;
    task["msdyn_subject"] = name;
    task["msdyn_effort"] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
    task["new_custom1"] = "Just my test";
    task["new_age"] = 98;
    task["new_amount"] = 591.34m;
    task["new_isready"] = new OptionSetValue(100000000);
    */

    if (parentReference == null)
    {
        task["msdyn_outlinelevel"] = 1;
    }
    else
    {
        task["msdyn_parenttask"] = parentReference;
    }

    return task;
}

private Entity GetResourceAssignment(string name, Entity teamMember, Entity task, Entity project)
{
    var assignment = new Entity("msdyn_resourceassignment", Guid.NewGuid());
    assignment["msdyn_projectteamid"] = teamMember.ToEntityReference();
    assignment["msdyn_taskid"] = task.ToEntityReference();
    assignment["msdyn_projectid"] = project.ToEntityReference();
    assignment["msdyn_name"] = name;
    assignment["msdyn_start"] = DateTime.Now;
    assignment["msdyn_finish"] = DateTime.Now;

    return assignment;
}

protected Entity GetTaskDependency(Entity project, Entity predecessor, Entity successor)
{
    var taskDependency = new Entity("msdyn_projecttaskdependency", Guid.NewGuid());
    taskDependency["msdyn_project"] = project.ToEntityReference();
    taskDependency["msdyn_predecessortask"] = predecessor.ToEntityReference();
    taskDependency["msdyn_successortask"] = successor.ToEntityReference();
    taskDependency["msdyn_linktype"] = new OptionSetValue(192350000);

    return taskDependency;
}

#endregion


#region OperationSetResponse DataContract --- Sample code ----

[DataContract]
public class OperationSetResponse
{
[DataMember(Name = "operationSetId")]
public Guid OperationSetId { get; set; }

[DataMember(Name = "operationSetDetailId")]
public Guid OperationSetDetailId { get; set; }

[DataMember(Name = "operationType")]
public string OperationType { get; set; }

[DataMember(Name = "recordId")]
public string RecordId { get; set; }

[DataMember(Name = "correlationId")]
public string CorrelationId { get; set; }
}

#endregion
```
