---
title: Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 32, V3
description: Chủ đề này liệt kê các tính năng và bản sửa lỗi có trong Bản phát hành cập nhật Project Service Automation 32, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
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
ms.openlocfilehash: 11bf451ef4f24e2301ffde4f86a556a8a4fe30b0
ms.sourcegitcommit: 886102894244887d72e5a6213071e8d8a52c9d48
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129692"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a><span data-ttu-id="d2c63-103">Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 32, V3</span><span class="sxs-lookup"><span data-stu-id="d2c63-103">What's new or changed in Project Service Automation Update Release 32, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="d2c63-104">Chúng tôi vui mừng được công bố bản cập nhật mới nhất cho ứng dụng Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="d2c63-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="d2c63-105">Bản phát hành này bao gồm một số cải tiến quan trọng về chất lượng, hiệu suất và khả năng sử dụng.</span><span class="sxs-lookup"><span data-stu-id="d2c63-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="d2c63-106">Bản này tương thích với Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="d2c63-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="d2c63-107">Để cập nhật lên bản phát hành này, hãy truy cập trang giải pháp trực tuyến Trung tâm quản trị cho Dynamics 365 và cài đặt bản cập nhật.</span><span class="sxs-lookup"><span data-stu-id="d2c63-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="d2c63-108">Để biết thêm thông tin, hãy xem [Cài đặt, cập nhật hoặc xóa giải pháp ưu tiên](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="d2c63-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="d2c63-109">Chủ đề này liệt kê các tính năng và bản sửa lỗi mới hoặc đã thay đổi cho Project Service Automation V3, Bản phát hành cập nhật 32.</span><span class="sxs-lookup"><span data-stu-id="d2c63-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 32.</span></span> <span data-ttu-id="d2c63-110">Phiên bản này có số bản dựng là V3.10.53.108 và được phát hành rộng rãi thông qua bản tự cập nhật vào tháng 6 năm 2021.</span><span class="sxs-lookup"><span data-stu-id="d2c63-110">This version has a build number of V3.10.53.108 and is generally available through a self-update in June 2021.</span></span>

## <a name="update-release-32"></a><span data-ttu-id="d2c63-111">Phát hành bản cập nhật 32</span><span class="sxs-lookup"><span data-stu-id="d2c63-111">Update Release 32</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="d2c63-112">Sửa lỗi</span><span class="sxs-lookup"><span data-stu-id="d2c63-112">Bug fixes</span></span>

#### <a name="general"></a><span data-ttu-id="d2c63-113">Chung</span><span class="sxs-lookup"><span data-stu-id="d2c63-113">General</span></span>

- <span data-ttu-id="d2c63-114">Khi hoạt động nâng cấp lớn không thành công, thì bạn chỉ nên chặn các điểm vào ứng dụng chính để bảo đảm rằng các thực thể được chia sẻ vẫn có thể truy nhập được.</span><span class="sxs-lookup"><span data-stu-id="d2c63-114">When a major upgrade fails, only the main application entry points should be blocked, to ensure that shared entities are still accessible.</span></span>

#### <a name="time-and-expense"></a><span data-ttu-id="d2c63-115">Thời gian và Chi phí</span><span class="sxs-lookup"><span data-stu-id="d2c63-115">Time and Expense</span></span>

<span data-ttu-id="d2c63-116">Các vấn đề sau đã được khắc phục:</span><span class="sxs-lookup"><span data-stu-id="d2c63-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="d2c63-117">**TimeEntriesImportFromResourceAssignment** không duy trì thời gian bắt đầu và kết thúc của lát đường bao chỉ định nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="d2c63-117">**TimeEntriesImportFromResourceAssignment** doesn't maintain the start and end times of the resource assignment contour slice.</span></span>
- <span data-ttu-id="d2c63-118">Khi bạn chọn **Mục nhập mở** trên lưới **Mục nhập thời gian**, bạn có thể không chọn được các biểu mẫu khác.</span><span class="sxs-lookup"><span data-stu-id="d2c63-118">When you select **Open Entry** on the **Time Entry** grid, you might be prevented from selecting other forms.</span></span>
- <span data-ttu-id="d2c63-119">Trong khi bạn nhập các mục chỉ định vào mục nhập thời gian, truy vấn mã máy khách có thể tạo ra một URL dài khiến truy vấn không thành công.</span><span class="sxs-lookup"><span data-stu-id="d2c63-119">While you import assignments to time entries, the client code query could generate a long URL that fails the query.</span></span>
- <span data-ttu-id="d2c63-120">Trong lưới **Mục nhập thời gian**, sau khi một giá trị bị xóa khỏi một ô, tiêu điểm sẽ không còn ở lưới nữa.</span><span class="sxs-lookup"><span data-stu-id="d2c63-120">In the **Time Entry** grid, after a value is deleted from a cell, the focus doesn't remain in the grid.</span></span>
- <span data-ttu-id="d2c63-121">Nút **Từ chối** bị loại bỏ khỏi dạng xem **Xử lý phê duyệt** đối với các mục phê duyệt hiện đại.</span><span class="sxs-lookup"><span data-stu-id="d2c63-121">The **Reject** button has been removed from the **Processing approvals** view for modern approvals.</span></span>
- <span data-ttu-id="d2c63-122">Tính ổn định và hiệu suất của chức năng phê duyệt hàng loạt mục nhập thời gian chịu sự ảnh hưởng của các điểm bế tắc và tình trạng không xử lý được thích hợp các mục tùy chỉnh liên quan đến thực thể **Mục nhập thời gian**.</span><span class="sxs-lookup"><span data-stu-id="d2c63-122">The stability and performance of time entry bulk approval are affected by deadlocks and a failure to appropriately handle customizations that are related to the **Time Entry** entity.</span></span>

#### <a name="project-planning"></a><span data-ttu-id="d2c63-123">Lập kế hoạch dự án</span><span class="sxs-lookup"><span data-stu-id="d2c63-123">Project Planning</span></span>

- <span data-ttu-id="d2c63-124">Một ngoại lệ tham chiếu null sẽ được tạo ra khi bạn cập nhật một dự án có giá trị null ở trường **Đơn vị hợp đồng**.</span><span class="sxs-lookup"><span data-stu-id="d2c63-124">A null reference exception is generated when you update a project that has a null value in the **Contracting Unit** field.</span></span>
- <span data-ttu-id="d2c63-125">Chức năng **Làm mới số liệu tổng của dự án** tính toán sai chi phí còn lại và doanh thu còn lại trên một dự án.</span><span class="sxs-lookup"><span data-stu-id="d2c63-125">**Refresh Project Totals** incorrectly calculates the remaining cost and remaining sales on a project.</span></span>
- <span data-ttu-id="d2c63-126">Các phép tính định giá thừa gây ảnh hưởng tới hiệu suất có liên quan đến các phần cập nhật đối với đường bao chỉ định nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="d2c63-126">Redundant pricing calculations affect performance that is related to updates on resource assignment contours.</span></span>

#### <a name="resource-management"></a><span data-ttu-id="d2c63-127">Quản lý nguồn lực</span><span class="sxs-lookup"><span data-stu-id="d2c63-127">Resource Management</span></span>

<span data-ttu-id="d2c63-128">Sự cố sau đây đã được khắc phục:</span><span class="sxs-lookup"><span data-stu-id="d2c63-128">The following issue has been fixed:</span></span>

- <span data-ttu-id="d2c63-129">Khi năng lực theo lịch của một nguồn lực có thể đặt trước lớn hơn 1, Project Service Automation nhận biết không chính xác giá trị năng lực này là 0 (không).</span><span class="sxs-lookup"><span data-stu-id="d2c63-129">When a bookable resource's calendar capacity is more than 1, Project Service Automation incorrectly recognizes the capacity as 0 (zero).</span></span> <span data-ttu-id="d2c63-130">Do đó, xuất hiện một vòng lặp vô hạn ở dạng xem lịch trình.</span><span class="sxs-lookup"><span data-stu-id="d2c63-130">Therefore, an infinite loop occurs in the schedule view.</span></span>

#### <a name="sales"></a><span data-ttu-id="d2c63-131">Bán hàng</span><span class="sxs-lookup"><span data-stu-id="d2c63-131">Sales</span></span>

<span data-ttu-id="d2c63-132">Các vấn đề sau đã được khắc phục:</span><span class="sxs-lookup"><span data-stu-id="d2c63-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="d2c63-133">Khi một dòng nhật ký kế toán được tạo có loại giao dịch là tùy chỉnh, ngoại lệ tham chiếu null sau đây sẽ xuất hiện: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType (TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span><span class="sxs-lookup"><span data-stu-id="d2c63-133">When a journal line is created that has a custom transaction type, the following null reference exception occurs: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span></span>
- <span data-ttu-id="d2c63-134">Các vai trò và danh mục bị vô hiệu hóa trước khi một báo giá được sao chép sẽ không được thêm vào các vai trò và danh mục có thể tính phí của báo giá mới được sao chép.</span><span class="sxs-lookup"><span data-stu-id="d2c63-134">Roles and categories that are inactivated before a quotation is copied should not be added to chargeable roles and categories of the newly copied quotation.</span></span>
- <span data-ttu-id="d2c63-135">Ngày lập chứng từ và ngày kế toán không được căn chỉnh với ngày bắt đầu có trên chi tiết dòng hóa đơn được tạo trực tiếp trên hóa đơn nháp.</span><span class="sxs-lookup"><span data-stu-id="d2c63-135">The document date and accounting date aren't aligned with the start date that is provided on an invoice line detail that is created directly on a draft invoice.</span></span>
- <span data-ttu-id="d2c63-136">Các ngoại lệ tham chiếu null sẽ được tạo trong các tình huống có liên quan đến việc vô hiệu hóa các vai trò và danh mục trước khi một báo giá được sao chép.</span><span class="sxs-lookup"><span data-stu-id="d2c63-136">Null reference exceptions are generated in scenarios that are related to inactivation of roles and categories before a quotation is copied.</span></span>
- <span data-ttu-id="d2c63-137">Hành động **Cập nhật giá** trên trang **Dự án** không cập nhật các giá trị ước tính chi phí và ước tính vật liệu.</span><span class="sxs-lookup"><span data-stu-id="d2c63-137">The **Update Prices** action on the **Projects** page doesn't update expense estimates and material estimates.</span></span>
