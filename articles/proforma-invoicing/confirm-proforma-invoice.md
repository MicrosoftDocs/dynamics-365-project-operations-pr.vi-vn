---
title: Xác nhận hóa đơn ước giá
description: Chủ đề này cung cấp thông tin về việc xác nhận hóa đơn ước giá.
author: rumant
manager: AnnBe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 560bb68cba865a6af60504114126ae6ea73dde2d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086953"
---
# <a name="confirm-a-proforma-invoice"></a><span data-ttu-id="b79f9-103">Xác nhận hóa đơn ước giá</span><span class="sxs-lookup"><span data-stu-id="b79f9-103">Confirm a proforma invoice</span></span>

<span data-ttu-id="b79f9-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_</span><span class="sxs-lookup"><span data-stu-id="b79f9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="b79f9-105">Sau khi hóa đơn ước giá được xác nhận, trạng thái của hóa đơn dự án được cập nhật thành **Đã xác nhận**.</span><span class="sxs-lookup"><span data-stu-id="b79f9-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="b79f9-106">Khi hóa đơn được xác nhận, mục đó sẽ trở thành dạng chỉ đọc.</span><span class="sxs-lookup"><span data-stu-id="b79f9-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="b79f9-107">Sau này, hóa đơn chỉ có thể được hiệu chỉnh nếu có bất kỳ sự chỉnh sửa hoặc ghi có nào do khách hàng thực hiện hoặc khi hóa đơn được đánh dấu là đã thanh toán.</span><span class="sxs-lookup"><span data-stu-id="b79f9-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, or when it's marked as paid.</span></span>

<span data-ttu-id="b79f9-108">Bảng sau liệt kê các giá trị thực tế được hệ thống tạo.</span><span class="sxs-lookup"><span data-stu-id="b79f9-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="b79f9-109">Các giá trị thực tế này được tạo ra khi một số hoạt động nhất định được thực hiện trên hóa đơn dự án nháp trước khi mục đó được xác nhận.</span><span class="sxs-lookup"><span data-stu-id="b79f9-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="416" valign="top">
                <p><span data-ttu-id="b79f9-110">
                    <strong>Kịch bản</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b79f9-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="608" valign="top">
                <p><span data-ttu-id="b79f9-111">
                    <strong>Giá trị thực tế được tạo khi xác nhận</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b79f9-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b79f9-112">Lập hóa đơn cho một giao dịch thời gian mà không có bất kỳ chỉnh sửa nào trên hóa đơn nháp.</span><span class="sxs-lookup"><span data-stu-id="b79f9-112">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b79f9-113">Một khoản đảo ngược doanh số chưa lập hóa đơn cho số giờ và số tiền khi phê duyệt thời gian ban đầu.</span><span class="sxs-lookup"><span data-stu-id="b79f9-113">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b79f9-114">Một giá trị thực tế doanh số đã lập hóa đơn cho số giờ và số tiền khi phê duyệt thời gian ban đầu.</span><span class="sxs-lookup"><span data-stu-id="b79f9-114">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="b79f9-115">Lập hóa đơn cho một giao dịch thời gian đã được sửa để giảm số lượng.</span><span class="sxs-lookup"><span data-stu-id="b79f9-115">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b79f9-116">Một khoản đảo ngược doanh số chưa lập hóa đơn cho số giờ và số tiền khi phê duyệt thời gian ban đầu.</span><span class="sxs-lookup"><span data-stu-id="b79f9-116">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b79f9-117">Giá trị thực tế doanh số chưa lập hóa đơn mới, có thể tính phí cho số giờ và số tiền trên chi tiết mô tả hóa đơn đã sửa, khoản đảo ngược của giá trị thực tế doanh số chưa lập hóa đơn và giá trị thực tế doanh số đã lập hóa đơn tương đương.</span><span class="sxs-lookup"><span data-stu-id="b79f9-117">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b79f9-118">Giá trị thực tế doanh số chưa lập hóa đơn mới, không thể tính phí cho số giờ và số tiền còn lại sau khi trừ số liệu đã hiệu chỉnh trên chi tiết mô tả hóa đơn đã sửa, khoản đảo ngược của giá trị thực tế doanh số chưa lập hóa đơn và giá trị thực tế doanh số đã lập hóa đơn tương đương.</span><span class="sxs-lookup"><span data-stu-id="b79f9-118">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b79f9-119">Lập hóa đơn cho một giao dịch thời gian đã được sửa để tăng số lượng.</span><span class="sxs-lookup"><span data-stu-id="b79f9-119">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b79f9-120">Một khoản đảo ngược doanh số chưa lập hóa đơn cho số giờ và số tiền khi phê duyệt thời gian ban đầu.</span><span class="sxs-lookup"><span data-stu-id="b79f9-120">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b79f9-121">Giá trị thực tế doanh số chưa lập hóa đơn mới, có thể tính phí cho số giờ và số tiền trên chi tiết mô tả hóa đơn đã sửa, khoản đảo ngược của giá trị thực tế doanh số chưa lập hóa đơn và giá trị thực tế doanh số đã lập hóa đơn tương đương.</span><span class="sxs-lookup"><span data-stu-id="b79f9-121">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b79f9-122">Lập hóa đơn cho một giao dịch chi phí mà không có bất kỳ chỉnh sửa nào trên hóa đơn nháp.</span><span class="sxs-lookup"><span data-stu-id="b79f9-122">Invoicing an expense transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b79f9-123">Một khoản đảo ngược doanh số chưa lập hóa đơn cho số lượng và số tiền khi phê duyệt chi phí ban đầu.</span><span class="sxs-lookup"><span data-stu-id="b79f9-123">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b79f9-124">Một giá trị thực tế doanh số đã lập hóa đơn cho số lượng và số tiền khi phê duyệt chi phí ban đầu.</span><span class="sxs-lookup"><span data-stu-id="b79f9-124">A billed sales actual for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="b79f9-125">Lập hóa đơn cho một giao dịch chi phí đã được sửa để giảm số lượng.</span><span class="sxs-lookup"><span data-stu-id="b79f9-125">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b79f9-126">Một khoản đảo ngược doanh số chưa lập hóa đơn cho số lượng và số tiền khi phê duyệt chi phí ban đầu.</span><span class="sxs-lookup"><span data-stu-id="b79f9-126">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b79f9-127">Giá trị thực tế doanh số chưa lập hóa đơn mới, có thể tính phí cho số lượng và số tiền trên chi tiết mô tả hóa đơn đã sửa, khoản đảo ngược của giá trị thực tế doanh số chưa lập hóa đơn và giá trị thực tế doanh số đã lập hóa đơn tương đương.</span><span class="sxs-lookup"><span data-stu-id="b79f9-127">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b79f9-128">Giá trị thực tế doanh số chưa lập hóa đơn mới, không thể tính phí cho số lượng và số tiền còn lại sau khi trừ số liệu đã hiệu chỉnh trên chi tiết mô tả hóa đơn đã sửa, khoản đảo ngược của giá trị thực tế doanh số chưa lập hóa đơn và giá trị thực tế doanh số đã lập hóa đơn tương đương.</span><span class="sxs-lookup"><span data-stu-id="b79f9-128">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent of the billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b79f9-129">Lập hóa đơn cho một giao dịch chi phí đã được sửa để tăng số lượng.</span><span class="sxs-lookup"><span data-stu-id="b79f9-129">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b79f9-130">Một khoản đảo ngược doanh số chưa lập hóa đơn cho số lượng và số tiền khi phê duyệt chi phí ban đầu.</span><span class="sxs-lookup"><span data-stu-id="b79f9-130">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b79f9-131">Giá trị thực tế doanh số chưa lập hóa đơn mới, có thể tính phí cho số lượng và số tiền trên chi tiết mô tả hóa đơn đã sửa, khoản đảo ngược của giá trị thực tế doanh số chưa lập hóa đơn và giá trị thực tế doanh số đã lập hóa đơn tương đương.</span><span class="sxs-lookup"><span data-stu-id="b79f9-131">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the untilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b79f9-132">Lập hóa đơn một khoản phí.</span><span class="sxs-lookup"><span data-stu-id="b79f9-132">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b79f9-133">Một khoản đảo ngược doanh số chưa lập hóa đơn cho số tiền phí trên dòng nhật ký kế toán ban đầu.</span><span class="sxs-lookup"><span data-stu-id="b79f9-133">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b79f9-134">Một giá trị thực tế doanh số đã lập hóa đơn cho số lượng và số tiền trên dòng nhật ký kế toán phí ban đầu.</span><span class="sxs-lookup"><span data-stu-id="b79f9-134">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="b79f9-135">Lập hóa đơn cho một mốc.</span><span class="sxs-lookup"><span data-stu-id="b79f9-135">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b79f9-136">Giá trị thực tế doanh số đã lập hóa đơn cho số tiền mốc trên mốc ban đầu trên mục mô tả hợp đồng dự án.</span><span class="sxs-lookup"><span data-stu-id="b79f9-136">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>
