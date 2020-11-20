---
title: Đánh giá nguồn lực được đề xuất
description: Chủ đề này cung cấp thông tin về cách đề xuất các nguồn lực dự án.
author: ruhercul
manager: AnnBe
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 54a0924da17eac86e2fa400540e629f6d803aa35
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401199"
---
# <a name="review-proposed-resources"></a><span data-ttu-id="5057e-103">Đánh giá nguồn lực được đề xuất</span><span class="sxs-lookup"><span data-stu-id="5057e-103">Review proposed resources</span></span>

<span data-ttu-id="5057e-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="5057e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5057e-105">Người quản lý nguồn lực có thể đề xuất nguồn lực với người quản lý dự án bằng yêu cầu nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="5057e-105">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="5057e-106">Từ lưới yêu cầu hoặc tự yêu cầu, hãy chọn **Tìm nguồn lực**.</span><span class="sxs-lookup"><span data-stu-id="5057e-106">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="5057e-107">Trên trang **Trợ lý lập lịch biểu**, hãy chọn nguồn lực, sau đó trong ngăn **Tạo đăng ký nguồn lực**, trong trường **Trạng thái đăng ký**, hãy chọn **Đăng ký**.</span><span class="sxs-lookup"><span data-stu-id="5057e-107">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

<span data-ttu-id="5057e-108">Các bản cập nhật trạng thái sau xảy ra:</span><span class="sxs-lookup"><span data-stu-id="5057e-108">The following status updates occur:</span></span>

- <span data-ttu-id="5057e-109">Trên trang **Trợ lý lập lịch biểu**, chỉ báo trạng thái được cập nhật để biểu thị đăng ký được đề xuất và không được đăng ký chắc chắn.</span><span class="sxs-lookup"><span data-stu-id="5057e-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>
- <span data-ttu-id="5057e-110">Trên yêu cầu nguồn lực, trạng thái này được thay đổi thành **Cần đánh giá**.</span><span class="sxs-lookup"><span data-stu-id="5057e-110">On the resource request, the status is changed to **Needs Review**.</span></span>
- <span data-ttu-id="5057e-111">Trên tab **Nhóm** của dự án này, giá trị **Trạng thái yêu cầu** của thành viên nhóm chung được thay đổi thành **Cần đánh giá**.</span><span class="sxs-lookup"><span data-stu-id="5057e-111">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

<span data-ttu-id="5057e-112">Người quản lý dự án có thể chấp nhận hoặc từ chối đề xuất.</span><span class="sxs-lookup"><span data-stu-id="5057e-112">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="5057e-113">Khi người quản lý nguồn lực xử lý các yêu cầu nguồn lực, họ có thể dùng bất kỳ cách tiếp cận nào sau đây:</span><span class="sxs-lookup"><span data-stu-id="5057e-113">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="5057e-114">Đề xuất nhiều nguồn lực để đáp ứng nhu cầu nếu không có nguồn lực đơn để để thực hiện các giờ cần thiết.</span><span class="sxs-lookup"><span data-stu-id="5057e-114">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="5057e-115">Các giờ đề xuất sau đó được chia cho nhiều nguồn lực có thể đáp ứng các giờ yêu cầu.</span><span class="sxs-lookup"><span data-stu-id="5057e-115">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="5057e-116">Trong trường hợp này, giờ không thể chồng chéo.</span><span class="sxs-lookup"><span data-stu-id="5057e-116">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="5057e-117">Đề xuất ít nguồn lực hơn yêu cầu.</span><span class="sxs-lookup"><span data-stu-id="5057e-117">Propose fewer resources than are required.</span></span> <span data-ttu-id="5057e-118">Trong trường hợp này, năng lực nguồn lực đề xuất ít hơn giờ yêu cầu mà người yêu cầu chỉ định.</span><span class="sxs-lookup"><span data-stu-id="5057e-118">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="5057e-119">Do đó, khi người yêu cầu chấp nhận các nguồn lực đề xuất, các yêu cầu nguồn lực chưa hoàn thành được tạo để ghi lại nhu cầu còn lại.</span><span class="sxs-lookup"><span data-stu-id="5057e-119">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="5057e-120">Đăng ký các nguồn lực để đáp ứng nhu cầu nếu không có nguồn lực đơn sẵn có để hoàn thành công việc.</span><span class="sxs-lookup"><span data-stu-id="5057e-120">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="5057e-121">Đăng ký ít nguồn lực hơn yêu cầu.</span><span class="sxs-lookup"><span data-stu-id="5057e-121">Book fewer resources than are required.</span></span> <span data-ttu-id="5057e-122">Trong trường hợp này, giờ đăng ký ít hơn giờ yêu cầu.</span><span class="sxs-lookup"><span data-stu-id="5057e-122">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="5057e-123">Hệ thống hướng dẫn bạn đề xuất nguồn lực thay vì đăng ký để người yêu cầu có thể xác minh và theo dõi các nhu cầu còn lại.</span><span class="sxs-lookup"><span data-stu-id="5057e-123">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="5057e-124">Khả năng dùng nguồn lực</span><span class="sxs-lookup"><span data-stu-id="5057e-124">Resource availability</span></span>

<span data-ttu-id="5057e-125">Điều quan trọng là người quản lý nguồn lực có thể xem trạng thái rảnh/bận của nguồn lực và cập nhật đăng ký.</span><span class="sxs-lookup"><span data-stu-id="5057e-125">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="5057e-126">Trong một số trường hợp, không có nhu cầu chính thức (yêu cầu nguồn lực) nhưng người quản lý nguồn lực phải phản hồi với nhu cầu không theo kế hoạch qua các kênh như email, cuộc gọi điện thoại hoặc tin nhắn tức thời.</span><span class="sxs-lookup"><span data-stu-id="5057e-126">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="5057e-127">Người quản lý nguồn lực dùng Bảng lịch trình để cập nhật tài nguyên và đăng ký.</span><span class="sxs-lookup"><span data-stu-id="5057e-127">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="5057e-128">Giờ làm việc của nguồn lực dùng làm cơ sở để tính toán trạng thái rảnh/bận của nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="5057e-128">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="5057e-129">Đăng ký nguồn lực tiêu thụ năng lực của nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="5057e-129">Resource bookings consume the capacity of the resources.</span></span>

<span data-ttu-id="5057e-130">Bảng lịch trình dùng màu và bóng để hiển thị đăng ký, trạng thái rảnh/bận, đăng ký quá mức và trạng thái của đăng ký.</span><span class="sxs-lookup"><span data-stu-id="5057e-130">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="5057e-131">Cài đặt trong cài đặt Bảng lịch trình cho phép bạn hiển thị chú thích.</span><span class="sxs-lookup"><span data-stu-id="5057e-131">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="5057e-132">Nếu một mũi tên trỏ sang phải xuất hiện bên cạnh nguồn lực riêng có thể đăng ký trên Bảng lịch trình, thì nguồn lực có thể được mở rộng để hiển thị chi tiết của công việc mà nguồn lực được đăng ký.</span><span class="sxs-lookup"><span data-stu-id="5057e-132">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

<span data-ttu-id="5057e-133">Do Dynamics 365 Project Operations sử dụng công cụ Universal Resource Scheduling, nếu bạn cũng đã cài Dynamics 365 Field Service, bạn có thể xem chi tiết về đăng ký nguồn lực cho dự án, lệnh sản xuất và mọi thực thể khác mà bạn đã mở rộng lịch trình đến đó.</span><span class="sxs-lookup"><span data-stu-id="5057e-133">Because Dynamics 365 Project Operations uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

<span data-ttu-id="5057e-134">Để xem thêm chi tiết về nguồn lực riêng, hãy bấm chuột phải để mở thẻ nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="5057e-134">To view more details about an individual resource, right-click it to open the resource card.</span></span>

