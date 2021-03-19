---
title: Thực tế
description: Chủ đề này cung cấp thông tin về cách làm việc với giá trị thực tế trong Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 6a94bd143b0d0dad2a08511a34e592a057b6d2a1
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291825"
---
# <a name="actuals"></a><span data-ttu-id="3a1a0-103">Thực tế</span><span class="sxs-lookup"><span data-stu-id="3a1a0-103">Actuals</span></span> 

<span data-ttu-id="3a1a0-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_</span><span class="sxs-lookup"><span data-stu-id="3a1a0-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="3a1a0-105">Thực tế là lượng công việc đã hoàn thành trên một dự án.</span><span class="sxs-lookup"><span data-stu-id="3a1a0-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="3a1a0-106">Chúng được tạo ra do kết quả của mục nhập thời gian và chi phí, bút toán và hóa đơn.</span><span class="sxs-lookup"><span data-stu-id="3a1a0-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="3a1a0-107">Dòng nhật ký kế toán và thời gian gửi</span><span class="sxs-lookup"><span data-stu-id="3a1a0-107">Journal lines and time submission</span></span>

<span data-ttu-id="3a1a0-108">Để biết thêm thông tin về mục nhập thời gian, hãy xem [Tổng quan về mục nhập thời gian](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3a1a0-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="3a1a0-109">Thời gian và vật tư</span><span class="sxs-lookup"><span data-stu-id="3a1a0-109">Time and materials</span></span>

<span data-ttu-id="3a1a0-110">Khi một mục nhập thời gian đã gửi được liên kết với một dự án ánh xạ tới mô tả hợp đồng thời gian và vật tư, hệ thống sẽ tạo ra hai dòng nhật ký kế toán, một dòng cho chi phí và một dòng cho doanh số chưa lập hóa đơn.</span><span class="sxs-lookup"><span data-stu-id="3a1a0-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="3a1a0-111">Giá cố định</span><span class="sxs-lookup"><span data-stu-id="3a1a0-111">Fixed price</span></span>

<span data-ttu-id="3a1a0-112">Khi một mục nhập thời gian được gửi được liên kết với một dự án được ánh xạ tới một mô tả hợp đồng giá cố định, thì hệ thống sẽ tạo ra một mô tả hợp đồng cho chi phí.</span><span class="sxs-lookup"><span data-stu-id="3a1a0-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="3a1a0-113">Giá mặc định</span><span class="sxs-lookup"><span data-stu-id="3a1a0-113">Default pricing</span></span>

<span data-ttu-id="3a1a0-114">Logic để tạo giá mặc định nằm trên dòng nhật ký kế toán.</span><span class="sxs-lookup"><span data-stu-id="3a1a0-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="3a1a0-115">Các giá trị trường từ mục nhập thời gian được sao chép vào dòng nhật ký kế toán.</span><span class="sxs-lookup"><span data-stu-id="3a1a0-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="3a1a0-116">Các giá trị này bao gồm ngày giao dịch, mô tả hợp đồng mà dự án được ánh xạ và kết quả tiền tệ trong bảng giá phù hợp.</span><span class="sxs-lookup"><span data-stu-id="3a1a0-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="3a1a0-117">Các trường ảnh hưởng đến giá mặc định, chẳng hạn như **Vai trò** và **Đơn vị tổ chức** được sử dụng để xác định giá thích hợp trên dòng nhật ký kế toán.</span><span class="sxs-lookup"><span data-stu-id="3a1a0-117">The fields that affect default pricing, such as **Role** and **Org Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="3a1a0-118">Bạn có thể thêm trường tùy chỉnh trên mục nhập thời gian.</span><span class="sxs-lookup"><span data-stu-id="3a1a0-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="3a1a0-119">Nếu bạn muốn điền giá trị trường vào giá trị thực tế, hãy tạo trường đó trên thực thể Thực tế và sử dụng ánh xạ trường để sao chép trường từ mục nhập thời gian tới giá trị thực tế.</span><span class="sxs-lookup"><span data-stu-id="3a1a0-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="3a1a0-120">Các dòng nhật ký kế toán và nộp chi phí cơ bản</span><span class="sxs-lookup"><span data-stu-id="3a1a0-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="3a1a0-121">Để biết thêm thông tin về mục nhập chi phí, hãy xem [Tổng quan về chi phí](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3a1a0-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="3a1a0-122">Thời gian và vật tư</span><span class="sxs-lookup"><span data-stu-id="3a1a0-122">Time and materials</span></span>

<span data-ttu-id="3a1a0-123">Khi một mục nhập chi phí cơ bản đã gửi đi được liên kết với một dự án ánh xạ tới mô tả hợp đồng thời gian và vật tư, hệ thống sẽ tạo ra hai dòng nhật ký kế toán, một dòng cho chi phí và một dòng cho doanh số chưa lập hóa đơn.</span><span class="sxs-lookup"><span data-stu-id="3a1a0-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="3a1a0-124">Giá cố định</span><span class="sxs-lookup"><span data-stu-id="3a1a0-124">Fixed price</span></span>

<span data-ttu-id="3a1a0-125">Khi một mục nhập chi phí cơ bản được gửi được liên kết với một dự án được ánh xạ tới một mô tả hợp đồng giá cố định, thì hệ thống sẽ tạo ra một dòng nhật ký kế toán cho chi phí.</span><span class="sxs-lookup"><span data-stu-id="3a1a0-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="3a1a0-126">Giá mặc định</span><span class="sxs-lookup"><span data-stu-id="3a1a0-126">Default pricing</span></span>

<span data-ttu-id="3a1a0-127">Logic để nhập giá mặc định cho các chi phí dựa trên danh mục chi phí.</span><span class="sxs-lookup"><span data-stu-id="3a1a0-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="3a1a0-128">Ngày giao dịch, dòng hợp đồng mà dự án được ánh xạ tới và tiền tệ được dùng để xác định bảng giá phù hợp.</span><span class="sxs-lookup"><span data-stu-id="3a1a0-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="3a1a0-129">Tuy nhiên, theo mặc định, số tiền mà người dùng nhập cho giá được đặt trực tiếp trên dòng nhật ký kế toán chi phí liên quan cho chi phí và bán hàng.</span><span class="sxs-lookup"><span data-stu-id="3a1a0-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="3a1a0-130">Mục nhập dựa trên danh mục của giá mặc định cho mỗi đơn vị trên các mục nhập chi phí không khả dụng.</span><span class="sxs-lookup"><span data-stu-id="3a1a0-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="3a1a0-131">Sử dụng bút toán để ghi lại chi phí</span><span class="sxs-lookup"><span data-stu-id="3a1a0-131">Use entry journals to record costs</span></span>

<span data-ttu-id="3a1a0-132">Bạn có thể sử dụng bút toán để ghi lại chi phí hoặc doanh thu trong lớp giao dịch thuế, chi phí, thời gian, phí hoặc vật tư.</span><span class="sxs-lookup"><span data-stu-id="3a1a0-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="3a1a0-133">Có thể sử dụng nhật ký cho các mục đích sau:</span><span class="sxs-lookup"><span data-stu-id="3a1a0-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="3a1a0-134">Ghi lại chi phí vật tư thực tế và bán hàng trên một dự án.</span><span class="sxs-lookup"><span data-stu-id="3a1a0-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="3a1a0-135">Di chuyển các giá trị thực tế của giao dịch từ một hệ thống khác sang Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="3a1a0-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="3a1a0-136">Ghi lại chi phí đã xảy ra trong hệ thống khác.</span><span class="sxs-lookup"><span data-stu-id="3a1a0-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="3a1a0-137">Các chi phí này có thể bao gồm chi phí mua sắm hoặc chi phí thầu phụ.</span><span class="sxs-lookup"><span data-stu-id="3a1a0-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3a1a0-138">Ứng dụng không xác nhận dòng nhật ký kế toán hoặc giá cả liên quan được nhập trên dòng nhật ký kế toán.</span><span class="sxs-lookup"><span data-stu-id="3a1a0-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="3a1a0-139">Do đó, chỉ người dùng có nhận thức đầy đủ về tác động kế toán mà các giá trị thực tế có đối với dự án mới được sử dụng bút toán để tạo các giá trị thực tế.</span><span class="sxs-lookup"><span data-stu-id="3a1a0-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="3a1a0-140">Do tác động của loại nhật ký này, bạn nên cẩn thận chọn người có quyền truy cập để tạo bút toán.</span><span class="sxs-lookup"><span data-stu-id="3a1a0-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="3a1a0-141">Ghi lại thực tế dựa trên sự kiện dự án</span><span class="sxs-lookup"><span data-stu-id="3a1a0-141">Record actuals based on project events</span></span>

<span data-ttu-id="3a1a0-142">Project Operations ghi lại các giao dịch tài chính xảy ra trong một dự án.</span><span class="sxs-lookup"><span data-stu-id="3a1a0-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="3a1a0-143">Các giao dịch này được ghi lại là thực tế.</span><span class="sxs-lookup"><span data-stu-id="3a1a0-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="3a1a0-144">Các bảng sau đây hiển thị các loại thực tế khác nhau được tạo, phụ thuộc vào việc dự án là dự án thời gian và vật tư hay giá cố định, ở giai đoạn trước khi bán hàng hay là dự án nội bộ.</span><span class="sxs-lookup"><span data-stu-id="3a1a0-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="3a1a0-145">Tài nguyên thuộc về cùng một đơn vị tổ chức như đơn vị hợp đồng của dự án</span><span class="sxs-lookup"><span data-stu-id="3a1a0-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="3a1a0-146">Sự kiện</span><span class="sxs-lookup"><span data-stu-id="3a1a0-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="3a1a0-147">Dự án có thể lập hóa đơn hoặc đã bán</span><span class="sxs-lookup"><span data-stu-id="3a1a0-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="3a1a0-148">Dự án trong giai đoạn trước khi bán</span><span class="sxs-lookup"><span data-stu-id="3a1a0-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="3a1a0-149">Dự án nội bộ</span><span class="sxs-lookup"><span data-stu-id="3a1a0-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="3a1a0-150">Thời gian và vật tư</span><span class="sxs-lookup"><span data-stu-id="3a1a0-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="3a1a0-151">Giá cố định</span><span class="sxs-lookup"><span data-stu-id="3a1a0-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="3a1a0-152">Thực tế</span><span class="sxs-lookup"><span data-stu-id="3a1a0-152">Actuals</span></span></th>
<th><span data-ttu-id="3a1a0-153">Loại tiền giao dịch</span><span class="sxs-lookup"><span data-stu-id="3a1a0-153">Transaction currency</span></span></th>
<th><span data-ttu-id="3a1a0-154">Giá cố định</span><span class="sxs-lookup"><span data-stu-id="3a1a0-154">Fixed price</span></span></th>
<th><span data-ttu-id="3a1a0-155">Loại tiền giao dịch</span><span class="sxs-lookup"><span data-stu-id="3a1a0-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3a1a0-156">Mục nhập thời gian được tạo.</span><span class="sxs-lookup"><span data-stu-id="3a1a0-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="3a1a0-157">Không có hoạt động trong thực thể Thực tế</span><span class="sxs-lookup"><span data-stu-id="3a1a0-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3a1a0-158">Mục nhập thời gian được gửi.</span><span class="sxs-lookup"><span data-stu-id="3a1a0-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="3a1a0-159">Không có hoạt động trong thực thể Thực tế</span><span class="sxs-lookup"><span data-stu-id="3a1a0-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="3a1a0-160">Thời gian được phê duyệt và số giờ có thể lập hóa đơn sẽ không thay đổi hay tăng trong quá trình phê duyệt.</span><span class="sxs-lookup"><span data-stu-id="3a1a0-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="3a1a0-161">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="3a1a0-161">Cost actual</span></span></td>
<td><span data-ttu-id="3a1a0-162">Tiền tệ của đơn vị hợp đồng</span><span class="sxs-lookup"><span data-stu-id="3a1a0-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="3a1a0-163">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="3a1a0-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="3a1a0-164">Tiền tệ của đơn vị hợp đồng</span><span class="sxs-lookup"><span data-stu-id="3a1a0-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="3a1a0-165">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="3a1a0-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="3a1a0-166">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="3a1a0-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3a1a0-167">Thực tế bán hàng chưa lập hóa đơn – Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="3a1a0-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="3a1a0-168">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3a1a0-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="3a1a0-169">Thời gian được phê duyệt và số giờ có thể lập hóa đơn giảm trong quá trình phê duyệt.</span><span class="sxs-lookup"><span data-stu-id="3a1a0-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="3a1a0-170">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="3a1a0-170">Cost actual</span></span></td>
<td><span data-ttu-id="3a1a0-171">Tiền tệ của đơn vị hợp đồng</span><span class="sxs-lookup"><span data-stu-id="3a1a0-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="3a1a0-172">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="3a1a0-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="3a1a0-173">Tiền tệ của đơn vị hợp đồng</span><span class="sxs-lookup"><span data-stu-id="3a1a0-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="3a1a0-174">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="3a1a0-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="3a1a0-175">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="3a1a0-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3a1a0-176">Thực tế bán hàng chưa lập hóa đơn – Có thể tính phí cho số lượng mới</span><span class="sxs-lookup"><span data-stu-id="3a1a0-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="3a1a0-177">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3a1a0-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3a1a0-178">Thực tế bán hàng chưa lập hóa đơn – Không thể tính phí cho phần chênh lệch</span><span class="sxs-lookup"><span data-stu-id="3a1a0-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="3a1a0-179">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3a1a0-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="3a1a0-180">Hóa đơn được xác nhận, số giờ có thể lập hóa đơn sẽ không thay đổi hay tăng.</span><span class="sxs-lookup"><span data-stu-id="3a1a0-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="3a1a0-181">Đảo ngược bán hàng chưa lập hóa đơn</span><span class="sxs-lookup"><span data-stu-id="3a1a0-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="3a1a0-182">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3a1a0-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="3a1a0-183">Doanh số đã lập hóa đơn cho mốc quan trọng</span><span class="sxs-lookup"><span data-stu-id="3a1a0-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="3a1a0-184">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3a1a0-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="3a1a0-185">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="3a1a0-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="3a1a0-186">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="3a1a0-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3a1a0-187">Doanh số đã lập hóa đơn</span><span class="sxs-lookup"><span data-stu-id="3a1a0-187">Billed sales</span></span></td>
<td><span data-ttu-id="3a1a0-188">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3a1a0-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="3a1a0-189">Hóa đơn được xác nhận, số giờ có thể lập hóa đơn giảm.</span><span class="sxs-lookup"><span data-stu-id="3a1a0-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="3a1a0-190">Đảo ngược bán hàng chưa lập hóa đơn</span><span class="sxs-lookup"><span data-stu-id="3a1a0-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="3a1a0-191">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3a1a0-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="3a1a0-192">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="3a1a0-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="3a1a0-193">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="3a1a0-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="3a1a0-194">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="3a1a0-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="3a1a0-195">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="3a1a0-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3a1a0-196">Doanh số chưa lập hóa đơn – Có thể tính phí cho số lượng mới</span><span class="sxs-lookup"><span data-stu-id="3a1a0-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="3a1a0-197">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3a1a0-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3a1a0-198">Doanh số chưa lập hóa đơn – Không thể tính phí cho phần chênh lệch</span><span class="sxs-lookup"><span data-stu-id="3a1a0-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="3a1a0-199">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3a1a0-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="3a1a0-200">Hóa đơn được sửa để tăng số lượng có thể tính phí.</span><span class="sxs-lookup"><span data-stu-id="3a1a0-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="3a1a0-201">Doanh số đã tính phí – Đảo ngược</span><span class="sxs-lookup"><span data-stu-id="3a1a0-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="3a1a0-202">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3a1a0-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="3a1a0-203">Đảo ngược doanh số đã lập hóa đơn cho mốc quan trọng</span><span class="sxs-lookup"><span data-stu-id="3a1a0-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="3a1a0-204">Thay đổi trạng thái mốc quan trọng từ <strong>Đã lập hóa đơn</strong> thành <strong>Sẵn sàng lập hóa đơn</strong></span><span class="sxs-lookup"><span data-stu-id="3a1a0-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="3a1a0-205">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3a1a0-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="3a1a0-206">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="3a1a0-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="3a1a0-207">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="3a1a0-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3a1a0-208">Doanh số đã lập hóa đơn</span><span class="sxs-lookup"><span data-stu-id="3a1a0-208">Billed sales</span></span></td>
<td><span data-ttu-id="3a1a0-209">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3a1a0-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="3a1a0-210">Hóa đơn được sửa để giảm số lượng có thể tính phí.</span><span class="sxs-lookup"><span data-stu-id="3a1a0-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="3a1a0-211">Doanh số đã tính phí – Đảo ngược</span><span class="sxs-lookup"><span data-stu-id="3a1a0-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="3a1a0-212">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3a1a0-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3a1a0-213">Doanh số chưa lập hóa đơn cho số lượng mới</span><span class="sxs-lookup"><span data-stu-id="3a1a0-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="3a1a0-214">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3a1a0-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3a1a0-215">Doanh số chưa lập hóa đơn – Có thể tính phí cho phần chênh lệch</span><span class="sxs-lookup"><span data-stu-id="3a1a0-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="3a1a0-216">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3a1a0-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="3a1a0-217">Tài nguyên thuộc về một đơn vị tổ chức khác với đơn vị hợp đồng của dự án</span><span class="sxs-lookup"><span data-stu-id="3a1a0-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="3a1a0-218">Sự kiện</span><span class="sxs-lookup"><span data-stu-id="3a1a0-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="3a1a0-219">Dự án có thể lập hóa đơn hoặc đã bán</span><span class="sxs-lookup"><span data-stu-id="3a1a0-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="3a1a0-220">Dự án trong giai đoạn trước khi bán</span><span class="sxs-lookup"><span data-stu-id="3a1a0-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="3a1a0-221">Dự án nội bộ</span><span class="sxs-lookup"><span data-stu-id="3a1a0-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="3a1a0-222">Thời gian và vật tư</span><span class="sxs-lookup"><span data-stu-id="3a1a0-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="3a1a0-223">Giá cố định</span><span class="sxs-lookup"><span data-stu-id="3a1a0-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="3a1a0-224">Thực tế</span><span class="sxs-lookup"><span data-stu-id="3a1a0-224">Actuals</span></span></th>
<th><span data-ttu-id="3a1a0-225">Loại tiền giao dịch</span><span class="sxs-lookup"><span data-stu-id="3a1a0-225">Transaction currency</span></span></th>
<th><span data-ttu-id="3a1a0-226">Giá cố định</span><span class="sxs-lookup"><span data-stu-id="3a1a0-226">Fixed price</span></span></th>
<th><span data-ttu-id="3a1a0-227">Loại tiền giao dịch</span><span class="sxs-lookup"><span data-stu-id="3a1a0-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3a1a0-228">Mục nhập thời gian được tạo.</span><span class="sxs-lookup"><span data-stu-id="3a1a0-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="3a1a0-229">Không có hoạt động trong thực thể Thực tế</span><span class="sxs-lookup"><span data-stu-id="3a1a0-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3a1a0-230">Mục nhập thời gian được gửi.</span><span class="sxs-lookup"><span data-stu-id="3a1a0-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="3a1a0-231">Không có hoạt động trong thực thể Thực tế</span><span class="sxs-lookup"><span data-stu-id="3a1a0-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="3a1a0-232">Thời gian được phê duyệt và số giờ có thể lập hóa đơn sẽ không thay đổi hay tăng trong quá trình phê duyệt.</span><span class="sxs-lookup"><span data-stu-id="3a1a0-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="3a1a0-233">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="3a1a0-233">Cost actual</span></span></td>
<td><span data-ttu-id="3a1a0-234">Tiền tệ của đơn vị hợp đồng</span><span class="sxs-lookup"><span data-stu-id="3a1a0-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="3a1a0-235">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="3a1a0-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="3a1a0-236">Tiền tệ của đơn vị hợp đồng</span><span class="sxs-lookup"><span data-stu-id="3a1a0-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="3a1a0-237">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="3a1a0-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="3a1a0-238">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="3a1a0-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3a1a0-239">Thực tế bán hàng chưa lập hóa đơn – Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="3a1a0-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="3a1a0-240">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3a1a0-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3a1a0-241">Chi phí đơn vị nguồn lực</span><span class="sxs-lookup"><span data-stu-id="3a1a0-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="3a1a0-242">Tiền tệ đơn vị nguồn lực</span><span class="sxs-lookup"><span data-stu-id="3a1a0-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3a1a0-243">Bán hàng liên tổ chức</span><span class="sxs-lookup"><span data-stu-id="3a1a0-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="3a1a0-244">Tiền tệ của đơn vị hợp đồng</span><span class="sxs-lookup"><span data-stu-id="3a1a0-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="3a1a0-245">Thời gian được phê duyệt và số giờ có thể lập hóa đơn giảm trong quá trình phê duyệt.</span><span class="sxs-lookup"><span data-stu-id="3a1a0-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="3a1a0-246">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="3a1a0-246">Cost actual</span></span></td>
<td><span data-ttu-id="3a1a0-247">Tiền tệ của đơn vị hợp đồng</span><span class="sxs-lookup"><span data-stu-id="3a1a0-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="3a1a0-248">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="3a1a0-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="3a1a0-249">Tiền tệ của đơn vị hợp đồng</span><span class="sxs-lookup"><span data-stu-id="3a1a0-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="3a1a0-250">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="3a1a0-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="3a1a0-251">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="3a1a0-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3a1a0-252">Chi phí đơn vị nguồn lực</span><span class="sxs-lookup"><span data-stu-id="3a1a0-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="3a1a0-253">Tiền tệ đơn vị nguồn lực</span><span class="sxs-lookup"><span data-stu-id="3a1a0-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3a1a0-254">Bán hàng liên tổ chức</span><span class="sxs-lookup"><span data-stu-id="3a1a0-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="3a1a0-255">Tiền tệ của đơn vị hợp đồng</span><span class="sxs-lookup"><span data-stu-id="3a1a0-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3a1a0-256">Thực tế bán hàng chưa lập hóa đơn – Có thể tính phí cho số lượng mới</span><span class="sxs-lookup"><span data-stu-id="3a1a0-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="3a1a0-257">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3a1a0-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3a1a0-258">Thực tế bán hàng chưa lập hóa đơn – Không thể tính phí cho phần chênh lệch</span><span class="sxs-lookup"><span data-stu-id="3a1a0-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="3a1a0-259">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3a1a0-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="3a1a0-260">Hóa đơn được xác nhận, số giờ có thể lập hóa đơn sẽ không thay đổi hay tăng.</span><span class="sxs-lookup"><span data-stu-id="3a1a0-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="3a1a0-261">Đảo ngược bán hàng chưa lập hóa đơn</span><span class="sxs-lookup"><span data-stu-id="3a1a0-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="3a1a0-262">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3a1a0-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="3a1a0-263">Doanh số đã lập hóa đơn cho mốc quan trọng</span><span class="sxs-lookup"><span data-stu-id="3a1a0-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="3a1a0-264">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3a1a0-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="3a1a0-265">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="3a1a0-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="3a1a0-266">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="3a1a0-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3a1a0-267">Doanh số đã lập hóa đơn</span><span class="sxs-lookup"><span data-stu-id="3a1a0-267">Billed sales</span></span></td>
<td><span data-ttu-id="3a1a0-268">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3a1a0-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="3a1a0-269">Hóa đơn được xác nhận, số giờ có thể lập hóa đơn giảm.</span><span class="sxs-lookup"><span data-stu-id="3a1a0-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="3a1a0-270">Đảo ngược bán hàng chưa lập hóa đơn</span><span class="sxs-lookup"><span data-stu-id="3a1a0-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="3a1a0-271">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3a1a0-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="3a1a0-272">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="3a1a0-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="3a1a0-273">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="3a1a0-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="3a1a0-274">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="3a1a0-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="3a1a0-275">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="3a1a0-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3a1a0-276">Doanh số chưa lập hóa đơn – Có thể tính phí cho số lượng mới</span><span class="sxs-lookup"><span data-stu-id="3a1a0-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="3a1a0-277">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3a1a0-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3a1a0-278">Doanh số chưa lập hóa đơn – Không thể tính phí cho phần chênh lệch</span><span class="sxs-lookup"><span data-stu-id="3a1a0-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="3a1a0-279">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3a1a0-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="3a1a0-280">Hóa đơn được sửa để tăng số lượng có thể tính phí.</span><span class="sxs-lookup"><span data-stu-id="3a1a0-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="3a1a0-281">Doanh số đã tính phí – Đảo ngược</span><span class="sxs-lookup"><span data-stu-id="3a1a0-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="3a1a0-282">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3a1a0-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="3a1a0-283">Đảo ngược doanh số đã lập hóa đơn cho mốc quan trọng</span><span class="sxs-lookup"><span data-stu-id="3a1a0-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="3a1a0-284">Thay đổi trạng thái mốc quan trọng từ <strong>Đã lập hóa đơn</strong> thành <strong>Sẵn sàng lập hóa đơn</strong></span><span class="sxs-lookup"><span data-stu-id="3a1a0-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="3a1a0-285">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3a1a0-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="3a1a0-286">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="3a1a0-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="3a1a0-287">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="3a1a0-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3a1a0-288">Doanh số đã lập hóa đơn</span><span class="sxs-lookup"><span data-stu-id="3a1a0-288">Billed sales</span></span></td>
<td><span data-ttu-id="3a1a0-289">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3a1a0-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="3a1a0-290">Hóa đơn được sửa để giảm số lượng có thể tính phí.</span><span class="sxs-lookup"><span data-stu-id="3a1a0-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="3a1a0-291">Doanh số đã tính phí – Đảo ngược</span><span class="sxs-lookup"><span data-stu-id="3a1a0-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="3a1a0-292">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3a1a0-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3a1a0-293">Doanh số chưa lập hóa đơn cho số lượng mới</span><span class="sxs-lookup"><span data-stu-id="3a1a0-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="3a1a0-294">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3a1a0-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3a1a0-295">Doanh số chưa lập hóa đơn – Có thể tính phí cho phần chênh lệch</span><span class="sxs-lookup"><span data-stu-id="3a1a0-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="3a1a0-296">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3a1a0-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]