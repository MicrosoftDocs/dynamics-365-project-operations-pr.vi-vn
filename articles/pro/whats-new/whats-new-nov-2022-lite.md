---
title: Có gì mới Tháng 11 năm 2022 - Triển khai rút gọn Project Operations
description: Bài viết này cung cấp thông tin về các bản cập nhật chất lượng có sẵn trong bản phát hành triển khai Microsoft Dynamics 365 Project Operations lite tháng 11 năm 2022.
author: ryansandness
ms.date: 12/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: ed61f8c03c4ab1960aaf97712b3d46dc298ce96a
ms.sourcegitcommit: 952fcefe33de192ad48f4108c3adbe658fd7b94f
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831153"
---
# <a name="whats-new-november-2022---project-operations-lite-deployment"></a>Có gì mới Tháng 11 năm 2022 - Triển khai rút gọn Project Operations

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Bài viết này áp dụng cho các phiên bản và thành phần sau của Microsoft Dynamics 365 Project Operations:

- Project Operations trong môi trường Dataverse phiên bản 4.58.0.119


## <a name="quality-updates"></a>Bản cập nhật chất lượng

| Lĩnh vực tính năng | Số tham chiếu | Cập nhật chất lượng |
| --- | --- | --- |
| Định giá và thanh toán | 2781818 | Lỗi không tìm thấy khóa trong khi đặt giá mặc định cho nhật ký sử dụng vật liệu. |
| Định giá và thanh toán | 2922373 | Không thể liên kết mô tả báo giá với dự án đã đóng dưới dạng báo giá bị mất. |
| Định giá và thanh toán | 2943206 | **Trường Mô tả hợp đồng** trong Thực thể dự án phải là tùy chọn. |
| Định giá và thanh toán | 2953182 | Cải thiện thông báo lỗi cho hóa đơn sửa chữa.|
| Định giá và thanh toán | 2959500 | Không thể liên kết mô tả báo giá với nhiệm vụ dự án đã được liên kết với báo giá bị mất.|
| Định giá và thanh toán | 2959560 | Đã nhận được thông báo "Khách hàng này đã có trong Hợp đồng dự án" khi đóng báo giá là đã thắng ở một số ngôn ngữ nhất định. |
| Định giá và thanh toán | 3031727 | Gán tài nguyên không thành công với trường Bắt buộc 'msdyn_Company' bị thiếu lỗi. |
| Định giá và thanh toán | 3036905 | Công ty sở hữu không bao giờ được khởi tạo trên ProjectTeamMember. |
| Quản lý cơ hội | 2763519 | Lỗi Tham chiếu Null trong EnsureProjectContractAllowsUpdates. |
| Quản lý cơ hội | 2783798 | Khi nhập ước tính dự án trên mô tả báo giá, mô tả nhiệm vụ bị thiếu đối với ước tính chi phí và vật liệu.|
| Quản lý cơ hội | 2988635 | Cải thiện mô tả thông báo lỗi khi xóa Khách hàng trên Báo giá. |
| Quản lý cơ hội | 3001191 | Không thể tạo báo giá từ Cơ hội trong đó phương thức thanh toán được chỉ định là null. |
| Nâng cấp | 3012324 | Chuyển đổi dự án không thành công trên một dự án có các ký tự điều khiển như Tab trong tên của dự án. || Hoạch định và theo dõi dự án | 2790384 | Thời gian chờ của OperationSet đang chờ xử lý quá ngắn. |
| Hoạch định và theo dõi dự án | 3044275 | Thiếu bản địa hóa cho: missingProjectSchedulerErrorMessage. |
| Hoạch định và theo dõi dự án | 3044277 | Lưới điều chỉnh dự án không tải khi bộ lập lịch không được đặt.|
| Quản lý nguồn lực | 2943153 | Cập nhật tab Theo dõi để hiển thị hai chữ số thập phân cho Thời lượng.|
| Hợp đồng phụ | 2932774 | Nhà cung cấp hóa đơn dòng chỉ đọc ném sai lỗi. |
| Hợp đồng phụ | 2939556 | Không nên đặt trạng thái Tiêu đề hóa đơn của nhà cung cấp thành Xóa bản nháp trực tuyến nếu không hoạt động. |
| Thời gian và Chi phí | 2939998 | Tiếp nhận phiên bản TESA mới trong ProjOps. |
