---
title: Xem lại tồn đọng về vấn đề lập hóa đơn đối với các dự án và hợp đồng dự án
description: Chủ đề này cung cấp thông tin về cách xem lại các tồn đọng về thời gian, chi phí và sản phẩm, cũng như cách đánh dấu các mục này là sẵn sàng để lập hóa đơn.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: eb6d942d61bf8b5d20afb75c88716132a596bcbd
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087317"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a><span data-ttu-id="6d804-103">Xem lại tồn đọng về vấn đề lập hóa đơn đối với các dự án và hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="6d804-103">Review the invoicing backlog on projects and project contracts</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="6d804-104">Khi một giao dịch sẵn sàng tạo và xử lý hóa đơn, thì giao dịch đó sẽ được đánh dấu là **Sẵn sàng lập hóa đơn**.</span><span class="sxs-lookup"><span data-stu-id="6d804-104">When a transaction is ready to have an invoice created and processed, the transaction should be marked **Ready to invoice**.</span></span> <span data-ttu-id="6d804-105">Chủ đề này mô tả các loại giao dịch có thể được tạo.</span><span class="sxs-lookup"><span data-stu-id="6d804-105">This topic describes the types of transactions that can be created.</span></span>

## <a name="review-the-time-and-material-billing-backlog"></a><span data-ttu-id="6d804-106">Xem lại tồn đọng về lập hóa đơn theo thời gian và tài liệu</span><span class="sxs-lookup"><span data-stu-id="6d804-106">Review the time and material billing backlog</span></span>

<span data-ttu-id="6d804-107">Khi một mục nhập thời gian hoặc chi phí được gửi và phê duyệt cho một dự án, PSA sẽ tạo ra một dự án thực tế.</span><span class="sxs-lookup"><span data-stu-id="6d804-107">When a time or expense entry is submitted and approved for a project, PSA creates a project actual.</span></span> <span data-ttu-id="6d804-108">Nếu tổ hợp dự án và lớp giao dịch phù hợp với một mô tả hợp đồng cho một dự án thời gian-và-tài liệu, thì hai số liệu thực sẽ được tạo ra khi mục nhập này được phê duyệt:</span><span class="sxs-lookup"><span data-stu-id="6d804-108">If the combination of the project and the transaction class are mapped to a contract line for a time-and-materials project, two actuals are created when the entry is approved:</span></span>

- <span data-ttu-id="6d804-109">Chi phí thực tế</span><span class="sxs-lookup"><span data-stu-id="6d804-109">Cost actual</span></span> 
- <span data-ttu-id="6d804-110">Doanh số chưa lập hóa đơn thực tế</span><span class="sxs-lookup"><span data-stu-id="6d804-110">Unbilled sales actual</span></span>

<span data-ttu-id="6d804-111">Doanh số chưa lập hóa đơn thực tế thể hiện tồn đọng lập hóa đơn, và trạng thái lập hóa đơn phải được đặt thành **Sẵn sàng lập hóa đơn**.</span><span class="sxs-lookup"><span data-stu-id="6d804-111">Unbilled sales actuals represent the billing backlog, and their billing status must be set to **Ready to Invoice**.</span></span> <span data-ttu-id="6d804-112">Khi một hóa đơn dự án được tạo, doanh số thực tế chưa lập hóa đơn được đánh dấu là **Sẵn sàng lập hóa đơn** sẽ được sao chép thành chi tiết mô tả hóa đơn.</span><span class="sxs-lookup"><span data-stu-id="6d804-112">When a project invoice is created, unbilled sales actuals that are marked **Ready to Invoice** are copied over as invoice line details.</span></span>

<span data-ttu-id="6d804-113">Để xem lại tồn đọng lập hóa đơn cho thời gian và tài liệu, hãy chuyển đến **Doanh số** \> **Lập hóa đơn** \> **Tồn đọng lập hóa đơn thời gian và tài liệu**.</span><span class="sxs-lookup"><span data-stu-id="6d804-113">To review the billing backlog for time and materials, go to **Sales** \> **Billing** \> **Time and Material Billing Backlog**.</span></span> <span data-ttu-id="6d804-114">Chọn tất cả doanh số thực tế chưa lập hóa đơn đã sẵn sàng được lập hóa đơn rồi chọn **Sẵn sàng lập hóa đơn**.</span><span class="sxs-lookup"><span data-stu-id="6d804-114">Select all the unbilled sales actuals that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="6d804-115">Trạng thái lập hóa đơn của các mục thực tế này được thay đổi thành **Sẵn sàng lập hóa đơn**.</span><span class="sxs-lookup"><span data-stu-id="6d804-115">The billing status of these actuals is changed to **Ready to Invoice**.</span></span>

![Tồn đọng lập hóa đơn thời gian và tài liệu](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a><span data-ttu-id="6d804-117">Đánh giá tồn đọng lập hóa đơn sản phẩm</span><span class="sxs-lookup"><span data-stu-id="6d804-117">Review the product billing backlog</span></span>

<span data-ttu-id="6d804-118">Trong PSA, khi hợp đồng dự án có mô tả sản phẩm dựa trên hợp đồng, những nội dung mô tả đó được xem xét để lập hóa đơn bất cứ khi nào hóa đơn được tạo cho hợp đồng dự án.</span><span class="sxs-lookup"><span data-stu-id="6d804-118">In PSA, when a project contract has product-based contract lines, those lines are considered for invoicing whenever an invoice is created for the project contract.</span></span> <span data-ttu-id="6d804-119">Mọi sản phẩm có mô tả hợp đồng được đánh dấu là **Sẵn sàng lập hóa đơn** sẽ được sao chép vào hóa đơn dự án dưới dạng mô tả hóa đơn dự án.</span><span class="sxs-lookup"><span data-stu-id="6d804-119">Any product that has contract lines that are marked **Ready to Invoice** is copied over to the project invoice as project invoice lines.</span></span>

<span data-ttu-id="6d804-120">Để đánh giá tồn đọng lập hóa đơn cho sản phẩm, hãy chuyển đến **Doanh số** \> **Lập hóa đơn** \> **Tồn đọng lập hóa đơn sản phẩm**.</span><span class="sxs-lookup"><span data-stu-id="6d804-120">To review the billing backlog for products, go to **Sales** \> **Billing** \> **Product Billing Backlog**.</span></span> <span data-ttu-id="6d804-121">Chọn tất cả mô tả hợp đồng dựa trên sản phẩm đã sẵn sàng được lập hóa đơn rồi chọn **Sẵn sàng lập hóa đơn**.</span><span class="sxs-lookup"><span data-stu-id="6d804-121">Select all the product-based contract lines that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="6d804-122">Trạng thái lập hóa đơn của những nội dung mô tả này được thay đổi thành **Sẵn sàng lập hóa đơn**.</span><span class="sxs-lookup"><span data-stu-id="6d804-122">The billing status of these lines is changed to **Ready to Invoice**.</span></span>

![Tồn đọng lập hóa đơn sản phẩm](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a><span data-ttu-id="6d804-124">Đánh giá các mốc lập hóa đơn đối với hợp đồng cố định giá</span><span class="sxs-lookup"><span data-stu-id="6d804-124">Review billing milestones on fixed-price contracts</span></span>

<span data-ttu-id="6d804-125">Mỗi nội dung mô tả hợp đồng dự án có một phương thức lập hóa đơn giá cố định phải xác định các cột mốc hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="6d804-125">Each project contract line that has a fixed-price billing method must define contract milestones.</span></span> <span data-ttu-id="6d804-126">Những cột mốc hợp đồng này có thể được lập hóa đơn nếu chúng được đánh dấu là **Sẵn sàng lập hóa đơn**.</span><span class="sxs-lookup"><span data-stu-id="6d804-126">These contract milestones can be invoiced only if they are marked **Ready to Invoice**.</span></span> 

<span data-ttu-id="6d804-127">Để xem lại các cột mốc lập hóa đơn, hãy chuyển đến **Doanh số** \> **Lập hóa đơn** \> **Mốc giá cố định**.</span><span class="sxs-lookup"><span data-stu-id="6d804-127">To review billing milestones, go to **Sales** \> **Billing** \> **Fixed Price Milestones**.</span></span> <span data-ttu-id="6d804-128">Chọn tất cả doanh số thực tế chưa lập hóa đơn đã sẵn sàng được lập hóa đơn rồi chọn **Sẵn sàng lập hóa đơn**.</span><span class="sxs-lookup"><span data-stu-id="6d804-128">Select the milestones that are ready to be invoiced, and then select **Ready to invoice**.</span></span> <span data-ttu-id="6d804-129">Trạng thái lập hóa đơn của các mốc này được thay đổi thành **Sẵn sàng lập hóa đơn**.</span><span class="sxs-lookup"><span data-stu-id="6d804-129">The billing status of these milestones is changed to **Ready to Invoice**.</span></span>

![Mốc giá cố định](media/FPBacklog.png)
