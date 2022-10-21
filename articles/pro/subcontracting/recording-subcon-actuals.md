---
title: Ghi lại thời gian, chi phí và mức sử dụng vật liệu cho các thành phần trong hợp đồng phụ
description: Bài viết này giải thích cách Microsoft theo dõi việc sử dụng thời gian, chi phí và vật liệu trên các dự án từ các thành phần được ký hợp đồng phụ Dynamics 365 Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b82c14412cfb0405040902a2329c3b6692422d89
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522540"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Ghi lại thời gian, chi phí và việc sử dụng vật liệu trong các dự án cho các thành phần được thầu phụ

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Bài viết này giải thích cách Microsoft theo dõi việc sử dụng thời gian, chi phí và vật liệu trên các dự án từ các thành phần được ký hợp đồng phụ Dynamics 365 Project Operations.

## <a name="costing-for-subcontractor-time-on-projects"></a>Tốn thời gian của nhà thầu phụ trong các dự án
Trong Hoạt động Dự án, nhân viên hợp đồng có thể ghi lại thời gian trên các dự án theo cách tương tự như nhân viên. Khi nhập thời gian vào các dự án và / hoặc nhiệm vụ dự án, nhân viên hợp đồng có thể chọn một hợp đồng phụ và dây chuyền hợp đồng phụ cụ thể.

Khi thời gian do nhân viên hợp đồng đệ trình được chấp thuận, chi phí dự án được ghi nhận bằng cách sử dụng tỷ lệ chi phí đơn vị được thiết lập cho nguồn nhân viên hợp đồng đó trong **Giá vai trò** phần bảng giá mua trên hợp đồng phụ.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>Định phí chi phí thầu phụ cho các dự án
Khi nhập chi phí phát sinh cho các dự án, bạn có thể chọn một hợp đồng phụ và dòng hợp đồng phụ trên mục nhập chi phí. 

Khi mục nhập chi phí này được đệ trình và phê duyệt, chi phí chi phí được ghi nhận vào dự án dựa trên đơn giá được thiết lập cho loại giao dịch đó trong **Giá loại** phần bảng giá mua trên hợp đồng phụ.

## <a name="costing-for-subcontracted-materials-on-projects"></a>Chi phí cho vật liệu thầu phụ trong các dự án
Khi nhập việc sử dụng vật liệu cho các dự án, bạn có thể chọn một hợp đồng phụ và dòng hợp đồng phụ trên nhật ký sử dụng vật liệu. Khi nhật ký sử dụng vật liệu được đệ trình và phê duyệt, chi phí vật liệu được ghi nhận vào dự án dựa trên đơn giá được thiết lập cho sản phẩm đó trong **Các mặt hàng trong bảng giá** phần bảng giá thầu phụ.

Việc sử dụng vật liệu cũng có thể được ghi lại cho các sản phẩm ghi trong các dự án. Loại hình sử dụng vật liệu này cũng có thể được liên kết với một đường dây thầu phụ và hợp đồng phụ. Khi ghi lại việc sử dụng nguyên liệu cho các sản phẩm viết sẵn, bạn cần nhập chi phí trên mỗi đơn vị của sản phẩm ghi sẵn. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]