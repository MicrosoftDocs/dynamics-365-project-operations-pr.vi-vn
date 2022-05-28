---
title: Phát triển mẫu dự án với chức năng Sao chép dự án
description: Chủ đề này cung cấp thông tin về cách tạo mẫu dự án bằng hành động tùy chỉnh Sao chép dự án.
author: stsporen
ms.date: 03/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 72aa2db7c717eeab85ada448c673bf702087baeb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590927"
---
# <a name="develop-project-templates-with-copy-project"></a>Phát triển mẫu dự án với chức năng Sao chép dự án

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Dynamics 365 Project Operations hỗ trợ khả năng sao chép dự án và đảo ngược lượt phân công bất kỳ lại cho nguồn lực chung đại diện cho vai trò. Khách hàng có thể sử dụng chức năng này để xây dựng các mẫu dự án cơ bản.

Khi bạn chọn **Sao chép dự án**, trạng thái của dự án mục tiêu sẽ được cập nhật. Hãy sử dụng **Lý do dẫn đến trạng thái** để xác định thời điểm hoàn tất hành động sao chép. Thao tác chọn **Sao chép dự án** cũng cập nhật ngày bắt đầu của dự án thành ngày bắt đầu hiện tại nếu không có ngày mục tiêu nào được phát hiện trong thực thể dự án mục tiêu.

## <a name="copy-project-custom-action"></a>Hành động tùy chỉnh Sao chép dự án

### <a name="name"></a>Tên 

msdyn\_ CopyProjectV3

### <a name="input-parameters"></a>Tham số đầu vào

Có ba tham số đầu vào:

- **ReplaceNamedResources** hoặc **ClearTeamsAndAssignments** - Chỉ đặt một trong các tùy chọn. Đừng đặt cả hai.

    - **\{"ReplaceNamedResources": true\}** - Hành vi mặc định cho Hoạt động Dự án. Mọi tài nguyên được đặt tên đều được thay thế bằng tài nguyên chung.
    - **\{"ClearTeamsAndAssignments": true\}** - Hành vi mặc định cho Dự án cho Web. Tất cả các nhiệm vụ và thành viên trong nhóm đều bị xóa.

- **SourceProject** - Tham chiếu thực thể của dự án nguồn để sao chép từ đó. Tham số này không được rỗng.
- **Mục tiêu** - Tham chiếu thực thể của dự án mục tiêu để sao chép vào. Tham số này không được rỗng.

Bảng sau đây cung cấp tóm tắt về ba tham số.

| Tham số                | Loại             | Giá_trị                 |
|--------------------------|------------------|-----------------------|
| ReplaceNamedResources    | Boolean          | **ĐÚNG VẬY** hoặc **SAI** |
| ClearTeamsAndAssignments | Boolean          | **ĐÚNG VẬY** hoặc **SAI** |
| SourceProject            | Tham chiếu thực thể | Dự án nguồn    |
| Mục tiêu                   | Tham chiếu thực thể | Dự án mục tiêu    |

Để biết thêm các mặc định về hành động, hãy xem [Sử dụng các hành động API Web](/powerapps/developer/common-data-service/webapi/use-web-api-actions).

### <a name="validations"></a>Xác thực

Các xác nhận sau đây được thực hiện.

1. Null kiểm tra và truy xuất nguồn và dự án đích để xác nhận sự tồn tại của cả hai dự án trong tổ chức.
2. Hệ thống xác nhận rằng dự án mục tiêu hợp lệ để sao chép bằng cách xác minh các điều kiện sau:

    - Không có hoạt động nào trước đó trong dự án (bao gồm cả việc lựa chọn **Nhiệm vụ**), và dự án mới được tạo.
    - Không có bản sao trước đó, không có lần nhập nào được yêu cầu đối với dự án này và dự án không có **Thất bại** tình trạng.

3. Thao tác không được gọi bằng cách sử dụng HTTP.

## <a name="specify-fields-to-copy"></a>Chỉ định các trường sẽ sao chép

Khi **Sao chép dự án** được gọi, hành động này sẽ xem xét mục **Sao chép cột dự án** của dạng xem dự án để xác định những trường nào sẽ được sao chép trong quá trình sao chép dự án.

### <a name="example"></a>Ví dụ:

Ví dụ sau đây cho thấy cách gọi **CopyProjectV3** hành động tùy chỉnh với **removeNamedResources** bộ tham số.

```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

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
            targetProject["msdyn_subject"] = "Example Project - Copy";
            targetProject.Id = organizationService.Create(targetProject);

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption, true, false);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, bool replaceNamedResources = true, bool clearTeamsAndAssignments = false)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV3");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;

            if (replaceNamedResources)
            {
                req["ReplaceNamedResources"] = true;
            }
            else
            {
                req["ClearTeamsAndAssignments"] = true;
            }

            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```

[!INCLUDE[footer-include](../includes/footer-banner.md)]
