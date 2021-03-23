---
title: Đặt cấu hình chi phí tiêu chuẩn cho nhân công và chi phí
description: Chủ đề này giải thích cách thiết lập chi phí tiêu chuẩn cho nhân công và chi phí cho dự án.
author: Yowelle
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b16ed50584b2b4535d1c61fe7069708182a4820e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288360"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="4142e-103">Đặt cấu hình chi phí tiêu chuẩn cho nhân công và chi phí</span><span class="sxs-lookup"><span data-stu-id="4142e-103">Configure standard costs for labor and expenses</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4142e-104">Chủ đề này giải thích cách thiết lập chi phí tiêu chuẩn cho nhân công và chi phí cho dự án.</span><span class="sxs-lookup"><span data-stu-id="4142e-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="4142e-105">Nhiệm vụ này sử dụng tập hợp dữ liệu USSI.</span><span class="sxs-lookup"><span data-stu-id="4142e-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="4142e-106">Ở ngăn điều hướng, chuyển tới **Mô-đun > Quản lý dự án và kế toán > Thiết lập> Giá > Giá vốn (giờ)**.</span><span class="sxs-lookup"><span data-stu-id="4142e-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="4142e-107">Chọn **Mới**.</span><span class="sxs-lookup"><span data-stu-id="4142e-107">Select **New**.</span></span>
3. <span data-ttu-id="4142e-108">Nhập ngày vào trường **Ngày có hiệu lực**.</span><span class="sxs-lookup"><span data-stu-id="4142e-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="4142e-109">Nhập số vào trường **Giá vốn**.</span><span class="sxs-lookup"><span data-stu-id="4142e-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="4142e-110">Bạn có thể thiết lập giá vốn tiêu chuẩn cho danh mục dự án hoặc bạn có thể thiết lập giá vốn theo số hiệu nhân viên, số dự án, danh mục, ngày hoặc bất kỳ tổ hợp nào của các yếu tố này.</span><span class="sxs-lookup"><span data-stu-id="4142e-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="4142e-111">Giá vốn được áp dụng là giá vốn có mức độ chi tiết cao nhất.</span><span class="sxs-lookup"><span data-stu-id="4142e-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="4142e-112">Chọn **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="4142e-112">Select **Save**.</span></span>
6. <span data-ttu-id="4142e-113">Ở ngăn điều hướng, chuyển tới **Mô-đun > Quản lý dự án và kế toán > Thiết lập> Giá > Giá bán (giờ)**.</span><span class="sxs-lookup"><span data-stu-id="4142e-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="4142e-114">Chọn **Mới**.</span><span class="sxs-lookup"><span data-stu-id="4142e-114">Select **New**.</span></span>
8. <span data-ttu-id="4142e-115">Nhập ngày vào trường **Ngày có hiệu lực**.</span><span class="sxs-lookup"><span data-stu-id="4142e-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="4142e-116">Chọn một tùy chọn trong trường **Hợp lệ trong**.</span><span class="sxs-lookup"><span data-stu-id="4142e-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="4142e-117">Nhập số vào trường **Định giá**.</span><span class="sxs-lookup"><span data-stu-id="4142e-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="4142e-118">Bạn có thể thiết lập giá bán tiêu chuẩn cho các giao dịch theo giờ hoặc cho một danh mục dự án.</span><span class="sxs-lookup"><span data-stu-id="4142e-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="4142e-119">Bạn cũng có thể thiết lập giá bán theo số hiệu nhân viên, số dự án, danh mục, ngày giao dịch hoặc bất kỳ tổ hợp nào của các yếu tố này.</span><span class="sxs-lookup"><span data-stu-id="4142e-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="4142e-120">Giá bán thực tế được áp dụng khi nhân viên nhập giao dịch vào nhật ký Giờ sẽ là giá bán có mức độ chi tiết cao nhất.</span><span class="sxs-lookup"><span data-stu-id="4142e-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="4142e-121">Chẳng hạn, nếu cả giá bán chung và giá bán riêng theo nhân viên đều được thiết lập, thì giá bán riêng theo nhân viên sẽ được sử dụng.</span><span class="sxs-lookup"><span data-stu-id="4142e-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="4142e-122">Chọn **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="4142e-122">Select **Save**.</span></span>
12. <span data-ttu-id="4142e-123">Đóng trang.</span><span class="sxs-lookup"><span data-stu-id="4142e-123">Close the page.</span></span>
13. <span data-ttu-id="4142e-124">Ở ngăn điều hướng, chuyển tới **Mô-đun > Quản lý dự án và kế toán > Thiết lập> Giá > Giá vốn (chi phí)**.</span><span class="sxs-lookup"><span data-stu-id="4142e-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="4142e-125">Chọn **Mới**.</span><span class="sxs-lookup"><span data-stu-id="4142e-125">Select **New**.</span></span>
15. <span data-ttu-id="4142e-126">Nhập ngày vào trường **Ngày có hiệu lực**.</span><span class="sxs-lookup"><span data-stu-id="4142e-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="4142e-127">Nhập số vào trường **Giá vốn**.</span><span class="sxs-lookup"><span data-stu-id="4142e-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="4142e-128">Bạn có thể điền nhiều trường, nhưng đây là mức tối thiểu cần có để lưu bản ghi.</span><span class="sxs-lookup"><span data-stu-id="4142e-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="4142e-129">Chọn **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="4142e-129">Select **Save**.</span></span>
18. <span data-ttu-id="4142e-130">Ở ngăn điều hướng, chuyển tới **Mô-đun > Quản lý dự án và kế toán > Thiết lập> Giá > Giá bán (chi phí)**.</span><span class="sxs-lookup"><span data-stu-id="4142e-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="4142e-131">Chọn **Mới**.</span><span class="sxs-lookup"><span data-stu-id="4142e-131">Select **New**.</span></span>
20. <span data-ttu-id="4142e-132">Nhập ngày vào trường **Ngày có hiệu lực**.</span><span class="sxs-lookup"><span data-stu-id="4142e-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="4142e-133">Chọn một tùy chọn trong trường **Hợp lệ trong**.</span><span class="sxs-lookup"><span data-stu-id="4142e-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="4142e-134">Nhập số vào trường **Định giá**.</span><span class="sxs-lookup"><span data-stu-id="4142e-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="4142e-135">Giá bán thực tế được áp dụng khi nhân viên nhập giao dịch vào nhật ký chi phí sẽ là giá bán có mức độ chi tiết cao nhất.</span><span class="sxs-lookup"><span data-stu-id="4142e-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="4142e-136">Chẳng hạn, nếu cả giá bán chung và giá bán riêng theo nhân viên đều được thiết lập, thì giá bán riêng theo nhân viên sẽ được sử dụng.</span><span class="sxs-lookup"><span data-stu-id="4142e-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="4142e-137">Chọn **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="4142e-137">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]