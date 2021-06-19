---
title: Cập nhật các thuộc tính phần bổ trợ để bao gồm thông số định giá mới
description: Chủ đề này cung cấp thông tin về cách cập nhật thuộc tính phần bổ trợ cho các thông số định giá.
author: Rumant
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: b0d50733340f277453f4ef5b52bdd3ee089449cd
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012837"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a><span data-ttu-id="8b163-103">Cập nhật các thuộc tính phần bổ trợ để bao gồm thông số định giá mới</span><span class="sxs-lookup"><span data-stu-id="8b163-103">Update plug-in attributes to include new pricing dimensions</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

> [!NOTE]
> <span data-ttu-id="8b163-104">Nếu đang không dùng tính năng Báo giá và Hợp đồng của Project Service Automation (PSA), bạn có thể bỏ qua chủ đề này.</span><span class="sxs-lookup"><span data-stu-id="8b163-104">If you are not using the Project Service Automation (PSA) Quoting and Contracting features, you can skip this topic.</span></span>

<span data-ttu-id="8b163-105">Chủ đề này giả định rằng bạn đã hoàn tất quy trình trong các chủ đề [Tạo trường và thực thể tùy chỉnh](create-custom-fields-entities.md), [Thêm các trường tùy chỉnh vào thực thể thiết lập và giao dịch giá](field-references.md) và [Thiết lập trường tùy chỉnh làm thông số định giá](set-up-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="8b163-105">This topic assumes that you have completed the procedures in the topics, [Create custom fields and entities](create-custom-fields-entities.md), [Add custom fields to price setup and transactional entities](field-references.md), and [Set up custom fields as pricing dimensions](set-up-pricing-dimensions.md).</span></span> <span data-ttu-id="8b163-106">Nếu bạn chưa hoàn thành các quy trình đó, hãy quay lại và hoàn thành chúng rồi trở lại chủ đề này.</span><span class="sxs-lookup"><span data-stu-id="8b163-106">If you haven't completed those procedures, go back and complete them and then return to this topic.</span></span>

<span data-ttu-id="8b163-107">Khi chi tiết mô tả báo giá được tạo trên trang **Mô tả báo giá** cho chi tiết báo giá dự án, hệ thống sẽ tạo 2 mô tả ước tính trong nền -- một mô tả cho chi phí ước tính và một mô tả cho doanh số.</span><span class="sxs-lookup"><span data-stu-id="8b163-107">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines in the background -- one line for the cost side of the estimate and one for sales side.</span></span> <span data-ttu-id="8b163-108">Điều này tương tự cho các mô tả hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="8b163-108">This is the same  for project contract lines.</span></span>

<span data-ttu-id="8b163-109">Khi bạn thay đổi số lượng hoặc trường đối với chi phí, thay đổi đó sẽ được chuyển sang bên doanh số.</span><span class="sxs-lookup"><span data-stu-id="8b163-109">When you make a change to the quantity or a field on the cost side, that change is propagated to the sales side.</span></span> <span data-ttu-id="8b163-110">Điều này có thể do phần bổ trợ sau phải được đăng ký lại sau khi thay đổi thông số định giá.</span><span class="sxs-lookup"><span data-stu-id="8b163-110">This is possible because of the following plug-ins that must be re-registered after a change to pricing dimensions.</span></span>

- <span data-ttu-id="8b163-111">PreOperationContractLineDetailUpdate - Cập nhật **msdyn_orderlinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="8b163-111">PreOperationContractLineDetailUpdate - Updates **msdyn_orderlinetransaction**.</span></span>
- <span data-ttu-id="8b163-112">PreOperationQuoteLineDetailUpdate - Cập nhật **msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="8b163-112">PreOperationQuoteLineDetailUpdate - Updates **msdyn_quotelinetransaction**.</span></span>

<span data-ttu-id="8b163-113">Các bước sau đây giải thích cho bạn quy trình đăng ký phần bổ trợ.</span><span class="sxs-lookup"><span data-stu-id="8b163-113">The following steps walk you through the process of registering the plug-ins.</span></span>

1. <span data-ttu-id="8b163-114">Mở **PluginRegistrationTool** và kết nối với phiên bản trực tuyến của bạn.</span><span class="sxs-lookup"><span data-stu-id="8b163-114">Open the **PluginRegistrationTool** and connect to your online instance.</span></span>
2. <span data-ttu-id="8b163-115">Bấm vào **Tìm kiếm** và tìm kiếm phần bổ trợ để được cập nhật.</span><span class="sxs-lookup"><span data-stu-id="8b163-115">Click **Search** and search for the plug-in to be updated.</span></span>

 ![Ảnh chụp màn hình về cây tìm kiếm](media/PRT-1.png)

3. <span data-ttu-id="8b163-117">Sau khi tìm thấy phần bổ trợ, hãy chọn phần bổ trợ đó rồi bấm vào **Chọn trên biểu mẫu chính**.</span><span class="sxs-lookup"><span data-stu-id="8b163-117">After the plug-in is found, select it and then click **Select on Main Form**.</span></span>

4. <span data-ttu-id="8b163-118">Chọn bước của phần bổ trợ sẽ được cập nhật, bấm chuột phải rồi chọn **Cập nhật**.</span><span class="sxs-lookup"><span data-stu-id="8b163-118">Select the step of the plug-in to be updated, right-click, and then select **Update**.</span></span>

 ![Ảnh chụp màn hình về phần bổ trợ sẽ được cập nhật](media/PRT-2.png)
 
5. <span data-ttu-id="8b163-120">Trong cửa sổ cập nhật, hãy bấm vào dấu ba chấm (**...**) trong các thuộc tính lọc.</span><span class="sxs-lookup"><span data-stu-id="8b163-120">In the update window, click the ellipsis (**...**) in the filtering attributes.</span></span>

 ![Ảnh chụp màn hình về Cập nhật thông tin cấu hình bước hiện có](media/PRT-3.png)
 
6. <span data-ttu-id="8b163-122">Chọn hộp kiểm thuộc tính định giá.</span><span class="sxs-lookup"><span data-stu-id="8b163-122">Select the pricing attribute check boxes.</span></span>

 ![Ảnh chụp màn hình minh họa thao tác lựa chọn hộp kiểm cho thuộc tính định giá](media/PRT-4.png)

7. <span data-ttu-id="8b163-124">Bấm **OK** để đóng trang rồi chọn **Cập nhật bước**.</span><span class="sxs-lookup"><span data-stu-id="8b163-124">Click **OK** to close the page and then select **Update Step**.</span></span>

 ![Ảnh chụp màn hình hiển thị nút “Cập nhật bước”](media/PRT-5.png)
 
8. <span data-ttu-id="8b163-126">Lặp lại quá trình này cho phần bổ trợ thứ hai **PreOperationQuoteLineDetail - Update of msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="8b163-126">Repeat this process for the second plug-in, **PreOperationQuoteLineDetail - Update of msdyn_quotelinetransaction**.</span></span>

9. <span data-ttu-id="8b163-127">Đóng công cụ đăng ký phần bổ trợ.</span><span class="sxs-lookup"><span data-stu-id="8b163-127">Close the plug-in registration tool.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]