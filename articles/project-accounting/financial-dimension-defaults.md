---
title: Giá trị mặc định cho thông số tài chính
description: Chủ đề này cung cấp thông tin về cách thiết lập các giá trị mặc định cho thông số tài chính.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0a76447bb1a81a7157fccc0cd58eddd1eb5995de
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950155"
---
# <a name="financial-dimension-defaults"></a><span data-ttu-id="dd16f-103">Giá trị mặc định cho thông số tài chính</span><span class="sxs-lookup"><span data-stu-id="dd16f-103">Financial dimension defaults</span></span>

<span data-ttu-id="dd16f-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_</span><span class="sxs-lookup"><span data-stu-id="dd16f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="dd16f-105">Dynamics 365 Project Operations dùng khung [Thông số tài chính](/dynamics365/finance/general-ledger/financial-dimensions) trong Dynamics 365 Finance để cung cấp thêm thông tin chi tiết về các giao dịch trong sổ cái phụ và sổ cái chung của dự án.</span><span class="sxs-lookup"><span data-stu-id="dd16f-105">Dynamics 365 Project Operations uses the [Financial dimensions](/dynamics365/finance/general-ledger/financial-dimensions) framework in Dynamics 365 Finance to provide additional insights on project subledger and general ledger transactions.</span></span>

<span data-ttu-id="dd16f-106">Các thông số tài chính mặc định có thể được đặt theo khách hàng, nguồn tài trợ dự án, mốc, phần mô tả hợp đồng dự án hoặc dự án.</span><span class="sxs-lookup"><span data-stu-id="dd16f-106">Default financial dimensions can be set on a customer, project funding source, milestone, project contract line, or project.</span></span>

## <a name="define-default-financial-dimensions-for-a-customer"></a><span data-ttu-id="dd16f-107">Xác định các thông số tài chính mặc định cho khách hàng</span><span class="sxs-lookup"><span data-stu-id="dd16f-107">Define default financial dimensions for a customer</span></span>

<span data-ttu-id="dd16f-108">Các giá trị mặc định của thông số khách hàng được chỉ định trong Finance.</span><span class="sxs-lookup"><span data-stu-id="dd16f-108">Customer dimension defaults are specified in Finance.</span></span> <span data-ttu-id="dd16f-109">Hoàn tất các bước sau để thiết lập giá trị mặc định cho thông số.</span><span class="sxs-lookup"><span data-stu-id="dd16f-109">Complete the following steps to set dimension defaults.</span></span>

1. <span data-ttu-id="dd16f-110">Chuyển đến **Khoản phải thu** > **Khách hàng** > **Tất cả khách hàng**.</span><span class="sxs-lookup"><span data-stu-id="dd16f-110">Go to **Accounts receivable** > **Customers** > **All customers**.</span></span>
2. <span data-ttu-id="dd16f-111">Trên trang **Khách hàng**, ở tab **Thông số tài chính**, hãy đặt các giá trị của thông số tài chính cho khách hàng cụ thể.</span><span class="sxs-lookup"><span data-stu-id="dd16f-111">On the **Customers** page, on the **Financial dimensions** tab, set the financial dimension values for specific customer.</span></span>

## <a name="define-default-financial-dimensions-for-project-contracts"></a><span data-ttu-id="dd16f-112">Xác định thông số tài chính mặc định cho các hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="dd16f-112">Define default financial dimensions for project contracts</span></span>

<span data-ttu-id="dd16f-113">Hợp đồng dự án được tạo và duy trì trong Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="dd16f-113">Project contracts are created and maintained in Common Data Service (CDS).</span></span> <span data-ttu-id="dd16f-114">Các thuộc tính kế toán của hợp đồng dự án được đặt ở mô-đun **Kế toán và quản lý dự án** trong Finance.</span><span class="sxs-lookup"><span data-stu-id="dd16f-114">Accounting attributes for project contracts are set in the **Project management and accounting** module in Finance.</span></span>

### <a name="set-financial-dimensions-for-a-project-funding-source"></a><span data-ttu-id="dd16f-115">Đặt các thông số tài chính cho nguồn tài trợ dự án</span><span class="sxs-lookup"><span data-stu-id="dd16f-115">Set financial dimensions for a project funding source</span></span>

1. <span data-ttu-id="dd16f-116">Chuyển đến **Kế toán và quản lý dự án** > **Dự án** > **Hợp đồng dự án**.</span><span class="sxs-lookup"><span data-stu-id="dd16f-116">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="dd16f-117">Chọn hồ sơ bạn muốn cập nhật, trên tab **Hợp đồng dự án**, chọn **Hiển thị giá trị kế toán mặc định**.</span><span class="sxs-lookup"><span data-stu-id="dd16f-117">Select the record you want to update, and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="dd16f-118">Mở rộng **Thông tin liên quan** rồi chọn tab **Nguồn tài trợ**.</span><span class="sxs-lookup"><span data-stu-id="dd16f-118">Expand **Related information** and select the **Funding sources** tab.</span></span>
4. <span data-ttu-id="dd16f-119">Đặt các giá trị mặc định cho thông số tài chính.</span><span class="sxs-lookup"><span data-stu-id="dd16f-119">Set the financial dimension defaults.</span></span> <span data-ttu-id="dd16f-120">Lưu ý rằng các thông số tài chính lấy giá trị mặc định từ tài khoản khách hàng.</span><span class="sxs-lookup"><span data-stu-id="dd16f-120">Notice that the financial dimensions default from the customer account.</span></span>

### <a name="set-financial-dimensions-for-a-project-contract-line"></a><span data-ttu-id="dd16f-121">Đặt các thông số tài chính cho phần mô tả hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="dd16f-121">Set financial dimensions for a project contract line</span></span>

1. <span data-ttu-id="dd16f-122">Chuyển đến **Kế toán và quản lý dự án** > **Dự án** > **Hợp đồng dự án**.</span><span class="sxs-lookup"><span data-stu-id="dd16f-122">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="dd16f-123">Chọn hồ sơ bạn muốn cập nhật, trên tab **Hợp đồng dự án**, chọn **Hiển thị giá trị kế toán mặc định**.</span><span class="sxs-lookup"><span data-stu-id="dd16f-123">Select the record you want to update and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="dd16f-124">Mở rộng **Thông tin liên quan** rồi chọn tab **Nguồn tài trợ**.</span><span class="sxs-lookup"><span data-stu-id="dd16f-124">Expand **Related information** and select the **Contract lines** tab.</span></span>
4. <span data-ttu-id="dd16f-125">Đặt các giá trị mặc định cho thông số tài chính.</span><span class="sxs-lookup"><span data-stu-id="dd16f-125">Set the financial dimension defaults.</span></span> <span data-ttu-id="dd16f-126">Các giá trị mặc định của thông số tài chính được áp dụng và chỉ có thể dùng với các dòng mô tả hợp đồng có Giá cố định (mốc).</span><span class="sxs-lookup"><span data-stu-id="dd16f-126">The financial dimension defaults are applicable and can be used only with Fixed price (milestone) contract lines.</span></span>

<span data-ttu-id="dd16f-127">Các giá trị mặc định này được sử dụng cho các giao dịch trên tài khoản và các dòng mô tả hóa đơn có liên quan của dự án.</span><span class="sxs-lookup"><span data-stu-id="dd16f-127">These defaults are used on related project on-account transactions and invoice lines.</span></span>

## <a name="define-default-financial-dimensions-for-projects"></a><span data-ttu-id="dd16f-128">Xác định thông số tài chính mặc định cho các dự án</span><span class="sxs-lookup"><span data-stu-id="dd16f-128">Define default financial dimensions for projects</span></span>

<span data-ttu-id="dd16f-129">Dự án được tạo và duy trì trong CDS.</span><span class="sxs-lookup"><span data-stu-id="dd16f-129">Projects are created and maintained in CDS.</span></span> <span data-ttu-id="dd16f-130">Các thuộc tính kế toán của dự án được đặt ở mô-đun **Kế toán và quản lý dự án** trong Finance.</span><span class="sxs-lookup"><span data-stu-id="dd16f-130">Accounting attributes for projects are set in the **Project management and accounting** module in Finance.</span></span>

1. <span data-ttu-id="dd16f-131">Chuyển đến **Kế toán và quản lý dự án** > **Dự án** > **Tất cả dự án**.</span><span class="sxs-lookup"><span data-stu-id="dd16f-131">Go to **Project management and accounting** > **Projects** > **All projects**.</span></span>
2. <span data-ttu-id="dd16f-132">Chọn hồ sơ bạn muốn cập nhật, trên tab **Dự án**, chọn **Hiển thị giá trị kế toán mặc định**.</span><span class="sxs-lookup"><span data-stu-id="dd16f-132">Select the record that you want to update and on the **Project** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="dd16f-133">Mở rộng **Thông tin liên quan** rồi chọn tab **Thiết lập**.</span><span class="sxs-lookup"><span data-stu-id="dd16f-133">Expand **Related information** and select the **Setup** tab.</span></span>
4. <span data-ttu-id="dd16f-134">Đặt các giá trị mặc định cho thông số tài chính.</span><span class="sxs-lookup"><span data-stu-id="dd16f-134">Set the financial dimension defaults.</span></span> <span data-ttu-id="dd16f-135">Lưu ý rằng các thông số tài chính lấy giá trị mặc định từ tài khoản khách hàng.</span><span class="sxs-lookup"><span data-stu-id="dd16f-135">Notice that financial dimensions default from the customer account.</span></span> <span data-ttu-id="dd16f-136">Nếu dự án được liên kết với phần mô tả hợp đồng có nhiều khách hàng trong hợp đồng dự án, thì khách hàng chính được sử dụng làm thông số tài chính mặc định.</span><span class="sxs-lookup"><span data-stu-id="dd16f-136">If the project is associated with a contract line with multiple project contract customers, the primary customer is used to default financial dimensions.</span></span>

<span data-ttu-id="dd16f-137">Các thông số tài chính mặc định của dự án được sử dụng để đặt các giá trị mặc định về thời gian, chi phí và phí giao dịch cho dòng nhật ký kế toán trong **Nhật ký tích hợp Project Operations** và trên các dòng mô tả hóa đơn dự án có liên quan.</span><span class="sxs-lookup"><span data-stu-id="dd16f-137">Project default financial dimensions are used to set journal line defaults for time, expense, and fee transactions in the **Project Operations Integration Journal** and on related project invoice lines.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]