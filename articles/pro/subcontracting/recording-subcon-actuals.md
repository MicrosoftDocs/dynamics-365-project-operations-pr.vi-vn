---
title: Ghi lại thời gian, chi phí và mức sử dụng vật liệu cho các thành phần trong hợp đồng phụ
description: Bài viết này giải thích cách Microsoft theo dõi thời gian, chi phí và việc sử dụng vật liệu trên các dự án từ các thành phần hợp đồng phụ được theo dõi bởi Microsoft Dynamics 365 Project Operations.
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
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Ghi lại thời gian, chi phí và mức sử dụng vật liệu trên dự án cho các thành phần trong hợp đồng phụ

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Bài viết này giải thích cách Microsoft theo dõi thời gian, chi phí và việc sử dụng vật liệu trên các dự án từ các thành phần hợp đồng phụ được theo dõi bởi Microsoft Dynamics 365 Project Operations.

## <a name="costing-for-subcontractor-time-on-projects"></a>Chi phí cho thời gian của nhà thầu phụ trong dự án
Trong Project Operations, nhân viên hợp đồng có thể ghi lại thời gian trên các dự án theo cách tương tự như nhân viên. Khi nhập thời gian trên dự án và/hoặc nhiệm vụ dự án, nhân viên hợp đồng có thể chọn một hợp đồng phụ và mô tả hợp đồng phụ cụ thể.

Khi thời gian do nhân viên hợp đồng gửi được chấp thuận, chi phí dự án được ghi lại bằng cách sử dụng tỷ lệ chi phí đơn vị được thiết lập cho nguồn lực nhân viên hợp đồng đó trong phần **Giá vai trò** của bảng giá mua trên hợp đồng phụ.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>Nhập chi phí theo hợp đồng phụ trên các dự án
Khi nhập chi phí phát sinh cho các dự án, bạn có thể chọn một hợp đồng phụ và mô tả hợp đồng phụ trên mục nhập chi phí. 

Khi mục nhập chi phí này được gửi và phê duyệt, chi phí được ghi lại trên dự án dựa theo chi phí đơn vị được thiết lập cho thể loại giao dịch đó trong phần **Giá thể loại** của bảng giá mua trên hợp đồng phụ.

## <a name="costing-for-subcontracted-materials-on-projects"></a>Nhập chi phí cho vật tư theo hợp đồng phụ trên các dự án
Khi nhập mức sử dụng vật tư cho các dự án, bạn có thể chọn một hợp đồng phụ và mô tả hợp đồng phụ trên nhật ký sử dụng vật tư. Khi nhật ký sử dụng vật tư này được gửi và phê duyệt, chi phí vật tư được ghi lại trên dự án dựa theo chi phí đơn vị được thiết lập cho sản phẩm đó trong phần **Mục bảng giá** của bảng giá hợp đồng phụ.

Việc sử dụng vật tư cũng có thể được ghi lại cho các sản phẩm chọn thêm trên dự án. Loại hình sử dụng vật tư này cũng có thể được liên kết với một hợp đồng phụ và mô tả hợp đồng phụ. Khi ghi lại việc sử dụng vật tư cho các sản phẩm chọn thêm, bạn cần nhập chi phí trên mỗi đơn vị của sản phẩm chọn thêm. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
