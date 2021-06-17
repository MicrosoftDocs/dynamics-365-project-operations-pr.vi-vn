---
title: Đặt cấu hình danh mục dự án
description: Chủ đề này cung cấp thông tin về cách thiết lập danh mục dự án.
author: sigitac
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d82302f12ba75a92f2de0e9746ad7e61ce0cdc6b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995197"
---
# <a name="configure-project-categories"></a><span data-ttu-id="1900f-103">Đặt cấu hình danh mục dự án</span><span class="sxs-lookup"><span data-stu-id="1900f-103">Configure project categories</span></span>

<span data-ttu-id="1900f-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_</span><span class="sxs-lookup"><span data-stu-id="1900f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="1900f-105">Project Operations cung cấp khả năng mạnh mẽ để phân loại doanh thu và chi phí trên các dự án.</span><span class="sxs-lookup"><span data-stu-id="1900f-105">Project Operations offers robust capabilities for categorizing revenue and expenses on projects.</span></span> <span data-ttu-id="1900f-106">Danh mục cung cấp khả năng báo cáo và phân tích các giao dịch dự án, đồng thời thúc đẩy việc đăng lên sổ cái.</span><span class="sxs-lookup"><span data-stu-id="1900f-106">Categories provide the ability to report on and analyze project transactions, and drive posting to the general ledger.</span></span>

<span data-ttu-id="1900f-107">Sơ đồ sau minh họa mối tương quan giữa các danh mục giao dịch, danh mục chia sẻ và danh mục dự án.</span><span class="sxs-lookup"><span data-stu-id="1900f-107">The following diagram illustrates the correlation between transaction categories, shared categories, and project categories.</span></span> 

<span data-ttu-id="1900f-108">Danh mục giao dịch là nhóm cơ bản cho các giao dịch dự án.</span><span class="sxs-lookup"><span data-stu-id="1900f-108">Transaction categories are the basic grouping for project transactions.</span></span> <span data-ttu-id="1900f-109">Trong nhóm đó, có một tập hợp các danh mục chung có thể được chia sẻ trên các ứng dụng và mô-đun.</span><span class="sxs-lookup"><span data-stu-id="1900f-109">Within that grouping, there is a set of shared categories that can be shared across applications and modules.</span></span> <span data-ttu-id="1900f-110">Phân tích các chi tiết cụ thể, danh mục dự án là cấp độ chi tiết nhất của các danh mục.</span><span class="sxs-lookup"><span data-stu-id="1900f-110">Getting even further into specifics, project categories are the most granular level of categories.</span></span> <span data-ttu-id="1900f-111">Các danh mục dự án dành riêng cho pháp nhân, mô-đun và ứng dụng.</span><span class="sxs-lookup"><span data-stu-id="1900f-111">Project categories are specific to legal entity, module, and application.</span></span>

![Mối tương quan giữa các danh mục giao dịch, danh mục chia sẻ và danh mục dự án](media/project-categories.png)

## <a name="transaction-categories"></a><span data-ttu-id="1900f-113">Danh mục giao dịch</span><span class="sxs-lookup"><span data-stu-id="1900f-113">Transaction categories</span></span>

<span data-ttu-id="1900f-114">Danh mục giao dịch đại diện cho nhóm cơ bản cho các giao dịch dự án và không dành riêng cho công ty hoặc loại giao dịch.</span><span class="sxs-lookup"><span data-stu-id="1900f-114">Transaction categories represent the basic grouping for project transactions and are not company or transaction type-specific.</span></span> <span data-ttu-id="1900f-115">Chẳng hạn, Contoso Robotics sử dụng các danh mục Thiết kế, Du lịch, Lắp đặt và Giao dịch dịch vụ để nhóm các giao dịch Dự án.</span><span class="sxs-lookup"><span data-stu-id="1900f-115">For example, Contoso Robotics uses Design, Travel, Installation, and Service Transaction categories to group Project transactions.</span></span>

<span data-ttu-id="1900f-116">Các danh mục giao dịch được xác định trong mô-đun Project Operations.</span><span class="sxs-lookup"><span data-stu-id="1900f-116">Transaction categories are defined in the Project Operations module.</span></span> 
1. <span data-ttu-id="1900f-117">Đi tới **Cài đặt** \> **Danh mục giao dịch** để mở biểu mẫu.</span><span class="sxs-lookup"><span data-stu-id="1900f-117">Go to **Settings** \> **Transaction Categories** to open the form.</span></span> 
2. <span data-ttu-id="1900f-118">Tạo một danh mục giao dịch mới bằng cách chọn **Mới** hoặc bằng cách chọn **Nhập từ Excel**.</span><span class="sxs-lookup"><span data-stu-id="1900f-118">Create a new transaction category either by selecting **New** or by selecting **Import from Excel**.</span></span>

## <a name="shared-categories"></a><span data-ttu-id="1900f-119">Danh mục chia sẻ</span><span class="sxs-lookup"><span data-stu-id="1900f-119">Shared categories</span></span>

<span data-ttu-id="1900f-120">Dynamics 365 sử dụng khái niệm Danh mục được chia sẻ để phân loại chi phí trong các ứng dụng khác nhau, chẳng hạn như Dynamics 365 Finance, Chuỗi cung ứng Dynamics 365 và Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="1900f-120">Dynamics 365 uses the Shared categories concept to categorize expenses in different applications, such as Dynamics 365 Finance, Dynamics 365 Supply Chain, and Dynamics 365 Project Operations.</span></span> <span data-ttu-id="1900f-121">Đối với mỗi danh mục giao dịch được tạo, Project Operations tự động tạo bốn danh mục được chia sẻ có liên quan: Giờ, Chi phí, Phí và Mục.</span><span class="sxs-lookup"><span data-stu-id="1900f-121">For each Transaction category created, Project Operations automatically creates four related Shared categories: Hours, Expense, Fees, and Item.</span></span> <span data-ttu-id="1900f-122">Bạn có thể xem lại và điều chỉnh các danh mục được chia sẻ bằng cách đi tới **Kế toán và quản lý dự án** \> **Thiết lập** \> **Thể loại** \> **Danh mục được chia sẻ**.</span><span class="sxs-lookup"><span data-stu-id="1900f-122">You can review and adjust the shared categories by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Shared Categories**.</span></span>

## <a name="project-categories"></a><span data-ttu-id="1900f-123">Thể loại dự án</span><span class="sxs-lookup"><span data-stu-id="1900f-123">Project categories</span></span>

<span data-ttu-id="1900f-124">Danh mục dự án đại diện cho mức độ chi tiết nhất của cấu hình danh mục và phải được định cấu hình riêng biệt và cho từng công ty, bởi một kế toán viên của dự án.</span><span class="sxs-lookup"><span data-stu-id="1900f-124">Project categories represent most granular level of category configuration and must be configured separately, and for each company, by a Project accountant.</span></span>

1. <span data-ttu-id="1900f-125">Đi đến **Kế toán và quản lý dự án** \> **Thiết lập** \> **Thể loại** \> **Danh mục dự án**.</span><span class="sxs-lookup"><span data-stu-id="1900f-125">Go to **Project Management and Accounting** \> **Setup** \> **Categories** \> **Project categories**.</span></span>
2. <span data-ttu-id="1900f-126">Chọn **Mới**.</span><span class="sxs-lookup"><span data-stu-id="1900f-126">Select **New**.</span></span>
3. <span data-ttu-id="1900f-127">Chọn **ID danh mục** của danh mục được chia sẻ mà bạn đã tạo trong phần trước.</span><span class="sxs-lookup"><span data-stu-id="1900f-127">Select the **Category ID** of the Shared category you created in the previous section.</span></span> <span data-ttu-id="1900f-128">Project Operations chỉ cho phép sử dụng những danh mục chia sẻ được liên kết với các danh mục giao dịch.</span><span class="sxs-lookup"><span data-stu-id="1900f-128">Project Operations allows using only those shared categories that are associated with transaction categories.</span></span>
4. <span data-ttu-id="1900f-129">Chọn một nhóm danh mục.</span><span class="sxs-lookup"><span data-stu-id="1900f-129">Select a category group.</span></span>

## <a name="category-groups"></a><span data-ttu-id="1900f-130">Nhóm danh mục</span><span class="sxs-lookup"><span data-stu-id="1900f-130">Category groups</span></span>

<span data-ttu-id="1900f-131">Nhóm danh mục được sử dụng để chia sẻ thuộc tính, chủ yếu đăng hồ sơ, giữa các danh mục dự án có liên quan.</span><span class="sxs-lookup"><span data-stu-id="1900f-131">Category groups are used to share properties, primarily posting profiles, between related Project categories.</span></span> <span data-ttu-id="1900f-132">Phải có ít nhất một nhóm danh mục cho mỗi loại giao dịch và mỗi danh mục dự án được chỉ định một nhóm.</span><span class="sxs-lookup"><span data-stu-id="1900f-132">There must be at least one category group for each transaction type and each project category is assigned a group.</span></span>

<span data-ttu-id="1900f-133">Thông số kỹ thuật đăng trong Project Operations được xác định bởi các quy tắc về hồ sơ doanh thu và chi phí dự án, danh mục dự án và nhóm danh mục.</span><span class="sxs-lookup"><span data-stu-id="1900f-133">The posting specifications in Project Operations are defined by the project cost and revenue profile rules, project categories, and category groups.</span></span> <span data-ttu-id="1900f-134">Bạn có thể thiết lập các nhóm danh mục bằng cách đi đến **Kế toán và quản lý dự án** \> **Thiết lập** \> **Danh mục** \> **Nhóm danh mục**.</span><span class="sxs-lookup"><span data-stu-id="1900f-134">You can set up category groups by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Category groups**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]