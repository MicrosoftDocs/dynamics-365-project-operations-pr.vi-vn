---
title: Các thay đổi về tính năng từ Project Service Automation sang Project Operations
description: Bài viết này cung cấp tổng quan về các thay đổi tính năng từ Tự động hóa dịch vụ dự án sang Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/03/2022
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: a9c69fc4296d30763f3994a4955e64ab258ceb4f
ms.sourcegitcommit: 675e9f3615e701c5f998de3a5ea3e25df11ae107
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 09/09/2022
ms.locfileid: "9459953"
---
# <a name="feature-changes-from-project-service-automation-to-project-operations"></a>Các thay đổi về tính năng từ Project Service Automation sang Project Operations

Việc nâng cấp từ Dynamics 365 Project Service Automation đến Dynamics 365 Project Operations Lite sẽ được phân phối trong ba giai đoạn. Bài viết này cung cấp thông tin về những thay đổi chính mà bạn có thể thấy khi nâng cấp hoàn tất.

| Nâng cấp giao hàng | Giai đoạn 1 <br>(Tháng 1 năm 2022) | Giai đoạn 2 <br>(Tháng 11 năm 2022) | Giai đoạn 3  |
|------------------|------------------------|---------------------------|---------------------------|
| Không phụ thuộc vào cấu trúc phân chia công việc (WBS) cho các dự án. | : heavy_check_mark: | : heavy_check_mark: | : heavy_check_mark: |
| WBS được bao gồm trong các giới hạn được hỗ trợ hiện tại của Hoạt động Dự án. | &nbsp; | : heavy_check_mark: | : heavy_check_mark: |
| WBS nằm ngoài giới hạn được hỗ trợ hiện tại của Hoạt động dự án, bao gồm hỗ trợ cho máy khách Project trên máy tính. | &nbsp; | &nbsp; | : heavy_check_mark: |

## <a name="project-management"></a>Quản lý dự án

Những thay đổi đáng kể nhất trong trải nghiệm người dùng sẽ nằm trong lĩnh vực lập kế hoạch dự án. Hoạt động dự án áp dụng trải nghiệm hiện đại mới để quản lý cấu trúc phân tích công việc (WBS) bằng cách tận dụng các khả năng lập lịch trình được cung cấp bởi [Dự án cho Web](https://support.microsoft.com/en-us/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5).

## <a name="differences-in-the-scheduling-experience"></a>Sự khác biệt trong trải nghiệm lập lịch trình

Bảng sau đây tóm tắt sự khác biệt về lịch trình giữa Tự động hóa dịch vụ dự án và Hoạt động dự án.

|  Lên lịch     |   Project Operations   |   PSA   |
|-----------------|------------------------|---------|
| Mẫu dự án - Khả năng xác định và áp dụng các mẫu dự án khi một dự án được tạo  |  &nbsp;    | : heavy_check_mark: |
| Tích hợp cấu trúc phân tích công việc dự án (WBS) với ứng dụng khách trên máy tính để bàn   |    &nbsp;  | : heavy_check_mark: |
| Ràng buộc - Bắt đầu không sớm hơn, kết thúc không muộn hơn  | : heavy_check_mark: |   &nbsp;  |
| Các mốc - Nhiệm vụ không có thời lượng   | : heavy_check_mark:  |  &nbsp;  |
| Các nhiệm vụ theo hướng tài nguyên sẽ tôn trọng tính khả dụng của các tài nguyên được giao   | : heavy_check_mark: |  &nbsp;    |
| Chỉnh sửa theo giai đoạn thời gian - Chỉnh sửa kế hoạch và làm việc hàng ngày   |   &nbsp;  | : heavy_check_mark: |
| Lập lịch tự động / thủ công - Sử dụng công cụ lập lịch Dự án để lên lịch tự động hoặc thủ công cho các tác vụ |  &nbsp; | : heavy_check_mark:  |
| Chỉnh sửa các dự án lớn trực tiếp trong giao diện người dùng: Không có giới hạn về kích thước của các kế hoạch có thể chỉnh sửa  | Giới hạn 500 nhiệm vụ  | : heavy_check_mark:       |
| Phần trăm hoàn thành - Đánh dấu tiến độ công việc   | : heavy_check_mark:  |  &nbsp;  |
| [Chế độ lịch trình dự án](../project-management/scheduling-modes.md) - Xác định dự án là các đơn vị cố định, nỗ lực cố định hoặc thời gian cố định | : heavy_check_mark: | &nbsp; |
| Dòng thời gian - Xây dựng và tùy chỉnh chế độ xem dòng thời gian để trực quan hóa chi tiết lịch trình và giao tiếp với các bên liên quan. | : heavy_check_mark:  | &nbsp; |
| Nhiệm vụ dựa trên nỗ lực - Công cụ lập lịch hỗ trợ để lập lịch cho một nhiệm vụ theo nỗ lực thúc đẩy  | : heavy_check_mark:  | &nbsp; |
| **Thông tin công việc** hộp thoại - Lưu chi tiết nhiệm vụ bằng hộp thoại | : heavy_check_mark:  |  &nbsp;  |
| Kéo và thả - Chọn nhiều nhiệm vụ và sửa đổi vị trí của chúng trên WBS | : heavy_check_mark: | &nbsp;  |
| Chế độ xem liên tục linh hoạt - Xác định chế độ xem chi tiết hơn của các thuộc tính nhiệm vụ   | : heavy_check_mark:  | &nbsp; |
| Sắp xếp và lọc WBS  | : heavy_check_mark:  | &nbsp; |
| Bảng xem để phân phối dự án không thác nước  | : heavy_check_mark:   | &nbsp; |
| Chế độ xem dòng thời gian - Biểu đồ Gantt tương tác được sử dụng để trực quan hóa và chỉnh sửa WBS   | : heavy_check_mark:  | &nbsp; |
| Phím tắt - Sử dụng phím tắt cho các thao tác phổ biến, chẳng hạn như thụt lề hoặc chèn  | : heavy_check_mark:  |  &nbsp; |
| Hoàn tác đa cấp - Thực hiện phân tích điều gì xảy ra để hiểu đầy đủ tác động của các thay đổi bằng cách đảo ngược và áp dụng lại toàn bộ tập hợp các thao tác | : heavy_check_mark: | &nbsp; |
| Cắt / Sao chép / Dán - Hợp tác phát triển theo lịch trình bằng cách sao chép và dán chi tiết lịch trình giữa các ứng dụng  | : heavy_check_mark: | &nbsp; |
| Danh sách kiểm tra công việc - Thêm tối đa 20 mục danh sách kiểm tra cho một công việc   | : heavy_check_mark: | &nbsp; |

## <a name="project-planning"></a>Lập kế hoạch dự án

Các **Dự án** trang trong Hoạt động dự án có một số khác biệt đáng kể so với **Dự án** trong Tự động hóa dịch vụ dự án.

Các hành động sau đã bị xóa khỏi **Dự án** trang như một phần của nâng cấp Giai đoạn 1:

  - **Mở trong MS Project**
  - **Tạo Mẫu**
  - **Hủy liên kết khỏi MS Project**

Các **Dự án** trong Hoạt động Dự án bao gồm các tab mới sau đây.

- **Ước tính vật liệu**
- **Thiết lập thanh toán theo tác vụ**

Các **Trạng thái** tab đã bị xóa và **Trạng thái** trường bây giờ là trên **Bản tóm tắt** tab với chế độ lập lịch của dự án.

   ![Cập nhật trang Dự án.](media/projectform.png)

Các **Lịch trình** tab đã được đổi tên thành **Nhiệm vụ** tab và giới thiệu trải nghiệm lập kế hoạch dự án mới với Project for the Web.

   ![Tab nhiệm vụ Dự án mới.](media/tasktab.png)

## <a name="scheduling-modes"></a>Chế độ lập lịch trình

Hoạt động Dự án đã giới thiệu một tính năng mới, [Lập lịch các chế độ](../project-management/scheduling-modes.md). Tất cả các dự án Tự động hóa dịch vụ dự án hiện có sẽ mặc định là **Thời lượng cố định** trong Hoạt động Dự án. Tuy nhiên, mặc định cho các dự án mới có thể được quản lý bằng cách vào **Cài đặt** > **Thông số** > **Tham số** > **Chế độ lên lịch**.

   ![Cài đặt tham số dự án cho chế độ Lịch biểu.](media/projectparameter.png)

## <a name="project-planning-limits"></a>Giới hạn lập kế hoạch dự án

Hoạt động Dự án dựa vào Dự án cho Web cho tất cả các hoạt động lập kế hoạch dự án. Project for the Web quản lý cấu trúc phân tích công việc bằng cách sử dụng các giới hạn trong bảng sau.

| **Trường**                                          | **Giới hạn**             |
|----------------------------------------------------|-----------------------|
| Tổng số nhiệm vụ tối đa cho một dự án                  | 500                   |
| Tổng khoảng thời gian tối đa cho một dự án               | 3650 ngày (10 năm)  |
| Tổng số tài nguyên tối đa cho một dự án              | 300                   |
| Tổng số liên kết tối đa (chỉ dành cho người kế nhiệm) cho một dự án | 600                   |
| Tổng số trường tùy chỉnh tối đa cho một dự án          | 10                    |
| Mức phân cấp tối đa                            | 10 cấp độ             |
| Liên kết tối đa (người kế nhiệm + người tiền nhiệm)            | 20                    |
| Thời lượng tối đa của nhiệm vụ lá                      | 1250 ngày             |
| Thời lượng tối đa của một nhiệm vụ tóm tắt                 | 3650 ngày (10 năm)  |
| Tài nguyên tối đa được chỉ định cho một nhiệm vụ               | 20 tài nguyên          |
| Phạm vi ngày được hỗ trợ cho một nhiệm vụ                    | 1/1/2000 - 12/31/2149 |
| Mục trong danh sách kiểm tra                                    | 20                    |

## <a name="project-planning-extensibility-and-development"></a>Khả năng mở rộng và phát triển lập kế hoạch dự án

Sau khi nâng cấp lên Hoạt động dự án, bạn phải sử dụng API lập lịch dự án để thực hiện các hoạt động tạo, cập nhật và xóa trên các thực thể sau:

|   Tên thực thể           |   Tên logic của thực thể       |
|-------------------------|-----------------------------|
| Dự án                 | msdyn_project               |
| Nhiệm vụ dự án            | msdyn_projecttask           |
| Quan hệ phụ thuộc Nhiệm vụ Dự án | msdyn_projecttaskdependency |
| Gán Nguồn lực     | msdyn_resourceassignment    |
| Bộ chứa Dự án          | msdyn_projectbucket         |
| Thành viên Nhóm Dự án     | msdyn_projectteam           |

Nếu bạn hiện có các tùy chỉnh liên quan đến các thực thể này, hãy xem [Sử dụng các API lịch trình Dự án để thực hiện các hoạt động với các thực thể Lập lịch biểu](../project-management/schedule-api-preview.md) để được hướng dẫn thực hiện.

## <a name="data-model-changes"></a>Thay đổi mô hình dữ liệu

Là một phần của Nâng cấp Giai đoạn 1, có những thay đổi đối với mô hình dữ liệu. Những thay đổi này chủ yếu là thay đổi trường đối với các thực thể hiện có. Trong Giai đoạn 1, các thực thể, **msydn_project** và **msdyn_projectteam** là sự tái cấu trúc các tùy chỉnh. 

> [!IMPORTANT]
> Phần này sẽ được cập nhật với các thực thể bổ sung khi các giai đoạn nâng cấp trong tương lai hoàn thành.

Các trường sau đã được thay thế bằng các trường mới.

|   Thực thể          |   Tên logic cũ   |   Tên logic mới    |
|-------------------|----------------------|-----------------------|
| msdyn_project     | msdyn_actualhours    | msdyn_effortcompleted |
| msdyn_project     | msdyn_plannedhours   | msdyn_effort          |
| msdyn_project     | msdyn_remaininghours | msdyn_effortremaining |
| msdyn_project     | msdyn_scheduledend   | msdyn_finish          |
| msdyn_project     | msdyn_wbsduration    | msdyn_duration        |
| msdyn_projectteam | msdyn_assignedhours  | msdyn_effort          |
| msdyn_projectteam | msdyn_from           | msdyn_start           |
| msdyn_projectteam | msdyn_to             | msdyn_finish          |

Các trường sau đây đã được thêm vào.

|   Thực thể          |   Tên lô-gic                               |   Description |
|-------------------|----------------------------------------------|---------------|
| msdyn_project     | msdyn_actualfeesales                         | Hiển thị tổng hợp doanh thu phí thực tế của dự án. Chỉ để sử dụng trong Tự động hóa dịch vụ dự án. |
| msdyn_project     | msdyn_actualmaterialcost                     | Thể hiện tổng hợp chi phí vật liệu thực tế của dự án. Chỉ để sử dụng trong Tự động hóa dịch vụ dự án. |
| msdyn_project     | msdyn_actualmaterialsales                    | Hiển thị tổng hợp doanh số bán vật liệu thực tế của dự án. Chỉ để sử dụng trong Tự động hóa dịch vụ dự án. |
| msdyn_project     | msdyn_businesscase                           |                |
| msdyn_project     | msdyn_contractlineproject                    | Dòng hợp đồng liên quan đến dự án này. |
| msdyn_project     | msdyn_copyprojectcorrelationid               | Đây là trường hệ thống nội bộ được sử dụng cho **Sao chép dự án** liên quan đến Mã định danh tương quan. Chỉ để sử dụng trong Tự động hóa dịch vụ dự án. |
| msdyn_project     | msdyn_copyprojectsessionid                   | Đây là trường hệ thống nội bộ, được sử dụng cho **Sao chép dự án** liên quan đến Mã định danh phiên. Chỉ để sử dụng trong Tự động hóa dịch vụ dự án. |
| msdyn_project     | msdyn_globalrevisiontoken                    | Đồng bộ lần cuối cùng Mã sửa đổi toàn cầu xRM từ dịch vụ lập lịch dự án. |
| msdyn_project     | msdyn_msprojectdocument                      | Tài liệu Microsoft Project thuộc về dự án. |
| msdyn_project     | msdyn_plannedmaterialcost                    | Tổng hợp chi phí vật liệu kế hoạch của dự án. Chỉ để sử dụng trong Tự động hóa dịch vụ dự án. |
| msdyn_project     | msdyn_plannedmaterialsales                   | Tổng hợp doanh thu bán vật tư theo kế hoạch của dự án. Chỉ để sử dụng trong Tự động hóa dịch vụ dự án. |
| msdyn_project     | msdyn_program                                | Chương trình mà dự án này có liên quan đến. |
| msdyn_project     | msdyn_quotelineproject                       | Dòng Trích dẫn liên quan đến dự án này. |
| msdyn_project     | msdyn_replaylogheader                        | Tiêu đề cho các bản ghi phát lại. |
| msdyn_project     | msdyn_schedulemode                           | Chế độ lập lịch mặc định được sử dụng cho tất cả các nhiệm vụ trong dự án.  |
| msdyn_project     | msdyn_taskearlieststart                      | Ngày bắt đầu sớm nhất của bất kỳ nhiệm vụ nào trong dự án.  |
| msdyn_project     | msdyn_valuestatement                         |                |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Thành viên nhóm dự án mà thành viên nhóm dự án này đã được sao chép từ đó. |
| msdyn_projectteam | msdyn_creategenericteammemberwithrequirement | Cho biết có tạo yêu cầu tài nguyên cho một thành viên nhóm chung mới được tạo hay không.  |
| msdyn_projectteam | msdyn_deletestatus                           | Trạng thái xóa của thành viên trong nhóm để theo dõi nếu có một yêu cầu xóa được gửi đến dịch vụ lập lịch Dự án và liệu nó có gửi phản hồi thành công trong khoảng thời gian dự kiến hay không. |
| msdyn_projectteam | msdyn_effortcompleted                        | Theo dõi nỗ lực hoàn thành của thành viên trong nhóm trong các nhiệm vụ của họ. |
| msdyn_projectteam | msdyn_effortremaining                        | Theo dõi nỗ lực chưa hoàn thành của thành viên trong nhóm về các bài tập của họ. |
| msdyn_projectteam | msdyn_markedfordeletiontimer                 | Khoảng thời gian chờ đợi từ khi thành viên trong nhóm gửi yêu cầu xóa tới dịch vụ lập lịch Dự án cho đến khi thành viên trong nhóm thực sự bị xóa vào Microsoft Dataverse.|
| msdyn_projectteam | msdyn_markedfordeletiontimestamp             | Dấu thời gian để ghi lại khi yêu cầu xóa thành viên trong nhóm được gửi đến dịch vụ lập lịch dự án. |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Hiển thị thành viên nhóm dự án mà thành viên nhóm dự án này đã được sao chép từ đó.  |

## <a name="project-templates"></a>Mẫu dự án

Hoạt động dự án không cung cấp hỗ trợ cho các mẫu dự án. Tuy nhiên, bạn có thể tái tạo nhiều chức năng cốt lõi với việc sử dụng [API sao chép dự án](../project-management/dev-copy-project.md).

## <a name="desktop-add-in-support"></a>Hỗ trợ bổ trợ cho máy tính để bàn

Hỗ trợ cho phần bổ trợ Microsoft Project Desktop sẽ không khả dụng trong 2 giai đoạn đầu tiên của quá trình nâng cấp. Trong Giai đoạn 3, những khách hàng có dự án lớn hơn giới hạn được hỗ trợ hiện tại của Dự án cho Web sẽ có thể sử dụng tiện ích bổ sung dành cho máy tính để bàn.

## <a name="editing-resource-assignment-contours"></a>Chỉnh sửa đường bao phân công tài nguyên

Khả năng chỉnh sửa đường bao phân bổ tài nguyên sẽ khả dụng khi có sẵn Giai đoạn 2 của nâng cấp.

## <a name="billing-and-pricing"></a>Định giá và thanh toán

Các tính năng mới sau đây đã được thêm vào Hoạt động Dự án. Các tính năng này có bản chất bổ sung và không ảnh hưởng đến mô hình dữ liệu Tự động hóa dịch vụ dự án.

- [Ghi lại việc sử dụng tài liệu cho các dự án và nhiệm vụ dự án](../material/material-usage-log.md)
- [Quản lý hợp đồng phụ](../pro/subcontracting/managing-subcontracts-overview.md)
- [Hợp đồng dựa trên tiền tạm ứng và giữ lại](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Hợp đồng không vượt quá trạng thái và xác nhận](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- [Thanh toán dựa trên công việc](../pro/sales/mapping-projects-tasks-quote-line-sales.md)

## <a name="deprecated-components"></a>Các thành phần không được dùng nữa

Các bảng sau ghi lại tất cả các trường không dùng nữa được chuyển đến bài nâng cấp giải pháp thành phần không dùng nữa. Để biết thêm thông tin và liên kết đến giải pháp, hãy xem [Dynamics 365 Project Service Automation 3x đến Hoạt động dự án 4x các thành phần không dùng nữa](https://github.com/microsoft/Dynamics365-Project-Operations-PowerApps/tree/main/3x-4x-deprecated-solution).

### <a name="invoicedetail"></a>Hóa đơn

| Các trường                                                    |
|-----------------------------------------------------------------------------------------------|
|Chemicaletail.msdyn_contractline    |

### <a name="msdyn_actual"></a>msdyn_actual

| Các trường                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_actual.msdyn_salescontractline                                                          |

### <a name="msdyn_characteristicreqforteammember"></a>msdyn_characteristicreqforteammember

| Các trường                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_characteristicreqforteammember.msdyn_characteristic                                     |
| msdyn_characteristicreqforteammember.msdyn_characteristicreqforteammemberid                   |
| msdyn_characteristicreqforteammember.msdyn_characteristictype                                 |
| msdyn_characteristicreqforteammember.msdyn_name                                               |
| msdyn_characteristicreqforteammember.msdyn_ratingvalue                                        |
| msdyn_characteristicreqforteammember.msdyn_resourcerequirementid                              |

### <a name="msdyn_contractlineinvoiceschedule"></a>msdyn_contractlineinvoiceschedule

| Các trường                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_contractlineinvoiceschedule.msdyn_contractline                                          |
| msdyn_contractlinescheduleofvalue.msdyn_contractline                                          |
 
### <a name="msdyn_dataexport"></a>msdyn_dataexport

| Các trường                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_dataexport.msdyn_dataexportid                                                           |
| msdyn_dataexport.msdyn_datatoken                                                              |
| msdyn_dataexport.msdyn_entityname                                                             |
| msdyn_dataexport.msdyn_exportedrecordcount                                                    |
| msdyn_dataexport.msdyn_exportstatus                                                           |
| msdyn_dataexport.msdyn_linkedentitydata                                                       |
| msdyn_dataexport.msdyn_name                                                                   |
| msdyn_dataexport.msdyn_pagingdata                                                             |

### <a name="msdyn_fact"></a>msdyn_fact

| Các trường                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_fact.msdyn_salescontractline                                                            |

### <a name="msdyn_findworkevent"></a>msdyn_findworkevent

| Các trường                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_findworkevent.msdyn_bookableresource                                                    |
| msdyn_findworkevent.msdyn_findworkeventid                                                     |
| msdyn_findworkevent.msdyn_name                                                                |
| msdyn_findworkevent.msdyn_timestamp                                                           |
| msdyn_findworkevent.msdyn_type                                                                |
| msdyn_findworkevent.msdyn_value                                                               |
| msdyn_findworkevent.msdyn_work                                                                |

### <a name="msdyn_invoicelinetransaction"></a>msdyn_invoicelinetransaction

| Các trường                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_invoicelinetransaction.msdyn_invoiceline                                                |
| msdyn_invoicelinetransaction.msdyn_salescontractline                                          |

### <a name="msdyn_journalline"></a>msdyn_journalline

| Các trường                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_journalline.msdyn_salescontractline                                                     |

### <a name="msdyn_opportunitylineresourcecategory"></a>msdyn_opportunitylineresourcecategory

| Các trường                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylineresourcecategory.msdyn_billingtype                                       |
| msdyn_opportunitylineresourcecategory.msdyn_description                                       |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylineresourcecategoryid                 |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylinetransactionclassification          |
| msdyn_opportunitylineresourcecategory.msdyn_resourcecategory                                  |

### <a name="msdyn_opportunitylinetransaction"></a>msdyn_opportunitylinetransaction

| Các trường                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransaction.msdyn_accountcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_accountingdate                                         |
| msdyn_opportunitylinetransaction.msdyn_accountvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_amount                                                 |
| msdyn_opportunitylinetransaction.msdyn_amount_base                                            |
| msdyn_opportunitylinetransaction.msdyn_amountmethod                                           |
| msdyn_opportunitylinetransaction.msdyn_basisamount                                            |
| msdyn_opportunitylinetransaction.msdyn_basisamount_base                                       |
| msdyn_opportunitylinetransaction.msdyn_basisprice                                             |
| msdyn_opportunitylinetransaction.msdyn_basisprice_base                                        |
| msdyn_opportunitylinetransaction.msdyn_basisquantity                                          |
| msdyn_opportunitylinetransaction.msdyn_billingtype                                            |
| msdyn_opportunitylinetransaction.msdyn_bookableresource                                       |
| msdyn_opportunitylinetransaction.msdyn_contactcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_contactvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_customertype                                           |
| msdyn_opportunitylinetransaction.msdyn_description                                            |
| msdyn_opportunitylinetransaction.msdyn_documentdate                                           |
| msdyn_opportunitylinetransaction.msdyn_enddatetime                                            |
| msdyn_opportunitylinetransaction.msdyn_exchangeratedate                                       |
| msdyn_opportunitylinetransaction.msdyn_opportunityline                                        |
| msdyn_opportunitylinetransaction.msdyn_opportunitylinetransactionid                           |
| msdyn_opportunitylinetransaction.msdyn_percent                                                |
| msdyn_opportunitylinetransaction.msdyn_price                                                  |
| msdyn_opportunitylinetransaction.msdyn_price_base                                             |
| msdyn_opportunitylinetransaction.msdyn_pricelist                                              |
| msdyn_opportunitylinetransaction.msdyn_product                                                |
| msdyn_opportunitylinetransaction.msdyn_project                                                |
| msdyn_opportunitylinetransaction.msdyn_quantity                                               |
| msdyn_opportunitylinetransaction.msdyn_resourcecategory                                       |
| msdyn_opportunitylinetransaction.msdyn_resourceorganizationalunitid                           |
| msdyn_opportunitylinetransaction.msdyn_startdatetime                                          |
| msdyn_opportunitylinetransaction.msdyn_task                                                   |
| msdyn_opportunitylinetransaction.msdyn_transactioncategory                                    |
| msdyn_opportunitylinetransaction.msdyn_transactionclassification                              |
| msdyn_opportunitylinetransaction.msdyn_transactiontypecode                                    |
| msdyn_opportunitylinetransaction.msdyn_unit                                                   |
| msdyn_opportunitylinetransaction.msdyn_unitschedule                                           |
| msdyn_opportunitylinetransaction.msdyn_vendortype                                             |

### <a name="msdyn_opportunitylinetransactioncategory"></a>msdyn_opportunitylinetransactioncategory

| Các trường                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactioncategory.msdyn_billingtype                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_description                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactioncategoryid           |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactionclassification       |
| msdyn_opportunitylinetransactioncategory.msdyn_transactioncategory                            |

### <a name="msdyn_opportunitylinetransactionclassificatio"></a>msdyn_opportunitylinetransactionclassificatio

| Các trường                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactionclassificatio.msdyn_billingtype                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_description                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_include                                   |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunityline                           |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunitylinetransactionclassificatioid |
| msdyn_opportunitylinetransactionclassificatio.msdyn_transactionclassification                 |

### <a name="msdyn_orderlineresourcecategory"></a>msdyn_orderlineresourcecategory

| Các trường                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlineresourcecategory.msdyn_contractline                                            |

### <a name="msdyn_orderlinetransaction"></a>msdyn_orderlinetransaction

| Các trường                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransaction.msdyn_salescontractline                                            |
| msdyn_orderlinetransactioncategory.msdyn_contractline                                         |

### <a name="msdyn_orderlinetransactionclassification"></a>msdyn_orderlinetransactionclassification

| Các trường                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransactionclassification.msdyn_contractline                                   |

### <a name="msdyn_project"></a>msdyn_project

| Các trường                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_project.msdyn_actualdurationminutes                                                     |
| msdyn_project.msdyn_actualhours                                                               |
| msdyn_project.msdyn_istemplate                                                                |
| msdyn_project.msdyn_plannedhours                                                              |
| msdyn_project.msdyn_projecttemplate                                                           |
| msdyn_project.msdyn_remaininghours                                                            |
| msdyn_project.msdyn_schediseddurationminutes                                                  |
| msdyn_project.msdyn_scheduledend                                                              |
| msdyn_project.msdyn_stagename                                                                 |
| msdyn_project.msdyn_wbsduration                                                               |


### <a name="msdyn_projecttask"></a>msdyn_projecttask

| Các trường                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttask.msdyn_actualdurationminutes                                                 |
| msdyn_projecttask.msdyn_actualeffort                                                          |
| msdyn_projecttask.msdyn_aggregationdirection                                                  |
| msdyn_projecttask.msdyn_assignedresources                                                     |
| msdyn_projecttask.msdyn_assignedteammembers                                                   |
| msdyn_projecttask.msdyn_autoscheduling                                                        |
| msdyn_projecttask.msdyn_costestimatecontour                                                   |
| msdyn_projecttask.msdyn_effortcontour                                                         |
| msdyn_projecttask.msdyn_islinetask                                                            |
| msdyn_projecttask.msdyn_numberofresources                                                     |
| msdyn_projecttask.msdyn_remaininghours                                                        |
| msdyn_projecttask.msdyn_resourceutilization                                                   |
| msdyn_projecttask.msdyn_salesestimatecontour                                                  |
| msdyn_projecttask.msdyn_schedonedhours                                                        |
| msdyn_projecttask.msdyn_wbsid                                                                 |

### <a name="msdyn_projecttaskstatususer"></a>msdyn_projecttaskstatususer

| Các trường                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttaskstatususer.msdyn_bookableresource                                            |
| msdyn_projecttaskstatususer.msdyn_description                                                 |
| msdyn_projecttaskstatususer.msdyn_empletecompletiondate                                      |
| msdyn_projecttaskstatususer.msdyn_empletehourstocomplete                                     |
| msdyn_projecttaskstatususer.msdyn_iscompleted                                                 |
| msdyn_projecttaskstatususer.msdyn_name                                                        |
| msdyn_projecttaskstatususer.msdyn_percentcomplete                                             |
| msdyn_projecttaskstatususer.msdyn_projecttaskid                                               |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatusindicator                                  |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatususerid                                     |

### <a name="msdyn_projectteam"></a>msdyn_projectteam

| Các trường                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteam.msdyn_applicantcount                                                        |
| msdyn_projectteam.msdyn_applicantsavailable                                                   |
| msdyn_projectteam.msdyn_assignedhours                                                         |
| msdyn_projectteam.msdyn_description                                                           |
| msdyn_projectteam.msdyn_from                                                                  |
| msdyn_projectteam.msdyn_hoursrequested                                                        |
| msdyn_projectteam.msdyn_membershipstatus                                                      |
| msdyn_projectteam.msdyn_number                                                                |
| msdyn_projectteam.msdyn_to                                                                    |

### <a name="msdyn_projectteammembersignup"></a>msdyn_projectteammembersignup

| Các trường                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteammembersignup.msdyn_bookableresource                                          |
| msdyn_projectteammembersignup.msdyn_membershipstatus                                          |
| msdyn_projectteammembersignup.msdyn_name                                                      |
| msdyn_projectteammembersignup.msdyn_projectteammembersignupid                                 |
| msdyn_projectteammembersignup.msdyn_teammembership                                            |

### <a name="msdyn_projecttransactioncategory"></a>msdyn_projecttransactioncategory

| Các trường                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttransactioncategory.msdyn_billingtype                                            |
| msdyn_projecttransactioncategory.msdyn_name                                                   |
| msdyn_projecttransactioncategory.msdyn_project                                                |
| msdyn_projecttransactioncategory.msdyn_projecttransactioncategoryid                           |
| msdyn_projecttransactioncategory.msdyn_transactioncategory                                    |

### <a name="msdyn_quotelineinvoiceschedule"></a>msdyn_quotelineinvoiceschedule

| Các trường                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_quotelineinvoiceschedule.msdyn_quoteline                                                |
| msdyn_quotelineresourcecategory.msdyn_quoteline                                               |
| msdyn_quotelinescheduleofvalue.msdyn_quoteline                                                |
| msdyn_quotelinetransaction.msdyn_quoteline                                                    |
| msdyn_quotelinetransactioncategory.msdyn_quoteline                                            |
| msdyn_quotelinetransactionclassification.msdyn_quoteline                                      |

### <a name="msdyn_resourceassignment"></a>msdyn_resourceassignment

| Các trường                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_resourceassignment.msdyn_hours                                                          |
| msdyn_resourceassignment.msdyn_fromdate                                                       |
| msdyn_resourceassignment.msdyn_msprojectclientid                                              |
| msdyn_resourceassignment.msdyn_todate                                                         |
| msdyn_resourceassignmentdetail.msdyn_duration                                                 |
| msdyn_resourceassignmentdetail.msdyn_from                                                     |
| msdyn_resourceassignmentdetail.msdyn_name                                                     |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentdetailid                               |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentid                                     |

### <a name="salesorderdetail"></a>đơn hàng bán hàng

| Các trường                                                    |
|-----------------------------------------------------------------------------------------------|
| salesorderdetail.msdyn_quoteline                                                              |

