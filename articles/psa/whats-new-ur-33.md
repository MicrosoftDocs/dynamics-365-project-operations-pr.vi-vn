---
title: Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 33, V3
description: Chủ đề này liệt kê các tính năng và bản sửa lỗi có trong Bản phát hành cập nhật Project Service Automation 33, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: 2c96e4abd484bb66285421baaad82ead9589bbe9
ms.sourcegitcommit: be5beba71ee9770c0083b4fe5cc89e7ec6b741b8
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334620"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a><span data-ttu-id="e4d55-103">Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 33, V3</span><span class="sxs-lookup"><span data-stu-id="e4d55-103">What's new or changed in Project Service Automation Update Release 33, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="e4d55-104">Chúng tôi vui mừng được công bố bản cập nhật mới nhất cho ứng dụng Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="e4d55-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="e4d55-105">Bản phát hành này bao gồm một số cải tiến quan trọng về chất lượng, hiệu suất và khả năng sử dụng.</span><span class="sxs-lookup"><span data-stu-id="e4d55-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="e4d55-106">Bản này tương thích với Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="e4d55-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="e4d55-107">Để cập nhật lên bản phát hành này, hãy truy cập trang giải pháp trực tuyến Trung tâm quản trị cho Dynamics 365 và cài đặt bản cập nhật.</span><span class="sxs-lookup"><span data-stu-id="e4d55-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="e4d55-108">Để biết thêm thông tin, hãy xem [Cài đặt, cập nhật hoặc xóa giải pháp ưu tiên](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="e4d55-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="e4d55-109">Chủ đề này liệt kê các tính năng và bản sửa lỗi mới hoặc đã thay đổi cho Project Service Automation V3, Bản phát hành cập nhật 33.</span><span class="sxs-lookup"><span data-stu-id="e4d55-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 33.</span></span> <span data-ttu-id="e4d55-110">Phiên bản này có số bản dựng là V3.10.54.98 và thường có sẵn thông qua bản tự cập nhật vào tháng 7 năm 2021.</span><span class="sxs-lookup"><span data-stu-id="e4d55-110">This version has a build number of V3.10.54.98 and is generally available through a self-update in July 2021.</span></span>

## <a name="update-release-33"></a><span data-ttu-id="e4d55-111">Phát hành bản cập nhật 33</span><span class="sxs-lookup"><span data-stu-id="e4d55-111">Update Release 33</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="e4d55-112">Sửa lỗi</span><span class="sxs-lookup"><span data-stu-id="e4d55-112">Bug fixes</span></span>

<span data-ttu-id="e4d55-113">**Thời gian và Chi phí**</span><span class="sxs-lookup"><span data-stu-id="e4d55-113">**Time and Expense**</span></span>

<span data-ttu-id="e4d55-114">Các vấn đề sau đã được khắc phục:</span><span class="sxs-lookup"><span data-stu-id="e4d55-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="e4d55-115">Hai trường bị khóa, **msdyn_description** và **msdyn_externaldescription** có thể chỉnh sửa sau khi gửi.</span><span class="sxs-lookup"><span data-stu-id="e4d55-115">Two locked fields, **msdyn_description** and **msdyn_externaldescription** are editable after submission.</span></span>
- <span data-ttu-id="e4d55-116">Thông báo lỗi xảy ra nếu một khoản chi phí được tạo ra không liên quan đến dự án.</span><span class="sxs-lookup"><span data-stu-id="e4d55-116">An error message occurs if an expense is created that isn't related to a project.</span></span>
- <span data-ttu-id="e4d55-117">Khi mục nhập thời gian được tạo, vai trò nguồn lực mặc định là vai trò không hoạt động.</span><span class="sxs-lookup"><span data-stu-id="e4d55-117">When a time entry is created, the resource role defaults to an inactive role.</span></span>
- <span data-ttu-id="e4d55-118">Các dòng nhật ký kế toán liên quan đến chi phí bị thu hồi và đã xóa sẽ không bị xóa.</span><span class="sxs-lookup"><span data-stu-id="e4d55-118">Journal lines associated with a recalled and deleted expense aren't deleted.</span></span>
- <span data-ttu-id="e4d55-119">Trên **Mục nhập thời gian Tạo biểu mẫu nhanh**, cập nhật dạng xem **Danh sách nhiệm vụ dự án** để thay đổi ngày được hiển thị theo mặc định thành ngày bắt đầu của nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="e4d55-119">On the **Time entry Quick Create Form**, update the **Project Task List** view to change the date displayed by default to the start date of the task.</span></span>
- <span data-ttu-id="e4d55-120">Khi bạn tạo một mục nhập thời gian từ tab **Có liên quan** của nguồn lực có thể đặt trước, mục nhập thời gian được tạo không chính xác cho người dùng đã đăng nhập thay vì nguồn lực chính có thể đặt trước.</span><span class="sxs-lookup"><span data-stu-id="e4d55-120">When you create a time entry from the **Related** tab of the bookable resource, the time entry is incorrectly created for the signed-in user instead of the parent bookable resource.</span></span>
- <span data-ttu-id="e4d55-121">Các trường mới được thêm vào hộp thoại **MDD phê duyệt hàng loạt**.</span><span class="sxs-lookup"><span data-stu-id="e4d55-121">New fields are added to the **Bulk approval MDD** dialog box.</span></span>

<span data-ttu-id="e4d55-122">**Lập kế hoạch dự án**</span><span class="sxs-lookup"><span data-stu-id="e4d55-122">**Project planning**</span></span>

<span data-ttu-id="e4d55-123">Các vấn đề sau đã được khắc phục:</span><span class="sxs-lookup"><span data-stu-id="e4d55-123">The following issues have been fixed:</span></span>
- <span data-ttu-id="e4d55-124">Hiệu suất tạo dự án chậm khi các mẫu giờ làm việc của dự án được áp dụng với các lịch phức tạp.</span><span class="sxs-lookup"><span data-stu-id="e4d55-124">Slow project creation performance when project work hour templates are applied with complex calendars.</span></span>
- <span data-ttu-id="e4d55-125">Khi ngày bắt đầu lớn hơn ngày kết thúc, lỗi sẽ hiển thị trên mẫu dự án sao chép do sự khác biệt về thành phần thời gian của mỗi trường.</span><span class="sxs-lookup"><span data-stu-id="e4d55-125">When the start date is greater than the end date, an error displays on the copy project template because of differences in the time component of each field.</span></span>

<span data-ttu-id="e4d55-126">**Quản lý nguồn lực**</span><span class="sxs-lookup"><span data-stu-id="e4d55-126">**Resource management**</span></span>

<span data-ttu-id="e4d55-127">Các vấn đề sau đã được khắc phục:</span><span class="sxs-lookup"><span data-stu-id="e4d55-127">The following issues have been fixed:</span></span>
- <span data-ttu-id="e4d55-128">Tham số không chính xác được sử dụng trong truy vấn sử dụng tài nguyên và XML dẫn đến kết quả bộ lọc không chính xác trên lưới **Thời gian làm việc của nguồn lực**.</span><span class="sxs-lookup"><span data-stu-id="e4d55-128">An incorrect parameter is used in the resource utilization query and the XML leads to incorrect filter results on the **Resource Utilization** grid.</span></span>
- <span data-ttu-id="e4d55-129">Xác nhận **Mở rộng đăng ký** hiển thị ngày kết thúc chính xác cho đăng ký.</span><span class="sxs-lookup"><span data-stu-id="e4d55-129">The **Extend Bookings** confirmation displays incorrect end date for bookings.</span></span>

<span data-ttu-id="e4d55-130">**Bán hàng**</span><span class="sxs-lookup"><span data-stu-id="e4d55-130">**Sales**</span></span>

<span data-ttu-id="e4d55-131">Các vấn đề sau đã được khắc phục:</span><span class="sxs-lookup"><span data-stu-id="e4d55-131">The following issues have been fixed:</span></span>
- <span data-ttu-id="e4d55-132">Thông báo lỗi xảy ra nếu giá danh mục được tạo với các giá trị bị thiếu.</span><span class="sxs-lookup"><span data-stu-id="e4d55-132">An error message occurs if a category price is created with missing values.</span></span>
- <span data-ttu-id="e4d55-133">Thông báo lỗi xảy ra nếu một mốc mô tả hợp đồng được tạo mà không có dòng đơn hàng.</span><span class="sxs-lookup"><span data-stu-id="e4d55-133">An error message occurs if a contract line milestone is created without an order line.</span></span>
