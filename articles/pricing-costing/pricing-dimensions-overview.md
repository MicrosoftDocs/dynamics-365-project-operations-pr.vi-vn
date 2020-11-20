---
title: Tổng quan về thông số định giá
description: Chủ đề này cung cấp thông tin về các tham số định giá trong Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: ec2e350e0e4c28ea1c9540d70c83fdf0a75dc408
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128489"
---
# <a name="pricing-dimensions-overview"></a><span data-ttu-id="d5e41-103">Tổng quan về thông số định giá</span><span class="sxs-lookup"><span data-stu-id="d5e41-103">Pricing dimensions overview</span></span>

<span data-ttu-id="d5e41-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="d5e41-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d5e41-105">Các tham số dùng trong nguồn nhân lực để thiết lập giá và chi phí rơi vào hai loại sau:</span><span class="sxs-lookup"><span data-stu-id="d5e41-105">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="d5e41-106">Mọi người</span><span class="sxs-lookup"><span data-stu-id="d5e41-106">People</span></span>
- <span data-ttu-id="d5e41-107">Công việc theo kế hoạch</span><span class="sxs-lookup"><span data-stu-id="d5e41-107">Planned work</span></span>

<span data-ttu-id="d5e41-108">Do vậy, có 2 loại giá trị tham số định giá được cung cấp:</span><span class="sxs-lookup"><span data-stu-id="d5e41-108">Because of this, there are two types of pricing dimension values available:</span></span>

- <span data-ttu-id="d5e41-109">**Bộ tùy chọn**: Tham số là các số liệu liệt kê cố định cho một bộ giá trị.</span><span class="sxs-lookup"><span data-stu-id="d5e41-109">**Option sets**: Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="d5e41-110">**Giá trị dựa trên thực thể**: Tham số có thể là bộ giá trị khác nhau.</span><span class="sxs-lookup"><span data-stu-id="d5e41-110">**Entity-based values**: Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="d5e41-111">Thông số định giá</span><span class="sxs-lookup"><span data-stu-id="d5e41-111">Pricing dimensions</span></span>

<span data-ttu-id="d5e41-112">Dynamics 365 Project Operations đi kèm với một bộ tham số định giá mặc định.</span><span class="sxs-lookup"><span data-stu-id="d5e41-112">Dynamics 365 Project Operations ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="d5e41-113">Bạn có thể xem các tham số định giá này bằng cách chuyển tới **Hoạt động dự án** > **Tham số**.</span><span class="sxs-lookup"><span data-stu-id="d5e41-113">You can view these pricing dimensions by going to **Project Operations** > **Parameters**.</span></span> <span data-ttu-id="d5e41-114">Trong bản ghi tham số, trên tab **Tham số giá dựa trên số tiền**, hãy xác minh rằng vai trò **msdyn_resourcecategory** và đơn vị tổ chức nguồn lực **msdyn_organizationalunit** có các trường **Áp dụng cho bán hàng** và **Áp dụng cho chi phí** được đặt thành **Có**.</span><span class="sxs-lookup"><span data-stu-id="d5e41-114">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="d5e41-115">Khi đã bật các trường này lên, bạn có thể thiết lập giá cả và chi phí cho từng tổ hợp vai trò và đơn vị tổ chức.</span><span class="sxs-lookup"><span data-stu-id="d5e41-115">With these fields enabled, you can set up the price and cost for each role and organizational unit combination.</span></span>

<span data-ttu-id="d5e41-116">Nếu cần giá hoặc chi phí cho nguồn lực của mình bằng các thuộc tính bổ sung, bạn có thể tạo các trường, thực thể và tham số tùy chỉnh.</span><span class="sxs-lookup"><span data-stu-id="d5e41-116">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span>

## <a name="pricing-human-resource-time"></a><span data-ttu-id="d5e41-117">Định giá thời gian nguồn nhân lực</span><span class="sxs-lookup"><span data-stu-id="d5e41-117">Pricing human resource time</span></span>
<span data-ttu-id="d5e41-118">Cách một tổ chức định giá thời gian nguồn nhân lực thường là một cân nhắc quan trọng mang tính chiến lược ảnh hưởng trực tiếp đến lợi nhuận của tổ chức.</span><span class="sxs-lookup"><span data-stu-id="d5e41-118">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="d5e41-119">Làm việc với các đội ngũ tài chính và người đứng đầu phụ trách thực hành khi tổ chức của bạn sẵn sàng xác định cách mong muốn để thiết lập tỷ lệ chi phí và hóa đơn cho thời gian nguồn nhân lực.</span><span class="sxs-lookup"><span data-stu-id="d5e41-119">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="d5e41-120">Các cân nhắc khác về giá bao gồm việc có tái sử dụng trường hoặc thực thể không phải là tham số giá hiện tại nhưng áp dụng dưới dạng tham số giá cho tổ chức của bạn hay không.</span><span class="sxs-lookup"><span data-stu-id="d5e41-120">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="d5e41-121">Các trường như **Loại giao dịch** (**msdyn_transactioncategory**) và **Nguồn lực có thể đăng ký** (**bookableresource**) là các ví dụ về tham số của ứng viên.</span><span class="sxs-lookup"><span data-stu-id="d5e41-121">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="d5e41-122">Bạn cũng nên cân nhắc xem liệu tham số định giá nên ở dạng bảng biểu hay bộ tùy chọn.</span><span class="sxs-lookup"><span data-stu-id="d5e41-122">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="d5e41-123">Nếu thấy trước các thay đổi về giá trị của tham số sẽ vượt quá 10 hoặc 12 và bạn cần các thuộc tính bổ sung trên các giá trị này, bạn có thể tạo một thực thể thay vì bộ tùy chọn.</span><span class="sxs-lookup"><span data-stu-id="d5e41-123">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="d5e41-124">Duy trì một bộ tùy chọn, chẳng hạn như thêm hoặc loại bỏ các giá trị, yêu cầu một quản trị viên hoặc nhà phát triển trong khi thêm hàng mới vào bảng có thể được hầu hết người dùng thực hiện.</span><span class="sxs-lookup"><span data-stu-id="d5e41-124">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="d5e41-125">Ví dụ sau cho thấy tỷ lệ hóa đơn được thiết lập dựa trên vai trò và đơn vị tổ chức nguồn lực mà nguồn lực thuộc về.</span><span class="sxs-lookup"><span data-stu-id="d5e41-125">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="d5e41-126">Tỷ lệ chi phí thường dựa trên thang lương của nhân viên và đơn vị tổ chức mà họ thuộc về.</span><span class="sxs-lookup"><span data-stu-id="d5e41-126">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="d5e41-127">Trong ví dụ này, các bảng tỷ lệ hóa đơn và tỷ lệ chi phí có dạng như sau.</span><span class="sxs-lookup"><span data-stu-id="d5e41-127">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="d5e41-128">**Tỷ lệ hóa đơn mẫu**</span><span class="sxs-lookup"><span data-stu-id="d5e41-128">**Sample bill rates**</span></span>

| <span data-ttu-id="d5e41-129">Vai trò</span><span class="sxs-lookup"><span data-stu-id="d5e41-129">Role</span></span>        | <span data-ttu-id="d5e41-130">Đơn vị tổ chức</span><span class="sxs-lookup"><span data-stu-id="d5e41-130">Org Unit</span></span>    |<span data-ttu-id="d5e41-131">Đơn vị</span><span class="sxs-lookup"><span data-stu-id="d5e41-131">Unit</span></span>      |<span data-ttu-id="d5e41-132">Giá</span><span class="sxs-lookup"><span data-stu-id="d5e41-132">Price</span></span>      |<span data-ttu-id="d5e41-133">Tiền tệ</span><span class="sxs-lookup"><span data-stu-id="d5e41-133">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="d5e41-134">Nhà phát triển</span><span class="sxs-lookup"><span data-stu-id="d5e41-134">Developer</span></span>   | <span data-ttu-id="d5e41-135">Contoso US</span><span class="sxs-lookup"><span data-stu-id="d5e41-135">Contoso US</span></span>  |<span data-ttu-id="d5e41-136">Hour</span><span class="sxs-lookup"><span data-stu-id="d5e41-136">Hour</span></span> | <span data-ttu-id="d5e41-137">200</span><span class="sxs-lookup"><span data-stu-id="d5e41-137">200</span></span>|<span data-ttu-id="d5e41-138">Giải pháp USD</span><span class="sxs-lookup"><span data-stu-id="d5e41-138">USD</span></span>     |
| <span data-ttu-id="d5e41-139">Nhà phát triển</span><span class="sxs-lookup"><span data-stu-id="d5e41-139">Developer</span></span>   | <span data-ttu-id="d5e41-140">Đàm Ấn Độ</span><span class="sxs-lookup"><span data-stu-id="d5e41-140">Contoso India</span></span> |<span data-ttu-id="d5e41-141">Hour</span><span class="sxs-lookup"><span data-stu-id="d5e41-141">Hour</span></span>|   <span data-ttu-id="d5e41-142">112</span><span class="sxs-lookup"><span data-stu-id="d5e41-142">112</span></span>|<span data-ttu-id="d5e41-143">Giải pháp USD</span><span class="sxs-lookup"><span data-stu-id="d5e41-143">USD</span></span>     |


<span data-ttu-id="d5e41-144">**Tỷ lệ chi phí mẫu**</span><span class="sxs-lookup"><span data-stu-id="d5e41-144">**Sample cost rates**</span></span>

| <span data-ttu-id="d5e41-145">Mức lương</span><span class="sxs-lookup"><span data-stu-id="d5e41-145">Salary Band</span></span>     | <span data-ttu-id="d5e41-146">Đơn vị tổ chức</span><span class="sxs-lookup"><span data-stu-id="d5e41-146">Org Unit</span></span>    |<span data-ttu-id="d5e41-147">Đơn vị</span><span class="sxs-lookup"><span data-stu-id="d5e41-147">Unit</span></span>      |<span data-ttu-id="d5e41-148">Giá</span><span class="sxs-lookup"><span data-stu-id="d5e41-148">Price</span></span>      |<span data-ttu-id="d5e41-149">Tiền tệ</span><span class="sxs-lookup"><span data-stu-id="d5e41-149">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="d5e41-150">My company_Band1</span><span class="sxs-lookup"><span data-stu-id="d5e41-150">My company_Band1</span></span> | <span data-ttu-id="d5e41-151">Contoso US</span><span class="sxs-lookup"><span data-stu-id="d5e41-151">Contoso US</span></span>  |<span data-ttu-id="d5e41-152">Hour</span><span class="sxs-lookup"><span data-stu-id="d5e41-152">Hour</span></span> | <span data-ttu-id="d5e41-153">145</span><span class="sxs-lookup"><span data-stu-id="d5e41-153">145</span></span>|<span data-ttu-id="d5e41-154">Giải pháp USD</span><span class="sxs-lookup"><span data-stu-id="d5e41-154">USD</span></span>     |
| <span data-ttu-id="d5e41-155">My company_Band2</span><span class="sxs-lookup"><span data-stu-id="d5e41-155">My company_Band2</span></span> | <span data-ttu-id="d5e41-156">Đàm Ấn Độ</span><span class="sxs-lookup"><span data-stu-id="d5e41-156">Contoso India</span></span> |<span data-ttu-id="d5e41-157">Hour</span><span class="sxs-lookup"><span data-stu-id="d5e41-157">Hour</span></span>|   <span data-ttu-id="d5e41-158">67</span><span class="sxs-lookup"><span data-stu-id="d5e41-158">67</span></span>|<span data-ttu-id="d5e41-159">Giải pháp USD</span><span class="sxs-lookup"><span data-stu-id="d5e41-159">USD</span></span>     |
