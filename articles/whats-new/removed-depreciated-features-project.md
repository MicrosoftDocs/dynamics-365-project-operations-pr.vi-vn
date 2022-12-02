---
title: Các tính năng bị xóa hoặc không dùng nữa trong Dynamics 365 Project Operations
description: Bài viết này mô tả các tính năng đã bị xóa hoặc được lên kế hoạch xóa khỏi Dynamics 365 Project Operations.
author: sigitac
ms.date: 03/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: f0fbaed028db11d8fb1551d304a40543faf35b0d
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028355"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-project-operations"></a>Các tính năng bị xóa hoặc không dùng nữa trong Dynamics 365 Project Operations

_**Áp dụng đối với:** Project Operations cho tình huống dựa trên nguồn lực/hàng không nhập kho, triển khai Lite - từ thỏa thuận đến lập hóa đơn ước giá và Project Operations cho tình huống dựa trên hàng trữ kho/sản xuất_

Bài viết này mô tả các tính năng đã bị xóa hoặc được lên kế hoạch xóa khỏi Dynamics 365 Project Operations.

- Tính năng *đã xóa* không còn khả dụng trong sản phẩm.
- Tính năng *không dùng nữa* không ở trong giai đoạn phát triển tích cực và có thể bị xóa khỏi bản cập nhật trong tương lai.

Danh sách này giúp bạn cân nhắc những tính năng cần xóa và không dùng nữa cho kế hoạch của riêng mình.

> [!NOTE]
> Thông tin chi tiết về các đối tượng trong ứng dụng tài chính và hoạt động có thể được tìm thấy trong [**Báo cáo tham chiếu kỹ thuật**](/dynamics/s-e/global/axtechrefrep_61). Bạn có thể so sánh các phiên bản khác nhau của các báo cáo này để tìm hiểu về các đối tượng đã thay đổi hoặc bị xóa trong mỗi phiên bản ứng dụng tài chính và hoạt động.

## <a name="features-removed-or-deprecated-in-the-project-operations-march-2022-release"></a>Các tính năng bị xóa hoặc không dùng nữa trong Project Operations bản phát hành tháng 3 năm 2022

### <a name="project-management-and-accounting-always-create-adjustment-transaction-parameter"></a>Tham số "Luôn tạo giao dịch điều chỉnh" của quản lý dự án và kế toán

| &nbsp; | &nbsp; |
|--------|--------|
| **Lý do không dùng nữa/xóa** | Các giao dịch điều chỉnh được yêu cầu cho mục đích kiểm toán. Sau khi không dùng nữa, tham số này sẽ bị ẩn. Hệ thống sẽ luôn tạo các giao dịch điều chỉnh, giống như hiện tại khi tham số được đặt thành **Có**. |
| **Được thay thế bởi một tính năng khác?** | No |
| **Lĩnh vực sản phẩm bị ảnh hưởng** | Ứng dụng |
| **Tùy chọn triển khai** | Project Operations dành cho tình huống dựa trên sản xuất/hàng trữ kho |
| **Trạng thái** | Không dùng nữa: Đến ngày 1 tháng 3 năm 2023, chúng tôi sẽ ẩn tham số và thay đổi hành vi hệ thống để các giao dịch điều chỉnh luôn được tạo. |

### <a name="project-management-and-accounting-use-adjustment-date-as-new-project-date-parameter"></a>Tham số "Sử dụng ngày điều chỉnh làm ngày dự án mới" của quản lý dự án và kế toán

| &nbsp; | &nbsp; |
|--------|--------|
| **Lý do không dùng nữa/xóa** | Tham số này ban đầu được sử dụng để cho phép điều chỉnh khi kỳ tài chính bị đóng. Tuy nhiên, nó không còn bắt buộc nữa, vì ngày kế toán của giao dịch có thể được thay đổi thành ngày đầu tiên của kỳ mở, nếu nó được định cấu hình. Ngày dự án không được thay đổi, vì nó đại diện cho ngày mà giao dịch xảy ra. |
| **Được thay thế bởi một tính năng khác?** | No |
| **Lĩnh vực sản phẩm bị ảnh hưởng** | Ứng dụng |
| **Tùy chọn triển khai** | Project Operations dành cho tình huống dựa trên sản xuất/hàng trữ kho |
| **Trạng thái** | Không dùng nữa: Đến ngày 1 tháng 3 năm 2023, chúng tôi sẽ ẩn tham số và thay đổi hành vi hệ thống để ngày giao dịch không bao giờ bị thay đổi khi điều chỉnh. |

### <a name="resource-request-workflow-in-project-operations-for-stockedproduction-based-scenarios"></a>Quy trình yêu cầu nguồn lực trong Project Operations cho các kịch bản dựa trên hàng trữ kho/sản xuất

| &nbsp; | &nbsp; |
|--------|--------|
| **Lý do không dùng nữa/xóa** | Không dùng nữa vì mức sử dụng thấp và giới hạn về khối lượng giao dịch. |
| **Được thay thế bởi một tính năng khác?** | No |
| **Lĩnh vực sản phẩm bị ảnh hưởng** | Ứng dụng |
| **Tùy chọn triển khai** | Project Operations dành cho tình huống dựa trên sản xuất/hàng trữ kho |
| **Trạng thái** | Không dùng nữa: Đến ngày 1 tháng 3 năm 2023, chúng tôi sẽ vô hiệu hóa tùy chọn yêu cầu nguồn lực cho dự án bằng cách sử dụng quy trình làm việc. |

### <a name="project-invoice-proposal-page-without-header-and-lines-views"></a>Trang đề xuất hóa đơn dự án không có dạng xem Tiêu đề và Dòng

| &nbsp; | &nbsp; |
|--------|--------|
| **Lý do không dùng nữa/xóa** | Không dùng nữa vì những cải tiến đối với trang đã được giới thiệu cùng với khóa tính năng **Sử dụng đề xuất hóa đơn Dự án và biểu mẫu nhật ký hóa đơn với dạng xem Tiêu đề và Dòng**. |
| **Được thay thế bởi một tính năng khác?** | Có |
| **Lĩnh vực sản phẩm bị ảnh hưởng** | Ứng dụng |
| **Tùy chọn triển khai** | Project Operations cho các tình huống sản xuất/trữ kho; Project Operations cho các tình huống nguồn lực/không trữ kho |
| **Trạng thái** | Không dùng nữa: Đến ngày 1 tháng 3 năm 2023, chúng tôi sẽ tắt trang trước đó (cũ) và bật khóa tính năng **Sử dụng đề xuất hóa đơn Dự án và biểu mẫu nhật ký hóa đơn với dạng xem Tiêu đề và Dòng** theo mặc định. |

## <a name="features-removed-or-deprecated-in-the-project-operations-december-2021-release"></a>Các tính năng bị xóa hoặc không dùng nữa trong Project Operations bản phát hành tháng 12 năm 2021

### <a name="collaboration-workspaces"></a>Không gian làm việc cộng tác

[Tạo hoặc liên kết đến một không gian làm việc cộng tác (Dự án)](/dynamicsax-2012/appuser-itpro/create-or-link-to-a-collaboration-workspace-project)

| &nbsp; | &nbsp; |
|--------|--------|
| **Lý do không dùng nữa/xóa** | Không dùng nữa do mức sử dụng thấp. Khách hàng sử dụng Project Operations cho các trường hợp nguồn lực/không trữ kho có thể tận dụng [Cộng tác với Nhóm Office](../project-management/collaboration-groups.md). |
| **Được thay thế bởi một tính năng khác?** | No |
| **Lĩnh vực sản phẩm bị ảnh hưởng** | Ứng dụng  |
| **Tùy chọn triển khai** | Project Operations dành cho tình huống dựa trên sản xuất/hàng trữ kho |
| **Trạng thái** | Không dùng nữa: Đến ngày 1 tháng 12 năm 2022, chúng tôi dự định sẽ không hỗ trợ không gian làm việc Cộng tác nữa. |
