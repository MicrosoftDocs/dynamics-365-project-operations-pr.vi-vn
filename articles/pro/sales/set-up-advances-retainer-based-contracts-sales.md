---
title: Hợp đồng dựa trên tiền tạm ứng và giữ lại
description: Chủ đề này cung cấp thông tin về các mô hình hợp đồng dựa trên tiền giữ lại và khoản tạm ứng trong Project Operations.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5ccf8ff4fa52fa6ff9fe534dfbe6736afc24ffba
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/21/2020
ms.locfileid: "4088159"
---
# <a name="advances-and-retainer-based-contracts"></a>Hợp đồng dựa trên tiền tạm ứng và giữ lại 


_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Dynamics 365 Project Operations hỗ trợ các hợp đồng dựa trên tiền giữ lại. Hợp đồng dựa trên tiền giữ lại là một tập hợp các khoản thanh toán được thương lượng phân bổ đều mà khách hàng sẽ được lập hóa đơn trong suốt thời gian của một dự án. Loại hợp đồng này thường được sử dụng cho các mô hình thanh toán dựa trên thời gian và vật tư hoặc dựa trên mức tiêu thụ khi cần cung cấp cho khách hàng một hóa đơn và lịch thanh toán có thể dự đoán. Doanh thu thực tế phát sinh mỗi kỳ được đối chiếu với khoản thanh toán nhận được từ khách hàng vào đầu kỳ. Theo khái niệm của mô hình thanh toán Thời gian và vật tư, giá trị doanh thu được tích lũy trong mỗi kỳ có thể thay đổi theo chi phí phát sinh. Nếu doanh thu tích lũy được nhiều hơn số tiền nhận được vào đầu kỳ, công ty giao dự án có thể:

- Chỉ xuất hóa đơn cho khách hàng đối với phần vượt quá 
- Trì hoãn việc đối chiếu doanh thu sang kỳ lập hóa đơn tiếp theo và thanh toán vào cuối dự án cho bất kỳ doanh thu nào còn lại chưa được lập hóa đơn

Khác biệt chính giữa mô hình hợp đồng dựa trên tiền giữ lại và mô hình hợp đồng giá cố định trong Project Operations là trong mô hình hợp đồng giá cố định, số tiền trên hóa đơn không được liên kết hoặc ràng buộc với chi phí phát sinh. Việc lập hóa đơn tuân theo phương pháp dựa trên mốc thời gian phù hợp với chi phí phát sinh cho thời kỳ đó. Trong hợp đồng dựa trên tiền giữ lại, doanh thu có thể lập hóa đơn được ghi lại dựa trên phương pháp thanh toán trên mô tả hợp đồng. Khi phương thức thanh toán là thời gian và vật tư, doanh thu có thể lập hóa đơn được liên kết với chi phí phát sinh trong bất kỳ thời kỳ nhất định nào và có thể thay đổi theo từng thời kỳ. Tuy nhiên, khách hàng chỉ được lập hóa đơn cho số tiền giữ lại định kỳ. Hệ thống sử dụng một hóa đơn khác vào cuối kỳ để đối chiếu doanh thu có thể lập hóa đơn được ghi nhận trong kỳ với số tiền mà khách hàng đã được lập hóa đơn vào đầu kỳ.

Ưu điểm của phương pháp này là chi phí của khách hàng có thể dự đoán được trong lịch trình giữ lại không giống như trong mô hình thời gian và vật tư thông thường. Tổ chức thực hiện dự án cũng có khả năng bù đắp rủi ro thu hồi các chi phí phát sinh do bất kỳ sự gia tăng nào về phạm vi mà mô hình giá cố định không cho phép họ thực hiện.

Ngoài lịch trình dựa trên tiền giữ lại định kỳ, Project Operations có thể ghi lại khoản tạm ứng một lần từ khách hàng và điều chỉnh số tiền đó với các thành phần chi phí khác nhau của dự án.

Tiền giữ lại trong Project Operations không có sẵn để sử dụng cho đến khi được lập hóa đơn cho khách hàng. Điều này được chỉ ra bởi các trường sau trên lưới con cho các khoản tạm ứng và tiền giữ lại.

| Trường | Mức độ liên quan, mục đích và hướng dẫn | Tác động xuôi tuyến |
| --- | --- | --- |
| Số tiền khả dụng | Số tiền có sẵn được sử dụng trên hồ sơ khoản tạm ứng và tiền giữ lại. | Cho đến khi được lập hóa đơn, khoản tạm ứng hoặc tiền giữ lại sẽ không được sử dụng có nghĩa là số tiền khả dụng sẽ bằng không. |
| Số tiền đã dùng | Số tiền đã được sử dụng trên hồ sơ khoản tạm ứng và tiền giữ lại. | Khoản tạm ứng hoặc tiền giữ lại có thể được đối chiếu một phần trên hóa đơn với chi phí thực tế sẽ có một số phần được đánh dấu là đã sử dụng hoặc đã dùng. Phần còn lại của số tiền tạm ứng hoặc tiền giữ lại có sẵn để đối chiếu trên hóa đơn trong tương lai với chi phí thực tế. |
