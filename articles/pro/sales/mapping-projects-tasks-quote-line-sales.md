---
title: Ánh xạ dự án và tác vụ với mô tả báo giá dựa trên dự án
description: Chủ đề này cung cấp thông tin về cách ánh xạ các dự án và tác vụ thành một mô tả tác vụ dựa trên dự án.
author: rumant
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d1c98d6a903393a0afc0e94d7f9859d55b9dc1f7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994612"
---
# <a name="map-projects-and-tasks-to-a-project-based-quote-line"></a><span data-ttu-id="c4abb-103">Ánh xạ dự án và tác vụ với mô tả báo giá dựa trên dự án</span><span class="sxs-lookup"><span data-stu-id="c4abb-103">Map projects and tasks to a project-based quote line</span></span>

<span data-ttu-id="c4abb-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="c4abb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c4abb-105">Trên các mô tả báo giá dựa trên dự án, bạn có thể ánh xạ các nhiệm vụ cụ thể của một dự án đã được liên kết với mô tả báo giá.</span><span class="sxs-lookup"><span data-stu-id="c4abb-105">On project-based quote lines, you can map the specific tasks of a project that is already associated to a quote line.</span></span>

<span data-ttu-id="c4abb-106">Khi bạn ánh xạ các tác vụ với một mô tả báo giá, các mục sau đây bạn đã xác định trên mô tả báo giá sẽ chỉ áp dụng cho các tác vụ đó:</span><span class="sxs-lookup"><span data-stu-id="c4abb-106">When you map tasks to a quote line, the following items you defined on the quote line will only apply to those tasks:</span></span>

- <span data-ttu-id="c4abb-107">Phương thức thanh toán</span><span class="sxs-lookup"><span data-stu-id="c4abb-107">Billing method</span></span>
- <span data-ttu-id="c4abb-108">Tùy chọn về khả năng tính phí</span><span class="sxs-lookup"><span data-stu-id="c4abb-108">Chargeability options</span></span>
- <span data-ttu-id="c4abb-109">Giới hạn không vượt quá</span><span class="sxs-lookup"><span data-stu-id="c4abb-109">Not-to-exceed limits</span></span>
- <span data-ttu-id="c4abb-110">Khách hàng</span><span class="sxs-lookup"><span data-stu-id="c4abb-110">Customers</span></span>

<span data-ttu-id="c4abb-111">Ví dụ: bạn có thể có một dự án trong đó một giai đoạn là giá cố định và tất cả các giai đoạn khác là thời gian và vật tư.</span><span class="sxs-lookup"><span data-stu-id="c4abb-111">For example, you might have a project where one phase is fixed price and all the other phases are time and materials.</span></span> <span data-ttu-id="c4abb-112">Trong trường hợp này, bạn có thể liên kết giai đoạn đầu tiên và tất cả các tác vụ con của nó với mô tả báo giá cho giai đoạn đó bằng phương thức thanh toán giá cố định.</span><span class="sxs-lookup"><span data-stu-id="c4abb-112">In this case, you can associate the first phase, and all of its child tasks, to the quote line for that phase with a fixed price billing method.</span></span> <span data-ttu-id="c4abb-113">Sau đó, bạn có thể liên kết tất cả các giai đoạn khác với mô tả báo giá dựa trên thời gian và vật tư.</span><span class="sxs-lookup"><span data-stu-id="c4abb-113">You can then associate all the other phases to the time and materials-based quote line.</span></span>

## <a name="associate-tasks-to-project-based-quote-lines"></a><span data-ttu-id="c4abb-114">Liên kết tác vụ với mô tả báo giá dựa trên dự án</span><span class="sxs-lookup"><span data-stu-id="c4abb-114">Associate tasks to project-based quote lines</span></span>

<span data-ttu-id="c4abb-115">Bạn có thể liên kết các tác vụ với các mô tả báo giá từ các vị trí sau đây:</span><span class="sxs-lookup"><span data-stu-id="c4abb-115">You can associate tasks with quote lines from the following locations:</span></span>

- <span data-ttu-id="c4abb-116">Trang **Dự án** > tab **Thanh toán theo tác vụ** (tối ưu)</span><span class="sxs-lookup"><span data-stu-id="c4abb-116">**Project** page > **Task billing** tab (optimal)</span></span>
- <span data-ttu-id="c4abb-117">Trang **Mô tả báo giá** > tab **Tác vụ có thể tính phí**</span><span class="sxs-lookup"><span data-stu-id="c4abb-117">**Quote Line** page > **Chargeable tasks** tab</span></span> 

### <a name="from-the-project-page"></a><span data-ttu-id="c4abb-118">Từ trang Dự án</span><span class="sxs-lookup"><span data-stu-id="c4abb-118">From the Project page</span></span>

<span data-ttu-id="c4abb-119">Trang **Dự án** cung cấp trải nghiệm tối ưu cho việc liên kết các tác vụ với mô tả báo giá.</span><span class="sxs-lookup"><span data-stu-id="c4abb-119">The **Project** page provides the optimal experience for associating tasks to quote lines.</span></span> <span data-ttu-id="c4abb-120">Bạn có thể sử dụng trang này để chọn nhiều tác vụ và liên kết tất cả các tác vụ đó, cộng với các tác vụ con của chúng, với mô tả báo giá đã chọn.</span><span class="sxs-lookup"><span data-stu-id="c4abb-120">You can use this page to select multiple tasks and associate all of them, plus their child tasks, to the selected quote line.</span></span>

1. <span data-ttu-id="c4abb-121">Trên tab **Tổng quát** của mô tả báo giá dựa trên dự án, hãy xác minh là trường **Dự án** đã được điền vào.</span><span class="sxs-lookup"><span data-stu-id="c4abb-121">On the **General** tab of a project–based quote line, verify the **Project** field is filled out.</span></span>
2. <span data-ttu-id="c4abb-122">Trong trường **Các tác vụ được đưa vào**, chọn **Chỉ các tác vụ được chọn**.</span><span class="sxs-lookup"><span data-stu-id="c4abb-122">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="c4abb-123">Lưu mô tả báo giá dựa trên dự án.</span><span class="sxs-lookup"><span data-stu-id="c4abb-123">Save the project-based quote line.</span></span> <span data-ttu-id="c4abb-124">Khi biểu mẫu làm mới, tab **Tác vụ có thể tính phí** sẽ hiển thị.</span><span class="sxs-lookup"><span data-stu-id="c4abb-124">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="c4abb-125">Trên tab **Tổng quát**, chọn liên kết cho dự án từ trường **Dự án**.</span><span class="sxs-lookup"><span data-stu-id="c4abb-125">On the **General** tab, select the link for the project from the **Project** field.</span></span>
5. <span data-ttu-id="c4abb-126">Trên trang **Dự án**, chọn tab **Thanh toán theo tác vụ**.</span><span class="sxs-lookup"><span data-stu-id="c4abb-126">On the **Project** page, select the **Task billing** tab.</span></span>
6. <span data-ttu-id="c4abb-127">Trong lưới thứ hai, áp dụng cho thiết lập thanh toán theo tác vụ cụ thể, hãy chọn một hoặc nhiều tác vụ rồi chọn **Liên kết các mô tả báo giá**.</span><span class="sxs-lookup"><span data-stu-id="c4abb-127">In the second grid, which applies to task-specific billing setup, select one or more tasks and then select **Associate quote lines**.</span></span>
7. <span data-ttu-id="c4abb-128">Trong trang hộp thoại xuất hiện, hãy chọn một mô tả báo giá hiển thị các mô tả báo giá dựa trên dự án trên báo giá.</span><span class="sxs-lookup"><span data-stu-id="c4abb-128">In the dialog page that appears, select a quote line that displays project-based quote lines on the quote.</span></span>
8. <span data-ttu-id="c4abb-129">Trong trường **Loại thanh toán**, cho biết những tác vụ này có thể tính phí hay không.</span><span class="sxs-lookup"><span data-stu-id="c4abb-129">In the **Billing type** field, indicate if these tasks are chargeable or non-chargeable.</span></span>
9. <span data-ttu-id="c4abb-130">Chọn hộp kiểm để cho biết liệu liên kết có nên bao gồm tác vụ con của các tác vụ đã chọn hay không.</span><span class="sxs-lookup"><span data-stu-id="c4abb-130">Select the check box to indicate if the association should include child tasks of the selected tasks.</span></span> <span data-ttu-id="c4abb-131">Chọn hộp sẽ liên kết các tác vụ con của các tác vụ đã chọn với mô tả báo giá.</span><span class="sxs-lookup"><span data-stu-id="c4abb-131">Checking the box will associate the child tasks of the selected tasks to the quote line.</span></span>
10. <span data-ttu-id="c4abb-132">Chọn **OK** để đóng hộp thoại.</span><span class="sxs-lookup"><span data-stu-id="c4abb-132">Select **OK** to close the dialog.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="c4abb-133">Từ trang Mô tả báo giá</span><span class="sxs-lookup"><span data-stu-id="c4abb-133">From the Quote line page</span></span>

<span data-ttu-id="c4abb-134">Bạn có thể liên kết các tác vụ dự án với mô tả báo giá từ tab **Tác vụ có thể tính phí** trên trang **Mô tả báo giá**.</span><span class="sxs-lookup"><span data-stu-id="c4abb-134">You can associate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

>[!NOTE]
><span data-ttu-id="c4abb-135">Nơi tối ưu để liên kết tác vụ dự án vào mô tả báo giá là trên tab **Thanh toán theo tác vụ** trên trang **Dự án**.</span><span class="sxs-lookup"><span data-stu-id="c4abb-135">The optimal place to associate project tasks to quote lines is on the **Task billing** tab on the **Project** page.</span></span> <span data-ttu-id="c4abb-136">Nếu bạn liên kết các tác vụ từ tab **Tác vụ có thể tính phí** trên trang **Mô tả báo giá**, bạn phải liên kết từng dự án theo cách thủ công.</span><span class="sxs-lookup"><span data-stu-id="c4abb-136">If you associate tasks from the **Chargeable tasks** tab on **Quote line** page, you must manually associate each project.</span></span>

1. <span data-ttu-id="c4abb-137">Trên tab **Tổng quát** của mô tả báo giá dựa trên dự án, hãy xác minh là có dự án được chọn trong trường **Dự án**.</span><span class="sxs-lookup"><span data-stu-id="c4abb-137">On the **General** tab of a project–based quote line, verify that there is a project selected in the **Project** field.</span></span>
2. <span data-ttu-id="c4abb-138">Trong trường **Các tác vụ được đưa vào**, chọn **Chỉ các tác vụ được chọn**.</span><span class="sxs-lookup"><span data-stu-id="c4abb-138">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="c4abb-139">Lưu mô tả báo giá dựa trên dự án.</span><span class="sxs-lookup"><span data-stu-id="c4abb-139">Save the project-based quote line.</span></span> <span data-ttu-id="c4abb-140">Khi biểu mẫu làm mới, tab **Tác vụ có thể tính phí** sẽ hiển thị.</span><span class="sxs-lookup"><span data-stu-id="c4abb-140">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="c4abb-141">Trên tab **Tác vụ có thể tính phí**, chọn **Thêm tác vụ mô tả báo giá**.</span><span class="sxs-lookup"><span data-stu-id="c4abb-141">On the **Chargeable tasks** tab, select **Add a quote line task**.</span></span>
5. <span data-ttu-id="c4abb-142">Trên trang **Tác vụ mô tả báo giá**, trong trường **Tác vụ**, chọn tác vụ và trong trường **Loại thanh toán**, chọn **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="c4abb-142">On the **Quote line task** page, in the **Tasks** field, select the task and in the **Billing type** field, select **Save**.</span></span> 
6. <span data-ttu-id="c4abb-143">Đóng trang.</span><span class="sxs-lookup"><span data-stu-id="c4abb-143">Close the page.</span></span> <span data-ttu-id="c4abb-144">Tác vụ vụ đã chọn bây giờ được liên kết với mô tả báo giá.</span><span class="sxs-lookup"><span data-stu-id="c4abb-144">The selected task is now associated to the quote line.</span></span>

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a><span data-ttu-id="c4abb-145">Dừng liên kết tác vụ với mô tả báo giá dựa trên dự án</span><span class="sxs-lookup"><span data-stu-id="c4abb-145">Disassociate tasks from project–based quote lines</span></span>

### <a name="from-the-project-page"></a><span data-ttu-id="c4abb-146">Từ trang Dự án</span><span class="sxs-lookup"><span data-stu-id="c4abb-146">From the Project page</span></span>

<span data-ttu-id="c4abb-147">Phương thức này cung cấp trải nghiệm tối ưu nhất cho việc dừng liên kết tác vụ với mô tả báo giá.</span><span class="sxs-lookup"><span data-stu-id="c4abb-147">This method provides the most optimal experience for disassociating tasks from quote lines.</span></span> <span data-ttu-id="c4abb-148">Bạn có thể chọn nhiều tác vụ và dừng liên kết tất cả các tác vụ đó và tác vụ con của chúng với mô tả báo giá đã chọn.</span><span class="sxs-lookup"><span data-stu-id="c4abb-148">You can select multiple tasks and disassociate all of the them, plus their child tasks, from the selected quote line.</span></span>

1. <span data-ttu-id="c4abb-149">Trên tab **Tổng quát** của mô tả báo giá dựa trên dự án, trong trường **Dự án**, chọn liên kết dự án.</span><span class="sxs-lookup"><span data-stu-id="c4abb-149">On the **General** tab of a project–based quote line, in the **Project** field, select the project link.</span></span>
2. <span data-ttu-id="c4abb-150">Trên trang **Dự án**, chọn tab **Thanh toán theo tác vụ**.</span><span class="sxs-lookup"><span data-stu-id="c4abb-150">On the **Project** page, select the **Task billing** tab.</span></span>
3. <span data-ttu-id="c4abb-151">Trong lưới thứ hai, áp dụng cho thiết lập thanh toán theo tác vụ cụ thể, hãy chọn một hoặc nhiều tác vụ rồi chọn **Dừng liên kết các mô tả báo giá**.</span><span class="sxs-lookup"><span data-stu-id="c4abb-151">In the second grid, which applies to task-specific billing setup, select one or more tasks, and then select **Disassociate quote lines**.</span></span>
4. <span data-ttu-id="c4abb-152">Trong trang hộp thoại xuất hiện, hãy chọn một mô tả báo giá.</span><span class="sxs-lookup"><span data-stu-id="c4abb-152">In the dialog page that appears, select a quote line.</span></span>
5. <span data-ttu-id="c4abb-153">Chọn hộp kiểm để cho biết liệu có nên loại bỏ cả liên kết khỏi các tác vụ con của tác vụ đã chọn không.</span><span class="sxs-lookup"><span data-stu-id="c4abb-153">Select the check box to indicate whether the association should also be removed from child tasks of the selected tasks.</span></span> <span data-ttu-id="c4abb-154">Việc chọn hộp cũng sẽ dừng liên kết tác vụ con của các tác vụ đã chọn với mô tả báo giá.</span><span class="sxs-lookup"><span data-stu-id="c4abb-154">Checking the box will also disassociate the child tasks of the selected tasks to the quote line.</span></span>
6. <span data-ttu-id="c4abb-155">Chọn **OK**.</span><span class="sxs-lookup"><span data-stu-id="c4abb-155">Select **OK**.</span></span> <span data-ttu-id="c4abb-156">Một cảnh báo cho bạn biết rằng nếu bạn loại bỏ liên kết này, bất kỳ giá trị thực tế nào được ghi trước đó về tác vụ có thể bị đảo ngược.</span><span class="sxs-lookup"><span data-stu-id="c4abb-156">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
7. <span data-ttu-id="c4abb-157">Chọn **OK** để tiếp tục và loại bỏ liên kết giữa tác vụ và mô tả báo giá dựa trên dự án.</span><span class="sxs-lookup"><span data-stu-id="c4abb-157">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="c4abb-158">Từ trang Mô tả báo giá</span><span class="sxs-lookup"><span data-stu-id="c4abb-158">From the Quote line page</span></span>

<span data-ttu-id="c4abb-159">Bạn cũng có thể dừng liên kết tác vụ dự án với mô tả báo giá từ tab **Tác vụ có thể tính phí** trên trang **Mô tả báo giá**.</span><span class="sxs-lookup"><span data-stu-id="c4abb-159">You can also disassociate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

1. <span data-ttu-id="c4abb-160">Trên tab **Tác vụ có thể tính phí**, chọn **Xóa tác vụ mô tả báo giá**.</span><span class="sxs-lookup"><span data-stu-id="c4abb-160">On the **Chargeable tasks** tab, select **Delete a quote line task**.</span></span>
2. <span data-ttu-id="c4abb-161">Chọn **OK**.</span><span class="sxs-lookup"><span data-stu-id="c4abb-161">Select **OK**.</span></span> <span data-ttu-id="c4abb-162">Một cảnh báo cho bạn biết rằng nếu bạn loại bỏ liên kết này, bất kỳ giá trị thực tế nào được ghi trước đó về tác vụ có thể bị đảo ngược.</span><span class="sxs-lookup"><span data-stu-id="c4abb-162">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
3. <span data-ttu-id="c4abb-163">Chọn **OK** để tiếp tục và loại bỏ liên kết giữa tác vụ và mô tả báo giá dựa trên dự án.</span><span class="sxs-lookup"><span data-stu-id="c4abb-163">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

>[!NOTE]
> <span data-ttu-id="c4abb-164">Quy trình này không xóa tác vụ khỏi dự án.</span><span class="sxs-lookup"><span data-stu-id="c4abb-164">This procedure doesn't delete the task from the project.</span></span> <span data-ttu-id="c4abb-165">Nó chỉ xóa liên kết tác vụ khỏi mô tả báo giá dựa trên dự án.</span><span class="sxs-lookup"><span data-stu-id="c4abb-165">It only removes the task association from the project-based quote line.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]