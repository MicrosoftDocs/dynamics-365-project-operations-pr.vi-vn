---
title: Loại bỏ giá trị ước tính dự án
description: Bài viết này cung cấp thông tin về việc loại bỏ giá trị ước tính dự án sau khi hoàn thành.
author: Yowelle
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: de54659f9e69daf1566f86bec16436c19eeacf49
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932230"
---
# <a name="eliminate-a-project-estimate"></a>Loại bỏ giá trị ước tính dự án

[!include [banner](../includes/banner.md)]

Giá trị ước tính dự án cung cấp dạng xem tài chính cho công việc được ước tính và lập lịch trình cho một dự án. Để làm việc với các giá trị ước tính cho dự án, bạn phải đính kèm dự án ấy với một dự án ước tính. Dự án ước tính luôn dựa trên một dự án hiện có, tuy nhiên, nhiều dự án có thể tham chiếu một dự án ước tính. Chỉ dự án đầu tư và giá cố định mới có thể được đính kèm với dự toán và các dự án đó phải nằm trong cùng nhóm dự án với dự án ước tính.

Để loại bỏ một dự án ước tính, dự án đó phải được hoàn thành. Các bước sau đây giải thích cách loại bỏ giá trị ước tính.

1. Chuyển tới **Quản lý dự án và kế toán** > **Tất cả dự án** và mở dự án. 
2. Chọn **Ước tính** trên tab **Quản lý** và trên trang **Ước tính**, hãy chọn **Loại bỏ**.
3. Trên trang **Loại bỏ giá trị ước tính** ở tab **Tổng quát**, hãy đặt các tùy chọn sau:

   - **Mã kỳ**: Chọn mã kỳ để chọn các dự án ước tính phù hợp. 
   - **Ngày ước tính**: Chọn ngày ước tính thích hợp cần loại bỏ.
   - **Loại bỏ với cảnh báo WIP**: Kích hoạt tùy chọn này để cung cấp thông báo khi giá trị ước tính sẽ loại bỏ được liên kết với công việc đang tiến hành (WIP). Khi tùy chọn này không được kích hoạt, hoạt động loại bỏ sẽ không thể tiếp tục nếu tồn tại bất kỳ giao dịch không ước tính nào. 
   > [!NOTE]
   > Tùy chọn này chỉ khả dụng khi hoạt động loại bỏ được áp dụng cho dự án ước tính. Tùy chọn này không có sẵn nếu bạn sử dụng mục đăng định kỳ. Mục thiết đặt này hoạt động với mục thiết đặt trên tab **Ước tính** ở trang **Tham số dự án**, trong nhóm trường **Cho phép loại bỏ khi tồn tại giao dịch không ước tính**.
   - **Đặt giai đoạn thành Đã kết thúc**: Kích hoạt tùy chọn này để đặt giai đoạn của dự án ước tính thành **Đã kết thúc** sau khi bạn chạy hoạt động loại bỏ.
   - **In danh sách giá trị ước tính**: Chọn thông tin sẽ đưa vào khi in danh sách giá trị ước tính.
   - **Hiển thị Infolog**: Kích hoạt tùy chọn này để hiển thị Infolog.
   - **Ngày đăng**: Chọn ngày đăng giá trị ước tính vào sổ cái.

4.  Chọn **OK**.
5. Sau khi quy trình loại bỏ hoàn tất, dự án ước tính đã loại bỏ sẽ được hiển thị với giá trị âm. 

Nếu bạn không định loại bỏ giá trị ước tính, thì bạn có thể chọn giá trị ước tính đã loại bỏ và chọn **Đảo ngược hoạt động loại bỏ**.   


[!INCLUDE[footer-include](../includes/footer-banner.md)]