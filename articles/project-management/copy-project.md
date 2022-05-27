---
title: Sao chép dự án
description: Chủ đề này cung cấp thông tin về việc sao chép dự án trong Dynamics 365 Project Operations.
author: ruhercul
ms.date: 03/07/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: e9b637d2d282d123dfacb8a295292ea06549aa1e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574456"
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
- Danh sách kiểm tra dự án
- Nhóm dự án

## <a name="project-properties"></a>Thuộc tính dự án

Khi dự án được sao chép, các giá trị trong các trường sau sẽ được sao chép.

| Trường | Hoạt động dự án Vật liệu không dự trữ | Project Operations Lite | Dự án cho Web |
|-------|------------------------------------------|-------------------------|---------------------|
| Tên | : heavy_check_mark: | : heavy_check_mark: | : heavy_check_mark: |
| Description | : heavy_check_mark: | : heavy_check_mark: | |
| Quý khách hàng | : heavy_check_mark: | : heavy_check_mark: | |
| Mẫu lịch | : heavy_check_mark: | : heavy_check_mark: | : heavy_check_mark: |
| Tiền tệ | : heavy_check_mark: | : heavy_check_mark: | |
| Đơn vị theo hợp đồng | : heavy_check_mark: | : heavy_check_mark: | |
| Công ty sở hữu | : heavy_check_mark: | | |
| Trình quản lý Dự án | : heavy_check_mark: | : heavy_check_mark: | : heavy_check_mark: |
| Trạng thái | : heavy_check_mark: | : heavy_check_mark: | |
| Trạng thái của Dự án Tổng thể | : heavy_check_mark: | : heavy_check_mark: | |
| Bình luận | : heavy_check_mark: | : heavy_check_mark: | |
| Ước tính | : heavy_check_mark: | : heavy_check_mark: | |
| <p>Ngày Bắt đầu Ước tính</p><p><strong>Ghi chú:</strong> Trường này chỉ định ngày dự án được tạo từ bản sao. | : heavy_check_mark: | : heavy_check_mark: | |
| <p>Ngày Kết thúc Ước tính</p><p><strong>Ghi chú:</strong> Ngày trong trường này được điều chỉnh dựa trên ngày bắt đầu của dự án mới được tạo từ bản sao.</p> | : heavy_check_mark: | : heavy_check_mark: | |
| Nỗ lực (giờ) | : heavy_check_mark: | : heavy_check_mark: | |
| Chi phí nhân công ước tính | : heavy_check_mark: | : heavy_check_mark: | |
| Chi phí phí tổn ước tính | : heavy_check_mark: | : heavy_check_mark: | |
| Chi phí ước tính của vật liệu | | : heavy_check_mark: | |

> [!NOTE]
> Thao tác sao chép dự án sẽ tốn nhiều thời gian. Bản ghi dự án, các thuộc tính tương ứng và nhiều thực thể liên quan cũng được sao chép. Do thao tác này sẽ kéo dài, nên sau khi quá trình sao chép bắt đầu, trang dự án đích sẽ bị khóa chức năng chỉnh sửa cho đến khi thao tác sao chép hoàn tất.

## <a name="work-breakdown-structure"></a>Cấu trúc phân tích công việc

Khi dự án được sao chép, toàn bộ cấu trúc phân tích công việc đã tải nguồn lực sẽ được sao chép. Nguồn lực có tên được thay thế bằng nguồn lực chung. Nếu tài nguyên được đặt tên không có cùng giờ làm việc với tài nguyên chung, lịch trình sẽ được tính toán lại và thời lượng tác vụ có thể thay đổi.

## <a name="project-team-members"></a>Thành viên nhóm dự án

Khi một nhóm dự án được sao chép từ dự án nguồn, các tài nguyên chung sẽ được sao chép. Việc phân công nguồn lực chung cũng được duy trì như khi chúng ở trong dự án nguồn. Các nguồn lực có tên sẽ được chuyển đổi thành các thành viên nhóm chung.

> [!NOTE]
> Các thành viên trong nhóm và nhiệm vụ không được sao chép trong Dự án cho Web.

## <a name="estimates"></a>Ước tính

Khi dự án được sao chép, các dòng ước tính tài nguyên, chi phí và vật tư được sao chép từ dự án nguồn. 

Để biết thông tin về cách truy nhập Sao chép dự án theo lập trình, hãy xem [Phát triển các mẫu dự án với Sao chép dự án](dev-copy-project.md).

## <a name="quotes-and-contracts"></a>Báo giá và hợp đồng

Báo giá và hợp đồng không được liên kết với dự án đích.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
