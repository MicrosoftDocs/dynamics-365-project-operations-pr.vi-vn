---
title: Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 25, V3
description: Chủ đề này liệt kê các tính năng và bản sửa lỗi có trong Bản phát hành cập nhật Project Service Automation 25, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: aabee3fe755e33d2c0f01a96b6f53a68957bc041
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143807"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a><span data-ttu-id="308cc-103">Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 25, V3</span><span class="sxs-lookup"><span data-stu-id="308cc-103">What's new or changed in Project Service Automation Update Release 25, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="308cc-104">Chúng tôi vui mừng thông báo bản cập nhật mới nhất dành cho ứng dụng Project Service Automation của Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="308cc-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="308cc-105">Bản phát hành này bao gồm một số cải tiến quan trọng về chất lượng, hiệu suất và khả năng sử dụng.</span><span class="sxs-lookup"><span data-stu-id="308cc-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="308cc-106">Bản phát hành này tương thích với Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="308cc-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="308cc-107">Để cập nhật lên bản phát hành này, hãy truy cập vào Trung tâm quản trị cho trang giải pháp trực tuyến Dynamics 365 để cài đặt bản cập nhật.</span><span class="sxs-lookup"><span data-stu-id="308cc-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="308cc-108">Để biết thêm thông tin, hãy xem [Cài đặt, cập nhật hoặc xóa giải pháp ưu tiên](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="308cc-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="308cc-109">Chủ đề này liệt kê các tính năng và bản sửa lỗi mới hoặc đã thay đổi đối với Project Service Automation V3, Bản phát hành cập nhật 25. Phiên bản này có số bản dựng là 3.10.43.76 và thường được cung cấp đại trà thông qua bản tự cập nhật vào tháng 10 năm 2020.</span><span class="sxs-lookup"><span data-stu-id="308cc-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 25 This version has a build number of V 3.10.43.76 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-25"></a><span data-ttu-id="308cc-110">Phát hành bản cập nhật 25</span><span class="sxs-lookup"><span data-stu-id="308cc-110">Update Release 25</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="308cc-111">Sửa lỗi</span><span class="sxs-lookup"><span data-stu-id="308cc-111">Bug fixes</span></span>

<span data-ttu-id="308cc-112">**Thời gian và Chi phí**</span><span class="sxs-lookup"><span data-stu-id="308cc-112">**Time and Expense**</span></span>

<span data-ttu-id="308cc-113">Sự cố sau đây đã được khắc phục:</span><span class="sxs-lookup"><span data-stu-id="308cc-113">The following issue has been fixed:</span></span>

- <span data-ttu-id="308cc-114">Biểu đồ mục nhập thời gian hiển thị dữ liệu bổ sung dựa trên khoảng thời gian được truy xuất quá lớn.</span><span class="sxs-lookup"><span data-stu-id="308cc-114">Time entry chart showing additional data based on too large of an interval being retrieved.</span></span>

<span data-ttu-id="308cc-115">**Quản lý nguồn lực**</span><span class="sxs-lookup"><span data-stu-id="308cc-115">**Resource Management**</span></span>

<span data-ttu-id="308cc-116">Sự cố sau đây đã được khắc phục:</span><span class="sxs-lookup"><span data-stu-id="308cc-116">The following issue has been fixed:</span></span>

- <span data-ttu-id="308cc-117">Đã thêm mã package deployer để bỏ qua bước nhập bản vá Universal Resource Scheduling nếu bản vá phiên bản cao hơn đã tồn tại.</span><span class="sxs-lookup"><span data-stu-id="308cc-117">Added package deployer code to skip the Universal Resource Scheduling patch import if a higher version patch already exists.</span></span>

<span data-ttu-id="308cc-118">**Quản lý dự án**</span><span class="sxs-lookup"><span data-stu-id="308cc-118">**Project Management**</span></span>

<span data-ttu-id="308cc-119">Các vấn đề sau đã được khắc phục:</span><span class="sxs-lookup"><span data-stu-id="308cc-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="308cc-120">Sửa sự chênh lệch về làm tròn và tỷ giá hối đoái dẫn đến chi phí dự kiến không chính xác trong lưới theo dõi dự án.</span><span class="sxs-lookup"><span data-stu-id="308cc-120">Corrected rounding and exchange rate discrepancies resulting in incorrect planned cost in the project tracking grid.</span></span>
- <span data-ttu-id="308cc-121">Hỗ trợ khả năng hiển thị hai hoặc nhiều lưới phản ứng trên biểu mẫu **Dự án**.</span><span class="sxs-lookup"><span data-stu-id="308cc-121">Support the ability to display two or more react grids on the **Project** form.</span></span>
- <span data-ttu-id="308cc-122">Cung cấp tính năng xác thực để giải quyết khả năng chỉ định một nhiệm vụ quá ngày kết thúc theo lịch, dẫn đến việc chỉ định nguồn lực không thành công.</span><span class="sxs-lookup"><span data-stu-id="308cc-122">Provided validation to address the ability to assign a task past the calendar end date, which results in a failed resource assignment.</span></span>
- <span data-ttu-id="308cc-123">Cải thiện khả năng xử lý lỗi để giải quyết Ngoại lệ tham chiếu null được tạo ra từ các trường hợp sau:</span><span class="sxs-lookup"><span data-stu-id="308cc-123">Improved error handling to address Null Reference Exception generated from the following:</span></span>

    - <span data-ttu-id="308cc-124">Phần bổ trợ **PreValidateProjectTeamMemberCreate**</span><span class="sxs-lookup"><span data-stu-id="308cc-124">**PreValidateProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="308cc-125">**PreValidateProjectTaskCreate** khi một nhiệm vụ dự án được tạo mà không có một dự án được liên kết</span><span class="sxs-lookup"><span data-stu-id="308cc-125">**PreValidateProjectTaskCreate** when a project task is created without an associated project</span></span>
    - <span data-ttu-id="308cc-126">Phần bổ trợ **PreProjectTeamMemberCreate**</span><span class="sxs-lookup"><span data-stu-id="308cc-126">**PreProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="308cc-127">Phần bổ trợ **PostProjectTeamMemberDelete**</span><span class="sxs-lookup"><span data-stu-id="308cc-127">**PostProjectTeamMemberDelete** plug-in</span></span>
    - <span data-ttu-id="308cc-128">Phần bổ trợ **PreValidateProjectTaskDelete**</span><span class="sxs-lookup"><span data-stu-id="308cc-128">**PreValidateProjectTaskDelete** plug-in</span></span>

<span data-ttu-id="308cc-129">**Sales**</span><span class="sxs-lookup"><span data-stu-id="308cc-129">**Sales**</span></span>

<span data-ttu-id="308cc-130">Các vấn đề sau đã được khắc phục:</span><span class="sxs-lookup"><span data-stu-id="308cc-130">The following issues have been fixed:</span></span>

- <span data-ttu-id="308cc-131">Cải thiện khả năng xử lý lỗi để giải quyết các Ngoại lệ tham chiếu null được tạo ra từ **Copy Project: Estimates HelperResource Management**.</span><span class="sxs-lookup"><span data-stu-id="308cc-131">Improved error handling to address Null Reference Exceptions generated from **Copy Project: Estimates HelperResource Management**.</span></span>
- <span data-ttu-id="308cc-132">Mục **Chưa sẵn sàng để lập hóa đơn** trên mục **Tồn đọng thanh toán cho thời gian và vật tư** không xóa trạng thái thanh toán.</span><span class="sxs-lookup"><span data-stu-id="308cc-132">**Not ready to Invoice** on a **Time and Material Billing Backlog** doesn't clear the billing status.</span></span>
- <span data-ttu-id="308cc-133">Đã sửa nút **Giá** bị gắn nhãn sai trên tab **Giá vai trò** và **Mục trong danh mục**.</span><span class="sxs-lookup"><span data-stu-id="308cc-133">Corrected mislabeled **Prices** buttons on the **Role Price** and **Catalog Items** tab.</span></span>
