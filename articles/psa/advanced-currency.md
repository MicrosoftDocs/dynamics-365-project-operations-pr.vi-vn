---
title: Tình huống nhiều loại tiền tệ (phiên bản 3.x)
description: Chủ đề này cung cấp thông tin về các trường hợp nhiều loại tiền tệ.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/26/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: bdb9ccad84e0f510118502d4253f5c83a760f8bb
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145699"
---
# <a name="multiple-currency-scenarios"></a>Tình huống nhiều loại tiền tệ

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Microsoft Dynamics 365 có hai khái niệm tiền tệ:

- **Tiền tệ giao dịch** - Tiền tệ tham gia vào một giao dịch. 
- **Tiền cơ sở** - Tiền tệ của phiên bản Dynamics 365. Tiền tệ này được thiết lập khi một phiên bản Dynamics 365 được cung cấp. Không thể thay đổi tiền tệ này.

Ví dụ: Contoso Mỹ đã bán 100 chiếc áo thun cho một khách hàng ở Anh với giá 15 ounds Sterling (GBP) mỗi chiếc. Bảng sau hiển thị cách giao dịch này được ghi lại trong thực thể sản phẩm đặt hàng.

| Sản phẩm | Số lượng | Đơn giá | Tiền tệ | Tổng số | Tỷ giá | Giá mỗi đơn vị (Cơ sở)| Số tiền (Gốc)|
|---------|----------|----------------|----------|--------|---------------|----------------------|--------------|
| Áo phông | 100      | 15             | GBP      | 1500   | 0.94          | $17,25               | $1.725       |

Cột **Tiền tệ** hiển thị tiền tệ giao dịch là loại tiền tệ trong giao dịch bán hàng. Cột **Tỷ giá hối đoái** là tỷ giá hối đoái giữa tiền tệ giao dịch và tiền tệ cơ sở. Tiền tệ cơ sở là đô la Mỹ (USD). Tiền tệ cơ sở được thiết lập khi một phiên bản Dynamics 365 được cung cấp.
Như bảng hiển thị, mỗi giao dịch được ghi lại trong cả hai loại tiền tệ giao dịch và tiền tệ cơ sở. Dynamics 365 sử dụng tỷ giá trao đổi tiền tệ để tính toán số tiền tệ cơ sở.

## <a name="project-service-automation-extensions"></a>Phần mở rộng Project Service Automation

Dynamics 365 Project Service Automation ảnh hưởng đến tiền tệ giao dịch, bởi vì các giao dịch kinh doanh thường có hai khía cạnh: chi phí và bán hàng.

Các thực thể sau đây được coi là giao dịch kinh doanh:

- Chi tiết mô tả báo giá
- Chi tiết dòng hợp đồng dự án
- Dòng ước tính
- Dòng nhật ký kế toán
- Chi tiết dòng hóa đơn
- Thực tế

Trong mỗi thực thể này, có một bản ghi đại diện cho số tiền chi phí hoặc số tiền bán hàng. Đối với bất kỳ thực thể Dynamics 365 nào có trường **Số tiền**, thì mỗi hồ sơ sẽ bao gồm số tiền ở cả loại tiền tệ giao dịch và cơ sở. 

PSA mở rộng khái niệm về tiền tệ giao dịch cho chi phí và bán hàng theo các cách sau:

- Tiền tệ giao dịch chi phí cho các giao dịch thời gian luôn xuất phát từ loại tiền tệ của đơn vị tổ chức sở hữu hoặc quản lý dự án. Đơn vị tổ chức này được gọi là đơn vị hợp đồng.
- Tiền giao dịch bán hàng cho giao dịch thời gian và chi phí luôn đến từ tiền tệ của hợp đồng dự án.
- Tiền tệ giao dịch chi phí cho các chi phí đến từ các loại tiền tệ mà mục nhập chi phí được tạo.

## <a name="multiple-currency-scenario"></a>Tình huống nhiều loại tiền tệ

Phần này mô tả một ví dụ về một dự án Contoso Anh cung cấp cho khách hàng có tên là Fabrikam, Nhật Bản. Đây là cách các kịch bản đã được thiết lập:

1. GBP và yên Nhật (JPY) được thiết lập trong **Cài đặt** \> **Quản lý doanh nghiệp** \> **Tiền tệ**. 
2. Tài khoản khách hàng được đặt tên là **Fabrikam - Nhật Bản** được thiết lập và JPY được chọn là loại tiền tệ trên tài khoản.
3. Đơn vị tổ chức có tên **Contoso Anh** được thiết lập và GBP được chọn là loại tiền tệ.
4. Hợp đồng dự án được tạo, trong đó **Contoso Anh** được chỉ định là đơn vị hợp đồng và **Fabrikam - Nhật Bản** được chỉ định là khách hàng.
5. Các dòng hợp đồng dự án được tạo, dựa trên bố trí lập hóa đơn cho nhiều lớp giao dịch khác nhau trên dự án, chẳng hạn như lập hóa đơn cho thời gian so với chi phí.
6. Một dự án được tạo, trong đó **Contoso Anh** được chỉ định là đơn vị hợp đồng. Dự án này được tạo và ánh xạ tới dòng hợp đồng dự án.


Trong quá trình ước tính sử dụng chi tiết dòng báo giá, chi tiết dòng hợp đồng dự án hoặc trên dòng ước tính của lịch trình, hai hồ sơ luôn được tạo trong thực thể. Một bản ghi dành cho chi phí và bản ghi còn lại dành cho bán hàng.

- Theo mặc định, tiền tệ giao dịch trên bản ghi chi phí được đặt thành đơn vị tiền tệ đơn vị hợp đồng của dự án. Trong ví dụ này, tiền tệ là GBP.
- Theo mặc định, tiền tệ giao dịch trên bản ghi bán hàng được đặt thành đơn vị tiền tệ của hợp đồng của dự án. Trong ví dụ này, tiền tệ là JPY.

Khi lợi nhuận được tạo cho thời gian sử dụng mục nhập thời gian hoặc dòng nhật ký kế toán, thì hành vi sau đây sẽ xuất hiện:

- Theo mặc định, tiền tệ giao dịch trên bản ghi chi phí được đặt thành đơn vị tiền tệ đơn vị hợp đồng của dự án.
- Theo mặc định, tiền tệ giao dịch trên bản ghi bán hàng được đặt thành đơn vị tiền tệ của hợp đồng của dự án.

Khi lợi nhuận được tạo cho chi phí bằng mục nhập chi phí hoặc dòng nhật ký kế toán, thì hành vi sau đây sẽ xuất hiện:

- Bạn có thể ghi lại tiền chi phí bằng bất kỳ loại tiền tệ nào. Chọn loại tiền tệ bằng cách sử dụng trình chọn tiền tệ trên trang **Mục nhập chi phí** hoặc trang **Dòng nhật ký kế toán**. Theo mặc định, tiền tệ giao dịch cho bản ghi chi phí được đặt thành đơn vị tiền tệ trên mục nhập chi phí. 
- Theo mặc định, tiền tệ giao dịch cho bản ghi bán hàng được đặt thành đơn vị tiền tệ của hợp đồng của dự án. Để đặt loại tiền tệ này, trước tiên, hệ thống sẽ chuyển đổi số tiền giao dịch bằng loại tiền tệ mà người dùng đã nhập vào tiền cơ sở. Sau đó, hệ thống sẽ chuyển đổi số tiền sang loại tiền tệ của hợp đồng dự án. 

### <a name="computing-roll-ups-when-project-actuals-are-recorded-in-multiple-transaction-currencies"></a>Tính toán cuốn chiếu khi doanh thu dự án được ghi lại bằng nhiều loại tiền tệ giao dịch

Dynamics 365 tự động xử lý cuốn chiếu các số tiền bằng nhiều đơn vị tiền tệ khác nhau. Dưới đây là một ví dụ.

| Lớp giao dịch | Loại giao dịch| Date   | Nguồn lực | Thể loại giao dịch | Số lượng | Đơn giá | Tổng số      | Tỷ giá | Số tiền gốc |
|-------------------|------------------|--------|----------|----------------------|----------|--------------|-------------|---------------|----------------|
| Time              | Bán hàng chưa lập hóa đơn   | 14 tháng 6 | Đức  |                      | 8 giờ    | 20.000 JPY    | 160.000 JPY | 123           | 1.300,81 USD    |
| Time              | Bán hàng chưa lập hóa đơn   | 15 tháng 6 | Đức  |                      | 8 giờ    | 20.000 JPY    | 160.000 JPY | 123           | 1.300,81 USD    |
| Chi phí           | Bán hàng chưa lập hóa đơn   | 16 tháng 6 | Đức  | Khách sạn                | 1 ea     | 250 EUR      | 250 EUR     | 0.94          | 265,95 USD     |
| Chi phí           | Bán hàng chưa lập hóa đơn   | 17 tháng 6 | Đức  | Thuê xe           | 1 ea     | 150 EUR      | 150 EUR     | 0.94          | 159,57 USD     |

Để tính tổng giá trị bán hàng chưa thanh toán trên dự án, bạn có thể tạo trường cuốn chiếu cho trường **Số tiền** trên tất cả doanh thu bán hàng chưa lập hóa đơn liên quan. Trường tổng số là một cấu trúc của Dynamics 365 cho phép tạo các công thức nhanh trên bản ghi liên quan.
