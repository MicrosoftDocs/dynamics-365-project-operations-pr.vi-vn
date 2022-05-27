---
title: Cân nhắc nâng cấp đối với Phê duyệt hiện đại
description: Chủ đề bao gồm các điểm mà quản trị viên nên xem xét khi họ bật chức năng Phê duyệt hiện đại.
author: stsporen
ms.date: 01/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: a3757f057a801318feccde9be3e49c7b40fa8fcb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578412"
---
# <a name="upgrade-considerations-for-modern-approvals"></a>Cân nhắc nâng cấp đối với Phê duyệt hiện đại 

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Là một phần của Bản phát hành Làn sóng 1 vào tháng 4 năm 2022, chức năng Phê duyệt hiện đại sẽ được bật theo mặc định. Chức năng này cải thiện độ tin cậy của logic phê duyệt và đảm bảo rằng bạn có thể xác định lý do nếu logic phê duyệt không thành công.

Là một phần của thay đổi này, các thay đổi trạng thái để phê duyệt dự án được cập nhật. Trạng thái bây giờ đi trực tiếp từ **Đã đệ trình** đến **Đã được phê duyệt**. **Chưa giải quyết** không còn là trạng thái để phê duyệt. Để xác định xem phê duyệt có đang chờ xử lý hay không, hãy xác minh rằng phê duyệt là một phần của tập hợp phê duyệt và xem xét trạng thái của tập hợp phê duyệt đính kèm.

## <a name="before-you-upgrade"></a>Trước khi bạn nâng cấp

Trước khi bạn nâng cấp lên Phê duyệt hiện đại, hãy đảm bảo rằng bạn không có phê duyệt nào đang chờ xử lý. Phê duyệt hiện đại không sử dụng **Chưa giải quyết** tình trạng. Do đó, mọi phê duyệt vẫn được đánh dấu là **Chưa giải quyết** sau khi nâng cấp sẽ không được xử lý.

## <a name="after-you-upgrade"></a>Sau khi bạn nâng cấp

Sau khi bạn nâng cấp lên Phê duyệt hiện đại, quản trị viên phải xác thực rằng luồng đám mây xử lý phê duyệt đã được bật.

1. đăng nhập vào [flow.microsoft.com](https://flow.microsoft.com)
2. Ở phía trên bên phải của trang, hãy chuyển môi trường của bạn sang môi trường mà bạn đã nâng cấp.
3. Lựa chọn **Các giải pháp** để liệt kê các giải pháp được cài đặt trong môi trường.
4. Trong danh sách giải pháp, hãy chọn **Hoạt động dự án** hoặc **Dịch vụ dự án**.
5. Thay đổi bộ lọc từ **Tất cả các** đến **Dòng chảy trên đám mây**.
6. Xác minh rằng **Dịch vụ dự án - Lập kế hoạch định kỳ Bộ phê duyệt dự án** tùy chọn được đặt thành **Trên**. Nếu không, hãy chọn luồng, sau đó chọn **Bật**.
7. Xác minh rằng quá trình xử lý đang diễn ra sau mỗi năm phút bằng cách xem xét **Công việc hệ thống** danh sách trong **Cài đặt** khu vực.

## <a name="short-term-rollback"></a>Hoàn vốn ngắn hạn

Nếu bạn không thể thực hiện các thay đổi hoặc nếu bạn gặp sự cố nghiêm trọng với tính năng này, bạn có thể tạm thời hoàn nguyên về quy trình phê duyệt ban đầu bằng cách thực hiện các bước sau:
1. Đăng nhập vào môi trường của bạn và xác minh rằng không có phê duyệt nào đang chờ xử lý.
2. Đi đến **Cài đặt** > **Tham số dự án**.
3. Lựa chọn **Kiểm soát tính năng** và sau đó chọn **Phê duyệt hiện đại** để tắt tính năng.

## <a name="removing-the-feature-flag"></a>Xóa cờ tính năng

Trong bản cập nhật Wave 2 tháng 10 năm 2022, khả năng tắt tính năng này sẽ bị loại bỏ.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
