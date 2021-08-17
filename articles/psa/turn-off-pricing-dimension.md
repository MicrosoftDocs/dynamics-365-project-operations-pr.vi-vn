---
title: Tắt thông số định giá
description: Chủ đề này cho biết cách thiết lập thông số định giá trong giải pháp Project Service.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 9f690dfdb40e962ef329f323716f3f755493805d764dbfaa2d4f9d042231cee7
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006812"
---
# <a name="turn-off-a-pricing-dimension"></a>Tắt thông số định giá

[!include [banner](../includes/psa-now-project-operations.md)]

Bạn có thể cần phải đánh giá và cập nhật chiến lược định giá mỗi vài năm. Mọi bản cập nhật bạn thực hiện có thể yêu cầu bạn tắt thông số định giá hiện có và tạo một thông số mới. Ví dụ: bạn có thể đã có giá theo **Vai trò** trước đây, nhưng bây giờ bạn đã quyết định giá theo **Kinh nghiệm làm việc**. Điều này có thể đòi hỏi bạn tắt **Vai trò** làm thông số định giá và tạo **Trải nghiệm làm việc** dưới dạng thông số định giá mới. 

Tắt thông số định giá, bất kể là sẵn dùng hay tùy chỉnh. Có thể thực hiện bằng cách đặt các trường **Áp dụng cho chi phí** và **Áp dụng cho doanh số** của Thông số định giá thành **Không**.

Tuy nhiên, khi thực hiện điều này, bạn có thể nhận được thông báo lỗi sau.

![Có khả năng xảy ra lỗi quy trình công việc khi tắt một thông số định giá.](media/Business-Process-Error.png)


Thông báo lỗi này chỉ ra rằng có các hồ sơ giá trước đây đã được thiết lập cho thông số đang bị tắt. Tất cả các hồ sơ **Giá theo vai trò** và **Tăng giá theo vai trò** nói đến một thông số phải được xóa trước khi có thể đặt khả năng của thông số thành **Không**. Quy tắc này áp dụng cho cả thông số định giá sẵn dùng và mọi thông số định giá tùy chỉnh mà bạn có thể đã tạo. Lý do xác thực là do Project Service có một hạn chế rằng mỗi hồ sơ **Giá theo vai trò** phải có một tổ hợp thông số duy nhất. Ví dụ: trên bảng giá tên là **Tỷ lệ chi phí 2018 của Hoa Kỳ**, bạn có các hàng **Giá theo vai trò** sau. 

| Tiêu đề chuẩn         | Đơn vị tổ chức    |Đơn vị   |Giá  |Tiền tệ  |
| -----------------------|-------------|-------|-------|----------|
| Kỹ sư hệ thống|Contoso Hoa Kỳ|Giờ| 100|Giải pháp USD|
| Kỹ sư hệ thống cao cấp|Contoso Hoa Kỳ|Giờ| 150| Giải pháp USD|


Khi bạn tắt **Tiêu đề chuẩn** làm thông số định giá và công cụ định giá Project Service tìm kiếm giá, thì công cụ đó sẽ chỉ sử dụng giá trị **Đơn vị tổ chức** từ ngữ cảnh nhập. Nếu **Đơn vị tổ chức** của ngữ cảnh nhập là "Contoso Hoa Kỳ", thì kết quả sẽ không xác định được bởi vì cả hai hàng đều sẽ phù hợp. Để tránh trường hợp này, khi bạn tạo **Giá theo vai trò**, Project Service xác thực rằng tổ hợp thông số là duy nhất. Nếu thông số bị tắt sau khi hồ sơ **Giá theo vai trò** được tạo, hạn chế này có thể bị vi phạm. Do đó, trước khi tắt một thông số, bạn cần xóa tất cả các hàng **Giá theo vai trò** và **Tăng giá theo vai trò** đã điền sẵn giá trị thông số đó.



[!INCLUDE[footer-include](../includes/footer-banner.md)]