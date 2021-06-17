---
title: Tổng quan về phê duyệt
description: Chủ đề này cung cấp thông tin về cách làm việc với các mục phê duyệt trong Project Operations.
author: stsporen
ms.date: 03/31/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 5e30b8a386805faee869f77e695d5ee492d78cdb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996727"
---
# <a name="approvals-overview"></a><span data-ttu-id="16194-103">Tổng quan về phê duyệt</span><span class="sxs-lookup"><span data-stu-id="16194-103">Approvals overview</span></span>

<span data-ttu-id="16194-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="16194-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="16194-105">Các mục nhập thời gian, chi phí và mức sử dụng vật tư đã gửi sẽ chuyển qua quy trình làm việc phê duyệt.</span><span class="sxs-lookup"><span data-stu-id="16194-105">Time, expense, and material usage submissions move through an approval workflow.</span></span> <span data-ttu-id="16194-106">Sau khi các mục nhập được phê duyệt, các giao dịch được ghi lại trong thực tế hoặc thời gian được đăng ký trong lịch trình.</span><span class="sxs-lookup"><span data-stu-id="16194-106">After the entries are approved, transactions are recorded in actuals or time is booked in the schedule.</span></span>

## <a name="approvals-workflow"></a><span data-ttu-id="16194-107">Quy trình làm việc phê duyệt</span><span class="sxs-lookup"><span data-stu-id="16194-107">Approvals workflow</span></span>
<span data-ttu-id="16194-108">Khi bạn tạo và gửi mục nhập thời gian, chi phí hoặc mức sử dụng vật tư, thì một bản ghi phê duyệt sẽ được tạo.</span><span class="sxs-lookup"><span data-stu-id="16194-108">When you create and submit a time, expense, or material usage entry, an approval record is created.</span></span> <span data-ttu-id="16194-109">Người phê duyệt dự án hoặc người quản lý xem xét và phê duyệt mục nhập đó.</span><span class="sxs-lookup"><span data-stu-id="16194-109">The project approver or manager reviews and approves the entry.</span></span> <span data-ttu-id="16194-110">Nếu mục nhập có liên quan đến một dự án, các giá trị thực tế sẽ được tạo ra khi mục nhập được phê duyệt.</span><span class="sxs-lookup"><span data-stu-id="16194-110">If the entry is related to a project, the actuals will be created when it's approved.</span></span> <span data-ttu-id="16194-111">Điều này cho phép theo dõi chi phí và thanh toán.</span><span class="sxs-lookup"><span data-stu-id="16194-111">This allows the cost and billing to be tracked.</span></span>

## <a name="approve-an-entry"></a><span data-ttu-id="16194-112">Phê duyệt một mục nhập</span><span class="sxs-lookup"><span data-stu-id="16194-112">Approve an entry</span></span>
<span data-ttu-id="16194-113">Trang **Phê duyệt** cho phép bạn chuyển đổi giữa các dạng xem khác nhau để bạn có thể xem các loại phê duyệt khác nhau.</span><span class="sxs-lookup"><span data-stu-id="16194-113">The **Approvals** page allows you to switch between different views so that you can view the different types of approvals.</span></span>
  
1. <span data-ttu-id="16194-114">Đi đến trang **Phê duyệt** rồi chọn **Chi phí**, **Thời gian**, **Sử dụng vật tư** hoặc **Thu hồi**.</span><span class="sxs-lookup"><span data-stu-id="16194-114">Go to the **Approvals** page and select **Expenses**, **Time**, **Material Usage**, or **Recalls**.</span></span>
2. <span data-ttu-id="16194-115">Đánh giá từng phê duyệt và chọn những phê duyệt mà bạn muốn phê duyệt.</span><span class="sxs-lookup"><span data-stu-id="16194-115">Review each approval, and select the ones you want to approve.</span></span>
3. <span data-ttu-id="16194-116">Chọn **Phê duyệt** để phê duyệt các mục nhập đã chọn.</span><span class="sxs-lookup"><span data-stu-id="16194-116">Select **Approve** to approve the selected entries.</span></span>
<span data-ttu-id="16194-117">Hệ thống xử lý các mục nhập này và tạo các giá trị thực tế.</span><span class="sxs-lookup"><span data-stu-id="16194-117">The system processes these entries and create actuals.</span></span>

## <a name="reject-an-entry"></a><span data-ttu-id="16194-118">Từ chối một mục nhập</span><span class="sxs-lookup"><span data-stu-id="16194-118">Reject an entry</span></span>
<span data-ttu-id="16194-119">Với tư cách là người phê duyệt dự án, bạn có thể phải gửi lại mục nhập cho người dùng để chỉnh sửa.</span><span class="sxs-lookup"><span data-stu-id="16194-119">As the Project approver, you may have to send an entry back to a user for correction.</span></span>
  
1. <span data-ttu-id="16194-120">Đi đến **Phê duyệt** rồi chọn mục nhập để từ chối.</span><span class="sxs-lookup"><span data-stu-id="16194-120">Go to the **Approvals** page and select the entry to reject.</span></span> 
2. <span data-ttu-id="16194-121">Chọn **Từ chối**.</span><span class="sxs-lookup"><span data-stu-id="16194-121">Select **Reject**.</span></span>
3. <span data-ttu-id="16194-122">Bạn cũng có thể chọn cách thêm nhận xét trong hộp thoại **Nhận xét về lý do từ chối** để thông báo cho người dùng lý do tại sao mục nhập lại bị từ chối.</span><span class="sxs-lookup"><span data-stu-id="16194-122">Optional, add a comment in the **Rejection Comments** dialog box to inform the user why the entry is being rejected.</span></span>
4. <span data-ttu-id="16194-123">Chọn **OK**.</span><span class="sxs-lookup"><span data-stu-id="16194-123">Select **OK**.</span></span> <span data-ttu-id="16194-124">Mục nhập sẽ được trả lại cho người dùng.</span><span class="sxs-lookup"><span data-stu-id="16194-124">The entry will be returned to the user.</span></span>
  
## <a name="cancel-approval"></a><span data-ttu-id="16194-125">Hủy phê duyệt</span><span class="sxs-lookup"><span data-stu-id="16194-125">Cancel approval</span></span>
<span data-ttu-id="16194-126">Trong một số trường hợp, bạn có thể cần phải hủy mục nhập đã được phê duyệt trước đó.</span><span class="sxs-lookup"><span data-stu-id="16194-126">In some cases, you might need to cancel a previously approved entry.</span></span> <span data-ttu-id="16194-127">Việc hủy một mục nhập đã được phê duyệt trước đó sẽ có ảnh hưởng đến tài chính.</span><span class="sxs-lookup"><span data-stu-id="16194-127">Canceling a previously approved entry will have a financial impact.</span></span> 

## <a name="approving-recall-requests"></a><span data-ttu-id="16194-128">Phê duyệt yêu cầu thu hồi</span><span class="sxs-lookup"><span data-stu-id="16194-128">Approving recall requests</span></span>
<span data-ttu-id="16194-129">Trong một số trường hợp, tư vấn viên có thể cần thu hồi một mục nhập đã được phê duyệt trước đó.</span><span class="sxs-lookup"><span data-stu-id="16194-129">In some cases, a consultant may need to recall a previously approved entry.</span></span> <span data-ttu-id="16194-130">Việc hủy một mục nhập đã được phê duyệt trước đó sẽ có ảnh hưởng đến tài chính.</span><span class="sxs-lookup"><span data-stu-id="16194-130">Canceling a previously approved entry will have a financial impact.</span></span> <span data-ttu-id="16194-131">Người phê duyệt dự án cần phải phê duyệt việc thu hồi để đảo ngược giao dịch trong mục Giá trị thực tế.</span><span class="sxs-lookup"><span data-stu-id="16194-131">The project approver is required to approve the recall to reverse the transaction in Actuals.</span></span>

## <a name="specify-project-approvers"></a><span data-ttu-id="16194-132">Chỉ định người phê duyệt dự án</span><span class="sxs-lookup"><span data-stu-id="16194-132">Specify Project approvers</span></span>
<span data-ttu-id="16194-133">Mỗi dự án có một số thành viên trong nhóm dự án.</span><span class="sxs-lookup"><span data-stu-id="16194-133">Each project has a number of project team members.</span></span> <span data-ttu-id="16194-134">Bạn có thể chỉ định thành viên nào trong nhóm cũng là người phê duyệt dự án.</span><span class="sxs-lookup"><span data-stu-id="16194-134">You can specify which team members are also Project approvers.</span></span>

1. <span data-ttu-id="16194-135">Đi đến **Dự án** và mở dự án từ danh sách.</span><span class="sxs-lookup"><span data-stu-id="16194-135">Go to the **Projects** page and open the project from the list.</span></span>
2. <span data-ttu-id="16194-136">Tên tab **Nhóm**, chọn thành viên nhóm sẽ là người phê duyệt dự án, sau đó chọn **Chỉnh sửa**.</span><span class="sxs-lookup"><span data-stu-id="16194-136">On the **Team** tab, select the team member who will be a Project approver and then select **Edit**.</span></span>
3. <span data-ttu-id="16194-137">Đặt trường **Người phê duyệt dự án** thành **Có**.</span><span class="sxs-lookup"><span data-stu-id="16194-137">Set the **Project Approver** field to **Yes**.</span></span>
4. <span data-ttu-id="16194-138">Chọn **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="16194-138">Select **Save**.</span></span>
5. <span data-ttu-id="16194-139">Lặp lại các bước 2-4 để thêm người phê duyệt dự án bổ sung.</span><span class="sxs-lookup"><span data-stu-id="16194-139">Repeat steps 2-4 to add additional Project approvers.</span></span>

## <a name="configure-the-users-manager"></a><span data-ttu-id="16194-140">Định cấu hình người quản lý của người dùng</span><span class="sxs-lookup"><span data-stu-id="16194-140">Configure the user's manager</span></span>

1. <span data-ttu-id="16194-141">Đi tới **Thiết đặt** > **Bảo mật** > **Người dùng**.</span><span class="sxs-lookup"><span data-stu-id="16194-141">Go to **Settings** > **Security** > **Users**.</span></span>
2. <span data-ttu-id="16194-142">Chọn người dùng mà bạn đang phân công người quản lý và trong vùng **Thông tin tổ chức**, chọn người quản lý từ danh sách.</span><span class="sxs-lookup"><span data-stu-id="16194-142">Select the user to whom you are assigning a manager and in the **Organization Information** area, select the manager from the list.</span></span> 
3. <span data-ttu-id="16194-143">Chọn **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="16194-143">Select **Save**.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
