---
title: Dự toán tài chính về thời gian nguồn lực cho dự án
description: Bài viết này cung cấp thông tin về cách tính các ước tính tài chính cho thời gian.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 03416feb178d883bba57dc14692049503b151ffd
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913554"
---
# <a name="financial-estimates-for-resource-time-on-projects"></a>Dự toán tài chính về thời gian nguồn lực cho dự án

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Dự toán tài chính cho thời gian được tính toán dựa trên ba yếu tố: 

- Loại thành viên nhóm chung hoặc riêng được chỉ định cho mỗi nhiệm vụ nút lá trên kế hoạch dự án. 
- Loại hoặc mức độ phức tạp của công việc.
- Sự phân chia công số cho công việc giao cho nguồn lực trên nhiệm vụ. 

Hai yếu tố đầu tiên ảnh hưởng đến chi phí đơn vị hoặc mức lương theo giờ của công việc giao cho nguồn lực. Chi phí đơn vị hoặc mức lương theo giờ của công việc giao cho nguồn lực được xác định theo các thuộc tính của nguồn lực được giao. Các thuộc tính này bao gồm đơn vị tổ chức của nguồn lực và vai trò tiêu chuẩn của nguồn lực. Bạn cũng có thể thêm các thuộc tính tùy chỉnh có liên quan đến doanh nghiệp của mình cho nguồn lực, như chức danh tiêu chuẩn hoặc mức độ kinh nghiệm và để chúng ảnh hưởng đến chi phí đơn vị hoặc mức lương theo giờ cho công việc được giao.
Ngoài các thuộc tính của nguồn lực, các thuộc tính của công việc, chẳng hạn như nhiệm vụ, cũng có thể ảnh hưởng đến mức lương theo giờ của đơn vị hoặc tỷ lệ chi phí của công việc được giao. Ví dụ: khi một số nhiệm vụ phức tạp hơn, công việc giao cho nguồn lực theo các nhiệm vụ cụ thể đó dẫn đến chi phí đơn vị hoặc mức lương theo giờ cao hơn so với các nhiệm vụ ít phức tạp hơn.   

Yếu tố thứ ba cung cấp số giờ ở mức lương đó. Trong trường hợp một nhiệm vụ bao gồm hai giai đoạn giá, có khả năng phần đầu tiên của công việc giao cho nguồn lực của nhiệm vụ đó được tính phí và định giá khác với phần thứ hai của nhiệm vụ. Ước tính công số cho mỗi công việc giao cho nguồn lực là một giá trị phức tạp được lưu trữ cùng với sự phân bổ công số mỗi ngày.

Để biết hướng dẫn chi tiết về cách thiết lập các thuộc tính tùy chỉnh của công việc và nguồn lực dưới dạng thứ nguyên giá và chi phí, hãy xem [Tổng quan về Thứ nguyên giá](../pricing-costing/pricing-dimensions-overview.md).

Dự toán tài chính cho mỗi công việc giao cho nguồn lực được tính theo công thức **mức lương/giờ của công việc được giao nhân với số giờ.**  Tương tự như ước tính công số, dự toán tài chính cho chi phí và doanh thu của mỗi công việc giao cho nguồn lực là một giá trị phức tạp được lưu trữ cùng với sự phân bổ số tiền mỗi ngày. 

## <a name="summarizing-financial-estimates-for-time"></a>Tổng hợp dự toán tài chính cho thời gian
Dự toán tài chính cho thời gian thực hiện nhiệm vụ nút lá là tổng các dự toán tài chính cho tất cả các công việc giao cho nguồn lực của nhiệm vụ đó.

Dự toán tài chính cho thời gian thực hiện nhiệm vụ mẹ hoặc nhiệm vụ tóm tắt là tổng các dự toán tài chính cho tất cả các nhiệm vụ con. Đây là chi phí nhân công ước tính cho dự án. 

![Ước tính nguồn lực.](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Loại tiền tệ chi phí và giá vốn mặc định

Giá vốn mặc định lấy từ các bảng giá đi kèm đơn vị thầu của dự án. Đơn vị tiền tệ chi phí của dự án luôn là đơn vị tiền tệ của đơn vị thầu của dự án. Trên công việc giao cho nguồn lực, dự toán tài chính cho chi phí được lưu trữ theo đơn vị tiền tệ chi phí của dự án. Đôi khi, đơn vị tiền tệ mà tỷ lệ chi phí được thiết lập trong bảng giá khác với đơn vị tiền tệ chi phí của dự án. Trong những trường hợp này, ứng dụng chuyển đổi đơn vị tiền tệ mà giá vốn được thiết lập thành đơn vị tiền tệ của dự án. Trên lưới **Ước tính**, tất cả các ước tính chi phí được hiển thị và tóm tắt bằng đơn vị tiền tệ chi phí của dự án. 

## <a name="default-bill-rate-and-sales-currency"></a>Loại tiền tệ bán hàng và tỷ lệ thanh toán mặc định

Giá bán mặc định được lấy từ bảng giá dự án đi kèm hợp đồng dự án có liên quan nếu đạt được thỏa thuận, hoặc từ báo giá dự án có liên quan nếu thỏa thuận vẫn đang trong giai đoạn tiền bán hàng. Đơn vị tiền tệ doanh số của dự án luôn là đơn vị tiền tệ của báo giá dự án hoặc hợp đồng dự án. Trên công việc giao cho nguồn lực, dự toán tài chính cho doanh thu được lưu trữ theo đơn vị tiền tệ doanh thu của dự án. Không giống như chi phí, giá bán được thiết lập trong bảng giá không bao giờ được khác với đơn vị tiền tệ doanh số của dự án. Không có trường hợp nào cần chuyển đổi đơn vị tiền tệ. Trên lưới **Ước tính**, tất cả các ước tính doanh thu được hiển thị và tóm tắt bằng đơn vị tiền tệ doanh thu của dự án. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
