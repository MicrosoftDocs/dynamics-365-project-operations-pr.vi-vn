---
title: Theo dõi trạng thái của dự án
description: Làm cách nào để theo dõi tình trạng dự án trong Project Service
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 58274886a9f9ce6ae49c64c1d7ac491e29c7d06c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593408"
---
# <a name="track-a-projects-status-project-service"></a>Theo dõi tình trạng dự án (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Sử dụng [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] để theo dõi tiến độ dự án của khách hàng.  

Về khía cạnh tiến độ cam kết, các giai đoạn dự án sẽ cập nhật để phản ánh giai đoạn cam kết:  

| Tác vụ | Description | 
|------------|----------|
| **New** | Khi bạn tạo một dự án, giai đoạn sẽ được đặt thành **Mới**. Nếu bạn đã tạo dự án từ một mẫu, ở giai đoạn này, dự án có thể có dữ liệu về lịch trình, ước tính và nhóm. Nếu không, đó sẽ là bản phác thảo của dự án và bạn cần phải nhập các thành phần còn lại của dự án theo cách thủ công. |
| **Báo giá** |  Khi bạn liên kết một dự án với một câu trích dẫn hoặc tạo nó từ một câu trích dẫn, giai đoạn dự án được đặt thành **Trích dẫn** và ngày bắt đầu và ngày kết thúc ước tính cũng được cập nhật. Khi dự án đang trong giai đoạn báo giá, các chi tiết về báo giá sẽ hiển thị trên tab **Kinh doanh** trên trang **Dự án**. |
| **Kế hoạch** |  Khi báo giá được liên kết với một dự án của bạn giành chiến thắng thì tiến độ cam kết cho giai đoạn hợp đồng, giai đoạn dự án sẽ cập nhật thành **Kế hoạch**. Chi tiết hợp đồng sẽ hiển thị trên tab **Kinh doanh** trên trang **Dự án**. |
| **Hoàn thành** | Khi đã hoàn tất công việc dự án, bạn có thể chuyển giai đoạn thành **Hoàn tất**. Khi giai đoạn dự án được đặt thành hoàn tất, mọi người sẽ hiểu rằng các công việc đã hoàn thành 100% nhưng dự án vẫn được để mở cho việc ghi lại bất kỳ mục nhập chi phí hoặc thời gian đang chờ xử lý nào. |
| **Đóng** | Khi tất cả các giao dịch đã được ghi lại trên dự án và bạn không muốn ghi thêm bất kỳ chi tiết nào nữa thì bạn có thể đặt giai đoạn thành **Đóng** theo cách thủ công. Khi dự án được đặt thành **Đóng**, bạn không thể ghi thêm bất kỳ giao dịch nào khác trên dự án và dự án sẽ ở trạng thái chỉ đọc. |

## <a name="to-track-a-projects-status"></a>Cách theo dõi trạng thái của dự án  

1.  Đi tới **Project Service > Dự án**.  

2.  Bấm vào dự án mà bạn muốn làm việc.  

3.  Trong thanh ở đầu màn hình, chọn mũi tên xuống bên cạnh tên dự án, sau đó bấm vào **Theo dõi Dự án**.  

4.  Chọn **Theo dõi Nỗ lực** hoặc **Theo dõi Chi phí** trong danh sách thả xuống ở trên danh sách tác vụ.  

5.  Bấm đúp vào bất cứ tác vụ nào để chỉnh sửa. Bạn cũng có thể di chuyển hoặc thay đổi kích thước các thanh trong biểu đồ Gantt để thay đổi thời gian và tiến bộ cho một nhiệm vụ.  

### <a name="see-also"></a>Xem thêm  
 [Hướng dẫn của Quản lý Dự án](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
