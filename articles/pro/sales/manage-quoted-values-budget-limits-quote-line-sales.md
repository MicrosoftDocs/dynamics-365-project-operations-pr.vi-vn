---
title: Mô tả báo giá dựa trên dự án (Dự án)
description: Chủ đề này cung cấp thông tin về việc sử dụng các mô tả báo giá dựa trên dự án cho công việc dự án. (Dự án)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a409d1e378afe97de7fb6c77cf3ad6703661bdff
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908739"
---
# <a name="project-based-quote-lines-pro"></a><span data-ttu-id="7e751-104">Mô tả báo giá dựa trên dự án (Dự án)</span><span class="sxs-lookup"><span data-stu-id="7e751-104">Project-based quote lines (Pro)</span></span>

<span data-ttu-id="7e751-105">_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="7e751-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="7e751-106">Các mô tả báo giá dựa trên dự án được thiết kế để giúp ước tính công việc dự án trên một cam kết.</span><span class="sxs-lookup"><span data-stu-id="7e751-106">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="7e751-107">Cấu trúc của mô tả báo giá dựa trên dự án được mở rộng cho các ước tính dự án với các khái niệm sau:</span><span class="sxs-lookup"><span data-stu-id="7e751-107">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="7e751-108">Phương thức Thanh toán</span><span class="sxs-lookup"><span data-stu-id="7e751-108">Billing Method</span></span>
- <span data-ttu-id="7e751-109">Ánh xạ dự án và tác vụ</span><span class="sxs-lookup"><span data-stu-id="7e751-109">Project and Task Mapping</span></span>
- <span data-ttu-id="7e751-110">Các lớp giao dịch được bao gồm</span><span class="sxs-lookup"><span data-stu-id="7e751-110">Included Transaction classes</span></span>
- <span data-ttu-id="7e751-111">Giới hạn không vượt quá</span><span class="sxs-lookup"><span data-stu-id="7e751-111">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="7e751-112">Thiết lập khả năng tính phí</span><span class="sxs-lookup"><span data-stu-id="7e751-112">Chargeability setup</span></span>
- <span data-ttu-id="7e751-113">Ước tính bằng cách sử dụng Chi tiết mô tả báo giá</span><span class="sxs-lookup"><span data-stu-id="7e751-113">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="7e751-114">Khách hàng trên mô tả báo giá</span><span class="sxs-lookup"><span data-stu-id="7e751-114">Quote line Customers</span></span>

<span data-ttu-id="7e751-115">Bảng sau cung cấp thông tin về các trường trên tab **Tổng quát** của mô tả báo giá dựa trên dự án.</span><span class="sxs-lookup"><span data-stu-id="7e751-115">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="7e751-116">Các trường này giúp thiết lập cơ sở để ước tính chi tiết, nền tảng cho công việc dự án.</span><span class="sxs-lookup"><span data-stu-id="7e751-116">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="7e751-117">**Trường**</span><span class="sxs-lookup"><span data-stu-id="7e751-117">**Field**</span></span> | <span data-ttu-id="7e751-118">**Mức độ liên quan, mục đích và hướng dẫn**</span><span class="sxs-lookup"><span data-stu-id="7e751-118">**Relevance, purpose, and guidance**</span></span> | <span data-ttu-id="7e751-119">**Tác động xuôi tuyến**</span><span class="sxs-lookup"><span data-stu-id="7e751-119">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="7e751-120">Tên</span><span class="sxs-lookup"><span data-stu-id="7e751-120">Name</span></span> | <span data-ttu-id="7e751-121">Tên của mô tả báo giá sẽ giúp bạn xác định thành phần riêng biệt của báo giá đang được ước tính.</span><span class="sxs-lookup"><span data-stu-id="7e751-121">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="7e751-122">Được sao chép vào mô tả hợp đồng dự án tạo từ mô tả báo giá này khi báo giá được chốt.</span><span class="sxs-lookup"><span data-stu-id="7e751-122">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="7e751-123">Phương thức Thanh toán</span><span class="sxs-lookup"><span data-stu-id="7e751-123">Billing Method</span></span> | <span data-ttu-id="7e751-124">Trên một báo giá tạo từ một cơ hội, giá trị này được sao chép từ trường tương ứng trên mô tả cơ hội.</span><span class="sxs-lookup"><span data-stu-id="7e751-124">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="7e751-125">Trường này bao gồm hai mô hình hợp đồng chính được hỗ trợ bởi Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="7e751-125">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="7e751-126">- Giá cố định</span><span class="sxs-lookup"><span data-stu-id="7e751-126">- Fixed price</span></span></br><span data-ttu-id="7e751-127">- Thời gian và vật tư.</span><span class="sxs-lookup"><span data-stu-id="7e751-127">- Time and material.</span></span>| <span data-ttu-id="7e751-128">Giá trị trường này được sao chép vào mô tả hợp đồng dự án tạo từ mô tả báo giá này khi báo giá được chốt.</span><span class="sxs-lookup"><span data-stu-id="7e751-128">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="7e751-129">Dự án</span><span class="sxs-lookup"><span data-stu-id="7e751-129">Project</span></span> | <span data-ttu-id="7e751-130">Sử dụng trường tùy chọn này để xác định dự án sẽ được sử dụng để thực hiện công việc trong cam kết này.</span><span class="sxs-lookup"><span data-stu-id="7e751-130">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="7e751-131">Khi một dự án được ánh xạ đến một mô tả báo giá, nó sẽ giúp thiết lập các tác vụ có thể tính phí, đồng thời đưa ước tính dựa trên dự án vào mô tả báo giá dưới dạng chi tiết mô tả báo giá.</span><span class="sxs-lookup"><span data-stu-id="7e751-131">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="7e751-132">Khi một dự án không được ánh xạ tới mô tả báo giá dựa trên dự án, ước tính sẽ được tạo theo cách thủ công bằng cách tạo chi tiết từng mô tả báo giá.</span><span class="sxs-lookup"><span data-stu-id="7e751-132">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="7e751-133">Giá trị trường này được sao chép vào mô tả hợp đồng dự án tạo từ mô tả báo giá này khi báo giá được chốt.</span><span class="sxs-lookup"><span data-stu-id="7e751-133">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="7e751-134">Các tác vụ được đưa vào</span><span class="sxs-lookup"><span data-stu-id="7e751-134">Included Tasks</span></span> | <span data-ttu-id="7e751-135">Cho biết mô tả báo giá này được sử dụng cho tất cả hoặc một số tác vụ dự án cho dự án đã chọn.</span><span class="sxs-lookup"><span data-stu-id="7e751-135">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="7e751-136">Trường này có các giá trị khả dĩ sau đây:</span><span class="sxs-lookup"><span data-stu-id="7e751-136">This field has the following possible values:</span></span></br><span data-ttu-id="7e751-137">- Tất cả tác vụ dự án</span><span class="sxs-lookup"><span data-stu-id="7e751-137">- All project tasks</span></span></br><span data-ttu-id="7e751-138">- Chỉ các tác vụ dự án đã chọn</span><span class="sxs-lookup"><span data-stu-id="7e751-138">- Selected project tasks only</span></span></br><span data-ttu-id="7e751-139">Giá trị trống trong trường này tương đương với tùy chọn **Tất cả tác vụ dự án**.</span><span class="sxs-lookup"><span data-stu-id="7e751-139">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="7e751-140">Khi **Chỉ các tác vụ dự án được chọn** được chọn, trên trang dự án, tab **Thiết lập thanh toán theo tác vụ** cho phép bạn chọn một số tác vụ cụ thể để liên kết chúng với mô tả báo giá này.</span><span class="sxs-lookup"><span data-stu-id="7e751-140">When **Selected project tasks only** is selected then on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="7e751-141">Giá trị trường này được sao chép vào mô tả hợp đồng dự án tạo từ mô tả báo giá này khi báo giá được chốt.</span><span class="sxs-lookup"><span data-stu-id="7e751-141">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="7e751-142">Bao gồm Thời gian</span><span class="sxs-lookup"><span data-stu-id="7e751-142">Include Time</span></span> | <span data-ttu-id="7e751-143">Cờ **Có**/**Không** cho biết nếu các giao dịch thời gian hoặc chi phí nhân công trên dự án đã chọn sẽ được bao gồm trong ước tính trên mô tả báo giá này.</span><span class="sxs-lookup"><span data-stu-id="7e751-143">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="7e751-144">Giá trị **Không** cho biết rằng giao dịch thời gian hoặc chi phí nhân công sẽ không được bao gồm trong ước tính trên mô tả báo giá này.</span><span class="sxs-lookup"><span data-stu-id="7e751-144">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="7e751-145">Giá trị **Có** cho biết rằng giao dịch thời gian hoặc chi phí nhân công sẽ được bao gồm trong ước tính trên mô tả báo giá này.</span><span class="sxs-lookup"><span data-stu-id="7e751-145">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="7e751-146">Giá trị trường này được sao chép vào mô tả hợp đồng dự án tạo từ mô tả báo giá này khi báo giá được chốt.</span><span class="sxs-lookup"><span data-stu-id="7e751-146">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="7e751-147">Bao gồm Chi phí</span><span class="sxs-lookup"><span data-stu-id="7e751-147">Include Expense</span></span> | <span data-ttu-id="7e751-148">Cờ **Có**/**Không** cho biết nếu chi phí phí tổn trên dự án đã chọn sẽ được bao gồm trong ước tính trên mô tả báo giá này.</span><span class="sxs-lookup"><span data-stu-id="7e751-148">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="7e751-149">Giá trị **Không** cho biết rằng chi phí phí tổn sẽ không được bao gồm trong ước tính trên mô tả báo giá này.</span><span class="sxs-lookup"><span data-stu-id="7e751-149">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="7e751-150">Giá trị **Có** cho biết rằng chi phí phí tổn sẽ được bao gồm trong ước tính trên mô tả báo giá này.</span><span class="sxs-lookup"><span data-stu-id="7e751-150">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="7e751-151">Giá trị trường này được sao chép vào mô tả hợp đồng dự án tạo từ mô tả báo giá này khi báo giá được chốt.</span><span class="sxs-lookup"><span data-stu-id="7e751-151">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="7e751-152">Bao gồm Phí</span><span class="sxs-lookup"><span data-stu-id="7e751-152">Include Fee</span></span> | <span data-ttu-id="7e751-153">Cờ **Có**/**Không** cho biết nếu các khoản phí trên dự án đã chọn sẽ được bao gồm trong ước tính trên mô tả báo giá này.</span><span class="sxs-lookup"><span data-stu-id="7e751-153">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="7e751-154">Giá trị **Không** cho biết rằng các khoản phí sẽ không được bao gồm trong ước tính trên mô tả báo giá này.</span><span class="sxs-lookup"><span data-stu-id="7e751-154">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="7e751-155">Giá trị **Có** cho biết rằng các khoản phí sẽ được bao gồm trong ước tính trên mô tả báo giá này.</span><span class="sxs-lookup"><span data-stu-id="7e751-155">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="7e751-156">Giá trị trường này được sao chép vào Mô tả hợp đồng dự án tạo từ mô tả báo giá này khi báo giá được chốt.</span><span class="sxs-lookup"><span data-stu-id="7e751-156">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="7e751-157">Số tiền Đã báo giá</span><span class="sxs-lookup"><span data-stu-id="7e751-157">Quoted Amount</span></span> | <span data-ttu-id="7e751-158">Đây là số tiền sẽ được báo giá cho khách hàng đối với tất cả các công việc được dự báo trên mô tả báo giá dựa trên dự án này.</span><span class="sxs-lookup"><span data-stu-id="7e751-158">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="7e751-159">Trên một báo giá tạo từ một cơ hội, giá trị này được sao chép từ trường **Ngân sách khách hàng** trên mô tả cơ hội.</span><span class="sxs-lookup"><span data-stu-id="7e751-159">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="7e751-160">Khi mô tả báo giá dựa trên dự án có chi tiết mô tả, trường này bị khóa tính năng chỉnh sửa và được tóm tắt từ số tiền trên chi tiết mô tả báo giá.</span><span class="sxs-lookup"><span data-stu-id="7e751-160">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="7e751-161">Giá trị trường này được sao chép vào mô tả hợp đồng dự án tạo từ mô tả báo giá này khi báo giá được chốt.</span><span class="sxs-lookup"><span data-stu-id="7e751-161">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="7e751-162">Thuế Ước tính</span><span class="sxs-lookup"><span data-stu-id="7e751-162">Estimated Tax</span></span> | <span data-ttu-id="7e751-163">Đây là trường có thể chỉnh sửa để người dùng thêm số tiền thuế ước tính trên mô tả báo giá.</span><span class="sxs-lookup"><span data-stu-id="7e751-163">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="7e751-164">Khi mô tả báo giá dựa trên dự án có chi tiết mô tả, trường này bị khóa tính năng chỉnh sửa và được tóm tắt từ số tiền thuế trên chi tiết mô tả báo giá.</span><span class="sxs-lookup"><span data-stu-id="7e751-164">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="7e751-165">Giá trị trường này được sao chép vào mô tả hợp đồng dự án tạo từ mô tả báo giá này khi báo giá được chốt.</span><span class="sxs-lookup"><span data-stu-id="7e751-165">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="7e751-166">Số tiền đã báo giá sau thuế</span><span class="sxs-lookup"><span data-stu-id="7e751-166">Quoted Amount after Tax</span></span> | <span data-ttu-id="7e751-167">Trường này là số tiền mô tả báo giá sau thuế và ở dạng chỉ đọc.</span><span class="sxs-lookup"><span data-stu-id="7e751-167">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="7e751-168">Số tiền trong trường này được tính là *Số tiền báo giá + Thuế*.</span><span class="sxs-lookup"><span data-stu-id="7e751-168">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="7e751-169">Giá trị trường này được sao chép vào mô tả hợp đồng dự án tạo từ mô tả báo giá này khi báo giá được chốt.</span><span class="sxs-lookup"><span data-stu-id="7e751-169">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="7e751-170">Giới hạn không vượt quá</span><span class="sxs-lookup"><span data-stu-id="7e751-170">Not-to-exceed Limit</span></span> | <span data-ttu-id="7e751-171">Trường này có thể chỉnh sửa và chỉ có sẵn trên các mô tả báo giá dựa trên dự án có phương thức thanh toán **Thời gian và vật tư**.</span><span class="sxs-lookup"><span data-stu-id="7e751-171">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="7e751-172">Giá trị trường này được sao chép vào mô tả hợp đồng dự án tạo từ mô tả báo giá này khi báo giá được chốt.</span><span class="sxs-lookup"><span data-stu-id="7e751-172">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="7e751-173">Ngân sách Khách hàng</span><span class="sxs-lookup"><span data-stu-id="7e751-173">Customer Budget</span></span> | <span data-ttu-id="7e751-174">Trường này có thể chỉnh sửa và được sao chép từ trường tương ứng trên mô tả cơ hội nếu báo giá được tạo từ một cơ hội.</span><span class="sxs-lookup"><span data-stu-id="7e751-174">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="7e751-175">Giá trị trường này được sao chép vào mô tả hợp đồng dự án tạo từ mô tả báo giá này khi báo giá được chốt.</span><span class="sxs-lookup"><span data-stu-id="7e751-175">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="7e751-176">Quy tắc xác thực cho các trường trên tab Tổng quát của các mô tả báo giá dựa trên dự án</span><span class="sxs-lookup"><span data-stu-id="7e751-176">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="7e751-177">**Quy tắc 1**: Nếu trường **Các tác vụ được đưa vào** bị trống hoặc nếu nó được đặt thành **Tất cả các tác vụ dự án**, một dự án sẽ được bao gồm trong mô tả báo giá.</span><span class="sxs-lookup"><span data-stu-id="7e751-177">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="7e751-178">**Quy tắc 2**: Nếu trường **Các tác vụ được đưa vào** bị trống hoặc nếu nó được đặt thành **Tất cả các tác vụ dự án**, một dự án và một lớp giao dịch nhất định chỉ có thể được đưa vào một mô tả báo giá dựa trên dự án của báo giá.</span><span class="sxs-lookup"><span data-stu-id="7e751-178">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="7e751-179">**Quy tắc 3**: Nếu trường **Các tác vụ được đưa vào** được đặt thành **Chỉ các tác vụ dự án đã chọn**, một dự án và một lớp giao dịch nhất định có thể được đưa vào nhiều mô tả báo giá dựa trên dự án của báo giá.</span><span class="sxs-lookup"><span data-stu-id="7e751-179">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="7e751-180">**Quy tắc 4**: Nếu một cơ hội có nhiều báo giá, có thể có các mô tả báo giá từ các báo giá khác nhau mà đều tham chiếu đến cùng một dự án và bao gồm cùng một lớp giao dịch.</span><span class="sxs-lookup"><span data-stu-id="7e751-180">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="7e751-181">**Quy tắc 5** : Nếu các báo giá không thuộc cùng một cơ hội, chúng không thể bao gồm cùng một dự án và lớp giao dịch.</span><span class="sxs-lookup"><span data-stu-id="7e751-181">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="7e751-182">
                    <strong>Cơ hội</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e751-182">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="7e751-183">
                    <strong>Báo giá</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e751-183">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="7e751-184">
                    <strong>Mô tả báo giá</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e751-184">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="7e751-185">
                    <strong>Dự án</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e751-185">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="90" valign="top">
                <p><span data-ttu-id="7e751-186">
                    <strong>Các tác vụ được đưa vào</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e751-186">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="7e751-187">
                    <strong>Bao gồm Thời gian</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e751-187">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="7e751-188">
                    <strong>Bao gồm Chi phí</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e751-188">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="7e751-189">
                    <strong>Bao gồm</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e751-189">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="7e751-190">
                    <strong>Phí</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e751-190">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="7e751-191">
                    <strong>Hợp lệ/Không hợp lệ</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e751-191">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="7e751-192">
                    <strong>Lý do</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7e751-192">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="7e751-193">O1</span><span class="sxs-lookup"><span data-stu-id="7e751-193">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="7e751-194">Q1</span><span class="sxs-lookup"><span data-stu-id="7e751-194">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="7e751-195">QL1</span><span class="sxs-lookup"><span data-stu-id="7e751-195">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="7e751-196">Kỳ 1</span><span class="sxs-lookup"><span data-stu-id="7e751-196">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="7e751-197">Trống</span><span class="sxs-lookup"><span data-stu-id="7e751-197">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="7e751-198">Có</span><span class="sxs-lookup"><span data-stu-id="7e751-198">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="7e751-199">Có</span><span class="sxs-lookup"><span data-stu-id="7e751-199">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="7e751-200">Có</span><span class="sxs-lookup"><span data-stu-id="7e751-200">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7e751-201">Không hợp lệ</span><span class="sxs-lookup"><span data-stu-id="7e751-201">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7e751-202">Vi phạm Quy tắc số 2.</span><span class="sxs-lookup"><span data-stu-id="7e751-202">Violation of Rule #2.</span></span> <span data-ttu-id="7e751-203">Thời gian, Chi phí và Phí cho dự án P1 được bao gồm trên các mô tả báo giá QL1 và QL2.</span><span class="sxs-lookup"><span data-stu-id="7e751-203">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="7e751-204">O1</span><span class="sxs-lookup"><span data-stu-id="7e751-204">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="7e751-205">Q1</span><span class="sxs-lookup"><span data-stu-id="7e751-205">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="7e751-206">QL2</span><span class="sxs-lookup"><span data-stu-id="7e751-206">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="7e751-207">Kỳ 1</span><span class="sxs-lookup"><span data-stu-id="7e751-207">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="7e751-208">Trống</span><span class="sxs-lookup"><span data-stu-id="7e751-208">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="7e751-209">Có</span><span class="sxs-lookup"><span data-stu-id="7e751-209">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="7e751-210">Có</span><span class="sxs-lookup"><span data-stu-id="7e751-210">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="7e751-211">Có</span><span class="sxs-lookup"><span data-stu-id="7e751-211">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="7e751-212">O1</span><span class="sxs-lookup"><span data-stu-id="7e751-212">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="7e751-213">Q1</span><span class="sxs-lookup"><span data-stu-id="7e751-213">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="7e751-214">QL1</span><span class="sxs-lookup"><span data-stu-id="7e751-214">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="7e751-215">Kỳ 1</span><span class="sxs-lookup"><span data-stu-id="7e751-215">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="7e751-216">Trống</span><span class="sxs-lookup"><span data-stu-id="7e751-216">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="7e751-217">Có</span><span class="sxs-lookup"><span data-stu-id="7e751-217">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="7e751-218">No</span><span class="sxs-lookup"><span data-stu-id="7e751-218">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="7e751-219">Có</span><span class="sxs-lookup"><span data-stu-id="7e751-219">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7e751-220">Không hợp lệ</span><span class="sxs-lookup"><span data-stu-id="7e751-220">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7e751-221">Vi phạm Quy tắc số 2.</span><span class="sxs-lookup"><span data-stu-id="7e751-221">Violation of Rule #2.</span></span> <span data-ttu-id="7e751-222">Thời gian và Phí cho dự án P1 được bao gồm trên các mô tả báo giá QL1 và QL2.</span><span class="sxs-lookup"><span data-stu-id="7e751-222">Time and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="7e751-223">O1</span><span class="sxs-lookup"><span data-stu-id="7e751-223">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="7e751-224">Q1</span><span class="sxs-lookup"><span data-stu-id="7e751-224">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="7e751-225">QL2</span><span class="sxs-lookup"><span data-stu-id="7e751-225">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="7e751-226">Kỳ 1</span><span class="sxs-lookup"><span data-stu-id="7e751-226">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="7e751-227">Trống</span><span class="sxs-lookup"><span data-stu-id="7e751-227">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="7e751-228">Có</span><span class="sxs-lookup"><span data-stu-id="7e751-228">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="7e751-229">Có</span><span class="sxs-lookup"><span data-stu-id="7e751-229">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="7e751-230">Có</span><span class="sxs-lookup"><span data-stu-id="7e751-230">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="7e751-231">O1</span><span class="sxs-lookup"><span data-stu-id="7e751-231">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="7e751-232">Q1</span><span class="sxs-lookup"><span data-stu-id="7e751-232">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="7e751-233">QL1</span><span class="sxs-lookup"><span data-stu-id="7e751-233">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="7e751-234">Kỳ 1</span><span class="sxs-lookup"><span data-stu-id="7e751-234">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="7e751-235">Trống</span><span class="sxs-lookup"><span data-stu-id="7e751-235">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="7e751-236">Có</span><span class="sxs-lookup"><span data-stu-id="7e751-236">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="7e751-237">No</span><span class="sxs-lookup"><span data-stu-id="7e751-237">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="7e751-238">Có</span><span class="sxs-lookup"><span data-stu-id="7e751-238">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7e751-239">Hợp lệ</span><span class="sxs-lookup"><span data-stu-id="7e751-239">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
<span data-ttu-id="7e751-240">Thời gian và Phí của dự án P1 được bao gồm trên QL1.</span><span class="sxs-lookup"><span data-stu-id="7e751-240">Time and Fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="7e751-241">Chi phí trên dự án P1 được bao gồm trên QL2.</span><span class="sxs-lookup"><span data-stu-id="7e751-241">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="7e751-242">Không có sự chồng chéo về những gì được bao gồm trên mỗi mô tả báo giá và hợp lệ.</span><span class="sxs-lookup"><span data-stu-id="7e751-242">There is no overlap in what is being included on each quote line and is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="7e751-243">O1</span><span class="sxs-lookup"><span data-stu-id="7e751-243">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="7e751-244">Q1</span><span class="sxs-lookup"><span data-stu-id="7e751-244">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="7e751-245">QL2</span><span class="sxs-lookup"><span data-stu-id="7e751-245">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="7e751-246">Kỳ 1</span><span class="sxs-lookup"><span data-stu-id="7e751-246">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="7e751-247">Trống</span><span class="sxs-lookup"><span data-stu-id="7e751-247">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="7e751-248">No</span><span class="sxs-lookup"><span data-stu-id="7e751-248">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="7e751-249">Có</span><span class="sxs-lookup"><span data-stu-id="7e751-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="7e751-250">No</span><span class="sxs-lookup"><span data-stu-id="7e751-250">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="7e751-251">O1</span><span class="sxs-lookup"><span data-stu-id="7e751-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="7e751-252">Q1</span><span class="sxs-lookup"><span data-stu-id="7e751-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="7e751-253">QL1</span><span class="sxs-lookup"><span data-stu-id="7e751-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="7e751-254">Kỳ 1</span><span class="sxs-lookup"><span data-stu-id="7e751-254">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="7e751-255">Chỉ các tác vụ được chọn</span><span class="sxs-lookup"><span data-stu-id="7e751-255">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="7e751-256">Có</span><span class="sxs-lookup"><span data-stu-id="7e751-256">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="7e751-257">Có</span><span class="sxs-lookup"><span data-stu-id="7e751-257">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="7e751-258">Có</span><span class="sxs-lookup"><span data-stu-id="7e751-258">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7e751-259">Không hợp lệ</span><span class="sxs-lookup"><span data-stu-id="7e751-259">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7e751-260">Vi phạm Quy tắc số 2 ở trên</span><span class="sxs-lookup"><span data-stu-id="7e751-260">Violation of Rule #2 above</span></span> </p>
                <p>
<span data-ttu-id="7e751-261">Q1 bao gồm Thời gian, Chi phí và Phí cho một tập hợp con các nhiệm vụ trong dự án P1.</span><span class="sxs-lookup"><span data-stu-id="7e751-261">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="7e751-262">QL2 bao gồm Thời gian, Chi phí và Phí cho toàn bộ dự án P1 và chồng chéo với những gì được bao gồm trong Q1.</span><span class="sxs-lookup"><span data-stu-id="7e751-262">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="7e751-263">O1</span><span class="sxs-lookup"><span data-stu-id="7e751-263">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="7e751-264">Q1</span><span class="sxs-lookup"><span data-stu-id="7e751-264">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="7e751-265">QL2</span><span class="sxs-lookup"><span data-stu-id="7e751-265">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="7e751-266">Kỳ 1</span><span class="sxs-lookup"><span data-stu-id="7e751-266">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="7e751-267">Trống</span><span class="sxs-lookup"><span data-stu-id="7e751-267">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="7e751-268">Có</span><span class="sxs-lookup"><span data-stu-id="7e751-268">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="7e751-269">Có</span><span class="sxs-lookup"><span data-stu-id="7e751-269">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="7e751-270">Có</span><span class="sxs-lookup"><span data-stu-id="7e751-270">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="7e751-271">O1</span><span class="sxs-lookup"><span data-stu-id="7e751-271">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="7e751-272">Q1</span><span class="sxs-lookup"><span data-stu-id="7e751-272">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="7e751-273">QL1</span><span class="sxs-lookup"><span data-stu-id="7e751-273">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="7e751-274">Kỳ 1</span><span class="sxs-lookup"><span data-stu-id="7e751-274">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="7e751-275">Chỉ các tác vụ được chọn</span><span class="sxs-lookup"><span data-stu-id="7e751-275">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="7e751-276">Có</span><span class="sxs-lookup"><span data-stu-id="7e751-276">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="7e751-277">Có</span><span class="sxs-lookup"><span data-stu-id="7e751-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="7e751-278">Có</span><span class="sxs-lookup"><span data-stu-id="7e751-278">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7e751-279">Hợp lệ</span><span class="sxs-lookup"><span data-stu-id="7e751-279">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7e751-280">Theo Quy tắc số 3 ở trên,</span><span class="sxs-lookup"><span data-stu-id="7e751-280">Per Rule #3 above,</span></span> </p>
                <p>
<span data-ttu-id="7e751-281">Q1 bao gồm Thời gian, Chi phí và Phí cho một tập hợp con các nhiệm vụ trong dự án P1.</span><span class="sxs-lookup"><span data-stu-id="7e751-281">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="7e751-282">QL2 bao gồm Thời gian, Chi phí và Phí cho một tập hợp con các nhiệm vụ trong dự án P1.</span><span class="sxs-lookup"><span data-stu-id="7e751-282">QL2 includes Time, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="7e751-283">Xác thực bổ sung duy nhất xoay quan tập hợp con gồm các nhiệm vụ trên QL1, khác với tập hợp con các nhiệm vụ trên QL2.</span><span class="sxs-lookup"><span data-stu-id="7e751-283">The only additional validation is around the subset of tasks on QL1 which are different from the subset of tasks on QL2.</span></span> <span data-ttu-id="7e751-284">Điều này đảm bảo rằng không có sự chồng chéo.</span><span class="sxs-lookup"><span data-stu-id="7e751-284">This ensures that there are no overlaps.</span></span> <span data-ttu-id="7e751-285">Điều này được hệ thống thực hiện khi các nhiệm vụ được liên kết.</span><span class="sxs-lookup"><span data-stu-id="7e751-285">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="7e751-286">O1</span><span class="sxs-lookup"><span data-stu-id="7e751-286">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="7e751-287">Q1</span><span class="sxs-lookup"><span data-stu-id="7e751-287">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="7e751-288">QL2</span><span class="sxs-lookup"><span data-stu-id="7e751-288">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="7e751-289">Kỳ 1</span><span class="sxs-lookup"><span data-stu-id="7e751-289">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="7e751-290">Chỉ các tác vụ được chọn</span><span class="sxs-lookup"><span data-stu-id="7e751-290">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="7e751-291">Có</span><span class="sxs-lookup"><span data-stu-id="7e751-291">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="7e751-292">Có</span><span class="sxs-lookup"><span data-stu-id="7e751-292">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="7e751-293">Có</span><span class="sxs-lookup"><span data-stu-id="7e751-293">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="7e751-294">O1</span><span class="sxs-lookup"><span data-stu-id="7e751-294">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="7e751-295">Q1</span><span class="sxs-lookup"><span data-stu-id="7e751-295">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="7e751-296">QL1</span><span class="sxs-lookup"><span data-stu-id="7e751-296">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="7e751-297">Kỳ 1</span><span class="sxs-lookup"><span data-stu-id="7e751-297">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="7e751-298">Tất cả các tác vụ dự án hoặc để trống</span><span class="sxs-lookup"><span data-stu-id="7e751-298">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="7e751-299">Có</span><span class="sxs-lookup"><span data-stu-id="7e751-299">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="7e751-300">Có</span><span class="sxs-lookup"><span data-stu-id="7e751-300">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="7e751-301">Có</span><span class="sxs-lookup"><span data-stu-id="7e751-301">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="7e751-302">Hợp lệ</span><span class="sxs-lookup"><span data-stu-id="7e751-302">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7e751-303">Dựa trên Quy tắc số 5, Q1 và Q2 là hai báo giá về cùng một cơ hội, vì vậy cả hai đều có thể ước tính cho các thành phần giống nhau của dự án.</span><span class="sxs-lookup"><span data-stu-id="7e751-303">Based on Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="7e751-304">O1</span><span class="sxs-lookup"><span data-stu-id="7e751-304">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="7e751-305">Q2</span><span class="sxs-lookup"><span data-stu-id="7e751-305">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="7e751-306">QL1</span><span class="sxs-lookup"><span data-stu-id="7e751-306">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="7e751-307">Kỳ 1</span><span class="sxs-lookup"><span data-stu-id="7e751-307">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="7e751-308">Tất cả các tác vụ dự án hoặc để trống</span><span class="sxs-lookup"><span data-stu-id="7e751-308">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="7e751-309">Có</span><span class="sxs-lookup"><span data-stu-id="7e751-309">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="7e751-310">Có</span><span class="sxs-lookup"><span data-stu-id="7e751-310">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="7e751-311">Có</span><span class="sxs-lookup"><span data-stu-id="7e751-311">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="7e751-312">O1</span><span class="sxs-lookup"><span data-stu-id="7e751-312">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="7e751-313">Q1</span><span class="sxs-lookup"><span data-stu-id="7e751-313">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="7e751-314">QL1</span><span class="sxs-lookup"><span data-stu-id="7e751-314">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="7e751-315">Kỳ 1</span><span class="sxs-lookup"><span data-stu-id="7e751-315">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="7e751-316">Tất cả các tác vụ dự án hoặc để trống</span><span class="sxs-lookup"><span data-stu-id="7e751-316">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="7e751-317">Có</span><span class="sxs-lookup"><span data-stu-id="7e751-317">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="7e751-318">Có</span><span class="sxs-lookup"><span data-stu-id="7e751-318">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="7e751-319">Có</span><span class="sxs-lookup"><span data-stu-id="7e751-319">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="7e751-320">Hợp lệ</span><span class="sxs-lookup"><span data-stu-id="7e751-320">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7e751-321">Dựa trên Quy tắc số 4, Q1 và Q2 là hai báo giá về các cơ hội khác nhau, vì vậy cả hai không thể ước tính cho các thành phần giống nhau của cùng dự án.</span><span class="sxs-lookup"><span data-stu-id="7e751-321">Based on Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="7e751-322">O2</span><span class="sxs-lookup"><span data-stu-id="7e751-322">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="7e751-323">Q1</span><span class="sxs-lookup"><span data-stu-id="7e751-323">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="7e751-324">QL1</span><span class="sxs-lookup"><span data-stu-id="7e751-324">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="7e751-325">Kỳ 1</span><span class="sxs-lookup"><span data-stu-id="7e751-325">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="7e751-326">Tất cả các tác vụ dự án hoặc để trống</span><span class="sxs-lookup"><span data-stu-id="7e751-326">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="7e751-327">Có</span><span class="sxs-lookup"><span data-stu-id="7e751-327">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="7e751-328">Có</span><span class="sxs-lookup"><span data-stu-id="7e751-328">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="7e751-329">Có</span><span class="sxs-lookup"><span data-stu-id="7e751-329">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="7e751-330">Không hợp lệ</span><span class="sxs-lookup"><span data-stu-id="7e751-330">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

