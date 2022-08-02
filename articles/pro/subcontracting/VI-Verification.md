---
title: Xác minh các hóa đơn của nhà cung cấp bằng số liệu thực tế đã được phê duyệt
description: Bài viết này giải thích cách Microsoft Dynamics 365 Project Operations hãy để các nhà quản lý dự án xác minh hóa đơn của nhà cung cấp với các thực tế đã được phê duyệt khi các nhà thầu thực hiện công việc và thời gian được ghi lại, cũng như các chi phí và vật liệu được các thành viên trong nhóm dự án sử dụng.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7bf48dd17063daece5df3ce44c0375eec3dc3cae
ms.sourcegitcommit: 49c2a668b8d7bf0acb9e9b0bb44687e6d3dcaa8c
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 07/28/2022
ms.locfileid: "9204201"
---
# <a name="verification-of-vendor-invoices-with-approved-actuals"></a>Xác minh các hóa đơn của nhà cung cấp bằng số liệu thực tế đã được phê duyệt

[!include [banner](../../includes/dataverse-preview.md)]

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Microsoft Dynamics 365 Project Operations hãy để các nhà quản lý dự án xác minh các dòng hóa đơn của nhà cung cấp theo những cách sau:

- Sử dụng **Tình trạng xác minh** trên các dòng hóa đơn của nhà cung cấp.
- Nếu các dòng hóa đơn của nhà cung cấp tham chiếu đến dòng hợp đồng phụ, hãy liên kết thực tế chi phí từ hoạt động của nhà thầu phụ với các dòng hóa đơn của nhà cung cấp đó. Liên kết được tạo bằng cách đối sánh các thực tế chi phí với các dòng hóa đơn của nhà cung cấp.

    > [!NOTE]
    > Mặc dù có thể theo dõi trạng thái xác minh đối với các dòng hóa đơn của nhà cung cấp không tham chiếu đến hợp đồng phụ, nhưng thực tế chi phí không thể được liên kết với các dòng hóa đơn của nhà cung cấp đó.

## <a name="verification-status"></a>Tình trạng xác minh

Các **Tình trạng xác minh** trên một dòng hóa đơn của nhà cung cấp cho biết trạng thái xác minh đó. Các trạng thái sau được hỗ trợ:

1. Chưa bắt đầu
2. Đang tiến hành
3. Hoàn tất

Các dòng hóa đơn của nhà cung cấp có trạng thái xác minh là **Chưa bắt đầu** có thể được chỉnh sửa.

Các dòng hóa đơn của nhà cung cấp có trạng thái xác minh là **Trong tiến trình** không còn có thể được chỉnh sửa. Đối với dòng hóa đơn của nhà cung cấp tham chiếu đến hợp đồng phụ, trạng thái xác minh sẽ tự động được đặt thành **Trong tiến trình** ngay sau khi chi phí thực tế đầu tiên được khớp với dòng hóa đơn của nhà cung cấp.

Các dòng hóa đơn của nhà cung cấp có trạng thái xác minh là **Hoàn thành** không còn có thể được chỉnh sửa. Khi tất cả các dòng trên hóa đơn của nhà cung cấp có trạng thái xác minh này, hóa đơn của nhà cung cấp có thể được xác nhận.

## <a name="match-cost-actuals-to-vendor-invoice-lines"></a>Khớp các thực tế chi phí với các dòng hóa đơn của nhà cung cấp

Việc so khớp các thực tế về chi phí giúp cho quá trình xác minh trên một dòng hóa đơn của nhà cung cấp. Để khớp các thực tế chi phí với một dòng hóa đơn của nhà cung cấp, hãy làm theo các bước sau.

1. Mở dòng hóa đơn của nhà cung cấp và chọn **Chi phí thực tế chưa từng có** chuyển hướng. Một lưới hiển thị danh sách các thực tế chi phí tham chiếu đến cùng một dòng hợp đồng phụ với dòng hóa đơn của nhà cung cấp.
2. Chọn một hoặc nhiều thực tế chi phí, sau đó chọn **Cuộc thi đấu** trên thanh công cụ phía trên lưới. Hệ thống xác nhận rằng các thực tế chi phí đã chọn có thể khớp với nhau. Sau khi xác thực được thông qua, các chi phí thực tế được liên kết với dòng hóa đơn của nhà cung cấp.

### <a name="validation-criteria-that-are-used-to-link-cost-actuals-to-vendor-invoice-lines"></a>Tiêu chí xác thực được sử dụng để liên kết các thực tế chi phí với các dòng hóa đơn của nhà cung cấp

Trong quá trình đối sánh, liên kết giữa chi phí thực tế và dòng hóa đơn của nhà cung cấp chỉ có thể được thiết lập nếu cả hai điều kiện sau được đáp ứng:

- Các **Tình trạng điều chỉnh** trường cho mọi chi phí thực tế đã chọn phải để trống. Nói cách khác, các sổ kế toán chi phí không được thay thế bằng các sổ kế toán chi phí khác trong quá trình thu hồi, hủy bỏ phê duyệt hoặc nhật ký sửa chữa.
- Giá trị của các trường sau được khớp giữa dòng hóa đơn của nhà cung cấp và chi phí thực tế đã chọn. Nếu bất kỳ trường nào không được đặt trên dòng hóa đơn của nhà cung cấp, thì trường đó không được coi là phù hợp.

    - Hợp đồng dự án
    - Mô tả hợp đồng dự án
    - Lớp giao dịch
    - Dự án
    - Tác vụ
    - Loại tài nguyên
    - Thể loại giao dịch
    - Sản phẩm
    - Dòng hợp đồng phụ
    - Nguồn lực có thể đặt trước

## <a name="unmatch-cost-actuals-from-a-vendor-invoice-line"></a>Khớp các thực tế chi phí từ một dòng hóa đơn của nhà cung cấp

Việc so khớp các thực tế về chi phí cũng có thể giúp thực hiện quá trình xác minh trên hóa đơn của nhà cung cấp bằng cách cho phép xóa các liên kết đã thiết lập trước đó. Chỉ có thể so khớp thực tế chi phí từ các dòng hóa đơn của nhà cung cấp có trạng thái xác minh là **Trong tiến trình**. Để bỏ khớp các thực tế chi phí khỏi dòng hóa đơn của nhà cung cấp, hãy làm theo các bước sau.

1. Mở dòng hóa đơn của nhà cung cấp và chọn **Thực tế chi phí phù hợp** chuyển hướng. Lưới hiển thị danh sách các thực tế chi phí tham chiếu đến dòng hóa đơn của nhà cung cấp.
2. Chọn một hoặc nhiều thực tế chi phí, sau đó chọn **Hủy Kết Nối** trên thanh công cụ phía trên lưới.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
