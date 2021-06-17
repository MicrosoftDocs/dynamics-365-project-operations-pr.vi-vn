---
title: Quản lý nhiều khách hàng trên các mô tả báo giá dựa trên dự án - bản đơn giản
description: Chủ đề này mô tả cách quản lý nhiều khách hàng trên dòng báo giá dựa trên dự án.
author: rumant
ms.date: 10/06/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f2e45e0a83f904a65a29c1e39b59adac47a77c58
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995017"
---
# <a name="manage-multiple-customers-on-project-based-quote-lines---lite"></a>Quản lý nhiều khách hàng trên các mô tả báo giá dựa trên dự án - bản đơn giản

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Các mô tả báo giá dựa trên dự án hỗ trợ các tình huống mà mỗi mô tả báo giá có một danh sách khách hàng đang trả tiền cho nó. Danh sách khách hàng trên mô tả báo giá theo dự án này có thể giống với danh sách khách hàng trên báo giá. Bạn cũng có thể thay đổi danh sách khách hàng cho khác đi. Khi chốt báo giá dự án, danh sách khách hàng trên mô tả báo giá dựa trên dự án được sao chép sang mô tả hợp đồng dựa trên dự án tương ứng để tạo hợp đồng dự án cuối cùng. Khách hàng trên báo giá dựa trên dự án được sao chép sang hợp đồng dự án.

Khi bạn lập hóa đơn cho hợp đồng dự án cuối cùng, danh sách khách hàng trên mô tả hợp đồng dựa trên dự án sẽ được ưu tiên hơn danh sách trên hợp đồng dự án. Danh sách khách hàng trên hợp đồng dự án chỉ được sử dụng cho giá trị mặc định trên mô tả hợp đồng dự án mới.

Tất cả các khách hàng báo giá trên tab **Khách hàng** của báo giá dự án mặc định là khách hàng mô tả báo giá trên bất kỳ mô tả báo giá dựa trên dự án mới nào được tạo cho báo giá dự án. Bất kỳ mô tả báo giá dựa trên dự án hiện có nào không kế thừa các bản ghi khách hàng báo giá mới được tạo sau chúng.

## <a name="create-update-or-delete-a-quote-line-customer-record"></a>Tạo, cập nhật hoặc xóa bản ghi khách hàng mô tả báo giá

Bạn có thể tạo, cập nhật hoặc xóa khách hàng nhận mô tả báo giá trên tab **Khách hàng nhận mô tả báo giá** trên trang **Mô tả báo giá dựa trên dự án**. Khi bạn thêm khách hàng mới trên mô tả báo giá dựa trên dự án, khách hàng đó cũng được thêm vào báo giá tổng thể làm khách hàng nhận báo giá, với tỷ lệ phần trăm thanh toán chia tách mặc định trên báo giá tổng thể là 0%. Tỷ lệ phần trăm thanh toán chia tách trên báo giá tổng thể được sao chép vào các mô tả báo giá mới và vào hợp đồng dự án cuối cùng. Tuy nhiên, khi bạn lập hóa đơn từ hợp đồng, tỷ lệ phần trăm thanh toán chia tách ở cấp mô tả báo giá sẽ được sử dụng, không phải tỷ lệ phần trăm thanh toán chia tách ở cấp độ hợp đồng tổng thể. 

Bảng sau hiển thị các trường trên bản ghi khách hàng nhận mô tả báo giá của mô tả báo giá dựa trên dự án.

| Trường | Vị trí | Mô tả và hướng dẫn | Tác động xuôi tuyến |
| --- | --- | --- | --- |
| **T.khoản** | Lưới có thể chỉnh sửa trên tab **Khách hàng nhận mô tả báo giá**, biểu mẫu chính và biểu mẫu tạo nhanh cho khách hàng nhận mô tả báo giá. | Liệt kê tất cả các tài khoản đang hoạt động. Trường này bị khóa sau khi bản ghi được tạo. Nếu bạn cần cập nhật trường, hãy xóa và tạo lại bản ghi. Nếu bạn đã ghi lại bất kỳ giá trị thực tế nào, bạn không thể xóa bản ghi. | Khi bạn chọn một tài khoản từ danh sách tài khoản chính để thêm, Khách hàng nhận mô tả báo giá cũng được thêm vào làm khách hàng nhận báo giá khi bạn lưu lại. Khi chốt báo giá, khách hàng nhận mô tả báo giá cũng được sao chép cho khách hàng nhận mô tả hợp đồng dự án. |
| **Phần trăm thanh toán chia tách** | Lưới có thể chỉnh sửa trên tab **Khách hàng nhận mô tả báo giá**, biểu mẫu chính và biểu mẫu tạo nhanh cho khách hàng nhận mô tả báo giá. | Cho biết tỷ lệ phần trăm của mỗi giao dịch bán hàng chưa thanh toán sẽ được quy cho khách hàng nhận mô tả báo giá này. | Được sao chép sang khách hàng nhận mô tả hợp đồng dự án. |
| **Giới hạn không vượt quá** | Lưới có thể chỉnh sửa trên tab **Khách hàng nhận mô tả báo giá**, biểu mẫu chính và biểu mẫu tạo nhanh cho khách hàng nhận mô tả báo giá. | Cho biết liệu có giới hạn thương lượng hoặc hạn mức cho tổng số tiền sẽ được lập hóa đơn cho khách hàng này đối với mô tả báo giá này hay không. | Sáp chép sang khách hàng nhận mô tả hợp đồng dự án khi báo giá được chốt. |
| **Là làm tròn** | Lưới có thể chỉnh sửa trên tab **Khách hàng nhận mô tả báo giá**, biểu mẫu chính và biểu mẫu tạo nhanh cho khách hàng nhận mô tả báo giá. | Cho biết liệu khách hàng này có phải là khách hàng làm tròn mặc định cho mô tả báo giá dựa trên dự án này hay không. | Sáp chép sang khách hàng nhận hợp đồng dự án khi báo giá được chốt. |

## <a name="edit-billing-split-percentages"></a>Chỉnh sửa tỷ lệ phần trăm thanh toán chia tách

Bạn có thể chỉnh sửa tỷ lệ phần trăm thanh toán chia tách nội tuyến. Khi tỷ lệ phần trăm thanh toán chia tách không có tổng bằng 100% thì lỗi sẽ xảy ra. Sau khi bạn chỉnh sửa tỷ lệ phần trăm thanh toán chia tách, hãy làm mới trang mô tả báo giá để xóa lỗi.

Sử dụng hành động phân bổ đồng đều trên lưới con của khách hàng nhận mô tả báo giá để phân bổ phần tách thanh toán cho tất cả khách hàng nhận mô tả báo giá. Nếu có hệ số làm tròn, yếu tố đó sẽ được thêm vào khách hàng làm tròn. Một trong những khách hàng nhận mô tả báo giá luôn được gắn thẻ là khách hàng làm tròn, có nghĩa là bản ghi khách hàng nhận mô tả báo giá có cờ làm tròn được đặt thành **Đúng**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]