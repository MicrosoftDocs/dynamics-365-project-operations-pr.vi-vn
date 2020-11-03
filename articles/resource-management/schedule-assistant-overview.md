---
title: Tổng quan về trợ lý lịch trình
description: Chủ đề này cung cấp thông tin về cách làm việc với Trợ lý lịch trình để đặt nguồn lực.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: da551e805f395e466952df1dbb7d193bdddba358
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4086964"
---
# <a name="schedule-assistant-overview"></a><span data-ttu-id="a25ec-103">Tổng quan về trợ lý lịch trình</span><span class="sxs-lookup"><span data-stu-id="a25ec-103">Schedule assistant overview</span></span>

<span data-ttu-id="a25ec-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="a25ec-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a25ec-105">Trợ lý lịch trình được sử dụng để đặt nguồn lực dựa trên các yêu cầu do người quản lý Dự án xác định.</span><span class="sxs-lookup"><span data-stu-id="a25ec-105">The Schedule assistant is used to book resources based on requirements defined by the Project manager.</span></span> <span data-ttu-id="a25ec-106">Trợ lý lịch trình dựa vào các tham số được cung cấp trong yêu cầu nguồn lực để tìm nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="a25ec-106">The schedule assistant relies on the parameters provided in the resource requirement to find the resource.</span></span> <span data-ttu-id="a25ec-107">Trợ lý lịch trình đề xuất các nguồn lực phù hợp với các yêu cầu liên quan, như khoảng thời gian hoặc các kỹ năng cần thiết.</span><span class="sxs-lookup"><span data-stu-id="a25ec-107">The Schedule assistant recommends resources that match relevant requirements, like time windows or skills needed.</span></span>

<span data-ttu-id="a25ec-108">Sau khi các nguồn lực phù hợp được xác định, Người quản lý nguồn lực hoặc dự án có thể đặt nguồn lực cho công việc.</span><span class="sxs-lookup"><span data-stu-id="a25ec-108">After suitable resources are identified, the Resource or Project manager can book the resource to the work.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a25ec-109">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="a25ec-109">Prerequisites</span></span>

<span data-ttu-id="a25ec-110">Trợ lý lịch trình là một phần của giải pháp Universal Resource Scheduling.</span><span class="sxs-lookup"><span data-stu-id="a25ec-110">The Schedule assistant is a part of the Universal Resource Scheduling solution.</span></span> <span data-ttu-id="a25ec-111">Giải pháp này được bao gồm và cài đặt với Dynamics 365 Project Operations, Dynamics 365 Field Service và Dynamics 365 Customer Service.</span><span class="sxs-lookup"><span data-stu-id="a25ec-111">This solution is included and installed with Dynamics 365 Project Operations, Dynamics 365 Field Service, and Dynamics 365 Customer Service.</span></span>

## <a name="matching-requirements-and-resources"></a><span data-ttu-id="a25ec-112">Khớp yêu cầu và nguồn lực</span><span class="sxs-lookup"><span data-stu-id="a25ec-112">Matching requirements and resources</span></span>

<span data-ttu-id="a25ec-113">Yêu cầu nguồn lực được tạo dựa trên các thông tin chi tiết như:</span><span class="sxs-lookup"><span data-stu-id="a25ec-113">A generated resource requirement is based on details such as:</span></span>

-   <span data-ttu-id="a25ec-114">Đặc tính</span><span class="sxs-lookup"><span data-stu-id="a25ec-114">Characteristics</span></span>
-   <span data-ttu-id="a25ec-115">Vai trò</span><span class="sxs-lookup"><span data-stu-id="a25ec-115">Roles</span></span>
-   <span data-ttu-id="a25ec-116">Đơn vị kinh doanh</span><span class="sxs-lookup"><span data-stu-id="a25ec-116">Business units</span></span>
-   <span data-ttu-id="a25ec-117">Các tùy chọn nguồn lực</span><span class="sxs-lookup"><span data-stu-id="a25ec-117">Resource preferences</span></span>
-   <span data-ttu-id="a25ec-118">Đường cong nhân công</span><span class="sxs-lookup"><span data-stu-id="a25ec-118">Effort contours</span></span>
-   <span data-ttu-id="a25ec-119">Múi giờ</span><span class="sxs-lookup"><span data-stu-id="a25ec-119">Time zone</span></span>

<span data-ttu-id="a25ec-120">Trợ lý lịch trình sử dụng các chi tiết này để lọc nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="a25ec-120">The Schedule assistant uses these details to filter resources.</span></span>

## <a name="launch-the-schedule-assistant"></a><span data-ttu-id="a25ec-121">Khởi chạy Trợ lý lịch trình</span><span class="sxs-lookup"><span data-stu-id="a25ec-121">Launch the Schedule assistant</span></span>

<span data-ttu-id="a25ec-122">Có hai cách để khởi chạy trợ lý lịch trình.</span><span class="sxs-lookup"><span data-stu-id="a25ec-122">There are two ways in which the schedule assistant is launched.</span></span> <span data-ttu-id="a25ec-123">Nếu đang sử dụng chế độ kết hợp, trong lưới thành viên nhóm, bạn có thể chọn bất kỳ thành viên nào trong nhóm có yêu cầu nguồn lực chưa được đáp ứng, sau đó chọn **Đăng ký**.</span><span class="sxs-lookup"><span data-stu-id="a25ec-123">If you're using the hybrid mode, in the team member grid you can select any team member with an unfulfilled resource requirement, and then select **Book**.</span></span> <span data-ttu-id="a25ec-124">Nếu bạn đang sử dụng chế độ trung tâm, Người quản lý nguồn lực sẽ tìm và chọn nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="a25ec-124">If you're using the central mode, the Resource manager finds and selects the resource.</span></span>

## <a name="schedule-assistant-filters"></a><span data-ttu-id="a25ec-125">Bộ lọc của trợ lý lịch trình</span><span class="sxs-lookup"><span data-stu-id="a25ec-125">Schedule assistant filters</span></span>

<span data-ttu-id="a25ec-126">Sau khi Trợ lý lịch trình chạy, các thông tin chi tiết từ yêu cầu nguồn lực được hiển thị dưới dạng các giá trị được lọc trong ngăn bên trái.</span><span class="sxs-lookup"><span data-stu-id="a25ec-126">After the Schedule assistant runs, the details from the resource requirement are displayed as filtered values in the left pane.</span></span> <span data-ttu-id="a25ec-127">Người quản lý nguồn lực hoặc Người quản lý dự án có thể tinh chỉnh kết quả bằng cách điều chỉnh các bộ lọc để đáp ứng nhu cầu lập lịch trình.</span><span class="sxs-lookup"><span data-stu-id="a25ec-127">The Resource manager or the Project manager can fine-tune results by adjusting filters to meet the scheduling needs.</span></span>

<span data-ttu-id="a25ec-128">Ngăn bộ lọc hiển thị các tùy chọn liên quan đến công việc, bao gồm:</span><span class="sxs-lookup"><span data-stu-id="a25ec-128">The filter pane shows work-related options, including:</span></span>

-   <span data-ttu-id="a25ec-129">Thời điểm bắt đầu và kết thúc công việc</span><span class="sxs-lookup"><span data-stu-id="a25ec-129">Work start and end</span></span>
-   <span data-ttu-id="a25ec-130">Đặc tính</span><span class="sxs-lookup"><span data-stu-id="a25ec-130">Characteristics</span></span>
-   <span data-ttu-id="a25ec-131">Vai trò</span><span class="sxs-lookup"><span data-stu-id="a25ec-131">Roles</span></span>
-   <span data-ttu-id="a25ec-132">Đơn vị tổ chức</span><span class="sxs-lookup"><span data-stu-id="a25ec-132">Organizational units</span></span>
-   <span data-ttu-id="a25ec-133">Công ty cung cấp nguồn lực</span><span class="sxs-lookup"><span data-stu-id="a25ec-133">Resourcing company</span></span>
-   <span data-ttu-id="a25ec-134">Loại nguồn lực</span><span class="sxs-lookup"><span data-stu-id="a25ec-134">Resource types</span></span>
-   <span data-ttu-id="a25ec-135">Nguồn lực ưu tiên</span><span class="sxs-lookup"><span data-stu-id="a25ec-135">Preferred resources</span></span>
