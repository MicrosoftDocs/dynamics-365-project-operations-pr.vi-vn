---
title: Cung cấp môi trường mới
description: Chủ đề này cung cấp thông tin về cách cung cấp môi trường Project Operations mới.
author: sigitac
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 45700371c50e3b5a840df45fc24fa8a5b4584b61
ms.sourcegitcommit: 87b7a8d793c19c50f3765b8d788cde24a6a0ca24
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949388"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="e098d-103">Cung cấp môi trường mới</span><span class="sxs-lookup"><span data-stu-id="e098d-103">Provision a new environment</span></span>

<span data-ttu-id="e098d-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_</span><span class="sxs-lookup"><span data-stu-id="e098d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="e098d-105">Chủ đề này cung cấp thông tin về cách cung cấp môi trường Dynamics 365 Project Operations mới cho kịch bản dựa trên nguồn lực/hàng không nhập kho.</span><span class="sxs-lookup"><span data-stu-id="e098d-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="e098d-106">Bật quy trình tự động cung cấp Project Operations trong dự án LCS</span><span class="sxs-lookup"><span data-stu-id="e098d-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="e098d-107">Sử dụng các bước sau để bật quy trình tự động cung cấp Project Operations cho dự án LCS của bạn.</span><span class="sxs-lookup"><span data-stu-id="e098d-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="e098d-108">Chuyển đến [LCS](https://lcs.dynamics.com/v2) và chọn ngăn xếp **Quản lý tính năng xem trước**.</span><span class="sxs-lookup"><span data-stu-id="e098d-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="e098d-109">Trong danh sách **Tính năng xem trước**, hãy chọn **Project Operations** và chọn **Đã bật tính năng xem trước** để kích hoạt Project Operations.</span><span class="sxs-lookup"><span data-stu-id="e098d-109">In the **Preview feature** list, select **Project Operations** and the select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="e098d-110">Bước này chỉ được thực hiện một lần cho mỗi dự án LCS.</span><span class="sxs-lookup"><span data-stu-id="e098d-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="e098d-111">Cung cấp môi trường Project Operations</span><span class="sxs-lookup"><span data-stu-id="e098d-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="e098d-112">Mở Dynamics 365 Finance mới [môi trường demo](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) hoặc triển khai [môi trường sản xuất/hộp cát](https://docs.microsoft.com/edynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure).</span><span class="sxs-lookup"><span data-stu-id="e098d-112">Open a new Dynamics 365 Finance [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](https://docs.microsoft.com/edynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="e098d-113">Tìm hiểu trình hướng dẫn **Cung cấp môi trường**.</span><span class="sxs-lookup"><span data-stu-id="e098d-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="e098d-114">Đảm bảo phiên bản ứng dụng đã chọn là 10.0.13 trở lên.</span><span class="sxs-lookup"><span data-stu-id="e098d-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="e098d-115">Để cung cấp Project Operations, trong phần **Cài đặt nâng cao**, hãy chọn **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="e098d-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="e098d-116">Bật **Thiết đặt Common Data Service** bằng việc chọn **Có** và sau đó nhập thông tin vào các trường bắt buộc:</span><span class="sxs-lookup"><span data-stu-id="e098d-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="e098d-117">Tên</span><span class="sxs-lookup"><span data-stu-id="e098d-117">Name</span></span>
  - <span data-ttu-id="e098d-118">Khu vực</span><span class="sxs-lookup"><span data-stu-id="e098d-118">Region</span></span>
  - <span data-ttu-id="e098d-119">Ngôn ngữ</span><span class="sxs-lookup"><span data-stu-id="e098d-119">Language</span></span>
  - <span data-ttu-id="e098d-120">Tiền tệ</span><span class="sxs-lookup"><span data-stu-id="e098d-120">Currency</span></span>
 
5. <span data-ttu-id="e098d-121">Trong trường **Mẫu Common Data Service**, hãy chọn **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="e098d-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="e098d-122">Chọn loại môi trường để triển khai.</span><span class="sxs-lookup"><span data-stu-id="e098d-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="e098d-123">Bản dùng thử dựa trên đăng ký sẽ cho phép bạn triển khai môi trường CDS trong 30 ngày.</span><span class="sxs-lookup"><span data-stu-id="e098d-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Cài đặt triển khai](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="e098d-125">Chọn **Đồng ý** để xác nhận các điều khoản dịch vụ và sau đó chọn **Xong** để quay lại cài đặt triển khai.</span><span class="sxs-lookup"><span data-stu-id="e098d-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Đồng ý triển khai](./media/2DeploymentConsent.png)

7. <span data-ttu-id="e098d-127">Hoàn thành các trường bắt buộc còn lại trong trình hướng dẫn và xác nhận việc triển khai.</span><span class="sxs-lookup"><span data-stu-id="e098d-127">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="e098d-128">Thời gian cung cấp môi trường thay đổi tùy theo loại môi trường.</span><span class="sxs-lookup"><span data-stu-id="e098d-128">Environment provisioning time varies based on the environment type.</span></span> <span data-ttu-id="e098d-129">Việc cung cấp có thể mất đến sáu giờ.</span><span class="sxs-lookup"><span data-stu-id="e098d-129">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="e098d-130">Sau khi quá trình triển khai hoàn tất thành công, môi trường sẽ hiển thị là **Đã triển khai**.</span><span class="sxs-lookup"><span data-stu-id="e098d-130">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

8. <span data-ttu-id="e098d-131">Để xác nhận môi trường đã được triển khai thành công, hãy chọn **Đăng nhập** và đăng nhập vào môi trường để xác nhận.</span><span class="sxs-lookup"><span data-stu-id="e098d-131">To confirm the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![Chi tiết môi trường ](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a><span data-ttu-id="e098d-133">Áp dụng dữ liệu demo Project Operations Finance (bước tùy chọn)</span><span class="sxs-lookup"><span data-stu-id="e098d-133">Apply Project Operations Finance demo data (optional step)</span></span>

<span data-ttu-id="e098d-134">Áp dụng dữ liệu demo Project Operations Finance cho bản phát hành dịch vụ 10.0.13 Môi trường lưu trữ trên đám mây như được mô tả trong [bài viết này](resource-apply-finance-demo-data.md).</span><span class="sxs-lookup"><span data-stu-id="e098d-134">Apply Project Operations Finance demo data to 10.0.13 service release Cloud Hosted Environment as described in [this article](resource-apply-finance-demo-data.md).</span></span>

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="e098d-135">Áp dụng nội dung cập nhật cho môi trường Finance</span><span class="sxs-lookup"><span data-stu-id="e098d-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="e098d-136">Project Operations yêu cầu môi trường Finance có phiên bản ứng dụng **10.0.13 (10.0.569.20009)** trở lên.</span><span class="sxs-lookup"><span data-stu-id="e098d-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="e098d-137">Bạn có thể cần áp dụng các bản cập nhật chất lượng cho môi trường Finance của mình để nhận được phiên bản này.</span><span class="sxs-lookup"><span data-stu-id="e098d-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="e098d-138">Trong LCS, trên trang **Chi tiết môi trường**, trong phần **Bản cập nhật có sẵn**, hãy chọn **Xem bản cập nhật**.</span><span class="sxs-lookup"><span data-stu-id="e098d-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Xem bản cập nhập](./media/5ViewUpdates.png)

2. <span data-ttu-id="e098d-140">Trên trang **Bản cập nhật nhị phân**, hãy chọn **Lưu gói.**</span><span class="sxs-lookup"><span data-stu-id="e098d-140">On the **Binary updates** page, select **Save package.**</span></span>

![Lưu gói](./media/6SavePackage.png)

3. <span data-ttu-id="e098d-142">Nhấp vào **Chọn tất cả** rồi chọn **Lưu gói**.</span><span class="sxs-lookup"><span data-stu-id="e098d-142">Click **Select all** and then select **Save package**.</span></span>

![Xem lại và lưu bản cập nhật](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="e098d-144">Nhập tên và mô tả của gói, sau đó chọn **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="e098d-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="e098d-145">Tùy thuộc vào kết nối Internet, quá trình này có thể mất một chút thời gian.</span><span class="sxs-lookup"><span data-stu-id="e098d-145">Depending on the internet connection, this process might take some time.</span></span>

![Tải gói lên Thư viện tài sản](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="e098d-147">Sau khi gói được lưu, hãy chọn **Xong** và lưu gói này vào Thư viện tài sản trong dự án LCS của bạn.</span><span class="sxs-lookup"><span data-stu-id="e098d-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="e098d-148">Việc lưu và xác nhận gói có thể mất khoảng 15 phút.</span><span class="sxs-lookup"><span data-stu-id="e098d-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="e098d-149">Để áp dụng bản cập nhật, hãy điều hướng đến trang **Môi trường chi tiết** trong LCS và chọn **Duy trì** > **Áp dụng bản cập nhật**.</span><span class="sxs-lookup"><span data-stu-id="e098d-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Duy trì môi trường](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="e098d-151">Trong danh sách bản cập nhật, hãy chọn gói bạn đã tạo và chọn **Áp dụng**.</span><span class="sxs-lookup"><span data-stu-id="e098d-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Áp dụng bản cập nhật](./media/10ApplyUpdates.png)

<span data-ttu-id="e098d-153">Việc cung cấp dịch vụ môi trường sẽ mất một thời gian.</span><span class="sxs-lookup"><span data-stu-id="e098d-153">Environment servicing will take some time.</span></span> <span data-ttu-id="e098d-154">Sau khi hoàn tất, môi trường sẽ trở lại trạng thái đã triển khai.</span><span class="sxs-lookup"><span data-stu-id="e098d-154">After it is complete, the environment will return to a deployed state.</span></span>

![Đã triển khai môi trường](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="e098d-156">Thiết lập kết nối Ghi kép</span><span class="sxs-lookup"><span data-stu-id="e098d-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="e098d-157">Trong dự án LCS của bạn, hãy chuyển đến trang **Chi tiết môi trường**.</span><span class="sxs-lookup"><span data-stu-id="e098d-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="e098d-158">Trong phần **Thông tin môi trường Common Data Service**, hãy chọn **Liên kết tới CDS for Apps**.</span><span class="sxs-lookup"><span data-stu-id="e098d-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="e098d-159">Sau khi liên kết hoàn tất, hãy chọn **Liên kết tới CDS for Apps** lần nữa.</span><span class="sxs-lookup"><span data-stu-id="e098d-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="e098d-160">Bạn sẽ được chuyển hướng đến Ghi kép trong Finance.</span><span class="sxs-lookup"><span data-stu-id="e098d-160">You will be redirected to Dual Write in Finance.</span></span>

![Liên kết tới CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="e098d-162">Chọn **Áp dụng giải pháp** để truy cập vào các thực thể sẽ được ánh xạ trong tích hợp.</span><span class="sxs-lookup"><span data-stu-id="e098d-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Áp dụng giải pháp](./media/13ApplySolutions.png)

5. <span data-ttu-id="e098d-164">Chọn cả hai giải pháp,**Bản đồ thực thể ghi kép của Dynamics 365 Finance and Operations** và **Bản đồ thực thể ghi kép của Dynamics 365 Project Operations**, và sau đó chọn **Áp dụng**.</span><span class="sxs-lookup"><span data-stu-id="e098d-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Xác nhận giải pháp](./media/14ConfirmSolutions.png)

<span data-ttu-id="e098d-166">Sau khi các giải pháp được áp dụng, các thực thể Ghi kép được áp dụng cho môi trường.</span><span class="sxs-lookup"><span data-stu-id="e098d-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Đang áp dụng giải pháp](./media/15ApplyingSolutions.png)

<span data-ttu-id="e098d-168">Sau khi các thực thể được áp dụng, tất cả các ánh xạ có sẵn sẽ được liệt kê trong môi trường.</span><span class="sxs-lookup"><span data-stu-id="e098d-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Bản đồ ghi kép](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="e098d-170">Làm mới các thực thể dữ liệu sau khi cập nhật</span><span class="sxs-lookup"><span data-stu-id="e098d-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="e098d-171">Trong Finance, hãy chuyển đến không gian làm việc **Quản lý dữ liệu**.</span><span class="sxs-lookup"><span data-stu-id="e098d-171">In Finance, go to the **Data management** workspace.</span></span>

![Không gian làm việc quản lý dữ liệu](./media/16DataManagement.png)

2. <span data-ttu-id="e098d-173">Chọn ngăn xếp **Tham số khung**.</span><span class="sxs-lookup"><span data-stu-id="e098d-173">Select the **Framework parameters** tile.</span></span>

![Tham số khung](./media/17FrameworkParameters.png)

3. <span data-ttu-id="e098d-175">Trên trang **Cài đặt thực thể**, hãy chọn **Làm mới danh sách thực thể**.</span><span class="sxs-lookup"><span data-stu-id="e098d-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Làm mới danh sách thực thể](./media/18RefreshEntityList.png)

<span data-ttu-id="e098d-177">Quá trình làm mới sẽ mất khoảng 20 phút.</span><span class="sxs-lookup"><span data-stu-id="e098d-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="e098d-178">Bạn sẽ nhận được một cảnh báo khi quá trình hoàn tất.</span><span class="sxs-lookup"><span data-stu-id="e098d-178">You will receive an alert when it is complete.</span></span>

![Xác nhận làm mới](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="e098d-180">Chạy bản đồ ghi kép Project Operations</span><span class="sxs-lookup"><span data-stu-id="e098d-180">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="e098d-181">Trong dự án LCS của bạn, hãy chuyển đến trang **Chi tiết môi trường**.</span><span class="sxs-lookup"><span data-stu-id="e098d-181">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="e098d-182">Trong phần **Thông tin môi trường Common Data Service**, hãy chọn **Liên kết tới CDS for Apps.**</span><span class="sxs-lookup"><span data-stu-id="e098d-182">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="e098d-183">Sau khi bạn chọn liên kết, bạn sẽ được chuyển hướng đến danh sách các thực thể trong ánh xạ.</span><span class="sxs-lookup"><span data-stu-id="e098d-183">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="e098d-184">Bắt đầu bản đồ như mô tả trong bảng sau.</span><span class="sxs-lookup"><span data-stu-id="e098d-184">Start the maps as described in the following table.</span></span> <span data-ttu-id="e098d-185">Đảm bảo làm theo trình tự như đã liệt kê.</span><span class="sxs-lookup"><span data-stu-id="e098d-185">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="e098d-186">**Sơ đồ thực thể**</span><span class="sxs-lookup"><span data-stu-id="e098d-186">**Entity Map**</span></span> | <span data-ttu-id="e098d-187">**Làm mới thực thể**</span><span class="sxs-lookup"><span data-stu-id="e098d-187">**Refresh entity**</span></span> | <span data-ttu-id="e098d-188">**Đồng bộ ban đầu**</span><span class="sxs-lookup"><span data-stu-id="e098d-188">**Initial sync**</span></span> | <span data-ttu-id="e098d-189">**Bản cái cho đồng bộ hóa ban đầu**</span><span class="sxs-lookup"><span data-stu-id="e098d-189">**Master for initial sync**</span></span> | <span data-ttu-id="e098d-190">**Chạy điều kiện tiên quyết**</span><span class="sxs-lookup"><span data-stu-id="e098d-190">**Run prerequisites**</span></span> | <span data-ttu-id="e098d-191">**Đồng bộ hóa ban đầu điều kiện tiên quyết**</span><span class="sxs-lookup"><span data-stu-id="e098d-191">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="e098d-192">**Vai trò nguồn lực dự án cho tất cả các công ty (các thể loại nguồn lực có thể đăng ký trước)**</span><span class="sxs-lookup"><span data-stu-id="e098d-192">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="e098d-193">No</span><span class="sxs-lookup"><span data-stu-id="e098d-193">No</span></span> | <span data-ttu-id="e098d-194">Có</span><span class="sxs-lookup"><span data-stu-id="e098d-194">Yes</span></span> | <span data-ttu-id="e098d-195">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="e098d-195">Common Data Service</span></span> | <span data-ttu-id="e098d-196">No</span><span class="sxs-lookup"><span data-stu-id="e098d-196">No</span></span> | <span data-ttu-id="e098d-197">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="e098d-197">N\A</span></span> |
| <span data-ttu-id="e098d-198">**Thực thể pháp lý (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="e098d-198">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="e098d-199">No</span><span class="sxs-lookup"><span data-stu-id="e098d-199">No</span></span> | <span data-ttu-id="e098d-200">Có</span><span class="sxs-lookup"><span data-stu-id="e098d-200">Yes</span></span> | <span data-ttu-id="e098d-201">Ứng dụng Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e098d-201">Finance and Operations apps</span></span> | <span data-ttu-id="e098d-202">No</span><span class="sxs-lookup"><span data-stu-id="e098d-202">No</span></span> | <span data-ttu-id="e098d-203">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="e098d-203">N\A</span></span> |
| <span data-ttu-id="e098d-204">**Giá trị tích hợp thực tế của Project Operations (msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="e098d-204">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="e098d-205">No</span><span class="sxs-lookup"><span data-stu-id="e098d-205">No</span></span> | <span data-ttu-id="e098d-206">No</span><span class="sxs-lookup"><span data-stu-id="e098d-206">No</span></span> | <span data-ttu-id="e098d-207">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="e098d-207">N\A</span></span> | <span data-ttu-id="e098d-208">Có</span><span class="sxs-lookup"><span data-stu-id="e098d-208">Yes</span></span> | <span data-ttu-id="e098d-209">No</span><span class="sxs-lookup"><span data-stu-id="e098d-209">No</span></span> |
| <span data-ttu-id="e098d-210">**Mô tả hợp đồng dự án (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="e098d-210">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="e098d-211">No</span><span class="sxs-lookup"><span data-stu-id="e098d-211">No</span></span> | <span data-ttu-id="e098d-212">No</span><span class="sxs-lookup"><span data-stu-id="e098d-212">No</span></span> | <span data-ttu-id="e098d-213">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="e098d-213">N\A</span></span> | <span data-ttu-id="e098d-214">No</span><span class="sxs-lookup"><span data-stu-id="e098d-214">No</span></span> | <span data-ttu-id="e098d-215">No</span><span class="sxs-lookup"><span data-stu-id="e098d-215">No</span></span> |
| <span data-ttu-id="e098d-216">**Thực thể tích hợp cho các mối quan hệ giao dịch dự án (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="e098d-216">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="e098d-217">No</span><span class="sxs-lookup"><span data-stu-id="e098d-217">No</span></span> | <span data-ttu-id="e098d-218">No</span><span class="sxs-lookup"><span data-stu-id="e098d-218">No</span></span> | <span data-ttu-id="e098d-219">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="e098d-219">N\A</span></span> | <span data-ttu-id="e098d-220">No</span><span class="sxs-lookup"><span data-stu-id="e098d-220">No</span></span> | <span data-ttu-id="e098d-221">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="e098d-221">N\A</span></span> |
| <span data-ttu-id="e098d-222">**Các mốc quan trọng của mô tả hợp đồng tích hợp Project Operations (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="e098d-222">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="e098d-223">No</span><span class="sxs-lookup"><span data-stu-id="e098d-223">No</span></span> | <span data-ttu-id="e098d-224">No</span><span class="sxs-lookup"><span data-stu-id="e098d-224">No</span></span> | <span data-ttu-id="e098d-225">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="e098d-225">N\A</span></span> | <span data-ttu-id="e098d-226">No</span><span class="sxs-lookup"><span data-stu-id="e098d-226">No</span></span> | <span data-ttu-id="e098d-227">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="e098d-227">N\A</span></span> |
| <span data-ttu-id="e098d-228">**Thực thể tích hợp Project Operations để ước tính chi phí (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="e098d-228">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="e098d-229">No</span><span class="sxs-lookup"><span data-stu-id="e098d-229">No</span></span> | <span data-ttu-id="e098d-230">No</span><span class="sxs-lookup"><span data-stu-id="e098d-230">No</span></span> | <span data-ttu-id="e098d-231">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="e098d-231">N\A</span></span> | <span data-ttu-id="e098d-232">No</span><span class="sxs-lookup"><span data-stu-id="e098d-232">No</span></span> | <span data-ttu-id="e098d-233">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="e098d-233">N\A</span></span> |
| <span data-ttu-id="e098d-234">**Thực thể tích hợp Project Operations để ước tính giờ (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="e098d-234">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="e098d-235">No</span><span class="sxs-lookup"><span data-stu-id="e098d-235">No</span></span> | <span data-ttu-id="e098d-236">No</span><span class="sxs-lookup"><span data-stu-id="e098d-236">No</span></span> | <span data-ttu-id="e098d-237">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="e098d-237">N\A</span></span> | <span data-ttu-id="e098d-238">No</span><span class="sxs-lookup"><span data-stu-id="e098d-238">No</span></span> | <span data-ttu-id="e098d-239">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="e098d-239">N\A</span></span> |
| <span data-ttu-id="e098d-240">**Thực thể xuất chi phí dự án tích hợp Project Operations (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="e098d-240">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="e098d-241">Có</span><span class="sxs-lookup"><span data-stu-id="e098d-241">Yes</span></span> | <span data-ttu-id="e098d-242">No</span><span class="sxs-lookup"><span data-stu-id="e098d-242">No</span></span> | <span data-ttu-id="e098d-243">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="e098d-243">N\A</span></span> | <span data-ttu-id="e098d-244">No</span><span class="sxs-lookup"><span data-stu-id="e098d-244">No</span></span> | <span data-ttu-id="e098d-245">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="e098d-245">N\A</span></span> |
| <span data-ttu-id="e098d-246">**Thực thể tích hợp Project Operations để ước tính giờ (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="e098d-246">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="e098d-247">Có</span><span class="sxs-lookup"><span data-stu-id="e098d-247">Yes</span></span> | <span data-ttu-id="e098d-248">No</span><span class="sxs-lookup"><span data-stu-id="e098d-248">No</span></span> | <span data-ttu-id="e098d-249">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="e098d-249">N\A</span></span> | <span data-ttu-id="e098d-250">No</span><span class="sxs-lookup"><span data-stu-id="e098d-250">No</span></span> | <span data-ttu-id="e098d-251">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="e098d-251">N\A</span></span> |

4. <span data-ttu-id="e098d-252">Để làm mới thực thể, hãy chọn tên bản đồ, sau đó chọn **Làm mới thực thể**.</span><span class="sxs-lookup"><span data-stu-id="e098d-252">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 
5. <span data-ttu-id="e098d-253">Tiếp tục chạy bản đồ sau khi quá trình làm mới hoàn tất.</span><span class="sxs-lookup"><span data-stu-id="e098d-253">Proceed with running the map after the refresh is complete.</span></span>

![Làm mới bản đồ](./media/20RefreshMapping.png)

<span data-ttu-id="e098d-255">Trước khi bạn bật bản đồ tiếp theo, hãy xác minh rằng bản đồ trong bảng ở trạng thái **Đang chạy**.</span><span class="sxs-lookup"><span data-stu-id="e098d-255">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="e098d-256">Việc chạy bản đồ với số lượng điều kiện tiên quyết lớn hơn có thể mất một chút thời gian.</span><span class="sxs-lookup"><span data-stu-id="e098d-256">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="e098d-257">Để chạy bản đồ với các điều kiện tiên quyết, hãy bật tùy chọn chuyển đổi **Hiển thị bản đồ thực thể liên quan**.</span><span class="sxs-lookup"><span data-stu-id="e098d-257">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="e098d-258">Nếu bảng cho biết **Đồng bộ hóa ban đầu điều kiện tiên quyết** là **Không**, hãy xác minh rằng cờ **Đồng bộ ban đầu** đang **Tắt** trong tất cả các bản đồ tiên quyết trước khi bạn chạy.</span><span class="sxs-lookup"><span data-stu-id="e098d-258">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Chạy bản đồ](./media/21RunMap.png)

6. <span data-ttu-id="e098d-260">Xác thực tất cả các bản đồ liên quan đến dự án đang ở trạng thái đang chạy.</span><span class="sxs-lookup"><span data-stu-id="e098d-260">Validate all project related maps are in the running state.</span></span>

![Tất cả các bản đồ đang chạy](./media/22AllMapsRunning.png)

<span data-ttu-id="e098d-262">Môi trường Project Operations của bạn hiện đã được cung cấp và đặt cấu hình.</span><span class="sxs-lookup"><span data-stu-id="e098d-262">Your Project Operations environment is now provisioned and configured.</span></span>
