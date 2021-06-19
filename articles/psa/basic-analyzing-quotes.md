---
title: Phân tích báo giá dự án
description: Chủ đề này cung cấp thông tin về phân tích báo giá dự án.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: acb3f1a2020cfd59f60f828e9092bd7ccde00077
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012477"
---
# <a name="analysis-of-project-quotes"></a><span data-ttu-id="46412-103">Phân tích báo giá dự án</span><span class="sxs-lookup"><span data-stu-id="46412-103">Analysis of project quotes</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="46412-104">Dynamics 365 Project Service Automation phân tích báo giá dự án để ước tính lợi nhuận.</span><span class="sxs-lookup"><span data-stu-id="46412-104">Dynamics 365 Project Service Automation analyzes project quotes to estimate profitability.</span></span> <span data-ttu-id="46412-105">Nó cũng phân tích xem báo cáo thống nhất như thế nào với kỳ vọng của khách hàng về ngày giao hàng hoặc ngày hoàn thành và về ngân sách.</span><span class="sxs-lookup"><span data-stu-id="46412-105">It also analyzes how well the quote is aligned with customer expectations about the delivery date or completion date, and about the budget.tions.</span></span>

## <a name="profitability-analysis"></a><span data-ttu-id="46412-106">Phân tích suất sinh lợi</span><span class="sxs-lookup"><span data-stu-id="46412-106">Profitability analysis</span></span>

<span data-ttu-id="46412-107">Project Service Automation phân tích suất sinh lợi bằng cách sử dụng lãi gộp và lãi gộp điều chỉnh.</span><span class="sxs-lookup"><span data-stu-id="46412-107">Project Service Automation analyzes profitability by using the gross margin and the adjusted gross margin.</span></span>

- <span data-ttu-id="46412-108">Lãi gộp được tính bằng cách sử dụng công thức sau đây:</span><span class="sxs-lookup"><span data-stu-id="46412-108">Gross margins are calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- <span data-ttu-id="46412-109">Lãi gộp điều chỉnh được tính bằng cách sử dụng công thức sau đây:</span><span class="sxs-lookup"><span data-stu-id="46412-109">The adjusted gross margin is calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

<span data-ttu-id="46412-110">Nếu giá trị cho lãi gộp và lãi gộp điều chỉnh khác với lãi chung, thì hầu hết công việc trong báo giá được phân loại là không thể tính phí.</span><span class="sxs-lookup"><span data-stu-id="46412-110">If the values for gross margin and adjusted gross margin differ by a wide margin, much of the work in the quote is classified as non-chargeable.</span></span>

## <a name="analysis-of-customer-expectations"></a><span data-ttu-id="46412-111">Phân tích kỳ vọng của khách hàng</span><span class="sxs-lookup"><span data-stu-id="46412-111">Analysis of customer expectations</span></span>

<span data-ttu-id="46412-112">Bạn có thể phân tích báo giá và tạo biểu đồ cho kỳ vọng của khách hàng về lịch trình cũng như ngân sách nếu bạn nhập giá trị cho các trường sau:</span><span class="sxs-lookup"><span data-stu-id="46412-112">You can analyze quotes and generate charts for customer expectations about the schedule and budget if you enter values for the following fields:</span></span>

- <span data-ttu-id="46412-113">Trường **Ngày giao hàng yêu cầu** trên tiêu đề báo giá.</span><span class="sxs-lookup"><span data-stu-id="46412-113">The **Requested delivery date** field on the quote header.</span></span>
- <span data-ttu-id="46412-114">Trường **Ngân sách khách hàng** cho mỗi dòng báo giá (đối với các dòng dựa trên dự án và các dòng dựa trên sản phẩm).</span><span class="sxs-lookup"><span data-stu-id="46412-114">The **Customer budget** field for each quote line (for project-based lines and product-based lines).</span></span>

<span data-ttu-id="46412-115">Phân tích các kỳ vọng của khách hàng về lịch trình được thực hiện bằng cách so sánh ngày kết thúc mới nhất của chi tiết dòng báo giá với ngày giao hàng yêu cầu trên tất cả các dòng báo giá trong báo giá.</span><span class="sxs-lookup"><span data-stu-id="46412-115">Analysis of customer expectations about the schedule is done by comparing the latest end date of the quote line detail with the requested delivery date across all quote lines in the quote.</span></span>

<span data-ttu-id="46412-116">Phân tích các kỳ vọng của khách hàng về ngân sách được thực hiện bằng cách so sánh tổng của tổng ngân sách khách hàng với số tiền báo giá trên tất cả các dòng báo giá.</span><span class="sxs-lookup"><span data-stu-id="46412-116">Analysis of customer expectations about the budget is done by comparing the sum of the total customer budget with the quoted amount across all quote lines.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]