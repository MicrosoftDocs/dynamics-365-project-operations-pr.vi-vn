---
title: Tổng quan về mô tả hợp đồng dựa trên dự án
description: Chủ đề này cung cấp thông tin về cách làm việc với phần mô tả hợp đồng dựa trên dự án.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 22e8ff927c5ff6c3748a35031e7703e3fcfe0dab
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369942"
---
# <a name="project-based-contract-lines-overview"></a><span data-ttu-id="58209-103">Tổng quan về mô tả hợp đồng dựa trên dự án</span><span class="sxs-lookup"><span data-stu-id="58209-103">Project-based contract lines overview</span></span>

<span data-ttu-id="58209-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="58209-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="58209-105">Mô tả hợp đồng theo dự án trong Dynamics 365 Project Operations được thiết kế để ghi lại ước tính và thỏa thuận thanh toán cho các thành phần cụ thể của dự án theo cam kết.</span><span class="sxs-lookup"><span data-stu-id="58209-105">Project-based contract lines in Dynamics 365 Project Operations are designed to hold the estimate and billing agreements for specific components of project work on an engagement.</span></span> <span data-ttu-id="58209-106">Cấu trúc của phần mô tả hợp đồng dựa trên dự án được mở rộng cho các ước tính và kịch bản thanh toán của dự án với các khái niệm sau:</span><span class="sxs-lookup"><span data-stu-id="58209-106">The structure of a project–based contract line is extended for project estimates and billing scenarios with the following concepts:</span></span>

- <span data-ttu-id="58209-107">Phương thức thanh toán</span><span class="sxs-lookup"><span data-stu-id="58209-107">Billing method</span></span>
- <span data-ttu-id="58209-108">Ánh xạ dự án và nhiệm vụ</span><span class="sxs-lookup"><span data-stu-id="58209-108">Project and task mapping</span></span>
- <span data-ttu-id="58209-109">Các lớp giao dịch được bao gồm</span><span class="sxs-lookup"><span data-stu-id="58209-109">Included transaction classes</span></span>
- <span data-ttu-id="58209-110">Giới hạn không vượt quá</span><span class="sxs-lookup"><span data-stu-id="58209-110">Not-to-exceed limit</span></span>
- <span data-ttu-id="58209-111">Thiết lập khả năng tính phí</span><span class="sxs-lookup"><span data-stu-id="58209-111">Chargeability setup</span></span>
- <span data-ttu-id="58209-112">Các ước tính dựa trên chi tiết mô tả hợp đồng</span><span class="sxs-lookup"><span data-stu-id="58209-112">Estimates using contract line details</span></span>
- <span data-ttu-id="58209-113">Khách hàng trong phần mô tả hợp đồng</span><span class="sxs-lookup"><span data-stu-id="58209-113">Contract line customers</span></span>

<span data-ttu-id="58209-114">Bảng sau bao gồm các trường trên tab **Chung** của phần mô tả hợp đồng dựa trên dự án giúp thiết lập cơ sở cho số liệu ước tính chi tiết, cơ bản và sắp xếp thanh toán cho công việc theo dự án.</span><span class="sxs-lookup"><span data-stu-id="58209-114">The following table includes the fields on the **General** tab of project–based contract lines that help set up the basis for a detailed, ground–up estimate and billing arrangements for project–based work.</span></span>

| <span data-ttu-id="58209-115">Trường</span><span class="sxs-lookup"><span data-stu-id="58209-115">Field</span></span> | <span data-ttu-id="58209-116">Nội dung mô tả</span><span class="sxs-lookup"><span data-stu-id="58209-116">Description</span></span> | <span data-ttu-id="58209-117">Tác động xuôi tuyến</span><span class="sxs-lookup"><span data-stu-id="58209-117">Downstream impact</span></span> |
| --- | --- | --- |
| <span data-ttu-id="58209-118">**Tên**</span><span class="sxs-lookup"><span data-stu-id="58209-118">**Name**</span></span> | <span data-ttu-id="58209-119">Tên phần mô tả hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="58209-119">Name of the contract line.</span></span> <span data-ttu-id="58209-120">Tên này xác định thành phần riêng biệt của hợp đồng đang được ước tính.</span><span class="sxs-lookup"><span data-stu-id="58209-120">This identifies the discrete component of the contract that is being estimated.</span></span> <span data-ttu-id="58209-121">Đối với hợp đồng dự án tạo từ báo giá, giá trị này sẽ được sao chép từ giá trị tương ứng của phần mô tả báo giá dựa trên dự án.</span><span class="sxs-lookup"><span data-stu-id="58209-121">For a project contract created from a quote, this value is copied from a corresponding value of the project-based quote line.</span></span> | <span data-ttu-id="58209-122">Tên được sao chép sang phần mô tả hóa đơn dự án được tạo từ phần mô tả hợp đồng này khi tạo hóa đơn.</span><span class="sxs-lookup"><span data-stu-id="58209-122">The name copied over to the project invoice line that is created from this contract line when the invoice is created.</span></span> |
| <span data-ttu-id="58209-123">**Phương thức Thanh toán**</span><span class="sxs-lookup"><span data-stu-id="58209-123">**Billing Method**</span></span> | <span data-ttu-id="58209-124">Đối với hợp đồng dự án tạo từ báo giá, giá trị này sẽ được sao chép từ trường tương ứng trên phần mô tả báo giá.</span><span class="sxs-lookup"><span data-stu-id="58209-124">On a project contract created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="58209-125">Dưới đây là bộ tùy chọn đại diện cho 2 mô hình hợp đồng chính được Project Operations hỗ trợ:</span><span class="sxs-lookup"><span data-stu-id="58209-125">This is an option set that represents the two main contracting models supported by Project Operations:</span></span></br><span data-ttu-id="58209-126">- **Giá cố định**</span><span class="sxs-lookup"><span data-stu-id="58209-126">- **Fixed Price**</span></span></br><span data-ttu-id="58209-127">- **Thời gian và Vật tư**</span><span class="sxs-lookup"><span data-stu-id="58209-127">- **Time and Material**</span></span> | <span data-ttu-id="58209-128">Dựa trên phương thức thanh toán được tham chiếu trong phần mô tả hợp đồng, giao dịch thực tế sẽ được xử lý.</span><span class="sxs-lookup"><span data-stu-id="58209-128">Based on the billing method of the referenced contract line, the actual transaction will be processed.</span></span> <span data-ttu-id="58209-129">Nếu phần mô tả hợp đồng tham chiếu theo giao dịch thực tế có phương thức thanh toán theo thời gian và vật tư, thì các hồ sơ chi phí và doanh số bán hàng thực tế chưa thanh toán sẽ được tạo.</span><span class="sxs-lookup"><span data-stu-id="58209-129">If the contract line referenced by the actual has a time and material billing method, cost and unbilled sales actual records are created.</span></span> <span data-ttu-id="58209-130">Nếu phần mô tả hợp đồng tham chiếu theo giao dịch thực tế có phương thức thanh toán theo giá cố định, thì chỉ một hồ sơ chi phí thực tế được tạo.</span><span class="sxs-lookup"><span data-stu-id="58209-130">If the contract line referenced by the actual has a fixed price billing method, only a cost actual is created.</span></span> |
| <span data-ttu-id="58209-131">**Dự án**</span><span class="sxs-lookup"><span data-stu-id="58209-131">**Project**</span></span> | <span data-ttu-id="58209-132">Sử dụng trường này để xác định dự án sẽ dùng để thực hiện công việc theo cam kết này.</span><span class="sxs-lookup"><span data-stu-id="58209-132">Use this field to identify the project that will be used to deliver the work on this engagement.</span></span> | <span data-ttu-id="58209-133">Giá trị này sẽ được sử dụng cùng với **Nhiệm vụ được đưa vào** và **Các loại giao dịch được đưa vào** để giải quyết tham chiếu mô tả hợp đồng trên bản ghi dòng giá trị thực tế hoặc ước tính.</span><span class="sxs-lookup"><span data-stu-id="58209-133">This value will be used in conjunction with **Included Tasks** and **Included Transaction Classes** to resolve the contract line reference on an actual or estimate line record.</span></span> |
| <span data-ttu-id="58209-134">**Các tác vụ được đưa vào**</span><span class="sxs-lookup"><span data-stu-id="58209-134">**Included Tasks**</span></span> | <span data-ttu-id="58209-135">Cho biết liệu phần mô tả hợp đồng này có bao gồm tất cả các nhiệm vụ dự án của dự án đã chọn hay chỉ một tập hợp con các nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="58209-135">Indicates if this contract line includes all project tasks for the selected project or only a subset of the tasks.</span></span> <span data-ttu-id="58209-136">Đây là một bộ tùy chọn có các giá trị có thể có sau đây:</span><span class="sxs-lookup"><span data-stu-id="58209-136">This is an option set that has the following possible values:</span></span></br><span data-ttu-id="58209-137">- **Tất cả Nhiệm vụ Dự án**</span><span class="sxs-lookup"><span data-stu-id="58209-137">- **All Project Tasks**</span></span></br><span data-ttu-id="58209-138">- **Chỉ các nhiệm vụ dự án đã chọn**.</span><span class="sxs-lookup"><span data-stu-id="58209-138">- **Selected Project Tasks Only**.</span></span> <span data-ttu-id="58209-139">Giá trị trống trong trường này tương đương với việc chọn **Tất cả nhiệm vụ dự án**.</span><span class="sxs-lookup"><span data-stu-id="58209-139">A blank value in this field is equal to selecting **All Project Tasks**.</span></span> | <span data-ttu-id="58209-140">Nếu **Chỉ các nhiệm vụ đã chọn** được lựa chọn, thì bạn có thể chọn các nhiệm vụ cụ thể và liên kết các nhiệm vụ đó với phần mô tả hợp đồng này trên tab **Thiết lập thanh toán theo nhiệm vụ** của trang **Dự án**.</span><span class="sxs-lookup"><span data-stu-id="58209-140">If **Selected Tasks Only** is selected, you can select specific tasks and associate them to this contract line on the **Task Billing Setup** tab on the **Project** page.</span></span> <span data-ttu-id="58209-141">Giá trị nói trên sẽ được sử dụng cùng với các **Dự án** và các lớp **Giao dịch được bao gồm** để xử lý việc tham chiếu phần mô tả hợp đồng cho hồ sơ mô tả số liệu ước tính hoặc thực tế.</span><span class="sxs-lookup"><span data-stu-id="58209-141">The value will be used in conjunction with **Project** and **Included Transaction** classes to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="58209-142">**Bao gồm Thời gian**</span><span class="sxs-lookup"><span data-stu-id="58209-142">**Include Time**</span></span> | <span data-ttu-id="58209-143">Giá trị **Có**/**Không** cho biết liệu các giao dịch thời gian hoặc chi phí nhân công của dự án đã chọn có được đưa vào mục mô tả hợp đồng này hay không.</span><span class="sxs-lookup"><span data-stu-id="58209-143">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="58209-144">Giá trị **Không** chỉ ra rằng các giao dịch theo thời gian hoặc chi phí lao động sẽ không được đưa vào phần mô tả hợp đồng này.</span><span class="sxs-lookup"><span data-stu-id="58209-144">A **No** value indicates that the time transactions or labor cost will not be included on this contract line.</span></span> <span data-ttu-id="58209-145">Giá trị **Có** chỉ ra điều ngược lại.</span><span class="sxs-lookup"><span data-stu-id="58209-145">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="58209-146">Giá trị này được dùng cùng với dự án để giải quyết tham chiếu mô tả hợp đồng trên bản ghi dòng giá trị thực tế hoặc ước tính.</span><span class="sxs-lookup"><span data-stu-id="58209-146">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="58209-147">**Bao gồm Chi phí**</span><span class="sxs-lookup"><span data-stu-id="58209-147">**Include Expense**</span></span> | <span data-ttu-id="58209-148">Giá trị **Có**/**Không** cho biết liệu các chi phí của dự án đã chọn có được đưa vào mục mô tả hợp đồng này hay không.</span><span class="sxs-lookup"><span data-stu-id="58209-148">A **Yes**/**No** value indicates if expense costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="58209-149">Giá trị **Không** chỉ ra rằng các chi phí sẽ không được đưa vào phần mô tả hợp đồng này.</span><span class="sxs-lookup"><span data-stu-id="58209-149">A **No** value indicates that the expense cost will not be included on this contract line.</span></span> <span data-ttu-id="58209-150">Giá trị **Có** chỉ ra điều ngược lại.</span><span class="sxs-lookup"><span data-stu-id="58209-150">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="58209-151">Giá trị này được dùng cùng với dự án để giải quyết tham chiếu mô tả hợp đồng trên bản ghi dòng giá trị thực tế hoặc ước tính.</span><span class="sxs-lookup"><span data-stu-id="58209-151">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="58209-152">**Bao gồm vật tư**</span><span class="sxs-lookup"><span data-stu-id="58209-152">**Include Materials**</span></span> | <span data-ttu-id="58209-153">Giá trị **Có**/**Không** cho biết liệu các chi phí vật tư của dự án đã chọn có được đưa vào mục mô tả hợp đồng này hay không.</span><span class="sxs-lookup"><span data-stu-id="58209-153">A **Yes**/**No** value indicates if material costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="58209-154">Giá trị **Không** cho biết các chi phí vật tư sẽ không được đưa vào mục mô tả hợp đồng này.</span><span class="sxs-lookup"><span data-stu-id="58209-154">A **No** value indicates that the material costs will not be included on this contract line.</span></span> <span data-ttu-id="58209-155">Giá trị **Có** chỉ ra điều ngược lại.</span><span class="sxs-lookup"><span data-stu-id="58209-155">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="58209-156">Giá trị này được dùng cùng với dự án để giải quyết tham chiếu mô tả hợp đồng trên bản ghi dòng giá trị thực tế hoặc ước tính.</span><span class="sxs-lookup"><span data-stu-id="58209-156">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="58209-157">**Bao gồm Phí**</span><span class="sxs-lookup"><span data-stu-id="58209-157">**Include Fee**</span></span> | <span data-ttu-id="58209-158">Giá trị **Có**/**Không** cho biết liệu các khoản phí của dự án đã chọn có được đưa vào mục mô tả hợp đồng này hay không.</span><span class="sxs-lookup"><span data-stu-id="58209-158">A **Yes**/**No** value indicates if fees on the selected project will be included on this contract line.</span></span> <span data-ttu-id="58209-159">Giá trị **Không** chỉ ra rằng các khoản phí sẽ không được đưa vào phần mô tả hợp đồng này.</span><span class="sxs-lookup"><span data-stu-id="58209-159">A **No** value indicates that the fees will not be included on this contract line.</span></span> <span data-ttu-id="58209-160">Giá trị **Có** chỉ ra điều ngược lại.</span><span class="sxs-lookup"><span data-stu-id="58209-160">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="58209-161">Giá trị này được dùng cùng với dự án để giải quyết tham chiếu mô tả hợp đồng trên bản ghi dòng giá trị thực tế hoặc ước tính.</span><span class="sxs-lookup"><span data-stu-id="58209-161">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="58209-162">**Số tiền Theo hợp đồng**</span><span class="sxs-lookup"><span data-stu-id="58209-162">**Contracted Amount**</span></span> | <span data-ttu-id="58209-163">Đối với phần mô tả hợp đồng có giá cố định, số tiền này là giá trị đã thỏa thuận mà khách hàng sẽ được lập hóa đơn cho tất cả các thành phần công việc liên quan đến phần mô tả hợp đồng này.</span><span class="sxs-lookup"><span data-stu-id="58209-163">On a fixed price contract line, this amount is the agreed-on value that will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="58209-164">Đối với phần mô tả hợp đồng vật tư và thời gian, số tiền này là giá trị ước tính của số tiền mà khách hàng sẽ được lập hóa đơn cho tất cả các thành phần công việc liên quan đến phần mô tả hợp đồng này.</span><span class="sxs-lookup"><span data-stu-id="58209-164">On a time and material contract line, this amount is an estimated value of what will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="58209-165">Đối với hợp đồng dự án tạo từ báo giá, giá trị này sẽ được sao chép từ trường tương ứng trên phần mô tả báo giá.</span><span class="sxs-lookup"><span data-stu-id="58209-165">On a project contract that is created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="58209-166">Khi phần mô tả hợp đồng dựa trên dự án có các chi tiết mô tả, bạn sẽ không chỉnh sửa được trường này. Ngoài ra, trường này có nội dung được tóm tắt dựa trên số tiền có trong các chi tiết mô tả hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="58209-166">When a project–based contract line has line details, this field is locked for editing and is summarized from the amount on the contract line details.</span></span> | <span data-ttu-id="58209-167">Khi phần mô tả hợp đồng có các chi tiết mô tả, giá trị này có thể được sửa đổi bằng cách thay đổi số tiền có trong các chi tiết mô tả.</span><span class="sxs-lookup"><span data-stu-id="58209-167">When the contract line has line details, this value can be modified by changing the amounts on the line details.</span></span> <span data-ttu-id="58209-168">Đối với phần mô tả hợp đồng có giá cố định, giá trị này dùng để đưa ra số tiền trước thuế cho các mốc thanh toán định kỳ.</span><span class="sxs-lookup"><span data-stu-id="58209-168">On a fixed price contract line, this value is used to generate the amount before tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="58209-169">**Thuế Ước tính**</span><span class="sxs-lookup"><span data-stu-id="58209-169">**Estimated Tax**</span></span> | <span data-ttu-id="58209-170">Người dùng có thể chỉnh sửa trường này để nhập số tiền thuế ước tính trên phần mô tả hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="58209-170">The user can edit this field to input the estimated tax amount on the contract line.</span></span> <span data-ttu-id="58209-171">Khi phần mô tả hợp đồng dựa trên dự án có các chi tiết mô tả, bạn sẽ không chỉnh sửa được trường này. Ngoài ra, trường này có nội dung được tóm tắt dựa trên số tiền thuế có trong các chi tiết mô tả hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="58209-171">When a project–based contract line has line details, this field is locked for editing and is summarized from the tax amount on the contract line details.</span></span> | <span data-ttu-id="58209-172">Khi phần mô tả hợp đồng có các chi tiết mô tả, giá trị này có thể được sửa đổi bằng cách thay đổi số tiền thuế có trong các chi tiết mô tả.</span><span class="sxs-lookup"><span data-stu-id="58209-172">When the contract line has line details, this value can be modified by changing the tax amounts on the line details.</span></span> <span data-ttu-id="58209-173">Đối với phần mô tả hợp đồng có giá cố định, giá trị này dùng để đưa ra khoản thuế cho các mốc thanh toán định kỳ.</span><span class="sxs-lookup"><span data-stu-id="58209-173">On a fixed price contract line, this value is used to generate the tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="58209-174">**Số tiền sau thuế theo hợp đồng**</span><span class="sxs-lookup"><span data-stu-id="58209-174">**Contracted Amount after Tax**</span></span> | <span data-ttu-id="58209-175">Số tiền sau thuế theo phần mô tả hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="58209-175">The contract line amount after tax.</span></span> <span data-ttu-id="58209-176">Trường này là trường chỉ đọc và được tính bằng công thức **Số tiền theo hợp đồng + Thuế**.</span><span class="sxs-lookup"><span data-stu-id="58209-176">This field is read only and is calculated as **Contracted Amount + Tax**.</span></span> | <span data-ttu-id="58209-177">Đối với phần mô tả hợp đồng có giá cố định, giá trị này dùng để đưa ra các mốc thanh toán định kỳ.</span><span class="sxs-lookup"><span data-stu-id="58209-177">On a fixed price contract line, this value is used to generate periodic billing milestones.</span></span> |
| <span data-ttu-id="58209-178">**Giới hạn không vượt quá**</span><span class="sxs-lookup"><span data-stu-id="58209-178">**Not-to-Exceed Limit**</span></span> | <span data-ttu-id="58209-179">Người dùng có thể chỉnh sửa trường này và đây là trường chỉ có trong phần mô tả hợp đồng dựa trên dự án có phương thức thanh toán được đặt là theo thời gian và vật tư.</span><span class="sxs-lookup"><span data-stu-id="58209-179">The user can edit this field and it is only available on project-based contract lines that have the billing method set as time and material.</span></span> | <span data-ttu-id="58209-180">Người dùng có thể chỉnh sửa trường này.</span><span class="sxs-lookup"><span data-stu-id="58209-180">The user can edit this field.</span></span> <span data-ttu-id="58209-181">Khi số liệu thực tế về thời gian và vật tư tham chiếu đến phần mô tả hợp đồng theo thời gian và vật tư này, số tiền thực tế được đánh giá theo giới hạn không vượt quá trên phần mô tả hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="58209-181">When an actual for time and material references this contract line for time and material, the amount on the actual is evaluated against the not-to-exceed limit on the contract line.</span></span> <span data-ttu-id="58209-182">Việc đánh giá này được hoàn thành sau khi các khoản đã chi và đã cam kết được hạch toán.</span><span class="sxs-lookup"><span data-stu-id="58209-182">This evaluation is completed after  the already spent and committed amounts are accounted for.</span></span> |
| <span data-ttu-id="58209-183">**Ngân sách Khách hàng**</span><span class="sxs-lookup"><span data-stu-id="58209-183">**Customer Budget**</span></span> | <span data-ttu-id="58209-184">Đây là trường có thể chỉnh sửa và được sao chép từ trường tương ứng trên phần mô tả báo giá nếu hợp đồng được tạo từ một báo giá.</span><span class="sxs-lookup"><span data-stu-id="58209-184">This field is editable and is copied from the corresponding field on the quote line if the contract was created from a quote.</span></span> | <span data-ttu-id="58209-185">Trường này chỉ dùng để cung cấp thông tin và không có bất kỳ ý nghĩa nào theo đó.</span><span class="sxs-lookup"><span data-stu-id="58209-185">This field is only used for information and does not have any downstream significance.</span></span> |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a><span data-ttu-id="58209-186">Quy tắc xác thực cho các tùy chọn trên tab Chung của phần mô tả hợp đồng dựa trên dự án</span><span class="sxs-lookup"><span data-stu-id="58209-186">Validation rules for the options on the General tab of project-based contract lines</span></span>

<span data-ttu-id="58209-187">Quy tắc 1: Nếu trường **Các nhiệm vụ được đưa vào** bị để trống hoặc được đặt thành **Tất cả nhiệm vụ dự án**, thì tất cả các nhiệm vụ của dự án được bao gồm trong phần mô tả hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="58209-187">Rule 1: If the **Included Tasks** field is blank or set to **All Project Tasks**, all tasks of the project are included on the contract line.</span></span>

<span data-ttu-id="58209-188">Quy tắc 2: Khi trường **Các nhiệm vụ được đưa vào** bị để trống hoặc được đặt rõ ràng thành **Tất cả nhiệm vụ dự án**, thì một dự án và một lớp giao dịch nhất định chỉ có thể được đưa vào một phần mô tả hợp đồng dựa trên dự án của một hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="58209-188">Rule 2: When the **Included Tasks** field is blank or explicitly set to **All Project Tasks**, a project and a certain transaction class can only be included on one project-based contract line of a contract.</span></span>

<span data-ttu-id="58209-189">Quy tắc 3: Khi trường **Các nhiệm vụ được đưa vào** được đặt thành **Chỉ các nhiệm vụ dự án đã chọn**, thì một dự án và một lớp giao dịch nhất định có thể được đưa vào nhiều phần mô tả hợp đồng dựa trên dự án của một hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="58209-189">Rule 3: When the **Included Tasks** field is set to **Selected Project Tasks Only**, a project and a certain transaction class can be included on multiple project-based contract lines of a contract.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p><span data-ttu-id="58209-190">
                    <strong>Hợp đồng</strong>
                </span><span class="sxs-lookup"><span data-stu-id="58209-190">
                    <strong>Contract</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="58209-191">
                    <strong>Mô tả hợp đồng</strong>
                </span><span class="sxs-lookup"><span data-stu-id="58209-191">
                    <strong>Contract line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="58209-192">
                    <strong>Dự án</strong>
                </span><span class="sxs-lookup"><span data-stu-id="58209-192">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="67" valign="top">
                <p><span data-ttu-id="58209-193">
                    <strong>Các tác vụ được đưa vào</strong>
                </span><span class="sxs-lookup"><span data-stu-id="58209-193">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="58209-194">
                    <strong>Bao gồm Thời gian</strong>
                </span><span class="sxs-lookup"><span data-stu-id="58209-194">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="58209-195">
                    <strong>Bao gồm Chi phí</strong>
                </span><span class="sxs-lookup"><span data-stu-id="58209-195">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="58209-196">
                    <strong>Bao gồm vật tư</strong>
                </span><span class="sxs-lookup"><span data-stu-id="58209-196">
                    <strong>Include Materials</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="58209-197">
                    <strong>Bao gồm</strong>
                </span><span class="sxs-lookup"><span data-stu-id="58209-197">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="58209-198">
                    <strong>Phí</strong>
                </span><span class="sxs-lookup"><span data-stu-id="58209-198">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="53" valign="top">
                <p><span data-ttu-id="58209-199">
                    <strong>Hợp lệ/Không hợp lệ</strong>
                </span><span class="sxs-lookup"><span data-stu-id="58209-199">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="250" valign="top">
                <p><span data-ttu-id="58209-200">
                    <strong>Lý do</strong>
                </span><span class="sxs-lookup"><span data-stu-id="58209-200">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="58209-201">C1</span><span class="sxs-lookup"><span data-stu-id="58209-201">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="58209-202">CL1</span><span class="sxs-lookup"><span data-stu-id="58209-202">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="58209-203">Kỳ 1</span><span class="sxs-lookup"><span data-stu-id="58209-203">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="58209-204">Trống</span><span class="sxs-lookup"><span data-stu-id="58209-204">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="58209-205">Có</span><span class="sxs-lookup"><span data-stu-id="58209-205">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="58209-206">Có</span><span class="sxs-lookup"><span data-stu-id="58209-206">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="58209-207">Có</span><span class="sxs-lookup"><span data-stu-id="58209-207">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="58209-208">Có</span><span class="sxs-lookup"><span data-stu-id="58209-208">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="58209-209">Không hợp lệ</span><span class="sxs-lookup"><span data-stu-id="58209-209">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="58209-210">Vi phạm Quy tắc số 2.</span><span class="sxs-lookup"><span data-stu-id="58209-210">Violation of Rule #2.</span></span> <span data-ttu-id="58209-211">Thời gian, Chi phí, Vật tư và Phí cho dự án P1 được thêm vào cả hai mục Mô tả hợp đồng CL1 và CL2.</span><span class="sxs-lookup"><span data-stu-id="58209-211">Time, Expense, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="58209-212">C1</span><span class="sxs-lookup"><span data-stu-id="58209-212">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="58209-213">CL2</span><span class="sxs-lookup"><span data-stu-id="58209-213">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="58209-214">Kỳ 1</span><span class="sxs-lookup"><span data-stu-id="58209-214">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="58209-215">Trống</span><span class="sxs-lookup"><span data-stu-id="58209-215">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="58209-216">Có</span><span class="sxs-lookup"><span data-stu-id="58209-216">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="58209-217">Có</span><span class="sxs-lookup"><span data-stu-id="58209-217">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="58209-218">Có</span><span class="sxs-lookup"><span data-stu-id="58209-218">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="58209-219">Có</span><span class="sxs-lookup"><span data-stu-id="58209-219">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="58209-220">C1</span><span class="sxs-lookup"><span data-stu-id="58209-220">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="58209-221">CL1</span><span class="sxs-lookup"><span data-stu-id="58209-221">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="58209-222">Kỳ 1</span><span class="sxs-lookup"><span data-stu-id="58209-222">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="58209-223">Trống</span><span class="sxs-lookup"><span data-stu-id="58209-223">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="58209-224">Có</span><span class="sxs-lookup"><span data-stu-id="58209-224">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="58209-225">No</span><span class="sxs-lookup"><span data-stu-id="58209-225">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="58209-226">Có</span><span class="sxs-lookup"><span data-stu-id="58209-226">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="58209-227">Có</span><span class="sxs-lookup"><span data-stu-id="58209-227">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="58209-228">Không hợp lệ</span><span class="sxs-lookup"><span data-stu-id="58209-228">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="58209-229">Vi phạm Quy tắc số 2.</span><span class="sxs-lookup"><span data-stu-id="58209-229">Violation of Rule #2.</span></span> <span data-ttu-id="58209-230">Thời gian, Vật tư và Phí cho dự án P1 được thêm vào cả hai mục Mô tả hợp đồng CL1 và CL2.</span><span class="sxs-lookup"><span data-stu-id="58209-230">Time, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="58209-231">C1</span><span class="sxs-lookup"><span data-stu-id="58209-231">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="58209-232">CL2</span><span class="sxs-lookup"><span data-stu-id="58209-232">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="58209-233">Kỳ 1</span><span class="sxs-lookup"><span data-stu-id="58209-233">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="58209-234">Trống</span><span class="sxs-lookup"><span data-stu-id="58209-234">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="58209-235">Có</span><span class="sxs-lookup"><span data-stu-id="58209-235">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="58209-236">Có</span><span class="sxs-lookup"><span data-stu-id="58209-236">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="58209-237">Có</span><span class="sxs-lookup"><span data-stu-id="58209-237">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="58209-238">Có</span><span class="sxs-lookup"><span data-stu-id="58209-238">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="58209-239">C1</span><span class="sxs-lookup"><span data-stu-id="58209-239">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="58209-240">CL1</span><span class="sxs-lookup"><span data-stu-id="58209-240">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="58209-241">Kỳ 1</span><span class="sxs-lookup"><span data-stu-id="58209-241">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="58209-242">Trống</span><span class="sxs-lookup"><span data-stu-id="58209-242">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="58209-243">Có</span><span class="sxs-lookup"><span data-stu-id="58209-243">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="58209-244">No</span><span class="sxs-lookup"><span data-stu-id="58209-244">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="58209-245">Có</span><span class="sxs-lookup"><span data-stu-id="58209-245">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="58209-246">Có</span><span class="sxs-lookup"><span data-stu-id="58209-246">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="58209-247">Hợp lệ</span><span class="sxs-lookup"><span data-stu-id="58209-247">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="58209-248">Thời gian, Vật tư và Phí cho dự án P1 được thêm vào CL1.</span><span class="sxs-lookup"><span data-stu-id="58209-248">Time, Materials, and Fees on P1 project are included on CL1.</span></span>
                </p>
                <ul>
                    <li>
<span data-ttu-id="58209-249">Chi phí trên dự án P1 được bao gồm trên CL2.</span><span class="sxs-lookup"><span data-stu-id="58209-249">Expense on P1 project is included on CL2.</span></span>
                    </li>
                </ul>
                <p>
<span data-ttu-id="58209-250">Những nội dung được thêm vào mỗi mục Mô tả hợp đồng là hợp lệ do không bị trùng lặp.</span><span class="sxs-lookup"><span data-stu-id="58209-250">No overlap in what is being included on each Contract line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="58209-251">C1</span><span class="sxs-lookup"><span data-stu-id="58209-251">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="58209-252">CL2</span><span class="sxs-lookup"><span data-stu-id="58209-252">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="58209-253">Kỳ 1</span><span class="sxs-lookup"><span data-stu-id="58209-253">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="58209-254">Trống</span><span class="sxs-lookup"><span data-stu-id="58209-254">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="58209-255">No</span><span class="sxs-lookup"><span data-stu-id="58209-255">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="58209-256">Có</span><span class="sxs-lookup"><span data-stu-id="58209-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="58209-257">No</span><span class="sxs-lookup"><span data-stu-id="58209-257">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="58209-258">No</span><span class="sxs-lookup"><span data-stu-id="58209-258">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="58209-259">C1</span><span class="sxs-lookup"><span data-stu-id="58209-259">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="58209-260">CL1</span><span class="sxs-lookup"><span data-stu-id="58209-260">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="58209-261">Kỳ 1</span><span class="sxs-lookup"><span data-stu-id="58209-261">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="58209-262">Chỉ các tác vụ được chọn</span><span class="sxs-lookup"><span data-stu-id="58209-262">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="58209-263">Có</span><span class="sxs-lookup"><span data-stu-id="58209-263">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="58209-264">Có</span><span class="sxs-lookup"><span data-stu-id="58209-264">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="58209-265">Có</span><span class="sxs-lookup"><span data-stu-id="58209-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="58209-266">Có</span><span class="sxs-lookup"><span data-stu-id="58209-266">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="58209-267">Không hợp lệ</span><span class="sxs-lookup"><span data-stu-id="58209-267">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="58209-268">Vi phạm quy tắc số 2</span><span class="sxs-lookup"><span data-stu-id="58209-268">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="58209-269">C1 bao gồm Thời gian, Vật tư, Chi phí và Phí cho một tập hợp con các nhiệm vụ trong dự án P1.</span><span class="sxs-lookup"><span data-stu-id="58209-269">C1 includes Time, Materials, Expenses and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="58209-270">CL2 bao gồm Thời gian, Vật tư, Chi phí và Phí cho toàn bộ dự án P1 và do đó trùng lặp với những nội dung được thêm vào C1.</span><span class="sxs-lookup"><span data-stu-id="58209-270">CL2 includes Time, Materials, Expenses and Fees for the whole project P1 and therefore overlaps with what is included on C1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="58209-271">C1</span><span class="sxs-lookup"><span data-stu-id="58209-271">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="58209-272">CL2</span><span class="sxs-lookup"><span data-stu-id="58209-272">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="58209-273">Kỳ 1</span><span class="sxs-lookup"><span data-stu-id="58209-273">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="58209-274">Trống</span><span class="sxs-lookup"><span data-stu-id="58209-274">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="58209-275">Có</span><span class="sxs-lookup"><span data-stu-id="58209-275">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="58209-276">Có</span><span class="sxs-lookup"><span data-stu-id="58209-276">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="58209-277">Có</span><span class="sxs-lookup"><span data-stu-id="58209-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="58209-278">Có</span><span class="sxs-lookup"><span data-stu-id="58209-278">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="58209-279">C1</span><span class="sxs-lookup"><span data-stu-id="58209-279">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="58209-280">CL1</span><span class="sxs-lookup"><span data-stu-id="58209-280">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="58209-281">Kỳ 1</span><span class="sxs-lookup"><span data-stu-id="58209-281">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="58209-282">Chỉ các tác vụ được chọn</span><span class="sxs-lookup"><span data-stu-id="58209-282">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="58209-283">Có</span><span class="sxs-lookup"><span data-stu-id="58209-283">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="58209-284">Có</span><span class="sxs-lookup"><span data-stu-id="58209-284">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="58209-285">Có</span><span class="sxs-lookup"><span data-stu-id="58209-285">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="58209-286">Có</span><span class="sxs-lookup"><span data-stu-id="58209-286">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="58209-287">Hợp lệ</span><span class="sxs-lookup"><span data-stu-id="58209-287">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="58209-288">Theo quy tắc số 3</span><span class="sxs-lookup"><span data-stu-id="58209-288">Per Rule #3</span></span> </p>
                <p>
<span data-ttu-id="58209-289">C1 bao gồm Thời gian, Chi phí, Vật tư, Chi phí và Phí cho một tập hợp con các nhiệm vụ trong dự án P1.</span><span class="sxs-lookup"><span data-stu-id="58209-289">C1 includes Time, Expenses, Materials, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="58209-290">CL2 bao gồm Thời gian, Chi phí, Vật tư, Chi phí và Phí cho một tập hợp con các nhiệm vụ trong dự án P1.</span><span class="sxs-lookup"><span data-stu-id="58209-290">CL2 includes Time, Expenses, Materials, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="58209-291">Bước xác thực bổ sung duy nhất xoay quanh việc tập hợp con các nhiệm vụ trên CL1 khác với tập hợp con các nhiệm vụ trên CL2 để đảm bảo rằng không có sự trùng lặp ở đó.</span><span class="sxs-lookup"><span data-stu-id="58209-291">The only additional validation is around the subset of tasks on CL1 is different from the subset of tasks on CL2 to ensure that there are no overlaps there.</span></span> <span data-ttu-id="58209-292">Điều này được hệ thống thực hiện khi các nhiệm vụ được liên kết.</span><span class="sxs-lookup"><span data-stu-id="58209-292">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="58209-293">C1</span><span class="sxs-lookup"><span data-stu-id="58209-293">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="58209-294">CL2</span><span class="sxs-lookup"><span data-stu-id="58209-294">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="58209-295">Kỳ 1</span><span class="sxs-lookup"><span data-stu-id="58209-295">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="58209-296">Chỉ các tác vụ được chọn</span><span class="sxs-lookup"><span data-stu-id="58209-296">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="58209-297">Có</span><span class="sxs-lookup"><span data-stu-id="58209-297">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="58209-298">Có</span><span class="sxs-lookup"><span data-stu-id="58209-298">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="58209-299">Có</span><span class="sxs-lookup"><span data-stu-id="58209-299">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="58209-300">Có</span><span class="sxs-lookup"><span data-stu-id="58209-300">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
