---
title: Cập nhật thuộc tính phần bổ trợ với các thông số định giá mới
description: Chủ đề này cung cấp thông tin về cách cập nhật thuộc tính phần bổ trợ đối với các thông số định giá.
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7999c003a0cf670d586ebf4445901e106fbee39f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274709"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a><span data-ttu-id="b2adf-103">Cập nhật thuộc tính phần bổ trợ với các thông số định giá mới</span><span class="sxs-lookup"><span data-stu-id="b2adf-103">Update plug-in attributes with new pricing dimensions</span></span>

<span data-ttu-id="b2adf-104">Chủ đề này cung cấp thông tin về cách cập nhật thuộc tính phần bổ trợ đối với các thông số định giá.</span><span class="sxs-lookup"><span data-stu-id="b2adf-104">This topic provides information about how to update plug-in attributes for pricing dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="b2adf-105">Chủ đề này chỉ áp dụng cho báo giá và hợp đồng có trong Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="b2adf-105">This topic is only applicable to the quote and contract features in Dynamics 365 Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b2adf-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="b2adf-106">Prerequisites</span></span>
<span data-ttu-id="b2adf-107">Trước khi hoàn tất các bước trong chủ đề này, bạn phải hoàn thành xong các quy trình trong các chủ đề sau đây:</span><span class="sxs-lookup"><span data-stu-id="b2adf-107">Before you complete the steps in this topic, you must have completed the procedures in the following topics:</span></span>

  - [<span data-ttu-id="b2adf-108">Tạo thực thể và trường tùy chỉnh</span><span class="sxs-lookup"><span data-stu-id="b2adf-108">Create custom fields and entities</span></span>](create-custom-fields-entities-pricing-dimensions.md) 
  - [<span data-ttu-id="b2adf-109">Thêm trường tùy chỉnh vào thực thể giao dịch và thiết lập giá </span><span class="sxs-lookup"><span data-stu-id="b2adf-109">Add custom fields to price setup and transactional entities</span></span>](add-custom-fields-price-setup-transactional-entities.md)
  - <span data-ttu-id="b2adf-110">[Thiết lập trường tùy chỉnh làm thông số định giá](set-up-custom-fields-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="b2adf-110">[Set up custom fields as pricing dimensions](set-up-custom-fields-pricing-dimensions.md).</span></span> 
  
<span data-ttu-id="b2adf-111">Nếu bạn chưa hoàn thành các quy trình đó, hãy hoàn thành rồi trở lại chủ đề này.</span><span class="sxs-lookup"><span data-stu-id="b2adf-111">If you haven't completed those procedures, complete them and then return to this topic.</span></span>

## <a name="register-a-plug-in"></a><span data-ttu-id="b2adf-112">Đăng ký phần bổ trợ</span><span class="sxs-lookup"><span data-stu-id="b2adf-112">Register a plug-in</span></span>
<span data-ttu-id="b2adf-113">Khi chi tiết của dòng báo giá được tạo trên trang **Dòng báo giá** cho một dòng báo giá dự án, hệ thống sẽ tạo 2 dòng ước tính.</span><span class="sxs-lookup"><span data-stu-id="b2adf-113">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines.</span></span> <span data-ttu-id="b2adf-114">Một dòng là mặt chi phí của ước tính và dòng còn lại là mặt doanh số.</span><span class="sxs-lookup"><span data-stu-id="b2adf-114">One line is for the cost side of the estimate and the other line is for sales the side.</span></span> <span data-ttu-id="b2adf-115">Điều này tương tự cho các mô tả hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="b2adf-115">This is the same  for project contract lines.</span></span>

<span data-ttu-id="b2adf-116">Khi bạn thay đổi số lượng hoặc trường đối với mặt chi phí, thay đổi đó cũng sẽ áp dụng cho mặt doanh số.</span><span class="sxs-lookup"><span data-stu-id="b2adf-116">When you make a change to the quantity or a field on the cost side, that change is also made on the sales side.</span></span> <span data-ttu-id="b2adf-117">Nguyên nhân có thể là do các phần bổ trợ PreOperation trên thực thể Quotelinedetail và contractline detail kết nối các thuộc tính cụ thể mở mặt chi phí với mặt doanh số của giao dịch.</span><span class="sxs-lookup"><span data-stu-id="b2adf-117">This is possible because the PreOperation plug-ins on Quotelinedetail and contractline detail entities connect specific attributes on the cost side to the sales side of the transaction.</span></span> <span data-ttu-id="b2adf-118">Nếu muốn các thay đổi đối với giá trị thông số định giá trên mặt doanh số cũng áp dụng cho mặt chi phí, thì bạn phải đăng ký những phần bổ trợ sau đây sau khi thay đổi thông số định giá.</span><span class="sxs-lookup"><span data-stu-id="b2adf-118">If you need changes made to the pricing dimension values on the sales side to also be made on the cost side, the following plug-ins must be re-registered after making changes to a pricing dimension.</span></span>

<span data-ttu-id="b2adf-119">Sau đây là những phần bổ trợ cần cập nhật và đăng ký lại:</span><span class="sxs-lookup"><span data-stu-id="b2adf-119">These are the plug-ins to update and re-register:</span></span>

- <span data-ttu-id="b2adf-120">PreOperationContractLineDetailUpdate - **Cập nhật msdyn_orderlinetransaction**</span><span class="sxs-lookup"><span data-stu-id="b2adf-120">PreOperationContractLineDetailUpdate - **Update msdyn_orderlinetransaction**</span></span>
- <span data-ttu-id="b2adf-121">PreOperationQuoteLineDetailUpdate - **Cập nhật msdyn_quotelinetransaction**</span><span class="sxs-lookup"><span data-stu-id="b2adf-121">PreOperationQuoteLineDetailUpdate - **Updates msdyn_quotelinetransaction**</span></span>

<span data-ttu-id="b2adf-122">Hoàn tất các bước sau để cập nhật và đăng ký lại các phần bổ trợ.</span><span class="sxs-lookup"><span data-stu-id="b2adf-122">Complete the following steps to update and re-register the plug-ins.</span></span>

1. <span data-ttu-id="b2adf-123">Mở **PluginRegistrationTool** rồi kết nối với môi trường Project Operations Dataverse.</span><span class="sxs-lookup"><span data-stu-id="b2adf-123">Open **PluginRegistrationTool** and connect to your Project Operations Dataverse environment.</span></span>
2. <span data-ttu-id="b2adf-124">Chọn **Tìm kiếm** rồi nhập một vài chữ cái đầu tiên của phần bổ trợ cần cập nhật.</span><span class="sxs-lookup"><span data-stu-id="b2adf-124">Select **Search**, and type in the first few letters of the plug-in to be updated.</span></span>
3. <span data-ttu-id="b2adf-125">Hãy chọn phần bổ trợ tìm thấy rồi bấm vào **Chọn trên biểu mẫu chính**.</span><span class="sxs-lookup"><span data-stu-id="b2adf-125">After the plug-in is found, select it, and then select **Select on Main Form**.</span></span>
4. <span data-ttu-id="b2adf-126">Chọn bước **Cập nhật msdyn_orderlinetransaction**, bấm chuột phải rồi chọn **Cập nhật**.</span><span class="sxs-lookup"><span data-stu-id="b2adf-126">Select the **Update msdyn_orderlinetransaction** step, right-click, and then select **Update**.</span></span>
5. <span data-ttu-id="b2adf-127">Trong trang hộp thoại **Cập nhật**, hãy chọn dấu 3 chấm (**...**) trong thuộc tính lọc.</span><span class="sxs-lookup"><span data-stu-id="b2adf-127">In the **Update** dialog page, select the ellipsis (**...**) in the filtering attributes.</span></span>
6. <span data-ttu-id="b2adf-128">Cửa sổ thuộc tính lọc sẽ mở ra, chứa danh sách mọi thuộc tính lọc trong thực thể và các thông số định giá.</span><span class="sxs-lookup"><span data-stu-id="b2adf-128">The filtering attributes window opens and provides a list of all attributes in the entity and the pricing dimensions.</span></span> <span data-ttu-id="b2adf-129">Đánh dấu vào các ô tương ứng với các thuộc tính thông số định giá.</span><span class="sxs-lookup"><span data-stu-id="b2adf-129">Select the check boxes for the pricing dimension attributes.</span></span>
7. <span data-ttu-id="b2adf-130">Chọn **OK** để đóng trang rồi chọn **Bước cập nhật**.</span><span class="sxs-lookup"><span data-stu-id="b2adf-130">Select **OK** to close the page, and then select **Update Step**.</span></span>
8. <span data-ttu-id="b2adf-131">Lặp lại các bước từ 2-7 cho phần bổ trợ thứ hai **PreOperationQuoteLineDetail**.</span><span class="sxs-lookup"><span data-stu-id="b2adf-131">Repeat steps 2-7 for the second plug-in, **PreOperationQuoteLineDetail**.</span></span> <span data-ttu-id="b2adf-132">Đối với phần bổ trợ này, bạn cần cập nhật bước **Update of msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="b2adf-132">For this plug-in, you need to update the **Update of msdyn_quotelinetransaction** step.</span></span>
9. <span data-ttu-id="b2adf-133">Đóng **PluginRegistrationTool**.</span><span class="sxs-lookup"><span data-stu-id="b2adf-133">Close **PluginRegistrationTool**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]