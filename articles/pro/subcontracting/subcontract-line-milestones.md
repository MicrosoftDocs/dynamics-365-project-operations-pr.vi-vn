---
title: Cột mốc mô tả hợp đồng phụ
description: Chủ đề này giải thích cách tạo và duy trì lịch hóa đơn dựa trên cột mốc cho hợp đồng phụ với nhà cung cấp.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3301e5a627e4842009fcd5e352f1b76fd3053ee3
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323802"
---
# <a name="subcontract-line-milestones"></a>Cột mốc mô tả hợp đồng phụ

[!include [banner](../../includes/dataverse-preview.md)]

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Trong Dynamics 365 Project Operations, một phần mô tả hợp đồng phụ có phương thức thanh toán giá cố định có thể chỉ định lịch hóa đơn dựa trên cột mốc với nhà cung cấp.

Các cột mốc để lập hóa đơn cho nhà cung cấp có thể được tạo tự động bằng cách sử dụng tần suất đã đặt hoặc bạn có thể tạo chúng theo cách thủ công.

## <a name="automatically-create-a-milestone-based-invoice-schedule-for-a-subcontract-line"></a>Tự động tạo lịch hóa đơn dựa trên cột mốc cho một mô tả hợp đồng phụ

Hoàn thành các bước sau để tự động tạo lịch hóa đơn dựa trên cột mốc cho một nhóm cột mốc cố định được phân bổ đều.

1. Đi đến **Cài đặt** > **Tần suất hóa đơn** và thiết lập tần suất xuất hóa đơn cho các mô tả hợp đồng phụ.
2. Mở trang **Hợp đồng phụ**, mở hợp đồng phụ mà bạn muốn làm việc, sau đó mở mô tả hợp đồng phụ giá cố định mà bạn sẽ tạo lịch biểu cột mốc.
3. Trên tab **Cột mốc mô tả hợp đồng phụ**, chọn **Tạo các cột mốc định kỳ**.
4. Trong hộp thoại, hãy nhập hoặc chọn phạm vi ngày, số cột mốc và tần suất lập hóa đơn. Bạn có thể chọn ngày bắt đầu hoặc bạn có thể chọn số cột mốc và tần suất lập hóa đơn hoặc ngày bắt đầu hoặc bạn có thể chọn ngày kết thúc và tần suất lập hóa đơn. Bạn không thể chọn ngày kết thúc và số cột mốc.
Sử dụng thông tin này, hệ thống tạo ra các cột mốc và bản ghi được hiển thị trong lưới **Cột mốc**.

   - **Tên cột mốc** - Tên của cột mốc được đặt thành ngày của cột mốc dựa trên tần suất lập hóa đơn.
   - **Ngày cột mốc** - Ngày dựa trên tần suất lập hóa đơn.
   - **Số tiền cột mốc** - Được tính bằng cách chia tổng số tiền trên mô tả hợp đồng phụ cho số cột mốc.

Nếu mô tả hợp đồng phụ có giá trị trong trường **Số tiền thuế ước tính**, giá trị này được cộng vào mỗi cột mốc như nhau khi tạo các cột mốc định kỳ.

Tổng số tiền của cột mốc trên mô tả hợp đồng phụ phải bằng giá trị của mô tả hợp đồng phụ. Nếu không, điều đó nghĩa là đã xảy ra lỗi. Bạn có thể sửa lỗi và xác minh rằng tổng cột mốc bằng với giá trị mô tả hợp đồng phụ bằng cách tạo, chỉnh sửa hoặc xóa cột mốc và số tiền thuế. Sau khi thực hiện các thay đổi, hãy lưu và làm mới trang để đảm bảo rằng không còn lỗi nào nữa.

## <a name="manually-create-subcontract-line-milestones"></a>Tạo các cột mốc mô tả hợp đồng phụ theo cách thủ công

Các cột mốc giá cố định trên một mô tả hợp đồng phụ có thể được tạo theo cách thủ công khi chúng không được phân chia theo định kỳ. Để tạo cột mốc mô tả hợp đồng phụ, hãy hoàn thành các bước sau.

1. Trên ngăn điều hướng, chọn **Hợp đồng phụ** và mở hợp đồng phụ mà bạn muốn làm việc.
2. Mở mô tả hợp đồng phụ giá cố định mà bạn muốn tạo cột mốc.
3. Trên tab **Cột mốc mô tả hợp đồng phụ**, trên lưới phụ, hãy chọn **+ Cột mốc mô tả hợp đồng phụ mới**.
4. Trên trang **Cột mốc mô tả hợp đồng phụ mới**, nhập thông tin cần thiết dựa trên bảng sau.

    | Trường | Mô tả |
    | --- | --- |
    | Tên mốc | Tên mốc thời gian. |
    | Mô tả | Mô tả về cột mốc.  |
    | Ngày cột mốc | Ngày mà quá trình tạo hóa đơn tự động cần tìm trạng thái của cột mốc này để xem xét cho việc lập hóa đơn. Giá trị này được bao gồm trên dòng hóa đơn của nhà cung cấp khi lập hóa đơn cho hợp đồng phụ này. |
    | Số lượng | Số tiền hay giá trị của mốc mà hóa đơn cho khách hàng sẽ được lập theo đó. Giá trị này được bao gồm trên dòng hóa đơn của nhà cung cấp khi lập hóa đơn cho hợp đồng phụ này. |
    | Thuế | Số tiền thuế được áp cho mốc. Giá trị này được bao gồm trên dòng hóa đơn của nhà cung cấp khi lập hóa đơn cho hợp đồng phụ này. |
    | Số tiền sau thuế | Trường chỉ đọc này được tính là Số tiền + Thuế. Giá trị này được bao gồm trên dòng hóa đơn của nhà cung cấp khi lập hóa đơn cho hợp đồng phụ này. |
    | Tình trạng hóa đơn | Khi cột mốc được tạo, trạng thái này luôn được đặt thành **Chưa sẵn sàng để lập hóa đơn**.  Khi trạng thái là **Sẵn sàng lập hóa đơn**, việc tạo hóa đơn của nhà cung cấp bao gồm cột mốc này trên hóa đơn của nhà cung cấp. |

5. Chọn **Lưu và Đóng**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
