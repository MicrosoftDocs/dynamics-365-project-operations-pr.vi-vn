---
title: Tính năng mới trong Phát hành bản cập nhật Project Service Automation 14, V3
description: Chủ đề này cung cấp thông tin về tính năng mới trong Phát hành bản cập nhật Project Service Automation 14 V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: c69eab3b-0bb9-4b52-b606-e8a96e893471
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 31134756a5f4bff3022fca7df8364c49217b9b55
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 03/24/2020
ms.locfileid: "3757054"
---
# <a name="project-service-automation-v3-update-release-14"></a><span data-ttu-id="173bc-103">Phát hành bản cập nhật Project Service Automation V3, 14</span><span class="sxs-lookup"><span data-stu-id="173bc-103">Project Service Automation V3, Update Release 14</span></span>
<span data-ttu-id="173bc-104">Chúng tôi vui mừng thông báo bản cập nhật mới nhất cho ứng dụng Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="173bc-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="173bc-105">Bản phát hành này bao gồm một số cải tiến quan trọng về chất lượng, hiệu suất và khả năng sử dụng.</span><span class="sxs-lookup"><span data-stu-id="173bc-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="173bc-106">Bản phát hành này tương thích với Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="173bc-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="173bc-107">Để cập nhật lên bản phát hành này, hãy truy cập vào Trung tâm quản trị cho Dynamics 365 trực tuyến và truy cập vào trang giải pháp để cài đặt bản cập nhật.</span><span class="sxs-lookup"><span data-stu-id="173bc-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="173bc-108">Để biết thêm thông tin, hãy xem [Cài đặt, cập nhật hoặc xóa giải pháp ưu tiên](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="173bc-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="173bc-109">Chủ đề này liệt kê các tính năng và bản sửa lỗi mới hoặc đã thay đổi cho PSA V3, Bản phát hành cập nhật 14.</span><span class="sxs-lookup"><span data-stu-id="173bc-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 14.</span></span> <span data-ttu-id="173bc-110">Phiên bản này có số bản dựng là V3.10.4.21 và có sẵn theo lịch trình sau:</span><span class="sxs-lookup"><span data-stu-id="173bc-110">This version has a build number of V3.10.4.21 and is available on the following schedule:</span></span>

- <span data-ttu-id="173bc-111">**Tính sẵn có chung (tự cập nhật):** Tháng 1 năm 2020</span><span class="sxs-lookup"><span data-stu-id="173bc-111">**General availability (self-update):** January 2020</span></span>
- <span data-ttu-id="173bc-112">**Cập nhật tự động:** Tháng 2 năm 2020</span><span class="sxs-lookup"><span data-stu-id="173bc-112">**Auto-update:** February 2020</span></span>

## <a name="update-release-14"></a><span data-ttu-id="173bc-113">Phát hành bản cập nhật 14</span><span class="sxs-lookup"><span data-stu-id="173bc-113">Update Release 14</span></span>

### <a name="enhancements"></a><span data-ttu-id="173bc-114">Cải tiến</span><span class="sxs-lookup"><span data-stu-id="173bc-114">Enhancements</span></span>

- <span data-ttu-id="173bc-115">Sales</span><span class="sxs-lookup"><span data-stu-id="173bc-115">Sales</span></span>

     - <span data-ttu-id="173bc-116">Các giá trị của trường tùy chỉnh từ **Chi tiết mô tả báo giá** được sao chép sang **Chi tiết mô tả hợp đồng dự án** khi báo giá được cập nhật thành **Đóng dưới dạng thắng**.</span><span class="sxs-lookup"><span data-stu-id="173bc-116">Custom field values from **Quote Line Details** are copied to **Project Contract Line Details** when a quote is updated to **Closed as won**.</span></span>
     - <span data-ttu-id="173bc-117">Có thể **Đóng dưới dạng thua** các dự án đã xác nhận.</span><span class="sxs-lookup"><span data-stu-id="173bc-117">Confirmed projects can be **Closed as lost**.</span></span>

- <span data-ttu-id="173bc-118">Quản lý nguồn lực</span><span class="sxs-lookup"><span data-stu-id="173bc-118">Resource Management</span></span>

     - <span data-ttu-id="173bc-119">Khi gia hạn đặt trước, người dùng sẽ được nhắc với hộp thoại xác nhận để tóm tắt kết quả đặt trước và cung cấp liên kết để Duy trì đặt trước.</span><span class="sxs-lookup"><span data-stu-id="173bc-119">When extending bookings, users will be prompted with a confirmation dialog box to summarize booking results and provide a link to Maintain Bookings.</span></span>


### <a name="bug-fixes"></a><span data-ttu-id="173bc-120">Sửa lỗi</span><span class="sxs-lookup"><span data-stu-id="173bc-120">Bug fixes</span></span>

- <span data-ttu-id="173bc-121">Thời gian và Chi phí</span><span class="sxs-lookup"><span data-stu-id="173bc-121">Time and Expense</span></span>

     - <span data-ttu-id="173bc-122">Đã sửa lỗi: Cải thiện trải nghiệm người dùng khi người dùng chưa chọn bất kỳ mục nhập nào cần sửa.</span><span class="sxs-lookup"><span data-stu-id="173bc-122">Fixed: Improved the user experience when the user has not selected any entries to be corrected.</span></span>

- <span data-ttu-id="173bc-123">Quản lý nguồn lực</span><span class="sxs-lookup"><span data-stu-id="173bc-123">Resource Management</span></span>

     - <span data-ttu-id="173bc-124">Đã sửa lỗi: Đặt trước một nguồn lực nhiều lần vượt quá tên của nguồn lực có thể đặt được.</span><span class="sxs-lookup"><span data-stu-id="173bc-124">Fixed: Booking a resource multiple times overflows the name of the bookable resource.</span></span>

- <span data-ttu-id="173bc-125">Sales</span><span class="sxs-lookup"><span data-stu-id="173bc-125">Sales</span></span>

     - <span data-ttu-id="173bc-126">Đã sửa lỗi: Tổng giá bán không được tính cho đến khi người dùng cũng nhập giá vốn cho ước tính chi phí cho một dự án.</span><span class="sxs-lookup"><span data-stu-id="173bc-126">Fixed: The total sales price is not calculated until the user also inputs a cost price for expense estimates on a project.</span></span>
     - <span data-ttu-id="173bc-127">Đã sửa lỗi: Việc đóng một báo giá là **Thắng** không thành công nếu hợp đồng dự án được liên kết không ở trạng thái **Bản nháp**.</span><span class="sxs-lookup"><span data-stu-id="173bc-127">Fixed: Closing a quote as **Won** fails if the associated project contract is not in a **Draft** state.</span></span>

