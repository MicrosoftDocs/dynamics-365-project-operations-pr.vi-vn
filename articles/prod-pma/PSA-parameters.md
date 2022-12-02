---
title: Tham số tích hợp Project Service Automation
description: Bài viết này giải thích cách đặt cấu hình cách nhập dữ liệu mặc định khi bạn tích hợp Microsoft Dynamics 365 for Project Service Automation với Microsoft Dynamics 365 Finance.
author: ruhercul
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: a4abeb2960981196ed1d7c453e7daa0558e326ef
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932322"
---
# <a name="project-service-automation-integration-parameters"></a>Tham số tích hợp Project Service Automation

[!include[banner](../includes/banner.md)]

Trên trang **Tham số tích hợp Project Service Automation**, bạn có thể đặt cấu hình cách nhập dữ liệu mặc định khi tích hợp Dynamics 365 Project Service Automation với Dynamics 365 Finance. Để các dự án được đồng bộ hóa thành công từ Project Service Automation sang Finance, bạn phải thiết lập các trường sau đây.

Để mở trang **Tham số tích hợp Project Service Automation**, hãy đi đến **Quản lý dự án và kế toán** \> **Thiết lập** \> **Tham số tích hợp Dynamics 365 for Project Service Automation**. 

> [!NOTE]
> - Tính năng tích hợp nhiệm vụ dự án, thể loại giao dịch chi phí, ước tính giờ, ước tính chi phí và khóa chức năng có sẵn trong phiên bản 8.0.
> - Tùy chọn tích hợp giá trị thực tế có sẵn từ phiên bản 8.0.1.


| Thẻ                    | Trường                | Mô tả |
|------------------------|----------------------|-------------|
| Chung                | Loại dự án mặc định | Chọn loại dự án mặc định. Khi các dự án được đồng bộ hóa từ Project Service Automation, giá trị này được sử dụng nếu bạn không cung cấp giá trị mặc định trong mẫu tích hợp. Trong quá trình đồng bộ hóa, trường **Loại dự án** của các dự án mới được đặt thành giá trị này. Tuy nhiên, giá trị có thể được cập nhật khi các dòng hợp đồng dự án được đồng bộ hóa từ Project Service Automation. |
|                        | Thể loại thời gian        | Chọn thể loại thời gian mặc định. Giá trị này được sử dụng khi ước tính giờ được đồng bộ hóa từ Project Service Automation. Khi ước tính giờ và giá trị giờ thực tế được đồng bộ hóa từ Project Service Automation, trường **Thể loại** của dự báo giờ dự án mới trong Finance được thiết lập thành giá trị này. |
|                        | Thể loại phí         | Chọn thể loại phí mặc định. Giá trị này được sử dụng khi giá trị phí thực tế được đồng bộ hóa từ Project Service Automation. Khi giá trị phí thực tế được đồng bộ hóa từ Project Service Automation, trường **Thể loại** của giao dịch phí mới trong Finance được thiết lập thành giá trị này. |
| Nhóm dự án mặc định | Loại dự án         | Nhấp vào **Mới** để thêm một hàng nơi bạn có thể chọn loại dự án để đặt nhóm dự án mặc định. Một loại dự án cụ thể chỉ có thể được chọn một lần trong cấu hình. |
|                        | Nhóm dự án        | Chọn nhóm dự án mặc định cho loại dự án đã chọn. Khi các dự án mới được đồng bộ hóa từ Project Service Automation, trường **Nhóm dự án** được đặt thành giá trị mặc định cho loại dự án nếu bạn không cung cấp giá trị mặc định trong mẫu tích hợp. |
| Loại thanh toán mặc định  | Loại thanh toán         | Nhấp vào **Mới** để thêm một hàng nơi bạn có thể chọn loại thanh toán để đặt thuộc tính dòng mặc định. Một loại thanh toán cụ thể chỉ có thể được chọn một lần trong cấu hình. |
|                        | Thuộc tính dòng        | Chọn thuộc tính dòng mặc định cho loại thanh toán đã chọn. Khi ước tính giờ mới, ước tính chi phí mới hoặc giá trị thực tế mới được đồng bộ hóa từ Project Service Automation, trường **Thuộc tính dòng** được đặt thành giá trị mặc định cho loại thanh toán. |
| Khóa chức năng  | Không áp dụng       | Chọn chức năng để tắt trong Finance cho các dự án và hợp đồng có nguồn gốc từ Project Service Automation. Ví dụ: bạn có thể tắt khả năng chỉnh sửa hợp đồng và dự án, tạo cấu trúc phân tích công việc và nhập bảng chấm công trong Finance. Các trường liên quan đến kế toán sẽ tiếp tục được bật, ngay cả khi chúng không được thiết lập tham số cung cấp. Theo mặc định, tất cả chức năng được bật. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]