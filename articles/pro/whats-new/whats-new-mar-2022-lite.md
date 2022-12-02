---
title: Tính năng mới tháng 3 năm 2022 - triển khai Project Operations lite
description: Bài viết này cung cấp thông tin về các bản cập nhật chất lượng có trong bản phát hành triển khai bản đơn giản Project Operations vào tháng 3 năm 2022.
author: sigitac
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 321d59568bfd33bb00a1500afe514fbecf9a0250
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934254"
---
# <a name="whats-new-march-2022---project-operations-lite-deployment"></a>Tính năng mới tháng 3 năm 2022 - triển khai Project Operations lite

_Áp dụng cho: Bản triển khai giản đơn - từ thỏa thuận đến lập hóa đơn ước giá_

Bài viết này áp dụng cho các phiên bản và thành phần sau của Microsoft Dynamics 365 Project Operations:

- Project Operations trong môi trường Dataverse phiên bản 4.30.0.99

## <a name="features-included-in-this-release"></a>Các tính năng có trong bản phát hành này

- Hợp đồng phụ: Tạo hóa đơn của nhà cung cấp và trải nghiệm so khớp

## <a name="quality-updates"></a>Bản cập nhật chất lượng

| Lĩnh vực tính năng | Số tham chiếu | Cập nhật chất lượng |
| --- | --- | --- |
| Thời gian và chi phí | 2388011 | Hiển thị nhận xét từ chối cho những người gửi mục nhập thời gian trong quá trình phê duyệt hàng loạt. |
| Hoạch định và theo dõi dự án | 2495294 | Không thể chỉnh sửa chi tiết dự án trên trang **Chi tiết công việc**. |
| Định giá và thanh toán | 2499605 | Các mốc hợp đồng được tạo từ các mốc báo giá được đánh dấu không chính xác là chỉ đọc. |
| Hoạch định và theo dõi dự án | 2506050 | Bộ thao tác vẫn chờ xử lý trong một giờ nếu không có thay đổi nào để lưu. Bộ này sau đó được đánh dấu sai là **Không thành công**, trong khi nó phải được hoàn thành ngay lập tức. |
| Định giá và thanh toán | 2507401 | Các đơn vị hợp đồng mặc định được nhập không chính xác vào các dự án do bộ nhớ đệm không chính xác. |
| Định giá và thanh toán | 2541660 | **Xác thực việc tạo đơn bán hàng** trong tính năng ghi kép chỉ dành cho các đơn hàng dựa trên dự án. |
| Định giá và thanh toán | 2552745 | Thuế không được phân chia giữa những khách hàng đã thiết lập các quy tắc thanh toán riêng. |
| Định giá và thanh toán | 2558859 | Thông báo lỗi được cải thiện khi các thứ nguyên giá được thiết lập. |
| Định giá và thanh toán | 2558933 | **Nhập từ ước tính dự báo** thất bại khi **msdyn\_project** được thêm làm thứ nguyên giá. |
| Định giá và thanh toán | 2559101 | Việc xóa tham số dự án không bị chặn và gây ra sự cố. |
|   Quản lý cơ hội | 2570390 | Phần bổ trợ ghi kép buộc loại tài khoản dựa trên báo giá, đơn hàng và cơ hội là **Khách hàng**, ngay cả khi loại tài khoản đó không chính xác. |
| Định giá và thanh toán | 2586097 | Các chi phí thực tế được lập hóa đơn chia nhỏ không bị đảo ngược khi một dự án bị xóa khỏi mô tả hợp đồng dự án. |
| Định giá và thanh toán | 2589619 | Thuế vật tư chọn thêm được truyền vào doanh số chưa lập hóa đơn thực tế và hóa đơn. |
|   Quản lý cơ hội | 2594015 | Không thể đóng báo giá là đã chốt cho khách hàng có điều khoản thanh toán **Net60**. |
| Hoạch định và theo dõi dự án | 2595841 | Trong Project for the Web, người dùng nhận được thông báo lỗi về **msdyn\_actualstart** còn thiếu khi tạo yêu cầu nguồn lực mới. |
| Thời gian và Chi phí | 2602511 | Trường **Người từ chối** cho mục nhập thời gian hiển thị **Hệ thống** thay vì người dùng được đặt tên làm người từ chối. |
| Thời gian và Chi phí | 2602528 | Người phê duyệt dự án có thể phê duyệt thời gian cho các dự án mà họ không được liệt kê là người phê duyệt. |
| Định giá và thanh toán | 2608550 | Hóa đơn điều chỉnh có thể được xác nhận ngay cả khi không có thay đổi so với bản gốc. |

## <a name="removed-and-deprecated-features"></a>Các tính năng bị xóa và không dùng nữa

Bài viết [Các tính năng bị xóa hoặc không dùng nữa trong Project Operations](../../whats-new/removed-depreciated-features-project.md) mô tả các tính năng đã bị xóa hoặc không được dùng nữa đối với Dynamics 365 Project Operations.

- Tính năng đã xóa không còn khả dụng trong sản phẩm.
- Tính năng không dùng nữa không ở trong giai đoạn phát triển và có thể bị xóa khỏi bản cập nhật trong tương lai.

Thông báo không dùng nữa sẽ xuất hiện trong bài viết [Các tính năng bị xóa hoặc không dùng nữa trong Project Operations](../../whats-new/removed-depreciated-features-project.md) 12 tháng trước khi bất kỳ tính năng nào bị xóa khỏi sản phẩm.
