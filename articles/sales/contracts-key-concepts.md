---
title: Khái niệm chính – Hợp đồng dự án
description: Chủ đề này cung cấp thông tin về các khái niệm chính của hợp đồng dự án trong Project Operations.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4ab43a9de6b27f0f0e9b8cbe6ea8b613ce81e08d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087044"
---
# <a name="key-concepts---project-contracts"></a>Khái niệm chính – Hợp đồng dự án

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Chủ đề này cung cấp những khái niệm chính mà bạn cần biết trước khi bắt đầu sử dụng Hợp đồng dự án trong Dynamics 365 Project Operations:

## <a name="owning-company"></a>Công ty sở hữu

Công ty sở hữu là pháp nhân ở mô-đun **Quản lý dự án và kế toán** cho Project Operations từ Dynamics 365 Finance. Công ty sở hữu đại diện cho pháp nhân sẽ chịu trách nhiệm đối với chi phí và doanh thu tích lũy từ một thỏa thuận.

## <a name="contracting-unit"></a>Đơn vị Hợp đồng

Đơn vị hợp đồng đại diện cho bộ phận hoặc đơn vị thực hành sở hữu hoạt động phân phối của dự án. Bạn có thể thiết lập chi phí nguồn lực cho mỗi đơn vị hợp đồng. Khi bạn chỉ định chi phí nguồn lực cho một nguồn lực, bạn cũng sẽ có thể thiết lập các mức chi phí khác nhau cho các nguồn lực. Đơn vị hợp đồng này mượn các nguồn lực này từ các bộ phận hoặc đơn vị thực hành khác trong doanh nghiệp. Mức chi phí cho nguồn lực được gọi là giá chuyển nhượng, giá mượn nguồn lực hoặc giá trao đổi. Khi bạn thiết lập mức chi phí để mượn nguồn lực từ các bộ phận khác, hãy sử dụng đơn vị tiền tệ của bộ phận cho mượn.

## <a name="cost-currency"></a>Đơn vị tiền tệ của chi phí

Đơn vị tiền tệ của chi phí là đơn vị tiền tệ được dùng để báo cáo chi phí trên màn hình. Đơn vị tiền tệ này được dẫn xuất từ đơn vị tiền tệ gắn liền với trường **Đơn vị hợp đồng** trên hợp đồng và dự án. Chi phí có thể được ghi bằng bất kỳ đơn vị tiền tệ nào dựa trên dự án. Tuy nhiên, có sự quy đổi loại tiền từ đơn vị tiền tệ dùng để ghi lại chi phí thành đơn vị tiền tệ của chi phí dự án khi được hiển thị trên màn hình.

Vì tỷ giá hối đoái trong nền tảng Common Data Service (CDS) không thể có hiệu lực theo ngày, nên tổng số trên màn hình có thể thay đổi theo thời gian nếu bạn cập nhật tỷ giá hối đoái của đơn vị tiền tệ. Tuy nhiên, chi phí được ghi lại trong cơ sở dữ liệu vẫn không thay đổi vì số tiền được lưu trữ theo đơn vị tiền tệ phát sinh.

## <a name="sales-currency"></a>Tiền tệ Bán hàng

Đơn vị tiền tệ bán hàng trong Project Operations là đơn vị tiền tệ mà số tiền bán hàng ước tính và thực tế được ghi lại và hiển thị. Đơn vị tiền tệ bán hàng cũng là đơn vị tiền tệ dùng để lập hóa đơn cho khách hàng trong thỏa thuận. Trên hợp đồng dự án, đơn vị tiền tệ bán hàng được lấy mặc định từ bản ghi khách hàng hoặc tài khoản và có thể thay đổi khi hợp đồng được tạo. Khi hợp đồng được tạo bằng cách đóng một mục báo giá là đã giành được, đơn vị tiền tệ trên hợp đồng được lấy mặc định từ đơn vị tiền tệ trên báo giá.

Khi tạo một hợp đồng dự án từ đầu, bạn không thể sửa trường **Đơn vị tiền tệ bán hàng**. Bảng giá sản phẩm và dự án xác định giá trị mặc định dựa trên đơn vị tiền tệ này trong hợp đồng.

Khác với chi phí, giá trị bán hàng chỉ có thể được ghi lại theo đơn vị tiền tệ bán hàng.

## <a name="billing-method"></a>Phương thức Thanh toán

Thông thường, có hai mô hình hợp đồng cho dự án: phí cố định và dựa trên mức sử dụng. Các mô hình này được trình bày trong Project Operations dưới dạng phương thức thanh toán với hai giá trị khả dĩ:

- Thời gian và vật tư: Mô hình hợp đồng dựa trên mức sử dụng, trong đó mỗi chi phí phát sinh được hỗ trợ bằng doanh thu tương ứng. Khi bạn ước tính hoặc phát sinh thêm chi phí, doanh số ước tính và thực tế tương ứng cũng tăng lên. Chỉ định giới hạn không vượt quá đối với các mục mô tả hợp đồng có phương thức thanh toán này, giới hạn đó sẽ thiết lập ngưỡng cho doanh thu thực tế. Các giới hạn không vượt quá không ảnh hưởng đến doanh thu ước tính.
- Giá cố định: Mô hình hợp đồng có phí cố định biểu thị giá trị bán hàng sẽ độc lập với chi phí phát sinh. Giá trị bán hàng là cố định và không thay đổi khi bạn ước tính hoặc phát sinh thêm chi phí.

## <a name="project-price-lists"></a>Bảng giá dự án

Bảng giá dự án là bảng giá được sử dụng lấy mặc định mức giá, chứ không phải mức chi phí, đối với thời gian, chi phí và các thành phần khác liên quan đến dự án. Có thể có nhiều bảng giá. Mỗi bảng giá có một khoảng ngày hiệu lực riêng cho từng hợp đồng dự án. Project Operations không hỗ trợ khoảng ngày hiệu lực chồng chéo trên bảng giá dự án.

Khi hợp đồng dự án được tạo qua việc giành được báo giá dự án, các bảng giá dự án sẽ được sao chép cùng với tên và ngày hợp đồng. Việc sao chép thông tin này cấu thành giá tùy chỉnh cho các thành phần dự án trên hợp đồng dự án này.

## <a name="transaction-classes"></a>Lớp giao dịch

Project Operations hỗ trợ bốn loại lớp giao dịch:

- Thời gian
- Chi phí
- Vật liệu
- Phí

Giá trị chi phí và doanh số có thể được ước tính và phát sinh theo các lớp giao dịch Thời gian, Phí tổn và Vật tư. Phí là lớp giao dịch chỉ có doanh thu.

## <a name="work-entities-and-billing-entities"></a>Thực thể công việc và thực thể thanh toán

Các thực thể đại diện cho công việc là dự án và nhiệm vụ. Các thực thể đại diện cho các khía cạnh thanh toán là mục mô tả hợp đồng. Bạn có thể liên kết các thực thể công việc khác nhau với các tùy chọn thanh toán bằng cách liên kết chúng với mục mô tả hợp đồng.

## <a name="multi-customer-deals"></a>Thỏa thuận nhiều khách hàng

Thỏa thuận nhiều khách hàng là loại có nhiều hơn một khách hàng cần được lập hóa đơn. Các ví dụ phổ biến về thỏa thuận này là:

- Doanh nghiệp OEM và đối tác của họ: Đối tác và người bán lại bán một sản phẩm kèm theo một số dịch vụ giá trị gia tăng, thường liên quan đến một thỏa thuận cụ thể với khách hàng. OEM đề nghị cấp vốn cho một phần dự án. 

- Các dự án khu vực công: Nhiều cơ quan của chính quyền địa phương đồng ý tài trợ cho một dự án và được lập hóa đơn theo sự phân chia đã thỏa thuận trước đó. Chẳng hạn, một học khu và chính quyền địa phương đồng ý tài trợ cho việc xây dựng hồ bơi.

## <a name="invoice-schedules"></a>Lịch trình hóa đơn

Lịch trình hóa đơn là dữ liệu cụ thể cho từng mục mô tả hợp đồng và là thông tin phải có để tính năng lập hóa đơn tự động hoạt động. Lịch trình hóa đơn được tạo dựa trên ngày bắt đầu và ngày kết thúc nhất định và tần suất lập hóa đơn. Lịch trình được sử dụng trong giai đoạn hợp đồng khi quy trình tạo hóa đơn tự động được đặt cấu hình. Khi hợp đồng dự án được tạo từ báo giá, lịch trình hóa đơn được sao chép từ báo giá vào hợp đồng dự án.

## <a name="changes-from-dynamics-365-sales-orders"></a>Các thay đổi so với đơn hàng Dynamics 365 Sales

Hợp đồng trong Project Operations được xây dựng dựa trên Đơn hàng trong Dynamics 365 Sales. Tuy nhiên, có một số điểm khác biệt quan trọng về chức năng. Hợp đồng có biểu mẫu, thành phần giao diện người dùng, quy tắc công việc, phần bổ trợ lô-gic kinh doanh và tập lệnh phía máy khách riêng, khác hẳn với những dữ liệu trong Đơn hàng. Vì vậy, bạn không được sử dụng đơn hàng Sales và hợp đồng Project Operations hoán đổi cho nhau.
