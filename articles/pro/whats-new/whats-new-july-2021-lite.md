---
title: Thông tin mới trong tháng 7 năm 2021 - Triển khai bản đơn giản Project Operations
description: Chủ đề này cung cấp thông tin về các bản cập nhật chất lượng có trong bản phát hành tháng 7 năm 2021 của triển khai bản đơn giản Project Operations.
author: sigitac
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6992498df5beb97d4e7197e301f093320dc28a23
ms.sourcegitcommit: 3abf1e67938d91bd826b025ae3187cd313f556b9
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 07/07/2021
ms.locfileid: "6433679"
---
# <a name="whats-new-july-2021---project-operations-lite-deployment"></a>Thông tin mới trong tháng 7 năm 2021 - Triển khai bản đơn giản Project Operations

_Áp dụng cho: Bản triển khai giản đơn - từ thỏa thuận đến lập hóa đơn ước giá_

Chủ đề này áp dụng cho các phiên bản và thành phần sau của Dynamics 365 Project Operations:

  - Project Operations trên môi trường Dataverse phiên bản 4.12.0.148.

## <a name="quality-updates"></a>Bản cập nhật chất lượng
| **Lĩnh vực tính năng**              | **Số tham chiếu** | **Cập nhật chất lượng**                                                                                                                                                                                             |
|-------------------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Định giá và thanh toán           | 2224046              | Trường **Lớp giao dịch** có thể chỉnh sửa được trên tab **Chi tiết mô tả báo giá**, nhưng bị khóa nếu bạn đang làm việc từ trang **Chi tiết mô tả báo giá**.                                                                     |
| Định giá và thanh toán           | 2224400              | Hành động **Đóng báo giá là đã giành được** không thành công khi báo giá không có mốc ngày.                                                                                                                                    |
| Định giá và thanh toán           | 2234089              | Khi bạn nhập mô tả sản phẩm theo cách thủ công, mô tả đó sẽ bị xóa sau khi bạn nhập số lượng để ước tính vật liệu.                                                                                                                         |
| Định giá và thanh toán           | 2234100              | Lưới **Thiết lập thanh toán theo tác vụ** không bao gồm cột **Vật liệu** và là giá trị trên tab **Thanh toán theo tác vụ** của dự án.                                                                                                       |
| Định giá và thanh toán           | 2277409              | ID sản phẩm không có sẵn trên chi tiết mô tả hợp đồng cho dòng loại vật liệu.                                                                                                                                        |
| Định giá và thanh toán           | 2281728              | Việc tạo một mô tả hợp đồng đánh giá lại các hành động một cách không cần thiết gây ra sự gia tăng đáng kể về khối lượng dữ liệu, điều này ảnh hưởng đến hiệu suất.                                                                                |
| Định giá và thanh toán           | 2298668              | Các dòng nhật ký kế toán liên quan đến chi phí bị thu hồi và đã xóa sẽ không bị xóa.                                                                                                                                     |
| Định giá và thanh toán           | 2300192              | Khi nhiều người dùng đang chỉnh sửa hóa đơn, có thể tạo chi tiết dòng hóa đơn mới trên hóa đơn đã xác nhận.                                                                                   |
| Định giá và thanh toán           | 2301569              | Không thể sửa hóa đơn nếu số tiền tạm ứng \$0 đã được áp dụng.                                                                                                                                        |
| Định giá và thanh toán           | 2307965              | Lỗi xảy ra nếu giá danh mục được tạo với các giá trị bị thiếu.                                                                                                                           |
| Định giá và thanh toán           | 2326870              | Một lỗi xảy ra trong **Microsoft.Dynamics.ProjectService.Plugins.PostInvoiceLineDelete** nếu **producttypecode** có giá trị rỗng.                                                                            |
| Định giá và thanh toán           | 2332732              | Lỗi xảy ra nếu một mốc mô tả hợp đồng được tạo mà không có dòng đơn hàng.                                                                                                                |
| Hoạch định và theo dõi dự án | 2181094              | API lập lịch dự án hiện hỗ trợ Nhật ký PSS và Nhật ký nhóm hoạt động được lưu trữ trong 90 ngày.                                                                                                                  |
| Hoạch định và theo dõi dự án | 2254201              | Nhãn **Chế độ lập lịch trình** được cập nhật với các chi tiết mô tả logic mặc định.                                                                                                                                      |
| Hoạch định và theo dõi dự án | 2300252              | Bộ đệm ẩn phản hồi **openProject** được cập nhật và bao gồm chủ sở hữu mã thông báo trong khóa bộ đệm ẩn, **Url cơ sở** và **Url phân khúc** để **Url yêu cầu** luôn có thể được tạo lại nếu **Url cơ sở** thay đổi. |
| Hoạch định và theo dõi dự án | 2301312              | **msdyn_membershipstatus** đã bị xóa khỏi dạng xem **Thành viên nhóm dự án**.                                                                                                                                        |
| Hoạch định và theo dõi dự án | 2302759              | Các sản phẩm được tìm nạp không cần thiết trên các tab **Gán nguồn lực**, **Ước tính** và **Ước tính chi phí**.                                                                                                        |
| Hoạch định và theo dõi dự án | 2308050              | **CopyProject** không thành công kèm theo lỗi, “Không thể nhận mã thông báo để giao tiếp với dịch vụ từ xa”.                                                                                                                           |
| Hoạch định và theo dõi dự án | 2322650              | Dạng xem **Danh sách nhiệm vụ trong dự án** đã được cập nhật để hiển thị ngày của nhiệm vụ theo mặc định.                                                                                                            |
| Hoạch định và theo dõi dự án | 2327266              | **CopyProject** tạo ra lỗi, "Không tìm thấy khóa trong từ điển" khi sao chép số liệu ước tính.                                                                                                      |
| Hoạch định và theo dõi dự án | 2328123              | **CopyProject** tạo ra lỗi, "Không thể nhận mã thông báo để giao tiếp với dịch vụ từ xa".                                                                                                                          |
| Hoạch định và theo dõi dự án | 2336258              | **CopyProject** sao chép sai tên vị trí của nguồn lực.                                                                                                                                                 |
| Định giá và thanh toán           | 2224476              | Trường **Nguồn lực có thể đặt trước** không được đặt mặc định đúng cho người dùng đã đăng nhập trên trang **Sử dụng vật liệu**.                                                                                                            |
| Quản lý nguồn lực           | 2277249              | Lỗi xảy ra khi yêu cầu nguồn lực không dựa trên dự án được cập nhật.                                                                                                            |
| Quản lý nguồn lực           | 2323869              | Việc sử dụng nguồn lực không nhận dạng chính xác các nguồn lực đã lọc.                                                                                                                                             |
| Thời gian và Chi phí              | 2176538              | Toán tử bộ lọc không chính xác được áp dụng cho điều khiển **Mục nhập thời gian**.                                                                                                                                                   |
| Thời gian và Chi phí              | 2177462              | Xóa mục nhập thời gian trong lưới không cập nhật trạng thái nút **Gửi**, **Gọi lại**, **Xóa** và **Chỉnh sửa mục nhập** theo dự kiến.                                                                                        |
| Thời gian và Chi phí              | 2299985              | **TimeEntriesImportFromResourceAssignment** không duy trì thời gian bắt đầu/kết thúc từ các mục phân phối giờ làm việc chỉ định.                                                                                                  |
| Thời gian và Chi phí              | 2318426              | Sau khi mục nhập thời gian được gửi, các trường bị khóa vẫn có thể được chỉnh sửa.                                                                                                                                   |
| Thời gian và Chi phí              | 2323749              | Lỗi xảy ra khi một khoản chi phí được tạo từ tab **Có liên quan** của một nguồn lực có thể đặt trước.                                                                                                      |
| Thời gian và Chi phí              | 2327678              | Khi bạn tạo một mục nhập thời gian từ tab **Có liên quan** của nguồn lực có thể đặt trước, nguồn lực chính không được chuyển cho kiểm soát mục nhập thời gian.                                                                            |
| Chung                       | 2296857              | Theo dõi tiến độ cho các công việc đang chạy trong thời gian dài.                                                                                                                                                                        |
| Chung                       | 2253682              | Không nên cài đặt giải pháp ghi kép Project Operations khi lõi ghi kép được cài đặt trong môi trường không có giải pháp điều phối ghi kép.                                                |
| Chung                       | 2316420              | Việc cung cấp dịch vụ dự án cốt lõi không thành công nếu đơn vị kinh doanh của người dùng ứng dụng bị thay đổi.                                                                                                                     |
