---
title: Mô tả hợp đồng phụ cho các hạng mục chi phí
description: Chủ đề này giải thích cách ghi lại các mô tả hợp đồng phụ cho chi phí và sử dụng các trường để ghi lại thời gian mua từ các nhà cung cấp.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 9eba8b70aeb98389515ee679e4bfb1426736ee2c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591706"
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

| **Trường** | **Mô tả** | **Tác động chức năng** |
| --- | --- | --- |
| Tên | Tên của mô tả hợp đồng phụ để giúp xác định. | Đây sẽ được hiển thị là cột đầu tiên trong tất cả các tra cứu dựa trên các mô tả hợp đồng phụ. |
| Mô tả | Mô tả ngắn gọn về các loại chi phí đang được mua trên mô tả hợp đồng phụ. | Không có |
|Loại mô tả | Trường này có giá trị mặc định là **Dựa trên số lượng**. |Không có |
| Phương thức thanh toán | Đây là bộ tùy chọn đại diện cho hai mô hình hợp đồng chính được Project Operations hỗ trợ: **Giá cố định** và **Thời gian và Vật liệu**. | Lịch hóa đơn dựa trên cột mốc được cung cấp cho các mô tả hợp đồng phụ nếu phương pháp thanh toán Giá cố định được chọn. |
| Lớp giao dịch | Trường này có giá trị mặc định là **Thời gian**. Để tạo các mô tả hợp đồng phụ cho việc mua sản phẩm, hãy đặt trường **Lớp giao dịch** thành **Chi phí**.  | Điều này cho thấy rằng mô tả hợp đồng phụ đang được sử dụng để ghi lại việc mua một loại chi phí được sử dụng cho các dự án. |
| Danh mục giao dịch | Hiển thị danh sách các danh mục giao dịch đang hoạt động trong hệ thống. |Không có |
| Ngày bắt đầu được yêu cầu | Nhập ngày mà các danh mục mua hàng phải có sẵn từ nhà cung cấp. | Bắt đầu được yêu cầu được sử dụng để chọn một bảng giá dự án từ các bảng giá dự án đính kèm với hợp đồng phụ. Chi phí của thể loại trên mô tả thầu phụ lấy từ bảng giá đó. |
| Ngày kết thúc được yêu cầu | Nhập ngày mà các danh mục mua hàng sẽ không còn cần thiết nữa. | Điều này sẽ được sử dụng để hiển thị cảnh báo khi người quản lý dự án liên kết mô tả hợp đồng phụ này với các dự toán chi phí cụ thể của dự án được yêu cầu sau ngày này. |
| Số lượng đã đặt hàng | Số lượng của danh mục được mua từ nhà cung cấp. | Điều này sẽ được sử dụng để hiển thị cảnh báo khi người quản lý dự án vẽ quá mức từ số lượng này.|
| nhóm đơn vị đo | Giá trị mặc định dựa trên nhóm đơn vị mặc định được thiết lập cho danh mục đã chọn. |Không có |
| Đơn vị | Giá trị mặc định dựa trên đơn vị mặc định được thiết lập cho danh mục đã chọn.  | Sự kết hợp của **Thể loại** và **Đơn vị** sẽ được sử dụng làm mặc định hoặc được tính cho đơn giá cho mô tả hợp đồng phụ.  |
| Đơn giá | Giá trị mặc định sử dụng kết hợp của **Thể loại** và **Đơn vị** từ giá thể loại liên quan đến bảng giá dự án, áp dụng cho việc bắt đầu mô tả thầu phụ được yêu cầu. |Không có |
| Tổng con | Đây là trường chỉ đọc được tính là Số lượng X Đơn giá, nếu cả giá trị số lượng và đơn giá đều được nhập. Nếu một trong hai hoặc cả hai trường đều trống, bạn có thể nhập giá trị vào trường này. |Không có |
| Thuế doanh thu | Nhập số tiền thuế bán hàng. |Không có |
| Tổng số tiền | Tổng số tiền của mô tả hợp đồng phụ bao gồm thuế. Trường này được tính là Tổng phụ + Thuế bán hàng. |Không có |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
