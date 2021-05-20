---
title: Chế độ lập lịch trình
description: Chủ đề này cung cấp thông tin về chế độ lập lịch trình.
author: ruhercul
manager: AnnBe
ms.date: 05/04/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fe54944999617b248ff925148a78601dd4be7aca
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981461"
---
# <a name="scheduling-modes"></a><span data-ttu-id="8d53b-103">Chế độ lập lịch trình</span><span class="sxs-lookup"><span data-stu-id="8d53b-103">Scheduling modes</span></span>

<span data-ttu-id="8d53b-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="8d53b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="8d53b-105">Dynamics 365 Project Operations cung cấp khả năng cho các tổ chức để xác định cách họ quản lý thay đổi đối với các biến chính trong nhiệm vụ của cấu trúc phân tích công việc.</span><span class="sxs-lookup"><span data-stu-id="8d53b-105">Dynamics 365 Project Operations provides the ability for organizations to define how they manage changes to key variables in tasks within the work breakdown structure.</span></span> <span data-ttu-id="8d53b-106">Dựa trên nhu cầu cụ thể của tổ chức, Người quản lý dự án có thể thực hiện các thay đổi đối với chế độ lập lịch trình khi một dự án được tạo.</span><span class="sxs-lookup"><span data-stu-id="8d53b-106">Based on the specific needs of the organization, Project Managers can make changes to the scheduling mode when a project is created.</span></span>

<span data-ttu-id="8d53b-107">Có ba chế độ lập lịch trình có sẵn trong Project Operations:</span><span class="sxs-lookup"><span data-stu-id="8d53b-107">There are three scheduling modes available in Project Operations:</span></span>

  - <span data-ttu-id="8d53b-108">Khoảng thời gian cố định (đây là chế độ mặc định)</span><span class="sxs-lookup"><span data-stu-id="8d53b-108">Fixed duration (this is the default mode)</span></span>
  - <span data-ttu-id="8d53b-109">Công việc cố định</span><span class="sxs-lookup"><span data-stu-id="8d53b-109">Fixed work</span></span>
  - <span data-ttu-id="8d53b-110">Đơn vị cố định</span><span class="sxs-lookup"><span data-stu-id="8d53b-110">Fixed units</span></span>

<span data-ttu-id="8d53b-111">Các giá trị bị định nghĩa của một chế độ lập lịch trình cụ thể tác động được xác định theo công thức sau:</span><span class="sxs-lookup"><span data-stu-id="8d53b-111">The values impacted by the definition of a specific scheduling mode are determined by the following formula:</span></span>

  <span data-ttu-id="8d53b-112">Nỗ lực (*Công việc*) = Khoảng thời gian x Đơn vị</span><span class="sxs-lookup"><span data-stu-id="8d53b-112">Effort (*Work*) = Duration x Units</span></span>

<span data-ttu-id="8d53b-113">Khi xác định chế độ lập lịch trình của dự án, bạn đang thiết lập một trong những giá trị này, sau đó không thể thay đổi được.</span><span class="sxs-lookup"><span data-stu-id="8d53b-113">When you define a project’s scheduling mode, you are setting one of these values, which then can't be changed.</span></span> <span data-ttu-id="8d53b-114">Duy trì giá trị này là một hằng số sẽ đặt ưu tiên cho giá trị đó, điều này sẽ thông báo cho hệ thống không thay đổi giá trị này khi hai giá trị khác thay đổi.</span><span class="sxs-lookup"><span data-stu-id="8d53b-114">Holding this value as a constant places a priority on that value, which notifies the system not to change it when the other two values change.</span></span> <span data-ttu-id="8d53b-115">Bảng sau đây cung cấp thông tin về tác động của việc chọn một chế độ cụ thể.</span><span class="sxs-lookup"><span data-stu-id="8d53b-115">The following table provides information about the impacts of selecting a specific mode.</span></span>

| <span data-ttu-id="8d53b-116">**Trong nhiệm vụ này**</span><span class="sxs-lookup"><span data-stu-id="8d53b-116">**In this task**</span></span>             | <span data-ttu-id="8d53b-117">**Nếu bạn sửa các đơn vị**</span><span class="sxs-lookup"><span data-stu-id="8d53b-117">**If you revise units**</span></span>   | <span data-ttu-id="8d53b-118">**Nếu bạn sửa khoảng thời gian**</span><span class="sxs-lookup"><span data-stu-id="8d53b-118">**If you revise duration**</span></span> | <span data-ttu-id="8d53b-119">**Nếu bạn sửa nỗ lực**</span><span class="sxs-lookup"><span data-stu-id="8d53b-119">**If you revise effort**</span></span>  |
|----------------------|---------------------------|----------------------------|---------------------------|
| <span data-ttu-id="8d53b-120">Nhiệm vụ đơn vị cố định</span><span class="sxs-lookup"><span data-stu-id="8d53b-120">Fixed units task</span></span>     | <span data-ttu-id="8d53b-121">Khoảng thời gian được tính toán lại.</span><span class="sxs-lookup"><span data-stu-id="8d53b-121">Duration is recalculated.</span></span> | <span data-ttu-id="8d53b-122">Nỗ lực được tính toán lại.</span><span class="sxs-lookup"><span data-stu-id="8d53b-122">Effort is recalculated.</span></span>    | <span data-ttu-id="8d53b-123">Khoảng thời gian được tính toán lại.</span><span class="sxs-lookup"><span data-stu-id="8d53b-123">Duration is recalculated.</span></span> |
| <span data-ttu-id="8d53b-124">Nhiệm vụ nỗ lực cố định</span><span class="sxs-lookup"><span data-stu-id="8d53b-124">Fixed effort task</span></span>    | <span data-ttu-id="8d53b-125">Khoảng thời gian được tính toán lại.</span><span class="sxs-lookup"><span data-stu-id="8d53b-125">Duration is recalculated.</span></span> | <span data-ttu-id="8d53b-126">Các đơn vị được tính toán lại.</span><span class="sxs-lookup"><span data-stu-id="8d53b-126">Units are recalculated.</span></span>    | <span data-ttu-id="8d53b-127">Khoảng thời gian được tính toán lại.</span><span class="sxs-lookup"><span data-stu-id="8d53b-127">Duration is recalculated.</span></span> |
| <span data-ttu-id="8d53b-128">Nhiệm vụ khoảng thời gian cố định</span><span class="sxs-lookup"><span data-stu-id="8d53b-128">Fixed duration task</span></span>  | <span data-ttu-id="8d53b-129">Nỗ lực được tính toán lại.</span><span class="sxs-lookup"><span data-stu-id="8d53b-129">Effort is recalculated.</span></span>   | <span data-ttu-id="8d53b-130">Nỗ lực được tính toán lại.</span><span class="sxs-lookup"><span data-stu-id="8d53b-130">Effort is recalculated.</span></span>    | <span data-ttu-id="8d53b-131">Các đơn vị được tính toán lại.</span><span class="sxs-lookup"><span data-stu-id="8d53b-131">Units are recalculated.</span></span>   |

<span data-ttu-id="8d53b-132">Để biết thêm thông tin về tác động của một chế độ nhất định, hãy xem [Thay đổi loại nhiệm vụ để lập lịch chính xác hơn](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span><span class="sxs-lookup"><span data-stu-id="8d53b-132">For more information about the implications of a given mode, see [Change the task type for more accurate scheduling](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span></span> <span data-ttu-id="8d53b-133">Trong chủ đề này, thuật ngữ **Công việc** được sử dụng thay cho **Nỗ lực**.</span><span class="sxs-lookup"><span data-stu-id="8d53b-133">In the topic, the term **Work** is used instead of **Effort**.</span></span>

## <a name="change-the-organizations-scheduling-mode"></a><span data-ttu-id="8d53b-134">Thay đổi chế độ lập lịch trình của tổ chức</span><span class="sxs-lookup"><span data-stu-id="8d53b-134">Change the organization’s scheduling mode</span></span>

<span data-ttu-id="8d53b-135">Hoàn thành các bước sau để xác định chế độ lập lịch trình của một tổ chức.</span><span class="sxs-lookup"><span data-stu-id="8d53b-135">Complete the following steps to define the scheduling mode of an organization.</span></span>

1. <span data-ttu-id="8d53b-136">Chuyển đến phần **Cài đặt** \> **Chung** \> **Thông số** rồi chọn thông số dự án.</span><span class="sxs-lookup"><span data-stu-id="8d53b-136">Go to **Settings** \> **General** \> **Parameters**, and then select the project parameter.</span></span> 
2. <span data-ttu-id="8d53b-137">Trên trang **Thông số dự án**, hãy chọn chế độ lập lịch trình mặc định cho tổ chức rồi xác định khả năng cho Người quản lý dự án ghi đè cài đặt khi tạo một dự án mới.</span><span class="sxs-lookup"><span data-stu-id="8d53b-137">On the **Project Parameters** page, select the default scheduling mode for the organization, and then define ability for the Project manager to override the setting when creating a new project.</span></span>

## <a name="change-the-scheduling-mode-setting-on-a-project"></a><span data-ttu-id="8d53b-138">Thay đổi tùy chọn cài đặt của chế độ lập lịch trình trên một dự án</span><span class="sxs-lookup"><span data-stu-id="8d53b-138">Change the scheduling mode setting on a project</span></span>

<span data-ttu-id="8d53b-139">Nếu một tổ chức cho phép Người quản lý dự án ghi đè chế độ lập lịch trình mặc định, Người quản lý dự án có thể thực hiện thay đổi đó khi họ tạo một dự án mới.</span><span class="sxs-lookup"><span data-stu-id="8d53b-139">If an organization allows the Project manager to override the default scheduling mode, the Project manager can make that change when they create a new project.</span></span> <span data-ttu-id="8d53b-140">Tuy nhiên, sau khi dự án đã được lưu, không thể thay đổi chế độ lập lịch trình.</span><span class="sxs-lookup"><span data-stu-id="8d53b-140">However, after the project has been saved, the scheduling mode can't be changed.</span></span>

## <a name="copied-projects"></a><span data-ttu-id="8d53b-141">Dự án được sao chép</span><span class="sxs-lookup"><span data-stu-id="8d53b-141">Copied projects</span></span>

<span data-ttu-id="8d53b-142">Vì dự án được tạo khi thực hiện thao tác sao chép dự án, nên Người quản lý dự án không thể thiết lập chế độ lập lịch trình.</span><span class="sxs-lookup"><span data-stu-id="8d53b-142">Because a project is created when the copy project action is taken, the Project manager can't set the scheduling mode.</span></span> <span data-ttu-id="8d53b-143">Dự án đích sẽ luôn mặc định chuyển về chế độ được xác định ở cấp tổ chức.</span><span class="sxs-lookup"><span data-stu-id="8d53b-143">The destination project will always default to the mode defined at the organizational level.</span></span>

## <a name="copied-tasks"></a><span data-ttu-id="8d53b-144">Nhiệm vụ được sao chép</span><span class="sxs-lookup"><span data-stu-id="8d53b-144">Copied tasks</span></span>

<span data-ttu-id="8d53b-145">Khi được sao chép từ dự án này sang dự án khác, nhiệm vụ sẽ kế thừa chế độ lập lịch trình của dự án đích.</span><span class="sxs-lookup"><span data-stu-id="8d53b-145">When a task is copied from one project to another, the task inherits the scheduling mode of the destination project.</span></span>
