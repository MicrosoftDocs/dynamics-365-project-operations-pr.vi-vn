---
title: Thông tin mới trong tháng 6 năm 2022 - Triển khai Project Operations bản đơn giản
description: Bài viết này cung cấp thông tin về các bản cập nhật chất lượng có trong lần triển khai bản đơn giản của Microsoft Dynamics 365 Project Operations phát hành vào tháng 6 năm 2022.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8313288ecf7ff1350cd82c62d3d0c291d8a3ded4
ms.sourcegitcommit: 7772d72a7c96a44ffb23369f8ffb436813449239
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/20/2022
ms.locfileid: "9031219"
---
# <a name="whats-new-june-2022---project-operations-lite-deployment"></a>Thông tin mới trong tháng 6 năm 2022 - Triển khai Project Operations bản đơn giản

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Bài viết này áp dụng cho các phiên bản và thành phần sau của Microsoft Dynamics 365 Project Operations:

- Project Operations trong môi trường Dataverse phiên bản 4.43.0.77 hoặc 4.43.0.119

## <a name="quality-updates"></a>Bản cập nhật chất lượng

| Lĩnh vực tính năng | Số tham chiếu | Cập nhật chất lượng |
| --- | --- | --- |
| Hợp đồng phụ | 2708885 | Đã sửa lỗi thông báo xuất hiện khi người dùng tạo bản ghi tiêu đề đặt trước nguồn lực có thể đặt trong đó không có nguồn có thể đặt nào được điền vào. |
| Hoạch định và theo dõi dự án | 2629441 | Đã sửa logic kích hoạt quy trình làm việc để giúp ngăn chặn vòng lặp vô hạn khi các nhiệm vụ dự án được cập nhật. |
| Thời gian và chi phí | 2641209 | Hoạt động nhập mục nhập thời gian từ phân công/đặt trước phải giữ lại một tham chiếu nguồn lực có thể đặt. |
| Hoạch định và theo dõi dự án | 2651148 | Tiêu đề tài liệu dự án phải được bảo vệ.|
| Hoạch định và theo dõi dự án | 2653145 | Đã thêm xác thực để đảm bảo rằng không thể tạo bản ghi dự án có các ký tự không hợp lệ trong tên. |
| Thời gian và chi phí | 2654710 | Đã sửa bộ lọc trên trang **Phê duyệt**. |
| Định giá và thanh toán | 2667805 | Đã thêm xác thực để giúp ngăn việc tạo doanh số đã lập hóa đơn thực tế nếu doanh số chưa lập hóa đơn thực tế phụ trợ không tồn tại. |
| Định giá và thanh toán | 2668378 | Đã thêm xác thực để giúp ngăn thứ nguyên giá tùy chỉnh được thêm vào trừ khi bạn điền vào tên logic và tên trường. |
| Thời gian và chi phí | 2700428 | Cải thiện logic phê duyệt để đảm bảo rằng các bộ phê duyệt khác cho dự án có thể được xử lý ngay cả khi một trong các bộ phê duyệt bị kẹt trong các công việc hệ thống. |
