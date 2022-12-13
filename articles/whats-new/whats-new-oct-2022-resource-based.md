---
title: Có gì mới Tháng 10 năm 2022 - Project Operations cho các tình huống dựa trên tài nguyên/không có hàng trong kho
description: Bài viết này cung cấp thông tin về các bản cập nhật chất lượng có sẵn trong bản phát hành tháng 10 năm 2022 của Microsoft Dynamics 365 Project Operations cho các tình huống dựa trên tài nguyên/không có hàng trong kho.
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 392a12d6954c2390e5bad8e8e36cf58b7a1d0749
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806749"
---
# <a name="whats-new-october-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Có gì mới Tháng 10 năm 2022 - Project Operations cho các tình huống dựa trên tài nguyên/không có hàng trong kho

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Bài viết này áp dụng cho các phiên bản và thành phần sau của Microsoft Dynamics 365 Project Operations:

- Project Operations trong môi trường Dataverse phiên bản 4.57.0.176
- Quản lý dự án và kế toán trong môi trường ứng dụng Dynamics 365 Finance phiên bản 10.0.30

## <a name="features-included-in-this-release"></a>Các tính năng có trong bản phát hành này

| Lĩnh vực tính năng | Tên tính năng | Thông tin thêm |
| --- | --- | --- |
| Hoạch định và theo dõi dự án | **Project Operations Lập kế hoạch bên ngoài**<br>Chế độ lập lịch trình bên ngoài cho phép khách hàng tự tạo, cập nhật và xóa các thực thể có liên quan đến cấu trúc phân chia công việc (WBS) bằng cách sử dụng các API Dataverse gốc, không có giới hạn hiện tại do Project for the Web thực thi. | [Lập lịch bên ngoài](/dynamics365/project-operations/project-management/external-scheduling) |
| Triển khai và cấu hình | <p>**Cho phép khách hàng lựa chọn hình thức triển khai**<br>Các bản cập nhật hướng sản phẩm (PDU) của Project Operations được sử dụng để tự động cài đặt giải pháp Ghi kép của Project Operations khi các giải pháp điều phối và lõi ghi kép được cài đặt trong môi trường.</p><p>Tính năng này giới thiệu một tham số **hành vi nâng cấp giải pháp** mới trong Tham số dự án. Khi thông số này được đặt thành **Chỉ Lite**, PUD sẽ không còn tự động cài đặt giải pháp Ghi kép cho Project Operations nữa, ngay cả khi các giải pháp điều phối và lõi ghi kép được cài đặt trong môi trường. Hành vi này sẽ mang lại lợi ích cho những khách hàng dự định sử dụng giải pháp Ghi kép để tích hợp đơn bán hàng vào ứng dụng tài chính và vận hành, nhưng muốn sử dụng Project Operations ở chế độ Lite (nghĩa là không tích hợp vào ứng dụng tài chính và vận hành).</p> | |
| Định giá và thanh toán | <p>**Quy đổi tiền tệ cho giao dịch bán hàng chưa thanh toán chi phí trong môi trường Tích hợp**<br>Đối với những khách hàng sử dụng Project Operations được tích hợp với các ứng dụng tài chính và vận hành (nghĩa là trong loại triển khai nguồn lực/không dự trữ), tỷ giá hối đoái thường được nắm vững trong các ứng dụng tài chính và vận hành. Tuy nhiên, nếu một loại chi phí phải được định giá bằng cách sử dụng phương pháp tính giá "theo giá gốc" hoặc "tăng giá trên chi phí" khi khách hàng được lập hóa đơn, thì tỷ giá hối đoái được sử dụng để tính toán số tiền bán hàng sẽ sử dụng tỷ giá hối đoái trong Dataverse, không phải tỷ giá hối đoái từ các ứng dụng tài chính và hoạt động.</p><p>Tính năng này giới thiệu một tham số **Hành vi chuyển đổi tiền tệ** mới trong Tham số dự án. Khi thông số này được đặt thành **Mở rộng với dự phòng**, số tiền bán hàng chưa được lập hóa đơn cho các giao dịch chi phí được tính bằng cách sử dụng tỷ giá hối đoái từ các ứng dụng tài chính và vận hành.</p> | |

## <a name="project-operations-dual-write-maps-updates"></a>Cập nhật về bản đồ ghi kép của Project Operations

Không có bản cập nhật nào cho bản đồ ghi kép Project Operations trong bản phát hành này. Để biết danh sách hiện tại và các phiên bản của bản đồ ghi kép Project Operations, hãy xem [Phiên bản bản đồ ghi kép Project Operations](../environment/resource-dual-write-maps.md).

Luôn chạy phiên bản bản đồ mới nhất trong môi trường của bạn và bật tất cả các bản đồ bảng liên quan khi bạn cập nhật phiên bản giải pháp Project Operations Dataverse và giải pháp Tài chính. Một số tính năng và chức năng nhất định có thể không hoạt động chính xác nếu phiên bản mới nhất của bản đồ không được kích hoạt. Bạn có thể xem phiên bản hiện hoạt của bản đồ trong cột **Phiên bản** trên trang **Ghi kép**. Để kích hoạt phiên bản mới của bản đồ, hãy chọn **Phiên bản bản đồ bảng**, chọn phiên bản mới nhất rồi lưu phiên bản đã chọn. Nếu đã tùy chỉnh sơ đồ bảng có sẵn, hãy áp dụng lại các thay đổi. Để biết thêm thông tin, hãy xem [Quản lý vòng đời áp dụng](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Nếu bạn gặp sự cố khi khởi động bản đồ, hãy làm theo hướng dẫn trong phần [Vấn đề thiếu cột trong bảng trên bản đồ](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) của hướng dẫn khắc phục sự cố Ghi kép.

## <a name="quality-updates"></a>Bản cập nhật chất lượng

### <a name="project-operations-on-dataverse"></a>Project Operations trên Dataverse

| Lĩnh vực tính năng | Số tham chiếu | Cập nhật chất lượng |
| --- | --- | --- |
| Định giá và thanh toán | 2316317 | Hệ thống cho phép tạo hóa đơn không có giao dịch tính phí. |
| Định giá và thanh toán | 2737300 | Xác thực tính khả dụng của trường **Khách hàng**  trước khi truy cập biểu mẫu. |
| Định giá và thanh toán | 2744948 | Thêm kiểm tra null cho Phương thức thanh toán. |
| Định giá và thanh toán | 2763515 | Xử lý lỗi tham chiếu null khi thiếu hợp đồng mua bán của hóa đơn. |
| Định giá và thanh toán | 2844301 | Tạo hóa đơn hàng loạt không thành công do lỗi. |
| Định giá và thanh toán | 2845869 | Lưu trữ Dịch vụ Tổ chức không chính xác. |
| Định giá và thanh toán | 2853729 | Chi tiết Vai trò và Giá được cập nhật khi Loại thanh toán được sửa đổi. |
| Định giá và thanh toán | 2940350 | Khi giá thực tế được định giá, chỉ các bảng giá đang hoạt động mới được nhập tự động. |
| Triển khai và cấu hình | 3001206 | Thực thể msdyn\_ replaylogheader đang ngăn việc nâng cấp của Tổ chức khách hàng. |
| Quản lý cơ hội | 2755582 | Xử lý ngoại lệ tham chiếu null trong Trình trợ giúp quy tắc thanh toán chia tách. |
| Quản lý cơ hội | 2761477 | Khi thanh toán chia nhỏ được sử dụng, việc xóa một cột mốc (tiêu đề) sẽ để lại các cột mốc mồ côi. |
| Quản lý cơ hội | 2767595 | Khi một bản ghi sử dụng tài liệu được mở trong biểu mẫu chính, tài nguyên có thể đặt trước cho bản ghi được thay đổi thành người dùng hiện đang đăng nhập. |
| Hoạch định và theo dõi dự án | 2790384 | Thời gian chờ của OperationSet đang chờ xử lý quá ngắn. |
| Hoạch định và theo dõi dự án | 2957840 | Không thể lưu tác vụ và không thể thêm cột vào trang **Nhiệm vụ** trong Hoạt động dự án tích hợp. |
| Quản lý nguồn lực | 2751560 | Đơn vị Tổ chức Ưu tiên Không nhất quán trong Yêu cầu Nguồn lực. |
| Hợp đồng phụ | 2853245 | Khớp với thực tế Dòng hóa đơn của nhà cung cấp không cập nhật trạng thái xác minh nếu mô tả hợp đồng đã được liên kết với dòng hóa đơn của nhà cung cấp. |
| Hợp đồng phụ | 2907231 | Không thể tạm ứng giai đoạn xử lý hóa đơn của nhà cung cấp. |
| Thời gian và Chi phí | 2867363 | Các bản ghi không nằm ngoài dạng xem Vắng mặt/Nghỉ phép để phê duyệt khi chúng đang xếp hàng chờ phê duyệt. |
| Thời gian và Chi phí | 2894405 | TESA: Thư mục POC không được sử dụng đang gây ra sự cố tuân thủ. |

### <a name="project-management-and-accounting-in-finance"></a>Quản lý dự án và kế toán trong Tài chính

Để biết thông tin về các bản sửa lỗi có trong bản cập nhật này, hãy đăng nhập vào Microsoft Dynamics Lifecycle Services và xem [Bài viết trên KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).
