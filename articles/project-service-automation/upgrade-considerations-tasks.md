---
title: Nâng cấp thông tin cân nhắc cho cấu trúc phân tích công việc
description: Chủ đề này cung cấp thông tin về cách nâng cấp cấu trúc phân tích công việc từ Project Service Automation 2.x lên 3.x.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 2.x
author: ruhercul
ms.assetid: 9e43d5b5-ca5d-41f5-9012-c48f8e3080f9
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 9aa35dd8784bfa55737b0836e653afd0442b80c2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 03/24/2020
ms.locfileid: "3757092"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a>Nâng cấp thông tin cân nhắc cho cấu trúc phân tích công việc
Chủ đề này cung cấp thông tin về cách nâng cấp cấu trúc phân tích công việc từ Project Service Automation 2.x lên 3.x. Chủ đề này xác định trạng thái ổn định của một dự án trong Project Service Automation (PSA) được yêu cầu để nâng cấp thành công. Cũng có thông tin về các điều kiện chặn phổ biến sẽ khiến không nâng cấp được. Để biết thêm thông tin về cách xác định nhiệm vụ dự án và các chức năng trong lịch trình dự án, hãy xem [Lịch biểu dự án](project-creating.md).

## <a name="key-entities"></a>Các thực thể chính
Đối với một cấu trúc phân tích công việc chính xác đã được tải với các nguồn lực, cần có các thực thể sau:

- [Dự án](../developer/entities/msdyn_project.md)
- [Nhóm Dự án](../developer/entities/msdyn_projectteam.md)
- [Nhiệm vụ Dự án](../developer/entities/msdyn_projecttask.md)
- [Gán Nguồn lực](../developer/entities/msdyn_resourceassignment.md)
- [Quan hệ phụ thuộc Nhiệm vụ Dự án](../developer/entities/msdyn_projecttaskdependency.md)
- [Nguồn lực có thể đặt trước](../developer/entities/bookableresource.md)

Để xác định cấu trúc phân tích công việc tải nguồn lực, bạn phải hoàn thành các bước sau:

1. Tạo dự án mới. Để biết thêm thông tin về cách tạo dự án mới, hãy xem [msdyn_project](../developer/entities/msdyn_project.md).
2. Tạo một hoặc nhiều nhiệm vụ. Để biết thêm thông tin về cách tạo nhiệm vụ, hãy xem [msdyn_projecttask](../developer/entities/msdyn_projecttask.md).
3. Xác định các yếu tố phụ thuộc nhiệm vụ. Để biết thêm thông tin, hãy xem [Quan hệ phụ thuộc nhiệm vụ dự án](../developer/entities/msdyn_projecttaskdependency.md).
4. Chỉ định thành viên nhóm dự án vào dự án. Để biết thêm thông tin, hãy xem [msdyn_projectteam](../developer/entities/msdyn_projectteam.md).
5. Chỉ định thành viên nhóm dự án vào nhiệm vụ. Để biết thêm thông tin, hãy xem [msdyn_resourceassignment](../developer/entities/msdyn_resourceassignment.md).

## <a name="project-team-relationships"></a>Mối quan hệ của nhóm dự án

Để đảm bảo nâng cấp thành công, phải duy trì chính xác các mối quan hệ sau:
- Tất cả thành viên nhóm dự án phải liên kết với một nguồn lực có thể đặt trước.
- Tất cả thành viên nhóm dự án phải liên kết với cùng một dự án. 

## <a name="project-task-relationships"></a>Mối quan hệ của nhiệm vụ dự án
Để đảm bảo nâng cấp thành công, phải duy trì chính xác các mối quan hệ sau:

- Mọi nhiệm vụ liên quan phải được liên kết với cùng một dự án.
- Mọi nhiệm vụ dòng phải có một nhiệm vụ chính.
- Mọi nhiệm vụ phải có một dự án chính.

### <a name="valid-conditions"></a>Điều kiện hợp lệ

- Tất cả các khoảng thời gian nhiệm vụ phải lớn hơn hoặc bằng (>=) một giờ và nhỏ hơn 1.800.000 phút (1.250 ngày).*
- Tất cả các nhiệm vụ phải có ngày bắt đầu không sớm hơn 2000/01/01.*
- Tất cả các nhiệm vụ phải có ngày bắt đầu không muộn hơn 17 năm kể từ ngày hiện tại.*
- Tất cả các nhiệm vụ phải có ngày bắt đầu sớm hơn hoặc bằng với ngày kết thúc.
- Tất cả các loại giao dịch về phân loại (Chi phí, tài liệu, thuế và thời gian) phải có giá trị **Đơn vị mặc định** và **Nhóm đơn vị**.
- Phải tránh các định dạng ngày có chữ cái.

### <a name="potential-mitigation-steps"></a>Các bước giảm nhẹ có thể áp dụng
- Sử dụng Tìm kiếm nâng cao để xác định các nhiệm vụ Dự án không chứa ID dự án.
- Sử dụng Tìm kiếm nâng cao để xác định các nhiệm vụ Dự án trong đó thời lượng dự kiến lớn hơn > 1.800.000.
- Trước khi thực hiện bất kỳ thay đổi dữ liệu nào, bạn nên điều tra mọi tùy chỉnh liên quan đến thực thể có thể dẫn đến việc đưa dữ liệu vào trạng thái xấu. Các tùy chỉnh này phải được xử lý trước khi tiến hành bất kỳ cập nhật nào liên quan đến dữ liệu.
- Đối với các nhiệm vụ đã xác định bị bỏ, hãy xem xét xóa các nhiệm vụ này nếu chúng không cần thiết hoặc nếu chúng cần được liên kết với dự án mẹ chính xác.
- Đối với bất kỳ nhiệm vụ nào có thời lượng lớn hơn 1.250 ngày, hãy xem xét thêm nhiều nhiệm vụ để thể hiện tổng thời lượng, nếu khả thi.

> [!NOTE]
> Các mục được ghi chú với dấu hoa thị (\*) có giới hạn do thực tế là công cụ quản lý quan hệ khách hàng (CRM) chỉ hỗ trợ mở rộng 7.320 lần xuất hiện lại. Bạn phải ở dưới giới hạn này.

## <a name="resource-assignment-relationships"></a>Mối quan hệ Gán nguồn lực
Để đảm bảo nâng cấp thành công, phải duy trì chính xác các mối quan hệ sau:

- Tất cả Gán nguồn lực trong cấu trúc phân tích công việc phải liên quan đến cùng một dự án.
- Tất cả Gán nguồn lực trong cấu trúc phân tích công việc phải liên quan đến các thành viên nhóm dự án trong cùng một dự án.

### <a name="potential-mitigation-steps"></a>Các bước giảm nhẹ có thể áp dụng
- Xác định tất cả các nhiệm vụ nằm ngoài các điều kiện được mô tả ở trên.  
- Bất kỳ Gán nguồn lực nào không còn hiệu lực sẽ bị xóa.

## <a name="project-task-dependency-relationships"></a>Mối quan hệ phụ thuộc của nhiệm vụ dự án
Để đảm bảo nâng cấp thành công, phải duy trì chính xác các mối quan hệ sau:

- Tất cả yếu tố phụ thuộc nhiệm vụ dự án phải liên quan đến cùng một dự án.
- Trong một nhiệm vụ, không được tham chiếu cùng một yếu tố phụ thuộc nhiều hơn một lần.
