---
title: Theo dõi chi phí dự án
description: Chủ đề này cung cấp thông tin về cách Project Operations theo dõi tiến độ dựa trên chi phí nhân công và mức chi tiêu cho một dự án.
author: rumant
manager: AnnBe
ms.date: 03/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 28cb692c61ae4137a28973dc1bd70ffd989dd535
ms.sourcegitcommit: a1f9f92546ab5d8d8e5a4710ce4c96414ea55d14
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 03/24/2021
ms.locfileid: "5711100"
---
# <a name="labor-cost-tracking-on-projects"></a>Theo dõi chi phí nhân công của dự án

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Dynamics 365 Project Operations theo dõi chi phí nhân công ước tính và mức chi tiêu một cách ít chi tiết nhất theo yêu cầu trong kế hoạch dự án. Ước tính tài chính về chi phí nhân công dựa trên công số dự kiến và các nguồn lực chung hoặc riêng được giao cho từng nhiệm vụ nút lá trong kế hoạch dự án. Khi dự án bắt đầu và mọi người bắt đầu báo cáo thời gian cho các nhiệm vụ khác nhau của dự án, mức chi tiêu thực tế cho nhân công sẽ được tóm tắt để bắt đầu các dự toán.

## <a name="labor-cost-tracking-view"></a>Dạng xem Theo dõi chi phí nhân công

Trên trang **Dự án**, trên tab **Theo dõi**, bạn có thể chọn **Theo dõi** > **Chi phí** để mở dạng xem **Theo dõi chi phí** và xem tiến độ chi tiêu cho nhân công của từng nhiệm vụ trong kế hoạch dự án. Dạng xem này cũng so sánh chi phí nhân công thực tế chi cho một nhiệm vụ với chi phí nhân công dự kiến của nhiệm vụ đó. Project Operations sử dụng các công thức sau để tính toán chỉ số chi phí nhân công:

- **Chi phí dự kiến**: Chi phí ước tính của tất cả các nhiệm vụ giao cho nguồn lực trên mỗi nhiệm vụ nút lá
- **Chi phí thực tế**: Tổng của tất cả các chi phí thực tế cho thời gian được ghi lại trên nhiệm vụ
- **Phần trăm sử dụng chi phí**: Chi phí thực tế ÷ Chi phí ước tính lúc hoàn thành
- **Chi phí còn lại**: Chi phí ước tính lúc hoàn thành – Chi phí thực tế
- **Chi phí lúc hoàn thành**: Chi phí còn lại + Chi phí thực tế
- **Chênh lệch chi phí**: Chi phí dự kiến – Chi phí ước tính lúc hoàn thành

Mỗi nhiệm vụ hiển thị một dự toán về mức chênh lệch chi phí của nhiệm vụ đó. Nếu chi phí ước tính lúc hoàn thành cao hơn chi phí dự kiến, thì nhiệm vụ theo dự toán là sẽ vượt quá ngân sách. Nếu chi phí ước tính lúc hoàn thành thấp hơn chi phí dự kiến, thì nhiệm vụ theo dự toán là không dùng hết ngân sách.

>[!NOTE]
> Project Operations chỉ hiển thị chi phí nhân công trên trang **Dự án**, trong tab **Theo dõi**. Trong khi vật tư và chi phí có thể được ước tính và theo dõi để biết mức sử dụng, những chi phí này không được đưa vào chi phí hiển thị trên tab **Theo dõi**. Tab này được thiết kế để chỉ hoạt động khi dự toán lại chi phí nhân công bằng cách dự toán lại công số.
Tất cả các khoản chi phí hiển thị được chuyển đổi sang đơn vị tiền tệ chi phí của dự án từ đơn vị tiền tệ giá vốn của dự án được sử dụng để xác định tỷ lệ chi phí. Đơn vị tiền tệ chi phí của dự án là đơn vị tiền tệ của đơn vị hợp đồng trong dự án. Giá trị chi phí ước tính cho thời gian được hiển thị trong tab **Ước tính** trên trang **Dự án** có thể không tính đến chi phí dự kiến trong tab **Theo dõi**. Lý do cho sự chênh lệch này là do sự khác biệt trong cách tổng hợp chi phí ước tính trên lưới **Ước tính** và cách tính chi phí dự kiến trên lưới **Theo dõi**. 
>
> - **Tab ước tính** tính toán chi phí ước tính bằng cách sử dụng cùng một đơn vị tiền tệ của tỷ lệ chi phí trong bảng giá. Sau đó, chi phí ước tính bằng đơn vị tiền tệ trong bảng giá được chuyển đổi thành chi phí ước tính bằng đơn vị tiền tệ chi phí của dự án. Chi phí ước tính bằng đơn vị tiền tệ của dự án được làm tròn đến 2 chữ số thập phân. Không có điểm nào trong quá trình chuyển đổi này được áp dụng độ chính xác của đơn vị tiền tệ. 
> - Trên tab **Theo dõi**, việc tính toán chi phí dự kiến tuân theo một trình tự tính toán hơi khác liên quan đến độ chính xác của đơn vị tiền tệ được áp dụng trong hai giai đoạn: 
   ><ol>
   ><li>Số tiền chi phí ước tính bằng đơn vị tiền tệ trong bảng giá được chuyển đổi sang đơn vị tiền tệ cơ sở (chuyển đổi 1).</li>
   ><li>Số tiền chi phí ước tính bằng đơn vị tiền tệ cơ sở được chuyển đổi sang đơn vị tiền tệ chi phí của dự án (chuyển đổi 2). </li>
   ></ol>
   >Độ chính xác của đơn vị tiền tệ được áp dụng trong cả hai bước để có được chi phí dự kiến (trên tab **Theo dõi**) chênh lệch một chút so với chi phí ước tính (trên dạng xem **Thời gian - theo giai đoạn** trên tab **Ước tính**). 
   
## <a name="reprojecting-costs-on-leaf-node-tasks"></a>Dự toán lại chi phí cho các nhiệm vụ nút lá

Không thể dự toán lại trực tiếp chi phí nhân công cho một nhiệm vụ nút lá trên tab **Theo dõi** trên **Trang dự án**. Tuy nhiên, bạn có thể sử dụng dạng xem **Theo dõi công số** để dự toán lại công số còn lại cho một nhiệm vụ. Điều này dẫn đến phải tính toán lại chi phí còn lại cho nhiệm vụ. Sau đây là phần mô tả về cách hoạt động của quy trình này.

1. Người quản lý dự án có thể dự toán lại công số cho nhiệm vụ bằng cách cập nhật giá trị mặc định trong trường **Công số còn lại** với một giá trị ước tính mới về công số còn lại cho nhiệm vụ. Việc dự toán lại sẽ dẫn đến tính toán lại công số ước tính lúc hoàn thành (EAC) của nhiệm vụ, tỷ lệ phần trăm tiến độ và mức chênh lệch công số đã dự toán trên một nhiệm vụ. EAC, ước tính đến lúc hoàn thành (ETC) và phần trăm tiến trình trên các nhiệm vụ tóm tắt cũng được tính toán lại và đưa ra dự toán mới về mức chênh lệch công số.
2. Dựa trên giá trị mới của công số còn lại cho nhiệm vụ, hệ thống sẽ tính toán chi phí còn lại trên dạng xem **Theo dõi chi phí**. Để tính toán chi phí còn lại dựa trên công số còn lại, trước tiên, hệ thống sẽ tính chi phí trung bình của một giờ công cho nhiệm vụ dưới dạng chi phí dự kiến hoặc công số dự kiến. Chi phí dự kiến là tổng chi phí của tất cả các công việc giao cho nguồn lực trên nhiệm vụ. Chi phí trung bình mỗi giờ được dùng để tính toán chi phí còn lại của công số còn lại mới dự toán cho nhiệm vụ.
3. Chi phí lúc hoàn thành và tỷ lệ phần trăm sử dụng chi phí trên nhiệm vụ nút lá được tính toán lại.
4. Giá trị chi phí lúc hoàn thành của mọi nhiệm vụ tóm tắt đến nút gốc được tính toán lại.

## <a name="reprojecting-costs-on-summary-tasks"></a>Dự toán lại chi phí cho các nhiệm vụ tóm tắt

Bạn có thể dự đoán lại chi phí nhân công cho các nhiệm vụ tóm tắt hoặc các nhiệm vụ vùng chứa. Tuy nhiên, bạn không thể dự toán lại trực tiếp chi phí nhân công cho một nhiệm vụ trên tab **Theo dõi** trên trang **Dự án**. Tương tự như các nhiệm vụ nút lá, bạn có thể dự toán lại các nhiệm vụ tóm tắt và vùng chứa bằng cách sử dụng dạng xem **Theo dõi công số**. Trong dạng xem này, bạn có thể dự toán lại công số còn lại cho một nhiệm vụ tóm tắt dẫn đến phải tính toán lại chi phí còn lại cho nhiệm vụ tóm tắt đó. Sau đây là phần mô tả về cách hoạt động của quy trình này.

1. Người quản lý dự án có thể dự toán lại công số cho nhiệm vụ tóm tắt bằng cách cập nhật giá trị mặc định của công số còn lại bằng một giá trị ước tính mới cho nhiệm vụ. Việc cập nhật này sẽ dẫn đến tính toán lại giá trị ước tính lúc hoàn thành (EAC) của nhiệm vụ tóm tắt, tỷ lệ phần trăm tiến độ và mức chênh lệch công số đã dự toán trên một nhiệm vụ. EAC, ETC và phần trăm tiến trình trên các nhiệm vụ tóm tắt cũng được tính toán lại và cung cấp dự kiến mới về chênh lệch nhân công.
2. Dựa trên giá trị mới của công số còn lại cho nhiệm vụ tóm  tắt, hệ thống sẽ tính toán chi phí còn lại trên dạng xem **Theo dõi chi phí**. Để tính toán chi phí còn lại dựa trên công số còn lại, trước tiên, hệ thống sẽ tính chi phí trung bình của một giờ công cho nhiệm vụ tóm tắt dưới dạng chi phí dự kiến hoặc công số dự kiến. Chi phí trung bình mỗi giờ được dùng để tính toán chi phí còn lại của công số còn lại mới dự toán cho nhiệm vụ tóm tắt.
3. Chi phí lúc hoàn thành và tỷ lệ phần trăm sử dụng chi phí trên nhiệm vụ tóm tắt được tính toán lại.
4. Giá trị mới của chi phí lúc hoàn thành được phân phối xuống các nhiệm vụ con theo cùng một tỷ lệ như chi phí dự kiến gốc trên nhiệm vụ.
5. Giá trị mới của chi phí lúc hoàn thành trên từng nhiệm vụ được phân phối xuống các nhiệm vụ nút lá sẽ được tính toán. Dựa trên giá trị này, các nhiệm vụ con bị ảnh hưởng được phân phối xuống các nút lá sẽ được tính toán lại tỷ lệ phần trăm sử dụng chi phí và chi phí còn lại của chúng dựa trên giá trị chi phí lúc hoàn thành. Giá trị này dẫn đến dự toán mới cho mức chênh lệch chi phí của nhiệm vụ. 


Bạn có thể đặt trường **Hiệu suất chi phí** từ dữ liệu theo dõi. Khi mức chênh lệch chi phí của nút gốc trong dạng xem **Theo dõi chi phí** là âm, bạn có thể đặt trường này thành **Dưới ngân sách**. Khi mức chênh lệch chi phí của nút gốc là dương, bạn có thể đặt giá trị này thành **Vượt quá ngân sách**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
