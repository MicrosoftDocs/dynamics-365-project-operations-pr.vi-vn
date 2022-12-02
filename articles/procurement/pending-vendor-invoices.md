---
title: Mua vật tư không tồn kho hoặc danh mục mua sắm bằng hóa đơn của nhà cung cấp đang chờ xử lý
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
# <a name="purchase-non-stocked-materials-or-procurement-categories-using-a-pending-vendor-invoice"></a>Mua vật tư không tồn kho hoặc danh mục mua sắm bằng hóa đơn của nhà cung cấp đang chờ xử lý

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Khi công ty mua vật tư không tồn kho hoặc danh mục mua sắm cho một dự án, chi phí có thể được ghi nhận ngay lập tức đối với dự án. 

Ví dụ, Contoso Robotics US đang thực hiện một dự án đổi mới thiết bị và cần giấy phép phần mềm. Nhà cung cấp bên thứ ba sẽ cấp các giấy phép này.  Khi sử dụng Dynamics 365 Finance, nhân viên ghi chép khoản phải trả ghi lại tài liệu hóa đơn của nhà cung cấp đang chờ xử lý và chỉ định chi phí giấy phép trực tiếp vào dự án đổi mới thiết bị. 

> [!IMPORTANT]
> Trước khi bạn sử dụng chức năng được mô tả trong bài viết này, hãy đánh giá và áp dụng các cấu hình cần thiết. Để biết thêm thông tin, hãy xem [Kích hoạt vật tư không tồn kho và hóa đơn của nhà cung cấp đang chờ xử lý](configure-materials-nonstocked.md) và [Sử dụng các danh mục mua với các đơn đặt hàng dự án và hóa đơn nhà cung cấp đang chờ xử lý](configure-procurement-categories.md)

## <a name="post-a-project-related-pending-vendor-invoice"></a>Đăng hóa đơn của nhà cung cấp đang chờ xử lý liên quan đến dự án 

Hóa đơn của nhà cung cấp đang chờ xử lý có thể được ghi lại trên trang **Hóa đơn của nhà cung cấp đang chờ xử lý** (**Khoản phải trả** > **Hóa đơn** > **Hóa đơn của nhà cung cấp đang chờ xử lý**). Hoàn thành các bước sau để đăng hóa đơn của nhà cung cấp đang chờ xử lý liên quan đến dự án:

1. Chuyển đến **Khoản phải trả** > **Hóa đơn** rồi chọn **Mới**. 
1. Trong trường **Tài khoản hóa đơn**, hãy chọn một nhà cung cấp, sau đó trong trường **Mã số**, nhập mã nhận dạng hóa đơn của nhà cung cấp.
1. Thêm một dòng vào hóa đơn của nhà cung cấp và sau đó trong trường **Số sản phẩm**, chọn sản phẩm không tồn kho được mua từ nhà cung cấp. Ngoài ra, trong trường **Danh mục mua sắm**, chọn danh mục mua sắm đã được mua từ nhà cung cấp.   
1. Thêm số lượng đã được mua. Hệ thống sẽ điền đơn giá dựa trên cấu hình giá của sản phẩm không tồn kho. 
1. Xác minh tổng số tiền và các chi tiết cần thiết khác trên dòng.
1. Trong phần chi tiết mô tả, trên tab **Dự án**, hãy chọn ID của dự án mà sản phẩm này sẽ được ghi vào.
1. Không bắt buộc: Chọn số hoạt động và cập nhật danh mục dự án cũng như thuộc tính dòng.
1. Đăng hóa đơn của nhà cung cấp đang chờ xử lý. Khi hóa đơn được đăng, hệ thống ghi lại thông tin sau đây:
    
    - Số dư của nhà cung cấp.
    - Số tiền thuế bán hàng.
    - Chi phí đối với dự án được ghi nhận vào tài khoản tính hợp mua sắm.
    - Chi phí thực tế của dự án giao dịch trong Dataverse.  Giao dịch này được tiếp tục xử lý bằng [Nhật ký Tích hợp Project Operations](../project-accounting/project-operations-integration-journal.md). Việc đăng nhật ký này sẽ chuyển số tiền từ tài khoản tích hợp mua sắm sang tài khoản chi phí dự án. 
    - Các giao dịch mua được thanh toán cho khách hàng của dự án bằng cách sử dụng phương thức thanh toán theo thời gian và vật liệu. Ngoài ra, các giao dịch bán hàng chưa lập hóa đơn được tạo cho các giao dịch mua trong Dataverse. Bảng giá sản phẩm trong Dataverse được sử dụng cho giá bán và số tiền cho giao dịch bán hàng chưa lập hóa đơn.
