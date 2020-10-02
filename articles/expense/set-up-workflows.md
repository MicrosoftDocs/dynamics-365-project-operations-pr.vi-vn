---
title: Thiết lập quy trình làm việc để quản lý chi phí
description: Bạn có thể thiết lập một quy trình làm việc được sử dụng để xem xét và phê duyệt các tài liệu về chi phí và đi lại.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: dfc5945f32bb8d4073fc31499979ba279fef66a4
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896577"
---
# <a name="set-up-workflows-for-expense-management"></a>Thiết lập quy trình làm việc để quản lý chi phí

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Bạn có thể thiết lập một quy trình làm việc để xem xét và phê duyệt các tài liệu về chi phí và đi lại. Bạn có thể xác định quy trình làm việc cho các báo cáo chi phí, tiêu chuẩn đi lại và yêu cầu tạm ứng tiền mặt.

Quy trình làm việc đại diện cho một quy trình kinh doanh và xác định cách tài liệu đi qua hệ thống. Quy trình làm việc cũng cho biết ai phải hoàn thành tác vụ hoặc phê duyệt tài liệu. Có một vài lợi ích khi sử dụng hệ thống quy trình làm việc trong tổ chức của bạn:

- **Quy trình nhất quán**: Bạn có thể xác định quy trình phê duyệt cho các tài liệu cụ thể, chẳng hạn như yêu cầu mua hàng và báo cáo chi phí. Sử dụng hệ thống quy trình làm việc giúp đảm bảo rằng các tài liệu được xử lý và phê duyệt một cách nhất quán và hiệu quả.
- **Khả năng hiển thị quá trình**: Bạn có thể theo dõi trạng thái, lịch sử và số liệu hiệu suất của một phiên bản quy trình làm việc cụ thể. Điều này giúp bạn xác định xem có nên thực hiện các thay đổi đối với quy trình làm việc để nâng cao hiệu quả hay không.
- **Danh sách công việc tập trung**: Người dùng có thể xem danh sách công việc tập trung để xem các tác vụ và mục phê duyệt của quy trình làm việc được chỉ định cho họ. 

## <a name="workflow-types"></a>Các loại quy trình làm việc

Bảng sau liệt kê các loại quy trình làm việc mà bạn có thể tạo trong **Quản lý chi phí**.


|              <strong>Loại</strong>              |                   <strong>Sử dụng loại này để</strong>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <strong>Tự động phê duyệt báo cáo chi phí</strong> |            Tạo quy trình làm việc cho báo cáo chi phí.             |
|  <strong>Tự động đăng báo cáo chi phí</strong>   |        Tạo quy trình làm việc tự động đăng cho báo cáo chi phí.        |
|       <strong>Mục mô tả chi phí</strong>        |     Tạo quy trình làm việc cho mục mô tả trên báo cáo chi phí.      |
| <strong>Tự động đăng mục mô tả chi phí</strong> | Tạo quy trình làm việc tự động đăng cho mục mô tả trên báo cáo chi phí. |
|       <strong>Tiêu chuẩn đi lại</strong>       |          Tạo quy trình làm việc phê duyệt cho tiêu chuẩn đi lại.           |
|      <strong>Yêu cầu tạm ứng tiền mặt</strong>      |         Tạo quy trình làm việc phê duyệt cho yêu cầu tạm ứng tiền mặt.          |
|        <strong>Hoàn thuế GTGT</strong>        | Tạo quy trình làm việc phê duyệt cho việc hoàn thuế giá trị gia tăng (VAT).  |
