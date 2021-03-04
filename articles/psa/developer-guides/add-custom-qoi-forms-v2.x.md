---
title: Thêm biểu mẫu thực thể tuỳ chỉnh mới (Project Service Automation 2.x)
description: Chủ đề này cung cấp thông tin về cách thêm biểu mẫu thực thể tùy chỉnh cho cơ hội, báo giá, đơn đặt hàng hoặc hóa đơn trong Dynamics 365 Project Service Automation 2.x.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 31986efed81892cc5722cb8f5e292cde14d8843d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144619"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a>Thêm biểu mẫu thực thể tuỳ chỉnh mới (Project Service Automation 2.x)

[!include [banner](../../includes/psa-now-project-operations.md)]

## <a name="type-field"></a>Trường loại 

Dynamics 365 Project Service Automation phụ thuộc vào trường **Loại** (**msdyn\_ordertype**) của thực thể Cơ hội, Báo giá, Đơn đặt hàng và Hóa đơn để phân biệt các phiên bản **dựa trên công việc** của các thực thể này từ phiên bản **dựa trên mục** và **dựa trên dịch vụ**. Các phiên bản dựa trên công việc của các thực thể này được xử lý bởi PSA. Rất nhiều logic kinh doanh phía máy khách và phía máy chủ của giải pháp phụ thuộc vào trường **Loại**. Do đó, điều quan trọng là trường được khởi tạo với một giá trị chính xác khi các thực thể được tạo. Một giá trị không đúng có thể gây ra các hành vi không chính xác và một số logic kinh doanh có thể không chạy đúng.

## <a name="automatic-form-switching"></a>Chuyển đổi biểu mẫu tự động

Để tránh khả năng hỏng dữ liệu và hành vi ngoài dự kiến gây ra do khởi tạo và chỉnh sửa bản ghi thực thể kinh doanh, PSA hiện bao gồm logic để tự động chuyển đổi biểu mẫu trong các biểu mẫu sẵn dùng. Logic này đưa người dùng đến biểu mẫu chính xác để làm việc với phiên bản dựa trên công việc hoặc bất kỳ loại thực thể cơ hội, báo giá, đơn đặt hàng hoặc hóa đơn nào. Khi người dùng mở phiên bản dựa trên công việc của một thực thể cơ hội, báo giá, đơn đặt hàng hoặc hóa đơn, biểu mẫu được chuyển sang **Thông tin dự án**.

Logic chuyển đổi biểu mẫu tự động dựa trên ánh xạ giữa giá trị **formId** và trường **msdyn\_ordertype**. Tất cả các biểu mẫu sẵn dùng đã được thêm vào ánh xạ đó. Tuy nhiên, biểu mẫu tùy chỉnh phải được thêm vào theo cách thủ công để cho biết phiên bản của thực thể mà họ muốn xử lý. Điều này dựa trên trường **msdyn\_ordertype**. Nếu ánh xạ bị thiếu chuyển đổi biểu mẫu, thì logic sẽ chuyển sang biểu mẫu sẵn dùng, dựa trên giá trị được lưu trong trường **msdyn\_ordertype** của thực thể.

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a>Thêm biểu mẫu tùy chỉnh và bật logic chuyển đổi biểu mẫu

Ví dụ sau cho thấy cách thêm một biểu mẫu tùy chỉnh **Thông tin dự án của tôi** để nó làm việc với các cơ hội dựa trên công việc. Quá trình tương tự được sử dụng để thêm biểu mẫu tùy chỉnh để chúng hoạt động với báo giá, đơn đặt hàng và hóa đơn.

Hãy làm theo các bước sau để tạo phiên bản tùy chỉnh của biểu mẫu **Thông tin dự án**.

1. Trong thực thể Cơ hội, mở biểu mẫu **Thông tin dự án** và lưu bản sao bằng tên **Thông tin dự án của tôi**.
2. Mở biểu mẫu mới, sau đó, trong thuộc tính, đảm bảo có các tập lệnh khởi tạo biểu mẫu từ biểu mẫu **Thông tin dự án**. 

    > [!IMPORTANT]
    > Không loại bỏ các tập lệnh này. Ngoài ra, một số dữ liệu có thể được khởi tạo không đúng.

3. Xác minh rằng trường **Loại** (**msdyn\_ordertype**) có trong biểu mẫu. 

    > [!IMPORTANT]
    > Không loại bỏ trường này. Nếu không, các tập lệnh khởi tạo sẽ bị lỗi.

4. Tìm giá trị **formId** của biểu mẫu mới. Bạn có thể hoàn thành bước này theo hai cách:

    - Xuất biểu mẫu **Thông tin dự án của tôi** dưới dạng giải pháp không được quản lý, sau đó tra cứu giá trị **formId** trong tệp customization.xml của giải pháp xuất.
    - Mở biểu mẫu **Thông tin dự án của tôi** trong công cụ biên tập biểu mẫu, sau đó tìm mã định danh duy nhất (GUID) bên cạnh thông số **fromId** trong URL như hiển thị trong hình minh họa sau đây.

    ![Giá trị formId của biểu mẫu mới trong URL](media/how-to-add-custom-forms-in-v2.0.png)

5. Tạo một ánh xạ **msdyn\_ordertype** cho giá trị **formId** bằng cách chỉnh sửa tài nguyên web msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js. Loại bỏ mã khỏi nguồn, thay bằng mã sau đây.

    ```javascript
    define(["require", "exports"], function (require, exports) {
        "use strict";
        var SalesDocumentCustomFormIds = (function () {
            function SalesDocumentCustomFormIds() {
            }
            SalesDocumentCustomFormIds.overwriteFormIds = function (mappedFormIds) {
                /*
                ---- Notes ----
                mappedFormIds[SalesEntity][OrderType] => The array of forms IDs that support particular entity and order type
                Add or overwrite customized formId for the particular entity and order type by calling:
                    mappedFormIds[<EntityType>][<msdyn_ordertype>].push("<formId>");
                Allowed msdyn_ordertype values for reference:
                    ServiceBased: 690970002 (Field Service version of the entity)
                    WorkBased: 192350001 (PSA version of the entity)
                    ItemBased: 192350000 (Regular out of the box entity)
                Uncomment and update one of the following lines to register custom PSA form for required entity:
                */      
                //mappedFormIds[1][192350001].push("<formId>"); //Quote
                //mappedFormIds[5][192350001].push("<formId>"); //Quote Line
                //mappedFormIds[2][192350001].push("<formId>"); //Sales Order
                //mappedFormIds[6][192350001].push("<formId>"); //Sales Order Line
                // In this example we have added new form for Opportunity
                mappedFormIds[0][192350001].push("192EE537-DCC4-45D3-B7AF-EA694B9113D2"); //Opportunity
                //mappedFormIds[4][192350001].push("<formId>"); //Opportunity Line
            };
            return SalesDocumentCustomFormIds;
        }());
        exports.default = SalesDocumentCustomFormIds;
    });
    ```

6. Lưu và xuất bản các mục tùy chỉnh.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]