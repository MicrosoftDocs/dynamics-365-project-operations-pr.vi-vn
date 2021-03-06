---
title: Sao chép dự án
description: Chủ đề này cung cấp thông tin về cách sao chép dự án trong Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e35dc725e7938e9f59f7151dd1b37500fabf77a4
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908737"
---
# <a name="copy-a-project"></a>Sao chép dự án

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Với Dynamics 365 Project Operations, bạn có thể nhanh chóng xây dựng các dự án mới bằng cách sử dụng thao tác **Sao chép dự án** trên biểu mẫu **Dự án**. Để sao chép dự án, hãy chọn một dự án, sau đó chọn **Sao chép**. Hành động sẽ sao chép:

- Thuộc tính dự án
- Cấu trúc phân tích công việc
- Thành viên nhóm dự án
- Ước tính dự án
- Ước tính chi phí dự án

## <a name="project-properties"></a>Thuộc tính dự án

Khi dự án được sao chép, các giá trị trong các trường sau sẽ được sao chép:

- Tên
- Nội dung mô tả
- Khách hàng
- Mẫu lịch
- Tiền tệ
- Đơn vị Hợp đồng
- Trình quản lý Dự án
- Trạng thái
- Trạng thái của Dự án Tổng thể
- Bình luận
- Ước tính
- Ngày Bắt đầu Ước tính
- Ngày hoàn thành
- Nỗ lực (giờ)
- Chi phí nhân công ước tính
- Chi phí Phí tổn Ước tính

## <a name="work-breakdown-structure"></a>Cấu trúc phân tích công việc

Khi dự án được sao chép, toàn bộ cấu trúc phân tích công việc đã tải nguồn lực sẽ được sao chép. Nguồn lực có tên được thay thế bằng nguồn lực chung. Nếu nguồn lực tên không có cùng giờ làm việc với nguồn lực chung, lịch trình sẽ được tính toán lại và thời lượng tác vụ có thể thay đổi.

## <a name="project-team-members"></a>Thành viên nhóm dự án

Khi một nhóm dự án được sao chép từ dự án nguồn, các tài nguyên chung sẽ được sao chép. Việc phân công nguồn lực chung cũng được duy trì như khi chúng ở trong dự án nguồn. Các nguồn lực có tên sẽ được chuyển đổi thành các thành viên nhóm chung.

## <a name="estimates"></a>Ước tính

Khi dự án được sao chép, cả dòng ước tính nguồn lực và chi phí đều được sao chép từ dự án nguồn.