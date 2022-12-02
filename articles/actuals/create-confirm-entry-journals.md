---
title: Tạo và xác nhận Bút toán
description: Bài viết này cung cấp thông tin về cách tạo và xác nhận Nhật ký mục nhập trong Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 138dccd72607d6515eeeffb066fa485f83eabbec
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912358"
---
# <a name="create-and-confirm-entry-journals"></a>Tạo và xác nhận Bút toán

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Bạn sử dụng Nhật ký mục nhập để ghi lại các số liệu thực tế trực tiếp trong Microsoft Dynamics 365 Project Operations. Khi bạn sử dụng Nhật ký mục nhập, bạn không phải nhập nhật ký sử dụng Thời gian, Chi phí và Vật tư trong Project Operations.

Một Nhật ký mục nhập cho phép bạn tạo nhiều dòng nhật ký kế toán. Khi nhật ký được xác nhận, một Dòng nhật ký kế toán mục nhập ghi lại số liệu thực tế cho các chi tiết sau:

- Chi phí hoặc doanh thu, tùy thuộc vào loại giao dịch đã được chọn.
- Lớp giao dịch được chọn. Các lớp có sẵn là **Thời gian**, **Chi phí**, **Vật tư**, **Khoản trả trước**, **Mốc** và **Thuế**.
- Dự án và/hoặc một nhiệm vụ được chọn trên dòng nhật ký kế toán.

Làm theo các bước sau để tạo một Nhật ký mục nhập trong Project Operations.

1. Đi đến **Doanh số** \> **Giao dịch** \> **Nhật ký**.
2. Trên trang danh sách **Nhật ký mục nhập**, trên Ngăn Hành động, hãy chọn **Mới** để tạo một nhật ký.
3. Trên trang **Nhật ký mới**, trong trường **Mô tả**, nhập mô tả của nhật ký.
4. Đảm bảo rằng trường **Loại nhật ký** được đặt thành **Mục nhập**, và sau đó chọn **Lưu**. Sau khi Nhật ký mục nhập mới được lưu, tab **Dòng nhật ký kế toán** sẽ xuất hiện trên trang nhật ký.
5. Trên tab **Dòng nhật ký kế toán** trên thanh công cụ phía trên lưới, hãy chọn **Mới** để tạo Dòng nhật ký kế toán mục nhập.
6. Trong hộp thoại **Tạo nhanh** để tạo Dòng nhật ký kế toán mục nhập, đặt các trường như được mô tả trong bảng sau.

    | Trường | Description | Tác động chức năng |
    | --- | --- | --- |
    | Lớp giao dịch | Dòng nhật ký có thể được phân loại thành một trong sáu lớp giao dịch: **Thời gian**, **Chi phí**, **Vật tư**, **Khoản trả trước**, **Mốc** hoặc **Thuế**. | Lớp giao dịch **Thuế** không được dùng nữa trong Project Operations. <br> Nếu bạn tạo một lớp giao dịch **Thuế**, nó sẽ không được xử lý bằng cách lập hóa đơn hoặc trong tính toán chi phí hoặc doanh thu. **Mốc** là lớp giao dịch chỉ có doanh thu. <br>Lớp giao dịch **Khoản trả trước** đại diện cho một khoản tạm ứng đã được nhận từ một khách hàng. Nó phải luôn được tạo thành một cặp dòng nhật ký kế toán doanh số đã lập hóa đơn và doanh số chưa lập hóa đơn. |
    | Loại Giao dịch | Các loại giao dịch **Chi phí**, **Doanh số liên tổ chức** và **Chi phí đơn vị nguồn lực** nên được sử dụng để ghi lại chi phí.<br> Các loại giao dịch **Doanh số chưa lập hóa đơn** và **Doanh số đã lập hóa đơn** nên được sử dụng để ghi lại doanh thu. | Lớp giao dịch **Khoản trả trước** chỉ hoạt động với các loại giao dịch **Doanh số chưa lập hóa đơn** và **Doanh số đã lập hóa đơn**.<br> Lớp giao dịch **Mốc** chỉ hoạt động với loại giao dịch **Doanh số đã lập hóa đơn**. <br>Loại giao dịch **Doanh số liên tổ chức** và **Chi phí đơn vị nguồn lực** chỉ áp dụng cho lớp giao dịch **Thời gian** và chúng chỉ có sẵn trên Nhật ký mục nhập trong kịch bản triển khai Bản đơn giản, đồng thời không có sẵn khi triển khai Project Operations trong các kịch bản Nguồn lực / Không nhập kho. |
    | Chọn sản phẩm | Khi lớp giao dịch **Vật tư** được chọn, trường này cho phép bạn chỉ định giao dịch vật tư mà bạn đang tạo dòng nhật ký kế toán là một sản phẩm hiện có hay một sản phẩm chọn thêm. | Nếu bạn chọn **Sản phẩm chọn thêm**, bạn có thể nhập tên cho sản phẩm. |
    | Sản phẩm | Một tham chiếu đến sản phẩm từ danh mục. | |
    | Description | Một mô tả cho dòng nhật ký kế toán để nó dễ nhận biết. | Đối với dòng nhật ký kế toán cho doanh số chưa lập hóa đơn, giá trị sẽ được sử dụng làm mô tả khi chi tiết dòng hóa đơn được tạo. |
    | Mô tả bên ngoài | Mô tả dòng nhật ký kế toán có thể được sử dụng để chia sẻ với các bên liên quan bên ngoài. | Đối với dòng nhật ký kế toán cho doanh số chưa lập hóa đơn, giá trị sẽ được sử dụng làm mô tả bên ngoài khi chi tiết dòng hóa đơn được tạo. Nó cũng có thể xuất hiện trên hóa đơn được gửi đến khách hàng. |
    | Loại thanh toán | Một giá trị cho biết liệu dòng nhật ký kế toán có được tính là một thành phần tính phí, miễn phí hay không tính phí trong dự án. | Trong một quy trình thông thường, loại lập hóa đơn bắt nguồn từ các điều khoản đã thỏa thuận được thiết lập trên hợp đồng. Tuy nhiên, khi bạn ghi lại một dòng nhật ký kế toán, bạn có thể nhập một giá trị vào trường này. |
    | Ngày phát hành tài liệu | Sử dụng một ngày khi giao dịch xảy ra. | |
    | Ngày bắt đầu | Sử dụng ngày khi giao dịch xảy ra. | Trường này được sử dụng để so sánh với ngày tạo hóa đơn cho các giao dịch thuộc loại **Doanh số chưa lập hóa đơn**. Phép so sánh này sẽ giúp bạn quyết định xem giao dịch là ngày trong tương lai hay trong quá khứ. Chỉ các giao dịch có ngày trong quá khứ mới được thêm vào hóa đơn. |
    | Ngày kết thúc | Sử dụng ngày khi giao dịch xảy ra. | |
    | Ngày tháng Kế toán | Sử dụng ngày khi tác động kế toán sẽ được ghi lại. | |
    | Khách hàng trên mô tả hợp đồng | Theo mặc định, nếu mô tả hợp đồng chỉ có một khách hàng, trường này được đặt thành khách hàng trên mô tả hợp đồng khi dòng nhật ký kế toán được lưu. Nếu mô tả hợp đồng có nhiều khách hàng, hãy chọn đúng khách hàng trên mô tả hợp đồng. | Nếu hệ thống không thể xác định khách hàng trong mô tả hợp đồng trên dòng nhật ký kế toán và nếu thông tin này trống trên giá trị thực tế loại **Doanh số chưa lập hóa đơn** được tạo từ dòng nhật ký kế toán, thì giá trị thực tế sẽ không được lập hóa đơn. |
    | Dự án | Chọn dự án để ghi lại giá trị thực tế. | Dựa trên dự án, lớp giao dịch và nhiệm vụ đã chọn, hệ thống sẽ cố gắng xác định hợp đồng, mô tả hợp đồng và khách hàng trong mô tả hợp đồng. |
    | Tác vụ | Chọn nhiệm vụ để ghi lại giá trị thực tế. | Nếu bạn liên kết các nhiệm vụ với các mô tả hợp đồng trong quá trình thiết lập hợp đồng, hệ thống sẽ sử dụng nhiệm vụ vụ đã chọn, cùng với một dự án và lớp giao dịch, để xác định hợp đồng, mô tả hợp đồng và khách hàng trong mô tả hợp đồng. |
    | Danh mục giao dịch | Chọn thể loại giao dịch để ghi lại giá trị thực tế. | Đối với chi phí, thể loại giao dịch đã chọn xác định giá mặc định sẽ được nhập trên dòng nhật ký kế toán khi nó được lưu. |
    | Vai trò | Trường này có liên quan đến dòng nhật ký kế toán Thời gian. Chọn vai trò của nguồn lực đã dành thời gian cho dự án và/hoặc nhiệm vụ. | Đối với dòng nhật ký kế toán Thời gian, nếu bạn sử dụng cấu hình dùng sẵn cho mục nhập chi phí nguồn lực mặc định và tỷ lệ thanh toán, thì vai trò đã chọn sẽ được sử dụng cùng với đơn vị cung ứng nguồn lực để xác định giá mặc định sẽ được nhập vào dòng nhật ký kết toán khi nó được lưu. Nếu bạn sử dụng cấu hình tùy chỉnh cho mục nhập giá mặc định, bạn nên xem lại cấu hình đó để xác định xem trường **Vai trò** có được sử dụng để nhập các giá trị giá mặc định hay không. |
    | Hợp đồng phụ | Nếu dòng nhật ký kết toán thể hiện nguồn lực của hợp đồng phụ, hoặc các chi phí hoặc vật tư thầu phụ, hãy chọn hợp đồng phụ có liên quan. | Khi các dòng nhật ký kế toán Chi phí được ghi lại, hợp đồng phụ được chọn sẽ xác định bảng giá được sử dụng để nhập đơn giá mặc định. |
    | Mô tả hợp đồng phụ | Nếu dòng nhật ký kết toán thể hiện nguồn lực của hợp đồng phụ, hoặc các chi phí hoặc vật tư thầu phụ, hãy chọn mô tả hợp đồng phụ có liên quan. | Khi các dòng nhật ký kế toán Chi phí được ghi lại, mô tả hợp đồng phụ được chọn sẽ đảm bảo rằng các tính toán nguồn lực trên mô tả hợp đồng phụ được tính toán chính xác. |
    | Phương thức số tiền | Theo mặc định, trường này được đặt thành **Nhân số lượng với giá cả**. Khi phương pháp này được sử dụng, số tiền sẽ được tính là *Số lượng* × *Giá*. Phương pháp được hỗ trợ khác là **Giá cố định**. Khi phương pháp này được sử dụng, giá sẽ được đặt thành số tiền và số lượng sẽ không được sử dụng trong phép tính. | |
    | Lịch đơn vị và đơn vị | Cùng với nhau, lịch đơn vị và đơn vị xác định đơn vị của số lượng. | Sự kết hợp giữa đơn vị và thể loại giao dịch được sử dụng để nhập giá mặc định cho chi phí. Trong cấu hình mặc định của Project Operations, kết hợp giữa đơn vị, vai trò và đơn vị cung ứng nguồn lực được sử dụng để nhập giá mặc định cho thời gian. Nếu bạn có cấu hình tùy chỉnh để nhập giá mặc định, cấu hình đó sẽ được sử dụng cùng với đơn vị. Kết hợp sản phẩm và đơn vị được sử dụng để nhập giá mặc định cho vật tư. |
    | Số lượng | Nhập số lượng. | |
    | Giá | Nếu giá được để trống khi tạo dòng nhật ký kết toán, các giá trị liên quan sẽ được sử dụng để nhập giá mặc định, tùy thuộc vào loại giao dịch. Nếu một giá được nhập khi dòng nhật ký kế toán được tạo, giá đó sẽ được sử dụng. | |
    | Thuế | Nhập số tiền thuế bất kỳ. | Tùy thuộc vào số tiền thuế được nhập, số tiền cần thanh toán sẽ được tính là *Số tiền* + *Thuế*. |

## <a name="confirm-an-entry-journal"></a>Xác nhận Nhật ký mục nhập

Sau khi bạn đã nhập tất cả các dòng nhật ký kết toán trong Nhật ký mục nhập, bạn có thể xác nhận nhật ký đó. Quá trình này sẽ ghi lại từng dòng nhật ký kết toán dưới dạng số liệu thực tế trên các dự án thích hợp.

Sau khi một nhật ký được xác nhận, bạn không thể chỉnh sửa nhật ký đó hoặc bất kỳ dòng nào của nó.

## <a name="actuals-created-by-entry-journal-confirmation"></a>Giá trị thực tế được tạo khi xác nhật nhật ký Mục nhập

Có một vài điểm khác biệt chính giữa các giá trị thực tế được tạo bởi xác nhận nhật ký Mục nhập và các giá trị thực tế được tạo ra trong quá trình phê duyệt nhật ký sử dụng Thời gian, Chi phí và Vật tư và xác nhận hóa đơn trong Project Operations:

- Nhật ký mục nhập vào không sử dụng các kết nối giao dịch để liên kết chi phí thực tế với doanh số chưa lập hóa đơn thực tế. Các giá trị thực tế được tạo khi nhật ký sử dụng Thời gian, Chi phí và Vật tư được phê duyệt luôn sử dụng các kết nối giao dịch để liên kết các giá trị thực tế về chi phí và doanh số chưa lập hóa đơn.
- Nhật ký mục nhập vào không sử dụng các nguồn gốc giao dịch để liên kết chi phí thực tế và doanh số chưa lập hóa đơn thực tế với bất kỳ bản ghi nguồn nào. Các giá trị thực tế được tạo khi nhật ký sử dụng Thời gian, Chi phí và Vật tư được phê duyệt luôn sử dụng các nguồn gốc giao dịch để liên kết các giá trị thực tế về chi phí và doanh số chưa lập hóa đơn với mục nhập thời gian nguồn.
- Khi doanh số chưa lập hóa đơn thực tế được tạo bởi xác nhận Nhật ký mục nhập được lập hóa đơn, các doanh số đã lập hóa đơn thực tế được tạo trong quá trình xác nhận hóa đơn được liên kết với doanh số chưa lập hóa đơn thực tế, theo cách tương tự như doanh số chưa lập hóa đơn được tạo khi nhật ký sử dụng Thời gian, Chi phí và Vật tư được phê duyệt.
- Các dòng nhật ký kế toán được tạo cho thời gian được nhập bởi các nguồn lực liên tổ chức không khiến giá trị thực tế thuộc loại **Chi phí đơn vị nguồn lực** và **Doanh số liên tổ chức** tự động được tạo. Những giá trị thực tế này phải được tạo thủ công. Hành vi này khác với hành vi cho các mục nhập thời gian được ghi lại bởi các nguồn lực liên tổ chức. Trong trường hợp đó, khi thời gian được phê duyệt, ứng dụng sẽ tự động tạo các giá trị thực tế loại **Chi phí** trên dự án và giá trị thực tế loại **Chi phí đơn vị nguồn lực** và **Doanh số liên tổ chức** trên phần sở hữu của nhân viên. Sau đó, nó sử dụng các kết nối giao dịch để liên kết các giá trị thực tế đó với nhau và nguồn giao dịch để liên kết chúng với mục nhập thời gian nguồn.
- Khi Nhật ký mục nhập được xác nhận, chúng tạo giá trị thực tế. Tuy nhiên, nhật ký Chỉnh sửa không thể được dùng để sửa lại các giá trị thực tế đó. Hành vi này khác với hành vi cho các giá trị thực tế được tạo khi nhật ký sử dụng Thời gian, Chi phí và Vật tư được phê duyệt. Trong trường hợp đó, ứng dụng cho phép bạn sử dụng nhật ký Chỉnh sửa để sửa lại các giá trị thực tế nhằm khắc phục bất kỳ lỗi nào, với điều kiện là những giá trị thực tế đó chưa được lập hóa đơn. Nếu chúng đã được lập hóa đơn, bạn vẫn có thể chỉnh sửa một giá trị thực tế nếu bạn xử lý một khoản tín dụng đầy đủ của giá trị thực tế đó cho khách hàng.

> [!NOTE]
> Nhật ký mục nhập không thực thi các quy tắc mặc định nghiêm ngặt. Do đó, hãy sử dụng các Nhật ký mục nhập này càng ít càng tốt, đồng thời thận trọng để đảm bảo rằng bạn không tạo ra dữ liệu tài chính bị hỏng trong hệ thống của mình. Bất cứ khi nào có thể, hãy sử dụng nhật ký sử dụng Thời gian, Chi phí và Vật tư, thiết lập mốc và khoản trả trước trên các hợp đồng dự án, và quy trình xác nhận hóa đơn dự án thay vì các Nhật ký mục nhập để tạo giá trị thực tế.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
