---
title: Dự báo và ngân sách dự án
description: Microsoft Dynamics 365 Finance cung cấp tính năng dự báo và ngân sách dự án để quản lý và kiểm soát dự án của bạn.
author: Yowelle
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ForecastModel, ProjYearEndProcess
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23501
ms.assetid: 4e6d1384-19a2-4232-b3f3-d2590c218bd7
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 47ea4c49a76a2bb0a1855fce2e9a874b4044e429d963c08392ec0ab471f89329
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988092"
---
# <a name="project-forecasts-and-budgets"></a>Dự báo và ngân sách dự án

[!include [banner](../includes/banner.md)]

Có hai cách quản lý và kiểm soát dự án của bạn: dự báo dự án và ngân sách dự án. 

Sử dụng tính năng dự báo nếu tổ chức của bạn có quan điểm ưu tiên hoạt động, và nếu nó tập trung vào doanh thu và chi phí nảy sinh trong các giao dịch cụ thể. Sử dụng tính năng lập ngân sách dự án nếu tổ chức của bạn chú trọng hơn vào các khoản tài chính. 

Cả dự báo dự án và ngân sách dự án đều sử dụng mô hình dự báo để nắm giữ số tiền giao dịch dự kiến. 

Mỗi phương pháp lại có những ưu điểm riêng. Bạn nên cân nhắc những điểm sau đây trước khi chọn phương thức cho tổ chức của mình.

|   Phương pháp phân bổ       |           Dự báo dự án            |        Lập ngân sách dự án                           |
|---------------------------|------------------------------------------|----------------------------------------------------|
| **Phân bổ thời gian**     | Bạn không thể phân bổ rõ ràng các giao dịch trong kỳ tài chính. Thay vào đó, dự báo và kiểm soát dự báo dựa trên vòng đời của dự án. Bởi vì dự báo dựa trên một ngày cụ thể, bạn phải suy ra khoảng thời gian từ ngày đó. | Bạn có thể phân bổ rõ ràng các giao dịch trong toàn bộ dự án hoặc kỳ tài chính. Nếu bạn phân bổ trong một khoảng thời gian, bạn có thể chuyển tiếp số tiền chưa sử dụng sang kỳ tài chính tiếp theo. |
| **Xem giao dịch**  | Bạn có thể xem giao dịch trong các biểu mẫu dự báo, nơi hiển thị dự báo cho toàn bộ công ty và cho tất cả các dự án, bất kể hệ thống cấp bậc. Để tập trung vào một dự án cụ thể, bạn phải lọc dữ liệu.                                       | Bạn có thể xem các giao dịch được lập ngân sách cho một hệ thống cấp bậc dự án. Do đó, bạn có thể xem chi tiết giao dịch của một dự án chính hoặc các dự án phụ.                 |
| **Các biến giao dịch** | Khi nhập các giao dịch dự báo, bạn có thể sử dụng mọi thuộc tính tồn tại cho một giao dịch thực tế. Điều này cho phép dự báo chi tiết hơn. Ví dụ: bạn có thể nhập chi tiết về số lượng, nhân viên, hạng mục hoặc thuộc tính dòng.         | Khi nhập chi tiết ngân sách, bạn chỉ có thể sử dụng số tiền, thể loại và hoạt động.                    |
| **Bảo mật**              | Dự báo dựa trên các giao dịch mà bạn nhập vào các biểu mẫu dự báo và không liên quan đến cơ chế kiểm soát quy trình. Bất kỳ nhân viên nào có quyền đối với biểu mẫu dự báo đều có thể sửa đổi thông tin mà không cần phê duyệt.                                        | Lập ngân sách sử dụng hệ thống quy trình làm việc, cho phép quản lý thay đổi và cho phép bạn lưu giữ lịch sử những lần sửa đổi.         |
| **Loại mục nhập**           | Các mục nhập giao dịch dự báo dựa trên số lượng đơn vị, cũng như chi phí và đơn giá bán hàng.  | Chi tiết ngân sách dựa trên số tiền, được phân chia thành chi phí và doanh thu.                                          |
| **Mô hình dự báo**       | Vì mỗi dự báo phải được liên kết với một mô hình, bạn có thể tạo nhiều mô hình dự báo và cũng có thể thiết lập các mô hình con.           | Tính năng lập ngân sách dự án giới hạn các mô hình dự báo được sử dụng để lập ngân sách. Ít mô hình dự báo hơn có thể giúp tăng tính nhất quán trong các dự báo.                           |
| **Thấu chi**         | Bạn chỉ có thể cho phép hoặc không cho phép nhập các giao dịch sẽ gây ra thấu chi.   | Lập ngân sách dự án cung cấp các tùy chọn kiểm soát bổ sung cho người dùng. Bạn có thể cho phép cảnh báo và thấu chi.                    |
| **Bộ điều khiển**               | Sử dụng tính năng giảm dự báo để kiểm soát dự báo. Số tiền thực tế được trừ vào số dư giao dịch dự báo mà không có biên bản kiểm tra nào. Điều này có thể gây khó khăn hơn trong việc theo dõi các giao dịch thực tế đã xảy ra ở đâu.                   | Trong kiểm soát ngân sách dự án, số tiền thực tế được trừ vào số tiền trong ngân sách còn lại. Điều này cho phép một biên bản kiểm tra rõ ràng hơn.                                   |

## <a name="project-forecasts"></a>Dự báo dự án
Khi sử dụng dự báo dự án, bạn có thể nhập các giao dịch dự báo trong các biểu mẫu dự báo cho từng loại giao dịch. Mọi thuộc tính có sẵn cho một giao dịch thực tế đều có thể được sử dụng cho một giao dịch dự báo – ví dụ: lợi nhuận dòng, thuộc tính dòng, nhân viên hoặc mô tả. Bạn cũng có thể dự đoán bao lâu sau khi phát sinh chi phí thì sẽ lập hóa đơn cho khách hàng. 

Các giao dịch dự báo dự án dựa trên đơn vị và số tiền. 

Bạn phải liên kết từng dự báo dự án với một mô hình dự báo. Khi bạn nhập một giao dịch dự báo, mô hình dự báo sẽ tự động được gợi ý. Mô hình dự báo hoạt động như một vùng chứa cho các giao dịch dự báo. 

Bạn có thể chỉ định các mô hình dự báo làm mô hình con cho một mô hình. Điều này cho phép bạn dự báo theo khu vực, khoảng thời gian hoặc bộ phận. Bạn có thể sao chép các giao dịch dự báo trong một mô hình để tạo một mô hình mới và bạn cũng có thể chuyển các giao dịch sang sổ cái chung. Do có mối quan hệ 1:1 giữa dự báo và mô hình, nên mỗi mô hình dự báo tạo ra một ngân sách riêng cho một dự án. 

Các mô hình dự báo có thể sử dụng tính năng giảm dự báo làm cơ chế kiểm soát cho các dự án. Trong tính năng giảm dự báo, các giao dịch thực tế sẽ giảm số dư của giao dịch dự báo. Tuy nhiên, vì tính năng giảm dự báo được áp dụng cho dự án cao nhất trong hệ thống cấp bậc, nên tính năng này chỉ cho thấy hạn chế những thay đổi trong dự báo. Ví dụ: nếu một nhân viên được liên kết với dự án nhỏ, các giao dịch thực tế cho nhân viên đó sẽ được đăng lên dự án chính. Điều này có thể gây khó khăn cho việc theo dõi thay đổi, vì bạn không thể dễ dàng xác định giao dịch nào trong dự án nhỏ nào đã gây ra việc giảm số tiền dự báo. Do đó, bạn nên tạo một bản sao của mô hình dự báo tính năng giảm dự báo sử dụng. Sau đó, bạn có thể sử dụng các báo cáo để xem những gì được dự báo ban đầu. 

Bạn có thể sửa đổi, sao chép, xóa hoặc chuyển các dự báo của dự án sang ngân sách sổ cái chung. Tuy nhiên, không có kiểm soát về quy trình. Bất kỳ nhân viên nào có quyền đối với biểu mẫu dự báo đều có thể sửa đổi mà không cần xét duyệt.

-   **Sửa đổi** – Bạn có thể sửa đổi giao dịch dự báo trong cùng biểu mẫu mà các mục nhập ban đầu được tạo.
-   **Sao chép hoặc xóa** – Khi bạn sao chép các giao dịch dự báo, bạn sao chép các dòng giao dịch của mô hình dự báo này sang mô hình dự báo khác. Khi bạn xóa dự báo, bạn sẽ xóa các giao dịch dự báo khỏi mô hình dự báo. Để hạn chế các giao dịch dự báo bị sao chép hoặc xóa, hãy chọn các loại và ngày giao dịch cụ thể. Điều này cho phép bạn chỉ sao chép hoặc xóa các phần cụ thể của dự báo.
-   **Chuyển** – Khi bạn chuyển dự báo dự án sang ngân sách sổ cái chung, bạn chuyển các giao dịch dự báo của mô hình dự báo sang ngân sách sổ cái chung. Bạn có thể ghi đè mọi giao dịch đã chuyển trước đó trong ngân sách sổ cái chung mà bạn chuyển dự báo dự án của mình sang.

## <a name="project-budgets"></a>Ngân sách dự án
Lập ngân sách dự án là một phương pháp đơn giản hơn so với dự báo, mặc dù nó tích hợp với các mô hình dự báo. Nó sử dụng một biểu mẫu mục nhập duy nhất cho các chi tiết và bản sửa đổi ngân sách ban đầu, đồng thời cho phép các dự báo chỉ dựa trên số tiền, thể loại hoặc hoạt động. 

Trong lập ngân sách dự án, tất cả ngân sách ban đầu và các bản sửa đổi phải được gửi đến quy trình làm việc dự án để được phê duyệt. Quy trình làm việc cung cấp cho bạn khả năng kiểm soát tốt hơn đối với quy trình và tạo bản ghi lịch sử thay đổi. 

Lập ngân sách dự án giống như lập ngân sách sổ cái chung, nhưng nhanh hơn và dễ thiết lập hơn. Nhiều tùy chọn trong lập ngân sách sổ cái chung, chẳng hạn như chuỗi số hoặc đơn vị tiền tệ, không cần phải được thiết lập riêng cho các dự án.

Ngân sách dự án tự động được liên kết với hai mô hình dự báo, một cho ngân sách ban đầu và một cho ngân sách còn lại. Do đó, các báo cáo dựa trên mô hình dự báo có thể sử dụng dữ liệu ngân sách. Khi ngân sách dự án được cam kết, hệ thống tạo ra giao dịch dự báo dựa trên các mô hình liên kết, được sử dụng cho mục đích báo cáo và kiểm soát.

## <a name="forecast-models"></a>Mô hình dự báo
Các mô hình dự báo có hệ thống cấp bậc một lớp. Điều này có nghĩa là mỗi dự báo dự án phải được liên kết với một mô hình dự báo.

Nếu bạn sử dụng dự báo dự án, bạn có thể xác định các mô hình là mô hình con. Sau đó, bạn có thể tạo dự báo theo bộ phận, khoảng thời gian hoặc khu vực. Ví dụ: bạn có thể tạo mô hình dự báo cho một năm, sau đó tạo mô hình con cho các dự báo khu vực Đông Bắc, Đông Nam, Tây Bắc và Tây Nam mà người đứng đầu khu vực gửi. Bằng cách chọn các tùy chọn khác nhau trong các báo cáo có sẵn, bạn có thể xem thông tin theo tổng dự báo hoặc theo mô hình con.





[!INCLUDE[footer-include](../includes/footer-banner.md)]