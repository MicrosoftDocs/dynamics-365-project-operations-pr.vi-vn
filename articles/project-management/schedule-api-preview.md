---
title: Sử dụng các API lịch trình dự án để thực hiện các hoạt động với các thực thể Lập lịch biểu
description: Chủ đề này cung cấp thông tin và các mẫu để sử dụng API lịch trình dự án.
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4915261c08a3271a919e04084e92a14b297c1b35
ms.sourcegitcommit: 2f16c2bc7c8350676a6a380c61fffa9958db6a0b
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/22/2021
ms.locfileid: "6293253"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="63468-103">Sử dụng các API lịch trình dự án để thực hiện các hoạt động với các thực thể Lập lịch biểu</span><span class="sxs-lookup"><span data-stu-id="63468-103">Use Project schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="63468-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="63468-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="63468-105">Một số hoặc tất cả chức năng được ghi chú trong chủ đề này khả dụng như một phần của bản phát hành xem trước.</span><span class="sxs-lookup"><span data-stu-id="63468-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="63468-106">Nội dung và chức năng có thể thay đổi.</span><span class="sxs-lookup"><span data-stu-id="63468-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="63468-107">Thực thể lập lịch trình</span><span class="sxs-lookup"><span data-stu-id="63468-107">Scheduling entities</span></span>

<span data-ttu-id="63468-108">Các API lịch trình dự án cung cấp khả năng thực hiện các hoạt động tạo, cập nhật và xóa với **Các thực thể lập lịch trình**.</span><span class="sxs-lookup"><span data-stu-id="63468-108">Project schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="63468-109">Các thực thể này được quản lý thông qua công cụ Lập lịch trình trong Dự án cho web.</span><span class="sxs-lookup"><span data-stu-id="63468-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="63468-110">Các thao tác tạo, cập nhật và xóa với **Thực thể lập lịch trình** đã bị hạn chế trong các bản phát hành Dynamics 365 Project Operations trước đó.</span><span class="sxs-lookup"><span data-stu-id="63468-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="63468-111">Bảng sau cung cấp danh sách đầy đủ các thực thể lịch trình của Dự án.</span><span class="sxs-lookup"><span data-stu-id="63468-111">The following table provides a full list of the Project schedule entities.</span></span>

| <span data-ttu-id="63468-112">Tên thực thể</span><span class="sxs-lookup"><span data-stu-id="63468-112">Entity name</span></span>  | <span data-ttu-id="63468-113">Tên logic của thực thể</span><span class="sxs-lookup"><span data-stu-id="63468-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="63468-114">Dự án</span><span class="sxs-lookup"><span data-stu-id="63468-114">Project</span></span> | <span data-ttu-id="63468-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="63468-115">msdyn_project</span></span> |
| <span data-ttu-id="63468-116">Nhiệm vụ dự án</span><span class="sxs-lookup"><span data-stu-id="63468-116">Project Task</span></span>  | <span data-ttu-id="63468-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="63468-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="63468-118">Quan hệ phụ thuộc Nhiệm vụ Dự án</span><span class="sxs-lookup"><span data-stu-id="63468-118">Project Task Dependency</span></span>  | <span data-ttu-id="63468-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="63468-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="63468-120">Gán Nguồn lực</span><span class="sxs-lookup"><span data-stu-id="63468-120">Resource Assignment</span></span> | <span data-ttu-id="63468-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="63468-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="63468-122">Bộ chứa Dự án</span><span class="sxs-lookup"><span data-stu-id="63468-122">Project Bucket</span></span>  | <span data-ttu-id="63468-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="63468-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="63468-124">Thành viên Nhóm Dự án</span><span class="sxs-lookup"><span data-stu-id="63468-124">Project Team Member</span></span> | <span data-ttu-id="63468-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="63468-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="63468-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="63468-126">OperationSet</span></span>

<span data-ttu-id="63468-127">OperationSet là một mẫu đơn vị công việc có thể được sử dụng khi phải xử lý một số yêu cầu tác động lên lịch trình trong một giao dịch.</span><span class="sxs-lookup"><span data-stu-id="63468-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="project-schedule-apis"></a><span data-ttu-id="63468-128">API lịch trình dự án</span><span class="sxs-lookup"><span data-stu-id="63468-128">Project schedule APIs</span></span>

<span data-ttu-id="63468-129">Sau đây là danh sách các API lịch trình Dự án hiện tại.</span><span class="sxs-lookup"><span data-stu-id="63468-129">The following is a list of current Project schedule APIs.</span></span>

- <span data-ttu-id="63468-130">**msdyn_CreateProjectV1**: API này có thể được dùng để tạo một dự án.</span><span class="sxs-lookup"><span data-stu-id="63468-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="63468-131">Nhóm dự án và dự án mặc định được tạo ngay lập tức.</span><span class="sxs-lookup"><span data-stu-id="63468-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="63468-132">**msdyn_CreateTeamMemberV1**: API này có thể được dùng để tạo một thành viên trong nhóm dự án.</span><span class="sxs-lookup"><span data-stu-id="63468-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="63468-133">Hồ sơ thành viên trong nhóm được tạo ngay lập tức.</span><span class="sxs-lookup"><span data-stu-id="63468-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="63468-134">**msdyn_CreateOperationSetV1**: API này có thể được dùng để lập lịch trình một số yêu cầu phải được thực hiện trong một giao dịch.</span><span class="sxs-lookup"><span data-stu-id="63468-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="63468-135">**msdyn_PSSCreateV1**: API này có thể được dùng để tạo một thực thể.</span><span class="sxs-lookup"><span data-stu-id="63468-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="63468-136">Thực thể có thể là bất kỳ thực thể lập lịch trình Dự án nào hỗ trợ hoạt động tạo.</span><span class="sxs-lookup"><span data-stu-id="63468-136">The entity can be any of the Project scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="63468-137">**msdyn_PSSUpdateV1**: API này có thể được dùng để cập nhật một thực thể.</span><span class="sxs-lookup"><span data-stu-id="63468-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="63468-138">Thực thể có thể là bất kỳ thực thể lập lịch trình Dự án nào hỗ trợ hoạt động cập nhật.</span><span class="sxs-lookup"><span data-stu-id="63468-138">The entity can be any of the Project scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="63468-139">**msdyn_PSSDeleteV1**: API này có thể được dùng để xóa một thực thể.</span><span class="sxs-lookup"><span data-stu-id="63468-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="63468-140">Thực thể có thể là bất kỳ thực thể lập lịch trình Dự án nào hỗ trợ hoạt động xóa.</span><span class="sxs-lookup"><span data-stu-id="63468-140">The entity can be any of the Project scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="63468-141">**msdyn_ExecuteOperationSetV1**: API này được dùng để thực thi tất cả các thao tác trong nhóm thao tác nhất định.</span><span class="sxs-lookup"><span data-stu-id="63468-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-project-schedule-apis-with-operationset"></a><span data-ttu-id="63468-142">Sử dụng API lịch trình dự án với OperationSet</span><span class="sxs-lookup"><span data-stu-id="63468-142">Using Project schedule APIs with OperationSet</span></span>

<span data-ttu-id="63468-143">Bởi vì bản ghi có cả **CreateProjectV1** và **CreateTeamMemberV1** được tạo ngay lập tức, nên không thể dùng các API này trực tiếp trong **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="63468-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="63468-144">Tuy nhiên, bạn có thể sử dụng API để tạo các bản ghi cần thiết, tạo một **OperationSet**, sau đó sử dụng các bản ghi được tạo trước này trong **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="63468-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="63468-145">Thao tác được hỗ trợ</span><span class="sxs-lookup"><span data-stu-id="63468-145">Supported operations</span></span>

| <span data-ttu-id="63468-146">Thực thể lập lịch trình</span><span class="sxs-lookup"><span data-stu-id="63468-146">Scheduling entity</span></span> | <span data-ttu-id="63468-147">Tạo</span><span class="sxs-lookup"><span data-stu-id="63468-147">Create</span></span> | <span data-ttu-id="63468-148">Update</span><span class="sxs-lookup"><span data-stu-id="63468-148">Update</span></span> | <span data-ttu-id="63468-149">Delete</span><span class="sxs-lookup"><span data-stu-id="63468-149">Delete</span></span> | <span data-ttu-id="63468-150">Những điều quan trọng cần cân nhắc</span><span class="sxs-lookup"><span data-stu-id="63468-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="63468-151">Nhiệm vụ dự án</span><span class="sxs-lookup"><span data-stu-id="63468-151">Project task</span></span> | <span data-ttu-id="63468-152">Có</span><span class="sxs-lookup"><span data-stu-id="63468-152">Yes</span></span> | <span data-ttu-id="63468-153">Có</span><span class="sxs-lookup"><span data-stu-id="63468-153">Yes</span></span> | <span data-ttu-id="63468-154">Có</span><span class="sxs-lookup"><span data-stu-id="63468-154">Yes</span></span> | <span data-ttu-id="63468-155">Không có</span><span class="sxs-lookup"><span data-stu-id="63468-155">None</span></span> |
| <span data-ttu-id="63468-156">Quan hệ phụ thuộc nhiệm vụ dự án</span><span class="sxs-lookup"><span data-stu-id="63468-156">Project task dependency</span></span> | <span data-ttu-id="63468-157">Có</span><span class="sxs-lookup"><span data-stu-id="63468-157">Yes</span></span> | <span data-ttu-id="63468-158">Có</span><span class="sxs-lookup"><span data-stu-id="63468-158">Yes</span></span> | | <span data-ttu-id="63468-159">Bản ghi quan hệ phụ thuộc nhiệm vụ dự án không được cập nhật.</span><span class="sxs-lookup"><span data-stu-id="63468-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="63468-160">Thay vào đó, một bản ghi cũ có thể bị xóa và một bản ghi mới có thể được tạo.</span><span class="sxs-lookup"><span data-stu-id="63468-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="63468-161">Công việc giao cho nguồn lực</span><span class="sxs-lookup"><span data-stu-id="63468-161">Resource assignment</span></span> | <span data-ttu-id="63468-162">Có</span><span class="sxs-lookup"><span data-stu-id="63468-162">Yes</span></span> | <span data-ttu-id="63468-163">Có</span><span class="sxs-lookup"><span data-stu-id="63468-163">Yes</span></span> | | <span data-ttu-id="63468-164">Không hỗ trợ thao tác với các trường sau: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** và **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="63468-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="63468-165">Bản ghi việc được giao không được cập nhật.</span><span class="sxs-lookup"><span data-stu-id="63468-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="63468-166">Thay vào đó, một bản ghi cũ có thể bị xóa và một bản ghi mới có thể được tạo.</span><span class="sxs-lookup"><span data-stu-id="63468-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="63468-167">Nhóm dự án</span><span class="sxs-lookup"><span data-stu-id="63468-167">Project bucket</span></span> | <span data-ttu-id="63468-168">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="63468-168">N/A</span></span> | <span data-ttu-id="63468-169">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="63468-169">N/A</span></span> | <span data-ttu-id="63468-170">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="63468-170">N/A</span></span> | <span data-ttu-id="63468-171">Nhóm mặc định được tạo bằng cách sử dụng API **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="63468-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="63468-172">Thành viên nhóm dự án</span><span class="sxs-lookup"><span data-stu-id="63468-172">Project team member</span></span> | <span data-ttu-id="63468-173">Có</span><span class="sxs-lookup"><span data-stu-id="63468-173">Yes</span></span> | <span data-ttu-id="63468-174">Có</span><span class="sxs-lookup"><span data-stu-id="63468-174">Yes</span></span> | <span data-ttu-id="63468-175">Có</span><span class="sxs-lookup"><span data-stu-id="63468-175">Yes</span></span> | <span data-ttu-id="63468-176">Đối với thao tác tạo, hãy sử dụng API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="63468-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="63468-177">Dự án</span><span class="sxs-lookup"><span data-stu-id="63468-177">Project</span></span> | <span data-ttu-id="63468-178">Có</span><span class="sxs-lookup"><span data-stu-id="63468-178">Yes</span></span> | <span data-ttu-id="63468-179">Có</span><span class="sxs-lookup"><span data-stu-id="63468-179">Yes</span></span> | <span data-ttu-id="63468-180">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="63468-180">N/A</span></span> | <span data-ttu-id="63468-181">Không hỗ trợ thao tác với các trường sau: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** và **Duration**.</span><span class="sxs-lookup"><span data-stu-id="63468-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="63468-182">Các API này có thể được gọi ra với các đối tượng thực thể bao gồm các trường tùy chỉnh.</span><span class="sxs-lookup"><span data-stu-id="63468-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="63468-183">Thuộc tính ID là không bắt buộc.</span><span class="sxs-lookup"><span data-stu-id="63468-183">The ID property is optional.</span></span> <span data-ttu-id="63468-184">Nếu được cung cấp, hệ thống sẽ cố gắng sử dụng ID thuộc tính và đưa ra một ngoại lệ nếu không thể sử dụng.</span><span class="sxs-lookup"><span data-stu-id="63468-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="63468-185">Nếu không được cung cấp, hệ thống sẽ tạo ID thuộc tính.</span><span class="sxs-lookup"><span data-stu-id="63468-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="63468-186">Các trường bị hạn chế</span><span class="sxs-lookup"><span data-stu-id="63468-186">Restricted fields</span></span>

<span data-ttu-id="63468-187">Các bảng sau xác định các trường bị hạn chế trong **Tạo** và **Chỉnh sửa**.</span><span class="sxs-lookup"><span data-stu-id="63468-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="63468-188">Nhiệm vụ dự án</span><span class="sxs-lookup"><span data-stu-id="63468-188">Project task</span></span>

| <span data-ttu-id="63468-189">**Tên lô-gic**</span><span class="sxs-lookup"><span data-stu-id="63468-189">**Logical name**</span></span>                       | <span data-ttu-id="63468-190">**Có thể tạo**</span><span class="sxs-lookup"><span data-stu-id="63468-190">**Can create**</span></span> | <span data-ttu-id="63468-191">**Có thể chỉnh sửa**</span><span class="sxs-lookup"><span data-stu-id="63468-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="63468-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="63468-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="63468-193">không</span><span class="sxs-lookup"><span data-stu-id="63468-193">no</span></span>             | <span data-ttu-id="63468-194">không</span><span class="sxs-lookup"><span data-stu-id="63468-194">no</span></span>               |
| <span data-ttu-id="63468-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="63468-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="63468-196">không</span><span class="sxs-lookup"><span data-stu-id="63468-196">no</span></span>             | <span data-ttu-id="63468-197">không</span><span class="sxs-lookup"><span data-stu-id="63468-197">no</span></span>               |
| <span data-ttu-id="63468-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="63468-198">msdyn_actualend</span></span>                        | <span data-ttu-id="63468-199">không</span><span class="sxs-lookup"><span data-stu-id="63468-199">no</span></span>             | <span data-ttu-id="63468-200">không</span><span class="sxs-lookup"><span data-stu-id="63468-200">no</span></span>               |
| <span data-ttu-id="63468-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="63468-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="63468-202">không</span><span class="sxs-lookup"><span data-stu-id="63468-202">no</span></span>             | <span data-ttu-id="63468-203">không</span><span class="sxs-lookup"><span data-stu-id="63468-203">no</span></span>               |
| <span data-ttu-id="63468-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="63468-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="63468-205">không</span><span class="sxs-lookup"><span data-stu-id="63468-205">no</span></span>             | <span data-ttu-id="63468-206">không</span><span class="sxs-lookup"><span data-stu-id="63468-206">no</span></span>               |
| <span data-ttu-id="63468-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="63468-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="63468-208">không</span><span class="sxs-lookup"><span data-stu-id="63468-208">no</span></span>             | <span data-ttu-id="63468-209">không</span><span class="sxs-lookup"><span data-stu-id="63468-209">no</span></span>               |
| <span data-ttu-id="63468-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="63468-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="63468-211">không</span><span class="sxs-lookup"><span data-stu-id="63468-211">no</span></span>             | <span data-ttu-id="63468-212">không</span><span class="sxs-lookup"><span data-stu-id="63468-212">no</span></span>               |
| <span data-ttu-id="63468-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="63468-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="63468-214">không</span><span class="sxs-lookup"><span data-stu-id="63468-214">no</span></span>             | <span data-ttu-id="63468-215">không</span><span class="sxs-lookup"><span data-stu-id="63468-215">no</span></span>               |
| <span data-ttu-id="63468-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="63468-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="63468-217">không</span><span class="sxs-lookup"><span data-stu-id="63468-217">no</span></span>             | <span data-ttu-id="63468-218">không</span><span class="sxs-lookup"><span data-stu-id="63468-218">no</span></span>               |
| <span data-ttu-id="63468-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="63468-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="63468-220">không</span><span class="sxs-lookup"><span data-stu-id="63468-220">no</span></span>             | <span data-ttu-id="63468-221">không</span><span class="sxs-lookup"><span data-stu-id="63468-221">no</span></span>               |
| <span data-ttu-id="63468-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="63468-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="63468-223">không</span><span class="sxs-lookup"><span data-stu-id="63468-223">no</span></span>             | <span data-ttu-id="63468-224">không</span><span class="sxs-lookup"><span data-stu-id="63468-224">no</span></span>               |
| <span data-ttu-id="63468-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="63468-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="63468-226">không</span><span class="sxs-lookup"><span data-stu-id="63468-226">no</span></span>             | <span data-ttu-id="63468-227">không</span><span class="sxs-lookup"><span data-stu-id="63468-227">no</span></span>               |
| <span data-ttu-id="63468-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="63468-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="63468-229">không</span><span class="sxs-lookup"><span data-stu-id="63468-229">no</span></span>             | <span data-ttu-id="63468-230">không</span><span class="sxs-lookup"><span data-stu-id="63468-230">no</span></span>               |
| <span data-ttu-id="63468-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="63468-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="63468-232">không</span><span class="sxs-lookup"><span data-stu-id="63468-232">no</span></span>             | <span data-ttu-id="63468-233">không</span><span class="sxs-lookup"><span data-stu-id="63468-233">no</span></span>               |
| <span data-ttu-id="63468-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="63468-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="63468-235">không</span><span class="sxs-lookup"><span data-stu-id="63468-235">no</span></span>             | <span data-ttu-id="63468-236">không</span><span class="sxs-lookup"><span data-stu-id="63468-236">no</span></span>               |
| <span data-ttu-id="63468-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="63468-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="63468-238">không</span><span class="sxs-lookup"><span data-stu-id="63468-238">no</span></span>             | <span data-ttu-id="63468-239">không</span><span class="sxs-lookup"><span data-stu-id="63468-239">no</span></span>               |
| <span data-ttu-id="63468-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="63468-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="63468-241">không</span><span class="sxs-lookup"><span data-stu-id="63468-241">no</span></span>             | <span data-ttu-id="63468-242">không</span><span class="sxs-lookup"><span data-stu-id="63468-242">no</span></span>               |
| <span data-ttu-id="63468-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="63468-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="63468-244">không</span><span class="sxs-lookup"><span data-stu-id="63468-244">no</span></span>             | <span data-ttu-id="63468-245">không</span><span class="sxs-lookup"><span data-stu-id="63468-245">no</span></span>               |
| <span data-ttu-id="63468-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="63468-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="63468-247">không</span><span class="sxs-lookup"><span data-stu-id="63468-247">no</span></span>             | <span data-ttu-id="63468-248">không</span><span class="sxs-lookup"><span data-stu-id="63468-248">no</span></span>               |
| <span data-ttu-id="63468-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="63468-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="63468-250">không</span><span class="sxs-lookup"><span data-stu-id="63468-250">no</span></span>             | <span data-ttu-id="63468-251">không</span><span class="sxs-lookup"><span data-stu-id="63468-251">no</span></span>               |
| <span data-ttu-id="63468-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="63468-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="63468-253">không</span><span class="sxs-lookup"><span data-stu-id="63468-253">no</span></span>             | <span data-ttu-id="63468-254">không</span><span class="sxs-lookup"><span data-stu-id="63468-254">no</span></span>               |
| <span data-ttu-id="63468-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="63468-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="63468-256">không</span><span class="sxs-lookup"><span data-stu-id="63468-256">no</span></span>             | <span data-ttu-id="63468-257">không</span><span class="sxs-lookup"><span data-stu-id="63468-257">no</span></span>               |
| <span data-ttu-id="63468-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="63468-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="63468-259">không</span><span class="sxs-lookup"><span data-stu-id="63468-259">no</span></span>             | <span data-ttu-id="63468-260">không</span><span class="sxs-lookup"><span data-stu-id="63468-260">no</span></span>               |
| <span data-ttu-id="63468-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="63468-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="63468-262">không</span><span class="sxs-lookup"><span data-stu-id="63468-262">no</span></span>             | <span data-ttu-id="63468-263">không</span><span class="sxs-lookup"><span data-stu-id="63468-263">no</span></span>               |
| <span data-ttu-id="63468-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="63468-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="63468-265">không</span><span class="sxs-lookup"><span data-stu-id="63468-265">no</span></span>             | <span data-ttu-id="63468-266">không</span><span class="sxs-lookup"><span data-stu-id="63468-266">no</span></span>               |
| <span data-ttu-id="63468-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="63468-267">msdyn_progress</span></span>                         | <span data-ttu-id="63468-268">không</span><span class="sxs-lookup"><span data-stu-id="63468-268">no</span></span>             | <span data-ttu-id="63468-269">không (có cho P4W)</span><span class="sxs-lookup"><span data-stu-id="63468-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="63468-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="63468-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="63468-271">không</span><span class="sxs-lookup"><span data-stu-id="63468-271">no</span></span>             | <span data-ttu-id="63468-272">không</span><span class="sxs-lookup"><span data-stu-id="63468-272">no</span></span>               |
| <span data-ttu-id="63468-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="63468-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="63468-274">không</span><span class="sxs-lookup"><span data-stu-id="63468-274">no</span></span>             | <span data-ttu-id="63468-275">không</span><span class="sxs-lookup"><span data-stu-id="63468-275">no</span></span>               |
| <span data-ttu-id="63468-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="63468-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="63468-277">không</span><span class="sxs-lookup"><span data-stu-id="63468-277">no</span></span>             | <span data-ttu-id="63468-278">không</span><span class="sxs-lookup"><span data-stu-id="63468-278">no</span></span>               |
| <span data-ttu-id="63468-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="63468-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="63468-280">không</span><span class="sxs-lookup"><span data-stu-id="63468-280">no</span></span>             | <span data-ttu-id="63468-281">không</span><span class="sxs-lookup"><span data-stu-id="63468-281">no</span></span>               |
| <span data-ttu-id="63468-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="63468-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="63468-283">không</span><span class="sxs-lookup"><span data-stu-id="63468-283">no</span></span>             | <span data-ttu-id="63468-284">không</span><span class="sxs-lookup"><span data-stu-id="63468-284">no</span></span>               |
| <span data-ttu-id="63468-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="63468-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="63468-286">không</span><span class="sxs-lookup"><span data-stu-id="63468-286">no</span></span>             | <span data-ttu-id="63468-287">không</span><span class="sxs-lookup"><span data-stu-id="63468-287">no</span></span>               |
| <span data-ttu-id="63468-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="63468-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="63468-289">không</span><span class="sxs-lookup"><span data-stu-id="63468-289">no</span></span>             | <span data-ttu-id="63468-290">không</span><span class="sxs-lookup"><span data-stu-id="63468-290">no</span></span>               |
| <span data-ttu-id="63468-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="63468-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="63468-292">không</span><span class="sxs-lookup"><span data-stu-id="63468-292">no</span></span>             | <span data-ttu-id="63468-293">không</span><span class="sxs-lookup"><span data-stu-id="63468-293">no</span></span>               |
| <span data-ttu-id="63468-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="63468-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="63468-295">không</span><span class="sxs-lookup"><span data-stu-id="63468-295">no</span></span>             | <span data-ttu-id="63468-296">không</span><span class="sxs-lookup"><span data-stu-id="63468-296">no</span></span>               |
| <span data-ttu-id="63468-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="63468-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="63468-298">không</span><span class="sxs-lookup"><span data-stu-id="63468-298">no</span></span>             | <span data-ttu-id="63468-299">không</span><span class="sxs-lookup"><span data-stu-id="63468-299">no</span></span>               |
| <span data-ttu-id="63468-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="63468-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="63468-301">không</span><span class="sxs-lookup"><span data-stu-id="63468-301">no</span></span>             | <span data-ttu-id="63468-302">không</span><span class="sxs-lookup"><span data-stu-id="63468-302">no</span></span>               |
| <span data-ttu-id="63468-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="63468-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="63468-304">không</span><span class="sxs-lookup"><span data-stu-id="63468-304">no</span></span>             | <span data-ttu-id="63468-305">không</span><span class="sxs-lookup"><span data-stu-id="63468-305">no</span></span>               |
| <span data-ttu-id="63468-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="63468-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="63468-307">không</span><span class="sxs-lookup"><span data-stu-id="63468-307">no</span></span>             | <span data-ttu-id="63468-308">không</span><span class="sxs-lookup"><span data-stu-id="63468-308">no</span></span>               |
| <span data-ttu-id="63468-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="63468-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="63468-310">không</span><span class="sxs-lookup"><span data-stu-id="63468-310">no</span></span>             | <span data-ttu-id="63468-311">không</span><span class="sxs-lookup"><span data-stu-id="63468-311">no</span></span>               |
| <span data-ttu-id="63468-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="63468-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="63468-313">không</span><span class="sxs-lookup"><span data-stu-id="63468-313">no</span></span>             | <span data-ttu-id="63468-314">không</span><span class="sxs-lookup"><span data-stu-id="63468-314">no</span></span>               |
| <span data-ttu-id="63468-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="63468-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="63468-316">không</span><span class="sxs-lookup"><span data-stu-id="63468-316">no</span></span>             | <span data-ttu-id="63468-317">không</span><span class="sxs-lookup"><span data-stu-id="63468-317">no</span></span>               |
| <span data-ttu-id="63468-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="63468-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="63468-319">không</span><span class="sxs-lookup"><span data-stu-id="63468-319">no</span></span>             | <span data-ttu-id="63468-320">không</span><span class="sxs-lookup"><span data-stu-id="63468-320">no</span></span>               |
| <span data-ttu-id="63468-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="63468-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="63468-322">không</span><span class="sxs-lookup"><span data-stu-id="63468-322">no</span></span>             | <span data-ttu-id="63468-323">không</span><span class="sxs-lookup"><span data-stu-id="63468-323">no</span></span>               |
| <span data-ttu-id="63468-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="63468-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="63468-325">không</span><span class="sxs-lookup"><span data-stu-id="63468-325">no</span></span>             | <span data-ttu-id="63468-326">không</span><span class="sxs-lookup"><span data-stu-id="63468-326">no</span></span>               |
| <span data-ttu-id="63468-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="63468-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="63468-328">không</span><span class="sxs-lookup"><span data-stu-id="63468-328">no</span></span>             | <span data-ttu-id="63468-329">không</span><span class="sxs-lookup"><span data-stu-id="63468-329">no</span></span>               |
| <span data-ttu-id="63468-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="63468-330">msdyn_summary</span></span>                          | <span data-ttu-id="63468-331">không</span><span class="sxs-lookup"><span data-stu-id="63468-331">no</span></span>             | <span data-ttu-id="63468-332">không</span><span class="sxs-lookup"><span data-stu-id="63468-332">no</span></span>               |
| <span data-ttu-id="63468-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="63468-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="63468-334">không</span><span class="sxs-lookup"><span data-stu-id="63468-334">no</span></span>             | <span data-ttu-id="63468-335">không</span><span class="sxs-lookup"><span data-stu-id="63468-335">no</span></span>               |
| <span data-ttu-id="63468-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="63468-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="63468-337">không</span><span class="sxs-lookup"><span data-stu-id="63468-337">no</span></span>             | <span data-ttu-id="63468-338">không</span><span class="sxs-lookup"><span data-stu-id="63468-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="63468-339">Quan hệ phụ thuộc nhiệm vụ dự án</span><span class="sxs-lookup"><span data-stu-id="63468-339">Project task dependency</span></span>

| <span data-ttu-id="63468-340">**Tên lô-gic**</span><span class="sxs-lookup"><span data-stu-id="63468-340">**Logical name**</span></span>              | <span data-ttu-id="63468-341">**Có thể tạo**</span><span class="sxs-lookup"><span data-stu-id="63468-341">**Can create**</span></span> | <span data-ttu-id="63468-342">**Có thể chỉnh sửa**</span><span class="sxs-lookup"><span data-stu-id="63468-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="63468-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="63468-343">msdyn_linktype</span></span>                | <span data-ttu-id="63468-344">không</span><span class="sxs-lookup"><span data-stu-id="63468-344">no</span></span>             | <span data-ttu-id="63468-345">không</span><span class="sxs-lookup"><span data-stu-id="63468-345">no</span></span>           |
| <span data-ttu-id="63468-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="63468-346">msdyn_linktypename</span></span>            | <span data-ttu-id="63468-347">không</span><span class="sxs-lookup"><span data-stu-id="63468-347">no</span></span>             | <span data-ttu-id="63468-348">không</span><span class="sxs-lookup"><span data-stu-id="63468-348">no</span></span>           |
| <span data-ttu-id="63468-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="63468-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="63468-350">có</span><span class="sxs-lookup"><span data-stu-id="63468-350">yes</span></span>            | <span data-ttu-id="63468-351">không</span><span class="sxs-lookup"><span data-stu-id="63468-351">no</span></span>           |
| <span data-ttu-id="63468-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="63468-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="63468-353">có</span><span class="sxs-lookup"><span data-stu-id="63468-353">yes</span></span>            | <span data-ttu-id="63468-354">không</span><span class="sxs-lookup"><span data-stu-id="63468-354">no</span></span>           |
| <span data-ttu-id="63468-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="63468-355">msdyn_project</span></span>                 | <span data-ttu-id="63468-356">có</span><span class="sxs-lookup"><span data-stu-id="63468-356">yes</span></span>            | <span data-ttu-id="63468-357">không</span><span class="sxs-lookup"><span data-stu-id="63468-357">no</span></span>           |
| <span data-ttu-id="63468-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="63468-358">msdyn_projectname</span></span>             | <span data-ttu-id="63468-359">có</span><span class="sxs-lookup"><span data-stu-id="63468-359">yes</span></span>            | <span data-ttu-id="63468-360">không</span><span class="sxs-lookup"><span data-stu-id="63468-360">no</span></span>           |
| <span data-ttu-id="63468-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="63468-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="63468-362">có</span><span class="sxs-lookup"><span data-stu-id="63468-362">yes</span></span>            | <span data-ttu-id="63468-363">không</span><span class="sxs-lookup"><span data-stu-id="63468-363">no</span></span>           |
| <span data-ttu-id="63468-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="63468-364">msdyn_successortask</span></span>           | <span data-ttu-id="63468-365">có</span><span class="sxs-lookup"><span data-stu-id="63468-365">yes</span></span>            | <span data-ttu-id="63468-366">không</span><span class="sxs-lookup"><span data-stu-id="63468-366">no</span></span>           |
| <span data-ttu-id="63468-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="63468-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="63468-368">có</span><span class="sxs-lookup"><span data-stu-id="63468-368">yes</span></span>            | <span data-ttu-id="63468-369">không</span><span class="sxs-lookup"><span data-stu-id="63468-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="63468-370">Công việc giao cho nguồn lực</span><span class="sxs-lookup"><span data-stu-id="63468-370">Resource assignment</span></span>

| <span data-ttu-id="63468-371">**Tên lô-gic**</span><span class="sxs-lookup"><span data-stu-id="63468-371">**Logical name**</span></span>             | <span data-ttu-id="63468-372">**Có thể tạo**</span><span class="sxs-lookup"><span data-stu-id="63468-372">**Can create**</span></span> | <span data-ttu-id="63468-373">**Có thể chỉnh sửa**</span><span class="sxs-lookup"><span data-stu-id="63468-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="63468-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="63468-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="63468-375">có</span><span class="sxs-lookup"><span data-stu-id="63468-375">yes</span></span>            | <span data-ttu-id="63468-376">không</span><span class="sxs-lookup"><span data-stu-id="63468-376">no</span></span>           |
| <span data-ttu-id="63468-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="63468-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="63468-378">có</span><span class="sxs-lookup"><span data-stu-id="63468-378">yes</span></span>            | <span data-ttu-id="63468-379">không</span><span class="sxs-lookup"><span data-stu-id="63468-379">no</span></span>           |
| <span data-ttu-id="63468-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="63468-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="63468-381">không</span><span class="sxs-lookup"><span data-stu-id="63468-381">no</span></span>             | <span data-ttu-id="63468-382">không</span><span class="sxs-lookup"><span data-stu-id="63468-382">no</span></span>           |
| <span data-ttu-id="63468-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="63468-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="63468-384">không</span><span class="sxs-lookup"><span data-stu-id="63468-384">no</span></span>             | <span data-ttu-id="63468-385">không</span><span class="sxs-lookup"><span data-stu-id="63468-385">no</span></span>           |
| <span data-ttu-id="63468-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="63468-386">msdyn_committype</span></span>             | <span data-ttu-id="63468-387">không</span><span class="sxs-lookup"><span data-stu-id="63468-387">no</span></span>             | <span data-ttu-id="63468-388">không</span><span class="sxs-lookup"><span data-stu-id="63468-388">no</span></span>           |
| <span data-ttu-id="63468-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="63468-389">msdyn_committypename</span></span>         | <span data-ttu-id="63468-390">không</span><span class="sxs-lookup"><span data-stu-id="63468-390">no</span></span>             | <span data-ttu-id="63468-391">không</span><span class="sxs-lookup"><span data-stu-id="63468-391">no</span></span>           |
| <span data-ttu-id="63468-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="63468-392">msdyn_effort</span></span>                 | <span data-ttu-id="63468-393">không</span><span class="sxs-lookup"><span data-stu-id="63468-393">no</span></span>             | <span data-ttu-id="63468-394">không</span><span class="sxs-lookup"><span data-stu-id="63468-394">no</span></span>           |
| <span data-ttu-id="63468-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="63468-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="63468-396">không</span><span class="sxs-lookup"><span data-stu-id="63468-396">no</span></span>             | <span data-ttu-id="63468-397">không</span><span class="sxs-lookup"><span data-stu-id="63468-397">no</span></span>           |
| <span data-ttu-id="63468-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="63468-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="63468-399">không</span><span class="sxs-lookup"><span data-stu-id="63468-399">no</span></span>             | <span data-ttu-id="63468-400">không</span><span class="sxs-lookup"><span data-stu-id="63468-400">no</span></span>           |
| <span data-ttu-id="63468-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="63468-401">msdyn_finish</span></span>                 | <span data-ttu-id="63468-402">không</span><span class="sxs-lookup"><span data-stu-id="63468-402">no</span></span>             | <span data-ttu-id="63468-403">không</span><span class="sxs-lookup"><span data-stu-id="63468-403">no</span></span>           |
| <span data-ttu-id="63468-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="63468-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="63468-405">không</span><span class="sxs-lookup"><span data-stu-id="63468-405">no</span></span>             | <span data-ttu-id="63468-406">không</span><span class="sxs-lookup"><span data-stu-id="63468-406">no</span></span>           |
| <span data-ttu-id="63468-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="63468-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="63468-408">không</span><span class="sxs-lookup"><span data-stu-id="63468-408">no</span></span>             | <span data-ttu-id="63468-409">không</span><span class="sxs-lookup"><span data-stu-id="63468-409">no</span></span>           |
| <span data-ttu-id="63468-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="63468-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="63468-411">không</span><span class="sxs-lookup"><span data-stu-id="63468-411">no</span></span>             | <span data-ttu-id="63468-412">không</span><span class="sxs-lookup"><span data-stu-id="63468-412">no</span></span>           |
| <span data-ttu-id="63468-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="63468-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="63468-414">không</span><span class="sxs-lookup"><span data-stu-id="63468-414">no</span></span>             | <span data-ttu-id="63468-415">không</span><span class="sxs-lookup"><span data-stu-id="63468-415">no</span></span>           |
| <span data-ttu-id="63468-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="63468-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="63468-417">không</span><span class="sxs-lookup"><span data-stu-id="63468-417">no</span></span>             | <span data-ttu-id="63468-418">không</span><span class="sxs-lookup"><span data-stu-id="63468-418">no</span></span>           |
| <span data-ttu-id="63468-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="63468-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="63468-420">không</span><span class="sxs-lookup"><span data-stu-id="63468-420">no</span></span>             | <span data-ttu-id="63468-421">không</span><span class="sxs-lookup"><span data-stu-id="63468-421">no</span></span>           |
| <span data-ttu-id="63468-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="63468-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="63468-423">không</span><span class="sxs-lookup"><span data-stu-id="63468-423">no</span></span>             | <span data-ttu-id="63468-424">không</span><span class="sxs-lookup"><span data-stu-id="63468-424">no</span></span>           |
| <span data-ttu-id="63468-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="63468-425">msdyn_projectid</span></span>              | <span data-ttu-id="63468-426">có</span><span class="sxs-lookup"><span data-stu-id="63468-426">yes</span></span>            | <span data-ttu-id="63468-427">không</span><span class="sxs-lookup"><span data-stu-id="63468-427">no</span></span>           |
| <span data-ttu-id="63468-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="63468-428">msdyn_projectidname</span></span>          | <span data-ttu-id="63468-429">không</span><span class="sxs-lookup"><span data-stu-id="63468-429">no</span></span>             | <span data-ttu-id="63468-430">không</span><span class="sxs-lookup"><span data-stu-id="63468-430">no</span></span>           |
| <span data-ttu-id="63468-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="63468-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="63468-432">không</span><span class="sxs-lookup"><span data-stu-id="63468-432">no</span></span>             | <span data-ttu-id="63468-433">không</span><span class="sxs-lookup"><span data-stu-id="63468-433">no</span></span>           |
| <span data-ttu-id="63468-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="63468-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="63468-435">không</span><span class="sxs-lookup"><span data-stu-id="63468-435">no</span></span>             | <span data-ttu-id="63468-436">không</span><span class="sxs-lookup"><span data-stu-id="63468-436">no</span></span>           |
| <span data-ttu-id="63468-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="63468-437">msdyn_start</span></span>                  | <span data-ttu-id="63468-438">không</span><span class="sxs-lookup"><span data-stu-id="63468-438">no</span></span>             | <span data-ttu-id="63468-439">không</span><span class="sxs-lookup"><span data-stu-id="63468-439">no</span></span>           |
| <span data-ttu-id="63468-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="63468-440">msdyn_taskid</span></span>                 | <span data-ttu-id="63468-441">không</span><span class="sxs-lookup"><span data-stu-id="63468-441">no</span></span>             | <span data-ttu-id="63468-442">không</span><span class="sxs-lookup"><span data-stu-id="63468-442">no</span></span>           |
| <span data-ttu-id="63468-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="63468-443">msdyn_taskidname</span></span>             | <span data-ttu-id="63468-444">không</span><span class="sxs-lookup"><span data-stu-id="63468-444">no</span></span>             | <span data-ttu-id="63468-445">không</span><span class="sxs-lookup"><span data-stu-id="63468-445">no</span></span>           |
| <span data-ttu-id="63468-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="63468-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="63468-447">không</span><span class="sxs-lookup"><span data-stu-id="63468-447">no</span></span>             | <span data-ttu-id="63468-448">không</span><span class="sxs-lookup"><span data-stu-id="63468-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="63468-449">Thành viên nhóm dự án</span><span class="sxs-lookup"><span data-stu-id="63468-449">Project team member</span></span>

| <span data-ttu-id="63468-450">**Tên lô-gic**</span><span class="sxs-lookup"><span data-stu-id="63468-450">**Logical name**</span></span>                                 | <span data-ttu-id="63468-451">**Có thể tạo**</span><span class="sxs-lookup"><span data-stu-id="63468-451">**Can create**</span></span> | <span data-ttu-id="63468-452">**Có thể chỉnh sửa**</span><span class="sxs-lookup"><span data-stu-id="63468-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="63468-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="63468-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="63468-454">không</span><span class="sxs-lookup"><span data-stu-id="63468-454">no</span></span>             | <span data-ttu-id="63468-455">không</span><span class="sxs-lookup"><span data-stu-id="63468-455">no</span></span>           |
| <span data-ttu-id="63468-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="63468-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="63468-457">không</span><span class="sxs-lookup"><span data-stu-id="63468-457">no</span></span>             | <span data-ttu-id="63468-458">không</span><span class="sxs-lookup"><span data-stu-id="63468-458">no</span></span>           |
| <span data-ttu-id="63468-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="63468-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="63468-460">không</span><span class="sxs-lookup"><span data-stu-id="63468-460">no</span></span>             | <span data-ttu-id="63468-461">không</span><span class="sxs-lookup"><span data-stu-id="63468-461">no</span></span>           |
| <span data-ttu-id="63468-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="63468-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="63468-463">không</span><span class="sxs-lookup"><span data-stu-id="63468-463">no</span></span>             | <span data-ttu-id="63468-464">không</span><span class="sxs-lookup"><span data-stu-id="63468-464">no</span></span>           |
| <span data-ttu-id="63468-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="63468-465">msdyn_effort</span></span>                                     | <span data-ttu-id="63468-466">không</span><span class="sxs-lookup"><span data-stu-id="63468-466">no</span></span>             | <span data-ttu-id="63468-467">không</span><span class="sxs-lookup"><span data-stu-id="63468-467">no</span></span>           |
| <span data-ttu-id="63468-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="63468-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="63468-469">không</span><span class="sxs-lookup"><span data-stu-id="63468-469">no</span></span>             | <span data-ttu-id="63468-470">không</span><span class="sxs-lookup"><span data-stu-id="63468-470">no</span></span>           |
| <span data-ttu-id="63468-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="63468-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="63468-472">không</span><span class="sxs-lookup"><span data-stu-id="63468-472">no</span></span>             | <span data-ttu-id="63468-473">không</span><span class="sxs-lookup"><span data-stu-id="63468-473">no</span></span>           |
| <span data-ttu-id="63468-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="63468-474">msdyn_finish</span></span>                                     | <span data-ttu-id="63468-475">không</span><span class="sxs-lookup"><span data-stu-id="63468-475">no</span></span>             | <span data-ttu-id="63468-476">không</span><span class="sxs-lookup"><span data-stu-id="63468-476">no</span></span>           |
| <span data-ttu-id="63468-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="63468-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="63468-478">không</span><span class="sxs-lookup"><span data-stu-id="63468-478">no</span></span>             | <span data-ttu-id="63468-479">không</span><span class="sxs-lookup"><span data-stu-id="63468-479">no</span></span>           |
| <span data-ttu-id="63468-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="63468-480">msdyn_hours</span></span>                                      | <span data-ttu-id="63468-481">không</span><span class="sxs-lookup"><span data-stu-id="63468-481">no</span></span>             | <span data-ttu-id="63468-482">không</span><span class="sxs-lookup"><span data-stu-id="63468-482">no</span></span>           |
| <span data-ttu-id="63468-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="63468-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="63468-484">không</span><span class="sxs-lookup"><span data-stu-id="63468-484">no</span></span>             | <span data-ttu-id="63468-485">không</span><span class="sxs-lookup"><span data-stu-id="63468-485">no</span></span>           |
| <span data-ttu-id="63468-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="63468-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="63468-487">không</span><span class="sxs-lookup"><span data-stu-id="63468-487">no</span></span>             | <span data-ttu-id="63468-488">không</span><span class="sxs-lookup"><span data-stu-id="63468-488">no</span></span>           |
| <span data-ttu-id="63468-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="63468-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="63468-490">không</span><span class="sxs-lookup"><span data-stu-id="63468-490">no</span></span>             | <span data-ttu-id="63468-491">không</span><span class="sxs-lookup"><span data-stu-id="63468-491">no</span></span>           |
| <span data-ttu-id="63468-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="63468-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="63468-493">không</span><span class="sxs-lookup"><span data-stu-id="63468-493">no</span></span>             | <span data-ttu-id="63468-494">không</span><span class="sxs-lookup"><span data-stu-id="63468-494">no</span></span>           |
| <span data-ttu-id="63468-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="63468-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="63468-496">không</span><span class="sxs-lookup"><span data-stu-id="63468-496">no</span></span>             | <span data-ttu-id="63468-497">không</span><span class="sxs-lookup"><span data-stu-id="63468-497">no</span></span>           |
| <span data-ttu-id="63468-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="63468-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="63468-499">không</span><span class="sxs-lookup"><span data-stu-id="63468-499">no</span></span>             | <span data-ttu-id="63468-500">không</span><span class="sxs-lookup"><span data-stu-id="63468-500">no</span></span>           |
| <span data-ttu-id="63468-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="63468-501">msdyn_start</span></span>                                      | <span data-ttu-id="63468-502">không</span><span class="sxs-lookup"><span data-stu-id="63468-502">no</span></span>             | <span data-ttu-id="63468-503">không</span><span class="sxs-lookup"><span data-stu-id="63468-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="63468-504">Dự án</span><span class="sxs-lookup"><span data-stu-id="63468-504">Project</span></span>

| <span data-ttu-id="63468-505">**Tên lô-gic**</span><span class="sxs-lookup"><span data-stu-id="63468-505">**Logical name**</span></span>                       | <span data-ttu-id="63468-506">**Có thể tạo**</span><span class="sxs-lookup"><span data-stu-id="63468-506">**Can create**</span></span> | <span data-ttu-id="63468-507">**Có thể chỉnh sửa**</span><span class="sxs-lookup"><span data-stu-id="63468-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="63468-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="63468-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="63468-509">không</span><span class="sxs-lookup"><span data-stu-id="63468-509">no</span></span>             | <span data-ttu-id="63468-510">không</span><span class="sxs-lookup"><span data-stu-id="63468-510">no</span></span>           |
| <span data-ttu-id="63468-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="63468-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="63468-512">không</span><span class="sxs-lookup"><span data-stu-id="63468-512">no</span></span>             | <span data-ttu-id="63468-513">không</span><span class="sxs-lookup"><span data-stu-id="63468-513">no</span></span>           |
| <span data-ttu-id="63468-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="63468-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="63468-515">không</span><span class="sxs-lookup"><span data-stu-id="63468-515">no</span></span>             | <span data-ttu-id="63468-516">không</span><span class="sxs-lookup"><span data-stu-id="63468-516">no</span></span>           |
| <span data-ttu-id="63468-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="63468-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="63468-518">không</span><span class="sxs-lookup"><span data-stu-id="63468-518">no</span></span>             | <span data-ttu-id="63468-519">không</span><span class="sxs-lookup"><span data-stu-id="63468-519">no</span></span>           |
| <span data-ttu-id="63468-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="63468-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="63468-521">không</span><span class="sxs-lookup"><span data-stu-id="63468-521">no</span></span>             | <span data-ttu-id="63468-522">không</span><span class="sxs-lookup"><span data-stu-id="63468-522">no</span></span>           |
| <span data-ttu-id="63468-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="63468-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="63468-524">không</span><span class="sxs-lookup"><span data-stu-id="63468-524">no</span></span>             | <span data-ttu-id="63468-525">không</span><span class="sxs-lookup"><span data-stu-id="63468-525">no</span></span>           |
| <span data-ttu-id="63468-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="63468-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="63468-527">có</span><span class="sxs-lookup"><span data-stu-id="63468-527">yes</span></span>            | <span data-ttu-id="63468-528">không</span><span class="sxs-lookup"><span data-stu-id="63468-528">no</span></span>           |
| <span data-ttu-id="63468-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="63468-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="63468-530">có</span><span class="sxs-lookup"><span data-stu-id="63468-530">yes</span></span>            | <span data-ttu-id="63468-531">không</span><span class="sxs-lookup"><span data-stu-id="63468-531">no</span></span>           |
| <span data-ttu-id="63468-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="63468-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="63468-533">có</span><span class="sxs-lookup"><span data-stu-id="63468-533">yes</span></span>            | <span data-ttu-id="63468-534">không</span><span class="sxs-lookup"><span data-stu-id="63468-534">no</span></span>           |
| <span data-ttu-id="63468-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="63468-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="63468-536">không</span><span class="sxs-lookup"><span data-stu-id="63468-536">no</span></span>             | <span data-ttu-id="63468-537">không</span><span class="sxs-lookup"><span data-stu-id="63468-537">no</span></span>           |
| <span data-ttu-id="63468-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="63468-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="63468-539">không</span><span class="sxs-lookup"><span data-stu-id="63468-539">no</span></span>             | <span data-ttu-id="63468-540">không</span><span class="sxs-lookup"><span data-stu-id="63468-540">no</span></span>           |
| <span data-ttu-id="63468-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="63468-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="63468-542">không</span><span class="sxs-lookup"><span data-stu-id="63468-542">no</span></span>             | <span data-ttu-id="63468-543">không</span><span class="sxs-lookup"><span data-stu-id="63468-543">no</span></span>           |
| <span data-ttu-id="63468-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="63468-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="63468-545">không</span><span class="sxs-lookup"><span data-stu-id="63468-545">no</span></span>             | <span data-ttu-id="63468-546">không</span><span class="sxs-lookup"><span data-stu-id="63468-546">no</span></span>           |
| <span data-ttu-id="63468-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="63468-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="63468-548">không</span><span class="sxs-lookup"><span data-stu-id="63468-548">no</span></span>             | <span data-ttu-id="63468-549">không</span><span class="sxs-lookup"><span data-stu-id="63468-549">no</span></span>           |
| <span data-ttu-id="63468-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="63468-550">msdyn_duration</span></span>                         | <span data-ttu-id="63468-551">không</span><span class="sxs-lookup"><span data-stu-id="63468-551">no</span></span>             | <span data-ttu-id="63468-552">không</span><span class="sxs-lookup"><span data-stu-id="63468-552">no</span></span>           |
| <span data-ttu-id="63468-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="63468-553">msdyn_effort</span></span>                           | <span data-ttu-id="63468-554">không</span><span class="sxs-lookup"><span data-stu-id="63468-554">no</span></span>             | <span data-ttu-id="63468-555">không</span><span class="sxs-lookup"><span data-stu-id="63468-555">no</span></span>           |
| <span data-ttu-id="63468-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="63468-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="63468-557">không</span><span class="sxs-lookup"><span data-stu-id="63468-557">no</span></span>             | <span data-ttu-id="63468-558">không</span><span class="sxs-lookup"><span data-stu-id="63468-558">no</span></span>           |
| <span data-ttu-id="63468-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="63468-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="63468-560">không</span><span class="sxs-lookup"><span data-stu-id="63468-560">no</span></span>             | <span data-ttu-id="63468-561">không</span><span class="sxs-lookup"><span data-stu-id="63468-561">no</span></span>           |
| <span data-ttu-id="63468-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="63468-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="63468-563">không</span><span class="sxs-lookup"><span data-stu-id="63468-563">no</span></span>             | <span data-ttu-id="63468-564">không</span><span class="sxs-lookup"><span data-stu-id="63468-564">no</span></span>           |
| <span data-ttu-id="63468-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="63468-565">msdyn_finish</span></span>                           | <span data-ttu-id="63468-566">có</span><span class="sxs-lookup"><span data-stu-id="63468-566">yes</span></span>            | <span data-ttu-id="63468-567">có</span><span class="sxs-lookup"><span data-stu-id="63468-567">yes</span></span>          |
| <span data-ttu-id="63468-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="63468-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="63468-569">không</span><span class="sxs-lookup"><span data-stu-id="63468-569">no</span></span>             | <span data-ttu-id="63468-570">không</span><span class="sxs-lookup"><span data-stu-id="63468-570">no</span></span>           |
| <span data-ttu-id="63468-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="63468-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="63468-572">không</span><span class="sxs-lookup"><span data-stu-id="63468-572">no</span></span>             | <span data-ttu-id="63468-573">không</span><span class="sxs-lookup"><span data-stu-id="63468-573">no</span></span>           |
| <span data-ttu-id="63468-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="63468-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="63468-575">không</span><span class="sxs-lookup"><span data-stu-id="63468-575">no</span></span>             | <span data-ttu-id="63468-576">không</span><span class="sxs-lookup"><span data-stu-id="63468-576">no</span></span>           |
| <span data-ttu-id="63468-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="63468-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="63468-578">không</span><span class="sxs-lookup"><span data-stu-id="63468-578">no</span></span>             | <span data-ttu-id="63468-579">không</span><span class="sxs-lookup"><span data-stu-id="63468-579">no</span></span>           |
| <span data-ttu-id="63468-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="63468-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="63468-581">không</span><span class="sxs-lookup"><span data-stu-id="63468-581">no</span></span>             | <span data-ttu-id="63468-582">không</span><span class="sxs-lookup"><span data-stu-id="63468-582">no</span></span>           |
| <span data-ttu-id="63468-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="63468-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="63468-584">không</span><span class="sxs-lookup"><span data-stu-id="63468-584">no</span></span>             | <span data-ttu-id="63468-585">không</span><span class="sxs-lookup"><span data-stu-id="63468-585">no</span></span>           |
| <span data-ttu-id="63468-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="63468-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="63468-587">không</span><span class="sxs-lookup"><span data-stu-id="63468-587">no</span></span>             | <span data-ttu-id="63468-588">không</span><span class="sxs-lookup"><span data-stu-id="63468-588">no</span></span>           |
| <span data-ttu-id="63468-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="63468-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="63468-590">không</span><span class="sxs-lookup"><span data-stu-id="63468-590">no</span></span>             | <span data-ttu-id="63468-591">không</span><span class="sxs-lookup"><span data-stu-id="63468-591">no</span></span>           |
| <span data-ttu-id="63468-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="63468-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="63468-593">không</span><span class="sxs-lookup"><span data-stu-id="63468-593">no</span></span>             | <span data-ttu-id="63468-594">không</span><span class="sxs-lookup"><span data-stu-id="63468-594">no</span></span>           |
| <span data-ttu-id="63468-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="63468-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="63468-596">không</span><span class="sxs-lookup"><span data-stu-id="63468-596">no</span></span>             | <span data-ttu-id="63468-597">không</span><span class="sxs-lookup"><span data-stu-id="63468-597">no</span></span>           |
| <span data-ttu-id="63468-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="63468-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="63468-599">không</span><span class="sxs-lookup"><span data-stu-id="63468-599">no</span></span>             | <span data-ttu-id="63468-600">không</span><span class="sxs-lookup"><span data-stu-id="63468-600">no</span></span>           |
| <span data-ttu-id="63468-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="63468-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="63468-602">không</span><span class="sxs-lookup"><span data-stu-id="63468-602">no</span></span>             | <span data-ttu-id="63468-603">không</span><span class="sxs-lookup"><span data-stu-id="63468-603">no</span></span>           |
| <span data-ttu-id="63468-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="63468-604">msdyn_progress</span></span>                         | <span data-ttu-id="63468-605">không</span><span class="sxs-lookup"><span data-stu-id="63468-605">no</span></span>             | <span data-ttu-id="63468-606">không</span><span class="sxs-lookup"><span data-stu-id="63468-606">no</span></span>           |
| <span data-ttu-id="63468-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="63468-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="63468-608">không</span><span class="sxs-lookup"><span data-stu-id="63468-608">no</span></span>             | <span data-ttu-id="63468-609">không</span><span class="sxs-lookup"><span data-stu-id="63468-609">no</span></span>           |
| <span data-ttu-id="63468-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="63468-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="63468-611">không</span><span class="sxs-lookup"><span data-stu-id="63468-611">no</span></span>             | <span data-ttu-id="63468-612">không</span><span class="sxs-lookup"><span data-stu-id="63468-612">no</span></span>           |
| <span data-ttu-id="63468-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="63468-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="63468-614">không</span><span class="sxs-lookup"><span data-stu-id="63468-614">no</span></span>             | <span data-ttu-id="63468-615">không</span><span class="sxs-lookup"><span data-stu-id="63468-615">no</span></span>           |
| <span data-ttu-id="63468-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="63468-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="63468-617">không</span><span class="sxs-lookup"><span data-stu-id="63468-617">no</span></span>             | <span data-ttu-id="63468-618">không</span><span class="sxs-lookup"><span data-stu-id="63468-618">no</span></span>           |
| <span data-ttu-id="63468-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="63468-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="63468-620">không</span><span class="sxs-lookup"><span data-stu-id="63468-620">no</span></span>             | <span data-ttu-id="63468-621">không</span><span class="sxs-lookup"><span data-stu-id="63468-621">no</span></span>           |
| <span data-ttu-id="63468-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="63468-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="63468-623">không</span><span class="sxs-lookup"><span data-stu-id="63468-623">no</span></span>             | <span data-ttu-id="63468-624">không</span><span class="sxs-lookup"><span data-stu-id="63468-624">no</span></span>           |
| <span data-ttu-id="63468-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="63468-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="63468-626">không</span><span class="sxs-lookup"><span data-stu-id="63468-626">no</span></span>             | <span data-ttu-id="63468-627">không</span><span class="sxs-lookup"><span data-stu-id="63468-627">no</span></span>           |
| <span data-ttu-id="63468-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="63468-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="63468-629">không</span><span class="sxs-lookup"><span data-stu-id="63468-629">no</span></span>             | <span data-ttu-id="63468-630">không</span><span class="sxs-lookup"><span data-stu-id="63468-630">no</span></span>           |
| <span data-ttu-id="63468-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="63468-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="63468-632">không</span><span class="sxs-lookup"><span data-stu-id="63468-632">no</span></span>             | <span data-ttu-id="63468-633">không</span><span class="sxs-lookup"><span data-stu-id="63468-633">no</span></span>           |
| <span data-ttu-id="63468-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="63468-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="63468-635">không</span><span class="sxs-lookup"><span data-stu-id="63468-635">no</span></span>             | <span data-ttu-id="63468-636">không</span><span class="sxs-lookup"><span data-stu-id="63468-636">no</span></span>           |
| <span data-ttu-id="63468-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="63468-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="63468-638">không</span><span class="sxs-lookup"><span data-stu-id="63468-638">no</span></span>             | <span data-ttu-id="63468-639">không</span><span class="sxs-lookup"><span data-stu-id="63468-639">no</span></span>           |
| <span data-ttu-id="63468-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="63468-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="63468-641">không</span><span class="sxs-lookup"><span data-stu-id="63468-641">no</span></span>             | <span data-ttu-id="63468-642">không</span><span class="sxs-lookup"><span data-stu-id="63468-642">no</span></span>           |
| <span data-ttu-id="63468-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="63468-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="63468-644">không</span><span class="sxs-lookup"><span data-stu-id="63468-644">no</span></span>             | <span data-ttu-id="63468-645">không</span><span class="sxs-lookup"><span data-stu-id="63468-645">no</span></span>           |
| <span data-ttu-id="63468-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="63468-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="63468-647">không</span><span class="sxs-lookup"><span data-stu-id="63468-647">no</span></span>             | <span data-ttu-id="63468-648">không</span><span class="sxs-lookup"><span data-stu-id="63468-648">no</span></span>           |
| <span data-ttu-id="63468-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="63468-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="63468-650">không</span><span class="sxs-lookup"><span data-stu-id="63468-650">no</span></span>             | <span data-ttu-id="63468-651">không</span><span class="sxs-lookup"><span data-stu-id="63468-651">no</span></span>           |
| <span data-ttu-id="63468-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="63468-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="63468-653">không</span><span class="sxs-lookup"><span data-stu-id="63468-653">no</span></span>             | <span data-ttu-id="63468-654">không</span><span class="sxs-lookup"><span data-stu-id="63468-654">no</span></span>           |
| <span data-ttu-id="63468-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="63468-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="63468-656">không</span><span class="sxs-lookup"><span data-stu-id="63468-656">no</span></span>             | <span data-ttu-id="63468-657">không</span><span class="sxs-lookup"><span data-stu-id="63468-657">no</span></span>           |
| <span data-ttu-id="63468-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="63468-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="63468-659">không</span><span class="sxs-lookup"><span data-stu-id="63468-659">no</span></span>             | <span data-ttu-id="63468-660">không</span><span class="sxs-lookup"><span data-stu-id="63468-660">no</span></span>           |
| <span data-ttu-id="63468-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="63468-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="63468-662">không</span><span class="sxs-lookup"><span data-stu-id="63468-662">no</span></span>             | <span data-ttu-id="63468-663">không</span><span class="sxs-lookup"><span data-stu-id="63468-663">no</span></span>           |
| <span data-ttu-id="63468-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="63468-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="63468-665">không</span><span class="sxs-lookup"><span data-stu-id="63468-665">no</span></span>             | <span data-ttu-id="63468-666">không</span><span class="sxs-lookup"><span data-stu-id="63468-666">no</span></span>           |
| <span data-ttu-id="63468-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="63468-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="63468-668">không</span><span class="sxs-lookup"><span data-stu-id="63468-668">no</span></span>             | <span data-ttu-id="63468-669">không</span><span class="sxs-lookup"><span data-stu-id="63468-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="63468-670">Các giới hạn và vấn đề đã biết</span><span class="sxs-lookup"><span data-stu-id="63468-670">Limitations and known issues</span></span>
<span data-ttu-id="63468-671">Sau đây là danh sách các giới hạn và vấn đề đã biết:</span><span class="sxs-lookup"><span data-stu-id="63468-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="63468-672">API lịch trình dự án chỉ có thể được sử dụng bởi **Người dùng có Giấy phép dự án của Microsoft.**</span><span class="sxs-lookup"><span data-stu-id="63468-672">Project Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="63468-673">Những đối tượng sau không thể sử dụng API lịch trình:</span><span class="sxs-lookup"><span data-stu-id="63468-673">They can't be used by:</span></span>
    - <span data-ttu-id="63468-674">Người dùng ứng dụng</span><span class="sxs-lookup"><span data-stu-id="63468-674">Application users</span></span>
    - <span data-ttu-id="63468-675">Người dùng hệ thống</span><span class="sxs-lookup"><span data-stu-id="63468-675">System users</span></span>
    - <span data-ttu-id="63468-676">Người dùng tích hợp</span><span class="sxs-lookup"><span data-stu-id="63468-676">Integration users</span></span>
    - <span data-ttu-id="63468-677">Những người dùng khác không có giấy phép bắt buộc</span><span class="sxs-lookup"><span data-stu-id="63468-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="63468-678">Mỗi **OperationSet** chỉ có thể có tối đa 100 thao tác.</span><span class="sxs-lookup"><span data-stu-id="63468-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="63468-679">Mỗi người dùng chỉ có tối đa 10 **OperationSets** đang mở.</span><span class="sxs-lookup"><span data-stu-id="63468-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="63468-680">Project Operations hiện hỗ trợ tổng cộng tối đa 500 nhiệm vụ trên một dự án.</span><span class="sxs-lookup"><span data-stu-id="63468-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="63468-681">Hiện không có nhật ký lỗi và trạng thái lỗi **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="63468-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- [<span data-ttu-id="63468-682">Giới hạn và ranh giới đối với các dự án và nhiệm vụ</span><span class="sxs-lookup"><span data-stu-id="63468-682">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="63468-683">Xử lý lỗi</span><span class="sxs-lookup"><span data-stu-id="63468-683">Error handling</span></span>

   - <span data-ttu-id="63468-684">Để xem lại các lỗi được tạo từ Bộ hoạt động, hãy chuyển đến phần **Cài đặt** \> **Tích hợp lịch biểu** \> **Bộ hoạt động**.</span><span class="sxs-lookup"><span data-stu-id="63468-684">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="63468-685">Để xem lại các lỗi được tạo ra từ Dịch vụ lịch trình dự án, hãy truy cập **Cài đặt** \> **Tích hợp lịch trình** \> **Nhật ký lỗi PSS**.</span><span class="sxs-lookup"><span data-stu-id="63468-685">To review errors generated from the Project schedule Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="63468-686">Kịch bản mẫu</span><span class="sxs-lookup"><span data-stu-id="63468-686">Sample scenario</span></span>

<span data-ttu-id="63468-687">Trong kịch bản này, bạn sẽ tạo một dự án, một thành viên nhóm, bốn nhiệm vụ và hai công việc giao cho nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="63468-687">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="63468-688">Tiếp theo, bạn sẽ cập nhật một nhiệm vụ, cập nhật dự án, xóa một nhiệm vụ, xóa một công việc giao cho nguồn lực và tạo một quan hệ phụ thuộc nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="63468-688">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

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

## <a name="additional-samples"></a><span data-ttu-id="63468-689">Các mẫu khác</span><span class="sxs-lookup"><span data-stu-id="63468-689">Additional samples</span></span>

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
