---
title: Quản lý nhiều khách hàng trên một hợp đồng dự án
description: Bài viết này cung cấp thông tin về cách quản lý nhiều khách hàng trên hợp đồng dự án.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 001c3c822a5d1cef6bd85164ef5e63e81719dafb
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824559"
---
# <a name="manage-multiple-customers-on-project-contracts"></a>Quản lý nhiều khách hàng trên một hợp đồng dự án

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Hợp đồng dự án trong Dynamics 365 Project Operations hỗ trợ trường hợp một thỏa thuận theo hợp đồng liên quan đến nhiều khách hàng đang cấp vốn cho thỏa thuận. Tab **Tóm tắt** trên trang **Hợp đồng dự án** bao gồm trường **Khách hàng**. Trường này xác định khách hàng chính của thỏa thuận. Các khách hàng khác của thỏa thuận có thể được thiết lập trên tab **Khách hàng** của trang **Hợp đồng dự án**.

Tất cả các khách hàng theo hợp đồng được liệt kê trên hợp đồng dự án đều mặc định là khách hàng trong phần mô tả hợp đồng của bất kỳ mô tả hợp đồng dựa trên dự án mới nào được tạo cho hợp đồng dự án. Các mô tả hợp đồng dựa trên dự án hiện có không kế thừa khách hàng mới theo hợp đồng khi hồ sơ mới được tạo.

Các mô tả hợp đồng dựa trên sản phẩm được tự động liên kết với khách hàng chính.

Khách hàng trên hợp đồng và khách hàng trong phần mô tả hợp đồng có thể được thêm, cập nhật hoặc xóa bất cứ lúc nào trước khi hợp đồng được ký kết.

## <a name="primary-customer"></a>Khách hàng chính

Khách hàng được liệt kê trên tab **Tóm tắt** của hợp đồng dự án dưới dạng khách hàng tiềm năng là khách hàng chính của hợp đồng. Khi cố gắng xóa khách hàng chính khỏi danh sách khách hàng trên hợp đồng, bạn sẽ nhận được thông báo lỗi cho biết không thể xóa hồ sơ khách hàng chính trên hợp đồng.

Bạn không thể cập nhật khách hàng chính trong danh sách khách hàng trên hợp đồng. Thay vào đó, hãy thay đổi khách hàng tiềm năng trên tab **Tóm tắt** của hợp đồng. Khi trường này được cập nhật trên trang **Tóm tắt hợp đồng**, khách hàng mới được thêm làm khách hàng mới trên hợp đồng kèm theo cờ **Chính**. Khách hàng chính trước đó sẽ vẫn là khách hàng trên hợp đồng.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Tạo, cập nhật hoặc xóa hồ sơ khách hàng trên hợp đồng

Bạn có thể tạo, cập nhật hoặc xóa một khách hàng trên hợp đồng khỏi tab **Khách hàng** của trang **Hợp đồng dự án**. Các trường trong bảng sau nằm trong hồ sơ khách hàng trên hợp đồng của hợp đồng dự án và cần lưu ý khi bạn làm việc với hợp đồng.

| Trường | Vị trí | Nội dung mô tả | Tác động xuôi tuyến |
| --- | --- | --- | --- |
| **T.khoản** | Bạn có thể chỉnh sửa lưới của tab **Khách hàng trên hợp đồng** cũng như các biểu mẫu **Chính** và **Tạo nhanh** cho khách hàng trên hợp đồng. | Liệt kê tất cả các tài khoản đang hoạt động. Trường này bị khóa sau khi bản ghi được tạo. Để cập nhật khách hàng, hãy xóa hồ sơ và tạo lại. Nếu đã ghi lại bất kỳ dữ liệu thực tế nào hoặc nếu hồ sơ khách hàng trên hợp đồng là hồ sơ khách hàng chính, thì bạn không thể xóa hồ sơ. | Khách hàng trên hợp đồng được sao chép qua dưới dạng khách hàng trong phần mô tả hợp đồng khi phần mô tả hợp đồng được tạo. |
| **Phần trăm Thanh toán Chia tách** | Bạn có thể chỉnh sửa lưới của tab **Khách hàng trên hợp đồng** cũng như các biểu mẫu **Chính** và **Tạo nhanh** cho khách hàng trên hợp đồng. | Thể hiện tỷ lệ phần trăm của mỗi giao dịch bán hàng chưa thanh toán được phân bổ cho khách hàng trên hợp đồng này. | Được sao chép sang phần mô tả hợp đồng mới và cho các khách hàng trong phần mô tả hợp đồng của dự án trên các mô tả hợp đồng dự án mới. |
| **Tên liên hệ xuất hóa đơn** | Bạn có thể chỉnh sửa lưới của tab **Khách hàng trên hợp đồng** cũng như các biểu mẫu **Chính** và **Tạo nhanh** cho khách hàng trên hợp đồng. | Trường văn bản này được sử dụng để xác định người liên hệ hóa đơn cho khách hàng này. Trường này lấy các giá trị mặc định từ hồ sơ khách hàng liên quan. | Được sao chép sang trường **Tên người thanh toán trên hợp đồng** của hóa đơn được tạo cho khách hàng này. |
| **Tên Nhận hóa đơn** | Bạn có thể chỉnh sửa lưới của tab **Khách hàng trên hợp đồng** cũng như các biểu mẫu **Chính** và **Tạo nhanh** cho khách hàng trên hợp đồng | Trường văn bản này được sử dụng để xác định người liên hệ hóa đơn cho khách hàng này. Trường này lấy các giá trị mặc định từ hồ sơ khách hàng liên quan. | Được sao chép sang trường **Tên người thanh toán trên hợp đồng** của hóa đơn được tạo cho khách hàng này. |
| **Điều khoản thanh toán** | Bạn có thể chỉnh sửa lưới của tab **Khách hàng trên hợp đồng** cũng như các biểu mẫu **Chính** và **Tạo nhanh** cho khách hàng trên hợp đồng. | Các giá trị mặc định được lấy từ hồ sơ khách hàng liên quan. | Được sao chép sang trường **Tên người thanh toán trên hợp đồng** của hóa đơn được tạo cho khách hàng này. |
| **Là Làm tròn** | Bạn có thể chỉnh sửa lưới của tab **Khách hàng trên hợp đồng** cũng như các biểu mẫu **Chính** và **Tạo nhanh** cho khách hàng trên hợp đồng. | Cho biết liệu khách hàng này có phải là khách hàng làm tròn mặc định cho thỏa thuận này hay không. Chỉ có thể có một khách hàng làm tròn trong hợp đồng dự án. | Khi việc phân tách chi phí và doanh số bán hàng chưa thanh toán theo số lượng dẫn đến chênh lệch do làm tròn số, thì chênh lệch đó được áp dụng cho số liệu thực tế ánh xạ đến khách hàng này. |
| **Giới hạn không vượt quá** | Bạn có thể chỉnh sửa lưới của tab **Khách hàng trên hợp đồng** cũng như các biểu mẫu **Chính** và **Tạo nhanh** cho khách hàng trên hợp đồng | Cho biết liệu có giới hạn đã được thương lượng cho tổng số tiền mà khách hàng sẽ được lập hóa đơn cho cam kết này hay không. | Việc thiết lập **Giới hạn không vượt quá** ở cấp khách hàng trên hợp đồng sẽ được đánh giá dựa theo **Dữ liệu thực tế về doanh thu bán hàng chưa lập hóa đơn** tham chiếu đến khách hàng trên hợp đồng này. |

## <a name="edit-billing-split-percentages"></a>Chỉnh sửa tỷ lệ phần trăm thanh toán chia tách

Bạn có thể chỉnh sửa tỷ lệ phần trăm thanh toán bằng cách sử dụng trải nghiệm chỉnh sửa lưới nội dòng. Khi tổng các tỷ lệ phần trăm thanh toán không bằng 100 phần trăm, bạn sẽ nhận được thông báo lỗi. Sau khi bạn chỉnh sửa tỷ lệ phần trăm thanh toán, hãy làm mới trang để loại bỏ lỗi nói trên.

Bạn cũng có thể chọn **Phân phối đồng đều** trên lưới con hiển thị **Khách hàng trên hợp đồng** để phân bổ đồng đều các phần thanh toán cho tất cả các khách hàng trên hợp đồng. Nếu có hệ số làm tròn, hệ số này sẽ được thêm cho khách hàng làm tròn. Một trong số khách hàng trên hợp đồng sẽ luôn được gắn thẻ là khách hàng **làm tròn**, nghĩa là hồ sơ của khách hàng trên hợp đồng đó có cờ làm tròn được đặt thành **Có**. Thông thường, đây là khách hàng chính của hợp đồng, nhưng điều đó cũng có thể được thay đổi.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
