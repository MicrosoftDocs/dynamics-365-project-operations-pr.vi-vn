---
title: Tại sao giá mặc định về 0 trên thực tế chi phí chi phí?
description: Khắc phục sự cố tại sao giá mặc định về 0 trên thực tế chi phí chi phí?
author: rumant
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: f6ea664f9f38621ce5d1b0dd033d7df491f845ff
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146374"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="f93d5-103">Tại sao giá mặc định về 0 trên thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="f93d5-103">Why is the price defaulting to zero on expense cost actuals</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="f93d5-104">Câu hỏi thường gặp này áp dụng cho các thực tế chi phí mà lớp giao dịch được đặt là Chi phí và loại giao dịch là Chi phí.</span><span class="sxs-lookup"><span data-stu-id="f93d5-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="f93d5-105">Khắc phục sự cố tỷ lệ chi phí trên thực tế chi phí chi phí</span><span class="sxs-lookup"><span data-stu-id="f93d5-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="f93d5-106">Hãy đến mục nhập chi phí liên quan và đảm bảo rằng có một số tiền trong trường mục nhập chi phí.</span><span class="sxs-lookup"><span data-stu-id="f93d5-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="f93d5-107">Nếu mục nhập chi phí khởi đầu không có trường số tiền được điền thì bạn đã cô lập được vấn đề.</span><span class="sxs-lookup"><span data-stu-id="f93d5-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="f93d5-108">Để giải quyết vấn đề này, hãy tạo lại mục nhập chi phí với một số tiền hợp lệ và phê duyệt mục nhập này.</span><span class="sxs-lookup"><span data-stu-id="f93d5-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>
