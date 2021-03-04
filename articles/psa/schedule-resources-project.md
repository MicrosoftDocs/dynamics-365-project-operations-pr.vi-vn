---
title: Lên lịch các nguồn lực cho dự án
description: Làm cách nào để lên lịch nguồn lực cho dự án trong Project Service
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: e39c95386eb2dd31fb54878bc203bd94931274de
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150469"
---
# <a name="schedule-resources-for-a-project-project-service"></a><span data-ttu-id="fd4fa-103">Lên lịch nguồn lực cho dự án (Project Service)</span><span class="sxs-lookup"><span data-stu-id="fd4fa-103">Schedule resources for a project (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="fd4fa-104">Bạn có thể kiểm tra nguồn lực sẵn có để có được một cái nhìn tổng thể về cách đặt nguồn lực của bạn hoặc bạn có thể lọc xem theo kỹ năng, nhóm, vị trí và các tùy chọn khác.</span><span class="sxs-lookup"><span data-stu-id="fd4fa-104">You can check resource availability to get an overall view of how booked your resources are, or you can filter the view by skills, team, location, and other options.</span></span>  
  
<span data-ttu-id="fd4fa-105">Bảng lịch trình hiển thị danh sách các nguồn lực và tính sẵn có của nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="fd4fa-105">The schedule board shows list of resources and their availability.</span></span> <span data-ttu-id="fd4fa-106">Chọn một dạng xem để hiển thị tính sẵn có theo **Giờ**, **Ngày**, **Tuần** hoặc **Tháng**.</span><span class="sxs-lookup"><span data-stu-id="fd4fa-106">Select a view mode to show availability by **Hours**, **Day**, **Week**, or **Month**.</span></span>  
  
<span data-ttu-id="fd4fa-107">Trước khi sử dụng bảng lịch trình, bạn cần thiết lập bảng đó.</span><span class="sxs-lookup"><span data-stu-id="fd4fa-107">Before you use the schedule board, it’s important to set it up.</span></span> <span data-ttu-id="fd4fa-108">Để biết thêm thông tin, hãy xem phần [Đặt cấu hình bảng lịch trình (Field Service hoặc Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).</span><span class="sxs-lookup"><span data-stu-id="fd4fa-108">For more information, see [Configure the schedule board (Field Service or Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).</span></span>
  
<span data-ttu-id="fd4fa-109">Nếu bạn đang sử dụng phiên bản cũ, để tìm hiểu về tính sẵn có của nguồn lực, hãy xem phần [Xem tính sẵn có của nguồn lực](../psa/view-resource-availability.md).</span><span class="sxs-lookup"><span data-stu-id="fd4fa-109">If you are using an older version, for resource availability, see [View resource availability](../psa/view-resource-availability.md).</span></span>  

> [!IMPORTANT]
>  <span data-ttu-id="fd4fa-110">Để sử dụng chức năng đặt trước bảng thông tin lịch trình, mã hóa địa lý và dịch vụ vị trí, bạn cần bật bản đồ.</span><span class="sxs-lookup"><span data-stu-id="fd4fa-110">To use the schedule board booking functionality, geocoding, and location services, you need to turn on maps.</span></span>  
> 
> 1. <span data-ttu-id="fd4fa-111">Trên menu chính, hãy chọn **Lập lịch trình Nguồn lực** > **Quản trị**.</span><span class="sxs-lookup"><span data-stu-id="fd4fa-111">On the main menu, select **Resource Scheduling** > **Administration**.</span></span>  
> 2. <span data-ttu-id="fd4fa-112">Bấm vào **Tham số lập lịch trình**.</span><span class="sxs-lookup"><span data-stu-id="fd4fa-112">Click **Scheduling parameters**.</span></span>  
> 3. <span data-ttu-id="fd4fa-113">Mở bản ghi rồi cuộn xuống phần **Resource Scheduling Optimization**.</span><span class="sxs-lookup"><span data-stu-id="fd4fa-113">Open record and scroll down to the **Resource Scheduling Optimization** section.</span></span>  
> 4. <span data-ttu-id="fd4fa-114">Trên trường **Kết nối với Bản đồ**, chọn **Có**.</span><span class="sxs-lookup"><span data-stu-id="fd4fa-114">On the **Connect to Maps** field, choose **Yes**.</span></span>  
> 5. <span data-ttu-id="fd4fa-115">Chấp nhận điều khoản và lưu bản ghi.</span><span class="sxs-lookup"><span data-stu-id="fd4fa-115">Accept terms and save the record.</span></span>  
> 6. <span data-ttu-id="fd4fa-116">Trên menu chính, hãy chọn **Project Service** > **Bảng lịch trình**.</span><span class="sxs-lookup"><span data-stu-id="fd4fa-116">On the main menu, select **Project Service** > **Schedule board**.</span></span> <span data-ttu-id="fd4fa-117">Từ đây, có vài cách để lên lịch thủ công một yêu cầu đăng ký.</span><span class="sxs-lookup"><span data-stu-id="fd4fa-117">From here, there are several ways to manually schedule a booking requirement.</span></span> <span data-ttu-id="fd4fa-118">Chọn phương thức phù hợp với bạn.</span><span class="sxs-lookup"><span data-stu-id="fd4fa-118">Choose the method that works for you.</span></span>
  
## <a name="find-available-resources"></a><span data-ttu-id="fd4fa-119">Tìm nguồn lực sẵn có</span><span class="sxs-lookup"><span data-stu-id="fd4fa-119">Find available resources</span></span>

1.  <span data-ttu-id="fd4fa-120">Từ danh sách **Yêu cầu Đăng ký**, bấm chuột phải một đăng ký chưa được lên lịch và chọn một trong các cách sau:</span><span class="sxs-lookup"><span data-stu-id="fd4fa-120">From the **Booking Requirement** list, right-click an unscheduled booking and choose one of the following:</span></span>  
  
- <span data-ttu-id="fd4fa-121">Chọn **Tìm tính sẵn có – Nguồn lực hiện tại** để tìm kiếm nguồn lực có sẵn từ danh sách trên bảng lịch trình.</span><span class="sxs-lookup"><span data-stu-id="fd4fa-121">Choose **Find availability - Current Resources** to find an available resource from the list on the schedule board.</span></span>  
- <span data-ttu-id="fd4fa-122">Chọn **Tìm tính sẵn có – Tất cả Nguồn lực** để tìm kiếm nguồn lực có sẵn từ các nguồn lực trong hệ thống</span><span class="sxs-lookup"><span data-stu-id="fd4fa-122">Choose **Find availability - All Resources**, to find an available resource from resources in the system</span></span>  
   > [!NOTE]
   >  <span data-ttu-id="fd4fa-123">Khi bạn thực hiện điều này, các bộ lọc sẽ hiển thị tùy chọn cho yêu cầu đặt trước đã chọn.</span><span class="sxs-lookup"><span data-stu-id="fd4fa-123">When you do this, the filters will show options for the selected booking requirement.</span></span>  
  
2. <span data-ttu-id="fd4fa-124">Khi bạn thấy một vị trí có sẵn, hãy nhấp chuột phải vào vị trí thời gian trên bảng lịch trình và chọn **Đăng ký Tại đây**.</span><span class="sxs-lookup"><span data-stu-id="fd4fa-124">When you see an available slot, right-click the time slot on the schedule board and choose **Book Here**.</span></span> <span data-ttu-id="fd4fa-125">Hoặc, kéo và thả yêu cầu đăng ký vào vị trí thời gian có sẵn.</span><span class="sxs-lookup"><span data-stu-id="fd4fa-125">Or, drag and drop the booking requirement to the available time slot.</span></span>  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a><span data-ttu-id="fd4fa-126">Đăng ký nguồn lực bằng cách sử dụng dạng xem hàng ngày và xem những ai còn trống lịch</span><span class="sxs-lookup"><span data-stu-id="fd4fa-126">Book a resource using the daily view and find who’s under-booked</span></span>
  
1.  <span data-ttu-id="fd4fa-127">Trên bảng lịch trình, hãy chọn **Chế độ Xem** rồi chọn **Ngày**.</span><span class="sxs-lookup"><span data-stu-id="fd4fa-127">On the schedule board, select **View Mode** and select **Days**.</span></span>  
  
    <span data-ttu-id="fd4fa-128">Thao tác này sẽ hiển thị dạng xem lưới về số giờ một nguồn lực được đăng ký mỗi ngày và ngày nào nguồn lực đó rảnh.</span><span class="sxs-lookup"><span data-stu-id="fd4fa-128">This shows a grid view of how many hours a resource is booked per day and which days they are free.</span></span>  
  
2.  <span data-ttu-id="fd4fa-129">Nhấp vào tên nguồn lực bạn muốn đăng ký rồi chọn **Đăng ký**.</span><span class="sxs-lookup"><span data-stu-id="fd4fa-129">Click the name of the resource you want to book, and then select **Book**.</span></span>  
  
3.  <span data-ttu-id="fd4fa-130">Trên hộp thoại **Đăng ký nguồn lực (tạo)**, hãy chọn dự án mà bạn muốn đăng ký nguồn lực cùng với phương pháp đăng ký và thời gian bắt đầu cũng như kết thúc.</span><span class="sxs-lookup"><span data-stu-id="fd4fa-130">On the **Resource booking (create)** dialog box, choose the project that you want to book the resource for along with booking method and start and end times.</span></span>  
  
4.  <span data-ttu-id="fd4fa-131">Sau khi hoàn tất, hãy chọn **Đăng ký**.</span><span class="sxs-lookup"><span data-stu-id="fd4fa-131">When you’re done, select **Book**.</span></span>  
  
## <a name="view-to-the-schedule-board"></a><span data-ttu-id="fd4fa-132">Dạng xem của bảng lịch trình</span><span class="sxs-lookup"><span data-stu-id="fd4fa-132">View to the schedule board</span></span>
  
1.  <span data-ttu-id="fd4fa-133">Chọn một yêu cầu đặt trước chưa lên lịch từ danh sách ở dưới cùng.</span><span class="sxs-lookup"><span data-stu-id="fd4fa-133">Select an unscheduled booking requirement from the list at the bottom.</span></span>  
  
2.  <span data-ttu-id="fd4fa-134">Kéo yêu cầu đăng ký đến vị trí thời gian/nguồn lực có sẵn trên bảng lịch trình.</span><span class="sxs-lookup"><span data-stu-id="fd4fa-134">Drag the booking requirement to an available resource/time slot on the schedule board.</span></span>  
  
3.  <span data-ttu-id="fd4fa-135">Sau khi hoàn tất, hãy chọn **Đăng ký**.</span><span class="sxs-lookup"><span data-stu-id="fd4fa-135">When you're done, select **Book**.</span></span>  
  
### <a name="additional-resources"></a><span data-ttu-id="fd4fa-136">Tài nguyên bổ sung</span><span class="sxs-lookup"><span data-stu-id="fd4fa-136">Additional resources</span></span>  
 [<span data-ttu-id="fd4fa-137">Hướng dẫn của người quản lý nguồn lực</span><span class="sxs-lookup"><span data-stu-id="fd4fa-137">Resource manager guide</span></span>](../psa/resource-manager-guide.md)
