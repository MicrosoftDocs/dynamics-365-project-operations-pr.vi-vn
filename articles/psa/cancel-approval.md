---
title: Huỷ mục nhập thời gian và chi phí đã được phê duyệt trước đó
description: Chủ đề này cung cấp thông tin về cách hủy giao dịch chi phí và thời gian dự án được phê duyệt.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
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
ms.openlocfilehash: bf3d146d2b07723b4d2e6e85eafd6f1b23b8b83f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014772"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a>Huỷ mục nhập thời gian hoặc chi phí đã được phê duyệt trước đó

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Trong phiên bản mới nhất của Dynamics 365 Project Service Automation, người phê duyệt có thể hủy mục nhập thời gian hoặc chi phí mà họ đã phê duyệt trước đó.

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a>Hủy mục nhập thời gian hoặc chi phí đã được phê duyệt trước đó

Hãy làm theo các bước sau để hủy mục nhập thời gian hoặc chi phí mà bạn đã phê duyệt trước đó.

1. Truy cập **Dự án** \> **Công việc của tôi** \> **Phê duyệt**.
2. Trên trang danh sách **Phê duyệt**, thay đổi dạng xem thành **Phê duyệt trước đây của tôi**. Danh sách các mục nhập thời gian và chi phí mà bạn đã phê duyệt trước đó được hiển thị.
3. Chọn một hoặc nhiều mục nhập, sau đó chọn **Hủy phê duyệt**. Bạn nhận được một thông báo cảnh báo.
4. Chọn **OK** để hủy phê duyệt.

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a>Hiểu rõ tác động của việc hủy bỏ một phê duyệt mục nhập thời gian hoặc chi phí

Khi hủy bỏ một chấp thuận, bạn sẽ tác động đến cả tài chính và vận hành.

### <a name="operational-impact"></a>Tác động đến vận hành

Về phía vận hành, khi hủy một phê duyệt, trạng thái của bản ghi sẽ được đặt lại thành **Bản nháp** và phê duyệt không còn xuất hiện trong dạng xem **Phê duyệt trước đây của tôi** nữa. Thay vào đó, phê duyệt bị hủy sẽ xuất hiện trong dạng xem **Mục nhập thời gian cần phê duyệt** hoặc dạng xem **Mục nhập chi phí cần phê duyệt**, tùy thuộc vào đó là mục nhập thời gian hay chi phí. Ngoài ra, trạng thái của mục nhập thời gian hoặc chi phí liên quan được đổi thành **Đã gửi** để mục nhập liên quan nhất quán với phê duyệt có trạng thái **Bản nháp**.

Là người phê duyệt, bạn có thể chỉnh sửa một số trường của phê duyệt có trạng thái **Bản nháp**. Các trường này bao gồm **Loại thanh toán** và **Số giờ có thể lập hóa đơn cho mục nhập thời gian**. Sau khi thực hiện thay đổi, bạn có thể phê duyệt lại bản ghi. Ngoài ra, bạn có thể từ chối mục nhập. Nếu bạn từ chối phê duyệt mục nhập thời gian, thì trạng thái của mục nhập được thay đổi thành **Đã trả lại**. Nếu bạn từ chối phê duyệt một mục nhập chi phí, thì trạng thái được thay đổi thành **Đã từ chối**. Về mặt chức năng, cả mục nhập đã trả về và đã từ chối đều hoạt động giống như mục nhập có trạng thái **Bản nháp**. Thành viên nhóm dự án có thể thực hiện bất kỳ thay đổi nào cần thiết cho mục nhập và sau đó gửi lại để phê duyệt hoặc xóa hoàn toàn mục nhập.

### <a name="financial-impact"></a>Tác động tài chính

Dự án cũng bị ảnh hưởng về tài chính khi phê duyệt bị hủy bỏ. Đầu tiên, thực tế tương ứng cho chi phí và doanh số được cập nhật theo cách sau:

- Trạng thái điều chỉnh được đặt thành **Đã điều chỉnh**.
- Trạng thái lập hóa đơn được đặt thành **Đã hủy**.

Tiếp theo, mục nhập đảo ngược được tạo trong bảng Thực tế. Để tạo các mục nhập đảo ngược, hệ thống sẽ sao chép trên các giá trị trường từ thực tế gốc. Giá trị duy nhất không được sao chép sang là giá trị số lượng. Các giá trị này bị đảo ngược. Thực tế đảo ngược được tạo cho cả thực tế **Chi phí** và **Doanh số chưa lập hóa đơn**. Trường **Trạng thái điều chỉnh** trên thực tế đảo ngược được đặt thành **Không thể điều chỉnh** và trạng thái lập hóa đơn được đặt thành **Đã hủy**.

Sau khi thực hiện các thay đổi này, số lượng được ghi dưới dạng đã sử dụng trên dự án và nhật ký doanh thu trên dự án sẽ không tính đến số lượng của những thực tế này nữa.


[!INCLUDE[footer-include](../includes/footer-banner.md)]