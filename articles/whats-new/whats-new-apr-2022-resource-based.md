---
title: Có gì mới Tháng 4 năm 2022 - Hoạt động Dự án cho các tình huống dựa trên tài nguyên / không có kho
description: Chủ đề này cung cấp thông tin về các bản cập nhật chất lượng có sẵn trong bản phát hành tháng 4 năm 2022 của Microsoft Dynamics 365 Project Operations cho các kịch bản dựa trên tài nguyên / không có hàng.
author: sigitac
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: dc713e7a0dd6993e38ce3e3b2ba19f796a6f4773
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/18/2022
ms.locfileid: "8613348"
---
# <a name="whats-new-april-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Có gì mới Tháng 4 năm 2022 - Hoạt động Dự án cho các tình huống dựa trên tài nguyên / không có kho

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Chủ đề này áp dụng cho các thành phần và phiên bản sau của Microsoft Dynamics 365 Project Operations:

- Hoạt động dự án trong một Dataverse phiên bản môi trường 4.41.0.45
- Quản lý dự án và kế toán trong môi trường Dynamics 365 Finance phiên bản 10.0.26

## <a name="features-included-in-this-release"></a>Các tính năng có trong bản phát hành này

Danh mục mua sắm có thể được sử dụng trong các đơn đặt hàng dự án và các hóa đơn của nhà cung cấp đang chờ xử lý. Để biết thêm thông tin, hãy xem [Sử dụng các danh mục mua sắm với các đơn đặt hàng dự án và các hóa đơn của nhà cung cấp đang chờ xử lý](configure-procurement-categories.md).

## <a name="project-operations-dual-write-maps-updates"></a>Cập nhật về bản đồ ghi kép của Project Operations

Bảng sau đây cho thấy các bản đồ viết kép đã được sửa đổi hoặc bổ sung trong bản phát hành tháng 3 năm 2022 của Hoạt động Dự án.

| Bản đồ thực thể | Phiên bản đã cập nhật | Bình luận |
| -------------- | ------------------- | ------------|
| Dự án Hoạt động tích hợp dự án nhà cung cấp thực thể xuất dòng hóa đơn msdyn\_ dự án | 1.0.0.4 | Bản đồ này hỗ trợ việc sử dụng các danh mục mua sắm với các đơn đặt hàng và hóa đơn của nhà cung cấp đang chờ xử lý. |

Luôn chạy phiên bản bản đồ mới nhất trong môi trường của bạn và bật tất cả các bản đồ bảng liên quan khi bạn cập nhật Hoạt động dự án của mình Dataverse giải pháp và phiên bản giải pháp Tài chính. Một số tính năng và khả năng có thể không hoạt động chính xác nếu phiên bản mới nhất của bản đồ không được kích hoạt. Bạn có thể xem phiên bản hiện hoạt của bản đồ trong cột **Phiên bản** trên trang **Ghi kép**. Để kích hoạt phiên bản mới của bản đồ, hãy chọn **Phiên bản bản đồ bảng**, chọn phiên bản mới nhất rồi lưu phiên bản đã chọn. Nếu bạn đã tùy chỉnh sơ đồ bảng ngoài hộp, hãy áp dụng lại các thay đổi. Để biết thêm thông tin, hãy xem [Quản lý vòng đời áp dụng](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Nếu bạn gặp sự cố khi khởi động bản đồ, hãy làm theo hướng dẫn trong [Vấn đề thiếu cột trong bảng trên bản đồ](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) phần của hướng dẫn khắc phục sự cố Ghi kép.

## <a name="quality-updates"></a>Bản cập nhật chất lượng

### <a name="project-operations-on-dataverse"></a>Project Operations trên Dataverse

| Lĩnh vực tính năng | Số tham chiếu | Cập nhật chất lượng |
| ------------ | ---------------- | -------------- |
| Thời gian và chi phí | 2573900 | Các **Phê duyệt hiện đại** tính năng phải được bật theo mặc định. |
| Định giá và thanh toán | 2603313 | Đã sửa lỗi bản ghi trùng lặp ngăn dòng báo giá và hợp đồng có sản phẩm được thêm vào. |
| Triển khai và cấu hình | 2611368 | Khách hàng phải có thể thêm tối đa năm thực thể tùy chỉnh vào giải pháp bằng cách sử dụng trình thiết kế ứng dụng hiện đại. |
| Thời gian và chi phí | 2628285 | Đã khắc phục sự cố ảnh hưởng đến khả năng đặt danh mục tài nguyên chính xác trong quá trình nhập mục nhập thời gian. |
|   Quản lý cơ hội| 2628815 | Cập nhật giới hạn ký tự của mô tả chi tiết dòng trích dẫn để khớp với giới hạn ký tự của chủ đề nhiệm vụ, để quá trình nhập thành công đối với các nhiệm vụ có chủ đề dài hơn 100 ký tự. |
| Thời gian và chi phí| 2629547 | Các **Gửi bởi** lĩnh vực phê duyệt dự án phải trỏ đến người dùng đã gửi hồ sơ. |
| Thời gian và chi phí| 2629865 | Các **Sao chép danh mục** trường trên các nhiệm vụ khi các dự án được sao chép. |
| Thời gian và chi phí| 2636463 | Đã sửa các bộ lọc về phê duyệt trong các biểu mẫu phê duyệt hiện đại. |
| Hoạch định và theo dõi dự án | 2648300 | Đã khắc phục sự cố ngăn không cho thay đổi chủ sở hữu dự án. |
| Định giá và thanh toán | 2563000 | Không được phép sử dụng các dòng nhật ký cho giao dịch bán chưa lập hóa đơn mà đơn vị tiền tệ khác với đơn vị tiền tệ của hợp đồng. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Quản lý dự án và kế toán trong Dynamics 365 Finance

Để biết thông tin về các bản sửa lỗi có trong bản cập nhật này, hãy đăng nhập vào Microsoft Dynamics Dịch vụ Vòng đời (LCS) và xem [KB bài báo](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
