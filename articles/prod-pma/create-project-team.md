---
title: Tạo nhóm dự án
description: Chủ đề này cung cấp thông tin về cách tạo và quản lý nhóm dự án.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kdwns
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a7eb9101352afd27b527bf6b8acc6f92198f44ea
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087273"
---
# <a name="create-a-project-team"></a><span data-ttu-id="3d054-103">Tạo nhóm dự án</span><span class="sxs-lookup"><span data-stu-id="3d054-103">Create a project team</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3d054-104">Để sử dụng các vai trò đã được thiết lập trước đó trong một dự án, người quản lý dự án phải liên kết các vai trò đó với dự án.</span><span class="sxs-lookup"><span data-stu-id="3d054-104">To use the roles that were previously set up in a project, a project manager must associate the roles with the project.</span></span> <span data-ttu-id="3d054-105">Có thể gán nhiều vai trò cho một dự án.</span><span class="sxs-lookup"><span data-stu-id="3d054-105">Multiple roles can be assigned for a project.</span></span> <span data-ttu-id="3d054-106">Để tránh nhầm lẫn, các vai trò này được tự động gắn nhãn trong quá trình dự trữ.</span><span class="sxs-lookup"><span data-stu-id="3d054-106">To prevent confusion, these roles are automatically labeled during reservation.</span></span> <span data-ttu-id="3d054-107">Ví dụ: nếu người quản lý dự án yêu cầu ba kỹ sư phần mềm, thì ba vai trò Kỹ sư phần mềm có nhãn là **kỹ sư phần mềm 1** , **kỹ sư phần mềm 2** và **kỹ sư phần mềm 3** sẽ được tạo tự động.</span><span class="sxs-lookup"><span data-stu-id="3d054-107">For example, if the project manager requires three software engineers, three Software engineer roles that have **software engineer 1** , **software engineer 2** , and **software engineer 3** as their labels are automatically generated.</span></span> <span data-ttu-id="3d054-108">Nếu các đặc điểm của vai trò đã được thiết lập cho vai trò, thì chúng được áp dụng như một bộ lọc trong quá trình tìm kiếm nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="3d054-108">If role characteristics were previously set for the role, they are applied as a filter during searches for a resource.</span></span> <span data-ttu-id="3d054-109">Các đặc điểm bổ sung có thể được thêm vào theo yêu cầu để tinh chỉnh thêm nội dung tìm kiếm.</span><span class="sxs-lookup"><span data-stu-id="3d054-109">Additional characteristics can be added as required to further refine the search.</span></span>

<span data-ttu-id="3d054-110">Cài đặt dạng xem cũng có thể được tùy chỉnh để mang lại dạng xem tốt hơn về tình trạng rảnh/bận của nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="3d054-110">View settings can also be customized to give a better view of resource availability.</span></span> <span data-ttu-id="3d054-111">Có các tùy chọn để hiển thị tình trạng rảnh/bận theo giờ, ngày, tuần, tháng, quý và năm.</span><span class="sxs-lookup"><span data-stu-id="3d054-111">There are options to show hourly, daily, weekly, monthly, quarterly, and annual availability.</span></span> <span data-ttu-id="3d054-112">Ngoài ra, còn có một tùy chọn để hiển thị năng lực sẵn sàng và còn lại của nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="3d054-112">There is also an option to show available and remaining capacity on resources.</span></span> <span data-ttu-id="3d054-113">Tùy chọn này hữu ích cho việc quản lý thời gian, khi bạn ước tính thời gian sẵn có cho các hoạt động hoặc tình trạng rảnh/bận của nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="3d054-113">This option is useful for time management, when you're estimating available time for activities or resource availability.</span></span>

<span data-ttu-id="3d054-114">Người quản lý dự án có thể chọn một vai trò trên trang và sau đó, nếu có sẵn một nguồn lực phù hợp với yêu cầu, hãy chọn dự trữ nguồn lực để thực hiện vai trò đó.</span><span class="sxs-lookup"><span data-stu-id="3d054-114">The project manager can select a role on the page and then, if there is an available resource that fits the requirement, select to reserve a resource to fill the role.</span></span> <span data-ttu-id="3d054-115">Lưu ý rằng không cần dự trữ nguồn lực tại thời điểm này trong giai đoạn lập kế hoạch.</span><span class="sxs-lookup"><span data-stu-id="3d054-115">Note that the resources don't have to be reserved at this point in the planning stage.</span></span> <span data-ttu-id="3d054-116">Khi tạo một WBS, bạn có thể thay các vai trò bằng nguồn lực có biên chế cho dự án.</span><span class="sxs-lookup"><span data-stu-id="3d054-116">When you create a WBS, you can replace roles with staffed resources for the project.</span></span> <span data-ttu-id="3d054-117">Nếu vai trò được thay bằng nguồn lực có biên chế trong WBS, thiết lập nguồn lực sẽ tự động cập nhật danh sách và lịch trình của nhóm dự án.</span><span class="sxs-lookup"><span data-stu-id="3d054-117">If roles are replaced with staffed resources in the WBS, the resource setup automatically updates the project team listing and scheduling.</span></span>

<span data-ttu-id="3d054-118">[![Danh sách nhóm dự án bao gồm cả vai trò và nguồn lực thực tế](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span><span class="sxs-lookup"><span data-stu-id="3d054-118">[![Project team listing that includes both roles and actual resources](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span></span> 

<span data-ttu-id="3d054-119">Người quản lý dự án có nhiều tùy chọn khác nhau để đặt trước nguồn lực cho một dự án, chẳng hạn như **Năng lực còn lại** , **Năng lực đầy đủ** , **Phần trăm năng lực** và **Chỉ định giờ**.</span><span class="sxs-lookup"><span data-stu-id="3d054-119">The project manager has various options for booking a resource for a project, such as **Remaining capacity** , **Full capacity** , **Capacity percentage** , and **Specify hours**.</span></span> <span data-ttu-id="3d054-120">Các tùy chọn đặt trước này có thể bị hủy bỏ bất cứ lúc nào nếu việc phân công nguồn lực thay đổi.</span><span class="sxs-lookup"><span data-stu-id="3d054-120">These booking options can be canceled at any time if resource assignments change.</span></span> <span data-ttu-id="3d054-121">Hai loại đặt trước được hỗ trợ:</span><span class="sxs-lookup"><span data-stu-id="3d054-121">Two types of booking are supported:</span></span>

- <span data-ttu-id="3d054-122">**Đặt trước chắc chắn** – Việc dự trữ nguồn lực đã được phê duyệt và xác nhận để tiến hành thuê trong thời gian quy định.</span><span class="sxs-lookup"><span data-stu-id="3d054-122">**Hard Book** – The resource reservation was approved and confirmed to work on the engagement for the specified duration.</span></span>
- <span data-ttu-id="3d054-123">**Đặt trước dự kiến** – Việc dự trữ nguồn lực được dự kiến thiết lập để tiến hành thuê trong thời gian quy định.</span><span class="sxs-lookup"><span data-stu-id="3d054-123">**Soft book** – The resource reservations was tentatively set to work on the engagement for the specified duration.</span></span>

<span data-ttu-id="3d054-124">Quy trình sau đây giải thích cách tạo nhóm dự án.</span><span class="sxs-lookup"><span data-stu-id="3d054-124">The following procedure explains how to create a project team.</span></span>

## <a name="create-a-project-team"></a><span data-ttu-id="3d054-125">Tạo nhóm dự án</span><span class="sxs-lookup"><span data-stu-id="3d054-125">Create a project team</span></span>

1. <span data-ttu-id="3d054-126">Trên trang danh sách **Tất cả dự án** , chọn dự án rồi chọn **Chỉnh sửa**.</span><span class="sxs-lookup"><span data-stu-id="3d054-126">On the **All projects** list page, select a project, and then select **Edit**.</span></span>
2. <span data-ttu-id="3d054-127">Trên tab **Nhóm dự án và lập lịch trình** , trong trường **Lên lịch ngày kết thúc** , nhập ngày bắt đầu lịch trình cộng thêm một tháng.</span><span class="sxs-lookup"><span data-stu-id="3d054-127">On the **Project team and scheduling** tab, in the **Schedule end date** field, enter the schedule start date plus one month.</span></span> <span data-ttu-id="3d054-128">Ví dụ: nếu ngày bắt đầu lịch trình là ngày 24 tháng 6 năm 2017 (24/06/2017), hãy nhập **24/07/2017**.</span><span class="sxs-lookup"><span data-stu-id="3d054-128">For example, if the schedule start date is June 24, 2017 (24/06/2017), enter **24/07/2017**.</span></span>
3. <span data-ttu-id="3d054-129">Chọn **Thêm**.</span><span class="sxs-lookup"><span data-stu-id="3d054-129">Select **Add**.</span></span>
4. <span data-ttu-id="3d054-130">Trong ngăn **Thêm vai trò vào dự án** , trong trường **Vai trò** , chọn **Người quản lý dự án cấp cao**.</span><span class="sxs-lookup"><span data-stu-id="3d054-130">In the **Add roles to the project** pane, in the **Role** field, select **Senior Project Manager**.</span></span>
5. <span data-ttu-id="3d054-131">Lựa chọn **Năng lực cần thiết**.</span><span class="sxs-lookup"><span data-stu-id="3d054-131">Select **Required competencies**.</span></span>
6. <span data-ttu-id="3d054-132">Trên trang **Chọn đặc điểm** , các đặc điểm mà bạn đã thiết lập cho vai trò Người quản lý dự án cấp cao được chọn theo mặc định.</span><span class="sxs-lookup"><span data-stu-id="3d054-132">On the **Choose characteristics** page, the characteristics that you previously set for the Senior project manager role are selected by default.</span></span> <span data-ttu-id="3d054-133">Chọn **OK**.</span><span class="sxs-lookup"><span data-stu-id="3d054-133">Select **OK**.</span></span>
7. <span data-ttu-id="3d054-134">Trên trang **Thêm vai trò vào dự án** , trong trường **Số lượng tài nguyên** , nhập **1**.</span><span class="sxs-lookup"><span data-stu-id="3d054-134">On the **Add roles to project** page, in the **Number of resources** field, enter **1**.</span></span>
8. <span data-ttu-id="3d054-135">Trong trường **Nguồn lực** , phần tra cứu hiển thị tất cả nguồn lực có năng lực cần thiết.</span><span class="sxs-lookup"><span data-stu-id="3d054-135">In the **Resource** field, the lookup shows all resources that have the required competencies.</span></span> <span data-ttu-id="3d054-136">Chọn **Daniel Goldschmidt** rồi chọn **Tạo**.</span><span class="sxs-lookup"><span data-stu-id="3d054-136">Select **Daniel Goldschmidt** , and then select **Create**.</span></span>
9. <span data-ttu-id="3d054-137">Trên trang **Dự án** , chọn **Thêm**.</span><span class="sxs-lookup"><span data-stu-id="3d054-137">On the **Project** page, select **Add**.</span></span>
10. <span data-ttu-id="3d054-138">Trong ngăn **Thêm vai trò vào dự án** , trong trường **Vai trò** , chọn **Thành viên nhóm**.</span><span class="sxs-lookup"><span data-stu-id="3d054-138">In the **Add roles to the project** pane, in the **Role** field, select **Team member**.</span></span> <span data-ttu-id="3d054-139">Trong trường **Số nguồn lực** , nhập **5**.</span><span class="sxs-lookup"><span data-stu-id="3d054-139">In the **Number of resources** field, enter **5**.</span></span>
11. <span data-ttu-id="3d054-140">Chọn **Tạo**.</span><span class="sxs-lookup"><span data-stu-id="3d054-140">Select **Create**.</span></span>
12. <span data-ttu-id="3d054-141">Trên trang **Dự án** , chọn **Đáp ứng nguồn lực**.</span><span class="sxs-lookup"><span data-stu-id="3d054-141">On the **Projects** page, select **Fulfill resource**.</span></span>

## <a name="monitor-project-teams"></a><span data-ttu-id="3d054-142">Giám sát các nhóm dự án</span><span class="sxs-lookup"><span data-stu-id="3d054-142">Monitor project teams</span></span>
1. <span data-ttu-id="3d054-143">Trên trang **Tất cả dự án** , chọn liên kết **ID dự án** cho dự án **Nâng cấp XYZ Giai đoạn 2**.</span><span class="sxs-lookup"><span data-stu-id="3d054-143">On the **All projects** page, select the **Project ID** link for the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="3d054-144">Trên **Nhóm dự án và lập lịch trình** FastTab, xác minh rằng các nguồn lực dự án được liệt kê là chính xác.</span><span class="sxs-lookup"><span data-stu-id="3d054-144">On the **Project team and scheduling** FastTab, verify that the project resources that are listed are correct.</span></span>
