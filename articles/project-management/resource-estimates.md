---
title: Ước tính nguồn lực
description: Chủ đề này cung cấp thông tin về cách tính ước tính nguồn lực trong Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 98a61746f172b50bf6fa29cb0d21462cd616f417
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286544"
---
# <a name="resource-estimates"></a><span data-ttu-id="eb9a8-103">Ước tính nguồn lực</span><span class="sxs-lookup"><span data-stu-id="eb9a8-103">Resource estimates</span></span>

<span data-ttu-id="eb9a8-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="eb9a8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="eb9a8-105">Ước tính nguồn lực đến từ nhân công theo từng giai đoạn thời gian được xác định trong cấu trúc phân tích công việc cùng với các thứ nguyên giá áp dụng.</span><span class="sxs-lookup"><span data-stu-id="eb9a8-105">Resource estimates come from time-phased effort that is defined in the work breakdown structure along with applicable pricing dimensions.</span></span> <span data-ttu-id="eb9a8-106">Thông thường, phép tính là **tốc độ/giờ cho mỗi vai trò x giờ.**</span><span class="sxs-lookup"><span data-stu-id="eb9a8-106">Typically, the calculation is **rate/hr for each role x hours.**</span></span> <span data-ttu-id="eb9a8-107">Nhân công theo giai đoạn thời gian cho mỗi nguồn lực được lưu trữ trong bản ghi gán nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="eb9a8-107">The time-phased effort for each resource is stored in the resource assignment record.</span></span> <span data-ttu-id="eb9a8-108">Giá được lưu trữ trong một bảng giá được xác định trước.</span><span class="sxs-lookup"><span data-stu-id="eb9a8-108">The pricing is stored in a pre-defined price list.</span></span> <span data-ttu-id="eb9a8-109">Quy đổi đơn vị được áp dụng dựa trên bảng giá áp dụng.</span><span class="sxs-lookup"><span data-stu-id="eb9a8-109">Unit conversion is applied based on the applicable price list.</span></span>

![Ước tính nguồn lực](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="eb9a8-111">Loại tiền tệ chi phí và giá vốn mặc định</span><span class="sxs-lookup"><span data-stu-id="eb9a8-111">Default cost price and cost currency</span></span>

<span data-ttu-id="eb9a8-112">Giá vốn được mặc định từ Đơn vị tổ chức.</span><span class="sxs-lookup"><span data-stu-id="eb9a8-112">Cost prices are defaulted from the Organizational Unit.</span></span>

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="eb9a8-113">Loại tiền tệ bán hàng và tỷ lệ thanh toán mặc định</span><span class="sxs-lookup"><span data-stu-id="eb9a8-113">Default bill rate and sales currency</span></span>

<span data-ttu-id="eb9a8-114">Giá bán hàng được áp dụng một lần cho mỗi thỏa thuận.</span><span class="sxs-lookup"><span data-stu-id="eb9a8-114">Sales prices are applied once per deal.</span></span> <span data-ttu-id="eb9a8-115">Hệ thống cấp bậc cho bảng giá ưu đãi mặc định như sau:</span><span class="sxs-lookup"><span data-stu-id="eb9a8-115">The hierarchy for sale price list defaulting is as follows:</span></span>

1. <span data-ttu-id="eb9a8-116">Tổ chức</span><span class="sxs-lookup"><span data-stu-id="eb9a8-116">Organization</span></span>
2. <span data-ttu-id="eb9a8-117">Khách hàng</span><span class="sxs-lookup"><span data-stu-id="eb9a8-117">Customer</span></span>
3. <span data-ttu-id="eb9a8-118">Báo giá/hợp đồng</span><span class="sxs-lookup"><span data-stu-id="eb9a8-118">Quote/contract</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]