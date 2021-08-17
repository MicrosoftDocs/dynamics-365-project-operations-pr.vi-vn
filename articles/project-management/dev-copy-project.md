---
title: Phát triển mẫu dự án với chức năng Sao chép dự án
description: Chủ đề này cung cấp thông tin về cách tạo mẫu dự án bằng hành động tùy chỉnh Sao chép dự án.
author: stsporen
ms.date: 01/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d12301b4e7baabeb0f045f9a11d4695fc026339af3fa7650db7177c495c71e90
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/06/2021
ms.locfileid: "6989305"
---
# <a name="develop-project-templates-with-copy-project"></a>Phát triển mẫu dự án với chức năng Sao chép dự án

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Operations hỗ trợ khả năng sao chép dự án và đảo ngược lượt phân công bất kỳ lại cho nguồn lực chung đại diện cho vai trò. Khách hàng có thể sử dụng chức năng này để xây dựng các mẫu dự án cơ bản.

Khi bạn chọn **Sao chép dự án**, trạng thái của dự án mục tiêu sẽ được cập nhật. Hãy sử dụng **Lý do dẫn đến trạng thái** để xác định thời điểm hoàn tất hành động sao chép. Thao tác chọn **Sao chép dự án** cũng cập nhật ngày bắt đầu của dự án thành ngày bắt đầu hiện tại nếu không có ngày mục tiêu nào được phát hiện trong thực thể dự án mục tiêu.

## <a name="copy-project-custom-action"></a>Hành động tùy chỉnh Sao chép dự án 

### <a name="name"></a>Tên 

**msdyn_CopyProjectV2**

### <a name="input-parameters"></a>Tham số đầu vào
Có ba tham số đầu vào:

| Tham số          | Loại   | Giá trị                                                   | 
|--------------------|--------|----------------------------------------------------------|
| ProjectCopyOption  | String | **{"removeNamedResources":true}** hoặc **{"clearTeamsAndAssignments":true}** |
| SourceProject      | Tham chiếu thực thể | Dự án nguồn |
| Đích             | Tham chiếu thực thể | Dự án mục tiêu |


- **{"clearTeamsAndAssignments":true}**: Hành vi mặc định cho Dự án dành cho web, sẽ loại bỏ tất cả các mục chỉ định và thành viên nhóm.
- **{"removeNamedResources":true}** Hành vi mặc định cho Project Operations, sẽ hoàn nguyên các mục chỉ định thành tài nguyên chung.

Để biết thêm các giá trị mặc định trên hành động, hãy xem [Sử dụng hành động Web API](/powerapps/developer/common-data-service/webapi/use-web-api-actions)

## <a name="specify-fields-to-copy"></a>Chỉ định các trường sẽ sao chép 
Khi **Sao chép dự án** được gọi, hành động này sẽ xem xét mục **Sao chép cột dự án** của dạng xem dự án để xác định những trường nào sẽ được sao chép trong quá trình sao chép dự án.


### <a name="example"></a>Ví dụ:
Ví dụ sau đây cho thấy cách gọi hành động tùy chỉnh **CopyProject** bằng tham số **removeNamedResources**.
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]