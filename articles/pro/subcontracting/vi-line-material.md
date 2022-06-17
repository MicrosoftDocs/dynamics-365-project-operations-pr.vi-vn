---
title: Dòng hóa đơn của nhà cung cấp trong dự án cho sản phẩm
description: Bài viết này giải thích cách ghi lại các dòng hóa đơn của nhà cung cấp cho các sản phẩm và sử dụng các trường khác nhau để ghi lại các giao dịch mua sản phẩm từ các nhà cung cấp.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 206dd36a1a1e7141678da27d76a99561ac89044b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931402"
---
# <a name="vendor-invoice-lines-for-products"></a>Dòng hóa đơn của nhà cung cấp trong dự án cho sản phẩm

[!include [banner](../../includes/dataverse-preview.md)]

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Hóa đơn của nhà cung cấp trong Microsoft Dynamics 365 Project Operations có thể có các dòng hóa đơn của nhà cung cấp cho các sản phẩm (còn được gọi là vật liệu). Người quản lý dự án có thể sử dụng các dòng hóa đơn của nhà cung cấp cho các sản phẩm để ghi lại chi phí của các sản phẩm đã được mua trong các dự án.

Các dòng hóa đơn của nhà cung cấp cho các sản phẩm có thể hoặc có thể không tham chiếu đến dòng hợp đồng phụ cho vật liệu. Nếu dòng hóa đơn của nhà cung cấp cho các sản phẩm tham chiếu đến hợp đồng phụ, người quản lý dự án sẽ có thể đối sánh và xác minh các sản phẩm đang được lập hóa đơn theo dòng hóa đơn của nhà cung cấp với việc sử dụng các sản phẩm đã mua đã được ghi lại và phê duyệt bởi người quản lý dự án.

Bảng sau cung cấp thông tin về các trường trên các dòng hóa đơn của nhà cung cấp cho các sản phẩm.

| Trường | Description | Tác động chức năng |
| --- | --- | --- |
| Tên | Tên của dòng hóa đơn của nhà cung cấp, để giúp xác định. | Tên này sẽ được hiển thị dưới dạng cột đầu tiên trong tất cả các tra cứu dựa trên các dòng hóa đơn của nhà cung cấp. |
| Description | Mô tả ngắn gọn về các sản phẩm đang được nhà cung cấp xuất hóa đơn trên dòng hóa đơn của nhà cung cấp. | Không có |
| Hợp đồng phụ | Hợp đồng phụ mà các sản phẩm được đặt hàng ban đầu. | Khi một hợp đồng phụ được chọn cho hóa đơn của nhà cung cấp, tất cả các dòng trên hóa đơn của nhà cung cấp sẽ kế thừa lựa chọn đó. Hóa đơn của nhà cung cấp không được có các dòng hóa đơn của nhà cung cấp tham chiếu đến các hợp đồng phụ khác nhau. |
| Dòng hợp đồng phụ | Dòng hợp đồng phụ mà các sản phẩm đã được đặt hàng. Danh sách các dòng hợp đồng phụ có thể được chọn được giới hạn trong các dòng trên hợp đồng phụ đã chọn. | Khi dòng hợp đồng phụ được chọn trên dòng hóa đơn của nhà cung cấp cho các sản phẩm, các giá trị mặc định cho **Dự án**, **vụ**, và **Sản phẩm** các trường được nhập từ các trường tương ứng trên dòng hợp đồng phụ. Nếu dòng hợp đồng phụ đã chọn có các giá trị trong **Dự án**, **vụ**, và **Sản phẩm**, giá trị của các trường tương ứng trên dòng hóa đơn của nhà cung cấp không được khác với các giá trị đó. |
| Ngày giao dịch | Ngày mà chi phí thực tế của dòng hóa đơn nhà cung cấp sẽ được ghi trên dự án. | Không có|
| Lớp giao dịch | Khi sản phẩm được lập hóa đơn, trường này phải được đặt thành **Vật chất**. | Giá trị **Vật chất** cho biết rằng dòng hóa đơn của nhà cung cấp đang được sử dụng để ghi lại số tiền hóa đơn cho các nguyên vật liệu đã được mua. |
| Dự án | Tên của dự án mà các sản phẩm đang được lập hóa đơn đã được sử dụng. | Trường này là bắt buộc và không được để trống. |
| Tác vụ | Tên của nhiệm vụ dự án mà các sản phẩm đang được lập hóa đơn đã được sử dụng. Trường này chỉ có sẵn nếu một dự án được chọn. Lựa chọn nhiệm vụ dự án là tùy chọn. | Nếu trường này được để trống, người quản lý dự án có thể đối sánh dòng hóa đơn của nhà cung cấp với sản phẩm đã mua được sử dụng cho bất kỳ nhiệm vụ nào của dự án. Nếu dòng hóa đơn của nhà cung cấp không tham chiếu đến dòng hợp đồng phụ và trường này để trống, thì giá thực tế được tạo bởi dòng hóa đơn của nhà cung cấp sẽ không được liên kết với bất kỳ hướng dẫn bán hàng chưa lập hóa đơn nào. Trong trường hợp này, nếu thanh toán dựa trên nhiệm vụ được thiết lập, chi phí sẽ không thể được lập hóa đơn cho khách hàng cuối cùng. |
| Chọn sản phẩm | Chọn xem sản phẩm đang được lập hóa đơn là sản phẩm hiện có từ danh mục hay sản phẩm viết sẵn. | Giá trị mặc định được nhập từ dòng hợp đồng phụ khi một dòng hợp đồng phụ được chọn. |
| Sản phẩm | Chọn sản phẩm từ danh mục. Nếu sản phẩm là sản phẩm viết sẵn, hãy nhập tên của sản phẩm. | Trường này được sử dụng để nhập giá mua mặc định cho các sản phẩm hiện có. |
| Số lượng | Nhập số lượng nguyên liệu được nhà cung cấp xuất hóa đơn trên dòng hóa đơn này. | Không có |
| Nhóm đơn vị đo | Chọn nhóm đơn vị của đơn vị mà số lượng đang được lập hóa đơn được thể hiện trong đó. | Không có |
| Đơn vị | Giá trị mặc định là đơn vị cơ sở của nhóm đơn vị được chọn. Bạn có thể thay đổi giá trị này để thanh toán trong bất kỳ đơn vị nào của nhóm đơn vị đã chọn. | Sự kết hợp của **Sản phẩm** và **Đơn vị** các giá trị sẽ được sử dụng làm giá trị mặc định hoặc giá trị được tính toán cho **Đơn giá** trên dòng hóa đơn của nhà cung cấp. |
| Giá đơn vị | Đơn giá mặc định sử dụng kết hợp của **Sản phẩm** và **Đơn vị** giá trị từ bảng giá dự án áp dụng cho ngày giao dịch của dòng hóa đơn nhà cung cấp. | Không có |
| Tổng con | Trường chỉ đọc này được tính là *Số lượng*&times;*Đơn giá*, nếu các giá trị được nhập vào cả hai **Số lượng** lĩnh vực và **Đơn giá** đồng ruộng. Nếu một hoặc cả hai trường đó trống, bạn có thể nhập giá trị vào trường này. | Không có |
| Thuế bán hàng | Nhập số tiền thuế bán hàng. | Không có |
| Tổng cộng | Tổng số tiền của dòng hóa đơn của nhà cung cấp, bao gồm cả thuế. Trường này được tính là *Tổng phụ* + *Thuế doanh thu*. | Không có |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
