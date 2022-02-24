---
title: Xác định ước tính doanh thu và chi phí dự án
description: Làm cách nào để xác định ước tính doanh thu và chi phí dự án trong Project Service
author: ruhercul
manager: kfend
ms.prod: ''
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
ms.openlocfilehash: a91e988632d2b2cdebfe7fd17516c5d6886728fc
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148849"
---
# <a name="determine-project-cost-and-revenue-estimates"></a>Xác định ước tính doanh thu và chi phí dự án 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Ước tính dự án cung cấp dạng xem tài chính cho các công việc được ước tính và lên lịch trong cấu trúc phân tích chi tiết công việc của dự án. Dạng xem ước tính cho bạn biết tác động của chi phí và doanh thu với những công việc dự định. Dạng xem ước tính cung cấp công cụ để xem thông tin về một số thứ nguyên được định trước nhằm cho bạn biết về các tác động tài chính của dự án một cách khái quát nhất.  
  
## <a name="cost-and-sales-value-of-the-project"></a>Giá trị chi phí và kinh doanh của dự án  
Bảng giá [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] xác định chi phí và mức tính phí cho các vai trò mà dự án sử dụng. Dựa trên vai trò được liên kết với các nhiệm vụ trong cấu trúc phân tích chi tiết công việc của dự án, bạn có thể xác định tác động của chi phí và doanh thu đến các công việc liên quan.  
  
## <a name="cost-price-defaulting"></a>Đặt mặc định giá vốn  
Mọi dự án đều thuộc về một tổ chức (được thể hiện trong **Đơn vị sở hữu** trong dự án). Biểu giá được liên kết với đơn vị tổ chức sở hữu xác định đơn giá vốn. [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] xác định giá vốn cho các vai trò bằng cách tìm kiếm bộ kết hợp vai trò, đơn vị hoặc đơn vị theo tổ chức trong bảng giá vốn để có giá vốn chính xác cho ngày có hiệu lực trên các đường dự toán.  
  
Nếu sự kết hợp giữa vai trò, đơn vị và đơn vị tổ chức không dẫn đến giá vốn từ biểu giá của đơn vị sở hữu, đơn vị được bỏ qua để tạo điều kiện cho sự kết hợp giữa vai trò và đơn vị tổ chức. Nếu có giá vốn, giá này sẽ được chuyển đổi thành đơn vị bạn đã chọn trên dòng ước tính.  
  
Nếu sự kết hợp giữa vai trò và đơn vị tổ chức không dẫn đến một mức giá vốn, đơn vị tổ chức được bỏ qua để tạo điều kiện cho sự kết hợp giữa vai trò và đơn vị và giá được đặt mặc định sau khi áp dụng bất kỳ hoạt động chuyển đổi nào, nếu cần thiết.  
  
 Nếu không có một mức giá cho vai trò thì giá vốn được đặt mặc định thành 0,00 trên dòng ước tính.  
  
 Tất cả số tiền chi phí trên dòng ước tính chi phí dự án sẽ theo đơn vị tiền tệ của đơn vị tổ chức sở hữu.  
  
## <a name="sales-price-defaulting"></a>Đặt mặc định giá bán  
Biểu giá bán sẽ dựa vào thực thể bán mà dự án được gán đến. Biểu giá bán được liên kết với báo giá hoặc hợp đồng sẽ xác định đơn giá bán. Nếu báo giá hoặc hợp đồng có biểu giá tùy chỉnh, đấy sẽ là biểu giá bán mặc định cho các ước tính dự án. Nếu không có liên kết với các thực thể bán thì biểu giá bán mặc định được định cấu hình trong cài đặt tham số sẽ là biểu giá bán mặc định cho dự án. Mỗi dòng ước tính được liên kết với một đơn vị tổ chức nguồn tài nguyên để chỉ ra đơn vị tổ chức nơi sẽ đặt nguồn tài nguyên để hoàn tất nhiệm vụ. Giá bán cho các vai trò được liên kết được xác định bằng cách tìm kiếm các cách kết hợp giữa vai trò, đơn vị và thiết bị tổ chức nguồn tài nguyên trong biểu giá bán để nhận đúng giá bán cho ngày có hiệu lực trên dòng ước tính.  
  
Nếu sự kết hợp giữa vai trò, đơn vị và đơn vị tổ chức nguồn tài nguyên không đưa ra một mức giá bán từ biểu giá bán, hệ thống sẽ bỏ qua đơn vị và tìm kiếm sự kết hợp giữa vai trò và đơn vị tổ chức nguồn tài nguyên. Nếu thấy giá bán, giá này sẽ được chuyển đổi sang đơn vị bạn đã chọn trên dòng ước tính bán hàng.  
  
Nếu hệ thống không tìm thấy giá cho vai trò thì giá bán phải được đặt mặc định thành 0,00 trên dòng ước tính.  
  
Dạng xem ước tính có dạng xem lưới hiển thị lưới đồng đều gồm các dòng ước tính có đơn vị, tổng chi phí và giá bán.  
  
## <a name="time-phased-view-of-project-estimates"></a>Dạng xem theo giai đoạn thời gian cho ước tính dự án  
Trong dạng xem theo giai đoạn thời gian cho ước tính dự án, dữ liệu ước tính từ dạng xem lưới được xoay theo mặc định theo vai trò và hiển thị bảng tính của các dữ liệu ước tính trên dòng thời gian trong tỷ lệ thời gian đã chọn.  
  
## <a name="effort-estimate-allocation-based-on-task-mode"></a>Phân bổ ước tính nỗ lực dựa trên chế độ nhiệm vụ  
Trong dạng xem theo giai đoạn thời gian, toàn bộ nỗ lực được ước tính cho nhiệm vụ được phân phối bằng cách phân bổ số giờ cố gắng cụ thể cho mỗi khoảng thời gian đơn vị của tỷ lệ thời gian đã chọn. Trong Project Service, chế độ nhiệm vụ xác định cách thức phân bổ nỗ lực trên khoảng thời gian của nhiệm vụ. Hai loại phân bổ là phân bổ đều và phân bổ dựa trên giờ làm việc. 
  
## <a name="work-hours-based-allocation"></a>Phân bổ dựa trên giờ làm việc  
Chế độ Tự động lên lịch nhiệm vụ với một nhiệm vi chi phối số lượng tài nguyên được dự tính trên nhiệm vụ, chúng được ước tính để được tận dụng cho toàn bộ số giờ làm việc mỗi ngày. Chế độ này sẽ áp dụng khi phân bổ nỗ lực bằng cách phân chia trên khoảng thời gian của nhiệm vụ trong dạng xem dựa trên giai đoạn thời gian. Ví dụ: trên một tỷ lệ thời gian 'Ngày', với một nhiệm vụ được ước tính cần hoàn tất bởi một tài nguyên, nhân công được phân bổ mỗi ngày sẽ không vượt quá số giờ làm việc mỗi ngày được xác định trong lịch của dự án. Vì vậy, việc phân bổ nỗ lực luôn đảm bảo rằng các nguồn lực được ước tính để tận dụng cho cả ngày.  
  
## <a name="even-distribution"></a>Phân phối đều  
Chế độ nhiệm vụ được lên lịch theo cách thủ công không tuân theo giờ làm việc, lịch dự án hay số nguồn lực được xác định cho nhiệm vụ. Lịch nhiệm vụ dựa trên mục nhập của người sử dụng. Với các nhiệm vụ như vậy, phân bổ nỗ lực cho mỗi khoảng thời gian đơn vị cho tỷ lệ đã chọn không có bất kỳ yếu tố hạn chế nào. Tổng nỗ lực trên một nhiệm vụ được chia và phân bổ đều cho mỗi khoảng thời gian đơn vị trên tỷ lệ thời gian đã chọn.  
  
Bằng cách này, chế độ nhiệm vụ được xác định cho nhiệm vụ sẽ xác định cách phân phối hoặc phân bổ nỗ lực trên mỗi khoảng thời gian đơn vị trong ước tính theo giai đoạn thời gian.  
  
## <a name="grouping-and-time-phasing-options"></a>Tùy chọn theo giai đoạn thời gian và phân nhóm  
Dạng xem này giúp bạn hiểu về cách phân phối nỗ lực, chi phí và ước tính bán hàn trên cơ sở mỗi ngày, mỗi tuần, mỗi tháng hoặc mỗi năm. Tùy chọn Nhóm theo cho phép thay đổi dữ liệu ước tính dựa trên hai thứ nguyên khác: danh mục và tài nguyên. Trên cả dạng xem lưới và dạng xem theo giai đoạn thời gian, bạn đều có thể chọn các trường cần được hiển thị. Tổng số cho mỗi khối thời gian được hiển thị ở dưới cùng cho biết tổng số nhân công, chi phí và doanh số ước tính cho ngày, tuần, tháng hoặc năm.  
  
Giá vốn và giá bán hàng mặc định có hiệu lực theo ngày. Khi tỷ lệ cho các vai trò thay đổi, dạng xem theo giai đoạn thời gian sẽ rõ ràng hơn khi xem dữ liệu ước tính được thay đổi theo ‘Tài nguyên’ và theo giai đoạn thời gian theo tuần.  
  
## <a name="expense-estimates"></a>Ước tính chi phí  
Bất kỳ chi phí nào phát sinh trong dự án mà không trực tiếp liên quan đến lao động được sử dụng có thể được ghi lại trong ước tính dự án ở dạng xem lưới. Sử dụng tùy chọn **Thêm ước tính chi phí** trong dạng xem lưới, bạn có thể hoàn thành tác vụ này. Có thể ghi lại các ước tính chi phí cho một nhiệm vụ cụ thể hoặc cho toàn bộ dự án. Bạn có thể chọn loại chi phí trên những dòng này và chọn ngày dự kiến phát sinh chi phí dự kiến. Nếu biểu giá bán và giá vốn được liên kết có giá mặc định hoặc tỷ lệ đánh dấu được xác định cho danh mục chi phí, giá đó sẽ được đặt mặc định trên dòng ước tính khi liên kết.  
  
### <a name="see-also"></a>Xem thêm  
 [Hướng dẫn của Quản lý Dự án](../psa/project-manager-guide.md)
