---
title: Tổng quan về triển khai Project Operations cho các tình huống dựa trên nguồn lực/hàng không trữ kho
description: Chủ đề này cung cấp thông tin về loại hình triển khai, Project Operations cho các tình huống dựa trên nguồn lực/hàng không trữ kho.
author: rumant
ms.date: 11/02/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: a66877471e584bc76ddfe508a5d4cb47e38dd7aeb5f2bebe795b41a1de462ef9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009737"
---
# <a name="project-operations-for-resourcenon-stocked-based-scenarios-deployment-overview"></a>Tổng quan về triển khai Project Operations cho các tình huống dựa trên nguồn lực/hàng không trữ kho

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Loại hình triển khai, Dynamics 365 Project Operations cho các trường hợp dựa trên nguồn lực/hàng không trữ kho có các tính năng sau dành cho những công ty dựa trên dự án:

- Lập kế hoạch dự án bằng Microsoft Project dành cho web
- Định giá và chi phí đa chiều cho nguồn lực lao động
- Định giá dựa trên thể loại cho các thể loại chi phí
- Quản lý bán hàng dựa trên dự án bằng các tính năng của Dynamics 365 Sales
- Universal resource scheduling hợp với các ứng dụng khác như Dynamics 365 Field Service và Dynamics 365 Customer Service
- Theo dõi thời gian và tiến độ dự án
- Giải pháp quản lý chi phí cơ bản và đầy đủ đối với các chi phí thuộc dự án và không thuộc dự án, bao gồm cả ghi lại biên nhận bằng cách sử dụng các tính năng OCR
- Việc lập hóa đơn mở rộng từ nền tảng ước giá cho đến nền tảng dành cho khách hàng và được hỗ trợ bởi thuế bán hàng cấp doanh nghiệp cũng như hệ thống tỷ giá hối đoái có hiệu lực theo ngày.
- Chi phí dự án có thể đặt cấu hình, hồ sơ doanh thu và quy tắc cho hoạt động kế toán và khoản dồn tích trong công việc đang thực hiện (WIP)
- Ghi nhận doanh thu dự án
- Khả năng mở rộng thông qua Power Platform

Loại hình triển khai này giúp mở rộng chức năng được các ứng dụng Dynamics 365 Finance và Dynamics 365 Supply Chain Management cung cấp.

Nên chọn loại hình triển khai này nếu điều kỳ vọng ở Project Operations là sử dụng toàn bộ vòng đời của dự án có các yêu cầu sau:

- Khả năng quản lý bán hàng dựa trên dự án thông qua các loại hình bán hàng khác bằng các tính năng trong ứng dụng Sales.
- Một hệ thống quản lý dự án tích hợp giúp quản lý các dự án nội bộ và dự án phải thanh toán đối với các vấn đề liên quan đến lịch trình và tài chính, từ bán hàng cho đến kế toán của dự án.
- Một hệ thống quản lý chi phí bao gồm việc thực thi chính sách và bồi hoàn để theo dõi các chi phí thuộc dự án và không thuộc dự án.
- Yêu cầu một công cụ hiệu quả cho tỷ giá hối đoái và thuế bán hàng cấp doanh nghiệp để tạo hóa đơn dành cho khách hàng của dự án.
- Hệ thống ghi nhận doanh thu và kế toán của dự án tuân thủ Tiêu chuẩn báo cáo tài chính quốc tế (IFRS).
- Các ứng dụng Finance hoặc Supply Chain Management và sự tích hợp các giao dịch dựa trên dự án.


[!INCLUDE[footer-include](../includes/footer-banner.md)]