---
title: Tùy chọn hợp đồng phụ cho thành viên nhóm dự án
description: Bài viết này giải thích các tùy chọn hợp đồng phụ cho các thành viên nhóm dự án trong Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 5e0955d58365a4ecbe1c053882736f196758816e
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261633"
---
# <a name="subcontracting-options-for-project-team-members"></a>Tùy chọn hợp đồng phụ cho thành viên nhóm dự án

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Trong Microsoft Dynamics 365 Project Operations, bạn có thể đánh giá các tùy chọn hợp đồng phụ có sẵn cho một hoặc nhiều thành viên trong nhóm dự án. Các tùy chọn hợp đồng phụ có sẵn cho phép bạn:

- Tạo một hợp đồng phụ mới và / hoặc tạo các dòng mới trên một hợp đồng phụ hiện có cho các thành viên nhóm dự án đã chọn. 
- Đặt trước hợp đồng phụ và hợp đồng phụ đã tồn tại. 

Bạn có thể chọn từ các tùy chọn hợp đồng phụ có sẵn cho các thành viên nhóm dự án chung hoặc chọn từ các thành viên nhóm dự án đã được biên chế với nguồn lực được đặt tên là nhân viên hợp đồng. 

Không có tùy chọn hợp đồng phụ nào có sẵn cho những điều sau:

- Các thành viên trong nhóm dự án đã được biên chế với một nhân viên. 
- Các thành viên trong nhóm dự án đã được liên kết với hợp đồng phụ và hợp đồng phụ. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Hợp đồng phụ với một thành viên trong nhóm dự án không được quản lý

Để xem xét và chọn từ các tùy chọn hợp đồng phụ có sẵn cho một thành viên nhóm dự án chung hoặc không bị phân bổ, hãy làm theo các bước sau:

1. Chọn một hoặc nhiều bản ghi thành viên nhóm dự án trong đó tài nguyên là tài nguyên chung.
2. Đảm bảo rằng không có hồ sơ thành viên nhóm dự án nào được chọn đã được ký hợp đồng phụ. 
3. Lựa chọn **Tùy chọn hợp đồng phụ** trên lưới phụ thành viên nhóm dự án. Các **Tùy chọn hợp đồng phụ** hộp thoại mở ra. 
4. Nếu bạn chỉ chọn một bản ghi thành viên nhóm dự án ở bước 1, thì các tùy chọn sau sẽ khả dụng:
    - Tạo các dòng hợp đồng phụ mới. 
    - Dự phòng trước hợp đồng phụ hiện có Nếu bạn đã chọn nhiều bản ghi thành viên nhóm dự án ở bước 1, thì tùy chọn duy nhất có sẵn là tạo một dòng hợp đồng phụ mới.
5. Tùy chọn đặt trước đối với dòng hợp đồng phụ hiện có cho phép bạn chọn một hợp đồng phụ và dòng hợp đồng phụ mà bạn muốn đặt trước. Khi chọn dòng hợp đồng phụ để dự trữ năng lực, bạn nên đảm bảo rằng dòng hợp đồng phụ được chọn là phù hợp với thời gian và vai trò cần thiết của thành viên nhóm dự án phù hợp với vai trò đã được mua trên dòng hợp đồng phụ.
6. Khi bạn chọn tạo các dòng hợp đồng phụ mới cho các thành viên trong nhóm dự án, hệ thống sẽ cho phép bạn chọn hợp đồng phụ mà bạn muốn tạo các dòng này. Hợp đồng phụ mà bạn chọn để tạo các dòng mới phải nằm trong **Bản thảo** trạng thái. Với tùy chọn này để tạo các dòng hợp đồng phụ mới cho các thành viên trong nhóm dự án đã chọn, hệ thống sẽ tạo một dòng hợp đồng phụ theo thời gian cho mỗi thành viên trong nhóm dự án. Vai trò, giờ và ngày tháng sẽ được sao chép từ thành viên nhóm dự án vào từng dòng hợp đồng phụ được tạo. 
7. Khi một thành viên trong nhóm chung được liên kết với hợp đồng phụ và dòng hợp đồng phụ, **Loại công nhân** trường trên hàng thành viên nhóm chung sẽ được cập nhật thành **Nhân viên hợp đồng** và **Hiệu lực hợp đồng phụ** giá trị sẽ được đặt thành **Có giá trị**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Hợp đồng phụ với một thành viên trong nhóm dự án có nhân sự

Giống như các thành viên trong nhóm chung chung hoặc không bị phân bổ, bạn cũng có thể xem các tùy chọn hợp đồng phụ cho một thành viên trong nhóm dự án có nhân viên miễn là thành viên được nhân viên đó là nhân viên hợp đồng. Để xem xét và chọn từ các tùy chọn hợp đồng phụ có sẵn cho một thành viên trong nhóm dự án có nhân viên hoặc có tên, hãy làm theo các bước sau:

1. Chọn một hoặc nhiều bản ghi thành viên nhóm dự án trong đó tài nguyên là nhân viên hợp đồng được đặt tên.
2. Đảm bảo rằng không có hồ sơ thành viên nhóm dự án nào được chọn đã được ký hợp đồng phụ. 
3. Lựa chọn **Tùy chọn hợp đồng phụ** trên lưới phụ thành viên nhóm dự án. Các **Tùy chọn hợp đồng phụ** hộp thoại mở ra. 
4. Nếu bạn chỉ chọn một bản ghi thành viên nhóm dự án ở bước 1, thì các tùy chọn sau sẽ khả dụng:
      - Tạo các dòng hợp đồng phụ mới.
      - Bảo lưu trước một hợp đồng phụ hiện có.
  Nếu bạn đã chọn nhiều bản ghi thành viên nhóm dự án ở bước 1, thì tùy chọn duy nhất có sẵn là tạo một dòng hợp đồng phụ mới.
5. Tùy chọn đặt trước đối với dòng hợp đồng phụ hiện có cho phép bạn chọn một hợp đồng phụ và dòng hợp đồng phụ mà bạn muốn đặt trước. Khi chọn dây chuyền thầu phụ để dự phòng công suất, bạn nên đảm bảo những điều sau:
      - Dòng hợp đồng phụ được chọn là dành cho thời gian. 
      - Vai trò được yêu cầu đối với thành viên nhóm dự án phù hợp với vai trò đã được mua trên dây chuyền hợp đồng phụ. 
      - Nhà cung cấp mà nhân viên hợp đồng được liên kết giống với nhà cung cấp trên hợp đồng phụ.
6. Khi bạn chọn tạo các dòng hợp đồng phụ mới cho các thành viên trong nhóm dự án, hệ thống sẽ cho phép bạn chọn hợp đồng phụ mà bạn muốn tạo các dòng này. Với tùy chọn này, bạn nên đảm bảo rằng nhà cung cấp mà nhân viên hợp đồng thuộc về giống với nhà cung cấp trên hợp đồng phụ. 
7. Hợp đồng phụ mà bạn chọn để tạo các dòng mới phải nằm trong **Bản thảo** trạng thái. Với tùy chọn này để tạo các dòng hợp đồng phụ mới cho các thành viên trong nhóm dự án đã chọn, hệ thống sẽ tạo một dòng hợp đồng phụ theo thời gian cho mỗi thành viên trong nhóm dự án. Vai trò, giờ và ngày tháng sẽ được sao chép từ thành viên nhóm dự án vào từng dòng hợp đồng phụ được tạo.  
8. Khi một thành viên trong nhóm có tên được liên kết với hợp đồng phụ và dòng hợp đồng phụ, **Loại công nhân** trường trên hàng thành viên nhóm đã đặt tên sẽ được cập nhật thành **Nhân viên hợp đồng** và **Hiệu lực hợp đồng phụ** giá trị sẽ được đặt thành **Có giá trị**.

## <a name="re-costing-subcontractor-assignments"></a>Định giá lại các nhiệm vụ nhà thầu phụ

Khi một thành viên trong nhóm dự án (chung chung hoặc có tên) được liên kết với các dòng hợp đồng phụ bằng cách sử dụng **Tùy chọn hợp đồng phụ** hộp thoại, bất kỳ sự phân công nhiệm vụ nào mà thành viên trong nhóm thực hiện sẽ được định giá lại dựa trên bảng giá mua kèm theo hợp đồng phụ. Trên **Ước tính** tab trên **Chi tiết dự án** trang, chọn **Cập nhật giá** để xem giá cập nhật và / hoặc chi phí do quyết định ký hợp đồng phụ.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
