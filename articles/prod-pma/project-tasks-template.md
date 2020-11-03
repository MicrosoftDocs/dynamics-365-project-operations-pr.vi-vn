---
title: Đồng bộ hóa nhiệm vụ dự án trực tiếp từ Project Service Automation sang Finance and Operations
description: Chủ đề này mô tả mẫu và nhiệm vụ cơ bản dùng để đồng bộ hóa trực tiếp các nhiệm vụ dự án từ Microsoft Dynamics 365 Project Service Automation sang Dynamics 365 Finance.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 0383607a07def6c21562bf4b0893fe3ce3db6a04
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087090"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>Đồng bộ hóa nhiệm vụ dự án trực tiếp từ Project Service Automation sang Finance and Operations

[!include[banner](../includes/banner.md)]

Chủ đề này mô tả mẫu và nhiệm vụ cơ bản dùng để đồng bộ hóa trực tiếp các nhiệm vụ dự án từ Dynamics 365 Project Service Automation sang Dynamics 365 Finance.

> [!NOTE]
> - Tính năng tích hợp nhiệm vụ dự án, thể loại giao dịch chi phí, ước tính giờ, ước tính chi phí và khóa chức năng có sẵn trong phiên bản 8.0.
> - Nếu bạn đang sử dụng Enterprise Edition 7.3.0, sau khi cài đặt KB 4132657 và KB 4132660, thì bạn sẽ có thể sử dụng các mẫu để tích hợp nhiệm vụ dự án, danh mục giao dịch chi phí, các giá trị ước tính giờ, ước tính chi phí và giá trị thực tế để đặt cấu hình tùy chọn khóa chức năng. Nếu bạn phải đặt lại các bản phân bổ kế toán, thì chúng tôi khuyên bạn cũng nên cài đặt KB 4131710.
> - Tùy chọn tích hợp giá trị thực tế có sẵn từ phiên bản 8.0.1.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Luồng dữ liệu cho Project Service Automation sang Finance

Giải pháp tích hợp Project Service Automation sang Finance sử dụng tính năng Tích hợp dữ liệu để đồng bộ hóa dữ liệu giữa các phiên bản của Project Service Automation và Finance. Các mẫu tích hợp có sẵn với tính năng Tích hợp dữ liệu sẽ tạo ra luồng dữ liệu về nhiệm vụ dự án từ Project Service Automation đến Finance.

Hình minh họa sau đây cho thấy cách dữ liệu được đồng bộ hóa giữa Project Service Automation và Finance.

[![Luồng dữ liệu cho phần tích hợp Project Service Automation với Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Mẫu và nhiệm vụ

Để truy cập vào mẫu, trong trung tâm quản trị Microsoft Power Apps, chọn **Dự án** và sau đó, ở góc trên bên phải, chọn **Dự án mới** để chọn các mẫu công khai.

Mẫu sau và nhiệm vụ cơ bản được sử dụng để đồng bộ hóa nhiệm vụ dự án từ Project Service Automation sang Finance:

- **Tên mẫu trong Tích hợp dữ liệu:** Nhiệm vụ dự án (PSA sang Fin and Ops)
- **Tên của nhiệm vụ trong dự án:** Nhiệm vụ dự án

Trước khi quá trình đồng bộ hóa nhiệm vụ dự án có thể xảy ra, bạn phải đồng bộ hóa hợp đồng dự án và dự án.

## <a name="entity-set"></a>Bộ thực thể

| Project Service Automation | Tài chính                             |
|----------------------------|-------------------------------------|
| Nhiệm vụ Dự án              | Thực thể tích hợp cho nhiệm vụ dự án |

## <a name="entity-flow"></a>Luồng thực thể

Nhiệm vụ dự án được quản lý trong Project Service Automation và được đồng bộ hóa với Finance dưới dạng hoạt động dự án.

## <a name="prerequisites-and-mapping-setup"></a>Điều kiện tiên quyết và thiết lập ánh xạ

Trước khi quá trình đồng bộ hóa nhiệm vụ dự án có thể xảy ra, bạn phải đồng bộ hóa hợp đồng dự án và dự án.

## <a name="power-query"></a>Power Query

Bạn phải sử dụng Microsoft Power Query dành cho Excel để lọc dữ liệu nếu điều kiện sau được đáp ứng:

- Bạn có bản ghi dành riêng cho nguồn lực trong nhiệm vụ dự án.

Nếu bạn phải sử dụng Power Query, hãy làm theo hướng dẫn sau:

- Mẫu Nhiệm vụ dự án (PSA sang Fin và Ops) có bộ lọc mặc định loại trừ các bản ghi dành riêng cho nguồn lực khỏi nhiệm vụ dự án bằng cách thiết lập bộ lọc trên **IsLineTask** thành **False**. Nếu bạn tạo mẫu của riêng mình, bạn phải thêm bộ lọc này.

## <a name="template-mapping-in-data-integration"></a>Ánh xạ mẫu trong tích hợp dữ liệu

Hình sau đây minh họa một ví dụ về việc ánh xạ nhiệm vụ mẫu trong Tích hợp dữ liệu. Tùy chọn ánh xạ hiển thị thông tin trường sẽ được đồng bộ hóa từ Project Service Automation sang Finance.

[![Ánh xạ mẫu](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)
