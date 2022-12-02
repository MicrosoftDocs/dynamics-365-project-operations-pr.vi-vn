---
title: Nguồn gốc giao dịch – Liên kết số liệu thực tế với nguồn
description: Bài viết này giải thích cách khái niệm nguồn giao dịch được sử dụng để liên kết giá trị thực tế với bản ghi nguồn, chẳng hạn như mục nhập thời gian, mục nhập chi phí hoặc nhật ký sử dụng vật tư.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f1beff392ddd449a930d38016ca6083fea97953b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921328"
---
# <a name="transaction-origins---link-actuals-to-their-source"></a>Nguồn gốc giao dịch – Liên kết số liệu thực tế với nguồn

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Bản ghi nguồn giao dịch được tạo để liên kết số liệu thực tế với nguồn của chúng, chẳng hạn như mục nhập thời gian, mục nhập chi phí, nhật ký sử dụng vật tư và hóa đơn dự án.

Ví dụ sau đây trình bày hoạt động xử lý thông thường các mục nhập thời gian trong vòng đời dự án Project Operations.

> ![Xử lý các mục nhập thời gian trong Project Operations.](media/basic-guide-17.png)
 
1. Gửi một mục nhập thời gian sẽ tạo ra hai dòng nhật ký kế toán: một cho chi phí và một cho doanh số chưa lập hóa đơn.
2. Việc phê duyệt mục nhập thời gian sẽ tạo ra hai thực tế: một cho chi phí và một cho doanh số chưa lập hóa đơn.
3. Khi người dùng tạo một hóa đơn dự án, giao dịch dòng hóa đơn được tạo bằng cách sử dụng dữ liệu từ thực tế doanh số chưa lập hóa đơn.
4. Khi hóa đơn được xác nhận, hai thực tế mới được tạo ra: một đảo ngược doanh số chưa lập hóa đơn và thực tế doanh số đã lập hóa đơn.

Mỗi sự kiện trong quy trình làm việc xử lý này sẽ kích hoạt việc tạo các bản ghi trong thực thể Nguồn giao dịch để để giúp xây dựng một dấu vết của mối quan hệ giữa các hồ sơ được tạo ra trên mục nhập thời gian, dòng nhật ký kế toán, số liệu thực tế và chi tiết mô tả hóa đơn.

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


Hình minh họa sau đây cho thấy các liên kết được tạo ra giữa các loại số liệu thực tế khác nhau và nguồn của chúng tại các sự kiện khác nhau bằng cách sử dụng ví dụ về mục nhập thời gian trong Project Operations.

> ![Cách các số liệu thực tế được liên kết tới bản ghi nguồn trong Project Operations.](media/TransactionOrigins.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
