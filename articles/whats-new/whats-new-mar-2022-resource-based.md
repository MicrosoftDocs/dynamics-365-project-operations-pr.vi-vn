---
title: Có gì mới trong tháng 3 năm 2022 – Project Operations cho các trường hợp dựa trên nguồn lực/không tồn kho
description: Bài viết này cung cấp thông tin về các bản cập nhật chất lượng được cung cấp trong lần triển khai bản phát hành Project Operations tháng 3 năm 2022 cho tình huống dựa trên nguồn lực/hàng không trữ kho.
author: sigitac
ms.date: 03/31/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 986d0652ed502873085259fef5ad40aba99c278d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910932"
---
# <a name="whats-new-march-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Có gì mới trong tháng 3 năm 2022 – Project Operations cho các trường hợp dựa trên nguồn lực/không tồn kho

*Áp dụng cho: Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho*

Bài viết này áp dụng cho các phiên bản và thành phần sau của Microsoft Dynamics 365 Project Operations:

- Project Operations trong môi trường Dataverse phiên bản 4.30.0.99
- Quản lý dự án và kế toán trong môi trường ứng dụng Dynamics 365 Finance phiên bản 10.0.25

## <a name="features-included-in-this-release"></a>Các tính năng có trong bản phát hành này

Công tác phí hiện được hỗ trợ trong không gian làm việc chi phí hiện đại mới và được thiết kế lại. Các công ty sử dụng công tác phí có thể bật tính năng này để người dùng dễ dàng đệ trình và được hoàn trả chi phí công tác phí. Để biết thêm thông tin, hãy xem phần [Chi phí công tác phí](../expense/per-diem-expenses.md).

## <a name="project-operations-dual-write-maps-updates"></a>Cập nhật về bản đồ ghi kép của Project Operations

Danh sách sau đây hiển thị các bản đồ ghi kép đã được sửa đổi hoặc bổ sung trong bản phát hành Project Operations vào tháng 3 năm 2022.

| **Bản đồ thực thể** | **Phiên bản đã cập nhật** | **Nhận xét** |
| --- | --- | --- |
| Thực thể xuất mô tả hóa đơn nhà cung cấp của dự án tích hợp Project Operations msdyn\_projectvendorinvoicelines | 1.0.0.3 | Các ánh xạ được cập nhật để thống nhất với thực thể mô tả hóa đơn của nhà cung cấp trong Dataverse. <br>Không kích hoạt phiên bản ánh xạ 1.0.0.4. Nó sẽ sẵn sàng để sử dụng kết hợp với môi trường Finance phiên bản 10.0.26 trong bản cập nhật hàng tháng tiếp theo. |

Luôn chạy phiên bản bản đồ mới nhất trong môi trường của bạn và bật tất cả các bản đồ bảng liên quan khi bạn cập nhật phiên bản giải pháp Project Operations Dataverse và giải pháp Tài chính. Một số tính năng và chức năng nhất định có thể không hoạt động chính xác nếu phiên bản mới nhất của bản đồ không được kích hoạt. Bạn có thể xem phiên bản hiện hoạt của bản đồ trong cột **Phiên bản** trên trang **Ghi kép**. Để kích hoạt phiên bản mới của bản đồ, hãy chọn **Phiên bản bản đồ bảng**, chọn phiên bản mới nhất rồi lưu phiên bản đã chọn. Nếu đã tùy chỉnh sơ đồ bảng có sẵn, hãy áp dụng lại các thay đổi. Để biết thêm thông tin, hãy xem [Quản lý vòng đời áp dụng](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Nếu bạn gặp sự cố khi khởi động bản đồ, hãy làm theo hướng dẫn trong phần [Vấn đề thiếu cột trong bảng trên bản đồ](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) của hướng dẫn khắc phục sự cố Ghi kép.

## <a name="quality-updates"></a>Bản cập nhật chất lượng

### <a name="project-operations-on-dataverse"></a>Project Operations trên Dataverse

| Lĩnh vực tính năng | Số tham chiếu | Cập nhật chất lượng |
| --- | --- | --- |
| Thời gian và chi phí | 2388011 | Hiển thị nhận xét từ chối cho những người gửi mục nhập thời gian trong quá trình phê duyệt hàng loạt. |
| Hoạch định và theo dõi dự án | 2495294 | Không thể chỉnh sửa chi tiết dự án trên trang **Chi tiết công việc**. |
| Định giá và thanh toán | 2499605 | Các mốc hợp đồng được tạo từ các mốc báo giá được đánh dấu không chính xác là chỉ đọc. |
| Hoạch định và theo dõi dự án | 2506050 | Bộ thao tác vẫn chờ xử lý trong một giờ nếu không có thay đổi nào để lưu. Bộ này sau đó được đánh dấu sai là **Không thành công**, trong khi nó phải được hoàn thành ngay lập tức. |
| Định giá và thanh toán | 2507401 | Các đơn vị hợp đồng mặc định được nhập không chính xác vào các dự án do bộ nhớ đệm không chính xác. |
| Định giá và thanh toán | 2541660 | **Xác thực việc tạo đơn bán hàng** trong tính năng ghi kép chỉ dành cho các đơn hàng dựa trên dự án. |
| Định giá và thanh toán | 2552745 | Thuế không được phân chia giữa những khách hàng đã thiết lập các quy tắc thanh toán riêng. |
| Định giá và thanh toán | 2558859 | Thông báo lỗi được cải thiện khi các thứ nguyên giá được thiết lập. |
| Định giá và thanh toán | 2558933 | **Nhập từ ước tính dự báo** thất bại khi **msdyn\_project** được thêm làm thứ nguyên giá. |
| Định giá và thanh toán | 2559101 | Việc xóa tham số dự án không bị chặn và gây ra sự cố. |
|   Quản lý cơ hội | 2570390 | Phần bổ trợ ghi kép buộc loại tài khoản dựa trên báo giá, đơn hàng và cơ hội là **Khách hàng**, ngay cả khi loại tài khoản đó không chính xác. |
| Định giá và thanh toán | 2586097 | Các chi phí thực tế được lập hóa đơn chia nhỏ không bị đảo ngược khi một dự án bị xóa khỏi mô tả hợp đồng dự án. |
| Định giá và thanh toán | 2589619 | Thuế vật tư chọn thêm được truyền vào doanh số chưa lập hóa đơn thực tế và hóa đơn. |
|   Quản lý cơ hội | 2594015 | Không thể đóng báo giá là đã chốt cho khách hàng có điều khoản thanh toán **Net60**. |
| Hoạch định và theo dõi dự án | 2595841 | Trong Project for the Web, người dùng nhận được thông báo lỗi về **msdyn\_actualstart** còn thiếu khi tạo yêu cầu nguồn lực mới. |
| Thời gian và Chi phí | 2602511 | Trường **Người từ chối** cho mục nhập thời gian hiển thị **Hệ thống** thay vì người dùng được đặt tên làm người từ chối. |
| Thời gian và Chi phí | 2602528 | Người phê duyệt dự án có thể phê duyệt thời gian cho các dự án mà họ không được liệt kê là người phê duyệt. |
| Định giá và thanh toán | 2608550 | Hóa đơn điều chỉnh có thể được xác nhận ngay cả khi không có thay đổi so với bản gốc. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Quản lý dự án và kế toán trên Dynamics 365 Finance

| Lĩnh vực tính năng | Số tham chiếu | Cập nhật chất lượng |
| --- | --- | --- |
| Quản lý dự án và kế toán | [606759](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606759) | Có sự không khớp giữa Finance và Project Operations trong độ dài cho phép của trường **ID danh mục**. |
| Quản lý dự án và kế toán | [617806](https://fix.lcs.dynamics.com/Issue/Details/?bugId=617806) | Các dự án giá cố định không thể bị loại khi trường **Lập hóa đơn trên tài khoản** được đặt thành **Lãi và lỗ** và nguyên tắc **Phần trăm hoàn thành** được sử dụng. |
| Quản lý dự án và kế toán | [620979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620979) | Nhóm thuế bán hàng mặc định không chính xác được nhập từ thiết lập dự án trên mô tả chi phí trong nhật ký tích hợp Project Operations. |
| Quản lý dự án và kế toán | [623014](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623014) | Bạn không thể chỉnh sửa thứ nguyên tiêu đề của đề xuất hóa đơn trong triển khai tích hợp với Project Operations. |
| Quản lý dự án và kế toán | [624283](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624283) | Hóa đơn nhà cung cấp liên công ty không được tích hợp với Dataverse. |
| Quản lý dự án và kế toán | [634156](https://fix.lcs.dynamics.com/Issue/Details/?bugId=634156) | Có sự không khớp trong đơn vị tiền tệ số dư của khách hàng và đơn vị tiền tệ báo cáo. |
| Quản lý dự án và kế toán | [641612](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641612) | Bạn có thể đăng hóa đơn dự án ngay cả khi khách hàng đang tạm giữ tất cả các hóa đơn. |
| Quản lý dự án và kế toán | [642945](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642945) | Nút **Xóa tất cả mô tả** bị thiếu trong các đề xuất hóa đơn dự án có dạng xem **Tiêu đề** và **Mô tả**. |
| Quản lý dự án và kế toán | [637760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=637760) | Khi bạn đăng hóa đơn của nhà cung cấp, lỗi sau xảy ra: "Ngày kế toán cho hóa đơn phải trong cùng niên độ kế toán với đơn đặt hàng có liên quan. Hãy chạy quy trình xử lý đơn hàng cuối năm hoặc thay đổi ngày thành niên độ kế toán hiện tại." |
| Đi lại và chi tiêu | [604128](https://fix.lcs.dynamics.com/Issue/Details/?bugId=604128) | Chi phí cam kết cho một dự án không được công bố sau khi thả yêu cầu đi lại với chi phí đã cam kết. |
| Đi lại và chi tiêu | [620803](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620803) | Lỗi sau xảy ra khi bạn gửi báo cáo chi phí: "Stack Trace: Công ty không tồn tại." |
| Đi lại và chi tiêu | [622465](https://fix.lcs.dynamics.com/Issue/Details/?bugId=622465) | **ID dự án** mặc định không được nhập vào báo cáo chi phí khi tham số **Yêu cầu hoạt động cho nhật ký** được chọn trên dự án. |
| Đi lại và chi tiêu | [626781](https://fix.lcs.dynamics.com/Issue/Details/?bugId=626781) | Nút **Đăng chi phí** không hoạt động chính xác trong Project Operations cho các trường hợp nguồn lực/không tồn kho. |
| Đi lại và chi tiêu | [635348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=635348) | Có sự cố với **Tỷ lệ mỗi dặm** cho một báo cáo chi phí số dặm bao gồm hành khách. |
| Đi lại và chi tiêu | [638019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=638019) | Tỷ lệ quãng đường chi phí cho nhân viên không được tính tổng chính xác khi hai loại xe khác nhau được sử dụng trong danh mục chi phí **Các bậc tỷ lệ khoảng cách**. |
| Đi lại và chi tiêu | [641272](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641272) | Tra cứu cho trường **Dự án** trên dòng yêu cầu đi lại không trả về danh sách chính xác các dự án. |
| Đi lại và chi tiêu | [645905](https://fix.lcs.dynamics.com/Issue/Details/?bugId=645905) | **Khoảng cách được đánh giá** hiển thị cảnh báo trên các báo cáo chi phí. |
| Đi lại và chi tiêu | [647819](https://fix.lcs.dynamics.com/Issue/Details/?bugId=647819) | Dịch vụ nhận dạng ký tự quang học (OCR) của biên lai không hoạt động do sự cố với URL của dịch vụ OCR chi phí. |
| Đi lại và chi tiêu | [648684](https://fix.lcs.dynamics.com/Issue/Details/?bugId=648684) | Khi tính năng **Khả năng ghi lại các chi phí định kỳ một cách nhanh chóng** được bật, số tiền trên các dòng thành khoản trên báo cáo chi phí thay đổi số tiền mỗi khi trang **Ghi lại** được mở. |
| Đi lại và chi tiêu | [651899](https://fix.lcs.dynamics.com/Issue/Details/?bugId=651899) | Bạn không thể xóa báo cáo chi phí khi danh sách tạm thời có nhiều hơn một người phê duyệt. |

## <a name="removed-and-deprecated-features"></a>Các tính năng bị xóa và không dùng nữa

Bài viết [Các tính năng bị xóa hoặc không dùng nữa trong Project Operations](removed-depreciated-features-project.md) mô tả các tính năng đã bị xóa hoặc không được dùng nữa đối với Dynamics 365 Project Operations.

- Tính năng đã xóa không còn khả dụng trong sản phẩm.
- Tính năng không dùng nữa không ở trong giai đoạn phát triển và có thể bị xóa khỏi bản cập nhật trong tương lai.

Thông báo không dùng nữa sẽ xuất hiện trong bài viết [Các tính năng bị xóa hoặc không dùng nữa trong Project Operations](removed-depreciated-features-project.md) 12 tháng trước khi bất kỳ tính năng nào bị xóa khỏi sản phẩm.

Đối với các thay đổi mới chỉ ảnh hưởng đến thời gian biên dịch, nhưng tương thích nhị phân với hộp cát và môi trường sản xuất, thời gian không dùng nữa sẽ ít hơn 12 tháng. Thông thường, những thay đổi này là các cập nhật chức năng phải được thực hiện cho công cụ biên soạn.
