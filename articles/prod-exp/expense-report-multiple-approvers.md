---
title: Nhiều người phê duyệt trên báo cáo chi phí
description: Chủ đề này cung cấp thông tin về các báo cáo chi phí cần được nhiều người phê duyệt.
author: saraschi2
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c745dda957fab5acc464b9d1c774fcdc783cde40
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005277"
---
# <a name="multiple-approvers-on-an-expense-report"></a><span data-ttu-id="d154b-103">Nhiều người phê duyệt trên báo cáo chi phí</span><span class="sxs-lookup"><span data-stu-id="d154b-103">Multiple approvers on an expense report</span></span>

<span data-ttu-id="d154b-104">Tùy theo chính sách phê duyệt chi phí của tổ chức của bạn, báo cáo chi phí do nhân viên nộp có thể phải được hai người trở lên phê duyệt.</span><span class="sxs-lookup"><span data-stu-id="d154b-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="d154b-105">Khi thiết lập quy trình làm việc để phê duyệt báo cáo chi phí, bạn có thể thêm các yếu tố quy trình công việc bao gồm các nhiệm vụ hoặc các bước cho một hoặc nhiều người phê duyệt báo cáo chi phí.</span><span class="sxs-lookup"><span data-stu-id="d154b-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="d154b-106">Chẳng hạn, bạn có thể yêu cầu rằng mọi báo cáo chi phí trước tiên phải được người quản lý của nhân viên đã nộp báo cáo phê duyệt, rồi sau đó là đến người điều phối Khoản phải trả phê duyệt.</span><span class="sxs-lookup"><span data-stu-id="d154b-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="d154b-107">Nếu quyết định yêu cầu nhiều người phê duyệt báo cáo chi phí, bạn có thể thêm các yếu tố quy trình làm việc theo bất kỳ cách nào sau đây:</span><span class="sxs-lookup"><span data-stu-id="d154b-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="d154b-108">Thêm một yếu tố phê duyệt có một bước.</span><span class="sxs-lookup"><span data-stu-id="d154b-108">Add one approval element that has one step.</span></span> <span data-ttu-id="d154b-109">Ví dụ: bước này có thể yêu cầu báo cáo chi phí được chỉ định cho một nhóm người dùng và phải được 50 phần trăm thành viên của nhóm người dùng phê duyệt.</span><span class="sxs-lookup"><span data-stu-id="d154b-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="d154b-110">Thêm một yếu tố phê duyệt có nhiều bước.</span><span class="sxs-lookup"><span data-stu-id="d154b-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="d154b-111">Ví dụ: yếu tố phê duyệt có thể có các bước sau:</span><span class="sxs-lookup"><span data-stu-id="d154b-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="d154b-112">Người quản lý của nhân viên đã nộp báo cáo chi phí phê duyệt báo cáo.</span><span class="sxs-lookup"><span data-stu-id="d154b-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="d154b-113">Thư ký Kế toán khoản phải trả xác minh biên lai và các mục báo cáo chi phí.</span><span class="sxs-lookup"><span data-stu-id="d154b-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="d154b-114">Chủ ngân sách phê duyệt báo cáo chi phí.</span><span class="sxs-lookup"><span data-stu-id="d154b-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="d154b-115">Thêm nhiều yếu tố phê duyệt, mỗi yếu tố có một bước.</span><span class="sxs-lookup"><span data-stu-id="d154b-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="d154b-116">Ví dụ: bạn có thể thêm một yếu tố phê duyệt riêng cho mỗi bước sau:</span><span class="sxs-lookup"><span data-stu-id="d154b-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="d154b-117">Người quản lý của nhân viên phê duyệt báo cáo chi phí.</span><span class="sxs-lookup"><span data-stu-id="d154b-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="d154b-118">Chủ ngân sách phê duyệt báo cáo chi phí.</span><span class="sxs-lookup"><span data-stu-id="d154b-118">The budget owner approves the expense report.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]