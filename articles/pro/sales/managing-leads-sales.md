---
title: Quản lý khách hàng tiềm năng (Dự án)
description: Chủ đề này cung cấp thông tin về quản lý khách hàng tiềm năng dựa trên dự án (dự án).
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 005e36811643b0b1e98a686792cf39125ae97949
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896352"
---
# <a name="manage-leads-pro"></a>Quản lý khách hàng tiềm năng (Dự án)

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Các khách hàng tiềm năng dựa trên dự án có thể được quản lý và định tính trong Project Operations. Quá trình quản lý khách hàng tiềm năng bao gồm việc tạo ra các khách hàng tiềm năng dựa trên công việc và định tính các khách hàng tiềm năng đó. 

## <a name="list-of-project-sales-leads"></a>Danh sách mối khách hàng dự án

Trong phần **Bán hàng**, trong ngăn điều hướng bên trái, hãy mở trang danh sách **Khách hàng tiềm năng** để xem danh sách tất cả các bản ghi khách hàng tiềm năng trong hệ thống. Danh sách khách hàng tiềm năng được hiển thị dựa trên công việc và bạn có thể tạo các loại khách hàng tiềm năng khác nếu bạn cũng có các ứng dụng Dynamics 365 Sales hoặc Dynamics 365 Field Service.

Bạn có thể tạo chế độ đã lọc để chỉ xem các khách hàng tiềm năng dựa trên dự án bằng cách tạo bộ lọc trên giá trị **Loại**. Ví dụ: bạn có thể chọn chỉ hiển thị khách hàng tiềm năng dựa trên công việc.

## <a name="creating-a-new-lead-for-a-project-based-deal"></a>Tạo khách hàng tiềm năng mới cho thỏa thuận dựa trên dự án

Khi khách hàng tiềm năng dựa trên dự án đủ điều kiện, cơ hội và tài khoản sẽ được tạo. Cơ hội dựa trên dự án là điểm khởi đầu cho các hoạt động theo đuổi doanh số trong giai đoạn Cơ hội. Các cơ hội dựa trên dự án có các khả năng độc đáo cần phải có để bán công việc của dự án. Những khả năng này bao gồm:

- Phương thức thanh toán cho Giá cố định, vật tư và thời gian
- Bảng giá có hiệu lực nhiều ngày cho nhân lực, chi phí và vật tư phát sinh cho các dự án.

Để khách hàng tiềm năng đủ điều kiện tự động tạo cơ hội, hãy đặt thuộc tính **Loại** thành **Dựa trên công việc** khi bạn tạo khách hàng tiềm năng. Nếu bạn chọn một loại khác, khách hàng tiềm năng sẽ không tạo cơ hội dựa trên dự án khi đủ điều kiện. Nếu cơ hội dựa trên dự án không được tạo, các khả năng dành riêng cho dự án sẽ không khả dụng trong quy trình bán hàng xuôi tuyến.

Bảng sau đây bao gồm thông tin trường quan trọng cho khách hàng tiềm năng và các tác động xuôi tuyến của những trường đó.

| **Trường** | **Vị trí** | **Mức độ liên quan, mục đích và hướng dẫn** | **Tác động xuôi tuyến** |
| --- | --- | --- | --- |
| Chủ đề | Tab tổng quát | Trường văn bản này phải chứa mô tả ngắn gọn về thỏa thuận. | Chủ đề của khách hàng tiềm năng sẽ được mặc định là chủ đề của Cơ hội, Tên báo giá và Hợp đồng dự án. |
| Loại | Tab tổng quát | Trường bộ tùy chọn này có các tùy chọn sau:</br>- Dựa trên công việc (chỉ khả dụng khi Project Operations được cài đặt)</br>- Dựa trên mục (chỉ khả dụng khi Project Operations và Sales được cài đặt)</br>- Dựa trên bảo trì dịch vụ (khả dụng khi Field Service được cài đặt) | Khi giá trị của trường này được đặt thành **Dựa trên công việc** trên khách hàng tiềm năng, khách hàng tiềm năng đủ điều kiện để tạo Cơ hội dựa trên dự án. Cần có cơ hội dựa trên dự án để kích hoạt tất cả các tiện ích và chức năng dành riêng cho dự án trong quy trình bán hàng xuôi tuyến cho thỏa thuận này. |
| Tên | Tab tổng quát | Tên người liên hệ của khách hàng triển vọng | Khi khách hàng tiềm năng đủ điều kiện, thì tài khoản, người liên hệ và cơ hội sẽ được tạo. Tên của người liên hệ là giá trị được đặt ở đây. |
| Họ | Tab tổng quát | Họ của người liên hệ của khách hàng triển vọng | Khi khách hàng tiềm năng đủ điều kiện, thì tài khoản, người liên hệ và cơ hội sẽ được tạo. Họ của người liên hệ là giá trị được đặt ở đây. |
| Công ty | Tab tổng quát | Tên công ty của khách hàng triển vọng | Khi khách hàng tiềm năng đủ điều kiện, thì tài khoản, người liên hệ và cơ hội sẽ được tạo. Tên của tài khoản đã tạo là giá trị được đặt ở đây. |
| Tiền tệ | Tab Chi tiết | Đơn vị tiền tệ của khách hàng triển vọng | Khi khách hàng tiềm năng đủ điều kiện, thì tài khoản, người liên hệ và cơ hội sẽ được tạo. Đơn vị tiền tệ của tài khoản đã tạo là giá trị được đặt ở đây. |

## <a name="qualify-a-new-project-based-lead"></a>Định tính khách hàng tiềm năng mới dựa trên dự án

Khách hàng tiềm năng có giá trị **Loại** được đặt thành **Dựa trên công việc** được gọi là khách hàng tiềm năng dựa trên dự án. Khi khách hàng tiềm năng dựa trên dự án đủ điều kiện, những nội dung sau sẽ được tạo:

- Tài khoản sử dụng trường **Công ty** từ khách hàng tiềm năng.
- Bản ghi người liên hệ được liên kết với tài khoản dựa trên các giá trị trong các trường **Tên** và **Họ** trên khách hàng tiềm năng.
- Cơ hội dựa trên dự án có trường **Loại** đặt thành &quot;**Dựa trên công việc**.

Để biết thêm thông tin chi tiết về khách hàng tiềm năng đủ điều kiện, hãy xem[Định tính hoặc chuyển đổi khách hàng tiềm năng](https://docs.microsoft.com/dynamics365/sales-enterprise/qualify-lead-convert-opportunity-sales).

## <a name="business-process-flow-for-project-based-deals"></a>Dòng quy trình công việc cho các thỏa thuận dựa trên dự án

Các dòng quy trình công việc sau được hỗ trợ cho những thỏa thuận dựa trên dự án trong Project Operations:

- Quy trình công việc từ khách hàng tiềm năng thành cơ hội
- Quy trình bán hàng từ cơ hội

Quy trình công việc từ khách hàng tiềm năng thành cơ hội hỗ trợ các giai đoạn sau:

| Tên giai đoạn | Thực thể được ánh xạ | Chức năng |
| --- | --- | --- |
| Bao gồm | Khách hàng tiềm năng | Định tính khách hàng tiềm năng để tạo tài khoản, người liên hệ và cơ hội. |
| Phát triển | Cơ hội | Tạo cơ hội để bổ sung thêm thông tin về công việc liên quan, các bên liên quan chính và đối thủ cạnh tranh. |
| Đề xuất | Cơ hội | Xây dựng đề xuất và nhận sự phê duyệt của nhóm đánh giá nội bộ. |
| Đóng | Cơ hội | Giành được cơ hội để chốt thỏa thuận. |
