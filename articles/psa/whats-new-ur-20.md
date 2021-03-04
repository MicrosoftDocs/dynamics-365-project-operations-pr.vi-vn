---
title: Tính năng mới hoặc đã thay đổi trong Bản phát hành cập nhật Project Service Automation 20, V3
description: Chủ đề này liệt kê các tính năng và bản sửa lỗi có trong Bản phát hành cập nhật Project Service Automation 20, V3
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: ee3be43da401af405ab329b9b5a724a2e95c0219
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147139"
---
# <a name="project-service-automation-update-release-20-v3"></a><span data-ttu-id="00e3c-103">Phát hành bản cập nhật Project Service Automation 20, V3</span><span class="sxs-lookup"><span data-stu-id="00e3c-103">Project Service Automation Update Release 20, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="00e3c-104">Chúng tôi vui mừng thông báo bản cập nhật mới nhất dành cho ứng dụng Project Service Automation của Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="00e3c-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="00e3c-105">Bản phát hành này bao gồm một số cải tiến quan trọng về chất lượng, hiệu suất và khả năng sử dụng.</span><span class="sxs-lookup"><span data-stu-id="00e3c-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="00e3c-106">Bản phát hành này tương thích với Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="00e3c-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="00e3c-107">Để cập nhật lên bản phát hành này, hãy truy cập vào Trung tâm quản trị cho trang giải pháp trực tuyến Dynamics 365 để cài đặt bản cập nhật.</span><span class="sxs-lookup"><span data-stu-id="00e3c-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="00e3c-108">Để biết thêm thông tin, hãy xem [Cài đặt, cập nhật hoặc xóa giải pháp ưu tiên](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="00e3c-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="00e3c-109">Chủ đề này liệt kê các tính năng và bản sửa lỗi mới hoặc đã thay đổi cho Project Service Automation V3, Bản phát hành cập nhật 20.</span><span class="sxs-lookup"><span data-stu-id="00e3c-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 20.</span></span> <span data-ttu-id="00e3c-110">Phiên bản này có số bản dựng là V 3.10.31.37 và thường được cung cấp thông qua bản tự cập nhật vào tháng 6 năm 2020.</span><span class="sxs-lookup"><span data-stu-id="00e3c-110">This version has a build number of V 3.10.31.37 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-20"></a><span data-ttu-id="00e3c-111">Phát hành bản cập nhật 20</span><span class="sxs-lookup"><span data-stu-id="00e3c-111">Update Release 20</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="00e3c-112">Sửa lỗi</span><span class="sxs-lookup"><span data-stu-id="00e3c-112">Bug fixes</span></span>

<span data-ttu-id="00e3c-113">**Quản lý dự án**</span><span class="sxs-lookup"><span data-stu-id="00e3c-113">**Project Management**</span></span>

<span data-ttu-id="00e3c-114">Các vấn đề sau đã được khắc phục:</span><span class="sxs-lookup"><span data-stu-id="00e3c-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="00e3c-115">Việc nhập thành viên nhóm dự án với phương pháp phân bổ yêu cầu số giờ dẫn đến thông báo lỗi không rõ ràng khi số giờ được chỉ định bằng không.</span><span class="sxs-lookup"><span data-stu-id="00e3c-115">Importing project team members with an allocation method that requires hours results in an unclear error message when the specified hours are zero.</span></span>
- <span data-ttu-id="00e3c-116">Người dùng nhận được lỗi không chính xác khi số lượng ký tự tối đa đã được nhập vào trường **Mô tả** cho một nhiệm vụ dự án.</span><span class="sxs-lookup"><span data-stu-id="00e3c-116">Users receive an incorrect error when the maximum number of characters have been entered into the **Description** field for a project task.</span></span>
- <span data-ttu-id="00e3c-117">Trang **Tải xuống phần bổ trợ Microsoft Dynamics 365 Project Service Automation** chuyển hướng đến trang tải xuống tiếng Anh khi cài đặt ngôn ngữ của người dùng được đặt thành tiếng Nhật.</span><span class="sxs-lookup"><span data-stu-id="00e3c-117">The **Microsoft Dynamics 365 Project Service Automation add-in download** page redirects to the English download page when the user’s language settings are set to Japanese.</span></span>
- <span data-ttu-id="00e3c-118">Khi xảy ra lỗi máy chủ, nhãn đồng bộ hóa trên tab **Lịch trình** của biểu mẫu **Dự án** đôi khi vẫn còn.</span><span class="sxs-lookup"><span data-stu-id="00e3c-118">When a server error occurs, the synchronization label on the **Schedule** tab of the **Projects** form sometimes remains.</span></span>
- <span data-ttu-id="00e3c-119">Các bản cập nhật nhiệm vụ dự phòng đang được gửi đến máy chủ khi một nhiệm vụ được sửa đổi.</span><span class="sxs-lookup"><span data-stu-id="00e3c-119">Redundant task updates are being sent to the server when a task is modified.</span></span>

<span data-ttu-id="00e3c-120">**Sales**</span><span class="sxs-lookup"><span data-stu-id="00e3c-120">**Sales**</span></span>

<span data-ttu-id="00e3c-121">Các vấn đề sau đã được khắc phục:</span><span class="sxs-lookup"><span data-stu-id="00e3c-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="00e3c-122">Trên biểu mẫu **Hợp đồng**, nhấp đúp vào **Tạo hóa đơn** tạo ra hai hóa đơn cho một bản ghi thực tế duy nhất.</span><span class="sxs-lookup"><span data-stu-id="00e3c-122">On the **Contract** form, double-clicking **Create Invoice** creates two invoices for a single actuals record.</span></span>
- <span data-ttu-id="00e3c-123">Trong Internet Explorer 11, người dùng không thể tạo các mục nhập chi phí.</span><span class="sxs-lookup"><span data-stu-id="00e3c-123">In Internet Explorer 11, users are unable to create expense entries.</span></span>
- <span data-ttu-id="00e3c-124">Đảo ngược Chi phí và đảo ngược Dữ liệu thực tế về doanh thu bán hàng chưa lập hóa đơn không được liên kết.</span><span class="sxs-lookup"><span data-stu-id="00e3c-124">Reversal of Cost and reversal of Unbilled Sales Actuals are not linked.</span></span>
- <span data-ttu-id="00e3c-125">Nút **Làm mới số liệu thực tế** trên biểu mẫu **Dự án** không làm mới **Số giờ thực tế cho nhiệm vụ**.</span><span class="sxs-lookup"><span data-stu-id="00e3c-125">The **Refresh Actuals** button on the **Project** form does not refresh **Task Actual Hours**.</span></span>
- <span data-ttu-id="00e3c-126">Phần bổ trợ **PreValidateProjectTeamMemberCreate** có thể tạo các nguồn lực có thể đặt trước chung khi thuộc tính **msdyn_isgenericresourceprojectscoped** được đặt thành **Sai**.</span><span class="sxs-lookup"><span data-stu-id="00e3c-126">The **PreValidateProjectTeamMemberCreate** plug-in can create duplicate generic bookable resources when the attribute **msdyn_isgenericresourceprojectscoped** is set to **False**.</span></span>
- <span data-ttu-id="00e3c-127">**Tính toán lại** xóa chi phí có thể tính phí của chi tiết mô tả báo giá dựa trên sản phẩm và chi tiết mô tả hợp đồng.</span><span class="sxs-lookup"><span data-stu-id="00e3c-127">**Recalculate** clears chargeable costs of product-based quote line details and contract line details.</span></span>
- <span data-ttu-id="00e3c-128">Trong các kịch bản cụ thể, phần bổ trợ **PostEstimateLineUpdate** hiển thị lỗi ngoại lệ tham chiếu null.</span><span class="sxs-lookup"><span data-stu-id="00e3c-128">In specific scenarios, the **PostEstimateLineUpdate** plug-in displays a null teference exception error.</span></span>
- <span data-ttu-id="00e3c-129">Khoảng thời gian giai đoạn thời gian trên **Biểu đồ phân tích lợi nhuận** không khớp với khoảng thời gian của chi phí trong chi tiết mô tả báo giá với chi phí cố định của báo giá.</span><span class="sxs-lookup"><span data-stu-id="00e3c-129">Time phase duration on the **Profitability Analysis Chart** does not match duration of the costs in the fixed-price quote line detail of the quote.</span></span>
- <span data-ttu-id="00e3c-130">Giá trị đơn vị và nhóm đơn vị không mặc định chính xác cho các danh mục chi phí trên các biểu mẫu **Chi tiết mô tả hợp đồng** và **Chi tiết mô tả báo giá**.</span><span class="sxs-lookup"><span data-stu-id="00e3c-130">Unit and unit group values do not default correctly for expense categories on the **Contract Line Details** and **Quote Line Details** forms.</span></span>
- <span data-ttu-id="00e3c-131">Danh sách **Giá vốn đơn vị tổ chức** cho phép chồng chéo trong hiệu lực ngày tháng.</span><span class="sxs-lookup"><span data-stu-id="00e3c-131">**Org Unit Cost Price** lists permit overlaps in the date effectivity.</span></span>
- <span data-ttu-id="00e3c-132">Người dùng không được phép thay đổi **Đơn vị tổ chức** khi loại đơn hàng không dựa trên công việc vì điều này sẽ dẫn đến lỗi ngoại lệ tham chiếu null.</span><span class="sxs-lookup"><span data-stu-id="00e3c-132">Users are not permitted to change the **OrgUnit** when the order type is not work-based because it will lead to a null reference exception error.</span></span>
- <span data-ttu-id="00e3c-133">Khi cố gắng điều hướng từ biểu mẫu **Chi tiết mô tả báo giá**, quay lại tab **Báo giá**, biểu mẫu làm mới và hiển thị tab **Tóm tắt**.</span><span class="sxs-lookup"><span data-stu-id="00e3c-133">When attempting to navigate from the **Quote Line Details** form, back to the **Quote** tab, the form refreshes and displays the **Summary** tab.</span></span>
