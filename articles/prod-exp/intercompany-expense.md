---
title: Chi phí liên công ty
description: Chủ đề này cung cấp thông tin về cách sử dụng chi phí liên công ty để chỉ định chi phí của nhân viên cho pháp nhân yêu cầu thực hiện công việc.
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
ms.openlocfilehash: d908a1c062f5b7f01cf340dcd6f7f24714a992bf
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271559"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="9cfdf-103">Chi phí liên công ty</span><span class="sxs-lookup"><span data-stu-id="9cfdf-103">Intercompany expenses</span></span>

<span data-ttu-id="9cfdf-104">Nhân viên của một pháp nhân trong một tổ chức có thể thực hiện công việc cho một pháp nhân khác trong cùng tổ chức đó.</span><span class="sxs-lookup"><span data-stu-id="9cfdf-104">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="9cfdf-105">Bạn có thể sử dụng chi phí liên công ty để chỉ định chi phí của nhân viên cho pháp nhân yêu cầu thực hiện công việc.</span><span class="sxs-lookup"><span data-stu-id="9cfdf-105">You can use intercompany expenses to assign the worker’s expenses to the legal entity for which the  work was performed.</span></span> <span data-ttu-id="9cfdf-106">Pháp nhân tuyển dụng nhân viên được gọi là pháp nhân cho mượn.</span><span class="sxs-lookup"><span data-stu-id="9cfdf-106">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="9cfdf-107">Pháp nhân chịu trách nhiệm đối với chi phí của nhân viên được gọi là pháp nhân mượn.</span><span class="sxs-lookup"><span data-stu-id="9cfdf-107">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="9cfdf-108">Trước khi một nhân viên có thể tạo và gửi chi phí liên công ty, bạn phải bật mô tả chi phí liên công ty.</span><span class="sxs-lookup"><span data-stu-id="9cfdf-108">Before a worker can create and submit intercompany expenses, you must enable intercompany expense lines.</span></span> <span data-ttu-id="9cfdf-109">Trong pháp nhân cho mượn, trên trang **Các tham số quản lý chi phí**, chọn **Cho phép mô tả chi phí liên công ty**.</span><span class="sxs-lookup"><span data-stu-id="9cfdf-109">In the loaning legal entity, on the **Expense management parameters** page, select **Allow intercompany expense lines**.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="9cfdf-110">Đăng thuế đối với chi phí liên công ty</span><span class="sxs-lookup"><span data-stu-id="9cfdf-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9cfdf-111">Để có thể dùng các nhóm thuế được liên kết với pháp nhân cho mượn (nguồn) thay vì pháp nhân mượn (đích) trong báo cáo chi phí, bạn phải bật chức năng này trong thiết lập thuế bán hàng của Sổ cái chung.</span><span class="sxs-lookup"><span data-stu-id="9cfdf-111">Before you can use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you must enable the functionality in the General ledger sales tax setup.</span></span> <span data-ttu-id="9cfdf-112">Khi tham số **Pháp nhân đăng thuế liên công ty** được đặt thành **Nguồn** và **Áp dụng các quy tắc đánh thuế bán hàng** được đặt thành **Không**, sự kết hợp thuế cho pháp nhân cho mượn sẽ được dùng.</span><span class="sxs-lookup"><span data-stu-id="9cfdf-112">When the **Legal entity for intercompany tax posting** parameter is set to **Source** and **Apply sales tax taxation rules** is set to **No**, the tax combination for the loaning legal entity is used.</span></span> <span data-ttu-id="9cfdf-113">Khi tham số đó được đặt thành **Đích**, tổ hợp thuế cho pháp nhân mượn sẽ được sử dụng.</span><span class="sxs-lookup"><span data-stu-id="9cfdf-113">When the same parameter is set to **Destination**, the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="9cfdf-114">Đối với các pháp nhân ở Hoa Kỳ, khi tham số được đặt thành **Nguồn**, trường **Thuế bán hàng phải thu** cũng phải được đặt cấu hình trên trang mới **Nhóm đăng trên Sổ Cái**.</span><span class="sxs-lookup"><span data-stu-id="9cfdf-114">For legal entities in the United States, when the parameter is set to **Source**, the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="9cfdf-115">Công cụ kế toán sẽ sử dụng thông tin ở trường này cho mục nhập kế toán liên quan đến thuế.</span><span class="sxs-lookup"><span data-stu-id="9cfdf-115">The accounting engine will use the information from this field for tax-related accounting entry.</span></span>   
<span data-ttu-id="9cfdf-116">Hành vi được thực hiện nhất quán đối với các mục mô tả chi phí được đăng có hoặc không có dự án.</span><span class="sxs-lookup"><span data-stu-id="9cfdf-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  


[!INCLUDE[footer-include](../includes/footer-banner.md)]