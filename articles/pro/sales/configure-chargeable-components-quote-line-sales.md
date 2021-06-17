---
title: Đặt cấu hình các thành phần có thể tính phí của mục mô tả báo giá
description: Chủ đề này cung cấp thông tin về cách thiết lập các thành phần có thể tính phí và không thể tính phí trên mục mô tả báo giá dựa trên dự án.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c933a3800aae72624dbcbe3f06df20e5981d74d4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003792"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a><span data-ttu-id="d9457-103">Đặt cấu hình các thành phần có thể tính phí của một mô tả báo giá</span><span class="sxs-lookup"><span data-stu-id="d9457-103">Configure the chargeable components of a quote line</span></span> 

<span data-ttu-id="d9457-104">_**Áp dụng cho:** Triển khai bản đơn giản - từ thỏa thuận đến lập hóa đơn ước giá, Project Operations cho các kịch bản dựa trên tài nguyên/không lưu kho_</span><span class="sxs-lookup"><span data-stu-id="d9457-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="d9457-105">Một mục mô tả báo giá dựa trên dự án có các thành phần *bao gồm* và thành phần *có thể tính phí*.</span><span class="sxs-lookup"><span data-stu-id="d9457-105">A project-based quote line has the concept of *included* components and *chargeable* components.</span></span>

<span data-ttu-id="d9457-106">Các thành phần bao gồm phải tuân theo:</span><span class="sxs-lookup"><span data-stu-id="d9457-106">Included components are subject to:</span></span>

  - <span data-ttu-id="d9457-107">Phương thức thanh toán và phần tách của khách hàng</span><span class="sxs-lookup"><span data-stu-id="d9457-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="d9457-108">Giới hạn không vượt quá</span><span class="sxs-lookup"><span data-stu-id="d9457-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="d9457-109">Các mục thiết đặt tần suất hóa đơn được xác định trên mục mô tả báo giá dựa trên dự án</span><span class="sxs-lookup"><span data-stu-id="d9457-109">Invoice frequency settings defined on the project-based quote line</span></span>

<span data-ttu-id="d9457-110">Một tập con các thành phần bao gồm có thể được đánh dấu là có thể tính phí bằng trường **Loại thanh toán**.</span><span class="sxs-lookup"><span data-stu-id="d9457-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="d9457-111">Trường **Loại thanh toán** là một bộ tùy chọn cho phép thiết lập các giá trị sau trong bối cảnh mục mô tả báo giá:</span><span class="sxs-lookup"><span data-stu-id="d9457-111">The **Billing Type** field is an option-set that allows the following values in the context of a quote line:</span></span>

  - <span data-ttu-id="d9457-112">Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="d9457-112">Chargeable</span></span>
  - <span data-ttu-id="d9457-113">Không thể tính phí</span><span class="sxs-lookup"><span data-stu-id="d9457-113">Non-chargeable</span></span>

<span data-ttu-id="d9457-114">Các thành phần có thể tính phí có thể được xác định trên nhiệm vụ, vai trò và danh mục giao dịch.</span><span class="sxs-lookup"><span data-stu-id="d9457-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="d9457-115">Khả năng tính phí được xác định trên các nhiệm vụ cho một mục mô tả báo giá và áp dụng cho tất cả các lớp giao dịch có trong mục mô tả đó.</span><span class="sxs-lookup"><span data-stu-id="d9457-115">Chargeability is defined on the tasks for a quote line and applies to all transaction classes included on that line.</span></span> <span data-ttu-id="d9457-116">Nếu trường **Bao gồm nhiệm vụ** được đặt thành **Toàn bộ dự án** hoặc bị để trống, thì tab **Nhiệm vụ có thể tính phí** sẽ không khả dụng.</span><span class="sxs-lookup"><span data-stu-id="d9457-116">If the **Include Tasks** field is set to **Entire project** or left blank, the **Chargeable Tasks** tab isn't available.</span></span>

<span data-ttu-id="d9457-117">Khả năng tính phí được xác định trên các vai trò cho một mục mô tả báo giá và chỉ áp dụng cho lớp giao dịch **Thời gian**.</span><span class="sxs-lookup"><span data-stu-id="d9457-117">Chargeability is defined on roles for a quote line and only applies to the **Time** transaction class.</span></span> <span data-ttu-id="d9457-118">Nếu trường **Bao gồm thời gian** được đặt thành **Không** trên một mục mô tả báo giá dự án, thì tab **Vai trò có thể tính phí** sẽ không khả dụng.</span><span class="sxs-lookup"><span data-stu-id="d9457-118">If the field, **Include Time** is set to **No** on a project quote line, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="d9457-119">Khả năng tính phí được xác định trên các danh mục giao dịch cho một mục mô tả báo giá và chỉ áp dụng cho lớp giao dịch **Chi phí**.</span><span class="sxs-lookup"><span data-stu-id="d9457-119">Chargeability is defined on transaction categories for a  quote line and only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="d9457-120">Nếu trường **Bao gồm chi phí** được đặt thành **Không** trên một mục mô tả báo giá dự án, thì tab **Danh mục có thể tính phí** sẽ không khả dụng.</span><span class="sxs-lookup"><span data-stu-id="d9457-120">If the field, **Include Expenses** is set to **No** on a project quote line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="d9457-121">Cập nhật nhiệm vụ dự án thành dạng có thể tính phí hoặc không thể tính phí</span><span class="sxs-lookup"><span data-stu-id="d9457-121">Update a project task to be chargeable or non-chargeable</span></span>

<span data-ttu-id="d9457-122">Một nhiệm vụ dự án có thể là nhiệm vụ phải chịu phí tổn hoặc không phải chịu phí tổn trong bối cảnh một mục mô tả báo giá dựa trên dự án cụ thể, vì vậy, các tổ hợp sau có thể được thiết lập.</span><span class="sxs-lookup"><span data-stu-id="d9457-122">A project task can be chargeable or non-chargeable in the context of a specific project-based quote line, which makes the following setup possible.</span></span>

<span data-ttu-id="d9457-123">Nếu mục mô tả báo giá dựa trên dự án bao gồm **Thời gian** và nhiệm vụ **T1**, thì nhiệm vụ được liên kết với mục mô tả báo giá dưới dạng có thể tính phí.</span><span class="sxs-lookup"><span data-stu-id="d9457-123">If a project-based quote line includes **Time** and the task **T1**, the task is associated to the quote line as chargeable.</span></span> <span data-ttu-id="d9457-124">Nếu có mục mô tả báo giá thứ hai bao gồm **Chi phí**, thì bạn có thể liên kết nhiệm vụ **T1** trên mục mô tả báo giá dưới dạng không thể tính phí.</span><span class="sxs-lookup"><span data-stu-id="d9457-124">If there is a second quote line that includes **Expenses**, you can associate the **T1** task on the quote line as non-chargeable.</span></span> <span data-ttu-id="d9457-125">Kết quả là toàn bộ thời gian được ghi lại trong nhiệm vụ đều là dạng có thể tính phí và tất cả các chi phí được ghi lại trong nhiệm vụ đều là dạng không thể tính phí.</span><span class="sxs-lookup"><span data-stu-id="d9457-125">The result is that all time recorded on the task is chargeable and all expenses recorded on the task are non-chargeable.</span></span>

<span data-ttu-id="d9457-126">Loại thanh toán của nhiệm vụ có thể được đặt cấu hình trên tab **Nhiệm vụ có thể tính phí** của mô tả báo giá dựa trên dự án bằng cách cập nhật trường **Loại thanh toán** trên lưới con **Nhiệm vụ trong mô tả báo giá**.</span><span class="sxs-lookup"><span data-stu-id="d9457-126">A task's billing type can be configured on the **Chargeable Tasks** tab of a project-based quote line by updating the **Billing Type** field on the **Quote Line Tasks** subgrid.</span></span> <span data-ttu-id="d9457-127">Ngoài ra, bạn có thể cập nhật loại thanh toán cho nhiệm vụ dự án trong trường **Loại thanh toán** trên lưới con khi thiết lập thanh toán cho nhiệm vụ của một dự án hiển thị mô tả báo giá được liên kết với một nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="d9457-127">Alternatively, you can update the billing type for a project task in the **Billing Type** field on the subgrid on the task billing setup of a project that shows the quote lines associated to a task.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="d9457-128">Cập nhật vai trò thành dạng có thể tính phí hoặc không thể tính phí</span><span class="sxs-lookup"><span data-stu-id="d9457-128">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="d9457-129">Một vai trò có thể là dạng có thể tính phí hoặc không thể tính phí trong bối cảnh một mục mô tả báo giá dựa trên dự án cụ thể.</span><span class="sxs-lookup"><span data-stu-id="d9457-129">A role can be chargeable or non-chargeable in the context of a specific project-based quote line.</span></span>

<span data-ttu-id="d9457-130">Loại thanh toán của một vai trò có thể được đặt cấu hình trên tab **Các vai trò có thể tính phí** của mô tả báo giá bằng cách cập nhật trường **Loại thanh toán** trên lưới con **Các vai trò có thể tính phí**.</span><span class="sxs-lookup"><span data-stu-id="d9457-130">A role's billing type can be configured on the **Chargeable Roles** tab of a quote line by updating the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="d9457-131">Cập nhật danh mục giao dịch thành dạng có thể tính phí hoặc không thể tính phí</span><span class="sxs-lookup"><span data-stu-id="d9457-131">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="d9457-132">Một danh mục giao dịch có thể là dạng có thể tính phí hoặc không thể tính phí trên một mục mô tả báo giá cụ thể.</span><span class="sxs-lookup"><span data-stu-id="d9457-132">A transaction category can be chargeable or non-chargeable on a specific quote line.</span></span>

<span data-ttu-id="d9457-133">Loại thanh toán của một giao dịch có thể được đặt cấu hình trên tab **Thể loại có thể tính phí** của mô tả báo giá bằng cách cập nhật trường **Loại thanh toán** trên lưới con **Thể loại có thể tính phí**.</span><span class="sxs-lookup"><span data-stu-id="d9457-133">A transaction's billing type can be configured on the **Chargeable Categories** tab of a quote line by updating the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="d9457-134">Giải quyết khả năng tính phí</span><span class="sxs-lookup"><span data-stu-id="d9457-134">Resolve chargeability</span></span>
<span data-ttu-id="d9457-135">Một giá trị ước tính hoặc thực tế được tạo cho thời gian sẽ chỉ được coi là phải chịu phí tổn nếu:</span><span class="sxs-lookup"><span data-stu-id="d9457-135">An estimate or actual created for time will only be considered chargeable if:</span></span>

   - <span data-ttu-id="d9457-136">**Thời gian** được thêm vào mô tả báo giá.</span><span class="sxs-lookup"><span data-stu-id="d9457-136">**Time** is included on the quote line.</span></span>
   - <span data-ttu-id="d9457-137">**Vai trò** được đặt cấu hình là phải chịu phí tổn trên mô tả báo giá.</span><span class="sxs-lookup"><span data-stu-id="d9457-137">**Role** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="d9457-138">**Các nhiệm vụ được đưa vào** được đặt thành **Các nhiệm vụ đã chọn** trên mô tả báo giá.</span><span class="sxs-lookup"><span data-stu-id="d9457-138">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span> 

<span data-ttu-id="d9457-139">Nếu ba điều này là đúng, thì **Nhiệm vụ** cũng được đặt cấu hình là phải chịu phí tổn.</span><span class="sxs-lookup"><span data-stu-id="d9457-139">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="d9457-140">Một giá trị ước tính hoặc thực tế được tạo cho chi phí chỉ được coi là phải chịu phí tổn nếu:</span><span class="sxs-lookup"><span data-stu-id="d9457-140">An estimate or actual created for expense is only considered chargeable if:</span></span> 

   - <span data-ttu-id="d9457-141">**Chi phí** được thêm vào mô tả báo giá.</span><span class="sxs-lookup"><span data-stu-id="d9457-141">**Expense** is included on the quote line.</span></span>
   - <span data-ttu-id="d9457-142">**Thể loại giao dịch** được đặt cấu hình là phải chịu phí tổn trên mô tả báo giá.</span><span class="sxs-lookup"><span data-stu-id="d9457-142">**Transaction category** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="d9457-143">**Các nhiệm vụ được đưa vào** được đặt thành **Các nhiệm vụ đã chọn** trên mô tả báo giá.</span><span class="sxs-lookup"><span data-stu-id="d9457-143">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="d9457-144">Nếu ba điều này là đúng, thì **Nhiệm vụ** cũng được đặt cấu hình là phải chịu phí tổn.</span><span class="sxs-lookup"><span data-stu-id="d9457-144">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="d9457-145">Một số liệu ước tính hoặc số liệu thực tế được tạo cho vật tư sẽ chỉ được coi là phải chịu phí tổn nếu:</span><span class="sxs-lookup"><span data-stu-id="d9457-145">An estimate or actual created for material will only be considered chargeable if:</span></span>

   - <span data-ttu-id="d9457-146">**Vật tư** được thêm vào mô tả báo giá.</span><span class="sxs-lookup"><span data-stu-id="d9457-146">**Materials** is included on the quote line.</span></span>
   - <span data-ttu-id="d9457-147">**Các nhiệm vụ được đưa vào** được đặt thành **Các nhiệm vụ đã chọn** trên mô tả báo giá.</span><span class="sxs-lookup"><span data-stu-id="d9457-147">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="d9457-148">Nếu hai điều này là đúng, thì **Nhiệm vụ** cũng nên được đặt cấu hình là phải chịu phí tổn.</span><span class="sxs-lookup"><span data-stu-id="d9457-148">If these two things are true, the **Task** should also be configured as chargeable.</span></span> 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="d9457-149">
                    <strong>Bao gồm thời gian</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9457-149">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="d9457-150">
                    <strong>Bao gồm chi phí</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9457-150">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="d9457-151">
                    <strong>Bao gồm vật tư</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9457-151">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="d9457-152">
                    <strong>Các tác vụ được đưa vào</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9457-152">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="d9457-153">
                    <strong>Vai trò</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9457-153">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="d9457-154">
                    <strong>Danh mục</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9457-154">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="d9457-155">
                    <strong>Tác vụ</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9457-155">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="d9457-156">
                    <strong>Tác động đến khả năng phải chịu phí tổn</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9457-156">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d9457-157">Có</span><span class="sxs-lookup"><span data-stu-id="d9457-157">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="d9457-158">Có</span><span class="sxs-lookup"><span data-stu-id="d9457-158">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="d9457-159">Có</span><span class="sxs-lookup"><span data-stu-id="d9457-159">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d9457-160">Toàn bộ dự án</span><span class="sxs-lookup"><span data-stu-id="d9457-160">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d9457-161">Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="d9457-161">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d9457-162">Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="d9457-162">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d9457-163">Không thể đặt</span><span class="sxs-lookup"><span data-stu-id="d9457-163">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d9457-164">Thanh toán theo giá trị thời gian thực tế: Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="d9457-164">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="d9457-165">Loại thanh toán theo giá trị chi phí thực tế: Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="d9457-165">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="d9457-166">Loại thanh toán theo giá trị vật tư thực tế: Phải chịu phí tổn</span><span class="sxs-lookup"><span data-stu-id="d9457-166">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d9457-167">Có</span><span class="sxs-lookup"><span data-stu-id="d9457-167">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="d9457-168">Có</span><span class="sxs-lookup"><span data-stu-id="d9457-168">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="d9457-169">Có</span><span class="sxs-lookup"><span data-stu-id="d9457-169">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d9457-170">Chỉ các tác vụ được chọn</span><span class="sxs-lookup"><span data-stu-id="d9457-170">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d9457-171">Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="d9457-171">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d9457-172">Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="d9457-172">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d9457-173">Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="d9457-173">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d9457-174">Thanh toán theo giá trị thời gian thực tế: Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="d9457-174">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="d9457-175">Loại thanh toán theo giá trị chi phí thực tế: Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="d9457-175">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="d9457-176">Loại thanh toán theo giá trị vật tư thực tế: Phải chịu phí tổn</span><span class="sxs-lookup"><span data-stu-id="d9457-176">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d9457-177">Có</span><span class="sxs-lookup"><span data-stu-id="d9457-177">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="d9457-178">Có</span><span class="sxs-lookup"><span data-stu-id="d9457-178">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="d9457-179">Có</span><span class="sxs-lookup"><span data-stu-id="d9457-179">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d9457-180">Chỉ các tác vụ được chọn</span><span class="sxs-lookup"><span data-stu-id="d9457-180">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="d9457-181">
                    <strong>Không phải chịu phí tổn</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9457-181">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d9457-182">Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="d9457-182">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d9457-183">Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="d9457-183">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d9457-184">Thanh toán theo giá trị thời gian thực tế: <strong>Không phải chịu phí tổn</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9457-184">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d9457-185">Loại thanh toán theo giá trị chi phí thực tế: Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="d9457-185">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="d9457-186">Loại thanh toán theo giá trị vật tư thực tế: Phải chịu phí tổn</span><span class="sxs-lookup"><span data-stu-id="d9457-186">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d9457-187">Có</span><span class="sxs-lookup"><span data-stu-id="d9457-187">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="d9457-188">Có</span><span class="sxs-lookup"><span data-stu-id="d9457-188">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="d9457-189">Có</span><span class="sxs-lookup"><span data-stu-id="d9457-189">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d9457-190">Chỉ các tác vụ được chọn</span><span class="sxs-lookup"><span data-stu-id="d9457-190">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d9457-191">Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="d9457-191">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d9457-192">Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="d9457-192">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="d9457-193">
                    <strong>Không phải chịu phí tổn</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9457-193">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d9457-194">Thanh toán theo giá trị thời gian thực tế: <strong>Không phải chịu phí tổn</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9457-194">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d9457-195">Loại thanh toán theo giá trị chi phí thực tế: <strong>Không phải chịu phí tổn</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9457-195">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d9457-196">Loại thanh toán theo giá trị vật tư thực tế: <strong>Không phải chịu phí tổn</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9457-196">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d9457-197">Có</span><span class="sxs-lookup"><span data-stu-id="d9457-197">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="d9457-198">Có</span><span class="sxs-lookup"><span data-stu-id="d9457-198">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="d9457-199">Có</span><span class="sxs-lookup"><span data-stu-id="d9457-199">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d9457-200">Chỉ các tác vụ được chọn</span><span class="sxs-lookup"><span data-stu-id="d9457-200">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="d9457-201">
                    <strong>Không phải chịu phí tổn</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9457-201">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d9457-202">Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="d9457-202">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="d9457-203">
                    <strong>Không phải chịu phí tổn</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9457-203">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d9457-204">Thanh toán theo giá trị thời gian thực tế: <strong>Không phải chịu phí tổn</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9457-204">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d9457-205">Loại thanh toán theo giá trị chi phí thực tế: <strong>Không phải chịu phí tổn</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9457-205">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d9457-206">Loại thanh toán theo giá trị vật tư thực tế: <strong>Không phải chịu phí tổn</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9457-206">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d9457-207">Có</span><span class="sxs-lookup"><span data-stu-id="d9457-207">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="d9457-208">Có</span><span class="sxs-lookup"><span data-stu-id="d9457-208">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="d9457-209">Có</span><span class="sxs-lookup"><span data-stu-id="d9457-209">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d9457-210">Chỉ các tác vụ được chọn</span><span class="sxs-lookup"><span data-stu-id="d9457-210">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="d9457-211">
                    <strong>Không phải chịu phí tổn</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9457-211">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="d9457-212">
                    <strong>Không phải chịu phí tổn</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9457-212">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d9457-213">Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="d9457-213">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d9457-214">Thanh toán theo giá trị thời gian thực tế: <strong>Không phải chịu phí tổn</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9457-214">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d9457-215">Loại thanh toán theo giá trị chi phí thực tế: <strong>Không phải chịu phí tổn</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9457-215">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d9457-216">Loại thanh toán theo giá trị vật tư thực tế: Phải chịu phí tổn</span><span class="sxs-lookup"><span data-stu-id="d9457-216">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="d9457-217">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9457-217">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="d9457-218">Có</span><span class="sxs-lookup"><span data-stu-id="d9457-218">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="d9457-219">Có</span><span class="sxs-lookup"><span data-stu-id="d9457-219">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d9457-220">Toàn bộ dự án</span><span class="sxs-lookup"><span data-stu-id="d9457-220">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d9457-221">Không thể đặt</span><span class="sxs-lookup"><span data-stu-id="d9457-221">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="d9457-222">
                    <strong>Có thể tính phí</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9457-222">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d9457-223">Không thể đặt</span><span class="sxs-lookup"><span data-stu-id="d9457-223">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d9457-224">Thanh toán theo giá trị thời gian thực tế: <strong>Không khả dụng</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9457-224">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d9457-225">Loại thanh toán theo giá trị chi phí thực tế: Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="d9457-225">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="d9457-226">Loại thanh toán theo giá trị vật tư thực tế: Phải chịu phí tổn</span><span class="sxs-lookup"><span data-stu-id="d9457-226">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="d9457-227">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9457-227">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="d9457-228">Có</span><span class="sxs-lookup"><span data-stu-id="d9457-228">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="d9457-229">Có</span><span class="sxs-lookup"><span data-stu-id="d9457-229">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d9457-230">Toàn bộ dự án</span><span class="sxs-lookup"><span data-stu-id="d9457-230">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d9457-231">Không thể đặt</span><span class="sxs-lookup"><span data-stu-id="d9457-231">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="d9457-232">
                    <strong>Không phải chịu phí tổn</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9457-232">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d9457-233">Không thể đặt</span><span class="sxs-lookup"><span data-stu-id="d9457-233">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d9457-234">Thanh toán theo giá trị thời gian thực tế: <strong>Không khả dụng</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9457-234">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d9457-235">Loại thanh toán theo giá trị chi phí thực tế: <strong>Không phải chịu phí tổn</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9457-235">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d9457-236">Loại thanh toán theo giá trị vật tư thực tế: Phải chịu phí tổn</span><span class="sxs-lookup"><span data-stu-id="d9457-236">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d9457-237">Có</span><span class="sxs-lookup"><span data-stu-id="d9457-237">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="d9457-238">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9457-238">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="d9457-239">Có</span><span class="sxs-lookup"><span data-stu-id="d9457-239">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d9457-240">Toàn bộ dự án</span><span class="sxs-lookup"><span data-stu-id="d9457-240">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d9457-241">Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="d9457-241">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d9457-242">Không thể đặt</span><span class="sxs-lookup"><span data-stu-id="d9457-242">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d9457-243">Không thể đặt</span><span class="sxs-lookup"><span data-stu-id="d9457-243">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d9457-244">Thanh toán theo giá trị thời gian thực tế: Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="d9457-244">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="d9457-245">Loại thanh toán theo giá trị chi phí thực tế:<strong> Không khả dụng</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9457-245">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d9457-246">Loại thanh toán theo giá trị vật tư thực tế: Phải chịu phí tổn</span><span class="sxs-lookup"><span data-stu-id="d9457-246">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d9457-247">Có</span><span class="sxs-lookup"><span data-stu-id="d9457-247">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="d9457-248">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9457-248">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="d9457-249">Có</span><span class="sxs-lookup"><span data-stu-id="d9457-249">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d9457-250">Toàn bộ dự án</span><span class="sxs-lookup"><span data-stu-id="d9457-250">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="d9457-251">
                    <strong>Không phải chịu phí tổn</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9457-251">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d9457-252">Không thể đặt</span><span class="sxs-lookup"><span data-stu-id="d9457-252">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d9457-253">Không thể đặt</span><span class="sxs-lookup"><span data-stu-id="d9457-253">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d9457-254">Thanh toán theo giá trị thời gian thực tế: <strong>Không phải chịu phí tổn</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9457-254">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="d9457-255">Loại thanh toán theo giá trị chi phí thực tế:<strong> Không khả dụng</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9457-255">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d9457-256">Loại thanh toán theo giá trị vật tư thực tế: Phải chịu phí tổn</span><span class="sxs-lookup"><span data-stu-id="d9457-256">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d9457-257">Có</span><span class="sxs-lookup"><span data-stu-id="d9457-257">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="d9457-258">Có</span><span class="sxs-lookup"><span data-stu-id="d9457-258">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="d9457-259">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9457-259">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d9457-260">Toàn bộ dự án</span><span class="sxs-lookup"><span data-stu-id="d9457-260">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d9457-261">Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="d9457-261">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d9457-262">Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="d9457-262">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d9457-263">Không thể đặt</span><span class="sxs-lookup"><span data-stu-id="d9457-263">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d9457-264">Thanh toán theo giá trị thời gian thực tế: Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="d9457-264">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="d9457-265">Loại thanh toán theo giá trị chi phí thực tế: Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="d9457-265">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="d9457-266">Loại thanh toán theo giá trị vật tư thực tế: <strong>Không khả dụng</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9457-266">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d9457-267">Có</span><span class="sxs-lookup"><span data-stu-id="d9457-267">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="d9457-268">Có</span><span class="sxs-lookup"><span data-stu-id="d9457-268">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="d9457-269">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9457-269">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d9457-270">Toàn bộ dự án</span><span class="sxs-lookup"><span data-stu-id="d9457-270">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="d9457-271">
                    <strong>Không phải chịu phí tổn</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9457-271">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="d9457-272">
                    <strong>Không thể tính phí</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9457-272">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d9457-273">Không thể đặt</span><span class="sxs-lookup"><span data-stu-id="d9457-273">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d9457-274">Thanh toán theo giá trị thời gian thực tế: <strong>Không phải chịu phí tổn</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9457-274">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="d9457-275">Loại thanh toán theo giá trị chi phí thực tế:<strong> Không phải chịu phí tổn</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9457-275">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="d9457-276">Loại thanh toán theo giá trị vật tư thực tế:<strong> Không khả dụng</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9457-276">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
