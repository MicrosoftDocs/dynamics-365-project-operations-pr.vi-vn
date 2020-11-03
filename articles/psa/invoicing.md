---
title: Lập hóa đơn trong Project Service Automation
description: Chủ đề này cung cấp thông tin về việc lập hóa đơn.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: f8107a660f9993c7b6a32d69047a81fb7e0abef8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087172"
---
# <a name="invoicing-in-project-service-automation"></a>Lập hóa đơn trong Project Service Automation

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Lập hóa đơn trong Dynamics 365 Project Service Automation hữu ích vì cung cấp cho người quản lý dự án mức phê duyệt thứ hai trước khi họ tạo hóa đơn cho khách hàng. Mức phê duyệt thứ nhất hoàn thành khi các mục nhập thời gian và chi phí mà thành viên nhóm dự án gửi được phê duyệt.

PSA không được thiết kế để tạo hóa đơn dành cho khách hàng vì các lý do sau:

- PSA không chứa thông tin thuế.
- PSA không thể chuyển đổi các loại tiền tệ khác thành tiền hệ lập hóa đơn bằng cách dùng tỷ giá hối đoái được đặt cấu hình chính xác.
- PSA không thể định dạng hóa đơn theo cách chính xác để các hóa đơn có thể được in.

Thay vào đó, bạn có thể dùng hệ thống kế toán hoặc tài chính để tạo hóa đơn dành cho khách hàng sử dụng thông tin từ đề xuất hóa đơn được tạo trong PSA.

## <a name="creating-project-invoices-in-psa"></a>Tạo hóa đơn dự án trong PSA

Hóa đơn dự án có thể được tạo lần lượt từng bản hoặc hàng loạt. Bạn có thể tạo hóa đơn theo cách thủ công hoặc đặt cấu hình để tạo hóa đơn trong các lượt chạy tự động.

### <a name="manually-create-project-invoices-in-psa"></a>Tạo hóa đơn dự án trong PSA theo cách thủ công

Từ trang danh sách **Hợp đồng dự án** , bạn có thể tạo hóa đơn riêng cho từng hợp đồng dự án hoặc tạo hàng loạt cho nhiều hợp đồng dự án.

Làm theo bước này để tạo hóa đơn cho một hợp đồng dự án cụ thể.

- Trên trang danh sách **Hợp đồng dự án** , hãy mở hợp đồng dự án rồi chọn **Tạo hóa đơn**.

    ![Tạo hóa đơn dự án cho hợp đồng dự án cụ thể](media/CreateProjectInvoicesOneByOne.png)

    Hóa đơn được tạo cho tất cả giao dịch cho hợp đồng dự án đã chọn có trạng thái **Sẵn sàng để lập hóa đơn**. Các giao dịch này bao gồm thời gian, chi phí, mốc và mô tả hợp đồng dựa trên sản phẩm.

Làm theo các bước sau để tạo hóa đơn hàng loạt.

1. Trên trang danh sách **Hợp đồng dự án** , hãy chọn một hoặc nhiều hợp đồng dự án mà bạn phải tạo hóa đơn rồi chọn **Tạo hóa đơn hợp đồng**.

    ![Tạo hóa đơn dự án hàng loạt](media/CreateProjectInvoicesBulk.png)

    Thông báo cảnh báo cho bạn biết rằng có thể có sự chậm trễ trước khi hóa đơn được tạo. Quá trình này cũng hiển thị.

2. Chọn **OK** để đóng hộp thông báo.

    Hóa đơn được tạo cho tất cả giao dịch trên mô tả hợp đồng có trạng thái **Sẵn sàng để lập hóa đơn**. Các giao dịch này bao gồm thời gian, chi phí, mốc và mô tả hợp đồng dựa trên sản phẩm.

3. Để xem các hóa đơn được tạo, hãy chuyển đến **Bán hàng** \> **Thanh toán** \> **Hóa đơn**. Bạn sẽ thấy một hóa đơn cho mỗi hợp đồng dự án.

### <a name="set-up-automated-creation-of-project-invoices-in-psa"></a>Thiết lập tự động tạo hóa đơn dự án trong PSA

Làm theo các bước sau để đặt cấu hình một lượt chạy hóa đơn tự động trong PSA.

1. Chuyển đến **Project Service** \> **Cài đặt** \> **Công việc lô**.
2. Tạo một công việc lô rồi đặt tên là **Tạo hóa đơn trong PSA**. Tên của công việc lô phải gồm cụm từ "Tạo hóa đơn".
3. Trong trường **Loại công việc** , hãy chọn **Không**. Theo mặc định, các tùy chọn **Tần suất hàng ngày** và **Hiện hoạt** được đặt thành **Có**.
4. Chọn **Chạy quy trình làm việc**. Trong hộp thoại **Tra cứu bản ghi** , bạn sẽ thấy 3 quy trình làm việc:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Chọn **ProcessRunCaller** rồi chọn **Thêm**.
6. Trong hộp thoại tiếp theo, hãy chọn **OK**. Quy trình làm việc **Ngủ** nằm trước quy trình công việc **Xử lý**.

    Bạn cũng có thể chọn **ProcessRunner** trong bước 5. Sau đó, khi bạn chọn **OK** , quy trình làm việc **Xử lý** nằm trước quy trình làm việc **Ngủ**.

Các quy trình làm việc **ProcessRunCaller** và **ProcessRunner** tạo các hóa đơn. **ProcessRunCaller** gọi **ProcessRunner**. **ProcessRunner** là quy trình làm việc thực sự tạo ra hóa đơn. Quy trình này thông qua tất cả mô tả hợp đồng mà các hóa đơn phải được tạo cho và tạo hóa đơn cho các mô tả đó. Để xác định mô tả hợp đồng mà hóa đơn phải được tạo cho, công việc xem xét ngày chạy hóa đơn cho mô tả hợp đồng. Nếu mô tả hợp đồng thuộc một hợp đồng có cùng ngày chạy hóa đơn, thì các giao dịch được kết hợp thành một hóa đơn và có 2 mô tả hóa đơn. Nếu không có giao dịch để tạo hóa đơn cho, công việc này sẽ bỏ qua bước tạo hóa đơn.

Sau khi **ProcessRunner** chạy xong, quy trình này gọi **ProcessRunCaller** , cung cấp thời gian kết thúc và đóng lại. Sau đó, **ProcessRunCaller** khởi động bộ hẹn giờ trong 24 giờ từ thời gian kết thúc đã chỉ định. Khi hết bộ hẹn giờ, **ProcessRunCaller** sẽ đóng lại.

Công việc xử lý lô cho việc tạo hóa đơn là công việc lặp lại. Nếu quy trình lô này chạy nhiều lần, thì nhiều trường hợp công việc được tạo và gây ra lỗi. Do đó, bạn chỉ nên bắt đầu quy trình lô một lần và bắt đầu lại chỉ khi quy trình này dừng chạy.

> [!NOTE]
> Tính năng lập hóa đơn hàng loạt trong Project Service Automation chỉ hoạt động đối với mô tả hợp đồng dự án được định cấu hình theo lịch trình hóa đơn. Mô tả hợp đồng với phương thức thanh toán giá cố định phải được định cấu hình các mốc. Mô tả hợp đồng dự án với phương thức thanh toán theo thời gian và vật tư cần thiết lập lịch trình lập hóa đơn theo ngày. Thông tin về việc thiết lập tần suất lập hóa đơn trong bối cảnh của dự án dựa trên mô tả báo giá có trong chủ đề [Báo giá và mô tả báo giá](basic-quote-lines.md#invoice-schedule). Điều này cũng áp dụng cho mô tả hợp đồng dựa trên dự án.      
 
### <a name="edit-a-draft-psa-invoice"></a>Chỉnh sửa hóa đơn PSA nháp

Khi bạn tạo một hóa đơn dự án nháp, tất cả giao dịch bán hàng chưa được lập hóa đơn sẽ được tạo khi các mục nhập thời gian và chi phí được phê duyệt được kéo vào hóa đơn. Bạn có thể thực hiện các điều chỉnh sau khi hóa đơn vẫn còn trong giai đoạn nháp:

- Xóa hoặc chỉnh sửa chi tiết mô tả hóa đơn.
- Chỉnh sửa và điều chỉnh loại thanh toán và số lượng.
- Trực tiếp thêm thời gian, chi phí và phí ở dạng các giao dịch trên hóa đơn. Bạn có thể sử dụng tính năng này nếu mô tả hóa đơn được ánh xạ đến mô tả hợp đồng cho phép các lớp giao dịch này.

Chọn **Xác nhận** để xác nhận hóa đơn. Hành động Xác nhận là hành động một chiều. khi bạn chọn **Xác nhận** , hệ thống đặt hóa đơn ở chế độ chỉ đọc và tạo doanh số bán hàng thực tế đã lập hóa đơn từ mỗi chi tiết mô tả hóa đơn cho mỗi mô tả hóa đơn. Nếu chi tiết mô tả hóa đơn tham chiếu doanh số bán hàng thực tế chưa lập hóa đơn, thì hệ thống cũng đảo ngược doanh số bán hàng thực tế chưa lập hóa đơn đó. (Mọi chi tiết mô tả hóa đơn được tạo từ mục nhập thời gian hoặc chi phí sẽ tham chiếu doanh số bán hàng thực tế chưa được lập hóa đơn). Các hệ thống tích hợp sổ cái chung có thể dùng đảo ngược này để đảo ngược công việc dự án đang tiến hành (WIP) cho mục đích kế toán.

### <a name="correct-a-confirmed-psa-invoice"></a>Sửa hóa đơn PSA đã xác nhận

Có thể chỉnh sửa các hóa đơn PSA đã xác nhận (đã chỉnh sửa). Khi bạn sửa các hóa đơn đã xác nhận, một hóa đơn hiệu chỉnh mới ở dạng bản nháp được tạo. Vì giả định là bạn muốn đảo ngược tất cả giao dịch và số lượng từ hóa đơn ban đầu, hóa đơn hiệu chỉnh này bao gồm tất cả giao dịch từ hóa đơn ban đầu và tất cả số lượng trên đó là 0 (không).

Nếu bất kỳ giao dịch nào không yêu cầu chỉnh sửa, bạn có thể xóa các giao dịch đó khỏi hóa đơn hiệu chỉnh ở dạng bản nháp. Nếu muốn đảo ngược hoặc chỉ trả lại một phần số lượng, bạn có chỉnh sửa trường **Số lượng** trên chi tiết mô tả. Nếu mở chi tiết mô tả hóa đơn, bạn có thể thấy số lượng hóa đơn ban đầu. Sau đó, bạn có thể chỉnh sửa số lượng hóa đơn hiện tại sao cho ít hơn hoặc nhiều hơn số lượng hóa đơn ban đầu.

Khi bạn xác nhận hóa đơn chỉnh sửa, doanh số bán hàng thực tế được lập hóa đơn ban đầu được đảo ngược và doanh số bán hàng thực tế mới được lập hóa đơn được tạo. Nếu số lượng giảm, sự khác biệt dẫn đến doanh số bán hàng thực tế mới chưa được lập hóa đơn cũng được tạo. Ví dụ: nếu doanh số bán hàng ban đầu được lập hóa đơn là trong 8 giờ, thì chi tiết mô tả hóa đơn hiệu chỉnh có số lượng giảm là 6 giờ, PSA đảo ngược mô tả bán hàng ban đầu được lập hóa đơn và tạo 2 doanh số bán hàng thực tế mới:

- Doanh số bán hàng thực tế được lập hóa đơn cho 6 giờ.
- Doanh số bán hàng thực tế được lập hóa đơn cho 2 giờ còn lại. Giao dịch này có thể được lập hóa đơn sau hoặc đánh dấu là không tính phí, tùy thuộc vào các cuộc đàm phán với khách hàng.
