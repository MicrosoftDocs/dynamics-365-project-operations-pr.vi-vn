---
title: Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 22, V3
description: Chủ đề này liệt kê các tính năng và bản sửa lỗi có trong Bản phát hành cập nhật Project Service Automation 22, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: 389897c2604974a0bf7f221758dd03e1748ffeb5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280604"
---
# <a name="project-service-automation-update-release-22-v3"></a><span data-ttu-id="feca9-103">Phát hành bản cập nhật Project Service Automation 22, V3</span><span class="sxs-lookup"><span data-stu-id="feca9-103">Project Service Automation Update Release 22, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="feca9-104">Chúng tôi vui mừng thông báo bản cập nhật mới nhất dành cho ứng dụng Project Service Automation của Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="feca9-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="feca9-105">Bản phát hành này bao gồm một số cải tiến quan trọng về chất lượng, hiệu suất và khả năng sử dụng.</span><span class="sxs-lookup"><span data-stu-id="feca9-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="feca9-106">Bản phát hành này tương thích với Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="feca9-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="feca9-107">Để cập nhật lên bản phát hành này, hãy truy cập vào Trung tâm quản trị cho trang giải pháp trực tuyến Dynamics 365 để cài đặt bản cập nhật.</span><span class="sxs-lookup"><span data-stu-id="feca9-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="feca9-108">Để biết thêm thông tin, hãy xem [Cài đặt, cập nhật hoặc xóa giải pháp ưu tiên](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="feca9-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="feca9-109">Chủ đề này liệt kê các tính năng và bản sửa lỗi mới hoặc đã thay đổi cho Project Service Automation V3, Bản phát hành cập nhật 22.</span><span class="sxs-lookup"><span data-stu-id="feca9-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 22.</span></span> <span data-ttu-id="feca9-110">Phiên bản này có số bản dựng là V 3.10.33.48 và thường được cung cấp thông qua bản tự cập nhật vào tháng 6 năm 2020.</span><span class="sxs-lookup"><span data-stu-id="feca9-110">This version has a build number of V 3.10.33.48 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-22"></a><span data-ttu-id="feca9-111">Phát hành bản cập nhật 22</span><span class="sxs-lookup"><span data-stu-id="feca9-111">Update Release 22</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="feca9-112">Sửa lỗi</span><span class="sxs-lookup"><span data-stu-id="feca9-112">Bug fixes</span></span>



<span data-ttu-id="feca9-113">**Thời gian và Chi phí**</span><span class="sxs-lookup"><span data-stu-id="feca9-113">**Time and Expense**</span></span>

<span data-ttu-id="feca9-114">Các vấn đề sau đã được khắc phục:</span><span class="sxs-lookup"><span data-stu-id="feca9-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="feca9-115">**Mục nhập thời gian** không được tự động thêm vào Lịch trình thời gian sau khi nhập.</span><span class="sxs-lookup"><span data-stu-id="feca9-115">**Time entries** are not automatically added in the Time entries schedule after import.</span></span>
- <span data-ttu-id="feca9-116">Bộ chọn ngày dạng lưới **Mục nhập thời gian** không nhận dạng tùy chọn cài đặt theo khu vực của người dùng.</span><span class="sxs-lookup"><span data-stu-id="feca9-116">The **Time Entry** grid date picker does not recognize a user's regional settings.</span></span>

<span data-ttu-id="feca9-117">**Quản lý nguồn lực**</span><span class="sxs-lookup"><span data-stu-id="feca9-117">**Resource Management**</span></span>

<span data-ttu-id="feca9-118">Các vấn đề sau đã được khắc phục:</span><span class="sxs-lookup"><span data-stu-id="feca9-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="feca9-119">Ở chế độ thủ công, những thay đổi đối với sự phân phối giờ làm việc **Gán Nguồn lực** không được nhận dạng khi tạo **Yêu cầu về Nguồn lực**.</span><span class="sxs-lookup"><span data-stu-id="feca9-119">In manual mode, changes to **Resource Assignment** contours are not recognized when generating **Resource Requirements**.</span></span>
- <span data-ttu-id="feca9-120">**Yêu cầu về Nguồn lực** không hỗ trợ các trạng thái yêu cầu tùy chỉnh.</span><span class="sxs-lookup"><span data-stu-id="feca9-120">**Resource Requests** do not support custom request statuses.</span></span>

<span data-ttu-id="feca9-121">**Quản lý dự án**</span><span class="sxs-lookup"><span data-stu-id="feca9-121">**Project Management**</span></span>

<span data-ttu-id="feca9-122">Các vấn đề sau đã được khắc phục:</span><span class="sxs-lookup"><span data-stu-id="feca9-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="feca9-123">Việc nhấp đúp vào EstimateGridControl sẽ không phân tích cú pháp chính xác các định dạng số của Hà Lan.</span><span class="sxs-lookup"><span data-stu-id="feca9-123">Using double-click on EstimateGridControl will not correctly parse Dutch format numbers.</span></span>
- <span data-ttu-id="feca9-124">Các giờ đã gán không cập nhật chính xác khi nhiệm vụ được thay đổi bằng phần bổ trợ của máy khách Microsoft Project.</span><span class="sxs-lookup"><span data-stu-id="feca9-124">Assigned hours do not update correctly when assignments are changed using the Microsoft Project desktop client add-in.</span></span>
- <span data-ttu-id="feca9-125">Lưới Theo dõi Dự án và Ước tính hiển thị không chính xác mã đơn vị tiền tệ bán hàng khi đơn vị tiền tệ trong hợp đồng khác với đơn vị tiền tệ của khách hàng và tổ chức được định cấu hình để hiển thị mã đơn vị tiền tệ thay vì ký hiệu tiền tệ.</span><span class="sxs-lookup"><span data-stu-id="feca9-125">Project Tracking and Estimates grids display incorrect sales currency code when contract currency is different than customer currency and organization is configured to display currency codes instead of currency symbols.</span></span>
- <span data-ttu-id="feca9-126">Ngày kết thúc của thành viên Nhóm sẽ được bổ sung thêm 1 ngày nếu lịch làm việc là 24 giờ mỗi ngày.</span><span class="sxs-lookup"><span data-stu-id="feca9-126">A Team member's finish date will add one day if the work hour schedule is 24-hours per day.</span></span>
- <span data-ttu-id="feca9-127">Trên Lịch trình Dự án, việc thêm Danh mục Giao dịch vào nhiệm vụ không kích hoạt tính năng lưu tự động.</span><span class="sxs-lookup"><span data-stu-id="feca9-127">On the Project Schedule, adding a Transaction Category to a task does not trigger auto save.</span></span>
- <span data-ttu-id="feca9-128">Lỗi sau sẽ xuất hiện khi thêm một thành viên nhóm vào Mẫu Dự án: "Không thể liên kết các yêu cầu về nguồn lực với mẫu dự án".</span><span class="sxs-lookup"><span data-stu-id="feca9-128">The following error is displayed when adding a team member to the Project Template: "Resource requirements cannot be associated with project templates".</span></span> 
- <span data-ttu-id="feca9-129">Tập lệnh quy tắc ruy băng "msdyn.Approval.CanApproveOrReject" hiển thị lỗi hết thời gian chờ.</span><span class="sxs-lookup"><span data-stu-id="feca9-129">Ribbon rule script "msdyn.Approval.CanApproveOrReject" displays a timeout error.</span></span>

<span data-ttu-id="feca9-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="feca9-130">**Sales**</span></span>

<span data-ttu-id="feca9-131">Các vấn đề sau đã được khắc phục:</span><span class="sxs-lookup"><span data-stu-id="feca9-131">The following issues have been fixed:</span></span>

- <span data-ttu-id="feca9-132">Thông báo lỗi xác thực không hiển thị khi một Hạng mục trong Bảng Giá được chọn khi tra cứu Bảng Giá trên biểu mẫu/thực thể "Bảng Giá Dự án Báo giá Mới".</span><span class="sxs-lookup"><span data-stu-id="feca9-132">Validation error message not displayed when a Cost Price List is selected in Price List lookup on 'New Quote Project Price List' form/entity.</span></span>
- <span data-ttu-id="feca9-133">Việc đóng báo giá ở trạng thái thành công sẽ không chuyển đến hợp đồng đã tạo nếu BPF đính kèm với báo giá đang ở giai đoạn cuối cùng.</span><span class="sxs-lookup"><span data-stu-id="feca9-133">Closing the quote as won does not navigate to the created contract if a BPF attached to the quote is in the final stage.</span></span>
- <span data-ttu-id="feca9-134">**Bán hàng Chưa lập hóa đơn** đảo ngược được liên kết với chi phí ban đầu khi mục nhập thời gian được thu hồi.</span><span class="sxs-lookup"><span data-stu-id="feca9-134">Reversing **Unbilled Sales** is linked to original cost when a time entry is recalled.</span></span>
- <span data-ttu-id="feca9-135">Sau khi chọn nút **Xác nhận**, trạng thái hóa đơn chỉ thay đổi thành **Đã xác nhận** khi hóa đơn được làm mới.</span><span class="sxs-lookup"><span data-stu-id="feca9-135">After selecting the **Confirm** button, the invoice status doesn't change to **Confirmed** unless the invoice is refreshed.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]