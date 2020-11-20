---
title: Thiết lập trường tùy chỉnh làm thông số định giá
description: Chủ đề này cung cấp thông tin về cách thiết lập thông số định giá bằng các trường tùy chỉnh.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 67e891d8576cd92f48466929fc53fe8a4203d72d
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119444"
---
# <a name="set-up-custom-fields-as-pricing-dimensions"></a>Thiết lập trường tùy chỉnh làm thông số định giá

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Trước khi bắt đầu, chủ đề này giả định rằng bạn đã hoàn tất quy trình trong các chủ đề, [Tạo trường và thực thể tùy chỉnh](create-custom-fields-entities-pricing-dimensions.md) và [Thêm các trường tùy chỉnh bắt buộc vào thực thể thiết lập giá và giao dịch](add-custom-fields-price-setup-transactional-entities.md). Nếu bạn chưa hoàn thành các quy trình đó, hãy quay lại và hoàn thành chúng rồi trở lại chủ đề này. 

Chủ đề này cung cấp thông tin về cách thiết lập thông số định giá tùy chỉnh. Trên trang **Tham số**, tab **Thông số định giá dựa trên số lượng** hiển thị các bản ghi trong thực thể thông số định giá. Theo mặc định, có hai hàng trong lưới trên tab này:

- **msdyn_resourcecategory** (Vai trò)
- **msdyn_OrganizationalUnit** (Đơn vị tổ chức)

> [!IMPORTANT]
> Không xóa các hàng này. Tuy nhiên, nếu không cần chúng, bạn có thể khiến chúng không áp dụng được trong một ngữ cảnh cụ thể bằng cách đặt **Áp dụng cho Chi phí**, **Áp dụng cho Doanh số** và **Áp dụng cho Lượt mua hàng** đều thành **Không**. Việc đặt các giá trị thuộc tính này thành **Không** có tác dụng tương tự như không có trường là thông số định giá.

Để một trường trở thành thông số định giá, trường đó phải:

- Được tạo dưới dạng trường trong các thực thể **Giá theo vai trò** và **Tăng Giá theo vai trò**. Để biết thêm thông tin về cách thực hiện, hãy xem phần [Thêm trường tùy chỉnh vào các thực thể giao dịch và thiết lập giá](add-custom-fields-price-setup-transactional-entities.md).
- Tạo dưới dạng hàng trong bảng **Thông số định giá**. Ví dụ: thêm các hàng thông số định giá như hiển thị trong đồ thị sau. 

Số giờ Làm việc của nguồn lực (**msdyn_resourceworkhours**) được thêm vào dưới dạng thông số dựa trên mức tăng và đã được thêm vào lưới trên tab **Thông số định giá dựa trên mức tăng**.

> [!IMPORTANT]
> Mọi thay đổi với dữ liệu thông số định giá trong bảng này, dù là hiện có hay mới, chỉ được truyền đến logic kinh doanh định giá sau khi làm mới bộ đệm ẩn. Thời gian làm mới bộ đệm ẩn có thể mất đến 10 phút. Cho phép khoảng thời gian đó để xem các thay đổi trong logic giá mặc định phải bắt nguồn từ những thay đổi với dữ liệu Thông số định giá.


## <a name="attributes-of-the-pricing-dimensions-table"></a>Các thuộc tính của bảng Thông số định giá
Phần sau đây cung cấp thông tin về các thuộc tính **khác nhau** trong bảng giá kích thước.

### <a name="pricing-dimension-name"></a>Tên thông số định giá
Giá trị này phải chính xác giống như tên sơ đồ của trường được thêm vào bảng **Giá theo vai trò** cho các thông số định giá tùy chỉnh. Để biết thêm thông tin về cách thêm các trường vào bảng **Giá theo vai trò**, hãy xem [Thêm trường tùy chỉnh vào các thực thể giao dịch và thiết lập giá](add-custom-fields-price-setup-transactional-entities.md).

### <a name="type-of-dimension"></a>Loại thông số
Có hai loại thông số định giá:
  
  - **Thông số dựa trên số tiền**: Giá trị thông số từ ngữ cảnh đầu vào được khớp với giá trị thứ nguyên trên dòng **Giá theo vai trò** và giá/chi phí được đặt mặc định ngay trong bảng **Giá theo vai trò**.
  - **Thông số dựa trên mức tăng**: Đây là các thông số mà quy trình 3 bước sau đây sẽ được sử dụng để có được giá/chi phí:
 
    1. Các giá trị thông số không dựa trên mức tăng từ ngữ cảnh đầu vào được khớp với dòng Giá theo vai trò để có được giá cơ sở.
    2. Các giá trị thông số từ ngữ cảnh đầu vào được khớp với dòng **Mức tăng Giá theo vai trò** để có được tỷ lệ phần trăm mức tăng.
    3. Tỷ lệ phần trăm mức tăng từ bước thứ hai được áp dụng cho giá cơ sở thu được từ bảng **Giá theo vai trò** trong bước đầu tiên để có giá/chi phí cuối cùng.
   
   Bảng sau minh họa cách tính mức tăng giá.
  
| Vai trò        | Đơn vị tổ chức    |Vị trí làm việc      |Tiêu đề chuẩn      |Giờ làm việc của nguồn lực      |  Tăng giá|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | Contoso Ấn Độ|Tại Cơ sở            |                    |Làm thêm                 |15     |
|             | Contoso Ấn Độ|Cục bộ             |                    |Làm thêm                 |10     |
|             | Contoso US   |Cục bộ             |                    |Làm thêm                 |20     |


Nếu một nguồn lực từ Contoso Ấn Độ có giá cơ sở là 100 USD đang làm việc tại cơ sở, họ ghi 8 giờ làm việc bình thường và 2 giờ làm thêm vào mục nhập thời gian, thì công cụ định giá sẽ sử dụng giá cơ sở là 100 cho 8 giờ để thành 800 USD. Đối với 2 giờ làm thêm, mức tăng giá 15% sẽ được áp dụng cho giá cơ sở 100 để có đơn giá là 115 USD và sẽ ghi lại tổng chi phí là 230 USD.

### <a name="applicable-to-cost"></a>Áp dụng cho chi phí 
Nếu được đặt thành **Có**, thì tùy chọn này chỉ ra rằng giá trị thông số từ ngữ cảnh đầu vào sẽ được dùng để khớp với **Giá theo vai trò** và **Mức tăng Giá theo vai trò** khi truy xuất chi phí và mức tăng giá.

### <a name="applicable-to-sales"></a>Áp dụng cho Doanh số
Nếu được đặt thành **Có**, thì tùy chọn này chỉ ra rằng giá trị thông số từ ngữ cảnh đầu vào sẽ được dùng để khớp với **Giá theo vai trò** và **Mức tăng Giá theo vai trò** khi truy xuất hóa đơn và mức tăng giá.

### <a name="applicable-to-purchase"></a>Áp dụng cho Mua hàng
Nếu được đặt thành **Có**, thì tùy chọn này chỉ ra rằng giá trị thông số từ ngữ cảnh đầu vào sẽ được dùng để khớp với **Giá theo vai trò** và **Mức tăng Giá theo vai trò** khi truy xuất giá mua. Không hỗ trợ các kịch bản thầu phụ, nên trường này không được dùng. 

### <a name="priority"></a>Mức độ ưu tiên
Việc đặt ra ưu tiên thông số sẽ giúp tính năng định giá tạo ra giá ngay cả khi không thể tìm thấy sự phù hợp chính xác giữa giá trị thông số đầu vào và giá trị từ các bảng **Giá theo vai trò** hoặc **Mức tăng Giá theo vai trò**. Trong trường hợp này, giá trị rỗng được sử dụng cho các giá trị thông số không phù hợp bằng cách tính trọng số theo thứ tự ưu tiên.

- **Ưu tiên về chi phí**: Giá trị ưu tiên chi phí của một thông số sẽ chỉ ra trọng số của thông số đó khi so khớp trong quá trình thiết lập giá chi phí. Giá trị **Ưu tiên chi phí** phải là duy nhất trên các thông số **Áp dụng cho chi phí**.
- **Ưu tiên về doanh số**: Giá trị ưu tiên doanh số của một thông số sẽ chỉ ra trọng số của thông số đó khi so khớp trong quá trình thiết lập giá bán hàng hoặc tỷ suất hóa đơn. Giá trị **Ưu tiên doanh số** phải là duy nhất trên các thông số **Áp dụng cho doanh số**.
