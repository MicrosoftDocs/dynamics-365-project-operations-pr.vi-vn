---
title: Đồng bộ hóa danh mục chi phí của dự án giữa Finance and Operations và Project Service Automation
description: Chủ đề này mô tả các mẫu và nhiệm vụ cơ bản dùng để đồng bộ hóa các danh mục chi phí của dự án giữa Microsoft Dynamics 365 Finance và Dynamics 365 Project Service Automation.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 2816d363dbfe6ef2d98a584b214f72d9b30c49bb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999877"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Đồng bộ hóa danh mục chi phí của dự án giữa Finance and Operations và Project Service Automation

[!include[banner](../includes/banner.md)]

Chủ đề này mô tả các mẫu và nhiệm vụ cơ bản dùng để đồng bộ hóa các danh mục chi phí của dự án giữa Dynamics 365 Finance và Dynamics 365 Project Service Automation.

> [!NOTE]
> - Tính năng tích hợp nhiệm vụ dự án, thể loại giao dịch chi phí, ước tính giờ, ước tính chi phí và khóa chức năng có sẵn trong phiên bản 8.0.
> - Tùy chọn tích hợp giá trị thực tế có sẵn từ phiên bản 8.0.1.
> - Nếu bạn đang sử dụng Enterprise Edition 7.3.0, sau khi cài đặt KB 4132657 và KB 4132660, thì bạn sẽ có thể sử dụng các mẫu để tích hợp nhiệm vụ dự án, danh mục giao dịch chi phí, các giá trị ước tính giờ, ước tính chi phí và giá trị thực tế để đặt cấu hình tùy chọn khóa chức năng. Nếu bạn phải đặt lại các bản phân bổ kế toán, thì chúng tôi khuyên bạn cũng nên cài đặt KB 4131710.

## <a name="data-flow-for-project-service-automation-and-finance"></a>Luồng dữ liệu cho Project Service Automation và Finance

Giải pháp tích hợp Project Service Automation và Finance sử dụng tính năng Tích hợp dữ liệu để đồng bộ hóa dữ liệu giữa các phiên bản của Project Service Automation và Finance. Các mẫu tích hợp có sẵn với tính năng Tích hợp dữ liệu sẽ tạo ra luồng dữ liệu về các danh mục giao dịch chi phí của dự án giữa Finance và Project Service Automation.

Nếu các danh mục chi phí dự án được tạo chính trong Finance, thì quy trình tích hợp trước tiên là từ Finance sang Project Service Automation. Sau đó, ID tích hợp của các danh mục chi phí của dự án được cập nhật thông qua hoạt động đồng bộ hóa từ Project Service Automation sang Finance.

Nếu các danh mục chi phí dự án được tạo chính trong Project Service Automation, thì quy trình tích hợp trước tiên là từ Project Service Automation sang Finance. Các danh mục dự án phải được đặt cấu hình sẵn trong Finance trước khi đồng bộ hóa từ Project Service Automation. Sau đó, đồng bộ hóa từ Finance trở lại Project Service Automation, rồi lại từ Project Service Automation sang Finance. Bằng cách này, bạn bảo đảm rằng các danh mục được liên kết và không có bản trùng lặp nào được tạo.

> [!NOTE]
> Thông thường, các danh mục chi phí của dự án được tạo chính trong Finance. Tuy nhiên, nếu bạn gặp trường hợp không phải như thế hoặc nếu danh mục chi phí đã được tạo sẵn trong Project Service Automation, thì trước tiên, bạn phải đồng bộ hóa bằng mẫu Danh mục giao dịch chi phí của dự án (PSA sang Fin and Ops). Sau đó, đồng bộ hóa bằng mẫu Danh mục giao dịch chi phí của dự án (Fin and Ops sang PSA). Tiếp đến, bạn nên chạy đồng bộ hóa từ Project Service Automation sang Finance một lần nữa.
>
> Nếu bạn đồng bộ hóa trước tiên từ Project Service Automation, thì các yêu cầu sau phải được đáp ứng trong Finance trước khi chạy đồng bộ hóa:
>
> - Danh mục dùng chung khớp với danh mục dự án được thiết lập trong Project Service Automation phải tồn tại và phải được bật cho cả **Dự án** và **Chi phí**.
> - Đối với mỗi pháp nhân Finance cần phải tích hợp, các danh mục dự án sau phải tồn tại:
>
>     - **Danh mục dự án** tồn tại. 
>     - **Sử dụng trong chi phí** được kích hoạt.
>     - **Hoạt động trong nhật ký** được kích hoạt.
>     - **Loại giao dịch** được đặt thành **Chi phí**.

Hình minh họa sau đây cho thấy cách dữ liệu được đồng bộ hóa giữa Project Service Automation và Finance.

[![Luồng dữ liệu cho phần tích hợp Project Service Automation với Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a>Đồng bộ hóa danh mục chi phí của dự án từ Finance sang Project Service Automation

### <a name="template-and-task"></a>Mẫu và nhiệm vụ

Để truy cập vào mẫu, trong trung tâm quản trị Microsoft Power Apps, chọn **Dự án** và sau đó, ở góc trên bên phải, chọn **Dự án mới** để chọn các mẫu công khai.

Mẫu sau và nhiệm vụ cơ bản được sử dụng để đồng bộ hóa các danh mục chi phí của dự án từ Finance sang Project Service Automation:

- **Tên mẫu trong Tích hợp dữ liệu:** Danh mục giao dịch chi phí của dự án (Fin and Ops sang PSA)
- **Tên nhiệm vụ trong dự án:** Đồng bộ hóa danh mục với PSA

### <a name="entity-set"></a>Bộ thực thể

| Tài chính                           | Project Service Automation |
|-----------------------------------|----------------------------|
| Thực thể tích hợp cho các danh mục | Danh mục giao dịch     |

### <a name="entity-flow"></a>Luồng thực thể

Các danh mục chi phí của dự án được quản lý trong Finance và được đồng bộ hóa với Project Service Automation dưới dạng danh mục giao dịch.

### <a name="power-query"></a>Power Query

Khi đồng bộ hóa với Project Service Automation, bạn phải sử dụng Microsoft Power Query dành cho Excel để thiết lập loại thanh toán trên danh mục giao dịch. Mẫu Danh mục giao dịch chi phí của dự án (Fin and Ops sang PSA) cung cấp một cột và tùy chọn ánh xạ mặc định. Nếu bạn tạo mẫu của riêng mình, thì bạn phải thêm cột có điều kiện trong Power Query. Làm theo các bước sau.

1. Bấm vào mũi tên để mở mục ánh xạ nhiệm vụ danh mục chi phí của dự án trong mẫu Danh mục giao dịch chi phí của dự án (Fin and Ops sang PSA).
2. Bấm vào liên kết **Truy vấn nâng cao và lọc** để mở Power Query.
2. Chọn **Thêm cột có điều kiện**.
3. Nhập tên cho cột mới, chẳng hạn như **Loại lập hóa đơn**.
4. Nhập điều kiện sau: **nếu CATEGORYID không rỗng thì phải là giá trị 19235001, nếu không thì là rỗng**.
5. Bấm vào **OK** trên cột.
6. Bảo đảm ánh xạ cột mới này trên trang ánh xạ.

Hình sau đây minh họa một ví dụ về việc ánh xạ nhiệm vụ mẫu trong Tích hợp dữ liệu. Tùy chọn ánh xạ hiển thị thông tin trường sẽ được đồng bộ hóa từ Finance sang Project Service Automation.

[![Ánh xạ mẫu danh mục chi phí của dự án với mẫu Project Service Automation](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a>Đồng bộ hóa danh mục chi phí của dự án từ Project Service Automation sang Finance

### <a name="template-and-task"></a>Mẫu và nhiệm vụ

Mẫu sau và nhiệm vụ cơ bản được sử dụng để đồng bộ hóa các danh mục chi phí của dự án từ Project Service Automation sang Finance:

- **Tên mẫu trong Tích hợp dữ liệu:** Danh mục giao dịch chi phí của dự án (PSA sang Fin and Ops)
- **Tên nhiệm vụ trong dự án:** Đồng bộ hóa danh mục với Fin Ops

### <a name="entity-set"></a>Bộ thực thể

| Project Service Automation | Tài chính                           |
|----------------------------|-----------------------------------|
| Danh mục giao dịch     | Thực thể tích hợp cho các danh mục |

### <a name="entity-flow"></a>Luồng thực thể

Các danh mục chi phí của dự án được quản lý trong Finance và được đồng bộ hóa với Project Service Automation dưới dạng danh mục giao dịch. Hoạt động đồng bộ hóa trở lại Finance sẽ cập nhật danh mục dự án trong Finance với ID tích hợp từ Project Service Automation.

### <a name="template-mapping-in-data-integration"></a>Ánh xạ mẫu trong tích hợp dữ liệu

Hình sau đây minh họa một ví dụ về việc ánh xạ nhiệm vụ mẫu trong Tích hợp dữ liệu.

> [!NOTE]
> Tùy chọn ánh xạ hiển thị thông tin trường sẽ được đồng bộ hóa từ Project Service Automation sang Finance.

[![Ánh xạ mẫu Project Service Automation với Finance](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]