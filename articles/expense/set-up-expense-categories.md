---
title: Thiết lập danh mục chi phí
description: Chủ đề này cung cấp thông tin về cách thiết lập danh mục chi phí và danh mục chia sẻ cho báo cáo chi phí.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: f051d70f3dfe3b241dc0a206c0cdfda000f87c76
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896712"
---
# <a name="set-up-expense-categories"></a><span data-ttu-id="2ffbe-103">Thiết lập danh mục chi phí</span><span class="sxs-lookup"><span data-stu-id="2ffbe-103">Set up expense categories</span></span>

<span data-ttu-id="2ffbe-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_</span><span class="sxs-lookup"><span data-stu-id="2ffbe-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="2ffbe-105">Khi nhân viên tạo báo cáo chi phí, mỗi khoản chi phí mà họ ghi lại phải được liên kết với một loại chi phí.</span><span class="sxs-lookup"><span data-stu-id="2ffbe-105">When employees create expense reports, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="2ffbe-106">Các danh mục chi phí có nguồn gốc từ các danh mục dùng chung có thể được chia sẻ giữa các pháp nhân trong tổ chức của bạn.</span><span class="sxs-lookup"><span data-stu-id="2ffbe-106">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="2ffbe-107">Tùy thuộc vào cách tổ chức của bạn được xác định, các danh mục chi phí này cũng có thể được dùng chung trong các lĩnh vực khác.</span><span class="sxs-lookup"><span data-stu-id="2ffbe-107">Depending on how your organization is defined, these expense categories can also be shared in other areas.</span></span> <span data-ttu-id="2ffbe-108">Dựa trên định nghĩa về tổ chức của bạn và hướng dẫn từ nhóm thực hiện, bạn phải xác định xem các danh mục được sử dụng trong quản lý Chi phí sẽ chỉ được sử dụng trong quản lý Chi phí hay nên được dùng chung trong các lĩnh vực khác.</span><span class="sxs-lookup"><span data-stu-id="2ffbe-108">Based on the definition of your organization and guidance from the implementation team, you must determine whether the categories that are used in Expense management will be used only in Expense management or should be shared in other areas.</span></span>

> [!NOTE]
> <span data-ttu-id="2ffbe-109">Các danh mục này có thể được chia sẻ giữa Quản lý dự án, kế toán và Quản lý chi phí, hoặc giữa Quản lý dự án, kế toán và Sản xuất.</span><span class="sxs-lookup"><span data-stu-id="2ffbe-109">These categories can be shared between Project management and accounting and Expense management, or between Project management and accounting and Production.</span></span> <span data-ttu-id="2ffbe-110">Tuy nhiên, Quản lý chi phí và Sản xuất không thể dùng chung các danh mục này.</span><span class="sxs-lookup"><span data-stu-id="2ffbe-110">However, they can't be shared between Expense management and Production.</span></span>

<span data-ttu-id="2ffbe-111">Trước khi bạn có thể bắt đầu quá trình thiết lập, các quyết định sau phải được thực hiện cho từng loại chi phí:</span><span class="sxs-lookup"><span data-stu-id="2ffbe-111">Before you can begin the setup process, the following decisions must be made for each expense category:</span></span>

- <span data-ttu-id="2ffbe-112">Thể loại chi phí là gì?</span><span class="sxs-lookup"><span data-stu-id="2ffbe-112">What is the expense category?</span></span> <span data-ttu-id="2ffbe-113">Ví dụ bao gồm các danh mục cho chuyến bay, khách sạn hoặc số dặm.</span><span class="sxs-lookup"><span data-stu-id="2ffbe-113">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="2ffbe-114">Danh mục chi phí cũng có thể được sử dụng trong Quản lý dự án và kế toán không?</span><span class="sxs-lookup"><span data-stu-id="2ffbe-114">Can the expense category also be used in Project management and accounting?</span></span> <span data-ttu-id="2ffbe-115">Nếu có thể, bạn cũng phải đưa ra các quyết định sau:</span><span class="sxs-lookup"><span data-stu-id="2ffbe-115">If it can, you must also make the following decisions:</span></span>

    - <span data-ttu-id="2ffbe-116">Tài khoản chi phí nào sẽ được sử dụng cho các khoản chi phí sau?</span><span class="sxs-lookup"><span data-stu-id="2ffbe-116">Which cost accounts will be used for the following expenses?</span></span>

        - <span data-ttu-id="2ffbe-117">Chi phí</span><span class="sxs-lookup"><span data-stu-id="2ffbe-117">Cost</span></span>
        - <span data-ttu-id="2ffbe-118">Phân bổ bảng lương</span><span class="sxs-lookup"><span data-stu-id="2ffbe-118">Payroll allocation</span></span>
        - <span data-ttu-id="2ffbe-119">Giá trị chi phí WIP</span><span class="sxs-lookup"><span data-stu-id="2ffbe-119">WIP-cost value</span></span>
        - <span data-ttu-id="2ffbe-120">Chi phí-mục</span><span class="sxs-lookup"><span data-stu-id="2ffbe-120">Cost-item</span></span>
        - <span data-ttu-id="2ffbe-121">Mục giá trị chi phí WIP</span><span class="sxs-lookup"><span data-stu-id="2ffbe-121">WIP-cost value-item</span></span>
        - <span data-ttu-id="2ffbe-122">Lỗ lũy kế</span><span class="sxs-lookup"><span data-stu-id="2ffbe-122">Accrued loss</span></span>
        - <span data-ttu-id="2ffbe-123">Lỗ lũy kế WIP</span><span class="sxs-lookup"><span data-stu-id="2ffbe-123">WIP-accrued loss</span></span>

    - <span data-ttu-id="2ffbe-124">Tài khoản doanh thu sẽ được sử dụng cho những nguồn thu nào sau đây?</span><span class="sxs-lookup"><span data-stu-id="2ffbe-124">Which revenue accounts will be used for the following sources of revenue?</span></span>

        - <span data-ttu-id="2ffbe-125">Doanh thu đã lập hóa đơn</span><span class="sxs-lookup"><span data-stu-id="2ffbe-125">Invoiced revenue</span></span>
        - <span data-ttu-id="2ffbe-126">Giá trị bán hàng – doanh thu tích lũy</span><span class="sxs-lookup"><span data-stu-id="2ffbe-126">Accrued revenue-sales value</span></span>
        - <span data-ttu-id="2ffbe-127">Giá trị bán hàng WIP</span><span class="sxs-lookup"><span data-stu-id="2ffbe-127">WIP-sales value</span></span>
        - <span data-ttu-id="2ffbe-128">Sản xuất – doanh thu tích lũy</span><span class="sxs-lookup"><span data-stu-id="2ffbe-128">Accrued revenue-production</span></span>
        - <span data-ttu-id="2ffbe-129">Sản xuất WIP</span><span class="sxs-lookup"><span data-stu-id="2ffbe-129">WIP-production</span></span>
        - <span data-ttu-id="2ffbe-130">Lợi nhuận – doanh thu tích lũy</span><span class="sxs-lookup"><span data-stu-id="2ffbe-130">Accrued revenue-profit</span></span>
        - <span data-ttu-id="2ffbe-131">WIP-lợi nhuận</span><span class="sxs-lookup"><span data-stu-id="2ffbe-131">WIP-profit</span></span>
        - <span data-ttu-id="2ffbe-132">Đăng ký – doanh thu tích lũy</span><span class="sxs-lookup"><span data-stu-id="2ffbe-132">Accrued revenue-subscription</span></span>
        - <span data-ttu-id="2ffbe-133">Đăng ký –WIP</span><span class="sxs-lookup"><span data-stu-id="2ffbe-133">WIP-subscription</span></span>

- <span data-ttu-id="2ffbe-134">Loại chi phí là gì?</span><span class="sxs-lookup"><span data-stu-id="2ffbe-134">What is the expense type?</span></span>
- <span data-ttu-id="2ffbe-135">Phương thức thanh toán mặc định cho loại chi phí là gì?</span><span class="sxs-lookup"><span data-stu-id="2ffbe-135">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="2ffbe-136">Các khoản chi trong danh mục chi phí có phải được chia thành từng khoản không?</span><span class="sxs-lookup"><span data-stu-id="2ffbe-136">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="2ffbe-137">Tài khoản chính mặc định cho loại chi phí là gì?</span><span class="sxs-lookup"><span data-stu-id="2ffbe-137">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="2ffbe-138">Nhóm thuế bán hàng mặc định cho danh mục chi phí là gì?</span><span class="sxs-lookup"><span data-stu-id="2ffbe-138">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="2ffbe-139">Các phương thức thanh toán bổ sung có được phép cho loại chi phí không?</span><span class="sxs-lookup"><span data-stu-id="2ffbe-139">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="2ffbe-140">Nếu có, đó là phương thức thanh toán bổ sung nào?</span><span class="sxs-lookup"><span data-stu-id="2ffbe-140">If so, what are they?</span></span>
- <span data-ttu-id="2ffbe-141">Có danh mục phụ nào trong danh mục chi phí này không?</span><span class="sxs-lookup"><span data-stu-id="2ffbe-141">Are there subcategories in this expense category?</span></span> <span data-ttu-id="2ffbe-142">Nếu có danh mục phụ, bạn cũng phải đưa ra các quyết định sau:</span><span class="sxs-lookup"><span data-stu-id="2ffbe-142">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="2ffbe-143">Có bất kỳ danh mục phụ nào bị loại trừ khỏi việc thu hồi thuế không?</span><span class="sxs-lookup"><span data-stu-id="2ffbe-143">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="2ffbe-144">Nhóm thuế bán hàng của các danh mục phụ là gì?</span><span class="sxs-lookup"><span data-stu-id="2ffbe-144">What is the item sales tax group of the subcategories?</span></span>
