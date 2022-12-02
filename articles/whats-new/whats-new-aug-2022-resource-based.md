---
title: Tính năng mới kể từ tháng 8 năm 2022 – Project Operations cho các kịch bản dựa trên nguồn lực/hàng không nhập kho
description: Bài viết này cung cấp thông tin về các bản cập nhật chất lượng có trong bản phát hành tháng 8 năm 2022 của Microsoft Dynamics 365 Project Operations cho các kịch bản dựa trên nguồn lực/hàng không nhập kho.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 4042dca72a33f48e04e51af2a3cfd2da83146afd
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403883"
---
# <a name="whats-new-august-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Tính năng mới kể từ tháng 8 năm 2022 – Project Operations cho các kịch bản dựa trên nguồn lực/hàng không nhập kho

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Bài viết này áp dụng cho các phiên bản và thành phần sau của Microsoft Dynamics 365 Project Operations:

- Project Operations trong môi trường Dataverse phiên bản 4.45.0.53
- Quản lý dự án và kế toán trong môi trường ứng dụng Dynamics 365 Finance phiên bản 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Cập nhật về bản đồ ghi kép của Project Operations

Không có bản cập nhật nào cho bản đồ ghi kép Project Operations trong bản phát hành này. Để biết danh sách hiện tại và các phiên bản của bản đồ ghi kép Project Operations, hãy xem [Phiên bản bản đồ ghi kép Project Operations](../environment/resource-dual-write-maps.md).

Luôn chạy phiên bản bản đồ mới nhất trong môi trường của bạn và bật tất cả các bản đồ bảng liên quan khi bạn cập nhật phiên bản giải pháp Project Operations Dataverse và giải pháp Tài chính. Một số tính năng và chức năng nhất định có thể không hoạt động chính xác nếu phiên bản mới nhất của bản đồ không được kích hoạt. Bạn có thể xem phiên bản hiện hoạt của bản đồ trong cột **Phiên bản** trên trang **Ghi kép**. Để kích hoạt phiên bản mới của bản đồ, hãy chọn **Phiên bản bản đồ bảng**, chọn phiên bản mới nhất rồi lưu phiên bản đã chọn. Nếu đã tùy chỉnh sơ đồ bảng có sẵn, hãy áp dụng lại các thay đổi. Để biết thêm thông tin, hãy xem [Quản lý vòng đời áp dụng](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Nếu bạn gặp sự cố khi khởi động bản đồ, hãy làm theo hướng dẫn trong phần [Vấn đề thiếu cột trong bảng trên bản đồ](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) của hướng dẫn khắc phục sự cố Ghi kép.

## <a name="quality-updates"></a>Bản cập nhật chất lượng

### <a name="project-operations-on-dataverse"></a>Project Operations trên Dataverse

| Lĩnh vực tính năng | Số tham chiếu | Cập nhật chất lượng |
| --- | --- | --- |
|   Quản lý cơ hội | 2762089 | Lỗi xử lý khi đóng hợp đồng là đã mất nếu tính năng tự động lưu bị tắt trong tổ chức.|
|Hoạch định và theo dõi dự án | 2767841 | Phương pháp đo từ xa cập nhật kịch bản Tạo hoặc Cập nhật Thực thể dự án.|
|Định giá và thanh toán | 2771072 | Xử lý ngoại lệ tham chiếu rỗng trong khi giành được báo giá.|
|Định giá và thanh toán | 2844181 |Không thể lấy id tương quan và chặn hoạt động tạo hóa đơn.|
|Định giá và thanh toán | 2852836 | Số liệu thực tế liên công ty còn thiếu cho Chi phí liên công ty được tạo và phê duyệt trong CE.|


### <a name="project-management-and-accounting-in-finance"></a>Quản lý dự án và kế toán trong Tài chính

Để biết thông tin về các bản sửa lỗi có trong bản cập nhật này, hãy đăng nhập vào Microsoft Dynamics Lifecycle Services (LCS) và xem [Bài viết trên KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).
