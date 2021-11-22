---
title: Tính năng mới trong tháng 8 năm 2021 - Triển khai bản đơn giản Project Operations
description: Chủ đề này cung cấp thông tin về các bản cập nhật chất lượng có trong bản phát hành tháng 8 năm 2021 của triển khai bản đơn giản Project Operations.
author: sigitac
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e1e0842edaa6153a4780bc799d8df3b6ebb12bba
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323532"
---
# <a name="whats-new-august-2021---project-operations-lite-deployment"></a>Tính năng mới trong tháng 8 năm 2021 - Triển khai bản đơn giản Project Operations

_Áp dụng cho: Bản triển khai giản đơn - từ thỏa thuận đến lập hóa đơn ước giá_

Chủ đề này áp dụng cho các phiên bản và thành phần sau của Dynamics 365 Project Operations:

  - Project Operations trên môi trường Dataverse phiên bản 4.13.0.152

## <a name="features-included-in-this-release"></a>Các tính năng có trong bản phát hành này

Sau đây là các tính năng có trong bản phát hành này:

- **Bộ phê duyệt**: Các bộ phê duyệt nhóm các yêu cầu phê duyệt thời gian, chi phí hoặc mức sử dụng vật liệu lại với nhau thành các tập hợp con thao tác nhỏ hơn. Việc nhóm này cho phép xử lý các phê duyệt theo yêu cầu cụ thể của dự án, đồng thời cho phép thử lại và sắp xếp theo trình tự. Việc nhóm các yêu cầu giúp cải thiện độ tin cậy và khả năng truy xuất nguồn gốc của việc xử lý phê duyệt đối với khối lượng phê duyệt lớn. Để biết thêm thông tin, hãy xem phần [Bộ phê duyệt](../../approvals/approval-sets.md).

## <a name="quality-updates"></a>Bản cập nhật chất lượng

### <a name="project-operations-on-dataverse"></a>Project Operations trên Dataverse

| **Lĩnh vực tính năng** | **Số tham chiếu** | **Cập nhật chất lượng** |
| --- | --- | --- |
| Định giá và thanh toán | 2295625 | Tên cột mốc phải được sao chép từ lịch hóa đơn sang chi tiết dòng hóa đơn. |
| Định giá và thanh toán | 2316323 | Không thể chỉnh sửa chiết khấu trên hóa đơn chiếu lệ trong Project Operations cho các tình huống dựa trên nguồn lực. |
|   Quản lý cơ hội | 2338619 | Chỉ được gọi các quy tắc kinh doanh **Cơ hội** và **Báo giá** trên các trang. |
| Quản lý nguồn lực | 2316523 | Việc sử dụng **Gửi yêu cầu** từ một yêu cầu nguồn lực có một vai trò được đính kèm sẽ không hiển thị lỗi. |
| Quản lý nguồn lực | 2326885 | Việc tạo yêu cầu nguồn lực thông qua một dự án sẽ không hiển thị lỗi. |
| Thời gian và chi phí | 2335584 | Dòng tác vụ không dùng nữa trong mục nhập thời gian. |
| Thời gian và chi phí | 2336884 | Nút nhập thời gian **Sao chép tuần** phải hoạt động không chỉ cho người dùng hiện tại. |