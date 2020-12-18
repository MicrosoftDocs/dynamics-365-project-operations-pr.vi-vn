---
title: Tạo thực thể và trường tùy chỉnh làm thông số định giá
description: Hoàn tất các bước sau bất kỳ lúc nào bạn muốn tạo bộ tùy chọn hoặc thực thể tùy chỉnh.
author: rumant
manager: AnnBe
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: fc5917856b8f28d36dc55593a68eba7823a00b36
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642839"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="8439f-103">Tạo thực thể và trường tùy chỉnh làm thông số định giá</span><span class="sxs-lookup"><span data-stu-id="8439f-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="8439f-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="8439f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8439f-105">Hãy làm theo các bước sau nếu bạn muốn tạo bộ tùy chọn hoặc thực thể tùy chỉnh để dùng làm thông số định giá.</span><span class="sxs-lookup"><span data-stu-id="8439f-105">Complete the following steps when you want to create a custom option set or entity for using it as a pricing dimension.</span></span> <span data-ttu-id="8439f-106">Để biết thêm thông tin, hãy xem [Tổng quan về thông số định giá](pricing-dimensions-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8439f-106">For more information, see [Pricing dimensions overview](pricing-dimensions-overview.md).</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="8439f-107">Bạn nên thực hiện tất cả thay đổi kích thước giá tùy chỉnh trong một giải pháp riêng.</span><span class="sxs-lookup"><span data-stu-id="8439f-107">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="8439f-108">Đây là phương pháp quan trọng mang đến sự linh hoạt nếu bạn cần cập nhật hoặc xóa các thay đổi trong tương lai.</span><span class="sxs-lookup"><span data-stu-id="8439f-108">This important best practice provides flexibility in the future to update or remove changes as needed.</span></span> <span data-ttu-id="8439f-109">Điều này cũng sẽ hỗ trợ việc sử dụng lại công việc của bạn, cũng như giúp bạn dễ dàng áp dụng những thay đổi này vào một phiên bản khác. Sau khi bạn đã thực hiện mọi thay đổi cần thiết, hãy xuất giải pháp này là **Giải pháp được quản lý**, sau đó nhập vào phiên bản khác để sử dụng lại cách thiết lập giá cả.</span><span class="sxs-lookup"><span data-stu-id="8439f-109">This will also help with re-use of your work and make it easier to port these changes to another instance After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="8439f-110">Tạo các trường tùy chỉnh và bộ tùy chọn trong giải pháp kích thước giá</span><span class="sxs-lookup"><span data-stu-id="8439f-110">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="8439f-111">Kích thước giá có thể là một bộ tùy chọn hoặc một thực thể.</span><span class="sxs-lookup"><span data-stu-id="8439f-111">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="8439f-112">Cả hai phải được tạo trong giải pháp giá cả của bạn.</span><span class="sxs-lookup"><span data-stu-id="8439f-112">Both must be created in your pricing solution.</span></span> <span data-ttu-id="8439f-113">Các bước trong quy trình này giải thích cách tạo kích thước dựa trên thực thể và kích thước dựa trên bộ tùy chọn.</span><span class="sxs-lookup"><span data-stu-id="8439f-113">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="8439f-114">Kích thước dựa trên thực thể</span><span class="sxs-lookup"><span data-stu-id="8439f-114">Entity-based dimensions</span></span>
<span data-ttu-id="8439f-115">Để tạo các thông số dựa trên thực thể, hãy làm theo các bước sau:</span><span class="sxs-lookup"><span data-stu-id="8439f-115">To create entity-based dimensions, follow these steps:</span></span>

1. <span data-ttu-id="8439f-116">Chọn **Chế độ Cài đặt** > **Giải pháp**, rồi nhấp đúp vào **\<your organization name> kích thước giá**.</span><span class="sxs-lookup"><span data-stu-id="8439f-116">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="8439f-117">Trong Trình khám phá giải pháp, trên ngăn điều hướng bên trái, hãy chọn **Thực thể**.</span><span class="sxs-lookup"><span data-stu-id="8439f-117">In Solution Explorer, in the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="8439f-118">Chọn **Mới** để tạo một thực thể mới gọi là **Chức vụ tiêu chuẩn**.</span><span class="sxs-lookup"><span data-stu-id="8439f-118">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="8439f-119">Nhập các thông tin cần thiết còn lại, sau đó chọn **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="8439f-119">Enter the remaining required information, and then select **Save**.</span></span>

> ![Định nghĩa thực thể chức vụ tiêu chuẩn](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a><span data-ttu-id="8439f-121">Kích thước dựa trên bộ tùy chọn</span><span class="sxs-lookup"><span data-stu-id="8439f-121">Option set-based dimensions</span></span> 
<span data-ttu-id="8439f-122">Bạn có thể tạo hai kích thước dựa trên bộ tùy chọn.</span><span class="sxs-lookup"><span data-stu-id="8439f-122">You can create two option set-based dimensions.</span></span> 

- <span data-ttu-id="8439f-123">Dùng **Vị trí làm việc của nguồn lực** để theo dõi giá của công việc có vị trí làm việc tại **Nhà** hoặc **Tại cơ sở**.</span><span class="sxs-lookup"><span data-stu-id="8439f-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work.</span></span> 
- <span data-ttu-id="8439f-124">Dùng **Giờ làm việc của nguồn lực** với giá trị là **Bình thường** và **Ngoài giờ** để áp dụng phần tăng giá khi công việc hoàn thành.</span><span class="sxs-lookup"><span data-stu-id="8439f-124">Use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when the work is complete.</span></span>

<span data-ttu-id="8439f-125">Hình sau mang đến cái nhìn tổng quan về thông số **Vị trí làm việc của nguồn lực**.</span><span class="sxs-lookup"><span data-stu-id="8439f-125">The following graphic provides a view of the **Resource Work Location** dimension.</span></span> 

> ![Kích thước giá dựa trên bộ tùy chọn gọi là Vị trí làm việc của nguồn lực](media/Option-set-PD-called-Resource-Work-Location.png)

<span data-ttu-id="8439f-127">Hình sau mang đến cái nhìn tổng quan về thông số **Giờ làm việc của nguồn lực**.</span><span class="sxs-lookup"><span data-stu-id="8439f-127">The following graphic provides a view of the **Resource Work Hours** dimension.</span></span> 

> ![Kích thước giá dựa trên bộ tùy chọn gọi là Số giờ làm việc của nguồn lực](media/Option-set-PD-called-Resource-Work-Hours.png)

1. <span data-ttu-id="8439f-129">Chọn **Chế độ Cài đặt** > **Giải pháp**, rồi nhấp đúp vào **\<your organization name> kích thước giá**.</span><span class="sxs-lookup"><span data-stu-id="8439f-129">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="8439f-130">Trong Trình khám phá giải pháp, trên ngăn điều hướng bên trái, chọn **Bộ tùy chọn**.</span><span class="sxs-lookup"><span data-stu-id="8439f-130">In Solution Explorer, in the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="8439f-131">Chọn **Mới** để tạo bộ tùy chọn mới, nhập thông tin yêu cầu còn lại, và sau đó chọn **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="8439f-131">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="8439f-132">Tạo dữ liệu cho kích thước dựa trên thực thể</span><span class="sxs-lookup"><span data-stu-id="8439f-132">Create data for entity-based dimensions</span></span>

<span data-ttu-id="8439f-133">Bạn có thể tạo dữ liệu cho kích thước dựa trên thực thể theo cách thủ công hoặc bằng cách sử dụng lệnh gọi dịch vụ hoặc nhập Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="8439f-133">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="8439f-134">Sử dụng các bước trong quy trình này để tạo hai chức vụ tiêu chuẩn là **Kỹ sư hệ thống** và **Kỹ sư hệ thống cấp cao** từ kích thước dựa trên thực thể **Chức vụ tiêu chuẩn**.</span><span class="sxs-lookup"><span data-stu-id="8439f-134">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="8439f-135">Nếu dữ liệu bạn muốn tạo nhỏ, như trong ví dụ sau đây, bạn có thể sử dụng biểu mẫu chuẩn.</span><span class="sxs-lookup"><span data-stu-id="8439f-135">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="8439f-136">Chọn **Tìm kiếm nâng cao**.</span><span class="sxs-lookup"><span data-stu-id="8439f-136">Select **Advanced Find**.</span></span>
2. <span data-ttu-id="8439f-137">Chọn thực thể **Chức vụ tiêu chuẩn**, sau đó chọn **Kết quả**.</span><span class="sxs-lookup"><span data-stu-id="8439f-137">Select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="8439f-138">Tất cả các hàng trong thực thể **Chức vụ tiêu chuẩn** sẽ hiển thị.</span><span class="sxs-lookup"><span data-stu-id="8439f-138">All of the rows in the **Standard Title** entity will be shown.</span></span>
3. <span data-ttu-id="8439f-139">Chọn **Mới**, và trong trường **Tên**, hãy nhập "Kỹ sư hệ thống" rồi chọn **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="8439f-139">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
4. <span data-ttu-id="8439f-140">Đóng trang.</span><span class="sxs-lookup"><span data-stu-id="8439f-140">Close the page.</span></span> 
5. <span data-ttu-id="8439f-141">Lặp lại bước 1-3 để tạo một chức vụ tiêu chuẩn khác cho "Kỹ sư hệ thống cao cấp".</span><span class="sxs-lookup"><span data-stu-id="8439f-141">Repeat steps 1-3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![Dữ liệu mẫu cho thực thể Chức vụ tiêu chuẩn](media/ST-data.png)
