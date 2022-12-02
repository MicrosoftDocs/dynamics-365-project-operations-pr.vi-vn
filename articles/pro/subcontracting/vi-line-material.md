---
title: Dòng hóa đơn của nhà cung cấp trong dự án cho sản phẩm
description: Bài viết này giải thích cách ghi lại các mô tả hóa đơn của nhà cung cấp cho sản phẩm và sử dụng các trường khác nhau để ghi lại các giao dịch mua sản phẩm từ các nhà cung cấp.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d38a447c576c095a7bbe2f5ed84342a88bf69a9b
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261585"
---
# <a name="vendor-invoice-lines-for-products"></a>Dòng hóa đơn của nhà cung cấp trong dự án cho sản phẩm

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Hóa đơn của nhà cung cấp trong Microsoft Dynamics 365 Project Operations có thể có mô tả hóa đơn của nhà cung cấp cho các sản phẩm (còn được gọi là vật tư). Người quản lý dự án có thể sử dụng mô tả hóa đơn của nhà cung cấp cho sản phẩm để ghi lại chi phí sản phẩm được mua trên các dự án.

Mô tả hóa đơn của nhà cung cấp cho sản phẩm có thể hoặc có thể không tham chiếu đến mô tả hợp đồng phụ cho vật tư. Khi mô tả hóa đơn của nhà cung cấp cho sản phẩm tham chiếu đến hợp đồng phụ, người quản lý dự án sẽ có thể đối sánh và xác minh sản phẩm đang được lập hóa đơn theo mô tả hóa đơn nhà cung cấp dựa trên việc sử dụng sản phẩm đã mua được ghi lại bởi nhà thầu phụ và được phê duyệt bởi người quản lý dự án.

Bảng dưới đây cung cấp các thông tin về các trường trên mô tả hóa đơn của nhà cung cấp cho sản phẩm.

| Trường | Description | Tác động chức năng |
| --- | --- | --- |
| Tên | Tên của mô tả hóa đơn của nhà cung cấp để giúp xác định. | Tên này sẽ được hiển thị là cột đầu tiên trong tất cả các tra cứu dựa trên các mô tả hóa đơn của nhà cung cấp. |
| Description | Mô tả ngắn gọn về các sản phẩm đang được lập hóa bởi nhà cung cấp trên mô tả hóa đơn của nhà cung cấp. | Không có |
| Hợp đồng phụ | Hợp đồng phụ mà các sản phẩm được đặt hàng ban đầu. | Khi một hợp đồng phụ được chọn cho hóa đơn của nhà cung cấp, tất cả các mô tả trên hóa đơn của nhà cung cấp sẽ kế thừa lựa chọn đó. Hóa đơn của nhà cung cấp không được có các mô tả hóa đơn của nhà cung cấp tham chiếu đến các hợp đồng phụ khác nhau. |
| Mô tả hợp đồng phụ | Mô tả hợp đồng phụ mà các sản phẩm được đặt hàng. Danh sách các mô tả hợp đồng phụ có thể được chọn được giới hạn trong các mô tả trên hợp đồng phụ đã chọn. | Khi một mô tả hợp đồng phụ được chọn trên một mô tả hóa đơn của nhà cung cấp cho sản phẩm, các giá trị mặc định cho các trường **Dự án**, **Vai trò** và **Sản phẩm** được nhập từ các trường tương ứng trên mô tả hợp đồng phụ. Nếu mô tả hợp đồng phụ đã chọn có các giá trị trong trường **Dự án**, **Nhiệm vụ** và **Sản phẩm**, giá trị của các trường tương ứng trên mô tả hóa đơn của nhà cung cấp không được khác với các giá trị đó. |
| Ngày giao dịch | Ngày mà chi phí thực tế của mô tả hóa đơn của nhà cung cấp sẽ được ghi lại trên dự án. | Không có|
| Lớp giao dịch | Khi sản phẩm được lập hóa đơn, trường này phải được đặt thành **Vật tư**. | Giá trị **Vật tư** cho biết rằng mô tả hóa đơn của nhà cung cấp đang được sử dụng để ghi lại số tiền hóa đơn cho vật tư đã được mua. |
| Dự án | Tên của dự án mà các sản phẩm đang lập hóa đơn đã được sử dụng. | Trường này là bắt buộc và không thể để trống. |
| Tác vụ | Tên của nhiệm vụ dự án mà các sản phẩm đang lập hóa đơn đã được sử dụng. Trường này chỉ có sẵn nếu một dự án được chọn. Lựa chọn nhiệm vụ dự án là không bắt buộc. | Nếu trường này được để trống, người quản lý dự án có thể đối sánh mô tả hóa đơn của nhà cung cấp với sản phẩm đã mua được sử dụng trên bất kỳ nhiệm vụ dự án nào. Nếu mô tả hóa đơn của nhà cung cấp không tham chiếu đến mô tả hợp đồng phụ và trường này để trống, thì chi phí thực tế được tạo bởi mô tả hóa đơn của nhà cung cấp sẽ không được liên kết với bất kỳ doanh số thực tế chưa lập hóa đơn nào. Trong trường hợp này, nếu thanh toán dựa trên nhiệm vụ được thiết lập, chi phí sẽ không được lập hóa đơn cho khách hàng cuối. |
| Chọn sản phẩm | Chọn xem sản phẩm đang được lập hóa đơn là sản phẩm hiện có từ danh mục hay sản phẩm chọn thêm. | Giá trị mặc định được nhập từ mô tả hợp đồng phụ khi một mô tả hợp đồng phụ được chọn. |
| Sản phẩm | Chọn sản phẩm từ danh mục. Nếu sản phẩm là sản phẩm chọn thêm, hãy nhập tên của sản phẩm. | Trường này được sử dụng để nhập giá mua mặc định cho các sản phẩm hiện có. |
| Số lượng | Nhập số lượng vật tư được lập hóa đơn bởi nhà cung cấp trên mô tả hóa đơn này. | Không có |
| Nhóm đơn vị đo | Chọn nhóm đơn vị của đơn vị mà số lượng đang lập hóa đơn được thể hiện trong đó. | Không có |
| Đơn vị | Giá trị mặc định là đơn vị cơ sở từ nhóm đơn được chọn. Bạn có thể thay đổi giá trị này để thanh toán bằng bất kỳ đơn vị nào của nhóm đơn vị đã chọn. | Sự kết hợp của các giá trị **Sản phẩm** và **Đơn vị** sẽ được sử dụng làm giá trị mặc định hoặc được tính cho trường **Đơn giá** trên mô tả hợp đồng của nhà cung cấp. |
| Giá đơn vị | Đơn giá đặt mặc định sử dụng kết hợp các giá trị **Sản phẩm** và **Đơn vị** từ bảng giá dự án áp dụng cho ngày giao dịch của mô tả hóa đơn nhà cung cấp. | Không có |
| Tổng con | Trường chỉ đọc này được tính dưới dạng *Số lượng* &times; *Đơn giá*, nếu các giá trị được nhập trong cả trường **Số lượng** và trường **Đơn giá**. Nếu một hoặc cả hai trường đều trống, bạn có thể nhập giá trị vào trường này. | Không có |
| Thuế bán hàng | Nhập số tiền thuế bán hàng. | Không có |
| Tổng số tiền | Tổng số tiền của mô tả hợp hóa đơn của nhà cung cấp, bao gồm thuế. Trường này được tính là *Tổng phụ* + *Thuế bán hàng*. | Không có |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
