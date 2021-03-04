---
title: Chi phí liên công ty
description: Chủ đề này cung cấp thông tin về cách sử dụng chi phí liên công ty để chỉ định chi phí của nhân viên cho pháp nhân yêu cầu thực hiện công việc.
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
ms.openlocfilehash: 553ddbe622210169db8de4aa506dcf1ea1e9d5ef
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960858"
---
# <a name="intercompany-expenses"></a>Chi phí liên công ty

Nhân viên của một pháp nhân trong một tổ chức có thể thực hiện công việc cho một pháp nhân khác trong cùng tổ chức đó. Bạn có thể sử dụng chi phí liên công ty để chỉ định chi phí của nhân viên cho pháp nhân yêu cầu thực hiện công việc. Pháp nhân tuyển dụng nhân viên được gọi là pháp nhân cho mượn. Pháp nhân chịu trách nhiệm đối với chi phí của nhân viên được gọi là pháp nhân mượn. 

Trước khi một nhân viên có thể tạo và gửi chi phí liên công ty, bạn phải bật mô tả chi phí liên công ty. Trong pháp nhân cho mượn, trên trang **Các tham số quản lý chi phí**, chọn **Cho phép mô tả chi phí liên công ty**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Đăng thuế đối với chi phí liên công ty

[!include [banner](../includes/banner.md)]

Để có thể dùng các nhóm thuế được liên kết với pháp nhân cho mượn (nguồn) thay vì pháp nhân mượn (đích) trong báo cáo chi phí, bạn phải bật chức năng này trong thiết lập thuế bán hàng của Sổ cái chung. Khi tham số **Pháp nhân đăng thuế liên công ty** được đặt thành **Nguồn** và **Áp dụng các quy tắc đánh thuế bán hàng** được đặt thành **Không**, sự kết hợp thuế cho pháp nhân cho mượn sẽ được dùng. Khi tham số đó được đặt thành **Đích**, tổ hợp thuế cho pháp nhân mượn sẽ được sử dụng. Đối với các pháp nhân ở Hoa Kỳ, khi tham số được đặt thành **Nguồn**, trường **Thuế bán hàng phải thu** cũng phải được đặt cấu hình trên trang mới **Nhóm đăng trên Sổ Cái**. Công cụ kế toán sẽ sử dụng thông tin ở trường này cho mục nhập kế toán liên quan đến thuế.   
Hành vi được thực hiện nhất quán đối với các mục mô tả chi phí được đăng có hoặc không có dự án.  


[!INCLUDE[footer-include](../includes/footer-banner.md)]