---
title: Tạo và áp dụng các điều khoản lưu giữ khoản thanh toán cho nhà cung cấp
description: Chủ đề này cung cấp thông tin về cách thiết lập và duy trì các điều khoản lưu giữ đối với khoản thanh toán của nhà cung cấp.
author: Yowelle
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 09bb30f55ee8e1f24634e9d8b7dea95bd3dbd24f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006357"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a><span data-ttu-id="3c1b5-103">Tạo và áp dụng các điều khoản lưu giữ khoản thanh toán cho nhà cung cấp</span><span class="sxs-lookup"><span data-stu-id="3c1b5-103">Create and apply vendor payment retention terms</span></span>

[!include [banner](../includes/banner.md)] 

<span data-ttu-id="3c1b5-104">Việc thiết lập các điều khoản lưu giữ khoản thanh toán cho nhà cung cấp cho một dự án sẽ hữu ích khi tổ chức của bạn muốn giữ lại một phần khoản thanh toán cho nhà cung cấp.</span><span class="sxs-lookup"><span data-stu-id="3c1b5-104">Setting up vendor payment retention terms for a project is useful when your organization wants to retain part of the payments made to a vendor.</span></span> <span data-ttu-id="3c1b5-105">Chẳng hạn, bạn muốn giữ khoản thanh toán cho nhà cung cấp cho đến khi sản phẩm được giao đáp ứng được kỳ vọng của bạn.</span><span class="sxs-lookup"><span data-stu-id="3c1b5-105">For example, when you want to hold payment to a vendor until the products delivered meet your expectations.</span></span> <span data-ttu-id="3c1b5-106">Điều khoản lưu giữ khoản thanh toán cho nhà cung cấp có thể được chỉ định khi bạn thương lượng hợp đồng với nhà cung cấp.</span><span class="sxs-lookup"><span data-stu-id="3c1b5-106">Vendor payment retention terms can be specified when you negotiate a vendor contract.</span></span>

## <a name="create-vendor-payment-retention-terms"></a><span data-ttu-id="3c1b5-107">Tạo điều khoản lưu giữ khoản thanh toán cho nhà cung cấp</span><span class="sxs-lookup"><span data-stu-id="3c1b5-107">Create vendor payment retention terms</span></span>

<span data-ttu-id="3c1b5-108">Bạn có thể nhập tỷ lệ phần trăm khoản thanh toán cho nhà cung cấp sẽ giữ lại và tỷ lệ phần trăm số tiền đã giữ lại trước đây sẽ được giải phóng.</span><span class="sxs-lookup"><span data-stu-id="3c1b5-108">You can enter the percentage of vendor payment for retention and the percentage of the previously retained amounts to be released.</span></span> <span data-ttu-id="3c1b5-109">Số tiền sẽ tự động được giữ lại trên hóa đơn của nhà cung cấp cho đến khi hợp đồng đạt đến trạng thái hoàn thành được chỉ định.</span><span class="sxs-lookup"><span data-stu-id="3c1b5-109">Amounts are automatically retained on vendor invoices until the contract reaches the specified state of completion.</span></span> <span data-ttu-id="3c1b5-110">Sau khi bạn thiết lập các điều khoản lưu giữ, bạn có thể áp dụng chúng cho bất kỳ dự án nào của nhà cung cấp đó.</span><span class="sxs-lookup"><span data-stu-id="3c1b5-110">After you set up the retention terms, you can apply them to any project for that vendor.</span></span>

<span data-ttu-id="3c1b5-111">Hãy sử dụng các bước sau để thiết lập và duy trì các điều khoản lưu giữ khoản thanh toán cho nhà cung cấp.</span><span class="sxs-lookup"><span data-stu-id="3c1b5-111">Use the following steps to set up and maintain retention terms for vendor payments.</span></span> 

1. <span data-ttu-id="3c1b5-112">Chuyển tới **Quản lý dự án và kế toán** > **Lưu giữ** > **Điều khoản lưu giữ khoản thanh toán cho nhà cung cấp**.</span><span class="sxs-lookup"><span data-stu-id="3c1b5-112">Go to **Project management and accounting** > **Retention** > **Vendor payment retention terms**.</span></span>
2. <span data-ttu-id="3c1b5-113">Chọn **Mới** để thêm điều khoản lưu giữ mới.</span><span class="sxs-lookup"><span data-stu-id="3c1b5-113">Select **New** to add a new vendor retention term.</span></span> <span data-ttu-id="3c1b5-114">Giá trị **ID quy tắc** cho điều khoản mới sẽ được nhập tự động.</span><span class="sxs-lookup"><span data-stu-id="3c1b5-114">The **Rule ID** value for the new term is automatically entered.</span></span> 
3. <span data-ttu-id="3c1b5-115">Nhập phần mô tả ngắn gọn vào trường **Mô tả** và trên FastTab **Điều khoản**, hãy chọn **Thêm dòng** để nhập các giá trị điều khoản cho những mục sau:</span><span class="sxs-lookup"><span data-stu-id="3c1b5-115">Enter a brief description in the **Description** field, and on the **Terms** FastTab, select **Add line** to enter term values for the following:</span></span>

   - <span data-ttu-id="3c1b5-116">**Phần trăm đơn vị được giao**: Nhập tỷ lệ phần trăm hoàn thành cho điều khoản.</span><span class="sxs-lookup"><span data-stu-id="3c1b5-116">**Percentage of units delivered**: Enter a percentage of completion for the term.</span></span> <span data-ttu-id="3c1b5-117">Số tiền sẽ tự động được giữ lại trên hóa đơn của nhà cung cấp cho đến khi giai đoạn hoàn thành của dự án đạt đến tỷ lệ phần trăm đã chỉ định.</span><span class="sxs-lookup"><span data-stu-id="3c1b5-117">Amounts are automatically retained on vendor invoices until the project stage of completion is equal to the specified percentage.</span></span> <span data-ttu-id="3c1b5-118">Chẳng hạn, nếu bạn nhập 50, thì số tiền sẽ được giữ lại cho đến khi dự án hoàn thành 50 phần trăm.</span><span class="sxs-lookup"><span data-stu-id="3c1b5-118">For example, if you enter 50.00, amounts are retained until the project is 50 percent completed.</span></span>
   - <span data-ttu-id="3c1b5-119">**Tỷ lệ phần trăm giữ lại**: Nhập tỷ lệ phần trăm số tiền sẽ được giữ lại trên hóa đơn của nhà cung cấp.</span><span class="sxs-lookup"><span data-stu-id="3c1b5-119">**Percentage to retain**: Enter a percentage of the vendor invoice amount to be retained.</span></span> <span data-ttu-id="3c1b5-120">Lấy ví dụ, nếu bạn nhập 10, thì 10 phần trăm số tiền trên hóa đơn của nhà cung cấp sẽ được giữ lại cho đến khi dự án đạt được tỷ lệ phần trăm hoàn thành như đã đặt trong trường **Phần trăm đơn vị được giao**.</span><span class="sxs-lookup"><span data-stu-id="3c1b5-120">For example, if you enter 10.00, then 10 percent of the amount on a vendor invoice is retained until the project reaches the percentage of completion as set in the **Percentage of units delivered field**.</span></span>
   - <span data-ttu-id="3c1b5-121">**Tỷ lệ phần trăm sẽ giải phóng**: Chọn **Thêm dòng** để nhập tỷ lệ phần trăm của bất kỳ số tiền nào đã giữ lại trước đây sẽ được giải phóng khi dự án đạt đến mức độ hoàn thành đã chọn.</span><span class="sxs-lookup"><span data-stu-id="3c1b5-121">**Percentage to release**: Select **Add line** to enter a percentage of any previously retained amounts to be released for the selected level of project completion.</span></span>

> [!NOTE]
> <span data-ttu-id="3c1b5-122">Nếu bạn có nhiều mốc cho các mức độ hoàn thành dự án khác nhau, hãy nhập một dòng điều khoản lưu giữ riêng biệt cho mỗi quy tắc lưu giữ.</span><span class="sxs-lookup"><span data-stu-id="3c1b5-122">If you have more than one milestone for different levels of project completion, enter a separate vendor retention term line for each retention rule.</span></span> <span data-ttu-id="3c1b5-123">Mỗi dòng có thể chỉ định một tỷ lệ phần trăm lưu giữ khác nhau và một tỷ lệ phần trăm giải phóng khác nhau đối với mỗi mức độ hoàn thành dự án được chỉ định.</span><span class="sxs-lookup"><span data-stu-id="3c1b5-123">Each line can specify a different retention percentage and a different release percentage for each designated level of project completion.</span></span>

<span data-ttu-id="3c1b5-124">Sau khi bạn thiết lập các điều khoản lưu giữ cho nhà cung cấp, bạn có thể áp dụng chúng cho dự án.</span><span class="sxs-lookup"><span data-stu-id="3c1b5-124">After you create vendor retention terms for a vendor, you can apply the terms to a project.</span></span>

## <a name="apply-vendor-retention-terms-to-a-project"></a><span data-ttu-id="3c1b5-125">Áp dụng điều khoản lưu giữ cho dự án của nhà cung cấp</span><span class="sxs-lookup"><span data-stu-id="3c1b5-125">Apply vendor retention terms to a project</span></span>

1. <span data-ttu-id="3c1b5-126">Chuyển tới **Quản lý dự án và kế toán** > **Dự án** > **Tất cả dự án** và mở một dự án trong trang danh sách dự án.</span><span class="sxs-lookup"><span data-stu-id="3c1b5-126">Go to **Project management and accounting** > **Projects** > **All projects** and open a project from the project list page.</span></span>
2. <span data-ttu-id="3c1b5-127">Trên FastTab **Thỏa thuận của nhà cung cấp**, hãy chọn **Thêm dòng**.</span><span class="sxs-lookup"><span data-stu-id="3c1b5-127">On the **Vendor agreements** FastTab, select **Add line**.</span></span>
3. <span data-ttu-id="3c1b5-128">Ở trường **Mã tài khoản**, hãy chọn một trong các tùy chọn sau:</span><span class="sxs-lookup"><span data-stu-id="3c1b5-128">In the **Account code field**, select one of the following options:</span></span> 

   - <span data-ttu-id="3c1b5-129">**Bảng**: Các điều khoản lưu giữ được áp dụng cho một nhà cung cấp.</span><span class="sxs-lookup"><span data-stu-id="3c1b5-129">**Table**: The vendor retention terms apply to a single vendor.</span></span>
   - <span data-ttu-id="3c1b5-130">**Nhóm**: Các điều khoản lưu giữ được áp dụng cho tất cả các nhà cung cấp trong một nhóm nhà cung cấp.</span><span class="sxs-lookup"><span data-stu-id="3c1b5-130">**Group**: The vendor retention terms apply to all vendors in a vendor group.</span></span>
   - <span data-ttu-id="3c1b5-131">**Tất cả**: Các điều khoản lưu giữ được áp dụng cho tất cả các nhà cung cấp.</span><span class="sxs-lookup"><span data-stu-id="3c1b5-131">**All**: The vendor retention terms apply to all vendors.</span></span>

4. <span data-ttu-id="3c1b5-132">Ở trường **Nhà cung cấp/nhóm nhà cung cấp**, hãy chọn nhà cung cấp hoặc nhóm nhà cung cấp sẽ được áp dụng các điều khoản lưu giữ.</span><span class="sxs-lookup"><span data-stu-id="3c1b5-132">In the **Vendor/Vendor group field**, select the vendor or vendor group to which the vendor retention terms apply.</span></span> <span data-ttu-id="3c1b5-133">Nếu bạn đã chọn **Tất cả** ở bước trước, thì trường này sẽ không khả dụng.</span><span class="sxs-lookup"><span data-stu-id="3c1b5-133">If you selected **All** in the previous step, this field is unavailable.</span></span>
5. <span data-ttu-id="3c1b5-134">Ở trường **Điều khoản lưu giữ cho nhà cung cấp**, hãy chọn các điều khoản lưu giữ mà bạn đã tạo trong quy trình trước.</span><span class="sxs-lookup"><span data-stu-id="3c1b5-134">In the **Vendor retention terms** field, select the retention terms that you created in the previous procedure.</span></span>
6. <span data-ttu-id="3c1b5-135">Nếu dự án cũng được thiết lập các điều khoản trả tiền khi được trả tiền (PWP) cho nhà cung cấp, hãy nhập tỷ lệ phần trăm ngưỡng cho dự án trong trường **Tỷ lệ phần trăm ngưỡng PWP**.</span><span class="sxs-lookup"><span data-stu-id="3c1b5-135">If the project also has pay-when-paid (PWP) terms set up for the vendor, enter the threshold percentage for the project in the **PWP threshold percentage** field.</span></span>

<span data-ttu-id="3c1b5-136">Các điều khoản lưu giữ cho nhà cung cấp cũng được hiển thị trên các đơn đặt hàng mà bạn tạo cho nhà cung cấp.</span><span class="sxs-lookup"><span data-stu-id="3c1b5-136">The vendor retention terms are also displayed on purchase orders that you create for the vendor.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]