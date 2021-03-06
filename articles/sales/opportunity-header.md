---
title: Tiêu đề/tóm tắt Cơ hội
description: Chủ đề này cung cấp thông tin về các thỏa thuận dựa trên dự án và mô tả cơ hội dựa trên dự án.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c4e91c1a869347ac1182db2de1ab9244309eb856
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908731"
---
# <a name="opportunity-headersummary"></a>Tiêu đề/tóm tắt Cơ hội

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_


Tiêu đề hay tóm tắt Cơ hội nắm bắt thông tin tổng thể về giao dịch dựa trên dự án áp dụng cho tất cả các mô tả trên cơ hội dựa trên dự án.

Cơ hội dựa trên dự án trong Dynamics 365 Project Operations là phần mở rộng của cơ hội trong Dynamics 365 Sales. Các phần mở rộng này cung cấp chức năng bổ sung dành riêng cho và cần thiết cho các cơ hội dựa trên dự án. Các phần mở rộng này có thể bao gồm các trường mới và các hành động ruy băng có sẵn trong cơ hội dựa trên dự án. Bạn có thể thấy một số trường, chức năng và logic mặc định có sẵn trong Sales nhưng không có trong Project Operations.

Bảng sau đây bao gồm các trường trong cơ hội dựa trên dự án của riêng Project Operations hoặc có một số thay đổi quan trọng trong hành vi so với Cơ hội trong Sales.

| **Trường** | **Vị trí** | **Mức độ liên quan, mục đích và hướng dẫn** | **Tác động xuôi tuyến** |
| --- | --- | --- | --- |
| Loại | Tab tổng quát (ẩn) | Trường bộ tùy chọn này có các tùy chọn sau:</br>- Dựa trên công việc (chỉ khả dụng với Project Operations)</br>- Dựa trên mục (chỉ khả dụng khi Project Operations và Sales được cài đặt)</br>- Dựa trên bảo trì dịch vụ (khả dụng khi Field Service được cài đặt) | Khi bạn sử dụng ứng dụng Project Operations, giá trị của trường này tự động được đặt thành **Dựa trên công việc** nhằm phân loại Cơ hội là dựa trên dự án. Cơ hội phải dựa trên dự án để kích hoạt tất cả các tiện ích và chức năng dành riêng cho dự án trong quy trình bán hàng xuôi tuyến cho thỏa thuận này. |
| Công ty sở hữu | Tab tổng quát | Đây là công ty hoặc pháp nhân sẽ giao dự án cho khách hàng. | Thông tin trường này sẽ được sao chép vào trường tương ứng trên báo giá Dự án được tạo từ Cơ hội này. |
| Liên hệ | Tab tổng quát | Tham chiếu đến người liên hệ chính của khách hàng cho thỏa thuận này. | |
| T.khoản | Tab tổng quát | Tham chiếu đến bản ghi công ty hoặc tài khoản của khách hàng. | |
| Người quản lý khách hàng | Tab tổng quát | Tên của Người quản lý tài khoản cho cơ hội dựa trên dự án này. | Người quản lý tài khoản chịu trách nhiệm quản lý mối quan hệ với khách hàng thông qua việc hoàn thành dự án này. Dựa trên bản ghi tài nguyên có thể đặt trước liên kết với Người quản lý tài khoản, đơn vị ký hợp đồng được mặc định. |
| Đơn vị Hợp đồng | Tab tổng quát | Đơn vị tổ chức chịu trách nhiệm bàn giao dự án hoặc các dự án liên quan đến thỏa thuận này. | Đơn vị ký hợp đồng là bộ phận của công ty sẽ hoàn thành dự án khi thỏa thuận được chốt. Mỗi đơn vị ký hợp đồng đều có một loại tiền tệ và đơn vị tiền tệ này được sử dụng để báo cáo chi phí ước tính và thực tế phát sinh trong dự án. |

Đối với tất cả các trường và phần khác trên tab **Tóm tắt** của cơ hội, hãy xem [Tạo hoặc chỉnh sửa cơ hội (Bán hàng và Trung tâm bán hàng)](https://docs.microsoft.com/dynamics365/sales-enterprise/create-edit-opportunity-sales).
