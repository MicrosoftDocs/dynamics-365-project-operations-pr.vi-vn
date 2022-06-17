---
title: Mua vật liệu không tồn kho hoặc danh mục mua sắm bằng cách sử dụng hóa đơn của nhà cung cấp đang chờ xử lý
description: Bài viết này giải thích cách ghi lại các hóa đơn của nhà cung cấp đang chờ xử lý.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b1c05755f6759e90e031a11261f15a2c4b6b716e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922018"
---
# <a name="purchase-non-stocked-materials-or-procurement-categories-using-a-pending-vendor-invoice"></a>Mua vật liệu không tồn kho hoặc danh mục mua sắm bằng cách sử dụng hóa đơn của nhà cung cấp đang chờ xử lý

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Khi một công ty mua vật liệu không tồn kho hoặc các hạng mục mua sắm cho một dự án, chi phí có thể được ghi nhận ngay lập tức đối với dự án. 

Ví dụ, Contoso Robotics US đang thực hiện một dự án đổi mới thiết bị và cần giấy phép phần mềm. Nhà cung cấp bên thứ ba sẽ cấp các giấy phép này.  Sử dụng Dynamics 365 Finance, nhân viên Kế toán khoản phải trả ghi lại tài liệu hóa đơn của nhà cung cấp đang chờ xử lý và phân bổ chi phí giấy phép trực tiếp cho dự án đổi mới thiết bị. 

> [!IMPORTANT]
> Trước khi bạn sử dụng chức năng được mô tả trong bài viết này, hãy xem xét và áp dụng các cấu hình cần thiết. Để biết thêm thông tin, hãy xem [Cho phép vật liệu không tồn kho và hóa đơn của nhà cung cấp đang chờ xử lý](configure-materials-nonstocked.md) và [Sử dụng các danh mục mua sắm với các đơn đặt hàng dự án và hóa đơn của nhà cung cấp đang chờ xử lý](configure-procurement-categories.md)

## <a name="post-a-project-related-pending-vendor-invoice"></a>Đăng hóa đơn của nhà cung cấp đang chờ xử lý liên quan đến dự án 

Hóa đơn của nhà cung cấp đang chờ xử lý có thể được ghi lại trên trang **Hóa đơn của nhà cung cấp đang chờ xử lý** (**Khoản phải trả** > **Hóa đơn** > **Hóa đơn của nhà cung cấp đang chờ xử lý**). Hoàn thành các bước sau để đăng hóa đơn của nhà cung cấp đang chờ xử lý liên quan đến dự án:

1. Đi đến **Các khoản phải trả** > **Hóa đơn** và chọn **Mới**. 
1. Bên trong **Tài khoản hóa đơn**, chọn một nhà cung cấp, sau đó, trong **Con số**, nhập nhận dạng hóa đơn của nhà cung cấp.
1. Thêm một dòng vào hóa đơn của nhà cung cấp, sau đó, trong **Số mặt hàng**, chọn mặt hàng không còn hàng đã được mua từ nhà cung cấp. Ngoài ra, trong **Hạng mục mua sắm**, chọn danh mục mua sắm đã được mua từ nhà cung cấp.   
1. Thêm số lượng đã được mua. Hệ thống điền đơn giá, dựa trên cấu hình giá mặt hàng không tồn kho. 
1. Xác minh tổng số tiền và các chi tiết cần thiết khác trên dòng.
1. Trong chi tiết dòng, trên **Dự án**, chọn ID của dự án mà mục này sẽ được ghi vào.
1. Tùy chọn: Chọn số hoạt động và cập nhật danh mục dự án và thuộc tính dòng.
1. Đăng hóa đơn nhà cung cấp đang chờ xử lý. Khi hóa đơn được đăng, hệ thống ghi lại các thông tin sau:
    
    - Số dư của nhà cung cấp.
    - Số tiền thuế bán hàng.
    - Chi phí đối với dự án được ghi nhận vào tài khoản tính hợp mua sắm.
    - Chi phí thực tế của dự án giao dịch trong Dataverse.  Giao dịch này được tiếp tục xử lý bằng [Nhật ký Tích hợp Project Operations](../project-accounting/project-operations-integration-journal.md). Việc đăng nhật ký này sẽ chuyển số tiền từ tài khoản tích hợp mua sắm sang tài khoản chi phí dự án. 
    - Các giao dịch mua được thanh toán cho khách hàng của dự án bằng cách sử dụng phương thức thanh toán theo thời gian và vật liệu. Ngoài ra, các giao dịch bán hàng chưa lập hóa đơn được tạo cho các giao dịch mua trong Dataverse. Bảng giá sản phẩm trong Dataverse được sử dụng cho giá bán và số tiền cho giao dịch bán hàng chưa lập hóa đơn.
