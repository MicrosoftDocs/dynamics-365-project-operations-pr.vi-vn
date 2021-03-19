---
title: Nhận các mặt hàng theo đơn đặt hàng từ yêu cầu mặt hàng
description: Chủ đề này giải thích cách nhận các mặt hàng trong đơn đặt hàng từ một yêu cầu về mặt hàng.
author: Yowelle
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c2083516ff929113fd6db377acfe5aeb104666dd
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288254"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="2b685-103">Nhận các mặt hàng theo đơn đặt hàng từ yêu cầu mặt hàng</span><span class="sxs-lookup"><span data-stu-id="2b685-103">Receive items on purchase order from item requirement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2b685-104">Chủ đề này giải thích cách nhận các mặt hàng trong đơn đặt hàng từ một yêu cầu về mặt hàng.</span><span class="sxs-lookup"><span data-stu-id="2b685-104">This topic explains how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="2b685-105">Bằng cách sử dụng yêu cầu mặt hàng thay vì giao dịch mặt hàng, bạn có thể lập kế hoạch giao hàng ngay trước khi mặt hàng đó thực sự được sử dụng, tạo đơn đặt hàng, đưa mặt hàng vào khuôn khổ thỏa thuận thương mại và đưa yêu cầu mặt hàng vào kế hoạch sản xuất.</span><span class="sxs-lookup"><span data-stu-id="2b685-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="2b685-106">Nhiệm vụ này sử dụng tập hợp dữ liệu USSI.</span><span class="sxs-lookup"><span data-stu-id="2b685-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="2b685-107">Ở ngăn điều hướng, chuyển tới **Mô-đun > Quản lý dự án và kế toán > Dự án > Tất cả dự án**.</span><span class="sxs-lookup"><span data-stu-id="2b685-107">In the navigation pane, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="2b685-108">Trong danh sách, chọn liên kết trong hàng mong muốn.</span><span class="sxs-lookup"><span data-stu-id="2b685-108">In the list, select the link in the desired row.</span></span>
3. <span data-ttu-id="2b685-109">Ở ngăn Hành động, chọn **Kế hoạch**.</span><span class="sxs-lookup"><span data-stu-id="2b685-109">On the Action Pane, select **Plan**.</span></span>
4. <span data-ttu-id="2b685-110">Chọn **Yêu cầu mặt hàng**.</span><span class="sxs-lookup"><span data-stu-id="2b685-110">Select **Item requirements**.</span></span>
5. <span data-ttu-id="2b685-111">Chọn **Mới**.</span><span class="sxs-lookup"><span data-stu-id="2b685-111">Select **New**.</span></span>
6. <span data-ttu-id="2b685-112">Trong hàng mới, hãy nhập hoặc chọn một giá trị trong trường **Số mặt hàng**.</span><span class="sxs-lookup"><span data-stu-id="2b685-112">In the new row, enter or select a value in the **Item number** field.</span></span>
7. <span data-ttu-id="2b685-113">Nhập số vào trường **Số lượng**.</span><span class="sxs-lookup"><span data-stu-id="2b685-113">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="2b685-114">Chọn **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="2b685-114">Select **Save**.</span></span>
9. <span data-ttu-id="2b685-115">Ở ngăn Hành động, chọn **Quản lý**.</span><span class="sxs-lookup"><span data-stu-id="2b685-115">On the Action Pane, select **Manage**.</span></span>
10. <span data-ttu-id="2b685-116">Chọn **Chức năng**.</span><span class="sxs-lookup"><span data-stu-id="2b685-116">Select **Functions**.</span></span>
11. <span data-ttu-id="2b685-117">Chọn **Tạo đơn đặt hàng**.</span><span class="sxs-lookup"><span data-stu-id="2b685-117">Select **Create purchase order**.</span></span>
12. <span data-ttu-id="2b685-118">Chọn hộp kiểm **Bao gồm tất cả**.</span><span class="sxs-lookup"><span data-stu-id="2b685-118">Select the **Include all** check box.</span></span>
13. <span data-ttu-id="2b685-119">Trong trường **Tài khoản nhà cung cấp**, nhập hoặc chọn một giá trị.</span><span class="sxs-lookup"><span data-stu-id="2b685-119">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="2b685-120">Chọn **OK**.</span><span class="sxs-lookup"><span data-stu-id="2b685-120">Select **OK**.</span></span>
15. <span data-ttu-id="2b685-121">Ở ngăn điều hướng, chuyển tới **Mô-đun > Tài khoản phải trả > Đơn đặt hàng > Tất cả đơn đặt hàng**.</span><span class="sxs-lookup"><span data-stu-id="2b685-121">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
16. <span data-ttu-id="2b685-122">Trong danh sách, chọn liên kết trong hàng mong muốn.</span><span class="sxs-lookup"><span data-stu-id="2b685-122">In the list, select the link in the desired row.</span></span>
17. <span data-ttu-id="2b685-123">Ở ngăn Hành động, chọn **Mua hàng**.</span><span class="sxs-lookup"><span data-stu-id="2b685-123">On the Action Pane, select **Purchase**.</span></span>
18. <span data-ttu-id="2b685-124">Chọn **Xác nhận**.</span><span class="sxs-lookup"><span data-stu-id="2b685-124">Select **Confirm**.</span></span>
19. <span data-ttu-id="2b685-125">Ở ngăn Hành động, chọn **Nhận**.</span><span class="sxs-lookup"><span data-stu-id="2b685-125">On the Action Pane, select **Receive**.</span></span>
20. <span data-ttu-id="2b685-126">Chọn **Biên lai sản phẩm**.</span><span class="sxs-lookup"><span data-stu-id="2b685-126">Select **Product receipt**.</span></span>
21. <span data-ttu-id="2b685-127">Trong trường **Biên lai sản phẩm**, nhập giá trị.</span><span class="sxs-lookup"><span data-stu-id="2b685-127">In the **Product receipt** field, type a value.</span></span>
22. <span data-ttu-id="2b685-128">Chọn **OK**.</span><span class="sxs-lookup"><span data-stu-id="2b685-128">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]