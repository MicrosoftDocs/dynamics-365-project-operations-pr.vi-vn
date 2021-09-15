---
title: Mô tả hợp đồng phụ cho các hạng mục chi phí
description: Chủ đề này giải thích cách ghi lại các mô tả hợp đồng phụ cho chi phí và sử dụng các trường để ghi lại thời gian mua từ các nhà cung cấp.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9e8e7bb66063dab6db1ac8da1753913aee0ef3fc
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323847"
---
#  <a name="subcontract-lines-for-expense-categories"></a>Mô tả hợp đồng phụ cho các hạng mục chi phí

[!include [banner](../../includes/dataverse-preview.md)]

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Một hợp đồng phụ trong Dynamics 365 Project Operations có thể có một dòng cho các loại chi phí. Mô tả hợp đồng phụ cho các hạng mục chi phí cho phép Người quản lý dự án mua các hạng mục dịch vụ hoặc sản phẩm từ các nhà cung cấp mà họ có thể tính phí cho một dự án.

Để tạo mô tả hợp đồng phụ cho các danh mục chi phí trong Project Operations, hãy hoàn thành các bước sau.

1. Trong ngăn điều hướng, hãy chọn **Hợp đồng phụ** và mở hợp đồng phụ mà bạn muốn làm việc.
2. Trên tab **Mô tả hợp đồng phụ**, chọn **Mới** để tạo một mô tả mới.
3. Trên trang **Tạo nhanh**, trong trường **Lớp giao dịch**, chọn **Chi phí** và nhập hoặc chọn bất kỳ thông tin trường bắt buộc nào khác.

Bảng sau cung cấp thông tin về các trường trên trang chi tiết **Mô tả hợp đồng phụ** và trang **Tạo nhanh**.

| **Trường** |  **Mô tả** |
| ----------| ---------------- |
| Tên | Tên của mô tả hợp đồng phụ. |
| Mô tả | Mô tả ngắn gọn về các loại dịch vụ và sản phẩm đang được mua trên mô tả hợp đồng phụ. |
| Loại mô tả | Trường này có giá trị mặc định là **Dựa trên số lượng**.  |
| Phương thức thanh toán | Phương thức thanh toán của mô tả hợp đồng phụ. Dựa trên phương thức thanh toán của phần mô tả, lịch trình hóa đơn dựa trên cột mốc có sẵn cho phương thức thanh toán theo giá cố định.  |
| Lớp giao dịch | Trường này có giá trị mặc định là **Thời gian**. Để tạo các mô tả hợp đồng phụ cho việc mua sản phẩm, hãy đặt trường **Lớp giao dịch** thành **Chi phí**. Giá trị trường này chỉ ra rằng mô tả hợp đồng phụ đang được sử dụng để ghi lại việc mua một loại sản phẩm hoặc dịch vụ sẽ được sử dụng cho các dự án. |
| Danh mục giao dịch | Chọn thể loại giao dịch. |
| Ngày bắt đầu được yêu cầu | Ngày mà các danh mục mua hàng phải có sẵn từ nhà cung cấp. Ngày yêu cầu được sử dụng để chọn một bảng giá dự án từ các bảng giá dự án kèm theo hợp đồng phụ. Chi phí của danh mục trên mô tả hợp đồng phụ được mặc định từ bảng giá đó. |
| Ngày kết thúc được yêu cầu | Ngày mà các danh mục mua hàng không còn cần thiết nữa. Ngày này gọi là cảnh báo khi người quản lý dự án liên kết mô tả hợp đồng phụ này với các ước tính chi phí cụ thể cho các dự án được ghi ngày sau ngày này. |
| Số lượng đã đặt hàng | Số lượng của danh mục được mua từ nhà cung cấp. Khi người quản lý dự án thấu chi từ số lượng đã mua, một cảnh báo sẽ xảy ra.  |
| Nhóm đơn vị | Giá trị trường này mặc định dựa trên nhóm đơn vị mặc định được thiết lập cho danh mục đã chọn. |
| Đơn vị | Giá trị trường này mặc định dựa trên đơn vị mặc định được thiết lập cho danh mục đã chọn. Sự kết hợp giữa danh mục và đơn vị được sử dụng để mặc định đơn giá trên mô tả hợp đồng phụ. |
| Đơn giá | Giá trị trường đơn giá mặc định từ sự kết hợp của danh mục và đơn vị từ giá danh mục liên quan đến bảng giá dự án áp dụng cho việc bắt đầu mô tả hợp đồng phụ được yêu cầu.  |
| Tổng con | Trường chỉ đọc này được tự động tính là đơn giá số lượng nếu cả giá trị số lượng và đơn giá được nhập. Nếu một trong hai hoặc cả hai trường trống, bạn có thể nhập giá trị vào trường này theo cách thủ công.  |
| Thuế doanh thu | Nhập số tiền thuế bán hàng.  |
| Tổng số tiền | Tổng số tiền của mô tả hợp đồng phụ bao gồm thuế. Trường này được tính là tổng phụ + thuế bán hàng.  |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
