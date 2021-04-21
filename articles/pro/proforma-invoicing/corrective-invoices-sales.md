---
title: Hóa đơn hiệu chỉnh của dự án
description: Chủ đề này cung cấp thông tin về cách tạo và xác nhận các hóa đơn hiệu chỉnh trong Project Operations.
author: rumant
manager: Annbe
ms.date: 04/05/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ae6d881e4e68b9f467478afe9735fc3186e6b0a8
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866617"
---
# <a name="corrective-project-invoices"></a><span data-ttu-id="b7bcf-103">Hóa đơn hiệu chỉnh của dự án</span><span class="sxs-lookup"><span data-stu-id="b7bcf-103">Corrective project invoices</span></span>

<span data-ttu-id="b7bcf-104">_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="b7bcf-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b7bcf-105">Hóa đơn dự án đã xác nhận có thể được hiệu chỉnh để xử lý các thay đổi hoặc tín dụng theo như sự thương lượng với khách hàng và người quản lý dự án.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="b7bcf-106">Để chỉnh sửa hóa đơn đã xác nhận, hãy mở hóa đơn đã xác nhận và chọn **Sửa chữa hóa đơn này**.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="b7bcf-107">Mục lựa chọn này sẽ không khả dụng cho đến khi hóa đơn dự án được xác nhận.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="b7bcf-108">Một hóa đơn nháp mới được tạo từ hóa đơn đã xác nhận.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="b7bcf-109">Tất cả các chi tiết mô tả hóa đơn từ hóa đơn đã được xác nhận trước đây sẽ được sao chép vào hóa đơn nháp mới.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="b7bcf-110">Sau đây là một số điểm chính mà bạn cần hiểu về chi tiết mô tả trên hóa đơn được hiệu chỉnh mới:</span><span class="sxs-lookup"><span data-stu-id="b7bcf-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="b7bcf-111">Tất cả các số lượng được cập nhật thành không.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-111">All quantities are updated to zero.</span></span> <span data-ttu-id="b7bcf-112">Ứng dụng giả định rằng tất cả các mặt hàng được lập hóa đơn đều được ghi có đầy đủ.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-112">The application assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="b7bcf-113">Nếu cần, bạn có thể cập nhật thủ công các số lượng này để phản ánh số lượng được lập hóa đơn chứ không phải số lượng được ghi có.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="b7bcf-114">Dựa trên số lượng bạn nhập, ứng dụng sẽ tính số lượng được ghi có.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="b7bcf-115">Số lượng này được phản ánh ở các giá trị thực tế sẽ được tạo ra khi hóa đơn hiệu chỉnh được xác nhận.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="b7bcf-116">Nếu bạn thay đổi số tiền thuế, thì bạn phải nhập số tiền thuế chính xác chứ không phải số tiền thuế được ghi có.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="b7bcf-117">Các mục mô tả hợp đồng dựa trên sản phẩm đã xác nhận trước đây sẽ không được sao chép sang hóa đơn mới.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-117">Previously confirmed product-based contract lines are not copied over.</span></span> <span data-ttu-id="b7bcf-118">Không hỗ trợ xử lý các phần hiệu chỉnh trên hóa đơn dự án dựa trên sản phẩm.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-118">Processing corrections on a product-based project invoice is not supported.</span></span>
- <span data-ttu-id="b7bcf-119">Các phần hiệu chỉnh mốc luôn được xử lý dưới dạng tín dụng đầy đủ.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-119">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="b7bcf-120">Số tiền trả trước hoặc tạm ứng có thể được hiệu chỉnh nếu khách hàng được lập hóa đơn một số tiền không chính xác.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-120">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="b7bcf-121">Các mục điều hòa số tiền trả trước và tạm ứng có thể được hiệu chỉnh nếu số tiền không chính xác được sử dụng để điều hòa với các khoản phí trên hóa đơn đã xác nhận trước đây.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-121">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b7bcf-122">Đối với các chi tiết mô tả hóa đơn là phần hiệu chỉnh cho các khoản phí đã được lập hóa đơn khác, trường **Sửa chữa** tương ứng được đặt thành **Có**.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-122">Invoice line details that are corrections to other already invoiced charges have the field **Correction** set to **Yes**.</span></span> <span data-ttu-id="b7bcf-123">Các hóa đơn được hiệu chỉnh chi tiết mô tả hóa đơn sẽ có một trường **Có nội dung điều chỉnh**, trường đó cũng được đặt thành **Có**.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-123">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a><span data-ttu-id="b7bcf-124">Các giá trị thực tế được tạo khi xác nhận hóa đơn hiệu chỉnh</span><span class="sxs-lookup"><span data-stu-id="b7bcf-124">Actuals created when a corrective invoice is confirmed</span></span>

<span data-ttu-id="b7bcf-125">Bảng sau liệt kê các giá trị thực tế được tạo khi xác nhận hóa đơn hiệu chỉnh.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-125">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="b7bcf-126">
                    <strong>Kịch bản</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b7bcf-126">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="b7bcf-127">
                    <strong>Giá trị thực tế được tạo khi xác nhận</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b7bcf-127">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="b7bcf-128">Xác nhận việc hiệu chỉnh khoản tạm ứng hoặc trả trước đã lập hóa đơn.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="b7bcf-128">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b7bcf-129">Khoản đảo ngược doanh số chưa lập hóa đơn của số tiền trả trước hoặc tạm ứng đã tạo để điều hòa.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-129">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="b7bcf-130">Số tiền này là số dương vì nó có tác dụng bù cho giá trị âm được tạo ra khi số tiền trả trước hoặc tạm ứng được lập hóa đơn.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-130">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b7bcf-131">Một giá trị thực tế đảo ngược doanh số đã lập hóa đơn được tạo cho số tiền trả trước hoặc tạm ứng để đảo ngược doanh số đã lập hóa đơn ban đầu.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-131">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b7bcf-132">Một giá trị thực tế doanh số được lập hóa đơn mới được tạo cho số tiền đã hiệu chỉnh đối với mục mô tả hóa đơn được hiệu chỉnh dựa trên số tiền trả trước hoặc tạm ứng.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-132">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b7bcf-133">Một giá trị thực tế doanh số chưa lập hóa đơn tương ứng với giá trị âm của mục mô tả hóa đơn được hiệu chỉnh dựa trên số tiền trả trước hoặc tạm ứng, sẽ được sử dụng để điều hòa.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-133">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="b7bcf-134">Một mục xác nhận việc hiệu chỉnh khoản tiền trả trước hoặc tạm ứng đã điều hòa trước đây.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-134">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b7bcf-135">Khoản đảo ngược doanh số chưa lập hóa đơn của số tiền trả trước hoặc tạm ứng đã tạo để điều hòa.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-135">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="b7bcf-136">Số tiền này là số dương và có tác dụng bù cho giá trị âm được tạo ra khi thực hiện việc điều hòa trước đây.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-136">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b7bcf-137">Một giá trị thực tế đảo ngược doanh số đã lập hóa đơn cho số tiền trên hóa đơn trước đây.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-137">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b7bcf-138">Một giá trị thực tế doanh số đã lập hóa đơn mới được tạo cho số tiền trả trước hiệu chỉnh được áp dụng cho hóa đơn hiệu chỉnh.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-138">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b7bcf-139">Một giá trị thực tế doanh số chưa lập hóa đơn có giá trị âm từ khoản tiền trả trước hoặc tạm ứng còn lại được hiệu chỉnh, sẽ được sử dụng để điều hòa trên các hóa đơn sau này.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-139">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b7bcf-140">Lập hóa đơn toàn bộ tín dụng của giao dịch thời gian đã lập hóa đơn trước đây.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-140">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b7bcf-141">Một khoản đảo ngược doanh số đã lập hóa đơn cho số giờ và số tiền trên chi tiết mô tả hóa đơn gốc cho thời gian.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-141">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b7bcf-142">Một giá trị thực tế đảo ngược doanh số chưa lập hóa đơn mới cho số giờ và số tiền trên chi tiết mô tả hóa đơn gốc cho thời gian.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-142">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="b7bcf-143">Lập hóa đơn một phần tín dụng trên một giao dịch thời gian.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-143">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b7bcf-144">Một khoản đảo ngược doanh số đã lập hóa đơn cho số giờ và số tiền được lập hóa đơn trên chi tiết mô tả hóa đơn gốc cho thời gian.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-144">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b7bcf-145">Giá trị thực tế doanh số chưa lập hóa đơn mới, có thể tính phí cho số giờ và số tiền trên chi tiết mô tả hóa đơn đã sửa, khoản đảo ngược của giá trị này và giá trị thực tế doanh số bán hàng đã lập hóa đơn tương đương.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-145">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b7bcf-146">Giá trị thực tế doanh số chưa lập hóa đơn mới, có thể tính phí cho số giờ và số tiền còn lại sau khi khấu trừ các số liệu đã hiệu chỉnh trên chi tiết mô tả hóa đơn.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-146">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b7bcf-147">Lập hóa đơn toàn bộ tín dụng của giao dịch chi phí đã lập hóa đơn trước đây.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-147">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b7bcf-148">Một khoản đảo ngược doanh số đã lập hóa đơn cho số lượng và số tiền trên chi tiết mô tả hóa đơn gốc cho chi phí.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-148">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b7bcf-149">Một giá trị thực tế đảo ngược doanh số chưa lập hóa đơn mới cho số lượng và số tiền trên chi tiết mô tả hóa đơn gốc cho chi phí.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-149">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="b7bcf-150">Lập hóa đơn một phần tín dụng của giao dịch chi phí đã lập hóa đơn trước đây.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-150">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b7bcf-151">Một khoản đảo ngược doanh số đã lập hóa đơn cho số lượng và số tiền được lập hóa đơn trên chi tiết mô tả hóa đơn gốc cho một chi phí.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-151">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b7bcf-152">Giá trị thực tế doanh số chưa lập hóa đơn mới, có thể tính phí cho số lượng và số tiền trên chi tiết mô tả hóa đơn đã hiệu chỉnh, khoản đảo ngược của giá trị này và giá trị thực tế doanh số đã lập hóa đơn tương đương.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-152">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b7bcf-153">Giá trị thực tế doanh số chưa lập hóa đơn mới, có thể tính phí cho số lượng và số tiền còn lại sau khi khấu trừ các số liệu đã hiệu chỉnh trên chi tiết mô tả hóa đơn.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-153">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b7bcf-154">Lập hóa đơn toàn bộ tín dụng của một giao dịch vật tư đã được lập hóa đơn trước đó.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-154">Invoicing the full credit of a previously invoiced material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b7bcf-155">Một khoản đảo ngược doanh số đã được lập hóa đơn cho số lượng và số tiền ghi trên chi tiết mô tả hóa đơn gốc cho vật tư.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-155">A billed sales reversal for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b7bcf-156">Một giá trị thực tế mới của doanh số bán hàng chưa được lập hóa đơn cho số lượng và số tiền ghi trên chi tiết mô tả hóa đơn gốc cho vật tư.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-156">A new unbilled sales actual for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="b7bcf-157">Lập hóa đơn tín dụng từng phần cho một giao dịch về vật tư.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-157">Invoicing the partial credit on a material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b7bcf-158">Một khoản đảo ngược doanh số đã được lập hóa đơn cho số lượng và số tiền ghi trên chi tiết mô tả hóa đơn gốc cho vật tư.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-158">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b7bcf-159">Một giá trị thực tế mới của doanh số bán hàng chưa lập hóa đơn. Đây là giá trị phải chịu phí tổn cho số lượng và số tiền ghi trên chi tiết mô tả hóa đơn đã chỉnh sửa, khoản đảo ngược của giá trị này và một giá trị thực tế của doanh số đã lập hóa đơn tương đương.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-159">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b7bcf-160">Giá trị thực tế doanh số chưa lập hóa đơn mới, có thể tính phí cho số lượng và số tiền còn lại sau khi khấu trừ các số liệu đã hiệu chỉnh trên chi tiết mô tả hóa đơn.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-160">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b7bcf-161">Lập hóa đơn toàn bộ tín dụng của giao dịch phí đã lập hóa đơn trước đây.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-161">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b7bcf-162">Một khoản đảo ngược doanh số đã lập hóa đơn cho số lượng và số tiền trên chi tiết mô tả hóa đơn gốc cho phí.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-162">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b7bcf-163">Một giá trị thực tế đảo ngược doanh số chưa lập hóa đơn mới cho số lượng và số tiền trên chi tiết mô tả hóa đơn gốc cho phí.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-163">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b7bcf-164">Lập hóa đơn một phần tín dụng của giao dịch phí đã lập hóa đơn trước đây.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-164">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b7bcf-165">Một khoản đảo ngược doanh số đã lập hóa đơn cho số lượng và số tiền được lập hóa đơn trên chi tiết mô tả hóa đơn gốc cho phí.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-165">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b7bcf-166">Giá trị thực tế doanh số chưa lập hóa đơn mới, có thể tính phí cho số lượng và số tiền trên chi tiết mô tả hóa đơn hiệu chỉnh đã sửa, khoản đảo ngược của giá trị này và giá trị thực tế doanh số đã lập hóa đơn tương đương.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-166">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="b7bcf-167">Lập hóa đơn toàn bộ tín dụng của mốc đã lập hóa đơn trước đây.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-167">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b7bcf-168">Một khoản đảo ngược doanh số đã lập hóa đơn cho số giờ và số tiền trên chi tiết mô tả hóa đơn gốc cho mốc.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-168">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="b7bcf-169">Trạng thái hóa đơn của mốc được cập nhật từ <b>Đã đăng hóa đơn khách hàng</b> thành <b>Sẵn sàng lập hóa đơn</b>.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-169">The invoice status of the milestone is updated from <b>Customer Invoice Posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="b7bcf-170">Lập hóa đơn một phần tín dụng của mốc đã lập hóa đơn trước đây.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-170">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b7bcf-171">Không Được hỗ trợ</span><span class="sxs-lookup"><span data-stu-id="b7bcf-171">Unsupported</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="b7bcf-172">Các khoản tín dụng và hiệu chỉnh của một mục mô tả hợp đồng dựa trên sản phẩm đã lập hóa đơn trước đây.</span><span class="sxs-lookup"><span data-stu-id="b7bcf-172">Credits and corrections of a previously invoiced product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b7bcf-173">Không Được hỗ trợ</span><span class="sxs-lookup"><span data-stu-id="b7bcf-173">Unsupported</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
