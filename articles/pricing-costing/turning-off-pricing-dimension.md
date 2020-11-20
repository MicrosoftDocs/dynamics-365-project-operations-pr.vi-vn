---
title: Tắt thông số định giá
description: Chủ đề này cung cấp thông tin về cách tắt thông số định giá.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: ffeff2ab465f37b8a4e40f4e64b118e3bb412cb8
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119309"
---
# <a name="turning-off-a-pricing-dimension"></a>Tắt thông số định giá

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Bạn có thể cần phải đánh giá và cập nhật chiến lược định giá mỗi vài năm. Mọi bản cập nhật bạn thực hiện có thể yêu cầu bạn tắt thông số định giá hiện có và tạo một thông số mới. Ví dụ: bạn có thể đã có giá theo **Vai trò** trước đây, nhưng bây giờ bạn đã quyết định giá theo **Kinh nghiệm làm việc**. Điều này có thể đòi hỏi bạn tắt **Vai trò** làm thông số định giá và tạo **Trải nghiệm làm việc** dưới dạng thông số định giá mới. 

Tắt thông số định giá, bất kể là sẵn dùng hay tùy chỉnh. Có thể thực hiện bằng cách đặt các trường **Áp dụng cho chi phí** và **Áp dụng cho doanh số** của Thông số định giá thành **Không**.

Tuy nhiên, khi thực hiện điều này, bạn có thể nhận được thông báo lỗi, **Không thể cập nhật hoặc xóa thông số định giá nếu có bản ghi giá được liên kết.**

Thông báo lỗi này chỉ ra rằng có các hồ sơ giá trước đây đã được thiết lập cho thông số đang bị tắt. Tất cả các hồ sơ **Giá theo vai trò** và **Tăng giá theo vai trò** nói đến một thông số phải được xóa trước khi có thể đặt khả năng của thông số thành **Không**. Quy tắc này áp dụng cho cả thông số định giá sẵn dùng và mọi thông số định giá tùy chỉnh mà bạn có thể đã tạo. Lý do xác thực là vì mỗi bản ghi **Giá theo vai trò** phải có một tổ hợp thông số duy nhất. Ví dụ: trên bảng giá tên là **Tỷ lệ chi phí 2018 của Hoa Kỳ**, bạn có các hàng **Giá theo vai trò** sau. 

| Tiêu đề chuẩn         | Đơn vị tổ chức    |Đơn vị   |Giá  |Tiền tệ  |
| -----------------------|-------------|-------|-------|----------|
| Kỹ sư hệ thống|Contoso US|Hour| 100|USD|
| Kỹ sư hệ thống cao cấp|Contoso US|Hour| 150| USD|


Khi bạn tắt **Tiêu đề chuẩn** làm thông số định giá và công cụ định giá, thì công cụ định giá sẽ chỉ sử dụng giá trị **Đơn vị tổ chức** từ ngữ cảnh nhập. Nếu **Đơn vị tổ chức** của ngữ cảnh nhập là “Contoso Hoa Kỳ”, thì kết quả sẽ không xác định bởi vì cả hai hàng sẽ phù hợp. Để tránh trường hợp này, khi bạn tạo bản ghi **Giá theo vai trò**, hệ thống sẽ xác thực rằng tổ hợp thông số là duy nhất. Nếu thông số bị tắt sau khi hồ sơ **Giá theo vai trò** được tạo, hạn chế này có thể bị vi phạm. Do đó, trước khi tắt một thông số, bạn cần xóa tất cả các hàng **Giá theo vai trò** và **Tăng giá theo vai trò** đã điền sẵn giá trị thông số đó.
