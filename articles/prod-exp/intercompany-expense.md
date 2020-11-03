---
title: Chi phí liên công ty
description: Nhân viên của một pháp nhân trong một tổ chức có thể thực hiện công việc cho một pháp nhân khác trong cùng tổ chức đó. Trong tình huống này, bạn có thể sử dụng tính năng chi phí liên công ty để chỉ định chi phí của nhân viên đó cho pháp nhân có công việc được thực hiện.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087259"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="75960-104">Chi phí liên công ty</span><span class="sxs-lookup"><span data-stu-id="75960-104">Intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="75960-105">Nhân viên của một pháp nhân trong một tổ chức có thể thực hiện công việc cho một pháp nhân khác trong cùng tổ chức đó.</span><span class="sxs-lookup"><span data-stu-id="75960-105">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="75960-106">Trong tình huống này, bạn có thể sử dụng tính năng chi phí liên công ty để chỉ định chi phí của nhân viên đó cho pháp nhân có công việc được thực hiện.</span><span class="sxs-lookup"><span data-stu-id="75960-106">In this situation, you can use the intercompany expense feature to assign the worker’s expenses to the legal entity for which the work was performed.</span></span> <span data-ttu-id="75960-107">Pháp nhân tuyển dụng nhân viên được gọi là pháp nhân cho mượn.</span><span class="sxs-lookup"><span data-stu-id="75960-107">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="75960-108">Pháp nhân chịu trách nhiệm đối với chi phí của nhân viên được gọi là pháp nhân mượn.</span><span class="sxs-lookup"><span data-stu-id="75960-108">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="75960-109">Trước khi nhân viên có thể tạo và gửi chi phí đối với công việc được thực hiện cho một pháp nhân khác, ở phần pháp nhân cho mượn, trên trang **Các tham số quản lý chi phí** , hãy chọn tùy chọn **Cho phép các dòng chi phí liên công ty**.</span><span class="sxs-lookup"><span data-stu-id="75960-109">Before a worker can create and submit expenses for work that is performed for a different legal entity, in the loaning legal entity, on the **Expense management parameters** page, select the **Allow intercompany expense lines** option.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="75960-110">Đăng thuế đối với chi phí liên công ty</span><span class="sxs-lookup"><span data-stu-id="75960-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="75960-111">Nếu bạn muốn sử dụng các nhóm thuế được liên kết với pháp nhân cho mượn (nguồn) thay vì pháp nhân mượn (đích) trong báo cáo chi phí, thì bạn sẽ cần phải đặt cấu hình nhóm thuế này trong phần thiết lập thuế bán hàng trên Sổ Cái.</span><span class="sxs-lookup"><span data-stu-id="75960-111">If you want to use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you will need to configure this in the General ledger sales tax set up.</span></span> <span data-ttu-id="75960-112">Khi tham số trong Sổ Cái **Pháp nhân để đăng thuế liên công ty** được đặt thành **Nguồn** và **Áp dụng các quy tắc đánh thuế bán hàng** được đặt thành **Không** , tổ hợp thuế cho pháp nhân cho mượn sẽ được sử dụng.</span><span class="sxs-lookup"><span data-stu-id="75960-112">When the General ledger parameter, **Legal entity for intercompany tax posting** is set to **Source** and **Apply sales tax taxation rules** is set to **No** , the tax combination for the loaning legal entity will be used.</span></span> <span data-ttu-id="75960-113">Khi tham số đó được đặt thành **Đích** , tổ hợp thuế cho pháp nhân mượn sẽ được sử dụng.</span><span class="sxs-lookup"><span data-stu-id="75960-113">When the same parameter is set to **Destination** , the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="75960-114">Đối với các pháp nhân ở Hoa Kỳ, khi tham số được đặt thành **Nguồn** , trường **Thuế bán hàng phải thu** cũng phải được đặt cấu hình trên trang mới **Nhóm đăng trên Sổ Cái**.</span><span class="sxs-lookup"><span data-stu-id="75960-114">For legal entities in the United States, when the parameter is set to **Source** , the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="75960-115">Công cụ kế toán sẽ sử dụng thông tin ở trường này cho mục nhập kế toán liên quan đến thuế.</span><span class="sxs-lookup"><span data-stu-id="75960-115">The accounting engine will use the information from this field for tax related accounting entry.</span></span>   
<span data-ttu-id="75960-116">Hành vi được thực hiện nhất quán đối với các mục mô tả chi phí được đăng có hoặc không có dự án.</span><span class="sxs-lookup"><span data-stu-id="75960-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  
