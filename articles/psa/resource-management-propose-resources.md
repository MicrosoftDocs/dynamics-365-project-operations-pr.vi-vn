---
title: Đề xuất nguồn lực dự án
description: Chủ đề này cung cấp thông tin về cách đề xuất các nguồn lực dự án.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 0a3eaa9929770c91523831d92744d5084aa28cb8
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147544"
---
# <a name="propose-project-resources"></a><span data-ttu-id="09997-103">Đề xuất nguồn lực dự án</span><span class="sxs-lookup"><span data-stu-id="09997-103">Propose project resources</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="09997-104">Người quản lý nguồn lực có thể đề xuất nguồn lực với người quản lý dự án bằng yêu cầu nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="09997-104">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="09997-105">Từ lưới yêu cầu hoặc tự yêu cầu, hãy chọn **Tìm nguồn lực**.</span><span class="sxs-lookup"><span data-stu-id="09997-105">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="09997-106">Trên trang **Trợ lý lập lịch biểu**, hãy chọn nguồn lực, sau đó trong ngăn **Tạo đăng ký nguồn lực**, trong trường **Trạng thái đăng ký**, hãy chọn **Đăng ký**.</span><span class="sxs-lookup"><span data-stu-id="09997-106">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

    ![Nguồn lực được đề xuất đã chọn](media/Resource-Management-image62.png)

<span data-ttu-id="09997-108">Các bản cập nhật trạng thái sau xảy ra:</span><span class="sxs-lookup"><span data-stu-id="09997-108">The following status updates occur:</span></span>

- <span data-ttu-id="09997-109">Trên trang **Trợ lý lập lịch biểu**, chỉ báo trạng thái được cập nhật để biểu thị đăng ký được đề xuất và không được đăng ký chắc chắn.</span><span class="sxs-lookup"><span data-stu-id="09997-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>

    ![Chỉ báo trạng thái cho đăng ký đề xuất trên trang Trợ lý lập lịch biểu](media/Resource-Management-image63.png)

- <span data-ttu-id="09997-111">Trên yêu cầu nguồn lực, trạng thái này được thay đổi thành **Cần đánh giá**.</span><span class="sxs-lookup"><span data-stu-id="09997-111">On the resource request, the status is changed to **Needs Review**.</span></span>

    ![Trạng thái yêu cầu nguồn lực được thay đổi thành Cần đánh giá](media/Resource-Management-image64.png)

- <span data-ttu-id="09997-113">Trên tab **Nhóm** của dự án này, giá trị **Trạng thái yêu cầu** của thành viên nhóm chung được thay đổi thành **Cần đánh giá**.</span><span class="sxs-lookup"><span data-stu-id="09997-113">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

    ![Trạng thái yêu cầu của thành viên nhóm chung được thay đổi thành Cần đánh giá trên tab Nhóm](media/Resource-Management-image48.png)

<span data-ttu-id="09997-115">Người quản lý dự án có thể chấp nhận hoặc từ chối đề xuất.</span><span class="sxs-lookup"><span data-stu-id="09997-115">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="09997-116">Khi người quản lý nguồn lực xử lý các yêu cầu nguồn lực, họ có thể dùng bất kỳ cách tiếp cận nào sau đây:</span><span class="sxs-lookup"><span data-stu-id="09997-116">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="09997-117">Đề xuất nhiều nguồn lực để đáp ứng nhu cầu nếu không có nguồn lực đơn để để thực hiện các giờ cần thiết.</span><span class="sxs-lookup"><span data-stu-id="09997-117">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="09997-118">Các giờ đề xuất sau đó được chia cho nhiều nguồn lực có thể đáp ứng các giờ yêu cầu.</span><span class="sxs-lookup"><span data-stu-id="09997-118">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="09997-119">Trong trường hợp này, giờ không thể chồng chéo.</span><span class="sxs-lookup"><span data-stu-id="09997-119">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="09997-120">Đề xuất ít nguồn lực hơn yêu cầu.</span><span class="sxs-lookup"><span data-stu-id="09997-120">Propose fewer resources than are required.</span></span> <span data-ttu-id="09997-121">Trong trường hợp này, năng lực nguồn lực đề xuất ít hơn giờ yêu cầu mà người yêu cầu chỉ định.</span><span class="sxs-lookup"><span data-stu-id="09997-121">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="09997-122">Do đó, khi người yêu cầu chấp nhận các nguồn lực đề xuất, các yêu cầu nguồn lực chưa hoàn thành được tạo để ghi lại nhu cầu còn lại.</span><span class="sxs-lookup"><span data-stu-id="09997-122">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="09997-123">Đăng ký các nguồn lực để đáp ứng nhu cầu nếu không có nguồn lực đơn sẵn có để hoàn thành công việc.</span><span class="sxs-lookup"><span data-stu-id="09997-123">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="09997-124">Đăng ký ít nguồn lực hơn yêu cầu.</span><span class="sxs-lookup"><span data-stu-id="09997-124">Book fewer resources than are required.</span></span> <span data-ttu-id="09997-125">Trong trường hợp này, giờ đăng ký ít hơn giờ yêu cầu.</span><span class="sxs-lookup"><span data-stu-id="09997-125">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="09997-126">Hệ thống hướng dẫn bạn đề xuất nguồn lực thay vì đăng ký để người yêu cầu có thể xác minh và theo dõi các nhu cầu còn lại.</span><span class="sxs-lookup"><span data-stu-id="09997-126">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="billable-utilization"></a><span data-ttu-id="09997-127">Thời gian làm việc tính phí</span><span class="sxs-lookup"><span data-stu-id="09997-127">Billable utilization</span></span>

<span data-ttu-id="09997-128">Nguồn lực có thể có thời gian làm việc tính phí mục tiêu.</span><span class="sxs-lookup"><span data-stu-id="09997-128">Resources can have a target billable utilization.</span></span> <span data-ttu-id="09997-129">Thời gian làm việc mục tiêu này được định nghĩa là thuộc tính trên vai trò mặc định của nguồn lực hoặc bộ trên bản ghi của nguồn lực riêng có thể đăng ký.</span><span class="sxs-lookup"><span data-stu-id="09997-129">This target utilization is either defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="09997-130">Phép tính thời gian làm việc dựa trên số giờ thực tế mà nguồn lực đã báo cáo bằng mục nhập thời gian được phê duyệt.</span><span class="sxs-lookup"><span data-stu-id="09997-130">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="09997-131">Công thức sau dùng để tính toán thời gian làm việc:</span><span class="sxs-lookup"><span data-stu-id="09997-131">The following formulas are used to calculate utilization:</span></span>

- <span data-ttu-id="09997-132">Thời gian làm việc tính phí = Giờ thực tế tính phí ÷ Năng lực của nguồn lực</span><span class="sxs-lookup"><span data-stu-id="09997-132">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
- <span data-ttu-id="09997-133">Thời gian làm việc không tính phí = Thời gian thực tế có ID loại thanh toán = Không tính phí, Bổ sung hoặc Không có ÷ Năng lực của nguồn lực</span><span class="sxs-lookup"><span data-stu-id="09997-133">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
- <span data-ttu-id="09997-134">Nội bộ =Thời gian thực tế không có hợp đồng bán hàng ÷ Năng lực của nguồn lực</span><span class="sxs-lookup"><span data-stu-id="09997-134">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
- <span data-ttu-id="09997-135">Năng lực của nguồn lực = Giờ làm việc của nguồn lực – Thời gian ngoài văn phòng – Ngày không làm việc</span><span class="sxs-lookup"><span data-stu-id="09997-135">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="09997-136">Bạn có thể tìm thấy dạng xem **Thời gian làm việc của nguồn lực** trong ngăn **Nguồn lực**.</span><span class="sxs-lookup"><span data-stu-id="09997-136">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

![Dạng xem thời gian làm việc của nguồn lực](media/Resource-Management-image65.png)

<span data-ttu-id="09997-138">Mỗi ô trong lưới đại diện cho phần trăm thời gian làm việc tính phí của nguồn lực trong một khoảng thời gian, chẳng hạn như ngày, tuần hoặc tháng.</span><span class="sxs-lookup"><span data-stu-id="09997-138">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="09997-139">Công thức sau dùng để tô màu các ô:</span><span class="sxs-lookup"><span data-stu-id="09997-139">The following formulas are used to color the cells:</span></span>

- <span data-ttu-id="09997-140">**Xanh lục:** Thời gian làm việc tính phí \>= Thời gian làm việc mục tiêu của nguồn lực</span><span class="sxs-lookup"><span data-stu-id="09997-140">**Green:** Billable utilization \>= Resource target utilization</span></span>
- <span data-ttu-id="09997-141">**Vàng:** Thời gian làm việc mục tiêu – 20 \<= Thời gian làm việc tính phí \< Thời gian làm việc mục tiêu</span><span class="sxs-lookup"><span data-stu-id="09997-141">**Yellow:** Target utilization – 20 \<= Billable utilization \< Target utilization</span></span>
- <span data-ttu-id="09997-142">**Đỏ:** Thời gian làm việc tính phí \< Thời gian làm việc mục tiêu – 20</span><span class="sxs-lookup"><span data-stu-id="09997-142">**Red:** Billable utilization \< Target utilization – 20</span></span>

<span data-ttu-id="09997-143">Vì dạng xem **Thời gian làm việc của nguồn lực** dựa trên Bảng lịch trình, nên bạn có thể dùng các khả năng lọc của Bảng lịch trình để lọc các kết quả.</span><span class="sxs-lookup"><span data-stu-id="09997-143">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="09997-144">Lưới yêu cầu rằng bạn đặt thời gian làm việc mục tiêu trên vai trò hoặc nguồn lực riêng.</span><span class="sxs-lookup"><span data-stu-id="09997-144">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="09997-145">Để thực hiện thiết lập này, hãy chuyển đến **Nguồn lực** \> **Vai trò nguồn lực**.</span><span class="sxs-lookup"><span data-stu-id="09997-145">To do this setup, go to **Resources** \> **Resource roles**.</span></span>

<span data-ttu-id="09997-146">Ngoài ra, vai trò mặc định phải được gán cho từng nguồn lực có thể đăng ký.</span><span class="sxs-lookup"><span data-stu-id="09997-146">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="09997-147">Truy cập vào **Nguồn lực** \> **Nguồn lực**.</span><span class="sxs-lookup"><span data-stu-id="09997-147">Go to **Resources** \> **Resources**.</span></span> <span data-ttu-id="09997-148">Trên tab **Project Service**, hãy xác minh vai trò nguồn lực được định nghĩa và trường **Là mặc định** cho vai trò được đặt thành **Có**.</span><span class="sxs-lookup"><span data-stu-id="09997-148">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field for it is set to **Yes**.</span></span> <span data-ttu-id="09997-149">Bạn có thể thêm các vai trò bổ sung mà **Là mặc định = Không**.</span><span class="sxs-lookup"><span data-stu-id="09997-149">You can add additional roles where **Is Default = No**.</span></span> <span data-ttu-id="09997-150">Vai trò mà **Là mặc định = Có** dùng để đánh giá thời gian làm việc của nguồn lực so với mục tiêu cho vai trò đó.</span><span class="sxs-lookup"><span data-stu-id="09997-150">The role where the **Is Default = Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

![Vai trò mặc định đã đặt](media/Resource-Management-image67.png)

<span data-ttu-id="09997-152">Trên tab **Project Service**, bạn cũng có thể đặt thời gian làm việc mục tiêu riêng cho nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="09997-152">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="09997-153">Sau đó, phép tính thời gian làm việc dùng thời gian làm việc mục tiêu đó để đánh giá mục tiêu của nguồn lực thay vì mục tiêu của vai trò mặc định của nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="09997-153">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="09997-154">Thời gian làm việc hiển thị cho nguồn lực chỉ khi nguồn lực được phê duyệt, thời gian tính phí trong khoảng thời gian hiển thị trong lưới.</span><span class="sxs-lookup"><span data-stu-id="09997-154">Utilization is shown for a resource only if that resource has approved, chargeable time during the period that is shown in the grid.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="09997-155">Khả năng dùng nguồn lực</span><span class="sxs-lookup"><span data-stu-id="09997-155">Resource availability</span></span>

<span data-ttu-id="09997-156">Điều quan trọng là người quản lý nguồn lực có thể xem trạng thái rảnh/bận của nguồn lực và cập nhật đăng ký.</span><span class="sxs-lookup"><span data-stu-id="09997-156">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="09997-157">Trong một số trường hợp, không có nhu cầu chính thức (yêu cầu nguồn lực) nhưng người quản lý nguồn lực phải phản hồi với nhu cầu không theo kế hoạch qua các kênh như email, cuộc gọi điện thoại hoặc tin nhắn tức thời.</span><span class="sxs-lookup"><span data-stu-id="09997-157">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="09997-158">Người quản lý nguồn lực dùng Bảng lịch trình để cập nhật tài nguyên và đăng ký.</span><span class="sxs-lookup"><span data-stu-id="09997-158">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="09997-159">Giờ làm việc của nguồn lực dùng làm cơ sở để tính toán trạng thái rảnh/bận của nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="09997-159">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="09997-160">Đăng ký nguồn lực tiêu thụ năng lực của nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="09997-160">Resource bookings consume the capacity of the resources.</span></span>

![Bảng thông tin lịch trình](media/Resource-Management-image68.png)

<span data-ttu-id="09997-162">Bảng lịch trình dùng màu và bóng để hiển thị đăng ký, trạng thái rảnh/bận, đăng ký quá mức và trạng thái của đăng ký.</span><span class="sxs-lookup"><span data-stu-id="09997-162">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="09997-163">Cài đặt trong cài đặt Bảng lịch trình cho phép bạn hiển thị chú thích.</span><span class="sxs-lookup"><span data-stu-id="09997-163">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="09997-164">Nếu một mũi tên trỏ sang phải xuất hiện bên cạnh nguồn lực riêng có thể đăng ký trên Bảng lịch trình, thì nguồn lực có thể được mở rộng để hiển thị chi tiết của công việc mà nguồn lực được đăng ký.</span><span class="sxs-lookup"><span data-stu-id="09997-164">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

![Nguồn lực có thể đăng ký được mở rộng trên Bảng lịch trình](media/Resource-Management-image69.png)

<span data-ttu-id="09997-166">Vì Dynamics 365 Project Service Automation dùng công cụ Universal Resource Scheduling, nếu bạn cũng có Dynamics 365 Field Service được cài đặt, bạn có thể xem chi tiết của đăng ký nguồn lực cho dự án, lệnh sản xuất và mọi thực thể khác mà bạn đã mở rộng lập lịch đến.</span><span class="sxs-lookup"><span data-stu-id="09997-166">Because Dynamics 365 Project Service Automation uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

![Chi tiết đăng ký nguồn lực cho dự án và lệnh sản xuất](media/Resource-Management-image70.png)

<span data-ttu-id="09997-168">Để xem thêm chi tiết về nguồn lực riêng, hãy bấm chuột phải để mở thẻ nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="09997-168">To view more details about an individual resource, right-click it to open the resource card.</span></span>

![Thẻ nguồn lực](media/Resource-Management-image71.png)
