---
title: Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 23, V3
description: Chủ đề này liệt kê các tính năng và bản sửa lỗi có trong Bản phát hành cập nhật Project Service Automation 23, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: adf893a0627ae59f2132bb46686110dafda01d3d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006492"
---
# <a name="project-service-automation-update-release-23-v3"></a><span data-ttu-id="0576c-103">Phát hành bản cập nhật Project Service Automation 23, V3</span><span class="sxs-lookup"><span data-stu-id="0576c-103">Project Service Automation Update Release 23, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="0576c-104">Chúng tôi vui mừng thông báo bản cập nhật mới nhất dành cho ứng dụng Project Service Automation của Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="0576c-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="0576c-105">Bản phát hành này bao gồm một số cải tiến quan trọng về chất lượng, hiệu suất và khả năng sử dụng.</span><span class="sxs-lookup"><span data-stu-id="0576c-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="0576c-106">Bản phát hành này tương thích với Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="0576c-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="0576c-107">Để cập nhật lên bản phát hành này, hãy truy cập vào Trung tâm quản trị cho trang giải pháp trực tuyến Dynamics 365 để cài đặt bản cập nhật.</span><span class="sxs-lookup"><span data-stu-id="0576c-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="0576c-108">Để biết thêm thông tin, hãy xem [Cài đặt, cập nhật hoặc xóa giải pháp ưu tiên](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="0576c-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="0576c-109">Chủ đề này liệt kê các tính năng và bản sửa lỗi mới hoặc đã thay đổi cho Project Service Automation V3, Bản phát hành cập nhật 23.</span><span class="sxs-lookup"><span data-stu-id="0576c-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 23.</span></span> <span data-ttu-id="0576c-110">Phiên bản này có số bản dựng là V 3.10.34.30 và thường có sẵn thông qua bản tự cập nhật vào tháng 8 năm 2020.</span><span class="sxs-lookup"><span data-stu-id="0576c-110">This version has a build number of V 3.10.34.30 and is generally available through a self-update in August 2020.</span></span>

## <a name="update-release-23"></a><span data-ttu-id="0576c-111">Phát hành bản cập nhật 23</span><span class="sxs-lookup"><span data-stu-id="0576c-111">Update Release 23</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="0576c-112">Sửa lỗi</span><span class="sxs-lookup"><span data-stu-id="0576c-112">Bug fixes</span></span>

<span data-ttu-id="0576c-113">**Thời gian và Chi phí**</span><span class="sxs-lookup"><span data-stu-id="0576c-113">**Time and Expense**</span></span>

<span data-ttu-id="0576c-114">Các vấn đề sau đã được khắc phục:</span><span class="sxs-lookup"><span data-stu-id="0576c-114">The following issues have been fixed:</span></span>
- <span data-ttu-id="0576c-115">Xử lý trường hợp cạnh trong **Xóa thành viên nhóm dự án** để cung cấp một ngoại lệ có ý nghĩa.</span><span class="sxs-lookup"><span data-stu-id="0576c-115">Handle edge case in **Project Team Member Delete** to provide a meaningful exception.</span></span>
- <span data-ttu-id="0576c-116">Kết quả nhập mục phân công trong một màn hình xóa trống.</span><span class="sxs-lookup"><span data-stu-id="0576c-116">Assignment import results in a blank remove screen.</span></span>

<span data-ttu-id="0576c-117">**Quản lý nguồn lực**</span><span class="sxs-lookup"><span data-stu-id="0576c-117">**Resource Management**</span></span>

<span data-ttu-id="0576c-118">Các vấn đề sau đã được khắc phục:</span><span class="sxs-lookup"><span data-stu-id="0576c-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="0576c-119">**Thẻ tài nguyên lưới thời gian làm việc của nguồn lực** cho thấy dữ liệu không chính xác khi thang thời gian lớn hơn năm ngày.</span><span class="sxs-lookup"><span data-stu-id="0576c-119">The **Resource utilization grid resource card** shows incorrect data when the time scale is more than five days.</span></span>
- <span data-ttu-id="0576c-120">Khi khách hàng tạo nguồn lực có thể đặt trước, phần bổ trợ liên tục không thể tự động thêm nguồn lực vào nhóm Microsoft Office 365.</span><span class="sxs-lookup"><span data-stu-id="0576c-120">When customers create a bookable resource, the plug-in intermittently fails to automatically add the resource to a Microsoft Office 365 group.</span></span>
- <span data-ttu-id="0576c-121">Dạng xem **điều hòa** hiển thị các đường viền thủ công không chính xác trong dạng xem **Tuần** hoặc **Tháng**.</span><span class="sxs-lookup"><span data-stu-id="0576c-121">**Reconciliation** view displays manual contours incorrectly in the **Week** or **Month** view.</span></span>

<span data-ttu-id="0576c-122">**Quản lý dự án**</span><span class="sxs-lookup"><span data-stu-id="0576c-122">**Project Management**</span></span>

<span data-ttu-id="0576c-123">Các vấn đề sau đã được khắc phục:</span><span class="sxs-lookup"><span data-stu-id="0576c-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="0576c-124">Một số lượng thực thể **RetrieveMultiple cho usersettings** quá lớn đang làm giảm hiệu suất cho các mục phê duyệt dự án và các thao tác khác.</span><span class="sxs-lookup"><span data-stu-id="0576c-124">An excessive number of **RetrieveMultiple for usersettings** entities are causing degraded performance for project approvals and other operations.</span></span>
- <span data-ttu-id="0576c-125">Tính năng tra cứu nguồn lực trong lưới **Lập kế hoạch nhiệm vụ** giới hạn để chỉ hiển thị năm thành viên nhóm từ nhóm dự án.</span><span class="sxs-lookup"><span data-stu-id="0576c-125">The **Task Planning** grid resource lookup is limited to only show up to five team members from the project team.</span></span> 
- <span data-ttu-id="0576c-126">Tính năng tra cứu nguồn lực trong lưới **Lập kế hoạch nhiệm vụ** không lọc nguồn lực không hoạt động.</span><span class="sxs-lookup"><span data-stu-id="0576c-126">The **Task Planning** grid resource lookup does not filter inactive resources.</span></span>
- <span data-ttu-id="0576c-127">Chế độ thủ công không hoạt động như mong đợi trong cấu trúc phân tích công việc lập kế hoạch dự án.</span><span class="sxs-lookup"><span data-stu-id="0576c-127">Manual mode is not working as expected in the project planning work breakdown structure.</span></span>
- <span data-ttu-id="0576c-128">Lưới **Lập kế hoạch nhiệm vụ** hiển thị **Hạng mục giao dịch không hoạt động**.</span><span class="sxs-lookup"><span data-stu-id="0576c-128">The **Task Planning** grid shows **Inactive Transaction Categories**.</span></span>
- <span data-ttu-id="0576c-129">Lưới **Phân công nguồn lực** làm tròn không chính xác khi một nhiệm vụ có nhiều nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="0576c-129">The **Resource Assignment** grid rounds incorrectly when a task has multiple assignments.</span></span>
- <span data-ttu-id="0576c-130">Các giá trị làm tròn khác nhau giữa chi phí theo kế hoạch và chi phí thực tế cho một nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="0576c-130">Rounding values are different between planned cost and actual cost for a single task.</span></span>

<span data-ttu-id="0576c-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="0576c-131">**Sales**</span></span>

<span data-ttu-id="0576c-132">Các vấn đề sau đã được khắc phục:</span><span class="sxs-lookup"><span data-stu-id="0576c-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="0576c-133">**Tìm nạp tất cả các hạng mục giao dịch** nhấp đúp để tạo nhiều dòng.</span><span class="sxs-lookup"><span data-stu-id="0576c-133">**Fetch All Transaction Categories** double-click creates multiple lines.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]