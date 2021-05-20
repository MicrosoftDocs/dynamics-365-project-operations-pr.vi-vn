---
title: Mô hình bảo mật
description: Chủ đề này cung cấp thông tin về mô hình bảo mật trong Dynamics 365 Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 8acaa86dec8ebca8f9850877d345e30be3e3a919
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/27/2021
ms.locfileid: "5951235"
---
# <a name="security-model"></a><span data-ttu-id="188cc-103">Mô hình bảo mật</span><span class="sxs-lookup"><span data-stu-id="188cc-103">Security Model</span></span>

<span data-ttu-id="188cc-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="188cc-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="188cc-105">Microsoft Dynamics 365 Project Operations chứa mô hình bảo mật độc đáo, tạo điều kiện cho mô hình bảo mật doanh nghiệp dựa trên vai trò phối hợp với Microsoft Office Groups.</span><span class="sxs-lookup"><span data-stu-id="188cc-105">Microsoft Dynamics 365 Project Operations contains a unique security model that allows for a role-based business security model that collaborates with Microsoft Office Groups.</span></span> 


## <a name="security-roles"></a><span data-ttu-id="188cc-106">Vai trò bảo mật</span><span class="sxs-lookup"><span data-stu-id="188cc-106">Security roles</span></span>
<span data-ttu-id="188cc-107">Các khả năng ngoại vi của Project Operations bao gồm các vai trò sau:</span><span class="sxs-lookup"><span data-stu-id="188cc-107">Project Operations front-end capabilities include the following roles:</span></span>

| <span data-ttu-id="188cc-108">Vai trò</span><span class="sxs-lookup"><span data-stu-id="188cc-108">Role</span></span>                          | <span data-ttu-id="188cc-109">Nội dung mô tả</span><span class="sxs-lookup"><span data-stu-id="188cc-109">Description</span></span>                                                                                                                                                                 | <span data-ttu-id="188cc-110">Phạm vi</span><span class="sxs-lookup"><span data-stu-id="188cc-110">Scope</span></span> |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|
| <span data-ttu-id="188cc-111">Người quản lý thực tiễn</span><span class="sxs-lookup"><span data-stu-id="188cc-111">Practice manager</span></span>              | <span data-ttu-id="188cc-112">Hỗ trợ báo cáo dự án chéo.</span><span class="sxs-lookup"><span data-stu-id="188cc-112">Supports cross-project reporting.</span></span>                                                                                                            | <span data-ttu-id="188cc-113">Đơn vị kinh doanh</span><span class="sxs-lookup"><span data-stu-id="188cc-113">Business unit</span></span>              |
| <span data-ttu-id="188cc-114">Người phê duyệt dự án</span><span class="sxs-lookup"><span data-stu-id="188cc-114">Project approver</span></span>              | <span data-ttu-id="188cc-115">Phê duyệt thời gian và chi phí cho dự án.</span><span class="sxs-lookup"><span data-stu-id="188cc-115">Approves time and expenses against a project.</span></span>                                                                                                                              | <span data-ttu-id="188cc-116">Đơn vị kinh doanh</span><span class="sxs-lookup"><span data-stu-id="188cc-116">Business unit</span></span> |
| <span data-ttu-id="188cc-117">Quản trị viên thanh toán dự án</span><span class="sxs-lookup"><span data-stu-id="188cc-117">Project billing administrator</span></span> | <span data-ttu-id="188cc-118">Tạo đề xuất hóa đơn.</span><span class="sxs-lookup"><span data-stu-id="188cc-118">Creates the invoice proposal.</span></span>                                                                                                                                                 | <span data-ttu-id="188cc-119">Đơn vị kinh doanh</span><span class="sxs-lookup"><span data-stu-id="188cc-119">Business unit</span></span> |
| <span data-ttu-id="188cc-120">Người quản lý dự án</span><span class="sxs-lookup"><span data-stu-id="188cc-120">Project manager</span></span>               | <span data-ttu-id="188cc-121">Tạo kế hoạch dự án và yêu cầu nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="188cc-121">Creates the project plan and requests resources.</span></span>                                                                                                                              | <span data-ttu-id="188cc-122">Đơn vị kinh doanh</span><span class="sxs-lookup"><span data-stu-id="188cc-122">Business unit</span></span> |
| <span data-ttu-id="188cc-123">Nguồn lực dự án</span><span class="sxs-lookup"><span data-stu-id="188cc-123">Project resource</span></span>              | <span data-ttu-id="188cc-124">Các thành viên trong nhóm có thể được đặt trước và báo cáo thời gian.</span><span class="sxs-lookup"><span data-stu-id="188cc-124">Team members who can be booked and report time.</span></span>                                                                                                          | <span data-ttu-id="188cc-125">Đơn vị kinh doanh</span><span class="sxs-lookup"><span data-stu-id="188cc-125">Business unit</span></span>|
| <span data-ttu-id="188cc-126">Resource Manager</span><span class="sxs-lookup"><span data-stu-id="188cc-126">Resource manager</span></span>              | <span data-ttu-id="188cc-127">Tất cả các chức năng quản lý nguồn lực, chẳng hạn như thực hiện các yêu cầu và đặt chỗ nguồn lực, được tách riêng để hỗ trợ người quản lý Dự án kết hợp + Cấu hình trình quản lý nguồn lực và vai trò người quản lý Tài nguyên tập trung và duy nhất.</span><span class="sxs-lookup"><span data-stu-id="188cc-127">All resource management functions, such as fulfill resource requests and bookings, separated to support a hybrid Project manager + Resource manager configuration and a single and centralized Resource manager role.</span></span> | <span data-ttu-id="188cc-128">Đơn vị kinh doanh</span><span class="sxs-lookup"><span data-stu-id="188cc-128">Business unit</span></span> |


<span data-ttu-id="188cc-129">Microsoft Project cho Web bao gồm các vai trò sau:</span><span class="sxs-lookup"><span data-stu-id="188cc-129">Microsoft Project for the Web includes the following roles:</span></span>

| <span data-ttu-id="188cc-130">Vai trò</span><span class="sxs-lookup"><span data-stu-id="188cc-130">Role</span></span>           | <span data-ttu-id="188cc-131">Nội dung mô tả</span><span class="sxs-lookup"><span data-stu-id="188cc-131">Description</span></span>                                                                                                        | <span data-ttu-id="188cc-132">Phạm vi</span><span class="sxs-lookup"><span data-stu-id="188cc-132">Scope</span></span>  |
|----------------|--------------------------------------------------------------------------------------------------------------------|--------|
| <span data-ttu-id="188cc-133">Người dùng dự án</span><span class="sxs-lookup"><span data-stu-id="188cc-133">Project user</span></span>   | <span data-ttu-id="188cc-134">Người dùng cộng tác của Dự án có thể tạo dự án của riêng họ và xem bất kỳ dự án nào được chia sẻ với họ.</span><span class="sxs-lookup"><span data-stu-id="188cc-134">Collaborative user of Project   who is able to create their own projects and view any projects shared with   them.</span></span> | <span data-ttu-id="188cc-135">Người dùng</span><span class="sxs-lookup"><span data-stu-id="188cc-135">User</span></span>   |
| <span data-ttu-id="188cc-136">Hệ thống dự án</span><span class="sxs-lookup"><span data-stu-id="188cc-136">Project system</span></span> | <span data-ttu-id="188cc-137">Vai trò được sử dụng cho ngữ cảnh ứng dụng.</span><span class="sxs-lookup"><span data-stu-id="188cc-137">Role used for application   context.</span></span> <span data-ttu-id="188cc-138">Khách hàng không nên sử dụng vai trò hệ thống này.</span><span class="sxs-lookup"><span data-stu-id="188cc-138">Customers should not use this system role.</span></span>                                    | <span data-ttu-id="188cc-139">Toàn bộ</span><span class="sxs-lookup"><span data-stu-id="188cc-139">Global</span></span> |

## <a name="security-enforcement"></a><span data-ttu-id="188cc-140">Thực thi bảo mật</span><span class="sxs-lookup"><span data-stu-id="188cc-140">Security enforcement</span></span>
<span data-ttu-id="188cc-141">Các hành động được thực hiện ở cấp độ dự án được thực hiện trong ngữ cảnh của người dùng đã đăng nhập.</span><span class="sxs-lookup"><span data-stu-id="188cc-141">Actions that are performed at the project level are performed in the context of the logged in user.</span></span> <span data-ttu-id="188cc-142">Điều này có nghĩa là để tạo, mở hoặc xóa một dự án, người dùng bắt buộc phải có quyền truy cập trong CDS.</span><span class="sxs-lookup"><span data-stu-id="188cc-142">This means that in order to create, open, or delete a project, the user is required to have access available in CDS.</span></span> <span data-ttu-id="188cc-143">Quyền truy cập trong CDS có thể được cấp thông qua bất kỳ cơ chế nào có thể có trong nền tảng.</span><span class="sxs-lookup"><span data-stu-id="188cc-143">Access in CDS may be granted through any of the possible mechanisms included in the platform.</span></span> <span data-ttu-id="188cc-144">Ví dụ: người dùng có phạm vi lớn hơn có thể truy cập dự án hoặc nếu hành động chia sẻ dự án rõ ràng đã được thực hiện để cấp quyền truy cập cho người dùng.</span><span class="sxs-lookup"><span data-stu-id="188cc-144">For example, a user with a larger scope may access the project or if an explicit project share action has been performed which grants the user access.</span></span>

<span data-ttu-id="188cc-145">Điều quan trọng là phải xem xét việc này khi tạo dự án trong Project Operations.</span><span class="sxs-lookup"><span data-stu-id="188cc-145">It's important to consider this when creating projects in Project Operations.</span></span>

## <a name="modern-group-collaboration-with-project-operations"></a><span data-ttu-id="188cc-146">Hợp tác nhóm hiện đại với Project Operations</span><span class="sxs-lookup"><span data-stu-id="188cc-146">Modern group collaboration with Project Operations</span></span>
<span data-ttu-id="188cc-147">Project for the Web và Project Operations hỗ trợ các nhóm hiện đại cộng tác.</span><span class="sxs-lookup"><span data-stu-id="188cc-147">Project for the Web and Project Operations support modern groups for collaboration.</span></span> <span data-ttu-id="188cc-148">Người dùng được thêm vào dự án thông qua một nhóm có thể chỉnh sửa kế hoạch dự án.</span><span class="sxs-lookup"><span data-stu-id="188cc-148">Users added to the project through a group are able to edit the project plan.</span></span>

<span data-ttu-id="188cc-149">Project for the Web tự động thêm người dùng vào nhóm khi được gán.</span><span class="sxs-lookup"><span data-stu-id="188cc-149">Project for the Web adds users to the group automatically upon assignment.</span></span>

<span data-ttu-id="188cc-150">Groups cho phép các quyền của dự án và các tạo tác hỗ trợ cộng tác được thực hiện một cách hợp tác.</span><span class="sxs-lookup"><span data-stu-id="188cc-150">Groups allow the permissions of the project and supporting collaboration artifacts to be worked on collaboratively.</span></span> <span data-ttu-id="188cc-151">Sơ đồ sau đây mô tả các sự kiện và thay đổi trạng thái xảy ra trong quy trình gán nhóm.</span><span class="sxs-lookup"><span data-stu-id="188cc-151">The following diagram depicts the events and state changes that happen during the group assignment process.</span></span>

<span data-ttu-id="188cc-152">Project Operations không tạo ra một nhóm thông qua hành động ngầm và chỉ thực hiện thông qua hành động rõ ràng của các nhóm thúc ép.</span><span class="sxs-lookup"><span data-stu-id="188cc-152">Project Operations does not create a group through implicit action and only does so through the explicit action of pressing groups.</span></span>

<span data-ttu-id="188cc-153">Tìm kiếm thành viên nhóm trong **Quản lý nhóm**, được giới hạn cho những người được đặt là một phần của nhóm bảo mật của môi trường.</span><span class="sxs-lookup"><span data-stu-id="188cc-153">Group member search in the **Group management** dialog, is limited to those who are set as part of the environment's security group.</span></span> <span data-ttu-id="188cc-154">Để biết thêm thông tin, xem [Kiểm soát quyền truy cập người dùng vào môi trường: nhóm bảo mật và giấy phép](/power-platform/admin/control-user-access).</span><span class="sxs-lookup"><span data-stu-id="188cc-154">For more information, see [Control user access to environments: security groups and licenses](/power-platform/admin/control-user-access).</span></span>

![Chế độ nhóm](./media/groupsmode.png)

1. <span data-ttu-id="188cc-156">Dự án được tạo và do thuộc sở hữu của Người dùng tạo.</span><span class="sxs-lookup"><span data-stu-id="188cc-156">The Project is created and owned by the creating User.</span></span>
2. <span data-ttu-id="188cc-157">Chủ dự án được cập nhật vào nhóm.</span><span class="sxs-lookup"><span data-stu-id="188cc-157">The Project owner is updated to the team.</span></span>
3. <span data-ttu-id="188cc-158">Nhóm chủ sở hữu được ánh xạ tới Office Group được chỉ định hoặc đã tạo.</span><span class="sxs-lookup"><span data-stu-id="188cc-158">The Owner team is mapped to the specified or created Office Group.</span></span>
4. <span data-ttu-id="188cc-159">Chủ sở hữu ban đầu của Dự án được thêm vào Office Group.</span><span class="sxs-lookup"><span data-stu-id="188cc-159">The original owner of the Project is added to the Office Group.</span></span>

## <a name="deployment-recommendation"></a><span data-ttu-id="188cc-160">Đề xuất triển khai</span><span class="sxs-lookup"><span data-stu-id="188cc-160">Deployment recommendation</span></span>
<span data-ttu-id="188cc-161">Khi mô hình cộng tác nhóm Office phát triển, chức năng sẽ được thêm vào để cung cấp khả năng kiểm soát chi tiết hơn theo thời gian.</span><span class="sxs-lookup"><span data-stu-id="188cc-161">As the Office group collaboration model evolves, functionality will be added to provide more detailed control over time.</span></span> <span data-ttu-id="188cc-162">Các khách hàng triển khai Project Operations ngày nay được khuyến khích tập trung vào Mô hình bảo mật Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="188cc-162">Customers that deploy Project Operations today are encouraged to focus on a traditional Microsoft Dynamics 365 security model.</span></span>

<span data-ttu-id="188cc-163">Để biết thêm thông tin, hãy xem [Bảo mật trong Common Data Service](/power-platform/admin/wp-security).</span><span class="sxs-lookup"><span data-stu-id="188cc-163">For more information, see [Security in Common Data Service](/power-platform/admin/wp-security).</span></span>

## <a name="project-operations-and-microsoft-dynamics-365-finance-security"></a><span data-ttu-id="188cc-164">Project Operations và bảo mật Microsoft Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="188cc-164">Project Operations and Microsoft Dynamics 365 Finance security</span></span>
<span data-ttu-id="188cc-165">Project Operations bao gồm các vai trò sau:</span><span class="sxs-lookup"><span data-stu-id="188cc-165">Project Operations includes the following roles:</span></span>

- <span data-ttu-id="188cc-166">Người quản lý dự án</span><span class="sxs-lookup"><span data-stu-id="188cc-166">Project manager</span></span>
- <span data-ttu-id="188cc-167">Kế toán dự án</span><span class="sxs-lookup"><span data-stu-id="188cc-167">Project accountant</span></span>

<span data-ttu-id="188cc-168">Để biết thêm thông tin về vai trò bảo mật trong Finance, hãy xem [Bảo mật dựa trên vai trò](/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security).</span><span class="sxs-lookup"><span data-stu-id="188cc-168">For more information about security in Finance, see [Role-based security](/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security).</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]