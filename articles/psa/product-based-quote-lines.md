---
title: Mô tả báo giá dựa trên sản phẩm
description: Chủ đề này cung cấp thông tin về mô tả báo giá dựa trên sản phẩm.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 55a5b5041a494892e6d96bf24e1bc132a26521dc
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087288"
---
# <a name="product-based-quote-lines"></a><span data-ttu-id="64b16-103">Mô tả báo giá dựa trên sản phẩm</span><span class="sxs-lookup"><span data-stu-id="64b16-103">Product-based quote lines</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


<span data-ttu-id="64b16-104">Bạn có thể tạo mô tả báo giá dựa trên sản phẩm trong Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="64b16-104">You can create product-based quote lines in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="64b16-105">Mô tả báo giá dựa trên sản phẩm có thể là mô tả chọn thêm hoặc các mục từ danh mục sản phẩm.</span><span class="sxs-lookup"><span data-stu-id="64b16-105">Product-based quote lines can be "write-in" lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="64b16-106">Danh mục sản phẩm</span><span class="sxs-lookup"><span data-stu-id="64b16-106">Product catalog</span></span>

<span data-ttu-id="64b16-107">Các sản phẩm trong danh mục sản phẩm Dynamics 365 có đơn vị mặc định và nhóm đơn vị đo.</span><span class="sxs-lookup"><span data-stu-id="64b16-107">The products in a Dynamics 365 product catalog have a default unit and unit group.</span></span> <span data-ttu-id="64b16-108">Nếu một số sản phẩm có cùng nhóm thuộc tính, bạn có thể tạo dòng sản phẩm cũng có các thuộc tính đó.</span><span class="sxs-lookup"><span data-stu-id="64b16-108">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="64b16-109">Tất cả sản phẩm trong một dòng sản phẩm thừa kế cùng bộ thuộc tính.</span><span class="sxs-lookup"><span data-stu-id="64b16-109">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="64b16-110">Ví dụ: công ty bán các giấy phép gói đăng ký cho một loạt các phần mềm.</span><span class="sxs-lookup"><span data-stu-id="64b16-110">For example, a company sells subscription licenses for a variety of software.</span></span> <span data-ttu-id="64b16-111">Tất cả phần mềm gói đăng ký có 2 thuộc tính sau:</span><span class="sxs-lookup"><span data-stu-id="64b16-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="64b16-112">Số người dùng</span><span class="sxs-lookup"><span data-stu-id="64b16-112">Number of users</span></span> 
- <span data-ttu-id="64b16-113">Thời gian đăng ký (trong tháng)</span><span class="sxs-lookup"><span data-stu-id="64b16-113">Subscription duration (in months)</span></span>

<span data-ttu-id="64b16-114">Cách tốt nhất để duy trì loại danh mục này là tạo dòng sản phẩm có tên **Phần mềm đăng ký** và **Số người dùng** và **Khoảng thời gian đăng ký** ở dạng thuộc tính.</span><span class="sxs-lookup"><span data-stu-id="64b16-114">A good way to maintain this type of catalog is to create a product family that is named **Subscription Software** , and that has **Number of users** and **Subscription duration** as attributes.</span></span> <span data-ttu-id="64b16-115">Sau đó, bạn có thể thêm từng sản phẩm, chẳng hạn như **Dynamics 365 Sales** hoặc **Dynamics 365 Field Service** vào dòng sản phẩm **Phần mềm đăng ký**.</span><span class="sxs-lookup"><span data-stu-id="64b16-115">You can then add individual products, such as **Dynamics 365 Sales** or **Dynamics 365 Field Service** to the **Subscription Software** product family.</span></span>

## <a name="adding-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="64b16-116">Thêm các mục danh mục sản phẩm vào báo giá dự án</span><span class="sxs-lookup"><span data-stu-id="64b16-116">Adding product catalog items to a project quote</span></span>

<span data-ttu-id="64b16-117">Các trang báo giá dự án và hợp đồng dự án có các phần cho 2 loại mô tả: mô tả dựa trên dự án và mô tả dựa trên sản phẩm.</span><span class="sxs-lookup"><span data-stu-id="64b16-117">Project quote and project contract pages have sections for two types of lines: project-based lines and product-based lines.</span></span> <span data-ttu-id="64b16-118">Đối với các mô tả dựa trên sản phẩm, Dynamics 365 dùng để thêm mục từ danh mục sản phẩm vào báo giá.</span><span class="sxs-lookup"><span data-stu-id="64b16-118">For product-based lines, Dynamics 365 is used to add items from a product catalog to a quote.</span></span> <span data-ttu-id="64b16-119">Danh sách thả xuống trên mô tả báo giá hoặc mô tả hợp đồng dự án bao gồm tất cả sản phẩm và đơn vị trong bảng giá sản phẩm được đính kèm với báo giá hoặc hợp đồng dự án.</span><span class="sxs-lookup"><span data-stu-id="64b16-119">The drop-down list on the quote line or project contract line includes all the products and units in the product price list that is attached to the quote or project contract.</span></span> <span data-ttu-id="64b16-120">Bạn cũng có thể thêm các sản phẩm không phải một phần trong bảng giá sản phẩm của báo giá.</span><span class="sxs-lookup"><span data-stu-id="64b16-120">You can also add products that aren't part of quote's product price list.</span></span>

<span data-ttu-id="64b16-121">Ngoài ra, bạn có thể chọn các sản phẩm từ bảng giá khác hoặc chọn các sản phẩm trực tiếp từ danh mục sản phẩm.</span><span class="sxs-lookup"><span data-stu-id="64b16-121">Additionally, you can select products from other price lists, or you can select products directly from the product catalog.</span></span> <span data-ttu-id="64b16-122">Khi bạn chọn các sản phẩm trực tiếp từ danh mục sản phẩm, bảng giá mặc định của sản phẩm đó dùng để nhận giá bán hàng của sản phẩm.</span><span class="sxs-lookup"><span data-stu-id="64b16-122">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="64b16-123">Nếu một bảng giá mặc định không được đặt, giá sẽ được đặt về 0 (không).</span><span class="sxs-lookup"><span data-stu-id="64b16-123">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="64b16-124">Nếu mô tả báo giá dựa trên danh mục sản phẩm, bạn có thể thay thế giá bán hàng trực tiếp trên mô tả báo giá.</span><span class="sxs-lookup"><span data-stu-id="64b16-124">If a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="64b16-125">Lưu ý rằng mô tả báo giá trong Dynamics 365 có trường **Giá**.</span><span class="sxs-lookup"><span data-stu-id="64b16-125">Note that a quote line in Dynamics 365 has a **Pricing** field.</span></span> <span data-ttu-id="64b16-126">Có hai giá trị:</span><span class="sxs-lookup"><span data-stu-id="64b16-126">Two values are available:</span></span>

- <span data-ttu-id="64b16-127">Thay thế giá</span><span class="sxs-lookup"><span data-stu-id="64b16-127">Override pricing</span></span>  
- <span data-ttu-id="64b16-128">Dùng mặc định</span><span class="sxs-lookup"><span data-stu-id="64b16-128">Use default</span></span>

<span data-ttu-id="64b16-129">Nếu bạn đặt trường này thành **Thay thế giá** , Dynamics 365 không đặt giá mặc định.</span><span class="sxs-lookup"><span data-stu-id="64b16-129">If you set this field to **Override pricing** , Dynamics 365 doesn't set a default price.</span></span> <span data-ttu-id="64b16-130">Bạn phải nhập giá cho sản phẩm trên mô tả báo giá.</span><span class="sxs-lookup"><span data-stu-id="64b16-130">You must enter a price for the product on the quote line.</span></span> <span data-ttu-id="64b16-131">Nếu bạn đặt trường này thành **Dùng mặc định** , Dynamics 365 sử dụng giá bán hàng mặc định và khóa trường để ngăn chỉnh sửa.</span><span class="sxs-lookup"><span data-stu-id="64b16-131">If you set this field to **Use default** , Dynamics 365 uses the default sales price and locks the field to prevent editing.</span></span>

<span data-ttu-id="64b16-132">Sau khi bạn cài đặt PSA, giá bán hàng mặc định được nhập trên mô tả dựa trên sản phẩm trên báo giá.</span><span class="sxs-lookup"><span data-stu-id="64b16-132">After you install PSA, default sales prices are entered on the product-based lines on a quote.</span></span> <span data-ttu-id="64b16-133">Sau đó, trường **Giá** được đặt thành **Thay thế giá** để bạn có thể chỉnh sửa giá mặc định trên mô tả báo giá.</span><span class="sxs-lookup"><span data-stu-id="64b16-133">The **Pricing** field is then set to **Override pricing** so that you can edit the default price on the quote lines.</span></span>

> ![Đặt giá thay thế](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a><span data-ttu-id="64b16-135">Yếu tố số lượng cho sản phẩm</span><span class="sxs-lookup"><span data-stu-id="64b16-135">Quantity factors for products</span></span>

<span data-ttu-id="64b16-136">PSA sử dụng các yếu tố số lượng để hỗ trợ việc bán các sản phẩm dựa trên đăng ký.</span><span class="sxs-lookup"><span data-stu-id="64b16-136">PSA uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="64b16-137">Đối với các sản phẩm dựa trên đăng ký, số lượng trên báo giá hoặc mô tả hợp đồng dự án được thể hiện ở dạng số tháng người dùng.</span><span class="sxs-lookup"><span data-stu-id="64b16-137">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user months.</span></span>

<span data-ttu-id="64b16-138">Thông thường, giá phần mềm đăng ký được lưu trữ trong danh mục ở dạng giá cho mỗi người dùng mỗi tháng.</span><span class="sxs-lookup"><span data-stu-id="64b16-138">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="64b16-139">Tuy nhiên, bạn có thể sử dụng mô tả thời gian khác thay thế.</span><span class="sxs-lookup"><span data-stu-id="64b16-139">However, you can use other time descriptions instead.</span></span> <span data-ttu-id="64b16-140">Trong quá trình bán hàng, giá trên mô tả báo giá thường là giá trên mỗi người dùng, mỗi tháng được đại lý bán hàng CNTT thương lượng và giảm giá.</span><span class="sxs-lookup"><span data-stu-id="64b16-140">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="64b16-141">Mỗi thỏa thuận có một số lượng người dùng khác nhau và số lượng tháng đăng ký khác nhau.</span><span class="sxs-lookup"><span data-stu-id="64b16-141">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="64b16-142">Số lượng được dùng để tính toán lượng mô tả báo giá là sản phẩm của số lượng người dùng và số lượng tháng đăng ký.</span><span class="sxs-lookup"><span data-stu-id="64b16-142">The quantity that is used to compute the amount of the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="64b16-143">Để hỗ trợ loại bán hàng này, PSA giới thiệu khái nhiệm yếu tố số lượng.</span><span class="sxs-lookup"><span data-stu-id="64b16-143">To support this type of sale, PSA introduced the concept of quantity factors.</span></span> <span data-ttu-id="64b16-144">Yếu tố số lượng dựa vào các thuộc tính sản phẩm trong Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="64b16-144">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="64b16-145">Khi bạn đặt cấu hình các thuộc tính cụ thể cho sản phẩm, PSA cho phép bạn gắn cờ một tập con của các thuộc tính đó hoặc tất cả thuộc tính ở dạng các yếu tố số lượng.</span><span class="sxs-lookup"><span data-stu-id="64b16-145">When you configure specific properties for a product, PSA lets you flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="64b16-146">PSA xác thực rằng chỉ có thuộc tính số hoặc các thuộc tính sản phẩm có loại dữ liệu số được gắn cờ ở dạng yếu tố số lượng.</span><span class="sxs-lookup"><span data-stu-id="64b16-146">PSA validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="64b16-147">Khi sản phẩm mà các yếu tố số lượng được đặt cấu hình được thêm vào mô tả báo giá, thì trường **Số lượng** trên mô tả báo giá trở thành trường chỉ đọc.</span><span class="sxs-lookup"><span data-stu-id="64b16-147">When a product that quantity factors are configured for is added to a quote line, the **Quantity** field on the quote line becomes a read-only field.</span></span> <span data-ttu-id="64b16-148">Sau khi bạn nhập giá trị cho các thuộc tính sản phẩm là các yếu tố số lượng, PSA tính số lượng của mô tả báo giá.</span><span class="sxs-lookup"><span data-stu-id="64b16-148">After you enter values for product properties that are quantity factors, PSA computes the quantity of the quote line.</span></span>

<span data-ttu-id="64b16-149">Ví dụ: Dynamics 365 có thể có các thuộc tính sau đây:</span><span class="sxs-lookup"><span data-stu-id="64b16-149">For example, Dynamics 365 might have the following properties:</span></span> 

- <span data-ttu-id="64b16-150">**Không có người dùng** – Số lượng người dùng</span><span class="sxs-lookup"><span data-stu-id="64b16-150">**No of users** - The number of users</span></span> 
- <span data-ttu-id="64b16-151">**Không có tháng** – Số lượng tháng đăng ký</span><span class="sxs-lookup"><span data-stu-id="64b16-151">**No of Months** - The number of subscription months</span></span>
- <span data-ttu-id="64b16-152">**SKU sản phẩm**</span><span class="sxs-lookup"><span data-stu-id="64b16-152">**Product SKU**</span></span> 

<span data-ttu-id="64b16-153">Các thuộc tính **Không có người dùng** và **Không có tháng** có thể được gắn cờ ở dạng yếu tố số lượng bằng cách chỉnh sửa các thuộc tính của mô tả sản phẩm.</span><span class="sxs-lookup"><span data-stu-id="64b16-153">Tne **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span> 

> ![Gắn cờ Không có người dùng và Không có tháng ở dạng các yếu tố chất lượng](media/basic-guide-11.png)
 
