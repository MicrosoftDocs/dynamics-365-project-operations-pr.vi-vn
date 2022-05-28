---
title: Chi phí liên công ty
description: Chủ đề này cung cấp thông tin về cách sử dụng chi phí liên công ty để chỉ định chi phí của nhân viên cho pháp nhân yêu cầu thực hiện công việc.
author: suvaidya
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6788a590879bd839ebb9dedc45895dc047cc9f15
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684260"
---
# <a name="intercompany-expenses"></a>Chi phí liên công ty

Nhân viên của một pháp nhân trong một tổ chức có thể thực hiện công việc cho một pháp nhân khác trong cùng tổ chức đó. Bạn có thể sử dụng chi phí liên công ty để chỉ định chi phí của nhân viên cho pháp nhân yêu cầu thực hiện công việc. Pháp nhân tuyển dụng nhân viên được gọi là pháp nhân cho mượn. Pháp nhân chịu trách nhiệm đối với chi phí của nhân viên được gọi là pháp nhân mượn. 

Trước khi một nhân viên có thể tạo và gửi chi phí liên công ty, bạn phải bật mô tả chi phí liên công ty. Trong pháp nhân cho mượn, trên trang **Các tham số quản lý chi phí**, chọn **Cho phép mô tả chi phí liên công ty**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Đăng thuế đối với chi phí liên công ty

[!include [banner](../includes/banner.md)]

Để có thể dùng các nhóm thuế được liên kết với pháp nhân cho mượn (nguồn) thay vì pháp nhân mượn (đích) trong báo cáo chi phí, bạn phải bật chức năng này trong thiết lập thuế bán hàng của Sổ cái chung. Khi tham số **Pháp nhân đăng thuế liên công ty** được đặt thành **Nguồn** và **Áp dụng các quy tắc đánh thuế bán hàng** được đặt thành **Không**, sự kết hợp thuế cho pháp nhân cho mượn sẽ được dùng. Khi tham số đó được đặt thành **Đích**, tổ hợp thuế cho pháp nhân mượn sẽ được sử dụng. Đối với các pháp nhân ở Hoa Kỳ, khi tham số được đặt thành **Nguồn**, trường **Thuế bán hàng phải thu** cũng phải được đặt cấu hình trên trang mới **Nhóm đăng trên Sổ Cái**. Công cụ kế toán sẽ sử dụng thông tin ở trường này cho mục nhập kế toán liên quan đến thuế.   
Hành vi được thực hiện nhất quán đối với các mục mô tả chi phí được đăng có hoặc không có dự án.  

## <a name="new-expense-expression-builder"></a>Trình tạo biểu thức chi phí mới

Trình tạo biểu thức chi phí mới giải quyết các vấn đề với các tình huống chi phí liên công ty sử dụng các dự án. Tính năng này đảm bảo rằng, khi bạn tạo chi phí liên công ty, chính sách chi phí được xác thực chính xác dựa trên dự án được chọn trên dòng chi phí và báo cáo chi phí có thể được gửi thành công.

Bạn phải bật tính năng trình tạo biểu thức chi phí nếu muốn sử dụng. Ngoài ra, bạn nên thiết lập chính sách chi phí có ID dự án.

Nếu bạn đã định cấu hình các chính sách xác thực ID dự án trên dòng chi phí, thì phải gỡ bỏ các chính sách đó. Sau đó, bạn có thể bật tính năng này và định cấu hình lại các chính sách.

Để bật tính năng này, hãy làm theo các bước bên dưới.

1. Chuyển đến **Không gian làm việc** \> **Quản lý tính năng**.
2. Trong danh sách, hãy chọn **Trình tạo biểu thức chi phí mới giải quyết các vấn đề với các tình huống chi phí liên công ty sử dụng các dự án**. Sau đó chọn **Kích hoạt ngay bây giờ**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
