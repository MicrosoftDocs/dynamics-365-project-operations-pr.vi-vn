---
title: Đặt cấu hình Project Service Automation
description: Các bước đặt cấu hình Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: fd02611b5b3133e097b2818a725b6c5d667e5ac0
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087217"
---
# <a name="configure-project-service"></a><span data-ttu-id="d712d-103">Đặt cấu hình Project Service</span><span class="sxs-lookup"><span data-stu-id="d712d-103">Configure Project Service</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="d712d-104">Trước khi bạn có thể sử dụng chức năng [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] trong [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] để quản lý khách hàng, dự án và nguồn lực, bạn cần hoàn tất một vài bước cấu hình để đảm bảo rằng giải pháp [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] phù hợp với nhu cầu tổ chức của bạn.</span><span class="sxs-lookup"><span data-stu-id="d712d-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="d712d-105">Các bước này bao gồm:</span><span class="sxs-lookup"><span data-stu-id="d712d-105">These steps include:</span></span>  
  
-   <span data-ttu-id="d712d-106">[Thiết lập đơn vị thời gian](../psa/set-up-time-units.md).</span><span class="sxs-lookup"><span data-stu-id="d712d-106">[Set up time units](../psa/set-up-time-units.md).</span></span> <span data-ttu-id="d712d-107">Cấu hình đơn vị thời gian trong danh mục sản phẩm mà bạn sẽ sử dụng làm cơ sở lên lịch và thanh toán dự án của bạn.</span><span class="sxs-lookup"><span data-stu-id="d712d-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="d712d-108">[Thiết lập đơn vị tiền tệ và tỷ giá hối đoái](../psa/set-up-currencies-exchange-rates.md).</span><span class="sxs-lookup"><span data-stu-id="d712d-108">[Set up currencies and exchange rates](../psa/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="d712d-109">Thiết lập đơn vị tiền tệ sẽ sử dụng cho dự án của bạn.</span><span class="sxs-lookup"><span data-stu-id="d712d-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="d712d-110">[Tạo đơn vị tổ chức](../psa/create-organizational-units.md).</span><span class="sxs-lookup"><span data-stu-id="d712d-110">[Create organizational units](../psa/create-organizational-units.md).</span></span> <span data-ttu-id="d712d-111">Thiết lập các nhóm mà công ty của bạn sẽ sử dụng để phân chia hoạt động kinh doanh, theo địa lý, chức năng kinh doanh hoặc bộ phận logic khác.</span><span class="sxs-lookup"><span data-stu-id="d712d-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="d712d-112">[Thiết lập tần suất hóa đơn](../psa/set-up-invoice-frequencies.md).</span><span class="sxs-lookup"><span data-stu-id="d712d-112">[Set up invoice frequencies](../psa/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="d712d-113">Thiết lập khoảng thời gian mà bạn muốn sử dụng để lập hóa đơn khách hàng của bạn.</span><span class="sxs-lookup"><span data-stu-id="d712d-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="d712d-114">[Đặt cấu hình danh mục giao dịch](../psa/configure-transaction-categories.md).</span><span class="sxs-lookup"><span data-stu-id="d712d-114">[Configure transaction categories](../psa/configure-transaction-categories.md).</span></span> <span data-ttu-id="d712d-115">Thiết lập thể loại giao dịch mà tư vấn viên có thể tính chi phí có thể lập hóa đơn và không thể lập hóa đơn.</span><span class="sxs-lookup"><span data-stu-id="d712d-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="d712d-116">[Đặt cấu hình danh mục chi phí](../psa/configure-expense-categories.md).</span><span class="sxs-lookup"><span data-stu-id="d712d-116">[Configure expense categories](../psa/configure-expense-categories.md).</span></span> <span data-ttu-id="d712d-117">Thiết lập thể loại mà tư vấn viên có thể tính chi phí có thể lập hóa đơn và không thể lập hóa đơn.</span><span class="sxs-lookup"><span data-stu-id="d712d-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="d712d-118">[Tạo các mục danh mục sản phẩm](../psa/create-product-catalog-items.md).</span><span class="sxs-lookup"><span data-stu-id="d712d-118">[Create product catalog items](../psa/create-product-catalog-items.md).</span></span> <span data-ttu-id="d712d-119">Thêm các sản phẩm bạn bán, chẳng hạn như giấy phép phần mềm, vào danh mục sản phẩm.</span><span class="sxs-lookup"><span data-stu-id="d712d-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="d712d-120">[Tạo danh sách giá](../psa/create-price-list.md).</span><span class="sxs-lookup"><span data-stu-id="d712d-120">[Create a price list](../psa/create-price-list.md).</span></span> <span data-ttu-id="d712d-121">Cấu hình bảng giá khác nhau, tùy thuộc vào số tiền bạn muốn tính cho khách hàng cho mỗi vai trò mà dự án của họ yêu cầu.</span><span class="sxs-lookup"><span data-stu-id="d712d-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="d712d-122">[Thiết lập nguồn lực](../psa/set-up-resources.md).</span><span class="sxs-lookup"><span data-stu-id="d712d-122">[Set up resources](../psa/set-up-resources.md).</span></span> <span data-ttu-id="d712d-123">Thêm kỹ năng, thành thạo, vai trò nguồn lực và các thông tin nguồn lực khác mà bạn cần cho dự án.</span><span class="sxs-lookup"><span data-stu-id="d712d-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="d712d-124">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="d712d-124">See Also</span></span>  
 <span data-ttu-id="d712d-125">[Tổng quan về Project Service Automation](../psa/overview.md) </span><span class="sxs-lookup"><span data-stu-id="d712d-125">[Overview of Project Service Automation](../psa/overview.md) </span></span>  
 <span data-ttu-id="d712d-126">[Đặt cấu hình Project Service Automation](../psa/configure.md) </span><span class="sxs-lookup"><span data-stu-id="d712d-126">[Configure Project Service Automation](../psa/configure.md) </span></span>  
 <span data-ttu-id="d712d-127">[Hướng dẫn của Quản lý Khách hàng](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="d712d-127">[Account Manager Guide](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="d712d-128">[Hướng dẫn của Quản lý Dự án](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="d712d-128">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 <span data-ttu-id="d712d-129">[Hướng dẫn của Quản lý Nguồn lực](../psa/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="d712d-129">[Resource Manager Guide](../psa/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="d712d-130">Hướng dẫn về Thời gian, Chi phí và Cộng tác</span><span class="sxs-lookup"><span data-stu-id="d712d-130">Time, Expense, and Collaboration Guid</span></span>](../psa/time-expense-collaboration-guide.md)
