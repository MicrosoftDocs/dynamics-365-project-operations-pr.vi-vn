---
title: Thiết lập tỷ lệ hóa đơn lao động – bản đơn giản
description: Chủ đề này cung cấp thông tin về cách thiết lập tỷ lệ thanh toán nhân công trong Project Operations.
author: rumant
manager: Annbe
ms.date: 10/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cf53f6909ed5fb9b143197118c799b9803699171
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181208"
---
# <a name="set-up-labor-bill-rates---lite"></a>Thiết lập tỷ lệ hóa đơn lao động – bản đơn giản

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Mỗi bảng giá có một tập hợp giá theo vai trò hoặc giá nhân công, hiệu quả cho ngữ cảnh và ngày hiệu quả có trên tiêu đề bảng giá. Tỷ giá hóa đơn cho thời gian trong Dynamics 365 Project Operations chỉ có thể được thiết lập bằng một đơn vị tiền tệ, là đơn vị tiền tệ trên tiêu đề Bảng giá.

1. Để thiết lập tỷ lệ hóa đơn nhân công cho một bảng giá bán hàng, hãy tạo một bảng giá dựa trên tiêu đề bảng giá. 
2. Trên tab **Giá theo vai trò**, trong lưới con, hãy chọn **+ Giá theo vai trò mới**. 
3. Trên ngăn **Tạo nhanh**, nhập tổ hợp vai trò và đơn vị tổ chức mà bạn cần thiết lập tỷ lệ thanh toán.

  Bảng sau bao gồm các trường trên tab **Tổng quát** và ngăn **Tạo nhanh** của mô tả giá theo vai trò mà bạn cần lưu ý khi tạo giá theo vai trò trên bảng giá bán hoặc bảng giá bán hàng:

  | Trường | Vị trí | Nội dung mô tả | Tác động xuôi tuyến |
  | --- | --- | --- | --- |
  | Vai trò | Tab **Tổng quát** và ngăn **Tạo nhanh** | Chọn vai trò mà bạn đang đặt tỷ lệ thanh toán. | Vai trò trên giá trị ước tính sắp đến hoặc thực tế sẽ được đối chiếu với mô tả này để đặt mặc định tỷ lệ thanh toán của vai trò. |
  | Đơn vị Nguồn lực | Tab **Tổng quát** và ngăn **Tạo nhanh** | Chọn đơn vị tổ chức hoặc bộ phận của công ty có vai trò. Ví dụ: một nhà phát triển từ bộ phận Robotics của Fabrikam Ấn Độ hoặc một nhà phát triển từ bộ phận Phần mềm của Fabrikam Hoa Kỳ. | Đơn vị cung cấp nguồn lực trên giá trị ước tính sắp đến hoặc thực tế sẽ được đối chiếu với mô tả này để đặt mặc định tỷ lệ thanh toán của vai trò. |
  | Giá | Tab **Tổng quát** và ngăn **Tạo nhanh** | Thiết lập tỷ lệ thanh toán cho tổ hợp công ty cung cấp vai trò và đơn vị cung cấp nguồn lực. Ví dụ: nhà phát triển từ Fabrikam Ấn Độ có tỷ lệ thanh toán là 100 USD hoặc nhà phát triển từ Fabrikam Hoa Kỳ có tỷ lệ thanh toán là 150 USD. | Giá này là tỷ lệ thanh toán mặc định trên giá trên đơn vị hoặc chi phí của ước tính đến hoặc mô tả thực tế cho loại giao dịch Thời gian. |
  | Tiền tệ | Tab **Tổng quát** và ngăn **Tạo nhanh**| Theo mặc định, giá trị đơn vị tiền tệ đến từ đơn vị tiền tệ trên tiêu đề của bảng giá bán hàng. Trên bảng giá bán hàng, không thể ghi đè đơn vị tiền tệ. | Đơn vị tiền tệ này là đơn vị tiền tệ mặc định dựa trên đơn giá của mô tả thực tế đến cho loại giao dịch chi phí thời gian. |
  | Lịch trình Đơn vị | Tab **Tổng quát** và ngăn **Tạo nhanh** | Lịch trình đơn vị này mặc định là Thời gian và không thể thay đổi trên thực thể Giá theo vai trò vì nó được sử dụng để biểu thị giá theo đơn vị thời gian. | Không có tác động xuôi tuyến đối với trường này. |
  | Đơn vị | Tab **Tổng quát** và ngăn **Tạo nhanh** | Giá trị đơn vị đến từ trường **Đơn vị thời gian** trên tiêu đề bảng giá bán hàng. Nhưng có thể ghi đè giá trị này. Ví dụ: một nhà phát triển từ Fabrikam Ấn Độ có tỷ lệ thanh toán là 1000 USD trên mỗi **Ngày Ấn Độ**. Một nhà phát triển từ Fabrikam Hoa Kỳ có tỷ lệ thanh toán là 1500 USD trên mỗi **Ngày Hoa Kỳ**. | Khi giá mỗi đơn vị mặc định trên một mô tả ước tính đến hoặc thực tế, hệ thống sử dụng hệ thống đơn vị và chuyển đổi theo đơn vị cơ sở để tính giá mỗi đơn vị. Ví dụ: ước tính là 10 **Ngày Ấn Độ** giá trị công việc của một Nhà phát triển đến từ Ấn Độ và đơn vị Ngày Ấn Độ được định nghĩa là 10 giờ. Khi định giá mô tả ước tính đó, ứng dụng sẽ tính đơn giá trên ước tính là 1000 USD/10 giờ = 100 USD mỗi giờ. |


## <a name="transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions"></a>Chuyển giá hoặc thiết lập tỷ lệ thanh toán cho các nguồn lực từ các đơn vị tổ chức hoặc bộ phận khác 

Các công ty dựa trên dự án để sử dụng nhân viên từ các bộ phận khác nhau của công ty để làm việc trong các dự án. Các dự án có thể được thực hiện từ một bộ phận trong khi nhân viên hoặc chuyên gia tư vấn đến từ một bộ phận khác của công ty. Dự án cũng có thể được tạo thành từ sự kết hợp của nhiều người từ các bộ phận khác nhau. Trong Project Operations, công ty sở hữu việc bàn giao dự án được gọi là **Đơn vị hợp đồng**. Tất cả các bộ phận khác cung cấp nguồn lực được gọi là **Đơn vị cung cấp nguồn lực**. Do sự khác biệt về chi phí lao động giữa các khu vực địa lý và thị trường lao động trên toàn thế giới, tỷ giá thanh toán cho lao động cũng được thiết lập khác nhau cho các khu vực địa lý khác nhau.

Ví dụ: một nhà phát triển từ Fabrikam Ấn Độ đang làm việc trong một dự án ở Hoa Kỳ được thanh toán ở mức 100 USD mỗi giờ. Một nhà phát triển từ Fabrikam Hoa Kỳ đang làm việc trong Dự án ở Hoa Kỳ được thanh toán ở mức 150 USD mỗi giờ.

### <a name="example-set-up-a-bill-rate"></a>Ví dụ: Thiết lập tỷ lệ thanh toán

1. Tạo một bảng giá bán hàng có tên *Tỷ lệ thanh toán Fabrikam Hoa Kỳ* và đặt hiệu quả ngày.
2. Trong bảng giá bán hàng, hãy nhập thông tin giá sau:

    | Vai trò | Đơn vị tổ chức | Tỷ lệ thanh toán |
    | --- | --- | --- |
    | Nhà phát triển | Fabrikam Ấn Độ | $100 |
    | Nhà phát triển | Fabrikam Philippines | 90 USD |
    | Nhà phát triển | Fabrikam Hoa Kỳ | 150 USD |

3. Đính kèm bảng giá bán hàng, **Tỷ lệ thanh toán Fabrikam Hoa Kỳ** vào bảng giá dự án của hợp đồng dự án hoặc vào một tài khoản nhất định.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]