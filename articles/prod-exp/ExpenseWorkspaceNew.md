---
title: Báo cáo chi phí được thiết kế lại
description: Chủ đề này cung cấp thông tin về trải nghiệm được thiết kế lại và xây dựng lại cho mục nhập báo cáo chi phí trong Microsoft Dynamics 365 Finance. Trong trải nghiệm mới, quá trình hoàn thành báo cáo chi phí sẽ đơn giản hơn và giảm bớt thời gian thực hiện.
author: ryansandness
manager: AnnBe
ms.date: 06/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2019-6-30
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: d076c0a596940cb08433f7ee57dea54903f6078f
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960273"
---
# <a name="redesigned-expense-reports"></a>Báo cáo chi phí được thiết kế lại

Mục nhập báo cáo chi phí đã được thiết kế lại để tinh giản quá trình hoàn thành báo cáo chi phí và giảm bớt thời gian thực hiện. Dưới đây là các thành phần chính của trải nghiệm chi phí mới:

- Một không gian làm việc quản lý chi phí mới cho phép bạn truy cập chi phí của người được ủy quyền.
- Trải nghiệm đối sánh biên lai mới để hiển thị tốt hơn các biên lai cấp tiêu đề và đơn giản hóa quy trình đính kèm biên lai vào dòng chi phí.
- Lưới chỉ đọc mới cho phép bạn xem thêm nhiều dòng chi phí và các cột dữ liệu bổ sung. Giờ đây, bạn có thể xem tất cả các dòng được chia thành từng mục và chia nhỏ, cùng với chi phí chính.
- Một ngăn đơn giản để chỉnh sửa chi phí.
- Các thông báo lỗi, cảnh báo và chính sách được thiết kế lại nhằm giúp bảo đảm rằng bạn có được bối cảnh chính xác để hiểu rõ vấn đề và cách giải quyết. Microsoft đã loại bỏ nhiều thông báo xuất hiện trước khi người dùng có cơ hội hoàn thành nhiệm vụ của họ và giải quyết vấn đề, như thông báo phân khoản chưa hoàn thành.
- Một trang mới để chỉ định trường nào được tổ chức của bạn yêu cầu, trường nào là không bắt buộc và trường nào không nên nắm bắt. Trang này sẽ giúp giảm số lượng trường mà người dùng phải đặt.
- Giao diện mới cho các báo cáo chi phí để báo cáo không còn giống như được thiết kế cho các nhân viên kế toán.

Để kích hoạt trải nghiệm mới, hãy sử dụng không gian làm việc **Quản lý tính năng** để kích hoạt tính năng **Báo cáo chi phí được xây dựng lại**. Khi bạn bật tính năng này, các tác vụ sau sẽ diễn ra:

- Không gian làm việc chi phí hiện có được thay thế bằng không gian làm việc mới.
- Một mục menu mới để hiển thị trường chi phí được thêm vào.
- Không có mục menu hiện có nào cho báo cáo chi phí (trang hiện có) hoặc các trường báo cáo chi phí bị xóa.
- Quy trình làm việc và mọi mục phê duyệt vẫn đưa bạn đến trang báo cáo chi phí hiện có.

## <a name="getting-started-video-for-new-users"></a>Video hướng dẫn dành cho người dùng mới

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE2Y7gO]

Video [Trải nghiệm chi phí trong Dynamics 365 for Finance and Operations](https://youtu.be/Ocy-MsTvEE0) (hiển thị bên trên) được bao gồm trong danh sách phát [Finance and Operations](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) có sẵn trên YouTube.

## <a name="new-features"></a>Tính năng mới

| Tính năng mới | Nội dung mô tả |
|---|----|
| Khả năng hiển thị trường chi phí | Trang thiết lập mới cho phép bạn chỉ định trường nào nên tắt cho tổ chức, trường nào bắt buộc và trường nào được khuyến nghị. |
| Trường bắt buộc | Cấu hình đơn giản mới cho phép bạn thực hiện một số trường bắt buộc mà không cần phải sử dụng khung chính sách. |
| Trường tùy chọn | Một trang thứ hai cho các trường tùy chọn được thêm vào. Bằng cách này, nhân viên sẽ không cảm thấy như thể họ phải thiết lập các trường, nhưng các trường vẫn có thể truy cập dễ dàng. |
| Thêm biên lai chưa đính kèm | Khả năng thêm các biên lai chưa đính kèm vào báo cáo chi phí được hiển thị rõ ràng hơn từ không gian làm việc và trên báo cáo chi phí. |
| Cải thiện tin nhắn | Có khả năng hiển thị tốt hơn đối với các mô tả chi phí có cảnh báo hoặc lỗi. |
| Giảm số lượng tin nhắn trong thanh tin nhắn| Số lượng tin nhắn Infolog đã giảm và một nỗ lực đã được thực hiện để ngăn các tin nhắn trùng lặp xuất hiện trong nhiều trường hợp. |
| Được nhóm cùng các thao tác chung | Giao diện đã được dọn dẹp với việc bổ sung nút thao tác mới cho hầu hết các hành động cấp dòng phổ biến và thêm nút dấu chấm lửng (...) cho tiêu đề và các thao tác ít thường xuyên khác. |
| Không gian làm việc mới để tăng khả năng hiển thị | Một không gian làm việc mới hợp nhất các tính năng và liên kết cho phép người dùng di chuyển đến các khu vực khác nhau. |
| Thêm các chi phí và biên lai hiện có trong quá trình tạo chi phí | Khi tạo báo cáo chi phí, bạn có thể thêm tất cả hoặc các khoản chi phí và biên lai đã chọn. |
| Bộ tính toán tỷ giá hối đoái | Một bộ tính toán tỷ giá hối đoái được thêm vào cho phép bạn tính toán tỷ giá hối đoái cho các giao dịch thanh toán bằng nhiều loại tiền. |
| Lưu và thêm các mô tả chi phí mới | Các nút **Lưu** và **Mới** có sẵn khi chi phí mới được nhập, nhằm giúp bạn nhanh chóng nhập mô tả chi phí. |
| Khả năng hiển thị tốt hơn thành các mô tả chia nhỏ và được chia thành từng khoản mục | Các mục mô tả được phân tách và phân khoản sẽ được thêm trực tiếp vào danh sách chi phí để tăng khả năng hiển thị và giúp bạn dễ dàng xác định xem có bất kỳ lỗi chính sách hay lỗi nào khác không. |
| Hiển thị biên lai trong quá trình chia thành từng khoản mục | Biên lai có thể được hiển thị trong quá trình chia thành từng khoản mục. |

Bản phát hành ban đầu tập trung vào các kịch bản nhập chi phí. Mọi kịch bản phê duyệt hoặc đánh giá báo cáo chi phí sẽ tiếp tục sử dụng trang mục nhập chi phí hiện có.

Các tính năng sau đây có trên trang hiện có nhưng chưa có trên trang mới. Các tính năng này sẽ được giới thiệu lại trong một số bản phát hành tiếp theo:

- Phê duyệt
- Các phê duyệt khoản phải trả và khả năng chỉnh sửa kế toán
- Nhiều điểm nhập
- Tích hợp yêu cầu đi lại
- Thực thể dữ liệu để hiển thị trường chi phí
- Mục nhập chi phí công tác phí
- Quy trình làm việc cấp dòng
- Hỗ trợ người phê duyệt tạm thời
- Thông tin phân khoản nâng cao


[!INCLUDE[footer-include](../includes/footer-banner.md)]