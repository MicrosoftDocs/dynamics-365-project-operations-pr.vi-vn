---
title: Báo giá - Các khái niệm chính
description: Chủ đề này cung cấp thông tin về các báo giá dự án và báo giá bán hàng được cung cấp trong Project Operations.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 8a1b5152b76cbcdfb5160a0af78eceec2c42b9a13dfc76701b6ad935318c7ba8
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997902"
---
# <a name="concepts-unique-to-project-based-quotes"></a>Các khái niệm duy nhất cho Báo giá dựa trên dự án

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Trong Dynamics 365 Project Operations, có hai loại báo giá: báo giá dự án và báo giá bán hàng. Hai loại báo giá khác nhau ở những điểm sau:

- **Lưới cho các mục mô tả**: Trên báo giá bán hàng, chỉ có một lưới cho các mục mô tả. Trên báo giá dự án, có hai lưới cho các mục mô tả. Một lưới dành cho các dòng mô tả dự án và lưới còn lại dành cho các dòng mô tả sản phẩm.
- **Kích hoạt và sửa đổi**: Báo giá bán hàng hỗ trợ kích hoạt và sửa đổi. Các quy trình này không được hỗ trợ trên báo giá dự án.
- **Đơn hàng đính kèm**: Bạn có thể đính kèm nhiều đơn hàng vào một báo giá bán hàng. Bạn chỉ có thể đính kèm một hợp đồng dự án vào báo giá dự án.
- **Giành được báo giá**: Khi bạn giành được một báo giá bán hàng, cơ hội liên quan có thể vẫn mở. Sau khi giành được một báo cáo dự án, cơ hội liên quan sẽ đóng lại.
- **Các trường và khái niệm**: Báo giá bán hàng không bao gồm một số trường và khái niệm có trong báo giá dự án. Các trường này bao gồm **Đơn vị ký hợp đồng**, **Người quản lý tài khoản** và **Tên người thanh toán**.  
- **Loại**: Báo giá bán hàng và báo giá dự án cũng được xác định theo một trường dựa trên bộ tùy chọn tên là **Loại**. Đối với báo giá bán hàng, trường này có giá trị **Dựa trên mục hàng**. Đối với báo giá dự án, nó có giá trị **Dựa trên công việc**.

Chủ đề này sẽ tập trung vào các chi tiết của báo giá dự án.

Một báo giá dự án trong Project Operations có thể có nhiều mục hàng hoặc dòng mô tả báo giá. Trong thực tế, một báo giá dự án có hai lưới cho các mục hàng. Một lưới là dành cho các mô tả dựa trên dự án cho phép các ước tính chi tiết. Lưới còn lại là dành cho các mô tả dựa trên sản phẩm sử dụng một đơn giá và phương pháp dựa trên số lượng đơn giản.

- **Dựa trên dự án**: Giá trị báo giá được xác định sau khi bạn ước tính lượng công việc cần thiết. Bạn có thể ước tính cho công việc ở mức độ cao, trực tiếp dưới dạng chi tiết mô tả bên dưới từng dòng báo giá hoặc dựa trên ước tính tổng thể, bằng cách sử dụng dự án và kế hoạch dự án. Mô tả báo giá dựa trên dự án chỉ có trong báo giá dựa trên dự án được tạo bằng cách sử dụng Project Operations. Loại mô tả báo giá này là một biểu mẫu tùy chỉnh của mô tả báo giá điền vào có sẵn trong Microsoft Dynamics 365 Sales.

- **Dựa trên sản phẩm**: Giá trị báo giá được xác định dựa trên số lượng đơn vị được bán và đơn giá bán hàng. Sản phẩm trên một mô tả dựa trên sản phẩm có thể đến từ một danh mục sản phẩm trong Sales hoặc có thể là một sản phẩm mà bạn xác định. Loại mô tả báo giá này cũng được cung cấp trong báo giá dựa trên dự án mà bạn tạo bằng Project Operations.

Số tiền trên báo giá là tổng cộng của tất cả các mô tả dựa trên sản phẩm và mô tả dựa trên dự án.

> [!NOTE]
> Báo giá và mô tả báo giá không bắt buộc trong Project Operations. Bạn có thể bắt đầu quy trình dự án với một hợp đồng dự án (dự án đã bán). Tuy nhiên, luôn phải có một cơ hội, bất kể bạn bắt đầu với một báo giá hay hợp đồng dự án.

## <a name="project-based-quote-lines"></a>Dòng báo giá dựa trên dự án

Mô tả báo giá dựa trên dự án trong Project Operations có các phương thức thanh toán sau đây:

- Thời gian và vật tư
- Giá cố định

### <a name="time-and-material"></a>Thời gian và vật tư

Thời gian và phương thức thanh toán vật tư dựa trên mức tiêu thụ. Khi bạn chọn phương thức thanh toán này, khách hàng được lập hóa đơn khi dự án phát sinh chi phí. Hóa đơn được tạo theo một tần số định kỳ dựa trên ngày. Trong quy trình bán hàng, giá trị báo giá của một thành phần thời gian-và-vật tư chỉ cho một ước tính về chi phí cuối cùng cho khách hàng. Nhà cung cấp không cam kết hoàn thành dự án với giá trị chính xác như báo giá. Các thành phần thời gian và vật tư sẽ khiến khách hàng chịu nhiều rủi ro hơn. Khách hàng có thể muốn thương lượng các điều khoản không vượt quá bổ sung để giảm thiểu rủi ro. Project Operations không hỗ trợ thiết lập các điều khoản không vượt quá.

### <a name="fixed-price"></a>Giá cố định

Trong phương thức thanh toán giá cố định, một nhà cung cấp cam kết phân phối dự án với chi phí cố định cho khách hàng. Khách hàng được lập hóa đơn giá trị báo giá của mô tả báo giá cố định, bất kể chi phí mà nhà cung cấp phải chi trả để cung cấp mô tả báo giá đó. Giá trị mô tả báo giá cố định được lập hóa đơn theo một trong các cách sau: 

- Là một số tiền trọn gói vào đầu hoặc cuối của dự án, hoặc khi đạt đến một mốc dự án. 
- Theo một tần suất theo ngày với cùng một khoản trả góp giá trị cố định trên mô tả báo giá. Những phần trả góp này được gọi là các mốc định kỳ.
- Trong các đợt trả góp có giá trị tiền tệ thống nhất với tiến độ công việc hoặc mốc cụ thể đạt được trên dự án. Trong trường hợp này, giá trị của mỗi phần trả góp có thể khác nhau, nhưng tất cả đều phải thêm vào giá trị cố định trên mô tả báo giá.

Project Operations hỗ trợ cả ba loại lịch trình hóa đơn cho các dòng mô tả báo giá cố định.

## <a name="transaction-classification"></a>Phân loại giao dịch

Các tổ chức dịch vụ chuyên nghiệp thường báo giá và lập hóa đơn khách hàng của họ bằng cách phân loại chi phí. Chi phí được thể hiện dưới các phân loại giao dịch sau đây:

- **Thời gian**: Phân loại này thể hiện chi phí thời gian của nhân công hoặc nhân lực trên một dự án.
- **Chi phí**: Phân loại này thể hiện tất cả các loại chi phí khác trên một dự án. Vì có thể chia chi phí thành nhiều loại nên hầu hết các tổ chức đều tạo các danh mục con, chẳng hạn như đi lại, thuê xe, khách sạn hoặc văn phòng phẩm.
- **Phí**: Phân loại này thể hiện chi phí quản lý khác, tiền phạt và các mục khác được tính cho khách hàng. 
- **Thuế**: Phân loại này thể hiện số tiền thuế mà người dùng thêm vào trong khi họ nhập chi phí.
- **Giao dịch vật tư**: Phân loại này thể hiện giá trị thực tế từ dòng mô tả sản phẩm trên một hóa đơn dự án đã xác nhận.
- **Mốc quan trọng**: Phân loại này được sử dùng theo logic lập hóa đơn giá cố định.

Một hoặc nhiều trong các phân loại giao dịch này có thể liên kết với mỗi dòng báo giá. Sau khi thắng một báo giá, ánh xạ giữa phân loại giao dịch và dòng báo giá được chuyển tới dòng hợp đồng.
  
Ví dụ: báo giá có thể chứa hai dòng báo giá sau đây: 

- Công việc tư vấn sử dụng một phương thức thanh toán thời gian và vật tư, trong đó áp dụng phân loại giao dịch thời gian và phí. Ví dụ: tất cả giao dịch thời gian và phí cho dự án ví dụ **Triển khai Dynamics AX** được lập hóa đơn cho khách hàng dựa trên thời gian và vật tư sử dụng. 
- Chi phí đi lại liên quan sử dụng phương thức thanh toán giá cố định. Ví dụ: tất cả chi phí đi đi lại cho dự án ví dụ **Triển khai Dynamics AX** được lập hóa đơn ở giá trị tiền tệ cố định.

> [!NOTE]
> Tổ hợp phân loại dự án và giao dịch của **Thời gian**, **Chi phí** và **Phí** được liên kết với một dòng báo giá hoặc dòng hợp đồng phải thống nhất. Nếu cùng một tổ hợp loại dự án và giao dịch được liên kết với nhiều dòng mô tả hợp đồng hoặc mô tả báo giá, Project Operations sẽ hoạt động không chính xác.

## <a name="billing-types"></a>Loại thanh toán

Trường **Loại thanh toán** xác định khái niệm về khả năng tính phí. Đó là một bộ tùy chọn có các giá trị có thể có sau đây:

- **Có thể tính phí**: Chi phí cộng dồn trong vai trò/danh mục này là một chi phí trực tiếp nhằm thúc đẩy việc thực hiện dự án và khách hàng sẽ thanh toán cho công việc này. Có thể quản lý thanh toán dưới dạng thỏa thuận giá cố định hoặc thời gian và vật tư. Tuy nhiên, nhân viên dành thời gian này sẽ nhận được tín dụng tương ứng cho mức sử dụng có thể lập hóa đơn của họ.
- **Không thể tính phí**: Chi phí cộng dồn trong vai trò/danh mục được coi là chi phí trực tiếp nhằm thúc đẩy việc thực hiện dự án, ngay cả khi khách hàng không nhận ra điều này và không thanh toán cho công việc này. Nhân viên dành thời gian này sẽ không được ghi nhận thời gian làm việc có thể tính phí.
- **Bổ trợ**: Chi phí cộng dồn trong vai trò/danh mục này được coi là một chi phí trực tiếp nhằm thúc đẩy việc thực hiện dự án và khách hàng có nhận ra điều này. Nhân viên dành thời gian này sẽ được ghi nhận thời gian làm việc có thể tính phí. Tuy nhiên, chi phí này không tính cho khách hàng.
- **Không có sẵn**: Chi phí phát sinh trên các dự án nội bộ không yêu cầu theo dõi doanh thu sẽ được theo dõi bằng tùy chọn này.

## <a name="invoice-schedule"></a>Lịch trình hóa đơn

Lịch trình lập hóa đơn là một loạt những ngày lập hóa đơn cho dự án. Bạn có thể tùy ý tạo một lịch trình hóa đơn trên một dòng báo giá. Mỗi dòng báo giá có thể có lịch trình hóa đơn riêng. Để tạo một lịch trình hóa đơn, bạn phải cung cấp các giá trị thuộc tính sau:

- Ngày bắt đầu lập hóa đơn 
- Ngày giao hàng đại diện cho ngày kết thúc lập hóa đơn trên dự án
- Tuần suất hóa đơn

Ba giá trị thuộc tính này được sử dụng để tạo ra một nhóm ngày dự kiến để bắt đầu lập hóa đơn.

## <a name="invoice-frequency"></a>Tần suất của hóa đơn

Tần suất hóa đơn là một thực thể lưu trữ các giá trị thuộc tính giúp thể hiện tần suất tạo hóa đơn. Các thuộc tính sau đây thể hiện hoặc xác định thực thể tần suất hóa đơn:

- **Khoảng thời gian**: Các khoảng thời gian theo hàng tháng, hai tháng một lần và hàng tuần được hỗ trợ. 
- **Số lần chạy mỗi khoảng thời gian**: Đối với khoảng thời gian theo hàng tuần và hai tuần một lần, bạn chỉ có thể xác định một lần chạy mỗi khoảng thời gian. Đối với khoảng thời gian hàng tháng, bạn có thể xác định từ một đến bốn lần chạy mỗi khoảng thời gian. 
- **Ngày chạy**: Các ngày chạy thao tác lập hóa đơn. Bạn có thể đặt cấu hình thuộc tính này theo hai cách:
  - **Ngày trong tuần**: Ví dụ: bạn có thể chỉ định chạy thao tác lập hóa đơn vào thứ Hai hàng tuần hoặc vào ngày đầu tuần thứ hai hàng tháng. Khách hàng phải đặt hóa đơn để chạy vào một ngày làm việc có thể thích loại cấu hình này. 
  - **Ngày theo lịch**: Ví dụ: bạn có thể chỉ định chạy thao tác lập hóa đơn vào ngày mùng bảy và ngày hai mươi mốt hàng tháng. Một số tổ chức có thể thích loại cấu hình này vì nó giúp đảm bảo chạy lập hóa đơn theo một lịch trình cố định mỗi tháng.
  
### <a name="invoice-schedule-for-a-fixed-price-quote-line"></a>Lịch trình hóa đơn cho một dòng báo giá cố định

Đối với dòng báo giá cố định, bạn có thể sử dụng lưới **Lịch trình hóa đơn** để tạo các mốc lập hóa đơn bằng với giá trị của dòng báo giá.

- Để tạo các mốc lập hóa đơn được chia bằng nhau, hãy chọn một tần suất hóa đơn, nhập ngày bắt đầu lập hóa đơn trên một dòng báo giá và chọn **Ngày hoàn thành yêu cầu** cho báo giá trong phần **Tóm tắt** của tiêu đề báo giá. Sau đó chọn **Tạo mốc định kỳ** để tạo các mốc chia đều dựa trên tần suất hóa đơn đã chọn. 
- Để tạo một cột mốc thanh toán trọn gói, hãy tạo ra một mốc, sau đó nhập giá trị dòng báo giá làm số lượng cột mốc.
- Để tạo các cột mốc lập hóa đơn dựa trên các tác vụ cụ thể trong kế hoạch dự án, hãy tạo một cột mốc và ánh xạ tới thành phần lịch biểu của dự án trong giao diện người dùng cột mốc thanh toán.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
