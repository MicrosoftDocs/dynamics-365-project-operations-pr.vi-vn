---
title: Thay đổi quản lý nguồn lực (Project Service Automation 3.x)
description: Chủ đề này cung cấp thông tin về các thay đổi cho Khu vực quản lý nguồn lực.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 5176d2c6b7b00d47d4aeb12f54bdb84d4b87304c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087299"
---
# <a name="resource-management-changes-project-service-automation-3x"></a><span data-ttu-id="ca75f-103">Thay đổi quản lý nguồn lực (Project Service Automation 3.x)</span><span class="sxs-lookup"><span data-stu-id="ca75f-103">Resource management changes (Project Service Automation 3.x)</span></span>

<span data-ttu-id="ca75f-104">Các phần của chủ đề này cung cấp thông tin về những thay đổi đã được thực hiện cho Khu vực quản lý nguồn lực của phiên bản Dynamics 365 Project Service Automation 3.x.</span><span class="sxs-lookup"><span data-stu-id="ca75f-104">The sections of this topic provide information about the changes that have been made to the Resource management area of Dynamics 365 Project Service Automation version 3.x.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="ca75f-105">Ước tính dự án</span><span class="sxs-lookup"><span data-stu-id="ca75f-105">Project estimates</span></span>

<span data-ttu-id="ca75f-106">Thay vì dựa trên thực thể **msdyn\_projecttask** ( **Nhiệm vụ dự án** ), ước tính dự án dựa trên thực thể **msdyn\_resourceassignment** ( **Phân công nguồn lực** ).</span><span class="sxs-lookup"><span data-stu-id="ca75f-106">Instead of being based on the **msdyn\_projecttask** entity ( **Project Task** ), project estimates are based on the **msdyn\_resourceassignment** entity ( **Resource Assignment** ).</span></span> <span data-ttu-id="ca75f-107">Phân công nguồn lực đã trở thành "nguồn tin cậy" cho định giá và lập lịch nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="ca75f-107">Resource assignments have become the "source of truth" for task scheduling and pricing.</span></span>

## <a name="line-tasks"></a><span data-ttu-id="ca75f-108">Nhiệm vụ mô tả</span><span class="sxs-lookup"><span data-stu-id="ca75f-108">Line tasks</span></span>

<span data-ttu-id="ca75f-109">Trong PSA 3.x, nhiệm vụ mô tả đã lỗi thời (không dùng nữa).</span><span class="sxs-lookup"><span data-stu-id="ca75f-109">In PSA 3.x, line tasks are obsolete (deprecated).</span></span> <span data-ttu-id="ca75f-110">Phân công hiện hướng đến toàn bộ nhiệm vụ thay vì nhiệm vụ mô tả.</span><span class="sxs-lookup"><span data-stu-id="ca75f-110">Assignments now point to the whole task instead of the line tasks.</span></span>

<span data-ttu-id="ca75f-111">Các ví dụ sau hiển thị cách một nhiệm vụ được đặt tên "Nhiệm vụ kiểm tra" được gán cho thành viên nhóm A và B trong phiên bản cũ hơn của PSA và trong PSA 3.x.</span><span class="sxs-lookup"><span data-stu-id="ca75f-111">The following example shows how a task that is named "Test task" is assigned to team members A and B in earlier versions of PSA and in PSA 3.x.</span></span>

- <span data-ttu-id="ca75f-112">**Trước PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="ca75f-112">**Before PSA 3.x:**</span></span>

    - <span data-ttu-id="ca75f-113">Nhiệm vụ kiểm tra</span><span class="sxs-lookup"><span data-stu-id="ca75f-113">Test task</span></span>

        - <span data-ttu-id="ca75f-114">Nhiệm vụ kiểm tra – Nhiệm vụ mô tả 1</span><span class="sxs-lookup"><span data-stu-id="ca75f-114">Test task – Line task 1</span></span>

            - <span data-ttu-id="ca75f-115">Phân công cho A</span><span class="sxs-lookup"><span data-stu-id="ca75f-115">Assignment to A</span></span>

        - <span data-ttu-id="ca75f-116">Nhiệm vụ kiểm tra – Nhiệm vụ mô tả 2</span><span class="sxs-lookup"><span data-stu-id="ca75f-116">Test task – Line task 2</span></span>

            - <span data-ttu-id="ca75f-117">Phân công cho B</span><span class="sxs-lookup"><span data-stu-id="ca75f-117">Assignment to B</span></span>

- <span data-ttu-id="ca75f-118">**PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="ca75f-118">**PSA 3.x:**</span></span>

    - <span data-ttu-id="ca75f-119">Nhiệm vụ kiểm tra</span><span class="sxs-lookup"><span data-stu-id="ca75f-119">Test task</span></span>

        - <span data-ttu-id="ca75f-120">Phân công cho A</span><span class="sxs-lookup"><span data-stu-id="ca75f-120">Assignment to A</span></span>
        - <span data-ttu-id="ca75f-121">Phân công cho B</span><span class="sxs-lookup"><span data-stu-id="ca75f-121">Assignment to B</span></span>

## <a name="unassigned-assignment"></a><span data-ttu-id="ca75f-122">Phân công chưa được chỉ định</span><span class="sxs-lookup"><span data-stu-id="ca75f-122">Unassigned assignment</span></span>

<span data-ttu-id="ca75f-123">Trong PSA 3.x, phân công chưa được chỉ định là phân công được chỉ định cho thành viên nhóm **NULL** và nguồn lực **NULL**.</span><span class="sxs-lookup"><span data-stu-id="ca75f-123">In PSA 3.x, an unassigned assignment is an assignment that is assigned to a **NULL** team member and a **NULL** resource.</span></span> <span data-ttu-id="ca75f-124">Phân công chưa được chỉ định có thể xảy ra trong một vài trường hợp:</span><span class="sxs-lookup"><span data-stu-id="ca75f-124">Unassigned assignments can occur in a couple of scenarios:</span></span>

- <span data-ttu-id="ca75f-125">Nếu một nhiệm vụ đã được tạo nhưng chưa được phân công cho bất kỳ thành viên nhóm này, thì phân công chưa được chỉ định luôn được tạo.</span><span class="sxs-lookup"><span data-stu-id="ca75f-125">If a task has been created, but it hasn't yet been assigned to any team member, an unassigned assignment is always created.</span></span> 
- <span data-ttu-id="ca75f-126">Nếu tất cả người được chỉ định trên nhiệm vụ bị xóa, nhiệm vụ chưa được chỉ định được tạo lại cho nhiệm vụ đó.</span><span class="sxs-lookup"><span data-stu-id="ca75f-126">If all assignees on a task are removed, an unassigned assignment is re-created for that task.</span></span>

## <a name="scheduling-fields-on-the-project-task-entity"></a><span data-ttu-id="ca75f-127">Lập lịch các trường trên thực thể Nhiệm vụ dự án</span><span class="sxs-lookup"><span data-stu-id="ca75f-127">Scheduling fields on the Project Task entity</span></span>

<span data-ttu-id="ca75f-128">Các trường trên thực thể **msdyn\_projecttask** được chấp nhận hoặc chuyển đến thực thể **msdyn\_resourceassignment** hoặc chúng hiện được tham chiếu từ thực thể **msdyn\_projectteam** ( **Thành viên nhóm dự án** ).</span><span class="sxs-lookup"><span data-stu-id="ca75f-128">The fields on the **msdyn\_projecttask** entity have been deprecated or moved to the **msdyn\_resourceassignment** entity, or they are now referenced from the **msdyn\_projectteam** entity ( **Project Team Member** ).</span></span>

| <span data-ttu-id="ca75f-129">Trường không dùng nữa trên msdyn\_projecttask (Nhiệm vụ dự án)</span><span class="sxs-lookup"><span data-stu-id="ca75f-129">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="ca75f-130">Trường mới trên msdyn\_resourceassignment (Phân công nguồn lực)</span><span class="sxs-lookup"><span data-stu-id="ca75f-130">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> | <span data-ttu-id="ca75f-131">Nhận xét</span><span class="sxs-lookup"><span data-stu-id="ca75f-131">Comment</span></span> |
|---|---|---|
| <span data-ttu-id="ca75f-132">msdyn\_assignedresources</span><span class="sxs-lookup"><span data-stu-id="ca75f-132">msdyn\_assignedresources</span></span> | <span data-ttu-id="ca75f-133">Không</span><span class="sxs-lookup"><span data-stu-id="ca75f-133">None</span></span> | |
| <span data-ttu-id="ca75f-134">msdyn\_assignedteammembers</span><span class="sxs-lookup"><span data-stu-id="ca75f-134">msdyn\_assignedteammembers</span></span> | <span data-ttu-id="ca75f-135">Không</span><span class="sxs-lookup"><span data-stu-id="ca75f-135">None</span></span> | |
| <span data-ttu-id="ca75f-136">msdyn\_numberofresources</span><span class="sxs-lookup"><span data-stu-id="ca75f-136">msdyn\_numberofresources</span></span> | <span data-ttu-id="ca75f-137">Không</span><span class="sxs-lookup"><span data-stu-id="ca75f-137">None</span></span> | |
| <span data-ttu-id="ca75f-138">msdyn\_scheduledhours</span><span class="sxs-lookup"><span data-stu-id="ca75f-138">msdyn\_scheduledhours</span></span> | <span data-ttu-id="ca75f-139">Không</span><span class="sxs-lookup"><span data-stu-id="ca75f-139">None</span></span> | |
| <span data-ttu-id="ca75f-140">msdyn\_effortcontour</span><span class="sxs-lookup"><span data-stu-id="ca75f-140">msdyn\_effortcontour</span></span> | <span data-ttu-id="ca75f-141">msdyn\_plannedwork</span><span class="sxs-lookup"><span data-stu-id="ca75f-141">msdyn\_plannedwork</span></span> | <span data-ttu-id="ca75f-142">Định dạng của cấu trúc dữ liệu Ký hiệu đối tượng JavaScript (JSON) được lưu trữ trong trường đã được thay đổi.</span><span class="sxs-lookup"><span data-stu-id="ca75f-142">The format of the JavaScript Object Notation (JSON) data structure that is stored in the field has been changed.</span></span> |

## <a name="schedule-contour"></a><span data-ttu-id="ca75f-143">Đường cong lịch trình</span><span class="sxs-lookup"><span data-stu-id="ca75f-143">Schedule contour</span></span>

<span data-ttu-id="ca75f-144">Đường cong lịch trình được lưu trữ trong trường **Công việc theo kế hoạch** ( **msdyn\_plannedwork** ) của từng thực thể **Phân công nguồn lực** ( **msdyn\_resourceassignment** ).</span><span class="sxs-lookup"><span data-stu-id="ca75f-144">The schedule contour is stored in the **Planned Work** field ( **msdyn\_plannedwork** ) of each **Resource Assignment** entity ( **msdyn\_resourceassignment** ).</span></span>

### <a name="structure"></a><span data-ttu-id="ca75f-145">Cấu trúc</span><span class="sxs-lookup"><span data-stu-id="ca75f-145">Structure</span></span>

<span data-ttu-id="ca75f-146">Cấu trúc mới của đường cong lịch trình bao gồm lát cắt thời gian linh hoạt được xác định cho từng ngày của lịch trình.</span><span class="sxs-lookup"><span data-stu-id="ca75f-146">The new structure of the schedule contour consists of flexible time slices that are defined for each day of the schedule.</span></span> <span data-ttu-id="ca75f-147">Mỗi lát cắt thời gian có các thuộc tính sau:</span><span class="sxs-lookup"><span data-stu-id="ca75f-147">Each time slice has the following properties:</span></span>

- <span data-ttu-id="ca75f-148">**Bắt đầu** – Bắt đầu giờ làm việc cho ngày, theo lịch dự án.</span><span class="sxs-lookup"><span data-stu-id="ca75f-148">**Start** – The start of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="ca75f-149">**Kết thúc** – Kết thúc giờ làm việc cho ngày, theo lịch dự án.</span><span class="sxs-lookup"><span data-stu-id="ca75f-149">**End** – The end of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="ca75f-150">**Giờ** – Số giờ được chỉ định vào ngày này.</span><span class="sxs-lookup"><span data-stu-id="ca75f-150">**Hours** – The number of hours that are assigned on the day.</span></span>

<span data-ttu-id="ca75f-151">**Ví dụ**</span><span class="sxs-lookup"><span data-stu-id="ca75f-151">**Example**</span></span>

<span data-ttu-id="ca75f-152">Ví dụ này sử dụng lịch dự án mà ngày làm việc từ 9:00 sáng đến 5:00 chiều theo múi giờ UTC-8.</span><span class="sxs-lookup"><span data-stu-id="ca75f-152">This example uses a project calendar where the workday is from 9 AM to 5 PM in the UTC-8 time zone.</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a><span data-ttu-id="ca75f-153">Tự động lập lịch và lập lịch theo cách thủ công</span><span class="sxs-lookup"><span data-stu-id="ca75f-153">Auto-scheduling and manual scheduling</span></span>

<span data-ttu-id="ca75f-154">Nếu một nhiệm vụ được lập lịch tự động, giờ được tải trước và khoảng thời gian nhiệm vụ có thể bị giảm.</span><span class="sxs-lookup"><span data-stu-id="ca75f-154">If a task is auto-scheduled, the hours are front-loaded, and the task duration might be reduced.</span></span>

<span data-ttu-id="ca75f-155">**Ví dụ**</span><span class="sxs-lookup"><span data-stu-id="ca75f-155">**Example**</span></span>

<span data-ttu-id="ca75f-156">Nhiệm vụ sau đây được tự động lập lịch trong 18 giờ trong ba ngày (ngày 3 tháng 12 năm 2018 đến ngày 5 tháng 12 năm 2018).</span><span class="sxs-lookup"><span data-stu-id="ca75f-156">The following task is auto-scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

<span data-ttu-id="ca75f-157">Nếu một nhiệm vụ được lập lịch theo cách thủ công, giờ được phân phối đều cho tất cả các ngày.</span><span class="sxs-lookup"><span data-stu-id="ca75f-157">If a task is manually scheduled, the hours are evenly distributed to all the dates.</span></span>

<span data-ttu-id="ca75f-158">**Ví dụ**</span><span class="sxs-lookup"><span data-stu-id="ca75f-158">**Example**</span></span>

<span data-ttu-id="ca75f-159">Nhiệm vụ sau đây được lập lịch theo cách thủ công trong 18 giờ trong ba ngày (ngày 3 tháng 12 năm 2018 đến ngày 5 tháng 12 năm 2018).</span><span class="sxs-lookup"><span data-stu-id="ca75f-159">The following task is manually scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a><span data-ttu-id="ca75f-160">Đơn vị phân công</span><span class="sxs-lookup"><span data-stu-id="ca75f-160">Assignment unit</span></span>

<span data-ttu-id="ca75f-161">Đơn vị phân công không còn dùng nữa trong PSA 3.x.</span><span class="sxs-lookup"><span data-stu-id="ca75f-161">The assignment unit has been deprecated in PSA 3.x.</span></span> <span data-ttu-id="ca75f-162">Giờ nhân công nhiệm vụ hiện được chia đều, mỗi ngày, trong tất cả nguồn lực được phân công.</span><span class="sxs-lookup"><span data-stu-id="ca75f-162">The task effort hours are now equally divided, per day, among all the assigned resources.</span></span>

<span data-ttu-id="ca75f-163">**Ví dụ**</span><span class="sxs-lookup"><span data-stu-id="ca75f-163">**Example**</span></span>

<span data-ttu-id="ca75f-164">Trong ví dụ này, nhiệm vụ được phân công cho 2 nguồn lực và được tự động lập lịch cho 36 giờ trong 3 ngày (ngày 3 tháng 12 năm 2018 đến ngày 5 tháng 12 năm 2018).</span><span class="sxs-lookup"><span data-stu-id="ca75f-164">In this example, the task is is assigned to two resources and is auto-scheduled for 36 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

- <span data-ttu-id="ca75f-165">Phân công 1:</span><span class="sxs-lookup"><span data-stu-id="ca75f-165">Assignment 1:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- <span data-ttu-id="ca75f-166">Phân công 2:</span><span class="sxs-lookup"><span data-stu-id="ca75f-166">Assignment 2:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a><span data-ttu-id="ca75f-167">Tham số giá</span><span class="sxs-lookup"><span data-stu-id="ca75f-167">Pricing dimensions</span></span>

<span data-ttu-id="ca75f-168">Trong PSA 3.x, trường tham số giá dành riêng cho nguồn lực (chẳng hạn như **Vai trò** và **Đơn vị tổ chức** ) bị xóa khỏi thực thể **msdyn\_projecttask**.</span><span class="sxs-lookup"><span data-stu-id="ca75f-168">In PSA 3.x, resource-specific pricing dimension fields (such as **Role** and **Organizational Unit** ) have been removed from the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="ca75f-169">Các trường này hiện có thể được lấy từ thành viên nhóm dự án tương ứng ( **msdyn\_projectteam** ) của phân công nguồn lực ( **msdyn\_resourceassignment** ) khi ước tính dự án được tạo.</span><span class="sxs-lookup"><span data-stu-id="ca75f-169">These fields can now be retrieved from the corresponding project team member ( **msdyn\_projectteam** ) of the resource assignment ( **msdyn\_resourceassignment** ) when project estimates are generated.</span></span> <span data-ttu-id="ca75f-170">Một trường mới, **msdyn\_OrganizationalUnit** , đã được thêm vào thực thể **thể msdyn\_projectteam**.</span><span class="sxs-lookup"><span data-stu-id="ca75f-170">A new field, **msdyn\_organizationalunit** , has been added to the **msdyn\_projectteam** entity.</span></span>

| <span data-ttu-id="ca75f-171">Trường không dùng nữa trên msdyn\_projecttask (Nhiệm vụ dự án)</span><span class="sxs-lookup"><span data-stu-id="ca75f-171">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="ca75f-172">Trường từ msdyn\_projectteam (Thành viên nhóm dự án) được sử dụng thay thế</span><span class="sxs-lookup"><span data-stu-id="ca75f-172">Field from msdyn\_projectteam (Project Team Member) that is used instead</span></span> |
|---|---|
| <span data-ttu-id="ca75f-173">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="ca75f-173">msdyn\_resourcecategory</span></span> | <span data-ttu-id="ca75f-174">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="ca75f-174">msdyn\_resourcecategory</span></span> |
| <span data-ttu-id="ca75f-175">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="ca75f-175">msdyn\_organizationalunit</span></span> | <span data-ttu-id="ca75f-176">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="ca75f-176">msdyn\_organizationalunit</span></span> |

## <a name="contours"></a><span data-ttu-id="ca75f-177">Đường cong</span><span class="sxs-lookup"><span data-stu-id="ca75f-177">Contours</span></span>

<span data-ttu-id="ca75f-178">Các trường đường cong ước tính và giá không còn được dùng trên thực thể **msdyn\_projecttask**.</span><span class="sxs-lookup"><span data-stu-id="ca75f-178">The pricing and estimation contour fields have been deprecated on the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="ca75f-179">Họ đã được chuyển đến thực thể **msdyn\_resourceassignment**.</span><span class="sxs-lookup"><span data-stu-id="ca75f-179">They have been moved to the **msdyn\_resourceassignment** entity.</span></span>

| <span data-ttu-id="ca75f-180">Trường không dùng nữa trên msdyn\_projecttask (Nhiệm vụ dự án)</span><span class="sxs-lookup"><span data-stu-id="ca75f-180">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="ca75f-181">Trường mới trên msdyn\_resourceassignment (Phân công nguồn lực)</span><span class="sxs-lookup"><span data-stu-id="ca75f-181">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> |
|---|---|
| <span data-ttu-id="ca75f-182">msdyn\_costestimatecontour</span><span class="sxs-lookup"><span data-stu-id="ca75f-182">msdyn\_costestimatecontour</span></span> | <span data-ttu-id="ca75f-183">msdyn\_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="ca75f-183">msdyn\_plannedcostcontour</span></span> |
| <span data-ttu-id="ca75f-184">msdyn\_salesestimatecontour</span><span class="sxs-lookup"><span data-stu-id="ca75f-184">msdyn\_salesestimatecontour</span></span> | <span data-ttu-id="ca75f-185">msdyn\_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="ca75f-185">msdyn\_plannedsalescontour</span></span> |

<span data-ttu-id="ca75f-186">Các trường sau được thêm vào thực thể **msdyn\_resourceassignment** :</span><span class="sxs-lookup"><span data-stu-id="ca75f-186">The following fields have been added to the **msdyn\_resourceassignment** entity:</span></span>

* <span data-ttu-id="ca75f-187">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="ca75f-187">msdyn\_plannedcost</span></span>
* <span data-ttu-id="ca75f-188">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="ca75f-188">msdyn\_plannedsales</span></span>

<span data-ttu-id="ca75f-189">Các trường sau cho chi phí và doanh thu dự kiến, thực tế và còn lại không bị thay đổi trên thực thể **msdyn\_projecttask** :</span><span class="sxs-lookup"><span data-stu-id="ca75f-189">The following fields for planned, actual, and remaining cost and sales are unchanged on the **msdyn\_projecttask** entity:</span></span>

* <span data-ttu-id="ca75f-190">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="ca75f-190">msdyn\_plannedcost</span></span>
* <span data-ttu-id="ca75f-191">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="ca75f-191">msdyn\_plannedsales</span></span>
* <span data-ttu-id="ca75f-192">msdyn\_actualcost</span><span class="sxs-lookup"><span data-stu-id="ca75f-192">msdyn\_actualcost</span></span>
* <span data-ttu-id="ca75f-193">msdyn\_actualsales</span><span class="sxs-lookup"><span data-stu-id="ca75f-193">msdyn\_actualsales</span></span>
* <span data-ttu-id="ca75f-194">msdyn\_remainingcost</span><span class="sxs-lookup"><span data-stu-id="ca75f-194">msdyn\_remainingcost</span></span>
* <span data-ttu-id="ca75f-195">msdyn\_remainingsales</span><span class="sxs-lookup"><span data-stu-id="ca75f-195">msdyn\_remainingsales</span></span>
