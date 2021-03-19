---
title: Khắc phục sự cố khi làm việc trong lưới Tác vụ
description: Chủ đề này cung cấp thông tin khắc phục sự cố cần thiết khi làm việc trong lưới Tác vụ.
author: ruhercul
manager: tfehr
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: dedd989cc7c959d9ea97a0abfb13f8f1b2150a56
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286589"
---
# <a name="troubleshoot-working-in-the-task-grid"></a><span data-ttu-id="c0846-103">Khắc phục sự cố khi làm việc trong lưới Tác vụ</span><span class="sxs-lookup"><span data-stu-id="c0846-103">Troubleshoot working in the Task grid</span></span> 

<span data-ttu-id="c0846-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="c0846-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c0846-105">Chủ đề này mô tả cách khắc phục các vấn đề bạn có thể gặp phải khi làm việc với quản lý chi phí.</span><span class="sxs-lookup"><span data-stu-id="c0846-105">This topic describes how to fix issues that you might encounter while working with cost management.</span></span>

## <a name="enable-cookies"></a><span data-ttu-id="c0846-106">Bật cookie</span><span class="sxs-lookup"><span data-stu-id="c0846-106">Enable cookies</span></span>

<span data-ttu-id="c0846-107">Project Operations yêu cầu bật cookie của bên thứ ba để kết xuất cấu trúc phân tích công việc.</span><span class="sxs-lookup"><span data-stu-id="c0846-107">Project Operations requires that third-party cookies be enabled in order to render the work breakdown structure.</span></span> <span data-ttu-id="c0846-108">Khi cookie của bên thứ ba không được bật, thay vì thấy các nhiệm vụ, bạn sẽ thấy trang trống khi chọn tab **Nhiệm vụ** trên trang **Dự án**.</span><span class="sxs-lookup"><span data-stu-id="c0846-108">When third-party cookies aren't enabled, instead of seeing tasks, you will see a blank page when you select the **Tasks** tab on the **Project** page.</span></span>

![Tab trống khi cookie của bên thứ ba không được bật](media/blankschedule.png)


### <a name="workaround"></a><span data-ttu-id="c0846-110">Giải pháp thay thế</span><span class="sxs-lookup"><span data-stu-id="c0846-110">Workaround</span></span>
<span data-ttu-id="c0846-111">Đối với Microsoft Edge hoặc trình duyệt Google Chrome, các quy trình sau đây trình bày cách cập nhật cài đặt trình duyệt của bạn để bật cookie của bên thứ ba.</span><span class="sxs-lookup"><span data-stu-id="c0846-111">For Microsoft Edge or Google Chrome browsers, the following procedures outline how to update your browser setting to enable third-party cookies.</span></span>

#### <a name="microsoft-edge"></a><span data-ttu-id="c0846-112">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c0846-112">Microsoft Edge</span></span>

1. <span data-ttu-id="c0846-113">Mở trình duyệt Edge.</span><span class="sxs-lookup"><span data-stu-id="c0846-113">Open your Edge browser.</span></span>
2. <span data-ttu-id="c0846-114">Ở góc trên bên phải, chọn biểu tượng **dấu chấm lửng** (...), sau đó chọn **Cài đặt**.</span><span class="sxs-lookup"><span data-stu-id="c0846-114">In the upper-right corner, select the **ellipsis** (...), and then select **Settings**.</span></span>
3. <span data-ttu-id="c0846-115">Trong **Cookie và quyền đối với trang web**, chọn **Cookie và dữ liệu trang web**.</span><span class="sxs-lookup"><span data-stu-id="c0846-115">Under **Cookies and site permissions**, select **Cookies and site data**.</span></span>
4. <span data-ttu-id="c0846-116">Tắt tùy chọn **Chặn cookie bên thứ ba**.</span><span class="sxs-lookup"><span data-stu-id="c0846-116">Turn off **Block third-party cookies**.</span></span>

#### <a name="google-chrome"></a><span data-ttu-id="c0846-117">Google Chrome</span><span class="sxs-lookup"><span data-stu-id="c0846-117">Google Chrome</span></span>

1. <span data-ttu-id="c0846-118">Mở trình duyệt Chrome.</span><span class="sxs-lookup"><span data-stu-id="c0846-118">Open your Chrome browser.</span></span>
2. <span data-ttu-id="c0846-119">Ở góc trên bên phải, chọn dấu 3 chấm dọc, sau đó chọn **Cài đặt**.</span><span class="sxs-lookup"><span data-stu-id="c0846-119">In the upper-right corner, select the three vertical dots, and then select **Settings**.</span></span>
3. <span data-ttu-id="c0846-120">Trong **Quyền riêng tư và bảo mật**, chọn **Cookie và dữ liệu khác của trang web**.</span><span class="sxs-lookup"><span data-stu-id="c0846-120">Under **Privacy and security**, select **Cookies and other site data**.</span></span>
4. <span data-ttu-id="c0846-121">Chọn **Cho phép tất cả cookie**.</span><span class="sxs-lookup"><span data-stu-id="c0846-121">Select **Allow all cookies**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c0846-122">Nếu bạn chặn cookie của bên thứ ba, tất cả cookie và dữ liệu trang web từ các trang web khác sẽ bị chặn, ngay cả khi trang web đó được cho phép trong danh sách ngoại lệ của bạn.</span><span class="sxs-lookup"><span data-stu-id="c0846-122">If you block third-party cookies, all cookies and site data from other sites will be blocked, even if the site is allowed on your exceptions list.</span></span>

## <a name="pex-endpoint"></a><span data-ttu-id="c0846-123">Điểm cuối PEX</span><span class="sxs-lookup"><span data-stu-id="c0846-123">PEX Endpoint</span></span>

<span data-ttu-id="c0846-124">Project Operations yêu cầu tham số dự án tham chiếu đến Điểm cuối PEX.</span><span class="sxs-lookup"><span data-stu-id="c0846-124">Project Operations requires that a project parameter reference the PEX Endpoint.</span></span> <span data-ttu-id="c0846-125">Điểm cuối này phải giao tiếp được với dịch vụ được sử dụng để kết xuất cấu trúc phân tích công việc.</span><span class="sxs-lookup"><span data-stu-id="c0846-125">This endpoint is required to communicate with the service used to render the work breakdown structure.</span></span> <span data-ttu-id="c0846-126">Nếu tham số không được bật, bạn sẽ nhận được lỗi "Tham số dự án không hợp lệ".</span><span class="sxs-lookup"><span data-stu-id="c0846-126">If the parameter isn't enabled, you will receive the error, "The project parameter is not valid".</span></span> 

### <a name="workaround"></a><span data-ttu-id="c0846-127">Giải pháp thay thế</span><span class="sxs-lookup"><span data-stu-id="c0846-127">Workaround</span></span>
 ![Trường Điểm cuối PEX trên tham số dự án](media/projectparameter.png)

1. <span data-ttu-id="c0846-129">Thêm trường **Điểm cuối PEX** vào trang **Tham số dự án**.</span><span class="sxs-lookup"><span data-stu-id="c0846-129">Add the **PEX Endpoint** field to the **Project Parameters** page.</span></span>
2. <span data-ttu-id="c0846-130">Cập nhật trường này với giá trị sau: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`</span><span class="sxs-lookup"><span data-stu-id="c0846-130">Update the field with the following value: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`</span></span>
3. <span data-ttu-id="c0846-131">Xóa trường khỏi trang **Tham số dự án**.</span><span class="sxs-lookup"><span data-stu-id="c0846-131">Remove the field from the **Project Parameters** page.</span></span>

## <a name="privileges-for-project-for-the-web"></a><span data-ttu-id="c0846-132">Đặc quyền cho Dự án cho Web</span><span class="sxs-lookup"><span data-stu-id="c0846-132">Privileges for Project for the Web</span></span>

<span data-ttu-id="c0846-133">Project Operations dựa vào một dịch vụ lập lịch bên ngoài.</span><span class="sxs-lookup"><span data-stu-id="c0846-133">Project Operations relies on an external scheduling service.</span></span> <span data-ttu-id="c0846-134">Dịch vụ này yêu cầu người dùng được chỉ định nhiều vai trò để đọc và ghi cho các thực thể liên quan đến cấu trúc phân tích công việc.</span><span class="sxs-lookup"><span data-stu-id="c0846-134">The service requires that a user have several roles assigned to read and write to entities related to the work breakdown structure.</span></span> <span data-ttu-id="c0846-135">Các thực thể này bao gồm nhiệm vụ dự án, phân công nguồn lực và mức phụ thuộc nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="c0846-135">These entities include project tasks, resource assignments, and task dependencies.</span></span> <span data-ttu-id="c0846-136">Nếu người dùng không thể kết xuất cấu trúc phân tích công việc khi họ truy cập tab **Nhiệm vụ**, có thể là do chưa bật Dự án cho Project Operations.</span><span class="sxs-lookup"><span data-stu-id="c0846-136">If a user can't render the work breakdown structure when they go to the **Tasks** tab, it's probably because Project for Project Operations hasn't been enabled.</span></span> <span data-ttu-id="c0846-137">Người dùng có thể nhận được lỗi vai trò bảo mật hoặc lỗi liên quan đến từ chối quyền truy cập.</span><span class="sxs-lookup"><span data-stu-id="c0846-137">A user might receive either a security role error, or an error related to a denial of access.</span></span>


## <a name="workaround"></a><span data-ttu-id="c0846-138">Giải pháp thay thế</span><span class="sxs-lookup"><span data-stu-id="c0846-138">Workaround</span></span>

1. <span data-ttu-id="c0846-139">Đi đến **Cài đặt > Bảo mật > Người dùng > Người dùng ứng dụng**.</span><span class="sxs-lookup"><span data-stu-id="c0846-139">Go to **Setting > Security > Users > Application Users**.</span></span>  

   ![Trình đọc ứng dụng](media/applicationuser.jpg)
   
2. <span data-ttu-id="c0846-141">Nhấp đúp vào hồ sơ người dùng ứng dụng để xác minh những nội dung sau:</span><span class="sxs-lookup"><span data-stu-id="c0846-141">Double-click the application user record to verify the following:</span></span>

 - <span data-ttu-id="c0846-142">Người dùng có quyền truy cập vào dự án.</span><span class="sxs-lookup"><span data-stu-id="c0846-142">The user has access to the project.</span></span> <span data-ttu-id="c0846-143">Việc xác minh này thường được thực hiện qua việc đảm bảo rằng người dùng có vai trò bảo mật là **Quản lý dự án**.</span><span class="sxs-lookup"><span data-stu-id="c0846-143">This verification is typically done by ensuring that the user has **Project Manager** security role.</span></span>
 - <span data-ttu-id="c0846-144">Người dùng ứng dụng Microsoft Project tồn tại và được định cấu hình chính xác.</span><span class="sxs-lookup"><span data-stu-id="c0846-144">The Microsoft Project application user exists and is configured correctly.</span></span>
 
3. <span data-ttu-id="c0846-145">Nếu người dùng này chưa tồn tại, bạn có thể tạo bản ghi người dùng mới.</span><span class="sxs-lookup"><span data-stu-id="c0846-145">If this user doesn't exist, you can create a new user record.</span></span> <span data-ttu-id="c0846-146">Chọn **Người dùng mới**.</span><span class="sxs-lookup"><span data-stu-id="c0846-146">Select **New Users**.</span></span> <span data-ttu-id="c0846-147">Thay đổi biểu mẫu nhập thành **Người dùng Ứng dụng**, sau đó thêm **ID ứng dụng**.</span><span class="sxs-lookup"><span data-stu-id="c0846-147">Change the entry form to **Application User**, and then add the **Application ID**.</span></span>

   ![Chi tiết người dùng ứng dụng](media/applicationuserdetails.jpg)

4. <span data-ttu-id="c0846-149">Xác minh rằng người dùng đã được gán đúng giấy phép và dịch vụ được bật trong chi tiết gói dịch vụ của giấy phép.</span><span class="sxs-lookup"><span data-stu-id="c0846-149">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
5. <span data-ttu-id="c0846-150">Xác minh rằng người dùng có thể mở project.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="c0846-150">Verify that the user can open project.microsoft.com.</span></span>
6. <span data-ttu-id="c0846-151">Xác minh thông qua các thông số dự án rằng hệ thống đang trỏ đến đúng điểm cuối dự án.</span><span class="sxs-lookup"><span data-stu-id="c0846-151">Verify through the project parameters that the system is pointing to the correct project endpoint.</span></span>
7. <span data-ttu-id="c0846-152">Xác minh rằng người dùng ứng dụng dự án được tạo.</span><span class="sxs-lookup"><span data-stu-id="c0846-152">Verify that the project application user is created.</span></span>
8. <span data-ttu-id="c0846-153">Áp dụng các vai trò bảo mật sau cho người dùng:</span><span class="sxs-lookup"><span data-stu-id="c0846-153">Apply the following security roles to the user:</span></span>

  - <span data-ttu-id="c0846-154">Người dùng Dataverse</span><span class="sxs-lookup"><span data-stu-id="c0846-154">Dataverse User</span></span>
  - <span data-ttu-id="c0846-155">Hệ thống Project Operations</span><span class="sxs-lookup"><span data-stu-id="c0846-155">Project Operations System</span></span>
  - <span data-ttu-id="c0846-156">Hệ thống Dự án</span><span class="sxs-lookup"><span data-stu-id="c0846-156">Project System</span></span>

## <a name="error-when-updating-the-work-breakdown-structure"></a><span data-ttu-id="c0846-157">Lỗi khi cập nhật cấu trúc phân tích công việc</span><span class="sxs-lookup"><span data-stu-id="c0846-157">Error when updating the work breakdown structure</span></span>

<span data-ttu-id="c0846-158">Khi có một hoặc nhiều bản cập nhật cho cấu trúc phân tích công việc, các thay đổi cuối cùng không thành công và không được lưu.</span><span class="sxs-lookup"><span data-stu-id="c0846-158">When one or more updates are made to the work breakdown structure, the changes eventually fail and aren't saved.</span></span> <span data-ttu-id="c0846-159">Lỗi xảy ra trong lưới lịch trình ghi chú rằng "Không thể lưu thay đổi bạn thực hiện gần đây".</span><span class="sxs-lookup"><span data-stu-id="c0846-159">An error occurs in the schedule grid noting that “Recent change you’ve made couldn’t be saved.”</span></span>

### <a name="workaround"></a><span data-ttu-id="c0846-160">Giải pháp thay thế</span><span class="sxs-lookup"><span data-stu-id="c0846-160">Workaround</span></span>

1. <span data-ttu-id="c0846-161">Xác minh rằng người dùng đã được gán đúng giấy phép và dịch vụ được bật trong chi tiết gói dịch vụ của giấy phép.</span><span class="sxs-lookup"><span data-stu-id="c0846-161">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
2. <span data-ttu-id="c0846-162">Xác minh rằng người dùng có thể mở project.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="c0846-162">Verify that the user can open project.microsoft.com.</span></span>
3. <span data-ttu-id="c0846-163">Xác minh rằng hệ thống đang trỏ đến đúng điểm cuối dự án.</span><span class="sxs-lookup"><span data-stu-id="c0846-163">Verify that the system is pointing to the correct project endpoint,.</span></span>
4. <span data-ttu-id="c0846-164">Xác minh rằng người dùng Ứng dụng Dự án đã được tạo.</span><span class="sxs-lookup"><span data-stu-id="c0846-164">Verify that the Project Application user has been created.</span></span>
5. <span data-ttu-id="c0846-165">Áp dụng các vai trò bảo mật sau cho người dùng:</span><span class="sxs-lookup"><span data-stu-id="c0846-165">Apply the following security roles to the user:</span></span>
  
  - <span data-ttu-id="c0846-166">Người dùng Dataverse hoặc người dùng Cơ sở</span><span class="sxs-lookup"><span data-stu-id="c0846-166">Dataverse user or Base user</span></span>
  - <span data-ttu-id="c0846-167">Hệ thống Project Operations</span><span class="sxs-lookup"><span data-stu-id="c0846-167">Project Operations System</span></span>
  - <span data-ttu-id="c0846-168">Hệ thống Dự án</span><span class="sxs-lookup"><span data-stu-id="c0846-168">Project System</span></span>
  - <span data-ttu-id="c0846-169">Hệ thống ghi kép của Project Operations (Vai trò này là bắt buộc nếu bạn đang triển khai kịch bản dựa trên nguồn lực/hàng không nhập kho của Project Operations.)</span><span class="sxs-lookup"><span data-stu-id="c0846-169">Project Operations Dual Write System (This role is required if you are deploying the resource/non-stocked based scenario of Project Operations.)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]