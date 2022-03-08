---
title: Sao chép dự án
description: Chủ đề này cung cấp thông tin về việc sao chép dự án trong Dynamics 365 Project Operations.
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fe76f59b315fd0f46b25e1d116acde1f6b2864d1753e01d6311ea93ae7d116fc
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007217"
---
# <a name="copy-a-project"></a>Sao chép dự án

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Với Dynamics 365 Project Operations, bạn có thể nhanh chóng tạo các dự án mới bằng cách chọn **Sao chép dự án** trên biểu mẫu **Dự án**. Để sao chép dự án, hãy mở dự án mà bạn muốn sao chép, rồi chọn **Sao chép dự án**. Hành động này sẽ sao chép:

- Thuộc tính dự án 
- Cấu trúc phân tích công việc
- Thành viên nhóm dự án
- Ước tính dự án
- Ước tính chi phí dự án
- Ước tính vật tư của dự án

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
- Nhận xét
- Ước tính
- Ngày bắt đầu ước tính: Đây là ngày tạo dự án từ bản sao.
- Ngày kết thúc ước tính: Ngày này được điều chỉnh dựa trên ngày bắt đầu của dự án mới được tạo từ bản sao.
- Nỗ lực (giờ)
- Chi phí nhân công ước tính
- Chi phí phí tổn ước tính
- Chi phí ước tính của vật liệu

> [!NOTE]
> Thao tác sao chép dự án sẽ tốn nhiều thời gian. Bản ghi dự án, các thuộc tính tương ứng và nhiều thực thể liên quan cũng được sao chép. Do thao tác này sẽ kéo dài, nên sau khi quá trình sao chép bắt đầu, trang dự án đích sẽ bị khóa chức năng chỉnh sửa cho đến khi thao tác sao chép hoàn tất.

## <a name="work-breakdown-structure"></a>Cấu trúc phân tích công việc

Khi dự án được sao chép, toàn bộ cấu trúc phân tích công việc đã tải nguồn lực sẽ được sao chép. Nguồn lực có tên được thay thế bằng nguồn lực chung. Nếu nguồn lực tên không có cùng giờ làm việc với nguồn lực chung, lịch trình sẽ được tính toán lại và thời lượng tác vụ có thể thay đổi.

## <a name="project-team-members"></a>Thành viên nhóm dự án

Khi một nhóm dự án được sao chép từ dự án nguồn, các tài nguyên chung sẽ được sao chép. Việc phân công nguồn lực chung cũng được duy trì như khi chúng ở trong dự án nguồn. Các nguồn lực có tên sẽ được chuyển đổi thành các thành viên nhóm chung.

## <a name="estimates"></a>Ước tính

Khi dự án được sao chép, các dòng ước tính tài nguyên, chi phí và vật tư được sao chép từ dự án nguồn. 

Để biết thông tin về cách truy nhập Sao chép dự án theo lập trình, hãy xem [Phát triển các mẫu dự án với Sao chép dự án](dev-copy-project.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
