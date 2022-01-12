---
title: Tính toán chi phí
description: Chủ đề này giải thích cách tối thiểu hóa chi phí bằng cách sử dụng không gian làm việc Chi phí được mô phỏng lại.
author: suvaidya
ms.date: 12/16/2021
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: b2077b77af036ce64aad203f52b03cacca8c4099
ms.sourcegitcommit: 9d20e7738cce195d344f5925a115741a1ce3ca36
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 12/21/2021
ms.locfileid: "7944163"
---
# <a name="expense-itemization"></a>Tính toán chi phí

[!include [banner](../includes/banner.md)]

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Các tổ chức thường yêu cầu nhân viên cung cấp bảng phân tích chi tiết các chi phí phát sinh trong quá trình đi du lịch. Ví dụ, một foo khách sạn có thể chứa một số dòng chia thành từng mục cho giá phòng, thuế, bãi đậu xe và các chi phí linh tinh khác phát sinh mỗi ngày trong suốt thời gian lưu trú. Hoặc chi phí bữa ăn có thể yêu cầu bạn cung cấp bảng phân tích chi tiết hơn cho bữa sáng, bữa trưa hoặc bữa tối. Bất kể nhu cầu của tổ chức là gì, mỗi danh mục chi phí có thể được thiết lập để phản ánh các danh mục phụ hoặc các mục hàng tạo nên một khoản chi phí. Mặc dù việc chia thành từng khoản luôn được hỗ trợ trong **Quản lý chi tiêu**, các **Chi phí mô phỏng lại** không gian làm việc cho phép chia mục hiệu quả hơn khi tính năng, **Khả năng thành các khoản chi phí định kỳ một cách nhanh chóng** được kích hoạt.  

## <a name="enable-quick-itemization"></a>Bật tính năng chia thành từng khoản nhanh 

Bạn có thể dùng **Khả năng thành các khoản chi phí định kỳ một cách nhanh chóng** tính năng ghi lại các khoản chi phí định kỳ một cách nhanh chóng trong khi tránh phải nhập các chi phí hàng ngày mỗi lần trong suốt thời gian lưu trú. Hoàn thành các bước sau để kích hoạt tính năng chia thành từng khoản nhanh chóng.

1. Đi đến **Quản lý tính năng** không gian làm việc và trong danh sách các tính năng, định vị và chọn, **Báo cáo chi phí được mô phỏng lại**. 
2. Chọn **Bật ngay**. 
3. Trong danh sách tính năng, hãy tìm và chọn, **Khả năng thành các khoản chi phí định kỳ một cách nhanh chóng**.
4. Chọn **Bật ngay**. 

## <a name="itemization-grid"></a>Lưới lặp lại 

Nếu một danh mục chi phí có các danh mục con hoặc các thành phần khác nhau tạo nên chi phí đó, thì nó có thể được chia thành từng khoản. Để tối thiểu hóa một khoản chi phí, hãy chọn dòng chi phí trong báo cáo chi phí và trong **Chi tiết chi phí** ngăn, chọn **Hành động** > **Lặp lại**. Các **Lặp lại** thanh trượt hiển thị một lưới với các trường. Bảng sau cung cấp ví dụ về từng trường trong lưới và cách trường được hiển thị trong báo cáo chi phí. 

|     Trường          |     Description                                                                                  |     Ví dụ:              |
|--------------------|--------------------------------------------------------------------------------------------------|--------------------------|
|     Thể loại con    |     Danh sách các danh mục con được định cấu hình trong loại danh mục chi phí, **Khách sạn**.             |     Giá phòng hàng ngày      |
|     Ngày bắt đầu     |     Ngày phát sinh khoản mục chi phí đầu tiên.                                           |     13/09/2021           |
|     Tỷ lệ hàng ngày     |     Số tiền phát sinh cho khoản mục chi phí.                                                    |     200                  |
|     Số lượng       |     Số lần sạc được lặp lại trong một khoảng thời gian liên tục.                       |     3                    |

![Giảm thiểu chi phí.](media/Itemization%20screen%201.png)

Khi bạn lưu một khoản mục, bạn sẽ thấy một dòng được chia thành từng khoản cho số lượng được chỉ định trong lưới Lặp lại. Mỗi dòng bắt đầu vào ngày được chỉ định trong lưới.

![Báo cáo được lặp lại.](media/Itemization%20screen%202.png)

