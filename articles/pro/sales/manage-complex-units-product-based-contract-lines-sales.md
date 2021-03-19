---
title: Quản lý nhiều đơn vị phức tạp cho các mô tả hợp đồng dựa trên sản phẩm - bản đơn giản
description: Chủ đề này cung cấp thông tin về việc hỗ trợ bán các sản phẩm dựa trên đăng ký.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 029d2aa4fd20fc036a34ae6136fe12454f3b7703
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273359"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a><span data-ttu-id="3bf8f-103">Quản lý nhiều đơn vị phức tạp cho các mô tả hợp đồng dựa trên sản phẩm - bản đơn giản</span><span class="sxs-lookup"><span data-stu-id="3bf8f-103">Manage complex units for product-based contract lines - lite</span></span>

<span data-ttu-id="3bf8f-104">_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="3bf8f-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3bf8f-105">Dynamics 365 Project Operations sử dụng các yếu tố số lượng để hỗ trợ bán các sản phẩm dựa trên đăng ký.</span><span class="sxs-lookup"><span data-stu-id="3bf8f-105">Dynamics 365 Project Operations uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="3bf8f-106">Đối với các sản phẩm dựa trên đăng ký, số lượng trên hợp đồng hoặc phần mô tả hợp đồng dự án được thể hiện dưới dạng số tháng làm người dùng.</span><span class="sxs-lookup"><span data-stu-id="3bf8f-106">For subscription-based products, the quantity on the contract or project contract line is expressed as the number of user-months.</span></span>

<span data-ttu-id="3bf8f-107">Giá của phần mềm đăng ký được lưu trữ trong danh mục dưới dạng giá cho mỗi người dùng mỗi tháng.</span><span class="sxs-lookup"><span data-stu-id="3bf8f-107">The price of subscription software is stored in the catalog as the price per-user, per-month.</span></span> <span data-ttu-id="3bf8f-108">Trong quá trình bán hàng, giá trên phần mô tả hợp đồng thường là giá trên mỗi người dùng, mỗi tháng do đại lý bán hàng thương lượng và giảm giá.</span><span class="sxs-lookup"><span data-stu-id="3bf8f-108">During the sales process, the price on the contract line is usually the per-user, per-month price that was negotiated and discounted by the sales agent.</span></span> <span data-ttu-id="3bf8f-109">Mỗi thỏa thuận có một số lượng người dùng khác nhau và số lượng tháng đăng ký khác nhau.</span><span class="sxs-lookup"><span data-stu-id="3bf8f-109">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="3bf8f-110">Số lượng dùng để tính số tiền trong phần mô tả hợp đồng là sản phẩm gồm số lượng người dùng và số lượng tháng đăng ký.</span><span class="sxs-lookup"><span data-stu-id="3bf8f-110">The quantity used to calculate the amount of the contract line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="3bf8f-111">Để hỗ trợ loại bán hàng này, Project Operations hỗ trợ khái niệm *hệ số số lượng*.</span><span class="sxs-lookup"><span data-stu-id="3bf8f-111">To support this type of sale, Project Operations supports the concept of *quantity factors*.</span></span> <span data-ttu-id="3bf8f-112">Yếu tố số lượng dựa vào các thuộc tính sản phẩm.</span><span class="sxs-lookup"><span data-stu-id="3bf8f-112">Quantity factors rely on product attributes.</span></span> <span data-ttu-id="3bf8f-113">Khi bạn đặt cấu hình các thuộc tính cụ thể cho sản phẩm, bạn có thể gắn cờ một tập con của các thuộc tính đó hoặc tất cả thuộc tính ở dạng các yếu tố số lượng.</span><span class="sxs-lookup"><span data-stu-id="3bf8f-113">When you configure specific properties for a product, you can flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="3bf8f-114">Project Operations xác thực rằng chỉ có thuộc tính số hoặc các thuộc tính sản phẩm có loại dữ liệu số được gắn cờ ở dạng yếu tố số lượng.</span><span class="sxs-lookup"><span data-stu-id="3bf8f-114">Project Operations validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="3bf8f-115">Khi một sản phẩm dã đặt cấu hình hệ số số lượng được thêm vào phần mô tả hợp đồng, trường **Số lượng** sẽ trở thành chỉ đọc.</span><span class="sxs-lookup"><span data-stu-id="3bf8f-115">When a product with configured quantity factors is added to a contract line, the **Quantity** field  becomes read-only.</span></span> <span data-ttu-id="3bf8f-116">Sau khi bạn nhập giá trị cho thuộc tính sản phẩm là hệ số số lượng, Project Operations sẽ tính số lượng có trong phần mô tả hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="3bf8f-116">After you enter values for product properties that are quantity factors, Project Operations calculates the quantity of the contract line.</span></span>

<span data-ttu-id="3bf8f-117">Ví dụ: Dynamics 365 Sales có thể có các thuộc tính sau đây:</span><span class="sxs-lookup"><span data-stu-id="3bf8f-117">For example, Dynamics 365 Sales might have the following properties:</span></span>

- <span data-ttu-id="3bf8f-118">**Số người dùng**: Số lượng người dùng.</span><span class="sxs-lookup"><span data-stu-id="3bf8f-118">**No of users**: The number of users.</span></span>
- <span data-ttu-id="3bf8f-119">**Số tháng**: Số lượng tháng đăng ký.</span><span class="sxs-lookup"><span data-stu-id="3bf8f-119">**No of Months**: The number of subscription months.</span></span>
- <span data-ttu-id="3bf8f-120">**SKU sản phẩm**: Đơn vị lưu kho (SKU) của sản phẩm.</span><span class="sxs-lookup"><span data-stu-id="3bf8f-120">**Product SKU**: The stock keeping unit (SKU) for the product.</span></span>

<span data-ttu-id="3bf8f-121">Các thuộc tính **Sô người dùng** và **Số tháng** có thể được gắn cờ ở dạng yếu tố số lượng bằng cách chỉnh sửa các thuộc tính của mô tả sản phẩm.</span><span class="sxs-lookup"><span data-stu-id="3bf8f-121">The **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span>

<span data-ttu-id="3bf8f-122">Để tạo các hệ số số lượng từ thuộc tính của sản phẩm, hãy hoàn thành các bước sau.</span><span class="sxs-lookup"><span data-stu-id="3bf8f-122">To create quantity factors from product properties, complete the following steps.</span></span>

1. <span data-ttu-id="3bf8f-123">Trên **Project Operations**, hãy chọn **Sản phẩm bán hàng**.</span><span class="sxs-lookup"><span data-stu-id="3bf8f-123">On the **Project Operations**, select **Sales-Products**.</span></span>
2. <span data-ttu-id="3bf8f-124">Mở sản phẩm mà bạn cần thiết lập hệ số số lượng.</span><span class="sxs-lookup"><span data-stu-id="3bf8f-124">Open the product for which you need to set up quantity factors.</span></span> <span data-ttu-id="3bf8f-125">Đảm bảo sản phẩm có các thuộc tính đã được thiết lập.</span><span class="sxs-lookup"><span data-stu-id="3bf8f-125">Make sure that the product has properties already set up.</span></span>
3. <span data-ttu-id="3bf8f-126">Trên trang **Thông tin dự án**, hãy chọn tab **Hệ số số lượng**.</span><span class="sxs-lookup"><span data-stu-id="3bf8f-126">On the **Project Information** page, select the **Quantity Factors** tab.</span></span>
4. <span data-ttu-id="3bf8f-127">Trong lưới con, chọn **+ Tính toán trường mới**.</span><span class="sxs-lookup"><span data-stu-id="3bf8f-127">In the subgrid, select **+ New field computation**.</span></span>
5. <span data-ttu-id="3bf8f-128">Nhập tên **Hệ số số lượng** rồi chọn giá trị thuộc tính ánh xạ đến mục tính toán của trường.</span><span class="sxs-lookup"><span data-stu-id="3bf8f-128">Enter the name of the **Quantity Factor** and select the property value that maps to the field computation.</span></span>
6. <span data-ttu-id="3bf8f-129">Lưu và đóng biểu mẫu.</span><span class="sxs-lookup"><span data-stu-id="3bf8f-129">Save and close the form.</span></span>
7. <span data-ttu-id="3bf8f-130">Lặp lại các bước từ 2 đến 6 cho tất cả các thuộc tính sẽ tạo nên số lượng trong phần mô tả hợp đồng dựa trên sản phẩm.</span><span class="sxs-lookup"><span data-stu-id="3bf8f-130">Repeat steps 2-6 for all the properties that together will make up the quantity for the product-based contract line.</span></span>

<span data-ttu-id="3bf8f-131">Nếu hệ số số lượng đã được thiết lập, khi người dùng tạo phần mô tả hợp đồng cho sản phẩm này, số lượng trong phần mô tả hợp đồng sẽ bị khóa.</span><span class="sxs-lookup"><span data-stu-id="3bf8f-131">With quantity factors set up, when the user creates a contract line for this product, the quantity of the contract line is locked.</span></span> <span data-ttu-id="3bf8f-132">Sau đó, số lượng được tính dưới dạng sản phẩm gồm các giá trị thuộc tính cho phần mô tả hợp đồng đó.</span><span class="sxs-lookup"><span data-stu-id="3bf8f-132">The quantity is then calculated as a product of the property values for that contract line.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]