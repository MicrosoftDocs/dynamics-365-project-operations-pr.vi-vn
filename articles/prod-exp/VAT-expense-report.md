---
title: Hoàn thuế GTGT
description: Chủ đề này sẽ giải thích cách thu hồi tiền hoàn lại cho các giao dịch thuế giá trị gia tăng (VAT).
author: saraschi2
ms.date: 02/26/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 76706fd8ced58063b05bc8ebe4b25c1dddbf0890e72e9c7194d17ff2937dc8ca
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986067"
---
# <a name="vat-recovery"></a>Hoàn thuế GTGT 

Để nhận được tiền hoàn lại cho các giao dịch đủ điều kiện về thuế giá trị gia tăng (VAT), công ty hoặc tổ chức phải xác định, thu thập, xác minh và gửi thông tin chính xác. Quá trình này bao gồm nhiều nhiệm vụ và có thể bao gồm một số nhân viên hoặc vai trò (tùy thuộc vào quy mô công ty của bạn).

Để thu hồi VAT bằng cách sử dụng Quản lý chi phí, bạn phải hoàn thành các điều kiện tiên quyết sau:

- Mã số thuế phải được tạo cho quốc gia/khu vực được phân bổ cho các loại chi phí.
- Một nhóm thuế bán hàng phải được tạo cho mỗi mã số thuế.
- Mục mã số thuế bán hàng phải được tạo cho mỗi nhóm thuế bán hàng.

Sau khi xong các điều kiện tiên quyết, nhân viên sẽ thực hiện theo các bước sau để yêu cầu hoàn lại tiền cho các giao dịch VAT.

1. Trên báo cáo chi phí, hãy nhập thông tin thuế về các giao dịch thẻ tín dụng để xác định các khoản hoàn thuế VAT đủ điều kiện.
2. Đảm bảo rằng tất cả thông tin thuế đã hoàn tất, sau đó đăng báo cáo chi phí.
3. Xử lý các chi phí đủ điều kiện để thu hồi thuế GTGT quốc tế.
4. Gửi dữ liệu hoàn thuế VAT cho nhà cung cấp bên thứ ba để nộp tờ khai hoàn thuế quốc tế.
5. Xử lý chi phí hoàn thuế GTGT trong nước.

Các phần sau đây cung cấp các ví dụ cho thấy cách thức hoàn thành từng bước của nhân viên Contoso.

## <a name="on-an-expense-report-enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>Trên báo cáo chi phí, hãy nhập thông tin thuế về các giao dịch thẻ tín dụng để xác định các khoản hoàn thuế VAT đủ điều kiện

Nancy, một đại diện bán hàng của Contoso làm việc tại Hoa Kỳ, vừa trở về sau một chuyến công tác bán hàng ở Vương quốc Anh. Trong chuyến đi, cô ấy phát sinh một số chi phí thẻ tín dụng cá nhân cho các bữa ăn. Nancy hiện phải tạo một báo cáo chi phí để đối chiếu các khoản chi của mình.

Khi Nancy nhập thông tin trên báo cáo chi phí của mình, cô chọn **Vương quốc Anh** trong trường **Quốc gia/khu vực** trên trang **Chỉnh sửa báo cáo chi phí**. Sau đó, danh sách các nhóm thuế bán hàng được lọc để chỉ hiển thị những nhóm áp dụng cho Vương quốc Anh. Linh chọn nhóm thuế bán hàng **Vương quốc Anh 001** rồi chọn nhóm thuế bán hàng **Bữa ăn**. Sau đó, Nancy thêm một giao dịch mới cho cơ sở lưu trú. Vì chỉ có một nhóm thuế bán hàng và một mục nhóm thuế bán hàng cho cơ sở lưu trú tại Vương quốc Anh, nên thông tin này sẽ tự động được điền vào báo cáo chi phí của Nancy.

Theo chính sách của Contoso, tất cả các chi phí phải có hóa đơn tương ứng. Do đó, khi Nancy lưu báo cáo chi phí, cô nhận được một thông báo cho biết cô phải đính kèm biên lai cho mỗi giao dịch đã liệt kê trên báo cáo chi phí của mình. Linh xác minh rằng cô đã đính kèm hình ảnh kỹ thuật số của mỗi biên lai giao dịch vào báo cáo chi phí của mình rồi gửi báo cáo để được phê duyệt. Sau đó, cô gửi biên lai giấy cho nhóm xử lý của văn phòng hỗ trợ. Nhóm này sẽ gửi dữ liệu hoàn thuế GTGT cho nhà cung cấp bên thứ ba để nộp các tờ khai hoàn thuế GTGT quốc tế cho Contoso.

## <a name="make-sure-that-all-tax-information-is-complete-and-then-post-the-expense-report"></a>Đảm bảo rằng tất cả thông tin thuế đã hoàn tất, sau đó đăng báo cáo chi phí

April, điều phối viên Tài khoản phải trả cho Contoso, phải nhập mọi thông tin thuế còn thiếu trong báo cáo chi phí trước khi báo cáo có thể được đăng. Cô mở **Chi tiết báo cáo chi phí** và xem báo cáo chi phí đã được phê duyệt của Linh. Sau đó, April mở báo cáo chi phí để xem chi tiết các giao dịch. Cô ấy thấy rằng Linh đã không nhập nhóm thuế bán hàng cho một trong các giao dịch. Vì thông tin này không được cung cấp, April không thể đăng báo cáo chi phí. Do đó, April xem trang **Cấu hình thuế** trong Quản lý chi phí rồi tìm nhóm thuế bán hàng thích hợp cho quốc gia/khu vực và loại giao dịch. Giờ đây, April có thể đăng báo cáo chi phí lên sổ cái.

Khi April đăng báo cáo chi phí, một hạng mục công việc có thể thu hồi VAT được tạo. Mục công việc này được gán cho một thành viên của nhóm xử lý của văn phòng hỗ trợ. April nhận được thông báo xác nhận rằng việc đăng đã thành công. Thông báo này cũng nêu số lượng giao dịch VAT đã được xác định để hoàn thuế.

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>Xử lý các chi phí đủ điều kiện để thu hồi thuế GTGT quốc tế

Arnie, một thành viên nhóm xử lý hỗ trợ của Contoso, chịu trách nhiệm xác nhận rằng tất cả các thông tin cần thiết cho việc hoàn thuế GTGT đều đã được đưa vào báo cáo chi phí. Anh mở trang **Hoàn thuế chi phí** rồi chọn báo cáo chi phí mà Linh đã gửi. Arnie xác minh rằng tất cả các biên lai bắt buộc đã được đính kèm và đã nhập đúng nhóm thuế bán hàng và mục mã số thuế bán hàng.

Khi Arnie nhận được biên lai giấy từ Nancy, anh xác minh chúng với biên lai kỹ thuật số và sau đó thay đổi trạng thái của báo cáo chi phí thành **Sẵn sàng phục hồi**.

## <a name="send-vat-recovery-data-to-the-third-party-vendor-to-file-international-recovery-returns"></a>Gửi dữ liệu hoàn thuế VAT cho nhà cung cấp bên thứ ba để nộp tờ khai hoàn thuế quốc tế

Khi Arnie đã sẵn sàng gửi dữ liệu báo cáo chi phí cho nhà cung cấp bên thứ ba sẽ nộp tờ khai thu hồi VAT, anh sẽ mở trang **Thu hồi chi phí thuế**. Anh lọc trang để trang chỉ hiển thị các báo cáo chi phí được đánh dấu là **Sẵn sàng hoàn thuế**. Sau đó, Arnie chọn **Tệp** &gt; **Xuất sang Excel**. Thông tin VAT từ các báo cáo chi phí được xuất sang bảng tính Microsoft Excel. Arnie gửi bảng tính này cho nhà cung cấp bên thứ ba và kèm theo một thông báo cho biết rằng biên lai giấy đã được gửi bằng chuyển phát nhanh.

## <a name="process-expenses-for-domestic-vat-recovery"></a>Xử lý chi phí hoàn thuế GTGT trong nước

Arnie phải xác minh rằng các giao dịch báo cáo chi phí đủ điều kiện để thu hồi VAT và các biên lai kỹ thuật số được đính kèm với báo cáo. Để bắt đầu xử lý các chi phí đủ điều kiện hoàn thuế nội địa, Arnie mở trang **Hoàn thuế chi phí** rồi chọn báo cáo chi phí cần xác minh. Anh xác minh rằng biên lai đứng tên công ty thay vì nhân viên. Đối với việc thu hồi thuế GTGT, hóa đơn phải đứng tên công ty. Sau đó, Arnie xác nhận rằng nhóm thuế bán hàng và mã số thuế bán mặt hàng chính xác đã được áp dụng.

Sau khi nhận được biên lai giấy, Arnie thay đổi trạng thái của báo cáo chi phí thành **Sẵn sàng hoàn thuế**. Sau đó, anh có thể nộp tờ khai cho cơ quan thuế thích hợp. Trong trường hợp này, cơ quan thuế thích hợp ở Hoa Kỳ là Sở Thuế vụ (IRS).


[!INCLUDE[footer-include](../includes/footer-banner.md)]