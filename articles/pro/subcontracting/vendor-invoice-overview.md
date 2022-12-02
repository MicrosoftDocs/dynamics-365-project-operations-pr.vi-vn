---
title: Lập hóa đơn cho nhà cung cấp – Khái niệm và tạo
description: Bài viết này mô tả khái niệm về hóa đơn của nhà cung cấp, trường hợp sử dụng và cách tạo hóa đơn của nhà cung cấp trong Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b57ec8cdb6097e6f2207056667aadfb43ee8acfc
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261970"
---
# <a name="vendor-invoicing---concept-and-creation"></a>Lập hóa đơn cho nhà cung cấp – Khái niệm và tạo

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Lập hóa đơn nhà cung cấp trong Microsoft Dynamics 365 Project Operations có thể được sử dụng để ghi lại chi phí từ việc cung cấp dịch vụ và/hoặc vật tư trên một dự án của nhà cung cấp.

Khi các dịch vụ và/hoặc vật liệu được ký hợp đồng phụ cho một nhà cung cấp, một hợp đồng phụ thể hiện thỏa thuận hợp đồng với nhà cung cấp đó. Khi nhà cung cấp cung cấp các dịch vụ hoặc các vật tư được nhận và sử dụng cho các nhiệm vụ dự án, chi phí sẽ được ghi nhận vào dự án. Theo định kỳ, nhà cung cấp gửi các hóa đơn được xác minh và khớp với các chi phí được ghi nhận trên dự án. Sau khi quá trình xác minh hoàn tất, hóa đơn của nhà cung cấp được xác nhận và phát hành để thanh toán.

## <a name="scenarios-for-use"></a>Trường hợp sử dụng

Hóa đơn của nhà cung cấp trong Project Operations có thể được sử dụng để hỗ trợ hai trường hợp riêng biệt.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Khách hàng sử dụng các trải nghiệm hợp đồng phụ đầy đủ

Trải nghiệm hóa đơn của nhà cung cấp mang lại một cách để xác minh và khớp các mục thời gian, sử dụng vật tư và các mục chi phí tham chiếu đến các thành phần hợp đồng phụ với các mô tả hóa đơn của nhà cung cấp. Quy trình này có thể được sử dụng để xác minh tính chính xác của mô tả hóa đơn của nhà cung cấp. Sau khi quá trình xác minh hoàn tất và hóa đơn của nhà cung cấp được xác nhận, ứng dụng sẽ đảo ngược các số liệu thực tế đã được ghi lại theo nhật ký thời gian, chi phí và sử dụng vật tư đã được phê duyệt, sau đó tạo các số liệu thực tế chi phí mới bằng cách sử dụng mô tả hóa đơn của nhà cung cấp.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Khách hàng không sử dụng toàn bộ trải nghiệm hợp đồng phụ nhưng muốn có một cái nhìn thống nhất về chi phí của các dự án trong Project Operations

Nếu bạn đang theo dõi quy trình hợp đồng phụ trong hệ thống của bên thứ ba, bạn có thể ghi lại chi phí từ hệ thống của bên thứ ba đó vào Project Operations bằng cách tạo hóa đơn của nhà cung cấp không tham chiếu đến hợp đồng phụ. Bằng cách này, người quản lý dự án của bạn có thể có một cái nhìn thống nhất, duy nhất về tất cả các chi phí trên một dự án nhất định.

## <a name="creation-of-vendor-invoices-in-project-operations"></a>Tạo hóa đơn nhà cung cấp trong Project Operations

Có thể tạo hóa đơn nhà cung cấp theo hai cách:

- Từ trang danh sách hóa đơn của nhà cung cấp hoặc trang chi tiết cho một hóa đơn của nhà cung cấp
- Từ trang danh sách hợp đồng phụ hoặc trang chi tiết cho một hợp đồng phụ duy nhất

### <a name="creation-from-the-vendor-invoice-list-page-or-details-page"></a>Tạo từ trang danh sách hóa đơn của nhà cung cấp hoặc trang chi tiết

1. Đi đến **Mua** \> **Hóa đơn của nhà cung cấp**.
2. Trên trang danh sách hóa đơn của nhà cung cấp hoặc trang chi tiết cho một hóa đơn của nhà cung cấp, hãy chọn **Mới** để tạo một hóa đơn nhà cung cấp mới.

Hóa đơn của nhà cung cấp được tạo theo cách này cũng có thể tham chiếu đến hợp đồng phụ.

### <a name="creation-from-the-subcontract-list-page-or-details-page"></a>Tạo từ trang danh sách hợp đồng phụ hoặc trang chi tiết

1. Đi đến **Mua** \> **Hợp đồng phụ**.
2. Chọn một hoặc nhiều hợp đồng phụ.
3. Trên trang danh sách hợp đồng phụ hoặc trang chi tiết cho một hợp đồng phụ, chọn **Tạo hóa đơn của nhà cung cấp** để tạo hóa đơn của nhà cung cấp mới.

Một hóa đơn của nhà cung cấp mới ở trạng thái **Bản nháp** được tạo cho mỗi hợp đồng phụ mà bạn đã chọn.

Hóa đơn của nhà cung cấp mà bạn tạo theo cách này luôn tham chiếu đến hợp đồng phụ trên tiêu đề hóa đơn của nhà cung cấp. Mỗi dòng trên hợp đồng phụ có phương thức thanh toán theo Thời gian và vật tư sẽ tạo ra một mô tả trên hóa đơn của nhà cung cấp. Mỗi mô tả trên hợp đồng phụ có phương thức thanh toán Giá cố định sẽ tạo ra một dòng mô tả trên hóa đơn của nhà cung cấp cho mỗi mốc mô tả hợp đồng phụ có trạng thái **Sẵn sàng lập hóa đơn**.

Các trường sau đây và các bản ghi liên quan sẽ được sao chép từ hợp đồng phụ sang tiêu đề của hóa đơn của nhà cung cấp:

- Nhà cung cấp.
- Bảng giá liên quan sẽ được sao chép vào hóa đơn của nhà cung cấp dưới dạng bảng giá.
- Tiền tệ.
- Đơn vị theo hợp đồng.
- Điều khoản thanh toán.

Đối với mô tả hợp đồng phụ Thời gian và vật tư, các trường sau đây và các bản ghi liên quan sẽ được sao chép từ mô tả hợp đồng phụ sang mô tả hóa đơn của nhà cung cấp:

- Tham chiếu hợp đồng phụ và mô tả hợp đồng phụ
- Lớp giao dịch
- Vai trò
- Thể loại giao dịch
- Trường sản phẩm
- Dự án
- Tác vụ
- Nguồn lực có thể đặt trước

Đối với mô tả hợp đồng phụ Giá cố định, các trường sau đây sẽ được sao chép từ mô tả hợp đồng phụ và mốc mô tả hợp đồng phụ sang mô tả hóa đơn của nhà cung cấp:

- Tham chiếu hợp đồng phụ và mô tả hợp đồng phụ.
- Lớp giao dịch. Theo mặc định, giá trị sẽ là **Mốc**.
- Tên mốc và số tiền sẽ được sao chép từ mốc mô tả hợp đồng phụ có liên quan.
- Người dùng sẽ có thể chọn một dự án và nhiệm vụ trên mô tả hóa đơn của nhà cung cấp.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
