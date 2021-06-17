---
title: Thông tin tóm tắt về báo giá dự án - bản đơn giản
description: Chủ đề này cung cấp thông tin về thông tin và cài đặt áp dụng và tác động đến báo giá dự án. (Sales)
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ad549513c70ccf935e4dfdc17123be09ad737c02
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994342"
---
# <a name="header-details-for-project-quotes"></a>Chi tiết của tiêu đề cho các báo giá dự án

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Bài viết này giải thích thông tin áp dụng cho báo giá dự án. Điều này bao gồm các cài đặt ảnh hưởng đến tất cả các mô tả báo giá và thông tin về báo giá được tóm tắt trên tất cả các mục hàng để thúc đẩy KPI của báo giá dự án.

Bảng sau liệt kê các trường thông tin tóm tắt trên báo giá dự án dành riêng cho Dynamics 365 Project Operations hoặc có một số thay đổi quan trọng trong hoạt động so với báo giá trong Dynamics 365 Sales.

| **Trường** | **Vị trí** | **Mô tả** | **Tác động xuôi tuyến** |
| --- | --- | --- | --- |
| Loại | Tab Tóm tắt (ẩn) | Trường bộ tùy chọn này có các tùy chọn sau:</br>- Dựa trên công việc (chỉ khả dụng khi Project Operations được cài đặt)</br>- Dựa trên mục (chỉ khả dụng khi Project Operations và Sales được cài đặt)</br>- Dựa trên bảo trì dịch vụ (có sẵn khi Dynamics 365 Field Service được cài đặt) | Khi bạn sử dụng ứng dụng Project Operations, giá trị của trường này tự động được đặt thành **Dựa trên công việc**. Điều này phân loại báo giá là báo giá dựa trên dự án. Báo giá phải dựa trên dự án để kích hoạt tất cả các tiện ích và chức năng dành riêng cho dự án. |
| Khách hàng Tiềm năng | Tab Tóm tắt | Tham chiếu đến bản ghi công ty hoặc tài khoản của khách hàng. Khi báo giá tạo từ một cơ hội, trường này được sao chép từ trường tương ứng trên mục cơ hội. | Đơn vị tiền tệ trên báo giá dự án được mặc định dựa trên đơn vị tiền tệ của khách hàng. Tuy nhiên, có thể thay đổi đơn vị tiền tệ trước khi lưu báo giá. |
| Người quản lý khách hàng | Tab Tóm tắt | Tên của Người quản lý tài khoản cho thỏa thuận này. Khi báo giá tạo từ một cơ hội, trường này được sao chép từ trường tương ứng trên mục cơ hội. | Người quản lý tài khoản chịu trách nhiệm quản lý mối quan hệ với khách hàng thông qua việc hoàn thành dự án này. Dựa trên bản ghi tài nguyên có thể đặt trước liên kết với Người quản lý tài khoản, đơn vị ký hợp đồng mặc định trên báo giá dự án. |
| Đơn vị Hợp đồng | Tab Tóm tắt | Đơn vị tổ chức chịu trách nhiệm bàn giao dự án hoặc các dự án liên quan đến báo giá này. Khi báo giá tạo từ một cơ hội, trường này được sao chép từ trường tương ứng trên mục cơ hội. | Đơn vị ký hợp đồng là bộ phận của công ty sẽ thực hiện các dự án sau khi thỏa thuận được chốt. Mỗi đơn vị ký hợp đồng đều có một loại tiền tệ và đơn vị tiền tệ này được sử dụng để báo cáo chi phí ước tính và thực tế phát sinh trong quá trình thực hiện dự án. |
| Bảng giá sản phẩm | Tab Tóm tắt | Đây là bảng giá dùng làm giá mặc định cho các mô tả báo giá theo sản phẩm. Danh sách các tùy chọn cho trường này hiển thị danh sách các bảng giá trong đó đơn vị tiền tệ của bảng giá khớp với đơn vị tiền tệ trên báo giá. Khi báo giá tạo từ một cơ hội, trường này được sao chép từ trường tương ứng trên mục cơ hội. Trường này trên mục cơ hội được mặc định từ bản ghi tài khoản nhưng có thể thay đổi. | Khi báo giá được chốt, giá trị trường được sao chép sang hợp động dự án được tạo. |
| Tiền tệ | Tab Tóm tắt | Điều này cho biết đơn vị tiền tệ sẽ được sử dụng để báo cáo giá trị của thỏa thuận này. Đây cũng là đơn vị tiền tệ mà khách hàng sẽ được lập hóa đơn nếu thỏa thuận được chốt. Khi báo giá tạo từ một cơ hội, trường này được sao chép từ trường tương ứng trên mục cơ hội. Trường này trên mục cơ hội mặc định từ bản ghi tài khoản nhưng người dùng có thể thay đổi. | Sau khi báo giá được lưu, trường này không chỉnh sửa được nữa. Mục này được dùng để mặc định bảng giá sản phẩm và dự án trên báo giá. Đơn vị tiền trên báo giá được dùng để khớp với đơn vị tiền tệ trên bảng giá. |
| Giới hạn không vượt quá | Tab Tóm tắt | Điều này cho biết giới hạn đã thương lượng về giá trị cuối cùng mà khách hàng đồng ý cho thỏa thuận này. | Giới hạn này được đánh giá trong quá trình thực hiện và có thể áp dụng cho tất cả các mục mô tả và dự án liên quan đến thỏa thuận này. |
| Ngày bàn giao được yêu cầu | Tab Tóm tắt | Khi báo giá tạo từ một cơ hội, trường này được sao chép từ trường tương ứng trên mục cơ hội. | Ngày này được sử dụng làm ngày kết thúc để tạo lịch trình hóa đơn. |

Dưới đây là các tab và KPI có sẵn trên báo giá dự án dành riêng cho Project Operations hoặc có một số thay đổi quan trọng trong hành vi từ báo giá Bán hàng:

| **Trường** | **Vị trí** | **Mô tả** |
| --- | --- | --- |
| Phân tích suất sinh lợi | Tab trên Báo giá | Tab hiển thị các số liệu sau đây:</br>- Tổng chi phí có thể tính phí</br></br>- Tổng chi phí không thể tính phí</br>- Tổng doanh thu</br>- Tổng doanh thu (gốc)</br>- Lãi gộp</br>- Lãi gộp đã điều chỉnh|
| So sánh với Kỳ vọng của Khách hàng | Tab trên Báo giá | Tab này hiển thị các số liệu sau đây:</br>- Hoàn thành ước tính</br>- Hoàn thành đã yêu cầu</br>- Ngân sách khách hàng</br>- Giá trị báo giá |
| Phân tích báo giá | Tab trên Báo giá | Tab này tóm tắt các KPI hàng đầu sau đây cho báo giá dự án</br>- So sánh với kỳ vọng của khách hàng về ngân sách và lịch trình</br>- Lãi gộp</br>- Lãi gộp đã điều chỉnh |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
