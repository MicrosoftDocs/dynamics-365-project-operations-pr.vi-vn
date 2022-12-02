---
title: Thành viên nhóm dự án hợp đồng phụ
description: Bài viết này giải thích cách thực hiện hợp đồng phụ cho các thành viên nhóm dự án trong Microsoft Dynamics 365 Project Operations.
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

Trong Microsoft Dynamics 365 Project Operations, bạn có thể chọn thực hiện hợp đồng phụ với các thành viên nhóm dự án chưa được bố trí hoặc có biên chế.

- Các thành viên nhóm dự án chưa được bố trí sẽ được phân công nguồn lực chung.
- Các thành viên nhóm biên chế được phân công nguồn lực có tên.

Khi bạn liên kết một thành viên nhóm dự án với một mô tả hợp đồng phụ, bất kỳ phân công nào cho các nhiệm vụ mà thành viên nhóm có sẽ được tính phí lại dựa trên bảng giá đính kèm với hợp đồng phụ.  Trên tab **Ước tính** trên trang **Chi tiết dự án**, chọn **Cập nhật giá** để xem giá cập nhật và/hoặc chi phí do quyết định thực hiện hợp đồng phụ. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Thực hiện hợp đồng phụ cho thành viên nhóm dự án chưa được bố trí
Trang **Chi tiết thành viên nhóm** có các trường mô tả hợp đồng phụ và hợp đồng phụ cho phép người quản lý dự án thể hiện cách họ muốn thu hút năng lực cần thiết từ hợp đồng phụ. Để thực hiện hợp đồng phụ với một thành viên nhóm dự án làm nguồn lực chung, hãy làm theo các bước sau:

1.  Chọn một hợp đồng phụ trên trang **Chi tiết thành viên nhóm**.

2.  Bạn chỉ có thể chọn hợp đồng phụ với trạng thái **Bản nháp** hoặc **Đã xác nhận**. Bạn không thể chọn các hợp đồng phụ **Đã đóng** hoặc **Đã hủy**. 

3.  Trường **Mô tả hợp đồng phụ** sẽ hiển thị sau khi bạn chọn hợp đồng phụ.

4.  Trong trường **Mô tả hợp đồng phụ**, bạn chỉ có thể chọn các mô tả hợp đồng phụ dành cho thời gian. Bạn không thể chọn mô tả hợp đồng phụ cho chi phí hoặc vật tư.

5.  Vai trò đối với bản ghi thành viên nhóm dự án cần khớp với vai trò trên mô tả hợp đồng phụ. Điều này đảm bảo rằng thời gian cho vai trò đang được ước tính trong dự án là vai trò được mua trên mô tả hợp đồng phụ. 

Khi một thành viên nhóm chung được liên kết với hợp đồng phụ và mô tả hợp đồng phụ, trường **Loại nhân viên** trên hàng thành viên nhóm chung sẽ được cập nhật thành **Nhân viên hợp đồng** và giá trị **Hiệu lực hợp đồng phụ** sẽ được đặt thành **Có hiệu lực**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Thực hiện hợp đồng phụ cho thành viên nhóm dự án có biên chế
Giống như các thành viên nhóm chung hoặc chưa được bố trí, năng lực của thành viên nhóm biên chế cần thiết trong một dự án cũng có thể được liên kết với một hợp đồng phụ. Để thực hiện hợp đồng phụ với một thành viên nhóm dự án có tên, hãy làm theo các bước sau:

1.  Đảm bảo rằng nguồn lực có tên được thiết lập dưới dạng loại nhân viên hợp đồng của nguồn lực có thể đặt. Ngoài ra, hãy đảm bảo rằng trường **Nhà cung cấp** trên nguồn lực có thể đặt trước khớp với nhà cung cấp trên hợp đồng phụ mà bạn đang chọn. 

2.  Bạn chỉ có thể chọn hợp đồng phụ ở trạng thái **Bản nháp** hoặc **Đã xác nhận**. Bạn không thể chọn các hợp đồng phụ **Đã đóng** hoặc **Đã hủy**. 

3.  Trường **Mô tả hợp đồng phụ** sẽ hiển thị sau khi bạn chọn hợp đồng phụ.

4.  Trong trường **Mô tả hợp đồng phụ**, bạn chỉ có thể chọn các mô tả hợp đồng phụ dành cho thời gian. Bạn không thể chọn mô tả hợp đồng phụ cho chi phí hoặc vật tư.

5.  Vai trò đối với bản ghi thành viên nhóm dự án cần khớp với vai trò trên mô tả hợp đồng phụ. Điều này đảm bảo rằng thời gian cho vai trò đang được ước tính trong dự án là vai trò được mua trên mô tả hợp đồng phụ. 

Các thành viên nhóm dự án có tên được thiết lập như một loại nhân viên hợp đồng **Nguồn lực có thể đặt** sẽ được hiển thị với trạng thái hiệu lực của hợp đồng phụ là **Không hợp lệ** nếu chúng không được liên kết với một hợp đồng phụ. Khi một thành viên nhóm dự án có tên được liên kết với hợp đồng phụ và mô tả hợp đồng phụ, trường **Loại nhân viên** trong hàng thành viên nhóm chung sẽ cập nhật thành **Nhân viên hợp đồng** và giá trị **Hiệu lực hợp đồng phụ** sẽ được đặt thành **Có hiệu lực**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
