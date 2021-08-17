---
title: Ghi lại hoạt động sử dụng vật tư của dự án và nhiệm vụ dự án
description: Chủ đề này cung cấp thông tin về cách ghi nhật ký sử dụng vật tư đối với dự án và nhiệm vụ của dự án.
author: rumant
ms.date: 03/31/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4d8757049953fab0ad8bf6ee1a1d695fcb6df75b1be52641ad4af3b3137d7a0a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999297"
---
# <a name="record-material-usage-on-projects-and-project-tasks"></a>Ghi lại hoạt động sử dụng vật tư của dự án và nhiệm vụ dự án

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/vật tư không tồn kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Khi một nhóm dự án làm việc thông qua các nhiệm vụ trong một dự án, họ tiêu thụ hoặc sử dụng vật tư. Nhật ký sử dụng vật tư cung cấp một cách ghi lại việc sử dụng này để người quản lý dự án có thể phê duyệt và cuối cùng lập hóa đơn cho khách hàng. 

Để ghi lại việc sử dụng danh mục hoặc vật tư chọn thêm và gửi chúng cho người phê duyệt, hãy làm theo các bước sau: 

1. Trong ngăn điều hướng, hãy chọn **Sử dụng vật tư** rồi chọn **Mới**.
2. Trên trang **Sử dụng vật tư mới**, hãy nhập thông tin sử dụng vật tư cần thiết, sau đó chọn **Lưu**.

Bảng sau cung cấp thông tin về các trường trên trang **Nhật ký sử dụng vật tư**. 

| **Trường** | **Mô tả** | **Tác động xuôi tuyến** |
| --- | --- | --- |
| Mô tả | Mô tả về việc sử dụng vật tư cụ thể. | Không có tác động xuôi tuyến đối với trường này. |
| Ngày | Ngày dự kiến sẽ sử dụng vật tư. | Không có tác động xuôi tuyến đối với trường này. |
| Dự án | Danh sách các dự án hiện hoạt. | Việc chọn một dự án cho nhật ký sử dụng vật tư sẽ ảnh hưởng đến trường **Nhiệm vụ** để chỉ hiển thị những nhiệm vụ có trong dự án. |
| Tác vụ | Danh sách các nhiệm vụ của dự án bao gồm nội dung tóm tắt và các nhiệm vụ nút lá. | Việc chọn một nhiệm vụ cho nhật ký sử dụng vật tư ảnh hưởng đến chi phí vật tư thực tế và doanh thu vật tư thực tế cho một nhiệm vụ. Nếu để trống trường này, chi phí sử dụng vật tư và doanh số tương ứng chỉ được theo dõi và tóm tắt ở cấp độ dự án. |
| Chọn sản phẩm | Chỉ định xem việc sử dụng vật tư là cho một sản phẩm (danh mục) **Hiện có** hay cho một sản phẩm **Chọn thêm**. | Trường này xác định loại sản phẩm. |
| Sản phẩm | ID của sản phẩm từ danh mục sản phẩm. Khi bạn chọn một ID sản phẩm, trường **Chọn sản phẩm** tự động cập nhật thành **Sản phẩm hiện có**. ID được dùng để truy xuất giá vốn và giá bán từ bảng giá. | Không có tác động xuôi tuyến đối với trường này. |
| Mô tả sản phẩm chọn thêm | Trường văn bản để viết tên của sản phẩm. Trường này chỉ có sẵn khi bạn chọn sản phẩm **Chọn thêm** bên trong trường **Chọn sản phẩm**.| Không có tác động xuôi tuyến đối với trường này. |
| Nguồn lực có thể đăng ký| Nguồn lực đã sử dụng vật tư này trong dự án. Giá trị mặc định cho trường này là nguồn lực có thể đặt trước của người dùng đã đăng nhập, nhưng bạn có thể thay đổi giá trị này để ghi lại việc sử dụng thay mặt cho các thành viên khác trong nhóm dự án. | Không có tác động xuôi tuyến đối với trường này. |
| Nhóm đơn vị đo | Giá trị mặc định trong trường này đến từ nhóm đơn vị được thiết lập làm giá trị mặc định trên sản phẩm danh mục. Bạn có thể cập nhật trường này để chọn một nhóm đơn vị khác. | Không có tác động xuôi tuyến đối với trường này. |
| Đơn vị | Giá trị mặc định trong trường này là đơn vị mặc định của sản phẩm đã chọn. Bạn có thể cập nhật trường này để chọn một đơn vị khác. | Việc thay đổi đơn vị sẽ dẫn đến một đơn giá và chi phí mặc định khác. |
| Số lượng | Số lượng sản phẩm đã được sử dụng cho dự án hoặc nhiệm vụ của dự án. | Không có tác động xuôi tuyến đối với trường này. |
| Chi phí đơn vị | Chi phí đơn vị của tổ hợp đơn vị và sản phẩm đã chọn như được thiết lập trong bảng giá vốn áp dụng. | Chi phí đơn vị luôn hiển thị theo đơn vị tiền tệ chi phí của dự án. Nếu không có chi phí đơn vị cho sản phẩm và đơn vị kết hợp trong bảng giá, thì chi phí đơn vị sẽ mặc định là 0,00. |
| Tổng chi phí | Số tiền chi phí được tính theo công thức số lượng \* chi phí đơn vị.| Số tiên chi phí luôn hiển thị theo đơn vị tiền tệ chi phí của dự án. |


## <a name="submit-material-usage-for-review-and-approval"></a>Gửi thông tin sử dụng vật tư để được xem xét và phê duyệt 
Sau khi ghi lại tất cả thông tin sử dụng vật tư của mình và đã sẵn sàng để xin sự phê duyệt, bạn phải gửi thông tin sử dụng để được xem xét.

1. Đi đến **Nhật ký sử dụng vật tư** rồi chọn một hoặc nhiều mục nhập. Hoặc, chọn tất cả các bản ghi hoạt động sử dụng vật tư bằng cách đánh dấu vào hộp kiểm trên tiêu đề.
2. Chọn **Gửi**. Hệ thống xử lý các mục nhập đã chọn rồi tạo các yêu cầu phê duyệt việc sử dụng vật tư.

## <a name="recall-a-material-usage-log"></a>Thu hồi nhật ký sử dụng vật tư

Khi cần, bạn có thể thu hồi thông tin sử dụng vật tư đã gửi. Thời gian cần thiết để thu hồi một mục nhập thông tin sử dụng vật tư phụ thuộc vào giai đoạn phê duyệt.  Nếu người phê duyệt chưa chấp thuận mục nhập, việc thu hồi có thể xảy ra ngay lập tức. Tuy nhiên, nếu mục nhập đã được phê duyệt, người phê duyệt được yêu cầu phê duyệt việc thu hồi và đảo ngược các giao dịch.

1. Đi đến **Sử dụng vật tư** và trong danh sách nhật ký sử dụng vật tư, hãy chọn thông tin sử dụng vật tư cần thu hồi.
2. Chọn **Thu hồi**. Nếu mục nhập thông tin sử dụng vật tư vẫn chưa được phê duyệt, hệ thống sẽ thu hồi ngay lập tức. Nếu mục nhập này đã được phê duyệt, một yêu cầu thu hồi sẽ được tạo để thông báo cho người phê duyệt rằng bạn muốn thu hồi thông tin sử dụng vật tư. Khi đó, người phê duyệt sẽ xác nhận rằng việc đảo ngược có thể được thực hiện và mục nhập sẽ được trả lại.

## <a name="delete-a-material-usage-log"></a>Xóa nhật ký sử dụng vật tư

Bạn có thể xóa nhật ký sử dụng vật tư chưa được gửi. Để xóa nhật ký sử dụng vật tư đã được gửi, trước tiên bạn phải thu hồi nó.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
