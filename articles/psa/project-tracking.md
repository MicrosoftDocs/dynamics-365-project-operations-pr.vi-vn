---
title: Tiến độ dự án và mức sử dụng chi phí
description: Bài viết này cung cấp thông tin về việc theo dõi tiến độ dự án và chi phí tiêu thụ.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 08/21/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: afcac5e6fbb7ed8a5a5f7f5876c6035b59eebcc2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921788"
---
# <a name="project-progress-and-cost-consumption"></a>Tiến độ dự án và mức sử dụng chi phí

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Sự cần thiết của việc theo dõi tiến độ đối với lịch trình thay đổi theo ngành. Một số ngành theo dõi ở cấp độ chi tiết, trong khi các ngành khác theo dõi ở cấp độ cao hơn. Bài viết này chỉ ra cách lập lịch để đáp ứng các yêu cầu của tổ chức bạn.

## <a name="effort-tracking-view"></a>Dạng xem theo dõi nhân công

Dạng xem **Theo dõi nhân công** theo dõi tiến độ của nhiệm vụ trong lịch trình. Dạng xem này so sánh thời gian thực tế đã thực hiện nhiệm vụ so với thời gian dự kiến. Project Service Automation sử dụng các công thức sau để tính toán các chỉ số theo dõi:

Ban đầu khi tạo nhiệm vụ: Chi phí theo kế hoạch sẽ được đặt thành Chi phí ước tính khi hoàn thành. Khi Giá trị thực tế được ghi lại trong nhiệm vụ, sau đây sẽ là phép tính trên dạng xem Theo dõi đối với Nhân công

- Phần trăm tiến độ = Nhân công thực tế đã dành ra cho đến nay ÷ Ước tính hoàn thành (EAC) 
- Ước tính hoàn thành (ETC) = Ước tính hoàn thành (EAC) - Nhân công thực tế đã dành ra cho đến nay 
- EAC = Nhân công còn lại + Nhân công thực tế đã dành ra cho đến nay 
- Chênh lệch nhân công dự kiến = Nhân công theo kế hoạch – EAC

Project Service Automation cho thấy dự đoán chênh lệch nhân công trên nhiệm vụ. Nếu EAC nhiều hơn nhân công theo kế hoạch, nghĩa là nhiệm vụ được dự kiến mất nhiều thời gian hơn so với kế hoạch ban đầu. Do đó, nhiệm vụ kết thúc muộn hơn so với lịch trình. Nếu EAC nhỏ hơn nhân công dự kiến, nghĩa là nhiệm vụ được dự kiến mất ít thời gian hơn so với kế hoạch ban đầu. Do đó, nhiệm vụ kết thúc sớm hơn so với lịch trình.

## <a name="reprojecting-effort"></a>Lên kế hoạch lại nhân công

Người quản lý dự án thường có thể sửa đổi ước tính ban đầu cho một nhiệm vụ. Lên kế hoạch lại dự án là khả năng ước tính của người quản lý dự án, dựa trên hiện trạng dự án. Tuy nhiên, người quản lý dự án không nên thay đổi các chỉ số ban đầu vì chỉ số ban đầu của dự án đại diện cho nguồn tin cậy đã được thiết lập đối với lịch trình và ước tính chi phí của dự án. Tất cả bên liên quan của dự án phải đồng ý với các chỉ số ban đầu.

Người quản lý dự án có thể lên kế hoạch lại nhân công cho nhiệm vụ bằng 2 cách:

- Thay thế ETC mặc định bằng ước tính mới của nhân công còn lại thực tế trên nhiệm vụ. 
- Thay thế phần trăm tiến trình mặc định bằng ước tính mới của tiến trình đúng trên nhiệm vụ.

Mỗi cách tiếp cận này mang đến một phép tính lại ETC, EAC và phần trăm tiến trình của nhiệm vụ cũng như chênh lệch nhân công dự kiến trên nhiệm vụ. EAC, ETC và phần trăm tiến trình trên các nhiệm vụ tóm tắt cũng được tính toán lại và cung cấp dự kiến mới về chênh lệch nhân công.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Lên kế hoạch lại nhân công cho các nhiệm vụ tóm tắt

Có thể lên kế hoạch lại nhân công cho các nhiệm vụ tóm tắt hoặc nhiệm vụ bộ chứa. Bất kể người dùng lên kế hoạch lại bằng nhân công còn lại hay phần trăm tiến trình trên nhiệm vụ tóm tắt, các bộ tính toán sau sẽ hoạt động:

- EAC, ETC và phần trăm tiến trình trên nhiệm vụ được tính.
- EAC mới được phân phối xuống các nhiệm vụ con trong cùng một tỷ lệ như EAC gốc trên nhiệm vụ.
- EAC mới trên mỗi nhiệm vụ riêng xuống các nhiệm vụ nút lá được tính toán. 
- Các nhiệm vụ con bị ảnh hưởng xuống các nút lá có ETC và phần trăm tiến trình được tính toán lại dựa trên giá trị EAC. Điều này dẫn đến dự kiến mới cho chênh lệch nhân công của nhiệm vụ. 
- EAC của nhiệm vụ tóm tắt đến các nút gốc được tính toán lại.

### <a name="cost-tracking-view"></a>Dạng xem theo dõi chi phí 

Dạng xem **Theo dõi chi phí** so sánh chi phí thực tế đã sử dụng cho nhiệm vụ với chi phí theo kế hoạch. 

> [!NOTE]
> Dạng xem này chỉ hiển thị chi phí lao động và không gồm chi phí từ ước tính chi phí. 

Project Service Automation sử dụng các công thức sau để tính toán các chỉ số theo dõi:

Khi một nhiệm vụ được tạo, chi phí theo kế hoạch bằng với chi phí ước tính khi hoàn thành. Sau khi các giá trị thực tế được ghi lại trong nhiệm vụ, phép tính sau đây được thực hiện trên dạng xem **Theo dõi** cho chi phí:

 - Phần trăm chi phí đã sử dụng = Chi phí thực tế đã sử dụng cho đến nay ÷ Chi phí ước tính khi hoàn thành nhiệm vụ
 - Chi phí hoàn thành (CTC) = Chi phí ước tính khi hoàn thành – Chi phí thực tế đã sử dụng cho đến nay
 - Chi phí hoàn thành (CTC) = CTC + Chi phí thực tế đã sử dụng cho đến nay
 - Chênh lệch chi phí dự kiến = Chi phí theo kế hoạch – Chi phí hoàn thành

Dự kiến của chênh lệch chi phí hiển thị trên nhiệm vụ. Nếu chi phí ước tính khi hoàn thành lớn hơn chi phí theo kế hoạch, nghĩa là nhiệm vụ được dự kiến mất nhiều chi phí hơn so với kế hoạch ban đầu. Do đó, chi phí của nhiệm vụ có xu hướng vượt quá ngân sách. Nếu chi phí ước tính khi hoàn thành nhỏ hơn chi phí theo kế hoạch, nghĩa là nhiệm vụ được dự kiến mất ít chi phí hơn so với kế hoạch ban đầu và có xu hướng ít hơn ngân sách.

## <a name="project-managers-reprojection-of-cost"></a>Người quản lý dự án lên kế hoạch lại chi phí

Khi nhân công được lên kế hoạch lại, CTC, Chi phí ước tính khi hoàn thành, phần trăm chi phí tiêu thụ và chênh lệch chi phí dự kiến đều được tính toán lại trong dạng xem **Theo dõi chi phí**.

## <a name="project-status-summary"></a>Tóm tắt trạng thái dự án

Theo dõi dữ liệu trong các dạng xem **Theo dõi nhân lực** và **Theo dõi chi phí** hiển thị tiến trình và mức sử dụng chi phí tại các cấp nút gốc dự án, các nhiệm vụ tóm tắt và nhiệm vụ nút lá. Phần **Trạng thái** trên trang **Thực thể dự án** hiển thị tóm tắt trạng thái cấp độ dự án.

## <a name="status-summary-fields"></a>Trường tóm tắt trạng thái

Trường **Tổng quan trạng thái dự án** là trường có thể chỉnh sửa hiển thị trạng thái tổng quan của dự án. Trường này dùng mã màu, chẳng hạn như xanh lục, vàng và đỏ để chỉ ra rủi ro gia tăng. Trường **Nhận xét** cho phép người quản lý dự án nhập nhận xét cụ thể về trạng thái. Trường **Ngày cập nhật trạng thái** không thể chỉnh sửa và giá trị này là dấu thời gian cho biết thời điểm trạng thái được cập nhật gần đây nhất.

Các trường **Hiệu suất lịch trình** và **Hiệu suất chi phí** được đặt từ ngày theo dõi. Khi chênh lệch lịch trình và chi phí cho các nút gốc trong dạng xem **Theo dõi nhân công** dương, bạn có thể đặt các trường này thành **Trước**. Khi chênh lệch lịch trình và chi phí cho nút gốc âm, bạn có thể đặt các trường này thành **Sau**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
