---
title: Xác định kiểu triển khai của bạn
description: Chủ đề này cung cấp thông tin nhằm giúp bạn xác định đúng loại triển khai Project Operations cho công ty của bạn.
author: stsporen
manager: Annbe
ms.date: 03/15/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 1aae04230104d27db2f62db8e674697fd83460ac
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948151"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="d3cb3-103">Xác định kiểu triển khai của bạn</span><span class="sxs-lookup"><span data-stu-id="d3cb3-103">Determine your deployment type</span></span>

<span data-ttu-id="d3cb3-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="d3cb3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d3cb3-105">Sau khi bạn mua giấy phép, hãy bắt đầu tại đây để xác định mô hình triển khai tốt nhất cho Dynamics 365 Project Operations sử dụng [Quy trình cài đặt có hướng dẫn](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="d3cb3-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="d3cb3-106">Sau khi hoàn thành quy trình cài đặt có hướng dẫn, bạn sẽ được chuyển đến đúng cổng quản lý để hoàn tất quá trình cài đặt của mình.</span><span class="sxs-lookup"><span data-stu-id="d3cb3-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="d3cb3-107">Xem thông tin chi tiết triển khai để hoàn tất việc cài đặt.</span><span class="sxs-lookup"><span data-stu-id="d3cb3-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="d3cb3-108">Khách hàng hiện tại của Dynamics đang sử dụng Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="d3cb3-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="d3cb3-109">Project Operations bao gồm các khả năng đi kèm với Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="d3cb3-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="d3cb3-110">Đường dẫn nâng cấp sẽ ra mắt những khách hàng này trong bản phát hành đợt 1 năm 2021.</span><span class="sxs-lookup"><span data-stu-id="d3cb3-110">An upgrade path will be released for these customers in the 2021 release wave 1.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="d3cb3-111">Khách hàng hiện tại của Dynamics 365 Finance sử dụng kế toán và quản lý dự án</span><span class="sxs-lookup"><span data-stu-id="d3cb3-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="d3cb3-112">Các khách hàng hiện tại của Finance sử dụng tính năng Kế toán và quản lý dự án vẫn có thể tiếp tục sử dụng tính năng này như cũ.</span><span class="sxs-lookup"><span data-stu-id="d3cb3-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use it as is.</span></span> <span data-ttu-id="d3cb3-113">Xem [Project Operations dành cho kịch bản dựa trên hàng nhập kho/lệnh sản xuất](#pma).</span><span class="sxs-lookup"><span data-stu-id="d3cb3-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-regions"></a><span data-ttu-id="d3cb3-114">Khu vực triển khai</span><span class="sxs-lookup"><span data-stu-id="d3cb3-114">Deployment regions</span></span>
<span data-ttu-id="d3cb3-115">Để xác định khu vực nào hỗ trợ triển khai Project Operations, hãy xem [Báo cáo khả năng cung cấp theo khu vực địa lý của Dynamics 365 và Power Platform](https://dynamics.microsoft.com/en-us/geographic-availability/).</span><span class="sxs-lookup"><span data-stu-id="d3cb3-115">To determine which regions support Project Operations deployment, see [Geographical availability for Dynamics 365 and Power Platform report](https://dynamics.microsoft.com/en-us/geographic-availability/).</span></span> <span data-ttu-id="d3cb3-116">Chọn **Xem báo cáo** và mở rộng **Dynamics 365 > Ứng dụng Operations > Dynamics 365 Project Operations** để xem các khu vực được hỗ trợ.</span><span class="sxs-lookup"><span data-stu-id="d3cb3-116">Select **View Report**, and expand **Dynamics 365 > Operations Apps > Dynamics 365 Project Operations** to view the supported regions.</span></span>

## <a name="deployment-types"></a><span data-ttu-id="d3cb3-117">Loại triển khai</span><span class="sxs-lookup"><span data-stu-id="d3cb3-117">Deployment types</span></span>
<span data-ttu-id="d3cb3-118">Project Operations hỗ trợ nhiều tùy chọn triển khai để phù hợp với yêu cầu của bạn.</span><span class="sxs-lookup"><span data-stu-id="d3cb3-118">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="d3cb3-119">Bất kể bạn là khách hàng Dynamics 365 mới hay là khách hàng hiện tại, Project Operations cũng có thể hỗ trợ nhu cầu của bạn.</span><span class="sxs-lookup"><span data-stu-id="d3cb3-119">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="d3cb3-120">[Bảng câu hỏi triển khai](https://aka.ms/provisionprojectoperations) của chúng tôi sẽ giúp bạn xác định đúng mô hình triển khai.</span><span class="sxs-lookup"><span data-stu-id="d3cb3-120">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="d3cb3-121">Kết quả sẽ hướng dẫn bạn đến một trong các kiểu triển khai sau:</span><span class="sxs-lookup"><span data-stu-id="d3cb3-121">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="d3cb3-122">Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn chiếu lệ</span><span class="sxs-lookup"><span data-stu-id="d3cb3-122">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="d3cb3-123">Project Operations dành cho tình huống dựa trên nguồn lực/hàng không trữ kho</span><span class="sxs-lookup"><span data-stu-id="d3cb3-123">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="d3cb3-124">Project Operations dành cho tình huống dựa trên hàng trữ kho/lệnh sản xuất</span><span class="sxs-lookup"><span data-stu-id="d3cb3-124">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="d3cb3-125">Project Operations hỗ trợ các kịch bản dựa trên hàng nhập kho/lệnh sản xuất và các kịch bản dựa trên hàng không nhập kho/nguồn lực trên cùng một môi trường thông qua các cấu hình cấp pháp nhân.</span><span class="sxs-lookup"><span data-stu-id="d3cb3-125">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="d3cb3-126">Ví dụ: Contoso có thể sử dụng các khả năng của lệnh sản xuất/vật liệu tồn kho tại cơ sở sản xuất ở Hoa Kỳ của họ (Pháp nhân = Contoso Manufacturing United States).</span><span class="sxs-lookup"><span data-stu-id="d3cb3-126">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="d3cb3-127">Contoso có thể sử dụng các khả năng dựa trên nguồn lực/vật tư không tồn kho trong cơ sở dịch vụ Contoso Robotics Arms ở Vương quốc Anh (Pháp nhân = Contoso Robotics United Kingdom).</span><span class="sxs-lookup"><span data-stu-id="d3cb3-127">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="d3cb3-128">Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá</span><span class="sxs-lookup"><span data-stu-id="d3cb3-128">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="d3cb3-129">Việc triển khai đơn giản bao gồm các khả năng sau:</span><span class="sxs-lookup"><span data-stu-id="d3cb3-129">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="d3cb3-130">Quy trình bán hàng của các dự án mở rộng trải nghiệm cho ứng dụng Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="d3cb3-130">Sales process for projects that extends Dynamics 365 Sales application experiences</span></span>
- <span data-ttu-id="d3cb3-131">Lập kế hoạch dự án bằng Microsoft Project dành cho web</span><span class="sxs-lookup"><span data-stu-id="d3cb3-131">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="d3cb3-132">Định giá dựa trên nhiều thông số</span><span class="sxs-lookup"><span data-stu-id="d3cb3-132">Multi-dimensional pricing</span></span>
- <span data-ttu-id="d3cb3-133">Quản lý nguồn lực hợp nhất</span><span class="sxs-lookup"><span data-stu-id="d3cb3-133">Unified resource management</span></span>
- <span data-ttu-id="d3cb3-134">Theo dõi thời gian</span><span class="sxs-lookup"><span data-stu-id="d3cb3-134">Time tracking</span></span>
- <span data-ttu-id="d3cb3-135">Chi phí cơ bản</span><span class="sxs-lookup"><span data-stu-id="d3cb3-135">Basic expense</span></span>
- <span data-ttu-id="d3cb3-136">Lập hóa đơn ước giá để Người quản lý dự án xem xét và chỉnh sửa</span><span class="sxs-lookup"><span data-stu-id="d3cb3-136">Proforma invoicing for Project manager's review and edits</span></span> 

#### <a name="deployment-steps"></a><span data-ttu-id="d3cb3-137">Các bước triển khai</span><span class="sxs-lookup"><span data-stu-id="d3cb3-137">Deployment steps</span></span>
<span data-ttu-id="d3cb3-138">Xác định mô hình triển khai tốt nhất của Project Operations bằng cách sử dụng [Bảng câu hỏi triển khai](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="d3cb3-138">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="d3cb3-139">Đối với việc triển khai này, hãy xem [Đăng ký gói đăng ký xem trước](lite-preview-subscription-sign-up.md) và [Cung cấp môi trường mới](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="d3cb3-139">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="d3cb3-140">Project Operations dành cho tình huống dựa trên nguồn lực/hàng không trữ kho</span><span class="sxs-lookup"><span data-stu-id="d3cb3-140">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="d3cb3-141">Project Operations cho các kịch bản dựa trên nguồn lực/hàng không nhập kho bao gồm các khả năng sau:</span><span class="sxs-lookup"><span data-stu-id="d3cb3-141">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
 
- <span data-ttu-id="d3cb3-142">Quy trình bán hàng của các dự án mở rộng ứng dụng Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="d3cb3-142">Sales process for projects that extends the Dynamics 365 Sales application</span></span>
- <span data-ttu-id="d3cb3-143">Lập kế hoạch dự án bằng Microsoft Project dành cho web</span><span class="sxs-lookup"><span data-stu-id="d3cb3-143">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="d3cb3-144">Định giá dựa trên nhiều thông số</span><span class="sxs-lookup"><span data-stu-id="d3cb3-144">Multi-dimensional pricing</span></span>
- <span data-ttu-id="d3cb3-145">Quản lý nguồn lực hợp nhất</span><span class="sxs-lookup"><span data-stu-id="d3cb3-145">Unified resource management</span></span>
- <span data-ttu-id="d3cb3-146">Theo dõi thời gian</span><span class="sxs-lookup"><span data-stu-id="d3cb3-146">Time tracking</span></span>
- <span data-ttu-id="d3cb3-147">Chi phí cơ bản</span><span class="sxs-lookup"><span data-stu-id="d3cb3-147">Basic expense</span></span>
- <span data-ttu-id="d3cb3-148">Chi phí đầy đủ</span><span class="sxs-lookup"><span data-stu-id="d3cb3-148">Full expense</span></span>
- <span data-ttu-id="d3cb3-149">Biên nhận OCR</span><span class="sxs-lookup"><span data-stu-id="d3cb3-149">Receipt OCR</span></span>
- <span data-ttu-id="d3cb3-150">Lập hóa đơn ước giá và hóa đơn dành cho khách hàng</span><span class="sxs-lookup"><span data-stu-id="d3cb3-150">Proforma and customer-facing invoicing</span></span> 
- <span data-ttu-id="d3cb3-151">Ghi nhận doanh thu cho dự án</span><span class="sxs-lookup"><span data-stu-id="d3cb3-151">Revenue recognition for projects</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="d3cb3-152">Các bước triển khai</span><span class="sxs-lookup"><span data-stu-id="d3cb3-152">Deployment steps</span></span>
<span data-ttu-id="d3cb3-153">Xác định mô hình triển khai tốt nhất của Project Operations bằng cách sử dụng [Bảng câu hỏi triển khai](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="d3cb3-153">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="d3cb3-154">Đối với việc triển khai này, hãy xem [Đăng ký gói đăng ký xem trước](resource-sign-up-preview-subscription.md) và [Cung cấp môi trường mới](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="d3cb3-154">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="d3cb3-155">Project Operations dành cho tình huống dựa trên hàng trữ kho/lệnh sản xuất</span><span class="sxs-lookup"><span data-stu-id="d3cb3-155">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="d3cb3-156">Lập kế hoạch dự án bằng WBS</span><span class="sxs-lookup"><span data-stu-id="d3cb3-156">Project planning using WBS</span></span>
- <span data-ttu-id="d3cb3-157">Quản lý nguồn lực</span><span class="sxs-lookup"><span data-stu-id="d3cb3-157">Resource management</span></span>
- <span data-ttu-id="d3cb3-158">Theo dõi thời gian</span><span class="sxs-lookup"><span data-stu-id="d3cb3-158">Time tracking</span></span>
- <span data-ttu-id="d3cb3-159">Chi phí đầy đủ</span><span class="sxs-lookup"><span data-stu-id="d3cb3-159">Full expense</span></span>
- <span data-ttu-id="d3cb3-160">Biên nhận OCR</span><span class="sxs-lookup"><span data-stu-id="d3cb3-160">Receipt OCR</span></span>
- <span data-ttu-id="d3cb3-161">Lập hóa đơn đầy đủ</span><span class="sxs-lookup"><span data-stu-id="d3cb3-161">Full invoicing</span></span>
- <span data-ttu-id="d3cb3-162">Ghi nhận doanh thu</span><span class="sxs-lookup"><span data-stu-id="d3cb3-162">Revenue recognition</span></span>
- <span data-ttu-id="d3cb3-163">Lệnh sản xuất</span><span class="sxs-lookup"><span data-stu-id="d3cb3-163">Production orders</span></span>
- <span data-ttu-id="d3cb3-164">Vật tư tồn kho hỗ trợ với hàng tồn kho</span><span class="sxs-lookup"><span data-stu-id="d3cb3-164">Stocked materials support with inventory</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="d3cb3-165">Các bước triển khai</span><span class="sxs-lookup"><span data-stu-id="d3cb3-165">Deployment steps</span></span>
<span data-ttu-id="d3cb3-166">Xác định mô hình triển khai tốt nhất của Project Operations bằng cách sử dụng [Bảng câu hỏi triển khai](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="d3cb3-166">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="d3cb3-167">Đối với việc triển khai này, hãy xem [Đăng ký gói đăng ký xem trước](/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=%2fdynamics365%2ffinance%2ftoc.json) và [Cung cấp môi trường mới](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=%2fdynamics365%2ffinance%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="d3cb3-167">For this deployment, see [Sign-up for preview subscriptions](/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=%2fdynamics365%2ffinance%2ftoc.json) and [Provision new environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=%2fdynamics365%2ffinance%2ftoc.json).</span></span> 



[!INCLUDE[footer-include](../includes/footer-banner.md)]