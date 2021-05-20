---
title: Mua vật tư không tồn kho bằng hóa đơn của nhà cung cấp đang chờ xử lý
description: Chủ đề này giải thích cách ghi lại các hóa đơn của nhà cung cấp đang chờ xử lý.
author: sigitac
manager: tfehr
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7a706f419443dcdf92ce3b247d719943272907d0
ms.sourcegitcommit: 7468d668c48c1d87934aab9a034decd51e56dec6
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880698"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a>Mua vật tư không tồn kho bằng hóa đơn của nhà cung cấp đang chờ xử lý

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Khi công ty mua vật tư không tồn kho cho một dự án, chi phí có thể được ghi nhận ngay lập tức đối với dự án. 

Ví dụ, Contoso Robotics US đang thực hiện một dự án đổi mới thiết bị và cần giấy phép phần mềm. Nhà cung cấp bên thứ ba sẽ cấp các giấy phép này.  Khi sử dụng Dynamics 365 Finance, nhân viên ghi chép khoản phải trả ghi lại tài liệu hóa đơn của nhà cung cấp đang chờ xử lý và chỉ định chi phí giấy phép trực tiếp vào dự án đổi mới thiết bị. 

> [!IMPORTANT]
> Trước khi bạn sử dụng chức năng được mô tả trong chủ đề này, hãy đánh giá và áp dụng các cấu hình cần thiết. Để biết thêm thông tin, hãy xem [Kích hoạt vật tư không tồn kho và hóa đơn của nhà cung cấp đang chờ xử lý](configure-materials-nonstocked.md). 

## <a name="post-a-project-related-pending-vendor-invoice"></a>Đăng hóa đơn của nhà cung cấp đang chờ xử lý liên quan đến dự án 

Hóa đơn của nhà cung cấp đang chờ xử lý có thể được ghi lại trên trang **Hóa đơn của nhà cung cấp đang chờ xử lý** (**Khoản phải trả** > **Hóa đơn** > **Hóa đơn của nhà cung cấp đang chờ xử lý**). Hoàn thành các bước sau để đăng hóa đơn của nhà cung cấp đang chờ xử lý liên quan đến dự án:

1. Chuyển đến **Khoản phải trả** > **Hóa đơn** rồi chọn **Mới**. 
2. Trong trường **Tài khoản hóa đơn**, hãy chọn một nhà cung cấp và trong trường **Mã số**, nhập mã nhận dạng hóa đơn của nhà cung cấp.
3. Thêm một dòng vào hóa đơn của nhà cung cấp và trong trường **Số sản phẩm**, chọn sản phẩm không tồn kho được mua từ nhà cung cấp. 

    > [!NOTE]
    > Không thể ghi các dòng hóa đơn của nhà cung cấp dựa trên danh mục mua sắm đối với dự án. 
    
5. Thêm số lượng đã mua. Hệ thống sẽ điền đơn giá dựa trên cấu hình giá của sản phẩm không tồn kho. 
6. Xác minh tổng số tiền và các chi tiết cần thiết khác trên dòng.
7. Trên chi tiết mô tả, trên tab **Dự án**, hãy chọn ID của dự án mà sản phẩm này sẽ được ghi vào.
8. Theo tùy chọn, hãy chọn số hoạt động và cập nhật danh mục dự án cũng như thuộc tính dòng.
9. Đăng hóa đơn của nhà cung cấp đang chờ xử lý. Khi hóa đơn được đăng, hệ thống ghi lại:
    
    - Số dư của nhà cung cấp.
    - Số tiền thuế bán hàng.
    - Chi phí đối với dự án được ghi nhận vào tài khoản tính hợp mua sắm.
    - Giao dịch thực tế của dự án tại Dataverse. Giao dịch này được tiếp tục xử lý bằng [Nhật ký Tích hợp Project Operations](../project-accounting/project-operations-integration-journal.md). Việc đăng nhật ký này sẽ chuyển số tiền từ tài khoản tích hợp mua sắm sang tài khoản chi phí dự án.
