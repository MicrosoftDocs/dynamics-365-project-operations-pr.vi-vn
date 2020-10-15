---
title: Áp dụng dữ liệu cấu hình và thiết lập demo
description: Chủ đề này cung cấp thông tin về cách áp dụng dữ liệu cấu hình và thiết lập demo cho Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 42e02f393e89d20b2a462645f519a3792bee8f2f
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949137"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="4ab89-103">Áp dụng dữ liệu cấu hình và thiết lập demo để triển khai Project Operations Lite – từ thỏa thuận đến lập hóa đơn ước giá</span><span class="sxs-lookup"><span data-stu-id="4ab89-103">Apply demo setup and configuration data for Project Operations lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="4ab89-104">_\*\*Triển khai Lite – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="4ab89-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

1. <span data-ttu-id="4ab89-105">Tải [Gói dữ liệu chính](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip) xuống.</span><span class="sxs-lookup"><span data-stu-id="4ab89-105">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="4ab89-106">Chuyển đến thư mục *ProjOpsDemoDataSetupAndMaster - Integrated CMT* rồi chạy tệp thực thi là *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="4ab89-106">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="4ab89-107">Trên trang 1 của Trình hướng dẫn di chuyển cấu hình (CMT) Common Data Service, hãy chọn **Nhập dữ liệu** và sau đó chọn **Tiếp tục**.</span><span class="sxs-lookup"><span data-stu-id="4ab89-107">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Di chuyển cấu hình](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="4ab89-109">Trên Trang 2 của Trình hướng dẫn CMT, hãy chọn **Office 365** làm **Loại triển khai**.</span><span class="sxs-lookup"><span data-stu-id="4ab89-109">On Page 2 of the CMT Wizard, select **Office 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="4ab89-110">Chọn **Hiển thị danh sách tổ chức khả dụng** và hộp kiểm **Hiển thị nâng cao**.</span><span class="sxs-lookup"><span data-stu-id="4ab89-110">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="4ab89-111">Chọn khu vực của đối tượng thuê của bạn, nhập thông tin xác thực của bạn, sau đó chọn **Đăng nhập**.</span><span class="sxs-lookup"><span data-stu-id="4ab89-111">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![Đăng nhập cấu hình](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="4ab89-113">Trên trang 3, từ danh sách Tổ chức trên Đối tượng thuê, hãy chọn tổ chức bạn muốn nhập dữ liệu demo vào rồi chọn **Đăng nhập**.</span><span class="sxs-lookup"><span data-stu-id="4ab89-113">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="4ab89-114">Trên trang 4, hãy chọn tệp zip là *MasterAndSetupData* từ thư mục đã giải nén là *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span><span class="sxs-lookup"><span data-stu-id="4ab89-114">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![Tệp Zip](./media/3ZipFile.png)

![Chọn tệp](./media/4SelectAFile.png)

9. <span data-ttu-id="4ab89-117">Sau khi chọn tệp zip, hãy chọn **Nhập dữ liệu**.</span><span class="sxs-lookup"><span data-stu-id="4ab89-117">After the zip file is selected, select **Import Data**.</span></span>

![Nhập dữ liệu](./media/5ImportData.png)

10. <span data-ttu-id="4ab89-119">Quá trình nhập sẽ chạy trong khoảng hai mười phút tùy thuộc vào tốc độ mạng của bạn.</span><span class="sxs-lookup"><span data-stu-id="4ab89-119">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="4ab89-120">Sau khi hoàn tất, hãy thoát khỏi CMT Wizard.</span><span class="sxs-lookup"><span data-stu-id="4ab89-120">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="4ab89-121">Kiểm tra tổ chức của bạn để tìm dữ liệu trong 20 thực thể sau:</span><span class="sxs-lookup"><span data-stu-id="4ab89-121">Check your organization for data in the following 20 entities:</span></span>

- <span data-ttu-id="4ab89-122">Tiền tệ</span><span class="sxs-lookup"><span data-stu-id="4ab89-122">Currency</span></span>
- <span data-ttu-id="4ab89-123">Đơn vị tổ chức</span><span class="sxs-lookup"><span data-stu-id="4ab89-123">Organizational Unit</span></span>
- <span data-ttu-id="4ab89-124">Liên hệ</span><span class="sxs-lookup"><span data-stu-id="4ab89-124">Contact</span></span>
- <span data-ttu-id="4ab89-125">Nhóm thuế</span><span class="sxs-lookup"><span data-stu-id="4ab89-125">Tax Group</span></span>
- <span data-ttu-id="4ab89-126">Nhóm khách hàng</span><span class="sxs-lookup"><span data-stu-id="4ab89-126">Customer Group</span></span>
- <span data-ttu-id="4ab89-127">Đơn vị</span><span class="sxs-lookup"><span data-stu-id="4ab89-127">Unit</span></span>
- <span data-ttu-id="4ab89-128">Nhóm đơn vị</span><span class="sxs-lookup"><span data-stu-id="4ab89-128">Unit Group</span></span>
- <span data-ttu-id="4ab89-129">Bảng giá</span><span class="sxs-lookup"><span data-stu-id="4ab89-129">Price List</span></span>
- <span data-ttu-id="4ab89-130">Bảng giá Tham số Dự án</span><span class="sxs-lookup"><span data-stu-id="4ab89-130">Project Parameter Price List</span></span>
- <span data-ttu-id="4ab89-131">Tuần suất hóa đơn</span><span class="sxs-lookup"><span data-stu-id="4ab89-131">Invoice Frequency</span></span>
- <span data-ttu-id="4ab89-132">Chi tiết Tuần suất Hóa đơn</span><span class="sxs-lookup"><span data-stu-id="4ab89-132">Invoice Frequency Detail</span></span>
- <span data-ttu-id="4ab89-133">Thể loại Nguồn lực có thể đăng ký trước</span><span class="sxs-lookup"><span data-stu-id="4ab89-133">Bookable Resource Category</span></span>
- <span data-ttu-id="4ab89-134">Thể loại giao dịch</span><span class="sxs-lookup"><span data-stu-id="4ab89-134">Transaction Category</span></span>
- <span data-ttu-id="4ab89-135">Thể loại Chi phí</span><span class="sxs-lookup"><span data-stu-id="4ab89-135">Expense Category</span></span>
- <span data-ttu-id="4ab89-136">Giá Vai trò</span><span class="sxs-lookup"><span data-stu-id="4ab89-136">Role Price</span></span>
- <span data-ttu-id="4ab89-137">Giá cả Thể loại Giao dịch</span><span class="sxs-lookup"><span data-stu-id="4ab89-137">Transaction Category Price</span></span>
- <span data-ttu-id="4ab89-138">Đặc tính</span><span class="sxs-lookup"><span data-stu-id="4ab89-138">Characteristic</span></span>
- <span data-ttu-id="4ab89-139">Nguồn lực có thể đăng ký</span><span class="sxs-lookup"><span data-stu-id="4ab89-139">Bookable Resource</span></span>
- <span data-ttu-id="4ab89-140">LK thể loại nguồn lực có thể đăng ký trước</span><span class="sxs-lookup"><span data-stu-id="4ab89-140">Bookable resource category Assn</span></span>
- <span data-ttu-id="4ab89-141">Đặc tính Nguồn lực có thể đăng ký trước</span><span class="sxs-lookup"><span data-stu-id="4ab89-141">Bookable Resource Characteristic</span></span>

![Hoàn thành quá trình nhập](./media/6CompleteImport.png)
