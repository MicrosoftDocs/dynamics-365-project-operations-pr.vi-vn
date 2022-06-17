---
title: Có gì mới hoặc thay đổi trong Hoạt động dự án, tháng 9 năm 2021 đối với các tình huống có hàng / dựa trên sản xuất
description: Bài viết này cung cấp thông tin về các bản cập nhật chất lượng có trong bản phát hành Hoạt động dự án vào tháng 9 năm 2021 cho các tình huống dựa trên sản xuất / tồn kho.
author: andchoi
ms.date: 11/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: 1e99471b4338209c1f7fe411084d1745d74b2d2c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916544"
---
# <a name="whats-new-or-changed-in-project-operations-september-2021-for-stockedproduction-based-scenarios"></a>Có gì mới hoặc thay đổi trong Hoạt động dự án, tháng 9 năm 2021 đối với các tình huống có hàng / dựa trên sản xuất

_**Áp dụng cho:** Project Operations cho tình huống dựa trên hàng trữ kho/sản xuất_

Bài viết này áp dụng cho các thành phần và phiên bản sau của Microsoft Dynamics 365 Project Operations:

- Quản lý dự án và kế toán trong môi trường Dynamics 365 Finance phiên bản 10.0.21
 
## <a name="quality-updates"></a>Bản cập nhật chất lượng

| Lĩnh vực tính năng | Số tham chiếu | Cập nhật chất lượng |
|---|---|---|
| Quản lý dự án và kế toán | [412077](https://fix.lcs.dynamics.com/Issue/Details/?bugId=412077) | Nếu vai trò Người quản lý mua hàng được cấp quyền truy cập cho một pháp nhân, thì vai trò này cũng có quyền truy cập vào tất cả các dự án trong tất cả các pháp nhân. |
| Quản lý dự án và kế toán | [537214](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537214) | Vấn đề làm tròn thuế giá trị gia tăng (VAT) xảy ra trong khi giấy báo có được thanh toán với hóa đơn gốc của dự án. |
| Quản lý dự án và kế toán | [538002](https://fix.lcs.dynamics.com/Issue/Details/?bugId=538002) | Sử dụng ngân sách dự án thay thế để xác minh ngân sách. |
| Quản lý dự án và kế toán | [546265](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546265) | Các **Giá bán hàng giờ** nhóm giá không được tính toán trên cơ cấu phân tích công việc để báo giá dự án. |
| Quản lý dự án và kế toán | [555604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=555604) | Việc loại bỏ ước tính không thành công khi **Bật đơn vị tiền tệ của hợp đồng dự án để tính toán ước tính** tính năng được kích hoạt. |
| Quản lý dự án và kế toán | [563523](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563523) | Việc phân bổ thuế bán hàng theo số lượng được cộng vào giá bán khi thuế sử dụng được sử dụng trên nhóm thuế doanh thu của Nhật ký chi phí dự án. |
| Quản lý dự án và kế toán | [564701](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564701) | Thuế có điều kiện không được tính chính xác cho lần thanh toán cuối cùng khi áp dụng việc giữ lại và trả trước của nhà cung cấp cho các hóa đơn đặt hàng. |
| Quản lý dự án và kế toán | [565642](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565642) | Dấu vết điều chỉnh không hoạt động đối với các tạp chí số dư đầu năm. |
| Quản lý dự án và kế toán | [568814](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568814) | **Phân bổ ngân sách dự án sửa đổi theo thời kỳ** được chia thành tất cả các khoảng thời gian ngân sách. Khi phân bổ được gửi, hồ sơ sẽ không bị xóa. |
| Quản lý dự án và kế toán | [569250](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569250) | Các bài đăng trong quá trình xử lý (WIP) lên sổ cái chung có số lượng không chính xác. |
| Quản lý dự án và kế toán | [570731](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570371) | Phê duyệt nhật ký dự án giờ không hoạt động. |
| Quản lý dự án và kế toán | [571391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571391) | Giá bán điều chỉnh dự án không được cập nhật với chi phí gián tiếp khi giới hạn tài trợ không được đánh dấu. |
| Quản lý dự án và kế toán | [575831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575831) | Không thể tạo yêu cầu mặt hàng khi tiêu đề bảng Bán hàng được lập hóa đơn và đơn đặt hàng dự phòng cho các dòng hiện có đã được hoàn tất. |
| Quản lý dự án và kế toán | [578036](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578036) | Số tiền giữ lại cho quy tắc thanh toán có mốc cho một dự án khác không được đăng trong ID dự án tương ứng đã được chọn cho mốc đó. Thay vào đó, nó được đăng cùng với dự án đầu tiên. |
| Quản lý dự án và kế toán | [578327](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578327) | Khi bạn chọn **Bộ kích thước tài chính** trên một đề xuất hóa đơn, lỗi sau xảy ra: "Không thể truyền đối tượng thuộc loại 'Dynamics.AX .Application.FormIntControl 'để nhập' Dynamics.AX .Application.FormStringControl '. " |
| Quản lý dự án và kế toán | [581167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581167) | Các **Hóa đơn dự án** báo cáo bỏ qua dòng. |
| Quản lý dự án và kế toán | [581489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581489) | Lỗi xảy ra khi bạn tính toán kiểm soát chi phí cho một dự án đầu tư. |
| Quản lý dự án và kế toán | [590357](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590357) | Các **ProjTable:: InitFromCustTable - canDeletePostalAddress** phương pháp gây ra sự cố về hiệu suất. |
| Quản lý dự án và kế toán | [592493](https://fix.lcs.dynamics.com/Issue/Details/?bugId=592493) | Thông báo lỗi phải rõ ràng hơn "Lỗi không mong muốn". |
| Quản lý dự án và kế toán | [598810](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598810) | Công việc đăng hàng loạt hóa đơn Dự án xử lý và đăng đề xuất hóa đơn ngay cả khi các dòng hóa đơn chưa được tạo. |
| Quản lý dự án và kế toán | [574282](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574282) | Sự cố làm tròn xảy ra khi khóa cấu hình giấy phép khu vực công cộng bị tắt. Chi phí hoặc giá bán không chính xác được tạo ra trên bảng chấm công giờ cho các hợp đồng có nhiều nguồn sáng lập. |
| Quản lý dự án và kế toán | [577598](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577598) | Giá bán dự án trên đơn đặt hàng dự án đã lập hóa đơn được tính không chính xác khi mô hình giá bán là **Tỷ lệ đóng góp**. |
| Quản lý dự án và kế toán | [580784](https://fix.lcs.dynamics.com/Issue/Details/?bugId=580784) | Hệ thống không xem xét những ngày hoạt động giữa thời điểm nó tính toán tỷ lệ lao động hiệu quả cho một nhân viên. |
| Quản lý dự án và kế toán | [584054](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584054) | Lỗi đăng xảy ra trên bảng chấm công liên công ty do lỗi xác thực sau: "Không có đối tác thương mại nào được định cấu hình cho pháp nhân." |
| Quản lý dự án và kế toán | [586303](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586303) | Mô tả từ một đơn đặt hàng có danh mục chi phí không được truy xuất trong danh sách giao dịch dự án đã đăng. |
| Quản lý dự án và kế toán | [590349](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590349) | Có một sự chuyển đổi không chính xác trên các tạp chí Hạng mục được đăng cho một dự án. |
| Quản lý dự án và kế toán | [557294](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557294) | Bạn có thể xác nhận đơn đặt hàng ngay cả khi đã vượt quá giới hạn tài trợ. |
| Quản lý dự án và kế toán | [574162](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574162) | Các **Sửa / Hủy hóa đơn** phần trên hóa đơn văn bản miễn phí sẽ biến mất khi ID dự án được chọn. |
| Quản lý dự án và kế toán | [575425](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575425) | Có các vấn đề về hiệu suất khi một đề xuất hóa đơn dự án được đăng từ một đơn đặt hàng bán dự án bao gồm một mặt hàng tồn kho. |
| Quản lý dự án và kế toán | [575939](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575939) | Không thể đăng hóa đơn mua dự án vì xảy ra lỗi sau: "Chức năng AccDistProcessorProjectExtension.createForProjectRevenueLine đã được gọi không chính xác." |
| Quản lý dự án và kế toán | [578970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578970) | Cập nhật để tạo các công việc hàng loạt ước tính dự án để hỗ trợ thực hiện nhiều nhiệm vụ con. |
| Quản lý dự án và kế toán | [584519](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584519) | Không thể cập nhật trạng thái của bảng chấm công thành **Bản thảo** khi quy trình làm việc bị mắc kẹt trong một **Đã hủy** tiểu bang. |
| Quản lý dự án và kế toán | [584757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584757) | Số tiền giữ lại không được tính trong đề xuất hóa đơn ghi có nếu có nhiều dòng. |
| Quản lý dự án và kế toán | [586034](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586034) | Khi bạn cố gắng thay đổi số tiền trên hóa đơn đã tạo từ một đơn đặt hàng, lỗi sau xảy ra: "Các giao dịch trên chứng từ không cân bằng theo XX / XX / XXXX. (đơn vị tiền tệ kế toán: 0,00 - đơn vị tiền tệ báo cáo: 0,01)." |
| Quản lý dự án và kế toán | [588714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588714) | Có vấn đề về hiệu suất khi một đề xuất hóa đơn dự án được đăng ở chế độ hàng loạt, do liên kết với **GeneralJournalAccountEntry**. |
| Quản lý dự án và kế toán | [588851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588851) | Có vấn đề về hiệu suất khi bảng chấm công được đăng. |
| Quản lý dự án và kế toán | [590535](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590535) | Hệ thống phân cấp ước tính chi phí của cấu trúc phân tích công việc không được căn chỉnh chính xác sau khi tất cả các tác vụ được mở rộng hoặc sau khi một tác vụ được mở rộng theo cách thủ công. |
| Quản lý dự án và kế toán | [593663](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593663) | Không thể thêm mẫu Excel báo giá dự án vào **Mở trong Excel** thực đơn. |
| Quản lý dự án và kế toán | [596669](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596669) | Số miễn thuế cho một pháp nhân không được bao gồm trên hóa đơn dự án in. |
| Quản lý dự án và kế toán | [597563](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597563) | Không có dữ liệu tài chính nào được cập nhật trong lỗi đơn vị hàng tồn kho khi một dự án được điều chỉnh liên quan đến hạn mức tín dụng. |
| Quản lý dự án và kế toán | [598109](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598109) | Sau khi áp dụng KB 461935, bạn không thể đăng ước tính nếu chuyển sang chuỗi số liên tục. |
| Quản lý dự án và kế toán | [598688](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598688) | **TimeEntryDataManager** khiến ứng dụng di động Bảng chấm công dự án cho Android để ngừng phản hồi. |
| Quản lý dự án và kế toán | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Giá trị WIP được đảo ngược từ lần đăng hóa đơn khác với giá trị WIP được đăng ban đầu từ mục nhập thời gian. |
| Quản lý dự án và kế toán | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Trong các trường hợp trả trước được áp dụng, các giao dịch trên phiếu mua hàng không cân bằng khi doanh thu được lập hóa đơn cho một dự án được đăng. |
| Quản lý dự án và kế toán | [603320](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603320) | Khi mà **Nâng cao hiệu suất lập kế hoạch tài nguyên dự án** tính năng được bật, các giá trị thập phân được làm tròn không chính xác đối với khả năng sẵn có và dung lượng của tài nguyên. |
| Quản lý dự án và kế toán | [607324](https://fix.lcs.dynamics.com/Issue/Details/?bugId=607324) | Khi mà **Tạo ước tính dự án bằng cách sử dụng nhiều nhiệm vụ hàng loạt** tính năng được bật, việc tạo ước tính trong một lô có nhiều nhiệm vụ phụ chỉ hoạt động cho giai đoạn hiện tại. |
| Đi lại và chi tiêu | [551911](https://fix.lcs.dynamics.com/Issue/Details/?bugId=551911) | Chính sách yêu cầu đi lại bị bỏ qua và quy trình làm việc được chấp thuận mà không có lỗi. |
| Đi lại và chi tiêu | [563752](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563752) | <p>Ứng dụng Chi phí di động không lưu thông tin sau vào dòng chi phí:</p><ul><li>ID dự án</li><li>Liệu chi phí có thể lập hóa đơn hay không</li><li>Số hoạt động</li></ul> |
| Đi lại và chi tiêu | [569458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569458) | Các **Biên lai đính kèm** trường được đặt thành **Đúng** ngay cả khi không có biên lai nào được đính kèm với dòng chi phí. |
| Đi lại và chi tiêu | [571334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571334) | Một lỗi xảy ra khi bạn thay đổi danh mục chi phí thành **Riêng tư**. |
| Đi lại và chi tiêu | [572783](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572783) | Bạn không thể đính kèm biên lai và chỉnh sửa chi phí của cha mẹ sau khi giao dịch thẻ tín dụng được tách thành chi phí cá nhân. |
| Đi lại và chi tiêu | [574252](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574252) | Chính sách chi phí cho các giao dịch giữa các công ty có ID dự án không hoạt động chính xác. |
| Đi lại và chi tiêu | [574489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574489) | Thông tin ngày đã đăng bị thiếu đối với các báo cáo chi phí đã đăng. |
| Đi lại và chi tiêu | [574504](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574504) | Có vấn đề về phương thức thanh toán trong ứng dụng Expense dành cho thiết bị di động. |
| Đi lại và chi tiêu | [584799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584799) | Yêu cầu đi lại được tạo cho một công nhân có thể được sử dụng cho báo cáo chi phí của một công nhân khác trước ngày ủy quyền. |
| Đi lại và chi tiêu | [586023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586023) | Khi bạn tạo một khoản chi phí, các thay đổi đối với giá trị thứ nguyên tài chính không được cập nhật chính xác ở cấp phân bổ kế toán trong **Quản lý chi tiêu** không gian làm việc. |
| Đi lại và chi tiêu | [586081](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586081) | Trạng thái phê duyệt dòng chi phí chính không được đồng bộ hóa với trạng thái phê duyệt dòng công việc theo từng dòng. |
| Đi lại và chi tiêu | [590544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590544) | Lỗi xảy ra nếu bạn đăng báo cáo chi phí và tính năng thu hồi thuế được bật. |
| Đi lại và chi tiêu | [564851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564851) | Người được ủy quyền không thể xóa tài liệu chi phí cho một nhân viên đã bị chấm dứt hợp đồng. |
| Đi lại và chi tiêu | [587306](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587306) | Việc xóa dòng chi phí mất nhiều thời gian hơn dự kiến và ảnh hưởng đến hiệu suất. |
| Đi lại và chi tiêu | [600455](https://fix.lcs.dynamics.com/Issue/Details/?bugId=600455) | **TrvExpTrans** gây ra một đứa trẻ mồ côi **Đã nộp thuế** ghi lại, bởi vì chỉ **SourceDocumentLine** bị xóa. |
| Đi lại và chi tiêu | [609918](https://fix.lcs.dynamics.com/Issue/Details/?bugId=609918) | **ReleaseUpdateDB72_Expense.updateTrvExpTransProjTransId ()** không tôn trọng **trvExpTrans.ReferenceDataAreaId** để tạo dãy số mới. |

## <a name="regulatory-updates"></a>Bản cập nhật theo quy định

Để biết thông tin về các cập nhật quy định cho các ứng dụng Tài chính và Hoạt động, hãy xem [Cập nhật quy định](/dynamics365/finance/localizations/regulatory-updates). Bạn cũng có thể đăng nhập vào Microsoft Dynamics Dịch vụ Vòng đời (LCS) và sử dụng công cụ tìm kiếm Vấn đề để xem các bản cập nhật quy định theo kế hoạch. Tìm kiếm vấn đề cho phép bạn tìm kiếm theo quốc gia hoặc khu vực, loại tính năng và bản phát hành.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
