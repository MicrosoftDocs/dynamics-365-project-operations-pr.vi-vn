---
title: Tính năng mới kể từ tháng 12 năm 2020 – triển khai Project Operations Lite – từ thỏa thuận đến lập hóa đơn ước giá
description: Chủ đề này cung cấp thông tin về các bản cập nhật chất lượng được cung cấp trong lần triển khai bản phát hành Project Operations Lite tháng 12 năm 2020 - từ thỏa thuận đến lập hóa đơn ước giá.
author: sigitac
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 81a5556e98d333fa86d73b1c7f03245a23a454372168f8bd7c79fc4425387734
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009377"
---
# <a name="whats-new-december-2020---project-operations-lite-deployment---deal-to-proforma-invoicing"></a>Tính năng mới kể từ tháng 12 năm 2020 – triển khai Project Operations Lite – từ thỏa thuận đến lập hóa đơn ước giá

_**Áp dụng cho:** Triển khai bản đơn giản – từ thỏa thuận đến lập hóa đơn ước giá_

Chủ đề này áp dụng cho các phiên bản và thành phần sau của Dynamics 365 Project Operations:

  - Project Operations trên môi trường Dataverse phiên bản 4.5.0.134 

Bảng sau liệt kê các bản cập nhật cho Project Operations trên môi trường Dataverse phiên bản 4.5.0.134.

| **Lĩnh vực tính năng** | **Số tham chiếu** | **Cập nhật chất lượng** |
| --- | --- | --- |
| Định giá và thanh toán | 1986009 | Các dòng nhật ký kế toán tạo thủ công sẽ hoạt động ổn định khi xác nhận trước khi dự án được liên kết hoặc bỏ liên kết với một dòng hợp đồng. |
| Định giá và thanh toán | 2014153 | Không lập hóa đơn cho các sản phẩm thực hiện từ lịch hóa đơn. |
| Định giá và thanh toán | 2014159 | Không lấy dữ liệu sản phẩm khi làm mới hóa đơn cho giao dịch. |
| Định giá và thanh toán | 2028174 | Những điểm cập nhật chi tết dòng hóa đơn phải tuân theo logic nhật ký sửa chữa. |
| Định giá và thanh toán | 2028315 | Sửa lỗi hành vi lưới lồng nhau chỉnh sửa được. |
| Định giá và thanh toán | 2031070 | Việc điều chỉnh chi tiết dòng hóa đơn phải tuân theo logic nhật ký sửa chữa. |
| Định giá và thanh toán | 2034186 | Phải có khả năng cập nhật dự án trên dòng hợp đồng. |
| Định giá và thanh toán | 2034206 | Trạng thái sửa đổi phải được thiết lập trong lần đảo ngược giá trị thực tế trong quá trình hủy liên kết dự án với dòng hợp đồng. |
| Định giá và thanh toán | 2040871 | Các điểm cập nhật của ô Cho phép đơn vị và Nhóm đơn vị trên lưới Ước tính khoản chi tiêu. |
| Định giá và thanh toán | 2053754 | Các giá trị thực tế tạo ra từ những điểm chỉnh sửa trên hóa đơn sẽ không được đánh dấu bằng trạng thái điều chỉnh và trạng thái thanh toán. |
| Định giá và thanh toán | 2057874 | Sửa kết nối giao dịch tạo ra trong quá trình chỉnh sửa chi tiết dòng hóa đơn. |
| Định giá và thanh toán | 2057875 | Sửa nguồn gốc giao dịch tạo ra trong quá trình chỉnh sửa chi tiết dòng hóa đơn. |
| Định giá và thanh toán | 2057944 | Trạng thái Cấm vượt quá được đặt là Cam kết đối với các trường hợp thực tế không sẵn sàng để lập hóa đơn từ lần sửa chữa hóa đơn. |
| Định giá và thanh toán | 2057963 | Tách quyền Create\_Product khỏi quyền Create\_ProjectContract. |
| Định giá và thanh toán | 2067622 | Biểu tượng đang xử lý sẽ hiển thị trong quá trình tạo mốc. |
| Định giá và thanh toán | 2067624 | Số tiền trong hợp đồng sẽ được đánh dấu là Đề xuất cho doanh nghiệp trong quá trình tạo mốc. |
| Định giá và thanh toán | 2086880 | Ẩn nút **Gợi ý** trên ruy băng của các dòng báo giá theo dự án. |
| Triển khai và cấu hình | 2101152 | Môi trường mới tạo bằng mẫu Project Operations trong Trung tâm quản trị viên Power Platform phải thực hiện tất cả các hoạt động sau cài đặt. |
|   Quản lý cơ hội | 2022204 | Lưới thanh toán theo dự án trên tab **Thanh toán cho nhiệm vụ** trên trang **Dự án** sẽ ẩn lưới theo dự án nếu không có dòng báo giá/hợp đồng nào có **Tất cả nhiệm vụ** và ngược lại. |
|   Quản lý cơ hội | 2086601 | Các vai trò và hạng mục đã hủy kích hoạt sẽ không được sao chép vào danh sách Vai trò có thể tính phí và Hạng mục có thể tính phí trên dòng báo giá và dòng hợp đồng. |
| Hoạch định và theo dõi dự án | 1949065 | Giao diện dữ liệu hoạt động bình thường khi phóng to 200% |
| Hoạch định và theo dõi dự án | 2046317 | Khả năng đổi tên thực thể dự án trong Project Operations |
| Hoạch định và theo dõi dự án | 2057171 | Cập nhật thông báo lỗi khi trường **Ngày bắt đầu dự án** bị để trống trên trang **Dự án**. |
| Hoạch định và theo dõi dự án | 2057197 | Chưa hỗ trợ khả năng sao chép dòng ước tính có tham chiếu nhiệm vụ. |
| Hoạch định và theo dõi dự án | 2060687 | Cảnh báo về múi giờ sẽ biến mất sau một khoảng thời gian nhất định. |
| Quản lý nguồn lực | 1832887 | ID hạng mục Nguồn lực mặc định phải ở trạng thái tĩnh để đảm bảo rằng dữ liệu khả lặp sẽ tải cho các môi trường Dataverse và Tài chính. |
| Thời gian và chi phí | 2034882 | Nút **Mới** hiển thị 2 lần trên thanh lệnh của các mục thời gian khi cài đặt Dynamics 365 Field Service. |
| Thời gian và chi phí | 2056028 | Cập nhật trang **Chỉnh sửa thời gian** để bao gồm dòng thời gian. |
| Thời gian và chi phí | 1983747 | Sơ đồ mục thời gian hiển thị thêm dữ liệu. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]