---
title: Sử dụng Thể loại giao dịch làm thông số định giá
description: Chủ đề này cung cấp thông tin về cách sử dụng trường Thể loại giao dịch làm thông số định giá.
author: rumant
manager: tfehr
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c84d3aaf7cd7577dcd15311f225c82b538586445
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274619"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a><span data-ttu-id="2052d-103">Sử dụng Thể loại giao dịch làm thông số định giá</span><span class="sxs-lookup"><span data-stu-id="2052d-103">Use Transaction Category as a pricing dimension</span></span>


<span data-ttu-id="2052d-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="2052d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="2052d-105">Chủ đề này giải thích cách dùng trường **Thể loại giao dịch** làm thông số định giá.</span><span class="sxs-lookup"><span data-stu-id="2052d-105">This topic explains how to use the **Transaction Category** field as a pricing dimension.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="2052d-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="2052d-106">Prerequisites</span></span>
<span data-ttu-id="2052d-107">Trước khi hoàn thành các quy trình trong chủ đề này, bạn phải có một giải pháp thông số định giá mới cho tổ chức của mình.</span><span class="sxs-lookup"><span data-stu-id="2052d-107">Before you complete the procedures in this topic, you must have a new pricing dimension solution for your organization.</span></span> <span data-ttu-id="2052d-108">Nếu chưa tạo giải pháp như vậy, hãy xem [Tạo các trường và thực thể tùy chỉnh dưới dạng thông số định giá](create-custom-fields-entities-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="2052d-108">If you haven't already created one, see [Create custom fields and entities as pricing dimensions](create-custom-fields-entities-pricing-dimensions.md).</span></span>

## <a name="add-the-transaction-category-field-to-forms-and-views"></a><span data-ttu-id="2052d-109">Thêm trường Thể loại giao dịch vào các biểu mẫu và dạng xem</span><span class="sxs-lookup"><span data-stu-id="2052d-109">Add the Transaction Category field to forms and views</span></span>
<span data-ttu-id="2052d-110">Để trường **Thể loại giao dịch** hiển thị trong giải pháp thông số định giá, bạn phải thêm trường này vào tất cả biểu mẫu và dạng xem như một thực thể.</span><span class="sxs-lookup"><span data-stu-id="2052d-110">To make the **Transaction Category** field visible in the pricing dimension solution, you need to add the field to all the forms and views as an entity.</span></span>

<span data-ttu-id="2052d-111">Bảng sau liệt kê tất cả mọi biểu mẫu và dạng xem sẵn dùng, theo thực thể.</span><span class="sxs-lookup"><span data-stu-id="2052d-111">The following table lists all of the out-of-the box forms and views, by entity.</span></span> <span data-ttu-id="2052d-112">Bạn cũng phải thêm trường mới vào biểu mẫu hoặc dạng xem bổ sung bất kỳ trong các thực thể đã tùy chỉnh.</span><span class="sxs-lookup"><span data-stu-id="2052d-112">You will also need to add the new field to any additional forms or views in your customized entities.</span></span>

|  <span data-ttu-id="2052d-113">Thực thể</span><span class="sxs-lookup"><span data-stu-id="2052d-113">Entity</span></span>        | <span data-ttu-id="2052d-114">Biểu mẫu</span><span class="sxs-lookup"><span data-stu-id="2052d-114">Forms</span></span>     |<span data-ttu-id="2052d-115">Dạng xem</span><span class="sxs-lookup"><span data-stu-id="2052d-115">Views</span></span>        |
| ------------------------------|---------------------------------|----------------------------------|
|  <span data-ttu-id="2052d-116">Giá Vai trò</span><span class="sxs-lookup"><span data-stu-id="2052d-116">Role Price</span></span>| <span data-ttu-id="2052d-117">Thông tin</span><span class="sxs-lookup"><span data-stu-id="2052d-117">Information</span></span> |<span data-ttu-id="2052d-118">- Giá danh mục nguồn lực đang hoạt động</span><span class="sxs-lookup"><span data-stu-id="2052d-118">- Active Resource Category Prices</span></span><br> <span data-ttu-id="2052d-119">- Giá danh mục nguồn lực có liên kết</span><span class="sxs-lookup"><span data-stu-id="2052d-119">- Resource Category Price Associated</span></span> |
|  <span data-ttu-id="2052d-120">Tăng giá theo Vai trò</span><span class="sxs-lookup"><span data-stu-id="2052d-120">Role Price Markup</span></span>| <span data-ttu-id="2052d-121">Thông tin</span><span class="sxs-lookup"><span data-stu-id="2052d-121">Information</span></span>|<span data-ttu-id="2052d-122">- Phần tăng giá theo vai trò đang hoạt động</span><span class="sxs-lookup"><span data-stu-id="2052d-122">- Active Role Price Markup</span></span><br><span data-ttu-id="2052d-123">- Phần tăng giá theo vai trò có liên kết</span><span class="sxs-lookup"><span data-stu-id="2052d-123">- Role Price Markup Associated</span></span> |
|  <span data-ttu-id="2052d-124">Chi tiết Mô tả Báo giá</span><span class="sxs-lookup"><span data-stu-id="2052d-124">Quote Line Detail</span></span>|<span data-ttu-id="2052d-125">- Thông tin dự án</span><span class="sxs-lookup"><span data-stu-id="2052d-125">- Project Information</span></span><br><span data-ttu-id="2052d-126">- Tạo nhanh dự án</span><span class="sxs-lookup"><span data-stu-id="2052d-126">- Project Quick Create</span></span>| <span data-ttu-id="2052d-127">- Chi tiết về dòng báo giá đang hoạt động</span><span class="sxs-lookup"><span data-stu-id="2052d-127">- Active Quote Line Detail</span></span><br><span data-ttu-id="2052d-128">- Chi tiết về dòng báo giá kết hợp</span><span class="sxs-lookup"><span data-stu-id="2052d-128">- Combined Quote Line Details</span></span><br><span data-ttu-id="2052d-129">- Chi tiết về dòng báo giá có liên kết</span><span class="sxs-lookup"><span data-stu-id="2052d-129">- Quote Line Detail Associated</span></span> |
|  <span data-ttu-id="2052d-130">Chi tiết Mô tả Hợp đồng Dự án</span><span class="sxs-lookup"><span data-stu-id="2052d-130">Project Contract Line Detail</span></span>|<span data-ttu-id="2052d-131">- Thông tin dự án</span><span class="sxs-lookup"><span data-stu-id="2052d-131">- Project Information</span></span><br><span data-ttu-id="2052d-132">- Tạo nhanh dự án</span><span class="sxs-lookup"><span data-stu-id="2052d-132">- Project Quick Create</span></span>|<span data-ttu-id="2052d-133">- Chi tiết về dòng hợp đồng kết hợp</span><span class="sxs-lookup"><span data-stu-id="2052d-133">- Combined Contract Line Details</span></span><br><span data-ttu-id="2052d-134">- Chi tiết về dòng hợp đồng đang hoạt động</span><span class="sxs-lookup"><span data-stu-id="2052d-134">- Active Contract Line Details</span></span><br><span data-ttu-id="2052d-135">- Chi tiết về dòng hợp đồng có liên kết</span><span class="sxs-lookup"><span data-stu-id="2052d-135">- Contract Line Detail Associated</span></span> |
|  <span data-ttu-id="2052d-136">Nhiệm vụ dự án</span><span class="sxs-lookup"><span data-stu-id="2052d-136">Project Task</span></span>|<span data-ttu-id="2052d-137">- Thông tin</span><span class="sxs-lookup"><span data-stu-id="2052d-137">- Information</span></span><br><span data-ttu-id="2052d-138">- Biểu mẫu mới</span><span class="sxs-lookup"><span data-stu-id="2052d-138">- New Form</span></span>| &nbsp; |
|  <span data-ttu-id="2052d-139">Thành viên Nhóm Dự án</span><span class="sxs-lookup"><span data-stu-id="2052d-139">Project Team Member</span></span>|<span data-ttu-id="2052d-140">- Thông tin</span><span class="sxs-lookup"><span data-stu-id="2052d-140">- Information</span></span><br><span data-ttu-id="2052d-141">- Biểu mẫu mới</span><span class="sxs-lookup"><span data-stu-id="2052d-141">- New Form</span></span>|<span data-ttu-id="2052d-142">- Thành viên nhóm dự án đang hoạt động</span><span class="sxs-lookup"><span data-stu-id="2052d-142">- Active Project Team Members</span></span><br><span data-ttu-id="2052d-143">- Thành viên nhóm dự án</span><span class="sxs-lookup"><span data-stu-id="2052d-143">- Project Team Members</span></span><br><span data-ttu-id="2052d-144">- Thành viên nhóm dự án có liên kết</span><span class="sxs-lookup"><span data-stu-id="2052d-144">- Project Team Members Associated</span></span> |
|  <span data-ttu-id="2052d-145">Mục nhập Thời gian</span><span class="sxs-lookup"><span data-stu-id="2052d-145">Time Entry</span></span>|<span data-ttu-id="2052d-146">- Thông tin</span><span class="sxs-lookup"><span data-stu-id="2052d-146">- Information</span></span><br><span data-ttu-id="2052d-147">- Tạo mục thời gian</span><span class="sxs-lookup"><span data-stu-id="2052d-147">- Create Time Entry</span></span>|<span data-ttu-id="2052d-148">- Mục thời gian của tôi theo ngày</span><span class="sxs-lookup"><span data-stu-id="2052d-148">- My Time Entries By Date</span></span><br><span data-ttu-id="2052d-149">- Mục thời gian của tôi cho tuần này</span><span class="sxs-lookup"><span data-stu-id="2052d-149">- My Time Entries for this Week</span></span><br><span data-ttu-id="2052d-150">- Mục thời gian cần để phê duyệt</span><span class="sxs-lookup"><span data-stu-id="2052d-150">- Time entries for Approval</span></span>|
|  <span data-ttu-id="2052d-151">Dòng nhật ký kế toán</span><span class="sxs-lookup"><span data-stu-id="2052d-151">Journal Line</span></span>|<span data-ttu-id="2052d-152">- Thông tin</span><span class="sxs-lookup"><span data-stu-id="2052d-152">- Information</span></span><br><span data-ttu-id="2052d-153">- Tạo nhanh</span><span class="sxs-lookup"><span data-stu-id="2052d-153">- Quick Create</span></span>|<span data-ttu-id="2052d-154">- Dòng nhật ký kế toán hiện hoạt</span><span class="sxs-lookup"><span data-stu-id="2052d-154">- Active Journal Lines</span></span><br><span data-ttu-id="2052d-155">- Dòng nhật ký kế toán có liên kết</span><span class="sxs-lookup"><span data-stu-id="2052d-155">- Journal Line Associated</span></span>|
|  <span data-ttu-id="2052d-156">Chi tiết Mô tả Hóa đơn</span><span class="sxs-lookup"><span data-stu-id="2052d-156">Invoice Line Detail</span></span>|<span data-ttu-id="2052d-157">- Thông tin</span><span class="sxs-lookup"><span data-stu-id="2052d-157">- Information</span></span><br><span data-ttu-id="2052d-158">- Tạo nhanh</span><span class="sxs-lookup"><span data-stu-id="2052d-158">- Quick Create</span></span>|<span data-ttu-id="2052d-159">- Chi tiết về dòng hóa đơn hiện hoạt</span><span class="sxs-lookup"><span data-stu-id="2052d-159">- Active Invoice Line Details</span></span><br><span data-ttu-id="2052d-160">- Giao dịch hóa đơn có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="2052d-160">- Chargeable Invoice Transactions</span></span><br><span data-ttu-id="2052d-161">- Giao dịch hóa đơn miễn phí</span><span class="sxs-lookup"><span data-stu-id="2052d-161">- Complimentary Invoice Transactions</span></span><br><span data-ttu-id="2052d-162">- Chi tiết về dòng hóa đơn có liên kết</span><span class="sxs-lookup"><span data-stu-id="2052d-162">- Invoice Line Detail Associated</span></span> <br><span data-ttu-id="2052d-163">- Giao dịch hóa đơn không thể tính phí</span><span class="sxs-lookup"><span data-stu-id="2052d-163">- Non-Chargeable Invoice Transactions</span></span>|
|  <span data-ttu-id="2052d-164">Thực tế</span><span class="sxs-lookup"><span data-stu-id="2052d-164">Actual</span></span>|<span data-ttu-id="2052d-165">- Thông tin</span><span class="sxs-lookup"><span data-stu-id="2052d-165">- Information</span></span><br><span data-ttu-id="2052d-166">- Trường hợp thực tế hiện hoạt</span><span class="sxs-lookup"><span data-stu-id="2052d-166">- Active Actuals</span></span>| <span data-ttu-id="2052d-167">Thực tế có liên kết</span><span class="sxs-lookup"><span data-stu-id="2052d-167">Actual Associated</span></span> |

## <a name="set-up-the-transaction-category-field-as-a-pricing-dimension"></a><span data-ttu-id="2052d-168">Thiết lập trường Thể loại giao dịch làm thông số định giá</span><span class="sxs-lookup"><span data-stu-id="2052d-168">Set up the Transaction Category field as a pricing dimension</span></span>

1. <span data-ttu-id="2052d-169">Đi tới **Cài đặt** > **Tham số**.</span><span class="sxs-lookup"><span data-stu-id="2052d-169">Go to **Settings** > **Parameters**.</span></span> 
2. <span data-ttu-id="2052d-170">Trên trang **Tham số**, trên tab **Thông số định giá dựa trên số tiền**, hãy xác minh rằng lưới này hiển thị các bản ghi trong thực thể **Thông số định giá**.</span><span class="sxs-lookup"><span data-stu-id="2052d-170">On the **Parameters** page, on the **Amount-Based Pricing Dimensions** tab, verify that the grid shows the records in the **Pricing Dimensions** entity.</span></span>
3. <span data-ttu-id="2052d-171">Thêm **Thể loại giao dịch** vào danh sách này rồi đặt các trường **Áp dụng cho chi phí** và **Áp dụng cho doanh số** thành **Có**.</span><span class="sxs-lookup"><span data-stu-id="2052d-171">Add **Transaction Category** to this list and set the **Applicable to Cost** and **Applicable to Sale** fields to **Yes**.</span></span>
4. <span data-ttu-id="2052d-172">Trong trường **Loại thông số**, hãy chọn **Dựa trên số tiền**, sau đó chọn mức ưu tiên cho **Thể loại giao dịch** có liên quan đến chi phí và doanh số.</span><span class="sxs-lookup"><span data-stu-id="2052d-172">In the **Dimension Type** field, select **Amount-based**, and then select the priority for **Transaction Category** as it relates to cost and sales.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]