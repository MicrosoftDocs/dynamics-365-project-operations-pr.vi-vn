---
title: Thiết lập quy trình làm việc để quản lý chi phí
description: Bạn có thể thiết lập một quy trình làm việc được sử dụng để xem xét và phê duyệt các tài liệu về chi phí và đi lại.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: db1bda71e18369550cd2d38fee1d0ac40e07555d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087135"
---
# <a name="set-up-workflows-for-expense-management"></a><span data-ttu-id="beb46-103">Thiết lập quy trình làm việc để quản lý chi phí</span><span class="sxs-lookup"><span data-stu-id="beb46-103">Set up workflows for Expense management</span></span>

<span data-ttu-id="beb46-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="beb46-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="beb46-105">Bạn có thể thiết lập một quy trình làm việc để xem xét và phê duyệt các tài liệu về chi phí và đi lại.</span><span class="sxs-lookup"><span data-stu-id="beb46-105">You can set up a workflow process to review and approve travel and expense documents.</span></span> <span data-ttu-id="beb46-106">Bạn có thể xác định quy trình làm việc cho các báo cáo chi phí, tiêu chuẩn đi lại và yêu cầu tạm ứng tiền mặt.</span><span class="sxs-lookup"><span data-stu-id="beb46-106">You can define workflows for expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="beb46-107">Quy trình làm việc đại diện cho một quy trình kinh doanh và xác định cách tài liệu đi qua hệ thống.</span><span class="sxs-lookup"><span data-stu-id="beb46-107">A workflow represents a business process and defines how a document flows through the system.</span></span> <span data-ttu-id="beb46-108">Quy trình làm việc cũng cho biết ai phải hoàn thành tác vụ hoặc phê duyệt tài liệu.</span><span class="sxs-lookup"><span data-stu-id="beb46-108">The workflow also indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="beb46-109">Có một vài lợi ích khi sử dụng hệ thống quy trình làm việc trong tổ chức của bạn:</span><span class="sxs-lookup"><span data-stu-id="beb46-109">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="beb46-110">**Quy trình nhất quán** : Bạn có thể xác định quy trình phê duyệt cho các tài liệu cụ thể, chẳng hạn như yêu cầu mua hàng và báo cáo chi phí.</span><span class="sxs-lookup"><span data-stu-id="beb46-110">**Consistent processes** : You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="beb46-111">Sử dụng hệ thống quy trình làm việc giúp đảm bảo rằng các tài liệu được xử lý và phê duyệt một cách nhất quán và hiệu quả.</span><span class="sxs-lookup"><span data-stu-id="beb46-111">Using the workflow system helps ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="beb46-112">**Khả năng hiển thị quá trình** : Bạn có thể theo dõi trạng thái, lịch sử và số liệu hiệu suất của một phiên bản quy trình làm việc cụ thể.</span><span class="sxs-lookup"><span data-stu-id="beb46-112">**Process visibility** : You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="beb46-113">Điều này giúp bạn xác định xem có nên thực hiện các thay đổi đối với quy trình làm việc để nâng cao hiệu quả hay không.</span><span class="sxs-lookup"><span data-stu-id="beb46-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="beb46-114">**Danh sách công việc tập trung** : Người dùng có thể xem danh sách công việc tập trung để xem các tác vụ và mục phê duyệt của quy trình làm việc được chỉ định cho họ.</span><span class="sxs-lookup"><span data-stu-id="beb46-114">**Centralized work list** : Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

## <a name="workflow-types"></a><span data-ttu-id="beb46-115">Các loại quy trình làm việc</span><span class="sxs-lookup"><span data-stu-id="beb46-115">Workflow types</span></span>

<span data-ttu-id="beb46-116">Bảng sau liệt kê các loại quy trình làm việc mà bạn có thể tạo trong **Quản lý chi phí**.</span><span class="sxs-lookup"><span data-stu-id="beb46-116">The following table lists the types of workflows that you can create in **Expense Management**.</span></span>


|              <span data-ttu-id="beb46-117"><strong>Loại</strong></span><span class="sxs-lookup"><span data-stu-id="beb46-117"><strong>Type</strong></span></span>              |                   <span data-ttu-id="beb46-118"><strong>Sử dụng loại này để</strong></span><span class="sxs-lookup"><span data-stu-id="beb46-118"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <span data-ttu-id="beb46-119"><strong>Tự động phê duyệt báo cáo chi phí</strong></span><span class="sxs-lookup"><span data-stu-id="beb46-119"><strong>Expense report auto approval</strong></span></span> |            <span data-ttu-id="beb46-120">Tạo quy trình làm việc cho báo cáo chi phí.</span><span class="sxs-lookup"><span data-stu-id="beb46-120">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="beb46-121"><strong>Tự động đăng báo cáo chi phí</strong></span><span class="sxs-lookup"><span data-stu-id="beb46-121"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="beb46-122">Tạo quy trình làm việc tự động đăng cho báo cáo chi phí.</span><span class="sxs-lookup"><span data-stu-id="beb46-122">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="beb46-123"><strong>Mục mô tả chi phí</strong></span><span class="sxs-lookup"><span data-stu-id="beb46-123"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="beb46-124">Tạo quy trình làm việc cho mục mô tả trên báo cáo chi phí.</span><span class="sxs-lookup"><span data-stu-id="beb46-124">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="beb46-125"><strong>Tự động đăng mục mô tả chi phí</strong></span><span class="sxs-lookup"><span data-stu-id="beb46-125"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="beb46-126">Tạo quy trình làm việc tự động đăng cho mục mô tả trên báo cáo chi phí.</span><span class="sxs-lookup"><span data-stu-id="beb46-126">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="beb46-127"><strong>Tiêu chuẩn đi lại</strong></span><span class="sxs-lookup"><span data-stu-id="beb46-127"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="beb46-128">Tạo quy trình làm việc phê duyệt cho tiêu chuẩn đi lại.</span><span class="sxs-lookup"><span data-stu-id="beb46-128">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="beb46-129"><strong>Yêu cầu tạm ứng tiền mặt</strong></span><span class="sxs-lookup"><span data-stu-id="beb46-129"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="beb46-130">Tạo quy trình làm việc phê duyệt cho yêu cầu tạm ứng tiền mặt.</span><span class="sxs-lookup"><span data-stu-id="beb46-130">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="beb46-131"><strong>Hoàn thuế GTGT</strong></span><span class="sxs-lookup"><span data-stu-id="beb46-131"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="beb46-132">Tạo quy trình làm việc phê duyệt cho việc hoàn thuế giá trị gia tăng (VAT).</span><span class="sxs-lookup"><span data-stu-id="beb46-132">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |
