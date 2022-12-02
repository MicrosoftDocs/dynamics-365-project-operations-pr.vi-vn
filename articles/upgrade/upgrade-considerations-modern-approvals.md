---
title: Các cân nhắc về nâng cấp cho Phê duyệt hiện đại
description: Bài viết đề cập đến những điểm mà quản trị viên nên xem xét khi họ bật chức năng Phê duyệt hiện đại.
author: stsporen
ms.date: 01/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 44a933c92d4ef8dff40f20200d74c4bbdf8caa76
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931770"
---
# <a name="upgrade-considerations-for-modern-approvals"></a>Các cân nhắc về nâng cấp cho Phê duyệt hiện đại 

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Là một phần của Bản phát hành tháng 4 năm 2022 Đợt 1, chức năng Phê duyệt hiện đại sẽ được bật theo mặc định. Chức năng này cải thiện độ tin cậy của logic phê duyệt và đảm bảo rằng bạn có thể xác định lý do nếu logic phê duyệt không thành công.

Là một phần của thay đổi này, các thay đổi trạng thái cho phê duyệt dự án được cập nhật. Trạng thái bây giờ sẽ chuyển trực tiếp từ **Đã gửi** thành **Đã phê duyệt**. **Đang chờ xử lý** không còn là trạng thái cần phê duyệt. Để xác định xem một mục phê duyệt có đang chờ xử lý hay không, hãy xác minh rằng mục phê duyệt đó là một phần của bộ phê duyệt và xem xét trạng thái của bộ phê duyệt đính kèm.

## <a name="before-you-upgrade"></a>Trước khi nâng cấp

Trước khi bạn nâng cấp lên Phê duyệt hiện đại, hãy đảm bảo rằng bạn không có mục phê duyệt nào đang chờ xử lý. Phê duyệt hiện đại không sử dụng trạng thái **Đang chờ xử lý**. Do đó, bất kỳ mục phê duyệt nào vẫn được đánh dấu là **Đang chờ xử lý** sau khi nâng cấp sẽ không được xử lý.

## <a name="after-you-upgrade"></a>Sau khi nâng cấp

Sau khi bạn nâng cấp lên Phê duyệt hiện đại, quản trị viên phải xác thực rằng dòng đám mây xử lý các mục phê duyệt đã được bật.

1. Đăng nhập vào [flow.microsoft.com](https://flow.microsoft.com)
2. Ở phía trên bên phải của trang, chuyển môi trường của bạn sang môi trường mà bạn đã nâng cấp.
3. Chọn **Giải pháp** để liệt kê các giải pháp được cài đặt trong môi trường.
4. Trong danh sách giải pháp, hãy chọn **Project Operations** hoặc **Project Service**.
5. Thay đổi bộ lọc từ **Tất cả** thành **Dòng đám mây**.
6. Xác minh rằng tùy chọn **Project Service – Lập lịch trình định kỳ Bộ phê duyệt dự án** được đặt thành **Bật**. Nếu không, chọn dòng rồi chọn **Bật**.
7. Xác minh rằng quá trình xử lý đang diễn ra sau mỗi năm phút bằng cách xem xét danh sách **Công việc hệ thống** trong khu vực **Cài đặt**.

## <a name="short-term-rollback"></a>Hoàn quy ngắn hạn

Nếu bạn không thể thực hiện các thay đổi hoặc nếu bạn gặp sự cố nghiêm trọng với tính năng này, bạn có thể tạm thời hoàn quy về quy trình phê duyệt ban đầu bằng cách thực hiện các bước sau:
1. Đăng nhập vào môi trường của bạn và xác minh rằng không có mục phê duyệt nào đang chờ xử lý.
2. Đi tới **Cài đặt** > **Tham số dự án**.
3. Chọn **Kiểm soát tính năng** và chọn **Phê duyệt hiện đại** để tắt tính năng.

## <a name="removing-the-feature-flag"></a>Xóa cờ tính năng

Trong bản cập nhật Tháng 10 năm 2022 Đợt 2, khả năng tắt tính năng này sẽ bị loại bỏ.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
