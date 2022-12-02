---
title: Có gì mới hoặc thay đổi trong Project Operations, tháng 9 năm 2021 cho các kịch bản dựa trên hàng trữ kho/sản xuất
description: Bài viết này cung cấp thông tin về các bản cập nhật chất lượng được cung cấp trong lần triển khai bản phát hành Project Operations tháng 9 năm 2021 cho tình huống dựa trên sản xuất/hàng trữ kho.
author: andchoi
ms.date: 11/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: be0f397df4a3e1973e1f5546e43b2cf9578950a0
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029878"
---
# <a name="whats-new-or-changed-in-project-operations-september-2021-for-stockedproduction-based-scenarios"></a>Có gì mới hoặc thay đổi trong Project Operations, tháng 9 năm 2021 cho các kịch bản dựa trên hàng trữ kho/sản xuất

_**Áp dụng cho:** Project Operations cho tình huống dựa trên hàng trữ kho/sản xuất_

Bài viết này áp dụng cho các phiên bản và thành phần sau của Microsoft Dynamics 365 Project Operations:

- Quản lý dự án và kế toán trong môi trường ứng dụng Dynamics 365 Finance phiên bản 10.0.21
 
## <a name="quality-updates"></a>Bản cập nhật chất lượng

| Lĩnh vực tính năng | Số tham chiếu | Cập nhật chất lượng |
|---|---|---|
| Quản lý dự án và kế toán | [412077](https://fix.lcs.dynamics.com/Issue/Details/?bugId=412077) | Nếu vai trò người quản lý Mua hàng được cấp quyền truy cập vào một thực thể, nó cũng có quyền truy cập vào tất cả các dự án trong tất cả các thực thể. |
| Quản lý dự án và kế toán | [537214](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537214) | Một vấn đề làm tròn thuế giá trị gia tăng (VAT) xảy ra trong khi ghi chú tín dụng được thanh toán dựa trên hóa đơn ban đầu của dự án. |
| Quản lý dự án và kế toán | [538002](https://fix.lcs.dynamics.com/Issue/Details/?bugId=538002) | Sử dụng ngân sách dự án thay thế để xác minh ngân sách. |
| Quản lý dự án và kế toán | [546265](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546265) | Nhóm giá **Giá bán hàng theo giờ** không được tính toán trên cấu trúc phân tích công việc cho báo giá dự án. |
| Quản lý dự án và kế toán | [555604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=555604) | Loại bỏ dự toán không thành công khi bật tính năng **Bật đơn vị tiền tệ của hợp đồng dự án để dự toán**. |
| Quản lý dự án và kế toán | [563523](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563523) | Phân bổ thuế bán hàng theo số lượng được cộng vào giá bán khi thuế sử dụng được sử dụng trên nhóm thuế doanh thu của nhật ký Chi phí dự án. |
| Quản lý dự án và kế toán | [564701](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564701) | Thuế có điều kiện không được tính chính xác cho lần thanh toán cuối cùng khi việc giữ lại và thanh toán trước của nhà cung cấp được áp dụng cho hóa đơn đặt hàng. |
| Quản lý dự án và kế toán | [565642](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565642) | Dấu vết điều chỉnh không hoạt động đối với nhật ký Số dư đầu kỳ. |
| Quản lý dự án và kế toán | [568814](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568814) | **Phân bổ sửa đổi ngân sách dự án theo kỳ** được chia thành tất cả các kỳ ngân sách. Khi phân bổ được gửi, bản ghi sẽ không bị xóa. |
| Quản lý dự án và kế toán | [569250](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569250) | Các bài đăng Công việc đang làm (WIP) lên sổ cái chung có số lượng không chính xác. |
| Quản lý dự án và kế toán | [570731](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570371) | Phê duyệt nhật ký giờ Dự án không hoạt động. |
| Quản lý dự án và kế toán | [571391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571391) | Giá bán hàng điều chỉnh dự án không được cập nhật chi phí gián tiếp khi giới hạn nguồn tiền không được đánh dấu. |
| Quản lý dự án và kế toán | [575831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575831) | Không thể tạo yêu cầu mặt hàng khi tiêu đề bảng Bán hàng được lập hóa đơn và đơn đặt hàng dự phòng cho các dòng hiện có đã được hoàn tất. |
| Quản lý dự án và kế toán | [578036](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578036) | Số tiền trả trước cho một quy tắc lập hóa đơn có mốc cho một dự án khác không được đăng trong ID dự án tương ứng đã được chọn cho mốc đó. Thay vào đó, nó được đăng cùng với dự án đầu tiên. |
| Quản lý dự án và kế toán | [578327](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578327) | Khi bạn chọn **Bộ thứ nguyên tài chính** trên một đề xuất hóa đơn, lỗi sau xảy ra: "Không thể truyền đối tượng thuộc loại 'Dynamics.AX.Application.FormIntControl' sang loại 'Dynamics.AX.Application.FormStringControl'." |
| Quản lý dự án và kế toán | [581167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581167) | Báo cáo **Hóa đơn dự án** bỏ qua các mô tả. |
| Quản lý dự án và kế toán | [581489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581489) | Lỗi xảy ra khi bạn tính phương án kiểm soát chi phí cho một dự án đầu tư. |
| Quản lý dự án và kế toán | [590357](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590357) | Phương thức **ProjTable::InitFromCustTable - canDeletePostalAddress** gây ra sự cố về hiệu suất. |
| Quản lý dự án và kế toán | [592493](https://fix.lcs.dynamics.com/Issue/Details/?bugId=592493) | Thông báo lỗi phải rõ ràng hơn "Lỗi không mong muốn". |
| Quản lý dự án và kế toán | [598810](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598810) | Tác vụ hàng loạt đăng hóa đơn Dự án xử lý và đăng đề xuất hóa đơn ngay cả khi chưa tạo các mô tả hóa đơn. |
| Quản lý dự án và kế toán | [574282](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574282) | Sự cố làm tròn xảy ra khi khóa cấu hình giấy phép khu vực công bị tắt. Chi phí hoặc giá bán không chính xác được tạo trên số giờ của bảng chấm công cho các hợp đồng có nhiều nguồn tạo lập. |
| Quản lý dự án và kế toán | [577598](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577598) | Giá bán dự án trên đơn đặt hàng dự án đã lập hóa đơn được tính không chính xác khi mô hình giá bán là **Tỷ lệ đóng góp**. |
| Quản lý dự án và kế toán | [580784](https://fix.lcs.dynamics.com/Issue/Details/?bugId=580784) | Hệ thống không xem xét các ngày hoạt động giữa thời điểm tính toán giá nhân công có hiệu lực cho một nhân viên. |
| Quản lý dự án và kế toán | [584054](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584054) | Lỗi đăng xảy ra trên bảng chấm công liên công ty do lỗi xác thực sau: "Chưa thiết lập đối tác thương mại cho pháp nhân." |
| Quản lý dự án và kế toán | [586303](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586303) | Mô tả từ một đơn đặt hàng có thể loại chi phí không được truy xuất trong danh sách giao dịch dự án đã đăng. |
| Quản lý dự án và kế toán | [590349](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590349) | Có một sự chuyển đổi không chính xác trên các nhật ký Mặt hàng được đăng cho một dự án. |
| Quản lý dự án và kế toán | [557294](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557294) | Bạn có thể xác nhận đơn đặt hàng ngay cả khi đã vượt quá giới hạn nguồn vốn. |
| Quản lý dự án và kế toán | [574162](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574162) | Phần **Chỉnh sửa/Hủy hóa đơn** trên hóa đơn văn bản miễn phí sẽ biến mất khi ID dự án được chọn. |
| Quản lý dự án và kế toán | [575425](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575425) | Có các vấn đề về hiệu suất khi một đề xuất hóa đơn dự án được đăng từ một đơn đặt hàng dự án bao gồm một mặt hàng có trong kho. |
| Quản lý dự án và kế toán | [575939](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575939) | Không thể đăng hóa đơn mua hàng của dự án vì xảy ra lỗi sau: "Chức năng AccDistProcessorProjectExtension.createForProjectRevenueLine đã được gọi không chính xác." |
| Quản lý dự án và kế toán | [578970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578970) | Cập nhật quá trình tạo công việc hàng loạt dự toán dự án để hỗ trợ thực hiện nhiều nhiệm vụ con. |
| Quản lý dự án và kế toán | [584519](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584519) | Không thể cập nhật trạng thái của bảng chấm công thành **Bản nháp** khi quy trình làm việc bị kẹt ở trạng thái **Đã hủy**. |
| Quản lý dự án và kế toán | [584757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584757) | Số tiền trả trước không được tính trong đề xuất hóa đơn ghi chú tín dụng nếu có nhiều mô tả. |
| Quản lý dự án và kế toán | [586034](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586034) | Khi bạn cố gắng thay đổi số tiền trên hóa đơn đã tạo từ đơn đặt hàng, lỗi sau xảy ra: "Các giao dịch trên chứng từ không cân bằng theo XX/XX/XXXX. (đơn vị tiền tệ kế toán: 0,00 - đơn vị tiền tệ báo cáo: 0,01)." |
| Quản lý dự án và kế toán | [588714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588714) | Có vấn đề về hiệu suất khi một đề xuất hóa đơn dự án được đăng ở chế độ lô, do liên kết với **GeneralJournalAccountEntry**. |
| Quản lý dự án và kế toán | [588851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588851) | Có vấn đề về hiệu suất khi bảng chấm công được đăng. |
| Quản lý dự án và kế toán | [590535](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590535) | Hệ thống cấp bậc ước tính chi phí của cấu trúc phân tích công việc không được căn chỉnh chính xác sau khi tất cả các nhiệm vụ được mở rộng hoặc sau khi một nhiệm vụ được mở rộng theo cách thủ công. |
| Quản lý dự án và kế toán | [593663](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593663) | Không thể thêm mẫu Excel báo giá dự án vào menu **Mở trong Excel**. |
| Quản lý dự án và kế toán | [596669](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596669) | Số miễn thuế cho một thực thể không được bao gồm trên hóa đơn dự án đã in. |
| Quản lý dự án và kế toán | [597563](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597563) | Không có dữ liệu tài chính được cập nhật trong lỗi đơn vị hàng tồn kho khi một dự án được điều chỉnh liên quan đến mô tả tín dụng. |
| Quản lý dự án và kế toán | [598109](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598109) | Sau khi áp dụng KB 461935, bạn không thể đăng ước tính nếu chuyển sang chuỗi số liên tục. |
| Quản lý dự án và kế toán | [598688](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598688) | **TimeEntryDataManager** khiến ứng dụng di động Bảng chấm công dự án cho Android ngừng phản hồi. |
| Quản lý dự án và kế toán | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Giá trị WIP đảo ngược từ việc đăng hóa đơn khác với giá trị WIP đã đăng ban đầu từ mục nhập thời gian. |
| Quản lý dự án và kế toán | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Trong các trường hợp trả trước được áp dụng, các giao dịch trên phiếu không cân bằng khi doanh thu đã lập hóa đơn cho một dự án được đăng. |
| Quản lý dự án và kế toán | [603320](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603320) | Khi tính năng **Nâng cao hiệu suất lập kế hoạch nguồn lực dự án** được bật, các giá trị thập phân được làm tròn không chính xác cho tình trạng rảnh/bận và năng lực của nguồn lực. |
| Quản lý dự án và kế toán | [607324](https://fix.lcs.dynamics.com/Issue/Details/?bugId=607324) | Khi tính năng **Tạo ước tính dự án bằng nhiều nhiệm vụ theo lô** được bật, việc tạo các ước tính theo lô có nhiều nhiệm vụ con chỉ hoạt động cho kỳ hiện tại. |
| Đi lại và chi tiêu | [551911](https://fix.lcs.dynamics.com/Issue/Details/?bugId=551911) | Chính sách yêu cầu đi lại bị bỏ qua và quy trình làm việc được phê duyệt mà không có lỗi. |
| Đi lại và chi tiêu | [563752](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563752) | <p>Ứng dụng Chi phí dành cho thiết bị di động không lưu thông tin sau vào mô tả chi phí:</p><ul><li>ID dự án</li><li>Liệu chi phí có thể lập hóa đơn hay không</li><li>Số hoạt động</li></ul> |
| Đi lại và chi tiêu | [569458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569458) | Trường **Biên nhận đính kèm** được đặt thành **Có** ngay cả khi không có biên nhận được đính kèm vào mô tả chi phí. |
| Đi lại và chi tiêu | [571334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571334) | Xuất hiện một lỗi khi bạn cố gắng thay đổi danh mục chi phí thành **Cá nhân**. |
| Đi lại và chi tiêu | [572783](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572783) | Bạn không thể đính kèm biên nhận và chỉnh sửa chi phí chính sau khi giao dịch thẻ tín dụng được phân chia vào chi phí cá nhân. |
| Đi lại và chi tiêu | [574252](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574252) | Chính sách chi phí cho các giao dịch giữa các công ty có ID dự án không hoạt động chính xác. |
| Đi lại và chi tiêu | [574489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574489) | Thông tin ngày đăng bị thiếu đối với các báo cáo chi phí đã đăng. |
| Đi lại và chi tiêu | [574504](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574504) | Có vấn đề về phương thức thanh toán trong ứng dụng Chi phí dành cho thiết bị di động. |
| Đi lại và chi tiêu | [584799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584799) | Yêu cầu đi lại được tạo cho một công nhân có thể được sử dụng cho báo cáo chi phí của công nhân khác trước ngày ủy quyền. |
| Đi lại và chi tiêu | [586023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586023) | Khi bạn tạo một khoản chi phí, các thay đổi về giá trị thứ nguyên tài chính không được cập nhật chính xác ở cấp độ phân bổ kế toán trong không gian làm việc **Quản lý chi tiêu** . |
| Đi lại và chi tiêu | [586081](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586081) | Trạng thái phê duyệt mô tả chi phí chính không được đồng bộ hóa với trạng thái phê duyệt quy trình làm việc theo mô tả chi tiết. |
| Đi lại và chi tiêu | [590544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590544) | Lỗi xảy ra nếu bạn đăng báo cáo chi phí và tính năng thu hồi thuế được bật. |
| Đi lại và chi tiêu | [564851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564851) | Người được ủy quyền không thể xóa tài liệu chi phí cho một nhân viên đã bị chấm dứt hợp đồng. |
| Đi lại và chi tiêu | [587306](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587306) | Việc xóa mô tả chi phí mất nhiều thời gian hơn dự kiến và ảnh hưởng đến hiệu suất. |
| Đi lại và chi tiêu | [600455](https://fix.lcs.dynamics.com/Issue/Details/?bugId=600455) | **TrvExpTrans** gây ra bản ghi **TaxUncommitted** không có nguồn gốc, vì chỉ có **SourceDocumentLine** bị xóa. |
| Đi lại và chi tiêu | [609918](https://fix.lcs.dynamics.com/Issue/Details/?bugId=609918) | Cập nhật phát hành **ReleaseUpdateDB72_Expense.updateTrvExpTransProjTransId()** không tính đến **trvExpTrans.ReferenceDataAreaId** tạo trình tự số mới. |

## <a name="regulatory-updates"></a>Bản cập nhật theo quy định

Để biết thông tin về các bản cập nhật theo quy định cho ứng dụng tài chính và hoạt động, hãy xem [Bản cập nhật theo quy định](/dynamics365/finance/localizations/regulatory-updates). Bạn cũng có thể đăng nhập vào Lifecycle Services (LCS) Microsoft Dynamics và sử dụng công cụ tìm kiếm Sự cố để xem các bản cập nhật quy định theo kế hoạch. Tìm kiếm vấn đề cho phép bạn tìm kiếm theo quốc gia hoặc khu vực, loại tính năng và bản phát hành.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
