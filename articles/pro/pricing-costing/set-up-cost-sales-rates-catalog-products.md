---
title: Thiết lập chi phí và tỷ lệ bán hàng cho các sản phẩm danh mục
description: Chủ đề này cung cấp thông tin về cách thiết lập chi phí và tỷ lệ bán hàng cho các mặt hàng trong danh mục sản phẩm.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5178a9143536bf4b2573403125325017861cdd5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087175"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products"></a><span data-ttu-id="32dbe-103">Thiết lập chi phí và tỷ lệ bán hàng cho các sản phẩm danh mục</span><span class="sxs-lookup"><span data-stu-id="32dbe-103">Set up cost and sales rates for catalog products</span></span>

<span data-ttu-id="32dbe-104">_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="32dbe-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="32dbe-105">Thiết lập giá cho các mặt hàng trong danh mục sản phẩm trong Dynamics 365 Project Operations giống như trong Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="32dbe-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="32dbe-106">Vì không thể ước tính hoặc sử dụng sản phẩm cho các dự án trong Project Operations, nên không cần đặt giá danh mục sản phẩm trên bảng giá dự án cho báo giá và hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="32dbe-106">Because products can't be estimated or used on projects in Project Operations, there is no need to set product catalog prices on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="32dbe-107">Giá danh mục sản phẩm nên được thiết lập trong trường **Giá sản phẩm** của báo giá, hợp đồng hoặc tài khoản.</span><span class="sxs-lookup"><span data-stu-id="32dbe-107">Product catalog prices should be set up in the **Product Price** field of a quote, contract, or account.</span></span> <span data-ttu-id="32dbe-108">Không thiết lập giá danh mục sản phẩm trong bảng giá dự án cho những thực thể này.</span><span class="sxs-lookup"><span data-stu-id="32dbe-108">Don't set up product catalog prices in the project price lists for these entities.</span></span> <span data-ttu-id="32dbe-109">Bảng giá dự án dành riêng cho Project Operations.</span><span class="sxs-lookup"><span data-stu-id="32dbe-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="32dbe-110">Có logic nghiệp vụ dành riêng cho ứng dụng sao chép bảng giá từ báo giá sang hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="32dbe-110">There is application-specific business logic that copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="32dbe-111">Kết quả là bảng giá dự án theo hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="32dbe-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="32dbe-112">Thao tác sao chép có thể trì hoãn quá trình nhận được báo giá nếu bảng giá dự án trên báo giá quá lớn.</span><span class="sxs-lookup"><span data-stu-id="32dbe-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="32dbe-113">Bảng giá sản phẩm không được sao chép để tạo bảng giá tùy chỉnh trên hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="32dbe-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="32dbe-114">Điều này có nghĩa là bảng giá sản phẩm không ảnh hưởng đến hiệu suất của quá trình nhận được báo giá.</span><span class="sxs-lookup"><span data-stu-id="32dbe-114">This means that product price lists don't impact the performance of the quote win process.</span></span>
