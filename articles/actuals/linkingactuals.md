---
title: Liên kết giá trị thực tế với bản ghi gốc
description: Chủ đề này giải thích cách liên kết giá trị thực tế với bản ghi gốc, chẳng hạn như mục nhập thời gian, mục nhập chi phí hoặc nhật ký sử dụng vật tư.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b5a70d2c2b3f98028b4e4998ed25ab73a275c66e4b8137eb573b943658a1a41e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991782"
---
# <a name="link-actuals-to-original-records"></a>Liên kết giá trị thực tế với bản ghi gốc

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_


Trong Dynamics 365 Project Operations, *giao dịch kinh doanh* là một khái niệm trừu tượng không được đại diện bởi bất kỳ thực thể nào. Tuy nhiên, một số trường phổ biến và quy trình trên thực thể được thiết kế để sử dụng các khái niệm về giao dịch kinh doanh. Các thực thể sau đây sử dụng khái niệm này:

- Chi tiết dòng báo giá
- Chi tiết dòng hợp đồng
- Dòng ước tính
- Dòng nhật ký kế toán
- Thực tế

Trong các thực thể này, **Chi tiết mô tả báo giá**, **Chi tiết mô tả hợp đồng** và **Dòng ước tính** được ánh xạ tới giai đoạn ước tính trong vòng đời dự án. **Dòng nhật ký kế toán** và **Thực thể thực tế** được ánh xạ tới giai đoạn thực thi trong chu kỳ dự án.

Project Operations công nhận các bản ghi trong năm thực thể này là giao dịch kinh doanh. Sự khác biệt duy nhất là bản ghi trong thực thể được ánh xạ tới giai đoạn ước tính được coi là dự báo tài chính, trong khi các bản ghi trong thực thể được ánh xạ tới giai đoạn thực hiện được coi là sự kiện tài chính đã xảy ra.

## <a name="concepts-that-are-unique-to-business-transactions"></a>Khái niệm duy nhất cho các giao dịch kinh doanh
Các khái niệm sau đây là duy nhất cho các khái niệm về giao dịch kinh doanh:

- Loại giao dịch
- Lớp giao dịch
- Nguồn gốc giao dịch
- Kết nối giao dịch

### <a name="transaction-type"></a>Loại giao dịch

Loại giao dịch đại diện cho thời gian và bối cảnh tác động tài chính trên một dự án. Loại giao dịch này được biểu thị bằng một bộ tùy chọn có các giá trị được hỗ trợ trong Project Operations:

  - Chi phí
  - Hợp đồng dự án
  - Doanh thu chưa lập hóa đơn
  - Doanh số đã lập hóa đơn
  - Bán hàng liên tổ chức
  - Chi phí đơn vị nguồn lực

### <a name="transaction-class"></a>Lớp giao dịch

Lớp giao dịch đại diện cho các loại chi phí khác nhau phát sinh trên dự án. Loại giao dịch này được biểu thị bằng một bộ tùy chọn có các giá trị được hỗ trợ trong Project Operations:

  - Thời gian
  - Chi phí
  - Vật liệu
  - Phí
  - Mốc
  - Thuế

**Mốc** thường được dùng bởi logic kinh doanh để lập hóa đơn giá cố định trong Project Operations.

### <a name="transaction-origin"></a>Nguồn gốc giao dịch

**Nguồn gốc giao dịch** là một thực thể giúp lưu trữ nguồn gốc của từng giao dịch kinh doanh. Khi một dự án đang được thực hiện, mỗi giao dịch kinh doanh sẽ làm phát sinh một giao dịch kinh doanh khác, từ đó sẽ tạo ra một giao dịch khác, v.v. Thực thể nguồn gốc giao dịch được thiết kế để lưu trữ dữ liệu về nguồn gốc của mỗi giao dịch để giúp báo cáo và truy xuất nguồn gốc. 

### <a name="transaction-connection"></a>Kết nối giao dịch

**Kết nối giao dịch** là một thực thể lưu trữ mối quan hệ giữa hai giao dịch kinh doanh tương tự, chẳng hạn như chi phí và giá trị thực tế về doanh số có liên quan hoặc các lần đảo ngược giao dịch được kích hoạt bởi các hoạt động lập hóa đơn như xác nhận hóa đơn hoặc chỉnh sửa hóa đơn.

**Nguồn gốc giao dịch** và **Kết nối giao dịch** kết hợp lại để giúp bạn theo dõi mối quan hệ giữa giao dịch và hành động kinh doanh dẫn đến một giao dịch kinh doanh cụ thể.

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>Ví dụ: Cách nguồn gốc giao dịch hoạt động với kết nối giao dịch

Ví dụ sau đây trình bày hoạt động xử lý thông thường các mục nhập thời gian trong vòng đời dự án Project Operations.

> ![Xử lý mục nhập thời gian trong vòng đời Project Service.](media/basic-guide-17.png)
 
1. Gửi một mục nhập thời gian sẽ tạo ra hai dòng nhật ký kế toán: một dòng cho chi phí và một dòng cho doanh số chưa lập hóa đơn.
2. Lần phê duyệt mục nhập thời gian cuối cùng sẽ tạo ra hai giá trị thực tế: một giá trị thực tế cho chi phí và một giá trị thực tế cho doanh số chưa lập hóa đơn.
3. Khi một hóa đơn dự án mới được tạo, giao dịch mô tả hóa đơn được tạo bằng cách sử dụng dữ liệu từ giá trị thực tế về doanh số chưa lập hóa đơn. 
4. Khi hóa đơn được xác nhận, hai giá trị thực tế mới được tạo ra: một giá trị thực tế đảo ngược doanh số chưa lập hóa đơn và một giá trị thực tế về doanh số đã lập hóa đơn.

Mỗi sự kiện này tạo ra một bản ghi trong các thực thể **Nguồn gốc giao dịch** và **Kết nối giao dịch**. Các bản ghi mới này giúp xây dựng lịch sử mối quan hệ giữa các bản ghi được tạo qua mục nhập thời gian, dòng nhật ký ký toán, giá trị thực tế và chi tiết mô tả hóa đơn.

Bảng sau hiển thị các bản ghi trong thực thể **Nguồn gốc giao dịch** cho quy trình làm việc.

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

Bảng sau hiển thị các bản ghi trong thực thể **Kết nối giao dịch** cho quy trình làm việc.

| Sự kiện                          | Giao dịch 1                 | Vai trò giao dịch 1 | Loại giao dịch 1           | Giao dịch 2                | Vai trò giao dịch 2 | Loại giao dịch 2 |
|--------------------------------|-------------------------------|--------------------|------------------------------|------------------------------|--------------------|--------------------|
| Gửi mục nhập thời gian          | GUID dòng nhật ký kế toán (doanh số)     | Doanh số chưa lập hóa đơn     | msdyn_journalline            | GUID dòng nhật ký kế toán (chi phí)     | Chi phí               | msdyn_journalline  |
| Phê duyệt thời gian                  | GUID thực tế chưa lập hóa đơn mới (Doanh số)  | Bán hàng Chưa lập hóa đơn     | msdyn_actual                 | GUID thực tế chi phí (chi phí)       | Chi phí               | msdyn_actual       |
| Tạo hóa đơn               | GUID chi tiết dòng hóa đơn      | Bán hàng Đã lập hóa đơn       | msdyn_invoicelinetransaction | GUID thực tế doanh số chưa lập hóa đơn   | Doanh số chưa lập hóa đơn     | msdyn_actual       |
| Thông tin hóa đơn           | GUID thực tế đảo ngược         | Đảo ngược          | msdyn_actual                 | GUID doanh số chưa lập hóa đơn gốc | Gốc           | msdyn_actual       |
| GUID doanh số đã lập hóa đơn              | Doanh số đã lập hóa đơn                  | msdyn_actual       | GUID thực tế doanh số chưa lập hóa đơn   | Doanh số chưa lập hóa đơn               | msdyn_actual       |                    |
| Chỉn sửa hóa đơn nháp       | GUID giao dịch dòng hóa đơn | Thay thế          | msdyn_invoicelinetransaction | GUID doanh số đã lập hóa đơn            | Gốc           | msdyn_actual       |
| Xác nhận sửa hóa đơn     | GUID đảo ngược doanh số đã lập hóa đơn    | Đảo ngược          | msdyn_actual                 | GUID doanh số đã lập hóa đơn            | Gốc           | msdyn_actual       |
| GUID thực tế doanh số chưa lập hóa đơn mới | Thay thế                     | msdyn_actual       | GUID doanh số đã lập hóa đơn            | Gốc                     | msdyn_actual       |                    |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
