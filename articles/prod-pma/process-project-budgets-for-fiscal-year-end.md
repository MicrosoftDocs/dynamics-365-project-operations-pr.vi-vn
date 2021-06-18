---
title: Chuyển ngân sách dự án vào cuối năm tài chính
description: Bài viết này cung cấp thông tin về cách chuyển số tiền ngân sách còn lại sang các năm trong tương lai và tạo chi tiết sổ đăng ký ngân sách.
author: Yowelle
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: be3dc039b92e88cac6f6b3b7f72bc32ecf587539
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008067"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a><span data-ttu-id="7892b-103">Chuyển ngân sách dự án vào cuối năm tài chính</span><span class="sxs-lookup"><span data-stu-id="7892b-103">Transfer project budgets at fiscal year end</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7892b-104">Khi thực hiện một dự án kéo dài nhiều năm, bạn có thể còn lại ngân sách vào cuối năm tài chính.</span><span class="sxs-lookup"><span data-stu-id="7892b-104">When working on a multi-year project, you might have remaining budget at the end of the fiscal year.</span></span> <span data-ttu-id="7892b-105">Bạn có thể chuyển số tiền ngân sách còn lại sang một năm trong tương lai và tạo chi tiết sổ đăng ký ngân sách cho số tiền trong các tài khoản sổ cái liên quan.</span><span class="sxs-lookup"><span data-stu-id="7892b-105">You can transfer the remaining budget amounts to a future year, and create budget register details for the amounts in the associated general ledger accounts.</span></span> <span data-ttu-id="7892b-106">Trước khi bạn chuyển tiếp số tiền còn lại, hãy xem xét và phân tích số tiền ngân sách còn lại.</span><span class="sxs-lookup"><span data-stu-id="7892b-106">Before you carry forward the remaining amounts, review and analyze the remaining budget amounts.</span></span>

## <a name="review-and-analyze-remaining-budget-amounts"></a><span data-ttu-id="7892b-107">Xem xét và phân tích số tiền ngân sách còn lại</span><span class="sxs-lookup"><span data-stu-id="7892b-107">Review and analyze remaining budget amounts</span></span>

<span data-ttu-id="7892b-108">Hoàn thành các bước sau để xem xét số tiền ngân sách cuối năm cho các dự án, nhưng không chuyển số tiền này.</span><span class="sxs-lookup"><span data-stu-id="7892b-108">Complete the following steps to review the year-end budget amounts for projects, but not carry the amounts forward.</span></span>

1. <span data-ttu-id="7892b-109">Đi đến **Kế toán và quản lý dự án** > **Định kỳ** > **Ngân sách** > **Chuyển tiếp ngân sách**.</span><span class="sxs-lookup"><span data-stu-id="7892b-109">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="7892b-110">Trên trang **Quy trình chuyển tiếp ngân sách dự án**, trên tab **Tùy chọn cuối năm**, xác minh rằng **Chuyển tiếp số tiền ngân sách dự án còn lại** không được kích hoạt.</span><span class="sxs-lookup"><span data-stu-id="7892b-110">On the **Project budget carry-forward process** page, on the **Year-end options** tab, verify that **Carry forward remaining project budget amounts** is not enabled.</span></span>
3. <span data-ttu-id="7892b-111">Trên tab **Tham số**, trong trường **Năm ngân sách dự án**, hãy chọn năm tài chính mà bạn muốn xem số tiền ngân sách còn lại.</span><span class="sxs-lookup"><span data-stu-id="7892b-111">On the **Parameters** tab, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
4. <span data-ttu-id="7892b-112">Trong trường **Bắt đầu năm tài chính**, hãy chọn năm tài chính mà bạn muốn xem số tiền ngân sách còn lại.</span><span class="sxs-lookup"><span data-stu-id="7892b-112">In the **Opening fiscal year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
5. <span data-ttu-id="7892b-113">Trong trường **Từ mô hình dự báo**, chọn **Ngân sách còn lại**.</span><span class="sxs-lookup"><span data-stu-id="7892b-113">In the **From forecast model** field, select **Remaining budget**.</span></span> 
6. <span data-ttu-id="7892b-114">Để bao gồm các dự án đáp ứng tiêu chí bạn đã chọn và không còn ngân sách, hãy chọn **Hiển thị không còn lại**.</span><span class="sxs-lookup"><span data-stu-id="7892b-114">To include projects that meet your selected criteria and have no remaining budget, select **Show zero remaining**.</span></span>  
7. <span data-ttu-id="7892b-115">Trên tab **Chọn ngân sách**, chọn **Truy xuất tất cả ngân sách** để tải tất cả các ngân sách phù hợp với tiêu chí bạn đã chọn, sau đó chọn **Xử lý**.</span><span class="sxs-lookup"><span data-stu-id="7892b-115">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match your selected criteria, and then select **Process**.</span></span> 
8. <span data-ttu-id="7892b-116">Để thiết kế truy vấn cơ sở dữ liệu tải một tập hợp ngân sách cụ thể vào ngăn, hãy chọn **Truy xuất các ngân sách đã chọn**.</span><span class="sxs-lookup"><span data-stu-id="7892b-116">To design a database query that loads a specific set of budgets into the pane, select **Retrieve selected budgets**.</span></span>

<span data-ttu-id="7892b-117">Để biết thêm thông tin về một dòng cụ thể trong ngăn, hãy chọn dòng, sau đó chọn **Xem chi tiết ngân sách** hoặc **Xem tài khoản**.</span><span class="sxs-lookup"><span data-stu-id="7892b-117">For more information about a specific line in the pane, select the line, and then select **View budget details** or **View accounts**.</span></span>

## <a name="carry-forward-remaining-budget-amounts"></a><span data-ttu-id="7892b-118">Chuyển tiếp số tiền ngân sách còn lại</span><span class="sxs-lookup"><span data-stu-id="7892b-118">Carry forward remaining budget amounts</span></span> 

<span data-ttu-id="7892b-119">Khi xử lý số tiền ngân sách còn lại, bạn có thể tạo các giao dịch trong sổ cái cho số tiền bạn đang chuyển tiếp.</span><span class="sxs-lookup"><span data-stu-id="7892b-119">When you process remaining budget amounts, you can create transactions in the general ledger for the amounts that you are carrying forward.</span></span> <span data-ttu-id="7892b-120">Để tạo các giao dịch sổ cái, hãy hoàn thành các bước trong phần [Chuyển tiếp số tiền ngân sách và tạo các giao dịch sổ cái](#carry-forward).</span><span class="sxs-lookup"><span data-stu-id="7892b-120">To create general ledger transactions, complete the steps in the section, [Carry forward budget amounts and create general ledger transactions](#carry-forward).</span></span> 

> [!NOTE]
> <span data-ttu-id="7892b-121">Số tiền ngân sách chuyển tiếp được chuyển sang mô hình dự báo được chọn trong trang **Các mô hình dự báo** làm mô hình dự báo chuyển tiếp.</span><span class="sxs-lookup"><span data-stu-id="7892b-121">Budget amounts that are carried forward are transferred to the forecast model that is selected in the **Forecast models** page as the carry-forward forecast model.</span></span>  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a><span data-ttu-id="7892b-122">Chuyển tiếp số tiền ngân sách và tạo các giao dịch sổ cái</span><span class="sxs-lookup"><span data-stu-id="7892b-122">Carry forward budget amounts and create general ledger transactions</span></span>

1.  <span data-ttu-id="7892b-123">Chọn **Kế toán và quản lý dự án** > **Định kỳ** > **Ngân sách** > **Chuyển tiếp ngân sách**.</span><span class="sxs-lookup"><span data-stu-id="7892b-123">Select **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="7892b-124">Trên trang **Quy trình chuyển tiếp ngân sách dự án**, chọn **Cuối năm**, sau đó bật **Chuyển tiếp số tiền ngân sách dự án còn lại** và **Tạo mục đăng ký ngân sách trong sổ cái**.</span><span class="sxs-lookup"><span data-stu-id="7892b-124">On the **Project budget carry-forward process** page, select **Year-end**, and then enable **Carry forward remaining project budget amounts** and **Create budget register entries in general ledger**.</span></span> 
3. <span data-ttu-id="7892b-125">Trên tab **Tham số**, trong nhóm trường **Tham số dự án**, chọn các mục sau:</span><span class="sxs-lookup"><span data-stu-id="7892b-125">On the **Parameters** tab, in the **Project parameters** field group, select the following:</span></span>

   - <span data-ttu-id="7892b-126">**Năm ngân sách dự án**: Chọn đầu năm tài chính mà bạn muốn xem số tiền ngân sách còn lại.</span><span class="sxs-lookup"><span data-stu-id="7892b-126">**Project budget year**: Select the beginning of the fiscal year for which you want to view the remaining budget amounts.</span></span> 
   - <span data-ttu-id="7892b-127">**Lãi và lỗ**: Tạo giao dịch lãi và lỗ trong sổ cái.</span><span class="sxs-lookup"><span data-stu-id="7892b-127">**Profit and loss**: Create profit and loss transactions in the general ledger.</span></span> 
   -  <span data-ttu-id="7892b-128">**WIP**: Tạo các giao dịch Đang tiến hành (WIP) trong sổ cái.</span><span class="sxs-lookup"><span data-stu-id="7892b-128">**WIP**: Create Work in Progress (WIP) transactions in the general ledger.</span></span>
   -  <span data-ttu-id="7892b-129">**Bảng lương**: Tạo giao dịch phân bổ bảng lương trong sổ cái.</span><span class="sxs-lookup"><span data-stu-id="7892b-129">**Payroll**: Create payroll allocation transactions in the general ledger.</span></span> 

5. <span data-ttu-id="7892b-130">Trong nhóm trường **Sổ cái**, hãy cung cấp thông tin sau:</span><span class="sxs-lookup"><span data-stu-id="7892b-130">In the **General ledger** field group, provide the following information:</span></span> 

   - <span data-ttu-id="7892b-131">Trong trường **Bắt đầu năm tài chính**, hãy chọn năm tài chính mà bạn muốn chuyển tiếp số tiền ngân sách còn lại cho dự án.</span><span class="sxs-lookup"><span data-stu-id="7892b-131">In the **Opening fiscal year** field, select the fiscal year that you want to transfer remaining budget amounts to for the projects.</span></span> <span data-ttu-id="7892b-132">Giá trị mặc định là một năm sau giá trị trong trường **Năm ngân sách dự án**.</span><span class="sxs-lookup"><span data-stu-id="7892b-132">The default value is one year after the value in the **Project budget year** field.</span></span>
   -  <span data-ttu-id="7892b-133">Trong trường **Kỳ chuyển tiếp**, chọn kỳ mà bạn muốn tạo chi tiết đăng ký nhật ký trong sổ cái.</span><span class="sxs-lookup"><span data-stu-id="7892b-133">In the **Carry-forward period** field, select the period that you want to create the budget register details for in the general ledger.</span></span> <span data-ttu-id="7892b-134">Đây thường là kỳ đầu tiên trong năm tài chính mở.</span><span class="sxs-lookup"><span data-stu-id="7892b-134">This is typically the first period in the opening fiscal year.</span></span>

6. <span data-ttu-id="7892b-135">Trong nhóm trường **Sao chép từ/tới**, hãy cung cấp thông tin sau:</span><span class="sxs-lookup"><span data-stu-id="7892b-135">In the **Copy from/to** field group, provide the following information:</span></span>

   - <span data-ttu-id="7892b-136">Trong trường **Từ mô hình dự báo**, chọn mô hình dự báo ngân sách dự án liên quan đến số tiền ngân sách còn lại mà bạn muốn chuyển cho dự án.</span><span class="sxs-lookup"><span data-stu-id="7892b-136">In the **From forecast model** field, select the project budget forecast model associated with the remaining budget amounts you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="7892b-137">Trong trường **Đến mô hình ngân sách sổ cái**, chọn mô hình ngân sách sổ cái liên quan đến số tiền ngân sách còn lại mà bạn muốn chuyển sang sổ cái.</span><span class="sxs-lookup"><span data-stu-id="7892b-137">In the **To ledger budget model** field, select the ledger budget model associated with the budget amounts you want to transfer to the general ledger.</span></span> 
   -  <span data-ttu-id="7892b-138">Chọn **Chuyển đơn vị tiền tệ bán hàng** để sử dụng đơn vị tiền tệ bán hàng của dự án cho các giao dịch sổ cái được tạo khi bạn chuyển số tiền ngân sách cho dự án.</span><span class="sxs-lookup"><span data-stu-id="7892b-138">Select **Transfer sales currency** to use the project's sales currency for the general ledger transactions that are created when you transfer the budget amounts for the projects.</span></span> <span data-ttu-id="7892b-139">Khi tùy chọn không được chọn, các giao dịch sẽ sử dụng đơn vị tiền tệ kế toán.</span><span class="sxs-lookup"><span data-stu-id="7892b-139">When the option is not selected, the transactions use the accounting currency.</span></span> 
   -  <span data-ttu-id="7892b-140">Chọn **Hiển thị không còn lại** để bao gồm các dự án không còn số tiền ngân sách, nhưng đáp ứng các tiêu chí khác mà bạn chọn trong các dự án được hiển thị ở ngăn dưới cùng.</span><span class="sxs-lookup"><span data-stu-id="7892b-140">Select **Show zero remaining** to include projects that have no remaining budget amounts, but meet the other criteria that you select in the projects displayed in the bottom pane.</span></span>

7. <span data-ttu-id="7892b-141">Trên tab **Chọn ngân sách**, hãy chọn **Truy xuất tất cả ngân sách** để tải tất cả ngân sách phù hợp với tiêu chí bạn đã chọn.</span><span class="sxs-lookup"><span data-stu-id="7892b-141">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match the criteria you selected.</span></span> <span data-ttu-id="7892b-142">Nếu bạn muốn thiết kế truy vấn cơ sở dữ liệu tải một tập hợp ngân sách dự án cụ thể vào ngăn, hãy chọn **Truy xuất các ngân sách đã chọn**.</span><span class="sxs-lookup"><span data-stu-id="7892b-142">If you prefer to design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>
8. <span data-ttu-id="7892b-143">Đối với mỗi dự án mà bạn muốn xử lý, hãy chọn tùy chọn ở đầu dòng cho dự án.</span><span class="sxs-lookup"><span data-stu-id="7892b-143">For each project that you want to process, select the option at the beginning of the line for the project.</span></span>

    > [!TIP]
    > <span data-ttu-id="7892b-144">Để chọn tất cả hoặc hầu hết các dự án, hãy chọn dấu kiểm ở góc trên bên trái.</span><span class="sxs-lookup"><span data-stu-id="7892b-144">To select all or most of the projects, select the check mark in the top upper-left corner.</span></span> <span data-ttu-id="7892b-145">Để loại trừ việc xử lý bất kỳ dự án nào, hãy xóa dấu kiểm cho dự án đó.</span><span class="sxs-lookup"><span data-stu-id="7892b-145">To exclude processing any project, clear the check mark for that project.</span></span>

9. <span data-ttu-id="7892b-146">Để chuyển số tiền ngân sách còn lại cho các dự án đã chọn sang năm tài chính đã chọn và tạo chi tiết đăng ký ngân sách trong sổ cái, hãy chọn **Xử lý**.</span><span class="sxs-lookup"><span data-stu-id="7892b-146">To transfer the remaining budget amounts for the selected projects to the selected fiscal year and create budget register details in the general ledger, select **Process**.</span></span>

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a><span data-ttu-id="7892b-147">Chuyển tiếp số tiền ngân sách mà không tạo các giao dịch sổ cái</span><span class="sxs-lookup"><span data-stu-id="7892b-147">Carry forward budget amounts without creating general ledger transactions</span></span>

1. <span data-ttu-id="7892b-148">Đi đến **Kế toán và quản lý dự án** > **Định kỳ** > **Ngân sách** > **Chuyển tiếp ngân sách**.</span><span class="sxs-lookup"><span data-stu-id="7892b-148">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span>
2. <span data-ttu-id="7892b-149">Trên trang **Quy trình chuyển tiếp ngân sách dự án**, trong trường **Tùy chọn cuối năm**, chọn **Chuyển tiếp số tiền ngân sách dự án còn lại**.</span><span class="sxs-lookup"><span data-stu-id="7892b-149">On the **Project budget carry-forward process** page, in the **Year-end options** field, select **Carry forward remaining project budget amounts**.</span></span>
3. <span data-ttu-id="7892b-150">Trong nhóm **Tham số**, trong trường **Năm ngân sách dự án**, hãy chọn năm tài chính mà bạn muốn xem số tiền ngân sách còn lại.</span><span class="sxs-lookup"><span data-stu-id="7892b-150">In the **Parameters** group, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amounts.</span></span>
4. <span data-ttu-id="7892b-151">Trong nhóm **Sao chép từ/tới**, hãy cung cấp thông tin sau:</span><span class="sxs-lookup"><span data-stu-id="7892b-151">In the **Copy from/to** group, provide the following information:</span></span>

   - <span data-ttu-id="7892b-152">Trong trường **Từ mô hình dự báo**, chọn mô hình dự báo ngân sách dự án liên quan đến số tiền ngân sách còn lại mà bạn muốn chuyển cho dự án.</span><span class="sxs-lookup"><span data-stu-id="7892b-152">In the **From forecast model** field, select the project budget forecast model that is associated with the remaining budget amounts that you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="7892b-153">Chọn **Hiển thị không còn lại** để bao gồm các dự án không còn ngân sách, nhưng đáp ứng các tiêu chí khác mà bạn đã chọn.</span><span class="sxs-lookup"><span data-stu-id="7892b-153">Select **Show zero remaining** to include projects that have no remaining budget amounts, but that meet the other criteria you selected.</span></span>
   - <span data-ttu-id="7892b-154">Trong nhóm **Chọn ngân sách**, hãy chọn **Truy xuất tất cả ngân sách** để tải tất cả ngân sách phù hợp với tiêu chí bạn đã chọn.</span><span class="sxs-lookup"><span data-stu-id="7892b-154">In the **Select Budgets** group, select **Retrieve all budgets** to load all budgets that match the criteria that you selected.</span></span> <span data-ttu-id="7892b-155">Để thiết kế truy vấn cơ sở dữ liệu tải một tập hợp ngân sách dự án cụ thể vào ngăn, hãy chọn **Truy xuất các ngân sách đã chọn**.</span><span class="sxs-lookup"><span data-stu-id="7892b-155">To design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>

5. <span data-ttu-id="7892b-156">Đối với mỗi dự án mà bạn muốn xử lý, hãy chọn tùy chọn ở đầu dòng cho dự án.</span><span class="sxs-lookup"><span data-stu-id="7892b-156">For each project that you want to process, select the option at the beginning of the line for the project.</span></span> 
6. <span data-ttu-id="7892b-157">Chọn **Xử lý** để chuyển số tiền ngân sách còn lại cho các dự án đã chọn sang năm tài chính đã chọn.</span><span class="sxs-lookup"><span data-stu-id="7892b-157">Select **Process** to transfer the remaining budget amounts for the selected projects to the selected fiscal year.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]