---
title: Hóa đơn hiệu chỉnh
description: Chủ đề này cung cấp thông tin về hóa đơn hiệu chỉnh.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: e14da1c07d5b697de6caf1b9041c30581ecff102
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898107"
---
# <a name="corrected-invoices"></a>Hóa đơn hiệu chỉnh

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Có thể chỉnh sửa các hóa đơn đã xác nhận. Khi bạn sửa các hóa đơn đã xác nhận, một hóa đơn hiệu chỉnh ở dạng bản nháp được tạo ra. Vì giả định là bạn muốn đảo ngược tất cả giao dịch và số lượng từ hóa đơn ban đầu, hóa đơn hiệu chỉnh bao gồm tất cả giao dịch từ hóa đơn ban đầu và tất cả số lượng trên đó là (0).

Khi các giao dịch không yêu cầu chỉnh sửa, bạn có thể xóa chúng khỏi hóa đơn hiệu chỉnh ở dạng bản nháp. Để đảo ngược hoặc chỉ trả lại một phần số lượng, bạn có chỉnh sửa trường Số lượng trên chi tiết dòng. Nếu mở chi tiết mô tả hóa đơn, bạn có thể thấy số lượng hóa đơn ban đầu. Sau đó, bạn có thể chỉnh sửa số lượng hóa đơn hiện tại sao cho ít hơn hoặc nhiều hơn số lượng hóa đơn ban đầu.

Khi bạn xác nhận hóa đơn chỉnh sửa, doanh số bán hàng thực tế được lập hóa đơn ban đầu được đảo ngược và doanh số bán hàng thực tế mới được lập hóa đơn được tạo. Nếu số lượng giảm, sự khác biệt dẫn đến doanh số bán hàng thực tế mới chưa được lập hóa đơn cũng được tạo. Ví dụ: nếu doanh số bán hàng ban đầu được lập hóa đơn là trong 8 giờ, thì chi tiết mô tả hóa đơn hiệu chỉnh có số lượng giảm là 6 giờ, dòng bán hàng ban đầu được lập hóa đơn bị đảo và tạo 2 doanh số bán hàng thực tế mới:

- Doanh số bán hàng thực tế được lập hóa đơn cho 6 giờ.
- Doanh số bán hàng thực tế được lập hóa đơn cho 2 giờ còn lại. Giao dịch này có thể được lập hóa đơn sau hoặc đánh dấu là không tính phí, tùy thuộc vào các cuộc đàm phán với khách hàng.
