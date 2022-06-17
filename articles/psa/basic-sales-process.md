---
title: Quy trình bán hàng
description: Bài viết này cung cấp thông tin về các quy trình bán hàng cơ bản.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 18a5ca0592dfefb611094685087351149a0f5e3b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923536"
---
# <a name="sales-processes"></a>Quy trình bán hàng

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Quy trình bán hàng được sử dụng trong tổ chức dựa trên dự án khác với quy trình bán hàng được sử dụng trong tổ chức dựa trên sản phẩm. Sự khác biệt này xảy ra do chu kỳ bán hàng cho các tổ chức dựa trên dự án sẽ dài hơn và yêu cầu các kỹ thuật ước tính tùy chỉnh để phân tích và tạo báo giá cho mỗi thỏa thuận. Dynamics 365 Project Service Automation sử dụng một số chức năng tương tự được sử dụng trong quy trình bán hàng cho Dynamics 365 Sales. Dưới đây là một số ví dụ:

- Thực thể khách hàng tiềm năng được sử dụng để theo dõi quá trình bán hàng.
- Định tính khách hàng tiềm năng được theo dõi dưới dạng cơ hội. Quá trình bán hàng cũng có thể bắt đầu với cơ hội.
- Tất cả các thành phần lạ liên quan cho một cơ hội được truy cập. Những thành phần lạ này bao gồm nhóm bán hàng, bên liên quan, xác suất, định mức, giai đoạn bán hàng, quy trình công việc.
- Nhiều báo giá được tạo cho một cơ hội.
- Báo giá được đánh dấu là **Đóng dưới dạng thắng** để tạo một yêu cầu bán hàng. Trong PSA, yêu cầu bán hàng được tùy chỉnh và được gọi là một hợp đồng dự án.

Hình minh họa sau hiển thị quy trình bán hàng thông thường trong tổ chức dựa trên dự án.

> ![Quá trình bán hàng trong một tổ chức dựa trên dự án.](media/basic-guide-1.png)

## <a name="estimating-a-sale"></a>Ước tính bán hàng
Giá trị của một giao dịch bán hàng có thể được ước tính dựa trên các dự án trước đây đã được cung cấp và sự phức tạp của các dự án. Đối với dự án có liên quan đến phần mở rộng cho các dự án trước đó hoặc các dự án đòi hỏi nhà cung cấp có chuyên môn cao, cần sử dụng mẫu công việc nổi tiếng, thì bạn có thể sử dụng một quy trình ước tính đơn giản hơn. Các dự án phức tạp hơn thường có một quy trình mua hàng lâu hơn. Do đó, có nhiều giai đoạn hơn trong quá trình ước tính bán hàng. Vào đầu quy trình, đội ngũ bán hàng sử dụng thông tin của người quản lý tài khoản và chuyên gia vấn đề (SME) để bắt đầu tạo một ước tính cấp cao cho từng thành phần riêng biệt của công việc được báo giá. Các thành phần này của công việc được đại diện bởi các dòng báo giá. 

Bạn có thể tạo một ước tính cấp cao của báo giá. Cuối cùng, ước tính cấp cao này sẽ được thay thế bằng một ước tính chi tiết hơn dựa trên một kế hoạch dự án mà bạn tạo bằng cách sử dụng các mẫu dự án được chuẩn hóa. Các mẫu này giúp bạn xây dựng một lịch trình và xác định giá trị tiền tệ trên báo giá cũng như các thành phần của nó (dòng báo giá). 

Bạn có thể tạo nhiều báo giá cho một dự án và nhóm chúng theo một loại thực thể cơ hội duy nhất. Cuối cùng, một trong các báo giá đó được đánh dấu là **Đóng dưới dạng thắng** và hợp đồng dự án hoặc bảng kê công việc (SOW) được tạo. Một hợp đồng dự án giữ giá trị ký kết cho mỗi thành phần (dòng hợp đồng) được khách hàng chấp nhận để giao hàng. Một SOW thường được tạo dưới dạng tài liệu Microsoft Word. Tất cả các hóa đơn được gửi đến khách hàng trong quá trình thực hiện dự án sẽ tham chiếu theo hợp đồng dự án hoặc SOW.

Bạn cũng có thể tạo báo giá thay thế theo một loại thực thể cơ hội hoặc thiết lập hệ thống để hợp đồng dự án được tạo khi giành được báo giá. Trong trường hợp này, bạn có thể đính kèm một tài liệu Word đại diện cho SOW vào bản ghi hợp đồng dự án.

![Đóng báo giá để tạo hợp đồng dự án.](media/basic-guide-2.png)

## <a name="configuring-the-sales-process"></a>Đặt cấu hình quy trình bán hàng
Bạn có thể sử dụng dòng quy trình công việc (BPF) trong Microsoft Dynamics 365 để đặt cấu hình quy trình bán hàng của bạn. BPF cung cấp cho nhân viên bán hàng của bạn một giao diện trực quan có hướng dẫn mà họ có thể dùng để tiếp tục di chuyển giao dịch qua các giai đoạn thông thường với công ty của bạn.

Ví dụ: công ty của bạn có thể có sáu giai đoạn sau trong quá trình bán hàng:

1. Bao gồm
2. Ước tính
3. Đánh giá nội bộ
4. Hợp đồng
5. Chuyển giao
6. Đóng

Sáu giai đoạn này được ký hiệu bằng nút hình V (\>) mà bạn chọn để mở rộng trong mỗi loại thực thể cơ hội mà bạn tạo.

![Cấu hình quy trình công việc trong Dynamics 365.](media/basic-guide-3.png)
 
Tổ chức của bạn có thể sử dụng các thực thể khác nhau để đại diện cho cùng một thỏa thuận khi nó phát triển. Vào đầu quy trình bán hàng, một giao dịch được đại diện bằng thực thể Cơ hội. Theo thời gian và chi tiết ngày một nhiều lên, bạn có thể sử dụng các ước tín cấp cao để tạo một hoặc nhiều báo giá. Nếu một trong những báo giá này được đánh giá bởi bên liên quan nội bộ và khách hàng, thì thực thể Báo giá đại diện cho giao dịch. Sau khi khách hàng chấp nhận báo giá, thì hợp đồng dự án hoặc SOW đại diện cho thỏa thuận này. Để hỗ trợ hành vi này, BPF được cấu trúc để từng giai đoạn trong quá trình được liên kết với một bảng cơ sở dữ liệu khác nhau.

Giai đoạn **Định tính** trong quy trình bán hàng có thể được hỗ trợ bằng một thực thể Cơ hội. Các giai đoạn **Ước tính** và **Đánh giá nội bộ** có thể được hỗ trợ bởi một thực thể Báo giá. Các giai đoạn **Hợp đồng**, **Giao hàng** và **Đóng** có thể được hỗ trợ bởi thực thể Hợp đồng dự án.

Khi bạn di chuyển các giao dịch theo giai đoạn, bạn sẽ được nhắc tạo bản ghi thực thể phù hợp để trợ giúp và hướng dẫn bạn trong suốt quy trình. Các giai đoạn có thể có điều kiện. Ví dụ: nếu bạn yêu cầu một nhận xét nội bộ của báo giá chỉ khi báo giá sử dụng bảng giá tùy chỉnh, thì bạn có thể đặt cấu hình điều kiện đó trong giai đoạn phù hợp của quy trình công việc. Khi đó, giai đoạn **Đánh giá nội bộ** chỉ hiển thị cho những báo giá sử dụng bảng giá tùy chỉnh. Đối với tất cả các thỏa thuận và báo giá khác, sau giai đoạn **Ước tính** là giai đoạn **Hợp đồng**.

> [!NOTE]
> PSA có các trang cụ thể cho các thực thể cơ hội, báo giá, đơn đặt hàng và hóa đơn. Bạn phải tạo cơ hội project service, báo giá, đơn đặt hàng và hóa đơn bằng cách sử dụng trang thông tin dự án cho các thực thể này. Nếu bạn sử dụng một trang khác để tạo bản ghi, bạn sẽ không thể mở bản ghi từ trang **Thông tin dự án**. Nếu bạn muốn mở một bản ghi từ trang **thông tin dự án**, thì bạn phải xóa bản ghi và tạo lại nó bằng cách sử dụng trang **Thông tin dự án**. Trên trang **thông tin dự án**, logic kinh doanh cho mỗi loại thực thể này đảm bảo rằng trường **Loại** của bản ghi được đặt chính xác, và tất cả các khái niệm bắt buộc được khởi tạo đúng cách.

> ![Thông tin dự án cho một đơn đặt hàng mới.](media/basic-guide-4.png)
 
## <a name="differences-between-project-service-automation-and-sales"></a>Sự khác biệt giữa Project Service Automation và Sales
Mặc dù quá trình bán hàng trong PSA sử dụng khả năng cơ bản của quá trình bán hàng trong Sales, nhưng nó có một số khác biệt quan trọng vì các biến thể trong thực tiễn kinh doanh của các tổ chức dựa trên dự án. Dưới đây là một số ví dụ:

- **Báo giá dự án**- Trong Project Service Automation, báo giá được đóng sau khi hợp đồng dự án được tạo từ báo giá. Trong Sales, bạn có thể giữ một báo giá mở sau khi bạn đã giành được nó. Lý do cho sự khác biệt này là một kết quả trùng khớp giữa báo giá và hợp đồng dự án sẽ tốt hơn cho các tổ chức dựa trên dự án. 
- **Kích hoạt và sửa đổi** - Trong PSA, kích hoạt và sửa đổi không được hỗ trợ cho báo giá dự án. Trong Sales, báo giá có thể bị khóa để tránh các chỉnh sửa bổ sung.
- **Đóng một báo giá dưới dạng thua hoặc thắng** - Trong PSA, khi một báo giá dự án đóng dưới dạng thắng hoặc thua, thì cơ hội vẫn mở. Tất cả các báo giá khác trên cơ hội được đóng dưới dạng thua. Trong Sales, khi một báo giá được đóng dưới dạng thắng hoặc thua, thì người dùng sẽ được nhắc thực hiện hành động trên cơ hội. Tùy thuộc vào thông tin nhập của người dùng, cơ hội đó có thể bị đóng hoặc vẫn mở.

## <a name="tracking-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>Theo dõi các bản sửa đổi với báo giá và kế hoạch dự án trong chu kỳ bán hàng
Trong PSA, bạn không thể theo dõi các sửa đổi được thực hiện đối với báo giá. Thay vào đó, bạn phải đánh dấu báo giá hiện tại là **Đóng dưới dạng thua**, sau đó tạo báo giá mới. Bạn có thể sao chép một báo giá hoặc nhân bản một dự án dựa trên dự án bằng cách sử dụng PSA.

## <a name="tracking-comments-and-approvals-of-quotes-and-project-contracts"></a>Theo dõi ý kiến và phê duyệt của báo giá và hợp đồng dự án
Bạn có thể quản lý việc đánh giá và phê duyệt báo giá cũng như hợp đồng dự án bằng cách sử dụng tường bản ghi và bài đăng. Tổ chức của bạn có thể tạo luồng công việc và phần bổ trợ tùy chỉnh để chỉ định, chuyển hướng, báo cáo vượt cấp và quản lý thông báo về các mục hoạt động đánh giá và phê duyệt.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
