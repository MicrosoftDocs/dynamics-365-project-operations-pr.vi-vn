---
title: Theo dõi doanh số dự án
description: Chủ đề này cung cấp thông tin về cách Project Operations theo dõi tiến độ dựa trên doanh thu nhân công của một dự án.
author: rumant
ms.date: 03/24/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 78d7bdaf9f5ca1757273cb81a1303befb0357ba547eb354097786fc3c38962b9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995607"
---
# <a name="project-sales-tracking"></a>Theo dõi doanh số dự án

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Dynamics 365 Project Operations theo dõi chi phí nhân công ước tính và doanh thu một cách ít chi tiết nhất theo yêu cầu trong kế hoạch dự án. Ước tính doanh thu nhân công dựa trên công số dự kiến và các nguồn lực chung hoặc riêng được giao cho từng nhiệm vụ nút lá trong kế hoạch dự án. Khi dự án bắt đầu và mọi người bắt đầu báo cáo thời gian cho các nhiệm vụ khác nhau của dự án, doanh thu thực tế cho nhân công sẽ được tóm tắt để bắt đầu các dự toán.

## <a name="labor-revenue-tracking-view"></a>Dạng xem Theo dõi doanh thu nhân công

Trên trang **Dự án**, trong tab **Theo dõi**, bạn có thể chọn **Theo dõi** > **Chi phí** để mở dạng xem **Theo dõi chi phí**. Hoặc, bạn có thể chọn **Sử dụng** > **Mức giá theo giờ** để mở dạng xem **Theo dõi doanh thu**. Dạng xem này hiển thị tiến độ của doanh thu nhân công trên từng nhiệm vụ trong kế hoạch dự án. Dạng xem này cũng so sánh doanh thu nhân công thực tế chi cho một nhiệm vụ với doanh thu nhân công dự kiến của nhiệm vụ đó. Project Operations sử dụng các công thức sau để tính toán chỉ số doanh thu nhân công:

- **Doanh thu dự kiến**: Giá trị doanh số ước tính của tất cả các công việc giao cho nguồn lực trên mỗi nhiệm vụ nút lá
- **Doanh thu thực tế**: Tổng của tất cả các doanh thu thực tế chưa lập hóa đơn cho thời gian được ghi lại trên nhiệm vụ
- **% doanh thu có thể lập hóa đơn**: Doanh thu thực tế ÷ Doanh thu ước tính lúc hoàn thành
- **Doanh thu còn lại**: Doanh thu ước tính lúc hoàn thành – Doanh thu thực tế
- **Doanh thu ước tính lúc hoàn thành**: Doanh thu còn lại + Doanh thu thực tế
- **Chênh lệch doanh thu**: Doanh thu dự kiến – Doanh thu ước tính lúc hoàn thành


> [!NOTE]
> Project Operations chỉ hiển thị doanh thu nhân công trên trang **Dự án**, trong tab **Theo dõi**. Mặc dù vật tư và chi phí có thể được ước tính và theo dõi để biết mức sử dụng, nhưng những doanh thu này không được đưa vào chi phí hiển thị trên tab **Theo dõi**. Tab này được thiết kế để chỉ hoạt động khi dự toán lại doanh thu nhân công bằng cách dự toán lại công số.  
> Tất cả số tiền doanh thu hiển thị được chuyển đổi sang đơn vị tiền tệ chi phí của dự án. Đơn vị tiền tệ chi phí của dự án là đơn vị tiền tệ của đơn vị hợp đồng trong dự án. Đối với dự án giá cố định, các số liệu doanh thu trên dạng xem **Theo dõi doanh thu nhân công** không liên quan bởi vì doanh số thực tế chưa lập hóa đơn không được ghi lại khi phê duyệt thời gian.
> Giá trị doanh số ước tính cho thời gian được hiển thị trên tab **Ước tính** của dự án có thể không tính vào giá trị doanh thu dự kiến trên tab **Theo dõi**. Có hai nguyên nhân gây ra sự chênh lệch này:
><ol>
   ><li> Tab <b>Ước tính</b> hiển thị doanh thu ước tính bằng đơn vị tiền tệ bán hàng, trong khi tab <b>Theo dõi</b> hiển thị doanh thu dự kiến được chuyển đổi sang đơn vị tiền tệ chi phí. </li>
   ><li> Khi doanh số ước tính được chuyển đổi sang đơn vị tiền tệ của hợp đồng như hiển thị trên tab <b>Ước tính</b>, sang đơn vị tiền tệ của dự án, việc chuyển đổi này bao gồm các bước có thể làm mất độ chính xác: </li>
><ol>
><li> Số tiền doanh số ước tính bằng đơn vị tiền tệ trong hợp đồng được chuyển đổi trước tiên sang đơn vị tiền tệ cơ sở (chuyển đổi 1).</li>
><li> Số tiền doanh số ước tính bằng đơn vị tiền tệ cơ sở được chuyển đổi sang đơn vị tiền tệ chi phí của dự án (chuyển đổi 2). </li>
></ol>
></ol>
> Độ chính xác của đơn vị tiền tệ được áp dụng trong cả hai bước, dẫn đến sự chênh lệch giữa doanh thu dự kiến tính bằng đơn vị tiền tệ của dự án so với doanh số dự kiến tính theo đơn vị tiền tệ của hợp đồng.
   

## <a name="reprojecting-revenues-on-leaf-node-tasks"></a>Dự toán lại donah thu cho các nhiệm vụ nút lá

Không thể dự toán lại trực tiếp doanh thu nhân công cho một nhiệm vụ nút lá trên tab **Theo dõi** trên trang **Dự án**. Tuy nhiên, bạn có thể sử dụng dạng xem **Theo dõi công số** để dự toán lại công số còn lại cho một nhiệm vụ. Điều này dẫn đến phải tính toán lại doanh thu còn lại cho nhiệm vụ. Sau đây là phần mô tả về cách hoạt động của quy trình này.

1. Người quản lý dự án có thể dự toán lại công số cho nhiệm vụ bằng cách cập nhật giá trị mặc định trong trường **Công số còn lại** với một giá trị ước tính mới về công số còn lại cho nhiệm vụ. Việc dự toán lại sẽ dẫn đến tính toán lại công số ước tính lúc hoàn thành (EAC) của nhiệm vụ, tỷ lệ phần trăm tiến độ và mức chênh lệch công số đã dự toán trên một nhiệm vụ. EAC, ước tính đến lúc hoàn thành (ETC) và phần trăm tiến trình trên các nhiệm vụ tóm tắt cũng được tính toán lại và đưa ra dự toán mới về mức chênh lệch công số.
2. Dựa trên giá trị mới của công số còn lại cho nhiệm vụ, hệ thống sẽ tính toán doanh thu còn lại trên dạng xem **Theo dõi doanh thu**. Để tính toán doanh thu còn lại dựa trên công số còn lại, trước tiên, hệ thống sẽ tính doanh thu trung bình của một giờ công cho nhiệm vụ dưới dạng doanh thu dự kiến hoặc công số dự kiến. Doanh thu dự kiến là tổng doanh thu của tất cả các công việc giao cho nguồn lực trên nhiệm vụ. Doanh thu trung bình mỗi giờ được dùng để tính toán doanh thu còn lại của công số còn lại mới dự toán cho nhiệm vụ.
3. Doanh thu ước tính lúc hoàn thành và tỷ lệ phần trăm sử dụng doanh thu trên nhiệm vụ nút lá được tính toán lại.
4. Giá trị doanh thu lúc hoàn thành của mọi nhiệm vụ tóm tắt đến nút gốc được tính toán lại.

## <a name="reprojecting-revenues-on-summary-tasks"></a>Dự toán lại doanh thu cho các nhiệm vụ tóm tắt

Bạn có thể dự đoán lại doanh thu nhân công cho các nhiệm vụ tóm tắt hoặc các nhiệm vụ vùng chứa. Tuy nhiên, bạn không thể dự toán lại trực tiếp doanh thu nhân công cho một nhiệm vụ tóm tắt trong tab **Theo dõi** trên trang **Dự án**. Tương tự như các nhiệm vụ nút lá, bạn có thể dự toán lại các nhiệm vụ tóm tắt và vùng chứa bằng cách sử dụng dạng xem **Theo dõi công số**. Trong dạng xem này, bạn có thể dự toán lại công số còn lại cho một nhiệm vụ tóm tắt dẫn đến phải tính toán lại doanh thu còn lại cho nhiệm vụ tóm tắt đó. Sau đây là phần mô tả về cách hoạt động của quy trình này.

1. Người quản lý dự án có thể dự toán lại công số cho nhiệm vụ bằng cách cập nhật giá trị mặc định trong trường **Công số còn lại** với một giá trị ước tính mới về **Công số còn lại** cho nhiệm vụ. Việc dự toán lại sẽ dẫn đến tính toán lại giá trị ước tính lúc hoàn thành (EAC) của nhiệm vụ, tỷ lệ phần trăm tiến độ và mức chênh lệch công số đã dự toán trên một nhiệm vụ. EAC, ETC và phần trăm tiến trình trên các nhiệm vụ tóm tắt cũng được tính toán lại và cung cấp dự kiến mới về chênh lệch nhân công.
2. Dựa trên giá trị mới trong trường **Công số còn lại** cho nhiệm vụ, hệ thống sẽ tính toán doanh thu còn lại trong dạng xem **Theo dõi doanh thu**. Để tính toán doanh thu còn lại dựa trên công số còn lại, trước tiên, hệ thống sẽ tính doanh thu trung bình của một giờ công cho nhiệm vụ dưới dạng doanh thu dự kiến hoặc công số dự kiến. Doanh thu dự kiến là tổng doanh thu của tất cả các công việc giao cho nguồn lực trên nhiệm vụ. Sau đó, doanh thu trung bình mỗi giờ này được dùng để tính toán doanh thu của công số còn lại mới dự toán cho nhiệm vụ.
3. Doanh thu ước tính lúc hoàn thành và tỷ lệ phần trăm sử dụng doanh thu trên nhiệm vụ tóm tắt được tính toán lại.
4. Giá trị mới của doanh thu ước tính lúc hoàn thành được phân phối xuống các nhiệm vụ con theo cùng một tỷ lệ như doanh thu dự kiến gốc trên nhiệm vụ.
5. Giá trị mới của doanh thu ước tính lúc hoàn thành trên từng nhiệm vụ được phân phối xuống các nhiệm vụ nút lá sẽ được tính toán. Dựa trên giá trị này, các nhiệm vụ con bị ảnh hưởng được phân phối xuống các nút lá sẽ được tính toán lại tỷ lệ phần trăm sử dụng doanh thu và chi phí còn lại của chúng dựa trên giá trị doanh thu lúc hoàn thành. Điều này dẫn đến dự toán mới cho mức chênh lệch doanh thu của nhiệm vụ. 
6. Giá trị doanh thu lúc hoàn thành của mọi nhiệm vụ tóm tắt đến nút gốc được tính toán lại.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

