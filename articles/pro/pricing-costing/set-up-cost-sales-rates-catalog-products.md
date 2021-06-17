---
title: Thiết lập chi phí và tỷ lệ bán hàng cho sản phẩm trên danh mục – bản đơn giản
description: Chủ đề này cung cấp thông tin về cách thiết lập chi phí và tỷ lệ bán hàng cho các mặt hàng trong danh mục sản phẩm.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4995859696c844e99593139f63dffbf86a52f2f0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004371"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="b32c9-103">Thiết lập chi phí và tỷ lệ bán hàng cho sản phẩm trên danh mục – bản đơn giản</span><span class="sxs-lookup"><span data-stu-id="b32c9-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="b32c9-104">_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="b32c9-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="b32c9-105">Cách thiết lập giá cho các mục thuộc danh mục sản phẩm trong Dynamics 365 Project Operations cũng giống như trong Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="b32c9-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="b32c9-106">Trong Project Operations, bạn không thể ước tính hoặc sử dụng sản phẩm trên dự án, nên không cần thiết lập giá của danh mục sản phẩm trên bảng giá dự án đối với báo giá và hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="b32c9-106">In Project Operations, products can't be estimated or used on projects, so product catalog prices don't need to be set on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="b32c9-107">Sử dụng trường **Giá sản phẩm** của một báo giá, hợp đồng hoặc tài khoản để thiết lập giá của danh mục sản phẩm.</span><span class="sxs-lookup"><span data-stu-id="b32c9-107">Use the **Product Price** field of a quote, contract, or account to set up product catalog prices.</span></span> <span data-ttu-id="b32c9-108">Không nên thiết lập giá của danh mục sản phẩm trong bảng giá dự án.</span><span class="sxs-lookup"><span data-stu-id="b32c9-108">Don't set up product catalog prices in the project price lists.</span></span> <span data-ttu-id="b32c9-109">Bảng giá dự án dành riêng cho Project Operations.</span><span class="sxs-lookup"><span data-stu-id="b32c9-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="b32c9-110">Logic kinh doanh dành riêng cho ứng dụng sẽ sao chép bảng giá từ báo giá sang hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="b32c9-110">Application-specific business logic copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="b32c9-111">Kết quả là bảng giá dự án theo hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="b32c9-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="b32c9-112">Thao tác sao chép có thể trì hoãn quá trình nhận được báo giá nếu bảng giá dự án trên báo giá quá lớn.</span><span class="sxs-lookup"><span data-stu-id="b32c9-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="b32c9-113">Bảng giá sản phẩm không được sao chép để tạo bảng giá tùy chỉnh trên hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="b32c9-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="b32c9-114">Do không có hoạt động sao chép nào liên quan, nên hiệu quả của quy trình báo giá không bị ảnh hưởng.</span><span class="sxs-lookup"><span data-stu-id="b32c9-114">Because there's no copying involved, the performance of the quote process isn't affected.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]