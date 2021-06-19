---
title: Chế độ lập lịch trình
description: Chủ đề này cung cấp thông tin về chế độ lập lịch trình.
author: ruhercul
ms.date: 05/28/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 508ff1df8f7e31066712fab6f8871dfdb107a43b
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116733"
---
# <a name="scheduling-modes"></a><span data-ttu-id="15884-103">Chế độ lập lịch trình</span><span class="sxs-lookup"><span data-stu-id="15884-103">Scheduling modes</span></span>

<span data-ttu-id="15884-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="15884-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="15884-105">Dynamics 365 Project Operations cung cấp khả năng cho các tổ chức để xác định cách họ quản lý thay đổi đối với các biến chính trong nhiệm vụ của cấu trúc phân tích công việc.</span><span class="sxs-lookup"><span data-stu-id="15884-105">Dynamics 365 Project Operations provides the ability for organizations to define how they manage changes to key variables in tasks within the work breakdown structure.</span></span> <span data-ttu-id="15884-106">Dựa trên nhu cầu cụ thể của tổ chức, Người quản lý dự án có thể thực hiện các thay đổi đối với chế độ lập lịch trình khi một dự án được tạo.</span><span class="sxs-lookup"><span data-stu-id="15884-106">Based on the specific needs of the organization, Project Managers can make changes to the scheduling mode when a project is created.</span></span>

<span data-ttu-id="15884-107">Có ba chế độ lập lịch trình có sẵn trong Project Operations:</span><span class="sxs-lookup"><span data-stu-id="15884-107">There are three scheduling modes available in Project Operations:</span></span>

  - <span data-ttu-id="15884-108">Khoảng thời gian cố định (đây là chế độ mặc định)</span><span class="sxs-lookup"><span data-stu-id="15884-108">Fixed duration (this is the default mode)</span></span>
  - <span data-ttu-id="15884-109">Nỗ lực cố định (*Công việc*)</span><span class="sxs-lookup"><span data-stu-id="15884-109">Fixed effort (*Work*)</span></span>
  - <span data-ttu-id="15884-110">Đơn vị cố định</span><span class="sxs-lookup"><span data-stu-id="15884-110">Fixed units</span></span>

<span data-ttu-id="15884-111">Các giá trị bị định nghĩa của một chế độ lập lịch trình cụ thể tác động được xác định theo công thức sau:</span><span class="sxs-lookup"><span data-stu-id="15884-111">The values impacted by the definition of a specific scheduling mode are determined by the following formula:</span></span>

  <span data-ttu-id="15884-112">Nỗ lực = Khoảng thời gian x Đơn vị</span><span class="sxs-lookup"><span data-stu-id="15884-112">Effort  = Duration x Units</span></span>

<span data-ttu-id="15884-113">Khi xác định chế độ lập lịch trình của dự án, bạn đang thiết lập một trong những giá trị này, sau đó không thể thay đổi được.</span><span class="sxs-lookup"><span data-stu-id="15884-113">When you define a project’s scheduling mode, you are setting one of these values, which then can't be changed.</span></span> <span data-ttu-id="15884-114">Duy trì giá trị này là một hằng số sẽ đặt ưu tiên cho giá trị đó, điều này sẽ thông báo cho hệ thống không thay đổi giá trị này khi hai giá trị khác thay đổi.</span><span class="sxs-lookup"><span data-stu-id="15884-114">Holding this value as a constant places a priority on that value, which notifies the system not to change it when the other two values change.</span></span> <span data-ttu-id="15884-115">Bảng sau đây cung cấp thông tin về tác động của việc chọn một chế độ cụ thể.</span><span class="sxs-lookup"><span data-stu-id="15884-115">The following table provides information about the impacts of selecting a specific mode.</span></span>

| <span data-ttu-id="15884-116">**Trong nhiệm vụ này**</span><span class="sxs-lookup"><span data-stu-id="15884-116">**In this task**</span></span>             | <span data-ttu-id="15884-117">**Nếu bạn sửa các đơn vị**</span><span class="sxs-lookup"><span data-stu-id="15884-117">**If you revise units**</span></span>   | <span data-ttu-id="15884-118">**Nếu bạn sửa khoảng thời gian**</span><span class="sxs-lookup"><span data-stu-id="15884-118">**If you revise duration**</span></span> | <span data-ttu-id="15884-119">**Nếu bạn sửa nỗ lực**</span><span class="sxs-lookup"><span data-stu-id="15884-119">**If you revise effort**</span></span>  |
|----------------------|---------------------------|----------------------------|---------------------------|
| <span data-ttu-id="15884-120">Nhiệm vụ đơn vị cố định</span><span class="sxs-lookup"><span data-stu-id="15884-120">Fixed units task</span></span>     | <span data-ttu-id="15884-121">Khoảng thời gian được tính toán lại.</span><span class="sxs-lookup"><span data-stu-id="15884-121">Duration is recalculated.</span></span> | <span data-ttu-id="15884-122">Nỗ lực được tính toán lại.</span><span class="sxs-lookup"><span data-stu-id="15884-122">Effort is recalculated.</span></span>    | <span data-ttu-id="15884-123">Khoảng thời gian được tính toán lại.</span><span class="sxs-lookup"><span data-stu-id="15884-123">Duration is recalculated.</span></span> |
| <span data-ttu-id="15884-124">Nhiệm vụ nỗ lực cố định</span><span class="sxs-lookup"><span data-stu-id="15884-124">Fixed effort task</span></span>    | <span data-ttu-id="15884-125">Khoảng thời gian được tính toán lại.</span><span class="sxs-lookup"><span data-stu-id="15884-125">Duration is recalculated.</span></span> | <span data-ttu-id="15884-126">Các đơn vị được tính toán lại.</span><span class="sxs-lookup"><span data-stu-id="15884-126">Units are recalculated.</span></span>    | <span data-ttu-id="15884-127">Khoảng thời gian được tính toán lại.</span><span class="sxs-lookup"><span data-stu-id="15884-127">Duration is recalculated.</span></span> |
| <span data-ttu-id="15884-128">Nhiệm vụ khoảng thời gian cố định</span><span class="sxs-lookup"><span data-stu-id="15884-128">Fixed duration task</span></span>  | <span data-ttu-id="15884-129">Nỗ lực được tính toán lại.</span><span class="sxs-lookup"><span data-stu-id="15884-129">Effort is recalculated.</span></span>   | <span data-ttu-id="15884-130">Nỗ lực được tính toán lại.</span><span class="sxs-lookup"><span data-stu-id="15884-130">Effort is recalculated.</span></span>    | <span data-ttu-id="15884-131">Các đơn vị được tính toán lại.</span><span class="sxs-lookup"><span data-stu-id="15884-131">Units are recalculated.</span></span>   |

<span data-ttu-id="15884-132">Để biết thêm thông tin về tác động của một chế độ nhất định, hãy xem [Thay đổi loại nhiệm vụ để lập lịch chính xác hơn](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span><span class="sxs-lookup"><span data-stu-id="15884-132">For more information about the implications of a given mode, see [Change the task type for more accurate scheduling](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span></span> <span data-ttu-id="15884-133">Trong chủ đề này, thuật ngữ **Công việc** được sử dụng thay cho **Nỗ lực**.</span><span class="sxs-lookup"><span data-stu-id="15884-133">In the topic, the term **Work** is used instead of **Effort**.</span></span>

## <a name="change-the-organizations-scheduling-mode"></a><span data-ttu-id="15884-134">Thay đổi chế độ lập lịch trình của tổ chức</span><span class="sxs-lookup"><span data-stu-id="15884-134">Change the organization’s scheduling mode</span></span>

<span data-ttu-id="15884-135">Hoàn thành các bước sau để xác định chế độ lập lịch trình của một tổ chức.</span><span class="sxs-lookup"><span data-stu-id="15884-135">Complete the following steps to define the scheduling mode of an organization.</span></span>

1. <span data-ttu-id="15884-136">Chuyển đến phần **Cài đặt** \> **Chung** \> **Thông số** rồi chọn thông số dự án.</span><span class="sxs-lookup"><span data-stu-id="15884-136">Go to **Settings** \> **General** \> **Parameters**, and then select the project parameter.</span></span> 
2. <span data-ttu-id="15884-137">Trên trang **Thông số dự án**, hãy chọn chế độ lập lịch trình mặc định cho tổ chức rồi xác định khả năng cho Người quản lý dự án ghi đè cài đặt khi tạo một dự án mới.</span><span class="sxs-lookup"><span data-stu-id="15884-137">On the **Project Parameters** page, select the default scheduling mode for the organization, and then define ability for the Project manager to override the setting when creating a new project.</span></span>

## <a name="change-the-scheduling-mode-setting-on-a-project"></a><span data-ttu-id="15884-138">Thay đổi tùy chọn cài đặt của chế độ lập lịch trình trên một dự án</span><span class="sxs-lookup"><span data-stu-id="15884-138">Change the scheduling mode setting on a project</span></span>

<span data-ttu-id="15884-139">Nếu một tổ chức cho phép Người quản lý dự án ghi đè chế độ lập lịch trình mặc định, Người quản lý dự án có thể thực hiện thay đổi đó khi họ tạo một dự án mới.</span><span class="sxs-lookup"><span data-stu-id="15884-139">If an organization allows the Project manager to override the default scheduling mode, the Project manager can make that change when they create a new project.</span></span> <span data-ttu-id="15884-140">Tuy nhiên, sau khi dự án đã được lưu, không thể thay đổi chế độ lập lịch trình.</span><span class="sxs-lookup"><span data-stu-id="15884-140">However, after the project has been saved, the scheduling mode can't be changed.</span></span>

## <a name="copied-projects"></a><span data-ttu-id="15884-141">Dự án được sao chép</span><span class="sxs-lookup"><span data-stu-id="15884-141">Copied projects</span></span>

<span data-ttu-id="15884-142">Vì dự án được tạo khi thực hiện thao tác sao chép dự án, nên Người quản lý dự án không thể thiết lập chế độ lập lịch trình.</span><span class="sxs-lookup"><span data-stu-id="15884-142">Because a project is created when the copy project action is taken, the Project manager can't set the scheduling mode.</span></span> <span data-ttu-id="15884-143">Dự án đích sẽ luôn mặc định chuyển về chế độ được xác định ở cấp tổ chức.</span><span class="sxs-lookup"><span data-stu-id="15884-143">The destination project will always default to the mode defined at the organizational level.</span></span>

## <a name="copied-tasks"></a><span data-ttu-id="15884-144">Nhiệm vụ được sao chép</span><span class="sxs-lookup"><span data-stu-id="15884-144">Copied tasks</span></span>

<span data-ttu-id="15884-145">Khi được sao chép từ dự án này sang dự án khác, nhiệm vụ sẽ kế thừa chế độ lập lịch trình của dự án đích.</span><span class="sxs-lookup"><span data-stu-id="15884-145">When a task is copied from one project to another, the task inherits the scheduling mode of the destination project.</span></span>
