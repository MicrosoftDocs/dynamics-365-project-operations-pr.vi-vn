---
title: Các phiên bản bản đồ ghi kép Project Operations
description: Bài viết này cung cấp danh sách các bản đồ viết kép được yêu cầu Dynamics 365 Project Operations.
author: sigitac
ms.date: 07/01/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b86b9ecdc63989189c76dd8380024aa44c7641a5
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621108"
---
# <a name="project-operations-dual-write-map-versions"></a>Các phiên bản bản đồ ghi kép Project Operations

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Sử dụng Dynamics 365 Project Operations cho các kịch bản nguồn lực/không tồn kho yêu cầu một tập hợp các bản đồ ghi kép để chạy trong môi trường. 

## <a name="prerequisite-maps-dual-write-orchestration-solution"></a>Bản đồ điều kiện tiên quyết: Giải pháp điều phối ghi kép

Các bản đồ sau đây là điều kiện tiên quyết cần thiết cho giải pháp Project Operations. Đảm bảo chạy các bản đồ được liệt kê trong bảng sau và bất kỳ bản đồ bảng nào có liên quan trong môi trường của bạn.

| Bản đồ bảng | Đồng bộ ban đầu |
| --- | --- |
| Sổ cái (msdyn_ledgers) | Yêu cầu đồng bộ ban đầu cho sơ đồ bảng và tất cả các điều kiện tiên quyết. Master cho đồng bộ hóa ban đầu là ứng dụng tài chính và hoạt động. |
| Pháp nhân (cdm_companies) | Không bắt buộc. Hệ thống tự động điền thực thể này khi các môi trường được liên kết bằng tính năng ghi kép. |
| Khách hàng V3 (tài khoản) | Không cần phải cung cấp. |
| Nhà cung cấp V2 (msdyn_vendors) | Không cần phải cung cấp. |

1. Từ danh sách sơ đồ, hãy chọn bản đồ Sổ cái **(msdyn\_ledgers)** với mọi yêu cầu tiên quyết rồi đánh dấu vào ô **Đồng bộ ban đầu**. Bên trong **Chính cho đồng bộ hóa ban đầu** trường, chọn **Ứng dụng tài chính và hoạt động** cho cả bản đồ sổ cái và tất cả các bản đồ tiên quyết. Chọn **Chạy**.

![Đồng bộ hóa sơ đồ sổ cái.](media/DW6.png)

2. Làm theo các bước tương tự cho tất cả các sơ đồ bảng còn lại được liệt kê trong bảng trên. Không chọn hộp kiểm **Đồng bộ ban đầu** khi chạy các bản đồ đó.

## <a name="project-operations-dual-write-maps"></a>Bản đồ ghi kép của Project Operations

Các bản đồ sau đây là điều kiện tiên quyết cần thiết cho một giải pháp Project Operations. Các phiên bản ánh xạ ghi kép được liệt kê từ bản cập nhật Project Operations tháng 5 năm 2021, phiên bản 4.10.0.186.

| Bản đồ thực thể | Phiên bản mới nhất | Đồng bộ ban đầu | Phiên bản Dynamics 365 Finance bắt buộc |
| --- | --- | --- | --- |
| Thực thể tích hợp cho các mối quan hệ giao dịch dự án (msdyn\_transactionconnections) | 1.0.0.0 | Không cần phải cung cấp. ||
| Tiêu đề hợp đồng dự án (đơn đặt hàng) | 1.0.0.1 | Không cần phải cung cấp. ||
| Mô tả hợp đồng dự án (salesorderdetails) | 1.0.0.0 | Không cần phải cung cấp. ||
| Nguồn tài trợ dự án (msdyn_projectcontractsplitbillingrules) | 1.0.0.2 | Không cần phải cung cấp. ||
| Bảng tích hợp dự án để ước tính vật liệu (msdyn\_ đường ước tính) | 1.0.0.0 | Không cần phải cung cấp. ||
| Đề xuất hóa đơn dự án V2 (hóa đơn) | 1.0.0.3 | Không cần phải cung cấp. ||
| Giá trị tích hợp thực tế của Project Operations (msdyn_actuals) | 1.0.0.15 | Không cần phải cung cấp. |10.0.29 trở lên|
| Các mốc quan trọng của mô tả hợp đồng tích hợp Project Operations (msdyn_contractlinescheduleofvalues) | 1.0.0.4 | Không cần phải cung cấp. ||
| Thực thể tích hợp Project Operations để dự toán chi phí (msdyn_estimatelines) | 1.0.0.2 | Không cần phải cung cấp. ||
| Thực thể tích hợp Project Operations để ước tính giờ (msdyn_resourceassignments) | 1.0.0.5 | Không cần phải cung cấp. ||
| Thực thể xuất danh mục chi phí dự án tích hợp của Project Operations (msdyn_expensecategories) | 1.0.0.1 | Không cần phải cung cấp. ||
| Thực thể xuất chi phí dự án tích hợp của Project Operations (msdyn_expenses) | 1.0.0.3 | Không cần phải cung cấp. ||
| Thực thể xuất hóa đơn nhà cung cấp của Project Operations (msdyn_projectvendorinvoices) | 1.0.0.2 | Không cần phải cung cấp. |10.0.29 trở lên|
| Thực thể xuất mô tả hóa đơn nhà cung cấp của Project Operations (msdyn_projectvendorinvoicelines) | 1.0.0.5 | Không cần phải cung cấp. | 10.0.29 trở lên |
| Vai trò nguồn lực dự án cho tất cả các công ty (bookableresourcecategories) | 1.0.0.1 | Yêu cầu đồng bộ hóa ban đầu cho sơ đồ bảng để đồng bộ hóa vai trò nguồn lực của Người quản lý dự án và thành viên Nhóm được điền trong môi trường Dynamics 365 Dataverse trong quá trình cung cấp. Dataverse là nguồn chính cho quá trình đồng bộ hóa ban đầu. ||
| Nhiệm vụ dự án (msdyn_projecttasks) | 1.0.0.4 | Không cần phải cung cấp. ||
| Danh mục giao dịch dự án (msdyn_transactioncategories) | 1.0.0.0 | Không cần phải cung cấp. ||
| Dự án V2 (msdyn_projects) | 1.0.0.2 | Không cần phải cung cấp. ||

Hoàn thành các bước sau để chạy các bản đồ được liệt kê.

1. Bật các vai trò nguồn lực Dự án cho bản đồ bảng **tất cả các công ty (bookableresourcecategories)** vì bản đồ này yêu cầu đồng bộ ban đầu. Trong trường **Bản cái cho đồng bộ hóa ban đầu**, hãy chọn **Common data service**. 

 ![Đồng bộ hóa bản đồ vai trò nguồn lực.](media/6ResourceInitialSync.jpg)

 Chờ đến khi trạng thái của bản đồ là **Đang chạy** trước khi bạn chuyển sang bước tiếp theo.

2. Chọn tất cả các bản đồ cần thiết còn lại. Bạn có thể lọc bản đồ trong danh sách bản đồ ghi kép bằng cách sử dụng từ khóa **Dự án** trong thanh tìm kiếm ở góc trên bên phải. Bạn có thể chọn nhiều bản đồ rồi chạy. Để biết thêm thông tin, hãy xem [Quản lý nhiều bản đồ bảng](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/multiple-entity-maps). Đảm bảo kích hoạt và chạy các bản đồ thực thể liên quan.

### <a name="project-operations-dual-write-map-versions"></a>Các phiên bản bản đồ ghi kép Project Operations

Luôn chạy phiên bản bản đồ mới nhất trong môi trường của bạn. Một số tính năng và chức năng nhất định có thể không hoạt động chính xác nếu tồn tại bất kỳ điều kiện nào sau đây:

- Bản đồ chưa được kích hoạt.
- Phiên bản mới nhất của bản đồ chưa được kích hoạt. 
- Bản đồ bảng có liên quan không được kích hoạt.

Bạn có thể xem phiên bản hiện hoạt của bản đồ trong cột **Phiên bản** trên trang **Ghi kép**. Bạn có thể kích hoạt phiên bản mới của bản đồ bằng cách chọn **Phiên bản bản đồ bảng**, chọn phiên bản mới nhất rồi lưu phiên bản đã chọn. Nếu đã tùy chỉnh sơ đồ bảng có sẵn, bạn sẽ cần áp dụng lại các thay đổi. Để biết thêm thông tin, hãy xem [Quản lý vòng đời áp dụng](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).