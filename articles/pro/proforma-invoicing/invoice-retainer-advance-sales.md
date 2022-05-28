---
title: Lập hóa đơn khoản trả trước hoặc khoản tạm ứng
description: Chủ đề này cung cấp thông tin về cách lập hóa đơn khoản trả trước hoặc khoản tạm ứng trong Project Operations.
author: rumant
ms.date: 10/20/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: aa659ebfa6d848f312caa1d197404d77b1f6ee21
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590602"
---
# <a name="invoice-a-retainer-or-an-advance"></a>Lập hóa đơn khoản tạm ứng hoặc khoản trả trước

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Dynamics 365 Project Operations hỗ trợ tạm ứng một lần và hợp đồng dựa trên khoản giữ lại. Trên hợp đồng dự án, bạn có thể ghi lại lịch trình của những khoản trả trước hoặc tạm ứng một lần. Tuy nhiên, việc ghi lại ở cấp độ hợp đồng dự án sẽ không làm cho một khoản trả trước hoặc tạm ứng chuyển ngay sang trạng thái sẵn dùng. Để sử dụng khoản trả trước hoặc tạm ứng trên một hóa đơn thực sự tính phí cho khách hàng, trước tiên, bạn phải lập hóa đơn khoản trả trước hoặc tạm ứng đó.

Hãy hoàn thành các bước sau để lập hóa đơn khoản trả trước hoặc tạm ứng.

1. Chọn **Bán hàng** > **Thanh toán** > **Khoản trả trước và tạm ứng**. 
2. Trên trang **Khoản tạm ứng và trả trước**, hãy sử dụng bộ lọc để chọn khoản trả trước hoặc tạm ứng cụ thể cần lập hóa đơn và đánh dấu mục đó là **Đã sẵn sàng để lập hóa đơn**.
3. Tạo thủ công hóa đơn từ danh sách **Hợp đồng dự án** hoặc trang chi tiết. Khoản trả trước hoặc tạm ứng được hiển thị trên hóa đơn nháp trong phần **Khoản tạm ứng và trả trước** trên trang **Hóa đơn**.
4. Xác nhận hóa đơn. Điều này sẽ làm cho khoản trả trước hoặc tạm ứng chuyển sang trạng thái sẵn dùng. Bạn có thể xác minh hóa đơn trên trang danh sách **Khoản trả trước và tạm ứng**. Đối với khoản Tạm ứng hoặc Giữ lại được lập hóa đơn, số tiền khả dụng được hiển thị trong lưới.

## <a name="create-a-retainer-or-advance-from-the-invoice-grid"></a>Tạo khoản trả trước hoặc tạm ứng từ lưới Hóa đơn

Bạn có thể tạo trực tiếp khoản trả trước hoặc tạm ứng trên hóa đơn.

1. Trên hóa đơn nháp, ở lưới con **Khoản tạm ứng và trả trước**, hãy chọn **Mới** để tạo khoản trả trước hoặc tạm ứng mới. 
2. Trên trang **Tạo nhanh**, hãy thêm thông tin cần thiết rồi chọn **Lưu**. Khoản trả trước hoặc tạm ứng được tạo trên hợp đồng dự án liên quan đến hóa đơn. Khoản tạm ứng hoặc trả trước được tự động đánh dấu là **Đã sẵn sàng để lập hóa đơn**, rồi được thêm vào lưới con **Khoản tạm ứng và trả trước** trên trang **Hóa đơn**.

## <a name="reconcile-an-invoiced-retainer-or-advance"></a>Điều hòa khoản trả trước hoặc tạm ứng đã lập hóa đơn

Sau khi khoản trả trước hoặc tạm ứng được lập hóa đơn, chúng có thể được sử dụng hoặc được điều hòa trên hóa đơn có mục thời gian, chi phí, mốc hoặc các phí khác dựa trên dự án. Khách hàng sẽ thấy số tiền trên hóa đơn của họ được trừ đi khoản trả trước hoặc tạm ứng dùng trên hóa đơn này.

Trên mọi hóa đơn được tạo cho một hợp đồng dự án có khoản trả trước hoặc tạm ứng đã lập hóa đơn, Project Operations tự động áp dụng khoản trả trước hoặc tạm ứng cho hóa đơn.

Bạn có thể thấy mục này trong lưới **Khoản trả trước và tạm ứng đã áp dụng** trên trang **Hóa đơn**. Bảng sau cung cấp thông tin về các trường trên trang **Khoản trả trước và tạm ứng đã áp dụng** của trang **Hóa đơn dự án**.

| Trường | Vị trí | Nội dung mô tả | Tác động xuôi tuyến |
| --- | --- | --- | --- |
| Nội dung mô tả | Lưới **Khoản trả trước và tạm ứng đã áp dụng** trên trang **Hóa đơn dự án** |Trường chỉ đọc này cung cấp nội dung mô tả về khoản trả trước hoặc tạm ứng được sử dụng trên hóa đơn này. Bạn không thể thay đổi giá trị này trên hóa đơn. Giá trị này có thể được cập nhật trên lưới con ở trang **Hợp đồng dự án**. | Trường này có thể được hiển thị cho khách hàng trên hóa đơn đã in để cho biết khoản trả trước hoặc tạm ứng nào được áp dụng trên hóa đơn. |
| Ngày giao | Lưới **Khoản trả trước và tạm ứng đã áp dụng** trên trang **Hóa đơn dự án**  | Trường chỉ đọc này cung cấp ngày lập hóa đơn của khoản trả trước hoặc tạm ứng được sử dụng trên hóa đơn này. Bạn không thể thay đổi giá trị này trên hóa đơn. Giá trị này có thể được cập nhật trên lưới con ở trang **Hợp đồng dự án**. | Trường này có thể được hiển thị cho khách hàng trên hóa đơn đã in để cho biết ngày lập hóa đơn đầu tiên của khoản trả trước hoặc tạm ứng cho khách hàng. |
| Số lượng | Lưới **Khoản trả trước và tạm ứng đã áp dụng** trên trang **Hóa đơn dự án**  | Trường chỉ đọc này cung cấp số tiền của khoản trả trước hoặc tạm ứng được sử dụng trên hóa đơn này. Bạn không thể thay đổi giá trị này trên hóa đơn. Giá trị này có thể được cập nhật trên lưới con ở trang **Hợp đồng dự án**. | Trường này có thể được hiển thị cho khách hàng trên hóa đơn đã in để cho biết số tiền trả trước hoặc tạm ứng ban đầu mà khách hàng chi trả. |
| Số tiền đã dùng | Lưới **Khoản trả trước và tạm ứng đã áp dụng** trên trang **Hóa đơn dự án**  | Trường chỉ đọc này cung cấp giá trị đã tính toán bao gồm số tiền đã sử dụng của khoản trả trước hoặc tạm ứng. | Trường này có thể được hiển thị cho khách hàng trên hóa đơn đã in để cho biết số tiền đã sử dụng trong khoản trả trước hoặc tạm ứng này. |
| Số tiền Cộng thêm | Lưới **Khoản trả trước và tạm ứng đã áp dụng** trên trang **Hóa đơn dự án**  | Trường có thể sửa này cung cấp số tiền của khoản trả trước hoặc tạm ứng hiện được sử dụng trên hóa đơn dự án này. Số tiền này không thể nhiều hơn số tiền có sẵn trong khoản tạm ứng. Hệ thống tự động tính toán mục này dưới dạng hiệu số giữa các giá trị trường **Số tiền** và **Số tiền đã sử dụng** trên lưới. Bạn có thể giảm giá trị này để không sử dụng hết số tiền hiện có, nhưng bạn không thể tăng số tiền vượt quá mức hiện có. | Trường này có thể được hiển thị cho khách hàng trên hóa đơn đã in để cho biết số tiền trong khoản trả trước hoặc tạm ứng này hiện được dùng trên hóa đơn. |
| Số dư trong khoản trả trước. | Lưới **Khoản trả trước và tạm ứng đã áp dụng** trên trang **Hóa đơn dự án**  | Trường chỉ đọc này cung cấp số tiền còn lại trong khoản trả trước hoặc tiền tạm ứng sau khi hóa đơn được xác nhận. | Trường này có thể được hiển thị cho khách hàng trên hóa đơn đã in để cho biết số tiền còn lại trong khoản trả trước hoặc tạm ứng này sau khi hóa đơn được xác nhận và thanh toán. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]