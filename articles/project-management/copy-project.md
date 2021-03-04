---
title: Sao chép dự án
description: Chủ đề này cung cấp thông tin về cách sao chép dự án trong Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 53c72e5fd680eb28128644788752368705440445
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131819"
---
# <a name="copy-a-project"></a>Sao chép dự án

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Với Dynamics 365 Project Operations, bạn có thể nhanh chóng xây dựng các dự án mới bằng cách chọn **Sao chép dự án** trên biểu mẫu **Dự án**. Để sao chép dự án, hãy mở dự án mà bạn muốn sao chép, rồi chọn **Sao chép dự án**. Hành động sẽ sao chép:

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

Để biết thông tin về cách truy nhập Sao chép dự án theo lập trình, hãy xem [Phát triển các mẫu dự án với Sao chép dự án](dev-copy-project.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]