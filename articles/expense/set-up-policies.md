---
title: Xác định chính sách chi phí
description: Bạn có thể xác định các chính sách chi phí mà nhân viên của bạn phải tuân theo khi nhập và gửi báo cáo chi phí cũng như tiêu chuẩn đi lại.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: c55cec132649daf9ee08ea4d8db3668860247934
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128444"
---
# <a name="define-expense-policies"></a><span data-ttu-id="df2e8-103">Xác định chính sách chi phí</span><span class="sxs-lookup"><span data-stu-id="df2e8-103">Define expense policies</span></span>

<span data-ttu-id="df2e8-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="df2e8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="df2e8-105">Bạn có thể xác định các chính sách mà nhân viên của bạn phải tuân theo khi nhập và gửi báo cáo chi phí cũng như tiêu chuẩn đi lại.</span><span class="sxs-lookup"><span data-stu-id="df2e8-105">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="df2e8-106">Thực hiện các chính sách chi phí có thể giúp bạn quản lý chi phí một cách hiệu quả.</span><span class="sxs-lookup"><span data-stu-id="df2e8-106">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="df2e8-107">Ví dụ: bạn có thể đặt chính sách cho chi phí khách sạn ở New York City, trong đó quy định rằng chi phí mỗi đêm không được vượt quá 250 USD.</span><span class="sxs-lookup"><span data-stu-id="df2e8-107">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="df2e8-108">Nếu một nhân viên nộp báo cáo chi phí hoặc tiêu chuẩn đi lại mà giá phòng vượt quá số tiền này, hệ thống sẽ thông báo</span><span class="sxs-lookup"><span data-stu-id="df2e8-108">If a worker submits an expense report or travel requisition where the room rate exceeds this amount, the system will notify the</span></span>         
<span data-ttu-id="df2e8-109">cho nhân viên rằng số tiền theo chính sách cho chi phí đó đã bị vượt quá.</span><span class="sxs-lookup"><span data-stu-id="df2e8-109">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="df2e8-110">Bạn có thể đặt cấu hình thông báo mà nhân viên sẽ nhận được khi bạn</span><span class="sxs-lookup"><span data-stu-id="df2e8-110">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="df2e8-111">xác định chính sách.</span><span class="sxs-lookup"><span data-stu-id="df2e8-111">define the policy.</span></span>      
        
<span data-ttu-id="df2e8-112">Bạn có thể xác định 3 loại chính sách:</span><span class="sxs-lookup"><span data-stu-id="df2e8-112">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="df2e8-113">**Cảnh báo**: Cho phép nhân viên gửi báo cáo chi phí hoặc tiêu chuẩn đi lại nhưng chi phí sẽ được đánh dấu cho tất cả những người phê duyệt và</span><span class="sxs-lookup"><span data-stu-id="df2e8-113">**Warning**: Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>         
  <span data-ttu-id="df2e8-114">cho báo cáo về sau.</span><span class="sxs-lookup"><span data-stu-id="df2e8-114">for later reporting.</span></span>        

- <span data-ttu-id="df2e8-115">**Lỗi**: Yêu cầu nhân viên sửa đổi chi phí để tuân thủ chính sách trước khi gửi báo cáo chi phí hoặc tiêu chuẩn đi lại.</span><span class="sxs-lookup"><span data-stu-id="df2e8-115">**Error**: Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>        
 
 - <span data-ttu-id="df2e8-116">**Chứng minh**: Yêu cầu nhân viên hoặc người quản lý nhập chứng minh cho việc vượt quá số tiền theo chính sách trước khi gửi báo cáo chi phí hoặc tiêu chuẩn đi lại.</span><span class="sxs-lookup"><span data-stu-id="df2e8-116">**Justification**: Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="df2e8-117">Mẹo chính sách</span><span class="sxs-lookup"><span data-stu-id="df2e8-117">Policy tips</span></span>
<span data-ttu-id="df2e8-118">Dưới đây là một số gợi ý có thể hỗ trợ bạn khi tạo các chính sách mới để quản lý chi phí:</span><span class="sxs-lookup"><span data-stu-id="df2e8-118">Here are a few suggestions that can assist you when creating new policies for expense management:</span></span> 

- <span data-ttu-id="df2e8-119">Các chính sách có hiệu lực theo ngày có nghĩa là chính sách sẽ không có hiệu lực nếu được tạo vào ngày sau ngày chi phí phát sinh.</span><span class="sxs-lookup"><span data-stu-id="df2e8-119">Policies are date effective which means a policy won't take effect if it's created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="df2e8-120">Ví dụ: bạn tạo chính sách mới hôm nay để áp dụng cho chi phí bữa ăn tối đa là 50 USD.</span><span class="sxs-lookup"><span data-stu-id="df2e8-120">For example, you create a new policy today to enforce a maximum meal expense of $50.</span></span> <span data-ttu-id="df2e8-121">Bất kỳ chi phí hiện có nào đã nhập từ ngày hôm qua sẽ không được kiểm tra theo chính sách này.</span><span class="sxs-lookup"><span data-stu-id="df2e8-121">Any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
- <span data-ttu-id="df2e8-122">Khi tạo chính sách cho danh mục chi phí có thể được chia thành từng khoản mục, hãy xem xét thêm điều kiện cho loại dòng chi phí.</span><span class="sxs-lookup"><span data-stu-id="df2e8-122">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="df2e8-123">Một số chính sách, chẳng hạn như yêu cầu biên lai, có thể không áp dụng cho các dòng được chia thành từng khoản mục.</span><span class="sxs-lookup"><span data-stu-id="df2e8-123">Some policies, such as requiring a receipt, may not make sense for itemized lines.</span></span> <span data-ttu-id="df2e8-124">Trong trường hợp này, chính sách chỉ được áp dụng cho dòng tiêu đề hoặc dòng không được chia thành từng khoản mục.</span><span class="sxs-lookup"><span data-stu-id="df2e8-124">In this situation, the policy only is applied to the header line or a non-itemized line.</span></span> 
- <span data-ttu-id="df2e8-125">Các chính sách quản lý chi phí được đánh giá dựa trên thực thể nguồn theo mặc định.</span><span class="sxs-lookup"><span data-stu-id="df2e8-125">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="df2e8-126">Đối với các tình huống liên công ty, bạn có thể đặt chính sách cần đánh giá dựa trên thực thể đích (thực thể mượn).</span><span class="sxs-lookup"><span data-stu-id="df2e8-126">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="df2e8-127">Để chạy các chính sách dựa trên thực thể đích, hãy bật tính năng **Đánh giá chính sách chi phí dựa trên pháp nhân mượn** trong không gian làm việc **Quản lý tính năng**.</span><span class="sxs-lookup"><span data-stu-id="df2e8-127">To run the policies against the destination entity, turn on the **Evaluate Expense policy against borrowing legal entity** feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="df2e8-128">Thời điểm đánh giá chính sách</span><span class="sxs-lookup"><span data-stu-id="df2e8-128">When to evaluate policies</span></span>

<span data-ttu-id="df2e8-129">Trong các tham số quản lý chi phí, bạn có thể chọn để đánh giá các chính sách quản lý chi phí khi một dòng được lưu hoặc khi báo cáo chi phí được gửi.</span><span class="sxs-lookup"><span data-stu-id="df2e8-129">In expense management parameters, you can select to evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="df2e8-130">Nếu bạn chọn đánh giá vào thời điểm lưu dòng, người dùng sẽ sớm thấy được những gì mình cần làm để hoàn thành báo cáo chi phí của mình cùng một lúc.</span><span class="sxs-lookup"><span data-stu-id="df2e8-130">If you choose to evaluate when a line is saved, users will have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="df2e8-131">Nếu không, bạn có thể trì hoãn việc đánh giá chính sách và tiết kiệm thời gian bằng cách xác thực vào lúc cuối, trong khi gửi lên quy trình làm việc.</span><span class="sxs-lookup"><span data-stu-id="df2e8-131">Otherwise, you can delay policy evaluation and save time by validating at the end, during the submission to workflow.</span></span>
