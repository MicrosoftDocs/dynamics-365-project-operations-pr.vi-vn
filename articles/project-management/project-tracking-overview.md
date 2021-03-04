---
title: Tổng quan về theo dõi dự án
description: Chủ đề này cung cấp thông tin về cách theo dõi tiến độ dự án và mức sử dụng chi phí.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: f159ecac53b824ef208221bb14958923fb5da63b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127401"
---
# <a name="project-tracking-overview"></a>Tổng quan về theo dõi dự án

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Sự cần thiết của việc theo dõi tiến độ đối với lịch trình thay đổi theo ngành. Một số ngành theo dõi ở cấp độ chi tiết, trong khi các ngành khác theo dõi ở cấp độ cao hơn. Chủ đề này cho biết cách lập lịch để đáp ứng các yêu cầu của tổ chức bạn.

## <a name="effort-tracking-view"></a>Dạng xem theo dõi nhân công

Dạng xem **Theo dõi nhân công** theo dõi tiến độ của các nhiệm vụ trong lịch trình bằng cách so sánh số giờ nhân công thực tế dành cho một nhiệm vụ với số giờ nhân công theo kế hoạch của nhiệm vụ. Dynamics 365 Project Operations sử dụng các công thức sau để tính toán các chỉ số theo dõi:

- **Phần trăm tiến độ**: Nhân công thực tế đã dành ra cho đến nay ÷ Ước tính hoàn thành (EAC) 
- **Ước tính hoàn thành (ETC)**: Nhân công theo kế hoạch – Nhân công thực tế đã dành ra cho đến nay 
- **EAC**: Nhân công còn lại + Nhân công thực tế đã dành ra cho đến nay 
- **Chênh lệch nhân công dự kiến**: Nhân công theo kế hoạch – EAC

Project Operations cho thấy dự đoán chênh lệch nhân công trên nhiệm vụ. Nếu EAC nhiều hơn nhân công theo kế hoạch, nghĩa là nhiệm vụ được dự kiến mất nhiều thời gian hơn so với kế hoạch ban đầu và đang chậm lịch trình. Nếu EAC ít hơn nhân công theo kế hoạch, nghĩa là nhiệm vụ được dự kiến mất ít thời gian hơn so với kế hoạch ban đầu và đang nhanh hơn lịch trình.

## <a name="reprojecting-effort"></a>Lên kế hoạch lại nhân công

Người quản lý dự án thường sửa đổi ước tính ban đầu cho nhiệm vụ. Lên kế hoạch lại dự án là khả năng ước tính của người quản lý dự án, dựa trên hiện trạng dự án. Tuy nhiên, chúng tôi khuyên những người quản lý dự án không nên thay đổi các con số cơ sở. Đó là vì chỉ số ban đầu của dự án đại diện cho nguồn tin cậy đã được thiết lập đối với lịch trình và ước tính chi phí của dự án. Tất cả bên liên quan của dự án phải đồng ý với các chỉ số ban đầu.

Người quản lý dự án có thể lên kế hoạch lại nhân công cho nhiệm vụ bằng 2 cách:

- Thay thế ETC mặc định bằng ước tính mới của nhân công còn lại thực tế trên nhiệm vụ. 
- Thay thế phần trăm tiến trình mặc định bằng ước tính mới của tiến trình đúng trên nhiệm vụ.

Mỗi phương pháp sẽ mang đến một phép tính lại ETC, EAC và phần trăm tiến trình của nhiệm vụ cũng như chênh lệch nhân công dự kiến trên nhiệm vụ. EAC, ETC và phần trăm tiến trình trên các nhiệm vụ tóm tắt cũng được tính toán lại và cung cấp dự kiến mới về chênh lệch nhân công.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Lên kế hoạch lại nhân công cho các nhiệm vụ tóm tắt

Có thể lên kế hoạch lại nhân công cho các nhiệm vụ tóm tắt hoặc nhiệm vụ bộ chứa. Bất kể người dùng lên kế hoạch lại bằng nhân công còn lại hay phần trăm tiến trình trên nhiệm vụ tóm tắt, các bộ tính toán sau sẽ hoạt động:

- EAC, ETC và phần trăm tiến trình trên nhiệm vụ được tính.
- EAC mới được phân phối xuống các nhiệm vụ con trong cùng một tỷ lệ như EAC gốc trên nhiệm vụ.
- EAC mới trên mỗi nhiệm vụ riêng xuống các nhiệm vụ nút lá được tính toán. 
- Các nhiệm vụ con bị ảnh hưởng xuống các nút lá có ETC và phần trăm tiến trình được tính toán lại dựa trên giá trị EAC. Điều này dẫn đến dự kiến mới cho chênh lệch nhân công của nhiệm vụ. 
- EAC của nhiệm vụ tóm tắt đến các nút gốc được tính toán lại.

### <a name="cost-tracking-view"></a>Dạng xem theo dõi chi phí 

Dạng xem **Theo dõi chi phí** so sánh chi phí thực tế đã sử dụng cho nhiệm vụ với chi phí dự kiến cho nhiệm vụ. 

> [!NOTE]
> Dạng xem này chỉ hiển thị chi phí lao động và không gồm chi phí từ ước tính chi phí. Project Operations sử dụng các công thức sau để tính toán các chỉ số theo dõi:

- **Phần trăm chi phí đã sử dụng**: Chi phí thực tế đã sử dụng cho đến nay ÷ Chi phí ước tính khi hoàn thành
- **Chi phí hoàn thành (CTC)**: Chi phí theo kế hoạch – Chi phí thực tế đã sử dụng cho đến nay
- **EAC**: Chi phí còn lại + Chi phí thực tế đã sử dụng cho đến nay
- **Chênh lệch chi phí dự kiến**: Chi phí theo kế hoạch – EAC

Dự kiến của chênh lệch chi phí hiển thị trên nhiệm vụ. Nếu EAC lớn hơn chi phí theo kế hoạch, nghĩa là nhiệm vụ được dự kiến mất nhiều chi phí hơn so với kế hoạch ban đầu. Do đó, chi phí của nhiệm vụ có xu hướng vượt quá ngân sách. Nếu EAC ít hơn chi phí theo kế hoạch, nghĩa là nhiệm vụ được dự kiến mất ít chi phí hơn so với kế hoạch ban đầu. Do đó, chi phí của nhiệm vụ có xu hướng ít hơn ngân sách.

## <a name="project-managers-reprojection-of-cost"></a>Người quản lý dự án lên kế hoạch lại chi phí

Khi nhân công được lên kế hoạch lại, CTC, EAC, phần trăm chi phí tiêu thụ và chênh lệch chi phí dự kiến đều được tính toán lại ở dạng xem **Theo dõi chi phí**.

## <a name="project-status-summary"></a>Tóm tắt trạng thái dự án

Theo dõi dữ liệu trong các dạng xem **Theo dõi nhân lực** và **Theo dõi chi phí** hiển thị tiến trình và mức sử dụng chi phí tại các cấp nút gốc dự án, các nhiệm vụ tóm tắt và nhiệm vụ nút lá. Phần **Trạng thái** trên trang **Thực thể dự án** hiển thị tóm tắt trạng thái cấp độ dự án.

## <a name="status-summary-fields"></a>Trường tóm tắt trạng thái

Trường **Tổng quan trạng thái dự án** là trường có thể chỉnh sửa hiển thị trạng thái tổng quan của dự án. Trường này dùng mã màu, chẳng hạn như xanh lục, vàng và đỏ để chỉ ra rủi ro gia tăng. Trường **Nhận xét** cho phép người quản lý dự án nhập nhận xét cụ thể về trạng thái. Trường **Ngày cập nhật trạng thái** không thể chỉnh sửa và giá trị này là dấu thời gian cho biết thời điểm trạng thái được cập nhật gần đây nhất.

Các trường **Hiệu suất lịch trình** và **Hiệu suất chi phí** được đặt từ ngày theo dõi. Khi chênh lệch lịch trình và chi phí cho các nút gốc trong dạng xem **Theo dõi nhân công** dương, bạn có thể đặt các trường này thành **Trước**. Khi chênh lệch lịch trình và chi phí cho nút gốc âm, bạn có thể đặt các trường này thành **Sau**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]