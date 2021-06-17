---
title: Áp dụng dữ liệu cấu hình và thiết lập bản demo – bản đơn giản
description: Chủ đề này cung cấp thông tin về cách áp dụng dữ liệu cấu hình và thiết lập demo cho Project Operations.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7729b4a9ef5f498b78af298f7233d7dd45434bb3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997177"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a><span data-ttu-id="f8678-103">Áp dụng dữ liệu cấu hình và thiết lập bản demo cho Project Operations – bản đơn giản</span><span class="sxs-lookup"><span data-stu-id="f8678-103">Apply demo setup and configuration data for Project Operations - lite</span></span> 

<span data-ttu-id="f8678-104">_\*\*Triển khai Lite – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="f8678-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="f8678-105">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="f8678-105">Prerequisites</span></span>

<span data-ttu-id="f8678-106">Trước khi bắt đầu cấu hình, bạn phải cung cấp môi trường Common Data Service (CDS) cho Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="f8678-106">Before you begin the configuration, you must have a Common Data Service (CDS) environment provisioned for Dynamics 365 Project Operations.</span></span>


## <a name="instructions"></a><span data-ttu-id="f8678-107">Hướng dẫn</span><span class="sxs-lookup"><span data-stu-id="f8678-107">Instructions</span></span>

1. <span data-ttu-id="f8678-108">Tải [Gói dữ liệu chính](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip) xuống.</span><span class="sxs-lookup"><span data-stu-id="f8678-108">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip).</span></span> 
2. <span data-ttu-id="f8678-109">Điều hướng đến thư mục *ProjOpsSampleSetupData - CE only CMT* và chạy tệp thực thi *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="f8678-109">Navigate to the folder *ProjOpsSampleSetupData - CE only CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="f8678-110">Trên trang 1 của Trình hướng dẫn di chuyển cấu hình (CMT) Common Data Service, hãy chọn **Nhập dữ liệu** và sau đó chọn **Tiếp tục**.</span><span class="sxs-lookup"><span data-stu-id="f8678-110">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

    ![Di chuyển cấu hình](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="f8678-112">Trên trang 2 của Trình hướng dẫn CMT, hãy chọn **Microsoft 365** làm **Loại triển khai**.</span><span class="sxs-lookup"><span data-stu-id="f8678-112">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="f8678-113">Chọn **Hiển thị danh sách tổ chức khả dụng** và hộp kiểm **Hiển thị nâng cao**.</span><span class="sxs-lookup"><span data-stu-id="f8678-113">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="f8678-114">Chọn khu vực của đối tượng thuê của bạn, nhập thông tin xác thực của bạn, sau đó chọn **Đăng nhập**.</span><span class="sxs-lookup"><span data-stu-id="f8678-114">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

   ![Đăng nhập cấu hình](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="f8678-116">Trên trang 3, từ danh sách Tổ chức trên Đối tượng thuê, hãy chọn tổ chức bạn muốn nhập dữ liệu demo vào rồi chọn **Đăng nhập**.</span><span class="sxs-lookup"><span data-stu-id="f8678-116">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="f8678-117">Trên trang 4, hãy chọn tệp zip *SampleSetupAndConfigData* ở thư mục được giải nén *ProjOpsSampleSetupData - CE only CMT*.</span><span class="sxs-lookup"><span data-stu-id="f8678-117">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder, *ProjOpsSampleSetupData - CE only CMT*.</span></span>

   ![Tệp Zip](./media/3ZipFile.png)

   ![Chọn một tệp](./media/4SelectAFile.png)

9. <span data-ttu-id="f8678-120">Sau khi chọn tệp zip, hãy chọn **Nhập dữ liệu**.</span><span class="sxs-lookup"><span data-stu-id="f8678-120">After the zip file is selected, select **Import Data**.</span></span>

   ![Nhập dữ liệu](./media/5ImportData.png)

10. <span data-ttu-id="f8678-122">Quá trình nhập sẽ chạy trong khoảng hai mười phút tùy thuộc vào tốc độ mạng của bạn.</span><span class="sxs-lookup"><span data-stu-id="f8678-122">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="f8678-123">Sau khi hoàn tất, hãy thoát khỏi CMT Wizard.</span><span class="sxs-lookup"><span data-stu-id="f8678-123">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="f8678-124">Kiểm tra tổ chức của bạn để tìm dữ liệu trong 18 thực thể sau:</span><span class="sxs-lookup"><span data-stu-id="f8678-124">Check your organization for data in the following 18 entities:</span></span>

    -   <span data-ttu-id="f8678-125">Tiền tệ</span><span class="sxs-lookup"><span data-stu-id="f8678-125">Currency</span></span>
    -   <span data-ttu-id="f8678-126">Tài khoản</span><span class="sxs-lookup"><span data-stu-id="f8678-126">Account</span></span>
    -   <span data-ttu-id="f8678-127">Đơn vị tổ chức</span><span class="sxs-lookup"><span data-stu-id="f8678-127">Organizational Unit</span></span>
    -   <span data-ttu-id="f8678-128">Liên hệ</span><span class="sxs-lookup"><span data-stu-id="f8678-128">Contact</span></span>
    -   <span data-ttu-id="f8678-129">Đơn vị</span><span class="sxs-lookup"><span data-stu-id="f8678-129">Unit</span></span>
    -   <span data-ttu-id="f8678-130">Nhóm đơn vị</span><span class="sxs-lookup"><span data-stu-id="f8678-130">Unit Group</span></span>
    -   <span data-ttu-id="f8678-131">Bảng giá</span><span class="sxs-lookup"><span data-stu-id="f8678-131">Price List</span></span>
    -   <span data-ttu-id="f8678-132">Bảng giá Tham số Dự án</span><span class="sxs-lookup"><span data-stu-id="f8678-132">Project Parameter Price List</span></span> 
    -   <span data-ttu-id="f8678-133">Tuần suất hóa đơn</span><span class="sxs-lookup"><span data-stu-id="f8678-133">Invoice Frequency</span></span>
    -   <span data-ttu-id="f8678-134">Thể loại Nguồn lực có thể đăng ký trước</span><span class="sxs-lookup"><span data-stu-id="f8678-134">Bookable Resource Category</span></span>
    -   <span data-ttu-id="f8678-135">Thể loại giao dịch</span><span class="sxs-lookup"><span data-stu-id="f8678-135">Transaction Category</span></span>
    -   <span data-ttu-id="f8678-136">Thể loại Chi phí</span><span class="sxs-lookup"><span data-stu-id="f8678-136">Expense Category</span></span>
    -   <span data-ttu-id="f8678-137">Giá Vai trò</span><span class="sxs-lookup"><span data-stu-id="f8678-137">Role Price</span></span>
    -   <span data-ttu-id="f8678-138">Giá cả Thể loại Giao dịch</span><span class="sxs-lookup"><span data-stu-id="f8678-138">Transaction Category Price</span></span>
    -   <span data-ttu-id="f8678-139">Đặc tính</span><span class="sxs-lookup"><span data-stu-id="f8678-139">Characteristic</span></span>
    -   <span data-ttu-id="f8678-140">Nguồn lực có thể đăng ký</span><span class="sxs-lookup"><span data-stu-id="f8678-140">Bookable Resource</span></span>
    -   <span data-ttu-id="f8678-141">LK thể loại nguồn lực có thể đăng ký trước</span><span class="sxs-lookup"><span data-stu-id="f8678-141">Bookable resource category Assn</span></span>
    -   <span data-ttu-id="f8678-142">Đặc tính Nguồn lực có thể đăng ký trước</span><span class="sxs-lookup"><span data-stu-id="f8678-142">Bookable Resource Characteristic</span></span>

    ![Hoàn thành quá trình nhập](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
