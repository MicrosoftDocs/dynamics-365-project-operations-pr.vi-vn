---
title: Phát triển mẫu dự án với chức năng Sao chép dự án
description: Bài viết này cung cấp thông tin về cách tạo mẫu dự án bằng hành động tùy chỉnh Sao chép dự án.
author: stsporen
ms.date: 03/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 47c1023bbc4c21e3571bffbf3670bf0f7854f81d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923858"
---
# <a name="develop-project-templates-with-copy-project"></a>Phát triển mẫu dự án với chức năng Sao chép dự án

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Dynamics 365 Project Operations hỗ trợ khả năng sao chép dự án và đảo ngược lượt phân công bất kỳ lại cho nguồn lực chung đại diện cho vai trò. Khách hàng có thể sử dụng chức năng này để xây dựng các mẫu dự án cơ bản.

Khi bạn chọn **Sao chép dự án**, trạng thái của dự án mục tiêu sẽ được cập nhật. Hãy sử dụng **Lý do dẫn đến trạng thái** để xác định thời điểm hoàn tất hành động sao chép. Thao tác chọn **Sao chép dự án** cũng cập nhật ngày bắt đầu của dự án thành ngày bắt đầu hiện tại nếu không có ngày mục tiêu nào được phát hiện trong thực thể dự án mục tiêu.

## <a name="copy-project-custom-action"></a>Hành động tùy chỉnh Sao chép dự án

### <a name="name"></a>Tên 

msdyn\_CopyProjectV3

### <a name="input-parameters"></a>Tham số đầu vào

Có ba tham số đầu vào:

- **ReplaceNamedResources** hoặc **ClearTeamsAndAssignments** – Chỉ đặt một trong các tùy chọn. Không đặt cả hai.

    - **\{"ReplaceNamedResources":true\}** – Hành vi mặc định cho Project Operations. Bất kỳ nguồn lực có tên được thay thế bằng nguồn lực chung.
    - **\{"ClearTeamsAndAssignments":true\}** – Hành vi mặc định cho Project for the Web. Tất cả các phân công và thành viên nhóm đều bị xóa.

- **SourceProject** – Tham chiếu thực thể của dự án nguồn để sao chép từ đó. Tham số này không được là null.
- **Target** – Tham chiếu thực thể của dự án địch để sao chép vào đó. Tham số này không được là null.

Bảng dưới đây đưa ra sự tóm tắt về ba tham số.

| Tham số                | Loại             | Giá_trị                 |
|--------------------------|------------------|-----------------------|
| ReplaceNamedResources    | Boolean          | **True** hoặc **False** |
| ClearTeamsAndAssignments | Boolean          | **True** hoặc **False** |
| SourceProject            | Tham chiếu thực thể | Dự án nguồn    |
| Mục tiêu                   | Tham chiếu thực thể | Dự án đích    |

Để biết thêm các giá trị mặc định trên hành động, hãy xem [Sử dụng hành động Web API](/powerapps/developer/common-data-service/webapi/use-web-api-actions).

### <a name="validations"></a>Xác thực

Các xác thực sau được thực hiện.

1. Kiểm tra và truy xuất rỗng các dự án nguồn và đích để xác nhận sự tồn tại của cả hai dự án trong tổ chức.
2. Hệ thống xác thực rằng dự án đích hợp lệ để sao chép bằng cách xác minh các điều kiện sau:

    - Không có hoạt động nào trước đó trong dự án (bao gồm cả việc chọn tab **Nhiệm vụ**), và dự án mới được tạo.
    - Không có bản sao nào trước đó, không có lần nhập nào được yêu cầu đối với dự án này và dự án không có trạng thái **Không thành công**.

3. Thao tác không được gọi bằng cách sử dụng HTTP.

## <a name="specify-fields-to-copy"></a>Chỉ định các trường sẽ sao chép

Khi **Sao chép dự án** được gọi, hành động này sẽ xem xét mục **Sao chép cột dự án** của dạng xem dự án để xác định những trường nào sẽ được sao chép trong quá trình sao chép dự án.

### <a name="example"></a>Ví dụ:

Ví dụ sau đây cho thấy cách gọi hành động tùy chỉnh **CopyProjectV3** bằng tham số **removeNamedResources**.

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
