---
title: Xác định lịch dự án
description: Chủ đề này cung cấp thông tin về việc sử dụng lịch dự án để theo dõi tiến độ dự án.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1d44a2d0d8c13fb9e93b9a6da15fb3a7ce8d764c
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898043"
---
# <a name="define-project-calendars"></a><span data-ttu-id="a2800-103">Xác định lịch dự án</span><span class="sxs-lookup"><span data-stu-id="a2800-103">Define project calendars</span></span>

<span data-ttu-id="a2800-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="a2800-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a2800-105">Để tạo lịch trình dự án, bạn tạo mẫu lịch dự án xác định số giờ làm việc mỗi ngày và thời gian đóng cửa.</span><span class="sxs-lookup"><span data-stu-id="a2800-105">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="a2800-106">Để tạo mẫu lịch dự án, bạn liên kết công việc với trường **Mẫu lịch** cho dự án.</span><span class="sxs-lookup"><span data-stu-id="a2800-106">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="a2800-107">Làm theo các bước sau để tạo mẫu công việc.</span><span class="sxs-lookup"><span data-stu-id="a2800-107">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="a2800-108">Trong ngăn điều hướng bên trái, hãy chọn **Nguồn lực**.</span><span class="sxs-lookup"><span data-stu-id="a2800-108">In the left navigation pane, select **Resources**.</span></span> 
2. <span data-ttu-id="a2800-109">Trên trang danh sách **Nguồn lực**, hãy mở bản ghi người dùng rồi chọn **Hiển thị giờ làm việc**.</span><span class="sxs-lookup"><span data-stu-id="a2800-109">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="a2800-110">Đảm bảo rằng bạn cho phép cửa sổ bật lên trên trang trình duyệt.</span><span class="sxs-lookup"><span data-stu-id="a2800-110">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="a2800-111">Điều này cho phép bạn xem giờ làm việc đã đặt cho nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="a2800-111">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="a2800-112">Trên tab **Xem hàng tháng**, hãy chọn **Thiết lập**.</span><span class="sxs-lookup"><span data-stu-id="a2800-112">On the **Monthly View** tab, select **Set Up**.</span></span> <span data-ttu-id="a2800-113">Danh sách ba tùy chọn xuất hiện:</span><span class="sxs-lookup"><span data-stu-id="a2800-113">A list of three options appears:</span></span> 

  - <span data-ttu-id="a2800-114">Lịch hàng tuần mới</span><span class="sxs-lookup"><span data-stu-id="a2800-114">New Weekly Schedule</span></span>
  - <span data-ttu-id="a2800-115">Lịch hoạt động cho một ngày</span><span class="sxs-lookup"><span data-stu-id="a2800-115">Work Schedule for One Day</span></span>
  - <span data-ttu-id="a2800-116">Thời gian Rảnh</span><span class="sxs-lookup"><span data-stu-id="a2800-116">Time Off</span></span>

4. <span data-ttu-id="a2800-117">Chọn **Lịch trình hàng tuần mới** rồi đặt tùy chọn cho lịch trình nguồn lực này.</span><span class="sxs-lookup"><span data-stu-id="a2800-117">Select **New Weekly Schedule**, and then set the options for this resource schedule.</span></span> <span data-ttu-id="a2800-118">Bạn có thể đặt lịch trình hàng tuần định kỳ, tham số giờ hàng ngày, thời gian đóng cửa và hơn thế nữa.</span><span class="sxs-lookup"><span data-stu-id="a2800-118">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="a2800-119">Để đặt phạm vi ngày, hãy chọn **Lưu** rồi chọn **Đóng**.</span><span class="sxs-lookup"><span data-stu-id="a2800-119">Set the date range, select **Save**, and then select **Close**.</span></span> 
6. <span data-ttu-id="a2800-120">Quay lại trang danh sách **Nguồn lực** rồi chọn nguồn lực mà bạn đặt giờ làm việc.</span><span class="sxs-lookup"><span data-stu-id="a2800-120">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="a2800-121">Chọn **Đặt lịch ở dạng** để đặt mẫu công việc.</span><span class="sxs-lookup"><span data-stu-id="a2800-121">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="a2800-122">Trong hộp thoại **Mẫu công việc**, hãy nhập tên cho mẫu công việc rồi chọn **Áp dụng**.</span><span class="sxs-lookup"><span data-stu-id="a2800-122">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="a2800-123">Bạn hiện có thể liên kết mẫu công việc với mẫu lịch dự án.</span><span class="sxs-lookup"><span data-stu-id="a2800-123">You can now associate the work template with a project calendar template.</span></span>