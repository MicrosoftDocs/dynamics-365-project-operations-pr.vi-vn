---
title: Thiết lập nhà thầu phụ làm nguồn lực có thể đặt trước
description: Bài viết này giải thích cách thiết lập và duy trì tài nguyên nhà thầu phụ được tạo từ người dùng và địa chỉ liên hệ trong hệ thống để chúng có thể được liên kết với hợp đồng phụ trong Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 07/28/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 67df514cd1a0bd07d4ff2582e1a7738d913e0ac5
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261350"
---
# <a name="set-up-subcontractors-as-bookable-resources"></a>Thiết lập nhà thầu phụ làm nguồn lực có thể đặt trước

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Hãy làm theo các bước sau để thiết lập nhà thầu phụ làm tài nguyên có thể đặt trước trong Microsoft Dynamics 365 Project Operations.

1. Truy cập **Dự án** \> **Nguồn lực**, rồi chọn **Mới**.
2. Trên trang **Nguồn lực mới có thể đặt trước**, trong trường **Loại nguồn lực**, hãy chọn một trong các tùy chọn sau:

    - **Người dùng** – Chọn loại tài nguyên này nếu nhà thầu phụ phải truy cập vào Project Operations để nhập thời gian hoặc chi phí. Nếu bạn chọn **Người dùng**, nhà thầu phụ yêu cầu giấy phép hợp lệ để truy cập hệ thống.
    - **Người liên hệ** hoặc **Tài khoản** – Chọn một trong các loại nguồn lực này nếu nhà thầu phụ không yêu cầu quyền truy cập vào Project Operations, nhưng phải sẵn sàng để giao nhiệm vụ hoặc đặt chỗ cho các dự án. Cả hai loại nguồn lực này đều không cung cấp quyền truy cập vào hệ thống. Chọn **Tài khoản** đại diện cho công ty của nhà cung cấp dưới dạng một tài nguyên có thể đặt trước. Chọn **Người liên hệ** đại diện cho từng nhân viên của nhà cung cấp.

3. Tùy thuộc vào loại nguồn lực đã chọn, bạn sẽ được nhắc chọn người dùng, tài khoản hoặc bản ghi liên hệ tương ứng.
4. Trong trường **Loại nhân viên**, hãy chọn "Nhân viên hợp đồng" để thiết lập nhà thầu phụ làm nguồn lực có thể đặt trước.

    > [!NOTE]
    > Nếu bạn để trống trường **Loại nhân viên**, tài nguyên có thể đặt trước sẽ được coi là nhân viên.

5. Nếu bạn chọn **Nhân viên hợp đồng** với tư cách là loại nhân viên, hãy chọn nhà cung cấp mà nguồn lực đó làm việc cho.
6. Chọn múi giờ của nguồn lực, sau đó chọn **Lưu**. Để chỉ định mẫu giờ làm việc cho nguồn lực có thể đặt trước, bạn có thể chọn **Đặt lịch** trên trang danh sách **Nguồn lực có thể đặt trước**.

Để được liên kết với một mô tả hợp đồng phụ, một nguồn lực có thể đặt trước phải đáp ứng các điều kiện sau:

- Tài nguyên có thể đặt trước phải là nhân viên hợp đồng.
- Một nguồn lực có thể đặt trước của loại nguồn lực **Liên hệ** phải được liên kết với tài khoản nhà cung cấp dưới dạng địa chỉ liên hệ. Không phải liên kết một nguồn lực có thể đặt trước của loại nguồn lực **Người dùng** với tài khoản nhà cung cấp dưới dạng địa chỉ liên hệ.
- Giá trị của trường **Nhà cung cấp** cho tài nguyên có thể đặt trước phải khớp với giá trị của trường **Nhà cung cấp** cho hợp đồng phụ.

## <a name="update-the-type-of-worker-and-vendor-mapping-for-bookable-resources"></a>Cập nhật loại ánh xạ công nhân và nhà cung cấp cho các nguồn lực có thể đặt trước

Trường **Loại nhân viên** cho tài nguyên có thể đặt trước sẽ xác định xem nguồn lực có thể đặt trước là nhân viên hợp đồng hay nhân viên. Trường **Nhà cung cấp** xác định tài khoản nhà cung cấp mà nguồn lực có thể đặt trước được liên kết. Bằng cách liên kết nguồn lực có thể đặt trước với một nhà cung cấp làm địa chỉ liên hệ, bạn cho biết rằng người liên hệ là nhân viên của công ty nhà cung cấp.

Nếu thay đổi trường **Loại nhân viên** và **Nhà cung cấp** cho nguồn lực có thể đặt trước, các thay đổi đó sẽ ảnh hưởng đến bất kỳ nội dung xác nhận nào trong tương lai trên các bản ghi mới mà nguồn lực có thể đặt trước được tạo ra, chẳng hạn như các mục thời gian. Tuy nhiên, các thay đổi đó không làm mất hiệu lực các bản ghi hiện có.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
