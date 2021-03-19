---
title: Sử dụng trường hiện có trong Project Service làm thông số định giá
description: Chủ đề này cung cấp thông tin về cách sử dụng trường Project Service hiện có làm thông số định giá.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: ad03f5f7c1c9e93ca12a8c8d48ffbd2f80b1511f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281594"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a><span data-ttu-id="8efb9-103">Sử dụng trường hiện có trong Project Service làm thông số định giá</span><span class="sxs-lookup"><span data-stu-id="8efb9-103">Use an existing field in Project Service as a pricing dimension</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="8efb9-104">Project Service Automation (PSA) có nhiều trường trên thực thể **Thực tế** có thể dùng làm thông số định giá để định giá dựa trên tài nguyên trong tổ chức dự án.</span><span class="sxs-lookup"><span data-stu-id="8efb9-104">Project Service Automation (PSA) has many fields on the **Actuals** entity that can be used as pricing dimensions for resource-based pricing in project organizations.</span></span> <span data-ttu-id="8efb9-105">Ví dụ: một trường thường gặp là **Nguồn lực có thể đặt**.</span><span class="sxs-lookup"><span data-stu-id="8efb9-105">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="8efb9-106">Các công ty nhỏ hơn có ít hơn 20-30 nguồn lực có thể tính phí có thể thấy rằng việc có tỷ lệ chi phí và hóa đơn cụ thể cho từng nguồn lực là cách tiếp cận đơn giản hơn.</span><span class="sxs-lookup"><span data-stu-id="8efb9-106">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="8efb9-107">Tuy nhiên, khi lực lượng lao động có thể tính phí tăng lên, mức giá cố định có thể trở nên không thực tế vì chi phí nguồn lực và mức tính phí bắt đầu thay đổi khi nguồn lực được thăng chức, có thêm kinh nghiệm hoặc đòi hỏi nhóm kỹ năng khác.</span><span class="sxs-lookup"><span data-stu-id="8efb9-107">However, as the billable workforce grows, specific rates could become unrealistic to maintain as resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different skill set.</span></span> <span data-ttu-id="8efb9-108">Vì cách tiếp cận này vẫn phù hợp với các công ty có quy mô nhất định, hãy xem [Sử dụng nguồn lực có thể đặt trước làm thông số định giá](bookable-resource-pricing-dimension.md) để tìm hiểu cách dùng trường Project Service làm thông số định giá.</span><span class="sxs-lookup"><span data-stu-id="8efb9-108">Because this approach still works for companies of a certain size, see [Use a bookable resource as a pricing dimension](bookable-resource-pricing-dimension.md) to understand how an existing Project Service field can be used as a pricing dimension.</span></span>

<span data-ttu-id="8efb9-109">Một ví dụ khác là đối với loại giao dịch.</span><span class="sxs-lookup"><span data-stu-id="8efb9-109">Another example is that of transaction category.</span></span> <span data-ttu-id="8efb9-110">Khách hàng và Người thực hiện đã sử dụng loại giao dịch trong PSA để phân loại công việc và sử dụng trường để định giá và chi phí dựa trên loại công việc.</span><span class="sxs-lookup"><span data-stu-id="8efb9-110">Customers and Implementers have used the transaction category in PSA to classify work and use the field to price and cost based on the category of work.</span></span> <span data-ttu-id="8efb9-111">Để biết thêm thông tin, hãy xem [Sử dụng loại giao dịch làm thông số định giá](transaction-category-pricing-dimension.md).</span><span class="sxs-lookup"><span data-stu-id="8efb9-111">For more information, see [Use transaction category as a pricing dimension](transaction-category-pricing-dimension.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]