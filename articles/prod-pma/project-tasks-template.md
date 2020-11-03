---
title: Đồng bộ hóa nhiệm vụ dự án trực tiếp từ Project Service Automation sang Finance and Operations
description: Chủ đề này mô tả mẫu và nhiệm vụ cơ bản dùng để đồng bộ hóa trực tiếp các nhiệm vụ dự án từ Microsoft Dynamics 365 Project Service Automation sang Dynamics 365 Finance.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 0383607a07def6c21562bf4b0893fe3ce3db6a04
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087090"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="e7b7c-103">Đồng bộ hóa nhiệm vụ dự án trực tiếp từ Project Service Automation sang Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e7b7c-103">Synchronize project tasks directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e7b7c-104">Chủ đề này mô tả mẫu và nhiệm vụ cơ bản dùng để đồng bộ hóa trực tiếp các nhiệm vụ dự án từ Dynamics 365 Project Service Automation sang Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="e7b7c-104">This topic describes the template and underlying task that are used to synchronize project tasks directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="e7b7c-105">Tính năng tích hợp nhiệm vụ dự án, thể loại giao dịch chi phí, ước tính giờ, ước tính chi phí và khóa chức năng có sẵn trong phiên bản 8.0.</span><span class="sxs-lookup"><span data-stu-id="e7b7c-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="e7b7c-106">Nếu bạn đang sử dụng Enterprise Edition 7.3.0, sau khi cài đặt KB 4132657 và KB 4132660, thì bạn sẽ có thể sử dụng các mẫu để tích hợp nhiệm vụ dự án, danh mục giao dịch chi phí, các giá trị ước tính giờ, ước tính chi phí và giá trị thực tế để đặt cấu hình tùy chọn khóa chức năng.</span><span class="sxs-lookup"><span data-stu-id="e7b7c-106">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="e7b7c-107">Nếu bạn phải đặt lại các bản phân bổ kế toán, thì chúng tôi khuyên bạn cũng nên cài đặt KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="e7b7c-107">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>
> - <span data-ttu-id="e7b7c-108">Tùy chọn tích hợp giá trị thực tế có sẵn từ phiên bản 8.0.1.</span><span class="sxs-lookup"><span data-stu-id="e7b7c-108">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="e7b7c-109">Luồng dữ liệu cho Project Service Automation sang Finance</span><span class="sxs-lookup"><span data-stu-id="e7b7c-109">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="e7b7c-110">Giải pháp tích hợp Project Service Automation sang Finance sử dụng tính năng Tích hợp dữ liệu để đồng bộ hóa dữ liệu giữa các phiên bản của Project Service Automation và Finance.</span><span class="sxs-lookup"><span data-stu-id="e7b7c-110">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="e7b7c-111">Các mẫu tích hợp có sẵn với tính năng Tích hợp dữ liệu sẽ tạo ra luồng dữ liệu về nhiệm vụ dự án từ Project Service Automation đến Finance.</span><span class="sxs-lookup"><span data-stu-id="e7b7c-111">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance.</span></span>

<span data-ttu-id="e7b7c-112">Hình minh họa sau đây cho thấy cách dữ liệu được đồng bộ hóa giữa Project Service Automation và Finance.</span><span class="sxs-lookup"><span data-stu-id="e7b7c-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="e7b7c-113">[![Luồng dữ liệu cho phần tích hợp Project Service Automation với Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="e7b7c-113">[![Data flow for Project Service Automation integration with Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="e7b7c-114">Mẫu và nhiệm vụ</span><span class="sxs-lookup"><span data-stu-id="e7b7c-114">Template and task</span></span>

<span data-ttu-id="e7b7c-115">Để truy cập vào mẫu, trong trung tâm quản trị Microsoft Power Apps, chọn **Dự án** và sau đó, ở góc trên bên phải, chọn **Dự án mới** để chọn các mẫu công khai.</span><span class="sxs-lookup"><span data-stu-id="e7b7c-115">To access the template, in the Microsoft Power Apps admin center, select **Projects** , and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="e7b7c-116">Mẫu sau và nhiệm vụ cơ bản được sử dụng để đồng bộ hóa nhiệm vụ dự án từ Project Service Automation sang Finance:</span><span class="sxs-lookup"><span data-stu-id="e7b7c-116">The following template and underlying task are used to synchronize project tasks from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="e7b7c-117">**Tên mẫu trong Tích hợp dữ liệu:** Nhiệm vụ dự án (PSA sang Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="e7b7c-117">**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="e7b7c-118">**Tên của nhiệm vụ trong dự án:** Nhiệm vụ dự án</span><span class="sxs-lookup"><span data-stu-id="e7b7c-118">**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="e7b7c-119">Trước khi quá trình đồng bộ hóa nhiệm vụ dự án có thể xảy ra, bạn phải đồng bộ hóa hợp đồng dự án và dự án.</span><span class="sxs-lookup"><span data-stu-id="e7b7c-119">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="e7b7c-120">Bộ thực thể</span><span class="sxs-lookup"><span data-stu-id="e7b7c-120">Entity set</span></span>

| <span data-ttu-id="e7b7c-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="e7b7c-121">Project Service Automation</span></span> | <span data-ttu-id="e7b7c-122">Tài chính</span><span class="sxs-lookup"><span data-stu-id="e7b7c-122">Finance</span></span>                             |
|----------------------------|-------------------------------------|
| <span data-ttu-id="e7b7c-123">Nhiệm vụ Dự án</span><span class="sxs-lookup"><span data-stu-id="e7b7c-123">Project Tasks</span></span>              | <span data-ttu-id="e7b7c-124">Thực thể tích hợp cho nhiệm vụ dự án</span><span class="sxs-lookup"><span data-stu-id="e7b7c-124">Integration entity for project task</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="e7b7c-125">Luồng thực thể</span><span class="sxs-lookup"><span data-stu-id="e7b7c-125">Entity flow</span></span>

<span data-ttu-id="e7b7c-126">Nhiệm vụ dự án được quản lý trong Project Service Automation và được đồng bộ hóa với Finance dưới dạng hoạt động dự án.</span><span class="sxs-lookup"><span data-stu-id="e7b7c-126">Project tasks are managed in Project Service Automation, and they are synchronized to Finance as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="e7b7c-127">Điều kiện tiên quyết và thiết lập ánh xạ</span><span class="sxs-lookup"><span data-stu-id="e7b7c-127">Prerequisites and mapping setup</span></span>

<span data-ttu-id="e7b7c-128">Trước khi quá trình đồng bộ hóa nhiệm vụ dự án có thể xảy ra, bạn phải đồng bộ hóa hợp đồng dự án và dự án.</span><span class="sxs-lookup"><span data-stu-id="e7b7c-128">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="e7b7c-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="e7b7c-129">Power Query</span></span>

<span data-ttu-id="e7b7c-130">Bạn phải sử dụng Microsoft Power Query dành cho Excel để lọc dữ liệu nếu điều kiện sau được đáp ứng:</span><span class="sxs-lookup"><span data-stu-id="e7b7c-130">You must use Microsoft Power Query for Excel to filter data if this condition is met:</span></span>

- <span data-ttu-id="e7b7c-131">Bạn có bản ghi dành riêng cho nguồn lực trong nhiệm vụ dự án.</span><span class="sxs-lookup"><span data-stu-id="e7b7c-131">You have resource-specific records in a project task.</span></span>

<span data-ttu-id="e7b7c-132">Nếu bạn phải sử dụng Power Query, hãy làm theo hướng dẫn sau:</span><span class="sxs-lookup"><span data-stu-id="e7b7c-132">If you must use Power Query, follow this guideline:</span></span>

- <span data-ttu-id="e7b7c-133">Mẫu Nhiệm vụ dự án (PSA sang Fin và Ops) có bộ lọc mặc định loại trừ các bản ghi dành riêng cho nguồn lực khỏi nhiệm vụ dự án bằng cách thiết lập bộ lọc trên **IsLineTask** thành **False**.</span><span class="sxs-lookup"><span data-stu-id="e7b7c-133">The Project tasks (PSA to Fin and Ops) template has a default filter that excludes resource-specific records from a project task by setting the filter on **IsLineTask** to **False**.</span></span> <span data-ttu-id="e7b7c-134">Nếu bạn tạo mẫu của riêng mình, bạn phải thêm bộ lọc này.</span><span class="sxs-lookup"><span data-stu-id="e7b7c-134">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="e7b7c-135">Ánh xạ mẫu trong tích hợp dữ liệu</span><span class="sxs-lookup"><span data-stu-id="e7b7c-135">Template mapping in Data integration</span></span>

<span data-ttu-id="e7b7c-136">Hình sau đây minh họa một ví dụ về việc ánh xạ nhiệm vụ mẫu trong Tích hợp dữ liệu.</span><span class="sxs-lookup"><span data-stu-id="e7b7c-136">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="e7b7c-137">Tùy chọn ánh xạ hiển thị thông tin trường sẽ được đồng bộ hóa từ Project Service Automation sang Finance.</span><span class="sxs-lookup"><span data-stu-id="e7b7c-137">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="e7b7c-138">[![Ánh xạ mẫu](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="e7b7c-138">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>
