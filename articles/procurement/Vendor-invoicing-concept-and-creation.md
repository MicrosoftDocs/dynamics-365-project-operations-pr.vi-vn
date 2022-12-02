---
title: Tạo hóa đơn của nhà cung cấp
description: Bài viết này mô tả khái niệm về hóa đơn của cung cấp và giải thích cách tạo chúng trong Microsoft Dynamics 365 Project Operations.
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

Để sử dụng chức năng được mô tả trong bài viết này, bạn phải bật tính năng **Cho phép xử lý các số liệu thực tế với Project Operations cho trường hợp dựa trên nguồn lực** trong không gian làm việc **Quản lý tính năng**.

Lập hóa đơn nhà cung cấp trong Microsoft Dynamics 365 Project Operations có thể được sử dụng để ghi lại chi phí từ việc cung cấp dịch vụ và/hoặc vật tư cho một dự án được hoàn thành bởi nhà cung cấp.

Khi các dịch vụ và/hoặc vật liệu được ký hợp đồng phụ cho một nhà cung cấp, một hợp đồng phụ thể hiện thỏa thuận hợp đồng với nhà cung cấp đó. Khi nhà cung cấp cung cấp các dịch vụ hoặc khi các vật tư được nhận và sử dụng cho các nhiệm vụ dự án, chi phí sẽ được ghi nhận vào dự án. Sau đó, nhà cung cấp sẽ gửi hóa đơn theo định kỳ. Những hóa đơn đó được xác minh và khớp với các chi phí được ghi nhận trên dự án. Sau khi quá trình xác minh hoàn tất, hóa đơn của nhà cung cấp được xác nhận và phát hành để thanh toán.

## <a name="scenarios-for-use"></a>Trường hợp sử dụng

Hóa đơn của nhà cung cấp trong Project Operations có thể được sử dụng để hỗ trợ hai trường hợp riêng biệt:

- Khách hàng sử dụng các trải nghiệm hợp đồng phụ đầy đủ.
- Khách hàng không sử dụng toàn bộ trải nghiệm hợp đồng phụ nhưng muốn có một cái nhìn thống nhất về chi phí của các dự án trong Project Operations.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Khách hàng sử dụng các trải nghiệm hợp đồng phụ đầy đủ

Trải nghiệm hóa đơn của nhà cung cấp mang lại một cách để xác minh các mục thời gian, sử dụng vật tư và các mục chi phí tham chiếu đến các thành phần hợp đồng phụ, đồng thời khớp chúng với các mô tả hóa đơn của nhà cung cấp. Quy trình này có thể được sử dụng để xác minh tính chính xác của mô tả hóa đơn của nhà cung cấp. Sau khi quá trình xác minh hoàn tất và hóa đơn của nhà cung cấp được xác nhận, hệ thống sẽ đảo ngược các số liệu thực tế đã được ghi lại theo nhật ký thời gian, chi phí và sử dụng vật tư đã được phê duyệt, sau đó tạo các số liệu thực tế chi phí mới bằng cách sử dụng mô tả hóa đơn của nhà cung cấp.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Khách hàng không sử dụng toàn bộ trải nghiệm hợp đồng phụ nhưng muốn có một cái nhìn thống nhất về chi phí của các dự án trong Project Operations

Nếu bạn đang theo dõi quy trình hợp đồng phụ trong hệ thống của bên thứ ba, bạn có thể ghi lại chi phí từ hệ thống của bên thứ ba đó vào Project Operations bằng cách tạo hóa đơn của nhà cung cấp không tham chiếu đến hợp đồng phụ. Bằng cách này, người quản lý dự án của bạn có thể có một cái nhìn thống nhất, duy nhất về tất cả các chi phí trên một dự án nhất định.

## <a name="create-vendor-invoices-in-project-operations"></a>Tạo hóa đơn nhà cung cấp trong Project Operations

Hóa đơn nhà cung cấp được tạo trong Dynamics 365 Finance, bằng cách sử dụng mô-đun **Khoản phải trả**. Bạn không thể tạo hóa đơn nhà cung cấp trực tiếp trong Dataverse.

### <a name="set-up-vendor-invoice-verification"></a>Thiết lập xác minh hóa đơn nhà cung cấp

Nếu hóa đơn nhà cung cấp được dành cho một hợp đồng phụ trong Dataverse, bạn phải kích hoạt tham số **Bắt buộc phải có xác minh thủ công của PM**. Cài đặt của tùy chọn xác định xem hóa đơn của nhà cung cấp có được xác nhận tự động trong Dataverse không, hoặc liệu nó có yêu cầu xác nhận thủ công hay không. Tiêu đề của mọi hóa đơn nhà cung cấp của dự án bao gồm một tùy chọn có cùng tên. Theo mặc định, tùy chọn trên tiêu đề của tất cả các hóa đơn nhà cung cấp của dự án được đặt thành giá trị mà bạn đặt ở đây. Tuy nhiên, bạn có thể cập nhật giá trị theo yêu cầu trên tiêu đề của hóa đơn nhà cung cấp riêng lẻ.

Nếu tùy chọn được đặt thành **Có**, hóa đơn nhà cung cấp được tạo trong Finance và được đồng bộ hóa với Dataverse có trạng thái **Bản nháp**. Sau đó, hóa đơn phải được xác thực và xác minh bởi người quản lý dự án, cũng như được xác nhận trước khi nó được xử lý và đăng lên dự án và sổ cái cụ thể trong Finance.

Nếu tùy chọn được đặt thành **Không**, hóa đơn nhà cung cấp được tự động xác nhận. Không yêu cầu thêm hành động nào.

Để thiết lập xác minh hóa đơn nhà cung cấp, hãy làm theo các bước sau.

1. Trong Finance, đi đến **Kế toán và quản lý dự án** \> **Thiết lập** \> **Tham số quản lý dự án và kế toán**.
1. Trên tab **Tài chính**, đặt tùy chọn **Bắt buộc phải có xác minh thủ công của PM** thành **Có** nếu chính sách của công ty yêu cầu xác minh hóa đơn nhà cung cấp của nhà thầu phụ. Nếu việc xác minh của người quản lý dự án không phải là bắt buộc trong Dataverse, Hãy để bộ tùy chọn thành **Không**. Theo mặc định, cài đặt này sẽ được sử dụng trên trang **Hóa đơn của nhà cung cấp đang chờ xử lý**.

> [!NOTE]
> Hóa đơn của nhà cung cấp được tạo cho các hợp đồng phụ trong Dataverse chỉ có thể được xử lý chính xác nếu tùy chọn **Bắt buộc phải có xác minh thủ công của PM** được đặt thành **Có**. Số liệu thực tế về thời gian, vật tư và chi phí vật liệu mà nhà thầu phụ tạo có thể được người quản lý dự án khớp thủ công với mô tả hóa đơn nhà cung cấp nếu tùy chọn này được đặt thành **Có**.

### <a name="set-up-a-procurement-integration-account-for-vendor-invoices"></a>Thiết lập tài khoản tích hợp mua sắm cho hóa đơn của nhà cung cấp

Khi hóa đơn của nhà cung cấp được đăng trong Finance for Project Operations – Môi trường tích hợp (không phải lưu kho), các khoản tài chính sẽ được đăng vào Tài khoản tích hợp mua sắm. Hệ thống tạo ra các số liệu thực tế trong Dataverse cho hóa đơn đã đăng. Các số liệu thực tế này được đăng trong Finance bằng cách sử dụng nhật ký Tích hợp dự án. Việc đăng nhật ký Tích hợp dự án sẽ đăng chi phí thực tế và đảo ngược Tài khoản tích hợp mua sắm.

Để thiết lập Tài khoản tích hợp mua sắm cho hóa đơn của nhà cung cấp, hãy làm theo các bước sau.

1. Trong Finance, đi đến **Kế toán và quản lý dự án** \> **Thiết lập** \> **Tham số quản lý dự án và kế toán**.
1. Trên tab **Project Operations trên Dynamics 365 Customer Engagement**, chọn **Vật tư** \> **Tài khoản tích hợp mua sắm**.

### <a name="create-and-post-subcontract-vendor-invoices"></a>Tạo và đăng hóa đơn của nhà cung cấp hợp đồng phụ

Khi nhân viên ghi chép Khoản phải trả nhận được hóa đơn từ nhà thầu phụ, một hóa đơn mới sẽ được tạo trong Finance.

1. Trong Finance, hãy chuyển đến **Khoản phải trả** \> **Hóa đơn** \> **Hóa đơn của nhà cung cấp đang chờ xử lý**.
1. Trên **Ngăn hành động**, chọn **Mới** để tạo hóa đơn nhà cung cấp.
1. Trên tiêu đề hóa đơn, trong trường **Tài khoản hóa đơn**, chọn **Nhà thầu phụ**.
1. Chọn ngày xuất hóa đơn.
1. Trên tab **Tiêu đề**, đặt tùy chọn **Bắt buộc phải có xác minh thủ công của PM** thành **Có**. Cài đặt mặc định của tùy chọn này đến từ trang **Quản lý dự án và các tham số kế toán**. Tuy nhiên, nó có thể được thay đổi ở cấp độ hóa đơn của nhà cung cấp.
1. Trên FastTab **Mô tả hóa đơn**, chọn **Thêm dòng** để tạo một dòng hóa đơn của nhà cung cấp.
1. Chọn danh mục mua sắm đã được tạo cho mô tả hợp đồng phụ rồi nhập đơn giá, đơn vị đo lường và số lượng.
1. Trong phần mô tả hóa đơn của nhà cung cấp, trên tab **Dự án**, chọn dự án mà nhà thầu phụ chia sẻ hóa đơn hợp đồng phụ.
1. Chọn thể loại dự án. Nó có thể thuộc loại **Mặt hàng**, **Chi phí**, **Vật tư**, hoặc **Giờ**.
1. Chỉ chọn vai trò nếu danh mục dự án đã chọn thuộc loại **Giờ**.
1. Chọn **Đăng** để đăng hóa đơn của nhà cung cấp.

Ngoài ra, bạn có thể tạo hóa đơn của nhà cung cấp bằng cách truy cập **Khoản phải trả** \> **Hóa đơn** \> **Hóa đơn của nhà cung cấp đang mở** và chọn **Mới**.

Khi hóa đơn của nhà cung cấp được đăng, nó sẽ có sẵn trong Dataverse cho việc xác minh và xử lý của người quản lý dự án.

## <a name="vendor-invoice-processing-in-dataverse"></a>Xử lý hóa đơn của nhà cung cấp trong Dataverse

Trong hóa đơn của nhà cung cấp được tạo trong Dataverse, một số giá trị trường đến từ hóa đơn của nhà cung cấp được ghi lại trong Finance. Các giá trị khác là giá trị mặc định đến từ hợp đồng phụ.

Các trường sau đây và các bản ghi liên quan sẽ được sao chép từ hợp đồng phụ sang tiêu đề của hóa đơn của nhà cung cấp:

- Tiền tệ
- Đơn vị hợp đồng
- Điều khoản thanh toán

Trên các mô tả hóa đơn của nhà cung cấp, Project Operations sử dụng các giá trị trường sau để nhập tham chiếu mô tả hợp đồng phụ và hợp đồng phụ mặc định:

- Lớp giao dịch
- Vai trò
- Thể loại giao dịch
- Trường sản phẩm
- Dự án
- Tác vụ

> [!NOTE]
> Mô tả hợp đồng phụ giá cố định không được hỗ trợ trong Project Operations.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
