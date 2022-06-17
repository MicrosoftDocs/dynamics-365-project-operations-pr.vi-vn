---
title: Dòng hóa đơn của nhà cung cấp trong dự án cho thời gian
description: Bài viết này giải thích cách ghi lại các dòng hóa đơn của nhà cung cấp cho chi phí thời gian mà các nhà thầu phụ đưa vào.
author: rumant
ms.date: 03/15/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0b81d2884580e9054457906627c1f9101f435524
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927584"
---
# <a name="vendor-invoice-lines-for-time"></a>Dòng hóa đơn của nhà cung cấp trong dự án cho thời gian

[!include [banner](../../includes/dataverse-preview.md)]

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Hóa đơn của nhà cung cấp trong Microsoft Dynamics 365 Project Operations có thể có các dòng hóa đơn của nhà cung cấp cho thời gian. Người quản lý dự án có thể sử dụng các dòng hóa đơn của nhà cung cấp để ghi lại chi phí thời gian của nhà thầu phụ trong các dự án.

Các dòng hóa đơn của nhà cung cấp cho thời gian có thể hoặc có thể không tham chiếu đến một dòng hợp đồng phụ theo thời gian. Nếu dòng hóa đơn nhà cung cấp cho thời gian tham chiếu đến hợp đồng phụ, người quản lý dự án sẽ có thể khớp và xác minh thời gian được dòng hóa đơn nhà cung cấp lập hóa đơn với thời gian được nhà thầu phụ ghi lại và được người quản lý dự án phê duyệt trong dự án.

Bảng sau cung cấp thông tin về các trường trên các dòng hóa đơn của nhà cung cấp theo thời gian.

| Trường | Description | Tác động chức năng |
| --- | --- | --- |
| Tên | Tên của dòng hóa đơn của nhà cung cấp, để giúp xác định. | Tên này sẽ được hiển thị dưới dạng cột đầu tiên trong tất cả các tra cứu dựa trên các dòng hóa đơn của nhà cung cấp. |
| Description | Mô tả ngắn gọn về các dịch vụ đang được nhà cung cấp lập hóa đơn trên dòng hóa đơn của nhà cung cấp. | Không có |
| Hợp đồng phụ | Hợp đồng phụ mà các dịch vụ được đặt hàng ban đầu. | Khi một hợp đồng phụ được chọn cho hóa đơn của nhà cung cấp, tất cả các dòng trên hóa đơn của nhà cung cấp sẽ kế thừa lựa chọn đó. Hóa đơn của nhà cung cấp không được có các dòng hóa đơn của nhà cung cấp tham chiếu đến các hợp đồng phụ khác nhau. |
| Dòng hợp đồng phụ | Dòng hợp đồng phụ mà các dịch vụ đã được đặt hàng. Danh sách các dòng hợp đồng phụ có thể được chọn được giới hạn trong các dòng trên hợp đồng phụ đã chọn. | Khi một dòng hợp đồng phụ được chọn trên một dòng hóa đơn của nhà cung cấp trong một thời gian, các giá trị mặc định cho **Dự án**, **diễn**, và **Tài nguyên có thể đặt trước** các trường được nhập từ các trường tương ứng trên dòng hợp đồng phụ. Nếu dòng hợp đồng phụ đã chọn có các giá trị trong **Dự án**, **diễn**, và **Có thể đặt trước**, giá trị của các trường tương ứng trên dòng hóa đơn của nhà cung cấp không được khác với các giá trị đó. |
| Ngày giao dịch | Ngày mà chi phí thực tế của dòng hóa đơn nhà cung cấp sẽ được ghi trên dự án. | Không có |
| Lớp giao dịch | Giá trị mặc định là **Thời gian**. | Giá trị **Thời gian** cho biết rằng dòng hóa đơn của nhà cung cấp đang được sử dụng để ghi số lượng hóa đơn của thời gian nhà thầu phụ. |
| Dự án | Tên của dự án mà các dịch vụ đang được lập hóa đơn đã được sử dụng. | Trường này là bắt buộc và không được để trống. |
| Tác vụ | Tên của nhiệm vụ dự án mà các dịch vụ đang được lập hóa đơn đã được sử dụng. Trường này chỉ có sẵn nếu một dự án được chọn. Lựa chọn nhiệm vụ dự án là tùy chọn. | Nếu trường này được để trống, người quản lý dự án có thể khớp dòng hóa đơn của nhà cung cấp với thời gian được ghi lại bởi các nguồn lực của nhà thầu phụ đối với bất kỳ nhiệm vụ nào của dự án. Nếu dòng hóa đơn của nhà cung cấp không tham chiếu đến dòng hợp đồng phụ và trường này để trống, thì giá thực tế được tạo bởi dòng hóa đơn của nhà cung cấp sẽ không được liên kết với bất kỳ hướng dẫn bán hàng chưa lập hóa đơn nào. Trong trường hợp này, nếu thanh toán dựa trên nhiệm vụ được thiết lập, chi phí có thể không được lập hóa đơn cho khách hàng cuối cùng. |
| Vai trò | Vai trò của các nguồn lực của hợp đồng phụ có thời gian được lập hóa đơn. | Trường này chỉ định vai trò được thực hiện bởi các tài nguyên hợp đồng phụ có thời gian được lập hóa đơn trên hóa đơn của nhà cung cấp. |
| Nguồn lực có thể đặt trước | Tên của nhà thầu phụ có thời gian được lập hóa đơn. Lựa chọn tài nguyên có thể đặt trước là tùy chọn. | Nếu trường này được để trống, người quản lý dự án có thể khớp dòng hóa đơn của nhà cung cấp với thời gian được ghi lại bởi bất kỳ tài nguyên nào thuộc về nhà cung cấp trên dòng hóa đơn của nhà cung cấp. |
| Số lượng | Nhập số giờ được nhà cung cấp lập hóa đơn trên dòng hóa đơn. |Không có |
| Nhóm đơn vị đo | Giá trị mặc định là **Nhóm đơn vị thời gian** và không thể thay đổi. | Không có |
| Đơn vị | Giá trị mặc định là đơn vị giờ cơ bản từ nhóm đơn vị thời gian. Bạn có thể thay đổi giá trị này để mua trong bất kỳ đơn vị nào của nhóm đơn vị thời gian, chẳng hạn như ngày hoặc tuần. | Sự kết hợp của **Vai diễn** và **Đơn vị** các giá trị sẽ được sử dụng làm giá trị mặc định hoặc giá trị được tính toán cho **Đơn giá** trên dòng hóa đơn của nhà cung cấp. |
| Giá đơn vị | Đơn giá mặc định sử dụng kết hợp của **Vai diễn** và **Đơn vị** giá trị từ bảng giá dự án áp dụng cho ngày giao dịch của dòng hóa đơn nhà cung cấp. | Nếu giá cho bảng giá dự án áp dụng được thiết lập theo một đơn vị khác với đơn vị trên dòng hóa đơn của nhà cung cấp, hệ thống sẽ sử dụng quy đổi đơn vị để tính giá mỗi đơn vị. |
| Tổng con | Trường chỉ đọc này được tính là *Số lượng*&times;*Đơn giá*, nếu các giá trị được nhập vào cả hai **Số lượng** lĩnh vực và **Đơn giá** đồng ruộng. Nếu một hoặc cả hai trường đó trống, bạn có thể nhập giá trị vào trường này. | Không có |
| Thuế bán hàng | Nhập số tiền thuế bán hàng. | Không có |
| Tổng cộng | Tổng số tiền của dòng hóa đơn của nhà cung cấp, bao gồm cả thuế. Trường này được tính là *Tổng phụ* + *Thuế doanh thu*. | Không có |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
