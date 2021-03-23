---
title: Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 24, V3
description: Chủ đề này liệt kê các tính năng và bản sửa lỗi có trong Bản phát hành cập nhật Project Service Automation 24, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: c789a65f1996d082410b3d8dd9e76e5065e708a2
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280514"
---
# <a name="project-service-automation-update-release-24-v3"></a><span data-ttu-id="1f00f-103">Phát hành bản cập nhật Project Service Automation 24, V3</span><span class="sxs-lookup"><span data-stu-id="1f00f-103">Project Service Automation Update Release 24, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="1f00f-104">Chúng tôi vui mừng thông báo bản cập nhật mới nhất dành cho ứng dụng Project Service Automation của Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="1f00f-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="1f00f-105">Bản phát hành này bao gồm một số cải tiến quan trọng về chất lượng, hiệu suất và khả năng sử dụng.</span><span class="sxs-lookup"><span data-stu-id="1f00f-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="1f00f-106">Bản phát hành này tương thích với Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="1f00f-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="1f00f-107">Để cập nhật lên bản phát hành này, hãy truy cập vào Trung tâm quản trị cho trang giải pháp trực tuyến Dynamics 365 để cài đặt bản cập nhật.</span><span class="sxs-lookup"><span data-stu-id="1f00f-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="1f00f-108">Để biết thêm thông tin, hãy xem [Cài đặt, cập nhật hoặc xóa giải pháp ưu tiên](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="1f00f-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="1f00f-109">Chủ đề này liệt kê các tính năng và bản sửa lỗi mới hoặc đã thay đổi cho Project Service Automation V3, Bản phát hành cập nhật 24.</span><span class="sxs-lookup"><span data-stu-id="1f00f-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 24.</span></span> <span data-ttu-id="1f00f-110">Phiên bản này có số bản dựng là V 3.10.42.43 và thường có sẵn thông qua bản tự cập nhật vào tháng 10 năm 2020.</span><span class="sxs-lookup"><span data-stu-id="1f00f-110">This version has a build number of V 3.10.42.43 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-24"></a><span data-ttu-id="1f00f-111">Phát hành bản cập nhật 24</span><span class="sxs-lookup"><span data-stu-id="1f00f-111">Update Release 24</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="1f00f-112">Sửa lỗi</span><span class="sxs-lookup"><span data-stu-id="1f00f-112">Bug fixes</span></span>

<span data-ttu-id="1f00f-113">**Sales**</span><span class="sxs-lookup"><span data-stu-id="1f00f-113">**Sales**</span></span>

<span data-ttu-id="1f00f-114">Các vấn đề sau đã được khắc phục:</span><span class="sxs-lookup"><span data-stu-id="1f00f-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="1f00f-115">Sự cố khi đặt bảng giá mặc định của sản phẩm.</span><span class="sxs-lookup"><span data-stu-id="1f00f-115">Problem while setting default price list of products.</span></span>
- <span data-ttu-id="1f00f-116">Hiệu suất giành được báo giá đang chậm do bản sao của bản ghi bảng giá và giá vai trò được nhúng.</span><span class="sxs-lookup"><span data-stu-id="1f00f-116">Performance of Quote win is slow due to the embedded price list and role price records copy.</span></span>
- <span data-ttu-id="1f00f-117">**Hợp đồng dự án/Trung tâm bán hàng** > **Hạng mục sản phẩm/Số lượng mô tả đơn hàng** được tự động làm tròn đến số nguyên gần nhất.</span><span class="sxs-lookup"><span data-stu-id="1f00f-117">**Project Contract/Sales Hub** > **Product Line Item/Order Line Quantity** is automatically rounded to the nearest integer.</span></span>
- <span data-ttu-id="1f00f-118">Nâng cao đặc quyền hệ thống khi đọc bảng giá.</span><span class="sxs-lookup"><span data-stu-id="1f00f-118">Elevate to system privileges when reading price lists.</span></span>
- <span data-ttu-id="1f00f-119">Sao chép các trường địa chỉ khách hàng **address1_freighttermscode** và **address1_shippingmethodcode** vào Báo giá/Đơn hàng.</span><span class="sxs-lookup"><span data-stu-id="1f00f-119">Copy customer address fields **address1_freighttermscode** and **address1_shippingmethodcode** to Quote/Order.</span></span> 


<span data-ttu-id="1f00f-120">**Thời gian và Chi phí**</span><span class="sxs-lookup"><span data-stu-id="1f00f-120">**Time and Expense**</span></span>

<span data-ttu-id="1f00f-121">Các vấn đề sau đã được khắc phục:</span><span class="sxs-lookup"><span data-stu-id="1f00f-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="1f00f-122">**Lưới mục nhập thời gian** không hỗ trợ hành vi thời gian **Chỉ ngày**.</span><span class="sxs-lookup"><span data-stu-id="1f00f-122">The **Time Entry Grid** doesn't support **Date Only** time behavior.</span></span>
- <span data-ttu-id="1f00f-123">**Mục nhập thời gian** không tự động làm mới.</span><span class="sxs-lookup"><span data-stu-id="1f00f-123">**Time Entry** is not refreshing automatically.</span></span> <span data-ttu-id="1f00f-124">Làm mới thủ công là bắt buộc.</span><span class="sxs-lookup"><span data-stu-id="1f00f-124">A manual refresh is required.</span></span>
- <span data-ttu-id="1f00f-125">Không thể nhập các mục nhập thời gian từ mục phân công khi có thời gian giải lao (0 giờ) trong mục phân công của nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="1f00f-125">Unable to import the time entries from an assignment when there is a break (0 hours) in a resource's assignments.</span></span>
- <span data-ttu-id="1f00f-126">Khi tạo mục nhập thời gian, hãy đặt thời gian bắt đầu giống như **msdyn_date**.</span><span class="sxs-lookup"><span data-stu-id="1f00f-126">When creating a time entry, set the start to the same as **msdyn_date**.</span></span>
- <span data-ttu-id="1f00f-127">Bật lại tính năng chỉnh sửa hàng loạt cho mục nhập thời gian.</span><span class="sxs-lookup"><span data-stu-id="1f00f-127">Re-enable bulk edit for time entry.</span></span>

<span data-ttu-id="1f00f-128">**Quản lý nguồn lực**</span><span class="sxs-lookup"><span data-stu-id="1f00f-128">**Resource Management**</span></span>

<span data-ttu-id="1f00f-129">Các vấn đề sau đã được khắc phục:</span><span class="sxs-lookup"><span data-stu-id="1f00f-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="1f00f-130">Việc cố gắng cập nhật trạng thái đặt trước giữa các ngày mà không có yêu cầu sẽ đưa ra ngoại lệ null-ref.</span><span class="sxs-lookup"><span data-stu-id="1f00f-130">Trying to update the status of an inter-day booking without a requirement will throw a null-ref exception.</span></span>
- <span data-ttu-id="1f00f-131">Lỗi khi tải **Dạng xem điều hòa**.</span><span class="sxs-lookup"><span data-stu-id="1f00f-131">Error loading the **Reconciliation View**.</span></span>


<span data-ttu-id="1f00f-132">**Quản lý dự án**</span><span class="sxs-lookup"><span data-stu-id="1f00f-132">**Project Management**</span></span>

<span data-ttu-id="1f00f-133">Các vấn đề sau đã được khắc phục:</span><span class="sxs-lookup"><span data-stu-id="1f00f-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="1f00f-134">Trong **Lịch trình dự án**, khi chuyển từ **Thủ công** sang **Tự động**, quá trình lưu tự động không hoàn thành.</span><span class="sxs-lookup"><span data-stu-id="1f00f-134">In the **Project Schedule**, when changing from **Manual** to **Auto**, auto save is not completing.</span></span>
- <span data-ttu-id="1f00f-135">Chí phí không được phép tính vào mức chênh lệch trên **Lưới theo dõi dự án**.</span><span class="sxs-lookup"><span data-stu-id="1f00f-135">Expense costs should not calculate toward variance on the **Project Tracking Grid**.</span></span>
- <span data-ttu-id="1f00f-136">Hành vi không nhất quán đối với cột **Thẻ ước tính** trong khi tải so với thay đổi loại **Thời gian - Giai đoạn**.</span><span class="sxs-lookup"><span data-stu-id="1f00f-136">Inconsistent behavior for **Estimates tag** columns during load versus changing the **Time-Phase** type.</span></span>
- <span data-ttu-id="1f00f-137">Chi phí thực tế của một dự án có thể không phản ánh tổng số từ **Thực tế**.</span><span class="sxs-lookup"><span data-stu-id="1f00f-137">The actual cost on a project may not reflect the totals from **Actuals**.</span></span>
- <span data-ttu-id="1f00f-138">**Ngày kết thúc ước tính** trên tab **Tóm tắt** không khớp với **Lịch trình WBS**.</span><span class="sxs-lookup"><span data-stu-id="1f00f-138">**Estimated Finish Date** on the **Summary** tab does not match the **WBS Schedule**.</span></span>
- <span data-ttu-id="1f00f-139">**Cập nhật giờ thực tế** trên phần nhô lề không hoạt động chính xác.</span><span class="sxs-lookup"><span data-stu-id="1f00f-139">**Update Actual Hours** on outdent does not work correctly.</span></span>
- <span data-ttu-id="1f00f-140">Người quản lý dự án bên ngoài **BU** gốc không thể tạo dự án.</span><span class="sxs-lookup"><span data-stu-id="1f00f-140">A Project manager outside of root **BU** can't create a project.</span></span>
- <span data-ttu-id="1f00f-141">Các thay đổi đối với nhiệm vụ hoặc thể loại trên **Ước tính chi phí** không tồn tại.</span><span class="sxs-lookup"><span data-stu-id="1f00f-141">Changes to task or category on **Expense Estimates** are not persisted.</span></span>
- <span data-ttu-id="1f00f-142">**Bản sao hợp đồng** sao chép lịch trình hóa đơn và trạng thái chạy.</span><span class="sxs-lookup"><span data-stu-id="1f00f-142">**Copy of contract** copies the invoice schedules and the run status.</span></span>
- <span data-ttu-id="1f00f-143">Nút **Làm mới giá trị thực tế** tính toán không chính xác các nhiệm vụ tóm tắt.</span><span class="sxs-lookup"><span data-stu-id="1f00f-143">**Refresh Actuals** button incorrectly calculates summary tasks.</span></span>
- <span data-ttu-id="1f00f-144">Phần bổ trợ Microsoft Project: Khắc phục lỗi tham chiếu rỗng nếu bất kỳ thành viên nào trong nhóm có đơn vị cung ứng nguồn lực trống.</span><span class="sxs-lookup"><span data-stu-id="1f00f-144">Microsoft Project Add-in: Fix null reference error if any team member has an empty resourcing unit.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]