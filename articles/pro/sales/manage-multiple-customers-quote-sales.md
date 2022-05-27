---
title: Quản lý nhiều khách hàng trên các báo giá dự án - bản đơn giản
description: Chủ đề này cung cấp thông tin về cách làm việc trên các báo giá có nhiều khách hàng sẽ tài trợ cho dự án. (Sales)
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 867d34f955ba53c74e9c31349b7f67d84ba10da4
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576802"
---
# <a name="manage-multiple-customers-on-project-quotes---lite"></a>Quản lý nhiều khách hàng trên các báo giá dự án - bản đơn giản

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Báo giá dự án hỗ trợ tình huống mà đề xuất có liên quan đến nhiều khách hàng sẽ tài trợ cho thỏa thuận. Tab **Tóm tắt** của Báo giá có trường **Khách hàng tiềm năng** nhằm xác định khách hàng chính của thỏa thuận. Các khách hàng khác cho thỏa thuận có thể được thiết lập trên tab **Khách hàng** của báo giá dự án.

Tất cả các khách hàng báo giá trên tab **Khách hàng** của báo giá dự án mặc định là khách hàng mô tả báo giá trên bất kỳ mô tả báo giá dựa trên dự án **mới** nào được tạo cho báo giá. Bất kỳ mô tả báo giá dựa trên dự án hiện có nào sẽ không kế thừa các bản ghi khách hàng báo giá mới được tạo sau chúng.

Các dòng báo giá dựa trên sản phẩm được tự động liên kết với khách hàng chính cũng là khách hàng trong trường **Khách hàng tiềm năng** trên tab **Tóm tắt** của báo giá.

Khách hàng báo giá và khách hàng mô tả báo giá có thể được thêm, cập nhật hoặc xóa bất kỳ lúc nào trước khi báo giá được chốt.

## <a name="concept-of-a-primary-customer"></a>Khái niệm về khách hàng chính

Khách hàng trên tab tóm tắt của báo giá dự án như khách hàng tiềm năng là khách hàng chính của báo giá. Khi bạn cố gắng xóa khách hàng chính khỏi danh sách khách hàng trên báo giá, bạn sẽ thấy lỗi rằng không thể xóa bản ghi khách hàng chính trên báo giá.

Không được cập nhật khách hàng chính từ danh sách khách hàng trên báo giá. Tuy nhiên, bạn có thể tác động đến khách hàng chính bằng cách thay đổi khách hàng tiềm năng trên tab **Tóm tắt** của báo giá. Khi trường này được cập nhật trên **Tóm tắt báo giá**, khách hàng tiềm năng mới được chọn sẽ được thêm làm khách hàng báo giá mới và đặt sẵn cờ **Chính**. Khách hàng tiềm năng cũ sẽ vẫn là khách hàng trên báo giá.

## <a name="create-update-or-delete-a-quote-customer-record"></a>Tạo, cập nhật hoặc xóa bản ghi khách hàng báo giá

Một khách hàng nhận báo giá có thể được tạo, cập nhật hoặc xóa trên tab **khách hàng nhận báo giá** trên trang **Báo giá**. Các trường được liệt kê trong bảng sau có trong bản ghi khách hàng nhận báo giá của một báo giá dự án.

| **Trường** | **Vị trí** | **Mô tả** | **Tác động xuôi tuyến** |
| --- | --- | --- | --- |
| T.khoản | Lưới có thể chỉnh sửa trên tab **Khách hàng nhận báo giá** và biểu mẫu **Chính** và **Tạo nhanh** cho khách hàng báo giá. | Liệt kê tất cả các tài khoản đang hoạt động. Trường này bị khóa sau khi bản ghi được tạo. Nếu bạn muốn cập nhật nó, hãy xóa bản ghi và tạo lại nó. Nếu bạn đã ghi lại bất kỳ số liệu thực tế nào, hoặc nếu bản ghi khách hàng báo giá là khách hàng chính, bạn sẽ không được phép xóa bản ghi. | Khách hàng nhận báo giá được sao chép dưới dạng khách hàng nhận mô tả báo giá khi mô tả báo giá được tạo. Khách hàng nhận báo giá cũng được sao chép cho khách hàng hợp đồng dự án khi báo giá được chốt. |
| Phần trăm thanh toán chia tách | Lưới có thể chỉnh sửa trên tab **Khách hàng nhận báo giá** và biểu mẫu **Chính** và **Tạo nhanh** cho khách hàng báo giá. | Cho biết tỷ lệ phần trăm của mỗi giao dịch bán hàng chưa thanh toán sẽ được quy cho khách hàng nhận báo giá này. | Sao chép sang mô tả báo giá mới tạo và sang khách hàng hợp đồng dự án. |
| Tên liên hệ xuất hóa đơn | Lưới có thể chỉnh sửa trên tab **Khách hàng nhận báo giá** và biểu mẫu **Chính** và **Tạo nhanh** cho khách hàng báo giá. | Đây là trường văn bản và cần được sử dụng để xác định người liên hệ Hóa đơn cho khách hàng này. Chúng được mặc định từ bản ghi tài khoản liên quan | Được sao chép sang khách hàng hợp đồng dự án khi chốt Báo giá và lần lượt đến trường Tên liên hệ xuất hóa đơn trên Hóa đơn được tạo cho khách hàng này. |
| Tên nhận hóa đơn | Lưới có thể chỉnh sửa trên tab **Khách hàng nhận báo giá** và biểu mẫu **Chính** và **Tạo nhanh** cho khách hàng báo giá. | Trường văn bản này được sử dụng để xác định người liên hệ hóa đơn cho khách hàng này. | Được sao chép sang khách hàng hợp đồng dự án khi chốt báo giá và lần lượt đến trường **Tên liên hệ xuất hóa đơn** trên hóa đơn được tạo cho khách hàng này. |
| Điều khoản thanh toán | Lưới có thể chỉnh sửa trên tab **Khách hàng nhận báo giá** và biểu mẫu **Chính** và **Tạo nhanh** cho khách hàng báo giá. | Đây là bộ tùy chọn với các giá trị được mặc định từ bản ghi tài khoản liên quan. | Được sao chép sang khách hàng hợp đồng dự án khi chốt báo giá và lần lượt đến trường **Tên liên hệ xuất hóa đơn** trên hóa đơn được tạo cho khách hàng này. |
| Là Làm tròn | Lưới có thể chỉnh sửa trên tab **Khách hàng nhận báo giá** và biểu mẫu **Chính** và **Tạo nhanh** cho khách hàng báo giá. | Cho biết liệu khách hàng này có phải là khách hàng làm tròn mặc định cho thỏa thuận này hay không. | Sáp chép sang khách hàng hợp đồng dự án khi báo giá được chốt. |
| Giới hạn không vượt quá | Lưới có thể chỉnh sửa trên tab **Khách hàng nhận báo giá** và biểu mẫu **Chính** và **Tạo nhanh** cho khách hàng báo giá. | Cho biết liệu có giới hạn thương lượng hoặc hạn mức cho tổng số tiền sẽ được lập hóa đơn cho khách hàng này đối với cam kết này hay không | Sáp chép sang khách hàng hợp đồng dự án khi báo giá được chốt. |

## <a name="editing-billing-split-percentages"></a>Chỉnh sửa tỷ lệ phần trăm thanh toán chia tách

Bạn có thể chỉnh sửa tỷ lệ phần trăm thanh toán chia tách bằng cách sử dụng trải nghiệm chỉnh sửa lưới nội tuyến. Khi tỷ lệ phần trăm thanh toán chia tách không có tổng bằng 100%, sẽ xảy ra lỗi. Sau khi bạn cập nhật tỷ lệ phần trăm thanh toán chia tách, hãy làm mới trang để xóa lỗi.

Bạn cũng có thể thử chọn **Phân phối đồng đều** trên lưới con của khách hàng báo giá. Hành động này phân bổ phần tách thanh toán cho tất cả các khách hàng nhận báo giá. Nếu có bất kỳ hệ số làm tròn nào, yếu tố đó sẽ được thêm vào khách hàng làm tròn. Một trong những khách hàng nhận báo giá luôn được gắn thẻ là khách hàng làm tròn. điều này có nghĩa là bản ghi khách hàng nhận báo giá có cờ **Làm tròn** được đặt thành **Đúng**. Thông thường, đây là khách hàng chính của báo giá, nhưng điều đó có thể được thay đổi.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
