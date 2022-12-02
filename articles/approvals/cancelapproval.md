---
title: Hủy phê duyệt đối với các mục nhập đã được phê duyệt trước đó
description: Bài viết này giải thích cách người quản lý dự án có thể hủy phê duyệt các mục nhập thời gian, chi phí hoặc sử dụng vật liệu đã được phê duyệt trước đó.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 08c2248a5fcfc9b7569871a76bc09234ffd172c7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930482"
---
# <a name="cancel-the-approval-of-previously-approved-entries"></a>Hủy phê duyệt đối với các mục nhập đã được phê duyệt trước đó

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Người quản lý dự án hoặc người phê duyệt đã phê duyệt các mục nhập thời gian, chi phí hoặc sử dụng vật tư có thể hủy phê duyệt các mục nhập đó. 

Hãy làm theo các bước sau để hủy phê duyệt mục nhập thời gian, chi phí hoặc sử dụng vật tư đã được phê duyệt trước đó.

1. Truy cập **Dự án** \> **Công việc của tôi** \> **Phê duyệt**.
2. Trang danh sách **Phê duyệt** hiển thị tất cả các mục nhập thời gian đang chờ phê duyệt. Thay đổi dạng xem thành **Phê duyệt trước đây của tôi**.
3. Chọn các mục phê duyệt thời gian, chi phí hoặc vật tư để hủy. Sau đó, trên Ngăn hành động, chọn **Hủy phê duyệt**.
4. Trong hộp thông báo xác nhận xuất hiện, hãy chọn **OK** để xác nhận hoạt động.

> [!IMPORTANT]
> Bạn không thể hủy phê duyệt mục nhập sử dụng vật tư, chi phí và thời gian đã phê duyệt đã được lập hóa đơn cho khách hàng. Nếu thử tạo, bạn sẽ nhận được thông báo cho biết rằng mục phê duyệt không thể bị hủy vì đã được lập hóa đơn. Trong trường hợp này, bạn chỉ có thể hủy phê duyệt nếu một hóa đơn điều chỉnh được sử dụng để cập một khoản tín dụng hoặc hoàn tiền đầy đủ cho khách hàng trên hóa đơn gốc.

## <a name="impact-of-canceling-the-approval-of-a-previously-approved-entry"></a>Tác động của việc hủy phê duyệt mục nhập được phê duyệt trước đó

Khi hủy bỏ một chấp thuận, bạn sẽ tác động đến cả tài chính và vận hành.

### <a name="operational-impact"></a>Tác động đến vận hành

Nếu việc phê duyệt một mục nhập bị hủy, bản ghi phê duyệt được đánh dấu là **Đã gửi**. Trạng thái của mục nhập được thay đổi thành **Đã gửi**. Trong giai đoạn này, một thành viên nhóm dự án có thể thu hồi mục nhập mà không cần gửi yêu cầu thu hồi.

Người phê duyệt có thể thay đổi các giá trị **Số lượng có thể lập hóa đơn** và **Loại lập hóa đơn**, sau đó phê duyệt mục nhập một lần nữa.

### <a name="financial-impact"></a>Tác động tài chính

Nếu việc phê duyệt một mục nhập bị hủy, các số liệu thực tế tương ứng cho chi phí và doanh thu được cập nhập theo cách sau:

- Trường **Trạng thái điều chỉnh** được cập nhật thành **Đã điều chỉnh**.
- Trường **Trạng thái thanh toán** được cập nhật thành **Đã hủy**.

Tiếp theo, mục nhập đảo ngược được tạo trong bảng Thực tế. Để tạo các mục nhập đảo ngược, hệ thống sẽ sao chép trên các giá trị trường từ thực tế gốc. Giá trị duy nhất không được sao chép sang là giá trị số lượng. Các giá trị này bị đảo ngược. Thực tế đảo ngược được tạo cho cả thực tế **Chi phí** và **Doanh số chưa lập hóa đơn**. Trường **Trạng thái điều chỉnh** trên số liệu thực tế đã đảo ngược thành **Không thể điều chỉnh** và trường **Trạng thái thanh toán** được đặt thành **Đã hủy**. Vì những thay đổi này, tồn đọng doanh thu và chi tiêu đã ghi trên dự án sẽ không còn tính cho khoản tiền mà những số liệu thực tế này đại diện nữa.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
