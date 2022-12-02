---
title: Kích hoạt và sửa đổi báo giá dự án
description: Bài viết này cung cấp thông tin về cách kích hoạt và sửa đổi báo giá trong Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e71102078832ac7d5f8e5edb40cc484df927eda4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410391"
---
# <a name="activate-and-revise-a-project-quote"></a>Kích hoạt và sửa đổi báo giá dự án

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Khả năng kích hoạt và sửa đổi giúp bạn theo dõi việc lập phiên bản cho các báo giá dựa trên dự án trong giai đoạn ước tính và thương lượng. Khi bản nháp của một báo giá được kích hoạt, nó sẽ trở thành chỉ đọc.

Khả năng kích hoạt và sửa đổi cho phép bạn thực hiện các nhiệm vụ sau:

- Giành hoặc mất báo giá chỉ sau khi kích hoạt.
- Sửa đổi báo giá để thực hiện các thay đổi đối với báo giá hiện có hoặc tạo phiên bản mới.

> [!NOTE]
> Sau khi tính năng kích hoạt và sửa đổi báo giá được bật, bạn không thể tắt tính năng này.

Để bật khả năng kích hoạt và sửa đổi báo giá dựa trên dự án, hãy làm theo các bước sau.

1. Đi tới **Cài đặt** \> **Tham số**.
1. Mở bản ghi **Tham số**.
1. Trên Ngăn hành động, trên tab **Kiểm soát tính năng**, chọn **Bật Kích hoạt và sửa lại báo giá**.
1. Chọn **OK** trong hộp thoại xác nhận.
1. Sau một lúc, hãy làm mới trình duyệt của bạn. Các khả năng kích hoạt và sửa đổi bây giờ sẽ có sẵn. Bạn sẽ biết rằng những khả năng này đã được kích hoạt nếu nút **Bật Kích hoạt và sửa lại báo giá** không còn xuất hiện trên Ngăn hành động.

## <a name="activating-a-quote"></a>Kích hoạt báo giá

Sau khi tính năng kích hoạt và sửa lại báo giá được bật, các nút **Đóng báo giá dưới dạng Đã giành được** và **Đóng báo giá dưới dạng Đã mất** trên Ngăn hành động không khả dụng cho báo giá dự án nháp. Chúng chỉ có sẵn sau khi một báo giá được kích hoạt.

Kích hoạt thể hiện giai đoạn trong quá trình báo giá khi bạn muốn ngăn chặn nhiều thay đổi hơn đối với báo giá. Ở giai đoạn này, báo giá được gửi để xem xét nội bộ hoặc gửi tới khách hàng.

Các nút **Đóng báo giá dưới dạng đã giành được** và **Đóng báo giá dưới dạng Đã mất** trên Ngăn hành động có sẵn cho các báo giá đã kích hoạt. Tùy thuộc vào kết quả của đánh giá nội bộ hoặc đánh giá của khách hàng, bạn có thể sử dụng một trong các nút này để đóng báo giá đã kích hoạt. Bạn có thể thương lượng và thay đổi báo giá đã kích hoạt bằng cách chọn **Sửa đổi báo giá**.

## <a name="revising-a-quote"></a>Sửa đổi báo giá

Nếu bạn phải thay đổi báo giá đã kích hoạt, hãy chọn **Sửa đổi báo giá**. Báo giá được đóng, và mã lý do **đã sửa lại** được sử dụng. Sau đó, một báo cáo mới được tạo có cùng ID và mã số sửa đổi tăng dần. Tất cả các chi tiết từ báo giá gốc được sao chép sang báo giá mới. Báo giá mới ở trạng thái nháp và có thể được chỉnh sửa theo yêu cầu.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
