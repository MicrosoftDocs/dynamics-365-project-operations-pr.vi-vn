---
title: Theo dõi công số dự án
description: Bài viết này cung cấp thông tin về cách theo dõi công số dự án và tiến độ công việc.
author: ruhercul
ms.date: 02/15/2022
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: c41dbc138f6fc92a9586de173ba5dfc89c7e44e3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929286"
---
# <a name="project-effort-tracking"></a>Theo dõi công số dự án

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Sự cần thiết của việc theo dõi tiến độ đối với lịch trình thay đổi theo ngành. Một số ngành theo dõi ở cấp độ chi tiết, trong khi các ngành khác theo dõi ở cấp độ cao hơn. Bài viết này cho biết cách lập lịch để đáp ứng các yêu cầu của tổ chức bạn.

## <a name="effort-tracking-view"></a>Dạng xem theo dõi nhân công

Dạng xem **Theo dõi nhân công** theo dõi tiến độ của các nhiệm vụ trong lịch trình bằng cách so sánh số giờ nhân công thực tế dành cho một nhiệm vụ với số giờ nhân công theo kế hoạch của nhiệm vụ. Dynamics 365 Project Operations sử dụng các công thức sau để tính toán các chỉ số theo dõi:

- **Phần trăm tiến độ**: Nhân công thực tế đã dành ra cho đến nay ÷ Ước tính hoàn thành (EAC) 
- **Công số còn lại**: Công số ước tính lúc hoàn thành – Công số thực tế đã dành ra cho đến nay 
- **EAC**: Nhân công còn lại + Nhân công thực tế đã dành ra cho đến nay 
- **Chênh lệch nhân công dự kiến**: Nhân công theo kế hoạch – EAC

Project Operations cho thấy dự đoán chênh lệch nhân công trên nhiệm vụ. Nếu EAC nhiều hơn nhân công theo kế hoạch, nghĩa là nhiệm vụ được dự kiến mất nhiều thời gian hơn so với kế hoạch ban đầu và đang chậm lịch trình. Nếu EAC ít hơn nhân công theo kế hoạch, nghĩa là nhiệm vụ được dự kiến mất ít thời gian hơn so với kế hoạch ban đầu và đang nhanh hơn lịch trình.

## <a name="reprojecting-effort-on-leaf-node-tasks"></a>Dự toán lại công số cho các nhiệm vụ nút lá

Người quản lý dự án thường sửa đổi ước tính ban đầu cho nhiệm vụ. Lên kế hoạch lại dự án là khả năng ước tính của người quản lý dự án, dựa trên hiện trạng dự án. Tuy nhiên, những người quản lý dự án nên thay đổi các số liệu công số dự kiến. Điều này là do công số dự kiến của dự án đại diện cho nguồn thông tin thực tế đã thiết lập cho ước tính chi phí và lịch trình của dự án, và tất cả các bên liên quan của dự án đã đồng ý với điều đó.

Người quản lý dự án có thể dự toán lại công số cho nhiệm vụ bằng cách cập nhật **Công số còn lại** mặc định bằng một giá trị ước tính mới cho nhiệm vụ. Việc cập nhật này sẽ dẫn đến tính toán lại giá trị ước tính lúc hoàn thành (EAC) của nhiệm vụ, tỷ lệ phần trăm tiến độ và mức chênh lệch công số đã dự toán trên một nhiệm vụ. EAC, ETC và phần trăm tiến trình trên các nhiệm vụ tóm tắt cũng được tính toán lại và cung cấp dự kiến mới về chênh lệch nhân công.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Lên kế hoạch lại nhân công cho các nhiệm vụ tóm tắt

Có thể lên kế hoạch lại nhân công cho các nhiệm vụ tóm tắt hoặc nhiệm vụ bộ chứa. Người quản lý dự án có thể cập nhật công số còn lại trên các nhiệm vụ tóm tắt. Việc cập nhật công số còn lại sẽ kích hoạt tập hợp các phép tính sau trong ứng dụng:

- EAC và tỷ lệ phần trăm tiến trình trên nhiệm vụ được tính.
- EAC mới được phân phối xuống các nhiệm vụ con trong cùng một tỷ lệ như EAC gốc trên nhiệm vụ.
- EAC mới trên mỗi nhiệm vụ riêng xuống các nhiệm vụ nút lá được tính toán. 
- Các nhiệm vụ con bị ảnh hưởng xuống các nút lá có công số còn lại và tỷ lệ phần trăm tiến trình được tính toán lại dựa trên giá trị EAC. Điều này dẫn đến dự kiến mới cho chênh lệch nhân công của nhiệm vụ. 
- EAC của nhiệm vụ tóm tắt đến các nút gốc được tính toán lại.
- Nỗ lực đã phê duyệt trên một nhiệm vụ tóm tắt là tổng nỗ lực đã phê duyệt trên tất cả các nhiệm vụ con cộng với nỗ lực đã phê duyệt trên nhiệm vụ tóm tắt.
- Nỗ lực còn lại một nhiệm vụ tóm tắt là tổng nỗ lực còn lại trên tất cả các nhiệm vụ con trừ đi nỗ lực đã phê duyệt trên nhiệm vụ tóm tắt.

## <a name="project-status-summary"></a>Tóm tắt trạng thái dự án

Theo dõi dữ liệu trong các dạng xem **Theo dõi nhân lực** và **Theo dõi chi phí** hiển thị tiến trình và mức sử dụng chi phí tại các cấp nút gốc dự án, các nhiệm vụ tóm tắt và nhiệm vụ nút lá. Phần **Trạng thái** trên trang **Thực thể dự án** hiển thị tóm tắt trạng thái cấp độ dự án.

## <a name="status-summary-fields"></a>Trường tóm tắt trạng thái

Trường **Tổng quan trạng thái dự án** là trường có thể chỉnh sửa hiển thị trạng thái tổng quan của dự án. Trường này dùng mã màu, chẳng hạn như xanh lục, vàng và đỏ để chỉ ra rủi ro gia tăng. Trường **Nhận xét** cho phép người quản lý dự án nhập nhận xét cụ thể về trạng thái. Trường **Ngày cập nhật trạng thái** không thể chỉnh sửa và giá trị này là dấu thời gian cho biết thời điểm trạng thái được cập nhật gần đây nhất.

Các trường **Hiệu suất lịch trình** và **Hiệu suất chi phí** được đặt từ ngày theo dõi. Khi chênh lệch lịch trình và chi phí cho các nút gốc trong dạng xem **Theo dõi nhân công** dương, bạn có thể đặt các trường này thành **Trước**. Khi chênh lệch lịch trình và chi phí cho nút gốc âm, bạn có thể đặt các trường này thành **Sau**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
