---
title: Tạo lịch trình hóa đơn trên mục mô tả hợp đồng dựa trên dự án
description: Chủ đề này cung cấp thông tin về cách tạo lịch trình hóa đơn và mốc trên mục mô tả hợp đồng.
author: rumant
manager: Annbe
ms.date: 10/17/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 674f4ccced3d0e3178799f60d9f95a2ec27cd153
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180803"
---
# <a name="create-an-invoice-schedule-on-a-project-based-contract-line"></a>Tạo lịch trình hóa đơn trên mục mô tả hợp đồng dựa trên dự án 

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Bạn có thể tạo lịch trình hóa đơn cho mục mô tả hợp đồng dựa trên dự án. Việc lập hóa đơn chỉ được cho phép sau khi bạn giành được hợp đồng và đang tạo hợp đồng dự án. Lịch trình hóa đơn cho phép hệ thống tự động tạo hóa đơn nháp cho mục mô tả hợp đồng dựa trên dự án. Tuy nhiên, nếu bạn chỉ tạo thủ công hóa đơn, thì bạn có thể bỏ qua việc tạo lịch trình hóa đơn trên mục mô tả hợp đồng.

## <a name="create-a-time-and-material-invoice-schedule-for-a-contract-line"></a>Tạo lịch trình hóa đơn theo thời gian và vật tư cho mục mô tả hợp đồng

Khi mục mô tả hợp đồng dựa trên dự án có phương thức thanh toán là theo thời gian và vật tư, hệ thống sẽ tạo lịch trình hóa đơn dựa trên ngày. Để tự động tạo lịch trình hóa đơn dựa trên ngày, hãy hoàn thành các bước sau.

1. Chuyển tới **Thiết đặt** > **Tần suất hóa đơn** và thiết lập tần suất hóa đơn.
2. Chuyển tới bản ghi hợp đồng dự án và trên tab **Tóm tắt**, trong trường **Ngày giao hàng đã yêu cầu**, hãy chọn ngày.
3. Mở mục mô tả hợp đồng **Thời gian và vật tư** mà bạn cần tạo lịch trình hóa đơn dựa trên ngày. 
4. Trên tab **Lịch trình hóa đơn**, hãy chọn ngày bắt đầu lập hóa đơn và tần suất hóa đơn.
5. Trên lưới con, hãy chọn **Tạo lịch trình hóa đơn**. Lịch trình hóa đơn sẽ được tạo với các trường **Ngày chạy hóa đơn**, **Ngày dứt điểm giao dịch** và **Trạng thái chạy** được đặt như sau:

    - **Ngày chạy hóa đơn**: Ngày này được xác định theo tần suất hóa đơn.
    - **Ngày dứt điểm giao dịch**: Ngày trước ngày chạy hóa đơn.
    - **Trạng thái chạy**: Được đặt tự động thành **Không chạy**. Khi công việc tự động tạo hóa đơn chạy trong một ngày chạy hóa đơn nhất định, trường này sẽ được cập nhật thành **Chạy thành công** hoặc **Chạy không thành công**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-contract-line"></a>Tạo lịch trình hóa đơn giá cố định cho mục mô tả hợp đồng

Khi mục mô tả hợp đồng có phương thức thanh toán cố định, bạn có thể tạo lịch trình hóa đơn dựa trên mốc. 

> [!NOTE]
> Bạn không thể tạo mốc trên mục mô tả hợp đồng nếu không có dự án nào được ánh xạ tới mục mô tả hợp đồng.

Hãy hoàn thành các bước sau để tạo lịch trình hóa đơn dựa trên mốc cho một tập hợp cố định các mốc được phân bổ đều cho khoảng thời gian theo lịch.

1. Chuyển tới **Thiết đặt** > **Tần suất hóa đơn** và thiết lập tần suất hóa đơn.
2. Chuyển tới bản ghi hợp đồng dự án và trên tab **Tóm tắt**, trong trường **Ngày giao hàng đã yêu cầu**, hãy chọn ngày.
3. Mở mục mô tả hợp đồng **Giá cố định** mà bạn định tạo lịch trình mốc. Trên tab **Mốc thanh toán**, hãy chọn ngày bắt đầu lập hóa đơn và tần suất hóa đơn. 
4. Trên lưới con, hãy chọn **Tạo các mốc định kỳ**. Lịch trình hóa đơn được tạo với các trường **Tên mốc**, **Ngày mốc** và **Số tiền mốc** được đặt như sau:

    - **Tên mốc**: Ngày này được xác định theo tần suất hóa đơn.
    - **Ngày mốc**: Ngày này được xác định theo tần suất hóa đơn.
    - **Số tiền mốc**: Số tiền này được tính bằng cách chia số tiền hợp đồng trên mục mô tả hợp đồng cho số mốc được xác định qua tần suất, ngày bắt đầu lập hóa đơn và ngày giao hàng đã yêu cầu.

    Nếu mục mô tả hợp đồng có giá trị ở trường **Số tiền thuế ước tính**, thì trường này cũng được phân chia đều nhau cho từng mốc khi tạo các mốc định kỳ.

Các mốc thanh toán phải bằng giá trị hợp đồng của mục mô tả hợp đồng. Nếu không, bạn sẽ nhận được lỗi trên trang **Mô tả hợp đồng**. Bạn có thể sửa lỗi này bằng cách xác minh rằng các mốc thanh toán bằng tổng giá trị hợp đồng của mục mô tả bằng cách tạo, chỉnh sửa hoặc xóa các mốc. Sau khi thay đổi được thực hiện, hãy làm mới trang để loại bỏ lỗi.

### <a name="manually-create-milestones"></a>Tạo thủ công các mốc thời gian

Bạn có thể tạo thủ công các mốc có giá cố định khi chúng không được phân chia thành các kỳ bằng nhau. Hãy hoàn thành các bước sau để tạo thủ công mốc.

1. Mở mục mô tả hợp đồng giá cố định mà bạn định tạo mốc, trên tab **Lịch trình hóa đơn**, trên lưới con, hãy chọn **+ Tạo mốc mới cho mục mô tả hợp đồng**. 
2. Trên trang **Tạo mốc**, hãy nhập thông tin cần thiết dựa trên bảng sau.

| Trường | Vị trí | Nội dung mô tả | Tác động xuôi tuyến |
| --- | --- | --- | --- |
| Tên mốc | Tạo nhanh | Trường văn bản dành cho tên mốc. | Mục này được chuyển qua mốc cho mục mô tả hợp đồng dự án và hóa đơn. |
| Nhiệm vụ dự án | Tạo nhanh | Nếu mốc được liên kết với nhiệm vụ dự án, hãy sử dụng mục tham chiếu này để thêm lô-gic tùy chỉnh nhằm đặt trạng thái mốc dựa trên trạng thái nhiệm vụ. | Ứng dụng, không có bất kỳ tác động xuôi tuyến nào của mục tham chiếu này đến nhiệm vụ. |
| Ngày Mốc | Tạo nhanh | Đặt ngày mà quá trình tạo hóa đơn tự động sẽ tìm kiếm trạng thái của mốc thời gian này để xem xét cho việc lập hóa đơn. | Mục này được chuyển qua mốc cho mục mô tả hợp đồng dự án và hóa đơn. |
| Trạng thái hóa đơn | Tạo nhanh | Khi mốc được tạo, trạng thái này luôn được đặt thành **Chưa sẵn sàng để lập hóa đơn** hoặc **Chưa bắt đầu**. | Mục này được chuyển qua mốc cho mục mô tả hợp đồng dự án và hóa đơn. |
| Số tiền mô tả | Tạo nhanh | Số tiền hoặc giá trị của mốc thời gian sẽ được lập hóa đơn cho khách hàng. | Mục này được chuyển qua mốc cho mục mô tả hợp đồng dự án và hóa đơn. |
| Thuế | Tạo nhanh | Số tiền thuế được áp cho mốc. | Mục này được chuyển qua mốc cho mục mô tả hợp đồng dự án và hóa đơn. |

3. Chọn **Lưu và Đóng**.
