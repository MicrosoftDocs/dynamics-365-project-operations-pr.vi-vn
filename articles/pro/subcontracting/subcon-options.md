---
title: Tùy chọn hợp đồng phụ cho thành viên nhóm dự án
description: Bài viết này giải thích các tùy chọn hợp đồng phụ cho các thành viên nhóm dự án trong Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 046b5d38ef7e433d02e3eac2e858a3333e941c45
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522305"
---
# <a name="subcontracting-options-for-project-team-members"></a>Tùy chọn hợp đồng phụ cho thành viên nhóm dự án

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Trong Microsoft Dynamics 365 Project Operations, bạn có thể đánh giá các tùy chọn hợp đồng phụ có sẵn cho một hoặc nhiều thành viên nhóm dự án. Các tùy chọn hợp đồng phụ có sẵn cho phép bạn:

- Tạo một hợp đồng phụ mới và/hoặc tạo các mô tả mới trên một hợp đồng phụ hiện có cho các thành viên nhóm dự án đã chọn. 
- Đặt trước một hợp đồng phụ và mô tả hợp đồng phụ hiện có. 

Bạn có thể chọn từ các tùy chọn hợp đồng phụ có sẵn cho các thành viên nhóm dự án chung hoặc chọn từ các thành viên nhóm dự án đã được bố trí nguồn lực có tên là nhân viên hợp đồng. 

Không có tùy chọn hợp đồng phụ cho những trường hợp sau:

- Các thành viên nhóm dự án đã được bố trí một nhân viên. 
- Các thành viên nhóm dự án đã được liên kết với một hợp đồng phụ và mô tả hợp đồng phụ. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Thực hiện hợp đồng phụ cho thành viên nhóm dự án chưa được bố trí

Để xem xét và chọn từ các tùy chọn hợp đồng phụ có sẵn cho thành viên nhóm dự án chung hoặc chưa được bố trí, hãy làm theo các bước sau:

1. Chọn một hoặc nhiều bản ghi thành viên nhóm dự án trong đó nguồn lực là nguồn lực chung.
2. Đảm bảo rằng không có bản ghi thành viên nhóm dự án nào được chọn đã có hợp đồng phụ. 
3. Chọn **Tùy chọn hợp đồng phụ** trên lưới phụ thành viên nhóm dự án. Hộp thoại **Tùy chọn hợp đồng phụ** sẽ mở. 
4. Nếu bạn chỉ chọn một bản ghi thành viên nhóm dự án ở bước 1, thì các tùy chọn sau sẽ khả dụng:
    - Tạo mô tả hợp đồng phụ mới. 
    - Đặt trước hợp đồng phụ hiện có Nếu bạn đã chọn nhiều bản ghi thành viên nhóm dự án ở bước 1, thì tùy chọn duy nhất có sẵn là tạo một mô tả hợp đồng phụ mới.
5. Tùy chọn đặt trước mô tả hợp đồng phụ hiện có cho phép bạn chọn một hợp đồng phụ và mô tả hợp đồng phụ mà bạn muốn đặt trước. Khi chọn mô tả hợp đồng phụ để dự trữ năng lực, bạn nên đảm bảo rằng mô tả hợp đồng phụ được chọn dành cho thời gian và vai trò cần thiết của thành viên nhóm dự án khớp với vai trò đã được mua trên mô tả hợp đồng phụ.
6. Khi bạn chọn tạo các mô tả hợp đồng phụ mới cho các thành viên nhóm dự án, hệ thống sẽ cho phép bạn chọn hợp đồng phụ mà bạn muốn tạo các mô tả này. Hợp đồng phụ mà bạn chọn để tạo các mô tả mới phải nằm trong trạng thái **Bản nháp**. Với tùy chọn này để tạo các mô tả hợp đồng phụ mới cho các thành viên nhóm dự án đã chọn, hệ thống sẽ tạo một mô tả hợp đồng phụ theo thời gian cho mỗi thành viên nhóm dự án. Vai trò, giờ và ngày sẽ được sao chép từ thành viên nhóm dự án vào từng mô tả hợp đồng phụ được tạo. 
7. Khi một thành viên nhóm chung được liên kết với hợp đồng phụ và mô tả hợp đồng phụ, trường **Loại nhân viên** trên hàng thành viên nhóm chung sẽ được cập nhật thành **Nhân viên hợp đồng** và giá trị **Hiệu lực hợp đồng phụ** sẽ được đặt thành **Có hiệu lực**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Thực hiện hợp đồng phụ cho thành viên nhóm dự án có biên chế

Giống như các thành viên nhóm chung hoặc chưa được bố trí, bạn cũng có thể xem các tùy chọn hợp đồng phụ cho một thành viên nhóm dự án đã bố trí miễn là thành viên nhóm được bố trí đó là nhân viên hợp đồng. Để xem xét và chọn từ các tùy chọn hợp đồng phụ có sẵn cho thành viên nhóm dự án đã bố trí hoặc có tên, hãy làm theo các bước sau:

1. Chọn một hoặc nhiều bản ghi thành viên nhóm dự án trong đó nguồn lực là nhân viên hợp đồng có tên.
2. Đảm bảo rằng không có bản ghi thành viên nhóm dự án nào đã chọn đang có hợp đồng phụ. 
3. Chọn **Tùy chọn hợp đồng phụ** trên lưới phụ thành viên nhóm dự án. Hộp thoại **Tùy chọn hợp đồng phụ** sẽ mở. 
4. Nếu bạn chỉ chọn một bản ghi thành viên nhóm dự án ở bước 1, thì các tùy chọn sau sẽ khả dụng:
      - Tạo mô tả hợp đồng phụ mới.
      - Đặt trước một hợp đồng phụ hiện có.
  Nếu bạn đã chọn nhiều bản ghi thành viên nhóm dự án ở bước 1, thì tùy chọn duy nhất có sẵn là tạo một mô tả hợp đồng phụ mới.
5. Tùy chọn đặt trước mô tả hợp đồng phụ hiện có cho phép bạn chọn một hợp đồng phụ và mô tả hợp đồng phụ mà bạn muốn đặt trước. Khi chọn mô tả hợp đồng phụ để dự phòng năng lực, bạn nên đảm bảo những điều sau:
      - Mô tả hợp đồng phụ được chọn là dành cho thời gian. 
      - Vai trò được yêu cầu đối với thành viên nhóm dự án khớp với vai trò đã được mua trên mô tả hợp đồng phụ. 
      - Nhà cung cấp mà nhân viên hợp đồng được liên kết giống với nhà cung cấp trên hợp đồng phụ.
6. Khi bạn chọn tạo các mô tả hợp đồng phụ mới cho các thành viên nhóm dự án, hệ thống sẽ cho phép bạn chọn hợp đồng phụ mà bạn muốn tạo các mô tả này. Với tùy chọn này, bạn phải đảm bảo nhà cung cấp của nhân viên hợp đồng giống với nhà cung cấp trên hợp đồng phụ này. 
7. Hợp đồng phụ mà bạn chọn để tạo các mô tả mới phải nằm trong trạng thái **Bản nháp**. Với tùy chọn này để tạo các mô tả hợp đồng phụ mới cho các thành viên nhóm dự án đã chọn, hệ thống sẽ tạo một mô tả hợp đồng phụ theo thời gian cho mỗi thành viên nhóm dự án. Vai trò, giờ và ngày sẽ được sao chép từ thành viên nhóm dự án vào từng mô tả hợp đồng phụ được tạo.  
8. Khi một thành viên nhóm có tên được liên kết với hợp đồng phụ và mô tả hợp đồng phụ, trường **Loại nhân viên** trên hàng thành viên nhóm có tên sẽ được cập nhật thành **Nhân viên hợp đồng** và giá trị **Hiệu lực hợp đồng phụ** sẽ được đặt thành **Có hiệu lực**.

## <a name="re-costing-subcontractor-assignments"></a>Định giá lại phân công nhà thầu phụ

Khi một thành viên nhóm dự án (chung hoặc có tên) được liên kết với mô tả hợp đồng phụ bằng cách sử dụng hộp thoại **Tùy chọn hợp đồng phụ**, bất kỳ sự phân công nhiệm vụ nào mà thành viên nhóm thực hiện sẽ được định giá lại dựa trên bảng giá mua kèm theo hợp đồng phụ. Trên tab **Ước tính** trên trang **Chi tiết dự án**, chọn **Cập nhật giá** để xem giá cập nhật và/hoặc chi phí do quyết định thực hiện hợp đồng phụ.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
