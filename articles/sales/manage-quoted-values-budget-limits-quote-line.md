---
title: Dòng báo giá dựa trên dự án
description: Chủ đề này cung cấp thông tin về việc sử dụng các mô tả báo giá dựa trên dự án cho công việc dự án.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 06a47c45dc3b3b174658e2fba14d3d2050aabf85
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086975"
---
# <a name="project-based-quote-lines"></a><span data-ttu-id="4cf84-103">Dòng báo giá dựa trên dự án</span><span class="sxs-lookup"><span data-stu-id="4cf84-103">Project-based quote lines</span></span>

<span data-ttu-id="4cf84-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_</span><span class="sxs-lookup"><span data-stu-id="4cf84-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="4cf84-105">Các mô tả báo giá dựa trên dự án được thiết kế để giúp ước tính công việc dự án trên một cam kết.</span><span class="sxs-lookup"><span data-stu-id="4cf84-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="4cf84-106">Cấu trúc của mô tả báo giá dựa trên dự án được mở rộng cho các ước tính dự án với các khái niệm sau:</span><span class="sxs-lookup"><span data-stu-id="4cf84-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="4cf84-107">Phương thức Thanh toán</span><span class="sxs-lookup"><span data-stu-id="4cf84-107">Billing Method</span></span>
- <span data-ttu-id="4cf84-108">Ánh xạ dự án</span><span class="sxs-lookup"><span data-stu-id="4cf84-108">Project Mapping</span></span>
- <span data-ttu-id="4cf84-109">Các lớp giao dịch được bao gồm</span><span class="sxs-lookup"><span data-stu-id="4cf84-109">Included Transaction classes</span></span>
- <span data-ttu-id="4cf84-110">Giới hạn không vượt quá</span><span class="sxs-lookup"><span data-stu-id="4cf84-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="4cf84-111">Thiết lập khả năng tính phí</span><span class="sxs-lookup"><span data-stu-id="4cf84-111">Chargeability setup</span></span>
- <span data-ttu-id="4cf84-112">Ước tính bằng cách sử dụng Chi tiết mô tả báo giá</span><span class="sxs-lookup"><span data-stu-id="4cf84-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="4cf84-113">Khách hàng trên mô tả báo giá</span><span class="sxs-lookup"><span data-stu-id="4cf84-113">Quote line Customers</span></span>

<span data-ttu-id="4cf84-114">Bảng sau cung cấp thông tin về các trường trên tab **Tổng quát** của mô tả báo giá dựa trên dự án.</span><span class="sxs-lookup"><span data-stu-id="4cf84-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="4cf84-115">Các trường này giúp thiết lập cơ sở để ước tính chi tiết, nền tảng cho công việc dự án.</span><span class="sxs-lookup"><span data-stu-id="4cf84-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="4cf84-116">**Trường**</span><span class="sxs-lookup"><span data-stu-id="4cf84-116">**Field**</span></span> | <span data-ttu-id="4cf84-117">**Mức độ liên quan, mục đích và hướng dẫn**</span><span class="sxs-lookup"><span data-stu-id="4cf84-117">**Relevance, purpose, and guidance**</span></span> | <span data-ttu-id="4cf84-118">**Tác động xuôi tuyến**</span><span class="sxs-lookup"><span data-stu-id="4cf84-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="4cf84-119">Tên</span><span class="sxs-lookup"><span data-stu-id="4cf84-119">Name</span></span> | <span data-ttu-id="4cf84-120">Tên của mô tả báo giá sẽ giúp bạn xác định thành phần riêng biệt của báo giá đang được ước tính.</span><span class="sxs-lookup"><span data-stu-id="4cf84-120">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="4cf84-121">Được sao chép vào mô tả hợp đồng dự án tạo từ mô tả báo giá này khi báo giá được chốt.</span><span class="sxs-lookup"><span data-stu-id="4cf84-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="4cf84-122">Phương thức Thanh toán</span><span class="sxs-lookup"><span data-stu-id="4cf84-122">Billing Method</span></span> | <span data-ttu-id="4cf84-123">Trên một báo giá tạo từ một cơ hội, giá trị này được sao chép từ trường tương ứng trên mô tả cơ hội.</span><span class="sxs-lookup"><span data-stu-id="4cf84-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="4cf84-124">Trường này bao gồm hai mô hình hợp đồng chính được hỗ trợ bởi Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="4cf84-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="4cf84-125">- Giá cố định</span><span class="sxs-lookup"><span data-stu-id="4cf84-125">- Fixed price</span></span></br><span data-ttu-id="4cf84-126">- Thời gian và vật tư.</span><span class="sxs-lookup"><span data-stu-id="4cf84-126">- Time and material.</span></span>| <span data-ttu-id="4cf84-127">Giá trị trường này được sao chép vào mô tả hợp đồng dự án tạo từ mô tả báo giá này khi báo giá được chốt.</span><span class="sxs-lookup"><span data-stu-id="4cf84-127">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="4cf84-128">Dự án</span><span class="sxs-lookup"><span data-stu-id="4cf84-128">Project</span></span> | <span data-ttu-id="4cf84-129">Sử dụng trường tùy chọn này để xác định dự án sẽ được sử dụng để thực hiện công việc trong cam kết này.</span><span class="sxs-lookup"><span data-stu-id="4cf84-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="4cf84-130">Khi một dự án được ánh xạ đến một mô tả báo giá, nó sẽ giúp thiết lập các tác vụ có thể tính phí, đồng thời đưa ước tính dựa trên dự án vào mô tả báo giá dưới dạng chi tiết mô tả báo giá.</span><span class="sxs-lookup"><span data-stu-id="4cf84-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="4cf84-131">Khi một dự án không được ánh xạ tới mô tả báo giá dựa trên dự án, ước tính sẽ được tạo theo cách thủ công bằng cách tạo chi tiết từng mô tả báo giá.</span><span class="sxs-lookup"><span data-stu-id="4cf84-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="4cf84-132">Giá trị trường này được sao chép vào mô tả hợp đồng dự án tạo từ mô tả báo giá này khi báo giá được chốt.</span><span class="sxs-lookup"><span data-stu-id="4cf84-132">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="4cf84-133">Bao gồm Thời gian</span><span class="sxs-lookup"><span data-stu-id="4cf84-133">Include Time</span></span> | <span data-ttu-id="4cf84-134">Cờ **Có**/**Không** cho biết nếu các giao dịch thời gian hoặc chi phí nhân công trên dự án đã chọn sẽ được bao gồm trong ước tính trên mô tả báo giá này.</span><span class="sxs-lookup"><span data-stu-id="4cf84-134">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="4cf84-135">Giá trị **Không** cho biết rằng giao dịch thời gian hoặc chi phí nhân công sẽ không được bao gồm trong ước tính trên mô tả báo giá này.</span><span class="sxs-lookup"><span data-stu-id="4cf84-135">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="4cf84-136">Giá trị **Có** cho biết rằng giao dịch thời gian hoặc chi phí nhân công sẽ được bao gồm trong ước tính trên mô tả báo giá này.</span><span class="sxs-lookup"><span data-stu-id="4cf84-136">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="4cf84-137">Giá trị trường này được sao chép vào mô tả hợp đồng dự án tạo từ mô tả báo giá này khi báo giá được chốt.</span><span class="sxs-lookup"><span data-stu-id="4cf84-137">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="4cf84-138">Bao gồm Chi phí</span><span class="sxs-lookup"><span data-stu-id="4cf84-138">Include Expense</span></span> | <span data-ttu-id="4cf84-139">Cờ **Có**/**Không** cho biết nếu chi phí phí tổn trên dự án đã chọn sẽ được bao gồm trong ước tính trên mô tả báo giá này.</span><span class="sxs-lookup"><span data-stu-id="4cf84-139">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="4cf84-140">Giá trị **Không** cho biết rằng chi phí phí tổn sẽ không được bao gồm trong ước tính trên mô tả báo giá này.</span><span class="sxs-lookup"><span data-stu-id="4cf84-140">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="4cf84-141">Giá trị **Có** cho biết rằng chi phí phí tổn sẽ được bao gồm trong ước tính trên mô tả báo giá này.</span><span class="sxs-lookup"><span data-stu-id="4cf84-141">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="4cf84-142">Giá trị trường này được sao chép vào mô tả hợp đồng dự án tạo từ mô tả báo giá này khi báo giá được chốt.</span><span class="sxs-lookup"><span data-stu-id="4cf84-142">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="4cf84-143">Bao gồm Phí</span><span class="sxs-lookup"><span data-stu-id="4cf84-143">Include Fee</span></span> | <span data-ttu-id="4cf84-144">Cờ **Có**/**Không** cho biết nếu các khoản phí trên dự án đã chọn sẽ được bao gồm trong ước tính trên mô tả báo giá này.</span><span class="sxs-lookup"><span data-stu-id="4cf84-144">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="4cf84-145">Giá trị **Không** cho biết rằng các khoản phí sẽ không được bao gồm trong ước tính trên mô tả báo giá này.</span><span class="sxs-lookup"><span data-stu-id="4cf84-145">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="4cf84-146">Giá trị **Có** cho biết rằng các khoản phí sẽ được bao gồm trong ước tính trên mô tả báo giá này.</span><span class="sxs-lookup"><span data-stu-id="4cf84-146">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="4cf84-147">Giá trị trường này được sao chép vào Mô tả hợp đồng dự án tạo từ mô tả báo giá này khi báo giá được chốt.</span><span class="sxs-lookup"><span data-stu-id="4cf84-147">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="4cf84-148">Số tiền Đã báo giá</span><span class="sxs-lookup"><span data-stu-id="4cf84-148">Quoted Amount</span></span> | <span data-ttu-id="4cf84-149">Đây là số tiền sẽ được báo giá cho khách hàng đối với tất cả các công việc được dự báo trên mô tả báo giá dựa trên dự án này.</span><span class="sxs-lookup"><span data-stu-id="4cf84-149">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="4cf84-150">Trên một báo giá tạo từ một cơ hội, giá trị này được sao chép từ trường **Ngân sách khách hàng** trên mô tả cơ hội.</span><span class="sxs-lookup"><span data-stu-id="4cf84-150">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="4cf84-151">Khi mô tả báo giá dựa trên dự án có chi tiết mô tả, trường này bị khóa tính năng chỉnh sửa và được tóm tắt từ số tiền trên chi tiết mô tả báo giá.</span><span class="sxs-lookup"><span data-stu-id="4cf84-151">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="4cf84-152">Giá trị trường này được sao chép vào mô tả hợp đồng dự án tạo từ mô tả báo giá này khi báo giá được chốt.</span><span class="sxs-lookup"><span data-stu-id="4cf84-152">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="4cf84-153">Thuế Ước tính</span><span class="sxs-lookup"><span data-stu-id="4cf84-153">Estimated Tax</span></span> | <span data-ttu-id="4cf84-154">Đây là trường có thể chỉnh sửa để người dùng thêm số tiền thuế ước tính trên mô tả báo giá.</span><span class="sxs-lookup"><span data-stu-id="4cf84-154">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="4cf84-155">Khi mô tả báo giá dựa trên dự án có chi tiết mô tả, trường này bị khóa tính năng chỉnh sửa và được tóm tắt từ số tiền thuế trên chi tiết mô tả báo giá.</span><span class="sxs-lookup"><span data-stu-id="4cf84-155">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="4cf84-156">Giá trị trường này được sao chép vào mô tả hợp đồng dự án tạo từ mô tả báo giá này khi báo giá được chốt.</span><span class="sxs-lookup"><span data-stu-id="4cf84-156">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="4cf84-157">Số tiền đã báo giá sau thuế</span><span class="sxs-lookup"><span data-stu-id="4cf84-157">Quoted Amount after Tax</span></span> | <span data-ttu-id="4cf84-158">Trường này là số tiền mô tả báo giá sau thuế và ở dạng chỉ đọc.</span><span class="sxs-lookup"><span data-stu-id="4cf84-158">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="4cf84-159">Số tiền trong trường này được tính là *Số tiền báo giá + Thuế*.</span><span class="sxs-lookup"><span data-stu-id="4cf84-159">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="4cf84-160">Giá trị trường này được sao chép vào mô tả hợp đồng dự án tạo từ mô tả báo giá này khi báo giá được chốt.</span><span class="sxs-lookup"><span data-stu-id="4cf84-160">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="4cf84-161">Giới hạn không vượt quá</span><span class="sxs-lookup"><span data-stu-id="4cf84-161">Not-to-exceed Limit</span></span> | <span data-ttu-id="4cf84-162">Trường này có thể chỉnh sửa và chỉ có sẵn trên các mô tả báo giá dựa trên dự án có phương thức thanh toán **Thời gian và vật tư**.</span><span class="sxs-lookup"><span data-stu-id="4cf84-162">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="4cf84-163">Giá trị trường này được sao chép vào mô tả hợp đồng dự án tạo từ mô tả báo giá này khi báo giá được chốt.</span><span class="sxs-lookup"><span data-stu-id="4cf84-163">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="4cf84-164">Ngân sách Khách hàng</span><span class="sxs-lookup"><span data-stu-id="4cf84-164">Customer Budget</span></span> | <span data-ttu-id="4cf84-165">Trường này có thể chỉnh sửa và được sao chép từ trường tương ứng trên mô tả cơ hội nếu báo giá được tạo từ một cơ hội.</span><span class="sxs-lookup"><span data-stu-id="4cf84-165">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="4cf84-166">Giá trị trường này được sao chép vào mô tả hợp đồng dự án tạo từ mô tả báo giá này khi báo giá được chốt.</span><span class="sxs-lookup"><span data-stu-id="4cf84-166">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="4cf84-167">Quy tắc xác thực cho các trường trên tab Tổng quát của các mô tả báo giá dựa trên dự án</span><span class="sxs-lookup"><span data-stu-id="4cf84-167">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="4cf84-168">**Quy tắc 1** : Một lớp giao dịch nhất định trên dự án đã chọn chỉ có thể được đưa vào một mô tả báo giá dựa trên dự án của một báo giá.</span><span class="sxs-lookup"><span data-stu-id="4cf84-168">**Rule 1** : A certain transaction class on the selected project can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="4cf84-169">**Quy tắc 2** : Nếu một cơ hội có nhiều báo giá, có thể có các dòng báo giá từ các báo giá khác nhau mà đều tham chiếu đến cùng một dự án và bao gồm cùng một lớp giao dịch.</span><span class="sxs-lookup"><span data-stu-id="4cf84-169">**Rule 2** : If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="4cf84-170">**Quy tắc 3** : Nếu các báo giá không thuộc cùng một cơ hội, chúng không thể bao gồm cùng một dự án và lớp giao dịch.</span><span class="sxs-lookup"><span data-stu-id="4cf84-170">**Rule 3** : If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="4cf84-171">
                    <strong>Cơ hội</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4cf84-171">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="4cf84-172">
                    <strong>Báo giá</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4cf84-172">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="4cf84-173">
                    <strong>Mô tả báo giá</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4cf84-173">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="4cf84-174">
                    <strong>Dự án</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4cf84-174">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="4cf84-175">
                    <strong>Bao gồm Thời gian</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4cf84-175">
                    <strong>Include time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="4cf84-176">
                    <strong>Bao gồm chi phí</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4cf84-176">
                    <strong>Include expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="4cf84-177">
                    <strong>Bao gồm</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4cf84-177">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="4cf84-178">
                    <strong>phí</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4cf84-178">
                    <strong>fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="4cf84-179">
                    <strong>Hợp lệ/Không hợp lệ</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4cf84-179">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="4cf84-180">
                    <strong>Lý do</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4cf84-180">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="4cf84-181">O1</span><span class="sxs-lookup"><span data-stu-id="4cf84-181">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4cf84-182">Q1</span><span class="sxs-lookup"><span data-stu-id="4cf84-182">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4cf84-183">QL1</span><span class="sxs-lookup"><span data-stu-id="4cf84-183">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4cf84-184">Kỳ 1</span><span class="sxs-lookup"><span data-stu-id="4cf84-184">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4cf84-185">Có</span><span class="sxs-lookup"><span data-stu-id="4cf84-185">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4cf84-186">Có</span><span class="sxs-lookup"><span data-stu-id="4cf84-186">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4cf84-187">Có</span><span class="sxs-lookup"><span data-stu-id="4cf84-187">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4cf84-188">Không hợp lệ</span><span class="sxs-lookup"><span data-stu-id="4cf84-188">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4cf84-189">Vi phạm Quy tắc số 1.</span><span class="sxs-lookup"><span data-stu-id="4cf84-189">Violation of Rule #1.</span></span> <span data-ttu-id="4cf84-190">Thời gian, Chi phí và Phí cho dự án P1 được bao gồm trên cả hai mô tả báo giá QL1 và QL2.</span><span class="sxs-lookup"><span data-stu-id="4cf84-190">Time, Expense, and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="4cf84-191">O1</span><span class="sxs-lookup"><span data-stu-id="4cf84-191">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4cf84-192">Q1</span><span class="sxs-lookup"><span data-stu-id="4cf84-192">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4cf84-193">QL2</span><span class="sxs-lookup"><span data-stu-id="4cf84-193">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4cf84-194">Kỳ 1</span><span class="sxs-lookup"><span data-stu-id="4cf84-194">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4cf84-195">Có</span><span class="sxs-lookup"><span data-stu-id="4cf84-195">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4cf84-196">Có</span><span class="sxs-lookup"><span data-stu-id="4cf84-196">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4cf84-197">Có</span><span class="sxs-lookup"><span data-stu-id="4cf84-197">Yes</span></span> </p>
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
<span data-ttu-id="4cf84-198">O1</span><span class="sxs-lookup"><span data-stu-id="4cf84-198">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4cf84-199">Q1</span><span class="sxs-lookup"><span data-stu-id="4cf84-199">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4cf84-200">QL1</span><span class="sxs-lookup"><span data-stu-id="4cf84-200">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4cf84-201">Kỳ 1</span><span class="sxs-lookup"><span data-stu-id="4cf84-201">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4cf84-202">Có</span><span class="sxs-lookup"><span data-stu-id="4cf84-202">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4cf84-203">No</span><span class="sxs-lookup"><span data-stu-id="4cf84-203">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4cf84-204">Có</span><span class="sxs-lookup"><span data-stu-id="4cf84-204">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4cf84-205">Không hợp lệ</span><span class="sxs-lookup"><span data-stu-id="4cf84-205">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4cf84-206">Vi phạm Quy tắc số 1.</span><span class="sxs-lookup"><span data-stu-id="4cf84-206">Violation of Rule #1.</span></span> <span data-ttu-id="4cf84-207">Thời gian và Chi phí cho dự án P1 được bao gồm trên cả hai mô tả báo giá QL1 và QL2.</span><span class="sxs-lookup"><span data-stu-id="4cf84-207">Time and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="4cf84-208">O1</span><span class="sxs-lookup"><span data-stu-id="4cf84-208">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4cf84-209">Q1</span><span class="sxs-lookup"><span data-stu-id="4cf84-209">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4cf84-210">QL2</span><span class="sxs-lookup"><span data-stu-id="4cf84-210">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4cf84-211">Kỳ 1</span><span class="sxs-lookup"><span data-stu-id="4cf84-211">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4cf84-212">Có</span><span class="sxs-lookup"><span data-stu-id="4cf84-212">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4cf84-213">Có</span><span class="sxs-lookup"><span data-stu-id="4cf84-213">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4cf84-214">Có</span><span class="sxs-lookup"><span data-stu-id="4cf84-214">Yes</span></span> </p>
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
<span data-ttu-id="4cf84-215">O1</span><span class="sxs-lookup"><span data-stu-id="4cf84-215">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4cf84-216">Q1</span><span class="sxs-lookup"><span data-stu-id="4cf84-216">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4cf84-217">QL1</span><span class="sxs-lookup"><span data-stu-id="4cf84-217">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4cf84-218">Kỳ 1</span><span class="sxs-lookup"><span data-stu-id="4cf84-218">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4cf84-219">Có</span><span class="sxs-lookup"><span data-stu-id="4cf84-219">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4cf84-220">No</span><span class="sxs-lookup"><span data-stu-id="4cf84-220">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4cf84-221">Có</span><span class="sxs-lookup"><span data-stu-id="4cf84-221">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4cf84-222">Hợp lệ</span><span class="sxs-lookup"><span data-stu-id="4cf84-222">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
<span data-ttu-id="4cf84-223">Thời gian và phí của dự án P1 được bao gồm trên QL1.</span><span class="sxs-lookup"><span data-stu-id="4cf84-223">Time and fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="4cf84-224">Chi phí trên dự án P1 được bao gồm trên QL2.</span><span class="sxs-lookup"><span data-stu-id="4cf84-224">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="4cf84-225">Không có sự chồng chéo về những gì được bao gồm trên mỗi mô tả, vì vậy mục này hợp lệ.</span><span class="sxs-lookup"><span data-stu-id="4cf84-225">There is no overlap in what is being included on each quote line so it is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="4cf84-226">O1</span><span class="sxs-lookup"><span data-stu-id="4cf84-226">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4cf84-227">Q1</span><span class="sxs-lookup"><span data-stu-id="4cf84-227">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4cf84-228">QL2</span><span class="sxs-lookup"><span data-stu-id="4cf84-228">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4cf84-229">Kỳ 1</span><span class="sxs-lookup"><span data-stu-id="4cf84-229">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4cf84-230">No</span><span class="sxs-lookup"><span data-stu-id="4cf84-230">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4cf84-231">Có</span><span class="sxs-lookup"><span data-stu-id="4cf84-231">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4cf84-232">No</span><span class="sxs-lookup"><span data-stu-id="4cf84-232">No</span></span> </p>
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
<span data-ttu-id="4cf84-233">O1</span><span class="sxs-lookup"><span data-stu-id="4cf84-233">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4cf84-234">Q1</span><span class="sxs-lookup"><span data-stu-id="4cf84-234">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4cf84-235">QL1</span><span class="sxs-lookup"><span data-stu-id="4cf84-235">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4cf84-236">Kỳ 1</span><span class="sxs-lookup"><span data-stu-id="4cf84-236">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4cf84-237">Có</span><span class="sxs-lookup"><span data-stu-id="4cf84-237">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4cf84-238">Có</span><span class="sxs-lookup"><span data-stu-id="4cf84-238">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4cf84-239">Có</span><span class="sxs-lookup"><span data-stu-id="4cf84-239">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4cf84-240">Không hợp lệ</span><span class="sxs-lookup"><span data-stu-id="4cf84-240">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4cf84-241">Vi phạm Quy tắc số 1 ở trên</span><span class="sxs-lookup"><span data-stu-id="4cf84-241">Violation of Rule #1 above</span></span> </p>
                <p>
<span data-ttu-id="4cf84-242">Q1 bao gồm Thời gian, Chi phí và Phí cho toàn bộ dự án P1.</span><span class="sxs-lookup"><span data-stu-id="4cf84-242">Q1 includes Time, Expenses, and Fees for the whole project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="4cf84-243">QL2 bao gồm Thời gian, Chi phí và Phí cho toàn bộ dự án P1 và chồng chéo với những gì được bao gồm trong Q1.</span><span class="sxs-lookup"><span data-stu-id="4cf84-243">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="4cf84-244">O1</span><span class="sxs-lookup"><span data-stu-id="4cf84-244">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4cf84-245">Q1</span><span class="sxs-lookup"><span data-stu-id="4cf84-245">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4cf84-246">QL2</span><span class="sxs-lookup"><span data-stu-id="4cf84-246">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4cf84-247">Kỳ 1</span><span class="sxs-lookup"><span data-stu-id="4cf84-247">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4cf84-248">Có</span><span class="sxs-lookup"><span data-stu-id="4cf84-248">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4cf84-249">Có</span><span class="sxs-lookup"><span data-stu-id="4cf84-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4cf84-250">Có</span><span class="sxs-lookup"><span data-stu-id="4cf84-250">Yes</span></span> </p>
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
<span data-ttu-id="4cf84-251">O1</span><span class="sxs-lookup"><span data-stu-id="4cf84-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4cf84-252">Q1</span><span class="sxs-lookup"><span data-stu-id="4cf84-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4cf84-253">QL1</span><span class="sxs-lookup"><span data-stu-id="4cf84-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4cf84-254">Kỳ 1</span><span class="sxs-lookup"><span data-stu-id="4cf84-254">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4cf84-255">Có</span><span class="sxs-lookup"><span data-stu-id="4cf84-255">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4cf84-256">Có</span><span class="sxs-lookup"><span data-stu-id="4cf84-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4cf84-257">Có</span><span class="sxs-lookup"><span data-stu-id="4cf84-257">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="4cf84-258">Hợp lệ</span><span class="sxs-lookup"><span data-stu-id="4cf84-258">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4cf84-259">Dựa trên Quy tắc số 2, Q1 và Q2 là hai báo giá về cùng một cơ hội, vì vậy cả hai đều có thể ước tính cho các thành phần giống nhau của dự án.</span><span class="sxs-lookup"><span data-stu-id="4cf84-259">Based on Rule #2, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="4cf84-260">O1</span><span class="sxs-lookup"><span data-stu-id="4cf84-260">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4cf84-261">Q2</span><span class="sxs-lookup"><span data-stu-id="4cf84-261">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4cf84-262">QL1 trên Q2</span><span class="sxs-lookup"><span data-stu-id="4cf84-262">QL1 on Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4cf84-263">Kỳ 1</span><span class="sxs-lookup"><span data-stu-id="4cf84-263">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4cf84-264">Có</span><span class="sxs-lookup"><span data-stu-id="4cf84-264">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4cf84-265">Có</span><span class="sxs-lookup"><span data-stu-id="4cf84-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4cf84-266">Có</span><span class="sxs-lookup"><span data-stu-id="4cf84-266">Yes</span></span> </p>
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
<span data-ttu-id="4cf84-267">O1</span><span class="sxs-lookup"><span data-stu-id="4cf84-267">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4cf84-268">Q1</span><span class="sxs-lookup"><span data-stu-id="4cf84-268">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4cf84-269">QL1</span><span class="sxs-lookup"><span data-stu-id="4cf84-269">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4cf84-270">Kỳ 1</span><span class="sxs-lookup"><span data-stu-id="4cf84-270">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4cf84-271">Có</span><span class="sxs-lookup"><span data-stu-id="4cf84-271">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4cf84-272">Có</span><span class="sxs-lookup"><span data-stu-id="4cf84-272">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4cf84-273">Có</span><span class="sxs-lookup"><span data-stu-id="4cf84-273">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="4cf84-274">Hợp lệ</span><span class="sxs-lookup"><span data-stu-id="4cf84-274">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4cf84-275">Dựa trên Quy tắc số 3, Q1 và Q2 là hai báo giá về các cơ hội khác nhau, vì vậy cả hai không thể ước tính cho các thành phần giống nhau của cùng dự án.</span><span class="sxs-lookup"><span data-stu-id="4cf84-275">Based on Rule #3, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="4cf84-276">O2</span><span class="sxs-lookup"><span data-stu-id="4cf84-276">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4cf84-277">Q1</span><span class="sxs-lookup"><span data-stu-id="4cf84-277">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4cf84-278">QL1</span><span class="sxs-lookup"><span data-stu-id="4cf84-278">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4cf84-279">Kỳ 1</span><span class="sxs-lookup"><span data-stu-id="4cf84-279">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4cf84-280">Có</span><span class="sxs-lookup"><span data-stu-id="4cf84-280">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="4cf84-281">Có</span><span class="sxs-lookup"><span data-stu-id="4cf84-281">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="4cf84-282">Có</span><span class="sxs-lookup"><span data-stu-id="4cf84-282">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="4cf84-283">Không hợp lệ</span><span class="sxs-lookup"><span data-stu-id="4cf84-283">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

