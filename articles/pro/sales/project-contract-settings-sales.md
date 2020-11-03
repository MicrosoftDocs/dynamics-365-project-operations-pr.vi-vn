---
title: Trường hợp đồng dự án và thông tin
description: Chủ đề này cung cấp thông tin về các trường ảnh hưởng đến mô tả hợp đồng và thông tin về hợp đồng được tóm tắt trên tất cả các mục hàng.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 082292c54682022933a4b46b856f9241078a9067
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/21/2020
ms.locfileid: "4088161"
---
# <a name="project-contract-fields-and-information"></a>Trường hợp đồng dự án và thông tin 

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Chủ đề này cung cấp thông tin về các trường áp dụng cho toàn bộ hợp đồng dự án bao gồm các thiết đặt ảnh hưởng đến tất cả mô tả hợp đồng. Thông tin về hợp đồng được tóm tắt trên tất cả các mục hàng để thúc đẩy KPI của hợp đồng dự án cũng được bao gồm.

Bảng sau liệt kê các trường thông tin tóm tắt trên hợp đồng dự án dành riêng cho Dynamics 365 Project Operations hoặc có một số thay đổi quan trọng về hành vi từ đơn bán hàng trong Dynamics 365 Sales.

| Trường | Vị trí | Mức độ liên quan, mục đích và hướng dẫn | Tác động xuôi tuyến |
| --- | --- | --- | --- |
| Loại | Tab **Tóm tắt** (ẩn) | Đây là trường bộ tùy chọn có các tùy chọn sau:</br>- **Dựa trên công việc** (Chỉ khả dụng khi Project Operations được cài đặt)</br>- **Dựa trên mục** (Chỉ khả dụng khi Project Operations và Sales được cài đặt)</br>- **Dựa trên bảo trì dịch vụ** (Khả dụng khi Dynamics 365 Field Service được cài đặt) | Trong Project Operations, giá trị của trường này mặc định là **Dựa trên công việc** và phân loại hợp đồng là hợp đồng dựa trên dự án. Hợp đồng phải dựa trên dự án để kích hoạt tất cả các tiện ích và chức năng dành riêng cho dự án. |
| Khách hàng Tiềm năng | Tab **Tóm tắt** | Tham chiếu đến bản ghi công ty hoặc tài khoản của khách hàng. Khi hợp đồng được tạo từ một báo giá, trường này được sao chép từ trường tương ứng trên bản ghi báo giá. | Đơn vị tiền tệ trên hợp đồng dự án được mặc định dựa trên đơn vị tiền tệ của khách hàng. Có thể thay đổi đơn vị tiền tệ trước khi lưu hợp đồng. |
| Người quản lý khách hàng | Tab **Tóm tắt** | Tên của Quản lý khách hàng cho thỏa thuận này. Khi hợp đồng được tạo từ một báo giá, trường này được sao chép từ trường tương ứng trên bản ghi báo giá. | Quản lý khách hàng chịu trách nhiệm quản lý mối quan hệ với khách hàng thông qua việc hoàn thành dự án này. Dựa trên bản ghi tài nguyên có thể đặt trước liên kết với Quản lý khách hàng, đơn vị ký hợp đồng mặc định trên hợp đồng dự án. |
| Đơn vị Hợp đồng | Tab **Tóm tắt** | Đơn vị tổ chức chịu trách nhiệm bàn giao dự án liên quan đến hợp đồng này. Khi hợp đồng được tạo từ một báo giá, trường này được sao chép từ trường tương ứng trên bản ghi báo giá. | Đơn vị ký hợp đồng là bộ phận của công ty sẽ thực hiện các dự án. Mỗi đơn vị ký hợp đồng đều có một loại tiền tệ và đơn vị tiền tệ này được sử dụng để báo cáo chi phí ước tính và thực tế phát sinh trong dự án. |
| Bảng giá sản phẩm | Tab **Tóm tắt** | Bảng giá này dùng làm giá mặc định cho các mô tả hợp đồng theo sản phẩm. Danh sách các tùy chọn thả xuống cho trường này hiển thị danh sách các bảng giá trong đó đơn vị tiền tệ của bảng giá khớp với đơn vị tiền tệ trên hợp đồng. Khi hợp đồng được tạo từ một báo giá, trường này được sao chép từ trường tương ứng trên bản ghi báo giá. Trên hợp đồng dự án, trường này được mặc định từ bản ghi tài khoản nhưng có thể thay đổi. | Không có mức độ liên quan xuôi tuyến cho trường này. |
| Tiền tệ | Tab **Tóm tắt** | Đơn vị tiền tệ được sử dụng để báo cáo giá trị của thỏa thuận này và đơn vị tiền tệ mà khách hàng sẽ được lập hóa đơn. Khi hợp đồng được tạo từ một báo giá, trường này được sao chép từ trường tương ứng trên bản ghi báo giá. Trên hợp đồng dự án, trường này được mặc định từ bản ghi tài khoản nhưng có thể thay đổi. | Sau khi hợp đồng được lưu, trường này không chỉnh sửa được nữa. Trường này được dùng để mặc định bảng giá sản phẩm và dự án trên hợp đồng. Đơn vị tiền tệ trên hợp đồng được dùng để khớp với đơn vị tiền tệ trên bảng giá. |
| Giới hạn không vượt quá | Tab **Tóm tắt** | Trường này cho biết giới hạn đã thương lượng về giá trị cuối cùng mà khách hàng đã đồng ý cho thỏa thuận này. | Giới hạn này được đánh giá trong quá trình thực hiện và có thể áp dụng cho tất cả các mục mô tả và dự án liên quan đến thỏa thuận này. |
| Ngày giao hàng đã yêu cầu | Tab **Tóm tắt** | Khi hợp đồng được tạo từ một báo giá dự án, trường này được sao chép từ trường tương ứng trên báo giá dự án. | Ngày này được sử dụng làm ngày kết thúc để tạo lịch trình hóa đơn. |

Các KPI sau đây có sẵn trên tab **Hiệu suất hợp đồng** của hợp đồng dự án.

| Trường | Vị trí | Mức độ liên quan, mục đích và hướng dẫn |
| --- | --- | --- |
| Giá trị hợp đồng | Hợp đồng tổng thể | Tổng giá trị của Hợp đồng dự án. |
| Số tiền Đã lập hóa đơn thanh toán | Hợp đồng tổng thể | Tổng số tiền trên tất cả các hóa đơn đối với hợp đồng này. |
| Chi phí phát sinh | Hợp đồng tổng thể | Tổng của tất cả các chi phí thực tế được ghi lại trên tất cả các dự án được ánh xạ đến hợp đồng. |
| Lãi gộp | Hợp đồng tổng thể | Số tiền được lập hóa đơn - Chi phí phát sinh cho đến ngày/Số tiền được lập hóa đơn |
| Lợi nhuận Dự kiến | Hợp đồng tổng thể | (Giá trị hợp đồng - Chi phí ước tính)/Giá trị hợp đồng Chi phí ước tính = Tổng của tất cả các chi phí ước tính trên tất cả các dự án được ánh xạ trong hợp đồng.|
| Giá trị hợp đồng | Mô tả dựa trên dự án | Giá trị của mô tả hợp đồng. |
| Số tiền đã lập hóa đơn thanh toán | Mô tả dựa trên dự án | Đối với mô tả hợp đồng giá cố định: Tổng số tiền trên tất cả các giá trị thực tế về mốc doanh số được lập hóa đơn đối với mô tả hợp đồng này trên các hóa đơn khác nhau được tạo cho hợp đồng này. Đối với mô tả hợp đồng thời gian và vật tư: Tổng số tiền trên tất cả các giá trị thực tế về doanh số được lập hóa đơn có thể tính phí được đối với mô tả hợp đồng này trên các hóa đơn khác nhau được tạo cho hợp đồng này. |
| Chi phí phát sinh | Mô tả dựa trên dự án | Tổng của tất cả các chi phí thực tế được ghi lại trên tất cả các dự án được ánh xạ đến mô tả hợp đồng. |
| Lãi gộp | Mô tả dựa trên dự án | (Số tiền được lập hóa đơn - Chi phí phát sinh cho đến ngày)/Số tiền được lập hóa đơn |
| Lợi nhuận Dự kiến | Mô tả dựa trên dự án | (Số tiền mô tả hợp đồng tính theo đơn vị tiền tệ cơ sở - Chi phí ước tính cho mô tả hợp đồng tính theo đơn vị tiền tệ cơ sở)/Số tiền mô tả hợp đồng tính theo đơn vị tiền tệ cơ bản |
| Chi phí phát sinh | Chi tiết về mô tả dựa trên dự án | Thời gian: Tổng lượng thời gian trên giá trị thực tế chi phí thời gian được ghi lại cho vai trò này trên dự án được ánh xạ tới mô tả hợp đồng này. Chi phí: Tổng số tiền trên giá trị thực tế chi phí thời gian được ghi lại cho danh mục này trên dự án được ánh xạ tới mô tả hợp đồng này. |
| Số lượng đã ghi lại | Chi tiết về mô tả dựa trên dự án | Thời gian: Tổng số giá trị thực tế chi phí thời gian cho một vai trò trong dự án được ánh xạ tới mô tả hợp đồng này. Chi phí: Tổng số lượng cho danh mục chi phí này trên giá trị thực tế chi phí trên dự án được ánh xạ tới mô tả hợp đồng này. |
| Số tiền Đã lập hóa đơn thanh toán | Chi tiết về mô tả dựa trên dự án | Đối với mô tả hợp đồng giá cố định, trường này được để trống ở cấp chi tiết và chỉ được hiển thị ở cấp mô tả hợp đồng. Đối với mô tả hợp đồng thời gian và vật tư, các tính toán được hoàn thành ở cấp độ chi tiết. Chi tiết hiển thị tổng số tiền trên tất cả các dòng doanh thu được lập hóa đơn so với mô tả hợp đồng có tính phí này. |
| Số lượng Đã lập hóa đơn thanh toán | Chi tiết về mô tả dựa trên dự án | Đối với mô tả hợp đồng giá cố định, trường này được để trống ở cấp chi tiết và chỉ được hiển thị ở cấp mô tả hợp đồng. Đối với mô tả hợp đồng thời gian và vật tư, các tính toán được hoàn thành ở cấp độ chi tiết cho thời gian và chi phí. Thời gian: Tổng số tiền trên tất cả các dòng doanh thu được lập hóa đơn cho vai trò này so với mô tả hợp đồng có tính phí này. Chi phí: Tổng số lượng cho danh mục chi phí này trên giá trị thực tế chi phí trên dự án được ánh xạ tới mô tả hợp đồng này. |
| Giá trị hợp đồng | Dòng dựa trên sản phẩm | Giá trị mô tả hợp đồng của mô tả hợp đồng dựa trên sản phẩm này. |
| Số tiền Đã lập hóa đơn thanh toán | Dòng dựa trên sản phẩm | Tổng số tiền trên tất cả các dòng hóa đơn đối với mô tả hợp đồng dựa trên sản phẩm này trên các hóa đơn khác nhau được tạo cho hợp đồng này. |
| Chi phí phát sinh | Dòng dựa trên sản phẩm | Tổng của tất cả các chi phí thực tế được ghi lại cho mô tả hợp đồng dựa trên sản phẩm. |
| Lãi gộp | Mô tả dựa trên dự án | Số tiền được lập hóa đơn - Chi phí phát sinh cho đến ngày/Số tiền được lập hóa đơn |
| Lợi nhuận Dự kiến | Dòng dựa trên sản phẩm | (Giá trị mô tả hợp đồng - Chi phí ước tính cho mô tả hợp đồng)/Giá trị mô tả hợp đồng |