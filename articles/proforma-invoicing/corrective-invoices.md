---
title: Hóa đơn hiệu chỉnh dựa trên dự án
description: Chủ đề này cung cấp thông tin về cách tạo và xác nhận các hóa đơn hiệu chỉnh dựa trên dự án trong Project Operations.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f6b6670f823577bf7f784443f97f0b77e1e9a6aa
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012297"
---
# <a name="corrective-project-based-invoices"></a><span data-ttu-id="b6978-103">Hóa đơn hiệu chỉnh dựa trên dự án</span><span class="sxs-lookup"><span data-stu-id="b6978-103">Corrective project-based invoices</span></span>

<span data-ttu-id="b6978-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_</span><span class="sxs-lookup"><span data-stu-id="b6978-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="b6978-105">Hóa đơn dự án đã xác nhận có thể được hiệu chỉnh để xử lý các thay đổi hoặc tín dụng theo như sự thương lượng với khách hàng và người quản lý dự án.</span><span class="sxs-lookup"><span data-stu-id="b6978-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="b6978-106">Để chỉnh sửa hóa đơn đã xác nhận, hãy mở hóa đơn đã xác nhận và chọn **Sửa chữa hóa đơn này**.</span><span class="sxs-lookup"><span data-stu-id="b6978-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="b6978-107">Lựa chọn này không khả dụng trừ khi hóa đơn dự án được xác nhận hoặc hóa đơn dựa trên dự án có các khoản tạm ứng hoặc đặt cọc hoặc các mục đối chiếu các khoản tạm ứng hoặc đặt cọc.</span><span class="sxs-lookup"><span data-stu-id="b6978-107">This selection isn't available unless a project invoice is confirmed or the project-based invoice has advances or retainers or reconciliations of advances or retainers.</span></span>

<span data-ttu-id="b6978-108">Một hóa đơn nháp mới được tạo từ hóa đơn đã xác nhận.</span><span class="sxs-lookup"><span data-stu-id="b6978-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="b6978-109">Tất cả các chi tiết mô tả hóa đơn từ hóa đơn đã được xác nhận trước đây sẽ được sao chép vào hóa đơn nháp mới.</span><span class="sxs-lookup"><span data-stu-id="b6978-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="b6978-110">Sau đây là một số điểm chính mà bạn cần hiểu về chi tiết mô tả trên hóa đơn được hiệu chỉnh mới:</span><span class="sxs-lookup"><span data-stu-id="b6978-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="b6978-111">Tất cả các số lượng được cập nhật thành không.</span><span class="sxs-lookup"><span data-stu-id="b6978-111">All quantities are updated to zero.</span></span> <span data-ttu-id="b6978-112">Dynamics 365 Project Operations giả định rằng tất cả các hạng mục đưa vào hóa đơn đều được ghi có đầy đủ.</span><span class="sxs-lookup"><span data-stu-id="b6978-112">Dynamics 365 Project Operations assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="b6978-113">Nếu cần, bạn có thể cập nhật thủ công các số lượng này để phản ánh số lượng được lập hóa đơn chứ không phải số lượng được ghi có.</span><span class="sxs-lookup"><span data-stu-id="b6978-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="b6978-114">Dựa trên số lượng bạn nhập, ứng dụng sẽ tính số lượng được ghi có.</span><span class="sxs-lookup"><span data-stu-id="b6978-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="b6978-115">Số lượng này được phản ánh ở các giá trị thực tế sẽ được tạo ra khi hóa đơn hiệu chỉnh được xác nhận.</span><span class="sxs-lookup"><span data-stu-id="b6978-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="b6978-116">Nếu bạn thay đổi số tiền thuế, thì bạn phải nhập số tiền thuế chính xác chứ không phải số tiền thuế được ghi có.</span><span class="sxs-lookup"><span data-stu-id="b6978-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="b6978-117">Các phần hiệu chỉnh mốc luôn được xử lý dưới dạng tín dụng đầy đủ.</span><span class="sxs-lookup"><span data-stu-id="b6978-117">Milestone corrections are always processed as full credits.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="b6978-118">Đối với chi tiết mô tả hóa đơn là các sửa đổi đối với những khoản phí đã được lập hóa đơn, trường **Điều chỉnh** được đặt thành **Có**.</span><span class="sxs-lookup"><span data-stu-id="b6978-118">For invoice line details that are corrections to other already invoiced charges, the **Correction** field is set to **Yes**.</span></span> <span data-ttu-id="b6978-119">Đối với hóa đơn có các chi tiết mô tả hóa đơn đã được sửa đổi, trường **Có nội dung điều chỉnh** được đặt thành **Có**.</span><span class="sxs-lookup"><span data-stu-id="b6978-119">For invoices that have corrected invoice line details, the **Has corrections** field is set to **Yes**.</span></span>

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a><span data-ttu-id="b6978-120">Các giá trị thực tế được tạo khi xác nhận hóa đơn hiệu chỉnh</span><span class="sxs-lookup"><span data-stu-id="b6978-120">Actuals created when a corrective invoice is confirmed</span></span>

<span data-ttu-id="b6978-121">Bảng sau liệt kê các giá trị thực tế được tạo khi xác nhận hóa đơn hiệu chỉnh.</span><span class="sxs-lookup"><span data-stu-id="b6978-121">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="b6978-122">
                    <strong>Kịch bản</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b6978-122">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="b6978-123">
                    <strong>Giá trị thực tế được tạo khi xác nhận</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b6978-123">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b6978-124">Lập hóa đơn toàn bộ tín dụng của giao dịch thời gian đã lập hóa đơn trước đây.</span><span class="sxs-lookup"><span data-stu-id="b6978-124">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b6978-125">Một khoản đảo ngược doanh số đã lập hóa đơn cho số giờ và số tiền trên chi tiết mô tả hóa đơn gốc cho thời gian.</span><span class="sxs-lookup"><span data-stu-id="b6978-125">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b6978-126">Một giá trị thực tế đảo ngược doanh số chưa lập hóa đơn mới cho số giờ và số tiền trên chi tiết mô tả hóa đơn gốc cho thời gian.</span><span class="sxs-lookup"><span data-stu-id="b6978-126">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="b6978-127">Lập hóa đơn một phần tín dụng trên một giao dịch thời gian.</span><span class="sxs-lookup"><span data-stu-id="b6978-127">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b6978-128">Một khoản đảo ngược doanh số đã lập hóa đơn cho số giờ và số tiền được lập hóa đơn trên chi tiết mô tả hóa đơn gốc cho thời gian.</span><span class="sxs-lookup"><span data-stu-id="b6978-128">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b6978-129">Giá trị thực tế doanh số chưa lập hóa đơn mới, có thể tính phí cho số giờ và số tiền trên chi tiết mô tả hóa đơn đã sửa, khoản đảo ngược của giá trị này và giá trị thực tế doanh số bán hàng đã lập hóa đơn tương đương.</span><span class="sxs-lookup"><span data-stu-id="b6978-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b6978-130">Giá trị thực tế doanh số chưa lập hóa đơn mới, có thể tính phí cho số giờ và số tiền còn lại sau khi khấu trừ các số liệu đã hiệu chỉnh trên chi tiết mô tả hóa đơn.</span><span class="sxs-lookup"><span data-stu-id="b6978-130">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b6978-131">Lập hóa đơn toàn bộ tín dụng của giao dịch chi phí đã lập hóa đơn trước đây.</span><span class="sxs-lookup"><span data-stu-id="b6978-131">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b6978-132">Một khoản đảo ngược doanh số đã lập hóa đơn cho số lượng và số tiền trên chi tiết mô tả hóa đơn gốc cho chi phí.</span><span class="sxs-lookup"><span data-stu-id="b6978-132">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b6978-133">Một giá trị thực tế đảo ngược doanh số chưa lập hóa đơn mới cho số lượng và số tiền trên chi tiết mô tả hóa đơn gốc cho chi phí.</span><span class="sxs-lookup"><span data-stu-id="b6978-133">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="b6978-134">Lập hóa đơn một phần tín dụng của giao dịch chi phí đã lập hóa đơn trước đây.</span><span class="sxs-lookup"><span data-stu-id="b6978-134">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b6978-135">Một khoản đảo ngược doanh số đã lập hóa đơn cho số lượng và số tiền được lập hóa đơn trên chi tiết mô tả hóa đơn gốc cho một chi phí.</span><span class="sxs-lookup"><span data-stu-id="b6978-135">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b6978-136">Giá trị thực tế doanh số chưa lập hóa đơn mới, có thể tính phí cho số lượng và số tiền trên chi tiết mô tả hóa đơn đã hiệu chỉnh, khoản đảo ngược của giá trị này và giá trị thực tế doanh số đã lập hóa đơn tương đương.</span><span class="sxs-lookup"><span data-stu-id="b6978-136">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b6978-137">Giá trị thực tế doanh số chưa lập hóa đơn mới, có thể tính phí cho số lượng và số tiền còn lại sau khi khấu trừ các số liệu đã hiệu chỉnh trên chi tiết mô tả hóa đơn.</span><span class="sxs-lookup"><span data-stu-id="b6978-137">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
                <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b6978-138">Lập hóa đơn toàn bộ tín dụng của một giao dịch vật tư đã được lập hóa đơn trước đó.</span><span class="sxs-lookup"><span data-stu-id="b6978-138">Invoicing the full credit of a previously invoiced material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b6978-139">Một khoản đảo ngược doanh số đã được lập hóa đơn cho số lượng và số tiền ghi trên chi tiết mô tả hóa đơn gốc cho vật tư.</span><span class="sxs-lookup"><span data-stu-id="b6978-139">A billed sales reversal for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b6978-140">Một giá trị thực tế mới của doanh số bán hàng chưa được lập hóa đơn cho số lượng và số tiền ghi trên chi tiết mô tả hóa đơn gốc cho vật tư.</span><span class="sxs-lookup"><span data-stu-id="b6978-140">A new unbilled sales actual for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="b6978-141">Lập hóa đơn tín dụng từng phần cho một giao dịch về vật tư.</span><span class="sxs-lookup"><span data-stu-id="b6978-141">Invoicing the partial credit on a material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b6978-142">Một khoản đảo ngược doanh số đã được lập hóa đơn cho số lượng và số tiền ghi trên chi tiết mô tả hóa đơn gốc cho vật tư.</span><span class="sxs-lookup"><span data-stu-id="b6978-142">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b6978-143">Một giá trị thực tế mới của doanh số bán hàng chưa lập hóa đơn. Đây là giá trị phải chịu phí tổn cho số lượng và số tiền ghi trên chi tiết mô tả hóa đơn đã chỉnh sửa, khoản đảo ngược của giá trị này và một giá trị thực tế của doanh số đã lập hóa đơn tương đương.</span><span class="sxs-lookup"><span data-stu-id="b6978-143">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b6978-144">Giá trị thực tế doanh số chưa lập hóa đơn mới, có thể tính phí cho số lượng và số tiền còn lại sau khi khấu trừ các số liệu đã hiệu chỉnh trên chi tiết mô tả hóa đơn.</span><span class="sxs-lookup"><span data-stu-id="b6978-144">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b6978-145">Lập hóa đơn toàn bộ tín dụng của giao dịch phí đã lập hóa đơn trước đây.</span><span class="sxs-lookup"><span data-stu-id="b6978-145">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b6978-146">Một khoản đảo ngược doanh số đã lập hóa đơn cho số lượng và số tiền trên chi tiết mô tả hóa đơn gốc cho phí.</span><span class="sxs-lookup"><span data-stu-id="b6978-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b6978-147">Một giá trị thực tế đảo ngược doanh số chưa lập hóa đơn mới cho số lượng và số tiền trên chi tiết mô tả hóa đơn gốc cho phí.</span><span class="sxs-lookup"><span data-stu-id="b6978-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b6978-148">Lập hóa đơn một phần tín dụng của giao dịch phí đã lập hóa đơn trước đây.</span><span class="sxs-lookup"><span data-stu-id="b6978-148">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b6978-149">Một khoản đảo ngược doanh số đã lập hóa đơn cho số lượng và số tiền được lập hóa đơn trên chi tiết mô tả hóa đơn gốc cho phí.</span><span class="sxs-lookup"><span data-stu-id="b6978-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b6978-150">Giá trị thực tế doanh số chưa lập hóa đơn mới, có thể tính phí cho số lượng và số tiền trên chi tiết mô tả hóa đơn hiệu chỉnh đã sửa, khoản đảo ngược của giá trị này và giá trị thực tế doanh số đã lập hóa đơn tương đương.</span><span class="sxs-lookup"><span data-stu-id="b6978-150">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="b6978-151">Lập hóa đơn toàn bộ tín dụng của mốc đã lập hóa đơn trước đây.</span><span class="sxs-lookup"><span data-stu-id="b6978-151">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b6978-152">Một khoản đảo ngược doanh số đã lập hóa đơn cho số giờ và số tiền trên chi tiết mô tả hóa đơn gốc cho mốc.</span><span class="sxs-lookup"><span data-stu-id="b6978-152">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="b6978-153">Trạng thái hóa đơn của mốc được cập nhật từ <b>Đã đăng hóa đơn khách hàng</b> thành <b>Sẵn sàng lập hóa đơn</b>.</span><span class="sxs-lookup"><span data-stu-id="b6978-153">The invoice status of the milestone is updated from <b>Customer Invoice Posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="b6978-154">Lập hóa đơn một phần tín dụng của mốc đã lập hóa đơn trước đây.</span><span class="sxs-lookup"><span data-stu-id="b6978-154">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b6978-155">Kịch bản này không được hỗ trợ.</span><span class="sxs-lookup"><span data-stu-id="b6978-155">This scenario isn't supported.</span></span>
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
