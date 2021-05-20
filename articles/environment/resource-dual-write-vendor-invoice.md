---
title: Tích hợp hóa đơn của nhà cung cấp
description: Chủ đề này cung cấp thông tin về tích hợp hóa đơn của nhà cung cấp trong Project Operations.
author: sigitac
manager: Annbe
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 07839436c3777b0554e0721d250bff643e38c088
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955862"
---
# <a name="vendor-invoice-integration"></a>Tích hợp hóa đơn của nhà cung cấp

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Hoạt động mua sắm liên quan đến dự án trong Dynamics 365 Project Operations có thể được ghi lại bằng cách chuyển đến **Tài khoản phải trả** > **Hóa đơn** > **Hóa đơn của nhà cung cấp đang chờ xử lý** và sử dụng tài liệu hóa đơn của nhà cung cấp đang chờ xử lý. Để biết thêm thông tin, hãy xem [Mua vật tư không tồn kho bằng hóa đơn của nhà cung cấp đang chờ xử lý](../procurement/pending-vendor-invoices.md).

> [!IMPORTANT]
> Trước khi bạn sử dụng chức năng được mô tả trong chủ đề này, hãy đánh giá và áp dụng các cấu hình cần thiết. Để biết thêm thông tin, hãy xem [Kích hoạt vật tư không tồn kho và hóa đơn của nhà cung cấp đang chờ xử lý](../procurement/configure-materials-nonstocked.md).

Trong Project Operations, các hóa đơn của nhà cung cấp liên quan đến dự án được đăng bằng các quy tắc đặc biệt:

- Chi phí liên quan đến dự án (bao gồm cả thuế không thu hồi được) không được đăng ngay vào tài khoản chi phí dự án trong sổ cái. Thay vào đó, chi phí được đăng vào **Tài khoản tích hợp mua sắm**. Tài khoản này được đặt cấu hình trong **Quản lý dự án và kế toán** > **Thiết lập** > **Quản lý dự án và thông số kế toán**, trên tab **Project Operations trên Dynamics 365 Customer Engagement**.
- Tính năng ghi kép đồng bộ hóa chi tiết hóa đơn của nhà cung cấp với Microsoft Dataverse bằng các bản đồ bảng sau:

     - **Thực thể xuất hóa đơn của nhà cung cấp dự án tích hợp Project Operations (msdyn_projectvendorinvoices)**: Bản đồ bảng này đồng bộ hóa thông tin tiêu đề hóa đơn của nhà cung cấp. Chỉ các hóa đơn của nhà cung cấp có ít nhất một dòng chứa ID dự án mới được đồng bộ hóa với Dataverse.
     - **Thực thể xuất mô tả hóa đơn của nhà cung cấp dự án tích hợp Project Operations (msdyn_projectvendorinvoicelines)**: Bản đồ bảng này đồng bộ hóa thông tin mô tả hóa đơn của nhà cung cấp. Chỉ những dòng chứa ID dự án mới được đồng bộ hóa với Dataverse.

     > [!NOTE]
     > Chi tiết hóa đơn của nhà cung cấp trong Dataverse không thể chỉnh sửa.

Sổ cái thuế, sổ cái nhà cung cấp và các bài đăng tài chính khác được ghi nhận là có thể áp dụng trong Dynamics 365 Finance khi hóa đơn của nhà cung cấp được đăng.

![Tích hợp hóa đơn của nhà cung cấp](media/DW7VendorInvoice.png)

Khi hồ sơ được ghi vào một thực thể **Hóa đơn bán hàng** trong Dataverse, quá trình phê duyệt tự động của các hồ sơ bắt đầu. Nếu cần, bạn có thể xem lại trạng thái quy trình phê duyệt tự động trong Dataverse bằng cách chuyển đến phần **Cài đặt nâng cao** > **Hệ thống** > **Công việc hệ thống**. Sau khi phê duyệt xong, hệ thống sẽ tạo bản ghi lớp giao dịch vật tư trong thực thể **Giá trị thực tế**.

Sau đó, các giá trị thực tế liên quan đến vật tư được xử lý bằng cách sử dụng sơ đồ bảng ghi kép, **Giá trị tích hợp thực tế của Project Operations (msdyn_actuals)**. Để biết thêm thông tin, hãy xem [Giá trị ước tính và thực tế của dự án](resource-dual-write-estimates-actuals.md).

Quy trình định kỳ **Nhập từ tách chuyển** tạo các dòng nhật ký kế toán tích hợp trong Project Operations liên quan đến hóa đơn của nhà cung cấp. Tài khoản bù trừ mặc định là tài khoản tích hợp cung ứng. Khi nhật ký tích hợp được đăng, số dư tài khoản sẽ được xóa cho giao dịch hóa đơn của nhà cung cấp và số tiền theo mô tả sẽ chuyển vào tài khoản chi phí dự án. Các giao dịch trong sổ cái của dự án cũng được tạo cho các mục đích lập hóa đơn và ghi nhận doanh thu xuôi tuyến.
