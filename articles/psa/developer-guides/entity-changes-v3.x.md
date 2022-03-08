---
title: Thay đổi thực thể, kiểm soát và giao diện người dùng (Project Service Automation 3.x)
description: Chủ đề này mô tả các thay đổi giả pháp cho Microsoft Dynamics Project Service Automation 3.x.
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 03/15/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 86b51e58189a62f15a5ded039e9265733a0d9d4a7c7bf8d18ac46aadf1d2a931
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987372"
---
# <a name="entity-control-and-user-interface-changes-project-service-automation-3x"></a>Thay đổi thực thể, kiểm soát và giao diện người dùng (Project Service Automation 3.x)

[!include [banner](../../includes/psa-now-project-operations.md)]


Với việc phát hành Microsoft Dynamics Project Service Automation (PSA) 3.x, nhiều thay đổi đã được thực hiện cho các thực thể, kiểm soát, dạng xem và giao diện người dùng. Chủ đề này cung cấp thông tin quan trọng về các thay đổi quan trọng sau:

## <a name="parent-child-relationships-for-sales-document-sales-document-line-sales-document-line-detail-entities"></a>Mối quan hệ chính-phụ cho thực thể tài liệu bán hàng, dòng tài liệu bán hàng, chi tiết dòng tài liệu bán hàng
Trong phiên bản Dynamics 365 Project Service Automation (PSA) phát hành trước phiên bản 3.0, một số mối quan hệ giữa các thực thể tài liệu bán hàng, dòng tài liệu bán hàng và chi tiết dòng tài liệu kinh doanh được thực hiện thông qua các trường chuỗi sẽ giữ một đại diện chuỗi của GUID của thực thể liên quan. Điều này là do những hạn chế về nền tảng yêu cầu mã tùy chỉnh chính phía máy chủ và máy khách của giải pháp để làm cho các mối quan hệ đó hoạt động tương tự như các mối quan hệ thực thể Dynamics CRM điển hình và để làm cho các trường chuỗi hoạt động như trường tra cứu.

PSA 3.0 đã được cập nhật để tận dụng các mối quan hệ thực thể mới giữa thực thể tài liệu bán hàng và dòng tài liệu bán hàng.

Vì hiện có thể sử dụng trường tra cứu để cho biết tham chiếu đến thực thể, các trường giữ giá trị chuỗi GUID của thực thể liên quan trong các phiên bản trước không còn cần thiết nên đã cho ngừng sử dụng. Mã phía máy chủ và máy khách tùy chỉnh xử lý mối quan hệ được xác định bằng các trường chuỗi cũ cũng bị ngừng sử dụng.

### <a name="entity-schema-changes"></a>Thay đổi sơ đồ thực thể
Bảng sau đây cung cấp một danh sách trực tiếp các trường chuỗi không còn dùng nữa và trường tra cứu mới cho các thực thể. 

 Thực thể |   Trường đã ngừng sử dụng (Chuỗi) | Trường mới (Tra cứu)
--- | --- | ---
invoicedetail (Dòng hóa đơn) |  msdyn_contractline |    msdyn_contractlineid
msdyn_actual (Thực tế) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_contractlineinvoiceschedule (Lịch trình hóa đơn dòng hợp đồng dự án) |    msdyn_contractline |    msdyn_contractlineid
msdyn_contractlinescheduleofvalue (Mốc dòng hợp đồng dự án) |   msdyn_contractline |    msdyn_contractlineid
msdyn_fact (Thực tế) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_invoicelinetransaction (Chi tiết dòng hóa đơn) | msdyn_invoiceline <br> msdyn_salescontractline | msdyn_invoicelineid <br> msdyn_salescontractlineid
msdyn_journalline (Dòng nhật ký kế toán) |  msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlineresourcecategory (Danh mục nguồn lực dòng hợp đồng dự án) | msdyn_salescontractline |   msdyn_contractlineid
msdyn_orderlinetransaction (Chi tiết dòng hợp đồng dự án) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlinetransactioncategory (Loại giao dịch dòng hợp đồng dự án) |   msdyn_contractline |    msdyn_contractlineid
msdyn_orderlinetransactionclassification (Phân loại giao dịch dòng hợp đồng dự án) |   msdyn_contractline |    msdyn_contractlineid
msdyn_quotelineinvoiceschedule (Lịch trình hóa đơn dòng báo giá) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelineresourcecategory (Thể loại nguồn lực dòng báo giá) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinescheduleofvalue (Mốc dòng báo giá) | msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransaction (Chi tiết dòng báo giá) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactioncategory (Danh mục giao dịch dòng báo giá) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactionclassification (Phân loại giao dịch dòng báo giá) |  msdyn_quoteline |   msdyn_quotelineid
SalesOrderDetail (Dòng đơn đặt hàng) | msdyn_quotelineid | msdyn_quoteline 

### <a name="deprecated-custom-views-and-controls"></a>Dạng xem và kiểm soát tùy chỉnh không dùng nữa
Các dạng xem và kiểm soát tùy chỉnh sau đây cũng như các thành phần giả liên quan của chúng đã bị ngừng cung cấp.

- Dạng xem khả năng tính phí.
- Kiểm soát lưới tùy chỉnh để hiển thị chi tiết dòng báo giá trên trang **Thông tin dự án** cho dòng báo giá.
- Kiểm soát lưới tùy chỉnh để hiển thị chi tiết dòng hợp đồng dự án trên trang **Thông tin dự án** cho dòng đơn đặt hàng bán hàng.

> [!NOTE]
> Để biết danh sách đầy đủ các tài nguyên không dùng nữa, hãy xem [Tài nguyên web không dùng nữa trong Project Service Automation v3.x](../developer-guides/web-resources-deprecated-v3.x.md)

## <a name="unified-client-interface-app-module"></a>Mô-đun ứng dụng giao diện khách hợp nhất
Với việc giới thiệu mô-đun ứng dụng giao diện khách hợp nhất (UCI), các mục sơ đồ trang web PSA đã bị xoá khỏi hệ thống.  
Chức năng liên quan đến hình thức chuyển đổi cơ hội, báo, đơn đặt hàng, hóa đơn đã được không được chấp nhận vì nó không còn cần thiết vì UCI App mô-đun chỉ bao gồm PSA Phiên bản của biểu mẫu.  

Các tài nguyên web sau đã bị ngừng hoạt động:

- msdyn_\SalesDocument\SalesDocumentFormLoader.js
- msdyn_\SalesDocument\PSSalesDocumentCustomFormIds.js

> [!NOTE]
> Để biết danh sách đầy đủ các tài nguyên không dùng nữa, hãy xem [Tài nguyên web không dùng nữa trong Project Service Automation v3.x](../developer-guides/web-resources-deprecated-v3.x.md).




[!INCLUDE[footer-include](../../includes/footer-banner.md)]