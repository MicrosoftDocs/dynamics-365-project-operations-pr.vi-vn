---
title: Theo dõi trạng thái của dự án
description: Làm cách nào để theo dõi tình trạng dự án trong Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: d57f33cdf240db4cae1f33fe962173790fe0fe7f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281954"
---
# <a name="track-a-projects-status-project-service"></a><span data-ttu-id="23598-103">Theo dõi tình trạng dự án (Project Service)</span><span class="sxs-lookup"><span data-stu-id="23598-103">Track a project’s status (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="23598-104">Sử dụng [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] để theo dõi tiến độ dự án của khách hàng.</span><span class="sxs-lookup"><span data-stu-id="23598-104">Use the [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] to track the progress of a client’s project.</span></span>  

<span data-ttu-id="23598-105">Về khía cạnh tiến độ cam kết, các giai đoạn dự án sẽ cập nhật để phản ánh giai đoạn cam kết:</span><span class="sxs-lookup"><span data-stu-id="23598-105">As the engagement progresses, the project stages update to reflect the stage of the engagement:</span></span>  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   <span data-ttu-id="23598-106">**Mới**</span><span class="sxs-lookup"><span data-stu-id="23598-106">**New**</span></span>    | <span data-ttu-id="23598-107">Khi bạn tạo một dự án, giai đoạn sẽ được đặt thành **Mới**.</span><span class="sxs-lookup"><span data-stu-id="23598-107">When you create a project, the stage is set to **New**.</span></span> <span data-ttu-id="23598-108">Nếu bạn đã tạo dự án từ một mẫu, ở giai đoạn này, dự án có thể có dữ liệu về lịch trình, ước tính và nhóm.</span><span class="sxs-lookup"><span data-stu-id="23598-108">If you created the project from a template, at this stage the project may have a schedule, estimates, and team data.</span></span> <span data-ttu-id="23598-109">Nếu không, đó sẽ là bản phác thảo của dự án và bạn cần phải nhập các thành phần còn lại của dự án theo cách thủ công.</span><span class="sxs-lookup"><span data-stu-id="23598-109">Otherwise, it will be the outline of the project and you need to manually enter the rest of the project components.</span></span> |
|  <span data-ttu-id="23598-110">**Báo giá**</span><span class="sxs-lookup"><span data-stu-id="23598-110">**Quote**</span></span>   |      <span data-ttu-id="23598-111">Khi bạn liên kết một dự án với một báo giá hoặc tạo dự án từ báo giá, giai đoạn dự án được đặt thành **Báo giá** và ngày bắt đầu và kết thúc ước tính cũng sẽ được cập nhật.</span><span class="sxs-lookup"><span data-stu-id="23598-111">When you associate a project to a quote or create it from a quote, the project stage is set to **Quote**, and the estimated start and end datesare updated as well.</span></span> <span data-ttu-id="23598-112">Khi dự án đang trong giai đoạn báo giá, các chi tiết về báo giá sẽ hiển thị trên tab **Kinh doanh** trên trang **Dự án**.</span><span class="sxs-lookup"><span data-stu-id="23598-112">When the project is in the quote stage, details on the quote display on the **Sales** tab on the **Project** page.</span></span>      |
|   <span data-ttu-id="23598-113">**Kế hoạch**</span><span class="sxs-lookup"><span data-stu-id="23598-113">**Plan**</span></span>   |                                     <span data-ttu-id="23598-114">Khi báo giá được liên kết với một dự án của bạn giành chiến thắng thì tiến độ cam kết cho giai đoạn hợp đồng, giai đoạn dự án sẽ cập nhật thành **Kế hoạch**.</span><span class="sxs-lookup"><span data-stu-id="23598-114">When you win a quote associated with a project, and when the engagement progresses to the contract stage, the project stage updates to **Plan**.</span></span> <span data-ttu-id="23598-115">Chi tiết hợp đồng sẽ hiển thị trên tab **Kinh doanh** trên trang **Dự án**.</span><span class="sxs-lookup"><span data-stu-id="23598-115">Contract details display on the **Sales** tab on the **Project** page.</span></span>                                      |
| <span data-ttu-id="23598-116">**Hoàn thành**</span><span class="sxs-lookup"><span data-stu-id="23598-116">**Complete**</span></span> |                    <span data-ttu-id="23598-117">Khi đã hoàn tất công việc dự án, bạn có thể chuyển giai đoạn thành **Hoàn tất**.</span><span class="sxs-lookup"><span data-stu-id="23598-117">When the project work is complete, you can flip the stage to **Complete**.</span></span> <span data-ttu-id="23598-118">Khi giai đoạn dự án được đặt thành hoàn tất, mọi người sẽ hiểu rằng các công việc đã hoàn thành 100% nhưng dự án vẫn được để mở cho việc ghi lại bất kỳ mục nhập chi phí hoặc thời gian đang chờ xử lý nào.</span><span class="sxs-lookup"><span data-stu-id="23598-118">When the project stage is set to complete, it’s understood that the work is 100% complete but the project is kept open for any pending time or expense entries to be recorded.</span></span>                     |
|  <span data-ttu-id="23598-119">**Đóng**</span><span class="sxs-lookup"><span data-stu-id="23598-119">**Close**</span></span>   |           <span data-ttu-id="23598-120">Khi tất cả các giao dịch đã được ghi lại trên dự án và bạn không muốn ghi thêm bất kỳ chi tiết nào nữa thì bạn có thể đặt giai đoạn thành **Đóng** theo cách thủ công.</span><span class="sxs-lookup"><span data-stu-id="23598-120">When all transactions have been recorded on the project and you don't expect any more to be logged, you can manually set the stage to **Close**.</span></span> <span data-ttu-id="23598-121">Khi dự án được đặt thành **Đóng**, bạn không thể ghi thêm bất kỳ giao dịch nào khác trên dự án và dự án sẽ ở trạng thái chỉ đọc.</span><span class="sxs-lookup"><span data-stu-id="23598-121">When the project is set to **Close**, you can’t log any more transactions on the project and the project will be read only.</span></span>           |

## <a name="to-track-a-projects-status"></a><span data-ttu-id="23598-122">Cách theo dõi trạng thái của dự án</span><span class="sxs-lookup"><span data-stu-id="23598-122">To track a project’s status</span></span>  

1.  <span data-ttu-id="23598-123">Đi tới **Project Service > Dự án**.</span><span class="sxs-lookup"><span data-stu-id="23598-123">Go to **Project Service > Projects**.</span></span>  

2.  <span data-ttu-id="23598-124">Bấm vào dự án mà bạn muốn làm việc.</span><span class="sxs-lookup"><span data-stu-id="23598-124">Click the project you want to work on.</span></span>  

3.  <span data-ttu-id="23598-125">Trong thanh ở đầu màn hình, chọn mũi tên xuống bên cạnh tên dự án, sau đó bấm vào **Theo dõi Dự án**.</span><span class="sxs-lookup"><span data-stu-id="23598-125">In the bar across the top of the screen, select the down arrow next to the project name, and then click **Project Tracking**.</span></span>  

4.  <span data-ttu-id="23598-126">Chọn **Theo dõi Nỗ lực** hoặc **Theo dõi Chi phí** trong danh sách thả xuống ở trên danh sách tác vụ.</span><span class="sxs-lookup"><span data-stu-id="23598-126">Select **Effort Tracking** or **Cost Tracking** in the drop-down list above the task list.</span></span>  

5.  <span data-ttu-id="23598-127">Bấm đúp vào bất cứ tác vụ nào để chỉnh sửa.</span><span class="sxs-lookup"><span data-stu-id="23598-127">Double-click any task to edit it.</span></span> <span data-ttu-id="23598-128">Bạn cũng có thể di chuyển hoặc thay đổi kích thước các thanh trong biểu đồ Gantt để thay đổi thời gian và tiến bộ cho một nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="23598-128">You can also move or resize the bars in the Gantt chart to change the time and progress for a task.</span></span>  

### <a name="see-also"></a><span data-ttu-id="23598-129">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="23598-129">See Also</span></span>  
 [<span data-ttu-id="23598-130">Hướng dẫn của Quản lý Dự án</span><span class="sxs-lookup"><span data-stu-id="23598-130">Project Manager Guide</span></span>](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]