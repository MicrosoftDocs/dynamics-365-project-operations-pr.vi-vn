---
title: Tiến độ dự án và mức sử dụng chi phí
description: Chủ đề này cung cấp thông tin về cách theo dõi tiến độ dự án và mức sử dụng chi phí.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 0d742164-5469-421d-8917-63160a81f651
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8aa5814938129f30885d8161a7c86197ab013364
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 03/24/2020
ms.locfileid: "3757114"
---
# <a name="project-progress-and-cost-consumption"></a>Tiến độ dự án và mức sử dụng chi phí

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Sự cần thiết của việc theo dõi tiến độ đối với lịch trình thay đổi theo ngành. Một số ngành theo dõi ở cấp độ chi tiết, trong khi các ngành khác theo dõi ở cấp độ cao hơn. Chủ đề này cho biết cách lập lịch để đáp ứng các yêu cầu của tổ chức bạn.

## <a name="effort-tracking-view"></a>Dạng xem theo dõi nhân công

Dạng xem **Theo dõi nhân công** theo dõi tiến độ của nhiệm vụ trong lịch trình. Dạng xem này so sánh giờ nhân công thực tế đã sử dụng cho nhiệm vụ so với giờ nhân công dự kiến cho nhiệm vụ đó. PSA sử dụng các công thức sau để tính toán các chỉ số theo dõi:

- Phần trăm tiến độ = Nhân công thực thế đã dành ra cho đến nay ÷ Nhân công theo kế hoạch cho nhiệm vụ 
- Ước tính hoàn thành (ETC) = Nhân công theo kế hoạch – Nhân công thực tế đã dành ra cho đến nay 
- Ước tính hoàn thành (EAC) = Nhân công còn lại + Nhân công thực tế đã dành ra cho đến nay 
- Chênh lệch nhân công dự kiến = Nhân công theo kế hoạch – EAC

PSA cho thấy dự đoán chênh lệch nhân công trên nhiệm vụ. Nếu EAC nhiều hơn nhân công theo kế hoạch, nghĩa là nhiệm vụ được dự kiến mất nhiều thời gian hơn so với kế hoạch ban đầu. Do đó, nhiệm vụ kết thúc muộn hơn so với lịch trình. Nếu EAC nhỏ hơn nhân công dự kiến, nghĩa là nhiệm vụ được dự kiến mất ít thời gian hơn so với kế hoạch ban đầu. Do đó, nhiệm vụ kết thúc sớm hơn so với lịch trình.

## <a name="re-projecting-effort"></a>Lên kế hoạch lại nhân công

Người quản lý dự án thường có thể sửa đổi ước tính ban đầu cho một nhiệm vụ. Lên kế hoạch lại dự án là nhận thức ước tính của người quản lý dự án, dựa trên hiện trạng dự án. Tuy nhiên, người quản lý dự án không nên thay đổi các chỉ số ban đầu vì chỉ số ban đầu của dự án đại diện cho nguồn tin cậy đã được thiết lập đối với lịch trình và ước tính chi phí của dự án. Tất cả bên liên quan của dự án phải đồng ý với các chỉ số ban đầu.

Có hai cách mà người quản lý dự án có thể lên kế hoạch lại nhân công trên nhiệm vụ:

- Thay thế ETC mặc định bằng ước tính mới của nhân công còn lại thực tế trên nhiệm vụ. 
- Thay thế phần trăm tiến trình mặc định bằng ước tính mới của tiến trình đúng trên nhiệm vụ.

Mỗi cách tiếp cận này mang đến một phép tính lại ETC, EAC và phần trăm tiến trình của nhiệm vụ cũng như chênh lệch nhân công dự kiến trên nhiệm vụ. EAC, ETC và phần trăm tiến trình trên các nhiệm vụ tóm tắt cũng được tính toán lại và cung cấp dự kiến mới về chênh lệch nhân công.

## <a name="re-projection-of-effort-on-summary-tasks"></a>Lên kế hoạch lại nhân công cho các nhiệm vụ tóm tắt

Có thể lên kế hoạch lại nhân công trên các nhiệm vụ tóm tắt hoặc nhiệm vụ bộ chứa. Bất kể người dùng lên kế hoạch lại bằng nhân công còn lại hay phần trăm tiến trình trên nhiệm vụ tóm tắt, các bộ tính toán sau sẽ bắt đầu:

- EAC, ETC và phần trăm tiến trình trên nhiệm vụ được tính.
- EAC mới được phân phối xuống các nhiệm vụ con trong cùng một tỷ lệ như EAC gốc trên nhiệm vụ.
- EAC mới trên mỗi nhiệm vụ riêng xuống các nhiệm vụ nút lá được tính toán. 
- Các nhiệm vụ con bị ảnh hưởng xuống các nút lá có ETC và phần trăm tiến trình được tính toán lại dựa trên giá trị EAC. Điều này dẫn đến dự kiến mới cho chênh lệch nhân công của nhiệm vụ. 
- EAC của nhiệm vụ tóm tắt đến các nút gốc được tính toán lại.

### <a name="cost-tracking-view"></a>Dạng xem theo dõi chi phí 

Dạng xem **Theo dõi chi phí** so sánh chi phí thực tế đã sử dụng cho nhiệm vụ với chi phí dự kiến cho nhiệm vụ. 

> [!NOTE]
> Dạng xem này chỉ hiển thị chi phí lao động và không gồm chi phí từ ước tính chi phí. 

PSA sử dụng các công thức sau để tính toán các chỉ số theo dõi:

- Phần trăm chi phí đã sử dụng = Chi phí thực tế đã sử dụng cho đến nay ÷ Chi phí theo kế hoạch cho nhiệm vụ
- Chi phí hoàn thành (CTC) = Chi phí theo kế hoạch – Chi phí thực tế đã sử dụng cho đến nay
- EAC = CTC + Chi phí thực tế đã sử dụng cho đến nay
- Chênh lệch chi phí dự kiến = Chi phí theo kế hoạch – EAC

Dự kiến của chênh lệch chi phí hiển thị trên nhiệm vụ. Nếu EAC lớn hơn chi phí theo kế hoạch, nghĩa là nhiệm vụ được dự kiến mất nhiều chi phí hơn so với kế hoạch ban đầu. Do đó, chi phí của nhiệm vụ có xu hướng vượt quá ngân sách. Nếu EAC ít hơn chi phí theo kế hoạch, nghĩa là nhiệm vụ được dự kiến mất ít chi phí hơn so với kế hoạch ban đầu. Do đó, chi phí của nhiệm vụ có xu hướng ít hơn ngân sách.

## <a name="project-managers-re-projection-of-cost"></a>Lên kế hoạch lại chi phí của người quản lý dự án

Khi nhân công được lên kế hoạch lại, CTC, EAC, phần trăm chi phí tiêu thụ và chênh lệch chi phí dự kiến đều được tính toán lại trong dạng xem **Theo dõi chi phí**.

## <a name="project-status-summary"></a>Tóm tắt trạng thái dự án

Theo dõi dữ liệu trong các dạng xem **Theo dõi nhân lực** và **Theo dõi chi phí** hiển thị tiến trình và mức sử dụng chi phí tại các cấp nút gốc dự án, các nhiệm vụ tóm tắt và nhiệm vụ nút lá. Phần **Trạng thái** trên trang **Thực thể dự án** hiển thị tóm tắt trạng thái cấp độ dự án.

## <a name="status-summary-fields"></a>Trường tóm tắt trạng thái

Trường **Tổng quan trạng thái dự án** là trường có thể chỉnh sửa hiển thị trạng thái tổng quan của dự án. Trường này dùng mã màu, chẳng hạn như xanh lục, vàng và đỏ để chỉ ra rủi ro gia tăng. Trường **Nhận xét** cho phép người quản lý dự án nhập nhận xét cụ thể về trạng thái. Trường **Ngày cập nhật trạng thái** không thể chỉnh sửa và giá trị này là dấu thời gian cho biết thời điểm trạng thái được cập nhật gần đây nhất.

Các trường **Hiệu suất lịch trình** và **Hiệu suất chi phí** được đặt từ ngày theo dõi. Khi chênh lệch lịch trình và chi phí cho các nút gốc trong dạng xem **Theo dõi nhân công** dương, bạn có thể đặt các trường này thành **Trước**. Khi chênh lệch lịch trình và chi phí cho nút gốc âm, bạn có thể đặt các trường này thành **Sau**.
