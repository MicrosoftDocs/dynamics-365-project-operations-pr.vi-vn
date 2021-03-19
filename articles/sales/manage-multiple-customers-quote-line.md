---
title: Quản lý nhiều khách hàng trên mô tả báo giá dựa trên dự án
description: Chủ đề này cung cấp thông tin về cách quản lý nhiều khách hàng trên mô tả báo giá dựa trên dự án.
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4fa0adc877797d782173f29690b33d38ba7f8dcd
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277949"
---
# <a name="manage-multiple-customers-on-project-based-quote-lines"></a>Quản lý nhiều khách hàng trên mô tả báo giá dựa trên dự án

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Các mô tả báo giá dựa trên dự án hỗ trợ các tình huống mà mỗi mô tả báo giá có một danh sách khách hàng đang trả tiền cho nó. Danh sách khách hàng trên mô tả báo giá theo dự án này có thể giống với danh sách khách hàng trên báo giá. Bạn cũng có thể thay đổi danh sách khách hàng cho khác đi. Để tạo hợp đồng dự án cuối cùng khi chốt báo giá dự án, danh sách khách hàng trên mô tả báo giá dựa trên dự án được sao chép sang mô tả hợp đồng dựa trên dự án tương ứng. Khách hàng trên báo giá dựa trên dự án được sao chép sang hợp đồng dự án.

Khi bạn lập hóa đơn cho hợp đồng dự án cuối cùng, danh sách khách hàng trên mô tả hợp đồng dựa trên dự án sẽ được ưu tiên hơn danh sách trên hợp đồng dự án. Danh sách khách hàng trên hợp đồng dự án chỉ được sử dụng để mặc định mô tả hợp đồng dự án mới.

Tất cả các khách hàng báo giá trên tab **Khách hàng** của báo giá dự án mặc định là khách hàng mô tả báo giá trên bất kỳ mô tả báo giá dựa trên dự án mới nào được tạo cho báo giá dự án. Bất kỳ mô tả báo giá dựa trên dự án hiện có nào không kế thừa các bản ghi khách hàng báo giá mới được tạo sau chúng.

## <a name="create-update-or-delete-a-quote-line-customer-record"></a>Tạo, cập nhật hoặc xóa bản ghi khách hàng mô tả báo giá

Bạn có thể tạo, cập nhật hoặc xóa khách hàng nhận mô tả báo giá trên tab **Khách hàng nhận mô tả báo giá** trên trang **Mô tả báo giá dựa trên dự án**. Khi bạn thêm khách hàng mới trên mô tả báo giá dựa trên dự án, khách hàng đó cũng được thêm vào báo giá tổng thể làm khách hàng nhận báo giá, với tỷ lệ phần trăm thanh toán chia tách mặc định trên báo giá tổng thể là 0%. Tỷ lệ phần trăm thanh toán chia tách trên báo giá tổng thể được sao chép vào các mô tả báo giá mới và vào hợp đồng dự án cuối cùng. Tuy nhiên, khi bạn lập hóa đơn từ hợp đồng, tỷ lệ phần trăm thanh toán chia tách ở cấp mô tả báo giá sẽ được sử dụng, không phải tỷ lệ phần trăm thanh toán chia tách ở cấp độ hợp đồng tổng thể. 

Bảng sau hiển thị các trường trên bản ghi khách hàng nhận mô tả báo giá của mô tả báo giá dựa trên dự án.

| Trường | Vị trí | Mô tả và hướng dẫn | Tác động xuôi tuyến |
| --- | --- | --- | --- |
| **T.khoản** | Lưới có thể chỉnh sửa trên tab **Khách hàng nhận mô tả báo giá**, biểu mẫu chính và biểu mẫu tạo nhanh cho khách hàng nhận mô tả báo giá. | Liệt kê tất cả các tài khoản đang hoạt động. Trường này bị khóa sau khi bản ghi được tạo. Nếu bạn cần cập nhật trường, hãy xóa và tạo lại bản ghi. Nếu bạn đã ghi lại bất kỳ giá trị thực tế nào, bạn không thể xóa bản ghi. | Khi bạn chọn một tài khoản từ danh sách tài khoản chính để thêm, Khách hàng nhận mô tả báo giá cũng được thêm vào làm Khách hàng nhận báo giá. Khách hàng nhận mô tả báo giá cũng được sao chép cho khách hàng nhận mô tả hợp đồng dự án khi báo giá được chốt. |
| **Phần trăm thanh toán chia tách** | Lưới có thể chỉnh sửa trên tab **Khách hàng nhận mô tả báo giá**, biểu mẫu chính và biểu mẫu tạo nhanh cho khách hàng nhận mô tả báo giá. | Cho biết tỷ lệ phần trăm của mỗi giao dịch bán hàng chưa thanh toán sẽ được quy cho khách hàng nhận mô tả báo giá này. | Được sao chép sang khách hàng nhận mô tả hợp đồng dự án. |
| **Giới hạn không vượt quá** | Lưới có thể chỉnh sửa trên tab **Khách hàng nhận mô tả báo giá**, biểu mẫu chính và biểu mẫu tạo nhanh cho khách hàng nhận mô tả báo giá. | Cho biết liệu có giới hạn thương lượng hoặc hạn mức cho tổng số tiền sẽ được lập hóa đơn cho khách hàng này đối với mô tả báo giá này hay không. | Sáp chép sang khách hàng nhận mô tả hợp đồng dự án khi báo giá được chốt. |
| **Công ty sở hữu** | Lưới có thể chỉnh sửa trên tab **Khách hàng nhận mô tả báo giá**, biểu mẫu chính và biểu mẫu tạo nhanh cho khách hàng nhận mô tả báo giá. | Pháp nhân mà khách hàng này được thiết lập trong mô-đun **Quản lý dự án và kế toán**. Trường này ở chế độ chỉ đọc và được đặt thành công ty sở hữu của chính báo giá. Danh sách khách hàng cần thêm vào trường **Tài khoản** đã được lọc vào danh sách từ công ty sở hữu trong mô-đun **Quản lý dự án và kế toán** của Project Operations. | Công ty sở hữu tương đương với khái niệm pháp nhân. Tất cả chi phí và doanh thu phát sinh từ dự án này được hạch toán trên sổ cái của công ty sở hữu. |
| **Là làm tròn** | Lưới có thể chỉnh sửa trên tab **Khách hàng nhận mô tả báo giá**, biểu mẫu chính và biểu mẫu tạo nhanh cho khách hàng nhận mô tả báo giá. | Cho biết liệu khách hàng này có phải là khách hàng làm tròn mặc định cho mô tả báo giá dựa trên dự án này hay không. | Sáp chép sang khách hàng nhận hợp đồng dự án khi báo giá được chốt. |

## <a name="edit-billing-split-percentages"></a>Chỉnh sửa tỷ lệ phần trăm thanh toán chia tách

Bạn có thể chỉnh sửa tỷ lệ phần trăm thanh toán chia tách nội tuyến. Khi tỷ lệ phần trăm thanh toán chia tách không có tổng bằng 100% thì lỗi sẽ xảy ra. Sau khi bạn chỉnh sửa tỷ lệ phần trăm thanh toán chia tách, hãy làm mới trang mô tả báo giá để xóa lỗi.

Sử dụng hành động phân bổ đồng đều trên lưới con của khách hàng nhận mô tả báo giá để phân bổ phần tách thanh toán cho tất cả khách hàng nhận mô tả báo giá. Nếu có hệ số làm tròn, yếu tố đó sẽ được thêm vào khách hàng làm tròn. Một trong những khách hàng nhận mô tả báo giá luôn được gắn thẻ là khách hàng làm tròn, có nghĩa là bản ghi khách hàng nhận mô tả báo giá có cờ làm tròn được đặt thành **Đúng**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]