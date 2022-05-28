---
title: Lập hóa đơn cho nhà cung cấp - Khái niệm và sáng tạo
description: Chủ đề này mô tả khái niệm về hóa đơn của nhà cung cấp, các tình huống sử dụng và cách tạo hóa đơn của nhà cung cấp trong Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: dc9b3954b237294f52aa0bb74f8008a5dfdf78fd
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580574"
---
# <a name="vendor-invoicing---concept-and-creation"></a>Lập hóa đơn cho nhà cung cấp - Khái niệm và sáng tạo

[!include [banner](../../includes/dataverse-preview.md)]

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Lập hóa đơn cho nhà cung cấp trong Microsoft Dynamics 365 Project Operations có thể được sử dụng để ghi lại chi phí từ việc cung cấp dịch vụ và / hoặc vật liệu cho một dự án của các nhà cung cấp.

Khi các dịch vụ và / hoặc vật liệu được ký hợp đồng phụ cho một nhà cung cấp, một hợp đồng phụ thể hiện thỏa thuận hợp đồng với nhà cung cấp đó. Khi nhà cung cấp cung cấp các dịch vụ, hoặc các vật liệu được nhận và sử dụng cho các nhiệm vụ của dự án, chi phí sẽ được ghi nhận vào dự án. Định kỳ, nhà cung cấp gửi các hóa đơn đã được xác minh và khớp với các chi phí được ghi nhận trên dự án. Sau khi quá trình xác minh hoàn tất, hóa đơn của nhà cung cấp được xác nhận và phát hành để thanh toán.

## <a name="scenarios-for-use"></a>Các tình huống sử dụng

Hóa đơn của nhà cung cấp trong Hoạt động Dự án có thể được sử dụng để hỗ trợ hai trường hợp riêng biệt.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Khách hàng sử dụng toàn bộ trải nghiệm hợp đồng phụ

Trải nghiệm hóa đơn của nhà cung cấp cung cấp một cách để xác minh và khớp các mục thời gian, sử dụng vật liệu và các mục chi phí tham chiếu các thành phần được hợp đồng phụ với các dòng hóa đơn của nhà cung cấp. Quy trình này có thể được sử dụng để xác minh tính chính xác của các dòng hóa đơn của nhà cung cấp. Sau khi quá trình xác minh hoàn tất và hóa đơn của nhà cung cấp được xác nhận, ứng dụng sẽ đảo ngược các thực tế đã được ghi lại theo nhật ký sử dụng vật liệu, chi phí và thời gian đã được phê duyệt, đồng thời tạo các thực tế chi phí mới bằng cách sử dụng các dòng hóa đơn của nhà cung cấp.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Khách hàng không sử dụng toàn bộ trải nghiệm thầu phụ nhưng muốn có cái nhìn thống nhất về chi phí của các dự án trong Hoạt động dự án

Nếu bạn đang theo dõi quy trình hợp đồng phụ trong hệ thống của bên thứ ba, bạn có thể ghi lại chi phí từ hệ thống của bên thứ ba đó vào Hoạt động dự án bằng cách tạo hóa đơn của nhà cung cấp không tham chiếu đến hợp đồng phụ. Bằng cách này, các nhà quản lý dự án của bạn có thể có cái nhìn thống nhất, duy nhất về tất cả các chi phí trên một dự án nhất định.

## <a name="creation-of-vendor-invoices-in-project-operations"></a>Tạo hóa đơn nhà cung cấp trong Hoạt động dự án

Hóa đơn của nhà cung cấp có thể được tạo theo hai cách:

- Từ trang danh sách hóa đơn của nhà cung cấp hoặc trang chi tiết cho một hóa đơn của nhà cung cấp
- Từ trang danh sách hợp đồng phụ hoặc trang chi tiết cho một hợp đồng phụ duy nhất

### <a name="creation-from-the-vendor-invoice-list-page-or-details-page"></a>Tạo từ trang danh sách hóa đơn của nhà cung cấp hoặc trang chi tiết

1. Đi đến **Thu mua** \> **Hóa đơn của nhà cung cấp**.
2. Trên trang danh sách hóa đơn của nhà cung cấp hoặc trang chi tiết cho một hóa đơn của nhà cung cấp, hãy chọn **Mới mẻ** để tạo một hóa đơn nhà cung cấp mới.

Hóa đơn của nhà cung cấp được tạo theo cách này cũng có thể tham chiếu đến hợp đồng phụ.

### <a name="creation-from-the-subcontract-list-page-or-details-page"></a>Tạo từ trang danh sách hợp đồng phụ hoặc trang chi tiết

1. Đi đến **Thu mua** \> **Hợp đồng phụ**.
2. Chọn một hoặc nhiều hợp đồng phụ.
3. Trên trang danh sách hợp đồng phụ hoặc trang chi tiết cho một hợp đồng phụ, hãy chọn **Tạo hóa đơn của nhà cung cấp** để tạo một hóa đơn nhà cung cấp mới.

Một hóa đơn nhà cung cấp mới trong **Bản thảo** trạng thái được tạo cho mỗi hợp đồng phụ mà bạn đã chọn.

Hóa đơn của nhà cung cấp mà bạn tạo theo cách này luôn tham chiếu đến hợp đồng phụ trên tiêu đề hóa đơn của nhà cung cấp. Mỗi dòng trên hợp đồng phụ có Phương thức thanh toán theo thời gian và vật chất sẽ tạo ra một dòng trên hóa đơn của nhà cung cấp. Mỗi dòng trên hợp đồng phụ có phương thức thanh toán Giá cố định sẽ tạo ra một dòng trên hóa đơn của nhà cung cấp cho mỗi mốc dòng của hợp đồng phụ có trạng thái **Sẵn sàng xuất hóa đơn**.

Các trường sau đây và các bản ghi liên quan sẽ được sao chép từ hợp đồng phụ sang tiêu đề của hóa đơn nhà cung cấp:

- Người bán.
- Bảng giá liên quan sẽ được sao chép vào hóa đơn của nhà cung cấp dưới dạng bảng giá.
- Tiền tệ.
- Đơn vị ký hợp đồng.
- Điều khoản thanh toán.

Đối với dòng hợp đồng phụ Thời gian và vật chất, các trường sau đây và các bản ghi liên quan sẽ được sao chép từ dòng hợp đồng phụ sang dòng hóa đơn của nhà cung cấp:

- Hợp đồng phụ và tham chiếu dòng hợp đồng phụ
- Lớp giao dịch
- Vai trò
- Thể loại giao dịch
- Lĩnh vực sản phẩm
- Dự án
- Tác vụ
- Nguồn lực có thể đặt trước

Đối với dòng hợp đồng phụ giá cố định, các trường sau sẽ được sao chép từ dòng hợp đồng phụ và mốc dòng hợp đồng phụ sang dòng hóa đơn của nhà cung cấp:

- Hợp đồng phụ và tham chiếu dòng hợp đồng phụ.
- Lớp giao dịch. Theo mặc định, giá trị sẽ là **Cột mốc**.
- Tên cột mốc và số tiền sẽ được sao chép từ cột mốc của dòng hợp đồng phụ liên quan.
- Người dùng sẽ có thể chọn một dự án và nhiệm vụ trên dòng hóa đơn của nhà cung cấp.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
