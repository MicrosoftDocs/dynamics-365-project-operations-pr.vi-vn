---
title: Thiết lập danh mục chi phí
description: Chủ đề này cung cấp thông tin về cách thiết lập danh mục chi phí và danh mục chia sẻ cho báo cáo chi phí.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: f051d70f3dfe3b241dc0a206c0cdfda000f87c76
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896712"
---
# <a name="set-up-expense-categories"></a>Thiết lập danh mục chi phí

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Khi nhân viên tạo báo cáo chi phí, mỗi khoản chi phí mà họ ghi lại phải được liên kết với một loại chi phí. Các danh mục chi phí có nguồn gốc từ các danh mục dùng chung có thể được chia sẻ giữa các pháp nhân trong tổ chức của bạn. Tùy thuộc vào cách tổ chức của bạn được xác định, các danh mục chi phí này cũng có thể được dùng chung trong các lĩnh vực khác. Dựa trên định nghĩa về tổ chức của bạn và hướng dẫn từ nhóm thực hiện, bạn phải xác định xem các danh mục được sử dụng trong quản lý Chi phí sẽ chỉ được sử dụng trong quản lý Chi phí hay nên được dùng chung trong các lĩnh vực khác.

> [!NOTE]
> Các danh mục này có thể được chia sẻ giữa Quản lý dự án, kế toán và Quản lý chi phí, hoặc giữa Quản lý dự án, kế toán và Sản xuất. Tuy nhiên, Quản lý chi phí và Sản xuất không thể dùng chung các danh mục này.

Trước khi bạn có thể bắt đầu quá trình thiết lập, các quyết định sau phải được thực hiện cho từng loại chi phí:

- Thể loại chi phí là gì? Ví dụ bao gồm các danh mục cho chuyến bay, khách sạn hoặc số dặm.
- Danh mục chi phí cũng có thể được sử dụng trong Quản lý dự án và kế toán không? Nếu có thể, bạn cũng phải đưa ra các quyết định sau:

    - Tài khoản chi phí nào sẽ được sử dụng cho các khoản chi phí sau?

        - Chi phí
        - Phân bổ bảng lương
        - Giá trị chi phí WIP
        - Chi phí-mục
        - Mục giá trị chi phí WIP
        - Lỗ lũy kế
        - Lỗ lũy kế WIP

    - Tài khoản doanh thu sẽ được sử dụng cho những nguồn thu nào sau đây?

        - Doanh thu đã lập hóa đơn
        - Giá trị bán hàng – doanh thu tích lũy
        - Giá trị bán hàng WIP
        - Sản xuất – doanh thu tích lũy
        - Sản xuất WIP
        - Lợi nhuận – doanh thu tích lũy
        - WIP-lợi nhuận
        - Đăng ký – doanh thu tích lũy
        - Đăng ký –WIP

- Loại chi phí là gì?
- Phương thức thanh toán mặc định cho loại chi phí là gì?
- Các khoản chi trong danh mục chi phí có phải được chia thành từng khoản không?
- Tài khoản chính mặc định cho loại chi phí là gì?
- Nhóm thuế bán hàng mặc định cho danh mục chi phí là gì?
- Các phương thức thanh toán bổ sung có được phép cho loại chi phí không? Nếu có, đó là phương thức thanh toán bổ sung nào?
- Có danh mục phụ nào trong danh mục chi phí này không? Nếu có danh mục phụ, bạn cũng phải đưa ra các quyết định sau:

    - Có bất kỳ danh mục phụ nào bị loại trừ khỏi việc thu hồi thuế không?
    - Nhóm thuế bán hàng của các danh mục phụ là gì?
