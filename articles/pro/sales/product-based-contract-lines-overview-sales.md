---
title: Tổng quan về mô tả hợp đồng dựa trên sản phẩm - bản đơn giản
description: Chủ đề này cung cấp thông tin về mô tả hợp đồng dựa trên sản phẩm.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6e9ef33cc9c79f828e85733f4f5a199bce842700
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272684"
---
# <a name="product-based-contract-lines-overview---lite"></a><span data-ttu-id="34e73-103">Tổng quan về mô tả hợp đồng dựa trên sản phẩm - bản đơn giản</span><span class="sxs-lookup"><span data-stu-id="34e73-103">Product-based contract lines overview - lite</span></span>

<span data-ttu-id="34e73-104">_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="34e73-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="34e73-105">Bạn có thể tạo mô tả báo giá dựa trên sản phẩm trong Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="34e73-105">You can create product-based contract lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="34e73-106">Mô tả hợp đồng dựa trên sản phẩm có thể là mô tả được tạo thủ công hoặc các mục từ danh mục sản phẩm.</span><span class="sxs-lookup"><span data-stu-id="34e73-106">Product-based contract lines can be manually created lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="34e73-107">Danh mục sản phẩm</span><span class="sxs-lookup"><span data-stu-id="34e73-107">Product catalog</span></span>

<span data-ttu-id="34e73-108">Các sản phẩm trong danh mục sản phẩm có đơn vị mặc định và nhóm đơn vị đo.</span><span class="sxs-lookup"><span data-stu-id="34e73-108">The products in the product catalog have a default unit and unit group.</span></span> <span data-ttu-id="34e73-109">Nếu một số sản phẩm có cùng nhóm thuộc tính, bạn có thể tạo dòng sản phẩm cũng có các thuộc tính đó.</span><span class="sxs-lookup"><span data-stu-id="34e73-109">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="34e73-110">Tất cả sản phẩm trong một dòng sản phẩm thừa kế cùng bộ thuộc tính.</span><span class="sxs-lookup"><span data-stu-id="34e73-110">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="34e73-111">Ví dụ: công ty bán các giấy phép gói đăng ký cho các loại phần mềm khác nhau.</span><span class="sxs-lookup"><span data-stu-id="34e73-111">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="34e73-112">Tất cả phần mềm gói đăng ký có 2 thuộc tính sau:</span><span class="sxs-lookup"><span data-stu-id="34e73-112">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="34e73-113">Số người dùng</span><span class="sxs-lookup"><span data-stu-id="34e73-113">Number of users</span></span>
- <span data-ttu-id="34e73-114">Thời gian đăng ký (trong tháng)</span><span class="sxs-lookup"><span data-stu-id="34e73-114">Subscription duration (in months)</span></span>

<span data-ttu-id="34e73-115">Để duy trì loại danh mục này, hãy tạo một dòng sản phẩm có tên **Phần mềm đăng ký**.</span><span class="sxs-lookup"><span data-stu-id="34e73-115">To maintain this type of catalog, create a product family that is named **Subscription Software**.</span></span> <span data-ttu-id="34e73-116">Thêm các thuộc tính, **Số lượng người dùng** và **Thời hạn đăng ký** cho dòng sản phẩm.</span><span class="sxs-lookup"><span data-stu-id="34e73-116">Add the attributes, **Number of users** and **Subscription duration** to the product family.</span></span> <span data-ttu-id="34e73-117">Sau đó, thêm các sản phẩm riêng lẻ vào dòng sản phẩm **Phần mềm đăng ký**.</span><span class="sxs-lookup"><span data-stu-id="34e73-117">Then, add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-contract"></a><span data-ttu-id="34e73-118">Thêm các mục danh mục sản phẩm vào hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="34e73-118">Add product catalog items to a project Contract</span></span>

<span data-ttu-id="34e73-119">Hợp đồng dự án có các phần cho 2 loại mô tả: mô tả dựa trên dự án và mô tả dựa trên sản phẩm.</span><span class="sxs-lookup"><span data-stu-id="34e73-119">Project contracts have sections for two types of lines, project-based and product-based.</span></span> <span data-ttu-id="34e73-120">Mô tả dựa trên sản phẩm bao gồm tất cả các sản phẩm và đơn vị trong bảng giá sản phẩm trên hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="34e73-120">Product-based lines include all of the products and units in the product price list on the contract.</span></span> <span data-ttu-id="34e73-121">Có thể thêm các sản phẩm không thuộc bảng giá sản phẩm của hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="34e73-121">Products that aren't part of contract's product price list can be added.</span></span>

<span data-ttu-id="34e73-122">Bạn có thể chọn sản phẩm từ các bảng giá khác hoặc trực tiếp từ danh mục sản phẩm.</span><span class="sxs-lookup"><span data-stu-id="34e73-122">You can select products from other price lists, or directly from the product catalog.</span></span> <span data-ttu-id="34e73-123">Khi bạn chọn các sản phẩm trực tiếp từ danh mục sản phẩm, bảng giá mặc định của sản phẩm đó dùng cho giá bán hàng của sản phẩm.</span><span class="sxs-lookup"><span data-stu-id="34e73-123">When you select products directly from a product catalog, the default price list of that product is used for the product's sales price.</span></span> <span data-ttu-id="34e73-124">Nếu một bảng giá mặc định không được đặt, giá sẽ được đặt về 0 (không).</span><span class="sxs-lookup"><span data-stu-id="34e73-124">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="34e73-125">Nếu mô tả hợp đồng dựa trên danh mục sản phẩm, bạn có thể thay thế giá bán hàng trực tiếp trên mô tả.</span><span class="sxs-lookup"><span data-stu-id="34e73-125">If a contract line is based on a product catalog, you can override the sales price directly on the line.</span></span> <span data-ttu-id="34e73-126">Mô tả hợp đồng có trường **Giá** có hai giá trị:</span><span class="sxs-lookup"><span data-stu-id="34e73-126">A contract line has the **Pricing** field with the two values:</span></span>

- <span data-ttu-id="34e73-127">**Thay thế giá**</span><span class="sxs-lookup"><span data-stu-id="34e73-127">**Override pricing**</span></span>
- <span data-ttu-id="34e73-128">**Dùng mặc định**</span><span class="sxs-lookup"><span data-stu-id="34e73-128">**Use default**</span></span>

<span data-ttu-id="34e73-129">Nếu bạn đặt trường **Giá** thành **Ghi đè giá**, giá mặc định không được đặt.</span><span class="sxs-lookup"><span data-stu-id="34e73-129">If you set the **Pricing** field to **Override pricing**, the default price isn't set.</span></span> <span data-ttu-id="34e73-130">Nhập giá cho sản phẩm trên mô tả hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="34e73-130">Enter a price for the product on the contract line.</span></span> <span data-ttu-id="34e73-131">Nếu bạn đặt trường thành **Sử dụng mặc định**, giá bán mặc định được sử dụng và không thể chỉnh sửa trường.</span><span class="sxs-lookup"><span data-stu-id="34e73-131">If you set the field to **Use default**, the default sales price is used and the field can't be edited.</span></span>

<span data-ttu-id="34e73-132">Sau khi bạn cài đặt Project Operations, giá bán hàng mặc định được nhập trên mô tả dựa trên sản phẩm trên hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="34e73-132">After you install Project Operations, default sales prices are entered on the product-based lines on a contract.</span></span> <span data-ttu-id="34e73-133">Sau đó, trường **Giá** được đặt thành **Thay thế giá** để bạn có thể chỉnh sửa giá mặc định trên mô tả hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="34e73-133">The **Pricing** field is set to **Override pricing** so that you can edit the default price on the contract lines.</span></span> <span data-ttu-id="34e73-134">Đây là giá trị ghi đè dành riêng cho Project Operations đối với hành vi mô tả dựa trên sản phẩm trong Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="34e73-134">This is a Project Operations-specific override to product-based lines behavior in Dynamics 365 Sales.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]