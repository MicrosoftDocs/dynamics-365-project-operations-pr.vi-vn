---
title: Tổng quan về giữ chân nhà cung cấp
description: Bài viết này cung cấp một cái nhìn tổng quan về khả năng giữ chân nhà cung cấp.
author: sigitac
ms.date: 10/01/2021
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 680786f239125905f3b8746cb8318732aa74d9e0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916866"
---
# <a name="vendor-retention-overview"></a>Tổng quan về giữ chân nhà cung cấp

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Tổ chức của bạn có thể muốn giữ lại một phần thanh toán cho các nhà cung cấp làm việc trong các dự án cho tổ chức của bạn. Ví dụ: trước khi thanh toán cho nhà cung cấp, bạn có thể muốn đảm bảo rằng các mặt hàng và dịch vụ mà họ cung cấp đáp ứng mong đợi của bạn.

Khi bạn thương lượng mua hàng cho các dự án với nhà cung cấp, bạn có thể chỉ định các điều khoản giữ chân nhà cung cấp bao gồm tỷ lệ phần trăm hoặc số tiền cần giữ lại. Khi nhà cung cấp phân phối các mặt hàng và dịch vụ, bạn sẽ khấu trừ phần trăm hoặc số tiền giữ lại được chỉ định từ khoản thanh toán của bạn cho nhà cung cấp. Khi dự án hoàn thành hoặc đạt đến giai đoạn tạm thời như được chỉ định trong hợp đồng nhà cung cấp, bạn giải ngân số tiền giữ lại và tạo khoản thanh toán cho nhà cung cấp.

## <a name="vendor-retention-example"></a>Ví dụ về giữ chân nhà cung cấp

Ví dụ sau đây cho thấy tỷ lệ phần trăm số tiền trong hóa đơn của nhà cung cấp được giữ lại dựa trên tỷ lệ phần trăm hoàn thành cho một dự án.

Contoso Robotics USA đã ký hợp đồng với nhà cung cấp Fabrikam để cung cấp 100 giờ đào tạo cho dự án đổi mới thiết bị. Tổng giá trị hợp đồng là 30.000 USD với giá mua thỏa thuận là 300 USD mỗi giờ.

Việc đào tạo sẽ được thực hiện trong ba giai đoạn với lịch trình như sau:

- Giai đoạn 1: 50 giờ hoặc 50% của dự án
- Giai đoạn 2: 30 giờ hoặc tổng cộng 80% của dự án
- Giai đoạn 3: 20 giờ hoặc 100% của dự án

Bảng sau liệt kê các điều khoản giữ chân.

| **Phần trăm đơn vị được giao** | **Phần trăm giữ lại** | **Phần trăm giải ngân** |
| --- | --- | --- |
| 50% | 20% | 0% |
| 80% | 10% | 10% |
| 100% | 0% | 100% |

Các giao dịch dẫn đến số tiền sau:

- Giai đoạn 1:
  - Số tiền phải trả là 50 x 300 hoặc 15.000.
  - 20% của số tiền, hoặc 3.000, được giữ lại và sẽ được giải ngân ở giai đoạn sau.
  - Số tiền được trả cho nhà cung cấp là 12.000.
- Giai đoạn 2:
  - Số tiền phải trả là 30 x 300 hoặc 9.000.
  - 10% của số tiền hoặc 900, được giữ lại.
  - 10% trong số 3.000 được giữ lại trong Giai đoạn 1 hoặc 300 được giải ngân.
  - Số tiền được trả cho nhà cung cấp là 8.400. Số tiền này ít hơn 9.000 so với 900 tiền giữ lại với 300 đã được giải ngân từ phần giữ lại của Giai đoạn 1.
- Giai đoạn 3:
  - Số tiền phải trả là 20 x 300 hoặc 6.000.
  - Không có số tiền nào được giữ lại.
  - Số tiền được giải ngân là 3.600. Số tiền này bao gồm 3.000 được giữ lại trong Giai đoạn 1, ít hơn 300 từ Giai đoạn 1 đã được giải ngân trong Giai đoạn 2, cộng với 900 được giữ lại trong Giai đoạn 2.
  - Số tiền được trả cho nhà cung cấp là 9.600. Số tiền này bao gồm số tiền giữ lại là 3.600 cộng với 6.000 để hoàn thành Giai đoạn 3.

Tổng số tiền phải trả cho nhà cung cấp sau khi ba giai đoạn hoàn tất là 30.000, là tổng số tiền của đơn đặt hàng (15.000 + 9.000 + 6.000).
