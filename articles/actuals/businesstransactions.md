---
title: Giao dịch kinh doanh trong Project Operations
description: Bài viết này cung cấp thông tin tổng quan về khái niệm giao dịch kinh doanh trong Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 01/31/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2022-01-31
ms.openlocfilehash: fab0061af6e615c25d0fbf79d024370285dc6f86
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923306"
---
# <a name="business-transactions-in-project-operations"></a>Giao dịch kinh doanh trong Project Operations

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/vật tư không tồn kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Trong Microsoft Dynamics 365 Project Operations, *giao dịch kinh doanh* là một khái niệm trừu tượng không được đại diện bởi bất kỳ thực thể nào. Tuy nhiên, một số trường phổ biến và quy trình trên thực thể được thiết kế để sử dụng các khái niệm về giao dịch kinh doanh. Các thực thể sau đây sử dụng khái niệm trừu tượng này:

- Chi tiết dòng báo giá
- Chi tiết dòng hợp đồng
- Dòng ước tính
- Dòng nhật ký kế toán
- Thực tế

Trong các thực thể này, Chi tiết mô tả báo giá, Chi tiết mô tả hợp đồng và Dòng ước tính được ánh xạ tới *giai đoạn ước tính* trong vòng đời dự án. Dòng nhật ký kế toán và Thực thể thực tế được ánh xạ tới giai *đoạn thực thi* trong chu kỳ dự án.

Project Operations ghi nhận các bản ghi trong cả năm thực thể này là giao dịch kinh doanh. Sự khác biệt duy nhất là bản ghi trong thực thể được ánh xạ tới giai đoạn ước tính (Chi tiết mô tả báo giá, Chi tiết mô tả hợp đồng và Chi tiết ước tính) được coi là *dự báo tài chính*, trong khi các bản ghi trong thực thể được ánh xạ tới giai đoạn thực hiện (Dòng nhật ký kế toán và Thực tế) được coi là *sự kiện tài chính* đã xảy ra.

Để biết thêm thông tin, hãy xem [Ước tính](../project-management/estimating-projects-overview.md) và [Thực tế](actuals-overview.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Khái niệm duy nhất cho các giao dịch kinh doanh

Các khái niệm sau đây là duy nhất cho các khái niệm về giao dịch kinh doanh:

- Loại giao dịch
- Lớp giao dịch
- Nguồn gốc giao dịch
- Kết nối giao dịch

### <a name="transaction-type"></a>Loại giao dịch

Loại giao dịch đại diện cho thời gian và bối cảnh tác động tài chính trên một dự án. Nó được xác định bằng một bộ tùy chọn có các giá trị được hỗ trợ trong Project Operations:

- Chi phí
- Hợp đồng dự án
- Doanh thu chưa lập hóa đơn
- Doanh số đã lập hóa đơn
- Bán hàng liên tổ chức
- Chi phí đơn vị nguồn lực

### <a name="transaction-class"></a>Lớp giao dịch

Lớp giao dịch đại diện cho các loại chi phí khác nhau phát sinh trên dự án. Nó được xác định bằng một bộ tùy chọn có các giá trị được hỗ trợ trong Project Operations:

- Thời gian
- Chi phí
- Vật liệu
- Phí
- Mốc
- Thuế

> [!NOTE]
> Giá trị **Mốc** thường được dùng bởi logic kinh doanh để lập hóa đơn giá cố định trong Project Operations.

### <a name="transaction-origin"></a>Nguồn gốc giao dịch

Nguồn gốc giao dịch là một thự thể lưu trữ nguồn gốc của mỗi giao dịch kinh doanh để giúp báo cáo và truy xuất nguồn gốc. Khi bắt đầu thực hiện dự án, mỗi giao dịch kinh doanh tạo ra một giao dịch kinh doanh khác, rồi giao dịch kinh doanh đó lại tạo ra một giao dịch kinh doanh khác, v.v.

### <a name="transaction-connection"></a>Kết nối giao dịch

Kết nối giao dịch là một thực thể lưu trữ mối quan hệ giữa hai giao dịch kinh doanh tương tự, chẳng hạn như chi phí và thực tế bán hàng liên quan hoặc đảo ngược giao dịch được kích hoạt bằng các hoạt động thanh toán như xác nhận hóa đơn hoặc chỉnh sửa hóa đơn.

Các thực thể nguồn gốc giao dịch và kết nối giao dịch kết hợp lại để giúp bạn theo dõi mối quan hệ giữa giao dịch và hành động kinh doanh đã tạo ra một giao dịch kinh doanh cụ thể.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
