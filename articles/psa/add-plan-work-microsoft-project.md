---
title: Sử dụng Trình bổ sung của Project Service để hoạch định công việc của bạn trong Microsoft Project | MicrosoftDocs
description: Chủ đề này cung cấp thông tin về cách thêm, cấu hình và sử dụng phần bổ trợ Microsoft Project cho Microsoft Project Service.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 04/06/2019
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
ms.openlocfilehash: 6bc74442866caccc02e53afc913a55aab81f9629
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129704"
---
# <a name="use-the-project-service-automation-add-in-to-plan-your-work-in-microsoft-project"></a><span data-ttu-id="f129c-103">Sử dụng Trình bổ sung Project Service Automation để lập kế hoạch công việc của bạn trong Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="f129c-103">Use the Project Service Automation Add-in to plan your work in Microsoft Project</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] <span data-ttu-id="f129c-104">giúp bạn lập kế hoạch dự án của mình dễ dàng hơn, kể cả việc ước tính.</span><span class="sxs-lookup"><span data-stu-id="f129c-104">makes it easier for you to do your project planning, including estimates.</span></span> <span data-ttu-id="f129c-105">Bạn có thể xác định công việc để có chi phí, nỗ lực và giá bán rõ ràng khi gửi đề xuất cuối cùng.</span><span class="sxs-lookup"><span data-stu-id="f129c-105">You can define the work so that costs, effort, and sales value are clear as the final proposal is submitted.</span></span>  

 <span data-ttu-id="f129c-106">Bây giờ bạn có thể cài đặt [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] và thực hiện việc lập kế hoạch trong môi trường quen thuộc của [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="f129c-106">Now you can install the [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] and do your planning work in the familiar environment of [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span> <span data-ttu-id="f129c-107">Sử dụng các tính năng lập kế hoạch và quản lý mạnh mẽ của [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] rồi cập nhật kế hoạch dự án của bạn trong Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="f129c-107">Use the robust planning and management capabilities of [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and then update your project plan in Project Service Automation.</span></span>  

> [!IMPORTANT]
> - <span data-ttu-id="f129c-108">Để dùng tính năng quản lý tài liệu SharePoint lưu trữ tệp [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] của bạn cho các dự án [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], quản trị viên [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] của bạn cần phải bật tính năng quản lý tài liệu.</span><span class="sxs-lookup"><span data-stu-id="f129c-108">To use SharePoint document management to store your [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] files for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projects, your [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] admin will need to turn on document management.</span></span> 
> - <span data-ttu-id="f129c-109">[!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] chỉ tương thích với [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.</span><span class="sxs-lookup"><span data-stu-id="f129c-109">The [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] is only compatible with [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.</span></span>  

## <a name="download-and-install-the-add-in"></a><span data-ttu-id="f129c-110">Tải xuống và cài đặt trình bổ sung</span><span class="sxs-lookup"><span data-stu-id="f129c-110">Download and install the add-in</span></span>  
 <span data-ttu-id="f129c-111">Chuẩn bị sẵn sàng thông tin đăng nhập [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] của bạn.</span><span class="sxs-lookup"><span data-stu-id="f129c-111">Have your [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sign-in information ready.</span></span> <span data-ttu-id="f129c-112">Bạn sẽ cần thông tin này để kết nối từ [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] đến [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="f129c-112">You will need this information to connect from [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

1.  <span data-ttu-id="f129c-113">Từ Trung tâm tải xuống, hãy tải xuống phần bổ trợ cho phiên bản Project Service được hỗ trợ, [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) hoặc [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).</span><span class="sxs-lookup"><span data-stu-id="f129c-113">From the Download Center, download the add-in for your supported version of Project Service, either [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) or [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).</span></span>  

2.  <span data-ttu-id="f129c-114">Bấm vào liên kết tải xuống.</span><span class="sxs-lookup"><span data-stu-id="f129c-114">Click the download link.</span></span>  

3.  <span data-ttu-id="f129c-115">Khi hoàn tất tải xuống, nhấp vào **Có** để cài đặt trình bổ sung.</span><span class="sxs-lookup"><span data-stu-id="f129c-115">When the download is complete, click **Yes** to install the add-in.</span></span>  

## <a name="configure-the-add-in"></a><span data-ttu-id="f129c-116">Định cấu hình cho trình bổ sung</span><span class="sxs-lookup"><span data-stu-id="f129c-116">Configure the add-in</span></span>  

1. <span data-ttu-id="f129c-117">Mở [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] và bấm vào thẻ **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="f129c-117">Open [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and click the **Project Service** tab.</span></span>  

2. <span data-ttu-id="f129c-118">Bấm vào **Kết nối**.</span><span class="sxs-lookup"><span data-stu-id="f129c-118">Click **Connect**.</span></span>  

3. <span data-ttu-id="f129c-119">Nhập thông tin đăng nhập của bạn rồi bấm vào **Đăng nhập**.</span><span class="sxs-lookup"><span data-stu-id="f129c-119">Enter your sign-in information and then click **Sign in**.</span></span>  

   <span data-ttu-id="f129c-120">Bây giờ bạn có thể bắt đầu sử dụng trình bổ sung.</span><span class="sxs-lookup"><span data-stu-id="f129c-120">Now you can start using the add-in.</span></span>  

## <a name="read-from-a-template"></a><span data-ttu-id="f129c-121">Đọc từ một mẫu</span><span class="sxs-lookup"><span data-stu-id="f129c-121">Read from a template</span></span>  
 <span data-ttu-id="f129c-122">Đọc từ một mẫu mà bạn tạo trong [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] và sao chép vào [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] để bắt đầu lên kế hoạch dự án của bạn.</span><span class="sxs-lookup"><span data-stu-id="f129c-122">Read from a template that you created in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] and copied into [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] to start your project planning.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="f129c-123">[Tạo mẫu dự án (Project Service Automation)](../psa/create-project-template.md)</span><span class="sxs-lookup"><span data-stu-id="f129c-123">[Create a project template (Project Service Automation)](../psa/create-project-template.md)</span></span>  

1.  <span data-ttu-id="f129c-124">Từ thẻ **Project Service**, bấm vào **Đọc** > **Mẫu Dự án Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="f129c-124">From the **Project Service** tab, click **Read** > **Project Service Automation Project Template**.</span></span>  

2.  <span data-ttu-id="f129c-125">Chọn một mẫu dự án từ danh sách rồi bấm vào **Mở**.</span><span class="sxs-lookup"><span data-stu-id="f129c-125">Choose a project template from the list and then click **Open**.</span></span>  

    > [!NOTE]
    >  <span data-ttu-id="f129c-126">Theo mặc định, các tác vụ được sao chép từ mẫu vào Project được đặt ở chế độ đã lên lịch thủ công.</span><span class="sxs-lookup"><span data-stu-id="f129c-126">By default, the tasks that are copied from the template into Project are set as manually scheduled.</span></span>  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a><span data-ttu-id="f129c-127">Gán vai trò [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] cho nguồn lực dự án</span><span class="sxs-lookup"><span data-stu-id="f129c-127">Assign [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] roles to project resources</span></span>  

1.  <span data-ttu-id="f129c-128">Mở một dự án và bấm vào ruy băng **Tác vụ**.</span><span class="sxs-lookup"><span data-stu-id="f129c-128">Open a project and click the **Task** ribbon.</span></span>  

2.  <span data-ttu-id="f129c-129">Bấm vào menu **Biểu đồ Gantt** rồi chọn **Trang tính Nguồn lực**.</span><span class="sxs-lookup"><span data-stu-id="f129c-129">Click the **Gantt Chart** menu and then choose **Resource Sheet**.</span></span>  

3.  <span data-ttu-id="f129c-130">Trên Trang tính Nguồn lực, bấm vào menu thả xuống **Vai trò Nguồn lực trong Project Service** và chọn một vai trò trong Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="f129c-130">On the Resource Sheet, click the **Project Service Resource Role** drop-down menu and choose a Project Service Automation role.</span></span>  

## <a name="staff-your-project-with-resources"></a><span data-ttu-id="f129c-131">Cung cấp nguồn lực cho dự án của bạn</span><span class="sxs-lookup"><span data-stu-id="f129c-131">Staff your project with resources</span></span>  

1.  <span data-ttu-id="f129c-132">Từ thẻ Project Service, chọn một hàng và bấm vào **Tìm Nguồn lực**.</span><span class="sxs-lookup"><span data-stu-id="f129c-132">From the Project Service tab, select a row and click **Find Resources**.</span></span>  

2.  <span data-ttu-id="f129c-133">Trên màn hình **Đăng ký Nguồn lực**, chọn nguồn lực bạn muốn sử dụng cho dự án.</span><span class="sxs-lookup"><span data-stu-id="f129c-133">On the **Book Resource** screen, select the resource that you want to use for the project.</span></span>  

3.  <span data-ttu-id="f129c-134">Bấm vào **Đăng ký** rồi bấm vào **OK**.</span><span class="sxs-lookup"><span data-stu-id="f129c-134">Click **Book** and then click **OK**.</span></span>  

## <a name="publish-your-project"></a><span data-ttu-id="f129c-135">Phát hành dự án của bạn</span><span class="sxs-lookup"><span data-stu-id="f129c-135">Publish your project</span></span>  
<span data-ttu-id="f129c-136">Khi bạn hoàn tất lập kế hoạch dự án, bước tiếp theo là nhập và phát hành dự án trong [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="f129c-136">When your project planning is complete, the next step is to import and publish the project in to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

<span data-ttu-id="f129c-137">Dự án sẽ được nhập vào [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="f129c-137">The project will import into [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> <span data-ttu-id="f129c-138">Quy trình tạo nhóm và định giá sẽ được áp dụng.</span><span class="sxs-lookup"><span data-stu-id="f129c-138">The pricing and team generation process are applied.</span></span> <span data-ttu-id="f129c-139">Mở dự án trong [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], bạn sẽ thấy nhóm, ước tính dự án và cấu trúc phân tích công việc đã được tạo.</span><span class="sxs-lookup"><span data-stu-id="f129c-139">Open the project in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to see that the team, project estimates, and work breakdown structure has been generated.</span></span> <span data-ttu-id="f129c-140">Bảng sau hiển thị nơi để tìm thấy các kết quả:</span><span class="sxs-lookup"><span data-stu-id="f129c-140">The following table shows where to find the results:</span></span>


|                                                                                          |                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="f129c-141">**Biểu đồ Gantt**</span><span class="sxs-lookup"><span data-stu-id="f129c-141">**Gantt Chart**</span></span>   | <span data-ttu-id="f129c-142">Nhập vào màn hình [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Cấu trúc Phân tích Công việc**.</span><span class="sxs-lookup"><span data-stu-id="f129c-142">Imports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Work Breakdown Structure** screen.</span></span> |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="f129c-143">**Trang tính Nguồn lực**</span><span class="sxs-lookup"><span data-stu-id="f129c-143">**Resource Sheet**</span></span> |   <span data-ttu-id="f129c-144">Nhập vào màn hình [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Team Members**.</span><span class="sxs-lookup"><span data-stu-id="f129c-144">Imports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Team Members** screen.</span></span>   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="f129c-145">**Mức sử dụng**</span><span class="sxs-lookup"><span data-stu-id="f129c-145">**Use Usage**</span></span>    |    <span data-ttu-id="f129c-146">Nhập vào màn hình [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Ước tính dự án**.</span><span class="sxs-lookup"><span data-stu-id="f129c-146">Omports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Estimates** screen.</span></span>     |

<span data-ttu-id="f129c-147">**Để nhập và phát hành dự án của bạn**</span><span class="sxs-lookup"><span data-stu-id="f129c-147">**To import and publish your project**</span></span>  
1. <span data-ttu-id="f129c-148">Từ thẻ **Project Service**, bấm vào **Phát hành** > **Dự án Project Service Automation mới**.</span><span class="sxs-lookup"><span data-stu-id="f129c-148">From the **Project Service** tab, click **Publish** > **New Project Service Automation Project**.</span></span>  

2. <span data-ttu-id="f129c-149">Trên hộp thoại **Phát hành dự án mới trong Project Service**, nhập **Tên Dự án** và chọn **Khách hàng**.</span><span class="sxs-lookup"><span data-stu-id="f129c-149">On **Publish to a new project in Project Service** dialog box, enter the **Project Name** and select the **Customer**.</span></span>  

3. <span data-ttu-id="f129c-150">Bạn có thể chọn **Liên kết kế hoạch dự án với Project Service Automation** để liên kết tệp kế hoạch Project với Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="f129c-150">Optionally check the **Link project plan to Project Service Automation** to link the plan Project file to Project Service Automation.</span></span>  

4. <span data-ttu-id="f129c-151">Bấm vào **xuất bản**.</span><span class="sxs-lookup"><span data-stu-id="f129c-151">Click **Publish**.</span></span>  

   <span data-ttu-id="f129c-152">Việc liên kết tệp Project với [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] làm cho tệp Project thành tệp chính và đặt cấu trúc phân tích công việc trong [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] thành chỉ đọc.</span><span class="sxs-lookup"><span data-stu-id="f129c-152">Linking the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes the Project file the master and sets the work breakdown structure in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to read-only.</span></span>  <span data-ttu-id="f129c-153">Để thực hiện thay đổi cho kế hoạch dự án, bạn cần làm điều đó trong [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] và phát hành thay đổi dưới dạng cập nhật vào [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="f129c-153">In order to make changes to the project plan, you need to make them in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and publish them as updates to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

## <a name="edit-a-project-thats-been-imported"></a><span data-ttu-id="f129c-154">Chỉnh sửa dự án đã được nhập</span><span class="sxs-lookup"><span data-stu-id="f129c-154">Edit a project that’s been imported</span></span>  
 <span data-ttu-id="f129c-155">Để thực hiện thay đổi đối với một kế hoạch dự án đã được nhập vào [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], bạn có hai tùy chọn:</span><span class="sxs-lookup"><span data-stu-id="f129c-155">To make changes to a project plan that's been imported into [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you have two options:</span></span>  

- <span data-ttu-id="f129c-156">Mở tệp chính rồi chỉnh sửa kế hoạch đó trong [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="f129c-156">Open the master file and edit it in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

- <span data-ttu-id="f129c-157">Hủy liên kết tệp và chỉnh sửa tệp trực tiếp trong Project Service.</span><span class="sxs-lookup"><span data-stu-id="f129c-157">Unlink the file and edit it directly in Project Service.</span></span> <span data-ttu-id="f129c-158">Theo mặc định, một dự án được tải lên từ [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] sẽ bị khóa và chỉ có thể được chỉnh sửa trong Project.</span><span class="sxs-lookup"><span data-stu-id="f129c-158">By default, a project that’s been uploaded from [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] is locked and can only be edited in Project.</span></span> <span data-ttu-id="f129c-159">Để chỉnh sửa tệp trong [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], tệp đó phải được hủy liên kết.</span><span class="sxs-lookup"><span data-stu-id="f129c-159">To edit the file in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], the file has to be unlinked.</span></span>  

### <a name="edit-in-pn_microsoft_project"></a><span data-ttu-id="f129c-160">Chỉnh sửa trong [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span><span class="sxs-lookup"><span data-stu-id="f129c-160">Edit in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span></span>  

1. <span data-ttu-id="f129c-161">Từ menu chính, bấm vào **Project Service** > **Dự án**.</span><span class="sxs-lookup"><span data-stu-id="f129c-161">From the main menu, click **Project Service** > **Projects**.</span></span>  

2. <span data-ttu-id="f129c-162">Từ danh sách các dự án, mở dự án bạn đã tạo trong [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="f129c-162">From the list of projects, open the one you created in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

3. <span data-ttu-id="f129c-163">Bấm vào **Mở trong MS Project** từ ruy băng.</span><span class="sxs-lookup"><span data-stu-id="f129c-163">Click **Open in MS Project** from the ribbon.</span></span> <span data-ttu-id="f129c-164">Thao tác này sẽ mở tệp chính được liên kết trong [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="f129c-164">This will open the linked master file in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a><span data-ttu-id="f129c-165">Hủy liên kết tệp và chỉnh sửa tệp trong [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service</span><span class="sxs-lookup"><span data-stu-id="f129c-165">Unlink a file and edit in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service</span></span>  

1. <span data-ttu-id="f129c-166">Từ menu chính, bấm vào **Project Service** > **Dự án**.</span><span class="sxs-lookup"><span data-stu-id="f129c-166">From the main menu, click **Project Service** > **Projects**.</span></span>  

2. <span data-ttu-id="f129c-167">Từ danh sách các dự án, mở dự án bạn đã tạo trong [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="f129c-167">From the list of projects, open the one you created in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

3. <span data-ttu-id="f129c-168">Bấm vào **Hủy liên kết khỏi MS Project** từ ruy băng.</span><span class="sxs-lookup"><span data-stu-id="f129c-168">Click **Unlink from MS Project** from the ribbon.</span></span>  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a><span data-ttu-id="f129c-169">Tải một tệp Project lên SharePoint hoặc Nhóm Office</span><span class="sxs-lookup"><span data-stu-id="f129c-169">Upload a Project file to SharePoint or Office Groups</span></span>  
 <span data-ttu-id="f129c-170">Bạn có thể tải tệp Project lên SharePoint và tìm thấy tệp đó trong Tài liệu Được liên kết cho dự án [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] của bạn.</span><span class="sxs-lookup"><span data-stu-id="f129c-170">You can upload your Project file to SharePoint and find it under the Associated Documents for your [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  <span data-ttu-id="f129c-171">Bạn cần phải yêu cầu quản trị viên đặt cấu hình tính năng quản lý tài liệu SharePoint rồi bật tính năng đó cho thực thể Dự án.</span><span class="sxs-lookup"><span data-stu-id="f129c-171">You need to have your administrator configure SharePoint document management and turn it on for the Project entity.</span></span> 

 <span data-ttu-id="f129c-172">Bạn cũng có thể tải tệp Project của mình lên [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] nếu đã thiết lập Nhóm Office.</span><span class="sxs-lookup"><span data-stu-id="f129c-172">You can also upload your Project file to [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] if you have Office Groups set up.</span></span>

### <a name="upload-a-file-for-sharepoint"></a><span data-ttu-id="f129c-173">Tải tệp lên cho SharePoint</span><span class="sxs-lookup"><span data-stu-id="f129c-173">Upload a file for SharePoint</span></span>  

1. <span data-ttu-id="f129c-174">Từ menu chính, bấm vào **Project Service** > **Tải lên**.</span><span class="sxs-lookup"><span data-stu-id="f129c-174">From the main menu, click **Project Service** > **Upload**.</span></span>  

2. <span data-ttu-id="f129c-175">Chọn **Lên Tài liệu Dự án trong Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="f129c-175">Select **To Project Service Automation Project Documents**.</span></span>  

3. <span data-ttu-id="f129c-176">Trên hộp thoại **Bật Mở trong [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**, hãy chọn **Có** hoặc **Không**.</span><span class="sxs-lookup"><span data-stu-id="f129c-176">On the **Enable Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dialog, select **Yes** or **No**.</span></span>  

   - <span data-ttu-id="f129c-177">Nếu bạn bấm vào **Có**, bạn có thể chọn nút **Mở trong [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** trong Project Service Automation, chạy [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] rồi tải tệp Dự án từ thư viện tài liệu SharePoint.</span><span class="sxs-lookup"><span data-stu-id="f129c-177">If you click **Yes**, you'll be able select the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button in Project Service Automation, launch [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], and load the Project file from the SharePoint document library.</span></span>  

   - <span data-ttu-id="f129c-178">Nếu bạn bấm vào **Không**, liên kết cho nút **Mở trong [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** sẽ không hoạt động.</span><span class="sxs-lookup"><span data-stu-id="f129c-178">If you click **No**, the link for the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button won't work.</span></span>  

4. <span data-ttu-id="f129c-179">Bạn có thể tìm thấy tệp [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] trong [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] trong **Tài liệu** cho dự án [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] cụ thể.</span><span class="sxs-lookup"><span data-stu-id="f129c-179">The [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] file can be found in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Documents** for the specific [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  

### <a name="upload-a-file-for-office-groups"></a><span data-ttu-id="f129c-180">Tải lên tệp dành cho Nhóm Office</span><span class="sxs-lookup"><span data-stu-id="f129c-180">Upload a file for Office Groups</span></span>  

1. <span data-ttu-id="f129c-181">Từ menu chính, bấm vào **Project Service** > **Tải lên**.</span><span class="sxs-lookup"><span data-stu-id="f129c-181">From the main menu, click **Project Service** > **Upload**.</span></span>  

2. <span data-ttu-id="f129c-182">Chọn **Lên Tài liệu Dự án trong Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="f129c-182">Select **To Project Service Automation Project Documents**.</span></span>  

3. <span data-ttu-id="f129c-183">Trên hộp thoại **Bật Mở trong [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**, hãy chọn **Có** hoặc **Không**.</span><span class="sxs-lookup"><span data-stu-id="f129c-183">On the **Enable Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dialog, select **Yes** or **No**.</span></span>  

   - <span data-ttu-id="f129c-184">Nếu bấm vào **Có**, bạn sẽ có thể chọn nút **Mở trong [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** trong Project Service Automation, chạy [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] rồi tải tệp Dự án từ thư viện tài liệu SharePoint.</span><span class="sxs-lookup"><span data-stu-id="f129c-184">If you click **Yes**, you'll be able to select the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button in Project Service Automation, launch [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], and load the Project file from the SharePoint document library.</span></span>  

   - <span data-ttu-id="f129c-185">Nếu bạn bấm vào **Không**, liên kết cho nút **Mở trong [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** sẽ không hoạt động.</span><span class="sxs-lookup"><span data-stu-id="f129c-185">If you click **No**, the link for the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button won't work.</span></span>  

4. <span data-ttu-id="f129c-186">Bạn có thể tìm thấy tệp [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] trong [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] trong **Tài liệu** cho dự án [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] cụ thể.</span><span class="sxs-lookup"><span data-stu-id="f129c-186">The [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] file can be found in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Documents** for the specific [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  

## <a name="publish--your-project-as-a-template"></a><span data-ttu-id="f129c-187">Phát hành dự án của bạn dưới dạng mẫu</span><span class="sxs-lookup"><span data-stu-id="f129c-187">Publish  your project as a template</span></span>  
 <span data-ttu-id="f129c-188">Bạn có thể lưu dự án của mình và tái sử dụng bằng cách lưu dự án đó làm mẫu dự án trong [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="f129c-188">You can save your project and reuse it by saving it as a project template in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  <span data-ttu-id="f129c-189">Mẫu dự án là các kế hoạch dự án có thể tái sử dụng trong [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="f129c-189">Project templates are reusable project plans in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="f129c-190">[Tạo mẫu dự án (Project Service Automation)](../psa/create-project-template.md)</span><span class="sxs-lookup"><span data-stu-id="f129c-190">[Create a project template (Project Service Automation)](../psa/create-project-template.md)</span></span>  

1. <span data-ttu-id="f129c-191">Từ thẻ **Project Service**, bấm vào **Phát hành** > **Mẫu Dự án Project Service Automation mới**.</span><span class="sxs-lookup"><span data-stu-id="f129c-191">From the **Project Service** tab, click **Publish** > **New Project Service Automation Project Template**.</span></span>  

2. <span data-ttu-id="f129c-192">Trên hộp thoại **Phát hành dự án mới trong mẫu Project Service**, nhập **Tên mẫu dự án**.</span><span class="sxs-lookup"><span data-stu-id="f129c-192">On the **Publish to a new project in Project Service template** dialog box, enter the **Project template name**.</span></span>  

3. <span data-ttu-id="f129c-193">Hoặc, chọn **Liên kết kế hoạch dự án với Project Service Automation** để liên kết tệp Dự án với [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="f129c-193">Optionally, check the **Link project plan to Project Service Automation** to link the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

4. <span data-ttu-id="f129c-194">Bấm vào **xuất bản**.</span><span class="sxs-lookup"><span data-stu-id="f129c-194">Click **Publish**.</span></span>  

<span data-ttu-id="f129c-195">Việc liên kết tệp Project với [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] làm cho tệp Project thành tệp chính và đặt cấu trúc phân tích công việc trong mẫu [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] thành chỉ đọc.</span><span class="sxs-lookup"><span data-stu-id="f129c-195">Linking the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes the Project file the master and sets the work breakdown structure in the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] template to read-only.</span></span>  <span data-ttu-id="f129c-196">Để thực hiện thay đổi cho kế hoạch dự án, bạn cần làm điều đó trong [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] và phát hành thay đổi dưới dạng cập nhật vào [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="f129c-196">In order to make changes to the project plan, you need to make them in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and publish them as updates to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>

### <a name="see-also"></a><span data-ttu-id="f129c-197">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="f129c-197">See Also</span></span>  
 [<span data-ttu-id="f129c-198">Hướng dẫn của Quản lý Dự án</span><span class="sxs-lookup"><span data-stu-id="f129c-198">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
