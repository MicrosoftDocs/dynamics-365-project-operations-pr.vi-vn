---
title: Xác minh các hóa đơn của nhà cung cấp bằng số liệu thực tế đã được phê duyệt
description: Bài viết này giải thích cách Microsoft Dynamics 365 Project Operations cho phép người quản lý dự án xác minh hóa đơn của nhà cung cấp với các số liệu thực tế đã được phê duyệt khi các nhà thầu thực hiện công việc và thời gian được ghi lại, cũng như các chi phí và vật tư được các thành viên nhóm dự án sử dụng.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 67e0a0143fa354ca9a87bfac5fbbd6306a97811c
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522958"
---
# <a name="verification-of-vendor-invoices-with-approved-actuals"></a>Xác minh các hóa đơn của nhà cung cấp bằng số liệu thực tế đã được phê duyệt

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Microsoft Dynamics 365 Project Operations cho phép người nhà quản lý dự án xác minh các mô tả hóa đơn của nhà cung cấp theo những cách sau:

- Sử dụng trường **Trạng thái xác minh** trên mô tả hóa đơn của nhà cung cấp.
- Nếu mô tả hóa đơn của nhà cung cấp tham chiếu đến mô tả hợp đồng phụ, hãy liên kết chi phí thực tế từ hoạt động của nhà thầu phụ với những mô tả hóa đơn của nhà cung cấp đó. Liên kết được tạo bằng cách đối sánh chi phí thực tế với mô tả hóa đơn của nhà cung cấp.

    > [!NOTE]
    > Mặc dù trạng thái xác minh có thể được theo dõi đối với mô tả hóa đơn của nhà cung cấp không tham chiếu đến hợp đồng phụ, nhưng chi phí thực tế không thể được liên kết với những mô tả hóa đơn của nhà cung cấp đó.

## <a name="verification-status"></a>Trạng thái xác minh

Trường **Trạng thái xác minh** trên một mô tả hóa đơn của nhà cung cấp cho biết trạng thái xác minh đó. Các trạng thái sau được hỗ trợ:

1. Chưa bắt đầu
2. Đang tiến hành
3. Hoàn tất

Các mô tả hóa đơn của nhà cung cấp có trạng thái xác minh là **Chưa bắt đầu** đều có thể được chỉnh sửa.

Các mô tả hóa đơn của nhà cung cấp có trạng thái xác minh là **Đang tiến hành** không thể chỉnh sửa nữa. Đối với dòng hóa đơn của nhà cung cấp tham chiếu đến hợp đồng phụ, trạng thái xác minh được đặt tự động thành **Đang tiến hành** ngay sau khi chi phí thực tế đầu tiên được khớp với mô tả hóa đơn của nhà cung cấp.

Các mô tả hóa đơn của nhà cung cấp có trạng thái xác minh là **Hoàn thành** không thể chỉnh sửa nữa. Khi tất cả các mô tả trên hóa đơn của nhà cung cấp có trạng thái xác minh này, hóa đơn của nhà cung cấp có thể được xác nhận.

## <a name="match-cost-actuals-to-vendor-invoice-lines"></a>Khớp chi phí thực tế với mô tả hóa đơn của nhà cung cấp

Việc khớp chi phí thực tế với quá trình xác minh trên mô tả hóa đơn của nhà cung cấp. Để khớp chi phí thực tế với mô tả hóa đơn của nhà cung cấp, hãy làm theo các bước sau.

1. Mở mô tả hóa đơn của nhà cung cấp và chọn tab **Số liệu thực tế về chi phí không khớp**. Một lưới hiển thị danh sách các chi phí thực tế có tham chiếu đến cùng một mô tả hợp đồng phụ với mô tả hóa đơn của nhà cung cấp.
2. Chọn một hoặc nhiều chi phí thực tế, sau đó chọn **Khớp** trên thanh công cụ phía trên lưới. Hệ thống xác thực rằng chi phí thực tế đã chọn có thể khớp với nhau. Sau khi xác thực được thông qua, chi phí thực tế được liên kết với mô tả hóa đơn của nhà cung cấp.

### <a name="validation-criteria-that-are-used-to-link-cost-actuals-to-vendor-invoice-lines"></a>Tiêu chí xác thực được sử dụng để liên kết chi phí thực tế với mô tả hóa đơn của nhà cung cấp

Trong quá trình đối sánh, liên kết giữa chi phí thực tế và mô tả hóa đơn của nhà cung cấp chỉ có thể được thiết lập nếu cả hai điều kiện sau được đáp ứng:

- Trường **Trạng thái điều chỉnh** cho mọi chi phí thực tế đã chọn phải để trống. Nói cách khác, chi phí thực tế phải không được thay thế bằng các chi phí thực tế khác trong quá trình thu hồi, hủy bỏ phê duyệt hoặc nhật ký chỉnh sửa.
- Giá trị của các trường sau đây được khớp giữa mô tả hóa đơn của nhà cung cấp và chi phí thực tế đã chọn. Nếu bất kỳ trường nào không được đặt trên mô tả hóa đơn của nhà cung cấp, thì trường đó không được coi là khớp.

    - Hợp đồng dự án
    - Mô tả hợp đồng dự án
    - Lớp giao dịch
    - Dự án
    - Tác vụ
    - Thể loại nguồn lực
    - Thể loại giao dịch
    - Sản phẩm
    - Mô tả hợp đồng phụ
    - Nguồn lực có thể đặt trước

## <a name="unmatch-cost-actuals-from-a-vendor-invoice-line"></a>Hủy khớp chi phí thực tế trên mô tả hóa đơn của nhà cung cấp

Việc hủy khớp chi phí thực tế cũng có thể hỗ trợ quá trình xác minh trên hóa đơn của nhà cung cấp bằng cách cho phép loại bỏ các liên kết được thiết lập trước đó. Chỉ có thể hủy khớp chi phí thực tế trên mô tả hóa đơn của nhà cung cấp có trạng thái xác minh là **Đang tiến hành**. Để hủy khớp chi phí thực tế trên mô tả hóa đơn của nhà cung cấp, hãy làm theo các bước sau.

1. Mở mô tả hóa đơn của nhà cung cấp và chọn tab **Chi phí thực tế không khớp**. Một lưới hiển thị danh sách các chi phí thực tế có tham chiếu đến cùng một mô tả hợp đồng phụ với mô tả hóa đơn của nhà cung cấp.
2. Chọn một hoặc nhiều chi phí thực tế, sau đó chọn **Bỏ so khớp** trên thanh công cụ phía trên lưới.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
