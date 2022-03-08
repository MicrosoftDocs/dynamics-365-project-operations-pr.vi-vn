---
title: Ước tính mô tả báo giá dựa trên dự án
description: Chủ đề này cung cấp thông tin về cách tạo ước tính trên mô tả báo giá dựa trên dự án.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a8e2b56b4a97ce184fc36145fffe63db8772bdef8bb89f9b60ddaf43db0c1ba4
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997317"
---
# <a name="estimating-a-project-based-quote-line"></a>Ước tính mô tả báo giá dựa trên dự án

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Mô tả báo giá dựa trên dự án có thông tin chi tiết giúp ước tính chi phí và doanh thu tiềm năng của công việc liên quan để cung cấp mô tả báo giá.

Để ước tính mô tả báo giá dựa trên dự án, trên mô tả báo giá dựa trên dự án, hãy chọn tab **Chi tiết mô tả báo giá**. Có hai cách để tạo ước tính trên mô tả báo giá dựa trên dự án:

- Tạo giá trị ước tính theo cách thủ công ngay trên mục mô tả báo giá bằng cách sử dụng chi tiết mô tả báo giá. 
- Tạo dự án và kế hoạch dự án, sau đó liên kết dự án và các nhiệm vụ trên dự án với mô tả báo giá. Quá trình nhập các ước tính về kế hoạch dự án vào mô tả báo giá dựa trên thông tin bạn cung cấp sẽ được kích hoạt.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Tạo giá trị ước tính trực tiếp trên mô tả báo giá dựa trên dự án

Để tạo ước tính trên mô tả báo giá dựa trên dự án, hãy chọn tab **Chi tiết mô tả báo giá**. Mục hàng mà bạn tạo trên tab này sẽ tóm tắt giá trị được báo giá cho mô tả báo giá này. 

Để tạo chi tiết mô tả báo giá, hãy chọn **Chi tiết mô tả báo giá mới** trên lưới con **Chi tiết mô tả báo giá**. Thanh trượt tạo nhanh sẽ mở ra. Bảng sau cung cấp thông tin chi tiết về các trường trên trang **Chi tiết mô tả báo giá** và cách các giá trị tác động đến chức năng.

| **Trường** | **Vị trí** | **Mô tả** | **Tác động xuôi tuyến** |
| --- | --- | --- | --- |
| Mô tả | Tạo nhanh | Mô tả ước tính cụ thể. | Giá trị này mặc định là chi tiết mô tả báo giá có liên quan cho chi phí được tạo tự động. |
| Lớp giao dịch | Tạo nhanh | Danh sách thả xuống này cung cấp các loại giao dịch có trên tab **Chung** của mục mô tả báo giá dựa trên dự án.  | Giá trị này mặc định là chi tiết mô tả báo giá có liên quan cho chi phí được tạo tự động. |
| Chọn sản phẩm | Tạo nhanh | Áp dụng khi loại giao dịch là **Vật tư**. Bạn có thể chọn chỉ định dòng ước tính này là cho một sản phẩm (danh mục) **Hiện có** hay cho một sản phẩm **Chọn thêm**. | Giá trị này mặc định là chi tiết mô tả báo giá có liên quan cho chi phí được tạo tự động. |
| Sản phẩm | Tạo nhanh | ID của sản phẩm từ danh mục sản phẩm. Trường này chỉ được bật nếu bạn chọn **Hiện có** bên trong trường **Chọn sản phẩm**. ID được dùng để truy xuất giá bán từ bảng giá dự án trên báo giá. | Giá trị này mặc định là chi tiết mô tả báo giá có liên quan cho chi phí được tạo tự động. |
| Sản phẩm chọn thêm | Tạo nhanh | Một hộp văn bản để viết tên của sản phẩm. Trường này chỉ được bật nếu bạn chọn **Chọn thêm** bên trong trường **Chọn sản phẩm**.| Giá trị này mặc định là chi tiết mô tả báo giá có liên quan cho chi phí được tạo tự động. |
| Vai trò | Tạo nhanh | Vai trò của người sẽ thực hiện công việc này hoặc chịu chi phí này. | Giá trị này mặc định là chi tiết mô tả báo giá có liên quan cho chi phí được tạo tự động. |
| Danh mục | Tạo nhanh | Thể loại của công việc hoặc chi phí. | Giá trị này mặc định là chi tiết mô tả báo giá có liên quan cho chi phí được tạo tự động. |
| Ngày bắt đầu | Tạo nhanh | Ngày bắt đầu công việc. | Trường này mặc định là chi tiết mô tả báo giá cho chi phí được tạo tự động. |
| Ngày kết thúc | Tạo nhanh | Ngày kết thúc công việc. | Trường này mặc định là chi tiết mô tả báo giá cho chi phí được tạo tự động. |
| Đơn vị nguồn lực | Tạo nhanh | Đơn vị cung ứng nguồn lực sẽ phải chịu chi phí này và cung cấp nguồn lực để thực hiện nó. | Giá trị này mặc định là chi tiết mô tả báo giá có liên quan cho chi phí được tạo tự động và được dùng khi truy xuất giá vốn. |
| Lịch trình đơn vị | Tạo nhanh | Nhóm đơn vị của công việc, sản phẩm hoặc chi phí. Các đơn vị thuộc một lịch trình đơn vị hoặc một nhóm đơn vị. Ví dụ: dặm và ki lô mét (km) là các đơn vị thuộc nhóm đơn vị mô tả khoảng cách. | Giá trị này mặc định là chi tiết mô tả báo giá có liên quan cho chi phí được tạo tự động. |
| Đơn vị | Tạo nhanh | Đơn vị của công việc, sản phẩm hoặc chi phí. | Giá trị này mặc định là chi tiết mô tả báo giá có liên quan cho chi phí được tạo tự động. |
| Số lượng | Tạo nhanh | Số lượng công việc, sản phẩm hoặc chi phí. | Giá trị này mặc định là chi tiết mô tả báo giá có liên quan cho chi phí được tạo tự động. |
| Đơn giá | Tạo nhanh |Mức lương theo giờ của vai trò đang thực hiện công việc, hoặc chi phí trên một đơn vị của thể loại chi phí hoặc chi phí đơn vị của sản phẩm. Giá trị mặc định cho trường này là **Thời gian** dựa trên sự kết hợp của các giá trị thứ nguyên về giá trên dòng giá theo vai trò trong bảng giá dự án có hiệu lực cho ngày bắt đầu. Đối với **Chi phí**, giá trị mặc định là mức giá thiết lập cho thể loại giao dịch trong bảng giá dự án có hiệu lực vào ngày bắt đầu. Nếu phương pháp đặt giá cho thể loại giao dịch không phải là đơn giá, thì sẽ không có giá trị mặc định và trường này được để trống. Đối với sản phẩm, giá trị mặc định của trường này dựa trên dòng **Hạng mục trong bảng giá** của bảng giá dự án có hiệu lực cho ngày bắt đầu.| Tỷ lệ chi phí của vai trò đang thực hiện công việc, hoặc chi phí trên một đơn vị của thể loại chi phí hoặc chi phí đơn vị của sản phẩm. Giá trị mặc định cho trường này là **Thời gian** dựa trên sự kết hợp của các giá trị thứ nguyên về giá trên dòng giá theo vai trò trong bảng giá dự án có hiệu lực cho ngày bắt đầu. Đối với **Chi phí**, giá trị mặc định là mức giá thiết lập cho thể loại giao dịch trong bảng giá dự án có hiệu lực vào ngày bắt đầu. Nếu phương pháp đặt giá cho thể loại giao dịch không phải là đơn giá, thì sẽ không có giá trị mặc định và trường này được để trống. Đối với sản phẩm, giá trị mặc định của trường này dựa trên dòng **Hạng mục trong bảng giá** của bảng giá dự án có hiệu lực cho ngày bắt đầu.|
| Thuế Ước tính | Tạo nhanh | Bạn có thể nhập thủ công thuế ước tính cho công việc hoặc chi phí này. | Không có tác động xuôi tuyến đối với trường này. |
| Số lượng | Tạo nhanh | Bạn có thể nhập thông tin vào trường này theo cách thủ công nếu các trường **Số lượng** và **Giá** được để trống. Nếu các trường này không được để trống, thì trường này sẽ trở thành trường chỉ đọc và được tính theo công thức (Số lượng \* Đơn giá) + Thuế. | Không có tác động xuôi tuyến đối với trường này. |


## <a name="update-prices-on-quote-line-details"></a>Cập nhật giá trên chi tiết mô tả báo giá

Nếu bạn đã thay đổi giá trên bảng giá dự án đính kèm với báo giá, hoặc trên bảng giá vốn của đơn vị hợp đồng, bạn có thể chọn **Tính toán lại** trên trang **Báo giá** để làm mới giá trên từng chi tiết mô tả báo giá nhằm phản ánh sự thay đổi này. Khi bạn chọn **Tính toán lại**, một cảnh báo xuất hiện thông báo cho bạn rằng giá trên chi tiết mô tả báo giá cho tất cả các mô tả báo giá trên báo giá này sẽ được đặt lại. Chọn **Có** để làm mới giá cho cả chi tiết mô tả báo giá bán hàng và chi phí.

## <a name="access-quote-line-details-for-cost"></a>Truy cập chi tiết mô tả báo giá để biết chi phí

Trên tab **Chi tiết mô tả báo giá**, chọn một hàng trong lưới để hiển thị một số tác vụ trên thanh công cụ của lưới con. Tác vụ đầu tiên trên thanh công cụ của lưới con khi chi tiết mô tả báo giá được chọn là **Mở chi tiết chi phí**. Chọn **Mở chi tiết chi phí** để xem tỷ lệ chi phí liên quan và số tiền cho mô tả báo giá này.

> [!NOTE]
> Việc thay đổi giá trị đơn vị cung ứng, số lượng, ngày tháng, vai trò hoặc danh mục trên chi tiết mô tả báo giá cho chi phí sẽ thay đổi các giá trị tương ứng trên chi tiết mô tả báo giá cho bán hàng.
## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Đơn vị tiền tệ trên chi tiết mô tả báo giá cho chi phí và bán hàng

Đơn vị tiền tệ trên chi tiết mô tả báo giá cho các mặc định bán hàng từ bảng giá dự án có hiệu lực cho ngày bắt đầu chi tiết mô tả báo giá.

Đơn vị tiền tệ trên chi tiết mô tả báo giá cho các mặc định chi phí từ bảng giá của đơn vị ký hợp đồng của báo giá có hiệu lực cho ngày bắt đầu chi tiết mô tả báo giá cho chi phí.

Tính toán lợi nhuận sẽ chuyển đổi số tiền trên chi tiết mô tả báo giá cho chi phí và bán hàng thành tiền tệ cơ bản của môi trường để báo cáo tổng lợi nhuận ước tính trên báo giá.

> [!GHI CHÚ
> > Lỗi làm tròn theo đơn vị tiền tệ và thay đổi lợi nhuận có thể xảy ra do thiếu tỷ giá hối đoái thực tế theo ngày. Chỉ sử dụng các tính toán này trên các hợp đồng dự án vì đây là các ước tính và không áp dụng cho báo cáo thực tế theo luật định hoặc báo cáo khác đòi hỏi độ chính xác cao hơn khi làm tròn và biết rõ tính hiệu lực của ngày đối với tỷ giá hối đoái.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
