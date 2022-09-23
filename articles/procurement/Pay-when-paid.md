---
title: Thanh toán khi thanh toán của nhà cung cấp đã thanh toán
description: Chủ đề này giải thích cách sử dụng kịch bản trả tiền khi được trả tiền (PWP).
author: mukumarm
ms.date: 08/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: mukumarm
ms.openlocfilehash: d1fe8d92663b31b22dc405fc1f3e06d976e6c5dc
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 09/16/2022
ms.locfileid: "9525396"
---
# <a name="pay-when-paid-vendor-payments"></a>Thanh toán khi thanh toán của nhà cung cấp đã thanh toán

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Chủ đề này giải thích cách sử dụng kịch bản trả tiền khi được trả tiền (PWP).

## <a name="create-a-purchase-order-that-has-pwp-terms"></a>Tạo đơn đặt hàng có các điều khoản PWP

Khi bạn đăng hóa đơn từ một nhà cung cấp, nếu nhà cung cấp phải tuân theo các điều khoản PWP, thì các điều khoản đó sẽ được hiển thị trên các dòng đơn đặt hàng (PO). Để tạo một đơn đặt hàng có các điều khoản PWP, hãy làm theo các bước sau.

1. Trong Microsoft Dynamics 365 Finance, hãy làm theo một trong các bước sau:

    - Đi đến **Thu mua và tìm nguồn cung ứng** \> **Đơn đặt hàng** \> **Tất cả đơn đặt hàng**. Ở ngăn Hành động, chọn **Mới**. Bên trong **Tạo đơn đặt hàng** hộp thoại, chọn nhà cung cấp mà các điều khoản PWP được thiết lập trên dự án, nhập thông tin cần thiết khác, sau đó chọn **ĐƯỢC RỒI**.
    - Chuyển đến **Quản lý dự án và kế toán** \> **Dự án** \> **Tất cả dự án**. Trên Ngăn hành động, trên **Quản lý** tab, chọn **Nhiệm vụ hạng mục**. Chọn đơn đặt hàng. Chọn nhà cung cấp mà các điều khoản PWP được thiết lập trên dự án, sau đó chọn **ĐƯỢC RỒI**.

2. Trên **Đơn đặt hàng** trang, trên **Mua hàng** Tab nhanh, chọn **Thêm dòng** để tạo một dòng đặt hàng.
3. Chọn số mặt hàng hoặc danh mục mua sắm, và nhập các chi tiết bắt buộc khác. Xem lại chi tiết của dòng PO cho nhà cung cấp.

    Tùy chọn **Trả khi được trả tiền** tự động được chọn và giá trị trong trường **Tỷ lệ phần trăm ngưỡng PWP** tự động được sao chép từ trường **Tỷ lệ phần trăm ngưỡng PWP** trên trang **Dự án**.

4. Nếu bạn không muốn áp dụng các điều khoản PWP cho nhà cung cấp cho một mô tả đơn đặt hàng, hãy bỏ chọn tùy chọn **Trả khi được trả tiền**. Trong trường hợp này, **Phần trăm ngưỡng PWP** trường cho dòng PO sẽ được đặt lại thành **0** (số không).
5. Trên **Đơn đặt hàng** trên Ngăn hành động, trên **Mua, tựa vào, bám vào** tab, chọn **Xác nhận** để xác nhận đơn đặt hàng.
6. Trên Ngăn hành động, trên **Hóa đơn** tab, chọn **Hóa đơn** để tạo hóa đơn cho đơn đặt hàng.

## <a name="create-a-project-invoice-proposal"></a>Tạo một đề xuất hóa đơn dự án

Đề xuất hóa đơn dự án được sử dụng để tạo hóa đơn dự án cho khách hàng. Trong kịch bản PWP, các khoản thanh toán của nhà cung cấp phụ thuộc vào các khoản thanh toán của khách hàng theo cài đặt PWP. Tuy nhiên, có các tùy chọn cho phép bạn giải phóng các khoản thanh toán mà không cần khách hàng thanh toán như bạn yêu cầu. Để tạo hóa đơn dự án cho khách hàng, hãy làm theo các bước sau.

1. Trong các ứng dụng tương tác với khách hàng, hãy chuyển đến **Dự án** \> **Dự án** và chọn dự án.
2. Trên **Thực tế**, hãy chọn dòng thực tế được tạo bởi PO có **Bán hàng chưa thanh toán** Loại giao dịch. Sau đó chọn **Sẵn sàng cho hóa đơn**.
3. Đi đến **Việc bán hàng** \> **Việc bán hàng** \> **Hợp đồng dự án**, và chọn hợp đồng dự án.
4. Trên Ngăn hành động, chọn **Hóa đơn** để tạo hóa đơn cho khách hàng.
5. Trong Tài chính, hãy chuyển đến **Quản lý dự án và kế toán** \> **Định kỳ** \> **Nhập từ bảng dàn** và chọn **ĐƯỢC RỒI** để tạo tạp chí tích hợp hoạt động Dự án.
6. Đi đến **Quản lý dự án và kế toán** \> **Hóa đơn dự án** \> **Đề xuất hóa đơn dự án** và chọn **Bưu kiện** để đăng đề xuất hóa đơn đã được tạo cho dự án.

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Cập nhật khoản thanh toán của khách hàng và thanh toán cho nhà cung cấp

Khi một nhà cung cấp hoàn thành công việc của mình trên một dự án và gửi cho bạn hóa đơn, bạn phải xem lại tình trạng dự án và hóa đơn của khách hàng để xác định xem các điều khoản PWP có được đáp ứng cho dự án hay không. Nếu các điều khoản PWP dành cho nhà cung cấp được đáp ứng, bạn có thể xác định mô tả nào trên hóa đơn nhà cung cấp cần thanh toán, dựa trên các khoản thanh toán của khách hàng cho dự án. Nếu bạn quyết định thanh toán cho nhà cung cấp mặc dù các điều khoản PWP không được đáp ứng, bạn có thể ghi đè các điều khoản PWP trên trang **Hóa đơn của nhà cung cấp có điều khoản trả khi được trả tiền**.

1. Trong Tài chính, hãy chuyển đến **Quản lý dự án và kế toán** \> **Dự án** \> **Tất cả các dự án** và chọn dự án.
2. Trên Ngăn hành động, chọn **Điều khiển**, và sau đó chọn **Hóa đơn của nhà cung cấp** để hiển thị tất cả các hóa đơn của nhà cung cấp đã được tạo cho dự án.
3. Trên trang **Hóa đơn của nhà cung cấp có điều khoản trả khi được trả tiền**, trong trường tìm kiếm, hãy nhập các giá trị để tìm hóa đơn của nhà cung cấp mà bạn muốn xem lại, sau đó chọn **Tìm kiếm**.
4. Chọn **Thanh toán khi thanh toán** tùy chọn chỉ xem hóa đơn PWP.
5. Trên **Các dòng hóa đơn của nhà cung cấp** Tab Nhanh, chọn các dòng mà bạn muốn phát hành để thanh toán.
6. Lựa chọn **Giải phóng thanh toán cho nhà cung cấp**. Tùy chọn **Trả khi được trả tiền** được bỏ chọn và giá trị của trường **Sẵn sàng thanh toán** được thay đổi thành **Có**.
