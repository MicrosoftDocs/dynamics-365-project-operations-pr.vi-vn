---
title: Mô tả hợp đồng phụ cho thời gian
description: Chủ đề này giải thích cách ghi lại các mô tả hợp đồng phụ cho thời gian và ghi lại giao dịch mua thời gian từ các nhà cung cấp.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 10ebe0fcc86b4652ac01e28108361df1f768b61d
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323892"
---
# <a name="subcontract-lines-for-time"></a>Mô tả hợp đồng phụ cho thời gian

[!include [banner](../../includes/dataverse-preview.md)]

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Một hợp đồng phụ trong Dynamics 365 Project Operations có thể có mô tả hợp đồng phụ về thời gian. Các mô tả hợp đồng phụ về thời gian cho phép Người quản lý dự án mua thời gian nguồn lực của nhà cung cấp để sắp xếp nhân viên thực hiện các nhiệm vụ dự án và các yêu cầu về nguồn lực.

Để tạo mô tả hợp đồng phụ về thời gian trong Project Operations, hãy hoàn thành các bước sau.

1. Trong ngăn điều hướng, hãy chọn **Hợp đồng phụ** và mở một hợp đồng phụ.
2. Trên tab **Mô tả hợp đồng phụ**, chọn **Mới** để tạo mô tả hợp đồng phụ mới.
3. Trên trang **Tạo nhanh**, trong trường **Lớp giao dịch**, chọn **Thời gian**.
4. Nhập thông tin còn lại của trường rồi chọn **Lưu**.

  Bảng sau cung cấp thông tin về các trường trên trang **Mô tả hợp đồng phụ** và trang **Tạo nhanh**.

| **Trường** | **Mô tả** |
| --- | --- |
| Tên | Tên của mô tả hợp đồng phụ. |
| Mô tả | Mô tả ngắn gọn về các dịch vụ đang được mua trên mục mô tả hợp đồng phụ. | 
| Loại mô tả | Trường này là một giá trị mặc định.  |
| Phương thức thanh toán | Chọn phương thức thanh toán. Dựa trên phương thức thanh toán của mô tả hợp đồng phụ được tham chiếu, lịch trình hóa đơn dựa trên cột mốc có sẵn cho phương thức thanh toán theo Giá cố định. |
| Lớp giao dịch | Trường này là một giá trị mặc định cho biết mô tả hợp đồng phụ có đang được sử dụng để ghi lại việc mua thời gian của nhà thầu phụ hay không. |
| Vai trò | Vai trò của các nguồn lực của hợp đồng phụ có thời gian được mua. Vai trò được giao cho các nguồn lực của hợp đồng phụ quyết định chi phí mua hàng. |
| Ngày bắt đầu được yêu cầu | Ngày mà các nguồn lực của nhà thầu phụ được yêu cầu để bắt đầu hoạt động. Ngày yêu cầu được sử dụng để chọn một bảng giá dự án từ các bảng giá dự án kèm theo hợp đồng phụ. Khi đó, chi phí của vai trò trên mô tả hợp đồng phụ được mặc định từ bảng giá đó. |
| Ngày kết thúc được yêu cầu | Ngày kết thúc công việc của nguồn lực của nhà thầu phụ. Ngày này được sử dụng để hiển thị cảnh báo khi Người quản lý dự án rút ra từ năng lực này đối với các yêu cầu nguồn lực xảy ra sau ngày này. |
| Số lượng đã đặt hàng | Số giờ của Vai trò được mua từ nhà cung cấp. Giá trị này được sử dụng để hiển thị cảnh báo khi Người quản lý dự án rút ra quá mức từ năng lực này đối với các yêu cầu nguồn lực. |
| nhóm đơn vị đo | Giá trị trường này mặc định cho nhóm Đơn vị thời gian và không thể thay đổi.  |
| Đơn vị | Trường này mặc định là đơn vị giờ cơ sở từ nhóm Đơn vị thời gian. Bạn có thể thay đổi giá trị này để mua bất kỳ đơn vị nào trong nhóm Đơn vị thời gian, chẳng hạn như ngày hoặc tuần. Sự kết hợp giữa Vai trò và Đơn vị được sử dụng để tính đơn giá cho mô tả hợp đồng phụ. |
| Đơn giá | Đơn giá đặt mặc định từ kết hợp Vai trò và Đơn vị từ bảng giá dự án áp dụng cho ngày bắt đầu được yêu cầu của mô tả hợp đồng phụ. Khi bảng giá dự án áp dụng có giá được lập theo đơn vị khác với đơn vị trên mô tả hợp đồng phụ, hệ thống sẽ sử dụng quy đổi đơn vị để tính theo đơn giá. |
| Tổng con | Đây là trường chỉ đọc được tự động tính là **Số lượng x Đơn giá** nếu cả giá trị số lượng và đơn giá được nhập. Nếu một trong hai hoặc cả hai trường số lượng, đơn giá đều trống, thì bạn có thể nhập giá trị vào trường này. |
| Thuế doanh thu |  Nhập số tiền thuế bán hàng. |
| Tổng số tiền | Tổng số tiền của mô tả hợp đồng phụ sau khi bao gồm thuế. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
