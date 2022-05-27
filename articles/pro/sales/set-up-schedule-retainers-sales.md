---
title: Thiết lập lịch trình khoản duy trì
description: Chủ đề này cung cấp thông tin về cách thiết lập một lịch trình tiền tạm ứng trong Project Operations.
author: rumant
ms.date: 10/22/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b1c48f04aa47d50c9f3ab46031ef0d6cd68619d5
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574778"
---
# <a name="set-up-a-retainer-schedule"></a>Thiết lập lịch trình khoản duy trì

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Lịch trình khoản duy trì được thiết lập trên trang **Hợp đồng dự án** trong Dynamics 365 Project Operations.

1. Trên trang **Hợp đồng dự án**, trên tab **Tiền trả trước và Tiền tạm ứng**, hãy chọn **Thiết lập lịch trình tiền tạm ứng**.
2. Trên trang hộp thoại mở ra, các trường được liệt kê trong bảng sau sẽ hiển thị. Bảng này cho biết cách các giá trị đã nhập tác động hoặc ảnh hưởng như thế nào đến lịch trình tiền tạm ứng sẽ được tạo.

| Trường | Nội dung mô tả | Tác động xuôi tuyến |
| --- | --- | --- |
| Khách hàng trên hợp đồng dự án | Khách hàng trên hợp đồng sẽ được lập hóa đơn cho khoản tạm ứng hoặc trả trước này. | Nếu bạn có nhiều khách hàng trong hợp đồng và muốn lập hóa đơn một khoản tạm ứng/trả trước cụ thể cho từng khách hàng, hãy tạo một hóa đơn cho từng khách hàng theo cách thủ công. |
| Bắt đầu lịch trình tiền tạm ứng | Nhập ngày bắt đầu của lịch trình tiền tạm ứng. | Ngày này có thể không phải là ngày tạo khoản tạm ứng hoặc trả trước đầu tiên. Ngày mà khoản tạm ứng hoặc trả trước đầu tiên được tạo, cũng bị ảnh hưởng bởi tần suất hóa đơn. |
| Kết thúc lịch trình tiền tạm ứng | Nhập ngày kết thúc của lịch trình tiền tạm ứng. | Ngày này có thể không phải là ngày tạo khoản tạm ứng hoặc trả trước cuối cùng. Ngày mà khoản tạm ứng hoặc trả trước cuối cùng được tạo, cũng bị ảnh hưởng bởi tần suất hóa đơn. |
| Số khoản tiền tạm ứng cần tạo | Khi bạn nhập số lượng khoản tạm ứng cần tạo, hệ thống sẽ sử dụng ngày bắt đầu và tần suất để tạo số lượng trong trường này. | Khi trường này được cập nhật theo cách thủ công, hệ thống sẽ bỏ qua giá trị trong trường **Kết thúc lịch trình tiền tạm ứng** và thay vào đó, tạo số lượng khoản tạm ứng hoặc trả trước cụ thể. |
| Tuần suất hóa đơn | Tần suất ứng dụng sẽ tạo các khoản tạm ứng và trả trước. | Giá trị này ảnh hưởng trực tiếp đến số lượng khoản tạm ứng và trả trước cũng như ngày được tạo. |
| Tổng số tiền | Tổng số tiền là số tiền được chia thành từng khoản tạm ứng hoặc trả trước sẽ được tạo. | Không có tác động xuôi tuyến đối với trường này. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]