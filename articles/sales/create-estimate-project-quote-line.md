---
title: Ước tính mô tả báo giá dự án
description: Chủ đề này cung cấp thông tin về cách tạo giá trị ước tính trên một mục mô tả báo giá hợp đồng dự án.
author: rumant
manager: Annbe
ms.date: 04/01/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b941511f842a81764ddd1c05a437578b9fd902ce
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858814"
---
# <a name="estimate-a-project-quote-line"></a>Ước tính mô tả báo giá dự án

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Mô tả báo giá dựa trên dự án có thông tin chi tiết giúp ước tính chi phí và doanh thu tiềm năng của công việc liên quan để cung cấp mô tả báo giá.

Để ước tính mục mô tả báo giá dựa trên dự án, trên mục mô tả báo giá, hãy chọn tab **Chi tiết mô tả báo giá**. Có hai cách để tạo giá trị ước tính trên môt mục mô tả báo giá dựa trên dự án:

   - Tạo giá trị ước tính theo cách thủ công ngay trên mục mô tả báo giá bằng cách sử dụng chi tiết mô tả báo giá. 
   - Tạo dự án và kế hoạch dự án, sau đó liên kết dự án và các nhiệm vụ trên dự án với mô tả báo giá. Quá trình nhập các ước tính về kế hoạch dự án vào mô tả báo giá dựa trên thông tin bạn cung cấp sẽ được kích hoạt.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Tạo giá trị ước tính trực tiếp trên mô tả báo giá dựa trên dự án

Để tạo các giá trị ước tính ngay trên một mục mô tả báo giá dựa trên dự án, hãy làm theo các bước sau:

1. Để tạo ước tính trên mô tả báo giá dựa trên dự án, hãy chọn tab **Chi tiết mô tả báo giá**. Mục hàng mà bạn tạo trên tab này sẽ tóm tắt giá trị được báo giá cho mô tả báo giá này. 
2. Để tạo chi tiết mô tả báo giá, hãy chọn **Chi tiết mô tả báo giá mới** trên lưới con **Chi tiết mô tả báo giá**. Thanh trượt tạo nhanh sẽ mở ra. Các trường sau trên trang **Mô tả báo giá**.

| **Trường** | **Vị trí** | **Mô tả** | **Tác động xuôi tuyến** |
| --- | --- | --- | --- |
| Mô tả | Tạo nhanh | Mô tả ước tính cụ thể. | Giá trị này mặc định là chi tiết mô tả báo giá có liên quan cho chi phí được tạo tự động. |
| Lớp giao dịch | Tạo nhanh | Danh sách thả xuống này cung cấp các lớp giao dịch được bao gồm trong tab **Tổng quát** của mô tả báo giá dựa trên dự án.  | Giá trị này mặc định là chi tiết mô tả báo giá có liên quan cho chi phí được tạo tự động. |
| Chọn sản phẩm | Tạo nhanh | Áp dụng khi loại giao dịch là **Vật tư**. Bạn có thể chọn chỉ định dòng ước tính này là cho một sản phẩm (danh mục) **Hiện có** hay cho một sản phẩm **Chọn thêm**. | Giá trị này mặc định là chi tiết mô tả báo giá có liên quan cho chi phí được tạo tự động. |
| Sản phẩm | Tạo nhanh | ID của sản phẩm từ danh mục sản phẩm. Trường này chỉ được bật khi bạn chọn **Hiện có** bên trong trường **Chọn sản phẩm**. ID được dùng để truy xuất giá bán từ bảng giá dự án trên báo giá. | Giá trị này mặc định là chi tiết mô tả báo giá có liên quan cho chi phí được tạo tự động. |
| Sản phẩm chọn thêm | Tạo nhanh | Một hộp văn bản để viết tên sản phẩm. Trường này chỉ được bật khi bạn chọn **Chọn thêm** bên trong trường **Chọn sản phẩm**.| Giá trị này mặc định là chi tiết mô tả báo giá có liên quan cho chi phí được tạo tự động. |
| Vai trò | Tạo nhanh | Vai trò của người sẽ thực hiện công việc này hoặc chịu chi phí này. | Giá trị này mặc định là chi tiết mô tả báo giá có liên quan cho chi phí được tạo tự động. |
| Danh mục | Tạo nhanh | Thể loại của công việc hoặc chi phí. | Giá trị này mặc định là chi tiết mô tả báo giá có liên quan cho chi phí được tạo tự động. |
| Ngày bắt đầu | Tạo nhanh | Ngày bắt đầu công việc. | Trường này mặc định là chi tiết mô tả báo giá cho chi phí được tạo tự động. |
| Ngày kết thúc | Tạo nhanh | Ngày kết thúc công việc. | Trường này mặc định là chi tiết mô tả báo giá cho chi phí được tạo tự động. |
| Công ty cung cấp nguồn lực | Tạo nhanh | Công ty cung ứng nguồn lực hoặc pháp nhân phải chịu chi phí này và cung cấp nguồn lực để thực hiện nó. | Giá trị này mặc định là chi tiết mô tả báo giá có liên quan cho chi phí được tạo tự động và được dùng khi truy xuất giá vốn. |
| Đơn vị nguồn lực | Tạo nhanh | Đơn vị cung ứng nguồn lực hoặc pháp nhân phải chịu chi phí này và cung cấp nguồn lực để thực hiện nó. | Giá trị này mặc định là chi tiết mô tả báo giá có liên quan cho chi phí được tạo tự động và được dùng khi truy xuất giá vốn. |
| Lịch trình đơn vị | Tạo nhanh | Nhóm đơn vị của công việc, sản phẩm hoặc chi phí. Các đơn vị thuộc một lịch trình đơn vị hoặc một nhóm đơn vị. Ví dụ: dặm và ki lô mét (km) là các đơn vị thuộc nhóm đơn vị mô tả khoảng cách. | Giá trị này mặc định là chi tiết mô tả báo giá có liên quan cho chi phí được tạo tự động. |
| Đơn vị | Tạo nhanh | Đơn vị của công việc, sản phẩm hoặc chi phí. | Giá trị này mặc định là chi tiết mô tả báo giá có liên quan cho chi phí được tạo tự động. |
| Số lượng | Tạo nhanh | Số lượng công việc, sản phẩm hoặc chi phí. | Giá trị này mặc định là chi tiết mô tả báo giá có liên quan cho chi phí được tạo tự động. |
| Đơn giá | Tạo nhanh |Mức lương theo giờ của vai trò đang thực hiện công việc, hoặc chi phí trên một đơn vị của thể loại chi phí hoặc chi phí đơn vị của sản phẩm. Mặc định cho **Thời gian** dựa trên sự kết hợp của các giá trị thứ nguyên về giá trên dòng giá theo vai trò trong bảng giá dự án có hiệu lực cho ngày bắt đầu. Đối với **Chi phí**, giá trị mặc định là mức giá thiết lập cho thể loại giao dịch trong bảng giá dự án có hiệu lực vào ngày bắt đầu. Nếu phương thức tính giá cho danh mục giao dịch không phải là giá mỗi đơn vị, thì không có giá trị mặc định và trường này được để trống. Đối với sản phẩm, giá trị mặc định của trường này dựa trên dòng **Hạng mục trong bảng giá** của bảng giá dự án có hiệu lực cho ngày bắt đầu.| Tỷ lệ chi phí của vai trò đang thực hiện công việc, hoặc chi phí trên một đơn vị của thể loại chi phí hoặc chi phí đơn vị của sản phẩm. Mặc định cho **Thời gian** dựa trên sự kết hợp của các giá trị thứ nguyên về giá trên dòng giá theo vai trò trong bảng giá vốn đính kèm đơn vị hợp đồng có hiệu lực cho ngày bắt đầu. Đối với chi phí, giá trị mặc định cho trường này dựa trên dòng giá theo thể loại trong bảng giá vốn đính kèm với đơn vị hợp đồng có hiệu lực cho ngày bắt đầu. Nếu phương pháp đặt giá cho thể loại giao dịch không phải là đơn giá, thì sẽ không có giá trị mặc định và trường này được để trống. Đối với sản phẩm, giá trị mặc định của trường này dựa trên dòng **Hạng mục trong bảng giá** của bảng giá vốn đính kèm với đơn vị hợp đồng có hiệu lực cho ngày bắt đầu.|
| Thuế Ước tính | Tạo nhanh | Bạn có thể nhập thủ công thuế ước tính cho công việc hoặc chi phí này. | Không có tác động xuôi tuyến đối với trường này. |
| Số lượng | Tạo nhanh | Bạn có thể nhập thông tin vào trường này theo cách thủ công nếu các trường **Số lượng** và **Giá** được để trống. Nếu các trường này không được để trống, thì trường này sẽ trở thành trường chỉ đọc và được tính theo công thức (Số lượng \* Đơn giá) + Thuế. | Không có tác động xuôi tuyến đối với trường này. |

## <a name="update-prices-on-quote-line-details"></a>Cập nhật giá trên chi tiết mô tả báo giá

Nếu bạn đã thay đổi giá trên bảng giá dự án đính kèm với báo giá, hoặc trên bảng giá chi phí của đơn vị ký hợp đồng, bạn có thể chọn **Tính toán lại** trên trang **Báo giá** để làm mới giá trên các chi tiết mô tả báo giá riêng lẻ để phản ánh thay đổi này. Khi bạn chọn **Tính toán lại**, một cảnh báo xuất hiện thông báo cho bạn rằng giá trên chi tiết mô tả báo giá cho tất cả các mô tả báo giá trên báo giá này sẽ được đặt lại. Chọn **Có** để làm mới giá cho cả chi tiết mô tả báo giá bán hàng và chi phí.

## <a name="access-quote-line-details-for-cost"></a>Truy cập chi tiết mô tả báo giá để biết chi phí

Để truy cập chi tiết mô tả báo giá để biết chi phí, hãy làm theo các bước sau:

1. Trên tab **Chi tiết mô tả báo giá**, hãy chọn một hàng trong lưới để kích hoạt các tác vụ trên thanh công cụ của lưới con. 
2. Chọn **Mở chi tiết chi phí** để xem tỷ lệ chi phí liên quan và số tiền cho mô tả báo giá này.

> [!NOTE]
> Việc thay đổi giá trị đơn vị cung ứng, số lượng, ngày tháng, vai trò hoặc danh mục trên chi tiết mô tả báo giá cho chi phí sẽ thay đổi các giá trị tương ứng trên chi tiết mô tả báo giá cho bán hàng.

## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Đơn vị tiền tệ trên chi tiết mô tả báo giá cho chi phí và bán hàng

Đơn vị tiền tệ trên chi tiết mô tả báo giá cho doanh số là đơn vị mặc định từ bảng giá dự án có hiệu lực cho ngày bắt đầu chi tiết mô tả báo giá.

Đơn vị tiền tệ trên chi tiết mô tả báo giá cho chi phí là đơn vị mặc định từ bảng giá của đơn vị hợp đồng có hiệu lực cho ngày bắt đầu chi tiết mô tả báo giá cho chi phí.

> [!NOTE]
> Tính toán lợi nhuận sẽ chuyển đổi số tiền trên chi tiết mô tả báo giá cho chi phí và bán hàng thành tiền tệ cơ bản của môi trường để báo cáo tổng lợi nhuận ước tính trên báo giá. Lỗi làm tròn theo đơn vị tiền tệ và thay đổi lợi nhuận có thể xảy ra do thiếu tỷ giá hối đoái thực tế theo ngày. Chỉ sử dụng các tính toán này trên các báo giá dự án vì đây là các ước tính và không áp dụng cho báo cáo thực tế theo luật định hoặc báo cáo khác đòi hỏi độ chính xác cao hơn khi làm tròn và biết rõ tính hiệu lực của ngày đối với tỷ giá hối đoái.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
