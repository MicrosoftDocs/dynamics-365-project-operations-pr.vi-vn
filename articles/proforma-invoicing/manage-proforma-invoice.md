---
title: Quản lý hóa đơn ước giá dựa trên dự án
description: Chủ đề này cung cấp thông tin về cách quản lý và làm việc với các hóa đơn ước giá dựa trên dự án.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cba74c14f6d039dce0650f25ee04cbe35ec8f668b774cdaaa3bbf1aab99cb44d
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/06/2021
ms.locfileid: "6989352"
---
# <a name="manage-a-proforma-project-based-invoice"></a>Quản lý hóa đơn ước giá dựa trên dự án

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Trong Dynamics 365 Project Operations, hóa đơn ước giá được tích hợp dưới dạng phần mở rộng cho các hóa đơn trong Dynamics 365 Sales. Tuy nhiên, có nhiều điểm khác biệt trong quy trình lập hóa đơn giữa Sales và Project Operations khi nói đến việc lập hóa đơn. Ví dụ: không thể tạo hóa đơn mới từ trang **Danh sách hóa đơn** trong Project Operations, nhưng có thể làm như vậy trong Sales. Những điểm khác biệt và tiện ích mở rộng này nhằm hỗ trợ quy trình lập hóa đơn cho các dự án khác với hóa đơn điển hình cho đơn bán hàng.

> [!IMPORTANT]
> Do các điểm khác biệt, không sử dụng hóa đơn trong Sales và Project Operations thay thế cho nhau.

## <a name="invoice-header"></a>Tiêu đề hóa đơn

Thông tin sau đây có trên tiêu đề hóa đơn ước giá trong Project Operations.

| Trường | Vị trí | Mô tả |
| --- | --- | --- | 
| **ID hóa đơn** | Tab **Tóm tắt** | ID sẽ tự động được tạo khi tạo hóa đơn ước giá. Trường chỉ đọc bị khóa không cho chỉnh sửa. Trường này được dùng làm tham chiếu cho mỗi hóa đơn ước giá. |
| **Tên** | Tab **Tóm tắt** | Đặt thành tên của hợp đồng dự án theo mặc định. Có thể chỉnh sửa trường này. | 
| **Tiền tệ** | Tab **Tóm tắt** | Đặt thành đơn vị tiền tệ của hợp đồng dự án theo mặc định. Trường chỉ đọc bị khóa không cho chỉnh sửa. |
| **Bảng giá** | Tab **Tóm tắt** | Đặt thành bảng giá của hợp đồng dự án theo mặc định. Trường chỉ đọc bị khóa không cho chỉnh sửa. | 
| **Cơ hội** | Tab **Tóm tắt** | Tham chiếu đến cơ hội được liên kết. Trường chỉ đọc bị khóa không cho chỉnh sửa. | 
| **Hợp đồng** | Tab **Tóm tắt** | Tham chiếu tới hợp đồng dự án được liên kết. Trường chỉ đọc bị khóa không cho chỉnh sửa. | 
| **Khách hàng** | Tab **Tóm tắt** | Tham chiếu tới hợp đồng dự án được liên kết. Trường chỉ đọc bị khóa không cho chỉnh sửa. |
| **Mô tả** | Tab **Tóm tắt** | Trường văn bản mô tả hóa đơn. Có thể chỉnh sửa trường này. | 
| Trường **Nhận hóa đơn** và các trường liên quan | **Tab Tóm tắt** | Giá trị mặc định được đặt từ khách hàng trong hợp đồng dự án. Có thể chỉnh sửa trường này.  | 
| **Trạng thái** | Tab **Tóm tắt** | Đặt các tùy chọn sau: **Hiện hoạt**, **Đã đóng**, **Đã thanh toán** và **Đã hủy**. Bạn có thể chỉnh sửa các tùy chọn này. Các trạng thái không được hỗ trợ cho Project Operations bao gồm **Đã chốt** và **Đã hủy**. </br> Trạng thái được đặt thành **Hiện hoạt** khi hóa đơn được tạo. </br>Trạng thái phải được đặt thành **Đã thanh toán** chỉ sau khi hóa đơn được xác nhận.  | 
| **Trạng thái Hóa đơn Dự án** | Tab **Tóm tắt** | Đặt các tùy chọn sau: **Bản nháp**, **Đang xem xét** và **Đã xác nhận**. Bạn có thể chỉnh sửa các tùy chọn này. Ở cả hai trạng thái **Bản nháp** và **Đang xem xét**, hóa đơn có thể chỉnh sửa được. Không thể chỉnh sửa hóa đơn sau khi đã xác nhận. | 
| **Số tiền Chi tiết** | Tab **Tóm tắt** | Tổng số tiền trên tất cả các mô tả hóa đơn sau khi ứng trước và khấu trừ. Trường chỉ đọc bị khóa không cho chỉnh sửa.  Trường này được dùng để tính toán số tiền cuối cùng. | 
| **Giảm giá (%)** | Tab **Tóm tắt** | Có thể chỉnh sửa trường này để nhập phần trăm chiết khấu. Trường này không được chức năng Project Operations hỗ trợ. Đây là một trường không được hỗ trợ.|  
| **Số tiền Giảm giá** | Tab **Tóm tắt** | Có thể chỉnh sửa trường này để nhập số tiền chiết khấu. Trường này không được chức năng Project Operations hỗ trợ. Đây là một trường không được hỗ trợ. |  
| **Số tiền vận chuyển hàng hóa thực** | **Tab Tóm tắt** | Tổng số tiền trên hóa đơn sau khi áp dụng chiết khấu. Trường chỉ đọc bị khóa không cho chỉnh sửa. Trường này được dùng để tính toán số tiền cuối cùng.  | 
| **Số tiền cước phí vận chuyển** | Tab **Tóm tắt** | Có thể chỉnh sửa trường này để nhập số tiền cước phí vận chuyển. Trường này không được chức năng Project Operations hỗ trợ. Đây là một trường không được hỗ trợ. |
| **Tổng số thuế** | Tab **Tóm tắt** | Tổng số thuế từ tất cả các mô tả hóa đơn trên hóa đơn. Trường chỉ đọc bị khóa không cho chỉnh sửa. | 
| **Tổng số tiền** | Tab **Tóm tắt** | Tổng số tiền sau khi chiết khấu và trừ thuế. Tổng là số tiền khách hàng cần thanh toán. | 

## <a name="project-based-invoice-lines"></a>Mô tả hóa đơn dựa trên dự án

Trong Project Operations, luôn có một mô tả hóa đơn cho mỗi mô tả hợp đồng dự án. Dòng hóa đơn được tạo ngay cả khi không có dữ liệu thực tế. Thông tin sau đây có trên mô tả hóa đơn ước giá.

| Trường | Vị trí | Mô tả | 
| --- | --- | --- |
| **ID hóa đơn** | Tab **Tổng quát** | Tham chiếu đến ID hóa đơn. Trường chỉ đọc bị khóa không cho chỉnh sửa. Liên kết ID hóa đơn có thể được dùng để quay lại tiêu đề hóa đơn. | 
| **Tên** | Tab **Tổng quát** | Tên mô tả hóa đơn được đặt theo mặc định từ tên mô tả hợp đồng. Có thể chỉnh sửa trường này. |
| **Dự án** | Tab **Tổng quát** | Dự án trên mô tả hợp đồng dự án có liên quan. Trường chỉ đọc bị khóa không cho chỉnh sửa. Liên kết dự án có thể được dùng để chuyển đến dự án. | 
| **Phương thức Thanh toán** | Tab **Tổng quát** | Phương thức thanh toán trên mô tả hợp đồng dự án có liên quan. Trường chỉ đọc bị khóa không cho chỉnh sửa. |
| **Số tiền Mô tả Hợp đồng** | Tab **Tổng quát** | Số tiền hợp đồng trên mô tả hợp đồng dự án có liên quan. Trường chỉ đọc bị khóa không cho chỉnh sửa. | 
| **Đã lập hóa đơn Đến nay** | Tab **Tổng quát** | Tổng số tiền trên tất cả thông tin chi tiết mô tả hóa đơn của hóa đơn này. Trường chỉ đọc bị khóa không cho chỉnh sửa. | 
| **Số lượng** | Tab **Tổng quát** | Tổng số tiền trên tất cả thông tin chi tiết mô tả hóa đơn phải thanh toán của hóa đơn này. Trường chỉ đọc bị khóa không cho chỉnh sửa. Trường này được dùng để tính toán số tiền cuối cùng trên tiêu đề hóa đơn. | 
| **Thuế** | Tab **Tổng quát** | Tổng số tiền thuế trên tất cả thông tin chi tiết mô tả hóa đơn của mô tả hóa đơn này. Trường chỉ đọc bị khóa không cho chỉnh sửa. Trường này được dùng để tính toán số tiền thuế cuối cùng trên tiêu đề hóa đơn. | 
| **Số tiền Cộng thêm** | Tab **Tổng quát** | Tổng số tiền (**Thuế + Số tiền**) trên tất cả thông tin chi tiết mô tả hóa đơn phải thanh toán của mô tả hóa đơn này. Trường chỉ đọc bị khóa không cho chỉnh sửa. Trường này được dùng để tính toán số tiền cuối cùng trên tiêu đề hóa đơn. |

## <a name="invoice-line-details"></a>Thông tin chi tiết mô tả hóa đơn

Mỗi mô tả hóa đơn trong hóa đơn dự án bao gồm thông tin chi tiết mô tả hóa đơn. Các thông tin chi tiết mô tả này liên quan đến doanh số thực tế chưa được thanh toán và các mốc quan trọng liên quan đến mô tả hợp đồng được tham chiếu theo mô tả hóa đơn. Tất cả các giao dịch này được đánh dấu là **Sẵn sàng lập hóa đơn**.

Đối với mục mô tả **Hóa đơn thời gian và vật tư**, các chi tiết mô tả hóa đơn được nhóm thành **Phải chịu phí tổn**, **Không phải chịu phí tổn** và **Miễn phí** trên trang **Mô tả hóa đơn**. Thông tin chi tiết **Mô tả hóa đơn phải thanh toán** làm tăng giá trị tổng trên mô tả hóa đơn. **Miễn** và **Các giá trị thực tế không phải thanh toán** không làm tăng giá trị tổng trên mô tả hóa đơn.

Đối với mục mô tả **Hóa đơn giá cố định**, chi tiết mô tả hóa đơn được tạo từ các mốc được đánh dấu là **Đã sẵn sàng để lập hóa đơn** trên mục mô tả hợp đồng có liên quan. Sau khi thông tin chi tiết mô tả hóa đơn được tạo từ một mốc, trạng thái thanh toán trên mốc đó sẽ cập nhật thành **Đã tạo hóa đơn khách hàng**.

### <a name="edit-invoice-line-details"></a>Chỉnh sửa thông tin chi tiết mô tả hóa đơn

Các trường sau có sẵn trên thông tin chi tiết mô tả hóa đơn được hỗ trợ bởi doanh số thực tế chưa được thanh toán.

| Trường | Mô tả |
| --- | --- | 
| **Mô tả hóa đơn** | Một tham chiếu đến **ID mô tả hóa đơn**. Trường này ở chế độ chỉ đọc và bị khóa không cho chỉnh sửa. Liên kết này có thể được dùng để quay lại tiêu đề hóa đơn. | 
| **Mô tả** | Một mô tả của thông tin chi tiết mô tả hóa đơn. Đặt theo mặc định từ trường **Nhận xét nội bộ** trên **Mục nhập thời gian** và từ trường **Mô tả** trên **Mục nhập chi phí**. Có thể chỉnh sửa trường này.| 
| **Mô tả Bên ngoài** | Một mô tả của thông tin chi tiết mô tả hóa đơn. Đặt theo mặc định từ trường **Nhận xét bên ngoài** trên **Mục nhập thời gian** và từ trường **Mô tả** trên **Mục nhập chi phí**. Có thể chỉnh sửa trường này. Mô tả này có thể được dùng để xác định những thông tin gì cần có trên hóa đơn in ra mà sẽ được gửi cho khách hàng. Trong Project Operations, một hóa đơn ước giá không có tất cả chức năng cần thiết để định cấu hình các tùy chọn cài đặt in cho hóa đơn. | 
| **Ngày bắt đầu** | Đây là trường chỉ đọc được đặt theo mặc định từ giá trị thực tế của nguồn. |
| **Dự án** | Đây là trường chỉ đọc được đặt theo mặc định từ giá trị thực tế của nguồn cho dự án trên mục mô tả hợp đồng có liên quan. |  
| **Tác vụ** | Đặt theo mặc định từ nguồn thực tế. Trường chỉ đọc bị khóa không cho chỉnh sửa. |
| **Thể loại giao dịch** | Đặt theo mặc định từ nguồn thực tế. Trường chỉ đọc bị khóa không cho chỉnh sửa. | 
| **Vai trò** | Đặt theo mặc định từ nguồn thực tế. Trường chỉ đọc bị khóa không cho chỉnh sửa. |  
| **Nguồn lực có thể đăng ký** | Đặt theo mặc định từ nguồn thực tế. Trường chỉ đọc bị khóa không cho chỉnh sửa. | 
| **Công ty cung cấp nguồn lực** | Đặt theo mặc định từ nguồn thực tế. Trường chỉ đọc bị khóa không cho chỉnh sửa. | 
| **Đơn vị nguồn lực** | Đặt theo mặc định từ nguồn thực tế. Trường chỉ đọc bị khóa không cho chỉnh sửa. | 
| **Số lượng** | Đặt theo mặc định từ nguồn thực tế. Trường chỉ đọc bị khóa không cho chỉnh sửa. |  
| **Lịch trình Đơn vị** | Đối với thông tin chi tiết mô tả hóa đơn cho thời gian, tùy chọn này luôn được đặt thành thời gian và không chỉnh sửa được. Đối với chi phí, tùy chọn này được đặt theo mặc định từ nguồn chi phí thực tế. Trường chỉ đọc bị khóa không cho chỉnh sửa. | 
| **Đơn vị** | Đặt theo mặc định từ nguồn thực tế. Trường chỉ đọc bị khóa không cho chỉnh sửa. |  
| **Giá** | Đặt theo mặc định từ nguồn thực tế. Trường chỉ đọc bị khóa không cho chỉnh sửa. |
| **Tiền tệ** | Đặt theo mặc định từ nguồn thực tế. Trường chỉ đọc bị khóa không cho chỉnh sửa. | 
| **Số lượng** | Đặt theo mặc định từ nguồn thực tế. Trường chỉ đọc bị khóa không cho chỉnh sửa. | 
| **Thuế** | Đặt theo mặc định từ nguồn thực tế. Có thể chỉnh sửa trường này.| 
| **Số tiền cần thanh toán** | Một trường tính toán, được tính là **Số tiền + Thuế**. Trường chỉ đọc bị khóa không cho chỉnh sửa. | 
| **Loại thanh toán** | Đặt theo mặc định từ nguồn thực tế. Có thể chỉnh sửa trường này. Việc chọn **Phải thanh toán** sẽ thêm mô tả vào mục tổng cộng trên mô tả hóa đơn. Việc chọn **Miễn** và **Không phải thanh toán** sẽ loại trừ mô tả khỏi mục tổng cộng trên mô tả hóa đơn.| 
| **Chọn sản phẩm** | Đặt theo mặc định từ nguồn thực tế. Trường chỉ đọc bị khóa không cho chỉnh sửa. |
| **Sản phẩm** | Đặt theo mặc định từ nguồn thực tế. Trường chỉ đọc bị khóa không cho chỉnh sửa. | 
| **Tên Sản phẩm** | Đặt theo mặc định từ nguồn thực tế. Trường chỉ đọc bị khóa không cho chỉnh sửa. |  
| **Mô tả sản phẩm chọn thêm** | Đặt theo mặc định từ nguồn thực tế. Trường chỉ đọc bị khóa không cho chỉnh sửa. |
| **Loại Giao dịch** | Đây là trường chỉ đọc được đặt theo mặc định thành **Doanh số đã lập hóa đơn** từ giá trị thực tế của nguồn. |  
| **Lớp giao dịch** | Đặt theo mặc định từ nguồn thực tế. Trường chỉ đọc bị khóa không cho chỉnh sửa. | 

Các trường sau có sẵn trên chi tiết mô tả hóa đơn được hỗ trợ theo mốc.

| Trường | Mô tả |
| --- | --- | 
| **Mô tả hóa đơn** | Tham chiếu đến **ID mô tả hóa đơn**. Trường chỉ đọc bị khóa không cho chỉnh sửa. Liên kết này có thể được dùng để quay lại tiêu đề hóa đơn.  | 
| **Mô tả** | Mô tả của thông tin chi tiết mô tả hóa đơn. Đặt theo mặc định từ mô tả mốc nguồn. | 
|**Mô tả Bên ngoài** | Mô tả của thông tin chi tiết mô tả hóa đơn được đặt theo mặc định từ mô tả mốc nguồn. Trường này có thể được dùng để xác định những thông tin gì cần có trên hóa đơn in ra mà sẽ được gửi cho khách hàng. Một hóa đơn ước giá trong Project Operations không có tất cả chức năng cần thiết để định cấu hình các tùy chọn cài đặt in cho hóa đơn. | 
| **Ngày bắt đầu** | Đặt theo mặc định từ ngày **Mốc** trên mốc nguồn. Trường chỉ đọc bị khóa không cho chỉnh sửa. | 
| **Dự án** | Đặt theo mặc định từ mốc nguồn. Trường chỉ đọc bị khóa không cho chỉnh sửa. |
| **Tác vụ** | Đặt theo mặc định từ mốc nguồn. Trường chỉ đọc bị khóa không cho chỉnh sửa. | 
| **Thể loại giao dịch** | Trường chỉ đọc bị khóa không cho chỉnh sửa. |
| **Vai trò** | Trường chỉ đọc bị khóa không cho chỉnh sửa. | 
| **Nguồn lực có thể đăng ký** | Trường chỉ đọc bị khóa không cho chỉnh sửa. | 
| **Đơn vị Nguồn lực** | Trường chỉ đọc bị khóa không cho chỉnh sửa. | 
| **Lịch trình Đơn vị** | Trường chỉ đọc bị khóa không cho chỉnh sửa. | 
| **Đơn vị** | Trường chỉ đọc bị khóa không cho chỉnh sửa. | 
| **Giá** | Đặt theo mặc định từ số tiền trên mốc nguồn. Trường chỉ đọc bị khóa không cho chỉnh sửa. |
| **Tiền tệ** | Đặt theo mặc định từ mốc nguồn. Trường chỉ đọc bị khóa không cho chỉnh sửa. |
| **Số lượng** | Đặt theo mặc định từ số tiền trên mốc nguồn. Trường chỉ đọc bị khóa không cho chỉnh sửa. | 
| **Thuế** | Đặt theo mặc định từ số tiền thuế trên mốc nguồn. Trường chỉ đọc bị khóa không cho chỉnh sửa. |
| **Số tiền Cộng thêm** | Đặt theo mặc định từ số lượng mở rộng trên mốc nguồn. Có thể chỉnh sửa trường này. | 
| **Loại thanh toán** | Luôn đặt theo mặc định thành **Phải thanh toán**. Trường chỉ đọc bị khóa không cho chỉnh sửa. |
| **Loại Giao dịch** | Đặt theo mặc định từ mốc nguồn. Trường chỉ đọc bị khóa không cho chỉnh sửa. | 
| **Lớp giao dịch** | Đặt theo mặc định từ mốc nguồn. Trường chỉ đọc bị khóa không cho chỉnh sửa. | 

## <a name="refresh-invoice-transactions"></a>Làm mới các giao dịch trên hóa đơn

Nếu có các giá trị thực tế sau khi tạo hóa đơn, bạn có thể đưa các giá trị này vào hóa đơn.

1. Trong **Dạng xem sự tồn đọng thanh toán**, hãy đánh dấu dữ liệu là **Sẵn sàng lập hóa đơn**.   
2. Mở bản nháp hóa đơn ước giá và trên ruy băng **Tác vụ**, hãy chọn **Làm mới các giao dịch trên mục mô tả hóa đơn**.

  Chi tiết mô tả hóa đơn được tạo cho bất kỳ giá trị thực tế nào trong quá khứ và được đánh dấu là **Đã sẵn sàng để lập hóa đơn**, nhưng không được thêm vào hóa đơn.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
