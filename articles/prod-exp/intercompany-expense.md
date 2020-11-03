---
title: Chi phí liên công ty
description: Nhân viên của một pháp nhân trong một tổ chức có thể thực hiện công việc cho một pháp nhân khác trong cùng tổ chức đó. Trong tình huống này, bạn có thể sử dụng tính năng chi phí liên công ty để chỉ định chi phí của nhân viên đó cho pháp nhân có công việc được thực hiện.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087259"
---
# <a name="intercompany-expenses"></a>Chi phí liên công ty

[!include [banner](../includes/banner.md)]

Nhân viên của một pháp nhân trong một tổ chức có thể thực hiện công việc cho một pháp nhân khác trong cùng tổ chức đó. Trong tình huống này, bạn có thể sử dụng tính năng chi phí liên công ty để chỉ định chi phí của nhân viên đó cho pháp nhân có công việc được thực hiện. Pháp nhân tuyển dụng nhân viên được gọi là pháp nhân cho mượn. Pháp nhân chịu trách nhiệm đối với chi phí của nhân viên được gọi là pháp nhân mượn. 

Trước khi nhân viên có thể tạo và gửi chi phí đối với công việc được thực hiện cho một pháp nhân khác, ở phần pháp nhân cho mượn, trên trang **Các tham số quản lý chi phí** , hãy chọn tùy chọn **Cho phép các dòng chi phí liên công ty**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Đăng thuế đối với chi phí liên công ty

[!include [banner](../includes/banner.md)]

Nếu bạn muốn sử dụng các nhóm thuế được liên kết với pháp nhân cho mượn (nguồn) thay vì pháp nhân mượn (đích) trong báo cáo chi phí, thì bạn sẽ cần phải đặt cấu hình nhóm thuế này trong phần thiết lập thuế bán hàng trên Sổ Cái. Khi tham số trong Sổ Cái **Pháp nhân để đăng thuế liên công ty** được đặt thành **Nguồn** và **Áp dụng các quy tắc đánh thuế bán hàng** được đặt thành **Không** , tổ hợp thuế cho pháp nhân cho mượn sẽ được sử dụng. Khi tham số đó được đặt thành **Đích** , tổ hợp thuế cho pháp nhân mượn sẽ được sử dụng. Đối với các pháp nhân ở Hoa Kỳ, khi tham số được đặt thành **Nguồn** , trường **Thuế bán hàng phải thu** cũng phải được đặt cấu hình trên trang mới **Nhóm đăng trên Sổ Cái**. Công cụ kế toán sẽ sử dụng thông tin ở trường này cho mục nhập kế toán liên quan đến thuế.   
Hành vi được thực hiện nhất quán đối với các mục mô tả chi phí được đăng có hoặc không có dự án.  
