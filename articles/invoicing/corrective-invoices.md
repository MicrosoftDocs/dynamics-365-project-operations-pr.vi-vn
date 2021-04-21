---
title: Tạo hóa đơn hiệu chỉnh dựa trên dự án
description: Chủ đề này cung cấp thông tin về hóa đơn hiệu chỉnh trong Project Operations.
author: rumant
manager: Annbe
ms.date: 03/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 32772d64b3fc77f0af9618edff40e3b295593454
ms.sourcegitcommit: 504c09365bf404c1f1aa9b5034c1e1e5bc9d0d54
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788910"
---
# <a name="create-corrective-project-based-invoices"></a><span data-ttu-id="5c830-103">Tạo hóa đơn hiệu chỉnh dựa trên dự án</span><span class="sxs-lookup"><span data-stu-id="5c830-103">Create corrective project-based invoices</span></span> 

<span data-ttu-id="5c830-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_</span><span class="sxs-lookup"><span data-stu-id="5c830-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="5c830-105">Hóa đơn dự án đã xác nhận có thể được hiệu chỉnh để xử lý các thay đổi hoặc tín dụng theo như sự thương lượng với khách hàng và người quản lý dự án.</span><span class="sxs-lookup"><span data-stu-id="5c830-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="5c830-106">Để chỉnh sửa hóa đơn đã xác nhận, hãy mở hóa đơn đã xác nhận và chọn **Sửa chữa hóa đơn này**.</span><span class="sxs-lookup"><span data-stu-id="5c830-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="5c830-107">Mục lựa chọn này sẽ không khả dụng cho đến khi hóa đơn dự án được xác nhận.</span><span class="sxs-lookup"><span data-stu-id="5c830-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="5c830-108">Một hóa đơn nháp mới được tạo từ hóa đơn đã xác nhận.</span><span class="sxs-lookup"><span data-stu-id="5c830-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="5c830-109">Tất cả các chi tiết mô tả hóa đơn từ hóa đơn đã được xác nhận trước đây sẽ được sao chép vào hóa đơn nháp mới.</span><span class="sxs-lookup"><span data-stu-id="5c830-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="5c830-110">Sau đây là một số điểm chính để giúp bạn hiểu thêm về chi tiết mô tả trên hóa đơn mới đã sửa:</span><span class="sxs-lookup"><span data-stu-id="5c830-110">The following are some key points to help you understand more about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="5c830-111">Tất cả các số lượng được cập nhật thành không.</span><span class="sxs-lookup"><span data-stu-id="5c830-111">All quantities are updated to zero.</span></span> <span data-ttu-id="5c830-112">Điều này giả định rằng tất cả các hạng mục đưa vào hóa đơn đều được ghi có đầy đủ.</span><span class="sxs-lookup"><span data-stu-id="5c830-112">This assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="5c830-113">Nếu cần, bạn có thể cập nhật thủ công các số lượng này để phản ánh số lượng được lập hóa đơn chứ không phải số lượng được ghi có.</span><span class="sxs-lookup"><span data-stu-id="5c830-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="5c830-114">Dựa trên số lượng bạn nhập, ứng dụng sẽ tính số lượng được ghi có.</span><span class="sxs-lookup"><span data-stu-id="5c830-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="5c830-115">Số lượng này được phản ánh ở các giá trị thực tế sẽ được tạo ra khi hóa đơn hiệu chỉnh được xác nhận.</span><span class="sxs-lookup"><span data-stu-id="5c830-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="5c830-116">Nếu bạn thay đổi số tiền thuế, thì bạn phải nhập số tiền thuế chính xác chứ không phải số tiền thuế được ghi có.</span><span class="sxs-lookup"><span data-stu-id="5c830-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="5c830-117">Các phần hiệu chỉnh mốc luôn được xử lý dưới dạng tín dụng đầy đủ.</span><span class="sxs-lookup"><span data-stu-id="5c830-117">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="5c830-118">Số tiền trả trước hoặc tạm ứng có thể được hiệu chỉnh nếu khách hàng được lập hóa đơn một số tiền không chính xác.</span><span class="sxs-lookup"><span data-stu-id="5c830-118">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="5c830-119">Các mục điều hòa số tiền trả trước và tạm ứng có thể được hiệu chỉnh nếu số tiền không chính xác được sử dụng để điều hòa với các khoản phí trên hóa đơn đã xác nhận trước đây.</span><span class="sxs-lookup"><span data-stu-id="5c830-119">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5c830-120">Chi tiết mô tả hóa đơn là các sửa đổi đối với những khoản phí đã được lập hóa đơn khác có trường **Điều chỉnh** được đặt thành **Có**.</span><span class="sxs-lookup"><span data-stu-id="5c830-120">Invoice line details that are corrections to other already invoiced charges have the **Correction** field set to **Yes**.</span></span> <span data-ttu-id="5c830-121">Các hóa đơn được hiệu chỉnh chi tiết mô tả hóa đơn sẽ có một trường **Có nội dung điều chỉnh**, trường đó cũng được đặt thành **Có**.</span><span class="sxs-lookup"><span data-stu-id="5c830-121">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a><span data-ttu-id="5c830-122">Các giá trị thực tế sẽ được tạo khi xác nhận hóa đơn hiệu chỉnh</span><span class="sxs-lookup"><span data-stu-id="5c830-122">Actuals created on confirmation of a corrective invoice</span></span>

<span data-ttu-id="5c830-123">Bảng sau liệt kê các giá trị thực tế được tạo khi xác nhận hóa đơn hiệu chỉnh.</span><span class="sxs-lookup"><span data-stu-id="5c830-123">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="5c830-124">
                    <strong>Kịch bản</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5c830-124">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="5c830-125">
                    <strong>Giá trị thực tế được tạo khi xác nhận</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5c830-125">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="5c830-126">Xác nhận việc hiệu chỉnh khoản tạm ứng hoặc trả trước đã lập hóa đơn.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="5c830-126">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5c830-127">Khoản đảo ngược doanh số chưa lập hóa đơn của số tiền trả trước hoặc tạm ứng đã tạo để điều hòa.</span><span class="sxs-lookup"><span data-stu-id="5c830-127">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="5c830-128">Số tiền này là số dương vì nó có tác dụng bù cho giá trị âm được tạo ra khi số tiền trả trước hoặc tạm ứng được lập hóa đơn.</span><span class="sxs-lookup"><span data-stu-id="5c830-128">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5c830-129">Một giá trị thực tế đảo ngược doanh số đã lập hóa đơn được tạo cho số tiền trả trước hoặc tạm ứng để đảo ngược doanh số đã lập hóa đơn ban đầu.</span><span class="sxs-lookup"><span data-stu-id="5c830-129">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5c830-130">Một giá trị thực tế doanh số được lập hóa đơn mới được tạo cho số tiền đã hiệu chỉnh đối với mục mô tả hóa đơn được hiệu chỉnh dựa trên số tiền trả trước hoặc tạm ứng.</span><span class="sxs-lookup"><span data-stu-id="5c830-130">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5c830-131">Một giá trị thực tế doanh số chưa lập hóa đơn tương ứng với giá trị âm của mục mô tả hóa đơn được hiệu chỉnh dựa trên số tiền trả trước hoặc tạm ứng, sẽ được sử dụng để điều hòa.</span><span class="sxs-lookup"><span data-stu-id="5c830-131">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="5c830-132">Một mục xác nhận việc hiệu chỉnh khoản tiền trả trước hoặc tạm ứng đã điều hòa trước đây.</span><span class="sxs-lookup"><span data-stu-id="5c830-132">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5c830-133">Khoản đảo ngược doanh số chưa lập hóa đơn của số tiền trả trước hoặc tạm ứng đã tạo để điều hòa.</span><span class="sxs-lookup"><span data-stu-id="5c830-133">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="5c830-134">Số tiền này là số dương và có tác dụng bù cho giá trị âm được tạo ra khi thực hiện việc điều hòa trước đây.</span><span class="sxs-lookup"><span data-stu-id="5c830-134">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5c830-135">Một giá trị thực tế đảo ngược doanh số đã lập hóa đơn cho số tiền trên hóa đơn trước đây.</span><span class="sxs-lookup"><span data-stu-id="5c830-135">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5c830-136">Một giá trị thực tế doanh số đã lập hóa đơn mới được tạo cho số tiền trả trước hiệu chỉnh được áp dụng cho hóa đơn hiệu chỉnh.</span><span class="sxs-lookup"><span data-stu-id="5c830-136">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5c830-137">Một giá trị thực tế doanh số chưa lập hóa đơn có giá trị âm từ khoản tiền trả trước hoặc tạm ứng còn lại được hiệu chỉnh, sẽ được sử dụng để điều hòa trên các hóa đơn sau này.</span><span class="sxs-lookup"><span data-stu-id="5c830-137">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5c830-138">Lập hóa đơn toàn bộ tín dụng của giao dịch thời gian đã lập hóa đơn trước đây.</span><span class="sxs-lookup"><span data-stu-id="5c830-138">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5c830-139">Một khoản đảo ngược doanh số đã lập hóa đơn cho số giờ và số tiền trên chi tiết mô tả hóa đơn gốc cho thời gian.</span><span class="sxs-lookup"><span data-stu-id="5c830-139">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5c830-140">Một giá trị thực tế đảo ngược doanh số chưa lập hóa đơn mới cho số giờ và số tiền trên chi tiết mô tả hóa đơn gốc cho thời gian.</span><span class="sxs-lookup"><span data-stu-id="5c830-140">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="5c830-141">Lập hóa đơn một phần tín dụng trên một giao dịch thời gian.</span><span class="sxs-lookup"><span data-stu-id="5c830-141">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5c830-142">Một khoản đảo ngược doanh số đã lập hóa đơn cho số giờ và số tiền được lập hóa đơn trên chi tiết mô tả hóa đơn gốc cho thời gian.</span><span class="sxs-lookup"><span data-stu-id="5c830-142">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5c830-143">Giá trị thực tế doanh số chưa lập hóa đơn mới, có thể tính phí cho số giờ và số tiền trên chi tiết mô tả hóa đơn đã sửa, khoản đảo ngược của giá trị này và giá trị thực tế doanh số bán hàng đã lập hóa đơn tương đương.</span><span class="sxs-lookup"><span data-stu-id="5c830-143">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5c830-144">Giá trị thực tế doanh số chưa lập hóa đơn mới, có thể tính phí cho số giờ và số tiền còn lại sau khi khấu trừ các số liệu đã hiệu chỉnh trên chi tiết mô tả hóa đơn.</span><span class="sxs-lookup"><span data-stu-id="5c830-144">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5c830-145">Lập hóa đơn toàn bộ tín dụng của giao dịch chi phí đã lập hóa đơn trước đây.</span><span class="sxs-lookup"><span data-stu-id="5c830-145">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5c830-146">Một khoản đảo ngược doanh số đã lập hóa đơn cho số lượng và số tiền trên chi tiết mô tả hóa đơn gốc cho chi phí.</span><span class="sxs-lookup"><span data-stu-id="5c830-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5c830-147">Một giá trị thực tế đảo ngược doanh số chưa lập hóa đơn mới cho số lượng và số tiền trên chi tiết mô tả hóa đơn gốc cho chi phí.</span><span class="sxs-lookup"><span data-stu-id="5c830-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="5c830-148">Lập hóa đơn một phần tín dụng của giao dịch chi phí đã lập hóa đơn trước đây.</span><span class="sxs-lookup"><span data-stu-id="5c830-148">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5c830-149">Một khoản đảo ngược doanh số đã lập hóa đơn cho số lượng và số tiền được lập hóa đơn trên chi tiết mô tả hóa đơn gốc cho một chi phí.</span><span class="sxs-lookup"><span data-stu-id="5c830-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5c830-150">Giá trị thực tế doanh số chưa lập hóa đơn mới, có thể tính phí cho số lượng và số tiền trên chi tiết mô tả hóa đơn đã hiệu chỉnh, khoản đảo ngược của giá trị này và giá trị thực tế doanh số đã lập hóa đơn tương đương.</span><span class="sxs-lookup"><span data-stu-id="5c830-150">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5c830-151">Giá trị thực tế doanh số chưa lập hóa đơn mới, có thể tính phí cho số lượng và số tiền còn lại sau khi khấu trừ các số liệu đã hiệu chỉnh trên chi tiết mô tả hóa đơn.</span><span class="sxs-lookup"><span data-stu-id="5c830-151">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5c830-152">Lập hóa đơn toàn bộ tín dụng của giao dịch phí đã lập hóa đơn trước đây.</span><span class="sxs-lookup"><span data-stu-id="5c830-152">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5c830-153">Một khoản đảo ngược doanh số đã lập hóa đơn cho số lượng và số tiền trên chi tiết mô tả hóa đơn gốc cho phí.</span><span class="sxs-lookup"><span data-stu-id="5c830-153">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5c830-154">Một giá trị thực tế đảo ngược doanh số chưa lập hóa đơn mới cho số lượng và số tiền trên chi tiết mô tả hóa đơn gốc cho phí.</span><span class="sxs-lookup"><span data-stu-id="5c830-154">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5c830-155">Lập hóa đơn một phần tín dụng của giao dịch phí đã lập hóa đơn trước đây.</span><span class="sxs-lookup"><span data-stu-id="5c830-155">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5c830-156">Một khoản đảo ngược doanh số đã lập hóa đơn cho số lượng và số tiền được lập hóa đơn trên chi tiết mô tả hóa đơn gốc cho phí.</span><span class="sxs-lookup"><span data-stu-id="5c830-156">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5c830-157">Giá trị thực tế doanh số chưa lập hóa đơn mới, có thể tính phí cho số lượng và số tiền trên chi tiết mô tả hóa đơn hiệu chỉnh đã sửa, khoản đảo ngược của giá trị này và giá trị thực tế doanh số đã lập hóa đơn tương đương.</span><span class="sxs-lookup"><span data-stu-id="5c830-157">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="5c830-158">Lập hóa đơn toàn bộ tín dụng của mốc đã lập hóa đơn trước đây.</span><span class="sxs-lookup"><span data-stu-id="5c830-158">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5c830-159">Một khoản đảo ngược doanh số đã lập hóa đơn cho số giờ và số tiền trên chi tiết mô tả hóa đơn gốc cho mốc.</span><span class="sxs-lookup"><span data-stu-id="5c830-159">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="5c830-160">Trạng thái hóa đơn trên mốc được cập nhật từ <b>Đã đăng hóa đơn khách hàng</b> thành <b>Sẵn sàng lập hóa đơn</b>.</span><span class="sxs-lookup"><span data-stu-id="5c830-160">The invoice status on the milestone is updated from <b>Customer invoice posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="5c830-161">Lập hóa đơn một phần tín dụng của mốc đã lập hóa đơn trước đây.</span><span class="sxs-lookup"><span data-stu-id="5c830-161">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5c830-162">Không Được hỗ trợ</span><span class="sxs-lookup"><span data-stu-id="5c830-162">Unsupported</span></span> </p>
            </td>
        </tr>        
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
