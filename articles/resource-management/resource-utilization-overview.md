---
title: Tổng quan về thời gian làm việc của nguồn lực
description: Chủ đề này cung cấp thông tin về cách sử dụng nguồn lực trong Project Operations.
author: ruhercul
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8b85464dbb68523b122116225a604f67e7236f3e
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401402"
---
# <a name="resource-utilization-overview"></a>Tổng quan về thời gian làm việc của nguồn lực

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho, triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Nguồn lực có thể có thời gian làm việc tính phí mục tiêu. Thời gian làm việc mục tiêu này được định nghĩa là thuộc tính trên vai trò mặc định của nguồn lực hoặc bộ trên bản ghi của nguồn lực riêng có thể đăng ký. Phép tính thời gian làm việc dựa trên số giờ thực tế mà nguồn lực đã báo cáo bằng mục nhập thời gian được phê duyệt.

Công thức sau dùng để tính toán thời gian làm việc:

  - Thời gian làm việc tính phí = Giờ thực tế tính phí ÷ Năng lực của nguồn lực
  - Thời gian làm việc không tính phí = Thời gian thực tế có ID loại thanh toán = Không tính phí, Bổ sung hoặc Không có ÷ Năng lực của nguồn lực
  - Nội bộ =Thời gian thực tế không có hợp đồng bán hàng ÷ Năng lực của nguồn lực
  - Năng lực của nguồn lực = Giờ làm việc của nguồn lực – Thời gian ngoài văn phòng – Ngày không làm việc

Bạn có thể tìm thấy dạng xem **Thời gian làm việc của nguồn lực** trong ngăn **Nguồn lực**.

Mỗi ô trong lưới đại diện cho phần trăm thời gian làm việc tính phí của nguồn lực trong một khoảng thời gian, chẳng hạn như ngày, tuần hoặc tháng. Công thức sau dùng để tô màu các ô:

  - **Màu lục**: Thời gian làm việc tính phí >= Thời gian làm việc mục tiêu của nguồn lực
  - **Màu vàng**: Thời gian làm việc mục tiêu – 20 <= Thời gian làm việc tính phí < Thời gian làm việc mục tiêu
  - **Màu đỏ**: Thời gian làm việc tính phí < Thời gian làm việc mục tiêu – 20

Vì dạng xem **Thời gian làm việc của nguồn lực** dựa trên Bảng lịch trình, nên bạn có thể dùng các khả năng lọc của Bảng lịch trình để lọc các kết quả.

Lưới yêu cầu rằng bạn đặt thời gian làm việc mục tiêu trên vai trò hoặc nguồn lực riêng. Để thực hiện bước thiết lập này, hãy chuyển đến **Nguồn lực** > **Vai trò nguồn lực**.

Ngoài ra, vai trò mặc định phải được gán cho từng nguồn lực có thể đăng ký. Chuyển đến **Nguồn lực** > **Nguồn lực**. Trên tab **Dịch vụ dự án**, hãy xác minh vai trò nguồn lực được xác định và trường **Là mặc định** được đặt thành **Có**. Bạn có thể thêm các vai trò bổ sung mà trường **Là mặc định** = **Không**. Vai trò mà trường **Là mặc định** = **Có** dùng để đánh giá thời gian làm việc của nguồn lực so với mục tiêu cho vai trò đó.

Trên tab **Project Service**, bạn cũng có thể đặt thời gian làm việc mục tiêu riêng cho nguồn lực. Sau đó, phép tính thời gian làm việc dùng thời gian làm việc mục tiêu đó để đánh giá mục tiêu của nguồn lực thay vì mục tiêu của vai trò mặc định của nguồn lực.

Thời gian làm việc chỉ hiển thị cho nguồn lực chỉ khi nguồn lực đã phê duyệt, thời gian phải thanh toán trong khoảng thời gian hiển thị trong lưới.


[!INCLUDE[footer-include](../includes/footer-banner.md)]