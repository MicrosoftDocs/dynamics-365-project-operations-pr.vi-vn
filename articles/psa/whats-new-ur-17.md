---
title: Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 17, V3
description: Chủ đề này liệt kê các tính năng và bản sửa lỗi có trong Bản phát hành cập nhật Project Service Automation 17, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: 7ba685568692dafe117de42a71bb14d391cd7cc4
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087064"
---
# <a name="project-service-automation-update-release-17-v3"></a><span data-ttu-id="cfbee-103">Phát hành bản cập nhật Project Service Automation 17, V3</span><span class="sxs-lookup"><span data-stu-id="cfbee-103">Project Service Automation Update Release 17, V3</span></span>

<span data-ttu-id="cfbee-104">Chúng tôi vui mừng thông báo bản cập nhật mới nhất dành cho ứng dụng Project Service Automation của Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="cfbee-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="cfbee-105">Bản phát hành này bao gồm một số cải tiến quan trọng về chất lượng, hiệu suất và khả năng sử dụng.</span><span class="sxs-lookup"><span data-stu-id="cfbee-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="cfbee-106">Bản phát hành này tương thích với Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="cfbee-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="cfbee-107">Để cập nhật lên bản phát hành này, hãy truy cập vào Trung tâm quản trị cho Dynamics 365 trực tuyến, rồi chuyển đến trang giải pháp để cài đặt bản cập nhật.</span><span class="sxs-lookup"><span data-stu-id="cfbee-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="cfbee-108">Để biết thêm thông tin, hãy xem [Cài đặt, cập nhật hoặc xóa giải pháp ưu tiên](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="cfbee-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="cfbee-109">Chủ đề này liệt kê các tính năng và bản sửa lỗi mới hoặc đã thay đổi cho PSA V3, Bản phát hành cập nhật 17.</span><span class="sxs-lookup"><span data-stu-id="cfbee-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 17.</span></span> <span data-ttu-id="cfbee-110">Phiên bản này có số bản dựng là V3.10.6.34 và thường có sẵn thông qua bản tự cập nhật vào tháng 3 năm 2020.</span><span class="sxs-lookup"><span data-stu-id="cfbee-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in March 2020.</span></span>


## <a name="update-release-17"></a><span data-ttu-id="cfbee-111">Phát hành bản cập nhật 17</span><span class="sxs-lookup"><span data-stu-id="cfbee-111">Update Release 17</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="cfbee-112">Sửa lỗi</span><span class="sxs-lookup"><span data-stu-id="cfbee-112">Bug fixes</span></span>

<span data-ttu-id="cfbee-113">**Sự cố chung**</span><span class="sxs-lookup"><span data-stu-id="cfbee-113">**General**</span></span>

- <span data-ttu-id="cfbee-114">Sửa lỗi: Cập nhật Project Service Automation để thực thi giấy phép Thành viên Nhóm (Trung tâm Nguồn lực Dự án sẽ bao gồm siêu dữ liệu của gói Dịch vụ Thành viên Nhóm 3.x)</span><span class="sxs-lookup"><span data-stu-id="cfbee-114">Fixed: Update Project Service Automation to enforce Team Member licenses (Project Resource Hub will include Team Member Service plan metadata 3.x)</span></span>
 
<span data-ttu-id="cfbee-115">**Thời gian và Chi phí**</span><span class="sxs-lookup"><span data-stu-id="cfbee-115">**Time and Expense**</span></span>

- <span data-ttu-id="cfbee-116">Sửa lỗi: Không thể thay đổi ước tính chi phí từ giá khác không thành không (0).</span><span class="sxs-lookup"><span data-stu-id="cfbee-116">Fixed: It is not possible to change an expense estimate from a non-zero price to zero (0).</span></span> <span data-ttu-id="cfbee-117">Thay đổi sẽ bị bỏ qua.</span><span class="sxs-lookup"><span data-stu-id="cfbee-117">The change is ignored.</span></span>

<span data-ttu-id="cfbee-118">**Quản lý dự án**</span><span class="sxs-lookup"><span data-stu-id="cfbee-118">**Project Management**</span></span>

- <span data-ttu-id="cfbee-119">Sửa lỗi: Thêm bước kiểm tra giá trị rỗng cho tên vị trí của thành viên nhóm.</span><span class="sxs-lookup"><span data-stu-id="cfbee-119">Fixed: A check for null values has been added on a team member's position name.</span></span>
- <span data-ttu-id="cfbee-120">Sửa lỗi: trường **msdyn_userresourceid** trên thực thể **msdyn_resourceassignment** không dùng được nữa.</span><span class="sxs-lookup"><span data-stu-id="cfbee-120">Fixed: **msdyn_userresourceid** field on the **msdyn_resourceassignment** entity has been deprecated.</span></span>
- <span data-ttu-id="cfbee-121">Sửa lỗi: Bản nâng cấp từ 2.x lên 3.x giờ sẽ xử lý các đường cong nỗ lực trống về phân công nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="cfbee-121">Fixed: Upgrade from 2.x to 3.x now handles empty effort contours on task assignments.</span></span>

<span data-ttu-id="cfbee-122">**Sales**</span><span class="sxs-lookup"><span data-stu-id="cfbee-122">**Sales**</span></span>

- <span data-ttu-id="cfbee-123">Sửa lỗi: **Invoice.PreValidateInvoiceUpdate** giờ sẽ xử lý kịch bản về quá trình gán lại chủ sở hữu đúng cách.</span><span class="sxs-lookup"><span data-stu-id="cfbee-123">Fixed: **Invoice.PreValidateInvoiceUpdate** now handles the scenario of reassigning record owners properly.</span></span>
- <span data-ttu-id="cfbee-124">Sửa lỗi: Khi lớp giao dịch là **Thời gian** , thì không chỉnh sửa được **UnitGroup** đối với tất cả thực thể, bao gồm **QuoteLineDetails** , **JournalLine** , **InvoiceLineDetail** và **ContractLineDetails**.</span><span class="sxs-lookup"><span data-stu-id="cfbee-124">Fixed: When the transaction class is **Time** , **UnitGroup** is non-editable for all entities including, **QuoteLineDetails** , **JournalLine** , **InvoiceLineDetail** , and **ContractLineDetails**.</span></span> <span data-ttu-id="cfbee-125">Tuy nhiên, chỉ không chỉnh sửa được **Đơn vị** đối với **JournalLine** và **InvoiceLineDetails**.</span><span class="sxs-lookup"><span data-stu-id="cfbee-125">However, **Unit** is non-editable only for **JournalLine** and **InvoiceLineDetails**.</span></span>


