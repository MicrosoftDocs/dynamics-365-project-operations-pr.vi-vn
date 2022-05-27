---
title: Tổng quan về quy trình bán hàng
description: Chủ đề này cung cấp thông tin về các quy trình bán hàng cơ bản.
author: rumant
ms.date: 10/29/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e99035798f775de5cd59724a9fe0d7ea6de40034
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578504"
---
# <a name="sales-process-overview"></a>Tổng quan về quy trình bán hàng

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Quy trình bán hàng được sử dụng trong tổ chức dựa trên dự án khác với quy trình bán hàng được sử dụng trong tổ chức dựa trên sản phẩm. Điều này là do chu kỳ bán hàng cho các tổ chức dựa trên dự án sẽ dài hơn và yêu cầu các kỹ thuật ước tính tùy chỉnh để phân tích và tạo báo giá cho từng giao dịch. Dynamics 365 Project Operations sử dụng một số chức năng sau được sử dụng trong quy trình bán hàng:

- Bản ghi Khách hàng tiềm năng được sử dụng để theo dõi quy trình bán hàng.
- Định tính khách hàng tiềm năng được theo dõi dưới dạng cơ hội.
- Tất cả các thành phần lạ có liên quan đối với một cơ hội đều có thể truy cập. Những thành phần lạ này bao gồm nhóm bán hàng, bên liên quan, xác suất, định mức, giai đoạn bán hàng, quy trình công việc.
- Nhiều báo giá được tạo cho một cơ hội.
- Báo giá được đặt trạng thái **Đóng do đã giành được** để tạo một đơn bán hàng. Trong Project Operations, đơn bán hàng được tùy chỉnh và được gọi là hợp đồng dự án.

## <a name="estimate-a-sale"></a>Ước tính giao dịch bán hàng
Giá trị của một giao dịch bán hàng có thể được ước tính dựa trên các dự án đã được bàn giao trước đây và độ phức tạp của các dự án. Đối với dự án có liên quan đến phần mở rộng cho các dự án trước đó hoặc các dự án đòi hỏi nhà cung cấp có chuyên môn cao, cần sử dụng mẫu công việc nổi tiếng, thì bạn có thể sử dụng một quy trình ước tính đơn giản hơn. Các dự án phức tạp hơn thường có một quy trình mua hàng lâu hơn. Do đó, có nhiều giai đoạn hơn trong quá trình ước tính bán hàng. Vào đầu quy trình, đội ngũ bán hàng sử dụng thông tin của người quản lý khách hàng và chuyên gia phụ trách vấn đề (SME) để tạo một ước tính cấp độ cao cho từng thành phần riêng biệt của công việc được báo giá. Các thành phần này của công việc được đại diện bởi các dòng báo giá. 

Bạn có thể tạo một ước tính cấp cao của báo giá. Cuối cùng, ước tính cấp cao này sẽ được thay thế bằng một ước tính chi tiết hơn dựa trên một kế hoạch dự án mà bạn tạo bằng cách sử dụng các mẫu dự án được chuẩn hóa. Các mẫu này giúp bạn xây dựng một lịch trình và xác định giá trị tiền tệ trên báo giá cũng như các thành phần của nó (dòng báo giá). 

Bạn có thể tạo nhiều báo giá cho một dự án và nhóm chúng theo một bản ghi cơ hội duy nhất. Cuối cùng, một trong các báo giá đó được đánh dấu là **Đóng do đã giành được** và hợp đồng dự án hoặc bảng kê công việc (SOW) được tạo. Một hợp đồng dự án giữ giá trị ký kết cho mỗi thành phần (dòng hợp đồng) được khách hàng chấp nhận để giao hàng. Một SOW thường được tạo dưới dạng tài liệu Microsoft Word. Tất cả các hóa đơn được gửi đến khách hàng trong quá trình thực hiện dự án sẽ tham chiếu theo hợp đồng dự án hoặc SOW.

Bạn cũng có thể tạo báo giá thay thế theo một bản ghi cơ hội hoặc thiết lập hệ thống để tạo hợp đồng dự án khi giành được báo giá. Trong trường hợp này, bạn có thể đính kèm một tài liệu Word đại diện cho SOW vào bản ghi hợp đồng dự án.

## <a name="configure-the-sales-process"></a>Đặt cấu hình quy trình bán hàng
Bạn có thể sử dụng dòng quy trình công việc để đặt cấu hình quy trình bán hàng của bạn. Các dòng này cung cấp giao diện trực quan có hướng dẫn để chuyển đi các giao dịch qua các giai đoạn của quy trình bán hàng.

Ví dụ: công ty của bạn có thể có sáu giai đoạn sau trong quá trình bán hàng:

1. Bao gồm
2. Ước tính
3. Đánh giá nội bộ
4. Hợp đồng
5. Chuyển giao
6. Đóng
 
Tổ chức của bạn có thể sử dụng các thực thể khác nhau để đại diện cho cùng một thỏa thuận khi nó phát triển. Vào đầu quy trình bán hàng, một giao dịch được đại diện bằng thực thể Cơ hội. Theo thời gian và chi tiết ngày một nhiều lên, bạn có thể sử dụng các ước tín cấp cao để tạo một hoặc nhiều báo giá. Nếu một trong những báo giá này được đánh giá bởi bên liên quan nội bộ và khách hàng, thì thực thể Báo giá đại diện cho giao dịch. Sau khi khách hàng chấp nhận báo giá, thì hợp đồng dự án hoặc SOW đại diện cho thỏa thuận này. Để hỗ trợ hành vi này, BPF được cấu trúc để từng giai đoạn trong quá trình được liên kết với một bảng cơ sở dữ liệu khác nhau.

Giai đoạn **Định tính** trong quy trình bán hàng có thể được hỗ trợ bằng một thực thể Cơ hội. Các giai đoạn **Ước tính** và **Đánh giá nội bộ** có thể được hỗ trợ bởi một thực thể Báo giá. Các giai đoạn **Hợp đồng**, **Giao hàng** và **Đóng** có thể được hỗ trợ bởi thực thể Hợp đồng dự án.

Khi bạn di chuyển các giao dịch theo giai đoạn, bạn sẽ được nhắc tạo bản ghi thực thể phù hợp để trợ giúp và hướng dẫn bạn trong suốt quy trình. Các giai đoạn có thể có điều kiện. Ví dụ: nếu bạn yêu cầu một nhận xét nội bộ của báo giá chỉ khi báo giá sử dụng bảng giá tùy chỉnh, thì bạn có thể đặt cấu hình điều kiện đó trong giai đoạn phù hợp của quy trình công việc. Khi đó, giai đoạn **Đánh giá nội bộ** chỉ hiển thị cho những báo giá sử dụng bảng giá tùy chỉnh. Đối với tất cả các thỏa thuận và báo giá khác, sau giai đoạn **Ước tính** là giai đoạn **Hợp đồng**.

> [!NOTE]
> Project Operations có các trang cụ thể cho các bản ghi thực thể Cơ hội, Báo giá, Đơn hàng và Hóa đơn. Bạn phải tạo các bản ghi này bằng cách sử dụng các trang thông tin dự án cho các thực thể này. Nếu không, bạn sẽ không thể mở các bản ghi từ trang **Thông tin dự án**. Nếu bạn muốn mở một bản ghi từ trang **Thông tin dự án**, bạn phải xóa bản ghi và tạo lại bằng cách sử dụng trang **Thông tin dự án**, sao cho logic kinh doanh cho từng loại thực thể này đảm bảo rằng trường **Kiểu** của bản ghi được đặt đúng và tất cả các khái niệm bắt buộc đều được khởi tạo đúng cách.


## <a name="track-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>Theo dõi các bản sửa đổi đối với báo giá và kế hoạch dự án trong chu kỳ bán hàng
Trong Project Operations, bạn không thể theo dõi các bản sửa đổi được thực hiện đối với báo giá. Thay vào đó, bạn phải đánh dấu báo giá hiện tại là **Đóng dưới dạng thua**, sau đó tạo báo giá mới. Bạn có thể sao chép một báo giá hoặc nhân bản một báo giá dựa trên dự án.

## <a name="track-comments-and-approvals-of-quotes-and-project-contracts"></a>Theo dõi ý kiến và việc phê duyệt báo giá và hợp đồng dự án
Bạn có thể quản lý việc đánh giá và phê duyệt báo giá cũng như hợp đồng dự án bằng cách sử dụng tường bản ghi và bài đăng. Tổ chức của bạn có thể tạo quy trình làm việc và phần bổ trợ tùy chỉnh để phân công, chuyển hướng, báo cáo và quản lý thông báo về việc đánh giá và phê duyệt các mục công việc.


[!INCLUDE[footer-include](../includes/footer-banner.md)]