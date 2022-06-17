---
title: Có gì mới Tháng 5 năm 2022 - Hoạt động Dự án cho các kịch bản dựa trên tài nguyên / không có kho
description: Bài viết này cung cấp thông tin về các bản cập nhật chất lượng có sẵn trong bản phát hành tháng 5 năm 2022 của Microsoft Dynamics 365 Project Operations cho các kịch bản dựa trên tài nguyên / không có kho.
author: sigitac
ms.date: 05/02/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: beb75fc4b721d52cddbdaf2d20194218cefced5e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921420"
---
# <a name="whats-new-may-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Có gì mới Tháng 5 năm 2022 - Hoạt động Dự án cho các kịch bản dựa trên tài nguyên / không có kho

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Bài viết này áp dụng cho các thành phần và phiên bản sau của Microsoft Dynamics 365 Project Operations:

- Hoạt động dự án trong một Dataverse phiên bản môi trường 4.42.0.70
- Quản lý dự án và kế toán trong môi trường Dynamics 365 Finance phiên bản 10.0.26

## <a name="project-operations-dual-write-maps-updates"></a>Cập nhật về bản đồ ghi kép của Project Operations

Không có bản cập nhật nào cho bản đồ ghi kép Project Operations trong bản phát hành này. Để biết danh sách hiện tại và các phiên bản của bản đồ ghi kép Project Operations, hãy xem [Phiên bản bản đồ ghi kép Project Operations](../environment/resource-dual-write-maps.md).

Luôn chạy phiên bản bản đồ mới nhất trong môi trường của bạn và bật tất cả các bản đồ bảng liên quan khi bạn cập nhật Hoạt động dự án của mình Dataverse giải pháp và phiên bản giải pháp Tài chính. Một số tính năng và khả năng có thể không hoạt động chính xác nếu phiên bản mới nhất của bản đồ không được kích hoạt. Bạn có thể xem phiên bản hiện hoạt của bản đồ trong cột **Phiên bản** trên trang **Ghi kép**. Để kích hoạt phiên bản mới của bản đồ, hãy chọn **Phiên bản bản đồ bảng**, chọn phiên bản mới nhất rồi lưu phiên bản đã chọn. Nếu bạn đã tùy chỉnh sơ đồ bảng ngoài hộp, hãy áp dụng lại các thay đổi. Để biết thêm thông tin, hãy xem [Quản lý vòng đời áp dụng](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Nếu bạn gặp sự cố khi khởi động bản đồ, hãy làm theo hướng dẫn trong [Vấn đề thiếu cột trong bảng trên bản đồ](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) phần của hướng dẫn khắc phục sự cố Ghi kép.

## <a name="quality-updates"></a>Bản cập nhật chất lượng
### <a name="project-operations-on-dataverse"></a>Project Operations trên Dataverse

| Lĩnh vực tính năng | Số tham chiếu | Cập nhật chất lượng |
| --- | --- | --- |
| Quản lý nguồn lực | 2634019 | Cải thiện thông báo lỗi cho xác thực nghiệp vụ khi thêm các thành viên nhóm chung làm tài nguyên. |
| Hoạch định và theo dõi dự án | 2648515 | Cập nhật hạn chế của **ownerid**, **bang**, và **trạng thái** trong các thực thể lập lịch. |
| Định giá và thanh toán | 2653167 | Các **Ước tính** dấu phân tách thập phân dạng lưới phải tuân theo cài đặt định dạng trong **Tùy chọn cá nhân**. |
| Định giá và thanh toán| 2662251 | Giá trị trong **Đã sửa đơn vị** và **Nhóm đơn vị** trường mặc định khi tạo bản ghi trong ước tính vật liệu. |
| Định giá và thanh toán| 2571408 | Các hướng dẫn sử dụng bán hàng chưa lập hóa đơn được đóng dấu bằng ID hóa đơn chiếu lệ khi tạo hóa đơn nháp. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Quản lý dự án và kế toán trong Dynamics 365 Finance

Để biết thông tin về các bản sửa lỗi có trong bản cập nhật này, hãy đăng nhập vào Microsoft Dynamics Dịch vụ Vòng đời (LCS) và xem [KB bài viết](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
