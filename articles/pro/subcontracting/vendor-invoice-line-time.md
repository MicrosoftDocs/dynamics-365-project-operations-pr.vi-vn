---
title: Dòng hóa đơn của nhà cung cấp trong dự án cho thời gian
description: Bài viết này giải thích cách ghi lại các dòng hóa đơn của nhà cung cấp cho chi phí thời gian mà các nhà thầu phụ đưa vào.
author: rumant
ms.date: 03/15/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7f28af3ad76d456dddcfd8e85d968cecb773f8fc
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262039"
---
# <a name="vendor-invoice-lines-for-time"></a>Dòng hóa đơn của nhà cung cấp trong dự án cho thời gian

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Hóa đơn của nhà cung cấp trong Microsoft Dynamics 365 Project Operations có thể có mô tả hóa đơn của nhà cung cấp cho thời gian. Người quản lý dự án có thể sử dụng mô tả hóa đơn của nhà cung cấp để ghi lại chi phí thời gian của nhà thầu phụ trong các dự án.

Mô tả hóa đơn của nhà cung cấp cho thời gian có thể hoặc có thể không tham chiếu đến mô tả hợp đồng phụ cho thời gian. Khi mô tả hóa đơn của nhà cung cấp cho thời gian tham chiếu đến hợp đồng phụ, người quản lý dự án sẽ có thể đối sánh và xác minh thời gian đang được lập hóa đơn theo mô tả hóa đơn nhà cung cấp dựa trên thời gian được ghi lại bởi nhà thầu phụ và được phê duyệt bởi người quản lý dự án trên dự án.

Bảng dưới đây cung cấp các thông tin về các trường trên mô tả hóa đơn của nhà cung cấp cho thời gian.

| Trường | Description | Tác động chức năng |
| --- | --- | --- |
| Tên | Tên của mô tả hóa đơn của nhà cung cấp để giúp xác định. | Tên này sẽ được hiển thị là cột đầu tiên trong tất cả các tra cứu dựa trên các mô tả hóa đơn của nhà cung cấp. |
| Description | Mô tả ngắn gọn về các dịch vụ và sản phẩm đang được lập hóa bởi nhà cung cấp trên mô tả hóa đơn của nhà cung cấp. | Không có |
| Hợp đồng phụ | Hợp đồng phụ mà các dịch vụ được đặt hàng ban đầu. | Khi một hợp đồng phụ được chọn cho hóa đơn của nhà cung cấp, tất cả các mô tả trên hóa đơn của nhà cung cấp sẽ kế thừa lựa chọn đó. Hóa đơn của nhà cung cấp không được có các mô tả hóa đơn của nhà cung cấp tham chiếu đến các hợp đồng phụ khác nhau. |
| Mô tả hợp đồng phụ | Mô tả hợp đồng phụ mà các dịch vụ được đặt hàng. Danh sách các mô tả hợp đồng phụ có thể được chọn được giới hạn trong các mô tả trên hợp đồng phụ đã chọn. | Khi một mô tả hợp đồng phụ được chọn trên một mô tả hóa đơn của nhà cung cấp cho thời gian, các giá trị mặc định cho các trường **Dự án**, **Vai trò** và **Nguồn lực có thể đặt trước** được nhập từ các trường tương ứng trên mô tả hợp đồng phụ. Nếu mô tả hợp đồng phụ đã chọn có các giá trị trong trường **Dự án**, **Vai trò** và **Có thể đặt**, giá trị của các trường tương ứng trên mô tả hóa đơn của nhà cung cấp không được khác với các giá trị đó. |
| Ngày giao dịch | Ngày mà chi phí thực tế của mô tả hóa đơn của nhà cung cấp sẽ được ghi lại trên dự án. | Không có |
| Lớp giao dịch | Giá trị mặc định là **Thời gian**. | Giá trị **Thời gian** cho biết rằng mô tả hóa đơn của nhà cung cấp đang được sử dụng để ghi lại số tiền hóa đơn của thời gian nhà thầu phụ. |
| Dự án | Tên của dự án mà các dịch vụ đang lập hóa đơn đã được sử dụng. | Trường này là bắt buộc và không thể để trống. |
| Tác vụ | Tên của nhiệm vụ dự án mà các dịch vụ đang lập hóa đơn đã được sử dụng. Trường này chỉ có sẵn nếu một dự án được chọn. Lựa chọn nhiệm vụ dự án là không bắt buộc. | Nếu trường này được để trống, người quản lý dự án có thể đối sánh mô tả hóa đơn của nhà cung cấp với thời gian được ghi lại trên bất kỳ nhiệm vụ nào của dự án. Nếu mô tả hóa đơn của nhà cung cấp không tham chiếu đến mô tả hợp đồng phụ và trường này để trống, thì chi phí thực tế được tạo bởi mô tả hóa đơn của nhà cung cấp sẽ không được liên kết với bất kỳ doanh số thực tế chưa lập hóa đơn nào. Trong trường hợp này, nếu thanh toán dựa trên nhiệm vụ được thiết lập, chi phí có thể không được lập hóa đơn cho khách hàng cuối. |
| Vai trò | Vai trò của các nguồn lực của hợp đồng phụ có thời gian được lập hóa đơn. | Trường này chỉ định vai trò được thực hiện bởi các nguồn lực hợp đồng phụ có thời gian được lập hóa đơn trên hóa đơn của nhà cung cấp. |
| Nguồn lực có thể đặt trước | Tên của nhà thầu phụ có thời gian được lập hóa đơn. Không bắt buộc chọn nguồn lực có thể đặt. | Nếu trường này được để trống, người quản lý dự án có thể đối sánh mô tả hóa đơn của nhà cung cấp với thời gian được ghi lại bởi bất kỳ nguồn lực nào thuộc về nhà cung cấp trên mô tả hóa đơn nhà cung cấp. |
| Số lượng | Nhập số giờ của thời gian đang được lập hóa bởi nhà cung cấp trên mô tả hóa đơn của nhà cung cấp. |Không có |
| Nhóm đơn vị đo | Giá trị mặc định là **Nhóm đơn vị đo thời gian** và không thể thay đổi. | Không có |
| Đơn vị | Giá trị mặc định là đơn vị giờ cơ sở từ nhóm nhóm đơn vị thời gian. Bạn có thể thay đổi giá trị này để mua bất kỳ đơn vị nào trong nhóm đơn vị thời gian, chẳng hạn như ngày hoặc tuần. | Sự kết hợp của các giá trị **Vai trò** và **Đơn vị** sẽ được sử dụng làm giá trị mặc định hoặc được tính cho trường **Đơn giá** trên mô tả hợp đồng của nhà cung cấp. |
| Giá đơn vị | Đơn giá đặt mặc định sử dụng kết hợp các giá trị **Vai trò** và **Đơn vị** từ bảng giá dự án áp dụng cho ngày giao dịch của mô tả hóa đơn nhà cung cấp. | Nếu giá cho bảng giá dự án áp dụng có giá được lập theo đơn vị khác với đơn vị trên mô tả hóa đơn của nhà cung cấp, hệ thống sẽ sử dụng quy đổi đơn vị để tính theo đơn giá. |
| Tổng con | Trường chỉ đọc này được tính dưới dạng *Số lượng* &times; *Đơn giá*, nếu các giá trị được nhập trong cả trường **Số lượng** và trường **Đơn giá**. Nếu một hoặc cả hai trường đều trống, bạn có thể nhập giá trị vào trường này. | Không có |
| Thuế bán hàng | Nhập số tiền thuế bán hàng. | Không có |
| Tổng số tiền | Tổng số tiền của mô tả hợp hóa đơn của nhà cung cấp, bao gồm thuế. Trường này được tính là *Tổng phụ* + *Thuế bán hàng*. | Không có |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
