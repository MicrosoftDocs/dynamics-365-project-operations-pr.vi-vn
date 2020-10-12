---
title: Bảng giá sản phẩm
description: Chủ đề này cung cấp thông tin về bảng giá khi định giá theo danh mục, được sử dụng cho báo giá và hợp đồng dự án.
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
ms.openlocfilehash: 3570aeb78804e9b267caa55a27e02d6c8df9a5c6
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898197"
---
# <a name="product-price-lists"></a><span data-ttu-id="f931f-103">Bảng giá sản phẩm</span><span class="sxs-lookup"><span data-stu-id="f931f-103">Product price lists</span></span>

<span data-ttu-id="f931f-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="f931f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f931f-105">Các thuộc tính bảng giá và hạng mục trong bảng giá hỗ trợ giá danh mục sản phẩm.</span><span class="sxs-lookup"><span data-stu-id="f931f-105">Price lists and price list item entities support product catalog pricing.</span></span> <span data-ttu-id="f931f-106">Đối với hầu hết các phần, chức năng này dùng cho mô tả dựa trên danh mục trên báo giá dự án và hợp đồng dự án.</span><span class="sxs-lookup"><span data-stu-id="f931f-106">For the most part, this functionality is used for catalog-based lines on project quotes and project contracts.</span></span>

<span data-ttu-id="f931f-107">Đối với các mô tả dựa trên dự án, hợp đồng đại diện cho thỏa thuận sau khi thắng.</span><span class="sxs-lookup"><span data-stu-id="f931f-107">For project-based lines, a contract represents the deal after it was won.</span></span> <span data-ttu-id="f931f-108">Bởi vì quá trình đàm phán thường diễn ra trước khi thắng, nên giá đính kèm với báo giá luôn được sao chép ở dạng nguyên trạng vào bảng giá mới và đính kèm với hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="f931f-108">Because the process of negotiation usually precedes the win, the pricing that is attached to the quote is always copied as-is to a new price list and attached to the contract.</span></span> <span data-ttu-id="f931f-109">Bảng giá mới này không thể thay đổi được ngoài phạm vi của hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="f931f-109">This new price list can't be changed outside the scope of the contract.</span></span> <span data-ttu-id="f931f-110">Hạn chế này giúp bảo vệ bảng giá được thương lượng khỏi mọi thay đổi về giá xảy ra trong bảng giá chính.</span><span class="sxs-lookup"><span data-stu-id="f931f-110">This limitation helps protect the rate card that was negotiated from any price changes that occur in the master price list.</span></span>

<span data-ttu-id="f931f-111">Sản phẩm nên được thiết lập để có chi phí và bảng giá mặc định trong danh mục sản phẩm.</span><span class="sxs-lookup"><span data-stu-id="f931f-111">Products should be set up so that they have default cost and price lists in the product catalog.</span></span> <span data-ttu-id="f931f-112">Sử dụng giá niêm yết, chi phí tiêu chuẩn và chi phí hiện tại để đặt cấu hình chi phí và bảng giá mặc định.</span><span class="sxs-lookup"><span data-stu-id="f931f-112">Use the list price, standard cost, and current cost to configure default cost and list prices.</span></span> <span data-ttu-id="f931f-113">Bảng giá mặc định chỉ dùng trên mô tả báo giá hoặc mô tả hợp đồng dự án khi hệ thống không thể tìm thấy mô tả bảng giá cho sản phẩm đó trong bảng giá sản phẩm cho báo giá hoặc hợp đồng dự án.</span><span class="sxs-lookup"><span data-stu-id="f931f-113">The default list prices are used on a quote line or a project contract line only when the system can't find a price list line for that product in the product price list for the quote or project contract.</span></span>

<span data-ttu-id="f931f-114">Giá vốn của mô tả danh mục sản phẩm có thể thay đổi giữa các báo giá.</span><span class="sxs-lookup"><span data-stu-id="f931f-114">The cost price of product catalog lines can be changed between quotes.</span></span> <span data-ttu-id="f931f-115">Khả năng này rất quan trọng, bởi vì nếu không theo dõi chính xác chi phí, bạn không thể xác định lợi nhuận hoạt động trên các tương tác dự án.</span><span class="sxs-lookup"><span data-stu-id="f931f-115">This capability is important, because if you don't accurately track costs, you can't determine operational profits on project engagements.</span></span> <span data-ttu-id="f931f-116">Theo mặc định, chi phí tiêu chuẩn của sản phẩm dùng làm giá vốn.</span><span class="sxs-lookup"><span data-stu-id="f931f-116">By default, the standard cost of the product is used as the cost price.</span></span> <span data-ttu-id="f931f-117">Tuy nhiên, giá vốn mặc định có thể được cập nhật trên mô tả báo giá nếu có giá vốn khác cho báo giá đó.</span><span class="sxs-lookup"><span data-stu-id="f931f-117">However, the default cost price can be updated on the quote line if there's a different cost price for that quote.</span></span>

## <a name="price-list-items"></a><span data-ttu-id="f931f-118">Hạng mục trong bảng giá</span><span class="sxs-lookup"><span data-stu-id="f931f-118">Price list items</span></span>

<span data-ttu-id="f931f-119">Bạn có thể thêm sản phẩm từ danh mục sản phẩm vào bảng giá khác.</span><span class="sxs-lookup"><span data-stu-id="f931f-119">You can add products from a product catalog to different price lists.</span></span> <span data-ttu-id="f931f-120">Mô tả bảng giá cho sản phẩm luôn tham chiếu một đơn vị cụ thể.</span><span class="sxs-lookup"><span data-stu-id="f931f-120">Price list lines for products always reference a specific unit.</span></span> <span data-ttu-id="f931f-121">Giá cho một sản phẩm trên hạng mục trong bảng giá có thể được đặt cấu hình ở dạng khoản tiền tệ.</span><span class="sxs-lookup"><span data-stu-id="f931f-121">Pricing for a product on price list items can be configured as a currency amount.</span></span> <span data-ttu-id="f931f-122">Ngoài ra, giá này có thể được đặt cấu hình ở dạng chức năng của bảng giá, chi phí hiện tại hoặc chi phí tiêu chuẩn.</span><span class="sxs-lookup"><span data-stu-id="f931f-122">Alternatively, it can be configured as a function of the list price, current cost, or standard cost.</span></span>

<span data-ttu-id="f931f-123">PSA hỗ trợ nhiều tùy chọn làm tròn khi giá được đặt cấu hình ở dạng chức năng của bảng giá, chi phí tiêu chuẩn hoặc chi phí hiện tại.</span><span class="sxs-lookup"><span data-stu-id="f931f-123">PSA supports various rounding options when prices are configured as a function of the list price, standard cost, or current cost.</span></span> <span data-ttu-id="f931f-124">Ngoài việc tận dụng nhiều phương pháp định giá và các tùy chọn làm tròn, bạn có thể liên kết danh sách giảm giá với các hạng mục trong bảng giá.</span><span class="sxs-lookup"><span data-stu-id="f931f-124">In addition to taking advantage of multiple pricing methods and rounding options, you can associate discount lists with price list items.</span></span> 

<span data-ttu-id="f931f-125">Khi bạn tạo một bảng giá tùy chỉnh mới cho báo giá bằng cách chọn **Tạo định giá tùy chỉnh** trên trang **Báo giá dự án**, một bản sao của bảng giá sẽ được tạo và trường **Thực thể** trên tiêu đề của bảng giá mới sẽ được đặt thành **Thực thể bán hàng**.</span><span class="sxs-lookup"><span data-stu-id="f931f-125">When you create a new custom price list for a quote by selecting **Create Custom Pricing** on the **Project Quote** page, a copy of the price list is made, and the **Entity** field on the header of the new price list is set to **Sales Entity**.</span></span> <span data-ttu-id="f931f-126">Tên của bảng giá mới được gắn với tên của báo giá và dấu thời gian.</span><span class="sxs-lookup"><span data-stu-id="f931f-126">The name of the new price list is appended with the name of the quote and a timestamp.</span></span> <span data-ttu-id="f931f-127">Bạn cũng có thể dùng tên của bảng giá mới và tên của báo giá trong quy trình làm việc tùy chỉnh để kích hoạt đánh giá hoặc phê duyệt bổ sung cho báo giá sử dụng giá tùy chỉnh.</span><span class="sxs-lookup"><span data-stu-id="f931f-127">You also can use the name of the new price list and the name of the quote in custom workflows to trigger additional review and approvals for quotes that use custom pricing.</span></span>

 
## <a name="default-product-price-list"></a><span data-ttu-id="f931f-128">Bảng giá sản phẩm mặc định</span><span class="sxs-lookup"><span data-stu-id="f931f-128">Default product price list</span></span>
<span data-ttu-id="f931f-129">Mỗi bản ghi khách hàng có trường **Bảng giá mặc định**, nơi bạn có thể chỉ định bảng giá khớp với đơn vị tiền tệ của khách hàng.</span><span class="sxs-lookup"><span data-stu-id="f931f-129">Each customer record has a **Default Price List** field, where you can specify a price list that matches the currency of the customer.</span></span> <span data-ttu-id="f931f-130">Giá trị mặc định sẽ không được nhập tự động vào trong trường này.</span><span class="sxs-lookup"><span data-stu-id="f931f-130">A default value isn't automatically entered in this field.</span></span> <span data-ttu-id="f931f-131">Khi một thỏa thuận giá tùy chỉnh có khách hàng cụ thể tồn tại, bạn có thể dùng trường này để liên kết bảng giá với khách hàng đó.</span><span class="sxs-lookup"><span data-stu-id="f931f-131">When a custom pricing agreement with a specific customer exists, you can use this field to associate a price list with that customer.</span></span>

<span data-ttu-id="f931f-132">Các thực thể Cơ hội, Báo giá và Hợp đồng dự án dùng các đơn hàng sau để nhập bảng giá sản phẩm mặc định.</span><span class="sxs-lookup"><span data-stu-id="f931f-132">The Opportunity, Quote, and Project Contract entities use the following order to enter default product price lists.</span></span> <span data-ttu-id="f931f-133">Cùng một thứ tự được dùng cho bảng giá sản phẩm.</span><span class="sxs-lookup"><span data-stu-id="f931f-133">The same order is used for project price lists.</span></span>

1.  <span data-ttu-id="f931f-134">Báo giá</span><span class="sxs-lookup"><span data-stu-id="f931f-134">Quote</span></span>
2.  <span data-ttu-id="f931f-135">Cơ hội</span><span class="sxs-lookup"><span data-stu-id="f931f-135">Opportunity</span></span>
3.  <span data-ttu-id="f931f-136">Khách hàng</span><span class="sxs-lookup"><span data-stu-id="f931f-136">Customer</span></span>
4.  <span data-ttu-id="f931f-137">Thiết đặt tổng thể</span><span class="sxs-lookup"><span data-stu-id="f931f-137">Global settings</span></span> 

<span data-ttu-id="f931f-138">Theo sản phẩm, trường **Sản phẩm** trên mô tả báo giá liệt kê tất cả sản phẩm hiện hoạt trong bảng giá sản phẩm của báo giá.</span><span class="sxs-lookup"><span data-stu-id="f931f-138">By default, the **Product** field on the quote line lists all the active products in the product price list of the quote.</span></span> <span data-ttu-id="f931f-139">Nếu sản phẩm đã bị hủy kích hoạt hoặc nếu đó là sản phẩm nháp, thì sản phẩm đó không được liệt kê ngay cả khi có trong bảng giá.</span><span class="sxs-lookup"><span data-stu-id="f931f-139">If a product has been inactivated, or if it's a draft product, it isn't listed, even if it's in the price list.</span></span> 

<span data-ttu-id="f931f-140">Mô tả danh mục sản phẩm được thêm vào mô tả hóa đơn trên hóa đơn đầu tiên được tạo cho hợp đồng dự án.</span><span class="sxs-lookup"><span data-stu-id="f931f-140">Product catalog lines are added as invoice lines on the first invoice that is created for a project contract.</span></span> <span data-ttu-id="f931f-141">Trên hóa đơn nháp, những mô tả hóa đơn đó có thể bị xóa.</span><span class="sxs-lookup"><span data-stu-id="f931f-141">On a draft invoice, those invoice lines can be deleted.</span></span> <span data-ttu-id="f931f-142">Trong trường hợp đó, các mô tả sẽ xuất hiện trên hóa đơn tiếp theo cho đến khi chúng được lập hóa đơn hoặc cho đến khi hóa đơn được gửi đến khách hàng.</span><span class="sxs-lookup"><span data-stu-id="f931f-142">In that case, the lines will appear on a subsequent invoice until they are invoiced, or until the invoice is sent to the customer.</span></span> <span data-ttu-id="f931f-143">Bạn không thể lập hóa đơn cho một phần số lượng theo dòng mô tả hóa đơn sản phẩm.</span><span class="sxs-lookup"><span data-stu-id="f931f-143">You can't invoice a partial quantity of a product invoice line.</span></span> <span data-ttu-id="f931f-144">Khi mô tả sản phẩm từ hóa đơn hợp đồng được lập hóa đơn, các số liệu thực tế sẽ được tạo.</span><span class="sxs-lookup"><span data-stu-id="f931f-144">When the product lines from the project contract are invoiced, actuals are created.</span></span> <span data-ttu-id="f931f-145">Tuy nhiên, các số liệu thực tế đó không liên kết với thực thể dự án liên quan.</span><span class="sxs-lookup"><span data-stu-id="f931f-145">However, those actuals aren't linked to the related project entity.</span></span> <span data-ttu-id="f931f-146">Nói cách khác, các mô tả hợp đồng dự án dựa trên sản phẩm độc lập với mọi việc sử dụng dựa trên dự án.</span><span class="sxs-lookup"><span data-stu-id="f931f-146">In other words, product-based project contract lines are independent of any project-based use.</span></span> <span data-ttu-id="f931f-147">Mức tiêu thụ vật liệu trên dự án sẽ không được theo dõi.</span><span class="sxs-lookup"><span data-stu-id="f931f-147">Material consumption on projects isn't tracked.</span></span>