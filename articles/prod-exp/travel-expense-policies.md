---
title: Thiết lập chính sách chi phí
description: Bạn có thể thiết lập các chính sách chi phí mà nhân viên của bạn phải tuân theo khi nhập và gửi báo cáo chi phí cũng như tiêu chuẩn đi lại trong Microsoft Dynamics 365 Finance.
author: suvaidya
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fa4f628a918e6e099a723ed05994f63d6ad847f5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005772"
---
# <a name="set-up-expense-policies"></a><span data-ttu-id="140af-103">Thiết lập chính sách chi phí</span><span class="sxs-lookup"><span data-stu-id="140af-103">Set up expense policies</span></span>

<span data-ttu-id="140af-104">Bạn có thể xác định các chính sách mà nhân viên của bạn phải tuân theo khi nhập và gửi báo cáo chi phí cũng như tiêu chuẩn đi lại.</span><span class="sxs-lookup"><span data-stu-id="140af-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="140af-105">Thực hiện các chính sách chi phí có thể giúp bạn quản lý chi phí một cách hiệu quả.</span><span class="sxs-lookup"><span data-stu-id="140af-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="140af-106">Ví dụ: bạn có thể đặt chính sách cho chi phí khách sạn ở New York City, trong đó quy định rằng chi phí mỗi đêm không được vượt quá 250 USD.</span><span class="sxs-lookup"><span data-stu-id="140af-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="140af-107">Nếu một nhân viên nộp báo cáo chi phí hoặc tiêu chuẩn đi lại mà giá phòng vượt quá số tiền này, hệ thống sẽ thông báo</span><span class="sxs-lookup"><span data-stu-id="140af-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="140af-108">cho nhân viên rằng số tiền theo chính sách cho chi phí đó đã bị vượt quá.</span><span class="sxs-lookup"><span data-stu-id="140af-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="140af-109">Bạn có thể đặt cấu hình thông báo mà nhân viên sẽ nhận được khi bạn</span><span class="sxs-lookup"><span data-stu-id="140af-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="140af-110">xác định chính sách.</span><span class="sxs-lookup"><span data-stu-id="140af-110">define the policy.</span></span>      
        
<span data-ttu-id="140af-111">Bạn có thể xác định 3 loại chính sách:</span><span class="sxs-lookup"><span data-stu-id="140af-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="140af-112">Cảnh báo – Cho phép nhân viên gửi báo cáo chi phí hoặc tiêu chuẩn đi lại nhưng chi phí sẽ được đánh dấu cho tất cả những người phê duyệt và</span><span class="sxs-lookup"><span data-stu-id="140af-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="140af-113">cho báo cáo về sau.</span><span class="sxs-lookup"><span data-stu-id="140af-113">for later reporting.</span></span>        

- <span data-ttu-id="140af-114">Lỗi – Yêu cầu nhân viên sửa đổi chi phí để tuân thủ chính sách trước khi gửi báo cáo chi phí hoặc tiêu chuẩn đi lại.</span><span class="sxs-lookup"><span data-stu-id="140af-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="140af-115">Chứng minh – Yêu cầu nhân viên hoặc người quản lý nhập chứng minh cho việc vượt quá số tiền theo chính sách trước khi gửi báo cáo chi phí hoặc tiêu chuẩn đi lại.</span><span class="sxs-lookup"><span data-stu-id="140af-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="140af-116">Mẹo chính sách</span><span class="sxs-lookup"><span data-stu-id="140af-116">Policy tips</span></span>
<span data-ttu-id="140af-117">Dưới đây là một số gợi ý có thể hỗ trợ bạn khi tạo các chính sách mới để quản lý chi phí.</span><span class="sxs-lookup"><span data-stu-id="140af-117">Here are a few suggestions that can assist you when creating new policies for expense management.</span></span> 
* <span data-ttu-id="140af-118">Các chính sách có hiệu lực theo ngày và sẽ không có hiệu lực nếu được tạo vào ngày sau ngày chi phí phát sinh.</span><span class="sxs-lookup"><span data-stu-id="140af-118">Policies are date effective and won't take effect if the policy is created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="140af-119">Ví dụ: nếu bạn đang tạo một chính sách mới hôm nay để thực thi chi phí bữa ăn tối đa là 50 USD, thì mọi chi phí hiện có đã nhập tính đến ngày hôm qua sẽ không được kiểm tra với chính sách này.</span><span class="sxs-lookup"><span data-stu-id="140af-119">For example, if you are creating a new policy today to enforce a maximum meal expense of $50, then any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
* <span data-ttu-id="140af-120">Khi tạo chính sách cho danh mục chi phí có thể được chia thành từng khoản mục, hãy xem xét thêm điều kiện cho loại dòng chi phí.</span><span class="sxs-lookup"><span data-stu-id="140af-120">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="140af-121">Một số chính sách như yêu cầu biên lai có thể không có ý nghĩa đối với các dòng được chia thành từng khoản và chỉ nên được áp dụng cho dòng tiêu đề hoặc dòng không được chia thành từng khoản.</span><span class="sxs-lookup"><span data-stu-id="140af-121">Some policies such as requiring a receipt may not make sense for itemized lines and should only be applied to the header line or a non-itemized line.</span></span> 
* <span data-ttu-id="140af-122">Các chính sách quản lý chi phí được đánh giá dựa trên thực thể nguồn theo mặc định.</span><span class="sxs-lookup"><span data-stu-id="140af-122">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="140af-123">Đối với các tình huống liên công ty, bạn có thể đặt chính sách cần đánh giá dựa trên thực thể đích (thực thể mượn).</span><span class="sxs-lookup"><span data-stu-id="140af-123">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="140af-124">Để chạy các chính sách dựa trên thực thể đích, hãy bật tính năng "Đánh giá chính sách chi phí dựa trên pháp nhân mượn" trong không gian làm việc **Quản lý tính năng**.</span><span class="sxs-lookup"><span data-stu-id="140af-124">To run the policies against the destination entity, turn on the "Evaluate Expense policy against borrowing legal entity" feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="140af-125">Thời điểm đánh giá chính sách</span><span class="sxs-lookup"><span data-stu-id="140af-125">When to evaluate policies</span></span>

<span data-ttu-id="140af-126">Trong các tham số quản lý chi phí, có thể đánh giá các chính sách quản lý chi phí khi một dòng được lưu hoặc khi báo cáo chi phí được gửi.</span><span class="sxs-lookup"><span data-stu-id="140af-126">In expense management parameters, there is an option to either evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="140af-127">Nếu bạn chọn đánh giá vào thời điểm lưu dòng, điều này đảm bảo rằng người dùng sớm thấy được những gì mình cần làm để hoàn thành báo cáo chi phí của mình cùng một lúc.</span><span class="sxs-lookup"><span data-stu-id="140af-127">If you choose to evaluate when a line is saved this ensures that users have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="140af-128">Nếu không, bạn có thể trì hoãn việc đánh giá chính sách và tiết kiệm thời gian nếu có xác thực vào lúc cuối, trong khi gửi lên quy trình làm việc.</span><span class="sxs-lookup"><span data-stu-id="140af-128">Otherwise, you can delay policy evaluation and save time if you have validation occur at the end, during submission to workflow.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]