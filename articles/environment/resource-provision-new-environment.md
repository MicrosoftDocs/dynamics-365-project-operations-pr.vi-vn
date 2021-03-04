---
title: Cung cấp môi trường mới
description: Chủ đề này cung cấp thông tin về cách cung cấp môi trường Project Operations mới.
author: sigitac
manager: Annbe
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 09af2a7693c45d1d0b9c75420d018cc50d2cc0fa
ms.sourcegitcommit: 04c446746aad97fc3f4c3d441983c586b918a3a6
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 12/11/2020
ms.locfileid: "4727816"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="e0dba-103">Cung cấp môi trường mới</span><span class="sxs-lookup"><span data-stu-id="e0dba-103">Provision a new environment</span></span>

<span data-ttu-id="e0dba-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_</span><span class="sxs-lookup"><span data-stu-id="e0dba-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="e0dba-105">Chủ đề này cung cấp thông tin về cách cung cấp môi trường Dynamics 365 Project Operations cho các tình huống dựa trên nguồn lực/hàng không trữ kho.</span><span class="sxs-lookup"><span data-stu-id="e0dba-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="e0dba-106">Bật quy trình tự động cung cấp Project Operations trong dự án LCS</span><span class="sxs-lookup"><span data-stu-id="e0dba-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="e0dba-107">Sử dụng các bước sau để bật quy trình tự động cung cấp Project Operations cho dự án LCS của bạn.</span><span class="sxs-lookup"><span data-stu-id="e0dba-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="e0dba-108">Chuyển đến [LCS](https://lcs.dynamics.com/v2) và chọn ngăn xếp **Quản lý tính năng xem trước**.</span><span class="sxs-lookup"><span data-stu-id="e0dba-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="e0dba-109">Trong danh sách **Tính năng xem trước**, hãy chọn **Tính năng Project Operations**, sau đó chọn **Đã bật tính năng xem trước** để kích hoạt Project Operations.</span><span class="sxs-lookup"><span data-stu-id="e0dba-109">In the **Preview feature** list, select **Project Operations Feature**, and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="e0dba-110">Bước này chỉ được thực hiện một lần cho mỗi dự án LCS.</span><span class="sxs-lookup"><span data-stu-id="e0dba-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="e0dba-111">Cung cấp môi trường Project Operations</span><span class="sxs-lookup"><span data-stu-id="e0dba-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="e0dba-112">Mở Dynamics 365 Finance mới [môi trường demo](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) hoặc triển khai [môi trường sản xuất/hộp cát](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure).</span><span class="sxs-lookup"><span data-stu-id="e0dba-112">Open a new Dynamics 365 Finance [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="e0dba-113">Tìm hiểu trình hướng dẫn **Cung cấp môi trường**.</span><span class="sxs-lookup"><span data-stu-id="e0dba-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="e0dba-114">Đảm bảo phiên bản ứng dụng đã chọn là 10.0.13 trở lên.</span><span class="sxs-lookup"><span data-stu-id="e0dba-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="e0dba-115">Để cung cấp Project Operations, trong phần **Cài đặt nâng cao**, hãy chọn **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="e0dba-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="e0dba-116">Bật **Thiết đặt Common Data Service** bằng việc chọn **Có** và sau đó nhập thông tin vào các trường bắt buộc:</span><span class="sxs-lookup"><span data-stu-id="e0dba-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="e0dba-117">Tên</span><span class="sxs-lookup"><span data-stu-id="e0dba-117">Name</span></span>
  - <span data-ttu-id="e0dba-118">Khu vực</span><span class="sxs-lookup"><span data-stu-id="e0dba-118">Region</span></span>
  - <span data-ttu-id="e0dba-119">Ngôn ngữ</span><span class="sxs-lookup"><span data-stu-id="e0dba-119">Language</span></span>
  - <span data-ttu-id="e0dba-120">Tiền tệ</span><span class="sxs-lookup"><span data-stu-id="e0dba-120">Currency</span></span>
 
5. <span data-ttu-id="e0dba-121">Trong trường **Mẫu Common Data Service**, hãy chọn **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="e0dba-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="e0dba-122">Chọn loại môi trường để triển khai.</span><span class="sxs-lookup"><span data-stu-id="e0dba-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="e0dba-123">Bản dùng thử dựa trên đăng ký sẽ cho phép bạn triển khai môi trường CDS trong 30 ngày.</span><span class="sxs-lookup"><span data-stu-id="e0dba-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Cài đặt triển khai](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="e0dba-125">Chọn **Đồng ý** để xác nhận các điều khoản dịch vụ và sau đó chọn **Xong** để quay lại cài đặt triển khai.</span><span class="sxs-lookup"><span data-stu-id="e0dba-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Đồng ý triển khai](./media/2DeploymentConsent.png)

7. <span data-ttu-id="e0dba-127">Không bắt buộc - Áp dụng dữ liệu demo cho môi trường.</span><span class="sxs-lookup"><span data-stu-id="e0dba-127">Optional - Apply demo data to the environment.</span></span> <span data-ttu-id="e0dba-128">Đi đến **Cài đặt nâng cao**, chọn **Tuy chỉnh cấu hình Cơ sở dữ liệu SQL** rồi đặt tùy chọn **Xác định tập dữ liệu cho cơ sở dữ liệu ứng dụng** thành **Demo**.</span><span class="sxs-lookup"><span data-stu-id="e0dba-128">Go to **Advanced settings**, select **Customize SQL Database Configuration**, and set **Specify a dataset for Application database** to **Demo**.</span></span>

8. <span data-ttu-id="e0dba-129">Hoàn thành các trường bắt buộc còn lại trong trình hướng dẫn và xác nhận việc triển khai.</span><span class="sxs-lookup"><span data-stu-id="e0dba-129">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="e0dba-130">Thời gian cung cấp môi trường sẽ khác nhau tùy theo loại môi trường.</span><span class="sxs-lookup"><span data-stu-id="e0dba-130">The time to provision the environment varies based on the environment type.</span></span> <span data-ttu-id="e0dba-131">Việc cung cấp có thể mất đến sáu giờ.</span><span class="sxs-lookup"><span data-stu-id="e0dba-131">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="e0dba-132">Sau khi quá trình triển khai hoàn tất thành công, môi trường sẽ hiển thị là **Đã triển khai**.</span><span class="sxs-lookup"><span data-stu-id="e0dba-132">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

9. <span data-ttu-id="e0dba-133">Để chắc chắn rằng môi trường đã được triển khai thành công, hãy chọn **Đăng nhập** rồi đăng nhập vào môi trường cần xác nhận.</span><span class="sxs-lookup"><span data-stu-id="e0dba-133">To confirm that the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![Chi tiết môi trường](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="e0dba-135">Áp dụng nội dung cập nhật cho môi trường Finance</span><span class="sxs-lookup"><span data-stu-id="e0dba-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="e0dba-136">Project Operations yêu cầu môi trường Finance có phiên bản ứng dụng **10.0.13 (10.0.569.20009)** trở lên.</span><span class="sxs-lookup"><span data-stu-id="e0dba-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="e0dba-137">Bạn có thể cần áp dụng các bản cập nhật chất lượng cho môi trường Finance của mình để nhận được phiên bản này.</span><span class="sxs-lookup"><span data-stu-id="e0dba-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="e0dba-138">Trong LCS, trên trang **Chi tiết môi trường**, trong phần **Bản cập nhật có sẵn**, hãy chọn **Xem bản cập nhật**.</span><span class="sxs-lookup"><span data-stu-id="e0dba-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Xem bản cập nhập](./media/5ViewUpdates.png)

2. <span data-ttu-id="e0dba-140">Trên trang **Bản cập nhật nhị phân**, hãy chọn **Lưu gói.**</span><span class="sxs-lookup"><span data-stu-id="e0dba-140">On the **Binary updates** page, select **Save package.**</span></span>

![Lưu gói](./media/6SavePackage.png)

3. <span data-ttu-id="e0dba-142">Nhấp vào **Chọn tất cả** rồi chọn **Lưu gói**.</span><span class="sxs-lookup"><span data-stu-id="e0dba-142">Click **Select all** and then select **Save package**.</span></span>

![Xem lại và lưu bản cập nhật](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="e0dba-144">Nhập tên và mô tả của gói, sau đó chọn **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="e0dba-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="e0dba-145">Tùy thuộc vào kết nối Internet, quá trình này có thể mất một chút thời gian.</span><span class="sxs-lookup"><span data-stu-id="e0dba-145">Depending on the internet connection, this process might take some time.</span></span>

![Tải gói lên Thư viện tài sản](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="e0dba-147">Sau khi gói được lưu, hãy chọn **Xong** và lưu gói này vào Thư viện tài sản trong dự án LCS của bạn.</span><span class="sxs-lookup"><span data-stu-id="e0dba-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="e0dba-148">Việc lưu và xác nhận gói có thể mất khoảng 15 phút.</span><span class="sxs-lookup"><span data-stu-id="e0dba-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="e0dba-149">Để áp dụng bản cập nhật, hãy điều hướng đến trang **Môi trường chi tiết** trong LCS và chọn **Duy trì** > **Áp dụng bản cập nhật**.</span><span class="sxs-lookup"><span data-stu-id="e0dba-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Duy trì môi trường](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="e0dba-151">Trong danh sách bản cập nhật, hãy chọn gói bạn đã tạo và chọn **Áp dụng**.</span><span class="sxs-lookup"><span data-stu-id="e0dba-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Áp dụng bản cập nhật](./media/10ApplyUpdates.png)

<span data-ttu-id="e0dba-153">Việc cung cấp dịch vụ môi trường sẽ mất một thời gian.</span><span class="sxs-lookup"><span data-stu-id="e0dba-153">Environment servicing will take some time.</span></span> <span data-ttu-id="e0dba-154">Sau khi hoàn tất, môi trường sẽ trở lại trạng thái đã triển khai.</span><span class="sxs-lookup"><span data-stu-id="e0dba-154">After it is complete, the environment will return to a deployed state.</span></span>

![Đã triển khai môi trường](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="e0dba-156">Thiết lập kết nối Ghi kép</span><span class="sxs-lookup"><span data-stu-id="e0dba-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="e0dba-157">Trong dự án LCS của bạn, hãy chuyển đến trang **Chi tiết môi trường**.</span><span class="sxs-lookup"><span data-stu-id="e0dba-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="e0dba-158">Trong phần **Thông tin môi trường Common Data Service**, hãy chọn **Liên kết tới CDS for Apps**.</span><span class="sxs-lookup"><span data-stu-id="e0dba-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="e0dba-159">Sau khi liên kết hoàn tất, hãy chọn **Liên kết tới CDS for Apps** lần nữa.</span><span class="sxs-lookup"><span data-stu-id="e0dba-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="e0dba-160">Bạn sẽ được chuyển hướng đến Ghi kép trong Finance.</span><span class="sxs-lookup"><span data-stu-id="e0dba-160">You will be redirected to Dual Write in Finance.</span></span>

![Liên kết tới CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="e0dba-162">Chọn **Áp dụng giải pháp** để truy cập vào các thực thể sẽ được ánh xạ trong tích hợp.</span><span class="sxs-lookup"><span data-stu-id="e0dba-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Áp dụng giải pháp](./media/13ApplySolutions.png)

5. <span data-ttu-id="e0dba-164">Chọn cả 2 giải pháp là Bản đồ thực thể ghi kép **Dynamics 365 Finance and Operations** và **Bản đồ thực thể ghi kép Dynamics 365 Project Operations** rồi chọn **Áp dụng**.</span><span class="sxs-lookup"><span data-stu-id="e0dba-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Xác nhận giải pháp](./media/14ConfirmSolutions.png)

<span data-ttu-id="e0dba-166">Sau khi các giải pháp được áp dụng, các thực thể Ghi kép được áp dụng cho môi trường.</span><span class="sxs-lookup"><span data-stu-id="e0dba-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Đang áp dụng giải pháp](./media/15ApplyingSolutions.png)

<span data-ttu-id="e0dba-168">Sau khi các thực thể được áp dụng, tất cả các ánh xạ có sẵn sẽ được liệt kê trong môi trường.</span><span class="sxs-lookup"><span data-stu-id="e0dba-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Bản đồ ghi kép](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="e0dba-170">Làm mới các thực thể dữ liệu sau khi cập nhật</span><span class="sxs-lookup"><span data-stu-id="e0dba-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="e0dba-171">Trong Finance, hãy chuyển đến không gian làm việc **Quản lý dữ liệu**.</span><span class="sxs-lookup"><span data-stu-id="e0dba-171">In Finance, go to the **Data management** workspace.</span></span>

![Không gian làm việc quản lý dữ liệu](./media/16DataManagement.png)

2. <span data-ttu-id="e0dba-173">Chọn ngăn xếp **Tham số khung**.</span><span class="sxs-lookup"><span data-stu-id="e0dba-173">Select the **Framework parameters** tile.</span></span>

![Tham số khung](./media/17FrameworkParameters.png)

3. <span data-ttu-id="e0dba-175">Trên trang **Cài đặt thực thể**, hãy chọn **Làm mới danh sách thực thể**.</span><span class="sxs-lookup"><span data-stu-id="e0dba-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Làm mới danh sách thực thể](./media/18RefreshEntityList.png)

<span data-ttu-id="e0dba-177">Quá trình làm mới sẽ mất khoảng 20 phút.</span><span class="sxs-lookup"><span data-stu-id="e0dba-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="e0dba-178">Bạn sẽ nhận được một cảnh báo khi quá trình hoàn tất.</span><span class="sxs-lookup"><span data-stu-id="e0dba-178">You will receive an alert when it is complete.</span></span>

![Xác nhận làm mới](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a><span data-ttu-id="e0dba-180">Cập nhật các tùy chọn cài đặt bảo mật trong Project Operations trên Dataverse</span><span class="sxs-lookup"><span data-stu-id="e0dba-180">Update security settings on Project Operations on Dataverse</span></span>

1. <span data-ttu-id="e0dba-181">Đi đến Project Operations trên môi trường Dataverse của bạn.</span><span class="sxs-lookup"><span data-stu-id="e0dba-181">Go to Project Operations on your Dataverse environment.</span></span> 
2. <span data-ttu-id="e0dba-182">Đi đến **Cài đặt** > **Bảo mật** > **Vai trò bảo mật**.</span><span class="sxs-lookup"><span data-stu-id="e0dba-182">Go to **Settings** > **Security** > **Security roles**.</span></span> 
3. <span data-ttu-id="e0dba-183">Trên trang **Vai trò bảo mật**, trong danh sách vai trò, hãy chọn **người dùng ứng dụng ghi kép** rồi chọn tab **Thực thể tùy chỉnh**.</span><span class="sxs-lookup"><span data-stu-id="e0dba-183">On the **Security roles** page, in the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span>  
4. <span data-ttu-id="e0dba-184">Xác minh rằng vai trò có quyền **Đọc** và **Gắn thêm vào** đối với:</span><span class="sxs-lookup"><span data-stu-id="e0dba-184">Verify that the role has **Read** and **Append To** permissions for the:</span></span>
      
      - <span data-ttu-id="e0dba-185">**Loại tỷ giá hối đoái**</span><span class="sxs-lookup"><span data-stu-id="e0dba-185">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="e0dba-186">**Biểu đồ tài khoản**</span><span class="sxs-lookup"><span data-stu-id="e0dba-186">**Chart Of Accounts**</span></span>
      - <span data-ttu-id="e0dba-187">**Lịch tài khóa**</span><span class="sxs-lookup"><span data-stu-id="e0dba-187">**Fiscal Calendar**</span></span>
      - <span data-ttu-id="e0dba-188">**Sổ cái**</span><span class="sxs-lookup"><span data-stu-id="e0dba-188">**Ledger**</span></span>

5. <span data-ttu-id="e0dba-189">Sau khi cập nhật xong vai trò bảo mật, hãy đi đến **Cài đặt** > **Bảo mật** > **Nhóm**, rồi chọn nhóm mặc định trong chế độ xem nhóm **Chủ sở hữu doanh nghiệp địa phương**.</span><span class="sxs-lookup"><span data-stu-id="e0dba-189">After the security role is updated, go to **Settings** > **Security** > **Teams**, and select the default team in the **Local Business Owner** team view.</span></span>
6. <span data-ttu-id="e0dba-190">Chọn **Quản lý vai trò** và xác minh rằng quyền bảo mật **người dùng ứng dụng ghi kép** đã được áp dụng cho nhóm này.</span><span class="sxs-lookup"><span data-stu-id="e0dba-190">Select **Manage Roles** and verify that the **dual-write app user** security privilege is applied to this team.</span></span>

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="e0dba-191">Chạy bản đồ ghi kép Project Operations</span><span class="sxs-lookup"><span data-stu-id="e0dba-191">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="e0dba-192">Trong dự án LCS của bạn, hãy chuyển đến trang **Chi tiết môi trường**.</span><span class="sxs-lookup"><span data-stu-id="e0dba-192">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="e0dba-193">Trong phần **Thông tin môi trường Common Data Service**, hãy chọn **Liên kết tới CDS for Apps.**</span><span class="sxs-lookup"><span data-stu-id="e0dba-193">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="e0dba-194">Sau khi bạn chọn liên kết, bạn sẽ được chuyển hướng đến danh sách các thực thể trong ánh xạ.</span><span class="sxs-lookup"><span data-stu-id="e0dba-194">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="e0dba-195">Bắt đầu bản đồ như mô tả trong bảng sau.</span><span class="sxs-lookup"><span data-stu-id="e0dba-195">Start the maps as described in the following table.</span></span> <span data-ttu-id="e0dba-196">Đảm bảo làm theo trình tự như đã liệt kê.</span><span class="sxs-lookup"><span data-stu-id="e0dba-196">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="e0dba-197">**Sơ đồ thực thể**</span><span class="sxs-lookup"><span data-stu-id="e0dba-197">**Entity Map**</span></span> | <span data-ttu-id="e0dba-198">**Làm mới thực thể**</span><span class="sxs-lookup"><span data-stu-id="e0dba-198">**Refresh entity**</span></span> | <span data-ttu-id="e0dba-199">**Đồng bộ ban đầu**</span><span class="sxs-lookup"><span data-stu-id="e0dba-199">**Initial sync**</span></span> | <span data-ttu-id="e0dba-200">**Bản cái cho đồng bộ hóa ban đầu**</span><span class="sxs-lookup"><span data-stu-id="e0dba-200">**Master for initial sync**</span></span> | <span data-ttu-id="e0dba-201">**Chạy điều kiện tiên quyết**</span><span class="sxs-lookup"><span data-stu-id="e0dba-201">**Run prerequisites**</span></span> | <span data-ttu-id="e0dba-202">**Đồng bộ hóa ban đầu điều kiện tiên quyết**</span><span class="sxs-lookup"><span data-stu-id="e0dba-202">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="e0dba-203">**Vai trò nguồn lực dự án cho tất cả các công ty (các thể loại nguồn lực có thể đăng ký trước)**</span><span class="sxs-lookup"><span data-stu-id="e0dba-203">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="e0dba-204">No</span><span class="sxs-lookup"><span data-stu-id="e0dba-204">No</span></span> | <span data-ttu-id="e0dba-205">Có</span><span class="sxs-lookup"><span data-stu-id="e0dba-205">Yes</span></span> | <span data-ttu-id="e0dba-206">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="e0dba-206">Common Data Service</span></span> | <span data-ttu-id="e0dba-207">No</span><span class="sxs-lookup"><span data-stu-id="e0dba-207">No</span></span> | <span data-ttu-id="e0dba-208">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="e0dba-208">N\A</span></span> |
| <span data-ttu-id="e0dba-209">**Thực thể pháp lý (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="e0dba-209">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="e0dba-210">No</span><span class="sxs-lookup"><span data-stu-id="e0dba-210">No</span></span> | <span data-ttu-id="e0dba-211">Có</span><span class="sxs-lookup"><span data-stu-id="e0dba-211">Yes</span></span> | <span data-ttu-id="e0dba-212">Ứng dụng Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e0dba-212">Finance and Operations apps</span></span> | <span data-ttu-id="e0dba-213">No</span><span class="sxs-lookup"><span data-stu-id="e0dba-213">No</span></span> | <span data-ttu-id="e0dba-214">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="e0dba-214">N\A</span></span> |
| <span data-ttu-id="e0dba-215">**Sổ cái (msdyn_ledgers)**</span><span class="sxs-lookup"><span data-stu-id="e0dba-215">**Ledger (msdyn_ledgers)**</span></span> | <span data-ttu-id="e0dba-216">No</span><span class="sxs-lookup"><span data-stu-id="e0dba-216">No</span></span> | <span data-ttu-id="e0dba-217">Có</span><span class="sxs-lookup"><span data-stu-id="e0dba-217">Yes</span></span> | <span data-ttu-id="e0dba-218">Ứng dụng Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e0dba-218">Finance and Operations apps</span></span> | <span data-ttu-id="e0dba-219">Có</span><span class="sxs-lookup"><span data-stu-id="e0dba-219">Yes</span></span> | <span data-ttu-id="e0dba-220">Có, các ứng dụng Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e0dba-220">Yes, Finance and Operations apps</span></span> |
| <span data-ttu-id="e0dba-221">**Giá trị tích hợp thực tế của Project Operations (msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="e0dba-221">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="e0dba-222">No</span><span class="sxs-lookup"><span data-stu-id="e0dba-222">No</span></span> | <span data-ttu-id="e0dba-223">No</span><span class="sxs-lookup"><span data-stu-id="e0dba-223">No</span></span> | <span data-ttu-id="e0dba-224">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="e0dba-224">N\A</span></span> | <span data-ttu-id="e0dba-225">Có</span><span class="sxs-lookup"><span data-stu-id="e0dba-225">Yes</span></span> | <span data-ttu-id="e0dba-226">No</span><span class="sxs-lookup"><span data-stu-id="e0dba-226">No</span></span> |
| <span data-ttu-id="e0dba-227">**Mô tả hợp đồng dự án (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="e0dba-227">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="e0dba-228">No</span><span class="sxs-lookup"><span data-stu-id="e0dba-228">No</span></span> | <span data-ttu-id="e0dba-229">No</span><span class="sxs-lookup"><span data-stu-id="e0dba-229">No</span></span> | <span data-ttu-id="e0dba-230">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="e0dba-230">N\A</span></span> | <span data-ttu-id="e0dba-231">No</span><span class="sxs-lookup"><span data-stu-id="e0dba-231">No</span></span> | <span data-ttu-id="e0dba-232">No</span><span class="sxs-lookup"><span data-stu-id="e0dba-232">No</span></span> |
| <span data-ttu-id="e0dba-233">**Thực thể tích hợp cho các mối quan hệ giao dịch dự án (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="e0dba-233">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="e0dba-234">No</span><span class="sxs-lookup"><span data-stu-id="e0dba-234">No</span></span> | <span data-ttu-id="e0dba-235">No</span><span class="sxs-lookup"><span data-stu-id="e0dba-235">No</span></span> | <span data-ttu-id="e0dba-236">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="e0dba-236">N\A</span></span> | <span data-ttu-id="e0dba-237">No</span><span class="sxs-lookup"><span data-stu-id="e0dba-237">No</span></span> | <span data-ttu-id="e0dba-238">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="e0dba-238">N\A</span></span> |
| <span data-ttu-id="e0dba-239">**Các mốc quan trọng của mô tả hợp đồng tích hợp Project Operations (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="e0dba-239">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="e0dba-240">No</span><span class="sxs-lookup"><span data-stu-id="e0dba-240">No</span></span> | <span data-ttu-id="e0dba-241">No</span><span class="sxs-lookup"><span data-stu-id="e0dba-241">No</span></span> | <span data-ttu-id="e0dba-242">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="e0dba-242">N\A</span></span> | <span data-ttu-id="e0dba-243">No</span><span class="sxs-lookup"><span data-stu-id="e0dba-243">No</span></span> | <span data-ttu-id="e0dba-244">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="e0dba-244">N\A</span></span> |
| <span data-ttu-id="e0dba-245">**Thực thể tích hợp Project Operations để ước tính chi phí (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="e0dba-245">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="e0dba-246">No</span><span class="sxs-lookup"><span data-stu-id="e0dba-246">No</span></span> | <span data-ttu-id="e0dba-247">No</span><span class="sxs-lookup"><span data-stu-id="e0dba-247">No</span></span> | <span data-ttu-id="e0dba-248">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="e0dba-248">N\A</span></span> | <span data-ttu-id="e0dba-249">No</span><span class="sxs-lookup"><span data-stu-id="e0dba-249">No</span></span> | <span data-ttu-id="e0dba-250">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="e0dba-250">N\A</span></span> |
| <span data-ttu-id="e0dba-251">**Thực thể xuất danh mục chi phí dự án tích hợp Project Operations (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="e0dba-251">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="e0dba-252">No</span><span class="sxs-lookup"><span data-stu-id="e0dba-252">No</span></span> | <span data-ttu-id="e0dba-253">No</span><span class="sxs-lookup"><span data-stu-id="e0dba-253">No</span></span> | <span data-ttu-id="e0dba-254">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="e0dba-254">N\A</span></span> | <span data-ttu-id="e0dba-255">No</span><span class="sxs-lookup"><span data-stu-id="e0dba-255">No</span></span> | <span data-ttu-id="e0dba-256">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="e0dba-256">N\A</span></span> |
| <span data-ttu-id="e0dba-257">**Thực thể xuất chi phí dự án tích hợp Project Operations (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="e0dba-257">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="e0dba-258">Có</span><span class="sxs-lookup"><span data-stu-id="e0dba-258">Yes</span></span> | <span data-ttu-id="e0dba-259">No</span><span class="sxs-lookup"><span data-stu-id="e0dba-259">No</span></span> | <span data-ttu-id="e0dba-260">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="e0dba-260">N\A</span></span> | <span data-ttu-id="e0dba-261">No</span><span class="sxs-lookup"><span data-stu-id="e0dba-261">No</span></span> | <span data-ttu-id="e0dba-262">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="e0dba-262">N\A</span></span> |
| <span data-ttu-id="e0dba-263">**Thực thể tích hợp Project Operations để ước tính giờ (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="e0dba-263">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="e0dba-264">Có</span><span class="sxs-lookup"><span data-stu-id="e0dba-264">Yes</span></span> | <span data-ttu-id="e0dba-265">No</span><span class="sxs-lookup"><span data-stu-id="e0dba-265">No</span></span> | <span data-ttu-id="e0dba-266">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="e0dba-266">N\A</span></span> | <span data-ttu-id="e0dba-267">No</span><span class="sxs-lookup"><span data-stu-id="e0dba-267">No</span></span> | <span data-ttu-id="e0dba-268">Không áp dụng</span><span class="sxs-lookup"><span data-stu-id="e0dba-268">N\A</span></span> |


4. <span data-ttu-id="e0dba-269">Để làm mới thực thể, hãy chọn tên bản đồ, sau đó chọn **Làm mới thực thể**.</span><span class="sxs-lookup"><span data-stu-id="e0dba-269">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Làm mới bản đồ](./media/20RefreshMapping.png)

5. <span data-ttu-id="e0dba-271">Sau khi quá trình làm mới hoàn tất, hãy chạy bản đồ.</span><span class="sxs-lookup"><span data-stu-id="e0dba-271">After the refresh is complete, run the map.</span></span> <span data-ttu-id="e0dba-272">Trước khi bạn bật bản đồ tiếp theo, hãy xác minh rằng bản đồ trong bảng ở trạng thái **Đang chạy**.</span><span class="sxs-lookup"><span data-stu-id="e0dba-272">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="e0dba-273">Việc chạy bản đồ với số lượng điều kiện tiên quyết lớn hơn có thể mất một chút thời gian.</span><span class="sxs-lookup"><span data-stu-id="e0dba-273">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="e0dba-274">Để chạy bản đồ với các điều kiện tiên quyết, hãy bật tùy chọn chuyển đổi **Hiển thị bản đồ thực thể liên quan**.</span><span class="sxs-lookup"><span data-stu-id="e0dba-274">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="e0dba-275">Nếu bảng cho biết **Đồng bộ hóa ban đầu điều kiện tiên quyết** là **Không**, hãy xác minh rằng cờ **Đồng bộ ban đầu** đang **Tắt** trong tất cả các bản đồ tiên quyết trước khi bạn chạy.</span><span class="sxs-lookup"><span data-stu-id="e0dba-275">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Chạy bản đồ](./media/21RunMap.png)

6. <span data-ttu-id="e0dba-277">Xác thực tất cả các bản đồ liên quan đến dự án đang ở trạng thái đang chạy.</span><span class="sxs-lookup"><span data-stu-id="e0dba-277">Validate all project related maps are in the running state.</span></span>

![Tất cả các bản đồ đang chạy](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a><span data-ttu-id="e0dba-279">Áp dụng dữ liệu cấu hình trong CDS cho Project Operations (tùy chọn)</span><span class="sxs-lookup"><span data-stu-id="e0dba-279">Apply configuration data in CDS for Project Operations (optional)</span></span>

<span data-ttu-id="e0dba-280">Nếu bạn đã áp dụng dữ liệu demo cho môi trường Tài chính, hãy xem [Thiết lập và áp dụng dữ liệu cấu hình trong Common Data Service cho Project Operations](resource-apply-pro-setup-config-data.md) để áp dụng dữ liệu demo cho môi trường CDS.</span><span class="sxs-lookup"><span data-stu-id="e0dba-280">If you have applied demo data to the Finance environment, see [Set up and apply configuration data in the Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) to apply demo data to CDS environment.</span></span>


<span data-ttu-id="e0dba-281">Môi trường Project Operations của bạn hiện đã được cung cấp và đặt cấu hình.</span><span class="sxs-lookup"><span data-stu-id="e0dba-281">Your Project Operations environment is now provisioned and configured.</span></span> 
