---
title: Dự toán tài chính về chi phí cho dự án
description: Chủ đề này cung cấp thông tin về xác định hoặc ước tính chi phí dựa trên dự án.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c14dc31d666d0e0d026cf9cddfa1e78dee40f717
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589499"
---
# <a name="financial-estimates-for-expenses-on-projects"></a>Dự toán tài chính về chi phí cho dự án
_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Dynamics 365 Project Operations cho phép Người quản lý dự án xác định chi phí dựa trên dự án cho từng dự án hoặc một nhiệm vụ. Mỗi hạng mục chi phí có thể được liên kết với một nhiệm vụ cụ thể của dự án. Các khoản chi phí được phân thành các thể loại chi phí khác nhau, được xác định ở cấp độ tổ chức. Giá và chi phí cho từng thể loại chi phí được xác định trong bảng giá. 

Hoàn thành các bước sau để xem, thêm hoặc xóa chi phí dự án.

1. Đi đến **Dự án** và chọn dự án bạn muốn làm việc.
2. Chọn tab **Ước tính dự án** và xem danh sách chi phí dự án.
3. Chọn **Chi phí mới** để thêm một khoản chi phí. Hoặc, chọn một khoản chi phí để xóa, rồi chọn **Xóa chi phí**.

Bảng sau cung cấp thông tin về các trường trên **Dòng Ước tính chi phí** của một Dự án. 

| **Trường** | **Mô tả** | **Tác động xuôi tuyến** |
| --- | --- | --- |
| Tác vụ | Một danh sách các nhiệm vụ trong dự án. Danh sách này bao gồm các nhiệm vụ tóm tắt và nhiệm vụ nút lá. | Việc chọn một nhiệm vụ cho dòng ước tính chi phí sẽ ảnh hưởng đến chi phí ước tính và doanh số bán hàng theo chi phí ước tính cho một nhiệm vụ. Nếu để trống trường này, chi phí ước tính chỉ được theo dõi và tóm tắt ở cấp độ dự án. |
| Danh mục | Một danh sách các thể loại giao dịch có các thể loại chi phí được liên kết trong ứng dụng. | Việc chọn một thể loại sẽ làm tăng giá và chi phí trên dòng ước tính chi phí. |
| Ngày bắt đầu | Ngày dự báo phát sinh chi phí. | Không có tác động xuôi tuyến đối với trường này. |
| Nhóm đơn vị đo | Giá trị mặc định trong trường này đến từ nhóm đơn vị được thiết lập làm giá trị mặc định trên thể loại đã chọn. Bạn có thể cập nhật trường này để chọn một nhóm đơn vị khác. | Không có tác động xuôi tuyến đối với trường này. |
| Đơn vị | Giá trị mặc định trong trường này là đơn vị mặc định của thể loại đã chọn. Bạn có thể cập nhật trường này để chọn một đơn vị khác. | Việc thay đổi đơn vị sẽ dẫn đến một đơn giá và chi phí mặc định khác. |
| Số lượng | Số lượng chi phí ước tính mà bạn sẽ phải chịu. | Không có tác động xuôi tuyến đối với trường này. |
| Chi phí đơn vị | Chi phí của tổ hợp đơn vị và thể loại đã chọn như được thiết lập trong bảng giá vốn áp dụng | Chi phí đơn vị luôn hiển thị theo đơn vị tiền tệ chi phí của dự án. |
| Đơn giá | Giá của tổ hợp đơn vị và thể loại đã chọn như được thiết lập trong bảng giá bán hàng áp dụng. | Đơn giá luôn hiển thị theo đơn vị tiền tệ bán hàng của dự án. |
| Tổng chi phí | Số tiền chi phí được tính theo công thức số lượng \* chi phí đơn vị.| Số tiên chi phí luôn hiển thị theo đơn vị tiền tệ chi phí của dự án. |
| Tổng doanh thu | Số tiền bán hàng được tính theo công thức số lượng \* đơn giá. | Số tiền bán hàng luôn hiển thị theo đơn vị tiền tệ bán hàng của dự án. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
