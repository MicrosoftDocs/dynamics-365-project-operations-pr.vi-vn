---
title: Quản lý múi giờ
description: Khi một dự án được tạo, múi giờ của nó dựa trên múi giờ được xác định trong mẫu giờ làm việc được áp dụng.
author: ruhercul
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 1480d68105be1041e791de567b180178b330d71e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997762"
---
# <a name="manage-time-zones"></a><span data-ttu-id="7dcc3-103">Quản lý múi giờ</span><span class="sxs-lookup"><span data-stu-id="7dcc3-103">Manage time zones</span></span>

<span data-ttu-id="7dcc3-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="7dcc3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


## <a name="projects"></a><span data-ttu-id="7dcc3-105">Dự án</span><span class="sxs-lookup"><span data-stu-id="7dcc3-105">Projects</span></span>

<span data-ttu-id="7dcc3-106">Khi một dự án được tạo, múi giờ dựa trên múi giờ được xác định trong mẫu giờ làm việc được áp dụng.</span><span class="sxs-lookup"><span data-stu-id="7dcc3-106">When a project is created, the time zone is based on the time zone defined in the applied work hour template.</span></span> <span data-ttu-id="7dcc3-107">Trên **Dự án**, ngày luôn tương ứng với múi giờ của người dùng đăng nhập trên từng tab, ngoại trừ tab **Tác vụ**. Khi bạn xem cấu trúc phân tích công việc, ngày tháng sẽ luôn được hiển thị trong múi giờ của dự án.</span><span class="sxs-lookup"><span data-stu-id="7dcc3-107">On the **Project** for, the dates are always relative to the time zone of the user that is logged in on each tab, except the **Task** tab. When you view the work breakdown structure, the dates will always be displayed in the project’s time zone.</span></span>

## <a name="tasks"></a><span data-ttu-id="7dcc3-108">Tác vụ</span><span class="sxs-lookup"><span data-stu-id="7dcc3-108">Tasks</span></span>

<span data-ttu-id="7dcc3-109">Khi một tác vụ được tạo, thời gian bắt đầu, thời gian kết thúc và giờ/ngày được kiểm soát bởi giờ làm việc của dự án.</span><span class="sxs-lookup"><span data-stu-id="7dcc3-109">When a task is created, the start time, end time, and hours/day is controlled by the working hours of the project.</span></span> <span data-ttu-id="7dcc3-110">Ví dụ: nếu một tác vụ được tạo với một dự án có múi giờ là -8 PST và có các giờ làm việc sau đây: 9:00 sáng đến 5:00 chiều từ Thứ Hai đến Thứ Sáu, thì bất kỳ tác vụ nào được tạo mà không có sự phân công sẽ tuân theo thời gian bắt đầu và thời gian kết thúc của lịch dự án.</span><span class="sxs-lookup"><span data-stu-id="7dcc3-110">For example, if a task is created with a project whose time zone is -8 PST and has the following working hours: 9:00 AM to 5:00 PM Monday to Friday, any task created without an assignment will respect the start time and end time of the project calendar.</span></span>

## <a name="manage-resources-with-time-zones"></a><span data-ttu-id="7dcc3-111">Quản lý nguồn lực với múi giờ</span><span class="sxs-lookup"><span data-stu-id="7dcc3-111">Manage resources with time zones</span></span>

<span data-ttu-id="7dcc3-112">Để có kết quả chính xác và dự đoán được khi sử dụng **Gia hạn mục đặt trước**, có hai điều kiện tiên quyết chính cần đáp ứng:</span><span class="sxs-lookup"><span data-stu-id="7dcc3-112">For accurate and predictable results when using **Extend Booking**, there are two key prerequisites that must be met:</span></span>  

- <span data-ttu-id="7dcc3-113">Người dùng phải đặt cấu hình múi giờ của thiết bị để khớp với múi giờ được xác định trong phần **Thiết đặt cá nhân hóa** của hệ thống.</span><span class="sxs-lookup"><span data-stu-id="7dcc3-113">The user must configure their device's time zone to match the time zone defined in the system's **Personalization Settings**.</span></span>
 
  ![Cài đặt múi giờ trong Windows 10](media/reconcile-assignments-03.png)

  ![Cài đặt múi giờ trong cài đặt cá nhân hóa](media/reconcile-assignments-04.png)
 
- <span data-ttu-id="7dcc3-116">Nguồn lực có thể đặt trước phải có ít nhất một phút thời gian làm việc trùng với các phân phối được sử dụng để xác định gia hạn được yêu cầu.</span><span class="sxs-lookup"><span data-stu-id="7dcc3-116">The bookable resource must have at least one minute of working time that overlaps with the contours that are used to define the requested extension.</span></span> <span data-ttu-id="7dcc3-117">Ví dụ: các nguồn lực sau đây có giờ làm việc rơi vào khoảng từ 9:00 sáng đến 7:00 tối.</span><span class="sxs-lookup"><span data-stu-id="7dcc3-117">For example, the following resources with working hours that fall between 9:00 AM and 7:00 PM.</span></span> 

  ![So sánh phân phối tài nguyên](media/reconcile-assignments-05.png)

<span data-ttu-id="7dcc3-119">Bảng sau đây hiển thị:</span><span class="sxs-lookup"><span data-stu-id="7dcc3-119">The following table shows:</span></span>

- <span data-ttu-id="7dcc3-120">Mẫu lịch dự án</span><span class="sxs-lookup"><span data-stu-id="7dcc3-120">A project calendar template</span></span>
- <span data-ttu-id="7dcc3-121">Nguồn lực A: Tài nguyên này có cùng lịch và nằm trong cùng múi giờ với dự án.</span><span class="sxs-lookup"><span data-stu-id="7dcc3-121">Resource A: This resource has the same calendar and is in the same time zone as the project.</span></span> <span data-ttu-id="7dcc3-122">Thời gian bắt đầu của các đăng ký sẽ là 9:00 giờ sáng.</span><span class="sxs-lookup"><span data-stu-id="7dcc3-122">The start time of the bookings will be 9:00 AM.</span></span>
- <span data-ttu-id="7dcc3-123">Nguồn lực B: Nguồn lực này thuộc một múi giờ khác so với dự án và bắt đầu lúc 7:00 sáng trong múi giờ của họ.</span><span class="sxs-lookup"><span data-stu-id="7dcc3-123">Resource B: This resource is located in a different time zone than the project and starts at 7:00 AM in their time zone.</span></span> <span data-ttu-id="7dcc3-124">Tuy nhiên, việc đăng ký sẽ bắt đầu lúc 9:00 giờ sáng vì đó là thời gian bắt đầu sớm nhất của phân phối giờ làm việc theo phân công.</span><span class="sxs-lookup"><span data-stu-id="7dcc3-124">However, the bookings will begin at 9:00 AM as that is the earliest start time of the assignment contour.</span></span>
- <span data-ttu-id="7dcc3-125">Nguồn lực C và D: Các nguồn lực thuộc các múi giờ khác nhau, cả hai đều khác nhau và khác dự án, và mục đặt trước của họ bắt đầu không sớm hơn thời gian rảnh tương ứng.</span><span class="sxs-lookup"><span data-stu-id="7dcc3-125">Resources C and D: The resources are located in different time zones, both different from each other and the project, and their bookings start no earlier than their respective available start times.</span></span>

|<span data-ttu-id="7dcc3-126">Thực thể</span><span class="sxs-lookup"><span data-stu-id="7dcc3-126">Entity</span></span>  |<span data-ttu-id="7dcc3-127">Lịch</span><span class="sxs-lookup"><span data-stu-id="7dcc3-127">Calendar</span></span>  |
|-|-|
|<span data-ttu-id="7dcc3-128">Mẫu lịch dự án</span><span class="sxs-lookup"><span data-stu-id="7dcc3-128">Project calendar template</span></span>   | ![lịch dự án](media/reconcile-assignments-06.png) |
|<span data-ttu-id="7dcc3-130">Nguồn lực A</span><span class="sxs-lookup"><span data-stu-id="7dcc3-130">Resource A</span></span>  | ![Lịch nguồn lực A](media/reconcile-assignments-06.png) |
|<span data-ttu-id="7dcc3-132">Nguồn lực B</span><span class="sxs-lookup"><span data-stu-id="7dcc3-132">Resource B</span></span>  |  ![Lịch nguồn lực B](media/reconcile-assignments-07.png) |
|<span data-ttu-id="7dcc3-134">Nguồn lực C</span><span class="sxs-lookup"><span data-stu-id="7dcc3-134">Resource C</span></span>  |  ![Lịch nguồn lực C](media/reconcile-assignments-08.png) |
|<span data-ttu-id="7dcc3-136">Nguồn lực D</span><span class="sxs-lookup"><span data-stu-id="7dcc3-136">Resource D</span></span>  | ![Lịch nguồn lực D](media/reconcile-assignments-09.png)  |
 
<span data-ttu-id="7dcc3-138">Khi bạn điều hướng đến dạng xem **Điều hòa**, các mục phân công tài nguyên và tình trạng thiếu đặt trước sẽ được hiển thị.</span><span class="sxs-lookup"><span data-stu-id="7dcc3-138">When you navigate to the **Reconciliation** view, the resource assignments and the associated booking shortages are displayed.</span></span>

![Dạng xem điều hòa trước khi gia hạn](media/reconcile-assignments-10.png)

<span data-ttu-id="7dcc3-140">Sau khi chức năng gia hạn đặt trước đã được sử dụng cho mỗi nguồn lực, nội dung đặt trước được mở rộng thành công cho từng nguồn lực do giờ làm việc của mỗi nguồn lực trùng với ranh giới thiếu hụt.</span><span class="sxs-lookup"><span data-stu-id="7dcc3-140">After the extend booking functionality has been used for each resource, bookings are successfully extended for each resource because each resource’s working hours overlapped with the contours of the shortage.</span></span>

![Dạng xem điều hòa sau khi gia hạn đăng ký](media/reconcile-assignments-11.png) 

<span data-ttu-id="7dcc3-142">Lưu ý rằng việc xem xét kỹ hơn các chi tiết của đặt chỗ sẽ cho thấy sự khác biệt về thời gian bắt đầu của mục đặt trước.</span><span class="sxs-lookup"><span data-stu-id="7dcc3-142">Notice that a closer look at the details of the bookings shows differences in the start time of the bookings.</span></span> <span data-ttu-id="7dcc3-143">Việc đặt trước bắt đầu không sớm hơn thời gian bắt đầu của ranh giới phân công và không sớm hơn thời gian bắt đầu có sẵn của nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="7dcc3-143">The bookings start no earlier than the start time of the assignment contour and no earlier than the available start time of the resource.</span></span>

![Các đăng ký nguồn lực mới trong bảng lịch trình](media/reconcile-assignments-12.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]