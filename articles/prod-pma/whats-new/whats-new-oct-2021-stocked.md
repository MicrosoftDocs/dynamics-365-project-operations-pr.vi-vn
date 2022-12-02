---
title: Có gì mới hoặc thay đổi trong Project Operations, tháng 10 năm 2021 cho các kịch bản dựa trên hàng trữ kho/sản xuất
description: Bài viết này cung cấp thông tin về các bản cập nhật chất lượng được cung cấp trong lần triển khai bản phát hành Project Operations tháng 10 năm 2021 cho tình huống dựa trên sản xuất/hàng trữ kho.
author: andchoi
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: aa36199c9e7b0a70307c5e9fb163d82554f6be16
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029969"
---
# <a name="whats-new-or-changed-in-project-operations-october-2021-for-stockedproduction-based-scenarios"></a>Có gì mới hoặc thay đổi trong Project Operations, tháng 10 năm 2021 cho các kịch bản dựa trên hàng trữ kho/sản xuất

_**Áp dụng cho:** Project Operations cho tình huống dựa trên hàng trữ kho/sản xuất_

Bài viết này áp dụng cho các phiên bản và thành phần sau của Microsoft Dynamics 365 Project Operations:

- Quản lý dự án và kế toán trong môi trường ứng dụng Dynamics 365 Finance phiên bản 10.0.22
 
## <a name="quality-updates"></a>Bản cập nhật chất lượng

| Lĩnh vực tính năng | Số tham chiếu | Cập nhật chất lượng |
|--------------|------------------|----------------|
| Quản lý dự án và kế toán | [557017](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557017) | Dự án đang thực hiện (WIP) và số tiền doanh thu tích lũy không được hoàn nguyên chính xác khi hóa đơn khách hàng liên công ty được đăng. |
| Quản lý dự án và kế toán | [558232](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558232) | Chức năng **Ngăn đóng dự án nếu giao dịch mở tồn tại** không hoạt động. |
| Quản lý dự án và kế toán | [559271](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559271) | Phân loại thanh toán trên hóa đơn văn bản tự do không tự động điền vào các thứ nguyên từ các dự án khi chức năng đó được bật. |
| Quản lý dự án và kế toán | [574013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574013) | Trong các trường hợp không phải liên công ty, WIP và số tiền doanh thu tích lũy không được hoàn nguyên chính xác khi hóa đơn dự án được đăng. |
| Quản lý dự án và kế toán | [577857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577857) | Giá trị ghi nợ và tín dụng được chuyển đổi khi phần bổ trợ Microsoft Excel được sử dụng với nhật ký Chi phí dự án và trường **Loại tài khoản bù trừ** được đặt thành **Dự án**. |
| Quản lý dự án và kế toán | [577972](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577972) | Số tiền được đăng trong các giao dịch dự án được phóng đại trên đơn đặt hàng dự án bao gồm các mặt hàng tồn kho và có tiền số thuế không được khấu trừ khi **UseTax** được đánh dấu. |
| Quản lý dự án và kế toán | [581216](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581216) | Hệ thống phân chia số tiền giữa các báo cáo lãi lỗ của dự án và các báo cáo WIP của dự án. |
| Quản lý dự án và kế toán | [582065](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582065) | Hàng tồn kho có sẵn không chính xác sau khi yêu cầu mặt hàng trả lại một phần được điều chỉnh. |
| Quản lý dự án và kế toán | [582682](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582682) | Tên nguồn lực được sao chép trong Project Operations khi chúng được chỉnh sửa trong Microsoft Project. |
| Quản lý dự án và kế toán | [583873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583873) | Các báo cáo chi phí liên công ty có các Khoản phải trả liên công ty đang chờ xử lý chi phí hóa đơn của nhà cung cấp lần đầu tiên được đăng lên kiểu đăng bài **Chi phí dự án WIP**. Tuy nhiên, trong quá trình xử lý, các chi phí liên quan đến ước tính được đăng lên kiểu đăng bài **Chi phí dự án** thay vì kiểu đăng bài **Chi phí liên công ty** dự kiến. |
| Quản lý dự án và kế toán | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Kết quả giữ lại của nhà cung cấp trong các giao dịch chi phí dự án không được hiển thị. |
| Quản lý dự án và kế toán | [587453](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587453) | Bảng chấm công phải làm tròn số tiền giao dịch trong đơn vị tiền tệ giao dịch tới một số có chữ số thập phân được chỉ định trên tất cả các khoản phân bổ kế toán và các bút toán chung. |
| Quản lý dự án và kế toán | [589409](https://fix.lcs.dynamics.com/Issue/Details/?bugId=589409) | Số lượng yêu cầu mục dự án được cập nhật tự động khi các đơn đặt hàng theo kế hoạch được quyết định. |
| Quản lý dự án và kế toán | [590206](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590206) | Không thể đảo ngược số chứng từ, số dư của nhà cung cấp loại giao dịch và số tài khoản trên hóa đơn thanh toán trước của đơn đặt hàng. |
| Quản lý dự án và kế toán | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Hóa đơn nhà cung cấp liên công ty bị hỏng khi tích hợp hóa đơn nhà cung cấp được bật. |
| Quản lý dự án và kế toán | [593335](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593335) | Khi bạn tạo nhật ký Chi phí dự án, số tiền chi phí được hiển thị trong trường **Tín dụng**. |
| Quản lý dự án và kế toán | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Các điều khoản thanh toán trên hóa đơn dự án không hoạt động như mong đợi. |
| Quản lý dự án và kế toán | [593565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593565) | Phiếu chấm công có thể được sử dụng lại khi dãy số được thiết lập dưới dạng liên tục. |
| Quản lý dự án và kế toán | [593652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593652) | PHÁP: Logic **Số tiền trả trước thủ công** không khớp với logic **Số tiền trả trước tự động** trong đề xuất hóa đơn hợp đồng Dự án. |
| Quản lý dự án và kế toán | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Khi khoản trả trước của nhà cung cấp được giải phóng, mục đăng phiếu có các dòng bổ sung không chính xác. |
| Quản lý dự án và kế toán | [596650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596650) | Khi trường **Ngày xuất hóa đơn** trên trang **Tạo đề xuất hóa đơn** được thay đổi, lỗi sau đây có thể xảy ra: "Tham chiếu đối tượng không được đặt thành phiên bản của đối tượng." |
| Quản lý dự án và kế toán | [597679](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597679) | Đã xảy ra lỗi khi bạn cố gắng phê duyệt bảng chấm công từ quy trình làm việc **TSLine** và có chính sách về bảng chấm công cho Thứ Bảy và Chủ Nhật. |
| Quản lý dự án và kế toán | [597801](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597801) | Loại mục dự án số dư đầu kỳ được loại trừ khỏi **Tóm tắt giao dịch đề xuất hóa đơn** khi tổng giá trị hóa đơn của đề xuất hóa đơn được tính toán. |
| Quản lý dự án và kế toán | [597886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597886) | Nếu chi phí tiêu thụ trên một đơn đặt hàng sản xuất dự án là 0 (không), thì lỗi sau đây xảy ra khi bạn cố gắng ước tính: "Đã cố gắng chia cho không." |
| Quản lý dự án và kế toán | [598706](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598706) | Ứng dụng dành cho thiết bị di động Project Timesheet cho Android ngừng phản hồi. Vấn đề liên quan đến **TimeEntryDataManager ArgumentNullException**. |
| Quản lý dự án và kế toán | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Nhật ký tích hợp Project Operations không được đăng vì một tài khoản bị thiếu thứ nguyên. Tuy nhiên, tài khoản thiếu thứ nguyên không phải là tài khoản mà bạn đang đăng lên. |
| Quản lý dự án và kế toán | [598929](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598929) | Bộ lọc **ToDate** trong tìm kiếm không bị xóa khi nó bị loại bỏ khỏi hộp thoại **Chọn**  trên trang **Đăng chi phí**. |
| Quản lý dự án và kế toán | [599757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=599757) | **Đặt lại tất cả phân bổ** không thành công và hiển thị lỗi cho các bảng chấm công được tạo cho dự án loại **Chỉ thời gian**. |
| Quản lý dự án và kế toán | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | Tab **Dự án** không thể chỉnh sửa trên hóa đơn nhà cung cấp đang chờ xử lý khi danh mục mua được chỉ định cho mặt hàng. |
| Quản lý dự án và kế toán | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Ngăn điều hướng không hiển thị nếu bạn chưa đăng nhập vào Project Operations Dataverse. |
| Quản lý dự án và kế toán | [546467](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546467) | Đối với các giao dịch điều chỉnh dự án liên công ty, có sự cố ở công ty đích. |
| Quản lý dự án và kế toán | [563579](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563579) | Chi phí đã cam kết cho dự án tính toán sai số lượng và giá vốn nếu đơn hàng được xử lý bằng  **Quy trình xử lý đơn hàng cuối năm** trong Sổ cái. |
| Quản lý dự án và kế toán | [581454](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581454) | Khi đơn đặt hàng sản xuất dự án có đơn đặt hàng chất lượng được báo cáo là đã hoàn thành, lỗi sau sẽ xảy ra: "Không có giao dịch ảo nào được đánh dấu với giao dịch hàng tồn kho". |
| Quản lý dự án và kế toán | [596408](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596408) | Khi một hóa đơn Khoản phải trả liên quan đến dự án được đăng, lỗi sau xảy ra: "Dự án - chi phí - mặt hàng văn bản liệt kê không tồn tại." |
| Quản lý dự án và kế toán | [597237](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597237) | Chi phí gián tiếp tăng gấp đôi khi bạn tích lũy doanh thu theo cách thủ công. |
| Quản lý dự án và kế toán | [601198](https://fix.lcs.dynamics.com/Issue/Details/?bugId=601198) | Tích lũy doanh thu và mục đăng WIP không tạo ra giao dịch. |
| Quản lý dự án và kế toán | [602095](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602095) | Kích hoạt giá đang chờ xử lý không thành công cho mục chi phí tiêu chuẩn khi đơn đặt hàng dự án đã nhận đang tồn tại. |
| Quản lý dự án và kế toán | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Giá trị WIP đảo ngược từ việc đăng hóa đơn khác với giá trị WIP đã đăng ban đầu từ mục nhập thời gian. |
| Quản lý dự án và kế toán | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Có sự cố đăng cho doanh thu được lập hóa đơn dự án trong các trường hợp trả trước được áp dụng trong đó các giao dịch phiếu thưởng không được cân bằng. |
| Quản lý dự án và kế toán | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Việc tạo ước tính sau khi đề xuất hóa đơn được đăng sẽ chặn việc nhập các dòng chỉnh sửa trong Project Operations. |
| Quản lý dự án và kế toán | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Không thể sửa đổi bản ghi mốc đã lập hóa đơn đầy đủ. |
| Quản lý dự án và kế toán | [611389](https://fix.lcs.dynamics.com/Issue/Details/?bugId=611389) | Khi tính phí tự động được sử dụng, không thể đăng hóa đơn khách hàng liên công ty cho bảng chấm công và thông báo lỗi sẽ hiển thị. |
| Quản lý dự án và kế toán | [612991](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612991) | Địa chỉ trên một dự án con không được cập nhật chính xác. |
| Quản lý dự án và kế toán | [613418](https://fix.lcs.dynamics.com/Issue/Details/?bugId=613418) | Giá vốn của các yêu cầu mặt hàng được cập nhật với giá mua của các đơn đặt hàng tổng hợp. |
| Quản lý dự án và kế toán | [614145](https://fix.lcs.dynamics.com/Issue/Details/?bugId=614145) | Chi phí đã đăng không chính xác sau khi giá mua được cập nhật và tham số **Kích hoạt quản lý thay đổi** được kích hoạt. |
| Đi lại và chi tiêu | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Tất cả chi phí của người dùng có thể hiển thị khi bạn tìm kiếm một thể loại trong ứng dụng Chi phí dành cho thiết bị di động. |
| Đi lại và chi tiêu | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Số tiền trên các giao dịch thuế bán hàng và giao dịch nhà cung cấp được tính từ một khoản chi phí được tạo ra từ giao dịch thẻ tín dụng là không chính xác. |
| Đi lại và chi tiêu | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Thông báo cảnh báo không liên quan được hiển thị khi bạn làm mới các trang báo cáo chi phí. |
| Đi lại và chi tiêu | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Sử dụng nhầm người phê duyệt tạm thời khi bạn xóa người phê duyệt tạm thời và sau đó gửi lại thông qua quy trình làm việc. |
| Đi lại và chi tiêu | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Lỗi đăng xảy ra có liên quan đến việc thiết lập khoảng cách. |
| Đi lại và chi tiêu | [620773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620773) | Phân bổ không cập nhật pháp nhân khi giao dịch không liên kết được thêm lại vào báo cáo chi phí trên chi phí liên công ty. |

### <a name="regulatory-updates"></a>Bản cập nhật theo quy định

Để biết thông tin về các bản cập nhật theo quy định cho ứng dụng tài chính và hoạt động, hãy xem [Bản cập nhật theo quy định](/dynamics365/finance/localizations/regulatory-updates). Bạn cũng có thể đăng nhập vào Lifecycle Services (LCS) Microsoft Dynamics và sử dụng công cụ tìm kiếm Sự cố để xem các bản cập nhật quy định theo kế hoạch. Tìm kiếm vấn đề cho phép bạn tìm kiếm theo quốc gia hoặc khu vực, loại tính năng và bản phát hành.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
