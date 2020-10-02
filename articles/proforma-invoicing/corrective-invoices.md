---
title: Hóa đơn hiệu chỉnh
description: Chủ đề này cung cấp thông tin về hóa đơn hiệu chỉnh.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e14da1c07d5b697de6caf1b9041c30581ecff102
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898107"
---
# <a name="corrected-invoices"></a><span data-ttu-id="d463a-103">Hóa đơn hiệu chỉnh</span><span class="sxs-lookup"><span data-stu-id="d463a-103">Corrected invoices</span></span>

<span data-ttu-id="d463a-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="d463a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d463a-105">Có thể chỉnh sửa các hóa đơn đã xác nhận.</span><span class="sxs-lookup"><span data-stu-id="d463a-105">Confirmed invoices can be edited.</span></span> <span data-ttu-id="d463a-106">Khi bạn sửa các hóa đơn đã xác nhận, một hóa đơn hiệu chỉnh ở dạng bản nháp được tạo ra.</span><span class="sxs-lookup"><span data-stu-id="d463a-106">When you edit a confirmed invoice, a draft of the corrected invoice is created.</span></span> <span data-ttu-id="d463a-107">Vì giả định là bạn muốn đảo ngược tất cả giao dịch và số lượng từ hóa đơn ban đầu, hóa đơn hiệu chỉnh bao gồm tất cả giao dịch từ hóa đơn ban đầu và tất cả số lượng trên đó là (0).</span><span class="sxs-lookup"><span data-stu-id="d463a-107">Because the assumption is that you want to reverse all the transactions and quantities from the original invoice, the corrected invoice includes all the transactions from the original invoice, and all the quantities on it are zero (0).</span></span>

<span data-ttu-id="d463a-108">Khi các giao dịch không yêu cầu chỉnh sửa, bạn có thể xóa chúng khỏi hóa đơn hiệu chỉnh ở dạng bản nháp.</span><span class="sxs-lookup"><span data-stu-id="d463a-108">When transactions don't require correction, you can remove them from the draft corrective invoice.</span></span> <span data-ttu-id="d463a-109">Để đảo ngược hoặc chỉ trả lại một phần số lượng, bạn có chỉnh sửa trường Số lượng trên chi tiết dòng.</span><span class="sxs-lookup"><span data-stu-id="d463a-109">To reverse or return only a partial quantity, you can edit the Quantity field on the line detail.</span></span> <span data-ttu-id="d463a-110">Nếu mở chi tiết mô tả hóa đơn, bạn có thể thấy số lượng hóa đơn ban đầu.</span><span class="sxs-lookup"><span data-stu-id="d463a-110">If you open the invoice line detail, you can see the original invoice quantity.</span></span> <span data-ttu-id="d463a-111">Sau đó, bạn có thể chỉnh sửa số lượng hóa đơn hiện tại sao cho ít hơn hoặc nhiều hơn số lượng hóa đơn ban đầu.</span><span class="sxs-lookup"><span data-stu-id="d463a-111">You can then edit the current invoice quantity so that it's less than or more than the original invoice quantity.</span></span>

<span data-ttu-id="d463a-112">Khi bạn xác nhận hóa đơn chỉnh sửa, doanh số bán hàng thực tế được lập hóa đơn ban đầu được đảo ngược và doanh số bán hàng thực tế mới được lập hóa đơn được tạo.</span><span class="sxs-lookup"><span data-stu-id="d463a-112">When you confirm a corrective invoice, the original billed sales actual is reversed, and a new billed sales actual is created.</span></span> <span data-ttu-id="d463a-113">Nếu số lượng giảm, sự khác biệt dẫn đến doanh số bán hàng thực tế mới chưa được lập hóa đơn cũng được tạo.</span><span class="sxs-lookup"><span data-stu-id="d463a-113">If the quantity was reduced, the difference will cause a new unbilled sales actual to be created too.</span></span> <span data-ttu-id="d463a-114">Ví dụ: nếu doanh số bán hàng ban đầu được lập hóa đơn là trong 8 giờ, thì chi tiết mô tả hóa đơn hiệu chỉnh có số lượng giảm là 6 giờ, dòng bán hàng ban đầu được lập hóa đơn bị đảo và tạo 2 doanh số bán hàng thực tế mới:</span><span class="sxs-lookup"><span data-stu-id="d463a-114">For example, if the original billed sale was for eight hours, and the corrected invoice line detail has a reduced quantity of six hours, the original billed sales line is revered and two new actuals are created:</span></span>

- <span data-ttu-id="d463a-115">Doanh số bán hàng thực tế được lập hóa đơn cho 6 giờ.</span><span class="sxs-lookup"><span data-stu-id="d463a-115">A billed sales actual for six hours.</span></span>
- <span data-ttu-id="d463a-116">Doanh số bán hàng thực tế được lập hóa đơn cho 2 giờ còn lại.</span><span class="sxs-lookup"><span data-stu-id="d463a-116">An unbilled sales actual for the remaining two hours.</span></span> <span data-ttu-id="d463a-117">Giao dịch này có thể được lập hóa đơn sau hoặc đánh dấu là không tính phí, tùy thuộc vào các cuộc đàm phán với khách hàng.</span><span class="sxs-lookup"><span data-stu-id="d463a-117">This transaction can either be billed later or marked as non-chargeable, depending on the negotiations with the customer.</span></span>
