---
title: Tạo thực thể và trường tùy chỉnh làm thông số định giá
description: Hoàn tất các bước sau bất kỳ lúc nào bạn muốn tạo bộ tùy chọn hoặc thực thể tùy chỉnh.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 2000f7e710267560fe2bd52b0e33024617d108ea
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898287"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="de0c8-103">Tạo thực thể và trường tùy chỉnh làm thông số định giá</span><span class="sxs-lookup"><span data-stu-id="de0c8-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="de0c8-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="de0c8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="de0c8-105">Hoàn tất các bước sau bất kỳ lúc nào bạn muốn tạo bộ tùy chọn hoặc thực thể tùy chỉnh.</span><span class="sxs-lookup"><span data-stu-id="de0c8-105">Complete the following steps any time that you want to create a custom option set or entity.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="de0c8-106">Bạn nên thực hiện tất cả thay đổi kích thước giá tùy chỉnh trong một giải pháp riêng.</span><span class="sxs-lookup"><span data-stu-id="de0c8-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="de0c8-107">Cách làm quan trọng này sẽ giúp bạn có thể thoải mái cập nhật hay loại bỏ các thay đổi khi cần, giúp sử dụng lại công việc và dễ chuyển các thay đổ này sang phiên bản khác.</span><span class="sxs-lookup"><span data-stu-id="de0c8-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="de0c8-108">Sau khi bạn thực hiện tất cả các thay đổi cần thiết, hãy xuất giải pháp này dưới dạng **Giải pháp được quản lý** và nhập nó vào các phiên bản khác để tái sử dụng thiết lập giá của bạn.</span><span class="sxs-lookup"><span data-stu-id="de0c8-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="de0c8-109">Tạo giải pháp tùy chỉnh cho kích thước giá</span><span class="sxs-lookup"><span data-stu-id="de0c8-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="de0c8-110">Chuyển đến **Chế độ cài đặt** > **Giải pháp**, rồi chọn **Mới** để tạo một giải pháp mới.</span><span class="sxs-lookup"><span data-stu-id="de0c8-110">Go to **Settings** > **Solutions**, and then select **New** to create a new solution.</span></span> 
2. <span data-ttu-id="de0c8-111">Đặt tên giải pháp, **\<your organization name> kích thước giá**, nhập thông tin yêu cầu còn lại, sau đó chọn **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="de0c8-111">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then select **Save**.</span></span>
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="de0c8-112">Tạo các trường tùy chỉnh và bộ tùy chọn trong giải pháp kích thước giá</span><span class="sxs-lookup"><span data-stu-id="de0c8-112">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="de0c8-113">Kích thước giá có thể là một bộ tùy chọn hoặc một thực thể.</span><span class="sxs-lookup"><span data-stu-id="de0c8-113">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="de0c8-114">Cả hai phải được tạo trong giải pháp giá cả của bạn.</span><span class="sxs-lookup"><span data-stu-id="de0c8-114">Both must be created in your pricing solution.</span></span> <span data-ttu-id="de0c8-115">Các bước trong quy trình này giải thích cách tạo kích thước dựa trên thực thể và kích thước dựa trên bộ tùy chọn.</span><span class="sxs-lookup"><span data-stu-id="de0c8-115">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="de0c8-116">Kích thước dựa trên thực thể</span><span class="sxs-lookup"><span data-stu-id="de0c8-116">Entity-based dimensions</span></span>

1. <span data-ttu-id="de0c8-117">Chọn **Chế độ Cài đặt** > **Giải pháp**, rồi nhấp đúp vào **\<your organization name> kích thước giá**.</span><span class="sxs-lookup"><span data-stu-id="de0c8-117">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="de0c8-118">Trong Solution Explorer, trên ngăn điều hướng bên trái, chọn **Thực thể**.</span><span class="sxs-lookup"><span data-stu-id="de0c8-118">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="de0c8-119">Chọn **Mới** để tạo một thực thể mới gọi là **Chức vụ tiêu chuẩn**.</span><span class="sxs-lookup"><span data-stu-id="de0c8-119">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="de0c8-120">Nhập các thông tin cần thiết còn lại, sau đó chọn **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="de0c8-120">Enter the remaining required information, and then select **Save**.</span></span>


### <a name="option-set-based-dimensions"></a><span data-ttu-id="de0c8-121">Kích thước dựa trên bộ tùy chọn</span><span class="sxs-lookup"><span data-stu-id="de0c8-121">Option set-based dimensions</span></span> 
<span data-ttu-id="de0c8-122">Bạn có thể tạo hai kích thước dựa trên bộ tùy chọn.</span><span class="sxs-lookup"><span data-stu-id="de0c8-122">You can create two option set-based dimensions.</span></span> <span data-ttu-id="de0c8-123">Sử dụng **Vị trí làm việc của nguồn lực** để theo dõi giá của công việc ở vị trí **Nhà** và công việc **Tại chỗ**, cũng như sử dụng **Số giờ làm việc của nguồn lực** với các giá trị **Giờ làm việc** và **Ngoài giờ** để áp dụng đánh dấu khi công việc hoàn tất.</span><span class="sxs-lookup"><span data-stu-id="de0c8-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="de0c8-124">Chọn **Chế độ Cài đặt** > **Giải pháp**, rồi nhấp đúp vào **\<your organization name> kích thước giá**.</span><span class="sxs-lookup"><span data-stu-id="de0c8-124">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="de0c8-125">Trong Solution Explorer, trên ngăn điều hướng bên trái, chọn **Bộ tùy chọn**.</span><span class="sxs-lookup"><span data-stu-id="de0c8-125">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="de0c8-126">Chọn **Mới** để tạo bộ tùy chọn mới, nhập thông tin yêu cầu còn lại, và sau đó chọn **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="de0c8-126">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="de0c8-127">Tạo dữ liệu cho kích thước dựa trên thực thể</span><span class="sxs-lookup"><span data-stu-id="de0c8-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="de0c8-128">Bạn có thể tạo dữ liệu cho kích thước dựa trên thực thể theo cách thủ công hoặc bằng cách sử dụng lệnh gọi dịch vụ hoặc nhập Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="de0c8-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="de0c8-129">Sử dụng các bước trong quy trình này để tạo hai chức vụ tiêu chuẩn là **Kỹ sư hệ thống** và **Kỹ sư hệ thống cấp cao** từ kích thước dựa trên thực thể **Chức vụ tiêu chuẩn**.</span><span class="sxs-lookup"><span data-stu-id="de0c8-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="de0c8-130">Nếu dữ liệu bạn muốn tạo nhỏ, như trong ví dụ sau đây, bạn có thể sử dụng biểu mẫu chuẩn.</span><span class="sxs-lookup"><span data-stu-id="de0c8-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="de0c8-131">Chọn **Tìm nâng cao**, chọn thực thể **Chức vụ tiêu chuẩn**, rồi chọn **Kết quả**.</span><span class="sxs-lookup"><span data-stu-id="de0c8-131">Select **Advanced Find**, select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="de0c8-132">Tất cả các hàng trong thực thể **Chức vụ tiêu chuẩn** sẽ hiển thị.</span><span class="sxs-lookup"><span data-stu-id="de0c8-132">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="de0c8-133">Chọn **Mới**, và trong trường **Tên**, hãy nhập "Kỹ sư hệ thống" rồi chọn **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="de0c8-133">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
3. <span data-ttu-id="de0c8-134">Đóng biểu mẫu.</span><span class="sxs-lookup"><span data-stu-id="de0c8-134">Close the form.</span></span> 
4. <span data-ttu-id="de0c8-135">Lặp lại bước 1-3 để tạo một chức vụ tiêu chuẩn khác cho "Kỹ sư hệ thống cao cấp".</span><span class="sxs-lookup"><span data-stu-id="de0c8-135">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="de0c8-136">Thêm tất cả các thực thể yêu cầu và các thành phần liên quan đến Giải pháp kích thước giá</span><span class="sxs-lookup"><span data-stu-id="de0c8-136">Add all required entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="de0c8-137">Bạn sẽ cần thêm các thực thể sau đây vào giải pháp giá của bạn.</span><span class="sxs-lookup"><span data-stu-id="de0c8-137">You will need to add the following entities to your pricing solution.</span></span> <span data-ttu-id="de0c8-138">Sử dụng các bước trong quy trình này để thực hiện một số thay đổi sơ đồ quan trọng trong giải pháp giá để các thực thể trở thành kích thước giá mới.</span><span class="sxs-lookup"><span data-stu-id="de0c8-138">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="de0c8-139">Chọn **Chế độ Cài đặt** > **Giải pháp**, rồi nhấp đúp vào **\<your organization name> kích thước giá**.</span><span class="sxs-lookup"><span data-stu-id="de0c8-139">Select **Settings** > **Solutions**, and double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="de0c8-140">Trong Solution Explorer, trên ngăn điều hướng bên trái, chọn **Thêm hiện có** > **Thực thể**.</span><span class="sxs-lookup"><span data-stu-id="de0c8-140">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="de0c8-141">Trong hộp thoại **Thành phần giải pháp**, chọn các thực thể sau:</span><span class="sxs-lookup"><span data-stu-id="de0c8-141">In the **Solution Components** dialog box, select the following entities:</span></span>

  - <span data-ttu-id="de0c8-142">Thực tế</span><span class="sxs-lookup"><span data-stu-id="de0c8-142">Actual</span></span>
  - <span data-ttu-id="de0c8-143">Nguồn lực có thể đặt trước</span><span class="sxs-lookup"><span data-stu-id="de0c8-143">Bookable Resource</span></span>
  - <span data-ttu-id="de0c8-144">Mô tả Ước tính</span><span class="sxs-lookup"><span data-stu-id="de0c8-144">Estimate Line</span></span>
  - <span data-ttu-id="de0c8-145">Chi tiết Mô tả Hóa đơn</span><span class="sxs-lookup"><span data-stu-id="de0c8-145">Invoice Line Detail</span></span>
  - <span data-ttu-id="de0c8-146">Dòng Nhật ký Kế toán</span><span class="sxs-lookup"><span data-stu-id="de0c8-146">Journal Line</span></span>
  - <span data-ttu-id="de0c8-147">Chi tiết Mô tả Hợp đồng Dự án</span><span class="sxs-lookup"><span data-stu-id="de0c8-147">Project Contract Line Detail</span></span>
  - <span data-ttu-id="de0c8-148">Thành viên Nhóm Dự án</span><span class="sxs-lookup"><span data-stu-id="de0c8-148">Project Team Member</span></span>
  - <span data-ttu-id="de0c8-149">Chi tiết Mô tả Báo giá</span><span class="sxs-lookup"><span data-stu-id="de0c8-149">Quote Line Detail</span></span>
  - <span data-ttu-id="de0c8-150">Tăng giá theo Vai trò</span><span class="sxs-lookup"><span data-stu-id="de0c8-150">Role Price Markup</span></span>
  - <span data-ttu-id="de0c8-151">Giá Vai trò</span><span class="sxs-lookup"><span data-stu-id="de0c8-151">Role Price</span></span> 
  - <span data-ttu-id="de0c8-152">Mục nhập Thời gian</span><span class="sxs-lookup"><span data-stu-id="de0c8-152">Time Entry</span></span> 


> [!NOTE]
> <span data-ttu-id="de0c8-153">Đảm bảo bao gồm tất cả các biểu mẫu và dạng xem cho từng thực thể được chọn.</span><span class="sxs-lookup"><span data-stu-id="de0c8-153">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="de0c8-154">Khi được nhắc đưa vào bất kỳ thực thể phụ thuộc nào cho các thực thể đã chọn ở trên, hãy chọn **Không**.</span><span class="sxs-lookup"><span data-stu-id="de0c8-154">When prompted to include any dependent entities for the entities selected above, select **No**.</span></span>
