---
title: Quản lý nguồn lực
description: Chủ đề này cung cấp thông tin về cách bạn có thể quản lý nguồn lực.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 05/13/2019
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
ms.openlocfilehash: 548ee7db1c8ca14f1b88d76a534d2922549eba138659e67a84cd89e6f7ee2170
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/06/2021
ms.locfileid: "6998532"
---
# <a name="manage-resources"></a>Quản lý nguồn lực

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation bao gồm một bảng thông tin cho người quản lý nguồn lực cung cấp tổng quan trực quan về nhu cầu nguồn lực và thời gian làm việc trong toàn tổ chức. Bạn có thể dùng biểu đồ trên bảng thông tin này để hình dung thông tin sau:

- **Nhu cầu nguồn lực** – Biểu đồ **Yêu cầu nguồn lực hiện hoạt** cho biết các nguồn lực đã được gửi. Các nguồn lực được tổng hợp theo vai trò hoặc dự án.
- **Nhu cầu nguồn lực chưa được gửi** – Biểu đồ **Nhu cầu nguồn lực chưa được gán** cho biết tất cả yêu cầu nguồn lực chưa được gửi. Biểu đồ này giúp người quản lý nguồn lực xem nhu cầu chưa chắc chắn và có thể được gửi thông qua yêu cầu nguồn lực.
- **Thời gian làm việc tính phí cho tuần qua** – Biểu đồ **Thời gian làm việc theo vai trò** hiển thị tỷ lệ thời gian làm việc tính phí thực tế của tổ chức theo vai trò so với thời gian làm việc tính phí mục tiêu của tổ chức theo vai trò.

    > [!NOTE]
    > Để chia sẻ biểu đồ **Thời gian làm việc theo vai trò**, hãy tạo một công việc chạy quy trình làm việc UpdateRoleUtilization. Công việc định kỳ này chạy 7 ngày 1 lần để tính thời gian làm việc tính phí cho 7 ngày trước đó. Kết quả được tổng hợp theo vai trò.

## <a name="manage-project-team-members"></a>Quản lý thành viên nhóm dự án

Người quản lý dự án có thể dùng bảng thông tin cho người quản lý dự án để quản lý nguồn lực trên dự án. Ví dụ: họ có thể thêm trực tiếp thành viên nhóm vào một dự án và đặt thành viên nhóm hoàn thành các yêu cầu nguồn lực được nguồn lực chung ghi lại.

### <a name="add-a-team-member-directly-to-a-project"></a>Thêm trực tiếp thành viên nhóm vào một dự án

Để thêm trực tiếp một thành viên nhóm vào dự án, trên trang **Dự án**, trên tab **Nhóm**, hãy chọn **Mới**. Hộp thoại **Tạo nhanh: Thành viên nhóm dự án** xuất hiện. Trong hộp thoại này, bạn có thể thực hiện các tác vụ sau:

- **Đặt một nguồn lực có tên** – Trong trường **Nguồn lực có thể đăng ký**, hãy chọn tên nguồn lực. Sau đó, chọn vai trò, thiết lập khoảng thời gian rồi chọn một phương pháp phân bổ. Nguồn lực có tên mà bạn đã chọn được thêm vào dự án bằng phương pháp phân bổ đã chọn và lịch nguồn lực.
- **Thêm nguồn lực chung** – Để trống trường **Tài nguyên có thể đăng ký**, sau đó chọn vai trò, chọn khoảng thời gian rồi chọn phương pháp phân bổ ưa thích. Nguồn lực chung được thêm vào nhóm ở dạng chỗ dành sẵn để giữ mẫu nhu cầu dùng để đặt nguồn lực có tên trong nhóm. Yêu cầu được thực hiện theo lịch dự án.
- **Thêm nguồn lực có tên vào nhóm mà không dùng năng lực của nguồn lực** – Trong trường **Nguồn lực có thể đăng ký**, hãy chọn một nguồn lực. Sau đó, chọn khoảng thời gian rồi chọn **Không** làm phương pháp phân bổ. Nguồn lực được thêm vào nhóm nhưng năng lực của nguồn lực không bị hao tốn khi đăng ký.

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a>Đăng ký một thành viên nhóm để thực hiện các yêu cầu nguồn lực cho nguồn lực chung

Trong PSA, bạn có thể đăng ký một nguồn lực chung trên nhóm dự án và có thể chỉ rõ vai trò, năng lực cần thiết và cách năng lực được phân bổ. Trên yêu cầu nguồn lực, bạn có thể chỉ định các thuộc tính liên kết với nguồn lực chung. Các thuộc tính này bao gồm các kỹ năng cần thiết, đơn vị tổ chức ưa thích và nguồn lực ưa thích.

Hãy làm theo các bước sau để chỉ định kỹ năng cần thiết trên nguồn lực chung cho nhà phát triển.

1. Trên trang **Dự án**, trên tab **Nhóm**, hãy chọn **Mới** để đăng ký nguồn lực chung.

    ![Nguồn lực chung đã đăng ký trong nhóm.](media/Resource-Management-image9.png)

2. Trong dạng xem **Tất cả thành viên nhóm**, trong cột **Yêu cầu nguồn lực**, hãy chọn liên kết để thêm kỹ năng cần thiết cho nguồn lực chung.

    ![Liên kết yêu cầu.](media/Resource-Management-image10.png)

3. Trên trang **Yêu cầu nguồn lực** xuất hiện, trong lưới **Kỹ năng**, hãy chọn dấu chấm lửng (**...**), sau đó chọn **Thêm đặc điểm yêu cầu mới** để thêm các kỹ năng cần thiết cho nhà phát triển của bạn.

    ![Lệnh Thêm đặc điểm yêu cầu mới.](media/Resource-Management-image11.png)

4. Trong hộp thoại **Tạo nhanh: Đặc điểm yêu cầu** xuất hiện, trong trường **Đặc điểm**, chọn kỹ năng cần thiết. Sau đó, trong trường **Giá trị xếp hạng**, hãy chọn mức độ thành thạo cho kỹ năng đó. Cuối cùng, trong trường **Yêu cầu nguồn lực**, hãy đặt yêu cầu thành nguồn lực nguồn từ đơn vị tổ chức hoặc thậm chí là nguồn lực có tên. Sau khi hoàn tất, hãy chọn **Lưu**.

    ![Hộp thoại Tạo nhanh: Đặc điểm yêu cầu.](media/Resource-Management-image12.png)

5. Trên trang **Yêu cầu nguồn lực**, hãy chọn **Đăng ký** để thực hiện yêu cầu nguồn lực.

    ![Nút Đăng ký trên trang Yêu cầu nguồn lực.](media/Resource-Management-image13.png)

    Bạn cũng có thể chọn nguồn lực chung trong lưới **Tất cả thành viên nhóm** rồi chọn **Đăng ký**.

    ![Nút Đăng ký dưới lưới Tất cả thành viên nhóm.](media/Resource-Management-image14.png)

    > [!NOTE]
    > Trong ví dụ này, có 40 giờ yêu cầu nhưng không có giờ đã đăng ký thực tế vì nguồn lực chung không có đăng ký. Ngoài ra, không có giờ được gán, vì nguồn lực chung được thêm trực tiếp vào nhóm. Nguồn lực không được thêm bằng cách phân công nhiệm vụ.

    Trên trang **Trợ lý lập lịch biểu**, bạn có thể lọc các nguồn lực có sẵn theo yêu cầu được chỉ định trên yêu cầu nguồn lực. Nguồn lực được sắp xếp theo các tham số sắp xếp đã chỉ định trên Bảng lịch trình.

    ![Trang Trợ lý lập lịch biểu.](media/Resource-Management-image15.png)

    Dưới đây là một số bộ lọc thường dùng:

    - **Đặc điểm cùng với xếp hạng** – Lọc theo kỹ năng, chứng nhận và các năng lực khác của nguồn lực, ngoài xếp hạng mức độ thành thạo.
    - **Vai trò** – Lọc theo các vai trò mặc định được gán cho các nguồn lực có thể đăng ký.
    - **Đơn vị tổ chức** – Lọc nguồn lực có thể đăng ký theo đơn vị tổ chức mà các nguồn lực này được phân công đến.

6. Nếu không hài lòng với kết quả tìm kiếm yêu cầu ban đầu, bạn có thể thay đổi tiêu chí lọc. Mở rộng ngăn **Dạng xem lọc** ở bên trái, sau đó chọn **Tìm kiếm** để tìm các nguồn lực bổ sung.

    ![Ngăn Dạng xem lọc.](media/Resource-Management-image16.png)

7. Để thay đổi cách kết quả được sắp xếp, hãy chọn **Sắp xếp**.

    ![Lệnh sắp xếp.](media/Resource-Management-image17.png)

8. Chọn nguồn lực theo nhu cầu được chỉ rõ trên yêu cầu, như đã nêu ở phần đầu lưới. Bạn có thể xóa lựa chọn các ô trong lưới và để năng lực của nguồn lực đó ở trạng thái mở. Chỉ có thể chọn từng nguồn lực một khi đăng ký.

9. Chọn **Đăng ký** để đăng ký nguồn lực đã chọn và để Bảng lịch trình ở trạng thái mở để bạn có thể chọn thêm nguồn lực. Ngoài ra, hãy chọn **Đăng ký và thoát** để đăng ký nguồn lực đã chọn và đóng Bảng lịch trình.

    ![Nguồn lực cần đăng ký.](media/Resource-Management-image19.png)

    Bạn nhận được thông báo về giờ đã đăng ký. Các chỉ số nhu cầu cho thấy lượng yêu cầu đăng ký được thỏa mãn và lượng còn lại. Bạn cũng có thể xem lượng tiêu thụ của năng lực của nguồn lực đã chọn. Chọn **Bung rộng** để xem thêm thông tin chi tiết về đăng ký nguồn lực.

9. Quay lại dạng xem **Tất cả thành viên**. Trong lưới, thông báo rằng nguồn lực chung đã được thay thế bằng nguồn lực có tên và 40 giờ được liệt kê là đã đăng ký cho nguồn lực đó.

    ![Lưới Tất cả thành viên nhóm đã cập nhật.](media/Resource-Management-image20.png)

    > [!NOTE]
    > Không có giờ đã phân công nào hiển thị vì nguồn lực được đăng ký trực tiếp trên nhóm. Các nguồn lực không được đăng ký bằng phân công nhiệm vụ.

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a>Phân công nhiệm vụ cho nguồn lực chung và tạo yêu cầu nguồn lực

Trong PSA, bạn có thể tạo các nhiệm vụ, sau đó phân công nguồn lực chung cho các nhiệm vụ đó. Bằng cách này, nhu cầu nguồn lực có thể được chỗ dành sẵn đại diện khi bạn ước tính số tài chính và lịch trình của mình. Sau đó, bạn có thể tạo yêu cầu nguồn lực cho nguồn lực chung và thực hiện các yêu cầu đó.

1. Trên trang **Dự án**, trên tab **Lịch trình**, hãy chọn **Thêm** để tạo nhiệm vụ.

    ![Nhiệm vụ mới được tạo.](media/Resource-Management-image21.png)

2. Trong trường **Nguồn lực**, hãy chọn biểu tượng **Bộ chọn nguồn lực**. Bộ chọn nguồn lực xuất hiện và hiển thị thành viên nhóm hiện tại cho dự án.

    ![Bộ chọn nguồn lực.](media/Resource-Management-image22.png)

3. Nhập tên của nguồn lực chung mới rồi chọn **Tạo**.

    ![Tên của nguồn lực chung mới đã tạo.](media/Resource-Management-image23.png)

4. Trong hộp thoại **Tạo nhanh: Thành viên nhóm dự án** xuất hiện, trong trường **Vai trò**, hãy chọn vai trò cho nguồn lực chung. Trong trường **Đơn vị nguồn lực**, hãy chọn đơn vị tổ chức cho nguồn lực chung. Tiếp đó, chọn **Lưu**.

    ![Hộp thoại Tạo nhanh: Thành viên nhóm dự án.](media/Resource-Management-image24.png)

    Thành viên nhóm chung hiện được phân công cho nhiệm vụ.

    ![Thành viên nhóm chung được phân công cho nhiệm vụ.](media/Resource-Management-image25.png)

    Trên tab **Nhóm**, bạn sẽ thấy thành viên nhóm chung mới. Lưu ý rằng nó chỉ có giờ được phân công. Các giờ này là tổng tất cả nhiệm vụ được phân công cho thành viên nhóm chung. Thành viên nhóm chung chưa có giờ yêu cầu hoặc yêu cầu nguồn lực.

    ![Thành viên nhóm chung trên tab Nhóm.](media/Resource-Management-image26.png)

5. Bạn hiện có thể phân công thành viên nhóm chung cho các nhiệm vụ khác bằng Bộ chọn nguồn lực.

    ![Thành viên nhóm chung trong Bộ chọn nguồn lực.](media/Resource-Management-image27.png)

    Khi đã hoàn tất việc phân công nguồn lực chung cho các nhiệm vụ, bạn có thể tạo yêu cầu nguồn lực cho nguồn lực chung.

5. Trên tab **Nhóm**, hãy chọn nguồn lực chung rồi chọn **Tạo yêu cầu**.

    ![Lệnh Tạo yêu cầu.](media/Resource-Management-image28.png)

    Khi yêu cầu được tạo, thành viên nhóm chung sẽ có giờ yêu cầu và liên kết cho yêu cầu nguồn lực.

    ![Liên kết yêu cầu nguồn lực.](media/Resource-Management-image29.png)

    Sau khi bạn đăng ký nguồn lực có tên, nguồn lực chung bị xóa khỏi nhóm và được thay thế bằng nguồn lực có tên.

    ![Nguồn lực chung được thay thế bằng nguồn lực có tên.](media/Resource-Management-image30.png)

    Trên tab **Lịch trình**, phân công nguồn lực chung bị xóa và thay thế bằng nguồn lực có tên.

    ![Phân công nguồn lực chung được thay thế bằng nguồn lực có tên trên tab Lịch trình.](media/Resource-Management-image31.png)

    > [!NOTE]
    > Hành vi này chỉ xảy ra khi nguồn lực có tên được đăng ký đầy đủ cho yêu cầu nguồn lực chung. Chọn nguồn lực có tên thay thế một phần cho yêu cầu nguồn lực chung hoặc nhiều nguồn lực có tên thay thế cho yêu cầu nguồn lực chung, nguồn lực chung vẫn được phân công cho nhiệm vụ.

    Trong hình minh họa sau, một nhiệm vụ 80 giờ được lên kế hoạch trong thời gian 5 ngày (16 giờ/ngày trong 5 ngày) và được phân công cho nguồn lực chung có tên **Chức năng**.

    ![Nhiệm vụ 80 giờ, 5 ngày được phân công cho nguồn lực chung Chức năng.](media/Resource-Management-image32.png)

    Khi bạn tạo yêu cầu, đó sẽ là yêu cầu 80 giờ trong 5 ngày.

    ![Yêu cầu được tạo ra cho 80 giờ trong 5 ngày.](media/Resource-Management-image33.png)

    Vì các nguồn lực có sẵn chỉ làm việc 8 giờ/ngày nên sẽ cần 2 nguồn lực để đáp ứng yêu cầu.

    ![Nguồn lực thứ hai.](media/Resource-Management-image35.png)

    Trên tab **Nhóm**, bạn hiện có thể thấy nguồn lực chung không có giờ yêu cầu, nhưng giờ được phân công vẫn xuất hiện cùng với 2 nguồn lực có tên thực hiện.

    ![2 nguồn lực có tên trên tab Nhóm.](media/Resource-Management-image36.png)

    Trên tab **Lịch trình**, nguồn lực chung vẫn được phân công cho nhiệm vụ.

    ![Nguồn lực chung trên tab Lịch trình.](media/Resource-Management-image37.png)

PSA không phân công cả hai nguồn lực cho nhiệm vụ, vì hành vi đó sẽ tạo ra lịch trình khó dự đoán. Trong ví dụ đơn giản này, thật dễ dàng để chia các giờ bằng nhau giữa hai nguồn lực. Tuy nhiên, trong trường hợp phức tạp hơn liên quan đến nhiều nhiệm vụ và nhiều nguồn lực, PSA sẽ phải đưa ra giả định về cách nó sẽ phân bổ các đăng ký nhận được cho nhiều nguồn lực trên nhiều nhiệm vụ.

Do đó, trong các trường hợp này, người quản lý dự án phụ trách việc phân tích nhiều đăng ký và phân công các đăng ký đó nếu cần. Để phân bổ các đăng ký, người quản lý dự án phân công các nhiệm vụ từ nguồn lực chung đến nguồn lực có tên, sau đó sử dụng dạng xem **Điều hòa** để đảm bảo phân bổ hoạt động với đăng ký.

### <a name="edit-a-resource-requirement"></a>Chỉnh sửa yêu cầu nguồn lực

Sau khi yêu cầu nguồn lực được tạo, người quản lý dự án hoặc người quản lý nguồn lực có thể muốn chỉnh sửa thông tin chi tiết để tinh chỉnh tiêu chí tìm kiếm khi Bảng lịch trình được dùng. Để chỉnh sửa yêu cầu nguồn lực, hãy làm theo các bước sau.

1. Trên trang **Dự án**, trên tab **Nhóm**, hãy chọn liên kết đến bất kỳ yêu cầu nào trên nguồn lực chung.
2. Trên trang **Yêu cầu nguồn lực** xuất hiện, bạn có thể cập nhật một số thuộc tính. Dưới đây là một số ví dụ:

    - Tên
    - Từ Ngày
    - Đến Ngày
    - Khoảng thời gian
    - Loại Nguồn lực

Trên trang **Yêu cầu nguồn lực**, người quản lý dự án hoặc người quản lý nguồn lực cũng có thể xác định thông tin sau:

- Kỹ năng
- Vai trò
- Các tùy chọn nguồn lực
- Đơn vị tổ chức ưu tiên

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a>Cập nhật đăng ký nguồn lực sau khi chúng được đăng ký trên dự án

Sau khi thêm nguồn lực chung hoặc có tên vào nhóm dự án, bạn có thể thay đổi đăng ký của nguồn lực.

1. Trên trang **Dự án**, trên tab **Nhóm**, hãy chọn thành viên nhóm rồi chọn **Duy trì đăng ký**.

    ![Bảng lịch trình mở cho thành viên nhóm đã chọn.](media/Resource-Management-image40.png)

    Bảng lịch trình xuất hiện và hiển thị các đăng ký của thành viên nhóm dự án. Mở rộng hồ sơ của thành viên nhóm để xem những giờ đã được đặt với dự án này và các dự án khác đang sử dụng năng lực của thành viên nhóm.

2. Chọn và kéo đăng ký để mở rộng hoặc thu gọn. Hộp thoại **Tạo đăng ký nguồn lực** xuất hiện cho phép bạn điều chỉnh đăng ký.

    ![Hộp thoại Tạo đăng ký nguồn lực.](media/Resource-Management-image41.png)

3. Bấm chuột phải vào đăng ký. Sau đó, bạn có thể dùng menu phím tắt để hoàn thành các hành động sau:

    - Thay đổi trạng thái đăng ký.
    - Chỉnh sửa đăng ký.
    - Thay thế nguồn lực trên nhóm dự án.

### <a name="change-the-booking-status"></a>Thay đổi trạng thái đăng ký

Bạn có thể thay đổi bất kỳ trạng thái đăng ký mặc định hoặc tùy chỉnh nào.

![Lệnh Thay đổi trạng thái.](media/Resource-Management-image42.png)

Các trạng thái sau có trong PSA:

- **Đã hủy** – Trạng thái này hủy đăng ký của nguồn lực và giải phóng năng lực của nguồn lực.
- **Đăng ký chắc chắn** – Trạng thái này chiếm năng lực của nguồn lực. Đăng ký thường có trạng thái này khi bạn mở **Duy trì đăng ký** từ lưới **Tất cả thành viên nhóm** trên trang **Dự án**.
- **Đăng ký không chắc chắn** – Trạng thái này thêm nguồn lực vào nhóm nhưng không chiếm năng lực của nguồn lực. Trạng thái này cho biết nguồn lực đã được dự trữ cho công việc tiềm năng nhưng vẫn có năng lực nếu công việc khác cần. Trong dạng xem tổng quan về trạng thái rảnh/bận của nguồn lực, đăng ký không chắc chắn có trạng thái khác với đăng ký chắc chắn.
- **Đã đề xuất** – Trạng thái này thể hiện nguồn lực được người quản lý nguồn lực hoặc người quản lý dự án đề xuất. Đề xuất không chiếm năng lực của nguồn lực và nguồn lực không được thêm vào nhóm dự án. Để đăng ký nguồn lực đó trên nhóm một cách chắc chắn, người quản lý dự án phải chấp nhận đề xuất.

### <a name="submit-resource-requests"></a>Gửi yêu cầu nguồn lực

Yêu cầu nguồn lực dùng để thực hiện nhu cầu (yêu cầu nguồn lực) phải được người quản lý nguồn lực thực hiện. Đối với nguồn lực chung đã có trong nhóm, bạn có thể gửi trực tiếp yêu cầu nguồn lực. Yêu cầu nguồn lực có thể được thực hiện theo hai cách:

- Người quản lý nguồn lực trực tiếp đáp ứng yêu cầu. Trong trường hợp này, nguồn lực chung được thay thế bằng đăng ký chắc chắn có nguồn lực có tên.
- Người quản lý nguồn lực đề xuất nguồn lực cho người quản lý dự án và người quản lý dự án phê duyệt hoặc từ chối nguồn lực được đề xuất.

#### <a name="direct-fulfillment-of-resource-requests"></a>Thực hiện trực tiếp yêu cầu nguồn lực

Khi yêu cầu nguồn lực được tạo, người quản lý dự án có thể gửi yêu cầu nguồn lực cho nguồn lực chung bằng cách chọn nguồn lực, sau đó chọn **Gửi yêu cầu**.

![Nút Gửi yêu cầu.](media/Resource-Management-image45.png)

Nhận xét về nguồn lực có thể được cung cấp cho người quản lý nguồn lực đang thực hiện yêu cầu. Sau khi yêu cầu được gửi, trường **Trạng thái** cho thành viên nhóm được thay đổi thành **Đã gửi**.

![Nhập nhận xét tùy chọn.](media/Resource-Management-image46.png)

Khi người quản lý nguồn lực đáp ứng yêu cầu, thành viên nhóm chung được thay thế bằng nguồn lực có tên trong lưới **Tất cả thành viên nhóm**.

![Thành viên nhóm chung được thay thế bằng nguồn lực có tên trong lưới Tất cả thành viên nhóm.](media/Resource-Management-image47.png)

#### <a name="use-a-resource-proposal-for-resource-requests"></a>Sử dụng đề xuất nguồn lực cho yêu cầu nguồn lực

Người quản lý nguồn lực có thể đề xuất nguồn lực cho người quản lý dự án thay vì trực tiếp đăng ký nguồn lực trên yêu cầu nguồn lực. Người quản lý nguồn lực có thể dùng tùy chọn này khi không có kết hợp chính xác cho yêu cầu. Khi người quản lý nguồn lực đề xuất nguồn lực, người quản lý dự án sẽ thấy trường **Trạng thái** cho thành viên nhóm chung được thay đổi thành **Cần đánh giá**.

![Trạng thái của thành viên nhóm chung thay đổi thành Cần đánh giá.](media/Resource-Management-image48.png)

Để xem nguồn lực được đề xuất cùng với trực quan hóa hiệu ứng đăng ký của đề xuất, hãy bấm đúp vào thành viên nhóm có trạng thái **Cần đánh giá**. Sau đó, chọn tab **Nguồn lực được đề xuất**.

![Tab Nguồn lực được đề xuất.](media/Resource-Management-image49.png)

Chọn **Chấp nhận tất cả đề xuất** để chấp nhận tất cả nguồn lực được đề xuất hoặc **Từ chối tất cả đề xuất** để từ chối các nguồn lực đó. Nếu bạn chấp nhận các nguồn lực được đề xuất, thì các nguồn lực này được đăng ký chắc chắn trên dự án ở dạng thành viên nhóm và thay thế nguồn lực chung.

> [!NOTE]
> Bạn phải chấp nhận hoặc từ chối tất cả nguồn lực được đề xuất. Bạn không thể chấp nhận một phần hoặc từ chối các nguồn lực này.

### <a name="substitute-a-resource-on-the-project-team"></a>Thay thế nguồn lực trên nhóm dự án

Đôi khi, người quản lý dự án phải thay thế một thành viên nhóm đã đăng ký trên một dự án.

1. Trong trang **Dự án**, trên tab **Nhóm**, hãy chọn nguồn lực cần thay thế rồi chọn **Duy trì đăng ký**.
2. Bung rộng nguồn lực để xem các dự án mà nguồn lực này được phân công.

    ![Nguồn lực được bung rộng để hiển thị các dự án được phân công.](media/Resource-Management-image50.png)

3. Bấm chuột phải vào dự án rồi chọn **Thay thế nguồn lực**.
4. Nếu bạn biết nguồn lực mà bạn muốn thay thế cho nguồn lực hiện tại, hãy chọn hoặc nhập tên rồi chọn **Phân công lại**.

    ![Chỉ định nguồn lực thay thế.](media/Resource-Management-image51.png)

    Ngoài ra, hãy làm theo các bước sau để tìm kiếm nguồn lực:

    1. Chọn **Tìm mục thay thế**.

        ![Tìm kiếm nguồn lực thay thế.](media/Resource-Management-image52.png)

        Trợ lý lập lịch biểu trả về danh sách các thay thế có sẵn. Trong Trợ lý lập lịch biểu, bạn có thể lọc thêm các nguồn lực có sẵn để tìm mục thay thế thích hợp.

        ![Danh sách mục thay thế có sẵn.](media/Resource-Management-image53.png)

    2. Để thay thế nguồn lực, hãy chọn nguồn lực mà bạn muốn rồi chọn **Thay thế**.

        ![Nguồn lực thay thế đã chọn.](media/Resource-Management-image54.png)

    Đăng ký và phân công được thay thế bằng nguồn lực mới.

    ![Đăng ký và phân công được thay thế bằng nguồn lực mới.](media/Resource-Management-image55.png)

## <a name="reconcile-team-member-bookings-and-assignments"></a>Điều hòa phân công và đăng ký thành viên nhóm

Đối với các thành viên nhóm, đăng ký và phân công được kết hợp lỏng lẻo. Nói cách khác, nguồn lực có thể có phân công nhưng không có đăng ký hoặc ngược lại. Tốt hơn hết, đăng ký nên phù hợp với phân công để các nguồn lực có năng lực được cam kết có thể thực hiện các phân công nhiệm vụ. Tuy nhiên, đăng ký có thể dựa trên trạng thái rảnh/bận và thời gian nhiệm vụ có thể thay đổi khi dự án tiếp tục. Do đó, việc kết hợp lỏng lẻo đăng ký và phân công mang đến sự linh hoạt.

PSA có tab **Điều hòa** cho phép người quản lý dự án điều hòa đăng ký và phân công của thành viên nhóm cho dự án.

![Tab Tổng hợp.](media/Resource-Management-image56.png)

Tab **Điều hòa** hiển thị đăng ký và phân công đến mức phân công nhiệm vụ cá nhân cho từng thành viên nhóm. Tab này hiển thị giờ trong các ô thể hiện cho khoảng thời gian từ tháng đến ngày.

Tab này cũng hiển thị tổng số ròng tổng thể cho dự án, cùng với cột tổng.

Đối với mỗi nguồn lực, tab này tính toán khác biệt giữa đăng ký của thành viên nhóm và tổng số phân công nhiệm vụ của thành viên nhóm đó. Khác biệt lý tưởng nhất là 0 (không). Nói cách khác, không nên có sự khác biệt giữa đăng ký và phân công. Khác biệt được tô và đánh bóng để dễ thấy 2 trạng thái:

- **Thiếu đăng ký** – Thiếu đăng ký xảy ra khi nguồn lực có nhiều phân công hơn đăng ký. Do năng lực này không được đăng ký trước nên người quản lý dự án có thể chỉnh sửa trạng thái này bằng cách mở rộng đăng ký nguồn lực để trang trải thâm hụt.
- **Đăng ký vượt mức** – Đăng ký vượt mức có thể xảy ra khi nguồn lực được đăng ký cho dự án nhưng không được phân công cho nhiệm vụ. Trạng thái này có thể chấp nhận được trong các trường hợp nguồn lực được đăng ký cho dự án trước khi phân công nhiệm vụ diễn ra. Tuy nhiên, trong các trường hợp khác, nguồn lực không được lên kế hoạch để được phân công nhiệm vụ. Trong những trường hợp này, người quản lý dự án nên xem xét hủy bỏ các đăng ký của nguồn lực để năng lực đó có thể dùng cho dự án khác.

Trong một số trường hợp, khi thấy mức thời gian cao hơn mức ngày (ví dụ: mức tháng), bạn có thể thấy khác biệt thực 0 cho nguồn lực (nói cách khác là đăng ký = phân công). Tuy nhiên, nếu thấy thời gian ở mức tuần, bạn có thể thấy phân công 0 giờ hoặc đăng ký 40 giờ trong tuần đầu tiên nhưng phân công 40 giờ và đăng ký 0 giờ trong tuần thứ hai. Nhìn chung, đăng ký và phân công được điều hòa nhưng khác nhau giữa một tuần và tuần tiếp theo.

Khi bạn thấy thời gian ở các mức cao hơn, các ô trong tab **Điều hòa** có chỉ báo để báo cho bạn biết rằng có sự khác biệt ở các mức thấp hơn. Bằng cách bấm đúp vào một ô, bạn có thể phóng to để xem sự khác biệt. Sau đó, bạn có thể bấm chuột phải để thu nhỏ. Bằng cách chọn một nguồn lực, sau đó dùng điều khiển **Khác biệt tiếp theo** trên thanh công cụ lưới, bạn có thể chuyển đến khác biệt tiếp theo giữa đăng ký và phân công cho nguồn lực. Sau đó, bạn có thể dùng điều khiển **Khác biệt trước đó** để quay lại. Bạn cũng có thể tắt chỉ báo khác biệt và hành vi điều hướng trong **Cài đặt**.

![Chỉ báo khác biệt.](media/Resource-Management-image57.png)

Nếu bạn có phân công nhiệm vụ cho nguồn lực nhưng không có đăng ký, trên trang **Dự án**, trên tab **Điều hòa**, hãy chọn thiếu đăng ký rồi chọn **Mở rộng đăng ký**. Hộp thoại **Mở rộng đăng ký** xuất hiện và hiển thị đăng ký cần thiết để khắc phục tình trạng thiếu của nguồn lực. Hộp thoại này cũng hiển thị đăng ký hiện có của nguồn lực trên tất cả dự án hoặc các thực thể có thể lập lịch khác. Nếu chọn **OK** để tạo đăng ký cho nguồn lực, bất kể trạng thái rảnh/bận của nguồn lực, bạn có thể gây ra tình trạng đăng ký vượt mức.

![Hộp thoại Mở rộng đăng ký.](media/Resource-Management-image58.png)

Người quản lý dự án hoặc người quản lý nguồn lực có thể dùng Bảng lịch trình để quản lý mọi tình huống nguồn lực bị đăng ký quá mức so với năng lực của họ.


[!INCLUDE[footer-include](../includes/footer-banner.md)]