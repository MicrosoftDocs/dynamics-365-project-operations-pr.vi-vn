---
title: Mô tả hợp đồng phụ cho sản phẩm
description: Bài viết này giải thích cách ghi lại các dòng hợp đồng phụ cho các sản phẩm và sử dụng các trường khác nhau để ghi lại các giao dịch mua sản phẩm từ các nhà cung cấp.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b5852df1876eff591ae6a131b229d979eacf5aad
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262149"
---
# <a name="subcontract-lines-for-products"></a>Mô tả hợp đồng phụ cho sản phẩm

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Một hợp đồng phụ trong Dynamics 365 Project Operations có thể có mô tả hợp đồng phụ cho các sản phẩm. Các dòng mô tả này cho phép Người quản lý dự án mua sản phẩm từ các nhà cung cấp mà sau đó họ có thể sử dụng cho các nhiệm vụ của dự án.

Hãy hoàn thành các bước sau để tạo mô tả hợp đồng phụ cho các sản phẩm trong Project Operations.

1. Trên trang điều hướng, hãy chọn **Hợp đồng phụ** rồi mở hợp đồng phụ mà bạn muốn làm việc. 
2. Trên tab **Mô tả hợp đồng phụ**, chọn **+ Mới** để tạo mô tả hợp đồng phụ mới.
3. Trên trang **Tạo nhanh**, trong trường **Lớp giao dịch**, chọn **Vật liệu** và nhập hoặc chọn thông tin trường bắt buộc. 
4. Chọn **Lưu**.

Bảng sau cung cấp thông tin về các trường trên trang **Chi tiết mô tả hợp đồng phụ** và trang **Tạo nhanh** vì chúng liên quan tới việc mua sản phẩm.

| Trường | Mô tả | Tác động chức năng|
| ----- | ----------- | ----------- |
| Tên | Tên của mô tả hợp đồng phụ để giúp xác định. |Đây sẽ được hiển thị là cột đầu tiên trong tất cả các tra cứu dựa trên các mô tả hợp đồng phụ.
| Mô tả | Mô tả ngắn gọn về các sản phẩm đang được đặt hàng trên mục mô tả hợp đồng phụ. | Không có |
| Loại mô tả | Trường này có giá trị mặc định là **Dựa trên số lượng**. |Không có |
| Phương thức thanh toán | Đây là bộ tùy chọn đại diện cho hai mô hình hợp đồng chính được Project Operations hỗ trợ: **Giá cố định** và **Thời gian và Vật liệu**. | Dựa trên phương thức thanh toán đã chọn, một lịch biểu hóa đơn dựa trên mốc thời gian được cung cấp cho các mô tả hợp đồng phụ với phương thức thanh toán Giá cố định. |
| Lớp giao dịch |Trường này có giá trị mặc định là **Thời gian**. Để tạo các mô tả hợp đồng phụ cho việc mua sản phẩm, hãy đặt trường **Lớp giao dịch** thành **Vật liệu**.  | Điều này cho thấy rằng mô tả hợp đồng phụ đang được sử dụng để ghi lại việc mua sản phẩm sẽ được sử dụng cho các dự án. |
| Chọn sản phẩm | Chọn xem sản phẩm đang mua được duy trì trong danh mục sản phẩm hay là sản phẩm chọn thêm. |Không có |
| Sản phẩm | Chọn một sản phẩm hiện hoạt từ danh mục. Trường này chỉ có sẵn khi **Chọn sản phẩm** được đặt thành **Hiện có**. |Sự kết hợp của **Sản phẩm** và **Đơn vị** sẽ được sử dụng làm mặc định hoặc được tính cho đơn giá cho mô tả hợp đồng phụ.
| Sản phẩm chọn thêm | Nhập tên của sản phẩm chọn thêm. Trường này chỉ có sẵn khi **Chọn sản phẩm** được đặt thành **Chọn thêm**.  |Giá mua sẽ không được tự động điền cho các sản phẩm chọn thêm.|
| Ngày giao hàng được yêu cầu | Nhập ngày giao hàng cần thiết cho các sản phẩm.| Ngày này cũng được sử dụng để chọn một bảng giá dự án từ các bảng giá dự án kèm theo hợp đồng phụ. Khi đó, chi phí của sản phẩm trên mô tả hợp đồng phụ được mặc định từ bảng giá đó. |
| Ngày giao hàng theo hợp đồng | Ghi ngày giao sản phẩm theo hợp đồng.  |Không có|
| Số lượng đã đặt hàng | Nhập số lượng sản phẩm được mua từ nhà cung cấp.| Điều này sẽ được sử dụng để hiển thị cảnh báo khi người quản lý dự án vẽ quá mức từ số lượng này.|
| nhóm đơn vị đo | Giá trị này chỉ mặc định cho các sản phẩm trong danh mục. |Khi cả **Sản phẩm** và **Ngày giao hàng được yêu cầu** đều được chọn, hệ thống sẽ chọn bảng giá áp dụng dựa trên ngày giao hàng. Các hạng mục trong bảng giá có liên quan được truy vấn cho sản phẩm phù hợp. Giá trị đơn vị và nhóm đơn vị được mặc định từ thiết lập trên bản ghi hạng mục trong bảng giá. |
| Đơn vị | Giá trị này mặc định cho đơn vị được thiết lập trên bản ghi mục bảng giá. Bạn có thể thay đổi đơn vị này thành một đơn vị khác nếu cần.| Sự kết hợp giữa sản phẩm và đơn vị được sử dụng để đặt mặc định đơn giá trên mô tả hợp đồng phụ cho các sản phẩm hiện có trong danh mục. |
| Đơn giá | Đơn giá đặt mặc định bằng cách sử dụng kết hợp sản phẩm và đơn vị từ các hạng mục trong bảng giá liên quan đến bảng giá dự án áp dụng cho ngày giao hàng được yêu cầu của mô tả hợp đồng phụ.  |Không có |
| Tổng con | Trường chỉ đọc này được tính là Số lượng x Đơn giá nếu cả hai trường đều có giá trị được nhập. Nếu một trong hai hoặc cả hai trường **Số lượng**, **Đơn giá** đều trống, thì bạn có thể nhập giá trị theo cách thủ công.  |Không có |
| Thuế doanh thu | Nhập giá trị thuế bán hàng. |Không có |
| Tổng số tiền | Trường tính toán này hiển thị tổng số tiền của mô tả hợp đồng phụ sau khi đã bao gồm thuế. Giá trị trong trường này được tính là Tổng phụ + Thuế. |Không có |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
