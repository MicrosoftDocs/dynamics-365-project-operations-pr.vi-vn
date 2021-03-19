---
title: Xem mức sử dụng có thể tính phí cho các nguồn lực
description: Chủ đề này cung cấp thông tin về cách xem mức sử dụng nguồn lực.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: b07af573bc8d312c45ee4aef50c95942401294fa
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285959"
---
# <a name="view-chargeable-utilization-for-resources"></a><span data-ttu-id="f7829-103">Xem mức sử dụng có thể tính phí cho các nguồn lực</span><span class="sxs-lookup"><span data-stu-id="f7829-103">View chargeable utilization for resources</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]
 
<span data-ttu-id="f7829-104">**Dạng xem thời gian làm việc** trên trang **Thời gian làm việc của nguồn lực trong Project Service** hiển thị thời gian làm việc có thể tính phí cho mỗi nguồn lực có thể đặt lịch.</span><span class="sxs-lookup"><span data-stu-id="f7829-104">The **Utilization View** on the **Project Service Resource Utilization** page shows the chargeable utilization for each bookable resource.</span></span> <span data-ttu-id="f7829-105">Vì dạng xem dựa trên bảng lịch trình, do đó, bạn sẽ tìm thấy nhiều chức năng tương tự.</span><span class="sxs-lookup"><span data-stu-id="f7829-105">Because the view is based on the schedule board, you’ll find many of the same functions.</span></span>

> ![Ảnh chụp màn hình của Dạng xem Thời gian làm việc](media/FAQ-utilization-1.png)
 

<span data-ttu-id="f7829-107">Thời gian làm việc có thể tính phí được tính như sau:</span><span class="sxs-lookup"><span data-stu-id="f7829-107">The chargeable utilization calculation works as follows:</span></span>

   <span data-ttu-id="f7829-108">Thời gian làm việc có thể tính phí = (Số giờ thực có thể tính phí)/ (Năng lực của nguồn lực)</span><span class="sxs-lookup"><span data-stu-id="f7829-108">Chargeable utilization = (Chargeable actual hours) / (resource capacity)</span></span>

<span data-ttu-id="f7829-109">Các ô đại diện cho thời gian làm việc có thể tính phí được tính cho khoảng thời gian được chọn (ngày, tuần hoặc tháng).</span><span class="sxs-lookup"><span data-stu-id="f7829-109">The cells represent the calculated chargeable utilization for the selected period (days, weeks, or months).</span></span>

<span data-ttu-id="f7829-110">Màu sắc trong mỗi ô hiển thị thời gian làm việc có thể tính phí đối với tài nguyên so với thời gian làm việc có thể tính phí mục tiêu.</span><span class="sxs-lookup"><span data-stu-id="f7829-110">The colors in each cell show the chargeable utilization for a resource as compared to their target chargeable utilization.</span></span> 

<span data-ttu-id="f7829-111">Thời gian làm việc mục tiêu có thể được đặt trên vai trò mặc định của nguồn lực hoặc trên bản thân nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="f7829-111">The target utilization can be set on the resource’s default role or on the individual resource itself.</span></span> <span data-ttu-id="f7829-112">Việc tính toán xét đến từng nguồn lực trước, sau đó đến vai trò mặc định của nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="f7829-112">The calculation looks at the individual for the target first, and then to the resource’s default role.</span></span>

## <a name="set-target-on-a-resource"></a><span data-ttu-id="f7829-113">Đặt mục tiêu trên tài nguyên</span><span class="sxs-lookup"><span data-stu-id="f7829-113">Set target on a resource</span></span>

1. <span data-ttu-id="f7829-114">Truy cập vào **Nguồn lực** \> **Nguồn lực**.</span><span class="sxs-lookup"><span data-stu-id="f7829-114">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="f7829-115">Chọn một nguồn lực để mở bản ghi.</span><span class="sxs-lookup"><span data-stu-id="f7829-115">Select a resource to open the record.</span></span> 
3. <span data-ttu-id="f7829-116">Trên tab **Project Service**, bạn có thể đặt thời gian làm việc mục tiêu của nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="f7829-116">On the **Project Service** tab, you can set the resource’s target utilization.</span></span>

> ![Ảnh chụp màn hình thao tác sử dụng tab Project Service để đặt thời gian làm việc mục tiêu](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a><span data-ttu-id="f7829-118">Đặt thời gian làm việc mục tiêu trên một vai trò</span><span class="sxs-lookup"><span data-stu-id="f7829-118">Set target utilization on a role</span></span>

1. <span data-ttu-id="f7829-119">Truy cập **Nguồn lực** \> **Vai trò nguồn lực**.</span><span class="sxs-lookup"><span data-stu-id="f7829-119">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="f7829-120">Chọn một vai trò và mở bản ghi.</span><span class="sxs-lookup"><span data-stu-id="f7829-120">Select a role and open the record.</span></span> 
3. <span data-ttu-id="f7829-121">Đặt thời gian làm việc mục tiêu cho vai trò.</span><span class="sxs-lookup"><span data-stu-id="f7829-121">Set the target utilization for the role.</span></span>

> ![Ảnh chụp màn hình khi sử dụng Vai trò Nguồn lực để đặt thời gian làm việc mục tiêu](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a><span data-ttu-id="f7829-123">Tính thời gian làm việc có thể tính phí cho một nguồn lực</span><span class="sxs-lookup"><span data-stu-id="f7829-123">Calculate chargeable utilization for a resource</span></span>

<span data-ttu-id="f7829-124">Để tính toán thời gian làm việc có thể tính phí cho một nguồn lực, bạn cần phải thực hiện một số điều kiện tiên quyết.</span><span class="sxs-lookup"><span data-stu-id="f7829-124">To calculate chargeable utilization for a resource, you will need to complete some pre-requisites.</span></span> 

### <a name="set-default-role-for-individual-resource"></a><span data-ttu-id="f7829-125">Đặt vai trò mặc định cho từng tài nguyên</span><span class="sxs-lookup"><span data-stu-id="f7829-125">Set default role for individual resource</span></span>

<span data-ttu-id="f7829-126">Đầu tiên, thời gian làm việc mục tiêu phải được đặt trên từng nguồn lực hoặc trên vai trò của nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="f7829-126">First, the target utilization must be set on either the individual resource or on resource roles.</span></span> <span data-ttu-id="f7829-127">Nếu bạn đang sử dụng vai trò của nguồn lực cho mục tiêu, từng nguồn lực phải có một vai trò mặc định.</span><span class="sxs-lookup"><span data-stu-id="f7829-127">If you are using resource roles for targets, each individual resource must have a default role.</span></span> 

1. <span data-ttu-id="f7829-128">Để đặt, hãy vào phần **Nguồn lực** \> **Nguồn lực**.</span><span class="sxs-lookup"><span data-stu-id="f7829-128">To set this, go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="f7829-129">Chọn một nguồn lực, mở bản ghi, sau đó chọn tab **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="f7829-129">Select a resource, open the record, and then select the **Project Service** tab.</span></span> 
3. <span data-ttu-id="f7829-130">Trong lưới **Vai trò nguồn lực**, đảm bảo có một vai trò cho nguồn lực và **Là mặc định** được đặt là **Có**.</span><span class="sxs-lookup"><span data-stu-id="f7829-130">In the **Resource Role** grid, make sure there’s one role for the resource and **Is Default** is set to **Yes**.</span></span>
 
### <a name="change-billing-type-for-resource-role"></a><span data-ttu-id="f7829-131">Thay đổi loại thanh toán cho vai trò nguồn lực này</span><span class="sxs-lookup"><span data-stu-id="f7829-131">Change billing type for resource role</span></span>

<span data-ttu-id="f7829-132">Vai trò của nguồn lực phải được đặt để có một loại thanh toán **Có thể tính phí**.</span><span class="sxs-lookup"><span data-stu-id="f7829-132">The resource roles must be set to have a billing type of **Chargeable**.</span></span> 

1. <span data-ttu-id="f7829-133">Truy cập **Nguồn lực** \> **Vai trò nguồn lực**.</span><span class="sxs-lookup"><span data-stu-id="f7829-133">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="f7829-134">Trên bản ghi bạn muốn cập nhật, sau đó thiết lập loại thanh toán mặc định thành **Có thể tính phí**.</span><span class="sxs-lookup"><span data-stu-id="f7829-134">Open the record you want to update, and then set the billing type default to **Chargeable**.</span></span>

### <a name="set-working-hours-for-resource-role"></a><span data-ttu-id="f7829-135">Đặt số giờ làm việc cho vai trò nguồn lực</span><span class="sxs-lookup"><span data-stu-id="f7829-135">Set working hours for resource role</span></span>
 
<span data-ttu-id="f7829-136">Nguồn lực phải có giờ làm việc để tính toán năng lực.</span><span class="sxs-lookup"><span data-stu-id="f7829-136">The resource must have working hours for the capacity calculation.</span></span> 

1. <span data-ttu-id="f7829-137">Truy cập vào **Nguồn lực** \> **Nguồn lực**.</span><span class="sxs-lookup"><span data-stu-id="f7829-137">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="f7829-138">Chọn một nguồn lực để mở bản ghi, sau đó chọn **Hiện số giờ làm việc**.</span><span class="sxs-lookup"><span data-stu-id="f7829-138">Select a resource to open the record, and then select **Show Work Hours**.</span></span> 
3. <span data-ttu-id="f7829-139">Bạn có thể cập nhật hàng loạt danh sách nguồn lực bằng cách áp dụng một **Mẫu giờ làm việc** từ dạng xem **Danh sách nguồn lực**.</span><span class="sxs-lookup"><span data-stu-id="f7829-139">You can bulk-update the list of resources by applying a **Work Hour Template** from the **Resource List** view.</span></span>

## <a name="troubleshooting-chargeable-actual-hours"></a><span data-ttu-id="f7829-140">Khắc phục sự cố giờ thực tế tính phí</span><span class="sxs-lookup"><span data-stu-id="f7829-140">Troubleshooting chargeable actual hours</span></span>

<span data-ttu-id="f7829-141">Giờ thực tế có thể tính phí có nguồn từ thực thể **Thực tế**.</span><span class="sxs-lookup"><span data-stu-id="f7829-141">The chargeable actual hours are sourced from the **Actuals** entity.</span></span> <span data-ttu-id="f7829-142">Quá trình tính toán bao gồm các thực tế với loại thanh toán **Có thể tính phí** và vì vậy, bạn phải có dự án mà trong đó các thực tế có thể tính phí.</span><span class="sxs-lookup"><span data-stu-id="f7829-142">Actuals with a billing type of **Chargeable** are included in the calculation and, for this reason, you must have projects where the actuals that are chargeable.</span></span>

<span data-ttu-id="f7829-143">Nếu không thấy thời gian làm việc có thể tính phí, bạn có thể kiểm tra một vài điều sau:</span><span class="sxs-lookup"><span data-stu-id="f7829-143">If you are not seeing chargeable utilization, here are some things you can check:</span></span>

- <span data-ttu-id="f7829-144">Nguồn lực có giờ làm việc được xác định cho năng lực.</span><span class="sxs-lookup"><span data-stu-id="f7829-144">The resource has working hours defined for capacity.</span></span>
- <span data-ttu-id="f7829-145">Nguồn lực có thời gian làm việc mục tiêu được xác định riêng hoặc có một vai trò mặc định được gán riêng.</span><span class="sxs-lookup"><span data-stu-id="f7829-145">The resource has either an individually defined utilization target or has a default role assigned to it.</span></span> <span data-ttu-id="f7829-146">Vai trò này có một thời gian làm việc mục được xác định riêng.</span><span class="sxs-lookup"><span data-stu-id="f7829-146">The role has a utilization target defined for it.</span></span>
- <span data-ttu-id="f7829-147">Các thực tế có một loại thanh toán **Có thể tính phí** cho khoảng thời gian mà bạn dự kiến tính toán thời gian làm việc.</span><span class="sxs-lookup"><span data-stu-id="f7829-147">Actuals have a billing type of **Chargeable** for the period you are expecting a utilization calculation for.</span></span> <span data-ttu-id="f7829-148">Kiểm tra các mục sau đây nếu thấy các thực tế có loại thanh toán khác với có thể tính phí:</span><span class="sxs-lookup"><span data-stu-id="f7829-148">Check the following if you are seeing actuals with billing types other than chargeable:</span></span>

  - <span data-ttu-id="f7829-149">Vai trò được sử dụng trên thực tế có một loại thanh toán mặc định khác có thể tính phí.</span><span class="sxs-lookup"><span data-stu-id="f7829-149">The role used on the actual has a default billing type of something other than chargeable.</span></span>
  - <span data-ttu-id="f7829-150">Vai trò trên mô tả hợp đồng hỗ trợ dự án đã được đặt thành không thể tính phí.</span><span class="sxs-lookup"><span data-stu-id="f7829-150">The role on the project contract line backing the project has been set to non-chargeable.</span></span>
  - <span data-ttu-id="f7829-151">Dự án không có mô tả hợp đồng được liên kết.</span><span class="sxs-lookup"><span data-stu-id="f7829-151">The project does not have an associated contract line.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]