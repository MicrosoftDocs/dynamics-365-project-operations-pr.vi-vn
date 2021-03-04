---
title: Báo giá - Khái niệm chính - bản đơn giản
description: Chủ đề này cung cấp thông tin về cách sử dụng báo giá dự án trong Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e86f1a5a7b2859df5bf9569ee9ca306c6dcc6293
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/30/2020
ms.locfileid: "4178032"
---
# <a name="quotes---key-concepts---lite"></a>Báo giá - Khái niệm chính - bản đơn giản

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_


Sau đây là những khái niệm chính cần biết trước khi bạn bắt đầu sử dụng báo giá dự án trong Dynamics 365 Project Operations:

## <a name="contracting-unit"></a>Đơn vị hợp đồng

Đơn vị hợp đồng đại diện cho bộ phận hoặc đơn vị thực hành sở hữu hoạt động phân phối dự án. Bạn có thể thiết lập chi phí nguồn lực cho mỗi đơn vị hợp đồng. Khi bạn chỉ định chi phí nguồn lực cho một nguồn lực trong đơn vị hợp đồng, bạn cũng sẽ có thể thiết lập các mức chi phí khác nhau cho các nguồn lực mà đơn vị hợp đồng này mượn, hoặc bộ phận hay đơn vị thực hành khác trong doanh nghiệp. Chúng được gọi là giá chuyển nhượng, mượn nguồn lực hoặc giá trao đổi. Khi bạn thiết lập chi phí mượn nguồn lực từ các bộ phận khác, bạn cũng có thể chọn thiết lập các mức chi phí đó theo đơn vị tiền tệ của bộ phận cho mượn.

## <a name="cost-currency"></a>Đơn vị tiền tệ của chi phí

Đơn vị tiền tệ của chi phí trong Project Operations là đơn vị tiền tệ mà chi phí được báo cáo. Đơn vị tiền tệ này có nguồn gốc từ đơn vị tiền tệ gắn liền với trường **Đơn vị hợp đồng** trong báo giá, hợp đồng và dự án. Chi phí có thể được ghi bằng bất kỳ đơn vị tiền tệ nào dựa trên dự án. Tuy nhiên, có sự quy đổi đơn vị tiền tệ từ đơn vị tiền tệ mà chi phí được ghi lại thành đơn vị tiền tệ của chi phí dự án.

Do tỷ giá hối đoái trong nền tảng CDS không thể có hiệu lực theo ngày, tổng chi phí trên màn hình có thể thay đổi theo thời gian nếu bạn cập nhật tỷ giá hối đoái của đơn vị tiền tệ. Tuy nhiên, chi phí được ghi lại trong cơ sở dữ liệu vẫn không thay đổi vì số tiền được lưu trữ bằng đơn vị tiền tệ mà chúng phát sinh.

## <a name="sales-currency"></a>Đơn vị tiền tệ bán hàng

Đơn vị tiền tệ bán hàng trong Project Operations là đơn vị tiền tệ mà số tiền bán hàng ước tính và thực tế được ghi lại và hiển thị. Nó cũng là đơn vị tiền tệ để lập hóa đơn cho khách hàng trong thỏa thuận. Trên báo giá dự án, đơn vị tiền tệ bán hàng được mặc định theo bản ghi khách hàng hoặc tài khoản và có thể thay đổi khi báo giá được tạo. Sau khi báo giá được lưu lại, bạn không thể thay đổi đơn vị tiền tệ bán hàng. Bảng giá sản phẩm và dự án mặc định dựa trên đơn vị tiền tệ bán hàng của báo giá.

Không giống như chi phí, giá trị bán hàng chỉ có thể được ghi lại bằng đơn vị tiền tệ Bán hàng.

## <a name="billing-method"></a>Phương thức thanh toán

Các dự án thường có phí cố định và mô hình hợp đồng dựa trên mức sử dụng. Điều này được thể hiện trong Project Operations như **Phương thức thanh toán** và có hai giá trị: thời gian và vật tư, giá cố định.

- **Thời gian và vật tư:** Đây là mô hình hợp đồng dựa trên mức sử dụng mà mỗi chi phí phát sinh được hỗ trợ bằng doanh thu tương ứng. Khi bạn ước tính hoặc phát sinh thêm chi phí, doanh số ước tính và thực tế tương ứng cũng sẽ tăng lên. Bạn có thể chỉ định giới hạn không vượt quá trên các mô tả báo giá có phương thức thanh toán này. Điều này sẽ giới hạn doanh thu thực tế. Doanh thu ước tính không bị ảnh hưởng bởi các giới hạn không vượt quá.
- **Giá cố định:** Đây là một mô hình hợp đồng có phí cố định cho biết giá trị bán hàng sẽ độc lập với chi phí phát sinh. Giá trị bán hàng là cố định và không thay đổi khi bạn ước tính hoặc phát sinh thêm chi phí.

## <a name="project-price-lists"></a>Bảng giá dự án

Bảng giá dự án là bảng giá được sử dụng để làm giá mặc định, chứ không phải mức chi phí, cho thời gian, phí tổn và các thành phần khác liên quan đến dự án. Có thể có nhiều bảng giá, và mỗi bảng giá có thể có hiệu lực theo ngày riêng cho từng báo giá dự án. Hiệu lực theo ngày chồng chéo trên các bảng giá dự án không được hỗ trợ trong Project Operations.

## <a name="product-price-lists"></a>Bảng giá sản phẩm

Bảng giá sản phẩm là bảng giá được sử dụng để làm giá mặc định, không phải mức chi phí, cho các mô tả dựa trên sản phẩm trong báo giá. Chỉ có một bảng giá sản phẩm cho mỗi lần báo giá.

## <a name="transaction-classes"></a>Lớp giao dịch

Project Operations hỗ trợ bốn loại lớp giao dịch:

- Thời gian
- Chi phí
- Vật liệu
- Phí

Giá trị chi phí và doanh số có thể được ước tính và phát sinh theo các lớp giao dịch Thời gian, Phí tổn và Vật tư. Phí là một lớp giao dịch chỉ có doanh thu.

## <a name="work-entities-and-billing-entities"></a>Thực thể công việc thực thể thanh toán

Các thực thể đại diện cho công việc là Dự án và Tác vụ. Các thực thể đại diện cho thanh toán là Mô tả báo giá và Mô tả hợp đồng. Bạn có thể liên kết các thực thể công việc khác nhau với các tùy chọn thanh toán bằng cách liên kết chúng với Mô tả báo giá hoặc Mô tả hợp đồng.

## <a name="multi-customer-deals"></a>Thỏa thuận nhiều khách hàng

Thỏa thuận nhiều khách hàng xảy ra khi có nhiều hơn một khách hàng để lập hóa đơn. Các ví dụ phổ biến về thỏa thuận này là:

- **Doanh nghiệp OEM và các đối tác của họ:** Đối tác và nhà bán lẻ bán một sản phẩm với các dịch vụ giá trị gia tăng. Đây thường là một tình huống mà trong một thỏa thuận cụ thể với khách hàng, OEM đề nghị tài trợ một phần dự án. 

- **Các dự án khu vực công:** Nhiều cơ quan của chính quyền địa phương đồng ý tài trợ cho một dự án và được lập hóa đơn theo sự phân chia đã thỏa thuận trước đó. Ví dụ: một học khu và sở chính quyền thành phố hoặc địa phương đồng ý tài trợ cho việc xây dựng hồ bơi.

## <a name="invoice-schedules"></a>Lịch trình hóa đơn

Lịch trình hóa đơn dành riêng cho từng mô tả báo giá và không bắt buộc. Lịch trình hóa đơn được tạo dựa trên ngày bắt đầu và ngày kết thúc nhất định và tần suất lập hóa đơn. Lịch trình hóa đơn được sử dụng trong giai đoạn hợp đồng khi quy trình tạo hóa đơn tự động được đặt cấu hình. Trong giai đoạn báo giá, lịch trình là không bắt buộc. Khi lịch trình hóa đơn được tạo ở giai đoạn **Báo giá**, chúng được sao chép vào hợp đồng dự án tạo khi báo giá dự án được chốt.

## <a name="changes-from-dynamics-365-sales-quote"></a>Những thay đổi từ báo giá Dynamics 365 Sales:

Báo giá Project Operations được xây dựng dựa trên báo giá Dynamics 365 Sales. Tuy nhiên, có một số khác biệt quan trọng về chức năng mà bạn cần lưu ý:

- Các hành động **Sửa lại** và **Kích hoạt** không được hỗ trợ.
- Báo giá Project Operations có hai loại mô tả khác nhau. Một cho dự án và một cho sản phẩm.
- Báo giá Project Operations có biểu mẫu và thành phần giao diện người dùng riêng, quy tắc công việc, logic kinh doanh trong phần bổ trợ và kịch bản phía khách hàng khiến chúng trở nên riêng biệt so với báo giá Sales.

Vì những lý do này, không nên sử dụng báo giá Sales và báo giá Project Operations thay thế cho nhau.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]