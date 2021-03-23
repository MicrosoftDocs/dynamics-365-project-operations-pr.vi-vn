---
title: Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 12, V3
description: Chủ đề này cung cấp thông tin về tính năng mới trong Phát hành bản cập nhật Project Service Automation 12, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: f1b2fdc37fa2c2e31537b89b7027d2833e905578
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281099"
---
# <a name="project-service-automation-update-release-12-v3"></a><span data-ttu-id="9d71e-103">Phát hành bản cập nhật Project Service Automation 12, V3</span><span class="sxs-lookup"><span data-stu-id="9d71e-103">Project Service Automation Update Release 12, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="9d71e-104">Chúng tôi vui mừng thông báo bản cập nhật mới nhất cho ứng dụng Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="9d71e-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="9d71e-105">Bản phát hành này bao gồm một số cải tiến quan trọng về chất lượng, hiệu suất và khả năng sử dụng.</span><span class="sxs-lookup"><span data-stu-id="9d71e-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="9d71e-106">Bản phát hành này tương thích với Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="9d71e-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="9d71e-107">Để cập nhật lên bản phát hành này, hãy truy cập vào Trung tâm quản trị cho Dynamics 365 trực tuyến và truy cập vào trang giải pháp để cài đặt bản cập nhật.</span><span class="sxs-lookup"><span data-stu-id="9d71e-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="9d71e-108">Để biết thêm thông tin, hãy xem [Cài đặt, cập nhật hoặc xóa giải pháp ưu tiên](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="9d71e-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="9d71e-109">Chủ đề này liệt kê các tính năng và bản sửa lỗi mới hoặc đã thay đổi cho Project Service Automation V3, Bản phát hành cập nhật 12.</span><span class="sxs-lookup"><span data-stu-id="9d71e-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 12.</span></span> <span data-ttu-id="9d71e-110">Phiên bản này có số bản dựng là V3.10.2.34 và thường có sẵn thông qua bản tự cập nhật vào tháng 10 năm 2019.</span><span class="sxs-lookup"><span data-stu-id="9d71e-110">This version has a build number of V3.10.2.34 and is generally available through a self-update in October 2019.</span></span>

## <a name="update-release-12"></a><span data-ttu-id="9d71e-111">Phát hành bản cập nhật 12</span><span class="sxs-lookup"><span data-stu-id="9d71e-111">Update Release 12</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="9d71e-112">Sửa lỗi</span><span class="sxs-lookup"><span data-stu-id="9d71e-112">Bug fixes</span></span>

- <span data-ttu-id="9d71e-113">Thời gian và Chi phí</span><span class="sxs-lookup"><span data-stu-id="9d71e-113">Time and Expense</span></span>

    - <span data-ttu-id="9d71e-114">Đã sửa lỗi: Thông báo lỗi nhập thời gian đã được cập nhật với ngữ cảnh phù hợp hơn.</span><span class="sxs-lookup"><span data-stu-id="9d71e-114">Fixed: Time entry error messaging has been updated with more relevant context.</span></span>
    - <span data-ttu-id="9d71e-115">Đã sửa lỗi: Lưới nhập thời gian và lịch trình hiển thị chính xác thanh cuộn dọc khi được yêu cầu.</span><span class="sxs-lookup"><span data-stu-id="9d71e-115">Fixed: Time entry grid and schedule correctly displays the vertical scrollbar when required.</span></span>
    - <span data-ttu-id="9d71e-116">Đã sửa lỗi: Bạn không thể phê duyệt các mục nhập thời gian và chi phí đã gửi.</span><span class="sxs-lookup"><span data-stu-id="9d71e-116">Fixed: Submitted expense and time entries can be approved.</span></span>
    - <span data-ttu-id="9d71e-117">Đã sửa lỗi: Thông báo trên hộp thoại xác nhận hủy phê duyệt đã được sửa để phản ánh trạng thái phê duyệt khi thay đổi từ **Đã phê duyệt** thành **Đã gửi**.</span><span class="sxs-lookup"><span data-stu-id="9d71e-117">Fixed: Cancel approval confirmation dialog message has been corrected to reflect the status of the approval when changed from **Approved** to **Submitted**.</span></span>
    - <span data-ttu-id="9d71e-118">Đã sửa lỗi: Trường **Giá**, **Đơn vị** và **Số lượng** hiện đã bị khóa trên bản ghi Chi phí sau khi đã được phê duyệt.</span><span class="sxs-lookup"><span data-stu-id="9d71e-118">Fixed: **Price**, **Unit**, and **Quantity** fields are now locked on the Expense record after it is has been approved.</span></span>

- <span data-ttu-id="9d71e-119">Quản lý dự án</span><span class="sxs-lookup"><span data-stu-id="9d71e-119">Project Management</span></span>

    - <span data-ttu-id="9d71e-120">Đã sửa lỗi: Hành động **Mới** trong biểu mẫu chính **Thành viên nhóm** đã bị xóa.</span><span class="sxs-lookup"><span data-stu-id="9d71e-120">Fixed: **New** action on **Team member** main form has been removed.</span></span>
    - <span data-ttu-id="9d71e-121">Đã sửa lỗi: Việc gán tài nguyên đã được cập nhật để giải thích cho các lỗi làm tròn không chính xác, dẫn đến sự thay đổi trong ngày kết thúc của nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="9d71e-121">Fixed: Resource assignments have been updated to account for inaccurate rounding errors, which lead to a shift in a task’s end date.</span></span>
    - <span data-ttu-id="9d71e-122">Đã sửa lỗi: Trong lưới nhiệm vụ, các lỗi phía máy chủ có liên quan sẽ xuất hiện cho người dùng.</span><span class="sxs-lookup"><span data-stu-id="9d71e-122">Fixed: In the task grid, relevant server-side errors will be surfaced to the user.</span></span>
    - <span data-ttu-id="9d71e-123">Đã sửa lỗi: Tên của thành viên trong nhóm hiện hiển thị trong bộ chọn người thực hiện nhiệm vụ thay vì tên vị trí.</span><span class="sxs-lookup"><span data-stu-id="9d71e-123">Fixed: The team member’s name now renders in the task people picker instead of the position name.</span></span>

- <span data-ttu-id="9d71e-124">Quản lý nguồn lực</span><span class="sxs-lookup"><span data-stu-id="9d71e-124">Resource Management</span></span>

    - <span data-ttu-id="9d71e-125">Đã sửa lỗi: Chi tiết yêu cầu nguồn lực cho các dự án được tạo từ mẫu hiện sử dụng lịch dự án.</span><span class="sxs-lookup"><span data-stu-id="9d71e-125">Fixed: Resource requirement details for projects created from a template now use the project calendar.</span></span>
    - <span data-ttu-id="9d71e-126">Đã sửa lỗi: Các kỹ năng và năng lực hiện được mặc định từ dữ liệu chính của vai trò đến yêu cầu nguồn lực được tạo cho vai trò đó.</span><span class="sxs-lookup"><span data-stu-id="9d71e-126">Fixed: Skills and competencies now default from role master data to the resource requirement created for that role.</span></span>

- <span data-ttu-id="9d71e-127">Sales</span><span class="sxs-lookup"><span data-stu-id="9d71e-127">Sales</span></span>

    - <span data-ttu-id="9d71e-128">Đã sửa lỗi: Đã tìm thấy ID đối tượng trùng lặp trong biểu mẫu **chính của Hợp động**.</span><span class="sxs-lookup"><span data-stu-id="9d71e-128">Fixed: Duplicate object IDs found on the **Contract main** form.</span></span>
    - <span data-ttu-id="9d71e-129">Đã sửa lỗi: Logic đã được cập nhật để hiển thị tab **Phân tích báo giá** sao cho tab này hiển thị thiết lập siêu dữ liệu của tab.</span><span class="sxs-lookup"><span data-stu-id="9d71e-129">Fixed: Logic has been updated to make the **Quote Analysis** tab visible so that it displays the metadata setup of the tab.</span></span>
    - <span data-ttu-id="9d71e-130">Đã sửa lỗi: Ngày tháng kế toán trên bản ghi thực bắt nguồn từ ngày nhập thời gian/chi phí và không phải ngày phê duyệt.</span><span class="sxs-lookup"><span data-stu-id="9d71e-130">Fixed: Accounting date on the actual record now comes from the date of the time/expense entry date and not the date of the approval.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]