---
title: Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 21, V3
description: Chủ đề này liệt kê các tính năng và bản sửa lỗi có trong Bản phát hành cập nhật Project Service Automation 21, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: dd894f27baac70238d0bd9e9b1a21a9a499e1ea7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002353"
---
# <a name="project-service-automation-update-release-21-v3"></a><span data-ttu-id="5700e-103">Phát hành bản cập nhật Project Service Automation 21, V3</span><span class="sxs-lookup"><span data-stu-id="5700e-103">Project Service Automation Update Release 21, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="5700e-104">Chúng tôi vui mừng thông báo bản cập nhật mới nhất dành cho ứng dụng Project Service Automation của Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="5700e-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="5700e-105">Bản phát hành này bao gồm một số cải tiến quan trọng về chất lượng, hiệu suất và khả năng sử dụng.</span><span class="sxs-lookup"><span data-stu-id="5700e-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="5700e-106">Bản phát hành này tương thích với Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="5700e-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="5700e-107">Để cập nhật lên bản phát hành này, hãy truy cập vào Trung tâm quản trị cho trang giải pháp trực tuyến Dynamics 365 để cài đặt bản cập nhật.</span><span class="sxs-lookup"><span data-stu-id="5700e-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="5700e-108">Để biết thêm thông tin, hãy xem [Cài đặt, cập nhật hoặc xóa giải pháp ưu tiên](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="5700e-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="5700e-109">Chủ đề này liệt kê các tính năng và bản sửa lỗi mới hoặc đã thay đổi cho Project Service Automation V3, Bản phát hành cập nhật 21.</span><span class="sxs-lookup"><span data-stu-id="5700e-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 21.</span></span> <span data-ttu-id="5700e-110">Phiên bản này có số bản dựng là V 3.10.32.50 và thường được cung cấp thông qua bản tự cập nhật vào tháng 6 năm 2020.</span><span class="sxs-lookup"><span data-stu-id="5700e-110">This version has a build number of V 3.10.32.50 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-21"></a><span data-ttu-id="5700e-111">Phát hành bản cập nhật 21</span><span class="sxs-lookup"><span data-stu-id="5700e-111">Update Release 21</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="5700e-112">Sửa lỗi</span><span class="sxs-lookup"><span data-stu-id="5700e-112">Bug fixes</span></span>

<span data-ttu-id="5700e-113">**Thời gian và Chi phí**</span><span class="sxs-lookup"><span data-stu-id="5700e-113">**Time and Expense**</span></span>

<span data-ttu-id="5700e-114">Các vấn đề sau đã được khắc phục:</span><span class="sxs-lookup"><span data-stu-id="5700e-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="5700e-115">Khi lưu trữ **Kiểm soát lưới mục nhập thời gian** trong Bảng điều khiển, lưới này không sử dụng toàn bộ chiều rộng của vùng chứa lưới bảng điều khiển.</span><span class="sxs-lookup"><span data-stu-id="5700e-115">When hosting the **Time Entry Grid Control** in Dashboards, the grid does not utilize the full width of the dashboard grid container.</span></span>
- <span data-ttu-id="5700e-116">Đối với các múi giờ cụ thể, kiểm soát lưới **Mục nhập Thời gian** không hiển thị bản ghi.</span><span class="sxs-lookup"><span data-stu-id="5700e-116">For specific time zones, the **Time Entry** grid control does not display records.</span></span>
- <span data-ttu-id="5700e-117">Các mục thời gian sau 21:00 sẽ hiển thị không đúng ngày.</span><span class="sxs-lookup"><span data-stu-id="5700e-117">Time entries that are after 9:00 PM appear on the wrong day.</span></span>
- <span data-ttu-id="5700e-118">Người dùng không thể gửi chi phí nếu loại chi phí **Yêu cầu biên nhận chi phí** không có giá trị.</span><span class="sxs-lookup"><span data-stu-id="5700e-118">Users are unable to submit expenses if the expense category, **Expense receipt required** has no value.</span></span>

<span data-ttu-id="5700e-119">**Quản lý nguồn lực**</span><span class="sxs-lookup"><span data-stu-id="5700e-119">**Resource Management**</span></span>

<span data-ttu-id="5700e-120">Các vấn đề sau đã được khắc phục:</span><span class="sxs-lookup"><span data-stu-id="5700e-120">The following issues have been fixed:</span></span>

- <span data-ttu-id="5700e-121">Các lượt đăng ký không hoạt động hiển thị ở dạng xem **Đối chiếu**.</span><span class="sxs-lookup"><span data-stu-id="5700e-121">Inactive bookings are displayed in the **Reconciliation** view.</span></span>
- <span data-ttu-id="5700e-122">Quá trình thực hiện nguồn lực chung thiếu thông tin xác thực để đảm bảo rằng có tồn tại trạng thái đăng ký hợp lệ.</span><span class="sxs-lookup"><span data-stu-id="5700e-122">Generic resource fulfillment was missing validation to ensure that a valid booking status exists.</span></span>

<span data-ttu-id="5700e-123">**Quản lý dự án**</span><span class="sxs-lookup"><span data-stu-id="5700e-123">**Project Management**</span></span>

<span data-ttu-id="5700e-124">Các vấn đề sau đã được khắc phục:</span><span class="sxs-lookup"><span data-stu-id="5700e-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="5700e-125">Lưới biểu mẫu **Dự án** (**Gán Nguồn lực**, **Nhiệm vụ**, dạng xem **Đối chiếu**, **Ước tính Chi phí**) vẫn có thể chỉnh sửa ngay cả khi dự án không hoạt động.</span><span class="sxs-lookup"><span data-stu-id="5700e-125">The **Project** form grids (**Resource Assignment**, **Task**, **Reconciliation** view, **Expense Estimates**) remain editable even when a project is not active.</span></span>
- <span data-ttu-id="5700e-126">Không thể hợp nhất các khách hàng trùng lặp với những khách hàng liên kết với hợp đồng dự án đã xác nhận.</span><span class="sxs-lookup"><span data-stu-id="5700e-126">Duplicate customers can't be merged with customers that are linked to confirmed project contracts.</span></span>
- <span data-ttu-id="5700e-127">Khi một nguồn lực không có lịch hợp lệ được thêm vào, hệ thống sẽ không trả về thông báo lỗi thân thiện với người dùng.</span><span class="sxs-lookup"><span data-stu-id="5700e-127">When a resource who does not have a valid calendar is added, the system does not return a user friendly-error message.</span></span>
- <span data-ttu-id="5700e-128">Nút **Thêm Nhiệm vụ** trên lưới nhiệm vụ được bật khi dự án liên kết với **Phần bổ trợ Microsoft Project**.</span><span class="sxs-lookup"><span data-stu-id="5700e-128">The **Add Task** button on the task grid is enabled when the project is linked to **Microsoft Project add-in**.</span></span>
- <span data-ttu-id="5700e-129">Nhân công tăng lên một cách không kiểm soát khi một nhiệm vụ có thể loại được giao cho một nguồn lực có vai trò được xác định giá vốn .</span><span class="sxs-lookup"><span data-stu-id="5700e-129">Effort grows uncontrollably when a task with a category is assigned to a resource with a role for which there is a cost price defined.</span></span>

<span data-ttu-id="5700e-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="5700e-130">**Sales**</span></span>

<span data-ttu-id="5700e-131">Chúng tôi đã thực hiện những cải tiến sau:</span><span class="sxs-lookup"><span data-stu-id="5700e-131">The following enhancements have been made:</span></span>

- <span data-ttu-id="5700e-132">**Tần suất Hóa đơn** và **Bắt đầu Thanh toán** đã được chuyển sang tab **Lập hóa đơn**.</span><span class="sxs-lookup"><span data-stu-id="5700e-132">**Invoice Frequency** and **Billing Start** have been moved to the **Invoice Schedule** tab.</span></span>

<span data-ttu-id="5700e-133">Các vấn đề sau đã được khắc phục:</span><span class="sxs-lookup"><span data-stu-id="5700e-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="5700e-134">**Tổng Giá bán** của **Thể loại** bằng không (0) mặc dù **Vai trò** có tổng giá bán khác 0.</span><span class="sxs-lookup"><span data-stu-id="5700e-134">**Total Sales Price** is zero (0) for **Category** even though **Role** has a total sales price that is not zero.</span></span>
- <span data-ttu-id="5700e-135">Khách hàng không thể thay đổi giá trị của trường **Trạng thái Hóa đơn** thành **Đã sẵn sàng để lập hóa đơn** khi một quy trình tùy chỉnh khác đang cập nhật một trường bổ sung.</span><span class="sxs-lookup"><span data-stu-id="5700e-135">Customers can't change the value of the **Invoice Status** field to **Ready for invoicing** when another customized process is updating an additional field.</span></span>
- <span data-ttu-id="5700e-136">Nút **Làm mới Thông tin Hóa đơn** có thể tạo nhiều dòng trùng lặp nếu được chọn nhiều lần.</span><span class="sxs-lookup"><span data-stu-id="5700e-136">The **Refresh Invoice Lines** button can create multiple duplicated lines if it is repeatedly selected.</span></span>
- <span data-ttu-id="5700e-137">Nút **Cập nhật giá** không hoạt động trên lưới con **Giá vai trò** trong biểu mẫu **Xem nhanh**.</span><span class="sxs-lookup"><span data-stu-id="5700e-137">The **Update Prices** button doesn't work on the **Role Prices** subgrid in the **Quick View** form.</span></span>
- <span data-ttu-id="5700e-138">Logic **Giải pháp Bảng giá Bán hàng** xử lý không đúng múi giờ, dẫn đến việc lựa chọn bảng giá không chính xác.</span><span class="sxs-lookup"><span data-stu-id="5700e-138">The **Sales Price List Resolution** logic improperly handles time zones, resulting in the incorrect selection of price lists.</span></span>
- <span data-ttu-id="5700e-139">**Tổng Chi phí Thực tế** của dự án có thể được giảm một phần nhỏ sau khi một mục nhập thời gian được chấp thuận.</span><span class="sxs-lookup"><span data-stu-id="5700e-139">A project’s **Total Actual Cost** can be off by a fractional amount after a single time entry is approved.</span></span>
- <span data-ttu-id="5700e-140">Logic **Giải pháp Giá bán** không trả về thông báo lỗi thân thiện với người dùng nếu **Giá Vai trò Đã truy xuất** không có giá trị trong trường **"Đơn vị Chính"** và **"Giá theo Đơn vị Chính"**.</span><span class="sxs-lookup"><span data-stu-id="5700e-140">The **Price Resolution** logic does not provide a user-friendly error message if **Retrieved RolePrice** doesn't have values in **'Primary Unit'** and **'Price In Primary Unit'** fields.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]