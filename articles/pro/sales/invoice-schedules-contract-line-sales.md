---
title: Tạo lịch lập hóa đơn trên phần mô tả hợp đồng dựa trên dự án - bản đơn giản
description: Chủ đề này cung cấp thông tin về cách tạo lịch và mốc lập hóa đơn.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4706a2a711efa7d176030deaa33b65bca28d8498
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273404"
---
# <a name="create-invoice-schedules-on-a-project-based-contract-line---lite"></a>Tạo lịch lập hóa đơn trên phần mô tả hợp đồng dựa trên dự án - bản đơn giản

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Bạn có thể đính kèm lịch lập hóa đơn trên phần mô tả hợp đồng dựa trên dự án. Việc lập hóa đơn chỉ được phép sau khi giành được hợp đồng để tạo Hợp đồng dự án. Lịch lập hóa đơn cho phép tạo tự động các hóa đơn nháp cho phần mô tả hợp đồng dựa trên dự án. Nếu định sẽ luôn tạo hóa đơn theo cách thủ công, bạn có thể bỏ qua việc tạo lịch lập hóa đơn trên phần mô tả hợp đồng dựa trên dự án hoặc phần mô tả hợp đồng.

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-contract-line"></a>Tạo lịch lập hóa đơn vật tư và thời gian cho phần mô tả hợp đồng dựa trên dự án

Khi mục mô tả hợp đồng dựa trên dự án có phương thức thanh toán là theo thời gian và vật tư, hệ thống sẽ tạo lịch trình hóa đơn dựa trên ngày. Để tự động tạo lịch trình hóa đơn dựa trên ngày, hãy hoàn thành các bước sau.

1. Chuyển đến **Cài đặt** > **Tần suất lập hóa đơn** để thiết lập tần suất hóa đơn.
2. Mở hợp đồng dự án và trên tab **Tóm tắt**, đặt ngày giao được yêu cầu.
3. Mở phần mô tả hợp đồng vật tư và thời gian mà bạn muốn tạo lịch lập hóa đơn dựa trên ngày. 
4. Trên tab **Lịch lập hóa đơn**, chọn ngày bắt đầu thanh toán và tần suất lập hóa đơn. 
5. Trên lưới con, hãy chọn **Tạo lịch trình hóa đơn**.

    Hệ thống tạo lịch lập hóa đơn với thông tin của các trường sau:

    - **Ngày chạy hóa đơn** được đặt theo ngày dựa trên tần suất lập hóa đơn.
    - **Ngày dứt điểm giao dịch** được đặt thành ngày trước **Ngày chạy hóa đơn**.
    - **Trạng thái chạy** được tự động đặt thành **Không chạy**. Khi lệnh tự động tạo hóa đơn chạy cho một **Ngày chạy hóa đơn** nhất định, trường này sẽ được cập nhật thành **Chạy thành công** hoặc **Chạy không thành công**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-contract-line"></a>Tạo lịch lập hóa đơn có giá cố định cho phần mô tả hợp đồng dựa trên dự án

Khi phần mô tả hợp đồng dựa trên dự án có phương thức thanh toán theo giá cố định, bạn có thể tạo lịch lập hóa đơn dựa theo mốc. Hoàn tất các bước sau để tự động tạo lịch lập hóa đơn dựa theo mốc cho một nhóm mốc cố định phân bổ đều trong khoảng thời gian theo lịch.

1. Chuyển đến **Cài đặt** > **Tần suất lập hóa đơn** để thiết lập tần suất hóa đơn.
2. Mở hợp đồng dự án và trên tab **Tóm tắt**, đặt ngày giao được yêu cầu.
3. Mở phần mô tả hợp đồng có giá cố định mà bạn cần tạo lịch theo mốc. 
4. Trên tab **Lịch lập hóa đơn (Mốc thanh toán)**, chọn ngày bắt đầu thanh toán và tần suất lập hóa đơn. 
5. Trên lưới con, hãy chọn **Tạo các mốc định kỳ**.

    Hệ thống tạo lịch lập hóa đơn với các thông tin sau đây về mốc.

    - **Tên mốc** được đặt theo ngày dựa trên tần suất hóa đơn.
    - **Ngày của mốc** được đặt theo ngày dựa trên tần suất hóa đơn.
    - **Số tiền mốc** được tính bằng cách chia số tiền theo hợp đồng trên phần mô tả hợp đồng dựa trên dự án cho số lượng mốc theo tần suất, ngày bắt đầu thanh toán và ngày giao được yêu cầu.
    - Nếu phần mô tả hợp đồng có giá trị nằm trong trường **Số tiền thuế ước tính**, thì trường này cũng được chia ra thành từng mốc ngang bằng nhau khi tạo các mốc định kỳ.

Các mốc thanh toán phải tương ứng với giá trị theo hợp đồng trong phần mô tả hợp đồng dựa trên dự án. Nếu không, điều đó nghĩa là đã xảy ra lỗi. Bạn có thể sửa lỗi đó bằng cách thông qua việc tạo, chỉnh sửa hoặc xóa các mốc, xác minh rằng tổng các mốc thanh toán tương ứng với giá trị theo hợp đồng trong phần mô tả. Sau khi thực hiện xong các thay đổi, hãy làm mới trang.

### <a name="manually-create-milestones"></a>Tạo thủ công các mốc thời gian

Bạn có thể tạo các mốc giá cố định theo cách thủ công khi các mốc này không được phân chia theo định kỳ. Để tạo mốc theo cách thủ công, hãy hoàn tất các bước sau.

1. Mở phần mô tả hợp đồng có giá cố định mà bạn muốn tạo mốc. 
2. Ở tab **Lịch lập hóa đơn**, trên lưới con, hãy chọn **+ Tạo mốc mới trong phần Mô tả hợp đồng**.
3. Trong biểu mẫu **Tạo mốc**, nhập các thông tin bắt buộc dựa trên bảng sau. 

| Trường | Vị trí | Nội dung mô tả | Tác động xuôi tuyến |
| --- | --- | --- | --- |
| Tên mốc | Tạo nhanh | Trường văn bản dành cho tên mốc. | Trường này được bao gồm trong hóa đơn và mốc của phần mô tả hợp đồng dự án. |
| Nhiệm vụ dự án | Tạo nhanh | Nếu mốc được liên kết với một nhiệm vụ dự án, hãy sử dụng tham chiếu này để thêm logic tùy chỉnh và đặt trạng thái mốc dựa trên trạng thái nhiệm vụ. | Tham chiếu này không có tác động xuôi chiều đến nhiệm vụ. |
| Ngày Mốc | Tạo nhanh | Ngày mà theo đó quy trình tạo hóa đơn tự động sẽ tìm kiếm trạng thái của mốc này để xem xét lập hóa đơn. | Ngày này được bao gồm trong hóa đơn và mốc của phần mô tả hợp đồng dự án. |
| Trạng thái hóa đơn | Tạo nhanh | Khi mốc được tạo, trạng thái này sẽ luôn được đặt thành **Chưa sẵn sàng lập hóa đơn** hoặc **Chưa bắt đầu**. | Ngày này được bao gồm trong hóa đơn và mốc của phần mô tả hợp đồng dự án. |
| Số tiền mô tả | Tạo nhanh | Số tiền hay giá trị của mốc mà hóa đơn cho khách hàng sẽ được lập theo đó. | Trường này được bao gồm trong hóa đơn và mốc của phần mô tả hợp đồng dự án. |
| Thuế | Tạo nhanh | Số tiền thuế được áp cho mốc. | Ngày này được bao gồm trong hóa đơn và mốc của phần mô tả hợp đồng dự án. |

4. Chọn **Lưu và Đóng**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]