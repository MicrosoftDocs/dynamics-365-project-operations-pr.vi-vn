---
title: Phân phối trên báo cáo chi phí
description: Khi nhập chi phí trên báo cáo chi phí, bạn có thể phân bổ chi phí cho nhiều dự án, pháp nhân hoặc tài khoản trong tổ chức của mình.
author: ShylaThompson
manager: AnnBe
ms.date: 09/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 857573c0c2ffaf1ce4bdeaf109a20c6c777b2288
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271784"
---
# <a name="expense-report-distributions"></a><span data-ttu-id="e5c38-103">Phân phối trên báo cáo chi phí</span><span class="sxs-lookup"><span data-stu-id="e5c38-103">Expense report distributions</span></span>

<span data-ttu-id="e5c38-104">Khi nhập chi phí trên báo cáo chi phí, bạn có thể phân bổ chi phí cho nhiều dự án, thông số tài chính hoặc tài khoản trong tổ chức của mình.</span><span class="sxs-lookup"><span data-stu-id="e5c38-104">When you enter expenses on an expense report, you can distribute the expense across multiple projects, financial dimensions, or accounts in your organization.</span></span>

<span data-ttu-id="e5c38-105">Ví dụ: Nancy, một đại diện bán hàng của Fabrikam, đã đi từ Copenhagen đến Frankfurt.</span><span class="sxs-lookup"><span data-stu-id="e5c38-105">For example, Nancy, a Fabrikam sales representative, traveled from Copenhagen to Frankfurt.</span></span> <span data-ttu-id="e5c38-106">Ở Frankfurt, cô ấy đã gặp hai tổ chức để thảo luận về các dự án riêng biệt cho từng tổ chức.</span><span class="sxs-lookup"><span data-stu-id="e5c38-106">In Frankfurt, she met with two organizations to discuss separate projects for each organization.</span></span> <span data-ttu-id="e5c38-107">Nancy đã dành 7 ngày làm việc với tổ chức A về dự án A và 3 ngày làm việc với tổ chức B về dự án B.</span><span class="sxs-lookup"><span data-stu-id="e5c38-107">Nancy spent seven business days working with organization A on project A, and three business days working with organization B on project B.</span></span>

<span data-ttu-id="e5c38-108">Bởi vì Nancy đã làm việc cho 2 dự án riêng biệt ở Frankfurt, nên khi cô ấy nhập báo cáo chi phí, Nancy phân bổ các chi phí phù hợp cho từng dự án.</span><span class="sxs-lookup"><span data-stu-id="e5c38-108">Because Nancy worked on two separate projects when she was in Frankfurt, when she enters her expense report, she distributes her expenses as appropriate for each project.</span></span> <span data-ttu-id="e5c38-109">Bảng sau cho thấy cách thức Nancy phân bổ chi phí.</span><span class="sxs-lookup"><span data-stu-id="e5c38-109">The following table shows how Nancy distributed her expenses.</span></span>


| <span data-ttu-id="e5c38-110">Loại chi phí</span><span class="sxs-lookup"><span data-stu-id="e5c38-110">Expense type</span></span> | <span data-ttu-id="e5c38-111">Tổng số tiền chi phí</span><span class="sxs-lookup"><span data-stu-id="e5c38-111">Total expense amount</span></span>|<span data-ttu-id="e5c38-112">Số tiền phân bổ cho dự án A</span><span class="sxs-lookup"><span data-stu-id="e5c38-112">Amount distributed to project A</span></span>| <span data-ttu-id="e5c38-113">Số tiền phân bổ cho dự án B</span><span class="sxs-lookup"><span data-stu-id="e5c38-113">Amount distributed to project B</span></span> |
|--------------|---------------------|-------------------------------|---------------------------------|
|<span data-ttu-id="e5c38-114">Vé tàu</span><span class="sxs-lookup"><span data-stu-id="e5c38-114">Train fare</span></span>   |<span data-ttu-id="e5c38-115">DKK 578</span><span class="sxs-lookup"><span data-stu-id="e5c38-115">DKK 578</span></span>              |<span data-ttu-id="e5c38-116">DKK 405</span><span class="sxs-lookup"><span data-stu-id="e5c38-116">DKK 405</span></span>                        |<span data-ttu-id="e5c38-117">DKK 173</span><span class="sxs-lookup"><span data-stu-id="e5c38-117">DKK 173</span></span>                          |
|<span data-ttu-id="e5c38-118">Khách sạn</span><span class="sxs-lookup"><span data-stu-id="e5c38-118">Hotel</span></span>         |<span data-ttu-id="e5c38-119">725 EUR</span><span class="sxs-lookup"><span data-stu-id="e5c38-119">EUR 725</span></span>              |<span data-ttu-id="e5c38-120">557 EUR</span><span class="sxs-lookup"><span data-stu-id="e5c38-120">EUR 557</span></span>                        |<span data-ttu-id="e5c38-121">168 EUR</span><span class="sxs-lookup"><span data-stu-id="e5c38-121">EUR 168</span></span>                          |
|<span data-ttu-id="e5c38-122">Bữa ăn</span><span class="sxs-lookup"><span data-stu-id="e5c38-122">Meals</span></span>         |<span data-ttu-id="e5c38-123">346 EUR</span><span class="sxs-lookup"><span data-stu-id="e5c38-123">EUR 346</span></span>              |<span data-ttu-id="e5c38-124">284 EUR</span><span class="sxs-lookup"><span data-stu-id="e5c38-124">EUR 284</span></span>                        |<span data-ttu-id="e5c38-125">62 EUR</span><span class="sxs-lookup"><span data-stu-id="e5c38-125">EUR 62</span></span>                           |



[!INCLUDE[footer-include](../includes/footer-banner.md)]