---
title: Hủy phê duyệt các mục đã được phê duyệt trước đó
description: Chủ đề này giải thích cách người quản lý dự án có thể hủy bỏ việc phê duyệt các mục sử dụng thời gian, chi phí hoặc vật liệu đã được phê duyệt trước đó.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 03d4511e85e9fc8d596b269274c4a7e10016244c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584806"
---
# <a name="cancel-the-approval-of-previously-approved-entries"></a>Hủy phê duyệt các mục đã được phê duyệt trước đó

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Người quản lý dự án hoặc người phê duyệt đã phê duyệt các mục sử dụng thời gian, chi phí hoặc vật liệu trước đó có thể hủy bỏ phê duyệt của họ đối với các mục đó. 

Thực hiện theo các bước sau để hủy phê duyệt mục sử dụng thời gian, chi phí hoặc vật liệu đã được phê duyệt trước đó.

1. Truy cập **Dự án** \> **Công việc của tôi** \> **Phê duyệt**.
2. Các **Phê duyệt** trang danh sách hiển thị tất cả các mục thời gian đang chờ phê duyệt. Thay đổi chế độ xem thành **Phê duyệt trước đây của tôi**.
3. Chọn thời gian, chi phí hoặc phê duyệt vật liệu để hủy bỏ. Sau đó, trên Ngăn hành động, chọn **Hủy phê duyệt**.
4. Trong hộp thông báo xác nhận xuất hiện, hãy chọn **ĐƯỢC RỒI** để xác nhận hoạt động.

> [!IMPORTANT]
> Bạn không thể hủy phê duyệt mục sử dụng thời gian, chi phí và nguyên liệu đã được phê duyệt trước đó đã được lập hóa đơn cho khách hàng. Nếu bạn cố gắng, bạn sẽ nhận được một thông báo cho biết rằng không thể hủy phê duyệt vì nó đã được lập hóa đơn. Trong trường hợp này, bạn chỉ có thể hủy phê duyệt nếu một hóa đơn điều chỉnh được sử dụng để phát hành một khoản tín dụng đầy đủ hoặc hoàn lại tiền cho khách hàng trên hóa đơn gốc.

## <a name="impact-of-canceling-the-approval-of-a-previously-approved-entry"></a>Tác động của việc hủy phê duyệt mục nhập đã được phê duyệt trước đó

Khi hủy bỏ một chấp thuận, bạn sẽ tác động đến cả tài chính và vận hành.

### <a name="operational-impact"></a>Tác động đến vận hành

Nếu việc phê duyệt một mục nhập bị hủy bỏ, thì hồ sơ phê duyệt được đánh dấu là **Đã đệ trình**. Trạng thái của mục nhập được thay đổi thành **Đã đệ trình**. Trong giai đoạn này, một thành viên trong nhóm dự án có thể thu hồi mục nhập mà không cần gửi yêu cầu thu hồi.

Người phê duyệt có thể thay đổi **Số lượng có thể thanh toán** và **Loại thanh toán** và sau đó phê duyệt mục nhập một lần nữa.

### <a name="financial-impact"></a>Tác động tài chính

Nếu việc phê duyệt một mục nhập bị hủy bỏ, các tài liệu thực tế tương ứng về chi phí và doanh thu sẽ được cập nhật theo cách sau:

- Trường **Trạng thái điều chỉnh** được cập nhật thành **Đã điều chỉnh**.
- Trường **Trạng thái thanh toán** được cập nhật thành **Đã hủy**.

Tiếp theo, mục nhập đảo ngược được tạo trong bảng Thực tế. Để tạo các mục nhập đảo ngược, hệ thống sẽ sao chép trên các giá trị trường từ thực tế gốc. Giá trị duy nhất không được sao chép sang là giá trị số lượng. Các giá trị này bị đảo ngược. Thực tế đảo ngược được tạo cho cả thực tế **Chi phí** và **Doanh số chưa lập hóa đơn**. Trường **Trạng thái điều chỉnh** trên số liệu thực tế đã đảo ngược thành **Không thể điều chỉnh** và trường **Trạng thái thanh toán** được đặt thành **Đã hủy**. Vì những thay đổi này, tồn đọng doanh thu và chi tiêu đã ghi trên dự án sẽ không còn tính cho khoản tiền mà những số liệu thực tế này đại diện nữa.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
