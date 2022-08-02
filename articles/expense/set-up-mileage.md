---
title: Thiết lập khoảng cách bằng cách sử dụng các bậc tỷ lệ khoảng cách
description: Bài viết này cung cấp thông tin về tỷ lệ số dặm và các cấp tỷ lệ số dặm.
author: suvaidya
ms.date: 05/20/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 9689bbaf4c4f88ad9f746c3f98676f97e634ab6c
ms.sourcegitcommit: 5e1f549a2e55a87351b2979e3aff402ed35487e1
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/29/2022
ms.locfileid: "9064304"
---
# <a name="set-up-mileage-using-mileage-rate-tiers"></a>Thiết lập khoảng cách bằng cách sử dụng các bậc tỷ lệ khoảng cách

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Khi một khoản chi phí được báo cáo và danh mục chi phí đã chọn là **Khoảng cách**, số tiền cho dòng chi phí đó được tính theo *tỷ lệ trên mỗi khoảng cách*. Số tiền này được xác định theo các bậc khoảng cách đã xác định hoặc, nếu không có mức tỷ lệ khoảng cách nào được thiết lập, theo tỷ lệ khoảng cách tiêu chuẩn. 

Các bậc tỷ lệ khoảng cách có thể được thiết lập bằng cách chuyển đến **Quản lý chi phí** > **Thiết lập** > **Chung** > **Danh mục chi phí** > **Khoảng cách** > **Thiết lập danh mục**.

Sau khi bạn nâng cấp lên phiên bản 10.0.18, nếu tổ chức của bạn sử dụng danh mục chi phí số dặm, hãy cân nhắc việc kích hoạt tính năng số dặm sau khi xem xét các thay đổi thiết kế bên dưới. 

Thiết kế mới của các bậc tỷ lệ khoảng cách có ảnh hưởng đến cách thức xử lý giá trị ở trường **Số lượng**. Trong các bản phát hành trước 10.0.18, giá trị ở trường **Số lượng** được coi là giới hạn dưới. Khi mức tích lũy vượt qua giá trị đó, tỷ lệ tương ứng sẽ được sử dụng.  Kể từ phiên bản 10.0.18, giá trị ở trường **Số lượng** được coi là giới hạn trên. Tỷ lệ tương ứng sẽ được sử dụng khi mức tích lũy khoảng cách nhỏ hơn giá trị ở trường **Số lượng** này.  Mô hình mới cho các bậc khoảng cách mang đến sự nhất quán giữa các bậc khoảng cách và khả năng sử dụng tốt hơn.   

Tất cả các báo cáo chi phí đã phê duyệt sẽ được tính toán lại trong quá trình đăng theo thiết kế mới.

## <a name="example"></a>Ví dụ:
 
### <a name="before-version-10018"></a>Trước phiên bản 10.0.18
Với hai bậc tỷ lệ khoảng cách, trường **Số lượng** ở mỗi bậc thể hiện giới hạn dưới về khoảng cách. Hiện tại, bậc một có giá trị là 0 và tỷ lệ là 0,45, còn bậc hai có giá trị là 1000 và tỷ lệ là 0,25. Nếu khoảng cách tích lũy (tính bằng dặm hoặc kilômét) vượt quá giá trị ở trường này, thì tỷ lệ tương ứng sẽ được sử dụng. Nếu không có dòng nào có số lượng bằng 0, thì hệ thống sẽ sử dụng tỷ lệ khoảng cách được xác định trong phần Quản lý chi phí. 
 
Nếu một nhân viên gửi báo cáo chi phí có giá trị khoảng cách là 1.500 dặm, thì hai dòng khoảng cách trên báo cáo chi phí được đăng sẽ là: 1000 (tỷ lệ 0,45) + 500 (tỷ lệ 0,25) = 575,00.

### <a name="after-version-10018"></a>Từ phiên bản 10.0.18 trở đi
Trong phiên bản 10.0.18, trường **Số lượng** ở mỗi bậc đại diện cho giới hạn trên của bậc đó. Hiện tại, bậc một có giá trị là 999 và tỷ lệ là 0,45, còn bậc hai có giá trị là 999.999.999,00 và tỷ lệ là 0,25. Nếu khoảng cách tích lũy (tính bằng dặm hoặc kilômét) vượt quá giá trị ở trường **Số lượng**, thì tỷ lệ tương ứng sẽ được sử dụng. Nếu giá trị khoảng cách vượt quá tất cả các giới hạn trên, thì hệ thống sẽ sử dụng tỷ lệ khoảng cách được xác định trong phần Quản lý chi phí. 
 
Để tính toán chính xác trong cùng một kịch bản, bạn phải thay đổi cách thiết lập bậc. Trường **Số lượng** có giá trị là 999,00 ở bậc một và 999.999.999,00 ở bậc hai. Nếu một nhân viên gửi giá trị vượt quá tổng số dặm hoặc kilômét ở bậc một, thì hệ thống sẽ sử dụng tỷ lệ khoảng cách được xác định trong phần Quản lý chi phí. 
  
Nếu một nhân viên gửi báo cáo chi phí có giá trị khoảng cách là 1.500 dặm, thì hai dòng khoảng cách trên báo cáo chi phí được đăng sẽ là: 1000 (tỷ lệ 0,45) + 500 (tỷ lệ 0,25) = 575

## <a name="enable-the-mileage-amount-calculation-for-multiple-mileage-tiers-with-same-rate-feature"></a>Kích hoạt tính năng Tính toán số tiền khoảng cách cho nhiều bậc khoảng cách với cùng một tỷ lệ

Tính năng **Tính toán số tiền khoảng cách cho nhiều bậc khoảng cách với cùng một tỷ lệ** giúp cải thiện việc tính toán tỷ lệ khoảng cách. Hãy hoàn thành các bước sau để kích hoạt tính năng này.

1. Chuyển đến **Không gian làm việc** > **Quản lý tính năng**. 
2. Trong danh sách, hãy tìm và chọn **Tính toán số tiền khoảng cách cho nhiều bậc khoảng cách với cùng một tỷ lệ**, rồi chọn **Kích hoạt ngay**.

Sau khi bạn kích hoạt tính năng này, hãy đặt lại các bậc khoảng cách để phản ánh chính xác giá trị của trường **Số lượng**. 

## <a name="enable-the-mileage-totals-calculation-by-fiscal-year-feature"></a>Bật tính năng tính tổng Dặm theo năm tài chính

Các **Tính tổng số dặm theo năm tài chính** tính năng này cho phép cài đặt mới trong các thông số Quản lý chi phí thực hiện các phép tính tổng số dặm theo năm tài chính thay vì năm dương lịch. Hãy hoàn thành các bước sau để kích hoạt tính năng này.

1. Chuyển đến **Không gian làm việc** > **Quản lý tính năng**.
1. Trong danh sách, tìm và chọn **Tính tổng số dặm theo năm tài chính**, và sau đó chọn **Kích hoạt ngay bây giờ**.
1. Đi đến **Quản lý chi tiêu** > **Thành lập** > **Chung** > **Các thông số quản lý chi phí**.
1. Trên **Các thông số quản lý chi phí** trang, định vị và kích hoạt **Sử dụng năm tài chính cho tổng số dặm**.

Sau khi bạn kích hoạt **Sử dụng năm tài chính cho tổng số dặm**, tổng số dặm được tính bằng năm tài chính.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
