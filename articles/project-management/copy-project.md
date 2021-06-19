---
title: Sao chép dự án
description: Chủ đề này cung cấp thông tin về việc sao chép dự án trong Dynamics 365 Project Operations.
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c3055ab5b8c07faa2bc9167956d283e2a66029dd
ms.sourcegitcommit: 173f2b1f4e063c440a5f78d76d456c62aadbd89e
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/24/2021
ms.locfileid: "6091280"
---
# <a name="copy-a-project"></a><span data-ttu-id="76f00-103">Sao chép dự án</span><span class="sxs-lookup"><span data-stu-id="76f00-103">Copy a project</span></span>

<span data-ttu-id="76f00-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="76f00-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="76f00-105">Với Dynamics 365 Project Operations, bạn có thể nhanh chóng tạo các dự án mới bằng cách chọn **Sao chép dự án** trên biểu mẫu **Dự án**.</span><span class="sxs-lookup"><span data-stu-id="76f00-105">With Dynamics 365 Project Operations, you can quickly build new projects by selecting **Copy Project** on the **Projects** form.</span></span> <span data-ttu-id="76f00-106">Để sao chép dự án, hãy mở dự án mà bạn muốn sao chép, rồi chọn **Sao chép dự án**.</span><span class="sxs-lookup"><span data-stu-id="76f00-106">To copy a project, open the project you want to copy, and then select **Copy project**.</span></span> <span data-ttu-id="76f00-107">Hành động này sẽ sao chép:</span><span class="sxs-lookup"><span data-stu-id="76f00-107">The action will copy the following:</span></span>

- <span data-ttu-id="76f00-108">Thuộc tính dự án</span><span class="sxs-lookup"><span data-stu-id="76f00-108">Project properties</span></span> 
- <span data-ttu-id="76f00-109">Cấu trúc phân tích công việc</span><span class="sxs-lookup"><span data-stu-id="76f00-109">Work breakdown structure</span></span>
- <span data-ttu-id="76f00-110">Thành viên nhóm dự án</span><span class="sxs-lookup"><span data-stu-id="76f00-110">Project team members</span></span>
- <span data-ttu-id="76f00-111">Ước tính dự án</span><span class="sxs-lookup"><span data-stu-id="76f00-111">Project estimates</span></span>
- <span data-ttu-id="76f00-112">Ước tính chi phí dự án</span><span class="sxs-lookup"><span data-stu-id="76f00-112">Project expense estimates</span></span>
- <span data-ttu-id="76f00-113">Ước tính vật tư của dự án</span><span class="sxs-lookup"><span data-stu-id="76f00-113">Project material estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="76f00-114">Thuộc tính dự án</span><span class="sxs-lookup"><span data-stu-id="76f00-114">Project properties</span></span>

<span data-ttu-id="76f00-115">Khi dự án được sao chép, các giá trị trong các trường sau sẽ được sao chép:</span><span class="sxs-lookup"><span data-stu-id="76f00-115">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="76f00-116">Tên</span><span class="sxs-lookup"><span data-stu-id="76f00-116">Name</span></span>
- <span data-ttu-id="76f00-117">Nội dung mô tả</span><span class="sxs-lookup"><span data-stu-id="76f00-117">Description</span></span>
- <span data-ttu-id="76f00-118">Khách hàng</span><span class="sxs-lookup"><span data-stu-id="76f00-118">Customer</span></span>
- <span data-ttu-id="76f00-119">Mẫu lịch</span><span class="sxs-lookup"><span data-stu-id="76f00-119">Calendar Template</span></span>
- <span data-ttu-id="76f00-120">Tiền tệ</span><span class="sxs-lookup"><span data-stu-id="76f00-120">Currency</span></span>
- <span data-ttu-id="76f00-121">Đơn vị Hợp đồng</span><span class="sxs-lookup"><span data-stu-id="76f00-121">Contracting Unit</span></span>
- <span data-ttu-id="76f00-122">Trình quản lý Dự án</span><span class="sxs-lookup"><span data-stu-id="76f00-122">Project Manager</span></span>
- <span data-ttu-id="76f00-123">Trạng thái</span><span class="sxs-lookup"><span data-stu-id="76f00-123">Status</span></span>
- <span data-ttu-id="76f00-124">Trạng thái của Dự án Tổng thể</span><span class="sxs-lookup"><span data-stu-id="76f00-124">Overall Project Status</span></span>
- <span data-ttu-id="76f00-125">Nhận xét</span><span class="sxs-lookup"><span data-stu-id="76f00-125">Comments</span></span>
- <span data-ttu-id="76f00-126">Ước tính</span><span class="sxs-lookup"><span data-stu-id="76f00-126">Estimates</span></span>
- <span data-ttu-id="76f00-127">Ngày bắt đầu ước tính: Đây là ngày tạo dự án từ bản sao.</span><span class="sxs-lookup"><span data-stu-id="76f00-127">Estimated Start Date: This is the date that the project is created from the copy.</span></span>
- <span data-ttu-id="76f00-128">Ngày kết thúc ước tính: Ngày này được điều chỉnh dựa trên ngày bắt đầu của dự án mới được tạo từ bản sao.</span><span class="sxs-lookup"><span data-stu-id="76f00-128">Estimated Finish Date: This date is adjusted based on the start date of the new project that was made from the copy.</span></span>
- <span data-ttu-id="76f00-129">Nỗ lực (giờ)</span><span class="sxs-lookup"><span data-stu-id="76f00-129">Effort (Hours)</span></span>
- <span data-ttu-id="76f00-130">Chi phí nhân công ước tính</span><span class="sxs-lookup"><span data-stu-id="76f00-130">Estimated Labor Cost</span></span>
- <span data-ttu-id="76f00-131">Chi phí phí tổn ước tính</span><span class="sxs-lookup"><span data-stu-id="76f00-131">Estimated Expense Cost</span></span>
- <span data-ttu-id="76f00-132">Chi phí ước tính của vật liệu</span><span class="sxs-lookup"><span data-stu-id="76f00-132">Estimated Material Cost</span></span>

> [!NOTE]
> <span data-ttu-id="76f00-133">Thao tác sao chép dự án sẽ tốn nhiều thời gian.</span><span class="sxs-lookup"><span data-stu-id="76f00-133">Copy project is a long running operation.</span></span> <span data-ttu-id="76f00-134">Bản ghi dự án, các thuộc tính tương ứng và nhiều thực thể liên quan cũng được sao chép.</span><span class="sxs-lookup"><span data-stu-id="76f00-134">Project records, their relevant attributes, and many related entities are also copied.</span></span> <span data-ttu-id="76f00-135">Do thao tác này sẽ kéo dài, nên sau khi quá trình sao chép bắt đầu, trang dự án đích sẽ bị khóa chức năng chỉnh sửa cho đến khi thao tác sao chép hoàn tất.</span><span class="sxs-lookup"><span data-stu-id="76f00-135">Because of the long running nature of the operation, after the copy starts, the target project page is locked for editing until the copy operation is complete.</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="76f00-136">Cấu trúc phân tích công việc</span><span class="sxs-lookup"><span data-stu-id="76f00-136">Work breakdown structure</span></span>

<span data-ttu-id="76f00-137">Khi dự án được sao chép, toàn bộ cấu trúc phân tích công việc đã tải nguồn lực sẽ được sao chép.</span><span class="sxs-lookup"><span data-stu-id="76f00-137">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="76f00-138">Nguồn lực có tên được thay thế bằng nguồn lực chung.</span><span class="sxs-lookup"><span data-stu-id="76f00-138">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="76f00-139">Nếu nguồn lực tên không có cùng giờ làm việc với nguồn lực chung, lịch trình sẽ được tính toán lại và thời lượng tác vụ có thể thay đổi.</span><span class="sxs-lookup"><span data-stu-id="76f00-139">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="76f00-140">Thành viên nhóm dự án</span><span class="sxs-lookup"><span data-stu-id="76f00-140">Project team members</span></span>

<span data-ttu-id="76f00-141">Khi một nhóm dự án được sao chép từ dự án nguồn, các tài nguyên chung sẽ được sao chép.</span><span class="sxs-lookup"><span data-stu-id="76f00-141">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="76f00-142">Việc phân công nguồn lực chung cũng được duy trì như khi chúng ở trong dự án nguồn.</span><span class="sxs-lookup"><span data-stu-id="76f00-142">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="76f00-143">Các nguồn lực có tên sẽ được chuyển đổi thành các thành viên nhóm chung.</span><span class="sxs-lookup"><span data-stu-id="76f00-143">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="76f00-144">Ước tính</span><span class="sxs-lookup"><span data-stu-id="76f00-144">Estimates</span></span>

<span data-ttu-id="76f00-145">Khi dự án được sao chép, các dòng ước tính tài nguyên, chi phí và vật tư được sao chép từ dự án nguồn.</span><span class="sxs-lookup"><span data-stu-id="76f00-145">When the project is copied, resource, expense and material estimate lines are copied from the source project.</span></span> 

<span data-ttu-id="76f00-146">Để biết thông tin về cách truy nhập Sao chép dự án theo lập trình, hãy xem [Phát triển các mẫu dự án với Sao chép dự án](dev-copy-project.md).</span><span class="sxs-lookup"><span data-stu-id="76f00-146">For information on how to programmatically access Copy Project, see [Develop project templates with Copy Project](dev-copy-project.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
