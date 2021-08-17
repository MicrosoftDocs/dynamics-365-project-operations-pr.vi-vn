---
title: Định giá dự án
description: Chủ đề này cung cấp thông tin về cách định giá hoạt động trong Dynamics 365 Project Service Automation.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/11/2019
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
ms.openlocfilehash: dfbfb59547f295e5fb275264b9222bfa20517f6278144ca013e14a99454b6840
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/06/2021
ms.locfileid: "7000602"
---
# <a name="project-pricing"></a>Định giá dự án 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation mở rộng thực thể Bảng giá trong Dynamics 365 Sales. 

## <a name="key-entities"></a>Các thực thể chính

Bảng giá bao gồm thông tin được cung cấp bởi bốn thực thể khác nhau:

- **Bảng giá** - Thực thể này lưu trữ thông tin về ngữ cảnh, tiền tệ, ngày hiệu lực và đơn vị thời gian cho thời gian áp dụng giá. Ngữ cảnh cho biết liệu bảng giá hiển thị chi phí hay giá bán. 
- **Tiền tệ** - Thực thể này lưu trữ tiền tệ của giá trên bảng giá. 
- **Ngày** - Thực thể này được sử dụng khi hệ thống cố gắng nhập một giá mặc định trên một giao dịch. Giá PSA sẽ chọn bảng giá có ngày hiệu lực bao gồm cả ngày giao dịch. Nếu giá PSA tìm thấy nhiều bảng giá có hiệu quả cho ngày giao dịch đính kèm báo giá, hợp đồng hoặc đơn vị tổ chức liên quan thì không có giá nào là mặc định. 
- **Thời gian** - Thực thể này lưu trữ đơn vị thời gian mà giá thể hiện, chẳng hạn như mức giá hàng ngày hoặc theo giờ. 

Thực thể bảng giá có ba bảng liên quan nhằm lưu trữ giá:

  - **Giá theo vai trò** - Bảng này lưu trữ một mức giá cho sự kết hợp giữa các giá trị vai trò và đơn vị tổ chức, được dùng để thiết lập giá dựa trên vai trò cho nguồn nhân lực.
  - **Giá theo loại giao dịch** - Bảng này lưu trữ giá theo loại giao dịch và được sử dụng để thiết lập giá theo loại chi phí.
  - **Hạng mục trong bảng giá** - Bảng này lưu trữ giá cho sản phẩm theo danh mục.

> ![Cấu hình giá bằng cách sử dụng bảng giá.](media/basic-guide-12.png)
 
Bảng giá là là một bảng giá. Bảng giá là sự kết hợp của thực thể Bảng giá và các hàng liên quan trong bảng giá theo vai trò, giá theo loại giao dịch và hạng mục trong bảng giá.

## <a name="resource-roles"></a>Vai trò nguồn lực

Thuật ngữ *vai trò nguồn lực* đề cập đến một bộ kỹ năng, năng lực và chứng chỉ mà một người phải có để thực hiện một bộ nhiệm vụ cụ thể trên một dự án.

Thời gian của nguồn lực thường được báo giá dựa trên vai trò mà một nguồn lực thực hiện dự án cụ thể. Đối với thời gian nguồn nhân lực, PSA hỗ trợ chi phí và thanh toán dựa trên vai trò tài nguyên. Có thể báo giá thời gian ở bất kỳ đơn vị nào trong nhóm đơn vị đo **Thời gian**.

Nhóm đơn vị đo **Thời gian** được tạo khi cài đặt PSA. Nó có một đơn vị mặc định là **Giờ**. Bạn không thể xóa, đổi tên hoặc chỉnh sửa các thuộc tính nhóm đơn vị đo **Thời gian** hoặc đơn vị **Giờ**. Tuy nhiên, bạn có thể thêm các đơn vị vào nhóm đơn vị đo **Thời gian**. Nếu bạn cố gắng xóa hoặc nhóm đơn vị đo **Thời gian** hoặc đơn vị **Giờ**, thì bạn có thể gây ra lỗi trong logic kinh doanh PSA.

> ![Cấu hình giá theo vai trò.](media/basic-guide-13.png)
 
## <a name="transaction-categories-and-expense-categories"></a>Danh mục giao dịch và loại chi phí

Chi phí đi lại và chi phí khác mà tư vấn viên dự án phải chịu thường được tính cho khách hàng. PSA hỗ trợ giá của loại chi phí bằng cách sử dụng danh sách giá. Vé máy bay, khách sạn và thuê xe là ví dụ về các loại chi phí. Mỗi dòng trong bảng giá cho các chi phí xác định giá cho một loại chi phí cụ thể. Đối với giá của các loại chi phí, PSA hỗ trợ ba phương pháp định giá sau:

- **Theo chi phí** - Chi phí được tính cho khách hàng và không áp dụng tăng.
- **Tỷ lệ phần trăm tăng** - Tỷ lệ phần trăm trên chi phí thực tế được lập hóa đơn cho khách hàng. 
- **Giá mỗi đơn vị** - Giá thanh toán được đặt cho từng đơn vị của danh mục chi phí. Số tiền được lập hóa đơn cho khách hàng được tính toán dựa trên lượng đơn vị chi phí mà các tư vấn viên báo cáo. Số dặm sử dụng phương pháp giá mỗi đơn vị. Ví dụ: danh mục chi phí số dặm có thể được cấu hình là 30 đô la Mỹ (USD) mỗi ngày hoặc 2 USD mỗi dặm. Khi một tư vấn viên báo cáo số dặm trên một dự án, thì số tiền lập hóa đơn được tính toán dựa trên số dặm mà các tư vấn viên đã báo cáo.

> ![Cấu hình giá cho loại chi phí.](media/basic-guide-14.png)
 
## <a name="project-sales-pricing-and-overrides"></a>Giá bán theo dự án và thay thế

Đối với báo giá dự án và hợp đồng, bảng giá dự án có mô hình thay thế giá khác với bảng giá sản phẩm. Trên dòng báo giá dựa trên danh mục sản phẩm, bạn có thể thay thế giá cho các vai trò và danh mục trực tiếp trên dòng báo giá vì mỗi dòng báo giá trỏ đến chính xác một mục trong danh mục. Tuy nhiên, trên dòng báo giá dựa trên dự án, bạn không thể thay thế giá cho vai trò và danh mục trực tiếp trên dòng báo giá. Để hỗ trợ hai mô hình thay thế khác nhau, PSA đã giới thiệu một liên kết bảng giá mới, đó là bảng giá dự án.

> [!NOTE]
> Bạn nên có một bảng giá riêng cho tài nguyên dự án và các mục trên danh mục của bạn vì sự khác biệt về hành vi giữa hai thứ này khi bạn thay thế giá.

Mỗi thực thể sau có thể có một hoặc nhiều bảng giá bán hàng liên quan cho giá dự án:

- Khách hàng (tài khoản) 
- Cơ hội 
- Báo giá 
- Hợp đồng Dự án

Một liên kết các thực thể này với bảng giá được biểu thị bằng bảng giá dự án. Bạn có thể liên kết một hoặc nhiều bảng giá với các thực thể bán hàng khách hàng, cơ hội, báo giá và hợp đồng dự án.

Bảng giá dự án mặc định không tự động nhập vào bản ghi khách hàng. Tuy nhiên, bạn có thể tự đính kèm bảng giá dự án vào bản ghi khách hàng. Tuy nhiên, bạn nên đính kèm bảng giá dự án chỉ khi có thỏa thuận giá tùy chỉnh với khách hàng. 

Khi một bảng giá dự án được đính kèm vào một thực thể bán hàng, PSA xác nhận thông tin sau:

- Bảng giá là một bối cảnh **Bán hàng**. 
- Tiền tệ của bảng giá phải khớp với loại tiền của khách hàng. 

Trên hợp đồng dự án, PSA sử dụng thứ tự ưu tiên sau đây để tự động đặt bảng giá dự án liên quan:

1. Báo giá
2. Cơ hội
3. Khách hàng 
4. Thiết đặt tổng thể cho PSA

Khi một bảng giá dự án được nhập theo mặc định, PSA sẽ xác thực rằng loại tiền tệ khớp với tiền tệ của khách hàng và các bảng giá mặc định đã nhập có bối cảnh **Bán hàng**.

Bạn có thể liên kết nhiều bảng giá dự án với các thực thể khách hàng, cơ hội, báo giá và hợp đồng dự án. Khả năng này hỗ trợ giá mặc định theo ngày cho một hợp đồng dự án dài, nơi bạn có thể yêu cầu nhiều bảng giá để tính đến khả năng cập nhật giá do lạm phát. Tuy nhiên, nếu bảng giá mà bạn liên kết với thực thể khách hàng, cơ hội, báo giá hoặc hợp đồng dự án có ngày hiệu lực chồng chéo, thì giá mặc định có thể không chính xác. Do đó, bạn phải đảm bảo rằng bảng giá dự án có ngày hiệu lực chồng chéo không liên kết với những thực thể đó.

### <a name="deal-specific-price-overrides"></a>Thay thế giá theo thỏa thuận

Trong PSA, bạn có thể tạo thay thế giá theo thỏa thuận cho giá được chọn trên bảng giá dự án được nhập theo mặc định trên báo giá hoặc hợp đồng dự án.

Theo mặc định, hợp đồng dự án luôn có một bản sao của bảng giá bán hàng chính thay vì một liên kết trực tiếp đến nó. Hành vi này giúp đảm bảo rằng thỏa thuận giá thực hiện với khách hàng cho một bảng kê công việc (SOW) không thay đổi nếu bảng giá chính thay đổi.

Tuy nhiên, trên báo giá, bạn có thể sử dụng một bảng giá chính. Ngoài ra, bạn có thể sao chép một bảng giá chính và chỉnh sửa nó để tạo một bảng giá tùy chỉnh chỉ áp dụng cho báo giá đó. Để tạo một bảng giá mới dành riêng cho báo giá, trên trang báo **Báo giá**, hãy chọn **Tạo giá tùy chỉnh**. Bạn có thể truy cập danh sách giá dự án dành riêng cho thỏa thuận chỉ từ báo giá. 

Khi bạn tạo một bảng giá dự án tùy chỉnh, chỉ các thành phần dự án của bảng giá được sao chép. Nói cách khác, một bảng giá mới được tạo ra như một bản sao của bảng giá dự án hiện có đính kèm báo giá và bảng giá mới này chỉ có giá liên quan đến vai trò và giá theo loại giao dịch.

> ![Xem và định cấu hình giá tùy chỉnh cho hợp đồng dự án.](media/basic-guide-15.png)
  
## <a name="tracking-costs"></a>Theo dõi chi phí

PSA theo dõi chi phí cho việc sử dụng thời gian nguồn nhân lực trên các dự án. PSA cũng theo dõi chi phí cho các chi phí khác phát sinh trong dự án, chẳng hạn như chi phí đi lại.

Giống như tỉ suất hóa đơn, tỷ suất chi phí cho nguồn nhân lực cũng được thiết lập bằng cách sử dụng danh sách giá. Dưới đây là những khác biệt chính trong hành vi của bảng giá chi phí và bảng giá bán hàng:

- Không thể thay thế tỉ suất chi phí của một tài nguyên trên một dự án, hợp đồng hoặc báo giá cụ thể. Tuy nhiên, có thể thay thế tỷ suất hóa đơn trên cơ sở mỗi thỏa thuận nếu thay đổi được thực hiện cụ thể cho bản chất của thỏa thuận này. 

- Một bảng giá chi phí được xử lý theo thứ tự sau đây:

    1. Bảng giá chi phí được đính kèm vào đơn vị tổ chức.
    2. Bảng giá chi phí được đính kèm vào các thông số Project Service. Vì có thể đính kèm bảng giá chi phí ở nhiều loại tiền tệ khác nhau vào tham số Project Service, nên PSA sẽ tiến hành khớp tiền tệ giữa các loại tiền tệ của đơn vị tổ chức ký kết hợp đồng của dự án, hợp đồng hoặc báo giá và tiền tệ của danh sách giá chi phí.
    3. Đối với chi phí, các phương pháp định giá theo chi phí và cố định không áp dụng cho danh sách giá chi phí. Ngay cả khi các phương pháp định giá này được sử dụng trên các dòng danh sách giá chi phí để thiết lập chi phí theo loại giao dịch, thì hệ thống cũng bỏ qua chúng và không có giá chi phí mặc định được nhập.


[!INCLUDE[footer-include](../includes/footer-banner.md)]