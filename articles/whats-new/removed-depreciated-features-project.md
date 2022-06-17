---
title: Các tính năng đã bị xóa hoặc không dùng nữa trong Dynamics 365 Project Operations
description: Bài viết này mô tả các tính năng đã bị xóa hoặc được lên kế hoạch xóa khỏi Dynamics 365 Project Operations.
author: sigitac
ms.date: 03/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: df9d8a40fa853e72416e64846bf59748815048be
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921512"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-project-operations"></a>Các tính năng đã bị xóa hoặc không dùng nữa trong Dynamics 365 Project Operations

_**Áp dụng đối với:** Project Operations cho tình huống dựa trên nguồn lực/hàng không nhập kho, triển khai Lite - từ thỏa thuận đến lập hóa đơn ước giá và Project Operations cho tình huống dựa trên hàng trữ kho/sản xuất_

Bài viết này mô tả các tính năng đã bị xóa hoặc được lên kế hoạch xóa khỏi Dynamics 365 Project Operations.

- Tính năng *đã xóa* không còn khả dụng trong sản phẩm.
- Tính năng *không dùng nữa* không ở trong giai đoạn phát triển tích cực và có thể bị xóa khỏi bản cập nhật trong tương lai.

Danh sách này giúp bạn cân nhắc những tính năng cần xóa và không dùng nữa cho kế hoạch của riêng mình.

> [!NOTE]
> Thông tin chi tiết về các đối tượng trong ứng dụng Tài chính và Hoạt động có thể được tìm thấy trong [**Các báo cáo tham khảo kỹ thuật**](/dynamics/s-e/global/axtechrefrep_61). Bạn có thể so sánh các phiên bản khác nhau của các báo cáo này để tìm hiểu về các đối tượng đã thay đổi hoặc bị xóa trong mỗi phiên bản của ứng dụng Tài chính và Hoạt động.

## <a name="features-removed-or-deprecated-in-the-project-operations-march-2022-release"></a>Các tính năng bị xóa hoặc không được dùng nữa trong bản phát hành Project Operations vào tháng 3 năm 2022

### <a name="project-management-and-accounting-always-create-adjustment-transaction-parameter"></a>Quản lý dự án và kế toán Tham số "Luôn tạo giao dịch điều chỉnh"

| &nbsp; | &nbsp; |
|--------|--------|
| **Lý do không dùng nữa/xóa** | Các giao dịch điều chỉnh là bắt buộc cho các mục đích kiểm toán. Sau khi không dùng nữa, thông số này sẽ bị ẩn. Hệ thống sẽ luôn tạo các giao dịch điều chỉnh, giống như hiện tại khi thông số được đặt thành **Đúng**. |
| **Được thay thế bởi một tính năng khác?** | No |
| **Lĩnh vực sản phẩm bị ảnh hưởng** | Ứng dụng |
| **Tùy chọn triển khai** | Hoạt động dự án cho các kịch bản sản xuất / tồn kho |
| **Trạng thái** | Không dùng nữa: Đến ngày 1 tháng 3 năm 2023, chúng tôi sẽ ẩn thông số và thay đổi hành vi hệ thống để các giao dịch điều chỉnh luôn được tạo. |

### <a name="project-management-and-accounting-use-adjustment-date-as-new-project-date-parameter"></a>Quản lý dự án và kế toán tham số "Sử dụng ngày điều chỉnh làm ngày dự án mới"

| &nbsp; | &nbsp; |
|--------|--------|
| **Lý do không dùng nữa/xóa** | Thông số này ban đầu được sử dụng để cho phép điều chỉnh khi kỳ tài chính bị đóng. Tuy nhiên, nó không còn bắt buộc nữa, vì ngày kế toán của giao dịch có thể được thay đổi thành ngày đầu tiên của khoảng thời gian mở, nếu nó được định cấu hình. Ngày của dự án không được thay đổi, vì nó đại diện cho ngày mà giao dịch xảy ra. |
| **Được thay thế bởi một tính năng khác?** | No |
| **Lĩnh vực sản phẩm bị ảnh hưởng** | Ứng dụng |
| **Tùy chọn triển khai** | Hoạt động dự án cho các kịch bản sản xuất / tồn kho |
| **Trạng thái** | Không dùng nữa: Đến ngày 1 tháng 3 năm 2023, chúng tôi sẽ ẩn tham số và thay đổi hành vi hệ thống để ngày dự án không bao giờ bị thay đổi khi điều chỉnh. |

### <a name="resource-request-workflow-in-project-operations-for-stockedproduction-based-scenarios"></a>Quy trình công việc yêu cầu tài nguyên trong Hoạt động dự án cho các tình huống có hàng / dựa trên sản xuất

| &nbsp; | &nbsp; |
|--------|--------|
| **Lý do không dùng nữa/xóa** | Không được chấp nhận vì hạn chế về số lượng sử dụng và giao dịch thấp. |
| **Được thay thế bởi một tính năng khác?** | No |
| **Lĩnh vực sản phẩm bị ảnh hưởng** | Ứng dụng |
| **Tùy chọn triển khai** | Hoạt động dự án cho các kịch bản sản xuất / tồn kho |
| **Trạng thái** | Không được chấp nhận: Trước ngày 1 tháng 3 năm 2023, chúng tôi sẽ vô hiệu hóa tùy chọn yêu cầu tài nguyên cho dự án bằng cách sử dụng quy trình làm việc. |

### <a name="project-invoice-proposal-page-without-header-and-lines-views"></a>Trang đề xuất hóa đơn dự án không có chế độ xem Tiêu đề và Dòng

| &nbsp; | &nbsp; |
|--------|--------|
| **Lý do không dùng nữa/xóa** | Không được chấp nhận vì những cải tiến đối với trang đã được giới thiệu cùng với **Sử dụng đề xuất hóa đơn Dự án và các biểu mẫu nhật ký hóa đơn với chế độ xem Header và Lines** phím tính năng. |
| **Được thay thế bởi một tính năng khác?** | Có |
| **Lĩnh vực sản phẩm bị ảnh hưởng** | Ứng dụng |
| **Tùy chọn triển khai** | Điều hành dự án cho các kịch bản sản xuất / tồn kho; Hoạt động dự án cho các tình huống tài nguyên / không có hàng |
| **Trạng thái** | Không được dùng nữa: Trước ngày 1 tháng 3 năm 2023, chúng tôi sẽ tắt trang cũ hơn (cũ hơn) và bật **Sử dụng đề xuất hóa đơn Dự án và các biểu mẫu nhật ký hóa đơn với chế độ xem Đầu trang và Dòng** phím tính năng theo mặc định. |

## <a name="features-removed-or-deprecated-in-the-project-operations-december-2021-release"></a>Các tính năng đã bị xóa hoặc không dùng nữa trong bản phát hành Project Operations vào tháng 12 năm 2021

### <a name="collaboration-workspaces"></a>Không gian làm việc cộng tác

[Tạo hoặc liên kết đến không gian làm việc cộng tác (Dự án)](/dynamicsax-2012/appuser-itpro/create-or-link-to-a-collaboration-workspace-project)

| &nbsp; | &nbsp; |
|--------|--------|
| **Lý do không dùng nữa/xóa** | Không được chấp nhận do mức sử dụng thấp. Khách hàng sử dụng Hoạt động dự án cho các tình huống tài nguyên / không có hàng có thể tận dụng [Cộng tác với các Nhóm văn phòng](../project-management/collaboration-groups.md). |
| **Được thay thế bởi một tính năng khác?** | No |
| **Lĩnh vực sản phẩm bị ảnh hưởng** | Ứng dụng  |
| **Tùy chọn triển khai** | Hoạt động dự án cho các kịch bản sản xuất / tồn kho |
| **Trạng thái** | Không dùng nữa: Trước ngày 1 tháng 12 năm 2022, chúng tôi dự định sẽ không hỗ trợ không gian làm việc Cộng tác nữa. |
