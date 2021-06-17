---
title: Thiết lập quy trình làm việc Quản lý chi phí
description: Bạn có thể thiết lập một quy trình làm việc để xem xét và phê duyệt các tài liệu về chi phí và đi lại.
author: ShylaThompson
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4070b4fb5109464abdabbce971688fb881dfcf2c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005142"
---
# <a name="set-up-expense-management-workflows"></a><span data-ttu-id="fa4a3-103">Thiết lập quy trình làm việc Quản lý chi phí</span><span class="sxs-lookup"><span data-stu-id="fa4a3-103">Set up Expense management workflows</span></span>

<span data-ttu-id="fa4a3-104">Bạn có thể thiết lập một quy trình làm việc được sử dụng để xem xét và phê duyệt các tài liệu về chi phí và đi lại.</span><span class="sxs-lookup"><span data-stu-id="fa4a3-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="fa4a3-105">Bạn có thể xác định quy trình làm việc cho các tài liệu như: báo cáo chi phí, yêu cầu đi lại và yêu cầu tạm ứng tiền mặt.</span><span class="sxs-lookup"><span data-stu-id="fa4a3-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="fa4a3-106">Mỗi quy trình làm việc đại diện cho một quy trình công việc.</span><span class="sxs-lookup"><span data-stu-id="fa4a3-106">A workflow represents a business process.</span></span> <span data-ttu-id="fa4a3-107">Quy trình này xác định cách thức đưa một tài liệu qua hệ thống và cho biết ai phải hoàn thành một nhiệm vụ hoặc phê duyệt một tài liệu.</span><span class="sxs-lookup"><span data-stu-id="fa4a3-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="fa4a3-108">Có một vài lợi ích khi sử dụng hệ thống quy trình làm việc trong tổ chức của bạn:</span><span class="sxs-lookup"><span data-stu-id="fa4a3-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="fa4a3-109">**Quy trình nhất quán**: Bạn có thể xác định quy trình phê duyệt cho các tài liệu cụ thể, như yêu cầu mua hàng và báo cáo chi phí.</span><span class="sxs-lookup"><span data-stu-id="fa4a3-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="fa4a3-110">Việc sử dụng hệ thống quy trình làm việc giúp bảo đảm rằng các tài liệu được xử lý và phê duyệt một cách nhất quán và hiệu quả.</span><span class="sxs-lookup"><span data-stu-id="fa4a3-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="fa4a3-111">Khả năng hiển thị trên quy trình: Bạn có thể theo dõi trạng thái, lịch sử và số liệu hiệu suất của một phiên bản quy trình làm việc cụ thể.</span><span class="sxs-lookup"><span data-stu-id="fa4a3-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="fa4a3-112">Điều này giúp bạn xác định xem có nên thực hiện các thay đổi đối với quy trình làm việc để nâng cao hiệu quả hay không.</span><span class="sxs-lookup"><span data-stu-id="fa4a3-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="fa4a3-113">Danh sách công việc tập trung: Người dùng có thể xem danh sách công việc tập trung để biết các nhiệm vụ và mục phê duyệt trong quy trình làm việc được chỉ định cho họ.</span><span class="sxs-lookup"><span data-stu-id="fa4a3-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="fa4a3-114">**Các loại quy trình làm việc mà bạn có thể tạo**</span><span class="sxs-lookup"><span data-stu-id="fa4a3-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="fa4a3-115">Bảng sau liệt kê các loại quy trình làm việc mà bạn có thể tạo trong **Chi phí**.</span><span class="sxs-lookup"><span data-stu-id="fa4a3-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="fa4a3-116"><strong>Loại</strong></span><span class="sxs-lookup"><span data-stu-id="fa4a3-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="fa4a3-117"><strong>Sử dụng loại này để</strong></span><span class="sxs-lookup"><span data-stu-id="fa4a3-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="fa4a3-118"><strong>Báo cáo chi phí</strong></span><span class="sxs-lookup"><span data-stu-id="fa4a3-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="fa4a3-119">Tạo quy trình làm việc cho báo cáo chi phí.</span><span class="sxs-lookup"><span data-stu-id="fa4a3-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="fa4a3-120"><strong>Tự động đăng báo cáo chi phí</strong></span><span class="sxs-lookup"><span data-stu-id="fa4a3-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="fa4a3-121">Tạo quy trình làm việc tự động đăng cho báo cáo chi phí.</span><span class="sxs-lookup"><span data-stu-id="fa4a3-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="fa4a3-122"><strong>Mục mô tả chi phí</strong></span><span class="sxs-lookup"><span data-stu-id="fa4a3-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="fa4a3-123">Tạo quy trình làm việc cho mục mô tả trên báo cáo chi phí.</span><span class="sxs-lookup"><span data-stu-id="fa4a3-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="fa4a3-124"><strong>Tự động đăng mục mô tả chi phí</strong></span><span class="sxs-lookup"><span data-stu-id="fa4a3-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="fa4a3-125">Tạo quy trình làm việc tự động đăng cho mục mô tả trên báo cáo chi phí.</span><span class="sxs-lookup"><span data-stu-id="fa4a3-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="fa4a3-126"><strong>Tiêu chuẩn đi lại</strong></span><span class="sxs-lookup"><span data-stu-id="fa4a3-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="fa4a3-127">Tạo quy trình làm việc phê duyệt cho tiêu chuẩn đi lại.</span><span class="sxs-lookup"><span data-stu-id="fa4a3-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="fa4a3-128"><strong>Yêu cầu tạm ứng tiền mặt</strong></span><span class="sxs-lookup"><span data-stu-id="fa4a3-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="fa4a3-129">Tạo quy trình làm việc phê duyệt cho yêu cầu tạm ứng tiền mặt.</span><span class="sxs-lookup"><span data-stu-id="fa4a3-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="fa4a3-130"><strong>Hoàn thuế GTGT</strong></span><span class="sxs-lookup"><span data-stu-id="fa4a3-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="fa4a3-131">Tạo quy trình làm việc phê duyệt cho việc hoàn thuế giá trị gia tăng (VAT).</span><span class="sxs-lookup"><span data-stu-id="fa4a3-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |



[!INCLUDE[footer-include](../includes/footer-banner.md)]