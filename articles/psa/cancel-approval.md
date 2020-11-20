---
title: Huỷ mục nhập thời gian và chi phí đã được phê duyệt trước đó
description: Chủ đề này cung cấp thông tin về cách hủy giao dịch chi phí và thời gian dự án được phê duyệt.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 84fc057599dd98162320d6104ed4a7612e894ecb
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123359"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a><span data-ttu-id="28269-103">Huỷ mục nhập thời gian hoặc chi phí đã được phê duyệt trước đó</span><span class="sxs-lookup"><span data-stu-id="28269-103">Cancel previously approved time or expense entries</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="28269-104">Trong phiên bản mới nhất của Dynamics 365 Project Service Automation, người phê duyệt có thể hủy mục nhập thời gian hoặc chi phí mà họ đã phê duyệt trước đó.</span><span class="sxs-lookup"><span data-stu-id="28269-104">In the latest version of Dynamics 365 Project Service Automation, approvers can cancel time or expense entries that they previously approved.</span></span>

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a><span data-ttu-id="28269-105">Hủy mục nhập thời gian hoặc chi phí đã được phê duyệt trước đó</span><span class="sxs-lookup"><span data-stu-id="28269-105">Cancel a previously approved time or expense entry</span></span>

<span data-ttu-id="28269-106">Hãy làm theo các bước sau để hủy mục nhập thời gian hoặc chi phí mà bạn đã phê duyệt trước đó.</span><span class="sxs-lookup"><span data-stu-id="28269-106">Follow these steps to cancel a time or expense entry that you previously approved.</span></span>

1. <span data-ttu-id="28269-107">Truy cập **Dự án** \> **Công việc của tôi** \> **Phê duyệt**.</span><span class="sxs-lookup"><span data-stu-id="28269-107">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="28269-108">Trên trang danh sách **Phê duyệt**, thay đổi dạng xem thành **Phê duyệt trước đây của tôi**.</span><span class="sxs-lookup"><span data-stu-id="28269-108">On the **Approvals** list page, change the view to **My past approvals**.</span></span> <span data-ttu-id="28269-109">Danh sách các mục nhập thời gian và chi phí mà bạn đã phê duyệt trước đó được hiển thị.</span><span class="sxs-lookup"><span data-stu-id="28269-109">A list of the time and expense entries that you previously approved is shown.</span></span>
3. <span data-ttu-id="28269-110">Chọn một hoặc nhiều mục nhập, sau đó chọn **Hủy phê duyệt**.</span><span class="sxs-lookup"><span data-stu-id="28269-110">Select one or more entries, and then select **Cancel approval**.</span></span> <span data-ttu-id="28269-111">Bạn nhận được một thông báo cảnh báo.</span><span class="sxs-lookup"><span data-stu-id="28269-111">You receive a warning message.</span></span>
4. <span data-ttu-id="28269-112">Chọn **OK** để hủy phê duyệt.</span><span class="sxs-lookup"><span data-stu-id="28269-112">Select **OK** to cancel the approval.</span></span>

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a><span data-ttu-id="28269-113">Hiểu rõ tác động của việc hủy bỏ một phê duyệt mục nhập thời gian hoặc chi phí</span><span class="sxs-lookup"><span data-stu-id="28269-113">Understand the impact of canceling a time or expense entry approval</span></span>

<span data-ttu-id="28269-114">Khi hủy bỏ một chấp thuận, bạn sẽ tác động đến cả tài chính và vận hành.</span><span class="sxs-lookup"><span data-stu-id="28269-114">When an approval is canceled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="28269-115">Tác động đến vận hành</span><span class="sxs-lookup"><span data-stu-id="28269-115">Operational impact</span></span>

<span data-ttu-id="28269-116">Về phía vận hành, khi hủy một phê duyệt, trạng thái của bản ghi sẽ được đặt lại thành **Bản nháp** và phê duyệt không còn xuất hiện trong dạng xem **Phê duyệt trước đây của tôi** nữa.</span><span class="sxs-lookup"><span data-stu-id="28269-116">On the operations side, when an approval is canceled, the status of the record is reset to **Draft**, and the approval no longer appears in the **My past approvals** view.</span></span> <span data-ttu-id="28269-117">Thay vào đó, phê duyệt bị hủy sẽ xuất hiện trong dạng xem **Mục nhập thời gian cần phê duyệt** hoặc dạng xem **Mục nhập chi phí cần phê duyệt**, tùy thuộc vào đó là mục nhập thời gian hay chi phí.</span><span class="sxs-lookup"><span data-stu-id="28269-117">Instead, the canceled approval appears in either the **Time entries for approval** view or the **Expense entries for approval** view, depending on whether it was a time entry or an expense entry.</span></span> <span data-ttu-id="28269-118">Ngoài ra, trạng thái của mục nhập thời gian hoặc chi phí liên quan được đổi thành **Đã gửi** để mục nhập liên quan nhất quán với phê duyệt có trạng thái **Bản nháp**.</span><span class="sxs-lookup"><span data-stu-id="28269-118">Additionally, the status of the related time or expense entry is changed to **Submitted**, so that the related entry is consistent with approvals that have a status of **Draft**.</span></span>

<span data-ttu-id="28269-119">Là người phê duyệt, bạn có thể chỉnh sửa một số trường của phê duyệt có trạng thái **Bản nháp**.</span><span class="sxs-lookup"><span data-stu-id="28269-119">As an approver, you can edit some of the fields of an approval that has a status of **Draft**.</span></span> <span data-ttu-id="28269-120">Các trường này bao gồm **Loại thanh toán** và **Số giờ có thể lập hóa đơn cho mục nhập thời gian**.</span><span class="sxs-lookup"><span data-stu-id="28269-120">These fields include **Billing Type** and **Billable Hours for Time Entries**.</span></span> <span data-ttu-id="28269-121">Sau khi thực hiện thay đổi, bạn có thể phê duyệt lại bản ghi.</span><span class="sxs-lookup"><span data-stu-id="28269-121">After you make changes, you can approve the record again.</span></span> <span data-ttu-id="28269-122">Ngoài ra, bạn có thể từ chối mục nhập.</span><span class="sxs-lookup"><span data-stu-id="28269-122">Alternatively, you can reject the entry.</span></span> <span data-ttu-id="28269-123">Nếu bạn từ chối phê duyệt mục nhập thời gian, thì trạng thái của mục nhập được thay đổi thành **Đã trả lại**.</span><span class="sxs-lookup"><span data-stu-id="28269-123">If you reject the approval of a time entry, the status of the entry is changed to **Returned**.</span></span> <span data-ttu-id="28269-124">Nếu bạn từ chối phê duyệt một mục nhập chi phí, thì trạng thái được thay đổi thành **Đã từ chối**.</span><span class="sxs-lookup"><span data-stu-id="28269-124">If you reject the approval of an expense entry, the status is changed to **Rejected**.</span></span> <span data-ttu-id="28269-125">Về mặt chức năng, cả mục nhập đã trả về và đã từ chối đều hoạt động giống như mục nhập có trạng thái **Bản nháp**.</span><span class="sxs-lookup"><span data-stu-id="28269-125">Functionally, both returned and rejected entries behave the same as an entry that has a status of **Draft**.</span></span> <span data-ttu-id="28269-126">Thành viên nhóm dự án có thể thực hiện bất kỳ thay đổi nào cần thiết cho mục nhập và sau đó gửi lại để phê duyệt hoặc xóa hoàn toàn mục nhập.</span><span class="sxs-lookup"><span data-stu-id="28269-126">A project team member can either make any required changes to the entry and then resubmit it for approval, or delete the entry entirely.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="28269-127">Tác động tài chính</span><span class="sxs-lookup"><span data-stu-id="28269-127">Financial impact</span></span>

<span data-ttu-id="28269-128">Dự án cũng bị ảnh hưởng về tài chính khi phê duyệt bị hủy bỏ.</span><span class="sxs-lookup"><span data-stu-id="28269-128">A project is also affected financially when an approval is canceled.</span></span> <span data-ttu-id="28269-129">Đầu tiên, thực tế tương ứng cho chi phí và doanh số được cập nhật theo cách sau:</span><span class="sxs-lookup"><span data-stu-id="28269-129">First, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="28269-130">Trạng thái điều chỉnh được đặt thành **Đã điều chỉnh**.</span><span class="sxs-lookup"><span data-stu-id="28269-130">The adjustment status is set to **Adjusted**.</span></span>
- <span data-ttu-id="28269-131">Trạng thái lập hóa đơn được đặt thành **Đã hủy**.</span><span class="sxs-lookup"><span data-stu-id="28269-131">The billing status is set to **Canceled**.</span></span>

<span data-ttu-id="28269-132">Tiếp theo, mục nhập đảo ngược được tạo trong bảng Thực tế.</span><span class="sxs-lookup"><span data-stu-id="28269-132">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="28269-133">Để tạo các mục nhập đảo ngược, hệ thống sẽ sao chép trên các giá trị trường từ thực tế gốc.</span><span class="sxs-lookup"><span data-stu-id="28269-133">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="28269-134">Giá trị duy nhất không được sao chép sang là giá trị số lượng.</span><span class="sxs-lookup"><span data-stu-id="28269-134">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="28269-135">Các giá trị này bị đảo ngược.</span><span class="sxs-lookup"><span data-stu-id="28269-135">These values are reversed instead.</span></span> <span data-ttu-id="28269-136">Thực tế đảo ngược được tạo cho cả thực tế **Chi phí** và **Doanh số chưa lập hóa đơn**.</span><span class="sxs-lookup"><span data-stu-id="28269-136">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="28269-137">Trường **Trạng thái điều chỉnh** trên thực tế đảo ngược được đặt thành **Không thể điều chỉnh** và trạng thái lập hóa đơn được đặt thành **Đã hủy**.</span><span class="sxs-lookup"><span data-stu-id="28269-137">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the billing status is set to **Canceled**.</span></span>

<span data-ttu-id="28269-138">Sau khi thực hiện các thay đổi này, số lượng được ghi dưới dạng đã sử dụng trên dự án và nhật ký doanh thu trên dự án sẽ không tính đến số lượng của những thực tế này nữa.</span><span class="sxs-lookup"><span data-stu-id="28269-138">After these changes are made, the amount that is recorded as spent on the project and the revenue backlog on the project will longer account for the amounts that these actuals represent.</span></span>
