---
title: Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 18, V3
description: Chủ đề này liệt kê các tính năng và bản sửa lỗi có trong Bản phát hành cập nhật Project Service Automation 18, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: 1d7ea200531dd24d56a829f879e3a2532a9b38dc
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087062"
---
# <a name="project-service-automation-update-release-18-v3"></a><span data-ttu-id="8cce6-103">Phát hành bản cập nhật Project Service Automation 18, V3</span><span class="sxs-lookup"><span data-stu-id="8cce6-103">Project Service Automation Update Release 18, V3</span></span>

<span data-ttu-id="8cce6-104">Chúng tôi vui mừng thông báo bản cập nhật mới nhất dành cho ứng dụng Project Service Automation của Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="8cce6-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="8cce6-105">Bản phát hành này bao gồm một số cải tiến quan trọng về chất lượng, hiệu suất và khả năng sử dụng.</span><span class="sxs-lookup"><span data-stu-id="8cce6-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="8cce6-106">Bản phát hành này tương thích với Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="8cce6-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="8cce6-107">Để cập nhật lên bản phát hành này, hãy truy cập vào Trung tâm quản trị cho Dynamics 365 trực tuyến, rồi chuyển đến trang giải pháp để cài đặt bản cập nhật.</span><span class="sxs-lookup"><span data-stu-id="8cce6-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="8cce6-108">Để biết thêm thông tin, hãy xem [Cài đặt, cập nhật hoặc xóa giải pháp ưu tiên](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="8cce6-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="8cce6-109">Chủ đề này liệt kê các tính năng và bản sửa lỗi mới hoặc đã thay đổi cho Project Service Automation V3, Bản phát hành cập nhật 18.</span><span class="sxs-lookup"><span data-stu-id="8cce6-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 18.</span></span> <span data-ttu-id="8cce6-110">Phiên bản này có số bản dựng là V3.10.8.12 và thường có sẵn thông qua bản tự cập nhật vào tháng 4 năm 2020.</span><span class="sxs-lookup"><span data-stu-id="8cce6-110">This version has a build number of V3.10.8.12 and is generally available through a self-update in April 2020.</span></span>

## <a name="update-release-18"></a><span data-ttu-id="8cce6-111">Phát hành bản cập nhật 18</span><span class="sxs-lookup"><span data-stu-id="8cce6-111">Update Release 18</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="8cce6-112">Sửa lỗi</span><span class="sxs-lookup"><span data-stu-id="8cce6-112">Bug fixes</span></span>

<span data-ttu-id="8cce6-113">**Thời gian và Chi phí**</span><span class="sxs-lookup"><span data-stu-id="8cce6-113">**Time and Expense**</span></span>

- <span data-ttu-id="8cce6-114">Đã sửa: Dòng **Thu hồi** , **Yêu cầu** và **Hủy phê duyệt** trả về ngoại lệ có thông báo lỗi không rõ ràng.</span><span class="sxs-lookup"><span data-stu-id="8cce6-114">Fixed: **Recall** , **Request** , and **Cancel Approval** flows throw exceptions with unclear error messages.</span></span>
- <span data-ttu-id="8cce6-115">Đã sửa: Khi **Hủy phê duyệt** không thành công đối với chi phí, một lỗi ngoại lệ có liên quan không được trả về.</span><span class="sxs-lookup"><span data-stu-id="8cce6-115">Fixed: When **Cancel Approval** fails for an expense, a relevant exception error is not thrown.</span></span>
- <span data-ttu-id="8cce6-116">Đã sửa: Lưới Mục nhập thời gian xử lý không chính xác những ngày không làm việc ở Úc sau khi chuyển đổi thời gian tiết kiệm ánh sáng ban ngày (DST) vào tháng 10.</span><span class="sxs-lookup"><span data-stu-id="8cce6-116">Fixed: The Time Entry grid incorrectly handles non-working days in Australia after the daylight savings time (DST) switch in October.</span></span>
- <span data-ttu-id="8cce6-117">Đã sửa: Logic mặc định không chính xác ngăn việc gửi chi phí.</span><span class="sxs-lookup"><span data-stu-id="8cce6-117">Fixed: Incorrect defaulting logic prevents submission of expenses.</span></span>
- <span data-ttu-id="8cce6-118">Đã sửa: Khi phê duyệt mục nhập thời gian không thành công, phê duyệt vẫn ở trạng thái **Đang chờ xử lý**.</span><span class="sxs-lookup"><span data-stu-id="8cce6-118">Fixed: When time entry approval fails, the approval remains in a state of **Pending**.</span></span>
- <span data-ttu-id="8cce6-119">Đã sửa: Lỗi SQL trên các phê duyệt hàng loạt (khóa chết/thời gian chờ).</span><span class="sxs-lookup"><span data-stu-id="8cce6-119">Fixed: SQL Errors on bulk approvals (deadlock/timeout).</span></span>
- <span data-ttu-id="8cce6-120">Đã sửa: Các sự cố hiệu suất đáng kể trong trải nghiệm người dùng gây ra bằng cách cập nhật thành viên trong nhóm trong khi phê duyệt các mục thời gian.</span><span class="sxs-lookup"><span data-stu-id="8cce6-120">Fixed: Significant performance issues in the user experience caused by updating team members while approving time entries.</span></span>

<span data-ttu-id="8cce6-121">**Quản lý dự án**</span><span class="sxs-lookup"><span data-stu-id="8cce6-121">**Project Management**</span></span>

- <span data-ttu-id="8cce6-122">Đã sửa: Thông báo múi giờ được chuyển từ dạng xem **Điều hòa** thành biểu mẫu chính của **Dự án**.</span><span class="sxs-lookup"><span data-stu-id="8cce6-122">Fixed: Time zone notification moved from the **Reconciliation** view to the **Project** main form.</span></span>
- <span data-ttu-id="8cce6-123">Đã sửa: Mẫu lịch không được mặc định chính xác khi biểu mẫu của dự án mới mở.</span><span class="sxs-lookup"><span data-stu-id="8cce6-123">Fixed: Calendar template is not correctly defaulting when a new project form opens.</span></span>
- <span data-ttu-id="8cce6-124">Đã sửa: Đối với các trình duyệt dựa trên chromium, người dùng không thể dễ dàng chọn các tác vụ trước đó để xóa.</span><span class="sxs-lookup"><span data-stu-id="8cce6-124">Fixed: For chromium-based browsers, users are unable to easily select predecessor tasks to delete.</span></span>
- <span data-ttu-id="8cce6-125">Đã sửa: Tạo hoặc sao chép **Dự án từ mẫu rỗng** tìm nạp các nhiệm vụ không liên quan.</span><span class="sxs-lookup"><span data-stu-id="8cce6-125">Fixed: Creating or copying **Project from Empty template** fetches unrelated assignments.</span></span>
- <span data-ttu-id="8cce6-126">Đã sửa: Trong các trường hợp cụ thể, việc tạo một nhiệm vụ mới từ lưới tác vụ dẫn đến các bản ghi trùng lặp được tạo.</span><span class="sxs-lookup"><span data-stu-id="8cce6-126">Fixed: In specific edge cases, creating a new assignment from the task grid results in duplicate records being created.</span></span>
- <span data-ttu-id="8cce6-127">Đã sửa: Trong chế độ thủ công, người dùng không thể cập nhật ngày bắt đầu tác vụ muộn hơn ngày hiện tại được lưu.</span><span class="sxs-lookup"><span data-stu-id="8cce6-127">Fixed: In manual mode, users are unable to update task start dates to be later than the current date saved.</span></span>

<span data-ttu-id="8cce6-128">**Quản lý nguồn lực**</span><span class="sxs-lookup"><span data-stu-id="8cce6-128">**Resource Management**</span></span>

- <span data-ttu-id="8cce6-129">Đã sửa: Hàng tổng dạng xem **Điều hòa** tính sai phương sai đặt chỗ sau khi mở rộng đặt chỗ.</span><span class="sxs-lookup"><span data-stu-id="8cce6-129">Fixed: **Reconciliation** view subtotal row incorrectly calculates bookings variance after extending bookings.</span></span>
- <span data-ttu-id="8cce6-130">Đã sửa: Dạng xem **Điều hòa** hiển thị không chính xác việc gán nguồn lực khi nguồn lực có thể ghi được có lịch không khớp với lịch dự án.</span><span class="sxs-lookup"><span data-stu-id="8cce6-130">Fixed: **Reconciliation** view incorrectly displays resource assignments when the bookable resource has a calendar that does not match the project calendar.</span></span>

<span data-ttu-id="8cce6-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="8cce6-131">**Sales**</span></span>

- <span data-ttu-id="8cce6-132">Đã sửa: Khi các mục nhập thời gian được phê duyệt lại ( **Phê duyệt > Hủy>** phê duyệt lại), giá trị thực tế không tính phí trùng lặp được tạo ra.</span><span class="sxs-lookup"><span data-stu-id="8cce6-132">Fixed: When time entries are re-approved ( **Approve > Cancel >** approve again), a duplicate non-chargeable actual is created.</span></span>
