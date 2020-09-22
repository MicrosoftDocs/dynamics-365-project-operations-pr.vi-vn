---
title: Đặt cấu hình việc lập hóa đơn dự án liên công ty
description: Chủ đề này trình bày cách thiết lập việc lập hóa đơn dự án giữa hai công ty trong tổ chức của bạn.
author: KimANelson
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.assetid: 72d6c257-f2d3-483b-8ff2-445263796963
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7b199c85736f6268bc5914fddaa10e4cabd44ef1
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 03/24/2020
ms.locfileid: "3757014"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="1c05b-103">Đặt cấu hình việc lập hóa đơn dự án liên công ty</span><span class="sxs-lookup"><span data-stu-id="1c05b-103">Configure intercompany project invoicing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1c05b-104">Chủ đề này trình bày cách thiết lập việc lập hóa đơn dự án giữa hai công ty trong tổ chức của bạn.</span><span class="sxs-lookup"><span data-stu-id="1c05b-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="1c05b-105">Nhiệm vụ này sử dụng tập hợp dữ liệu USSI.</span><span class="sxs-lookup"><span data-stu-id="1c05b-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="1c05b-106">Ở ngăn điều hướng, chuyển tới **Mô-đun > Tài khoản phải trả > Nhà cung cấp > Tất cả nhà cung cấp**.</span><span class="sxs-lookup"><span data-stu-id="1c05b-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="1c05b-107">Trong danh sách **Tất cả nhà cung cấp**, tìm và chọn bản ghi mong muốn.</span><span class="sxs-lookup"><span data-stu-id="1c05b-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="1c05b-108">Ở ngăn Hành động, chọn **Chung**.</span><span class="sxs-lookup"><span data-stu-id="1c05b-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="1c05b-109">Chọn **Liên công ty**.</span><span class="sxs-lookup"><span data-stu-id="1c05b-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="1c05b-110">Đặt **Hiện hoạt** thành **Có** để cho phép giao dịch liên công ty.</span><span class="sxs-lookup"><span data-stu-id="1c05b-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="1c05b-111">Trong trường **Công ty khách hàng**, nhập hoặc chọn một giá trị.</span><span class="sxs-lookup"><span data-stu-id="1c05b-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="1c05b-112">Trong trường **Tài khoản của tôi**, nhập hoặc chọn một giá trị.</span><span class="sxs-lookup"><span data-stu-id="1c05b-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="1c05b-113">Chọn **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="1c05b-113">Select **Save**.</span></span>
9. <span data-ttu-id="1c05b-114">Đóng các trang để quay lại trang chủ.</span><span class="sxs-lookup"><span data-stu-id="1c05b-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="1c05b-115">Ở ngăn điều hướng, chuyển tới **Mô-đun > Quản lý dự án và kế toán > Thiết lập> Tham số quản lý dự án và kế toán**.</span><span class="sxs-lookup"><span data-stu-id="1c05b-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="1c05b-116">Chọn tab **Liên công ty**.</span><span class="sxs-lookup"><span data-stu-id="1c05b-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="1c05b-117">Di chuyển thanh trượt sang **Có** để cho phép lập lịch trình nguồn lực và bảng chấm công liên công ty.</span><span class="sxs-lookup"><span data-stu-id="1c05b-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="1c05b-118">Trong danh sách, đánh dấu hàng được chọn.</span><span class="sxs-lookup"><span data-stu-id="1c05b-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="1c05b-119">Chọn **Mới**.</span><span class="sxs-lookup"><span data-stu-id="1c05b-119">Select **New**.</span></span>
15. <span data-ttu-id="1c05b-120">Trong trường **Pháp nhân vay**, nhập hoặc chọn một giá trị.</span><span class="sxs-lookup"><span data-stu-id="1c05b-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="1c05b-121">Đánh dấu chọn hộp kiểm **Tích lũy doanh thu**.</span><span class="sxs-lookup"><span data-stu-id="1c05b-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="1c05b-122">Trong trường **Danh mục bảng chấm công mặc định**, nhập hoặc chọn một giá trị.</span><span class="sxs-lookup"><span data-stu-id="1c05b-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="1c05b-123">Trong trường **Danh mục chi phí mặc định**, nhập hoặc chọn một giá trị.</span><span class="sxs-lookup"><span data-stu-id="1c05b-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="1c05b-124">Chọn **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="1c05b-124">Select **Save**.</span></span>
20. <span data-ttu-id="1c05b-125">Đóng trang.</span><span class="sxs-lookup"><span data-stu-id="1c05b-125">Close the page.</span></span>
21. <span data-ttu-id="1c05b-126">Ở ngăn điều hướng, chuyển tới **Mô-đun > Quản lý dự án và kế toán > Thiết lập> Đăng > Thiết lập đăng sổ cái**.</span><span class="sxs-lookup"><span data-stu-id="1c05b-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="1c05b-127">Trong trường **Loại tài khoản sổ cái**, chọn một tùy chọn.</span><span class="sxs-lookup"><span data-stu-id="1c05b-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="1c05b-128">Chọn **Mới**.</span><span class="sxs-lookup"><span data-stu-id="1c05b-128">Select **New**.</span></span>
24. <span data-ttu-id="1c05b-129">Trong trường **Tài khoản chính** của hàng mới, chỉ định các giá trị mong muốn.</span><span class="sxs-lookup"><span data-stu-id="1c05b-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="1c05b-130">Chọn **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="1c05b-130">Select **Save**.</span></span>
26. <span data-ttu-id="1c05b-131">Đóng trang.</span><span class="sxs-lookup"><span data-stu-id="1c05b-131">Close the page.</span></span>
27. <span data-ttu-id="1c05b-132">Ở ngăn điều hướng, chuyển tới **Mô-đun > Quản lý dự án và kế toán > Thiết lập> Giá > Giá chuyển nhượng**.</span><span class="sxs-lookup"><span data-stu-id="1c05b-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="1c05b-133">Chọn **Mới**.</span><span class="sxs-lookup"><span data-stu-id="1c05b-133">Select **New**.</span></span>
29. <span data-ttu-id="1c05b-134">Nhập ngày vào trường **Ngày có hiệu lực**.</span><span class="sxs-lookup"><span data-stu-id="1c05b-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="1c05b-135">Trong trường **Pháp nhân vay**, nhập hoặc chọn một giá trị.</span><span class="sxs-lookup"><span data-stu-id="1c05b-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="1c05b-136">Trong trường **Mô hình giá chuyển nhượng**, chọn một tùy chọn.</span><span class="sxs-lookup"><span data-stu-id="1c05b-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="1c05b-137">Nhập số vào trường **Định giá**.</span><span class="sxs-lookup"><span data-stu-id="1c05b-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="1c05b-138">Chọn **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="1c05b-138">Select **Save**.</span></span>

