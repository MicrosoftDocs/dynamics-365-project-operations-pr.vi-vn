---
title: Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 31, V3
description: Chủ đề này liệt kê các tính năng và bản sửa lỗi có trong Bản phát hành cập nhật Project Service Automation 31, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: 160187ba7b96547e85a7a4ec4bf84c86d8fd8257
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999157"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a><span data-ttu-id="b02c8-103">Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 31, V3</span><span class="sxs-lookup"><span data-stu-id="b02c8-103">What's new or changed in Project Service Automation Update Release 31, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="b02c8-104">Chúng tôi vui mừng thông báo bản cập nhật mới nhất dành cho ứng dụng Project Service Automation của Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="b02c8-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="b02c8-105">Bản phát hành này bao gồm một số cải tiến quan trọng về chất lượng, hiệu suất và khả năng sử dụng.</span><span class="sxs-lookup"><span data-stu-id="b02c8-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="b02c8-106">Bản phát hành này tương thích với Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="b02c8-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="b02c8-107">Để cập nhật lên bản phát hành này, hãy truy cập vào Trung tâm quản trị cho trang giải pháp trực tuyến Dynamics 365 để cài đặt bản cập nhật.</span><span class="sxs-lookup"><span data-stu-id="b02c8-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="b02c8-108">Để biết thêm thông tin, hãy xem [Cài đặt, cập nhật hoặc xóa giải pháp ưu tiên](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="b02c8-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="b02c8-109">Chủ đề này liệt kê các tính năng và bản sửa lỗi mới hoặc đã thay đổi cho Project Service Automation V3, Bản phát hành cập nhật 31.</span><span class="sxs-lookup"><span data-stu-id="b02c8-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 31.</span></span> <span data-ttu-id="b02c8-110">Phiên bản này có số bản dựng là V3.10.52.77 và thường có sẵn thông qua bản tự cập nhật vào tháng 5 năm 2021.</span><span class="sxs-lookup"><span data-stu-id="b02c8-110">This version has a build number of V3.10.52.77 and is generally available through a self-update in May 2021.</span></span>

## <a name="update-release-31"></a><span data-ttu-id="b02c8-111">Phát hành bản cập nhật 31</span><span class="sxs-lookup"><span data-stu-id="b02c8-111">Update Release 31</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="b02c8-112">Sửa lỗi</span><span class="sxs-lookup"><span data-stu-id="b02c8-112">Bug fixes</span></span>

<span data-ttu-id="b02c8-113">**Thời gian và Chi phí**</span><span class="sxs-lookup"><span data-stu-id="b02c8-113">**Time and Expense**</span></span>

<span data-ttu-id="b02c8-114">Các vấn đề sau đã được khắc phục:</span><span class="sxs-lookup"><span data-stu-id="b02c8-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="b02c8-115">Các nút lệnh điều khiển mục nhập thời gian trên trang **Nguồn lực có thể đặt trước** gây khó hiểu.</span><span class="sxs-lookup"><span data-stu-id="b02c8-115">Time entry control command buttons on the **Bookable Resource** page were confusing.</span></span>
- <span data-ttu-id="b02c8-116">Một ngoại lệ tham chiếu rỗng đã được tạo trong **Project.SetTrackingFields** khi phê duyệt mục nhập thời gian.</span><span class="sxs-lookup"><span data-stu-id="b02c8-116">A null reference exception was generated in **Project.SetTrackingFields** when approving a time entry.</span></span>

<span data-ttu-id="b02c8-117">**Quản lý nguồn lực**</span><span class="sxs-lookup"><span data-stu-id="b02c8-117">**Resource Management**</span></span>

<span data-ttu-id="b02c8-118">Các vấn đề sau đã được khắc phục:</span><span class="sxs-lookup"><span data-stu-id="b02c8-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="b02c8-119">**Tạo thành viên trong nhóm** không hiển thị chính xác cài đặt siêu dữ liệu về thiết lập đăng ký cho **Trạng thái cam kết đăng ký mặc định**.</span><span class="sxs-lookup"><span data-stu-id="b02c8-119">**Create Team Member** doesn't correctly display the booking setup metadata setting for **Default Booking Committed Status**.</span></span>
- <span data-ttu-id="b02c8-120">Khi nâng cấp từ PSA 1.X lên 3.X, quá trình nâng cấp không thành công tại **UpgradeResourceRequirements**.</span><span class="sxs-lookup"><span data-stu-id="b02c8-120">When upgrading from PSA 1.X to 3.X, the upgrade process fails at **UpgradeResourceRequirements**.</span></span>


<span data-ttu-id="b02c8-121">**Bán hàng**</span><span class="sxs-lookup"><span data-stu-id="b02c8-121">**Sales**</span></span>

<span data-ttu-id="b02c8-122">Các vấn đề sau đã được khắc phục:</span><span class="sxs-lookup"><span data-stu-id="b02c8-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="b02c8-123">Doanh thu thực tế chuyển đổi số tiền sang đơn vị tiền tệ của dự án trong bảng theo dõi.</span><span class="sxs-lookup"><span data-stu-id="b02c8-123">Actual revenue converts the amounts to the project currency in the tracking grid.</span></span>
- <span data-ttu-id="b02c8-124">Đơn vị tiền tệ mặc định không rõ ràng khi tạo dòng nhật ký kế toán, mô tả báo giá và mô tả hợp đồng trong các tình huống mà đơn vị tiền tệ cơ bản của một tổ chức khác với đơn vị tiền tệ của dự án.</span><span class="sxs-lookup"><span data-stu-id="b02c8-124">The currency default is unclear when creating journal lines, quote lines, and contract lines in scenarios where an organization's base currency differs from the project currency.</span></span>
- <span data-ttu-id="b02c8-125">Truy vấn **Đang chờ xác thực nhật ký sửa chữa** không lọc theo dự án.</span><span class="sxs-lookup"><span data-stu-id="b02c8-125">**Pending correction journal validation** query doesn't filter by project.</span></span>
- <span data-ttu-id="b02c8-126">Doanh số còn lại được tính không chính xác trên một dự án.</span><span class="sxs-lookup"><span data-stu-id="b02c8-126">Remaining sales are calculated incorrectly on a project.</span></span>
- <span data-ttu-id="b02c8-127">Báo giá dựa trên liên hệ không thành công khi được tạo mà không có bảng giá.</span><span class="sxs-lookup"><span data-stu-id="b02c8-127">Quotes based on a contact fail when they are created without a price list.</span></span>
- <span data-ttu-id="b02c8-128">Không có vòng xoay xử lý nào được hiển thị khi bạn chọn **Xác nhận hóa đơn**.</span><span class="sxs-lookup"><span data-stu-id="b02c8-128">No processing spinner is shown when you select **Confirm Invoice**.</span></span>
- <span data-ttu-id="b02c8-129">Không có vòng xoay xử lý nào được hiển thị khi bạn chọn **Tạo hóa đơn**.</span><span class="sxs-lookup"><span data-stu-id="b02c8-129">No processing spinner is shown when you select **Create Invoice**.</span></span>
- <span data-ttu-id="b02c8-130">Việc đóng một báo giá khi bị mất không hủy bỏ các lượt đăng ký.</span><span class="sxs-lookup"><span data-stu-id="b02c8-130">Closing a quote as lost doesn't cancel the bookings.</span></span>







