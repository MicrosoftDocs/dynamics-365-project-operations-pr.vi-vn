---
title: Đồng bộ hóa ước tính dự án trực tiếp từ Project Service Automation sang Finance and Operations
description: Chủ đề này mô tả các mẫu và nhiệm vụ cơ bản dùng để đồng bộ hóa trực tiếp các ước tính giờ dự án và ước tính chi phí dự án trực tiếp từ Microsoft Dynamics 365 Project Service Automation sang Dynamics 365 Finance.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 336de474c859d30d1ec07ae34bf0c3d578faeef1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087236"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="81116-103">Đồng bộ hóa ước tính dự án trực tiếp từ Project Service Automation sang Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="81116-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="81116-104">Chủ đề này mô tả các mẫu và nhiệm vụ cơ bản dùng để đồng bộ hóa trực tiếp các ước tính giờ dự án và ước tính chi phí dự án trực tiếp từ Dynamics 365 Project Service Automation sang Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="81116-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="81116-105">Tính năng tích hợp nhiệm vụ dự án, thể loại giao dịch chi phí, ước tính giờ, ước tính chi phí và khóa chức năng có sẵn trong phiên bản 8.0.</span><span class="sxs-lookup"><span data-stu-id="81116-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in version 8.0.</span></span>
> - <span data-ttu-id="81116-106">Tùy chọn tích hợp giá trị thực tế có sẵn từ phiên bản 8.0.1.</span><span class="sxs-lookup"><span data-stu-id="81116-106">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="81116-107">Luồng dữ liệu cho Project Service Automation sang Finance</span><span class="sxs-lookup"><span data-stu-id="81116-107">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="81116-108">Giải pháp tích hợp Project Service Automation sang Finance sử dụng tính năng Tích hợp dữ liệu để đồng bộ hóa dữ liệu giữa các phiên bản của Project Service Automation và Finance.</span><span class="sxs-lookup"><span data-stu-id="81116-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="81116-109">Các mẫu tích hợp có sẵn với tính năng Tích hợp dữ liệu sẽ tạo ra luồng dữ liệu về các các ước tính số giờ dự án và ước tính chi phí dự án từ Project Service Automation sang Finance.</span><span class="sxs-lookup"><span data-stu-id="81116-109">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance.</span></span>

<span data-ttu-id="81116-110">Hình minh họa sau đây cho thấy cách dữ liệu được đồng bộ hóa giữa Project Service Automation và Finance.</span><span class="sxs-lookup"><span data-stu-id="81116-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="81116-111">[![Luồng dữ liệu cho phần tích hợp Project Service Automation với Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="81116-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="81116-112">Ước tính số giờ dự án</span><span class="sxs-lookup"><span data-stu-id="81116-112">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="81116-113">Mẫu và nhiệm vụ</span><span class="sxs-lookup"><span data-stu-id="81116-113">Template and tasks</span></span>

<span data-ttu-id="81116-114">Để truy cập các mẫu có sẵn, trong trung tâm quản trị Microsoft Power Apps, chọn **Dự án** và sau đó, ở góc trên bên phải, chọn **Dự án mới** để chọn các mẫu công khai.</span><span class="sxs-lookup"><span data-stu-id="81116-114">To access the available templates, in the Microsoft Power Apps admin center, select **Projects** , and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="81116-115">Mẫu sau và các nhiệm vụ cơ bản được sử dụng để đồng bộ hóa ước tính giờ dự án từ Project Service Automation sang Finance:</span><span class="sxs-lookup"><span data-stu-id="81116-115">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="81116-116">**Tên mẫu trong Tích hợp dữ liệu:** Ước tính giờ dự án (PSA sang Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="81116-116">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="81116-117">**Tên của nhiệm vụ trong dự án:**</span><span class="sxs-lookup"><span data-stu-id="81116-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="81116-118">Các mối quan hệ giao dịch</span><span class="sxs-lookup"><span data-stu-id="81116-118">Transaction relationships</span></span>
    - <span data-ttu-id="81116-119">Ước tính chi phí</span><span class="sxs-lookup"><span data-stu-id="81116-119">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="81116-120">Bộ thực thể</span><span class="sxs-lookup"><span data-stu-id="81116-120">Entity set</span></span>

| <span data-ttu-id="81116-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="81116-121">Project Service Automation</span></span> | <span data-ttu-id="81116-122">Tài chính</span><span class="sxs-lookup"><span data-stu-id="81116-122">Finance</span></span>                                       |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="81116-123">Nhiệm vụ dự án</span><span class="sxs-lookup"><span data-stu-id="81116-123">Project tasks</span></span>              | <span data-ttu-id="81116-124">Thực thể tích hợp cho ước tính giờ dự án</span><span class="sxs-lookup"><span data-stu-id="81116-124">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="81116-125">Luồng thực thể</span><span class="sxs-lookup"><span data-stu-id="81116-125">Entity flow</span></span>

<span data-ttu-id="81116-126">Ước tính giờ dự án được quản lý trong Project Service Automation và được đồng bộ hóa với Finance dưới dạng dự báo giờ dự án.</span><span class="sxs-lookup"><span data-stu-id="81116-126">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="81116-127">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="81116-127">Prerequisites</span></span>

<span data-ttu-id="81116-128">Trước khi đồng bộ hóa ước tính giờ dự án có thể xảy ra, bạn phải đồng bộ hóa dự án, nhiệm vụ dự án và thể loại giao dịch chi phí dự án.</span><span class="sxs-lookup"><span data-stu-id="81116-128">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="81116-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="81116-129">Power Query</span></span>

<span data-ttu-id="81116-130">Trong mẫu ước tính giờ dự án, bạn phải sử dụng Microsoft Power Query dành cho Excel để hoàn thành các nhiệm vụ sau:</span><span class="sxs-lookup"><span data-stu-id="81116-130">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="81116-131">Thiết lập ID mô hình dự báo mặc định sẽ được sử dụng khi tùy chọn tích hợp tạo dự báo giờ mới.</span><span class="sxs-lookup"><span data-stu-id="81116-131">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="81116-132">Lọc ra bất kỳ bản ghi nguồn lực cụ thể nào trong nhiệm vụ sẽ không tích hợp được vào dự báo giờ.</span><span class="sxs-lookup"><span data-stu-id="81116-132">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="81116-133">Lọc ra bất kỳ hàng thể loại giao dịch trống nào.</span><span class="sxs-lookup"><span data-stu-id="81116-133">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="81116-134">Không hoàn thành nhiệm vụ này có thể dẫn đến việc dự báo giờ không chính xác.</span><span class="sxs-lookup"><span data-stu-id="81116-134">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="81116-135">Thiết lập ID mô hình dự báo mặc định</span><span class="sxs-lookup"><span data-stu-id="81116-135">Set the default forecast model ID</span></span>

<span data-ttu-id="81116-136">Để cập nhật ID mô hình dự báo mặc định trong mẫu, hãy bấm vào mũi tên **Bản đồ** để mở phần ánh xạ.</span><span class="sxs-lookup"><span data-stu-id="81116-136">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="81116-137">Sau đó, chọn liên kết **Truy vấn nâng cao và lọc**.</span><span class="sxs-lookup"><span data-stu-id="81116-137">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="81116-138">Nếu bạn đang sử dụng mẫu Ước tính giờ dự án mặc định (PSA sang Fin and Ops) mặc định, hãy chọn **Điều kiện đã chèn** trong danh sách **Các bước được áp dụng**.</span><span class="sxs-lookup"><span data-stu-id="81116-138">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="81116-139">Trong mục nhập **Hàm** , thay **O\_forecast** bằng tên của ID mô hình dự đoán sẽ dùng với tùy chọn tích hợp.</span><span class="sxs-lookup"><span data-stu-id="81116-139">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="81116-140">Mẫu mặc định có ID mô hình dự báo từ dữ liệu demo.</span><span class="sxs-lookup"><span data-stu-id="81116-140">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="81116-141">Nếu bạn đang tạo một mẫu mới, bạn phải thêm cột này.</span><span class="sxs-lookup"><span data-stu-id="81116-141">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="81116-142">Trong Power Query, chọn **Thêm cột điều kiện** và nhập tên của cột mới, như **ID mô hình**.</span><span class="sxs-lookup"><span data-stu-id="81116-142">In Power Query, select **Add Conditional Column** , and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="81116-143">Nhập điều kiện cho cột, trong đó, nếu nhiệm vụ dự án không phải là null, thì \<enter the forecast model ID\>; nếu không thì nhập null.</span><span class="sxs-lookup"><span data-stu-id="81116-143">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="81116-144">Lọc ra các bản ghi dành riêng cho nguồn lực</span><span class="sxs-lookup"><span data-stu-id="81116-144">Filter out resource-specific records</span></span>

<span data-ttu-id="81116-145">Mẫu ước tính giờ dự án (PSA sang Fin và Ops) có bộ lọc mặc định nhằm loại bỏ bất kỳ bản ghi dành riêng cho nguồn lực nào.</span><span class="sxs-lookup"><span data-stu-id="81116-145">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="81116-146">Nếu bạn tạo mẫu của riêng mình, bạn phải thêm bộ lọc này.</span><span class="sxs-lookup"><span data-stu-id="81116-146">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="81116-147">Chọn liên kết **Truy vấn nâng cao và lọc** để lọc trên cột **msdyn\_islinetask** sao cho chỉ bản ghi **False** được bao gồm.</span><span class="sxs-lookup"><span data-stu-id="81116-147">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="81116-148">Lọc ra các hàng thể loại giao dịch trống</span><span class="sxs-lookup"><span data-stu-id="81116-148">Filter out empty transaction category rows</span></span>

<span data-ttu-id="81116-149">Bạn phải thêm bộ lọc để loại bỏ bất kỳ hàng nào có thể loại giao dịch trống.</span><span class="sxs-lookup"><span data-stu-id="81116-149">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="81116-150">Tác vụ này là bắt buộc, bất kể bạn đang sử dụng mẫu mặc định hay tạo mẫu của riêng mình.</span><span class="sxs-lookup"><span data-stu-id="81116-150">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="81116-151">Bộ lọc này loại bỏ bất kỳ hàng tóm tắt nào ra khỏi Project Service Automation có thể khiến dự báo giờ trong Finance không chính xác.</span><span class="sxs-lookup"><span data-stu-id="81116-151">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance to be incorrect.</span></span> <span data-ttu-id="81116-152">Chọn liên kết **Truy vấn nâng cao và lọc** để lọc các bản ghi null trong cột **msdyn\_transactioncategory\_value**.</span><span class="sxs-lookup"><span data-stu-id="81116-152">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="81116-153">Ánh xạ mẫu trong tích hợp dữ liệu</span><span class="sxs-lookup"><span data-stu-id="81116-153">Template mapping in Data integration</span></span>

<span data-ttu-id="81116-154">Hình sau đây minh họa một ví dụ về việc ánh xạ nhiệm vụ mẫu trong Tích hợp dữ liệu.</span><span class="sxs-lookup"><span data-stu-id="81116-154">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="81116-155">Tùy chọn ánh xạ hiển thị thông tin trường sẽ được đồng bộ hóa từ Project Service Automation sang Finance.</span><span class="sxs-lookup"><span data-stu-id="81116-155">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="81116-156">[![Ánh xạ nhiệm vụ mẫu trong tích hợp dữ liệu](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="81116-156">[![Template task mapping in data integration](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="81116-157">Ước tính chi phí dự án</span><span class="sxs-lookup"><span data-stu-id="81116-157">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="81116-158">Mẫu và nhiệm vụ</span><span class="sxs-lookup"><span data-stu-id="81116-158">Template and tasks</span></span>

<span data-ttu-id="81116-159">Mẫu sau và các nhiệm vụ cơ bản được sử dụng để đồng bộ hóa ước tính chi phí dự án từ Project Service Automation sang Finance:</span><span class="sxs-lookup"><span data-stu-id="81116-159">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="81116-160">**Tên mẫu trong Tích hợp dữ liệu:** Ước tính chi phí dự án (PSA sang Fin và Ops)</span><span class="sxs-lookup"><span data-stu-id="81116-160">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="81116-161">**Tên của nhiệm vụ trong dự án:**</span><span class="sxs-lookup"><span data-stu-id="81116-161">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="81116-162">Các mối quan hệ giao dịch</span><span class="sxs-lookup"><span data-stu-id="81116-162">Transaction relationships</span></span> 
    - <span data-ttu-id="81116-163">Ước tính chi phí</span><span class="sxs-lookup"><span data-stu-id="81116-163">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="81116-164">Bộ thực thể</span><span class="sxs-lookup"><span data-stu-id="81116-164">Entity set</span></span>

| <span data-ttu-id="81116-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="81116-165">Project Service Automation</span></span> | <span data-ttu-id="81116-166">Tài chính</span><span class="sxs-lookup"><span data-stu-id="81116-166">Finance</span></span>                                                  |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="81116-167">Kết nối Giao dịch</span><span class="sxs-lookup"><span data-stu-id="81116-167">Transaction Connections</span></span>    | <span data-ttu-id="81116-168">Thực thể tích hợp cho các mối quan hệ giao dịch dự án</span><span class="sxs-lookup"><span data-stu-id="81116-168">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="81116-169">Mô tả Ước tính</span><span class="sxs-lookup"><span data-stu-id="81116-169">Estimate Lines</span></span>             | <span data-ttu-id="81116-170">Thực thể tích hợp cho ước tính chi phí dự án</span><span class="sxs-lookup"><span data-stu-id="81116-170">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="81116-171">Luồng thực thể</span><span class="sxs-lookup"><span data-stu-id="81116-171">Entity flow</span></span>

<span data-ttu-id="81116-172">Ước tính chi phí dự án được quản lý trong Project Service Automation và được đồng bộ hóa với Finance dưới dạng dự báo chi phí dự án.</span><span class="sxs-lookup"><span data-stu-id="81116-172">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="81116-173">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="81116-173">Prerequisites</span></span>

<span data-ttu-id="81116-174">Trước khi đồng bộ hóa ước tính chi phí dự án có thể xảy ra, bạn phải đồng bộ hóa dự án, nhiệm vụ dự án và thể loại giao dịch chi phí dự án.</span><span class="sxs-lookup"><span data-stu-id="81116-174">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="81116-175">Power Query</span><span class="sxs-lookup"><span data-stu-id="81116-175">Power Query</span></span>

<span data-ttu-id="81116-176">Trong mẫu ước tính chi phí dự án, bạn phải sử dụng Power Query để hoàn thành các nhiệm vụ sau:</span><span class="sxs-lookup"><span data-stu-id="81116-176">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="81116-177">Lọc để chỉ bao gồm các bản ghi dòng ước tính chi phí.</span><span class="sxs-lookup"><span data-stu-id="81116-177">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="81116-178">Thiết lập ID mô hình dự báo mặc định sẽ được sử dụng khi tùy chọn tích hợp tạo dự báo giờ mới.</span><span class="sxs-lookup"><span data-stu-id="81116-178">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="81116-179">Chuyển đổi các loại thanh toán.</span><span class="sxs-lookup"><span data-stu-id="81116-179">Transform the billing types.</span></span>
- <span data-ttu-id="81116-180">Chuyển đổi các loại giao dịch.</span><span class="sxs-lookup"><span data-stu-id="81116-180">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="81116-181">Lọc để chỉ bao gồm các dòng ước tính chi phí</span><span class="sxs-lookup"><span data-stu-id="81116-181">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="81116-182">Mẫu ước tính chi phí dự án (PSA sang Fin và Ops) có bộ lọc mặc định chỉ bao gồm các dòng chi phí trong tích hợp.</span><span class="sxs-lookup"><span data-stu-id="81116-182">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="81116-183">Nếu bạn tạo mẫu của riêng mình, bạn phải thêm bộ lọc này.</span><span class="sxs-lookup"><span data-stu-id="81116-183">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="81116-184">Chọn nhiệm vụ **Mối quan hệ giao dịch** rồi nhấp vào mũi tên **Bản đồ** để mở ánh xạ.</span><span class="sxs-lookup"><span data-stu-id="81116-184">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="81116-185">Chọn liên kết **Truy vấn nâng cao và lọc**.</span><span class="sxs-lookup"><span data-stu-id="81116-185">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="81116-186">Lọc cột **msdyn\_transactiontype1** đê chỉ bao gồm **msdyn\_estimateline**.</span><span class="sxs-lookup"><span data-stu-id="81116-186">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="81116-187">Thiết lập ID mô hình dự báo mặc định</span><span class="sxs-lookup"><span data-stu-id="81116-187">Set the default forecast model ID</span></span>

<span data-ttu-id="81116-188">Để cập nhật ID mô hình dự báo mặc định trong mẫu, hãy chọn nhiệm vụ **Ước tính chi phí** rồi nhấp vào mũi tên **Bản đồ** để mở ánh xạ.</span><span class="sxs-lookup"><span data-stu-id="81116-188">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="81116-189">Chọn liên kết **Truy vấn nâng cao và lọc**.</span><span class="sxs-lookup"><span data-stu-id="81116-189">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="81116-190">Nếu bạn đang sử dụng mẫu Ước tính chi phí dự án (PSA sang Fin and Ops) mặc định, thì trong Power Query, trước tiên hãy chọn **Điều kiện đã chèn** ở phần **Các bước được áp dụng**.</span><span class="sxs-lookup"><span data-stu-id="81116-190">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="81116-191">Trong mục nhập **Hàm** , thay **O\_forecast** bằng tên của ID mô hình dự đoán sẽ dùng với tùy chọn tích hợp.</span><span class="sxs-lookup"><span data-stu-id="81116-191">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="81116-192">Mẫu mặc định có ID mô hình dự báo từ dữ liệu demo.</span><span class="sxs-lookup"><span data-stu-id="81116-192">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="81116-193">Nếu bạn đang tạo một mẫu mới, bạn phải thêm cột này.</span><span class="sxs-lookup"><span data-stu-id="81116-193">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="81116-194">Trong Power Query, chọn **Thêm cột điều kiện** và nhập tên của cột mới, như **ID mô hình**.</span><span class="sxs-lookup"><span data-stu-id="81116-194">In Power Query, select **Add Conditional Column** , and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="81116-195">Nhập điều kiện cho cột, trong đó, nếu ID dòng ước tính không phải là null, thì \<enter the forecast model ID\>; nếu không thì nhập null.</span><span class="sxs-lookup"><span data-stu-id="81116-195">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="81116-196">Chuyển đổi các loại thanh toán</span><span class="sxs-lookup"><span data-stu-id="81116-196">Transform the billing types</span></span>

<span data-ttu-id="81116-197">Mẫu ước tính chi phí dự án (PSA sang Fin và Ops) bao gồm một cột có điều kiện được sử dụng để chuyển đổi các loại lập hóa đơn nhận được từ Project Service Automation trong quá trình tích hợp.</span><span class="sxs-lookup"><span data-stu-id="81116-197">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="81116-198">Nếu bạn tạo mẫu của riêng mình, bạn phải thêm cột điều kiện này.</span><span class="sxs-lookup"><span data-stu-id="81116-198">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="81116-199">Chọn liên kết **Truy vấn nâng cao và lọc** rồi chọn **Thêm cột bổ sung**.</span><span class="sxs-lookup"><span data-stu-id="81116-199">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="81116-200">Nhập tên cho cột mới, chẳng hạn như **Loại lập hóa đơn**.</span><span class="sxs-lookup"><span data-stu-id="81116-200">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="81116-201">Sau đó, nhập điều kiện sau:</span><span class="sxs-lookup"><span data-stu-id="81116-201">Then enter the following condition:</span></span>

<span data-ttu-id="81116-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span><span class="sxs-lookup"><span data-stu-id="81116-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="81116-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span><span class="sxs-lookup"><span data-stu-id="81116-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="81116-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span><span class="sxs-lookup"><span data-stu-id="81116-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="81116-205">else **NotAvailable**</span><span class="sxs-lookup"><span data-stu-id="81116-205">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="81116-206">Chuyển đổi các loại giao dịch</span><span class="sxs-lookup"><span data-stu-id="81116-206">Transform the transaction types</span></span>

<span data-ttu-id="81116-207">Mẫu ước tính chi phí dự án (PSA sang Fin và Ops) bao gồm một cột có điều kiện được sử dụng để chuyển đổi các loại giao dịch nhận được từ Project Service Automation trong quá trình tích hợp.</span><span class="sxs-lookup"><span data-stu-id="81116-207">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="81116-208">Nếu bạn tạo mẫu của riêng mình, bạn phải thêm cột điều kiện này.</span><span class="sxs-lookup"><span data-stu-id="81116-208">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="81116-209">Chọn liên kết **Truy vấn nâng cao và lọc** rồi chọn **Thêm cột bổ sung**.</span><span class="sxs-lookup"><span data-stu-id="81116-209">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="81116-210">Nhập tên cho cột mới, chẳng hạn như **Loại giao dịch**.</span><span class="sxs-lookup"><span data-stu-id="81116-210">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="81116-211">Sau đó, nhập điều kiện sau:</span><span class="sxs-lookup"><span data-stu-id="81116-211">Then enter the following condition:</span></span>

<span data-ttu-id="81116-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span><span class="sxs-lookup"><span data-stu-id="81116-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="81116-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span><span class="sxs-lookup"><span data-stu-id="81116-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="81116-214">else **null**</span><span class="sxs-lookup"><span data-stu-id="81116-214">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="81116-215">Ánh xạ mẫu trong tích hợp dữ liệu</span><span class="sxs-lookup"><span data-stu-id="81116-215">Template mapping in Data integration</span></span>

<span data-ttu-id="81116-216">Các hình sau đây minh họa các ví dụ về việc ánh xạ nhiệm vụ mẫu trong Tích hợp dữ liệu.</span><span class="sxs-lookup"><span data-stu-id="81116-216">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="81116-217">Tùy chọn ánh xạ hiển thị thông tin trường sẽ được đồng bộ hóa từ Project Service Automation sang Finance.</span><span class="sxs-lookup"><span data-stu-id="81116-217">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="81116-218">[![Ánh xạ mẫu của giao dịch ước tính chi phí](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="81116-218">[![Template mapping of expense estimate transactions](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="81116-219">[![Ánh xạ mẫu của ước tính chi phí](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="81116-219">[![Template mapping of expense estimates](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>
