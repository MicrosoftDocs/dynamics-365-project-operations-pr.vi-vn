---
title: Tạo và xác nhận các tạp chí Entry
description: Chủ đề này cung cấp thông tin về cách tạo và xác nhận các tạp chí Entry trong Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: 8cb768337bc197895a837670f93b99b132c97437
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584254"
---
# <a name="create-and-confirm-entry-journals"></a>Tạo và xác nhận các tạp chí Entry

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Bạn sử dụng tạp chí Entry để ghi lại thực tế trực tiếp trong Microsoft Dynamics 365 Project Operations. Khi bạn sử dụng tạp chí Entry, bạn không phải nhập nhật ký sử dụng Thời gian, Chi phí và Vật liệu trong Hoạt động Dự án.

Một tạp chí Entry cho phép bạn tạo nhiều dòng nhật ký. Khi nhật ký được xác nhận, một dòng nhật ký Entry ghi lại thực tế cho các chi tiết sau:

- Chi phí hoặc doanh thu, tùy thuộc vào loại giao dịch đã được chọn.
- Loại giao dịch đã chọn. Các lớp học có sẵn là **Thời gian**, **phí**, **chất**, **giữ lại**, **mốc**, và **Thuế**.
- Dự án và / hoặc một nhiệm vụ được chọn trên dòng nhật ký.

Làm theo các bước sau để tạo một tạp chí Entry trong Hoạt động Dự án.

1. Đi đến **Bán hàng** \> **Giao dịch** \> **Tạp chí**.
2. Trên **Tạp chí đầu vào** trang danh sách, trên Ngăn Hành động, hãy chọn **Mới mẻ** để tạo một nhật ký.
3. Trên **Tạp chí mới** trang, trong **Sự miêu tả**, nhập mô tả của tạp chí.
4. Đảm bảo rằng **Loại tạp chí** trường được đặt thành **Lối vào**, và sau đó chọn **Cứu**. Sau khi tạp chí Entry mới được lưu, **Dòng nhật ký** tab sẽ xuất hiện trên trang tạp chí.
5. Trên **Dòng nhật ký** trên thanh công cụ phía trên lưới, hãy chọn **Mới mẻ** để tạo một dòng nhật ký Entry.
6. Bên trong **Tạo nhanh** hộp thoại để tạo dòng nhật ký Nhập, đặt các trường như được mô tả trong bảng sau.

    | Trường | Description | Tác động chức năng |
    | --- | --- | --- |
    | Lớp giao dịch | Dòng nhật ký có thể được phân loại thành một trong sáu loại giao dịch: **Thời gian**, **phí**, **chất**, **giữ lại**, **mốc**, hoặc **Thuế**. | Các **Thuế** lớp giao dịch đã không được chấp nhận trong Hoạt động dự án. <br> Nếu bạn tạo một **Thuế** lớp giao dịch, nó sẽ không được xử lý bằng cách lập hóa đơn hoặc trong các tính toán chi phí hoặc doanh thu. **Cột mốc** là một lớp giao dịch chỉ doanh thu. <br>Các **Người giữ lại** lớp giao dịch đại diện cho một khoản tạm ứng đã nhận được từ một khách hàng. Nó phải luôn được tạo thành một cặp dòng nhật ký bán hàng đã lập hóa đơn và bán hàng chưa lập hóa đơn. |
    | Loại Giao dịch | Các **Phí tổn**, **hàng nội bộ**, và **Chi phí đơn vị nguồn cung ứng** loại giao dịch nên được sử dụng để ghi lại chi phí.<br> Các **Bán hàng chưa lập hóa đơn** và **Bán hàng được lập hóa đơn** loại giao dịch nên được sử dụng để ghi nhận doanh thu. | Các **Người giữ lại** lớp giao dịch chỉ hoạt động với **Bán hàng chưa lập hóa đơn** và **Bán hàng được lập hóa đơn** các loại giao dịch.<br> Các **Cột mốc** lớp giao dịch chỉ hoạt động với **Bán hàng được lập hóa đơn** Loại giao dịch. <br>Các **Bán hàng nội bộ** và **Chi phí đơn vị nguồn cung ứng** các loại giao dịch chỉ áp dụng cho **Thời gian** lớp giao dịch và những lớp này chỉ có thể quan sát được trên các tạp chí Entry trong scneario triển khai Lite chứ không phải khi triển khai Hoạt động dự án trong các tình huống Tài nguyên / Không có sẵn. |
    | Chọn sản phẩm | Khi mà **Vật chất** lớp giao dịch được chọn, trường này cho phép bạn chỉ định giao dịch quan trọng mà bạn đang tạo dòng nhật ký là một sản phẩm hiện có hay một sản phẩm ghi vào. | Nếu bạn chọn **Ghi sản phẩm**, bạn có thể nhập tên cho sản phẩm. |
    | Sản phẩm | Tham khảo sản phẩm từ danh mục. | |
    | Description | Mô tả dòng tạp chí để giúp bạn dễ dàng xác định. | Đối với dòng nhật ký bán hàng chưa lập hóa đơn, giá trị sẽ được sử dụng làm mô tả khi tạo chi tiết dòng hóa đơn. |
    | Mô tả bên ngoài | Mô tả dòng tạp chí có thể được sử dụng để chia sẻ với các bên liên quan bên ngoài. | Đối với dòng nhật ký bán hàng chưa lập hóa đơn, giá trị sẽ được sử dụng làm mô tả bên ngoài khi tạo chi tiết dòng hóa đơn. Nó cũng có thể xuất hiện trên hóa đơn được gửi cho khách hàng. |
    | Loại thanh toán | Một giá trị cho biết liệu dòng tạp chí sẽ được tính là một thành phần có tính phí, miễn phí hay không tính phí trong dự án. | Trong một quy trình thông thường, loại thanh toán bắt nguồn từ các điều khoản đã thỏa thuận được thiết lập trên hợp đồng. Tuy nhiên, khi bạn ghi lại một dòng nhật ký, bạn có thể nhập một giá trị vào trường này. |
    | Ngày phát hành tài liệu | Sử dụng ngày khi giao dịch xảy ra. | |
    | Ngày bắt đầu | Sử dụng ngày khi giao dịch xảy ra. | Trường này được sử dụng để so sánh với ngày tạo hóa đơn cho các giao dịch của **Bán hàng chưa lập hóa đơn** gõ phím. So sánh này sẽ giúp bạn quyết định xem giao dịch là ngày trong tương lai hay quá khứ. Chỉ các giao dịch ngày trước mới được thêm vào hóa đơn. |
    | Ngày kết thúc | Sử dụng ngày khi giao dịch xảy ra. | |
    | Ngày tháng Kế toán | Sử dụng ngày khi tác động kế toán sẽ được ghi nhận. | |
    | Khách hàng dòng hợp đồng | Theo mặc định, nếu dòng hợp đồng chỉ có một khách hàng, trường này được đặt thành khách hàng trên dòng hợp đồng khi dòng nhật ký được lưu. Nếu dòng hợp đồng có nhiều khách hàng, hãy chọn đúng khách hàng trên dòng hợp đồng. | Nếu hệ thống không thể xác định khách hàng dòng hợp đồng trên dòng nhật ký và nếu nó trống trên thực tế của **Bán hàng chưa lập hóa đơn** loại được tạo từ dòng nhật ký, thực tế sẽ không được lập hóa đơn. |
    | Dự án | Chọn dự án để ghi lại thực tế trên. | Dựa trên dự án, lớp giao dịch và nhiệm vụ đã chọn, hệ thống sẽ cố gắng xác định hợp đồng, dòng hợp đồng và khách hàng dòng hợp đồng. |
    | Tác vụ | Chọn nhiệm vụ để ghi lại thực tế trên. | Nếu bạn liên kết các nhiệm vụ với các dòng hợp đồng trong quá trình thiết lập hợp đồng, hệ thống sẽ sử dụng tác vụ đã chọn, cùng với một dự án và lớp giao dịch, để xác định hợp đồng, dòng hợp đồng và khách hàng dòng hợp đồng. |
    | Danh mục giao dịch | Chọn danh mục giao dịch để ghi lại thực tế trên. | Đối với chi phí, loại giao dịch đã chọn xác định giá mặc định sẽ được nhập vào dòng nhật ký khi nó được lưu. |
    | Vai trò | Trường này có liên quan đến các dòng tạp chí Thời gian. Chọn vai trò của nguồn lực đã dành thời gian cho dự án và / hoặc nhiệm vụ. | Đối với dòng Nhật ký thời gian, nếu bạn sử dụng cấu hình out-of-box cho mục nhập chi phí tài nguyên mặc định và tỷ lệ hóa đơn, thì vai trò đã chọn sẽ được sử dụng cùng với đơn vị cung ứng để xác định giá mặc định sẽ được nhập vào dòng nhật ký khi nó đã được lưu. Nếu bạn sử dụng cấu hình tùy chỉnh để nhập giá mặc định, bạn nên xem lại cấu hình đó để xác định xem **Vai diễn** được sử dụng để nhập các giá trị giá mặc định. |
    | Hợp đồng phụ | Nếu dòng nhật ký thể hiện năng lực được thầu phụ, hoặc các chi phí hoặc nguyên vật liệu được thầu phụ, hãy chọn hợp đồng phụ có liên quan. | Khi các dòng Nhật ký chi phí được ghi lại, hợp đồng phụ được chọn sẽ xác định bảng giá được sử dụng để nhập đơn giá mặc định. |
    | Dòng hợp đồng phụ | Nếu dòng nhật ký thể hiện năng lực hợp đồng phụ, hoặc chi phí hoặc nguyên vật liệu được thầu phụ, hãy chọn dòng hợp đồng phụ có liên quan. | Khi các dòng Nhật ký chi phí được ghi lại, dòng hợp đồng phụ được chọn sẽ đảm bảo rằng các phép tính công suất khả dụng trên dòng hợp đồng phụ được tính toán chính xác. |
    | Phương thức số tiền | Theo mặc định, trường này được đặt thành **Nhân số lượng với giá**. Khi phương pháp này được sử dụng, số tiền sẽ được tính là *Định lượng* ×*Giá*. Phương pháp được hỗ trợ khác là **Giá cố định**. Khi phương pháp này được sử dụng, giá sẽ được đặt thành số tiền và số lượng sẽ không được sử dụng trong tính toán. | |
    | Đơn vị lịch biểu và đơn vị | Cùng với nhau, đơn vị lịch trình và đơn vị xác định đơn vị của số lượng. | Sự kết hợp giữa đơn vị và danh mục giao dịch được sử dụng để nhập giá mặc định cho chi phí. Trong cấu hình mặc định của Hoạt động dự án, sự kết hợp của đơn vị, vai trò và đơn vị cung ứng nguồn lực được sử dụng để nhập giá mặc định cho thời gian. Nếu bạn có cấu hình tùy chỉnh để nhập giá mặc định, cấu hình đó sẽ được sử dụng cùng với đơn vị. Sự kết hợp của sản phẩm và đơn vị được sử dụng để nhập giá mặc định cho vật liệu. |
    | Số lượng | Nhập số lượng. | |
    | Giá | Nếu giá được để trống khi tạo dòng nhật ký, các giá trị liên quan sẽ được sử dụng để nhập giá mặc định, tùy thuộc vào loại giao dịch. Nếu một giá được nhập khi dòng nhật ký được tạo, giá đó sẽ được sử dụng. | |
    | Thuế | Nhập bất kỳ số tiền thuế nào. | Tùy thuộc vào số tiền thuế được nhập, số tiền gia hạn sẽ được tính như *Số lượng* + *Thuế*. |

## <a name="confirm-an-entry-journal"></a>Xác nhận một tạp chí Entry

Sau khi bạn đã nhập tất cả các dòng nhật ký trong một tạp chí Entry, bạn có thể xác nhận tạp chí đó. Quá trình này sẽ ghi lại từng dòng nhật ký dưới dạng các tài liệu thực tế về các dự án thích hợp.

Sau khi một tạp chí được xác nhận, bạn không thể chỉnh sửa nó nữa hoặc bất kỳ dòng nào của nó.

## <a name="actuals-created-by-entry-journal-confirmation"></a>Thực tế được tạo bởi xác nhận tạp chí Entry

Có một vài khác biệt chính giữa các thực tế được tạo bởi xác nhận của Nhật ký đầu vào và các thực tế được tạo ra trong quá trình phê duyệt nhật ký sử dụng Thời gian, Chi phí và Vật liệu và xác nhận hóa đơn trong Hoạt động Dự án:

- Các tạp chí nhập không sử dụng các kết nối giao dịch để liên kết chi phí thực tế với doanh thu bán hàng chưa được lập hóa đơn. Các thực tế được tạo khi nhật ký sử dụng Thời gian, Chi phí và Vật liệu được phê duyệt luôn sử dụng các kết nối giao dịch để liên kết các thực tế bán hàng chưa lập hóa đơn và chi phí.
- Các tạp chí đầu vào không sử dụng nguồn gốc giao dịch để liên kết chi phí thực tế và các thực tế bán hàng chưa lập hóa đơn với bất kỳ hồ sơ gốc nào. Các thực tế được tạo khi nhật ký sử dụng Thời gian, Chi phí và Vật liệu được phê duyệt luôn sử dụng nguồn gốc giao dịch để liên kết các thực tế bán hàng chưa lập hóa đơn và chi phí với mục nhập thời gian ban đầu.
- Khi các hành động bán hàng chưa lập hóa đơn được tạo bằng xác nhận của Nhật ký nhập hóa đơn được lập hóa đơn, các sổ tay bán hàng đã lập hóa đơn được tạo trong quá trình xác nhận hóa đơn được liên kết với các hành động bán hàng chưa lập hóa đơn, theo cách tương tự như các hành động bán hàng chưa lập hóa đơn được tạo khi Thời gian, Chi phí và Nhật ký sử dụng vật liệu được phê duyệt.
- Các dòng nhật ký đầu vào được tạo ra cho thời gian được nhập bởi các nguồn lực liên tổ chức không gây ra các hành động của **Chi phí đơn vị nguồn cung ứng** và **Bán hàng nội bộ** các loại được tạo tự động. Các thực tế này phải được tạo thủ công. Hành vi này khác với hành vi đối với các mục thời gian được ghi lại bởi các nguồn lực giữa các tổ chức. Trong trường hợp đó, khi thời gian được chấp thuận, ứng dụng sẽ tự động tạo các thực tế của **Phí tổn** gõ vào dự án và thực tế của **Chi phí đơn vị nguồn cung ứng** và **Bán hàng nội bộ** loại trên bộ phận sở hữu của nhân viên. Sau đó, nó sử dụng các kết nối giao dịch để liên kết các thực tế đó với nhau và nguồn gốc giao dịch để liên kết chúng với mục nhập thời gian ban đầu.
- Khi các tạp chí Entry được xác nhận, chúng sẽ tạo ra các thông tin thực tế. Tuy nhiên, tạp chí Correction không thể được sử dụng để sửa chữa những thực tế đó. Hành vi này khác với hành vi đối với các hành động được tạo khi nhật ký sử dụng Thời gian, Chi phí và Vật liệu được phê duyệt. Trong trường hợp đó, ứng dụng cho phép bạn sử dụng các tạp chí Sửa lỗi để sửa các thực tế nhằm sửa bất kỳ lỗi nào, với điều kiện là những thực tế đó chưa được lập hóa đơn. Nếu chúng đã được lập hóa đơn, bạn vẫn có thể sửa một khoản tiền thực tế nếu bạn xử lý một khoản tín dụng đầy đủ của khoản tiền thực tế đó cho khách hàng.

> [!NOTE]
> Các tạp chí đầu vào không thực thi các quy tắc mặc định nghiêm ngặt. Do đó, hãy sử dụng các Tạp chí Mục nhập này càng ít càng tốt, đồng thời thận trọng và cẩn thận để đảm bảo rằng bạn không tạo ra dữ liệu tài chính bị hỏng trong hệ thống của mình. Bất cứ khi nào bạn có thể, hãy sử dụng nhật ký sử dụng Thời gian, Chi phí và Vật liệu, thiết lập cột mốc và lưu giữ trên các hợp đồng dự án và quy trình xác nhận hóa đơn dự án thay vì các tạp chí Entry để tạo thực tế.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
