---
title: Tổng quan về lập hóa đơn liên công ty
description: Chủ đề này cung cấp thông tin và ví dụ về cách lập hóa đơn liên công ty cho các dự án.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 3ad75089de1a2f99646f7aba213e199a2bec347d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287354"
---
# <a name="intercompany-invoicing-overview"></a>Tổng quan về lập hóa đơn liên công ty

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Tổ chức của bạn có thể có nhiều bộ phận, công ty con và pháp nhân khác chuyển sản phẩm và dịch vụ cho nhau trong các dự án. Pháp nhân cung cấp sản phẩm hoặc dịch vụ được gọi là *pháp nhân cho thuê*. Pháp nhân nhận sản phẩm hoặc dịch vụ được gọi là *pháp nhân đi thuê*.

Hình sau minh họa trường hợp thường gặp, đó là khi Contoso Robotics USA (pháp nhân đi thuê) và Contoso Robotics UK (pháp nhân cho thuê) chia sẻ nguồn lực để thực hiện dự án cho khách hàng Adventure Works. Trong tình huống này, Contoso Robotics USA đã ký hợp đồng thực hiện công việc cho Adventure Works.

![Lập hóa đơn liên công ty](./media/IntercompanyScenario.png) 

Dynamics 365 Project Operations dùng quy trình sau để xử lý các giao dịch liên công ty:

1. Nguồn lực của pháp nhân cho thuê ghi lại các giao dịch thời gian hoặc chi phí liên công ty bằng cách đăng ký thời gian và chi phí đối với các dự án trong pháp nhân đi thuê.
2. Giá thời gian và chi phí được ghi lại trong công ty cho thuê bằng cách dùng bảng giá chi phí đơn vị của công ty đi thuê.
3. Giao dịch bán hàng liên công ty chưa thanh toán được ghi lại trong công ty cho thuê bằng cách dùng bảng giá chi phí đơn vị của công ty đi thuê.
4. Doanh thu chưa thanh toán được ghi lại trong công ty đi thuê bằng cách dùng bảng giá bán hàng theo hợp đồng dự án. Khách hàng có thể được lập hóa đơn khi doanh thu chưa thanh toán được ghi lại. Khách hàng không phải đợi đến khi quy trình xử lý hóa đơn liên công ty hoàn tất.
5. Hóa đơn khách hàng liên công ty được tạo theo định kỳ trong công ty cho thuê. Các hóa đơn được tạo theo cách thủ công hoặc bằng cách dùng quy trình tự động hóa theo định kỳ. Bạn có thể tạo một hóa đơn riêng lẻ cho từng pháp nhân đi thuê hoặc tạo các hóa đơn tách biệt theo dự án.
6. Khi hóa đơn khách hàng liên công ty được đăng trong pháp nhân cho thuê, hóa đơn nhà cung cấp tương ứng đang ở trạng thái chờ xử lý sẽ được tạo trong pháp nhân đi thuê. Các chi phí trong hóa đơn nhà cung cấp đang chờ xử lý sẽ được ghi lại vào sổ cái phụ của dự án khi hóa đơn đó được đăng.

Sơ đồ sau minh họa quy trình lập hóa đơn liên công ty vì quy trình này có liên quan đến các sự kiện kế toán và những lần đăng dự kiến vào sổ cái chung.

![Quy trình liên công ty](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a>Tài nguyên bổ sung

- [Đặt cấu hình hoạt động lập hóa đơn liên công ty](configure-intercompany-invoicing.md)
- [Ghi lại giao dịch liên công ty](create-intercompany-transactions.md)
- [Lập hóa đơn cho nhà cung cấp và khách hàng liên công ty](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]