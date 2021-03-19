---
title: Đặt cấu hình danh mục dự án
description: Chủ đề này cung cấp thông tin về cách thiết lập danh mục dự án.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b7adf61a82714a0148d9c8b1d2b2b37fd611c1cf
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287534"
---
# <a name="configure-project-categories"></a>Đặt cấu hình danh mục dự án

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Project Operations cung cấp khả năng mạnh mẽ để phân loại doanh thu và chi phí trên các dự án. Danh mục cung cấp khả năng báo cáo và phân tích các giao dịch dự án, đồng thời thúc đẩy việc đăng lên sổ cái.

Sơ đồ sau minh họa mối tương quan giữa các danh mục giao dịch, danh mục chia sẻ và danh mục dự án. 

Danh mục giao dịch là nhóm cơ bản cho các giao dịch dự án. Trong nhóm đó, có một tập hợp các danh mục chung có thể được chia sẻ trên các ứng dụng và mô-đun. Phân tích các chi tiết cụ thể, danh mục dự án là cấp độ chi tiết nhất của các danh mục. Các danh mục dự án dành riêng cho pháp nhân, mô-đun và ứng dụng.

![Mối tương quan giữa các danh mục giao dịch, danh mục chia sẻ và danh mục dự án](media/project-categories.png)

## <a name="transaction-categories"></a>Danh mục giao dịch

Danh mục giao dịch đại diện cho nhóm cơ bản cho các giao dịch dự án và không dành riêng cho công ty hoặc loại giao dịch. Ví dụ: Contoso Robotics sử dụng các danh mục Thiết kế, Du lịch, Cài đặt và Dịch vụ để nhóm các giao dịch dự án.

Các danh mục giao dịch được xác định trong mô-đun Project Operations. 
1. Đi tới **Cài đặt** \> **Danh mục giao dịch** để mở biểu mẫu. 
2. Tạo một danh mục giao dịch mới bằng cách chọn **Mới** hoặc bằng cách chọn **Nhập từ Excel**.

## <a name="shared-categories"></a>Danh mục chia sẻ

Dynamics 365 sử dụng khái niệm Danh mục được chia sẻ để phân loại chi phí trong các ứng dụng khác nhau, chẳng hạn như Dynamics 365 Finance, Chuỗi cung ứng Dynamics 365 và Dynamics 365 Project Operations. Đối với mỗi danh mục giao dịch được tạo, Project Operations tự động tạo bốn danh mục được chia sẻ có liên quan: Giờ, Chi phí, Phí và Mục. Bạn có thể xem lại và điều chỉnh các danh mục được chia sẻ bằng cách đi tới **Kế toán và quản lý dự án** \> **Thiết lập** \> **Thể loại** \> **Danh mục được chia sẻ**.

## <a name="project-categories"></a>Thể loại dự án

Danh mục dự án đại diện cho mức độ chi tiết nhất của cấu hình danh mục và phải được định cấu hình riêng biệt và cho từng công ty, bởi một kế toán viên của dự án.

1. Đi đến **Kế toán và quản lý dự án** \> **Thiết lập** \> **Thể loại** \> **Danh mục dự án**.
2. Chọn **Mới**.
3. Chọn **ID danh mục** của danh mục được chia sẻ mà bạn đã tạo trong phần trước. Project Operations chỉ cho phép sử dụng những danh mục chia sẻ được liên kết với các danh mục giao dịch.
4. Chọn một nhóm danh mục.

## <a name="category-groups"></a>Nhóm danh mục

Nhóm danh mục được sử dụng để chia sẻ thuộc tính, chủ yếu đăng hồ sơ, giữa các danh mục dự án có liên quan. Phải có ít nhất một nhóm danh mục cho mỗi loại giao dịch và mỗi danh mục dự án được chỉ định một nhóm.

Thông số kỹ thuật đăng trong Project Operations được xác định bởi các quy tắc về hồ sơ doanh thu và chi phí dự án, danh mục dự án và nhóm danh mục. Bạn có thể thiết lập các nhóm danh mục bằng cách đi đến **Kế toán và quản lý dự án** \> **Thiết lập** \> **Danh mục** \> **Nhóm danh mục**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]