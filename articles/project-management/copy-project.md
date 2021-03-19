---
title: Sao chép dự án
description: Chủ đề này cung cấp thông tin về việc sao chép dự án trong Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 02/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: af1942e81691d9e13fdcbbf68599c1a8a4004582
ms.sourcegitcommit: 24528bb9c0ef8898077cb3bc672daa211c0e73aa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 03/04/2021
ms.locfileid: "5479545"
---
# <a name="copy-a-project"></a><span data-ttu-id="c397d-103">Sao chép dự án</span><span class="sxs-lookup"><span data-stu-id="c397d-103">Copy a project</span></span>

<span data-ttu-id="c397d-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="c397d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c397d-105">Với Dynamics 365 Project Operations, bạn có thể nhanh chóng tạo các dự án mới bằng cách chọn **Sao chép dự án** trên biểu mẫu **Dự án**.</span><span class="sxs-lookup"><span data-stu-id="c397d-105">With Dynamics 365 Project Operations, you can quickly build new projects by selecting **Copy Project** on the **Projects** form.</span></span> <span data-ttu-id="c397d-106">Để sao chép dự án, hãy mở dự án mà bạn muốn sao chép, rồi chọn **Sao chép dự án**.</span><span class="sxs-lookup"><span data-stu-id="c397d-106">To copy a project, open the project you want to copy, and then select **Copy project**.</span></span> <span data-ttu-id="c397d-107">Hành động sẽ sao chép:</span><span class="sxs-lookup"><span data-stu-id="c397d-107">The action will copy:</span></span>

- <span data-ttu-id="c397d-108">Thuộc tính dự án (Ngày bắt đầu ước tính được sao chép từ dự án nguồn)</span><span class="sxs-lookup"><span data-stu-id="c397d-108">Project properties (The estimated start date is copied from the source project)</span></span>
- <span data-ttu-id="c397d-109">Cấu trúc phân tích công việc</span><span class="sxs-lookup"><span data-stu-id="c397d-109">The Work breakdown structure</span></span>
- <span data-ttu-id="c397d-110">Thành viên nhóm dự án</span><span class="sxs-lookup"><span data-stu-id="c397d-110">Project team members</span></span>
- <span data-ttu-id="c397d-111">Ước tính dự án</span><span class="sxs-lookup"><span data-stu-id="c397d-111">Project estimates</span></span>
- <span data-ttu-id="c397d-112">Ước tính chi phí dự án</span><span class="sxs-lookup"><span data-stu-id="c397d-112">Project expense estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="c397d-113">Thuộc tính dự án</span><span class="sxs-lookup"><span data-stu-id="c397d-113">Project properties</span></span>

<span data-ttu-id="c397d-114">Khi dự án được sao chép, các giá trị trong các trường sau sẽ được sao chép:</span><span class="sxs-lookup"><span data-stu-id="c397d-114">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="c397d-115">Tên</span><span class="sxs-lookup"><span data-stu-id="c397d-115">Name</span></span>
- <span data-ttu-id="c397d-116">Nội dung mô tả</span><span class="sxs-lookup"><span data-stu-id="c397d-116">Description</span></span>
- <span data-ttu-id="c397d-117">Khách hàng</span><span class="sxs-lookup"><span data-stu-id="c397d-117">Customer</span></span>
- <span data-ttu-id="c397d-118">Mẫu lịch</span><span class="sxs-lookup"><span data-stu-id="c397d-118">Calendar Template</span></span>
- <span data-ttu-id="c397d-119">Tiền tệ</span><span class="sxs-lookup"><span data-stu-id="c397d-119">Currency</span></span>
- <span data-ttu-id="c397d-120">Đơn vị Hợp đồng</span><span class="sxs-lookup"><span data-stu-id="c397d-120">Contracting Unit</span></span>
- <span data-ttu-id="c397d-121">Trình quản lý Dự án</span><span class="sxs-lookup"><span data-stu-id="c397d-121">Project Manager</span></span>
- <span data-ttu-id="c397d-122">Trạng thái</span><span class="sxs-lookup"><span data-stu-id="c397d-122">Status</span></span>
- <span data-ttu-id="c397d-123">Trạng thái của Dự án Tổng thể</span><span class="sxs-lookup"><span data-stu-id="c397d-123">Overall Project Status</span></span>
- <span data-ttu-id="c397d-124">Bình luận</span><span class="sxs-lookup"><span data-stu-id="c397d-124">Comments</span></span>
- <span data-ttu-id="c397d-125">Ước tính</span><span class="sxs-lookup"><span data-stu-id="c397d-125">Estimates</span></span>
- <span data-ttu-id="c397d-126">Ngày Bắt đầu Ước tính</span><span class="sxs-lookup"><span data-stu-id="c397d-126">Estimated Start Date</span></span>
- <span data-ttu-id="c397d-127">Ngày hoàn thành</span><span class="sxs-lookup"><span data-stu-id="c397d-127">Finish Date</span></span>
- <span data-ttu-id="c397d-128">Nỗ lực (giờ)</span><span class="sxs-lookup"><span data-stu-id="c397d-128">Effort (Hours)</span></span>
- <span data-ttu-id="c397d-129">Chi phí nhân công ước tính</span><span class="sxs-lookup"><span data-stu-id="c397d-129">Estimated Labor Cost</span></span>
- <span data-ttu-id="c397d-130">Chi phí Phí tổn Ước tính</span><span class="sxs-lookup"><span data-stu-id="c397d-130">Estimated Expense Cost</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="c397d-131">Cấu trúc phân tích công việc</span><span class="sxs-lookup"><span data-stu-id="c397d-131">Work breakdown structure</span></span>

<span data-ttu-id="c397d-132">Khi dự án được sao chép, toàn bộ cấu trúc phân tích công việc đã tải nguồn lực sẽ được sao chép.</span><span class="sxs-lookup"><span data-stu-id="c397d-132">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="c397d-133">Nguồn lực có tên được thay thế bằng nguồn lực chung.</span><span class="sxs-lookup"><span data-stu-id="c397d-133">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="c397d-134">Nếu nguồn lực tên không có cùng giờ làm việc với nguồn lực chung, lịch trình sẽ được tính toán lại và thời lượng tác vụ có thể thay đổi.</span><span class="sxs-lookup"><span data-stu-id="c397d-134">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="c397d-135">Thành viên nhóm dự án</span><span class="sxs-lookup"><span data-stu-id="c397d-135">Project team members</span></span>

<span data-ttu-id="c397d-136">Khi một nhóm dự án được sao chép từ dự án nguồn, các tài nguyên chung sẽ được sao chép.</span><span class="sxs-lookup"><span data-stu-id="c397d-136">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="c397d-137">Việc phân công nguồn lực chung cũng được duy trì như khi chúng ở trong dự án nguồn.</span><span class="sxs-lookup"><span data-stu-id="c397d-137">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="c397d-138">Các nguồn lực có tên sẽ được chuyển đổi thành các thành viên nhóm chung.</span><span class="sxs-lookup"><span data-stu-id="c397d-138">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="c397d-139">Ước tính</span><span class="sxs-lookup"><span data-stu-id="c397d-139">Estimates</span></span>

<span data-ttu-id="c397d-140">Khi dự án được sao chép, cả dòng ước tính nguồn lực và chi phí đều được sao chép từ dự án nguồn.</span><span class="sxs-lookup"><span data-stu-id="c397d-140">When the project is copied, both resource and expense estimate lines are copied from the source project.</span></span> 

<span data-ttu-id="c397d-141">Để biết thông tin về cách truy nhập Sao chép dự án theo lập trình, hãy xem [Phát triển các mẫu dự án với Sao chép dự án](dev-copy-project.md).</span><span class="sxs-lookup"><span data-stu-id="c397d-141">For information on how to programmatically access Copy Project, see [Develop project templates with Copy Project](dev-copy-project.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
