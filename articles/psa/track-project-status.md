---
title: Theo dõi trạng thái của dự án
description: Làm cách nào để theo dõi tình trạng dự án trong Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 70d07c98bd9432712e939445dbf867b96642f5ba
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087194"
---
# <a name="track-a-projects-status-project-service"></a>Theo dõi tình trạng dự án (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Sử dụng [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] để theo dõi tiến độ dự án của khách hàng.  

Về khía cạnh tiến độ cam kết, các giai đoạn dự án sẽ cập nhật để phản ánh giai đoạn cam kết:  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   **Mới**    | Khi bạn tạo một dự án, giai đoạn sẽ được đặt thành **Mới**. Nếu bạn đã tạo dự án từ một mẫu, ở giai đoạn này, dự án có thể có dữ liệu về lịch trình, ước tính và nhóm. Nếu không, đó sẽ là bản phác thảo của dự án và bạn cần phải nhập các thành phần còn lại của dự án theo cách thủ công. |
|  **Báo giá**   |      Khi bạn liên kết một dự án với một báo giá hoặc tạo dự án từ báo giá, giai đoạn dự án được đặt thành **Báo giá** và ngày bắt đầu và kết thúc ước tính cũng sẽ được cập nhật. Khi dự án đang trong giai đoạn báo giá, các chi tiết về báo giá sẽ hiển thị trên tab **Kinh doanh** trên trang **Dự án**.      |
|   **Kế hoạch**   |                                     Khi báo giá được liên kết với một dự án của bạn giành chiến thắng thì tiến độ cam kết cho giai đoạn hợp đồng, giai đoạn dự án sẽ cập nhật thành **Kế hoạch**. Chi tiết hợp đồng sẽ hiển thị trên tab **Kinh doanh** trên trang **Dự án**.                                      |
| **Hoàn thành** |                    Khi đã hoàn tất công việc dự án, bạn có thể chuyển giai đoạn thành **Hoàn tất**. Khi giai đoạn dự án được đặt thành hoàn tất, mọi người sẽ hiểu rằng các công việc đã hoàn thành 100% nhưng dự án vẫn được để mở cho việc ghi lại bất kỳ mục nhập chi phí hoặc thời gian đang chờ xử lý nào.                     |
|  **Đóng**   |           Khi tất cả các giao dịch đã được ghi lại trên dự án và bạn không muốn ghi thêm bất kỳ chi tiết nào nữa thì bạn có thể đặt giai đoạn thành **Đóng** theo cách thủ công. Khi dự án được đặt thành **Đóng** , bạn không thể ghi thêm bất kỳ giao dịch nào khác trên dự án và dự án sẽ ở trạng thái chỉ đọc.           |

## <a name="to-track-a-projects-status"></a>Cách theo dõi trạng thái của dự án  

1.  Đi tới **Project Service > Dự án**.  

2.  Bấm vào dự án mà bạn muốn làm việc.  

3.  Trong thanh ở đầu màn hình, chọn mũi tên xuống bên cạnh tên dự án, sau đó bấm vào **Theo dõi Dự án**.  

4.  Chọn **Theo dõi Nỗ lực** hoặc **Theo dõi Chi phí** trong danh sách thả xuống ở trên danh sách tác vụ.  

5.  Bấm đúp vào bất cứ tác vụ nào để chỉnh sửa. Bạn cũng có thể di chuyển hoặc thay đổi kích thước các thanh trong biểu đồ Gantt để thay đổi thời gian và tiến bộ cho một nhiệm vụ.  

### <a name="see-also"></a>Xem thêm  
 [Hướng dẫn của Quản lý Dự án](../psa/project-manager-guide.md)
