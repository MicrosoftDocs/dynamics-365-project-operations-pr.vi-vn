---
title: Truy vấn về Lịch trình chi tiêu của Giải thưởng Liên bang
description: Chủ đề này cung cấp thông tin về truy vấn Lịch trình chi tiêu của Giải thưởng Liên bang.
author: velofog
manager: Ann Beebe
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: eaf523ab147cbe974fed6e7eab21967404583fe6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087092"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="b6a82-103">Truy vấn về Lịch trình chi tiêu của Giải thưởng Liên bang</span><span class="sxs-lookup"><span data-stu-id="b6a82-103">Schedule of Expenditures of Federal Awards inquiry</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b6a82-104">Theo Thông tư A-133 của Văn phòng Quản lý và Ngân sách, các cơ quan nhận quỹ liên bang phải tuân theo các yêu cầu kiểm toán, còn được gọi là kiểm toán đơn lẻ.</span><span class="sxs-lookup"><span data-stu-id="b6a82-104">According to Office of Management and Budget Circular A-133, agencies that receive federal funds are subject to audit requirements, which are also known as single audits.</span></span> <span data-ttu-id="b6a82-105">Quy trình kiểm toán được sử dụng để báo cáo định kỳ các khoản thu và chi của các khoản trợ cấp liên bang.</span><span class="sxs-lookup"><span data-stu-id="b6a82-105">The audit process is used to report on the revenues and expenditures of federal grants on a recurring basis.</span></span> <span data-ttu-id="b6a82-106">Một phần của báo cáo kiểm toán đơn lẻ bao gồm Lịch trình chi tiêu của Giải thưởng Liên bang (SEFA).</span><span class="sxs-lookup"><span data-stu-id="b6a82-106">Part of the single audit report includes the Schedule of Expenditures of Federal Awards (SEFA).</span></span>

<span data-ttu-id="b6a82-107">Truy vấn Lịch trình chi tiêu của Giải thưởng Liên bang bao gồm tiêu đề và số hiệu của Sản phẩm hỗ trợ liên bang trong nước (CFDA), số hiệu trợ cấp, năm trợ cấp, tên cơ quan thuộc liên bang cung cấp tiền và tên của thực thể chuyển tiếp.</span><span class="sxs-lookup"><span data-stu-id="b6a82-107">The Schedule of Expenditures of Federal Awards inquiry includes the Catalog of Federal Domestic Assistance (CFDA) title and number, the grant number, the year of the grant, the name of the federal agency that provides the funds, and the name of the pass-through entity.</span></span> <span data-ttu-id="b6a82-108">Cuộc điều tra diễn ra trong một khoảng thời gian cụ thể.</span><span class="sxs-lookup"><span data-stu-id="b6a82-108">The inquiry is for a specific period.</span></span> <span data-ttu-id="b6a82-109">Thông thường, khoảng thời gian đó giống với kỳ báo cáo tài chính, là năm tài chính.</span><span class="sxs-lookup"><span data-stu-id="b6a82-109">Typically, that period is the same as the financial statement period, which is a fiscal year.</span></span>

<span data-ttu-id="b6a82-110">Truy vấn bao gồm các khoản trợ cấp có ngày dự kiến trong phạm vi ngày đã chọn.</span><span class="sxs-lookup"><span data-stu-id="b6a82-110">The inquiry includes grants that have projection dates in the selected date range.</span></span> <span data-ttu-id="b6a82-111">Cột **Cơ quan trợ cấp** của truy vấn hiển thị khách hàng trợ cấp hoặc đối với khoản trợ cấp chuyển tiếp, là cơ quan trợ cấp.</span><span class="sxs-lookup"><span data-stu-id="b6a82-111">The **Grantor agency** column of the inquiry shows the grant customer or, for a pass-through grant, the grantor agency.</span></span> <span data-ttu-id="b6a82-112">Đối với khoản trợ cấp chuyển tiếp, cột **Cơ quan chuyển tiếp** hiển thị khách hàng trợ cấp.</span><span class="sxs-lookup"><span data-stu-id="b6a82-112">For a pass-through grant, the **Pass-through agency** column shows the grant customer.</span></span> <span data-ttu-id="b6a82-113">Nếu khoản trợ cấp không phải là chuyển tiếp, thì cột **Cơ quan chuyển tiếp** sẽ trống.</span><span class="sxs-lookup"><span data-stu-id="b6a82-113">If the grant isn't a pass-through grant, the **Pass-through agency** column is blank.</span></span>

## <a name="set-up-the-cfda-clusters"></a><span data-ttu-id="b6a82-114">Thiết lập cụm CFDA</span><span class="sxs-lookup"><span data-stu-id="b6a82-114">Set up the CFDA clusters</span></span>

<span data-ttu-id="b6a82-115">Bạn phải thiết lập các cụm CFDA có thể được liên kết với các số CFDA trong truy vấn Lịch trình chi tiêu của Giải thưởng Liên bang.</span><span class="sxs-lookup"><span data-stu-id="b6a82-115">You must set up the CFDA clusters that can be associated with CFDA numbers in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="b6a82-116">Đi đến **Quản lý dự án và kế toán \> Thiết lập \> Khoản trợ cấp \> cụm Sản phẩm hỗ trợ liên bang trong nước**.</span><span class="sxs-lookup"><span data-stu-id="b6a82-116">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance clusters**.</span></span>
2. <span data-ttu-id="b6a82-117">Chọn **Mới** để tạo cụm CFDA.</span><span class="sxs-lookup"><span data-stu-id="b6a82-117">Select **New** to create a CFDA cluster.</span></span>
3. <span data-ttu-id="b6a82-118">Nhập tên cụm.</span><span class="sxs-lookup"><span data-stu-id="b6a82-118">Enter the cluster name.</span></span>
4. <span data-ttu-id="b6a82-119">Chọn **Lưu** để lưu thay đổi của bạn.</span><span class="sxs-lookup"><span data-stu-id="b6a82-119">Select **Save** to save your changes.</span></span>

## <a name="set-up-cfda-numbers"></a><span data-ttu-id="b6a82-120">Thiết lập cụm CFDA</span><span class="sxs-lookup"><span data-stu-id="b6a82-120">Set up CFDA numbers</span></span>

<span data-ttu-id="b6a82-121">Bạn phải thiết lập số CFDA có thể được thêm vào khoản trợ cấp và được bao gồm trong truy vấn Lịch trình chi tiêu của Giải thưởng Liên bang.</span><span class="sxs-lookup"><span data-stu-id="b6a82-121">You must set up CFDA numbers that can be added to grants and included in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="b6a82-122">Đi đến **Quản lý dự án và kế toán \> Thiết lập \> Khoản trợ cấp \> số hiệu Sản phẩm hỗ trợ liên bang trong nước**.</span><span class="sxs-lookup"><span data-stu-id="b6a82-122">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance numbers**.</span></span>
2. <span data-ttu-id="b6a82-123">Chọn **Mới** để tạo số hiệu CFDA.</span><span class="sxs-lookup"><span data-stu-id="b6a82-123">Select **New** to create a CFDA number.</span></span>
3. <span data-ttu-id="b6a82-124">Trong cột **Số hiệu** , hãy nhập số hiệu CFDA.</span><span class="sxs-lookup"><span data-stu-id="b6a82-124">In the **Number** column, enter the CFDA number.</span></span>
4. <span data-ttu-id="b6a82-125">Nhấn phím **Tab**.</span><span class="sxs-lookup"><span data-stu-id="b6a82-125">Press the **Tab** key.</span></span>
5. <span data-ttu-id="b6a82-126">Trong cột **Mô tả** , hãy nhập tiêu đề CFDA.</span><span class="sxs-lookup"><span data-stu-id="b6a82-126">In the **Description** column, enter the CFDA title.</span></span>
6. <span data-ttu-id="b6a82-127">Nhấn phím **Tab**.</span><span class="sxs-lookup"><span data-stu-id="b6a82-127">Press the **Tab** key.</span></span>
7. <span data-ttu-id="b6a82-128">Tùy chọn: Trong trường **Cụm chương trình** , thêm cụm CFDA thích hợp.</span><span class="sxs-lookup"><span data-stu-id="b6a82-128">Optional: In the **Program cluster** field, add the appropriate CFDA cluster.</span></span>
8. <span data-ttu-id="b6a82-129">Chọn **Lưu** để lưu thay đổi của bạn.</span><span class="sxs-lookup"><span data-stu-id="b6a82-129">Select **Save** to save your changes.</span></span>

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="b6a82-130">Thiết lập các khoản trợ cấp để báo cáo cho truy vấn về Lịch trình chi tiêu của Giải thưởng Liên bang</span><span class="sxs-lookup"><span data-stu-id="b6a82-130">Set up grants to report for the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="b6a82-131">Đi đến **Quản lý dự án và kế toán \> Khoản trợ cấp \> Khoản trợ cấp** và chọn một khoản trợ cấp hiện có.</span><span class="sxs-lookup"><span data-stu-id="b6a82-131">Go to **Project management and accounting \> Grants \> Grants** , and select an existing grant.</span></span>
2. <span data-ttu-id="b6a82-132">Trên FastTab **Thiết lập** , trong trường **Sản phẩm hỗ trợ liên bang trong nước** , hãy gán số hiệu CFDA.</span><span class="sxs-lookup"><span data-stu-id="b6a82-132">On the **Setup** FastTab, in the  **Catalog of Federal Domestic Assistance** field, assign the CFDA number.</span></span> <span data-ttu-id="b6a82-133">Số hiệu CFDA trên khoản trợ cấp xác định cụm CFDA để báo cáo.</span><span class="sxs-lookup"><span data-stu-id="b6a82-133">The CFDA number on the grant determines the CFDA cluster for reporting.</span></span>
3. <span data-ttu-id="b6a82-134">Trên FastTab **Thông tin liên lạc** , nhập thông tin người tài trợ bằng cách làm theo các bước sau:</span><span class="sxs-lookup"><span data-stu-id="b6a82-134">On **Contact information** FastTab, enter the grantor information by following these steps:</span></span>

    1. <span data-ttu-id="b6a82-135">Trong trường **Khách hàng trợ cấp** , nhập khách hàng chịu trách nhiệm cho khoản trợ cấp.</span><span class="sxs-lookup"><span data-stu-id="b6a82-135">In the **Grant customer** field, enter the customer who is responsible for the grant.</span></span> <span data-ttu-id="b6a82-136">Đối với một khoản trợ cấp hiện có, thông tin này có thể đã được nhập.</span><span class="sxs-lookup"><span data-stu-id="b6a82-136">For an existing grant, this information might already be entered.</span></span>
    2. <span data-ttu-id="b6a82-137">Cho biết khách hàng trợ cấp có phải là nhà tài trợ hay không.</span><span class="sxs-lookup"><span data-stu-id="b6a82-137">Indicate whether the grant customer is the funder.</span></span> <span data-ttu-id="b6a82-138">Nếu khách hàng trợ cấp là nhà tài trợ, không chọn hộp kiểm **Chuyển tiếp**.</span><span class="sxs-lookup"><span data-stu-id="b6a82-138">If the grant customer is the funder, leave the **Pass-through** check box cleared.</span></span> <span data-ttu-id="b6a82-139">Nếu khách hàng khác là nhà tài trợ và khách hàng trợ cấp chịu trách nhiệm chi tiêu và theo dõi số tiền, hãy chọn hộp kiểm **Chuyển tiếp**.</span><span class="sxs-lookup"><span data-stu-id="b6a82-139">If another customer is the funder, and the grant customer is responsible for spending and tracking the money, select the **Pass-through** check box.</span></span>

4. <span data-ttu-id="b6a82-140">Nếu bạn đã chọn hộp kiểm **Chuyển tiếp** trong bước trước đó, trong trường **Cơ quan trợ cấp** , hãy nhập khách hàng đã cung cấp khoản trợ cấp.</span><span class="sxs-lookup"><span data-stu-id="b6a82-140">If you selected the **Pass-through** check box in the previous step, in the **Grantor agency** field, enter the customer who provided the grant.</span></span> <span data-ttu-id="b6a82-141">Cơ quan trợ cấp và khách hàng trợ cấp không được là cùng một khách hàng.</span><span class="sxs-lookup"><span data-stu-id="b6a82-141">The grantor agency and the grant customer can't be the same customer.</span></span>

<span data-ttu-id="b6a82-142">Dưới đây là một ví dụ về khoản trợ cấp chuyển tiếp:</span><span class="sxs-lookup"><span data-stu-id="b6a82-142">Here is an example of a pass-through grant:</span></span>

<span data-ttu-id="b6a82-143">Chính phủ liên bang đã tài trợ một dự án cơ sở hạ tầng cho một tiểu bang.</span><span class="sxs-lookup"><span data-stu-id="b6a82-143">The federal government funded an infrastructure project for a state.</span></span> <span data-ttu-id="b6a82-144">Chính phủ liên bang đã cung cấp tiền để tiểu bang chi tiêu.</span><span class="sxs-lookup"><span data-stu-id="b6a82-144">The federal government gave the money to the state to spend.</span></span> <span data-ttu-id="b6a82-145">Trong trường hợp này, chính phủ liên bang là cơ quan trợ cấp và tiểu bang là khách hàng trợ cấp.</span><span class="sxs-lookup"><span data-stu-id="b6a82-145">In this case, the federal government is the grantor agency, and the state is the grant customer.</span></span>

> [!NOTE] 
> <span data-ttu-id="b6a82-146">Khi bạn bật tính năng này lần đầu tiên, số hiệu CFDA ban đầu sẽ được nhập bằng cách sử dụng các số hiệu hiện có trên khoản trợ cấp.</span><span class="sxs-lookup"><span data-stu-id="b6a82-146">When you first turn on the feature, initial CFDA numbers will be entered by using the existing numbers on grants.</span></span>

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a><span data-ttu-id="b6a82-147">Loại trừ các khoản trợ cấp khỏi báo cáo SEFA dựa trên loại trợ cấp</span><span class="sxs-lookup"><span data-stu-id="b6a82-147">Exclude grants from SEFA reporting based on the grant type</span></span>

1. <span data-ttu-id="b6a82-148">Đi đến **Quản lý dự án và kế toán \> Thiết lập \> Khoản trợ cấp \> Các loại trợ cấp**.</span><span class="sxs-lookup"><span data-stu-id="b6a82-148">Go to **Project management and accounting \> Setup \> Grants \> Grant types**.</span></span>
2. <span data-ttu-id="b6a82-149">Trên FastTab **Thông tin mặc định** , chọn hộp kiểm **Loại trừ khỏi Lịch trình chi tiêu của Giải thưởng Liên bang**.</span><span class="sxs-lookup"><span data-stu-id="b6a82-149">On the **Default information** FastTab, select the **Exclude from Schedule of Expenditures of Federal Awards** check box.</span></span>
3. <span data-ttu-id="b6a82-150">Chọn **Lưu** để lưu thay đổi của bạn.</span><span class="sxs-lookup"><span data-stu-id="b6a82-150">Select **Save** to save your changes.</span></span>

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="b6a82-151">Chạy truy vấn về Lịch trình chi tiêu của Giải thưởng Liên bang</span><span class="sxs-lookup"><span data-stu-id="b6a82-151">Run the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="b6a82-152">Đi đến **Quản lý dự án và kế toán \> Truy vấn và báo cáo \> Truy vấn về khoản trợ cấp \> Lịch trình chi tiêu của Giải thưởng Liên bang**.</span><span class="sxs-lookup"><span data-stu-id="b6a82-152">Go to **Project management and accounting \> Inquiries and reports \> Grant inquiry \> Schedule of Expenditures of Federal Awards**.</span></span>
2. <span data-ttu-id="b6a82-153">Trong phần **Tham số** , hãy làm theo các bước sau:</span><span class="sxs-lookup"><span data-stu-id="b6a82-153">In the **Parameters** section, follow these steps:</span></span>

    1. <span data-ttu-id="b6a82-154">Trong trường **Khoảng ngày** , chọn mã cho khoảng ngày.</span><span class="sxs-lookup"><span data-stu-id="b6a82-154">In the **Date interval** field, select the code for the date interval.</span></span> <span data-ttu-id="b6a82-155">Hoặc, trong các trường **Từ ngày** và **Đến ngày** , hãy xác định khoảng ngày.</span><span class="sxs-lookup"><span data-stu-id="b6a82-155">Alternatively, in the **From date** and **To date** fields, define the date interval.</span></span>
    2. <span data-ttu-id="b6a82-156">Tùy chọn: Để chỉ bao gồm các giao dịch đã lập hóa đơn dưới dạng doanh thu trong truy vấn, hãy đặt tùy chọn **Chỉ bao gồm doanh thu đã lập hóa đơn** thành **Có**.</span><span class="sxs-lookup"><span data-stu-id="b6a82-156">Optional: To include only billed transactions as revenue in the inquiry, set the **Include only billed revenues** option to **Yes**.</span></span>

## <a name="columns"></a><span data-ttu-id="b6a82-157">Cột</span><span class="sxs-lookup"><span data-stu-id="b6a82-157">Columns</span></span>

<span data-ttu-id="b6a82-158">Truy vấn Lịch trình chi tiêu của Giải thưởng Liên bang bao gồm các cột sau:</span><span class="sxs-lookup"><span data-stu-id="b6a82-158">The Schedule of Expenditures of Federal Awards inquiry includes the following columns:</span></span>

- <span data-ttu-id="b6a82-159">Tên cụm Sản phẩm hỗ trợ liên bang trong nước</span><span class="sxs-lookup"><span data-stu-id="b6a82-159">Catalog of Federal Domestic Assistance cluster name</span></span>
- <span data-ttu-id="b6a82-160">Cơ quan trợ cấp</span><span class="sxs-lookup"><span data-stu-id="b6a82-160">Grantor agency</span></span>
- <span data-ttu-id="b6a82-161">Cơ quan chuyển tiếp</span><span class="sxs-lookup"><span data-stu-id="b6a82-161">Pass-through agency</span></span>
- <span data-ttu-id="b6a82-162">Tên khoản trợ cấp</span><span class="sxs-lookup"><span data-stu-id="b6a82-162">Grant name</span></span>
- <span data-ttu-id="b6a82-163">ID khoản trợ cấp</span><span class="sxs-lookup"><span data-stu-id="b6a82-163">Grant ID</span></span>
- <span data-ttu-id="b6a82-164">ID đơn đăng ký trợ cấp</span><span class="sxs-lookup"><span data-stu-id="b6a82-164">Grant application ID</span></span>
- <span data-ttu-id="b6a82-165">Sản phẩm hỗ trợ liên bang trong nước</span><span class="sxs-lookup"><span data-stu-id="b6a82-165">Catalog of Federal Domestic Assistance</span></span>
- <span data-ttu-id="b6a82-166">Biên nhận</span><span class="sxs-lookup"><span data-stu-id="b6a82-166">Receipts</span></span>
- <span data-ttu-id="b6a82-167">Các khoản chi tiêu</span><span class="sxs-lookup"><span data-stu-id="b6a82-167">Expenditures</span></span>
