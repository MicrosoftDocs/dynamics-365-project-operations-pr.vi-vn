---
title: Tạo các trường và thực thể tùy chỉnh
description: Chủ đề này giải thích cách tạo bộ tùy chọn và thực thể trong giải pháp của riêng bạn trong nền tảng Power Apps.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 03/24/2020
ms.locfileid: "3757121"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="c5118-103">Tạo các trường và thực thể tùy chỉnh</span><span class="sxs-lookup"><span data-stu-id="c5118-103">Create custom fields and entities</span></span> 

<span data-ttu-id="c5118-104">Hoàn tất các bước sau bất kỳ lúc nào bạn muốn tạo bộ tùy chọn hoặc thực thể tùy chỉnh trên nền tảng Power Apps.</span><span class="sxs-lookup"><span data-stu-id="c5118-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="c5118-105">Các quy trình trong chủ đề này sẽ được hoàn thành bằng cách sử dụng giao diện web của Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="c5118-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c5118-106">Bạn nên thực hiện tất cả thay đổi kích thước giá tùy chỉnh trong một giải pháp riêng.</span><span class="sxs-lookup"><span data-stu-id="c5118-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="c5118-107">Cách làm quan trọng này sẽ giúp bạn có thể thoải mái cập nhật hay loại bỏ các thay đổi khi cần, giúp sử dụng lại công việc và dễ chuyển các thay đổ này sang phiên bản khác.</span><span class="sxs-lookup"><span data-stu-id="c5118-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="c5118-108">Sau khi bạn thực hiện tất cả các thay đổi cần thiết, hãy xuất giải pháp này dưới dạng **Giải pháp được quản lý** và nhập nó vào các phiên bản khác để tái sử dụng thiết lập giá của bạn.</span><span class="sxs-lookup"><span data-stu-id="c5118-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="c5118-109">Tạo giải pháp tùy chỉnh cho kích thước giá</span><span class="sxs-lookup"><span data-stu-id="c5118-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="c5118-110">Trong PSA, nhấp vào **Thiết đặt** > **Giải pháp**, sau đó nhấp vào **Mới** để tạo một giải pháp mới.</span><span class="sxs-lookup"><span data-stu-id="c5118-110">In PSA, click **Settings** > **Solutions**, and then click **New** to create a new solution.</span></span> 
2. <span data-ttu-id="c5118-111">Đặt tên giải pháp, **\<tên tổ chức của bạn> kích thước giá**, nhập thông tin yêu cầu còn lại, sau đó nhấp vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="c5118-111">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then click **Save**.</span></span>

> ![Tạo giải pháp tùy chỉnh cho kích thước giá](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="c5118-113">Tạo các trường tùy chỉnh và bộ tùy chọn trong giải pháp kích thước giá</span><span class="sxs-lookup"><span data-stu-id="c5118-113">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="c5118-114">Kích thước giá có thể là một bộ tùy chọn hoặc một thực thể.</span><span class="sxs-lookup"><span data-stu-id="c5118-114">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="c5118-115">Cả hai phải được tạo trong giải pháp giá cả của bạn.</span><span class="sxs-lookup"><span data-stu-id="c5118-115">Both must be created in your pricing solution.</span></span> <span data-ttu-id="c5118-116">Các bước trong quy trình này giải thích cách tạo kích thước dựa trên thực thể và kích thước dựa trên bộ tùy chọn.</span><span class="sxs-lookup"><span data-stu-id="c5118-116">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="c5118-117">Kích thước dựa trên thực thể</span><span class="sxs-lookup"><span data-stu-id="c5118-117">Entity-based dimensions</span></span>

1. <span data-ttu-id="c5118-118">Trong PSA, nhấp vào **Cài đặt** > **Giải pháp**, sau đó nhấp đúp vào **\<tên tổ chức > kích thước giá**.</span><span class="sxs-lookup"><span data-stu-id="c5118-118">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="c5118-119">Trong Solution Explorer, trên ngăn điều hướng bên trái, chọn **Thực thể**.</span><span class="sxs-lookup"><span data-stu-id="c5118-119">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="c5118-120">Nhấp vào **Mới** để tạo một thực thể mới gọi là **Chức vụ tiêu chuẩn**.</span><span class="sxs-lookup"><span data-stu-id="c5118-120">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="c5118-121">Nhập các thông tin cần thiết còn lại, sau đó nhấp vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="c5118-121">Enter the remaining required information, and then click **Save**.</span></span>

> ![Định nghĩa thực thể chức vụ tiêu chuẩn](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="c5118-123">Kích thước dựa trên bộ tùy chọn</span><span class="sxs-lookup"><span data-stu-id="c5118-123">Option set-based dimensions</span></span> 
<span data-ttu-id="c5118-124">Bạn có thể tạo hai kích thước dựa trên bộ tùy chọn.</span><span class="sxs-lookup"><span data-stu-id="c5118-124">You can create two option set-based dimensions.</span></span> <span data-ttu-id="c5118-125">Sử dụng **Vị trí làm việc của nguồn lực** để theo dõi giá của công việc ở vị trí **Nhà** và công việc **Tại chỗ**, cũng như sử dụng **Số giờ làm việc của nguồn lực** với các giá trị **Giờ làm việc** và **Ngoài giờ** để áp dụng đánh dấu khi công việc hoàn tất.</span><span class="sxs-lookup"><span data-stu-id="c5118-125">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="c5118-126">Trong PSA, nhấp vào **Cài đặt** > **Giải pháp**, sau đó nhấp đúp vào **\<tên tổ chức > kích thước giá**.</span><span class="sxs-lookup"><span data-stu-id="c5118-126">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="c5118-127">Trong Solution Explorer, trên ngăn điều hướng bên trái, chọn **Bộ tùy chọn**.</span><span class="sxs-lookup"><span data-stu-id="c5118-127">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="c5118-128">Nhấp vào **Mới** để tạo bộ tùy chọn mới, nhập thông tin yêu cầu còn lại, và sau đó nhấp vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="c5118-128">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="c5118-129">Kích thước giá dựa trên bộ tùy chọn gọi là Vị trí làm việc của nguồn lực</span><span class="sxs-lookup"><span data-stu-id="c5118-129">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="c5118-130">Kích thước giá dựa trên bộ tùy chọn gọi là Số giờ làm việc của nguồn lực</span><span class="sxs-lookup"><span data-stu-id="c5118-130">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="c5118-131">Tạo dữ liệu cho kích thước dựa trên thực thể</span><span class="sxs-lookup"><span data-stu-id="c5118-131">Create data for entity-based dimensions</span></span>

<span data-ttu-id="c5118-132">Bạn có thể tạo dữ liệu cho kích thước dựa trên thực thể theo cách thủ công hoặc bằng cách sử dụng lệnh gọi dịch vụ hoặc nhập Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="c5118-132">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="c5118-133">Sử dụng các bước trong quy trình này để tạo hai chức vụ tiêu chuẩn là **Kỹ sư hệ thống** và **Kỹ sư hệ thống cấp cao** từ kích thước dựa trên thực thể **Chức vụ tiêu chuẩn**.</span><span class="sxs-lookup"><span data-stu-id="c5118-133">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="c5118-134">Nếu dữ liệu bạn muốn tạo nhỏ, như trong ví dụ sau đây, bạn có thể sử dụng biểu mẫu chuẩn.</span><span class="sxs-lookup"><span data-stu-id="c5118-134">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="c5118-135">Trong PSA, nhấp vào **Tìm kiếm nâng cao**.</span><span class="sxs-lookup"><span data-stu-id="c5118-135">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="c5118-136">Chọn thực thể **Chức vụ tiêu chuẩn**, sau đó nhấp vào **Kết quả**.</span><span class="sxs-lookup"><span data-stu-id="c5118-136">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="c5118-137">Tất cả các hàng trong thực thể **Chức vụ tiêu chuẩn** sẽ hiển thị.</span><span class="sxs-lookup"><span data-stu-id="c5118-137">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="c5118-138">Bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="c5118-138">Click **New**.</span></span> <span data-ttu-id="c5118-139">Trong trường **Tên**, nhập "Kỹ sư hệ thống", sau đó nhấp vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="c5118-139">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="c5118-140">Đóng biểu mẫu.</span><span class="sxs-lookup"><span data-stu-id="c5118-140">Close the form.</span></span> 
4. <span data-ttu-id="c5118-141">Lặp lại bước 1-3 để tạo một chức vụ tiêu chuẩn khác cho "Kỹ sư hệ thống cao cấp".</span><span class="sxs-lookup"><span data-stu-id="c5118-141">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="c5118-142">Dữ liệu mẫu cho thực thể chức vụ tiêu chuẩn</span><span class="sxs-lookup"><span data-stu-id="c5118-142">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="c5118-143">Thêm tất cả các thực thể PSA yêu cầu và các thành phần liên quan đến giải pháp kích thước giá</span><span class="sxs-lookup"><span data-stu-id="c5118-143">Add all required PSA entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="c5118-144">Bạn sẽ cần thêm các thực thể Project Service sau đây vào giải pháp giá của bạn.</span><span class="sxs-lookup"><span data-stu-id="c5118-144">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="c5118-145">Sử dụng các bước trong quy trình này để thực hiện một số thay đổi sơ đồ quan trọng trong giải pháp giá để các thực thể trở thành kích thước giá mới.</span><span class="sxs-lookup"><span data-stu-id="c5118-145">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="c5118-146">Trong PSA, nhấp vào **Cài đặt** > **Giải pháp**, sau đó nhấp đúp vào **\<tên tổ chức > kích thước giá**.</span><span class="sxs-lookup"><span data-stu-id="c5118-146">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="c5118-147">Trong Solution Explorer, trên ngăn điều hướng bên trái, chọn **Thêm hiện có** > **Thực thể**.</span><span class="sxs-lookup"><span data-stu-id="c5118-147">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="c5118-148">Trong hộp thoại **Thành phần giải pháp**, chọn các thực thể sau:</span><span class="sxs-lookup"><span data-stu-id="c5118-148">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="c5118-149">Thực tế</span><span class="sxs-lookup"><span data-stu-id="c5118-149">Actual</span></span>
- <span data-ttu-id="c5118-150">Nguồn lực có thể đặt trước</span><span class="sxs-lookup"><span data-stu-id="c5118-150">Bookable Resource</span></span>
- <span data-ttu-id="c5118-151">Mô tả Ước tính</span><span class="sxs-lookup"><span data-stu-id="c5118-151">Estimate Line</span></span>
- <span data-ttu-id="c5118-152">Chi tiết Mô tả Hóa đơn</span><span class="sxs-lookup"><span data-stu-id="c5118-152">Invoice Line Detail</span></span>
- <span data-ttu-id="c5118-153">Dòng Nhật ký Kế toán</span><span class="sxs-lookup"><span data-stu-id="c5118-153">Journal Line</span></span>
- <span data-ttu-id="c5118-154">Chi tiết Mô tả Hợp đồng Dự án</span><span class="sxs-lookup"><span data-stu-id="c5118-154">Project Contract Line Detail</span></span>
- <span data-ttu-id="c5118-155">Thành viên Nhóm Dự án</span><span class="sxs-lookup"><span data-stu-id="c5118-155">Project Team Member</span></span>
- <span data-ttu-id="c5118-156">Chi tiết Mô tả Báo giá</span><span class="sxs-lookup"><span data-stu-id="c5118-156">Quote Line Detail</span></span>
- <span data-ttu-id="c5118-157">Tăng giá theo Vai trò</span><span class="sxs-lookup"><span data-stu-id="c5118-157">Role Price Markup</span></span>
- <span data-ttu-id="c5118-158">Giá Vai trò</span><span class="sxs-lookup"><span data-stu-id="c5118-158">Role Price</span></span> 
- <span data-ttu-id="c5118-159">Mục nhập Thời gian</span><span class="sxs-lookup"><span data-stu-id="c5118-159">Time Entry</span></span> 

> ![Thêm các thực thể hiện có vào giải pháp kích thước giá](media/Existing-entities-to-PD-solution.png)

> ![Chọn thành phần giải pháp.](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="c5118-162">Đảm bảo bao gồm tất cả các biểu mẫu và dạng xem cho từng thực thể được chọn.</span><span class="sxs-lookup"><span data-stu-id="c5118-162">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="c5118-163">Khi được nhắc đưa vào bất kỳ thực thể phụ thuộc nào cho các thực thể đã chọn ở trên, nhấp vào **Không**.</span><span class="sxs-lookup"><span data-stu-id="c5118-163">When prompted to include any dependent entities for the entities selected above, click **No**.</span></span>

> ![Không bao gồm tất cả thành phần liên quan](media/Do-not-include-required.png)


