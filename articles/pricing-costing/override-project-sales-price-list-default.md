---
title: Thay thế bảng giá bán hàng của dự án
description: Chủ đề này cung cấp thông tin về cách tạo bảng giá bán hàng tùy chỉnh.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c97dca8685c2db7d256017cf4442416feb0e005b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130874"
---
# <a name="override-project-sales-price-lists"></a><span data-ttu-id="35be8-103">Thay thế bảng giá bán hàng của dự án</span><span class="sxs-lookup"><span data-stu-id="35be8-103">Override project sales price lists</span></span>

<span data-ttu-id="35be8-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="35be8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="customer-specific-project-price-lists"></a><span data-ttu-id="35be8-105">Bảng giá dự án cụ thể cho từng khách hàng</span><span class="sxs-lookup"><span data-stu-id="35be8-105">Customer-specific project price lists</span></span>

<span data-ttu-id="35be8-106">Các thỏa thuận về giá cụ thể cho từng khách hàng có thể được thiết lập dưới dạng bảng giá dự án trên hồ sơ tài khoản trong Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="35be8-106">Customer-specific price agreements can be set up as project price lists on an account record in Dynamics 365 Project Operations.</span></span>

<span data-ttu-id="35be8-107">Để thiết lập bảng giá dự án cụ thể cho từng khách hàng, trong khu vực **Bán hàng**, hãy chuyển đến hồ sơ tài khoản.</span><span class="sxs-lookup"><span data-stu-id="35be8-107">To set up a customer-specific project price list, in the **Sales** area, navigate to the account record.</span></span>

1. <span data-ttu-id="35be8-108">Mở trang danh sách **Tài khoản**.</span><span class="sxs-lookup"><span data-stu-id="35be8-108">Open the **Accounts** list page.</span></span>
2. <span data-ttu-id="35be8-109">Tìm và nhấp đúp vào hồ sơ khách hàng để mở trang chi tiết **Tài khoản**.</span><span class="sxs-lookup"><span data-stu-id="35be8-109">Locate and double-click a customer record to open the **Account** details page.</span></span>
3. <span data-ttu-id="35be8-110">Trên tab **Bảng giá dự án**, hãy chọn \*\*+ Bảng giá dự án mới^^.</span><span class="sxs-lookup"><span data-stu-id="35be8-110">On the **Project Price lists** tab, select \*\*+ New Project Price List^^.</span></span>
4. <span data-ttu-id="35be8-111">Trên **Bảng giá dự án mới**, hãy chọn một bảng giá từ danh sách thả xuống.</span><span class="sxs-lookup"><span data-stu-id="35be8-111">On the **New Project Price List** page, select a price list from the drop-down.</span></span> <span data-ttu-id="35be8-112">Chỉ đưa vào các bảng giá có ngữ cảnh được đặt thành **Bán hàng** và đơn vị tiền tệ của bảng giá đó khớp với đơn vị tiền tệ của tài khoản.</span><span class="sxs-lookup"><span data-stu-id="35be8-112">Only price lists that have the context set to **Sales** and whose currency matches the account currency are included.</span></span>
5. <span data-ttu-id="35be8-113">Đặt tên cho liên kết rồi chọn **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="35be8-113">Name the association, and then select **Save**.</span></span> <span data-ttu-id="35be8-114">Một bảng giá dự án cụ thể cho từng khách hàng được tạo.</span><span class="sxs-lookup"><span data-stu-id="35be8-114">A customer-specific project price list is created.</span></span> <span data-ttu-id="35be8-115">Bảng giá này sẽ được dùng để đặt mặc định giá dự án trên báo giá dự án hoặc hợp đồng được tạo cho khách hàng này, trong đó ngày tạo báo giá hoặc hợp đồng dự án nằm trong ngày có hiệu lực của bảng giá.</span><span class="sxs-lookup"><span data-stu-id="35be8-115">This price list will be used to default project prices on project quotes or contracts created for this customer where the created date of the quote or project contract falls within the date effectivity of the price list.</span></span>

## <a name="custom-pricing-on-project-quotes"></a><span data-ttu-id="35be8-116">Giá tùy chỉnh trên báo giá dự án</span><span class="sxs-lookup"><span data-stu-id="35be8-116">Custom pricing on project quotes</span></span>

<span data-ttu-id="35be8-117">Trên báo giá dự án, bạn có thể có giá dự án bắt đầu với một bảng giá tiêu chuẩn mặc định do khách hàng đặt hoặc từ các tham số dự án.</span><span class="sxs-lookup"><span data-stu-id="35be8-117">On project quotes, you can have project pricing that starts with a default standard price list that defaults from the customer or from the project parameters.</span></span>

<span data-ttu-id="35be8-118">Khi bạn cần giá tùy chỉnh cho công việc liên quan đến dự án trên một báo giá cụ thể, bạn có thể lấy giá đó từ thực thể liên kết với bảng giá dự án.</span><span class="sxs-lookup"><span data-stu-id="35be8-118">When you need custom pricing for project-related work on a particular quote, you can get that from the project price lists associated entity.</span></span>

<span data-ttu-id="35be8-119">Hoàn thành các bước sau để thiết lập giá dự án cụ thể theo báo giá.</span><span class="sxs-lookup"><span data-stu-id="35be8-119">Complete the following steps to set up quote-specific project pricing.</span></span>

1. <span data-ttu-id="35be8-120">Mở báo giá dự án rồi chọn tab **Bảng giá dự án**.</span><span class="sxs-lookup"><span data-stu-id="35be8-120">Open the project quote and select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="35be8-121">Trong lưới con, hãy chọn **Tạo giá tùy chỉnh**.</span><span class="sxs-lookup"><span data-stu-id="35be8-121">In the subgrid, select **Create custom pricing**.</span></span>

<span data-ttu-id="35be8-122">Tất cả bảng giá dự án đính kèm với báo giá đều được sao chép sang bảng giá mới.</span><span class="sxs-lookup"><span data-stu-id="35be8-122">All the project price lists that are attached to the quote are copied to new price lists.</span></span> <span data-ttu-id="35be8-123">Tên của các bảng giá mới phản ánh tên của báo giá có dấu ngày giờ cho biết thời điểm tạo các bảng giá này.</span><span class="sxs-lookup"><span data-stu-id="35be8-123">The names of the new price lists reflect the name of quote with a date-time stamp for when these price lists were created.</span></span>

<span data-ttu-id="35be8-124">Bạn có thể sử dụng từng bảng giá đó và cập nhật giá nhân công (giá vai trò) và giá chi phí (giá thể loại).</span><span class="sxs-lookup"><span data-stu-id="35be8-124">You can use each of those price lists and make updates to labor (role price) and expense (category price) prices.</span></span> <span data-ttu-id="35be8-125">Các mức giá này sẽ chỉ áp dụng cho báo giá dự án này.</span><span class="sxs-lookup"><span data-stu-id="35be8-125">These prices will only be applicable to this project quote.</span></span>

## <a name="price-lists-on-a-project-contract"></a><span data-ttu-id="35be8-126">Bảng giá trên hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="35be8-126">Price lists on a project contract</span></span>

<span data-ttu-id="35be8-127">Trên hợp đồng dự án, giá dự án luôn được đặt mặc định dưới dạng bảng giá tùy chỉnh với tên hợp đồng và dấu ngày giờ tạo được thêm vào tên.</span><span class="sxs-lookup"><span data-stu-id="35be8-127">On a project contract, project pricing always defaults as a custom price list with the name of contract and the created date time stamp appended to the name.</span></span> <span data-ttu-id="35be8-128">Điều này cũng đúng cho dù hợp đồng được tạo khi đã có báo giá hay hợp đồng được tạo từ đầu.</span><span class="sxs-lookup"><span data-stu-id="35be8-128">This is true whether the contract was created when the quote was won or if the contract was created from scratch.</span></span> <span data-ttu-id="35be8-129">Nếu cần, bạn có thể loại bỏ liên kết này khỏi bảng giá tùy chỉnh và liên kết bảng giá chuẩn với hợp đồng dự án.</span><span class="sxs-lookup"><span data-stu-id="35be8-129">If needed, you can remove this association to the custom price list and associate a standard price list to the project contract instead.</span></span>

<span data-ttu-id="35be8-130">Khi bạn liên kết một bảng giá chuẩn với bảng giá dự án trên báo giá hoặc hợp đồng, bất kỳ thay đổi nào được thực hiện đối với giá trong bảng giá đó sẽ ảnh hưởng đến tất cả báo giá và hợp đồng sử dụng bảng giá đó.</span><span class="sxs-lookup"><span data-stu-id="35be8-130">When you associate a standard price list to the project price lists on quote or contract, any changes made to the prices in the price list will impact all quotes and contracts that use the price list.</span></span>
