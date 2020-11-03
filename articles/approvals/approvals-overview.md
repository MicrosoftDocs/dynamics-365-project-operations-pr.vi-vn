---
title: Tổng quan về phê duyệt
description: Chủ đề này cung cấp thông tin về cách làm việc với các mục phê duyệt trong Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 37994422e9146765076fdbb77f5c763b4f1d0802
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086968"
---
# <a name="approvals-overview"></a><span data-ttu-id="a0776-103">Tổng quan về phê duyệt</span><span class="sxs-lookup"><span data-stu-id="a0776-103">Approvals overview</span></span>

<span data-ttu-id="a0776-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="a0776-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a0776-105">Thời gian và nộp chi phí chuyển qua một quy trình làm việc phê duyệt.</span><span class="sxs-lookup"><span data-stu-id="a0776-105">Time and Expense submissions move through an approval workflow.</span></span> <span data-ttu-id="a0776-106">Sau khi các mục nhập được phê duyệt, các giao dịch được ghi lại trong thực tế hoặc thời gian được đăng ký trong lịch trình.</span><span class="sxs-lookup"><span data-stu-id="a0776-106">After the entries are approved, transactions are recorded in actuals or time is booked in the schedule.</span></span>

## <a name="approvals-workflow"></a><span data-ttu-id="a0776-107">Quy trình làm việc phê duyệt</span><span class="sxs-lookup"><span data-stu-id="a0776-107">Approvals workflow</span></span>
<span data-ttu-id="a0776-108">Khi bạn tạo và gửi mục nhập thời gian hoặc chi phí, mục nhập phê duyệt sẽ được tạo.</span><span class="sxs-lookup"><span data-stu-id="a0776-108">When you create and submit a time or expense entry, an approval entry is created.</span></span> <span data-ttu-id="a0776-109">Người phê duyệt dự án hoặc người quản lý đánh giá và chấp thuận mục nhập của bạn.</span><span class="sxs-lookup"><span data-stu-id="a0776-109">The Project approver or your manager reviews and approves your entry.</span></span> <span data-ttu-id="a0776-110">Nếu mục nhập liên quan đến một dự án, khi được phê duyệt, các giá trị thực tế sẽ được tạo.</span><span class="sxs-lookup"><span data-stu-id="a0776-110">If the entry is related to a project, when it's approved, the actuals will be created.</span></span> <span data-ttu-id="a0776-111">Điều này cho phép theo dõi chi phí và thanh toán.</span><span class="sxs-lookup"><span data-stu-id="a0776-111">This allows the cost and billing to be tracked.</span></span> 

## <a name="approve-an-entry"></a><span data-ttu-id="a0776-112">Phê duyệt một mục nhập</span><span class="sxs-lookup"><span data-stu-id="a0776-112">Approve an entry</span></span>
<span data-ttu-id="a0776-113">Biểu mẫu **Phê duyệt** cho phép bạn chuyển đổi giữa các dạng xem khác nhau để bạn có thể xem các loại phê duyệt khác nhau.</span><span class="sxs-lookup"><span data-stu-id="a0776-113">The **Approvals** form allows you to switch between different views so that you can view the different types of approvals.</span></span>
  
1. <span data-ttu-id="a0776-114">Đi đến biểu mẫu **Phê duyệt** và chọn **Chi phí** , **Thời gian** hoặc **Thu hồi**.</span><span class="sxs-lookup"><span data-stu-id="a0776-114">Go to the **Approvals** form and select **Expenses** , **Time** , or **Recalls**.</span></span>
2. <span data-ttu-id="a0776-115">Đánh giá từng phê duyệt và chọn những phê duyệt mà bạn muốn phê duyệt.</span><span class="sxs-lookup"><span data-stu-id="a0776-115">Review each approval, and select the ones you want to approve.</span></span>
3. <span data-ttu-id="a0776-116">Chọn **Phê duyệt** để phê duyệt các mục nhập đã chọn.</span><span class="sxs-lookup"><span data-stu-id="a0776-116">Select **Approve** to approve the selected entries.</span></span>
<span data-ttu-id="a0776-117">Hệ thống sẽ xử lý các mục nhập này và tạo các giá trị thực tế hoặc đăng ký.</span><span class="sxs-lookup"><span data-stu-id="a0776-117">The system will process these entries and create actuals or a booking.</span></span>

## <a name="reject-an-entry"></a><span data-ttu-id="a0776-118">Từ chối một mục nhập</span><span class="sxs-lookup"><span data-stu-id="a0776-118">Reject an entry</span></span>
<span data-ttu-id="a0776-119">Với tư cách là người phê duyệt dự án, bạn có thể phải gửi lại mục nhập cho người dùng để chỉnh sửa.</span><span class="sxs-lookup"><span data-stu-id="a0776-119">As the Project approver, you may have to send an entry back to a user for correction.</span></span>
  
1. <span data-ttu-id="a0776-120">Đi đến biểu mẫu **Phê duyệt** và chọn mục nhập để từ chối.</span><span class="sxs-lookup"><span data-stu-id="a0776-120">Go to the **Approvals** form and select the entry to reject.</span></span> 
2. <span data-ttu-id="a0776-121">Chọn **Từ chối**.</span><span class="sxs-lookup"><span data-stu-id="a0776-121">Select **Reject**.</span></span>
3. <span data-ttu-id="a0776-122">Tùy chọn - Thêm nhận xét trong hộp thoại **Nhận xét từ chối** để thông báo cho người dùng lý do từ chối mục nhập.</span><span class="sxs-lookup"><span data-stu-id="a0776-122">Optional - Add a comment in the **Rejection Comments** dialog to inform the user why the entry is being rejected.</span></span>
4. <span data-ttu-id="a0776-123">Chọn **OK**.</span><span class="sxs-lookup"><span data-stu-id="a0776-123">Select **OK**.</span></span> <span data-ttu-id="a0776-124">Mục nhập sẽ được trả lại cho người dùng.</span><span class="sxs-lookup"><span data-stu-id="a0776-124">The entry will be returned to the user.</span></span>
  
## <a name="recall-entries"></a><span data-ttu-id="a0776-125">Thu hồi mục nhập</span><span class="sxs-lookup"><span data-stu-id="a0776-125">Recall entries</span></span>
<span data-ttu-id="a0776-126">Tại một số thời điểm, bạn có thể cần phải thu hồi mục nhập đã gửi.</span><span class="sxs-lookup"><span data-stu-id="a0776-126">At some point, you might need to recall a submitted entry.</span></span> <span data-ttu-id="a0776-127">Nếu chưa được duyệt, mục nhập sẽ bị trả lại ngay.</span><span class="sxs-lookup"><span data-stu-id="a0776-127">If the entry has not been approved, it will be returned immediately.</span></span> <span data-ttu-id="a0776-128">Tuy nhiên, một mục nhập đã được phê duyệt có thể có tác động đáng kể.</span><span class="sxs-lookup"><span data-stu-id="a0776-128">An approved entry however, may have a material impact.</span></span> <span data-ttu-id="a0776-129">Người phê duyệt dự án được yêu cầu phê duyệt việc thu hồi để đảo ngược giao dịch trong Thực tế.</span><span class="sxs-lookup"><span data-stu-id="a0776-129">The Project approver is required to approve the recall in order to reverse the transaction in Actuals.</span></span>

## <a name="specify-project-approvers"></a><span data-ttu-id="a0776-130">Chỉ định người phê duyệt dự án</span><span class="sxs-lookup"><span data-stu-id="a0776-130">Specify Project approvers</span></span>
<span data-ttu-id="a0776-131">Mỗi dự án có một số thành viên trong nhóm dự án.</span><span class="sxs-lookup"><span data-stu-id="a0776-131">Each project has a number of project team members.</span></span> <span data-ttu-id="a0776-132">Bạn có thể chỉ định thành viên nào trong nhóm cũng là người phê duyệt dự án.</span><span class="sxs-lookup"><span data-stu-id="a0776-132">You can specify which team members are also Project approvers.</span></span>

1. <span data-ttu-id="a0776-133">Đi đến biểu mẫu **Dự án** và mở dự án từ danh sách.</span><span class="sxs-lookup"><span data-stu-id="a0776-133">Go to the **Projects** form and open the project from the list.</span></span>
2. <span data-ttu-id="a0776-134">Tên tab **Nhóm** , chọn thành viên nhóm sẽ là người phê duyệt dự án, sau đó chọn **Chỉnh sửa**.</span><span class="sxs-lookup"><span data-stu-id="a0776-134">On the **Team** tab, select the team member who will be a Project approver and then select **Edit**.</span></span>
3. <span data-ttu-id="a0776-135">Đặt trường **Người phê duyệt dự án** thành **Có**.</span><span class="sxs-lookup"><span data-stu-id="a0776-135">Set the **Project Approver** field to **Yes**.</span></span>
4. <span data-ttu-id="a0776-136">Chọn **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="a0776-136">Select **Save**.</span></span>
5. <span data-ttu-id="a0776-137">Lặp lại các bước 2-4 để thêm người phê duyệt dự án bổ sung.</span><span class="sxs-lookup"><span data-stu-id="a0776-137">Repeat steps 2-4 to add additional Project approvers.</span></span>

## <a name="configure-the-users-manager"></a><span data-ttu-id="a0776-138">Định cấu hình người quản lý của người dùng</span><span class="sxs-lookup"><span data-stu-id="a0776-138">Configure the user's manager</span></span>

1. <span data-ttu-id="a0776-139">Đi tới **Thiết đặt** > **Bảo mật** > **Người dùng**.</span><span class="sxs-lookup"><span data-stu-id="a0776-139">Go to **Settings** > **Security** > **Users**.</span></span>
2. <span data-ttu-id="a0776-140">Chọn người dùng mà bạn đang phân công người quản lý và trong vùng **Thông tin tổ chức** , chọn người quản lý từ danh sách.</span><span class="sxs-lookup"><span data-stu-id="a0776-140">Select the user to whom you are assigning a manager and in the **Organization Information** area, select the manager from the list.</span></span> 
3. <span data-ttu-id="a0776-141">Chọn **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="a0776-141">Select **Save**.</span></span>


