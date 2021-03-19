---
title: Tạo danh sách giá
description: Làm cách nào để tạo bảng giá trong Project Service
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 0732ccca43e404412efae8a91873e43c28d041ca
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290341"
---
# <a name="create-a-price-list-project-service"></a><span data-ttu-id="9276d-103">Tạo bảng giá (Project Service)</span><span class="sxs-lookup"><span data-stu-id="9276d-103">Create a price list (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="9276d-104">Bảng giá cung cấp một mẫu mà quản lý khách hàng của bạn có thể sử dụng để tạo báo giá và dự án và để thiết lập chi phí của dự án.</span><span class="sxs-lookup"><span data-stu-id="9276d-104">Price lists provide a template your account managers can use for creating quotes and projects, and for establishing the costs of a project.</span></span> <span data-ttu-id="9276d-105">Chúng cung cấp danh sách mục hàng của vai trò và chi phí và giá bạn sẽ tính cho từng mục.</span><span class="sxs-lookup"><span data-stu-id="9276d-105">They provide a line item list of roles and expenses, and the price you will charge for each.</span></span> <span data-ttu-id="9276d-106">Bạn có thể tạo nhiều bảng giá để bạn có thể duy trì cấu trúc giá riêng biệt cho các khu vực khác mà bạn bán sản phẩm theo hoặc cho các kênh bán hàng khác nhau.</span><span class="sxs-lookup"><span data-stu-id="9276d-106">You can create multiple price lists so that you can maintain separate price structures for different regions you sell your products in or for different sales channels.</span></span> <span data-ttu-id="9276d-107">Ý tưởng hay là tạo ít nhất một bảng giá cho mọi loại tiền bạn lập kế hoạch để tính hóa đơn cho khách hàng.</span><span class="sxs-lookup"><span data-stu-id="9276d-107">It’s a good idea to create at least one price list for every currency you plan to bill your customers in.</span></span>  
  
<span data-ttu-id="9276d-108">Để tạo ước tính tài chính cho công việc được giao, đảm bảo mỗi dự án có một bảng giá bán hàng và chi phí dự phòng.</span><span class="sxs-lookup"><span data-stu-id="9276d-108">To create financial estimates for the work to be delivered, make sure every project has a backing cost and sales price list.</span></span> <span data-ttu-id="9276d-109">Thiết lập bảng giá bán hàng và chi phí mặc định áp dụng cho tất cả dự án được tạo trong tổ chức của bạn.</span><span class="sxs-lookup"><span data-stu-id="9276d-109">Set up a default cost and sales pricelist that applies to all projects created in your organization.</span></span>  
  
<span data-ttu-id="9276d-110">Bảng giá dựa vào các loại vai trò và chi phí, vì vậy trước khi bạn tạo một bảng giá, hãy chắc chắn rằng bạn đã cấu hình các loại vai trò và chi phí mà bạn muốn sử dụng trong khi tạo bảng giá.</span><span class="sxs-lookup"><span data-stu-id="9276d-110">Price lists rely on roles and expense categories, so before you create a price list, make sure you’ve already configured the roles and expense categories you want to use while creating the price list.</span></span>  
  
1.  <span data-ttu-id="9276d-111">Đi tới **Project Service > Bảng giá**.</span><span class="sxs-lookup"><span data-stu-id="9276d-111">Go to **Project Service > Price Lists**.</span></span>  
  
2.  <span data-ttu-id="9276d-112">Bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="9276d-112">Click **New**.</span></span>  
  
3.  <span data-ttu-id="9276d-113">Trong **Ngữ cảnh**, chọn xem bảng giá này có dành cho **Chi phí**, **Mua** hoặc **Bán hàng** không.</span><span class="sxs-lookup"><span data-stu-id="9276d-113">In **Context**, select whether this price list is for **Cost**, **Purchase**, or **Sales**.</span></span>  
  
4.  <span data-ttu-id="9276d-114">Trong **Tên**, nhập tên cho bảng giá.</span><span class="sxs-lookup"><span data-stu-id="9276d-114">In **Name**, enter a name for the price list.</span></span>  
  
5.  <span data-ttu-id="9276d-115">Trong **Loại tiền**, chọn loại tiền bạn sẽ sử dụng để lập hóa đơn hoặc tính chi phí.</span><span class="sxs-lookup"><span data-stu-id="9276d-115">In **Currency**, select the currency you’re going to use for billing or costing.</span></span>  
  
6.  <span data-ttu-id="9276d-116">Trong **Đơn vị thời gian**, chỉ định khoảng thời gian áp dụng giá, chẳng hạn như ngày hoặc giờ.</span><span class="sxs-lookup"><span data-stu-id="9276d-116">In **Time Unit**, specify the period of time the price applies to, such as day or hour.</span></span>  
  
7.  <span data-ttu-id="9276d-117">Điền vào **Ngày bắt đầu**, **Ngày kết thúc** và **Mô tả** khi cần.</span><span class="sxs-lookup"><span data-stu-id="9276d-117">Fill in the **Start Date**, **End Date**, and **Description** as needed.</span></span>  
  
8.  <span data-ttu-id="9276d-118">Bấm vào **Lưu** để tạo bản ghi để bạn có thể tiếp tục chỉnh sửa.</span><span class="sxs-lookup"><span data-stu-id="9276d-118">Click **Save** to create the record so you can continue editing it.</span></span>  
  
9. <span data-ttu-id="9276d-119">Để thêm giá vai trò vào bảng giá, bấm vào **+** trong **Giá vai trò**.</span><span class="sxs-lookup"><span data-stu-id="9276d-119">To add a role price to the price list, click **+** under **Role prices**.</span></span>  
  
10. <span data-ttu-id="9276d-120">Trong ngăn **Giá vai trò**, điền thông tin chi tiết, sau đó bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="9276d-120">In the **Role Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="9276d-121">Tiếp tục thêm giá vai trò khi cần thiết.</span><span class="sxs-lookup"><span data-stu-id="9276d-121">Continue adding role prices as necessary.</span></span> <span data-ttu-id="9276d-122">Khi bạn hoàn tất, bấm vào **Lưu** ở góc dưới cùng bên phải của màn hình.</span><span class="sxs-lookup"><span data-stu-id="9276d-122">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
11. <span data-ttu-id="9276d-123">Để thêm giá loại chi phí vào bảng giá, bấm vào **+** trong **Giá loại**.</span><span class="sxs-lookup"><span data-stu-id="9276d-123">To add an expense category price to the price list, click **+** under **Category prices**.</span></span>  
  
12. <span data-ttu-id="9276d-124">Trong ngăn **Giá loại giao dịch**, điền thông tin chi tiết, sau đó bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="9276d-124">In the **Transaction Category Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="9276d-125">Tiếp tục thêm giá loại khi cần thiết.</span><span class="sxs-lookup"><span data-stu-id="9276d-125">Continue adding category prices as necessary.</span></span> <span data-ttu-id="9276d-126">Khi bạn hoàn tất, bấm vào **Lưu** ở góc dưới cùng bên phải của màn hình.</span><span class="sxs-lookup"><span data-stu-id="9276d-126">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
13. <span data-ttu-id="9276d-127">Để thêm hạng mục trong bảng giá vào bảng giá, bấm vào **+** trong **Hạng mục trong Bảng giá**.</span><span class="sxs-lookup"><span data-stu-id="9276d-127">To add price list items to the price list, click **+** under **Price List Items**.</span></span>  
  
14. <span data-ttu-id="9276d-128">Trong ngăn **Mục bảng giá**, điền thông tin chi tiết, sau đó bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="9276d-128">In the **Price List Item** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="9276d-129">Tiếp tục thêm mục bảng giá khi cần thiết.</span><span class="sxs-lookup"><span data-stu-id="9276d-129">Continue adding price list items as necessary.</span></span> <span data-ttu-id="9276d-130">Khi bạn hoàn tất, bấm vào **Lưu** ở góc dưới cùng bên phải của màn hình.</span><span class="sxs-lookup"><span data-stu-id="9276d-130">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
15. <span data-ttu-id="9276d-131">Để thêm mối quan hệ lãnh thổ vào bảng giá, bấm vào **+** trong **Mối quan hệ Lãnh thổ**.</span><span class="sxs-lookup"><span data-stu-id="9276d-131">To add territory relationships to the price list, click **+** under **Territory Relationships**.</span></span>  
  
16. <span data-ttu-id="9276d-132">Trong cửa sổ **Kết nối mới**, điền thông tin chi tiết, sau đó bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="9276d-132">In the **New Connection** window, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="9276d-133">Tiếp tục thêm mối quan hệ lãnh thổ khi cần thiết.</span><span class="sxs-lookup"><span data-stu-id="9276d-133">Continue adding territory relationships as necessary.</span></span> <span data-ttu-id="9276d-134">Khi bạn hoàn tất, bấm vào **Lưu** ở góc dưới cùng bên phải của màn hình.</span><span class="sxs-lookup"><span data-stu-id="9276d-134">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="9276d-135">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="9276d-135">See Also</span></span>  
 [<span data-ttu-id="9276d-136">Đặt cấu hình Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="9276d-136">Configure Project Service Automation</span></span>](../psa/configure.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]