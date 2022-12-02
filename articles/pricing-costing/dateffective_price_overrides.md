---
title: Ngày bắt đầu có hiệu lực thay thế giá
description: Bài viết này giải thích cách thiết lập thay thế giá cho các mức giá cụ thể trong bảng giá.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 41af5176c0809c9621fc0fa946a04492da7d152b
ms.sourcegitcommit: 37293b0b28f072deafc00112ddbbea91c48a7802
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 09/08/2022
ms.locfileid: "9446014"
---
# <a name="date-effective-price-overrides"></a>Ngày bắt đầu có hiệu lực thay thế giá 

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

*Ngày bắt đầu có hiệu lực thay thế giá* cung cấp cách thay thế hoặc thay đổi các mức giá cụ thể trong bảng giá. Ví dụ: bạn có một bảng giá chuẩn có hiệu lực từ ngày 1 tháng 1 năm 2022 đến hết ngày 31 tháng 12 năm 2022. Bảng giá này có giá cho nhiều vai trò. Giá được thiết lập cho vai trò **Kỹ thuật viên mạng** là 100 đô-la Mỹ (USD) mỗi giờ. Khi kỹ thuật viên mạng ghi lại thời gian từ ngày 1 tháng 1 năm 2022 đến ngày 31 tháng 12 năm 2022, thời gian có giá là 100 USD. Ngày 1 tháng 10 năm 2022, bạn phải điều chỉnh giá *chỉ* cho vai trò **Kỹ thuật viên mạng**, từ 100 USD mỗi giờ đến 110 USD mỗi giờ. Tính năng **Ngày bắt đầu có hiệu lực thay thế giá** cho phép bạn thiết lập thay đổi này dưới dạng ghi thay thế cho giá của vai trò cụ thể đó. Do đó, bạn không cần phải sao chép toàn bộ bảng giá và thay đổi giá của chỉ một hàng đó.

## <a name="date-effective-price-overrides-for-labor-pricing"></a>Ngày bắt đầu có hiệu lực thay thế giá cho giá nhân công

Quá trình thiết lập ngày bắt đầu có hiệu lực thay thế giá cho thời gian nhân công trong một dự án bao gồm hai bước cơ bản.

1. Bật tính năng **Ngày bắt đầu có hiệu lực thay thế giá**.
1. Thiết lập Ngày bắt đầu có hiệu lực thay thế giá.

### <a name="enable-the-date-effective-price-overrides-feature"></a>Bật tính năng Ngày bắt đầu có hiệu lực thay thế giá

> [!NOTE]
> Sau khi tính năng **Ngày bắt đầu có hiệu lực thay thế giá** được bật, không thể tắt tính năng này.

Để bật tính năng **Ngày bắt đầu có hiệu lực thay thế giá**, hãy làm theo các bước sau.

1. Đi tới **Cài đặt** \> **Tham số**.
1. Mở bản ghi **Tham số**.
1. Trên Ngăn hành động, trên tab **Kiểm soát tính năng**, chọn **Bật Ngày bắt đầu có hiệu lực thay thế giá**.
1. Chọn **OK** trong hộp thoại xác nhận.
1. Sau một lúc, hãy làm mới trình duyệt của bạn. Tính năng Ngày bắt đầu có hiệu lực thay thế giá sẽ khả dụng. Bạn sẽ biết rằng những khả năng này đã được kích hoạt nếu **Bật Ngày bắt đầu có hiệu lực thay thế giá** không còn xuất hiện trên Ngăn hành động.

### <a name="set-up-a-date-effective-price-override"></a>Thiết lập Ngày bắt đầu có hiệu lực thay thế giá

Ngày bắt đầu có hiệu lực thay thế giá có thể được thiết lập trên bảng giá **Chi phí**, **Doanh số** hoặc **Mua hàng**.

> [!NOTE]
>Hành vi của **Ngày bắt đầu có hiệu lực thay thế giá** hiện có những hạn chế sau:
>
> - Chỉ giá vai trò và tăng giá theo vai trò mới hỗ trợ tính năng **Ngày bắt đầu có hiệu lực thay thế giá** trong Project Operations.
> - Khi bạn sao chép một bảng giá bằng cách sử dụng hành động **Sao chép** trên trang **Chi tiết bảng giá** và khi bạn tạo danh sách giá dự án từ danh sách giá tiêu chuẩn hoặc tùy chỉnh trong quá trình tạo hợp đồng, ngày bắt đầu có hiệu lực thay thế giá **không** được sao chép từ bảng giá nguồn.

Để thiết lập ngày bắt đầu có hiệu lực thay thế giá cho giá vai trò hoặc tăng giá theo vai trò, hãy làm theo các bước sau.

1. Mở trang cho bảng giá mà bạn muốn thiết lập ngày bắt đầu có hiệu lực thay thế giá.
1. Chọn tab **Giá vai trò**. Tab này liệt kê tất cả bản ghi **Giá vai trò** trong bảng giá.
1. Chọn bản ghi **Giá vai trò** mà bạn muốn thiết lập ngày bắt đầu có hiệu lực thay thế giá mới, sau đó nhấn đúp (hoặc nhấp đúp) vào **Giá vai trò** để mở trang **Chi tiết giá vai trò**.
1. Chọn tab **Ngày bắt đầu có hiệu lực thay thế**. Lưới trên tab này liệt kê tất cả các ngày bắt đầu có hiệu lực thay thế giá cho bản ghi **Giá vai trò** đã chọn.
1. Trên thanh công cụ phía trên lưới, chọn **Thay thế giá theo vai trò mới**. Thanh trượt **Thay thế giá theo vai trò mới** mở ra.
1. Chỉ định ngày có hiệu lực, đơn vị và giá mới cho thay thế giá. Sau đó, chọn **Lưu** rồi đóng biểu mẫu.

> [!NOTE]
> - Ngày bắt đầu có hiệu lực thay thế giá cho giá vai trò hoặc tăng giá theo vai trò có thể áp dụng cho cùng một kết hợp các giá trị thứ nguyên đặt giá tồn tại trên hàng chính **Giá vai trò** hoặc **Tăng giá theo vai trò**.
> - Ngày được chọn trong trường **Có hiệu lực từ** phải nằm trong ngày có hiệu lực của bảng giá gốc. Thay thế giá sẽ có hiệu lực vào ngày được chọn trong trường **Có hiệu lực từ** và sẽ áp dụng cho đến hết ngày kết thúc của bảng giá gốc. Nếu bạn thiết lập một ngày bắt đầu có hiệu lực thay thế giá khác cho cùng một giá vai trò, thay thế giá đầu tiên sẽ có hiệu lực vào ngày được chọn trong trường **Có hiệu lực từ** và sẽ áp dụng cho đến khi bắt đầu thay thế thứ hai.

## <a name="examples"></a>Ví dụ

### <a name="example-1-determining-date-effectivity-for-a-role-price-that-has-role-price-overrides"></a>Ví dụ 1: Xác định ngày có hiệu lực cho một giá vai trò có các thay giá vai trò

Ví dụ sau đây cho thấy cách xác định ngày có hiệu lực cho một giá vai trò cụ thể mà được thiết lập các thay thế giá vai trò.

**Bảng giá A: 1 tháng 1 đến 30 tháng 6**

*Giá vai trò*

| Giá vai trò | Đơn vị | Giá | Ảnh hưởng giá cho các giao dịch đến |
|---|---|---|---|
| Kỹ thuật viên mạng | Giờ | 100 | Giá này sẽ được sử dụng cho bất kỳ giao dịch nào có ngày giao dịch từ ngày 1 tháng 1 đến ngày 14 tháng 3. |

*Thay thế giá theo vai trò*

| Có hiệu lực từ | Đơn vị | Giá | Ảnh hưởng giá cho các giao dịch đến |
|---|---|---|---|
| Ngày 15 tháng 3 | Giờ | 110 | Giá này sẽ được sử dụng cho bất kỳ giao dịch nào có ngày giao dịch từ ngày 15 tháng 3 đến ngày 30 tháng 3. |
| Ngày 1 tháng 4 | Giờ | 120 | Giá này sẽ được sử dụng cho bất kỳ giao dịch nào có ngày giao dịch từ ngày 1 tháng 4 đến ngày 30 tháng 6. |

### <a name="example-2-determining-date-effectivity-for-a-role-price-markup-that-has-role-price-markup-overrides"></a>Ví dụ 2: Xác định ngày có hiệu lực cho một tăng giá theo vai trò có các thay thế tăng giá theo vai trò

Ví dụ sau đây cho thấy cách xác định ngày có hiệu lực cho một tăng giá theo vai trò cụ thể mà được thiết lập các thay thế tăng giá theo vai trò.

**Bảng giá A: 1 tháng 1 đến 30 tháng 6**

*Giá vai trò*

| Giá vai trò | Giờ làm việc | Đơn vị | Giá | Ảnh hưởng giá cho các giao dịch đến |
|---|---|---|---|---|
| Kỹ thuật viên mạng | Thường xuyên | Giờ | 100 | Giá này sẽ được sử dụng cho bất kỳ giao dịch nào có ngày giao dịch từ ngày 1 tháng 1 đến ngày 14 tháng 3. |

*Tăng giá theo vai trò*

| Đơn vị tổ chức | Giờ làm việc | % Tăng giá |
|---|---|---|
| Contoso US | Làm thêm | 10% |

*Thay thế tăng giá theo vai trò*

| Có hiệu lực từ | Giá | Ảnh hưởng giá cho các giao dịch đến |
|---|---|---|
| Ngày 15 tháng 3 | 20% | Phần trăm tăng giá này sẽ được sử dụng cho bất kỳ giao dịch nào có ngày giao dịch từ ngày 15 tháng 3 đến ngày 30 tháng 3. |
| Ngày 1 tháng 4 | 25% | Tăng giá này sẽ được sử dụng cho bất kỳ giao dịch nào có ngày giao dịch từ ngày 1 tháng 4 đến ngày 30 tháng 6. |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
