---
title: Sử dụng API lịch trình để thực hiện các hoạt động với các thực thể Lập lịch trình
description: Chủ đề này cung cấp thông tin và mẫu để sử dụng API lịch trình.
author: sigitac
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a50a2c6220bb49de8146d0758019827e120e0526
ms.sourcegitcommit: 8ff9fe396db6dec581c21cd6bb9acc2691c815b0
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/07/2021
ms.locfileid: "5868155"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="8d804-103">Sử dụng API lịch trình để thực hiện các hoạt động với các thực thể Lập lịch trình</span><span class="sxs-lookup"><span data-stu-id="8d804-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="8d804-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="8d804-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="8d804-105">Một số hoặc tất cả chức năng được ghi chú trong chủ đề này khả dụng như một phần của bản phát hành xem trước.</span><span class="sxs-lookup"><span data-stu-id="8d804-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="8d804-106">Nội dung và chức năng có thể thay đổi.</span><span class="sxs-lookup"><span data-stu-id="8d804-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="8d804-107">Thực thể lập lịch trình</span><span class="sxs-lookup"><span data-stu-id="8d804-107">Scheduling entities</span></span>

<span data-ttu-id="8d804-108">API lịch trình cung cấp khả năng thực hiện các thao tác tạo, cập nhật và xóa với **Thực thể lập lịch trình**.</span><span class="sxs-lookup"><span data-stu-id="8d804-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="8d804-109">Các thực thể này được quản lý thông qua công cụ Lập lịch trình trong Dự án cho web.</span><span class="sxs-lookup"><span data-stu-id="8d804-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="8d804-110">Các thao tác tạo, cập nhật và xóa với **Thực thể lập lịch trình** đã bị hạn chế trong các bản phát hành Dynamics 365 Project Operations trước đó.</span><span class="sxs-lookup"><span data-stu-id="8d804-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="8d804-111">Bảng sau cung cấp danh sách đầy đủ các **Thực thể lập lịch trình**.</span><span class="sxs-lookup"><span data-stu-id="8d804-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="8d804-112">Tên thực thể</span><span class="sxs-lookup"><span data-stu-id="8d804-112">Entity name</span></span>  | <span data-ttu-id="8d804-113">Tên logic của thực thể</span><span class="sxs-lookup"><span data-stu-id="8d804-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="8d804-114">Dự án</span><span class="sxs-lookup"><span data-stu-id="8d804-114">Project</span></span> | <span data-ttu-id="8d804-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="8d804-115">msdyn_project</span></span> |
| <span data-ttu-id="8d804-116">Nhiệm vụ dự án</span><span class="sxs-lookup"><span data-stu-id="8d804-116">Project Task</span></span>  | <span data-ttu-id="8d804-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="8d804-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="8d804-118">Quan hệ phụ thuộc Nhiệm vụ Dự án</span><span class="sxs-lookup"><span data-stu-id="8d804-118">Project Task Dependency</span></span>  | <span data-ttu-id="8d804-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="8d804-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="8d804-120">Gán Nguồn lực</span><span class="sxs-lookup"><span data-stu-id="8d804-120">Resource Assignment</span></span> | <span data-ttu-id="8d804-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="8d804-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="8d804-122">Bộ chứa Dự án</span><span class="sxs-lookup"><span data-stu-id="8d804-122">Project Bucket</span></span>  | <span data-ttu-id="8d804-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="8d804-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="8d804-124">Thành viên Nhóm Dự án</span><span class="sxs-lookup"><span data-stu-id="8d804-124">Project Team Member</span></span> | <span data-ttu-id="8d804-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="8d804-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="8d804-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="8d804-126">OperationSet</span></span>

<span data-ttu-id="8d804-127">OperationSet là một mẫu đơn vị công việc có thể được sử dụng khi phải xử lý một số yêu cầu tác động lên lịch trình trong một giao dịch.</span><span class="sxs-lookup"><span data-stu-id="8d804-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="8d804-128">API lịch trình</span><span class="sxs-lookup"><span data-stu-id="8d804-128">Schedule APIs</span></span>

<span data-ttu-id="8d804-129">Sau đây là danh sách các API lịch trình hiện tại.</span><span class="sxs-lookup"><span data-stu-id="8d804-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="8d804-130">**msdyn_CreateProjectV1**: API này có thể được dùng để tạo một dự án.</span><span class="sxs-lookup"><span data-stu-id="8d804-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="8d804-131">Nhóm dự án và dự án mặc định được tạo ngay lập tức.</span><span class="sxs-lookup"><span data-stu-id="8d804-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="8d804-132">**msdyn_CreateTeamMemberV1**: API này có thể được dùng để tạo một thành viên trong nhóm dự án.</span><span class="sxs-lookup"><span data-stu-id="8d804-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="8d804-133">Hồ sơ thành viên trong nhóm được tạo ngay lập tức.</span><span class="sxs-lookup"><span data-stu-id="8d804-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="8d804-134">**msdyn_CreateOperationSetV1**: API này có thể được dùng để lập lịch trình một số yêu cầu phải được thực hiện trong một giao dịch.</span><span class="sxs-lookup"><span data-stu-id="8d804-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="8d804-135">**msdyn_PSSCreateV1**: API này có thể được dùng để tạo một thực thể.</span><span class="sxs-lookup"><span data-stu-id="8d804-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="8d804-136">Thực thể có thể là bất kỳ thực thể Lập lịch trình nào hỗ trợ thao tác tạo.</span><span class="sxs-lookup"><span data-stu-id="8d804-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="8d804-137">**msdyn_PSSUpdateV1**: API này có thể được dùng để cập nhật một thực thể.</span><span class="sxs-lookup"><span data-stu-id="8d804-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="8d804-138">Thực thể có thể là bất kỳ thực thể Lập lịch trình nào hỗ trợ thao tác cập nhật.</span><span class="sxs-lookup"><span data-stu-id="8d804-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="8d804-139">**msdyn_PSSDeleteV1**: API này có thể được dùng để xóa một thực thể.</span><span class="sxs-lookup"><span data-stu-id="8d804-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="8d804-140">Thực thể có thể là bất kỳ thực thể Lập lịch trình nào hỗ trợ thao tác xóa.</span><span class="sxs-lookup"><span data-stu-id="8d804-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="8d804-141">**msdyn_ExecuteOperationSetV1**: API này được dùng để thực thi tất cả các thao tác trong nhóm thao tác nhất định.</span><span class="sxs-lookup"><span data-stu-id="8d804-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="8d804-142">Sử dụng API lịch trình với OperationSet</span><span class="sxs-lookup"><span data-stu-id="8d804-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="8d804-143">Bởi vì bản ghi có cả **CreateProjectV1** và **CreateTeamMemberV1** được tạo ngay lập tức, nên không thể dùng các API này trực tiếp trong **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="8d804-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="8d804-144">Tuy nhiên, bạn có thể sử dụng API để tạo các bản ghi cần thiết, tạo một **OperationSet**, sau đó sử dụng các bản ghi được tạo trước này trong **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="8d804-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="8d804-145">Thao tác được hỗ trợ</span><span class="sxs-lookup"><span data-stu-id="8d804-145">Supported operations</span></span>

| <span data-ttu-id="8d804-146">Thực thể lập lịch trình</span><span class="sxs-lookup"><span data-stu-id="8d804-146">Scheduling entity</span></span> | <span data-ttu-id="8d804-147">Tạo</span><span class="sxs-lookup"><span data-stu-id="8d804-147">Create</span></span> | <span data-ttu-id="8d804-148">Update</span><span class="sxs-lookup"><span data-stu-id="8d804-148">Update</span></span> | <span data-ttu-id="8d804-149">Delete</span><span class="sxs-lookup"><span data-stu-id="8d804-149">Delete</span></span> | <span data-ttu-id="8d804-150">Những điều quan trọng cần cân nhắc</span><span class="sxs-lookup"><span data-stu-id="8d804-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="8d804-151">Nhiệm vụ dự án</span><span class="sxs-lookup"><span data-stu-id="8d804-151">Project task</span></span> | <span data-ttu-id="8d804-152">Có</span><span class="sxs-lookup"><span data-stu-id="8d804-152">Yes</span></span> | <span data-ttu-id="8d804-153">Có</span><span class="sxs-lookup"><span data-stu-id="8d804-153">Yes</span></span> | <span data-ttu-id="8d804-154">Có</span><span class="sxs-lookup"><span data-stu-id="8d804-154">Yes</span></span> | <span data-ttu-id="8d804-155">Không có</span><span class="sxs-lookup"><span data-stu-id="8d804-155">None</span></span> |
| <span data-ttu-id="8d804-156">Quan hệ phụ thuộc nhiệm vụ dự án</span><span class="sxs-lookup"><span data-stu-id="8d804-156">Project task dependency</span></span> | <span data-ttu-id="8d804-157">Có</span><span class="sxs-lookup"><span data-stu-id="8d804-157">Yes</span></span> | <span data-ttu-id="8d804-158">Có</span><span class="sxs-lookup"><span data-stu-id="8d804-158">Yes</span></span> | | <span data-ttu-id="8d804-159">Bản ghi quan hệ phụ thuộc nhiệm vụ dự án không được cập nhật.</span><span class="sxs-lookup"><span data-stu-id="8d804-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="8d804-160">Thay vào đó, một bản ghi cũ có thể bị xóa và một bản ghi mới có thể được tạo.</span><span class="sxs-lookup"><span data-stu-id="8d804-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="8d804-161">Công việc giao cho nguồn lực</span><span class="sxs-lookup"><span data-stu-id="8d804-161">Resource assignment</span></span> | <span data-ttu-id="8d804-162">Có</span><span class="sxs-lookup"><span data-stu-id="8d804-162">Yes</span></span> | <span data-ttu-id="8d804-163">Có</span><span class="sxs-lookup"><span data-stu-id="8d804-163">Yes</span></span> | | <span data-ttu-id="8d804-164">Không hỗ trợ thao tác với các trường sau: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** và **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="8d804-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="8d804-165">Bản ghi việc được giao không được cập nhật.</span><span class="sxs-lookup"><span data-stu-id="8d804-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="8d804-166">Thay vào đó, một bản ghi cũ có thể bị xóa và một bản ghi mới có thể được tạo.</span><span class="sxs-lookup"><span data-stu-id="8d804-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="8d804-167">Nhóm dự án</span><span class="sxs-lookup"><span data-stu-id="8d804-167">Project bucket</span></span> | <span data-ttu-id="8d804-168">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="8d804-168">N/A</span></span> | <span data-ttu-id="8d804-169">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="8d804-169">N/A</span></span> | <span data-ttu-id="8d804-170">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="8d804-170">N/A</span></span> | <span data-ttu-id="8d804-171">Nhóm mặc định được tạo bằng cách sử dụng API **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="8d804-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="8d804-172">Thành viên nhóm dự án</span><span class="sxs-lookup"><span data-stu-id="8d804-172">Project team member</span></span> | <span data-ttu-id="8d804-173">Có</span><span class="sxs-lookup"><span data-stu-id="8d804-173">Yes</span></span> | <span data-ttu-id="8d804-174">Có</span><span class="sxs-lookup"><span data-stu-id="8d804-174">Yes</span></span> | <span data-ttu-id="8d804-175">Có</span><span class="sxs-lookup"><span data-stu-id="8d804-175">Yes</span></span> | <span data-ttu-id="8d804-176">Đối với thao tác tạo, hãy sử dụng API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="8d804-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="8d804-177">Dự án</span><span class="sxs-lookup"><span data-stu-id="8d804-177">Project</span></span> | <span data-ttu-id="8d804-178">Có</span><span class="sxs-lookup"><span data-stu-id="8d804-178">Yes</span></span> | <span data-ttu-id="8d804-179">Có</span><span class="sxs-lookup"><span data-stu-id="8d804-179">Yes</span></span> | <span data-ttu-id="8d804-180">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="8d804-180">N/A</span></span> | <span data-ttu-id="8d804-181">Không hỗ trợ thao tác với các trường sau: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** và **Duration**.</span><span class="sxs-lookup"><span data-stu-id="8d804-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="8d804-182">Các API này có thể được gọi ra với các đối tượng thực thể bao gồm các trường tùy chỉnh.</span><span class="sxs-lookup"><span data-stu-id="8d804-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="8d804-183">Thuộc tính ID là không bắt buộc.</span><span class="sxs-lookup"><span data-stu-id="8d804-183">The ID property is optional.</span></span> <span data-ttu-id="8d804-184">Nếu được cung cấp, hệ thống sẽ cố gắng sử dụng ID thuộc tính và đưa ra một ngoại lệ nếu không thể sử dụng.</span><span class="sxs-lookup"><span data-stu-id="8d804-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="8d804-185">Nếu không được cung cấp, hệ thống sẽ tạo ID thuộc tính.</span><span class="sxs-lookup"><span data-stu-id="8d804-185">If it isn't provided, the system will generate it.</span></span>

## <a name="limitations-and-known-issues"></a><span data-ttu-id="8d804-186">Các giới hạn và vấn đề đã biết</span><span class="sxs-lookup"><span data-stu-id="8d804-186">Limitations and known issues</span></span>
<span data-ttu-id="8d804-187">Sau đây là danh sách các giới hạn và vấn đề đã biết:</span><span class="sxs-lookup"><span data-stu-id="8d804-187">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="8d804-188">Chỉ **Người dùng có giấy phép dự án của Microsoft** là có thể sử dụng API lịch trình.</span><span class="sxs-lookup"><span data-stu-id="8d804-188">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="8d804-189">Những đối tượng sau không thể sử dụng API lịch trình:</span><span class="sxs-lookup"><span data-stu-id="8d804-189">They can't be used by:</span></span>
    - <span data-ttu-id="8d804-190">Người dùng ứng dụng</span><span class="sxs-lookup"><span data-stu-id="8d804-190">Application users</span></span>
    - <span data-ttu-id="8d804-191">Người dùng hệ thống</span><span class="sxs-lookup"><span data-stu-id="8d804-191">System users</span></span>
    - <span data-ttu-id="8d804-192">Người dùng tích hợp</span><span class="sxs-lookup"><span data-stu-id="8d804-192">Integration users</span></span>
    - <span data-ttu-id="8d804-193">Những người dùng khác không có giấy phép bắt buộc</span><span class="sxs-lookup"><span data-stu-id="8d804-193">Other users that don't have the required license</span></span>
- <span data-ttu-id="8d804-194">Mỗi **OperationSet** chỉ có thể có tối đa 100 thao tác.</span><span class="sxs-lookup"><span data-stu-id="8d804-194">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="8d804-195">Mỗi người dùng chỉ có tối đa 10 **OperationSets** đang mở.</span><span class="sxs-lookup"><span data-stu-id="8d804-195">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="8d804-196">Project Operations hiện hỗ trợ tổng cộng tối đa 500 nhiệm vụ trên một dự án.</span><span class="sxs-lookup"><span data-stu-id="8d804-196">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="8d804-197">Hiện không có nhật ký lỗi và trạng thái lỗi **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="8d804-197">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- <span data-ttu-id="8d804-198">API lịch trình ở Bản xem trước công khai.</span><span class="sxs-lookup"><span data-stu-id="8d804-198">Schedule APIs are in Public preview.</span></span> <span data-ttu-id="8d804-199">Microsoft không hỗ trợ sử dụng các API này trong Môi trường sản xuất.</span><span class="sxs-lookup"><span data-stu-id="8d804-199">Using these APIs in a Production environment isn't supported by Microsoft.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="8d804-200">Kịch bản mẫu</span><span class="sxs-lookup"><span data-stu-id="8d804-200">Sample scenario</span></span>

<span data-ttu-id="8d804-201">Trong kịch bản này, bạn sẽ tạo một dự án, một thành viên nhóm, bốn nhiệm vụ và hai công việc giao cho nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="8d804-201">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="8d804-202">Tiếp theo, bạn sẽ cập nhật một nhiệm vụ, cập nhật dự án, xóa một nhiệm vụ, xóa một công việc giao cho nguồn lực và tạo một quan hệ phụ thuộc nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="8d804-202">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```C#
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
var task4 = GetTask("4ZZ";, projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment"R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

varassignment1Response = CallPssCreateAction(assignment1, operationSetId);
varassignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

varassignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="8d804-203">Các mẫu khác</span><span class="sxs-lookup"><span data-stu-id="8d804-203">Additional samples</span></span>

```C#
#region Call actions 

///<summary>
/// Calls the action to create an operationSet
/// </summary>
/// <paramname="projectId">project id for the operations to be included in this operationSet>/param>
/// <paramname="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
privatestring CallCreateOperationSetAction(Guid projectId, string description)
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
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary<
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet Id</param>
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
/// <summary>
/// <paramname="recordId">Id of the record to be deleted</param>
/// <paramname="entityLogicalName">Entity logical name of the record</param>
/// <paramname="operationSetId">OperationSet Id</param>
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
/// <summary>
/// <paramname="operationSetId">operationSet id</param>
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
/// <paramname="operationSetId">operationSet id</param>
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
/// <paramname="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1";
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);

    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <paramname="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
privatestring CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject><OperationSetResponse>
    ((string)orgResponse.Results["OperationSetResponse";]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet(";msdyn_project", "msdyn_name");
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
    task["msdyn_effort";] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
        task["new_custom1"] = "Just my test";
        task[";new_age"] = 98;
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
publicclassOperationSetResponse
{
    [DataMember(Name = "operationSetId")]
    public Guid OperationSetId { get; set; }

    [DataMember(Name = "operationSetDetailId")]
    public Guid OperationSetDetailId { get; set; }

    [DataMember(Name = "operationType")]
    publicstring OperationType { get; set; }

    [DataMember(Name = "recordId")]
    publicstring RecordId { get; set; }

    [DataMember(Name = "correlationId")]
    publicstring CorrelationId { get; set; }
}

#endregion
```
