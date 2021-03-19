---
title: Tắt thông số định giá
description: Chủ đề này cung cấp thông tin về cách tắt thông số định giá.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: d2e10c9ce782697fa4cbbe6eb63491ebb573a6f6
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274754"
---
# <a name="turning-off-a-pricing-dimension"></a><span data-ttu-id="54f46-103">Tắt thông số định giá</span><span class="sxs-lookup"><span data-stu-id="54f46-103">Turning off a pricing dimension</span></span>

<span data-ttu-id="54f46-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="54f46-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="54f46-105">Bạn có thể cần phải đánh giá và cập nhật chiến lược định giá mỗi vài năm.</span><span class="sxs-lookup"><span data-stu-id="54f46-105">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="54f46-106">Mọi bản cập nhật bạn thực hiện có thể yêu cầu bạn tắt thông số định giá hiện có và tạo một thông số mới.</span><span class="sxs-lookup"><span data-stu-id="54f46-106">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="54f46-107">Ví dụ: bạn có thể đã có giá theo **Vai trò** trước đây, nhưng bây giờ bạn đã quyết định giá theo **Kinh nghiệm làm việc**.</span><span class="sxs-lookup"><span data-stu-id="54f46-107">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="54f46-108">Điều này có thể đòi hỏi bạn tắt **Vai trò** làm thông số định giá và tạo **Trải nghiệm làm việc** dưới dạng thông số định giá mới.</span><span class="sxs-lookup"><span data-stu-id="54f46-108">This may require you to turn off **Role** as a pricing dimension and create **Work Experience** as a new pricing dimension.</span></span> 

<span data-ttu-id="54f46-109">Tắt thông số định giá, bất kể là sẵn dùng hay tùy chỉnh. Có thể thực hiện bằng cách đặt các trường **Áp dụng cho chi phí** và **Áp dụng cho doanh số** của Thông số định giá thành **Không**.</span><span class="sxs-lookup"><span data-stu-id="54f46-109">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="54f46-110">Tuy nhiên, khi thực hiện điều này, bạn có thể nhận được thông báo lỗi, **Không thể cập nhật hoặc xóa thông số định giá nếu có bản ghi giá được liên kết.**</span><span class="sxs-lookup"><span data-stu-id="54f46-110">However, when you do this, you might receive the error message, **Pricing dimension cannot be updated or deleted if there are associated price records.**</span></span>

![Có khả năng xảy ra lỗi quy trình công việc khi tắt một thông số định giá.](media/Business-Process-Error.png)

<span data-ttu-id="54f46-112">Thông báo lỗi này chỉ ra rằng có các hồ sơ giá trước đây đã được thiết lập cho thông số đang bị tắt.</span><span class="sxs-lookup"><span data-stu-id="54f46-112">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="54f46-113">Tất cả các hồ sơ **Giá theo vai trò** và **Tăng giá theo vai trò** nói đến một thông số phải được xóa trước khi có thể đặt khả năng của thông số thành **Không**.</span><span class="sxs-lookup"><span data-stu-id="54f46-113">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="54f46-114">Quy tắc này áp dụng cho cả thông số định giá sẵn dùng và mọi thông số định giá tùy chỉnh mà bạn có thể đã tạo.</span><span class="sxs-lookup"><span data-stu-id="54f46-114">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="54f46-115">Lý do xác thực là vì mỗi bản ghi **Giá theo vai trò** phải có một tổ hợp thông số duy nhất.</span><span class="sxs-lookup"><span data-stu-id="54f46-115">The reason for this validation is because each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="54f46-116">Ví dụ: trên bảng giá tên là **Tỷ lệ chi phí 2018 của Hoa Kỳ**, bạn có các hàng **Giá theo vai trò** sau.</span><span class="sxs-lookup"><span data-stu-id="54f46-116">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="54f46-117">Tiêu đề chuẩn</span><span class="sxs-lookup"><span data-stu-id="54f46-117">Standard Title</span></span>         | <span data-ttu-id="54f46-118">Đơn vị tổ chức</span><span class="sxs-lookup"><span data-stu-id="54f46-118">Org Unit</span></span>    |<span data-ttu-id="54f46-119">Đơn vị</span><span class="sxs-lookup"><span data-stu-id="54f46-119">Unit</span></span>   |<span data-ttu-id="54f46-120">Giá</span><span class="sxs-lookup"><span data-stu-id="54f46-120">Price</span></span>  |<span data-ttu-id="54f46-121">Tiền tệ</span><span class="sxs-lookup"><span data-stu-id="54f46-121">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="54f46-122">Kỹ sư hệ thống</span><span class="sxs-lookup"><span data-stu-id="54f46-122">Systems Engineer</span></span>|<span data-ttu-id="54f46-123">Contoso US</span><span class="sxs-lookup"><span data-stu-id="54f46-123">Contoso US</span></span>|<span data-ttu-id="54f46-124">Hour</span><span class="sxs-lookup"><span data-stu-id="54f46-124">Hour</span></span>| <span data-ttu-id="54f46-125">100</span><span class="sxs-lookup"><span data-stu-id="54f46-125">100</span></span>|<span data-ttu-id="54f46-126">USD</span><span class="sxs-lookup"><span data-stu-id="54f46-126">USD</span></span>|
| <span data-ttu-id="54f46-127">Kỹ sư hệ thống cao cấp</span><span class="sxs-lookup"><span data-stu-id="54f46-127">Senior Systems Engineer</span></span>|<span data-ttu-id="54f46-128">Contoso US</span><span class="sxs-lookup"><span data-stu-id="54f46-128">Contoso US</span></span>|<span data-ttu-id="54f46-129">Hour</span><span class="sxs-lookup"><span data-stu-id="54f46-129">Hour</span></span>| <span data-ttu-id="54f46-130">150</span><span class="sxs-lookup"><span data-stu-id="54f46-130">150</span></span>| <span data-ttu-id="54f46-131">USD</span><span class="sxs-lookup"><span data-stu-id="54f46-131">USD</span></span>|


<span data-ttu-id="54f46-132">Khi bạn tắt **Tiêu đề chuẩn** làm thông số định giá và công cụ định giá, thì công cụ định giá sẽ chỉ sử dụng giá trị **Đơn vị tổ chức** từ ngữ cảnh nhập.</span><span class="sxs-lookup"><span data-stu-id="54f46-132">When you turn off **Standard Title** as the pricing dimension, and the pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="54f46-133">Nếu **Đơn vị tổ chức** của ngữ cảnh nhập là “Contoso Hoa Kỳ”, thì kết quả sẽ không xác định bởi vì cả hai hàng sẽ phù hợp.</span><span class="sxs-lookup"><span data-stu-id="54f46-133">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="54f46-134">Để tránh trường hợp này, khi bạn tạo bản ghi **Giá theo vai trò**, hệ thống sẽ xác thực rằng tổ hợp thông số là duy nhất.</span><span class="sxs-lookup"><span data-stu-id="54f46-134">To avoid this scenario, when you create **Role Price** records, the system validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="54f46-135">Nếu thông số bị tắt sau khi hồ sơ **Giá theo vai trò** được tạo, hạn chế này có thể bị vi phạm.</span><span class="sxs-lookup"><span data-stu-id="54f46-135">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="54f46-136">Do đó, trước khi tắt một thông số, bạn cần xóa tất cả các hàng **Giá theo vai trò** và **Tăng giá theo vai trò** đã điền sẵn giá trị thông số đó.</span><span class="sxs-lookup"><span data-stu-id="54f46-136">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]