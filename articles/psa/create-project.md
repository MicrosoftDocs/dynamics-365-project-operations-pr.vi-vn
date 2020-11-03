---
title: Tạo dự án
description: Làm cách nào để tạo dự án trong Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/13/2020
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
ms.openlocfilehash: a1a229641d0694311ecb7019e3915d0e8e6783c3
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087120"
---
# <a name="create-a-project-project-service"></a><span data-ttu-id="e2e9a-103">Tạo dự án (Project Service)</span><span class="sxs-lookup"><span data-stu-id="e2e9a-103">Create a project (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="e2e9a-104">Tạo dự án bằng chức năng [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] trong [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] khi bạn muốn tạo cơ hội, báo giá hoặc hợp đồng cho dịch vụ dựa trên dự án.</span><span class="sxs-lookup"><span data-stu-id="e2e9a-104">Create a project using the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] when you want to create an opportunity, quote, or contract for project-based services.</span></span> <span data-ttu-id="e2e9a-105">Các chức năng [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] giúp bạn quản lý dự án của mình từ cơ hội cho đến khi hoàn thành.</span><span class="sxs-lookup"><span data-stu-id="e2e9a-105">The [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities help you manage your project from opportunity through completion.</span></span> <span data-ttu-id="e2e9a-106">Khi bạn tạo dự án, bạn cũng sẽ tạo cấu trúc phân tích công việc, điều này tác động đến báo giá, ước tính chi phí và quản lý nguồn lực.</span><span class="sxs-lookup"><span data-stu-id="e2e9a-106">When you create a project, you’ll also create a work breakdown structure, which affects your quotes, cost estimates, and resource management.</span></span>  
  
1.  <span data-ttu-id="e2e9a-107">Đi tới **Project Service > Dự án**.</span><span class="sxs-lookup"><span data-stu-id="e2e9a-107">Go to **Project Service > Projects**.</span></span>  
  
2.  <span data-ttu-id="e2e9a-108">Bấm vào **Dự án mới**.</span><span class="sxs-lookup"><span data-stu-id="e2e9a-108">Click **New Project**.</span></span>  
  
3.  <span data-ttu-id="e2e9a-109">Trong vùng **Tóm tắt** , nhập tên cho dự án của bạn, sau đó điền càng nhiều thông tin chi tiết càng tốt.</span><span class="sxs-lookup"><span data-stu-id="e2e9a-109">In the **Summary** area, enter a name for your project, and then fill in as many of the details as you can.</span></span> <span data-ttu-id="e2e9a-110">Các mục được đánh dấu bằng dấu hoa thị (\*) màu đỏ là bắt buộc.</span><span class="sxs-lookup"><span data-stu-id="e2e9a-110">Items marked with a red asterisk (\*) are required.</span></span>  
  
4.  <span data-ttu-id="e2e9a-111">Bấm vào **Lưu** để tạo dự án để bạn có thể tiếp tục chỉnh sửa.</span><span class="sxs-lookup"><span data-stu-id="e2e9a-111">Click **Save** to create your project so you can continue editing it.</span></span>  
  
<span data-ttu-id="e2e9a-112">Tiếp theo, bạn sẽ tạo một cấu trúc phân tích công việc cho dự án của bạn để xác định nhiệm vụ, thời gian và vai trò của nguồn lực cần thiết cho dự án.</span><span class="sxs-lookup"><span data-stu-id="e2e9a-112">Next, you’ll create a work breakdown structure for your project to define the tasks, timing, and resource roles needed for the project.</span></span>  

> [!NOTE]
> <span data-ttu-id="e2e9a-113">Khi lên lịch, Project Service Automation tôn trọng múi giờ của mẫu **Giờ làm việc** được áp dụng.</span><span class="sxs-lookup"><span data-stu-id="e2e9a-113">When scheduling, Project Service Automation respects the time zone of the applied **Work Hour** template.</span></span> <span data-ttu-id="e2e9a-114">Tuy nhiên, khi xem các nhiệm vụ lịch trình, ngày bắt đầu và ngày kết thúc của một nhiệm vụ sẽ được hiển thị theo múi giờ của người dùng.</span><span class="sxs-lookup"><span data-stu-id="e2e9a-114">However, when viewing the schedule tasks, the start and end dates of a task will be displayed in the user's time zone.</span></span> <span data-ttu-id="e2e9a-115">Điều này áp dụng cho các dạng xem theo giai đoạn thời gian trong biểu mẫu **Dự án**.</span><span class="sxs-lookup"><span data-stu-id="e2e9a-115">This applies to other time-phased views in the **Project** form.</span></span> <span data-ttu-id="e2e9a-116">Nếu múi giờ của người dùng không khớp với múi giờ của mẫu giờ làm việc được áp dụng cho dự án, một cảnh báo giải thích sự khác biệt sẽ xảy ra.</span><span class="sxs-lookup"><span data-stu-id="e2e9a-116">If the user's time zone does not match the time zone of the work hour template applied to the project, a warning which explains the difference will occur.</span></span> 
  
### <a name="see-also"></a><span data-ttu-id="e2e9a-117">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="e2e9a-117">See Also</span></span>  
 [<span data-ttu-id="e2e9a-118">Hướng dẫn của Quản lý Dự án</span><span class="sxs-lookup"><span data-stu-id="e2e9a-118">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
