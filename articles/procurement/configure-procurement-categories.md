---
title: Sử dụng các danh mục mua với các đơn đặt hàng dự án và hóa đơn nhà cung cấp đang chờ xử lý
description: Bài viết này mô tả cách định cấu hình các danh mục mua có thể được sử dụng với các đơn đặt hàng dự án và hóa đơn nhà cung cấp đang chờ xử lý.
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
# <a name="use-procurement-categories-with-project-purchase-orders-and-pending-vendor-invoices"></a>Sử dụng các danh mục mua với các đơn đặt hàng dự án và hóa đơn nhà cung cấp đang chờ xử lý

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Các chuyên gia mua hàng có thể tạo và duy trì danh mục các mặt hàng và dịch vụ có thể được sử dụng trong các đơn đặt hàng dự án và các hóa đơn của nhà cung cấp đang chờ xử lý. [Danh mục mua](/dynamics365/supply-chain/procurement/procurement-catalogs) cung cấp cho bạn một cách dễ dàng để phân loại các giao dịch mua mà không cần phải định cấu hình và sử dụng danh mục sản phẩm đã phát hành. Mỗi danh mục mua có thể được ánh xạ tới một danh mục dự án cho các giao dịch về thời gian, chi phí hoặc mặt hàng. Sau khi một hóa đơn của nhà cung cấp đang chờ xử lý sử dụng danh mục mua được đăng, hệ thống sẽ tạo các mục nhập thời gian, chi phí hoặc số liệu thực tế của dự án vật tư, giao dịch trong dự án và sổ phụ.

## <a name="minimum-version-requirements"></a>Yêu cầu phiên bản tối thiểu

Các phiên bản sau được yêu cầu để sử dụng danh mục mua với các đơn đặt hàng dự án cho các tình huống không trữ kho/nguồn lực của Microsoft Dynamics 365 Project Operations:

- Project Operations Dataverse phiên bản giải pháp 4.41.0.45 trở lên
- Môi trường tài chính và hoạt động phiên bản 10.0.26 trở lên

## <a name="run-dual-write-maps-for-procurement-category-support"></a>Chạy ánh xạ ghi kép để hỗ trợ danh mục mua

Đảm bảo ánh xạ cho **Thực thể xuất mô tả hóa đơn của nhà cung cấp dự án tích hợp Project Operations msdyn\_projectvendorinvoicelines** sử dụng phiên bản 1.0.0.4 trở lên.

## <a name="enable-the-feature-key-for-procurement-categories"></a>Bật khóa tính năng cho các danh mục mua

Thực hiện theo các bước sau để bật chức năng sử dụng các danh mục mua với các đơn đặt hàng dự án.

1. Trong Dynamics 365 Finance, mở không gian làm việc **Quản lý tính năng**.
1. Trong danh sách tính năng, hãy tìm tính năng **Sử dụng các danh mục mua trong Project Operations cho các kịch bản dựa trên nguồn lực/vật tư không tồn kho** rồi chọn **Kích hoạt**.

> [!IMPORTANT]
> Như một điều kiện tiên quyết, bạn cũng phải bật tính năng **Kích hoạt hóa đơn của nhà cung cấp đang chờ xử lý trên Project Operations cho các kịch bản dựa trên nguồn lực/vật tư không tồn kho**.

## <a name="map-project-categories-in-the-procurement-category-hierarchy"></a>Ánh xạ các danh mục dự án trong hệ thống cấp bậc danh mục mua

Thực hiện theo các bước sau để ánh xạ các danh mục dự án thành các danh mục mua trong hệ thống cấp bậc **Danh mục mua**:

1. Chuyển đến **Thu mua và tìm nguồn cung ứng \> Danh mục mua**.
1. Chọn **Chỉnh sửa hệ thống cấp bậc danh mục**.
1. Chọn nút hệ thống cấp bậc danh mục mong muốn, sau đó, trên tab **Chỉ định danh mục dự án**, liên kết nút với danh mục dự án từ danh mục **Thời gian**, **Chi phí** hoặc **Dự án hạng mục** (nghĩa là danh mục **Thời gian mặc định** hoặc **Chi phí mặc định**).
1. Chọn **Lưu.**
1. Đóng trang.

> [!NOTE]
> Không bắt buộc ánh xạ danh mục mua sang danh mục dự án. Nếu danh mục mua không được ánh xạ, hệ thống sẽ sử dụng giá trị được đặt trong trường **Mặt hàng** trong phần **Thể loại dự án mặc định** trên tab **Project Operations trên tab Dynamics 365 Customer Engagement** trên trang **Các tham số quản lý dự án và kế toán**.
