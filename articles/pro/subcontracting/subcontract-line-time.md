---
title: Mô tả hợp đồng phụ cho thời gian
description: Bài viết này giải thích cách ghi các dòng hợp đồng phụ cho thời gian và ghi lại việc mua thời gian từ các nhà cung cấp.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0295ddd1b36eef9289110c4fe7b51397d81320d6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925974"
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

| **Trường** | **Mô tả** | **Tác động chức năng** |
| --- | --- | --- |
| Tên | Tên của mô tả hợp đồng phụ để giúp xác định. | Đây sẽ được hiển thị là cột đầu tiên trong tất cả các tra cứu dựa trên các mô tả hợp đồng phụ. |
| Mô tả | Mô tả ngắn gọn về các dịch vụ đang được mua trên mục mô tả hợp đồng phụ. |Không có |
| Loại mô tả |   Trường này có giá trị mặc định là **Dựa trên số lượng**.| Không có |
| Phương thức thanh toán | Đây là bộ tùy chọn đại diện cho hai mô hình hợp đồng chính được Project Operations hỗ trợ: **Giá cố định** và **Thời gian và Vật liệu**. | Dựa trên phương thức thanh toán đã chọn, một lịch biểu hóa đơn dựa trên mốc thời gian được cung cấp cho các mô tả hợp đồng phụ với phương thức thanh toán Giá cố định. |
| Lớp giao dịch | Giá trị mặc định là **Thời gian**. | Điều này cho thấy rằng mô tả hợp đồng phụ đang được sử dụng để ghi lại việc mua thời gian của nhà thầu phụ. |
| Vai trò | Chọn vai trò của các nguồn lực hợp đồng phụ có thời gian được mua. | Vai trò được thực hiện bởi các nguồn lực của hợp đồng phụ xác định chi phí mua hàng. |
| Ngày bắt đầu được yêu cầu | Nhập ngày mà các nguồn lực của nhà thầu phụ được yêu cầu để bắt đầu hoạt động. | Điều này được sử dụng để chọn một bảng giá dự án từ các bảng giá dự án kèm theo hợp đồng phụ. Chi phí của vai trò trên mô tả thầu phụ lấy từ bảng giá đó. |
| Ngày kết thúc được yêu cầu | Nhập ngày kết thúc phân công nguồn lực của nhà thầu phụ. | Điều này sẽ được sử dụng để hiển thị các cảnh báo khi người quản lý dự án rút ra từ khả năng cho các yêu cầu nguồn lực xảy ra sau ngày này. |
| Số lượng đã đặt hàng | Nhập số giờ của vai trò được mua từ nhà cung cấp. | Điều này sẽ được sử dụng để hiển thị cảnh báo khi một người quản lý dự án đang sử dụng quá mức năng lực này cho các yêu cầu nguồn lực. |
| nhóm đơn vị đo | Giá trị mặc định là **Nhóm đơn vị đo thời gian**, không thể thay đổi. | Không có|
| Đơn vị | Giá trị mặc định cho trường này là đơn vị giờ cơ bản từ **Nhóm đơn vị đo thời gian**. Bạn có thể thay đổi giá trị này để mua bất kỳ đơn vị nào trong **Nhóm đơn vị đo thời gian**, chẳng hạn như ngày hoặc tuần. | Sự kết hợp của **Vai trò** và **Đơn vị** sẽ được sử dụng làm mặc định hoặc được tính cho đơn giá cho mô tả hợp đồng phụ. |
| Đơn giá | Đơn giá mặc định sử dụng kết hợp **Vai trò** và **Đơn vị** từ bảng giá dự án áp dụng cho ngày **Bắt đầu được yêu cầu** của mô tả hợp đồng phụ. | Khi bảng giá dự án áp dụng có giá được lập theo đơn vị khác với đơn vị trên mô tả hợp đồng phụ, hệ thống sẽ sử dụng quy đổi đơn vị để tính theo đơn giá. |
| Tổng con |    Đây là trường chỉ đọc được tính là Số lượng x Đơn giá, nếu cả giá trị số lượng và đơn giá đều được nhập. Nếu một trong hai hoặc cả hai trường số lượng, đơn giá đều trống, thì bạn có thể nhập giá trị vào trường này. | Không có|
| Thuế doanh thu |   Nhập số tiền thuế bán hàng. |Không có |
| Tổng số tiền | Tổng số tiền của mô tả hợp đồng phụ bao gồm thuế. Trường này được tính là Tổng phụ + Thuế bán hàng.|Không có |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
