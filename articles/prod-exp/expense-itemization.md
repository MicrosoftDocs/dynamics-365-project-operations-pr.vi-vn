---
title: Phân loại thành các khoản chi phí
description: Bài viết này giải thích cách ghi từng khoản chi phí bằng cách sử dụng không gian làm việc Chi phí được thiết kế lại.
author: suvaidya
ms.date: 12/16/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 71bfbe83259804fc0b0355c81d430805da23dd45
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920960"
---
# <a name="expense-itemization"></a>Phân loại thành các khoản chi phí

[!include [banner](../includes/banner.md)]

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Các tổ chức thường yêu cầu nhân viên cung cấp bảng phân tích chi tiết các chi phí phát sinh trong quá trình đi lại. Ví dụ, một hồ sơ khách sạn có thể chứa một vài dòng được ghi thành khoản tương ứng với giá phòng, thuế, phí đỗ xe và các chi phí khác phát sinh mỗi ngày trong suốt thời gian lưu trú. Hoặc chi phí bữa ăn có thể yêu cầu bạn cung cấp bảng phân tích chi tiết hơn cho bữa sáng, bữa trưa hoặc bữa tối. Bất kể nhu cầu của tổ chức là gì, mỗi danh mục chi phí có thể được thiết lập để phản ánh các danh mục phụ hoặc các mục mô tả tạo nên một khoản chi phí. Mặc dù việc ghi thành từng khoản luôn được hỗ trợ trong **Quản lý chi phí**, không gian làm việc **Chi phí mô phỏng lại** cho phép việc ghi lại từng khoản được hiệu quả hơn khi tính năng **Khả năng ghi từng khoản chi phí định kỳ một cách nhanh chóng** được kích hoạt.  

## <a name="enable-quick-itemization"></a>Bật phân khoản nhanh 

Bạn có thể dùng tính năng **Khả năng ghi lại các chi phí định kỳ một cách nhanh chóng** để ghi từng khoản định kỳ một cách nhanh chóng trong khi tránh phải nhập các chi phí hàng ngày mỗi lần trong suốt thời gian lưu trú. Hoàn thành các bước sau để bật tính năng phân khoản nhanh.

1. Chuyển tới không gian làm việc **Quản lý tính năng** và trong danh sách các tính năng, tìm và chọn **Báo cáo chi phí được xây dựng lại**. 
2. Chọn **Bật ngay**. 
3. Trong danh sách tính năng, tìm và chọn **Khả năng ghi lại các chi phí định kỳ một cách nhanh chóng**.
4. Chọn **Bật ngay**. 

## <a name="itemization-grid"></a>Lưới phân khoản 

Nếu một danh mục chi phí có các danh mục con hoặc các thành phần khác nhau tạo nên chi phí đó, thì nó có thể được ghi từng khoản. Để ghi lại một khoản chi phí, hãy chọn dòng chi phí trong báo cáo chi phí và trong ngăn **Chi tiết chi phí**, chọn **Hành động** > **Ghi thành từng khoản**. Thanh trượt **Ghi thành từng khoản** hiện ra một lưới có các trường. Bảng sau đây cung cấp ví dụ về từng trường trong lưới và cách trường được hiển thị trong báo cáo chi phí. 

|     Trường          |     Description                                                                                  |     Ví dụ:              |
|--------------------|--------------------------------------------------------------------------------------------------|--------------------------|
|     Thể loại con    |     Danh sách các danh mục con được định cấu hình trong loại danh mục chi phí, **Khách sạn**.             |     Giá phòng hàng ngày      |
|     Ngày bắt đầu     |     Ngày phát sinh khoản mục chi phí đầu tiên.                                           |     13/09/2021           |
|     Tỷ lệ hàng ngày     |     Số tiền phát sinh cho khoản mục chi phí.                                                    |     200                  |
|     Số lượng       |     Số lần hoạt động nạp được lặp lại trong một khoảng thời gian liên tục.                       |     3                    |

![Chi phí chia khoản.](media/Itemization%20screen%201.png)

Khi bạn lưu một khoản mục, bạn sẽ thấy một dòng được ghi từng khoản cho số lượng được chỉ định trong lưới Phân khoản. Mỗi dòng bắt đầu vào ngày được chỉ định trong lưới.

![Báo cáo được ghi từng khoản.](media/Itemization%20screen%202.png)

