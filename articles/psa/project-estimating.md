---
title: Chi phí và doanh thu dự án
description: Chủ đề này cung cấp thông tin về ước tính chi phí và doanh thu dự án.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: fe51af8adb7c3831a57494b8359def2a0176b552efe16feb53a2a265f5ffcb0c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/06/2021
ms.locfileid: "7002582"
---
# <a name="project-costs-and-revenue"></a>Chi phí và doanh thu dự án

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Ước tính dự án cung cấp dạng xem tài chính cho các công việc được ước tính và lập lịch trong lịch trình dự án. Tab **Ước tính** trên trang **Dự án** hiển thị tác động doanh thu và chi phí của công việc bạn đang lên kế hoạch. Tab này cũng cung cấp thông tin về nhiều tham số được xác định trước. 

> ![Tab ước tính.](media/project-5.png)

## <a name="cost-and-sales-values-of-the-project"></a>Giá trị chi phí và kinh doanh của dự án

Bảng giá xác định tỷ suất chiết khấu và chi phí cho các vai trò trong dự án. Bạn có thể xác định tác động chi phí và doanh thu của công việc, dựa trên các vai trò liên kết với tên vị trí và nguồn lực có tên được phân công cho nhiệm vụ. Nếu nhiệm vụ không có phân công (chung hoặc có tên), bạn không thể nhận ước tính doanh thu hoặc chi phí. Giá trị chi phí và doanh thu xem xét ngày được xác định trong bảng giá.

### <a name="default-cost-price"></a>Giá vốn mặc định  

Mỗi dự án thuộc về một tổ chức. Tổ chức này hiển thị trong trường **Đơn vị ký hợp đồng** trong dự án. Bảng giá liên quan đến đơn vị ký hợp đồng dùng để xác định giá vốn cho đơn vị. Để xác định giá vốn chính xác trên các vai trò cho ngày được xác định trên mô tả ước tính, hãy tìm kiếm kết hợp vai trò, đơn vị và đơn vị tổ chức trong bảng giá vốn. 

Vì vậy, giá vốn của họ có thể được tính toán, tất cả nhiệm vụ phải được phân công cho nguồn lực. Mọi nhiệm vụ chưa được phân công sẽ có giá vốn là 0,00.

Nếu kết hợp vai trò, đơn vị và đơn vị tổ chức không trả lại giá vốn từ bảng giá của đơn vị ký hợp đồng, hệ thống sẽ bỏ qua đơn vị đó. Thay vào đó, hệ thống tìm kiếm kết hợp chỉ có vai trò và đơn vị tổ chức. Nếu giá vốn được tìm thấy, các yếu tố chuyển đổi được dùng để chuyển đổi giá vốn sang đơn vị mà bạn đã chọn trên mô tả ước tính.

Nếu kết hợp vai trò và đơn vị tổ chức không trả lại giá vốn, thì hệ thống sẽ bỏ qua đơn vị tổ chức đó. Thay vào đó, hệ thống tìm kiếm kết hợp vai trò và đơn vị để đặt giá mặc định (sau khi bất cứ chuyển đổi nào được áp dụng).

Nếu hệ thống không tìm thấy giá cho vai trò, thì giá vốn trên mô tả ước tính được đặt thành giá mặc định **0,00**. Tất cả số tiền chi phí trên mô tả ước tính chi phí dự án được ghi theo đơn vị tiền tệ của tổ chức ký hợp đồng.

> [!NOTE]
> Theo mặc định, Microsoft Dynamics 365 lưu trữ số tiền chi phí theo đơn vị tiền tệ cơ sở của bạn. Tuy nhiên, số tiền chi phí hiển thị trên tab **Ước tính** trong đơn vị tiền tệ của đơn vị ký hợp đồng.  

### <a name="default-sales-price"></a>Giá bán hàng mặc định 

Bảng giá bán hàng được thực thể bán hàng mà dự án được gắn kèm hoặc khách hàng dự án xác định. Khi một thực thể bán hàng, chẳng hạn như cơ hội, báo giá hoặc hợp đồng liên kết với dự án, thì giá bán hàng của thực thể bán hàng được xác định bởi bảng giá liên kết với báo giá hoặc hợp đồng. Nếu báo giá hoặc hợp đồng có bảng giá tùy chỉnh, thì bảng giá đó sẽ dùng làm bảng giá bán hàng mặc định cho ước tính dự án. Nếu không có liên kết với thực thể bán hàng, bảng giá bán hàng mặc định từ các tham số được sử dụng như bảng giá bán hàng mặc định của dự án phù hợp với đơn vị tiền tệ của khách hàng được xác định trên dự án.

Mỗi mô tả ước tính có một đơn vị nguồn lực liên kết với mô tả đó. Đơn vị nguồn lực cho biết đơn vị tổ chức mà nguồn lực được đăng ký để hoàn thành nhiệm vụ. Để xác định giá bán hàng cho các vai trò liên kết, hãy tìm kiếm kết hợp vai trò, đơn vị và đơn vị nguồn lực trong bảng giá bán hàng. Nếu không có phân công trên nhiệm vụ, giá bán hàng cho nhiệm vụ này là 0,00.

Nếu kết hợp vai trò, đơn vị và đơn vị nguồn lực không trả lại giá bán hàng từ bảng giá bán hàng, thì hệ thống sẽ bỏ qua đơn vị đó. Thay vào đó, hệ thống tìm kiếm kết hợp chỉ có vai trò và đơn vị nguồn lực. Nếu giá bán hàng được tìm thấy, các yếu tố chuyển đổi được dùng để chuyển đổi giá vốn sang đơn vị mà bạn đã chọn trên mô tả ước tính bán hàng. 

Nếu kết hợp vai trò và đơn vị nguồn lực không trả lại giá bán hàng từ bảng giá bán hàng, thì hệ thống sẽ bỏ qua đơn vị nguồn lực đó. Thay vào đó, hệ thống tìm kiếm kết hợp vai trò và đơn vị để đặt giá mặc định (sau khi bất cứ chuyển đổi nào được áp dụng).

Nếu hệ thống không tìm thấy giá cho vai trò, thì giá bán hàng trên mô tả ước tính được đặt thành giá trị mặc định **0,00**.

Tab **Ước tính** có dạng xem lưới hiển thị mô tả ước tính. Lưới bao gồm các cột cho đơn vị, tổng giá vốn và tổng giá bán hàng như hiển thị trong hình minh họa sau. 

> ![Dạng xem lưới trên tab Ước tính.](media/project-6.png)

## <a name="time-phased-view-of-project-estimates"></a>Dạng xem theo giai đoạn thời gian cho ước tính dự án

Dạng xem theo giai đoạn thời gian của các ước tính dự án hiển thị dữ liệu ước tính từ dạng xem lưới trên dòng thời gian, trong quy mô thời gian mà bạn chọn. Theo mặc định, dữ liệu ước tính dựa trên tham số **Vai trò**.

> ![Dạng xem theo giai đoạn thời gian cho ước tính dự án.](media/project-7.png)

## <a name="allocating-estimated-effort-based-on-the-task-mode"></a>Phân bổ nhân công ước tính dựa trên chế độ nhiệm vụ

Trong dạng xem theo giai đoạn thời gian, bạn phân bổ tổng nhân công được ước tính cho nhiệm vụ bằng cách phân bổ giờ nhân công/giai đoạn thời gian cho đơn vị trong thang thời gian đã chọn. Chế độ nhiệm vụ xác định cách nhân công được phân bổ trên khoảng thời gian của nhiệm vụ. Hai loại phân bổ là **Ngang bằng** và **Dựa trên giờ làm việc**.

### <a name="work-hours-based-allocation"></a>Phân bổ dựa trên giờ làm việc
 
Trong chế độ tự động lập lịch nhiệm vụ, giờ làm việc mặc định hàng ngày cho các nguồn lực nhiệm vụ được đặt thành tỷ lệ giờ làm việc đầy đủ. Hành vi này áp dụng khi nhân công được phân bổ bằng cách phân chia trên khoảng thời gian của nhiệm vụ trong dạng xem theo giai đoạn thời gian. Ví dụ: nếu bạn ước tính nhiệm vụ sẽ được một nguồn lực hoàn thành trong thang thời gian **Ngày**, thì nhân công được phân bổ mỗi ngày sẽ không vượt quá giờ làm việc mỗi ngày được xác định trong lịch dự án. Vì vậy, việc phân bổ nhân công luôn đảm bảo rằng các nguồn lực được ước tính để sử dụng cho cả ngày.

### <a name="even-allocation"></a>Phân bổ đều

Trong chế độ nhiệm vụ được lập lịch theo cách thủ công, giờ làm việc từ lịch dự án không được sử dụng. Thay vào đó, lịch nhiệm vụ dựa trên đầu vào của người dùng. Với các nhiệm vụ này, phân bổ nhân công theo khoảng thời gian cho đơn vị trong thang thời gian đã chọn không có yếu tố hạn chế nào. Tổng nhân công trên một nhiệm vụ được chia và phân bổ đều cho mỗi khoảng thời gian đơn vị trong thang thời gian đã chọn. Do đó, chế độ nhiệm vụ được xác định trên nhiệm vụ xác định phân bổ nỗ lực hoặc phân bổ của nhân công/khoảng thời gian cho đơn vị trong ước tính theo giai đoạn thời gian.

## <a name="grouping-and-time-phasing-options"></a>Tùy chọn theo giai đoạn thời gian và phân nhóm

Dạng xem theo giai đoạn thời gian hiển thị phân bổ nhân công, chi phí và ước tính bán hàng trên cơ sở hàng ngày, hàng tuần, hàng tháng hoặc hàng năm. Theo mặc định, dữ liệu ước tính dựa trên tham số **Vai trò**. Tuy nhiên, bạn có thể dùng tùy chọn **Nhóm theo** để xoay vòng 2 tham số khác: **Thể loại** và **Nguồn lực**.

Trong cả dạng xem lưới và dạng xem theo giai đoạn thời gian, bạn có thể chọn các trường hiển thị. Tổng số cho mỗi khối thời gian hiển thị ở dưới cùng của dự án. Các số liệu này cho biết tổng số nhân công, chi phí và doanh số ước tính cho ngày, tuần, tháng hoặc năm. Giá vốn và giá bán hàng mặc định có hiệu lực theo ngày. Nói cách khác, các giá này thay đổi theo từng nguồn lực, dựa trên dạng xem theo giai đoạn thời gian mà bạn chọn.

## <a name="expense-estimates"></a>Ước tính chi phí

Nút **Thêm ước tính chi phí mới** trong dạng xem lưới cho phép bạn ghi lại mọi chi phí phát sinh trong dự án nhưng không liên quan trực tiếp tới lao động. Bạn có thể ghi lại các ước tính chi phí cho một nhiệm vụ cụ thể hoặc cho toàn bộ dự án. Chọn loại chi phí và ngày dự định khi bạn muốn chịu chi phí. Nếu bảng giá vốn và bảng giá bán hàng được liên kết có giá mặc định (hoặc nếu tỷ lệ tăng được xác định cho loại chi phí), các giá này tự động được nhập vào mô tả ước tính khi liên kết xuất hiện.


[!INCLUDE[footer-include](../includes/footer-banner.md)]