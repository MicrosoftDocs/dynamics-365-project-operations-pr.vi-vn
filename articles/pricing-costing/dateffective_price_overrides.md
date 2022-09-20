---
title: Ghi đè giá theo ngày có hiệu lực
description: Bài viết này giải thích cách thiết lập ghi đè giá cho các giá cụ thể trong danh sách giá.
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
# <a name="date-effective-price-overrides"></a>Ghi đè giá theo ngày có hiệu lực 

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

*Ghi đè giá theo ngày có hiệu lực* cung cấp cách ghi đè hoặc thay đổi giá cụ thể trong bảng giá. Ví dụ: bạn có một bảng giá chuẩn có hiệu lực từ ngày 1 tháng 1 năm 2022 đến hết ngày 31 tháng 12 năm 2022. Bảng giá này có giá cho nhiều vai trò. Giá được thiết lập cho **Kỹ thuật viên mạng** vai trò là 100 đô la Mỹ (USD) mỗi giờ. Khi kỹ thuật viên mạng ghi lại thời gian từ ngày 1 tháng 1 năm 2022 đến ngày 31 tháng 12 năm 2022, thời gian có giá là 100 USD. Ngày 1 tháng 10 năm 2022, bạn phải điều chỉnh giá *chỉ có* cho **Kỹ thuật viên mạng** vai trò, từ 100 USD mỗi giờ đến 110 USD mỗi giờ. Các **Ghi đè giá có hiệu lực theo ngày** tính năng này cho phép bạn thiết lập thay đổi này dưới dạng ghi đè hàng cho giá vai trò cụ thể đó. Do đó, bạn không cần phải sao chép toàn bộ bảng giá và thay đổi giá của chỉ một hàng đó.

## <a name="date-effective-price-overrides-for-labor-pricing"></a>Ghi đè giá theo ngày có hiệu lực để định giá lao động

Quá trình thiết lập ghi đè giá có hiệu lực theo ngày cho thời gian lao động trong một dự án bao gồm hai bước cơ bản.

1. Cho phép **Ghi đè giá có hiệu lực theo ngày** tính năng.
1. Thiết lập ghi đè giá có hiệu lực theo ngày.

### <a name="enable-the-date-effective-price-overrides-feature"></a>Bật tính năng ghi đè giá có hiệu lực Ngày

> [!NOTE]
> Sau **Ghi đè giá có hiệu lực theo ngày** tính năng được bật, không thể tắt được.

Để kích hoạt **Ghi đè giá theo ngày có hiệu lực**, hãy làm theo các bước sau.

1. Đi đến **Cài đặt** \> **Thông số**.
1. Mở **Thông số** ghi lại.
1. Trên Ngăn hành động, trên **Kiểm soát tính năng** tab, chọn **Bật ghi đè giá có hiệu lực theo ngày**.
1. Chọn **OK** trong hộp thoại xác nhận.
1. Sau một lúc, hãy làm mới trình duyệt của bạn. Tính năng ghi đè giá có hiệu lực theo ngày giờ sẽ khả dụng. Bạn sẽ biết rằng những khả năng này đã được kích hoạt nếu **Bật ghi đè giá có hiệu lực theo ngày** không còn xuất hiện trên Ngăn hành động.

### <a name="set-up-a-date-effective-price-override"></a>Thiết lập ghi đè giá có hiệu lực theo ngày

Ghi đè giá có hiệu lực theo ngày có thể được thiết lập vào **Phí tổn**, **bán hàng**, hoặc **Mua, tựa vào, bám vào** bảng giá.

> [!NOTE]
>Hành vi của **Ghi đè giá có hiệu lực theo ngày** hiện có những hạn chế sau:
>
> - Chỉ giá vai trò và đánh dấu giá vai trò mới hỗ trợ **Ghi đè giá có hiệu lực theo ngày** tính năng trong Hoạt động dự án.
> - Khi bạn sao chép một bảng giá bằng cách sử dụng **Sao chép** hành động trên **Chi tiết bảng giá** và khi bạn tạo danh sách giá dự án từ danh sách giá tiêu chuẩn hoặc tùy chỉnh trong quá trình tạo hợp đồng, ghi đè giá có hiệu lực theo ngày sẽ **không phải** được sao chép từ bảng giá nguồn.

Để thiết lập ghi đè giá có hiệu lực theo ngày cho giá vai trò hoặc đánh dấu giá vai trò, hãy làm theo các bước sau.

1. Mở trang cho bảng giá mà bạn muốn thiết lập ghi đè giá có hiệu lực theo ngày.
1. Chọn **Giá vai trò** chuyển hướng. Tab này liệt kê tất cả **Giá vai trò** hồ sơ trong bảng giá.
1. Chọn **Giá vai trò** ghi lại rằng bạn muốn thiết lập giá ghi đè có hiệu lực theo ngày mới, sau đó nhấn đúp (hoặc nhấp đúp) **Giá vai trò** để mở **Chi tiết giá vai trò** trang.
1. Chọn **Ghi đè ngày có hiệu lực** chuyển hướng. Lưới trên tab này liệt kê tất cả các ghi đè giá có hiệu lực theo ngày cho giá đã chọn **Giá vai trò** ghi lại.
1. Trên thanh công cụ phía trên lưới, hãy chọn **Ghi đè giá vai trò mới**. Các **Ghi đè giá vai trò mới** thanh trượt mở ra.
1. Chỉ định ngày có hiệu lực, đơn vị và giá mới cho ghi đè giá. Sau đó chọn **Tiết kiệm** và đóng biểu mẫu.

> [!NOTE]
> - Ghi đè giá có hiệu lực theo ngày cho giá vai trò hoặc đánh dấu giá vai trò có thể áp dụng cho cùng một tổ hợp các giá trị thứ nguyên đặt giá tồn tại trên giá chính **Giá vai trò** hoặc **Đánh giá vai trò** hàng ngang.
> - Ngày được chọn trong **Có hiệu lực từ** trường phải nằm trong ngày có hiệu lực của bảng giá gốc. Ghi đè giá sẽ có hiệu lực vào ngày được chọn trong **Có hiệu lực từ** và sẽ áp dụng cho đến cuối ngày kết thúc của bảng giá gốc. Nếu bạn thiết lập một ghi đè giá có hiệu lực theo ngày khác cho cùng một giá vai trò, ghi đè giá đầu tiên sẽ có hiệu lực vào ngày được chọn trong **Có hiệu lực từ** và sẽ áp dụng cho đến khi bắt đầu ghi đè thứ hai.

## <a name="examples"></a>Ví dụ

### <a name="example-1-determining-date-effectivity-for-a-role-price-that-has-role-price-overrides"></a>Ví dụ 1: Xác định tính hiệu quả của ngày cho một giá vai trò có ghi đè giá vai trò

Ví dụ sau đây cho thấy cách xác định tính hiệu quả của ngày cho một giá vai trò cụ thể mà giá ghi đè giá vai trò được thiết lập.

**Bảng giá A: 1 tháng 1 đến 30 tháng 6**

*Giá vai trò*

| Giá vai trò | Đơn vị | Giá | Ảnh hưởng đến việc định giá cho các giao dịch đến |
|---|---|---|---|
| Kỹ thuật viên mạng | Giờ | 100 | Giá này sẽ được sử dụng cho bất kỳ giao dịch nào có ngày giao dịch từ ngày 1 tháng 1 đến ngày 14 tháng 3. |

*Ghi đè giá vai trò*

| Có hiệu lực từ | Đơn vị | Giá | Ảnh hưởng đến việc định giá cho các giao dịch đến |
|---|---|---|---|
| Ngày 15 tháng 3 | Giờ | 110 | Giá này sẽ được sử dụng cho bất kỳ giao dịch nào có ngày giao dịch từ ngày 15 tháng 3 đến ngày 30 tháng 3. |
| 1 Tháng 4 | Giờ | 120 | Giá này sẽ được sử dụng cho bất kỳ giao dịch nào có ngày giao dịch từ ngày 1 tháng 4 đến ngày 30 tháng 6. |

### <a name="example-2-determining-date-effectivity-for-a-role-price-markup-that-has-role-price-markup-overrides"></a>Ví dụ 2: Xác định tính hiệu quả của ngày cho đánh dấu giá vai trò có ghi đè đánh dấu giá vai trò

Ví dụ sau đây cho thấy cách xác định hiệu quả của ngày đối với đánh dấu giá vai trò cụ thể mà ghi đè đánh dấu giá vai trò được thiết lập.

**Bảng giá A: 1 tháng 1 đến 30 tháng 6**

*Giá vai trò*

| Giá vai trò | Giờ làm việc | Đơn vị | Giá | Ảnh hưởng đến việc định giá cho các giao dịch đến |
|---|---|---|---|---|
| Kỹ thuật viên mạng | Thường xuyên | Giờ | 100 | Giá này sẽ được sử dụng cho bất kỳ giao dịch nào có ngày giao dịch từ ngày 1 tháng 1 đến ngày 14 tháng 3. |

*Đánh giá vai trò*

| Đơn vị tổ chức | Giờ làm việc | Đánh dấu% |
|---|---|---|
| Contoso US | Làm thêm | 10% |

*Ghi đè đánh dấu giá vai trò*

| Có hiệu lực từ | Giá | Ảnh hưởng đến việc định giá cho các giao dịch đến |
|---|---|---|
| Ngày 15 tháng 3 | 20% | Phần trăm đánh dấu này sẽ được sử dụng cho bất kỳ giao dịch nào có ngày giao dịch từ ngày 15 tháng 3 đến ngày 30 tháng 3. |
| 1 Tháng 4 | 25% | Đánh dấu này sẽ được sử dụng cho bất kỳ giao dịch nào có ngày giao dịch từ ngày 1 tháng 4 đến ngày 30 tháng 6. |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
