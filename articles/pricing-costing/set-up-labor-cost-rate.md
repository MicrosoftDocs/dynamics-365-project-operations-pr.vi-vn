---
title: Thiết lập tỷ lệ chi phí lao động
description: Chủ đề này cung cấp thông tin về cách thiết lập tỷ lệ chi phí nhân công trong Project Operations
author: rumant
manager: Annbe
ms.date: 10/12/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 697129b65f53359615ea537fe135d657748dd909
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180623"
---
# <a name="set-up-labor-cost-rates"></a>Thiết lập tỷ lệ chi phí lao động

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_


Mỗi bảng giá có một tập hợp giá nhân công (giá theo vai trò) phù hợp với ngữ cảnh và ngày hiệu quả của bảng giá.

1. Tạo một bảng giá và trên tab **Giá vai trò**, trong lưới con, hãy chọn **Vai trò mới**.
2. Trên trang **Tạo nhanh**, chọn vai trò và đơn vị tổ chức.
3. Nhập mọi thông tin vào các trường bắt buộc khác.

Bảng sau đây bao gồm một số trường quan trọng khi tạo giá nhân công trên bảng giá vốn.

| Trường | Vị trí | Nội dung mô tả | Tác động xuôi tuyến |
| --- | --- | --- | --- |
| Vai trò | Tab **Tổng quát** và trang **Tạo nhanh** | Chọn vai trò áp dụng tỷ lệ chi phí. | Vai trò trên giá trị ước tính sắp đến hoặc thực tế sẽ được đối chiếu với mô tả này để đặt mặc định chi phí của vai trò. |
| Công ty cung cấp nguồn lực | Tab **Tổng quát** và trang **Tạo nhanh** | Chọn pháp nhân được gán vai trò. Ví dụ: một nhà phát triển từ Fabrikam Ấn Độ hoặc một nhà phát triển từ Fabrikam Hoa Kỳ. | Công ty cung cấp nguồn lực trên giá trị ước tính sắp đến hoặc thực tế sẽ được đối chiếu với mô tả này để đặt mặc định tỷ lệ chi phí của vai trò. |
| Đơn vị Nguồn lực | Tab **Tổng quát** và trang **Tạo nhanh** | Chọn đơn vị tổ chức hoặc bộ phận của công ty sẽ sử dụng vai trò này. Ví dụ: một nhà phát triển từ bộ phận Robotics của Fabrikam Ấn Độ hoặc một nhà phát triển từ bộ phận Phần mềm của Fabrikam Hoa Kỳ. | Đơn vị cung cấp nguồn lực trên giá trị ước tính sắp đến hoặc thực tế sẽ được đối chiếu với mô tả này để đặt mặc định chi phí của vai trò. |
| Giá | Tab **Tổng quát** và trang **Tạo nhanh** | Thiết lập tỷ lệ chi phí cho tổ hợp vai trò, công ty cung cấp nguồn lực và đơn vị cung cấp nguồn lực. Ví dụ: một nhà phát triển từ Fabrikam Ấn Độ có chi phí 1000 INR hoặc một nhà phát triển từ Fabrikam Hoa Kỳ có chi phí 150 USD. | Giá là tỷ lệ chi phí mặc định trên chi phí trên đơn vị hoặc chi phí của ước tính đến hoặc mô tả thực tế cho loại giao dịch **Thời gian**. |
| Tiền tệ | Tab **Tổng quát** và trang **Tạo nhanh** | Theo mặc định, giá trị đơn vị tiền tệ đến từ đơn vị tiền tệ trên tiêu đề của bảng giá vốn nhưng có thể bị ghi đè. Ví dụ: một nhà phát triển từ Fabrikam Ấn Độ có chi phí 1000 INR. Một nhà phát triển từ Fabrikam Hoa Kỳ có chi phí 150 USD. | Đơn vị tiền tệ này mặc định theo chi phí trên đơn vị của đường đẳng phí đến cho loại giao dịch **Thời gian**. Trên ước tính dự án, giá trị tiền tệ được chuyển đổi sang đơn vị tiền tệ của dự án và được hiển thị trên chế độ xem theo thời gian của giá trị ước tính. |
| Lịch trình Đơn vị | Tab **Tổng quát** và trang **Tạo nhanh** | Lịch trình đơn vị này mặc định là Thời gian và không thể thay đổi trên thực thể Giá theo vai trò vì nó được sử dụng để biểu thị giá theo đơn vị thời gian. | Không có ảnh hưởng xuôi tuyến. |
| Đơn vị | Tab **Tổng quát** và trang **Tạo nhanh** | Theo mặc định, giá trị đến từ trường **Đơn vị thời gian** trên tiêu đề của bảng giá vốn. Có thể ghi đè giá trị này. Ví dụ: một nhà phát triển từ Fabrikam Ấn Độ có chi phí 1000 INR trên mỗi **Ngày Ấn Độ**. Một nhà phát triển từ Fabrikam Hoa Kỳ có chi phí 150 USD cho mỗi **Ngày Hoa Kỳ**. | Hệ thống sẽ sử dụng hệ thống đơn vị và chuyển đổi theo đơn vị cơ sở để tính toán chi phí trên đơn vị để tính toán đơn giá mặc định trên mô tả giá trị thực tế hoặc ước tính đến. Ví dụ: giá trị ước tính cho 10 **Ngày Ấn Độ** giá trị công việc của một nhà phát triển đến từ Ấn Độ và đơn vị **Ngày Ấn Độ** được định nghĩa là 10 giờ. Khi tính chi phí mô tả ước tính đó, ứng dụng sẽ tính toán đơn giá trên ước tính là: 1000 INR/10 giờ = 100 INR mỗi giờ, được chuyển đổi thành USD và được hiển thị dưới dạng đơn giá trên trang **Ước tính dự án**. |

## <a name="transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity"></a>Chuyển giá và chi phí cho các nguồn lực bên ngoài bộ phận hoặc pháp nhân của bạn

Các công ty dựa trên dự án thường sử dụng nhân viên từ các pháp nhân hoặc bộ phận khác nhau trên dự án. Một dự án có thể được thực hiện bởi một pháp nhân, nhưng nhân viên hoặc chuyên gia tư vấn làm việc trong dự án có thể đến từ cùng một pháp nhân hoặc từ một pháp nhân khác hoặc có thể kết hợp cả hai. Trong Dynamics 365 Project Operations, pháp nhân sở hữu việc bàn giao dự án được gọi là **Sở hữu công ty** và bộ phận sở hữu việc phân phối được gọi là **Đơn vị hợp đồng**. Các pháp nhân khác cung cấp nguồn lực được gọi là **Công ty cung cấp nguồn lực** và các bộ phận cung cấp nguồn lực được gọi là **Đơn vị cung cấp nguồn lực**. Ở hầu hết các quốc gia, các công ty phải đảm bảo rằng pháp nhân hoặc bộ phận cung cấp nguồn lực, tính phí cho công ty sở hữu và đơn vị ký hợp đồng sử dụng các nguồn lực.

Ví dụ: tập đoàn Fabrikam phải đảm bảo rằng Fabrikam India-Robotics có một thẻ tỷ lệ chi phí thương lượng với Fabrikam US-Robotics hoặc Fabrikam UK-Robotics.

Một nhà phát triển từ Fabrikam India-Robotic tính phí 100 USD khi cho Fabrikam US-Robotics mượn và 150 USD khi cho Fabrikam U-Robotics mượn.

### <a name="set-up-costs-for-outside-resources"></a>Thiết lập chi phí cho các nguồn lực bên ngoài

1. Tạo một bảng giá vốn được gọi là *tỷ lệ chi phí Fabrikam US-Robotics* và đặt phạm vi ngày có hiệu lực.
2. Trong bảng giá vốn, hãy thiết lập tỷ giá bằng cách sử dụng thông tin từ bảng sau. 

| Vai trò | Công ty cung cấp nguồn lực | Đơn vị Nguồn lực | Tỷ lệ chi phí |
| --- | --- | --- | --- |
| Nhà phát triển | Fabrikam Ấn Độ | Fabrikam India-Robotics | $100 |
| Nhà phát triển | Fabrikam Philippines | Fabrikam Philippines-Robotics | 90 USD |
| Nhà phát triển | Fabrikam Hoa Kỳ | Fabrikam US-Robotics | 150 USD |

3. Đính kèm bảng giá vốn này cho đơn vị tổ chức Fabrikam US-Robotics.

### <a name="set-up-transfer-pricing-for-a-resource-in-the-appropriate-currency"></a>Thiết lập giá chuyển nhượng cho một nguồn lực bằng đơn vị tiền tệ thích hợp 

Trong Project Operations, định giá nguồn lực có thể được thiết lập bằng bất kỳ đơn vị tiền tệ nào. Đơn vị tiền tệ được mặc định theo giá trị trên tiêu đề bảng giá, nhưng có thể thay đổi.

Sử dụng ví dụ về thiết lập giá chuyển nhượng, thông tin có thể được thay đổi thành:

Tập đoàn Fabrikam phải đảm bảo rằng Fabrikam India-Robotics có tỷ lệ chi phí thương lượng với Fabrikam US-Robotics hoặc Fabrikam UK-Robotics.

Một nhà phát triển từ Fabrikam India-Robotics tính phí 5000 INR khi cho Fabrikam US-Robotics mượn và 5500 INR khi cho Fabrikam UK-Robotics mượn.

Trong bảng giá vốn cho Fabrikam US-Robotics, tỷ lệ chi phí có thể được biểu thị như sau:

| Vai trò | Công ty cung cấp nguồn lực | Chi phí |
| --- | --- | --- |
| Nhà phát triển | Fabrikam Ấn Độ | 5000 INR |
| Nhà phát triển | Fabrikam Hoa Kỳ | 115 USD |

Trong bảng giá vốn cho Fabrikam UK-Robotics, tỷ lệ chi phí có thể được biểu thị như sau:

| Vai trò | Công ty cung cấp nguồn lực | Chi phí |
| --- | --- | --- |
| Nhà phát triển | Fabrikam Ấn Độ | 5500 INR |
| Nhà phát triển | Fabrikam Vương quốc Anh | 115 GBP |

Bảng giá vốn có thể cung cấp tỷ giá nhân công bằng nhiều đơn vị tiền tệ. Khi tạo ước tính chi phí cho dự án, Project Operations sẽ chuyển đổi các tỷ lệ chi phí này thành đơn vị tiền tệ của dự án và hiển thị cho người dùng. Khi mục nhập thời gian được chấp thuận và chi phí thực tế được tạo, chi phí thực tế được định giá bằng đơn vị tiền tệ của mô tả giá theo vai trò phù hợp trên bảng giá vốn. Chi phí thực tế cho thời gian cho một dự án có thể được ghi lại bằng nhiều đơn vị tiền tệ. Tuy nhiên, khi tính tổng hoặc tổng hợp chi phí lao động thực tế ở cấp độ dự án, Project Operations sẽ chuyển đổi tất cả các khoản chi phí lao động sang đơn vị tiền tệ của dự án mà người dùng có thể xem.
