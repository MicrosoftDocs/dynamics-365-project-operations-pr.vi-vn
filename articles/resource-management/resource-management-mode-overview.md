---
title: Tổng quan về chế độ quản lý nguồn lực
description: Chủ đề này cung cấp thông tin về chức năng Quản lý nguồn lực trong Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4a8e605109e48b50da68abeee989f8ac8d3d659c
ms.sourcegitcommit: cf79185c8c84c55fbae55f9cfc1b17840e072b49
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930117"
---
# <a name="resource-management-modes-overview"></a>Tổng quan về chế độ quản lý nguồn lực

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_


Dynamics 365 Project Operations hỗ trợ hai chế độ để bạn thực hiện quy trình đặt trước tổng thể. Chế độ quản lý được xác định như một tham số dự án và có thể được sửa đổi nếu nhu cầu kinh doanh của bạn thay đổi.    

## <a name="central-mode"></a>Chế độ trung tâm
Đối với các tổ chức tập trung phân bổ nguồn lực cho các dự án, Chế độ trung tâm cung cấp cách thức để đảm bảo Người quản lý dự án có thể xác định các yêu cầu về nguồn lực ở cấp độ dự án. Việc thực hiện các yêu cầu về nguồn lực được giao cho Người quản lý nguồn lực. Người quản lý dự án có thể chấp nhận hoặc từ chối các nguồn lực do Người quản lý nguồn lực đề xuất.

![Chế độ trung tâm](./media/resource-management-central.png)

Để quản lý nguồn lực bằng Chế độ trung tâm, hãy xem:

- [Chỉ định nguồn lực chung có thể đăng ký trước cho nhiệm vụ và tạo yêu cầu về nguồn lực](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [Đặt trước nguồn lực được nêu tên từ yêu cầu nguồn lực](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [Gửi đề nghị nguồn lực](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [Thực hiện yêu cầu nguồn lực](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [Chấp nhận hoặc từ chối nguồn lực được đề xuất từ yêu cầu nguồn lực](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>Chế độ kết hợp
Đối với các tổ chức yêu cầu sự linh hoạt trong việc phân bổ nguồn lực, chế độ kết hợp cho phép cả Người quản lý dự án và Người quản lý nguồn lực có khả năng đặt trước nguồn lực.

![Chế độ kết hợp](./media/resource-management-hybrid.png)

Ngoài quy trình ở Chế độ trung tâm được hỗ trợ, hãy xem các chủ đề sau để quản lý tất cả các quy trình đặt trước được hỗ trợ khác trong Chế độ kết hợp:

Đặt trước nguồn lực trực tiếp cho dự án:
- [Đặt trước nguồn lực có thể đặt lịch có tên cho nhóm dự án và chỉ định nhiệm vụ](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

Đặt trước nguồn lực từ yêu cầu nguồn lực:
- [Chỉ định nguồn lực chung có thể đăng ký trước cho nhiệm vụ và tạo yêu cầu về nguồn lực](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [Đặt trước nguồn lực được nêu tên từ yêu cầu nguồn lực](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
