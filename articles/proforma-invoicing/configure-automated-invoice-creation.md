---
title: Định cấu hình hoạt động tạo hóa đơn tự động
description: Chủ đề này cung cấp thông tin về cách thức định cấu hình hệ thống để tạo hóa đơn tự động.
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
ms.openlocfilehash: 764fd4568619e4f5676ee3cbf7fce14ffb069548
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898152"
---
# <a name="configure-automated-invoice-creation"></a>Định cấu hình hoạt động tạo hóa đơn tự động

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Hoàn thành các bước sau để định cấu hình chạy hóa đơn tự động trong Hoạt động dự án.

1. Chuyển đến **Chế độ cài đặt** \> **Công việc theo lô**.
2. Tạo một công việc theo lô rồi đặt tên là **Tạo hóa đơn trong hoạt động dự án**. Tên của công việc theo lô phải gồm cụm từ "tạo hóa đơn".
3. Trong trường **Loại công việc**, hãy chọn **Không**. Theo mặc định, các tùy chọn **Tần suất hàng ngày** và **Hiện hoạt** được đặt thành **Có**.
4. Chọn **Chạy quy trình làm việc**. Trong hộp thoại **Tra cứu bản ghi**, bạn sẽ thấy 3 quy trình làm việc:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Chọn **ProcessRunCaller** rồi chọn **Thêm**.
6. Trong hộp thoại tiếp theo, hãy chọn **OK**. Quy trình làm việc **Ngủ** nằm trước quy trình công việc **Xử lý**.

    Bạn cũng có thể chọn **ProcessRunner** trong bước 5. Sau đó, khi bạn chọn **OK**, quy trình làm việc **Xử lý** nằm trước quy trình làm việc **Ngủ**.

Các quy trình làm việc **ProcessRunCaller** và **ProcessRunner** tạo các hóa đơn. **ProcessRunCaller** gọi **ProcessRunner**. **ProcessRunner** là quy trình làm việc thực sự tạo ra hóa đơn. Quy trình này thông qua tất cả mô tả hợp đồng mà các hóa đơn phải được tạo cho và tạo hóa đơn cho các mô tả đó. Để xác định mô tả hợp đồng mà hóa đơn phải được tạo cho, công việc xem xét ngày chạy hóa đơn cho mô tả hợp đồng. Nếu mô tả hợp đồng thuộc một hợp đồng có cùng ngày chạy hóa đơn, thì các giao dịch được kết hợp thành một hóa đơn và có 2 mô tả hóa đơn. Nếu không có giao dịch để tạo hóa đơn cho, công việc này sẽ bỏ qua bước tạo hóa đơn.

Sau khi **ProcessRunner** chạy xong, quy trình này gọi **ProcessRunCaller**, cung cấp thời gian kết thúc và đóng lại. Sau đó, **ProcessRunCaller** khởi động bộ hẹn giờ trong 24 giờ từ thời gian kết thúc đã chỉ định. Khi hết bộ hẹn giờ, **ProcessRunCaller** sẽ đóng lại.

Công việc xử lý lô cho việc tạo hóa đơn là công việc lặp lại. Nếu quy trình lô này chạy nhiều lần, thì nhiều trường hợp công việc được tạo và gây ra lỗi. Do đó, bạn chỉ nên bắt đầu quy trình lô một lần và bắt đầu lại chỉ khi quy trình này dừng chạy.

> [!NOTE]
> Việc lập hóa đơn theo lô chỉ chạy cho các dòng hợp đồng dự án được định cấu hình theo lịch trình hóa đơn. Mô tả hợp đồng với phương thức thanh toán giá cố định phải được định cấu hình các mốc. Mô tả hợp đồng dự án với phương thức thanh toán theo thời gian và vật tư cần thiết lập lịch trình lập hóa đơn theo ngày. Điều này cũng áp dụng cho mô tả hợp đồng dựa trên dự án.     
