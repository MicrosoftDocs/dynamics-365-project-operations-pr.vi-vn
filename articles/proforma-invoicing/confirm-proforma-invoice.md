---
title: Xác nhận hóa đơn ước giá dựa trên dự án
description: Chủ đề này cung cấp thông tin về việc xác nhận hóa đơn ước giá dựa trên dự án.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1e4591d97e9d895dade42b2bcce57f22208cba96
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012162"
---
# <a name="confirm-a-proforma-project-based-invoice"></a><span data-ttu-id="4162c-103">Xác nhận hóa đơn ước giá dựa trên dự án</span><span class="sxs-lookup"><span data-stu-id="4162c-103">Confirm a proforma project-based invoice</span></span>

<span data-ttu-id="4162c-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_</span><span class="sxs-lookup"><span data-stu-id="4162c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="4162c-105">Sau khi hóa đơn ước giá được xác nhận, trạng thái của hóa đơn dự án được cập nhật thành **Đã xác nhận**.</span><span class="sxs-lookup"><span data-stu-id="4162c-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="4162c-106">Khi hóa đơn được xác nhận, mục đó sẽ trở thành dạng chỉ đọc.</span><span class="sxs-lookup"><span data-stu-id="4162c-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="4162c-107">Từ giờ trở đi, chỉ có thể sửa hóa đơn nếu có bất kỳ sự sửa đổi hoặc ghi có nào do khách hàng thực hiện.</span><span class="sxs-lookup"><span data-stu-id="4162c-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits.</span></span>

<span data-ttu-id="4162c-108">Bảng sau liệt kê các giá trị thực tế được hệ thống tạo.</span><span class="sxs-lookup"><span data-stu-id="4162c-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="4162c-109">Các giá trị thực tế này được tạo ra khi một số hoạt động nhất định được thực hiện trên hóa đơn dự án nháp trước khi mục đó được xác nhận.</span><span class="sxs-lookup"><span data-stu-id="4162c-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="4162c-110">
                    <strong>Kịch bản</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4162c-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="4162c-111">
                    <strong>Giá trị thực tế được tạo khi xác nhận</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4162c-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4162c-112">Lập hóa đơn khoản tạm ứng hoặc trả trước</span><span class="sxs-lookup"><span data-stu-id="4162c-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4162c-113">Giá trị thực tế doanh số được lập hóa đơn thuộc loại <strong>Khoản trả trước</strong> được tạo ra cho số tiền tạm ứng hoặc trả trước.</span><span class="sxs-lookup"><span data-stu-id="4162c-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4162c-114">Giá trị thực tế của doanh số chưa lập hóa đơn có số tiền đặt cọc hoặc tạm ứng âm được dùng để đối chiếu.</span><span class="sxs-lookup"><span data-stu-id="4162c-114">An unbilled sales actual with a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4162c-115">Sau khi điều hòa đầy đủ khoản trả trước hoặc tạm ứng trên hóa đơn.</span><span class="sxs-lookup"><span data-stu-id="4162c-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4162c-116">Khoản đảo ngược doanh số chưa lập hóa đơn của số tiền trả trước hoặc tạm ứng đã tạo để điều hòa.</span><span class="sxs-lookup"><span data-stu-id="4162c-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="4162c-117">Số tiền này là số dương vì nó có tác dụng bù cho giá trị âm được tạo ra khi khoản trả trước hoặc tạm ứng được lập hóa đơn.</span><span class="sxs-lookup"><span data-stu-id="4162c-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4162c-118">Một giá trị thực tế doanh số đã lập hóa đơn cho số tiền trên hóa đơn này.</span><span class="sxs-lookup"><span data-stu-id="4162c-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="4162c-119">Sau khi điều hòa một phần khoản trả trước hoặc tạm ứng trên hóa đơn.</span><span class="sxs-lookup"><span data-stu-id="4162c-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4162c-120">Khoản đảo ngược doanh số chưa lập hóa đơn của số tiền trả trước hoặc tạm ứng đã tạo để điều hòa.</span><span class="sxs-lookup"><span data-stu-id="4162c-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="4162c-121">Số tiền này là số dương vì nó có tác dụng bù cho giá trị âm được tạo ra khi khoản trả trước hoặc tạm ứng được lập hóa đơn.</span><span class="sxs-lookup"><span data-stu-id="4162c-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4162c-122">Một giá trị thực tế doanh số đã lập hóa đơn cho số tiền trên hóa đơn này.</span><span class="sxs-lookup"><span data-stu-id="4162c-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4162c-123">Một giá trị thực tế doanh số chưa lập hóa đơn, có giá trị âm của số tiền trả trước hoặc tạm ứng sẽ được sử dụng để điều hòa trong các hóa đơn sau này.</span><span class="sxs-lookup"><span data-stu-id="4162c-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4162c-124">Lập hóa đơn cho một giao dịch thời gian mà không có bất kỳ chỉnh sửa nào trên hóa đơn nháp.</span><span class="sxs-lookup"><span data-stu-id="4162c-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4162c-125">Một khoản đảo ngược doanh số chưa lập hóa đơn cho số giờ và số tiền khi phê duyệt thời gian ban đầu.</span><span class="sxs-lookup"><span data-stu-id="4162c-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4162c-126">Một giá trị thực tế doanh số đã lập hóa đơn cho số giờ và số tiền khi phê duyệt thời gian ban đầu.</span><span class="sxs-lookup"><span data-stu-id="4162c-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="4162c-127">Lập hóa đơn cho một giao dịch thời gian đã được sửa để giảm số lượng.</span><span class="sxs-lookup"><span data-stu-id="4162c-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4162c-128">Một khoản đảo ngược doanh số chưa lập hóa đơn cho số giờ và số tiền khi phê duyệt thời gian ban đầu.</span><span class="sxs-lookup"><span data-stu-id="4162c-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4162c-129">Giá trị thực tế doanh số chưa lập hóa đơn mới, có thể tính phí cho số giờ và số tiền trên chi tiết mô tả hóa đơn đã sửa, khoản đảo ngược của giá trị thực tế doanh số và giá trị thực tế doanh số đã lập hóa đơn tương đương.</span><span class="sxs-lookup"><span data-stu-id="4162c-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4162c-130">Giá trị thực tế mới của doanh số bán hàng chưa lập hóa đơn. Đây là giá trị không phải chịu phí tổn cho số giờ và số tiền còn lại sau khi trừ đi các số liệu đã sửa trên chi tiết mô tả hóa đơn đã chỉnh sửa, khoản đảo ngược giá trị thực tế của doanh số và giá trị thực tế của doanh số được lập hóa đơn tương đương.</span><span class="sxs-lookup"><span data-stu-id="4162c-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4162c-131">Lập hóa đơn cho một giao dịch thời gian đã được sửa để tăng số lượng.</span><span class="sxs-lookup"><span data-stu-id="4162c-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4162c-132">Một khoản đảo ngược doanh số chưa lập hóa đơn cho số giờ và số tiền khi phê duyệt thời gian ban đầu.</span><span class="sxs-lookup"><span data-stu-id="4162c-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4162c-133">Giá trị thực tế doanh số chưa lập hóa đơn mới, có thể tính phí cho số giờ và số tiền trên chi tiết mô tả hóa đơn đã sửa, khoản đảo ngược của giá trị thực tế doanh số chưa lập hóa đơn và giá trị thực tế doanh số đã lập hóa đơn tương đương.</span><span class="sxs-lookup"><span data-stu-id="4162c-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4162c-134">Lập hóa đơn cho một giao dịch chi phí mà không có bất kỳ chỉnh sửa nào trên hóa đơn nháp.</span><span class="sxs-lookup"><span data-stu-id="4162c-134">Invoicing an expense transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4162c-135">Một khoản đảo ngược doanh số chưa lập hóa đơn cho số lượng và số tiền khi phê duyệt chi phí ban đầu.</span><span class="sxs-lookup"><span data-stu-id="4162c-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4162c-136">Một giá trị thực tế doanh số đã lập hóa đơn cho số lượng và số tiền khi phê duyệt chi phí ban đầu.</span><span class="sxs-lookup"><span data-stu-id="4162c-136">A billed sales actual for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="4162c-137">Lập hóa đơn cho một giao dịch chi phí đã được sửa để giảm số lượng.</span><span class="sxs-lookup"><span data-stu-id="4162c-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4162c-138">Một khoản đảo ngược doanh số chưa lập hóa đơn cho số lượng và số tiền khi phê duyệt chi phí ban đầu.</span><span class="sxs-lookup"><span data-stu-id="4162c-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4162c-139">Giá trị thực tế doanh số chưa lập hóa đơn mới, có thể tính phí cho số lượng và số tiền trên chi tiết mô tả hóa đơn đã sửa, khoản đảo ngược của giá trị thực tế doanh số chưa lập hóa đơn và giá trị thực tế doanh số đã lập hóa đơn tương đương.</span><span class="sxs-lookup"><span data-stu-id="4162c-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4162c-140">Giá trị thực tế doanh số chưa lập hóa đơn mới, không thể tính phí cho số lượng và số tiền còn lại sau khi trừ số liệu đã hiệu chỉnh trên chi tiết mô tả hóa đơn đã sửa, khoản đảo ngược của giá trị thực tế doanh số chưa lập hóa đơn và giá trị thực tế doanh số đã lập hóa đơn tương đương.</span><span class="sxs-lookup"><span data-stu-id="4162c-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4162c-141">Lập hóa đơn cho một giao dịch chi phí đã được sửa để tăng số lượng.</span><span class="sxs-lookup"><span data-stu-id="4162c-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4162c-142">Một khoản đảo ngược doanh số chưa lập hóa đơn cho số lượng và số tiền khi phê duyệt chi phí ban đầu.</span><span class="sxs-lookup"><span data-stu-id="4162c-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4162c-143">Giá trị thực tế doanh số chưa lập hóa đơn mới, có thể tính phí cho số lượng và số tiền trên chi tiết mô tả hóa đơn đã sửa, khoản đảo ngược của giá trị thực tế doanh số chưa lập hóa đơn và giá trị thực tế doanh số đã lập hóa đơn tương đương.</span><span class="sxs-lookup"><span data-stu-id="4162c-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4162c-144">Lập hóa đơn cho một giao dịch về vật tư mà không có bất kỳ chỉnh sửa nào trên hóa đơn dự thảo.</span><span class="sxs-lookup"><span data-stu-id="4162c-144">Invoicing a material transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4162c-145">Một khoản đảo ngược doanh số chưa lập hóa đơn cho số lượng và số tiền trên bản phê duyệt sử dụng vật tư ban đầu.</span><span class="sxs-lookup"><span data-stu-id="4162c-145">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4162c-146">Giá trị thực tế của doanh số được lập hóa đơn cho số lượng và số tiền trên bản phê duyệt sử dụng vật tư ban đầu.</span><span class="sxs-lookup"><span data-stu-id="4162c-146">A billed sales actual for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="4162c-147">Lập hóa đơn cho một giao dịch về vật tư đã được chỉnh sửa để giảm số lượng.</span><span class="sxs-lookup"><span data-stu-id="4162c-147">Invoicing a material transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4162c-148">Một khoản đảo ngược doanh số chưa lập hóa đơn cho số lượng và số tiền trên bản phê duyệt thời gian ban đầu.</span><span class="sxs-lookup"><span data-stu-id="4162c-148">An unbilled sales reversal for the quantity and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4162c-149">Giá trị thực tế doanh số chưa lập hóa đơn mới, có thể tính phí cho số lượng và số tiền trên chi tiết mô tả hóa đơn đã sửa, khoản đảo ngược của giá trị thực tế doanh số chưa lập hóa đơn và giá trị thực tế doanh số đã lập hóa đơn tương đương.</span><span class="sxs-lookup"><span data-stu-id="4162c-149">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4162c-150">Giá trị thực tế doanh số chưa lập hóa đơn mới, không thể tính phí cho số lượng và số tiền còn lại sau khi trừ số liệu đã hiệu chỉnh trên chi tiết mô tả hóa đơn đã sửa, khoản đảo ngược của giá trị thực tế doanh số chưa lập hóa đơn và giá trị thực tế doanh số đã lập hóa đơn tương đương.</span><span class="sxs-lookup"><span data-stu-id="4162c-150">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4162c-151">Lập hóa đơn cho một giao dịch về vật tư đã được chỉnh sửa để tăng số lượng.</span><span class="sxs-lookup"><span data-stu-id="4162c-151">Invoicing a material transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4162c-152">Một khoản đảo ngược doanh số chưa lập hóa đơn cho số lượng và số tiền trên bản phê duyệt sử dụng vật tư ban đầu.</span><span class="sxs-lookup"><span data-stu-id="4162c-152">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4162c-153">Giá trị thực tế doanh số chưa lập hóa đơn mới, có thể tính phí cho số lượng và số tiền trên chi tiết mô tả hóa đơn đã sửa, khoản đảo ngược của giá trị thực tế doanh số chưa lập hóa đơn và giá trị thực tế doanh số đã lập hóa đơn tương đương.</span><span class="sxs-lookup"><span data-stu-id="4162c-153">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4162c-154">Lập hóa đơn một khoản phí.</span><span class="sxs-lookup"><span data-stu-id="4162c-154">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4162c-155">Một khoản đảo ngược doanh số chưa lập hóa đơn cho số tiền phí trên dòng nhật ký kế toán ban đầu.</span><span class="sxs-lookup"><span data-stu-id="4162c-155">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4162c-156">Một giá trị thực tế doanh số đã lập hóa đơn cho số lượng và số tiền trên dòng nhật ký kế toán phí ban đầu.</span><span class="sxs-lookup"><span data-stu-id="4162c-156">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="4162c-157">Lập hóa đơn cho một mốc.</span><span class="sxs-lookup"><span data-stu-id="4162c-157">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4162c-158">Giá trị thực tế doanh số đã lập hóa đơn cho số tiền mốc trên mốc ban đầu trên mục mô tả hợp đồng dự án.</span><span class="sxs-lookup"><span data-stu-id="4162c-158">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
       
    </tbody>
</table>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
