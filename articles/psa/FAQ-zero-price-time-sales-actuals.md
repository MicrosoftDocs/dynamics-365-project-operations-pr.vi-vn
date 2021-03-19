---
title: Tại sao giá được mặc định là 0 trên thực tế thời gian bán hàng?
description: Khắc phục sự cố tại sao giá mặc định về 0 trên thực tế thời gian bán hàng.
author: rumant
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: cfb359b4ebd7c1a7a70ffdc2c47cf6291c797566
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285779"
---
# <a name="why-is-price-defaulting-to-zero-on-time-sales-actuals"></a>Tại sao giá được mặc định là 0 trên thực tế thời gian bán hàng?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Câu hỏi thường gặp này áp dụng cho các thực tế mà lớp giao dịch được đặt thành Thời gian và loại giao dịch là Bán hàng Chưa lập hóa đơn. Ba bước kiểm tra sau đây sẽ giúp bạn khắc phục sự cố tại sao giá (tỷ lệ thanh toán) mặc định là 0 vào trên thực tế thời gian bán hàng.

## <a name="check-1-identify-the-sales-price-list-for-the-project"></a>Bước 1: Xác định bảng giá bán hàng dành cho dự án

Tìm dự án từ trường dự án của thực tế và đi đến trang dự án. Sau đó vào tab Bán hàng và trên lưới Mô tả hợp đồng Dự án, hãy nhấp vào liên kết trong trường Hợp đồng Dự án. Trang Hợp đồng của dự án sẽ mở ra. Trên trang Hợp đồng Dự án, hãy vào tab Bảng giá Dự án. Kiểm tra xem có ít nhất một bảng giá giá đính kèm ở đây không. Nếu không có bảng giá được đính kèm trong lưới Bảng giá Dự án của trường Hợp đồng Dự án thì bạn đã cô lập vấn đề. Đính kèm một bảng giá vào lưới Bảng giá Dự án. Bảng giá được phép đính kèm ở đây phải có trường ngữ cảnh được đặt thành Bán hàng và trường tiền tệ trong bảng giá phải khớp với trường tiền tệ trên Hợp đồng Dự án. Khi bạn đã thực hiện xong các bản sửa lỗi cần thiết, hãy tạo lại một mục nhập thời gian, phê duyệt mục đó và xác minh rằng thực tế bán hàng chưa lập hóa đơn hiển thị mức giá hợp lệ. 

Nếu bạn có một hoặc nhiều bảng giá được đính kèm trong lưới Bảng giá Dự án của trường Hợp đồng Dự án thì hãy tiếp tục đến bước kiểm tra tiếp theo trong tài liệu.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-sales-actual"></a>Bước 2: Có bất kỳ bảng giá nào được xác định ở trên hợp lệ cho ngày cụ thể của thực tế thời gian bán hàng không?

Để Project Service xem xét đặt mức giá mặc định cho một bảng giá, bảng giá đó phải được áp dụng cho ngày cụ thể trên thực tế thời gian bán hàng. Kiểm tra những điều sau đây để xem liệu (các) bảng giá được xác định ở trên có được áp dụng hay không:
- Kiểm tra xem ngày bắt đầu và ngày kết thúc trên tab chung cho các bảng giá đính kèm có trống không. Nếu ngày bắt đầu và kết thúc trên bảng giá được xác định ở trên trống, bạn đã cô lập được vấn đề. 
- Ghi chú về trường ngày bắt đầu trên thực tế thời gian bán hàng của bạn và kiểm tra xem có bất kỳ danh sách giá nào được xác định có thể áp dụng cho ngày đó hay không. Ví dụ: ngày trên thực tế thời gian bán hàng phải nằm giữa ngày bắt đầu và ngày kết thúc trên bảng giá. 
    - Nếu không có bảng giá nào bao gồm ngày đó trên thực tế thời gian bán hàng thì bạn đã cô lập được vấn đề. Thay đổi ngày bắt đầu và kết thúc của bảng giá để đảm bảo rằng bảng giá bao gồm ngày trên thực tế thời gian bán hàng. 
    - Nếu có nhiều hơn một bảng giá bao gồm ngày đó trên thực tế thời gian bán hàng thì bạn đã cô lập được vấn đề. Bạn có thể sửa lỗi này bằng cách chỉnh sửa ngày bắt đầu và kết thúc của (các) bảng giá để chỉ có một bảng giá bao gồm ngày trên thực tế thời gian bán hàng. 
    - Nếu có chỉ có một bảng giá bao gồm ngày trên thực tế thời gian bán hàng, hãy đến với Bước 3.
Khi bạn đã thực hiện xong các bản sửa lỗi cần thiết, hãy tạo lại một mục nhập thời gian, phê duyệt mục đó và xác minh rằng thực tế thời gian bán hàng hiển thị mức giá hợp lệ.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-sales-actual"></a>Bước 3: Có mức giá nào trong bảng giá dành cho kích thước định giá trên thực tế thời gian bán hàng không?

Nếu bạn đã hoàn thành Bước 1 và Bước 2, bây giờ bạn chỉ có một bảng giá được áp dụng cho ngày cụ thể trên thực tế thời gian bán hàng. Mở Bảng giá này và di chuyển đến tab Giá Vai trò. Đảm bảo rằng có một hàng trên lưới dành cho kích thước giá trên thực tế Thời gian bán hàng.

Nếu không có hàng nào trong lưới giá vai trò cho kích thước định giá trên thực tế thời gian bán hàng thì bạn đã cô lập được vấn đề. Tạo một hàng trong lưới Giá vai trò cho kích thước định giá trên thực tế thời gian bán hàng. Khi bạn đã thực hiện xong, hãy tạo lại một mục nhập thời gian, phê duyệt mục đó và xác minh rằng thực tế thời gian bán hàng hiển thị mức giá hợp lệ.

Nếu bạn vẫn không thấy một mức giá hợp lệ trên thực tế thời gian bán hàng của mình sau khi làm theo ba bước kiểm tra ở trên, vui lòng ghi một phiếu hỗ trợ. 



[!INCLUDE[footer-include](../includes/footer-banner.md)]