---
title: Các khái niệm chính trong hợp đồng phụ
description: Bài viết này giải thích một số khái niệm chính áp dụng cho hợp đồng phụ trong Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 08/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0ac84d132a2d62528d97ed3776a78062a589a380
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927722"
---
# <a name="key-concepts-in-subcontracting"></a>Các khái niệm chính trong hợp đồng phụ

[!include [banner](../../includes/dataverse-preview.md)]

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Bài viết giải thích một số khái niệm chính mà bạn nên biết trước khi bắt đầu sử dụng chức năng hợp đồng phụ trong Microsoft Dynamics 365 Project Operations.

## <a name="contracting-unit-on-the-subcontract"></a>Đơn vị ký hợp đồng trên hợp đồng phụ

Đơn vị ký hợp đồng đại diện cho bộ phận hoặc đơn vị phụ trách việc bàn giao dự án cuối cùng. Đơn vị ký hợp đồng cũng là bộ phận tham gia vào mối quan hệ hợp đồng với nhà cung cấp.

## <a name="purchase-currency"></a>Đơn vị tiền tệ của giao dịch mua

Trong Project Operations, đơn vị tiền tệ của giao dịch mua là đơn vị tiền tệ của hợp đồng phụ. Đây cũng là đơn vị tiền tệ để ghi chi phí của nhà thầu phụ trong một dự án. Đơn vị tiền tệ của giao dịch mua có thể khác với đơn vị tiền tệ của dự án, đồng thời, đơn vị tiền tệ của dự án cũng có thể khác với đơn vị tiền tệ bán hàng.

## <a name="billing-methods-on-subcontract-lines"></a>Phương thức thanh toán trên mô tả hợp đồng phụ

Đối với dự án, thường có các mô hình hợp đồng dựa trên mức phí cố định và mức tiêu thụ. Project Operations hỗ trợ các phương thức thanh toán này trong bối cảnh bán hàng và mua hàng. Đối với giao dịch mua, các phương thức thanh toán hoạt động theo cách sau:

- **Thời gian và Vật liệu** – Khi một mô tả hợp đồng phụ sử dụng phương thức thanh toán **Thời gian và Vật liệu**, chi phí thời gian được ghi nhận trên dự án khi các nhà thầu phụ làm việc trên dự án đó và ghi lại thời gian. Sau đó, các giao dịch chi phí này từ các nhà thầu phụ sẽ được khớp với các mục hàng trên hóa đơn của nhà cung cấp. Trong mô hình này, người quản lý dự án sử dụng Project Operations có thể khớp và xác minh các dòng hóa đơn của nhà cung cấp với thời gian của nhà thầu phụ được ghi lại và phê duyệt. Sau khi xác minh xong, các chi phí thực tế đã được ghi lại sau khi phê duyệt sẽ được đảo ngược và các chi phí thực tế mới dựa trên hóa đơn của nhà cung cấp sẽ được tạo trên dự án.
- **Giá cố định** – Trong mô hình hợp đồng phí cố định này, hóa đơn của nhà cung cấp được dựa trên các mốc thời gian cố định. Tuy nhiên, nguồn lực của nhà thầu phụ cũng có thể báo cáo thời gian. Sau đó, người quản lý dự án sẽ xem xét và phê duyệt thời gian. Khi được phê duyệt, Project Operations sẽ tạo ra các chi phí thực tế tạm thời cho dự án. Sau khi nhà cung cấp gửi hóa đơn cho một mốc, người quản lý dự án có thể khớp các chi phí thực tế đã ghi trước đó với mốc này. Khi xác minh xong, chi phí thực tế sẽ được đảo ngược và chi phí dựa trên mốc thời gian sẽ được ghi lại.

## <a name="project-price-lists-on-subcontracts"></a>Bảng giá dự án trên hợp đồng phụ

Bảng giá dự án là bảng giá được sử dụng để thiết lập giá mua cho thời gian, chi phí và các thành phần khác liên quan đến dự án. Có thể có nhiều bảng giá, mỗi bảng có thể có hợp đồng phụ có hiệu lực theo ngày trong Project Operations. Project Operations không hỗ trợ các ngày có hiệu lực trùng nhau trên bảng giá dự án cho một hợp đồng phụ.

## <a name="transaction-classes-on-subcontracts"></a>Các lớp giao dịch trên hợp đồng phụ

Project Operations hỗ trợ bốn loại lớp giao dịch:

- Thời gian
- Chi phí
- Vật liệu
- Phí

Chỉ có thể ước tính và chi trả chi phí mua hàng trên các lớp giao dịch **Thời gian**, **Chi phí** và **Vật liệu**. **Phí** là một lớp giao dịch chỉ dành cho doanh thu và không có sẵn trong nội dung mua hàng.

## <a name="purchase-pricing-dimensions"></a>Các phương diện giá mua hàng

Phương diện giá cho phép bạn quyết định những thuộc tính được dùng để thiết lập giá mua và đặt giá trị mặc định cho các giao dịch theo thời gian. Liên quan đến mua hàng, Project Operations chỉ hỗ trợ các bộ phương diện cố định để thiết lập và đặt giá trị mặc định cho giá mua. Đối với việc thiết lập giá mua và đặt giá trị mặc định trên các dòng hợp đồng phụ và giao dịch theo thời gian của hợp đồng phụ, các thuộc tính là **Vai trò** và **Tài nguyên có thể đặt trước**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
