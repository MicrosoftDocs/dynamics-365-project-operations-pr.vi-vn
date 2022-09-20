---
title: Tạo hóa đơn của nhà cung cấp
description: Bài viết này mô tả khái niệm về hóa đơn của nhà cung cấp và giải thích cách tạo chúng trong Microsoft Dynamics 365 Project Operations.
author: suvaidya
ms.date: 9/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 7f6c1ec46f23b6823734b28755b80ced4e3f9325
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475487"
---
# <a name="create-vendor-invoices"></a>Tạo hóa đơn của nhà cung cấp

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Để sử dụng chức năng được mô tả trong bài viết này, bạn phải bật **Cho phép xử lý các thủ tục hợp đồng phụ với Hoạt động dự án cho các tình huống dựa trên tài nguyên** tính năng trong **Quản lý tính năng** không gian làm việc.

Lập hóa đơn cho nhà cung cấp trong Microsoft Dynamics 365 Project Operations có thể được sử dụng để ghi lại chi phí từ việc cung cấp dịch vụ và / hoặc vật liệu cho một dự án được hoàn thành bởi các nhà cung cấp.

Khi các dịch vụ và / hoặc vật liệu được ký hợp đồng phụ cho một nhà cung cấp, một hợp đồng phụ thể hiện thỏa thuận hợp đồng với nhà cung cấp đó. Khi nhà cung cấp cung cấp các dịch vụ hoặc khi các vật liệu được nhận và sử dụng cho các nhiệm vụ của dự án, chi phí sẽ được ghi nhận vào dự án. Sau đó nhà cung cấp sẽ gửi hóa đơn theo định kỳ. Những hóa đơn đó được xác minh và khớp với chi phí được ghi nhận trên dự án. Sau khi quá trình xác minh hoàn tất, hóa đơn của nhà cung cấp được xác nhận và phát hành để thanh toán.

## <a name="scenarios-for-use"></a>Các tình huống sử dụng

Hóa đơn của nhà cung cấp trong Hoạt động Dự án có thể được sử dụng để hỗ trợ hai trường hợp riêng biệt:

- Khách hàng sử dụng các trải nghiệm hợp đồng phụ đầy đủ.
- Khách hàng không sử dụng toàn bộ trải nghiệm thầu phụ nhưng muốn có một cái nhìn thống nhất về chi phí của các dự án trong Hoạt động Dự án.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Khách hàng sử dụng toàn bộ trải nghiệm hợp đồng phụ

Trải nghiệm hóa đơn của nhà cung cấp cung cấp một cách để xác minh các mục thời gian, sử dụng vật liệu và các mục chi phí tham chiếu đến các thành phần được hợp đồng phụ và khớp chúng với các dòng hóa đơn của nhà cung cấp. Quy trình này có thể được sử dụng để xác minh tính chính xác của các dòng hóa đơn của nhà cung cấp. Sau khi quá trình xác minh hoàn tất và hóa đơn của nhà cung cấp được xác nhận, hệ thống sẽ đảo ngược các thực tế đã được ghi lại theo nhật ký sử dụng vật liệu, chi phí và thời gian đã được phê duyệt, sau đó tạo các thực tế chi phí mới bằng cách sử dụng các dòng hóa đơn của nhà cung cấp.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Khách hàng không sử dụng toàn bộ trải nghiệm thầu phụ nhưng muốn có cái nhìn thống nhất về chi phí của các dự án trong Hoạt động dự án

Nếu bạn đang theo dõi quy trình hợp đồng phụ trong hệ thống của bên thứ ba, bạn có thể ghi lại chi phí từ hệ thống của bên thứ ba đó vào Hoạt động dự án bằng cách tạo hóa đơn của nhà cung cấp không tham chiếu đến hợp đồng phụ. Bằng cách này, các nhà quản lý dự án của bạn có thể có một cái nhìn thống nhất, duy nhất về tất cả các chi phí trên một dự án nhất định.

## <a name="create-vendor-invoices-in-project-operations"></a>Tạo hóa đơn nhà cung cấp trong Hoạt động dự án

Hóa đơn của nhà cung cấp được tạo trong Dynamics 365 Finance, bằng cách sử dụng **Các khoản phải trả** mô-đun. Bạn không thể tạo hóa đơn của nhà cung cấp trực tiếp trong Dataverse.

### <a name="set-up-vendor-invoice-verification"></a>Thiết lập xác minh hóa đơn của nhà cung cấp

Nếu hóa đơn của nhà cung cấp được dành cho một hợp đồng phụ trong Dataverse, bạn phải kích hoạt **Xác minh thủ công bởi PM là bắt buộc** tham số. Cài đặt của tùy chọn xác định xem hóa đơn của nhà cung cấp có được xác nhận tự động trong Dataverse, hoặc liệu nó có yêu cầu xác nhận thủ công hay không. Tiêu đề của mọi hóa đơn của nhà cung cấp dự án bao gồm một tùy chọn có cùng tên. Theo mặc định, tùy chọn trên tiêu đề của tất cả các hóa đơn của nhà cung cấp dự án được đặt thành giá trị mà bạn đặt ở đây. Tuy nhiên, bạn có thể cập nhật giá trị theo yêu cầu trên tiêu đề của hóa đơn nhà cung cấp riêng lẻ.

Nếu tùy chọn được đặt thành **Đúng**, hóa đơn của nhà cung cấp được tạo trong Finance và được đồng bộ hóa với Dataverse có **Bản thảo** trạng thái. Sau đó, hóa đơn phải được người quản lý dự án xác nhận và xác nhận, đồng thời xác nhận trước khi nó được xử lý và đăng lên các tài khoản dự án và sổ cái cụ thể trong Tài chính.

Nếu tùy chọn được đặt thành **Không**, hóa đơn của nhà cung cấp được tự động xác nhận. Không có thêm hành động được yêu cầu.

Để thiết lập xác minh hóa đơn của nhà cung cấp, hãy làm theo các bước sau.

1. Trong Tài chính, hãy chuyển đến **Quản lý dự án và kế toán** \> **Thành lập** \> **Các thông số kế toán và quản lý dự án**.
1. Trên **Tài chính** tab, đặt **Xác minh thủ công bởi PM là bắt buộc** tùy chọn để **Đúng** nếu chính sách của công ty yêu cầu xác minh hóa đơn nhà thầu phụ của nhà cung cấp. Nếu sự xác minh của người quản lý dự án không được yêu cầu trong Dataverse, để lại bộ tùy chọn cho **Không**. Theo mặc định, cài đặt này sẽ được sử dụng trên **Hóa đơn của nhà cung cấp đang chờ xử lý** trang.

> [!NOTE]
> Hóa đơn của nhà cung cấp được tạo cho các hợp đồng phụ trong Dataverse chỉ có thể được xử lý chính xác nếu **Xác minh thủ công bởi PM là bắt buộc** tùy chọn được đặt thành **Đúng**. Các thông số về chi phí thời gian, vật liệu và chi phí mà nhà thầu phụ tạo ra có thể được người quản lý dự án đối sánh theo cách thủ công với các dòng hóa đơn của nhà cung cấp nếu tùy chọn này được đặt thành **Đúng**.

### <a name="set-up-a-procurement-integration-account-for-vendor-invoices"></a>Thiết lập tài khoản tích hợp mua sắm cho các hóa đơn của nhà cung cấp

Khi hóa đơn của nhà cung cấp được đăng trong Tài chính cho Hoạt động Dự án - Môi trường tích hợp (không phải chứng khoán), các khoản tài chính sẽ được đăng vào tài khoản tích hợp Mua sắm. Hệ thống tạo ra các thực tế trong Dataverse cho hóa đơn đã đăng. Các tài liệu thực tế này được đăng trên tạp chí Tài chính bằng cách sử dụng tạp chí tích hợp Dự án. Đăng tạp chí Tích hợp dự án đăng chi phí thực tế và hoàn nhập tài khoản tích hợp Mua sắm.

Để thiết lập tài khoản tích hợp Mua sắm cho các hóa đơn của nhà cung cấp, hãy làm theo các bước sau.

1. Trong Tài chính, hãy chuyển đến **Quản lý dự án và kế toán** \> **Thành lập** \> **Các thông số kế toán và quản lý dự án**.
1. Trên **Dự án hoạt động trên Dynamics 365 tương tác với khách hàng** tab, chọn **Vật liệu** \> **Tài khoản tích hợp mua sắm**.

### <a name="create-and-post-subcontract-vendor-invoices"></a>Tạo và đăng hóa đơn nhà cung cấp hợp đồng phụ

Khi nhân viên Kế toán phải trả nhận được hóa đơn từ nhà thầu phụ, một hóa đơn mới sẽ được tạo trong Tài chính.

1. Trong Tài chính, hãy chuyển đến **Các khoản phải trả** \> **Hóa đơn** \> **Hóa đơn của nhà cung cấp đang chờ xử lý**.
1. Trên **Ngăn hành động**, lựa chọn **Mới** để tạo hóa đơn nhà cung cấp.
1. Trên tiêu đề hóa đơn, trong **Tài khoản hóa đơn** trường, chọn **Nhà thầu phụ**.
1. Chọn ngày lập hóa đơn.
1. Trên **Tiêu đề** tab, đặt **Xác minh thủ công bởi PM là bắt buộc** tùy chọn để **Đúng**. Cài đặt mặc định của tùy chọn này đến từ **Quản lý dự án và các thông số kế toán** trang. Tuy nhiên, nó có thể được thay đổi ở cấp hóa đơn của nhà cung cấp.
1. Trên **Dòng hóa đơn** FastTab, chọn **Thêm dòng** để tạo một dòng hóa đơn của nhà cung cấp.
1. Chọn danh mục mua sắm đã được tạo cho các dây chuyền thầu phụ và nhập đơn giá, đơn vị đo lường và số lượng.
1. Trong phần dòng hóa đơn của nhà cung cấp, trên **Dự án**, chọn dự án mà nhà thầu phụ chia sẻ hóa đơn hợp đồng phụ.
1. Chọn danh mục dự án. Nó có thể thuộc bất kỳ loại nào **Mục**, **phí**, **liệu**, hoặc **Giờ**.
1. Chỉ chọn vai trò nếu danh mục dự án đã chọn thuộc **Giờ** loại hình.
1. Lựa chọn **Bưu kiện** để đăng hóa đơn của nhà cung cấp.

Ngoài ra, bạn có thể tạo hóa đơn của nhà cung cấp bằng cách truy cập **Các khoản phải trả** \> **Hóa đơn** \> **Mở hóa đơn của nhà cung cấp** và lựa chọn **Mới**.

Khi hóa đơn của nhà cung cấp được đăng, nó sẽ có sẵn trong Dataverse để quản lý dự án xác minh và xử lý.

## <a name="vendor-invoice-processing-in-dataverse"></a>Xử lý hóa đơn của nhà cung cấp trong Dataverse

Trong hóa đơn của nhà cung cấp được tạo trong Dataverse, một số giá trị trường đến từ hóa đơn của nhà cung cấp được ghi trong Tài chính. Các giá trị khác là giá trị mặc định đến từ hợp đồng phụ.

Các trường sau đây và các bản ghi liên quan sẽ được sao chép từ hợp đồng phụ sang tiêu đề của hóa đơn nhà cung cấp:

- Tiền tệ
- Đơn vị hợp đồng
- Điều khoản thanh toán

Trên các dòng hóa đơn của nhà cung cấp, Hoạt động dự án sử dụng các giá trị trường sau để nhập tham chiếu dòng hợp đồng phụ và hợp đồng phụ mặc định:

- Lớp giao dịch
- Vai trò
- Thể loại giao dịch
- Các lĩnh vực sản phẩm
- Dự án
- Tác vụ

> [!NOTE]
> Dòng hợp đồng phụ giá cố định không được hỗ trợ trong Hoạt động dự án.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
