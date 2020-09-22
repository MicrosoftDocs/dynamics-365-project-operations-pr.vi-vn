---
title: Tại sao giá mặc định về 0 trên thực tế chi phí chi phí?
description: Khắc phục sự cố tại sao giá mặc định về 0 trên thực tế chi phí chi phí?
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/22/2018
ms.topic: article
ms.prod: Project Service
ms.technology: ''
ms.assetid: bc1ebc58-c733-4310-8435-572ed9a9fef9
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 3fb678822877a61d141de75aea29b7d5cdf292c4
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 03/24/2020
ms.locfileid: "3757048"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="c01bb-103">Tại sao giá mặc định về 0 trên thực tế chi phí chi phí?</span><span class="sxs-lookup"><span data-stu-id="c01bb-103">Why is the price defaulting to zero on expense cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="c01bb-104">Câu hỏi thường gặp này áp dụng cho các thực tế chi phí mà lớp giao dịch được đặt là Chi phí và loại giao dịch là Chi phí.</span><span class="sxs-lookup"><span data-stu-id="c01bb-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="c01bb-105">Khắc phục sự cố tỷ lệ chi phí trên thực tế chi phí chi phí</span><span class="sxs-lookup"><span data-stu-id="c01bb-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="c01bb-106">Hãy đến mục nhập chi phí liên quan và đảm bảo rằng có một số tiền trong trường mục nhập chi phí.</span><span class="sxs-lookup"><span data-stu-id="c01bb-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="c01bb-107">Nếu mục nhập chi phí khởi đầu không có trường số tiền được điền thì bạn đã cô lập được vấn đề.</span><span class="sxs-lookup"><span data-stu-id="c01bb-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="c01bb-108">Để giải quyết vấn đề này, hãy tạo lại mục nhập chi phí với một số tiền hợp lệ và phê duyệt mục nhập này.</span><span class="sxs-lookup"><span data-stu-id="c01bb-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>
