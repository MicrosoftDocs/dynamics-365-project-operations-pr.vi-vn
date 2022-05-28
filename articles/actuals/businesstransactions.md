---
title: Giao dịch kinh doanh trong hoạt động dự án
description: Chủ đề này cung cấp một cái nhìn tổng quan về khái niệm giao dịch kinh doanh trong Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: 0c6fe583af0dcaa62204b35c1093746b13b6e00e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582230"
---
# <a name="business-transactions-in-project-operations"></a>Giao dịch kinh doanh trong hoạt động dự án

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/vật tư không tồn kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Trong Microsoft Dynamics 365 Project Operations, *dịch kinh doanh* là một khái niệm trừu tượng không được đại diện bởi bất kỳ thực thể nào. Tuy nhiên, một số trường phổ biến và quy trình trên thực thể được thiết kế để sử dụng các khái niệm về giao dịch kinh doanh. Các thực thể sau đây sử dụng khái niệm trừu tượng này:

- Chi tiết dòng báo giá
- Chi tiết dòng hợp đồng
- Dòng ước tính
- Dòng nhật ký kế toán
- Thực tế

Trong số các thực thể này, chi tiết dòng Báo giá, chi tiết dòng hợp đồng và dòng ước tính được ánh xạ tới *giai đoạn ước tính* trong vòng đời của dự án. Các thực thể Dòng Nhật ký và Thực tế được ánh xạ tới *Giai đoạn thực hiện* trong vòng đời của dự án.

Hoạt động Dự án coi các bản ghi trong tất cả năm thực thể này là các giao dịch kinh doanh. Sự khác biệt duy nhất là các bản ghi trong các thực thể được ánh xạ đến giai đoạn ước tính (Chi tiết dòng báo giá, Chi tiết dòng hợp đồng và dòng Ước tính) được xem xét *dự báo tài chính*, trong khi các bản ghi trong các thực thể được ánh xạ tới giai đoạn thực thi (Dòng nhật ký và Thực tế) được coi là *sự thật tài chính* điều đó đã xảy ra.

Để biết thêm thông tin, hãy xem [Ước tính](../project-management/estimating-projects-overview.md) và [Thực tế](actuals-overview.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Khái niệm duy nhất cho các giao dịch kinh doanh

Các khái niệm sau đây là duy nhất cho các khái niệm về giao dịch kinh doanh:

- Loại giao dịch
- Lớp giao dịch
- Nguồn gốc giao dịch
- Kết nối giao dịch

### <a name="transaction-type"></a>Loại giao dịch

Loại giao dịch đại diện cho thời gian và bối cảnh tác động tài chính trên một dự án. Nó được xác định bởi bộ tùy chọn có các giá trị được hỗ trợ sau trong Hoạt động dự án:

- Chi phí
- Hợp đồng dự án
- Doanh thu chưa lập hóa đơn
- Doanh số đã lập hóa đơn
- Bán hàng liên tổ chức
- Chi phí đơn vị nguồn lực

### <a name="transaction-class"></a>Lớp giao dịch

Lớp giao dịch đại diện cho các loại chi phí khác nhau phát sinh trên dự án. Nó được xác định bởi bộ tùy chọn có các giá trị được hỗ trợ sau trong Hoạt động dự án:

- Thời gian
- Chi phí
- Vật liệu
- Phí
- Mốc
- Thuế

> [!NOTE]
> Các **Cột mốc** giá trị thường được logic nghiệp vụ sử dụng để lập hóa đơn giá cố định trong Hoạt động dự án.

### <a name="transaction-origin"></a>Nguồn gốc giao dịch

Nguồn gốc giao dịch là một thực thể lưu trữ nguồn gốc của mỗi giao dịch kinh doanh để giúp báo cáo và truy xuất nguồn gốc. Khi bắt đầu thực hiện dự án, mỗi giao dịch kinh doanh tạo ra một giao dịch kinh doanh khác, đến lượt nó, sẽ tạo ra một giao dịch kinh doanh khác, v.v.

### <a name="transaction-connection"></a>Kết nối giao dịch

Kết nối giao dịch là một thực thể lưu trữ mối quan hệ giữa hai giao dịch kinh doanh tương tự, chẳng hạn như chi phí và các thủ tục bán hàng có liên quan hoặc việc đảo ngược giao dịch được kích hoạt bởi các hoạt động thanh toán như xác nhận hóa đơn hoặc chỉnh sửa hóa đơn.

Cùng với nhau, Nguồn gốc giao dịch và các thực thể kết nối Giao dịch giúp bạn theo dõi các mối quan hệ giữa các giao dịch kinh doanh và các hành động đã tạo ra một giao dịch kinh doanh cụ thể.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
