---
title: Ước tính mô tả hợp đồng dựa trên dự án
description: Bài viết này cung cấp thông tin về các giá trị ước tính trên một mục mô tả hợp đồng dự án.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 633ad3130a28d75ad10b81e03a883e0a732b1ba8
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825239"
---
# <a name="estimate-a-project-based-contract-line"></a>Ước tính mô tả hợp đồng dựa trên dự án

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_ 

Trong Dynamics 365 Project Operations, phần mô tả hợp đồng dựa trên dự án có các chi tiết giúp ước tính chi phí và doanh thu tiềm năng của công việc liên quan để cung cấp cho phần mô tả hợp đồng.

Để đưa ra số liệu ước tính trong phần hợp đồng dựa trên dự án, hãy chuyển đến tab **Chi tiết mô tả hợp đồng** trong phần **Mô tả hợp đồng** dựa trên dự án.  Có 2 cách để tạo số liệu ước tính trong phần mô tả hợp đồng dựa trên dự án, đó là:

   - Tạo trực tiếp số liệu ước tính trên phần mô tả hợp đồng bằng cách thêm các chi tiết mô tả hợp đồng theo cách thủ công.
   - Tạo một dự án và một kế hoạch dự án, sau đó liên kết dự án đó và các nhiệm vụ với phần mô tả hợp đồng của dự án. Thao tác này kích hoạt quy trình để bạn nhập số liệu ước tính của kế hoạch dự án vào phần mô tả hợp đồng dựa trên các thành phần có trong phần mô tả hợp đồng.

## <a name="create-an-estimate-directly-on-a-project-contract-line"></a>Tạo giá trị ước tính ngay trên mục mô tả hợp đồng dự án

Để tạo giá trị ước tính ngay trên mục mô tả hợp đồng dự án, hãy làm theo các bước sau:

1. Chuyển đến phần mô tả hợp đồng và chọn tab **Chi tiết mô tả hợp đồng**. Các dòng bạn tạo trên tab này được tóm tắt và hiển thị dưới dạng **Giá trị hợp đồng** cho phần **Mô tả hợp đồng** này. 
2. Trên lưới con **Chi tiết mô tả hợp đồng**, hãy chọn **Chi tiết mô tả hợp đồng mới**. Một thanh trượt tạo nhanh sẽ mở ra. Các trường sau đây có sẵn trên trang **Chi tiết mô tả hợp đồng**.

| Trường | Vị trí | Mô tả | Tác động xuôi tuyến |
| --- | --- | --- | --- |
| **Mô tả** | **Tạo nhanh** | Mô tả ước tính cụ thể. | Giá trị này mặc định là chi tiết mô tả hợp đồng có liên quan cho chi phí được tạo tự động. |
| **Lớp giao dịch** | **Tạo nhanh** | Danh sách các loại giao dịch này có trong tab **Chung** của mục mô tả hợp đồng dựa trên dự án. | Giá trị này mặc định là chi tiết mô tả hợp đồng có liên quan cho chi phí được tạo tự động. |
| **Chọn sản phẩm** | **Tạo nhanh** | Áp dụng khi loại giao dịch là **Vật tư**. Bạn có thể chọn chỉ định dòng ước tính này là cho một sản phẩm (danh mục) **Hiện có** hoặc một sản phẩm **Chọn thêm**. | Giá trị này mặc định là chi tiết mô tả hợp đồng có liên quan cho chi phí được tạo tự động. |
| **Sản phẩm** | **Tạo nhanh** | ID của sản phẩm từ danh mục sản phẩm. Trường này chỉ được bật khi bạn chọn **Sản phẩm hiện có** bên trong trường **Chọn sản phẩm**. ID được dùng để truy xuất giá bán từ bảng giá dự án trên hợp đồng. | Giá trị này mặc định là chi tiết mô tả hợp đồng có liên quan cho chi phí được tạo tự động. |
| **Sản phẩm chọn thêm** | **Tạo nhanh** | Một trường văn bản để nhập tên của sản phẩm. Trường này chỉ được bật khi bạn chọn **Chọn thêm** bên trong trường **Chọn sản phẩm**.| Giá trị này mặc định là chi tiết mô tả hợp đồng có liên quan cho chi phí được tạo tự động. |
| **Vai trò** | **Tạo nhanh** | Vai trò của người đang thực hiện công việc này hoặc chịu chi phí này. | Giá trị này mặc định là chi tiết mô tả hợp đồng có liên quan cho chi phí được tạo tự động.|
| **Danh mục** | **Tạo nhanh** | Thể loại của công việc hoặc chi phí. | Giá trị này mặc định là chi tiết mô tả hợp đồng có liên quan cho chi phí được tạo tự động.|
| **Ngày bắt đầu** | **Tạo nhanh** | Ngày bắt đầu công việc. | Giá trị này mặc định là chi tiết mô tả hợp đồng có liên quan cho chi phí được tạo tự động. |
| **Ngày kết thúc** | **Tạo nhanh** | Ngày kết thúc công việc. | Giá trị này mặc định là chi tiết mô tả hợp đồng có liên quan cho chi phí được tạo tự động. |
| **Công ty cung cấp nguồn lực** | **Tạo nhanh** | Công ty cung ứng nguồn lực hoặc pháp nhân phải chịu chi phí này và cung cấp nguồn lực để thực hiện nó. | Giá trị này mặc định là chi tiết mô tả hợp đồng có liên quan cho chi phí được tạo tự động và được dùng khi truy xuất giá vốn. |
| **Đơn vị nguồn lực** | **Tạo nhanh** | Đơn vị cung ứng nguồn lực hoặc pháp nhân phải chịu chi phí này và cung cấp nguồn lực để thực hiện nó. | Giá trị này mặc định là chi tiết mô tả hợp đồng có liên quan cho chi phí được tạo tự động và được dùng khi truy xuất giá vốn. |
| **Lịch trình đơn vị** | **Tạo nhanh** | Nhóm đơn vị của công việc, sản phẩm hoặc chi phí. Các đơn vị thuộc một lịch trình đơn vị hoặc một nhóm đơn vị. Ví dụ: *dặm* và *ki lô mét (km)* là các đơn vị thuộc nhóm đơn vị mô tả khoảng cách. | Giá trị này mặc định là chi tiết mô tả hợp đồng có liên quan cho chi phí được tạo tự động. |
| **Đơn vị** | **Tạo nhanh** | Đơn vị của công việc, sản phẩm hoặc chi phí. | Giá trị này mặc định là chi tiết mô tả hợp đồng có liên quan cho chi phí được tạo tự động. |
| **Số lượng** | **Tạo nhanh** | Số lượng công việc, sản phẩm hoặc chi phí. | Giá trị này mặc định là chi tiết mô tả hợp đồng có liên quan cho chi phí được tạo tự động. |
| **Giá đơn vị** | **Tạo nhanh** | Mức lương theo giờ của vai trò đang thực hiện công việc, hoặc chi phí trên một đơn vị của thể loại chi phí hoặc chi phí đơn vị của sản phẩm. Mặc định cho **Thời gian** dựa trên sự kết hợp của các giá trị thứ nguyên về giá trên dòng giá theo vai trò trong bảng giá dự án có hiệu lực cho ngày bắt đầu. Đối với **Chi phí**, giá trị mặc định cho trường này là từ giá được thiết lập cho thể loại giao dịch trong bảng giá dự án có hiệu lực cho ngày bắt đầu. Nếu phương thức tính giá cho thể loại giao dịch không phải là **đơn giá**, thì không có giá trị mặc định và trường này được để trống. Đối với sản phẩm, giá trị mặc định của trường này dựa trên dòng **Hạng mục trong bảng giá** của bảng giá dự án có hiệu lực cho ngày bắt đầu.| Tỷ lệ chi phí của vai trò đang thực hiện công việc, hoặc chi phí trên một đơn vị của thể loại chi phí hoặc chi phí đơn vị của sản phẩm. Mặc định cho **Thời gian** dựa trên sự kết hợp của các giá trị thứ nguyên về giá trên dòng giá theo vai trò trong bảng giá vốn đính kèm đơn vị hợp đồng có hiệu lực cho ngày bắt đầu. Đối với **Chi phí**, giá trị mặc định cho trường này dựa trên dòng giá theo thể loại trong bảng giá vốn đính kèm với đơn vị hợp đồng có hiệu lực cho ngày bắt đầu. Nếu phương thức tính giá cho danh mục giao dịch không phải là giá mỗi đơn vị, thì không có giá trị mặc định và trường này được để trống. Đối với sản phẩm, giá trị mặc định của trường này dựa trên dòng **Hạng mục trong bảng giá** của bảng giá vốn đính kèm với đơn vị hợp đồng có hiệu lực cho ngày bắt đầu.|
| **Thuế Ước tính** | **Tạo nhanh** | Thuế ước tính cho công việc hoặc chi phí này do người dùng nhập. | &nbsp; |
| **Số lượng** | **Tạo nhanh** | Có thể thêm giá trị trong trường này nếu các trường **Số lượng** và **Giá** được để trống. Nếu các trường **Số lượng** và **Giá** được điền, trường **Số tiền** sẽ ở chế độ chỉ đọc và được tính theo công thức **(Số lượng \* Đơn giá) + Thuế**. | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a>Cập nhật giá trên chi tiết mô tả hợp đồng

Nếu thay đổi các mức giá trên bảng giá dự án được đính kèm với hợp đồng hoặc bảng giá vốn của đơn vị ký hợp đồng, bạn có thể làm mới các mức giá cho từng chi tiết mô tả hợp đồng để phản ánh sự thay đổi. Trên trang **Hợp đồng**, chọn **Tính toán lại**. Một cảnh báo xuất hiện để thông báo cho bạn rằng giá cho tất cả các mô tả hợp đồng trên hợp đồng này đã được đặt lại. Chọn **Có** để làm mới giá cho cả chi tiết mô tả hợp đồng bán hàng và chi phí.

## <a name="access-contract-line-details-for-cost"></a>Truy cập vào chi tiết mô tả hợp đồng để biết chi phí

Trên tab **Chi tiết mô tả hợp đồng**, chọn một hàng trong lưới để hiển thị các tác vụ trên thanh công cụ của lưới con. Tác vụ đầu tiên trên thanh công cụ của lưới con là **Mở chi tiết chi phí**. Để xem tỷ lệ chi phí liên quan và số tiền có trong chi tiết mô tả hợp đồng, chọn **Mở chi tiết chi phí**. 

> [!NOTE]
> Việc thay đổi công ty cung ứng nguồn lực, đơn vị cung ứng nguồn lực, số lượng, ngày tháng, vai trò hoặc giá trị thể loại trên chi tiết mô tả **Chi phí** của hợp đồng cũng sẽ làm thay đổi các giá trị tương ứng trên chi tiết mô tả **Doanh thu** của hợp đồng.

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a>Đơn vị tiền tệ trên các chi tiết mô tả chi phí và doanh thu của hợp đồng

Chi tiết mô tả **Doanh thu** của hợp đồng lấy đơn vị tiền tệ của bảng giá dự án có hiệu lực vào ngày bắt đầu của chi tiết mô tả hợp đồng làm đơn vị tiền tệ mặc định.

Chi tiết mô tả **Chi phí** của hợp đồng lấy đơn vị tiền tệ từ bảng giá của đơn vị ký kết hợp đồng có hiệu lực vào ngày bắt đầu của chi tiết mô tả **Chi phí** của hợp đồng làm đơn vị tiền tệ mặc định.

Các tính toán lợi nhuận chuyển đổi số tiền trong chi tiết mô tả **Chi phí** và **Doanh thu** của hợp đồng sang đơn vị tiền tệ cơ sở của môi trường để báo cáo tổng lợi nhuận thực tế và ước tính trên hợp đồng.

> [!NOTE]
> Lỗi làm tròn theo đơn vị tiền tệ và thay đổi lợi nhuận có thể xảy ra do thiếu tỷ giá hối đoái thực tế theo ngày. Chỉ sử dụng các tính toán này trên các hợp đồng dự án vì đây là các ước tính và không áp dụng cho báo cáo thực tế theo luật định hoặc báo cáo khác đòi hỏi độ chính xác cao hơn khi làm tròn và biết rõ tính hiệu lực của ngày đối với tỷ giá hối đoái.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
