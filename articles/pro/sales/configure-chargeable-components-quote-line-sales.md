---
title: Đặt cấu hình các thành phần có thể tính phí của một mô tả báo giá - bản đơn giản
description: Chủ đề này cung cấp thông tin về cách thiết lập các thành phần có thể tính phí và không thể tính phí trên mục mô tả báo giá dựa trên dự án.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0e293587adf15d0523bef6b7e688fdc883aba0fa
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273899"
---
# <a name="configure-the-chargeable-components-of-a-quote-line---lite"></a><span data-ttu-id="a6ac9-103">Đặt cấu hình các thành phần có thể tính phí của một mô tả báo giá - bản đơn giản</span><span class="sxs-lookup"><span data-stu-id="a6ac9-103">Configure the chargeable components of a quote line - lite</span></span>

<span data-ttu-id="a6ac9-104">_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="a6ac9-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a6ac9-105">Một mục mô tả báo giá dựa trên dự án có các thành phần *bao gồm* và thành phần *có thể tính phí*.</span><span class="sxs-lookup"><span data-stu-id="a6ac9-105">A project-based quote line has the concept of *included* components and *chargeable* components.</span></span>

<span data-ttu-id="a6ac9-106">Các thành phần bao gồm phải tuân theo:</span><span class="sxs-lookup"><span data-stu-id="a6ac9-106">Included components are subject to:</span></span>

  - <span data-ttu-id="a6ac9-107">Phương thức thanh toán và phần tách của khách hàng</span><span class="sxs-lookup"><span data-stu-id="a6ac9-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="a6ac9-108">Giới hạn không vượt quá</span><span class="sxs-lookup"><span data-stu-id="a6ac9-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="a6ac9-109">Các mục thiết đặt tần suất hóa đơn được xác định trên mục mô tả báo giá dựa trên dự án</span><span class="sxs-lookup"><span data-stu-id="a6ac9-109">Invoice frequency settings defined on the project-based quote line</span></span>

<span data-ttu-id="a6ac9-110">Một tập con các thành phần bao gồm có thể được đánh dấu là có thể tính phí bằng trường **Loại thanh toán**.</span><span class="sxs-lookup"><span data-stu-id="a6ac9-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="a6ac9-111">Trường **Loại thanh toán** là một bộ tùy chọn cho phép thiết lập các giá trị sau trong bối cảnh mục mô tả báo giá:</span><span class="sxs-lookup"><span data-stu-id="a6ac9-111">The **Billing Type** field is an option-set that allows the following values in the context of a quote line:</span></span>

  - <span data-ttu-id="a6ac9-112">Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="a6ac9-112">Chargeable</span></span>
  - <span data-ttu-id="a6ac9-113">Không thể tính phí</span><span class="sxs-lookup"><span data-stu-id="a6ac9-113">Non-chargeable</span></span>

<span data-ttu-id="a6ac9-114">Các thành phần có thể tính phí có thể được xác định trên nhiệm vụ, vai trò và danh mục giao dịch.</span><span class="sxs-lookup"><span data-stu-id="a6ac9-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="a6ac9-115">Khả năng tính phí được xác định trên các nhiệm vụ cho một mục mô tả báo giá và áp dụng cho tất cả các lớp giao dịch có trong mục mô tả đó.</span><span class="sxs-lookup"><span data-stu-id="a6ac9-115">Chargeability is defined on the tasks for a quote line and applies to all transaction classes included on that line.</span></span> <span data-ttu-id="a6ac9-116">Nếu trường **Bao gồm nhiệm vụ** được đặt thành **Toàn bộ dự án** hoặc bị để trống, thì tab **Nhiệm vụ có thể tính phí** sẽ không khả dụng.</span><span class="sxs-lookup"><span data-stu-id="a6ac9-116">If the **Include Tasks** field is set to **Entire project** or left blank, the **Chargeable Tasks** tab isn't available.</span></span>

<span data-ttu-id="a6ac9-117">Khả năng tính phí được xác định trên các vai trò cho một mục mô tả báo giá và chỉ áp dụng cho lớp giao dịch **Thời gian**.</span><span class="sxs-lookup"><span data-stu-id="a6ac9-117">Chargeability is defined on roles for a quote line and only applies to the **Time** transaction class.</span></span> <span data-ttu-id="a6ac9-118">Nếu trường **Bao gồm thời gian** được đặt thành **Không** trên một mục mô tả báo giá dự án, thì tab **Vai trò có thể tính phí** sẽ không khả dụng.</span><span class="sxs-lookup"><span data-stu-id="a6ac9-118">If the field, **Include Time** is set to **No** on a project quote line, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="a6ac9-119">Khả năng tính phí được xác định trên các danh mục giao dịch cho một mục mô tả báo giá và chỉ áp dụng cho lớp giao dịch **Chi phí**.</span><span class="sxs-lookup"><span data-stu-id="a6ac9-119">Chargeability is defined on transaction categories for a  quote line and only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="a6ac9-120">Nếu trường **Bao gồm chi phí** được đặt thành **Không** trên một mục mô tả báo giá dự án, thì tab **Danh mục có thể tính phí** sẽ không khả dụng.</span><span class="sxs-lookup"><span data-stu-id="a6ac9-120">If the field, **Include Expenses** is set to **No** on a project quote line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="a6ac9-121">Cập nhật nhiệm vụ dự án thành dạng có thể tính phí hoặc không thể tính phí</span><span class="sxs-lookup"><span data-stu-id="a6ac9-121">Update a project task to be chargeable or non-chargeable</span></span>

<span data-ttu-id="a6ac9-122">Một nhiệm vụ dự án có thể là dạng có thể tính phí hoặc không thể tính phí trong bối cảnh một mục mô tả báo giá dựa trên dự án cụ thể, vì vậy, các tổ hợp sau có thể được thiết lập:</span><span class="sxs-lookup"><span data-stu-id="a6ac9-122">A project task can be chargeable or non-chargeable in the context of a specific project-based quote line, which makes the following setup possible:</span></span>

<span data-ttu-id="a6ac9-123">Nếu mục mô tả báo giá dựa trên dự án bao gồm **Thời gian** và nhiệm vụ **T1**, thì nhiệm vụ được liên kết với mục mô tả báo giá dưới dạng có thể tính phí.</span><span class="sxs-lookup"><span data-stu-id="a6ac9-123">If a project-based quote line includes **Time** and the task **T1**, the task is associated to the quote line as chargeable.</span></span> <span data-ttu-id="a6ac9-124">Nếu có mục mô tả báo giá thứ hai bao gồm **Chi phí**, thì bạn có thể liên kết nhiệm vụ **T1** trên mục mô tả báo giá dưới dạng không thể tính phí.</span><span class="sxs-lookup"><span data-stu-id="a6ac9-124">If there is a second quote line that includes **Expenses**, you can associate the **T1** task on the quote line as non-chargeable.</span></span> <span data-ttu-id="a6ac9-125">Kết quả là toàn bộ thời gian được ghi lại trong nhiệm vụ đều là dạng có thể tính phí và tất cả các chi phí được ghi lại trong nhiệm vụ đều là dạng không thể tính phí.</span><span class="sxs-lookup"><span data-stu-id="a6ac9-125">The result is that all time recorded on the task is chargeable and all expenses recorded on the task are non-chargeable.</span></span>

<span data-ttu-id="a6ac9-126">Loại thanh toán của nhiệm vụ có thể được đặt cấu hình trên tab **Nhiệm vụ có thể tính phí** của mô tả báo giá dựa trên dự án bằng cách cập nhật trường **Loại thanh toán** trên lưới con **Nhiệm vụ trong mô tả báo giá**.</span><span class="sxs-lookup"><span data-stu-id="a6ac9-126">A task's billing type can be configured on the **Chargeable Tasks** tab of a project-based quote line by updating the **Billing Type** field on the **Quote Line Tasks** subgrid.</span></span> <span data-ttu-id="a6ac9-127">Ngoài ra, bạn có thể cập nhật loại thanh toán cho nhiệm vụ dự án trong trường **Loại thanh toán** trên lưới con khi thiết lập thanh toán cho nhiệm vụ của một dự án hiển thị mô tả báo giá được liên kết với một nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="a6ac9-127">Alternatively, you can update the billing type for a project task in the **Billing Type** field on the subgrid on the task billing setup of a project that shows the quote lines associated to a task.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="a6ac9-128">Cập nhật vai trò thành dạng có thể tính phí hoặc không thể tính phí</span><span class="sxs-lookup"><span data-stu-id="a6ac9-128">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="a6ac9-129">Một vai trò có thể là dạng có thể tính phí hoặc không thể tính phí trong bối cảnh một mục mô tả báo giá dựa trên dự án cụ thể.</span><span class="sxs-lookup"><span data-stu-id="a6ac9-129">A role can be chargeable or non-chargeable in the context of a specific project-based quote line.</span></span>

<span data-ttu-id="a6ac9-130">Loại thanh toán của một vai trò có thể được đặt cấu hình trên tab **Các vai trò có thể tính phí** của mô tả báo giá bằng cách cập nhật trường **Loại thanh toán** trên lưới con **Các vai trò có thể tính phí**.</span><span class="sxs-lookup"><span data-stu-id="a6ac9-130">A role's billing type can be configured on the **Chargeable Roles** tab of a quote line by updating the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="a6ac9-131">Cập nhật danh mục giao dịch thành dạng có thể tính phí hoặc không thể tính phí</span><span class="sxs-lookup"><span data-stu-id="a6ac9-131">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="a6ac9-132">Một danh mục giao dịch có thể là dạng có thể tính phí hoặc không thể tính phí trên một mục mô tả báo giá cụ thể.</span><span class="sxs-lookup"><span data-stu-id="a6ac9-132">A transaction category can be chargeable or non-chargeable on a specific quote line.</span></span>

<span data-ttu-id="a6ac9-133">Loại thanh toán của một giao dịch có thể được đặt cấu hình trên tab **Thể loại có thể tính phí** của mô tả báo giá bằng cách cập nhật trường **Loại thanh toán** trên lưới con **Thể loại có thể tính phí**.</span><span class="sxs-lookup"><span data-stu-id="a6ac9-133">A transaction's billing type can be configured on the **Chargeable Categories** tab of a quote line by updating the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="a6ac9-134">Giải quyết khả năng tính phí</span><span class="sxs-lookup"><span data-stu-id="a6ac9-134">Resolve chargeability</span></span>
<span data-ttu-id="a6ac9-135">Giá trị ước tính hoặc thực tế được tạo cho thời gian sẽ chỉ được coi là có thể tính phí nếu **Thời gian** được bao gồm trên mục mô tả báo giá và nếu **Nhiệm vụ**, **Vai trò** được đặt cấu hình là có thể tính phí trên mục mô tả báo giá.</span><span class="sxs-lookup"><span data-stu-id="a6ac9-135">An estimate or actual created for time will only be considered chargeable if **Time** is included on the quote line, and if **Task** and **Role** are configured as chargeable on the quote line.</span></span>

<span data-ttu-id="a6ac9-136">Giá trị ước tính hoặc thực tế được tạo cho chi phí sẽ chỉ được coi là có thể tính phí nếu **Chi phí** được bao gồm trên mục mô tả báo giá và nếu **Nhiệm vụ**, **Danh mục giao dịch** được đặt cấu hình là có thể tính phí trên mục mô tả báo giá.</span><span class="sxs-lookup"><span data-stu-id="a6ac9-136">An estimate or actual created for expense will only be considered chargeable if **Expense** is included on the quote line, and if **Task** and **Transaction Category** are configured as chargeable on the quote line.</span></span>

| <span data-ttu-id="a6ac9-137">Bao gồm thời gian</span><span class="sxs-lookup"><span data-stu-id="a6ac9-137">Includes Time</span></span> | <span data-ttu-id="a6ac9-138">Bao gồm chi phí</span><span class="sxs-lookup"><span data-stu-id="a6ac9-138">Includes Expense</span></span> | <span data-ttu-id="a6ac9-139">Các tác vụ được đưa vào</span><span class="sxs-lookup"><span data-stu-id="a6ac9-139">Included Tasks</span></span> | <span data-ttu-id="a6ac9-140">Vai trò</span><span class="sxs-lookup"><span data-stu-id="a6ac9-140">Role</span></span> | <span data-ttu-id="a6ac9-141">Danh mục</span><span class="sxs-lookup"><span data-stu-id="a6ac9-141">Category</span></span> | <span data-ttu-id="a6ac9-142">Tác vụ</span><span class="sxs-lookup"><span data-stu-id="a6ac9-142">Task</span></span> | <span data-ttu-id="a6ac9-143">Thanh toán</span><span class="sxs-lookup"><span data-stu-id="a6ac9-143">Billing</span></span> |
| --- | --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="a6ac9-144">Có</span><span class="sxs-lookup"><span data-stu-id="a6ac9-144">Yes</span></span> | <span data-ttu-id="a6ac9-145">Có</span><span class="sxs-lookup"><span data-stu-id="a6ac9-145">Yes</span></span> | <span data-ttu-id="a6ac9-146">Toàn bộ dự án</span><span class="sxs-lookup"><span data-stu-id="a6ac9-146">Entire project</span></span> | <span data-ttu-id="a6ac9-147">Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="a6ac9-147">Chargeable</span></span> | <span data-ttu-id="a6ac9-148">Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="a6ac9-148">Chargeable</span></span> | <span data-ttu-id="a6ac9-149">Không thể đặt</span><span class="sxs-lookup"><span data-stu-id="a6ac9-149">Can't be set</span></span> | <span data-ttu-id="a6ac9-150">Thanh toán theo giá trị thời gian thực tế: Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="a6ac9-150">Billing on a time actual: Chargeable</span></span> </br><span data-ttu-id="a6ac9-151">Loại thanh toán theo giá trị chi phí thực tế: Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="a6ac9-151">Billing type on expense actual: Chargeable</span></span> |
| <span data-ttu-id="a6ac9-152">Có</span><span class="sxs-lookup"><span data-stu-id="a6ac9-152">Yes</span></span> | <span data-ttu-id="a6ac9-153">Có</span><span class="sxs-lookup"><span data-stu-id="a6ac9-153">Yes</span></span> | <span data-ttu-id="a6ac9-154">Chỉ các tác vụ được chọn</span><span class="sxs-lookup"><span data-stu-id="a6ac9-154">Selected tasks only</span></span> | <span data-ttu-id="a6ac9-155">Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="a6ac9-155">Chargeable</span></span> | <span data-ttu-id="a6ac9-156">Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="a6ac9-156">Chargeable</span></span> | <span data-ttu-id="a6ac9-157">Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="a6ac9-157">Chargeable</span></span> | <span data-ttu-id="a6ac9-158">Thanh toán theo giá trị thời gian thực tế: Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="a6ac9-158">Billing on a time actual: Chargeable</span></span></br><span data-ttu-id="a6ac9-159">Loại thanh toán theo giá trị chi phí thực tế: Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="a6ac9-159">Billing type on expense actual: Chargeable</span></span> |
| <span data-ttu-id="a6ac9-160">Có</span><span class="sxs-lookup"><span data-stu-id="a6ac9-160">Yes</span></span> | <span data-ttu-id="a6ac9-161">Có</span><span class="sxs-lookup"><span data-stu-id="a6ac9-161">Yes</span></span> | <span data-ttu-id="a6ac9-162">Chỉ các tác vụ được chọn</span><span class="sxs-lookup"><span data-stu-id="a6ac9-162">Selected tasks only</span></span> | <span data-ttu-id="a6ac9-163">Không thể tính phí</span><span class="sxs-lookup"><span data-stu-id="a6ac9-163">Non-chargeable</span></span> | <span data-ttu-id="a6ac9-164">Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="a6ac9-164">Chargeable</span></span> | <span data-ttu-id="a6ac9-165">Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="a6ac9-165">Chargeable</span></span> | <span data-ttu-id="a6ac9-166">Thanh toán theo giá trị thời gian thực tế: Không thể tính phí</span><span class="sxs-lookup"><span data-stu-id="a6ac9-166">Billing on a time actual: Non-Chargeable</span></span></br><span data-ttu-id="a6ac9-167">Loại thanh toán theo giá trị chi phí thực tế: Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="a6ac9-167">Billing type on expense actual: Chargeable</span></span> |
| <span data-ttu-id="a6ac9-168">Có</span><span class="sxs-lookup"><span data-stu-id="a6ac9-168">Yes</span></span> | <span data-ttu-id="a6ac9-169">Có</span><span class="sxs-lookup"><span data-stu-id="a6ac9-169">Yes</span></span> | <span data-ttu-id="a6ac9-170">Chỉ các tác vụ được chọn</span><span class="sxs-lookup"><span data-stu-id="a6ac9-170">Selected tasks only</span></span> | <span data-ttu-id="a6ac9-171">Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="a6ac9-171">Chargeable</span></span> | <span data-ttu-id="a6ac9-172">Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="a6ac9-172">Chargeable</span></span> | <span data-ttu-id="a6ac9-173">Không thể tính phí</span><span class="sxs-lookup"><span data-stu-id="a6ac9-173">Non-Chargeable</span></span> | <span data-ttu-id="a6ac9-174">Thanh toán theo giá trị thời gian thực tế: Không thể tính phí</span><span class="sxs-lookup"><span data-stu-id="a6ac9-174">Billing on a time actual: Non-Chargeable</span></span></br> <span data-ttu-id="a6ac9-175">Loại thanh toán theo giá trị chi phí thực tế: Không thể tính phí</span><span class="sxs-lookup"><span data-stu-id="a6ac9-175">Billing type on expense actual: Non-Chargeable</span></span> |
| <span data-ttu-id="a6ac9-176">Có</span><span class="sxs-lookup"><span data-stu-id="a6ac9-176">Yes</span></span> | <span data-ttu-id="a6ac9-177">Có</span><span class="sxs-lookup"><span data-stu-id="a6ac9-177">Yes</span></span> | <span data-ttu-id="a6ac9-178">Chỉ các tác vụ được chọn</span><span class="sxs-lookup"><span data-stu-id="a6ac9-178">Selected tasks only</span></span> | <span data-ttu-id="a6ac9-179">Không thể tính phí</span><span class="sxs-lookup"><span data-stu-id="a6ac9-179">Non-Chargeable</span></span> | <span data-ttu-id="a6ac9-180">Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="a6ac9-180">Chargeable</span></span> | <span data-ttu-id="a6ac9-181">Không thể tính phí</span><span class="sxs-lookup"><span data-stu-id="a6ac9-181">Non- Chargeable</span></span> | <span data-ttu-id="a6ac9-182">Thanh toán theo giá trị thời gian thực tế: Không thể tính phí</span><span class="sxs-lookup"><span data-stu-id="a6ac9-182">Billing on a time actual: Non-Chargeable</span></span></br> <span data-ttu-id="a6ac9-183">Loại thanh toán theo giá trị chi phí thực tế: Không thể tính phí</span><span class="sxs-lookup"><span data-stu-id="a6ac9-183">Billing type on expense actual: Non-Chargeable</span></span> |
| <span data-ttu-id="a6ac9-184">Có</span><span class="sxs-lookup"><span data-stu-id="a6ac9-184">Yes</span></span> | <span data-ttu-id="a6ac9-185">Có</span><span class="sxs-lookup"><span data-stu-id="a6ac9-185">Yes</span></span> | <span data-ttu-id="a6ac9-186">Chỉ các tác vụ được chọn</span><span class="sxs-lookup"><span data-stu-id="a6ac9-186">Selected tasks only</span></span> | <span data-ttu-id="a6ac9-187">Không thể tính phí</span><span class="sxs-lookup"><span data-stu-id="a6ac9-187">Non-Chargeable</span></span> | <span data-ttu-id="a6ac9-188">Không thể tính phí</span><span class="sxs-lookup"><span data-stu-id="a6ac9-188">Non-Chargeable</span></span> | <span data-ttu-id="a6ac9-189">Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="a6ac9-189">Chargeable</span></span> | <span data-ttu-id="a6ac9-190">Thanh toán theo giá trị thời gian thực tế: Không thể tính phí</span><span class="sxs-lookup"><span data-stu-id="a6ac9-190">Billing on a time actual: Non-Chargeable</span></span></br> <span data-ttu-id="a6ac9-191">Loại thanh toán theo giá trị chi phí thực tế: Không thể tính phí</span><span class="sxs-lookup"><span data-stu-id="a6ac9-191">Billing type on expense actual: Non-Chargeable</span></span> |
| <span data-ttu-id="a6ac9-192">No</span><span class="sxs-lookup"><span data-stu-id="a6ac9-192">No</span></span> | <span data-ttu-id="a6ac9-193">Có</span><span class="sxs-lookup"><span data-stu-id="a6ac9-193">Yes</span></span> | <span data-ttu-id="a6ac9-194">Toàn bộ dự án</span><span class="sxs-lookup"><span data-stu-id="a6ac9-194">Entire project</span></span> | <span data-ttu-id="a6ac9-195">Không thể đặt</span><span class="sxs-lookup"><span data-stu-id="a6ac9-195">Can't be set</span></span> | <span data-ttu-id="a6ac9-196">Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="a6ac9-196">Chargeable</span></span> | <span data-ttu-id="a6ac9-197">Không thể đặt</span><span class="sxs-lookup"><span data-stu-id="a6ac9-197">Can't be set</span></span> | <span data-ttu-id="a6ac9-198">Thanh toán theo giá trị thời gian thực tế: Không khả dụng</span><span class="sxs-lookup"><span data-stu-id="a6ac9-198">Billing on a time actual: Not available</span></span> </br><span data-ttu-id="a6ac9-199">Loại thanh toán theo giá trị chi phí thực tế: Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="a6ac9-199">Billing type on expense actual: Chargeable</span></span> |
| <span data-ttu-id="a6ac9-200">No</span><span class="sxs-lookup"><span data-stu-id="a6ac9-200">No</span></span> | <span data-ttu-id="a6ac9-201">Có</span><span class="sxs-lookup"><span data-stu-id="a6ac9-201">Yes</span></span> | <span data-ttu-id="a6ac9-202">Toàn bộ dự án</span><span class="sxs-lookup"><span data-stu-id="a6ac9-202">Entire project</span></span> | <span data-ttu-id="a6ac9-203">Không thể đặt</span><span class="sxs-lookup"><span data-stu-id="a6ac9-203">Can't be set</span></span> | <span data-ttu-id="a6ac9-204">Không thể tính phí</span><span class="sxs-lookup"><span data-stu-id="a6ac9-204">Non-chargeable</span></span> | <span data-ttu-id="a6ac9-205">Không thể đặt</span><span class="sxs-lookup"><span data-stu-id="a6ac9-205">Can't be set</span></span> | <span data-ttu-id="a6ac9-206">Thanh toán theo giá trị thời gian thực tế: Không khả dụng</span><span class="sxs-lookup"><span data-stu-id="a6ac9-206">Billing on a time actual: Not available</span></span> </br><span data-ttu-id="a6ac9-207">Loại thanh toán theo giá trị chi phí thực tế: Không thể tính phí</span><span class="sxs-lookup"><span data-stu-id="a6ac9-207">Billing type on expense actual: Non-chargeable</span></span> |
| <span data-ttu-id="a6ac9-208">Có</span><span class="sxs-lookup"><span data-stu-id="a6ac9-208">Yes</span></span> | <span data-ttu-id="a6ac9-209">No</span><span class="sxs-lookup"><span data-stu-id="a6ac9-209">No</span></span> | <span data-ttu-id="a6ac9-210">Toàn bộ dự án</span><span class="sxs-lookup"><span data-stu-id="a6ac9-210">Entire project</span></span> | <span data-ttu-id="a6ac9-211">Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="a6ac9-211">Chargeable</span></span> | <span data-ttu-id="a6ac9-212">Không thể đặt</span><span class="sxs-lookup"><span data-stu-id="a6ac9-212">Can't be set</span></span> | <span data-ttu-id="a6ac9-213">Không thể đặt</span><span class="sxs-lookup"><span data-stu-id="a6ac9-213">Can't be set</span></span> | <span data-ttu-id="a6ac9-214">Thanh toán theo giá trị thời gian thực tế: Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="a6ac9-214">Billing on a time actual: Chargeable</span></span></br><span data-ttu-id="a6ac9-215">Loại thanh toán theo giá trị chi phí thực tế: Không khả dụng</span><span class="sxs-lookup"><span data-stu-id="a6ac9-215">Billing type on expense actual: Not available</span></span> |
| <span data-ttu-id="a6ac9-216">Có</span><span class="sxs-lookup"><span data-stu-id="a6ac9-216">Yes</span></span> | <span data-ttu-id="a6ac9-217">No</span><span class="sxs-lookup"><span data-stu-id="a6ac9-217">No</span></span> | <span data-ttu-id="a6ac9-218">Toàn bộ dự án</span><span class="sxs-lookup"><span data-stu-id="a6ac9-218">Entire project</span></span> | <span data-ttu-id="a6ac9-219">Không thể tính phí</span><span class="sxs-lookup"><span data-stu-id="a6ac9-219">Non-chargeable</span></span> | <span data-ttu-id="a6ac9-220">Không thể đặt</span><span class="sxs-lookup"><span data-stu-id="a6ac9-220">Can't be set</span></span> | <span data-ttu-id="a6ac9-221">Không thể đặt</span><span class="sxs-lookup"><span data-stu-id="a6ac9-221">Can't be set</span></span> | <span data-ttu-id="a6ac9-222">Thanh toán theo giá trị thời gian thực tế: Không thể tính phí</span><span class="sxs-lookup"><span data-stu-id="a6ac9-222">Billing on a time actual: Non-chargeable</span></span> </br><span data-ttu-id="a6ac9-223">Loại thanh toán theo giá trị chi phí thực tế: Không khả dụng</span><span class="sxs-lookup"><span data-stu-id="a6ac9-223">Billing type on expense actual: Not available</span></span> |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]