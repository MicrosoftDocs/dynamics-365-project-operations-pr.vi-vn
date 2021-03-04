---
title: Thiết lập quy trình làm việc Quản lý chi phí
description: Bạn có thể thiết lập một quy trình làm việc để xem xét và phê duyệt các tài liệu về chi phí và đi lại.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8f3235d12499c68a52f9d1c7e118e7bc91dc3a0a
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960543"
---
# <a name="set-up-expense-management-workflows"></a>Thiết lập quy trình làm việc Quản lý chi phí

Bạn có thể thiết lập một quy trình làm việc được sử dụng để xem xét và phê duyệt các tài liệu về chi phí và đi lại. Bạn có thể xác định quy trình làm việc cho các tài liệu như: báo cáo chi phí, yêu cầu đi lại và yêu cầu tạm ứng tiền mặt.

Mỗi quy trình làm việc đại diện cho một quy trình công việc. Quy trình này xác định cách thức đưa một tài liệu qua hệ thống và cho biết ai phải hoàn thành một nhiệm vụ hoặc phê duyệt một tài liệu. Có một vài lợi ích khi sử dụng hệ thống quy trình làm việc trong tổ chức của bạn:

-   **Quy trình nhất quán**: Bạn có thể xác định quy trình phê duyệt cho các tài liệu cụ thể, như yêu cầu mua hàng và báo cáo chi phí. Việc sử dụng hệ thống quy trình làm việc giúp bảo đảm rằng các tài liệu được xử lý và phê duyệt một cách nhất quán và hiệu quả.

-   Khả năng hiển thị trên quy trình: Bạn có thể theo dõi trạng thái, lịch sử và số liệu hiệu suất của một phiên bản quy trình làm việc cụ thể. Điều này giúp bạn xác định xem có nên thực hiện các thay đổi đối với quy trình làm việc để nâng cao hiệu quả hay không.

-   Danh sách công việc tập trung: Người dùng có thể xem danh sách công việc tập trung để biết các nhiệm vụ và mục phê duyệt trong quy trình làm việc được chỉ định cho họ. 

**Các loại quy trình làm việc mà bạn có thể tạo**

Bảng sau liệt kê các loại quy trình làm việc mà bạn có thể tạo trong **Chi phí**.


|              <strong>Loại</strong>              |                   <strong>Sử dụng loại này để</strong>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <strong>Báo cáo chi phí</strong>         |            Tạo quy trình làm việc cho báo cáo chi phí.             |
|  <strong>Tự động đăng báo cáo chi phí</strong>   |        Tạo quy trình làm việc tự động đăng cho báo cáo chi phí.        |
|       <strong>Mục mô tả chi phí</strong>        |     Tạo quy trình làm việc cho mục mô tả trên báo cáo chi phí.      |
| <strong>Tự động đăng mục mô tả chi phí</strong> | Tạo quy trình làm việc tự động đăng cho mục mô tả trên báo cáo chi phí. |
|       <strong>Tiêu chuẩn đi lại</strong>       |          Tạo quy trình làm việc phê duyệt cho tiêu chuẩn đi lại.           |
|      <strong>Yêu cầu tạm ứng tiền mặt</strong>      |         Tạo quy trình làm việc phê duyệt cho yêu cầu tạm ứng tiền mặt.          |
|        <strong>Hoàn thuế GTGT</strong>        | Tạo quy trình làm việc phê duyệt cho việc hoàn thuế giá trị gia tăng (VAT).  |



[!INCLUDE[footer-include](../includes/footer-banner.md)]