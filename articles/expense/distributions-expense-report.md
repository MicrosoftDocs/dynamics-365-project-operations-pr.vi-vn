---
title: Phân phối trên báo cáo chi phí
description: Khi nhập chi phí trên báo cáo chi phí, bạn có thể phân bổ chúng cho nhiều dự án, pháp nhân hoặc tài khoản trong tổ chức của mình.
author: suvaidya
manager: AnnBe
ms.date: 10/10/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: a1fa7383e7715fe57380de0a006ccc4e020bb5a5
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086989"
---
# <a name="distributions-on-an-expense-report"></a><span data-ttu-id="43e4c-103">Phân phối trên báo cáo chi phí</span><span class="sxs-lookup"><span data-stu-id="43e4c-103">Distributions on an expense report</span></span>

<span data-ttu-id="43e4c-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_</span><span class="sxs-lookup"><span data-stu-id="43e4c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="43e4c-105">Khi nhập chi phí trên báo cáo chi phí, bạn có thể phân bổ chúng cho nhiều dự án, lĩnh vực tài chính hoặc tài khoản trong tổ chức của mình.</span><span class="sxs-lookup"><span data-stu-id="43e4c-105">When you enter expenses on an expense report, you can distribute them across multiple projects, financial dimensions, or accounts in your organization.</span></span>

<span data-ttu-id="43e4c-106">Ví dụ: Nancy, một đại diện bán hàng của Fabrikam, đã đi từ Copenhagen đến Frankfurt.</span><span class="sxs-lookup"><span data-stu-id="43e4c-106">For example, Nancy, a Fabrikam sales representative, traveled from Copenhagen to Frankfurt.</span></span> <span data-ttu-id="43e4c-107">Tại Frankfurt, Nancy đã gặp hai tổ chức để thảo luận về các dự án riêng biệt cho từng tổ chức.</span><span class="sxs-lookup"><span data-stu-id="43e4c-107">In Frankfurt, Nancy met with two organizations to discuss separate projects for each organization.</span></span> <span data-ttu-id="43e4c-108">Nancy đã dành 7 ngày làm việc với tổ chức A về dự án A và 3 ngày làm việc với tổ chức B về dự án B.</span><span class="sxs-lookup"><span data-stu-id="43e4c-108">Nancy spent seven business days working with organization A on project A, and three business days working with organization B on project B.</span></span>

<span data-ttu-id="43e4c-109">Bởi vì Nancy đã làm việc cho 2 dự án riêng biệt khi ở Frankfurt, khi cô ấy nhập báo cáo chi phí, Nancy phân bổ các chi phí phù hợp cho từng dự án.</span><span class="sxs-lookup"><span data-stu-id="43e4c-109">Because Nancy worked on two separate projects while was in Frankfurt, when she enters the expense report, Nancy distributes the expenses as appropriate for each project.</span></span> <span data-ttu-id="43e4c-110">Bảng sau đây cho thấy cách Nancy phân bổ chi phí.</span><span class="sxs-lookup"><span data-stu-id="43e4c-110">The following table shows how Nancy distributed the expenses.</span></span>

| <span data-ttu-id="43e4c-111">Loại chi phí</span><span class="sxs-lookup"><span data-stu-id="43e4c-111">Expense type</span></span> | <span data-ttu-id="43e4c-112">Tổng số tiền chi phí</span><span class="sxs-lookup"><span data-stu-id="43e4c-112">Total expense amount</span></span> | <span data-ttu-id="43e4c-113">Số tiền phân bổ cho dự án A</span><span class="sxs-lookup"><span data-stu-id="43e4c-113">Amount distributed to project A</span></span> | <span data-ttu-id="43e4c-114">Số tiền phân bổ cho dự án B</span><span class="sxs-lookup"><span data-stu-id="43e4c-114">Amount distributed to project B</span></span> |
|--------------|----------------------|---------------------------------|---------------------------------|
| <span data-ttu-id="43e4c-115">Vé tàu</span><span class="sxs-lookup"><span data-stu-id="43e4c-115">Train fare</span></span>   | <span data-ttu-id="43e4c-116">DKK 578</span><span class="sxs-lookup"><span data-stu-id="43e4c-116">DKK 578</span></span>              | <span data-ttu-id="43e4c-117">DKK 405</span><span class="sxs-lookup"><span data-stu-id="43e4c-117">DKK 405</span></span>                         | <span data-ttu-id="43e4c-118">DKK 173</span><span class="sxs-lookup"><span data-stu-id="43e4c-118">DKK 173</span></span>                         |
| <span data-ttu-id="43e4c-119">Khách sạn</span><span class="sxs-lookup"><span data-stu-id="43e4c-119">Hotel</span></span>        | <span data-ttu-id="43e4c-120">725 EUR</span><span class="sxs-lookup"><span data-stu-id="43e4c-120">EUR 725</span></span>              | <span data-ttu-id="43e4c-121">557 EUR</span><span class="sxs-lookup"><span data-stu-id="43e4c-121">EUR 557</span></span>                         | <span data-ttu-id="43e4c-122">168 EUR</span><span class="sxs-lookup"><span data-stu-id="43e4c-122">EUR 168</span></span>                         |
| <span data-ttu-id="43e4c-123">Bữa ăn</span><span class="sxs-lookup"><span data-stu-id="43e4c-123">Meals</span></span>        | <span data-ttu-id="43e4c-124">346 EUR</span><span class="sxs-lookup"><span data-stu-id="43e4c-124">EUR 346</span></span>              | <span data-ttu-id="43e4c-125">284 EUR</span><span class="sxs-lookup"><span data-stu-id="43e4c-125">EUR 284</span></span>                         | <span data-ttu-id="43e4c-126">62 EUR</span><span class="sxs-lookup"><span data-stu-id="43e4c-126">EUR 62</span></span>                          |
