---
title: Kết nối giao dịch - Liên kết các thực tế của các loại giao dịch khác nhau
description: Chủ đề này giải thích cách kết nối giao dịch được sử dụng để liên kết các thực tế thuộc các loại khác nhau nhằm giúp theo dõi khả năng sinh lời, tồn đọng thanh toán và tính toán doanh thu đã lập hóa đơn so với chưa lập hóa đơn.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2e8d75a69e27619e6a21f0fe61e2c656e94017b0
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580804"
---
# <a name="transaction-connections---link-actuals-of-different-transaction-types"></a>Kết nối giao dịch - Liên kết các thực tế của các loại giao dịch khác nhau

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Bản ghi kết nối giao dịch được tạo để liên kết các loại thực tế khác nhau khi thời gian, chi phí hoặc việc sử dụng vật liệu di chuyển trong vòng đời của nó từ giai đoạn báo giá hoặc trước khi bán hàng sang giai đoạn hợp đồng, phê duyệt và / hoặc thu hồi, lập hóa đơn và có khả năng lập hóa đơn sửa chữa hoặc báo giá.

Ví dụ sau đây trình bày hoạt động xử lý thông thường các mục nhập thời gian trong vòng đời dự án Project Operations.

> ![Các mục thời gian xử lý trong Hoạt động dự án.](media/basic-guide-17.png)

Việc xử lý các mục thời gian trong vòng đời dự án Hoạt động Dự án tuân theo các bước sau: 

1. Việc nộp một mục nhập thời gian sẽ tạo ra hai dòng nhật ký: một dòng cho chi phí và một cho doanh thu chưa lập hóa đơn. 
2. Sự chấp thuận cuối cùng đối với mục nhập thời gian khiến hai thực tế được tạo ra: một cho chi phí và một cho doanh số bán hàng chưa lập hóa đơn. 2 thực tế này được liên kết bằng cách sử dụng các kết nối giao dịch.
3. Khi người dùng tạo một hóa đơn dự án, giao dịch dòng hóa đơn được tạo bằng cách sử dụng dữ liệu từ thực tế doanh số chưa lập hóa đơn.
4. Khi hóa đơn được xác nhận, điều này sẽ tạo ra hai thực tế mới: một khoản hoàn nhập bán hàng chưa lập hóa đơn và một khoản bán hàng thực tế đã lập hóa đơn. Việc hoàn nhập doanh số bán hàng chưa lập hóa đơn và doanh số bán hàng thực tế chưa lập hóa đơn ban đầu được kết nối với nhau bằng cách sử dụng các kết nối giao dịch đảo chiều. Doanh số bán hàng đã lập hóa đơn và các tài liệu hướng dẫn bán hàng chưa lập hóa đơn ban đầu cũng được kết nối để hiển thị mối liên hệ giữa doanh thu đã từng tồn đọng hoặc doanh thu đang làm dở (WIP) với doanh thu hiện được lập hóa đơn.   

Mỗi sự kiện trong quy trình xử lý sẽ kích hoạt việc tạo các bản ghi trong **Kết nối giao dịch** bàn. Điều này giúp xây dựng dấu vết về mối quan hệ giữa các bản ghi được tạo qua mục nhập thời gian, dòng nhật ký, thực tế và chi tiết dòng hóa đơn.

Bảng sau đây cho thấy các bản ghi trong **Kết nối giao dịch** thực thể cho quy trình công việc trước đó.

|Sự kiện                   |Giao dịch 1                 |Vai trò giao dịch 1 |Loại giao dịch 1       |Giao dịch 2          |Vai trò giao dịch 2 |Loại giao dịch 2 |
|------------------------|------------------------------|---------------|-----------------------------|-----------------------------|-------------------|-------------------|
|Gửi mục nhập thời gian   |GUID dòng nhật ký kế toán (doanh số)     |Doanh số chưa lập hóa đơn |msdyn_journalline            |GUID dòng nhật ký kế toán (chi phí)     |Chi phí            |msdyn_journalline  |
|Phê duyệt thời gian           |GUID thực tế chưa lập hóa đơn mới (Doanh số)  |Bán hàng Chưa lập hóa đơn |msdyn_actual                 |GUID thực tế chi phí (chi phí)       |Chi phí            |msdyn_actual       |
|Tạo hóa đơn        |GUID chi tiết dòng hóa đơn      |Bán hàng Đã lập hóa đơn   |msdyn_invoicelinetransaction |GUID thực tế doanh số chưa lập hóa đơn   |Doanh số chưa lập hóa đơn  |msdyn_actual       |
|Thông tin hóa đơn    |GUID thực tế đảo ngược         |Đảo ngược      |msdyn_actual                 |GUID doanh số chưa lập hóa đơn gốc |Gốc        |msdyn_actual       |
|                        |GUID doanh số đã lập hóa đơn             |Doanh số đã lập hóa đơn   |msdyn_actual                 |GUID thực tế doanh số chưa lập hóa đơn   |Doanh số chưa lập hóa đơn  |msdyn_actual       |
|Chỉn sửa hóa đơn nháp |GUID giao dịch dòng hóa đơn|Thay thế      |msdyn_invoicelinetransaction |GUID doanh số đã lập hóa đơn            |Gốc        |msdyn_actual       |
|Xác nhận sửa hóa đơn|GUID đảo ngược doanh số đã lập hóa đơn  |Đảo ngược      |msdyn_actual                 |GUID doanh số đã lập hóa đơn            |Gốc        |msdyn_actual       |
|                        |HƯỚNG DẪN Bán Hàng Chưa Lập Hóa Đơn Mới |Thay thế            |msdyn_actual                 |GUID doanh số đã lập hóa đơn            |Gốc        |msdyn_actual       |


Hình minh họa sau đây cho thấy các liên kết được tạo ra giữa các loại thực tế khác nhau tại các sự kiện khác nhau bằng cách sử dụng ví dụ về các mục thời gian trong Hoạt động dự án.

> ![Các thực tế thuộc các loại khác nhau được liên kết với nhau như thế nào trong Hoạt động Dự án.](media/TransactionConnections.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
