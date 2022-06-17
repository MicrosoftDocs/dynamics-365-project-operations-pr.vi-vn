---
title: Phân tích báo giá dự án
description: Bài báo này cung cấp thông tin về phân tích báo giá dự án.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
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
ms.openlocfilehash: 9db924c16c5eca17e7962ff1d88b09e581347fa5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919304"
---
# <a name="analysis-of-project-quotes"></a>Phân tích báo giá dự án

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation phân tích báo giá dự án để ước tính lợi nhuận. Nó cũng phân tích xem báo cáo thống nhất như thế nào với kỳ vọng của khách hàng về ngày giao hàng hoặc ngày hoàn thành và về ngân sách.

## <a name="profitability-analysis"></a>Phân tích suất sinh lợi

Project Service Automation phân tích suất sinh lợi bằng cách sử dụng lãi gộp và lãi gộp điều chỉnh.

- Lãi gộp được tính bằng cách sử dụng công thức sau đây:

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- Lãi gộp điều chỉnh được tính bằng cách sử dụng công thức sau đây:

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

Nếu giá trị cho lãi gộp và lãi gộp điều chỉnh khác với lãi chung, thì hầu hết công việc trong báo giá được phân loại là không thể tính phí.

## <a name="analysis-of-customer-expectations"></a>Phân tích kỳ vọng của khách hàng

Bạn có thể phân tích báo giá và tạo biểu đồ cho kỳ vọng của khách hàng về lịch trình cũng như ngân sách nếu bạn nhập giá trị cho các trường sau:

- Trường **Ngày giao hàng yêu cầu** trên tiêu đề báo giá.
- Trường **Ngân sách khách hàng** cho mỗi dòng báo giá (đối với các dòng dựa trên dự án và các dòng dựa trên sản phẩm).

Phân tích các kỳ vọng của khách hàng về lịch trình được thực hiện bằng cách so sánh ngày kết thúc mới nhất của chi tiết dòng báo giá với ngày giao hàng yêu cầu trên tất cả các dòng báo giá trong báo giá.

Phân tích các kỳ vọng của khách hàng về ngân sách được thực hiện bằng cách so sánh tổng của tổng ngân sách khách hàng với số tiền báo giá trên tất cả các dòng báo giá.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
