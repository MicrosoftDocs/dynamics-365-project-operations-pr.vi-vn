---
title: Trang chủ tham số giá và chi phí
description: Chủ đề này cung cấp tổng quan về tham số giá.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 425d7bb8-9015-4f67-b9c9-cf3602e9afe8
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 2379d0d2e038f28a1a8df87a851e9bf7db7fe33f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 03/24/2020
ms.locfileid: "3757037"
---
# <a name="pricing-and-costing-dimensions-home-page"></a><span data-ttu-id="1c8c9-103">Trang chủ tham số giá và chi phí</span><span class="sxs-lookup"><span data-stu-id="1c8c9-103">Pricing and costing dimensions home page</span></span>

<span data-ttu-id="1c8c9-104">Các tham số dùng trong nguồn nhân lực để thiết lập giá và chi phí rơi vào hai loại sau:</span><span class="sxs-lookup"><span data-stu-id="1c8c9-104">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="1c8c9-105">Mọi người</span><span class="sxs-lookup"><span data-stu-id="1c8c9-105">People</span></span>
- <span data-ttu-id="1c8c9-106">Công việc theo kế hoạch</span><span class="sxs-lookup"><span data-stu-id="1c8c9-106">Planned work</span></span>

<span data-ttu-id="1c8c9-107">Do vậy, có 2 loại giá trị tham số giá trong Project Service Automation (PSA):</span><span class="sxs-lookup"><span data-stu-id="1c8c9-107">Because of this, there are two types of pricing dimension values available in Project Service Automation (PSA):</span></span> 

- <span data-ttu-id="1c8c9-108">**Bộ tùy chọn** – Tham số là liệt kê cố định cho một bộ giá trị.</span><span class="sxs-lookup"><span data-stu-id="1c8c9-108">**Option sets** - Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="1c8c9-109">**Giá trị dựa trên thực thể** – Tham số có thể là bộ giá trị thay đổi.</span><span class="sxs-lookup"><span data-stu-id="1c8c9-109">**Entity-based values** - Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="1c8c9-110">Tham số giá</span><span class="sxs-lookup"><span data-stu-id="1c8c9-110">Pricing dimensions</span></span>

<span data-ttu-id="1c8c9-111">PSA vận chuyển với một bộ tham số giá mặc định.</span><span class="sxs-lookup"><span data-stu-id="1c8c9-111">PSA ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="1c8c9-112">Bạn có thể xem các tham số này bằng các chuyển đến **Project Service** > **Tham số**.</span><span class="sxs-lookup"><span data-stu-id="1c8c9-112">You can view these by going to **Project Service** > **Parameters**.</span></span> <span data-ttu-id="1c8c9-113">Trong bản ghi tham số, trên tab **Tham số giá dựa trên số tiền**, hãy xác minh rằng vai trò **msdyn_resourcecategory** và đơn vị tổ chức nguồn lực **msdyn_organizationalunit** có các trường **Áp dụng cho bán hàng** và **Áp dụng cho chi phí** được đặt thành **Có**.</span><span class="sxs-lookup"><span data-stu-id="1c8c9-113">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="1c8c9-114">Điều này sẽ cho phép bạn thiết lập giá cả và chi phí cho mỗi kết hợp vai trò và đơn vị tổ chức.</span><span class="sxs-lookup"><span data-stu-id="1c8c9-114">This will allow you to set up the price and cost for each role and organizational unit combination.</span></span>

![Ảnh chụp màn hình của tham số Project Service với "Áp dụng cho bán hàng" được đánh dấu](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> <span data-ttu-id="1c8c9-116">Nếu bạn đã dùng các trường sẵn dùng của vai trò và đơn vị tổ chức ở dạng tham số giá trước phiên bản 3 của PSA, thì sẽ không có thay đổi nào có thể quan sát được.</span><span class="sxs-lookup"><span data-stu-id="1c8c9-116">If you have been the using out-of-the box fields of role and organizational unit as pricing dimensions prior to version 3 of PSA, there will not be any observable change.</span></span> <span data-ttu-id="1c8c9-117">Bạn có thể tiếp tục sử dụng Project Service như bình thường.</span><span class="sxs-lookup"><span data-stu-id="1c8c9-117">You can continue to use Project Service as usual.</span></span> 

<span data-ttu-id="1c8c9-118">Nếu cần giá hoặc chi phí cho nguồn lực của mình bằng các thuộc tính bổ sung, bạn có thể tạo các trường, thực thể và tham số tùy chỉnh.</span><span class="sxs-lookup"><span data-stu-id="1c8c9-118">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="1c8c9-119">Để biết thêm thông tin, hãy xem các chủ đề sau, tuy nhiên lưu ý rằng bạn phải hoàn tất các quy trình theo thứ tự liệt kê dưới đây:</span><span class="sxs-lookup"><span data-stu-id="1c8c9-119">For more information, see the following topics, however note that you must complete the procedures in the order listed below:</span></span>

- [<span data-ttu-id="1c8c9-120">Tạo các trường và thực thể tùy chỉnh</span><span class="sxs-lookup"><span data-stu-id="1c8c9-120">Create custom fields and entities</span></span>](create-custom-fields-entities.md)
- [<span data-ttu-id="1c8c9-121">Thêm các trường tùy chỉnh vào thực thể thiết lập và giao dịch</span><span class="sxs-lookup"><span data-stu-id="1c8c9-121">Add custom fields to price setup and transactional entities</span></span>](field-references.md)
- [<span data-ttu-id="1c8c9-122">Thiết lập trường tùy chỉnh dưới dạng tham số giá</span><span class="sxs-lookup"><span data-stu-id="1c8c9-122">Set up custom fields as pricing dimensions</span></span>](set-up-pricing-dimensions.md)
- [<span data-ttu-id="1c8c9-123">Cập nhật các thuộc tính phần bổ trợ để bao gồm tham số giá mới</span><span class="sxs-lookup"><span data-stu-id="1c8c9-123">Update plug-in attributes to include new pricing dimensions</span></span>](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a><span data-ttu-id="1c8c9-124">Định giá thời gian nguồn nhân lực</span><span class="sxs-lookup"><span data-stu-id="1c8c9-124">Pricing human resource time</span></span>
<span data-ttu-id="1c8c9-125">Cách một tổ chức định giá thời gian nguồn nhân lực thường là một cân nhắc quan trọng mang tính chiến lược ảnh hưởng trực tiếp đến lợi nhuận của tổ chức.</span><span class="sxs-lookup"><span data-stu-id="1c8c9-125">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="1c8c9-126">Làm việc với các đội ngũ tài chính và người đứng đầu phụ trách thực hành khi tổ chức của bạn sẵn sàng xác định cách mong muốn để thiết lập tỷ lệ chi phí và hóa đơn cho thời gian nguồn nhân lực.</span><span class="sxs-lookup"><span data-stu-id="1c8c9-126">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="1c8c9-127">Các cân nhắc khác về giá bao gồm việc có tái sử dụng trường hoặc thực thể không phải là tham số giá hiện tại nhưng áp dụng dưới dạng tham số giá cho tổ chức của bạn hay không.</span><span class="sxs-lookup"><span data-stu-id="1c8c9-127">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="1c8c9-128">Các trường như **Loại giao dịch** (**msdyn_transactioncategory**) và **Nguồn lực có thể đăng ký** (**bookableresource**) là các ví dụ về tham số của ứng viên.</span><span class="sxs-lookup"><span data-stu-id="1c8c9-128">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="1c8c9-129">Bạn cũng nên cân nhắc xem liệu thông số giá nên là bảng hay bộ tùy chọn.</span><span class="sxs-lookup"><span data-stu-id="1c8c9-129">You should also consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="1c8c9-130">Nếu thấy trước các thay đổi về giá trị của tham số sẽ vượt quá 10 hoặc 12 và bạn cần các thuộc tính bổ sung trên các giá trị này, bạn có thể tạo một thực thể thay vì bộ tùy chọn.</span><span class="sxs-lookup"><span data-stu-id="1c8c9-130">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="1c8c9-131">Duy trì một bộ tùy chọn, chẳng hạn như thêm hoặc loại bỏ các giá trị, yêu cầu một quản trị viên hoặc nhà phát triển trong khi thêm hàng mới vào bảng có thể được hầu hết người dùng thực hiện.</span><span class="sxs-lookup"><span data-stu-id="1c8c9-131">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="1c8c9-132">Ví dụ sau cho thấy tỷ lệ hóa đơn được thiết lập dựa trên vai trò và đơn vị tổ chức nguồn lực mà nguồn lực thuộc về.</span><span class="sxs-lookup"><span data-stu-id="1c8c9-132">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="1c8c9-133">Tỷ lệ chi phí thường dựa trên thang lương của nhân viên và đơn vị tổ chức mà họ thuộc về.</span><span class="sxs-lookup"><span data-stu-id="1c8c9-133">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="1c8c9-134">Trong ví dụ này, các bảng tỷ lệ hóa đơn và tỷ lệ chi phí có dạng như sau.</span><span class="sxs-lookup"><span data-stu-id="1c8c9-134">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="1c8c9-135">**Tỷ lệ hóa đơn mẫu**</span><span class="sxs-lookup"><span data-stu-id="1c8c9-135">**Sample bill rates**</span></span>

| <span data-ttu-id="1c8c9-136">Vai trò</span><span class="sxs-lookup"><span data-stu-id="1c8c9-136">Role</span></span>        | <span data-ttu-id="1c8c9-137">Đơn vị tổ chức</span><span class="sxs-lookup"><span data-stu-id="1c8c9-137">Org Unit</span></span>    |<span data-ttu-id="1c8c9-138">Đơn vị</span><span class="sxs-lookup"><span data-stu-id="1c8c9-138">Unit</span></span>      |<span data-ttu-id="1c8c9-139">Giá</span><span class="sxs-lookup"><span data-stu-id="1c8c9-139">Price</span></span>      |<span data-ttu-id="1c8c9-140">Tiền tệ</span><span class="sxs-lookup"><span data-stu-id="1c8c9-140">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="1c8c9-141">Nhà phát triển</span><span class="sxs-lookup"><span data-stu-id="1c8c9-141">Developer</span></span>   | <span data-ttu-id="1c8c9-142">Contoso US</span><span class="sxs-lookup"><span data-stu-id="1c8c9-142">Contoso US</span></span>  |<span data-ttu-id="1c8c9-143">Hour</span><span class="sxs-lookup"><span data-stu-id="1c8c9-143">Hour</span></span> | <span data-ttu-id="1c8c9-144">200</span><span class="sxs-lookup"><span data-stu-id="1c8c9-144">200</span></span>|<span data-ttu-id="1c8c9-145">Giải pháp USD</span><span class="sxs-lookup"><span data-stu-id="1c8c9-145">USD</span></span>     |
| <span data-ttu-id="1c8c9-146">Nhà phát triển</span><span class="sxs-lookup"><span data-stu-id="1c8c9-146">Developer</span></span>   | <span data-ttu-id="1c8c9-147">Đàm Ấn Độ</span><span class="sxs-lookup"><span data-stu-id="1c8c9-147">Contoso India</span></span> |<span data-ttu-id="1c8c9-148">Hour</span><span class="sxs-lookup"><span data-stu-id="1c8c9-148">Hour</span></span>|   <span data-ttu-id="1c8c9-149">112</span><span class="sxs-lookup"><span data-stu-id="1c8c9-149">112</span></span>|<span data-ttu-id="1c8c9-150">Giải pháp USD</span><span class="sxs-lookup"><span data-stu-id="1c8c9-150">USD</span></span>     |


<span data-ttu-id="1c8c9-151">**Tỷ lệ chi phí mẫu**</span><span class="sxs-lookup"><span data-stu-id="1c8c9-151">**Sample cost rates**</span></span>

| <span data-ttu-id="1c8c9-152">Mức lương</span><span class="sxs-lookup"><span data-stu-id="1c8c9-152">Salary Band</span></span>     | <span data-ttu-id="1c8c9-153">Đơn vị tổ chức</span><span class="sxs-lookup"><span data-stu-id="1c8c9-153">Org Unit</span></span>    |<span data-ttu-id="1c8c9-154">Đơn vị</span><span class="sxs-lookup"><span data-stu-id="1c8c9-154">Unit</span></span>      |<span data-ttu-id="1c8c9-155">Giá</span><span class="sxs-lookup"><span data-stu-id="1c8c9-155">Price</span></span>      |<span data-ttu-id="1c8c9-156">Tiền tệ</span><span class="sxs-lookup"><span data-stu-id="1c8c9-156">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="1c8c9-157">My company_Band1</span><span class="sxs-lookup"><span data-stu-id="1c8c9-157">My company_Band1</span></span> | <span data-ttu-id="1c8c9-158">Contoso US</span><span class="sxs-lookup"><span data-stu-id="1c8c9-158">Contoso US</span></span>  |<span data-ttu-id="1c8c9-159">Hour</span><span class="sxs-lookup"><span data-stu-id="1c8c9-159">Hour</span></span> | <span data-ttu-id="1c8c9-160">145</span><span class="sxs-lookup"><span data-stu-id="1c8c9-160">145</span></span>|<span data-ttu-id="1c8c9-161">Giải pháp USD</span><span class="sxs-lookup"><span data-stu-id="1c8c9-161">USD</span></span>     |
| <span data-ttu-id="1c8c9-162">My company_Band2</span><span class="sxs-lookup"><span data-stu-id="1c8c9-162">My company_Band2</span></span> | <span data-ttu-id="1c8c9-163">Đàm Ấn Độ</span><span class="sxs-lookup"><span data-stu-id="1c8c9-163">Contoso India</span></span> |<span data-ttu-id="1c8c9-164">Hour</span><span class="sxs-lookup"><span data-stu-id="1c8c9-164">Hour</span></span>|   <span data-ttu-id="1c8c9-165">67</span><span class="sxs-lookup"><span data-stu-id="1c8c9-165">67</span></span>|<span data-ttu-id="1c8c9-166">Giải pháp USD</span><span class="sxs-lookup"><span data-stu-id="1c8c9-166">USD</span></span>     |
