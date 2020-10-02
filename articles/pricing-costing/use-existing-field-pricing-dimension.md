---
title: Các trường Project Operations làm thông số định giá
description: Chủ đề này cung cấp thông tin sử dụng các trường làm thông số định giá trong Dynamics 365 Project Operations.
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
ms.openlocfilehash: 3ddf3098e45fdc9b99067b64df05e2adc0b6ad05
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896442"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a><span data-ttu-id="515fa-103">Các trường Project Operations làm thông số định giá</span><span class="sxs-lookup"><span data-stu-id="515fa-103">Project Operations fields as pricing dimensions</span></span>

<span data-ttu-id="515fa-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="515fa-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="515fa-105">Thực thể **Thực tế** có nhiều trường có thể dùng làm thông số định giá để định giá dựa trên nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="515fa-105">The **Actuals** entity has many fields that can be used as pricing dimensions for resource-based pricing.</span></span> <span data-ttu-id="515fa-106">Ví dụ: một trường thường gặp là **Nguồn lực có thể đặt**.</span><span class="sxs-lookup"><span data-stu-id="515fa-106">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="515fa-107">Các công ty nhỏ hơn có ít hơn 20-30 nguồn lực có thể tính phí có thể thấy rằng việc có tỷ lệ chi phí và hóa đơn cụ thể cho từng nguồn lực là cách tiếp cận đơn giản hơn.</span><span class="sxs-lookup"><span data-stu-id="515fa-107">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="515fa-108">Tuy nhiên, khi lực lượng lao động có thể thanh toán tăng lên, tỷ lệ dành riêng cho nguồn lực có thể không duy trì được do không thực tế.</span><span class="sxs-lookup"><span data-stu-id="515fa-108">However, as the billable workforce grows, resource-secific rates could become unrealistic to maintain.</span></span> <span data-ttu-id="515fa-109">Chi phí nguồn lực và mức tính phí bắt đầu thay đổi khi nguồn lực được thăng chức, có thêm kinh nghiệm hoặc có được các bộ kỹ năng khác nhau.</span><span class="sxs-lookup"><span data-stu-id="515fa-109">Resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different set of skills.</span></span> 

<span data-ttu-id="515fa-110">Một ví dụ khác là đối với loại giao dịch.</span><span class="sxs-lookup"><span data-stu-id="515fa-110">Another example is that of transaction category.</span></span> <span data-ttu-id="515fa-111">Khách hàng và Người thực hiện đã sử dụng loại giao dịch để phân loại công việc và sử dụng trường để định giá và chi phí dựa trên loại công việc.</span><span class="sxs-lookup"><span data-stu-id="515fa-111">Customers and Implementers have used the transaction category to classify work and use the field to price and cost based on the category of work.</span></span>
