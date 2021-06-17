---
title: Tổng quan về các mô tả báo giá dựa trên dự án
description: Chủ đề này cung cấp thông tin về việc sử dụng các mô tả báo giá dựa trên dự án cho công việc dự án.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 32337b05f09ef7c5b84fdff9870744d6367e2693
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994882"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="4018d-103">Tổng quan về mô tả báo giá dựa trên dự án</span><span class="sxs-lookup"><span data-stu-id="4018d-103">Project-based quote lines overview</span></span> 

<span data-ttu-id="4018d-104">_**Áp dụng cho:** Triển khai bản đơn giản - từ thỏa thuận đến lập hóa đơn ước giá, Project Operations cho các kịch bản dựa trên tài nguyên/không lưu kho_</span><span class="sxs-lookup"><span data-stu-id="4018d-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="4018d-105">Các mô tả báo giá dựa trên dự án được thiết kế để giúp ước tính công việc dự án trên một cam kết.</span><span class="sxs-lookup"><span data-stu-id="4018d-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="4018d-106">Cấu trúc của mô tả báo giá dựa trên dự án được mở rộng cho các ước tính dự án với các khái niệm sau:</span><span class="sxs-lookup"><span data-stu-id="4018d-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="4018d-107">Phương thức Thanh toán</span><span class="sxs-lookup"><span data-stu-id="4018d-107">Billing Method</span></span>
- <span data-ttu-id="4018d-108">Ánh xạ dự án và tác vụ</span><span class="sxs-lookup"><span data-stu-id="4018d-108">Project and Task Mapping</span></span>
- <span data-ttu-id="4018d-109">Các lớp giao dịch được bao gồm</span><span class="sxs-lookup"><span data-stu-id="4018d-109">Included Transaction classes</span></span>
- <span data-ttu-id="4018d-110">Giới hạn không vượt quá</span><span class="sxs-lookup"><span data-stu-id="4018d-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="4018d-111">Thiết lập khả năng tính phí</span><span class="sxs-lookup"><span data-stu-id="4018d-111">Chargeability setup</span></span>
- <span data-ttu-id="4018d-112">Ước tính bằng cách sử dụng Chi tiết mô tả báo giá</span><span class="sxs-lookup"><span data-stu-id="4018d-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="4018d-113">Khách hàng trên mô tả báo giá</span><span class="sxs-lookup"><span data-stu-id="4018d-113">Quote line Customers</span></span>

<span data-ttu-id="4018d-114">Bảng sau cung cấp thông tin về các trường trên tab **Tổng quát** của mô tả báo giá dựa trên dự án.</span><span class="sxs-lookup"><span data-stu-id="4018d-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="4018d-115">Các trường này giúp thiết lập cơ sở để ước tính chi tiết, nền tảng cho công việc dự án.</span><span class="sxs-lookup"><span data-stu-id="4018d-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="4018d-116">**Trường**</span><span class="sxs-lookup"><span data-stu-id="4018d-116">**Field**</span></span> | <span data-ttu-id="4018d-117">**Mô tả**</span><span class="sxs-lookup"><span data-stu-id="4018d-117">**Description**</span></span> | <span data-ttu-id="4018d-118">**Tác động xuôi tuyến**</span><span class="sxs-lookup"><span data-stu-id="4018d-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="4018d-119">Tên</span><span class="sxs-lookup"><span data-stu-id="4018d-119">Name</span></span> | <span data-ttu-id="4018d-120">Tên của mục mô tả báo giá giúp bạn xác định thành thành phần riêng rẽ của báo giá đang được ước tính.</span><span class="sxs-lookup"><span data-stu-id="4018d-120">The name of quote line that helps you to identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="4018d-121">Được sao chép vào mô tả hợp đồng dự án tạo từ mô tả báo giá này khi báo giá được chốt.</span><span class="sxs-lookup"><span data-stu-id="4018d-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="4018d-122">Phương thức Thanh toán</span><span class="sxs-lookup"><span data-stu-id="4018d-122">Billing Method</span></span> | <span data-ttu-id="4018d-123">Trên một báo giá tạo từ một cơ hội, giá trị này được sao chép từ trường tương ứng trên mô tả cơ hội.</span><span class="sxs-lookup"><span data-stu-id="4018d-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="4018d-124">Trường này bao gồm 2 mô hình hợp đồng được hỗ trợ bởi Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="4018d-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="4018d-125">- Giá cố định</span><span class="sxs-lookup"><span data-stu-id="4018d-125">- Fixed price</span></span></br><span data-ttu-id="4018d-126">- Thời gian và vật tư.</span><span class="sxs-lookup"><span data-stu-id="4018d-126">- Time and material.</span></span>| <span data-ttu-id="4018d-127">Giá trị này được sao chép vào mục mô tả hợp đồng dự án được tạo từ mục mô tả báo giá này khi có được báo giá.</span><span class="sxs-lookup"><span data-stu-id="4018d-127">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="4018d-128">Dự án</span><span class="sxs-lookup"><span data-stu-id="4018d-128">Project</span></span> | <span data-ttu-id="4018d-129">Sử dụng trường tùy chọn này để xác định dự án sẽ được sử dụng để thực hiện công việc trong cam kết này.</span><span class="sxs-lookup"><span data-stu-id="4018d-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="4018d-130">Khi một dự án được ánh xạ đến một mô tả báo giá, nó sẽ giúp thiết lập các tác vụ có thể tính phí, đồng thời đưa ước tính dựa trên dự án vào mô tả báo giá dưới dạng chi tiết mô tả báo giá.</span><span class="sxs-lookup"><span data-stu-id="4018d-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="4018d-131">Khi một dự án không được ánh xạ tới mô tả báo giá dựa trên dự án, ước tính sẽ được tạo theo cách thủ công bằng cách tạo chi tiết từng mô tả báo giá.</span><span class="sxs-lookup"><span data-stu-id="4018d-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="4018d-132">Giá trị này được sao chép vào mục mô tả hợp đồng dự án được tạo từ mục mô tả báo giá này khi có được báo giá.</span><span class="sxs-lookup"><span data-stu-id="4018d-132">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="4018d-133">Các tác vụ được đưa vào</span><span class="sxs-lookup"><span data-stu-id="4018d-133">Included Tasks</span></span> | <span data-ttu-id="4018d-134">Cho biết mô tả báo giá này được sử dụng cho tất cả hoặc một số tác vụ dự án cho dự án đã chọn.</span><span class="sxs-lookup"><span data-stu-id="4018d-134">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="4018d-135">Trường này có các giá trị khả dĩ sau đây:</span><span class="sxs-lookup"><span data-stu-id="4018d-135">This field has the following possible values:</span></span></br><span data-ttu-id="4018d-136">- Tất cả tác vụ dự án</span><span class="sxs-lookup"><span data-stu-id="4018d-136">- All project tasks</span></span></br><span data-ttu-id="4018d-137">- Chỉ các tác vụ dự án đã chọn</span><span class="sxs-lookup"><span data-stu-id="4018d-137">- Selected project tasks only</span></span></br><span data-ttu-id="4018d-138">Giá trị trống trong trường này tương đương với tùy chọn **Tất cả tác vụ dự án**.</span><span class="sxs-lookup"><span data-stu-id="4018d-138">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="4018d-139">Khi **Chỉ các nhiệm vụ dự án đã chọn** được chọn trên trang dự án, tab **Thiết lập thanh toán theo nhiệm vụ** cho phép bạn chọn các nhiệm vụ cụ thể để liên kết chúng với mục mô tả báo giá này.</span><span class="sxs-lookup"><span data-stu-id="4018d-139">When **Selected project tasks only** is selected on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="4018d-140">Giá trị này được sao chép vào mục mô tả hợp đồng dự án được tạo từ mục mô tả báo giá này khi có được báo giá.</span><span class="sxs-lookup"><span data-stu-id="4018d-140">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="4018d-141">Bao gồm Thời gian</span><span class="sxs-lookup"><span data-stu-id="4018d-141">Include Time</span></span> | <span data-ttu-id="4018d-142">Giá trị **Có**/**Không** cho biết liệu các giao dịch thời gian hoặc chi phí nhân công của dự án đã chọn có được đưa vào phần ước tính trên mục mô tả báo giá này hay không.</span><span class="sxs-lookup"><span data-stu-id="4018d-142">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="4018d-143">Giá trị **Không** cho biết rằng giao dịch thời gian hoặc chi phí nhân công sẽ không được bao gồm trong ước tính trên mô tả báo giá này.</span><span class="sxs-lookup"><span data-stu-id="4018d-143">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="4018d-144">Giá trị **Có** cho biết rằng giao dịch thời gian hoặc chi phí nhân công sẽ được bao gồm trong ước tính trên mô tả báo giá này.</span><span class="sxs-lookup"><span data-stu-id="4018d-144">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="4018d-145">Giá trị này được sao chép vào mục mô tả hợp đồng dự án được tạo từ mục mô tả báo giá này khi có được báo giá.</span><span class="sxs-lookup"><span data-stu-id="4018d-145">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="4018d-146">Bao gồm Chi phí</span><span class="sxs-lookup"><span data-stu-id="4018d-146">Include Expense</span></span> | <span data-ttu-id="4018d-147">Giá trị **Có**/**Không** cho biết liệu các chi phí của dự án đã chọn có được đưa vào phần ước tính trên mục mô tả báo giá này hay không.</span><span class="sxs-lookup"><span data-stu-id="4018d-147">A **Yes**/**No** value indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="4018d-148">Giá trị **Không** cho biết rằng chi phí phí tổn sẽ không được bao gồm trong ước tính trên mô tả báo giá này.</span><span class="sxs-lookup"><span data-stu-id="4018d-148">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="4018d-149">Giá trị **Có** cho biết rằng chi phí phí tổn sẽ được bao gồm trong ước tính trên mô tả báo giá này.</span><span class="sxs-lookup"><span data-stu-id="4018d-149">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="4018d-150">Giá trị này được sao chép vào mục mô tả hợp đồng dự án được tạo từ mục mô tả báo giá này khi có được báo giá.</span><span class="sxs-lookup"><span data-stu-id="4018d-150">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="4018d-151">Bao gồm vật liệu</span><span class="sxs-lookup"><span data-stu-id="4018d-151">Include Material</span></span> | <span data-ttu-id="4018d-152">Giá trị **Có**/**Không** cho biết liệu các chi phí vật tư của dự án đã chọn có được đưa vào phần ước tính trên mục mô tả báo giá này hay không.</span><span class="sxs-lookup"><span data-stu-id="4018d-152">A **Yes**/**No** value indicates if material costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="4018d-153">Giá trị **Không** cho biết các chi phí vật tư sẽ không được đưa vào phần ước tính trên mục mô tả báo giá này.</span><span class="sxs-lookup"><span data-stu-id="4018d-153">A **No** value indicates that the material costs will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="4018d-154">Giá trị **Có** cho biết các chi phí vật tư sẽ không được đưa vào phần ước tính trên mục mô tả báo giá này.</span><span class="sxs-lookup"><span data-stu-id="4018d-154">A **Yes** value indicates that the material costs will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="4018d-155">Giá trị này được sao chép vào mục mô tả hợp đồng dự án được tạo từ mục mô tả báo giá này khi có được báo giá.</span><span class="sxs-lookup"><span data-stu-id="4018d-155">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="4018d-156">Bao gồm Phí</span><span class="sxs-lookup"><span data-stu-id="4018d-156">Include Fee</span></span> | <span data-ttu-id="4018d-157">Giá trị **Có**/**Không** cho biết liệu các khoản phí của dự án đã chọn có được đưa vào phần ước tính trên mục mô tả báo giá này hay không.</span><span class="sxs-lookup"><span data-stu-id="4018d-157">A **Yes**/**No** value indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="4018d-158">Giá trị **Không** cho biết rằng các khoản phí sẽ không được đưa vào phần ước tính trên mục mô tả báo giá này.</span><span class="sxs-lookup"><span data-stu-id="4018d-158">A **No** value indicates that the fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="4018d-159">Giá trị **Có** cho biết rằng các khoản phí sẽ được đưa vào phần ước tính trên mục mô tả báo giá này.</span><span class="sxs-lookup"><span data-stu-id="4018d-159">A **Yes** value indicates that the fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="4018d-160">Giá trị này được sao chép vào mục Mô tả hợp đồng dự án được tạo từ mục mô tả báo giá này khi có được báo giá.</span><span class="sxs-lookup"><span data-stu-id="4018d-160">This value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="4018d-161">Số tiền Đã báo giá</span><span class="sxs-lookup"><span data-stu-id="4018d-161">Quoted Amount</span></span> | <span data-ttu-id="4018d-162">Đây là số tiền sẽ được báo giá cho khách hàng đối với tất cả các công việc được dự báo trên mục mô tả báo giá dựa trên dự án này.</span><span class="sxs-lookup"><span data-stu-id="4018d-162">This is the amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="4018d-163">Trên một báo giá tạo từ một cơ hội, giá trị này được sao chép từ trường **Ngân sách khách hàng** trên mô tả cơ hội.</span><span class="sxs-lookup"><span data-stu-id="4018d-163">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="4018d-164">Khi mô tả báo giá dựa trên dự án có chi tiết mô tả, trường này bị khóa tính năng chỉnh sửa và được tóm tắt từ số tiền trên chi tiết mô tả báo giá.</span><span class="sxs-lookup"><span data-stu-id="4018d-164">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="4018d-165">Giá trị này được sao chép vào mục mô tả hợp đồng dự án được tạo từ mục mô tả báo giá này khi có được báo giá.</span><span class="sxs-lookup"><span data-stu-id="4018d-165">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="4018d-166">Thuế Ước tính</span><span class="sxs-lookup"><span data-stu-id="4018d-166">Estimated Tax</span></span> | <span data-ttu-id="4018d-167">Đây là trường có thể chỉnh sửa để người dùng thêm số tiền thuế ước tính trên mô tả báo giá.</span><span class="sxs-lookup"><span data-stu-id="4018d-167">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="4018d-168">Khi mô tả báo giá dựa trên dự án có chi tiết mô tả, trường này bị khóa tính năng chỉnh sửa và được tóm tắt từ số tiền thuế trên chi tiết mô tả báo giá.</span><span class="sxs-lookup"><span data-stu-id="4018d-168">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="4018d-169">Giá trị này được sao chép vào mục mô tả hợp đồng dự án được tạo từ mục mô tả báo giá này khi có được báo giá.</span><span class="sxs-lookup"><span data-stu-id="4018d-169">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="4018d-170">Số tiền đã báo giá sau thuế</span><span class="sxs-lookup"><span data-stu-id="4018d-170">Quoted Amount after Tax</span></span> | <span data-ttu-id="4018d-171">Trường này là số tiền mô tả báo giá sau thuế và ở dạng chỉ đọc.</span><span class="sxs-lookup"><span data-stu-id="4018d-171">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="4018d-172">Số tiền trong trường này được tính là *Số tiền báo giá + Thuế*.</span><span class="sxs-lookup"><span data-stu-id="4018d-172">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="4018d-173">Giá trị này được sao chép vào mục mô tả hợp đồng dự án được tạo từ mục mô tả báo giá này khi có được báo giá.</span><span class="sxs-lookup"><span data-stu-id="4018d-173">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="4018d-174">Giới hạn không vượt quá</span><span class="sxs-lookup"><span data-stu-id="4018d-174">Not-to-exceed Limit</span></span> | <span data-ttu-id="4018d-175">Trường này có thể chỉnh sửa và chỉ có sẵn trên các mô tả báo giá dựa trên dự án có phương thức thanh toán **Thời gian và vật tư**.</span><span class="sxs-lookup"><span data-stu-id="4018d-175">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="4018d-176">Giá trị này được sao chép vào mục mô tả hợp đồng dự án được tạo từ mục mô tả báo giá này khi có được báo giá.</span><span class="sxs-lookup"><span data-stu-id="4018d-176">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="4018d-177">Ngân sách Khách hàng</span><span class="sxs-lookup"><span data-stu-id="4018d-177">Customer Budget</span></span> | <span data-ttu-id="4018d-178">Trường này có thể chỉnh sửa và được sao chép từ trường tương ứng trên mô tả cơ hội nếu báo giá được tạo từ một cơ hội.</span><span class="sxs-lookup"><span data-stu-id="4018d-178">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="4018d-179">Giá trị này được sao chép vào mục mô tả hợp đồng dự án được tạo từ mục mô tả báo giá này khi có được báo giá.</span><span class="sxs-lookup"><span data-stu-id="4018d-179">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="4018d-180">Quy tắc xác thực cho các trường trên tab Tổng quát của các mô tả báo giá dựa trên dự án</span><span class="sxs-lookup"><span data-stu-id="4018d-180">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="4018d-181">**Quy tắc 1**: Nếu trường **Các tác vụ được đưa vào** bị trống hoặc nếu nó được đặt thành **Tất cả các tác vụ dự án**, một dự án sẽ được bao gồm trong mô tả báo giá.</span><span class="sxs-lookup"><span data-stu-id="4018d-181">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="4018d-182">**Quy tắc 2**: Nếu trường **Các tác vụ được đưa vào** bị trống hoặc nếu nó được đặt thành **Tất cả các tác vụ dự án**, một dự án và một lớp giao dịch nhất định chỉ có thể được đưa vào một mô tả báo giá dựa trên dự án của báo giá.</span><span class="sxs-lookup"><span data-stu-id="4018d-182">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="4018d-183">**Quy tắc 3**: Nếu trường **Các tác vụ được đưa vào** được đặt thành **Chỉ các tác vụ dự án đã chọn**, một dự án và một lớp giao dịch nhất định có thể được đưa vào nhiều mô tả báo giá dựa trên dự án của báo giá.</span><span class="sxs-lookup"><span data-stu-id="4018d-183">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="4018d-184">**Quy tắc 4**: Nếu một cơ hội có nhiều báo giá, có thể có các mô tả báo giá từ các báo giá khác nhau mà đều tham chiếu đến cùng một dự án và bao gồm cùng một lớp giao dịch.</span><span class="sxs-lookup"><span data-stu-id="4018d-184">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="4018d-185">**Quy tắc 5** : Nếu các báo giá không thuộc cùng một cơ hội, chúng không thể bao gồm cùng một dự án và lớp giao dịch.</span><span class="sxs-lookup"><span data-stu-id="4018d-185">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p><span data-ttu-id="4018d-186">
                    <strong>Cơ hội</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4018d-186">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="39" valign="top">
                <p><span data-ttu-id="4018d-187">
                    <strong>Báo giá</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4018d-187">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="40" valign="top">
                <p><span data-ttu-id="4018d-188">
                    <strong>Mô tả báo giá</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4018d-188">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="4018d-189">
                    <strong>Dự án</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4018d-189">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="77" valign="top">
                <p><span data-ttu-id="4018d-190">
                    <strong>Các tác vụ được đưa vào</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4018d-190">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="45" valign="top">
                <p><span data-ttu-id="4018d-191">
                    <strong>Bao gồm Thời gian</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4018d-191">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="46" valign="top">
                <p><span data-ttu-id="4018d-192">
                    <strong>Bao gồm Chi phí</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4018d-192">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="43" valign="top">
                <p><span data-ttu-id="4018d-193">
                    <strong>Bao gồm vật liệu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4018d-193">
                    <strong>Include Material</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="4018d-194">
                    <strong>Bao gồm</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4018d-194">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="4018d-195">
                    <strong>Phí</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4018d-195">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="49" valign="top">
                <p><span data-ttu-id="4018d-196">
                    <strong>Hợp lệ/Không hợp lệ</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4018d-196">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="200" valign="top">
                <p><span data-ttu-id="4018d-197">
                    <strong>Lý do</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4018d-197">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="4018d-198">O1</span><span class="sxs-lookup"><span data-stu-id="4018d-198">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="4018d-199">Q1</span><span class="sxs-lookup"><span data-stu-id="4018d-199">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="4018d-200">QL1</span><span class="sxs-lookup"><span data-stu-id="4018d-200">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4018d-201">Kỳ 1</span><span class="sxs-lookup"><span data-stu-id="4018d-201">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="4018d-202">Trống</span><span class="sxs-lookup"><span data-stu-id="4018d-202">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="4018d-203">Có</span><span class="sxs-lookup"><span data-stu-id="4018d-203">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="4018d-204">Có</span><span class="sxs-lookup"><span data-stu-id="4018d-204">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="4018d-205">Có</span><span class="sxs-lookup"><span data-stu-id="4018d-205">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4018d-206">Có</span><span class="sxs-lookup"><span data-stu-id="4018d-206">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4018d-207">Không hợp lệ</span><span class="sxs-lookup"><span data-stu-id="4018d-207">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4018d-208">Vi phạm Quy tắc số 2.</span><span class="sxs-lookup"><span data-stu-id="4018d-208">Violation of Rule #2.</span></span> <span data-ttu-id="4018d-209">Thời gian, Chi phí và Phí cho dự án P1 được đưa vào các mục mô tả báo giá QL1 và QL2</span><span class="sxs-lookup"><span data-stu-id="4018d-209">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="4018d-210">O1</span><span class="sxs-lookup"><span data-stu-id="4018d-210">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="4018d-211">Q1</span><span class="sxs-lookup"><span data-stu-id="4018d-211">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="4018d-212">QL2</span><span class="sxs-lookup"><span data-stu-id="4018d-212">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4018d-213">Kỳ 1</span><span class="sxs-lookup"><span data-stu-id="4018d-213">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="4018d-214">Trống</span><span class="sxs-lookup"><span data-stu-id="4018d-214">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="4018d-215">Có</span><span class="sxs-lookup"><span data-stu-id="4018d-215">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="4018d-216">Có</span><span class="sxs-lookup"><span data-stu-id="4018d-216">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="4018d-217">Có</span><span class="sxs-lookup"><span data-stu-id="4018d-217">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4018d-218">Có</span><span class="sxs-lookup"><span data-stu-id="4018d-218">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="4018d-219">O1</span><span class="sxs-lookup"><span data-stu-id="4018d-219">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="4018d-220">Q1</span><span class="sxs-lookup"><span data-stu-id="4018d-220">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="4018d-221">QL1</span><span class="sxs-lookup"><span data-stu-id="4018d-221">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4018d-222">Kỳ 1</span><span class="sxs-lookup"><span data-stu-id="4018d-222">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="4018d-223">Trống</span><span class="sxs-lookup"><span data-stu-id="4018d-223">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="4018d-224">Có</span><span class="sxs-lookup"><span data-stu-id="4018d-224">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="4018d-225">No</span><span class="sxs-lookup"><span data-stu-id="4018d-225">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="4018d-226">Có</span><span class="sxs-lookup"><span data-stu-id="4018d-226">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4018d-227">Có</span><span class="sxs-lookup"><span data-stu-id="4018d-227">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4018d-228">Không hợp lệ</span><span class="sxs-lookup"><span data-stu-id="4018d-228">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4018d-229">Vi phạm Quy tắc số 2.</span><span class="sxs-lookup"><span data-stu-id="4018d-229">Violation of Rule #2.</span></span> <span data-ttu-id="4018d-230">Thời gian, Vật tư và Phí cho dự án P1 được đưa vào các mục mô tả báo giá QL1 và QL2</span><span class="sxs-lookup"><span data-stu-id="4018d-230">Time, Material, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="4018d-231">O1</span><span class="sxs-lookup"><span data-stu-id="4018d-231">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="4018d-232">Q1</span><span class="sxs-lookup"><span data-stu-id="4018d-232">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="4018d-233">QL2</span><span class="sxs-lookup"><span data-stu-id="4018d-233">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4018d-234">Kỳ 1</span><span class="sxs-lookup"><span data-stu-id="4018d-234">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="4018d-235">Trống</span><span class="sxs-lookup"><span data-stu-id="4018d-235">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="4018d-236">Có</span><span class="sxs-lookup"><span data-stu-id="4018d-236">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="4018d-237">Có</span><span class="sxs-lookup"><span data-stu-id="4018d-237">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="4018d-238">Có</span><span class="sxs-lookup"><span data-stu-id="4018d-238">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4018d-239">Có</span><span class="sxs-lookup"><span data-stu-id="4018d-239">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="4018d-240">O1</span><span class="sxs-lookup"><span data-stu-id="4018d-240">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="4018d-241">Q1</span><span class="sxs-lookup"><span data-stu-id="4018d-241">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="4018d-242">QL1</span><span class="sxs-lookup"><span data-stu-id="4018d-242">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4018d-243">Kỳ 1</span><span class="sxs-lookup"><span data-stu-id="4018d-243">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="4018d-244">Trống</span><span class="sxs-lookup"><span data-stu-id="4018d-244">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="4018d-245">Có</span><span class="sxs-lookup"><span data-stu-id="4018d-245">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="4018d-246">No</span><span class="sxs-lookup"><span data-stu-id="4018d-246">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="4018d-247">Có</span><span class="sxs-lookup"><span data-stu-id="4018d-247">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4018d-248">Có</span><span class="sxs-lookup"><span data-stu-id="4018d-248">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4018d-249">Hợp lệ</span><span class="sxs-lookup"><span data-stu-id="4018d-249">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4018d-250">Thời gian, Vật tư và Phí cho dự án P1 được đưa vào QL1</span><span class="sxs-lookup"><span data-stu-id="4018d-250">Time, Material, and Fees on P1 project are included on QL1</span></span> <br>
<span data-ttu-id="4018d-251">Chi phí trên dự án P1 được đưa vào QL2</span><span class="sxs-lookup"><span data-stu-id="4018d-251">Expense on P1 project is included on QL2</span></span> <br>
<span data-ttu-id="4018d-252">Những nội dung được đưa vào mỗi mục mô tả báo giá là hợp lệ do không bị trùng lặp.</span><span class="sxs-lookup"><span data-stu-id="4018d-252">No overlap in what is being included on each quote line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="4018d-253">O1</span><span class="sxs-lookup"><span data-stu-id="4018d-253">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="4018d-254">Q1</span><span class="sxs-lookup"><span data-stu-id="4018d-254">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="4018d-255">QL2</span><span class="sxs-lookup"><span data-stu-id="4018d-255">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4018d-256">Kỳ 1</span><span class="sxs-lookup"><span data-stu-id="4018d-256">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="4018d-257">Trống</span><span class="sxs-lookup"><span data-stu-id="4018d-257">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="4018d-258">No</span><span class="sxs-lookup"><span data-stu-id="4018d-258">No</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="4018d-259">Có</span><span class="sxs-lookup"><span data-stu-id="4018d-259">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="4018d-260">No</span><span class="sxs-lookup"><span data-stu-id="4018d-260">No</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4018d-261">No</span><span class="sxs-lookup"><span data-stu-id="4018d-261">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="4018d-262">O1</span><span class="sxs-lookup"><span data-stu-id="4018d-262">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="4018d-263">Q1</span><span class="sxs-lookup"><span data-stu-id="4018d-263">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="4018d-264">QL1</span><span class="sxs-lookup"><span data-stu-id="4018d-264">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4018d-265">Kỳ 1</span><span class="sxs-lookup"><span data-stu-id="4018d-265">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="4018d-266">Chỉ các tác vụ được chọn</span><span class="sxs-lookup"><span data-stu-id="4018d-266">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="4018d-267">Có</span><span class="sxs-lookup"><span data-stu-id="4018d-267">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="4018d-268">Có</span><span class="sxs-lookup"><span data-stu-id="4018d-268">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="4018d-269">Có</span><span class="sxs-lookup"><span data-stu-id="4018d-269">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4018d-270">Có</span><span class="sxs-lookup"><span data-stu-id="4018d-270">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4018d-271">Không hợp lệ</span><span class="sxs-lookup"><span data-stu-id="4018d-271">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4018d-272">Vi phạm quy tắc số 2</span><span class="sxs-lookup"><span data-stu-id="4018d-272">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="4018d-273">Q1 bao gồm Thời gian, Vật tư, Chi phí và Phí cho một tập hợp con các nhiệm vụ trong dự án P1</span><span class="sxs-lookup"><span data-stu-id="4018d-273">Q1 includes Time, Material, Expenses and Fees on a subset of tasks on project P1</span></span> </p>
                <p>
<span data-ttu-id="4018d-274">QL2 bao gồm Thời gian, Chi phí và Phí của toàn bộ dự án P1, do đó trùng lặp với những số liệu được đưa vào Q1.</span><span class="sxs-lookup"><span data-stu-id="4018d-274">QL2 includes Time, Expenses, and Fees for the whole project P1 and therefore overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="4018d-275">O1</span><span class="sxs-lookup"><span data-stu-id="4018d-275">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="4018d-276">Q1</span><span class="sxs-lookup"><span data-stu-id="4018d-276">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="4018d-277">QL2</span><span class="sxs-lookup"><span data-stu-id="4018d-277">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4018d-278">Kỳ 1</span><span class="sxs-lookup"><span data-stu-id="4018d-278">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="4018d-279">Trống</span><span class="sxs-lookup"><span data-stu-id="4018d-279">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="4018d-280">Có</span><span class="sxs-lookup"><span data-stu-id="4018d-280">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="4018d-281">Có</span><span class="sxs-lookup"><span data-stu-id="4018d-281">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="4018d-282">Có</span><span class="sxs-lookup"><span data-stu-id="4018d-282">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4018d-283">Có</span><span class="sxs-lookup"><span data-stu-id="4018d-283">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="4018d-284">O1</span><span class="sxs-lookup"><span data-stu-id="4018d-284">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="4018d-285">Q1</span><span class="sxs-lookup"><span data-stu-id="4018d-285">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="4018d-286">QL1</span><span class="sxs-lookup"><span data-stu-id="4018d-286">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4018d-287">Kỳ 1</span><span class="sxs-lookup"><span data-stu-id="4018d-287">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="4018d-288">Chỉ các tác vụ được chọn</span><span class="sxs-lookup"><span data-stu-id="4018d-288">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="4018d-289">Có</span><span class="sxs-lookup"><span data-stu-id="4018d-289">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="4018d-290">Có</span><span class="sxs-lookup"><span data-stu-id="4018d-290">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="4018d-291">Có</span><span class="sxs-lookup"><span data-stu-id="4018d-291">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4018d-292">Có</span><span class="sxs-lookup"><span data-stu-id="4018d-292">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4018d-293">Hợp lệ</span><span class="sxs-lookup"><span data-stu-id="4018d-293">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4018d-294">Theo quy tắc số 3,</span><span class="sxs-lookup"><span data-stu-id="4018d-294">Per Rule #3,</span></span> </p>
                <p>
<span data-ttu-id="4018d-295">Q1 bao gồm Thời gian, Vật tư, Chi phí và Phí cho một tập hợp con các nhiệm vụ trong dự án P1.</span><span class="sxs-lookup"><span data-stu-id="4018d-295">Q1 includes Time, Material, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="4018d-296">QL2 bao gồm Thời gian, Vật tư, Chi phí và Phí cho một tập hợp con các nhiệm vụ trong dự án P1.</span><span class="sxs-lookup"><span data-stu-id="4018d-296">QL2 includes Time, Material, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="4018d-297">Bước xác thực bổ sung duy nhất xoay quanh việc tập hợp con các nhiệm vụ trên QL1 khác với tập hợp con các nhiệm vụ trên QL2 để đảm bảo rằng không có sự trùng lặp.</span><span class="sxs-lookup"><span data-stu-id="4018d-297">The only additional validation is around the subset of tasks on QL1 which is different from the subset of tasks on QL2 to ensure that there is no overlap.</span></span> <span data-ttu-id="4018d-298">Điều này được hệ thống thực hiện khi các nhiệm vụ được liên kết.</span><span class="sxs-lookup"><span data-stu-id="4018d-298">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="4018d-299">O1</span><span class="sxs-lookup"><span data-stu-id="4018d-299">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="4018d-300">Q1</span><span class="sxs-lookup"><span data-stu-id="4018d-300">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="4018d-301">QL2</span><span class="sxs-lookup"><span data-stu-id="4018d-301">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4018d-302">Kỳ 1</span><span class="sxs-lookup"><span data-stu-id="4018d-302">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="4018d-303">Chỉ các tác vụ được chọn</span><span class="sxs-lookup"><span data-stu-id="4018d-303">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="4018d-304">Có</span><span class="sxs-lookup"><span data-stu-id="4018d-304">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="4018d-305">Có</span><span class="sxs-lookup"><span data-stu-id="4018d-305">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="4018d-306">Có</span><span class="sxs-lookup"><span data-stu-id="4018d-306">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4018d-307">Có</span><span class="sxs-lookup"><span data-stu-id="4018d-307">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="4018d-308">O1</span><span class="sxs-lookup"><span data-stu-id="4018d-308">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="4018d-309">Q1</span><span class="sxs-lookup"><span data-stu-id="4018d-309">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="4018d-310">QL1</span><span class="sxs-lookup"><span data-stu-id="4018d-310">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4018d-311">Kỳ 1</span><span class="sxs-lookup"><span data-stu-id="4018d-311">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="4018d-312">Tất cả các tác vụ dự án hoặc để trống</span><span class="sxs-lookup"><span data-stu-id="4018d-312">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="4018d-313">Có</span><span class="sxs-lookup"><span data-stu-id="4018d-313">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="4018d-314">Có</span><span class="sxs-lookup"><span data-stu-id="4018d-314">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="4018d-315">Có</span><span class="sxs-lookup"><span data-stu-id="4018d-315">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4018d-316">Có</span><span class="sxs-lookup"><span data-stu-id="4018d-316">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4018d-317">Hợp lệ</span><span class="sxs-lookup"><span data-stu-id="4018d-317">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4018d-318">Theo Quy tắc số 5, Q1 và Q2 là hai báo giá về cùng một cơ hội, vì vậy cả hai đều có thể ước tính cho các thành phần giống nhau của một dự án.</span><span class="sxs-lookup"><span data-stu-id="4018d-318">Per Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="4018d-319">O1</span><span class="sxs-lookup"><span data-stu-id="4018d-319">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="4018d-320">Q2</span><span class="sxs-lookup"><span data-stu-id="4018d-320">Q2</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="4018d-321">QL1</span><span class="sxs-lookup"><span data-stu-id="4018d-321">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4018d-322">Kỳ 1</span><span class="sxs-lookup"><span data-stu-id="4018d-322">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="4018d-323">Tất cả các tác vụ dự án hoặc để trống</span><span class="sxs-lookup"><span data-stu-id="4018d-323">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="4018d-324">Có</span><span class="sxs-lookup"><span data-stu-id="4018d-324">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="4018d-325">Có</span><span class="sxs-lookup"><span data-stu-id="4018d-325">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="4018d-326">Có</span><span class="sxs-lookup"><span data-stu-id="4018d-326">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4018d-327">Có</span><span class="sxs-lookup"><span data-stu-id="4018d-327">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="4018d-328">O1</span><span class="sxs-lookup"><span data-stu-id="4018d-328">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="4018d-329">Q1</span><span class="sxs-lookup"><span data-stu-id="4018d-329">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="4018d-330">QL1</span><span class="sxs-lookup"><span data-stu-id="4018d-330">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4018d-331">Kỳ 1</span><span class="sxs-lookup"><span data-stu-id="4018d-331">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="4018d-332">Tất cả các tác vụ dự án hoặc để trống</span><span class="sxs-lookup"><span data-stu-id="4018d-332">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="4018d-333">Có</span><span class="sxs-lookup"><span data-stu-id="4018d-333">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="4018d-334">Có</span><span class="sxs-lookup"><span data-stu-id="4018d-334">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="4018d-335">Có</span><span class="sxs-lookup"><span data-stu-id="4018d-335">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4018d-336">Có</span><span class="sxs-lookup"><span data-stu-id="4018d-336">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4018d-337">Không hợp lệ</span><span class="sxs-lookup"><span data-stu-id="4018d-337">Not Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4018d-338">Theo Quy tắc số 4, Q1 và Q2 là hai báo giá về các cơ hội khác nhau, vì vậy cả hai đều không thể ước tính cho các thành phần giống nhau của cùng một dự án.</span><span class="sxs-lookup"><span data-stu-id="4018d-338">Per Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="4018d-339">O2</span><span class="sxs-lookup"><span data-stu-id="4018d-339">O2</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="4018d-340">Q1</span><span class="sxs-lookup"><span data-stu-id="4018d-340">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="4018d-341">QL1</span><span class="sxs-lookup"><span data-stu-id="4018d-341">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4018d-342">Kỳ 1</span><span class="sxs-lookup"><span data-stu-id="4018d-342">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="4018d-343">Tất cả các tác vụ dự án hoặc để trống</span><span class="sxs-lookup"><span data-stu-id="4018d-343">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="4018d-344">Có</span><span class="sxs-lookup"><span data-stu-id="4018d-344">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="4018d-345">Có</span><span class="sxs-lookup"><span data-stu-id="4018d-345">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="4018d-346">Có</span><span class="sxs-lookup"><span data-stu-id="4018d-346">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4018d-347">Có</span><span class="sxs-lookup"><span data-stu-id="4018d-347">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
