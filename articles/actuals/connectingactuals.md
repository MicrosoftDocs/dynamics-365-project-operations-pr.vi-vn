---
title: Kết nối giao dịch – Liên kết số liệu thực tế của các loại giao dịch khác nhau
description: Bài viết này giải thích cách kết nối giao dịch được sử dụng để liên kết số liệu thực tế thuộc các loại khác nhau nhằm giúp theo dõi khả năng sinh lời, tồn đọng lập hóa đơn và các phép tính doanh thu đã lập hóa đơn so với chưa lập hóa đơn.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 19a78336099f54c5d6b36a963a90b9fd77e3d0af
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926112"
---
# <a name="transaction-connections---link-actuals-of-different-transaction-types"></a>Kết nối giao dịch – Liên kết số liệu thực tế của các loại giao dịch khác nhau

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Bản ghi kết nối giao dịch được tạo để liên kết các số liệu thực tế thuộc các loại khác nhau khi thời gian, chi phí hoặc việc sử dụng vật tư di chuyển trong chu kỳ của nó từ giai đoạn báo giá hoặc trước bán hàng sang giai đoạn hợp đồng, phê duyệt và/hoặc thu hồi, lập hóa đơn và có thể là lập hóa đơn tín dụng hoặc chỉnh sửa.

Ví dụ sau đây trình bày hoạt động xử lý thông thường các mục nhập thời gian trong vòng đời dự án Project Operations.

> ![Xử lý các mục nhập thời gian trong Project Operations.](media/basic-guide-17.png)

Hoạt động mục nhập thời gian trong chu kỳ dự án Project Operations làm theo các bước sau: 

1. Gửi một mục nhập thời gian sẽ tạo ra hai dòng nhật ký kế toán: một cho chi phí và một cho doanh số chưa lập hóa đơn. 
2. Việc phê duyệt mục nhập thời gian sẽ tạo ra hai thực tế: một cho chi phí và một cho doanh số chưa lập hóa đơn. 2 số liệu thực tế này được liên kết bằng các kết nối giao dịch.
3. Khi người dùng tạo một hóa đơn dự án, giao dịch dòng hóa đơn được tạo bằng cách sử dụng dữ liệu từ thực tế doanh số chưa lập hóa đơn.
4. Khi hóa đơn được xác nhận, điều này tạo hai số liệu thực tế mới: một đảo ngược doanh số chưa lập hóa đơn và thực tế doanh số đã lập hóa đơn. Đảo ngược doanh số chưa lập hóa đơn và thực tế doanh số chưa lập hóa đơn ban đầu được liên kết bằng các kết nối giao dịch đảo ngược. Doanh số đã lập hóa đơn và doanh số chưa lập hóa đơn thực tế ban đầu cũng được kết nối để thể hiện sự liên kết giữa doanh thu đã từng tồn đọng hoặc doanh thu đang xử lý (WIP) với doanh thu hiện đã được lập hóa đơn.   

Mỗi sự kiện trong dòng công việc xử lý sẽ kích hoạt việc tạo các bản ghi trong bảng **Kết nối giao dịch**. Điều này góp phần xây dựng mối quan hệ giữa các bản ghi được tạo qua mục nhập thời gian, dòng nhật ký kế toán, giá trị thực tế và chi tiết mô tả hóa đơn.

Bảng sau hiển thị các bản ghi trong thực thể **Kết nối giao dịch** cho dòng công việc trước đó.

|Sự kiện                   |Giao dịch 1                 |Vai trò giao dịch 1 |Loại giao dịch 1       |Giao dịch 2          |Vai trò giao dịch 2 |Loại giao dịch 2 |
|------------------------|------------------------------|---------------|-----------------------------|-----------------------------|-------------------|-------------------|
|Gửi mục nhập thời gian   |GUID dòng nhật ký kế toán (doanh số)     |Doanh số chưa lập hóa đơn |msdyn_journalline            |GUID dòng nhật ký kế toán (chi phí)     |Chi phí            |msdyn_journalline  |
|Phê duyệt thời gian           |GUID thực tế chưa lập hóa đơn mới (Doanh số)  |Bán hàng Chưa lập hóa đơn |msdyn_actual                 |GUID thực tế chi phí (chi phí)       |Chi phí            |msdyn_actual       |
|Tạo hóa đơn        |GUID chi tiết dòng hóa đơn      |Bán hàng Đã lập hóa đơn   |msdyn_invoicelinetransaction |GUID thực tế doanh số chưa lập hóa đơn   |Doanh số chưa lập hóa đơn  |msdyn_actual       |
|Thông tin hóa đơn    |GUID thực tế đảo ngược         |Đảo ngược      |msdyn_actual                 |GUID doanh số chưa lập hóa đơn gốc |Gốc        |msdyn_actual       |
|                        |GUID doanh số đã lập hóa đơn             |Doanh số đã lập hóa đơn   |msdyn_actual                 |GUID thực tế doanh số chưa lập hóa đơn   |Doanh số chưa lập hóa đơn  |msdyn_actual       |
|Chỉn sửa hóa đơn nháp |GUID giao dịch dòng hóa đơn|Thay thế      |msdyn_invoicelinetransaction |GUID doanh số đã lập hóa đơn            |Gốc        |msdyn_actual       |
|Xác nhận sửa hóa đơn|GUID đảo ngược doanh số đã lập hóa đơn  |Đảo ngược      |msdyn_actual                 |GUID doanh số đã lập hóa đơn            |Gốc        |msdyn_actual       |
|                        |GUID doanh số chưa lập hóa đơn mới |Thay thế            |msdyn_actual                 |GUID doanh số đã lập hóa đơn            |Gốc        |msdyn_actual       |


Hình minh họa sau đây cho thấy các liên kết được tạo ra giữa các loại số liệu thực tế khác nhau tại các sự kiện khác nhau bằng cách sử dụng ví dụ về mục nhập thời gian trong Project Operations.

> ![Cách số liệu thực tế thuộc các loại khác nhau được liên kết với nhau trong Project Operations.](media/TransactionConnections.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
