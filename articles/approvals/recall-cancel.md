---
title: Gọi lại các mục đã được phê duyệt trước đó
description: Chủ đề này giải thích cách một thành viên trong nhóm dự án có thể yêu cầu thu hồi hồ sơ sử dụng vật liệu, chi phí và thời gian đã được đệ trình và phê duyệt trước đó cũng như cách người quản lý dự án có thể phê duyệt hoặc từ chối yêu cầu thu hồi.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 18796e803ff73806aaa60b453048ee3160406b40
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586600"
---
# <a name="recall-previously-approved-entries"></a>Gọi lại các mục đã được phê duyệt trước đó

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Một thành viên trong nhóm dự án gửi mục nhập sử dụng thời gian, chi phí hoặc vật liệu có thể thu hồi mục nhập đó sau khi nó đã được phê duyệt. Quy trình thu hồi có hai bước chính:

1. Người gửi yêu cầu thu hồi.
2. Người phê duyệt phê duyệt yêu cầu thu hồi.

## <a name="request-a-recall"></a>Yêu cầu thu hồi

Thực hiện theo các bước sau để yêu cầu thu hồi các mục sử dụng thời gian, chi phí hoặc vật liệu đã được phê duyệt.

1. Thực hiện theo một trong các bước sau, tùy thuộc vào loại mục nhập mà bạn muốn gọi lại:

    - Đối với các mục thời gian, hãy truy cập **Dự án** \> **Công việc của tôi** \> **Thời gian nhập cảnh**, và chọn tất cả các mục thời gian cho sự kết hợp cụ thể giữa một dự án và một nhiệm vụ. Ngoài ra, trong lưới, chọn các ô riêng lẻ cho thời gian vào một ngày cụ thể cho một dự án cụ thể.
    - Đối với các mục nhập chi phí, hãy chuyển đến **Dự án** \> **Công việc của tôi** \> **Chi phí**, và chọn hàng cho mục nhập chi phí để gọi lại.
    - Đối với các mục sử dụng vật liệu, hãy truy cập **Dự án** \> **Công việc của tôi** \> **Nhật ký sử dụng vật liệu**, và chọn hàng cho mục sử dụng vật liệu để gọi lại.

2. Chọn **Thu hồi**. Một hộp thoại xác nhận sẽ xuất hiện. Nếu các mục sử dụng thời gian, chi phí hoặc vật liệu đã chọn đã được phê duyệt, bạn sẽ được nhắc nhập lý do thu hồi.
3. Nhập một lý do để thu hồi rồi chọn **OK** để xác nhận hoạt động. Hệ thống gửi người đã phê duyệt các mục nhập yêu cầu phê duyệt yêu cầu thu hồi.

> [!IMPORTANT]
> Bạn không thể tạo yêu cầu thu hồi cho mục sử dụng thời gian, chi phí hoặc nguyên liệu đã được phê duyệt đã được lập hóa đơn cho khách hàng. Nếu bạn cố gắng, bạn sẽ nhận được một thông báo cho biết rằng không thể gọi lại mục nhập sử dụng thời gian, chi phí hoặc nguyên vật liệu vì nó đã được lập hóa đơn. Trong trường hợp này, bạn chỉ có thể yêu cầu thu hồi mục nhập nếu một hóa đơn điều chỉnh được sử dụng để cấp đầy đủ tín dụng hoặc hoàn lại tiền cho khách hàng trên hóa đơn gốc.

## <a name="approve-or-reject-a-recall-request"></a>Phê duyệt hoặc từ chối yêu cầu thu hồi

Thực hiện theo các bước sau để phê duyệt hoặc từ chối yêu cầu thu hồi.

1. Truy cập **Dự án** \> **Công việc của tôi** \> **Phê duyệt**.
2. Trên trang danh sách **Phê duyệt**, hãy thay đổi dạng xem thành **Yêu cầu thu hồi để phê duyệt**. Danh sách các yêu cầu thu hồi đã gửi được hiển thị.
3. Chọn một hoặc nhiều mục nhập, sau đó chọn **Phê duyệt** hoặc **Hủy**.
4. Nếu chọn **Phê duyệt**, bạn nhận được thông báo cảnh báo giải thích ảnh hưởng của phê duyệt. Chọn **OK** để xác nhận hoạt động. Yêu cầu thu hồi đã được phê duyệt.

    –hoặc–

    Nếu bạn chọn **Từ chối**, yêu cầu thu hồi sẽ bị từ chối.

> [!IMPORTANT]
> Khi việc thu hồi được chấp thuận, cũng như khi được yêu cầu, hệ thống sẽ kiểm tra bất kỳ hoạt động lập hóa đơn nào trên các mục nhập thời gian, chi phí hoặc sử dụng vật liệu. Nếu mục nhập đã được lập hóa đơn hoặc nếu mục đó nằm trên hóa đơn nháp, người phê duyệt sẽ nhận được thông báo lỗi cho biết rằng thời gian hoặc chi phí không thể được chấp thuận để thu hồi vì nó đã được lập hóa đơn. Trong trường hợp này, người phê duyệt chỉ có thể chấp thuận việc thu hồi nếu một hóa đơn sửa chữa được sử dụng để phát hành tín dụng đầy đủ hoặc hoàn lại tiền cho khách hàng trên hóa đơn gốc.

## <a name="impact-of-a-recall-request"></a>Ảnh hưởng của yêu cầu thu hồi

Khi phê duyệt được thu hồi sẽ gây tác động tài chính và vận hành.

### <a name="operational-impact"></a>Tác động đến vận hành

Nếu yêu cầu thu hồi được phê duyệt, thì bản ghi phê duyệt được đánh dấu là **Bị từ chối**. Trạng thái của mục nhập được thay đổi thành **Trả lại** hoặc **Từ chối**, tùy thuộc vào việc đó là một mục nhập thời gian hay nhập chi phí hoặc sử dụng vật liệu.

Thành viên nhóm dự án có thể xem các mục nhập, chỉnh sửa và sau đó gửi lại các mục nhập hoặc xóa hoàn toàn các mục nhập.

Nếu yêu cầu thu hồi bị từ chối, mục nhập vẫn ở trạng thái **Đã phê duyệt** và thành viên nhóm dự án hoặc người phê duyệt cho dự án không thể chỉnh sửa.

### <a name="financial-impact"></a>Tác động tài chính

Nếu yêu cầu thu hồi được phê duyệt, các số liệu thực tế tương ứng cho chi phí và doanh thu được cập nhập theo cách sau:

- Trường **Trạng thái điều chỉnh** được cập nhật thành **Đã điều chỉnh**.
- Trường **Trạng thái thanh toán** được cập nhật thành **Đã hủy**.

Tiếp theo, mục nhập đảo ngược được tạo trong bảng Thực tế. Để tạo các mục nhập đảo ngược, hệ thống sẽ sao chép trên các giá trị trường từ thực tế gốc. Giá trị duy nhất không được sao chép sang là giá trị số lượng. Các giá trị này bị đảo ngược. Thực tế đảo ngược được tạo cho cả thực tế **Chi phí** và **Doanh số chưa lập hóa đơn**. Trường **Trạng thái điều chỉnh** trên số liệu thực tế đã đảo ngược thành **Không thể điều chỉnh** và trường **Trạng thái thanh toán** được đặt thành **Đã hủy**. Vì những thay đổi này, tồn đọng doanh thu và chi tiêu đã ghi trên dự án sẽ không còn tính cho khoản tiền mà những số liệu thực tế này đại diện nữa.

Nếu yêu cầu thu hồi bị từ chối, thì không có ảnh hưởng tài chính nào đối với dự án.

## <a name="changes-to-time-entry-records"></a>Các thay đổi đối với bản ghi mục nhập thời gian

Hình minh họa sau đây cho thấy những thay đổi xảy ra đối với các mục thời gian đã được phê duyệt và các bản ghi phê duyệt tương ứng khi chúng được thu hồi.

![Chuyển đổi trạng thái nhập thời gian.](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-and-material-usage-entry-records"></a>Các thay đổi đối với hồ sơ nhập chi phí và sử dụng nguyên vật liệu

Hình minh họa sau đây cho thấy những thay đổi xảy ra đối với các bút toán sử dụng nguyên vật liệu và chi phí đã được phê duyệt và các hồ sơ phê duyệt tương ứng khi chúng được thu hồi.

![Chuyển đổi trạng thái đầu vào chi phí.](media/ExpenseEntryStateTransitions.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
