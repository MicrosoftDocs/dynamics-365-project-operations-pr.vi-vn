---
title: Cập nhật Project Operations trong môi trường Tài chính
description: Chủ đề này cung cấp thông tin về cách cập nhật Project Operations trong môi trường Dynamics 365 Finance.
author: ruhercul
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d85a180aa094a048b4422605b25151d10785f67d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011082"
---
# <a name="update-project-operations-in-your-finance-environment"></a><span data-ttu-id="65d2a-103">Cập nhật Project Operations trong môi trường Tài chính</span><span class="sxs-lookup"><span data-stu-id="65d2a-103">Update Project Operations in your Finance environment</span></span>

<span data-ttu-id="65d2a-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_</span><span class="sxs-lookup"><span data-stu-id="65d2a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="65d2a-105">Chủ đề này cung cấp thông tin về cách cập nhật Dynamics 365 Project Operations trong môi trường Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="65d2a-105">This topic provides information about how to update Dynamics 365 Project Operations in your Dynamics 365 Finance environment.</span></span> <span data-ttu-id="65d2a-106">Bạn phải làm theo 3 quy trình để cập nhật Project Operations lên Bản cập nhật 5 (UR5):</span><span class="sxs-lookup"><span data-stu-id="65d2a-106">There are three procedures that are required to update Project Operations to Update 5 (UR5):</span></span>

- [<span data-ttu-id="65d2a-107">Nhập gói vào dự án thử nghiệm</span><span class="sxs-lookup"><span data-stu-id="65d2a-107">Import the package into your preview project</span></span>](#import)
- [<span data-ttu-id="65d2a-108">Áp dụng bản cập nhật</span><span class="sxs-lookup"><span data-stu-id="65d2a-108">Apply the update</span></span>](#apply)
- [<span data-ttu-id="65d2a-109">Cập nhật môi trường Dataverse</span><span class="sxs-lookup"><span data-stu-id="65d2a-109">Update your Dataverse environment</span></span>](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a><span data-ttu-id="65d2a-110">Nhập gói vào dự án LCS</span><span class="sxs-lookup"><span data-stu-id="65d2a-110">Import the package into your LCS project</span></span>

1. <span data-ttu-id="65d2a-111">Đăng nhập vào [Lifecycle Services (LCS)](https://lcs.dynamics.com/) với vai trò Chủ dự án hoặc Người quản lý môi trường.</span><span class="sxs-lookup"><span data-stu-id="65d2a-111">Sign in to [Lifecycle Services (LCS)](https://lcs.dynamics.com/) as a Project Owner or Environment manager.</span></span>
2. <span data-ttu-id="65d2a-112">Chọn dự án LCS của bạn từ danh sách dự án.</span><span class="sxs-lookup"><span data-stu-id="65d2a-112">From the list of projects, select your LCS project.</span></span>
3. <span data-ttu-id="65d2a-113">Trên trang **Dự án**, trong nhóm **Môi trường**, hãy mở môi trường bạn muốn cập nhật.</span><span class="sxs-lookup"><span data-stu-id="65d2a-113">On the **Project** page, in the **Environments** group, open the environment that you want to update.</span></span>
4. <span data-ttu-id="65d2a-114">Xác nhận rằng môi trường đó đang chạy.</span><span class="sxs-lookup"><span data-stu-id="65d2a-114">Verify that the environment is running.</span></span> <span data-ttu-id="65d2a-115">Nếu môi trường đó chưa khởi động, hãy khởi động.</span><span class="sxs-lookup"><span data-stu-id="65d2a-115">If it isn't started, start the environment.</span></span>
5. <span data-ttu-id="65d2a-116">Trong phần **Bản phát hành mới** ở trang **Các bản cập nhật hiện có**, hãy chọn **Xem bản cập nhật** để tìm bản 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="65d2a-116">In the **New release** section under **Available updates**, select **View update** for 10.0.15.</span></span>

![Nút Xem bản cập nhật](media/view-update.png)

6. <span data-ttu-id="65d2a-118">Trên trang **Bảng cập nhật nhị phân**, hãy chọn **Lưu gói**.</span><span class="sxs-lookup"><span data-stu-id="65d2a-118">On the **Binary updates** page, select **Save package**.</span></span>
7. <span data-ttu-id="65d2a-119">Trên trang **Xem lại và lưu bản cập nhật**, hãy chọn **Lưu gói**.</span><span class="sxs-lookup"><span data-stu-id="65d2a-119">On the **Review and save updates** page, select **Save package**.</span></span>
8. <span data-ttu-id="65d2a-120">Trên ngăn **Lưu gói vào thư viện tài sản** mở ra, hãy nhập tên gói rồi chọn **Lưu gói**.</span><span class="sxs-lookup"><span data-stu-id="65d2a-120">On the **Save package to asset library** pane that opens, enter the package name and then select **Save package**.</span></span>
9. <span data-ttu-id="65d2a-121">Khi LCS lưu xong gói, nút **Xong** sẽ sẵn sàng.</span><span class="sxs-lookup"><span data-stu-id="65d2a-121">When LCS has finished saving the package, the **Done** button is enabled.</span></span> <span data-ttu-id="65d2a-122">Chọn **Xong**.</span><span class="sxs-lookup"><span data-stu-id="65d2a-122">Select **Done**.</span></span> <span data-ttu-id="65d2a-123">LCS sẽ xác minh gói.</span><span class="sxs-lookup"><span data-stu-id="65d2a-123">LCS will verify the package.</span></span> <span data-ttu-id="65d2a-124">Quá trình xác minh có thể mất ít phút hoặc tối đa là 1 giờ.</span><span class="sxs-lookup"><span data-stu-id="65d2a-124">Verification can take a few minutes or up to one hour.</span></span>


## <a name="apply-the-package-update"></a><a name="apply"></a><span data-ttu-id="65d2a-125">Áp dụng bản cập nhật gói</span><span class="sxs-lookup"><span data-stu-id="65d2a-125">Apply the package update</span></span>

1. <span data-ttu-id="65d2a-126">Trong LCS, trên trang **Chi tiết môi trường**, hãy chọn **Bảo trì** > **Áp dụng bản cập nhật**.</span><span class="sxs-lookup"><span data-stu-id="65d2a-126">In LCS, on the **Environment details** page, select **Maintain** > **Apply Updates**.</span></span>
2. <span data-ttu-id="65d2a-127">Từ danh sách, hãy chọn gói bạn đã lưu trước đó rồi chọn **Áp dụng**.</span><span class="sxs-lookup"><span data-stu-id="65d2a-127">From the list, select the package that you saved earlier, and then select **Apply**.</span></span>
3. <span data-ttu-id="65d2a-128">Chọn **Có** để xác nhận rằng bạn muốn triển khai gói.</span><span class="sxs-lookup"><span data-stu-id="65d2a-128">Select **Yes** to confirm that you want to deploy the package.</span></span>

![Xác nhận hộp thoại triển khai gói](media/confirm-package-deployment.png)

4. <span data-ttu-id="65d2a-130">Chọn **Có** để xác nhận rằng bạn muốn cập nhật ứng dụng.</span><span class="sxs-lookup"><span data-stu-id="65d2a-130">Select **Yes** to confirm that you want to update the application.</span></span>

![Xác nhận hộp thoại cập nhật ứng dụng](media/confirm-application-update.png)

<span data-ttu-id="65d2a-132">Quá trình triển khai và cập nhật ứng dụng sẽ bắt đầu.</span><span class="sxs-lookup"><span data-stu-id="65d2a-132">The deployment and application update will start.</span></span> 

<span data-ttu-id="65d2a-133">Trên trang **Chi tiết môi trường**, ở góc trên cùng bên phải, trạng thái môi trường sẽ chuyển thành **Đang phục vụ**.</span><span class="sxs-lookup"><span data-stu-id="65d2a-133">On the **Environment details** page, in the top-right corner, the environment status will update to **Servicing**.</span></span> <span data-ttu-id="65d2a-134">Trong khoảng hai giờ, quá trình cập nhật sẽ hoàn tất.</span><span class="sxs-lookup"><span data-stu-id="65d2a-134">In approximately two hours, the update will be complete.</span></span> <span data-ttu-id="65d2a-135">Thông tin bản phát hành ứng dụng sẽ chuyển thành **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** và trạng thái môi trường sẽ chuyển thành **Đã triển khai**.</span><span class="sxs-lookup"><span data-stu-id="65d2a-135">The application release information will update to **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** and the environment status will update to **Deployed**.</span></span>


## <a name="update-your-dataverse-environment"></a><a name="update"></a><span data-ttu-id="65d2a-136">Cập nhật môi trường Dataverse</span><span class="sxs-lookup"><span data-stu-id="65d2a-136">Update your Dataverse environment</span></span>

1. <span data-ttu-id="65d2a-137">Đăng nhập vào [Trung tâm quản trị Power Platform](https://admin.powerplatform.com/).</span><span class="sxs-lookup"><span data-stu-id="65d2a-137">Sign in to the [Power Platform admin center](https://admin.powerplatform.com/).</span></span>
2. <span data-ttu-id="65d2a-138">Trong danh sách, hãy tìm và mở môi trường mà bạn đã dùng để cài đặt Project Operations.</span><span class="sxs-lookup"><span data-stu-id="65d2a-138">In the list, find and open the environment that you used to install Project Operations.</span></span>
3. <span data-ttu-id="65d2a-139">Trên trang **Môi trường**, hãy chọn **Nguồn lực** > **Ứng dụng Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="65d2a-139">On the **Environments** page, select **Resource** > **Dynamics 365 apps**.</span></span>
4. <span data-ttu-id="65d2a-140">Trong danh sách, hãy tìm **Microsoft Dynamics 365 Project Operations** và trong cột **Trạng thái**, hãy chọn **Có sẵn bản cập nhật**.</span><span class="sxs-lookup"><span data-stu-id="65d2a-140">In the list, locate **Microsoft Dynamics 365 Project Operations**, and in the **Status** column, select **Update Available**.</span></span>
5. <span data-ttu-id="65d2a-141">Đánh dấu vào ô **Tôi đồng ý với điều khoản dịch vụ** rồi chọn **Cập nhật**.</span><span class="sxs-lookup"><span data-stu-id="65d2a-141">Select the **I agree to the terms of service** check box, and then select **Update**.</span></span> <span data-ttu-id="65d2a-142">Phiên bản mới nhất của giải pháp sẽ được cài đặt.</span><span class="sxs-lookup"><span data-stu-id="65d2a-142">The latest version of the solution will be installed.</span></span>

<span data-ttu-id="65d2a-143">Sau khi cài đặt xong, bạn sẽ có phiên bản 4.5.0.134.</span><span class="sxs-lookup"><span data-stu-id="65d2a-143">After the installation is complete, you'll have version 4.5.0.134 installed.</span></span>

## <a name="configure-new-features"></a><span data-ttu-id="65d2a-144">Đặt cấu hình các tính năng mới</span><span class="sxs-lookup"><span data-stu-id="65d2a-144">Configure new features</span></span>

### <a name="enable-dual-write-mapping"></a><span data-ttu-id="65d2a-145">Bật ánh xạ ghi kép</span><span class="sxs-lookup"><span data-stu-id="65d2a-145">Enable dual-write mapping</span></span>

<span data-ttu-id="65d2a-146">Sau khi cập nhật xong trên môi trường Tài chính và Dataverse, bạn có thể bật các ánh xạ ghi kép cần thiết.</span><span class="sxs-lookup"><span data-stu-id="65d2a-146">After you complete the update on the Finance and Dataverse environments, you can enable the required dual-write mappings.</span></span> <span data-ttu-id="65d2a-147">Hãy hoàn tất các quy trình sau để bật ánh xạ ghi kép.</span><span class="sxs-lookup"><span data-stu-id="65d2a-147">Complete the following procedures to enable dual-write mappings.</span></span>

- [<span data-ttu-id="65d2a-148">Cập nhật các tùy chọn cài đặt bảo mật trên môi trường Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="65d2a-148">Update security settings on Customer Engagement environment</span></span>](#security)
- [<span data-ttu-id="65d2a-149">Làm mới các thực thể dữ liệu</span><span class="sxs-lookup"><span data-stu-id="65d2a-149">Refresh data entities</span></span>](#refresh)
- [<span data-ttu-id="65d2a-150">Cập nhật và chạy các ánh xạ ghi kép</span><span class="sxs-lookup"><span data-stu-id="65d2a-150">Update and run the dual-write mappings</span></span>](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a><span data-ttu-id="65d2a-151">Cập nhật các tùy chọn cài đặt bảo mật trên môi trường Dataverse</span><span class="sxs-lookup"><span data-stu-id="65d2a-151">Update security settings on the Dataverse environment</span></span>

<span data-ttu-id="65d2a-152">Các chi tiết cập nhật sau đây đối với quyền bảo mật của thực thể là bắt buộc như một phần của bản cập nhật lên UR5.</span><span class="sxs-lookup"><span data-stu-id="65d2a-152">The following updates to the security privileges for entities are required as part of the update to UR5.</span></span>

1. <span data-ttu-id="65d2a-153">Trong môi trường Dataverse, hãy đi đến **Cài đặt** và trong nhóm **Hệ thống**, hãy chọn **Bảo mật**.</span><span class="sxs-lookup"><span data-stu-id="65d2a-153">In your Dataverse environment, go to **Settings**, and in the **System** group, select **Security**.</span></span>

![Cài đặt môi trường Dataverse](media/Picture21.png)

2. <span data-ttu-id="65d2a-155">Chọn **Vai trò Bảo mật**.</span><span class="sxs-lookup"><span data-stu-id="65d2a-155">Select **Security Roles**.</span></span>
3. <span data-ttu-id="65d2a-156">Từ danh sách vai trò, hãy chọn **Người dùng ứng dụng ghi kép** rồi chọn tab **Thực thể tùy chỉnh**.</span><span class="sxs-lookup"><span data-stu-id="65d2a-156">From the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span> 
4. <span data-ttu-id="65d2a-157">Xác minh rằng vai trò có quyền **Đọc** và **Gắn thêm vào** đối với:</span><span class="sxs-lookup"><span data-stu-id="65d2a-157">Verify that the role has **Read** and **Append To** permissions for:</span></span>

      - <span data-ttu-id="65d2a-158">**Loại tỷ giá hối đoái**</span><span class="sxs-lookup"><span data-stu-id="65d2a-158">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="65d2a-159">**Biểu đồ tài khoản**</span><span class="sxs-lookup"><span data-stu-id="65d2a-159">**Chart Of Accounts**</span></span> 
      - <span data-ttu-id="65d2a-160">**Lịch tài khóa**</span><span class="sxs-lookup"><span data-stu-id="65d2a-160">**Fiscal Calendar**</span></span> 
      - <span data-ttu-id="65d2a-161">**Sổ cái**</span><span class="sxs-lookup"><span data-stu-id="65d2a-161">**Ledger**</span></span>

5. <span data-ttu-id="65d2a-162">Sau khi cập nhật xong vai trò bảo mật, hãy đi đến **Cài đặt** > **Bảo mật** > **Nhóm**.</span><span class="sxs-lookup"><span data-stu-id="65d2a-162">After the security role is updated, go to **Settings** > **Security** > **Teams**.</span></span> <span data-ttu-id="65d2a-163">Xác minh rằng vai trò **người dùng ứng dụng ghi kép** đã được áp dụng cho nhóm.</span><span class="sxs-lookup"><span data-stu-id="65d2a-163">Verify that the **dual-write app user** role has been applied to the team.</span></span> 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a><span data-ttu-id="65d2a-164">Làm mới các thực thể dữ liệu từ bản cập nhật</span><span class="sxs-lookup"><span data-stu-id="65d2a-164">Refresh data entities from the update</span></span>

1. <span data-ttu-id="65d2a-165">Trong môi trường Tài chính, hãy mở không gian làm việc **Quản lý dữ liệu** rồi mở trang **Tham số khuôn khổ**.</span><span class="sxs-lookup"><span data-stu-id="65d2a-165">In your Finance environment, open the **Data management** workspace, and then open the **Framework parameters** page.</span></span>
2. <span data-ttu-id="65d2a-166">Trên tab **Cài đặt thực thể**, hãy chọn **Làm mới danh sách thực thể**.</span><span class="sxs-lookup"><span data-stu-id="65d2a-166">On the **Entity settings** tab, select **Refresh entity list**.</span></span>
3. <span data-ttu-id="65d2a-167">Chọn **Đóng** để xác nhận việc làm mới thực thể.</span><span class="sxs-lookup"><span data-stu-id="65d2a-167">Select **Close** to confirm the entity refresh.</span></span>

 > [!NOTE]
 > <span data-ttu-id="65d2a-168">Quá trình này sẽ mất khoảng 20 phút để hoàn tất.</span><span class="sxs-lookup"><span data-stu-id="65d2a-168">This process will take approximately 20 minutes to complete.</span></span> <span data-ttu-id="65d2a-169">Bạn sẽ được thông báo khi quá trình làm mới hoàn tất.</span><span class="sxs-lookup"><span data-stu-id="65d2a-169">You will be notified when the refresh is complete.</span></span>

### <a name="update-dual-write-mappings"></a><a name="run"></a><span data-ttu-id="65d2a-170">Cập nhật ánh xạ ghi kép</span><span class="sxs-lookup"><span data-stu-id="65d2a-170">Update dual-write mappings</span></span>

1. <span data-ttu-id="65d2a-171">Trong không gian làm việc **Quản lý dữ liệu**, hãy chọn **Ghi kép**.</span><span class="sxs-lookup"><span data-stu-id="65d2a-171">In the **Data management** workspace, select **Dual-write**.</span></span>
2. <span data-ttu-id="65d2a-172">Chọn **Áp dụng giải pháp**, chọn cả 2 giải pháp trong danh sách rồi chọn **Áp dụng**.</span><span class="sxs-lookup"><span data-stu-id="65d2a-172">Select **Apply solutions**, select both solutions in the list, and then select **Apply**.</span></span>
3. <span data-ttu-id="65d2a-173">Trên trang **Ghi kép**, chọn các sơ đồ bảng sau rồi chọn **Dừng**.</span><span class="sxs-lookup"><span data-stu-id="65d2a-173">On the **Dual-write** page, select the following table maps, and then select **Stop**.</span></span>

    - <span data-ttu-id="65d2a-174">**Giá trị tích hợp thực tế của Project Operations (msdyn_actuals)**</span><span class="sxs-lookup"><span data-stu-id="65d2a-174">**Project Operations integration actuals (msdyn_actuals)**</span></span>
    - <span data-ttu-id="65d2a-175">**Hạng mục chi tiêu dự án tích hợp trong Project Operations (msdyn_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="65d2a-175">**Project Operations integration project expense categories (msdyn_expensecategories)**</span></span>
    - <span data-ttu-id="65d2a-176">**Thực thể xuất chi tiêu dự án thực tích hợp trong Project Operations (msdyn_expenses)**</span><span class="sxs-lookup"><span data-stu-id="65d2a-176">**Project Operations integration actuals project expenses export entity (msdyn_expenses)**</span></span>

4. <span data-ttu-id="65d2a-177">Trên trang **Phiên bản sơ đồ bảng**, hãy áp dụng phiên bản mới của bảng cho từng thực thể trong số 3 thực thể.</span><span class="sxs-lookup"><span data-stu-id="65d2a-177">On the **Table map version** page, apply a new version of the map to each of the three entities.</span></span>
5. <span data-ttu-id="65d2a-178">Trên trang **Ghi kép**, hãy chọn chạy để khởi động lại sơ đồ.</span><span class="sxs-lookup"><span data-stu-id="65d2a-178">On the **Dual-write** page, select run to restart the maps.</span></span>
6. <span data-ttu-id="65d2a-179">Từ danh sách sơ đồ, hãy chọn **Sổ cái (msdyn_ledgers)** ánh xạ với mọi yêu cầu tiên quyết rồi đánh dấu vào ô **Đồng bộ ban đầu**.</span><span class="sxs-lookup"><span data-stu-id="65d2a-179">From the list of maps, select the **Ledger (msdyn_ledgers)** map with all prerequisites and select the **Initial sync** check box.</span></span> 
7. <span data-ttu-id="65d2a-180">Trong trường **Đối tượng chính cho đồng bộ hóa ban đầu**, hãy chọn **ứng dụng Finance and Operations** rồi chọn **Chạy**.</span><span class="sxs-lookup"><span data-stu-id="65d2a-180">In the **Master for initial sync** field, select **Finance and Operations apps** and then select **Run**.</span></span>
 
 ![Đồng bộ hóa sơ đồ sổ cái](media/DW6.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]