---
title: Tạo dự án mới
description: Chủ đề này cung cấp thông tin về cách tạo dự án mới.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b29340dc88aea888ea2f5ea975eaea59d014279
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270749"
---
# <a name="create-a-new-project"></a><span data-ttu-id="3377f-103">Tạo dự án mới</span><span class="sxs-lookup"><span data-stu-id="3377f-103">Create a new project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3377f-104">Hoàn thành các bước sau để tạo dự án mới.</span><span class="sxs-lookup"><span data-stu-id="3377f-104">Complete the following steps to create a new project.</span></span>

1. <span data-ttu-id="3377f-105">Trên trang **Quản lý dự án**, chọn **Dự án mới** rồi nhập các giá trị sau đây:</span><span class="sxs-lookup"><span data-stu-id="3377f-105">On the **Project management** page, select **New project**, and enter the following values:</span></span>

    - <span data-ttu-id="3377f-106">**Loại dự án:** Thời gian và vật liệu</span><span class="sxs-lookup"><span data-stu-id="3377f-106">**Project type:** Time and material</span></span>
    - <span data-ttu-id="3377f-107">**Tên dự án:** Nâng cấp XYZ Giai đoạn 2</span><span class="sxs-lookup"><span data-stu-id="3377f-107">**Project name:** XYZ Upgrade Phase 2</span></span>
    - <span data-ttu-id="3377f-108">**Nhóm dự án:** TM\_WIP</span><span class="sxs-lookup"><span data-stu-id="3377f-108">**Project group:** TM\_WIP</span></span>
    - <span data-ttu-id="3377f-109">**ID hợp đồng dự án:** 00000002</span><span class="sxs-lookup"><span data-stu-id="3377f-109">**Project contract ID:** 00000002</span></span>

2. <span data-ttu-id="3377f-110">Chọn **Tạo dự án**.</span><span class="sxs-lookup"><span data-stu-id="3377f-110">Select **Create project**.</span></span>

## <a name="assign-a-resource-to-a-project"></a><span data-ttu-id="3377f-111">Chỉ định nguồn lực cho dự án</span><span class="sxs-lookup"><span data-stu-id="3377f-111">Assign a resource to a project</span></span>

1. <span data-ttu-id="3377f-112">Trên trang **Nhân viên** trong danh sách **Nhân viên**, chọn bản ghi cho nhân viên mà bạn đã thiết lập năng lực và mở bản ghi nhân viên.</span><span class="sxs-lookup"><span data-stu-id="3377f-112">On the **Workers** page, in the **Workers** list, select the record for the worker that you previously set up competencies for, and open the worker record.</span></span>
2. <span data-ttu-id="3377f-113">Trên Ngăn hành động, trên tab **Dự án**, trong nhóm **Thiết lập**, chọn **Chỉ định dự án**.</span><span class="sxs-lookup"><span data-stu-id="3377f-113">On the Action Pane, on the **Project** tab, in the **Setup** group, select **Assign projects**.</span></span>
3. <span data-ttu-id="3377f-114">Trên trang **Phân công dự án xác thực nguồn lực**, trên tab **Dự án**, trong trường **Thêm dự án vào các dự án đã chọn**, lọc trên dự án **Nâng cấp XYZ Giai đoạn 2**.</span><span class="sxs-lookup"><span data-stu-id="3377f-114">On the **Resource validation project assignments** page, on the **Projects** tab, in the **Add the project to selected projects** field, filter on the **XYZ Upgrade Phase 2** project.</span></span>
4. <span data-ttu-id="3377f-115">Trong ngăn **Dự án còn lại**, chọn dự án rồi chọn nút mũi tên để thêm vào ngăn **Dự án đã chọn**.</span><span class="sxs-lookup"><span data-stu-id="3377f-115">In the **Remaining projects** pane, select a project, and then select the arrow button to add it to the **Selected projects** pane.</span></span>

<span data-ttu-id="3377f-116">Bạn cũng có thể chỉ định các thể loại cho nguồn lực mà mình cần.</span><span class="sxs-lookup"><span data-stu-id="3377f-116">You can also assign categories for a resource as you require.</span></span> <span data-ttu-id="3377f-117">Thể loại là **Chi phí** hoặc **Doanh thu**.</span><span class="sxs-lookup"><span data-stu-id="3377f-117">The category type is either **Cost** or **Revenue**.</span></span> <span data-ttu-id="3377f-118">Thể loại được xác định bởi tổ chức của bạn.</span><span class="sxs-lookup"><span data-stu-id="3377f-118">The category type is determined by your organization.</span></span> <span data-ttu-id="3377f-119">Nếu không có thể loại nào được chỉ định cho nguồn lực, Finance sẽ tra cứu thể loại mặc định trên giá theo giờ để biết chi phí và doanh thu.</span><span class="sxs-lookup"><span data-stu-id="3377f-119">If no categories are assigned for a resource, Finance looks up the default category on hour prices for cost and revenue.</span></span>

## <a name="set-up-project-resource-and-role-characteristics"></a><span data-ttu-id="3377f-120">Thiết lập đặc điểm vai trò và nguồn lực dự án</span><span class="sxs-lookup"><span data-stu-id="3377f-120">Set up project resource and role characteristics</span></span>

<span data-ttu-id="3377f-121">Người quản lý dự án có thể sử dụng chức năng nguồn lực dự án để tạo các vai trò cần thiết cho dự án.</span><span class="sxs-lookup"><span data-stu-id="3377f-121">A project manager can use the project resourcing functionality to create the roles that are required for the project.</span></span> <span data-ttu-id="3377f-122">Có thể sử dụng vai trò nếu nguồn lực đã xác nhận vẫn là không xác định khi nguồn lực đang được dự trữ.</span><span class="sxs-lookup"><span data-stu-id="3377f-122">Roles can be used if confirmed resources are still unknown when resources are being reserved.</span></span> <span data-ttu-id="3377f-123">Các vai trò có thể được dự trữ tạm thời dưới dạng nguồn lực đã lập kế hoạch để bạn có thể tiếp tục các giai đoạn lập kế hoạch dự án.</span><span class="sxs-lookup"><span data-stu-id="3377f-123">Roles can be temporarily reserved as planned resources, so that you can continue the project planning stages.</span></span>

<span data-ttu-id="3377f-124">[![Ví dụ về vai trò](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span><span class="sxs-lookup"><span data-stu-id="3377f-124">[![Example of a role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span></span> 

<span data-ttu-id="3377f-125">**Tình huống:** Contoso được thuê để hoàn thành một dự án Thời gian và vật liệu có điều lệ dự án đã được phê duyệt.</span><span class="sxs-lookup"><span data-stu-id="3377f-125">**Scenario:** Contoso was hired to complete a Time and material project that has an approved project charter.</span></span> <span data-ttu-id="3377f-126">Người quản lý dự án cấp dưới vẫn đang hoàn thành phạm vi của dự án.</span><span class="sxs-lookup"><span data-stu-id="3377f-126">The junior project manager is still completing the scope of the project.</span></span> <span data-ttu-id="3377f-127">Người quản lý tài nguyên hiện đang xác định các nguồn lực cụ thể sẽ được dự trữ để thực hiện dự án mới.</span><span class="sxs-lookup"><span data-stu-id="3377f-127">The resource manager is currently identifying specific resources that will be reserved to work on the new project.</span></span> <span data-ttu-id="3377f-128">Do tính chất quan trọng của dự án, nhà tài trợ dự án đã yêu cầu Người quản lý dự án cấp cao là một trong các vai trò.</span><span class="sxs-lookup"><span data-stu-id="3377f-128">Because of the critical nature of the project, the project sponsor requested Senior project manager as one of the roles.</span></span> <span data-ttu-id="3377f-129">Người quản lý tài nguyên phải có được nguồn lực mới và xác định vai trò trong hệ thống trong trường hợp người quản lý dự án cấp dưới yêu cầu thông tin tài nguyên trong quá trình lập kế hoạch dự án.</span><span class="sxs-lookup"><span data-stu-id="3377f-129">The resource manager must acquire the new resource and define the role in the system in case the junior project manager requires the resource information during project planning.</span></span>

<span data-ttu-id="3377f-130">Các bước sau đây cho thấy cách người quản lý nguồn lực có thể thiết lập vai trò Người quản lý dự án cấp cao và liên kết các đặc điểm của nguồn lực với vai trò đó.</span><span class="sxs-lookup"><span data-stu-id="3377f-130">The following steps show how the resource manager can set up the Senior project manager role and associate resource characteristics with it.</span></span> <span data-ttu-id="3377f-131">Sau đó, vai trò có thể được sử dụng để tìm kiếm các nguồn lực có sẵn phù hợp với năng lực của nguồn lực được yêu cầu.</span><span class="sxs-lookup"><span data-stu-id="3377f-131">Later, the role can be used to search for available resources that match the required resource competencies.</span></span>

1. <span data-ttu-id="3377f-132">Trên trang **Thiết lập vai trò**, chọn **Mới** rồi nhập các giá trị sau đây:</span><span class="sxs-lookup"><span data-stu-id="3377f-132">On the **Setup roles** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="3377f-133">**ID vai trò:** Người quản lý dự án cấp cao</span><span class="sxs-lookup"><span data-stu-id="3377f-133">**Role ID:** Senior Project Manager</span></span>
    - <span data-ttu-id="3377f-134">**Mô tả:** Người quản lý dự án cấp cao</span><span class="sxs-lookup"><span data-stu-id="3377f-134">**Description:** Senior Project Manager</span></span>

2. <span data-ttu-id="3377f-135">Chọn **Tạo**.</span><span class="sxs-lookup"><span data-stu-id="3377f-135">Select **Create**.</span></span>
3. <span data-ttu-id="3377f-136">Chọn vai trò **Người quản lý dự án cấp cao** rồi chọn **Đặt cấu hình đặc điểm**.</span><span class="sxs-lookup"><span data-stu-id="3377f-136">Select the **Senior Project Manager** role, and then select **Configure characteristics**.</span></span>
4. <span data-ttu-id="3377f-137">Trong trường **Loại đặc điểm**, chọn **Kỹ năng**.</span><span class="sxs-lookup"><span data-stu-id="3377f-137">In the **Characteristics type** field, select **Skill**.</span></span>
5. <span data-ttu-id="3377f-138">Trong trường **Đặc điểm có sẵn**, nhập kỹ năng để tìm kiếm.</span><span class="sxs-lookup"><span data-stu-id="3377f-138">In the **Available characteristics** field, enter the skill to search for.</span></span>
6. <span data-ttu-id="3377f-139">Trong trường **Loại đặc điểm**, chọn **Chứng chỉ**.</span><span class="sxs-lookup"><span data-stu-id="3377f-139">In the **Characteristic type** field, select **Certificate**.</span></span>
7. <span data-ttu-id="3377f-140">Trong trường **Đặc điểm có sẵn**, nhập loại chứng chỉ để tìm kiếm.</span><span class="sxs-lookup"><span data-stu-id="3377f-140">In the **Available characteristics** field, enter the certificate type to search for.</span></span>

## <a name="assign-a-project-resource-to-a-project"></a><span data-ttu-id="3377f-141">Chỉ định nguồn lực dự án cho dự án</span><span class="sxs-lookup"><span data-stu-id="3377f-141">Assign a project resource to a project</span></span>

1. <span data-ttu-id="3377f-142">Trên trang **Tất cả dự án**, chọn dự án **Nâng cấp XYZ Giai đoạn 2**.</span><span class="sxs-lookup"><span data-stu-id="3377f-142">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="3377f-143">Trên tab **Nhóm dự án và lập lịch trình**, chọn **Thêm**.</span><span class="sxs-lookup"><span data-stu-id="3377f-143">On the **Project team and scheduling** tab, select **Add**.</span></span>
3. <span data-ttu-id="3377f-144">Trong trường **Vai trò**, chọn **Thành viên nhóm**.</span><span class="sxs-lookup"><span data-stu-id="3377f-144">In the **Role** field, select **Team member**.</span></span>
4. <span data-ttu-id="3377f-145">Chọn **Đặt từ lịch**.</span><span class="sxs-lookup"><span data-stu-id="3377f-145">Select **Book from calendar**.</span></span>
5. <span data-ttu-id="3377f-146">Trên trang **Khả năng dùng nguồn lực**, chọn **Thiết đặt dạng xem**.</span><span class="sxs-lookup"><span data-stu-id="3377f-146">On the **Resource availability** page, select **View settings**.</span></span>
6. <span data-ttu-id="3377f-147">Trên trang **Điều chỉnh thiết đặt dạng xem**, nhập các giá trị sau đây:</span><span class="sxs-lookup"><span data-stu-id="3377f-147">On the **Adjust view settings** page, enter the following values:</span></span>

    - <span data-ttu-id="3377f-148">**Định dạng cho dạng xem phạm vi ngày:** Ngày</span><span class="sxs-lookup"><span data-stu-id="3377f-148">**Format for date range view:** Day</span></span>
    - <span data-ttu-id="3377f-149">**Hiển thị mô tả tình trạng rảnh/bận:** Có</span><span class="sxs-lookup"><span data-stu-id="3377f-149">**Display availability descriptions:** Yes</span></span>
    - <span data-ttu-id="3377f-150">**Hiển thị năng lực còn lại:** Có</span><span class="sxs-lookup"><span data-stu-id="3377f-150">**Display remaining capacity:** Yes</span></span>

7. <span data-ttu-id="3377f-151">Trong danh sách nguồn lực, chọn một nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="3377f-151">In the list of resources, select a resource.</span></span>
8. <span data-ttu-id="3377f-152">Chọn **Đặt trước chắc chắn** và **Năng lực đầy đủ**.</span><span class="sxs-lookup"><span data-stu-id="3377f-152">Select **Hard book** and **Full capacity**.</span></span>

## <a name="assign-a-resource-to-a-default-role"></a><span data-ttu-id="3377f-153">Chỉ định nguồn lực cho vai trò mặc định</span><span class="sxs-lookup"><span data-stu-id="3377f-153">Assign a resource to a default role</span></span>

<span data-ttu-id="3377f-154">Giúp các nhà quản lý dự án hoặc nguồn lực xem chi tiết các nguồn lực có thể được dành riêng cho một dự án.</span><span class="sxs-lookup"><span data-stu-id="3377f-154">To help project or resource managers can drill down further on the resources that can be reserved for a project.</span></span> <span data-ttu-id="3377f-155">Bạn có thể liên kết một vai trò mặc định với một tài nguyên hiện có hoặc một tài nguyên mới có được.</span><span class="sxs-lookup"><span data-stu-id="3377f-155">You can associate a default role with an existing resource or a newly acquired resource.</span></span> <span data-ttu-id="3377f-156">Ví dụ: khi Daniel được thuê, anh ấy có kinh nghiệm và kỹ năng để đảm nhiệm vai trò Phân tích viên kinh doanh.</span><span class="sxs-lookup"><span data-stu-id="3377f-156">For example, when Daniel was hired, he had the experience and skills to fill the Business analyst role.</span></span> <span data-ttu-id="3377f-157">Người quản lý nguồn lực đã gán vai trò này là vai trò mặc định của Daniel.</span><span class="sxs-lookup"><span data-stu-id="3377f-157">The resource manager assigned this role as Daniel's default role.</span></span> <span data-ttu-id="3377f-158">Do đó, người quản lý nguồn lực đã thêm Daniel vào một nhóm các phân tích viên kinh doanh sẵn sàng làm việc trong các dự án.</span><span class="sxs-lookup"><span data-stu-id="3377f-158">Therefore, the resource manager added Daniel to a pool of business analysts who are available to work on projects.</span></span>

<span data-ttu-id="3377f-159">Trong quá trình dự trữ nguồn lực, người quản lý dự án có thể lọc các nguồn lực vai trò có sẵn để thực hiện dự án.</span><span class="sxs-lookup"><span data-stu-id="3377f-159">During resource reservation, project managers can filter the role resources that are available to work on projects.</span></span> <span data-ttu-id="3377f-160">Họ có thể sử dụng thông tin này như một tiêu chí khi thực hiện phân tích quyết định đa tiêu chí trong quá trình thực hiện nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="3377f-160">They can use this information as one criterion when they perform multi-criteria decision analysis during resource fulfillment.</span></span> <span data-ttu-id="3377f-161">Họ cũng có thể thêm các đặc điểm nguồn lực khác vào bộ lọc để tìm kiếm các tài nguyên có kỹ năng, trình độ học vấn và kinh nghiệm cụ thể cho một dự án nhất định.</span><span class="sxs-lookup"><span data-stu-id="3377f-161">They can also add other resource characteristics to the filter to search for resources that have specific skills, education, and experience for a given project.</span></span>

<span data-ttu-id="3377f-162">**Tình huống:** Một dự án được phê duyệt đã bắt đầu và vai trò Người quản lý dự án cấp cao được dự trữ như một nguồn lực theo kế hoạch trong giai đoạn lập kế hoạch dự án.</span><span class="sxs-lookup"><span data-stu-id="3377f-162">**Scenario:** An approved project has started, and the Senior project manager role was reserved as a planned resource during the project planning stage.</span></span> <span data-ttu-id="3377f-163">Người quản lý nguồn lực hiện đã có được một nguồn lực để thực hiện vai trò Người quản lý dự án cấp cao.</span><span class="sxs-lookup"><span data-stu-id="3377f-163">The resource manager has now acquired a resource to fulfill the Senior project manager role.</span></span>

1. <span data-ttu-id="3377f-164">Trên trang **Danh sách nguồn lực**, chọn **Daniel Goldschmidt**.</span><span class="sxs-lookup"><span data-stu-id="3377f-164">On the **Resources list** page, select **Daniel Goldschmidt**.</span></span>
2. <span data-ttu-id="3377f-165">Trên trang **Vai trò nguồn lực**, chọn **Mới** rồi nhập các giá trị sau đây:</span><span class="sxs-lookup"><span data-stu-id="3377f-165">On the **Resource role** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="3377f-166">**Có hiệu lực:** Nhập ngày hiện tại.</span><span class="sxs-lookup"><span data-stu-id="3377f-166">**Effective:** Enter the current date.</span></span>
    - <span data-ttu-id="3377f-167">**Hết hạn:** Nhập **Không bao giờ**.</span><span class="sxs-lookup"><span data-stu-id="3377f-167">**Expiration:** Enter **Never**.</span></span>
    - <span data-ttu-id="3377f-168">**Vai trò:** Nhập **Người quản lý dự án cấp cao**.</span><span class="sxs-lookup"><span data-stu-id="3377f-168">**Role:** Enter **Senior Project Manager**.</span></span>

3. <span data-ttu-id="3377f-169">Chọn **Lưu** rồi đóng trang.</span><span class="sxs-lookup"><span data-stu-id="3377f-169">Select **Save**, and then close the page.</span></span>
4. <span data-ttu-id="3377f-170">Trên tab **Năng lực**, thêm kỹ năng **Quản lý dự án** và chứng chỉ **PMP**.</span><span class="sxs-lookup"><span data-stu-id="3377f-170">On the **Competencies** tab, add the **ProjectMgmt** skill and the **PMP** certificate.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]