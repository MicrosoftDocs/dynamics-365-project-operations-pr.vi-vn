---
title: Ước tính mô tả báo giá dựa trên dự án
description: Chủ đề này cung cấp thông tin về cách tạo ước tính trên mô tả báo giá dựa trên dự án.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 56892a134c0c739958f7f939214930631dea7420
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180398"
---
# <a name="estimating-a-project-based-quote-line"></a>Ước tính mô tả báo giá dựa trên dự án

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Mô tả báo giá dựa trên dự án có thông tin chi tiết giúp ước tính chi phí và doanh thu tiềm năng của công việc liên quan để cung cấp mô tả báo giá.

Để ước tính mô tả báo giá dựa trên dự án, trên mô tả báo giá dựa trên dự án, hãy chọn tab **Chi tiết mô tả báo giá**. Có hai cách để tạo ước tính trên mô tả báo giá dựa trên dự án:

- Tạo ước tính theo cách thủ công trực tiếp trên mô tả báo giá bằng cách sử dụng chi tiết mô tả báo giá 
- Tạo dự án và kế hoạch dự án, sau đó liên kết dự án và các nhiệm vụ trên dự án với mô tả báo giá. Quá trình nhập các ước tính về kế hoạch dự án vào mô tả báo giá dựa trên thông tin bạn cung cấp sẽ được kích hoạt.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Tạo giá trị ước tính trực tiếp trên mô tả báo giá dựa trên dự án

Để tạo ước tính trên mô tả báo giá dựa trên dự án, hãy chọn tab **Chi tiết mô tả báo giá**. Mục hàng mà bạn tạo trên tab này sẽ tóm tắt giá trị được báo giá cho mô tả báo giá này. 

Để tạo chi tiết mô tả báo giá, hãy chọn **+ Chi tiết mô tả báo giá mới** trên lưới con **Chi tiết mô tả báo giá**. Thanh trượt tạo nhanh sẽ mở ra. Các trường sau trên biểu mẫu **Mô tả báo giá**:

| **Trường** | **Vị trí** | **Mô tả** | **Tác động xuôi tuyến** |
| --- | --- | --- | --- |
| Nội dung mô tả | Tạo nhanh | Mô tả ước tính cụ thể. | Trường này mặc định là chi tiết mô tả báo giá liên quan cho chi phí được tạo tự động. |
| Lớp giao dịch | Tạo nhanh | Danh sách thả xuống này cung cấp các lớp giao dịch được bao gồm trong tab **Tổng quát** của mô tả báo giá dựa trên dự án.  | Trường này mặc định là chi tiết mô tả báo giá liên quan cho chi phí được tạo tự động. |
| Vai trò | Tạo nhanh | Người sẽ thực hiện công việc này hoặc chịu chi phí này. | Trường này mặc định là chi tiết mô tả báo giá liên quan cho chi phí được tạo tự động. |
| Danh mục | Tạo nhanh | Danh mục công việc hoặc chi phí. | Trường này mặc định là chi tiết mô tả báo giá liên quan cho chi phí được tạo tự động. |
| Ngày bắt đầu | Tạo nhanh | Ngày bắt đầu của công việc. | Trường này mặc định là chi tiết mô tả báo giá liên quan cho chi phí được tạo tự động. |
| Ngày kết thúc | Tạo nhanh | Ngày kết thúc của công việc. | Trường này mặc định là chi tiết mô tả báo giá liên quan cho chi phí được tạo tự động. |
| Đơn vị Nguồn lực | Tạo nhanh | Đơn vị cung ứng nguồn lực sẽ phải chịu chi phí này và cung cấp nguồn lực để thực hiện. | Trường này mặc định là chi tiết mô tả báo giá liên quan cho chi phí được tạo tự động. Trường này cũng được sử dụng trong truy xuất giá vốn. |
| Lịch trình đơn vị | Tạo nhanh | Nhóm đơn vị đo của công việc hoặc chi phí. Các đơn vị thuộc một lịch trình đơn vị hoặc một nhóm đơn vị. Ví dụ: Dặm và km là đơn vị đó thuộc về một nhóm các đơn vị mô tả khoảng cách. | Trường này mặc định là chi tiết mô tả báo giá liên quan cho chi phí được tạo tự động. |
| Đơn vị | Tạo nhanh | Đơn vị đo của công việc hoặc chi phí. | Trường này mặc định là chi tiết mô tả báo giá liên quan cho chi phí được tạo tự động. |
| Số lượng | Tạo nhanh | Số lượng công việc hoặc chi phí | Trường này mặc định là chi tiết mô tả báo giá liên quan cho chi phí được tạo tự động. |
| Đơn giá | Tạo nhanh | Tỷ lệ thanh toán của vai trò đang thực hiện công việc hoặc giá bán hàng của loại chi phí. Trường này mặc định cho thời gian dựa trên sự kết hợp vai trò và đơn vị cung ứng nguồn lực trên bảng giá dự án có hiệu lực cho ngày bắt đầu. Đối với chi phí, trường này mặc định từ thiết lập giá cho loại giao dịch trong bảng giá dự án có hiệu lực cho ngày bắt đầu. Nếu phương thức tính giá cho danh mục giao dịch không phải là giá mỗi đơn vị, thì không có giá trị mặc định và trường này được để trống. | Tỷ lệ chi phí của vai trò đang thực hiện công việc hoặc chi phí trên đơn vị của loại chi phí. Trường này mặc định cho thời gian dựa trên sự kết hợp vai trò và đơn vị cung ứng nguồn lực trên giá của đơn vị hợp đồng của bảng giá báo giá có hiệu lực cho ngày bắt đầu. Đối với chi phí, trường này mặc định từ thiết lập giá cho loại giao dịch trong bảng giá chi phí của đơn vị hợp đồng có hiệu lực cho ngày bắt đầu. Nếu phương thức tính giá cho danh mục giao dịch không phải là giá mỗi đơn vị, thì không có giá trị mặc định và trường này được để trống. |
| Thuế Ước tính | Tạo nhanh | Bạn có thể nhập thủ công thuế ước tính cho công việc hoặc chi phí này. | Không có tác động xuôi tuyến của trường này. |
| Số lượng | Tạo nhanh | Bạn có thể nhập thông tin vào trường này theo cách thủ công nếu các trường **Số lượng** và **Giá** được để trống. Nếu các trường này không trống, trường này sẽ trở thành chỉ đọc và được tính là (Số lượng \* Đơn giá) + Thuế. | Không có tác động xuôi tuyến của trường này. |

## <a name="update-prices-on-quote-line-details"></a>Cập nhật giá trên chi tiết mô tả báo giá

Nếu bạn đã thay đổi giá trên bảng giá dự án đính kèm với báo giá, hoặc trên bảng giá chi phí của đơn vị ký hợp đồng, bạn có thể chọn **Tính toán lại** trên trang **Báo giá** để làm mới giá trên các chi tiết mô tả báo giá riêng lẻ để phản ánh thay đổi này. Khi bạn chọn **Tính toán lại**, một cảnh báo xuất hiện thông báo cho bạn rằng giá trên chi tiết mô tả báo giá cho tất cả các mô tả báo giá trên bảng báo giá này sẽ được đặt lại. Chọn **Có** để làm mới giá cho cả chi tiết mô tả báo giá bán hàng và chi phí.

## <a name="access-quote-line-details-for-cost"></a>Truy cập chi tiết mô tả báo giá để biết chi phí

Trên tab **Chi tiết mô tả báo giá**, chọn một hàng trong lưới để hiển thị một số tác vụ trên thanh công cụ của lưới con. Tác vụ đầu tiên trên thanh công cụ của lưới con khi chi tiết mô tả báo giá được chọn là **Mở chi tiết chi phí**. Chọn **Mở chi tiết chi phí** để xem tỷ lệ chi phí liên quan và số tiền cho mô tả báo giá này.

> [!NOTE]
> Việc thay đổi giá trị đơn vị cung ứng, số lượng, ngày tháng, vai trò hoặc danh mục trên chi tiết mô tả báo giá cho chi phí sẽ thay đổi các giá trị tương ứng trên chi tiết mô tả báo giá cho bán hàng.
## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Đơn vị tiền tệ trên chi tiết mô tả báo giá cho chi phí và bán hàng

Đơn vị tiền tệ trên chi tiết mô tả báo giá cho các mặc định bán hàng từ bảng giá dự án có hiệu lực cho ngày bắt đầu chi tiết mô tả báo giá.

Đơn vị tiền tệ trên chi tiết mô tả báo giá cho các mặc định chi phí từ bảng giá của đơn vị ký hợp đồng của báo giá có hiệu lực cho ngày bắt đầu chi tiết mô tả báo giá cho chi phí.

Tính toán lợi nhuận sẽ chuyển đổi số tiền trên chi tiết mô tả báo giá cho chi phí và bán hàng thành tiền tệ cơ bản của môi trường để báo cáo tổng lợi nhuận ước tính trên báo giá.

Điều này có thể dẫn đến lỗi làm tròn tiền tệ và thay đổi lợi nhuận do thiếu tỷ giá hối đoái có hiệu lực theo ngày. Chỉ sử dụng các tính toán này trên báo giá dự án dưới dạng ước lượng chứ không phải báo cáo thực tế theo luật định hoặc báo cáo khác đòi hỏi độ chính xác cao hơn trong việc làm tròn và nhận thức về ngày có hiệu lực đối với tỷ giá hối đoái.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]