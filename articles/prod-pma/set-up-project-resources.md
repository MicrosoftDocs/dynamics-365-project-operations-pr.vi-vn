---
title: Thiết lập nguồn lực dự án
description: Chủ đề này cung cấp thông tin về cách thiết lập hoặc yêu cầu nguồn lực dự án.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 49e0ca6254518079d2e01d92ac2e31d119468c4b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997717"
---
# <a name="set-up-project-resources"></a><span data-ttu-id="d99a7-103">Thiết lập nguồn lực dự án</span><span class="sxs-lookup"><span data-stu-id="d99a7-103">Set up project resources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d99a7-104">Bạn phải thiết lập lịch và liên kết nó với nhân viên.</span><span class="sxs-lookup"><span data-stu-id="d99a7-104">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="d99a7-105">Lịch được sử dụng để lập lịch trình cho dự án và thời gian làm việc của các nguồn lực được dành cho dự án.</span><span class="sxs-lookup"><span data-stu-id="d99a7-105">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="d99a7-106">Trong quá trình thiết lập lịch, người quản lý dự án có thể cân bằng tài nguyên trong quá trình tối ưu hóa nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="d99a7-106">During calendar setup, project managers can do resource leveling as part of resource optimization.</span></span> <span data-ttu-id="d99a7-107">Dựa trên lịch trình theo lịch, có thể đưa ra các hạn chế đối với nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="d99a7-107">Based on the calendar schedule, restrictions can be put on resources.</span></span> <span data-ttu-id="d99a7-108">Bạn có thể thiết lập lịch trên trang **Lịch**.</span><span class="sxs-lookup"><span data-stu-id="d99a7-108">You can set up a calendar on the **Calendars** page.</span></span>

<span data-ttu-id="d99a7-109">Khi bạn thiết lập nhân viên làm nguồn lực dự án, bạn có thể chọn từ nhân viên làm việc trong công ty mà bạn đang thiết lập nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="d99a7-109">When you set up a worker as a project resource, you can select from workers who work in the company that you're setting up resources for.</span></span> <span data-ttu-id="d99a7-110">Ngoài ra, bạn có thể chọn nhân viên từ các công ty khác trong tổ chức của mình.</span><span class="sxs-lookup"><span data-stu-id="d99a7-110">Alternatively, you can select workers from other companies in your organization.</span></span> <span data-ttu-id="d99a7-111">Những nhân viên này được gọi là nguồn lực liên công ty.</span><span class="sxs-lookup"><span data-stu-id="d99a7-111">These workers are known as intercompany resources.</span></span>

<span data-ttu-id="d99a7-112">Các quy trình sau đây giải thích cách thiết lập một nhân viên làm nguồn lực dự án trong công ty của bạn và cách thiết lập nguồn lực dự án liên công ty.</span><span class="sxs-lookup"><span data-stu-id="d99a7-112">The following procedures explain how to set up a worker as a project resource in your company and how to set up an intercompany project resource.</span></span>

## <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="d99a7-113">Thiết lập nhân viên làm nguồn lực dự án</span><span class="sxs-lookup"><span data-stu-id="d99a7-113">Set up a worker as a project resource</span></span>

1. <span data-ttu-id="d99a7-114">Trên trang **Nhân viên** trong danh sách **Nhân viên**, chọn nhân viên mà bạn đang thêm làm nguồn lực dự án và mở hồ sơ nhân viên.</span><span class="sxs-lookup"><span data-stu-id="d99a7-114">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2. <span data-ttu-id="d99a7-115">Trên Ngăn hành động, chọn **Dự án** &gt; **Thiết lập** &gt; **Thiết lập dự án**.</span><span class="sxs-lookup"><span data-stu-id="d99a7-115">On the Action Pane, select **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3. <span data-ttu-id="d99a7-116">Chọn lịch rồi đóng trang.</span><span class="sxs-lookup"><span data-stu-id="d99a7-116">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="d99a7-117">Bạn cũng có thể chỉ định các dự án mặc định cho một nguồn lực như một loại phân công trước.</span><span class="sxs-lookup"><span data-stu-id="d99a7-117">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="d99a7-118">Phân công trước có thể được sử dụng khi người quản lý tài nguyên hoặc người quản lý dự án biết trước dự án mà nguồn lực sẽ thực hiện.</span><span class="sxs-lookup"><span data-stu-id="d99a7-118">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="d99a7-119">Phân công trước cũng có thể dựa trên yêu cầu về người tài trợ dự án hoặc khách hàng.</span><span class="sxs-lookup"><span data-stu-id="d99a7-119">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="d99a7-120">Để phân công trước dự án, trên trang **Chỉ định dự án**, trên tab **Dự án**, trong danh sách **Dự án còn lại**, chọn dự án thích hợp.</span><span class="sxs-lookup"><span data-stu-id="d99a7-120">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

## <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="d99a7-121">Thiết lập nguồn lực liên công ty</span><span class="sxs-lookup"><span data-stu-id="d99a7-121">Set up an intercompany resource</span></span>

<span data-ttu-id="d99a7-122">Khi bạn thiết lập một nhân viên làm nguồn lực liên công ty, bạn phải hoàn thành việc thiết lập ở cả công ty cho mượn và công ty mượn.</span><span class="sxs-lookup"><span data-stu-id="d99a7-122">When you set up a worker as an intercompany resource, you must complete the setup in both the lending company and the borrowing company.</span></span>

### <a name="in-the-lending-company"></a><span data-ttu-id="d99a7-123">Ở công ty cho mượn</span><span class="sxs-lookup"><span data-stu-id="d99a7-123">In the lending company</span></span>

1. <span data-ttu-id="d99a7-124">Trong Finance, hãy xác minh rằng công ty cho mượn đã được chọn, rồi hoàn thành quy trình trong phần trước đó: "Thiết lập nhân viên làm nguồn lực dự án".</span><span class="sxs-lookup"><span data-stu-id="d99a7-124">In Finance, verify that the lending company is selected, and then complete the procedure in the previous section, "Set up a worker as a project resource."</span></span>
2. <span data-ttu-id="d99a7-125">Trên trang **Kế toán liên công ty**, chọn **Mới**.</span><span class="sxs-lookup"><span data-stu-id="d99a7-125">On the **Intercompany accounting** page, select **New**.</span></span>
3. <span data-ttu-id="d99a7-126">Trong trường **ID pháp nhân**, chọn công ty cho mượn.</span><span class="sxs-lookup"><span data-stu-id="d99a7-126">In the **Legal entity ID** field, select the lending company.</span></span> <span data-ttu-id="d99a7-127">Điền vào các trường còn lại là thích hợp, sau đó chọn **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="d99a7-127">Fill in the remaining fields as appropriate, and then select **Save**.</span></span>
4. <span data-ttu-id="d99a7-128">Trên trang **Giá chuyển nhượng**, chọn **Mới**.</span><span class="sxs-lookup"><span data-stu-id="d99a7-128">On the **Transfer price** page, select **New**.</span></span>
5. <span data-ttu-id="d99a7-129">Trong trường **Pháp nhân mượn**, chọn công ty thích hợp.</span><span class="sxs-lookup"><span data-stu-id="d99a7-129">In the **Borrowing legal entity** field, select the appropriate company.</span></span>
6. <span data-ttu-id="d99a7-130">Để chỉ cho mượn nguồn lực mà bạn tạo ở đầu phần này, trong trường **Nguồn lực**, chọn tên của nguồn lực mà bạn đã tạo.</span><span class="sxs-lookup"><span data-stu-id="d99a7-130">To lend the borrowing company only the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="d99a7-131">Để hiển thị toàn bộ nguồn lực của công ty cho mượn cho công ty mượn, hãy để trống trường **Nguồn lực**.</span><span class="sxs-lookup"><span data-stu-id="d99a7-131">To make all resources in the lending company available to the borrowing company, leave the **Resource** field blank.</span></span>
7. <span data-ttu-id="d99a7-132">Trên trang **Tham số quản lý dự án và kế toán**, trên tab **Liên công ty**, đặt tùy chọn **Bật lập lịch và bảng chấm công nguồn lực** thành **Có**.</span><span class="sxs-lookup"><span data-stu-id="d99a7-132">On the **Project management and accounting parameters** page, on the **Intercompany** tab, set the **Enable intercompany resource scheduling and timesheets** option to **Yes**.</span></span>

### <a name="in-the-borrowing-company"></a><span data-ttu-id="d99a7-133">Ở công ty mượn</span><span class="sxs-lookup"><span data-stu-id="d99a7-133">In the borrowing company</span></span>

- <span data-ttu-id="d99a7-134">Trên trang **Danh sách nguồn lực**, trong bộ lọc tìm kiếm, hãy nhập tên nguồn lực mà bạn đã tạo cho công ty cho mượn, để xác minh rằng tên đó có trong danh sách nguồn lực dành cho công ty mượn hay không.</span><span class="sxs-lookup"><span data-stu-id="d99a7-134">On the **Resources list** page, in the search filter, enter the name of the resource that you created for the lending company, to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="request-project-resources"></a><span data-ttu-id="d99a7-135">Yêu cầu nguồn lực dự án</span><span class="sxs-lookup"><span data-stu-id="d99a7-135">Request project resources</span></span>
<span data-ttu-id="d99a7-136">Chức năng lập lịch trình nguồn lực dự án chỉ cho phép người quản lý nguồn lực phân phối nguồn lực biên chế trong hoạt động thuê hoặc dự án.</span><span class="sxs-lookup"><span data-stu-id="d99a7-136">The functionality for project resource scheduling only lets resource managers distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="d99a7-137">Để bật chức năng này, hãy hoàn thành các nhiệm vụ sau hoặc xác minh rằng chúng đã được hoàn thành:</span><span class="sxs-lookup"><span data-stu-id="d99a7-137">To enable this functionality, complete the following tasks, or verify that they have been completed:</span></span>

- <span data-ttu-id="d99a7-138">Thiết lập chuỗi số.</span><span class="sxs-lookup"><span data-stu-id="d99a7-138">Set up number sequences.</span></span>
- <span data-ttu-id="d99a7-139">Thiết lập quy trình công việc kế toán và quản lý dự án.</span><span class="sxs-lookup"><span data-stu-id="d99a7-139">Set up project management and accounting workflows.</span></span>
- <span data-ttu-id="d99a7-140">Bật quy trình công việc yêu cầu nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="d99a7-140">Enable resource request workflows.</span></span>

<span data-ttu-id="d99a7-141">Sau khi hoàn thành các nhiệm vụ liên trước, bạn có thể hoàn thành các nhiệm vụ sau theo yêu cầu:</span><span class="sxs-lookup"><span data-stu-id="d99a7-141">After the preceding tasks have been completed, you can complete the following tasks as you require:</span></span>

- <span data-ttu-id="d99a7-142">Tạo một yêu cầu nguồn lực từ nguồn lực biên chế đã đặt trước dự kiến.</span><span class="sxs-lookup"><span data-stu-id="d99a7-142">Create a resource request from a soft-booked staffed resource.</span></span>
- <span data-ttu-id="d99a7-143">Giám sát yêu cầu nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="d99a7-143">Monitor resource requests.</span></span>
- <span data-ttu-id="d99a7-144">Thực hiện các đề nghị nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="d99a7-144">Fulfill resource requests.</span></span>
- <span data-ttu-id="d99a7-145">Yêu cầu nguồn lực biên chế từ WBS.</span><span class="sxs-lookup"><span data-stu-id="d99a7-145">Request a staffed resource from a WBS.</span></span>
- <span data-ttu-id="d99a7-146">Đặt trước nguồn lực cho dự án mà không có yêu cầu về nguồn lực biên chế.</span><span class="sxs-lookup"><span data-stu-id="d99a7-146">Book resources to a project without having a request for a staffed resource.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]