---
title: Đồng bộ hóa danh mục chi phí của dự án giữa Finance and Operations và Project Service Automation
description: Chủ đề này mô tả các mẫu và nhiệm vụ cơ bản dùng để đồng bộ hóa các danh mục chi phí của dự án giữa Microsoft Dynamics 365 Finance và Dynamics 365 Project Service Automation.
author: KimANelson
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
ms.assetid: 7dd914dc-1913-45eb-8a67-e897b00089fa
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 757fe1dbc804b986fc3334ebae7254a3f0491f59
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 03/24/2020
ms.locfileid: "3757084"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="5710f-103">Đồng bộ hóa danh mục chi phí của dự án giữa Finance and Operations và Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="5710f-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="5710f-104">Chủ đề này mô tả các mẫu và nhiệm vụ cơ bản dùng để đồng bộ hóa các danh mục chi phí của dự án giữa Dynamics 365 Finance và Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="5710f-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Dynamics 365 Finance and Dynamics 365 Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="5710f-105">Tính năng tích hợp nhiệm vụ dự án, thể loại giao dịch chi phí, ước tính giờ, ước tính chi phí và khóa chức năng có sẵn trong phiên bản 8.0.</span><span class="sxs-lookup"><span data-stu-id="5710f-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="5710f-106">Tùy chọn tích hợp giá trị thực tế có sẵn từ phiên bản 8.0.1.</span><span class="sxs-lookup"><span data-stu-id="5710f-106">Actuals integration is available in version 8.0.1 or later.</span></span>
> - <span data-ttu-id="5710f-107">Nếu bạn đang sử dụng Enterprise Edition 7.3.0, sau khi cài đặt KB 4132657 và KB 4132660, thì bạn sẽ có thể sử dụng các mẫu để tích hợp nhiệm vụ dự án, danh mục giao dịch chi phí, các giá trị ước tính giờ, ước tính chi phí và giá trị thực tế để đặt cấu hình tùy chọn khóa chức năng.</span><span class="sxs-lookup"><span data-stu-id="5710f-107">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="5710f-108">Nếu bạn phải đặt lại các bản phân bổ kế toán, thì chúng tôi khuyên bạn cũng nên cài đặt KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="5710f-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance"></a><span data-ttu-id="5710f-109">Luồng dữ liệu cho Project Service Automation và Finance</span><span class="sxs-lookup"><span data-stu-id="5710f-109">Data flow for Project Service Automation and Finance</span></span>

<span data-ttu-id="5710f-110">Giải pháp tích hợp Project Service Automation và Finance sử dụng tính năng Tích hợp dữ liệu để đồng bộ hóa dữ liệu giữa các phiên bản của Project Service Automation và Finance.</span><span class="sxs-lookup"><span data-stu-id="5710f-110">The Project Service Automation and Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="5710f-111">Các mẫu tích hợp có sẵn với tính năng Tích hợp dữ liệu sẽ tạo ra luồng dữ liệu về các danh mục giao dịch chi phí của dự án giữa Finance và Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="5710f-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Project Service Automation.</span></span>

<span data-ttu-id="5710f-112">Nếu các danh mục chi phí dự án được tạo chính trong Finance, thì quy trình tích hợp trước tiên là từ Finance sang Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="5710f-112">If the project expense categories are mastered in Finance, the integration flow is first from Finance to Project Service Automation.</span></span> <span data-ttu-id="5710f-113">Sau đó, ID tích hợp của các danh mục chi phí của dự án được cập nhật thông qua hoạt động đồng bộ hóa từ Project Service Automation sang Finance.</span><span class="sxs-lookup"><span data-stu-id="5710f-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance.</span></span>

<span data-ttu-id="5710f-114">Nếu các danh mục chi phí dự án được tạo chính trong Project Service Automation, thì quy trình tích hợp trước tiên là từ Project Service Automation sang Finance.</span><span class="sxs-lookup"><span data-stu-id="5710f-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance.</span></span> <span data-ttu-id="5710f-115">Các danh mục dự án phải được đặt cấu hình sẵn trong Finance trước khi đồng bộ hóa từ Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="5710f-115">The project categories must already be configured in Finance before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="5710f-116">Sau đó, đồng bộ hóa từ Finance trở lại Project Service Automation, rồi lại từ Project Service Automation sang Finance.</span><span class="sxs-lookup"><span data-stu-id="5710f-116">Then synchronize from Finance back to Project Service Automation, and then from Project Service Automation to Finance again.</span></span> <span data-ttu-id="5710f-117">Bằng cách này, bạn bảo đảm rằng các danh mục được liên kết và không có bản trùng lặp nào được tạo.</span><span class="sxs-lookup"><span data-stu-id="5710f-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="5710f-118">Thông thường, các danh mục chi phí của dự án được tạo chính trong Finance.</span><span class="sxs-lookup"><span data-stu-id="5710f-118">Typically, the project expense categories are mastered in Finance.</span></span> <span data-ttu-id="5710f-119">Tuy nhiên, nếu bạn gặp trường hợp không phải như thế hoặc nếu danh mục chi phí đã được tạo sẵn trong Project Service Automation, thì trước tiên, bạn phải đồng bộ hóa bằng mẫu Danh mục giao dịch chi phí của dự án (PSA sang Fin and Ops).</span><span class="sxs-lookup"><span data-stu-id="5710f-119">However, if they aren't, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="5710f-120">Sau đó, đồng bộ hóa bằng mẫu Danh mục giao dịch chi phí của dự án (Fin and Ops sang PSA).</span><span class="sxs-lookup"><span data-stu-id="5710f-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="5710f-121">Tiếp đến, bạn nên chạy đồng bộ hóa từ Project Service Automation sang Finance một lần nữa.</span><span class="sxs-lookup"><span data-stu-id="5710f-121">You should then run the synchronization from Project Service Automation to Finance one more time.</span></span>
>
> <span data-ttu-id="5710f-122">Nếu bạn đồng bộ hóa trước tiên từ Project Service Automation, thì các yêu cầu sau phải được đáp ứng trong Finance trước khi chạy đồng bộ hóa:</span><span class="sxs-lookup"><span data-stu-id="5710f-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance before the synchronization is run:</span></span>
>
> - <span data-ttu-id="5710f-123">Danh mục dùng chung khớp với danh mục dự án được thiết lập trong Project Service Automation phải tồn tại và phải được bật cho cả **Dự án** và **Chi phí**.</span><span class="sxs-lookup"><span data-stu-id="5710f-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="5710f-124">Đối với mỗi pháp nhân Finance cần phải tích hợp, các danh mục dự án sau phải tồn tại:</span><span class="sxs-lookup"><span data-stu-id="5710f-124">For each Finance legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="5710f-125">**Danh mục dự án** tồn tại.</span><span class="sxs-lookup"><span data-stu-id="5710f-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="5710f-126">**Sử dụng trong chi phí** được kích hoạt.</span><span class="sxs-lookup"><span data-stu-id="5710f-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="5710f-127">**Hoạt động trong nhật ký** được kích hoạt.</span><span class="sxs-lookup"><span data-stu-id="5710f-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="5710f-128">**Loại giao dịch** được đặt thành **Chi phí**.</span><span class="sxs-lookup"><span data-stu-id="5710f-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="5710f-129">Hình minh họa sau đây cho thấy cách dữ liệu được đồng bộ hóa giữa Project Service Automation và Finance.</span><span class="sxs-lookup"><span data-stu-id="5710f-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="5710f-130">[![Luồng dữ liệu cho phần tích hợp Project Service Automation với Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="5710f-130">[![Data flow for Project Service Automation integration with Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a><span data-ttu-id="5710f-131">Đồng bộ hóa danh mục chi phí của dự án từ Finance sang Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="5710f-131">Project expense category synchronization from Finance to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="5710f-132">Mẫu và nhiệm vụ</span><span class="sxs-lookup"><span data-stu-id="5710f-132">Template and task</span></span>

<span data-ttu-id="5710f-133">Để truy cập vào mẫu, trong trung tâm quản trị Microsoft Power Apps, chọn **Dự án** và sau đó, ở góc trên bên phải, chọn **Dự án mới** để chọn các mẫu công khai.</span><span class="sxs-lookup"><span data-stu-id="5710f-133">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="5710f-134">Mẫu sau và nhiệm vụ cơ bản được sử dụng để đồng bộ hóa các danh mục chi phí của dự án từ Finance sang Project Service Automation:</span><span class="sxs-lookup"><span data-stu-id="5710f-134">The following template and underlying task are used to synchronize project expense categories from Finance to Project Service Automation:</span></span>

- <span data-ttu-id="5710f-135">**Tên mẫu trong Tích hợp dữ liệu:** Danh mục giao dịch chi phí của dự án (Fin and Ops sang PSA)</span><span class="sxs-lookup"><span data-stu-id="5710f-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="5710f-136">**Tên nhiệm vụ trong dự án:** Đồng bộ hóa danh mục với PSA</span><span class="sxs-lookup"><span data-stu-id="5710f-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="5710f-137">Bộ thực thể</span><span class="sxs-lookup"><span data-stu-id="5710f-137">Entity set</span></span>

| <span data-ttu-id="5710f-138">Tài chính</span><span class="sxs-lookup"><span data-stu-id="5710f-138">Finance</span></span>                           | <span data-ttu-id="5710f-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="5710f-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="5710f-140">Thực thể tích hợp cho các danh mục</span><span class="sxs-lookup"><span data-stu-id="5710f-140">Integration entity for categories</span></span> | <span data-ttu-id="5710f-141">Danh mục giao dịch</span><span class="sxs-lookup"><span data-stu-id="5710f-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="5710f-142">Luồng thực thể</span><span class="sxs-lookup"><span data-stu-id="5710f-142">Entity flow</span></span>

<span data-ttu-id="5710f-143">Các danh mục chi phí của dự án được quản lý trong Finance và được đồng bộ hóa với Project Service Automation dưới dạng danh mục giao dịch.</span><span class="sxs-lookup"><span data-stu-id="5710f-143">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="5710f-144">Power Query</span><span class="sxs-lookup"><span data-stu-id="5710f-144">Power Query</span></span>

<span data-ttu-id="5710f-145">Khi đồng bộ hóa với Project Service Automation, bạn phải sử dụng Microsoft Power Query dành cho Excel để thiết lập loại thanh toán trên danh mục giao dịch.</span><span class="sxs-lookup"><span data-stu-id="5710f-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="5710f-146">Mẫu Danh mục giao dịch chi phí của dự án (Fin and Ops sang PSA) cung cấp một cột và tùy chọn ánh xạ mặc định.</span><span class="sxs-lookup"><span data-stu-id="5710f-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="5710f-147">Nếu bạn tạo mẫu của riêng mình, thì bạn phải thêm cột có điều kiện trong Power Query.</span><span class="sxs-lookup"><span data-stu-id="5710f-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="5710f-148">Làm theo các bước sau.</span><span class="sxs-lookup"><span data-stu-id="5710f-148">Follow these steps.</span></span>

1. <span data-ttu-id="5710f-149">Bấm vào mũi tên để mở mục ánh xạ nhiệm vụ danh mục chi phí của dự án trong mẫu Danh mục giao dịch chi phí của dự án (Fin and Ops sang PSA).</span><span class="sxs-lookup"><span data-stu-id="5710f-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="5710f-150">Bấm vào liên kết **Truy vấn nâng cao và lọc** để mở Power Query.</span><span class="sxs-lookup"><span data-stu-id="5710f-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="5710f-151">Chọn **Thêm cột có điều kiện**.</span><span class="sxs-lookup"><span data-stu-id="5710f-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="5710f-152">Nhập tên cho cột mới, chẳng hạn như **Loại lập hóa đơn**.</span><span class="sxs-lookup"><span data-stu-id="5710f-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="5710f-153">Nhập điều kiện sau: **nếu CATEGORYID không rỗng thì phải là giá trị 19235001, nếu không thì là rỗng**.</span><span class="sxs-lookup"><span data-stu-id="5710f-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="5710f-154">Bấm vào **OK** trên cột.</span><span class="sxs-lookup"><span data-stu-id="5710f-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="5710f-155">Bảo đảm ánh xạ cột mới này trên trang ánh xạ.</span><span class="sxs-lookup"><span data-stu-id="5710f-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="5710f-156">Hình sau đây minh họa một ví dụ về việc ánh xạ nhiệm vụ mẫu trong Tích hợp dữ liệu.</span><span class="sxs-lookup"><span data-stu-id="5710f-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="5710f-157">Tùy chọn ánh xạ hiển thị thông tin trường sẽ được đồng bộ hóa từ Finance sang Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="5710f-157">The mapping shows the field information that will be synchronized from Finance to Project Service Automation.</span></span>

<span data-ttu-id="5710f-158">[![Ánh xạ mẫu](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="5710f-158">[![Template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a><span data-ttu-id="5710f-159">Đồng bộ hóa danh mục chi phí của dự án từ Project Service Automation sang Finance</span><span class="sxs-lookup"><span data-stu-id="5710f-159">Project expense category synchronization from Project Service Automation to Finance</span></span>

### <a name="template-and-task"></a><span data-ttu-id="5710f-160">Mẫu và nhiệm vụ</span><span class="sxs-lookup"><span data-stu-id="5710f-160">Template and task</span></span>

<span data-ttu-id="5710f-161">Mẫu sau và nhiệm vụ cơ bản được sử dụng để đồng bộ hóa các danh mục chi phí của dự án từ Project Service Automation sang Finance:</span><span class="sxs-lookup"><span data-stu-id="5710f-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="5710f-162">**Tên mẫu trong Tích hợp dữ liệu:** Danh mục giao dịch chi phí của dự án (PSA sang Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="5710f-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="5710f-163">**Tên nhiệm vụ trong dự án:** Đồng bộ hóa danh mục với Fin Ops</span><span class="sxs-lookup"><span data-stu-id="5710f-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="5710f-164">Bộ thực thể</span><span class="sxs-lookup"><span data-stu-id="5710f-164">Entity set</span></span>

| <span data-ttu-id="5710f-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="5710f-165">Project Service Automation</span></span> | <span data-ttu-id="5710f-166">Tài chính</span><span class="sxs-lookup"><span data-stu-id="5710f-166">Finance</span></span>                           |
|----------------------------|-----------------------------------|
| <span data-ttu-id="5710f-167">Danh mục giao dịch</span><span class="sxs-lookup"><span data-stu-id="5710f-167">Transaction categories</span></span>     | <span data-ttu-id="5710f-168">Thực thể tích hợp cho các danh mục</span><span class="sxs-lookup"><span data-stu-id="5710f-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="5710f-169">Luồng thực thể</span><span class="sxs-lookup"><span data-stu-id="5710f-169">Entity flow</span></span>

<span data-ttu-id="5710f-170">Các danh mục chi phí của dự án được quản lý trong Finance và được đồng bộ hóa với Project Service Automation dưới dạng danh mục giao dịch.</span><span class="sxs-lookup"><span data-stu-id="5710f-170">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="5710f-171">Hoạt động đồng bộ hóa trở lại Finance sẽ cập nhật danh mục dự án trong Finance với ID tích hợp từ Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="5710f-171">The synchronization back to Finance updates the project category in Finance with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="5710f-172">Ánh xạ mẫu trong tích hợp dữ liệu</span><span class="sxs-lookup"><span data-stu-id="5710f-172">Template mapping in Data integration</span></span>

<span data-ttu-id="5710f-173">Hình sau đây minh họa một ví dụ về việc ánh xạ nhiệm vụ mẫu trong Tích hợp dữ liệu.</span><span class="sxs-lookup"><span data-stu-id="5710f-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="5710f-174">Tùy chọn ánh xạ hiển thị thông tin trường sẽ được đồng bộ hóa từ Project Service Automation sang Finance.</span><span class="sxs-lookup"><span data-stu-id="5710f-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="5710f-175">[![Ánh xạ mẫu](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="5710f-175">[![Template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>
