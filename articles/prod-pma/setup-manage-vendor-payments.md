---
title: Thiết lập và sử dụng các khoản thanh toán của nhà cung cấp trả khi được trả tiền
description: Chủ đề này giải thích cách tạo các điều khoản trả khi được trả tiền (PWP) để bạn có thể giải phóng một phần khoản thanh toán cho nhà cung cấp, dựa trên các khoản thanh toán của khách hàng.
author: RadhikaRS
manager: AnnBe
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: f2469c8396eb4867b435f70b046aa421552d0fa1
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288629"
---
# <a name="set-up-and-use-pay-when-paid-vendor-payments"></a>Thiết lập và sử dụng các khoản thanh toán của nhà cung cấp trả khi được trả tiền

[!include [banner](../includes/banner.md)]

Khi bạn chấp thuận một nhà cung cấp làm việc với tư cách là nhà thầu phụ, bạn có thể muốn giữ lại khoản thanh toán cho nhà cung cấp cho đến khi khách hàng của bạn trả tiền cho bạn cho dự án. Để hỗ trợ tình huống này, bạn có thể thiết lập các điều khoản trả khi được trả tiền (PWP) khi bạn thiết lập đơn đặt hàng (PO) với nhà cung cấp.

Ví dụ: khi khách hàng thanh toán một số tiền trên hóa đơn dự án, bạn có thể giải phóng một số hoặc tất cả số tiền trên hóa đơn của nhà cung cấp. Chỉ cần thiết lập các điều khoản PWP chỉ định rằng nhà cung cấp sẽ được thanh toán sau khi bạn nhận được phần trăm khoản thanh toán liên quan từ khách hàng. Nếu bạn nhận được một phần thanh toán từ khách hàng, bạn có thể xuất một số hóa đơn của nhà cung cấp có liên quan để thanh toán theo cách thủ công.

Ví dụ sau đây phác thảo quy trình khi các điều khoản PWP được sử dụng.

## <a name="example"></a>Ví dụ:

Tổ chức của bạn đồng ý cung cấp cho khách hàng 100 máy tính đã được cài đặt phần mềm, với giá 150 đô la Mỹ (USD) cho mỗi máy tính. Sau đó, bạn thuê một nhà cung cấp để cung cấp cho bạn những máy tính đã được cài đặt phần mềm. Theo thỏa thuận, khách hàng phải phê duyệt chất lượng của máy tính trước khi trả tiền cho tổ chức của bạn. Chính sách của tổ chức bạn là giữ lại khoản thanh toán cho các nhà cung cấp cho đến khi khách hàng đã thanh toán cho bạn. Do đó, bạn thiết lập dự án sao cho có tỷ lệ PWP là 100 phần trăm.

Nhà cung cấp gửi cho bạn 100 máy tính đã cài đặt phần mềm cùng với hóa đơn 10.000 USD. Vì các điều khoản PWP được thiết lập cho dự án của bạn, bạn không phải trả tiền cho nhà cung cấp khi nhận máy tính. Thay vào đó, bạn gửi máy tính cho khách hàng cùng với hóa đơn 15.000. Khách hàng kiểm tra máy tính và duyệt toàn bộ số tiền của hóa đơn dự án.

Sau khi bạn nhận được khoản thanh toán đầy đủ từ khách hàng, bạn thanh toán 10.000 cho nhà cung cấp, toàn bộ số tiền trong hóa đơn của nhà cung cấp.

## <a name="set-up-pwp-terms-for-a-project"></a>Thiết lập các điều khoản PWP cho một dự án

Khi bạn thiết lập các điều khoản PWP cho một dự án, bạn phải chỉ định, theo tỷ lệ phần trăm, số tiền tối thiểu mà khách hàng phải trả cho bạn cho dự án trước khi bạn trả tiền cho nhà cung cấp. Số tiền ngưỡng được tính toán tự động trên các hóa đơn của khách hàng cho dự án. Làm theo các bước sau để thiết lập tỷ lệ phần trăm ngưỡng cho các điều khoản PWP.

1. Chuyển đến **Quản lý dự án và kế toán** \> **Dự án** \> **Tất cả dự án**.
2. Tìm và mở dự án mà bạn muốn thiết lập các điều khoản PWP.
3. Trên FastTab **Thỏa thuận của nhà cung cấp**, hãy chọn **Thêm dòng**.
3. Trong trường **Mã tài khoản**, hãy chọn một trong các tùy chọn sau:

    - **Bảng** – Các điều khoản PWP được áp dụng cho một nhà cung cấp.
    - **Nhóm** – Các điều khoản PWP được áp dụng cho tất cả các nhà cung cấp trong một nhóm nhà cung cấp.
    - **Tất cả** – Các điều khoản PWP được áp dụng cho tất cả các nhà cung cấp.

4. Nếu bạn đã chọn **Bảng** hoặc **Nhóm** trong bước trước, trong trường **Nhà cung cấp/Nhóm nhà cung cấp**, hãy chọn nhà cung cấp hoặc nhóm nhà cung cấp được áp dụng các điều khoản PWP. Nếu bạn đã chọn **Tất cả** trong bước trước, bạn không thể chỉnh sửa trường **Nhà cung cấp/Nhóm nhà cung cấp**.
5. Nếu điều khoản giữ khoản thanh toán cho nhà cung cấp được thiết lập cho nhà cung cấp trong dự án, trong trường **Điều khoản giữ khoản thanh toán cho nhà cung cấp**, chọn ID quy tắc cho các điều khoản giữ khoản thanh toán.
6. Trong trường **Phần trăm ngưỡng PWP**, nhập tỷ lệ phần trăm ngưỡng cho dự án. Tỷ lệ phần trăm mà bạn nhập cho dự án xác định số tiền tối thiểu mà khách hàng phải trả cho bạn trước khi bạn trả tiền cho nhà cung cấp.

## <a name="create-a-po-that-has-pwp-terms"></a>Tạo một đơn đặt hàng có các điều khoản PWP

Khi bạn đăng hóa đơn từ một nhà cung cấp, nếu nhà cung cấp phải tuân theo các điều khoản PWP, các điều khoản đó sẽ được hiển thị trên mô tả đơn đặt hàng. Để tạo một đơn đặt hàng có các điều khoản PWP, hãy làm theo các bước sau.

1. Đi đến **Thu mua và tìm nguồn cung ứng** \> **Đơn đặt hàng** \> **Tất cả đơn đặt hàng**.
2. Ở ngăn Hành động, chọn **Mới**. Sau đó, trong hộp thoại **Tạo đơn đặt hàng**, nhập thông tin cần thiết và chọn **OK**.

    Ngoài ra, hãy mở một đơn đặt hàng hiện có trên trang danh sách **Tất cả đơn đặt hàng**.

4. Trên trang **Đơn đặt hàng**, trên FastTab **Mô tả đơn đặt hàng**, xem lại chi tiết mô tả đơn đặt hàng cho nhà cung cấp. Tùy chọn **Trả khi được trả tiền** tự động được chọn và giá trị trong trường **Tỷ lệ phần trăm ngưỡng PWP** tự động được sao chép từ trường **Tỷ lệ phần trăm ngưỡng PWP** trên trang **Dự án**.
6. Nếu bạn không muốn áp dụng các điều khoản PWP cho nhà cung cấp cho một mô tả đơn đặt hàng, hãy bỏ chọn tùy chọn **Trả khi được trả tiền**. Trong trường hợp này, **Tỷ lệ phần trăm ngưỡng PWP** cho mô tả đơn đặt hàng sẽ được đặt lại thành 0 (không).

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Cập nhật khoản thanh toán của khách hàng và thanh toán cho nhà cung cấp

Khi một nhà cung cấp hoàn thành công việc của mình trên một dự án và gửi cho bạn hóa đơn, bạn phải xem lại tình trạng dự án và hóa đơn của khách hàng để xác định xem các điều khoản PWP đã được đáp ứng cho dự án hay chưa. Nếu các điều khoản PWP dành cho nhà cung cấp được đáp ứng, bạn có thể xác định mô tả nào trên hóa đơn nhà cung cấp cần thanh toán, dựa trên các khoản thanh toán của khách hàng cho dự án. Nếu bạn quyết định thanh toán cho nhà cung cấp mặc dù các điều khoản PWP không được đáp ứng, bạn có thể ghi đè các điều khoản PWP trên trang **Hóa đơn của nhà cung cấp có điều khoản trả khi được trả tiền**.

1. Đi đến **Quản lý dự án và kế toán** \> **Yêu cầu và báo cáo** \> **Yêu cầu giữ lại khoản thanh toán** \> **Hóa đơn của nhà cung cấp có điều khoản trả khi được trả tiền**.
2. Trên trang **Hóa đơn của nhà cung cấp có điều khoản trả khi được trả tiền**, trong trường tìm kiếm, hãy nhập các giá trị để tìm hóa đơn của nhà cung cấp mà bạn muốn xem lại, sau đó chọn **Tìm kiếm**.
3. Trên FastTab **Mô tả hóa đơn của nhà cung cấp**, hãy chọn các mô tả mà bạn muốn thay đổi.
4. Nếu điều kiện **Trả khi được trả tiền** được đáp ứng cho mô tả hóa đơn, hãy chọn **Thanh toán cho nhà cung cấp**. Tùy chọn **Trả khi được trả tiền** được bỏ chọn và giá trị của trường **Sẵn sàng thanh toán** được thay đổi thành **Có**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]