---
title: Thông tin mới trong tháng 6 năm 2021 - Triển khai bản đơn giản Project Operations
description: Bài viết này cung cấp thông tin về các bản cập nhật chất lượng có sẵn trong bản triển khai Project Operations lite vào tháng 6 năm 2021.
author: sigitac
ms.date: 06/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 16fffb06ebb72ac25982374bff27a015eccfae1b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913968"
---
# <a name="whats-new-june-2021---project-operations-lite-deployment"></a>Thông tin mới trong tháng 6 năm 2021 - Triển khai bản đơn giản Project Operations

_Áp dụng cho: Bản triển khai giản đơn - từ thỏa thuận đến lập hóa đơn ước giá_

Bài viết này áp dụng cho những điều sau Dynamics 365 Project Operations các thành phần và phiên bản:

  - Project Operations trên môi trường Dataverse phiên bản 4.11.0.156 hoặc 4.11.0.164.

## <a name="quality-updates"></a>Bản cập nhật chất lượng

| **Lĩnh vực tính năng** | **Số tham chiếu** | **Cập nhật chất lượng** |
| --- | --- | --- |
| Định giá và thanh toán | 2281417 | Đã khắc phục sự cố liên quan đến việc không thực hiện được hành động tạo hóa đơn tự động thông qua lịch trình hóa đơn. |
| Định giá và thanh toán | 2287835 |   Đã cải thiện hiệu suất xác nhận hóa đơn. |
| Quản lý cơ hội | 2222555 | Khả năng tính phí ước tính vật liệu phải được sao chép chính xác để báo giá chi tiết dòng khi sử dụng **Nhập từ Ước tính dự án**. |
| Quản lý cơ hội | 2223427 | Các tùy chỉnh hiện được phép cho hành động, **GenerateRetainersFromRetainerScheduleOptions**. |
| Quản lý cơ hội | 2277528 | Tính toán giá trị mốc thanh toán cố định cho các mô tả hợp đồng dự án với nhiều khách hàng. |
| Hoạch định và theo dõi dự án | 2226110 | Đã khắc phục sự cố gián đoạn với hàm **Tạo yêu cầu** trong lưới **Nhóm dự án**. |
| Hoạch định và theo dõi dự án | 2208109 | Người dùng không thể tạo dự án bằng một đơn vị tiền tệ với các nhiệm vụ liên quan bằng đơn vị tiền tệ khác. |
| Hoạch định và theo dõi dự án | 2258228 | Danh sách các trường được phép sửa đổi với thực thể **Lập lịch trình** sử dụng API lịch trình đã được cập nhật. |
| Hoạch định và theo dõi dự án | 2293989 | Ngôn ngữ và cài đặt khu vực chính xác phải được chuyển sang lưới **Nhiệm vụ dự án**.|
| Quản lý nguồn lực | 2220493 | Đã sửa lỗi trải nghiệm người dùng trong lưới **Nhiệm vụ** khi nhanh chóng đánh dấu một yêu cầu nguồn lực là hoàn thành. |
| Quản lý nguồn lực | 2330496 | Đã sửa lỗi tải **Bảng lịch trình**. (Bản cập nhật chất lượng có sẵn trong phiên bản 4.11.0.164) |
| Thời gian và Chi phí | 2194431 | Lưới **Mục nhập thời gian** phải tuân thủ đầu tuần như đã thiết lập trong **Cài đặt hệ thống**. |
| Thời gian và Chi phí | 2277311 | Sau khi bạn xóa giá trị trong một ô trong lưới **Mục nhập thời gian**, con trỏ vẫn ở trong lưới. |