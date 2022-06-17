---
title: Có gì mới Tháng 6 năm 2022 - Hoạt động Dự án cho các kịch bản dựa trên tài nguyên / không có kho
description: Bài viết này cung cấp thông tin về các bản cập nhật chất lượng có sẵn trong bản phát hành tháng 6 năm 2022 của Microsoft Dynamics 365 Project Operations cho các kịch bản dựa trên tài nguyên / không có kho.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fde1f0be42eecfc5ee809cb9b2191d3aeae57131
ms.sourcegitcommit: 51745acac29dfacba43a4003d86baff4d6ca2fb8
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/14/2022
ms.locfileid: "8959722"
---
# <a name="whats-new-june-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Có gì mới Tháng 6 năm 2022 - Hoạt động Dự án cho các kịch bản dựa trên tài nguyên / không có kho

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Bài viết này áp dụng cho các thành phần và phiên bản sau của Microsoft Dynamics 365 Project Operations:

- Hoạt động dự án trong một Dataverse phiên bản môi trường 4.43.0.77
- Quản lý dự án và kế toán trong môi trường Dynamics 365 Finance phiên bản 10.0.27

## <a name="project-operations-dual-write-maps-updates"></a>Cập nhật về bản đồ ghi kép của Project Operations

Bảng sau đây cho thấy các bản đồ viết kép đã được sửa đổi hoặc bổ sung trong bản phát hành Project Operations vào tháng 6 năm 2022.

| Bản đồ thực thể | Phiên bản đã cập nhật | Bình luận |
| --- | --- | --- |
| Thực thể xuất hóa đơn nhà cung cấp của Project Operations (msdyn_projectvendorinvoices) | 1.0.0.1 | Không dùng trường kế thừa và được ánh xạ tới trường mới để theo dõi trạng thái hóa đơn của nhà cung cấp. |

Luôn chạy phiên bản bản đồ mới nhất trong môi trường của bạn và bật tất cả các bản đồ bảng liên quan khi bạn cập nhật Hoạt động dự án của mình Dataverse giải pháp và phiên bản giải pháp Tài chính. Một số tính năng và khả năng có thể không hoạt động chính xác nếu phiên bản mới nhất của bản đồ không được kích hoạt. Bạn có thể xem phiên bản hiện hoạt của bản đồ trong cột **Phiên bản** trên trang **Ghi kép**. Để kích hoạt phiên bản mới của bản đồ, hãy chọn **Phiên bản bản đồ bảng**, chọn phiên bản mới nhất rồi lưu phiên bản đã chọn. Nếu bạn đã tùy chỉnh sơ đồ bảng ngoài hộp, hãy áp dụng lại các thay đổi. Để biết thêm thông tin, hãy xem [Quản lý vòng đời áp dụng](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Nếu bạn gặp sự cố khi khởi động bản đồ, hãy làm theo hướng dẫn trong [Vấn đề thiếu cột trong bảng trên bản đồ](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) phần của hướng dẫn khắc phục sự cố Ghi kép.

## <a name="quality-updates"></a>Bản cập nhật chất lượng

### <a name="project-operations-on-dataverse"></a>Project Operations trên Dataverse

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
| Thầu phụ | 2677485 | Đã cập nhật phiên bản mục tiêu của bản đồ viết kép các dòng hóa đơn của nhà cung cấp. |
| Thời gian và chi phí | 2700428 | Cải thiện logic phê duyệt để đảm bảo rằng các bộ phê duyệt khác cho dự án có thể được xử lý ngay cả khi một trong các bộ phê duyệt bị kẹt trong các công việc hệ thống. |

### <a name="project-management-and-accounting-in-finance"></a>Quản lý dự án và kế toán trong lĩnh vực tài chính

Để biết thông tin về các bản sửa lỗi có trong bản cập nhật này, hãy đăng nhập vào Microsoft Dynamics Dịch vụ Vòng đời (LCS) và xem [KB bài báo](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271).
