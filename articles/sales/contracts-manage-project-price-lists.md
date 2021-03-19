---
title: Quản lý bảng giá dự án trên hợp đồng dự án
description: Chủ đề này cung cấp thông tin về cách quản lý bảng giá dự án trên hợp đồng dự án.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2cfac6eda64d1d8e578115bba07942a7d786328f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278624"
---
# <a name="manage-project-price-lists-on-project-contracts"></a><span data-ttu-id="2f2ba-103">Quản lý bảng giá dự án trên hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="2f2ba-103">Manage project price lists on project contracts</span></span>

<span data-ttu-id="2f2ba-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="2f2ba-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2f2ba-105">Hợp đồng dự án trong Dynamics 365 Project Operations được thiết kế để hỗ trợ nhiều bảng giá bán hàng có hiệu lực theo ngày trên hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="2f2ba-105">Project contracts in Dynamics 365 Project Operations are designed to support multiple date effective sales price lists on a contract.</span></span> <span data-ttu-id="2f2ba-106">Trong Project Operations, có một thực thể liên kết mới có tên là **Bảng giá dự án**.</span><span class="sxs-lookup"><span data-stu-id="2f2ba-106">In Project Operations, there is a new associated entity called **Project Price Lists**.</span></span> <span data-ttu-id="2f2ba-107">Thực thể này có mối quan hệ một-nhiều đối với hợp đồng dự án.</span><span class="sxs-lookup"><span data-stu-id="2f2ba-107">This entity has a one-to-many relationship to a project contract.</span></span>

<span data-ttu-id="2f2ba-108">Bảng giá dự án được sử dụng để định giá các giao dịch thời gian và chi phí trên một dự án.</span><span class="sxs-lookup"><span data-stu-id="2f2ba-108">Project price lists are used to price time and expense transactions on a project.</span></span> <span data-ttu-id="2f2ba-109">Khi hợp đồng có một hoặc nhiều bảng giá dự án, các bảng giá này sẽ dùng để đưa ra mức giá dựa trên các số liệu thực tế và ước tính về thời gian, chi phí cho các dự án có liên quan đến hợp đồng thông qua mô tả hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="2f2ba-109">When a contract has one or more project price lists, these price lists are used to price for time and expense estimates and actuals on projects that are associated to the contract through the contract line.</span></span>

<span data-ttu-id="2f2ba-110">Khi không có bảng giá dự án trên hợp đồng dự án, bạn sẽ thấy cảnh báo cho biết không có bảng giá dự án nào nên không có mức giá cho các ước tính, công việc thực tế của dự án và chi phí.</span><span class="sxs-lookup"><span data-stu-id="2f2ba-110">When there are no project price lists on a project contract, you will see a warning message that there are no project price lists and your estimates, actual project work, and expenses will not be priced.</span></span> <span data-ttu-id="2f2ba-111">Sẽ không có mức giá cho các giá trị doanh thu.</span><span class="sxs-lookup"><span data-stu-id="2f2ba-111">There will be no price for sales values.</span></span>

## <a name="associate-or-unassociate-a-project-price-list-on-a-project-contract"></a><span data-ttu-id="2f2ba-112">Liên kết hoặc hủy liên kết bảng giá dự án trên một hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="2f2ba-112">Associate or unassociate a project price list on a project contract</span></span>

### <a name="create-or-associate-a-specific-price-list-for-estimating-project-based-work-and-expenses"></a><span data-ttu-id="2f2ba-113">Tạo hoặc liên kết với một bảng giá cụ thể để ước tính công việc và chi phí dựa trên dự án</span><span class="sxs-lookup"><span data-stu-id="2f2ba-113">Create or associate a specific price list for estimating project-based work and expenses</span></span>

1. <span data-ttu-id="2f2ba-114">Trên hợp đồng dự án, hãy chọn tab **Bảng giá dự án**.</span><span class="sxs-lookup"><span data-stu-id="2f2ba-114">On the project contract, select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="2f2ba-115">Trong lưới con, hãy chọn **+ Thêm bảng giá dự án mới**.</span><span class="sxs-lookup"><span data-stu-id="2f2ba-115">In the subgrid, select **+ Add New Project Price List**.</span></span>
3. <span data-ttu-id="2f2ba-116">Trên thanh trượt **Tạo nhanh**, chọn một bảng giá.</span><span class="sxs-lookup"><span data-stu-id="2f2ba-116">On the **Quick Create** slider, select a price list.</span></span> 

  <span data-ttu-id="2f2ba-117">Danh sách thả xuống hiển thị tất cả các bảng giá có ngữ cảnh được đặt thành **Bán hàng**, trong đó đơn vị tiền tệ trên bảng giá khớp với đơn vị tiền tệ trên hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="2f2ba-117">The drop-down list shows all price lists that have the context set to **Sales**, where the currency on the price list matches the currency on the contract.</span></span>
  
4. <span data-ttu-id="2f2ba-118">Nhập mô tả cho liên kết bảng giá dự án, chọn **Tiết kiệm**, sau đó đóng thanh trượt **Tạo nhanh**.</span><span class="sxs-lookup"><span data-stu-id="2f2ba-118">Enter a description for the project price list association, select **Save**, and then close the **Quick Create** slider.</span></span>

   <span data-ttu-id="2f2ba-119">Liên kết bảng giá dự án được tạo.</span><span class="sxs-lookup"><span data-stu-id="2f2ba-119">A project price list association is created.</span></span>
   
5. <span data-ttu-id="2f2ba-120">Lặp lại các bước từ 1 đến 4 để liên kết nhiều bảng giá dự án với hợp đồng dự án.</span><span class="sxs-lookup"><span data-stu-id="2f2ba-120">Repeat steps 1-4 to associate more than one project price list to the project contract.</span></span> <span data-ttu-id="2f2ba-121">Chỉ tạo nhiều bảng giá dự án nếu ngày có hiệu lực của từng bảng giá được liên kết là khác nhau.</span><span class="sxs-lookup"><span data-stu-id="2f2ba-121">Only create multiple project price lists if you have different date effectivity on each of the associated project price list.</span></span>

> [!NOTE]
> <span data-ttu-id="2f2ba-122">Project Operations không hỗ trợ trường hợp các ngày có hiệu lực của bảng giá dự án bị chồng chéo.</span><span class="sxs-lookup"><span data-stu-id="2f2ba-122">Project Operations doesn't support overlapping the date effectivity of the project price lists.</span></span> <span data-ttu-id="2f2ba-123">Nếu nhiều bảng giá dự án của một giao dịch có chung một ngày cụ thể, thì mức giá của giao dịch đó sẽ được đặt mặc định là 0.</span><span class="sxs-lookup"><span data-stu-id="2f2ba-123">If there are multiple project prices lists for a transaction with a given date, the price on that transaction will be defaulted to zero.</span></span>

### <a name="remove-a-project-price-list-association"></a><span data-ttu-id="2f2ba-124">Hủy liên kết bảng giá dự án</span><span class="sxs-lookup"><span data-stu-id="2f2ba-124">Remove a project price list association</span></span>

- <span data-ttu-id="2f2ba-125">Chọn bảng giá dự án, sau đó chọn **Xóa bảng giá dự án hợp đồng** trên lưới con.</span><span class="sxs-lookup"><span data-stu-id="2f2ba-125">Select the project price list, and then select **Delete Contract Project Price List** on the subgrid.</span></span> 

  <span data-ttu-id="2f2ba-126">Bảng giá sẽ được xóa khỏi các bảng giá của dự án trên hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="2f2ba-126">The price list is removed from the project price lists on the contract.</span></span> <span data-ttu-id="2f2ba-127">Bản thân bảng giá sẽ không bị xóa.</span><span class="sxs-lookup"><span data-stu-id="2f2ba-127">The price list itself will not be deleted.</span></span> <span data-ttu-id="2f2ba-128">Chỉ sự liên kết giữa bảng giá với hợp đồng bị xóa.</span><span class="sxs-lookup"><span data-stu-id="2f2ba-128">Only the association to the contract will be deleted.</span></span>

## <a name="set-up-automatic-defaulting-of-project-price-lists-on-a-contract"></a><span data-ttu-id="2f2ba-129">Thiết lập để tự động đặt các bảng giá dự án làm bảng giá mặc định trên hợp đồng</span><span class="sxs-lookup"><span data-stu-id="2f2ba-129">Set up automatic defaulting of project price lists on a contract</span></span>

<span data-ttu-id="2f2ba-130">Bảng giá dự án có thể được thiết lập làm bảng giá mặc định trên hợp đồng dự án.</span><span class="sxs-lookup"><span data-stu-id="2f2ba-130">A project price list can be set up as the default list on a project contract.</span></span> <span data-ttu-id="2f2ba-131">Thiết lập này có thể giúp đảm bảo rằng tất cả hợp đồng trong tổ chức của bạn luôn bắt đầu với một bảng giá tiêu chuẩn cho khoảng thời gian áp dụng mức giá đó.</span><span class="sxs-lookup"><span data-stu-id="2f2ba-131">This setup can help ensure that all contracts in your organization always start with a standard price list for that price period.</span></span>

### <a name="set-up-the-organizational-default-for-project-price-lists"></a><span data-ttu-id="2f2ba-132">Thiết lập bảng giá mặc định của tổ chức cho bảng giá dự án</span><span class="sxs-lookup"><span data-stu-id="2f2ba-132">Set up the organizational default for project price lists</span></span>

1. <span data-ttu-id="2f2ba-133">Chuyển đến **Cài đặt** > **Chung**, sau đó chọn **Tham số**.</span><span class="sxs-lookup"><span data-stu-id="2f2ba-133">Go to **Settings** > **General**, and then select **Parameters**.</span></span>
2. <span data-ttu-id="2f2ba-134">Trên trang danh sách **Tham số hoạt động**, chọn và bấm đúp vào hồ sơ để mở hồ sơ.</span><span class="sxs-lookup"><span data-stu-id="2f2ba-134">In the **Active Parameters** list page, select and double-click the record to open it.</span></span> <span data-ttu-id="2f2ba-135">Trong khi bấm đúp, hãy đảm bảo bạn không bấm vào giá trị trường là siêu liên kết.</span><span class="sxs-lookup"><span data-stu-id="2f2ba-135">While double–clicking, make sure that you are not clicking on a field value that is hyperlink.</span></span> 
3. <span data-ttu-id="2f2ba-136">Trên trang **Tham số hoạt động**, chọn tab **Bảng giá**. Một lưới con hiển thị danh sách các bảng giá mặc định sẽ xuất hiện.</span><span class="sxs-lookup"><span data-stu-id="2f2ba-136">On the **Active Parameters** page, select the **Price List** tab. A subgrid shows a list of default price lists.</span></span> <span data-ttu-id="2f2ba-137">Đây là bảng kê giá vốn và giá bán tiêu chuẩn.</span><span class="sxs-lookup"><span data-stu-id="2f2ba-137">This is a list of standard cost and sales price lists.</span></span> <span data-ttu-id="2f2ba-138">Việc có một bảng kê giá **Bán** tại đây cho mỗi đơn vị tiền tệ mà bạn bán hàng theo đó sẽ đảm bảo rằng bảng giá bán hàng là bảng giá mặc định trên bất kỳ hợp đồng nào bạn tạo cho khách hàng giao dịch bằng đơn vị tiền tệ này.</span><span class="sxs-lookup"><span data-stu-id="2f2ba-138">Having a **Sales** price list associated here for every currency that you sell in ensures that the sales price list is the default on any contract that you create for customers that transact in this currency.</span></span>

### <a name="set-up-a-customer-specific-project-price-list"></a><span data-ttu-id="2f2ba-139">Thiết lập bảng giá dự án dành riêng cho khách hàng</span><span class="sxs-lookup"><span data-stu-id="2f2ba-139">Set up a customer-specific project price list</span></span>

<span data-ttu-id="2f2ba-140">Bạn cũng có thể thiết lập bảng giá dự án dành riêng cho khách hàng khi đã thương lượng được một mức giá cơ bản với khách hàng.</span><span class="sxs-lookup"><span data-stu-id="2f2ba-140">You can also set up customer–specific project price lists when you have negotiated a master pricing agreement with your customers.</span></span>

1. <span data-ttu-id="2f2ba-141">Chuyển đến **Bán hàng** > **Khách hàng**.</span><span class="sxs-lookup"><span data-stu-id="2f2ba-141">Go to **Sales** > **Customers**.</span></span>
2. <span data-ttu-id="2f2ba-142">Trong danh sách các khách hàng hiện hoạt, hãy chọn khách hàng có bảng giá riêng.</span><span class="sxs-lookup"><span data-stu-id="2f2ba-142">From the list of active accounts, select the customer for whom have special price list.</span></span>
3. <span data-ttu-id="2f2ba-143">Chọn hồ sơ khách hàng đó để mở hồ sơ rồi chọn tab **Bảng giá dự án**. Một lưới con hiển thị danh sách bảng giá dự án cụ thể cho khách hàng này sẽ xuất hiện.</span><span class="sxs-lookup"><span data-stu-id="2f2ba-143">Select the customer record to open it and then select the **Project Price Lists** tab. A subgrid shows a list of project price lists specific to this customer.</span></span> 
4. <span data-ttu-id="2f2ba-144">Tạo một liên kết bảng giá mới tại đây để có bảng giá dự án dành riêng cho khách hàng này.</span><span class="sxs-lookup"><span data-stu-id="2f2ba-144">Create a new price list association here to have project price list specific to this customer.</span></span>

## <a name="custom-pricing-on-a-project-contract"></a><span data-ttu-id="2f2ba-145">Mức giá tùy chỉnh trên hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="2f2ba-145">Custom pricing on a project contract</span></span>

<span data-ttu-id="2f2ba-146">Sau khi bạn có bảng giá dự án mặc định cho tổ chức và khách hàng cụ thể, các hợp đồng dự án của bạn sẽ tự động được tạo với các liên kết bảng giá dự án này.</span><span class="sxs-lookup"><span data-stu-id="2f2ba-146">After you have organizational and customer-specific default project price lists, your project contracts will be created with these project price list associations automatically.</span></span> <span data-ttu-id="2f2ba-147">Tuy nhiên, các bảng giá dự án trong hợp đồng dự án sẽ luôn được sao chép cùng với ngày tháng và tên hợp đồng được gắn kèm.</span><span class="sxs-lookup"><span data-stu-id="2f2ba-147">However, project price lists on a project contract are always copied with the date and contract name appended to them.</span></span> <span data-ttu-id="2f2ba-148">Khi đó, người quản lý dự án và khách hàng có thể bắt đầu chỉnh sửa mức giá trên các bản sao nói trên.</span><span class="sxs-lookup"><span data-stu-id="2f2ba-148">The account and project managers can then begin making edits to prices on these copies.</span></span> <span data-ttu-id="2f2ba-149">Các mức giá đã thay đổi sẽ chỉ áp dụng cho hợp đồng dự án này.</span><span class="sxs-lookup"><span data-stu-id="2f2ba-149">These changed prices will be applicable to this project contract only.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]