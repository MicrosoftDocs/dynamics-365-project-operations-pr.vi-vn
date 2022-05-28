---
title: Nguồn gốc giao dịch - Liên kết thực tế với nguồn của chúng
description: Chủ đề này giải thích cách sử dụng khái niệm nguồn gốc giao dịch để liên kết thực tế với bản ghi nguồn gốc, chẳng hạn như mục nhập thời gian, mục nhập chi phí hoặc nhật ký sử dụng vật liệu.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 908f78f7d58ec4b18f37d03b6fa7c4e2295491fa
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584852"
---
# <a name="transaction-origins---link-actuals-to-their-source"></a>Nguồn gốc giao dịch - Liên kết thực tế với nguồn của chúng

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Bản ghi nguồn gốc giao dịch được tạo để liên kết thực tế với nguồn của chúng, chẳng hạn như mục thời gian, mục chi phí, nhật ký sử dụng vật liệu và hóa đơn dự án.

Ví dụ sau đây trình bày hoạt động xử lý thông thường các mục nhập thời gian trong vòng đời dự án Project Operations.

> ![Thời gian xử lý phụ thuộc vào Hoạt động của Dự án.](media/basic-guide-17.png)
 
1. Việc nộp một mục nhập thời gian sẽ tạo ra hai dòng nhật ký: một dòng cho chi phí và một cho doanh thu chưa lập hóa đơn.
2. Sự chấp thuận cuối cùng đối với mục nhập thời gian khiến hai thực tế được tạo ra: một cho chi phí và một cho doanh số bán hàng chưa lập hóa đơn.
3. Khi người dùng tạo một hóa đơn dự án, giao dịch dòng hóa đơn được tạo bằng cách sử dụng dữ liệu từ thực tế doanh số chưa lập hóa đơn.
4. Khi hóa đơn được xác nhận, hai thực tế mới được tạo ra: một đảo ngược doanh số chưa lập hóa đơn và thực tế doanh số đã lập hóa đơn.

Mỗi sự kiện trong quy trình xử lý này sẽ kích hoạt việc tạo các bản ghi trong thực thể gốc Giao dịch để giúp xây dựng dấu vết về mối quan hệ giữa các bản ghi này được tạo qua mục nhập thời gian, dòng nhật ký, thực tế và chi tiết dòng hóa đơn.

Bảng sau hiển thị các bản ghi trong thực thể nguồn gốc giao dịch cho luồng công việc trước đó.

| Sự kiện                        | Nguồn gốc                   | Loại nguồn gốc                       | Giao dịch                       | Loại giao dịch         |
|------------------------------|--------------------------|-----------------------------------|-----------------------------------|--------------------------|
| Gửi mục nhập thời gian        | GUID bản ghi mục nhập thời gian   | Mục nhập Thời gian                        | GUID bản ghi dòng nhật ký kế toán (chi phí)   | Dòng Nhật ký Kế toán             |
| GUID bản ghi mục nhập thời gian       | Mục nhập Thời gian               | GUID bản ghi dòng nhật ký kế toán (doanh số)  | Dòng Nhật ký Kế toán                      |                          |
| Phê duyệt thời gian                | GUID bản ghi dòng nhật ký kế toán | Dòng Nhật ký Kế toán                      | GUID bản ghi doanh số chưa lập hóa đơn        | Thực tế                   |
| GUID bản ghi mục nhập thời gian       | Mục nhập Thời gian               | GUID bản ghi doanh số chưa lập hóa đơn        | Thực tế                            |                          |
| GUID bản ghi dòng nhật ký kế toán     | Dòng Nhật ký Kế toán             | GUID bản ghi thực tế chi phí           | Thực tế                            |                          |
| GUID bản ghi mục nhập thời gian       | Mục nhập Thời gian               | GUID bản ghi thực tế chi phí           | Thực tế                            |                          |
| Tạo hóa đơn             | GUID bản ghi mục nhập thời gian   | Mục nhập Thời gian                        | GUID giao dịch dòng hóa đơn     | Giao dịch dòng hóa đơn |
| GUID bản ghi dòng nhật ký kế toán     | Dòng Nhật ký Kế toán             | GUID giao dịch dòng hóa đơn     | Giao dịch dòng hóa đơn          |                          |
| Thông tin hóa đơn         | GUID dòng hóa đơn        | Mô tả Hóa đơn                      | GUID bản ghi doanh số đã lập hóa đơn          | Thực tế                   |
| GUID hóa đơn                 | Hóa đơn                  | GUID bản ghi doanh số đã lập hóa đơn          | Thực tế                            |                          |
| GUID chi tiết dòng hóa đơn     | Chi tiết Mô tả Hóa đơn      | GUID bản ghi doanh số đã lập hóa đơn          | Thực tế                            |                          |
| GUID bản ghi mục nhập thời gian       | Mục nhập Thời gian               | GUID bản ghi doanh số đã lập hóa đơn          | Thực tế                            |                          |
| GUID bản ghi dòng nhật ký kế toán     | Dòng Nhật ký Kế toán             | GUID bản ghi doanh số đã lập hóa đơn          | Thực tế                            |                          |
| GUID bản ghi mục nhập thời gian       | Mục nhập Thời gian               | GUID đảo ngược doanh số chưa lập hóa đơn      | Thực tế                            |                          |
| GUID bản ghi dòng nhật ký kế toán     | Dòng Nhật ký Kế toán             | GUID đảo ngược doanh số chưa lập hóa đơn      | Thực tế                            |                          |
| Chỉn sửa hóa đơn nháp     | GUID ILD cũ             | Giao dịch dòng hóa đơn          | GUID ILD sửa chữa               | Giao dịch dòng hóa đơn |
| GUID IL cũ                  | Mô tả Hóa đơn             | GUID ILD sửa chữa               | Giao dịch dòng hóa đơn          |                          |
| GUID hóa đơn cũ             | Hóa đơn                  | GUID ILD sửa chữa               | Giao dịch dòng hóa đơn          |                          |
| GUID bản ghi mục nhập thời gian       | Mục nhập Thời gian               | GUID ILD sửa chữa               | Giao dịch dòng hóa đơn          |                          |
| GUID bản ghi dòng nhật ký kế toán     | Dòng Nhật ký Kế toán             | GUID ILD sửa chữa               | Giao dịch dòng hóa đơn          |                          |
| Sửa hóa đơn đã xác nhận | GUID ILD cũ             | Giao dịch dòng hóa đơn          | GUID thực tế doanh số đã lập hóa đơn đã đảo ngược | Thực tế                   |
| GUID IL cũ                  | Mô tả Hóa đơn             | GUID thực tế doanh số đã lập hóa đơn đã đảo ngược | Thực tế                            |                          |
| GUID hóa đơn cũ             | Hóa đơn                  | GUID thực tế doanh số đã lập hóa đơn đã đảo ngược | Thực tế                            |                          |
| GUID bản ghi mục nhập thời gian       | Mục nhập Thời gian               | GUID thực tế doanh số đã lập hóa đơn đã đảo ngược | Thực tế                            |                          |
| GUID bản ghi dòng nhật ký kế toán     | Dòng Nhật ký Kế toán             | GUID thực tế doanh số đã lập hóa đơn đã đảo ngược | Thực tế                            |                          |
| GUID ILD cũ                 | Giao dịch dòng hóa đơn | GUID thực tế doanh số chưa lập hóa đơn mới    | Thực tế                            |                          |
| GUID IL cũ                  | Mô tả Hóa đơn             | GUID thực tế doanh số chưa lập hóa đơn mới    | Thực tế                            |                          |
| GUID hóa đơn cũ             | Hóa đơn                  | GUID thực tế doanh số chưa lập hóa đơn mới    | Thực tế                            |                          |
| GUID bản ghi mục nhập thời gian       | Mục nhập Thời gian               | GUID thực tế doanh số chưa lập hóa đơn mới    | Thực tế                            |                          |
| GUID bản ghi dòng nhật ký kế toán     | Dòng Nhật ký Kế toán             | GUID thực tế doanh số chưa lập hóa đơn mới    | Thực tế                            |                          |
| GUID ILD sửa chữa          | Giao dịch dòng hóa đơn | GUID thực tế doanh số chưa lập hóa đơn mới    | Thực tế                            |                          |
| GUID IL sửa chữa           | Mô tả Hóa đơn             | GUID thực tế doanh số chưa lập hóa đơn mới    | Thực tế                            |                          |
| GUID hóa đơn sửa chữa      | Hóa đơn                  | GUID thực tế doanh số chưa lập hóa đơn mới    | Thực tế                            |                          |


Hình minh họa sau đây cho thấy các liên kết được tạo giữa thực tế và nguồn của chúng tại các sự kiện khác nhau bằng cách sử dụng ví dụ về các mục thời gian trong Hoạt động dự án.

> ![Cách các thực tế được liên kết với các bản ghi nguồn trong Hoạt động Dự án.](media/TransactionOrigins.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
