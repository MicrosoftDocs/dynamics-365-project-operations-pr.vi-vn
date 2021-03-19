---
title: Tổng quan về các mô tả báo giá dựa trên sản phẩm - bản đơn giản
description: Chủ đề này cung cấp thông tin về cách làm việc với mô tả báo giá dựa trên sản phẩm.
author: rumant
manager: Annbe
ms.date: 10/30/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 29d82637c6c8bb5b5cde7707d181d5b3d3b235c4
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272594"
---
# <a name="product-based-quote-lines-overview---lite"></a><span data-ttu-id="8c727-103">Tổng quan về các mô tả báo giá dựa trên sản phẩm - bản đơn giản</span><span class="sxs-lookup"><span data-stu-id="8c727-103">Product-based quote lines overview - lite</span></span>

<span data-ttu-id="8c727-104">_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="8c727-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8c727-105">Bạn có thể tạo mô tả báo giá dựa trên sản phẩm trong Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="8c727-105">You can create product-based quote lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="8c727-106">Các mô tả báo giá dựa trên sản phẩm có thể thêm được theo cách thủ công hoặc chúng có thể là các mục từ danh mục sản phẩm.</span><span class="sxs-lookup"><span data-stu-id="8c727-106">Product-based quote lines can be manually added, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="8c727-107">Danh mục sản phẩm</span><span class="sxs-lookup"><span data-stu-id="8c727-107">Product catalog</span></span>

<span data-ttu-id="8c727-108">Mỗi sản phẩm trong danh mục sản phẩm đều có đơn vị mặc định và nhóm đơn vị đo.</span><span class="sxs-lookup"><span data-stu-id="8c727-108">Each product in the product catalog has a default unit and unit group.</span></span> <span data-ttu-id="8c727-109">Nếu nhiều sản phẩm có cùng nhóm thuộc tính, bạn có thể tạo dòng sản phẩm cũng có các thuộc tính đó.</span><span class="sxs-lookup"><span data-stu-id="8c727-109">If multiple products share the same set of attributes, you can create a product family that share those attributes.</span></span> 

<span data-ttu-id="8c727-110">Ví dụ: công ty bán các giấy phép gói đăng ký cho các loại phần mềm khác nhau.</span><span class="sxs-lookup"><span data-stu-id="8c727-110">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="8c727-111">Tất cả phần mềm gói đăng ký có 2 thuộc tính sau:</span><span class="sxs-lookup"><span data-stu-id="8c727-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="8c727-112">Số người dùng</span><span class="sxs-lookup"><span data-stu-id="8c727-112">Number of users</span></span>
- <span data-ttu-id="8c727-113">Khoảng thời gian đăng ký được tính theo tháng</span><span class="sxs-lookup"><span data-stu-id="8c727-113">A subscription duration measured in months</span></span>

<span data-ttu-id="8c727-114">Để duy trì loại danh mục này, hãy tạo dòng sản phẩm có tên **Phần mềm đăng ký** và thêm số người dùng cũng như khoảng thời gian đăng ký làm thuộc tính.</span><span class="sxs-lookup"><span data-stu-id="8c727-114">To maintain this type of catalog, create a product family named **Subscription Software** and add the number of users and the subscription duration as attributes.</span></span> <span data-ttu-id="8c727-115">Tiếp theo, bạn có thể thêm từng sản phẩm vào dòng sản phẩm **Phần mềm đăng ký**.</span><span class="sxs-lookup"><span data-stu-id="8c727-115">Next, you can add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="8c727-116">Thêm các mục trong danh mục sản phẩm vào báo giá dự án</span><span class="sxs-lookup"><span data-stu-id="8c727-116">Add product catalog items to a project quote</span></span>

<span data-ttu-id="8c727-117">Các trang **Báo giá dự án** và **Hợp đồng dự án** có các phần cho mô tả dựa trên dự án và mô tả dựa trên sản phẩm.</span><span class="sxs-lookup"><span data-stu-id="8c727-117">The **Project Quote** and **Project Contract** pages have sections for project-based lines and product-based lines.</span></span> <span data-ttu-id="8c727-118">Đối với mô tả dựa trên sản phẩm, danh sách thả xuống trên mô tả báo giá hoặc mô tả hợp đồng dự án bao gồm tất cả sản phẩm và đơn vị trong bảng giá sản phẩm.</span><span class="sxs-lookup"><span data-stu-id="8c727-118">For product-based lines, the drop-down list on the quote line or project contract line includes all the products and units in the product price list.</span></span> <span data-ttu-id="8c727-119">Bạn cũng có thể thêm các sản phẩm không thuộc bảng giá sản phẩm.</span><span class="sxs-lookup"><span data-stu-id="8c727-119">You can also add products that aren't part of the product price list.</span></span>

<span data-ttu-id="8c727-120">Ngoài ra, bạn có thể chọn các sản phẩm từ bảng giá khác hoặc ngay từ danh mục sản phẩm.</span><span class="sxs-lookup"><span data-stu-id="8c727-120">Additionally, you can select products from other price lists or directly from the product catalog.</span></span> <span data-ttu-id="8c727-121">Khi bạn chọn các sản phẩm trực tiếp từ danh mục sản phẩm, bảng giá mặc định của sản phẩm đó dùng để nhận giá bán hàng của sản phẩm.</span><span class="sxs-lookup"><span data-stu-id="8c727-121">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="8c727-122">Nếu một bảng giá mặc định không được đặt, giá sẽ được đặt về không (0).</span><span class="sxs-lookup"><span data-stu-id="8c727-122">If a default price list isn't set, the price is set to zero (0).</span></span>

<span data-ttu-id="8c727-123">Khi mô tả báo giá dựa trên danh mục sản phẩm, bạn có thể thay thế giá bán hàng trực tiếp trên mô tả báo giá.</span><span class="sxs-lookup"><span data-stu-id="8c727-123">When a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="8c727-124">Một mô tả báo giá trong trường **Giá** có sẵn hai giá trị:</span><span class="sxs-lookup"><span data-stu-id="8c727-124">A quote line in **Pricing** field with two available values:</span></span>

- <span data-ttu-id="8c727-125">**Thay thế giá**</span><span class="sxs-lookup"><span data-stu-id="8c727-125">**Override Pricing**</span></span>
- <span data-ttu-id="8c727-126">**Dùng mặc định**</span><span class="sxs-lookup"><span data-stu-id="8c727-126">**Use Default**</span></span>

<span data-ttu-id="8c727-127">Nếu bạn chọn **Thay thế giá**, giá mặc định sẽ không được đặt.</span><span class="sxs-lookup"><span data-stu-id="8c727-127">If you select **Override Pricing**, the default price isn't set.</span></span> <span data-ttu-id="8c727-128">Thay vào đó, bạn phải nhập giá cho sản phẩm trên mô tả báo giá.</span><span class="sxs-lookup"><span data-stu-id="8c727-128">Instead, you must enter a price for the product on the quote line.</span></span> <span data-ttu-id="8c727-129">Nếu bạn chọn **Sử dụng giá mặc định**, giá bán mặc định sẽ được dùng và trường bị khóa không cho chỉnh sửa.</span><span class="sxs-lookup"><span data-stu-id="8c727-129">If you select **Use Default**, the default sales price is used and the field is locked for editing.</span></span>

<span data-ttu-id="8c727-130">Giá bán mặc định được nhập trên mô tả theo sản phẩm trong báo giá.</span><span class="sxs-lookup"><span data-stu-id="8c727-130">Default sales prices are entered on the product-based lines of a quote.</span></span> <span data-ttu-id="8c727-131">Sau đó, trường **Giá** được đặt thành **Thay thế giá** để bạn có thể chỉnh sửa giá mặc định trên mô tả báo giá.</span><span class="sxs-lookup"><span data-stu-id="8c727-131">The **Pricing** field is then set to **Override Pricing** so that you can edit the default price on the quote lines.</span></span> <span data-ttu-id="8c727-132">Đây là một tính năng thay thế dành riêng cho Project Operations đối với các hành vi mô tả dựa trên sản phẩm trong Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="8c727-132">This is a Project Operations-specific override to the product-based lines behavior in Dynamics 365 Sales.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]