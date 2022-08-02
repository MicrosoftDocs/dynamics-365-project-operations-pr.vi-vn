---
title: Có gì mới vào tháng 7 năm 2022 - Hoạt động dự án cho các kịch bản dựa trên tài nguyên / không có kho
description: Bài viết này cung cấp thông tin về các bản cập nhật chất lượng có sẵn trong bản phát hành tháng 7 năm 2022 của Microsoft Dynamics 365 Project Operations cho các kịch bản dựa trên tài nguyên / không có kho.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: cbee9281d2fae485a3ebcd38bb884a2b2322f8d1
ms.sourcegitcommit: 66e376675e6df8efc86fa84ec24e9aad6a980304
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 07/21/2022
ms.locfileid: "9183950"
---
# <a name="whats-new-july-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Có gì mới vào tháng 7 năm 2022 - Hoạt động dự án cho các kịch bản dựa trên tài nguyên / không có kho

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Bài viết này áp dụng cho các thành phần và phiên bản sau của Microsoft Dynamics 365 Project Operations:

- Hoạt động dự án trong một Dataverse phiên bản môi trường 4.44.0.22
- Quản lý dự án và kế toán trong môi trường Dynamics 365 Finance phiên bản 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Cập nhật về bản đồ ghi kép của Project Operations

Không có bản cập nhật nào cho bản đồ ghi kép Project Operations trong bản phát hành này. Để biết danh sách hiện tại và các phiên bản của bản đồ ghi kép Project Operations, hãy xem [Phiên bản bản đồ ghi kép Project Operations](../environment/resource-dual-write-maps.md).

Luôn chạy phiên bản bản đồ mới nhất trong môi trường của bạn và bật tất cả các bản đồ bảng liên quan khi bạn cập nhật Hoạt động dự án của mình Dataverse giải pháp và phiên bản giải pháp Tài chính. Một số tính năng và khả năng có thể không hoạt động chính xác nếu phiên bản mới nhất của bản đồ không được kích hoạt. Bạn có thể xem phiên bản hiện hoạt của bản đồ trong cột **Phiên bản** trên trang **Ghi kép**. Để kích hoạt phiên bản mới của bản đồ, hãy chọn **Phiên bản bản đồ bảng**, chọn phiên bản mới nhất rồi lưu phiên bản đã chọn. Nếu bạn đã tùy chỉnh sơ đồ bảng ngoài hộp, hãy áp dụng lại các thay đổi. Để biết thêm thông tin, hãy xem [Quản lý vòng đời áp dụng](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Nếu bạn gặp sự cố khi khởi động bản đồ, hãy làm theo hướng dẫn trong [Vấn đề thiếu cột trong bảng trên bản đồ](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) của Hướng dẫn khắc phục sự cố ghi kép.

## <a name="quality-updates"></a>Bản cập nhật chất lượng

### <a name="project-operations-on-dataverse"></a>Project Operations trên Dataverse

| Lĩnh vực tính năng | Số tham chiếu | Cập nhật chất lượng |
| --- | --- | --- |
| Triển khai và cấu hình | 2761472 | Đã xử lý lỗi cài đặt Hoạt động Dự án. |
| Định giá và thanh toán | 2746940 | Tên dòng hợp đồng phụ phải có độ dài tối đa là 100 ký tự. |
| Định giá và thanh toán | 2739162 | Khách hàng phải có thể nhìn thấy các nút ruy-băng trong chế độ xem lưới thực tế. |
| Hoạch định và theo dõi dự án | 2730318 | Đã cập nhật xác thực cho các ký tự không được hỗ trợ trong chủ đề dự án. |
| Định giá và thanh toán | 2705361 | Các sổ tay bán hàng được lập hóa đơn theo cột mốc phải được đưa vào các trường theo dõi dự án. |
| Định giá và thanh toán | 2675880 | Ngăn một dự án được liên kết với một dòng hợp đồng không dựa trên công việc. |
| Định giá và thanh toán | 2664396 | Nếu một danh sách báo giá được lưu mà không có báo giá, thì phải có lỗi thông báo rằng báo giá không được để trống. |
| Định giá và thanh toán | 2184019 | Các **Thanh toán Dựa trên Nhiệm vụ** tab sẽ không được hiển thị cho các dự án không có hợp đồng hỗ trợ hoặc báo giá. |

### <a name="project-management-and-accounting-in-finance"></a>Quản lý dự án và kế toán trong lĩnh vực tài chính

Để biết thông tin về các bản sửa lỗi có trong bản cập nhật này, hãy đăng nhập vào Microsoft Dynamics Dịch vụ Vòng đời (LCS) và xem [KB bài báo](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Các tính năng được bật theo mặc định trong bản phát hành sắp tới

Bảng sau liệt kê các tính năng được bật theo mặc định trong phiên bản 10.0.29. Hầu hết các tính năng đã được bật tự động có thể được tắt trong [Quản lý tính năng](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). Trong tương lai, một số tính năng đã được bật tự động có thể bị xóa khỏi Quản lý tính năng và trở thành tính năng bắt buộc. Thay đổi này đảm bảo rằng khách hàng đang sử dụng chức năng hiện tại, để các cải tiến có thể xây dựng dựa trên chức năng hiện tại khi chúng được thêm vào. Các tính năng sẽ không bao giờ được bật tự động trong vòng chưa đầy một năm, trừ khi chúng được xác định là cần thiết.

| Tên tính năng | Ngày kích hoạt | Đã thêm tính năng | Trạng thái tính năng | Mô-đun |
| --- | --- | --- |--- |--- |
| Cho phép điều chỉnh giao dịch theo giờ dựa trên sự thay đổi trong phân bổ quy tắc cấp vốn | 16 tháng 9 năm 2022 | Ngày 7 tháng 10 năm 2020 | Bật theo mặc định | Quản lý dự án và kế toán |
| Tính năng đảo ngược hóa đơn thanh toán trước đơn đặt hàng dự án | 16 tháng 9 năm 2022 | Ngày 6 tháng 10 năm 2021 | Bật theo mặc định | Quản lý dự án và kế toán |
| Xóa các dòng đề xuất hóa đơn khi sử dụng Hoạt động dự án cho các tình huống dựa trên tài nguyên / không có kho | 16 tháng 9 năm 2022 | Ngày 6 tháng 10 năm 2021 | Bật theo mặc định | Quản lý dự án và kế toán |
| Điều chỉnh kế toán trên một giao dịch dự án đã đăng | 16 tháng 9 năm 2022 | Ngày 10 tháng 5 năm 2020 | Bật theo mặc định | Quản lý dự án và kế toán |
| Bật thiết lập kế toán mặc định cho dự án | 16 tháng 9 năm 2022 | Tháng 19 năm 2020 | Bật theo mặc định | Quản lý dự án và kế toán |
| Cho phép nhiều mô tả hợp đồng cho một dự án | 16 tháng 9 năm 2022 | Ngày 29 tháng 6 năm 2020 | Bật theo mặc định | Quản lý dự án và kế toán |
| Đặt các tạp chí trong Giờ Dự án ở chế độ chỉ đọc nếu trạng thái phê duyệt hiện tại không cho phép chỉnh sửa | 16 tháng 9 năm 2022 | Ngày 6 tháng 10 năm 2021 | Bật theo mặc định | Quản lý dự án và kế toán |
| Bật đồng bộ hóa dòng bán hàng từ dòng mua khi dòng mua được cập nhật và thông số quản lý thay đổi đơn đặt hàng được bật | 16 tháng 9 năm 2022 | Ngày 7 tháng 10 năm 2020 | Bật theo mặc định | Quản lý dự án và kế toán |
| Bật Hoạt động Dự án trên Dynamics 365 Customer Engagement | 16 tháng 9 năm 2022 | Ngày 29 tháng 6 năm 2020 | Bật theo mặc định | Quản lý dự án và kế toán |
| Tính năng điều chỉnh đảo ngược giao dịch dự án | 16 tháng 9 năm 2022 | Ngày 13 tháng 7 năm 2020 | Bật theo mặc định | Quản lý dự án và kế toán |

## <a name="features-that-become-mandatory-in-the-upcoming-release"></a>Các tính năng trở thành bắt buộc trong bản phát hành sắp tới

Bảng sau liệt kê các tính năng bắt buộc từ phiên bản 10.0.29 trở đi.

| Tên tính năng | Ngày kích hoạt | Đã thêm tính năng | Trạng thái tính năng | Mô-đun |
| --- | --- | --- | --- | --- |
| Tính giá trị cam kết trên nguồn vốn mà không làm tròn tỷ giá hối đoái | 16 tháng 9 năm 2022 | Ngày 14 tháng 6 năm 2020 | Bắt buộc | Quản lý dự án và kế toán |
| Cho phép đăng điều chỉnh dự án với cùng một tài khoản sổ cái như giao dịch ban đầu | 16 tháng 9 năm 2022 | Ngày 14 tháng 6 năm 2020 | Bắt buộc | Quản lý dự án và kế toán |
| Hợp đồng dự án chi tiết số tiền cam kết | 16 tháng 9 năm 2022 | Ngày 31 tháng 8 năm 2019 | Bắt buộc | Quản lý dự án và kế toán |
| Cho phép sắp xếp theo tài nguyên trong quá trình tạo đề xuất hóa đơn dự án | 16 tháng 9 năm 2022 | Ngày 31 tháng 8 năm 2019 | Bắt buộc | Quản lý dự án và kế toán |
