---
title: Tạo cấu trúc phân tích công việc
description: Chủ đề này giải thích cách tạo cấu trúc phân tích công việc (WBS) bao gồm bộ điều khiển cơ bản trong giao diện lập lịch mới.
author: ruhercul
manager: tfehr
ms.date: 01/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 695bbc2ae1ba1e762472b5f5fa853c89017d2f52
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287039"
---
# <a name="create-a-work-breakdown-structure-wbs"></a>Tạo cấu trúc phân tích công việc (WBS)

Lịch trình dự án cho biết những việc cần hoàn thành, các nguồn lực sẽ thực hiện công việc và khung thời gian cần hoàn thành công việc. Lịch trình phản ánh tất cả công việc liên quan đến việc giao dự án đúng thời hạn. Trong Dynamics 365 Project Operations, bạn tạo lịch trình dự án bằng cách:

  - Chi nhỏ công việc thành các nhiệm vụ có thể quản lý.
  - Ước tính thời gian cần thiết để thực hiện mỗi nhiệm vụ.
  - Đặt mức phụ thuộc của nhiệm vụ.
  - Đặt thời gian nhiệm vụ.
  - Ước tính nguồn lực chung sẽ thực hiện nhiệm vụ. 

Lịch trình dự án được tạo trên tab **Lịch trình** của trang **Dự án**.

## <a name="tasks"></a>Tác vụ

Bước đầu tiên trong việc tạo ra một lịch trình dự án là chia nhỏ công việc thành các phần có thể quản lý. Lịch trình trong Project Operations hỗ trợ các tính năng sau:

- Nhiệm vụ tóm tắt hoặc vùng chứa
- Nhiệm vụ nút lá

### <a name="summary-tasks"></a>Nhiệm vụ tóm tắt

Nhiệm vụ tóm tắt có thể lưu trữ các nhiệm vụ tóm tắt khác hoặc các nhiệm vụ nút lá. Chúng không có nhân công công việc hoặc chi phí của riêng mình. Thay vào đó, chi phí và nhân công công việc là tổng số nhân công công việc và chi phí của các nhiệm vụ bộ chứa của chúng. Ngày bắt đầu nhiệm vụ tóm tắt là ngày bắt đầu của nhiệm vụ bộ chứa và ngày kết thúc là ngày kết thúc của các nhiệm vụ bộ chứa. Có thể chỉnh sửa tên của nhiệm vụ tóm tắt nhưng không thể chỉnh sửa các thuộc tính lập lịch, bao gồm nhân công, ngày và khoảng thời gian. Nếu xóa nhiệm vụ tóm tắt, bạn cũng có thể xóa tất cả các nhiệm vụ bộ chứa của nó.

### <a name="leaf-node-tasks"></a>Nhiệm vụ nút lá

Các nhiệm vụ nút lá biểu thị công việc chi tiết nhất trên dự án. Chúng có khoảng thời gian, ngày kết thúc và bắt đầu theo kế hoạch, nguồn lực và nhân công ước tính.

## <a name="create-a-task-hierarchy"></a>Tạo một hệ thống cấp bậc cho nhiệm vụ

### <a name="add-a-task"></a>Thêm nhiệm vụ

Để thêm một hoặc nhiều nhiệm vụ, hãy hoàn thành các bước sau đây.

1. Đi đến **Dự án**, rồi chọn và mở bản ghi dự án mà bạn muốn tạo lịch trình. 
2. Chọn tab **Nhiệm vụ**. 
3. Chọn **Thêm nhiệm vụ mới**, nhập tên cho nhiệm vụ, rồi nhấn Enter.
2. Nhập tên nhiệm vụ khác và nhấn Enter lần nữa cho đến khi hoàn thành danh sách nhiệm vụ.

### <a name="manage-hierarchy-of-a-task"></a>Quản lý hệ thống cấp bậc của nhiệm vụ

Khi được thụt lề, một nhiệm vụ sẽ trở thành một nhiệm vụ con ngay bên trên. Sau đó, ID lịch trình của nhiệm vụ được tính toán lại để dựa trên ID lịch trình của nhiệm vụ mẹ của nó và tuân theo lược đồ đánh số phác thảo. Nhiệm vụ mẹ đang là một nhiệm vụ tóm tắt. Do đó, nhiệm vụ này sẽ trở thành tổng của các nhiệm vụ con. Khi được tăng cấp, nhiệm vụ này không còn là nhiệm vụ con của nhiệm vụ mẹ trước kia. Sau đó, ID lịch trình được tính toán lại để phản ảnh độ sâu và vị trí đã cập nhật của nhiệm vụ trong hệ thống cấp bậc. Nhân công, chi phí và ngày của nhiệm vụ mẹ trước đó được tính toán lại để chúng không bao gồm nhiệm vụ này.

Để thụt lề hoặc tăng cấp nhiệm vụ, hãy hoàn thành các bước sau đây.

1. Trong trang **Dự án**, vào tab **Nhiệm vụ** rồi vào phần **Nhiệm vụ tóm tắt**, hãy chọn dấu 3 chấm dọc cạnh tên nhiệm vụ, sau đó chọn **Tạo nhiệm vụ phụ**. 
2. Chọn nhiệm vụ để thụt lề hoặc tăng cấp. Để chọn nhiều nhiệm vụ cùng lúc, hãy chọn một nhiệm vụ rồi nhấn và giữ phím Ctrl, sau đó chọn thêm nhiệm vụ khác.
2. Chọn **Thụt lề** hoặc **Đẩy nhiệm vụ phụ** để đưa nhiệm vụ vào hoặc ra khỏi phần nhiệm vụ tóm tắt.

### <a name="move-tasks-up-and-down"></a>Di chuyển nhiệm vụ lên và xuống

Có thể chuyển nhiệm vụ đến bất kỳ cấp nào trong cấu trúc phân tích công việc theo một trong hai cách:

- Chọn thêm một nhiệm vụ và kéo đến vị trí mong muốn.
- Chọn một hoặc nhiều nhiệm vụ, nhấp chuột phải và chọn **Cắt**, chọn ô đích trong lịch trình, sau đó bấm chuột phải và chọn **Dán**.

## <a name="task-attributes"></a>Thuộc tính nhiệm vụ

Tên nhiệm vụ mô tả công việc phải hoàn thành. Trong Project Operations, các thuộc tính có liên quan đến một nhiệm vụ mô tả lịch trình và các yêu cầu bố trí nhân viên của nhiệm vụ đó.

## <a name="schedule-attributes"></a>Thuộc tính lịch trình

Các thuộc tính **Nhân công**, **Ngày bắt đầu**, **Ngày kết thúc** và **Khoảng thời gian** xác định lịch trình cho nhiệm vụ.

Bảng sau đây hiển thị các thuộc tính lịch trình bổ sung.

| **Tên hiển thị cuối cùng** | **Mô tả cuối cùng** |
| --- | --- |
| Nỗ lực Hoàn thành (Giờ) | Công việc đã hoàn thành cho nhiệm vụ theo giờ. |
| Thời lượng | Hiển thị khoảng thời gian theo ngày cho nhiệm vụ. |
| Tổng mức Nỗ lực | Tổng lượng việc cho nhiệm vụ theo giờ. |
| Kết thúc | Ngày và giờ kết thúc. |
| % Hoàn thành | Tỷ lệ phần trăm nhiệm vụ đã hoàn thành. |
| Bộ chứa Dự án | Bảng nhiệm vụ có thể được nhóm theo bộ chứa để mỗi bộ chứa đều có cột riêng. |
| Nỗ lực Còn lại (Giờ) | Công việc còn lại cho nhiệm vụ theo giờ. |
| Bắt đầu | Ngày và giờ bắt đầu. |
| Tên | Tên của nhiệm vụ. |
| ID | ID của nhiệm vụ trong cấu trúc phân tích công việc. |

Với tư cách là quản trị viên, bạn có thể xác định các trường tùy chỉnh trên thực thể nhiệm vụ. Tuy nhiên, các trường không thể được hiển thị trên lưới lịch biểu. Để xem các trường tùy chỉnh của bạn, hãy thêm chúng vào trang chi tiết **Nhiệm vụ dự án**.

## <a name="staffing-attributes"></a>Thuộc tính sắp xếp nhân viên

Có thể truy cập các thuộc tính bố trí nhân viên thông qua trường **Nguồn lực** trong lịch trình. Bạn cũng có thể tìm kiếm nguồn lực hiện có hoặc chọn **Tạo** và trong khung **Tạo nhanh**, thêm thành viên nhóm dự án ở dạng nguồn lực mới.

Các trường **Vai trò**, **Đơn vị nguồn lực** và **Tên vị trí** dùng để mô tả các yêu cầu bố trí nhân viên cho nhiệm vụ. Các thuộc tính bố trí nhân viên này cùng với lịch trình nhiệm vụ dùng để tìm các nguồn lực có sẵn để thực hiện nhiệm vụ này.

   - **Vai trò**: Chỉ định loại nguồn lực cần thiết để thực hiện nhiệm vụ này.
   - **Đơn vị nguồn lực**: Chỉ định đơn vị nên dùng để phân công nguồn lực cho nhiệm vụ. Các thuộc tính này ảnh hưởng đến ước tính chi phí và doanh thu cho nhiệm vụ nếu tỷ lệ hóa đơn và chi phí cho nguồn lực được đặt dựa trên các đơn vị nguồn lực.
   - **Tên vị trí**: Nhập tên cho nguồn chung dùng làm chỗ dành sẵn cho nguồn lực cuối cùng sẽ thực hiện công việc.

Trường **Nguồn lực** giữ tên vị trí cho nguồn lực chung hoặc nguồn lực có tên khi một nguồn lực được tìm thấy.

Trường **Thể loại** giữ giá trị cho biết loại công việc rộng hơn mà nhiệm vụ có thể được nhóm cùng. Trường này không ảnh hưởng đến việc lập lịch hoặc bố trí nhân viên. Thay vào đó, trường này chỉ được dùng để báo cáo.

## <a name="task-dependencies"></a>Đối tượng phụ thuộc của nhiệm vụ

Bạn có thể sử dụng lịch trình trong Project Operations để tạo mối quan hệ tiếp trước giữa các nhiệm vụ. Trường **Tiếp trước** dùng một hoặc nhiều giá trị cho biết các nhiệm vụ mà một nhiệm vụ phụ thuộc vào. Khi các giá trị tiếp trước được gán cho một nhiệm vụ, thì nhiệm vụ chỉ có thể bắt đầu sau khi tất cả các nhiệm vụ tiếp trước được hoàn thành. Do sự phụ thuộc, ngày bắt đầu nhiệm vụ theo kế hoạch được đặt lại thành ngày các nhiệm vụ tiếp trước được hoàn thành.

Chế độ nhiệm vụ không ảnh hưởng đến các thông tin cập nhật được thực hiện với ngày bắt đầu và ngày kết thúc của nhiệm vụ tiếp trước/phụ thuộc.

## <a name="accessibility-and-keyboard-shortcuts"></a>Trợ năng và phím tắt

Bạn hoàn toàn có thể truy cập lưới và dùng lưới **Lịch trình** với các trình đọc màn hình như Trình tường thuật, JAWS hoặc NVDA. Bạn có thể di chuyển qua vùng lưới bằng cách dùng các phím mũi tên (như trong Microsoft Excel), dùng phím Tab để cải thiện thông qua các yếu tố giao diện người dùng mang tính tương tác, dùng phím Mũi tên xuống, phím Enter hoặc Dấu cách để chọn hoặc mở các menu thả xuống.


[!INCLUDE[footer-include](../includes/footer-banner.md)]