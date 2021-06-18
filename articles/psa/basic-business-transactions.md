---
title: Giao dịch kinh doanh
description: Chủ đề này cung cấp thông tin về các giao dịch kinh doanh.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 33c27acc6747c94d76892f41031adc46150da0e0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011577"
---
# <a name="business-transactions"></a>Giao dịch kinh doanh

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Trong Dynamics 365 Project Service Automation, *giao dịch kinh doanh* là một khái niệm trừu tượng không được đại diện bởi bất kỳ thực thể nào. Tuy nhiên, một số trường phổ biến và quy trình trên thực thể được thiết kế để sử dụng các khái niệm về giao dịch kinh doanh. Các thực thể sau đây sử dụng khái niệm trừu tượng này:

- Chi tiết dòng báo giá
- Chi tiết dòng hợp đồng
- Dòng ước tính
- Dòng nhật ký kế toán
- Thực tế

Trong các thực thể này, chi tiết dòng báo giá, chi tiết dòng hợp đồng và dòng ước tính được ánh xạ tới giai đoạn ước tính trong vòng đời dự án. Dòng nhật ký dự án và thực thể thực tế được ánh xạ tới giai đoạn thực thi trong chu kỳ dự án.

PSA xử lý hồ sơ trong năm thực thể này như giao dịch kinh doanh. Sự khác biệt duy nhất là hồ sơ trong thực thể được ánh xạ tới giai đoạn ước tính được coi là dự báo tài chính, trong khi các bản ghi trong thực thể được ánh xạ tới giai đoạn thực hiện được coi là sự kiện tài chính đã xảy ra.

Để biết thêm thông tin, hãy xem [Ước tính](estimates.md) và [Thực tế](actuals.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Khái niệm duy nhất cho các giao dịch kinh doanh
Các khái niệm sau đây là duy nhất cho các khái niệm về giao dịch kinh doanh:

- Loại giao dịch
- Lớp giao dịch
- Nguồn gốc giao dịch
- Kết nối giao dịch

### <a name="transaction-type"></a>Loại giao dịch

Loại giao dịch đại diện cho thời gian và bối cảnh tác động tài chính trên một dự án. Nó được biểu thị bằng một bộ tùy chọn có các giá trị được hỗ trợ trong PSA:
- Chi phí
- Hợp đồng dự án
- Bán hàng chưa lập hóa đơn
- Doanh số đã lập hóa đơn
- Bán hàng liên tổ chức
- Chi phí đơn vị nguồn lực

### <a name="transaction-class"></a>Lớp giao dịch

Lớp giao dịch đại diện cho các loại chi phí khác nhau phát sinh trên dự án. Nó được biểu thị bằng một bộ tùy chọn có các giá trị được hỗ trợ trong PSA:

- Time
- Chi phí
- Vật tư
- Phí
- Mốc
- Thuế

Giá trị **mốc quan trọng** thường được dùng bởi logic kinh doanh để lập hóa đơn giá cố định trong PSA.

### <a name="transaction-origin"></a>Nguồn gốc giao dịch

Nguồn gốc giao dịch là một thực thể giúp lưu trữ nguồn gốc của từng giao dịch kinh doanh. Khi bắt đầu thực hiện dự án, mỗi giao dịch kinh doanh sẽ tạo ra một giao dịch kinh doanh khác, rồi giao dịch kinh doanh đó lại tạo ra một giao dịch kinh doanh khác, v.v. Thực thể nguồn gốc giao dịch được thiết kế để lưu trữ dữ liệu về nguồn gốc của từng giao dịch để hỗ trợ công việc báo cáo và truy xuất nguồn gốc. 

### <a name="transaction-connection"></a>Kết nối giao dịch

Kết nối giao dịch là một thực thể lưu trữ mối quan hệ giữa hai giao dịch kinh doanh tương tự, chẳng hạn như chi phí và thực tế bán hàng liên quan hoặc đảo ngược giao dịch được kích hoạt bằng các hoạt động thanh toán như xác nhận hóa đơn hoặc chỉnh sửa hóa đơn.

Các thực thể nguồn gốc giao dịch và kết nối giao dịch kết hợp lại để giúp bạn theo dõi mối quan hệ giữa giao dịch và hành động kinh doanh dẫn đến việc tạo ra một giao dịch kinh doanh cụ thể.

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>Ví dụ: Cách nguồn gốc giao dịch hoạt động với kết nối giao dịch

Ví dụ sau đây trình bày hoạt động xử lý thông thường các mục nhập thời gian trong vòng đời dự án PSA.

> ![Xử lý mục nhập thời gian trong vòng đời Project Service](media/basic-guide-17.png)
 
1. Gửi một mục nhập thời gian sẽ tạo ra hai dòng nhật ký kế toán: một cho chi phí và một cho doanh số chưa lập hóa đơn.
2. Việc phê duyệt mục nhập thời gian sẽ tạo ra hai thực tế: một cho chi phí và một cho doanh số chưa lập hóa đơn.
3. Khi người dùng tạo một hóa đơn dự án, giao dịch dòng hóa đơn được tạo bằng cách sử dụng dữ liệu từ thực tế doanh số chưa lập hóa đơn. 
4. Khi hóa đơn được xác nhận, hai thực tế mới được tạo ra: một đảo ngược doanh số chưa lập hóa đơn và thực tế doanh số đã lập hóa đơn.

Mỗi sự kiện trong số này sẽ khiến tạo ra các hồ sơ trong thực thể nguồn gốc giao dịch và kết nối giao dịch để giúp xây dựng một dấu vết của mối quan hệ giữa các hồ sơ được tạo ra trên mục nhập thời gian, dòng nhật ký kế toán, thực tế và chi tiết dòng hóa đơn.

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

Bảng sau hiển thị các bản ghi trong thực thể kết nối giao dịch cho luồng công việc trước đó.

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