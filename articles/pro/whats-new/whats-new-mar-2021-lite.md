---
title: Tính năng mới tháng 3 năm 2021 - triển khai Project Operations lite
description: Chủ đề này cung cấp thông tin về các bản cập nhật chất lượng được cung cấp trong bản triển khai giản đơn Project Operations phát hành vào tháng 3 năm 2021.
author: sigitac
manager: tfehr
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: bd1518ef8f5645bace63a222b92cfd16d9c19a21
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500054"
---
# <a name="whats-new-march-2021---project-operations-lite-deployment"></a><span data-ttu-id="55c71-103">Tính năng mới tháng 3 năm 2021 - triển khai Project Operations lite</span><span class="sxs-lookup"><span data-stu-id="55c71-103">What's new March 2021 - Project Operations lite deployment</span></span>

<span data-ttu-id="55c71-104">_Áp dụng cho: Bản triển khai giản đơn - từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="55c71-104">_Applies To: Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="55c71-105">Chủ đề này áp dụng cho các phiên bản và thành phần sau của Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="55c71-105">This topic applies to the following Dynamics 365 Project Operations components and versions:</span></span>

- <span data-ttu-id="55c71-106">Project Operations trên môi trường Dataverse phiên bản 4.8.0.91</span><span class="sxs-lookup"><span data-stu-id="55c71-106">Project Operations on Dataverse environment version 4.8.0.91</span></span> 

## <a name="quality-updates"></a><span data-ttu-id="55c71-107">Bản cập nhật chất lượng</span><span class="sxs-lookup"><span data-stu-id="55c71-107">Quality updates</span></span>

| <span data-ttu-id="55c71-108">**Lĩnh vực tính năng**</span><span class="sxs-lookup"><span data-stu-id="55c71-108">**Feature area**</span></span> | <span data-ttu-id="55c71-109">**Số tham chiếu**</span><span class="sxs-lookup"><span data-stu-id="55c71-109">**Reference number**</span></span> | <span data-ttu-id="55c71-110">**Cập nhật chất lượng**</span><span class="sxs-lookup"><span data-stu-id="55c71-110">**Quality update**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="55c71-111">Định giá và thanh toán</span><span class="sxs-lookup"><span data-stu-id="55c71-111">Billing and pricing</span></span> | <span data-ttu-id="55c71-112">2133873</span><span class="sxs-lookup"><span data-stu-id="55c71-112">2133873</span></span> | <span data-ttu-id="55c71-113">Sửa lỗi hiển thị ký hiệu tiền tệ **Đơn giá bán hàng** trong lưới **Ước tính chi phí**.</span><span class="sxs-lookup"><span data-stu-id="55c71-113">Fixed the display of **Unit Sales Price** currency symbol in the **Expense Estimates** grid.</span></span> |
| <span data-ttu-id="55c71-114">Định giá và thanh toán</span><span class="sxs-lookup"><span data-stu-id="55c71-114">Billing and pricing</span></span> | <span data-ttu-id="55c71-115">2174616</span><span class="sxs-lookup"><span data-stu-id="55c71-115">2174616</span></span> | <span data-ttu-id="55c71-116">Khi giành được báo giá, bảng giá tùy chỉnh hợp đồng được tham chiếu đến các chi tiết dòng hợp đồng được sao chép từ báo giá.</span><span class="sxs-lookup"><span data-stu-id="55c71-116">When a quote is won, the contract custom pricelist is referenced on contract line details that are copied from the quote.</span></span> |
| <span data-ttu-id="55c71-117">Quản lý cơ hội</span><span class="sxs-lookup"><span data-stu-id="55c71-117">Opportunity Management</span></span> | <span data-ttu-id="55c71-118">2167475</span><span class="sxs-lookup"><span data-stu-id="55c71-118">2167475</span></span> | <span data-ttu-id="55c71-119">Số thuế cố định trong hóa đơn điều chỉnh có nguồn gốc từ một mục nhập thực tế chưa được lập hóa đơn.</span><span class="sxs-lookup"><span data-stu-id="55c71-119">Fixed tax amount in the correction invoice that originated an unbilled actual entry.</span></span> |
| <span data-ttu-id="55c71-120">Quản lý cơ hội</span><span class="sxs-lookup"><span data-stu-id="55c71-120">Opportunity Management</span></span> | <span data-ttu-id="55c71-121">2176285</span><span class="sxs-lookup"><span data-stu-id="55c71-121">2176285</span></span> | <span data-ttu-id="55c71-122">Số thuế không được sao chép từ chi tiết hợp đồng mua bán / dòng báo giá sang chi tiết hợp đồng chi phí / dòng báo giá.</span><span class="sxs-lookup"><span data-stu-id="55c71-122">Tax amount must not be copied from sales contract/quote line details to cost contract/quote line details.</span></span> |
| <span data-ttu-id="55c71-123">Quản lý cơ hội</span><span class="sxs-lookup"><span data-stu-id="55c71-123">Opportunity Management</span></span> | <span data-ttu-id="55c71-124">2188079</span><span class="sxs-lookup"><span data-stu-id="55c71-124">2188079</span></span> | <span data-ttu-id="55c71-125">Quy tắc thanh toán tách biệt không được tạo cho các hợp đồng không dựa trên công việc.</span><span class="sxs-lookup"><span data-stu-id="55c71-125">Split billing rule must not be created for contracts that are not work-based.</span></span> |
| <span data-ttu-id="55c71-126">Hoạch định và theo dõi dự án</span><span class="sxs-lookup"><span data-stu-id="55c71-126">Planning and Tracking</span></span> | <span data-ttu-id="55c71-127">2138853</span><span class="sxs-lookup"><span data-stu-id="55c71-127">2138853</span></span> | <span data-ttu-id="55c71-128">Chức năng sao chép dự án được cập nhật để đảm bảo các dòng ước tính chi phí mà các nhiệm vụ tham chiếu được sao chép vào dự án đích.</span><span class="sxs-lookup"><span data-stu-id="55c71-128">Project copy function updated to ensure expense estimate lines that reference tasks are copied to the destination project.</span></span> |
| <span data-ttu-id="55c71-129">Hoạch định và theo dõi dự án</span><span class="sxs-lookup"><span data-stu-id="55c71-129">Planning and Tracking</span></span> | <span data-ttu-id="55c71-130">2173259</span><span class="sxs-lookup"><span data-stu-id="55c71-130">2173259</span></span> | <span data-ttu-id="55c71-131">Chức năng sao chép dự án được cập nhật để đảm bảo nó không hiển thị thông báo lỗi **Sao chép WBS** trong một số trường hợp nhất định.</span><span class="sxs-lookup"><span data-stu-id="55c71-131">Project copy function updated to ensure it doesn't display the **Copying WBS** error message in certain scenarios.</span></span> |
| <span data-ttu-id="55c71-132">Thời gian và Chi phí</span><span class="sxs-lookup"><span data-stu-id="55c71-132">Time and Expense</span></span> | <span data-ttu-id="55c71-133">2148910</span><span class="sxs-lookup"><span data-stu-id="55c71-133">2148910</span></span> | <span data-ttu-id="55c71-134">Khắc phục lỗi hiển thị với trang **Chỉnh sửa mục nhập** trong lưới **Mục nhập thời gian**.</span><span class="sxs-lookup"><span data-stu-id="55c71-134">Fixed display issue with the **Edit Entry** page in the **Time Entry** grid.</span></span> |
| <span data-ttu-id="55c71-135">Thời gian và Chi phí</span><span class="sxs-lookup"><span data-stu-id="55c71-135">Time and Expense</span></span> | <span data-ttu-id="55c71-136">2159798</span><span class="sxs-lookup"><span data-stu-id="55c71-136">2159798</span></span> | <span data-ttu-id="55c71-137">Kiểm soát chặt chẽ để đảm bảo không thể chỉnh sửa các mục chi phí đã được phê duyệt.</span><span class="sxs-lookup"><span data-stu-id="55c71-137">Tightened controls to ensure approved expense entries can't be edited.</span></span> |


