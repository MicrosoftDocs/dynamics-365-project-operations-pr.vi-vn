---
title: Tính năng mới hoặc đã thay đổi trong Project Service Automation phiên bản 3
description: Chủ đề này cung cấp thông tin về tính năng mới và đã thay đổi trong Project Service Automation phiên bản 3.
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
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
ms.openlocfilehash: 15925cb88cc413f9a23a25e89ddd29668e9171de
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581678"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3"></a>Tính năng mới hoặc đã thay đổi trong Project Service Automation phiên bản 3

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]



Chủ đề này cung cấp thông tin về các thay đổi đối với giao diện người dùng (UI), chức năng và thuật ngữ trong Project Service Automation giữa phiên bản 2 hoặc phiên bản 1 và phiên bản 3.

## <a name="project-scheduling"></a>Lên lịch dự án
Lịch trình dự án, còn được gọi là Cấu trúc phân tích công việc (WBS) trong các phiên bản trước, đã được đổi tên thành Lịch trình và có thể truy cập bằng cách bấm vào tab **Lịch trình**. 

![Lịch trình dự án.](media/psa-schedule-01.png)

Lịch trình hiện có một giao diện tương tác mới vừa hiện đại vừa dễ tiếp cận. Tuy nhiên, công cụ lập lịch trình Project Service Automation cơ bản không thay đổi. Các nút điều khiển trong ruy băng lưới lịch trình cho phép bạn tương tác với lịch trình, tương tự như phiên bản Project Service Automation trước. Các thay đổi bổ sung với lịch trình bao gồm:

- **Biểu đồ Gantt** - Biểu đồ Gantt không còn xuất hiện nữa. Tính năng trực quan hóa Gannt mới sẽ trở lại trong bản cập nhật sau này.
- **Tiêu đề cột** - Bạn có thể ẩn các tiêu đề cột trong lưới bằng cách nhấp vào chỉ báo xuống dưới bên cạnh tiêu đề cột. 
- **Cột** - Bạn có thể hiển thị các cột bị ẩn bằng cách bấm vào **Thêm cột**. 
- **Loại giao dịch** - Tính năng tra cứu **Loại giao dịch** đã được thêm vào lưới lịch trình và được hiển thị theo mặc định. 
 
## <a name="project-templates"></a>Mẫu dự án
Các thay đổi sau đã được thực hiện đối với chức năng mẫu dự án.

### <a name="create-a-project-template"></a>Tạo mẫu dự án 
Bạn có thể tạo mẫu dự án trong phiên bản 3 tương tự như phiên bản Project Service Automation trước. Mẫu này chỉ có thể chứa một lịch trình và lịch trình có thể bao gồm nhiệm vụ, nhưng không bắt buộc. Nếu lịch trình không có nhiệm vụ, nhiệm vụ có thể chỉ dành co nguồn lực chung. Bạn có thể tạo yêu cầu nguồn lực cho các nguồn lực chung, nhưng không thể đặt với các nguồn lực thực tế trong mẫu. Bạn không thể đặt một nguồn lực thực cho một nhóm trong mẫu. 

### <a name="create-a-template-from-an-existing-template"></a>Tạo mẫu từ mẫu hiện có
Khi bạn tạo một mẫu dự án mới từ một mẫu hiện có trong Project Service Automation phiên bản 3, tình huống sau sẽ xảy ra: 

- Lịch trình của dự án nguồn lực được sao chép vào mẫu. 
- Các nguồn lực chung được sao chép vào nhóm và mọi nhiệm vụ của nguồn lực chung được sao chép vào đó. Các yêu cầu cho nguồn lực chung không được sao chép. 

### <a name="create-a-template-from-an-existing-project"></a>Tạo mẫu từ dự án hiện có
Khi bạn tạo mẫu dự án mới từ dự án hiện có, tình huống sau sẽ xảy ra: 

- Lịch trình của dự án nguồn lực được sao chép vào mẫu. 
- Các nguồn lực chung được sao chép vào nhóm và mọi nhiệm vụ của nguồn lực chung được giữ nguyên. Các yêu cầu cho nguồn lực chung không được sao chép.    
- Các nguồn lực có tên, cả đã chỉ định lẫn chưa chỉ định, đều bị xóa khỏi nhóm và được thay thế bằng nguồn lực chung.
- Nếu xuất hiện, thông tin dự án sẽ bị xóa. 
- Nếu xuất hiện, tham chiếu đến báo giá và hợp đồng sẽ bị xóa. 

### <a name="create-a-project-from-a-template"></a>Tạo dự án từ mẫu
Khi bạn tạo một mẫu dự án mới trong Project Service Automation phiên bản 3, tình huống sau sẽ xảy ra:

- Lịch trình, nhóm và nhiệm vụ được sao chép vào dự án mới.   
- Ngày bắt đầu là ngày sao chép hoặc ngày do người dùng chọn.   
- Đối với bất kỳ thành viên nào của nhóm chung có các yêu cầu nguồn lực trong mẫu, các yêu cầu này không được sao chép hoặc tạo tự động. Bạn cần phải tạo chúng. 

## <a name="copy-a-project"></a>Sao chép dự án
Khi bạn sao chép một dự án trong Project Service Automation phiên bản 3, tình huống sau sẽ xảy ra: 

- Ngày bắt đầu ước tính được sao chép nhưng có thể thay đổi.  
- Lịch trình và nhiệm vụ dự án được sao chép. 
- Các nguồn lực chung và nhiệm vụ của họ được sao chép. Các yêu cầu về nguồn lực cho nguồn lực chung không được sao chép. Bạn cần phải tạo lại chúng. 
- Các nguồn lực thực và nhiệm vụ của họ không được sao chép. Thay vào đó, chúng được thay thế bằng nguồn lực chung. 
- Mục thực tế không được sao chép vào dự án mới. 

## <a name="move-a-scheduled-project"></a>Di chuyển dự án đã lên lịch
Khi bạn di chuyển lịch trình của một dự án hiện có, tình huống sau sẽ xảy ra: 

- Các ngày của nhiệm vụ tự động được di chuyển để tương ứng với khoảng thời gian di chuyển. 
- Nguồn lực nói chung được chỉ định sẽ giữ nguyên nội dung chỉ định.   
- Nếu các nguồn lực được tạo trước khi dự án di chuyển, thì các yêu cầu cho nguồn lực chung sẽ vẫn giữ nguyên và không được tạo lại tự động. Bạn sẽ cần tạo lại chúng để phản ánh các nội dung chỉ định mới do di chuyển tác vụ. 
- Nhiệm vụ của các nguồn lực thực sẽ thay đổi cho phù hợp với việc chuyển ngày tác vụ. Nội dung đặt các nguồn lực thực không thay đổi. Bạn cần sửa đổi nội dung đặt qua dạng xem điều hòa. 
- Các nguồn lực của nhóm có nội dung đặt nhưng không phải là nhiệm vụ sẽ không thay đổi. 
- Mục thực tế không di chuyển. 

## <a name="estimates"></a>Ước tính
Ước tính đã được chia thành hai tab **Nhiệm vụ nguồn lực** và **Ước tính**. Tab **Chỉ định nguồn lực** chứa các ước tính về nguồn lực và cho thấy các nội dung chỉ định nguồn lực của các nhiệm vụ trong dạng xem theo theo thời gian. Bạn có thể chỉnh sửa ước tính dựa trên những gì công cụ lên lịch đã tạo.

![Tab Gán nguồn lực hiển thị các ước tính về nỗ lực và nội dung gán nguồn lực cho nhiệm vụ.](media/resource-assignments-tab-02.png)

Tab **Ước tính** hiển thị chi phí và doanh số cho các nhiệm vụ của nguồn lực. Các số liệu đều ở dạng chỉ đọc. Cách định giá chi phí và doanh số hiện phát triển từ nhiệm vụ của thành viên nhóm trên lịch trình. Điều này nghĩa là nếu bạn có một nhiệm vụ mà không có chỉ định, nhiệm vụ đó sẽ hiển thị bên dưới nhóm chưa chỉ định. Điều này cũng có nghĩa là nếu không có **vai trò**, thông số định giá mặc định, thì không có chi phí hay doanh số ước tính nếu bạn có khách hàng hoặc hợp đồng/báo giá liên kết với dự án. 

![Tab Ước tính hiển thị chi phí và doanh số.](media/estimates-tab-03.png)
  
Danh mục cũng được hỗ trợ đối với các nhiệm vụ trong dạng xem lịch trình. Việc nhóm theo danh mục trên dạng xem ước tính dựa trên thời gian sẽ mang lại trải nghiệm tốt hơn, đặc biệt là khi bạn cũng có ước tính chi phí trong dự án. Ước tính chi phí được nhập qua lưới trên tab riêng. 

Có thể nhập ước tính chi phí vào lưới trên tab **Ước tính chi phí**. 

![Tab Ước tính chi phí hiển thị lưới ước tính chi phí.](media/expense-estimates-tab-04.png)

## <a name="resource-management"></a>Quản lý nguồn lực
Trong Project Service Automation phiên bản 3, với UI ứng dụng hợp nhất mới và các thay đổi trong mối quan hệ giữa nhiệm vụ và nội dung đặt trước, việc chia ca một dự án có các nguồn lực chung hoặc thực tế đã thay đổi đáng kể so với phiên bản 2 và phiên bản 1. Tuy nhiên, các khái niệm nguồn lực có thể đặt, cả **thực** và **chung** đều giữ nguyên, giống như thành viên nhóm, yêu cầu, nhiệm vụ và đăng ký.   

![Sử dụng bộ chọn nguồn lực.](media/resource-management-05.png)

### <a name="assign-a-real-bookable-resource"></a>Chỉ định nguồn lực thực có thể đặt 
Trong Project Service Automation phiên bản 3, việc đặt chỗ và phân công nhiệm vụ không được đan xen chặt chẽ như trong các phiên bản trước của Project Service Automation. Bạn có thể sử dụng lưới của nhóm để đặt một thành viên nhóm **thực**, tương tự như trong thị trường.

Sử dụng bộ chọn tài nguyên trên lịch trình, bạn có thể chọn thành viên nhóm được tạo trong dạng xem nhóm rồi chỉ định nhiệm vụ cho họ. Bạn có thể tiếp tục chỉ định nhiệm vụ cho họ, thậm chí quá cả nội dung đặt của họ. Sử dụng tab **Điều hòa** để điều hòa các thành viên nhóm khác nhau về nhiệm vụ và nội dung đặt.

Bộ chọn nguồn lực sẽ hiển thị thành viên nhóm cho dự án. Bạn cũng có thể sử dụng bộ chọn nguồn lực để tìm kiếm và xem các nguồn lực có thể đặt khác không thuộc nhóm dự án. Bạn cũng có thể chỉ định nhiệm vụ cho họ và họ sẽ trở thành một phần trong nhóm dự án. Bạn cần đặt họ bằng cách sử dụng tab **Bảng lịch trình** hoặc **Điều hòa**.

### <a name="assign-a-generic-bookable-resource-on-a-task-and-project-team-and-then-fulfill-with-a-real-resource-via-schedule-board"></a>Chỉ định nguồn lực chung có thể đặt cho một nhiệm vụ và nhóm dự án, sau đó thực hiện với nguồn lực thực qua Bảng lịch trình 
Trong Project Service Automation phiên bản 3, chức năng tạo nhóm không được sử dụng cho nguồn lực chung. Thay vào đó, bạn có thể tạo và chỉ định trực tiếp nguồn lực chung từ lịch trình bằng cách nhập tên vị trí của nguồn lực chung trong ô nguồn lực của lịch trình. Hoặc, bạn có thể chọn biểu tượng nguồn lực trong ô rồi sử dụng bộ chọn nguồn lực để nhập tên của nguồn lực chung mà mình muốn tạo. Điều này sẽ mở một ngăn tạo nhanh cho phép bạn đặt vai trò và đơn vị tổ chức của thành viên nhóm nguồn lực chung. Sau khi bạn tạo nguồn lực, nguồn lực sẽ được chỉ định một nhiệm vụ và bạn có thể tiếp tục chỉ định nguồn lực chung đó cho các nhiệm vụ khác trong lịch trình.    
 
Khi bạn đã chỉ định các nguồn lực cho tất cả các nhiệm vụ phù hợp, bạn có thể tạo một yêu cầu nguồn lực rồi sau đó thực hiện trực tiếp yêu cầu bằng cách đặt với **Bảng lịch trình** hoặc gửi yêu cầu nguồn lực. Bạn cũng có thể thêm trực tiếp nguồn lực chung vào lưới thành viên nhóm. 

Các nguồn lực chung được thêm vào nhóm dự án không có yêu cầu về nguồn lực và có ngày bắt đầu/kết thúc của dự án cho đến khi yêu cầu nguồn lực được tạo ra. Để tạo yêu cầu, hãy chọn nguồn lực chung rồi bấm vào **Tạo**. Liên kết yêu cầu bây giờ sẽ hiển thị và các giờ yêu cầu sẽ được điền sẵn bằng các giờ đã chỉ định. Bạn có thể bấm vào liên kết để mở và cập nhật yêu cầu.
  
Khi một nguồn lực có tên đã đặt trước xong và thực hiện đầy đủ, thì nguồn lực chung sẽ được thay thế bằng nguồn lực có tên và nhiệm vụ trên lịch trình sẽ được cập nhật bằng nguồn lực có tên. 

Các nguồn lực đề xuất cho các yêu cầu hiện được lưu trên một tab thay vì một phần riêng.

### <a name="multiple-named-resources-fulfilling-a-generic-resource"></a>Nhiều nguồn lực có tên đáp ứng một nguồn lực chung
Khi một yêu cầu được thực hiện với nhiều nguồn lực, thì nguồn lực chung vẫn còn nguyên trên nhóm và được chỉ định nhiệm vụ. Các thành viên nhóm có tên được đặt trước không được chỉ định là một phần của vị trí. Người quản lý dự án có thể chỉ định công việc khi cần cho nguồn lực thực.  Dạng xem **Điều hòa** cung cấp phân tích về các nội dung đặt trước cho nhiều nguồn lực với nhiều nhiệm vụ. Điều này không được thực hiện tự động vì trong những tình huống phức tạp hơn, chẳng hạn như khi bạn cần giả định một nhóm nhiệm vụ tạo thành yêu cầu, ý định về cách người quản lý dự án muốn chỉ định. Vì hệ thống không thể hiểu được ý định, nên các giả định có thể sẽ khác như ý định và có thể xảy ra kết quả không chính xác hoặc không dự đoán được. Kết quả có thể dự đoán là nguồn lực chung vẫn được chỉ định cho đến khi người quản lý dự án tự do chỉ định nguồn lực bằng dạng xem **Điều hòa**.

### <a name="reconciliation"></a>Điều hòa
Tab **Điều hòa** hiển thị nội dung đặt trước và tất cả nhiệm vụ cho từng thành viên nhóm dự án. Chế độ xem này hiển thị số giờ trong ô, có thể đại diện các thời điểm từ tháng đến ngày. Dạng xem này cho phép người quản lý dự án điều hòa nội dung đặt trước cho thành viên dự án và nội dung chỉ định của họ cho nhóm dự án. Điều này hữu ích vì nội dung đặt trước và chỉ định nhiệm vụ không đi liền với nhau, nhằm linh hoạt hơn khi lên kế hoạch dự án. 

![Tab Điều hòa hiển thị nội dung đặt trước và nhiệm vụ cho các thành viên nhóm dự án.](media/resource-reconciliation-tab-06.png)

Đối với từng nguồn lực, dạng xem này lại khác nhau giữa nội dung đặt trước cho thành viên nhóm và bảng phân công nhiệm vụ của họ, đồng thời cho thấy hai điểm khác biệt sau có thể xuất hiện giữa nội dung đặt trước và nhiệm vụ trong dự án: 

- **Thiếu đăng ký** - Tình huống thiếu đăng ký có thể xuất hiện khi một nguồn lực có nhiều nhiệm vụ hơn đăng ký. Vì chưa được đặt trước, người quản lý dự án có thể khắc phục điều này bằng cách mở rộng đăng ký cho nguồn lực để bù đắp sự cho sự thiếu hụt. 
- **Vượt quá đăng ký** - Vượt quá đăng ký xảy ra khi nguồn lực đã được đặt cho một dự án nhưng chưa được chỉ định các nhiệm vụ.  Điều này có thể lặp lại chấp nhận được, chẳng hạn như nếu một nguồn lực được đặt trước khi chỉ định nhiệm vụ. Tuy nhiên, trong các trường hợp khác, nguồn lực có thể không được lên kế hoạch chỉ định, và người quản lý dự án nên xem xét hủy đăng ký của nguồn lực để nguồn lực đó được sử dụng cho một dự án khác. 

Khi bạn có các nhiệm vụ cho một nguồn lực mà không đặt trước (thiếu đăng ký), bạn có thể chọn mục thiếu đăng ký tổng hợp và bấm vào **Mở rộng đăng ký**. Tại đây, bạn có thể xem thông tin đặt trước cần thiết để giải quyết sự thiếu hụt nguồn lực và tình hình của nguồn lực. 
 
## <a name="time-and-expense"></a>Thời gian và chi phí
Phần này cung cấp thông tin về thay đổi đối với thời gian, chi phí và hoạt động phê duyệt trong phiên bản 3 của Project Service Automation. Nằm trong giải pháp Dynamics 365 Project Service Automation, tính năng **Mục nhập thời gian** đã được làm mới để sử dụng khung Giao diện hợp nhất. Điều này mang lại một giao diện người dùng nhất quán, thống nhất và tuân theo các nguyên tắc thiết kế phản hồi để tối ưu hóa trải nghiệm xem trên mọi kích thước màn hình hoặc thiết bị. 

### <a name="landing-page"></a>Trang đích
Trải nghiệm mục nhập thời gian tùy chỉnh không thể mở rộng đã không được dùng nữa trong phiên bản 3. Thay vào đó, hiện có một trải nghiệm lưới tự nhiên có thể mở rộng và truy cập. Bạn có thể truy cập chức năng mục nhập thời gian bằng cách sử dụng sơ đồ trang web ở bên trái. Với thay đổi này, bạn sẽ không thể nhập thời gian cho một tuần vào cùng một thời điểm nữa. Thay vào đó, bạn cần tạo một mục nhập thời gian cho từng ngày trong lưới. Sau khi một vài mục nhập thời gian đã được tạo, người dùng có thể tạo hàng loạt mục nhập thời gian bằng chức năng **Sao chép** được giải thích ở phần sau của chủ đề này. 

![Trang đích mục nhập thời gian.](media/time-entry-landing-page-07.png)
 
### <a name="create-new-time-entries"></a>Tạo mục nhập thời gian mới 
Bấm vào **Mới** trong ruy băng để mở trang tạo nhanh cho mục nhập thời gian khi bạn nhập khoảng thời gian theo phút, giờ hoặc ngày. Để làm điều này, chỉ cần bắt đầu nhập giờ, tháng hoặc ngày cùng với số lượng.  

![Tạo nhanh mục nhập thời gian.](media/quick-create-time-entry-08.png)

Các trường tra cứu được dạng xem hệ thống hỗ trợ. Ví dụ: sau khi bạn nhập thông tin dự án, trường **Nhiệm vụ dự án** được đặt theo mặc định thành dạng xem **Nhiệm vụ dự án mở của tôi**. Để tạo mục nhập thời gian cho các tác vụ chưa được chỉ định cho người dùng, hãy bấm vào **Thay đổi dạng xem** trên mục tra cứu và chọn **Tất cả nhiệm vụ dự án hiện hoạt**. Sau khi mục nhập thời gian đã được tạo và hiển thị trong lưới, bạn có thể chỉnh sửa bất kỳ giá trị dòng nào ngay trong lưới.  

### <a name="bulk-createcopy"></a>Tạo/sao chép hàng loạt 
Sau khi một vài mục nhập thời gian đã được tạo, bạn có thể sử dụng chức năng sao chép để tạo hàng loạt các mục nhập thời gian bổ sung. Bấm vào **Sao chép** để mở hộp thoại **Sao chép**. Trong **Từ khoảng thời gian: Ngày bắt đầu**, chọn phạm vi ngày phải được sao chép khoảng thời gian. Trong **Tới khoảng thời gian: Ngày bắt đầu**, chọn ngày phải tạo mục nhập thời gian. Bấm vào **Sao chép** để sao chép các mục nhập thời gian vào ngày tương ứng trong tuần được nêu trong trường **Tới khoảng thời gian**. Ví dụ: mục nhập thời gian của Thứ hai từ tuần trước sẽ được sao chép vào Thứ hai của tuần nêu trong trường **Tới khoảng tời gian**. 

![Sao chép hàng loạt mục nhập thời gian.](media/bulk-copy-time-entry-09.png)
 
### <a name="import-data"></a>Nhập dữ liệu 
Nội dung chỉ định và thay đổi tuân theo cùng một mẫu giao diện người dùng, cho phép người dùng chỉ định phạm vi ngày mà cần nhập đăng ký. Sau đó, bạn phải chọn rõ ràng các mục đặt trước sẽ được sao chép vào mục nhập thời gian **Nháp**. Trong phiên bản 3, bạn không còn thấy mẫu mục nhập thời gian **Đề xuất** trên lưới và trên lịch nữa.  

### <a name="change-in-calendar-control"></a>Thay đổi trong bộ kiểm soát lịch
Trong phiên bản 3, chúng tôi đã bỏ bộ kiểm soát lịch tùy chỉnh và hiện sử dụng Lịch UC để hiển thị các mục nhập thời gian trong tuần. Với lịch này, bạn có thể xem ngày, tuần và tháng. 

> [!NOTE]
> Giới hạn của Lịch là bộ kiểm soát này không hỗ trợ các hành động đối với từng mục riêng trên lịch. Ví dụ: bạn không thể chọn một hoặc nhiều mục trên lịch và gửi hoặc xóa các mục đó. Thao tác bấm vào mục trên lịch sẽ mở trang **Thực thể mục nhập thời gian** cho các hành động bổ sung. 

### <a name="extensibility"></a>Khả năng mở rộng
**Chỉ chụp dữ liệu trên các trường tùy chỉnh trong thực thể mục nhập thời gian và chi phí** - Mục nhập thời gian sử dụng lưới có thể chỉnh sửa, lưới chỉ đọc và các bộ kiểm soát lịch từ nền tảng. Tất cả các bộ kiểm soát này đều tự nhiên và do đó, sẽ hỗ trợ các tùy chỉnh. Trong Project Service Automation phiên bản 3, bạn có thể thêm các trường tùy chỉnh bổ sung, thiết lập các trường tra cứu và sao lưu chúng bằng dạng xem tùy chỉnh. Bạn cũng có thể đặt logic công việc tùy chỉnh theo các giá trị đã chọn trong trường tùy chỉnh.  

**Chụp dữ liệu trên các trường tùy chỉnh trong mục nhập thời gian và chi phí, rồi lan truyền thông qua các thực thể hỗ trợ luồng gửi và phê duyệt** - Quá trình xử lý mục nhập thời gian thông thường được hiển thị trong sơ đồ sau.

![Luồng xử lý mục nhập thời gian.](media/process-time-entries-10.png)

Nếu yêu cầu công việc quy định rằng các thực thể thời gian và chi phí phải bao gồm các thông số định giá tùy chỉnh và lan truyền các giá trị do một nguồn lực thời gian và mục nhập trong thông số định giá tùy chỉnh thông qua tất cả các thực thể trong sơ đồ trước, hãy xem phần [Thiết lập các trường tùy chỉnh làm thông số định giá](set-up-pricing-dimensions.md)

Để hỗ trợ các yêu cầu công việc trong đó thực thể thời gian và chi phí phải bao gồm các thông số không định giá tùy chỉnh và lan truyền các giá trị, bạn có thể sử dụng tính năng thiết lập thông số định giá và thể hiện thông số tùy chỉnh dưới dạng thông số định giá mà không có tỷ lệ chi phí hoặc hóa đơn. Một tình huống khác là thêm trường tùy chỉnh vào từng thực thể, sử dụng cùng một tên trường cho tất cả các thực thể. Có thể tạo các phần bổ trợ tùy chỉnh để liên hệ các bản ghi trong thực thể sẽ tham gia vào luồng gửi/phê duyệt bằng các thực thể nguồn gốc giao dịch và kết nối giao dịch.  

### <a name="delegate-time-and-expense-entry"></a>Ủy quyền mục nhập thời gian và chi phí
Nền tảng Common Data Service không hỗ trợ việc một người dùng mạo danh là người dùng khác, điều này nghĩa là trong phiên bản 3 của Project Service Automation, không có tính năng hỗ trợ mục nhập thời gian và chi phí được ủy quyền. Tuy nhiên, đối tác và khách hàng đã sử dụng một giải pháp để cho phép hỗ trợ trải nghiệm mục nhập thời gian được ủy quyền trong phiên bản 3. Đây chỉ là một phương án chứ không phải một giải pháp toàn diện, do đó, cần hiểu được các giới hạn và chỉ sử dụng phương án này nếu các giới hạn chấp nhận được. 

> [!IMPORTANT]
> Chỉ xem xét thông tin này, trong đó có hướng dẫn đề xuất đối tác/khách hàng triển khai tùy chỉnh. Nhóm sản phẩm sẽ không cung cấp tính năng hỗ trợ thông thường cho chức năng này thông qua bất kỳ kênh hỗ trợ nào.

### <a name="customization-details"></a>Thông tin chi tiết về quá trình tùy chỉnh 
Quá trình tùy chỉnh cho phép bạn thêm **Nguồn lực có thể đặt** vào trải nghiệm tạo và chỉnh sửa, điều này sẽ cho phép người dùng hành động với tư cách người ủy quyền bằng cách thay đổi trường **Đăng ký nguồn lực** thành một người dùng khác cần ghi lại các mục nhập thời gian và chi phí. Các bước sau minh họa quá trình ủy quyền mục nhập thời gian. Thông tin này cũng áp dụng cho việc ủy quyền mục nhập chi phí. 
 
1.  Đảm bảo rằng người dùng đã ủy quyền có quyền truy cập bảo mật toàn cầu vào các nhiệm vụ dự án và dự án. 
1.  Vì trường **Đăng ký nguồn lực** trên thực thể **Mục nhập thời gian** không hiển thị trên trang **Tạo nhanh** nên bạn cần thêm trường đó.

    -hoặc-

    Tạo dạng xem tùy chỉnh bao gồm cột **Nguồn lực có thể đặt trước** để chỉ xem mục nhập thời gian được tạo cho nguồn lực. Đăng các mục tùy chỉnh lên công cụ thiết kế mô-đun ứng dụng để dạng xem này hiển thị trong phần **Bộ chọn dạng xem** trên trang **Mục nhập thời gian**. Có hai phần bổ trợ xử lý việc đặt người quản lý cho các mục nhập thời gian không phải của dự án:

    - PreValidateTimeEntryCreate
    - PreValidateTimeEntryUpdate
 
1. Tạo phần bổ trợ mới để ghi đè trường **Người quản lý** thành người quản lý của người dùng được chỉ định trong trường **Nguồn lực có thể đặt**. Sử dụng cùng một **Giai đoạn thực thi** làm phần bổ trợ ngoài băng (OOB) (trước khi xác thực) và một **Thứ tự thực thi** cao hơn phần bổ trợ OOB (lớn hơn 1). Điều này sẽ đảm bảo rằng phần bổ trợ tùy chỉnh được thực thi sau phần bổ trợ OOB.  
 
### <a name="end-user-experience"></a>Trải nghiệm người dùng cuối
1.  Khi bạn tạo mục nhập thời gian trên trang tạo nhanh, hãy nhập thông tin chi tiết của Dự án và Nhiệm vụ dự án rồi chọn người dùng trên trường **Nguồn lực có thể đặt** mà có mục nhập thời gian cần ghi. 
2.  Theo mặc định, trường này đặt mặc định ở người dùng đăng nhập. Tuy nhiên, trong trường hợp người dùng đã ghi đè trường này, thì mục nhập thời gian sẽ được tạo cho **Nguồn lực có thể đặt** đã chọn.
3.  Khi bạn gửi mục nhập thời gian mình đã tạo cho các bản ghi này, các mục nhập sẽ ở trong hàng đợi để chờ phê duyệt trong dự án như mong đợi. 
4.  Khi bạn lấy lại mục nhập thời gian được tạo cho người dùng còn lại, các mục nhập thời gian sẽ được trả về trạng thái **Nháp** có trường **Nguồn lực có thể đặt** được đặt thành người dùng còn lại. 
5.  Nếu muốn, bạn có thể chuyển sang dạng xem tùy chỉnh để lọc các mục nhập thời gian được tạo cho người dùng còn lại. 
 
### <a name="limitations"></a>Giới hạn
Chức năng **Sao chép** và **Nhập** chỉ hoạt động trong ngữ cảnh của người dùng đã đăng nhập. Điều này nghĩa là không thể sao chép hoặc nhập các mục nhập thời gian được tạo cho người dùng đã đăng nhập với tư cách là nguồn lực có thể đặt.

Các mục nhập thời gian không dành cho dự án sẽ chỉ được chuyển sang trạng thái chờ phê duyệt của người quản lý nguồn lực có thể đặt nếu đã hoàn thành bước 4 trong phần **Thông tin chi tiết về quá trình tùy chỉnh** ở trên. Nếu không, các mục nhập thời gian không thuộc dự án cho người dùng còn lại sẽ được chuyển không chính xác đến người quản lý của người dùng đã đăng nhập. 

### <a name="other-changes"></a>Các thay đổi khác 
Chức năng **Đăng ký và nhiệm vụ** đã bị gỡ bỏ. 

## <a name="multidimensional-pricing"></a>Định giá dựa trên nhiều thông số
Để tăng tối đa sự linh hoạt và đáp ứng các yêu cầu công việc khác nhau, phiên bản 3 của Project Service Automation hỗ trợ việc áp dụng cụ thể thông số định giá đặt thành tỷ lệ chi phí và hóa đơn. Có thể đặt các giá trị thông số là mặc định, sau đó áp dụng trên quy trình định giá và tính phí, từ nguồn lực đến lập hồ sơ, đến mục nhập thời gian và thực tế dự án. Cấu hình dành riêng cho khách hàng và sửa đổi hoặc tiện ích tận dụng cơ sở hạ tầng tùy chỉnh tiêu chuẩn.

Project Service Automation đi kèm với một bộ thông số định giá, vai trò và đơn vị nguồn lực mặc định, cho phép thiết lập giá và chi phí cho từng tổ hợp Vai trò và Đơn vị tổ chức.

Đối với các khách hàng của Project Service Automation muốn tiếp tục sử dụng các trường sẵn dùng này làm thông số định giá trong phiên bản 3, không có bất kỳ thay đổi nào quá rõ rệt. Bạn có thể tiếp tục sử dụng Project Service Automation như bình thường. Tuy nhiên, nếu bạn cần định giá hoặc chi phí cho nguồn lực của mình bằng các thuộc tính bổ sung khác, thì phiên bản 3 cho phép thêm thông số định giá tùy chỉnh của riêng bạn vào Project Service Automation. Việc mở rộng các thông số định giá tùy chỉnh là một trải nghiệm cấu hình phức tạp. 

## <a name="quotes-and-contracts"></a>Báo giá và hợp đồng
Trong phiên bản 3 của Project Service Automation, các khía cạnh thiết lập cũng như quản lý báo giá và hợp đồng đã thay đổi. Các phần sau cung cấp thêm thông tin chi tiết.

### <a name="set-up-chargeability-options"></a>Thiết lập các tùy chọn cho khả năng tính phí
Trong phiên bản 1 và 2, việc thiết lập khả năng tính phí cho vai trò và danh mục cho báo giá cũng như hợp đồng chi tiết đã được thực hiện bằng chế độ xem **Khả năng tính phí** ở phần điều hướng trên cùng của mô tả báo giá hoặc mô tả hợp đồng. Đây cũng là nơi bạn có thể thiết lập giá cho các danh mục vai trò và chi phí đó.

Kể từ phiên bản 3, việc thiết lập các tùy chọn về khả năng tính phí theo vai trò và danh mục chi phí sẽ được thực hiện ở cấp mô tả báo giá hoặc hợp đồng. Quá trình thiết lập giá sẽ tách biệt với thiết lập khả năng tính phí. Bạn sẽ có thể tìm **Vai trò có thể tính phí** và **Danh mục có thể tính phí** dưới dạng tab trên các trang **Mô tả báo giá** và **Mô tả hợp đồng** mà không phải sử dụng phần điều hướng ở trên cùng.

![Các vai trò có thể tính phí.](media/chargeable-12.png)
 
Việc thiết lập Vai trò có thể tính phí và Danh mục có thể tính phí cũng tận dụng bộ kiểm soát lưới có thể chỉnh sửa sẵn dùng. Đối với mỗi vai trò và danh mục, các lựa chọn được hỗ trợ đối với loại lập hóa đơn trong giai đoạn Báo giá và Tạo hợp đồng sẽ không thay đổi so với các phiên bản trước, đó là **Có thể tính phí** và **Không thể tính phí**. **Miễn phí** không phải là loại được hỗ trợ trong giai đoạn Báo giá hoặc Tạo hợp đồng. **Miễn phí** chỉ được hỗ trợ trong quá trình phê duyệt Thời gian hoặc Chi phí.  
 
### <a name="create-and-edit-custom-pricing-for-a-project-service-automation-quote-and-project-contract"></a>Tạo và chỉnh sửa tùy chọn định giá tùy chỉnh cho hợp đồng dự án và báo giá Project Service Automation
Trong phiên bản 1 và 2, việc sử dụng bảng giá tùy chỉnh cho các hợp đồng và báo giá cụ thể đã được thực hiện bằng mục **Chỉnh sửa giá** trên dạng xem **Khả năng tính phí**. Dạng xem **Khả năng tính phí** nằm ở phần điều hướng trên cùng của mô tả báo giá hoặc mô tả hợp đồng. Đây cũng là nơi bạn có thể thiết lập các tùy chọn cho khả năng tính phí đối với danh mục vai trò hoặc chi phí.

Kể từ phiên bản 3, việc tạo và sử dụng bảng giá tùy chỉnh cho dự án đối với báo giá Project Service Automation và hợp đồng dự án Project Service Automation đã tách biệt với tùy chọn thiết lập khả năng tính phí. Báo giá Project Service Automation và hợp đồng dự án Project Service Automation có một tab mới gọi là **Bảng giá dự án**. Tab này hiển thị dạng xem liên kết của tất cả bảng giá Dự án được đính kèm với báo giá Project Service Automation hoặc hợp đồng dự án. Để tạo bảng giá tùy chỉnh từ một bảng giá hiện có đã được liên kết với hợp đồng hoặc báo giá dự án, hãy bấm vào **Tạo nội dung định giá tùy chỉnh**. Thao tác này sẽ tạo một bản sao của tất cả các bảng giá liên kết rồi đính kèm chúng với Báo giá hoặc hợp đồng. Giờ đây, bạn có thể mở bảng giá và chỉnh sửa giá theo danh mục vai trò hoặc chi phí để những thay đổi về giá đó sẽ chỉ áp dụng cho báo giá hoặc hợp đồng này. 
  
Sơ đồ sau đây là trước khi tạo bảng giá tùy chỉnh.

![Trước bảng giá tùy chỉnh.](media/before-custom-price-lists-13.png)

Sơ đồ sau đây là sau khi tạo bảng giá tùy chỉnh.

![Sau bảng giá tùy chỉnh.](media/after-custom-price-lists-14.png)

> [!NOTE]
> Có thể xuất hiện tình trạng chậm trễ trong thời gian ngắn khi bạn bấm vào **Tạo nội dung định giá tùy chỉnh** khi bảng giá được tạo. Bạn nên làm mới lưới thay vì bấm nhiều lần. Một bảng giá tùy chỉnh đã được tạo nếu tên bảng giá liên kết có tên báo giá hoặc tên hợp đồng dự án đi kèm.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
