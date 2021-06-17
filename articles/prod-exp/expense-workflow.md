---
title: Quy trình làm việc quản lý chi phí
description: Chủ đề này giải thích cách thức bạn có thể sử dụng hệ thống quy trình làm việc trong Microsoft Dynamics 365 Finance để thiết lập quy trình đánh giá báo cáo chi phí trong phần Quản lý chi phí.
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
ms.openlocfilehash: 51ac2712f62d5c5d85b21c0ea929517ccb893bca
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005232"
---
# <a name="expense-management-workflow"></a><span data-ttu-id="2d974-103">Quy trình làm việc quản lý chi phí</span><span class="sxs-lookup"><span data-stu-id="2d974-103">Expense management workflow</span></span>

<span data-ttu-id="2d974-104">Bạn có thể sử dụng hệ thống quy trình làm việc để thiết lập quy trình đánh giá báo cáo chi phí trong phần Quản lý chi phí.</span><span class="sxs-lookup"><span data-stu-id="2d974-104">You can use the workflow system to set up a review process for expense reports in Expense management.</span></span> <span data-ttu-id="2d974-105">Bạn có thể thiết lập một quy trình làm việc sử dụng các tiêu chí sau để xác định ai phê duyệt báo cáo chi phí:</span><span class="sxs-lookup"><span data-stu-id="2d974-105">You can set up a workflow that uses the following criteria to determine who approves expense reports:</span></span>

- <span data-ttu-id="2d974-106">Hệ thống phân cấp báo cáo của nhân viên và các giới hạn phê duyệt được xác định trước</span><span class="sxs-lookup"><span data-stu-id="2d974-106">The employee reporting hierarchy and predefined approval limits</span></span>
- <span data-ttu-id="2d974-107">Hệ thống phê duyệt đa cấp hỗ trợ người phê duyệt tạm thời và người phê duyệt cuối cùng</span><span class="sxs-lookup"><span data-stu-id="2d974-107">Multi-level approval that supports interim approvers and a final approver</span></span>
- <span data-ttu-id="2d974-108">Các thông số tài chính và trách nhiệm trong dự án</span><span class="sxs-lookup"><span data-stu-id="2d974-108">Financial dimensions and project responsibility</span></span>
- <span data-ttu-id="2d974-109">Phần chỉ định cho người dùng hoặc nhóm người dùng cụ thể</span><span class="sxs-lookup"><span data-stu-id="2d974-109">Assignment to specific users or user groups</span></span>

<span data-ttu-id="2d974-110">Các mục phê duyệt trong quy trình làm việc có thể được tạo cho báo cáo chi phí, yêu cầu đi lại, tạm ứng tiền mặt và thu hồi thuế giá trị gia tăng (VAT).</span><span class="sxs-lookup"><span data-stu-id="2d974-110">Workflow approvals can be created for expense reports, travel requisitions, cash advances, and value-added tax (VAT) recovery.</span></span>

<span data-ttu-id="2d974-111">**Ví dụ:**</span><span class="sxs-lookup"><span data-stu-id="2d974-111">**Example**</span></span>

<span data-ttu-id="2d974-112">Quy trình sau đây là một ví dụ về quy trình làm việc quản lý chi phí cho một báo cáo chi phí.</span><span class="sxs-lookup"><span data-stu-id="2d974-112">The following process is an example of the expense management workflow for an expense report.</span></span>

1. <span data-ttu-id="2d974-113">Một nhân viên tạo và lưu báo cáo chi phí.</span><span class="sxs-lookup"><span data-stu-id="2d974-113">An employee creates and saves an expense report.</span></span>
2. <span data-ttu-id="2d974-114">Nhân viên gửi báo cáo chi phí để phê duyệt.</span><span class="sxs-lookup"><span data-stu-id="2d974-114">The employee submits the expense report for approval.</span></span> <span data-ttu-id="2d974-115">Người phê duyệt được xác định dựa trên các quy tắc đã xác định trong quá trình thiết lập quy trình làm việc.</span><span class="sxs-lookup"><span data-stu-id="2d974-115">The approver is identified based on the rules that were defined when the workflow was set up.</span></span>
3. <span data-ttu-id="2d974-116">Người phê duyệt nhận được thông báo rằng có một báo cáo chi phí đã sẵn sàng để phê duyệt.</span><span class="sxs-lookup"><span data-stu-id="2d974-116">The approver receives a notification that an expense report is ready for approval.</span></span> <span data-ttu-id="2d974-117">Người phê duyệt đánh giá báo cáo chi phí và xác minh rằng các điều kiện sau được đáp ứng:</span><span class="sxs-lookup"><span data-stu-id="2d974-117">The approver reviews the expense report and verifies that the following conditions are met:</span></span>

    - <span data-ttu-id="2d974-118">Các chi phí không vi phạm bất kỳ chính sách chi phí nào.</span><span class="sxs-lookup"><span data-stu-id="2d974-118">The expenses don't violate any expense policies.</span></span> <span data-ttu-id="2d974-119">Nếu có một khoản chi phí vi phạm chính sách, thì người phê duyệt xác minh rằng trong báo cáo chi phí có chi tiết biện minh kinh doanh hợp lệ.</span><span class="sxs-lookup"><span data-stu-id="2d974-119">If an expense violates a policy, the approver verifies that the expense report includes a valid business justification.</span></span>
    - <span data-ttu-id="2d974-120">Biên lai điện tử được đính kèm với báo cáo chi phí.</span><span class="sxs-lookup"><span data-stu-id="2d974-120">Electronic receipts are attached to the expense report.</span></span>

4. <span data-ttu-id="2d974-121">Người phê duyệt tiến hành phê duyệt báo cáo chi phí.</span><span class="sxs-lookup"><span data-stu-id="2d974-121">The approver approves the expense report.</span></span>
5. <span data-ttu-id="2d974-122">Báo cáo chi phí được giao cho người điều phối Khoản phải trả để đăng.</span><span class="sxs-lookup"><span data-stu-id="2d974-122">The expense report is assigned to the Accounts payable coordinator for posting.</span></span>
6. <span data-ttu-id="2d974-123">Một trong các bước sau xảy ra, tùy thuộc vào việc chức năng đăng tự động có được đặt cấu hình hay không:</span><span class="sxs-lookup"><span data-stu-id="2d974-123">One of the following steps occurs, depending on whether automatic posting is configured:</span></span>

    - <span data-ttu-id="2d974-124">Nếu chức năng đăng tự động được đặt cấu hình, thì báo cáo chi phí sẽ được xử lý để thanh toán và trạng thái của báo cáo chi phí được cập nhật.</span><span class="sxs-lookup"><span data-stu-id="2d974-124">If automatic posting is configured, the expense report is processed for payment, and the status of the expense report is updated.</span></span>
    - <span data-ttu-id="2d974-125">Nếu chức năng đăng tự động không được đặt cấu hình, thì điều phối viên Khoản phải trả xác minh rằng tất cả các biên lai gốc đã được gửi và các biên lai đó phù hợp với chi phí trên báo cáo chi phí.</span><span class="sxs-lookup"><span data-stu-id="2d974-125">If automatic posting isn't configured, the Accounts payable coordinator verifies that all original receipts have been submitted, and that the receipts are aligned with the expenses on the expense report.</span></span> <span data-ttu-id="2d974-126">Tất cả các mã số thuế được nhập trên báo cáo chi phí cũng phải được xác nhận là chính xác.</span><span class="sxs-lookup"><span data-stu-id="2d974-126">All tax codes that are entered on the expense report must also be verified as correct.</span></span>

<span data-ttu-id="2d974-127">Sau khi các yêu cầu này được xác minh, báo cáo chi phí sẽ được đăng.</span><span class="sxs-lookup"><span data-stu-id="2d974-127">After these requirements are verified, the expense report is posted.</span></span>

<span data-ttu-id="2d974-128">Sau khi báo cáo chi phí được đăng, việc thanh toán được chấp thuận đối với báo cáo chi phí và nhân viên được hoàn trả.</span><span class="sxs-lookup"><span data-stu-id="2d974-128">After the expense report is posted, payment is authorized for the expense report, and the employee is reimbursed.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]