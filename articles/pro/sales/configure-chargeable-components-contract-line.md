---
title: Đặt cấu hình các thành phần có thể tính phí của mô tả hợp đồng dựa trên dự án
description: Chủ đề này cung cấp thông tin về cách thêm các thành phần có thể tính phí vào mục mô tả hợp đồng trong Hoạt động Dự án.
author: rumant
ms.date: 10/08/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b29c912828aa4af2d2d9cb47869012087cb834b4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003747"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a><span data-ttu-id="e27e2-103">Đặt cấu hình các thành phần có thể tính phí của mô tả hợp đồng dựa trên dự án</span><span class="sxs-lookup"><span data-stu-id="e27e2-103">Configure chargeable components of a project-based contract line</span></span>

<span data-ttu-id="e27e2-104">_**Áp dụng cho:** Triển khai bản đơn giản - từ thỏa thuận đến lập hóa đơn ước giá, Project Operations cho các kịch bản dựa trên tài nguyên/không lưu kho_</span><span class="sxs-lookup"><span data-stu-id="e27e2-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="e27e2-105">Một mục mô tả hợp đồng dựa trên dự án có các thành phần *bao gồm* và thành phần *có thể tính phí*.</span><span class="sxs-lookup"><span data-stu-id="e27e2-105">A project-based contract line has *included* components and *chargeable* components.</span></span>

<span data-ttu-id="e27e2-106">Thành phần bao gồm là các thành phần phải tuân theo:</span><span class="sxs-lookup"><span data-stu-id="e27e2-106">Included components are components that are subject to:</span></span>

  - <span data-ttu-id="e27e2-107">Phương thức thanh toán và phần tách của khách hàng</span><span class="sxs-lookup"><span data-stu-id="e27e2-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="e27e2-108">Giới hạn không vượt quá</span><span class="sxs-lookup"><span data-stu-id="e27e2-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="e27e2-109">Các mục thiết đặt tần suất hóa đơn được xác định trên mục mô tả hợp đồng dựa trên dự án</span><span class="sxs-lookup"><span data-stu-id="e27e2-109">Invoice frequency settings defined on the project-based contract line</span></span>

<span data-ttu-id="e27e2-110">Một tập con các thành phần bao gồm có thể được đánh dấu là có thể tính phí bằng trường **Loại thanh toán**.</span><span class="sxs-lookup"><span data-stu-id="e27e2-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="e27e2-111">Trường **Loại thanh toán** là một bộ tùy chọn cho phép thiết lập các giá trị sau trong bối cảnh mục mô tả hợp đồng:</span><span class="sxs-lookup"><span data-stu-id="e27e2-111">The **Billing Type** field is an option-set that allows the following values in the context of a contract line:</span></span>

  - <span data-ttu-id="e27e2-112">Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="e27e2-112">Chargeable</span></span>
  - <span data-ttu-id="e27e2-113">Không thể tính phí</span><span class="sxs-lookup"><span data-stu-id="e27e2-113">Non-chargeable</span></span>

<span data-ttu-id="e27e2-114">Các thành phần có thể tính phí có thể được xác định trên nhiệm vụ, vai trò và danh mục giao dịch.</span><span class="sxs-lookup"><span data-stu-id="e27e2-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="e27e2-115">Khả năng tính phí được xác định trên các nhiệm vụ cho một mục mô tả hợp đồng dự án và áp dụng cho tất cả các lớp giao dịch có trong mục mô tả này.</span><span class="sxs-lookup"><span data-stu-id="e27e2-115">Chargeability is defined on tasks for a project contract line and applies to all transaction classes included on the line.</span></span> <span data-ttu-id="e27e2-116">Nếu trường **Bao gồm nhiệm vụ** trên một mục mô tả hợp đồng bị để trống hoặc được đặt thành **Toàn bộ dự án**, thì tab **Nhiệm vụ có thể tính phí** sẽ không khả dụng.</span><span class="sxs-lookup"><span data-stu-id="e27e2-116">If the **Include Tasks** field on a contract line is blank or set to **Entire project**, the **Chargeable tasks** tab will not be available.</span></span>

<span data-ttu-id="e27e2-117">Khả năng tính phí được xác định trên các vai trò cho một mục mô tả hợp đồng dự án và chỉ áp dụng cho lớp giao dịch **Thời gian**.</span><span class="sxs-lookup"><span data-stu-id="e27e2-117">Chargeability defined on roles for a project contract line only applies to the **Time** transaction class.</span></span> <span data-ttu-id="e27e2-118">Nếu trường **Bao gồm thời gian** trên một mục mô tả hợp đồng dự án được đặt thành **Không**, thì tab **Vai trò có thể tính phí** sẽ không khả dụng.</span><span class="sxs-lookup"><span data-stu-id="e27e2-118">If the **Include Time** field on a contract line is set to **No**, the **Chargeable roles** tab will not be available.</span></span>

<span data-ttu-id="e27e2-119">Khả năng tính phí được xác định trên các danh mục giao dịch cho một mục mô tả hợp đồng dự án và chỉ áp dụng cho lớp giao dịch **Chi phí**.</span><span class="sxs-lookup"><span data-stu-id="e27e2-119">Chargeability defined on transaction categories for a project contract line only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="e27e2-120">Nếu trường **Bao gồm chi phí** được đặt thành **Không**, thì tab **Danh mục có thể tính phí** sẽ không khả dụng.</span><span class="sxs-lookup"><span data-stu-id="e27e2-120">If the **Include Expenses** field is set to **No**, the **Chargeable Categories** tab will not be available.</span></span>

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a><span data-ttu-id="e27e2-121">Cập nhật nhiệm vụ dự án thành dạng có thể tính phí hoặc không thể tính phí</span><span class="sxs-lookup"><span data-stu-id="e27e2-121">Update a project task as chargeable or non-chargeable</span></span>

<span data-ttu-id="e27e2-122">Một nhiệm vụ dự án có thể là nhiệm vụ phải chịu phí tổn hoặc không phải chịu phí tổn trên một mục mô tả hợp đồng cụ thể, vì vậy, có thể có các cách thiết lập sau đây:</span><span class="sxs-lookup"><span data-stu-id="e27e2-122">A project task can be chargeable or non-chargeable on a specific contract line, which makes the following setup possible:</span></span>

<span data-ttu-id="e27e2-123">Nếu một mục mô tả hợp đồng dựa trên dự án có **Thời gian** và một nhiệm vụ nhất định, thì **T1** sẽ được liên kết với mục đó dưới dạng có thể tính phí.</span><span class="sxs-lookup"><span data-stu-id="e27e2-123">If a project-based contract line includes **Time** and a certain task, **T1** is associated to it as chargeable.</span></span> <span data-ttu-id="e27e2-124">Nếu có mục mô tả hợp đồng thứ hai bao gồm **Chi phí**, thì bạn có thể liên kết nhiệm vụ T1 trên mục mô tả hợp đồng dưới dạng không thể tính phí.</span><span class="sxs-lookup"><span data-stu-id="e27e2-124">If there is a second contract line that includes **Expense**, you can associate the T1 task on the contract line as non-chargeable.</span></span> <span data-ttu-id="e27e2-125">Kết quả là toàn bộ thời gian được ghi lại trong nhiệm vụ đều là dạng có thể tính phí và tất cả các chi phí là dạng không thể tính phí.</span><span class="sxs-lookup"><span data-stu-id="e27e2-125">The result is that all of the time recorded on the task is chargeable and all expenses are non-chargeable.</span></span>

<span data-ttu-id="e27e2-126">Loại thanh toán của nhiệm vụ có thể được đặt cấu hình trên tab **Nhiệm vụ có thể tính phí** của mô tả hợp đồng bằng cách cập nhật trường **Loại thanh toán** trên lưới con nhiệm vụ trong mô tả hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="e27e2-126">A task's billing type can be configured on the **Chargeable Tasks** tab of the contract line by updating the **Billing Type** field on the contract line tasks subgrid.</span></span> <span data-ttu-id="e27e2-127">Ngoài ra, bạn có thể cập nhật trường **Loại thanh toán** trên lưới con của nhiệm vụ Thiết lập thanh toán trong một dự án hiển thị mô tả hợp đồng được liên kết với một nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="e27e2-127">Alternatively, you can update the **Billing Type** field on the subgrid of the task Billing setup of a project that shows the contract lines associated to a task.</span></span>

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a><span data-ttu-id="e27e2-128">Cập nhật vai trò thành dạng có thể tính phí hoặc không thể tính phí</span><span class="sxs-lookup"><span data-stu-id="e27e2-128">Update a role as chargeable or non-chargeable</span></span>

<span data-ttu-id="e27e2-129">Một vai trò có thể là dạng có thể tính phí hoặc không thể tính phí trên một mục mô tả hợp đồng cụ thể.</span><span class="sxs-lookup"><span data-stu-id="e27e2-129">A role can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="e27e2-130">Bạn có thể đặt cấu hình loại thanh toán của một vai trò trên tab **Vai trò có thể tính phí** của mục mô tả hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="e27e2-130">A role's billing type can be configured on the **Chargeable Roles** tab of a contract line.</span></span> <span data-ttu-id="e27e2-131">Để làm điều này, hãy cập nhật trường **Loại thanh toán** trên lưới con **Vai trò có thể tính phí**.</span><span class="sxs-lookup"><span data-stu-id="e27e2-131">To do this, update the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a><span data-ttu-id="e27e2-132">Cập nhật danh mục giao dịch thành dạng có thể tính phí hoặc không thể tính phí</span><span class="sxs-lookup"><span data-stu-id="e27e2-132">Update a transaction category as chargeable or non-chargeable</span></span>

<span data-ttu-id="e27e2-133">Một danh mục giao dịch có thể là dạng có thể tính phí hoặc không thể tính phí trên một mục mô tả hợp đồng cụ thể.</span><span class="sxs-lookup"><span data-stu-id="e27e2-133">A transaction category can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="e27e2-134">Bạn có thể đặt cấu hình loại thanh toán của một giao dịch trên tab **Danh mục có thể tính phí** của mục mô tả hợp đồng dựa trên dự án.</span><span class="sxs-lookup"><span data-stu-id="e27e2-134">A transaction's billing type can be configured on the **Chargeable Categories** tab of a project-based contract line.</span></span> <span data-ttu-id="e27e2-135">Để làm điều này, hãy cập nhật trường **Loại thanh toán** trên lưới con **Thể loại có thể tính phí**.</span><span class="sxs-lookup"><span data-stu-id="e27e2-135">To do this, update the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="e27e2-136">Giải quyết khả năng tính phí</span><span class="sxs-lookup"><span data-stu-id="e27e2-136">Resolve chargeability</span></span>

<span data-ttu-id="e27e2-137">Một giá trị ước tính hoặc thực tế được tạo cho thời gian chỉ được coi là phải chịu phí tổn nếu:</span><span class="sxs-lookup"><span data-stu-id="e27e2-137">An estimate or actual created for time is only considered chargeable if:</span></span>

   - <span data-ttu-id="e27e2-138">**Thời gian** được thêm vào mô tả hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="e27e2-138">**Time** is included on the contract line.</span></span>
   - <span data-ttu-id="e27e2-139">**Vai trò** được đặt cấu hình là phải chịu phí tổn trên mô tả hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="e27e2-139">**Role** is configured as chargeable on the contract line.</span></span>
   - <span data-ttu-id="e27e2-140">**Các nhiệm vụ được đưa vào** được đặt thành **Các nhiệm vụ đã chọn** trên mô tả hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="e27e2-140">**Included Tasks** is set to **Selected tasks** on the contract line.</span></span>
 
 <span data-ttu-id="e27e2-141">Nếu ba điều này là đúng, thì nhiệm vụ được đặt cấu hình là phải chịu phí tổn.</span><span class="sxs-lookup"><span data-stu-id="e27e2-141">If these three things are true, the task is configured as chargeable.</span></span> 

<span data-ttu-id="e27e2-142">Một giá trị ước tính hoặc thực tế được tạo cho chi phí chỉ được coi là phải chịu phí tổn nếu:</span><span class="sxs-lookup"><span data-stu-id="e27e2-142">An estimate or actual created for expense is only considered chargeable if:</span></span>

   - <span data-ttu-id="e27e2-143">**Chi phí** được thêm vào mô tả hợp đồng</span><span class="sxs-lookup"><span data-stu-id="e27e2-143">**Expense** is included on the contract line</span></span>
   - <span data-ttu-id="e27e2-144">**Thể loại giao dịch** được đặt cấu hình là phải chịu phí tổn trên mô tả hợp đồng</span><span class="sxs-lookup"><span data-stu-id="e27e2-144">**Transaction category** is configured as chargeable on the contract line</span></span>
   - <span data-ttu-id="e27e2-145">**Các nhiệm vụ được đưa vào** được đặt thành **Nhiệm vụ đã chọn** trên mô tả hợp đồng</span><span class="sxs-lookup"><span data-stu-id="e27e2-145">**Included Tasks** is set to **Selected task** on the contract line</span></span>
  
 <span data-ttu-id="e27e2-146">Nếu ba điều này là đúng, thì **Nhiệm vụ** được đặt cấu hình là phí tổn phải trả.</span><span class="sxs-lookup"><span data-stu-id="e27e2-146">If these three things are true, the **Task** is configured as chargeable.</span></span> 

<span data-ttu-id="e27e2-147">Một số liệu ước tính hoặc số liệu thực tế được tạo cho vật tư chỉ được coi là phí tổn phải trả nếu:</span><span class="sxs-lookup"><span data-stu-id="e27e2-147">An estimate or actual created for material is only considered chargeable if:</span></span>

   - <span data-ttu-id="e27e2-148">**Vật tư** được thêm vào mô tả hợp đồng</span><span class="sxs-lookup"><span data-stu-id="e27e2-148">**Materials** is included on the contract line</span></span>
   - <span data-ttu-id="e27e2-149">**Các nhiệm vụ được đưa vào** được đặt thành **Các nhiệm vụ đã chọn** trên mô tả hợp đồng</span><span class="sxs-lookup"><span data-stu-id="e27e2-149">**Included Tasks** is set to **Selected tasks** on the contract line</span></span>

<span data-ttu-id="e27e2-150">Nếu hai điều này là đúng, thì **Nhiệm vụ** được đặt cấu hình là phí tổn phải trả.</span><span class="sxs-lookup"><span data-stu-id="e27e2-150">If these two things are true, the **Task** is configured as chargeable.</span></span> 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="e27e2-151">
                    <strong>Bao gồm thời gian</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e27e2-151">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="e27e2-152">
                    <strong>Bao gồm chi phí</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="e27e2-152">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="e27e2-153">
                    <strong>Bao gồm vật tư</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="e27e2-153">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="e27e2-154">
                    <strong>Các tác vụ được đưa vào</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="e27e2-154">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="e27e2-155">
                    <strong>Vai trò</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="e27e2-155">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="e27e2-156">
                    <strong>Danh mục</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="e27e2-156">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="e27e2-157">
                    <strong>Tác vụ</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="e27e2-157">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="e27e2-158">
                    <strong>Tác động đến khả năng phải chịu phí tổn</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e27e2-158">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e27e2-159">Có</span><span class="sxs-lookup"><span data-stu-id="e27e2-159">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="e27e2-160">Có</span><span class="sxs-lookup"><span data-stu-id="e27e2-160">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="e27e2-161">Có</span><span class="sxs-lookup"><span data-stu-id="e27e2-161">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="e27e2-162">Toàn bộ dự án</span><span class="sxs-lookup"><span data-stu-id="e27e2-162">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e27e2-163">Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="e27e2-163">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e27e2-164">Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="e27e2-164">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e27e2-165">Không thể đặt</span><span class="sxs-lookup"><span data-stu-id="e27e2-165">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="e27e2-166">Thanh toán theo giá trị thời gian thực tế: <strong>Phải chịu phí tổn</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e27e2-166">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="e27e2-167">Loại thanh toán theo giá trị chi phí thực tế: <strong>Phải chịu phí tổn</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e27e2-167">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="e27e2-168">Loại thanh toán theo giá trị vật tư thực tế: <strong>Phải chịu phí tổn</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e27e2-168">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e27e2-169">Có</span><span class="sxs-lookup"><span data-stu-id="e27e2-169">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="e27e2-170">Có</span><span class="sxs-lookup"><span data-stu-id="e27e2-170">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="e27e2-171">Có</span><span class="sxs-lookup"><span data-stu-id="e27e2-171">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="e27e2-172">Chỉ các tác vụ được chọn</span><span class="sxs-lookup"><span data-stu-id="e27e2-172">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e27e2-173">Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="e27e2-173">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e27e2-174">Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="e27e2-174">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e27e2-175">Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="e27e2-175">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="e27e2-176">Thanh toán theo giá trị thời gian thực tế: <strong>Phải chịu phí tổn</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e27e2-176">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="e27e2-177">Loại thanh toán theo giá trị chi phí thực tế: <strong>Phải chịu phí tổn</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e27e2-177">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="e27e2-178">Loại thanh toán theo giá trị vật tư thực tế: <strong>Phải chịu phí tổn</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e27e2-178">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e27e2-179">Có</span><span class="sxs-lookup"><span data-stu-id="e27e2-179">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="e27e2-180">Có</span><span class="sxs-lookup"><span data-stu-id="e27e2-180">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="e27e2-181">Có</span><span class="sxs-lookup"><span data-stu-id="e27e2-181">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="e27e2-182">Chỉ các tác vụ được chọn</span><span class="sxs-lookup"><span data-stu-id="e27e2-182">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="e27e2-183">
                    <strong>Không phải chịu phí tổn</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e27e2-183">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e27e2-184">Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="e27e2-184">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e27e2-185">Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="e27e2-185">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="e27e2-186">Thanh toán theo giá trị thời gian thực tế: <strong>Không phải chịu phí tổn</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e27e2-186">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="e27e2-187">Loại thanh toán theo giá trị chi phí thực tế: Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="e27e2-187">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="e27e2-188">Loại thanh toán theo giá trị vật tư thực tế: Phải chịu phí tổn</span><span class="sxs-lookup"><span data-stu-id="e27e2-188">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e27e2-189">Có</span><span class="sxs-lookup"><span data-stu-id="e27e2-189">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="e27e2-190">Có</span><span class="sxs-lookup"><span data-stu-id="e27e2-190">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="e27e2-191">Có</span><span class="sxs-lookup"><span data-stu-id="e27e2-191">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="e27e2-192">Chỉ các tác vụ được chọn</span><span class="sxs-lookup"><span data-stu-id="e27e2-192">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e27e2-193">Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="e27e2-193">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e27e2-194">Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="e27e2-194">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="e27e2-195">
                    <strong>Không phải chịu phí tổn</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e27e2-195">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="e27e2-196">Thanh toán theo giá trị thời gian thực tế: <strong>Không phải chịu phí tổn</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e27e2-196">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="e27e2-197">Loại thanh toán theo giá trị chi phí thực tế: <strong>Không phải chịu phí tổn</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e27e2-197">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="e27e2-198">Loại thanh toán theo giá trị vật tư thực tế: <strong>Không phải chịu phí tổn</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e27e2-198">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e27e2-199">Có</span><span class="sxs-lookup"><span data-stu-id="e27e2-199">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="e27e2-200">Có</span><span class="sxs-lookup"><span data-stu-id="e27e2-200">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="e27e2-201">Có</span><span class="sxs-lookup"><span data-stu-id="e27e2-201">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="e27e2-202">Chỉ các tác vụ được chọn</span><span class="sxs-lookup"><span data-stu-id="e27e2-202">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="e27e2-203">
                    <strong>Không phải chịu phí tổn</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e27e2-203">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e27e2-204">Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="e27e2-204">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="e27e2-205">
                    <strong>Không phải chịu phí tổn</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e27e2-205">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="e27e2-206">Thanh toán theo giá trị thời gian thực tế: <strong>Không phải chịu phí tổn</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e27e2-206">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="e27e2-207">Loại thanh toán theo giá trị chi phí thực tế: <strong>Không phải chịu phí tổn</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e27e2-207">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="e27e2-208">Loại thanh toán theo giá trị vật tư thực tế: <strong>Không phải chịu phí tổn</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e27e2-208">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e27e2-209">Có</span><span class="sxs-lookup"><span data-stu-id="e27e2-209">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="e27e2-210">Có</span><span class="sxs-lookup"><span data-stu-id="e27e2-210">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="e27e2-211">Có</span><span class="sxs-lookup"><span data-stu-id="e27e2-211">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="e27e2-212">Chỉ các tác vụ được chọn</span><span class="sxs-lookup"><span data-stu-id="e27e2-212">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="e27e2-213">
                    <strong>Không phải chịu phí tổn</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e27e2-213">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="e27e2-214">
                    <strong>Không phải chịu phí tổn</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e27e2-214">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e27e2-215">Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="e27e2-215">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="e27e2-216">Thanh toán theo giá trị thời gian thực tế: <strong>Không phải chịu phí tổn</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e27e2-216">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="e27e2-217">Loại thanh toán theo giá trị chi phí thực tế: <strong>Không phải chịu phí tổn</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e27e2-217">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="e27e2-218">Loại thanh toán theo giá trị vật tư thực tế: Phải chịu phí tổn</span><span class="sxs-lookup"><span data-stu-id="e27e2-218">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="e27e2-219">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e27e2-219">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="e27e2-220">Có</span><span class="sxs-lookup"><span data-stu-id="e27e2-220">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="e27e2-221">Có</span><span class="sxs-lookup"><span data-stu-id="e27e2-221">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="e27e2-222">Toàn bộ dự án</span><span class="sxs-lookup"><span data-stu-id="e27e2-222">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e27e2-223">Không thể đặt</span><span class="sxs-lookup"><span data-stu-id="e27e2-223">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="e27e2-224">
                    <strong>Có thể tính phí</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e27e2-224">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e27e2-225">Không thể đặt</span><span class="sxs-lookup"><span data-stu-id="e27e2-225">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="e27e2-226">Thanh toán theo giá trị thời gian thực tế: <strong>Không khả dụng</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e27e2-226">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="e27e2-227">Loại thanh toán theo giá trị chi phí thực tế: Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="e27e2-227">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="e27e2-228">Loại thanh toán theo giá trị vật tư thực tế: Phải chịu phí tổn</span><span class="sxs-lookup"><span data-stu-id="e27e2-228">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="e27e2-229">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e27e2-229">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="e27e2-230">Có</span><span class="sxs-lookup"><span data-stu-id="e27e2-230">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="e27e2-231">Có</span><span class="sxs-lookup"><span data-stu-id="e27e2-231">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="e27e2-232">Toàn bộ dự án</span><span class="sxs-lookup"><span data-stu-id="e27e2-232">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e27e2-233">Không thể đặt</span><span class="sxs-lookup"><span data-stu-id="e27e2-233">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="e27e2-234">
                    <strong>Không phải chịu phí tổn</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e27e2-234">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e27e2-235">Không thể đặt</span><span class="sxs-lookup"><span data-stu-id="e27e2-235">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="e27e2-236">Thanh toán theo giá trị thời gian thực tế: <strong>Không khả dụng</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e27e2-236">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="e27e2-237">Loại thanh toán theo giá trị chi phí thực tế: <strong>Không phải chịu phí tổn</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e27e2-237">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="e27e2-238">Loại thanh toán theo giá trị vật tư thực tế: Phải chịu phí tổn</span><span class="sxs-lookup"><span data-stu-id="e27e2-238">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e27e2-239">Có</span><span class="sxs-lookup"><span data-stu-id="e27e2-239">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="e27e2-240">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e27e2-240">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="e27e2-241">Có</span><span class="sxs-lookup"><span data-stu-id="e27e2-241">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="e27e2-242">Toàn bộ dự án</span><span class="sxs-lookup"><span data-stu-id="e27e2-242">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e27e2-243">Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="e27e2-243">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e27e2-244">Không thể đặt</span><span class="sxs-lookup"><span data-stu-id="e27e2-244">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e27e2-245">Không thể đặt</span><span class="sxs-lookup"><span data-stu-id="e27e2-245">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="e27e2-246">Thanh toán theo giá trị thời gian thực tế: Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="e27e2-246">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="e27e2-247">Loại thanh toán theo giá trị chi phí thực tế:<strong> Không khả dụng</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e27e2-247">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="e27e2-248">Loại thanh toán theo giá trị vật tư thực tế: Phải chịu phí tổn</span><span class="sxs-lookup"><span data-stu-id="e27e2-248">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e27e2-249">Có</span><span class="sxs-lookup"><span data-stu-id="e27e2-249">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="e27e2-250">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e27e2-250">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="e27e2-251">Có</span><span class="sxs-lookup"><span data-stu-id="e27e2-251">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="e27e2-252">Toàn bộ dự án</span><span class="sxs-lookup"><span data-stu-id="e27e2-252">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="e27e2-253">
                    <strong>Không phải chịu phí tổn</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e27e2-253">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e27e2-254">Không thể đặt</span><span class="sxs-lookup"><span data-stu-id="e27e2-254">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e27e2-255">Không thể đặt</span><span class="sxs-lookup"><span data-stu-id="e27e2-255">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="e27e2-256">Thanh toán theo giá trị thời gian thực tế: <strong>Không phải chịu phí tổn</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e27e2-256">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="e27e2-257">Loại thanh toán theo giá trị chi phí thực tế:<strong> Không khả dụng</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e27e2-257">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="e27e2-258">Loại thanh toán theo giá trị vật tư thực tế: Phải chịu phí tổn</span><span class="sxs-lookup"><span data-stu-id="e27e2-258">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e27e2-259">Có</span><span class="sxs-lookup"><span data-stu-id="e27e2-259">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="e27e2-260">Có</span><span class="sxs-lookup"><span data-stu-id="e27e2-260">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="e27e2-261">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e27e2-261">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="e27e2-262">Toàn bộ dự án</span><span class="sxs-lookup"><span data-stu-id="e27e2-262">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e27e2-263">Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="e27e2-263">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e27e2-264">Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="e27e2-264">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e27e2-265">Không thể đặt</span><span class="sxs-lookup"><span data-stu-id="e27e2-265">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="e27e2-266">Thanh toán theo giá trị thời gian thực tế: Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="e27e2-266">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="e27e2-267">Loại thanh toán theo giá trị chi phí thực tế: Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="e27e2-267">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="e27e2-268">Loại thanh toán theo giá trị vật tư thực tế: <strong>Không khả dụng</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e27e2-268">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e27e2-269">Có</span><span class="sxs-lookup"><span data-stu-id="e27e2-269">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="e27e2-270">Có</span><span class="sxs-lookup"><span data-stu-id="e27e2-270">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="e27e2-271">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e27e2-271">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="e27e2-272">Toàn bộ dự án</span><span class="sxs-lookup"><span data-stu-id="e27e2-272">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="e27e2-273">
                    <strong>Không phải chịu phí tổn</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e27e2-273">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="e27e2-274">
                    <strong>Không thể tính phí</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e27e2-274">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e27e2-275">Không thể đặt</span><span class="sxs-lookup"><span data-stu-id="e27e2-275">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="e27e2-276">Thanh toán theo giá trị thời gian thực tế: <strong>Không phải chịu phí tổn</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e27e2-276">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="e27e2-277">Loại thanh toán theo giá trị chi phí thực tế:<strong> Không phải chịu phí tổn</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e27e2-277">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="e27e2-278">Loại thanh toán theo giá trị vật tư thực tế:<strong> Không khả dụng</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e27e2-278">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
