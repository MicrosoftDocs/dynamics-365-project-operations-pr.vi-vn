---
title: Mô tả hợp đồng dựa trên chi phí sản phẩm - bản đơn giản
description: Chủ đề này cung cấp thông tin về việc tạo
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a81c972f36179621f0547c24fc53d294485f638c
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764485"
---
# <a name="cost-product-based-contract-lines---lite"></a><span data-ttu-id="f521f-103">Mô tả hợp đồng dựa trên chi phí sản phẩm - bản đơn giản</span><span class="sxs-lookup"><span data-stu-id="f521f-103">Cost product-based contract lines - lite</span></span>

<span data-ttu-id="f521f-104">_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="f521f-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="f521f-105">Mô tả hợp đồng dựa trên dự án trong Dynamics 365 Project Operations bao gồm trường **Giá vốn**, trường này chỉ giá vốn của sản phẩm để tính toán lợi nhuận xuôi dòng.</span><span class="sxs-lookup"><span data-stu-id="f521f-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="f521f-106">Khi mục mô tả hợp đồng dựa trên sản phẩm được tạo cho một sản phẩm trong danh mục, chi phí trong mô tả mặc định từ trường **Chi phí tiêu chuẩn** trong danh mục sản phẩm.</span><span class="sxs-lookup"><span data-stu-id="f521f-106">When a product-based contract line is created for a catalog product, the cost of the line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="f521f-107">Trường **Chi phí tiêu chuẩn** trong danh mục sản phẩm được thiết lập theo đơn vị tiền tệ cơ sở của tổ chức.</span><span class="sxs-lookup"><span data-stu-id="f521f-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="f521f-108">Khi chi phí đơn vị được lấy mặc định trên mục mô tả hợp đồng, giá trị này được chuyển đổi theo đơn vị tiền tệ bán hàng trên hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="f521f-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="f521f-109">Chi phí đơn vị trên mục mô tả hợp đồng dựa trên sản phẩm</span><span class="sxs-lookup"><span data-stu-id="f521f-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="f521f-110">Khi có chi phí đơn vị trên mục mô tả hợp đồng dựa trên sản phẩm, mỗi lần bán đơn vị sẽ có một mục chi phí sản phẩm khác nhau.</span><span class="sxs-lookup"><span data-stu-id="f521f-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="f521f-111">Tuy điều này không phải lúc nào cũng cần thiết, nhưng vẫn có một số trường hợp nhất định mà nhà cung cấp có thể chiết khấu chi phí sản phẩm cho khách hàng.</span><span class="sxs-lookup"><span data-stu-id="f521f-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="f521f-112">Xem xét kịch bản ví dụ sau đây:</span><span class="sxs-lookup"><span data-stu-id="f521f-112">Consider the following scenario:</span></span>

<span data-ttu-id="f521f-113">Fabrikam Robotics lắp đặt các cánh tay rô-bốt tại dây chuyền lắp ráp của Adatum Corporation.</span><span class="sxs-lookup"><span data-stu-id="f521f-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="f521f-114">Tuy Fabrikam cung cấp dịch vụ lắp đặt nhưng cánh tay robot là sản phẩm của Trey Research.</span><span class="sxs-lookup"><span data-stu-id="f521f-114">Fabrikam provides installation services but the robotic arms are from Trey Research.</span></span> <span data-ttu-id="f521f-115">Nếu việc lắp đặt cánh tay rô-bốt tại Adatum Corporation mở ra một ngành mới cho Trey Research, thì công ty này có thể áp dụng chiết khấu đặc biệt cho thỏa thuận này với Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="f521f-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="f521f-116">Trong trường hợp này, Fabrikam tạo một mô tả hợp đồng dựa trên sản phẩm cho Robotic Arms.</span><span class="sxs-lookup"><span data-stu-id="f521f-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms.</span></span> <span data-ttu-id="f521f-117">Chi phí trên đơn vị được nhập cho hợp đồng này.</span><span class="sxs-lookup"><span data-stu-id="f521f-117">A per unit cost is entered for this contract.</span></span> <span data-ttu-id="f521f-118">Chi phí này khác với chi phí của các cánh tay robot từ Trey Research.</span><span class="sxs-lookup"><span data-stu-id="f521f-118">The cost is different from the cost of robotic arms from Trey Research.</span></span>
