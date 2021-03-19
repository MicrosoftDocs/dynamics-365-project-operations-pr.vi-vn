---
title: Tạo hợp đồng nâng cao để thanh toán dựa trên tiến độ
description: Chủ đề này giải thích cách tạo hợp đồng dự án để bạn có thể tạo hóa đơn cho khách hàng, dựa trên phần trăm công việc đã hoàn thành.
author: RadhikaRS
manager: AnnBe
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: b1de330df8cf85ed30c0ee4e4f2f2fe74d05dbff
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289530"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a><span data-ttu-id="75a69-103">Tạo hợp đồng nâng cao để thanh toán dựa trên tiến độ</span><span class="sxs-lookup"><span data-stu-id="75a69-103">Create advanced contracts for billing based on progress</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="75a69-104">Chủ đề này giải thích cách tạo hợp đồng dự án để bạn có thể tạo hóa đơn cho khách hàng, dựa trên phần trăm công việc đã hoàn thành.</span><span class="sxs-lookup"><span data-stu-id="75a69-104">This topic explains how to create project contracts so that you can create invoices for customers, based on a percentage of completed work.</span></span> <span data-ttu-id="75a69-105">Số tiền trong hóa đơn được tính toán tự động cho các hạng mục ngân sách của công việc mà bạn thiết lập cho một dự án.</span><span class="sxs-lookup"><span data-stu-id="75a69-105">Invoice amounts are automatically calculated for the budget categories of work that you set up for a project.</span></span> <span data-ttu-id="75a69-106">Thời gian lập hóa đơn được đặt khi bạn thương lượng hợp đồng dự án với khách hàng.</span><span class="sxs-lookup"><span data-stu-id="75a69-106">The invoice timing is set when you negotiate the project contract with the customer.</span></span>

<span data-ttu-id="75a69-107">Sử dụng các quy trình trong chủ đề này để thiết lập một hợp đồng, một dự án liên quan và các quy tắc thanh toán để tính toán số tiền trên hóa đơn cho các hạng mục ngân sách của công việc mà bạn thiết lập cho dự án.</span><span class="sxs-lookup"><span data-stu-id="75a69-107">Use the procedures in this topic to set up a contract, an associated project, and the billing rules that calculate invoice amounts for the budget categories of work that you set up for the project.</span></span>

<span data-ttu-id="75a69-108">Sau khi tạo hợp đồng và dự án, bạn có thể thiết lập các chi tiết của dự án.</span><span class="sxs-lookup"><span data-stu-id="75a69-108">After you've created the contract and the project, you can set up the details of the project.</span></span> <span data-ttu-id="75a69-109">Ví dụ: bạn có thể xác định các hoạt động và chỉ định nhân viên cho dự án.</span><span class="sxs-lookup"><span data-stu-id="75a69-109">For example, you can define activities and assign workers to the project.</span></span>

## <a name="example"></a><span data-ttu-id="75a69-110">Ví dụ:</span><span class="sxs-lookup"><span data-stu-id="75a69-110">Example</span></span>

<span data-ttu-id="75a69-111">Tổ chức của bạn là một công ty phát triển phần mềm.</span><span class="sxs-lookup"><span data-stu-id="75a69-111">Your organization is a software development firm.</span></span> <span data-ttu-id="75a69-112">Bạn đồng ý phát triển gói kế toán tính lương cho một khách hàng với tổng phí là 20.000 đô la Mỹ (USD).</span><span class="sxs-lookup"><span data-stu-id="75a69-112">You agree to develop a payroll accounting package for a customer for a total fee of 20,000 US dollars (USD).</span></span> <span data-ttu-id="75a69-113">Tổ chức của bạn đồng ý xuất hóa đơn cho khách hàng khi bạn hoàn thành tỷ lệ phần trăm cụ thể của dự án.</span><span class="sxs-lookup"><span data-stu-id="75a69-113">Your organization agrees to invoice the customer as you complete specific percentages of the project.</span></span> <span data-ttu-id="75a69-114">Bạn thiết lập các danh mục dự án sau cho công việc để có thể sử dụng chúng trong quy trình thanh toán:</span><span class="sxs-lookup"><span data-stu-id="75a69-114">You set up the following project categories for the work, so that you can use them in the billing process:</span></span>

- <span data-ttu-id="75a69-115">Tư vấn</span><span class="sxs-lookup"><span data-stu-id="75a69-115">Consulting</span></span>
- <span data-ttu-id="75a69-116">Thiết kế</span><span class="sxs-lookup"><span data-stu-id="75a69-116">Design</span></span>
- <span data-ttu-id="75a69-117">Cài đặt</span><span class="sxs-lookup"><span data-stu-id="75a69-117">Installation</span></span>

<span data-ttu-id="75a69-118">Bạn cũng thiết lập các quy tắc thanh toán tự động tính toán số tiền trên hóa đơn cho tỷ lệ phần trăm công việc dự án đã hoàn thành trong từng hạng mục.</span><span class="sxs-lookup"><span data-stu-id="75a69-118">You also set up billing rules that automatically calculate the invoice amounts for the percentage of project work that is completed in each category.</span></span>

<span data-ttu-id="75a69-119">Người quản lý ngân sách tạo ngân sách cho các hạng mục dự án.</span><span class="sxs-lookup"><span data-stu-id="75a69-119">The budget manager creates a budget for the project categories.</span></span> <span data-ttu-id="75a69-120">Khối lượng công việc đã hoàn thành tự động được tính theo tỷ lệ phần trăm của công việc thực tế so với số tiền được lập ngân sách.</span><span class="sxs-lookup"><span data-stu-id="75a69-120">The amount of completed work is automatically calculated as a percentage of actual work in comparison to the budgeted amounts.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="75a69-121">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="75a69-121">Prerequisites</span></span>

<span data-ttu-id="75a69-122">Trước khi tạo một dự án sử dụng quy tắc thanh toán, bạn phải thiết lập chuỗi số cho quy tắc thanh toán và nhật ký phí được sử dụng để đăng các hóa đơn tiến độ.</span><span class="sxs-lookup"><span data-stu-id="75a69-122">Before you create a project that uses billing rules, you must set up the number sequences for billing rules and a fee journal that is used to post progress billings.</span></span>

1. <span data-ttu-id="75a69-123">Đi đến **Kế toán và quản lý dự án** \> **Thiết lập** \> **Tham số quản lý dự án và kế toán**.</span><span class="sxs-lookup"><span data-stu-id="75a69-123">Go to **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>
2. <span data-ttu-id="75a69-124">Trên trang **Tham số quản lý dự án và kế toán**, trên tab **Số chuỗi**, hãy thiết lập chuỗi số mà bạn muốn sử dụng khi tạo quy tắc thanh toán.</span><span class="sxs-lookup"><span data-stu-id="75a69-124">On the **Project management and accounting parameters** page, on the **Number sequences** tab, set up the number sequence that you want to use when billing rules are created.</span></span>
3. <span data-ttu-id="75a69-125">Đi đến **Quản lý dự án và kế toán** \> **Nhật ký** \> **Phí**.</span><span class="sxs-lookup"><span data-stu-id="75a69-125">Go to **Project management and accounting** \> **Journals** \> **Fee**.</span></span>
4. <span data-ttu-id="75a69-126">Trên trang **Nhật ký phí**, chọn **Mới** và nhập tên nhật ký.</span><span class="sxs-lookup"><span data-stu-id="75a69-126">On the **Fee journal** page, select **New**, and enter the journal name.</span></span>

## <a name="create-a-contract-for-progress-billings"></a><span data-ttu-id="75a69-127">Tạo hợp đồng để lập hóa đơn tiến độ</span><span class="sxs-lookup"><span data-stu-id="75a69-127">Create a contract for progress billings</span></span>

<span data-ttu-id="75a69-128">Sử dụng quy trình này để tạo hợp đồng dự án cho một dự án theo giá cố định.</span><span class="sxs-lookup"><span data-stu-id="75a69-128">Use this procedure to create a project contract for a fixed-price project.</span></span> <span data-ttu-id="75a69-129">Bạn tạo hóa đơn dự án khi công việc được hoàn thành trên dự án đạt tỷ lệ phần trăm được chỉ định.</span><span class="sxs-lookup"><span data-stu-id="75a69-129">You create a project invoice when the work that is completed on the project reaches a specified percentage.</span></span>

1. <span data-ttu-id="75a69-130">Đi đến **Quản lý dự án và kế toán** \> **Dự án** \> **Hợp đồng dự án**.</span><span class="sxs-lookup"><span data-stu-id="75a69-130">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="75a69-131">Trên trang **Hợp đồng dự án**, chọn **Mới**.</span><span class="sxs-lookup"><span data-stu-id="75a69-131">On the **Project contracts** page, select **New**.</span></span>
3. <span data-ttu-id="75a69-132">Trong hộp thoại **Hợp đồng dự án mới**, hãy cài đặt các trường sau:</span><span class="sxs-lookup"><span data-stu-id="75a69-132">In the **New project contract** dialog box, set the following fields:</span></span>

    - <span data-ttu-id="75a69-133">**Tên**</span><span class="sxs-lookup"><span data-stu-id="75a69-133">**Name**</span></span>
    - <span data-ttu-id="75a69-134">**Loại ràng buộc**</span><span class="sxs-lookup"><span data-stu-id="75a69-134">**Funding type**</span></span>
    - <span data-ttu-id="75a69-135">**Nguồn tiền**</span><span class="sxs-lookup"><span data-stu-id="75a69-135">**Funding source**</span></span>
    - <span data-ttu-id="75a69-136">**Đơn vị tiền tệ bán hàng** – Theo mặc định, đơn vị tiền tệ này được sử dụng cho các hóa đơn của khách hàng có liên quan đến hợp đồng dự án.</span><span class="sxs-lookup"><span data-stu-id="75a69-136">**Sales currency** – By default, this currency is used for customer invoices that are associated with the project contract.</span></span> <span data-ttu-id="75a69-137">Tuy nhiên, bạn có thể thay đổi đơn vị tiền tệ bán hàng trên hóa đơn của một khách hàng cụ thể.</span><span class="sxs-lookup"><span data-stu-id="75a69-137">However, you can change the sales currency on a specific customer invoice.</span></span>

4. <span data-ttu-id="75a69-138">Chọn **OK**.</span><span class="sxs-lookup"><span data-stu-id="75a69-138">Select **OK**.</span></span> <span data-ttu-id="75a69-139">Thông tin được sao chép vào tiêu đề của trang **Hợp đồng dự án**.</span><span class="sxs-lookup"><span data-stu-id="75a69-139">The information is copied to the header of the **Project contracts** page.</span></span>
5. <span data-ttu-id="75a69-140">Trên trang **Hợp đồng dự án**, điền vào phần còn lại của thông tin cần thiết cho dự án.</span><span class="sxs-lookup"><span data-stu-id="75a69-140">On the **Project contracts** page, fill in the rest of the required information for the project.</span></span>

## <a name="create-a-project-for-progress-billings"></a><span data-ttu-id="75a69-141">Tạo dự án để lập hóa đơn tiến độ</span><span class="sxs-lookup"><span data-stu-id="75a69-141">Create a project for progress billings</span></span>

<span data-ttu-id="75a69-142">Làm theo các bước sau để tạo một dự án và bất kỳ dự án con nào được liên kết với hợp đồng dự án.</span><span class="sxs-lookup"><span data-stu-id="75a69-142">Follow these steps to create a project and any subprojects that are associated with a project contract.</span></span>

1. <span data-ttu-id="75a69-143">Chuyển đến **Quản lý dự án và kế toán** \> **Dự án** \> **Tất cả dự án**.</span><span class="sxs-lookup"><span data-stu-id="75a69-143">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="75a69-144">Trên trang **Tất cả dự án**, chọn **Mới**.</span><span class="sxs-lookup"><span data-stu-id="75a69-144">On the **All projects** page, select **New**.</span></span>
3. <span data-ttu-id="75a69-145">Trong hộp thoại **Dự án mới**, trong trường **Loại dự án**, chọn **Thời gian và vật tư**.</span><span class="sxs-lookup"><span data-stu-id="75a69-145">In the **New project** dialog box, in the **Project type** field, select **Time and material**.</span></span>
4. <span data-ttu-id="75a69-146">Chọn nhóm dự án.</span><span class="sxs-lookup"><span data-stu-id="75a69-146">Select a project group.</span></span> <span data-ttu-id="75a69-147">Nhóm dự án xác định thông tin đăng cho các dự án được chỉ định cho nhóm.</span><span class="sxs-lookup"><span data-stu-id="75a69-147">A project group defines the posting information for the projects that are assigned to the group.</span></span>
5. <span data-ttu-id="75a69-148">Chọn **Tạo dự án**.</span><span class="sxs-lookup"><span data-stu-id="75a69-148">Select **Create project**.</span></span>
6. <span data-ttu-id="75a69-149">Sau khi dự án được tạo, hãy đặt giai đoạn dự án thành **Đang diễn ra**.</span><span class="sxs-lookup"><span data-stu-id="75a69-149">After the project is created, set the project stage to **In process**.</span></span>

## <a name="create-a-budget-for-a-project"></a><span data-ttu-id="75a69-150">Tạo ngân sách cho một dự án</span><span class="sxs-lookup"><span data-stu-id="75a69-150">Create a budget for a project</span></span>

<span data-ttu-id="75a69-151">Danh mục ngân sách được sử dụng để tự động tính toán số tiền trên hóa đơn cho tỷ lệ phần trăm công việc đã hoàn thành cho từng hạng mục.</span><span class="sxs-lookup"><span data-stu-id="75a69-151">Budget categories are used to automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="75a69-152">Thực hiện theo các bước sau để tạo danh mục ngân sách cho chi phí ước tính.</span><span class="sxs-lookup"><span data-stu-id="75a69-152">Follow these steps to create budget categories for the estimated costs.</span></span>

1. <span data-ttu-id="75a69-153">Chuyển đến **Quản lý dự án và kế toán** \> **Dự án** \> **Tất cả dự án**.</span><span class="sxs-lookup"><span data-stu-id="75a69-153">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="75a69-154">Trên trang **Tất cả dự án**, chọn và mở dự án mà bạn muốn.</span><span class="sxs-lookup"><span data-stu-id="75a69-154">On the **All projects** page, select and open the project that you want.</span></span>
3. <span data-ttu-id="75a69-155">Trên trang **Dự án**, trên ngăn Hành động, trên tab **Kế hoạch**, trong nhóm **Ngân sách**, chọn **Ngân sách dự án**.</span><span class="sxs-lookup"><span data-stu-id="75a69-155">On the **Projects** page, on the Action Pane, on the **Plan** tab, in the **Budget** group, select **Project budget**.</span></span>
4. <span data-ttu-id="75a69-156">Trên trang **Ngân sách dự án**, nhập chi phí ước tính cho từng hạng mục trong dự án.</span><span class="sxs-lookup"><span data-stu-id="75a69-156">On the **Project budget** page, enter an estimated cost for each category in the project.</span></span>

## <a name="create-billing-rules-for-progress-billings"></a><span data-ttu-id="75a69-157">Tạo quy tắc thanh toán cho các hóa đơn tiến độ</span><span class="sxs-lookup"><span data-stu-id="75a69-157">Create billing rules for progress billings</span></span>

1. <span data-ttu-id="75a69-158">Đi đến **Quản lý dự án và kế toán** \> **Dự án** \> **Hợp đồng dự án**.</span><span class="sxs-lookup"><span data-stu-id="75a69-158">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="75a69-159">Trên trang **Hợp đồng dự án**, hãy chọn và mở hợp đồng dự án.</span><span class="sxs-lookup"><span data-stu-id="75a69-159">On the **Project contracts** page, select and open a project contract.</span></span>
3. <span data-ttu-id="75a69-160">Trên trang hợp đồng dự án, trên FastTab **Quy tắc thanh toán**, chọn **Thêm**.</span><span class="sxs-lookup"><span data-stu-id="75a69-160">On the project contract page, on the **Billing rules** FastTab, select **Add**.</span></span>
4. <span data-ttu-id="75a69-161">Trên trang **Quy tắc thanh toán**, trong trường **Loại mô tả**, chọn **Tiến độ**.</span><span class="sxs-lookup"><span data-stu-id="75a69-161">On the **Billing rule** page, in the **Line type** field, select **Progress**.</span></span>
5. <span data-ttu-id="75a69-162">Trên FastTab **Chi tiết mô tả quy tắc thanh toán**, trong trường **Giá trị hợp đồng**, hãy nhập tổng giá trị của hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="75a69-162">On the **Billing rule line details** FastTab, in the **Contract value** field, enter the total value of the contract.</span></span>
6. <span data-ttu-id="75a69-163">Trong trường **Danh mục**, chọn danh mục để đăng giao dịch phí.</span><span class="sxs-lookup"><span data-stu-id="75a69-163">In the **Category** field, select the category to post the fee transaction to.</span></span>
7. <span data-ttu-id="75a69-164">Trong trường **Dự án**, hãy chọn dự án sử dụng quy tắc thanh toán này.</span><span class="sxs-lookup"><span data-stu-id="75a69-164">In the **Project** field, select the project that uses this billing rule.</span></span>
8. <span data-ttu-id="75a69-165">Tùy chọn: Chỉ định quy tắc thanh toán cho các dự án bổ sung.</span><span class="sxs-lookup"><span data-stu-id="75a69-165">Optional: Assign the billing rule to additional projects.</span></span> <span data-ttu-id="75a69-166">Trên FastTab **Dự án**, trong phần **Dự án có sẵn**, chọn một dự án, sau đó chọn nút mũi tên phải để thêm dự án vào phần **Dự án đã chọn**.</span><span class="sxs-lookup"><span data-stu-id="75a69-166">On the **Project** FastTab, in the **Available projects** section, select a project, and then select the right arrow button to add the project to the **Selected projects** section.</span></span>
9. <span data-ttu-id="75a69-167">Tùy chọn: Tính số tiền phần trăm mà khách hàng giữ lại từ các khoản thanh toán trên hóa đơn.</span><span class="sxs-lookup"><span data-stu-id="75a69-167">Optional: Calculate the percentage amount that the customer withholds from payments on an invoice.</span></span> <span data-ttu-id="75a69-168">Trên FastTab **Điều khoản lưu giữ thanh toán**, chọn nguồn tiền, sau đó, trong trường **Tỷ lệ phần trăm lưu giữ**, nhập tỷ lệ phần trăm lưu giữ.</span><span class="sxs-lookup"><span data-stu-id="75a69-168">On the **Payment retention terms** FastTab, select the funding source, and then, in the **Retention percentage** field, enter the retention percentage.</span></span>
10. <span data-ttu-id="75a69-169">Lặp lại các bước này để tạo các quy tắc thanh toán bổ sung cho hợp đồng dự án.</span><span class="sxs-lookup"><span data-stu-id="75a69-169">Repeat these steps to create additional billing rules for the project contract.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]