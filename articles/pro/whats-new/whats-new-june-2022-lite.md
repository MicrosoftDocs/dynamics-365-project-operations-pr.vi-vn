---
title: Có gì mới vào tháng 6 năm 2022 - Triển khai Project Operations Lite
description: Bài viết này cung cấp thông tin về các bản cập nhật chất lượng có sẵn trong bản phát hành tháng 6 năm 2022 của Microsoft Dynamics 365 Project Operations triển khai lite.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 2d773603abef7ab45d4d1c298e5553e57893294d
ms.sourcegitcommit: 51745acac29dfacba43a4003d86baff4d6ca2fb8
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/14/2022
ms.locfileid: "8959715"
---
# <a name="whats-new-june-2022---project-operations-lite-deployment"></a>Có gì mới vào tháng 6 năm 2022 - Triển khai Project Operations Lite

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Bài viết này áp dụng cho các thành phần và phiên bản sau của Microsoft Dynamics 365 Project Operations:

- Hoạt động dự án trong một Dataverse phiên bản môi trường 4.43.0.77

## <a name="quality-updates"></a>Bản cập nhật chất lượng

| Lĩnh vực tính năng | Số tham chiếu | Cập nhật chất lượng |
| --- | --- | --- |
| Thầu phụ | 2708885 | Đã sửa lỗi thông báo xuất hiện khi người dùng tạo bản ghi tiêu đề đặt trước tài nguyên có thể đặt chỗ trong đó không có tài nguyên có thể đặt được nào được điền vào. |
| Hoạch định và theo dõi dự án | 2629441 | Đã sửa lỗi logic kích hoạt quy trình làm việc để giúp ngăn chặn vòng lặp vô hạn khi các nhiệm vụ dự án được cập nhật. |
| Thời gian và chi phí | 2641209 | Mục nhập thời gian nhập từ nhiệm vụ / đặt chỗ phải giữ lại một tài nguyên tham khảo có thể đặt trước. |
| Hoạch định và theo dõi dự án | 2651148 | Tiêu đề tài liệu dự án phải được bảo vệ.|
| Hoạch định và theo dõi dự án | 2653145 | Đã thêm xác thực để đảm bảo rằng không thể tạo bản ghi dự án có các ký tự không hợp lệ trong tên của nó. |
| Thời gian và chi phí | 2654710 | Đã sửa bộ lọc trên **Phê duyệt** trang. |
| Định giá và thanh toán | 2667805 | Đã thêm xác thực để giúp ngăn chặn việc tạo các thực tế bán hàng đã lập hóa đơn nếu các thực tế bán hàng chưa lập hóa đơn hỗ trợ không tồn tại. |
| Định giá và thanh toán | 2668378 | Đã thêm xác thực để giúp ngăn thứ nguyên đặt giá tùy chỉnh được thêm vào trừ khi điền tên lôgic và tên trường. |
| Thời gian và chi phí | 2700428 | Cải thiện logic phê duyệt để đảm bảo rằng các bộ phê duyệt khác cho dự án có thể được xử lý ngay cả khi một trong các bộ phê duyệt bị kẹt trong các công việc hệ thống. |
