---
title: Cung cấp dự toán công việc cho một dự án trong quá trình bán hàng
description: Làm cách nào để cung cấp ước tính công việc cho dự án trong quy trình bán hàng ở Project Service
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
ms.openlocfilehash: 49ea8327ae34a69eba1585f1b1b4e557fd4eac93
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283574"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a>Cung cấp ước tính công việc cho dự án trong quy trình bán hàng (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Trong quá trình bán hàng, bạn có thể tạo ước tính bán hàng từ đầu với mô tả báo giá. Các chức năng [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] trong [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] cung cấp cách dự toán doanh số một cách khoa học và chính xác hơn bằng cách chia nhỏ mục công việc và kết hợp các thuộc tính có liên quan góp phần vào ước tính cho dự án trong cấu trúc phân tích công việc.  
  
 Sau khi giành được việc bán hàng, bạn có thể sử dụng cấu trúc phân tích công việc có liên quan trong kế hoạch, điều chỉnh khi cần để hoàn thành thành công dự án của bạn.  
  
## <a name="link-a-project-to-a-quote-line"></a>Liên kết dự án với mô tả báo giá  
 Khi tạo một mô tả báo giá dựa trên dự án, bạn có thể tạo một dự án mới từ mô tả báo giá. Sau đó, bạn có thể sử dụng mẫu dự án, là các kế hoạch tiêu chuẩn cấu hình sẵn và ước tính tài chính chung trong tổ chức của bạn hoặc bản sao kế hoạch dự án và ước tính từ dự án trước. Khi bạn tạo một dự án, việc chọn một mẫu dự án sẽ cung cấp cơ sở điều chỉnh kế hoạch dự án, ước tính và yêu cầu vai trò. Bằng cách tạo dự án của bạn từ báo giá, dự án tự động được kết hợp với mô tả báo giá.  
  
## <a name="project-estimate-components"></a>Thành phần ước tính của dự án  
 Cấu trúc phân tích công việc trong một dự án cung cấp cách để phân chia công việc thành các nhiệm vụ, duy trì một hệ thống phân cấp nhiệm vụ và gán ước tính nỗ lực cần thiết để hoàn thành mỗi nhiệm vụ. Bạn cũng có thể kết hợp các vai trò với một nhiệm vụ để chỉ ra một ước tính loại nguồn lực cần thiết để hoàn thành nhiệm vụ và lịch trình.  
  
 Cấu trúc phân tích công việc giúp bạn xác định nỗ lực làm việc và ước tính lịch trình. Theo mặc định, dự án sử dụng bảng giá mặc định mà bạn đã xác định trước đó. Chi phí và giá bán được xác định trong bảng giá giúp quyết định ước tính tài chính cho phân tích công việc của dự án.  
  
 Nếu dự án của bạn được liên kết với một báo giá và báo giá có bảng giá khác với bảng giá mặc định, bảng giá của báo giá được sử dụng cho ước tính tài chính.  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a>Nhập ước tính từ dự án vào báo giá  
 Sau khi có ước tính dự án trong dự án, bạn có thể nhập những ước tính này vào mô tả báo giá:  
  
-   Trong **Chi tiết mô tả báo giá**, bấm vào **Nhập từ ước tính**. 

-   Chọn nhập ước tính dự án được tóm tắt theo loại giao dịch, vai trò hoặc cấp độ nút cấu trúc phân tích công việc.  
  
### <a name="see-also"></a>Xem thêm  
 [Hướng dẫn của Quản lý Dự án](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]