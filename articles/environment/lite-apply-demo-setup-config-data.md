---
title: Áp dụng dữ liệu cấu hình và thiết lập bản demo – bản đơn giản
description: Chủ đề này cung cấp thông tin về cách áp dụng dữ liệu cấu hình và thiết lập demo cho Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 421c9d28088c92617687641d93b3ad5d6bfea73c
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642119"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a><span data-ttu-id="eb6b0-103">Áp dụng dữ liệu cấu hình và thiết lập bản demo cho Project Operations – bản đơn giản</span><span class="sxs-lookup"><span data-stu-id="eb6b0-103">Apply demo setup and configuration data for Project Operations - lite</span></span> 

<span data-ttu-id="eb6b0-104">_\*\*Triển khai Lite – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="eb6b0-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="eb6b0-105">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="eb6b0-105">Prerequisites</span></span>

<span data-ttu-id="eb6b0-106">Trước khi bắt đầu cấu hình, bạn phải cung cấp môi trường Common Data Service (CDS) cho Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="eb6b0-106">Before you begin the configuration, you must have a Common Data Service (CDS) environment provisioned for Dynamics 365 Project Operations.</span></span>


## <a name="instructions"></a><span data-ttu-id="eb6b0-107">Hướng dẫn</span><span class="sxs-lookup"><span data-stu-id="eb6b0-107">Instructions</span></span>

1. <span data-ttu-id="eb6b0-108">Tải [Gói dữ liệu chính](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip) xuống.</span><span class="sxs-lookup"><span data-stu-id="eb6b0-108">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="eb6b0-109">Chuyển đến thư mục *ProjOpsDemoDataSetupAndMaster - Integrated CMT* rồi chạy tệp thực thi là *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="eb6b0-109">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="eb6b0-110">Trên trang 1 của Trình hướng dẫn di chuyển cấu hình (CMT) Common Data Service, hãy chọn **Nhập dữ liệu** và sau đó chọn **Tiếp tục**.</span><span class="sxs-lookup"><span data-stu-id="eb6b0-110">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Di chuyển cấu hình](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="eb6b0-112">Trên trang 2 của Trình hướng dẫn CMT, hãy chọn **Microsoft 365** làm **Loại triển khai**.</span><span class="sxs-lookup"><span data-stu-id="eb6b0-112">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="eb6b0-113">Chọn **Hiển thị danh sách tổ chức khả dụng** và hộp kiểm **Hiển thị nâng cao**.</span><span class="sxs-lookup"><span data-stu-id="eb6b0-113">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="eb6b0-114">Chọn khu vực của đối tượng thuê của bạn, nhập thông tin xác thực của bạn, sau đó chọn **Đăng nhập**.</span><span class="sxs-lookup"><span data-stu-id="eb6b0-114">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![Đăng nhập cấu hình](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="eb6b0-116">Trên trang 3, từ danh sách Tổ chức trên Đối tượng thuê, hãy chọn tổ chức bạn muốn nhập dữ liệu demo vào rồi chọn **Đăng nhập**.</span><span class="sxs-lookup"><span data-stu-id="eb6b0-116">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="eb6b0-117">Trên trang 4, hãy chọn tệp zip là *MasterAndSetupData* từ thư mục đã giải nén là *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span><span class="sxs-lookup"><span data-stu-id="eb6b0-117">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![Tệp Zip](./media/3ZipFile.png)

![Chọn tệp](./media/4SelectAFile.png)

9. <span data-ttu-id="eb6b0-120">Sau khi chọn tệp zip, hãy chọn **Nhập dữ liệu**.</span><span class="sxs-lookup"><span data-stu-id="eb6b0-120">After the zip file is selected, select **Import Data**.</span></span>

![Nhập dữ liệu](./media/5ImportData.png)

10. <span data-ttu-id="eb6b0-122">Quá trình nhập sẽ chạy trong khoảng hai mười phút tùy thuộc vào tốc độ mạng của bạn.</span><span class="sxs-lookup"><span data-stu-id="eb6b0-122">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="eb6b0-123">Sau khi hoàn tất, hãy thoát khỏi CMT Wizard.</span><span class="sxs-lookup"><span data-stu-id="eb6b0-123">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="eb6b0-124">Kiểm tra tổ chức của bạn để tìm dữ liệu trong 20 thực thể sau:</span><span class="sxs-lookup"><span data-stu-id="eb6b0-124">Check your organization for data in the following 20 entities:</span></span>

-   <span data-ttu-id="eb6b0-125">Tiền tệ</span><span class="sxs-lookup"><span data-stu-id="eb6b0-125">Currency</span></span>
-   <span data-ttu-id="eb6b0-126">T.khoản</span><span class="sxs-lookup"><span data-stu-id="eb6b0-126">Account</span></span>
-   <span data-ttu-id="eb6b0-127">Đơn vị tổ chức</span><span class="sxs-lookup"><span data-stu-id="eb6b0-127">Organizational Unit</span></span>
-   <span data-ttu-id="eb6b0-128">Liên hệ</span><span class="sxs-lookup"><span data-stu-id="eb6b0-128">Contact</span></span>
-   <span data-ttu-id="eb6b0-129">Nhóm thuế</span><span class="sxs-lookup"><span data-stu-id="eb6b0-129">Tax Group</span></span>
-   <span data-ttu-id="eb6b0-130">Nhóm khách hàng</span><span class="sxs-lookup"><span data-stu-id="eb6b0-130">Customer Group</span></span>
-   <span data-ttu-id="eb6b0-131">Đơn vị</span><span class="sxs-lookup"><span data-stu-id="eb6b0-131">Unit</span></span>
-   <span data-ttu-id="eb6b0-132">Nhóm đơn vị</span><span class="sxs-lookup"><span data-stu-id="eb6b0-132">Unit Group</span></span>
-   <span data-ttu-id="eb6b0-133">Bảng giá</span><span class="sxs-lookup"><span data-stu-id="eb6b0-133">Price List</span></span>
-   <span data-ttu-id="eb6b0-134">Bảng giá Tham số Dự án</span><span class="sxs-lookup"><span data-stu-id="eb6b0-134">Project Parameter Price List</span></span> 
-   <span data-ttu-id="eb6b0-135">Tuần suất hóa đơn</span><span class="sxs-lookup"><span data-stu-id="eb6b0-135">Invoice Frequency</span></span>
-   <span data-ttu-id="eb6b0-136">Thể loại Nguồn lực có thể đăng ký trước</span><span class="sxs-lookup"><span data-stu-id="eb6b0-136">Bookable Resource Category</span></span>
-   <span data-ttu-id="eb6b0-137">Thể loại giao dịch</span><span class="sxs-lookup"><span data-stu-id="eb6b0-137">Transaction Category</span></span>
-   <span data-ttu-id="eb6b0-138">Thể loại Chi phí</span><span class="sxs-lookup"><span data-stu-id="eb6b0-138">Expense Category</span></span>
-   <span data-ttu-id="eb6b0-139">Giá Vai trò</span><span class="sxs-lookup"><span data-stu-id="eb6b0-139">Role Price</span></span>
-   <span data-ttu-id="eb6b0-140">Giá cả Thể loại Giao dịch</span><span class="sxs-lookup"><span data-stu-id="eb6b0-140">Transaction Category Price</span></span>
-   <span data-ttu-id="eb6b0-141">Đặc tính</span><span class="sxs-lookup"><span data-stu-id="eb6b0-141">Characteristic</span></span>
-   <span data-ttu-id="eb6b0-142">Nguồn lực có thể đăng ký</span><span class="sxs-lookup"><span data-stu-id="eb6b0-142">Bookable Resource</span></span>
-   <span data-ttu-id="eb6b0-143">LK thể loại nguồn lực có thể đăng ký trước</span><span class="sxs-lookup"><span data-stu-id="eb6b0-143">Bookable resource category Assn</span></span>
-   <span data-ttu-id="eb6b0-144">Đặc tính Nguồn lực có thể đăng ký trước</span><span class="sxs-lookup"><span data-stu-id="eb6b0-144">Bookable Resource Characteristic</span></span>

![Hoàn thành quá trình nhập](./media/6CompleteImport.png)
