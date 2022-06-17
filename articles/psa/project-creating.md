---
title: Lịch trình dự án
description: Bài viết này cung cấp thông tin về cách tạo lịch biểu.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 3/01/2019
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
ms.openlocfilehash: f0d052efda1b78161feed1c1e4cd70a31f3c4dea
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915900"
---
# <a name="project-schedules"></a>Lịch trình dự án 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Lịch trình dự án cho biết những việc cần hoàn thành, các nguồn lực sẽ thực hiện công việc và khung thời gian cần hoàn thành công việc. Lịch trình này phản ánh tất cả công việc liên quan đến việc cung cấp dự án đúng giờ. Trong Dynamics 365 Project Service Automation, bạn tạo một lịch trình dự án bằng cách chia nhỏ công việc thành các nhiệm vụ có thể quản lý, ước tính thời gian cần thiết để thực hiện từng nhiệm vụ, đặt mức phụ thuộc của nhiệm vụ, đặt thời gian nhiệm vụ và ước tính nguồn lực chung sẽ thực hiện nhiệm vụ. Lịch trình dự án được tạo trên tab **Lịch trình** của trang dự án.
 
## <a name="tasks"></a>Nhiệm vụ

Bước đầu tiên trong việc tạo ra một lịch trình dự án là chia nhỏ công việc thành các phần có thể quản lý. Lịch trình trong PSA hỗ trợ các tính năng sau:

- Nút gốc dự án.
- Nhiệm vụ tóm tắt hoặc vùng chứa
- Nhiệm vụ nút lá

### <a name="project-root-node"></a>Nút gốc dự án.

Nút gốc của dự án là nhiệm vụ tóm tắt cấp cao nhất cho dự án. Tất cả các nhiệm vụ khác của dự án được tạo trong nhiệm vụ này. Tên nút gốc luôn được đặt thành tên dự án. Nhân công, ngày và khoảng thời gian của nút gốc được tóm tắt dựa trên các giá trị trong hệ thống cấp bậc dưới nó. Bạn không thể chỉnh sửa các thuộc tính của nút gốc. Bạn cũng không thể xóa nút gốc.

### <a name="summary-or-container-tasks"></a>Nhiệm vụ tóm tắt hoặc vùng chứa 

Nhiệm vụ tóm tắt có nhiệm vụ phụ hoặc nhiệm vụ bộ chứa dưới chúng. Chúng không có nhân công công việc hoặc chi phí của riêng mình. Thay vào đó, chi phí và nhân công công việc là tổng số nhân công công việc và chi phí của các nhiệm vụ bộ chứa của chúng. Ngày bắt đầu nhiệm vụ tóm tắt là ngày bắt đầu của nhiệm vụ bộ chứa và ngày kết thúc là ngày kết thúc của các nhiệm vụ bộ chứa. Có thể chỉnh sửa tên của nhiệm vụ tóm tắt những không thể chỉnh sửa việc lập lịch các thuộc tính (nhân công, ngày và khoảng thời gian). Nếu xóa nhiệm vụ tóm tắt, bạn cũng có thể xóa tất cả các nhiệm vụ bộ chứa của nó.

### <a name="leaf-node-tasks"></a>Nhiệm vụ nút lá

Các nhiệm vụ nút lá biểu thị công việc chi tiết nhất trên dự án. Chúng có khoảng thời gian, ngày kết thúc và bắt đầu theo kế hoạch, nguồn lực và nhân công ước tính.
 
## <a name="creating-a-task-hierarchy"></a>Tạo một hệ thống cấp bậc cho nhiệm vụ

Bạn có thể tạo hệ thống cấp bậc cho nhiệm vụ bằng cách sử dụng các tùy chọn bên dưới:

- Nút **Thêm nhiệm vụ**
- Nút **Thụt lề nhiệm vụ**
- Nút **Nhô lề nhiệm vụ**
- Các nút **Chuyển lên** và **Chuyển xuống**
- Trợ năng và phím tắt

### <a name="add-task"></a>Thêm nhiệm vụ

Nút **Thêm nhiệm vụ** cho phép bạn tạo nhiệm vụ mới trong hệ thống cấp bậc. Nếu bạn không chọn một vị trí, nhiệm vụ sẽ được thêm vào phần cuối. 

ID lịch trình được gán cho mọi nhiệm vụ. ID lịch trình biểu thị cho độ sâu và vị trí của nhiệm vụ trong hệ thống cấp bậc. ID lịch trình dùng đánh số phác thảo. Đối với các nhiệm vụ ở cấp 1 trong nút gốc dự án, lược đồ đánh số 1, 2, 3, v.v. được sử dụng. Đối với các nhiệm vụ dưới cấp 1, lược đồ đánh số 1.1, 1.2, 1.3, v.v. được sử dụng.

### <a name="indent-task"></a>Thụt lề nhiệm vụ

Khi được thụt lề, một nhiệm vụ sẽ trở thành một nhiệm vụ con ngay bên trên. Sau đó, ID lịch trình của nhiệm vụ được tính toán lại để dựa trên ID lịch trình của nhiệm vụ mẹ của nó và tuân theo lược đồ đánh số phác thảo. Nhiệm vụ mẹ hiện là nhiệm vụ tóm tắt hoặc nhiệm vụ bộ chứa. Do đó, nhiệm vụ này sẽ trở thành tổng của các nhiệm vụ con.

### <a name="outdent-task"></a>Nhô lề nhiệm vụ 

Khi được nhô lề, nhiệm vụ này không còn là nhiệm vụ con của nhiệm vụ mẹ trước kia. Sau đó, ID lịch trình được tính toán lại để phản ảnh độ sâu và vị trí đã cập nhật của nhiệm vụ trong hệ thống cấp bậc. Nhân công, chi phí và ngày của nhiệm vụ mẹ trước đó được tính toán lại để chúng không bao gồm nhiệm vụ này.

### <a name="move-up-and-move-down"></a>Chuyển lên và chuyển xuống 

Các nút **Chuyển lên** và **Chuyển xuống** thay đổi vị trí của nhiệm vụ trong hệ thống cấp bậc mẹ của nó. Các thay đổi của loại này không ảnh hưởng đến nhân công, chi phí, ngày hoặc khoảng thời gian của nhiệm vụ. Chỉ có ID lịch trình của nhiệm vụ bị ảnh hưởng. ID lịch trình được tính toán lại để phản ánh vị trí mới của nhiệm vụ này trong danh sách các nhiệm vụ con của nhiệm vụ mẹ.

### <a name="accessibility-and-keyboard-shortcuts"></a>Trợ năng và phím tắt

Bạn hoàn toàn có thể truy cập lưới và dùng lưới **Lịch trình** với các trình đọc màn hình như Trình tường thuật, JAWS hoặc NVDA. Bạn có thể di chuyển qua vùng lưới bằng cách dùng các phím mũi tên (như trong Microsoft Excel), dùng phím Tab để cải thiện thông qua các yếu tố giao diện người dùng mang tính tương tác, dùng phím Mũi tên xuống, phím Enter hoặc Dấu cách để chọn hoặc gọi các menu thả xuống. Tiêu đề cột cũng mang tính tương tác. Bạn có thể ẩn và hiển thị các cột, dùng phím Tab và các phím mũi tên xuống để di chuyển qua các tiêu đề cột và dùng các nút hành động trên thanh công cụ. Ngoài ra, bạn có thể sử dụng các phím tắt sau:

- **Làm mới**: ALT+SHIFT+F5
- **Thêm**: ALT+SHIFT+Insert
- **Xóa**: ALT+SHIFT+Delete
- **Chuyển lên/xuống**: ALT+SHIFT+Up/Mũi tên xuống
- **Thụt lề/Nhô lề**: ALT_SHIFT+Left/Mũi tên phải
- **Bung rộng/Thu gọn hệ thống cấp bậc**: ALT+SHIFT+Plus/Phím trừ

## <a name="task-attributes"></a>Thuộc tính nhiệm vụ

Tên nhiệm vụ mô tả công việc phải hoàn thành. Trong PSA, các thuộc tính có liên quan đến một nhiệm vụ mô tả lịch trình của nhiệm vụ và các yêu cầu bố trí nhân viên của nhiệm vụ đó.

> ![Thuộc tính nhiệm vụ.](media/project-2.png)
 
### <a name="schedule-attributes"></a>Thuộc tính lịch trình

Các thuộc tính **Nhân công**, **Ngày bắt đầu**, **Ngày kết thúc** và **Khoảng thời gian** xác định lịch trình cho nhiệm vụ.

Các thuộc tính lịch trình bổ sung bao gồm:

- **Giờ nhân công**: Nhập ước tính thời gian cần thiết để hoàn thành nhiệm vụ. 
- **Khoảng thời gian**: Chỉ định số ngày làm việc cần thiết để hoàn thành nhiệm vụ.
- **ID lịch trình**: ID được tạo tự động này dùng để sắp xếp nhiệm vụ trong hệ thống cấp bậc. Sự phụ thuộc giữa các nhiệm vụ quản lý thứ tự thực tế của các nhiệm vụ.
 
### <a name="staffing-attributes"></a>Thuộc tính sắp xếp nhân viên

Có thể truy cập các thuộc tính bố trí nhân viên thông qua trường **Nguồn lực** trong lịch trình. Bạn cũng có thể tìm kiếm nguồn lực hiện có hoặc bấm vào **Tạo** và trong khung **Tạo nhanh**, thêm thành viên nhóm dự án ở dạng nguồn lực mới.

Các trường **Vai trò**, **Đơn vị nguồn lực** và **Tên vị trí** dùng để mô tả các yêu cầu bố trí nhân viên cho nhiệm vụ. Các thuộc tính bố trí nhân viên này cùng với lịch trình nhiệm vụ dùng để tìm các nguồn lực có sẵn để thực hiện nhiệm vụ này.

**Vai trò** – Chỉ định loại nguồn lực cần thiết để thực hiện nhiệm vụ này.

**Đơn vị nguồn lực** – Chỉ định đơn vị nên dùng để phân công nguồn lực cho nhiệm vụ. Các thuộc tính này ảnh hưởng đến ước tính chi phí và doanh thu cho nhiệm vụ nếu tỷ lệ hóa đơn và chi phí cho nguồn lực được đặt dựa trên các đơn vị nguồn lực.

**Tên vị trí** – Nhập tên thân thiện cho nguồn chung dùng làm chỗ dành sẵn cho nguồn lực cuối cùng sẽ thực hiện công việc.

Trường **Nguồn lực** giữ tên vị trí cho nguồn lực chung hoặc nguồn lực có tên khi một nguồn lực được tìm thấy.

Trường **Thể loại** giữ giá trị cho biết loại công việc rộng hơn mà nhiệm vụ có thể được nhóm cùng. Trường này không ảnh hưởng đến việc lập lịch hoặc bố trí nhân viên. Trường này chỉ dùng để báo cáo.

### <a name="task-dependencies"></a>Đối tượng phụ thuộc của nhiệm vụ 

Bạn có thể sử dụng lịch trình trong PSA để tạo mối quan hệ tiếp trước giữa các nhiệm vụ. Trường **Tiếp trước** trong **Nhiệm vụ** có một hoặc nhiều giá trị cho biết các nhiệm vụ mà một nhiệm vụ phụ thuộc vào. Khi các giá trị tiếp trước được gán cho một nhiệm vụ, thì nhiệm vụ chỉ có thể bắt đầu sau khi tất cả các nhiệm vụ tiếp trước được hoàn thành. Do sự phụ thuộc, ngày bắt đầu nhiệm vụ theo kế hoạch được đặt lại thành ngày các nhiệm vụ tiếp trước được hoàn thành.

Chế độ nhiệm vụ không ảnh hưởng đến các thông tin cập nhật được thực hiện với ngày bắt đầu và ngày kết thúc của nhiệm vụ tiếp trước/phụ thuộc.

## <a name="task-mode"></a>Chế độ nhiệm vụ 

Chế độ nhiệm vụ xác định việc lập lịch các nhiệm vụ nút lá. PSA hỗ trợ 2 chế độ nhiệm vụ cho mỗi nhiệm vụ: lập lịch tự động và lập lịch thủ công.

### <a name="auto-scheduling"></a>Tự động lập lịch 
 
Khi bạn đặt chế độ nhiệm vụ thành **Đã tự động lập lịch** cho một nhiệm vụ, thì công cụ lập lịch nhiệm vụ sử dụng các quy tắc lập lịch trên thuộc tính nhiệm vụ để xác định lịch trình cho nhiệm vụ.

#### <a name="scheduling-rules"></a>Quy tắc lập lịch

Theo mặc định, nếu nhiệm vụ nút lá không có nhiệm vụ tiếp trước, thì ngày bắt đầu của nhiệm vụ này được đặt thành ngày bắt đầu theo lịch của dự án. Khoảng thời gian của nhiệm vụ nút lá luôn được tính toán là số ngày làm việc giữa của ngày bắt đầu và ngày kết thúc. Khi một nhiệm vụ được lập lịch tự động, công cụ lập lịch tuân thủ các quy tắc dưới đây:

- Ngày bắt đầu và ngày kết thúc của nhiệm vụ phải là ngày làm việc, theo lịch lập dịch của dự án. 
- Đối với mọi nhiệm vụ có nhiệm vụ tiếp trước, ngày bắt đầu tự động được đặt thành ngày kết thúc muộn nhất của nhiệm vụ tiếp trước.
- Nhân công được tính bằng cách sử dụng công thức này: Số người × Khoảng thời gian × Giờ trong ngày làm việc tiêu chuẩn trong lịch dự án.

### <a name="manual-scheduling"></a>Lên lịch thủ công

Nếu quy tắc của lập lịch tự động không đáp ứng các yêu cầu của bạn, thì bạn có thể đặt chế độ nhiệm vụ cho nhiệm vụ thành **Đã lập lịch theo cách thủ công**. Cài đặt này sẽ ngăn công cụ lập lịch không tính toán giá trị của các thuộc tính lập lịch khác. Bất kể chế độ nhiệm vụ, nếu đặt nhiệm vụ tiếp trước trên các nhiệm vụ, bạn sẽ luôn làm ảnh hưởng đến ngày bắt đầu của nhiệm vụ phụ thuộc.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
