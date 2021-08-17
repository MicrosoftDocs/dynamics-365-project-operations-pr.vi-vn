---
title: Đặt nguồn lực có tên từ yêu cầu nguồn lực
description: Chủ đề này cung cấp thông tin về đặt lịch nguồn lực có tên cho một yêu cầu nguồn lực chung.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: e929a5fb4c307d3b64d0f7f70203fe20bc6dd4f99e89e039fae0ce8276c69c52
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/06/2021
ms.locfileid: "7000512"
---
# <a name="book-named-resources-from-resource-requirements"></a>Đặt nguồn lực có tên từ yêu cầu nguồn lực

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Bạn có thể đặt một nguồn lực được đặt tên để thay thế nguồn lực chung có yêu cầu nguồn lực.

1. Trong Project Service Automation (PSA), trên trang **Dự án**, nhấp vào tab **Nhóm**.
2. Chọn nguồn lực chung có yêu cầu nguồn lực từ danh sách, sau đó nhấp vào **Đặt lịch**. Hoặc mở yêu cầu nguồn lực rồi nhấp vào **Đặt lịch**.


![Đặt một thành viên nhóm chung.](media/RM-how-to-14.png)


3. Trên trang **Trợ lý lịch trình**, chọn nguồn lực có tên để đặt lịch vào nhóm dự án của bạn rồi nhấp vào **Đặt lịch**.

![Đặt một thành viên nhóm chung bằng trợ lý lịch trình.](media/RM-how-to-15.png)

Khi đặt lịch xong và được thực hiện bởi một nguồn lực có tên, thì nguồn lực chung được thay thế bằng nguồn lực có tên đó.

![Thành viên nhóm có tên thay thế cho thành viên nhóm chung.](media/RM-how-to-16.png)

Các phân công trên lịch trình cũng được cập nhật bằng nguồn lực có tên.

![Thành viên nhóm có tên được phân công cho nhiệm vụ dự án.](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Hoàn thành một nguồn lực chung với nhiều nguồn lực được đặt tên
Thực hiện một yêu cầu cho một nguồn lực chung với nhiều nguồn lực có tên sẽ tương tự như việc gán một nguồn lực có tên. Ví dụ: có một nhiệm vụ với thời gian năm ngày và 120 giờ làm việc. Một nguồn lực không thể hoàn thành nhiệm vụ này trong tám giờ trong năm ngày trong tuần. 

![Một nhiệm vụ cần 120 giờ trong năm ngày.](media/RM-how-to-21.png)

Yêu cầu này là cho 120 giờ kỹ thuật robot trong năm ngày, trong đó mỗi ngày 24 giờ.

![Yêu cầu theo ngày.](media/RM-how-to-22.png)

Đây là một ví dụ khi nhiều nguồn lực được đặt tên là cần thiết để hoàn thành một yêu cầu nguồn lực chung. Bạn sẽ cần phải đặt nhiều nguồn lực để hoàn thành yêu cầu.

![Đặt nhiều nguồn lực để hoàn thành yêu cầu.](media/RM-how-to-23.png)

Sự khác biệt chính trong trường hợp này là nguồn lực chung vẫn còn trên nhóm được chỉ định nhiệm vụ và các thành viên nhóm nguồn lực được đặt tên không được chỉ định là một phần của vị trí. Người quản lý dự án có thể gán công việc phù hợp với các nguồn lực được đặt tên. Dạng xem **Hợp nhất** có thể hỗ trợ người quản lý dự án trong việc chia các đặt lịch cho nhiều nguồn lực cho phân công nhiệm vụ. Điều này không được thực hiện tự động bởi vì trong bất kỳ trường hợp nào phức tạp hơn ví dụ đơn giản ở trên, chẳng hạn như nơi bạn có một yêu cầu gồm nhiều nhiệm vụ, ý định về cách thức người quản lý dự án muốn chỉ định, mà hệ thống cần tính đến. Bởi vì hệ thống không thể hiểu được ý định, nên có khả năng là các giả định sẽ khác với dự kiến và cho một kết quả không chính xác hoặc không thể đoán trước. Kết quả dự đoán được đó là nguồn lực chung vẫn được gán cho đến khi ngời quản lý dự án cố ý tạo phân công với sự trợ giúp của dạng xem **Hợp nhất**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]