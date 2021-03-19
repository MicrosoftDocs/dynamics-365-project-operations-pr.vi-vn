---
title: Đơn đặt hàng cho dự án
description: Bài viết này mô tả các phương thức khác nhau mà bạn có thể sử dụng để tạo đơn đặt hàng cho một dự án. Phương thức bạn dùng tùy vào mục đích của đơn đặt hàng và khi mặt hàng đã mua được tiêu dùng và tính phí cho dự án.
author: Yowelle
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5f3f5d196e0d7db4a6d8c4cfe834a335f4ef737c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289215"
---
# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="1a65f-104">Đơn đặt hàng cho dự án</span><span class="sxs-lookup"><span data-stu-id="1a65f-104">Purchase orders for a project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1a65f-105">Bài viết này mô tả các phương thức khác nhau mà bạn có thể sử dụng để tạo đơn đặt hàng cho một dự án.</span><span class="sxs-lookup"><span data-stu-id="1a65f-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="1a65f-106">Phương thức bạn dùng tùy vào mục đích của đơn đặt hàng và khi mặt hàng đã mua được tiêu dùng và tính phí cho dự án.</span><span class="sxs-lookup"><span data-stu-id="1a65f-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="1a65f-107">Phương thức tạo đơn đặt hàng</span><span class="sxs-lookup"><span data-stu-id="1a65f-107">Methods for creating a purchase order</span></span>

<span data-ttu-id="1a65f-108">Bạn có thể sử dụng một trong các phương pháp sau để tạo đơn đặt hàng trong Quản lý dự án và kế toán.</span><span class="sxs-lookup"><span data-stu-id="1a65f-108">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="1a65f-109">Mục đích của đơn đặt hàng sẽ xác định thời điểm cần thực hiện đơn đặt hàng và từ đó xác định khi nào tính phí mặt hàng vào dự án.</span><span class="sxs-lookup"><span data-stu-id="1a65f-109">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1a65f-110">Phương pháp</span><span class="sxs-lookup"><span data-stu-id="1a65f-110">Method</span></span></th>
<th><span data-ttu-id="1a65f-111">Mục đích</span><span class="sxs-lookup"><span data-stu-id="1a65f-111">Purpose</span></span></th>
<th><span data-ttu-id="1a65f-112">Tiêu thụ mặt hàng</span><span class="sxs-lookup"><span data-stu-id="1a65f-112">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1a65f-113">Tạo đơn đặt hàng trực tiếp từ dự án.</span><span class="sxs-lookup"><span data-stu-id="1a65f-113">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="1a65f-114">Sử dụng phương thức này để mua mặt hàng từ nhà cung cấp bên ngoài để tiêu dùng cho một dự án.</span><span class="sxs-lookup"><span data-stu-id="1a65f-114">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="1a65f-115">Bạn có thể tạo đơn đặt hàng theo hai cách:</span><span class="sxs-lookup"><span data-stu-id="1a65f-115">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="1a65f-116">Từ chính dự án.</span><span class="sxs-lookup"><span data-stu-id="1a65f-116">From the project itself.</span></span> <span data-ttu-id="1a65f-117">Trong trường hợp này, dự án đã được xác định cho đơn đặt hàng.</span><span class="sxs-lookup"><span data-stu-id="1a65f-117">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="1a65f-118">Bằng cách điều hướng đến đơn đặt hàng của dự án.</span><span class="sxs-lookup"><span data-stu-id="1a65f-118">By navigating to the project purchase order.</span></span> <span data-ttu-id="1a65f-119">Bạn phải chọn cả nhà cung cấp và dự án để tạo đơn đặt hàng.</span><span class="sxs-lookup"><span data-stu-id="1a65f-119">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="1a65f-120">Mặt hàng được tiêu thụ khi hóa đơn của nhà cung cấp được cập nhật.</span><span class="sxs-lookup"><span data-stu-id="1a65f-120">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a65f-121">Tạo đơn đặt hàng từ đơn bán hàng.</span><span class="sxs-lookup"><span data-stu-id="1a65f-121">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="1a65f-122">Sử dụng phương thức này để mua mặt hàng khi bạn tạo đơn bán hàng từ dự án.</span><span class="sxs-lookup"><span data-stu-id="1a65f-122">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="1a65f-123">Mặt hàng được tiêu thụ khi đơn bán hàng được lập hóa đơn cho khách hàng.</span><span class="sxs-lookup"><span data-stu-id="1a65f-123">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1a65f-124">Tạo đơn đặt hàng từ yêu cầu về mặt hàng.</span><span class="sxs-lookup"><span data-stu-id="1a65f-124">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="1a65f-125">Sử dụng phương thức này để mua mặt hàng khi bạn tạo yêu cầu mặt hàng từ dự án.</span><span class="sxs-lookup"><span data-stu-id="1a65f-125">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="1a65f-126">Mặt hàng được tiêu thụ khi phiếu đóng gói cho yêu cầu về mặt hàng được cập nhật.</span><span class="sxs-lookup"><span data-stu-id="1a65f-126">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="1a65f-127">Khi bạn cập nhật hóa đơn của nhà cung cấp hoặc phiếu đóng gói, bạn sẽ được nhắc cập nhật phiếu đóng gói theo yêu cầu mặt hàng.</span><span class="sxs-lookup"><span data-stu-id="1a65f-127">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="1a65f-128">Để biết thêm thông tin, hãy xem [Nhận các mặt hàng theo đơn đặt hàng từ yêu cầu mặt hàng](tasks/receive-items-purchase-order-item-requirement.md).</span><span class="sxs-lookup"><span data-stu-id="1a65f-128">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]