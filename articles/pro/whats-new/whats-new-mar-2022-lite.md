---
title: Có gì mới Tháng 3 năm 2022 - Triển khai Project Operations Lite
description: Chủ đề này cung cấp thông tin về các bản cập nhật chất lượng có sẵn trong bản triển khai Project Operations lite tháng 3 năm 2022.
author: sigitac
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8a83491da1d312406dfb36f5ad214c307c15cfbf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583776"
---
# <a name="whats-new-march-2022---project-operations-lite-deployment"></a>Có gì mới Tháng 3 năm 2022 - Triển khai Project Operations Lite

_Áp dụng cho: Bản triển khai giản đơn - từ thỏa thuận đến lập hóa đơn ước giá_

Chủ đề này áp dụng cho các thành phần và phiên bản sau của Microsoft Dynamics 365 Project Operations:

- Hoạt động dự án trong một Dataverse phiên bản môi trường 4.30.0.99

## <a name="features-included-in-this-release"></a>Các tính năng có trong bản phát hành này

- Hợp đồng phụ: Tạo hóa đơn của nhà cung cấp và trải nghiệm đối sánh

## <a name="quality-updates"></a>Bản cập nhật chất lượng

| Lĩnh vực tính năng | Số tham chiếu | Cập nhật chất lượng |
| --- | --- | --- |
| Thời gian và chi phí | 2388011 | Hiển thị nhận xét từ chối cho những người gửi mục nhập thời gian trong quá trình phê duyệt hàng loạt. |
| Hoạch định và theo dõi dự án | 2495294 | Không thể chỉnh sửa chi tiết dự án trên **Chi tiết công việc** trang. |
| Định giá và thanh toán | 2499605 | Các mốc hợp đồng được tạo từ các mốc báo giá được đánh dấu không chính xác là chỉ đọc. |
| Hoạch định và theo dõi dự án | 2506050 | Tập hợp hoạt động vẫn chờ xử lý trong một giờ nếu không có thay đổi nào để lưu. Tập hợp này sau đó được đánh dấu sai là **Thất bại**, trong khi nó phải được hoàn thành ngay lập tức. |
| Định giá và thanh toán | 2507401 | Các đơn vị hợp đồng mặc định được nhập không chính xác vào các dự án do bộ nhớ đệm không chính xác. |
| Định giá và thanh toán | 2541660 | **Xác thực việc tạo đơn hàng bán hàng** trong tính năng ghi kép chỉ dành cho các đơn đặt hàng dựa trên dự án. |
| Định giá và thanh toán | 2552745 | Thuế không được phân chia giữa những khách hàng đã thiết lập các quy tắc thanh toán riêng lẻ. |
| Định giá và thanh toán | 2558859 | Thông báo lỗi được cải thiện khi thiết lập thứ nguyên đặt giá. |
| Định giá và thanh toán | 2558933 | **Nhập từ Dự toán Dự án** thất bại khi **msdyn\_ dự định** được thêm vào làm thứ nguyên định giá. |
| Định giá và thanh toán | 2559101 | Việc xóa thông số dự án không bị chặn và gây ra sự cố. |
|   Quản lý cơ hội | 2570390 | Trình cắm ghi kép buộc loại tài khoản dựa trên báo giá, đơn đặt hàng và cơ hội **Khách hàng**, ngay cả khi loại tài khoản đó không chính xác. |
| Định giá và thanh toán | 2586097 | Các thực tế về chi phí được lập hóa đơn chia nhỏ không bị đảo ngược khi một dự án bị xóa khỏi dòng hợp đồng dự án. |
| Định giá và thanh toán | 2589619 | Thuế đối với tài liệu ghi vào được tuyên truyền đến các thực tế bán hàng chưa lập hóa đơn và hóa đơn. |
|   Quản lý cơ hội | 2594015 | Một báo giá không thể được đóng là giành cho những khách hàng có **Net60** điều khoản thanh toán. |
| Hoạch định và theo dõi dự án | 2595841 | Trong Dự án cho Web, người dùng nhận được thông báo lỗi về việc thiếu **msdyn\_ bắt đầu thực tế** khi họ tạo một yêu cầu tài nguyên mới. |
| Thời gian và Chi phí | 2602511 | Các **Bị từ chối bởi** trường cho các mục thời gian hiển thị **Hệ thống** thay vì một người dùng được đặt tên làm người từ chối. |
| Thời gian và Chi phí | 2602528 | Người phê duyệt dự án có thể phê duyệt thời gian cho các dự án mà họ không được liệt kê là người phê duyệt. |
| Định giá và thanh toán | 2608550 | Hóa đơn sửa chữa có thể được xác nhận ngay cả khi không có thay đổi so với bản gốc. |

## <a name="removed-and-deprecated-features"></a>Các tính năng đã bị xóa và không dùng nữa

Các [Các tính năng bị xóa hoặc không dùng nữa trong Hoạt động dự án](../../whats-new/removed-depreciated-features-project.md) chủ đề mô tả các tính năng đã bị xóa hoặc không được dùng nữa Dynamics 365 Project Operations.

- Tính năng đã xóa không còn khả dụng trong sản phẩm.
- Một tính năng không dùng nữa không được phát triển tích cực và có thể bị xóa trong bản cập nhật trong tương lai.

Thông báo ngừng sử dụng sẽ xuất hiện trong [Các tính năng bị xóa hoặc không dùng nữa trong Hoạt động dự án](../../whats-new/removed-depreciated-features-project.md) chủ đề 12 tháng trước khi bất kỳ tính năng nào bị xóa khỏi sản phẩm.
