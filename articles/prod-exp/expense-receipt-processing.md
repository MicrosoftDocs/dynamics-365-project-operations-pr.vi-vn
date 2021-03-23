---
title: Xử lý biên lai chi phí
description: Chủ đề này cung cấp thông tin về quy trình xử lý nhận dạng ký tự quang học (OCR) cho biên lai. Tính năng này được thiết kế để cải thiện trải nghiệm người dùng khi tạo báo cáo chi phí trong Microsoft Dynamics 365 Finance.
author: stsporen
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 57ef67412eb3c5795559e4f6d011e97c4d7a1338
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271829"
---
# <a name="expense-receipt-processing"></a><span data-ttu-id="8ba60-104">Xử lý biên lai chi phí</span><span class="sxs-lookup"><span data-stu-id="8ba60-104">Expense receipt processing</span></span>

<span data-ttu-id="8ba60-105">Quy trình nhập chi phí đã được nâng cao thông qua việc bổ sung quy trình xử lý nhận dạng ký tự quang học (OCR) cho biên lai.</span><span class="sxs-lookup"><span data-stu-id="8ba60-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="8ba60-106">Tính năng này được thiết kế để cải thiện trải nghiệm người dùng khi tạo báo cáo chi phí.</span><span class="sxs-lookup"><span data-stu-id="8ba60-106">This feature is designed to improve the user experience when expense reports are created.</span></span>

## <a name="key-features"></a><span data-ttu-id="8ba60-107">Tính năng chính</span><span class="sxs-lookup"><span data-stu-id="8ba60-107">Key features</span></span>

- <span data-ttu-id="8ba60-108">Tên người bán, ngày tháng và tổng số tiền được trích xuất từ biên lai.</span><span class="sxs-lookup"><span data-stu-id="8ba60-108">The merchant name, date, and total amount are extracted from receipts.</span></span>
- <span data-ttu-id="8ba60-109">Tính năng này sẽ cố gắng so khớp các biên lai chưa đính kèm với các giao dịch chi phí chưa đính kèm.</span><span class="sxs-lookup"><span data-stu-id="8ba60-109">The feature tries to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="8ba60-110">Người dùng có thể tạo các giao dịch chi phí được nhập thủ công từ biên lai.</span><span class="sxs-lookup"><span data-stu-id="8ba60-110">Users can create manually entered expense transactions from receipts.</span></span>

## <a name="usage-examples"></a><span data-ttu-id="8ba60-111">Ví dụ sử dụng</span><span class="sxs-lookup"><span data-stu-id="8ba60-111">Usage examples</span></span>

<span data-ttu-id="8ba60-112">Để tự động đính kèm biên lai có giao dịch bằng thẻ tín dụng khi báo cáo chi phí được tạo, hãy làm như sau:</span><span class="sxs-lookup"><span data-stu-id="8ba60-112">To automatically attach receipts that include credit card transactions when an expense report is created, do the following:</span></span>

  1. <span data-ttu-id="8ba60-113">Mở không gian làm việc **Quản lý chi phí**.</span><span class="sxs-lookup"><span data-stu-id="8ba60-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="8ba60-114">Trên tab **Biên lai**, hãy xác minh rằng biên lai chưa đính kèm có tồn tại.</span><span class="sxs-lookup"><span data-stu-id="8ba60-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="8ba60-115">Bạn cũng có thể tải lên biên lai trên tab **Biên lai**.</span><span class="sxs-lookup"><span data-stu-id="8ba60-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="8ba60-116">Trên tab **Biên lai**, hãy xác minh rằng chi phí chưa đính kèm có tồn tại.</span><span class="sxs-lookup"><span data-stu-id="8ba60-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="8ba60-117">Thông thường, người quản lý chi phí nhập các chi phí này từ nhà cung cấp thẻ tín dụng.</span><span class="sxs-lookup"><span data-stu-id="8ba60-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="8ba60-118">Chọn **Báo cáo chi phí mới**.</span><span class="sxs-lookup"><span data-stu-id="8ba60-118">Select **New expense report**.</span></span> <span data-ttu-id="8ba60-119">Lưu ý rằng kể cả bây giờ, bạn cũng có thể kèm theo chi phí và biên lai khi tạo báo cáo chi phí.</span><span class="sxs-lookup"><span data-stu-id="8ba60-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="8ba60-120">Nếu bạn thêm cả chi phí và biên lai, thao tác đối sánh tự động giữa các khoản thu với chi phí sẽ được kích hoạt.</span><span class="sxs-lookup"><span data-stu-id="8ba60-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

<span data-ttu-id="8ba60-121">Để tạo chi phí hoặc so khớp chi phí từ biên lai, hãy làm như sau:</span><span class="sxs-lookup"><span data-stu-id="8ba60-121">To create an expense, or match an expense from a receipt, do the following:</span></span>

  1. <span data-ttu-id="8ba60-122">Trên báo cáo chi phí, trên tab **Biên lai**, hãy đính kèm biên lai bằng cách chọn **Thêm biên lai**.</span><span class="sxs-lookup"><span data-stu-id="8ba60-122">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="8ba60-123">Dưới hình ảnh đã tải lên của biên lai, hãy lưu ý các tùy chọn **Tạo** và **So khớp**.</span><span class="sxs-lookup"><span data-stu-id="8ba60-123">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="8ba60-124">Chọn **Tạo** để tạo một giao dịch chi phí được nhập theo cách thủ công và điền vào các giá trị được trích xuất từ biên lai.</span><span class="sxs-lookup"><span data-stu-id="8ba60-124">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="8ba60-125">Nếu bạn chọn **So khớp**, hệ thống cố gắng khớp một khoản chi phí hiện có với biên lai.</span><span class="sxs-lookup"><span data-stu-id="8ba60-125">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="8ba60-126">Cài đặt</span><span class="sxs-lookup"><span data-stu-id="8ba60-126">Installation</span></span>

<span data-ttu-id="8ba60-127">Tính năng này hoạt động kết hợp với tính năng **Báo cáo chi phí được xây dựng lại** để mang đến trải nghiệm chi phí đơn giản hơn.</span><span class="sxs-lookup"><span data-stu-id="8ba60-127">This feature works in combination with the **Expense reports re-imagined** feature to help simplify the expense experience.</span></span> <span data-ttu-id="8ba60-128">Tính năng này chỉ khả dụng cho môi trường Cấp 2 trở lên, tức là Hộp cát và Sản xuất.</span><span class="sxs-lookup"><span data-stu-id="8ba60-128">This feature is only available for Tier 2+ environments, which are Sandbox and Production.</span></span>

<span data-ttu-id="8ba60-129">Để sử dụng các tính năng về chi phí nâng cao này, hãy cài đặt trình bổ sung Dịch vụ quản lý chi phí cho Microsoft Dynamics 365 Finance và bật các tính năng trong phiên bản của bạn.</span><span class="sxs-lookup"><span data-stu-id="8ba60-129">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="8ba60-130">Bạn có thể truy cập vào trình bổ sung từ dự án của mình trong Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="8ba60-130">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="8ba60-131">Đăng nhập vào LCS và mở môi trường mong muốn.</span><span class="sxs-lookup"><span data-stu-id="8ba60-131">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="8ba60-132">Chuyển tới **Chi tiết đầy đủ**.</span><span class="sxs-lookup"><span data-stu-id="8ba60-132">Go to **Full details**.</span></span>
3. <span data-ttu-id="8ba60-133">Chọn **Duy trì =** hoặc cuộn xuống FastTab **Trình bổ sung cho môi trường**.</span><span class="sxs-lookup"><span data-stu-id="8ba60-133">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="8ba60-134">Chọn **Cài đặt trình bổ sung mới**.</span><span class="sxs-lookup"><span data-stu-id="8ba60-134">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="8ba60-135">Chọn **Dịch vụ quản lý chi phí**.</span><span class="sxs-lookup"><span data-stu-id="8ba60-135">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="8ba60-136">Làm theo hướng dẫn cài đặt và đồng ý với các điều khoản và điều kiện.</span><span class="sxs-lookup"><span data-stu-id="8ba60-136">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="8ba60-137">Chọn **Cài đặt**.</span><span class="sxs-lookup"><span data-stu-id="8ba60-137">Select **Install**.</span></span>

<span data-ttu-id="8ba60-138">Trong không gian làm việc **Quản lý tính năng**, hãy bật các tính năng sau:</span><span class="sxs-lookup"><span data-stu-id="8ba60-138">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="8ba60-139">Báo cáo chi phí đã được xây dựng lại</span><span class="sxs-lookup"><span data-stu-id="8ba60-139">Expense reports re-imagined</span></span>
- <span data-ttu-id="8ba60-140">Tự động so khớp và tạo chi phí từ biên lai</span><span class="sxs-lookup"><span data-stu-id="8ba60-140">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="8ba60-141">Khi bạn bật các tính năng này, các tác vụ sau sẽ diễn ra:</span><span class="sxs-lookup"><span data-stu-id="8ba60-141">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="8ba60-142">Không gian làm việc **Quản lý chi phí** hiện có được thay thế bằng không gian làm việc mới.</span><span class="sxs-lookup"><span data-stu-id="8ba60-142">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="8ba60-143">Một mục menu mới để hiển thị trường chi phí được thêm vào.</span><span class="sxs-lookup"><span data-stu-id="8ba60-143">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="8ba60-144">Bạn vẫn có thể mở trang **Báo cáo chi phí** trước bằng cách chuyển tới **Quản lý chi phí> Chi phí của tôi > Báo cáo chi phí**.</span><span class="sxs-lookup"><span data-stu-id="8ba60-144">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="8ba60-145">Quy trình làm việc và mọi mục phê duyệt vẫn đưa bạn đến trang báo cáo chi phí hiện có.</span><span class="sxs-lookup"><span data-stu-id="8ba60-145">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="8ba60-146">Biên lai sẽ được xử lý thông qua Microsoft Azure Cognitive Services và siêu dữ liệu sẽ được trích xuất và thêm vào.</span><span class="sxs-lookup"><span data-stu-id="8ba60-146">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="8ba60-147">Một tùy chọn được thêm vào, cho phép bạn tạo báo cáo chi phí bao gồm các biên lai chưa đính kèm đã được so khớp.</span><span class="sxs-lookup"><span data-stu-id="8ba60-147">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="8ba60-148">Một tùy chọn được thêm vào báo cáo chi phí, cho phép bạn tạo dòng chi phí từ biên lai hoặc thử so khớp biên lai hiện có với dòng chi phí hiện có.</span><span class="sxs-lookup"><span data-stu-id="8ba60-148">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

<span data-ttu-id="8ba60-149">Để biết thêm thông tin về tính năng Báo cáo chi phí được xây dựng lại, hãy xem [Báo cáo chi phí được xây dựng lại](ExpenseWorkspaceNew.md).</span><span class="sxs-lookup"><span data-stu-id="8ba60-149">For more information about the Expense reports re-imagined feature, see [Expense reports reimagined](ExpenseWorkspaceNew.md).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="8ba60-150">Câu hỏi thường gặp</span><span class="sxs-lookup"><span data-stu-id="8ba60-150">Frequently asked questions</span></span>

<span data-ttu-id="8ba60-151">**Microsoft có sử dụng dữ liệu của tôi cho các mô hình của hãng không?**</span><span class="sxs-lookup"><span data-stu-id="8ba60-151">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="8ba60-152">Không, Microsoft đã xây dựng một mô hình máy học chung cho dịch vụ xử lý biên lai của hãng.</span><span class="sxs-lookup"><span data-stu-id="8ba60-152">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="8ba60-153">Mô hình này không dựa vào biên lai mà bạn tải lên.</span><span class="sxs-lookup"><span data-stu-id="8ba60-153">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="8ba60-154">**Tính năng này được cung cấp và xử lý ở đâu?**</span><span class="sxs-lookup"><span data-stu-id="8ba60-154">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="8ba60-155">Hiện tại, có Hoa Kỳ được hỗ trợ.</span><span class="sxs-lookup"><span data-stu-id="8ba60-155">Currently, the United States is supported.</span></span>

<span data-ttu-id="8ba60-156">**Biên lai của tôi sẽ chuyển tới đâu?**</span><span class="sxs-lookup"><span data-stu-id="8ba60-156">**Where do my receipts go?**</span></span>

<span data-ttu-id="8ba60-157">Finance sẽ liên hệ với Cognitive Services để trích xuất dữ liệu trong trường này.</span><span class="sxs-lookup"><span data-stu-id="8ba60-157">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="8ba60-158">Cognitive Services sẽ giữ lại bản sao biên lai của bạn trong tối đa 24 giờ trong khi quy trình xử lý diễn ra.</span><span class="sxs-lookup"><span data-stu-id="8ba60-158">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="8ba60-159">Sau khi quy trình xử lý đã hoàn tất, Cognitive Services sẽ xóa biên lai.</span><span class="sxs-lookup"><span data-stu-id="8ba60-159">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="8ba60-160">Biên lai vẫn được lưu trữ trong Finance.</span><span class="sxs-lookup"><span data-stu-id="8ba60-160">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="8ba60-161">Để biết thêm thông tin, hãy xem [Cho phép tìm hiểu về biên lai bằng chức năng mới của Form Recognizer](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="8ba60-161">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]