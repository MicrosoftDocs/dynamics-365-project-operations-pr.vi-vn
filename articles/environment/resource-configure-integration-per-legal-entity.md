---
title: Đặt cấu hình tích hợp Project Operations cho mỗi pháp nhân
description: Bài viết này cung cấp thông tin về cách thiết lập tích hợp của pháp nhân trong Hoạt động dự án.
author: sigitac
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3f33e641ee0932655282618c99a26e2603660059
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914704"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>Đặt cấu hình tích hợp Project Operations cho mỗi pháp nhân 

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Bài viết này hướng dẫn bạn các bước cần thiết để cấu hình Dynamics 365 Project Operations mỗi pháp nhân.

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>Bật các phím tính năng trong Dynamics 365 Finance

Hoàn thành các bước sau để bật các tính năng cần thiết.

1. Trong Dynamics 365 Finance, hãy chuyển đến **Quản lý tính năng** không gian làm việc.
2. Trong **Danh sách tính năng**, tìm và bật các tính năng sau:
  
    - **Cho phép nhiều mô tả hợp đồng cho một dự án**
    - **Bật Hoạt động Dự án trên Dynamics 365 Customer Engagement**

> [!NOTE]
> Nếu bạn không thấy **Khóa tính năng** được liệt kê, xác minh rằng phiên bản Finance của bạn đáp ứng yêu cầu phiên bản tối thiểu (phiên bản ứng dụng 10.0.13 với tất cả các bản cập nhật chất lượng được áp dụng hoặc cao hơn). Chọn **Kiểm tra cập nhật** để làm mới danh sách tính năng.

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>Xác định kịch bản triển khai Project Operations cho một pháp nhân

Bạn có thể bật Hoạt động dự án trên Dynamics 365 Customer Engagement ở cấp pháp nhân. Bạn có thể có một pháp nhân hợp pháp sử dụng Hoạt động dự án trên Dynamics 365 Customer Engagement cho các tình huống dựa trên tài nguyên / không có kho. Trong cùng một môi trường, bạn có thể có một pháp nhân khác sử dụng Project Operations cho các kịch bản trữ kho/lệnh sản xuất.

1. Trong Dynamics 365 Finance, hãy truy cập **Quản lý dự án và kế toán** > **Thành lập** > **Quản lý dự án toàn cầu và các thông số kế toán**.
2. Trong danh sách các pháp nhân hiện có, hãy chọn các pháp nhân có nhiều dòng hợp đồng và Hoạt động dự án trên các tính năng Dynamics 365 Customer Engagement sẽ được bật. Bỏ chọn các pháp nhân sẽ sử dụng Project Operations cho các kịch bản trữ kho/lệnh sản xuất.

> [!NOTE]
> Một pháp nhân chỉ có thể được chọn nếu nó không có bất kỳ dự án hiện có nào.

## <a name="configure-project-management-and-accounting-parameters"></a>Đặt cấu hình quản lý dự án và các tham số kế toán

Mỗi pháp nhân sử dụng Hoạt động dự án trên Dynamics 365 Customer Engagement cần một bộ thông số mặc định. Các tham số này được đặt cấu hình trên tab **Project Operations** trên trang **Tham số kế toán và quản lý dự án**. Các tham số là:

  - **Loại thanh toán mặc định**: Project Operations sử dụng một tập hợp cố định các loại thanh toán mặc định phải được ánh xạ tới thuộc tính mô tả Finance. Tạo bản ghi cho từng loại thanh toán: **Không được chỉ định**, **Có thể tính phí**, **Không tính phí**, **Miễn phí** và **Không có sẵn**.
  - **Danh mục dự án mặc định**: Chọn các danh mục dự án mặc định sẽ được sử dụng cho từng loại giao dịch. Các giá trị mặc định này sẽ được sử dụng trong **nhật ký Tích hợp Project Operations** và trong các giá trị ước tính mà không có danh mục giao dịch nào được chỉ định cho giá trị thực tế của dự án.
  - **Dự báo**: Chọn mô hình dự báo được sử dụng để ước tính thời gian và chi phí.


[!INCLUDE[footer-include](../includes/footer-banner.md)]