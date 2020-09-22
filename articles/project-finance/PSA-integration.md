---
title: Tổng quan về Project Service Automation
description: Chủ đề này cung cấp thông tin về giải pháp tích hợp Dynamics 365 Project Service Automation sang Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: 897e1a1c-d31c-42b8-bb59-6b67202d8d61
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 080a545d8713e52d9778367aec1969b815d683e5
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 03/24/2020
ms.locfileid: "3757078"
---
# <a name="project-service-automation-overview"></a><span data-ttu-id="578ae-103">Tổng quan về Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="578ae-103">Project Service Automation overview</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="578ae-104">Giải pháp tích hợp Project Service Automation sang Finance sử dụng tính năng Tích hợp dữ liệu để đồng bộ hóa dữ liệu giữa các phiên bản của Dynamics 365 Finance và Dynamics 365 Project Service Automation qua Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="578ae-104">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Dynamics 365 Finance and Dynamics 365 Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="578ae-105">Mẫu tích hợp có sẵn với tính năng Tích hợp dữ liệu cho phép dòng dữ liệu về dự án, hợp đồng dự án, mô tả hợp đồng dự án, mốc thời gian mô tả hợp đồng dự án, nhiệm vụ dự án, thể loại giao dịch chi phí, ước tính giờ và ước tính chi phí từ Project Service Automation sang Finance.</span><span class="sxs-lookup"><span data-stu-id="578ae-105">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="578ae-106">Nếu đang sử dụng phiên bản 7.3.0, bạn phải cài đặt KB 4074835.</span><span class="sxs-lookup"><span data-stu-id="578ae-106">If you're using version 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="578ae-107">Sau đó, bạn sẽ có thể tích hợp các dự án giá cố định.</span><span class="sxs-lookup"><span data-stu-id="578ae-107">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="578ae-108">Nếu bạn đang sử dụng phiên bản 7.3.0 và bạn đang chuyển các giao dịch phí từ Project Service Automation, bạn phải cài đặt KB 4345320 để bao gồm các khoản phí đó trong hóa đơn dự án.</span><span class="sxs-lookup"><span data-stu-id="578ae-108">If you're using version 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="578ae-109">Nếu bạn đang sử dụng phiên bản 8.0, bạn có thể sử dụng tính năng tích hợp nhiệm vụ dự án, thể loại giao dịch chi phí, ước tính giờ, ước tính chi phí và khóa chức năng.</span><span class="sxs-lookup"><span data-stu-id="578ae-109">If you're using version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="578ae-110">Nếu bạn đang sử dụng phiên bản 8.0.1 trở lên, bạn sẽ có thể đồng bộ hóa giá trị thực tế.</span><span class="sxs-lookup"><span data-stu-id="578ae-110">If you're using version 8.0.1 or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="578ae-111">Trước khi bạn có thể tích hợp Project Service Automation Finance, bạn phải đặt cấu hình các tham số tích hợp Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="578ae-111">Before you can integrate Project Service Automation Finance, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="578ae-112">Để biết thêm thông tin, hãy xem [tham số tích hợp Project Service Automation](PSA-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="578ae-112">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="578ae-113">Giải pháp tích hợp này cho phép đồng bộ hóa trực tiếp trong các trường hợp sau:</span><span class="sxs-lookup"><span data-stu-id="578ae-113">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="578ae-114">Duy trì các hợp đồng dự án trong Project Service Automation và đồng bộ hóa chúng trực tiếp từ Project Service Automation sang Finance.</span><span class="sxs-lookup"><span data-stu-id="578ae-114">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="578ae-115">Tạo dự án trong Project Service Automation và đồng bộ hóa chúng trực tiếp từ Project Service Automation sang Finance.</span><span class="sxs-lookup"><span data-stu-id="578ae-115">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="578ae-116">Duy trì các mô tả hợp đồng dự án trong Project Service Automation và đồng bộ hóa chúng trực tiếp từ Project Service Automation sang Finance.</span><span class="sxs-lookup"><span data-stu-id="578ae-116">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="578ae-117">Duy trì các mốc thời gian mô tả hợp đồng dự án trong Project Service Automation và đồng bộ hóa chúng trực tiếp từ Project Service Automation sang Finance.</span><span class="sxs-lookup"><span data-stu-id="578ae-117">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="578ae-118">Duy trì các nhiệm vụ dự án trong Project Service Automation và đồng bộ hóa chúng trực tiếp từ Project Service Automation sang Finance.</span><span class="sxs-lookup"><span data-stu-id="578ae-118">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="578ae-119">Duy trì các thể loại giao dịch chi phí trong Finance và đồng bộ hóa chúng trực tiếp từ Finance sang Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="578ae-119">Maintain expense transaction categories in Finance, and synchronize them directly from Finance to Project Service Automation.</span></span>
- <span data-ttu-id="578ae-120">Tạo ước tính giờ dự án trong Project Service Automation và đồng bộ hóa chúng trực tiếp từ Project Service Automation sang Finance.</span><span class="sxs-lookup"><span data-stu-id="578ae-120">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="578ae-121">Tạo ước tính chi phí dự án trong Project Service Automation và đồng bộ hóa chúng trực tiếp từ Project Service Automation sang Finance.</span><span class="sxs-lookup"><span data-stu-id="578ae-121">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="578ae-122">Tạo thời gian dự án, chi phí và giá trị thực tế của chi phí trong Project Service Automation và tạo các giao dịch dự án trong nhật ký tích hợp Project Service Automation sao cho chúng có thể được đăng trên Finance.</span><span class="sxs-lookup"><span data-stu-id="578ae-122">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="578ae-123">Đồng bộ hóa dữ liệu</span><span class="sxs-lookup"><span data-stu-id="578ae-123">Data synchronization</span></span>

<span data-ttu-id="578ae-124">Hình minh họa sau đây cho thấy cách dữ liệu được đồng bộ hóa như một phần của quá trình tích hợp giữa Project Service Automation và Finance.</span><span class="sxs-lookup"><span data-stu-id="578ae-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance.</span></span>

> [!NOTE]
> <span data-ttu-id="578ae-125">Không phải tất cả các mẫu đều có sẵn.</span><span class="sxs-lookup"><span data-stu-id="578ae-125">Not all templates are currently available.</span></span> <span data-ttu-id="578ae-126">Các mẫu sẽ được phát hành khi chúng hoàn thành.</span><span class="sxs-lookup"><span data-stu-id="578ae-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="578ae-127">[![Tích hợp Project Service Automation với Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="578ae-127">[![Project Service Automation integration with Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance"></a><span data-ttu-id="578ae-128">Yêu cầu hệ thống đối với Finance</span><span class="sxs-lookup"><span data-stu-id="578ae-128">System requirements for Finance</span></span>

<span data-ttu-id="578ae-129">Để sử dụng giải pháp tích hợp Project Service Automation với Finance, bạn phải cài đặt Enterprise Edition 7.3 với bản cập nhật Nền tảng từ 12 trở lên.</span><span class="sxs-lookup"><span data-stu-id="578ae-129">To use the Project Service Automation to Finance integration solution, you must install Enterprise edition 7.3 with Platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="578ae-130">Yêu cầu hệ thống đối với Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="578ae-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="578ae-131">Để sử dụng giải pháp tích hợp Project Service Automation sang Finance, bạn phải cài đặt các thành phần sau:</span><span class="sxs-lookup"><span data-stu-id="578ae-131">To use the Project Service Automation to Finance integration solution, you must install the following components:</span></span>

- <span data-ttu-id="578ae-132">Dynamics 365 Project Service Automation phiên bản 9.0.0.0 trở lên</span><span class="sxs-lookup"><span data-stu-id="578ae-132">Dynamics 365 Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="578ae-133">Triển vọng giải pháp tiền mặt cho Dynamics 365 Sales, phiên bản 1.14.0.0 (v14) trở lên</span><span class="sxs-lookup"><span data-stu-id="578ae-133">Prospect to cash solution for Dynamics 365 Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="578ae-134">Giải pháp Project Service Automation sang Finance cho Dynamics 365 Project Service Automation phiên bản 1.0.0.0 trở lên</span><span class="sxs-lookup"><span data-stu-id="578ae-134">Project Service Automation to Finance solution for Dynamics 365 Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="578ae-135">Cài đặt giải pháp tích hợp Project Service Automation sang Finance trong phiên bản Project Service Automation của bạn</span><span class="sxs-lookup"><span data-stu-id="578ae-135">Install the Project Service Automation to Finance integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="578ae-136">Tải xuống giải pháp tích hợp Project Service Automation sang Finance từ [Trung tâm Tải xuống của Microsoft ](https://www.microsoft.com/download/details.aspx?id=57016) và làm theo hướng dẫn đi kèm với giải pháp.</span><span class="sxs-lookup"><span data-stu-id="578ae-136">Download the Project Service Automation to Finance integration solution from [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>
