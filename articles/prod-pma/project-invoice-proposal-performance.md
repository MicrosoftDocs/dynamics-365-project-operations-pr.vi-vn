---
title: Hiệu suất của đề xuất hóa đơn dự án
description: Chủ đề này cung cấp thông tin về việc cải thiện hiệu suất cho các đề xuất hóa đơn của dự án.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5a14acf51d277b16896d64c4b12ee00bfb326910
ms.sourcegitcommit: 3a4b181be08ef0428104d72b54a3e61ac2782f14
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/17/2021
ms.locfileid: "6269816"
---
# <a name="project-invoice-proposal-performance"></a><span data-ttu-id="08671-103">Hiệu suất của đề xuất hóa đơn dự án</span><span class="sxs-lookup"><span data-stu-id="08671-103">Project invoice proposal performance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="08671-104">Khi tạo một đề xuất hóa đơn mới, bạn có thể gặp phải các vấn đề về hiệu suất do số lượng dự án và tiểu dự án tăng lên.</span><span class="sxs-lookup"><span data-stu-id="08671-104">When you create a new invoice proposal you might encounter performance issues as the number of projects and subprojects increase.</span></span> <span data-ttu-id="08671-105">Để cải thiện hiệu suất, có một tính năng giúp giảm thời gian cần có để tạo một đề xuất hóa đơn mới cho các giao dịch dự án đã đăng.</span><span class="sxs-lookup"><span data-stu-id="08671-105">To improve performance, a feature is available that reduces the time needed to create a new invoice proposal for posted project transactions.</span></span>

## <a name="enable-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="08671-106">Cho phép cải thiện hiệu suất đề xuất hóa đơn</span><span class="sxs-lookup"><span data-stu-id="08671-106">Enable project invoice proposal performance enhancement</span></span>
<span data-ttu-id="08671-107">Để bật tính năng nâng cao hiệu suất đề xuất hóa đơn dự án, hãy hoàn thành các bước sau.</span><span class="sxs-lookup"><span data-stu-id="08671-107">To enable the project invoice proposal performance enhancement feature, complete the following steps.</span></span>

1.  <span data-ttu-id="08671-108">Đi đến **Quản lý tính năng** > **Tất cả**.</span><span class="sxs-lookup"><span data-stu-id="08671-108">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="08671-109">Trong danh sách tính năng, hãy tìm mục **Nâng cao hiệu suất đề xuất hóa đơn dự án**.</span><span class="sxs-lookup"><span data-stu-id="08671-109">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="08671-110">Chọn **Bật ngay**.</span><span class="sxs-lookup"><span data-stu-id="08671-110">Select **Enable now**.</span></span>
3.  <span data-ttu-id="08671-111">Làm mới trình duyệt của bạn, sau đó tạo một đề xuất hóa đơn mới.</span><span class="sxs-lookup"><span data-stu-id="08671-111">Refresh your browser, and then create a new invoice proposal.</span></span>

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="08671-112">Tắt tính năng nâng cao hiệu suất đề xuất hóa đơn dự án</span><span class="sxs-lookup"><span data-stu-id="08671-112">Turn off project invoice proposal performance enhancement</span></span>
<span data-ttu-id="08671-113">Hoàn thành các bước sau để tắt tính năng nâng cao hiệu suất đề xuất hóa đơn dự án.</span><span class="sxs-lookup"><span data-stu-id="08671-113">Complete the following steps to turn off the project invoice proposal performance enhancement.</span></span>

1.  <span data-ttu-id="08671-114">Đi đến **Quản lý tính năng** > **Tất cả**.</span><span class="sxs-lookup"><span data-stu-id="08671-114">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="08671-115">Trong danh sách tính năng, hãy tìm mục **Nâng cao hiệu suất đề xuất hóa đơn dự án**.</span><span class="sxs-lookup"><span data-stu-id="08671-115">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="08671-116">Chọn **Vô hiệu hoá**.</span><span class="sxs-lookup"><span data-stu-id="08671-116">Select **Disable**.</span></span>
3.  <span data-ttu-id="08671-117">Làm mới trình duyệt của bạn.</span><span class="sxs-lookup"><span data-stu-id="08671-117">Refresh your browser.</span></span>

> [!NOTE]
> <span data-ttu-id="08671-118">Không thể áp dụng hiệu suất đề xuất hóa đơn khi các quy tắc thanh toán được bật.</span><span class="sxs-lookup"><span data-stu-id="08671-118">Invoice proposal performance can't be applied when billing rules are enabled.</span></span>
> 
> <span data-ttu-id="08671-119">Trong quá trình hàng loạt để tạo đề xuất hóa đơn, số lượng nhiệm vụ phụ sẽ chia nhỏ các nhiệm vụ thành số lượng tối đa dựa trên số lượng hợp đồng có giao dịch có thể lập hóa đơn, bất kể bạn đã nhập những gì.</span><span class="sxs-lookup"><span data-stu-id="08671-119">During the batch process to create invoice proposals, the number of subtasks will split the tasks to a maximum number based on the number of contracts with invoiceable transactions, regardless of what you have entered.</span></span> <span data-ttu-id="08671-120">Ví dụ: nếu bạn nhập **3** đối với số lượng nhiệm vụ phụ để tạo đề xuất hóa đơn hàng loạt và chỉ có hai hợp đồng với các giao dịch có thể lập hóa đơn, chỉ có hai nhiệm vụ phụ được tạo.</span><span class="sxs-lookup"><span data-stu-id="08671-120">For example, if you enter **3** for the number of subtasks for invoice proposal creation in batch, and there are only two contracts with invoiceable transactions, only two subtasks are created.</span></span>
