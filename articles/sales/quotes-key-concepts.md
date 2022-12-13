---
title: Các khái niệm duy nhất cho báo giá dựa trên dự án
description: Bài viết này cung cấp thông tin về báo giá dự án trong Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/02/2022
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 89867cfbe92f47d58b16da40b62d3d9dd6a15b64
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824378"
---
# <a name="concepts-unique-to-project-based-quotes"></a>Các khái niệm duy nhất cho báo giá dựa trên dự án

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Trước khi bắt đầu sử dụng báo giá dự án trong Microsoft Dynamics 365 Project Operations, bạn nên biết các khái niệm chính sau.

## <a name="owning-company"></a>Công ty sở hữu

Công ty sở hữu đại diện pháp nhân sở hữu chuyển giao dự án. Khách hàng trên báo giá phải là khách hàng hợp lệ trong pháp nhân đó trong ứng dụng tài chính và hoạt động. Đơn vị tiền tệ của công ty sở hữu và đơn vị tiền tệ của đơn vị hợp đồng được chọn trên báo giá dựa trên dự án phải khớp nhau.

## <a name="contracting-unit"></a>Đơn vị hợp đồng

Một đơn vị hợp đồng đại diện cho bộ phận hoặc thực hành sở hữu việc cung cấp dự án. Bạn có thể thiết lập chi phí nguồn lực cho mỗi đơn vị hợp đồng. Khi bạn chỉ định chi phí tài nguyên cho một tài nguyên trong đơn vị hợp đồng, bạn có thể thiết lập các mức chi phí khác nhau cho các tài nguyên mà đơn vị hợp đồng mượn hoặc cho các bộ phận hoặc thông lệ khác trong doanh nghiệp. Các tỷ lệ chi phí này được gọi là giá chuyển nhượng, vay mượn tài nguyên hoặc giá trao đổi. Khi bạn thiết lập chi phí vay tài nguyên từ các bộ phận khác, bạn có thể thiết lập tỷ lệ chi phí bằng đơn vị tiền tệ của bộ phận cho vay.

## <a name="cost-currency"></a>Đơn vị tiền tệ của chi phí

Đơn vị tiền tệ chi phí trong Project Operations là đơn vị tiền tệ mà chi phí được báo cáo. Đơn vị tiền tệ này được lấy từ đơn vị tiền tệ được đính kèm với trường **Đơn vị hợp đồng** trên báo giá, hợp đồng và dự án. Chi phí đối với một dự án có thể được ghi lại bằng bất kỳ loại tiền tệ nào. Tuy nhiên, có sự chuyển đổi đơn vị tiền tệ từ đơn vị tiền tệ ghi lại chi phí sang đơn vị tiền tệ chi phí của dự án.

Do tỷ giá hối đoái trên nền tảng Dataverse không thể có hiệu lực theo ngày nên tổng chi phí trên màn hình có thể thay đổi theo thời gian nếu bạn cập nhật tỷ giá hối đoái. Tuy nhiên, chi phí được ghi lại trong cơ sở dữ liệu vẫn không thay đổi, bởi vì số tiền được lưu trữ bằng loại tiền mà chúng phát sinh.

## <a name="sales-currency"></a>Đơn vị tiền tệ bán hàng

Đơn vị tiền tệ bán hàng trong Project Operations là đơn vị tiền tệ mà số tiền bán hàng ước tính và thực tế được ghi lại và hiển thị. Đó cũng là đơn vị tiền tệ mà khách hàng được lập hóa đơn cho giao dịch. Đối với báo giá dự án, đơn vị tiền tệ bán hàng mặc định được đặt từ bản ghi khách hàng hoặc tài khoản và có thể thay đổi đơn vị tiền tệ này khi báo giá được tạo. Tuy nhiên, không thể thay đổi đơn vị tiền tệ bán hàng sau khi báo giá được lưu. Bảng giá sản phẩm và dự án mặc định được đặt dựa trên đơn vị tiền tệ bán hàng của báo giá.

Không giống như chi phí, giá trị bán hàng chỉ có thể được ghi lại **bằng** đơn vị tiền tệ bán hàng.

## <a name="billing-method"></a>Phương thức thanh toán

Các dự án thường có các mô hình hợp đồng dựa trên mức phí và tiêu dùng cố định. Trong Project Operations, mô hình hợp đồng của dự án được thể hiện bằng phương thức thanh toán. Phương thức thanh toán có hai giá trị: thời gian và vật liệu và giá cố định.

- **Thời gian và vật chất** – Mô hình hợp đồng dựa trên mức tiêu thụ trong đó mỗi chi phí phát sinh được hỗ trợ bởi doanh thu tương ứng. Khi bạn ước tính hoặc phát sinh thêm chi phí, doanh số ước tính và thực tế tương ứng cũng tăng lên. Bạn có thể chỉ định giới hạn không vượt quá trên các mô tả báo giá có phương thức thanh toán này. Bằng cách này, bạn có thể giới hạn doanh thu thực tế. Doanh thu ước tính không bị ảnh hưởng bởi các giới hạn không vượt quá.
- **Giá cố định** – Mô hình hợp đồng có phí cố định trong đó giá trị bán hàng không phụ thuộc vào chi phí phát sinh. Giá trị bán hàng là cố định và không thay đổi khi bạn ước tính hoặc phát sinh thêm chi phí.

## <a name="project-price-lists"></a>Bảng giá dự án

Bảng giá dự án là bảng giá được sử dụng để nhập giá mặc định, không phải giá chi phí, cho thời gian, chi phí và các thành phần khác liên quan đến dự án. Có thể có nhiều bảng giá, và mỗi bảng giá có thể có hiệu lực theo ngày riêng cho từng báo giá dự án. Project Operations không hỗ trợ hiệu lực ngày chồng chéo cho bảng giá dự án.

## <a name="product-price-lists"></a>Bảng giá sản phẩm

Bảng giá sản phẩm là bảng giá được sử dụng để nhập giá mặc định, không phải giá vốn, cho các mô tả dựa trên sản phẩm trên báo giá. Chỉ có một bảng giá sản phẩm cho mỗi báo giá.

## <a name="transaction-classes"></a>Lớp giao dịch

Project Operations hỗ trợ bốn loại lớp giao dịch:

- Thời gian
- Chi phí
- Vật liệu
- Phí

Giá trị chi phí và doanh thu có thể được ước tính và phát sinh vào **Thời gian**, **Chi phí** và **Các lớp giao dịch Material** . **Phí** là loại giao dịch chỉ tính doanh thu.

## <a name="work-entities-and-billing-entities"></a>Thực thể công việc thực thể thanh toán

Dự án và Nhiệm vụ là các thực thể đại diện cho công việc. Mô tả báo giá và Mô tả hợp đồng là các thực thể đại diện cho việc thanh toán. Bạn có thể liên kết các thực thể công việc khác nhau với các tùy chọn thanh toán bằng cách liên kết chúng với Mô tả báo giá hoặc Mô tả hợp đồng.

## <a name="multi-customer-deals"></a>Thỏa thuận nhiều khách hàng

Giao dịch nhiều khách hàng xảy ra khi có nhiều khách hàng trên mỗi hóa đơn. Dưới đây là một số ví dụ điển hình:

- **Doanh nghiệp sản xuất thiết bị gốc (OEM) và đối tác của họ** – Đối tác và người bán lại bán sản phẩm bao gồm các dịch vụ giá trị gia tăng. Trong một thỏa thuận với khách hàng, OEM thường đề nghị tài trợ cho một phần của dự án.
- **Các dự án khu vực công** – Nhiều phòng ban của chính quyền địa phương đồng ý tài trợ cho một dự án và được lập hóa đơn theo cách phân chia đã thỏa thuận trước đó. Ví dụ: một học khu và sở chính quyền thành phố hoặc địa phương đồng ý tài trợ cho việc xây dựng hồ bơi.

## <a name="invoice-schedules"></a>Lịch trình hóa đơn

Lịch trình hóa đơn dành riêng cho từng mô tả báo giá và là tùy chọn. Lịch trình hóa đơn được tạo dựa trên ngày bắt đầu và ngày kết thúc cụ thể cũng như tần suất xuất hóa đơn. Chúng được sử dụng trong giai đoạn hợp đồng, khi quy trình tạo hóa đơn tự động được định cấu hình. Trong giai đoạn báo giá, lịch trình hóa đơn là tùy chọn. Nếu chúng được tạo trong giai đoạn báo giá, chúng sẽ được sao chép vào hợp đồng dự án được tạo khi giành được báo giá dự án.

## <a name="differences-from-dynamics-365-sales-quotes"></a>Sự khác biệt so với báo giá Dynamics 365 Sales

Báo giá Project Operations được xây dựng dựa trên báo giá Dynamics 365 Sales. Tuy nhiên, có một số khác biệt quan trọng về chức năng mà bạn cần lưu ý:

- Báo giá Project Operations có hai loại dòng khác nhau: một dòng dành cho dự án và một dòng dành cho sản phẩm.
- Báo giá Project Operations có trang riêng và các thành phần giao diện người dùng (UI), quy tắc kinh doanh, logic kinh doanh trong phần bổ trợ và tập lệnh phía máy khách giúp chúng khác biệt với báo giá Bán hàng.
- Trong Bán hàng, bạn có thể đính kèm nhiều đơn đặt hàng vào một báo giá bán hàng. Trong Project Operations, bạn chỉ có thể đính kèm một hợp đồng dự án vào báo giá dự án.
- Khi bạn giành được báo giá bán hàng, cơ hội liên quan có thể vẫn mở. Sau khi giành được một báo cáo dự án, cơ hội liên quan sẽ đóng lại.
- Báo giá bán hàng không bao gồm một số trường và khái niệm mà báo giá dự án bao gồm. Các trường này bao gồm **Đơn vị ký hợp đồng**, **Người quản lý tài khoản** và **Tên người thanh toán**.
- Báo giá bán hàng và báo giá dự án được xác định bởi trường bộ tùy chọn–dựa trên **Loại** . Đối với báo giá bán hàng, giá trị của trường này là **Dựa trên mặt hàng**. Đối với báo giá dự án, giá trị là **Dựa trên công việc**.

Vì những khác biệt này, chúng tôi khuyên bạn không nên sử dụng thay thế cho báo giá Bán hàng và báo giá Hoạt động dự án.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
