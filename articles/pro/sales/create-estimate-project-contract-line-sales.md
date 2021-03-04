---
title: Số liệu ước tính cho phần mô tả hợp đồng dựa trên dự án - bản đơn giản
description: Chủ đề này cung cấp thông tin về cách đưa ra ước tính trong phần mô tả hợp đồng dựa trên dự án.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2d0d8309fcb4300e33ed2f5933259f99ad7e0d6a
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180443"
---
# <a name="estimate-a-projectbased-contract-line---lite"></a>Số liệu ước tính cho phần mô tả hợp đồng dựa trên dự án - bản đơn giản

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Trong Dynamics 365 Project Operations, phần mô tả hợp đồng dựa trên dự án có các chi tiết giúp ước tính chi phí và doanh thu tiềm năng của công việc liên quan để cung cấp cho phần mô tả hợp đồng.

Để đưa ra số liệu ước tính trong phần hợp đồng dựa trên dự án, hãy chuyển đến tab **Chi tiết mô tả hợp đồng** trong phần **Mô tả hợp đồng** dựa trên dự án.  Có 2 cách để tạo số liệu ước tính trong phần mô tả hợp đồng dựa trên dự án, đó là:

   - Tạo trực tiếp số liệu ước tính trên phần mô tả hợp đồng bằng cách thêm các chi tiết mô tả hợp đồng theo cách thủ công.
   - Tạo một dự án và một kế hoạch dự án, sau đó liên kết dự án đó và các nhiệm vụ với phần mô tả hợp đồng của dự án. Thao tác này kích hoạt quy trình để bạn nhập số liệu ước tính của kế hoạch dự án vào phần mô tả hợp đồng dựa trên các thành phần có trong phần mô tả hợp đồng.

## <a name="create-an-estimation-directly-on-a-projectbased-contract-line"></a>Tạo trực tiếp số liệu ước tính trong phần mô tả hợp đồng dựa trên dự án

1. Chuyển đến phần mô tả hợp đồng và chọn tab **Chi tiết mô tả hợp đồng**. Các dòng bạn tạo trên tab này được tóm tắt và hiển thị dưới dạng **Giá trị hợp đồng** cho phần **Mô tả hợp đồng** này. 
2. Trên lưới con **Chi tiết mô tả hợp đồng**, hãy chọn **+ Chi tiết mô tả hợp đồng mới**. Một thanh trượt tạo nhanh sẽ mở ra. Các trường sau có sẵn trên biểu mẫu **Chi tiết mô tả hợp đồng**:

| Trường | Vị trí | Nội dung mô tả | Tác động xuôi tuyến |
| --- | --- | --- | --- |
| **Mô tả** | **Tạo nhanh** | Mô tả ước tính cụ thể. | Trường này mặc định sẽ là thông tin chi tiết mô tả hợp đồng liên quan cho các chi phí được tạo tự động. |
| **Lớp giao dịch** | **Tạo nhanh** | Trình đơn thả xuống này là danh sách các lớp giao dịch có trong tab **Chung** của phần mô tả hợp đồng dựa trên dự án. | Trường này mặc định sẽ là thông tin chi tiết mô tả hợp đồng liên quan cho các chi phí được tạo tự động. |
| **Vai trò** | **Tạo nhanh** | Vai trò của người đang thực hiện công việc này hoặc chịu chi phí này. | Trường này mặc định sẽ là thông tin chi tiết mô tả hợp đồng liên quan cho các chi phí được tạo tự động. |
| **Danh mục** | **Tạo nhanh** | Thể loại của công việc hoặc chi phí. | Trường này mặc định sẽ là thông tin chi tiết mô tả hợp đồng liên quan cho các chi phí được tạo tự động. |
| **Ngày bắt đầu** | **Tạo nhanh** | Ngày bắt đầu công việc. | Trường này mặc định sẽ là thông tin chi tiết mô tả hợp đồng liên quan cho các chi phí được tạo tự động. |
| **Ngày kết thúc** | **Tạo nhanh** | Ngày kết thúc công việc. | Trường này mặc định sẽ là thông tin chi tiết mô tả hợp đồng liên quan cho chi phí được tạo tự động. |
| **Đơn vị Nguồn lực** | **Tạo nhanh** | Đơn vị cung ứng nguồn lực chịu chi phí này và cung cấp nguồn lực để thực hiện. | Trường này mặc định sẽ là thông tin chi tiết mô tả hợp đồng liên quan cho các chi phí được tạo tự động. Trường này cũng được sử dụng trong truy xuất giá vốn. |
| **Lịch trình đơn vị** | **Tạo nhanh** | Nhóm đơn vị đo của công việc hoặc chi phí. Các đơn vị thuộc một lịch trình đơn vị hoặc một nhóm đơn vị. Ví dụ: *dặm* và *ki lô mét (km)* là các đơn vị thuộc nhóm đơn vị mô tả khoảng cách. | Trường này mặc định sẽ là thông tin chi tiết mô tả hợp đồng liên quan cho các chi phí được tạo tự động. |
| **Đơn vị** | **Tạo nhanh** | Đơn vị đo lường công việc hoặc chi phí. | Trường này mặc định sẽ là thông tin chi tiết mô tả hợp đồng liên quan cho các chi phí được tạo tự động. |
| **Số lượng** | **Tạo nhanh** | Số lượng công việc hoặc chi phí. | Trường này mặc định sẽ là thông tin chi tiết mô tả hợp đồng liên quan cho các chi phí được tạo tự động. |
| **Giá đơn vị** | **Tạo nhanh** | Tỷ lệ thanh toán của vai trò đang thực hiện công việc hoặc giá bán của loại chi phí. Trường này lấy giá trị mặc định cho **Thời gian** dựa theo tổ hợp vai trò và đơn vị cung ứng nguồn lực trên bảng giá dự án có hiệu lực vào ngày bắt đầu. Đối với chi phí, giá trị mặc định của trường này chính là mức giá thiết lập cho thể loại giao dịch trong bảng giá dự án có hiệu lực vào ngày bắt đầu. Nếu phương thức tính giá cho thể loại giao dịch không phải là **đơn giá**, thì không có giá trị mặc định và trường này được để trống. | Tỷ lệ chi phí của vai trò đang thực hiện công việc hoặc đơn giá của thể loại chi phí. Trường này lấy giá trị mặc định cho **Thời gian dựa theo tổ hợp vai trò** và đơn vị cung ứng nguồn lực trên dòng mô tả giá theo vai trò của bảng giá vốn được đính kèm với đơn vị ký hợp đồng có hiệu lực vào ngày bắt đầu. Đối với chi phí, giá trị mặc định của trường này dựa trên dòng mô tả mức giá theo thể loại của bảng giá vốn được đính kèm với đơn vị ký hợp đồng có hiệu lực vào ngày bắt đầu. Nếu phương thức tính giá cho danh mục giao dịch không phải là giá mỗi đơn vị, thì không có giá trị mặc định và trường này được để trống. |
| **Thuế Ước tính** | **Tạo nhanh** | Thuế ước tính cho công việc hoặc chi phí này do người dùng nhập. | Thuế ước tính cho công việc hoặc chi phí này do người dùng nhập. |
| **Số lượng** | **Tạo nhanh** | Giá trị trong trường này có thể do người dùng thêm nếu các trường **Số lượng** và **Giá** được để trống. Nếu **Số lượng** và **Giá** đã được điền, thì trường **Số tiền** là trường chỉ đọc và được tính là **(Số lượng \* Đơn giá) + Thuế**. | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a>Cập nhật giá trên chi tiết mô tả hợp đồng

Nếu thay đổi các mức giá trên bảng giá dự án được đính kèm với hợp đồng hoặc bảng giá vốn của đơn vị ký hợp đồng, bạn có thể làm mới các mức giá cho từng chi tiết mô tả hợp đồng để phản ánh sự thay đổi. Trên trang **Hợp đồng**, chọn **Tính toán lại**. Một cảnh báo sẽ mở ra để thông báo cho bạn biết rằng mức giá của tất cả các dòng mô tả hợp đồng trên hợp đồng này đã được đặt lại. Chọn **Có** để làm mới giá cho cả chi tiết mô tả hợp đồng bán hàng và chi phí.

## <a name="access-contract-line-details-for-cost"></a>Truy cập vào chi tiết mô tả hợp đồng để biết chi phí

Trên tab **Chi tiết mô tả hợp đồng**, chọn một hàng trong lưới để hiển thị các tác vụ trên thanh công cụ của lưới con. Tác vụ đầu tiên trên thanh công cụ của lưới con là **Mở chi tiết chi phí**. Để xem tỷ lệ chi phí liên quan và số tiền có trong chi tiết mô tả hợp đồng, chọn **Mở chi tiết chi phí**. 

> [!NOTE]
> Việc thay đổi công ty cung ứng nguồn lực, đơn vị cung ứng nguồn lực, số lượng, ngày tháng, vai trò hoặc giá trị thể loại trên chi tiết mô tả **Chi phí** của hợp đồng cũng sẽ làm thay đổi các giá trị tương ứng trên chi tiết mô tả **Doanh thu** của hợp đồng.

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a>Đơn vị tiền tệ trên các chi tiết mô tả chi phí và doanh thu của hợp đồng

Chi tiết mô tả **Doanh thu** của hợp đồng lấy đơn vị tiền tệ của bảng giá dự án có hiệu lực vào ngày bắt đầu của chi tiết mô tả hợp đồng làm đơn vị tiền tệ mặc định.

Chi tiết mô tả **Chi phí** của hợp đồng lấy đơn vị tiền tệ từ bảng giá của đơn vị ký kết hợp đồng có hiệu lực vào ngày bắt đầu của chi tiết mô tả **Chi phí** của hợp đồng làm đơn vị tiền tệ mặc định.

Các tính toán lợi nhuận chuyển đổi số tiền trong chi tiết mô tả **Chi phí** và **Doanh thu** của hợp đồng sang đơn vị tiền tệ cơ sở của môi trường để báo cáo tổng lợi nhuận thực tế và ước tính trên hợp đồng.

> [!NOTE]
> Lỗi làm tròn theo đơn vị tiền tệ và thay đổi lợi nhuận có thể xảy ra do thiếu tỷ giá hối đoái thực tế theo ngày. Chỉ sử dụng các tính toán trên những hợp đồng dự án này dưới dạng ước lượng và không áp dụng cho các báo cáo thực tế theo luật định hoặc các báo cáo khác đòi hỏi độ chính xác cao hơn liên quan đến việc làm tròn và tỷ giá hối đoái thực tế theo ngày.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]