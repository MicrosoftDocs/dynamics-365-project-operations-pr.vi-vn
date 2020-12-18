---
title: Tạo giải pháp cho thông số định giá tùy chỉnh
description: Chủ đề này trình bày thông tin về cách tạo giải pháp cho các thông số giá cả tùy chỉnh.
author: Rumant
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 441501dff23d16960381b3f9fb4b2cceba2b3ba5
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 11/12/2020
ms.locfileid: "4514037"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="7d59d-103">Tạo giải pháp cho thông số định giá tùy chỉnh</span><span class="sxs-lookup"><span data-stu-id="7d59d-103">Create a solution for custom pricing dimensions</span></span>

 <span data-ttu-id="7d59d-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="7d59d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span> 

>[!IMPORTANT]
><span data-ttu-id="7d59d-105">Tất cả các thay đổi về thông số định giá tùy chỉnh phải nằm trong một giải pháp riêng biệt.</span><span class="sxs-lookup"><span data-stu-id="7d59d-105">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="7d59d-106">Cách làm quan trọng này sẽ cho phép bạn thoải mái cập nhật hay loại bỏ các thay đổi khi cần, giúp sử dụng lại công việc và dễ chuyển các thay đổ này sang các phiên bản khác.</span><span class="sxs-lookup"><span data-stu-id="7d59d-106">This important best practice allows the flexibility to update or remove changes as needed, helps with re-use of your work, and makes it easier to port changes to other instances.</span></span> <span data-ttu-id="7d59d-107">Sau khi bạn thực hiện tất cả các thay đổi cần thiết, hãy xuất giải pháp này dưới dạng giải pháp **Được quản lý** và nhập vào các phiên bản khác để tái sử dụng thiết lập giá của bạn.</span><span class="sxs-lookup"><span data-stu-id="7d59d-107">After you make the required changes, export this solution as a **Managed** solution, and then import into other instances for reuse.</span></span>

## <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="7d59d-108">Tạo giải pháp cho thông số định giá tùy chỉnh</span><span class="sxs-lookup"><span data-stu-id="7d59d-108">Create a solution for custom pricing dimensions</span></span>

1.  <span data-ttu-id="7d59d-109">Chọn **Cài đặt** > **Giải pháp** rồi chọn **Mới**.</span><span class="sxs-lookup"><span data-stu-id="7d59d-109">Select **Settings** > **Solutions**, and then select **New**.</span></span>
2.  <span data-ttu-id="7d59d-110">Đặt tên giải pháp này là *<your organization name> thông số giá*.</span><span class="sxs-lookup"><span data-stu-id="7d59d-110">Name the solution, *<your organization name> pricing dimensions*.</span></span>
3. <span data-ttu-id="7d59d-111">Nhập các thông tin cần thiết còn lại, sau đó chọn **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="7d59d-111">Enter the remaining required information, and then select **Save**.</span></span>

  ![Cách tạo giải pháp thông số giá tùy chỉnh](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="7d59d-113">Thêm tất cả các thực thể cần thiết và các thành phần liên quan vào giải pháp Thông số định giá</span><span class="sxs-lookup"><span data-stu-id="7d59d-113">Add all required entities and related components to the Pricing dimension solution</span></span>

<span data-ttu-id="7d59d-114">Thêm các thực thể Project Service sau vào giải pháp giá của bạn để thực hiện những thay đổi quan trọng đối với sơ đồ trong giải pháp giá.</span><span class="sxs-lookup"><span data-stu-id="7d59d-114">Add the following Project Service entities to your pricing solution to make important schema changes in the pricing solution.</span></span> <span data-ttu-id="7d59d-115">Sau khi bạn hoàn tất quy trình này, các thực thể sẽ ghi nhận các thông số giá mới.</span><span class="sxs-lookup"><span data-stu-id="7d59d-115">After you have completed this procedure, the entities will recognize the new pricing dimensions.</span></span>

1.  <span data-ttu-id="7d59d-116">Chọn **Cài đặt** > **Giải pháp** rồi bấm đúp vào **<*tên tổ chức của bạn*> thông số giá**.</span><span class="sxs-lookup"><span data-stu-id="7d59d-116">Select **Settings** > **Solutions**, and then double-click **<*your organization name*> pricing dimensions**.</span></span>
2.  <span data-ttu-id="7d59d-117">Trong Solution Explorer, trên ngăn điều hướng bên trái, chọn **Thêm hiện có** > **Thực thể**.</span><span class="sxs-lookup"><span data-stu-id="7d59d-117">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3.  <span data-ttu-id="7d59d-118">Trong hộp thoại **Thành phần giải pháp**, chọn các thực thể sau:</span><span class="sxs-lookup"><span data-stu-id="7d59d-118">In the **Solution Components** dialog box, select the following entities:</span></span>
 
   - <span data-ttu-id="7d59d-119">**Thực tế**</span><span class="sxs-lookup"><span data-stu-id="7d59d-119">**Actual**</span></span>
   - <span data-ttu-id="7d59d-120">**Nguồn lực có thể đăng ký**</span><span class="sxs-lookup"><span data-stu-id="7d59d-120">**Bookable Resource**</span></span>
   - <span data-ttu-id="7d59d-121">**Mô tả Ước tính**</span><span class="sxs-lookup"><span data-stu-id="7d59d-121">**Estimate Line**</span></span>
   - <span data-ttu-id="7d59d-122">**Nhiệm vụ dự án**</span><span class="sxs-lookup"><span data-stu-id="7d59d-122">**Project Task**</span></span>
   - <span data-ttu-id="7d59d-123">**Chi tiết Mô tả Hóa đơn**</span><span class="sxs-lookup"><span data-stu-id="7d59d-123">**Invoice Line Detail**</span></span>
   - <span data-ttu-id="7d59d-124">**Dòng nhật ký kế toán**</span><span class="sxs-lookup"><span data-stu-id="7d59d-124">**Journal Line**</span></span>
   - <span data-ttu-id="7d59d-125">**Chi tiết Mô tả Hợp đồng Dự án**</span><span class="sxs-lookup"><span data-stu-id="7d59d-125">**Project Contract Line Detail**</span></span>
   - <span data-ttu-id="7d59d-126">**Thành viên Nhóm Dự án**</span><span class="sxs-lookup"><span data-stu-id="7d59d-126">**Project Team Member**</span></span>
   - <span data-ttu-id="7d59d-127">**Chi tiết Mô tả Báo giá**</span><span class="sxs-lookup"><span data-stu-id="7d59d-127">**Quote Line Detail**</span></span>
   - <span data-ttu-id="7d59d-128">**Tăng giá theo Vai trò**</span><span class="sxs-lookup"><span data-stu-id="7d59d-128">**Role Price Markup**</span></span>
   - <span data-ttu-id="7d59d-129">**Giá Vai trò**</span><span class="sxs-lookup"><span data-stu-id="7d59d-129">**Role Price**</span></span>
   - <span data-ttu-id="7d59d-130">**Mục nhập Thời gian**</span><span class="sxs-lookup"><span data-stu-id="7d59d-130">**Time Entry**</span></span>
 
   ![Thêm giải pháp thông số giá tùy chỉnh cho các thực thể hiện có](./media/Existing-entities-to-PD-solution.png)
 
 4. <span data-ttu-id="7d59d-132">Đối với từng thực thể, hãy xem lại các thành phần được thêm cũng như danh sách chính thức của các tài sản thực thể.</span><span class="sxs-lookup"><span data-stu-id="7d59d-132">For each entity, review the components being added and the final list of entity assets for each entity.</span></span> 

   >[!NOTE]
   > <span data-ttu-id="7d59d-133">Đưa vào tất cả biểu mẫu và dạng xem cho từng thực thể đã chọn.</span><span class="sxs-lookup"><span data-stu-id="7d59d-133">Include all forms and views for each of the selected entities.</span></span>

  ![Đã thêm thực thể](./media/solution-component-selection.png)


5.  <span data-ttu-id="7d59d-135">Khi được nhắc đưa vào bất kỳ thực thể phụ thuộc nào cho các thực thể đã chọn, hãy bấm vào **Không, không đưa vào các thành phần bắt buộc.**</span><span class="sxs-lookup"><span data-stu-id="7d59d-135">When prompted to include any dependent entities for the selected entities, select **No, do not include required components.**</span></span>

    ![Đưa vào các thực thể phụ thuộc](./media/Do-not-include-required.png)
