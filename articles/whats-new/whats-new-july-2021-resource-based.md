---
title: Tính năng mới kể từ tháng 7 năm 2021 – Project Operations cho các kịch bản dựa trên nguồn lực/hàng không trữ kho
description: Chủ đề này cung cấp thông tin về các bản cập nhật chất lượng có trong bản phát hành tháng 7 năm 2021 của Project Operations cho các kịch bản dựa trên nguồn lực/hàng không trữ kho.
author: sigitac
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 69507427521466335df9cbbaba79db1cfc7be91386b8b2ded5b1c384555946ee
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/06/2021
ms.locfileid: "7008072"
---
# <a name="whats-new-july-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Tính năng mới kể từ tháng 7 năm 2021 – Project Operations cho các kịch bản dựa trên nguồn lực/hàng không trữ kho

*Áp dụng cho: Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho*

Chủ đề này áp dụng cho các phiên bản và thành phần sau của Dynamics 365 Project Operations:

   - Project Operations trong môi trường Microsoft Dataverse phiên bản 4.12.0.148 hoặc 4.12.0.152.
   - Quản lý dự án và kế toán trong môi trường Dynamics 365 Finance phiên bản 10.0.20.

## <a name="features-included-in-this-release"></a>Các tính năng có trong bản phát hành này

Sau đây là các tính năng có trong bản phát hành này:

- Khả năng cho phép quản trị viên xem nhật ký PSS và Thiết lập Operations từ menu cài đặt. Các nhật ký được lưu trữ trong 90 ngày.

## <a name="project-operations-dual-write-maps-updates"></a>Cập nhật về bản đồ ghi kép của Project Operations

Không có bản cập nhật nào cho bản đồ ghi kép Project Operations trong bản phát hành này.

Để biết danh sách hiện tại và các phiên bản của bản đồ ghi kép Project Operations, hãy xem [Phiên bản bản đồ ghi kép Project Operations](../environment/resource-dual-write-maps.md).

Luôn chạy phiên bản bản đồ mới nhất trong môi trường của bạn và bật tất cả các bản đồ bảng liên quan khi bạn cập nhật phiên bản giải pháp Project Operations Dataverse và giải pháp Tài chính. Một số tính năng và chức năng nhất định có thể không hoạt động chính xác nếu phiên bản mới nhất của bản đồ không được kích hoạt. Bạn có thể xem phiên bản đang hoạt động của bản đồ trên trang **Ghi kép** trong cột **Phiên bản**. Kích hoạt phiên bản mới của bản đồ bằng cách chọn **Các phiên bản bản đồ bảng**, chọn phiên bản mới nhất, sau đó lưu phiên bản đã chọn. Nếu đã tùy chỉnh sơ đồ bảng có sẵn, hãy áp dụng lại các thay đổi. Để biết thêm thông tin, hãy xem [Quản lý vòng đời áp dụng](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Nếu bạn gặp sự cố khi khởi động bản đồ, hãy làm theo hướng dẫn trong phần [Vấn đề thiếu cột trong bảng trên bản đồ](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) trong hướng dẫn khắc phục sự cố Ghi kép.

## <a name="quality-updates"></a>Bản cập nhật chất lượng

### <a name="project-operations-on-dataverse"></a>Project Operations trên Dataverse

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
| Chung                       | 2376405              | Đã khắc phục sự cố cập nhật theo nhà xuất bản (Bản cập nhật chất lượng có sẵn trong phiên bản 4.12.0.152)                                                                                                                     |
### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Quản lý dự án và kế toán trong Dynamics 365 Finance

| Lĩnh vực tính năng                      | Số tham chiếu | Cập nhật chất lượng                                                                                                                                                                                                                                                                                                                |
|-----------------------------------|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Quản lý dự án và kế toán | 4620267          | Không thể cá nhân hóa các biểu mẫu để thêm trường **Mục đích** vào các trang **Giao dịch đã kết sổ của dự án**, **Tạo đề xuất hóa đơn** và **Đề xuất hóa đơn**.                                                                                                                                                                                         |
| Quản lý dự án và kế toán | 4613449          | Khi bạn chọn ID hợp đồng dự án trong Tài chính, môi trường tích hợp Project Operations sẽ mở trang để tạo bản ghi mới thay vì mở trang cho hợp đồng dự án đã được tạo.                                                                                                                                           |
| Quản lý dự án và kế toán | 4614445          | Trong triển khai kịch bản tích hợp Project Operations, bạn không thể chỉnh sửa trường **Nhóm thuế bán hàng** trên đề xuất hóa đơn được nhập từ môi trường tách chuyển. Nhóm thuế bán hàng phải có thể chỉnh sửa đối với đề xuất hóa đơn mở của tất cả các loại giao dịch bao gồm trên tài khoản, giờ, chi phí, phí và mặt hàng. |
| Quản lý dự án và kế toán |                  | Không thể đăng đề xuất hóa đơn do chỉnh sửa giao dịch theo thời gian âm.                                                                                                                                                                                                                                              |
| Quản lý dự án và kế toán |                  | Các dòng đề xuất hóa đơn bị trùng lặp do có nhiều quy trình định kỳ **Nhập từ tách chuyển** đang chạy cùng lúc.                                                                                                                                                                                                                |

