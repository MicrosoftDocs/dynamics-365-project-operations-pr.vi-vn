---
title: Tiến độ dự án và mức sử dụng chi phí
description: Chủ đề này cung cấp thông tin về cách theo dõi tiến độ dự án và mức sử dụng chi phí.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 08/21/2020
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
ms.openlocfilehash: 3b60f72b371a76a59216b0b528d8e63513b06e0d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087269"
---
# <a name="project-progress-and-cost-consumption"></a><span data-ttu-id="e80e0-103">Tiến độ dự án và mức sử dụng chi phí</span><span class="sxs-lookup"><span data-stu-id="e80e0-103">Project progress and cost consumption</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="e80e0-104">Sự cần thiết của việc theo dõi tiến độ đối với lịch trình thay đổi theo ngành.</span><span class="sxs-lookup"><span data-stu-id="e80e0-104">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="e80e0-105">Một số ngành theo dõi ở cấp độ chi tiết, trong khi các ngành khác theo dõi ở cấp độ cao hơn.</span><span class="sxs-lookup"><span data-stu-id="e80e0-105">Some industries track at a granular level, whereas other industries track at a higher level.</span></span> <span data-ttu-id="e80e0-106">Chủ đề này cho biết cách lập lịch để đáp ứng các yêu cầu của tổ chức bạn.</span><span class="sxs-lookup"><span data-stu-id="e80e0-106">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="e80e0-107">Dạng xem theo dõi nhân công</span><span class="sxs-lookup"><span data-stu-id="e80e0-107">Effort tracking view</span></span>

<span data-ttu-id="e80e0-108">Dạng xem **Theo dõi nhân công** theo dõi tiến độ của nhiệm vụ trong lịch trình.</span><span class="sxs-lookup"><span data-stu-id="e80e0-108">The **Effort tracking** view tracks the progress of tasks in the schedule.</span></span> <span data-ttu-id="e80e0-109">Dạng xem này so sánh thời gian thực tế đã thực hiện nhiệm vụ so với thời gian dự kiến.</span><span class="sxs-lookup"><span data-stu-id="e80e0-109">It compares the actual effort hours spent on a task to the task's planned effort hours.</span></span> <span data-ttu-id="e80e0-110">Project Service Automation sử dụng các công thức sau để tính toán các chỉ số theo dõi:</span><span class="sxs-lookup"><span data-stu-id="e80e0-110">Project Service Automation uses the following formulas to calculate the tracking metrics:</span></span>

<span data-ttu-id="e80e0-111">Ban đầu khi tạo nhiệm vụ: Chi phí theo kế hoạch sẽ được đặt thành Chi phí ước tính khi hoàn thành.</span><span class="sxs-lookup"><span data-stu-id="e80e0-111">Initially on the task creation: Planned cost will be set to the Estimated cost at complete.</span></span> <span data-ttu-id="e80e0-112">Khi Giá trị thực tế được ghi lại trong nhiệm vụ, sau đây sẽ là phép tính trên dạng xem Theo dõi đối với Nhân công</span><span class="sxs-lookup"><span data-stu-id="e80e0-112">Once Actuals are recorded on the task, the following will be calculation on the Tracking view for Effort</span></span>

- <span data-ttu-id="e80e0-113">Phần trăm tiến độ = Nhân công thực tế đã dành ra cho đến nay ÷ Ước tính hoàn thành (EAC)</span><span class="sxs-lookup"><span data-stu-id="e80e0-113">Progress percentage = Actual effort spent to date ÷ Estimate at complete (EAC)</span></span> 
- <span data-ttu-id="e80e0-114">Ước tính hoàn thành (ETC) = Ước tính hoàn thành (EAC) - Nhân công thực tế đã dành ra cho đến nay</span><span class="sxs-lookup"><span data-stu-id="e80e0-114">Estimate to complete (ETC) = Estimate at complete (EAC)  – Actual effort spent to date</span></span> 
- <span data-ttu-id="e80e0-115">EAC = Nhân công còn lại + Nhân công thực tế đã dành ra cho đến nay</span><span class="sxs-lookup"><span data-stu-id="e80e0-115">EAC = Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="e80e0-116">Chênh lệch nhân công dự kiến = Nhân công theo kế hoạch – EAC</span><span class="sxs-lookup"><span data-stu-id="e80e0-116">Projected effort variance = Planned effort – EAC</span></span>

<span data-ttu-id="e80e0-117">Project Service Automation cho thấy dự đoán chênh lệch nhân công trên nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="e80e0-117">Project Service Automation shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="e80e0-118">Nếu EAC nhiều hơn nhân công theo kế hoạch, nghĩa là nhiệm vụ được dự kiến mất nhiều thời gian hơn so với kế hoạch ban đầu.</span><span class="sxs-lookup"><span data-stu-id="e80e0-118">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned.</span></span> <span data-ttu-id="e80e0-119">Do đó, nhiệm vụ kết thúc muộn hơn so với lịch trình.</span><span class="sxs-lookup"><span data-stu-id="e80e0-119">Therefore, it's behind schedule.</span></span> <span data-ttu-id="e80e0-120">Nếu EAC nhỏ hơn nhân công dự kiến, nghĩa là nhiệm vụ được dự kiến mất ít thời gian hơn so với kế hoạch ban đầu.</span><span class="sxs-lookup"><span data-stu-id="e80e0-120">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned.</span></span> <span data-ttu-id="e80e0-121">Do đó, nhiệm vụ kết thúc sớm hơn so với lịch trình.</span><span class="sxs-lookup"><span data-stu-id="e80e0-121">Therefore, it's ahead of schedule.</span></span>

## <a name="reprojecting-effort"></a><span data-ttu-id="e80e0-122">Lên kế hoạch lại nhân công</span><span class="sxs-lookup"><span data-stu-id="e80e0-122">Reprojecting effort</span></span>

<span data-ttu-id="e80e0-123">Người quản lý dự án thường có thể sửa đổi ước tính ban đầu cho một nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="e80e0-123">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="e80e0-124">Lên kế hoạch lại dự án là khả năng ước tính của người quản lý dự án, dựa trên hiện trạng dự án.</span><span class="sxs-lookup"><span data-stu-id="e80e0-124">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="e80e0-125">Tuy nhiên, người quản lý dự án không nên thay đổi các chỉ số ban đầu vì chỉ số ban đầu của dự án đại diện cho nguồn tin cậy đã được thiết lập đối với lịch trình và ước tính chi phí của dự án. Tất cả bên liên quan của dự án phải đồng ý với các chỉ số ban đầu.</span><span class="sxs-lookup"><span data-stu-id="e80e0-125">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="e80e0-126">Người quản lý dự án có thể lên kế hoạch lại nhân công cho nhiệm vụ bằng 2 cách:</span><span class="sxs-lookup"><span data-stu-id="e80e0-126">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="e80e0-127">Thay thế ETC mặc định bằng ước tính mới của nhân công còn lại thực tế trên nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="e80e0-127">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="e80e0-128">Thay thế phần trăm tiến trình mặc định bằng ước tính mới của tiến trình đúng trên nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="e80e0-128">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="e80e0-129">Mỗi cách tiếp cận này mang đến một phép tính lại ETC, EAC và phần trăm tiến trình của nhiệm vụ cũng như chênh lệch nhân công dự kiến trên nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="e80e0-129">Each of these approaches cause a recalculation of the task's ETC, EAC, and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="e80e0-130">EAC, ETC và phần trăm tiến trình trên các nhiệm vụ tóm tắt cũng được tính toán lại và cung cấp dự kiến mới về chênh lệch nhân công.</span><span class="sxs-lookup"><span data-stu-id="e80e0-130">The EAC, ETC, and progress percentage on the summary tasks are also recalculated, and produce a new projection of effort variance.</span></span>

## <a name="reprojection-of-effort-on-summary-tasks"></a><span data-ttu-id="e80e0-131">Lên kế hoạch lại nhân công cho các nhiệm vụ tóm tắt</span><span class="sxs-lookup"><span data-stu-id="e80e0-131">Reprojection of effort on summary tasks</span></span>

<span data-ttu-id="e80e0-132">Có thể lên kế hoạch lại nhân công cho các nhiệm vụ tóm tắt hoặc nhiệm vụ bộ chứa.</span><span class="sxs-lookup"><span data-stu-id="e80e0-132">Effort on summary tasks or container tasks can be reprojected.</span></span> <span data-ttu-id="e80e0-133">Bất kể người dùng lên kế hoạch lại bằng nhân công còn lại hay phần trăm tiến trình trên nhiệm vụ tóm tắt, các bộ tính toán sau sẽ hoạt động:</span><span class="sxs-lookup"><span data-stu-id="e80e0-133">Regardless of whether the user reprojects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="e80e0-134">EAC, ETC và phần trăm tiến trình trên nhiệm vụ được tính.</span><span class="sxs-lookup"><span data-stu-id="e80e0-134">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="e80e0-135">EAC mới được phân phối xuống các nhiệm vụ con trong cùng một tỷ lệ như EAC gốc trên nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="e80e0-135">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="e80e0-136">EAC mới trên mỗi nhiệm vụ riêng xuống các nhiệm vụ nút lá được tính toán.</span><span class="sxs-lookup"><span data-stu-id="e80e0-136">The new EAC on each of the individual tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="e80e0-137">Các nhiệm vụ con bị ảnh hưởng xuống các nút lá có ETC và phần trăm tiến trình được tính toán lại dựa trên giá trị EAC.</span><span class="sxs-lookup"><span data-stu-id="e80e0-137">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="e80e0-138">Điều này dẫn đến dự kiến mới cho chênh lệch nhân công của nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="e80e0-138">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="e80e0-139">EAC của nhiệm vụ tóm tắt đến các nút gốc được tính toán lại.</span><span class="sxs-lookup"><span data-stu-id="e80e0-139">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="e80e0-140">Dạng xem theo dõi chi phí</span><span class="sxs-lookup"><span data-stu-id="e80e0-140">Cost tracking view</span></span> 

<span data-ttu-id="e80e0-141">Dạng xem **Theo dõi chi phí** so sánh chi phí thực tế đã sử dụng cho nhiệm vụ với chi phí theo kế hoạch.</span><span class="sxs-lookup"><span data-stu-id="e80e0-141">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost.</span></span> 

> [!NOTE]
> <span data-ttu-id="e80e0-142">Dạng xem này chỉ hiển thị chi phí lao động và không gồm chi phí từ ước tính chi phí.</span><span class="sxs-lookup"><span data-stu-id="e80e0-142">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> 

<span data-ttu-id="e80e0-143">Project Service Automation sử dụng các công thức sau để tính toán các chỉ số theo dõi:</span><span class="sxs-lookup"><span data-stu-id="e80e0-143">Project Service Automation uses the following formulas to calculate the tracking metrics:</span></span>

<span data-ttu-id="e80e0-144">Khi một nhiệm vụ được tạo, chi phí theo kế hoạch bằng với chi phí ước tính khi hoàn thành.</span><span class="sxs-lookup"><span data-stu-id="e80e0-144">When a task is created, the planned cost is equal to the estimated cost at complete.</span></span> <span data-ttu-id="e80e0-145">Sau khi các giá trị thực tế được ghi lại trong nhiệm vụ, phép tính sau đây được thực hiện trên dạng xem **Theo dõi** cho chi phí:</span><span class="sxs-lookup"><span data-stu-id="e80e0-145">After actuals are recorded on the task, the following is calculated on the **Tracking** view for cost:</span></span>

 - <span data-ttu-id="e80e0-146">Phần trăm chi phí đã sử dụng = Chi phí thực tế đã sử dụng cho đến nay ÷ Chi phí ước tính khi hoàn thành nhiệm vụ</span><span class="sxs-lookup"><span data-stu-id="e80e0-146">Percentage of cost consumed = Actual cost spent to date ÷ Estimated cost at complete for the task</span></span>
 - <span data-ttu-id="e80e0-147">Chi phí hoàn thành (CTC) = Chi phí ước tính khi hoàn thành – Chi phí thực tế đã sử dụng cho đến nay</span><span class="sxs-lookup"><span data-stu-id="e80e0-147">Cost to complete (CTC) = Estimated cost at complete – Actual cost spent to date</span></span>
 - <span data-ttu-id="e80e0-148">Chi phí hoàn thành (CTC) = CTC + Chi phí thực tế đã sử dụng cho đến nay</span><span class="sxs-lookup"><span data-stu-id="e80e0-148">Estimated cost at complete = CTC + Actual cost spent to date</span></span>
 - <span data-ttu-id="e80e0-149">Chênh lệch chi phí dự kiến = Chi phí theo kế hoạch – Chi phí hoàn thành</span><span class="sxs-lookup"><span data-stu-id="e80e0-149">Projected cost variance = Planned cost – Estimated cost at complete</span></span>

<span data-ttu-id="e80e0-150">Dự kiến của chênh lệch chi phí hiển thị trên nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="e80e0-150">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="e80e0-151">Nếu chi phí ước tính khi hoàn thành lớn hơn chi phí theo kế hoạch, nghĩa là nhiệm vụ được dự kiến mất nhiều chi phí hơn so với kế hoạch ban đầu.</span><span class="sxs-lookup"><span data-stu-id="e80e0-151">If the estimated cost at complete is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="e80e0-152">Do đó, chi phí của nhiệm vụ có xu hướng vượt quá ngân sách.</span><span class="sxs-lookup"><span data-stu-id="e80e0-152">Therefore, it's trending over budget.</span></span> <span data-ttu-id="e80e0-153">Nếu chi phí ước tính khi hoàn thành nhỏ hơn chi phí theo kế hoạch, nghĩa là nhiệm vụ được dự kiến mất ít chi phí hơn so với kế hoạch ban đầu và có xu hướng ít hơn ngân sách.</span><span class="sxs-lookup"><span data-stu-id="e80e0-153">If the Estimated cost at complete is less than the planned cost, the task is projected to cost less than was originally planned and is trending under budget.</span></span>

## <a name="project-managers-reprojection-of-cost"></a><span data-ttu-id="e80e0-154">Người quản lý dự án lên kế hoạch lại chi phí</span><span class="sxs-lookup"><span data-stu-id="e80e0-154">Project manager’s reprojection of cost</span></span>

<span data-ttu-id="e80e0-155">Khi nhân công được lên kế hoạch lại, CTC, Chi phí ước tính khi hoàn thành, phần trăm chi phí tiêu thụ và chênh lệch chi phí dự kiến đều được tính toán lại trong dạng xem **Theo dõi chi phí**.</span><span class="sxs-lookup"><span data-stu-id="e80e0-155">When effort is reprojected, the CTC, Estimated cost at complete, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="e80e0-156">Tóm tắt trạng thái dự án</span><span class="sxs-lookup"><span data-stu-id="e80e0-156">Project status summary</span></span>

<span data-ttu-id="e80e0-157">Theo dõi dữ liệu trong các dạng xem **Theo dõi nhân lực** và **Theo dõi chi phí** hiển thị tiến trình và mức sử dụng chi phí tại các cấp nút gốc dự án, các nhiệm vụ tóm tắt và nhiệm vụ nút lá.</span><span class="sxs-lookup"><span data-stu-id="e80e0-157">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="e80e0-158">Phần **Trạng thái** trên trang **Thực thể dự án** hiển thị tóm tắt trạng thái cấp độ dự án.</span><span class="sxs-lookup"><span data-stu-id="e80e0-158">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="e80e0-159">Trường tóm tắt trạng thái</span><span class="sxs-lookup"><span data-stu-id="e80e0-159">Status summary fields</span></span>

<span data-ttu-id="e80e0-160">Trường **Tổng quan trạng thái dự án** là trường có thể chỉnh sửa hiển thị trạng thái tổng quan của dự án.</span><span class="sxs-lookup"><span data-stu-id="e80e0-160">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="e80e0-161">Trường này dùng mã màu, chẳng hạn như xanh lục, vàng và đỏ để chỉ ra rủi ro gia tăng.</span><span class="sxs-lookup"><span data-stu-id="e80e0-161">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="e80e0-162">Trường **Nhận xét** cho phép người quản lý dự án nhập nhận xét cụ thể về trạng thái.</span><span class="sxs-lookup"><span data-stu-id="e80e0-162">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="e80e0-163">Trường **Ngày cập nhật trạng thái** không thể chỉnh sửa và giá trị này là dấu thời gian cho biết thời điểm trạng thái được cập nhật gần đây nhất.</span><span class="sxs-lookup"><span data-stu-id="e80e0-163">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="e80e0-164">Các trường **Hiệu suất lịch trình** và **Hiệu suất chi phí** được đặt từ ngày theo dõi.</span><span class="sxs-lookup"><span data-stu-id="e80e0-164">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="e80e0-165">Khi chênh lệch lịch trình và chi phí cho các nút gốc trong dạng xem **Theo dõi nhân công** dương, bạn có thể đặt các trường này thành **Trước**.</span><span class="sxs-lookup"><span data-stu-id="e80e0-165">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="e80e0-166">Khi chênh lệch lịch trình và chi phí cho nút gốc âm, bạn có thể đặt các trường này thành **Sau**.</span><span class="sxs-lookup"><span data-stu-id="e80e0-166">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>
