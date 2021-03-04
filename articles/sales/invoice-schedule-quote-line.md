---
title: Lịch trình hóa đơn cho mô tả báo giá dựa trên dự án
description: Chủ đề này cung cấp thông tin về việc tạo lịch trình hóa đơn và các mốc quan trọng cho mô tả báo giá.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2b69742915fe79ee59e7fdcf317000cea79c5929
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180848"
---
# <a name="invoice-schedules-on-project-based-quote-lines"></a>Lịch trình hóa đơn cho mô tả báo giá dựa trên dự án

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Mô tả báo giá dựa trên dự án cung cấp khả năng thể hiện lịch trình hóa đơn. Đây là tùy chọn trong giai đoạn báo giá vì ứng dụng không hỗ trợ lập hóa đơn cho một dự án khi dự án được liên kết với mô tả báo giá. Việc lập hóa đơn chỉ được phép sau khi giành được báo giá. Tác động cuối cùng duy nhất của việc tạo lịch trình hóa đơn trong giai đoạn báo giá là lịch trình hóa đơn này được sao chép sang mô tả hợp đồng dựa trên dự án. Nếu không tạo lịch trình hóa đơn trong giai đoạn báo giá, bạn sẽ có thể làm như vậy trên mô tả hợp đồng dựa trên dự án.

Nhìn chung, mục đích của lịch trình hóa đơn là cho phép tự động tạo các hóa đơn nháp cho một mô tả hợp đồng dựa trên dự án. 

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-quote-line"></a>Tạo lịch trình hóa đơn theo thời gian và vật tư cho mô tả báo giá dựa trên dự án

Khi phương thức thanh toán cho mô tả báo giá dựa trên dự án là thời gian và vật tư, hệ thống sẽ tạo lịch trình hóa đơn dựa trên ngày. Để tự động tạo lịch trình hóa đơn dựa trên ngày, hãy hoàn thành các bước sau.

1. Đi đến **Thiết đặt** > **tần suất hóa đơn** và thiết lập tần suất hóa đơn.
2. Trên trang **Báo giá**, mở báo giá Dự án và trên trang **Tóm tắt**, đặt ngày giao hàng được yêu cầu.
3. Mở mô tả báo giá thời gian và vật tư mà bạn cần để tạo lịch trình hóa đơn dựa trên ngày. 
4. Trên tab **Lịch trình hóa đơn**, chọn các giá trị trong trường **Bắt đầu thanh toán** và **Tần suất hóa đơn**. 
5. Trên lưới con, hãy chọn **Tạo lịch trình hóa đơn**.
6. Ứng dụng tạo lịch trình hóa đơn với các trường **Ngày chạy hóa đơn**, **Ngày kết thúc giao dịch** và **Trạng thái chạy** được đặt theo cách sau:

    - **Ngày chạy hóa đơn** được đặt thành ngày được đọc dựa trên tần suất hóa đơn.
    - **Ngày kết thúc giao dịch** được đặt thành ngày trước **Ngày chạy hóa đơn**.
    - **Trạng thái chạy** được tự động đặt thành **Không chạy**. Khi công việc tạo hóa đơn tự động chạy trong một ngày chạy hóa đơn nhất định, nó sẽ cập nhật trường này thành **Chạy thành công** hoặc **Chạy không thành công**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-quote-line"></a>Tạo lịch trình hóa đơn giá cố định cho mô tả báo giá dựa trên dự án

Khi mô tả báo giá dựa trên dự án có phương thức thanh toán **Cố định**, hệ thống sẽ tạo lịch trình hóa đơn dựa trên mốc thời gian. Hoàn thành các bước sau để tự động tạo lịch trình này cho một tập hợp các mốc thời gian cố định được phân bổ đều cho khoảng thời gian theo lịch.

1. Đi đến **Thiết đặt** > **tần suất hóa đơn** và thiết lập tần suất hóa đơn.
2. Trên trang **Báo giá**, mở báo giá Dự án và trên trang **Tóm tắt**, đặt ngày giao hàng được yêu cầu.
3. Mở mô tả báo giá cố định mà bạn cần tạo một lịch trình mốc thời gian. 
4. Trên tab **Lịch trình hóa đơn**, chọn các giá trị trong trường **Bắt đầu thanh toán** và **Tần suất hóa đơn**. 
5. Trên lưới con, hãy chọn **Tạo các mốc định kỳ**.
6. Ứng dụng tạo lịch trình hóa đơn với tên mốc thời gian, ngày tháng và số tiền.

    - Tên mốc thời gian được đặt thành ngày được đọc dựa trên tần suất hóa đơn.
    - Ngày trên mốc thời gian được đặt thành ngày được đọc dựa trên tần suất hóa đơn.
    - Số tiền trên mốc thời gian được tính bằng cách chia số tiền báo giá trên mô tả báo giá dựa trên dự án cho số mốc thời gian được xác định bởi tần suất, ngày bắt đầu thanh toán và ngày giao hàng được yêu cầu.
    - Nếu mô tả báo giá cũng có số tiền thuế ước tính, giá trị này sẽ được chia đều cho mỗi mốc thời gian khi tạo các mốc thời gian định kỳ.

### <a name="manually-create-milestones"></a>Tạo thủ công các mốc thời gian

Các mốc giá cố định cũng có thể được tạo theo cách thủ công khi chúng không được phân chia định kỳ. Cách tạo thủ công một mốc thời gian:

Mở mô tả báo giá giá cố định mà bạn cần tạo một mốc thời gian. Ở tab **Lên lịch lập hóa đơn**, trên lưới con, chọn **+ Tạo mốc mô tả báo giá mới** rồi nhập thông tin cần thiết dựa trên bảng sau.

| **Trường** | **Vị trí** | **Mô tả** | **Tác động xuôi tuyến** |
| --- | --- | --- | --- |
| Tên mốc thời gian | Tạo nhanh | Tên mốc thời gian. | Điều này được truyền đến mốc thời gian trê mô tả hợp đồng dự án và hóa đơn |
| Nhiệm vụ dự án | Tạo nhanh | Nếu mốc thời gian liên quan đến nhiệm vụ dự án, bạn có thể sử dụng tham chiếu này để thêm logic tùy chỉnh đặt trạng thái mốc thời gian dựa trên trạng thái nhiệm vụ. | Ứng dụng, không có bất kỳ tác động xuôi tuyến nào của tham chiếu này đến nhiệm vụ. |
| Ngày trên mốc thời gian | Tạo nhanh | Đặt ngày mà quá trình tạo hóa đơn tự động sẽ tìm kiếm trạng thái của mốc thời gian này để xem xét cho việc lập hóa đơn. | Điều này được truyền đến mốc thời gian trê mô tả hợp đồng dự án và hóa đơn. |
| Trạng thái hóa đơn | Tạo nhanh | Khi một mốc thời gian được tạo, trạng thái này luôn được đặt thành **Chưa sẵn sàng để lập hóa đơn**. | Điều này được truyền đến mốc thời gian trê mô tả hợp đồng dự án và hóa đơn. |
| Số tiền mô tả | Tạo nhanh | Số tiền hoặc giá trị của mốc thời gian sẽ được lập hóa đơn cho khách hàng. | Điều này được truyền đến mốc thời gian trê mô tả hợp đồng dự án và hóa đơn. |
| Thuế | Tạo nhanh | Số tiền thuế sẽ được áp dụng cho mốc thời gian. | Điều này được truyền đến mốc thời gian trê mô tả hợp đồng dự án và hóa đơn. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]