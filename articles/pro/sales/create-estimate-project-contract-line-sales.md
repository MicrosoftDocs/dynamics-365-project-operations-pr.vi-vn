---
title: Số liệu ước tính cho phần mô tả hợp đồng dựa trên dự án - bản đơn giản
description: Chủ đề này cung cấp thông tin về cách đưa ra ước tính trong phần mô tả hợp đồng dựa trên dự án.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 186b982ee440576e10cf5b78922848b8877afd51
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273629"
---
# <a name="estimate-a-projectbased-contract-line---lite"></a><span data-ttu-id="d1467-103">Số liệu ước tính cho phần mô tả hợp đồng dựa trên dự án - bản đơn giản</span><span class="sxs-lookup"><span data-stu-id="d1467-103">Estimate a project–based contract line - lite</span></span>

<span data-ttu-id="d1467-104">_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="d1467-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d1467-105">Trong Dynamics 365 Project Operations, phần mô tả hợp đồng dựa trên dự án có các chi tiết giúp ước tính chi phí và doanh thu tiềm năng của công việc liên quan để cung cấp cho phần mô tả hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="d1467-105">In Dynamics 365 Project Operations, a project-based contract line has details that help estimate the cost and potential revenue of the work involved to deliver the contract line.</span></span>

<span data-ttu-id="d1467-106">Để đưa ra số liệu ước tính trong phần hợp đồng dựa trên dự án, hãy chuyển đến tab **Chi tiết mô tả hợp đồng** trong phần **Mô tả hợp đồng** dựa trên dự án.</span><span class="sxs-lookup"><span data-stu-id="d1467-106">To estimate a project-based contract line, go to the **Contract Line Detail** tab on the project-based **Contract Line**.</span></span>  <span data-ttu-id="d1467-107">Có 2 cách để tạo số liệu ước tính trong phần mô tả hợp đồng dựa trên dự án, đó là:</span><span class="sxs-lookup"><span data-stu-id="d1467-107">There are two ways to create an estimate on a project-based contract line:</span></span>

   - <span data-ttu-id="d1467-108">Tạo trực tiếp số liệu ước tính trên phần mô tả hợp đồng bằng cách thêm các chi tiết mô tả hợp đồng theo cách thủ công.</span><span class="sxs-lookup"><span data-stu-id="d1467-108">Create an estimate directly on the contract line by manually adding contract line details.</span></span>
   - <span data-ttu-id="d1467-109">Tạo một dự án và một kế hoạch dự án, sau đó liên kết dự án đó và các nhiệm vụ với phần mô tả hợp đồng của dự án.</span><span class="sxs-lookup"><span data-stu-id="d1467-109">Create a project and a project plan, and then associate the project and tasks to the project's contract line.</span></span> <span data-ttu-id="d1467-110">Thao tác này kích hoạt quy trình để bạn nhập số liệu ước tính của kế hoạch dự án vào phần mô tả hợp đồng dựa trên các thành phần có trong phần mô tả hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="d1467-110">This enables the process by which you can import the project plan estimate into the contract line based on the components included on the contract line.</span></span>

## <a name="create-an-estimation-directly-on-a-projectbased-contract-line"></a><span data-ttu-id="d1467-111">Tạo trực tiếp số liệu ước tính trong phần mô tả hợp đồng dựa trên dự án</span><span class="sxs-lookup"><span data-stu-id="d1467-111">Create an estimation directly on a project–based contract line</span></span>

1. <span data-ttu-id="d1467-112">Chuyển đến phần mô tả hợp đồng và chọn tab **Chi tiết mô tả hợp đồng**. Các dòng bạn tạo trên tab này được tóm tắt và hiển thị dưới dạng **Giá trị hợp đồng** cho phần **Mô tả hợp đồng** này.</span><span class="sxs-lookup"><span data-stu-id="d1467-112">Go to the contract line and select the **Contract Line Detail** tab. The lines you create on this tab are summarized and display as the **Contracted Value** for this **Contract Line**.</span></span> 
2. <span data-ttu-id="d1467-113">Trên lưới con **Chi tiết mô tả hợp đồng**, hãy chọn **+ Chi tiết mô tả hợp đồng mới**.</span><span class="sxs-lookup"><span data-stu-id="d1467-113">In the **Contract Line Details** subgrid, select **+ New Contract Line Detail**.</span></span> <span data-ttu-id="d1467-114">Một thanh trượt tạo nhanh sẽ mở ra.</span><span class="sxs-lookup"><span data-stu-id="d1467-114">A quick-create slider opens.</span></span> <span data-ttu-id="d1467-115">Các trường sau có sẵn trên biểu mẫu **Chi tiết mô tả hợp đồng**:</span><span class="sxs-lookup"><span data-stu-id="d1467-115">The following fields are available on the **Contract Line Details** form:</span></span>

| <span data-ttu-id="d1467-116">Trường</span><span class="sxs-lookup"><span data-stu-id="d1467-116">Field</span></span> | <span data-ttu-id="d1467-117">Vị trí</span><span class="sxs-lookup"><span data-stu-id="d1467-117">Location</span></span> | <span data-ttu-id="d1467-118">Nội dung mô tả</span><span class="sxs-lookup"><span data-stu-id="d1467-118">Description</span></span> | <span data-ttu-id="d1467-119">Tác động xuôi tuyến</span><span class="sxs-lookup"><span data-stu-id="d1467-119">Downstream impact</span></span> |
| --- | --- | --- | --- |
| <span data-ttu-id="d1467-120">**Mô tả**</span><span class="sxs-lookup"><span data-stu-id="d1467-120">**Description**</span></span> | <span data-ttu-id="d1467-121">**Tạo nhanh**</span><span class="sxs-lookup"><span data-stu-id="d1467-121">**Quick Create**</span></span> | <span data-ttu-id="d1467-122">Mô tả ước tính cụ thể.</span><span class="sxs-lookup"><span data-stu-id="d1467-122">A description of the specific estimate.</span></span> | <span data-ttu-id="d1467-123">Trường này mặc định sẽ là thông tin chi tiết mô tả hợp đồng liên quan cho các chi phí được tạo tự động.</span><span class="sxs-lookup"><span data-stu-id="d1467-123">This field defaults to the related contract line detail for costs that are automatically created.</span></span> |
| <span data-ttu-id="d1467-124">**Lớp giao dịch**</span><span class="sxs-lookup"><span data-stu-id="d1467-124">**Transaction Class**</span></span> | <span data-ttu-id="d1467-125">**Tạo nhanh**</span><span class="sxs-lookup"><span data-stu-id="d1467-125">**Quick Create**</span></span> | <span data-ttu-id="d1467-126">Trình đơn thả xuống này là danh sách các lớp giao dịch có trong tab **Chung** của phần mô tả hợp đồng dựa trên dự án.</span><span class="sxs-lookup"><span data-stu-id="d1467-126">This drop-down is a list of transaction classes included on the **General** tab of the project-based contract line.</span></span> | <span data-ttu-id="d1467-127">Trường này mặc định sẽ là thông tin chi tiết mô tả hợp đồng liên quan cho các chi phí được tạo tự động.</span><span class="sxs-lookup"><span data-stu-id="d1467-127">This field defaults to the related contract line detail for costs that are automatically created.</span></span> |
| <span data-ttu-id="d1467-128">**Vai trò**</span><span class="sxs-lookup"><span data-stu-id="d1467-128">**Role**</span></span> | <span data-ttu-id="d1467-129">**Tạo nhanh**</span><span class="sxs-lookup"><span data-stu-id="d1467-129">**Quick Create**</span></span> | <span data-ttu-id="d1467-130">Vai trò của người đang thực hiện công việc này hoặc chịu chi phí này.</span><span class="sxs-lookup"><span data-stu-id="d1467-130">The role of the person who is performing this work or incurring this expense.</span></span> | <span data-ttu-id="d1467-131">Trường này mặc định sẽ là thông tin chi tiết mô tả hợp đồng liên quan cho các chi phí được tạo tự động.</span><span class="sxs-lookup"><span data-stu-id="d1467-131">This field defaults to the related contract line detail for costs that are automatically created.</span></span> |
| <span data-ttu-id="d1467-132">**Danh mục**</span><span class="sxs-lookup"><span data-stu-id="d1467-132">**Category**</span></span> | <span data-ttu-id="d1467-133">**Tạo nhanh**</span><span class="sxs-lookup"><span data-stu-id="d1467-133">**Quick Create**</span></span> | <span data-ttu-id="d1467-134">Thể loại của công việc hoặc chi phí.</span><span class="sxs-lookup"><span data-stu-id="d1467-134">The category of the work or expense.</span></span> | <span data-ttu-id="d1467-135">Trường này mặc định sẽ là thông tin chi tiết mô tả hợp đồng liên quan cho các chi phí được tạo tự động.</span><span class="sxs-lookup"><span data-stu-id="d1467-135">This field defaults to the related contract line detail for costs that are automatically created.</span></span> |
| <span data-ttu-id="d1467-136">**Ngày bắt đầu**</span><span class="sxs-lookup"><span data-stu-id="d1467-136">**Start Date**</span></span> | <span data-ttu-id="d1467-137">**Tạo nhanh**</span><span class="sxs-lookup"><span data-stu-id="d1467-137">**Quick Create**</span></span> | <span data-ttu-id="d1467-138">Ngày bắt đầu công việc.</span><span class="sxs-lookup"><span data-stu-id="d1467-138">The start date of the work.</span></span> | <span data-ttu-id="d1467-139">Trường này mặc định sẽ là thông tin chi tiết mô tả hợp đồng liên quan cho các chi phí được tạo tự động.</span><span class="sxs-lookup"><span data-stu-id="d1467-139">This field defaults to the related contract line detail for costs that are automatically created.</span></span> |
| <span data-ttu-id="d1467-140">**Ngày kết thúc**</span><span class="sxs-lookup"><span data-stu-id="d1467-140">**End Date**</span></span> | <span data-ttu-id="d1467-141">**Tạo nhanh**</span><span class="sxs-lookup"><span data-stu-id="d1467-141">**Quick Create**</span></span> | <span data-ttu-id="d1467-142">Ngày kết thúc công việc.</span><span class="sxs-lookup"><span data-stu-id="d1467-142">The end date of the work.</span></span> | <span data-ttu-id="d1467-143">Trường này mặc định sẽ là thông tin chi tiết mô tả hợp đồng liên quan cho chi phí được tạo tự động.</span><span class="sxs-lookup"><span data-stu-id="d1467-143">This field defaults to the related contract line detail for the cost that is automatically created.</span></span> |
| <span data-ttu-id="d1467-144">**Đơn vị Nguồn lực**</span><span class="sxs-lookup"><span data-stu-id="d1467-144">**Resourcing Unit**</span></span> | <span data-ttu-id="d1467-145">**Tạo nhanh**</span><span class="sxs-lookup"><span data-stu-id="d1467-145">**Quick Create**</span></span> | <span data-ttu-id="d1467-146">Đơn vị cung ứng nguồn lực chịu chi phí này và cung cấp nguồn lực để thực hiện.</span><span class="sxs-lookup"><span data-stu-id="d1467-146">The resourcing unit that incurs this cost and provies the resource to work on it.</span></span> | <span data-ttu-id="d1467-147">Trường này mặc định sẽ là thông tin chi tiết mô tả hợp đồng liên quan cho các chi phí được tạo tự động.</span><span class="sxs-lookup"><span data-stu-id="d1467-147">This field defaults to the related contract line detail for costs that are automatically created.</span></span> <span data-ttu-id="d1467-148">Trường này cũng được sử dụng trong truy xuất giá vốn.</span><span class="sxs-lookup"><span data-stu-id="d1467-148">This field is also used in cost price retrieval.</span></span> |
| <span data-ttu-id="d1467-149">**Lịch trình đơn vị**</span><span class="sxs-lookup"><span data-stu-id="d1467-149">**Unit schedule**</span></span> | <span data-ttu-id="d1467-150">**Tạo nhanh**</span><span class="sxs-lookup"><span data-stu-id="d1467-150">**Quick create**</span></span> | <span data-ttu-id="d1467-151">Nhóm đơn vị đo của công việc hoặc chi phí.</span><span class="sxs-lookup"><span data-stu-id="d1467-151">The unit group of the work or expense.</span></span> <span data-ttu-id="d1467-152">Các đơn vị thuộc một lịch trình đơn vị hoặc một nhóm đơn vị.</span><span class="sxs-lookup"><span data-stu-id="d1467-152">Units belong to a unit schedule or a group of units.</span></span> <span data-ttu-id="d1467-153">Ví dụ: *dặm* và *ki lô mét (km)* là các đơn vị thuộc nhóm đơn vị mô tả khoảng cách.</span><span class="sxs-lookup"><span data-stu-id="d1467-153">For example, *miles* and *kilometers (Kms)* are units that belong to a group of units that describe distance.</span></span> | <span data-ttu-id="d1467-154">Trường này mặc định sẽ là thông tin chi tiết mô tả hợp đồng liên quan cho các chi phí được tạo tự động.</span><span class="sxs-lookup"><span data-stu-id="d1467-154">This field defaults to the related contract line detail for costs that are automatically created.</span></span> |
| <span data-ttu-id="d1467-155">**Đơn vị**</span><span class="sxs-lookup"><span data-stu-id="d1467-155">**Unit**</span></span> | <span data-ttu-id="d1467-156">**Tạo nhanh**</span><span class="sxs-lookup"><span data-stu-id="d1467-156">**Quick Create**</span></span> | <span data-ttu-id="d1467-157">Đơn vị đo lường công việc hoặc chi phí.</span><span class="sxs-lookup"><span data-stu-id="d1467-157">The unit of work or expense.</span></span> | <span data-ttu-id="d1467-158">Trường này mặc định sẽ là thông tin chi tiết mô tả hợp đồng liên quan cho các chi phí được tạo tự động.</span><span class="sxs-lookup"><span data-stu-id="d1467-158">This field defaults to the related contract line detail for costs that are automatically created.</span></span> |
| <span data-ttu-id="d1467-159">**Số lượng**</span><span class="sxs-lookup"><span data-stu-id="d1467-159">**Quantity**</span></span> | <span data-ttu-id="d1467-160">**Tạo nhanh**</span><span class="sxs-lookup"><span data-stu-id="d1467-160">**Quick Create**</span></span> | <span data-ttu-id="d1467-161">Số lượng công việc hoặc chi phí.</span><span class="sxs-lookup"><span data-stu-id="d1467-161">The quantity of work or expense.</span></span> | <span data-ttu-id="d1467-162">Trường này mặc định sẽ là thông tin chi tiết mô tả hợp đồng liên quan cho các chi phí được tạo tự động.</span><span class="sxs-lookup"><span data-stu-id="d1467-162">This field defaults to the related contract line detail for costs that are automatically created.</span></span> |
| <span data-ttu-id="d1467-163">**Giá đơn vị**</span><span class="sxs-lookup"><span data-stu-id="d1467-163">**Unit price**</span></span> | <span data-ttu-id="d1467-164">**Tạo nhanh**</span><span class="sxs-lookup"><span data-stu-id="d1467-164">**Quick Create**</span></span> | <span data-ttu-id="d1467-165">Tỷ lệ thanh toán của vai trò đang thực hiện công việc hoặc giá bán của loại chi phí.</span><span class="sxs-lookup"><span data-stu-id="d1467-165">The bill rate of the role that is performing the work or the sales price of the expense category.</span></span> <span data-ttu-id="d1467-166">Trường này lấy giá trị mặc định cho **Thời gian** dựa theo tổ hợp vai trò và đơn vị cung ứng nguồn lực trên bảng giá dự án có hiệu lực vào ngày bắt đầu.</span><span class="sxs-lookup"><span data-stu-id="d1467-166">This field defaults for **Time** based on the role and resourcing unit combination on the project price list that is effective for the start date.</span></span> <span data-ttu-id="d1467-167">Đối với chi phí, giá trị mặc định của trường này chính là mức giá thiết lập cho thể loại giao dịch trong bảng giá dự án có hiệu lực vào ngày bắt đầu.</span><span class="sxs-lookup"><span data-stu-id="d1467-167">For expenses, this field's default is from the price setup for the transaction category in the project price list that is effective for the start date.</span></span> <span data-ttu-id="d1467-168">Nếu phương thức tính giá cho thể loại giao dịch không phải là **đơn giá**, thì không có giá trị mặc định và trường này được để trống.</span><span class="sxs-lookup"><span data-stu-id="d1467-168">If the pricing method for the transaction category is not **price-per-unit**, there is no default, and this field is left blank.</span></span> | <span data-ttu-id="d1467-169">Tỷ lệ chi phí của vai trò đang thực hiện công việc hoặc đơn giá của thể loại chi phí.</span><span class="sxs-lookup"><span data-stu-id="d1467-169">The cost rate of the role that is performing the work, or the cost per unit of the expense category.</span></span> <span data-ttu-id="d1467-170">Trường này lấy giá trị mặc định cho **Thời gian dựa theo tổ hợp vai trò** và đơn vị cung ứng nguồn lực trên dòng mô tả giá theo vai trò của bảng giá vốn được đính kèm với đơn vị ký hợp đồng có hiệu lực vào ngày bắt đầu.</span><span class="sxs-lookup"><span data-stu-id="d1467-170">This field defaults for **Time based on the role** and the resourcing unit combination on the role price line of the cost price list attached to the contracting unit effective for the start date.</span></span> <span data-ttu-id="d1467-171">Đối với chi phí, giá trị mặc định của trường này dựa trên dòng mô tả mức giá theo thể loại của bảng giá vốn được đính kèm với đơn vị ký hợp đồng có hiệu lực vào ngày bắt đầu.</span><span class="sxs-lookup"><span data-stu-id="d1467-171">For expenses, this field's default is based on the category price line of the cost price list attached to the contracting unit that is effective for the start date.</span></span> <span data-ttu-id="d1467-172">Nếu phương thức tính giá cho danh mục giao dịch không phải là giá mỗi đơn vị, thì không có giá trị mặc định và trường này được để trống.</span><span class="sxs-lookup"><span data-stu-id="d1467-172">If the pricing method for the transaction category is not price-per-unit, there is no default and this field is left blank.</span></span> |
| <span data-ttu-id="d1467-173">**Thuế Ước tính**</span><span class="sxs-lookup"><span data-stu-id="d1467-173">**Estimated Tax**</span></span> | <span data-ttu-id="d1467-174">**Tạo nhanh**</span><span class="sxs-lookup"><span data-stu-id="d1467-174">**Quick Create**</span></span> | <span data-ttu-id="d1467-175">Thuế ước tính cho công việc hoặc chi phí này do người dùng nhập.</span><span class="sxs-lookup"><span data-stu-id="d1467-175">The estimated tax for this work or expense as input by the user.</span></span> | <span data-ttu-id="d1467-176">Thuế ước tính cho công việc hoặc chi phí này do người dùng nhập.</span><span class="sxs-lookup"><span data-stu-id="d1467-176">The estimated tax for this work or expense as input by the user.</span></span> |
| <span data-ttu-id="d1467-177">**Số lượng**</span><span class="sxs-lookup"><span data-stu-id="d1467-177">**Amount**</span></span> | <span data-ttu-id="d1467-178">**Tạo nhanh**</span><span class="sxs-lookup"><span data-stu-id="d1467-178">**Quick Create**</span></span> | <span data-ttu-id="d1467-179">Giá trị trong trường này có thể do người dùng thêm nếu các trường **Số lượng** và **Giá** được để trống.</span><span class="sxs-lookup"><span data-stu-id="d1467-179">This value in this field can be added by the user if the **Quantity** and **Price** fields are left blank.</span></span> <span data-ttu-id="d1467-180">Nếu **Số lượng** và **Giá** đã được điền, thì trường **Số tiền** là trường chỉ đọc và được tính là **(Số lượng \* Đơn giá) + Thuế**.</span><span class="sxs-lookup"><span data-stu-id="d1467-180">If **Quantity** and **Price** are filled, the **Amount** field is read-only and is calculated as **(Quantity \* Unit price) + Tax**.</span></span> | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a><span data-ttu-id="d1467-181">Cập nhật giá trên chi tiết mô tả hợp đồng</span><span class="sxs-lookup"><span data-stu-id="d1467-181">Update prices on contract line details</span></span>

<span data-ttu-id="d1467-182">Nếu thay đổi các mức giá trên bảng giá dự án được đính kèm với hợp đồng hoặc bảng giá vốn của đơn vị ký hợp đồng, bạn có thể làm mới các mức giá cho từng chi tiết mô tả hợp đồng để phản ánh sự thay đổi.</span><span class="sxs-lookup"><span data-stu-id="d1467-182">If you change prices on the project price list that is attached to the contract or the cost price list of the contracting unit, you can refresh the prices on the individual contract line details to reflect the change.</span></span> <span data-ttu-id="d1467-183">Trên trang **Hợp đồng**, chọn **Tính toán lại**.</span><span class="sxs-lookup"><span data-stu-id="d1467-183">On the **Contract** page, select **Recalculate**.</span></span> <span data-ttu-id="d1467-184">Một cảnh báo sẽ mở ra để thông báo cho bạn biết rằng mức giá của tất cả các dòng mô tả hợp đồng trên hợp đồng này đã được đặt lại.</span><span class="sxs-lookup"><span data-stu-id="d1467-184">A warning opens to inform you that prices for all contract lines on this contract are reset.</span></span> <span data-ttu-id="d1467-185">Chọn **Có** để làm mới giá cho cả chi tiết mô tả hợp đồng bán hàng và chi phí.</span><span class="sxs-lookup"><span data-stu-id="d1467-185">Select **Yes** to refresh prices for both sales and cost contract line details.</span></span>

## <a name="access-contract-line-details-for-cost"></a><span data-ttu-id="d1467-186">Truy cập vào chi tiết mô tả hợp đồng để biết chi phí</span><span class="sxs-lookup"><span data-stu-id="d1467-186">Access contract line details for cost</span></span>

<span data-ttu-id="d1467-187">Trên tab **Chi tiết mô tả hợp đồng**, chọn một hàng trong lưới để hiển thị các tác vụ trên thanh công cụ của lưới con.</span><span class="sxs-lookup"><span data-stu-id="d1467-187">On the **Contract Line Details** tab, select a row in the grid to display actions on the toolbar of the subgrid.</span></span> <span data-ttu-id="d1467-188">Tác vụ đầu tiên trên thanh công cụ của lưới con là **Mở chi tiết chi phí**.</span><span class="sxs-lookup"><span data-stu-id="d1467-188">The first action on the subgrid tool bar is **Open Cost Detail**.</span></span> <span data-ttu-id="d1467-189">Để xem tỷ lệ chi phí liên quan và số tiền có trong chi tiết mô tả hợp đồng, chọn **Mở chi tiết chi phí**.</span><span class="sxs-lookup"><span data-stu-id="d1467-189">To see the related cost rate and amount for this contract line detail, select **Open Cost Detail**.</span></span> 

> [!NOTE]
> <span data-ttu-id="d1467-190">Việc thay đổi công ty cung ứng nguồn lực, đơn vị cung ứng nguồn lực, số lượng, ngày tháng, vai trò hoặc giá trị thể loại trên chi tiết mô tả **Chi phí** của hợp đồng cũng sẽ làm thay đổi các giá trị tương ứng trên chi tiết mô tả **Doanh thu** của hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="d1467-190">Changing the resourcing company, resourcing unit, quantity, dates, role, or category values on the contract line detail for **Cost** also changes the corresponding values on the contract line detail for **Sales**.</span></span>

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a><span data-ttu-id="d1467-191">Đơn vị tiền tệ trên các chi tiết mô tả chi phí và doanh thu của hợp đồng</span><span class="sxs-lookup"><span data-stu-id="d1467-191">Currency on contract line details for cost and sales</span></span>

<span data-ttu-id="d1467-192">Chi tiết mô tả **Doanh thu** của hợp đồng lấy đơn vị tiền tệ của bảng giá dự án có hiệu lực vào ngày bắt đầu của chi tiết mô tả hợp đồng làm đơn vị tiền tệ mặc định.</span><span class="sxs-lookup"><span data-stu-id="d1467-192">The contract line detail for **Sales** sets the default currency from the project price list that is effective for the start date of the contract line detail.</span></span>

<span data-ttu-id="d1467-193">Chi tiết mô tả **Chi phí** của hợp đồng lấy đơn vị tiền tệ từ bảng giá của đơn vị ký kết hợp đồng có hiệu lực vào ngày bắt đầu của chi tiết mô tả **Chi phí** của hợp đồng làm đơn vị tiền tệ mặc định.</span><span class="sxs-lookup"><span data-stu-id="d1467-193">The contract line detail for **Cost** sets the default currency from the price list of the contracting unit of the contract that is effective for the start date of the contract line detail for **Cost**.</span></span>

<span data-ttu-id="d1467-194">Các tính toán lợi nhuận chuyển đổi số tiền trong chi tiết mô tả **Chi phí** và **Doanh thu** của hợp đồng sang đơn vị tiền tệ cơ sở của môi trường để báo cáo tổng lợi nhuận thực tế và ước tính trên hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="d1467-194">Profitability calculations convert the amounts for the contract line details for **Cost** and **Sales** into the base currency of the environment to report the overall actual and estimated margins on the contract.</span></span>

> [!NOTE]
> <span data-ttu-id="d1467-195">Lỗi làm tròn theo đơn vị tiền tệ và thay đổi lợi nhuận có thể xảy ra do thiếu tỷ giá hối đoái thực tế theo ngày.</span><span class="sxs-lookup"><span data-stu-id="d1467-195">Currency rounding errors and changed margins could occur because of the lack of date effective exchange rates.</span></span> <span data-ttu-id="d1467-196">Chỉ sử dụng các tính toán trên những hợp đồng dự án này dưới dạng ước lượng và không áp dụng cho các báo cáo thực tế theo luật định hoặc các báo cáo khác đòi hỏi độ chính xác cao hơn liên quan đến việc làm tròn và tỷ giá hối đoái thực tế theo ngày.</span><span class="sxs-lookup"><span data-stu-id="d1467-196">Use these calculations on project contracts only as approximations and not for actual statutory or other reporting that requires higher precision of rounding and awareness of date effectivity for exchange rates.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]