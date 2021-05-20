---
title: Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 29, V3
description: Chủ đề này liệt kê các tính năng và bản sửa lỗi có trong Bản phát hành cập nhật Project Service Automation 29, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 2ac47974b9cc8386c7446136faf48724de73efce
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948688"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a><span data-ttu-id="1b56f-103">Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 29, V3</span><span class="sxs-lookup"><span data-stu-id="1b56f-103">What's new or changed in Project Service Automation Update Release 29, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="1b56f-104">Chúng tôi vui mừng thông báo bản cập nhật mới nhất dành cho ứng dụng Project Service Automation của Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="1b56f-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="1b56f-105">Bản phát hành này bao gồm một số cải tiến quan trọng về chất lượng, hiệu suất và khả năng sử dụng.</span><span class="sxs-lookup"><span data-stu-id="1b56f-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="1b56f-106">Bản phát hành này tương thích với Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="1b56f-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="1b56f-107">Để cập nhật lên bản phát hành này, hãy truy cập vào Trung tâm quản trị cho trang giải pháp trực tuyến Dynamics 365 để cài đặt bản cập nhật.</span><span class="sxs-lookup"><span data-stu-id="1b56f-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="1b56f-108">Để biết thêm thông tin, hãy xem [Cài đặt, cập nhật hoặc xóa giải pháp ưu tiên](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="1b56f-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="1b56f-109">Chủ đề này liệt kê các tính năng và bản sửa lỗi mới hoặc đã thay đổi cho Project Service Automation V3, Bản phát hành cập nhật 29.</span><span class="sxs-lookup"><span data-stu-id="1b56f-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 29.</span></span> <span data-ttu-id="1b56f-110">Phiên bản này có số bản dựng là V3.10.47.7 và thường ra mắt rộng rãi thông qua bản tự cập nhật vào tháng 2 năm 2021.</span><span class="sxs-lookup"><span data-stu-id="1b56f-110">This version has a build number of V3.10.47.7 and is generally available through a self-update in February 2021.</span></span>

## <a name="update-release-29"></a><span data-ttu-id="1b56f-111">Phát hành bản cập nhật 29</span><span class="sxs-lookup"><span data-stu-id="1b56f-111">Update Release 29</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="1b56f-112">Sửa lỗi</span><span class="sxs-lookup"><span data-stu-id="1b56f-112">Bug fixes</span></span>

<span data-ttu-id="1b56f-113">**Thời gian và Chi phí**</span><span class="sxs-lookup"><span data-stu-id="1b56f-113">**Time and Expense**</span></span>

<span data-ttu-id="1b56f-114">Các vấn đề sau đã được khắc phục:</span><span class="sxs-lookup"><span data-stu-id="1b56f-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="1b56f-115">Người dùng không thể xem giờ làm việc được ghi vào những ngày không làm việc trong lưới nhập thời gian.</span><span class="sxs-lookup"><span data-stu-id="1b56f-115">Users can't see working hours logged on non-working days in the time entry grid.</span></span>
- <span data-ttu-id="1b56f-116">Các mục chi phí đã được phê duyệt có thể được chỉnh sửa trên lưới.</span><span class="sxs-lookup"><span data-stu-id="1b56f-116">Approved expense entries can be edited on the grid.</span></span>

<span data-ttu-id="1b56f-117">**Quản lý dự án**</span><span class="sxs-lookup"><span data-stu-id="1b56f-117">**Project Management**</span></span>

<span data-ttu-id="1b56f-118">Các vấn đề sau đã được khắc phục:</span><span class="sxs-lookup"><span data-stu-id="1b56f-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="1b56f-119">Thiếu logic xác thực để đảm bảo giờ nỗ lực phân công tài nguyên không thể bị âm.</span><span class="sxs-lookup"><span data-stu-id="1b56f-119">Missing validation logic to ensure resource assignment effort hours can't be negative.</span></span>
- <span data-ttu-id="1b56f-120">Hành động tùy chỉnh, **AssignResourcesForTask** cập nhật tất cả các trường thay vì chỉ các trường đã thay đổi.</span><span class="sxs-lookup"><span data-stu-id="1b56f-120">The custom action, **AssignResourcesForTask** updates all fields instead of only changed fields.</span></span>
- <span data-ttu-id="1b56f-121">Khi sao chép một dự án trong một môi trường có phần bổ trợ hoặc quy trình công việc được đăng ký trên sự kiện **CreateProject**, thuộc tính **msdyn_bulkgenerationstatus** không được cập nhật nếu **CopyWBSToProject** lỗi.</span><span class="sxs-lookup"><span data-stu-id="1b56f-121">When copying a project in an environment with plug-ins or workflows that are registered on the **CreateProject** event, the **msdyn_bulkgenerationstatus** attribute isn't updated if the **CopyWBSToProject** fails.</span></span>
- <span data-ttu-id="1b56f-122">Khi bạn mở rộng lịch dự án, ngày làm việc không được sắp xếp theo thứ tự tăng dần khiến một số cập nhật nhiệm vụ dự án không thành công.</span><span class="sxs-lookup"><span data-stu-id="1b56f-122">When you expand the project calendar, the working days aren't sorted in ascending order causing some project task updates to fail.</span></span>
- <span data-ttu-id="1b56f-123">Việc thay đổi Trình quản lý dự án trên một dự án hiện có sẽ kích hoạt logic mặc định của đơn vị tổ chức.</span><span class="sxs-lookup"><span data-stu-id="1b56f-123">Changing the Project Manager on an existing project triggers the organizational unit defaulting logic.</span></span>

<span data-ttu-id="1b56f-124">**Bán hàng**</span><span class="sxs-lookup"><span data-stu-id="1b56f-124">**Sales**</span></span>

<span data-ttu-id="1b56f-125">Các vấn đề sau đã được khắc phục:</span><span class="sxs-lookup"><span data-stu-id="1b56f-125">The following issues have been fixed:</span></span>

- <span data-ttu-id="1b56f-126">Tab **Thực hiện hợp đồng** trên trang **Hợp đồng** không thành công trong quá trình khởi tạo khi không có dòng hợp đồng nào.</span><span class="sxs-lookup"><span data-stu-id="1b56f-126">The **Contract Performance** tab on the **Contract** page fails silently during initialization when no contract lines are present.</span></span>