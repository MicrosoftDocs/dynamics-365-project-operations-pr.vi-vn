---
title: Tạo giải pháp tùy chỉnh cho thông số định giá
description: Chủ đề này giải thích cách tạo giải pháp tùy chỉnh khi tạo thông số định giá tùy chỉnh.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 3810df9b875d017a8d639b5253b96275571898f3
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144665"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a><span data-ttu-id="ce055-103">Tạo giải pháp tùy chỉnh cho thông số định giá</span><span class="sxs-lookup"><span data-stu-id="ce055-103">Create custom solutions for pricing dimensions</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

> [!IMPORTANT]
> <span data-ttu-id="ce055-104">Tất cả các thay đổi về thông số định giá tùy chỉnh phải nằm trong một giải pháp riêng biệt.</span><span class="sxs-lookup"><span data-stu-id="ce055-104">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="ce055-105">Cách làm quan trọng này sẽ giúp bạn có thể thoải mái cập nhật hay loại bỏ các thay đổi khi cần, giúp sử dụng lại công việc và dễ chuyển các thay đổ này sang phiên bản khác.</span><span class="sxs-lookup"><span data-stu-id="ce055-105">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="ce055-106">Sau khi bạn thực hiện các thay đổi cần thiết, hãy xuất giải pháp này dưới dạng **Giải pháp được quản lý** và nhập nó vào các phiên bản khác để tái sử dụng thiết lập giá của bạn.</span><span class="sxs-lookup"><span data-stu-id="ce055-106">After you make the required changes, export this solution as a **Managed solution**, and import it into other instances to reuse your pricing setup.</span></span>

1. <span data-ttu-id="ce055-107">Chọn **Cài đặt** > **Giải pháp** rồi chọn **Mới**.</span><span class="sxs-lookup"><span data-stu-id="ce055-107">Select **Settings** > **Solutions**, and then select **New**.</span></span> 
2. <span data-ttu-id="ce055-108">Đặt tên giải pháp, **\<your organization name> kích thước giá**, nhập thông tin yêu cầu còn lại, sau đó chọn **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="ce055-108">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then select **Save**.</span></span>

> ![Tạo giải pháp tùy chỉnh cho kích thước giá](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="ce055-110">Thêm tất cả các thực thể cần thiết và các thành phần liên quan vào giải pháp Thông số định giá</span><span class="sxs-lookup"><span data-stu-id="ce055-110">Add all required entities and related components to the Pricing dimension solution</span></span>
<span data-ttu-id="ce055-111">Bạn sẽ cần thêm các thực thể Project Service sau đây vào giải pháp giá của bạn.</span><span class="sxs-lookup"><span data-stu-id="ce055-111">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="ce055-112">Hoàn thành các bước trong quy trình này để thực hiện một số thay đổi sơ đồ quan trọng trong giải pháp giá để các thực thể trở thành kích thước giá mới.</span><span class="sxs-lookup"><span data-stu-id="ce055-112">Complete the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="ce055-113">Chọn **Chế độ Cài đặt** > **Giải pháp**, rồi nhấp đúp vào **\<your organization name> kích thước giá**.</span><span class="sxs-lookup"><span data-stu-id="ce055-113">Select **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="ce055-114">Trong Solution Explorer, trên ngăn điều hướng bên trái, chọn **Thêm hiện có** > **Thực thể**.</span><span class="sxs-lookup"><span data-stu-id="ce055-114">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="ce055-115">Trong hộp thoại **Thành phần giải pháp**, chọn các thực thể sau:</span><span class="sxs-lookup"><span data-stu-id="ce055-115">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="ce055-116">Thực tế</span><span class="sxs-lookup"><span data-stu-id="ce055-116">Actual</span></span>
- <span data-ttu-id="ce055-117">Nguồn lực có thể đăng ký</span><span class="sxs-lookup"><span data-stu-id="ce055-117">Bookable Resource</span></span>
- <span data-ttu-id="ce055-118">Mô tả Ước tính</span><span class="sxs-lookup"><span data-stu-id="ce055-118">Estimate Line</span></span>
- <span data-ttu-id="ce055-119">Nhiệm vụ dự án</span><span class="sxs-lookup"><span data-stu-id="ce055-119">Project Task</span></span>
- <span data-ttu-id="ce055-120">Chi tiết Mô tả Hóa đơn</span><span class="sxs-lookup"><span data-stu-id="ce055-120">Invoice Line Detail</span></span>
- <span data-ttu-id="ce055-121">Dòng nhật ký kế toán</span><span class="sxs-lookup"><span data-stu-id="ce055-121">Journal Line</span></span>
- <span data-ttu-id="ce055-122">Chi tiết Mô tả Hợp đồng Dự án</span><span class="sxs-lookup"><span data-stu-id="ce055-122">Project Contract Line Detail</span></span>
- <span data-ttu-id="ce055-123">Thành viên Nhóm Dự án</span><span class="sxs-lookup"><span data-stu-id="ce055-123">Project Team Member</span></span>
- <span data-ttu-id="ce055-124">Chi tiết Mô tả Báo giá</span><span class="sxs-lookup"><span data-stu-id="ce055-124">Quote Line Detail</span></span>
- <span data-ttu-id="ce055-125">Tăng giá theo Vai trò</span><span class="sxs-lookup"><span data-stu-id="ce055-125">Role Price Markup</span></span>
- <span data-ttu-id="ce055-126">Giá Vai trò</span><span class="sxs-lookup"><span data-stu-id="ce055-126">Role Price</span></span> 
- <span data-ttu-id="ce055-127">Mục nhập Thời gian</span><span class="sxs-lookup"><span data-stu-id="ce055-127">Time Entry</span></span> 

> ![Thêm các thực thể hiện có vào giải pháp kích thước giá](media/Existing-entities-to-PD-solution.png)

> ![Chọn thành phần giải pháp.](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="ce055-130">Đảm bảo bao gồm tất cả các biểu mẫu và dạng xem cho từng thực thể được chọn.</span><span class="sxs-lookup"><span data-stu-id="ce055-130">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="ce055-131">Khi được nhắc đưa vào tất cả các thực thể phụ thuộc cho các thực thể đã chọn, hãy chọn **Không**.</span><span class="sxs-lookup"><span data-stu-id="ce055-131">When prompted to include any dependent entities for the selected entities, select **No**.</span></span>

> ![Không bao gồm tất cả thành phần liên quan](media/Do-not-include-required.png)


