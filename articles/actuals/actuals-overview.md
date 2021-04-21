---
title: Thực tế
description: Chủ đề này cung cấp thông tin về cách làm việc với giá trị thực tế trong Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 304c51a4e502ad6ecec1fd821e98d6604ddd59ba
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852570"
---
# <a name="actuals"></a><span data-ttu-id="73b62-103">Thực tế</span><span class="sxs-lookup"><span data-stu-id="73b62-103">Actuals</span></span> 

<span data-ttu-id="73b62-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/vật tư không tồn kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="73b62-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="73b62-105">Giá trị thực tế đại diện cho tiến độ tài chính và lịch trình đã được xem xét và phê duyệt trên một dự án.</span><span class="sxs-lookup"><span data-stu-id="73b62-105">Actuals represent the reviewed and approved financial and schedule progress on a project.</span></span> <span data-ttu-id="73b62-106">Chúng được tạo ra do thời gian, chi phí, các mục nhập mức sử dụng vật tư, bút toán và hóa đơn được phê duyệt.</span><span class="sxs-lookup"><span data-stu-id="73b62-106">They are created as a result of approval of time, expense, material usage entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="73b62-107">Dòng nhật ký kế toán và thời gian gửi</span><span class="sxs-lookup"><span data-stu-id="73b62-107">Journal lines and time submission</span></span>

<span data-ttu-id="73b62-108">Để biết thêm thông tin về mục nhập thời gian, hãy xem [Tổng quan về mục nhập thời gian](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="73b62-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="73b62-109">Thời gian và vật tư</span><span class="sxs-lookup"><span data-stu-id="73b62-109">Time and materials</span></span>

<span data-ttu-id="73b62-110">Khi một mục nhập thời gian đã gửi được liên kết với một dự án ánh xạ tới mô tả hợp đồng thời gian và vật tư, hệ thống sẽ tạo ra hai dòng nhật ký kế toán, một dòng cho chi phí và một dòng cho doanh số chưa lập hóa đơn.</span><span class="sxs-lookup"><span data-stu-id="73b62-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="73b62-111">Giá cố định</span><span class="sxs-lookup"><span data-stu-id="73b62-111">Fixed price</span></span>

<span data-ttu-id="73b62-112">Khi một mục nhập thời gian được gửi được liên kết với một dự án được ánh xạ tới một mô tả hợp đồng giá cố định, thì hệ thống sẽ tạo ra một mô tả hợp đồng cho chi phí.</span><span class="sxs-lookup"><span data-stu-id="73b62-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="73b62-113">Giá mặc định</span><span class="sxs-lookup"><span data-stu-id="73b62-113">Default pricing</span></span>

<span data-ttu-id="73b62-114">Logic để tạo giá mặc định nằm trên dòng nhật ký kế toán.</span><span class="sxs-lookup"><span data-stu-id="73b62-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="73b62-115">Các giá trị trường từ mục nhập thời gian được sao chép vào dòng nhật ký kế toán.</span><span class="sxs-lookup"><span data-stu-id="73b62-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="73b62-116">Các giá trị này bao gồm ngày giao dịch, mô tả hợp đồng mà dự án được ánh xạ và kết quả tiền tệ trong bảng giá phù hợp.</span><span class="sxs-lookup"><span data-stu-id="73b62-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="73b62-117">Các trường ảnh hưởng đến giá mặc định, chẳng hạn như **Vai trò** và **Đơn vị nguồn lực** được dùng để xác định mức giá phù hợp trên dòng nhật ký kế toán.</span><span class="sxs-lookup"><span data-stu-id="73b62-117">The fields that affect default pricing, such as **Role** and **Resourcing Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="73b62-118">Bạn có thể thêm trường tùy chỉnh trên mục nhập thời gian.</span><span class="sxs-lookup"><span data-stu-id="73b62-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="73b62-119">Nếu bạn muốn giá trị trường được điền vào giá trị thực tế, hãy tạo trường trong các bảng **Giá trị thực tế** và **Dòng nhật ký kế toán**.</span><span class="sxs-lookup"><span data-stu-id="73b62-119">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="73b62-120">Sử dụng mã tùy chỉnh để điền giá trị trường đã chọn từ Mục nhập thời gian vào Giá trị thực tế thông qua dòng nhật ký kế toán bằng cách sử dụng nguồn gốc giao dịch.</span><span class="sxs-lookup"><span data-stu-id="73b62-120">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="73b62-121">Để biết thêm thông tin về nguồn gốc và kết nối giao dịch, hãy xem [Liên kết Giá trị thực tế với bản ghi gốc](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="73b62-121">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="73b62-122">Các dòng nhật ký kế toán và nộp chi phí cơ bản</span><span class="sxs-lookup"><span data-stu-id="73b62-122">Journal lines and basic expense submission</span></span>

<span data-ttu-id="73b62-123">Để biết thêm thông tin về mục nhập chi phí, hãy xem [Tổng quan về chi phí](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="73b62-123">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="73b62-124">Thời gian và vật tư</span><span class="sxs-lookup"><span data-stu-id="73b62-124">Time and materials</span></span>

<span data-ttu-id="73b62-125">Khi một mục nhập chi phí cơ bản đã gửi đi được liên kết với một dự án ánh xạ tới mô tả hợp đồng thời gian và vật tư, hệ thống sẽ tạo ra hai dòng nhật ký kế toán, một dòng cho chi phí và một dòng cho doanh số chưa lập hóa đơn.</span><span class="sxs-lookup"><span data-stu-id="73b62-125">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="73b62-126">Giá cố định</span><span class="sxs-lookup"><span data-stu-id="73b62-126">Fixed price</span></span>

<span data-ttu-id="73b62-127">Khi một mục nhập chi phí cơ bản đã gửi liên kết với một dự án được ánh xạ tới một mô tả hợp đồng giá cố định, thì hệ thống sẽ tạo một dòng nhật ký kế toán cho chi phí.</span><span class="sxs-lookup"><span data-stu-id="73b62-127">When a submitted basic expense entry is linked to a project that's mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="73b62-128">Giá mặc định</span><span class="sxs-lookup"><span data-stu-id="73b62-128">Default pricing</span></span>

<span data-ttu-id="73b62-129">Logic để nhập giá mặc định cho các chi phí dựa trên danh mục chi phí.</span><span class="sxs-lookup"><span data-stu-id="73b62-129">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="73b62-130">Ngày giao dịch, mô tả hợp đồng mà dự án được ánh xạ tới và tiền tệ đều được dùng để xác định bảng giá phù hợp.</span><span class="sxs-lookup"><span data-stu-id="73b62-130">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="73b62-131">Các trường ảnh hưởng đến giá mặc định, chẳng hạn như **Thể loại giao dịch** và **Đơn vị** được dùng để xác định mức giá phù hợp trên dòng nhật ký kế toán.</span><span class="sxs-lookup"><span data-stu-id="73b62-131">The fields that affect default pricing, such as **Transaction Category** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="73b62-132">Tuy nhiên, điều này chỉ có tác dụng khi phương pháp định giá trong danh sách giá là **Đơn giá**.</span><span class="sxs-lookup"><span data-stu-id="73b62-132">However, this only works when the pricing method in the price list is **Price per unit**.</span></span> <span data-ttu-id="73b62-133">Nếu phương pháp định giá là **Theo chi phí** hoặc **Tăng trên chi phí**, thì giá được nhập khi tạo mục nhập chi phí sẽ được dùng cho chi phí và giá trên dòng nhật ký kế toán về doanh số sẽ được tính theo phương pháp định giá.</span><span class="sxs-lookup"><span data-stu-id="73b62-133">If pricing method is **At cost** or **Markup over cost**, the price entered when the expense entry is created is used for cost and the price on the sales journal line is calculated based on the pricing method.</span></span> 

<span data-ttu-id="73b62-134">Bạn có thể thêm một trường tùy chỉnh vào mục nhập chi phí.</span><span class="sxs-lookup"><span data-stu-id="73b62-134">You can add a custom field on the expense entry.</span></span> <span data-ttu-id="73b62-135">Nếu bạn muốn giá trị trường được điền vào giá trị thực tế, hãy tạo trường trong các bảng **Giá trị thực tế** và **Dòng nhật ký kế toán**.</span><span class="sxs-lookup"><span data-stu-id="73b62-135">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="73b62-136">Sử dụng mã tùy chỉnh để điền giá trị trường đã chọn từ Mục nhập thời gian vào Giá trị thực tế thông qua dòng nhật ký kế toán bằng cách sử dụng nguồn gốc giao dịch.</span><span class="sxs-lookup"><span data-stu-id="73b62-136">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="73b62-137">Để biết thêm thông tin về nguồn gốc và kết nối giao dịch, hãy xem [Liên kết Giá trị thực tế với bản ghi gốc](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="73b62-137">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-material-usage-log-submission"></a><span data-ttu-id="73b62-138">Các dòng nhật ký kế toán và việc gửi nhật ký sử dụng vật tư</span><span class="sxs-lookup"><span data-stu-id="73b62-138">Journal lines and material usage log submission</span></span>

<span data-ttu-id="73b62-139">Để biết thêm thông tin về mục nhập chi phí, hãy xem [Nhật ký sử dụng vật tư](../material/material-usage-log.md).</span><span class="sxs-lookup"><span data-stu-id="73b62-139">For more information about expense entry, see [Material Usage Log](../material/material-usage-log.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="73b62-140">Thời gian và vật tư</span><span class="sxs-lookup"><span data-stu-id="73b62-140">Time and materials</span></span>

<span data-ttu-id="73b62-141">Khi một mục nhập nhật ký sử dụng vật tư đã gửi liên kết với một dự án được ánh xạ tới mô tả hợp đồng thời gian và vật tư, hệ thống sẽ tạo ra hai dòng nhật ký kế toán, một dòng cho chi phí và một dòng cho doanh số chưa lập hóa đơn.</span><span class="sxs-lookup"><span data-stu-id="73b62-141">When a submitted material usage log entry is linked to a project that is mapped to a time and materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="73b62-142">Giá cố định</span><span class="sxs-lookup"><span data-stu-id="73b62-142">Fixed price</span></span>

<span data-ttu-id="73b62-143">Khi một mục nhập nhật ký sử dụng vật tư đã gửi liên kết với một dự án được ánh xạ tới một mô tả hợp đồng giá cố định, thì hệ thống sẽ tạo một dòng nhật ký kế toán cho chi phí.</span><span class="sxs-lookup"><span data-stu-id="73b62-143">When a submitted material usage log entry is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="73b62-144">Giá mặc định</span><span class="sxs-lookup"><span data-stu-id="73b62-144">Default pricing</span></span>

<span data-ttu-id="73b62-145">Logic để nhập giá mặc định cho vật tư dựa trên sự kết hợp giữa sản phẩm và đơn vị.</span><span class="sxs-lookup"><span data-stu-id="73b62-145">The logic for entering default prices for material is based on the product and unit combination.</span></span> <span data-ttu-id="73b62-146">Ngày giao dịch, mô tả hợp đồng mà dự án được ánh xạ tới và tiền tệ đều được dùng để xác định bảng giá phù hợp.</span><span class="sxs-lookup"><span data-stu-id="73b62-146">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="73b62-147">Các trường ảnh hưởng đến giá mặc định, chẳng hạn như **ID sản phẩm** và **Đơn vị** được dùng để xác định mức giá phù hợp trên dòng nhật ký kế toán.</span><span class="sxs-lookup"><span data-stu-id="73b62-147">The fields that affect default pricing, such as **Product ID** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="73b62-148">Tuy nhiên, điều này chỉ áp dụng cho các sản phẩm trong danh mục.</span><span class="sxs-lookup"><span data-stu-id="73b62-148">However, this only works for catalog products.</span></span> <span data-ttu-id="73b62-149">Đối với sản phẩm chọn thêm, giá được nhập khi tạo mục nhập nhật ký sử dụng vật tư được dùng cho chi phí và giá bán trên các dòng nhật ký kế toán.</span><span class="sxs-lookup"><span data-stu-id="73b62-149">For write-in products, the price entered when the material usage log entry is created is used for cost and sales price on the journal lines.</span></span> 

<span data-ttu-id="73b62-150">Bạn có thể thêm một trường tùy chỉnh vào mục nhập **Nhật ký sử dụng vật tư**.</span><span class="sxs-lookup"><span data-stu-id="73b62-150">You can add a custom field on the **Material Usage Log** entry.</span></span> <span data-ttu-id="73b62-151">Nếu bạn muốn giá trị trường được điền vào giá trị thực tế, hãy tạo trường trong các bảng **Giá trị thực tế** và **Dòng nhật ký kế toán**.</span><span class="sxs-lookup"><span data-stu-id="73b62-151">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="73b62-152">Sử dụng mã tùy chỉnh để điền giá trị trường đã chọn từ Mục nhập thời gian vào Giá trị thực tế thông qua dòng nhật ký kế toán bằng cách sử dụng nguồn gốc giao dịch.</span><span class="sxs-lookup"><span data-stu-id="73b62-152">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="73b62-153">Để biết thêm thông tin về nguồn gốc và kết nối giao dịch, hãy xem [Liên kết Giá trị thực tế với bản ghi gốc](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="73b62-153">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="73b62-154">Sử dụng bút toán để ghi lại chi phí</span><span class="sxs-lookup"><span data-stu-id="73b62-154">Use entry journals to record costs</span></span>

<span data-ttu-id="73b62-155">Bạn có thể sử dụng bút toán để ghi lại chi phí hoặc doanh thu trong lớp giao dịch thuế, chi phí, thời gian, phí hoặc vật tư.</span><span class="sxs-lookup"><span data-stu-id="73b62-155">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="73b62-156">Có thể sử dụng nhật ký cho các mục đích sau:</span><span class="sxs-lookup"><span data-stu-id="73b62-156">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="73b62-157">Di chuyển các giá trị thực tế của giao dịch từ một hệ thống khác sang Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="73b62-157">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="73b62-158">Ghi lại chi phí đã xảy ra trong hệ thống khác.</span><span class="sxs-lookup"><span data-stu-id="73b62-158">Record costs that occurred in another system.</span></span> <span data-ttu-id="73b62-159">Các chi phí này có thể bao gồm chi phí mua sắm hoặc chi phí thầu phụ.</span><span class="sxs-lookup"><span data-stu-id="73b62-159">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="73b62-160">Ứng dụng không xác nhận dòng nhật ký kế toán hoặc giá cả liên quan được nhập trên dòng nhật ký kế toán.</span><span class="sxs-lookup"><span data-stu-id="73b62-160">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="73b62-161">Do đó, chỉ người dùng có nhận thức đầy đủ về tác động kế toán mà các giá trị thực tế có đối với dự án mới được sử dụng bút toán để tạo các giá trị thực tế.</span><span class="sxs-lookup"><span data-stu-id="73b62-161">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="73b62-162">Do tác động của loại nhật ký này, bạn nên cẩn thận chọn người có quyền truy cập để tạo bút toán.</span><span class="sxs-lookup"><span data-stu-id="73b62-162">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>

## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="73b62-163">Ghi lại thực tế dựa trên sự kiện dự án</span><span class="sxs-lookup"><span data-stu-id="73b62-163">Record actuals based on project events</span></span>

<span data-ttu-id="73b62-164">Project Operations ghi lại các giao dịch tài chính xảy ra trong một dự án.</span><span class="sxs-lookup"><span data-stu-id="73b62-164">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="73b62-165">Các giao dịch này được ghi lại là thực tế.</span><span class="sxs-lookup"><span data-stu-id="73b62-165">These transactions are recorded as actuals.</span></span> <span data-ttu-id="73b62-166">Các bảng sau đây hiển thị các loại thực tế khác nhau được tạo, phụ thuộc vào việc dự án là dự án thời gian và vật tư hay giá cố định, ở giai đoạn trước khi bán hàng hay là dự án nội bộ.</span><span class="sxs-lookup"><span data-stu-id="73b62-166">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="73b62-167">Tài nguyên thuộc về cùng một đơn vị tổ chức như đơn vị hợp đồng của dự án</span><span class="sxs-lookup"><span data-stu-id="73b62-167">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="73b62-168">Sự kiện</span><span class="sxs-lookup"><span data-stu-id="73b62-168">Event</span></span></th>
<th colspan="4"><span data-ttu-id="73b62-169">Dự án có thể lập hóa đơn hoặc đã bán</span><span class="sxs-lookup"><span data-stu-id="73b62-169">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="73b62-170">Dự án trong giai đoạn trước khi bán</span><span class="sxs-lookup"><span data-stu-id="73b62-170">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="73b62-171">Dự án nội bộ</span><span class="sxs-lookup"><span data-stu-id="73b62-171">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="73b62-172">Thời gian và vật tư</span><span class="sxs-lookup"><span data-stu-id="73b62-172">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="73b62-173">Giá cố định</span><span class="sxs-lookup"><span data-stu-id="73b62-173">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="73b62-174">Thực tế</span><span class="sxs-lookup"><span data-stu-id="73b62-174">Actuals</span></span></th>
<th><span data-ttu-id="73b62-175">Loại tiền giao dịch</span><span class="sxs-lookup"><span data-stu-id="73b62-175">Transaction currency</span></span></th>
<th><span data-ttu-id="73b62-176">Giá cố định</span><span class="sxs-lookup"><span data-stu-id="73b62-176">Fixed price</span></span></th>
<th><span data-ttu-id="73b62-177">Loại tiền giao dịch</span><span class="sxs-lookup"><span data-stu-id="73b62-177">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73b62-178">Mục nhập thời gian được tạo.</span><span class="sxs-lookup"><span data-stu-id="73b62-178">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="73b62-179">Không có hoạt động trong thực thể Thực tế</span><span class="sxs-lookup"><span data-stu-id="73b62-179">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73b62-180">Mục nhập thời gian được gửi.</span><span class="sxs-lookup"><span data-stu-id="73b62-180">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="73b62-181">Không có hoạt động trong thực thể Thực tế</span><span class="sxs-lookup"><span data-stu-id="73b62-181">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="73b62-182">Thời gian được phê duyệt và số giờ có thể lập hóa đơn sẽ không thay đổi hay tăng trong quá trình phê duyệt.</span><span class="sxs-lookup"><span data-stu-id="73b62-182">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="73b62-183">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="73b62-183">Cost actual</span></span></td>
<td><span data-ttu-id="73b62-184">Tiền tệ của đơn vị hợp đồng</span><span class="sxs-lookup"><span data-stu-id="73b62-184">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="73b62-185">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="73b62-185">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="73b62-186">Tiền tệ của đơn vị hợp đồng</span><span class="sxs-lookup"><span data-stu-id="73b62-186">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="73b62-187">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="73b62-187">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="73b62-188">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="73b62-188">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73b62-189">Thực tế bán hàng chưa lập hóa đơn – Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="73b62-189">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="73b62-190">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="73b62-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="73b62-191">Thời gian được phê duyệt và số giờ có thể lập hóa đơn giảm trong quá trình phê duyệt.</span><span class="sxs-lookup"><span data-stu-id="73b62-191">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="73b62-192">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="73b62-192">Cost actual</span></span></td>
<td><span data-ttu-id="73b62-193">Tiền tệ của đơn vị hợp đồng</span><span class="sxs-lookup"><span data-stu-id="73b62-193">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="73b62-194">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="73b62-194">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="73b62-195">Tiền tệ của đơn vị hợp đồng</span><span class="sxs-lookup"><span data-stu-id="73b62-195">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="73b62-196">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="73b62-196">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="73b62-197">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="73b62-197">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73b62-198">Thực tế bán hàng chưa lập hóa đơn – Có thể tính phí cho số lượng mới</span><span class="sxs-lookup"><span data-stu-id="73b62-198">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="73b62-199">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="73b62-199">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73b62-200">Thực tế bán hàng chưa lập hóa đơn – Không thể tính phí cho phần chênh lệch</span><span class="sxs-lookup"><span data-stu-id="73b62-200">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="73b62-201">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="73b62-201">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="73b62-202">Hóa đơn được xác nhận, số giờ có thể lập hóa đơn sẽ không thay đổi hay tăng.</span><span class="sxs-lookup"><span data-stu-id="73b62-202">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="73b62-203">Đảo ngược bán hàng chưa lập hóa đơn</span><span class="sxs-lookup"><span data-stu-id="73b62-203">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="73b62-204">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="73b62-204">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="73b62-205">Doanh số đã lập hóa đơn cho mốc quan trọng</span><span class="sxs-lookup"><span data-stu-id="73b62-205">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="73b62-206">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="73b62-206">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="73b62-207">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="73b62-207">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="73b62-208">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="73b62-208">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73b62-209">Doanh số đã lập hóa đơn</span><span class="sxs-lookup"><span data-stu-id="73b62-209">Billed sales</span></span></td>
<td><span data-ttu-id="73b62-210">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="73b62-210">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="73b62-211">Hóa đơn được xác nhận, số giờ có thể lập hóa đơn giảm.</span><span class="sxs-lookup"><span data-stu-id="73b62-211">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="73b62-212">Đảo ngược bán hàng chưa lập hóa đơn</span><span class="sxs-lookup"><span data-stu-id="73b62-212">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="73b62-213">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="73b62-213">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="73b62-214">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="73b62-214">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="73b62-215">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="73b62-215">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="73b62-216">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="73b62-216">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="73b62-217">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="73b62-217">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73b62-218">Doanh số chưa lập hóa đơn – Có thể tính phí cho số lượng mới</span><span class="sxs-lookup"><span data-stu-id="73b62-218">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="73b62-219">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="73b62-219">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73b62-220">Doanh số chưa lập hóa đơn – Không thể tính phí cho phần chênh lệch</span><span class="sxs-lookup"><span data-stu-id="73b62-220">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="73b62-221">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="73b62-221">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="73b62-222">Hóa đơn được sửa để tăng số lượng có thể tính phí.</span><span class="sxs-lookup"><span data-stu-id="73b62-222">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="73b62-223">Doanh số đã tính phí – Đảo ngược</span><span class="sxs-lookup"><span data-stu-id="73b62-223">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="73b62-224">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="73b62-224">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="73b62-225">Đảo ngược doanh số đã lập hóa đơn cho mốc quan trọng</span><span class="sxs-lookup"><span data-stu-id="73b62-225">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="73b62-226">Thay đổi trạng thái mốc quan trọng từ <strong>Đã lập hóa đơn</strong> thành <strong>Sẵn sàng lập hóa đơn</strong></span><span class="sxs-lookup"><span data-stu-id="73b62-226">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="73b62-227">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="73b62-227">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="73b62-228">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="73b62-228">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="73b62-229">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="73b62-229">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73b62-230">Doanh số đã lập hóa đơn</span><span class="sxs-lookup"><span data-stu-id="73b62-230">Billed sales</span></span></td>
<td><span data-ttu-id="73b62-231">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="73b62-231">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="73b62-232">Hóa đơn được sửa để giảm số lượng có thể tính phí.</span><span class="sxs-lookup"><span data-stu-id="73b62-232">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="73b62-233">Doanh số đã tính phí – Đảo ngược</span><span class="sxs-lookup"><span data-stu-id="73b62-233">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="73b62-234">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="73b62-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73b62-235">Doanh số chưa lập hóa đơn cho số lượng mới</span><span class="sxs-lookup"><span data-stu-id="73b62-235">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="73b62-236">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="73b62-236">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73b62-237">Doanh số chưa lập hóa đơn – Có thể tính phí cho phần chênh lệch</span><span class="sxs-lookup"><span data-stu-id="73b62-237">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="73b62-238">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="73b62-238">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="73b62-239">Tài nguyên thuộc về một đơn vị tổ chức khác với đơn vị hợp đồng của dự án</span><span class="sxs-lookup"><span data-stu-id="73b62-239">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="73b62-240">Sự kiện</span><span class="sxs-lookup"><span data-stu-id="73b62-240">Event</span></span></th>
<th colspan="4"><span data-ttu-id="73b62-241">Dự án có thể lập hóa đơn hoặc đã bán</span><span class="sxs-lookup"><span data-stu-id="73b62-241">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="73b62-242">Dự án trong giai đoạn trước khi bán</span><span class="sxs-lookup"><span data-stu-id="73b62-242">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="73b62-243">Dự án nội bộ</span><span class="sxs-lookup"><span data-stu-id="73b62-243">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="73b62-244">Thời gian và vật tư</span><span class="sxs-lookup"><span data-stu-id="73b62-244">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="73b62-245">Giá cố định</span><span class="sxs-lookup"><span data-stu-id="73b62-245">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="73b62-246">Thực tế</span><span class="sxs-lookup"><span data-stu-id="73b62-246">Actuals</span></span></th>
<th><span data-ttu-id="73b62-247">Loại tiền giao dịch</span><span class="sxs-lookup"><span data-stu-id="73b62-247">Transaction currency</span></span></th>
<th><span data-ttu-id="73b62-248">Giá cố định</span><span class="sxs-lookup"><span data-stu-id="73b62-248">Fixed price</span></span></th>
<th><span data-ttu-id="73b62-249">Loại tiền giao dịch</span><span class="sxs-lookup"><span data-stu-id="73b62-249">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="73b62-250">Mục nhập thời gian được tạo.</span><span class="sxs-lookup"><span data-stu-id="73b62-250">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="73b62-251">Không có hoạt động trong thực thể Thực tế</span><span class="sxs-lookup"><span data-stu-id="73b62-251">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73b62-252">Mục nhập thời gian được gửi.</span><span class="sxs-lookup"><span data-stu-id="73b62-252">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="73b62-253">Không có hoạt động trong thực thể Thực tế</span><span class="sxs-lookup"><span data-stu-id="73b62-253">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="73b62-254">Thời gian được phê duyệt và số giờ có thể lập hóa đơn sẽ không thay đổi hay tăng trong quá trình phê duyệt.</span><span class="sxs-lookup"><span data-stu-id="73b62-254">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="73b62-255">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="73b62-255">Cost actual</span></span></td>
<td><span data-ttu-id="73b62-256">Tiền tệ của đơn vị hợp đồng</span><span class="sxs-lookup"><span data-stu-id="73b62-256">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="73b62-257">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="73b62-257">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="73b62-258">Tiền tệ của đơn vị hợp đồng</span><span class="sxs-lookup"><span data-stu-id="73b62-258">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="73b62-259">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="73b62-259">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="73b62-260">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="73b62-260">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73b62-261">Thực tế bán hàng chưa lập hóa đơn – Có thể tính phí</span><span class="sxs-lookup"><span data-stu-id="73b62-261">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="73b62-262">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="73b62-262">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73b62-263">Chi phí đơn vị nguồn lực</span><span class="sxs-lookup"><span data-stu-id="73b62-263">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="73b62-264">Tiền tệ đơn vị nguồn lực</span><span class="sxs-lookup"><span data-stu-id="73b62-264">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73b62-265">Bán hàng liên tổ chức</span><span class="sxs-lookup"><span data-stu-id="73b62-265">Interorganizational sales</span></span></td>
<td><span data-ttu-id="73b62-266">Tiền tệ của đơn vị hợp đồng</span><span class="sxs-lookup"><span data-stu-id="73b62-266">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="73b62-267">Thời gian được phê duyệt và số giờ có thể lập hóa đơn giảm trong quá trình phê duyệt.</span><span class="sxs-lookup"><span data-stu-id="73b62-267">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="73b62-268">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="73b62-268">Cost actual</span></span></td>
<td><span data-ttu-id="73b62-269">Tiền tệ của đơn vị hợp đồng</span><span class="sxs-lookup"><span data-stu-id="73b62-269">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="73b62-270">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="73b62-270">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="73b62-271">Tiền tệ của đơn vị hợp đồng</span><span class="sxs-lookup"><span data-stu-id="73b62-271">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="73b62-272">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="73b62-272">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="73b62-273">Thực tế chi phí</span><span class="sxs-lookup"><span data-stu-id="73b62-273">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73b62-274">Chi phí đơn vị nguồn lực</span><span class="sxs-lookup"><span data-stu-id="73b62-274">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="73b62-275">Tiền tệ đơn vị nguồn lực</span><span class="sxs-lookup"><span data-stu-id="73b62-275">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73b62-276">Bán hàng liên tổ chức</span><span class="sxs-lookup"><span data-stu-id="73b62-276">Interorganizational sales</span></span></td>
<td><span data-ttu-id="73b62-277">Tiền tệ của đơn vị hợp đồng</span><span class="sxs-lookup"><span data-stu-id="73b62-277">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73b62-278">Thực tế bán hàng chưa lập hóa đơn – Có thể tính phí cho số lượng mới</span><span class="sxs-lookup"><span data-stu-id="73b62-278">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="73b62-279">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="73b62-279">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73b62-280">Thực tế bán hàng chưa lập hóa đơn – Không thể tính phí cho phần chênh lệch</span><span class="sxs-lookup"><span data-stu-id="73b62-280">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="73b62-281">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="73b62-281">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="73b62-282">Hóa đơn được xác nhận, số giờ có thể lập hóa đơn sẽ không thay đổi hay tăng.</span><span class="sxs-lookup"><span data-stu-id="73b62-282">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="73b62-283">Đảo ngược bán hàng chưa lập hóa đơn</span><span class="sxs-lookup"><span data-stu-id="73b62-283">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="73b62-284">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="73b62-284">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="73b62-285">Doanh số đã lập hóa đơn cho mốc quan trọng</span><span class="sxs-lookup"><span data-stu-id="73b62-285">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="73b62-286">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="73b62-286">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="73b62-287">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="73b62-287">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="73b62-288">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="73b62-288">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73b62-289">Doanh số đã lập hóa đơn</span><span class="sxs-lookup"><span data-stu-id="73b62-289">Billed sales</span></span></td>
<td><span data-ttu-id="73b62-290">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="73b62-290">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="73b62-291">Hóa đơn được xác nhận, số giờ có thể lập hóa đơn giảm.</span><span class="sxs-lookup"><span data-stu-id="73b62-291">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="73b62-292">Đảo ngược bán hàng chưa lập hóa đơn</span><span class="sxs-lookup"><span data-stu-id="73b62-292">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="73b62-293">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="73b62-293">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="73b62-294">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="73b62-294">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="73b62-295">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="73b62-295">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="73b62-296">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="73b62-296">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="73b62-297">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="73b62-297">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73b62-298">Doanh số chưa lập hóa đơn – Có thể tính phí cho số lượng mới</span><span class="sxs-lookup"><span data-stu-id="73b62-298">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="73b62-299">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="73b62-299">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73b62-300">Doanh số chưa lập hóa đơn – Không thể tính phí cho phần chênh lệch</span><span class="sxs-lookup"><span data-stu-id="73b62-300">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="73b62-301">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="73b62-301">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="73b62-302">Hóa đơn được sửa để tăng số lượng có thể tính phí.</span><span class="sxs-lookup"><span data-stu-id="73b62-302">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="73b62-303">Doanh số đã tính phí – Đảo ngược</span><span class="sxs-lookup"><span data-stu-id="73b62-303">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="73b62-304">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="73b62-304">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="73b62-305">Đảo ngược doanh số đã lập hóa đơn cho mốc quan trọng</span><span class="sxs-lookup"><span data-stu-id="73b62-305">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="73b62-306">Thay đổi trạng thái mốc quan trọng từ <strong>Đã lập hóa đơn</strong> thành <strong>Sẵn sàng lập hóa đơn</strong></span><span class="sxs-lookup"><span data-stu-id="73b62-306">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="73b62-307">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="73b62-307">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="73b62-308">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="73b62-308">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="73b62-309">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="73b62-309">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73b62-310">Doanh số đã lập hóa đơn</span><span class="sxs-lookup"><span data-stu-id="73b62-310">Billed sales</span></span></td>
<td><span data-ttu-id="73b62-311">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="73b62-311">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="73b62-312">Hóa đơn được sửa để giảm số lượng có thể tính phí.</span><span class="sxs-lookup"><span data-stu-id="73b62-312">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="73b62-313">Doanh số đã tính phí – Đảo ngược</span><span class="sxs-lookup"><span data-stu-id="73b62-313">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="73b62-314">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="73b62-314">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73b62-315">Doanh số chưa lập hóa đơn cho số lượng mới</span><span class="sxs-lookup"><span data-stu-id="73b62-315">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="73b62-316">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="73b62-316">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="73b62-317">Doanh số chưa lập hóa đơn – Có thể tính phí cho phần chênh lệch</span><span class="sxs-lookup"><span data-stu-id="73b62-317">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="73b62-318">Tiền tệ hợp đồng dự án</span><span class="sxs-lookup"><span data-stu-id="73b62-318">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
