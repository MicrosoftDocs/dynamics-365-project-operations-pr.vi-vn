---
title: Hóa đơn ước giá
description: Bài viết này cung cấp thông tin về hóa đơn chiếu lệ trong Hoạt động dự án.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7b56c3908cce3115d5c95a4b1b233db70fb6c149
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920592"
---
# <a name="proforma-invoices"></a>Hóa đơn ước giá

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Lập hóa đơn ước giá cung cấp cho người quản lý dự án mức phê duyệt thứ hai trước khi họ tạo hóa đơn cho khách hàng. Mức phê duyệt thứ nhất hoàn thành khi các mục nhập thời gian, chi phí và vật tư mà thành viên nhóm dự án gửi được phê duyệt. Hóa đơn ước giá đã xác nhận có sẵn trong mô-đun Kế toán dự án của Project Operations. Các kế toán viên của dự án có thể thực hiện các cập nhật bổ sung như thuế bán hàng, kế toán và bố cục hóa đơn.


## <a name="creating-project-invoices"></a>Tạo hóa đơn dự án

Hóa đơn dự án có thể được tạo lần lượt từng bản hoặc hàng loạt. Bạn có thể tạo hóa đơn theo cách thủ công hoặc đặt cấu hình để tạo hóa đơn trong các lượt chạy tự động.

### <a name="manually-create-project-invoices"></a>Tạo hóa đơn dự án theo cách thủ công 

Từ trang danh sách **Hợp đồng dự án**, bạn có thể tạo hóa đơn riêng cho từng hợp đồng dự án hoặc tạo hàng loạt cho nhiều hợp đồng dự án.

Làm theo bước này để tạo hóa đơn cho một hợp đồng dự án cụ thể.

- Trên trang danh sách **Hợp đồng dự án**, hãy mở hợp đồng dự án rồi chọn **Tạo hóa đơn**.

    Hóa đơn được tạo cho tất cả giao dịch cho hợp đồng dự án đã chọn có trạng thái **Sẵn sàng để lập hóa đơn**. Các giao dịch này bao gồm thời gian, chi phí, vật tư, mốc và các dòng nhật ký kế toán về doanh số bán hàng chưa lập hóa đơn khác.

Làm theo các bước sau để tạo hóa đơn hàng loạt.

1. Trên trang danh sách **Hợp đồng dự án**, hãy chọn một hoặc nhiều hợp đồng dự án mà bạn phải tạo hóa đơn rồi chọn **Tạo hóa đơn hợp đồng**.

    Thông báo cảnh báo cho bạn biết rằng có thể có sự chậm trễ trước khi hóa đơn được tạo. Quá trình này cũng hiển thị.

2. Chọn **OK** để đóng hộp thông báo.

    Hóa đơn được tạo cho tất cả giao dịch trên mô tả hợp đồng có trạng thái **Sẵn sàng để lập hóa đơn**. Các giao dịch này bao gồm thời gian, chi phí, vật tư, mốc và các dòng nhật ký kế toán về doanh số bán hàng chưa lập hóa đơn khác.

3. Để xem các hóa đơn được tạo, hãy chuyển đến **Bán hàng** \> **Thanh toán** \> **Hóa đơn**. Bạn sẽ thấy một hóa đơn cho mỗi hợp đồng dự án.

### <a name="set-up-automated-creation-of-project-invoices"></a>Thiết lập tự động tạo hóa đơn dự án 

Làm theo các bước sau để đặt cấu hình một lượt chạy hóa đơn tự động.

1. Chuyển đến **Chế độ cài đặt** \> **Công việc theo lô**.
2. Tạo một công việc theo lô rồi đặt tên là **Tạo hóa đơn trong Hoạt động dự án**. Tên của công việc lô phải gồm cụm từ "Tạo hóa đơn".
3. Trong trường **Loại công việc**, hãy chọn **Không**. Theo mặc định, các tùy chọn **Tần suất hàng ngày** và **Hiện hoạt** được đặt thành **Có**.
4. Chọn **Chạy quy trình làm việc**. Trong hộp thoại **Tra cứu bản ghi**, bạn sẽ thấy 3 quy trình làm việc:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Chọn **ProcessRunCaller** rồi chọn **Thêm**.
6. Trong hộp thoại tiếp theo, hãy chọn **OK**. Quy trình làm việc **Ngủ** nằm trước quy trình công việc **Xử lý**.

    Bạn cũng có thể chọn **ProcessRunner** trong bước 5. Sau đó, khi bạn chọn **OK**, quy trình làm việc **Xử lý** nằm trước quy trình làm việc **Ngủ**.

Các quy trình làm việc **ProcessRunCaller** và **ProcessRunner** tạo các hóa đơn. **ProcessRunCaller** gọi **ProcessRunner**. **ProcessRunner** là quy trình làm việc thực sự tạo ra hóa đơn. Quy trình này thông qua tất cả mô tả hợp đồng mà các hóa đơn phải được tạo cho và tạo hóa đơn cho các mô tả đó. Để xác định mô tả hợp đồng mà hóa đơn phải được tạo cho, công việc xem xét ngày chạy hóa đơn cho mô tả hợp đồng. Nếu mô tả hợp đồng thuộc một hợp đồng có cùng ngày chạy hóa đơn, thì các giao dịch được kết hợp thành một hóa đơn và có 2 mô tả hóa đơn. Nếu không có giao dịch để tạo hóa đơn cho, công việc này sẽ bỏ qua bước tạo hóa đơn.

Sau khi **ProcessRunner** chạy xong, quy trình này gọi **ProcessRunCaller**, cung cấp thời gian kết thúc và đóng lại. Sau đó, **ProcessRunCaller** khởi động bộ hẹn giờ trong 24 giờ từ thời gian kết thúc đã chỉ định. Khi hết bộ hẹn giờ, **ProcessRunCaller** sẽ đóng lại.

Công việc xử lý lô cho việc tạo hóa đơn là công việc lặp lại. Nếu quy trình lô này chạy nhiều lần, thì nhiều trường hợp công việc được tạo và gây ra lỗi. Do đó, bạn chỉ nên bắt đầu quy trình lô một lần và bắt đầu lại chỉ khi quy trình này dừng chạy.

> [!NOTE]
> Việc lập hóa đơn theo lô chỉ chạy cho các dòng hợp đồng dự án được định cấu hình theo lịch trình hóa đơn. Mô tả hợp đồng với phương thức thanh toán giá cố định phải được định cấu hình các mốc. Mô tả hợp đồng dự án với phương thức thanh toán theo thời gian và vật tư cần thiết lập lịch trình lập hóa đơn theo ngày. Điều này cũng áp dụng cho mô tả hợp đồng dựa trên dự án.      
 
### <a name="edit-a-draft-invoice"></a>Sửa hóa đơn đã xác nhận

Khi bạn tạo một hóa đơn dự án nháp, tất cả giao dịch bán hàng chưa được lập hóa đơn sẽ được tạo khi các mục nhập thời gian, chi phí và mức sử dụng vật tư được phê duyệt được kéo vào hóa đơn. Bạn có thể thực hiện các điều chỉnh sau khi hóa đơn vẫn còn trong giai đoạn nháp:

- Xóa hoặc chỉnh sửa chi tiết mô tả hóa đơn.
- Chỉnh sửa và điều chỉnh loại thanh toán và số lượng.

Chọn **Xác nhận** để xác nhận hóa đơn. Hành động Xác nhận là hành động một chiều. khi bạn chọn **Xác nhận**, hệ thống đặt hóa đơn ở chế độ chỉ đọc và tạo doanh số bán hàng thực tế đã lập hóa đơn từ mỗi chi tiết mô tả hóa đơn cho mỗi mô tả hóa đơn. Nếu chi tiết mô tả hóa đơn tham chiếu doanh số bán hàng thực tế chưa lập hóa đơn, thì hệ thống cũng đảo ngược doanh số bán hàng thực tế chưa lập hóa đơn đó. (Mọi chi tiết mô tả hóa đơn được tạo từ mục nhập thời gian hoặc chi phí sẽ tham chiếu doanh số bán hàng thực tế chưa được lập hóa đơn). Các hệ thống tích hợp sổ cái chung có thể dùng đảo ngược này để đảo ngược công việc dự án đang tiến hành (WIP) cho mục đích kế toán.

> [!NOTE]
> Không thể chỉnh sửa hoặc xóa các hóa đơn chiếu lệ đã xác nhận và các bản ghi liên quan như dòng hóa đơn và dòng hóa đơn. 

### <a name="correct-a-confirmed-invoice"></a>Sửa hóa đơn đã xác nhận

Có thể chỉnh sửa các hóa đơn đã xác nhận (đã chỉnh sửa). Khi bạn sửa các hóa đơn đã xác nhận, một hóa đơn hiệu chỉnh mới ở dạng bản nháp được tạo. Vì giả định là bạn muốn đảo ngược tất cả giao dịch và số lượng từ hóa đơn ban đầu, hóa đơn hiệu chỉnh này bao gồm tất cả giao dịch từ hóa đơn ban đầu và tất cả số lượng trên đó là 0 (không).

Nếu bất kỳ giao dịch nào không yêu cầu chỉnh sửa, bạn có thể xóa các giao dịch đó khỏi hóa đơn hiệu chỉnh ở dạng bản nháp. Nếu muốn đảo ngược hoặc chỉ trả lại một phần số lượng, bạn có chỉnh sửa trường **Số lượng** trên chi tiết mô tả. Nếu mở chi tiết mô tả hóa đơn, bạn có thể thấy số lượng hóa đơn ban đầu. Sau đó, bạn có thể chỉnh sửa số lượng hóa đơn hiện tại sao cho ít hơn hoặc nhiều hơn số lượng hóa đơn ban đầu.

Khi bạn xác nhận hóa đơn chỉnh sửa, doanh số bán hàng thực tế được lập hóa đơn ban đầu được đảo ngược và doanh số bán hàng thực tế mới được lập hóa đơn được tạo. Nếu số lượng giảm, sự khác biệt dẫn đến doanh số bán hàng thực tế mới chưa được lập hóa đơn cũng được tạo. Ví dụ: nếu doanh số bán hàng ban đầu được lập hóa đơn là trong 8 giờ, thì chi tiết mô tả dòng hóa đơn hiệu chỉnh có số lượng giảm là 6 giờ, dòng bán hàng ban đầu được lập hóa đơn bị đảo và tạo ra 2 doanh số bán hàng thực tế mới:

- Doanh số bán hàng thực tế được lập hóa đơn cho 6 giờ.
- Doanh số bán hàng thực tế được lập hóa đơn cho 2 giờ còn lại. Giao dịch này có thể được lập hóa đơn sau hoặc đánh dấu là không tính phí, tùy thuộc vào các cuộc đàm phán với khách hàng.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
