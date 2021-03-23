---
title: Tạo lịch lập hóa đơn trên phần mô tả hợp đồng dựa trên dự án - bản đơn giản
description: Chủ đề này cung cấp thông tin về cách tạo lịch và mốc lập hóa đơn.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4706a2a711efa7d176030deaa33b65bca28d8498
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273404"
---
# <a name="create-invoice-schedules-on-a-project-based-contract-line---lite"></a><span data-ttu-id="27daa-103">Tạo lịch lập hóa đơn trên phần mô tả hợp đồng dựa trên dự án - bản đơn giản</span><span class="sxs-lookup"><span data-stu-id="27daa-103">Create invoice schedules on a project-based contract line - lite</span></span>

<span data-ttu-id="27daa-104">_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="27daa-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="27daa-105">Bạn có thể đính kèm lịch lập hóa đơn trên phần mô tả hợp đồng dựa trên dự án.</span><span class="sxs-lookup"><span data-stu-id="27daa-105">You can attach an invoice schedule on a project-based contract line.</span></span> <span data-ttu-id="27daa-106">Việc lập hóa đơn chỉ được phép sau khi giành được hợp đồng để tạo Hợp đồng dự án.</span><span class="sxs-lookup"><span data-stu-id="27daa-106">Invoicing is only allowed after the contract is won to create a Project contract.</span></span> <span data-ttu-id="27daa-107">Lịch lập hóa đơn cho phép tạo tự động các hóa đơn nháp cho phần mô tả hợp đồng dựa trên dự án.</span><span class="sxs-lookup"><span data-stu-id="27daa-107">Invoice schedules allow draft invoices for a project-based contract line to be created automatically.</span></span> <span data-ttu-id="27daa-108">Nếu định sẽ luôn tạo hóa đơn theo cách thủ công, bạn có thể bỏ qua việc tạo lịch lập hóa đơn trên phần mô tả hợp đồng dựa trên dự án hoặc phần mô tả hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="27daa-108">If you plan to always create invoices manually, you can skip creating invoice schedules on a project-based contract line or a contract line.</span></span>

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-contract-line"></a><span data-ttu-id="27daa-109">Tạo lịch lập hóa đơn vật tư và thời gian cho phần mô tả hợp đồng dựa trên dự án</span><span class="sxs-lookup"><span data-stu-id="27daa-109">Create a time and material invoice schedule for a project-based contract line</span></span>

<span data-ttu-id="27daa-110">Khi mục mô tả hợp đồng dựa trên dự án có phương thức thanh toán là theo thời gian và vật tư, hệ thống sẽ tạo lịch trình hóa đơn dựa trên ngày.</span><span class="sxs-lookup"><span data-stu-id="27daa-110">When a project-based contract line has a time and material billing method, you can create a date-based invoice schedule.</span></span> <span data-ttu-id="27daa-111">Để tự động tạo lịch trình hóa đơn dựa trên ngày, hãy hoàn thành các bước sau.</span><span class="sxs-lookup"><span data-stu-id="27daa-111">To automatically generate a date-based invoice schedule, complete the following steps.</span></span>

1. <span data-ttu-id="27daa-112">Chuyển đến **Cài đặt** > **Tần suất lập hóa đơn** để thiết lập tần suất hóa đơn.</span><span class="sxs-lookup"><span data-stu-id="27daa-112">Go to **Settings** > **Invoice Frequencies** to set up invoice frequency.</span></span>
2. <span data-ttu-id="27daa-113">Mở hợp đồng dự án và trên tab **Tóm tắt**, đặt ngày giao được yêu cầu.</span><span class="sxs-lookup"><span data-stu-id="27daa-113">Open the project contract and on the **Summary** tab, set the requested delivery date.</span></span>
3. <span data-ttu-id="27daa-114">Mở phần mô tả hợp đồng vật tư và thời gian mà bạn muốn tạo lịch lập hóa đơn dựa trên ngày.</span><span class="sxs-lookup"><span data-stu-id="27daa-114">Open the time and material contract line that you want to create a date-based invoice schedule for.</span></span> 
4. <span data-ttu-id="27daa-115">Trên tab **Lịch lập hóa đơn**, chọn ngày bắt đầu thanh toán và tần suất lập hóa đơn.</span><span class="sxs-lookup"><span data-stu-id="27daa-115">On the **Invoice Schedule** tab, select a billing start date and the invoice frequency.</span></span> 
5. <span data-ttu-id="27daa-116">Trên lưới con, hãy chọn **Tạo lịch trình hóa đơn**.</span><span class="sxs-lookup"><span data-stu-id="27daa-116">On the subgrid, select **Generate Invoice Schedule**.</span></span>

    <span data-ttu-id="27daa-117">Hệ thống tạo lịch lập hóa đơn với thông tin của các trường sau:</span><span class="sxs-lookup"><span data-stu-id="27daa-117">The system generates the invoice schedule with the following field information:</span></span>

    - <span data-ttu-id="27daa-118">**Ngày chạy hóa đơn** được đặt theo ngày dựa trên tần suất lập hóa đơn.</span><span class="sxs-lookup"><span data-stu-id="27daa-118">**Invoice Run Date** is set to the date based on the invoice frequency.</span></span>
    - <span data-ttu-id="27daa-119">**Ngày dứt điểm giao dịch** được đặt thành ngày trước **Ngày chạy hóa đơn**.</span><span class="sxs-lookup"><span data-stu-id="27daa-119">**Transaction Cut-off Date** is set to the day before the **Invoice Run Date**.</span></span>
    - <span data-ttu-id="27daa-120">**Trạng thái chạy** được tự động đặt thành **Không chạy**.</span><span class="sxs-lookup"><span data-stu-id="27daa-120">**Run Status** is automatically set to **Not Run**.</span></span> <span data-ttu-id="27daa-121">Khi lệnh tự động tạo hóa đơn chạy cho một **Ngày chạy hóa đơn** nhất định, trường này sẽ được cập nhật thành **Chạy thành công** hoặc **Chạy không thành công**.</span><span class="sxs-lookup"><span data-stu-id="27daa-121">When the automatic invoice creation job runs for a certain **Invoice Run Date**, this field is updated to **Run Successful** or **Run Failed**.</span></span>

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-contract-line"></a><span data-ttu-id="27daa-122">Tạo lịch lập hóa đơn có giá cố định cho phần mô tả hợp đồng dựa trên dự án</span><span class="sxs-lookup"><span data-stu-id="27daa-122">Create a fixed price invoice schedule for a project-based contract line</span></span>

<span data-ttu-id="27daa-123">Khi phần mô tả hợp đồng dựa trên dự án có phương thức thanh toán theo giá cố định, bạn có thể tạo lịch lập hóa đơn dựa theo mốc.</span><span class="sxs-lookup"><span data-stu-id="27daa-123">When a project-based contract line has a fixed price billing method, you can create a milestone-based invoice schedule.</span></span> <span data-ttu-id="27daa-124">Hoàn tất các bước sau để tự động tạo lịch lập hóa đơn dựa theo mốc cho một nhóm mốc cố định phân bổ đều trong khoảng thời gian theo lịch.</span><span class="sxs-lookup"><span data-stu-id="27daa-124">Complete the following steps to automatically generate a milestone-based invoice schedule for a fixed set of milestones that distribute equally for the calendar period.</span></span>

1. <span data-ttu-id="27daa-125">Chuyển đến **Cài đặt** > **Tần suất lập hóa đơn** để thiết lập tần suất hóa đơn.</span><span class="sxs-lookup"><span data-stu-id="27daa-125">Go to **Settings** > **Invoice Frequencies** to set up invoice frequency.</span></span>
2. <span data-ttu-id="27daa-126">Mở hợp đồng dự án và trên tab **Tóm tắt**, đặt ngày giao được yêu cầu.</span><span class="sxs-lookup"><span data-stu-id="27daa-126">Open the project contract and on the **Summary** tab, set the requested delivery date.</span></span>
3. <span data-ttu-id="27daa-127">Mở phần mô tả hợp đồng có giá cố định mà bạn cần tạo lịch theo mốc.</span><span class="sxs-lookup"><span data-stu-id="27daa-127">Open the fixed price contract line on which you need to create a milestone schedule.</span></span> 
4. <span data-ttu-id="27daa-128">Trên tab **Lịch lập hóa đơn (Mốc thanh toán)**, chọn ngày bắt đầu thanh toán và tần suất lập hóa đơn.</span><span class="sxs-lookup"><span data-stu-id="27daa-128">On the **Invoice Schedule (Billing Milestones)** tab, select the billing start date and the invoice frequency.</span></span> 
5. <span data-ttu-id="27daa-129">Trên lưới con, hãy chọn **Tạo các mốc định kỳ**.</span><span class="sxs-lookup"><span data-stu-id="27daa-129">On the subgrid, select **Generate Periodic Milestones**.</span></span>

    <span data-ttu-id="27daa-130">Hệ thống tạo lịch lập hóa đơn với các thông tin sau đây về mốc.</span><span class="sxs-lookup"><span data-stu-id="27daa-130">The system generates the invoice schedule with the following milestone information.</span></span>

    - <span data-ttu-id="27daa-131">**Tên mốc** được đặt theo ngày dựa trên tần suất hóa đơn.</span><span class="sxs-lookup"><span data-stu-id="27daa-131">**Milestone Name** is set to the date that is dictated based on the invoice frequency.</span></span>
    - <span data-ttu-id="27daa-132">**Ngày của mốc** được đặt theo ngày dựa trên tần suất hóa đơn.</span><span class="sxs-lookup"><span data-stu-id="27daa-132">**Milestone Date** is set to the date that is dictated based on the invoice frequency.</span></span>
    - <span data-ttu-id="27daa-133">**Số tiền mốc** được tính bằng cách chia số tiền theo hợp đồng trên phần mô tả hợp đồng dựa trên dự án cho số lượng mốc theo tần suất, ngày bắt đầu thanh toán và ngày giao được yêu cầu.</span><span class="sxs-lookup"><span data-stu-id="27daa-133">**Milestone Amount** is calculated by dividing the contract amount on the project-based contract line by the number of milestones as dictated by the frequency, billing start, and requested delivery dates.</span></span>
    - <span data-ttu-id="27daa-134">Nếu phần mô tả hợp đồng có giá trị nằm trong trường **Số tiền thuế ước tính**, thì trường này cũng được chia ra thành từng mốc ngang bằng nhau khi tạo các mốc định kỳ.</span><span class="sxs-lookup"><span data-stu-id="27daa-134">If the contract line has a value in the **Estimated Tax Amount** field, this field is also apportioned to each milestone equally when generating periodic milestones.</span></span>

<span data-ttu-id="27daa-135">Các mốc thanh toán phải tương ứng với giá trị theo hợp đồng trong phần mô tả hợp đồng dựa trên dự án.</span><span class="sxs-lookup"><span data-stu-id="27daa-135">Billing milestones should equal the contracted value of the project-based contract line.</span></span> <span data-ttu-id="27daa-136">Nếu không, điều đó nghĩa là đã xảy ra lỗi.</span><span class="sxs-lookup"><span data-stu-id="27daa-136">If they aren't equal, an error occurs.</span></span> <span data-ttu-id="27daa-137">Bạn có thể sửa lỗi đó bằng cách thông qua việc tạo, chỉnh sửa hoặc xóa các mốc, xác minh rằng tổng các mốc thanh toán tương ứng với giá trị theo hợp đồng trong phần mô tả.</span><span class="sxs-lookup"><span data-stu-id="27daa-137">You can fix that error by verifying that the billing milestones total the contracted value of the line by either creating, editing, or deleting milestones.</span></span> <span data-ttu-id="27daa-138">Sau khi thực hiện xong các thay đổi, hãy làm mới trang.</span><span class="sxs-lookup"><span data-stu-id="27daa-138">After the changes are made, refresh the page.</span></span>

### <a name="manually-create-milestones"></a><span data-ttu-id="27daa-139">Tạo thủ công các mốc thời gian</span><span class="sxs-lookup"><span data-stu-id="27daa-139">Manually create milestones</span></span>

<span data-ttu-id="27daa-140">Bạn có thể tạo các mốc giá cố định theo cách thủ công khi các mốc này không được phân chia theo định kỳ.</span><span class="sxs-lookup"><span data-stu-id="27daa-140">Fixed price milestones can be generated manually when they aren't periodically split.</span></span> <span data-ttu-id="27daa-141">Để tạo mốc theo cách thủ công, hãy hoàn tất các bước sau.</span><span class="sxs-lookup"><span data-stu-id="27daa-141">To create a milestone manually, complete the following steps.</span></span>

1. <span data-ttu-id="27daa-142">Mở phần mô tả hợp đồng có giá cố định mà bạn muốn tạo mốc.</span><span class="sxs-lookup"><span data-stu-id="27daa-142">Open the fixed price contract line on which you want to create a milestone.</span></span> 
2. <span data-ttu-id="27daa-143">Ở tab **Lịch lập hóa đơn**, trên lưới con, hãy chọn **+ Tạo mốc mới trong phần Mô tả hợp đồng**.</span><span class="sxs-lookup"><span data-stu-id="27daa-143">On the **Invoice Schedule** tab, on the subgrid, select **+ Create new Contract line milestone**.</span></span>
3. <span data-ttu-id="27daa-144">Trong biểu mẫu **Tạo mốc**, nhập các thông tin bắt buộc dựa trên bảng sau.</span><span class="sxs-lookup"><span data-stu-id="27daa-144">On the **Milestone Creation** form, enter the required information based on the following table.</span></span> 

| <span data-ttu-id="27daa-145">Trường</span><span class="sxs-lookup"><span data-stu-id="27daa-145">Field</span></span> | <span data-ttu-id="27daa-146">Vị trí</span><span class="sxs-lookup"><span data-stu-id="27daa-146">Location</span></span> | <span data-ttu-id="27daa-147">Nội dung mô tả</span><span class="sxs-lookup"><span data-stu-id="27daa-147">Description</span></span> | <span data-ttu-id="27daa-148">Tác động xuôi tuyến</span><span class="sxs-lookup"><span data-stu-id="27daa-148">Downstream impact</span></span> |
| --- | --- | --- | --- |
| <span data-ttu-id="27daa-149">Tên mốc</span><span class="sxs-lookup"><span data-stu-id="27daa-149">Milestone Name</span></span> | <span data-ttu-id="27daa-150">Tạo nhanh</span><span class="sxs-lookup"><span data-stu-id="27daa-150">Quick Create</span></span> | <span data-ttu-id="27daa-151">Trường văn bản dành cho tên mốc.</span><span class="sxs-lookup"><span data-stu-id="27daa-151">Text field for the name of the milestone.</span></span> | <span data-ttu-id="27daa-152">Trường này được bao gồm trong hóa đơn và mốc của phần mô tả hợp đồng dự án.</span><span class="sxs-lookup"><span data-stu-id="27daa-152">This field is included on the project contract line milestone and the invoice.</span></span> |
| <span data-ttu-id="27daa-153">Nhiệm vụ dự án</span><span class="sxs-lookup"><span data-stu-id="27daa-153">Project Task</span></span> | <span data-ttu-id="27daa-154">Tạo nhanh</span><span class="sxs-lookup"><span data-stu-id="27daa-154">Quick Create</span></span> | <span data-ttu-id="27daa-155">Nếu mốc được liên kết với một nhiệm vụ dự án, hãy sử dụng tham chiếu này để thêm logic tùy chỉnh và đặt trạng thái mốc dựa trên trạng thái nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="27daa-155">If the milestone is tied to a project task, use this reference to add custom logic and set the milestone status based on the task status.</span></span> | <span data-ttu-id="27daa-156">Tham chiếu này không có tác động xuôi chiều đến nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="27daa-156">There is no downstream impact of this reference to a task.</span></span> |
| <span data-ttu-id="27daa-157">Ngày Mốc</span><span class="sxs-lookup"><span data-stu-id="27daa-157">Milestone Date</span></span> | <span data-ttu-id="27daa-158">Tạo nhanh</span><span class="sxs-lookup"><span data-stu-id="27daa-158">Quick Create</span></span> | <span data-ttu-id="27daa-159">Ngày mà theo đó quy trình tạo hóa đơn tự động sẽ tìm kiếm trạng thái của mốc này để xem xét lập hóa đơn.</span><span class="sxs-lookup"><span data-stu-id="27daa-159">The date on which the automatic invoice creation process should look for the status of this milestone to consider it for invoicing.</span></span> | <span data-ttu-id="27daa-160">Ngày này được bao gồm trong hóa đơn và mốc của phần mô tả hợp đồng dự án.</span><span class="sxs-lookup"><span data-stu-id="27daa-160">This is included on the project contract line milestone and the invoice.</span></span> |
| <span data-ttu-id="27daa-161">Trạng thái hóa đơn</span><span class="sxs-lookup"><span data-stu-id="27daa-161">Invoice Status</span></span> | <span data-ttu-id="27daa-162">Tạo nhanh</span><span class="sxs-lookup"><span data-stu-id="27daa-162">Quick Create</span></span> | <span data-ttu-id="27daa-163">Khi mốc được tạo, trạng thái này sẽ luôn được đặt thành **Chưa sẵn sàng lập hóa đơn** hoặc **Chưa bắt đầu**.</span><span class="sxs-lookup"><span data-stu-id="27daa-163">When the milestone is created, this status is always set to **Not ready for invoicing** or **Not started**.</span></span> | <span data-ttu-id="27daa-164">Ngày này được bao gồm trong hóa đơn và mốc của phần mô tả hợp đồng dự án.</span><span class="sxs-lookup"><span data-stu-id="27daa-164">This is included on the project contract line milestone and the invoice.</span></span> |
| <span data-ttu-id="27daa-165">Số tiền mô tả</span><span class="sxs-lookup"><span data-stu-id="27daa-165">Line Amount</span></span> | <span data-ttu-id="27daa-166">Tạo nhanh</span><span class="sxs-lookup"><span data-stu-id="27daa-166">Quick Create</span></span> | <span data-ttu-id="27daa-167">Số tiền hay giá trị của mốc mà hóa đơn cho khách hàng sẽ được lập theo đó.</span><span class="sxs-lookup"><span data-stu-id="27daa-167">The amount or value of the milestone that will be invoiced to the customer.</span></span> | <span data-ttu-id="27daa-168">Trường này được bao gồm trong hóa đơn và mốc của phần mô tả hợp đồng dự án.</span><span class="sxs-lookup"><span data-stu-id="27daa-168">This field is included on the project contract line milestone and the invoice,</span></span> |
| <span data-ttu-id="27daa-169">Thuế</span><span class="sxs-lookup"><span data-stu-id="27daa-169">Tax</span></span> | <span data-ttu-id="27daa-170">Tạo nhanh</span><span class="sxs-lookup"><span data-stu-id="27daa-170">Quick Create</span></span> | <span data-ttu-id="27daa-171">Số tiền thuế được áp cho mốc.</span><span class="sxs-lookup"><span data-stu-id="27daa-171">The tax amount applied on the milestone.</span></span> | <span data-ttu-id="27daa-172">Ngày này được bao gồm trong hóa đơn và mốc của phần mô tả hợp đồng dự án.</span><span class="sxs-lookup"><span data-stu-id="27daa-172">This is included on the project contract line milestone and the invoice.</span></span> |

4. <span data-ttu-id="27daa-173">Chọn **Lưu và Đóng**.</span><span class="sxs-lookup"><span data-stu-id="27daa-173">Select **Save and Close**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]