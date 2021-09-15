---
title: Mô tả hợp đồng phụ cho sản phẩm
description: Chủ đề này giải thích cách ghi lại các mô tả hợp đồng phụ cho sản phẩm và sử dụng các trường khác nhau để ghi lại các giao dịch mua sản phẩm từ các nhà cung cấp.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c0ddc39638ae9830eacc57f3e1def75aa36e6553
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323712"
---
# <a name="subcontract-lines-for-products"></a>Mô tả hợp đồng phụ cho sản phẩm

[!include [banner](../../includes/dataverse-preview.md)]

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Một hợp đồng phụ trong Dynamics 365 Project Operations có thể có mô tả hợp đồng phụ cho các sản phẩm. Các dòng mô tả này cho phép Người quản lý dự án mua sản phẩm từ các nhà cung cấp mà sau đó họ có thể sử dụng cho các nhiệm vụ của dự án.

Hãy hoàn thành các bước sau để tạo mô tả hợp đồng phụ cho các sản phẩm trong Project Operations.

1. Trên trang điều hướng, hãy chọn **Hợp đồng phụ** rồi mở hợp đồng phụ mà bạn muốn làm việc. 
2. Trên tab **Mô tả hợp đồng phụ**, chọn **+ Mới** để tạo mô tả hợp đồng phụ mới.
3. Trên trang **Tạo nhanh**, trong trường **Lớp giao dịch**, chọn **Vật liệu** và nhập hoặc chọn thông tin trường bắt buộc. 
4. Chọn **Lưu**.

Bảng sau cung cấp thông tin về các trường trên trang **Chi tiết mô tả hợp đồng phụ** và trang **Tạo nhanh** vì chúng liên quan tới việc mua sản phẩm.

| Trường | Mô tả |
| ----- | ----------- |
| Tên | Tên của mô tả hợp đồng phụ. |
| Mô tả | Mô tả ngắn gọn về các sản phẩm đang được đặt hàng trên mục mô tả hợp đồng phụ. |
| Loại mô tả | Trường này có giá trị mặc định là **Dựa trên số lượng**. |
| Phương thức thanh toán |  Phương thức thanh toán của mô tả hợp đồng phụ. Lịch trình hóa đơn dựa trên cột mốc có sẵn cho các phương pháp thanh toán theo giá cố định. |
| Lớp giao dịch | Trường này có giá trị mặc định là **Thời gian**. Để tạo mô tả hợp đồng phụ cho việc mua sản phẩm, trong trường **Lớp giao dịch** hãy chọn **Vật liệu**. Lựa chọn này chỉ ra rằng mô tả hợp đồng phụ đang được sử dụng để ghi lại việc mua các sản phẩm sẽ được sử dụng cho các dự án. |
| Chọn sản phẩm | Chọn xem sản phẩm đang mua được duy trì trong danh mục sản phẩm hay là sản phẩm chọn thêm. |
| Sản phẩm | Chọn một sản phẩm hiện hoạt từ danh mục. Trường này chỉ có sẵn khi **Chọn sản phẩm** được đặt thành **Hiện có**. |
| Sản phẩm chọn thêm | Nhập tên của sản phẩm chọn thêm. Trường này chỉ có sẵn khi **Chọn sản phẩm** được đặt thành **Chọn thêm**.  |
| Ngày giao hàng được yêu cầu | Chọn ngày giao hàng cần thiết cho các sản phẩm. Ngày này cũng được sử dụng để chọn một bảng giá dự án từ các bảng giá dự án kèm theo hợp đồng phụ. Khi đó, chi phí của sản phẩm trên mô tả hợp đồng phụ được mặc định từ bảng giá đó. |
| Ngày giao hàng theo hợp đồng | Chọn ngày thỏa thuận giao sản phẩm theo hợp đồng.  |
| Số lượng đã đặt hàng | Nhập số lượng sản phẩm được mua từ nhà cung cấp. Nếu Người quản lý dự án thấu chi từ số lượng này, một cảnh báo sẽ xảy ra. |
| Nhóm đơn vị đo | Giá trị này chỉ mặc định cho các sản phẩm trong danh mục. Khi cả **Sản phẩm** và **Ngày giao hàng được yêu cầu** đều được chọn, hệ thống sẽ chọn bảng giá áp dụng dựa trên ngày giao hàng. Các hạng mục trong bảng giá có liên quan được truy vấn cho sản phẩm phù hợp. Giá trị đơn vị và nhóm đơn vị được mặc định từ thiết lập trên bản ghi hạng mục trong bảng giá. |
| Đơn vị | Giá trị này mặc định cho thiết lập đơn vị trên bản ghi hạng mục trong bảng giá. Bạn có thể thay đổi đơn vị này thành một đơn vị khác nếu cần. Sự kết hợp giữa sản phẩm và đơn vị được sử dụng để đặt mặc định đơn giá trên mô tả hợp đồng phụ cho các sản phẩm hiện có trong danh mục. |
| Đơn giá | Đơn giá đặt mặc định bằng cách sử dụng kết hợp sản phẩm và đơn vị từ các hạng mục trong bảng giá liên quan đến bảng giá dự án áp dụng cho ngày giao hàng được yêu cầu của mô tả hợp đồng phụ.  |
| Tổng con | Trường chỉ đọc này được tính là Số lượng x Đơn giá nếu cả hai trường đều có giá trị được nhập. Nếu một trong hai hoặc cả hai trường **Số lượng**, **Đơn giá** đều trống, thì bạn có thể nhập giá trị theo cách thủ công.  |
| Thuế doanh thu | Nhập giá trị thuế bán hàng. |
| Tổng số tiền | Trường tính toán này hiển thị tổng số tiền của mô tả hợp đồng phụ sau khi đã bao gồm thuế. Giá trị trong trường này được tính là tổng phụ + thuế. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
