---
title: Có gì mới Tháng 3 năm 2022 - Hoạt động Dự án cho các kịch bản dựa trên tài nguyên / không có kho
description: Chủ đề này cung cấp thông tin về các bản cập nhật chất lượng có sẵn trong bản phát hành tháng 3 năm 2022 của Hoạt động dự án cho các tình huống dựa trên tài nguyên / không có kho.
author: sigitac
ms.date: 03/31/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: afd5149cda909b5367e7f12382423179d7e19267
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600768"
---
# <a name="whats-new-march-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Có gì mới Tháng 3 năm 2022 - Hoạt động Dự án cho các kịch bản dựa trên tài nguyên / không có kho

*Áp dụng cho: Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho*

Chủ đề này áp dụng cho các thành phần và phiên bản sau của Microsoft Dynamics 365 Project Operations:

- Hoạt động dự án trong một Dataverse phiên bản môi trường 4.30.0.99
- Quản lý dự án và kế toán trong môi trường Dynamics 365 Finance phiên bản 10.0.25

## <a name="features-included-in-this-release"></a>Các tính năng có trong bản phát hành này

Công tác phí hiện được hỗ trợ trong không gian làm việc chi phí hiện đại mới và được mô phỏng lại. Các công ty sử dụng công tác phí có thể kích hoạt tính năng này để người dùng dễ dàng nộp và được hoàn trả chi phí công tác phí. Để biết thêm thông tin, hãy xem [Công tác phí](../expense/per-diem-expenses.md).

## <a name="project-operations-dual-write-maps-updates"></a>Cập nhật về bản đồ ghi kép của Project Operations

Danh sách sau đây hiển thị các bản đồ viết kép đã được sửa đổi hoặc bổ sung trong bản phát hành Project Operations tháng 3 năm 2022.

| **Bản đồ thực thể** | **Phiên bản đã cập nhật** | **Nhận xét** |
| --- | --- | --- |
| Dự án Hoạt động tích hợp dự án nhà cung cấp thực thể xuất dòng hóa đơn msdyn\_ dự án | 1.0.0.3 | Đã cập nhật ánh xạ để phù hợp với thực thể dòng hóa đơn của nhà cung cấp trong Dataverse. <br>Không kích hoạt phiên bản ánh xạ 1.0.0.4. Nó sẽ sẵn sàng để sử dụng kết hợp với môi trường Tài chính phiên bản 10.0.26 trong bản cập nhật hàng tháng tiếp theo. |

Luôn chạy phiên bản bản đồ mới nhất trong môi trường của bạn và bật tất cả các bản đồ bảng liên quan khi bạn cập nhật Hoạt động dự án của mình Dataverse giải pháp và phiên bản giải pháp Tài chính. Một số tính năng và khả năng có thể không hoạt động chính xác nếu phiên bản mới nhất của bản đồ không được kích hoạt. Bạn có thể xem phiên bản hiện hoạt của bản đồ trong cột **Phiên bản** trên trang **Ghi kép**. Để kích hoạt phiên bản mới của bản đồ, hãy chọn **Phiên bản bản đồ bảng**, chọn phiên bản mới nhất rồi lưu phiên bản đã chọn. Nếu bạn đã tùy chỉnh sơ đồ bảng ngoài hộp, hãy áp dụng lại các thay đổi. Để biết thêm thông tin, hãy xem [Quản lý vòng đời áp dụng](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Nếu bạn gặp sự cố khi khởi động bản đồ, hãy làm theo hướng dẫn trong [Vấn đề thiếu cột trong bảng trên bản đồ](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) phần của hướng dẫn khắc phục sự cố Ghi kép.

## <a name="quality-updates"></a>Bản cập nhật chất lượng

### <a name="project-operations-on-dataverse"></a>Project Operations trên Dataverse

| Lĩnh vực tính năng | Số tham chiếu | Cập nhật chất lượng |
| --- | --- | --- |
| Thời gian và chi phí | 2388011 | Hiển thị nhận xét từ chối cho những người gửi mục nhập thời gian trong quá trình phê duyệt hàng loạt. |
| Hoạch định và theo dõi dự án | 2495294 | Không thể chỉnh sửa chi tiết dự án trên **Chi tiết công việc** trang. |
| Định giá và thanh toán | 2499605 | Các mốc hợp đồng được tạo từ các mốc báo giá được đánh dấu không chính xác là chỉ đọc. |
| Hoạch định và theo dõi dự án | 2506050 | Tập hợp hoạt động vẫn chờ xử lý trong một giờ nếu không có thay đổi nào để lưu. Tập hợp này sau đó được đánh dấu sai là **Thất bại**, trong khi nó phải được hoàn thành ngay lập tức. |
| Định giá và thanh toán | 2507401 | Các đơn vị hợp đồng mặc định được nhập không chính xác vào các dự án do bộ nhớ đệm không chính xác. |
| Định giá và thanh toán | 2541660 | **Xác thực việc tạo đơn hàng bán hàng** trong tính năng ghi kép chỉ dành cho các đơn đặt hàng dựa trên dự án. |
| Định giá và thanh toán | 2552745 | Thuế không được phân chia giữa những khách hàng đã thiết lập các quy tắc thanh toán riêng lẻ. |
| Định giá và thanh toán | 2558859 | Thông báo lỗi được cải thiện khi thiết lập thứ nguyên đặt giá. |
| Định giá và thanh toán | 2558933 | **Nhập từ Dự toán Dự án** thất bại khi **msdyn\_ dự định** được thêm vào làm thứ nguyên định giá. |
| Định giá và thanh toán | 2559101 | Việc xóa thông số dự án không bị chặn và gây ra sự cố. |
|   Quản lý cơ hội | 2570390 | Trình cắm ghi kép buộc loại tài khoản dựa trên báo giá, đơn đặt hàng và cơ hội **Khách hàng**, ngay cả khi loại tài khoản đó không chính xác. |
| Định giá và thanh toán | 2586097 | Các thực tế về chi phí được lập hóa đơn chia nhỏ không bị đảo ngược khi một dự án bị xóa khỏi dòng hợp đồng dự án. |
| Định giá và thanh toán | 2589619 | Thuế đối với tài liệu ghi vào được tuyên truyền đến các thực tế bán hàng chưa lập hóa đơn và hóa đơn. |
|   Quản lý cơ hội | 2594015 | Một báo giá không thể được đóng là giành cho những khách hàng có **Net60** điều khoản thanh toán. |
| Hoạch định và theo dõi dự án | 2595841 | Trong Dự án cho Web, người dùng nhận được thông báo lỗi về việc thiếu **msdyn\_ bắt đầu thực tế** khi họ tạo một yêu cầu tài nguyên mới. |
| Thời gian và Chi phí | 2602511 | Các **Bị từ chối bởi** trường cho các mục thời gian hiển thị **Hệ thống** thay vì một người dùng được đặt tên làm người từ chối. |
| Thời gian và Chi phí | 2602528 | Người phê duyệt dự án có thể phê duyệt thời gian cho các dự án mà họ không được liệt kê là người phê duyệt. |
| Định giá và thanh toán | 2608550 | Hóa đơn sửa chữa có thể được xác nhận ngay cả khi không có thay đổi so với bản gốc. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Quản lý dự án và kế toán trên Dynamics 365 Finance

| Lĩnh vực tính năng | Số tham chiếu | Cập nhật chất lượng |
| --- | --- | --- |
| Quản lý dự án và kế toán | [606759](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606759) | Có sự không phù hợp giữa Tài chính và Hoạt động Dự án trong độ dài cho phép của **Thể loại ID** đồng ruộng. |
| Quản lý dự án và kế toán | [617806](https://fix.lcs.dynamics.com/Issue/Details/?bugId=617806) | Các dự án giá cố định không thể bị loại bỏ khi **Khi lập hóa đơn tài khoản** trường được đặt thành **Lợi nhuận và thua lỗ** và **Phần trăm hoàn thành** nguyên tắc được sử dụng. |
| Quản lý dự án và kế toán | [620979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620979) | Nhóm thuế bán hàng mặc định không chính xác được nhập từ thiết lập dự án trên các dòng chi phí trong tạp chí tích hợp Hoạt động Dự án. |
| Quản lý dự án và kế toán | [623014](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623014) | Bạn không thể chỉnh sửa kích thước tiêu đề đề xuất hóa đơn dự án trong triển khai tích hợp với Hoạt động dự án. |
| Quản lý dự án và kế toán | [624283](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624283) | Hóa đơn nhà cung cấp liên công ty không được tích hợp với Dataverse. |
| Quản lý dự án và kế toán | [634156](https://fix.lcs.dynamics.com/Issue/Details/?bugId=634156) | Có sự không khớp trong đơn vị tiền tệ số dư của khách hàng và đơn vị tiền tệ báo cáo. |
| Quản lý dự án và kế toán | [641612](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641612) | Bạn có thể đăng hóa đơn dự án ngay cả khi khách hàng đang giữ tất cả các hóa đơn. |
| Quản lý dự án và kế toán | [642945](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642945) | Các **Xóa tất cả các dòng** thiếu nút trong các đề xuất hóa đơn dự án có **Tiêu đề** và **Dòng** lượt xem. |
| Quản lý dự án và kế toán | [637760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=637760) | Khi bạn đăng hóa đơn của nhà cung cấp, lỗi sau xảy ra: "Ngày kế toán cho hóa đơn phải cùng niên độ kế toán với đơn hàng đã mua có liên quan. Chạy quy trình cuối năm của đơn đặt hàng hoặc thay đổi ngày thành niên độ kế toán hiện tại. " |
| Đi lại và chi tiêu | [604128](https://fix.lcs.dynamics.com/Issue/Details/?bugId=604128) | Chi phí cam kết cho một dự án không được công bố sau khi chi phí cam kết của yêu cầu du lịch được công bố. |
| Đi lại và chi tiêu | [620803](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620803) | Lỗi sau xảy ra khi bạn gửi báo cáo chi phí: "Stack Trace: Công ty không tồn tại." |
| Đi lại và chi tiêu | [622465](https://fix.lcs.dynamics.com/Issue/Details/?bugId=622465) | Mặc định **ID dự án** không được nhập vào báo cáo chi phí khi **Yêu cầu hoạt động cho tạp chí** tham số được chọn trên dự án. |
| Đi lại và chi tiêu | [626781](https://fix.lcs.dynamics.com/Issue/Details/?bugId=626781) | Các **Đăng chi phí** nút không hoạt động chính xác trong Hoạt động dự án cho các tình huống tài nguyên / không có sẵn. |
| Đi lại và chi tiêu | [635348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=635348) | Có một vấn đề với **Tỷ lệ mỗi dặm** cho một báo cáo chi phí số dặm bao gồm hành khách. |
| Đi lại và chi tiêu | [638019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=638019) | Tỷ lệ số dặm chi phí cho nhân viên không được tính tổng chính xác khi hai loại xe khác nhau được sử dụng trong **Các bậc tỷ lệ dặm bay** danh mục chi phí. |
| Đi lại và chi tiêu | [641272](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641272) | Tra cứu **Dự định** trường trên dòng yêu cầu du lịch không trả về danh sách chính xác các dự án. |
| Đi lại và chi tiêu | [645905](https://fix.lcs.dynamics.com/Issue/Details/?bugId=645905) | **Số dặm được đánh giá** hiển thị cảnh báo trên các báo cáo chi phí. |
| Đi lại và chi tiêu | [647819](https://fix.lcs.dynamics.com/Issue/Details/?bugId=647819) | Dịch vụ nhận dạng ký tự quang học (OCR) của biên lai không hoạt động do có sự cố với URL của dịch vụ OCR chi phí. |
| Đi lại và chi tiêu | [648684](https://fix.lcs.dynamics.com/Issue/Details/?bugId=648684) | Khi mà **Khả năng lập thành các khoản chi phí định kỳ một cách nhanh chóng** tính năng được kích hoạt, số tiền trên các dòng thành khoản trên báo cáo chi phí thay đổi số tiền mỗi khi **Lặp lại** trang được mở. |
| Đi lại và chi tiêu | [651899](https://fix.lcs.dynamics.com/Issue/Details/?bugId=651899) | Bạn không thể xóa báo cáo chi phí khi danh sách tạm thời có nhiều hơn một người phê duyệt. |

## <a name="removed-and-deprecated-features"></a>Các tính năng đã bị xóa và không dùng nữa

Các [Các tính năng bị xóa hoặc không dùng nữa trong Hoạt động dự án](removed-depreciated-features-project.md) chủ đề mô tả các tính năng đã bị xóa hoặc không được dùng nữa đối với Dynamics 365 Project Operations.

- Tính năng đã xóa không còn khả dụng trong sản phẩm.
- Một tính năng không dùng nữa không được phát triển tích cực và có thể bị xóa trong bản cập nhật trong tương lai.

Thông báo ngừng sử dụng sẽ xuất hiện trong [Các tính năng bị xóa hoặc không dùng nữa trong Hoạt động dự án](removed-depreciated-features-project.md) chủ đề 12 tháng trước khi bất kỳ tính năng nào bị xóa khỏi sản phẩm.

Đối với các thay đổi vi phạm chỉ ảnh hưởng đến thời gian biên dịch, nhưng tương thích nhị phân với hộp cát và môi trường sản xuất, thời gian ngừng sử dụng sẽ dưới 12 tháng. Thông thường, những thay đổi này là các cập nhật chức năng phải được thực hiện cho trình biên dịch.
