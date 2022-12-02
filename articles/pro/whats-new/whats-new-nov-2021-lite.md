---
title: Tính năng mới kể từ tháng 11 năm 2021 – triển khai bản đơn giản Project Operations
description: Bài viết này cung cấp thông tin về các bản cập nhật chất lượng có trong bản phát hành triển khai bản đơn giản Project Operations vào tháng 11 năm 2021.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 947e7f6183ddeef3ab9a88d140331956bbcf23bd
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913830"
---
# <a name="whats-new-november-2021---project-operations-lite-deployment"></a>Tính năng mới kể từ tháng 11 năm 2021 – triển khai bản đơn giản Project Operations

_Áp dụng cho: Bản triển khai giản đơn - từ thỏa thuận đến lập hóa đơn ước giá_

Bài viết này áp dụng cho các phiên bản và thành phần sau của Microsoft Dynamics 365 Project Operations:

- Project Operations trong môi trường Dataverse phiên bản 4.26.0.145, 4.26.0.148, 4.26.0.150, 4.26.0.155
  
## <a name="features-included-in-this-release"></a>Các tính năng có trong bản phát hành này

Sau đây là các tính năng có trong bản phát hành này:

- Các giao diện lập trình ứng dụng (API) Lập lịch dự án hiện hỗ trợ khả năng tạo và xóa các Bộ chứa dự án

## <a name="quality-updates"></a>Bản cập nhật chất lượng

### <a name="project-operations-in-dataverse"></a>Project Operations trong Dataverse

| Lĩnh vực tính năng | Số tham chiếu | Cập nhật chất lượng |
| --- | --- | --- |
| Định giá và thanh toán | 2358236 | Chỉnh sửa hóa đơn phải cho phép các chỉnh sửa có đường giá bằng không. |
| Quản lý nguồn lực | 2410072 | Cho phép thiết lập nguồn lực được phân công vào nhiệm vụ với tư cách người quản lý dự án. |
| Định giá và thanh toán | 2430234 | Khắc phục sự cố tính toán hiệu suất chi phí. |
| Thời gian và Chi phí | 2436978 | Cho phép nhập thời gian ở định dạng hh:mm. |
| Định giá và thanh toán | 2448623 | Cho phép cập nhật bảng giá sau khi chúng được liên kết với đơn vị tổ chức. |
| Thời gian và Chi phí | 2460396 | Cho phép xóa mục nhập thời gian bằng cách xóa ô. |
| Định giá và thanh toán | 2467386 | Cho phép xóa một dự án có nhiệm vụ, ngay cả khi nhiệm vụ được liên kết với một báo giá đã giành được. |
| Thời gian và Chi phí | 2461744 | Dạng xem **Phê duyệt không thành công của tôi** chỉ chứa các phê duyệt dự án ở giai đoạn **Đã gửi**. |
| Thời gian và Chi phí | 2464082 | Xóa liên kết từ phê duyệt dự án đến bộ phê duyệt khi trạng thái mục tiêu được so khớp. |
| Thời gian và Chi phí | 2468108 | Công việc Lập lịch không được đặt trạng thái **Xử lý** cho bộ phê duyệt. |
| Thời gian và Chi phí | 2471503 | Xóa bộ phê duyệt tồn tại được 7 ngày. |
| Định giá và thanh toán | 2480687 | Không được xóa tham chiếu mô tả báo giá khi mốc mô tả báo giá được tạo. |
