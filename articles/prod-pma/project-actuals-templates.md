---
title: Đồng bộ hóa trực tiếp các giá trị thực tế trong dự án từ Project Service Automation vào nhật ký tích hợp dự án để đăng trong Finance and Operations
description: Chủ đề này mô tả các mẫu và nhiệm vụ cơ bản dùng để đồng bộ hóa trực tiếp các giá trị thực tế trong dự án từ Microsoft Dynamics 365 Project Service Automation sang Finance and Operations.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 85b6c07464e919e363f28d8bc62115e8fb4c72ea6631269b98fd00f324a01cba
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988137"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>Đồng bộ hóa trực tiếp các giá trị thực tế trong dự án từ Project Service Automation vào nhật ký tích hợp dự án để đăng trong Finance and Operations

[!include[banner](../includes/banner.md)]

Chủ đề này mô tả các mẫu và nhiệm vụ cơ bản dùng để đồng bộ hóa trực tiếp các giá trị thực tế trong dự án từ Dynamics 365 Project Service Automation sang Dynamics 365 Finance.

Mẫu này đồng bộ hóa các giao dịch từ Project Service Automation sang một bảng dàn trong Finance. Sau khi quá trình đồng bộ hóa hoàn tất, bạn **phải** nhập dữ liệu từ bảng dàn vào nhật ký tích hợp.

> [!NOTE]
> - Tùy chọn tích hợp giá trị thực tế trong dự án có sẵn từ phiên bản 8.0.1.
> - Nếu bạn đang sử dụng phiên bản Enterprise 7.3.0 sau khi cài đặt KB 4132657 và KB 4132660, thì bạn sẽ có thể sử dụng các mẫu để tích hợp nhiệm vụ dự án, danh mục giao dịch chi phí, các giá trị ước tính giờ, ước tính chi phí và giá trị thực tế để đặt cấu hình tùy chọn khóa chức năng. Nếu bạn phải đặt lại các bản phân bổ kế toán, thì chúng tôi khuyên bạn cũng nên cài đặt KB 4131710.
> - Nếu bạn đang sử dụng phiên bản 7.3.0 và bạn đang chuyển các giao dịch phí từ Project Service Automation, bạn phải cài đặt KB 4345320 để bao gồm các khoản phí đó trong hóa đơn dự án.
> - Nếu bạn đang nhập số tiền thuế bán hàng vào các giao dịch thời gian hoặc chi phí trong Project Service Automation, thì bạn phải cài đặt Project Service Automation bản cập nhật 7. Nếu không, các giá trị thuế thực tế sẽ không được liên kết với các giá trị thời gian hoặc chi phí thực tế có liên quan và chúng sẽ không được đồng bộ hóa với Finance. Để biết thêm thông tin, hãy liên hệ với bộ phận Hỗ trợ.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Luồng dữ liệu cho Project Service Automation sang Finance

Giải pháp tích hợp Project Service Automation sang Finance sử dụng tính năng Tích hợp dữ liệu để đồng bộ hóa dữ liệu giữa các phiên bản của Project Service Automation và Finance. Các mẫu tích hợp có sẵn với tính năng Tích hợp dữ liệu sẽ tạo ra luồng dữ liệu về giá trị thực tế trong dự án từ Project Service Automation đến Finance.

Hình minh họa sau đây cho thấy cách dữ liệu được đồng bộ hóa giữa Project Service Automation và Finance.

[![Luồng dữ liệu cho phần tích hợp Project Service Automation với Finance and Operations.](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)

## <a name="project-actuals-from-project-service-automation"></a>Giá trị thực tế trong dự án từ Project Service Automation

### <a name="template-and-tasks"></a>Mẫu và nhiệm vụ

Để truy cập các mẫu có sẵn, trong trung tâm quản trị Microsoft Power Apps, chọn **Dự án** và sau đó, ở góc trên bên phải, chọn **Dự án mới** để chọn các mẫu công khai.

Mẫu sau và các nhiệm vụ cơ bản được sử dụng để đồng bộ hóa giá trị thực tế trong dự án từ Project Service Automation sang Finance:

- **Tên mẫu trong Tích hợp dữ liệu:** Giá trị thực tế trong dự án (PSA sang Fin and Ops)
- **Tên của nhiệm vụ trong dự án:**

    - Thực tế
    - Kết nối giao dịch

### <a name="entity-set"></a>Bộ thực thể

| Project Service Automation | Tài chính                                   |
|----------------------------|----------------------------------------------------------|
| Thực tế                    | Thực thể tích hợp cho các giá trị thực tế trong dự án                   |
| Kết nối Giao dịch    | Thực thể tích hợp cho các mối quan hệ giao dịch dự án |

### <a name="entity-flow"></a>Luồng thực thể

Các giá trị thực tế trong dự án được quản lý trong Project Service Automation và được đồng bộ hóa với nhật ký tích hợp dự án trong Finance. Hoạt động kế toán sẽ được áp dụng dựa trên các yếu tố tài chính mặc định và phần thiết lập đăng.

### <a name="prerequisites"></a>Điều kiện tiên quyết

Trước khi việc đồng bộ hóa giá trị thực tế có thể thực hiện, bạn phải đặt cấu hình các tham số tích hợp Project Service Automation và đồng bộ hóa dự án, nhiệm vụ trong dự án và danh mục giao dịch chi phí dự án.

### <a name="power-query"></a>Power Query

Trong mẫu giá trị thực tế trong dự án, bạn phải sử dụng Microsoft Power Query dành cho Excel để hoàn thành các nhiệm vụ sau:

- Chuyển loại giao dịch trong Project Service Automation thành loại giao dịch chính xác trong Finance. Sự chuyển đổi này đã được xác định trong mẫu Giá trị thực tế trong dự án (PSA sang Fin and Ops).
- Chuyển loại thanh toán trong Project Service Automation thành loại thanh toán chính xác trong Finance. Sự chuyển đổi này đã được xác định trong mẫu Giá trị thực tế trong dự án (PSA sang Fin and Ops). Sau đó, loại thanh toán này được ánh xạ với thuộc tính dòng, dựa trên cấu hình trên trang **Tham số tích hợp Project Service Automation**.
- Lọc các đơn vị tổ chức nguồn lực cụ thể phải được đồng bộ hóa với mẫu này.
- Nếu các giá trị thời gian hoặc chi phí thực tế liên công ty sẽ được đồng bộ hóa với Finance, thì bạn phải chuyển đổi đơn vị tổ chức trong hợp đồng thành pháp nhân phù hợp trong Finance. Trong mẫu Giá trị thực tế trong dự án (PSA sang Fin and Ops), một cột có điều kiện được xác định dựa trên dữ liệu demo. Bạn phải cập nhật cột có điều kiện được chèn gần đây nhất cho đúng pháp nhân. Nếu không, có thể xảy ra lỗi tích hợp hoặc các giao dịch thực tế không chính xác có thể được nhập vào Finance.
- Nếu các giá trị thời gian hoặc chi phí thực tế liên công ty sẽ không được đồng bộ hóa với Finance, thì bạn phải xóa cột có điều kiện được chèn gần đây nhất khỏi mẫu của bạn. Nếu không, có thể xảy ra lỗi tích hợp hoặc các giao dịch thực tế không chính xác có thể được nhập vào Finance.

#### <a name="contract-organizational-unit"></a>Đơn vị tổ chức trong hợp đồng
Để cập nhật cột có điều kiện đã chèn trong mẫu, hãy bấm vào mũi tên **Bản đồ** để mở phần ánh xạ. Chọn liên kết **Truy vấn nâng cao và lọc** để mở Power Query.

- Nếu bạn đang sử dụng mẫu Giá trị thực tế trong dự án (PSA sang Fin and Ops) mặc định, thì trong Power Query, hãy chọn **Điều kiện đã chèn** ở phần **Các bước được áp dụng**. Trong mục nhập **Hàm**, thay **USSI** bằng tên của pháp nhân sẽ dùng với phần tích hợp. Thêm các điều kiện bổ sung vào mục nhập **Hàm** theo như yêu cầu của bạn và cập nhật điều kiện **khác** từ **USMF** thành đúng pháp nhân.
- Nếu bạn tạo mẫu mới, thì bạn phải thêm cột để hỗ trợ các mục thời gian và chi phí liên công ty. Chọn **Thêm cột có điều kiện** và nhập tên cho cột, chẳng hạn như **Pháp nhân**. Nhập điều kiện cho cột, trong đó, nếu **msdyn\_contractorganizationalunitid.msdyn\_name** là \<organizational unit\>, thì \<enter the legal entity\>; nếu không thì nhập null.

### <a name="template-mapping-in-data-integration"></a>Ánh xạ mẫu trong tích hợp dữ liệu

Các hình sau đây minh họa một ví dụ về việc ánh xạ nhiệm vụ mẫu trong Tích hợp dữ liệu. Tùy chọn ánh xạ hiển thị thông tin trường sẽ được đồng bộ hóa từ Project Service Automation sang Finance.

[![Ánh xạ mẫu - Thực tế.](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Ánh xạ mẫu - Kết nối giao dịch.](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a>Nhập từ bảng dàn sau khi tích hợp từ Project Service Automation

Quy trình định kỳ Nhập từ bảng dàn phải được chạy sau khi đồng bộ hóa các giá trị thực tế từ Project Service Automation sang Finance. Quy trình này sẽ nhập các giao dịch dự án từ bảng dàn vào nhật ký tích hợp Project Service Automation, nơi áp dụng hoạt động kế toán và các giao dịch đã nhập có thể được đăng. Chúng tôi khuyên bạn nên chạy quy trình này ở chế độ hàng loạt, bạn có thể tùy ý thiết lập để chạy tùy chọn này như một lô định kỳ.

## <a name="update-actuals-from-finance"></a>Cập nhật giá trị thực tế từ Finance

### <a name="template-and-tasks"></a>Mẫu và nhiệm vụ

Mẫu sau và các nhiệm vụ cơ bản sau được sử dụng để đồng bộ hóa số chứng từ và thuế bán hàng cho các giao dịch dự án đã đăng từ Finance vào Project Service Automation:

- **Tên mẫu trong Tích hợp dữ liệu:** Cập nhật giá trị thực tế trong dự án (Fin Ops sang PSA)
- **Tên của nhiệm vụ trong dự án:**

    - Thực tế 
    - Kết nối giao dịch

### <a name="entity-set"></a>Bộ thực thể

| Tài chính                                                  | Project Service Automation |
|----------------------------------------------------------|----------------------------|
| Thực thể tích hợp cho các giá trị thực tế trong dự án                   | Thực tế                    |
| Thực thể tích hợp cho các mối quan hệ giao dịch dự án | Kết nối Giao dịch    |

### <a name="entity-flow"></a>Luồng thực thể

Các giá trị thực tế trong dự án được quản lý trong Project Service Automation và được đồng bộ hóa với nhật ký tích hợp dự án trong Finance. Sau khi các giá trị thực tế được đăng trên Finance, chúng được cập nhật trong Project Service Automation với số chứng từ từ Finance. Nếu thuế bán hàng được thêm ở Finance, các giá trị thuế thực tế mới sẽ được tạo ở Project Service Automation.

### <a name="power-query"></a>Power Query

Trong mẫu cập nhật giá trị thực tế trong dự án, bạn phải sử dụng Power Query để hoàn thành các nhiệm vụ sau:

- Chuyển loại giao dịch trong Finance thành loại giao dịch chính xác trong Project Service Automation. Sự chuyển đổi này đã được xác định trong mẫu Cập nhật giá trị thực tế trong dự án (Fin Ops sang PSA).
- Chuyển loại thanh toán trong Finance thành loại thanh toán chính xác trong Project Service Automation. Sự chuyển đổi này đã được xác định trong mẫu Cập nhật giá trị thực tế trong dự án (Fin Ops sang PSA).

### <a name="template-mapping-in-data-integration"></a>Ánh xạ mẫu trong tích hợp dữ liệu

Các hình sau đây minh họa các ví dụ về việc ánh xạ nhiệm vụ mẫu trong Tích hợp dữ liệu. Tùy chọn ánh xạ hiển thị thông tin trường sẽ được đồng bộ hóa từ Finance sang Project Service Automation.

[![Ánh xạ mẫu - Cập nhật giá trị thực tế.](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Ánh xạ mẫu - Cập nhật giao dịch.](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]