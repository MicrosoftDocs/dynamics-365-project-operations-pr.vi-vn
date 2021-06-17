---
title: Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 26, V3
description: Chủ đề này liệt kê các tính năng và bản sửa lỗi có trong Bản phát hành cập nhật Project Service Automation 26, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 6aafe66fe8c63dc886455a36e93f32d4a581d5cc
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005592"
---
# <a name="project-service-automation-update-release-26-v3"></a><span data-ttu-id="7658c-103">Phát hành bản cập nhật Project Service Automation 26, V3</span><span class="sxs-lookup"><span data-stu-id="7658c-103">Project Service Automation Update Release 26, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="7658c-104">Chúng tôi vui mừng thông báo bản cập nhật mới nhất dành cho ứng dụng Project Service Automation của Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="7658c-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="7658c-105">Bản phát hành này bao gồm một số cải tiến quan trọng về chất lượng, hiệu suất và khả năng sử dụng.</span><span class="sxs-lookup"><span data-stu-id="7658c-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="7658c-106">Bản phát hành này tương thích với Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="7658c-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="7658c-107">Để cập nhật lên bản phát hành này, hãy truy cập vào Trung tâm quản trị cho trang giải pháp trực tuyến Dynamics 365 để cài đặt bản cập nhật.</span><span class="sxs-lookup"><span data-stu-id="7658c-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="7658c-108">Để biết thêm thông tin, hãy xem [Cài đặt, cập nhật hoặc xóa giải pháp ưu tiên](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="7658c-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="7658c-109">Chủ đề này liệt kê các tính năng và bản sửa lỗi mới hoặc đã thay đổi cho Project Service Automation, Bản phát hành cập nhật 26, V3.</span><span class="sxs-lookup"><span data-stu-id="7658c-109">This topic lists the features and fixes that are new or changed for Project Service Automation Update Release 26, V3.</span></span> <span data-ttu-id="7658c-110">Phiên bản này có mã số bản dựng là V3.10.44.59 và được phát hành rộng rãi thông qua bản tự cập nhật vào tháng 12 năm 2020.</span><span class="sxs-lookup"><span data-stu-id="7658c-110">This version has a build number of V3.10.44.59 and is generally available through a self-update in December 2020.</span></span>

## <a name="update-release-26"></a><span data-ttu-id="7658c-111">Phát hành bản cập nhật 26</span><span class="sxs-lookup"><span data-stu-id="7658c-111">Update Release 26</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="7658c-112">Sửa lỗi</span><span class="sxs-lookup"><span data-stu-id="7658c-112">Bug fixes</span></span>

<span data-ttu-id="7658c-113">**Thời gian và Chi phí**</span><span class="sxs-lookup"><span data-stu-id="7658c-113">**Time and Expense**</span></span>

<span data-ttu-id="7658c-114">Các vấn đề sau đã được khắc phục:</span><span class="sxs-lookup"><span data-stu-id="7658c-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="7658c-115">Người dùng có thể thay đổi nhiệm vụ trên mục thời gian đã được phê duyệt/gửi.</span><span class="sxs-lookup"><span data-stu-id="7658c-115">Users are able to change the task on a time entry that has been approved/submitted.</span></span>
- <span data-ttu-id="7658c-116">Lỗi "Chưa đặt tham chiếu đối tượng" khi lưu mục thời gian.</span><span class="sxs-lookup"><span data-stu-id="7658c-116">"Object Reference Not Set" error when saving time entry.</span></span>
- <span data-ttu-id="7658c-117">Mục thời gian nhập từ các lần phân công nguồn lực sẽ tạo ra các mục thời gian có giá trị DateTime không chính xác.</span><span class="sxs-lookup"><span data-stu-id="7658c-117">Time entry import from resource assignments creates time entries with the incorrect DateTime values.</span></span>
- <span data-ttu-id="7658c-118">Khi cài đặt cả ứng dụng Project Service Automation và Field Service, nút **Mới** hiển thị 2 lần trên thanh lệnh của các mục thời gian trong ứng dụng Field Service.</span><span class="sxs-lookup"><span data-stu-id="7658c-118">When Project Service Automation and the Field Service app are both installed, the **New** button is displaying twice on the command bar for time entries in the Field Service app.</span></span>
- <span data-ttu-id="7658c-119">Điểm cập nhật ô **Cho phép đơn vị** và **Nhóm đơn vị** giờ đã có tác dụng trên lưới **Ước tính chi phí**.</span><span class="sxs-lookup"><span data-stu-id="7658c-119">**Allow Unit** and **Unit group** cells updates now work on the **Expense Estimates** grid.</span></span>
- <span data-ttu-id="7658c-120">Biểu mẫu **Chỉnh sửa cập nhật mục thời gian** có chứa **Dòng thời gian**.</span><span class="sxs-lookup"><span data-stu-id="7658c-120">**Update Time Entry Edit** form includes **Timeline**.</span></span>
- <span data-ttu-id="7658c-121">Việc phê duyệt thời gian đối với các mục thời gian không có trong dự án sẽ chặn hệ thống khi tìm kiếm vai trò người phê duyệt dự án.</span><span class="sxs-lookup"><span data-stu-id="7658c-121">Time approval for non-project time entries blocks the system when searching for a project approver role.</span></span>

<span data-ttu-id="7658c-122">**Quản lý nguồn lực**</span><span class="sxs-lookup"><span data-stu-id="7658c-122">**Resource Management**</span></span>

<span data-ttu-id="7658c-123">Các vấn đề sau đã được khắc phục:</span><span class="sxs-lookup"><span data-stu-id="7658c-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="7658c-124">Thêm quy trình xác thực trong phần bổ trợ **PostProjectCreate** để kiểm tra yêu cầu chính trước khi tạo.</span><span class="sxs-lookup"><span data-stu-id="7658c-124">Added validation in the **PostProjectCreate** plug-in to check for a primary requirement before creating one.</span></span>
- <span data-ttu-id="7658c-125">Biểu mẫu tạo nhanh **Thành viên nhóm dự án** trả về ngoại lệ tham chiếu rỗng nếu các trường bị xóa khỏi biểu mẫu.</span><span class="sxs-lookup"><span data-stu-id="7658c-125">**Project Team Member** quick create form throws a null reference exception if fields are removed from the form.</span></span>
- <span data-ttu-id="7658c-126">Tạo các yêu cầu trong 12 giờ thay vì 1 năm sẽ không thành công.</span><span class="sxs-lookup"><span data-stu-id="7658c-126">Generate requirements for 12 hours over 1 year will fail.</span></span>
- <span data-ttu-id="7658c-127">Cải thiện thông báo lỗi ngoại lệ tham chiếu rỗng trong quá trình tạo yêu cầu nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="7658c-127">Improved error message null reference exception during resource requirement creation.</span></span>

<span data-ttu-id="7658c-128">**Quản lý dự án**</span><span class="sxs-lookup"><span data-stu-id="7658c-128">**Project Management**</span></span>

<span data-ttu-id="7658c-129">Các vấn đề sau đã được khắc phục:</span><span class="sxs-lookup"><span data-stu-id="7658c-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="7658c-130">Cải thiện chức năng xác thực để giải quyết ngoại lệ tham chiếu rỗng trong phần bổ trợ **PreProjectUpdate**.</span><span class="sxs-lookup"><span data-stu-id="7658c-130">Improved validation to address null reference exception generated in the **PreProjectUpdate** plug-in.</span></span>
- <span data-ttu-id="7658c-131">Các dự án do phần bổ trợ của Microsoft Project trên máy tính sẽ xóa những lần phân công chưa giao.</span><span class="sxs-lookup"><span data-stu-id="7658c-131">Projects published by the Microsoft Project desktop add-in delete unassigned assignments.</span></span>
- <span data-ttu-id="7658c-132">Thêm tùy chọn xác thực mới khi tham chiếu dự án của nhiệm vụ không hợp lệ do ngoại lệ tham chiếu rỗng trong phần bổ trợ **PreValidateProjectTaskUpdate**.</span><span class="sxs-lookup"><span data-stu-id="7658c-132">Added new validation when a task’s project reference is invalid due to null reference exception in **PreValidateProjectTaskUpdate** plug-in.</span></span>
- <span data-ttu-id="7658c-133">Lưới Thành viên nhóm không hiển thị các lượt phần công riêng biệt trên bản ghi thành viên nhóm.</span><span class="sxs-lookup"><span data-stu-id="7658c-133">Team Member grid does not show distinct assignments on the team member record.</span></span>
- <span data-ttu-id="7658c-134">Thêm tùy chọn xác thực và thông báo lỗi mới do ngoại lệ tham chiếu rỗng trong phần bổ trợ **PreProjectTaskDelete**.</span><span class="sxs-lookup"><span data-stu-id="7658c-134">Added new validation and error messages due to null reference exception in **PreProjectTaskDelete** plug-in.</span></span>

<span data-ttu-id="7658c-135">**Sales**</span><span class="sxs-lookup"><span data-stu-id="7658c-135">**Sales**</span></span>

<span data-ttu-id="7658c-136">Các vấn đề sau đã được khắc phục:</span><span class="sxs-lookup"><span data-stu-id="7658c-136">The following issues have been fixed:</span></span>

- <span data-ttu-id="7658c-137">Khi chọn một dòng dựa trên dự án trong báo giá hoặc hợp đồng, nút **Gợi ý** chỉ hiển thị khi chọn một dòng dựa trên sản phẩm có liên kết với sản phẩm hiện tại.</span><span class="sxs-lookup"><span data-stu-id="7658c-137">When selecting a project-based line in quote or contract, the **Suggestion** button should only be visible when selecting a product-based line associated with an existing product.</span></span>
- <span data-ttu-id="7658c-138">Tách quyền **Create_Product** khỏi quyền **Create_ProjectContract**.</span><span class="sxs-lookup"><span data-stu-id="7658c-138">Split **Create_Product** privilege from **Create_ProjectContract** privilege.</span></span>
- <span data-ttu-id="7658c-139">Thao tác xóa dòng hóa đơn gây ra lỗi tham chiếu rỗng **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span><span class="sxs-lookup"><span data-stu-id="7658c-139">Deleting an invoice line causes null reference failure on **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]