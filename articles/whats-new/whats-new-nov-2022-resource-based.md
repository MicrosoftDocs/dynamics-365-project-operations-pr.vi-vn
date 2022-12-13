---
title: Có gì mới Tháng 11 năm 2022 - Project Operations cho các tình huống dựa trên nguồn lực/không có hàng trong kho
description: Bài viết này cung cấp thông tin về các bản cập nhật chất lượng có sẵn trong bản phát hành tháng 11 năm 2022 của Microsoft Dynamics 365 Project Operations cho các tình huống dựa trên tài nguyên/không có hàng trong kho.
author: ryansandness
ms.date: 12/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 509e303aeb0567627590fd89c6888b59a414c6f1
ms.sourcegitcommit: 952fcefe33de192ad48f4108c3adbe658fd7b94f
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831152"
---
# <a name="whats-new-november-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Có gì mới Tháng 11 năm 2022 - Project Operations cho các tình huống dựa trên nguồn lực/không có hàng trong kho

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Bài viết này áp dụng cho các phiên bản và thành phần sau của Microsoft Dynamics 365 Project Operations:

- Project Operations trong môi trường Dataverse phiên bản 4.58.0.119
- Quản lý dự án và kế toán trong môi trường ứng dụng Dynamics 365 Finance phiên bản 10.0.30

## <a name="project-operations-dual-write-maps-updates"></a>Cập nhật về bản đồ ghi kép của Project Operations

Không có bản cập nhật nào cho bản đồ ghi kép Project Operations trong bản phát hành này. Để biết danh sách hiện tại và các phiên bản của bản đồ ghi kép Project Operations, hãy xem [Phiên bản bản đồ ghi kép Project Operations](../environment/resource-dual-write-maps.md).

Luôn chạy phiên bản bản đồ mới nhất trong môi trường của bạn và bật tất cả các bản đồ bảng liên quan khi bạn cập nhật phiên bản giải pháp Project Operations Dataverse và giải pháp Tài chính. Một số tính năng và chức năng nhất định có thể không hoạt động chính xác nếu phiên bản mới nhất của bản đồ không được kích hoạt. Bạn có thể xem phiên bản hiện hoạt của bản đồ trong cột **Phiên bản** trên trang **Ghi kép**. Để kích hoạt phiên bản mới của bản đồ, hãy chọn **Phiên bản bản đồ bảng**, chọn phiên bản mới nhất rồi lưu phiên bản đã chọn. Nếu đã tùy chỉnh sơ đồ bảng có sẵn, hãy áp dụng lại các thay đổi. Để biết thêm thông tin, hãy xem [Quản lý vòng đời áp dụng](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Nếu bạn gặp sự cố khi khởi động bản đồ, hãy làm theo hướng dẫn trong phần [Vấn đề thiếu cột trong bảng trên bản đồ](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) của hướng dẫn khắc phục sự cố Ghi kép.

## <a name="quality-updates"></a>Bản cập nhật chất lượng

### <a name="project-operations-on-dataverse"></a>Project Operations trên Dataverse

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


### <a name="project-management-and-accounting-in-finance"></a>Quản lý dự án và kế toán trong Tài chính

Để biết thông tin về các bản sửa lỗi có trong bản cập nhật này, hãy đăng nhập vào Microsoft Dynamics Lifecycle Services và xem [Bài viết trên KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).
