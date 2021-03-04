---
title: Đặt cấu hình quản lý chi phí
description: Bài viết này mô tả những cân nhắc và quyết định mà bạn phải thực hiện trong quá trình lập kế hoạch trước khi đặt cấu hình Quản lý chi phí trong Microsoft Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: db3529597c662a326730cf6a0b855ae865f0dce5
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960363"
---
# <a name="configure-expense-management"></a><span data-ttu-id="9f6e5-103">Đặt cấu hình quản lý chi phí</span><span class="sxs-lookup"><span data-stu-id="9f6e5-103">Configure expense management</span></span>

<span data-ttu-id="9f6e5-104">Chủ đề này mô tả những cân nhắc và quyết định mà bạn phải thực hiện trong quá trình lập kế hoạch trước khi đặt cấu hình Quản lý chi phí.</span><span class="sxs-lookup"><span data-stu-id="9f6e5-104">This topic describes the considerations and the decisions that you must make during the planning process before you configure Expense management.</span></span> <span data-ttu-id="9f6e5-105">Trong Quản lý chi phí, bạn có thể lưu trữ thông tin về phương thức thanh toán, tiêu chuẩn đi lại, báo cáo chi phí, chính sách, v.v.</span><span class="sxs-lookup"><span data-stu-id="9f6e5-105">In Expense management, you can store information about payment methods, travel requisitions, expense reports, policies, and so on.</span></span>

<span data-ttu-id="9f6e5-106">Bởi vì nhiều quyết định mà bạn đưa ra khi lập kế hoạch cấu hình cho Quản lý chi phí dựa trên hệ thống cấp bậc và cấu trúc tài chính của tổ chức bạn, bạn phải tham khảo các tài liệu lập kế hoạch cho các lĩnh vực đó.</span><span class="sxs-lookup"><span data-stu-id="9f6e5-106">Because many of the decisions that you make when you plan your configuration for Expense management are based on your organization’s hierarchy and financial structure, you must refer to the planning documents for those areas.</span></span>

## <a name="intercompany-expenses"></a><span data-ttu-id="9f6e5-107">Chi phí liên công ty</span><span class="sxs-lookup"><span data-stu-id="9f6e5-107">Intercompany expenses</span></span>

<span data-ttu-id="9f6e5-108">Khi kích hoạt chi phí liên công ty, bạn cho phép các pháp nhân và nhân viên chịu chi phí thay mặt cho một pháp nhân khác và thu tiền thanh toán từ pháp nhân lao động trong tổ chức của bạn.</span><span class="sxs-lookup"><span data-stu-id="9f6e5-108">When you enable intercompany expenses, you allow legal entities and employees to incur expenses on behalf of another legal entity, and collect payment from the legal entity of employment within your organization.</span></span> <span data-ttu-id="9f6e5-109">Ví dụ: một nhân viên trong pháp nhân A hoàn thành một dự án cho pháp nhân B và dự án phát sinh các chi phí liên quan đến việc đi lại.</span><span class="sxs-lookup"><span data-stu-id="9f6e5-109">For example, an employee in legal entity A completes a project for legal entity B, and the project incurs travel related expenses.</span></span> <span data-ttu-id="9f6e5-110">Nếu chi phí liên công ty được kích hoạt, thì nhân viên có thể gửi báo cáo chi phí sẽ đăng chi phí đó cho pháp nhân B và chi phí phải do pháp nhân A thanh toán. Nếu tổ chức của bạn không có nhiều pháp nhân, bạn không phải kích hoạt chi phí liên công ty.</span><span class="sxs-lookup"><span data-stu-id="9f6e5-110">If intercompany expenses are enabled, the employee can then file an expense report that will post the expense to legal entity B, and the expense must then be paid by legal entity A. If your organization doesn’t have multiple legal entities, you don’t have to enable intercompany expenses.</span></span>

<span data-ttu-id="9f6e5-111">**Quyết định:** Bạn có muốn kích hoạt chi phí liên công ty không?</span><span class="sxs-lookup"><span data-stu-id="9f6e5-111">**Decision:** Do you want to enable intercompany expenses?</span></span>

## <a name="financial-management"></a><span data-ttu-id="9f6e5-112">Quản lý tài chính</span><span class="sxs-lookup"><span data-stu-id="9f6e5-112">Financial management</span></span>

<span data-ttu-id="9f6e5-113">Quản lý chi phí được tích hợp chặt chẽ với quản lý tài chính của tổ chức bạn.</span><span class="sxs-lookup"><span data-stu-id="9f6e5-113">Expense management is tightly integrated with the financial management of your organization.</span></span> <span data-ttu-id="9f6e5-114">Rất nhiều cấu hình của bạn cho Quản lý chi phí sẽ dựa trên các quyết định mà bạn đã đưa ra về tài chính của tổ chức bạn.</span><span class="sxs-lookup"><span data-stu-id="9f6e5-114">Lots of your configuration for Expense management will be based on the decisions that you’ve made about your organization’s finances.</span></span> <span data-ttu-id="9f6e5-115">Các phần sau đây mô tả những lĩnh vực khác nhau yêu cầu lập kế hoạch và quyết định, dựa trên các quyết định tài chính của tổ chức bạn và hướng dẫn từ nhóm lãnh đạo của bạn.</span><span class="sxs-lookup"><span data-stu-id="9f6e5-115">The following sections describe the various areas that require planning and decisions, based on your organization’s financial decisions and guidance from your leadership team.</span></span>

### <a name="per-diems"></a><span data-ttu-id="9f6e5-116">Công nhật</span><span class="sxs-lookup"><span data-stu-id="9f6e5-116">Per diems</span></span>

<span data-ttu-id="9f6e5-117">Bạn phải xác định công tác phí của nhân viên mà tổ chức của bạn cung cấp.</span><span class="sxs-lookup"><span data-stu-id="9f6e5-117">You must define the employee per diems that your organization provides.</span></span> <span data-ttu-id="9f6e5-118">Vì công tác phí thường được sử dụng để trang trải các chi phí như ăn uống, chỗ ở và các chi phí phát sinh khác, bạn có thể tạo quy tắc cho phụ cấp công tác phí mà tổ chức của bạn cung cấp.</span><span class="sxs-lookup"><span data-stu-id="9f6e5-118">Because per diems are typically used to cover expenses such as meals, lodging, and other incidental expenses, you can create rules for the per diem allowances that your organization offers.</span></span> <span data-ttu-id="9f6e5-119">mức công tác phí có thể dựa trên thời gian trong năm, địa điểm đến hoặc cả hai.</span><span class="sxs-lookup"><span data-stu-id="9f6e5-119">per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="9f6e5-120">Khi bạn xác định quy tắc công tác phí, bạn có thể chỉ định rằng tỷ lệ phần trăm công tác phí sẽ được giữ lại nếu người lao động nhận được các bữa ăn hoặc dịch vụ miễn phí.</span><span class="sxs-lookup"><span data-stu-id="9f6e5-120">When you define a per diem rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="9f6e5-121">Bạn cũng có thể xác định các bậc mức công tác phí để đặt số giờ tối thiểu và tối đa mà mức công tác phí có thể áp dụng cho việc đi lại của nhân viên.</span><span class="sxs-lookup"><span data-stu-id="9f6e5-121">You can also define per diem rate tiers to set the minimum and maximum number of hours that the per diem rate can be applied to a worker’s travel.</span></span>

<span data-ttu-id="9f6e5-122">**Quyết định:**</span><span class="sxs-lookup"><span data-stu-id="9f6e5-122">**Decisions:**</span></span>

- <span data-ttu-id="9f6e5-123">Quy tắc công tác phí mặc định cho ngày đầu tiên và ngày cuối cùng:</span><span class="sxs-lookup"><span data-stu-id="9f6e5-123">Default per diem rules for the first and last days:</span></span>

    - <span data-ttu-id="9f6e5-124">Số giờ tối thiểu mà một nhân viên có thể yêu cầu trong một ngày mà vẫn nhận được công tác phí là bao nhiêu?</span><span class="sxs-lookup"><span data-stu-id="9f6e5-124">What is the minimum number of hours that an employee can claim for a day and still receive a per diem?</span></span>
    - <span data-ttu-id="9f6e5-125">Có giảm số lượng được cung cấp cho các bữa ăn của ngày đầu tiên và ngày cuối cùng không?</span><span class="sxs-lookup"><span data-stu-id="9f6e5-125">Is there a reduction in the amount that is offered for meals for the first day and last day?</span></span> <span data-ttu-id="9f6e5-126">Nếu có giảm thì phần trăm giảm là bao nhiêu?</span><span class="sxs-lookup"><span data-stu-id="9f6e5-126">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="9f6e5-127">Có giảm số lượng được cung cấp cho chi phí khách sạn của ngày đầu tiên và ngày cuối cùng không?</span><span class="sxs-lookup"><span data-stu-id="9f6e5-127">Is there a reduction in the amount that is offered for a hotel for the first day and last day?</span></span> <span data-ttu-id="9f6e5-128">Nếu có giảm thì phần trăm giảm là bao nhiêu?</span><span class="sxs-lookup"><span data-stu-id="9f6e5-128">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="9f6e5-129">Có giảm số lượng được cung cấp cho các chi phí khác phát sinh vào ngày đầu tiên và ngày cuối cùng không?</span><span class="sxs-lookup"><span data-stu-id="9f6e5-129">Is there a reduction in the amount that is offered for other expenses that are incurred on the first day and last day?</span></span> <span data-ttu-id="9f6e5-130">Nếu có giảm thì phần trăm giảm là bao nhiêu?</span><span class="sxs-lookup"><span data-stu-id="9f6e5-130">If there is a reduction, what is the percentage of the reduction?</span></span>

- <span data-ttu-id="9f6e5-131">Quy tắc công tác phí mặc định:</span><span class="sxs-lookup"><span data-stu-id="9f6e5-131">Default per diem rules:</span></span>

    - <span data-ttu-id="9f6e5-132">Ví dụ: Có giảm phần trăm phụ cấp công tác phí cho mỗi bữa ăn nếu bữa ăn đó là miễn phí không?</span><span class="sxs-lookup"><span data-stu-id="9f6e5-132">Is there a percentage reduction in the per diem allowance for each meal if, for example, the meal is complimentary?</span></span> <span data-ttu-id="9f6e5-133">Nếu có giảm thì phần trăm giảm cho mỗi bữa ăn là bao nhiêu?</span><span class="sxs-lookup"><span data-stu-id="9f6e5-133">If there is a reduction, what is the reduction percentage for each meal?</span></span>
    - <span data-ttu-id="9f6e5-134">Mức giảm tiền ăn được tính theo ngày, theo chuyến đi hay theo số bữa ăn trong ngày?</span><span class="sxs-lookup"><span data-stu-id="9f6e5-134">Is the meal reduction calculated per day, per trip, or by the number of meals per day?</span></span>
    - <span data-ttu-id="9f6e5-135">Số tiền công tác phí nên được làm tròn theo cách thông thường hay làm tròn tăng?</span><span class="sxs-lookup"><span data-stu-id="9f6e5-135">Should per diem amounts be rounded in the regular manner or rounded up?</span></span>
    - <span data-ttu-id="9f6e5-136">Công tác phí được tính theo chu kỳ 24 giờ hay theo ngày dương lịch?</span><span class="sxs-lookup"><span data-stu-id="9f6e5-136">Are per diems calculated on a 24-hour period or on a calendar day?</span></span>

- <span data-ttu-id="9f6e5-137">Quy tắc công tác phí dựa trên vị trí:</span><span class="sxs-lookup"><span data-stu-id="9f6e5-137">Per diem rules that are based on location:</span></span>

    - <span data-ttu-id="9f6e5-138">Mức công tác phí có thay đổi theo vị trí không?</span><span class="sxs-lookup"><span data-stu-id="9f6e5-138">Do per diem rates vary according to location?</span></span> <span data-ttu-id="9f6e5-139">Bao gồm những vị trí nào?</span><span class="sxs-lookup"><span data-stu-id="9f6e5-139">What locations are included?</span></span>
    - <span data-ttu-id="9f6e5-140">Nếu mức công tác phí thay đổi theo vị trí thì đối với từng vị trí, tỷ lệ phần trăm được cung cấp cho các loại chi phí sau:</span><span class="sxs-lookup"><span data-stu-id="9f6e5-140">If per diem rates vary according to location, for each location, what percentage amount is provided for the following types of expenses:</span></span>

        - <span data-ttu-id="9f6e5-141">Bữa ăn</span><span class="sxs-lookup"><span data-stu-id="9f6e5-141">Meals</span></span>
        - <span data-ttu-id="9f6e5-142">Khách sạn</span><span class="sxs-lookup"><span data-stu-id="9f6e5-142">Hotel</span></span>
        - <span data-ttu-id="9f6e5-143">Chi phí khác</span><span class="sxs-lookup"><span data-stu-id="9f6e5-143">Other expenses</span></span>

### <a name="expense-management-journals-and-accounts"></a><span data-ttu-id="9f6e5-144">Nhật ký và tài khoản quản lý chi phí</span><span class="sxs-lookup"><span data-stu-id="9f6e5-144">Expense management journals and accounts</span></span>

<span data-ttu-id="9f6e5-145">Quản lý chi phí yêu cầu bạn sử dụng nhiều nhật ký và tài khoản.</span><span class="sxs-lookup"><span data-stu-id="9f6e5-145">Expense management requires that you use multiple journals and accounts.</span></span> <span data-ttu-id="9f6e5-146">Ví dụ: bạn phải quyết định xem cùng một tài khoản có được sử dụng cho các xung đột tạm ứng tiền mặt và thẻ tín dụng hay không.</span><span class="sxs-lookup"><span data-stu-id="9f6e5-146">You must decide, for example, whether the same account is used for cash advances and credit card disputes.</span></span>

<span data-ttu-id="9f6e5-147">**Quyết định:**</span><span class="sxs-lookup"><span data-stu-id="9f6e5-147">**Decisions:**</span></span>

- <span data-ttu-id="9f6e5-148">Các báo cáo chi phí đã được phê duyệt được đăng lên nhật ký sổ cái nào?</span><span class="sxs-lookup"><span data-stu-id="9f6e5-148">Which ledger journal are approved expense reports posted to?</span></span>
- <span data-ttu-id="9f6e5-149">Tài khoản nào dùng để ứng trước tiền mặt?</span><span class="sxs-lookup"><span data-stu-id="9f6e5-149">Which account is used for cash advances?</span></span>
- <span data-ttu-id="9f6e5-150">Có nên đăng ứng tiền mặt ngay lập tức không?</span><span class="sxs-lookup"><span data-stu-id="9f6e5-150">Should cash advances be posted immediately?</span></span>

### <a name="payment-methods"></a><span data-ttu-id="9f6e5-151">Phương thức thanh toán</span><span class="sxs-lookup"><span data-stu-id="9f6e5-151">Payment methods</span></span>

<span data-ttu-id="9f6e5-152">Khi bạn cho phép nhân viên thanh toán chi phí thay mặt cho doanh nghiệp của mình, bạn phải xác định các phương thức thanh toán mà nhân viên được phép sử dụng.</span><span class="sxs-lookup"><span data-stu-id="9f6e5-152">When you allow employees to incur expenses on behalf of your business, you must define the payment methods that employees are allowed to use.</span></span> <span data-ttu-id="9f6e5-153">Ví dụ: bạn có thể cho phép nhân viên sử dụng tiền mặt hoặc thẻ tín dụng của công ty.</span><span class="sxs-lookup"><span data-stu-id="9f6e5-153">For example, you might allow employees to use cash or a corporate credit card.</span></span> <span data-ttu-id="9f6e5-154">Bạn cũng có thể cho phép nhân viên sử dụng thẻ tín dụng cá nhân, sau đó hoàn tiền cho nhân viên.</span><span class="sxs-lookup"><span data-stu-id="9f6e5-154">You might also allow employees to use personal credit cards, and then reimburse the employees.</span></span> <span data-ttu-id="9f6e5-155">Bạn phải đưa ra các quyết định sau cho từng phương thức thanh toán mà bạn cho phép.</span><span class="sxs-lookup"><span data-stu-id="9f6e5-155">You must make the following decisions for each payment method that you allow.</span></span>

<span data-ttu-id="9f6e5-156">**Quyết định:**</span><span class="sxs-lookup"><span data-stu-id="9f6e5-156">**Decisions:**</span></span>

- <span data-ttu-id="9f6e5-157">Những phương thức thanh toán nào được phép?</span><span class="sxs-lookup"><span data-stu-id="9f6e5-157">What payment methods are allowed?</span></span>
- <span data-ttu-id="9f6e5-158">Ai sở hữu chi phí phương thức thanh toán?</span><span class="sxs-lookup"><span data-stu-id="9f6e5-158">Who owns the payment method expenses?</span></span>
- <span data-ttu-id="9f6e5-159">Có loại tài khoản bù trừ không?</span><span class="sxs-lookup"><span data-stu-id="9f6e5-159">Is there an offset account type?</span></span> <span data-ttu-id="9f6e5-160">Nếu có một loại tài khoản bù trừ, loại tài khoản đó là gì?</span><span class="sxs-lookup"><span data-stu-id="9f6e5-160">If there is an offset account type, what is it?</span></span>
- <span data-ttu-id="9f6e5-161">Nếu có một tài khoản bù trừ, tài khoản đó là gì?</span><span class="sxs-lookup"><span data-stu-id="9f6e5-161">If there is an offset account, what is the account?</span></span>
- <span data-ttu-id="9f6e5-162">Nếu phương thức thanh toán là thẻ tín dụng, phương thức thanh toán chỉ nên được sử dụng với các giao dịch nhập khẩu?</span><span class="sxs-lookup"><span data-stu-id="9f6e5-162">If the payment method is a credit card, should the payment method be used only with imported transactions?</span></span>

### <a name="expense-categories-and-shared-categories"></a><span data-ttu-id="9f6e5-163">Danh mục chi phí và danh mục chia sẻ</span><span class="sxs-lookup"><span data-stu-id="9f6e5-163">Expense categories and shared categories</span></span>

<span data-ttu-id="9f6e5-164">Khi nhân viên tạo báo cáo chi phí, mỗi khoản chi phí mà họ ghi lại phải được liên kết với một loại chi phí.</span><span class="sxs-lookup"><span data-stu-id="9f6e5-164">When employees create an expense report, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="9f6e5-165">Các danh mục chi phí có nguồn gốc từ các danh mục dùng chung có thể được chia sẻ giữa các pháp nhân trong tổ chức của bạn.</span><span class="sxs-lookup"><span data-stu-id="9f6e5-165">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="9f6e5-166">Các danh mục này cũng có thể được chia sẻ trong Kế toán và quản lý dự án, tùy thuộc vào cách tổ chức của bạn được xác định.</span><span class="sxs-lookup"><span data-stu-id="9f6e5-166">These categories can also be shared in Project management and accounting, depending on the way that your organization is defined.</span></span> <span data-ttu-id="9f6e5-167">Dựa trên định nghĩa về tổ chức của bạn và hướng dẫn từ nhóm thực hiện, bạn phải xác định xem các danh mục được sử dụng trong quản lý Chi phí sẽ chỉ được sử dụng trong Quản lý chi phí hay nên được dùng chung giữa Quản lý dự án và Quản lý chi phí và kế toán.</span><span class="sxs-lookup"><span data-stu-id="9f6e5-167">Based on the definition of your organization and guidance from the implementation team, determine whether the categories that are used in Expense management will be used only in Expense management, or whether they should be shared between Project management and accounting and Expense management.</span></span> <span data-ttu-id="9f6e5-168">Lưu ý rằng các danh mục này có thể được chia sẻ giữa Dự án và chi phí hoặc Dự án và sản xuất, nhưng không được chia sẻ giữa Chi phí và Sản xuất.</span><span class="sxs-lookup"><span data-stu-id="9f6e5-168">Note that these categories can be shared between Project and Expense or Project and Production, but not between Expense and Production.</span></span> <span data-ttu-id="9f6e5-169">Bạn phải đưa ra các quyết định sau cho từng danh mục chi phí.</span><span class="sxs-lookup"><span data-stu-id="9f6e5-169">You must make the following decisions for each expense category.</span></span>

<span data-ttu-id="9f6e5-170">**Quyết định:**</span><span class="sxs-lookup"><span data-stu-id="9f6e5-170">**Decisions:**</span></span>

- <span data-ttu-id="9f6e5-171">Thể loại chi phí là gì?</span><span class="sxs-lookup"><span data-stu-id="9f6e5-171">What is the expense category?</span></span> <span data-ttu-id="9f6e5-172">Ví dụ bao gồm các danh mục cho chuyến bay, khách sạn hoặc số dặm.</span><span class="sxs-lookup"><span data-stu-id="9f6e5-172">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="9f6e5-173">Danh mục chi phí cũng có thể được sử dụng trong Quản lý dự án và kế toán không?</span><span class="sxs-lookup"><span data-stu-id="9f6e5-173">Can the expense category also be used in Project management and accounting?</span></span>
- <span data-ttu-id="9f6e5-174">Loại chi phí là gì?</span><span class="sxs-lookup"><span data-stu-id="9f6e5-174">What is the expense type?</span></span>
- <span data-ttu-id="9f6e5-175">Phương thức thanh toán mặc định cho loại chi phí là gì?</span><span class="sxs-lookup"><span data-stu-id="9f6e5-175">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="9f6e5-176">Các khoản chi trong danh mục chi phí có phải được chia thành từng khoản không?</span><span class="sxs-lookup"><span data-stu-id="9f6e5-176">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="9f6e5-177">Tài khoản chính mặc định cho loại chi phí là gì?</span><span class="sxs-lookup"><span data-stu-id="9f6e5-177">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="9f6e5-178">Nhóm thuế bán hàng mặc định cho danh mục chi phí là gì?</span><span class="sxs-lookup"><span data-stu-id="9f6e5-178">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="9f6e5-179">Các phương thức thanh toán bổ sung có được phép cho loại chi phí không?</span><span class="sxs-lookup"><span data-stu-id="9f6e5-179">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="9f6e5-180">Nếu cho phép các phương thức thanh toán bổ sung, chúng là gì?</span><span class="sxs-lookup"><span data-stu-id="9f6e5-180">If additional payment methods are allowed, what are they?</span></span>
- <span data-ttu-id="9f6e5-181">Có danh mục phụ nào trong danh mục chi phí này không?</span><span class="sxs-lookup"><span data-stu-id="9f6e5-181">Are there subcategories in this expense category?</span></span> <span data-ttu-id="9f6e5-182">Nếu có danh mục phụ, bạn cũng phải đưa ra các quyết định sau:</span><span class="sxs-lookup"><span data-stu-id="9f6e5-182">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="9f6e5-183">Có bất kỳ danh mục phụ nào bị loại trừ khỏi việc thu hồi thuế không?</span><span class="sxs-lookup"><span data-stu-id="9f6e5-183">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="9f6e5-184">Nhóm thuế bán hàng của các danh mục phụ là gì?</span><span class="sxs-lookup"><span data-stu-id="9f6e5-184">What is the item sales tax group of the subcategories?</span></span>

<span data-ttu-id="9f6e5-185">Nếu danh mục chi phí cũng được sử dụng trong Kế toán và quản lý dự án, hãy trả lời các câu hỏi còn lại.</span><span class="sxs-lookup"><span data-stu-id="9f6e5-185">If the expense category is also used in Project management and accounting, answer the remaining questions.</span></span> <span data-ttu-id="9f6e5-186">Nếu không, hãy chuyển sang phần tiếp theo.</span><span class="sxs-lookup"><span data-stu-id="9f6e5-186">Otherwise, move on to the next section.</span></span>

- <span data-ttu-id="9f6e5-187">Tài khoản chi phí nào sẽ được sử dụng cho các khoản chi phí sau?</span><span class="sxs-lookup"><span data-stu-id="9f6e5-187">Which cost accounts will be used for the following expenses?</span></span>

    - <span data-ttu-id="9f6e5-188">Chi phí</span><span class="sxs-lookup"><span data-stu-id="9f6e5-188">Cost</span></span>
    - <span data-ttu-id="9f6e5-189">Phân bổ bảng lương</span><span class="sxs-lookup"><span data-stu-id="9f6e5-189">Payroll allocation</span></span>
    - <span data-ttu-id="9f6e5-190">Giá trị chi phí WIP</span><span class="sxs-lookup"><span data-stu-id="9f6e5-190">WIP-cost value</span></span>
    - <span data-ttu-id="9f6e5-191">Chi phí-mục</span><span class="sxs-lookup"><span data-stu-id="9f6e5-191">Cost-item</span></span>
    - <span data-ttu-id="9f6e5-192">Mục giá trị chi phí WIP</span><span class="sxs-lookup"><span data-stu-id="9f6e5-192">WIP-cost value-item</span></span>
    - <span data-ttu-id="9f6e5-193">Lỗ lũy kế</span><span class="sxs-lookup"><span data-stu-id="9f6e5-193">Accrued loss</span></span>
    - <span data-ttu-id="9f6e5-194">Lỗ lũy kế WIP</span><span class="sxs-lookup"><span data-stu-id="9f6e5-194">WIP-accrued loss</span></span>

- <span data-ttu-id="9f6e5-195">Tài khoản doanh thu nào sẽ được sử dụng cho các khoản sau?</span><span class="sxs-lookup"><span data-stu-id="9f6e5-195">Which revenue accounts will be used for the following?</span></span>

    - <span data-ttu-id="9f6e5-196">Doanh thu đã lập hóa đơn</span><span class="sxs-lookup"><span data-stu-id="9f6e5-196">Invoiced revenue</span></span>
    - <span data-ttu-id="9f6e5-197">Giá trị bán hàng – doanh thu tích lũy</span><span class="sxs-lookup"><span data-stu-id="9f6e5-197">Accrued revenue-sales value</span></span>
    - <span data-ttu-id="9f6e5-198">Giá trị bán hàng WIP</span><span class="sxs-lookup"><span data-stu-id="9f6e5-198">WIP-sales value</span></span>
    - <span data-ttu-id="9f6e5-199">Sản xuất – doanh thu tích lũy</span><span class="sxs-lookup"><span data-stu-id="9f6e5-199">Accrued revenue-production</span></span>
    - <span data-ttu-id="9f6e5-200">Sản xuất WIP</span><span class="sxs-lookup"><span data-stu-id="9f6e5-200">WIP-production</span></span>
    - <span data-ttu-id="9f6e5-201">Lợi nhuận – doanh thu tích lũy</span><span class="sxs-lookup"><span data-stu-id="9f6e5-201">Accrued revenue-profit</span></span>
    - <span data-ttu-id="9f6e5-202">WIP-lợi nhuận</span><span class="sxs-lookup"><span data-stu-id="9f6e5-202">WIP-profit</span></span>
    - <span data-ttu-id="9f6e5-203">Đăng ký – doanh thu tích lũy</span><span class="sxs-lookup"><span data-stu-id="9f6e5-203">Accrued revenue-subscription</span></span>
    - <span data-ttu-id="9f6e5-204">Đăng ký –WIP</span><span class="sxs-lookup"><span data-stu-id="9f6e5-204">WIP-subscription</span></span>

### <a name="taxes"></a><span data-ttu-id="9f6e5-205">Thuế</span><span class="sxs-lookup"><span data-stu-id="9f6e5-205">Taxes</span></span>

<span data-ttu-id="9f6e5-206">Đối với các khoản thuế liên quan đến chi phí, bạn phải xác định những gì được bao gồm hoặc kích hoạt trên báo cáo chi phí.</span><span class="sxs-lookup"><span data-stu-id="9f6e5-206">For expense-related taxes, you must determine what is included or enabled on expense reports.</span></span>

<span data-ttu-id="9f6e5-207">**Quyết định:**</span><span class="sxs-lookup"><span data-stu-id="9f6e5-207">**Decisions:**</span></span>

- <span data-ttu-id="9f6e5-208">Thuế bán hàng có được tính vào chi phí không?</span><span class="sxs-lookup"><span data-stu-id="9f6e5-208">Is sales tax included in the expense amounts?</span></span>
- <span data-ttu-id="9f6e5-209">Có nên kích hoạt thu hồi thuế đối với chi phí không?</span><span class="sxs-lookup"><span data-stu-id="9f6e5-209">Should tax recovery be enabled on expenses?</span></span>

    > [!NOTE]
    > <span data-ttu-id="9f6e5-210">Khi lập kế hoạch sổ cái, nếu bạn quyết định áp dụng các quy tắc thuế sử dụng và thuế bán hàng của Hoa Kỳ, bạn không thể kích hoạt thu hồi thuế đối với chi phí.</span><span class="sxs-lookup"><span data-stu-id="9f6e5-210">When you were planning the general ledger, if you decided to apply U.S. sales tax and use tax rules, you can’t enable tax recovery on expenses.</span></span> <span data-ttu-id="9f6e5-211">(Để áp dụng các quy tắc thuế bán hàng và thuế sử dụng của Hoa Kỳ, hãy đặt tùy chọn **Áp dụng các quy tắc đánh thuế bán hàng** thành **Có**.)</span><span class="sxs-lookup"><span data-stu-id="9f6e5-211">(To apply U.S. sales tax and use tax rules, set the **Apply sales tax taxations rules** option to **Yes**.)</span></span>

## <a name="policies"></a><span data-ttu-id="9f6e5-212">Chính sách</span><span class="sxs-lookup"><span data-stu-id="9f6e5-212">Policies</span></span>

<span data-ttu-id="9f6e5-213">Bằng cách tạo các chính sách báo cáo chi phí, bạn có thể giúp tổ chức của mình tiết kiệm thời gian và tiền bạc khi nhân viên thay mặt tổ chức thanh toán các khoản chi phí.</span><span class="sxs-lookup"><span data-stu-id="9f6e5-213">By creating expense report policies, you can help your organization save time and money when employees incur expenses on its behalf.</span></span> <span data-ttu-id="9f6e5-214">Các chính sách giúp đảm bảo rằng nhân viên chi tiêu trong phạm vi ngân sách, cung cấp tất cả thông tin được yêu cầu và chỉ chi tiền khi họ yêu cầu.</span><span class="sxs-lookup"><span data-stu-id="9f6e5-214">Policies help guarantee that employees stay in budget, provide all required information, and spend money only as they require it.</span></span> <span data-ttu-id="9f6e5-215">Bạn phải đưa ra các quyết định sau cho từng chính sách báo cáo chi phí và từng chính sách phê duyệt báo cáo chi phí mà bạn tạo.</span><span class="sxs-lookup"><span data-stu-id="9f6e5-215">You must make the following decisions for each expense report policy and each expense report approval policy that you create.</span></span>

<span data-ttu-id="9f6e5-216">**Quyết định:**</span><span class="sxs-lookup"><span data-stu-id="9f6e5-216">**Decisions:**</span></span>

- <span data-ttu-id="9f6e5-217">Tên của chính sách là gì?</span><span class="sxs-lookup"><span data-stu-id="9f6e5-217">What is the name of the policy?</span></span>
- <span data-ttu-id="9f6e5-218">Chính sách chi phí là gì?</span><span class="sxs-lookup"><span data-stu-id="9f6e5-218">What is the expense policy for?</span></span>
- <span data-ttu-id="9f6e5-219">Nếu trước đây bạn quyết định cho phép chi phí liên công ty, thì chính sách này sẽ áp dụng cho những công ty nào trong tổ chức của bạn?</span><span class="sxs-lookup"><span data-stu-id="9f6e5-219">If you previously decided to enable intercompany expenses, which companies in your organization will this policy apply to?</span></span>
- <span data-ttu-id="9f6e5-220">Khi nào thì chính sách có hiệu lực?</span><span class="sxs-lookup"><span data-stu-id="9f6e5-220">When does the policy become effective?</span></span>
- <span data-ttu-id="9f6e5-221">Khi nào chính sách hết hạn?</span><span class="sxs-lookup"><span data-stu-id="9f6e5-221">When does the policy expire?</span></span>
- <span data-ttu-id="9f6e5-222">Quy tắc chính sách là gì?</span><span class="sxs-lookup"><span data-stu-id="9f6e5-222">What is the policy rule?</span></span>
- <span data-ttu-id="9f6e5-223">Kết quả của quy tắc chính sách là gì?</span><span class="sxs-lookup"><span data-stu-id="9f6e5-223">What is the outcome of the policy rule?</span></span>
