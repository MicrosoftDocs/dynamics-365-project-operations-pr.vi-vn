---
title: Áp dụng dữ liệu minh họa cho môi trường Finance được lưu trữ trên đám mây
description: Chủ đề này sẽ giải thích cách áp dụng dữ liệu demo từ Project Operations cho môi trường Dynamics 365 Finance được lưu trữ trên đám mây.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a7cdbd2847ce45972aadd0d1a2d4f26270727ad9
ms.sourcegitcommit: d33ef0ae39f90fe3b0f6b4524f483e8052057361
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 11/03/2020
ms.locfileid: "4365264"
---
# <a name="apply-demo-data-to-a-finance-cloud-hosted-environment"></a><span data-ttu-id="b2ddc-103">Áp dụng dữ liệu minh họa cho môi trường Finance được lưu trữ trên đám mây</span><span class="sxs-lookup"><span data-stu-id="b2ddc-103">Apply demo data to a Finance Cloud-hosted environment</span></span>

<span data-ttu-id="b2ddc-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_</span><span class="sxs-lookup"><span data-stu-id="b2ddc-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b2ddc-105">Chủ đề này chỉ có thể áp dụng cho Microsoft Dynamics 365 Finance phiên bản 10.0.13 và chỉ có thể được thực hiện trên môi trường được lưu trữ trên đám mây.</span><span class="sxs-lookup"><span data-stu-id="b2ddc-105">This topic is only applicable only Microsoft Dynamics 365 Finance version 10.0.13 and can be performed only on a Cloud-hosted environment.</span></span> <span data-ttu-id="b2ddc-106">Hoàn thành các bước trong chủ đề này **TRƯỚC** khi bạn áp dụng các bản cập nhật chất lượng cho môi trường.</span><span class="sxs-lookup"><span data-stu-id="b2ddc-106">Complete the steps in this topic **BEFORE** you apply quality updates to the environment.</span></span>

1. <span data-ttu-id="b2ddc-107">Trong dự án LCS của bạn, hãy mở trang **Chi tiết môi trường**.</span><span class="sxs-lookup"><span data-stu-id="b2ddc-107">In your LCS project, open the **Environment details** page.</span></span> <span data-ttu-id="b2ddc-108">Lưu ý rằng trang này bao gồm các chi tiết cần thiết để kết nối với môi trường bằng cách sử dụng Giao thức Máy tính Từ xa (RDP).</span><span class="sxs-lookup"><span data-stu-id="b2ddc-108">Notice that it includes the details needed to connect to the environment by using Remote Desktop Protocol (RDP).</span></span>

![Chi tiết môi trường](./media/1EnvironmentDetails.png)

<span data-ttu-id="b2ddc-110">Bộ thông tin xác thực được đánh dấu đầu tiên là thông tin xác thực tài khoản cục bộ và chứa siêu liên kết đến kết nối máy tính từ xa.</span><span class="sxs-lookup"><span data-stu-id="b2ddc-110">The first set of highlighted credentials are the local account credentials and contain a hyperlink to the remote desktop connection.</span></span> <span data-ttu-id="b2ddc-111">Thông tin xác thực bao gồm tên người dùng và mật khẩu quản trị môi trường.</span><span class="sxs-lookup"><span data-stu-id="b2ddc-111">The credentials include the environment admin username and password.</span></span> <span data-ttu-id="b2ddc-112">Bộ thông tin xác thực thứ hai được sử dụng để đăng nhập vào SQL Server trong môi trường này.</span><span class="sxs-lookup"><span data-stu-id="b2ddc-112">The second set of credentials are used to log in to SQL Server in this environment.</span></span>

2. <span data-ttu-id="b2ddc-113">Kết nối với môi trường bằng siêu liên kết trong **Tài khoản cục bộ** và sử dụng **Thông tin xác thực tài khoản cục bộ** để xác thực.</span><span class="sxs-lookup"><span data-stu-id="b2ddc-113">Remote to the environment by the hyperlink in **Local Accounts**, and use the **Local Account credentials** to authenticate.</span></span>
3. <span data-ttu-id="b2ddc-114">Chuyển đến **Dịch vụ thông tin Internet** > **Bộ ứng dụng** > **AOSService** và ngừng dịch vụ.</span><span class="sxs-lookup"><span data-stu-id="b2ddc-114">Go to **Internet Information Services** > **Application Pools** > **AOSService** and stop the service.</span></span> <span data-ttu-id="b2ddc-115">Bạn hiện đang ngừng dịch vụ để có thể tiếp tục thay thế cơ sở dữ liệu SQL.</span><span class="sxs-lookup"><span data-stu-id="b2ddc-115">You are stopping the service at this point so that you can continue to replace the SQL database.</span></span>

![Ngừng AOS](./media/2StopAOS.png)

4. <span data-ttu-id="b2ddc-117">Chuyển đến **Dịch vụ** và ngừng hai mục sau:</span><span class="sxs-lookup"><span data-stu-id="b2ddc-117">Go to **Services** and stop the following two items:</span></span>

- <span data-ttu-id="b2ddc-118">Microsoft Dynamics 365 Unified Operations: Dịch vụ quản lý lô</span><span class="sxs-lookup"><span data-stu-id="b2ddc-118">Microsoft Dynamics 365 Unified Operations: Batch Management Service</span></span>
- <span data-ttu-id="b2ddc-119">Microsoft Dynamics 365 Unified Operations: Khung xuất nhập dữ liệu</span><span class="sxs-lookup"><span data-stu-id="b2ddc-119">Microsoft Dynamics 365 Unified Operations: Data Import Export Framework</span></span>

![Ngừng dịch vụ](./media/3StopServices.png)

5. <span data-ttu-id="b2ddc-121">Mở Microsoft SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="b2ddc-121">Open Microsoft SQL Server Management Studio.</span></span> <span data-ttu-id="b2ddc-122">Đăng nhập bằng thông tin xác thực SQL server và sử dụng mật khẩu và người dùng axdbadmin từ trang **Chi tiết môi trường** LCS.</span><span class="sxs-lookup"><span data-stu-id="b2ddc-122">Log in with SQL server credentials and use the axdbadmin user and password from the LCS **Environments details** page.</span></span>

![SQL Server Management Studio](./media/4SSMS.png)

6. <span data-ttu-id="b2ddc-124">Trong Trình khám phá đối tượng, **Cơ sở dữ liệu** và xác định vị trí **AXDB**.</span><span class="sxs-lookup"><span data-stu-id="b2ddc-124">In Object Explorer, **Databases** and locate **AXDB**.</span></span> <span data-ttu-id="b2ddc-125">Bạn sẽ thay thế cơ sở dữ liệu bằng một cơ sở dữ liệu mới nằm trong [Trung tâm tải xuống](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span><span class="sxs-lookup"><span data-stu-id="b2ddc-125">You will replace database with a new database that is located in the [Download Center](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span></span> 
7. <span data-ttu-id="b2ddc-126">Sao chép tệp zip vào máy ảo mà bạn được điều khiển từ xa rồi giải nén nội dung tệp zip.</span><span class="sxs-lookup"><span data-stu-id="b2ddc-126">Copy the zip file to the VM you are remoted into and extract zip contents.</span></span>
8. <span data-ttu-id="b2ddc-127">Trong SQL Server Management Studio, hãy nhấp chuột phải vào **AxDB** rồi chọn **Nhiệm vụ** > **Khôi phục** > **Cơ sở dữ liệu**.</span><span class="sxs-lookup"><span data-stu-id="b2ddc-127">In SQL Server Management Studio, right-click **AxDB**, and then select **Tasks** > **Restore** > **Database**.</span></span>

![Khôi phục cơ sở dữ liệu](./media/5RestoreDatabase.png)

9. <span data-ttu-id="b2ddc-129">Chọn **Thiết bị nguồn** và điều hướng đến tệp được giải nén từ tệp zip bạn đã sao chép.</span><span class="sxs-lookup"><span data-stu-id="b2ddc-129">Select **Source Device** and navigate to the file extracted from zip you copied.</span></span>

![Thiết bị nguồn](./media/6SourceDevice.png)

10. <span data-ttu-id="b2ddc-131">Chọn **Tùy chọn** rồi chọn **Ghi đè cơ sở dữ liệu hiện có** và **Đóng các kết nối hiện có đến cơ sở dữ liệu đích**.</span><span class="sxs-lookup"><span data-stu-id="b2ddc-131">Select **Options**, and then select **Overwrite the existing database** and **Close existing connections to destination database**.</span></span> 
11. <span data-ttu-id="b2ddc-132">Chọn **OK**.</span><span class="sxs-lookup"><span data-stu-id="b2ddc-132">Select **OK**.</span></span>

![Khôi phục thiết đặt](./media/7RestoreSetting.png)

<span data-ttu-id="b2ddc-134">Bạn sẽ nhận được xác nhận rằng khôi phục AXDB đã thành công.</span><span class="sxs-lookup"><span data-stu-id="b2ddc-134">You will receive confirmation that the AXDB restore was successful.</span></span> <span data-ttu-id="b2ddc-135">Sau khi nhận được xác nhận này, bạn có thể đóng SQL Services Management Studio.</span><span class="sxs-lookup"><span data-stu-id="b2ddc-135">After you receive this confirmation, you can close SQL Services Management Studio.</span></span>

12. <span data-ttu-id="b2ddc-136">Quay lại **Dịch vụ thông tin Internet** > **Bộ ứng dụng** > **AOSService** và bắt đầu AOSService.</span><span class="sxs-lookup"><span data-stu-id="b2ddc-136">Go back to **Internet Information Services** > **Application Pools** > **AOSService** and start the AOSService.</span></span>
13. <span data-ttu-id="b2ddc-137">Chuyển đến **Dịch vụ** và bắt đầu hai dịch vụ bạn đã ngừng trước đó.</span><span class="sxs-lookup"><span data-stu-id="b2ddc-137">Go to **Services** and start the two services you stopped earlier.</span></span>

14. <span data-ttu-id="b2ddc-138">Xác định vị trí công cụ AdminUserProvisioning trên máy ảo này.</span><span class="sxs-lookup"><span data-stu-id="b2ddc-138">Locate the AdminUserProvisioning tool on this VM.</span></span> <span data-ttu-id="b2ddc-139">Xem trong phần K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span><span class="sxs-lookup"><span data-stu-id="b2ddc-139">Look under, K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span></span>
15. <span data-ttu-id="b2ddc-140">Chạy tệp .ext bằng địa chỉ người dùng của bạn trong trường **Địa chỉ email**.</span><span class="sxs-lookup"><span data-stu-id="b2ddc-140">Run the .ext file using your user address in the **Email Address** field.</span></span> 
16. <span data-ttu-id="b2ddc-141">Chọn **Gửi**.</span><span class="sxs-lookup"><span data-stu-id="b2ddc-141">Select **Submit**.</span></span>

![Cung cấp Người dùng là quản trị viên](./media/8AdminUserProvisioning.png)

<span data-ttu-id="b2ddc-143">Quá trình này mất vài phút để hoàn thành.</span><span class="sxs-lookup"><span data-stu-id="b2ddc-143">This takes a couple of minutes to complete.</span></span> <span data-ttu-id="b2ddc-144">Bạn sẽ nhận được thông báo xác nhận rằng Người dùng là quản trị viên đã được cập nhật thành công.</span><span class="sxs-lookup"><span data-stu-id="b2ddc-144">You should receive a confirmation message that the Admin user was successfully updated.</span></span>

17. <span data-ttu-id="b2ddc-145">Cuối cùng, chạy Dấu nhắc lệnh với tư cách là Quản trị viên và thực hiện iisreset</span><span class="sxs-lookup"><span data-stu-id="b2ddc-145">Lastly, run Command Prompt as Administrator and perform iisreset</span></span>

![Đặt lại IIS](./media/9IISReset.png)

18. <span data-ttu-id="b2ddc-147">Đóng phiên máy tính từ xa và sử dụng trang **Môi trường chi tiết** LCS để đăng nhập vào môi trường để xác nhận rằng môi trường đang hoạt động như mong đợi.</span><span class="sxs-lookup"><span data-stu-id="b2ddc-147">Close the remote desktop session and use the LCS **Environment details** page to log in to the environment to confirm it is working as expected.</span></span>

![Finance and Operations](./media/10FinanceAndOperations.png)
