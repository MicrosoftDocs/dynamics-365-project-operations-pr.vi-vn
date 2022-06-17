---
title: Ước tính doanh số và chi phí khi một nguồn lực có thể đăng ký đảm nhận nhiều vai trò của dự án
description: Bài viết này giải thích cách sử dụng thứ nguyên định giá để hỗ trợ ước tính giá và chi phí cho một tài nguyên đảm nhiệm nhiều vai trò trong một dự án.
author: rumant
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 9bb59537aaa75d9003925bec37642a2fa7c9ca22
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923490"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-on-a-project"></a>Ước tính doanh số và chi phí khi một nguồn lực có thể đăng ký đảm nhận nhiều vai trò của dự án 

_**Áp dụng đối với:** Project Operations cho tình huống dựa trên nguồn lực/hàng không nhập kho, triển khai Lite - từ thỏa thuận đến lập hóa đơn ước giá, Project Operations cho tình huống dựa trên hàng trữ kho/sản xuất_ 

Thông thường, các công ty hoạt động theo dự án sẽ cần có một nguồn lực đảm nhận nhiều vai trò trong một dự án. Mỗi vai trò có thể có giá và chi phí khác nhau. Điều này nghĩa là thời gian của cùng một nguồn lực trong dự án có thể được ước tính tài chính khác nhau, tùy theo hóa đơn và mức phí của từng vai trò. Bạn có thể thiết lập các giá trị trên bản ghi thành viên nhóm đối với nguồn lực đã đặt tên với các bản ghi đè khác nhau cho mỗi nhiệm vụ mà thành viên nhóm được chỉ định.

Ví dụ sau đây sẽ trình bày cách chỉ cần thay đổi một giá trị đơn giản, nguồn lực sẽ có thể có nhiều vai trò trong dự án với mức chi phí và hóa đơn khác nhau.

## <a name="create-tasks"></a>Tạo nhiệm vụ
Để tạo nhiệm vụ, bạn phải thêm nhiệm vụ, cũng như nhiệm vụ tóm tắt, sau đó bạn cần giao nhiệm vụ trước khi thêm thời gian nhiệm vụ. 

### <a name="add-tasks-and-summary-tasks"></a>Thêm nhiệm vụ và nhiệm vụ tóm tắt
Để thêm nhiệm vụ, hãy hoàn thành các bước sau đây.

1. Đi đến **Dự án** rồi mở dự án mà bạn muốn thêm nhiệm vụ.
2. Chọn **Thêm nhiệm vụ mới**. Đặt tên cho nhiệm vụ rồi nhấn vào **Nhập**.
3. Nhập tên khác cho nhiệm vụ rồi nhấn **Nhập**. Lặp lại thao tác này cho đến khi hoàn thành danh sách nhiệm vụ.
3. Để thụt dòng nhiệm vụ vào phần nhiệm vụ **Tóm tắt**, hãy chọn dấu 3 chấm dọc cạnh tên nhiệm vụ, sau đó chọn **Tạo nhiệm vụ phụ**. 

  > [!TIP]
  > Để chọn nhiều nhiệm vụ cùng lúc, hãy chọn một nhiệm vụ rồi nhấn và giữ phím **Ctrl**, sau đó chọn các nhiệm vụ khác.
  >
  > Bạn cũng có thể chọn **Đẩy nhiệm vụ phụ** để đưa nhiệm vụ ra khỏi phần nhiệm vụ **Tóm tắt**.

### <a name="assign-tasks"></a>Giao nhiệm vụ

Để giao nhiệm vụ, hãy hoàn thành các bước sau đây.

1. Trong cột **Giao cho** của nhiệm vụ, hãy chọn biểu tượng người.
2. Chọn một thành viên nhóm trong danh sách hoặc nhập văn bản để tìm tên.

### <a name="add-task-duration-and-columns"></a>Thêm thời gian nhiệm vụ và các cột

Thời gian là cách dễ nhất để bắt đầu xây dựng dự án. Để thêm thời gian nhiệm vụ, hãy hoàn thành các bước sau đây.

1. Trong cột **Thời gian** của một nhiệm vụ, hãy nhập số ngày bạn cho là cần thiết để hoàn thành nhiệm vụ. Nếu bạn muốn dùng đơn vị thời gian khác, hãy nhập một số kèm theo từ **giờ**, **tuần** hoặc **tháng**.
2. Nếu bạn muốn nhiệm vụ xuất hiện dưới mốc hình kim cương trong chế độ xem **Dòng thời gian** thì trong cột **Thời gian**, hãy nhập **0 ngày**.
3. Nhấn vào **Nhập** để chuyển đến trường **Thời gian** của nhiệm vụ tiếp theo và tiếp tục nhập các khoảng thời gian.

  > [!NOTE]
  > Bạn không thể nhập thời gian cho các nhiệm vụ tóm tắt.

Bạn có thể thêm các cột vào dự án để cung cấp thêm thông tin chi tiết. Để thực hiện việc này, hãy chọn **Thêm cột**. 

Để biết thêm thông tin, hãy xem [Tạo dự án](https://support.microsoft.com/en-us/office/create-a-project-a5b5e823-fb2e-45fd-be00-7d84422d9749).

## <a name="set-up-the-role-and-organization-unit-for-a-generic-project-team-member"></a>Thiết lập vai trò và đơn vị tổ chức cho một thành viên nhóm dự án chung
Hoàn thành các bước sau để thiết lập vai trò và đơn vị tổ chức cho một thành viên nhóm chung.

1. Trên trang **Nhiệm vụ**, hãy chọn dòng **Nhiệm vụ** cho **Nhiệm vụ A**. 
2. Trong phần **Giao cho**, hãy chọn **Thêm nguồn lực chung**. Trang **Tạo nhanh thành viên nhóm** sẽ mở ra.
3. Trên trang **Tạo nhanh thành viên nhóm**, chỉ định thuộc tính của thành viên nhóm chung có thể thực hiện nhiệm vụ này.
4. Chọn vai trò và đơn vị tổ chức thích hợp, sau đó chọn **Lưu và đóng**. Một thành viên nhóm chung được tạo và phân công nhiệm vụ này. 
5. Lặp lại các bước từ 1-4 cho **Nhiệm vụ B**. Tuy nhiên, thành viên chung của **Nhiệm vụ B** phải được chỉ định vai trò và đơn vị tổ chức khác với **Nhiệm vụ A**. 

## <a name="set-up-the-role-and-organization-unit-for-a-project-task"></a>Thiết lập vai trò và đơn vị tổ chức cho một nhiệm vụ dự án
Hoàn thành các bước sau để thiết lập vai trò và đơn vị tổ chức cho một nhiệm vụ.

1. Sau khi bạn tạo **Nhiệm vụ A**, hãy chọn nhiệm vụ đó rồi bấm vào biểu tượng **i** để mở ngăn **Chi tiết nhiệm vụ**. 
2. Trên ngăn **Chi tiết nhiệm vụ**, hãy cuộn xuống dưới cùng rồi chọn **Xem chi tết** để mở ngăn **Chi tiết nhiệm vụ**.
3. Trên trang **Chi tiết nhiệm vụ**, trong phần **Vai trò** và **Đơn vị tổ chức**, hãy thêm các giá trị cần thiết để thực hiện nhiệm vụ này cho nguồn lực. 

  > [!NOTE]
  > Nếu bạn hoàn tất kịch bản này bằng dữ liệu minh họa của Project Operations, hãy chọn **Tư vấn trưởng** đối với vai trò, và **Fabrikam US** làm đơn vị tổ chức.

4. Chọn **Nhiệm vụ B** rồi chọn nhiệm vụ này.
5. Chọn biểu tượng **i** để mở ngăn **Chi tiết nhiệm vụ**. 
6. Trên ngăn **Chi tiết nhiệm vụ**, hãy cuộn xuống dưới cùng rồi chọn **Xem chi tết** để mở ngăn **Chi tiết nhiệm vụ**.
7. Trên trang **Chi tiết về nhiệm vụ**, trong phần **Vai trò** và **Đơn vị tổ chức**, hãy thêm các giá trị cần thiết mà nguồn lực cần để thực hiện nhiệm vụ này. Các giá trị trong phần **Vai trò** và **Đơn vị tổ chức** của **Nhiệm vụ B** phải khác với **Nhiệm vụ A**. 

  > [!NOTE]
  > Nếu bạn hoàn tất kịch bản này bằng dữ liệu minh họa của Project Operations, hãy chọn **Kỹ thuật viên mạng** đối với vai trò, và **Fabrikam US** làm đơn vị tổ chức.

8. Lưu và đóng trang **Chi tiết nhiệm vụ**. 

## <a name="team-member-and-estimates-behavior"></a>Hành vi thành viên nhóm và giá trị ước tính 
Để hiểu được hành vi trên lưới **Thành viên nhóm** và các giá trị ước tính, hãy hoàn tất các bước sau.

1. Trên lưới **Thành viên nhóm**, hãy chọn 2 thành viên nhóm chung, sau đó chọn **Tạo yêu cầu**. Thao tác này sẽ tạo yêu cầu về nguồn lực. 
2. Chọn hàng thành viên nhóm cho **Tư vấn trưởng** rồi chọn **Đăng ký**. Bảng lịch trình sẽ mở ra, chứa danh sách các nguồn lực. Chọn một nguồn lực rồi chọn **Đăng ký** để đăng ký nguồn lực phù hợp với yêu cầu đó.
3. Chọn hàng thành viên nhóm cho **Kỹ thuật viên mạng**, sau đó chọn **Đăng ký**. Bảng lịch trình sẽ mở ra, chứa danh sách các nguồn lực. Chọn nguồn lực giống như ở trên rồi chọn **Đăng ký** để đăng ký nguồn lực phù hợp với yêu cầu đó.

### <a name="team-member-grid"></a>Lưới Thành viên nhóm 

Trên lưới **Thành viên nhóm**, các bản ghi của 2 thành viên nhóm chung sẽ bị xóa và được thay thế bằng một nguồn lực duy nhất. Có một bộ giá trị cho nguồn lực đó. Đây là bộ giá trị mặc định của **Vai trò** và **Đơn vị tổ chức**.

Khi mở rộng hàng này cho bản ghi thành viên nhóm đó, bạn có thể xem những lượt phân công riêng biệt trên bản ghi thành viên nhóm của cả 2 nhiệm vụ. Mỗi hàng phân công có các giá trị cụ thể cho nhiệm vụ đối với **Vai trò** và **Đơn vị tổ chức**. 

### <a name="estimates-grid"></a>Lưới ước tính 

Trên lưới **Ước tính**, 2 lượt phân công của cùng một nguồn lực sẽ có giá khác nhau. Lượt phân công nguồn lực cho **Nhiệm vụ A** được tính theo giá trị của thuộc tính **Vai trò** là **Tư vấn trưởng**. Lượt phân công cũng của nguồn lực đó cho **Nhiệm vụ B** được tính theo giá trị của thuộc tính **Vai trò** là **Kỹ thuật viên mạng**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]