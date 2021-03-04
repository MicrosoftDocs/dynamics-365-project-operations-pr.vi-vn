---
title: Tại sao giá được mặc định là 0 trên thực tế chi phí bán hàng?
description: Ba bước kiểm tra sau đây sẽ giúp bạn khắc phục sự cố tại sao giá mặc định là 0 trên thực tế chi phí bán hàng.
author: rumant
manager: kfend
ms.prod: ''
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
ms.openlocfilehash: d4910d3727085a45036f3b438ecd69abc3e99836
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146329"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-sales-actuals"></a>Tại sao giá được mặc định là 0 trên thực tế chi phí bán hàng?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Câu hỏi thường gặp này áp dụng cho các thực tế chi phí mà lớp giao dịch được đặt là Chi phí và loại giao dịch là Bán hàng Chưa lập hóa đơn. Ba bước kiểm tra sau đây sẽ giúp bạn khắc phục sự cố tại sao giá (tỷ lệ thanh toán) mặc định là 0 trên thực tế chi phí bán hàng.

## <a name="check-1-identify-the-sales-price-list-for-project"></a>Bước 1: Xác định bảng giá bán hàng dành cho dự án

Tìm dự án từ trường dự án của thực tế và đi đến trang dự án. Sau đó vào tab Bán hàng. Trên lưới Mô tả hợp đồng Dự án, hãy nhấp vào liên kết trong trường Hợp đồng Dự án. Trang Hợp đồng của dự án sẽ mở ra. Trên trang Hợp đồng Dự án, hãy vào tab Bảng giá Dự án. Kiểm tra xem có ít nhất một bảng giá giá đính kèm ở đây không.

Nếu không có bảng giá được đính kèm trong lưới Bảng giá Dự án của Hợp đồng Dự án thì:

- Đính kèm một bảng giá vào lưới Bảng giá Dự án. Bảng giá được phép đính kèm ở đây phải có trường ngữ cảnh được đặt thành Bán hàng và trường tiền tệ trong bảng giá phải khớp với trường tiền tệ trên Hợp đồng Dự án. Khi bạn đã thực hiện các bản sửa lỗi cần thiết, hãy tạo lại một mục nhập chi phí, phê duyệt mục đó và xác minh rằng thực tế bán hàng chưa lập hóa đơn hiển thị mức giá hợp lệ.
- Nếu bạn có một hoặc nhiều bảng giá được đính kèm trong lưới Bảng giá Dự án của trường Hợp đồng Dự án thì hãy đến Bước 2.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-expense-actual"></a>Bước 2: Có bất kỳ bảng giá nào được xác định ở trên hợp lệ cho ngày cụ thể của thực tế chi phí bán hàng không?

Để Project Service xem xét đặt mức giá mặc định cho một bảng giá, bảng giá đó phải được áp dụng cho ngày cụ thể trên thực tế chi phí bán hàng. Kiểm tra những điều sau đây để xem liệu (các) bảng giá được xác định ở trên có được áp dụng hay không:

- Bắt đầu bằng cách kiểm tra xem ngày bắt đầu và ngày kết thúc trên tab chung cho các bảng giá đính kèm có trống không. Nếu ngày bắt đầu và kết thúc trên danh sách giá được xác định ở trên trống, bạn đã cô lập được vấn đề. 
- Ghi chú về trường ngày bắt đầu trên thực tế chi phí bán hàng của bạn và kiểm tra xem có bất kỳ danh sách giá nào được xác định có thể áp dụng cho ngày đó hay không. Ví dụ: ngày trên thực tế chi phí bán hàng phải nằm giữa ngày bắt đầu và ngày kết thúc trên bảng giá. 
    - Nếu không có bảng giá nào bao gồm ngày đó trên thực tế chi phí bán hàng thì bạn đã cô lập được vấn đề. Thay đổi ngày bắt đầu và kết thúc của bảng giá để đảm bảo rằng bảng giá bao gồm ngày trên thực tế chi phí bán hàng. 
    - Nếu có nhiều hơn một bảng giá bao gồm ngày đó trên thực tế chi phí bán hàng thì bạn đã cô lập được vấn đề. Chỉnh sửa ngày bắt đầu và kết thúc của (các) bảng giá để chỉ có một bảng giá bao gồm ngày trên thực tế chi phí. 
    - Nếu có chỉ có một bảng giá bao gồm ngày trên thực tế chi phí bán hàng, hãy đến với Bước 3.
Khi bạn đã hoàn thành các bản sửa lỗi cần thiết, hãy tạo lại một mục nhập chi phí, phê duyệt mục đó và xác minh rằng thực tế bán hàng chưa lập hóa đơn hiển thị mức giá hợp lệ.

## <a name="check-3-is-there-a-valid-price-for-the-expense-category-in-the-applicable-project-price-list"></a>Bước 3: Có giá hợp lệ cho thể loại chi phí trong bảng giá dự án áp dụng không? 

Nếu bạn đã hoàn thành Bước 1 và Bước 2, bây giờ bạn chỉ có một bảng giá dự án được áp dụng cho ngày cụ thể trên thực tế chi phí bán hàng. Mở Bảng giá Dự án này và di chuyển đến tab Giá cả Thể loại. Đảm bảo rằng có một hàng trên lưới dành cho thể loại chi phí cụ thể trên thực tế Chi phí bán hàng.
 
- Nếu không có hàng thì bạn đã cô lập được vấn đề. Tạo một hàng trong lưới Giá cả thể loại cho thể loại trên thực tế chi phí của bạn. Sau đó, hãy tạo lại một mục nhập chi phí, phê duyệt mục đó và xác minh rằng thực tế bán hàng chưa lập hóa đơn hiển thị mức giá hợp lệ. 
- Nếu có một hàng cho thể loại chi phí trong lưới giá cả thể loại, kiểm tra nếu nó có một mức giá hợp lệ.

Để hiểu giá hợp lệ là gì, hãy sử dụng các phương pháp sau:

- Nếu trường Phương pháp Định giá trên dòng Giá cả thể loại được đặt là Theo Chi phí, thì tỷ lệ đơn vị trên thực tế Chi phí bán hàng sẽ được mặc định thành giá trị trong mục nhập Chi phí.
- Nếu trường Phương pháp Định giá trên dòng Giá cả thể loại được đặt là Phần trăm Tăng thì hãy kiểm tra xem trường Phần trăm có được đặt thành giá trị hợp lệ hay không. Tỷ lệ đơn vị trên thực tế Chi phí bán hàng sẽ được mặc định bằng cách áp dụng phần trăm tăng này cho giá trong mục nhập Chi phí.
- Nếu trường Phương pháp Định giá trên dòng Giá cả thể loại được đặt là Đơn giá thì hãy kiểm tra xem trường Giá có được đặt thành giá trị hợp lệ hay không. Tỷ lệ đơn vị trên thực tế Chi phí bán hàng sẽ được mặc định theo lượng tiền tệ được chỉ định trong trường Giá.

Nếu việc thiết lập giá cho thể loại chi phí không hợp lệ thì bạn đã cô lập được vấn đề. Giải pháp là chỉnh sửa dòng giá cả thể loại với một mức giá hợp lệ cho thể loại chi phí phù hợp với các quy tắc trên. Khi bạn đã thực hiện xong, hãy tạo lại một mục nhập chi phí, phê duyệt mục đó và kiểm tra xem thực tế bán hàng chưa lập hóa đơn đã có mức giá hợp lệ hay chưa.

Nếu bạn vẫn không thấy một mức giá hợp lệ trên thực tế chi phí bán hàng của mình sau khi làm theo ba bước kiểm tra ở trên, hãy ghi phiếu hỗ trợ.




[!INCLUDE[footer-include](../includes/footer-banner.md)]