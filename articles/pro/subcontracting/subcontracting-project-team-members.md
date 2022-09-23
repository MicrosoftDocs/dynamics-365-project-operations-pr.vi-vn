---
title: Thành viên nhóm dự án hợp đồng phụ
description: Bài viết này giải thích cách ký hợp đồng phụ với các thành viên nhóm dự án trong Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 9/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a2f17d6f270029e3a517e99c7bb518cdb19b8d23
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522822"
---
# <a name="subcontracting-project-team-members"></a>Thành viên nhóm dự án hợp đồng phụ

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Trong Microsoft Dynamics 365 Project Operations, bạn có thể chọn hợp đồng phụ với các thành viên trong nhóm dự án không có biên chế hoặc có nhân viên.

- Các thành viên trong nhóm dự án chưa được phân bổ có một nguồn lực chung được chỉ định.
- Các thành viên trong nhóm có nhân viên được chỉ định một tài nguyên được đặt tên.

Khi bạn liên kết một thành viên trong nhóm dự án với một dòng hợp đồng phụ, bất kỳ nhiệm vụ nào cho các nhiệm vụ mà thành viên trong nhóm có sẽ được hoàn thành dựa trên bảng giá mua kèm theo hợp đồng phụ.  Trên **Ước tính** tab trên **Chi tiết dự án** trang, chọn **Cập nhật giá** để xem giá cập nhật và / hoặc chi phí do quyết định ký hợp đồng phụ. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Hợp đồng phụ với một thành viên trong nhóm dự án không được quản lý
Các **Thông tin chi tiết về thành viên trong nhóm** trang có các trường dòng hợp đồng phụ và hợp đồng phụ cho phép người quản lý dự án thể hiện cách họ muốn thu hút năng lực cần thiết từ hợp đồng phụ. Để ký hợp đồng phụ với một thành viên trong nhóm dự án làm tài nguyên chung, hãy làm theo các bước sau:

1.  Chọn một hợp đồng phụ trên **Chi tiết thành viên nhóm** trang.

2.  Bạn chỉ có thể chọn các hợp đồng phụ với **Bản thảo** hoặc **Đã xác nhận** trạng thái. **Đã đóng cửa** hoặc **Đã hủy** hợp đồng phụ không thể được chọn. 

3.  Các **Dòng hợp đồng phụ** trường sẽ hiển thị sau khi bạn chọn hợp đồng phụ.

4.  Bên trong **Dòng hợp đồng phụ**, bạn chỉ có thể chọn các dòng hợp đồng phụ dành cho thời gian. Bạn không thể chọn dòng hợp đồng phụ cho chi phí hoặc vật liệu.

5.  Vai trò đối với hồ sơ thành viên nhóm dự án cần khớp với vai trò trên dòng hợp đồng phụ. Điều này đảm bảo rằng thời gian cho vai trò đang được ước tính trong dự án là vai trò được mua trên dây chuyền hợp đồng phụ. 

Khi một thành viên trong nhóm chung được liên kết với hợp đồng phụ và dòng hợp đồng phụ, **Loại công nhân** trường trên hàng thành viên nhóm chung sẽ được cập nhật thành **Nhân viên hợp đồng** và **Hiệu lực hợp đồng phụ** sẽ được đặt thành **Có giá trị**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Hợp đồng phụ với một thành viên trong nhóm dự án có nhân sự
Giống như các thành viên trong nhóm chung chung hoặc không bị phân bổ, năng lực của các thành viên trong nhóm có nhân sự cần thiết trong một dự án cũng có thể được liên kết với một hợp đồng phụ. Để ký hợp đồng phụ với một thành viên nhóm dự án có tên, hãy làm theo các bước sau:

1.  Đảm bảo rằng tài nguyên được đặt tên được thiết lập như một loại tài nguyên có thể đặt trước của nhân viên hợp đồng. Ngoài ra, hãy đảm bảo rằng **Người bán** trường trên tài nguyên có thể đặt trước khớp với nhà cung cấp trên hợp đồng phụ mà bạn đang chọn. 

2.  Bạn chỉ có thể chọn các hợp đồng phụ trong **Bản thảo** hoặc **Đã xác nhận** trạng thái. **Đã đóng cửa** hoặc **Đã hủy** hợp đồng phụ không thể được chọn. 

3.  Các **Dòng hợp đồng phụ** trường sẽ hiển thị sau khi bạn chọn hợp đồng phụ.

4.  Bên trong **Dòng hợp đồng phụ**, bạn chỉ có thể chọn các dòng hợp đồng phụ dành cho thời gian. Bạn không thể chọn dòng hợp đồng phụ cho chi phí hoặc vật liệu.

5.  Vai trò đối với hồ sơ thành viên nhóm dự án cần khớp với vai trò trên dòng hợp đồng phụ. Điều này đảm bảo rằng thời gian cho vai trò đang được ước tính trong dự án là vai trò được mua trên dây chuyền hợp đồng phụ. 

Các thành viên nhóm dự án được đặt tên được thiết lập như một loại nhân viên hợp đồng của **Tài nguyên có thể đặt trước** sẽ được hiển thị với trạng thái hiệu lực của hợp đồng phụ là **Không hợp lệ** nếu chúng không được liên kết với một hợp đồng phụ. Khi một thành viên trong nhóm dự án có tên được liên kết với hợp đồng phụ và dòng hợp đồng phụ, **Loại công nhân** trường trong hàng thành viên trong nhóm sẽ cập nhật thành **Nhân viên hợp đồng** và **Hiệu lực hợp đồng phụ** sẽ được đặt thành **Có giá trị**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
