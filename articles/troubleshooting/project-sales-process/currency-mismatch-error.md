---
title: Lỗi không khớp đơn vị tiền tệ
description: Bài viết này cung cấp thông tin khắc phục sự cố về lỗi không khớp đơn vị tiền tệ xảy ra khi bạn lưu các loại bản ghi cụ thể.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5b0973a340dec8e68f326803d75bea9803e19791
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914750"
---
# <a name="currency-mismatch-error"></a>Lỗi không khớp đơn vị tiền tệ 

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Khi bạn lưu một dự án, hợp đồng, báo giá hoặc nguồn lực có thể đặt, bạn có thể nhận được lỗi **Công ty sở hữu hợp đồng dự án không khớp với tiền tệ của đơn vị hợp đồng. Hãy chọn một công ty sở hữu hoặc đơn vị hợp đồng khác để tiếp tục.** Điều này là do có sự không khớp về đơn vị tiền tệ giữa đơn vị tiền tệ của hợp đồng cho bản ghi và đơn vị tiền tệ của công ty sở hữu.


## <a name="resolution"></a>Cách giải quyết

Để khắc phục sự cố này, hãy làm theo cách sau:
- Xác minh đơn vị tiền tệ của đơn vị hợp đồng cho bản ghi này. Bạn có thể xem đơn vị tiền tệ bằng cách mở bản ghi đơn vị tổ chức và xác minh giá trị trên tab **Chung** trong trường **Đơn vị tiền tệ**.
- Xác minh đơn vị tiền tệ của công ty sở hữu. Bạn có thể xem đơn vị tiền tệ bằng cách truy cập **Có liên quan** > **Sổ cái** trong bản ghi công ty. Nhấp đúp vào bản ghi sổ cái được liên kết với công ty và xác minh giá trị trên tab **Chung** trong trường **Đơn vị tiền tệ kế toán**.

Nếu đơn vị tiền tệ được đặt trong đơn vị hợp đồng và bản ghi sổ cái không khớp, hãy điều chỉnh cấu hình hoặc chọn các giá trị khác nhau khi bạn lưu bản ghi. Hệ thống yêu cầu các bản ghi này phải khớp để đảm bảo các dòng lập hóa đơn liên công ty chính xác. Để biết thêm thông tin về cấu hình liên công ty, hãy xem [Tạo giao dịch liên công ty](../../project-accounting/create-intercompany-transactions.md).

Nếu bản ghi công ty không có bản ghi sổ cái được liên kết, điều này cho thấy rằng có một cấu hình bị thiếu khi thiết lập môi trường. Cấu hình phải được sửa chữa bởi quản trị viên hệ thống. Người quản trị hệ thống phải đi tới **Cấu hình ghi kép** rồi dừng và khởi động lại **Ánh xạ ghi kép sổ cái** với đồng bộ hóa ban đầu của ánh xạ này và các điều kiện tiên quyết của nó. Để biết thêm thông tin, hãy xem [Các phiên bản ánh xạ ghi kép Project Operations](../../environment/resource-dual-write-maps.md).
