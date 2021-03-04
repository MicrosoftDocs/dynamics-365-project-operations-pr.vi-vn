---
title: Phát triển mẫu dự án với chức năng Sao chép dự án
description: Chủ đề này cung cấp thông tin về cách tạo mẫu dự án bằng hành động tùy chỉnh Sao chép dự án.
author: stsporen
manager: Annbe
ms.date: 01/21/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 87696b41db20e9ec70270c850d9acfe05df8cd84
ms.sourcegitcommit: d5004acb6f1c257b30063c873896fdea92191e3b
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/22/2021
ms.locfileid: "5045035"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="5acad-103">Phát triển mẫu dự án với chức năng Sao chép dự án</span><span class="sxs-lookup"><span data-stu-id="5acad-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="5acad-104">_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_</span><span class="sxs-lookup"><span data-stu-id="5acad-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="5acad-105">Dynamics 365 Project Operations hỗ trợ khả năng sao chép dự án và đảo ngược lượt phân công bất kỳ lại cho nguồn lực chung đại diện cho vai trò.</span><span class="sxs-lookup"><span data-stu-id="5acad-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="5acad-106">Khách hàng có thể sử dụng chức năng này để xây dựng các mẫu dự án cơ bản.</span><span class="sxs-lookup"><span data-stu-id="5acad-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="5acad-107">Khi bạn chọn **Sao chép dự án**, trạng thái của dự án mục tiêu sẽ được cập nhật.</span><span class="sxs-lookup"><span data-stu-id="5acad-107">When you select **Copy Project**, the status of the target project is updated.</span></span> <span data-ttu-id="5acad-108">Hãy sử dụng **Lý do dẫn đến trạng thái** để xác định thời điểm hoàn tất hành động sao chép.</span><span class="sxs-lookup"><span data-stu-id="5acad-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="5acad-109">Thao tác chọn **Sao chép dự án** cũng cập nhật ngày bắt đầu của dự án thành ngày bắt đầu hiện tại nếu không có ngày mục tiêu nào được phát hiện trong thực thể dự án mục tiêu.</span><span class="sxs-lookup"><span data-stu-id="5acad-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="5acad-110">Hành động tùy chỉnh Sao chép dự án</span><span class="sxs-lookup"><span data-stu-id="5acad-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="5acad-111">Tên</span><span class="sxs-lookup"><span data-stu-id="5acad-111">Name</span></span> 

<span data-ttu-id="5acad-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="5acad-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="5acad-113">Tham số đầu vào</span><span class="sxs-lookup"><span data-stu-id="5acad-113">Input parameters</span></span>
<span data-ttu-id="5acad-114">Có ba tham số đầu vào:</span><span class="sxs-lookup"><span data-stu-id="5acad-114">There are three input parameters:</span></span>

| <span data-ttu-id="5acad-115">Tham số</span><span class="sxs-lookup"><span data-stu-id="5acad-115">Parameter</span></span>          | <span data-ttu-id="5acad-116">Loại</span><span class="sxs-lookup"><span data-stu-id="5acad-116">Type</span></span>   | <span data-ttu-id="5acad-117">Giá trị</span><span class="sxs-lookup"><span data-stu-id="5acad-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="5acad-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="5acad-118">ProjectCopyOption</span></span>  | <span data-ttu-id="5acad-119">String</span><span class="sxs-lookup"><span data-stu-id="5acad-119">String</span></span> | <span data-ttu-id="5acad-120">**{"removeNamedResources":true}** hoặc **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="5acad-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="5acad-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="5acad-121">SourceProject</span></span>      | <span data-ttu-id="5acad-122">Tham chiếu thực thể</span><span class="sxs-lookup"><span data-stu-id="5acad-122">Entity Reference</span></span> | <span data-ttu-id="5acad-123">Dự án nguồn</span><span class="sxs-lookup"><span data-stu-id="5acad-123">Source Project</span></span> |
| <span data-ttu-id="5acad-124">Đích</span><span class="sxs-lookup"><span data-stu-id="5acad-124">Target</span></span>             | <span data-ttu-id="5acad-125">Tham chiếu thực thể</span><span class="sxs-lookup"><span data-stu-id="5acad-125">Entity Reference</span></span> | <span data-ttu-id="5acad-126">Dự án mục tiêu</span><span class="sxs-lookup"><span data-stu-id="5acad-126">Target Project</span></span> |


- <span data-ttu-id="5acad-127">**{"clearTeamsAndAssignments":true}**: Hành vi mặc định cho Dự án dành cho web, sẽ loại bỏ tất cả các mục chỉ định và thành viên nhóm.</span><span class="sxs-lookup"><span data-stu-id="5acad-127">**{"clearTeamsAndAssignments":true}**: Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="5acad-128">**{"removeNamedResources":true}** Hành vi mặc định cho Project Operations, sẽ hoàn nguyên các mục chỉ định thành tài nguyên chung.</span><span class="sxs-lookup"><span data-stu-id="5acad-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="5acad-129">Để biết thêm các giá trị mặc định trên hành động, hãy xem [Sử dụng hành động Web API](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="5acad-129">For more defaults on actions, see [Use Web API actions](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="5acad-130">Chỉ định các trường sẽ sao chép</span><span class="sxs-lookup"><span data-stu-id="5acad-130">Specify fields to copy</span></span> 
<span data-ttu-id="5acad-131">Khi **Sao chép dự án** được gọi, hành động này sẽ xem xét mục **Sao chép cột dự án** của dạng xem dự án để xác định những trường nào sẽ được sao chép trong quá trình sao chép dự án.</span><span class="sxs-lookup"><span data-stu-id="5acad-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>


### <a name="example"></a><span data-ttu-id="5acad-132">Ví dụ:</span><span class="sxs-lookup"><span data-stu-id="5acad-132">Example</span></span>
<span data-ttu-id="5acad-133">Ví dụ sau đây cho thấy cách gọi hành động tùy chỉnh **CopyProject** bằng tham số **removeNamedResources**.</span><span class="sxs-lookup"><span data-stu-id="5acad-133">The following example shows how to call the **CopyProject** custom action with the **removeNamedResources** parameter set.</span></span>
```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

    [DataContract]
    public class ProjectCopyOption
    {
        /// <summary>
        /// Clear teams and assignments.
        /// </summary>
        [DataMember(Name = "clearTeamsAndAssignments")]
        public bool ClearTeamsAndAssignments { get; set; }

        /// <summary>
        /// Replace named resource with generic resource.
        /// </summary>
        [DataMember(Name = "removeNamedResources")]
        public bool ReplaceNamedResources { get; set; }
    }

    public class CopyProjectSample
    {
        private IOrganizationService organizationService;

        public CopyProjectSample(IOrganizationService organizationService)
        {
            this.organizationService = organizationService;
        }

        public void SampleRun()
        {
            // Example source project GUID
            Guid sourceProjectId = new Guid("11111111-1111-1111-1111-111111111111");
            var sourceProject = new Entity("msdyn_project", sourceProjectId);

            Entity targetProject = new Entity("msdyn_project");
            targetProject["msdyn_subject"] = "Example Project";
            targetProject.Id = organizationService.Create(targetProject);

            ProjectCopyOption copyOption = new ProjectCopyOption();
            copyOption.ReplaceNamedResources = true;

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, ProjectCopyOption projectCopyOption)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV2");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;
            req["ProjectCopyOption"] = JsonConvert.SerializeObject(projectCopyOption);
            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```
