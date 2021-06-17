---
title: Thiết lập và áp dụng dữ liệu cấu hình trong Common Data Service
description: Chủ đề này cung cấp thông tin về cách thiết lập và áp dụng dữ liệu cấu hình trong Project Operations.
author: sigitac
ms.date: 05/10/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2ea00df6112fb69b61f1889463424fdfee79aec9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001317"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a><span data-ttu-id="65bb3-103">Thiết lập và áp dụng dữ liệu cấu hình trong Common Data Service</span><span class="sxs-lookup"><span data-stu-id="65bb3-103">Set up and apply configuration data in the Common Data Service</span></span> 

<span data-ttu-id="65bb3-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_</span><span class="sxs-lookup"><span data-stu-id="65bb3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="65bb3-105">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="65bb3-105">Prerequisites</span></span>

<span data-ttu-id="65bb3-106">Trước khi bắt đầu đặt cấu hình dữ liệu trong Common Data Service (CDS), bạn phải đáp ứng được các điều kiện tiên quyết sau:</span><span class="sxs-lookup"><span data-stu-id="65bb3-106">Before you begin to configure data in the Common Data Service (CDS), the following prerequisites must be met:</span></span>

1.  <span data-ttu-id="65bb3-107">Cung phép cho môi trường CDS và môi trường Dynamics 365 Finance cho Project Operations.</span><span class="sxs-lookup"><span data-stu-id="65bb3-107">Provision a CDS environment and a Dynamics 365 Finance environment for Project Operations.</span></span>
2.  <span data-ttu-id="65bb3-108">Thông tin pháp nhân từ Dynamics 365 Finance được chia sẻ với môi trường CDS.</span><span class="sxs-lookup"><span data-stu-id="65bb3-108">Legal entity information from Dynamics 365 Finance is shared to the CDS environment.</span></span> <span data-ttu-id="65bb3-109">Điều này có nghĩa là thực thể **Công ty** trong CDS có các hồ sơ công ty sau:</span><span class="sxs-lookup"><span data-stu-id="65bb3-109">This means that the **Company** entity in CDS has the following company records:</span></span>
  - <span data-ttu-id="65bb3-110">THPM</span><span class="sxs-lookup"><span data-stu-id="65bb3-110">THPM</span></span>
  - <span data-ttu-id="65bb3-111">USPM</span><span class="sxs-lookup"><span data-stu-id="65bb3-111">USPM</span></span>
  - <span data-ttu-id="65bb3-112">GBPM</span><span class="sxs-lookup"><span data-stu-id="65bb3-112">GBPM</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="65bb3-113">Cài đặt dữ liệu cấu hình và thiết lập</span><span class="sxs-lookup"><span data-stu-id="65bb3-113">Install setup and configuration data</span></span>

1. <span data-ttu-id="65bb3-114">Tải xuống, bỏ chặn và giải nén [Gói dữ liệu cấu hình và thiết lập](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip).</span><span class="sxs-lookup"><span data-stu-id="65bb3-114">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip).</span></span>
2. <span data-ttu-id="65bb3-115">Chuyển đến thư mục đã giải nén rồi chạy tệp thực thi là *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="65bb3-115">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="65bb3-116">Trên trang 1 của Trình hướng dẫn di chuyển cấu hình (CMT) Common Data Service, hãy chọn **Nhập dữ liệu** và sau đó chọn **Tiếp tục**.</span><span class="sxs-lookup"><span data-stu-id="65bb3-116">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Di chuyển cấu hình](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="65bb3-118">Trên trang 2 của Trình hướng dẫn CMT, hãy chọn **Microsoft 365** làm **Loại triển khai**.</span><span class="sxs-lookup"><span data-stu-id="65bb3-118">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="65bb3-119">Chọn **Hiển thị danh sách tổ chức khả dụng** và hộp kiểm **Hiển thị nâng cao**.</span><span class="sxs-lookup"><span data-stu-id="65bb3-119">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="65bb3-120">Chọn khu vực của đối tượng thuê của bạn, nhập thông tin xác thực của bạn rồi chọn **Đăng nhập**.</span><span class="sxs-lookup"><span data-stu-id="65bb3-120">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Đăng nhập cấu hình](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="65bb3-122">Trên trang 3, từ danh sách tổ chức trên đối tượng thuê, hãy chọn tổ chức bạn muốn nhập dữ liệu demo vào rồi chọn **Đăng nhập**.</span><span class="sxs-lookup"><span data-stu-id="65bb3-122">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="65bb3-123">Trên trang 4, hãy chọn tệp zip là *SampleSetupAndConfigData* từ thư mục đã giải nén.</span><span class="sxs-lookup"><span data-stu-id="65bb3-123">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Chọn tệp zip](./media/3ZipFile.png)

![Chọn tệp](./media/4SelectAFile.png)

9. <span data-ttu-id="65bb3-126">Sau khi chọn tệp zip, hãy chọn **Nhập dữ liệu**.</span><span class="sxs-lookup"><span data-stu-id="65bb3-126">After the zip file is selected, select **Import Data**.</span></span>

![Nhập dữ liệu](./media/5ImportData.png)

10. <span data-ttu-id="65bb3-128">Quá trình nhập sẽ chạy trong khoảng hai mười phút tùy thuộc vào tốc độ mạng của bạn.</span><span class="sxs-lookup"><span data-stu-id="65bb3-128">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="65bb3-129">Sau khi hoàn tất quá trình nhập, hãy thoát khỏi Trình hướng dẫn CMT.</span><span class="sxs-lookup"><span data-stu-id="65bb3-129">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="65bb3-130">Kiểm tra tổ chức của bạn để tìm dữ liệu trong 26 thực thể sau:</span><span class="sxs-lookup"><span data-stu-id="65bb3-130">Check your organization for data in the following 26 entities:</span></span>

  - <span data-ttu-id="65bb3-131">Tiền tệ</span><span class="sxs-lookup"><span data-stu-id="65bb3-131">Currency</span></span>
  - <span data-ttu-id="65bb3-132">Biểu đồ tài khoản</span><span class="sxs-lookup"><span data-stu-id="65bb3-132">Chart of Accounts</span></span>
  - <span data-ttu-id="65bb3-133">Lịch tài khóa</span><span class="sxs-lookup"><span data-stu-id="65bb3-133">Fiscal Calendar</span></span>
  - <span data-ttu-id="65bb3-134">Các loại tỷ giá hối đoái</span><span class="sxs-lookup"><span data-stu-id="65bb3-134">Currency Exchange Rate Types</span></span>
  - <span data-ttu-id="65bb3-135">Ngày thanh toán</span><span class="sxs-lookup"><span data-stu-id="65bb3-135">Payment Day</span></span>
  - <span data-ttu-id="65bb3-136">Lịch trình thanh toán</span><span class="sxs-lookup"><span data-stu-id="65bb3-136">Payment Schedule</span></span>
  - <span data-ttu-id="65bb3-137">Điều khoản Thanh toán</span><span class="sxs-lookup"><span data-stu-id="65bb3-137">Payment Term</span></span>
  - <span data-ttu-id="65bb3-138">Đơn vị tổ chức</span><span class="sxs-lookup"><span data-stu-id="65bb3-138">Organizational Unit</span></span>
  - <span data-ttu-id="65bb3-139">Liên hệ</span><span class="sxs-lookup"><span data-stu-id="65bb3-139">Contact</span></span>
  - <span data-ttu-id="65bb3-140">Nhóm thuế</span><span class="sxs-lookup"><span data-stu-id="65bb3-140">Tax Group</span></span>
  - <span data-ttu-id="65bb3-141">Nhóm khách hàng</span><span class="sxs-lookup"><span data-stu-id="65bb3-141">Customer Group</span></span>
  - <span data-ttu-id="65bb3-142">Nhóm nhà cung cấp</span><span class="sxs-lookup"><span data-stu-id="65bb3-142">Vendor Group</span></span>
  - <span data-ttu-id="65bb3-143">Đơn vị</span><span class="sxs-lookup"><span data-stu-id="65bb3-143">Unit</span></span>
  - <span data-ttu-id="65bb3-144">Nhóm đơn vị đo</span><span class="sxs-lookup"><span data-stu-id="65bb3-144">Unit Group</span></span>
  - <span data-ttu-id="65bb3-145">Bảng giá</span><span class="sxs-lookup"><span data-stu-id="65bb3-145">Price List</span></span>
  - <span data-ttu-id="65bb3-146">Bảng giá Tham số Dự án</span><span class="sxs-lookup"><span data-stu-id="65bb3-146">Project Parameter Price List</span></span>
  - <span data-ttu-id="65bb3-147">Tuần suất hóa đơn</span><span class="sxs-lookup"><span data-stu-id="65bb3-147">Invoice Frequency</span></span>
  - <span data-ttu-id="65bb3-148">Thể loại Nguồn lực có thể đăng ký trước</span><span class="sxs-lookup"><span data-stu-id="65bb3-148">Bookable Resource Category</span></span>
  - <span data-ttu-id="65bb3-149">Thể loại giao dịch</span><span class="sxs-lookup"><span data-stu-id="65bb3-149">Transaction Category</span></span>
  - <span data-ttu-id="65bb3-150">Thể loại Chi phí</span><span class="sxs-lookup"><span data-stu-id="65bb3-150">Expense Category</span></span>
  - <span data-ttu-id="65bb3-151">Giá Vai trò</span><span class="sxs-lookup"><span data-stu-id="65bb3-151">Role Price</span></span>
  - <span data-ttu-id="65bb3-152">Giá cả Thể loại Giao dịch</span><span class="sxs-lookup"><span data-stu-id="65bb3-152">Transaction Category Price</span></span>
  - <span data-ttu-id="65bb3-153">Đặc tính</span><span class="sxs-lookup"><span data-stu-id="65bb3-153">Characteristic</span></span>
  - <span data-ttu-id="65bb3-154">Nguồn lực có thể đăng ký</span><span class="sxs-lookup"><span data-stu-id="65bb3-154">Bookable Resource</span></span>
  - <span data-ttu-id="65bb3-155">LK thể loại nguồn lực có thể đăng ký trước</span><span class="sxs-lookup"><span data-stu-id="65bb3-155">Bookable resource category Assn</span></span>
  - <span data-ttu-id="65bb3-156">Đặc tính Nguồn lực có thể đăng ký trước</span><span class="sxs-lookup"><span data-stu-id="65bb3-156">Bookable Resource Characteristic</span></span>

![Hoàn thành quá trình nhập](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="65bb3-158">Cập nhật cấu hình Project Operations</span><span class="sxs-lookup"><span data-stu-id="65bb3-158">Update Project Operations configurations</span></span>

1. <span data-ttu-id="65bb3-159">Điều hướng tới môi trường CE.</span><span class="sxs-lookup"><span data-stu-id="65bb3-159">Navigate to the CE environment.</span></span> <span data-ttu-id="65bb3-160">Bạn có thể tìm môi trường này bằng cách mở [Trung tâm quản trị Power Platform](https://admin.powerplatform.microsoft.com/environments), chọn môi trường, sau đó chọn **Mở môi trường**.</span><span class="sxs-lookup"><span data-stu-id="65bb3-160">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Mở môi trường](./media/7OpenEnvironment.png)

2. <span data-ttu-id="65bb3-162">Chuyển đến **Dự án** > **Nguồn lực** rồi chọn **Mới** để tạo nguồn lực có thể đăng ký trước cho người dùng của bạn.</span><span class="sxs-lookup"><span data-stu-id="65bb3-162">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Nguồn lực có thể đăng ký trước](./media/8BookableResources.png)

3. <span data-ttu-id="65bb3-164">Trên tab **Tổng quát**, hãy chọn người dùng là quản trị viên của bạn.</span><span class="sxs-lookup"><span data-stu-id="65bb3-164">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="65bb3-165">Xác minh rằng múi giờ khớp với múi giờ bạn đang ở.</span><span class="sxs-lookup"><span data-stu-id="65bb3-165">Verify that the time zone matches the one you are in.</span></span> 

![Nguồn lực mới có thể đăng ký trước](./media/9NewBookableResource.png)

4. <span data-ttu-id="65bb3-167">Trên tab **Lên lịch**, trong trường **Công ty**, hãy chọn công ty **USPM** rồi chọn **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="65bb3-167">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Tab Lên lịch](./media/10SchedulingTab.png)

5. <span data-ttu-id="65bb3-169">Chọn tab **Giờ làm việc**.</span><span class="sxs-lookup"><span data-stu-id="65bb3-169">Select the **Work hours** tab.</span></span>  

![Giờ Làm việc](./media/11WorkHours.png)

6. <span data-ttu-id="65bb3-171">Nhấp đúp chuột vào bất kỳ giá trị nào trong lịch và chọn **Chỉnh sửa** > **Tất cả các sự kiện trong chuỗi**.</span><span class="sxs-lookup"><span data-stu-id="65bb3-171">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Lịch làm việc](./media/12WorkCalendar.png)

7. <span data-ttu-id="65bb3-173">Thay đổi giờ làm việc thành một ngày làm việc tám (8) giờ, đánh dấu các ngày cuối tuần là ngày không làm việc và đảm bảo múi giờ khớp với múi giờ của bạn.</span><span class="sxs-lookup"><span data-stu-id="65bb3-173">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="65bb3-174">Chọn **Lưu và đóng**.</span><span class="sxs-lookup"><span data-stu-id="65bb3-174">Select **Save and close**.</span></span>

![Cập nhật lịch](./media/13UpdateCalendar.png)

9. <span data-ttu-id="65bb3-176">Chuyển đến **Thiết đặt** > **Các mẫu lịch** và chọn **Mới**.</span><span class="sxs-lookup"><span data-stu-id="65bb3-176">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Mẫu lịch](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="65bb3-178">Nhập tên, chọn nguồn lực mẫu bạn đã tạo, sau đó chọn **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="65bb3-178">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Lưu mẫu lịch](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="65bb3-180">Chuyển đến **Tham số** và nhấp đúp vào bản ghi.</span><span class="sxs-lookup"><span data-stu-id="65bb3-180">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Tham số Dự án](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="65bb3-182">Cập nhật các trường sau:</span><span class="sxs-lookup"><span data-stu-id="65bb3-182">Update the following fields:</span></span>

 - <span data-ttu-id="65bb3-183">**Công ty mặc định**: USPM</span><span class="sxs-lookup"><span data-stu-id="65bb3-183">**Default company**: USPM</span></span>
 - <span data-ttu-id="65bb3-184">**Đơn vị tổ chức mặc định**: Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="65bb3-184">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="65bb3-185">**Tần suất hóa đơn** : Ngày thứ bảy và ngày cuối cùng</span><span class="sxs-lookup"><span data-stu-id="65bb3-185">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="65bb3-186">**Mẫu giờ làm việc** : Thay đổi mẫu bạn đã tạo.</span><span class="sxs-lookup"><span data-stu-id="65bb3-186">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="65bb3-187">Chọn **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="65bb3-187">Select **Save**.</span></span> 

![Đã cập nhật tham số dự án](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
