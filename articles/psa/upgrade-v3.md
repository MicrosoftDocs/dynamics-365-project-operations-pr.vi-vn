---
title: Thông tin cần cân nhắc khi nâng cấp - Microsoft Dynamics 365 Project Service Automation phiên bản 2.x hoặc 1.x lên phiên bản 3
description: Chủ đề này cung cấp thông tin về những nội dung cần cân nhắc bạn phải thực hiện khi nâng cấp từ Project Service Automation phiên bản 2.x hoặc 1.x lên phiên bản 3.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 11/13/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 19d6d312c7cedd2d7b9b5649452b85dd24fae761
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087188"
---
# <a name="upgrade-considerations---psa-version-2x-or-1x-to-version-3"></a>Nội dung cần cân nhắc khi nâng cấp - PSA phiên bản 2.x hoặc 1.x lên phiên bản 3
[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="project-service-automation-and-field-service"></a>Project Service Automation và Field Service
Cả Dynamics 365 Project Service Automation và Dynamics 365 Field Service đều dùng giải pháp Universal Resourcing Scheduling (URS) để lập lịch trình nguồn lực. Nếu có cả Project Service Automation và Field Service trong phiên bản của mình, bạn nên lập kế hoạch nâng cấp cả hai giải pháp lên phiên bản mới nhất (phiên bản 3.x cho Project Service Automation, phiên bản 8.x cho Field Service). Thao tác nâng cấp Project Service Automation hoặc Field Service sẽ cài đặt phiên bản URS mới nhất, có nghĩa là có thể xảy ra hành vi không nhất quán nếu cả hai giải pháp Project Service Automation và Field Service trong cùng một phiên bản không được nâng cấp lên phiên bản mới nhất.

## <a name="resource-assignments"></a>Gán nguồn lực
Trong Project Service Automation phiên bản 2 và phiên bản 1, nội dung gán nhiệm vụ được lưu trữ dưới dạng nhiệm vụ con (còn được gọi là nhiệm vụ mô tả) trong **Thực thể nhiệm vụ** và có liên quan gián tiếp đến thực thể **Gán nguồn lực**. Nhiệm vụ mô tả hiển thị trong cửa sổ gán bật lên trên Cấu trúc phân tích công việc (WBS).

![Các nhiệm vụ mô tả trên WBS trong Project Service Automation phiên bản 2 và phiên bản 1](media/upgrade-line-task-01.png)

Trong phiên bản 3 của Project Service Automation, sơ đồ cơ sở của việc gán nguồn lực có thể đặt trước đã thay đổi. Nhiệm vụ dòng không còn dùng nữa và có mối liên hệ trực tiếp 1:1 giữa nhiệm vụ trong **Thực thể nhiệm vụ** và thành viên nhóm trong thực thể **Gán tài nguyên**. Các nhiệm vụ được gán cho một thành viên nhóm dự án hiện được lưu trữ trực tiếp trong thực thể Gán tài nguyên.  

Những thay đổi này ảnh hưởng đến việc nâng cấp bất kỳ dự án hiện có nào có nội dung gán nguồn lực cho nguồn lực có tên có thể đặt và nguồn lực chung cho một nhóm dự án. Chủ đề này cung cấp thông tin cần cân nhắc mà bạn phải xem xét cho dự án của mình khi nâng cấp lên phiên bản 3. 

### <a name="tasks-assigned-to-named-resources"></a>Nhiệm vụ được gán cho các nguồn được đặt tên
Sử dụng thực thể nhiệm vụ cơ bản, các nhiệm vụ trong phiên bản 2 và phiên bản 1 cho phép thành viên nhóm mô tả vai trò chứ không phải là vai trò đã xác định mặc định của họ. Ví dụ: Đặng Ngoan, người theo mặc định được gán vai trò Người quản lý chương trình, có thể được gán cho một nhiệm vụ có vai trò là Nhà phát triển. Trong phiên bản 3, vai trò của một thành viên nhóm được đặt tên luôn là mặc định, cũng như mọi nhiệm vụ mà Đặng Ngoan được gán để sử dụng vai trò mặc định là Người quản lý chương trình của cô.

Nếu bạn đã gán nguồn lực cho một nhiệm vụ ngoài vai trò mặc định của họ trong phiên bản 2 và phiên bản 1, thì khi bạn nâng cấp, nguồn lực có tên sẽ được gán vai trò mặc định cho tất cả các nội dung gán nhiệm vụ, bất kể nội dung gán vai trò trong phiên bản 2. Điều này sẽ dẫn đến sự khác biệt trong tính toán ước tính từ phiên bản 2 hoặc phiên bản 1 đến phiên bản 3 vì nội dung ước tính dựa trên vai trò của nguồn lực này chứ không phải là nội dung gán nhiệm vụ dòng. Ví dụ: trong phiên bản 2, hai nhiệm vụ đã được gán cho Chế Hà. Vai trò trên nhiệm vụ dòng cho nhiệm vụ 1 là Nhà phát triển và cho nhiệm vụ 2 là Người quản lý chương trình. Chế Hà có vai trò mặc định là Người quản lý chương trình.

![Nhiều vai trò được gán cho một nguồn lực.](media/upgrade-multiple-roles-02.png)

Vì vai trò của Nhà phát triển và Người quản lý chương trình là khác nhau, nên chi phí và doanh số ước tính sẽ như sau:

![Chi phí ước tính cho vai trò nguồn lực](media/upggrade-cost-estimates-03.png)

![Doanh số ước tính cho vai trò nguồn lực](media/upgrade-sales-estimates-04.png)

Khi bạn nâng cấp lên phiên bản 3, các nhiệm vụ dòng được thay thế bằng nội dung gán nguồn lực đối với nhiệm vụ của thành viên nhóm nguồn lực có thể đặt. Nội dung gán sẽ sử dụng vai trò mặc định của nguồn lực có thể đặt. Trong đồ họa sau đây, Chế Hà, người có vai trò Người quản lý chương trình, là một nguồn lực.

![Gán nguồn lực](media/resource-assignment-v2-05.png)

Bởi vì các ước tính dựa trên vai trò mặc định của nguồn lực, nên ước tính doanh số và chi phí có thể thay đổi. Lưu ý rằng trong biểu đồ sau đây, bạn không còn thấy vai trò **Nhà phát triển** vì vai trò này hiện được lấy từ vai trò mặc định của nguồn lực có thể đặt.

![Ước tính chi phí cho vai trò mặc định](media/resource-assignment-cost-estimate-06.png)
![Ước tính doanh số cho vai trò mặc định](media/resource-assignment-sales-estimate-07.png)

Sau khi nâng cấp xong, bạn có thể chỉnh sửa vai trò của một thành viên nhóm thành vai trò nào đó không phải là vai trò được gán mặc định. Tuy nhiên, nếu bạn thay đổi vai trò của thành viên nhóm, vai trò đó sẽ được thay đổi trên tất cả các nhiệm vụ được gán vì thành viên nhóm không còn được phép gán nhiều vai trò trong phiên bản 3.

![Cập nhật vai trò nguồn lực](media/resource-role-assignment-08.png)

Điều này cũng đúng đối với các nhiệm vụ dòng được gán nguồn lực có tên khi bạn thay đổi đơn vị tổ chức của nguồn lực từ mặc định thành một đơn vị tổ chức khác. Sau khi nâng cấp xong phiên bản 3, nội dung gán sẽ sử dụng đơn vị tổ chức mặc định của nguồn lực thay vì đơn vị được đặt trong nhiệm vụ dòng.

### <a name="tasks-assigned-to-generic-resources"></a>Nhiệm vụ được gán cho các nguồn lực chung
Trong phiên bản 2 và phiên bản 1, bạn có thể đặt vai trò và đơn vị tổ chức cho một nhiệm vụ, sau đó sử dụng tính năng **Tạo nhóm** để tạo các tài nguyên chung theo thuộc tính được đặt trên nhiệm vụ. Trong phiên bản 3, bạn tạo các thành viên nhóm chung với vai trò và đơn vị tổ chức, sau đó chỉ định các thành viên nhóm cho nhiệm vụ.

Trong phiên bản 2 và phiên bản 1, các dự án có nguồn lực chung có thể ở 2 trạng thái hoặc kết hợp cả hai ở cấp nhiệm vụ. Ví dụ: bạn có thể có các tình huống sau:

- Các nhiệm vụ có vai trò và đơn vị tổ chức được đặt, nhưng chưa tạo nội dung gán nguồn lực liên kết nào.
- Các nhiệm vụ có nội dung gán nguồn lực là thành viên nhóm được chỉ định bằng cách tạo nguồn lực chung bằng tính năng **Tạo nhóm**.

Trước khi bạn bắt đầu nâng cấp, bạn nên tạo lại nhóm cho từng dự án có nhiệm vụ được gán nguồn lực chung hoặc chưa tạo quy trình nhóm để chạy.

Đối với các nhiệm vụ được gán cho thành viên nhóm chung được tạo bằng tính năng **Tạo nhóm** , việc nâng cấp sẽ rời khỏi nguồn lực chung của nhóm và không gán cho thành viên nhóm chung đó. Bạn nên tạo yêu cầu nguồn lực cho thành viên nhóm chung sau khi nâng cấp nhưng trước khi bạn đặt hoặc gửi yêu cầu nguồn lực. Điều này sẽ bảo vệ mọi nội dung gán đơn vị tổ chức cho thành viên nhóm chung khác với đơn vị tổ chức hợp đồng của dự án.

Ví dụ: trong dự án Project Z, đơn vị tổ chức hợp đồng là Contoso Hoa Kỳ. Trong kế hoạch dự án, các nhiệm vụ kiểm tra trong giai đoạn thực hiện đã được chỉ định vai trò Tư vấn kỹ thuật và đơn vị tổ chức đã chỉ định là Contoso India.

![Chỉ định tổ chức trong giai đoạn thực hiện](media/org-unit-assignment-09.png)

Sau giai đoạn thực hiện, nhiệm vụ kiểm tra tích hợp được gán cho vai trò Tư vấn kỹ thuật, nhưng tổ chức được đặt thành Contoso Hoa Kỳ.  

![Chỉ định tổ chức nhiệm vụ kiểm tra tích hợp](media/org-unit-generate-team-10.png)

Khi bạn tạo một nhóm cho dự án, hai thành viên nhóm chung sẽ được tạo do các đơn vị tổ chức khác nhau trong tác vụ. Tư vấn kỹ thuật 1 sẽ được gán các nhiệm vụ của Contoso Ấn Độ và Tư vấn kỹ thuật 2 sẽ có nhiệm vụ của Contoso Hoa Kỳ.  

![Thành viên nhóm chung đã tạo](media/org-unit-assignments-multiple-resources-11.png)

> [!NOTE]
> Trong Project Service Automation phiên bản 2 và phiên bản 1, thành viên nhóm không duy trì đơn vị tổ chức, được duy trì trên nhiệm vụ mô tả.

![Các nhiệm vụ mô tả phiên bản 2 và phiên bản 1 trong Project Service Automation](media/line-tasks-12.png)

Bạn có thể xem đơn vị tổ chức trên dạng xem ước tính. 

![Ước tính đơn vị tổ chức](media/org-unit-estimates-view-13.png)
 
Khi nâng cấp xong, đơn vị tổ chức trên nhiệm vụ dòng tương ứng với thành viên nhóm chung được thêm vào thành viên nhóm chung và tác vụ dòng bị xóa. Do đó, trước khi nâng cấp, bạn tạo hoặc tạo lại nhóm trên mỗi dự án chứa các nguồn lực chung.

Đối với các nhiệm vụ được chỉ định vai trò với đơn vị tổ chức khác với đơn vị tổ chức của dự án hợp đồng, và nhóm chưa được tạo, việc nâng cấp sẽ tạo một thành viên nhóm chung cho vai trò, nhưng sẽ sử dụng đơn vị hợp đồng của dự án cho đơn vị tổ chức của thành viên dự án. Quay lại ví dụ với Dự án Z, điều này nghĩa là đơn vị tổ chức hợp đồng Contoso Hoa Kỳ và các nhiệm vụ kiểm tra kế hoạch dự án trong giai đoạn Thực hiển đã được gán vai trò Tư vấn kỹ thuật với đơn vị tổ chức được gán cho Contoso Ấn Độ. Nhiệm vụ kiểm tra tích hợp được hoàn thành sau giai đoạn Thực hiện đã được gán vai trò Tư vấn kỹ thuật. Đơn vị tổ chức là Contoso Hoa Kỳ và nhóm chưa được tạo. Việc nâng cấp sẽ tạo một thành viên nhóm chung, Một nhà tư vấn kỹ thuật có giờ được chỉ định của tất cả ba nhiệm vụ và đơn vị tổ chức của Contoso Hoa Kỳ, đơn vị của dự án ký kết hợp đồng.   
 
Thay đổi mặc định của tổ chức tài chính khác nhau trên các thành viên nhóm được tạo ra là lý do chúng tôi khuyên bạn tạo hoặc tạo lại nhóm trên mỗi dự án có nguồn lực chung trước khi nâng cấp để gán đơn vị không bị mất.

