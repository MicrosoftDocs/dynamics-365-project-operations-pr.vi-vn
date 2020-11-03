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
ms.openlocfilehash: 57d4b9aad433af6d3e73369c76f2793f349c6965
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087302"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a><span data-ttu-id="2905a-103">Thêm biểu mẫu thực thể tuỳ chỉnh mới (Project Service Automation 2.x)</span><span class="sxs-lookup"><span data-stu-id="2905a-103">Add new custom entity forms (Project Service Automation 2.x)</span></span>

## <a name="type-field"></a><span data-ttu-id="2905a-104">Trường loại</span><span class="sxs-lookup"><span data-stu-id="2905a-104">Type field</span></span> 

<span data-ttu-id="2905a-105">Dynamics 365 Project Service Automation phụ thuộc vào trường **Loại** ( **msdyn\_ordertype** ) của thực thể Cơ hội, Báo giá, Đơn đặt hàng và Hóa đơn để phân biệt các phiên bản **dựa trên công việc** của các thực thể này từ phiên bản **dựa trên mục** và **dựa trên dịch vụ**.</span><span class="sxs-lookup"><span data-stu-id="2905a-105">Dynamics 365 Project Service Automation relies on the **Type** ( **msdyn\_ordertype** ) field of the Opportunity, Quote, Order, and Invoice entities to distinguish **work-based** versions of these entities from **item-based** and **service-based** versions.</span></span> <span data-ttu-id="2905a-106">Các phiên bản dựa trên công việc của các thực thể này được xử lý bởi PSA.</span><span class="sxs-lookup"><span data-stu-id="2905a-106">Work-based versions of these entities are handled by PSA.</span></span> <span data-ttu-id="2905a-107">Rất nhiều logic kinh doanh phía máy khách và phía máy chủ của giải pháp phụ thuộc vào trường **Loại**.</span><span class="sxs-lookup"><span data-stu-id="2905a-107">Lots of business logic on the client side and server side of the solution depends on the **Type** field.</span></span> <span data-ttu-id="2905a-108">Do đó, điều quan trọng là trường được khởi tạo với một giá trị chính xác khi các thực thể được tạo.</span><span class="sxs-lookup"><span data-stu-id="2905a-108">Therefore, it's important that the field be initialized with a correct value when the entities are created.</span></span> <span data-ttu-id="2905a-109">Một giá trị không đúng có thể gây ra các hành vi không chính xác và một số logic kinh doanh có thể không chạy đúng.</span><span class="sxs-lookup"><span data-stu-id="2905a-109">An incorrect value can cause incorrect behaviors, and some business logic might not run correctly.</span></span>

## <a name="automatic-form-switching"></a><span data-ttu-id="2905a-110">Chuyển đổi biểu mẫu tự động</span><span class="sxs-lookup"><span data-stu-id="2905a-110">Automatic form switching</span></span>

<span data-ttu-id="2905a-111">Để tránh khả năng hỏng dữ liệu và hành vi ngoài dự kiến gây ra do khởi tạo và chỉnh sửa bản ghi thực thể kinh doanh, PSA hiện bao gồm logic để tự động chuyển đổi biểu mẫu trong các biểu mẫu sẵn dùng.</span><span class="sxs-lookup"><span data-stu-id="2905a-111">To avoid potential data corruption and unexpected behaviors that are caused by incorrect initialization and editing of the sales entity records, PSA now includes logic for automatic form switching in out-of-box forms.</span></span> <span data-ttu-id="2905a-112">Logic này đưa người dùng đến biểu mẫu chính xác để làm việc với phiên bản dựa trên công việc hoặc bất kỳ loại thực thể cơ hội, báo giá, đơn đặt hàng hoặc hóa đơn nào.</span><span class="sxs-lookup"><span data-stu-id="2905a-112">This logic takes users to the correct form for working with the work-based version or any other type of Opportunity, Quote, Order, or Invoice entity.</span></span> <span data-ttu-id="2905a-113">Khi người dùng mở phiên bản dựa trên công việc của một thực thể cơ hội, báo giá, đơn đặt hàng hoặc hóa đơn, biểu mẫu được chuyển sang **Thông tin dự án**.</span><span class="sxs-lookup"><span data-stu-id="2905a-113">When a user opens the work-based version of an Opportunity, Quote, Order, or Invoice entity, the form is switched to **Project Information**.</span></span>

<span data-ttu-id="2905a-114">Logic chuyển đổi biểu mẫu tự động dựa trên ánh xạ giữa giá trị **formId** và trường **msdyn\_ordertype**.</span><span class="sxs-lookup"><span data-stu-id="2905a-114">The automatic form switching logic relies on the mapping between the **formId** value and the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="2905a-115">Tất cả các biểu mẫu sẵn dùng đã được thêm vào ánh xạ đó.</span><span class="sxs-lookup"><span data-stu-id="2905a-115">All out-of-box forms have been added to that mapping.</span></span> <span data-ttu-id="2905a-116">Tuy nhiên, biểu mẫu tùy chỉnh phải được thêm vào theo cách thủ công để cho biết phiên bản của thực thể mà họ muốn xử lý.</span><span class="sxs-lookup"><span data-stu-id="2905a-116">However, custom forms must be manually added to indicate which version of the entity they are intended to handle.</span></span> <span data-ttu-id="2905a-117">Điều này dựa trên trường **msdyn\_ordertype**.</span><span class="sxs-lookup"><span data-stu-id="2905a-117">This is based on the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="2905a-118">Nếu ánh xạ bị thiếu chuyển đổi biểu mẫu, thì logic sẽ chuyển sang biểu mẫu sẵn dùng, dựa trên giá trị được lưu trong trường **msdyn\_ordertype** của thực thể.</span><span class="sxs-lookup"><span data-stu-id="2905a-118">If the form switching is missing from the mapping, logic will switch to the out-of-box form, based on the value that is saved in the **msdyn\_ordertype** field of the entity.</span></span>

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a><span data-ttu-id="2905a-119">Thêm biểu mẫu tùy chỉnh và bật logic chuyển đổi biểu mẫu</span><span class="sxs-lookup"><span data-stu-id="2905a-119">Add custom forms and turn on the form switching logic</span></span>

<span data-ttu-id="2905a-120">Ví dụ sau cho thấy cách thêm một biểu mẫu tùy chỉnh **Thông tin dự án của tôi** để nó làm việc với các cơ hội dựa trên công việc.</span><span class="sxs-lookup"><span data-stu-id="2905a-120">The following example shows how to add a custom form, **My Project Information** , so that it works with work-based opportunities.</span></span> <span data-ttu-id="2905a-121">Quá trình tương tự được sử dụng để thêm biểu mẫu tùy chỉnh để chúng hoạt động với báo giá, đơn đặt hàng và hóa đơn.</span><span class="sxs-lookup"><span data-stu-id="2905a-121">The same process is used to add custom forms so that they work with quotes, orders, and invoices.</span></span>

<span data-ttu-id="2905a-122">Hãy làm theo các bước sau để tạo phiên bản tùy chỉnh của biểu mẫu **Thông tin dự án**.</span><span class="sxs-lookup"><span data-stu-id="2905a-122">Follow these steps to create a custom version of the **Project Information** form.</span></span>

1. <span data-ttu-id="2905a-123">Trong thực thể Cơ hội, mở biểu mẫu **Thông tin dự án** và lưu bản sao bằng tên **Thông tin dự án của tôi**.</span><span class="sxs-lookup"><span data-stu-id="2905a-123">In the Opportunity entity, open the **Project Information** form, and save a copy under the name **My Project Information**.</span></span>
2. <span data-ttu-id="2905a-124">Mở biểu mẫu mới, sau đó, trong thuộc tính, đảm bảo có các tập lệnh khởi tạo biểu mẫu từ biểu mẫu **Thông tin dự án**.</span><span class="sxs-lookup"><span data-stu-id="2905a-124">Open the new form, and then, in the properties, make sure that the form initialization scripts from the **Project Information** form are present.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="2905a-125">Không loại bỏ các tập lệnh này.</span><span class="sxs-lookup"><span data-stu-id="2905a-125">Don't remove the scripts.</span></span> <span data-ttu-id="2905a-126">Ngoài ra, một số dữ liệu có thể được khởi tạo không đúng.</span><span class="sxs-lookup"><span data-stu-id="2905a-126">Otherwise, some data might be initialized incorrectly.</span></span>

3. <span data-ttu-id="2905a-127">Xác minh rằng trường **Loại** ( **msdyn\_ordertype** ) có trong biểu mẫu.</span><span class="sxs-lookup"><span data-stu-id="2905a-127">Verify that the **Type** ( **msdyn\_ordertype** ) field is present in the form.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="2905a-128">Không loại bỏ trường này.</span><span class="sxs-lookup"><span data-stu-id="2905a-128">Don't remove this field.</span></span> <span data-ttu-id="2905a-129">Nếu không, các tập lệnh khởi tạo sẽ bị lỗi.</span><span class="sxs-lookup"><span data-stu-id="2905a-129">Otherwise, the initialization scripts will fail.</span></span>

4. <span data-ttu-id="2905a-130">Tìm giá trị **formId** của biểu mẫu mới.</span><span class="sxs-lookup"><span data-stu-id="2905a-130">Find the **formId** value of the new form.</span></span> <span data-ttu-id="2905a-131">Bạn có thể hoàn thành bước này theo hai cách:</span><span class="sxs-lookup"><span data-stu-id="2905a-131">You can complete this step in two ways:</span></span>

    - <span data-ttu-id="2905a-132">Xuất biểu mẫu **Thông tin dự án của tôi** dưới dạng giải pháp không được quản lý, sau đó tra cứu giá trị **formId** trong tệp customization.xml của giải pháp xuất.</span><span class="sxs-lookup"><span data-stu-id="2905a-132">Export the **My Project Information** form as part of an unmanaged solution, and then look up the **formId** value in the customization.xml file of the exported solution.</span></span>
    - <span data-ttu-id="2905a-133">Mở biểu mẫu **Thông tin dự án của tôi** trong công cụ biên tập biểu mẫu, sau đó tìm mã định danh duy nhất (GUID) bên cạnh thông số **fromId** trong URL như hiển thị trong hình minh họa sau đây.</span><span class="sxs-lookup"><span data-stu-id="2905a-133">Open the **My Project Information** form in the form editor, and then look for the globally unique identifier (GUID) next to the **fromId** parameter in the URL, as shown in the following illustration.</span></span>

    ![Giá trị formId của biểu mẫu mới trong URL](media/how-to-add-custom-forms-in-v2.0.png)

5. <span data-ttu-id="2905a-135">Tạo một ánh xạ **msdyn\_ordertype** cho giá trị **formId** bằng cách chỉnh sửa tài nguyên web msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js.</span><span class="sxs-lookup"><span data-stu-id="2905a-135">Create an **msdyn\_ordertype** mapping for the **formId** value by editing the msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js web resource.</span></span> <span data-ttu-id="2905a-136">Loại bỏ mã khỏi nguồn, thay bằng mã sau đây.</span><span class="sxs-lookup"><span data-stu-id="2905a-136">Remove the code from the resource, and replace it with the following code.</span></span>

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

6. <span data-ttu-id="2905a-137">Lưu và xuất bản các mục tùy chỉnh.</span><span class="sxs-lookup"><span data-stu-id="2905a-137">Save and then publish the customizations.</span></span>
