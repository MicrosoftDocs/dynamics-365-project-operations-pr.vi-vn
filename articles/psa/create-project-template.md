---
title: Tạo mẫu dự án
description: Làm cách nào để tạo mẫu dự án trong Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 700d1bb1fd7299b49b6c6f8e4d84d14bc1d52c1a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087121"
---
# <a name="create-a-project-template-project-service"></a><span data-ttu-id="f0b85-103">Tạo mẫu dự án (Project Service)</span><span class="sxs-lookup"><span data-stu-id="f0b85-103">Create a project template (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="f0b85-104">Mẫu dự án tiết kiệm thời gian cho bạn nếu công ty của bạn thường xuyên đấu thầu các loại dự án giống nhau.</span><span class="sxs-lookup"><span data-stu-id="f0b85-104">Project templates save you time if your company regularly bids on similar types of projects.</span></span> <span data-ttu-id="f0b85-105">Các mẫu này cung cấp một bộ tiêu chuẩn cho vai trò và thời gian ước tính cho một loại dự án.</span><span class="sxs-lookup"><span data-stu-id="f0b85-105">They provide a standard set of roles and estimated hours for a type of project.</span></span> <span data-ttu-id="f0b85-106">Giám đốc khách hàng và giám đốc dự án có thể tạo các dự án dựa trên mẫu dự án hoặc họ có thể sao chép mẫu và tự tạo mẫu riêng.</span><span class="sxs-lookup"><span data-stu-id="f0b85-106">Account managers and project managers can create projects based on a project template, or they can copy the template and make one of their own.</span></span>  
  
## <a name="components-of-project-template"></a><span data-ttu-id="f0b85-107">Các thành phần của mẫu dự án</span><span class="sxs-lookup"><span data-stu-id="f0b85-107">Components of project template</span></span>
 <span data-ttu-id="f0b85-108">Một mẫu dự án bao gồm ba thành phần:</span><span class="sxs-lookup"><span data-stu-id="f0b85-108">A project template consists of three components:</span></span>  
  
- <span data-ttu-id="f0b85-109">**Cấu trúc phân tích công việc** : Cấu trúc phân tích công việc trong một mẫu dự án có tập hợp các yếu tố giống như trong dự án.</span><span class="sxs-lookup"><span data-stu-id="f0b85-109">**Work breakdown structure** : A work breakdown structure in a project template has the same set of elements as in the project.</span></span> <span data-ttu-id="f0b85-110">Bạn có thể tạo một hệ thống cấp bậc nhiệm vụ, liên kết vai trò với nhiệm vụ, xác định các thuộc tính lịch trình, thiết lập quan hệ phụ thuộc và xem tất cả dữ liệu trong Gantt.</span><span class="sxs-lookup"><span data-stu-id="f0b85-110">You can create a task hierarchy, associate roles to task, define schedule attributes, set dependencies and view all the data in the Gantt.</span></span> <span data-ttu-id="f0b85-111">Cấu trúc phân tích công việc trong mẫu dự án cũng hỗ trợ chế độ nhiệm vụ cho mỗi nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="f0b85-111">The work breakdown structure in project templates also support task modes for each task.</span></span> <span data-ttu-id="f0b85-112">Tạo lịch trình công việc cho mẫu dự án và dự án là giống nhau.</span><span class="sxs-lookup"><span data-stu-id="f0b85-112">There is no difference between a project template and a project when creating work schedule.</span></span>  
  
- <span data-ttu-id="f0b85-113">**Dự toán dự án** : Dự toán dự án trong các mẫu hoạt động giống như trong các dự án, ngoại trừ bảng giá để đặt mặc định chi phí và giá bán luôn là chi phí và bảng giá bán mặc định được xác định trong tham số [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="f0b85-113">**Project estimates** : Project estimates in templates work the same way as they do in projects, except the price lists for defaulting the cost and sales prices are always the default cost and sales price lists defined in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] parameters.</span></span> <span data-ttu-id="f0b85-114">Các tính năng còn lại giống với các tính năng trong một dự án.</span><span class="sxs-lookup"><span data-stu-id="f0b85-114">The rest of the functionality is the same as in a project.</span></span>  
  
- <span data-ttu-id="f0b85-115">**Hình thành nhóm dự án** : Khi hình thành nhóm dự án cho mẫu dự án, bạn có thể đặt lịch một nguồn lực được nêu tên trong một mẫu.</span><span class="sxs-lookup"><span data-stu-id="f0b85-115">**Project team formation** : When forming a project team for a project template, you can’t book a named resource in a template.</span></span> <span data-ttu-id="f0b85-116">Bạn có thể sử dụng **Tạo Nhóm Dự án** trong cấu trúc phân tích công việc để tạo ra một tập hợp các nguồn lực chung.</span><span class="sxs-lookup"><span data-stu-id="f0b85-116">You can use **Generate Project Team** in the work breakdown structure to generate a set of generic resources.</span></span> <span data-ttu-id="f0b85-117">Bạn cũng có thể chỉ định các kỹ năng và mức độ thành thạo cần thiết cho nguồn lực chung.</span><span class="sxs-lookup"><span data-stu-id="f0b85-117">You can also specify required skills and proficiencies for generic resources.</span></span> <span data-ttu-id="f0b85-118">Bạn không thể thay thế nguồn lực chung bằng nguồn lực có thể đặt lịch trong mẫu dự án.</span><span class="sxs-lookup"><span data-stu-id="f0b85-118">You can’t substitute a generic resource with a bookable resource in project templates.</span></span>  
  
## <a name="create-a-project-from-a-template"></a><span data-ttu-id="f0b85-119">Tạo dự án từ mẫu</span><span class="sxs-lookup"><span data-stu-id="f0b85-119">Create a project from a template</span></span>  
 <span data-ttu-id="f0b85-120">Bạn có thể tạo một dự án từ mẫu theo các cách sau đây:</span><span class="sxs-lookup"><span data-stu-id="f0b85-120">You can create a project from a template in these following ways:</span></span>  
  
-   <span data-ttu-id="f0b85-121">Khi tạo dự án từ báo giá, bạn có thể chọn một mẫu dự án trong biểu mẫu tạo nhanh dự án.</span><span class="sxs-lookup"><span data-stu-id="f0b85-121">When creating a project from the quote, you can choose a project template in the project quick create form.</span></span>  
  
-   <span data-ttu-id="f0b85-122">Khi tạo một dự án bằng cách bấm vào **Dự án Mới** , biểu mẫu dự án sẽ hiển thị trước khi bạn lưu bản ghi.</span><span class="sxs-lookup"><span data-stu-id="f0b85-122">When creating a project by clicking **New Project** , the project form displays before you save the record.</span></span> <span data-ttu-id="f0b85-123">Từ đây, bạn có thể bấm vào trường **Chọn một mẫu** để chọn từ danh sách các mẫu dự án được xác định trước trong tổ chức của bạn.</span><span class="sxs-lookup"><span data-stu-id="f0b85-123">From here, you can click **Pick a template** field to choose from the list of pre-defined project templates in your organization.</span></span>  
  
-   <span data-ttu-id="f0b85-124">Bấm vào **Tạo dự án từ mẫu** trên trang **Mẫu Dự án** để tạo dự án từ mẫu.</span><span class="sxs-lookup"><span data-stu-id="f0b85-124">Click **Create project from a template** on the **Project Template** page to create a project from the template.</span></span>  
  
## <a name="copying-components-of-a-template-to-a-project"></a><span data-ttu-id="f0b85-125">Sao chép các thành phần của một mẫu vào dự án</span><span class="sxs-lookup"><span data-stu-id="f0b85-125">Copying components of a template to a project</span></span>  
 <span data-ttu-id="f0b85-126">Khi sao chép các thành phần của mẫu vào dự án, bạn cần lưu ý một số nội dung sau.</span><span class="sxs-lookup"><span data-stu-id="f0b85-126">When you copy components of a template into a project, there are a few things you should know about.</span></span>  
  
 <span data-ttu-id="f0b85-127">**Sao chép một cấu trúc phân tích công việc** : Khi sao chép cấu trúc phân tích công việc từ một mẫu dự án, nếu dự án có một lịch dự án khác với mẫu, thì giờ làm việc từ lịch của dự án sẽ được áp dụng cho lịch trình công việc.</span><span class="sxs-lookup"><span data-stu-id="f0b85-127">**Copying a work breakdown structure** : When you copy the work breakdown structure from a project template, if the project has a different project calendar than the template, the work hours from the project’s calendar will be applied to the schedule of tasks.</span></span> <span data-ttu-id="f0b85-128">Điều này điều chỉnh lịch trình về lịch dự án được hỗ trợ.</span><span class="sxs-lookup"><span data-stu-id="f0b85-128">This adjusts the schedule to the backing project calendar.</span></span> <span data-ttu-id="f0b85-129">Tương tự như vậy, nhiệm vụ đầu tiên trên cấu trúc phân tích công việc sẽ lấy ngày bắt đầu của dự án, do đó, phần còn lại của lịch trình hệ thống cấp bậc nhiệm vụ được cập nhật dựa trên khoảng thời gian và thành phần phụ thuộc được chỉ ra trong cấu trúc phân tích công việc của mẫu.</span><span class="sxs-lookup"><span data-stu-id="f0b85-129">Similarly, the first task on the work breakdown structure takes the project’s start date, so the rest of the task hierarchy schedule is updated based on the duration and dependencies specified in the template’s work breakdown structure.</span></span>  
  
 <span data-ttu-id="f0b85-130">**Sao chép dự toán dự án** : Khi bạn sao chép giữa các dòng dự toán của dự án, bảng giá được cập nhật dựa trên đơn vị sở hữu của dự án đối với bảng giá vốn và khách hàng đối với bảng giá bán.</span><span class="sxs-lookup"><span data-stu-id="f0b85-130">**Copying project estimates** : When you copy across project estimate lines, price lists are updated based on the owning unit of the project for the cost price list and customer for the sales price list.</span></span> <span data-ttu-id="f0b85-131">Chi phí sản xuất và giá bán được xác định từ các bảng giá này trên các dự án được liên kết với thực thể bán hàng.</span><span class="sxs-lookup"><span data-stu-id="f0b85-131">The unit cost and sales prices are determined from these price lists on projects that are associated to a sales entity.</span></span>  
  
 <span data-ttu-id="f0b85-132">**Sao chép một nhóm dự án** : Khi bạn sao chép nhóm dự án từ mẫu sang một dự án, các nguồn lực chung được sao chép cùng với các kỹ năng và mức độ thành thạo được xác định trong mẫu.</span><span class="sxs-lookup"><span data-stu-id="f0b85-132">**Copying a project team** : When you copy the project team from the template to a project, the generic resources are copied across, along with the skills and proficiencies defined in the template.</span></span> <span data-ttu-id="f0b85-133">Việc phân công nguồn lực chung cũng được duy trì như trong mẫu dự án.</span><span class="sxs-lookup"><span data-stu-id="f0b85-133">Generic resource assignments are also maintained as in the project template.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="f0b85-134">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="f0b85-134">See Also</span></span>  
 [<span data-ttu-id="f0b85-135">Hướng dẫn của Quản lý Dự án</span><span class="sxs-lookup"><span data-stu-id="f0b85-135">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
