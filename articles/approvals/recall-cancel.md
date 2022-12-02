---
title: Thu hồi các mục nhập được phê duyệt trước đây
description: Bài viết này giải thích cách một thành viên nhóm dự án có thể yêu cầu thu hồi các bản ghi thời gian, chi phí và sử dụng vật tư được phi duyệt, cũng như cách người quản lý dự án có thể phê duyệt hoặc từ chối yêu cầu thu hồi.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 54fc7ac2301a4423ebf70b0b67ad489580c347b5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930390"
---
# <a name="recall-previously-approved-entries"></a>Thu hồi các mục nhập được phê duyệt trước đây

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Thành viên nhóm dự án hoặc người khác gửi mục nhập thời gian, chi phí hoặc sử dụng vật tư có thể thu hồi mục nhập đó sau khi nó được phê duyệt. Quy trình thu hồi bao gồm hai bước chính:

1. Người gửi yêu cầu thu hồi.
2. Người phê duyệt phê duyệt yêu cầu thu hồi.

## <a name="request-a-recall"></a>Yêu cầu thu hồi

Làm theo các bước này để yêu cầu thu hồi mục nhập thời gian, chi phí hoặc sử dụng vật tư.

1. Thực hiện theo một trong các bước sau, tùy thuộc vào loại mục nhập mà bạn muốn thu hồi:

    - Đối với mục nhập thời gian, hãy chuyển tới **Dự án** \> **Công việc của tôi** \> **Mục nhập thời gian** và chọn tất cả mục nhập thời gian cho kết hợp dự án hoặc nhiệm vụ cụ thể. Ngoài ra, trong lưới, chọn các ô riêng lẻ cho thời gian vào một ngày cụ thể cho một dự án cụ thể.
    - Đối với mục nhập chi phí, hãy chuyển tới **Dự án** \> **Công việc của tôi** \> **Chi phí** và chọn hàng mục nhập chi phí để thu hồi.
    - Đối với mục nhập sử dụng vật tư, hãy chuyển tới **Dự án** \> **Công việc của tôi** \> **Nhật ký sử dụng vật liệu** và chọn hàng cho mục nhập sử dụng vật tư để thu hồi.

2. Chọn **Thu hồi**. Một hộp thoại xác nhận sẽ xuất hiện. Nếu các mục nhập thời gian, chi phí hoặc sử dụng vật tư đã chọn đã được phê duyệt, bạn sẽ được nhắc nhập lý do để thu hồi.
3. Nhập một lý do để thu hồi rồi chọn **OK** để xác nhận hoạt động. Hệ thống gửi người đã phê duyệt các mục nhập yêu cầu phê duyệt yêu cầu thu hồi.

> [!IMPORTANT]
> Bạn không thể tạo yêu cầu thu hồi cho mục nhập sử dụng vật tư, chi phí hoặc thời gian đã phê duyệt đã được lập hóa đơn cho khách hàng. Nếu thử tạo, bạn sẽ nhận được thông báo cho biết rằng mục nhập thời gian, chi phí hoặc sử dụng vật tư không thể được thu hồi vì đã được lập hóa đơn. Trong trường hợp này, bạn chỉ có thể yêu cầu thu hồi mục nhập nếu một hóa đơn điều chỉnh được sử dụng để cập một khoản tín dụng hoặc hoàn tiền đầy đủ cho khách hàng trên hóa đơn gốc.

## <a name="approve-or-reject-a-recall-request"></a>Phê duyệt hoặc từ chối yêu cầu thu hồi

Thực hiện theo các bước sau để phê duyệt hoặc từ chối yêu cầu thu hồi.

1. Truy cập **Dự án** \> **Công việc của tôi** \> **Phê duyệt**.
2. Trên trang danh sách **Phê duyệt**, hãy thay đổi dạng xem thành **Yêu cầu thu hồi để phê duyệt**. Danh sách các yêu cầu thu hồi đã gửi được hiển thị.
3. Chọn một hoặc nhiều mục nhập, sau đó chọn **Phê duyệt** hoặc **Hủy**.
4. Nếu chọn **Phê duyệt**, bạn nhận được thông báo cảnh báo giải thích ảnh hưởng của phê duyệt. Chọn **OK** để xác nhận hoạt động. Yêu cầu thu hồi đã được phê duyệt.

    –hoặc–

    Nếu bạn chọn **Từ chối**, yêu cầu thu hồi sẽ bị từ chối.

> [!IMPORTANT]
> Khi yêu cầu thu hồi được phê duyệt, giống như khi được yêu cầu, hệ thống sẽ kiểm tra mọi hoạt động lập hóa đơn trên các mục nhập thời gian, chi phí hoặc sử dụng vật tư. Nếu mục nhập đã được lập hóa đơn hoặc có trên hóa đơn dạng nháp, thì người phê duyệt sẽ nhận thông báo lỗi cho biết rằng thời gian hoặc chi phí không thể được phê duyệt để thu hồi vì đã được lập hóa đơn. Trong trường hợp này, người phê duyệt có thể phê duyệt yêu cầu thu hồi chỉ khi một hóa đơn điều chỉnh được sử dụng để cập một khoản tín dụng hoặc hoàn tiền đầy đủ cho khách hàng trên hóa đơn gốc.

## <a name="impact-of-a-recall-request"></a>Ảnh hưởng của yêu cầu thu hồi

Khi phê duyệt được thu hồi sẽ gây tác động tài chính và vận hành.

### <a name="operational-impact"></a>Tác động đến vận hành

Nếu yêu cầu thu hồi được phê duyệt, thì bản ghi phê duyệt được đánh dấu là **Bị từ chối**. Trạng thái của mục nhập được thay đổi thành **Đã trả lại** hoặc **Đã từ chối**, tùy thuộc vào mục nhập đó là thời, chi phí hay sử dụng vật liệu.

Thành viên nhóm dự án có thể xem các mục nhập, chỉnh sửa rồi gửi lại các mục nhập hoặc xóa toàn bộ mục nhập.

Nếu yêu cầu thu hồi bị từ chối, mục nhập vẫn ở trạng thái **Đã phê duyệt** và thành viên nhóm dự án hoặc người phê duyệt cho dự án không thể chỉnh sửa.

### <a name="financial-impact"></a>Tác động tài chính

Nếu yêu cầu thu hồi được phê duyệt, các số liệu thực tế tương ứng cho chi phí và doanh thu được cập nhập theo cách sau:

- Trường **Trạng thái điều chỉnh** được cập nhật thành **Đã điều chỉnh**.
- Trường **Trạng thái thanh toán** được cập nhật thành **Đã hủy**.

Tiếp theo, mục nhập đảo ngược được tạo trong bảng Thực tế. Để tạo các mục nhập đảo ngược, hệ thống sẽ sao chép trên các giá trị trường từ thực tế gốc. Giá trị duy nhất không được sao chép sang là giá trị số lượng. Các giá trị này bị đảo ngược. Thực tế đảo ngược được tạo cho cả thực tế **Chi phí** và **Doanh số chưa lập hóa đơn**. Trường **Trạng thái điều chỉnh** trên số liệu thực tế đã đảo ngược thành **Không thể điều chỉnh** và trường **Trạng thái thanh toán** được đặt thành **Đã hủy**. Vì những thay đổi này, tồn đọng doanh thu và chi tiêu đã ghi trên dự án sẽ không còn tính cho khoản tiền mà những số liệu thực tế này đại diện nữa.

Nếu yêu cầu thu hồi bị từ chối, thì không có ảnh hưởng tài chính nào đối với dự án.

## <a name="changes-to-time-entry-records"></a>Các thay đổi đối với bản ghi mục nhập thời gian

Hình minh họa sau hiển thị các thay đổi xảy ra đối với các mục nhập thời gian đã phê duyệt và bản ghi phê duyệt tương ứng khi chúng được thu hồi.

![Chuyển đổi trạng thái mục nhập thời gian.](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-and-material-usage-entry-records"></a>Các thay đổi đối với bản ghi mục nhập chi phí và sử dụng vật tư

Hình minh họa sau hiển thị các thay đổi xảy ra đối với các mục nhập chi phí và sử dụng vật tư đã phê duyệt và bản ghi phê duyệt tương ứng khi chúng được thu hồi.

![Giao dịch trạng thái mục nhập chi phí.](media/ExpenseEntryStateTransitions.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
