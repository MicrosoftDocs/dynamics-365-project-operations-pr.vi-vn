---
title: Tính năng mới kể từ tháng 4 năm 2022 – Project Operations cho các kịch bản dựa trên nguồn lực/vật tư không tồn kho
description: Bài viết này cung cấp thông tin về các bản cập nhật chất lượng có trong bản phát hành tháng 4 năm 2022 của Microsoft Dynamics 365 Project Operations cho các kịch bản dựa trên nguồn lực/hàng không nhập kho.
author: sigitac
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 999006b2c2fe2b31d6e47910a3f1a55cab415f0e
ms.sourcegitcommit: 5c971b15295046b3c92ff6638dd1352129f1c390
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 07/01/2022
ms.locfileid: "9110910"
---
# <a name="whats-new-april-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Tính năng mới kể từ tháng 4 năm 2022 – Project Operations cho các kịch bản dựa trên nguồn lực/vật tư không tồn kho

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Bài viết này áp dụng cho các phiên bản và thành phần sau của Microsoft Dynamics 365 Project Operations:

- Project Operations trong môi trường Dataverse phiên bản 4.41.0.45
- Quản lý dự án và kế toán trong môi trường ứng dụng Dynamics 365 Finance phiên bản 10.0.26

## <a name="features-included-in-this-release"></a>Các tính năng có trong bản phát hành này

Các danh mục mua có thể được sử dụng trong đơn đặt hàng dự án và hóa đơn nhà cung cấp đang chờ xử lý. Để biết thêm thông tin, hãy xem [Sử dụng các danh mục mua với các đơn đặt hàng dự án và hóa đơn nhà cung cấp đang chờ xử lý](../procurement/configure-procurement-categories.md).

## <a name="project-operations-dual-write-maps-updates"></a>Cập nhật về bản đồ ghi kép của Project Operations

Bảng sau đây hiển thị các bản đồ ghi kép đã được sửa đổi hoặc bổ sung trong bản phát hành Project Operations vào tháng 3 năm 2022.

| Bản đồ thực thể | Phiên bản đã cập nhật | Bình luận |
| -------------- | ------------------- | ------------|
| Thực thể xuất mô tả hóa đơn nhà cung cấp của dự án tích hợp Project Operations msdyn\_projectvendorinvoicelines | 1.0.0.4 | Bản đồ này hỗ trợ việc sử dụng các danh mục mua với các đơn đặt hàng dự án và hóa đơn nhà cung cấp đang chờ xử lý. |

Luôn chạy phiên bản bản đồ mới nhất trong môi trường của bạn và bật tất cả các bản đồ bảng liên quan khi bạn cập nhật phiên bản giải pháp Project Operations Dataverse và giải pháp Tài chính. Một số tính năng và chức năng nhất định có thể không hoạt động chính xác nếu phiên bản mới nhất của bản đồ không được kích hoạt. Bạn có thể xem phiên bản hiện hoạt của bản đồ trong cột **Phiên bản** trên trang **Ghi kép**. Để kích hoạt phiên bản mới của bản đồ, hãy chọn **Phiên bản bản đồ bảng**, chọn phiên bản mới nhất rồi lưu phiên bản đã chọn. Nếu đã tùy chỉnh sơ đồ bảng có sẵn, hãy áp dụng lại các thay đổi. Để biết thêm thông tin, hãy xem [Quản lý vòng đời áp dụng](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Nếu bạn gặp sự cố khi khởi động bản đồ, hãy làm theo hướng dẫn trong phần [Vấn đề thiếu cột trong bảng trên bản đồ](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) của hướng dẫn khắc phục sự cố Ghi kép.

## <a name="quality-updates"></a>Bản cập nhật chất lượng

### <a name="project-operations-on-dataverse"></a>Project Operations trên Dataverse

| Lĩnh vực tính năng | Số tham chiếu | Cập nhật chất lượng |
| ------------ | ---------------- | -------------- |
| Thời gian và chi phí | 2573900 | Tính năng **Phê duyệt hiện đại** phải được bật theo mặc định. |
| Định giá và thanh toán | 2603313 | Đã sửa lỗi bản ghi trùng lặp ngăn mô tả báo giá và hợp đồng có sản phẩm được thêm vào. |
| Đợt triển khai và Cấu hình | 2611368 | Khách hàng phải có thể thêm tối đa năm thực thể tùy chỉnh vào giải pháp bằng cách sử dụng công cụ thiết kế ứng dụng hiện đại. |
| Thời gian và chi phí | 2628285 | Đã khắc phục sự cố ảnh hưởng đến khả năng đặt danh mục nguồn lực chính xác trong quá trình nhập mục nhập thời gian. |
|   Quản lý cơ hội| 2628815 | Cập nhật giới hạn ký tự của mô tả chi tiết dòng báo giá để khớp với giới hạn ký tự của chủ đề nhiệm vụ, sao cho quá trình nhập thành công đối với các nhiệm vụ trong đó chủ đề dài hơn 100 ký tự. |
| Thời gian và chi phí| 2629547 | Trường **Người gửi** trong các phê duyệt dự án phải trỏ đến người dùng đã gửi bản ghi. |
| Thời gian và chi phí| 2629865 | Trường **Sao chép danh mục** trên các nhiệm vụ khi dự án được sao chép. |
| Thời gian và chi phí| 2636463 | Đã sửa các bộ lọc về phê duyệt trong các biểu mẫu phê duyệt hiện đại. |
| Hoạch định và theo dõi dự án | 2648300 | Đã khắc phục sự cố ngăn không cho thay đổi chủ sở hữu dự án. |
| Định giá và thanh toán | 2563000 | Dòng nhật ký kế toán cho doanh thu chưa lập hóa đơn trong đó đơn vị tiền tệ khác với đơn vị tiền tệ hợp đồng phải không được cho phép. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Quản lý dự án và kế toán trong Dynamics 365 Finance

Để biết thông tin về các bản sửa lỗi có trong bản cập nhật này, hãy đăng nhập vào Microsoft Dynamics Lifecycle Services (LCS) và xem [Bài viết trên KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
