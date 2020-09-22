---
title: Tích hợp Microsoft Project Client
description: Việc lập kế hoạch và duy trì lịch trình dự án có thể phức tạp, vì vậy người quản lý dự án cần sử dụng các công cụ giúp họ quản lý công việc này. Tích hợp với Microsoft Project Client cung cấp sự hỗ trợ để mở và quản lý cấu trúc phân tích công việc của dự án.
author: KimANelson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: c6478e05-50ee-4993-87f4-6ce9cb78f076
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: e35e1e54bad659d1329c333479830b680a17cbb0
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 03/24/2020
ms.locfileid: "3757116"
---
# <a name="microsoft-project-client-integration"></a><span data-ttu-id="fdb65-104">Tích hợp Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="fdb65-104">Microsoft Project client integration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fdb65-105">Việc lập kế hoạch và duy trì lịch trình dự án có thể phức tạp, vì vậy người quản lý dự án cần sử dụng các công cụ giúp họ quản lý công việc này.</span><span class="sxs-lookup"><span data-stu-id="fdb65-105">Planning and maintaining a project schedule can be complex, so project managers need to use tools that help them manage this task.</span></span> <span data-ttu-id="fdb65-106">Tích hợp với Microsoft Project Client cung cấp sự hỗ trợ để mở và quản lý cấu trúc phân tích công việc của dự án.</span><span class="sxs-lookup"><span data-stu-id="fdb65-106">Integration with Microsoft Project Client provides support to open and manage a project work breakdown structure.</span></span> <span data-ttu-id="fdb65-107">Người quản lý dự án có thể xuất bản bất kỳ thay đổi nào trở lại cấu trúc phân tích công việc dự án Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="fdb65-107">The project manager can publish any changes back to the Dynamics 365 Finance project work breakdown structure.</span></span>

> [!NOTE]
> <span data-ttu-id="fdb65-108">Nếu bạn đang sử dụng bản cập nhật tháng 7 (phiên bản 10.0.4), bạn phải cài đặt KB 4054797 và 4055884.</span><span class="sxs-lookup"><span data-stu-id="fdb65-108">If you are using the July update (version 10.0.4), you must install KB 4054797 and 4055884.</span></span>

## <a name="configure-the-microsoft-project-client-add-in"></a><span data-ttu-id="fdb65-109">Đặt cấu hình phần bổ trợ Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="fdb65-109">Configure the Microsoft Project Client add-in</span></span>
<span data-ttu-id="fdb65-110">Để cho phép tích hợp với Microsoft Project Client, phần bổ trợ Microsoft Dynamics 365 bắt buộc phải được cài đặt trong ứng dụng Microsoft Project máy khách của người dùng.</span><span class="sxs-lookup"><span data-stu-id="fdb65-110">To enable the integration with Microsoft Project Client, a Microsoft Dynamics 365 add-in is required to be installed in the user’s client Microsoft Project application.</span></span> <span data-ttu-id="fdb65-111">Điều này được thực hiện bằng cách mở **Không gian làm việc quản lý dự án**.</span><span class="sxs-lookup"><span data-stu-id="fdb65-111">This is done by opening the **Project management workspace**.</span></span>

<span data-ttu-id="fdb65-112">•   Nhấp vào **Đặt cấu hình phần bổ trợ máy khách dự án** từ phần **Liên kết** > **Thiết lập** của không gian làm việc.</span><span class="sxs-lookup"><span data-stu-id="fdb65-112">•   Click **Configure project client add-in** from the **Links** > **Setup** section of the workspace.</span></span>

<span data-ttu-id="fdb65-113">•   Nhấp vào **Mở**, sau đó nhấp vào **Chạy** khi được nhắc.</span><span class="sxs-lookup"><span data-stu-id="fdb65-113">•   Click **Open**, then click **Run** when prompted.</span></span>

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a><span data-ttu-id="fdb65-114">Mở và chỉnh sửa cấu trúc phân tích công việc bản nháp hiện có trong Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="fdb65-114">Open and edit an existing draft work breakdown structure in Microsoft Project Client</span></span>
<span data-ttu-id="fdb65-115">Nếu một dự án trong Dynamics 365 Finance đã được tạo cấu trúc phân tích công việc, cấu trúc phân tích công việc đó có thể được mở trong ứng dụng Microsoft Project Client nếu cấu trúc phân tích công việc ở trạng thái bản nháp.</span><span class="sxs-lookup"><span data-stu-id="fdb65-115">If a project in Dynamics 365 Finance already has a work breakdown structure created, the work breakdown structure can be opened in the Microsoft Project Client application if the work breakdown structure is in a draft status.</span></span> <span data-ttu-id="fdb65-116">Để mở từ trang **Dự án**, nhấp vào liên kết **Mở trong Microsoft Project** từ tab **Kế hoạch**. Trang này cũng có thể được mở từ trong ứng dụng Microsoft Project Client bằng cách nhấp vào **Mở** trong tab **Microsoft Dynamics 365**. Chọn **Pháp nhân** và **Dự án** từ danh sách.</span><span class="sxs-lookup"><span data-stu-id="fdb65-116">To open from the **Project** page, click **Open in Microsoft Project** link from the **Plan** tab. This page can also be opened from within the Microsoft Project Client application by clicking **Open** in the **Microsoft Dynamics 365** tab. Select the **Legal entity** and **Project** from the list.</span></span>

> [!NOTE]
> <span data-ttu-id="fdb65-117">Nếu bạn đang sử dụng Internet Explorer là trình duyệt của mình, bạn sẽ cần nhấp vào **Lưu** để mở thủ công từ vị trí tệp được tải xuống.</span><span class="sxs-lookup"><span data-stu-id="fdb65-117">If you're using Internet Explorer as your browser, you will need to click **Save** to manually open from the location that the file is downloaded to.</span></span> <span data-ttu-id="fdb65-118">Hoặc, nhấp vào **Lưu và mở** để mở tệp trong Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="fdb65-118">Or, click **Save and open** to open the file in Microsoft Project Client.</span></span> <span data-ttu-id="fdb65-119">Không đổi tên tệp khi lưu.</span><span class="sxs-lookup"><span data-stu-id="fdb65-119">Do not rename the file name when saving.</span></span>

<span data-ttu-id="fdb65-120">Trước khi thực hiện bất kỳ chỉnh sửa nào đối với tệp bằng Microsoft Project Client, bạn cần kiểm tra nó. Nhấp vào **Kiểm tra** trong tab **Microsoft Dynamics 365**. Điều này sẽ ngăn những người dùng khác chỉnh sửa cấu trúc phân tích công việc từ bên trong Finance cùng một lúc.</span><span class="sxs-lookup"><span data-stu-id="fdb65-120">Before making any edits to the file using Microsoft Project Client, you need to check it out. Click **Check out** in the **Microsoft Dynamics 365** tab. This will prevent other users from editing the work breakdown structure from within Finance at the same time.</span></span> <span data-ttu-id="fdb65-121">Để phát hành cấu trúc phân tích công việc sau khi hoàn thành bất kỳ chỉnh sửa nào, hãy nhấp vào **Kiểm nhập** trên tab **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="fdb65-121">To publish the work breakdown structure after completing any edits, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

<span data-ttu-id="fdb65-122">Nếu một nhóm dự án đã được thêm vào dự án trong Finance, danh sách nguồn lực sẽ được điền với các thành viên trong nhóm.</span><span class="sxs-lookup"><span data-stu-id="fdb65-122">If a project team has already been added to the project in Finance, the resource list will be populated with the team members.</span></span> <span data-ttu-id="fdb65-123">Nếu nhóm dự án chưa được thêm vào dự án, bạn có thể chọn nguồn lực và xây dựng nhóm trong Microsoft Project Client bằng cách nhấp vào nút **Nguồn lực** trên tab **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="fdb65-123">If a project team has not yet been added to the project, you can select resources and build the team within Microsoft Project Client by clicking the **Resources** button on the **Microsoft Dynamics 365** tab.</span></span> 

<span data-ttu-id="fdb65-124">Dữ liệu sau đây sẽ được đồng bộ hóa trở lại Finance như một phần của quy trình kiểm nhập:</span><span class="sxs-lookup"><span data-stu-id="fdb65-124">The following data will be synced back to Finance as part of the check-in process:</span></span>

<span data-ttu-id="fdb65-125">•   Tên tác vụ</span><span class="sxs-lookup"><span data-stu-id="fdb65-125">•   Task name</span></span>

<span data-ttu-id="fdb65-126">•   Ngày bắt đầu</span><span class="sxs-lookup"><span data-stu-id="fdb65-126">•   Start date</span></span>

<span data-ttu-id="fdb65-127">•   Ngày hoàn thành</span><span class="sxs-lookup"><span data-stu-id="fdb65-127">•   Finish date</span></span>

<span data-ttu-id="fdb65-128">•   Người tiền nhiệm</span><span class="sxs-lookup"><span data-stu-id="fdb65-128">•   Predecessors</span></span>

<span data-ttu-id="fdb65-129">•   Tên nguồn lực</span><span class="sxs-lookup"><span data-stu-id="fdb65-129">•   Resource names</span></span>

<span data-ttu-id="fdb65-130">•   Thể loại</span><span class="sxs-lookup"><span data-stu-id="fdb65-130">•   Category</span></span>

<span data-ttu-id="fdb65-131">•   Thể loại nguồn lực</span><span class="sxs-lookup"><span data-stu-id="fdb65-131">•   Resource category</span></span>

<span data-ttu-id="fdb65-132">•   Giờ làm việc</span><span class="sxs-lookup"><span data-stu-id="fdb65-132">•   Work hours</span></span>

<span data-ttu-id="fdb65-133">•   Ghi chú</span><span class="sxs-lookup"><span data-stu-id="fdb65-133">•   Notes</span></span>

<span data-ttu-id="fdb65-134">•   Mức ưu tiên</span><span class="sxs-lookup"><span data-stu-id="fdb65-134">•   Priority</span></span>

> [!NOTE]
> <span data-ttu-id="fdb65-135">Nếu bạn thêm bất kỳ cột nào khác vào tệp Microsoft Project Client của mình, chúng sẽ không được lưu vào tệp và sẽ không được hiển thị khi tệp được mở lại.</span><span class="sxs-lookup"><span data-stu-id="fdb65-135">If you add any other columns to your Microsoft Project Client file, they will not be saved to the file and will not be displayed when the file is opened again.</span></span>

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="fdb65-136">Tạo cấu trúc phân tích công việc cho một dự án hiện có bằng Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="fdb65-136">Create the work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="fdb65-137">Để tạo cấu trúc phân tích công việc mới bằng Microsoft Project Client, hãy làm theo các bước sau:</span><span class="sxs-lookup"><span data-stu-id="fdb65-137">To create a new work breakdown structure using Microsoft Project Client, follow these steps:</span></span>


1.  <span data-ttu-id="fdb65-138">Mở Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="fdb65-138">Open Microsoft Project Client.</span></span>

2.  <span data-ttu-id="fdb65-139">Trên tab **Microsoft Dynamics 365**, nhấp vào **Mở**.</span><span class="sxs-lookup"><span data-stu-id="fdb65-139">On the **Microsoft Dynamics 365** tab, click **Open**.</span></span>

3.  <span data-ttu-id="fdb65-140">Chọn **Pháp nhân** cho dự án.</span><span class="sxs-lookup"><span data-stu-id="fdb65-140">Select the **Legal entity** for the project.</span></span>

4.  <span data-ttu-id="fdb65-141">Chọn **Dự án**.</span><span class="sxs-lookup"><span data-stu-id="fdb65-141">Select the **Project**.</span></span>

5.  <span data-ttu-id="fdb65-142">Nhấp vào **Kiểm tra** trên tab **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="fdb65-142">Click **Check out** on the **Microsoft Dynamics 365** tab.</span></span>

6.  <span data-ttu-id="fdb65-143">Khi sẵn sàng phát hành lên Finance, hãy nhấp vào **Đăng ký** trên tab **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="fdb65-143">When ready to publish to Finance, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="fdb65-144">Thay thế cấu trúc phân tích công việc hiện có cho một dự án hiện có bằng Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="fdb65-144">Replace the existing work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="fdb65-145">Để tạo cấu trúc phân tích công việc mới bằng Microsoft Project Client và thay thế cấu trúc phân tích công việc hiện có cho một dự án hiện có, hãy làm theo các bước sau:</span><span class="sxs-lookup"><span data-stu-id="fdb65-145">To create a new work breakdown structure using Microsoft Project Client and replace an existing work breakdown structure for an existing project, follow these steps:</span></span>

1.  <span data-ttu-id="fdb65-146">Mở Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="fdb65-146">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="fdb65-147">Tạo lịch trình Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="fdb65-147">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="fdb65-148">Trên tab **Microsoft Dynamics 365**, nhấp vào **Lưu thay đổi** > **Thay thế dự án hiện có**.</span><span class="sxs-lookup"><span data-stu-id="fdb65-148">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Replace existing project**.</span></span>

4.  <span data-ttu-id="fdb65-149">Chọn **Pháp nhân** cho dự án.</span><span class="sxs-lookup"><span data-stu-id="fdb65-149">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="fdb65-150">Chọn **Dự án**.</span><span class="sxs-lookup"><span data-stu-id="fdb65-150">Select the **Project**.</span></span>

6.  <span data-ttu-id="fdb65-151">Bấm **OK**.</span><span class="sxs-lookup"><span data-stu-id="fdb65-151">Click **OK**.</span></span>

## <a name="create-a-new-project-from-within-microsoft-project-client"></a><span data-ttu-id="fdb65-152">Tạo một dự án mới từ trong Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="fdb65-152">Create a new project from within Microsoft Project Client</span></span>


1.  <span data-ttu-id="fdb65-153">Mở Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="fdb65-153">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="fdb65-154">Tạo lịch trình Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="fdb65-154">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="fdb65-155">Trên tab **Microsoft Dynamics 365**, nhấp vào **Lưu thay đổi** > **Lưu vào Dự án mới**.</span><span class="sxs-lookup"><span data-stu-id="fdb65-155">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Save to new Project**.</span></span>

4.  <span data-ttu-id="fdb65-156">Chọn **Pháp nhân** cho dự án.</span><span class="sxs-lookup"><span data-stu-id="fdb65-156">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="fdb65-157">Nhập **ID dự án** nếu cần.</span><span class="sxs-lookup"><span data-stu-id="fdb65-157">Enter the **Project ID**, if necessary.</span></span>

6.  <span data-ttu-id="fdb65-158">Nhập **Tên dự án**.</span><span class="sxs-lookup"><span data-stu-id="fdb65-158">Enter the **Project name**.</span></span>

7.  <span data-ttu-id="fdb65-159">Chọn **Loại dự án**, **Nhóm dự án** và **ID hợp đồng dự án**.</span><span class="sxs-lookup"><span data-stu-id="fdb65-159">Select the **Project type**, **Project group** and the **Project contract ID**.</span></span> <span data-ttu-id="fdb65-160">Ngoài ra, bạn có thể tạo hợp đồng dự án mới bằng cách nhấp vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="fdb65-160">Alternatively, you can create a new project contract by clicking **New**.</span></span>

8.  <span data-ttu-id="fdb65-161">Chọn **Lịch** để sử dụng cho việc cấp nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="fdb65-161">Select the **Calendar** to be used for resourcing.</span></span>

11. <span data-ttu-id="fdb65-162">Bấm **OK**.</span><span class="sxs-lookup"><span data-stu-id="fdb65-162">Click **OK**.</span></span>
