---
title: Loại triển khai
description: Chủ đề này cung cấp thông tin nhằm giúp bạn xác định đúng loại triển khai Project Operations cho công ty của bạn.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c3cf378caae4510482a8ee6771bf2e6decfe3b48
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949138"
---
# <a name="deployment-types"></a><span data-ttu-id="37544-103">Loại triển khai</span><span class="sxs-lookup"><span data-stu-id="37544-103">Deployment types</span></span>

<span data-ttu-id="37544-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="37544-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="37544-105">Sau khi bạn mua giấy phép, hãy bắt đầu tại đây để xác định mô hình triển khai tốt nhất của Dynamics 365 Project Operations bằng cách sử dụng [Quy trình cài đặt có hướng dẫn](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="37544-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="37544-106">Sau khi hoàn thành quy trình cài đặt có hướng dẫn, bạn sẽ được chuyển đến đúng cổng quản lý để hoàn tất quá trình cài đặt của mình.</span><span class="sxs-lookup"><span data-stu-id="37544-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="37544-107">Xem chi tiết triển khai bên dưới để hoàn tất cài đặt.</span><span class="sxs-lookup"><span data-stu-id="37544-107">See the deployment details below to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="37544-108">Khách hàng hiện tại của Dynamics đang sử dụng Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="37544-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="37544-109">Project Operations bao gồm các khả năng đi kèm với Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="37544-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="37544-110">Đường dẫn nâng cấp sẽ được phát hành cho những khách hàng này trong tương lai.</span><span class="sxs-lookup"><span data-stu-id="37544-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="37544-111">Khách hàng hiện tại của Dynamics 365 Finance sử dụng kế toán và quản lý dự án</span><span class="sxs-lookup"><span data-stu-id="37544-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="37544-112">Các khách hàng hiện tại của Finance sử dụng chức năng kế toán và quản lý dự án có thể tiếp tục sử dụng chức năng này.</span><span class="sxs-lookup"><span data-stu-id="37544-112">Existing customers of Finance who use the Project management and accounting functionality can continue use this as is.</span></span> <span data-ttu-id="37544-113">Xem [Project Operations dành cho kịch bản dựa trên hàng nhập kho/lệnh sản xuất](#pma).</span><span class="sxs-lookup"><span data-stu-id="37544-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>

<span data-ttu-id="37544-114">Project Operations hỗ trợ nhiều tùy chọn triển khai để phù hợp với yêu cầu của bạn.</span><span class="sxs-lookup"><span data-stu-id="37544-114">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="37544-115">Cho dù bạn là khách hàng Dynamics 365 mới hay hiện tại, Project Operations có thể hỗ trợ nhu cầu của bạn.</span><span class="sxs-lookup"><span data-stu-id="37544-115">Whether you are a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="37544-116">[Bảng câu hỏi triển khai](https://aka.ms/provisionprojectoperations) của chúng tôi sẽ giúp bạn xác định đúng mô hình triển khai.</span><span class="sxs-lookup"><span data-stu-id="37544-116">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="37544-117">Kết quả sẽ hướng dẫn bạn đến một trong các kiểu triển khai sau:</span><span class="sxs-lookup"><span data-stu-id="37544-117">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="37544-118">Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn chiếu lệ</span><span class="sxs-lookup"><span data-stu-id="37544-118">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="37544-119">Project Operations dành cho tình huống dựa trên nguồn lực/hàng không trữ kho</span><span class="sxs-lookup"><span data-stu-id="37544-119">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="37544-120">Project Operations dành cho tình huống dựa trên hàng trữ kho/lệnh sản xuất</span><span class="sxs-lookup"><span data-stu-id="37544-120">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="37544-121">Project Operations hỗ trợ các kịch bản dựa trên hàng nhập kho/lệnh sản xuất và các kịch bản dựa trên hàng không nhập kho/nguồn lực trên cùng một môi trường thông qua các cấu hình cấp pháp nhân.</span><span class="sxs-lookup"><span data-stu-id="37544-121">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="37544-122">Ví dụ: Contoso có thể tận dụng khả năng hàng nhập kho/lệnh sản xuất tại cơ sở sản xuất ở Hoa Kỳ của họ (Pháp nhân = Contoso Manufacturing United States) và các khả năng dựa trên nguồn lực/hàng không nhập kho trong cơ sở cung cấp cánh tay robot Contoso của họ ở Vương quốc Anh (Pháp nhân = Contoso Robotics United Kingdom).</span><span class="sxs-lookup"><span data-stu-id="37544-122">For example, Contoso can leverage stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States) and non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

## <a name="a-namelitelite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="37544-123"><a name="lite"><a/>Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá</span><span class="sxs-lookup"><span data-stu-id="37544-123"><a name="lite"><a/>Lite deployment - deal to proforma invoicing</span></span>
<span data-ttu-id="37544-124">Việc triển khai đơn giản bao gồm các khả năng sau:</span><span class="sxs-lookup"><span data-stu-id="37544-124">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="37544-125">Lập kế hoạch dự án bằng Microsoft Project dành cho web</span><span class="sxs-lookup"><span data-stu-id="37544-125">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="37544-126">Định giá dựa trên nhiều thông số</span><span class="sxs-lookup"><span data-stu-id="37544-126">Multi-dimensional pricing</span></span>
- <span data-ttu-id="37544-127">Quản lý nguồn lực hợp nhất</span><span class="sxs-lookup"><span data-stu-id="37544-127">Unified Resource Management</span></span>
- <span data-ttu-id="37544-128">Theo dõi thời gian</span><span class="sxs-lookup"><span data-stu-id="37544-128">Time Tracking</span></span>
- <span data-ttu-id="37544-129">Chi phí cơ bản</span><span class="sxs-lookup"><span data-stu-id="37544-129">Basic Expense</span></span>
- <span data-ttu-id="37544-130">Đề xuất hóa đơn</span><span class="sxs-lookup"><span data-stu-id="37544-130">Invoice Proposal</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="37544-131">Các bước triển khai:</span><span class="sxs-lookup"><span data-stu-id="37544-131">Deployment steps:</span></span>
<span data-ttu-id="37544-132">Xác định mô hình triển khai tốt nhất của Project Operations bằng cách sử dụng [Bảng câu hỏi triển khai](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="37544-132">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="37544-133">Đối với việc triển khai này, hãy xem [Đăng ký gói đăng ký xem trước](lite-preview-subscription-sign-up.md) và [Cung cấp môi trường mới](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="37544-133">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


## <a name="a-nameintegratedproject-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="37544-134"><a name="integrated"><a/>Project Operations dành cho tình huống dựa trên nguồn lực/hàng không trữ kho</span><span class="sxs-lookup"><span data-stu-id="37544-134"><a name="integrated"><a/>Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="37544-135">Project Operations cho các kịch bản dựa trên nguồn lực/hàng không nhập kho bao gồm các khả năng sau:</span><span class="sxs-lookup"><span data-stu-id="37544-135">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="37544-136">Lập kế hoạch dự án bằng Microsoft Project dành cho web</span><span class="sxs-lookup"><span data-stu-id="37544-136">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="37544-137">Định giá dựa trên nhiều thông số</span><span class="sxs-lookup"><span data-stu-id="37544-137">Multi-dimensional pricing</span></span>
- <span data-ttu-id="37544-138">Quản lý nguồn lực hợp nhất</span><span class="sxs-lookup"><span data-stu-id="37544-138">Unified Resource Management</span></span>
- <span data-ttu-id="37544-139">Theo dõi thời gian</span><span class="sxs-lookup"><span data-stu-id="37544-139">Time Tracking</span></span>
- <span data-ttu-id="37544-140">Chi phí cơ bản</span><span class="sxs-lookup"><span data-stu-id="37544-140">Basic Expense</span></span>
- <span data-ttu-id="37544-141">Chi phí đầy đủ</span><span class="sxs-lookup"><span data-stu-id="37544-141">Full Expense</span></span>
- <span data-ttu-id="37544-142">Biên nhận OCR</span><span class="sxs-lookup"><span data-stu-id="37544-142">Receipt OCR</span></span>
- <span data-ttu-id="37544-143">Lập hóa đơn đầy đủ</span><span class="sxs-lookup"><span data-stu-id="37544-143">Full Invoicing</span></span>
- <span data-ttu-id="37544-144">Ghi nhận doanh thu</span><span class="sxs-lookup"><span data-stu-id="37544-144">Revenue Recognition</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="37544-145">Các bước triển khai:</span><span class="sxs-lookup"><span data-stu-id="37544-145">Deployment steps:</span></span>
<span data-ttu-id="37544-146">Xác định mô hình triển khai tốt nhất của Project Operations bằng cách sử dụng [Bảng câu hỏi triển khai](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="37544-146">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="37544-147">Đối với việc triển khai này, hãy xem [Đăng ký gói đăng ký xem trước](resource-sign-up-preview-subscription.md) và [Cung cấp môi trường mới](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="37544-147">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


## <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="37544-148">Project Operations dành cho tình huống dựa trên hàng trữ kho/lệnh sản xuất</span><span class="sxs-lookup"><span data-stu-id="37544-148">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="37544-149">Lập kế hoạch dự án bằng WBS</span><span class="sxs-lookup"><span data-stu-id="37544-149">Project planning using WBS</span></span>
- <span data-ttu-id="37544-150">Quản lý nguồn lực</span><span class="sxs-lookup"><span data-stu-id="37544-150">Resource Management</span></span>
- <span data-ttu-id="37544-151">Theo dõi thời gian</span><span class="sxs-lookup"><span data-stu-id="37544-151">Time Tracking</span></span>
- <span data-ttu-id="37544-152">Chi phí đầy đủ</span><span class="sxs-lookup"><span data-stu-id="37544-152">Full Expense</span></span>
- <span data-ttu-id="37544-153">Biên nhận OCR</span><span class="sxs-lookup"><span data-stu-id="37544-153">Receipt OCR</span></span>
- <span data-ttu-id="37544-154">Lập hóa đơn đầy đủ</span><span class="sxs-lookup"><span data-stu-id="37544-154">Full Invoicing</span></span>
- <span data-ttu-id="37544-155">Ghi nhận doanh thu</span><span class="sxs-lookup"><span data-stu-id="37544-155">Revenue Recognition</span></span>
- <span data-ttu-id="37544-156">Đơn hàng sản xuất</span><span class="sxs-lookup"><span data-stu-id="37544-156">Production Orders</span></span>
- <span data-ttu-id="37544-157">Hỗ trợ vật tư</span><span class="sxs-lookup"><span data-stu-id="37544-157">Materials support</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="37544-158">Các bước triển khai:</span><span class="sxs-lookup"><span data-stu-id="37544-158">Deployment steps:</span></span>
<span data-ttu-id="37544-159">Xác định mô hình triển khai tốt nhất của Project Operations bằng cách sử dụng [Bảng câu hỏi triển khai](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="37544-159">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="37544-160">Đối với việc triển khai này, hãy xem [Đăng ký gói đăng ký xem trước](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) và [Cung cấp môi trường mới](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="37544-160">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 



