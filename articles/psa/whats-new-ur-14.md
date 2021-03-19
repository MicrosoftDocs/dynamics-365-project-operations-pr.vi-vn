---
title: Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 14, V3
description: Chủ đề này cung cấp thông tin về tính năng mới trong Phát hành bản cập nhật Project Service Automation 14 V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
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
ms.openlocfilehash: e19c8ffe7d92ab7ec9eb46aff8f944c62b0bb4bc
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281009"
---
# <a name="project-service-automation-update-release-14-v3"></a><span data-ttu-id="00223-103">Phát hành bản cập nhật Project Service Automation 14, V3</span><span class="sxs-lookup"><span data-stu-id="00223-103">Project Service Automation Update Release 14, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="00223-104">Chúng tôi vui mừng thông báo bản cập nhật mới nhất cho ứng dụng Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="00223-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="00223-105">Bản phát hành này bao gồm một số cải tiến quan trọng về chất lượng, hiệu suất và khả năng sử dụng.</span><span class="sxs-lookup"><span data-stu-id="00223-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="00223-106">Bản phát hành này tương thích với Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="00223-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="00223-107">Để cập nhật lên bản phát hành này, hãy truy cập vào Trung tâm quản trị cho Dynamics 365 trực tuyến và truy cập vào trang giải pháp để cài đặt bản cập nhật.</span><span class="sxs-lookup"><span data-stu-id="00223-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="00223-108">Để biết thêm thông tin, hãy xem [Cài đặt, cập nhật hoặc xóa giải pháp ưu tiên](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="00223-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="00223-109">Chủ đề này liệt kê các tính năng và bản sửa lỗi mới hoặc đã thay đổi cho PSA V3, Bản phát hành cập nhật 14.</span><span class="sxs-lookup"><span data-stu-id="00223-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 14.</span></span> <span data-ttu-id="00223-110">Phiên bản này có số bản dựng là V3.10.4.21 và có sẵn theo lịch trình sau:</span><span class="sxs-lookup"><span data-stu-id="00223-110">This version has a build number of V3.10.4.21 and is available on the following schedule:</span></span>

- <span data-ttu-id="00223-111">**Tính sẵn có chung (tự cập nhật):** Tháng 1 năm 2020</span><span class="sxs-lookup"><span data-stu-id="00223-111">**General availability (self-update):** January 2020</span></span>
- <span data-ttu-id="00223-112">**Cập nhật tự động:** Tháng 2 năm 2020</span><span class="sxs-lookup"><span data-stu-id="00223-112">**Auto-update:** February 2020</span></span>

## <a name="update-release-14"></a><span data-ttu-id="00223-113">Phát hành bản cập nhật 14</span><span class="sxs-lookup"><span data-stu-id="00223-113">Update Release 14</span></span>

### <a name="enhancements"></a><span data-ttu-id="00223-114">Cải tiến</span><span class="sxs-lookup"><span data-stu-id="00223-114">Enhancements</span></span>

- <span data-ttu-id="00223-115">Sales</span><span class="sxs-lookup"><span data-stu-id="00223-115">Sales</span></span>

     - <span data-ttu-id="00223-116">Các giá trị của trường tùy chỉnh từ **Chi tiết mô tả báo giá** được sao chép sang **Chi tiết mô tả hợp đồng dự án** khi báo giá được cập nhật thành **Đóng dưới dạng thắng**.</span><span class="sxs-lookup"><span data-stu-id="00223-116">Custom field values from **Quote Line Details** are copied to **Project Contract Line Details** when a quote is updated to **Closed as won**.</span></span>
     - <span data-ttu-id="00223-117">Có thể **Đóng dưới dạng thua** các dự án đã xác nhận.</span><span class="sxs-lookup"><span data-stu-id="00223-117">Confirmed projects can be **Closed as lost**.</span></span>

- <span data-ttu-id="00223-118">Quản lý nguồn lực</span><span class="sxs-lookup"><span data-stu-id="00223-118">Resource Management</span></span>

     - <span data-ttu-id="00223-119">Khi gia hạn đặt trước, người dùng sẽ được nhắc với hộp thoại xác nhận để tóm tắt kết quả đặt trước và cung cấp liên kết để Duy trì đặt trước.</span><span class="sxs-lookup"><span data-stu-id="00223-119">When extending bookings, users will be prompted with a confirmation dialog box to summarize booking results and provide a link to Maintain Bookings.</span></span>


### <a name="bug-fixes"></a><span data-ttu-id="00223-120">Sửa lỗi</span><span class="sxs-lookup"><span data-stu-id="00223-120">Bug fixes</span></span>

- <span data-ttu-id="00223-121">Thời gian và Chi phí</span><span class="sxs-lookup"><span data-stu-id="00223-121">Time and Expense</span></span>

     - <span data-ttu-id="00223-122">Đã sửa lỗi: Cải thiện trải nghiệm người dùng khi người dùng chưa chọn bất kỳ mục nhập nào cần sửa.</span><span class="sxs-lookup"><span data-stu-id="00223-122">Fixed: Improved the user experience when the user has not selected any entries to be corrected.</span></span>

- <span data-ttu-id="00223-123">Quản lý nguồn lực</span><span class="sxs-lookup"><span data-stu-id="00223-123">Resource Management</span></span>

     - <span data-ttu-id="00223-124">Đã sửa lỗi: Đặt trước một nguồn lực nhiều lần vượt quá tên của nguồn lực có thể đặt được.</span><span class="sxs-lookup"><span data-stu-id="00223-124">Fixed: Booking a resource multiple times overflows the name of the bookable resource.</span></span>

- <span data-ttu-id="00223-125">Sales</span><span class="sxs-lookup"><span data-stu-id="00223-125">Sales</span></span>

     - <span data-ttu-id="00223-126">Đã sửa lỗi: Tổng giá bán không được tính cho đến khi người dùng cũng nhập giá vốn cho ước tính chi phí cho một dự án.</span><span class="sxs-lookup"><span data-stu-id="00223-126">Fixed: The total sales price is not calculated until the user also inputs a cost price for expense estimates on a project.</span></span>
     - <span data-ttu-id="00223-127">Đã sửa lỗi: Việc đóng một báo giá là **Thắng** không thành công nếu hợp đồng dự án được liên kết không ở trạng thái **Bản nháp**.</span><span class="sxs-lookup"><span data-stu-id="00223-127">Fixed: Closing a quote as **Won** fails if the associated project contract is not in a **Draft** state.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]