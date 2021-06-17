---
title: Mục nhập chi phí (bản đơn giản)
description: Chủ đề này cung cấp thông tin về cách làm việc với mục nhập chi phí trong một triển khai bản đơn giản.
author: stsporen
ms.date: 11/19/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e75a61c25be06a9db121e8165e8ccd25d4719d08
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002217"
---
# <a name="expense-entry-lite"></a><span data-ttu-id="5322b-103">Mục nhập chi phí (bản đơn giản)</span><span class="sxs-lookup"><span data-stu-id="5322b-103">Expense entry (lite)</span></span>

<span data-ttu-id="5322b-104">_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="5322b-104">_**Applies to:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5322b-105">Quản lý chi phí cơ bản hay đơn giản là khả năng ghi lại các khoản chi phí đơn giản.</span><span class="sxs-lookup"><span data-stu-id="5322b-105">Basic, or lite, expense management is the capability to record simple expenses.</span></span> <span data-ttu-id="5322b-106">Bạn có thể ghi lại các chi phí cho một dự án, sau đó người phê duyệt dự án sẽ đánh giá và phê duyệt chúng.</span><span class="sxs-lookup"><span data-stu-id="5322b-106">You can record expenses against a project, and then the project approver will review and approve them.</span></span>

<span data-ttu-id="5322b-107">Để biết thêm thông tin về các chức năng liên quan đến chi phí trong Dynamics 365 Project Operations, hãy xem [Tổng quan về chi phí](expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="5322b-107">For more information about expense capabilities in Dynamics 365 Project Operations, see [Expense overview](expense-overview.md).</span></span>

## <a name="capture-a-basic-expense"></a><span data-ttu-id="5322b-108">Ghi lại chi phí cơ bản</span><span class="sxs-lookup"><span data-stu-id="5322b-108">Capture a basic expense</span></span>

<span data-ttu-id="5322b-109">Bạn có thể ghi lại chi phí của mình để gửi cho người phê duyệt.</span><span class="sxs-lookup"><span data-stu-id="5322b-109">You can capture your expenses so that you can submit them to the approver.</span></span>

1. <span data-ttu-id="5322b-110">Đi đến **Chi phí** và chọn **Mới**.</span><span class="sxs-lookup"><span data-stu-id="5322b-110">Go to **Expenses**, and select **New**.</span></span>
2. <span data-ttu-id="5322b-111">Trên trang **Chi phí mới**, nhập thông tin chi phí bắt buộc, sau đó chọn **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="5322b-111">On the **New Expense** page, enter the required expense information, and then select **Save**.</span></span>

## <a name="submit-a-basic-expense"></a><span data-ttu-id="5322b-112">Gửi chi phí cơ bản</span><span class="sxs-lookup"><span data-stu-id="5322b-112">Submit a basic expense</span></span>

<span data-ttu-id="5322b-113">Sau khi hoàn tất việc ghi lại tất cả chi phí và sẵn sàng gửi để phê duyệt, bạn phải gửi chúng.</span><span class="sxs-lookup"><span data-stu-id="5322b-113">After you've finished capturing all your expenses, and you're ready to have them approved, you must submit them.</span></span>

1. <span data-ttu-id="5322b-114">Đi đến **Chi phí** và chọn một chi phí.</span><span class="sxs-lookup"><span data-stu-id="5322b-114">Go to **Expenses**, and select an expense.</span></span> <span data-ttu-id="5322b-115">Hoặc chọn tất cả các chi phí bằng cách sử dụng hộp kiểm trên tiêu đề.</span><span class="sxs-lookup"><span data-stu-id="5322b-115">Or, select all the expenses by using the check box on the header.</span></span>
2. <span data-ttu-id="5322b-116">Chọn **Gửi**.</span><span class="sxs-lookup"><span data-stu-id="5322b-116">Select **Submit**.</span></span> <span data-ttu-id="5322b-117">Hệ thống xử lý các mục nhập đã chọn, sau đó tạo các yêu cầu phê duyệt chi phí.</span><span class="sxs-lookup"><span data-stu-id="5322b-117">The system processes the selected entries and then creates expense approval requests.</span></span>

## <a name="add-an-attachment"></a><span data-ttu-id="5322b-118">Thêm tệp đính kèm</span><span class="sxs-lookup"><span data-stu-id="5322b-118">Add an attachment</span></span>

<span data-ttu-id="5322b-119">Bạn có thể phải cung cấp cho người phê duyệt tài liệu bổ sung về chi phí của bạn.</span><span class="sxs-lookup"><span data-stu-id="5322b-119">You may have to provide the approver with additional documentation about your expense.</span></span> <span data-ttu-id="5322b-120">Bạn có thể đính kèm biên nhận vào dòng thời gian của mục chi phí.</span><span class="sxs-lookup"><span data-stu-id="5322b-120">You can attach a receipt in the timeline of the expense entry.</span></span> <span data-ttu-id="5322b-121">Chọn **Chỉnh sửa** rồi trong phần **Dòng thời gian**, chọn biểu tượng kẹp giấy để đính kèm biên nhận.</span><span class="sxs-lookup"><span data-stu-id="5322b-121">Select **Edit** and in the **Timeline** section, and then select the paperclip icon to attach your receipt.</span></span>

## <a name="recall-a-basic-expense"></a><span data-ttu-id="5322b-122">Thu hồi chi phí cơ bản</span><span class="sxs-lookup"><span data-stu-id="5322b-122">Recall a basic expense</span></span>

<span data-ttu-id="5322b-123">Khi gửi nhầm một khoản chi phí, bạn có thể thu hồi khoản chi phí đó.</span><span class="sxs-lookup"><span data-stu-id="5322b-123">When you submit an expense by mistake, you can recall it.</span></span> <span data-ttu-id="5322b-124">Thời gian cần thiết để thu hồi một mục nhập chi phí phụ thuộc vào giai đoạn phê duyệt của nó.</span><span class="sxs-lookup"><span data-stu-id="5322b-124">The time that is required to recall an expense entry depends on its approval stage.</span></span>  <span data-ttu-id="5322b-125">Nếu người phê duyệt chưa chấp thuận mục nhập, việc thu hồi có thể xảy ra ngay lập tức.</span><span class="sxs-lookup"><span data-stu-id="5322b-125">If the approver hasn't yet approved the entry, the recall can occur immediately.</span></span> <span data-ttu-id="5322b-126">Tuy nhiên, nếu mục nhập đã được phê duyệt, người phê duyệt được yêu cầu phê duyệt việc thu hồi và đảo ngược các giao dịch.</span><span class="sxs-lookup"><span data-stu-id="5322b-126">However, if the entry has already been approved, the approver is asked to approve the recall and reverse the transactions.</span></span>

1. <span data-ttu-id="5322b-127">Đi đến **Chi phí**, sau đó, trong danh sách chi phí, hãy chọn chi phí cần thu hồi.</span><span class="sxs-lookup"><span data-stu-id="5322b-127">Go to **Expenses**, and then, in the list of expenses, select the expense to recall.</span></span>
2. <span data-ttu-id="5322b-128">Chọn **Thu hồi**.</span><span class="sxs-lookup"><span data-stu-id="5322b-128">Select **Recall**.</span></span> <span data-ttu-id="5322b-129">Nếu mục nhập chi phí chưa được duyệt, hệ thống sẽ thu hồi ngay lập tức.</span><span class="sxs-lookup"><span data-stu-id="5322b-129">If the expense entry hasn't yet been approved, the system immediately recalls it.</span></span> <span data-ttu-id="5322b-130">Nếu mục nhập chi phí đã được phê duyệt, một yêu cầu thu hồi sẽ được tạo để thông báo cho người phê duyệt rằng bạn muốn đảo ngược chi phí.</span><span class="sxs-lookup"><span data-stu-id="5322b-130">If the expense entry has already been approved, a recall request is created to notify the approver that you want to reverse the expense.</span></span> <span data-ttu-id="5322b-131">Khi đó, người phê duyệt sẽ xác nhận rằng việc đảo ngược có thể được thực hiện và mục nhập sẽ được trả lại.</span><span class="sxs-lookup"><span data-stu-id="5322b-131">The approver will then confirm that the reversal can be done, and the entry will be returned.</span></span>

## <a name="delete-a-basic-expense"></a><span data-ttu-id="5322b-132">Xóa chi phí cơ bản</span><span class="sxs-lookup"><span data-stu-id="5322b-132">Delete a basic expense</span></span>

<span data-ttu-id="5322b-133">Các chi phí chưa được gửi có thể bị xóa.</span><span class="sxs-lookup"><span data-stu-id="5322b-133">Expenses that haven't yet been submitted can be deleted.</span></span> <span data-ttu-id="5322b-134">Để xóa một khoản chi phí đã được gửi, trước tiên bạn phải thu hồi nó.</span><span class="sxs-lookup"><span data-stu-id="5322b-134">To delete an expense that has already been submitted, you must first recall it.</span></span>

## <a name="see-also"></a><span data-ttu-id="5322b-135">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="5322b-135">See also</span></span>

- [<span data-ttu-id="5322b-136">Tổng quan về phê duyệt</span><span class="sxs-lookup"><span data-stu-id="5322b-136">Approvals overview</span></span>](../approvals/approvals-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]