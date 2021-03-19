---
title: Tắt thông số định giá
description: Chủ đề này cho biết cách thiết lập thông số định giá trong giải pháp Project Service.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 6e4b80b9c4b1b0f57d04079c9d2f84051b451d29
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281864"
---
# <a name="turn-off-a-pricing-dimension"></a><span data-ttu-id="4ab16-103">Tắt thông số định giá</span><span class="sxs-lookup"><span data-stu-id="4ab16-103">Turn off a pricing dimension</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="4ab16-104">Bạn có thể cần phải đánh giá và cập nhật chiến lược định giá mỗi vài năm.</span><span class="sxs-lookup"><span data-stu-id="4ab16-104">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="4ab16-105">Mọi bản cập nhật bạn thực hiện có thể yêu cầu bạn tắt thông số định giá hiện có và tạo một thông số mới.</span><span class="sxs-lookup"><span data-stu-id="4ab16-105">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="4ab16-106">Ví dụ: bạn có thể đã có giá theo **Vai trò** trước đây, nhưng bây giờ bạn đã quyết định giá theo **Kinh nghiệm làm việc**.</span><span class="sxs-lookup"><span data-stu-id="4ab16-106">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="4ab16-107">Điều này có thể đòi hỏi bạn tắt **Vai trò** làm thông số định giá và tạo **Trải nghiệm làm việc** dưới dạng thông số định giá mới.</span><span class="sxs-lookup"><span data-stu-id="4ab16-107">This may require you to turn off **Role** as a pricing dimension and create **Work Expereince** as a new pricing dimension.</span></span> 

<span data-ttu-id="4ab16-108">Tắt thông số định giá, bất kể là sẵn dùng hay tùy chỉnh. Có thể thực hiện bằng cách đặt các trường **Áp dụng cho chi phí** và **Áp dụng cho doanh số** của Thông số định giá thành **Không**.</span><span class="sxs-lookup"><span data-stu-id="4ab16-108">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="4ab16-109">Tuy nhiên, khi thực hiện điều này, bạn có thể nhận được thông báo lỗi sau.</span><span class="sxs-lookup"><span data-stu-id="4ab16-109">However, when you do this, you might receive the following error message.</span></span>

![Có khả năng xảy ra lỗi quy trình công việc khi tắt một thông số định giá.](media/Business-Process-Error.png)


<span data-ttu-id="4ab16-111">Thông báo lỗi này chỉ ra rằng có các hồ sơ giá trước đây đã được thiết lập cho thông số đang bị tắt.</span><span class="sxs-lookup"><span data-stu-id="4ab16-111">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="4ab16-112">Tất cả các hồ sơ **Giá theo vai trò** và **Tăng giá theo vai trò** nói đến một thông số phải được xóa trước khi có thể đặt khả năng của thông số thành **Không**.</span><span class="sxs-lookup"><span data-stu-id="4ab16-112">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="4ab16-113">Quy tắc này áp dụng cho cả thông số định giá sẵn dùng và mọi thông số định giá tùy chỉnh mà bạn có thể đã tạo.</span><span class="sxs-lookup"><span data-stu-id="4ab16-113">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="4ab16-114">Lý do xác thực là do Project Service có một hạn chế rằng mỗi hồ sơ **Giá theo vai trò** phải có một tổ hợp thông số duy nhất.</span><span class="sxs-lookup"><span data-stu-id="4ab16-114">The reason for this validation is because Project Service has a constraint that each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="4ab16-115">Ví dụ: trên bảng giá tên là **Tỷ lệ chi phí 2018 của Hoa Kỳ**, bạn có các hàng **Giá theo vai trò** sau.</span><span class="sxs-lookup"><span data-stu-id="4ab16-115">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="4ab16-116">Tiêu đề chuẩn</span><span class="sxs-lookup"><span data-stu-id="4ab16-116">Standard Title</span></span>         | <span data-ttu-id="4ab16-117">Đơn vị tổ chức</span><span class="sxs-lookup"><span data-stu-id="4ab16-117">Org Unit</span></span>    |<span data-ttu-id="4ab16-118">Đơn vị</span><span class="sxs-lookup"><span data-stu-id="4ab16-118">Unit</span></span>   |<span data-ttu-id="4ab16-119">Giá</span><span class="sxs-lookup"><span data-stu-id="4ab16-119">Price</span></span>  |<span data-ttu-id="4ab16-120">Tiền tệ</span><span class="sxs-lookup"><span data-stu-id="4ab16-120">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="4ab16-121">Kỹ sư hệ thống</span><span class="sxs-lookup"><span data-stu-id="4ab16-121">Systems Engineer</span></span>|<span data-ttu-id="4ab16-122">Contoso US</span><span class="sxs-lookup"><span data-stu-id="4ab16-122">Contoso US</span></span>|<span data-ttu-id="4ab16-123">Hour</span><span class="sxs-lookup"><span data-stu-id="4ab16-123">Hour</span></span>| <span data-ttu-id="4ab16-124">100</span><span class="sxs-lookup"><span data-stu-id="4ab16-124">100</span></span>|<span data-ttu-id="4ab16-125">USD</span><span class="sxs-lookup"><span data-stu-id="4ab16-125">USD</span></span>|
| <span data-ttu-id="4ab16-126">Kỹ sư hệ thống cao cấp</span><span class="sxs-lookup"><span data-stu-id="4ab16-126">Senior Systems Engineer</span></span>|<span data-ttu-id="4ab16-127">Contoso US</span><span class="sxs-lookup"><span data-stu-id="4ab16-127">Contoso US</span></span>|<span data-ttu-id="4ab16-128">Hour</span><span class="sxs-lookup"><span data-stu-id="4ab16-128">Hour</span></span>| <span data-ttu-id="4ab16-129">150</span><span class="sxs-lookup"><span data-stu-id="4ab16-129">150</span></span>| <span data-ttu-id="4ab16-130">USD</span><span class="sxs-lookup"><span data-stu-id="4ab16-130">USD</span></span>|


<span data-ttu-id="4ab16-131">Khi bạn tắt **Tiêu đề chuẩn** làm thông số định giá và công cụ định giá Project Service tìm kiếm giá, thì công cụ đó sẽ chỉ sử dụng giá trị **Đơn vị tổ chức** từ ngữ cảnh nhập.</span><span class="sxs-lookup"><span data-stu-id="4ab16-131">When you turn off **Standard Title** as the pricing dimension, and the Project Service pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="4ab16-132">Nếu **Đơn vị tổ chức** của ngữ cảnh nhập là “Contoso Hoa Kỳ”, thì kết quả sẽ không xác định bởi vì cả hai hàng sẽ phù hợp.</span><span class="sxs-lookup"><span data-stu-id="4ab16-132">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="4ab16-133">Để tránh trường hợp này, khi bạn tạo **Giá theo vai trò**, Project Service xác thực rằng tổ hợp thông số là duy nhất.</span><span class="sxs-lookup"><span data-stu-id="4ab16-133">To avoid this scenario, when you create **Role Price** records, Project Service validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="4ab16-134">Nếu thông số bị tắt sau khi hồ sơ **Giá theo vai trò** được tạo, hạn chế này có thể bị vi phạm.</span><span class="sxs-lookup"><span data-stu-id="4ab16-134">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="4ab16-135">Do đó, trước khi tắt một thông số, bạn cần xóa tất cả các hàng **Giá theo vai trò** và **Tăng giá theo vai trò** đã điền sẵn giá trị thông số đó.</span><span class="sxs-lookup"><span data-stu-id="4ab16-135">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]