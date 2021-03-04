---
title: Chỉnh sửa hàng loạt dữ liệu thực tế được tạo bởi các mục nhập thời gian và chi phí đã phê duyệt
description: Chủ đề này giải thích cách quản trị viên có thể thực hiện chỉnh sửa từng phần hoặc hàng loạt đối với các mục nhập thời gian hoặc chi phí đã phê duyệt trước đó nếu chưa hoàn tất thanh toán.
author: rumant
manager: AnnBe
ms.date: 04/02/2020
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
search.app:
- ProjectOperations
ms.openlocfilehash: 063c4d017f5904f09c3c239bfa432a128872e4d7
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144979"
---
# <a name="bulk-corrections-of-actuals-created-by-approved-time-and-expense-entries"></a><span data-ttu-id="8b1b2-103">Chỉnh sửa hàng loạt dữ liệu thực tế được tạo bởi các mục nhập thời gian và chi phí đã phê duyệt</span><span class="sxs-lookup"><span data-stu-id="8b1b2-103">Bulk corrections of actuals created by approved time and expense entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="8b1b2-104">Đôi khi, một mục nhập thời gian hoặc chi phí có thể bị nhập sai.</span><span class="sxs-lookup"><span data-stu-id="8b1b2-104">Occasionally a time or expense entry may be entered incorrectly.</span></span> <span data-ttu-id="8b1b2-105">Ví dụ: tư vấn viên có thể chọn sai ngày khi tạo mục nhập thời gian hoặc họ có thể đổi chỗ các số khi nhập chi phí.</span><span class="sxs-lookup"><span data-stu-id="8b1b2-105">For example, a consultant might select the wrong date when creating a time entry or they might transpose the numbers when entering an expense.</span></span> <span data-ttu-id="8b1b2-106">Nếu tư vấn viên không thể cập nhật các mục nhập đã gửi, thì quản trị viên có thể trực tiếp chỉnh sửa mục nhập đó cho dự án.</span><span class="sxs-lookup"><span data-stu-id="8b1b2-106">If a consultant can’t make the updates to the submitted entries, an administrator can directly correct the entry for a project.</span></span>

<span data-ttu-id="8b1b2-107">Để hoàn thành các quy trình trong chủ đề này, bạn sẽ cần các quyền của Quản trị viên.</span><span class="sxs-lookup"><span data-stu-id="8b1b2-107">To complete the procedures in this topic, you will need Administrator permissions.</span></span>

## <a name="correct-approved-time-entries"></a><span data-ttu-id="8b1b2-108">Chỉnh sửa mục nhập thời gian đã phê duyệt</span><span class="sxs-lookup"><span data-stu-id="8b1b2-108">Correct approved time entries</span></span>     

<span data-ttu-id="8b1b2-109">Hoàn thành các bước sau để chỉnh sửa một hoặc nhiều mục nhập thời gian cho dự án.</span><span class="sxs-lookup"><span data-stu-id="8b1b2-109">Complete the following steps to correct single or multiple time entries for a project.</span></span>

1. <span data-ttu-id="8b1b2-110">Trong vùng **Bán hàng**, hãy chọn **Giao dịch**, sau đó chọn **Thời gian Đã phê duyệt**.</span><span class="sxs-lookup"><span data-stu-id="8b1b2-110">In the **Sales** area, select **Transactions**, and then select **Approved Time**.</span></span> 

2. <span data-ttu-id="8b1b2-111">Trong danh sách **Thời gian Đã phê duyệt**, hãy tìm và chọn một hoặc nhiều mục nhập thời gian cần chỉnh sửa.</span><span class="sxs-lookup"><span data-stu-id="8b1b2-111">In the **Approved Time** list, locate and select one or more approved time entries to correct.</span></span> <span data-ttu-id="8b1b2-112">Bạn có thể sử dụng bộ lọc để tìm các mục nhập liên quan.</span><span class="sxs-lookup"><span data-stu-id="8b1b2-112">You can use the filter to locate related entries.</span></span> <span data-ttu-id="8b1b2-113">Ví dụ: bạn có thể lọc trên ID Dự án và chọn tất cả các mục nhập thời gian đã phê duyệt với ID Dự án đó.</span><span class="sxs-lookup"><span data-stu-id="8b1b2-113">For example, you might filter on a Project ID, and select all approved time entries with that Project ID.</span></span>

3. <span data-ttu-id="8b1b2-114">Chọn **Sửa chữa các mục nhập**.</span><span class="sxs-lookup"><span data-stu-id="8b1b2-114">Select **Correct entries**.</span></span> <span data-ttu-id="8b1b2-115">Hệ thống tự động tạo một nhật ký chỉnh sửa mới, với loại được gán là **Sửa chữa thời gian**.</span><span class="sxs-lookup"><span data-stu-id="8b1b2-115">A new correction journal is automatically created, with the assigned type **Time correction**.</span></span> <span data-ttu-id="8b1b2-116">Các mục nhập bạn đã chọn được thêm vào nhật ký.</span><span class="sxs-lookup"><span data-stu-id="8b1b2-116">The entries you selected are added to the journal.</span></span> 

4. <span data-ttu-id="8b1b2-117">Trên trang **Nhật ký Mới**, hãy nhập **Mô tả** cho nhật ký chỉnh sửa của bạn rồi chọn tab **Sửa chữa Mục nhập Thời gian**.</span><span class="sxs-lookup"><span data-stu-id="8b1b2-117">On the **New Journal** page, enter a **Description** for your correction journal, and then select the **Time Entry Corrections** tab.</span></span>  
5. <span data-ttu-id="8b1b2-118">Trong phần **Các giá trị mới cho Mục nhập Thời gian**, hãy cập nhật các trường với thông tin chính xác nếu cần.</span><span class="sxs-lookup"><span data-stu-id="8b1b2-118">In the **New Values for Time Entries** section, update the fields with the correct information as necessary.</span></span> <span data-ttu-id="8b1b2-119">Ví dụ: bạn có thể thay đổi dự án đã gán hoặc nguồn lực có thể đăng ký.</span><span class="sxs-lookup"><span data-stu-id="8b1b2-119">For example, you can change the assigned project or the bookable resource.</span></span>

6. <span data-ttu-id="8b1b2-120">Chọn **Xem trước**.</span><span class="sxs-lookup"><span data-stu-id="8b1b2-120">Select **Preview**.</span></span> <span data-ttu-id="8b1b2-121">Trong hộp thoại, hãy chọn **OK**.</span><span class="sxs-lookup"><span data-stu-id="8b1b2-121">In the dialog box, select **OK**.</span></span> <span data-ttu-id="8b1b2-122">Trên tab **Dòng nhật ký kế toán**, bạn có thể xem danh sách dữ liệu thực tế ban đầu có liên quan đến các mục nhập thời gian bạn chọn đã bị hủy bỏ và các dòng tương ứng đã chỉnh sửa được tạo.</span><span class="sxs-lookup"><span data-stu-id="8b1b2-122">On the **Journal lines** tab, you can view a list of the original actuals that are related to the selected time entries that have been reversed and the corrected corresponding lines that have been created.</span></span> <span data-ttu-id="8b1b2-123">Nếu cần chỉnh sửa thêm, hãy lặp lại bước 5 và 6.</span><span class="sxs-lookup"><span data-stu-id="8b1b2-123">If additional corrections need to be made, repeat steps 5 and 6.</span></span> 

> [!NOTE]
> <span data-ttu-id="8b1b2-124">Tất cả dữ liệu thực tế đã chỉnh sửa sẽ có cùng giá trị với giá trị mà bạn đã chọn trong phần **Các giá trị mới cho Mục nhập Thời gian**.</span><span class="sxs-lookup"><span data-stu-id="8b1b2-124">All the corrected actuals will have the same values that you selected in the **New values for Time Entries** section.</span></span>

7. <span data-ttu-id="8b1b2-125">Nếu các giá trị chỉnh sửa xuất hiện như mong đợi, hãy chọn **Xác nhận**.</span><span class="sxs-lookup"><span data-stu-id="8b1b2-125">If the corrections appear as expected, select **Confirm**.</span></span> <span data-ttu-id="8b1b2-126">Trong hộp thoại, hãy chọn **OK**.</span><span class="sxs-lookup"><span data-stu-id="8b1b2-126">In the dialog box, select **OK**.</span></span>

8. <span data-ttu-id="8b1b2-127">Quay lại vùng **Bán hàng**, chọn **Dự án** rồi mở dự án mà bạn vừa cập nhật các mục nhập thời gian.</span><span class="sxs-lookup"><span data-stu-id="8b1b2-127">Return to the **Sales** area, select **Projects**, and then open the project for which you just updated the time entries.</span></span> 

9. <span data-ttu-id="8b1b2-128">Trên trang **Dự án**, trên tab **Dữ liệu thực tế**, hãy xem các thay đổi mà bạn đã thực hiện.</span><span class="sxs-lookup"><span data-stu-id="8b1b2-128">On the **Projects** page, on the **Actuals** tab, view the changes that you made.</span></span> 

> [!NOTE]
> <span data-ttu-id="8b1b2-129">Nếu tab **Dữ liệu thực tế** không hiển thị, hãy chọn **Có liên quan** > **Dữ liệu thực tế**.</span><span class="sxs-lookup"><span data-stu-id="8b1b2-129">If the **Actuals** tab is not visible, select **Related** > **Actuals**.</span></span>  

10. <span data-ttu-id="8b1b2-130">Trong danh sách **Dạng xem Liên kết Thực tế**, bạn có thể thấy rằng các mục nhập thời gian ban đầu đã hủy bỏ vẫn có trong danh sách, cũng như các mục nhập thời gian tương ứng đã chỉnh sửa.</span><span class="sxs-lookup"><span data-stu-id="8b1b2-130">In the **Actual Associated View** list, you can see that the original time entries that have been reversed are still listed, as are the corresponding corrected time entries.</span></span> 

<span data-ttu-id="8b1b2-131">Ví dụ: trong hình ảnh sau, có hai mục hàng với số lượng 8 có khoản ghi nợ được liệt kê trong cột Số tiền.</span><span class="sxs-lookup"><span data-stu-id="8b1b2-131">For example, in the following graphic, there are two line items with a quantity of 8.00 that have debits listed in the Amount column.</span></span> <span data-ttu-id="8b1b2-132">Ngoài ra, có hai mục hàng với số lượng -8 hiển thị số tiền đã ghi có trong cột Số tiền.</span><span class="sxs-lookup"><span data-stu-id="8b1b2-132">Additionally, there are two line items with a quantity of -8.00 that show credited amounts in the Amount column.</span></span> <span data-ttu-id="8b1b2-133">Những giá trị chỉnh sửa này đã đưa số lượng về 0.</span><span class="sxs-lookup"><span data-stu-id="8b1b2-133">These corrections bring the quantity to zero.</span></span>

![Danh sách dạng xem liên kết thực tế](https://github.com/MicrosoftDocs/dynamics-365-customer-engagement-pr/blob/bulk-corrections-actuals-created-by-approved-time-expense-entries.md/time-actuals.png)
 
## <a name="correct-approved-expense-entries"></a><span data-ttu-id="8b1b2-135">Chỉnh sửa mục nhập chi phí đã phê duyệt</span><span class="sxs-lookup"><span data-stu-id="8b1b2-135">Correct approved expense entries</span></span>

<span data-ttu-id="8b1b2-136">Hoàn thành các bước sau để chỉnh sửa một hoặc nhiều mục nhập chi phí.</span><span class="sxs-lookup"><span data-stu-id="8b1b2-136">Complete the following steps to correct one or more expense entries.</span></span> 

1. <span data-ttu-id="8b1b2-137">Trong vùng **Bán hàng**, trong ngăn điều hướng bên trái, trong phần **Giao dịch**, hãy chọn **Chi phí Đã phê duyệt**.</span><span class="sxs-lookup"><span data-stu-id="8b1b2-137">In the **Sales** area, in the left navigation pane, under **Transactions**, select **Approved Expenses**.</span></span>

2. <span data-ttu-id="8b1b2-138">Trong danh sách **Chi phí Đã phê duyệt**, hãy chọn dự án bạn muốn chỉnh sửa rồi chọn **Sửa chữa các mục nhập**.</span><span class="sxs-lookup"><span data-stu-id="8b1b2-138">In the **Approved Expenses** list, select the project that you want to correct, and then select **Correct entries**.</span></span> <span data-ttu-id="8b1b2-139">Hệ thống tự động tạo một nhật ký chỉnh sửa mới, với loại được gán là **Sửa chữa chi phí**.</span><span class="sxs-lookup"><span data-stu-id="8b1b2-139">A new correction journal will be created automatically with the assigned type of **Expense correction**.</span></span> 

3. <span data-ttu-id="8b1b2-140">Trên trang **Nhật ký Mới**, hãy nhập **Mô tả** cho thao tác điều chỉnh, và trên tab **Sửa chữa Chi phí**, trong phần **Các giá trị mới cho Chi phí**, hãy chọn các trường dữ liệu mà bạn muốn chỉnh sửa cho các dòng chi phí đã chọn.</span><span class="sxs-lookup"><span data-stu-id="8b1b2-140">On the **New Journal** page, enter a **Description** for the correction, and on the **Expense Correction** tab, in the **New Values for Expenses** section, select the data fields that you want to correct for the selected expense lines.</span></span> <span data-ttu-id="8b1b2-141">Ví dụ: bạn có thể gán chi phí cho một **Dự án** khác hoặc chỉnh sửa **Loại Chi phí**, **Ngày phát sinh Chi phí** hoặc **Nguồn lực Có thể đăng ký**.</span><span class="sxs-lookup"><span data-stu-id="8b1b2-141">For example, you can assign the expense to another **Project**, or correct the **Expense Category**, **Expense Date**, or **Bookable Resource**.</span></span>

4. <span data-ttu-id="8b1b2-142">Chọn **Xem trước**.</span><span class="sxs-lookup"><span data-stu-id="8b1b2-142">Select **Preview**.</span></span> <span data-ttu-id="8b1b2-143">Trong hộp thoại, hãy chọn **OK**.</span><span class="sxs-lookup"><span data-stu-id="8b1b2-143">In the dialog box, select **OK**.</span></span> 

5. <span data-ttu-id="8b1b2-144">Xác minh các giá trị chỉnh sửa trên tab **Dòng nhật ký kế toán**. Bạn có thể xem danh sách dữ liệu thực tế ban đầu có liên quan đến các mục nhập chi phí bạn chọn đã bị hủy bỏ và các dòng tương ứng đã chỉnh sửa được tạo.</span><span class="sxs-lookup"><span data-stu-id="8b1b2-144">Verify the corrections on the **Journal lines** tab. You can view a list of the original actuals that are related to the selected expense entries that have been reversed and the corrected corresponding lines that have been created.</span></span>

6. <span data-ttu-id="8b1b2-145">Nếu các giá trị chỉnh sửa xuất hiện như mong đợi, hãy chọn **Xác nhận**.</span><span class="sxs-lookup"><span data-stu-id="8b1b2-145">If the corrected values are as expected, select **Confirm**.</span></span> <span data-ttu-id="8b1b2-146">Trong hộp thoại, hãy chọn **OK.**</span><span class="sxs-lookup"><span data-stu-id="8b1b2-146">In the dialog box, select **OK.**</span></span> <span data-ttu-id="8b1b2-147">Nếu các giá trị không hiển thị như mong đợi, hãy chọn **Hủy** để quay lại danh sách **Chi phí Đã phê duyệt**.</span><span class="sxs-lookup"><span data-stu-id="8b1b2-147">If the values are not showing as expected, select **Cancel** to return to the **Approved Expenses** list.</span></span> <span data-ttu-id="8b1b2-148">Lặp lại các bước từ 2 đến 5.</span><span class="sxs-lookup"><span data-stu-id="8b1b2-148">Repeat steps 2 through 5.</span></span> 

> [!NOTE]
> <span data-ttu-id="8b1b2-149">Dữ liệu thực tế đã chỉnh sửa sẽ có cùng giá trị với giá trị mà bạn đã chọn trong phần **Các giá trị mới cho Chi phí**.</span><span class="sxs-lookup"><span data-stu-id="8b1b2-149">The corrected actuals will have the same values that you selected in the **New values for Expenses** section.</span></span>

7. <span data-ttu-id="8b1b2-150">Sau khi bạn xác nhận nhật ký chỉnh sửa, hãy quay lại dự án hoặc các dự án mà bạn đã cập nhật để xem các thay đổi mà bạn đã thực hiện.</span><span class="sxs-lookup"><span data-stu-id="8b1b2-150">After you confirm the correction journal, navigate back to the project or projects that you updated, to view your changes.</span></span>  

8. <span data-ttu-id="8b1b2-151">Trong trang dự án, trên tab **Dữ liệu thực tế**, hãy xem lại **Dạng xem Liên kết Thực tế**.</span><span class="sxs-lookup"><span data-stu-id="8b1b2-151">In the project page, on the **Actuals** tab, review the **Actual Associated View**.</span></span> <span data-ttu-id="8b1b2-152">Các mục nhập ban đầu và mục nhập đã chỉnh sửa đều được liệt kê.</span><span class="sxs-lookup"><span data-stu-id="8b1b2-152">The original entries and the corrected entries are listed.</span></span> <span data-ttu-id="8b1b2-153">Hình ảnh sau đây cho thấy số tiền trong mục nhập chi phí ban đầu và số tiền trong mục nhập chi phí tương ứng đã điều chỉnh.</span><span class="sxs-lookup"><span data-stu-id="8b1b2-153">The following graphic shows original expense entry amounts and the corresponding corrected expense entry amounts.</span></span> 

![Expense_actuals](https://user-images.githubusercontent.com/60806505/77122219-4cd52900-69fa-11ea-8349-ccd2ffebf640.png)
