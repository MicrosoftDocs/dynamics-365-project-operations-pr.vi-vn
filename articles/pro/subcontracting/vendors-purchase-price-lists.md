---
title: Quản lý nhà cung cấp và bảng giá mua trong Project Operations
description: Chủ đề này cung cấp những thông tin sẽ giúp bạn tạo và duy trì dữ liệu nhà cung cấp cũng như bảng giá mua cho hợp đồng phụ.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cf62ef8eb87ac2bc138e63c7f92132e00451df6d7766291a8399a94a070799ab
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994167"
---
# <a name="vendor-and-purchase-price-list-management-in-project-operations"></a>Quản lý nhà cung cấp và bảng giá mua trong Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

## <a name="vendors-in-project-operations"></a>Các nhà cung cấp trong Project Operations

Trong Microsoft Dynamics 365 Project Operations, tài khoản nhà cung cấp có kiểu quan hệ là **Nhà cung cấp** hoặc **Nhà cung ứng**. Bạn chỉ có thể chọn một bản ghi tài khoản có một trong các loại mối quan hệ này với tư cách là nhà cung cấp trên hợp đồng phụ.

Bạn có thể liên kết một hoặc nhiều bảng giá mua với một hồ sơ nhà cung cấp. Tuy nhiên, mỗi bảng giá mua được liên kết với một hồ sơ nhà cung cấp phải có hiệu lực vào ngày riêng biệt. Project Operations không hỗ trợ các ngày có hiệu lực trùng nhau đối với bảng giá mua.

Theo mặc định, các trường và khái niệm sau trên một hồ sơ nhà cung cấp được sử dụng cho bất kỳ hợp đồng phụ nào được tạo cho nhà cung cấp:

- Điều khoản thanh toán
- Người thanh toán
- Người liên hệ chính

    > [!NOTE]
    > Theo mặc định, người liên hệ chính của nhà cung cấp được sử dụng làm người quản lý tài khoản nhà cung cấp của hợp đồng phụ.

- Tiền tệ
- Bảng giá mua hiện tại

## <a name="purchase-price-lists-in-project-operations"></a>Bảng giá mua trong Project Operations

Một bảng giá trong đó trường **Ngữ cảnh** được đặt thành **Mua** được coi là một bảng giá mua. Có thể định nghĩa Bảng giá mua để đại diện cho một danh mục tỷ giá mua cho thời gian, chi phí và vật liệu. Bảng giá mua tương tự như bảng giá chi phí và giá bán trong Project Operations. Các khái niệm sau đây áp dụng cho bảng giá mua giống như cách chúng áp dụng cho bảng giá chi phí và giá bán:

- **Ngày hiệu lực** – Bảng giá mua có hiệu lực. Ngày hiệu lực được thể hiện bằng các trường ngày bắt đầu và ngày kết thúc trên mỗi bảng giá. Khoảng thời gian giữa ngày bắt đầu và ngày kết thúc là khoảng thời gian có hiệu lực.
- **Đơn vị tiền tệ** – Đơn vị tiền tệ trên tiêu đề bảng giá được sử dụng làm đơn vị tiền tệ thể hiện giá mua cho các hạng mục nhân công, chi phí và sản phẩm trong danh mục.
- **Đơn vị thời gian mặc định** – Đơn vị thời gian mặc định thể hiện giá nhân công cho giao dịch mua. Trường đơn vị thời gian trên bảng giá chỉ được sử dụng để cung cấp giá trị mặc định. Có thể thay đổi giá trị đó trên từng hàng giá vai trò.

Có thể đính kèm bảng giá mua với hồ sơ nhà cung cấp dưới dạng liên kết được gọi là bảng giá dự án. Các bảng giá này được dùng để nhập giá mặc định trên các dòng hợp đồng phụ. Theo mặc định, khi nhiều bảng giá mua được đính kèm vào hồ sơ nhà cung cấp, bảng giá mới nhất sẽ được sử dụng cho các hợp đồng phụ được tạo cho nhà cung cấp. Chỉ có thể đính kèm những danh sách giá trong đó trường **Ngữ cảnh** được đặt thành **Mua** vào hồ sơ nhà cung cấp.

### <a name="subcontract-specific-purchase-price-lists"></a>Bảng giá mua cụ thể theo hợp đồng phụ

Cũng có thể đính kèm bảng giá mua với hợp đồng phụ dưới dạng liên kết được gọi là bảng giá dự án. Các bảng giá này được dùng để nhập giá mặc định trên các dòng hợp đồng phụ. Theo mặc định, khi nhiều bảng giá mua được đính kèm với một hợp đồng phụ, mỗi bảng giá phải có hiệu lực theo ngày riêng biệt. Project Operations không hỗ trợ những bảng giá mua có ngày hiệu lực trùng nhau. Chỉ có thể đính kèm những danh sách giá trong đó trường **Ngữ cảnh** được đặt thành **Mua** vào hợp đồng phụ.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
