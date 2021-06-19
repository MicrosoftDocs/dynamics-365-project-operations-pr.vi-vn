---
title: Bộ phê duyệt
description: Chủ đề này cung cấp thông tin về bộ phê duyệt, yêu cầu và tập hợp con của các thao tác đó.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ac73313420029ece740d0bdb9c21c7abaa9defc6
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116897"
---
# <a name="approval-sets"></a>Bộ phê duyệt

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Bộ phê duyệt có tác dụng nhóm các yêu cầu phê duyệt lại với nhau thành các tập hợp thao tác nhỏ hơn. Việc lập nhóm này giúp cho tính năng Dự án xử lý các mục phê duyệt theo thứ tự, cũng như cho phép thử lại và sắp xếp theo trình tự. Việc lập nhóm sẽ cải thiện độ tin cậy và khả năng truy nguyên của quá trình phê duyệt đối với khối lượng phê duyệt lớn.

Các bộ phê duyệt cho biết trạng thái xử lý tổng thể của các bản ghi liên quan. Khi một bản ghi phê duyệt được xử lý bằng bộ phê duyệt, bản ghi đó sẽ chuyển từ **Đã gửi** thành **Đã phê duyệt** và được hủy liên kết khỏi bộ phê duyệt. Nếu bản ghi đã gửi không được phê duyệt, thì bản ghi đó vẫn ở trạng thái **Đã gửi** và bộ phê duyệt được đánh dấu là không thành công. Bộ phê duyệt ghi lại thông báo lỗi về sự thất bại đó.

## <a name="processing-approvals-and-approval-sets"></a>Xử lý mục phê duyệt và bộ phê duyệt
Các mục phê duyệt được xếp hàng đợi để xử lý sẽ xuất hiện ở dạng xem **Xử lý mục phê duyệt**. Hệ thống sẽ cố gắng xử lý không đồng bộ tất cả các mục nhập nhiều lần, kể cả việc thử lại mục phê duyệt nếu những lần thử trước không thành công.

Trường **Thời gian tồn tại của bộ phê duyệt** ghi lại số lần thử còn lại để xử lý bộ phê duyệt trước khi mục này được đánh dấu là không thành công.

## <a name="failed-approvals-and-approval-sets"></a>Mục phê duyệt và bộ phê duyệt không thành công
Dạng xem **Mục phê duyệt không thành công** liệt kê tất cả các mục phê duyệt cần có sự can thiệp của người dùng. Hãy mở nhật ký bộ phê duyệt được liên kết để xác định nguyên nhân của sự thất bại.
Thao tác chọn **Thử lại** sẽ tăng số lần trong thời gian tồn tại của bộ phê duyệt, chuyển bộ phê duyệt trở lại trạng thái **Đang xử lý** và cố gắng xử lý các bản ghi còn lại.

## <a name="configure-approval-sets"></a>Đặt cấu hình bộ phê duyệt

###  <a name="enable-the-approval-sets-feature"></a>Bật tính năng Bộ phê duyệt
Trước khi bạn bật tính năng Bộ phê duyệt, hãy xác minh rằng không có mục phê duyệt nào hiện đang được xử lý.

- Chuyển đến trang **Thông số dự án** và chọn **Kiểm soát tính năng** > **Bật phê duyệt hiện đại**.

### <a name="turn-off-the-approval-sets-feature"></a>Tắt tính năng Bộ phê duyệt
Trước khi bạn tắt tính năng Bộ phê duyệt, hãy xác minh rằng không có mục phê duyệt nào hiện đang được xử lý.

- Chuyển đến trang **Thông số dự án** và chọn **Kiểm soát tính năng** > **Tắt phê duyệt hiện đại**.

### <a name="configuring-the-asynchronous-threshold"></a>Định cấu hình ngưỡng không đồng bộ 
Khi các bộ phê duyệt được tạo, quá trình xử lý sẽ chuyển sang nền khi số lượng bản ghi đã chọn để phê duyệt vượt quá ngưỡng được chỉ định. Sử dụng trường **Ngưỡng không đồng thời** để đặt cấu hình khi nào hoạt động xử lý phê duyệt nên chạy đồng bộ hoặc không đồng bộ.
Các giá trị hợp lệ là:

  - Không: Tất cả các yêu cầu phải được xử lý không đồng bộ. 
  - Số lớn hơn 0: Các mục phê duyệt chỉ được xử lý không đồng bộ khi số lượng mục phê duyệt đã gửi vượt quá giá trị này.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
