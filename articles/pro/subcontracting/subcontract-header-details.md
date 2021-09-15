---
title: Chi tiết tiêu đề cho các hợp đồng phụ
description: Chủ đề này giải thích chức năng được cung cấp trên tiêu đề hợp đồng phụ trong Project Operations.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 49158af1a430033db3a5db57a840512c45bc17e2
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323667"
---
# <a name="header-details-for-subcontracts"></a>Chi tiết tiêu đề cho các hợp đồng phụ

[!include [banner](../../includes/dataverse-preview.md)]

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Chủ đề này giải thích chức năng được cung cấp trên tiêu đề hợp đồng phụ trong Dynamics 365 Project Operations.

Khi Người quản lý dự án lập kế hoạch và thực hiện các dự án, họ có thể thuê các nhà thầu phụ cũng như mua các sản phẩm và dịch vụ từ các nhà cung cấp. Khi Người quản lý dự án cần mua sản phẩm hoặc dịch vụ, họ có thể tạo hợp đồng phụ trong Project Operations.

Để tạo hợp đồng phụ, hãy hoàn thành các bước sau.

1. Trong ngăn điều hướng, hãy chọn **Hợp đồng phụ**, và trên trang **Hợp đồng phụ**, chọn **Mới**.
2. Nhập các thông tin cần thiết, sau đó chọn **Lưu**.

    Bảng sau cung cấp thông tin về các trường trên trang tiêu đề Hợp đồng phụ.

    | **Trường** | **Mô tả** |
    | --- | --- | 
    | Tên | Tên của hợp đồng phụ. |
    | Mô tả | Mô tả ngắn gọn về các dịch vụ và sản phẩm đang được mua trên hợp đồng phụ. |
    | Nhà cung cấp | Tên của công ty mà các sản phẩm và dịch vụ đang được mua. Bản ghi khách hàng này có kiểu quan hệ là **Nhà cung cấp** hoặc **Nhà cung ứng**. |
    | Ngày tạo hợp đồng phụ | Ngày hợp đồng phụ được tạo. |
    | Lý do cho trạng thái | Trạng thái của hợp đồng phụ. |
    | Tiền tệ | Đơn vị tiền tệ mà sản phẩm và dịch vụ được mua. Giá trị trong trường này được mặc định từ tài khoản nhà cung cấp nhưng có thể thay đổi. Bảng giá dự án được sử dụng để định giá sản phẩm và dịch vụ trên hợp đồng phụ phải bằng đơn vị tiền tệ này. Bảng giá bằng bất kỳ đơn vị tiền tệ nào khác không được liên kết với hợp đồng phụ. Giá thành của sản phẩm và dịch vụ phát sinh trên hợp đồng phụ này sẽ được ghi nhận vào dự án bằng đơn vị tiền tệ này. |
    | Đơn vị theo hợp đồng | Bộ phận của công ty đang ký kết hợp đồng mua bán hoặc hợp đồng phụ với nhà cung cấp. |
    | Điều khoản thanh toán | Các điều khoản thanh toán trên hóa đơn của nhà cung cấp được phát hành trên hợp đồng phụ này. Giá trị trong trường này được mặc định từ bản ghi tài khoản nhà cung cấp. |
    | Địa chỉ thanh toán | Địa chỉ nơi thanh toán trên hóa đơn của nhà cung cấp được gửi. Giá trị trong trường này được mặc định từ bản ghi tài khoản nhà cung cấp. |
    | Tên người nhận hóa đơn | Tên của người hoặc bộ phận trong công ty của nhà cung cấp sẽ gửi hóa đơn. Giá trị trong trường này được mặc định từ bản ghi tài khoản nhà cung cấp và sẽ được sử dụng làm tên của người liên hệ chính trên hóa đơn nhà cung cấp được tạo cho hợp đồng phụ này. |
    | Địa chỉ nhận hóa đơn | Địa chỉ được sử dụng trên hóa đơn từ nhà cung cấp này. Giá trị trong trường này được mặc định từ bản ghi tài khoản nhà cung cấp. Địa chỉ này cũng được sử dụng làm hóa đơn từ địa chỉ trên hóa đơn của nhà cung cấp được tạo cho hợp đồng phụ này. |
    | Tổng con | Nếu hợp đồng phụ không có mô tả, hãy nhập một giá trị vào trường này biểu thị tổng phụ của đơn hàng trước thuế. Nếu hợp đồng phụ có mô tả, thì trường này chỉ đọc được. Số tiền được hiển thị là tổng số tiền từ tất cả các dòng mô tả trên hợp đồng phụ. |
    | Tổng thuế | Nếu hợp đồng phụ không có mô tả, hãy nhập một giá trị vào trường này biểu thị thuế trên hợp đồng phụ này. Nếu hợp đồng phụ có mô tả, thì trường này chỉ đọc được. Số tiền được hiển thị là tổng số tiền thuế từ tất cả các dòng mô tả trên hợp đồng phụ. |
    | Tổng số tiền |  Trường được tính toán này hiển thị tổng số tiền của hợp đồng phụ sau khi đã bao gồm thuế.  |
    | Ngày đã xác nhận | Ngày hợp đồng phụ đã được xác nhận.  |
    | Người yêu cầu | Giá trị trong trường này mặc định là tên của người dùng tạo hợp đồng phụ. Giá trị này có thể được thay đổi bởi người tạo hợp đồng phụ để cho biết người đó thay mặt họ tạo hợp đồng phụ.  |
    | Người quản lý tài khoản nhà cung cấp | Tên của người liên hệ chính của tài khoản nhà cung cấp. Giá trị trong trường này được mặc định từ bản ghi tài khoản nhà cung cấp. Người dùng có thể thay đổi giá trị trường này để chọn một địa chỉ liên hệ khác làm người quản lý tài khoản nhà cung cấp của hợp đồng phụ. Thông báo qua email và thương lượng giá có thể được đặt cấu hình và gửi bởi người liên hệ này. |


