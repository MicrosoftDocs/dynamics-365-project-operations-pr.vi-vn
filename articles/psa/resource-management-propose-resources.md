---
title: Đề xuất nguồn lực dự án
description: Chủ đề này cung cấp thông tin về cách đề xuất các nguồn lực dự án.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 0a3eaa9929770c91523831d92744d5084aa28cb8
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147544"
---
# <a name="propose-project-resources"></a>Đề xuất nguồn lực dự án

[!include [banner](../includes/psa-now-project-operations.md)]

Người quản lý nguồn lực có thể đề xuất nguồn lực với người quản lý dự án bằng yêu cầu nguồn lực.

1. Từ lưới yêu cầu hoặc tự yêu cầu, hãy chọn **Tìm nguồn lực**.
2. Trên trang **Trợ lý lập lịch biểu**, hãy chọn nguồn lực, sau đó trong ngăn **Tạo đăng ký nguồn lực**, trong trường **Trạng thái đăng ký**, hãy chọn **Đăng ký**.

    ![Nguồn lực được đề xuất đã chọn](media/Resource-Management-image62.png)

Các bản cập nhật trạng thái sau xảy ra:

- Trên trang **Trợ lý lập lịch biểu**, chỉ báo trạng thái được cập nhật để biểu thị đăng ký được đề xuất và không được đăng ký chắc chắn.

    ![Chỉ báo trạng thái cho đăng ký đề xuất trên trang Trợ lý lập lịch biểu](media/Resource-Management-image63.png)

- Trên yêu cầu nguồn lực, trạng thái này được thay đổi thành **Cần đánh giá**.

    ![Trạng thái yêu cầu nguồn lực được thay đổi thành Cần đánh giá](media/Resource-Management-image64.png)

- Trên tab **Nhóm** của dự án này, giá trị **Trạng thái yêu cầu** của thành viên nhóm chung được thay đổi thành **Cần đánh giá**.

    ![Trạng thái yêu cầu của thành viên nhóm chung được thay đổi thành Cần đánh giá trên tab Nhóm](media/Resource-Management-image48.png)

Người quản lý dự án có thể chấp nhận hoặc từ chối đề xuất.

Khi người quản lý nguồn lực xử lý các yêu cầu nguồn lực, họ có thể dùng bất kỳ cách tiếp cận nào sau đây:

- Đề xuất nhiều nguồn lực để đáp ứng nhu cầu nếu không có nguồn lực đơn để để thực hiện các giờ cần thiết. Các giờ đề xuất sau đó được chia cho nhiều nguồn lực có thể đáp ứng các giờ yêu cầu. Trong trường hợp này, giờ không thể chồng chéo.
- Đề xuất ít nguồn lực hơn yêu cầu. Trong trường hợp này, năng lực nguồn lực đề xuất ít hơn giờ yêu cầu mà người yêu cầu chỉ định. Do đó, khi người yêu cầu chấp nhận các nguồn lực đề xuất, các yêu cầu nguồn lực chưa hoàn thành được tạo để ghi lại nhu cầu còn lại.
- Đăng ký các nguồn lực để đáp ứng nhu cầu nếu không có nguồn lực đơn sẵn có để hoàn thành công việc.
- Đăng ký ít nguồn lực hơn yêu cầu. Trong trường hợp này, giờ đăng ký ít hơn giờ yêu cầu. Hệ thống hướng dẫn bạn đề xuất nguồn lực thay vì đăng ký để người yêu cầu có thể xác minh và theo dõi các nhu cầu còn lại.

## <a name="billable-utilization"></a>Thời gian làm việc tính phí

Nguồn lực có thể có thời gian làm việc tính phí mục tiêu. Thời gian làm việc mục tiêu này được định nghĩa là thuộc tính trên vai trò mặc định của nguồn lực hoặc bộ trên bản ghi của nguồn lực riêng có thể đăng ký. Phép tính thời gian làm việc dựa trên số giờ thực tế mà nguồn lực đã báo cáo bằng mục nhập thời gian được phê duyệt.

Công thức sau dùng để tính toán thời gian làm việc:

- Thời gian làm việc tính phí = Giờ thực tế tính phí ÷ Năng lực của nguồn lực
- Thời gian làm việc không tính phí = Thời gian thực tế có ID loại thanh toán = Không tính phí, Bổ sung hoặc Không có ÷ Năng lực của nguồn lực
- Nội bộ =Thời gian thực tế không có hợp đồng bán hàng ÷ Năng lực của nguồn lực
- Năng lực của nguồn lực = Giờ làm việc của nguồn lực – Thời gian ngoài văn phòng – Ngày không làm việc

Bạn có thể tìm thấy dạng xem **Thời gian làm việc của nguồn lực** trong ngăn **Nguồn lực**.

![Dạng xem thời gian làm việc của nguồn lực](media/Resource-Management-image65.png)

Mỗi ô trong lưới đại diện cho phần trăm thời gian làm việc tính phí của nguồn lực trong một khoảng thời gian, chẳng hạn như ngày, tuần hoặc tháng. Công thức sau dùng để tô màu các ô:

- **Xanh lục:** Thời gian làm việc tính phí \>= Thời gian làm việc mục tiêu của nguồn lực
- **Vàng:** Thời gian làm việc mục tiêu – 20 \<= Thời gian làm việc tính phí \< Thời gian làm việc mục tiêu
- **Đỏ:** Thời gian làm việc tính phí \< Thời gian làm việc mục tiêu – 20

Vì dạng xem **Thời gian làm việc của nguồn lực** dựa trên Bảng lịch trình, nên bạn có thể dùng các khả năng lọc của Bảng lịch trình để lọc các kết quả.

Lưới yêu cầu rằng bạn đặt thời gian làm việc mục tiêu trên vai trò hoặc nguồn lực riêng. Để thực hiện thiết lập này, hãy chuyển đến **Nguồn lực** \> **Vai trò nguồn lực**.

Ngoài ra, vai trò mặc định phải được gán cho từng nguồn lực có thể đăng ký. Truy cập vào **Nguồn lực** \> **Nguồn lực**. Trên tab **Project Service**, hãy xác minh vai trò nguồn lực được định nghĩa và trường **Là mặc định** cho vai trò được đặt thành **Có**. Bạn có thể thêm các vai trò bổ sung mà **Là mặc định = Không**. Vai trò mà **Là mặc định = Có** dùng để đánh giá thời gian làm việc của nguồn lực so với mục tiêu cho vai trò đó.

![Vai trò mặc định đã đặt](media/Resource-Management-image67.png)

Trên tab **Project Service**, bạn cũng có thể đặt thời gian làm việc mục tiêu riêng cho nguồn lực. Sau đó, phép tính thời gian làm việc dùng thời gian làm việc mục tiêu đó để đánh giá mục tiêu của nguồn lực thay vì mục tiêu của vai trò mặc định của nguồn lực.

Thời gian làm việc hiển thị cho nguồn lực chỉ khi nguồn lực được phê duyệt, thời gian tính phí trong khoảng thời gian hiển thị trong lưới.

## <a name="resource-availability"></a>Khả năng dùng nguồn lực

Điều quan trọng là người quản lý nguồn lực có thể xem trạng thái rảnh/bận của nguồn lực và cập nhật đăng ký. Trong một số trường hợp, không có nhu cầu chính thức (yêu cầu nguồn lực) nhưng người quản lý nguồn lực phải phản hồi với nhu cầu không theo kế hoạch qua các kênh như email, cuộc gọi điện thoại hoặc tin nhắn tức thời. Người quản lý nguồn lực dùng Bảng lịch trình để cập nhật tài nguyên và đăng ký.

Giờ làm việc của nguồn lực dùng làm cơ sở để tính toán trạng thái rảnh/bận của nguồn lực. Đăng ký nguồn lực tiêu thụ năng lực của nguồn lực.

![Bảng thông tin lịch trình](media/Resource-Management-image68.png)

Bảng lịch trình dùng màu và bóng để hiển thị đăng ký, trạng thái rảnh/bận, đăng ký quá mức và trạng thái của đăng ký. Cài đặt trong cài đặt Bảng lịch trình cho phép bạn hiển thị chú thích.

Nếu một mũi tên trỏ sang phải xuất hiện bên cạnh nguồn lực riêng có thể đăng ký trên Bảng lịch trình, thì nguồn lực có thể được mở rộng để hiển thị chi tiết của công việc mà nguồn lực được đăng ký.

![Nguồn lực có thể đăng ký được mở rộng trên Bảng lịch trình](media/Resource-Management-image69.png)

Vì Dynamics 365 Project Service Automation dùng công cụ Universal Resource Scheduling, nếu bạn cũng có Dynamics 365 Field Service được cài đặt, bạn có thể xem chi tiết của đăng ký nguồn lực cho dự án, lệnh sản xuất và mọi thực thể khác mà bạn đã mở rộng lập lịch đến.

![Chi tiết đăng ký nguồn lực cho dự án và lệnh sản xuất](media/Resource-Management-image70.png)

Để xem thêm chi tiết về nguồn lực riêng, hãy bấm chuột phải để mở thẻ nguồn lực.

![Thẻ nguồn lực](media/Resource-Management-image71.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]