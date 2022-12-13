---
title: Có gì mới Tháng 10 năm 2022 - Triển khai rút gọn Project Operations
description: Bài viết này cung cấp thông tin về các bản cập nhật chất lượng có sẵn trong bản phát hành tháng 10 năm 2022 của triển khai Microsoft Dynamics 365 Project Operations lite.
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: b6975e1f8645721fc03239b355b117eb664785f0
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806770"
---
# <a name="whats-new-october-2022---project-operations-lite-deployment"></a>Có gì mới Tháng 10 năm 2022 - Triển khai rút gọn Project Operations

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Bài viết này áp dụng cho các phiên bản và thành phần sau của Microsoft Dynamics 365 Project Operations:

- Project Operations trong môi trường Dataverse phiên bản 4.57.0.176

## <a name="features-included-in-this-release"></a>Các tính năng có trong bản phát hành này

| Lĩnh vực tính năng | Tên tính năng | Thông tin thêm |
| --- | --- | --- |
| Hoạch định và theo dõi dự án | **Project Operations Lập kế hoạch bên ngoài**<br>Chế độ lập lịch trình bên ngoài cho phép khách hàng tự tạo, cập nhật và xóa các thực thể có liên quan đến cấu trúc phân chia công việc (WBS) bằng cách sử dụng các API Dataverse gốc, không có giới hạn hiện tại do Project for the Web thực thi. | [Lập lịch bên ngoài](/dynamics365/project-operations/project-management/external-scheduling) |
| Triển khai và cấu hình | <p>**Cho phép khách hàng lựa chọn hình thức triển khai**<br>Các bản cập nhật hướng sản phẩm (PDU) của Project Operations được sử dụng để tự động cài đặt giải pháp Ghi kép của Project Operations khi các giải pháp điều phối và lõi ghi kép được cài đặt trong môi trường.</p><p>Tính năng này giới thiệu một tham số **hành vi nâng cấp giải pháp** mới trong Tham số dự án. Khi thông số này được đặt thành **Chỉ Lite**, PUD sẽ không còn tự động cài đặt giải pháp Ghi kép cho Project Operations nữa, ngay cả khi các giải pháp điều phối và lõi ghi kép được cài đặt trong môi trường. Hành vi này sẽ mang lại lợi ích cho những khách hàng dự định sử dụng giải pháp Ghi kép để tích hợp đơn bán hàng vào ứng dụng tài chính và vận hành, nhưng muốn sử dụng Project Operations ở chế độ Lite (nghĩa là không tích hợp vào ứng dụng tài chính và vận hành).</p> | |

## <a name="quality-updates"></a>Bản cập nhật chất lượng

| Lĩnh vực tính năng | Số tham chiếu | Cập nhật chất lượng |
| --- | --- | --- |
| Định giá và thanh toán | 2316317 | Hệ thống cho phép tạo hóa đơn không có giao dịch tính phí. |
| Định giá và thanh toán | 2737300 | Xác thực tính khả dụng của trường Khách hàng trước khi biểu mẫu được truy cập. |
| Định giá và thanh toán | 2744948 | Thêm kiểm tra null cho Phương thức thanh toán. |
| Định giá và thanh toán | 2763515 | Xử lý lỗi tham chiếu null khi thiếu hợp đồng mua bán của hóa đơn. |
| Định giá và thanh toán | 2844301 | Tạo hóa đơn hàng loạt không thành công do lỗi. |
| Định giá và thanh toán | 2845869 | Lưu trữ Dịch vụ Tổ chức không chính xác. |
| Định giá và thanh toán | 2853729 | Chi tiết Vai trò và Giá được cập nhật khi Loại thanh toán được sửa đổi. |
| Định giá và thanh toán | 2940350 | Khi giá thực tế được định giá, chỉ các bảng giá đang hoạt động mới được nhập tự động. |
| Triển khai và cấu hình | 3001206 | Thực thể msdyn\_ replaylogheader đang ngăn việc nâng cấp của Tổ chức khách hàng. |
| Quản lý cơ hội | 2755582 | Xử lý ngoại lệ tham chiếu null trong Trình trợ giúp quy tắc thanh toán chia tách. |
| Quản lý cơ hội | 2761477 | Khi thanh toán chia nhỏ được sử dụng, việc xóa một cột mốc (tiêu đề) sẽ để lại các cột mốc mồ côi. |
| Quản lý cơ hội | 2767595 | Khi một bản ghi sử dụng tài liệu được mở trong biểu mẫu chính, tài nguyên có thể đặt trước cho bản ghi được thay đổi thành người dùng hiện đang đăng nhập. |
| Hoạch định và theo dõi dự án | 2790384 | Thời gian chờ của OperationSet đang chờ xử lý quá ngắn. |
| Quản lý nguồn lực | 2751560 | Đơn vị Tổ chức Ưu tiên Không nhất quán trong Yêu cầu Nguồn lực. |
| Hợp đồng phụ | 2907231 | Không thể tạm ứng giai đoạn xử lý hóa đơn của nhà cung cấp. |
| Thời gian và Chi phí | 2867363 | Các bản ghi không nằm ngoài dạng xem Vắng mặt/Nghỉ phép để phê duyệt khi chúng đang xếp hàng chờ phê duyệt. |
| Thời gian và Chi phí | 2894405 | TESA: Thư mục POC không được sử dụng đang gây ra sự cố tuân thủ. |
