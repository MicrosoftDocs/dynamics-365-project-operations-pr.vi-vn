---
title: Hướng dẫn cho người quản lý nguồn lực
description: Hướng dẫn cho quản trị nguồn lực trong Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 4a3f3fa7-ae1a-4139-974b-f61cc8a8bda7
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 67b400fe3e6bb60775ee144c1d3720a311204d7d
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 03/24/2020
ms.locfileid: "3757131"
---
# <a name="resource-manager-guide-project-service"></a><span data-ttu-id="36bcd-103">Hướng dẫn cho người quản lý nguồn lực (Project Service)</span><span class="sxs-lookup"><span data-stu-id="36bcd-103">Resource manager guide (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="36bcd-104">Các khả năng [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] trong [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] giúp bạn tìm đúng nguồn lực tại đúng thời điểm cho đúng dự án và đảm bảo tất cả nguồn lực được sử dụng hiệu quả.</span><span class="sxs-lookup"><span data-stu-id="36bcd-104">The [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] help you find the right resources at the right time for the right project and make sure all resources are utilized efficiently.</span></span>  
  
 <span data-ttu-id="36bcd-105">Triển khai hiệu quả cho các tư vấn viên của công ty với [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="36bcd-105">Deploy your company’s consultants efficiently and effectively with the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> <span data-ttu-id="36bcd-106">Điều này cung cấp cho bạn các công cụ bạn cần để lên lịch nguồn lực dựa trên các yêu cầu và lịch trình tư vấn dự án và các kỹ năng và tính sẵn có của tư vấn viên.</span><span class="sxs-lookup"><span data-stu-id="36bcd-106">These provide you with the tools you need to schedule resources based on the requirements and schedules of consulting projects and on the skills and availability of your consultants.</span></span> <span data-ttu-id="36bcd-107">Bạn có thể nhanh chóng tìm thấy các chuyên gia tư vấn đủ điều kiện nhất có sẵn để làm việc về các dự án và bạn có thể dễ dàng biết cách lên lịch họ tốt hơn trong thời gian của từng dự án.</span><span class="sxs-lookup"><span data-stu-id="36bcd-107">You can quickly find the most qualified consultants who are available to work on projects, and you can easily see how to better schedule them during the course of each project.</span></span>  
  
 <span data-ttu-id="36bcd-108">Lên lịch nguồn lực giúp bạn thực hiện những điều sau:</span><span class="sxs-lookup"><span data-stu-id="36bcd-108">Resource scheduling helps you do the following:</span></span>  
  
- <span data-ttu-id="36bcd-109">Kết hợp nguồn lực với dự án, dựa trên mức kỹ năng và thành thạo kết hợp với yêu cầu nguồn lực dự án.</span><span class="sxs-lookup"><span data-stu-id="36bcd-109">Match resources to projects, based on how well their skills and proficiency levels match the project resource requirements.</span></span>  
  
- <span data-ttu-id="36bcd-110">Kết hợp lịch trình của nguồn lực với lịch dự án, dựa trên tính khả dụng và thời gian rảnh theo lịch.</span><span class="sxs-lookup"><span data-stu-id="36bcd-110">Match a resource’s schedule to a project calendar, based on their availability and scheduled time off.</span></span> <span data-ttu-id="36bcd-111">Lịch mã hóa màu cung cấp cho bạn cái nhìn trực quan về tính khả dụng của nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="36bcd-111">The color-coded calendar gives you visual cues about resource availability.</span></span>  
  
- <span data-ttu-id="36bcd-112">Xem xét năng lực của từng tư vấn viên và xác định năng lực đó hiện được sử dụng như thế nào.</span><span class="sxs-lookup"><span data-stu-id="36bcd-112">Review the capacity of each consultant and determine how that capacity is currently used.</span></span> <span data-ttu-id="36bcd-113">Điều này có thể giúp bạn biết tư vấn viên có thể đang được sử dụng dưới hoặc trên mức khả năng hoặc họ đang làm việc đúng khả năng.</span><span class="sxs-lookup"><span data-stu-id="36bcd-113">This can help you find where a consultant might be under- or over-utilized, or if they’re working at capacity.</span></span>  
  
- <span data-ttu-id="36bcd-114">Chỉ định phần trăm hoặc số giờ cụ thể cho năng lực của công nhân cho một dự án.</span><span class="sxs-lookup"><span data-stu-id="36bcd-114">Assign a percentage or a specific number of hours for a worker’s capacity to a project.</span></span>  
  
- <span data-ttu-id="36bcd-115">Đăng ký nguồn lực nhóm.</span><span class="sxs-lookup"><span data-stu-id="36bcd-115">Make group resource bookings.</span></span>  
  
- <span data-ttu-id="36bcd-116">Đăng ký mềm hoặc đăng ký cứng nguồn lực và chuyển đổi số giờ đăng ký mềm thành số giờ đăng ký cứng trong một bước.</span><span class="sxs-lookup"><span data-stu-id="36bcd-116">Soft book or hard book resources, and convert soft-booked hours into hard-booked hours in one step.</span></span>  
  
- <span data-ttu-id="36bcd-117">Tự động hình thành nhóm dự án dựa trên nguồn lực đã xác định trong cấu trúc phân tích công việc cho dự án.</span><span class="sxs-lookup"><span data-stu-id="36bcd-117">Automatically form a project team based on resources defined in a work breakdown structure for a project.</span></span>  
  
- <span data-ttu-id="36bcd-118">Đáp ứng các yêu cầu nguồn lực (đăng ký, đề xuất, tìm nguồn lực thay thế).</span><span class="sxs-lookup"><span data-stu-id="36bcd-118">Fulfill resource requests (book, propose, find substitute resources).</span></span>  
  
- <span data-ttu-id="36bcd-119">Chỉ định các nguồn lực theo mô hình trung tâm (chỉ định quản lý nguồn lực) hoặc mô hình lai (quản lý nguồn lực và các quản lý khác có thể chỉ định).</span><span class="sxs-lookup"><span data-stu-id="36bcd-119">Assign resources according to a central (resource manager assigns) or hybrid model (resource manager and other managers can assign).</span></span> <span data-ttu-id="36bcd-120">Để thêm thông tin về thiết đặt một mô hình quản trị nguồn lực lai với trung tâm, hãy xem [Đặt cấu hình cho các thiết đặt cho các tham số bổ sung (Project Service)](../project-service/configure-additional-parameters-settings.md).</span><span class="sxs-lookup"><span data-stu-id="36bcd-120">For more information about setting a central versus hybrid resource management model, see [Configure additional parameters settings (Project Service)](../project-service/configure-additional-parameters-settings.md).</span></span>  
  
  <span data-ttu-id="36bcd-121">Bạn có thể quản lý nguồn lực hiệu quả trên dự án và đảm bảo rằng dự án được bố trí nhân viên phù hợp.</span><span class="sxs-lookup"><span data-stu-id="36bcd-121">You can manage resources efficiently across projects and ensure that projects are staffed appropriately.</span></span> <span data-ttu-id="36bcd-122">Bạn sẽ cần thực hiện các công việc sau:</span><span class="sxs-lookup"><span data-stu-id="36bcd-122">You’ll need to perform the following tasks:</span></span>  
  
- <span data-ttu-id="36bcd-123">[Quản lý yêu cầu nguồn lực](../project-service/manage-resource-requests.md).</span><span class="sxs-lookup"><span data-stu-id="36bcd-123">[Manage resource requests](../project-service/manage-resource-requests.md).</span></span> <span data-ttu-id="36bcd-124">Kết hợp kỹ năng và mức độ thành thạo của tư vấn viên với đúng dự án.</span><span class="sxs-lookup"><span data-stu-id="36bcd-124">Match the skills and proficiencies of your consultants to the right projects.</span></span>  
  
- <span data-ttu-id="36bcd-125">[Xem nguồn lực sẵn có](../project-service/view-resource-availability.md).</span><span class="sxs-lookup"><span data-stu-id="36bcd-125">[View resource availability](../project-service/view-resource-availability.md).</span></span> <span data-ttu-id="36bcd-126">Kiểm tra tính sẵn sàng của tư vấn viên trong dạng xem lịch.</span><span class="sxs-lookup"><span data-stu-id="36bcd-126">Check consultants’ availability in a calendar view.</span></span>  
  
- <span data-ttu-id="36bcd-127">[Xem thời gian làm việc của nguồn lực](../project-service/view-resource-utilization.md).</span><span class="sxs-lookup"><span data-stu-id="36bcd-127">[View resource utilization](../project-service/view-resource-utilization.md).</span></span> <span data-ttu-id="36bcd-128">Xem phần trăm thời gian mà tư vấn viên của bạn hiện được đăng ký.</span><span class="sxs-lookup"><span data-stu-id="36bcd-128">See the percentage of time that your consultants are currently booked.</span></span>  
  
- <span data-ttu-id="36bcd-129">[Lên lịch các nguồn lực cho dự án](../project-service/schedule-resources-project.md).</span><span class="sxs-lookup"><span data-stu-id="36bcd-129">[Schedule resources for a project](../project-service/schedule-resources-project.md).</span></span> <span data-ttu-id="36bcd-130">Lên lịch tư vấn viên cho dự án.</span><span class="sxs-lookup"><span data-stu-id="36bcd-130">Schedule consultants for a project.</span></span>  
  
  <span data-ttu-id="36bcd-131">Để biết thêm thông tin về cách gửi yêu cầu nguồn lực cho từng dự án, hãy xem [Gửi yêu cầu nguồn lực](../project-service/submit-resource-requests.md).</span><span class="sxs-lookup"><span data-stu-id="36bcd-131">For more information about submitting resource requests for individual projects, see [Submit resource requests](../project-service/submit-resource-requests.md).</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="36bcd-132">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="36bcd-132">See Also</span></span>  
 <span data-ttu-id="36bcd-133">[Tổng quan về Project Service](../project-service/overview.md) </span><span class="sxs-lookup"><span data-stu-id="36bcd-133">[Overview of Project Service](../project-service/overview.md) </span></span>  
 <span data-ttu-id="36bcd-134">[Hướng dẫn của Quản trị viên](../project-service/admin-guide.md) </span><span class="sxs-lookup"><span data-stu-id="36bcd-134">[Administrator Guide](../project-service/admin-guide.md) </span></span>  
 <span data-ttu-id="36bcd-135">[Hướng dẫn của Quản lý Khách hàng](../project-service/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="36bcd-135">[Account Manager Guiden](../project-service/account-manager-guide.md) </span></span>  
 <span data-ttu-id="36bcd-136">[Hướng dẫn của Quản lý Dự án](../project-service/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="36bcd-136">[Project Manager Guide](../project-service/project-manager-guide.md) </span></span>  
 [<span data-ttu-id="36bcd-137">Hướng dẫn về Thời gian, Chi phí và Cộng tác</span><span class="sxs-lookup"><span data-stu-id="36bcd-137">Time, Expense, and Collaboration Guide</span></span>](../project-service/time-expense-collaboration-guide.md)
