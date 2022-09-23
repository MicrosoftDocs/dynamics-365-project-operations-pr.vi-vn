---
title: Đăng báo cáo chi phí
description: Bài viết này giải thích cách đăng báo cáo chi phí.
author: ramagadu
ms.date: 08/12/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: d0ae4559a08553236158a663513401cb38cbe28f
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524896"
---
# <a name="post-expense-reports"></a>Đăng báo cáo chi phí

Sau khi báo cáo chi phí đã được duyệt và chuyển vào sổ nhật ký chung, nó có thể được đăng. Khi bạn đăng báo cáo chi phí, các khoản chi phí đủ điều kiện để thu hồi thuế giá trị gia tăng (VAT) sẽ được xác định. Nhiệm vụ xác minh và thu hồi các khoản thanh toán thuế GTGT được giao cho nhân viên chịu trách nhiệm xác minh báo cáo chi phí.

Nếu các chi phí trên báo cáo chi phí được tính cho một công ty không phải là công ty thuê nhân viên, bạn phải xác minh cả công ty rằng những chi phí đó là của họ và công ty mà họ phải trả. Ví dụ: nhân viên đã nộp báo cáo chi phí làm việc cho công ty DAT nhưng lại tính một khoản chi phí cho công ty DIR. Trong trường hợp này, DAT là công ty phải trả khoản chi phí và DIR là công ty chịu khoản chi phí đó. Sau khi bạn xác minh các dòng nhật ký này, bạn có thể đăng các dòng chi phí lên sổ cái.

Để đăng báo cáo chi phí, trên trang **Báo cáo chi phí được phê duyệt**, chọn báo cáo chi phí, sau đó, trên Ngăn hành động, hãy chọn **Đăng**.

Bạn cũng có thể đăng tất cả các báo cáo chi phí trong danh sách cùng một lúc. Chọn tất cả các báo cáo chi phí, sau đó chọn **Đăng**.

## <a name="enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature"></a>Bật tính năng Khả năng ghi trách nhiệm pháp lý chi phí bằng đơn vị tiền tệ của nhà cung cấp cho tính năng phương thức thanh toán bằng tiền mặt

Các **Khả năng tính trách nhiệm pháp lý chi phí bằng đơn vị tiền tệ của nhà cung cấp đối với phương thức thanh toán bằng tiền mặt** tính năng này cho phép đăng báo cáo chi phí bằng đơn vị tiền tệ của nhà cung cấp cho phương thức thanh toán bằng tiền mặt.

Hiện tại, khi bạn gửi chi phí tiền mặt, báo cáo chi phí sẽ được đăng theo đơn vị tiền tệ kế toán. Do sự chuyển đổi số tiền giữa đơn vị tiền tệ giao dịch, đơn vị tiền tệ kế toán và đơn vị tiền tệ của nhà cung cấp, một số tiền không chính xác sẽ được thanh toán cho nhà cung cấp nếu ngày giao dịch chi phí và ngày thanh toán thực tế có tỷ giá hối đoái khác nhau.

Tính năng này sẽ đảm bảo rằng số dư của nhà cung cấp được ghi lại bằng đơn vị tiền tệ của nhà cung cấp khi báo cáo chi phí được đăng.

1. Chuyển đến **Không gian làm việc** \> **Quản lý tính năng**.
2. Trong danh sách, hãy tìm và chọn **Khả năng tính trách nhiệm pháp lý chi phí bằng đơn vị tiền tệ của nhà cung cấp đối với phương thức thanh toán bằng tiền mặt**, và sau đó chọn **Kích hoạt ngay bây giờ**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
