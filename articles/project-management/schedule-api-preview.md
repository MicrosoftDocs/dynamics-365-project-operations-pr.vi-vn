---
title: Sử dụng API lịch trình để thực hiện các hoạt động với các thực thể Lập lịch trình
description: Chủ đề này cung cấp thông tin và mẫu để sử dụng API lịch trình.
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4a032dc7bcbdf23fce3c3b2ca63c51d473bd8e26
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116823"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="62c13-103">Sử dụng API lịch trình để thực hiện các hoạt động với các thực thể Lập lịch trình</span><span class="sxs-lookup"><span data-stu-id="62c13-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="62c13-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="62c13-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="62c13-105">Một số hoặc tất cả chức năng được ghi chú trong chủ đề này khả dụng như một phần của bản phát hành xem trước.</span><span class="sxs-lookup"><span data-stu-id="62c13-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="62c13-106">Nội dung và chức năng có thể thay đổi.</span><span class="sxs-lookup"><span data-stu-id="62c13-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="62c13-107">Thực thể lập lịch trình</span><span class="sxs-lookup"><span data-stu-id="62c13-107">Scheduling entities</span></span>

<span data-ttu-id="62c13-108">API lịch trình cung cấp khả năng thực hiện các thao tác tạo, cập nhật và xóa với **Thực thể lập lịch trình**.</span><span class="sxs-lookup"><span data-stu-id="62c13-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="62c13-109">Các thực thể này được quản lý thông qua công cụ Lập lịch trình trong Dự án cho web.</span><span class="sxs-lookup"><span data-stu-id="62c13-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="62c13-110">Các thao tác tạo, cập nhật và xóa với **Thực thể lập lịch trình** đã bị hạn chế trong các bản phát hành Dynamics 365 Project Operations trước đó.</span><span class="sxs-lookup"><span data-stu-id="62c13-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="62c13-111">Bảng sau cung cấp danh sách đầy đủ các **Thực thể lập lịch trình**.</span><span class="sxs-lookup"><span data-stu-id="62c13-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="62c13-112">Tên thực thể</span><span class="sxs-lookup"><span data-stu-id="62c13-112">Entity name</span></span>  | <span data-ttu-id="62c13-113">Tên logic của thực thể</span><span class="sxs-lookup"><span data-stu-id="62c13-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="62c13-114">Dự án</span><span class="sxs-lookup"><span data-stu-id="62c13-114">Project</span></span> | <span data-ttu-id="62c13-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="62c13-115">msdyn_project</span></span> |
| <span data-ttu-id="62c13-116">Nhiệm vụ dự án</span><span class="sxs-lookup"><span data-stu-id="62c13-116">Project Task</span></span>  | <span data-ttu-id="62c13-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="62c13-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="62c13-118">Quan hệ phụ thuộc Nhiệm vụ Dự án</span><span class="sxs-lookup"><span data-stu-id="62c13-118">Project Task Dependency</span></span>  | <span data-ttu-id="62c13-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="62c13-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="62c13-120">Gán Nguồn lực</span><span class="sxs-lookup"><span data-stu-id="62c13-120">Resource Assignment</span></span> | <span data-ttu-id="62c13-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="62c13-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="62c13-122">Bộ chứa Dự án</span><span class="sxs-lookup"><span data-stu-id="62c13-122">Project Bucket</span></span>  | <span data-ttu-id="62c13-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="62c13-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="62c13-124">Thành viên Nhóm Dự án</span><span class="sxs-lookup"><span data-stu-id="62c13-124">Project Team Member</span></span> | <span data-ttu-id="62c13-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="62c13-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="62c13-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="62c13-126">OperationSet</span></span>

<span data-ttu-id="62c13-127">OperationSet là một mẫu đơn vị công việc có thể được sử dụng khi phải xử lý một số yêu cầu tác động lên lịch trình trong một giao dịch.</span><span class="sxs-lookup"><span data-stu-id="62c13-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="62c13-128">API lịch trình</span><span class="sxs-lookup"><span data-stu-id="62c13-128">Schedule APIs</span></span>

<span data-ttu-id="62c13-129">Sau đây là danh sách các API lịch trình hiện tại.</span><span class="sxs-lookup"><span data-stu-id="62c13-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="62c13-130">**msdyn_CreateProjectV1**: API này có thể được dùng để tạo một dự án.</span><span class="sxs-lookup"><span data-stu-id="62c13-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="62c13-131">Nhóm dự án và dự án mặc định được tạo ngay lập tức.</span><span class="sxs-lookup"><span data-stu-id="62c13-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="62c13-132">**msdyn_CreateTeamMemberV1**: API này có thể được dùng để tạo một thành viên trong nhóm dự án.</span><span class="sxs-lookup"><span data-stu-id="62c13-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="62c13-133">Hồ sơ thành viên trong nhóm được tạo ngay lập tức.</span><span class="sxs-lookup"><span data-stu-id="62c13-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="62c13-134">**msdyn_CreateOperationSetV1**: API này có thể được dùng để lập lịch trình một số yêu cầu phải được thực hiện trong một giao dịch.</span><span class="sxs-lookup"><span data-stu-id="62c13-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="62c13-135">**msdyn_PSSCreateV1**: API này có thể được dùng để tạo một thực thể.</span><span class="sxs-lookup"><span data-stu-id="62c13-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="62c13-136">Thực thể có thể là bất kỳ thực thể Lập lịch trình nào hỗ trợ thao tác tạo.</span><span class="sxs-lookup"><span data-stu-id="62c13-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="62c13-137">**msdyn_PSSUpdateV1**: API này có thể được dùng để cập nhật một thực thể.</span><span class="sxs-lookup"><span data-stu-id="62c13-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="62c13-138">Thực thể có thể là bất kỳ thực thể Lập lịch trình nào hỗ trợ thao tác cập nhật.</span><span class="sxs-lookup"><span data-stu-id="62c13-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="62c13-139">**msdyn_PSSDeleteV1**: API này có thể được dùng để xóa một thực thể.</span><span class="sxs-lookup"><span data-stu-id="62c13-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="62c13-140">Thực thể có thể là bất kỳ thực thể Lập lịch trình nào hỗ trợ thao tác xóa.</span><span class="sxs-lookup"><span data-stu-id="62c13-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="62c13-141">**msdyn_ExecuteOperationSetV1**: API này được dùng để thực thi tất cả các thao tác trong nhóm thao tác nhất định.</span><span class="sxs-lookup"><span data-stu-id="62c13-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="62c13-142">Sử dụng API lịch trình với OperationSet</span><span class="sxs-lookup"><span data-stu-id="62c13-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="62c13-143">Bởi vì bản ghi có cả **CreateProjectV1** và **CreateTeamMemberV1** được tạo ngay lập tức, nên không thể dùng các API này trực tiếp trong **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="62c13-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="62c13-144">Tuy nhiên, bạn có thể sử dụng API để tạo các bản ghi cần thiết, tạo một **OperationSet**, sau đó sử dụng các bản ghi được tạo trước này trong **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="62c13-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="62c13-145">Thao tác được hỗ trợ</span><span class="sxs-lookup"><span data-stu-id="62c13-145">Supported operations</span></span>

| <span data-ttu-id="62c13-146">Thực thể lập lịch trình</span><span class="sxs-lookup"><span data-stu-id="62c13-146">Scheduling entity</span></span> | <span data-ttu-id="62c13-147">Tạo</span><span class="sxs-lookup"><span data-stu-id="62c13-147">Create</span></span> | <span data-ttu-id="62c13-148">Update</span><span class="sxs-lookup"><span data-stu-id="62c13-148">Update</span></span> | <span data-ttu-id="62c13-149">Delete</span><span class="sxs-lookup"><span data-stu-id="62c13-149">Delete</span></span> | <span data-ttu-id="62c13-150">Những điều quan trọng cần cân nhắc</span><span class="sxs-lookup"><span data-stu-id="62c13-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="62c13-151">Nhiệm vụ dự án</span><span class="sxs-lookup"><span data-stu-id="62c13-151">Project task</span></span> | <span data-ttu-id="62c13-152">Có</span><span class="sxs-lookup"><span data-stu-id="62c13-152">Yes</span></span> | <span data-ttu-id="62c13-153">Có</span><span class="sxs-lookup"><span data-stu-id="62c13-153">Yes</span></span> | <span data-ttu-id="62c13-154">Có</span><span class="sxs-lookup"><span data-stu-id="62c13-154">Yes</span></span> | <span data-ttu-id="62c13-155">Không có</span><span class="sxs-lookup"><span data-stu-id="62c13-155">None</span></span> |
| <span data-ttu-id="62c13-156">Quan hệ phụ thuộc nhiệm vụ dự án</span><span class="sxs-lookup"><span data-stu-id="62c13-156">Project task dependency</span></span> | <span data-ttu-id="62c13-157">Có</span><span class="sxs-lookup"><span data-stu-id="62c13-157">Yes</span></span> | <span data-ttu-id="62c13-158">Có</span><span class="sxs-lookup"><span data-stu-id="62c13-158">Yes</span></span> | | <span data-ttu-id="62c13-159">Bản ghi quan hệ phụ thuộc nhiệm vụ dự án không được cập nhật.</span><span class="sxs-lookup"><span data-stu-id="62c13-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="62c13-160">Thay vào đó, một bản ghi cũ có thể bị xóa và một bản ghi mới có thể được tạo.</span><span class="sxs-lookup"><span data-stu-id="62c13-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="62c13-161">Công việc giao cho nguồn lực</span><span class="sxs-lookup"><span data-stu-id="62c13-161">Resource assignment</span></span> | <span data-ttu-id="62c13-162">Có</span><span class="sxs-lookup"><span data-stu-id="62c13-162">Yes</span></span> | <span data-ttu-id="62c13-163">Có</span><span class="sxs-lookup"><span data-stu-id="62c13-163">Yes</span></span> | | <span data-ttu-id="62c13-164">Không hỗ trợ thao tác với các trường sau: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** và **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="62c13-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="62c13-165">Bản ghi việc được giao không được cập nhật.</span><span class="sxs-lookup"><span data-stu-id="62c13-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="62c13-166">Thay vào đó, một bản ghi cũ có thể bị xóa và một bản ghi mới có thể được tạo.</span><span class="sxs-lookup"><span data-stu-id="62c13-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="62c13-167">Nhóm dự án</span><span class="sxs-lookup"><span data-stu-id="62c13-167">Project bucket</span></span> | <span data-ttu-id="62c13-168">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="62c13-168">N/A</span></span> | <span data-ttu-id="62c13-169">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="62c13-169">N/A</span></span> | <span data-ttu-id="62c13-170">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="62c13-170">N/A</span></span> | <span data-ttu-id="62c13-171">Nhóm mặc định được tạo bằng cách sử dụng API **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="62c13-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="62c13-172">Thành viên nhóm dự án</span><span class="sxs-lookup"><span data-stu-id="62c13-172">Project team member</span></span> | <span data-ttu-id="62c13-173">Có</span><span class="sxs-lookup"><span data-stu-id="62c13-173">Yes</span></span> | <span data-ttu-id="62c13-174">Có</span><span class="sxs-lookup"><span data-stu-id="62c13-174">Yes</span></span> | <span data-ttu-id="62c13-175">Có</span><span class="sxs-lookup"><span data-stu-id="62c13-175">Yes</span></span> | <span data-ttu-id="62c13-176">Đối với thao tác tạo, hãy sử dụng API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="62c13-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="62c13-177">Dự án</span><span class="sxs-lookup"><span data-stu-id="62c13-177">Project</span></span> | <span data-ttu-id="62c13-178">Có</span><span class="sxs-lookup"><span data-stu-id="62c13-178">Yes</span></span> | <span data-ttu-id="62c13-179">Có</span><span class="sxs-lookup"><span data-stu-id="62c13-179">Yes</span></span> | <span data-ttu-id="62c13-180">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="62c13-180">N/A</span></span> | <span data-ttu-id="62c13-181">Không hỗ trợ thao tác với các trường sau: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** và **Duration**.</span><span class="sxs-lookup"><span data-stu-id="62c13-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="62c13-182">Các API này có thể được gọi ra với các đối tượng thực thể bao gồm các trường tùy chỉnh.</span><span class="sxs-lookup"><span data-stu-id="62c13-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="62c13-183">Thuộc tính ID là không bắt buộc.</span><span class="sxs-lookup"><span data-stu-id="62c13-183">The ID property is optional.</span></span> <span data-ttu-id="62c13-184">Nếu được cung cấp, hệ thống sẽ cố gắng sử dụng ID thuộc tính và đưa ra một ngoại lệ nếu không thể sử dụng.</span><span class="sxs-lookup"><span data-stu-id="62c13-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="62c13-185">Nếu không được cung cấp, hệ thống sẽ tạo ID thuộc tính.</span><span class="sxs-lookup"><span data-stu-id="62c13-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="62c13-186">Các trường bị hạn chế</span><span class="sxs-lookup"><span data-stu-id="62c13-186">Restricted fields</span></span>

<span data-ttu-id="62c13-187">Các bảng sau xác định các trường bị hạn chế trong **Tạo** và **Chỉnh sửa**.</span><span class="sxs-lookup"><span data-stu-id="62c13-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="62c13-188">Nhiệm vụ dự án</span><span class="sxs-lookup"><span data-stu-id="62c13-188">Project task</span></span>

| <span data-ttu-id="62c13-189">**Tên lô-gic**</span><span class="sxs-lookup"><span data-stu-id="62c13-189">**Logical name**</span></span>                       | <span data-ttu-id="62c13-190">**Có thể tạo**</span><span class="sxs-lookup"><span data-stu-id="62c13-190">**Can create**</span></span> | <span data-ttu-id="62c13-191">**Có thể chỉnh sửa**</span><span class="sxs-lookup"><span data-stu-id="62c13-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="62c13-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="62c13-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="62c13-193">không</span><span class="sxs-lookup"><span data-stu-id="62c13-193">no</span></span>             | <span data-ttu-id="62c13-194">không</span><span class="sxs-lookup"><span data-stu-id="62c13-194">no</span></span>               |
| <span data-ttu-id="62c13-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="62c13-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="62c13-196">không</span><span class="sxs-lookup"><span data-stu-id="62c13-196">no</span></span>             | <span data-ttu-id="62c13-197">không</span><span class="sxs-lookup"><span data-stu-id="62c13-197">no</span></span>               |
| <span data-ttu-id="62c13-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="62c13-198">msdyn_actualend</span></span>                        | <span data-ttu-id="62c13-199">không</span><span class="sxs-lookup"><span data-stu-id="62c13-199">no</span></span>             | <span data-ttu-id="62c13-200">không</span><span class="sxs-lookup"><span data-stu-id="62c13-200">no</span></span>               |
| <span data-ttu-id="62c13-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="62c13-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="62c13-202">không</span><span class="sxs-lookup"><span data-stu-id="62c13-202">no</span></span>             | <span data-ttu-id="62c13-203">không</span><span class="sxs-lookup"><span data-stu-id="62c13-203">no</span></span>               |
| <span data-ttu-id="62c13-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="62c13-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="62c13-205">không</span><span class="sxs-lookup"><span data-stu-id="62c13-205">no</span></span>             | <span data-ttu-id="62c13-206">không</span><span class="sxs-lookup"><span data-stu-id="62c13-206">no</span></span>               |
| <span data-ttu-id="62c13-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="62c13-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="62c13-208">không</span><span class="sxs-lookup"><span data-stu-id="62c13-208">no</span></span>             | <span data-ttu-id="62c13-209">không</span><span class="sxs-lookup"><span data-stu-id="62c13-209">no</span></span>               |
| <span data-ttu-id="62c13-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="62c13-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="62c13-211">không</span><span class="sxs-lookup"><span data-stu-id="62c13-211">no</span></span>             | <span data-ttu-id="62c13-212">không</span><span class="sxs-lookup"><span data-stu-id="62c13-212">no</span></span>               |
| <span data-ttu-id="62c13-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="62c13-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="62c13-214">không</span><span class="sxs-lookup"><span data-stu-id="62c13-214">no</span></span>             | <span data-ttu-id="62c13-215">không</span><span class="sxs-lookup"><span data-stu-id="62c13-215">no</span></span>               |
| <span data-ttu-id="62c13-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="62c13-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="62c13-217">không</span><span class="sxs-lookup"><span data-stu-id="62c13-217">no</span></span>             | <span data-ttu-id="62c13-218">không</span><span class="sxs-lookup"><span data-stu-id="62c13-218">no</span></span>               |
| <span data-ttu-id="62c13-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="62c13-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="62c13-220">không</span><span class="sxs-lookup"><span data-stu-id="62c13-220">no</span></span>             | <span data-ttu-id="62c13-221">không</span><span class="sxs-lookup"><span data-stu-id="62c13-221">no</span></span>               |
| <span data-ttu-id="62c13-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="62c13-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="62c13-223">không</span><span class="sxs-lookup"><span data-stu-id="62c13-223">no</span></span>             | <span data-ttu-id="62c13-224">không</span><span class="sxs-lookup"><span data-stu-id="62c13-224">no</span></span>               |
| <span data-ttu-id="62c13-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="62c13-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="62c13-226">không</span><span class="sxs-lookup"><span data-stu-id="62c13-226">no</span></span>             | <span data-ttu-id="62c13-227">không</span><span class="sxs-lookup"><span data-stu-id="62c13-227">no</span></span>               |
| <span data-ttu-id="62c13-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="62c13-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="62c13-229">không</span><span class="sxs-lookup"><span data-stu-id="62c13-229">no</span></span>             | <span data-ttu-id="62c13-230">không</span><span class="sxs-lookup"><span data-stu-id="62c13-230">no</span></span>               |
| <span data-ttu-id="62c13-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="62c13-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="62c13-232">không</span><span class="sxs-lookup"><span data-stu-id="62c13-232">no</span></span>             | <span data-ttu-id="62c13-233">không</span><span class="sxs-lookup"><span data-stu-id="62c13-233">no</span></span>               |
| <span data-ttu-id="62c13-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="62c13-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="62c13-235">không</span><span class="sxs-lookup"><span data-stu-id="62c13-235">no</span></span>             | <span data-ttu-id="62c13-236">không</span><span class="sxs-lookup"><span data-stu-id="62c13-236">no</span></span>               |
| <span data-ttu-id="62c13-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="62c13-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="62c13-238">không</span><span class="sxs-lookup"><span data-stu-id="62c13-238">no</span></span>             | <span data-ttu-id="62c13-239">không</span><span class="sxs-lookup"><span data-stu-id="62c13-239">no</span></span>               |
| <span data-ttu-id="62c13-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="62c13-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="62c13-241">không</span><span class="sxs-lookup"><span data-stu-id="62c13-241">no</span></span>             | <span data-ttu-id="62c13-242">không</span><span class="sxs-lookup"><span data-stu-id="62c13-242">no</span></span>               |
| <span data-ttu-id="62c13-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="62c13-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="62c13-244">không</span><span class="sxs-lookup"><span data-stu-id="62c13-244">no</span></span>             | <span data-ttu-id="62c13-245">không</span><span class="sxs-lookup"><span data-stu-id="62c13-245">no</span></span>               |
| <span data-ttu-id="62c13-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="62c13-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="62c13-247">không</span><span class="sxs-lookup"><span data-stu-id="62c13-247">no</span></span>             | <span data-ttu-id="62c13-248">không</span><span class="sxs-lookup"><span data-stu-id="62c13-248">no</span></span>               |
| <span data-ttu-id="62c13-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="62c13-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="62c13-250">không</span><span class="sxs-lookup"><span data-stu-id="62c13-250">no</span></span>             | <span data-ttu-id="62c13-251">không</span><span class="sxs-lookup"><span data-stu-id="62c13-251">no</span></span>               |
| <span data-ttu-id="62c13-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="62c13-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="62c13-253">không</span><span class="sxs-lookup"><span data-stu-id="62c13-253">no</span></span>             | <span data-ttu-id="62c13-254">không</span><span class="sxs-lookup"><span data-stu-id="62c13-254">no</span></span>               |
| <span data-ttu-id="62c13-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="62c13-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="62c13-256">không</span><span class="sxs-lookup"><span data-stu-id="62c13-256">no</span></span>             | <span data-ttu-id="62c13-257">không</span><span class="sxs-lookup"><span data-stu-id="62c13-257">no</span></span>               |
| <span data-ttu-id="62c13-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="62c13-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="62c13-259">không</span><span class="sxs-lookup"><span data-stu-id="62c13-259">no</span></span>             | <span data-ttu-id="62c13-260">không</span><span class="sxs-lookup"><span data-stu-id="62c13-260">no</span></span>               |
| <span data-ttu-id="62c13-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="62c13-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="62c13-262">không</span><span class="sxs-lookup"><span data-stu-id="62c13-262">no</span></span>             | <span data-ttu-id="62c13-263">không</span><span class="sxs-lookup"><span data-stu-id="62c13-263">no</span></span>               |
| <span data-ttu-id="62c13-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="62c13-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="62c13-265">không</span><span class="sxs-lookup"><span data-stu-id="62c13-265">no</span></span>             | <span data-ttu-id="62c13-266">không</span><span class="sxs-lookup"><span data-stu-id="62c13-266">no</span></span>               |
| <span data-ttu-id="62c13-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="62c13-267">msdyn_progress</span></span>                         | <span data-ttu-id="62c13-268">không</span><span class="sxs-lookup"><span data-stu-id="62c13-268">no</span></span>             | <span data-ttu-id="62c13-269">không (có cho P4W)</span><span class="sxs-lookup"><span data-stu-id="62c13-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="62c13-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="62c13-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="62c13-271">không</span><span class="sxs-lookup"><span data-stu-id="62c13-271">no</span></span>             | <span data-ttu-id="62c13-272">không</span><span class="sxs-lookup"><span data-stu-id="62c13-272">no</span></span>               |
| <span data-ttu-id="62c13-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="62c13-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="62c13-274">không</span><span class="sxs-lookup"><span data-stu-id="62c13-274">no</span></span>             | <span data-ttu-id="62c13-275">không</span><span class="sxs-lookup"><span data-stu-id="62c13-275">no</span></span>               |
| <span data-ttu-id="62c13-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="62c13-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="62c13-277">không</span><span class="sxs-lookup"><span data-stu-id="62c13-277">no</span></span>             | <span data-ttu-id="62c13-278">không</span><span class="sxs-lookup"><span data-stu-id="62c13-278">no</span></span>               |
| <span data-ttu-id="62c13-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="62c13-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="62c13-280">không</span><span class="sxs-lookup"><span data-stu-id="62c13-280">no</span></span>             | <span data-ttu-id="62c13-281">không</span><span class="sxs-lookup"><span data-stu-id="62c13-281">no</span></span>               |
| <span data-ttu-id="62c13-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="62c13-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="62c13-283">không</span><span class="sxs-lookup"><span data-stu-id="62c13-283">no</span></span>             | <span data-ttu-id="62c13-284">không</span><span class="sxs-lookup"><span data-stu-id="62c13-284">no</span></span>               |
| <span data-ttu-id="62c13-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="62c13-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="62c13-286">không</span><span class="sxs-lookup"><span data-stu-id="62c13-286">no</span></span>             | <span data-ttu-id="62c13-287">không</span><span class="sxs-lookup"><span data-stu-id="62c13-287">no</span></span>               |
| <span data-ttu-id="62c13-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="62c13-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="62c13-289">không</span><span class="sxs-lookup"><span data-stu-id="62c13-289">no</span></span>             | <span data-ttu-id="62c13-290">không</span><span class="sxs-lookup"><span data-stu-id="62c13-290">no</span></span>               |
| <span data-ttu-id="62c13-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="62c13-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="62c13-292">không</span><span class="sxs-lookup"><span data-stu-id="62c13-292">no</span></span>             | <span data-ttu-id="62c13-293">không</span><span class="sxs-lookup"><span data-stu-id="62c13-293">no</span></span>               |
| <span data-ttu-id="62c13-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="62c13-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="62c13-295">không</span><span class="sxs-lookup"><span data-stu-id="62c13-295">no</span></span>             | <span data-ttu-id="62c13-296">không</span><span class="sxs-lookup"><span data-stu-id="62c13-296">no</span></span>               |
| <span data-ttu-id="62c13-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="62c13-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="62c13-298">không</span><span class="sxs-lookup"><span data-stu-id="62c13-298">no</span></span>             | <span data-ttu-id="62c13-299">không</span><span class="sxs-lookup"><span data-stu-id="62c13-299">no</span></span>               |
| <span data-ttu-id="62c13-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="62c13-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="62c13-301">không</span><span class="sxs-lookup"><span data-stu-id="62c13-301">no</span></span>             | <span data-ttu-id="62c13-302">không</span><span class="sxs-lookup"><span data-stu-id="62c13-302">no</span></span>               |
| <span data-ttu-id="62c13-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="62c13-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="62c13-304">không</span><span class="sxs-lookup"><span data-stu-id="62c13-304">no</span></span>             | <span data-ttu-id="62c13-305">không</span><span class="sxs-lookup"><span data-stu-id="62c13-305">no</span></span>               |
| <span data-ttu-id="62c13-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="62c13-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="62c13-307">không</span><span class="sxs-lookup"><span data-stu-id="62c13-307">no</span></span>             | <span data-ttu-id="62c13-308">không</span><span class="sxs-lookup"><span data-stu-id="62c13-308">no</span></span>               |
| <span data-ttu-id="62c13-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="62c13-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="62c13-310">không</span><span class="sxs-lookup"><span data-stu-id="62c13-310">no</span></span>             | <span data-ttu-id="62c13-311">không</span><span class="sxs-lookup"><span data-stu-id="62c13-311">no</span></span>               |
| <span data-ttu-id="62c13-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="62c13-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="62c13-313">không</span><span class="sxs-lookup"><span data-stu-id="62c13-313">no</span></span>             | <span data-ttu-id="62c13-314">không</span><span class="sxs-lookup"><span data-stu-id="62c13-314">no</span></span>               |
| <span data-ttu-id="62c13-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="62c13-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="62c13-316">không</span><span class="sxs-lookup"><span data-stu-id="62c13-316">no</span></span>             | <span data-ttu-id="62c13-317">không</span><span class="sxs-lookup"><span data-stu-id="62c13-317">no</span></span>               |
| <span data-ttu-id="62c13-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="62c13-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="62c13-319">không</span><span class="sxs-lookup"><span data-stu-id="62c13-319">no</span></span>             | <span data-ttu-id="62c13-320">không</span><span class="sxs-lookup"><span data-stu-id="62c13-320">no</span></span>               |
| <span data-ttu-id="62c13-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="62c13-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="62c13-322">không</span><span class="sxs-lookup"><span data-stu-id="62c13-322">no</span></span>             | <span data-ttu-id="62c13-323">không</span><span class="sxs-lookup"><span data-stu-id="62c13-323">no</span></span>               |
| <span data-ttu-id="62c13-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="62c13-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="62c13-325">không</span><span class="sxs-lookup"><span data-stu-id="62c13-325">no</span></span>             | <span data-ttu-id="62c13-326">không</span><span class="sxs-lookup"><span data-stu-id="62c13-326">no</span></span>               |
| <span data-ttu-id="62c13-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="62c13-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="62c13-328">không</span><span class="sxs-lookup"><span data-stu-id="62c13-328">no</span></span>             | <span data-ttu-id="62c13-329">không</span><span class="sxs-lookup"><span data-stu-id="62c13-329">no</span></span>               |
| <span data-ttu-id="62c13-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="62c13-330">msdyn_summary</span></span>                          | <span data-ttu-id="62c13-331">không</span><span class="sxs-lookup"><span data-stu-id="62c13-331">no</span></span>             | <span data-ttu-id="62c13-332">không</span><span class="sxs-lookup"><span data-stu-id="62c13-332">no</span></span>               |
| <span data-ttu-id="62c13-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="62c13-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="62c13-334">không</span><span class="sxs-lookup"><span data-stu-id="62c13-334">no</span></span>             | <span data-ttu-id="62c13-335">không</span><span class="sxs-lookup"><span data-stu-id="62c13-335">no</span></span>               |
| <span data-ttu-id="62c13-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="62c13-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="62c13-337">không</span><span class="sxs-lookup"><span data-stu-id="62c13-337">no</span></span>             | <span data-ttu-id="62c13-338">không</span><span class="sxs-lookup"><span data-stu-id="62c13-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="62c13-339">Quan hệ phụ thuộc nhiệm vụ dự án</span><span class="sxs-lookup"><span data-stu-id="62c13-339">Project task dependency</span></span>

| <span data-ttu-id="62c13-340">**Tên lô-gic**</span><span class="sxs-lookup"><span data-stu-id="62c13-340">**Logical name**</span></span>              | <span data-ttu-id="62c13-341">**Có thể tạo**</span><span class="sxs-lookup"><span data-stu-id="62c13-341">**Can create**</span></span> | <span data-ttu-id="62c13-342">**Có thể chỉnh sửa**</span><span class="sxs-lookup"><span data-stu-id="62c13-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="62c13-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="62c13-343">msdyn_linktype</span></span>                | <span data-ttu-id="62c13-344">không</span><span class="sxs-lookup"><span data-stu-id="62c13-344">no</span></span>             | <span data-ttu-id="62c13-345">không</span><span class="sxs-lookup"><span data-stu-id="62c13-345">no</span></span>           |
| <span data-ttu-id="62c13-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="62c13-346">msdyn_linktypename</span></span>            | <span data-ttu-id="62c13-347">không</span><span class="sxs-lookup"><span data-stu-id="62c13-347">no</span></span>             | <span data-ttu-id="62c13-348">không</span><span class="sxs-lookup"><span data-stu-id="62c13-348">no</span></span>           |
| <span data-ttu-id="62c13-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="62c13-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="62c13-350">có</span><span class="sxs-lookup"><span data-stu-id="62c13-350">yes</span></span>            | <span data-ttu-id="62c13-351">không</span><span class="sxs-lookup"><span data-stu-id="62c13-351">no</span></span>           |
| <span data-ttu-id="62c13-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="62c13-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="62c13-353">có</span><span class="sxs-lookup"><span data-stu-id="62c13-353">yes</span></span>            | <span data-ttu-id="62c13-354">không</span><span class="sxs-lookup"><span data-stu-id="62c13-354">no</span></span>           |
| <span data-ttu-id="62c13-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="62c13-355">msdyn_project</span></span>                 | <span data-ttu-id="62c13-356">có</span><span class="sxs-lookup"><span data-stu-id="62c13-356">yes</span></span>            | <span data-ttu-id="62c13-357">không</span><span class="sxs-lookup"><span data-stu-id="62c13-357">no</span></span>           |
| <span data-ttu-id="62c13-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="62c13-358">msdyn_projectname</span></span>             | <span data-ttu-id="62c13-359">có</span><span class="sxs-lookup"><span data-stu-id="62c13-359">yes</span></span>            | <span data-ttu-id="62c13-360">không</span><span class="sxs-lookup"><span data-stu-id="62c13-360">no</span></span>           |
| <span data-ttu-id="62c13-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="62c13-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="62c13-362">có</span><span class="sxs-lookup"><span data-stu-id="62c13-362">yes</span></span>            | <span data-ttu-id="62c13-363">không</span><span class="sxs-lookup"><span data-stu-id="62c13-363">no</span></span>           |
| <span data-ttu-id="62c13-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="62c13-364">msdyn_successortask</span></span>           | <span data-ttu-id="62c13-365">có</span><span class="sxs-lookup"><span data-stu-id="62c13-365">yes</span></span>            | <span data-ttu-id="62c13-366">không</span><span class="sxs-lookup"><span data-stu-id="62c13-366">no</span></span>           |
| <span data-ttu-id="62c13-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="62c13-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="62c13-368">có</span><span class="sxs-lookup"><span data-stu-id="62c13-368">yes</span></span>            | <span data-ttu-id="62c13-369">không</span><span class="sxs-lookup"><span data-stu-id="62c13-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="62c13-370">Công việc giao cho nguồn lực</span><span class="sxs-lookup"><span data-stu-id="62c13-370">Resource assignment</span></span>

| <span data-ttu-id="62c13-371">**Tên lô-gic**</span><span class="sxs-lookup"><span data-stu-id="62c13-371">**Logical name**</span></span>             | <span data-ttu-id="62c13-372">**Có thể tạo**</span><span class="sxs-lookup"><span data-stu-id="62c13-372">**Can create**</span></span> | <span data-ttu-id="62c13-373">**Có thể chỉnh sửa**</span><span class="sxs-lookup"><span data-stu-id="62c13-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="62c13-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="62c13-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="62c13-375">có</span><span class="sxs-lookup"><span data-stu-id="62c13-375">yes</span></span>            | <span data-ttu-id="62c13-376">không</span><span class="sxs-lookup"><span data-stu-id="62c13-376">no</span></span>           |
| <span data-ttu-id="62c13-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="62c13-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="62c13-378">có</span><span class="sxs-lookup"><span data-stu-id="62c13-378">yes</span></span>            | <span data-ttu-id="62c13-379">không</span><span class="sxs-lookup"><span data-stu-id="62c13-379">no</span></span>           |
| <span data-ttu-id="62c13-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="62c13-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="62c13-381">không</span><span class="sxs-lookup"><span data-stu-id="62c13-381">no</span></span>             | <span data-ttu-id="62c13-382">không</span><span class="sxs-lookup"><span data-stu-id="62c13-382">no</span></span>           |
| <span data-ttu-id="62c13-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="62c13-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="62c13-384">không</span><span class="sxs-lookup"><span data-stu-id="62c13-384">no</span></span>             | <span data-ttu-id="62c13-385">không</span><span class="sxs-lookup"><span data-stu-id="62c13-385">no</span></span>           |
| <span data-ttu-id="62c13-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="62c13-386">msdyn_committype</span></span>             | <span data-ttu-id="62c13-387">không</span><span class="sxs-lookup"><span data-stu-id="62c13-387">no</span></span>             | <span data-ttu-id="62c13-388">không</span><span class="sxs-lookup"><span data-stu-id="62c13-388">no</span></span>           |
| <span data-ttu-id="62c13-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="62c13-389">msdyn_committypename</span></span>         | <span data-ttu-id="62c13-390">không</span><span class="sxs-lookup"><span data-stu-id="62c13-390">no</span></span>             | <span data-ttu-id="62c13-391">không</span><span class="sxs-lookup"><span data-stu-id="62c13-391">no</span></span>           |
| <span data-ttu-id="62c13-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="62c13-392">msdyn_effort</span></span>                 | <span data-ttu-id="62c13-393">không</span><span class="sxs-lookup"><span data-stu-id="62c13-393">no</span></span>             | <span data-ttu-id="62c13-394">không</span><span class="sxs-lookup"><span data-stu-id="62c13-394">no</span></span>           |
| <span data-ttu-id="62c13-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="62c13-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="62c13-396">không</span><span class="sxs-lookup"><span data-stu-id="62c13-396">no</span></span>             | <span data-ttu-id="62c13-397">không</span><span class="sxs-lookup"><span data-stu-id="62c13-397">no</span></span>           |
| <span data-ttu-id="62c13-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="62c13-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="62c13-399">không</span><span class="sxs-lookup"><span data-stu-id="62c13-399">no</span></span>             | <span data-ttu-id="62c13-400">không</span><span class="sxs-lookup"><span data-stu-id="62c13-400">no</span></span>           |
| <span data-ttu-id="62c13-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="62c13-401">msdyn_finish</span></span>                 | <span data-ttu-id="62c13-402">không</span><span class="sxs-lookup"><span data-stu-id="62c13-402">no</span></span>             | <span data-ttu-id="62c13-403">không</span><span class="sxs-lookup"><span data-stu-id="62c13-403">no</span></span>           |
| <span data-ttu-id="62c13-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="62c13-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="62c13-405">không</span><span class="sxs-lookup"><span data-stu-id="62c13-405">no</span></span>             | <span data-ttu-id="62c13-406">không</span><span class="sxs-lookup"><span data-stu-id="62c13-406">no</span></span>           |
| <span data-ttu-id="62c13-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="62c13-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="62c13-408">không</span><span class="sxs-lookup"><span data-stu-id="62c13-408">no</span></span>             | <span data-ttu-id="62c13-409">không</span><span class="sxs-lookup"><span data-stu-id="62c13-409">no</span></span>           |
| <span data-ttu-id="62c13-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="62c13-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="62c13-411">không</span><span class="sxs-lookup"><span data-stu-id="62c13-411">no</span></span>             | <span data-ttu-id="62c13-412">không</span><span class="sxs-lookup"><span data-stu-id="62c13-412">no</span></span>           |
| <span data-ttu-id="62c13-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="62c13-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="62c13-414">không</span><span class="sxs-lookup"><span data-stu-id="62c13-414">no</span></span>             | <span data-ttu-id="62c13-415">không</span><span class="sxs-lookup"><span data-stu-id="62c13-415">no</span></span>           |
| <span data-ttu-id="62c13-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="62c13-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="62c13-417">không</span><span class="sxs-lookup"><span data-stu-id="62c13-417">no</span></span>             | <span data-ttu-id="62c13-418">không</span><span class="sxs-lookup"><span data-stu-id="62c13-418">no</span></span>           |
| <span data-ttu-id="62c13-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="62c13-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="62c13-420">không</span><span class="sxs-lookup"><span data-stu-id="62c13-420">no</span></span>             | <span data-ttu-id="62c13-421">không</span><span class="sxs-lookup"><span data-stu-id="62c13-421">no</span></span>           |
| <span data-ttu-id="62c13-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="62c13-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="62c13-423">không</span><span class="sxs-lookup"><span data-stu-id="62c13-423">no</span></span>             | <span data-ttu-id="62c13-424">không</span><span class="sxs-lookup"><span data-stu-id="62c13-424">no</span></span>           |
| <span data-ttu-id="62c13-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="62c13-425">msdyn_projectid</span></span>              | <span data-ttu-id="62c13-426">có</span><span class="sxs-lookup"><span data-stu-id="62c13-426">yes</span></span>            | <span data-ttu-id="62c13-427">không</span><span class="sxs-lookup"><span data-stu-id="62c13-427">no</span></span>           |
| <span data-ttu-id="62c13-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="62c13-428">msdyn_projectidname</span></span>          | <span data-ttu-id="62c13-429">không</span><span class="sxs-lookup"><span data-stu-id="62c13-429">no</span></span>             | <span data-ttu-id="62c13-430">không</span><span class="sxs-lookup"><span data-stu-id="62c13-430">no</span></span>           |
| <span data-ttu-id="62c13-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="62c13-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="62c13-432">không</span><span class="sxs-lookup"><span data-stu-id="62c13-432">no</span></span>             | <span data-ttu-id="62c13-433">không</span><span class="sxs-lookup"><span data-stu-id="62c13-433">no</span></span>           |
| <span data-ttu-id="62c13-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="62c13-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="62c13-435">không</span><span class="sxs-lookup"><span data-stu-id="62c13-435">no</span></span>             | <span data-ttu-id="62c13-436">không</span><span class="sxs-lookup"><span data-stu-id="62c13-436">no</span></span>           |
| <span data-ttu-id="62c13-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="62c13-437">msdyn_start</span></span>                  | <span data-ttu-id="62c13-438">không</span><span class="sxs-lookup"><span data-stu-id="62c13-438">no</span></span>             | <span data-ttu-id="62c13-439">không</span><span class="sxs-lookup"><span data-stu-id="62c13-439">no</span></span>           |
| <span data-ttu-id="62c13-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="62c13-440">msdyn_taskid</span></span>                 | <span data-ttu-id="62c13-441">không</span><span class="sxs-lookup"><span data-stu-id="62c13-441">no</span></span>             | <span data-ttu-id="62c13-442">không</span><span class="sxs-lookup"><span data-stu-id="62c13-442">no</span></span>           |
| <span data-ttu-id="62c13-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="62c13-443">msdyn_taskidname</span></span>             | <span data-ttu-id="62c13-444">không</span><span class="sxs-lookup"><span data-stu-id="62c13-444">no</span></span>             | <span data-ttu-id="62c13-445">không</span><span class="sxs-lookup"><span data-stu-id="62c13-445">no</span></span>           |
| <span data-ttu-id="62c13-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="62c13-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="62c13-447">không</span><span class="sxs-lookup"><span data-stu-id="62c13-447">no</span></span>             | <span data-ttu-id="62c13-448">không</span><span class="sxs-lookup"><span data-stu-id="62c13-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="62c13-449">Thành viên nhóm dự án</span><span class="sxs-lookup"><span data-stu-id="62c13-449">Project team member</span></span>

| <span data-ttu-id="62c13-450">**Tên lô-gic**</span><span class="sxs-lookup"><span data-stu-id="62c13-450">**Logical name**</span></span>                                 | <span data-ttu-id="62c13-451">**Có thể tạo**</span><span class="sxs-lookup"><span data-stu-id="62c13-451">**Can create**</span></span> | <span data-ttu-id="62c13-452">**Có thể chỉnh sửa**</span><span class="sxs-lookup"><span data-stu-id="62c13-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="62c13-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="62c13-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="62c13-454">không</span><span class="sxs-lookup"><span data-stu-id="62c13-454">no</span></span>             | <span data-ttu-id="62c13-455">không</span><span class="sxs-lookup"><span data-stu-id="62c13-455">no</span></span>           |
| <span data-ttu-id="62c13-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="62c13-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="62c13-457">không</span><span class="sxs-lookup"><span data-stu-id="62c13-457">no</span></span>             | <span data-ttu-id="62c13-458">không</span><span class="sxs-lookup"><span data-stu-id="62c13-458">no</span></span>           |
| <span data-ttu-id="62c13-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="62c13-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="62c13-460">không</span><span class="sxs-lookup"><span data-stu-id="62c13-460">no</span></span>             | <span data-ttu-id="62c13-461">không</span><span class="sxs-lookup"><span data-stu-id="62c13-461">no</span></span>           |
| <span data-ttu-id="62c13-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="62c13-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="62c13-463">không</span><span class="sxs-lookup"><span data-stu-id="62c13-463">no</span></span>             | <span data-ttu-id="62c13-464">không</span><span class="sxs-lookup"><span data-stu-id="62c13-464">no</span></span>           |
| <span data-ttu-id="62c13-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="62c13-465">msdyn_effort</span></span>                                     | <span data-ttu-id="62c13-466">không</span><span class="sxs-lookup"><span data-stu-id="62c13-466">no</span></span>             | <span data-ttu-id="62c13-467">không</span><span class="sxs-lookup"><span data-stu-id="62c13-467">no</span></span>           |
| <span data-ttu-id="62c13-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="62c13-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="62c13-469">không</span><span class="sxs-lookup"><span data-stu-id="62c13-469">no</span></span>             | <span data-ttu-id="62c13-470">không</span><span class="sxs-lookup"><span data-stu-id="62c13-470">no</span></span>           |
| <span data-ttu-id="62c13-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="62c13-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="62c13-472">không</span><span class="sxs-lookup"><span data-stu-id="62c13-472">no</span></span>             | <span data-ttu-id="62c13-473">không</span><span class="sxs-lookup"><span data-stu-id="62c13-473">no</span></span>           |
| <span data-ttu-id="62c13-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="62c13-474">msdyn_finish</span></span>                                     | <span data-ttu-id="62c13-475">không</span><span class="sxs-lookup"><span data-stu-id="62c13-475">no</span></span>             | <span data-ttu-id="62c13-476">không</span><span class="sxs-lookup"><span data-stu-id="62c13-476">no</span></span>           |
| <span data-ttu-id="62c13-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="62c13-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="62c13-478">không</span><span class="sxs-lookup"><span data-stu-id="62c13-478">no</span></span>             | <span data-ttu-id="62c13-479">không</span><span class="sxs-lookup"><span data-stu-id="62c13-479">no</span></span>           |
| <span data-ttu-id="62c13-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="62c13-480">msdyn_hours</span></span>                                      | <span data-ttu-id="62c13-481">không</span><span class="sxs-lookup"><span data-stu-id="62c13-481">no</span></span>             | <span data-ttu-id="62c13-482">không</span><span class="sxs-lookup"><span data-stu-id="62c13-482">no</span></span>           |
| <span data-ttu-id="62c13-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="62c13-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="62c13-484">không</span><span class="sxs-lookup"><span data-stu-id="62c13-484">no</span></span>             | <span data-ttu-id="62c13-485">không</span><span class="sxs-lookup"><span data-stu-id="62c13-485">no</span></span>           |
| <span data-ttu-id="62c13-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="62c13-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="62c13-487">không</span><span class="sxs-lookup"><span data-stu-id="62c13-487">no</span></span>             | <span data-ttu-id="62c13-488">không</span><span class="sxs-lookup"><span data-stu-id="62c13-488">no</span></span>           |
| <span data-ttu-id="62c13-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="62c13-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="62c13-490">không</span><span class="sxs-lookup"><span data-stu-id="62c13-490">no</span></span>             | <span data-ttu-id="62c13-491">không</span><span class="sxs-lookup"><span data-stu-id="62c13-491">no</span></span>           |
| <span data-ttu-id="62c13-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="62c13-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="62c13-493">không</span><span class="sxs-lookup"><span data-stu-id="62c13-493">no</span></span>             | <span data-ttu-id="62c13-494">không</span><span class="sxs-lookup"><span data-stu-id="62c13-494">no</span></span>           |
| <span data-ttu-id="62c13-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="62c13-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="62c13-496">không</span><span class="sxs-lookup"><span data-stu-id="62c13-496">no</span></span>             | <span data-ttu-id="62c13-497">không</span><span class="sxs-lookup"><span data-stu-id="62c13-497">no</span></span>           |
| <span data-ttu-id="62c13-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="62c13-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="62c13-499">không</span><span class="sxs-lookup"><span data-stu-id="62c13-499">no</span></span>             | <span data-ttu-id="62c13-500">không</span><span class="sxs-lookup"><span data-stu-id="62c13-500">no</span></span>           |
| <span data-ttu-id="62c13-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="62c13-501">msdyn_start</span></span>                                      | <span data-ttu-id="62c13-502">không</span><span class="sxs-lookup"><span data-stu-id="62c13-502">no</span></span>             | <span data-ttu-id="62c13-503">không</span><span class="sxs-lookup"><span data-stu-id="62c13-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="62c13-504">Dự án</span><span class="sxs-lookup"><span data-stu-id="62c13-504">Project</span></span>

| <span data-ttu-id="62c13-505">**Tên lô-gic**</span><span class="sxs-lookup"><span data-stu-id="62c13-505">**Logical name**</span></span>                       | <span data-ttu-id="62c13-506">**Có thể tạo**</span><span class="sxs-lookup"><span data-stu-id="62c13-506">**Can create**</span></span> | <span data-ttu-id="62c13-507">**Có thể chỉnh sửa**</span><span class="sxs-lookup"><span data-stu-id="62c13-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="62c13-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="62c13-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="62c13-509">không</span><span class="sxs-lookup"><span data-stu-id="62c13-509">no</span></span>             | <span data-ttu-id="62c13-510">không</span><span class="sxs-lookup"><span data-stu-id="62c13-510">no</span></span>           |
| <span data-ttu-id="62c13-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="62c13-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="62c13-512">không</span><span class="sxs-lookup"><span data-stu-id="62c13-512">no</span></span>             | <span data-ttu-id="62c13-513">không</span><span class="sxs-lookup"><span data-stu-id="62c13-513">no</span></span>           |
| <span data-ttu-id="62c13-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="62c13-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="62c13-515">không</span><span class="sxs-lookup"><span data-stu-id="62c13-515">no</span></span>             | <span data-ttu-id="62c13-516">không</span><span class="sxs-lookup"><span data-stu-id="62c13-516">no</span></span>           |
| <span data-ttu-id="62c13-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="62c13-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="62c13-518">không</span><span class="sxs-lookup"><span data-stu-id="62c13-518">no</span></span>             | <span data-ttu-id="62c13-519">không</span><span class="sxs-lookup"><span data-stu-id="62c13-519">no</span></span>           |
| <span data-ttu-id="62c13-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="62c13-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="62c13-521">không</span><span class="sxs-lookup"><span data-stu-id="62c13-521">no</span></span>             | <span data-ttu-id="62c13-522">không</span><span class="sxs-lookup"><span data-stu-id="62c13-522">no</span></span>           |
| <span data-ttu-id="62c13-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="62c13-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="62c13-524">không</span><span class="sxs-lookup"><span data-stu-id="62c13-524">no</span></span>             | <span data-ttu-id="62c13-525">không</span><span class="sxs-lookup"><span data-stu-id="62c13-525">no</span></span>           |
| <span data-ttu-id="62c13-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="62c13-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="62c13-527">có</span><span class="sxs-lookup"><span data-stu-id="62c13-527">yes</span></span>            | <span data-ttu-id="62c13-528">không</span><span class="sxs-lookup"><span data-stu-id="62c13-528">no</span></span>           |
| <span data-ttu-id="62c13-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="62c13-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="62c13-530">có</span><span class="sxs-lookup"><span data-stu-id="62c13-530">yes</span></span>            | <span data-ttu-id="62c13-531">không</span><span class="sxs-lookup"><span data-stu-id="62c13-531">no</span></span>           |
| <span data-ttu-id="62c13-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="62c13-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="62c13-533">có</span><span class="sxs-lookup"><span data-stu-id="62c13-533">yes</span></span>            | <span data-ttu-id="62c13-534">không</span><span class="sxs-lookup"><span data-stu-id="62c13-534">no</span></span>           |
| <span data-ttu-id="62c13-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="62c13-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="62c13-536">không</span><span class="sxs-lookup"><span data-stu-id="62c13-536">no</span></span>             | <span data-ttu-id="62c13-537">không</span><span class="sxs-lookup"><span data-stu-id="62c13-537">no</span></span>           |
| <span data-ttu-id="62c13-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="62c13-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="62c13-539">không</span><span class="sxs-lookup"><span data-stu-id="62c13-539">no</span></span>             | <span data-ttu-id="62c13-540">không</span><span class="sxs-lookup"><span data-stu-id="62c13-540">no</span></span>           |
| <span data-ttu-id="62c13-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="62c13-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="62c13-542">không</span><span class="sxs-lookup"><span data-stu-id="62c13-542">no</span></span>             | <span data-ttu-id="62c13-543">không</span><span class="sxs-lookup"><span data-stu-id="62c13-543">no</span></span>           |
| <span data-ttu-id="62c13-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="62c13-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="62c13-545">không</span><span class="sxs-lookup"><span data-stu-id="62c13-545">no</span></span>             | <span data-ttu-id="62c13-546">không</span><span class="sxs-lookup"><span data-stu-id="62c13-546">no</span></span>           |
| <span data-ttu-id="62c13-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="62c13-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="62c13-548">không</span><span class="sxs-lookup"><span data-stu-id="62c13-548">no</span></span>             | <span data-ttu-id="62c13-549">không</span><span class="sxs-lookup"><span data-stu-id="62c13-549">no</span></span>           |
| <span data-ttu-id="62c13-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="62c13-550">msdyn_duration</span></span>                         | <span data-ttu-id="62c13-551">không</span><span class="sxs-lookup"><span data-stu-id="62c13-551">no</span></span>             | <span data-ttu-id="62c13-552">không</span><span class="sxs-lookup"><span data-stu-id="62c13-552">no</span></span>           |
| <span data-ttu-id="62c13-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="62c13-553">msdyn_effort</span></span>                           | <span data-ttu-id="62c13-554">không</span><span class="sxs-lookup"><span data-stu-id="62c13-554">no</span></span>             | <span data-ttu-id="62c13-555">không</span><span class="sxs-lookup"><span data-stu-id="62c13-555">no</span></span>           |
| <span data-ttu-id="62c13-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="62c13-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="62c13-557">không</span><span class="sxs-lookup"><span data-stu-id="62c13-557">no</span></span>             | <span data-ttu-id="62c13-558">không</span><span class="sxs-lookup"><span data-stu-id="62c13-558">no</span></span>           |
| <span data-ttu-id="62c13-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="62c13-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="62c13-560">không</span><span class="sxs-lookup"><span data-stu-id="62c13-560">no</span></span>             | <span data-ttu-id="62c13-561">không</span><span class="sxs-lookup"><span data-stu-id="62c13-561">no</span></span>           |
| <span data-ttu-id="62c13-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="62c13-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="62c13-563">không</span><span class="sxs-lookup"><span data-stu-id="62c13-563">no</span></span>             | <span data-ttu-id="62c13-564">không</span><span class="sxs-lookup"><span data-stu-id="62c13-564">no</span></span>           |
| <span data-ttu-id="62c13-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="62c13-565">msdyn_finish</span></span>                           | <span data-ttu-id="62c13-566">có</span><span class="sxs-lookup"><span data-stu-id="62c13-566">yes</span></span>            | <span data-ttu-id="62c13-567">có</span><span class="sxs-lookup"><span data-stu-id="62c13-567">yes</span></span>          |
| <span data-ttu-id="62c13-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="62c13-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="62c13-569">không</span><span class="sxs-lookup"><span data-stu-id="62c13-569">no</span></span>             | <span data-ttu-id="62c13-570">không</span><span class="sxs-lookup"><span data-stu-id="62c13-570">no</span></span>           |
| <span data-ttu-id="62c13-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="62c13-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="62c13-572">không</span><span class="sxs-lookup"><span data-stu-id="62c13-572">no</span></span>             | <span data-ttu-id="62c13-573">không</span><span class="sxs-lookup"><span data-stu-id="62c13-573">no</span></span>           |
| <span data-ttu-id="62c13-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="62c13-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="62c13-575">không</span><span class="sxs-lookup"><span data-stu-id="62c13-575">no</span></span>             | <span data-ttu-id="62c13-576">không</span><span class="sxs-lookup"><span data-stu-id="62c13-576">no</span></span>           |
| <span data-ttu-id="62c13-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="62c13-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="62c13-578">không</span><span class="sxs-lookup"><span data-stu-id="62c13-578">no</span></span>             | <span data-ttu-id="62c13-579">không</span><span class="sxs-lookup"><span data-stu-id="62c13-579">no</span></span>           |
| <span data-ttu-id="62c13-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="62c13-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="62c13-581">không</span><span class="sxs-lookup"><span data-stu-id="62c13-581">no</span></span>             | <span data-ttu-id="62c13-582">không</span><span class="sxs-lookup"><span data-stu-id="62c13-582">no</span></span>           |
| <span data-ttu-id="62c13-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="62c13-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="62c13-584">không</span><span class="sxs-lookup"><span data-stu-id="62c13-584">no</span></span>             | <span data-ttu-id="62c13-585">không</span><span class="sxs-lookup"><span data-stu-id="62c13-585">no</span></span>           |
| <span data-ttu-id="62c13-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="62c13-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="62c13-587">không</span><span class="sxs-lookup"><span data-stu-id="62c13-587">no</span></span>             | <span data-ttu-id="62c13-588">không</span><span class="sxs-lookup"><span data-stu-id="62c13-588">no</span></span>           |
| <span data-ttu-id="62c13-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="62c13-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="62c13-590">không</span><span class="sxs-lookup"><span data-stu-id="62c13-590">no</span></span>             | <span data-ttu-id="62c13-591">không</span><span class="sxs-lookup"><span data-stu-id="62c13-591">no</span></span>           |
| <span data-ttu-id="62c13-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="62c13-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="62c13-593">không</span><span class="sxs-lookup"><span data-stu-id="62c13-593">no</span></span>             | <span data-ttu-id="62c13-594">không</span><span class="sxs-lookup"><span data-stu-id="62c13-594">no</span></span>           |
| <span data-ttu-id="62c13-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="62c13-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="62c13-596">không</span><span class="sxs-lookup"><span data-stu-id="62c13-596">no</span></span>             | <span data-ttu-id="62c13-597">không</span><span class="sxs-lookup"><span data-stu-id="62c13-597">no</span></span>           |
| <span data-ttu-id="62c13-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="62c13-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="62c13-599">không</span><span class="sxs-lookup"><span data-stu-id="62c13-599">no</span></span>             | <span data-ttu-id="62c13-600">không</span><span class="sxs-lookup"><span data-stu-id="62c13-600">no</span></span>           |
| <span data-ttu-id="62c13-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="62c13-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="62c13-602">không</span><span class="sxs-lookup"><span data-stu-id="62c13-602">no</span></span>             | <span data-ttu-id="62c13-603">không</span><span class="sxs-lookup"><span data-stu-id="62c13-603">no</span></span>           |
| <span data-ttu-id="62c13-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="62c13-604">msdyn_progress</span></span>                         | <span data-ttu-id="62c13-605">không</span><span class="sxs-lookup"><span data-stu-id="62c13-605">no</span></span>             | <span data-ttu-id="62c13-606">không</span><span class="sxs-lookup"><span data-stu-id="62c13-606">no</span></span>           |
| <span data-ttu-id="62c13-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="62c13-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="62c13-608">không</span><span class="sxs-lookup"><span data-stu-id="62c13-608">no</span></span>             | <span data-ttu-id="62c13-609">không</span><span class="sxs-lookup"><span data-stu-id="62c13-609">no</span></span>           |
| <span data-ttu-id="62c13-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="62c13-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="62c13-611">không</span><span class="sxs-lookup"><span data-stu-id="62c13-611">no</span></span>             | <span data-ttu-id="62c13-612">không</span><span class="sxs-lookup"><span data-stu-id="62c13-612">no</span></span>           |
| <span data-ttu-id="62c13-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="62c13-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="62c13-614">không</span><span class="sxs-lookup"><span data-stu-id="62c13-614">no</span></span>             | <span data-ttu-id="62c13-615">không</span><span class="sxs-lookup"><span data-stu-id="62c13-615">no</span></span>           |
| <span data-ttu-id="62c13-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="62c13-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="62c13-617">không</span><span class="sxs-lookup"><span data-stu-id="62c13-617">no</span></span>             | <span data-ttu-id="62c13-618">không</span><span class="sxs-lookup"><span data-stu-id="62c13-618">no</span></span>           |
| <span data-ttu-id="62c13-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="62c13-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="62c13-620">không</span><span class="sxs-lookup"><span data-stu-id="62c13-620">no</span></span>             | <span data-ttu-id="62c13-621">không</span><span class="sxs-lookup"><span data-stu-id="62c13-621">no</span></span>           |
| <span data-ttu-id="62c13-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="62c13-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="62c13-623">không</span><span class="sxs-lookup"><span data-stu-id="62c13-623">no</span></span>             | <span data-ttu-id="62c13-624">không</span><span class="sxs-lookup"><span data-stu-id="62c13-624">no</span></span>           |
| <span data-ttu-id="62c13-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="62c13-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="62c13-626">không</span><span class="sxs-lookup"><span data-stu-id="62c13-626">no</span></span>             | <span data-ttu-id="62c13-627">không</span><span class="sxs-lookup"><span data-stu-id="62c13-627">no</span></span>           |
| <span data-ttu-id="62c13-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="62c13-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="62c13-629">không</span><span class="sxs-lookup"><span data-stu-id="62c13-629">no</span></span>             | <span data-ttu-id="62c13-630">không</span><span class="sxs-lookup"><span data-stu-id="62c13-630">no</span></span>           |
| <span data-ttu-id="62c13-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="62c13-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="62c13-632">không</span><span class="sxs-lookup"><span data-stu-id="62c13-632">no</span></span>             | <span data-ttu-id="62c13-633">không</span><span class="sxs-lookup"><span data-stu-id="62c13-633">no</span></span>           |
| <span data-ttu-id="62c13-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="62c13-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="62c13-635">không</span><span class="sxs-lookup"><span data-stu-id="62c13-635">no</span></span>             | <span data-ttu-id="62c13-636">không</span><span class="sxs-lookup"><span data-stu-id="62c13-636">no</span></span>           |
| <span data-ttu-id="62c13-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="62c13-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="62c13-638">không</span><span class="sxs-lookup"><span data-stu-id="62c13-638">no</span></span>             | <span data-ttu-id="62c13-639">không</span><span class="sxs-lookup"><span data-stu-id="62c13-639">no</span></span>           |
| <span data-ttu-id="62c13-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="62c13-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="62c13-641">không</span><span class="sxs-lookup"><span data-stu-id="62c13-641">no</span></span>             | <span data-ttu-id="62c13-642">không</span><span class="sxs-lookup"><span data-stu-id="62c13-642">no</span></span>           |
| <span data-ttu-id="62c13-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="62c13-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="62c13-644">không</span><span class="sxs-lookup"><span data-stu-id="62c13-644">no</span></span>             | <span data-ttu-id="62c13-645">không</span><span class="sxs-lookup"><span data-stu-id="62c13-645">no</span></span>           |
| <span data-ttu-id="62c13-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="62c13-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="62c13-647">không</span><span class="sxs-lookup"><span data-stu-id="62c13-647">no</span></span>             | <span data-ttu-id="62c13-648">không</span><span class="sxs-lookup"><span data-stu-id="62c13-648">no</span></span>           |
| <span data-ttu-id="62c13-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="62c13-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="62c13-650">không</span><span class="sxs-lookup"><span data-stu-id="62c13-650">no</span></span>             | <span data-ttu-id="62c13-651">không</span><span class="sxs-lookup"><span data-stu-id="62c13-651">no</span></span>           |
| <span data-ttu-id="62c13-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="62c13-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="62c13-653">không</span><span class="sxs-lookup"><span data-stu-id="62c13-653">no</span></span>             | <span data-ttu-id="62c13-654">không</span><span class="sxs-lookup"><span data-stu-id="62c13-654">no</span></span>           |
| <span data-ttu-id="62c13-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="62c13-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="62c13-656">không</span><span class="sxs-lookup"><span data-stu-id="62c13-656">no</span></span>             | <span data-ttu-id="62c13-657">không</span><span class="sxs-lookup"><span data-stu-id="62c13-657">no</span></span>           |
| <span data-ttu-id="62c13-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="62c13-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="62c13-659">không</span><span class="sxs-lookup"><span data-stu-id="62c13-659">no</span></span>             | <span data-ttu-id="62c13-660">không</span><span class="sxs-lookup"><span data-stu-id="62c13-660">no</span></span>           |
| <span data-ttu-id="62c13-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="62c13-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="62c13-662">không</span><span class="sxs-lookup"><span data-stu-id="62c13-662">no</span></span>             | <span data-ttu-id="62c13-663">không</span><span class="sxs-lookup"><span data-stu-id="62c13-663">no</span></span>           |
| <span data-ttu-id="62c13-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="62c13-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="62c13-665">không</span><span class="sxs-lookup"><span data-stu-id="62c13-665">no</span></span>             | <span data-ttu-id="62c13-666">không</span><span class="sxs-lookup"><span data-stu-id="62c13-666">no</span></span>           |
| <span data-ttu-id="62c13-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="62c13-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="62c13-668">không</span><span class="sxs-lookup"><span data-stu-id="62c13-668">no</span></span>             | <span data-ttu-id="62c13-669">không</span><span class="sxs-lookup"><span data-stu-id="62c13-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="62c13-670">Các giới hạn và vấn đề đã biết</span><span class="sxs-lookup"><span data-stu-id="62c13-670">Limitations and known issues</span></span>
<span data-ttu-id="62c13-671">Sau đây là danh sách các giới hạn và vấn đề đã biết:</span><span class="sxs-lookup"><span data-stu-id="62c13-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="62c13-672">Chỉ **Người dùng có giấy phép dự án của Microsoft** là có thể sử dụng API lịch trình.</span><span class="sxs-lookup"><span data-stu-id="62c13-672">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="62c13-673">Những đối tượng sau không thể sử dụng API lịch trình:</span><span class="sxs-lookup"><span data-stu-id="62c13-673">They can't be used by:</span></span>
    - <span data-ttu-id="62c13-674">Người dùng ứng dụng</span><span class="sxs-lookup"><span data-stu-id="62c13-674">Application users</span></span>
    - <span data-ttu-id="62c13-675">Người dùng hệ thống</span><span class="sxs-lookup"><span data-stu-id="62c13-675">System users</span></span>
    - <span data-ttu-id="62c13-676">Người dùng tích hợp</span><span class="sxs-lookup"><span data-stu-id="62c13-676">Integration users</span></span>
    - <span data-ttu-id="62c13-677">Những người dùng khác không có giấy phép bắt buộc</span><span class="sxs-lookup"><span data-stu-id="62c13-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="62c13-678">Mỗi **OperationSet** chỉ có thể có tối đa 100 thao tác.</span><span class="sxs-lookup"><span data-stu-id="62c13-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="62c13-679">Mỗi người dùng chỉ có tối đa 10 **OperationSets** đang mở.</span><span class="sxs-lookup"><span data-stu-id="62c13-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="62c13-680">Project Operations hiện hỗ trợ tổng cộng tối đa 500 nhiệm vụ trên một dự án.</span><span class="sxs-lookup"><span data-stu-id="62c13-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="62c13-681">Hiện không có nhật ký lỗi và trạng thái lỗi **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="62c13-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- [<span data-ttu-id="62c13-682">Giới hạn và ranh giới đối với các dự án và nhiệm vụ</span><span class="sxs-lookup"><span data-stu-id="62c13-682">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="62c13-683">Xử lý lỗi</span><span class="sxs-lookup"><span data-stu-id="62c13-683">Error handling</span></span>

   - <span data-ttu-id="62c13-684">Để xem lại các lỗi được tạo từ Bộ hoạt động, hãy chuyển đến phần **Cài đặt** \> **Tích hợp lịch biểu** \> **Bộ hoạt động**.</span><span class="sxs-lookup"><span data-stu-id="62c13-684">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="62c13-685">Để xem lại các lỗi được tạo từ Dịch vụ lên lịch dự án, hãy chuyển đến phần **Cài đặt** \> **Tích hợp lịch biểu** \> **Nhật ký lỗi PSS**.</span><span class="sxs-lookup"><span data-stu-id="62c13-685">To review errors generated from the Project Scheduling Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="62c13-686">Kịch bản mẫu</span><span class="sxs-lookup"><span data-stu-id="62c13-686">Sample scenario</span></span>

<span data-ttu-id="62c13-687">Trong kịch bản này, bạn sẽ tạo một dự án, một thành viên nhóm, bốn nhiệm vụ và hai công việc giao cho nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="62c13-687">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="62c13-688">Tiếp theo, bạn sẽ cập nhật một nhiệm vụ, cập nhật dự án, xóa một nhiệm vụ, xóa một công việc giao cho nguồn lực và tạo một quan hệ phụ thuộc nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="62c13-688">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

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

## <a name="additional-samples"></a><span data-ttu-id="62c13-689">Các mẫu khác</span><span class="sxs-lookup"><span data-stu-id="62c13-689">Additional samples</span></span>

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
