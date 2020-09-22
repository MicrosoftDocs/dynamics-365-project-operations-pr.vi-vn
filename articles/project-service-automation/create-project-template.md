---
title: Tạo mẫu dự án
description: Làm cách nào để tạo mẫu dự án trong Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: ba15d6d5-a43b-456a-9488-db6e92023fa1
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 50e12d65d5ed957565485413490b8d9f0e2f47ab
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 03/24/2020
ms.locfileid: "3757015"
---
# <a name="create-a-project-template-project-service"></a>Tạo mẫu dự án (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Mẫu dự án tiết kiệm thời gian cho bạn nếu công ty của bạn thường xuyên đấu thầu các loại dự án giống nhau. Các mẫu này cung cấp một bộ tiêu chuẩn cho vai trò và thời gian ước tính cho một loại dự án. Giám đốc khách hàng và giám đốc dự án có thể tạo các dự án dựa trên mẫu dự án hoặc họ có thể sao chép mẫu và tự tạo mẫu riêng.  
  
## <a name="components-of-project-template"></a>Các thành phần của mẫu dự án
 Một mẫu dự án bao gồm ba thành phần:  
  
- **Cấu trúc phân tích công việc**: Cấu trúc phân tích công việc trong một mẫu dự án có tập hợp các yếu tố giống như trong dự án. Bạn có thể tạo một hệ thống cấp bậc nhiệm vụ, liên kết vai trò với nhiệm vụ, xác định các thuộc tính lịch trình, thiết lập quan hệ phụ thuộc và xem tất cả dữ liệu trong Gantt. Cấu trúc phân tích công việc trong mẫu dự án cũng hỗ trợ chế độ nhiệm vụ cho mỗi nhiệm vụ. Tạo lịch trình công việc cho mẫu dự án và dự án là giống nhau.  
  
- **Dự toán dự án**: Dự toán dự án trong các mẫu hoạt động giống như trong các dự án, ngoại trừ bảng giá để đặt mặc định chi phí và giá bán luôn là chi phí và bảng giá bán mặc định được xác định trong tham số [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Các tính năng còn lại giống với các tính năng trong một dự án.  
  
- **Hình thành nhóm dự án**: Khi hình thành nhóm dự án cho mẫu dự án, bạn có thể đặt lịch một nguồn lực được nêu tên trong một mẫu. Bạn có thể sử dụng **Tạo Nhóm Dự án** trong cấu trúc phân tích công việc để tạo ra một tập hợp các nguồn lực chung. Bạn cũng có thể chỉ định các kỹ năng và mức độ thành thạo cần thiết cho nguồn lực chung. Bạn không thể thay thế nguồn lực chung bằng nguồn lực có thể đặt lịch trong mẫu dự án.  
  
## <a name="create-a-project-from-a-template"></a>Tạo dự án từ mẫu  
 Bạn có thể tạo một dự án từ mẫu theo các cách sau đây:  
  
-   Khi tạo dự án từ báo giá, bạn có thể chọn một mẫu dự án trong biểu mẫu tạo nhanh dự án.  
  
-   Khi tạo một dự án bằng cách bấm vào **Dự án Mới**, biểu mẫu dự án sẽ hiển thị trước khi bạn lưu bản ghi. Từ đây, bạn có thể bấm vào trường **Chọn một mẫu** để chọn từ danh sách các mẫu dự án được xác định trước trong tổ chức của bạn.  
  
-   Bấm vào **Tạo dự án từ mẫu** trên trang **Mẫu Dự án** để tạo dự án từ mẫu.  
  
## <a name="copying-components-of-a-template-to-a-project"></a>Sao chép các thành phần của một mẫu vào dự án  
 Khi sao chép các thành phần của mẫu vào dự án, bạn cần lưu ý một số nội dung sau.  
  
 **Sao chép một cấu trúc phân tích công việc**: Khi sao chép cấu trúc phân tích công việc từ một mẫu dự án, nếu dự án có một lịch dự án khác với mẫu, thì giờ làm việc từ lịch của dự án sẽ được áp dụng cho lịch trình công việc. Điều này điều chỉnh lịch trình về lịch dự án được hỗ trợ. Tương tự như vậy, nhiệm vụ đầu tiên trên cấu trúc phân tích công việc sẽ lấy ngày bắt đầu của dự án, do đó, phần còn lại của lịch trình hệ thống cấp bậc nhiệm vụ được cập nhật dựa trên khoảng thời gian và thành phần phụ thuộc được chỉ ra trong cấu trúc phân tích công việc của mẫu.  
  
 **Sao chép dự toán dự án**: Khi bạn sao chép giữa các dòng dự toán của dự án, bảng giá được cập nhật dựa trên đơn vị sở hữu của dự án đối với bảng giá vốn và khách hàng đối với bảng giá bán. Chi phí sản xuất và giá bán được xác định từ các bảng giá này trên các dự án được liên kết với thực thể bán hàng.  
  
 **Sao chép một nhóm dự án**: Khi bạn sao chép nhóm dự án từ mẫu sang một dự án, các nguồn lực chung được sao chép cùng với các kỹ năng và mức độ thành thạo được xác định trong mẫu. Việc phân công nguồn lực chung cũng được duy trì như trong mẫu dự án.  
  
### <a name="see-also"></a>Xem thêm  
 [Hướng dẫn của Quản lý Dự án](../project-service/project-manager-guide.md)
