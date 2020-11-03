---
title: Đặt trước cho dự án
description: Chủ đề này cung cấp thông tin về cách đăng ký nguồn lực cho một dự án.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 19128264ed3db7efeeba948155f0ddbdc806c2a0
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086960"
---
# <a name="book-to-a-project"></a><span data-ttu-id="6535e-103">Đặt trước cho dự án</span><span class="sxs-lookup"><span data-stu-id="6535e-103">Book to a project</span></span>

<span data-ttu-id="6535e-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="6535e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6535e-105">Đôi khi, người quản lý dự án hoặc người quản lý nguồn lực sẽ cần phân bổ nguồn lực cho dự án mà không có yêu cầu cụ thể nào được xác định từ một thành viên chung trong nhóm.</span><span class="sxs-lookup"><span data-stu-id="6535e-105">There are times where a Project manager or Resource manager will need to allocate a resource to project without a specific requirement being defined from a generic team member.</span></span> <span data-ttu-id="6535e-106">Điều này có thể đạt được bằng một trong ba cách.</span><span class="sxs-lookup"><span data-stu-id="6535e-106">This can be achieved in one of three ways.</span></span>

- <span data-ttu-id="6535e-107">Đăng ký từ lưới thành viên nhóm</span><span class="sxs-lookup"><span data-stu-id="6535e-107">Book from the team member grid</span></span>
- <span data-ttu-id="6535e-108">Đặt trước từ bảng lịch trình</span><span class="sxs-lookup"><span data-stu-id="6535e-108">Book from the schedule board</span></span>
- <span data-ttu-id="6535e-109">Đăng ký từ biểu mẫu **Dự án**</span><span class="sxs-lookup"><span data-stu-id="6535e-109">Book from the **Project** form</span></span>

## <a name="book-from-the-team-member-grid"></a><span data-ttu-id="6535e-110">Đăng ký từ lưới thành viên nhóm</span><span class="sxs-lookup"><span data-stu-id="6535e-110">Book from the team member grid</span></span>

<span data-ttu-id="6535e-111">Nếu tổ chức của bạn đang hoạt động ở chế độ phân bổ nguồn lực kết hợp, người quản lý dự án có thể đăng ký nguồn lực trực tiếp cho dự án bằng cách hoàn thành các bước sau.</span><span class="sxs-lookup"><span data-stu-id="6535e-111">If your organization is operating in hybrid Resource allocation mode, the Project manager can book a resource directly to the project by completing the following steps.</span></span>

1. <span data-ttu-id="6535e-112">Từ dự án, chuyển đến lưới thành viên trong nhóm và chọn **Mới**.</span><span class="sxs-lookup"><span data-stu-id="6535e-112">From the project, go to the team member grid and select **New**.</span></span>
2. <span data-ttu-id="6535e-113">Xác định tên vị trí và vai trò của nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="6535e-113">Define the position name and the role of the resource.</span></span>
3. <span data-ttu-id="6535e-114">Chọn nguồn lực có thể đăng ký từ tra cứu có sẵn.</span><span class="sxs-lookup"><span data-stu-id="6535e-114">Select the bookable resource from the available lookup.</span></span>
4. <span data-ttu-id="6535e-115">Sau khi bạn chọn nguồn lực, hãy xác định thông tin trường sau để đăng ký nguồn lực:</span><span class="sxs-lookup"><span data-stu-id="6535e-115">After you select the resource, define the following field information to book the resource:</span></span>

    - <span data-ttu-id="6535e-116">Ngày bắt đầu</span><span class="sxs-lookup"><span data-stu-id="6535e-116">Start date</span></span>
    - <span data-ttu-id="6535e-117">Ngày hoàn thành</span><span class="sxs-lookup"><span data-stu-id="6535e-117">Finish date</span></span>
    - <span data-ttu-id="6535e-118">Phương pháp phân bổ</span><span class="sxs-lookup"><span data-stu-id="6535e-118">Allocation method</span></span>
    - <span data-ttu-id="6535e-119">Giờ, nếu có</span><span class="sxs-lookup"><span data-stu-id="6535e-119">Hours, if applicable</span></span>
    - <span data-ttu-id="6535e-120">Người phê duyệt dự án</span><span class="sxs-lookup"><span data-stu-id="6535e-120">Project approver</span></span>

6. <span data-ttu-id="6535e-121">Chọn **Lưu và Đóng**</span><span class="sxs-lookup"><span data-stu-id="6535e-121">Select **Save and Close**</span></span>

## <a name="book-from-the-schedule-board"></a><span data-ttu-id="6535e-122">Đặt trước từ bảng lịch trình</span><span class="sxs-lookup"><span data-stu-id="6535e-122">Book from the schedule board</span></span>

<span data-ttu-id="6535e-123">Khi người quản lý nguồn lực cần đăng ký nguồn lực trực tiếp cho một dự án, họ có thể sử dụng bảng lịch trình và yêu cầu của dự án.</span><span class="sxs-lookup"><span data-stu-id="6535e-123">When a Resource manager needs to book a resource directly to a project, they can use the schedule board and the project requirement.</span></span> <span data-ttu-id="6535e-124">Yêu cầu của dự án là một yêu cầu về nguồn lực luôn có sẵn để đăng ký.</span><span class="sxs-lookup"><span data-stu-id="6535e-124">The project requirement is a resource requirement that is always available to be booked against.</span></span> <span data-ttu-id="6535e-125">Để đăng ký trực tiếp cho một dự án từ bảng lịch trình, hãy hoàn tất các bước sau.</span><span class="sxs-lookup"><span data-stu-id="6535e-125">To book directly to a project form the schedule board, complete the following steps.</span></span>

1. <span data-ttu-id="6535e-126">Điều hướng đến bảng lịch trình và trên trang bên trái, lọc các nguồn lực bạn đang xem xét cho yêu cầu.</span><span class="sxs-lookup"><span data-stu-id="6535e-126">Navigate to the schedule board and on the left page, filter for the resources you are considering for the requirement.</span></span>
2. <span data-ttu-id="6535e-127">Trong ngăn dưới cùng, hãy chọn **Dự án** để xem danh sách các yêu cầu của dự án.</span><span class="sxs-lookup"><span data-stu-id="6535e-127">In the bottom pane, select the **Project** tab to view a list of project requirements.</span></span>
3. <span data-ttu-id="6535e-128">Kéo yêu cầu vào một nguồn lực và xác định thông tin sau:</span><span class="sxs-lookup"><span data-stu-id="6535e-128">Drag the requirement onto a resource and define the following information:</span></span>

    - <span data-ttu-id="6535e-129">Ngày bắt đầu</span><span class="sxs-lookup"><span data-stu-id="6535e-129">Start date</span></span>
    - <span data-ttu-id="6535e-130">Ngày hoàn thành</span><span class="sxs-lookup"><span data-stu-id="6535e-130">Finish date</span></span>
    - <span data-ttu-id="6535e-131">Trạng thái đăng ký</span><span class="sxs-lookup"><span data-stu-id="6535e-131">Booking status</span></span>
    - <span data-ttu-id="6535e-132">Phương thức đăng ký</span><span class="sxs-lookup"><span data-stu-id="6535e-132">Booking method</span></span>
    - <span data-ttu-id="6535e-133">Thời lượng</span><span class="sxs-lookup"><span data-stu-id="6535e-133">Duration</span></span>

## <a name="book-from-the-project-form"></a><span data-ttu-id="6535e-134">Đăng ký từ biểu mẫu Dự án</span><span class="sxs-lookup"><span data-stu-id="6535e-134">Book from the Project form</span></span>

<span data-ttu-id="6535e-135">Là người quản lý dự án, bạn có thể cần đăng ký nguồn lực cho một dự án, nhưng chỉ biết các tiêu chí chứ không phải tên của nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="6535e-135">As a Project manager, you might need to book a resource to a project, but only know the criteria rather than the name of the resource.</span></span> <span data-ttu-id="6535e-136">Hoàn thành các bước sau để sử dụng trợ lý lịch trình để tìm nguồn lực dựa trên bất kỳ thuộc tính nào có sẵn của nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="6535e-136">Complete the following steps to use the schedule assistant to find a resource based on any available attributes of the resource.</span></span> 

1. <span data-ttu-id="6535e-137">Điều hướng đến dự án và chọn **Đăng ký** để mở Trợ lý lịch trình.</span><span class="sxs-lookup"><span data-stu-id="6535e-137">Navigate to the project and select **Book** to open the Schedule Assistant.</span></span>
2. <span data-ttu-id="6535e-138">Sử dụng các bộ lọc ở bên trái của Trợ lý lịch trình, thu hẹp tiêu chí và chọn **Tìm kiếm.**</span><span class="sxs-lookup"><span data-stu-id="6535e-138">Using the filters on the left side of the Schedule Assistant, narrow the criteria and select **Search.**</span></span>
3. <span data-ttu-id="6535e-139">Dựa trên nguồn lực được trả về trong kết quả, bạn có thể đăng ký nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="6535e-139">Based on resources returned in the results, you can book a resource.</span></span>

> [!NOTE]
> <span data-ttu-id="6535e-140">Phương pháp này không tạo bất kỳ lượt đăng ký nào cho nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="6535e-140">This method doesn't create any bookings for the resource.</span></span> <span data-ttu-id="6535e-141">Thay vào đó, phương thức này sẽ thêm nguồn lực vào nhóm.</span><span class="sxs-lookup"><span data-stu-id="6535e-141">Instead, it adds the resource to the team.</span></span> <span data-ttu-id="6535e-142">Sau khi thành viên trong nhóm đã được thêm vào dự án, người quản lý dự án có thể sử dụng các lượt đăng ký duy trì hoặc mở rộng lượt đăng ký để thêm các lượt đăng ký cần thiết vào nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="6535e-142">After the team member has been added to the project, the project manager can use maintain bookings or extend bookings to add the required bookings to the resource.</span></span>
