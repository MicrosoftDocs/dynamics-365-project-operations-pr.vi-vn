---
title: Sử dụng trường hiện có trong Project Service làm thông số định giá
description: Bài viết này cung cấp thông tin về cách sử dụng trường Project Service hiện có làm thông số định giá.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: abc3a3a2b61ea6f8dd34d82bf91546f8f7552a61
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925238"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a>Sử dụng trường hiện có trong Project Service làm thông số định giá

[!include [banner](../includes/psa-now-project-operations.md)]

Project Service Automation (PSA) có nhiều trường trên thực thể **Thực tế** có thể dùng làm thông số định giá để định giá dựa trên tài nguyên trong tổ chức dự án. Ví dụ: một trường thường gặp là **Nguồn lực có thể đặt**. Các công ty nhỏ hơn có ít hơn 20-30 nguồn lực có thể tính phí có thể thấy rằng việc có tỷ lệ chi phí và hóa đơn cụ thể cho từng nguồn lực là cách tiếp cận đơn giản hơn. Tuy nhiên, khi lực lượng lao động có thể tính phí tăng lên, mức giá cố định có thể trở nên không thực tế vì chi phí nguồn lực và mức tính phí bắt đầu thay đổi khi nguồn lực được thăng chức, có thêm kinh nghiệm hoặc đòi hỏi nhóm kỹ năng khác. Vì cách tiếp cận này vẫn phù hợp với các công ty có quy mô nhất định, hãy xem [Sử dụng nguồn lực có thể đặt trước làm thông số định giá](bookable-resource-pricing-dimension.md) để tìm hiểu cách dùng trường Project Service làm thông số định giá.

Một ví dụ khác là đối với loại giao dịch. Khách hàng và Người thực hiện đã sử dụng loại giao dịch trong PSA để phân loại công việc và sử dụng trường để định giá và chi phí dựa trên loại công việc. Để biết thêm thông tin, hãy xem [Sử dụng loại giao dịch làm thông số định giá](transaction-category-pricing-dimension.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
