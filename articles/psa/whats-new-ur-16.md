---
title: Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 16, V3
description: Chủ đề này liệt kê các tính năng và bản sửa lỗi có trong Bản phát hành cập nhật Project Service Automation 16, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
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
ms.openlocfilehash: 1f3bb4442ce1d06807f264003c930dbbee19a5c7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280919"
---
# <a name="project-service-automation-update-release-16-v3"></a><span data-ttu-id="13b79-103">Phát hành bản cập nhật Project Service Automation 16, V3</span><span class="sxs-lookup"><span data-stu-id="13b79-103">Project Service Automation Update Release 16, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="13b79-104">Chúng tôi vui mừng thông báo bản cập nhật mới nhất dành cho ứng dụng Project Service Automation của Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="13b79-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="13b79-105">Bản phát hành này bao gồm một số cải tiến quan trọng về chất lượng, hiệu suất và khả năng sử dụng.</span><span class="sxs-lookup"><span data-stu-id="13b79-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="13b79-106">Bản phát hành này tương thích với Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="13b79-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="13b79-107">Để cập nhật lên bản phát hành này, hãy truy cập vào Trung tâm quản trị cho Dynamics 365 trực tuyến, rồi chuyển đến trang giải pháp để cài đặt bản cập nhật.</span><span class="sxs-lookup"><span data-stu-id="13b79-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="13b79-108">Để biết thêm thông tin, hãy xem phần [Cài đặt, cập nhật giải pháp ưu tiên](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).</span><span class="sxs-lookup"><span data-stu-id="13b79-108">For more information, see [Install, Update a Preferred Solution](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).</span></span>
<span data-ttu-id="13b79-109">Chủ đề này liệt kê các tính năng và bản sửa lỗi mới hoặc đã thay đổi cho PSA V3, Bản phát hành cập nhật 16.</span><span class="sxs-lookup"><span data-stu-id="13b79-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 16.</span></span> <span data-ttu-id="13b79-110">Phiên bản này có số bản dựng là V3.10.6.34 và thường có sẵn thông qua bản tự cập nhật vào tháng 1 năm 2020.</span><span class="sxs-lookup"><span data-stu-id="13b79-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in January 2020.</span></span>


## <a name="update-release-16"></a><span data-ttu-id="13b79-111">Phát hành bản cập nhật 16</span><span class="sxs-lookup"><span data-stu-id="13b79-111">Update Release 16</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="13b79-112">Sửa lỗi</span><span class="sxs-lookup"><span data-stu-id="13b79-112">Bug fixes</span></span>

-   <span data-ttu-id="13b79-113">Thời gian và Chi phí</span><span class="sxs-lookup"><span data-stu-id="13b79-113">Time and Expense</span></span>

    -   <span data-ttu-id="13b79-114">Sửa lỗi: Người dùng cố gửi các mục nhập thời gian và chi phí đã xóa để phê duyệt giờ sẽ nhận được thông báo lỗi có liên quan.</span><span class="sxs-lookup"><span data-stu-id="13b79-114">Fixed: Users attempting to submit deleted time and expense entries for approvals will now receive relevant error messages.</span></span>

-   <span data-ttu-id="13b79-115">Quản lý dự án</span><span class="sxs-lookup"><span data-stu-id="13b79-115">Project Management</span></span>

    -   <span data-ttu-id="13b79-116">Sửa lỗi: Đơn vị cấp nguồn lực đã xác định cho các thành viên nhóm trong mẫu được xem xét với mẫu được áp dụng cho dự án mới.</span><span class="sxs-lookup"><span data-stu-id="13b79-116">Fixed: The resourcing units defined for team members in templates are respected with the templates are applied to a new project.</span></span>

    -   <span data-ttu-id="13b79-117">Sửa lỗi: Cải thiện việc xử lý quá trình gán lại quyền sở hữu bản ghi.</span><span class="sxs-lookup"><span data-stu-id="13b79-117">Fixed: Improved handling of the re-assignment of record ownership.</span></span>

    -   <span data-ttu-id="13b79-118">Sửa lỗi: Các dự án đang được sao chép sẽ không được phép sao chép cho đến khi tất cả các thao tác sao chép hoàn tất.</span><span class="sxs-lookup"><span data-stu-id="13b79-118">Fixed: Projects that are in the process of being copied will not be permitted to copied until all copy operations are complete.</span></span>

-   <span data-ttu-id="13b79-119">Quản lý nguồn lực</span><span class="sxs-lookup"><span data-stu-id="13b79-119">Resource Management</span></span>

    -   <span data-ttu-id="13b79-120">Sửa lỗi: Thao tác mở rộng đăng ký giờ sẽ xử lý khoảng thời gian ngắn một cách chính xác và không còn tạo ra 0 giờ cho lượt đăng ký mở rộng.</span><span class="sxs-lookup"><span data-stu-id="13b79-120">Fixed: Extend bookings now handles short durations correctly and no longer creates zero hours for extended bookings.</span></span>

    -   <span data-ttu-id="13b79-121">Sửa lỗi: Dạng xem điều hòa giờ sẽ hiển thị khi múi giờ dự án là +5:30 GMT và múi giờ của người dùng là khác nhau.</span><span class="sxs-lookup"><span data-stu-id="13b79-121">Fixed: The reconciliation view now renders when the project time zone is +5:30 GMT and the user’s time aone is different.</span></span>

-   <span data-ttu-id="13b79-122">Sales</span><span class="sxs-lookup"><span data-stu-id="13b79-122">Sales</span></span>

    -   <span data-ttu-id="13b79-123">Sửa lỗi: Khi một dự án đã ánh xạ đến mô tả hợp đồng bị xóa và một dự án mới được ánh xạ, bản ghi thực tế trên dự án mới không được đánh giá lại dựa trên các quy tắc thanh toán và định giá đã xác định trên mô tả hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="13b79-123">Fixed: When a project mapped to a contract line is removed and a new project is mapped, the actual records on the new project were not getting re-evaluated based on the billing and pricing rules defined on the contract line.</span></span> <span data-ttu-id="13b79-124">Lỗi này đã được khắc phục trong bản phát hành này.</span><span class="sxs-lookup"><span data-stu-id="13b79-124">This has been fixed in this release.</span></span> <span data-ttu-id="13b79-125">Bản ghi thực tế và giá trên dự án mới được ánh xạ sẽ bị hủy bỏ và được tạo lại chính xác dựa trên các quy tắc định giá và thanh toán của mô tả hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="13b79-125">Pricing and actual records on the newly mapped project will get reversed and re-created correctly based on the pricing and billing rules of the contract line.</span></span> <span data-ttu-id="13b79-126">Kết quả là bản ghi thực tế của dự án không được ánh xạ cũng sẽ được đánh giá lại và tạo lại.</span><span class="sxs-lookup"><span data-stu-id="13b79-126">The actual records of the un-mapped project will also get re-evaluated and re-created as a consequence.</span></span>

    -   <span data-ttu-id="13b79-127">Sửa lỗi: Thêm xác thực bổ sung vào trường **Số tiền** của mô tả ước tính để đảm bảo rằng các giá trị rỗng không được giữ tiếp tục.</span><span class="sxs-lookup"><span data-stu-id="13b79-127">Fixed: Additional validation has been added to an estimate line’s **Amount** field to ensure that null values are not persisted.</span></span>

    -   <span data-ttu-id="13b79-128">Sửa lỗi: Khi dữ liệu thực tế đã được cập nhật trên một dự án, một nút làm mới đã được thêm vào biểu mẫu chính của dự án để cho phép người dùng đồng bộ hóa lại dữ liệu thực tế.</span><span class="sxs-lookup"><span data-stu-id="13b79-128">Fixed: When actuals have been updated on a project, a refresh button has been added to the project main form to allow users to re-sync the actuals.</span></span>

    -   <span data-ttu-id="13b79-129">Sửa lỗi: Khi người dùng nâng cấp từ 2.X lên 3.X, các dự án có giá trị RỖNG cho tên dự án sẽ được cho phép.</span><span class="sxs-lookup"><span data-stu-id="13b79-129">Fixed: When users upgrade from 2.X to 3.X, projects with a NULL value for project name will be permitted.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]