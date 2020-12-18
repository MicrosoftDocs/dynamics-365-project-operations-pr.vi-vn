---
title: Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 26, V3
ms.openlocfilehash: 849e7288ee91d3e9360c0b03f6b8b37ff29338e7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643289"
---
<a name="project-service-automation-update-release-26-v3"></a><span data-ttu-id="eecb9-102">Phát hành bản cập nhật Project Service Automation 26, V3</span><span class="sxs-lookup"><span data-stu-id="eecb9-102">Project Service Automation Update Release 26, V3</span></span>
================================================

<span data-ttu-id="eecb9-103">Chúng tôi vui mừng thông báo bản cập nhật mới nhất dành cho ứng dụng Project Service Automation của Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="eecb9-103">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="eecb9-104">Bản phát hành này bao gồm một số cải tiến quan trọng về chất lượng, hiệu suất và khả năng sử dụng.</span><span class="sxs-lookup"><span data-stu-id="eecb9-104">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="eecb9-105">Bản phát hành này tương thích với Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="eecb9-105">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="eecb9-106">Để cập nhật lên bản phát hành này, hãy truy cập vào Trung tâm quản trị cho trang giải pháp trực tuyến Dynamics 365 để cài đặt bản cập nhật.</span><span class="sxs-lookup"><span data-stu-id="eecb9-106">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="eecb9-107">Để biết thêm thông tin, hãy xem [Cài đặt, cập nhật hoặc xóa giải pháp ưu tiên](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="eecb9-107">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="eecb9-108">Chủ đề này liệt kê các tính năng và bản sửa lỗi mới hoặc đã thay đổi cho Project Service Automation, Bản phát hành cập nhật 26, V3.</span><span class="sxs-lookup"><span data-stu-id="eecb9-108">This topic lists the features and fixes that are new or changed for Project Service Automation Update Release 26, V3.</span></span> <span data-ttu-id="eecb9-109">Phiên bản này có mã số bản dựng là V3.10.44.59 và được phát hành rộng rãi thông qua bản tự cập nhật vào tháng 12 năm 2020.</span><span class="sxs-lookup"><span data-stu-id="eecb9-109">This version has a build number of V3.10.44.59 and is generally available through a self-update in December 2020.</span></span>

<a name="update-release-26"></a><span data-ttu-id="eecb9-110">Phát hành bản cập nhật 26</span><span class="sxs-lookup"><span data-stu-id="eecb9-110">Update Release 26</span></span>
-----------------

### <a name="bug-fixes"></a><span data-ttu-id="eecb9-111">Sửa lỗi</span><span class="sxs-lookup"><span data-stu-id="eecb9-111">Bug fixes</span></span>

<span data-ttu-id="eecb9-112">**Thời gian và Chi phí**</span><span class="sxs-lookup"><span data-stu-id="eecb9-112">**Time and Expense**</span></span>

<span data-ttu-id="eecb9-113">Các vấn đề sau đã được khắc phục:</span><span class="sxs-lookup"><span data-stu-id="eecb9-113">The following issues have been fixed:</span></span>

-   <span data-ttu-id="eecb9-114">Người dùng có thể thay đổi nhiệm vụ trên mục thời gian đã được phê duyệt/gửi.</span><span class="sxs-lookup"><span data-stu-id="eecb9-114">Users are able to change the task on a time entry that has been approved/submitted.</span></span>

-   <span data-ttu-id="eecb9-115">Lỗi "Chưa đặt tham chiếu đối tượng" khi lưu mục thời gian.</span><span class="sxs-lookup"><span data-stu-id="eecb9-115">"Object Reference Not Set" error when saving time entry.</span></span>

-   <span data-ttu-id="eecb9-116">Mục thời gian nhập từ các lần phân công nguồn lực sẽ tạo ra các mục thời gian có giá trị DateTime không chính xác.</span><span class="sxs-lookup"><span data-stu-id="eecb9-116">Time entry import from resource assignments creates time entries with the incorrect DateTime values.</span></span>

-   <span data-ttu-id="eecb9-117">Khi cài đặt cả ứng dụng Project Service Automation và Field Service, nút **Mới** hiển thị 2 lần trên thanh lệnh của các mục thời gian trong ứng dụng Field Service.</span><span class="sxs-lookup"><span data-stu-id="eecb9-117">When Project Service Automation and the Field Service app are both installed, the **New** button is displaying twice on the command bar for time entries in the Field Service app.</span></span>

-   <span data-ttu-id="eecb9-118">Điểm cập nhật ô **Cho phép đơn vị** và **Nhóm đơn vị** giờ đã có tác dụng trên lưới **Ước tính chi phí**.</span><span class="sxs-lookup"><span data-stu-id="eecb9-118">**Allow Unit** and **Unit group** cells updates now work on the **Expense Estimates** grid.</span></span>

-   <span data-ttu-id="eecb9-119">Biểu mẫu **Chỉnh sửa cập nhật mục thời gian** có chứa **Dòng thời gian**.</span><span class="sxs-lookup"><span data-stu-id="eecb9-119">**Update Time Entry Edit** form includes **Timeline**.</span></span>

-   <span data-ttu-id="eecb9-120">Việc phê duyệt thời gian đối với các mục thời gian không có trong dự án sẽ chặn hệ thống khi tìm kiếm vai trò người phê duyệt dự án.</span><span class="sxs-lookup"><span data-stu-id="eecb9-120">Time approval for non-project time entries blocks the system when searching for a project approver role.</span></span>

<span data-ttu-id="eecb9-121">**Quản lý nguồn lực**</span><span class="sxs-lookup"><span data-stu-id="eecb9-121">**Resource Management**</span></span>

<span data-ttu-id="eecb9-122">Các vấn đề sau đã được khắc phục:</span><span class="sxs-lookup"><span data-stu-id="eecb9-122">The following issues have been fixed:</span></span>

-   <span data-ttu-id="eecb9-123">Thêm quy trình xác thực trong phần bổ trợ **PostProjectCreate** để kiểm tra yêu cầu chính trước khi tạo.</span><span class="sxs-lookup"><span data-stu-id="eecb9-123">Added validation in the **PostProjectCreate** plug-in to check for a primary requirement before creating one.</span></span>

-   <span data-ttu-id="eecb9-124">Biểu mẫu tạo nhanh **Thành viên nhóm dự án** trả về ngoại lệ tham chiếu rỗng nếu các trường bị xóa khỏi biểu mẫu.</span><span class="sxs-lookup"><span data-stu-id="eecb9-124">**Project Team Member** quick create form throws a null reference exception if fields are removed from the form.</span></span>

-   <span data-ttu-id="eecb9-125">Tạo các yêu cầu trong 12 giờ thay vì 1 năm sẽ không thành công.</span><span class="sxs-lookup"><span data-stu-id="eecb9-125">Generate requirements for 12 hours over 1 year will fail.</span></span>

-   <span data-ttu-id="eecb9-126">Cải thiện thông báo lỗi ngoại lệ tham chiếu rỗng trong quá trình tạo yêu cầu nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="eecb9-126">Improved error message null reference exception during resource requirement creation.</span></span>

<span data-ttu-id="eecb9-127">**Quản lý dự án**</span><span class="sxs-lookup"><span data-stu-id="eecb9-127">**Project Management**</span></span>

<span data-ttu-id="eecb9-128">Các vấn đề sau đã được khắc phục:</span><span class="sxs-lookup"><span data-stu-id="eecb9-128">The following issues have been fixed:</span></span>

-   <span data-ttu-id="eecb9-129">Cải thiện chức năng xác thực để giải quyết ngoại lệ tham chiếu rỗng trong phần bổ trợ **PreProjectUpdate**.</span><span class="sxs-lookup"><span data-stu-id="eecb9-129">Improved validation to address null reference exception generated in the **PreProjectUpdate** plug-in.</span></span>

-   <span data-ttu-id="eecb9-130">Các dự án do phần bổ trợ của Microsoft Project trên máy tính sẽ xóa những lần phân công chưa giao.</span><span class="sxs-lookup"><span data-stu-id="eecb9-130">Projects published by the Microsoft Project desktop add-in delete unassigned assignments.</span></span>

-   <span data-ttu-id="eecb9-131">Thêm tùy chọn xác thực mới khi tham chiếu dự án của nhiệm vụ không hợp lệ do ngoại lệ tham chiếu rỗng trong phần bổ trợ **PreValidateProjectTaskUpdate**.</span><span class="sxs-lookup"><span data-stu-id="eecb9-131">Added new validation when a task’s project reference is invalid due to null reference exception in **PreValidateProjectTaskUpdate** plug-in.</span></span>

-   <span data-ttu-id="eecb9-132">Lưới Thành viên nhóm không hiển thị các lượt phần công riêng biệt trên bản ghi thành viên nhóm.</span><span class="sxs-lookup"><span data-stu-id="eecb9-132">Team Member grid does not show distinct assignments on the team member record.</span></span>

-   <span data-ttu-id="eecb9-133">Thêm tùy chọn xác thực và thông báo lỗi mới do ngoại lệ tham chiếu rỗng trong phần bổ trợ **PreProjectTaskDelete**.</span><span class="sxs-lookup"><span data-stu-id="eecb9-133">Added new validation and error messages due to null reference exception in **PreProjectTaskDelete** plug-in.</span></span>

<span data-ttu-id="eecb9-134">**Sales**</span><span class="sxs-lookup"><span data-stu-id="eecb9-134">**Sales**</span></span>

<span data-ttu-id="eecb9-135">Các vấn đề sau đã được khắc phục:</span><span class="sxs-lookup"><span data-stu-id="eecb9-135">The following issues have been fixed:</span></span>

-   <span data-ttu-id="eecb9-136">Khi chọn một dòng dựa trên dự án trong báo giá hoặc hợp đồng, nút **Gợi ý** chỉ hiển thị khi chọn một dòng dựa trên sản phẩm có liên kết với sản phẩm hiện tại.</span><span class="sxs-lookup"><span data-stu-id="eecb9-136">When selecting a project-based line in quote or contract, the **Suggestion** button should only be visible when selecting a product-based line associated with an existing product.</span></span>

-   <span data-ttu-id="eecb9-137">Tách quyền **Create_Product** khỏi quyền **Create_ProjectContract**.</span><span class="sxs-lookup"><span data-stu-id="eecb9-137">Split **Create_Product** privilege from **Create_ProjectContract** privilege.</span></span>

-   <span data-ttu-id="eecb9-138">Thao tác xóa dòng hóa đơn gây ra lỗi tham chiếu rỗng **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span><span class="sxs-lookup"><span data-stu-id="eecb9-138">Deleting an invoice line causes null reference failure on **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span></span>
