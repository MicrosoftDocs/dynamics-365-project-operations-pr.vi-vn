---
title: Thay đổi quản lý nguồn lực (Project Service Automation 3.x)
description: Chủ đề này cung cấp thông tin về các thay đổi cho Khu vực quản lý nguồn lực.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
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
ms.openlocfilehash: 94f9adc67163254486387a1ce59d5d3e8e93c335
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148669"
---
# <a name="resource-management-changes-project-service-automation-3x"></a>Thay đổi quản lý nguồn lực (Project Service Automation 3.x)

[!include [banner](../../includes/psa-now-project-operations.md)]

Các phần của chủ đề này cung cấp thông tin về những thay đổi đã được thực hiện cho Khu vực quản lý nguồn lực của phiên bản Dynamics 365 Project Service Automation 3.x.

## <a name="project-estimates"></a>Ước tính dự án

Thay vì dựa trên thực thể **msdyn\_projecttask** (**Nhiệm vụ dự án**), ước tính dự án dựa trên thực thể **msdyn\_resourceassignment** (**Phân công nguồn lực**). Phân công nguồn lực đã trở thành "nguồn tin cậy" cho định giá và lập lịch nhiệm vụ.

## <a name="line-tasks"></a>Nhiệm vụ mô tả

Trong PSA 3.x, nhiệm vụ mô tả đã lỗi thời (không dùng nữa). Phân công hiện hướng đến toàn bộ nhiệm vụ thay vì nhiệm vụ mô tả.

Các ví dụ sau hiển thị cách một nhiệm vụ được đặt tên "Nhiệm vụ kiểm tra" được gán cho thành viên nhóm A và B trong phiên bản cũ hơn của PSA và trong PSA 3.x.

- **Trước PSA 3.x:**

    - Nhiệm vụ kiểm tra

        - Nhiệm vụ kiểm tra – Nhiệm vụ mô tả 1

            - Phân công cho A

        - Nhiệm vụ kiểm tra – Nhiệm vụ mô tả 2

            - Phân công cho B

- **PSA 3.x:**

    - Nhiệm vụ kiểm tra

        - Phân công cho A
        - Phân công cho B

## <a name="unassigned-assignment"></a>Phân công chưa được chỉ định

Trong PSA 3.x, phân công chưa được chỉ định là phân công được chỉ định cho thành viên nhóm **NULL** và nguồn lực **NULL**. Phân công chưa được chỉ định có thể xảy ra trong một vài trường hợp:

- Nếu một nhiệm vụ đã được tạo nhưng chưa được phân công cho bất kỳ thành viên nhóm này, thì phân công chưa được chỉ định luôn được tạo. 
- Nếu tất cả người được chỉ định trên nhiệm vụ bị xóa, nhiệm vụ chưa được chỉ định được tạo lại cho nhiệm vụ đó.

## <a name="scheduling-fields-on-the-project-task-entity"></a>Lập lịch các trường trên thực thể Nhiệm vụ dự án

Các trường trên thực thể **msdyn\_projecttask** được chấp nhận hoặc chuyển đến thực thể **msdyn\_resourceassignment** hoặc chúng hiện được tham chiếu từ thực thể **msdyn\_projectteam** (**Thành viên nhóm dự án**).

| Trường không dùng nữa trên msdyn\_projecttask (Nhiệm vụ dự án) | Trường mới trên msdyn\_resourceassignment (Phân công nguồn lực) | Nhận xét |
|---|---|---|
| msdyn\_assignedresources | Không | |
| msdyn\_assignedteammembers | Không | |
| msdyn\_numberofresources | Không | |
| msdyn\_scheduledhours | Không | |
| msdyn\_effortcontour | msdyn\_plannedwork | Định dạng của cấu trúc dữ liệu Ký hiệu đối tượng JavaScript (JSON) được lưu trữ trong trường đã được thay đổi. |

## <a name="schedule-contour"></a>Đường cong lịch trình

Đường cong lịch trình được lưu trữ trong trường **Công việc theo kế hoạch** (**msdyn\_plannedwork**) của từng thực thể **Phân công nguồn lực** (**msdyn\_resourceassignment**).

### <a name="structure"></a>Cấu trúc

Cấu trúc mới của đường cong lịch trình bao gồm lát cắt thời gian linh hoạt được xác định cho từng ngày của lịch trình. Mỗi lát cắt thời gian có các thuộc tính sau:

- **Bắt đầu** – Bắt đầu giờ làm việc cho ngày, theo lịch dự án.
- **Kết thúc** – Kết thúc giờ làm việc cho ngày, theo lịch dự án.
- **Giờ** – Số giờ được chỉ định vào ngày này.

**Ví dụ**

Ví dụ này sử dụng lịch dự án mà ngày làm việc từ 9:00 sáng đến 5:00 chiều theo múi giờ UTC-8.

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a>Tự động lập lịch và lập lịch theo cách thủ công

Nếu một nhiệm vụ được lập lịch tự động, giờ được tải trước và khoảng thời gian nhiệm vụ có thể bị giảm.

**Ví dụ**

Nhiệm vụ sau đây được tự động lập lịch trong 18 giờ trong ba ngày (ngày 3 tháng 12 năm 2018 đến ngày 5 tháng 12 năm 2018).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

Nếu một nhiệm vụ được lập lịch theo cách thủ công, giờ được phân phối đều cho tất cả các ngày.

**Ví dụ**

Nhiệm vụ sau đây được lập lịch theo cách thủ công trong 18 giờ trong ba ngày (ngày 3 tháng 12 năm 2018 đến ngày 5 tháng 12 năm 2018).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a>Đơn vị phân công

Đơn vị phân công không còn dùng nữa trong PSA 3.x. Giờ nhân công nhiệm vụ hiện được chia đều, mỗi ngày, trong tất cả nguồn lực được phân công.

**Ví dụ**

Trong ví dụ này, nhiệm vụ được phân công cho 2 nguồn lực và được tự động lập lịch cho 36 giờ trong 3 ngày (ngày 3 tháng 12 năm 2018 đến ngày 5 tháng 12 năm 2018).

- Phân công 1:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- Phân công 2:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a>Tham số giá

Trong PSA 3.x, trường tham số giá dành riêng cho nguồn lực (chẳng hạn như **Vai trò** và **Đơn vị tổ chức**) bị xóa khỏi thực thể **msdyn\_projecttask**. Các trường này hiện có thể được lấy từ thành viên nhóm dự án tương ứng (**msdyn\_projectteam**) của phân công nguồn lực (**msdyn\_resourceassignment**) khi ước tính dự án được tạo. Một trường mới, **msdyn\_OrganizationalUnit**, đã được thêm vào thực thể **thể msdyn\_projectteam**.

| Trường không dùng nữa trên msdyn\_projecttask (Nhiệm vụ dự án) | Trường từ msdyn\_projectteam (Thành viên nhóm dự án) được sử dụng thay thế |
|---|---|
| msdyn\_resourcecategory | msdyn\_resourcecategory |
| msdyn\_organizationalunit | msdyn\_organizationalunit |

## <a name="contours"></a>Đường cong

Các trường đường cong ước tính và giá không còn được dùng trên thực thể **msdyn\_projecttask**. Họ đã được chuyển đến thực thể **msdyn\_resourceassignment**.

| Trường không dùng nữa trên msdyn\_projecttask (Nhiệm vụ dự án) | Trường mới trên msdyn\_resourceassignment (Phân công nguồn lực) |
|---|---|
| msdyn\_costestimatecontour | msdyn\_plannedcostcontour |
| msdyn\_salesestimatecontour | msdyn\_plannedsalescontour |

Các trường sau được thêm vào thực thể **msdyn\_resourceassignment**:

* msdyn\_plannedcost
* msdyn\_plannedsales

Các trường sau cho chi phí và doanh thu dự kiến, thực tế và còn lại không bị thay đổi trên thực thể **msdyn\_projecttask**:

* msdyn\_plannedcost
* msdyn\_plannedsales
* msdyn\_actualcost
* msdyn\_actualsales
* msdyn\_remainingcost
* msdyn\_remainingsales
