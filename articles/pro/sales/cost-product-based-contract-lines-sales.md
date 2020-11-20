---
title: Mô tả hợp đồng dựa trên chi phí sản phẩm - bản đơn giản
description: Chủ đề này cung cấp thông tin về việc tạo
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0e961bcf32a5dd662b7cd27a23eb5f664c45c292
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177268"
---
# <a name="cost-product-based-contract-lines---lite"></a><span data-ttu-id="c1697-103">Mô tả hợp đồng dựa trên chi phí sản phẩm - bản đơn giản</span><span class="sxs-lookup"><span data-stu-id="c1697-103">Cost product-based contract lines - lite</span></span>

<span data-ttu-id="c1697-104">_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="c1697-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="c1697-105">Các mục mô tả hợp đồng dựa trên sản phẩm trong Dynamics 365 Project Operations có trường **Giá vốn**, đây là trường lưu trữ giá vốn của sản phẩm để tính toán lợi nhuận xuôi tuyến.</span><span class="sxs-lookup"><span data-stu-id="c1697-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="c1697-106">Khi mục mô tả hợp đồng dựa trên sản phẩm được tạo cho một sản phẩm trong danh mục, chi phí của mục mô tả hợp đồng dựa trên sản phẩm đó được lấy mặc định từ trường **Chi phí tiêu chuẩn** trong danh mục sản phẩm.</span><span class="sxs-lookup"><span data-stu-id="c1697-106">When a product-based contract line is created for a catalog product, the cost of the product-based contract line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="c1697-107">Trường **Chi phí tiêu chuẩn** trong danh mục sản phẩm được thiết lập theo đơn vị tiền tệ cơ sở của tổ chức.</span><span class="sxs-lookup"><span data-stu-id="c1697-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="c1697-108">Khi chi phí đơn vị được lấy mặc định trên mục mô tả hợp đồng, giá trị này được chuyển đổi theo đơn vị tiền tệ bán hàng trên hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="c1697-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="c1697-109">Chi phí đơn vị trên mục mô tả hợp đồng dựa trên sản phẩm</span><span class="sxs-lookup"><span data-stu-id="c1697-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="c1697-110">Khi có chi phí đơn vị trên mục mô tả hợp đồng dựa trên sản phẩm, mỗi lần bán đơn vị sẽ có một mục chi phí sản phẩm khác nhau.</span><span class="sxs-lookup"><span data-stu-id="c1697-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="c1697-111">Tuy điều này không phải lúc nào cũng cần thiết, nhưng vẫn có một số trường hợp nhất định mà nhà cung cấp có thể chiết khấu chi phí sản phẩm cho khách hàng.</span><span class="sxs-lookup"><span data-stu-id="c1697-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="c1697-112">Xem xét kịch bản ví dụ sau đây:</span><span class="sxs-lookup"><span data-stu-id="c1697-112">Consider the following scenario:</span></span>

<span data-ttu-id="c1697-113">Fabrikam Robotics lắp đặt các cánh tay rô-bốt tại dây chuyền lắp ráp của Adatum Corporation.</span><span class="sxs-lookup"><span data-stu-id="c1697-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="c1697-114">Fabrikam cung cấp dịch vụ lắp đặt nhưng các cánh tay rô-bốt được mua từ Trey Research.</span><span class="sxs-lookup"><span data-stu-id="c1697-114">Fabrikam provides installation services but the robotic arms are procured from Trey Research.</span></span> <span data-ttu-id="c1697-115">Nếu việc lắp đặt cánh tay rô-bốt tại Adatum Corporation mở ra một ngành mới cho Trey Research, thì công ty này có thể áp dụng chiết khấu đặc biệt cho thỏa thuận này với Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="c1697-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="c1697-116">Trong trường hợp này, Fabrikam tạo một mục mo tả hợp đồng dựa trên sản phẩm cho Robotic Arms và nhập chi phí trên đơn vị cho hợp đồng này khác với chi phí tiêu chuẩn cho cánh tay rô-bốt của Trey Research.</span><span class="sxs-lookup"><span data-stu-id="c1697-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms and inputs a per unit cost for this contract that is different from the standard cost of robotic arms from Trey Research.</span></span>
