---
title: Đồng bộ hóa các dự toán dự án trực tiếp từ Tự động hóa dịch vụ dự án đến Tài chính và Vận hành
description: Chủ đề này mô tả các mẫu và nhiệm vụ cơ bản được sử dụng để đồng bộ hóa ước tính giờ dự án và ước tính chi phí dự án trực tiếp từ Microsoft Dynamics 365 Project Service Automation tới Dynamics 365 Finance.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 47de3556034227e072d14dc93908edec42cec93c
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684622"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a>Đồng bộ hóa các dự toán dự án trực tiếp từ Tự động hóa dịch vụ dự án đến Tài chính và Vận hành

[!include[banner](../includes/banner.md)]

Chủ đề này mô tả các mẫu và nhiệm vụ cơ bản được sử dụng để đồng bộ hóa ước tính giờ dự án và ước tính chi phí dự án trực tiếp từ Dynamics 365 Project Service Automation tới Dynamics 365 Finance.

> [!NOTE]
> - Tính năng tích hợp nhiệm vụ dự án, thể loại giao dịch chi phí, ước tính giờ, ước tính chi phí và khóa chức năng có sẵn trong phiên bản 8.0.
> - Tùy chọn tích hợp giá trị thực tế có sẵn từ phiên bản 8.0.1.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Luồng dữ liệu cho Project Service Automation sang Finance

Giải pháp tích hợp Project Service Automation sang Finance sử dụng tính năng Tích hợp dữ liệu để đồng bộ hóa dữ liệu giữa các phiên bản của Project Service Automation và Finance. Các mẫu tích hợp có sẵn với tính năng Tích hợp dữ liệu sẽ tạo ra luồng dữ liệu về các các ước tính số giờ dự án và ước tính chi phí dự án từ Project Service Automation sang Finance.

Hình minh họa sau đây cho thấy cách dữ liệu được đồng bộ hóa giữa Project Service Automation và Finance.

[![Luồng dữ liệu cho phần tích hợp Project Service Automation với Finance.](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)

## <a name="project-hour-estimates"></a>Ước tính số giờ dự án

### <a name="template-and-tasks"></a>Mẫu và nhiệm vụ

Để truy cập các mẫu có sẵn, trong trung tâm quản trị Microsoft Power Apps, chọn **Dự án** và sau đó, ở góc trên bên phải, chọn **Dự án mới** để chọn các mẫu công khai.

Mẫu sau và các nhiệm vụ cơ bản được sử dụng để đồng bộ hóa ước tính giờ dự án từ Project Service Automation sang Finance:

- **Tên mẫu trong Tích hợp dữ liệu:** Ước tính giờ dự án (PSA sang Fin and Ops)
- **Tên của nhiệm vụ trong dự án:**

    - Các mối quan hệ giao dịch
    - Ước tính chi phí

### <a name="entity-set"></a>Bộ thực thể

| Project Service Automation | Tài chính                                       |
|----------------------------|-----------------------------------------------|
| Nhiệm vụ dự án              | Thực thể tích hợp cho ước tính giờ dự án |

### <a name="entity-flow"></a>Luồng thực thể

Ước tính giờ dự án được quản lý trong Project Service Automation và được đồng bộ hóa với Finance dưới dạng dự báo giờ dự án.

### <a name="prerequisites"></a>Điều kiện tiên quyết

Trước khi đồng bộ hóa ước tính giờ dự án có thể xảy ra, bạn phải đồng bộ hóa dự án, nhiệm vụ dự án và thể loại giao dịch chi phí dự án.

### <a name="power-query"></a>Power Query

Trong mẫu ước tính giờ dự án, bạn phải sử dụng Microsoft Power Query để Excel hoàn thành các tác vụ này:

- Thiết lập ID mô hình dự báo mặc định sẽ được sử dụng khi tùy chọn tích hợp tạo dự báo giờ mới.
- Lọc ra bất kỳ bản ghi nguồn lực cụ thể nào trong nhiệm vụ sẽ không tích hợp được vào dự báo giờ.
- Lọc ra bất kỳ hàng thể loại giao dịch trống nào. Không hoàn thành nhiệm vụ này có thể dẫn đến việc dự báo giờ không chính xác.

#### <a name="set-the-default-forecast-model-id"></a>Thiết lập ID mô hình dự báo mặc định

Để cập nhật ID mô hình dự báo mặc định trong mẫu, hãy bấm vào mũi tên **Bản đồ** để mở phần ánh xạ. Sau đó, chọn liên kết **Truy vấn nâng cao và lọc**.

- Nếu bạn đang sử dụng mẫu Ước tính giờ dự án mặc định (PSA sang Fin and Ops) mặc định, hãy chọn **Điều kiện đã chèn** trong danh sách **Các bước được áp dụng**. Trong mục nhập **Hàm**, thay **O\_forecast** bằng tên của ID mô hình dự đoán sẽ dùng với tùy chọn tích hợp. Mẫu mặc định có ID mô hình dự báo từ dữ liệu demo.
- Nếu bạn đang tạo một mẫu mới, bạn phải thêm cột này. Trong Power Query, lựa chọn **Thêm cột có điều kiện** và nhập tên cho cột mới, chẳng hạn như **ModelID**. Nhập điều kiện cho cột, trong đó, nếu nhiệm vụ dự án không phải là null, thì \<enter the forecast model ID\>; nếu không thì nhập null.

#### <a name="filter-out-resource-specific-records"></a>Lọc ra các bản ghi dành riêng cho nguồn lực

Mẫu ước tính giờ dự án (PSA sang Fin và Ops) có bộ lọc mặc định nhằm loại bỏ bất kỳ bản ghi dành riêng cho nguồn lực nào. Nếu bạn tạo mẫu của riêng mình, bạn phải thêm bộ lọc này. Chọn liên kết **Truy vấn nâng cao và lọc** để lọc trên cột **msdyn\_islinetask** sao cho chỉ bản ghi **False** được bao gồm.

#### <a name="filter-out-empty-transaction-category-rows"></a>Lọc ra các hàng thể loại giao dịch trống

Bạn phải thêm bộ lọc để loại bỏ bất kỳ hàng nào có thể loại giao dịch trống. Tác vụ này là bắt buộc, bất kể bạn đang sử dụng mẫu mặc định hay tạo mẫu của riêng mình. Bộ lọc này loại bỏ bất kỳ hàng tóm tắt nào ra khỏi Project Service Automation có thể khiến dự báo giờ trong Finance không chính xác. Chọn liên kết **Truy vấn nâng cao và lọc** để lọc các bản ghi null trong cột **msdyn\_transactioncategory\_value**.

### <a name="template-mapping-in-data-integration"></a>Ánh xạ mẫu trong tích hợp dữ liệu

Hình sau đây minh họa một ví dụ về việc ánh xạ nhiệm vụ mẫu trong Tích hợp dữ liệu. Tùy chọn ánh xạ hiển thị thông tin trường sẽ được đồng bộ hóa từ Project Service Automation sang Finance.

[![Ánh xạ nhiệm vụ mẫu trong tích hợp dữ liệu.](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

## <a name="project-expense-estimates"></a>Ước tính chi phí dự án

### <a name="template-and-tasks"></a>Mẫu và nhiệm vụ

Mẫu sau và các nhiệm vụ cơ bản được sử dụng để đồng bộ hóa ước tính chi phí dự án từ Project Service Automation sang Finance:

- **Tên mẫu trong Tích hợp dữ liệu:** Ước tính chi phí dự án (PSA sang Fin và Ops)
- **Tên của nhiệm vụ trong dự án:**

    - Các mối quan hệ giao dịch 
    - Ước tính chi phí

### <a name="entity-set"></a>Bộ thực thể

| Project Service Automation | Tài chính                                                  |
|----------------------------|----------------------------------------------------------|
| Kết nối Giao dịch    | Thực thể tích hợp cho các mối quan hệ giao dịch dự án |
| Mô tả Ước tính             | Thực thể tích hợp cho ước tính chi phí dự án         |

### <a name="entity-flow"></a>Luồng thực thể

Ước tính chi phí dự án được quản lý trong Project Service Automation và được đồng bộ hóa với Finance dưới dạng dự báo chi phí dự án.

### <a name="prerequisites"></a>Điều kiện tiên quyết

Trước khi đồng bộ hóa ước tính chi phí dự án có thể xảy ra, bạn phải đồng bộ hóa dự án, nhiệm vụ dự án và thể loại giao dịch chi phí dự án.

### <a name="power-query"></a>Power Query

Trong mẫu ước tính chi phí dự án, bạn phải sử dụng Power Query để hoàn thành các nhiệm vụ sau:

- Lọc để chỉ bao gồm các bản ghi dòng ước tính chi phí.
- Thiết lập ID mô hình dự báo mặc định sẽ được sử dụng khi tùy chọn tích hợp tạo dự báo giờ mới.
- Chuyển đổi các loại thanh toán.
- Chuyển đổi các loại giao dịch.

#### <a name="filter-to-include-only-expense-estimate-lines"></a>Lọc để chỉ bao gồm các dòng ước tính chi phí

Mẫu ước tính chi phí dự án (PSA sang Fin và Ops) có bộ lọc mặc định chỉ bao gồm các dòng chi phí trong tích hợp. Nếu bạn tạo mẫu của riêng mình, bạn phải thêm bộ lọc này. Chọn nhiệm vụ **Mối quan hệ giao dịch** rồi nhấp vào mũi tên **Bản đồ** để mở ánh xạ. Chọn liên kết **Truy vấn nâng cao và lọc**. Lọc cột **msdyn\_transactiontype1** đê chỉ bao gồm **msdyn\_estimateline**.

#### <a name="set-the-default-forecast-model-id"></a>Thiết lập ID mô hình dự báo mặc định

Để cập nhật ID mô hình dự báo mặc định trong mẫu, hãy chọn nhiệm vụ **Ước tính chi phí** rồi nhấp vào mũi tên **Bản đồ** để mở ánh xạ. Chọn liên kết **Truy vấn nâng cao và lọc**.

- Nếu bạn đang sử dụng mẫu ước tính chi phí Dự án (PSA to Fin và Ops) mặc định, trong Power Query, chọn cái đầu tiên **Điều kiện đã chèn** từ **Các bước áp dụng** tiết diện. Trong mục nhập **Hàm**, thay **O\_forecast** bằng tên của ID mô hình dự đoán sẽ dùng với tùy chọn tích hợp. Mẫu mặc định có ID mô hình dự báo từ dữ liệu demo.
- Nếu bạn đang tạo một mẫu mới, bạn phải thêm cột này. Trong Power Query, lựa chọn **Thêm cột có điều kiện** và nhập tên cho cột mới, chẳng hạn như **ModelID**. Nhập điều kiện cho cột, trong đó, nếu ID dòng ước tính không phải là null, thì \<enter the forecast model ID\>; nếu không thì nhập null.

#### <a name="transform-the-billing-types"></a>Chuyển đổi các loại thanh toán

Mẫu ước tính chi phí dự án (PSA sang Fin và Ops) bao gồm một cột có điều kiện được sử dụng để chuyển đổi các loại lập hóa đơn nhận được từ Project Service Automation trong quá trình tích hợp. Nếu bạn tạo mẫu của riêng mình, bạn phải thêm cột điều kiện này. Chọn liên kết **Truy vấn nâng cao và lọc** rồi chọn **Thêm cột bổ sung**. Nhập tên cho cột mới, chẳng hạn như **Loại lập hóa đơn**. Sau đó, nhập điều kiện sau:

If **msdyn\_billingtype** = 192350000, then **NonChargeable**  
else if **msdyn\_billingtype** = 192350001, then **Chargeable**  
else if **msdyn\_billingtype** = 192350002, then **Complimentary**  
else **NotAvailable**

#### <a name="transform-the-transaction-types"></a>Chuyển đổi các loại giao dịch

Mẫu ước tính chi phí dự án (PSA sang Fin và Ops) bao gồm một cột có điều kiện được sử dụng để chuyển đổi các loại giao dịch nhận được từ Project Service Automation trong quá trình tích hợp. Nếu bạn tạo mẫu của riêng mình, bạn phải thêm cột điều kiện này. Chọn liên kết **Truy vấn nâng cao và lọc** rồi chọn **Thêm cột bổ sung**. Nhập tên cho cột mới, chẳng hạn như **Loại giao dịch**. Sau đó, nhập điều kiện sau:

If **msdyn\_transactiontypecode** = 192350000, then **Cost**  
else if **msdyn\_transactiontypecode** = 192350005, then **Sales**  
else **null**

### <a name="template-mapping-in-data-integration"></a>Ánh xạ mẫu trong tích hợp dữ liệu

Các hình sau đây minh họa các ví dụ về việc ánh xạ nhiệm vụ mẫu trong Tích hợp dữ liệu. Tùy chọn ánh xạ hiển thị thông tin trường sẽ được đồng bộ hóa từ Project Service Automation sang Finance.

[![Ánh xạ mẫu của giao dịch ước tính chi phí.](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![Ánh xạ mẫu của ước tính chi phí.](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]