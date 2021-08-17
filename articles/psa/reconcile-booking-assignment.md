---
title: Điều hòa đăng ký và phân công
description: Chủ đề này cung cấp thông tin về số liệu thực tế.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 11/27/2019
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
ms.openlocfilehash: 264271a5be63cb2e51f175595a48bef5fbff0a42a37795c85dd5b4725deec35e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995157"
---
# <a name="reconcile-bookings-and-assignments"></a>Điều hòa đăng ký và phân công

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Đăng ký dự án và phân công nhiệm vụ dự án của thành viên nhóm dự án được kết hợp lỏng lẻo. Do đó, nguồn lực có thể có phân công nhiệm vụ không tương ứng với đăng ký và ngược lại. Tốt hơn hết, đăng ký và phân công dự án phải tương ứng để nguồn lực có năng lực cam kết để thực hiện các phân công nhiệm vụ của họ. Tuy nhiên, trong thực tế có thể có đăng ký dựa trên trạng thái rảnh/bận và thời gian nhiệm vụ có thể thay đổi khi dự án tiếp tục qua vòng đời của nó. Do đó, kết hợp lỏng lẻo này tạo ra sự linh hoạt.

Do việc kết hợp lỏng lẻo của đăng ký dự án và phân công nhiệm vụ, tab **Điều hòa** được đưa vào thực thể Dự án. Tab này giúp người quản lý dự án điều hòa đăng ký của các thành viên nhóm và phân công của họ cho nhóm dự án.

Đối với mỗi thành viên nhóm có tên, tab **Điều hòa** hiển thị đăng ký và phân công đến từng phân công nhiệm vụ riêng. Tab này hiển thị giờ trong các ô có thể thể hiện cho khoảng thời gian từ tháng đến ngày.

Trong tường **Thang thời gian**, bạn có thể chọn **Tháng**, **Tuần** hoặc **Ngày**. Theo mặc định, **Tuần** sẽ được chọn. Tuy nhiên, bạn có thể thay đổi giá trị mặc định bằng cách chọn nút **Thiết đặt**. Khi tab **Điều hòa** mở, tab này hiển thị ngày hiện tại, nhưng bạn có thể dùng điều khiển lịch để di chuyển tiến hoặc lùi theo thời gian. Khi dự án có ngày bắt đầu trong tương lai, tab hiển thị ngày đó khi ngày được mở. Điều khiển lịch cũng có các tùy chọn cho phép bạn di chuyển đến ngày bắt đầu và kết thúc dự án.

Bạn có thể sử dụng điều khiển trình mở rộng trên mỗi nguồn lực để hiển thị chi tiết của đăng ký nguồn lực. Bạn cũng có thể mở rộng phân công của mỗi nguồn lực đến cấp nhiệm vụ riêng.

Ở cuối tab **Điều hòa** hiển thị tổng số ròng tổng thể cho dự án và tab này cũng chứa cột tổng. Đối với mỗi nguồn lực, tab này tính sự chênh lệch giữa đăng ký của thành viên nhóm trên dự án và tổng số phân công nhiệm vụ của thành viên nhóm đó. Chênh lệch lý tưởng nhất là 0 (không). Nói cách khác, không nên có sự chênh lệch giữa đăng ký và phân công nhiệm vụ của nguồn lực. Mọi chênh lệch được chỉ ra bằng màu và bóng để gọi 2 trạng thái sau:

- **Thiếu đăng ký** – Thiếu đăng ký xảy ra khi nguồn lực có nhiều phân công hơn đăng ký. Do năng lực của nguồn lực này không được đăng ký trước nên người quản lý dự án có thể chỉnh sửa trạng thái này bằng cách mở rộng đăng ký của nguồn lực để trang trải thâm hụt.
- **Đăng ký vượt mức** – Đăng ký vượt mức có thể xảy ra khi nguồn lực được đăng ký cho dự án nhưng không được phân công cho nhiệm vụ. Trạng thái này có thể chấp nhận được nếu, ví dụ: nguồn lực được đăng ký trước khi được phân công nhiệm vụ. Tuy nhiên, trong các trường hợp khác, nguồn lực có thể không được lên kế hoạch phân công nhiệm vụ. Trong những trường hợp này, người quản lý dự án nên xem xét hủy bỏ các đăng ký của nguồn lực để năng lực đó có thể dùng cho dự án khác.

> [!NOTE]
> Chú thích cho những trạng thái này có thể bị ẩn để nhường chỗ cho lưới. Trong trường hợp này, bạn có thể hiển thị chú thích bằng cách chọn nút **Thiết đặt**.

Trong một số trường hợp, khi trường **Thang thời gian** được đặt thành mức cao hơn **Ngày**, thì chênh lệch có thể được tính bằng 0 (không). Ví dụ: ở cấp **Tháng**, chênh lệch thực cho nguồn lực có thể bằng 0 (không) để chỉ ra đăng ký bằng phân công. Tuy nhiên, nếu thấy cấp **Tuần**, bạn có thể thấy 0 (không) giờ phân công và 40 giờ đăng ký trong tuần đầu tiên của tháng, và 40 giờ phân công và 0 (không) giờ đăng ký trong tuần thứ hai của tháng. Mặc dù tổng số đăng ký và phân công cho tháng bằng nhau nhưng sẽ khác nhau theo tuần.

Khi bạn thấy cấp thời gian cao hơn, tab **Điều hòa** hiển thị các chỉ báo cho thông báo cho bạn biết rằng có sự khác biệt giữa các cấp thời gian thấp hơn. Ví dụ, trong hình minh họa sau đây, một chỉ báo ô xuất hiện trong ô cho tháng 10 năm 2018 cho nguồn lực có tên là Đỗ Ngọc Bích. Do đó, bạn có thể thấy rằng mặc dù đăng ký và phân công của nguồn lực tương đương khi chúng được tổng hợp ở cấp **Tháng**, nhưng chúng không khớp ở các cấp thấp hơn.

![Các mục đặt trước và chỉ định không khớp ở cấp độ hàng tháng.](media/reconcile-assignments-01.JPG)

Bấm đúp vào một ô để phóng to đến cấp thấp hơn tiếp theo và xem sự khác biệt. Ví dụ, nếu bấm đúp vào chênh lệch tháng 10 năm 2018 cho Đỗ Ngọc Bích, bạn có thể xem chi tiết cấp **Tuần**. Sau đó, bạn có thể thấy nguồn lực có 16 giờ đăng ký nhưng không có phân công trong 2 tuần đầu tiên của tháng 10, và 16 giờ phân công nhưng không có đăng ký trong tuần thứ ba của tháng 10.

![Các mục đặt trước và chỉ định không khớp ở cấp độ hàng tuần.](media/reconcile-assignments-02.JPG)

Bạn có thể bấm chuột phải vào một ô để thu nhỏ cấp cao hơn tiếp theo. Bạn cũng có thể tắt chỉ báo ô bằng cách chọn nút **Thiết đặt**. 

Bạn cũng có thể dùng các nút **Trước** và **Tiếp theo** trên lưới để di chuyển qua mọi chênh lệch trong dự án. Để sử dụng các nút này, trước tiên bạn phải chọn một nguồn lực. Chọn **Tiếp theo** để di chuyển đến chênh lệch tiếp theo giữa đăng ký và phân công cho nguồn lực đó. Chọn **Trước đó** để chuyển về chênh lệch trước đó.

Trong các trường hợp có phân công nhiệm vụ cho nguồn lực nhưng không có đăng ký, bạn có thể chọn thiếu đăng ký rồi chọn **Mở rộng đăng ký**, Sau đó, bạn có thể xem đăng ký cần thiết để giải quyết tình trạng thiếu của nguồn lực. Bạn cũng có thể xem đăng ký trên dự án hiện tại và các dự án khác. Chọn **OK** để tạo đăng ký cho nguồn lực mà không có trạng thái rảnh/bận hiện tại. Sau đó, người quản lý dự án hoặc người quản lý nguồn lực có thể dùng Bảng lịch trình để quản lý tình huống mà nguồn lực bị đăng ký quá mức so với năng lực do đăng ký của họ được mở rộng.

## <a name="managing-with-time-zones"></a>Quản lý theo múi giờ
Để đảm bảo kết quả chính xác và có thể dự đoán được khi sử dụng Gia hạn đăng ký, có hai điều kiện tiên quyết chính phải được đáp ứng:  

- Người dùng phải đặt cấu hình múi giờ của thiết bị của họ để khớp với múi giờ được xác định trong Cài đặt cá nhân hóa hệ thống của bạn.
 
  ![Cài đặt múi giờ trong Windows 10.](media/reconcile-assignments-03.png)

  ![Cài đặt múi giờ trong cài đặt cá nhân hóa.](media/reconcile-assignments-04.png)
 
- Tài nguyên có thể đặt trước phải có ít nhất một phút thời gian làm việc trùng với các phân phối được sử dụng để xác định gia hạn được yêu cầu. Chẳng hạn ví dụ sau đây cho thấy các tài nguyên đánh giá với giờ làm việc rơi vào khoảng từ 9:00 giờ sáng đến 7:00 giờ tối. 

  ![So sánh phân phối tài nguyên.](media/reconcile-assignments-05.png)

Bảng sau đây hiển thị:

- Mẫu lịch dự án.
- Nguồn lực A: Tài nguyên này có cùng lịch và nằm trong cùng múi giờ với dự án. Thời gian bắt đầu của các đăng ký sẽ là 9:00 giờ sáng.
- Nguồn lực B: Tài nguyên này nằm ở múi giờ khác với dự án và do đó bắt đầu lúc 7:00 giờ sáng theo múi giờ của họ. Tuy nhiên, việc đăng ký sẽ bắt đầu lúc 9:00 giờ sáng vì đó là thời gian bắt đầu sớm nhất của phân phối giờ làm việc theo phân công.
- Nguồn lực C và D: Các tài nguyên cũng được đặt ở các múi giờ khác nhau, cả hai khác nhau và khác với dự án, và việc đăng ký bắt đầu không sớm hơn thời gian bắt đầu có sẵn tương ứng.

|Thực thể  |Lịch  |
|-|-|
|Mẫu lịch dự án   | ![lịch dự án.](media/reconcile-assignments-06.png) |
|Nguồn lực A  | ![Lịch nguồn lực A.](media/reconcile-assignments-06.png) |
|Nguồn lực B  |  ![Lịch nguồn lực B.](media/reconcile-assignments-07.png) |
|Nguồn lực C  |  ![Lịch nguồn lực C.](media/reconcile-assignments-08.png) |
|Nguồn lực D  | ![Lịch nguồn lực D.](media/reconcile-assignments-09.png)  |
 
Khi bạn chuyển đến dạng xem điều hòa, các phân công nguồn lực và thiếu hụt đăng ký có liên quan sẽ hiển thị.
 ![Dạng xem điều hòa trước khi gia hạn.](media/reconcile-assignments-10.png)

Sau khi chức năng Gia hạn đăng ký đã được thực thi trên mỗi nguồn lực, đăng ký sẽ được gia hạn thành công cho mỗi nguồn lực. Điều này là do giờ làm việc của mỗi nguồn lực chồng chéo với phân phối giờ làm việc thiếu hụt.
 ![Dạng xem điều hòa sau khi gia hạn đăng ký.](media/reconcile-assignments-11.png) 

Tuy nhiên, xem xét kỹ hơn các chi tiết của các đặt phòng cho thấy sự khác biệt trong thời gian bắt đầu của các đăng ký. Đăng ký sẽ bắt đầu không sớm hơn thời gian bắt đầu phân phối giờ làm việc theo phân công và không sớm hơn thời gian bắt đầu có sẵn của nguồn lực.
 ![Các đăng ký nguồn lực mới trong bảng lịch trình.](media/reconcile-assignments-12.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]