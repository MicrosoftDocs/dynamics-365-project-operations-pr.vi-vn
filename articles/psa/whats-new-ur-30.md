---
title: Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 30, V3
description: Chủ đề này liệt kê các tính năng và bản sửa lỗi có trong Bản phát hành cập nhật Project Service Automation 30, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 1169ee13c42e982cb30a40d92df660f8933786a9
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852907"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a><span data-ttu-id="70140-103">Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 30, V3</span><span class="sxs-lookup"><span data-stu-id="70140-103">What's new or changed in Project Service Automation Update Release 30, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="70140-104">Chúng tôi vui mừng thông báo bản cập nhật mới nhất dành cho ứng dụng Project Service Automation của Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="70140-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="70140-105">Bản phát hành này bao gồm một số cải tiến quan trọng về chất lượng, hiệu suất và khả năng sử dụng.</span><span class="sxs-lookup"><span data-stu-id="70140-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="70140-106">Bản phát hành này tương thích với Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="70140-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="70140-107">Để cập nhật lên bản phát hành này, hãy truy cập vào Trung tâm quản trị cho trang giải pháp trực tuyến Dynamics 365 để cài đặt bản cập nhật.</span><span class="sxs-lookup"><span data-stu-id="70140-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="70140-108">Để biết thêm thông tin, hãy xem [Cài đặt, cập nhật hoặc xóa giải pháp ưu tiên](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="70140-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="70140-109">Chủ đề này liệt kê các tính năng và bản sửa lỗi mới hoặc đã thay đổi cho Project Service Automation V3, Bản phát hành cập nhật 30.</span><span class="sxs-lookup"><span data-stu-id="70140-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 30.</span></span> <span data-ttu-id="70140-110">Phiên bản này có số bản dựng là V3.10.51.61 và thường có sẵn thông qua bản tự cập nhật vào tháng 4 năm 2021.</span><span class="sxs-lookup"><span data-stu-id="70140-110">This version has a build number of V3.10.51.61 and is generally available through a self-update in April 2021.</span></span>

## <a name="update-release-30"></a><span data-ttu-id="70140-111">Phát hành bản cập nhật 30</span><span class="sxs-lookup"><span data-stu-id="70140-111">Update Release 30</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="70140-112">Sửa lỗi</span><span class="sxs-lookup"><span data-stu-id="70140-112">Bug fixes</span></span>

<span data-ttu-id="70140-113">**Thời gian và Chi phí**</span><span class="sxs-lookup"><span data-stu-id="70140-113">**Time and Expense**</span></span>

<span data-ttu-id="70140-114">Các vấn đề sau đã được khắc phục:</span><span class="sxs-lookup"><span data-stu-id="70140-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="70140-115">Đã xảy ra lỗi khi bạn tạo và lưu mục nhập thời gian trên trang **Tạo nhanh** nếu trường **Vai trò** bị xóa.</span><span class="sxs-lookup"><span data-stu-id="70140-115">An error occurs when you create and save a time entry on the **Quick Create** page if the **Role** field is removed.</span></span>
- <span data-ttu-id="70140-116">Bộ lọc Mục nhập thời gian áp dụng sai toán tử bộ lọc.</span><span class="sxs-lookup"><span data-stu-id="70140-116">The Time Entry filter applies the wrong filter operator.</span></span>
- <span data-ttu-id="70140-117">Bảng chấm công đã sao chép không tự động hiển thị khi bạn chọn **Sao chép tuần** khi kiểm soát mục nhập thời gian.</span><span class="sxs-lookup"><span data-stu-id="70140-117">Copied timesheets aren't automatically displayed when you select **Copy Week** on the time entry control.</span></span>

<span data-ttu-id="70140-118">**Quản lý nguồn lực**</span><span class="sxs-lookup"><span data-stu-id="70140-118">**Resource Management**</span></span>

<span data-ttu-id="70140-119">Các vấn đề sau đã được khắc phục:</span><span class="sxs-lookup"><span data-stu-id="70140-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="70140-120">Khi bạn gia hạn đặt chỗ, trạng thái đặt chỗ được chỉ định cho loại hình đặt chỗ cứng là không chính xác.</span><span class="sxs-lookup"><span data-stu-id="70140-120">When you extend a booking, the booking status assigned to the hard booking is incorrect.</span></span> <span data-ttu-id="70140-121">Việc gia hạn đặt chỗ dựa trên trạng thái đặt chỗ được xác định là **Đã cam kết** trong siêu dữ liệu thiết lập đặt chỗ.</span><span class="sxs-lookup"><span data-stu-id="70140-121">Extending a booking respects the booking status defined as **Committed** in the booking setup metadata.</span></span>
- <span data-ttu-id="70140-122">Khi bạn không chỉ định trạng thái đặt chỗ hợp lệ, thông báo lỗi sẽ không được bản địa hóa một cách chính xác.</span><span class="sxs-lookup"><span data-stu-id="70140-122">When a valid booking status isn't specified, the error message is not correctly localized.</span></span>

<span data-ttu-id="70140-123">**Quản lý dự án**</span><span class="sxs-lookup"><span data-stu-id="70140-123">**Project Management**</span></span>

<span data-ttu-id="70140-124">Các vấn đề sau đã được khắc phục:</span><span class="sxs-lookup"><span data-stu-id="70140-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="70140-125">Không thể tạo dự án bằng một đơn vị tiền tệ và bao gồm các nhiệm vụ có liên quan bằng một đơn vị tiền tệ khác.</span><span class="sxs-lookup"><span data-stu-id="70140-125">Projects can't be created in one currency and include related tasks in another currency.</span></span>

<span data-ttu-id="70140-126">**Bán hàng**</span><span class="sxs-lookup"><span data-stu-id="70140-126">**Sales**</span></span>

<span data-ttu-id="70140-127">Các vấn đề sau đã được khắc phục:</span><span class="sxs-lookup"><span data-stu-id="70140-127">The following issues have been fixed:</span></span>

- <span data-ttu-id="70140-128">Khi bảng giá được sao chép, giá sẽ không được cập nhật.</span><span class="sxs-lookup"><span data-stu-id="70140-128">When a price list is copied, prices aren't updated.</span></span>
- <span data-ttu-id="70140-129">Việc chốt báo giá là thắng sẽ không thành công khi chi tiết chi phí có giá trị gốc.</span><span class="sxs-lookup"><span data-stu-id="70140-129">Closing a quote as won fails when the cost detail has a value for origin.</span></span>
- <span data-ttu-id="70140-130">Trên thực thể **Nhiệm vụ dự án**, **Chi phí ước tính** đã được đổi tên thành **Chi phí dự kiến (Cơ sở)**.</span><span class="sxs-lookup"><span data-stu-id="70140-130">On the **Project Task** entity, **Estimated Cost** has been renamed to **Planned Cost (Base)**.</span></span>
- <span data-ttu-id="70140-131">Một ngoại lệ tham chiếu rỗng được tạo ra khi các hóa đơn được tạo hoặc xóa.</span><span class="sxs-lookup"><span data-stu-id="70140-131">A null reference exception is generated when invoices are created or deleted.</span></span>
