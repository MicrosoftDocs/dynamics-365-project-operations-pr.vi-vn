---
title: Tạo báo giá của dự án từ cơ hội
description: Chủ đề này cung cấp thông tin về cách tạo báo giá của dự án từ cơ hội.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 606098473db479d0015e3a7a3c01a3d3b6de9db1
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898558"
---
# <a name="create-project-quotes-from-opportunities"></a><span data-ttu-id="6dbd6-103">Tạo báo giá của dự án từ cơ hội</span><span class="sxs-lookup"><span data-stu-id="6dbd6-103">Create project quotes from opportunities</span></span>

<span data-ttu-id="6dbd6-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="6dbd6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6dbd6-105">Báo giá có thể được tạo từ cơ hội dự án theo những cách sau:</span><span class="sxs-lookup"><span data-stu-id="6dbd6-105">Quotes can be created from project opportunities in the following ways:</span></span>

- <span data-ttu-id="6dbd6-106">Từ tab **Báo giá** trên trang **Cơ hội dự án**</span><span class="sxs-lookup"><span data-stu-id="6dbd6-106">From the **Quotes** tab on the **Project Opportunity** page</span></span>
- <span data-ttu-id="6dbd6-107">Từ Dòng quy trình bán hàng từ cơ hội</span><span class="sxs-lookup"><span data-stu-id="6dbd6-107">From the Opportunity sales process flow</span></span>
- <span data-ttu-id="6dbd6-108">Bằng cách cập nhật tham chiếu cơ hội trên một báo giá hiện có</span><span class="sxs-lookup"><span data-stu-id="6dbd6-108">By updating the opportunity reference on an existing quote</span></span>

## <a name="from-the-quotes-tab-of-the-project-opportunity-page"></a><span data-ttu-id="6dbd6-109">Từ tab Báo giá của trang Cơ hội dự án</span><span class="sxs-lookup"><span data-stu-id="6dbd6-109">From the Quotes tab of the Project Opportunity page</span></span>

<span data-ttu-id="6dbd6-110">Để tạo báo giá dự án từ cơ hội, hãy hoàn thành các bước sau.</span><span class="sxs-lookup"><span data-stu-id="6dbd6-110">To create a project quote from an opportunity, complete the following steps.</span></span>

1. <span data-ttu-id="6dbd6-111">Mở trang **Cơ hội dự án** rồi chọn tab **Báo giá**.</span><span class="sxs-lookup"><span data-stu-id="6dbd6-111">Open the **Project Opportunity** page and select the **Quotes** tab.</span></span> 
2. <span data-ttu-id="6dbd6-112">Trên lưới con **Báo giá**, hãy chọn **+** để tạo báo giá dự án mới dựa trên cơ hội.</span><span class="sxs-lookup"><span data-stu-id="6dbd6-112">On the **Quotes** sub-grid, select the **+** to create a new project quote based on the opportunity.</span></span> <span data-ttu-id="6dbd6-113">Tất cả các mô tả cơ hội và Bảng giá dự án có liên quan được sao chép sang báo giá mới từ cơ hội.</span><span class="sxs-lookup"><span data-stu-id="6dbd6-113">All of the opportunity lines and related Project price lists are copied to the new quote from the opportunity.</span></span>

## <a name="from-the-opportunity-sales-process-flow"></a><span data-ttu-id="6dbd6-114">Từ Dòng quy trình bán hàng từ cơ hội</span><span class="sxs-lookup"><span data-stu-id="6dbd6-114">From the Opportunity sales process flow</span></span>

<span data-ttu-id="6dbd6-115">Để tạo báo giá dự án từ Dòng quy trình bán hàng từ cơ hội, hãy hoàn thành các bước sau.</span><span class="sxs-lookup"><span data-stu-id="6dbd6-115">To create a quote from the Opportunity sales process flow, complete the following steps.</span></span>

1. <span data-ttu-id="6dbd6-116">Từ Dòng quy trình bán hàng từ cơ hội, hãy mở Cơ hội.</span><span class="sxs-lookup"><span data-stu-id="6dbd6-116">From the Opportunity sales process flow, open the Opportunity.</span></span>
2. <span data-ttu-id="6dbd6-117">Chọn giai đoạn **Định tính**.</span><span class="sxs-lookup"><span data-stu-id="6dbd6-117">Select the **Qualify** stage.</span></span> 
3. <span data-ttu-id="6dbd6-118">Chọn **Tiếp theo** rồi chọn **+ Tạo** để tạo một báo giá mới.</span><span class="sxs-lookup"><span data-stu-id="6dbd6-118">Select **Next** and then select **+ Create** to create a new quote.</span></span> <span data-ttu-id="6dbd6-119">Hầu hết thông tin trên tab **Tóm tắt** cho báo giá mới này sẽ được mặc định từ cơ hội.</span><span class="sxs-lookup"><span data-stu-id="6dbd6-119">Most of the information on the **Summary** tab for this new quote will have defaulted from the opportunity.</span></span> 
4. <span data-ttu-id="6dbd6-120">Nhập bất kỳ thông tin bắt buộc nào bị thiếu hoặc cập nhật các giá trị mặc định nếu cần trên tab **Tóm tắt**,</span><span class="sxs-lookup"><span data-stu-id="6dbd6-120">Enter in any required information that is missing, or update defaulted values as necessary on the **Summary** tab,</span></span>
5. <span data-ttu-id="6dbd6-121">Chọn **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="6dbd6-121">Select **Save**.</span></span> <span data-ttu-id="6dbd6-122">Báo giá mới được tạo và liên kết với cơ hội.</span><span class="sxs-lookup"><span data-stu-id="6dbd6-122">The new quote is created and associated to the opportunity.</span></span> <span data-ttu-id="6dbd6-123">Giờ đây, bạn có thể xem thông tin báo giá trên tab **Báo giá** của trang **Cơ hội**.</span><span class="sxs-lookup"><span data-stu-id="6dbd6-123">You can now view the quote information on the **Quotes** tab of the **Opportunity** page.</span></span> 

   <span data-ttu-id="6dbd6-124">Quy trình bán hàng từ cơ hội sẽ chuyển sang giai đoạn tiếp theo là giai đoạn **Đề xuất**.</span><span class="sxs-lookup"><span data-stu-id="6dbd6-124">The Opportunity sales process moves to the next stage, **Propose**.</span></span>


## <a name="by-updating-the-opportunity-reference-on-an-existing-quote"></a><span data-ttu-id="6dbd6-125">Bằng cách cập nhật tham chiếu cơ hội trên một báo giá hiện có</span><span class="sxs-lookup"><span data-stu-id="6dbd6-125">By updating the opportunity reference on an existing quote</span></span>

<span data-ttu-id="6dbd6-126">Báo giá hiện có có thể được liên kết với Cơ hội.</span><span class="sxs-lookup"><span data-stu-id="6dbd6-126">An existing quote can be linked to an Opportunity.</span></span> <span data-ttu-id="6dbd6-127">Hoàn thành các bước sau để cập nhật Thông tin cơ hội trên báo giá hiện có.</span><span class="sxs-lookup"><span data-stu-id="6dbd6-127">Complete the following steps to update the Opportunity information on an existing quote.</span></span>

1. <span data-ttu-id="6dbd6-128">Mở trang **Báo giá** rồi chọn tab **Tóm tắt**.</span><span class="sxs-lookup"><span data-stu-id="6dbd6-128">Open the **Quote** page and select the **Summary** tab.</span></span>
2. <span data-ttu-id="6dbd6-129">Trong trường **Cơ hội**, hãy chọn cơ hội mà bạn muốn liên kết đến báo giá.</span><span class="sxs-lookup"><span data-stu-id="6dbd6-129">In the **Opportunity** field, select the opportunity that you want to link to the quote.</span></span> <span data-ttu-id="6dbd6-130">Bạn có thể xem báo giá trong lưới **Báo giá** của Cơ hội.</span><span class="sxs-lookup"><span data-stu-id="6dbd6-130">You can see the quote in the **Quotes** grid of the Opportunity.</span></span> 
3. <span data-ttu-id="6dbd6-131">Sử dụng Quy trình bán hàng từ cơ hội, cơ hội có thể được chuyển sang giai đoạn tiếp theo là giai đoạn **Đề xuất**.</span><span class="sxs-lookup"><span data-stu-id="6dbd6-131">Using the Opportunity sales process, the opportunity can be moved to the next stage, **Propose**.</span></span> 

   <span data-ttu-id="6dbd6-132">Khi bạn chuyển một cơ hội sang giai đoạn này, bạn có thể chọn báo giá này từ danh sách các báo giá được liên kết với cơ hội này.</span><span class="sxs-lookup"><span data-stu-id="6dbd6-132">When you move an opportunity to this stage, you can select this quote from a list of quotes associated with this opportunity.</span></span> <span data-ttu-id="6dbd6-133">Việc chọn báo giá này cho thấy rằng bạn đang tiếp tục với báo giá.</span><span class="sxs-lookup"><span data-stu-id="6dbd6-133">Selecting this quote indicates that you're moving forward with it.</span></span>

   <span data-ttu-id="6dbd6-134">Tất cả báo giá khác được liên kết với Cơ hội sẽ vẫn có sẵn và hiện hoạt cho đến khi bạn giành được một trong số các báo giá đó.</span><span class="sxs-lookup"><span data-stu-id="6dbd6-134">All the other quotes associated with the Opportunity will still be available and active until one of them is won.</span></span> <span data-ttu-id="6dbd6-135">Bạn có thể chuyển quy trình bán hàng trở lại giai đoạn trước đó là giai đoạn **Định tính** rồi chọn một báo giá khác để tiếp tục.</span><span class="sxs-lookup"><span data-stu-id="6dbd6-135">You can move the sales process back to the previous stage **Qualify**, and pick another quote to move forward with.</span></span>
