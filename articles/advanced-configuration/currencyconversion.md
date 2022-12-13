---
title: Thiết lập chuyển đổi tiền tệ để tính giá bán từ tỷ lệ chi phí
description: Bài viết này giải thích cách định cấu hình hành vi chuyển đổi tiền tệ sẽ được sử dụng trong Microsoft Dynamics 365 Project Operations khi các giao dịch bán hàng được tạo từ các giao dịch chi phí.
author: rumant
ms.date: 11/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3fa8077deb18f1a54e7f0f5e6dc4491a830df45b
ms.sourcegitcommit: 95e52fcf012a51229f3f6ae7dbf7b0fa56072a85
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 12/01/2022
ms.locfileid: "9816703"
---
# <a name="set-up-currency-conversion-to-calculate-sales-prices-from-cost-rates"></a>Thiết lập chuyển đổi tiền tệ để tính giá bán từ tỷ lệ chi phí

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Trong Microsoft Dynamics 365 Project Operations, giá bán cho các loại chi phí có thể được thiết lập dưới dạng giá trị số hoặc chúng có thể được thiết lập để chúng được tính toán dựa trên chi phí phát sinh.

Khi chúng được thiết lập để tính toán dựa trên chi phí phát sinh, sẽ có các tùy chọn sau:

- Tại mức chi phí
- Đánh dấu tỷ lệ phần trăm trên chi phí

Trong các tình huống mà chi phí phát sinh bằng đơn vị tiền tệ khác với đơn vị tiền tệ bán hàng cho hợp đồng dự án, quy đổi tiền tệ là bắt buộc để tính giá bán hàng dựa trên chi phí.

## <a name="currency-conversion-behavior-that-uses-native-dataverse-exchange-rates"></a>Hành vi chuyển đổi tiền tệ sử dụng tỷ giá hối đoái Dataverse gốc

Theo mặc định, Project Operations sử dụng tỷ giá hối đoái tiền tệ được lưu trữ trong bảng Tiền tệ Dataverse. Để định cấu hình Project Operations nhằm sử dụng tỷ giá hối đoái gốc để tính giá bán từ chi phí, hãy làm theo các bước sau.

1. Chuyển đến **Hoạt động dự án \> Cài đặt \> Tham số**.
1. Mở trang chi tiết **Tham số dự án** .
1. Đặt trường **Logic chuyển đổi tiền tệ** thành một giá trị trống.

## <a name="currency-conversion-behavior-that-uses-exchange-rates-from-finance-and-operations-apps"></a>Hành vi chuyển đổi tiền tệ sử dụng tỷ giá hối đoái từ các ứng dụng tài chính và hoạt động

Tỷ giá hối đoái trong bảng Tiền tệ sẵn có trong Dataverse không có ngày hiệu lực. Do đó, chúng có thể không phải lúc nào cũng được điều chỉnh theo yêu cầu mà bạn có để tính giá bán từ giá vốn.

Bạn có thể sử dụng tỷ giá hối đoái từ môi trường tài chính và hoạt động để tính giá bán bằng đơn vị tiền tệ bán hàng từ tỷ giá chi phí bằng đơn vị tiền tệ chi phí. Để định cấu hình hành vi chuyển đổi tiền tệ này, hãy làm theo các bước sau.

1. Trên trang **Thông số dự án**, hãy thêm trường **Logic chuyển đổi tiền tệ** . Sau đó lưu và xuất bản tùy chỉnh.
1. Chuyển đến **Hoạt động dự án \> Cài đặt \> Tham số**.
1. Mở trang chi tiết **Tham số dự án** . 
1. Đặt trường **Hành vi chuyển đổi tiền tệ** thành **Mở rộng với dự phòng thành mặc định**.
1. Cấp cho **Người dùng ứng dụng ghi kép** vai trò bảo mật **Quyền đọc toàn cầu** đối với các bảng sau:

    - msdyn\_ trao đổi tiền tệ
    - msdyn\_ cặp tỷ giá hối đoái
    - msdyn\_ các loại tỷ giá hối đoái

1. Trong môi trường hoạt động và tài chính của bạn, hãy chạy các bản đồ ghi kép sau với đồng bộ hóa ban đầu:

    - Loại tỷ giá hối đoái (msdyn\_ exchangeratetypes)
    - Cặp tiền tỷ giá hối đoái (msdyn\_ currencyexchangeratepairs)
    - Tỷ giá hối đoái CDS (msdyn\_ trao đổi tiền tệ)

Sau khi những thay đổi này hoàn tất, tính năng ghi kép sẽ cung cấp tỷ giá hối đoái từ môi trường tài chính và hoạt động trong Dataverse. Sau đó, Project Operations sẽ sử dụng các tỷ giá hối đoái đó để chuyển đổi tỷ giá chi phí thành đơn vị tiền tệ bán hàng của hợp đồng.

> [!NOTE]
> Hành vi chuyển đổi tiền tệ này chỉ áp dụng cho việc tính toán giá bán từ tỷ lệ chi phí. Nó sẽ không được sử dụng để tính toán chung các giá trị tiền tệ cơ sở. Các giá trị tiền tệ cơ sở sẽ luôn sử dụng tỷ giá hối đoái Dataverse gốc, bất kể bạn có hoàn thành quy trình này hay không.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
