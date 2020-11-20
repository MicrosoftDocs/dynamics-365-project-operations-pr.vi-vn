---
title: Lên lịch dự án với cấu trúc phân tích công việc
description: Làm cách nào để lên lịch dự án bằng cấu trúc phân tích công việc trong Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 04f30f2f2ed93dd1525f1c86a7521cdbf39a77bc
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127904"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a><span data-ttu-id="38a4b-103">Lên lịch dự án bằng cấu trúc phân tích công việc (Project Service)</span><span class="sxs-lookup"><span data-stu-id="38a4b-103">Schedule a project with a work breakdown structure (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="38a4b-104">Lịch trình dự án cho biết những việc cần được thực hiện, nguồn lực nào sẽ thực hiện công việc và khung thời gian cần hoàn thành công việc.</span><span class="sxs-lookup"><span data-stu-id="38a4b-104">A project schedule communicates what work needs to be performed, which resources will perform the work, and the timeframe in which that work needs to be completed.</span></span> <span data-ttu-id="38a4b-105">Lịch trình dự án phản ánh tất cả công việc liên quan đến việc cung cấp dự án đúng thời gian.</span><span class="sxs-lookup"><span data-stu-id="38a4b-105">The project schedule reflects all the work associated with delivering the project on time.</span></span> <span data-ttu-id="38a4b-106">Một trong những bước đầu tiên trong giai đoạn khởi đầu của dự án là tạo lịch trình dự án.</span><span class="sxs-lookup"><span data-stu-id="38a4b-106">One of the first steps in the initiation phase of the project is to come up with a project schedule.</span></span> <span data-ttu-id="38a4b-107">Để thiết lập một lịch trình dự án, bạn cần phải tạo một cấu trúc phân tích công việc.</span><span class="sxs-lookup"><span data-stu-id="38a4b-107">To establish a project schedule, you need to create a work breakdown structure.</span></span>  
  
 <span data-ttu-id="38a4b-108">Tạo cấu trúc dự án với cấu trúc phân tích công việc giúp bạn:</span><span class="sxs-lookup"><span data-stu-id="38a4b-108">Create a project structure with a work breakdown structure, which helps you:</span></span>  
  
- <span data-ttu-id="38a4b-109">Phân tích công việc thành các nhiệm vụ có thể quản lý</span><span class="sxs-lookup"><span data-stu-id="38a4b-109">Break down work into manageable tasks</span></span>  
  
- <span data-ttu-id="38a4b-110">Ước tính thời gian cần thiết để hoàn thành công việc</span><span class="sxs-lookup"><span data-stu-id="38a4b-110">Estimate the time required to complete a task</span></span>  
  
- <span data-ttu-id="38a4b-111">Thiết lập đối tượng phụ thuộc nhiệm vụ và khoảng thời gian của nhiệm vụ</span><span class="sxs-lookup"><span data-stu-id="38a4b-111">Set task dependencies and task duration</span></span>  
  
- <span data-ttu-id="38a4b-112">Xác định vai trò cần thiết để hoàn thành mỗi nhiệm vụ</span><span class="sxs-lookup"><span data-stu-id="38a4b-112">Determine the roles required to complete each task</span></span>  
  
  <span data-ttu-id="38a4b-113">Lịch trình dự án trong cấu trúc phân tích công việc có giao diện quen thuộc, hoàn chỉnh với biểu đồ Gantt tương tác.</span><span class="sxs-lookup"><span data-stu-id="38a4b-113">The project schedule in the work breakdown structure has a familiar look and feel, complete with an interactive Gantt chart.</span></span>  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a><span data-ttu-id="38a4b-114">Tạo cấu trúc phân tích công việc cho một dự án</span><span class="sxs-lookup"><span data-stu-id="38a4b-114">Create a work breakdown structure for a project</span></span>  
 <span data-ttu-id="38a4b-115">Tạo cấu trúc phân tích công việc đại diện cho chuỗi các nhiệm vụ trong một dự án.</span><span class="sxs-lookup"><span data-stu-id="38a4b-115">Create a work breakdown structure to represent the sequence of tasks in a project.</span></span> <span data-ttu-id="38a4b-116">Cấu trúc phân tích công việc bao gồm các nhiệm vụ, yêu cầu đối với từng nhiệm vụ và thông tin về doanh thu và chi phí.</span><span class="sxs-lookup"><span data-stu-id="38a4b-116">The work breakdown structure includes tasks, requirements for each task, and revenue and cost information.</span></span> <span data-ttu-id="38a4b-117">Trong cấu trúc phân tích công việc của bạn, bạn có thể thêm:</span><span class="sxs-lookup"><span data-stu-id="38a4b-117">In your work breakdown structure, you can add:</span></span>  
  
-   <span data-ttu-id="38a4b-118">Trình tự nhiệm vụ trong một hệ thống cấp bậc</span><span class="sxs-lookup"><span data-stu-id="38a4b-118">The sequence of tasks in a hierarchy</span></span>  
  
-   <span data-ttu-id="38a4b-119">Các nhiệm vụ khác, nếu có, phải được hoàn thành trước khi có thể bắt đầu một nhiệm vụ</span><span class="sxs-lookup"><span data-stu-id="38a4b-119">Other tasks, if any, that must be completed before a task can be started</span></span>  
  
-   <span data-ttu-id="38a4b-120">Ngày bắt đầu, ngày kết thúc và khoảng thời gian của nhiệm vụ</span><span class="sxs-lookup"><span data-stu-id="38a4b-120">The starting date, ending date, and duration of a task</span></span>  
  
-   <span data-ttu-id="38a4b-121">Số giờ cần cho một nhiệm vụ</span><span class="sxs-lookup"><span data-stu-id="38a4b-121">The number of hours required for a task</span></span>  
  
-   <span data-ttu-id="38a4b-122">Mọi kỹ năng và bằng cấp công nhân được yêu cầu</span><span class="sxs-lookup"><span data-stu-id="38a4b-122">Any required worker skills and education</span></span>  
  
-   <span data-ttu-id="38a4b-123">Công nhân được giao nhiệm vụ</span><span class="sxs-lookup"><span data-stu-id="38a4b-123">The workers who are assigned to a task</span></span>  
  
-   <span data-ttu-id="38a4b-124">Chi phí và doanh thu ước tính</span><span class="sxs-lookup"><span data-stu-id="38a4b-124">Estimated revenue and costs</span></span>  
  
## <a name="task-types"></a><span data-ttu-id="38a4b-125">Loại nhiệm vụ</span><span class="sxs-lookup"><span data-stu-id="38a4b-125">Task types</span></span>  
<span data-ttu-id="38a4b-126">Bạn sẽ sử dụng các loại nhiệm vụ sau khi tạo cấu trúc phân tích công việc:</span><span class="sxs-lookup"><span data-stu-id="38a4b-126">You’ll use the following types of tasks when creating your work breakdown structure:</span></span>  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| <span data-ttu-id="38a4b-127">**Nút gốc dự án**.</span><span class="sxs-lookup"><span data-stu-id="38a4b-127">**Project root node**</span></span> | <span data-ttu-id="38a4b-128">Nhiệm vụ tóm tắt cấp cao cho dự án.</span><span class="sxs-lookup"><span data-stu-id="38a4b-128">The top-level summary task for the project.</span></span> <span data-ttu-id="38a4b-129">Tất cả các nhiệm vụ khác của dự án được tạo trong nhiệm vụ này.</span><span class="sxs-lookup"><span data-stu-id="38a4b-129">All other project tasks are created under it.</span></span> <span data-ttu-id="38a4b-130">Tên của nhiệm vụ gốc là tên dự án.</span><span class="sxs-lookup"><span data-stu-id="38a4b-130">The name of the root task is the project name.</span></span> <span data-ttu-id="38a4b-131">Nỗ lực, ngày tháng và thời gian của nút gốc dựa trên các giá trị trên hệ thống cấp bậc dưới nó.</span><span class="sxs-lookup"><span data-stu-id="38a4b-131">The effort, dates, and duration of the root node are based on the values on the hierarchy below it.</span></span> <span data-ttu-id="38a4b-132">Bạn không thể chỉnh sửa thuộc tính nút gốc hoặc xóa nút gốc.</span><span class="sxs-lookup"><span data-stu-id="38a4b-132">You can’t edit root node properties or delete the root node.</span></span> | 
| <span data-ttu-id="38a4b-133">**Nhiệm vụ tóm tắt hoặc vùng chứa**</span><span class="sxs-lookup"><span data-stu-id="38a4b-133">**Summary or container tasks**</span></span> | <span data-ttu-id="38a4b-134">Nhiệm vụ tóm tắt là nhiệm vụ có các nhiệm vụ phụ trong đó.</span><span class="sxs-lookup"><span data-stu-id="38a4b-134">A summary task is a task that has sub-tasks under it.</span></span> <span data-ttu-id="38a4b-135">Nhiệm vụ tóm tắt không có bất kỳ nỗ lực làm việc hoặc chi phí riêng nào.</span><span class="sxs-lookup"><span data-stu-id="38a4b-135">A summary task doesn’t have any work effort or cost of its own.</span></span> <span data-ttu-id="38a4b-136">Nỗ lực làm việc và chi phí là tập hợp các nhiệm vụ phụ.</span><span class="sxs-lookup"><span data-stu-id="38a4b-136">Its work effort and cost are a rollup of its sub-tasks.</span></span> <span data-ttu-id="38a4b-137">Bạn có thể thay đổi tên của nhiệm vụ tóm tắt, nhưng bạn không thể thay đổi nỗ lực, ngày tháng hoặc thời gian thực hiện, bởi vì những yếu tố này được tính toán tự động.</span><span class="sxs-lookup"><span data-stu-id="38a4b-137">You can change the name of a summary task, but you can’t change the effort, dates, or duration, because those are automatically calculated.</span></span> <span data-ttu-id="38a4b-138">Xóa nhiệm vụ tóm tắt sẽ xóa nhiệm vụ và tất cả các nhiệm vụ phụ.</span><span class="sxs-lookup"><span data-stu-id="38a4b-138">Deleting a summary task deletes the task and all of its sub-tasks.</span></span>|  
| <span data-ttu-id="38a4b-139">**Nhiệm vụ nút lá**</span><span class="sxs-lookup"><span data-stu-id="38a4b-139">**Leaf node tasks**</span></span> | <span data-ttu-id="38a4b-140">Nhiệm vụ nút lá biểu thị công việc chi tiết nhất trên dự án.</span><span class="sxs-lookup"><span data-stu-id="38a4b-140">A leaf node task represents the most detailed work on the project.</span></span> <span data-ttu-id="38a4b-141">Nhiệm vụ này có nỗ lực ước tính, số nguồn lực theo kế hoạch, ngày bắt đầu và kết thúc theo kế hoạch và khoảng thời gian.</span><span class="sxs-lookup"><span data-stu-id="38a4b-141">It has an estimated effort, a planned number of resources, planned start and end dates, and a duration.</span></span>|

  
## <a name="task-hierarchy"></a><span data-ttu-id="38a4b-142">Hệ thống cấp bậc của nhiệm vụ</span><span class="sxs-lookup"><span data-stu-id="38a4b-142">Task hierarchy</span></span>  
 <span data-ttu-id="38a4b-143">Bạn có các tùy chọn sau khi tạo hệ thống cấp bậc của nhiệm vụ:</span><span class="sxs-lookup"><span data-stu-id="38a4b-143">You have the following options when creating a task hierarchy:</span></span>  
  
- <span data-ttu-id="38a4b-144">**Thêm nhiệm vụ**.</span><span class="sxs-lookup"><span data-stu-id="38a4b-144">**Add task**.</span></span>   <span data-ttu-id="38a4b-145">Bạn có thể thêm một nhiệm vụ tại vị trí mà bạn chọn trong hệ thống cấp bậc của nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="38a4b-145">You can add a task at a position you choose in the task hierarchy.</span></span> <span data-ttu-id="38a4b-146">Nếu bạn không chọn một vị trí, nhiệm vụ mới của bạn sẽ xuất hiện ở cuối.</span><span class="sxs-lookup"><span data-stu-id="38a4b-146">If you don’t select a position, your new task appears at the end.</span></span>  
  
- <span data-ttu-id="38a4b-147">**Thụt lề nhiệm vụ**.</span><span class="sxs-lookup"><span data-stu-id="38a4b-147">**Indent task**.</span></span>   <span data-ttu-id="38a4b-148">Thụt lề nhiệm vụ để tạo nhiệm vụ con ngay bên trên.</span><span class="sxs-lookup"><span data-stu-id="38a4b-148">Indent a task to make it a child of the task directly above it.</span></span>  
  
- <span data-ttu-id="38a4b-149">**Tăng lề nhiệm vụ**.</span><span class="sxs-lookup"><span data-stu-id="38a4b-149">**Outdent task**.</span></span>   <span data-ttu-id="38a4b-150">Tăng lề nhiệm vụ để nhiệm vụ đó không còn là nhiệm vụ phụ của nhiệm vụ chính gốc nữa.</span><span class="sxs-lookup"><span data-stu-id="38a4b-150">Outdent a task to make it so it’s no longer a sub-task of its original parent task.</span></span>  
  
- <span data-ttu-id="38a4b-151">**Chuyển lên và chuyển xuống**.</span><span class="sxs-lookup"><span data-stu-id="38a4b-151">**Move up and Move down**.</span></span>   <span data-ttu-id="38a4b-152">Di chuyển nhiệm vụ lên và xuống trong hệ thống cấp bậc của nhiệm vụ chính.</span><span class="sxs-lookup"><span data-stu-id="38a4b-152">Move tasks up and down in the hierarchy of its parent task.</span></span> <span data-ttu-id="38a4b-153">Di chuyển một nhiệm vụ lên hoặc xuống không ảnh hưởng đến nỗ lực, chi phí, ngày hoặc khoảng thời gian của nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="38a4b-153">Moving a task up or down has no effect on its effort, cost, dates, or duration.</span></span>  
  
## <a name="task-attributes"></a><span data-ttu-id="38a4b-154">Thuộc tính nhiệm vụ</span><span class="sxs-lookup"><span data-stu-id="38a4b-154">Task attributes</span></span>  
 <span data-ttu-id="38a4b-155">Tên nhiệm vụ mô tả công việc cần được hoàn thành.</span><span class="sxs-lookup"><span data-stu-id="38a4b-155">A task’s name describes the work that needs to be completed.</span></span> <span data-ttu-id="38a4b-156">Bạn sử dụng các thuộc tính nhiệm vụ khác nhau để mô tả các yêu cầu lịch trình và bố trí nhân viên cho nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="38a4b-156">You use various task attributes to describe the schedule and staffing requirements for the task.</span></span>  
  
### <a name="schedule-attributes"></a><span data-ttu-id="38a4b-157">Thuộc tính lịch trình</span><span class="sxs-lookup"><span data-stu-id="38a4b-157">Schedule attributes</span></span>

 - <span data-ttu-id="38a4b-158">Gán giá trị cho **Số giờ nỗ lực**, **Số nguồn lực**, **Ngày bắt đầu**, **Ngày kết thúc** và **Khoảng thời gian** để xác định lịch trình cho nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="38a4b-158">Assign values to **Effort hours**, **Number of resources**, **Start date**, **End date**, and **Duration** to determine the schedule for the task.</span></span> 
 - <span data-ttu-id="38a4b-159">**Nỗ lực** là ước tính giờ cần để hoàn thành nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="38a4b-159">**Effort** is an estimate of the hours it takes to complete the task.</span></span>
 - <span data-ttu-id="38a4b-160">**Số nguồn lực** là ước tính mà người quản lý dự án đặt trong nhiệm vụ để giúp tạo lịch trình tốt nhất có thể.</span><span class="sxs-lookup"><span data-stu-id="38a4b-160">**Number of resources** is an estimate that the project manager puts in the task to help come up with the best possible schedule.</span></span> 
 - <span data-ttu-id="38a4b-161">**Khoảng thời gian** (tính theo ngày) cho biết số ngày làm việc sẽ cần hoàn thành nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="38a4b-161">**Duration** (in days) indicates the number of work days it will take to complete the task.</span></span>  
  
### <a name="staffing-attributes"></a><span data-ttu-id="38a4b-162">Thuộc tính sắp xếp nhân viên</span><span class="sxs-lookup"><span data-stu-id="38a4b-162">Staffing attributes</span></span>

 - <span data-ttu-id="38a4b-163">**Vai trò**, **Đơn vị tổ chức nguồn lực**, **Số nguồn lực** và **Nguồn lực** mô tả các yêu cầu sắp xếp nhân viên cho nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="38a4b-163">**Role**, **Resource organizational unit**, **Number of resources**, and **Resources** describe the staffing requirements for the task.</span></span> 
 - <span data-ttu-id="38a4b-164">**Vai trò** mô tả loại nguồn lực cần thiết để thực hiện nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="38a4b-164">**Role** describes the type of resource needed to perform the task.</span></span> 
 - <span data-ttu-id="38a4b-165">**Đơn vị tổ chức nguồn lực** biểu thị đơn vị tổ chức mà từ đó nguồn lực phải được sắp xếp nhân viên cho nhiệm vụ đó; điều này cũng tác động đến ước tính chi phí và bán hàng của nhiệm vụ, vì điều này được cân nhắc khi xác định giá bán đơn vị cho nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="38a4b-165">**Resource organizational unit** indicates the organizational unit from which resources should be staffed for that task; this also impacts the cost and sales estimate of the task, since this is accounted for when determining the unit sales price for the resource.</span></span> 
 - <span data-ttu-id="38a4b-166">**Nguồn lực** chứa nguồn lực chung hoặc nguồn lực được đặt tên khi tìm thấy nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="38a4b-166">**Resources** holds a generic resource or a named resource when one is found.</span></span>  
  
## <a name="task-dependencies"></a><span data-ttu-id="38a4b-167">Đối tượng phụ thuộc của nhiệm vụ</span><span class="sxs-lookup"><span data-stu-id="38a4b-167">Task dependencies</span></span>  
 <span data-ttu-id="38a4b-168">Bạn có thể tạo mối quan hệ trước đó giữa một hoặc nhiều nhiệm vụ trong cấu trúc phân tích công việc.</span><span class="sxs-lookup"><span data-stu-id="38a4b-168">You can create predecessor relationships between one or more tasks in the work breakdown structure.</span></span> <span data-ttu-id="38a4b-169">Bạn có thể đặt một hoặc nhiều giá trị cho các trường trước đó về nhiệm vụ để biểu thị nhiệm vụ mà giá trị sẽ phụ thuộc vào.</span><span class="sxs-lookup"><span data-stu-id="38a4b-169">You can set one or more values for the predecessor field on tasks to indicate the tasks that it will be dependent on.</span></span> <span data-ttu-id="38a4b-170">Khi bạn gán một giá trị trước đó cho một nhiệm vụ, nhiệm vụ chỉ có thể bắt đầu khi tất cả các nhiệm vụ trước đó đã hoàn thành.</span><span class="sxs-lookup"><span data-stu-id="38a4b-170">When you assign a predecessor value to a task, the task can only start when all the predecessor tasks have completed.</span></span> <span data-ttu-id="38a4b-171">Đặt đối tượng phụ thuộc này vào một nhiệm vụ sẽ dẫn đến tính toán lại ngày bắt đầu theo kế hoạch của nhiệm vụ là kết thúc muộn nhất của tất cả người tiền nhiệm.</span><span class="sxs-lookup"><span data-stu-id="38a4b-171">Setting this dependency on a task will result in the recalculation of the planned start date of the task as the latest end of all of its predecessors.</span></span> <span data-ttu-id="38a4b-172">Tác động liên quan đến người tiền nhiệm đối với lịch trình không bị giới hạn bởi chế độ nhiệm vụ được xác định trên nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="38a4b-172">Predecessor-related impacts on a schedule are not limited by the task mode defined on the task.</span></span>  
  
## <a name="task-mode"></a><span data-ttu-id="38a4b-173">Chế độ nhiệm vụ</span><span class="sxs-lookup"><span data-stu-id="38a4b-173">Task mode</span></span>  
 <span data-ttu-id="38a4b-174">Chế độ nhiệm vụ là một trong những yếu tố quan trọng để xác định việc lên lịch nhiệm vụ nút lá.</span><span class="sxs-lookup"><span data-stu-id="38a4b-174">Task mode is one of the important factors that determine scheduling leaf node tasks.</span></span> <span data-ttu-id="38a4b-175">Có hai chế độ nhiệm vụ cho mỗi nhiệm vụ: chế độ lên lịch tự động và chế độ lên lịch thủ công.</span><span class="sxs-lookup"><span data-stu-id="38a4b-175">There are two task modes for every task: auto scheduling mode and manual scheduling mode.</span></span>  
  
-   <span data-ttu-id="38a4b-176">**Tự động lên lịch**.</span><span class="sxs-lookup"><span data-stu-id="38a4b-176">**Auto scheduling**.</span></span>   <span data-ttu-id="38a4b-177">Khi bạn đặt chế độ nhiệm vụ thành Tự động Lên lịch, công cụ lên lịch nhiệm vụ sử dụng quy tắc lên lịch trên các thuộc tính nhiệm vụ sau để xác định lịch trình cho nhiệm vụ:</span><span class="sxs-lookup"><span data-stu-id="38a4b-177">When you set the task mode to Automatically Scheduled, the task scheduling engine uses the scheduling rules on the following task attributes to determine the schedule for the task:</span></span>  
  
    -   <span data-ttu-id="38a4b-178">Người tiền nhiệm</span><span class="sxs-lookup"><span data-stu-id="38a4b-178">Predecessors</span></span>  
  
    -   <span data-ttu-id="38a4b-179">Nỗ lực</span><span class="sxs-lookup"><span data-stu-id="38a4b-179">Effort</span></span>  
  
    -   <span data-ttu-id="38a4b-180">Số nguồn lực</span><span class="sxs-lookup"><span data-stu-id="38a4b-180">Number of resources</span></span>  
  
    -   <span data-ttu-id="38a4b-181">Ngày bắt đầu và ngày kết thúc</span><span class="sxs-lookup"><span data-stu-id="38a4b-181">Start and end dates</span></span>  
  
-   <span data-ttu-id="38a4b-182">**Quy tắc lên lịch**.</span><span class="sxs-lookup"><span data-stu-id="38a4b-182">**Scheduling rules**.</span></span>   <span data-ttu-id="38a4b-183">Ngày bắt đầu của một nhiệm vụ nút lá không có người tiền nhiệm sẽ mặc định là ngày bắt đầu lên lịch của dự án.</span><span class="sxs-lookup"><span data-stu-id="38a4b-183">The start date of a leaf node task that does not have predecessors defaults to the project’s scheduling start date.</span></span> <span data-ttu-id="38a4b-184">Khoảng thời gian của nhiệm vụ nút lá luôn được tính toán là số ngày làm việc giữa của ngày bắt đầu và ngày kết thúc.</span><span class="sxs-lookup"><span data-stu-id="38a4b-184">The duration of a leaf node task is always calculated as the number of working days between its start and end dates.</span></span> <span data-ttu-id="38a4b-185">Khi một nhiệm vụ được lên lịch tự động, công cụ lên lịch tuân thủ các quy tắc dưới đây:</span><span class="sxs-lookup"><span data-stu-id="38a4b-185">When a task is automatically scheduled, the scheduling engine follows the rules below:</span></span>  
  
    -   <span data-ttu-id="38a4b-186">Ngày bắt đầu và ngày kết thúc của nhiệm vụ luôn phải là ngày làm việc theo lịch lên lịch của dự án</span><span class="sxs-lookup"><span data-stu-id="38a4b-186">Start and end dates of a task must always be working days according to the project’s scheduling calendar</span></span>  
  
    -   <span data-ttu-id="38a4b-187">Ngày bắt đầu của nhiệm vụ có người tiền nhiệm sẽ mặc định là ngày kết thúc muộn nhất của người tiền nhiệm</span><span class="sxs-lookup"><span data-stu-id="38a4b-187">The start date of a task that has predecessors defaults to the latest end date of its predecessors</span></span>  
  
    -   <span data-ttu-id="38a4b-188">Nỗ lực = Số người \* Khoảng thời gian \* số giờ trong ngày làm việc tiêu chuẩn của lịch dự án</span><span class="sxs-lookup"><span data-stu-id="38a4b-188">Effort = Number of people \* Duration \* hours in a standard work day of the project calendar</span></span>  
  
-   <span data-ttu-id="38a4b-189">**Lên lịch thủ công**.</span><span class="sxs-lookup"><span data-stu-id="38a4b-189">**Manual scheduling**.</span></span>   <span data-ttu-id="38a4b-190">Trong một số trường hợp, bạn có thể cần phân biệt với những quy tắc này.</span><span class="sxs-lookup"><span data-stu-id="38a4b-190">In some cases, you might want to deviate from these rules.</span></span> <span data-ttu-id="38a4b-191">Trong những trường hợp này, bạn có thể thiết lập chế độ nhiệm vụ cho nhiệm vụ được lên lịch theo cách thủ công.</span><span class="sxs-lookup"><span data-stu-id="38a4b-191">In these cases, you can set the task mode for the task to be manually scheduled.</span></span> <span data-ttu-id="38a4b-192">Điều này sẽ ngăn công cụ lên lịch tính toán giá trị cho các thuộc tính lên lịch khác.</span><span class="sxs-lookup"><span data-stu-id="38a4b-192">This stops the scheduling engine from calculating the values for other scheduling attributes.</span></span> <span data-ttu-id="38a4b-193">Thiết lập người tiền nhiệm về nhiệm vụ luôn luôn ảnh hưởng đến ngày bắt đầu của nhiệm vụ phụ thuộc.</span><span class="sxs-lookup"><span data-stu-id="38a4b-193">Setting predecessors on tasks always impacts the dependent task’s start date.</span></span>  
  
## <a name="create-a-work-breakdown-structure"></a><span data-ttu-id="38a4b-194">Tạo cấu trúc phân tích công việc</span><span class="sxs-lookup"><span data-stu-id="38a4b-194">Create a work breakdown structure</span></span>  
  
1.  <span data-ttu-id="38a4b-195">Đi tới **Project Service > Dự án**.</span><span class="sxs-lookup"><span data-stu-id="38a4b-195">Go to **Project Service > Projects**.</span></span>  
  
2.  <span data-ttu-id="38a4b-196">Bấm vào dự án mà bạn muốn làm việc.</span><span class="sxs-lookup"><span data-stu-id="38a4b-196">Click the project you want to work on.</span></span>  
  
3.  <span data-ttu-id="38a4b-197">Trong thanh ở đầu màn hình, chọn mũi tên xuống bên cạnh tên dự án, sau đó bấm vào Cấu trúc phân tích công việc.</span><span class="sxs-lookup"><span data-stu-id="38a4b-197">In the bar across the top of the screen, select the down arrow next to the project name, and then click Work breakdown structure.</span></span>  
  
4.  <span data-ttu-id="38a4b-198">Để thêm một nhiệm vụ, bấm **Thêm nhiệm vụ**.</span><span class="sxs-lookup"><span data-stu-id="38a4b-198">To add a task, click **Add Task**.</span></span> <span data-ttu-id="38a4b-199">Điền vào các trường cho nhiệm vụ, sau đó bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="38a4b-199">Fill in the fields for the task, and then click **Save**.</span></span>  
  
5.  <span data-ttu-id="38a4b-200">Tiếp tục thêm nhiệm vụ cho đến khi cấu trúc phân tích công việc của bạn hoàn thành.</span><span class="sxs-lookup"><span data-stu-id="38a4b-200">Continue adding tasks until your work breakdown structure is complete.</span></span> <span data-ttu-id="38a4b-201">Trong khi tạo cấu trúc phân tích công việc, bạn có thể làm những điều sau đây để tổ chức các nhiệm vụ của mình:</span><span class="sxs-lookup"><span data-stu-id="38a4b-201">While creating your work breakdown structure, you can do the following to organize your tasks:</span></span>  
  
    -   <span data-ttu-id="38a4b-202">Chọn nhiệm vụ và bấm vào **Thụt lề** để di chuyển xuống một nhiệm vụ khác hoặc bấm vào Tăng lề để di chuyển lên một cấp độ.</span><span class="sxs-lookup"><span data-stu-id="38a4b-202">Select a task and click **Indent** to move it under another task or click Outdent to move it out a level.</span></span>  
  
    -   <span data-ttu-id="38a4b-203">Chọn một nhiệm vụ và bấm vào **Di chuyển lên** hoặc **Di chuyển xuống** để chuyển nhiệm vụ lên hoặc xuống trong danh sách.</span><span class="sxs-lookup"><span data-stu-id="38a4b-203">Select a task and click **Move Up** or **Move Down** to move it up or down in the list.</span></span>  
  
    -   <span data-ttu-id="38a4b-204">Bấm vào **Ẩn Gantt** để ẩn biểu đồ Gantt và bấm vào **Hiển thị Gantt** để hiển thị lại biểu đồ.</span><span class="sxs-lookup"><span data-stu-id="38a4b-204">Click **Hide Gantt** to hide the Gantt chart, and click **Show Gantt** to display it again.</span></span>  
  
    -   <span data-ttu-id="38a4b-205">Chọn khoảng thời gian khác cho biểu đồ Gantt trong **Thang thời gian**.</span><span class="sxs-lookup"><span data-stu-id="38a4b-205">Select a different period of time for the Gantt chart in **Time Scale**.</span></span>  
  
6.  <span data-ttu-id="38a4b-206">Để thêm vai trò bạn đã chỉ định trong cấu trúc phân tích công việc vào thành viên nhóm của dự án, bấm vào **Tạo nhóm dự án**.</span><span class="sxs-lookup"><span data-stu-id="38a4b-206">To add the roles you specified in your work breakdown structure to your project’s team members, click **Generate Project Team**.</span></span>  
  
7.  <span data-ttu-id="38a4b-207">Bấm **Lưu** ở góc dưới cùng bên phải của màn hình khi bạn hoàn tất việc thay đổi.</span><span class="sxs-lookup"><span data-stu-id="38a4b-207">Click **Save** at the bottom right corner of the screen when you’re done making changes.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="38a4b-208">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="38a4b-208">See Also</span></span>  
 [<span data-ttu-id="38a4b-209">Hướng dẫn của quản lý dự án</span><span class="sxs-lookup"><span data-stu-id="38a4b-209">Project manager guide</span></span>](../psa/project-manager-guide.md)
