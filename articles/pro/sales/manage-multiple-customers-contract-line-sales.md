---
title: Quản lý nhiều khách hàng trong phần mô tả hợp đồng dựa trên dự án - bản đơn giản
description: Bài viết này cung cấp thông tin về việc quản lý nhiều khách hàng trên các dòng hợp đồng dựa trên dự án.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f7648c7ef7ec6ffb68932552a0c25b79f1f93733
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922156"
---
# <a name="manage-multiple-customers-on-project-based-contract-lines---lite"></a>Quản lý nhiều khách hàng trong phần mô tả hợp đồng dựa trên dự án - bản đơn giản

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Các phần mô tả hợp đồng dựa trên dự án có thể bao gồm danh sách các khách hàng chịu trách nhiệm thanh toán. Danh sách khách hàng trong phần mô tả hợp đồng dựa trên dự án này có thể giống với danh sách khách hàng trên hợp đồng nhưng điều đó không bắt buộc. Khi báo giá dự án thành công, một hợp đồng dự án sẽ được tạo, danh sách khách hàng trên phần mô tả báo giá sẽ được sao chép sang phần mô tả hợp đồng tương ứng. Khách hàng trên báo giá được sao chép sang hợp đồng đó.

Khi hợp đồng dự án được lập hóa đơn, danh sách khách hàng trong phần mô tả hợp đồng dựa trên dự án sẽ được ưu tiên hơn danh sách khách hàng trên hợp đồng. Danh sách khách hàng trên hợp đồng dự án chỉ được sử dụng làm mặc định cho các mô tả hợp đồng mới.

Tất cả các khách hàng trên hợp đồng ở tab **Khách hàng** của hợp đồng dự án đều mặc định là khách hàng trong phần mô tả hợp đồng của bất kỳ mô tả hợp đồng mới nào được tạo cho hợp đồng dự án. Bất kỳ mô tả hợp đồng hiện có nào sẽ không kế thừa các hồ sơ khách hàng mới trên hợp đồng được tạo sau đó.

## <a name="create-update-or-delete-a-contract-line-customer-record"></a>Tạo, cập nhật hoặc xóa hồ sơ khách hàng trong phần mô tả hợp đồng

Bạn có thể tạo, cập nhật hoặc xóa khách hàng trong phần mô tả hợp đồng khỏi tab Khách hàng trong phần mô tả hợp đồng của trang Mô tả hợp đồng dựa trên dự án. Khi một khách hàng mới được thêm vào phần mô tả hợp đồng dựa trên dự án, họ cũng được thêm vào hợp đồng tổng thể dưới tư cách là khách hàng trên hợp đồng với tỷ lệ thanh toán mặc định là 0 phần trăm. Tỷ lệ phần trăm thanh toán trên hợp đồng tổng thể được sao chép sang các phần mô tả hợp đồng mới và sang hợp đồng dự án cuối cùng. Tuy nhiên, khi lập hóa đơn dựa trên hợp đồng thì tỷ lệ phần trăm thanh toán ở cấp mô tả hợp đồng sẽ được sử dụng chứ không phải tỷ lệ phần trăm thanh toán ở cấp hợp đồng tổng thể.

Dưới đây là các trường trên hồ sơ khách hàng trong phần mô tả **Hợp đồng** dựa trên dự án mà bạn cần lưu ý khi làm việc:

| Trường | Vị trí | Nội dung mô tả | Tác động xuôi tuyến |
| --- | --- | --- | --- |
| **T.khoản** | Lưới có thể chỉnh sửa của tab **Khách hàng trên hợp đồng** cũng như các biểu mẫu **Chính** và **Tạo nhanh** cho khách hàng trên hợp đồng. | Tất cả các khách hàng hiện hoạt. Trường này bị khóa sau khi bản ghi được tạo. Để cập nhật trường, hãy xóa hồ sơ và tạo một hồ sơ mới. Nếu đã ghi lại bất kỳ dữ liệu thực tế nào, bạn không thể xóa hồ sơ. Tuy nhiên, bạn có thể đánh dấu tỷ lệ phần trăm thanh toán là 0 cho khách hàng đó. Khi hồ sơ được đánh dấu là 0, mọi chi phí và doanh thu thực tế trong tương lai được phân bổ hoặc chia cho khách hàng này đều sẽ bị ảnh hưởng. | Khi bạn chọn một khách hàng trong danh sách khách hàng chính để thêm và lưu, khách hàng trong phần mô tả hợp đồng đó cũng được thêm làm khách hàng trên hợp đồng. Khách hàng trong phần mô tả hợp đồng được sử dụng khi tạo hóa đơn. |
| **Phần trăm Thanh toán Chia tách** | Lưới có thể chỉnh sửa của tab **Khách hàng trên hợp đồng** cũng như các biểu mẫu **Chính** và **Tạo nhanh** cho khách hàng trên hợp đồng. | Trường này thể hiện tỷ lệ phần trăm của mỗi giao dịch bán hàng chưa thanh toán sẽ được phân bổ cho khách hàng trong phần mô tả hợp đồng này. | Khách hàng trong phần mô tả hợp đồng và tỷ lệ phần trăm thanh toán sẽ được sử dụng khi dữ liệu thực tế được tạo sau khi phê duyệt cũng như khi hóa đơn được tạo. |
| **Giới hạn không vượt quá** | Lưới có thể chỉnh sửa của tab **Khách hàng trên hợp đồng** cũng như các biểu mẫu **Chính** và **Tạo nhanh** cho khách hàng trên hợp đồng. | Cho biết liệu có giới hạn đã được thương lượng cho tổng số tiền mà khách hàng này sẽ được lập hóa đơn theo mô tả hợp đồng hay không. | Giới hạn không vượt quá dành cho khách hàng trong phần mô tả hợp đồng được sử dụng khi hóa đơn và dữ liệu thực tế được tạo. |
| **Là Làm tròn** | Lưới có thể chỉnh sửa của tab **Khách hàng trên hợp đồng** cũng như các biểu mẫu **Chính** và **Tạo nhanh** cho khách hàng trên phần mô tả hợp đồng. | Trường này cho biết liệu khách hàng này có phải là khách hàng làm tròn mặc định của phần mô tả hợp đồng dựa trên dự án này hay không. | Khi bạn tạo dữ liệu thực tế theo tỷ lệ phần trăm thanh toán, có thể có sự chênh lệch nào đó do làm tròn. Trong trường hợp đó, sự chênh lệch do làm tròn nói trên được quy cho khách hàng này. |

## <a name="edit-billing-split-percentages"></a>Chỉnh sửa tỷ lệ phần trăm thanh toán chia tách

Bạn có thể chỉnh sửa tỷ lệ phần trăm thanh toán trong lưới. Khi tổng các tỷ lệ phần trăm thanh toán không bằng 100 phần trăm, sẽ xảy ra lỗi. Sau khi bạn chỉnh sửa tỷ lệ phần trăm thanh toán, hãy làm mới trang để loại bỏ lỗi đó.

Bạn cũng có thể chọn **Phân phối đồng đều** trên lưới con hiển thị khách hàng trong phần mô tả hợp đồng. Thao tác này phân bổ đồng đều các phần thanh toán cho tất cả khách hàng trong phần mô tả hợp đồng. Nếu có bất kỳ hệ số làm tròn nào, hệ số này sẽ được thêm cho khách hàng làm tròn. Một khách hàng trong phần mô tả hợp đồng sẽ luôn được gắn thẻ là khách hàng **Làm tròn** với cờ **Làm tròn** được đặt thành **Có**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]