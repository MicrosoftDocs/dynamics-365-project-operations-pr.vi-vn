---
title: Tính năng mới kể từ tháng 7 năm 2022 – Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho
description: Bài viết này cung cấp thông tin về các bản cập nhật chất lượng có trong bản phát hành tháng 7 năm 2022 của Microsoft Dynamics 365 Project Operations cho các kịch bản dựa trên nguồn lực/hàng không nhập kho.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: e63b29741dbaa400a2176ff8b4c35c6d64dfeab4
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403978"
---
# <a name="whats-new-july-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Tính năng mới kể từ tháng 7 năm 2022 – Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Bài viết này áp dụng cho các phiên bản và thành phần sau của Microsoft Dynamics 365 Project Operations:

- Project Operations trong môi trường Dataverse phiên bản 4.44.0.22
- Quản lý dự án và kế toán trong môi trường ứng dụng Dynamics 365 Finance phiên bản 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Cập nhật về bản đồ ghi kép của Project Operations

Không có bản cập nhật nào cho bản đồ ghi kép Project Operations trong bản phát hành này. Để biết danh sách hiện tại và các phiên bản của bản đồ ghi kép Project Operations, hãy xem [Phiên bản bản đồ ghi kép Project Operations](../environment/resource-dual-write-maps.md).

Luôn chạy phiên bản bản đồ mới nhất trong môi trường của bạn và bật tất cả các bản đồ bảng liên quan khi bạn cập nhật phiên bản giải pháp Project Operations Dataverse và giải pháp Tài chính. Một số tính năng và chức năng nhất định có thể không hoạt động chính xác nếu phiên bản mới nhất của bản đồ không được kích hoạt. Bạn có thể xem phiên bản hiện hoạt của bản đồ trong cột **Phiên bản** trên trang **Ghi kép**. Để kích hoạt phiên bản mới của bản đồ, hãy chọn **Phiên bản bản đồ bảng**, chọn phiên bản mới nhất rồi lưu phiên bản đã chọn. Nếu đã tùy chỉnh sơ đồ bảng có sẵn, hãy áp dụng lại các thay đổi. Để biết thêm thông tin, hãy xem [Quản lý vòng đời áp dụng](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Nếu bạn gặp sự cố khi khởi động bản đồ, hãy làm theo hướng dẫn trong phần [Vấn đề thiếu cột trong bảng trên bản đồ](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) của hướng dẫn khắc phục sự cố Ghi kép.

## <a name="quality-updates"></a>Bản cập nhật chất lượng

### <a name="project-operations-on-dataverse"></a>Project Operations trên Dataverse

| Lĩnh vực tính năng | Số tham chiếu | Cập nhật chất lượng |
| --- | --- | --- |
| Triển khai và cấu hình | 2761472 | Lỗi cài đặt Project Operations được xử lý. |
| Định giá và thanh toán | 2746940 | Tên mô tả hợp đồng phụ phải có độ dài tối đa là 100 ký tự. |
| Định giá và thanh toán | 2739162 | Khách hàng phải có thể nhìn thấy các nút ruy băng trong dạng xem lưới thực tế. |
| Hoạch định và theo dõi dự án | 2730318 | Đã cập nhật xác thực cho các ký tự không được hỗ trợ trong chủ đề dự án. |
| Định giá và thanh toán | 2705361 | Doanh số đã lập hóa đơn thực tế theo mốc phải được bao gồm trong các trường theo dõi dự án. |
| Định giá và thanh toán | 2675880 | Ngăn một dự án được liên kết với một mô tả hợp đồng không dựa trên công việc. |
| Định giá và thanh toán | 2664396 | Nếu một bảng giá của báo giá được lưu mà không có báo giá, thì phải có lỗi thông báo rằng báo giá đó không được để trống. |
| Định giá và thanh toán | 2184019 | Tab **Lập hóa đơn dựa trên nhiệm vụ** sẽ không được hiển thị cho các dự án không có hợp đồng hoặc báo giá hỗ trợ. |
| Thời gian và Chi phí | 2754459 | Khi dòng đám mây lập lịch định kỳ không hoạt động, hiển thị thông báo biểu ngữ và bỏ qua xử lý không đồng bộ. |
| Định giá và thanh toán | 2724391 | Ngoại lệ sai được đưa ra khi quy tắc lập hóa đơn chia nhỏ hợp đồng dự án bị thiếu giá trị khách hàng. |
| Định giá và thanh toán | 2708638 | Bản ghi không được tìm thấy trong khi tìm kiếm bằng cách sử dụng tìm kiếm theo lưới trong Sử dụng vật tư và Phê duyệt sử dụng vật tư.|
| Định giá và thanh toán | 2686977 | Ngăn xác thực cho mô tả hóa đơn trong khi tạo hóa đơn. |
| Định giá và thanh toán | 2683032 | Việc sao chép các vai trò và danh mục có thể tính phí không vượt quá 5000 bản ghi.|
| Định giá và thanh toán | 2673363 | % Sử dụng chi phí trên Dự án bị hỏng khi tồn tại cả ước tính Nỗ lực và Chi phí và số liệu thực tế cho một dự án. |

### <a name="project-management-and-accounting-in-finance"></a>Quản lý dự án và kế toán trong Tài chính

Để biết thông tin về các bản sửa lỗi có trong bản cập nhật này, hãy đăng nhập vào Microsoft Dynamics Lifecycle Services (LCS) và xem [Bài viết trên KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Các tính năng được bật theo mặc định trong bản phát hành sắp tới

Bảng sau liệt kê các tính năng được bật theo mặc định trong phiên bản 10.0.29. Hầu hết các tính năng đã được tự động bật có thể được tắt trong [Quản lý tính năng](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). Trong tương lai, một số tính năng đã được bật tự động có thể bị xóa khỏi Quản lý tính năng và trở thành tính năng bắt buộc. Thay đổi này đảm bảo rằng khách hàng đang sử dụng chức năng hiện tại, sao cho các cải tiến có thể xây dựng dựa trên chức năng hiện tại khi chúng được thêm vào. Các tính năng sẽ không bao giờ được bật tự động trong vòng chưa đầy một năm, trừ khi chúng được xác định là cần thiết.

| Tên tính năng | Ngày kích hoạt | Tính năng được thêm | Trạng thái tính năng | Mô-đun |
| --- | --- | --- |--- |--- |
| Cho phép điều chỉnh giao dịch theo giờ dựa trên sự thay đổi trong phân bổ quy tắc cấp vốn | Ngày 16 tháng 09 năm 2022 | Ngày 7 tháng 10 năm 2020 | Bật theo mặc định | Quản lý dự án và kế toán |
| Tính năng đảo ngược hóa đơn thanh toán trước đơn đặt hàng dự án | Ngày 16 tháng 09 năm 2022 | Ngày 6 tháng 10 năm 2021 | Bật theo mặc định | Quản lý dự án và kế toán |
| Xóa mô tả đề xuất hóa đơn khi sử dụng Project Operations cho các kịch bản dựa trên tài nguyên/không lưu kho | Ngày 16 tháng 09 năm 2022 | Ngày 6 tháng 10 năm 2021 | Bật theo mặc định | Quản lý dự án và kế toán |
| Điều chỉnh kế toán trên một giao dịch dự án đã đăng | Ngày 16 tháng 09 năm 2022 | Ngày 10 tháng 5 năm 2020 | Bật theo mặc định | Quản lý dự án và kế toán |
| Bật thiết lập kế toán mặc định cho dự án | Ngày 16 tháng 09 năm 2022 | Tháng 19 năm 2020 | Bật theo mặc định | Quản lý dự án và kế toán |
| Cho phép nhiều mô tả hợp đồng cho một dự án | Ngày 16 tháng 09 năm 2022 | Ngày 29 tháng 6 năm 2020 | Bật theo mặc định | Quản lý dự án và kế toán |
| Đặt nhật ký Giờ dự án là chỉ đọc nếu trạng thái phê duyệt hiện tại không cho phép chỉnh sửa | Ngày 16 tháng 09 năm 2022 | Ngày 6 tháng 10 năm 2021 | Bật theo mặc định | Quản lý dự án và kế toán |
| Bật đồng bộ hóa mô tả doanh số từ mô tả mua hàng khi mô tả mua hàng được cập nhật và tham số quản lý thay đổi thứ tự mua hàng được bật | Ngày 16 tháng 09 năm 2022 | Ngày 7 tháng 10 năm 2020 | Bật theo mặc định | Quản lý dự án và kế toán |
| Kích hoạt Project Operations trên Dynamics 365 Customer Engagement | Ngày 16 tháng 09 năm 2022 | Ngày 29 tháng 6 năm 2020 | Bật theo mặc định | Quản lý dự án và kế toán |
| Tính năng điều chỉnh đảo ngược giao dịch dự án | Ngày 16 tháng 09 năm 2022 | Ngày 13 tháng 7 năm 2020 | Bật theo mặc định | Quản lý dự án và kế toán |

## <a name="features-that-become-mandatory-in-the-upcoming-release"></a>Các tính năng trở thành bắt buộc trong bản phát hành sắp tới

Bảng sau liệt kê các tính năng là bắt buộc từ phiên bản 10.0.29 trở về sau.

| Tên tính năng | Ngày kích hoạt | Tính năng được thêm | Trạng thái tính năng | Mô-đun |
| --- | --- | --- | --- | --- |
| Tính giá trị cam kết trên nguồn vốn mà không làm tròn tỷ giá hối đoái | Ngày 16 tháng 09 năm 2022 | Ngày 14 tháng 6 năm 2020 | Bắt buộc | Quản lý dự án và kế toán |
| Cho phép đăng điều chỉnh dự án với cùng một tài khoản sổ cái dưới dạng giao dịch ban đầu | Ngày 16 tháng 09 năm 2022 | Ngày 14 tháng 6 năm 2020 | Bắt buộc | Quản lý dự án và kế toán |
| Chi tiết số tiền cam kết cho hợp đồng dự án | Ngày 16 tháng 09 năm 2022 | Ngày 31 tháng 08 năm 2019 | Bắt buộc | Quản lý dự án và kế toán |
| Cho phép sắp xếp theo nguồn lực trong quá trình tạo đề xuất hóa đơn dự án | Ngày 16 tháng 09 năm 2022 | Ngày 31 tháng 08 năm 2019 | Bắt buộc | Quản lý dự án và kế toán |
