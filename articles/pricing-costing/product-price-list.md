---
title: Bảng giá sản phẩm
description: Chủ đề này cung cấp thông tin về bảng giá khi định giá theo danh mục, được sử dụng cho báo giá và hợp đồng dự án.
author: rumant
manager: AnnBe
ms.date: 04/05/2021
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
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e37f0bf9eef946ab4ebd658cef4e1269cbaf686d
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877517"
---
# <a name="product-price-lists"></a><span data-ttu-id="a8764-103">Bảng giá sản phẩm</span><span class="sxs-lookup"><span data-stu-id="a8764-103">Product price lists</span></span>

<span data-ttu-id="a8764-104">_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="a8764-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

 <span data-ttu-id="a8764-105">Trong Project Operations, **Bảng giá sản phẩm** và các thực thể hạng mục trong bảng giá có liên quan hỗ trợ chức năng định giá sản phẩm trên các mục mô tả hợp đồng và báo giá dựa trên sản phẩm.</span><span class="sxs-lookup"><span data-stu-id="a8764-105">In Project Operations, **Product price lists** and related price list item entities support functionality for pricing products on product-based quote and contract lines.</span></span> <span data-ttu-id="a8764-106">Đối với các sản phẩm dùng cho dự án, hồ sơ hạng mục trong bảng giá của bảng giá dự án sẽ được sử dụng.</span><span class="sxs-lookup"><span data-stu-id="a8764-106">For products used on projects, the price list item records for project price lists are used.</span></span> 

<span data-ttu-id="a8764-107">Sản phẩm nên được thiết lập để có chi phí và bảng giá mặc định trong danh mục sản phẩm.</span><span class="sxs-lookup"><span data-stu-id="a8764-107">Products should be set up so that they have default cost and price lists in the product catalog.</span></span> <span data-ttu-id="a8764-108">Sử dụng giá niêm yết, chi phí tiêu chuẩn và chi phí hiện tại để đặt cấu hình chi phí và bảng giá mặc định.</span><span class="sxs-lookup"><span data-stu-id="a8764-108">Use the list price, standard cost, and current cost to configure default cost and list prices.</span></span> <span data-ttu-id="a8764-109">Bảng giá mặc định chỉ dùng trên mô tả báo giá hoặc mô tả hợp đồng dự án khi hệ thống không thể tìm thấy mô tả bảng giá cho sản phẩm đó trong bảng giá sản phẩm cho báo giá hoặc hợp đồng dự án.</span><span class="sxs-lookup"><span data-stu-id="a8764-109">The default list prices are used on a quote line or a project contract line only when the system can't find a price list line for that product in the product price list for the quote or project contract.</span></span>

<span data-ttu-id="a8764-110">Giá vốn của mô tả danh mục sản phẩm có thể thay đổi giữa các báo giá.</span><span class="sxs-lookup"><span data-stu-id="a8764-110">The cost price of product catalog lines can be changed between quotes.</span></span> <span data-ttu-id="a8764-111">Khả năng này rất quan trọng, bởi vì nếu không theo dõi chính xác chi phí, bạn không thể xác định lợi nhuận hoạt động trên các tương tác dự án.</span><span class="sxs-lookup"><span data-stu-id="a8764-111">This capability is important, because if you don't accurately track costs, you can't determine operational profits on project engagements.</span></span> <span data-ttu-id="a8764-112">Theo mặc định, chi phí tiêu chuẩn của sản phẩm dùng làm giá vốn.</span><span class="sxs-lookup"><span data-stu-id="a8764-112">By default, the standard cost of the product is used as the cost price.</span></span> <span data-ttu-id="a8764-113">Tuy nhiên, giá vốn mặc định có thể được cập nhật trên mô tả báo giá nếu có giá vốn khác cho báo giá đó.</span><span class="sxs-lookup"><span data-stu-id="a8764-113">However, the default cost price can be updated on the quote line if there's a different cost price for that quote.</span></span>

## <a name="price-list-items"></a><span data-ttu-id="a8764-114">Hạng mục trong bảng giá</span><span class="sxs-lookup"><span data-stu-id="a8764-114">Price list items</span></span>

<span data-ttu-id="a8764-115">Bạn có thể thêm sản phẩm từ danh mục sản phẩm vào bảng giá khác.</span><span class="sxs-lookup"><span data-stu-id="a8764-115">You can add products from a product catalog to different price lists.</span></span> <span data-ttu-id="a8764-116">Mô tả bảng giá cho sản phẩm luôn tham chiếu một đơn vị cụ thể.</span><span class="sxs-lookup"><span data-stu-id="a8764-116">Price list lines for products always reference a specific unit.</span></span> <span data-ttu-id="a8764-117">Giá cho một sản phẩm trên hạng mục trong bảng giá có thể được đặt cấu hình ở dạng khoản tiền tệ.</span><span class="sxs-lookup"><span data-stu-id="a8764-117">Pricing for a product on price list items can be configured as a currency amount.</span></span> <span data-ttu-id="a8764-118">Ngoài ra, giá này có thể được đặt cấu hình ở dạng chức năng của bảng giá, chi phí hiện tại hoặc chi phí tiêu chuẩn.</span><span class="sxs-lookup"><span data-stu-id="a8764-118">Alternatively, it can be configured as a function of the list price, current cost, or standard cost.</span></span>

<span data-ttu-id="a8764-119">Chức năng định giá hỗ trợ nhiều tùy chọn làm tròn khi giá sản phẩm được đặt cấu hình ở dạng hàm số của giá niêm yết, chi phí tiêu chuẩn hoặc chi phí hiện tại.</span><span class="sxs-lookup"><span data-stu-id="a8764-119">Pricing functionality supports various rounding options when product prices are configured as a function of the list price, standard cost, or current cost.</span></span> <span data-ttu-id="a8764-120">Ngoài việc tận dụng nhiều phương pháp định giá và các tùy chọn làm tròn, bạn có thể liên kết danh sách giảm giá với các hạng mục trong bảng giá.</span><span class="sxs-lookup"><span data-stu-id="a8764-120">In addition to taking advantage of multiple pricing methods and rounding options, you can associate discount lists with price list items.</span></span> 

 
## <a name="default-product-price-list"></a><span data-ttu-id="a8764-121">Bảng giá sản phẩm mặc định</span><span class="sxs-lookup"><span data-stu-id="a8764-121">Default product price list</span></span>
<span data-ttu-id="a8764-122">Mỗi bản ghi khách hàng có trường **Bảng giá mặc định**, nơi bạn có thể chỉ định bảng giá khớp với đơn vị tiền tệ của khách hàng.</span><span class="sxs-lookup"><span data-stu-id="a8764-122">Each customer record has a **Default Price List** field, where you can specify a price list that matches the currency of the customer.</span></span> <span data-ttu-id="a8764-123">Giá trị mặc định sẽ không được nhập tự động vào trong trường này.</span><span class="sxs-lookup"><span data-stu-id="a8764-123">A default value isn't automatically entered in this field.</span></span> <span data-ttu-id="a8764-124">Khi một thỏa thuận giá tùy chỉnh có khách hàng cụ thể tồn tại, bạn có thể dùng trường này để liên kết bảng giá với khách hàng đó.</span><span class="sxs-lookup"><span data-stu-id="a8764-124">When a custom pricing agreement with a specific customer exists, you can use this field to associate a price list with that customer.</span></span>

<span data-ttu-id="a8764-125">Các thực thể Cơ hội, Báo giá và Hợp đồng dự án dùng các đơn hàng sau để nhập bảng giá sản phẩm mặc định.</span><span class="sxs-lookup"><span data-stu-id="a8764-125">The Opportunity, Quote, and Project Contract entities use the following order to enter default product price lists.</span></span> <span data-ttu-id="a8764-126">Cùng một thứ tự được dùng cho bảng giá sản phẩm.</span><span class="sxs-lookup"><span data-stu-id="a8764-126">The same order is used for project price lists.</span></span>

1.  <span data-ttu-id="a8764-127">Báo giá</span><span class="sxs-lookup"><span data-stu-id="a8764-127">Quote</span></span>
2.  <span data-ttu-id="a8764-128">Cơ hội</span><span class="sxs-lookup"><span data-stu-id="a8764-128">Opportunity</span></span>
3.  <span data-ttu-id="a8764-129">Khách hàng</span><span class="sxs-lookup"><span data-stu-id="a8764-129">Customer</span></span>
4.  <span data-ttu-id="a8764-130">Thiết đặt tổng thể</span><span class="sxs-lookup"><span data-stu-id="a8764-130">Global settings</span></span> 

<span data-ttu-id="a8764-131">Theo sản phẩm, trường **Sản phẩm** trên mô tả báo giá liệt kê tất cả sản phẩm hiện hoạt trong bảng giá sản phẩm của báo giá.</span><span class="sxs-lookup"><span data-stu-id="a8764-131">By default, the **Product** field on the quote line lists all the active products in the product price list of the quote.</span></span> <span data-ttu-id="a8764-132">Nếu sản phẩm đã bị hủy kích hoạt hoặc nếu đó là sản phẩm nháp, thì sản phẩm đó không được liệt kê ngay cả khi có trong bảng giá.</span><span class="sxs-lookup"><span data-stu-id="a8764-132">If a product has been inactivated, or if it's a draft product, it isn't listed, even if it's in the price list.</span></span> 

<span data-ttu-id="a8764-133">Mô tả danh mục sản phẩm được thêm vào mô tả hóa đơn trên hóa đơn đầu tiên được tạo cho hợp đồng dự án.</span><span class="sxs-lookup"><span data-stu-id="a8764-133">Product catalog lines are added as invoice lines on the first invoice that is created for a project contract.</span></span> <span data-ttu-id="a8764-134">Trên hóa đơn nháp, những mô tả hóa đơn đó có thể bị xóa.</span><span class="sxs-lookup"><span data-stu-id="a8764-134">On a draft invoice, those invoice lines can be deleted.</span></span> <span data-ttu-id="a8764-135">Trong trường hợp đó, các mô tả sẽ xuất hiện trên hóa đơn tiếp theo cho đến khi chúng được lập hóa đơn hoặc cho đến khi hóa đơn được gửi đến khách hàng.</span><span class="sxs-lookup"><span data-stu-id="a8764-135">In that case, the lines will appear on a subsequent invoice until they are invoiced, or until the invoice is sent to the customer.</span></span> <span data-ttu-id="a8764-136">Bạn không thể lập hóa đơn cho một phần số lượng theo dòng mô tả hóa đơn sản phẩm.</span><span class="sxs-lookup"><span data-stu-id="a8764-136">You can't invoice a partial quantity of a product invoice line.</span></span> <span data-ttu-id="a8764-137">Khi mô tả sản phẩm từ hóa đơn hợp đồng được lập hóa đơn, các số liệu thực tế sẽ được tạo.</span><span class="sxs-lookup"><span data-stu-id="a8764-137">When the product lines from the project contract are invoiced, actuals are created.</span></span> <span data-ttu-id="a8764-138">Tuy nhiên, các số liệu thực tế đó không liên kết với thực thể dự án liên quan.</span><span class="sxs-lookup"><span data-stu-id="a8764-138">However, those actuals aren't linked to the related project entity.</span></span> <span data-ttu-id="a8764-139">Nói cách khác, các mô tả hợp đồng dự án dựa trên sản phẩm độc lập với mọi việc sử dụng dựa trên dự án.</span><span class="sxs-lookup"><span data-stu-id="a8764-139">In other words, product-based project contract lines are independent of any project-based use.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
