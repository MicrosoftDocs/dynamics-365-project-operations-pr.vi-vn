---
title: Tại sao giá mặc định về 0 trên thực tế chi phí chi phí?
description: Khắc phục sự cố tại sao giá mặc định về 0 trên thực tế chi phí chi phí?
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/22/2018
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
ms.openlocfilehash: 9f4ff8a96250d675faeda3246c2d0a6c5bd83286
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087129"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="16043-103">Tại sao giá mặc định về 0 trên thực tế chi phí chi phí?</span><span class="sxs-lookup"><span data-stu-id="16043-103">Why is the price defaulting to zero on expense cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="16043-104">Câu hỏi thường gặp này áp dụng cho các thực tế chi phí mà lớp giao dịch được đặt là Chi phí và loại giao dịch là Chi phí.</span><span class="sxs-lookup"><span data-stu-id="16043-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="16043-105">Khắc phục sự cố tỷ lệ chi phí trên thực tế chi phí chi phí</span><span class="sxs-lookup"><span data-stu-id="16043-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="16043-106">Hãy đến mục nhập chi phí liên quan và đảm bảo rằng có một số tiền trong trường mục nhập chi phí.</span><span class="sxs-lookup"><span data-stu-id="16043-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="16043-107">Nếu mục nhập chi phí khởi đầu không có trường số tiền được điền thì bạn đã cô lập được vấn đề.</span><span class="sxs-lookup"><span data-stu-id="16043-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="16043-108">Để giải quyết vấn đề này, hãy tạo lại mục nhập chi phí với một số tiền hợp lệ và phê duyệt mục nhập này.</span><span class="sxs-lookup"><span data-stu-id="16043-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>
