---
title: Lên lịch dự án với cấu trúc phân tích công việc
description: Làm cách nào để lên lịch dự án bằng cấu trúc phân tích công việc trong Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 04f30f2f2ed93dd1525f1c86a7521cdbf39a77bc
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127904"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a>Lên lịch dự án bằng cấu trúc phân tích công việc (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Lịch trình dự án cho biết những việc cần được thực hiện, nguồn lực nào sẽ thực hiện công việc và khung thời gian cần hoàn thành công việc. Lịch trình dự án phản ánh tất cả công việc liên quan đến việc cung cấp dự án đúng thời gian. Một trong những bước đầu tiên trong giai đoạn khởi đầu của dự án là tạo lịch trình dự án. Để thiết lập một lịch trình dự án, bạn cần phải tạo một cấu trúc phân tích công việc.  
  
 Tạo cấu trúc dự án với cấu trúc phân tích công việc giúp bạn:  
  
- Phân tích công việc thành các nhiệm vụ có thể quản lý  
  
- Ước tính thời gian cần thiết để hoàn thành công việc  
  
- Thiết lập đối tượng phụ thuộc nhiệm vụ và khoảng thời gian của nhiệm vụ  
  
- Xác định vai trò cần thiết để hoàn thành mỗi nhiệm vụ  
  
  Lịch trình dự án trong cấu trúc phân tích công việc có giao diện quen thuộc, hoàn chỉnh với biểu đồ Gantt tương tác.  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a>Tạo cấu trúc phân tích công việc cho một dự án  
 Tạo cấu trúc phân tích công việc đại diện cho chuỗi các nhiệm vụ trong một dự án. Cấu trúc phân tích công việc bao gồm các nhiệm vụ, yêu cầu đối với từng nhiệm vụ và thông tin về doanh thu và chi phí. Trong cấu trúc phân tích công việc của bạn, bạn có thể thêm:  
  
-   Trình tự nhiệm vụ trong một hệ thống cấp bậc  
  
-   Các nhiệm vụ khác, nếu có, phải được hoàn thành trước khi có thể bắt đầu một nhiệm vụ  
  
-   Ngày bắt đầu, ngày kết thúc và khoảng thời gian của nhiệm vụ  
  
-   Số giờ cần cho một nhiệm vụ  
  
-   Mọi kỹ năng và bằng cấp công nhân được yêu cầu  
  
-   Công nhân được giao nhiệm vụ  
  
-   Chi phí và doanh thu ước tính  
  
## <a name="task-types"></a>Loại nhiệm vụ  
Bạn sẽ sử dụng các loại nhiệm vụ sau khi tạo cấu trúc phân tích công việc:  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| **Nút gốc dự án**. | Nhiệm vụ tóm tắt cấp cao cho dự án. Tất cả các nhiệm vụ khác của dự án được tạo trong nhiệm vụ này. Tên của nhiệm vụ gốc là tên dự án. Nỗ lực, ngày tháng và thời gian của nút gốc dựa trên các giá trị trên hệ thống cấp bậc dưới nó. Bạn không thể chỉnh sửa thuộc tính nút gốc hoặc xóa nút gốc. | 
| **Nhiệm vụ tóm tắt hoặc vùng chứa** | Nhiệm vụ tóm tắt là nhiệm vụ có các nhiệm vụ phụ trong đó. Nhiệm vụ tóm tắt không có bất kỳ nỗ lực làm việc hoặc chi phí riêng nào. Nỗ lực làm việc và chi phí là tập hợp các nhiệm vụ phụ. Bạn có thể thay đổi tên của nhiệm vụ tóm tắt, nhưng bạn không thể thay đổi nỗ lực, ngày tháng hoặc thời gian thực hiện, bởi vì những yếu tố này được tính toán tự động. Xóa nhiệm vụ tóm tắt sẽ xóa nhiệm vụ và tất cả các nhiệm vụ phụ.|  
| **Nhiệm vụ nút lá** | Nhiệm vụ nút lá biểu thị công việc chi tiết nhất trên dự án. Nhiệm vụ này có nỗ lực ước tính, số nguồn lực theo kế hoạch, ngày bắt đầu và kết thúc theo kế hoạch và khoảng thời gian.|

  
## <a name="task-hierarchy"></a>Hệ thống cấp bậc của nhiệm vụ  
 Bạn có các tùy chọn sau khi tạo hệ thống cấp bậc của nhiệm vụ:  
  
- **Thêm nhiệm vụ**.   Bạn có thể thêm một nhiệm vụ tại vị trí mà bạn chọn trong hệ thống cấp bậc của nhiệm vụ. Nếu bạn không chọn một vị trí, nhiệm vụ mới của bạn sẽ xuất hiện ở cuối.  
  
- **Thụt lề nhiệm vụ**.   Thụt lề nhiệm vụ để tạo nhiệm vụ con ngay bên trên.  
  
- **Tăng lề nhiệm vụ**.   Tăng lề nhiệm vụ để nhiệm vụ đó không còn là nhiệm vụ phụ của nhiệm vụ chính gốc nữa.  
  
- **Chuyển lên và chuyển xuống**.   Di chuyển nhiệm vụ lên và xuống trong hệ thống cấp bậc của nhiệm vụ chính. Di chuyển một nhiệm vụ lên hoặc xuống không ảnh hưởng đến nỗ lực, chi phí, ngày hoặc khoảng thời gian của nhiệm vụ.  
  
## <a name="task-attributes"></a>Thuộc tính nhiệm vụ  
 Tên nhiệm vụ mô tả công việc cần được hoàn thành. Bạn sử dụng các thuộc tính nhiệm vụ khác nhau để mô tả các yêu cầu lịch trình và bố trí nhân viên cho nhiệm vụ.  
  
### <a name="schedule-attributes"></a>Thuộc tính lịch trình

 - Gán giá trị cho **Số giờ nỗ lực**, **Số nguồn lực**, **Ngày bắt đầu**, **Ngày kết thúc** và **Khoảng thời gian** để xác định lịch trình cho nhiệm vụ. 
 - **Nỗ lực** là ước tính giờ cần để hoàn thành nhiệm vụ.
 - **Số nguồn lực** là ước tính mà người quản lý dự án đặt trong nhiệm vụ để giúp tạo lịch trình tốt nhất có thể. 
 - **Khoảng thời gian** (tính theo ngày) cho biết số ngày làm việc sẽ cần hoàn thành nhiệm vụ.  
  
### <a name="staffing-attributes"></a>Thuộc tính sắp xếp nhân viên

 - **Vai trò**, **Đơn vị tổ chức nguồn lực**, **Số nguồn lực** và **Nguồn lực** mô tả các yêu cầu sắp xếp nhân viên cho nhiệm vụ. 
 - **Vai trò** mô tả loại nguồn lực cần thiết để thực hiện nhiệm vụ. 
 - **Đơn vị tổ chức nguồn lực** biểu thị đơn vị tổ chức mà từ đó nguồn lực phải được sắp xếp nhân viên cho nhiệm vụ đó; điều này cũng tác động đến ước tính chi phí và bán hàng của nhiệm vụ, vì điều này được cân nhắc khi xác định giá bán đơn vị cho nguồn lực. 
 - **Nguồn lực** chứa nguồn lực chung hoặc nguồn lực được đặt tên khi tìm thấy nguồn lực.  
  
## <a name="task-dependencies"></a>Đối tượng phụ thuộc của nhiệm vụ  
 Bạn có thể tạo mối quan hệ trước đó giữa một hoặc nhiều nhiệm vụ trong cấu trúc phân tích công việc. Bạn có thể đặt một hoặc nhiều giá trị cho các trường trước đó về nhiệm vụ để biểu thị nhiệm vụ mà giá trị sẽ phụ thuộc vào. Khi bạn gán một giá trị trước đó cho một nhiệm vụ, nhiệm vụ chỉ có thể bắt đầu khi tất cả các nhiệm vụ trước đó đã hoàn thành. Đặt đối tượng phụ thuộc này vào một nhiệm vụ sẽ dẫn đến tính toán lại ngày bắt đầu theo kế hoạch của nhiệm vụ là kết thúc muộn nhất của tất cả người tiền nhiệm. Tác động liên quan đến người tiền nhiệm đối với lịch trình không bị giới hạn bởi chế độ nhiệm vụ được xác định trên nhiệm vụ.  
  
## <a name="task-mode"></a>Chế độ nhiệm vụ  
 Chế độ nhiệm vụ là một trong những yếu tố quan trọng để xác định việc lên lịch nhiệm vụ nút lá. Có hai chế độ nhiệm vụ cho mỗi nhiệm vụ: chế độ lên lịch tự động và chế độ lên lịch thủ công.  
  
-   **Tự động lên lịch**.   Khi bạn đặt chế độ nhiệm vụ thành Tự động Lên lịch, công cụ lên lịch nhiệm vụ sử dụng quy tắc lên lịch trên các thuộc tính nhiệm vụ sau để xác định lịch trình cho nhiệm vụ:  
  
    -   Người tiền nhiệm  
  
    -   Nỗ lực  
  
    -   Số nguồn lực  
  
    -   Ngày bắt đầu và ngày kết thúc  
  
-   **Quy tắc lên lịch**.   Ngày bắt đầu của một nhiệm vụ nút lá không có người tiền nhiệm sẽ mặc định là ngày bắt đầu lên lịch của dự án. Khoảng thời gian của nhiệm vụ nút lá luôn được tính toán là số ngày làm việc giữa của ngày bắt đầu và ngày kết thúc. Khi một nhiệm vụ được lên lịch tự động, công cụ lên lịch tuân thủ các quy tắc dưới đây:  
  
    -   Ngày bắt đầu và ngày kết thúc của nhiệm vụ luôn phải là ngày làm việc theo lịch lên lịch của dự án  
  
    -   Ngày bắt đầu của nhiệm vụ có người tiền nhiệm sẽ mặc định là ngày kết thúc muộn nhất của người tiền nhiệm  
  
    -   Nỗ lực = Số người * Khoảng thời gian * số giờ trong ngày làm việc tiêu chuẩn của lịch dự án  
  
-   **Lên lịch thủ công**.   Trong một số trường hợp, bạn có thể cần phân biệt với những quy tắc này. Trong những trường hợp này, bạn có thể thiết lập chế độ nhiệm vụ cho nhiệm vụ được lên lịch theo cách thủ công. Điều này sẽ ngăn công cụ lên lịch tính toán giá trị cho các thuộc tính lên lịch khác. Thiết lập người tiền nhiệm về nhiệm vụ luôn luôn ảnh hưởng đến ngày bắt đầu của nhiệm vụ phụ thuộc.  
  
## <a name="create-a-work-breakdown-structure"></a>Tạo cấu trúc phân tích công việc  
  
1.  Đi tới **Project Service > Dự án**.  
  
2.  Bấm vào dự án mà bạn muốn làm việc.  
  
3.  Trong thanh ở đầu màn hình, chọn mũi tên xuống bên cạnh tên dự án, sau đó bấm vào Cấu trúc phân tích công việc.  
  
4.  Để thêm một nhiệm vụ, bấm **Thêm nhiệm vụ**. Điền vào các trường cho nhiệm vụ, sau đó bấm vào **Lưu**.  
  
5.  Tiếp tục thêm nhiệm vụ cho đến khi cấu trúc phân tích công việc của bạn hoàn thành. Trong khi tạo cấu trúc phân tích công việc, bạn có thể làm những điều sau đây để tổ chức các nhiệm vụ của mình:  
  
    -   Chọn nhiệm vụ và bấm vào **Thụt lề** để di chuyển xuống một nhiệm vụ khác hoặc bấm vào Tăng lề để di chuyển lên một cấp độ.  
  
    -   Chọn một nhiệm vụ và bấm vào **Di chuyển lên** hoặc **Di chuyển xuống** để chuyển nhiệm vụ lên hoặc xuống trong danh sách.  
  
    -   Bấm vào **Ẩn Gantt** để ẩn biểu đồ Gantt và bấm vào **Hiển thị Gantt** để hiển thị lại biểu đồ.  
  
    -   Chọn khoảng thời gian khác cho biểu đồ Gantt trong **Thang thời gian**.  
  
6.  Để thêm vai trò bạn đã chỉ định trong cấu trúc phân tích công việc vào thành viên nhóm của dự án, bấm vào **Tạo nhóm dự án**.  
  
7.  Bấm **Lưu** ở góc dưới cùng bên phải của màn hình khi bạn hoàn tất việc thay đổi.  
  
### <a name="see-also"></a>Xem thêm  
 [Hướng dẫn của quản lý dự án](../psa/project-manager-guide.md)
