---
title: Tại sao giá được mặc định là 0 trên thực tế thời gian chi phí?
description: Khắc phục sự cố tại sao giá mặc định về 0 trên thực tế chi phí bán hàng.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
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
ms.openlocfilehash: e1f81268c894e2ff5d607d8008876c84f7eafdf05f8b1f3212263a5dfa89b69d
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997002"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a>Tại sao giá được mặc định là 0 trên thực tế thời gian chi phí?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Câu hỏi thường gặp này áp dụng cho các thực tế mà lớp giao dịch được đặt thành Thời gian và loại giao dịch là Chi phí. Ba bước kiểm tra sau đây sẽ giúp bạn khắc phục sự cố tại sao giá (tỷ lệ thanh toán) mặc định là 0 vào trên thực tế thời gian chi phí.
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a>Bước 1: Xác định bảng giá chi phí dành cho dự án

Tìm dự án từ trường dự án của thực tế và đi đến trang dự án. Nhấp vào liên kết đơn vị hợp đồng trong trường này. Trên trang Đơn vị hợp đồng, kiểm tra xem đơn vị hợp đồng có bảng giá trong lưới Bảng Giá Vốn hay không.

Nếu có nhiều hơn một bảng giá, bạn đã cô lập được vấn đề. Project Service chỉ hỗ trợ một bảng giá cho mỗi đơn vị tổ chức. Loại bỏ tất cả bảng giá từ thực thể này cho đến khi chỉ có một bảng giá được đính kèm trong lưới Bảng Giá Vốn của Đơn vị Tổ chức.

Nếu không có bảng giá đính kèm với Đơn vị Tổ chức, hãy ghi lại đơn vị tiền tệ của Đơn vị Tổ chức. Hãy vào Project Service, sau đó vào Tham số và mở tab Bảng giá. Kiểm tra xem có bất kỳ bảng giá nào có ngữ cảnh được đặt thành Chi phí và đơn vị tiền tệ khớp với đơn vị tiền tệ của Đơn vị Tổ chức hay không.
 
Nếu không có bảng giá nào phù hợp với tiêu chí đó, bạn đã cô lập được vấn đề. Đảm bảo có ít nhất một bảng giá có ngữ cảnh được đặt thành Chi phí và đơn vị tiền tệ khớp với đơn vị tiền tệ của Đơn vị Tổ chức.

Nếu có nhiều hơn một bảng giá phù hợp với tiêu chí đó, tiếp tục đọc tài liệu này để thực hiện kiểm tra thêm.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a>Bước 2: Có bất kỳ bảng giá nào được xác định ở trên hợp lệ cho ngày cụ thể của thực tế thời gian chi phí không?

Để Project Service xem xét đặt mức giá mặc định cho một bảng giá, bảng giá đó phải được áp dụng cho ngày cụ thể trên thực tế thời gian chi phí. Kiểm tra những điều sau đây để xem liệu (các) bảng giá được xác định ở trên có được áp dụng hay không:

- Kiểm tra xem ngày bắt đầu và ngày kết thúc trên tab chung cho các bảng giá đính kèm có trống không. Nếu ngày bắt đầu và kết thúc trên bảng giá được xác định ở trên trống, bạn đã cô lập được vấn đề. 
- Ghi chú về trường ngày bắt đầu trên thực tế thời gian chi phí của bạn và kiểm tra xem có bất kỳ danh sách giá nào được xác định có thể áp dụng cho ngày đó hay không. Ví dụ: ngày trên thực tế thời gian chi phí phải nằm giữa ngày bắt đầu và ngày kết thúc trên bảng giá. 
    - Nếu không có bảng giá nào bao gồm ngày đó trên thực tế thời gian chi phí thì bạn đã cô lập được vấn đề. Thay đổi ngày bắt đầu và kết thúc của bảng giá để đảm bảo rằng bảng giá bao gồm ngày trên thực tế thời gian chi phí. 
    - Nếu có nhiều hơn một bảng giá bao gồm ngày đó trên thực tế thời gian cho phí thì bạn đã cô lập được vấn đề. Bạn có thể sửa lỗi này bằng cách chỉnh sửa ngày bắt đầu và kết thúc của (các) bảng giá để chỉ có một bảng giá bao gồm ngày trên thực tế thời gian chi phí. 
    - Nếu có chỉ có một bảng giá bao gồm ngày đó chi phí thời gian thực tế, di chuyển đến phòng tiếp theo trong tài liệu.
Khi bạn đã thực hiện xong các bản sửa lỗi cần thiết, hãy tạo lại một mục nhập thời gian, phê duyệt mục đó và xác minh rằng thực tế thời gian chi phí hiển thị mức giá hợp lệ.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a>Bước 3: Có mức giá nào trong bảng giá dành cho kích thước định giá trên thực tế thời gian chi phí không?

Nếu bạn đã hoàn thành Bước 1 và Bước 2, bây giờ bạn chỉ có một bảng giá được áp dụng cho ngày cụ thể trên thực tế thời gian chi phí. Mở Bảng giá này và di chuyển đến tab Giá Vai trò. Đảm bảo rằng có một hàng trên lưới dành cho kích thước giá trên thực tế thời gian chi phí.

Nếu không có hàng nào trong lưới giá vai trò cho kích thước định giá trên thực tế thời gian chi phí thì bạn đã cô lập được vấn đề. Tạo một hàng trong lưới Giá vai trò cho kích thước định giá trên thực tế thời gian chi phí. Khi bạn đã thực hiện xong, hãy tạo lại một mục nhập thời gian, phê duyệt mục đó và xác minh rằng thực tế thời gian chi phí hiển thị mức giá hợp lệ.
 
Nếu bạn vẫn không thấy một mức giá hợp lệ trên thực tế thời gian chi phí của mình sau khi hoàn thành ba bước kiểm tra ở trên, vui lòng ghi một phiếu hỗ trợ.





[!INCLUDE[footer-include](../includes/footer-banner.md)]