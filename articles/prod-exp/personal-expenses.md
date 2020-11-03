---
title: Chi phí cá nhân trên báo cáo chi phí
description: Chủ đề này giải thích hai phương pháp để xử lý chi phí cá nhân của nhân viên trong Microsoft Dynamics 365 Finance.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 825b6c131c8a65b99d5b7ebdadcd6389886f2d11
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087257"
---
# <a name="personal-expenses-on-an-expense-report"></a><span data-ttu-id="2c3aa-103">Chi phí cá nhân trên báo cáo chi phí</span><span class="sxs-lookup"><span data-stu-id="2c3aa-103">Personal expenses on an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2c3aa-104">Trong thời gian đi công tác, đôi khi nhân viên có thể chi trả các chi phí cá nhân vào thẻ tín dụng công ty của họ.</span><span class="sxs-lookup"><span data-stu-id="2c3aa-104">During business travel, workers might sometimes charge personal expenses to their corporate credit cards.</span></span> <span data-ttu-id="2c3aa-105">Nếu bạn không xác định quy trình xử lý chi phí cá nhân, quy trình phê duyệt báo cáo chi phí có thể bị ảnh hưởng khi nhân viên gửi báo cáo chi phí theo từng khoản của họ.</span><span class="sxs-lookup"><span data-stu-id="2c3aa-105">If you don't define a process for handling personal expenses, the approval process for expense reports might be disrupted when workers submit their itemized expense reports.</span></span> 

<span data-ttu-id="2c3aa-106">Có hai phương pháp để xử lý chi phí cá nhân của nhân viên:</span><span class="sxs-lookup"><span data-stu-id="2c3aa-106">There are two methods for handling a worker's personal expenses:</span></span>

- <span data-ttu-id="2c3aa-107">**Do nhân viên trả** – Tổ chức của bạn không thanh toán các chi phí cá nhân xuất hiện trên hóa đơn cho thẻ tín dụng công ty.</span><span class="sxs-lookup"><span data-stu-id="2c3aa-107">**Paid by employee** – Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="2c3aa-108">Thay vào đó, tổ chức sẽ tạo ra một báo cáo hiển thị chi phí cá nhân cùng với chi phí của công ty đã được tính vào thẻ tín dụng của công ty.</span><span class="sxs-lookup"><span data-stu-id="2c3aa-108">Instead, it creates a report that shows personal expenses together with the corporate expenses that were charged to the corporate credit card.</span></span>
- <span data-ttu-id="2c3aa-109">**Do công ty trả** – Tổ chức của bạn thanh toán toàn bộ hóa đơn cho thẻ tín dụng công ty, sau đó tính các khoản chi phí cá nhân vào tài khoản của nhân viên.</span><span class="sxs-lookup"><span data-stu-id="2c3aa-109">**Paid by company** – Your organization pays the whole bill for the corporate credit card and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="2c3aa-110">Bạn có thể chọn phương pháp mà tổ chức sẽ sử dụng trên trang **Các tham số quản lý chi phí**.</span><span class="sxs-lookup"><span data-stu-id="2c3aa-110">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>
