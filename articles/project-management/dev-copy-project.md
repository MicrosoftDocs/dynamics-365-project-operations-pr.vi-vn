---
title: Phát triển mẫu dự án với chức năng Sao chép dự án
description: Chủ đề này cung cấp thông tin về cách tạo mẫu dự án bằng hành động tùy chỉnh Sao chép dự án.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cb49109e8c199bc4569702ae844a19985534294d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087048"
---
# <a name="develop-project-templates-with-copy-project"></a>Phát triển mẫu dự án với chức năng Sao chép dự án

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Dynamics 365 Project Operations hỗ trợ khả năng sao chép dự án và hoàn nguyên mọi mục chỉ định thành các tài nguyên chung đại diện cho vai trò. Khách hàng có thể sử dụng chức năng này để xây dựng các mẫu dự án cơ bản.

Khi bạn chọn **Sao chép dự án** , trạng thái của dự án mục tiêu sẽ được cập nhật. Hãy sử dụng **Lý do dẫn đến trạng thái** để xác định thời điểm hoàn tất hành động sao chép. Thao tác chọn **Sao chép dự án** cũng cập nhật ngày bắt đầu của dự án thành ngày bắt đầu hiện tại nếu không có ngày mục tiêu nào được phát hiện trong thực thể dự án mục tiêu.

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


- **{"clearTeamsAndAssignments":true}** : Hành vi mặc định cho Dự án dành cho web, sẽ loại bỏ tất cả các mục chỉ định và thành viên nhóm.
- **{"removeNamedResources":true}** Hành vi mặc định cho Project Operations, sẽ hoàn nguyên các mục chỉ định thành tài nguyên chung.

Để biết thêm các giá trị mặc định trên hành động, hãy xem [Sử dụng hành động Web API](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)

## <a name="specify-fields-to-copy"></a>Chỉ định các trường sẽ sao chép 
Khi **Sao chép dự án** được gọi, hành động này sẽ xem xét mục **Sao chép cột dự án** của dạng xem dự án để xác định những trường nào sẽ được sao chép trong quá trình sao chép dự án.
