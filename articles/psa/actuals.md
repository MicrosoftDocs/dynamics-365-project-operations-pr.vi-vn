---
title: Tổng quan về giá trị thực tế
description: Chủ đề này cung cấp thông tin về thực tế dự án.
author: rumant
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 08/03/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: cbb3e5c7f74cdf37ae4d259687bf7a98102a8131
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368187"
---
# <a name="actuals-overview"></a><span data-ttu-id="d4592-103">Tổng quan về giá trị thực tế</span><span class="sxs-lookup"><span data-stu-id="d4592-103">Actuals overview</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="d4592-104">Thực tế là lượng công việc đã hoàn thành trên một dự án.</span><span class="sxs-lookup"><span data-stu-id="d4592-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="d4592-105">Có thể truy nguyên thực tế dự án theo tài liệu nguồn.</span><span class="sxs-lookup"><span data-stu-id="d4592-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="d4592-106">Các tài liệu nguồn đó bao gồm mục nhập thời gian, chi phí và nhật ký cũng như hóa đơn.</span><span class="sxs-lookup"><span data-stu-id="d4592-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Cách truy nguyên thực tế dự án theo tài liệu nguồn](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="d4592-108">Gửi mục nhập thời gian</span><span class="sxs-lookup"><span data-stu-id="d4592-108">Submitting a time entry</span></span>

<span data-ttu-id="d4592-109">Trong PSA, khi một mục thời gian được gửi cho một dự án được ánh xạ tới một dòng hợp đồng thời gian và vật tư, hai dòng nhật ký kế toán sẽ được tạo.</span><span class="sxs-lookup"><span data-stu-id="d4592-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="d4592-110">Một dòng dành cho chi phí và dòng còn lại dành cho bán hàng chưa lập hóa đơn.</span><span class="sxs-lookup"><span data-stu-id="d4592-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="d4592-111">Khi một mục thời gian được gửi cho một dự án được ánh xạ tới một dòng hợp đồng giá cố định, thì dòng nhật ký kế toán chỉ được tạo cho chi phí.</span><span class="sxs-lookup"><span data-stu-id="d4592-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="d4592-112">Logic để nhập giá mặc định nằm trên dòng nhật ký kế toán.</span><span class="sxs-lookup"><span data-stu-id="d4592-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="d4592-113">Tất cả các giá trị trường từ một mục nhập thời gian được sao chép vào dòng nhật ký kế toán.</span><span class="sxs-lookup"><span data-stu-id="d4592-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="d4592-114">Các trường này bao gồm ngày giao dịch, dòng hợp đồng mà dự án được ánh xạ tới và kết quả tiền tệ trong bảng giá phù hợp.</span><span class="sxs-lookup"><span data-stu-id="d4592-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="d4592-115">Các trường ảnh hưởng đến giá mặc định, chẳng hạn như **Vai trò** và **Đơn vị tổ chức** có thể khiến một mức giá phù hợp được nhập vào dòng nhật ký kế toán theo mặc định.</span><span class="sxs-lookup"><span data-stu-id="d4592-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="d4592-116">Nếu bạn thêm một trường tùy chỉnh vào mục nhập thời gian và bạn muốn điền vào thực tế, hãy tạo trường đó trên thực thể Thực tế và sử dụng ánh xạ trường để sao chép trường từ mục nhập thời gian tới thực tế.</span><span class="sxs-lookup"><span data-stu-id="d4592-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="d4592-117">Gửi một mục nhập chi phí</span><span class="sxs-lookup"><span data-stu-id="d4592-117">Submitting an expense entry</span></span>

<span data-ttu-id="d4592-118">Trong PSA, khi một mục nhập chi phí được gửi cho một dự án được ánh xạ tới một dòng hợp đồng thời gian và vật tư, hai dòng nhật ký kế toán sẽ được tạo.</span><span class="sxs-lookup"><span data-stu-id="d4592-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="d4592-119">Một dòng dành cho chi phí và dòng còn lại dành cho bán hàng chưa lập hóa đơn.</span><span class="sxs-lookup"><span data-stu-id="d4592-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="d4592-120">Khi một mục nhập chi phí được gửi cho một dự án được ánh xạ tới một dòng hợp đồng giá cố định, thì dòng nhật ký kế toán chỉ được tạo cho chi phí.</span><span class="sxs-lookup"><span data-stu-id="d4592-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="d4592-121">Logic để nhập giá mặc định cho chi phí dựa trên loại chi phí được chọn trên trang **Mục nhập chi phí**.</span><span class="sxs-lookup"><span data-stu-id="d4592-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="d4592-122">Ngày giao dịch, dòng hợp đồng mà dự án được ánh xạ tới và tiền tệ được dùng để xác định bảng giá phù hợp.</span><span class="sxs-lookup"><span data-stu-id="d4592-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="d4592-123">Tuy nhiên, đối với giá, số tiền mà người dùng nhập được đặt trực tiếp trên dòng nhật ký kế toán chi phí liên quan cho chi phí và bán hàng theo mặc định.</span><span class="sxs-lookup"><span data-stu-id="d4592-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="d4592-124">Trong phiên bản hiện tại của PSA, mục nhập dựa trên danh mục của giá mặc định cho mỗi đơn vị các mục nhập chi phí không khả dụng.</span><span class="sxs-lookup"><span data-stu-id="d4592-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="d4592-125">Sử dụng nhật ký Mục nhập để ghi lại chi phí</span><span class="sxs-lookup"><span data-stu-id="d4592-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="d4592-126">Trong PSA, nhật ký Mục nhập cho phép bạn ghi lại chi phí hoặc doanh thu trong lớp giao dịch thuế, chi phí, thời gian, phí hoặc vật tư.</span><span class="sxs-lookup"><span data-stu-id="d4592-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="d4592-127">Nhật ký kế toán có tiêu đề, các dòng và hành động **Xác nhận**.</span><span class="sxs-lookup"><span data-stu-id="d4592-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="d4592-128">Dưới đây là một số tình huống mà bạn có thể sử dụng một nhật ký kế toán:</span><span class="sxs-lookup"><span data-stu-id="d4592-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="d4592-129">Bạn phải ghi lại các chi phí vật tư thực tế và bán hàng trên một dự án.</span><span class="sxs-lookup"><span data-stu-id="d4592-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="d4592-130">Bạn phải di chuyển thực tế giao dịch từ một hệ thống khác sang PSA.</span><span class="sxs-lookup"><span data-stu-id="d4592-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="d4592-131">Bạn phải ghi lại chi phí xảy ra trong một hệ thống khác, chẳng hạn như mua sắm hoặc chi phí thầu phụ.</span><span class="sxs-lookup"><span data-stu-id="d4592-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d4592-132">Chỉ người dùng nhận biết đầy đủ về tác động kế toán của Thực tế đối với dự án mới có thể dùng nhật ký Mục nhập để tạo thực thể Thực tế.</span><span class="sxs-lookup"><span data-stu-id="d4592-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="d4592-133">Điều này là do ứng dụng không xác nhận loại dòng nhật ký kế toán hoặc giá liên quan được nhập vào dòng nhật ký kế toán.</span><span class="sxs-lookup"><span data-stu-id="d4592-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="d4592-134">Do tác động của loại nhật ký này, hãy thận trọng đối với người được cấp quyền truy cập để tạo nhật ký Mục nhập.</span><span class="sxs-lookup"><span data-stu-id="d4592-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="d4592-135">Ghi lại thực tế dựa trên sự kiện dự án</span><span class="sxs-lookup"><span data-stu-id="d4592-135">Recording actuals based on project events</span></span>

<span data-ttu-id="d4592-136">PSA ghi lại các giao dịch tài chính xảy ra trong một dự án.</span><span class="sxs-lookup"><span data-stu-id="d4592-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="d4592-137">Các giao dịch này được ghi lại là **thực tế**.</span><span class="sxs-lookup"><span data-stu-id="d4592-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="d4592-138">Các bảng sau đây hiển thị các loại thực tế khác nhau được tạo, phụ thuộc vào việc dự án là dự án thời gian và vật tư hay giá cố định, ở giai đoạn trước khi bán hàng hay là dự án nội bộ.</span><span class="sxs-lookup"><span data-stu-id="d4592-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="d4592-139">**Tài nguyên thuộc về cùng một đơn vị tổ chức như đơn vị hợp đồng của dự án**</span><span class="sxs-lookup"><span data-stu-id="d4592-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="d4592-140">Sự kiện</span><span class="sxs-lookup"><span data-stu-id="d4592-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="d4592-141">Dự án có thể lập hóa đơn hoặc đã bán</span><span class="sxs-lookup"><span data-stu-id="d4592-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="d4592-142">Dự án trong giai đoạn trước khi bán</span><span class="sxs-lookup"><span data-stu-id="d4592-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="d4592-143">Dự án nội bộ</span><span class="sxs-lookup"><span data-stu-id="d4592-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="d4592-144">Thời gian và vật tư</span><span class="sxs-lookup"><span data-stu-id="d4592-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="d4592-145">Giá cố định</span><span class="sxs-lookup"><span data-stu-id="d4592-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="d4592-146">Thực tế</span><span class="sxs-lookup"><span data-stu-id="d4592-146">Actuals</span></span></th>
<th><span data-ttu-id="d4592-147">Loại tiền giao dịch</span><span class="sxs-lookup"><span data-stu-id="d4592-147">Transaction currency</span></span></th>
<th><span data-ttu-id="d4592-148">Giá cố định</span><span class="sxs-lookup"><span data-stu-id="d4592-148">Fixed price</span></span></th>
<th><span data-ttu-id="d4592-149">Loại tiền giao dịch</span><span class="sxs-lookup"><span data-stu-id="d4592-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d4592-150">Mục nhập thời gian được tạo.</span><span class="sxs-lookup"><span data-stu-id="d4592-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="d4592-151">Không có hoạt động trong thực thể Thực tế</span><span class="sxs-lookup"><span data-stu-id="d4592-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4592-152">Mục nhập thời gian được gửi.</span><span class="sxs-lookup"><span data-stu-id="d4592-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="d4592-153">Không có hoạt động trong thực thể Thực tế</span><span class="sxs-lookup"><span data-stu-id="d4592-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d4592-154">Thời gian được phê duyệt và số giờ có thể lập hóa đơn sẽ không thay đổi hay tăng trong quá trình phê duyệt.</span><span class="sxs-lookup"><span data-stu-id="d4592-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="d4592-155">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="d4592-155">Cost actual</span></span></td>
<td><span data-ttu-id="d4592-156">Tiền tệ của đơn vị hợp đồng</span><span class="sxs-lookup"><span data-stu-id="d4592-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="d4592-157">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="d4592-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="d4592-158">Tiền tệ của đơn vị hợp đồng</span><span class="sxs-lookup"><span data-stu-id="d4592-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="d4592-159">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="d4592-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="d4592-160">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="d4592-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4592-161">Thực tế bán hàng chưa lập hóa đơn – Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="d4592-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="d4592-162">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="d4592-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d4592-163">Thời gian được phê duyệt và số giờ có thể lập hóa đơn giảm trong quá trình phê duyệt.</span><span class="sxs-lookup"><span data-stu-id="d4592-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="d4592-164">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="d4592-164">Cost actual</span></span></td>
<td><span data-ttu-id="d4592-165">Tiền tệ của đơn vị hợp đồng</span><span class="sxs-lookup"><span data-stu-id="d4592-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="d4592-166">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="d4592-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="d4592-167">Tiền tệ của đơn vị hợp đồng</span><span class="sxs-lookup"><span data-stu-id="d4592-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="d4592-168">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="d4592-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="d4592-169">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="d4592-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4592-170">Thực tế bán hàng chưa lập hóa đơn – Có thể tính phí cho số lượng mới</span><span class="sxs-lookup"><span data-stu-id="d4592-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="d4592-171">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="d4592-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4592-172">Thực tế bán hàng chưa lập hóa đơn – Không thể tính phí cho phần chênh lệch</span><span class="sxs-lookup"><span data-stu-id="d4592-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="d4592-173">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="d4592-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d4592-174">Hóa đơn được xác nhận, số giờ có thể lập hóa đơn sẽ không thay đổi hay tăng.</span><span class="sxs-lookup"><span data-stu-id="d4592-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="d4592-175">Đảo ngược bán hàng chưa lập hóa đơn</span><span class="sxs-lookup"><span data-stu-id="d4592-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="d4592-176">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="d4592-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="d4592-177">Doanh số đã lập hóa đơn cho mốc quan trọng</span><span class="sxs-lookup"><span data-stu-id="d4592-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="d4592-178">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="d4592-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="d4592-179">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="d4592-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="d4592-180">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="d4592-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4592-181">Doanh số đã lập hóa đơn</span><span class="sxs-lookup"><span data-stu-id="d4592-181">Billed sales</span></span></td>
<td><span data-ttu-id="d4592-182">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="d4592-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d4592-183">Hóa đơn được xác nhận, số giờ có thể lập hóa đơn giảm.</span><span class="sxs-lookup"><span data-stu-id="d4592-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="d4592-184">Đảo ngược bán hàng chưa lập hóa đơn</span><span class="sxs-lookup"><span data-stu-id="d4592-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="d4592-185">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="d4592-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="d4592-186">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="d4592-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d4592-187">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="d4592-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d4592-188">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="d4592-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d4592-189">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="d4592-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4592-190">Doanh số chưa lập hóa đơn – Có thể tính phí cho số lượng mới</span><span class="sxs-lookup"><span data-stu-id="d4592-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="d4592-191">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="d4592-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4592-192">Doanh số chưa lập hóa đơn – Không thể tính phí cho phần chênh lệch</span><span class="sxs-lookup"><span data-stu-id="d4592-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="d4592-193">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="d4592-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d4592-194">Hóa đơn được sửa để tăng số lượng có thể tính phí.</span><span class="sxs-lookup"><span data-stu-id="d4592-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="d4592-195">Doanh số đã tính phí – Đảo ngược</span><span class="sxs-lookup"><span data-stu-id="d4592-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="d4592-196">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="d4592-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="d4592-197">Đảo ngược doanh số đã lập hóa đơn cho mốc quan trọng</span><span class="sxs-lookup"><span data-stu-id="d4592-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="d4592-198">Thay đổi trạng thái mốc quan trọng từ <strong>Đã lập hóa đơn</strong> thành <strong>Sẵn sàng lập hóa đơn</strong></span><span class="sxs-lookup"><span data-stu-id="d4592-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="d4592-199">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="d4592-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="d4592-200">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="d4592-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="d4592-201">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="d4592-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4592-202">Doanh số đã lập hóa đơn</span><span class="sxs-lookup"><span data-stu-id="d4592-202">Billed sales</span></span></td>
<td><span data-ttu-id="d4592-203">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="d4592-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d4592-204">Hóa đơn được sửa để giảm số lượng có thể tính phí.</span><span class="sxs-lookup"><span data-stu-id="d4592-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="d4592-205">Doanh số đã tính phí – Đảo ngược</span><span class="sxs-lookup"><span data-stu-id="d4592-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="d4592-206">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="d4592-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4592-207">Doanh số chưa lập hóa đơn cho số lượng mới</span><span class="sxs-lookup"><span data-stu-id="d4592-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="d4592-208">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="d4592-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4592-209">Doanh số chưa lập hóa đơn – Có thể tính phí cho phần chênh lệch</span><span class="sxs-lookup"><span data-stu-id="d4592-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="d4592-210">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="d4592-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d4592-211">**Tài nguyên thuộc về một đơn vị tổ chức khác với đơn vị hợp đồng của dự án**</span><span class="sxs-lookup"><span data-stu-id="d4592-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="d4592-212">Sự kiện</span><span class="sxs-lookup"><span data-stu-id="d4592-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="d4592-213">Dự án có thể lập hóa đơn hoặc đã bán</span><span class="sxs-lookup"><span data-stu-id="d4592-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="d4592-214">Dự án trong giai đoạn trước khi bán</span><span class="sxs-lookup"><span data-stu-id="d4592-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="d4592-215">Dự án nội bộ</span><span class="sxs-lookup"><span data-stu-id="d4592-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="d4592-216">Thời gian và vật tư</span><span class="sxs-lookup"><span data-stu-id="d4592-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="d4592-217">Giá cố định</span><span class="sxs-lookup"><span data-stu-id="d4592-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="d4592-218">Thực tế</span><span class="sxs-lookup"><span data-stu-id="d4592-218">Actuals</span></span></th>
<th><span data-ttu-id="d4592-219">Loại tiền giao dịch</span><span class="sxs-lookup"><span data-stu-id="d4592-219">Transaction currency</span></span></th>
<th><span data-ttu-id="d4592-220">Giá cố định</span><span class="sxs-lookup"><span data-stu-id="d4592-220">Fixed price</span></span></th>
<th><span data-ttu-id="d4592-221">Loại tiền giao dịch</span><span class="sxs-lookup"><span data-stu-id="d4592-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d4592-222">Mục nhập thời gian được tạo.</span><span class="sxs-lookup"><span data-stu-id="d4592-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="d4592-223">Không có hoạt động trong thực thể Thực tế</span><span class="sxs-lookup"><span data-stu-id="d4592-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4592-224">Mục nhập thời gian được gửi.</span><span class="sxs-lookup"><span data-stu-id="d4592-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="d4592-225">Không có hoạt động trong thực thể Thực tế</span><span class="sxs-lookup"><span data-stu-id="d4592-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="d4592-226">Thời gian được phê duyệt và số giờ có thể lập hóa đơn sẽ không thay đổi hay tăng trong quá trình phê duyệt.</span><span class="sxs-lookup"><span data-stu-id="d4592-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="d4592-227">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="d4592-227">Cost actual</span></span></td>
<td><span data-ttu-id="d4592-228">Tiền tệ của đơn vị hợp đồng</span><span class="sxs-lookup"><span data-stu-id="d4592-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="d4592-229">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="d4592-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="d4592-230">Tiền tệ của đơn vị hợp đồng</span><span class="sxs-lookup"><span data-stu-id="d4592-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="d4592-231">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="d4592-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="d4592-232">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="d4592-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4592-233">Thực tế bán hàng chưa lập hóa đơn – Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="d4592-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="d4592-234">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="d4592-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4592-235">Chi phí đơn vị nguồn lực</span><span class="sxs-lookup"><span data-stu-id="d4592-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="d4592-236">Tiền tệ đơn vị nguồn lực</span><span class="sxs-lookup"><span data-stu-id="d4592-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4592-237">Bán hàng liên tổ chức</span><span class="sxs-lookup"><span data-stu-id="d4592-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="d4592-238">Tiền tệ của đơn vị hợp đồng</span><span class="sxs-lookup"><span data-stu-id="d4592-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="d4592-239">Thời gian được phê duyệt và số giờ có thể lập hóa đơn giảm trong quá trình phê duyệt.</span><span class="sxs-lookup"><span data-stu-id="d4592-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="d4592-240">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="d4592-240">Cost actual</span></span></td>
<td><span data-ttu-id="d4592-241">Tiền tệ của đơn vị hợp đồng</span><span class="sxs-lookup"><span data-stu-id="d4592-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="d4592-242">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="d4592-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="d4592-243">Tiền tệ của đơn vị hợp đồng</span><span class="sxs-lookup"><span data-stu-id="d4592-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="d4592-244">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="d4592-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="d4592-245">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="d4592-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4592-246">Chi phí đơn vị nguồn lực</span><span class="sxs-lookup"><span data-stu-id="d4592-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="d4592-247">Tiền tệ đơn vị nguồn lực</span><span class="sxs-lookup"><span data-stu-id="d4592-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4592-248">Bán hàng liên tổ chức</span><span class="sxs-lookup"><span data-stu-id="d4592-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="d4592-249">Tiền tệ của đơn vị hợp đồng</span><span class="sxs-lookup"><span data-stu-id="d4592-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4592-250">Thực tế bán hàng chưa lập hóa đơn – Có thể tính phí cho số lượng mới</span><span class="sxs-lookup"><span data-stu-id="d4592-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="d4592-251">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="d4592-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4592-252">Thực tế bán hàng chưa lập hóa đơn – Không thể tính phí cho phần chênh lệch</span><span class="sxs-lookup"><span data-stu-id="d4592-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="d4592-253">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="d4592-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d4592-254">Hóa đơn được xác nhận, số giờ có thể lập hóa đơn sẽ không thay đổi hay tăng.</span><span class="sxs-lookup"><span data-stu-id="d4592-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="d4592-255">Đảo ngược bán hàng chưa lập hóa đơn</span><span class="sxs-lookup"><span data-stu-id="d4592-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="d4592-256">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="d4592-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="d4592-257">Doanh số đã lập hóa đơn cho mốc quan trọng</span><span class="sxs-lookup"><span data-stu-id="d4592-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="d4592-258">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="d4592-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="d4592-259">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="d4592-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="d4592-260">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="d4592-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4592-261">Doanh số đã lập hóa đơn</span><span class="sxs-lookup"><span data-stu-id="d4592-261">Billed sales</span></span></td>
<td><span data-ttu-id="d4592-262">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="d4592-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d4592-263">Hóa đơn được xác nhận, số giờ có thể lập hóa đơn giảm.</span><span class="sxs-lookup"><span data-stu-id="d4592-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="d4592-264">Đảo ngược bán hàng chưa lập hóa đơn</span><span class="sxs-lookup"><span data-stu-id="d4592-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="d4592-265">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="d4592-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="d4592-266">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="d4592-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d4592-267">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="d4592-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d4592-268">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="d4592-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d4592-269">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="d4592-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4592-270">Doanh số chưa lập hóa đơn – Có thể tính phí cho số lượng mới</span><span class="sxs-lookup"><span data-stu-id="d4592-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="d4592-271">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="d4592-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4592-272">Doanh số chưa lập hóa đơn – Không thể tính phí cho phần chênh lệch</span><span class="sxs-lookup"><span data-stu-id="d4592-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="d4592-273">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="d4592-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d4592-274">Hóa đơn được sửa để tăng số lượng có thể tính phí.</span><span class="sxs-lookup"><span data-stu-id="d4592-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="d4592-275">Doanh số đã tính phí – Đảo ngược</span><span class="sxs-lookup"><span data-stu-id="d4592-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="d4592-276">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="d4592-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="d4592-277">Đảo ngược doanh số đã lập hóa đơn cho mốc quan trọng</span><span class="sxs-lookup"><span data-stu-id="d4592-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="d4592-278">Thay đổi trạng thái mốc quan trọng từ <strong>Đã lập hóa đơn</strong> thành <strong>Sẵn sàng lập hóa đơn</strong></span><span class="sxs-lookup"><span data-stu-id="d4592-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="d4592-279">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="d4592-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="d4592-280">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="d4592-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="d4592-281">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="d4592-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4592-282">Doanh số đã lập hóa đơn</span><span class="sxs-lookup"><span data-stu-id="d4592-282">Billed sales</span></span></td>
<td><span data-ttu-id="d4592-283">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="d4592-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d4592-284">Hóa đơn được sửa để giảm số lượng có thể tính phí.</span><span class="sxs-lookup"><span data-stu-id="d4592-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="d4592-285">Doanh số đã tính phí – Đảo ngược</span><span class="sxs-lookup"><span data-stu-id="d4592-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="d4592-286">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="d4592-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4592-287">Doanh số chưa lập hóa đơn cho số lượng mới</span><span class="sxs-lookup"><span data-stu-id="d4592-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="d4592-288">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="d4592-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4592-289">Doanh số chưa lập hóa đơn – Có thể tính phí cho phần chênh lệch</span><span class="sxs-lookup"><span data-stu-id="d4592-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="d4592-290">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="d4592-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]