---
title: Tạo mẫu dự án
description: Làm cách nào để tạo mẫu dự án trong Project Service
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 07/19/2022
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
ms.openlocfilehash: 8159e0390441e5029f9beb0228cffcbc4d683479
ms.sourcegitcommit: 278740b352f1ed9618ee5c79597c8f449984d6f4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 07/19/2022
ms.locfileid: "9177452"
---
# <a name="create-a-project-template-project-service"></a>Tạo mẫu dự án (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Mẫu dự án tiết kiệm thời gian cho bạn nếu công ty của bạn thường xuyên đấu thầu các loại dự án giống nhau. Các mẫu này cung cấp một bộ tiêu chuẩn cho vai trò và thời gian ước tính cho một loại dự án. Giám đốc khách hàng và giám đốc dự án có thể tạo các dự án dựa trên mẫu dự án hoặc họ có thể sao chép mẫu và tự tạo mẫu riêng.  
  
## <a name="components-of-project-template"></a>Các thành phần của mẫu dự án
 Một mẫu dự án bao gồm ba thành phần:  
  
- **Cấu trúc phân tích công việc**: Cấu trúc phân tích công việc trong một mẫu dự án có tập hợp các yếu tố giống như trong dự án. Bạn có thể tạo hệ thống phân cấp nhiệm vụ, liên kết các vai trò với nhiệm vụ, xác định các thuộc tính lịch trình, đặt các phần phụ thuộc và xem tất cả dữ liệu trong Gantt. Cấu trúc phân tích công việc trong các mẫu dự án cũng hỗ trợ các chế độ tác vụ cho từng tác vụ. Không có sự khác biệt giữa mẫu dự án và dự án khi tạo lịch trình làm việc.  
  
- **Dự toán dự án**: Dự toán dự án trong các mẫu hoạt động giống như trong các dự án, ngoại trừ bảng giá để đặt mặc định chi phí và giá bán luôn là chi phí và bảng giá bán mặc định được xác định trong tham số [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Các tính năng còn lại giống với các tính năng trong một dự án.  
  
- **Hình thành nhóm dự án**: Khi hình thành nhóm dự án cho mẫu dự án, bạn có thể đặt lịch một nguồn lực được nêu tên trong một mẫu. Bạn có thể sử dụng **Tạo Nhóm Dự án** trong cấu trúc phân tích công việc để tạo ra một tập hợp các nguồn lực chung. Bạn cũng có thể chỉ định các kỹ năng và mức độ thành thạo cần thiết cho nguồn lực chung. Bạn không thể thay thế nguồn lực chung bằng nguồn lực có thể đặt lịch trong mẫu dự án.  

## <a name="create-a-project-template-from-an-existing-project"></a>Tạo một mẫu dự án từ một dự án hiện có
Bạn có thể tạo một mẫu dự án từ một dự án theo những cách sau:

- **Cấu trúc phân chia công việc** : Một cấu trúc phân tích công việc trong một mẫu có nguồn gốc từ một dự án sẽ sao chép tất cả các nhiệm vụ và phần phụ thuộc. Các nhiệm vụ được tạo sẽ dựa trên các thành viên nhóm chung được thêm vào nhóm dự án khi mẫu dự án được tạo.
- **Dự toán dự án** : Khi một mẫu dự án được tạo từ một dự án hiện có, các ước tính từ dự án nguồn sẽ được sao chép vào mẫu dự án.
- **Thành viên nhóm dự án** : Khi một mẫu được tạo từ một dự án hiện có, tất cả các thành viên trong nhóm được đặt tên sẽ được thay thế bằng tài nguyên chung của tổ chức. Tất cả các tên vị trí và vai trò được duy trì.

## <a name="create-a-project-from-a-template"></a>Tạo dự án từ mẫu  
 Bạn có thể tạo một dự án từ một mẫu theo những cách sau:  
  
-   Khi tạo dự án từ báo giá, bạn có thể chọn một mẫu dự án trong biểu mẫu tạo nhanh dự án.  
  
-   Khi tạo một dự án bằng cách bấm vào **Dự án Mới**, biểu mẫu dự án sẽ hiển thị trước khi bạn lưu bản ghi. Từ đây, bạn có thể bấm vào trường **Chọn một mẫu** để chọn từ danh sách các mẫu dự án được xác định trước trong tổ chức của bạn.  
  
-   Bấm vào **Tạo dự án từ mẫu** trên trang **Mẫu Dự án** để tạo dự án từ mẫu.  
  
## <a name="copying-components-of-a-template-to-a-project"></a>Sao chép các thành phần của một mẫu vào dự án  
 Khi sao chép các thành phần của mẫu vào dự án, bạn cần lưu ý một số nội dung sau.  
  
 **Sao chép một cấu trúc phân tích công việc**: Khi sao chép cấu trúc phân tích công việc từ một mẫu dự án, nếu dự án có một lịch dự án khác với mẫu, thì giờ làm việc từ lịch của dự án sẽ được áp dụng cho lịch trình công việc. Điều này điều chỉnh lịch trình về lịch dự án được hỗ trợ. Tương tự như vậy, nhiệm vụ đầu tiên trên cấu trúc phân tích công việc sẽ lấy ngày bắt đầu của dự án, do đó, phần còn lại của lịch trình hệ thống cấp bậc nhiệm vụ được cập nhật dựa trên khoảng thời gian và thành phần phụ thuộc được chỉ ra trong cấu trúc phân tích công việc của mẫu.  
  
 **Sao chép dự toán dự án**: Khi bạn sao chép giữa các dòng dự toán của dự án, bảng giá được cập nhật dựa trên đơn vị sở hữu của dự án đối với bảng giá vốn và khách hàng đối với bảng giá bán. Chi phí sản xuất và giá bán được xác định từ các bảng giá này trên các dự án được liên kết với thực thể bán hàng.  
  
 **Sao chép một nhóm dự án**: Khi bạn sao chép nhóm dự án từ mẫu sang một dự án, các nguồn lực chung được sao chép cùng với các kỹ năng và mức độ thành thạo được xác định trong mẫu. Việc phân công nguồn lực chung cũng được duy trì như trong mẫu dự án.  
  
### <a name="see-also"></a>Xem thêm  
 [Hướng dẫn của Quản lý Dự án](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
