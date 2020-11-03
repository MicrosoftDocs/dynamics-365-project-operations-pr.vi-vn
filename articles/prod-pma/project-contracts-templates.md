---
title: Đồng bộ hóa các hợp đồng dự án và dự án trực tiếp từ Project Service Automation sang Finance and Operations
description: Chủ đề này mô tả mẫu và nhiệm vụ cơ bản dùng để đồng bộ hóa trực tiếp các hợp đồng dự án và dự án trực tiếp từ Microsoft Dynamics 365 Project Service Automation sang Dynamics 365 Finance.
author: Yowelle
manager: AnnBe
ms.date: 09/09/2019
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
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 9e4f11ec0bb88ed0971a3d082e7ca7823fcf8453
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087242"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance-and-operations"></a>Đồng bộ hóa các hợp đồng dự án và dự án trực tiếp từ Project Service Automation sang Finance and Operations

[!include[banner](../includes/banner.md)]

Chủ đề này mô tả mẫu và nhiệm vụ cơ bản dùng để đồng bộ hóa trực tiếp các hợp đồng dự án và dự án trực tiếp từ Dynamics 365 Project Service Automation sang Dynamics 365 Finance.

> [!NOTE] 
> Nếu đang sử dụng Enterprise Edition 7.3.0, bạn phải cài đặt KB 4074835.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Luồng dữ liệu cho Project Service Automation sang Finance

> [!NOTE]
> Trước khi có thể sử dụng giải pháp tích hợp Project Service Automation sang Finance, bạn nên làm quen với tính năng tích hợp Dynamics 365 Data.

Giải pháp tích hợp Project Service Automation sang Finance sử dụng tính năng Tích hợp dữ liệu để đồng bộ hóa dữ liệu giữa các phiên bản của Project Service Automation và Finance. Mẫu tích hợp có sẵn với tính năng Tích hợp dữ liệu cho phép dòng dữ liệu về hợp đồng dự án, dự án, mô tả hợp đồng dự án và các mốc thời gian mô tả hợp đồng dự án từ Project Service Automation sang Finance.

Hình minh họa sau đây cho thấy cách dữ liệu được đồng bộ hóa giữa Project Service Automation và Finance.

[![Luồng dữ liệu cho phần tích hợp Project Service Automation với Finance](./media/ProjectsAndContractsFlow_upd.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>Mẫu và nhiệm vụ

Để truy cập các mẫu có sẵn, trong trung tâm quản trị Microsoft Power Apps, chọn **Dự án** và sau đó, ở góc trên bên phải, chọn **Dự án mới** để chọn các mẫu công khai.

Các mẫu sau và các nhiệm vụ cơ bản được sử dụng để đồng bộ hóa giá trị thực tế trong hợp đồng dự án và dự án từ Project Service Automation sang Finance:

### <a name="integrating-with-dynamics-365-project-service-automation-v2x"></a>Tích hợp với Dynamics 365 Project Service Automation v2.x
- **Tên mẫu trong Tích hợp dữ liệu:** Dự án và hợp đồng (PSA sang Fin và Ops)
- **Tên của nhiệm vụ trong dự án:**

    - Hợp đồng dự án PSA sang Fin và Ops
    - Dự án PSA sang Fin và Ops
    - Mô tả hợp đồng dự án PSA sang Fin và Ops
    - Các mốc thời gian mô tả hợp đồng dự án PSA sang Fin và Ops
  
### <a name="integrating-with-dynamics-365-project-service-automation-v3x"></a>Tích hợp với Dynamics 365 Project Service Automation v3.x
Có một sự thay đổi về lược đồ trong Project Service Automation ảnh hưởng đến mẫu mốc thời gian mô tả hợp đồng dự án và cần sử dụng phiên bản v2 của mẫu để tích hợp Project Service Automation v3.x với Dynamics 365.

- **Tên mẫu trong Tích hợp dữ liệu:** Dự án và hợp đồng (PSA 3.x sang Fin và Ops) - v2
- **Tên của nhiệm vụ trong dự án:**

    - Hợp đồng dự án PSA sang Fin và Ops
    - Dự án PSA sang Fin và Ops
    - Mô tả hợp đồng dự án PSA sang Fin và Ops
    - Các mốc thời gian mô tả hợp đồng dự án PSA sang Fin và Ops

Trước khi quá trình đồng bộ hóa hợp đồng dự án và dự án có thể xảy ra, bạn phải đồng bộ hóa các tài khoản.

## <a name="entity-set"></a>Bộ thực thể

| Project Service Automation       | Tài chính                                                |
|----------------------------------|--------------------------------------------------------|
| Đơn hàng                           | Thực thể tích hợp cho hợp đồng dự án                |
| Dự án                         | Thực thể tích hợp cho dự án                         |
| Dòng mô tả Đơn hàng                      | Thực thể tích hợp cho mô tả hợp đồng dự án           |
| Mốc thời gian mô tả hợp đồng dự án | Thực thể tích hợp cho mốc thời gian mô tả hợp đồng dự án |

## <a name="entity-flow"></a>Luồng thực thể

Hợp đồng dự án được quản lý trong Project Service Automation và được đồng bộ hóa với Finance dưới dạng hợp đồng dự án. Là một phần của mẫu tích hợp, bạn có thể thiết lập nguồn tích hợp trong Finance cho hợp đồng dự án.

Dự án Thời gian và vật liệu và dự án Giá cố định được quản lý trong Project Service Automation và được đồng bộ hóa với Finance dưới dạng dự án. Là một phần của tích hợp mẫu, bạn có thể thiết lập nguồn tích hợp trong Finance cho dự án.

Mô tả hợp đồng dự án được quản lý trong Project Service Automation và được đồng bộ hóa với Finance dưới dạng quy tắc thanh toán hợp đồng dự án. Nếu phương thức thanh toán khác với loại dự án mặc định, việc đồng bộ hóa sẽ cập nhật loại dự án cho dự án mô tả hợp đồng và nhóm dự án.

Mốc thời gian mô tả hợp đồng dự án được quản lý trong Project Service Automation và được đồng bộ hóa với Finance dưới dạng mốc thời gian quy tắc thanh toán hợp đồng dự án.

## <a name="project-service-automation-to-finance-integration-solution"></a>Giải pháp tích hợp Project Service Automation với Finance

Trường **ID hợp đồng dự án** có sẵn trên trang **Hợp đồng dự án**. Trường này đã được tạo thành một chìa khóa tự nhiên và duy nhất để hỗ trợ quá trình tích hợp.

Khi hợp đồng dự án mới được tạo, nếu giá trị **ID hợp đồng dự án** chưa tồn tại, nó sẽ được tạo tự động bằng cách sử dụng một chuỗi số. Giá trị bao gồm **ORD** , theo sau là một dãy số tăng dần và sau đó là một hậu tố gồm sáu ký tự. Đây là một ví dụ: **ORD-01022-Z4M9Q0**.

Trường **Số dự án** có sẵn trên trang **Dự án**. Trường này đã được tạo thành một chìa khóa tự nhiên và duy nhất để hỗ trợ quá trình tích hợp.

Khi dự án mới được tạo, nếu giá trị **Số dự án** chưa tồn tại, nó sẽ được tạo tự động bằng cách sử dụng một chuỗi số. Giá trị bao gồm **PRJ** , theo sau là một dãy số tăng dần và sau đó là một hậu tố gồm sáu ký tự. Đây là một ví dụ: **PRJ-01049-CCNID0**.

Khi áp dụng giải pháp tích hợp Project Service Automation với Finance, tập lệnh nâng cấp sẽ đặt trường **ID hợp đồng dự án** cho các hợp đồng dự án hiện có và trường **Số dự án** cho các dự án hiện có trong Project Service Automation.

## <a name="prerequisites-and-mapping-setup"></a>Điều kiện tiên quyết và thiết lập ánh xạ

- Trước khi quá trình đồng bộ hóa hợp đồng dự án và dự án có thể xảy ra, bạn phải đồng bộ hóa các tài khoản.
- Trong bộ kết nối của bạn, hãy thêm ánh xạ trường khóa tích hợp cho **msdyn\_organizationalunits** đến **msdyn\_name \[Name\]**. Trước tiên, bạn có thể cần thêm một dự án vào bộ kết nối. Để biết thêm thông tin, hãy xem [Tích hợp dữ liệu vào Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).
- Trong bộ kết nối của bạn, hãy thêm ánh xạ trường khóa tích hợp cho **msdyn\_projects** đến **msdynce\_projectnumber \[Project Number\]**. Trước tiên, bạn có thể cần thêm một dự án vào bộ kết nối. Để biết thêm thông tin, hãy xem [Tích hợp dữ liệu vào Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).
- **SourceDataID** cho các hợp đồng dự án và dự án có thể được cập nhật thành một giá trị khác hoặc loại bỏ khỏi ánh xạ. Giá trị mẫu mặc định là **Project Service Automation**.
- Ánh xạ **PaymentTerms** phải được cập nhật để phản ánh các điều khoản thanh toán hợp lệ trong Finance. Bạn cũng có thể loại bỏ ánh xạ khỏi nhiệm vụ dự án. Ánh xạ giá trị mặc định có các giá trị mặc định cho dữ liệu demo. Bảng sau đây cho thấy các giá trị trong Project Service Automation.

    | Giá trị | Mô tả   |
    |-------|---------------|
    | 1     | Tổng 30        |
    | 2     | 2% 10, Tổng 30 |
    | 3     | Tổng 45        |
    | 4     | Tổng 60        |

## <a name="power-query"></a>Power Query

Bạn phải sử dụng Microsoft Power Query dành cho Excel để lọc dữ liệu nếu các điều kiện sau được đáp ứng:

- Bạn có đơn đặt hàng trong Dynamics 365 Sales.
- Bạn có nhiều đơn vị tổ chức trong Project Service Automation và các đơn vị tổ chức này sẽ được ánh xạ tới nhiều pháp nhân trong Finance.

Nếu bạn phải sử dụng Power Query, hãy làm theo các nguyên tắc sau:

- Mẫu Dự án và hợp đồng (PSA sang Fin và Ops) có bộ lọc mặc định chỉ bao gồm đơn đặt hàng thuộc loại **Mục công việc (msdyn\_ordertype = 192350001)**. Bộ lọc này giúp đảm bảo rằng hợp đồng dự án không được tạo cho đơn đặt hàng trong Finance. Nếu bạn tạo mẫu của riêng mình, bạn phải thêm bộ lọc này.
- Bạn phải tạo bộ lọc Power Query chỉ bao gồm các tổ chức hợp đồng sẽ được đồng bộ hóa với pháp nhân của bộ kết nối tích hợp. Ví dụ: các hợp đồng dự án mà bạn có với đơn vị tổ chức hợp đồng của Contoso US phải được đồng bộ hóa với pháp nhân USSI, nhưng các hợp đồng dự án mà bạn có với đơn vị tổ chức hợp đồng của Contoso Global phải được đồng bộ hóa với pháp nhân USMF. Nếu bạn không thêm bộ lọc này vào ánh xạ nhiệm vụ của mình, tất cả các hợp đồng dự án sẽ được đồng bộ hóa với pháp nhân được xác định cho bộ kết nối, bất kể đơn vị tổ chức hợp đồng là gì.

## <a name="template-mapping-in-data-integration"></a>Ánh xạ mẫu trong tích hợp dữ liệu

> [!NOTE] 
> Các trường **CustomerReference** , **AddressCity** , **AddressCountryRegionID** , **AddressDescription** , **AddressLine1** , **AddressLine2** , **AddressState** , and **AddressZipCode** không được bao gồm trong ánh xạ mặc định cho hợp đồng dự án. Bạn có thể thêm các ánh xạ nếu bạn yêu cầu dữ liệu này được đồng bộ hóa cho các hợp đồng dự án.
>
> Các trường **Description** , **ParentID** , **ProjectGroup** , **ProjectManagerPersonnelNumber** và **ProjectType** không được bao gồm trong ánh xạ mặc định cho dự án. Bạn có thể thêm các ánh xạ nếu bạn yêu cầu dữ liệu này được đồng bộ hóa cho các dự án.

Các hình sau đây minh họa các ví dụ về việc ánh xạ nhiệm vụ mẫu trong Tích hợp dữ liệu. Tùy chọn ánh xạ hiển thị thông tin trường sẽ được đồng bộ hóa từ Project Service Automation sang Finance.

[![Ánh xạ mẫu hợp đồng dự án](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![Ánh xạ mẫu dự án](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![Ánh xạ mẫu mô tả hợp đồng dự án](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![Ánh xạ mẫu mốc thời gian mô tả hợp đồng dự án](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)

#### <a name="project-contract-line-milestone-mapping-in-the-projects-and-contracts-psa-3x-to-dynamics---v2-template"></a>Ánh xạ mốc thời gian mô tả hợp đồng dự án trong Dự án và Hợp đồng (PSA 3.x sang Dynamics) - mẫu v2:

[![Ánh xạ mốc thời gian mô tả hợp đồng dự án với phiên bản 2 mẫu](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)