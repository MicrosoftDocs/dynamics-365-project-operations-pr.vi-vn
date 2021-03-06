---
title: Tạm ứng tiền mặt
description: Chủ đề này cung cấp thông tin về tạm ứng tiền mặt.
author: suvaidya
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 209fe0b8a79b2c0689c458c423664cb292da249b
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908730"
---
# <a name="cash-advance"></a>Tạm ứng tiền mặt

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Tạm ứng tiền mặt cho phép nhân viên vay tiền từ công ty của họ trước khi phát sinh bất kỳ chi phí nào. Khi một khoản tạm ứng tiền mặt theo yêu cầu được chấp thuận và thanh toán, nhân viên có thể sử dụng số tiền này cho các chi phí kinh doanh mà họ có thể phải chịu. 

## <a name="create-and-submit-a-cash-advance-request"></a>Tạo và gửi yêu cầu tạm ứng tiền mặt

1. Trong **Chi phí của tôi**, chọn **Tạm ứng tiền mặt** > **Mới** để tạo yêu cầu tạm ứng tiền mặt mới. 
2. Trên trang **Yêu cầu tạm ứng tiền mặt mới**, nhập mục đích chi phí và chọn địa điểm sẽ phát sinh chi phí.
3. Nhập số tiền và đơn vị tiền tệ được yêu cầu, sau đó chọn **Lưu**. 
4. Khi bạn sẵn sàng gửi yêu cầu tạm ứng tiền mặt, trên trang **Yêu cầu tạm ứng tiền mặt**, chọn **Quy trình làm việc** > **Gửi**.

## <a name="modify-a-cash-advance-request"></a>Sửa đổi yêu cầu tạm ứng tiền mặt

Bạn có thể sửa đổi yêu cầu tạm ứng tiền mặt nếu yêu cầu chưa được gửi để phê duyệt.

1. Trong **Chi phí của tôi: Tạm ứng tiền mặt**, tìm và chọn tạm ứng tiền mặt mà bạn muốn chỉnh sửa.
2. Chọn **Chỉnh sửa** và thực hiện các thay đổi cần thiết đối với yêu cầu tạm ứng tiền mặt. 
3. Chọn **Lưu và đóng**.


## <a name="view-cash-advance-requests"></a>Xem yêu cầu tạm ứng tiền mặt
Bạn có thể xem lại danh sách tất cả các khoản tạm ứng tiền mặt đang trong bản nháp, đã nộp, đang xem xét hoặc được thanh toán trong **Chi phí của tôi: Tạm ứng tiền mặt**. 

## <a name="approve-cash-advance-requests"></a>Phê duyệt yêu cầu tạm ứng tiền mặt

Người quản lý hoặc người dùng được định cấu hình làm người phê duyệt trong quy trình làm việc sẽ có thể phê duyệt các khoản tạm ứng tiền mặt được gửi cho họ để đánh giá. 

1. Để chấp thuận tạm ứng tiền mặt, trong **Xử lý các khoản tạm ứng tiền mặt**, chọn **Tạm ứng tiền mặt để tôi đánh giá**.
2. Chọn tạm ứng tiền mặt mà bạn cần đánh giá và chọn **Phê duyệt**.  

## <a name="pay-cash-advances"></a>Thanh toán tạm ứng tiền mặt 
Quy trình sau đây thường được hoàn thành bởi kế toán viên hoặc người dùng có quyền kế toán.

1. Để đăng các khoản tạm ứng tiền mặt đã được phê duyệt, hãy chọn **Các khoản tạm ứng tiền mặt được chấp thuận**, sau đó chọn **Thanh toán và chuyển khoản**.  
2. Cung cấp chi tiết nhật ký cho các khoản tạm ứng tiền mặt, sau đó chọn **OK**. 

## <a name="submit-an-expense-report-against-a-paid-cash-advance"></a>Gửi báo cáo chi phí so với khoản tạm ứng tiền mặt đã trả 

Khi bạn tạo và gửi báo cáo chi phí cho khoản tạm ứng tiền mặt mà bạn đã nhận được, chi phí sẽ được tự động điều chỉnh so với khoản tạm ứng đó. Nếu số tiền tạm ứng của bạn lớn hơn số tiền đã chi tiêu, bạn phải trả lại số dư cho công ty bằng cách sử dụng danh mục chi phí **Trả lại tiền mặt**. Nếu khoản tạm ứng tiền mặt do công ty thanh toán ít hơn số tiền bạn đã chi tiêu, công ty phải hoàn trả số dư cho bạn. 

### <a name="example"></a>Ví dụ:
Bạn dự định đi dự hội nghị từ Seattle đến Thành phố New York. Bạn tạo yêu cầu tạm ứng tiền mặt cho 3000 USD vì bạn đã ước tính chi phí vé hội nghị, vé máy bay, khách sạn, bữa ăn và taxi gần bằng số tiền này. Bạn sẽ không được trả tiền trừ khi người quản lý của bạn chấp thuận yêu cầu này. Sau khi người quản lý của bạn phê duyệt, khoản tạm ứng tiền mặt được yêu cầu sẽ được thanh toán bằng 3000 USD vào tài khoản ngân hàng của bạn. Sau đó bạn tham dự hội nghị. Sau khi hoàn thành chuyến đi của mình, bạn thấy rằng tổng chi tiêu chỉ là 2790 USD. Chọn **Tiền mặt** trong trường **Phương thức thanh toán** và gửi chi phí của bạn cho 2790 USD. Số tiền chi phí đã gửi của bạn tự động được điều chỉnh dựa trên khoản tạm ứng tiền mặt 3000 USD đã cho bạn vay. Bạn hiện nợ công ty số dư 210 USD (3000-2790) và bạn có thể trả lại công ty bằng cách sử dụng danh mục chi phí **Trả lại tiền mặt**. 
