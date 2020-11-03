---
title: Đặt cấu hình hoạt động tạo hóa đơn tự động
description: Chủ đề này cung cấp thông tin về cách thức đặt cấu hình để hệ thống tự động tạo hóa đơn.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4e7572f2bc6201960ac01ce521adf39ac2577dbe
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087001"
---
# <a name="configure-automatic-invoice-creation"></a>Đặt cấu hình hoạt động tạo hóa đơn tự động

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_


Hoàn thành các bước sau để đặt cấu hình lần chạy hóa đơn tự động trong Dynamics 365 Project Operations.

1. Chuyển tới **Thiết đặt** > **Công việc theo lô**.
2. Tạo một công việc theo lô rồi đặt tên là **Tạo hóa đơn trong hoạt động dự án**. Tên của công việc theo lô phải có cụm từ "tạo hóa đơn".
3. Ở trường **Loại công việc** , hãy chọn **Không có**. Theo mặc định, các tùy chọn **Tần suất hàng ngày** và **Hiện hoạt** được đặt thành **Có**.
4. Chọn **Chạy quy trình làm việc**. Trong hộp thoại **Tra cứu bản ghi** , bạn sẽ thấy 3 quy trình làm việc:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Chọn **ProcessRunCaller** rồi chọn **Thêm**.
6. Trong hộp thoại tiếp theo, hãy chọn **OK**. Quy trình làm việc **Ngủ** nằm trước quy trình công việc **Xử lý**.

  > [!NOTE]
  > Bạn cũng có thể chọn **ProcessRunner** trong bước 5. Sau đó, khi bạn chọn **OK** , quy trình làm việc **Xử lý** nằm trước quy trình làm việc **Ngủ**.

Các quy trình làm việc **ProcessRunCaller** và **ProcessRunner** tạo các hóa đơn. **ProcessRunCaller** gọi **ProcessRunner**. **ProcessRunner** là quy trình làm việc thực sự tạo ra hóa đơn. Quy trình này thông qua tất cả mô tả hợp đồng mà các hóa đơn phải được tạo cho và tạo hóa đơn cho các mô tả đó. Để xác định mô tả hợp đồng mà hóa đơn phải được tạo cho, công việc xem xét ngày chạy hóa đơn cho mô tả hợp đồng. Nếu mô tả hợp đồng thuộc một hợp đồng có cùng ngày chạy hóa đơn, thì các giao dịch được kết hợp thành một hóa đơn và có 2 mô tả hóa đơn. Nếu không có giao dịch để tạo hóa đơn cho, công việc này sẽ bỏ qua bước tạo hóa đơn.

Sau khi **ProcessRunner** chạy xong, quy trình này gọi **ProcessRunCaller** , cung cấp thời gian kết thúc và đóng lại. Sau đó, **ProcessRunCaller** khởi động bộ hẹn giờ trong 24 giờ từ thời gian kết thúc đã chỉ định. Khi hết bộ hẹn giờ, **ProcessRunCaller** sẽ đóng lại.

Công việc xử lý lô cho việc tạo hóa đơn là công việc lặp lại. Nếu quy trình lô này chạy nhiều lần, thì nhiều trường hợp công việc được tạo và gây ra lỗi. Do đó, bạn chỉ nên bắt đầu quy trình lô một lần và bắt đầu lại chỉ khi quy trình này dừng chạy.

> [!NOTE]
> Việc lập hóa đơn theo lô chỉ chạy cho các dòng hợp đồng dự án được định cấu hình theo lịch trình hóa đơn. Mô tả hợp đồng với phương thức thanh toán giá cố định phải được định cấu hình các mốc. Mô tả hợp đồng dự án với phương thức thanh toán theo thời gian và vật tư cần thiết lập lịch trình lập hóa đơn theo ngày. Điều này cũng áp dụng cho mô tả hợp đồng dựa trên dự án.     
