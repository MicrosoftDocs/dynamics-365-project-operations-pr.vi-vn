---
title: Báo cáo chi phí và nhiều người phê duyệt
description: Chủ đề này cung cấp thông tin về các báo cáo chi phí cần hai người trở lên phê duyệt.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 818092dd631d07cc0a7d63c9eec51eeff4f67ffe
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897117"
---
# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="852ba-103">Báo cáo chi phí và nhiều người phê duyệt</span><span class="sxs-lookup"><span data-stu-id="852ba-103">Expense reports and multiple approvers</span></span>

<span data-ttu-id="852ba-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="852ba-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="852ba-105">Tùy thuộc vào chính sách phê duyệt chi phí của tổ chức của bạn, hai người trở lên có thể phải phê duyệt báo cáo chi phí đã nộp.</span><span class="sxs-lookup"><span data-stu-id="852ba-105">Depending on your organization's expense approval policies, more than one person might have to approve a submitted expense report.</span></span> <span data-ttu-id="852ba-106">Khi thiết lập quy trình làm việc để phê duyệt báo cáo chi phí, bạn có thể thêm các yếu tố quy trình công việc bao gồm các nhiệm vụ hoặc các bước cho một hoặc nhiều người phê duyệt báo cáo chi phí.</span><span class="sxs-lookup"><span data-stu-id="852ba-106">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="852ba-107">Ví dụ: bạn có thể yêu cầu hai người riêng biệt, người quản lý của nhân viên đã nộp báo cáo và người điều phối Khoản phải trả, phê duyệt tất cả các báo cáo chi phí.</span><span class="sxs-lookup"><span data-stu-id="852ba-107">For example, you might require that all expense reports be approved by two separate people, the manager of the employee who submitted the report and the Accounts payable coordinator.</span></span>

<span data-ttu-id="852ba-108">Nếu quyết định yêu cầu nhiều người phê duyệt báo cáo chi phí, bạn có thể thêm các yếu tố quy trình làm việc theo bất kỳ cách nào sau đây:</span><span class="sxs-lookup"><span data-stu-id="852ba-108">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="852ba-109">Thêm một yếu tố phê duyệt có một bước.</span><span class="sxs-lookup"><span data-stu-id="852ba-109">Add one approval element that has one step.</span></span> <span data-ttu-id="852ba-110">Ví dụ: bước này có thể yêu cầu báo cáo chi phí được chỉ định cho một nhóm người dùng và phải được 50 phần trăm thành viên của nhóm người dùng phê duyệt.</span><span class="sxs-lookup"><span data-stu-id="852ba-110">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="852ba-111">Thêm một yếu tố phê duyệt có nhiều bước.</span><span class="sxs-lookup"><span data-stu-id="852ba-111">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="852ba-112">Ví dụ: yếu tố phê duyệt có thể có các bước sau:</span><span class="sxs-lookup"><span data-stu-id="852ba-112">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="852ba-113">Người quản lý của nhân viên đã nộp báo cáo chi phí phê duyệt báo cáo.</span><span class="sxs-lookup"><span data-stu-id="852ba-113">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="852ba-114">Thư ký Kế toán khoản phải trả xác minh biên lai và các mục báo cáo chi phí.</span><span class="sxs-lookup"><span data-stu-id="852ba-114">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="852ba-115">Chủ ngân sách phê duyệt báo cáo chi phí.</span><span class="sxs-lookup"><span data-stu-id="852ba-115">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="852ba-116">Thêm nhiều yếu tố phê duyệt, mỗi yếu tố có một bước.</span><span class="sxs-lookup"><span data-stu-id="852ba-116">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="852ba-117">Ví dụ: bạn có thể thêm một yếu tố phê duyệt riêng cho mỗi bước sau:</span><span class="sxs-lookup"><span data-stu-id="852ba-117">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="852ba-118">Người quản lý của nhân viên phê duyệt báo cáo chi phí.</span><span class="sxs-lookup"><span data-stu-id="852ba-118">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="852ba-119">Chủ ngân sách phê duyệt báo cáo chi phí.</span><span class="sxs-lookup"><span data-stu-id="852ba-119">The budget owner approves the expense report.</span></span>
