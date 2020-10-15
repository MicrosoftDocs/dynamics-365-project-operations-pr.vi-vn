---
title: Sao chép dự án
description: Chủ đề này cung cấp thông tin về cách sao chép dự án trong Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e35dc725e7938e9f59f7151dd1b37500fabf77a4
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908737"
---
# <a name="copy-a-project"></a><span data-ttu-id="a428a-103">Sao chép dự án</span><span class="sxs-lookup"><span data-stu-id="a428a-103">Copy a project</span></span>

<span data-ttu-id="a428a-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="a428a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a428a-105">Với Dynamics 365 Project Operations, bạn có thể nhanh chóng xây dựng các dự án mới bằng cách sử dụng thao tác **Sao chép dự án** trên biểu mẫu **Dự án**.</span><span class="sxs-lookup"><span data-stu-id="a428a-105">With Dynamics 365 Project Operations, you can quickly build new projects by using the **Copy Project** action on the **Projects** from.</span></span> <span data-ttu-id="a428a-106">Để sao chép dự án, hãy chọn một dự án, sau đó chọn **Sao chép**.</span><span class="sxs-lookup"><span data-stu-id="a428a-106">To copy a project, select a project, and then select **Copy**.</span></span> <span data-ttu-id="a428a-107">Hành động sẽ sao chép:</span><span class="sxs-lookup"><span data-stu-id="a428a-107">The action will copy:</span></span>

- <span data-ttu-id="a428a-108">Thuộc tính dự án</span><span class="sxs-lookup"><span data-stu-id="a428a-108">Project properties</span></span>
- <span data-ttu-id="a428a-109">Cấu trúc phân tích công việc</span><span class="sxs-lookup"><span data-stu-id="a428a-109">The Work breakdown structure</span></span>
- <span data-ttu-id="a428a-110">Thành viên nhóm dự án</span><span class="sxs-lookup"><span data-stu-id="a428a-110">Project team members</span></span>
- <span data-ttu-id="a428a-111">Ước tính dự án</span><span class="sxs-lookup"><span data-stu-id="a428a-111">Project estimates</span></span>
- <span data-ttu-id="a428a-112">Ước tính chi phí dự án</span><span class="sxs-lookup"><span data-stu-id="a428a-112">Project expense estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="a428a-113">Thuộc tính dự án</span><span class="sxs-lookup"><span data-stu-id="a428a-113">Project properties</span></span>

<span data-ttu-id="a428a-114">Khi dự án được sao chép, các giá trị trong các trường sau sẽ được sao chép:</span><span class="sxs-lookup"><span data-stu-id="a428a-114">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="a428a-115">Tên</span><span class="sxs-lookup"><span data-stu-id="a428a-115">Name</span></span>
- <span data-ttu-id="a428a-116">Nội dung mô tả</span><span class="sxs-lookup"><span data-stu-id="a428a-116">Description</span></span>
- <span data-ttu-id="a428a-117">Khách hàng</span><span class="sxs-lookup"><span data-stu-id="a428a-117">Customer</span></span>
- <span data-ttu-id="a428a-118">Mẫu lịch</span><span class="sxs-lookup"><span data-stu-id="a428a-118">Calendar Template</span></span>
- <span data-ttu-id="a428a-119">Tiền tệ</span><span class="sxs-lookup"><span data-stu-id="a428a-119">Currency</span></span>
- <span data-ttu-id="a428a-120">Đơn vị Hợp đồng</span><span class="sxs-lookup"><span data-stu-id="a428a-120">Contracting Unit</span></span>
- <span data-ttu-id="a428a-121">Trình quản lý Dự án</span><span class="sxs-lookup"><span data-stu-id="a428a-121">Project Manager</span></span>
- <span data-ttu-id="a428a-122">Trạng thái</span><span class="sxs-lookup"><span data-stu-id="a428a-122">Status</span></span>
- <span data-ttu-id="a428a-123">Trạng thái của Dự án Tổng thể</span><span class="sxs-lookup"><span data-stu-id="a428a-123">Overall Project Status</span></span>
- <span data-ttu-id="a428a-124">Bình luận</span><span class="sxs-lookup"><span data-stu-id="a428a-124">Comments</span></span>
- <span data-ttu-id="a428a-125">Ước tính</span><span class="sxs-lookup"><span data-stu-id="a428a-125">Estimates</span></span>
- <span data-ttu-id="a428a-126">Ngày Bắt đầu Ước tính</span><span class="sxs-lookup"><span data-stu-id="a428a-126">Estimated Start Date</span></span>
- <span data-ttu-id="a428a-127">Ngày hoàn thành</span><span class="sxs-lookup"><span data-stu-id="a428a-127">Finish Date</span></span>
- <span data-ttu-id="a428a-128">Nỗ lực (giờ)</span><span class="sxs-lookup"><span data-stu-id="a428a-128">Effort (Hours)</span></span>
- <span data-ttu-id="a428a-129">Chi phí nhân công ước tính</span><span class="sxs-lookup"><span data-stu-id="a428a-129">Estimated Labor Cost</span></span>
- <span data-ttu-id="a428a-130">Chi phí Phí tổn Ước tính</span><span class="sxs-lookup"><span data-stu-id="a428a-130">Estimated Expense Cost</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="a428a-131">Cấu trúc phân tích công việc</span><span class="sxs-lookup"><span data-stu-id="a428a-131">Work breakdown structure</span></span>

<span data-ttu-id="a428a-132">Khi dự án được sao chép, toàn bộ cấu trúc phân tích công việc đã tải nguồn lực sẽ được sao chép.</span><span class="sxs-lookup"><span data-stu-id="a428a-132">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="a428a-133">Nguồn lực có tên được thay thế bằng nguồn lực chung.</span><span class="sxs-lookup"><span data-stu-id="a428a-133">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="a428a-134">Nếu nguồn lực tên không có cùng giờ làm việc với nguồn lực chung, lịch trình sẽ được tính toán lại và thời lượng tác vụ có thể thay đổi.</span><span class="sxs-lookup"><span data-stu-id="a428a-134">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="a428a-135">Thành viên nhóm dự án</span><span class="sxs-lookup"><span data-stu-id="a428a-135">Project team members</span></span>

<span data-ttu-id="a428a-136">Khi một nhóm dự án được sao chép từ dự án nguồn, các tài nguyên chung sẽ được sao chép.</span><span class="sxs-lookup"><span data-stu-id="a428a-136">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="a428a-137">Việc phân công nguồn lực chung cũng được duy trì như khi chúng ở trong dự án nguồn.</span><span class="sxs-lookup"><span data-stu-id="a428a-137">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="a428a-138">Các nguồn lực có tên sẽ được chuyển đổi thành các thành viên nhóm chung.</span><span class="sxs-lookup"><span data-stu-id="a428a-138">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="a428a-139">Ước tính</span><span class="sxs-lookup"><span data-stu-id="a428a-139">Estimates</span></span>

<span data-ttu-id="a428a-140">Khi dự án được sao chép, cả dòng ước tính nguồn lực và chi phí đều được sao chép từ dự án nguồn.</span><span class="sxs-lookup"><span data-stu-id="a428a-140">When the project is copied, both resource and expense estimate lines are copied from the source project.</span></span>