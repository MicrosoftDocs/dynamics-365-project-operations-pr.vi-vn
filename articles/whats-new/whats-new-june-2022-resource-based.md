---
title: Tính năng mới kể từ tháng 6 năm 2022 – Project Operations cho các kịch bản dựa trên nguồn lực/hàng không trữ kho
description: Bài viết này cung cấp thông tin về các bản cập nhật chất lượng có trong bản phát hành tháng 6 năm 2022 của Microsoft Dynamics 365 Project Operations cho các kịch bản dựa trên nguồn lực/hàng không nhập kho.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 32bc7793c5a0ee8c04272d3ffcbd290b39fce4cc
ms.sourcegitcommit: 7772d72a7c96a44ffb23369f8ffb436813449239
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/20/2022
ms.locfileid: "9031357"
---
# <a name="whats-new-june-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Tính năng mới kể từ tháng 6 năm 2022 – Project Operations cho các kịch bản dựa trên nguồn lực/hàng không trữ kho

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Bài viết này áp dụng cho các phiên bản và thành phần sau của Microsoft Dynamics 365 Project Operations:

- Project Operations trong môi trường Dataverse phiên bản 4.43.0.77 hoặc 4.43.0.119
- Quản lý dự án và kế toán trong môi trường ứng dụng Dynamics 365 Finance phiên bản 10.0.27

## <a name="project-operations-dual-write-maps-updates"></a>Cập nhật về bản đồ ghi kép của Project Operations

Bảng sau đây hiển thị các bản đồ ghi kép đã được sửa đổi hoặc bổ sung trong bản phát hành Project Operations vào tháng 6 năm 2022.

| Bản đồ thực thể | Phiên bản đã cập nhật | Bình luận |
| --- | --- | --- |
| Thực thể xuất hóa đơn nhà cung cấp của Project Operations (msdyn_projectvendorinvoices) | 1.0.0.1 | Không dùng trường cũ và ánh xạ sang trường mới đối với theo dõi trạng thái hóa đơn của nhà cung cấp. |

Luôn chạy phiên bản bản đồ mới nhất trong môi trường của bạn và bật tất cả các bản đồ bảng liên quan khi bạn cập nhật phiên bản giải pháp Project Operations Dataverse và giải pháp Tài chính. Một số tính năng và chức năng nhất định có thể không hoạt động chính xác nếu phiên bản mới nhất của bản đồ không được kích hoạt. Bạn có thể xem phiên bản hiện hoạt của bản đồ trong cột **Phiên bản** trên trang **Ghi kép**. Để kích hoạt phiên bản mới của bản đồ, hãy chọn **Phiên bản bản đồ bảng**, chọn phiên bản mới nhất rồi lưu phiên bản đã chọn. Nếu đã tùy chỉnh sơ đồ bảng có sẵn, hãy áp dụng lại các thay đổi. Để biết thêm thông tin, hãy xem [Quản lý vòng đời áp dụng](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Nếu bạn gặp sự cố khi khởi động bản đồ, hãy làm theo hướng dẫn trong phần [Vấn đề thiếu cột trong bảng trên bản đồ](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) của hướng dẫn khắc phục sự cố Ghi kép.

## <a name="quality-updates"></a>Bản cập nhật chất lượng

### <a name="project-operations-on-dataverse"></a>Project Operations trên Dataverse

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
| Hợp đồng phụ | 2677485 | Đã cập nhật phiên bản mục tiêu của ánh xạ ghi kéo mô tả hóa đơn của nhà cung cấp. |
| Thời gian và chi phí | 2700428 | Cải thiện logic phê duyệt để đảm bảo rằng các bộ phê duyệt khác cho dự án có thể được xử lý ngay cả khi một trong các bộ phê duyệt bị kẹt trong các công việc hệ thống. |

### <a name="project-management-and-accounting-in-finance"></a>Quản lý dự án và kế toán trong Tài chính

Để biết thông tin về các bản sửa lỗi có trong bản cập nhật này, hãy đăng nhập vào Microsoft Dynamics Lifecycle Services (LCS) và xem [Bài viết trên KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271).
