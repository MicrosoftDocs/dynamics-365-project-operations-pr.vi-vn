---
title: Thiết lập bảng giá bán hàng
description: Chủ đề này cung cấp thông tin về bảng giá bán hàng cho giá dự án.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 2a66802adfcadab7b4d34149b146ca3cb27c903e
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896487"
---
# <a name="sales-price-list-setup"></a><span data-ttu-id="e5ac3-103">Thiết lập bảng giá bán hàng</span><span class="sxs-lookup"><span data-stu-id="e5ac3-103">Sales price list setup</span></span>

<span data-ttu-id="e5ac3-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="e5ac3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e5ac3-105">Đối với báo giá dự án và hợp đồng, bảng giá dự án có mô hình thay thế giá khác với bảng giá sản phẩm.</span><span class="sxs-lookup"><span data-stu-id="e5ac3-105">For project quotes and contracts, a project price list has a different price override pattern than a product price list.</span></span> <span data-ttu-id="e5ac3-106">Trên dòng báo giá dựa trên danh mục sản phẩm, bạn có thể thay thế giá cho các vai trò và danh mục trực tiếp trên dòng báo giá vì mỗi dòng báo giá trỏ đến chính xác một mục trong danh mục.</span><span class="sxs-lookup"><span data-stu-id="e5ac3-106">On a product catalog–based quote line, you can override the price to roles and categories directly on the quote line, because each quote line points to exactly one catalog item.</span></span> <span data-ttu-id="e5ac3-107">Tuy nhiên, trên dòng báo giá dựa trên dự án, bạn không thể thay thế giá cho vai trò và danh mục trực tiếp trên dòng báo giá.</span><span class="sxs-lookup"><span data-stu-id="e5ac3-107">However, on a project-based quote line, you can't override the price to roles and categories directly on the quote line.</span></span> <span data-ttu-id="e5ac3-108">Bạn có thể sử dụng bảng giá dự án để làm việc với hai mô hình thay thế khác nhau.</span><span class="sxs-lookup"><span data-stu-id="e5ac3-108">You can use the project price list to work with the two distinct override patterns.</span></span>

> [!NOTE]
> <span data-ttu-id="e5ac3-109">Bạn nên có một bảng giá riêng cho tài nguyên dự án và các mục trên danh mục của bạn vì sự khác biệt về hành vi giữa hai thứ này khi bạn thay thế giá.</span><span class="sxs-lookup"><span data-stu-id="e5ac3-109">We recommend that you have a separate price list for your project resources and your catalog items, because of the behavior differences between the two when you override pricing.</span></span>

<span data-ttu-id="e5ac3-110">Mỗi thực thể sau có thể có một hoặc nhiều bảng giá bán hàng liên quan cho giá dự án:</span><span class="sxs-lookup"><span data-stu-id="e5ac3-110">Each of the following entities can have one or more associated sales price lists for project pricing:</span></span>

- <span data-ttu-id="e5ac3-111">Khách hàng (tài khoản)</span><span class="sxs-lookup"><span data-stu-id="e5ac3-111">Customer (account)</span></span> 
- <span data-ttu-id="e5ac3-112">Cơ hội</span><span class="sxs-lookup"><span data-stu-id="e5ac3-112">Opportunity</span></span> 
- <span data-ttu-id="e5ac3-113">Báo giá</span><span class="sxs-lookup"><span data-stu-id="e5ac3-113">Quote</span></span> 
- <span data-ttu-id="e5ac3-114">Hợp đồng Dự án</span><span class="sxs-lookup"><span data-stu-id="e5ac3-114">Project Contract</span></span>

<span data-ttu-id="e5ac3-115">Một liên kết các thực thể này với bảng giá được biểu thị bằng bảng giá dự án.</span><span class="sxs-lookup"><span data-stu-id="e5ac3-115">The association of these entities with a price list is indicated by the project price lists.</span></span> <span data-ttu-id="e5ac3-116">Bạn có thể liên kết một hoặc nhiều bảng giá với các thực thể bán hàng khách hàng, cơ hội, báo giá và hợp đồng dự án.</span><span class="sxs-lookup"><span data-stu-id="e5ac3-116">You can associate one or more price lists with the Customer, Opportunity, Quote, and Project Contract sales entities.</span></span>

<span data-ttu-id="e5ac3-117">Bảng giá dự án mặc định không tự động nhập vào bản ghi khách hàng.</span><span class="sxs-lookup"><span data-stu-id="e5ac3-117">A default project price list isn't automatically entered on a customer record.</span></span> <span data-ttu-id="e5ac3-118">Tuy nhiên, bạn có thể tự đính kèm bảng giá dự án vào bản ghi khách hàng.</span><span class="sxs-lookup"><span data-stu-id="e5ac3-118">However, you can manually attach a project price list to the customer record.</span></span> <span data-ttu-id="e5ac3-119">Tuy nhiên, bạn nên đính kèm bảng giá dự án chỉ khi có thỏa thuận giá tùy chỉnh với khách hàng.</span><span class="sxs-lookup"><span data-stu-id="e5ac3-119">Nevertheless, you should manually attach a project price list only when you have a custom pricing agreement with the customer.</span></span> 

<span data-ttu-id="e5ac3-120">Khi một bảng giá dự án được đính kèm vào một thực thể bán hàng, thông tin sau đây được xác thực:</span><span class="sxs-lookup"><span data-stu-id="e5ac3-120">When a project price list is attached to a sales entity, the following information is validated:</span></span>

- <span data-ttu-id="e5ac3-121">Bảng giá là có bối cảnh **Bán hàng**.</span><span class="sxs-lookup"><span data-stu-id="e5ac3-121">The price list has a context of **Sales**.</span></span> 
- <span data-ttu-id="e5ac3-122">Tiền tệ của bảng giá phải khớp với loại tiền của khách hàng.</span><span class="sxs-lookup"><span data-stu-id="e5ac3-122">The price list currency matches the customer currency.</span></span> 

<span data-ttu-id="e5ac3-123">Trên hợp đồng dự án, thứ tự ưu tiên sau đây được sử dụng để tự động đặt bảng giá dự án liên quan:</span><span class="sxs-lookup"><span data-stu-id="e5ac3-123">On a project contract, the following order of precedence is used to automatically set related project price lists:</span></span>

1. <span data-ttu-id="e5ac3-124">Báo giá</span><span class="sxs-lookup"><span data-stu-id="e5ac3-124">Quote</span></span>
2. <span data-ttu-id="e5ac3-125">Cơ hội</span><span class="sxs-lookup"><span data-stu-id="e5ac3-125">Opportunity</span></span>
3. <span data-ttu-id="e5ac3-126">Khách hàng</span><span class="sxs-lookup"><span data-stu-id="e5ac3-126">Customer</span></span> 
4. <span data-ttu-id="e5ac3-127">Thiết đặt tổng thể</span><span class="sxs-lookup"><span data-stu-id="e5ac3-127">Global settings</span></span> 

<span data-ttu-id="e5ac3-128">Khi một bảng giá dự án được nhập theo mặc định, hệ thống sẽ xác thực rằng loại tiền tệ khớp với tiền tệ của khách hàng và các bảng giá mặc định đã nhập có bối cảnh **Bán hàng**.</span><span class="sxs-lookup"><span data-stu-id="e5ac3-128">When a project price list is entered by default, the system validates that the currency matches the customer’s currency, and that the default price lists that have been entered have a context of **Sales**.</span></span>

<span data-ttu-id="e5ac3-129">Bạn có thể liên kết nhiều bảng giá dự án với các thực thể khách hàng, cơ hội, báo giá và hợp đồng dự án.</span><span class="sxs-lookup"><span data-stu-id="e5ac3-129">You can associate multiple project price lists with the Customer, Opportunity, Quote, and Project Contract entities.</span></span> <span data-ttu-id="e5ac3-130">Khả năng này hỗ trợ giá mặc định theo ngày cho một hợp đồng dự án dài, nơi bạn có thể yêu cầu nhiều bảng giá để tính đến khả năng cập nhật giá do lạm phát.</span><span class="sxs-lookup"><span data-stu-id="e5ac3-130">This capability supports date-specific default prices for a long-running project contract, where you might require more than one price list to account for price updates that occur because of inflation.</span></span> <span data-ttu-id="e5ac3-131">Tuy nhiên, nếu bảng giá mà bạn liên kết với thực thể khách hàng, cơ hội, báo giá hoặc hợp đồng dự án có ngày hiệu lực chồng chéo, thì giá mặc định có thể không chính xác.</span><span class="sxs-lookup"><span data-stu-id="e5ac3-131">However, if the price lists that you associate with the Customer, Opportunity, Quote, or Project Contract entity have overlapping date effectivity, the default prices might be incorrect.</span></span> <span data-ttu-id="e5ac3-132">Do đó, bạn phải đảm bảo rằng bảng giá dự án có ngày hiệu lực chồng chéo không liên kết với những thực thể đó.</span><span class="sxs-lookup"><span data-stu-id="e5ac3-132">Therefore, you should make sure that project price lists that have overlapping date effectivity aren't associated with those entities.</span></span>
