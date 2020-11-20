---
title: Quản lý trạng thái không được vượt quá và các mục xác thực
description: Chủ đề này cung cấp thông tin về các hoạt động kiểm tra giới hạn không vượt quá được thực hiện trong Project Operations.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 09dea414e91a365f33bd23089c427b5f63f55c8e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130019"
---
# <a name="manage-not-to-exceed-status-and-validations"></a>Quản lý trạng thái không được vượt quá và các mục xác thực 

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

## <a name="not-to-exceed-on-approvals"></a>Không vượt quá khi phê duyệt

Khi một mục nhập thời gian hoặc chi phí được gửi, một hồ sơ phê duyệt sẽ được tạo. Nếu hồ sơ phê duyệt đó là phải thanh toán và ánh xạ đến một mô tả hợp đồng thời gian và vật tư, hệ thống sẽ hoàn thành quy trình kiểm tra xác thực không vượt quá ở các cấp độ sau:

  - Kiểm tra dựa trên giới hạn được thiết lập cho khách hàng trên mô tả hợp đồng dự án
  - Kiểm tra dựa trên giới hạn được thiết lập trên mô tả hợp đồng
  - Kiểm tra dựa trên giới hạn được thiết lập cho khách hàng
  - Kiểm tra dựa trên giới hạn được thiết lập trên hợp đồng

Quy trình kiểm tra ở mỗi cấp là để đảm bảo rằng giá trị doanh số trong lần phê duyệt này sẽ không cao hơn giới hạn không vượt quá ở cấp đó sau khi làm rõ số tiền trong mục tồn đọng thanh toán đã được ghi lại và số tiền được lập hóa đơn cho đến nay ở cấp đó.

Nếu vượt qua bước kiểm tra, bước phê duyệt sẽ có trạng thái xác thực là **Thành công**.

Nếu không vượt qua bước kiểm tra, bước phê duyệt sẽ có trạng thái xác thực là **Không thành công**. Thông tin chi tiết về quy trình xác thực không vượt quá sẽ cho người dùng biết bước xác thực không thành công ở cấp nào.

Khi mục nhập thời gian hoặc chi phí đã gửi được coi là không phải thanh toán, trạng thái xác thực không vượt quá được đặt thành **Không áp dụng** với thông tin chi tiết xác thực tương đương với **Không áp dụng**.

## <a name="not-to-exceed-on-unbilled-sales-actuals"></a>Giới hạn không vượt quá đối với doanh số thực tế chưa được thanh toán

Khi một mục nhập thời gian hoặc chi phí được phê duyệt, các bản ghi doanh số thực tế chưa được thanh toán và chi phí sẽ được tạo. Nếu doanh số thực tế chưa được thanh toán đang được tạo thuộc trường hợp phải thanh toán và ánh xạ đến một mô tả hợp đồng thời gian và vật tư, thì ứng dụng sẽ tiến hành bước kiểm tra xác thực không vượt quá ở các cấp độ sau:

  - Kiểm tra dựa trên giới hạn được thiết lập cho khách hàng trên mô tả hợp đồng dự án
  - Kiểm tra dựa trên giới hạn được thiết lập trên mô tả hợp đồng
  - Kiểm tra dựa trên giới hạn được thiết lập cho khách hàng
  - Kiểm tra dựa trên giới hạn được thiết lập trên hợp đồng

Quy trình kiểm tra ở mỗi cấp sẽ đảm bảo rằng giá trị doanh số trên thực tế sẽ không cao hơn giới hạn không vượt quá ở cấp đó sau khi làm rõ số tiền trong mục tồn đọng thanh toán đã được ghi lại và số tiền được lập hóa đơn cho đến nay ở cấp đó.

Nếu vượt qua bước kiểm tra, doanh số thực tế chưa được thanh toán sẽ có trạng thái không vượt quá là **Đã cam kết**.

Nếu không vượt qua bước kiểm tra, doanh số thực tế chưa được thanh toán sẽ có trạng thái không vượt quá là **Không thành công**. Thông tin xác thực chi tiết sẽ cho người dùng biết bước xác thực không thành công ở cấp nào.

Khi doanh số thực tế chưa được thanh toán được coi là phải thanh toán hoặc miễn, nếu không có giới hạn không vượt quá nào được thiết lập ở bất kỳ cấp độ nào trong số bốn cấp độ hoặc nếu giá trị thực tế được tạo là Chi phí, Tiền tạm ứng, Đơn vị nguồn lực hoặc Doanh số liên tổ chức, thì các trường **Trạng thái không vượt quá** và **Chi tiết xác thực không vượt quá** phải được đặt thành **Không áp dụng**.

## <a name="reset-the-not-to-exceed-status"></a>Đặt lại trạng thái không vượt quá

Bạn có thể thực hiện đặt lại hàng loạt trạng thái không vượt quá. Điều này cho phép Người quản lý dự án điều chỉnh việc xác thực không vượt quá để ưu tiên lập hóa đơn cho một phần công việc, thời gian hoặc chi phí cụ thể hơn những phần khác đã được cam kết từ số tiền không vượt quá hiện có.

Sau khi trạng thái không vượt quá được đặt lại cho doanh số thực tế chưa được thanh toán, số tiền đã cam kết sẽ giảm xuống. Người quản lý dự án có thể chọn một phần công việc, thời gian hoặc chi phí khác mà trước đó đã không thế tiến hành xác thực không vượt quá và đánh giá lại chúng. Với việc giảm số tiền đã cam kết, những giá trị thực tế này sẽ vượt qua quy trình xác thực. Điều này giúp Người quản lý dự án có khả năng tác động và kiểm soát tốt hơn đối với các giao dịch có thể lập hóa đơn cho giai đoạn đó.

Để đặt lại trạng thái không vượt quá, hãy chọn một hoặc nhiều giá trị thực tế từ dạng xem **Tồn đọng thanh toán cho thời gian và vật tư** hoặc **Giá trị thực tế**, sau đó chọn **Đặt lại trạng thái không vượt quá**.

Trạng thái không vượt quá được đặt lại thành **Chưa đánh giá** trên tất cả các giá trị thực tế phù hợp được chọn. Các giá trị thực tế được đặt lại trạng thái không vượt quá là các doanh số thực tế chưa được thanh toán. Các giá trị này chưa được lập hóa đơn, không có trên hóa đơn nháp và được đánh dấu là phải thanh toán. Mọi giá trị thực tế đã chọn khác đều bị bỏ qua.

## <a name="reevaluate-not-to-exceed-status"></a>Đánh giá lại trạng thái không vượt quá

Bạn có thể thực hiện đánh giá lại hàng loạt trạng thái không vượt quá. Việc đánh giá lại trạng thái không vượt quá là hữu ích khi:

  - Đã có một cuộc thương lượng lại về giới hạn không vượt quá với khách hàng và các giá trị thực tế sẽ cần được đánh giá lại.
  - Người quản lý dự án muốn điều chỉnh việc lập hóa đơn cho các doanh số tồn đọng chưa được thanh toán bằng cách ưu tiên một phần công việc hơn phần khác.

Để đặt lại trạng thái không vượt quá, hãy chọn một hoặc nhiều giá trị thực tế từ dạng xem **Tồn đọng thanh toán cho thời gian và vật tư** hoặc **Giá trị thực tế**, sau đó chọn **Đánh giá lại trạng thái không vượt quá**.

Tất cả giá trị thực tế phù hợp được chọn với giới hạn không vượt quá sẽ được đánh giá dựa trên sự thiết lập giới hạn không vượt quá. Các giá trị thực tế phù hợp để đánh giá lại trạng thái không vượt quá là các doanh số thực tế chưa được thanh toán. Các giá trị này chưa được lập hóa đơn, không có trên hóa đơn nháp và được đánh dấu là phải thanh toán. Bất kỳ giá trị thực tế nào khác được chọn.
