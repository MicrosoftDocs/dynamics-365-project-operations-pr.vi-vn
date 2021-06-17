---
title: Mẫu dự án
description: Chủ đề này cung cấp thông tin về cách sử dụng mẫu dự án để thiết lập dự án nhanh chóng.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: bedcbc76d932a81e0c78bb58ce6a161446a26dde
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998302"
---
# <a name="project-templates"></a><span data-ttu-id="4cfdd-103">Mẫu dự án</span><span class="sxs-lookup"><span data-stu-id="4cfdd-103">Project templates</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="4cfdd-104">Mẫu dự án là một khuôn khổ được xác định trước giúp bạn nhanh chóng và dễ dàng bắt đầu một dự án.</span><span class="sxs-lookup"><span data-stu-id="4cfdd-104">A project template is a predefined framework that helps you quickly and easily start a project.</span></span> <span data-ttu-id="4cfdd-105">Bạn có thể sử dụng một mẫu được xác định trước để tạo dự án mới chỉ bằng một cú bấm chuột.</span><span class="sxs-lookup"><span data-stu-id="4cfdd-105">You can use a predefined template to create a new project with a single click.</span></span> <span data-ttu-id="4cfdd-106">Như đối với dự án, bạn phải xác định điều kiện tiên quyết cho mẫu dự án.</span><span class="sxs-lookup"><span data-stu-id="4cfdd-106">As for projects, you must define the prerequisites for project templates.</span></span> <span data-ttu-id="4cfdd-107">Bạn phải xác định lịch dự án cho từng mẫu dự án, và vai trò cũng như bảng giá phải được xác định trước trong tổ chức để các thành phần của mẫu có dữ liệu hữu ích.</span><span class="sxs-lookup"><span data-stu-id="4cfdd-107">You must define a project calendar for each project template, and roles and price lists must be predefined in the organization, so that the components of the template have useful data.</span></span>

<span data-ttu-id="4cfdd-108">Mẫu dự án bao gồm ba thành phần: lịch trình, ước tính dự án và các thành viên nhóm dự án.</span><span class="sxs-lookup"><span data-stu-id="4cfdd-108">A project template consists of three components: a schedule, project estimates, and project team members.</span></span>

## <a name="schedule"></a><span data-ttu-id="4cfdd-109">Lịch trình</span><span class="sxs-lookup"><span data-stu-id="4cfdd-109">Schedule</span></span>

<span data-ttu-id="4cfdd-110">Lịch trình trong mẫu dự án có cùng bộ thành phần như lịch trình trong dự án.</span><span class="sxs-lookup"><span data-stu-id="4cfdd-110">A schedule in a project template has the same set of elements as a schedule in a project.</span></span> <span data-ttu-id="4cfdd-111">Bạn có thể tạo một hệ thống cấp bậc nhiệm vụ, liên kết vai trò với nhiệm vụ, xác định thuộc tính lịch trình và đặt mức phụ thuộc.</span><span class="sxs-lookup"><span data-stu-id="4cfdd-111">You can create a task hierarchy, associate roles with tasks, define schedule attributes, and set dependencies.</span></span> <span data-ttu-id="4cfdd-112">Lịch trình trong mẫu dự án cũng hỗ trợ các chế độ nhiệm vụ cho từng nhiệm vụ.</span><span class="sxs-lookup"><span data-stu-id="4cfdd-112">A schedule in a project template also supports task modes for each task.</span></span> <span data-ttu-id="4cfdd-113">Do đó, lịch trình hỗ trợ các công cụ lập lịch.</span><span class="sxs-lookup"><span data-stu-id="4cfdd-113">Therefore, it supports the scheduling engine.</span></span> <span data-ttu-id="4cfdd-114">Bạn phải liên kết lịch trình dự án với dự án.</span><span class="sxs-lookup"><span data-stu-id="4cfdd-114">You must associate a project calendar with the project.</span></span> <span data-ttu-id="4cfdd-115">Khi bạn tạo lịch trình công việc, không có sự khác biệt giữa mẫu dự án và dự án.</span><span class="sxs-lookup"><span data-stu-id="4cfdd-115">When you create a work schedule, there is no difference between a project template and a project.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="4cfdd-116">Ước tính dự án</span><span class="sxs-lookup"><span data-stu-id="4cfdd-116">Project estimates</span></span>

<span data-ttu-id="4cfdd-117">Ước tính dự án trong một mẫu dự án hoạt động theo cách tương tự như ước tính dự án trong một dự án.</span><span class="sxs-lookup"><span data-stu-id="4cfdd-117">Project estimates in a project template work the same way as project estimates in a project.</span></span> <span data-ttu-id="4cfdd-118">Tuy nhiên, chi phí và giá bán được lấy từ bảng giá bán và chi phí mặc định được xác định trong các tham số.</span><span class="sxs-lookup"><span data-stu-id="4cfdd-118">However, the cost and sales prices are pulled from the default cost and sales price lists that are defined in the parameters.</span></span>

## <a name="creating-a-project-from-a-template"></a><span data-ttu-id="4cfdd-119">Tạo dự án từ mẫu</span><span class="sxs-lookup"><span data-stu-id="4cfdd-119">Creating a project from a template</span></span>
 
<span data-ttu-id="4cfdd-120">Có một số cách để tạo một dự án từ một mẫu dự án:</span><span class="sxs-lookup"><span data-stu-id="4cfdd-120">There are several ways to create a project from a project template:</span></span>

- <span data-ttu-id="4cfdd-121">Khi tạo dự án từ báo giá, bạn có thể chọn mẫu dự án trong hộp thoại **Tạo nhanh: Dự án**.</span><span class="sxs-lookup"><span data-stu-id="4cfdd-121">When you create a project from a quote, you can select a project template in the **Quick Create: Project** dialog box.</span></span>

> ![Hộp thoại Tạo nhanh: Dự án](media/project-11.png)

- <span data-ttu-id="4cfdd-123">Khi bạn tạo một dự án bằng cách chọn **Dự án mới**, trang **Dự án** xuất hiện trước khi bản ghi được lưu.</span><span class="sxs-lookup"><span data-stu-id="4cfdd-123">When you create a project by selecting **New Project**, the **Project** page appears before the record is saved.</span></span> <span data-ttu-id="4cfdd-124">Trong trường **Chọn mẫu**, hãy chọn một trong các mẫu dự án đã xác định trước trong tổ chức.</span><span class="sxs-lookup"><span data-stu-id="4cfdd-124">In the **Pick a Template** field, select one of the predefined project templates in the organization.</span></span>
- <span data-ttu-id="4cfdd-125">Sử dụng **Tạo dự án từ mẫu** trên trang **Thực thể mẫu**.</span><span class="sxs-lookup"><span data-stu-id="4cfdd-125">Use **Create Project from a Template** on the **Template Entity** page.</span></span>

## <a name="copying-components-of-template-to-project"></a><span data-ttu-id="4cfdd-126">Sao chép các thành phần của một mẫu vào dự án</span><span class="sxs-lookup"><span data-stu-id="4cfdd-126">Copying components of template to project</span></span>

<span data-ttu-id="4cfdd-127">Khi bạn sao chép các cấu phần của một mẫu dự án vào dự án, một vài thao tác thay thế có thể xảy ra, tuỳ thuộc vào thiết đặt trong dự án.</span><span class="sxs-lookup"><span data-stu-id="4cfdd-127">When you copy the components of a project template to a project, a few overrides can occur, depending on the settings in the project.</span></span>

### <a name="copying-the-schedule"></a><span data-ttu-id="4cfdd-128">Sao chép lịch trình</span><span class="sxs-lookup"><span data-stu-id="4cfdd-128">Copying the schedule</span></span>

<span data-ttu-id="4cfdd-129">Khi bạn sao chép lịch trình từ mẫu dự án, nếu dự án có lịch trình dự án khác thay vì mẫu, giờ làm việc từ lịch của dự án đã được áp dụng cho lịch trình dự án.</span><span class="sxs-lookup"><span data-stu-id="4cfdd-129">When you copy the schedule from a project template, if the project has a different project calendar than the template, work hours from the project's calendar are applied to the task schedule.</span></span> <span data-ttu-id="4cfdd-130">Trong cách này, lịch trình được điều chỉnh để khớp với lịch dự án hỗ trợ.</span><span class="sxs-lookup"><span data-stu-id="4cfdd-130">In this way, the schedule is adjusted to match the backing project calendar.</span></span> <span data-ttu-id="4cfdd-131">Tương tự, nhiệm vụ đầu tiên trên lịch trình lấy ngày bắt đầu của dự án và lịch trình của phần còn lại của hệ thống cấp bậc được cập nhật dựa trên khoảng thời gian và mức phụ thuộc được chỉ định trong mẫu.</span><span class="sxs-lookup"><span data-stu-id="4cfdd-131">Similarly, the first task on the schedule takes the project's start date, and the schedule of the rest of the hierarchy is updated based on the duration and dependencies that are specified in the template.</span></span> 

### <a name="copying-project-estimates"></a><span data-ttu-id="4cfdd-132">Sao chép ước tính dự án</span><span class="sxs-lookup"><span data-stu-id="4cfdd-132">Copying project estimates</span></span> 

<span data-ttu-id="4cfdd-133">Khi bạn sao chép trên các mô tả ước tính dự án, bảng giá sẽ được cập nhật.</span><span class="sxs-lookup"><span data-stu-id="4cfdd-133">When you copy across project estimate lines, the price lists are updated.</span></span> <span data-ttu-id="4cfdd-134">Đối với bảng giá chi phí, những thông tin cập nhật này dựa trên đơn vị sở hữu của dự án.</span><span class="sxs-lookup"><span data-stu-id="4cfdd-134">For the cost price list, these updates are based on the owning unit of the project.</span></span> <span data-ttu-id="4cfdd-135">Đối với bảng giá bán, những thông tin cập nhật này dựa trên khách hàng.</span><span class="sxs-lookup"><span data-stu-id="4cfdd-135">For the sales price list, they are based on the customer.</span></span> <span data-ttu-id="4cfdd-136">Đối với dự án liên kết với thực thể bán hàng, giá bán và chi phí được xác định dựa trên các bảng giá này.</span><span class="sxs-lookup"><span data-stu-id="4cfdd-136">For projects that are associated with a sales entity, the unit cost and sales prices are determined based on these price lists.</span></span>

### <a name="copying-a-project-team"></a><span data-ttu-id="4cfdd-137">Sao chép một nhóm dự án</span><span class="sxs-lookup"><span data-stu-id="4cfdd-137">Copying a project team</span></span>

<span data-ttu-id="4cfdd-138">Khi nhóm dự án được sao chép từ mẫu dự án vào dự án, nguồn lực chung được sao chép cùng với kỹ năng và mức độ thành thạo được xác định trong mẫu.</span><span class="sxs-lookup"><span data-stu-id="4cfdd-138">When a project team is copied from a project template to a project, the generic resources are copied, together with the skills and proficiencies that are defined in the template.</span></span> <span data-ttu-id="4cfdd-139">Việc phân công nguồn lực chung cũng được duy trì như khi chúng ở trong mẫu dự án.</span><span class="sxs-lookup"><span data-stu-id="4cfdd-139">Generic resource assignments are also maintained as they were in the project template.</span></span> <span data-ttu-id="4cfdd-140">Nguồn lực có tên không được hỗ trợ trong mẫu dự án.</span><span class="sxs-lookup"><span data-stu-id="4cfdd-140">Named resources aren't supported in project templates.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]