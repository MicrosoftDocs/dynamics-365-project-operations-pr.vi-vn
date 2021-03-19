---
title: Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 13, V3
description: Chủ đề này cung cấp thông tin về tính năng mới trong Phát hành bản cập nhật Project Service Automation 13, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: dbdcb811bfeacf17e841d679f097c591c16cd4c0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281054"
---
# <a name="project-service-automation-update-release-13-v3"></a><span data-ttu-id="a5a04-103">Phát hành bản cập nhật Project Service Automation 13, V3</span><span class="sxs-lookup"><span data-stu-id="a5a04-103">Project Service Automation Update Release 13, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="a5a04-104">Chúng tôi vui mừng thông báo bản cập nhật mới nhất cho ứng dụng Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="a5a04-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="a5a04-105">Bản phát hành này bao gồm một số cải tiến quan trọng về chất lượng, hiệu suất và khả năng sử dụng.</span><span class="sxs-lookup"><span data-stu-id="a5a04-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="a5a04-106">Bản phát hành này tương thích với Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="a5a04-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="a5a04-107">Để cập nhật lên bản phát hành này, hãy truy cập vào Trung tâm quản trị cho Dynamics 365 trực tuyến và truy cập vào trang giải pháp để cài đặt bản cập nhật.</span><span class="sxs-lookup"><span data-stu-id="a5a04-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="a5a04-108">Để biết thêm thông tin, hãy xem [Cài đặt, cập nhật hoặc xóa giải pháp ưu tiên](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="a5a04-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="a5a04-109">Chủ đề này liệt kê các tính năng và bản sửa lỗi mới hoặc đã thay đổi cho Project Service Automation V3, Bản phát hành cập nhật 13.</span><span class="sxs-lookup"><span data-stu-id="a5a04-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="a5a04-110">Phiên bản này có số bản dựng là V3.10.3.18 và có sẵn theo lịch trình sau:</span><span class="sxs-lookup"><span data-stu-id="a5a04-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="a5a04-111">**Tính sẵn có chung (tự cập nhật):** Tháng 11 năm 2019</span><span class="sxs-lookup"><span data-stu-id="a5a04-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="a5a04-112">**Tự động cập nhật:** Tháng 12 năm 2019</span><span class="sxs-lookup"><span data-stu-id="a5a04-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="a5a04-113">Phát hành bản cập nhật 13</span><span class="sxs-lookup"><span data-stu-id="a5a04-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="a5a04-114">Sửa lỗi</span><span class="sxs-lookup"><span data-stu-id="a5a04-114">Bug fixes</span></span>

- <span data-ttu-id="a5a04-115">Thời gian và Chi phí</span><span class="sxs-lookup"><span data-stu-id="a5a04-115">Time and Expense</span></span>

     - <span data-ttu-id="a5a04-116">Đã sửa lỗi: Chức năng tìm kiếm trên trang **Phê duyệt chi phí** không hoạt động khi tìm kiếm theo mục đích chi phí.</span><span class="sxs-lookup"><span data-stu-id="a5a04-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="a5a04-117">Quản lý nguồn lực</span><span class="sxs-lookup"><span data-stu-id="a5a04-117">Resource Management</span></span>

     - <span data-ttu-id="a5a04-118">Đã sửa lỗi: Các số trong phần điều hòa đã được cập nhật để được chứng minh là đúng.</span><span class="sxs-lookup"><span data-stu-id="a5a04-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="a5a04-119">Đã sửa lỗi: Không thể gán Nguồn lực được đặt tên cho các nhiệm vụ thông qua tab **Lịch trình**.</span><span class="sxs-lookup"><span data-stu-id="a5a04-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="a5a04-120">Quản lý dự án</span><span class="sxs-lookup"><span data-stu-id="a5a04-120">Project Management</span></span>

     - <span data-ttu-id="a5a04-121">Đã sửa lỗi: Ngoại lệ tham chiếu null khi gán thành viên nhóm khi **Loại giao dịch** thiếu thông tin thiết lập cho **Đơn vị** và **Nhóm mặc định**.</span><span class="sxs-lookup"><span data-stu-id="a5a04-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="a5a04-122">Sales</span><span class="sxs-lookup"><span data-stu-id="a5a04-122">Sales</span></span>

     - <span data-ttu-id="a5a04-123">Đã sửa lỗi: Bản ghi loại giao dịch trùng lặp trả về lỗi khi bản ghi giá vai trò được tạo.</span><span class="sxs-lookup"><span data-stu-id="a5a04-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="a5a04-124">Đã sửa: Các nút bổ sung cho **Cơ hội mới**, **Báo giá**, **Mô tả đơn hàng** và **Thêm sản phẩm** hiển thị trong các lệnh cho Cơ hội, Báo giá, Sản phẩm đặt hàng và lưới con Mô tả dựa trên dự án.</span><span class="sxs-lookup"><span data-stu-id="a5a04-124">Fixed: Extra buttons for **New Opportunity**, **Quote**, **Order Line**, and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines subgrid.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]