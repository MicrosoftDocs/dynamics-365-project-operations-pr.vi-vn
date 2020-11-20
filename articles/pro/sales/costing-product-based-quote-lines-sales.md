---
title: Dòng báo giá dựa trên sản phẩm chi phí
description: Chủ đề này cung cấp thông tin về cách áp dụng giá vốn vào mô tả báo giá dựa trên sản phẩm.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d21ab159294cac66ffeb8abcf0943b4babd7b360
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4118959"
---
# <a name="costing-product-based-quote-lines"></a><span data-ttu-id="a4c4e-103">Dòng báo giá dựa trên sản phẩm chi phí</span><span class="sxs-lookup"><span data-stu-id="a4c4e-103">Costing product-based quote lines</span></span>

<span data-ttu-id="a4c4e-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="a4c4e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="a4c4e-105">Các mô tả báo giá dựa trên sản phẩm trong Dynamics 365 Project Operations cũng có trường **Giá vốn**.</span><span class="sxs-lookup"><span data-stu-id="a4c4e-105">Product-based quote lines in Dynamics 365 Project Operations also have a **Cost Price** field.</span></span> <span data-ttu-id="a4c4e-106">Trường này được sử dụng để theo dõi giá vốn của sản phẩm trên mô tả báo giá và để tính toán lợi nhuận trong tương lai.</span><span class="sxs-lookup"><span data-stu-id="a4c4e-106">This field is used to track the cost price for the product on the quote line and for downstream profitability calculations.</span></span>

<span data-ttu-id="a4c4e-107">Khi mô tả báo giá dựa trên sản phẩm được tạo cho một sản phẩm trong danh mục, chi phí của mô tả báo giá dựa trên sản phẩm được mặc định từ trường **Chi phí tiêu chuẩn** trong danh mục sản phẩm.</span><span class="sxs-lookup"><span data-stu-id="a4c4e-107">When a product-based quote line is created for a catalog product, the cost of the product-based quote line is defaulted from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="a4c4e-108">Trường chi phí tiêu chuẩn trong danh mục sản phẩm được thiết lập theo đơn vị tiền tệ cơ sở của tổ chức.</span><span class="sxs-lookup"><span data-stu-id="a4c4e-108">The standard cost field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="a4c4e-109">Chi phí đơn vị mặc định trên mô tả báo giá dựa trên sản phẩm được chuyển đổi thành đơn vị tiền tệ bán hàng trên báo giá.</span><span class="sxs-lookup"><span data-stu-id="a4c4e-109">The default unit cost on the product-based quote line is converted to the sales currency on the quote.</span></span>

## <a name="unit-cost-on-a-product-based-quote-line"></a><span data-ttu-id="a4c4e-110">Chi phí đơn vị trên mô tả báo giá dựa trên sản phẩm</span><span class="sxs-lookup"><span data-stu-id="a4c4e-110">Unit cost on a product-based quote line</span></span>

<span data-ttu-id="a4c4e-111">Mục đích của việc có chi phí đơn vị trên mô tả báo giá dựa trên sản phẩm là cho phép các chi phí khác nhau cho một sản phẩm cho mỗi lần bán hàng.</span><span class="sxs-lookup"><span data-stu-id="a4c4e-111">The purpose of having a unit cost on a product-based quote line is to allow for different costs for a product for each sale.</span></span> <span data-ttu-id="a4c4e-112">Đây không phải là một kịch bản điển hình, nhưng đôi khi chi phí của sản phẩm có thể được nhà cung cấp chiết khấu tùy thuộc vào khách hàng của đợt bán hàng cuối cùng.</span><span class="sxs-lookup"><span data-stu-id="a4c4e-112">This is not a typical scenario, but sometimes the cost of the product may be discounted by the supplier depending on the customer of the final sale.</span></span>

<span data-ttu-id="a4c4e-113">Ví dụ:</span><span class="sxs-lookup"><span data-stu-id="a4c4e-113">For example:</span></span>

<span data-ttu-id="a4c4e-114">Fabrikam Robotics đang lắp đặt các cánh tay robot tại dây chuyền lắp ráp của A Datum Corporation.</span><span class="sxs-lookup"><span data-stu-id="a4c4e-114">Fabrikam Robotics is installing robotic arms at A Datum Corporation's assembly lines.</span></span> <span data-ttu-id="a4c4e-115">Fabrikam cung cấp dịch vụ lắp đặt nhưng các cánh tay robot được mua từ công ty chế tạo robot Trey.</span><span class="sxs-lookup"><span data-stu-id="a4c4e-115">Fabrikam provides installation services but the robotic arms are procured from Trey robotics.</span></span> <span data-ttu-id="a4c4e-116">Nếu việc lắp đặt cánh tay robot tại A Datum Corporation mở ra một ngành công nghiệp mới cho cánh tay robot của Trey, Trey có thể giảm giá đặc biệt đối với giao dịch này cho Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="a4c4e-116">If the installation of robotic arms at A Datum Corporation opens a new industry vertical for Trey's robotic arms, Trey could give a special discount for this deal to Fabrikam.</span></span>

<span data-ttu-id="a4c4e-117">Trong trường hợp này, Fabrikam sẽ tạo dòng báo giá dựa trên sản phẩm cho cánh tay robot và nhập một chi phí đặc biệt trên mỗi đơn vị cho báo giá này.</span><span class="sxs-lookup"><span data-stu-id="a4c4e-117">In this case, Fabrikam will create product-based quote line for Robotic Arms and input a special per unit cost for this quote.</span></span> <span data-ttu-id="a4c4e-118">Chi phí này khác với chi phí tiêu chuẩn của cánh tay robot Trey.</span><span class="sxs-lookup"><span data-stu-id="a4c4e-118">This cost is different from the standard cost of Trey Robotic Arms.</span></span>
