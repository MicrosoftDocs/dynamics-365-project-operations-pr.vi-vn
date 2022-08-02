---
title: Sử dụng các danh mục mua sắm với các đơn đặt hàng dự án và các hóa đơn của nhà cung cấp đang chờ xử lý
description: Bài viết này mô tả cách định cấu hình danh mục mua sắm có thể được sử dụng với các đơn đặt hàng dự án và hóa đơn của nhà cung cấp đang chờ xử lý.
author: sigitac
ms.date: 04/07/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: f71c6bfcd183613471a4cc10e16a5a54571fac31
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028636"
---
# <a name="use-procurement-categories-with-project-purchase-orders-and-pending-vendor-invoices"></a>Sử dụng các danh mục mua sắm với các đơn đặt hàng dự án và các hóa đơn của nhà cung cấp đang chờ xử lý

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Các chuyên gia mua hàng có thể tạo và duy trì danh mục các mặt hàng và dịch vụ có thể được sử dụng trong các đơn đặt hàng dự án và các hóa đơn của nhà cung cấp đang chờ xử lý. [Danh mục mua sắm](/dynamics365/supply-chain/procurement/procurement-catalogs) cung cấp cho bạn một cách dễ dàng để phân loại các giao dịch mua mà không cần phải định cấu hình và sử dụng danh mục sản phẩm đã phát hành. Mỗi hạng mục mua sắm có thể được ánh xạ thành một hạng mục dự án cho các giao dịch về thời gian, chi phí hoặc hạng mục. Sau khi hóa đơn của nhà cung cấp đang chờ xử lý sử dụng danh mục mua sắm được đăng, hệ thống sẽ tạo các thực tế về thời gian, chi phí hoặc vật chất của dự án, các giao dịch dự án và các mục nhập sổ cái.

## <a name="minimum-version-requirements"></a>Yêu cầu phiên bản tối thiểu

Các phiên bản sau được yêu cầu để sử dụng danh mục mua sắm với đơn đặt hàng mua dự án cho Microsoft Dynamics 365 Project Operations tình huống không có hàng / dựa trên tài nguyên:

- Hoạt động dự án Dataverse phiên bản giải pháp 4.41.0.45 trở lên
- Môi trường tài chính và hoạt động phiên bản 10.0.26 trở lên

## <a name="run-dual-write-maps-for-procurement-category-support"></a>Chạy bản đồ ghi kép để hỗ trợ danh mục mua sắm

Đảm bảo rằng ánh xạ cho **Dự án Hoạt động tích hợp dự án nhà cung cấp thực thể xuất dòng hóa đơn msdyn\_ dự án** sử dụng phiên bản 1.0.0.4 trở lên.

## <a name="enable-the-feature-key-for-procurement-categories"></a>Bật khóa tính năng cho các danh mục mua sắm

Thực hiện theo các bước sau để bật chức năng sử dụng các danh mục mua sắm với các đơn đặt hàng mua dự án.

1. Trong Dynamics 365 Finance, hãy mở **Quản lý tính năng** không gian làm việc.
1. Trong danh sách tính năng, hãy tìm **Sử dụng các danh mục mua sắm trong Hoạt động dự án cho các tình huống dựa trên tài nguyên / không có hàng** tính năng, và sau đó chọn **Cho phép**.

> [!IMPORTANT]
> Như một điều kiện tiên quyết, bạn cũng phải bật **Bật hóa đơn của nhà cung cấp đang chờ xử lý về Hoạt động dự án cho các tình huống dựa trên tài nguyên / không có hàng** tính năng.

## <a name="map-project-categories-in-the-procurement-category-hierarchy"></a>Lập bản đồ các hạng mục dự án trong hệ thống phân cấp hạng mục Mua sắm

Thực hiện theo các bước sau để ánh xạ các danh mục dự án thành các danh mục mua sắm trong **Hạng mục mua sắm** hệ thống cấp bậc:

1. Đi đến **Mua sắm và tìm nguồn cung ứng \> Các hạng mục mua sắm**.
1. Lựa chọn **Chỉnh sửa phân cấp danh mục**.
1. Chọn nút phân cấp danh mục mong muốn, sau đó trên **Chỉ định các hạng mục dự án**, liên kết nút với danh mục dự án từ **Thời gian**, **phí**, hoặc, **Dự án hạng mục** danh mục (nghĩa là, **Thời gian mặc định** hoặc **Chi phí mặc định** thể loại).
1. Chọn **Lưu.**
1. Đóng trang.

> [!NOTE]
> Ánh xạ danh mục mua sắm sang danh mục dự án là tùy chọn. Nếu một danh mục mua sắm không được ánh xạ, hệ thống sẽ sử dụng giá trị được đặt trong **Mục** lĩnh vực trong **Danh mục dự án mặc định** phần trên **Hoạt động dự án trên Dynamics 365 Sự tham gia của khách hàng** tab của **Quản lý dự án và các thông số kế toán** trang.
