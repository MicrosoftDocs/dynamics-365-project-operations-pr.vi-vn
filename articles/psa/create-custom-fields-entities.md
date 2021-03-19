---
title: Tạo các trường và thực thể tùy chỉnh
description: Chủ đề này giải thích cách tạo bộ tùy chọn và thực thể trong giải pháp của riêng bạn trong nền tảng Power Apps.
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
ms.openlocfilehash: c58745a46e84a40b90fbb3cbf89b10e293588fc3
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290564"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="d70f2-103">Tạo các trường và thực thể tùy chỉnh</span><span class="sxs-lookup"><span data-stu-id="d70f2-103">Create custom fields and entities</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="d70f2-104">Hoàn tất các bước sau bất kỳ lúc nào bạn muốn tạo bộ tùy chọn hoặc thực thể tùy chỉnh trên nền tảng Power Apps.</span><span class="sxs-lookup"><span data-stu-id="d70f2-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="d70f2-105">Các quy trình trong chủ đề này sẽ được hoàn thành bằng cách sử dụng giao diện web của Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="d70f2-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d70f2-106">Bạn nên thực hiện tất cả thay đổi kích thước giá tùy chỉnh trong một giải pháp riêng.</span><span class="sxs-lookup"><span data-stu-id="d70f2-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="d70f2-107">Cách làm quan trọng này sẽ giúp bạn có thể thoải mái cập nhật hay loại bỏ các thay đổi khi cần, giúp sử dụng lại công việc và dễ chuyển các thay đổ này sang phiên bản khác.</span><span class="sxs-lookup"><span data-stu-id="d70f2-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="d70f2-108">Sau khi bạn thực hiện tất cả các thay đổi cần thiết, hãy xuất giải pháp này dưới dạng **Giải pháp được quản lý** và nhập nó vào các phiên bản khác để tái sử dụng thiết lập giá của bạn.</span><span class="sxs-lookup"><span data-stu-id="d70f2-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="d70f2-109">Tạo các trường tùy chỉnh và bộ tùy chọn trong giải pháp kích thước giá</span><span class="sxs-lookup"><span data-stu-id="d70f2-109">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="d70f2-110">Kích thước giá có thể là một bộ tùy chọn hoặc một thực thể.</span><span class="sxs-lookup"><span data-stu-id="d70f2-110">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="d70f2-111">Cả hai phải được tạo trong giải pháp giá cả của bạn.</span><span class="sxs-lookup"><span data-stu-id="d70f2-111">Both must be created in your pricing solution.</span></span> <span data-ttu-id="d70f2-112">Các bước trong quy trình này giải thích cách tạo kích thước dựa trên thực thể và kích thước dựa trên bộ tùy chọn.</span><span class="sxs-lookup"><span data-stu-id="d70f2-112">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="d70f2-113">Kích thước dựa trên thực thể</span><span class="sxs-lookup"><span data-stu-id="d70f2-113">Entity-based dimensions</span></span>

1. <span data-ttu-id="d70f2-114">Trong PSA, nhấp vào **Cài đặt** > **Giải pháp**, rồi nhấp đúp vào **\<your organization name> thông số định giá**.</span><span class="sxs-lookup"><span data-stu-id="d70f2-114">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="d70f2-115">Trong Solution Explorer, trên ngăn điều hướng bên trái, chọn **Thực thể**.</span><span class="sxs-lookup"><span data-stu-id="d70f2-115">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="d70f2-116">Nhấp vào **Mới** để tạo một thực thể mới gọi là **Chức vụ tiêu chuẩn**.</span><span class="sxs-lookup"><span data-stu-id="d70f2-116">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="d70f2-117">Nhập các thông tin cần thiết còn lại, sau đó nhấp vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="d70f2-117">Enter the remaining required information, and then click **Save**.</span></span>

> ![Định nghĩa thực thể chức vụ tiêu chuẩn](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="d70f2-119">Kích thước dựa trên bộ tùy chọn</span><span class="sxs-lookup"><span data-stu-id="d70f2-119">Option set-based dimensions</span></span> 
<span data-ttu-id="d70f2-120">Bạn có thể tạo hai kích thước dựa trên bộ tùy chọn.</span><span class="sxs-lookup"><span data-stu-id="d70f2-120">You can create two option set-based dimensions.</span></span> <span data-ttu-id="d70f2-121">Sử dụng **Vị trí làm việc của nguồn lực** để theo dõi giá của công việc ở vị trí **Nhà** và công việc **Tại chỗ**, cũng như sử dụng **Số giờ làm việc của nguồn lực** với các giá trị **Giờ làm việc** và **Ngoài giờ** để áp dụng đánh dấu khi công việc hoàn tất.</span><span class="sxs-lookup"><span data-stu-id="d70f2-121">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="d70f2-122">Trong PSA, nhấp vào **Cài đặt** > **Giải pháp**, rồi nhấp đúp vào **\<your organization name> thông số định giá**.</span><span class="sxs-lookup"><span data-stu-id="d70f2-122">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="d70f2-123">Trong Solution Explorer, trên ngăn điều hướng bên trái, chọn **Bộ tùy chọn**.</span><span class="sxs-lookup"><span data-stu-id="d70f2-123">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="d70f2-124">Nhấp vào **Mới** để tạo bộ tùy chọn mới, nhập thông tin yêu cầu còn lại, và sau đó nhấp vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="d70f2-124">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="d70f2-125">Kích thước giá dựa trên bộ tùy chọn gọi là Vị trí làm việc của nguồn lực</span><span class="sxs-lookup"><span data-stu-id="d70f2-125">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="d70f2-126">Kích thước giá dựa trên bộ tùy chọn gọi là Số giờ làm việc của nguồn lực</span><span class="sxs-lookup"><span data-stu-id="d70f2-126">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="d70f2-127">Tạo dữ liệu cho kích thước dựa trên thực thể</span><span class="sxs-lookup"><span data-stu-id="d70f2-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="d70f2-128">Bạn có thể tạo dữ liệu cho kích thước dựa trên thực thể theo cách thủ công hoặc bằng cách sử dụng lệnh gọi dịch vụ hoặc nhập Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="d70f2-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="d70f2-129">Sử dụng các bước trong quy trình này để tạo hai chức vụ tiêu chuẩn là **Kỹ sư hệ thống** và **Kỹ sư hệ thống cấp cao** từ kích thước dựa trên thực thể **Chức vụ tiêu chuẩn**.</span><span class="sxs-lookup"><span data-stu-id="d70f2-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="d70f2-130">Nếu dữ liệu bạn muốn tạo nhỏ, như trong ví dụ sau đây, bạn có thể sử dụng biểu mẫu chuẩn.</span><span class="sxs-lookup"><span data-stu-id="d70f2-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="d70f2-131">Trong PSA, nhấp vào **Tìm kiếm nâng cao**.</span><span class="sxs-lookup"><span data-stu-id="d70f2-131">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="d70f2-132">Chọn thực thể **Chức vụ tiêu chuẩn**, sau đó nhấp vào **Kết quả**.</span><span class="sxs-lookup"><span data-stu-id="d70f2-132">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="d70f2-133">Tất cả các hàng trong thực thể **Chức vụ tiêu chuẩn** sẽ hiển thị.</span><span class="sxs-lookup"><span data-stu-id="d70f2-133">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="d70f2-134">Bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="d70f2-134">Click **New**.</span></span> <span data-ttu-id="d70f2-135">Trong trường **Tên**, nhập "Kỹ sư hệ thống", sau đó nhấp vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="d70f2-135">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="d70f2-136">Đóng biểu mẫu.</span><span class="sxs-lookup"><span data-stu-id="d70f2-136">Close the form.</span></span> 
4. <span data-ttu-id="d70f2-137">Lặp lại bước 1-3 để tạo một chức vụ tiêu chuẩn khác cho "Kỹ sư hệ thống cao cấp".</span><span class="sxs-lookup"><span data-stu-id="d70f2-137">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="d70f2-138">Dữ liệu mẫu cho thực thể chức vụ tiêu chuẩn</span><span class="sxs-lookup"><span data-stu-id="d70f2-138">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]