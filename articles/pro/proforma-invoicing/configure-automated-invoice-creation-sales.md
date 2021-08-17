---
title: Thiết lập chế độ tự động tạo hóa đơn
description: Chủ đề này cung cấp thông tin về cách thiết lập và định cấu hình chế độ tự động tạo hóa đơn ước giá.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1cce457fbc04ba9d3890d73439e6e7fd3db44d84a4498d5dc68ed82d362158b5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997542"
---
# <a name="set-up-automatic-invoice-creation"></a>Thiết lập chế độ tự động tạo hóa đơn 
 
_**Áp dụng cho:** Triển khai bản đơn giản - từ thỏa thuận đến lập hóa đơn ước giá, Project Operations cho các kịch bản dựa trên tài nguyên/không lưu kho_

Bạn có thể đặt cấu hình hoạt động tạo hóa đơn tự động trong Dynamics 365 Project Operations. Hệ thống tạo một hóa đơn ước giá nháp dựa trên lịch hóa đơn cho từng hợp đồng dự án và mục mô tả hợp đồng. Lịch trình hóa đơn được đặt cấu hình ở cấp độ mô tả hợp đồng. Mỗi mục mô tả trên hợp đồng có thể có một lịch trình hóa đơn riêng biệt hoặc cùng một lịch trình hóa đơn có thể được áp dụng cho mọi mục mô tả của hợp đồng.

Khi bạn tạo hóa đơn, hệ thống luôn tạo ít nhất một hóa đơn cho mỗi hợp đồng dự án. Trong một số trường hợp, có thể có nhiều hóa đơn được tạo. Chẳng hạn, nếu hợp đồng có nhiều khách hàng thì số lượng hóa đơn được tạo sẽ bằng với số lượng khách hàng có giao dịch có thể tính phí cần lập hóa đơn trên hợp đồng dự án đó.

## <a name="understand-how-transactions-are-included-on-an-invoice"></a>Tìm hiểu cách xác định các giao dịch sẽ được đưa vào hóa đơn 

Đôi khi, mỗi mục mô tả hợp đồng dựa trên dự án lại có một lịch trình hóa đơn riêng biệt. Lấy ví dụ, các dịch vụ triển khai cho hợp đồng Adatum có các mục mô tả hợp đồng sau:

- Công việc tạo bản mẫu có giá cố định với hai mốc được tạo thủ công.
- Công việc triển khai bao gồm Thời gian và sẽ được lập hóa đơn hai tuần một lần vào các thứ Hai.
- Các chi phí phát sinh cần được lập hóa đơn hằng tháng vào thứ Hai đầu tiên của mỗi tháng.

Lịch trình hóa đơn được xác định trên lần lượt một trong hai mục mô tả này sẽ trông giống như bảng sau:

| Mô tả hợp đồng | Ngày chạy hóa đơn | Ngày dứt điểm giao dịch | Ngày trên mốc thời gian | Số tiền mốc |
| --- | --- | --- | --- | --- |
| Công việc tạo bản mẫu | Ngày 5 tháng 10, thứ Hai | - | Ngày 5 tháng 10, thứ Hai | 5000 USD |
| - | Ngày 3 tháng 11, thứ Ba | - | Ngày 3 tháng 11, thứ Ba | 12,000 USD |
| Công việc triển khai | Ngày 5 tháng 10, thứ Hai | Ngày 4 tháng 10, Chủ nhật | - | - |
| - | Ngày 19 tháng 10, thứ Hai | Ngày 18 tháng 10, Chủ nhật | - | - |
| - | Ngày 2 tháng 11, thứ Hai | Ngày 1 tháng 11, Chủ nhật | - | - |
| - | Ngày 16 tháng 11, thứ Hai | Ngày 15 tháng 11, Chủ nhật | - | - |
| Chi phí phát sinh | Ngày 5 tháng 10, thứ Hai | Ngày 4 tháng 10, Chủ nhật | - | - |
| - | Ngày 2 tháng 11, thứ Hai | Ngày 1 tháng 11, Chủ nhật | - | - |

Trong ví dụ này, khi chức năng lập hóa đơn tự động chạy vào:

- **Ngày 4 tháng 10 trở về trước**: Không có hóa đơn nào được tạo cho hợp đồng này vì bảng **Lịch trình hóa đơn** cho mỗi mục mô tả hợp đồng này không xác định ngày 4 tháng 10, Chủ nhật là ngày chạy hóa đơn.
- **Ngày 5 tháng 10, thứ Hai**: Một hóa đơn được tạo cho:

    - Công việc tạo bản mẫu có mốc, nếu mục đó được đánh dấu là **Đã sẵn sàng để lập hóa đơn**.
    - Công việc triển khai có tất cả các giao dịch Thời gian được tạo trước ngày dứt điểm giao dịch là ngày 4 tháng 10, Chủ nhật và được đánh dấu là **Đã sẵn sàng để lập hóa đơn**.
    - Các chi phí phát sinh có tất cả các giao dịch Chi phí được tạo trước ngày dứt điểm giao dịch là ngày 4 tháng 10, Chủ nhật và được đánh dấu là **Đã sẵn sàng để lập hóa đơn**.
  
- **Ngày 6 tháng 10 hoặc bất kỳ ngày nào trước 19 tháng 10**: Không có hóa đơn nào được tạo cho hợp đồng này vì bảng **Lịch trình hóa đơn** cho mỗi mục mô tả hợp đồng này không xác định ngày 6 tháng 10 hay bất kỳ ngày nào trước 19 tháng 10 là ngày chạy hóa đơn.
- **Ngày 19 tháng 10, thứ Hai**: Một hóa đơn được tạo cho công việc triển khai có tất cả các giao dịch Thời gian được tạo trước ngày dứt điểm giao dịch là ngày 18 tháng 10, Chủ nhật và được đánh dấu là **Đã sẵn sàng để lập hóa đơn**.
- **Ngày 2 tháng 11, thứ Hai**: Một hóa đơn được tạo cho:

    - Công việc triển khai có tất cả các giao dịch Thời gian được tạo trước ngày dứt điểm giao dịch là ngày 1 tháng 11, Chủ nhật và được đánh dấu là **Đã sẵn sàng để lập hóa đơn**.
    - Các chi phí phát sinh có tất cả các giao dịch Chi phí được tạo trước ngày dứt điểm giao dịch là ngày 1 tháng 11, Chủ nhật và được đánh dấu là **Đã sẵn sàng để lập hóa đơn**.

- **Ngày 3 tháng 11, thứ Ba**: Một hóa đơn được tạo cho công việc tạo bản mẫu có mốc cho 12.000 USD, nếu mục đó được đánh dấu là **Đã sẵn sàng để lập hóa đơn**.

## <a name="configure-automatic-invoicing"></a>Đặt cấu hình chức năng lập hóa đơn tự động

Hãy hoàn thành các bước sau để đặt cấu hình một lần chạy hóa đơn tự động.

1. Trong **Project Operations**, hãy chuyển tới **Thiết đặt** > **Thiết lập hóa đơn lặp lại**.
2. Tạo một công việc theo lô và đặt tên là **Tạo hóa đơn trong Project Operations**. Tên của công việc theo lô phải có cụm từ "tạo hóa đơn".
3. Ở trường **Loại công việc**, hãy chọn **Không có**. Theo mặc định, các trường **Tần suất hằng ngày** và **Đang hiện hoạt** được đặt thành **Có**.
4. Chọn **Chạy quy trình làm việc**. Trong hộp thoại **Tra cứu bản ghi**, bạn sẽ thấy 3 quy trình làm việc:

- ProcessRunCaller
- ProcessRunner
- UpdateRoleUtilization

5. Chọn **ProcessRunCaller** rồi chọn **Thêm**.
6. Trong hộp thoại tiếp theo, hãy chọn **OK**. Quy trình làm việc **Ngủ** nằm trước quy trình công việc **Xử lý**. 

> [!NOTE]
> Bạn cũng có thể chọn **ProcessRunner** trong bước 5. Sau đó, khi bạn chọn **OK**, quy trình làm việc **Xử lý** nằm trước quy trình làm việc **Ngủ**.

Các quy trình làm việc **ProcessRunCaller** và **ProcessRunner** tạo các hóa đơn. **ProcessRunCaller** gọi **ProcessRunner**. **ProcessRunner** là quy trình làm việc thực sự tạo ra hóa đơn. Quy trình làm việc kiểm tra tất cả mục mô tả hợp đồng cần phải lập hóa đơn và tạo hóa đơn cho các mục mô tả đó. Để xác định mô tả hợp đồng mà hóa đơn phải được tạo cho, công việc xem xét ngày chạy hóa đơn cho mô tả hợp đồng. Nếu mô tả hợp đồng thuộc một hợp đồng có cùng ngày chạy hóa đơn, thì các giao dịch được kết hợp thành một hóa đơn và có 2 mô tả hóa đơn. Nếu không có giao dịch nào cần lập hóa đơn, thì công việc này sẽ bỏ qua bước tạo hóa đơn.

Sau khi **ProcessRunner** chạy xong, quy trình này gọi **ProcessRunCaller**, cung cấp thời gian kết thúc và đóng lại. Sau đó, **ProcessRunCaller** sẽ khởi động một bộ đếm ngược 24 giờ tính từ thời gian kết thúc đã chỉ định. Khi hết bộ hẹn giờ, **ProcessRunCaller** sẽ đóng lại.

Công việc xử lý lô cho việc tạo hóa đơn là công việc lặp lại. Nếu quy trình lô này chạy nhiều lần, thì nhiều trường hợp công việc sẽ được tạo và gây ra lỗi. Do đó, bạn chỉ nên bắt đầu quy trình lô này một lần và chỉ bắt đầu lại nếu quy trình này dừng chạy.

> [!NOTE]
> Hoạt động lập hóa đơn theo lô trong Project Operations chỉ chạy cho các mục mô tả hợp đồng dự án được đặt cấu hình theo lịch trình hóa đơn. Mô tả hợp đồng với phương thức thanh toán giá cố định phải được định cấu hình các mốc. Mô tả hợp đồng dự án với phương thức thanh toán theo thời gian và vật tư cần thiết lập lịch trình lập hóa đơn theo ngày.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
