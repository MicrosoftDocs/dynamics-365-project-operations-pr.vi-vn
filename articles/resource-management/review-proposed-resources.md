---
title: Đánh giá nguồn lực được đề xuất
description: Chủ đề này cung cấp thông tin về cách đề xuất các nguồn lực dự án.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: ad5cbdeb5fe05e6115eb024833a8d58b626ea4c9
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4087075"
---
# <a name="review-proposed-resources"></a>Đánh giá nguồn lực được đề xuất

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Người quản lý nguồn lực có thể đề xuất nguồn lực với người quản lý dự án bằng yêu cầu nguồn lực.

1. Từ lưới yêu cầu hoặc tự yêu cầu, hãy chọn **Tìm nguồn lực**.
2. Trên trang **Trợ lý lập lịch biểu** , hãy chọn nguồn lực, sau đó trong ngăn **Tạo đăng ký nguồn lực** , trong trường **Trạng thái đăng ký** , hãy chọn **Đăng ký**.

Các bản cập nhật trạng thái sau xảy ra:

- Trên trang **Trợ lý lập lịch biểu** , chỉ báo trạng thái được cập nhật để biểu thị đăng ký được đề xuất và không được đăng ký chắc chắn.
- Trên yêu cầu nguồn lực, trạng thái này được thay đổi thành **Cần đánh giá**.
- Trên tab **Nhóm** của dự án này, giá trị **Trạng thái yêu cầu** của thành viên nhóm chung được thay đổi thành **Cần đánh giá**.

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

Mỗi ô trong lưới đại diện cho phần trăm thời gian làm việc tính phí của nguồn lực trong một khoảng thời gian, chẳng hạn như ngày, tuần hoặc tháng. Công thức sau dùng để tô màu các ô:

- **Xanh lục:** Thời gian làm việc tính phí \>= Thời gian làm việc mục tiêu của nguồn lực
- **Vàng:** Thời gian làm việc mục tiêu – 20 \<= Thời gian làm việc tính phí \< Thời gian làm việc mục tiêu
- **Đỏ:** Thời gian làm việc tính phí \< Thời gian làm việc mục tiêu – 20

Vì dạng xem **Thời gian làm việc của nguồn lực** dựa trên Bảng lịch trình, nên bạn có thể dùng các khả năng lọc của Bảng lịch trình để lọc các kết quả.

Lưới yêu cầu rằng bạn đặt thời gian làm việc mục tiêu trên vai trò hoặc nguồn lực riêng. Để thực hiện thiết lập này, hãy chuyển đến **Nguồn lực** \> **Vai trò nguồn lực**.

Ngoài ra, vai trò mặc định phải được gán cho từng nguồn lực có thể đăng ký. Truy cập vào **Nguồn lực** \> **Nguồn lực**. Trên tab **Project Service** , hãy xác minh vai trò nguồn lực được định nghĩa và trường **Là mặc định** cho vai trò được đặt thành **Có**. Bạn có thể thêm các vai trò bổ sung mà **Là mặc định = Không**. Vai trò mà **Là mặc định = Có** dùng để đánh giá thời gian làm việc của nguồn lực so với mục tiêu cho vai trò đó.

Trên tab **Project Service** , bạn cũng có thể đặt thời gian làm việc mục tiêu riêng cho nguồn lực. Sau đó, phép tính thời gian làm việc dùng thời gian làm việc mục tiêu đó để đánh giá mục tiêu của nguồn lực thay vì mục tiêu của vai trò mặc định của nguồn lực.

Thời gian làm việc hiển thị cho nguồn lực chỉ khi nguồn lực được phê duyệt, thời gian tính phí trong khoảng thời gian hiển thị trong lưới.

## <a name="resource-availability"></a>Khả năng dùng nguồn lực

Điều quan trọng là người quản lý nguồn lực có thể xem trạng thái rảnh/bận của nguồn lực và cập nhật đăng ký. Trong một số trường hợp, không có nhu cầu chính thức (yêu cầu nguồn lực) nhưng người quản lý nguồn lực phải phản hồi với nhu cầu không theo kế hoạch qua các kênh như email, cuộc gọi điện thoại hoặc tin nhắn tức thời. Người quản lý nguồn lực dùng Bảng lịch trình để cập nhật tài nguyên và đăng ký.

Giờ làm việc của nguồn lực dùng làm cơ sở để tính toán trạng thái rảnh/bận của nguồn lực. Đăng ký nguồn lực tiêu thụ năng lực của nguồn lực.

Bảng lịch trình dùng màu và bóng để hiển thị đăng ký, trạng thái rảnh/bận, đăng ký quá mức và trạng thái của đăng ký. Cài đặt trong cài đặt Bảng lịch trình cho phép bạn hiển thị chú thích.

Nếu một mũi tên trỏ sang phải xuất hiện bên cạnh nguồn lực riêng có thể đăng ký trên Bảng lịch trình, thì nguồn lực có thể được mở rộng để hiển thị chi tiết của công việc mà nguồn lực được đăng ký.

Do Dynamics 365 Project Operations sử dụng công cụ Universal Resource Scheduling, nếu bạn cũng đã cài Dynamics 365 Field Service, bạn có thể xem chi tiết về đăng ký nguồn lực cho dự án, lệnh sản xuất và mọi thực thể khác mà bạn đã mở rộng lịch trình đến đó.

Để xem thêm chi tiết về nguồn lực riêng, hãy bấm chuột phải để mở thẻ nguồn lực.

