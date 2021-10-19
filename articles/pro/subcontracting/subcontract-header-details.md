---
title: Chi tiết tiêu đề cho các hợp đồng phụ
description: Chủ đề này giải thích chức năng được cung cấp trên tiêu đề hợp đồng phụ trong Project Operations.
author: rumant
ms.date: 09/14/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ee863d31b45e7de962488fe804202ddfe580eb04
ms.sourcegitcommit: 083e3d219cd5126eecb74debb1b70b361680b1f6
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 09/18/2021
ms.locfileid: "7501352"
---
# <a name="header-details-for-subcontracts"></a>Chi tiết tiêu đề cho các hợp đồng phụ

[!include [banner](../../includes/dataverse-preview.md)]

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Chủ đề này giải thích chức năng được cung cấp trên tiêu đề hợp đồng phụ trong Dynamics 365 Project Operations.

Khi Người quản lý dự án lập kế hoạch và thực hiện các dự án, họ có thể thuê các nhà thầu phụ cũng như mua các sản phẩm và dịch vụ từ các nhà cung cấp. Khi Người quản lý dự án cần mua sản phẩm hoặc dịch vụ, họ có thể tạo hợp đồng phụ trong Project Operations.

Để tạo hợp đồng phụ, hãy hoàn thành các bước sau.

1. Trong ngăn điều hướng, hãy chọn **Hợp đồng phụ**, và trên trang **Hợp đồng phụ**, chọn **Mới**.
2. Nhập các thông tin cần thiết, sau đó chọn **Lưu**.

    Bảng sau cung cấp thông tin về các trường trên trang **Tiêu đề hợp đồng phụ**.

    | Trường | Mô tả |Tác động chức năng |
    |---|------|---| 
    | Tên | Tên của hợp đồng phụ. | Trong tất cả danh sách thả xuống hợp đồng phụ, tên của hợp đồng phụ được liệt kê trong cột đầu tiên để giúp bạn xác định hợp đồng phụ. | 
    | Mô tả | Mô tả ngắn gọn về các dịch vụ và sản phẩm đang được mua trên hợp đồng phụ. | Không có |
    | Nhà cung cấp | Tên của công ty mà các sản phẩm và dịch vụ đang được mua. Bản ghi khách hàng này có kiểu quan hệ là **Nhà cung cấp** hoặc **Nhà cung ứng**. | Dựa trên nhà cung cấp được chọn, các giá trị mặc định được tự động nhập cho các trường sau:<br/> **• Tiền tệ** </br> **• Bảng giá** </br> **• Điều khoản thanh toán**</br> **• Địa chỉ thanh toán**</br> **• Địa chỉ nhận hóa đơn**</br> **• Tên nhận hóa đơn** </br>**• Người quản lý tài khoản nhà cung cấp**|
    | Ngày hợp đồng phụ | Ngày tạo hợp đồng phụ. | Ngày ký hợp đồng phụ được sử dụng để chọn đúng bảng giá mua từ các bảng giá được đính kèm với nhà cung cấp liên quan hoặc từ các tham số của dự án. |
    | Lý do cho trạng thái | Trạng thái của hợp đồng phụ. | Trạng thái xác định vị trí của hợp đồng phụ trong quy trình kinh doanh và liệu có thể chỉnh sửa hợp đồng đó hay không. <br/>Các giá trị bao gồm:<br>• **Bản nháp**: Hợp đồng phụ có thể được chỉnh sửa. Bạn chỉ có thể chỉnh sửa hợp đồng phụ có trạng thái **Bản nháp**.<br/>• **Đã xác nhận** : Việc thương lượng với nhà cung cấp đã hoàn tất và hợp đồng phụ được chấp thuận để giao hàng. <br/>• **Đã đóng** : Việc giao hàng trên hợp đồng phụ đã hoàn tất.<br/>• **Đã hủy** : Hợp đồng phụ đã bị hủy bỏ và không có kế hoạch giao hàng.  | 
    | Tiền tệ | Đơn vị tiền tệ mà sản phẩm và dịch vụ được mua. Giá trị mặc định được nhập tự động từ tài khoản nhà cung cấp, nhưng có thể thay đổi. | Đơn vị tiền tệ của hợp đồng phụ được sử dụng để chọn bảng giá mua từ các bảng giá được đính kèm với nhà cung cấp liên quan hoặc từ các tham số của dự án. Không thể liên kết bảng giá bằng đơn vị tiền tệ khác với hợp đồng phụ. Chi phí về thời gian, chi phí và nguyên vật liệu mà các nguồn lực của nhà cung cấp cung cấp từ hợp đồng phụ này được ghi nhận bằng đơn vị tiền tệ này trong dự án. Sau khi hồ sơ hợp đồng phụ được lưu, không thể thay đổi đơn vị tiền tệ của hợp đồng phụ.|
    | Đơn vị theo hợp đồng | Bộ phận của công ty đang ký kết hợp đồng mua bán hoặc hợp đồng phụ với nhà cung cấp. | Không có |
    | Điều khoản thanh toán | Các điều khoản thanh toán trên hóa đơn của nhà cung cấp được giải ngân trên hợp đồng phụ này. Giá trị mặc định được nhập tự động từ bản ghi tài khoản nhà cung cấp. | Các điều khoản thanh toán từ hợp đồng phụ được sao chép vào tất cả các hóa đơn của nhà cung cấp có liên quan đến hợp đồng phụ này. Điều khoản thanh toán có thể được cập nhật nếu hợp đồng phụ có trạng thái **Bản nháp**. | 
    | Địa chỉ thanh toán | Địa chỉ của nhà cung cấp mà các khoản thanh toán phải được gửi đến. Giá trị mặc định được nhập tự động từ bản ghi tài khoản nhà cung cấp. | Địa chỉ thanh toán từ hợp đồng phụ được sao chép làm địa chỉ thanh toán cho tất cả các hóa đơn của nhà cung cấp được tạo cho hợp đồng phụ này. Địa chỉ thanh toán có thể được cập nhật nếu hợp đồng phụ có trạng thái **Bản nháp**.|
    | Tên nhận hóa đơn | Tên của người hoặc bộ phận trong công ty của nhà cung cấp sẽ gửi hóa đơn. Giá trị mặc định được nhập tự động từ bản ghi tài khoản nhà cung cấp. | Giá trị **Tên nhận hóa đơn** từ hợp đồng phụ được sao chép vào tất cả các hóa đơn của nhà cung cấp có liên quan đến hợp đồng phụ này. Trường này có thể được cập nhật nếu hợp đồng phụ có trạng thái **Bản nháp**.|
    | Địa chỉ nhận hóa đơn | Địa chỉ được sử dụng trên hóa đơn từ nhà cung cấp. Giá trị mặc định được nhập tự động từ bản ghi tài khoản nhà cung cấp. | Địa chỉ này là địa chỉ "hóa đơn từ" trên các hóa đơn của nhà cung cấp được tạo cho hợp đồng phụ này. |
    | Tổng con | Nếu hợp đồng phụ không có mô tả, hãy nhập tổng phụ của đơn hàng trước thuế. Nếu hợp đồng phụ có mô tả, thì trường này chỉ đọc được. Số tiền được hiển thị là tổng phụ của tất cả các mô tả trên hợp đồng phụ. | Không có |
    | Tổng thuế | Nếu hợp đồng phụ không có mô tả, hãy nhập tổng số thuế của hợp đồng phụ này. Nếu hợp đồng phụ có mô tả, thì trường này chỉ đọc được. Số tiền được hiển thị là tổng số tiền thuế từ tất cả các mô tả trên hợp đồng phụ. | Không có |
    | Tổng số tiền | Trường được tính toán này hiển thị tổng số tiền của hợp đồng phụ sau khi đã bao gồm thuế. | Không có |
    | Ngày đã xác nhận | Ngày mà hợp đồng phụ được xác nhận. | Không có |
    | Người yêu cầu | Theo mặc định, trường này được đặt thành tên của người dùng tạo hợp đồng phụ. Tuy nhiên, người tạo hợp đồng phụ có thể thay đổi giá trị để cho người đó biết rằng họ đang thay mặt họ tạo hợp đồng phụ. | Không có |
    | Người quản lý tài khoản nhà cung cấp | Tên của người liên hệ chính của tài khoản nhà cung cấp. Giá trị mặc định được nhập tự động từ bản ghi tài khoản nhà cung cấp. Bạn có thể chọn một địa chỉ liên hệ khác làm người quản lý tài khoản nhà cung cấp của hợp đồng phụ. | Bạn có thể thiết lập cảnh báo qua email để thông báo cho người liên hệ khi có những thay đổi đối với hợp đồng phụ do thương lượng giá cả. |
