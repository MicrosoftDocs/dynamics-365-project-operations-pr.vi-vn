---
title: Thực tế
description: Chủ đề này cung cấp thông tin về thực tế dự án.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 44c6e85f-5b21-4e24-999c-15a2f065d977
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8291e0eb8531e8e9690368675f333c44b6e92e48
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 03/24/2020
ms.locfileid: "3757118"
---
# <a name="actuals"></a><span data-ttu-id="3c500-103">Thực tế</span><span class="sxs-lookup"><span data-stu-id="3c500-103">Actuals</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="3c500-104">Thực tế là lượng công việc đã hoàn thành trên một dự án.</span><span class="sxs-lookup"><span data-stu-id="3c500-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="3c500-105">Có thể truy nguyên thực tế dự án theo tài liệu nguồn.</span><span class="sxs-lookup"><span data-stu-id="3c500-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="3c500-106">Các tài liệu nguồn đó bao gồm mục nhập thời gian, chi phí và nhật ký cũng như hóa đơn.</span><span class="sxs-lookup"><span data-stu-id="3c500-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Cách truy nguyên thực tế dự án theo tài liệu nguồn](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="3c500-108">Gửi mục nhập thời gian</span><span class="sxs-lookup"><span data-stu-id="3c500-108">Submitting a time entry</span></span>

<span data-ttu-id="3c500-109">Trong PSA, khi một mục thời gian được gửi cho một dự án được ánh xạ tới một dòng hợp đồng thời gian và vật tư, hai dòng nhật ký kế toán sẽ được tạo.</span><span class="sxs-lookup"><span data-stu-id="3c500-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="3c500-110">Một dòng dành cho chi phí và dòng còn lại dành cho bán hàng chưa lập hóa đơn.</span><span class="sxs-lookup"><span data-stu-id="3c500-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="3c500-111">Khi một mục thời gian được gửi cho một dự án được ánh xạ tới một dòng hợp đồng giá cố định, thì dòng nhật ký kế toán chỉ được tạo cho chi phí.</span><span class="sxs-lookup"><span data-stu-id="3c500-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="3c500-112">Logic để nhập giá mặc định nằm trên dòng nhật ký kế toán.</span><span class="sxs-lookup"><span data-stu-id="3c500-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="3c500-113">Tất cả các giá trị trường từ một mục nhập thời gian được sao chép vào dòng nhật ký kế toán.</span><span class="sxs-lookup"><span data-stu-id="3c500-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="3c500-114">Các trường này bao gồm ngày giao dịch, dòng hợp đồng mà dự án được ánh xạ tới và kết quả tiền tệ trong bảng giá phù hợp.</span><span class="sxs-lookup"><span data-stu-id="3c500-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="3c500-115">Các trường ảnh hưởng đến giá mặc định, chẳng hạn như **Vai trò** và **Đơn vị tổ chức** có thể khiến một mức giá phù hợp được nhập vào dòng nhật ký kế toán theo mặc định.</span><span class="sxs-lookup"><span data-stu-id="3c500-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="3c500-116">Nếu bạn thêm một trường tùy chỉnh vào mục nhập thời gian và bạn muốn điền vào thực tế, hãy tạo trường đó trên thực thể Thực tế và sử dụng ánh xạ trường để sao chép trường từ mục nhập thời gian tới thực tế.</span><span class="sxs-lookup"><span data-stu-id="3c500-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="3c500-117">Gửi một mục nhập chi phí</span><span class="sxs-lookup"><span data-stu-id="3c500-117">Submitting an expense entry</span></span>

<span data-ttu-id="3c500-118">Trong PSA, khi một mục nhập chi phí được gửi cho một dự án được ánh xạ tới một dòng hợp đồng thời gian và vật tư, hai dòng nhật ký kế toán sẽ được tạo.</span><span class="sxs-lookup"><span data-stu-id="3c500-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="3c500-119">Một dòng dành cho chi phí và dòng còn lại dành cho bán hàng chưa lập hóa đơn.</span><span class="sxs-lookup"><span data-stu-id="3c500-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="3c500-120">Khi một mục nhập chi phí được gửi cho một dự án được ánh xạ tới một dòng hợp đồng giá cố định, thì dòng nhật ký kế toán chỉ được tạo cho chi phí.</span><span class="sxs-lookup"><span data-stu-id="3c500-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="3c500-121">Logic để nhập giá mặc định cho chi phí dựa trên loại chi phí được chọn trên trang **Mục nhập chi phí**.</span><span class="sxs-lookup"><span data-stu-id="3c500-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="3c500-122">Ngày giao dịch, dòng hợp đồng mà dự án được ánh xạ tới và tiền tệ được dùng để xác định bảng giá phù hợp.</span><span class="sxs-lookup"><span data-stu-id="3c500-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="3c500-123">Tuy nhiên, đối với giá, số tiền mà người dùng nhập được đặt trực tiếp trên dòng nhật ký kế toán chi phí liên quan cho chi phí và bán hàng theo mặc định.</span><span class="sxs-lookup"><span data-stu-id="3c500-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="3c500-124">Trong phiên bản hiện tại của PSA, mục nhập dựa trên danh mục của giá mặc định cho mỗi đơn vị các mục nhập chi phí không khả dụng.</span><span class="sxs-lookup"><span data-stu-id="3c500-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-journals-to-record-costs"></a><span data-ttu-id="3c500-125">Sử dụng nhật ký kế toán để ghi lại chi phí</span><span class="sxs-lookup"><span data-stu-id="3c500-125">Using journals to record costs</span></span>

<span data-ttu-id="3c500-126">Trong PSA, nhật ký kế toán cho phép bạn ghi lại chi phí hoặc doanh thu trong lớp giao dịch thuế, chi phí, thời gian, phí hoặc vật tư.</span><span class="sxs-lookup"><span data-stu-id="3c500-126">In PSA, journals let you record cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="3c500-127">Nhật ký kế toán có tiêu đề, các dòng và hành động **Xác nhận**.</span><span class="sxs-lookup"><span data-stu-id="3c500-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="3c500-128">Dưới đây là một số tình huống mà bạn có thể sử dụng một nhật ký kế toán:</span><span class="sxs-lookup"><span data-stu-id="3c500-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="3c500-129">Bạn phải ghi lại các chi phí vật tư thực tế và bán hàng trên một dự án.</span><span class="sxs-lookup"><span data-stu-id="3c500-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="3c500-130">Bạn phải di chuyển thực tế giao dịch từ một hệ thống khác sang PSA.</span><span class="sxs-lookup"><span data-stu-id="3c500-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="3c500-131">Bạn phải ghi lại chi phí xảy ra trong một hệ thống khác, chẳng hạn như mua sắm hoặc chi phí thầu phụ.</span><span class="sxs-lookup"><span data-stu-id="3c500-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="3c500-132">Ghi lại thực tế dựa trên sự kiện dự án</span><span class="sxs-lookup"><span data-stu-id="3c500-132">Recording actuals based on project events</span></span>

<span data-ttu-id="3c500-133">PSA ghi lại các giao dịch tài chính xảy ra trong một dự án.</span><span class="sxs-lookup"><span data-stu-id="3c500-133">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="3c500-134">Các giao dịch này được ghi lại là **thực tế**.</span><span class="sxs-lookup"><span data-stu-id="3c500-134">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="3c500-135">Các bảng sau đây hiển thị các loại thực tế khác nhau được tạo, phụ thuộc vào việc dự án là dự án thời gian và vật tư hay giá cố định, ở giai đoạn trước khi bán hàng hay là dự án nội bộ.</span><span class="sxs-lookup"><span data-stu-id="3c500-135">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="3c500-136">**Tài nguyên thuộc về cùng một đơn vị tổ chức như đơn vị hợp đồng của dự án**</span><span class="sxs-lookup"><span data-stu-id="3c500-136">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="3c500-137">Sự kiện</span><span class="sxs-lookup"><span data-stu-id="3c500-137">Event</span></span></th>
<th colspan="4"><span data-ttu-id="3c500-138">Dự án có thể lập hóa đơn hoặc đã bán</span><span class="sxs-lookup"><span data-stu-id="3c500-138">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="3c500-139">Dự án trong giai đoạn trước khi bán</span><span class="sxs-lookup"><span data-stu-id="3c500-139">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="3c500-140">Dự án nội bộ</span><span class="sxs-lookup"><span data-stu-id="3c500-140">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="3c500-141">Thời gian và vật tư</span><span class="sxs-lookup"><span data-stu-id="3c500-141">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="3c500-142">Giá cố định</span><span class="sxs-lookup"><span data-stu-id="3c500-142">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="3c500-143">Thực tế</span><span class="sxs-lookup"><span data-stu-id="3c500-143">Actuals</span></span></th>
<th><span data-ttu-id="3c500-144">Loại tiền giao dịch</span><span class="sxs-lookup"><span data-stu-id="3c500-144">Transaction currency</span></span></th>
<th><span data-ttu-id="3c500-145">Giá cố định</span><span class="sxs-lookup"><span data-stu-id="3c500-145">Fixed price</span></span></th>
<th><span data-ttu-id="3c500-146">Loại tiền giao dịch</span><span class="sxs-lookup"><span data-stu-id="3c500-146">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3c500-147">Mục nhập thời gian được tạo.</span><span class="sxs-lookup"><span data-stu-id="3c500-147">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="3c500-148">Không có hoạt động trong thực thể Thực tế</span><span class="sxs-lookup"><span data-stu-id="3c500-148">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c500-149">Mục nhập thời gian được gửi.</span><span class="sxs-lookup"><span data-stu-id="3c500-149">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="3c500-150">Không có hoạt động trong thực thể Thực tế</span><span class="sxs-lookup"><span data-stu-id="3c500-150">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="3c500-151">Thời gian được phê duyệt và số giờ có thể lập hóa đơn sẽ không thay đổi hay tăng trong quá trình phê duyệt.</span><span class="sxs-lookup"><span data-stu-id="3c500-151">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="3c500-152">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="3c500-152">Cost actual</span></span></td>
<td><span data-ttu-id="3c500-153">Tiền tệ của đơn vị hợp đồng</span><span class="sxs-lookup"><span data-stu-id="3c500-153">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="3c500-154">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="3c500-154">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="3c500-155">Tiền tệ của đơn vị hợp đồng</span><span class="sxs-lookup"><span data-stu-id="3c500-155">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="3c500-156">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="3c500-156">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="3c500-157">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="3c500-157">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c500-158">Thực tế bán hàng chưa lập hóa đơn – Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="3c500-158">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="3c500-159">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3c500-159">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="3c500-160">Thời gian được phê duyệt và số giờ có thể lập hóa đơn giảm trong quá trình phê duyệt.</span><span class="sxs-lookup"><span data-stu-id="3c500-160">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="3c500-161">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="3c500-161">Cost actual</span></span></td>
<td><span data-ttu-id="3c500-162">Tiền tệ của đơn vị hợp đồng</span><span class="sxs-lookup"><span data-stu-id="3c500-162">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="3c500-163">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="3c500-163">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="3c500-164">Tiền tệ của đơn vị hợp đồng</span><span class="sxs-lookup"><span data-stu-id="3c500-164">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="3c500-165">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="3c500-165">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="3c500-166">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="3c500-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c500-167">Thực tế bán hàng chưa lập hóa đơn – Có thể tính phí cho số lượng mới</span><span class="sxs-lookup"><span data-stu-id="3c500-167">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="3c500-168">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3c500-168">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c500-169">Thực tế bán hàng chưa lập hóa đơn – Không thể tính phí cho phần chênh lệch</span><span class="sxs-lookup"><span data-stu-id="3c500-169">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="3c500-170">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3c500-170">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="3c500-171">Hóa đơn được xác nhận, số giờ có thể lập hóa đơn sẽ không thay đổi hay tăng.</span><span class="sxs-lookup"><span data-stu-id="3c500-171">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="3c500-172">Đảo ngược bán hàng chưa lập hóa đơn</span><span class="sxs-lookup"><span data-stu-id="3c500-172">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="3c500-173">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3c500-173">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="3c500-174">Doanh số đã lập hóa đơn cho mốc quan trọng</span><span class="sxs-lookup"><span data-stu-id="3c500-174">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="3c500-175">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3c500-175">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="3c500-176">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="3c500-176">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="3c500-177">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="3c500-177">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c500-178">Doanh số đã lập hóa đơn</span><span class="sxs-lookup"><span data-stu-id="3c500-178">Billed sales</span></span></td>
<td><span data-ttu-id="3c500-179">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3c500-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="3c500-180">Hóa đơn được xác nhận, số giờ có thể lập hóa đơn giảm.</span><span class="sxs-lookup"><span data-stu-id="3c500-180">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="3c500-181">Đảo ngược bán hàng chưa lập hóa đơn</span><span class="sxs-lookup"><span data-stu-id="3c500-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="3c500-182">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3c500-182">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="3c500-183">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="3c500-183">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="3c500-184">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="3c500-184">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="3c500-185">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="3c500-185">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="3c500-186">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="3c500-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c500-187">Doanh số chưa lập hóa đơn – Có thể tính phí cho số lượng mới</span><span class="sxs-lookup"><span data-stu-id="3c500-187">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="3c500-188">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3c500-188">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c500-189">Doanh số chưa lập hóa đơn – Không thể tính phí cho phần chênh lệch</span><span class="sxs-lookup"><span data-stu-id="3c500-189">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="3c500-190">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3c500-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="3c500-191">Hóa đơn được sửa để tăng số lượng có thể tính phí.</span><span class="sxs-lookup"><span data-stu-id="3c500-191">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="3c500-192">Doanh số đã tính phí – Đảo ngược</span><span class="sxs-lookup"><span data-stu-id="3c500-192">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="3c500-193">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3c500-193">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="3c500-194">Đảo ngược doanh số đã lập hóa đơn cho mốc quan trọng</span><span class="sxs-lookup"><span data-stu-id="3c500-194">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="3c500-195">Thay đổi trạng thái mốc quan trọng từ <strong>Đã lập hóa đơn</strong> thành <strong>Sẵn sàng lập hóa đơn</strong></span><span class="sxs-lookup"><span data-stu-id="3c500-195">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="3c500-196">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3c500-196">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="3c500-197">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="3c500-197">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="3c500-198">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="3c500-198">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c500-199">Doanh số đã lập hóa đơn</span><span class="sxs-lookup"><span data-stu-id="3c500-199">Billed sales</span></span></td>
<td><span data-ttu-id="3c500-200">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3c500-200">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="3c500-201">Hóa đơn được sửa để giảm số lượng có thể tính phí.</span><span class="sxs-lookup"><span data-stu-id="3c500-201">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="3c500-202">Doanh số đã tính phí – Đảo ngược</span><span class="sxs-lookup"><span data-stu-id="3c500-202">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="3c500-203">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3c500-203">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c500-204">Doanh số chưa lập hóa đơn cho số lượng mới</span><span class="sxs-lookup"><span data-stu-id="3c500-204">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="3c500-205">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3c500-205">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c500-206">Doanh số chưa lập hóa đơn – Có thể tính phí cho phần chênh lệch</span><span class="sxs-lookup"><span data-stu-id="3c500-206">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="3c500-207">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3c500-207">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3c500-208">**Tài nguyên thuộc về một đơn vị tổ chức khác với đơn vị hợp đồng của dự án**</span><span class="sxs-lookup"><span data-stu-id="3c500-208">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="3c500-209">Sự kiện</span><span class="sxs-lookup"><span data-stu-id="3c500-209">Event</span></span></th>
<th colspan="4"><span data-ttu-id="3c500-210">Dự án có thể lập hóa đơn hoặc đã bán</span><span class="sxs-lookup"><span data-stu-id="3c500-210">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="3c500-211">Dự án trong giai đoạn trước khi bán</span><span class="sxs-lookup"><span data-stu-id="3c500-211">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="3c500-212">Dự án nội bộ</span><span class="sxs-lookup"><span data-stu-id="3c500-212">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="3c500-213">Thời gian và vật tư</span><span class="sxs-lookup"><span data-stu-id="3c500-213">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="3c500-214">Giá cố định</span><span class="sxs-lookup"><span data-stu-id="3c500-214">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="3c500-215">Thực tế</span><span class="sxs-lookup"><span data-stu-id="3c500-215">Actuals</span></span></th>
<th><span data-ttu-id="3c500-216">Loại tiền giao dịch</span><span class="sxs-lookup"><span data-stu-id="3c500-216">Transaction currency</span></span></th>
<th><span data-ttu-id="3c500-217">Giá cố định</span><span class="sxs-lookup"><span data-stu-id="3c500-217">Fixed price</span></span></th>
<th><span data-ttu-id="3c500-218">Loại tiền giao dịch</span><span class="sxs-lookup"><span data-stu-id="3c500-218">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3c500-219">Mục nhập thời gian được tạo.</span><span class="sxs-lookup"><span data-stu-id="3c500-219">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="3c500-220">Không có hoạt động trong thực thể Thực tế</span><span class="sxs-lookup"><span data-stu-id="3c500-220">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c500-221">Mục nhập thời gian được gửi.</span><span class="sxs-lookup"><span data-stu-id="3c500-221">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="3c500-222">Không có hoạt động trong thực thể Thực tế</span><span class="sxs-lookup"><span data-stu-id="3c500-222">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="3c500-223">Thời gian được phê duyệt và số giờ có thể lập hóa đơn sẽ không thay đổi hay tăng trong quá trình phê duyệt.</span><span class="sxs-lookup"><span data-stu-id="3c500-223">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="3c500-224">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="3c500-224">Cost actual</span></span></td>
<td><span data-ttu-id="3c500-225">Tiền tệ của đơn vị hợp đồng</span><span class="sxs-lookup"><span data-stu-id="3c500-225">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="3c500-226">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="3c500-226">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="3c500-227">Tiền tệ của đơn vị hợp đồng</span><span class="sxs-lookup"><span data-stu-id="3c500-227">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="3c500-228">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="3c500-228">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="3c500-229">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="3c500-229">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c500-230">Thực tế bán hàng chưa lập hóa đơn – Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="3c500-230">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="3c500-231">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3c500-231">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c500-232">Chi phí đơn vị nguồn lực</span><span class="sxs-lookup"><span data-stu-id="3c500-232">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="3c500-233">Tiền tệ đơn vị nguồn lực</span><span class="sxs-lookup"><span data-stu-id="3c500-233">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c500-234">Bán hàng liên tổ chức</span><span class="sxs-lookup"><span data-stu-id="3c500-234">Interorganizational sales</span></span></td>
<td><span data-ttu-id="3c500-235">Tiền tệ của đơn vị hợp đồng</span><span class="sxs-lookup"><span data-stu-id="3c500-235">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="3c500-236">Thời gian được phê duyệt và số giờ có thể lập hóa đơn giảm trong quá trình phê duyệt.</span><span class="sxs-lookup"><span data-stu-id="3c500-236">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="3c500-237">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="3c500-237">Cost actual</span></span></td>
<td><span data-ttu-id="3c500-238">Tiền tệ của đơn vị hợp đồng</span><span class="sxs-lookup"><span data-stu-id="3c500-238">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="3c500-239">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="3c500-239">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="3c500-240">Tiền tệ của đơn vị hợp đồng</span><span class="sxs-lookup"><span data-stu-id="3c500-240">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="3c500-241">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="3c500-241">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="3c500-242">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="3c500-242">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c500-243">Chi phí đơn vị nguồn lực</span><span class="sxs-lookup"><span data-stu-id="3c500-243">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="3c500-244">Tiền tệ đơn vị nguồn lực</span><span class="sxs-lookup"><span data-stu-id="3c500-244">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c500-245">Bán hàng liên tổ chức</span><span class="sxs-lookup"><span data-stu-id="3c500-245">Interorganizational sales</span></span></td>
<td><span data-ttu-id="3c500-246">Tiền tệ của đơn vị hợp đồng</span><span class="sxs-lookup"><span data-stu-id="3c500-246">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c500-247">Thực tế bán hàng chưa lập hóa đơn – Có thể tính phí cho số lượng mới</span><span class="sxs-lookup"><span data-stu-id="3c500-247">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="3c500-248">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3c500-248">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c500-249">Thực tế bán hàng chưa lập hóa đơn – Không thể tính phí cho phần chênh lệch</span><span class="sxs-lookup"><span data-stu-id="3c500-249">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="3c500-250">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3c500-250">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="3c500-251">Hóa đơn được xác nhận, số giờ có thể lập hóa đơn sẽ không thay đổi hay tăng.</span><span class="sxs-lookup"><span data-stu-id="3c500-251">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="3c500-252">Đảo ngược bán hàng chưa lập hóa đơn</span><span class="sxs-lookup"><span data-stu-id="3c500-252">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="3c500-253">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3c500-253">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="3c500-254">Doanh số đã lập hóa đơn cho mốc quan trọng</span><span class="sxs-lookup"><span data-stu-id="3c500-254">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="3c500-255">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3c500-255">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="3c500-256">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="3c500-256">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="3c500-257">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="3c500-257">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c500-258">Doanh số đã lập hóa đơn</span><span class="sxs-lookup"><span data-stu-id="3c500-258">Billed sales</span></span></td>
<td><span data-ttu-id="3c500-259">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3c500-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="3c500-260">Hóa đơn được xác nhận, số giờ có thể lập hóa đơn giảm.</span><span class="sxs-lookup"><span data-stu-id="3c500-260">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="3c500-261">Đảo ngược bán hàng chưa lập hóa đơn</span><span class="sxs-lookup"><span data-stu-id="3c500-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="3c500-262">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3c500-262">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="3c500-263">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="3c500-263">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="3c500-264">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="3c500-264">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="3c500-265">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="3c500-265">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="3c500-266">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="3c500-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c500-267">Doanh số chưa lập hóa đơn – Có thể tính phí cho số lượng mới</span><span class="sxs-lookup"><span data-stu-id="3c500-267">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="3c500-268">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3c500-268">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c500-269">Doanh số chưa lập hóa đơn – Không thể tính phí cho phần chênh lệch</span><span class="sxs-lookup"><span data-stu-id="3c500-269">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="3c500-270">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3c500-270">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="3c500-271">Hóa đơn được sửa để tăng số lượng có thể tính phí.</span><span class="sxs-lookup"><span data-stu-id="3c500-271">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="3c500-272">Doanh số đã tính phí – Đảo ngược</span><span class="sxs-lookup"><span data-stu-id="3c500-272">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="3c500-273">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3c500-273">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="3c500-274">Đảo ngược doanh số đã lập hóa đơn cho mốc quan trọng</span><span class="sxs-lookup"><span data-stu-id="3c500-274">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="3c500-275">Thay đổi trạng thái mốc quan trọng từ <strong>Đã lập hóa đơn</strong> thành <strong>Sẵn sàng lập hóa đơn</strong></span><span class="sxs-lookup"><span data-stu-id="3c500-275">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="3c500-276">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3c500-276">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="3c500-277">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="3c500-277">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="3c500-278">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="3c500-278">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c500-279">Doanh số đã lập hóa đơn</span><span class="sxs-lookup"><span data-stu-id="3c500-279">Billed sales</span></span></td>
<td><span data-ttu-id="3c500-280">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3c500-280">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="3c500-281">Hóa đơn được sửa để giảm số lượng có thể tính phí.</span><span class="sxs-lookup"><span data-stu-id="3c500-281">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="3c500-282">Doanh số đã tính phí – Đảo ngược</span><span class="sxs-lookup"><span data-stu-id="3c500-282">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="3c500-283">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3c500-283">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c500-284">Doanh số chưa lập hóa đơn cho số lượng mới</span><span class="sxs-lookup"><span data-stu-id="3c500-284">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="3c500-285">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3c500-285">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c500-286">Doanh số chưa lập hóa đơn – Có thể tính phí cho phần chênh lệch</span><span class="sxs-lookup"><span data-stu-id="3c500-286">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="3c500-287">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="3c500-287">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
