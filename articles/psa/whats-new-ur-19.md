---
title: Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 19, V3
description: Chủ đề này liệt kê các tính năng và bản sửa lỗi có trong Bản phát hành cập nhật Project Service Automation 19, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: e116bcbb8e9d184b7b894709c893aaf1dadefc2f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126869"
---
# <a name="project-service-automation-update-release-19-v3"></a><span data-ttu-id="6cfc5-103">Phát hành bản cập nhật Project Service Automation 19, V3</span><span class="sxs-lookup"><span data-stu-id="6cfc5-103">Project Service Automation Update Release 19, V3</span></span>

<span data-ttu-id="6cfc5-104">Chúng tôi vui mừng thông báo bản cập nhật mới nhất dành cho ứng dụng Project Service Automation của Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="6cfc5-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="6cfc5-105">Bản phát hành này bao gồm một số cải tiến quan trọng về chất lượng, hiệu suất và khả năng sử dụng.</span><span class="sxs-lookup"><span data-stu-id="6cfc5-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="6cfc5-106">Bản phát hành này tương thích với Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="6cfc5-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="6cfc5-107">Để cập nhật lên bản phát hành này, hãy truy cập vào Trung tâm quản trị cho trang giải pháp trực tuyến Dynamics 365 để cài đặt bản cập nhật.</span><span class="sxs-lookup"><span data-stu-id="6cfc5-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="6cfc5-108">Để biết thêm thông tin, hãy xem [Cài đặt, cập nhật hoặc xóa giải pháp ưu tiên](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="6cfc5-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="6cfc5-109">Chủ đề này liệt kê các tính năng và bản sửa lỗi mới hoặc đã thay đổi cho PSA V3, Bản phát hành cập nhật 19.</span><span class="sxs-lookup"><span data-stu-id="6cfc5-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 19.</span></span> <span data-ttu-id="6cfc5-110">Phiên bản này có số bản dựng là V3.10.30.41 và thường có sẵn thông qua bản tự cập nhật vào tháng 5 năm 2020.</span><span class="sxs-lookup"><span data-stu-id="6cfc5-110">This version has a build number of V3.10.30.41 and is generally available through a self-update in May 2020.</span></span>

## <a name="update-release-19"></a><span data-ttu-id="6cfc5-111">Phát hành bản cập nhật 19</span><span class="sxs-lookup"><span data-stu-id="6cfc5-111">Update Release 19</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="6cfc5-112">Sửa lỗi</span><span class="sxs-lookup"><span data-stu-id="6cfc5-112">Bug fixes</span></span>

<span data-ttu-id="6cfc5-113">**Thời gian và Chi phí**</span><span class="sxs-lookup"><span data-stu-id="6cfc5-113">**Time and Expense**</span></span>

<span data-ttu-id="6cfc5-114">Các vấn đề sau đã được khắc phục:</span><span class="sxs-lookup"><span data-stu-id="6cfc5-114">The following issues have been fixed:</span></span> 

- <span data-ttu-id="6cfc5-115">Lỗi xuất phát từ mục nhập thời gian hiển thị không chính xác.</span><span class="sxs-lookup"><span data-stu-id="6cfc5-115">Errors derived from time entry imports are not surfaced correctly.</span></span>
- <span data-ttu-id="6cfc5-116">Lưới mục nhập thời gian không hỗ trợ hành vi trường **Chỉ ngày**.</span><span class="sxs-lookup"><span data-stu-id="6cfc5-116">Time Entry Grid does not support **Date Only** field behavior.</span></span>
- <span data-ttu-id="6cfc5-117">Nguồn lực dự án không thể tạo ra một chi phí với một dự án.</span><span class="sxs-lookup"><span data-stu-id="6cfc5-117">Project Resources are unable to create an expense with a project.</span></span>

<span data-ttu-id="6cfc5-118">**Quản lý dự án**</span><span class="sxs-lookup"><span data-stu-id="6cfc5-118">**Project Management**</span></span>

<span data-ttu-id="6cfc5-119">Các vấn đề sau đã được khắc phục:</span><span class="sxs-lookup"><span data-stu-id="6cfc5-119">The following issues have been fixed:</span></span> 

-  <span data-ttu-id="6cfc5-120">Nhiệm vụ cháu gây ra ước tính nỗ lực không chính xác trong khi Tính toán hoàn thành (EAC).</span><span class="sxs-lookup"><span data-stu-id="6cfc5-120">Grandchild task causes an incorrect effort estimate during the Completion (EAC) Calculation.</span></span>

<span data-ttu-id="6cfc5-121">**Sales**</span><span class="sxs-lookup"><span data-stu-id="6cfc5-121">**Sales**</span></span>

<span data-ttu-id="6cfc5-122">Các vấn đề sau đã được khắc phục:</span><span class="sxs-lookup"><span data-stu-id="6cfc5-122">The following issues have been fixed:</span></span> 

- <span data-ttu-id="6cfc5-123">Hành động **Tính toán lại** không hoạt động với chi tiết mô tả hợp đồng chi phí hoặc chi tiết mô tả báo giá.</span><span class="sxs-lookup"><span data-stu-id="6cfc5-123">The **Recalculate** action does not work with expense contract line details or quote line details.</span></span>
- <span data-ttu-id="6cfc5-124">**Cập nhật giá** bị thiếu cho ước tính chi phí.</span><span class="sxs-lookup"><span data-stu-id="6cfc5-124">**Update Prices** is missing for expense estimates.</span></span>
-  <span data-ttu-id="6cfc5-125">Khách hàng không thể chọn lý do dẫn đến trạng thái hợp đồng tùy chỉnh từ trang **Hợp đồng dự án**.</span><span class="sxs-lookup"><span data-stu-id="6cfc5-125">Customers are unable to select custom contract status reasons from the **Project Contract** page.</span></span>
- <span data-ttu-id="6cfc5-126">Khách hàng trải nghiệm hiệu suất xuống cấp khi tạo một bảng giá tùy chỉnh từ một báo giá.</span><span class="sxs-lookup"><span data-stu-id="6cfc5-126">Customers experience degraded performance when creating a custom price list from a quote.</span></span>
- <span data-ttu-id="6cfc5-127">Trải nghiệm khách hàng không nhất quán với **đơn vị** mặc định trên các trang **Chi tiết mô tả báo giá** và **Chi tiết mô tả hợp đồng**.</span><span class="sxs-lookup"><span data-stu-id="6cfc5-127">Customers experience inconsistency with **unit** defaults on **Quote Line Details** and **Contract Line Details** pages.</span></span>
- <span data-ttu-id="6cfc5-128">Việc thêm các mục danh mục giao dịch không thể tính phí vào mô tả hợp đồng có thể tính phí sẽ không tôn trọng loại thanh toán **Không thể tính phí** của danh mục giao dịch.</span><span class="sxs-lookup"><span data-stu-id="6cfc5-128">Adding non-chargeable transaction category items to a chargeable contract line will not respect the **Non-chargeable** billing type of the transaction category.</span></span>
- <span data-ttu-id="6cfc5-129">Khách hàng không thể sử dụng các vai trò và danh mục mới được thêm trên các hợp đồng được tạo trước đó.</span><span class="sxs-lookup"><span data-stu-id="6cfc5-129">Customers can't use the newly added roles and category on previously created contracts.</span></span>
- <span data-ttu-id="6cfc5-130">Khách hàng trải nghiệm hiệu suất bị suy giảm Truy xuất không cần thiết trong PreValidateProjectTeamMemberUpdate.cs</span><span class="sxs-lookup"><span data-stu-id="6cfc5-130">Customers experience degraded performance Unnecessary retrieve in PreValidateProjectTeamMemberUpdate.cs</span></span>
- <span data-ttu-id="6cfc5-131">Vai trò được thiết lập là không thể tính phí trong danh sách **Danh mục nguồn lực** nên được thêm vào tab **Vai trò có thể tính phí** dưới dạng **Không thể tính phí** trên mô tả hợp đồng cho một dự án.</span><span class="sxs-lookup"><span data-stu-id="6cfc5-131">Roles set up as non-chargeable in the **Resource Categories** list should be added to the **Chargeable Roles** tab as **Non0chargeable** on the contract line for a project.</span></span>
- <span data-ttu-id="6cfc5-132">Khách hàng có thể gặp hiệu suất xuống cấp khi tạo dự án vì **GetBookableResourceIdFromUser** truy xuất tất cả các cột của nguồn lực có thể đặt trước thay vì chỉ truy xuất ID chính.</span><span class="sxs-lookup"><span data-stu-id="6cfc5-132">Customers may experience degraded performance when creating a project because **GetBookableResourceIdFromUser** retrieves all columns of bookable resources instead of just the primary ID.</span></span>
- <span data-ttu-id="6cfc5-133">Thực thể **Loại giao dịch** thiếu phần bổ trợ cập nhật xác thực trước để ngăn người dùng nhập **Đơn vị** và **Nhóm đơn vị** không hợp lệ cho các loại giao dịch.</span><span class="sxs-lookup"><span data-stu-id="6cfc5-133">**TransactionType** entity missing the pre-validation update plug-in to prevent users from entering **Units** and **UnitGroups** that are not valid for transaction types.</span></span>
- <span data-ttu-id="6cfc5-134">Bước **Loại bỏ** không hoạt động để nhập mục nhập thời gian.</span><span class="sxs-lookup"><span data-stu-id="6cfc5-134">The **Remove** step does not work for time entry import.</span></span>
