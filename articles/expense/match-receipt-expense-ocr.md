---
title: Chụp biên nhận bằng OCR
description: Chủ đề này cung cấp thông tin về quy trình xử lý nhận dạng ký tự quang học (OCR) cho biên lai.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fd0cb0fb094260fa3e82d7a2f200f328a39dd7a1
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 03/04/2021
ms.locfileid: "5499877"
---
# <a name="capture-a-receipt-using-ocr"></a><span data-ttu-id="5fc01-103">Chụp biên nhận bằng OCR</span><span class="sxs-lookup"><span data-stu-id="5fc01-103">Capture a receipt using OCR</span></span>

<span data-ttu-id="5fc01-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="5fc01-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5fc01-105">Quy trình nhập chi phí đã được nâng cao thông qua việc bổ sung quy trình xử lý nhận dạng ký tự quang học (OCR) cho biên lai.</span><span class="sxs-lookup"><span data-stu-id="5fc01-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="5fc01-106">Chức năng này được thiết kế để cải thiện trải nghiệm người dùng khi tạo báo cáo chi phí.</span><span class="sxs-lookup"><span data-stu-id="5fc01-106">This functionality is designed to improve the user experience when creating expense reports.</span></span>

## <a name="key-features"></a><span data-ttu-id="5fc01-107">Tính năng chính</span><span class="sxs-lookup"><span data-stu-id="5fc01-107">Key features</span></span>

- <span data-ttu-id="5fc01-108">Hệ thống trích xuất tên người bán, ngày tháng và tổng số tiền từ biên lai.</span><span class="sxs-lookup"><span data-stu-id="5fc01-108">The system extracts the merchant name, date, and total amount from receipts.</span></span>
- <span data-ttu-id="5fc01-109">Hệ thống sẽ cố gắng so khớp các biên lai chưa đính kèm với các giao dịch chi phí chưa đính kèm.</span><span class="sxs-lookup"><span data-stu-id="5fc01-109">The system will try to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="5fc01-110">Bạn có thể tạo các giao dịch chi phí được nhập theo cách thủ công từ biên lai.</span><span class="sxs-lookup"><span data-stu-id="5fc01-110">You can create manually entered expense transactions from receipts.</span></span>

## <a name="attach-receipts-to-an-expense-report"></a><span data-ttu-id="5fc01-111">Đính kèm biên lai vào báo cáo chi phí</span><span class="sxs-lookup"><span data-stu-id="5fc01-111">Attach receipts to an expense report</span></span>

<span data-ttu-id="5fc01-112">Để tự động đính kèm biên lai bao gồm các giao dịch bằng thẻ tín dụng khi báo cáo chi phí được tạo, hãy hoàn thành các bước sau.</span><span class="sxs-lookup"><span data-stu-id="5fc01-112">To automatically attach receipts that include credit card transactions when an expense report is created, complete the following steps.</span></span>

  1. <span data-ttu-id="5fc01-113">Mở không gian làm việc **Quản lý chi phí**.</span><span class="sxs-lookup"><span data-stu-id="5fc01-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="5fc01-114">Trên tab **Biên lai**, hãy xác minh rằng biên lai chưa đính kèm có tồn tại.</span><span class="sxs-lookup"><span data-stu-id="5fc01-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="5fc01-115">Bạn cũng có thể tải lên biên lai trên tab **Biên lai**.</span><span class="sxs-lookup"><span data-stu-id="5fc01-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="5fc01-116">Trên tab **Biên lai**, hãy xác minh rằng chi phí chưa đính kèm có tồn tại.</span><span class="sxs-lookup"><span data-stu-id="5fc01-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="5fc01-117">Thông thường, người quản lý chi phí nhập các chi phí này từ nhà cung cấp thẻ tín dụng.</span><span class="sxs-lookup"><span data-stu-id="5fc01-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="5fc01-118">Chọn **Báo cáo chi phí mới**.</span><span class="sxs-lookup"><span data-stu-id="5fc01-118">Select **New expense report**.</span></span> <span data-ttu-id="5fc01-119">Lưu ý rằng kể cả bây giờ, bạn cũng có thể kèm theo chi phí và biên lai khi tạo báo cáo chi phí.</span><span class="sxs-lookup"><span data-stu-id="5fc01-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="5fc01-120">Nếu bạn thêm cả chi phí và biên lai, thao tác đối sánh tự động giữa các khoản thu với chi phí sẽ được kích hoạt.</span><span class="sxs-lookup"><span data-stu-id="5fc01-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

## <a name="create-or-match-receipts-to-an-expense-report"></a><span data-ttu-id="5fc01-121">Tạo hoặc so khớp biên lai vào báo cáo chi phí</span><span class="sxs-lookup"><span data-stu-id="5fc01-121">Create or match receipts to an expense report</span></span>
<span data-ttu-id="5fc01-122">Để tạo một khoản chi phí hoặc so khớp một khoản chi phí từ biên lai, hãy hoàn thành các bước sau.</span><span class="sxs-lookup"><span data-stu-id="5fc01-122">To create an expense, or match an expense from a receipt, complete the following steps.</span></span>

  1. <span data-ttu-id="5fc01-123">Trên báo cáo chi phí, trên tab **Biên lai**, hãy đính kèm biên lai bằng cách chọn **Thêm biên lai**.</span><span class="sxs-lookup"><span data-stu-id="5fc01-123">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="5fc01-124">Dưới hình ảnh đã tải lên của biên lai, hãy lưu ý các tùy chọn **Tạo** và **So khớp**.</span><span class="sxs-lookup"><span data-stu-id="5fc01-124">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="5fc01-125">Chọn **Tạo** để tạo một giao dịch chi phí được nhập theo cách thủ công và điền vào các giá trị được trích xuất từ biên lai.</span><span class="sxs-lookup"><span data-stu-id="5fc01-125">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="5fc01-126">Nếu bạn chọn **So khớp**, hệ thống cố gắng khớp một khoản chi phí hiện có với biên lai.</span><span class="sxs-lookup"><span data-stu-id="5fc01-126">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="5fc01-127">Cài đặt</span><span class="sxs-lookup"><span data-stu-id="5fc01-127">Installation</span></span>

<span data-ttu-id="5fc01-128">Để sử dụng các tính năng về chi phí nâng cao này, hãy cài đặt trình bổ sung Dịch vụ quản lý chi phí cho Microsoft Dynamics 365 Finance và bật các tính năng trong phiên bản của bạn.</span><span class="sxs-lookup"><span data-stu-id="5fc01-128">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="5fc01-129">Bạn có thể truy cập vào trình bổ sung từ dự án của mình trong Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="5fc01-129">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="5fc01-130">Đăng nhập vào LCS và mở môi trường mong muốn.</span><span class="sxs-lookup"><span data-stu-id="5fc01-130">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="5fc01-131">Chuyển tới **Chi tiết đầy đủ**.</span><span class="sxs-lookup"><span data-stu-id="5fc01-131">Go to **Full details**.</span></span>
3. <span data-ttu-id="5fc01-132">Chọn **Duy trì =** hoặc cuộn xuống FastTab **Trình bổ sung cho môi trường**.</span><span class="sxs-lookup"><span data-stu-id="5fc01-132">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="5fc01-133">Chọn **Cài đặt trình bổ sung mới**.</span><span class="sxs-lookup"><span data-stu-id="5fc01-133">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="5fc01-134">Chọn **Dịch vụ quản lý chi phí**.</span><span class="sxs-lookup"><span data-stu-id="5fc01-134">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="5fc01-135">Làm theo hướng dẫn cài đặt và đồng ý với các điều khoản và điều kiện.</span><span class="sxs-lookup"><span data-stu-id="5fc01-135">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="5fc01-136">Chọn **Cài đặt**.</span><span class="sxs-lookup"><span data-stu-id="5fc01-136">Select **Install**.</span></span>

<span data-ttu-id="5fc01-137">Trong không gian làm việc **Quản lý tính năng**, hãy bật các tính năng sau:</span><span class="sxs-lookup"><span data-stu-id="5fc01-137">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="5fc01-138">Báo cáo chi phí đã được xây dựng lại</span><span class="sxs-lookup"><span data-stu-id="5fc01-138">Expense reports re-imagined</span></span>
- <span data-ttu-id="5fc01-139">Tự động so khớp và tạo chi phí từ biên lai</span><span class="sxs-lookup"><span data-stu-id="5fc01-139">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="5fc01-140">Khi bạn bật các tính năng này, các tác vụ sau sẽ diễn ra:</span><span class="sxs-lookup"><span data-stu-id="5fc01-140">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="5fc01-141">Không gian làm việc **Quản lý chi phí** hiện có được thay thế bằng không gian làm việc mới.</span><span class="sxs-lookup"><span data-stu-id="5fc01-141">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="5fc01-142">Một mục menu mới để hiển thị trường chi phí được thêm vào.</span><span class="sxs-lookup"><span data-stu-id="5fc01-142">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="5fc01-143">Bạn vẫn có thể mở trang **Báo cáo chi phí** trước bằng cách chuyển tới **Quản lý chi phí> Chi phí của tôi > Báo cáo chi phí**.</span><span class="sxs-lookup"><span data-stu-id="5fc01-143">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="5fc01-144">Quy trình làm việc và mọi mục phê duyệt vẫn đưa bạn đến trang báo cáo chi phí hiện có.</span><span class="sxs-lookup"><span data-stu-id="5fc01-144">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="5fc01-145">Biên lai sẽ được xử lý thông qua Microsoft Azure Cognitive Services và siêu dữ liệu sẽ được trích xuất và thêm vào.</span><span class="sxs-lookup"><span data-stu-id="5fc01-145">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="5fc01-146">Một tùy chọn được thêm vào, cho phép bạn tạo báo cáo chi phí bao gồm các biên lai chưa đính kèm đã được so khớp.</span><span class="sxs-lookup"><span data-stu-id="5fc01-146">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="5fc01-147">Một tùy chọn được thêm vào báo cáo chi phí, cho phép bạn tạo dòng chi phí từ biên lai hoặc thử so khớp biên lai hiện có với dòng chi phí hiện có.</span><span class="sxs-lookup"><span data-stu-id="5fc01-147">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="5fc01-148">Câu hỏi thường gặp</span><span class="sxs-lookup"><span data-stu-id="5fc01-148">Frequently asked questions</span></span>

<span data-ttu-id="5fc01-149">**Microsoft có sử dụng dữ liệu của tôi cho các mô hình của hãng không?**</span><span class="sxs-lookup"><span data-stu-id="5fc01-149">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="5fc01-150">Không, Microsoft đã xây dựng một mô hình máy học chung cho dịch vụ xử lý biên lai của hãng.</span><span class="sxs-lookup"><span data-stu-id="5fc01-150">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="5fc01-151">Mô hình này không dựa vào biên lai mà bạn tải lên.</span><span class="sxs-lookup"><span data-stu-id="5fc01-151">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="5fc01-152">**Tính năng này được cung cấp và xử lý ở đâu?**</span><span class="sxs-lookup"><span data-stu-id="5fc01-152">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="5fc01-153">Hiện tại, có Hoa Kỳ được hỗ trợ.</span><span class="sxs-lookup"><span data-stu-id="5fc01-153">Currently, the United States is supported.</span></span>

<span data-ttu-id="5fc01-154">**Biên lai của tôi sẽ chuyển tới đâu?**</span><span class="sxs-lookup"><span data-stu-id="5fc01-154">**Where do my receipts go?**</span></span>

<span data-ttu-id="5fc01-155">Finance sẽ liên hệ với Cognitive Services để trích xuất dữ liệu trong trường này.</span><span class="sxs-lookup"><span data-stu-id="5fc01-155">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="5fc01-156">Cognitive Services sẽ giữ lại bản sao biên lai của bạn trong tối đa 24 giờ trong khi quy trình xử lý diễn ra.</span><span class="sxs-lookup"><span data-stu-id="5fc01-156">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="5fc01-157">Sau khi quy trình xử lý đã hoàn tất, Cognitive Services sẽ xóa biên lai.</span><span class="sxs-lookup"><span data-stu-id="5fc01-157">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="5fc01-158">Biên lai vẫn được lưu trữ trong Finance.</span><span class="sxs-lookup"><span data-stu-id="5fc01-158">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="5fc01-159">Để biết thêm thông tin, hãy xem [Cho phép tìm hiểu về biên lai bằng chức năng mới của Form Recognizer](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="5fc01-159">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
