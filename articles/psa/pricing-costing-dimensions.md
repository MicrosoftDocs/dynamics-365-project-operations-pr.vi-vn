---
title: Trang chủ tham số giá và chi phí
description: Chủ đề này cung cấp tổng quan về tham số giá.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 515a2e2e518614884b414ca43702e8bfea2c6919
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087149"
---
# <a name="pricing-and-costing-dimensions-home-page"></a><span data-ttu-id="e6b10-103">Trang chủ tham số giá và chi phí</span><span class="sxs-lookup"><span data-stu-id="e6b10-103">Pricing and costing dimensions home page</span></span>

<span data-ttu-id="e6b10-104">Các thông số được sử dụng để đặt giá và tính chi phí nhân công trong các tổ chức dựa trên dự án chịu ảnh hưởng của các thuộc tính sau:</span><span class="sxs-lookup"><span data-stu-id="e6b10-104">The dimensions used to set labor pricing and costing in project-based organizations are influenced by the following attributes:</span></span>

- <span data-ttu-id="e6b10-105">Những người làm công việc giống với kinh nghiệm, vai trò hoặc vị trí địa lý của họ</span><span class="sxs-lookup"><span data-stu-id="e6b10-105">People doing work similar to their experience, role, or geography</span></span>
- <span data-ttu-id="e6b10-106">Công việc được thực hiện tương tự với mức độ phức tạp hoặc thời gian trong ngày</span><span class="sxs-lookup"><span data-stu-id="e6b10-106">Work to be performed similar to its complexity or time of day</span></span>

<span data-ttu-id="e6b10-107">Do tính chất điển hình của các loại công việc này và những người cần thiết để thực hiện công việc, có hai loại giá trị thông số định giá có sẵn trong Project Service Automation:</span><span class="sxs-lookup"><span data-stu-id="e6b10-107">Given the typical nature of these attrubutes of the work and the people required to perform the work, there are two types of pricing dimension values available in Project Service Automation:</span></span> 

- <span data-ttu-id="e6b10-108">**Bộ tùy chọn** - Thuộc tính là các số liệu liệt kê cố định cho một bộ giá trị.</span><span class="sxs-lookup"><span data-stu-id="e6b10-108">**Option sets** - Attributes that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="e6b10-109">**Giá trị dựa trên thực thể** - Các thuộc tính có thể có một bộ giá trị đa dạng là hữu hạn nhưng có thể thay đổi theo thời gian.</span><span class="sxs-lookup"><span data-stu-id="e6b10-109">**Entity-based values** - Attributes that can have a varied set of values that are finite but can change over time.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="e6b10-110">Thông số định giá</span><span class="sxs-lookup"><span data-stu-id="e6b10-110">Pricing dimensions</span></span>

<span data-ttu-id="e6b10-111">PSA vận chuyển với một bộ tham số giá mặc định.</span><span class="sxs-lookup"><span data-stu-id="e6b10-111">PSA ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="e6b10-112">Bạn có thể xem các tham số này bằng các chuyển đến **Project Service** > **Tham số**.</span><span class="sxs-lookup"><span data-stu-id="e6b10-112">You can view these by going to **Project Service** > **Parameters**.</span></span> <span data-ttu-id="e6b10-113">Trong bản ghi tham số, trên tab **Tham số giá dựa trên số tiền** , hãy xác minh rằng vai trò **msdyn_resourcecategory** và đơn vị tổ chức nguồn lực **msdyn_organizationalunit** có các trường **Áp dụng cho bán hàng** và **Áp dụng cho chi phí** được đặt thành **Có**.</span><span class="sxs-lookup"><span data-stu-id="e6b10-113">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="e6b10-114">Điều này sẽ cho phép bạn thiết lập giá cả và chi phí cho mỗi kết hợp vai trò và đơn vị tổ chức.</span><span class="sxs-lookup"><span data-stu-id="e6b10-114">This will allow you to set up the price and cost for each role and organizational unit combination.</span></span>

![Ảnh chụp màn hình của tham số Project Service với "Áp dụng cho bán hàng" được đánh dấu](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> <span data-ttu-id="e6b10-116">Nếu bạn đã dùng các trường sẵn dùng của vai trò và đơn vị tổ chức ở dạng tham số giá trước phiên bản 3 của PSA, thì sẽ không có thay đổi nào có thể quan sát được.</span><span class="sxs-lookup"><span data-stu-id="e6b10-116">If you have been the using out-of-the box fields of role and organizational unit as pricing dimensions prior to version 3 of PSA, there will not be any observable change.</span></span> <span data-ttu-id="e6b10-117">Bạn có thể tiếp tục sử dụng Project Service như bình thường.</span><span class="sxs-lookup"><span data-stu-id="e6b10-117">You can continue to use Project Service as usual.</span></span> 

<span data-ttu-id="e6b10-118">Nếu cần giá hoặc chi phí cho nguồn lực của mình bằng các thuộc tính bổ sung, bạn có thể tạo các trường, thực thể và tham số tùy chỉnh.</span><span class="sxs-lookup"><span data-stu-id="e6b10-118">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="e6b10-119">Để biết thêm thông tin, hãy xem các chủ đề sau, tuy nhiên lưu ý rằng bạn phải hoàn tất các quy trình theo thứ tự liệt kê dưới đây:</span><span class="sxs-lookup"><span data-stu-id="e6b10-119">For more information, see the following topics, however note that you must complete the procedures in the order listed below:</span></span>

- [<span data-ttu-id="e6b10-120">Tạo các trường và thực thể tùy chỉnh</span><span class="sxs-lookup"><span data-stu-id="e6b10-120">Create custom fields and entities</span></span>](create-custom-fields-entities.md)
- [<span data-ttu-id="e6b10-121">Thêm các trường tùy chỉnh vào thực thể thiết lập và giao dịch</span><span class="sxs-lookup"><span data-stu-id="e6b10-121">Add custom fields to price setup and transactional entities</span></span>](field-references.md)
- [<span data-ttu-id="e6b10-122">Thiết lập trường tùy chỉnh làm thông số định giá </span><span class="sxs-lookup"><span data-stu-id="e6b10-122">Set up custom fields as pricing dimensions</span></span>](set-up-pricing-dimensions.md)
- [<span data-ttu-id="e6b10-123">Cập nhật các thuộc tính phần bổ trợ để bao gồm tham số giá mới</span><span class="sxs-lookup"><span data-stu-id="e6b10-123">Update plug-in attributes to include new pricing dimensions</span></span>](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a><span data-ttu-id="e6b10-124">Định giá thời gian nguồn nhân lực</span><span class="sxs-lookup"><span data-stu-id="e6b10-124">Pricing human resource time</span></span>
<span data-ttu-id="e6b10-125">Cách một tổ chức định giá thời gian nguồn nhân lực thường là một cân nhắc quan trọng mang tính chiến lược ảnh hưởng trực tiếp đến lợi nhuận của tổ chức.</span><span class="sxs-lookup"><span data-stu-id="e6b10-125">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="e6b10-126">Làm việc với các đội ngũ tài chính và người đứng đầu phụ trách thực hành khi tổ chức của bạn sẵn sàng xác định cách mong muốn để thiết lập tỷ lệ chi phí và hóa đơn cho thời gian nguồn nhân lực.</span><span class="sxs-lookup"><span data-stu-id="e6b10-126">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="e6b10-127">Các cân nhắc khác về giá bao gồm việc có tái sử dụng trường hoặc thực thể không phải là tham số giá hiện tại nhưng áp dụng dưới dạng tham số giá cho tổ chức của bạn hay không.</span><span class="sxs-lookup"><span data-stu-id="e6b10-127">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="e6b10-128">Các trường như **Loại giao dịch** ( **msdyn_transactioncategory** ) và **Nguồn lực có thể đăng ký** ( **bookableresource** ) là các ví dụ về tham số của ứng viên.</span><span class="sxs-lookup"><span data-stu-id="e6b10-128">Fields like **Transaction Category** ( **msdyn_transactioncategory** ) and **Bookable Resource** ( **bookableresource** ) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="e6b10-129">Bạn cũng nên cân nhắc xem liệu tham số định giá nên ở dạng bảng biểu hay bộ tùy chọn.</span><span class="sxs-lookup"><span data-stu-id="e6b10-129">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="e6b10-130">Nếu thấy trước các thay đổi về giá trị của tham số sẽ vượt quá 10 hoặc 12 và bạn cần các thuộc tính bổ sung trên các giá trị này, hãy tạo một thực thể thay vì bộ tùy chọn.</span><span class="sxs-lookup"><span data-stu-id="e6b10-130">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, create an entity rather than an option set.</span></span> <span data-ttu-id="e6b10-131">Duy trì một bộ tùy chọn, chẳng hạn như thêm hoặc loại bỏ các giá trị, yêu cầu một quản trị viên hoặc nhà phát triển trong khi thêm hàng mới vào bảng có thể được hầu hết người dùng doanh nghiệp thực hiện.</span><span class="sxs-lookup"><span data-stu-id="e6b10-131">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most business users.</span></span>

<span data-ttu-id="e6b10-132">Ví dụ sau cho thấy tỷ lệ hóa đơn được thiết lập dựa trên vai trò và đơn vị tổ chức nguồn lực mà nguồn lực thuộc về.</span><span class="sxs-lookup"><span data-stu-id="e6b10-132">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="e6b10-133">Tỷ lệ chi phí thường dựa trên thang lương của nhân viên và đơn vị tổ chức mà họ thuộc về.</span><span class="sxs-lookup"><span data-stu-id="e6b10-133">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="e6b10-134">Trong ví dụ này, các bảng tỷ lệ hóa đơn và tỷ lệ chi phí có dạng như sau.</span><span class="sxs-lookup"><span data-stu-id="e6b10-134">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="e6b10-135">**Tỷ lệ hóa đơn mẫu**</span><span class="sxs-lookup"><span data-stu-id="e6b10-135">**Sample bill rates**</span></span>

| <span data-ttu-id="e6b10-136">Vai trò</span><span class="sxs-lookup"><span data-stu-id="e6b10-136">Role</span></span>        | <span data-ttu-id="e6b10-137">Đơn vị tổ chức</span><span class="sxs-lookup"><span data-stu-id="e6b10-137">Org Unit</span></span>    |<span data-ttu-id="e6b10-138">Đơn vị</span><span class="sxs-lookup"><span data-stu-id="e6b10-138">Unit</span></span>      |<span data-ttu-id="e6b10-139">Giá</span><span class="sxs-lookup"><span data-stu-id="e6b10-139">Price</span></span>      |<span data-ttu-id="e6b10-140">Tiền tệ</span><span class="sxs-lookup"><span data-stu-id="e6b10-140">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="e6b10-141">Nhà phát triển</span><span class="sxs-lookup"><span data-stu-id="e6b10-141">Developer</span></span>   | <span data-ttu-id="e6b10-142">Contoso US</span><span class="sxs-lookup"><span data-stu-id="e6b10-142">Contoso US</span></span>  |<span data-ttu-id="e6b10-143">Hour</span><span class="sxs-lookup"><span data-stu-id="e6b10-143">Hour</span></span> | <span data-ttu-id="e6b10-144">200</span><span class="sxs-lookup"><span data-stu-id="e6b10-144">200</span></span>|<span data-ttu-id="e6b10-145">Giải pháp USD</span><span class="sxs-lookup"><span data-stu-id="e6b10-145">USD</span></span>     |
| <span data-ttu-id="e6b10-146">Nhà phát triển</span><span class="sxs-lookup"><span data-stu-id="e6b10-146">Developer</span></span>   | <span data-ttu-id="e6b10-147">Đàm Ấn Độ</span><span class="sxs-lookup"><span data-stu-id="e6b10-147">Contoso India</span></span> |<span data-ttu-id="e6b10-148">Hour</span><span class="sxs-lookup"><span data-stu-id="e6b10-148">Hour</span></span>|   <span data-ttu-id="e6b10-149">112</span><span class="sxs-lookup"><span data-stu-id="e6b10-149">112</span></span>|<span data-ttu-id="e6b10-150">Giải pháp USD</span><span class="sxs-lookup"><span data-stu-id="e6b10-150">USD</span></span>     |


<span data-ttu-id="e6b10-151">**Tỷ lệ chi phí mẫu**</span><span class="sxs-lookup"><span data-stu-id="e6b10-151">**Sample cost rates**</span></span>

| <span data-ttu-id="e6b10-152">Mức lương</span><span class="sxs-lookup"><span data-stu-id="e6b10-152">Salary Band</span></span>     | <span data-ttu-id="e6b10-153">Đơn vị tổ chức</span><span class="sxs-lookup"><span data-stu-id="e6b10-153">Org Unit</span></span>    |<span data-ttu-id="e6b10-154">Đơn vị</span><span class="sxs-lookup"><span data-stu-id="e6b10-154">Unit</span></span>      |<span data-ttu-id="e6b10-155">Giá</span><span class="sxs-lookup"><span data-stu-id="e6b10-155">Price</span></span>      |<span data-ttu-id="e6b10-156">Tiền tệ</span><span class="sxs-lookup"><span data-stu-id="e6b10-156">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="e6b10-157">My company_Band1</span><span class="sxs-lookup"><span data-stu-id="e6b10-157">My company_Band1</span></span> | <span data-ttu-id="e6b10-158">Contoso US</span><span class="sxs-lookup"><span data-stu-id="e6b10-158">Contoso US</span></span>  |<span data-ttu-id="e6b10-159">Hour</span><span class="sxs-lookup"><span data-stu-id="e6b10-159">Hour</span></span> | <span data-ttu-id="e6b10-160">145</span><span class="sxs-lookup"><span data-stu-id="e6b10-160">145</span></span>|<span data-ttu-id="e6b10-161">Giải pháp USD</span><span class="sxs-lookup"><span data-stu-id="e6b10-161">USD</span></span>     |
| <span data-ttu-id="e6b10-162">My company_Band2</span><span class="sxs-lookup"><span data-stu-id="e6b10-162">My company_Band2</span></span> | <span data-ttu-id="e6b10-163">Đàm Ấn Độ</span><span class="sxs-lookup"><span data-stu-id="e6b10-163">Contoso India</span></span> |<span data-ttu-id="e6b10-164">Hour</span><span class="sxs-lookup"><span data-stu-id="e6b10-164">Hour</span></span>|   <span data-ttu-id="e6b10-165">67</span><span class="sxs-lookup"><span data-stu-id="e6b10-165">67</span></span>|<span data-ttu-id="e6b10-166">Giải pháp USD</span><span class="sxs-lookup"><span data-stu-id="e6b10-166">USD</span></span>     |
