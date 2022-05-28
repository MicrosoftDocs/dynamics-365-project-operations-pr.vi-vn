---
title: Tiền tệ không khớp lỗi
description: Chủ đề này cung cấp thông tin gỡ rối về lỗi không khớp tiền tệ xảy ra khi bạn lưu các loại bản ghi cụ thể.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5bb54a121f0dc22f1c0ea88ada9c922c1d4c6544
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589774"
---
# <a name="currency-mismatch-error"></a>Tiền tệ không khớp lỗi 

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Khi bạn lưu dự án, hợp đồng, báo giá hoặc tài nguyên có thể đặt trước, bạn có thể gặp lỗi, **Đơn vị tiền tệ của công ty sở hữu không khớp với đơn vị tiền tệ của hợp đồng. Chọn công ty sở hữu hoặc đơn vị hợp đồng khác để tiếp tục**. Điều này là do có sự không khớp về đơn vị tiền tệ giữa đơn vị tiền tệ của hợp đồng cho hồ sơ và đơn vị tiền tệ của công ty sở hữu.


## <a name="resolution"></a>Cách giải quyết

Để khắc phục sự cố này, hãy làm như sau:
- Xác minh loại tiền của đơn vị ký hợp đồng cho hồ sơ này. Bạn có thể xem đơn vị tiền tệ bằng cách mở hồ sơ đơn vị tổ chức và xác minh giá trị trên **Chung** tab trong **Tiền tệ** đồng ruộng.
- Xác minh đơn vị tiền tệ của công ty sở hữu. Bạn có thể xem tiền tệ bằng cách truy cập **Có liên quan** > **Sổ cái** trong hồ sơ công ty. Bấm đúp vào bản ghi sổ cái được liên kết với công ty và xác minh giá trị trên **Chung** tab trong **Đơn vị tiền tệ kế toán** đồng ruộng.

Nếu đơn vị tiền tệ được đặt trong đơn vị hợp đồng và bản ghi sổ cái không khớp, hãy điều chỉnh cấu hình hoặc chọn các giá trị khác nhau khi bạn lưu bản ghi. Hệ thống yêu cầu các bản ghi này phải khớp để đảm bảo các luồng lập hóa đơn liên công ty chính xác. Để biết thêm thông tin về cấu hình liên công ty, hãy xem [Tạo giao dịch liên công ty](../../project-accounting/create-intercompany-transactions.md).

Nếu bản ghi công ty không có bản ghi sổ cái liên quan, điều này cho thấy rằng có một cấu hình bị thiếu khi thiết lập môi trường. Cấu hình phải được sửa chữa bởi quản trị viên hệ thống. Người quản trị hệ thống phải đi đến **Cấu hình ghi kép** và dừng và khởi động lại **Bản đồ ghi kép sổ cái** với sự đồng bộ ban đầu của bản đồ này và đó là điều kiện tiên quyết. Để biết thêm thông tin, hãy xem [Các phiên bản ánh xạ ghi kép Project Operations](../../environment/resource-dual-write-maps.md).
