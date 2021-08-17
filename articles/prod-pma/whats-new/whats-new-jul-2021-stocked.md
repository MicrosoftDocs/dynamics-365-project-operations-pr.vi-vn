---
title: Tính năng mới hoặc thay đổi trong Project Operations, tháng 7 năm 2021 cho các kịch bản dựa trên hàng trữ kho/sản xuất
description: Chủ đề này cung cấp thông tin về các bản cập nhật chất lượng có trong bản phát hành tháng 7 năm 2021 của Project Operations cho các kịch bản dựa trên hàng trữ kho/sản xuất.
author: andchoi
ms.date: 07/01/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: andchoi
ms.openlocfilehash: dadcf3e9fa8432fb66f76b7c2f0fdb98bc00511d93984ea98fa30b4fc03fa426
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992727"
---
# <a name="whats-new-or-changed-in-project-operations-july-2021-for-stockedproduction-based-scenarios"></a>Tính năng mới hoặc thay đổi trong Project Operations, tháng 7 năm 2021 cho các kịch bản dựa trên hàng trữ kho/sản xuất

_**Áp dụng cho:** Project Operations cho tình huống dựa trên hàng trữ kho/sản xuất_

Chủ đề này áp dụng cho các phiên bản và thành phần sau của Dynamics 365 Project Operations:

- Quản lý dự án và kế toán trong các môi trường Dynamics 365 Finance phiên bản 10.0.20
 
### <a name="quality-updates"></a>Bản cập nhật chất lượng
                                                                                                                                                                                  
| Lĩnh vực tính năng                      | Số tham chiếu| Cập nhật chất lượng                                                                                                                                                                          |
|-----------------------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Quản lý dự án và kế toán | [485394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485394) | Hồ sơ cam kết chi phí từ yêu cầu mua được xóa ngay sau khi đơn đặt hàng được giải phóng khỏi vấn đề yêu cầu mua.                                                                           |
| Quản lý dự án và kế toán | [529602](https://fix.lcs.dynamics.com/Issue/Details/?bugId=529602) | Xác thực ngân sách xảy ra hai lần đối với yêu cầu mua hàng. Sự trùng lặp này có nghĩa là không thể đóng yêu cầu và đơn đặt hàng tương ứng không được tạo.                                                                                                                        |
| Quản lý dự án và kế toán | [539439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539439) | Quy tắc thanh toán **Phần trăm thanh toán trên** không thể hoàn thành do vấn đề làm tròn.                                                                              |
| Quản lý dự án và kế toán | [540023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540023) | Khi bạn điều chỉnh giao dịch và tỷ lệ phần trăm có số thập phân, chi phí và giá bán không được điều chỉnh chính xác.                                      |
| Quản lý dự án và kế toán | [540927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540927) | Trình khám phá nguồn kế toán hiển thị giờ cho một dòng bảng chấm công cho nhiều dòng bảng chấm công với các hoạt động khác nhau.                                      |
| Quản lý dự án và kế toán | [541471](https://fix.lcs.dynamics.com/Issue/Details/?bugId=541471) | Chế độ xem đã lưu và cá nhân hóa chi tiết dòng bảng chấm công khiến hệ thống luôn mở chi tiết cho bảng chấm công đầu tiên trong danh sách khi cố gắng mở bảng chấm công.  |
| Quản lý dự án và kế toán | [548677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548677) | Nút gốc của dự án biến mất và các bản ghi cấu trúc phân tích công việc bị xóa sau khi nhập.                                                                                             |
| Quản lý dự án và kế toán | [548999](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548999) | Khi các mặt hàng được nhận và phát hành một phần từ yêu cầu mặt hàng, hệ thống sẽ cập nhật số dư tiêu dùng ngân sách sai. |
| Quản lý dự án và kế toán | [550959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550959) | Các đơn đặt hàng mua lại dự án không hiển thị tổng số một cách chính xác trong ngăn **Tổng số** hoặc lưới **Hóa đơn đang chờ xử lý**.                                                                  |
| Quản lý dự án và kế toán | [554593](https://fix.lcs.dynamics.com/Issue/Details/?bugId=554593) | Khi khóa sổ hàng tồn kho, các điều chỉnh chi phí hạng mục dự án được kết sổ vào tài khoản số dư thay vì tài khoản lãi lỗ.                                                            |
| Quản lý dự án và kế toán | [557394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557394) | Một dự án đã đăng chứng từ giao dịch và chứng từ ước tính sử dụng USD làm đơn vị tiền tệ kế toán nhưng số tiền cho thấy giá trị tương đương CAD.              |
| Quản lý dự án và kế toán | [560140](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560140) | Chi phí đã cam kết với một yêu cầu về mặt hàng và đơn đặt hàng bị sai trong quy trình lập hóa đơn đơn đặt hàng với việc nhận một phần sản phẩm và lập hóa đơn một phần.       |
| Quản lý dự án và kế toán | [560567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560567) | Việc điều chỉnh dự án không cập nhật chính xác số tiền bán hàng có chi phí gián tiếp.                                                                                    |
| Quản lý dự án và kế toán | [561137](https://fix.lcs.dynamics.com/Issue/Details/?bugId=561137) | Bảng **Phiếu chấm công** thiếu mối quan hệ đã xác định với dạng xem **Nhân viên/Nguồn lực**.                                                                                   |
| Quản lý dự án và kế toán | [563330](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563330) | Không thể điền vào trường **Số hoạt động** khi bạn chọn từ menu thả xuống cho bảng chấm công liên công ty.                                                                 |
| Quản lý dự án và kế toán | [563840](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563840) | Bạn không thể thêm trường **Mục đích** hoặc **Mô tả hoạt động** vào các trang sau: **Giao dịch đã kết sổ của dự án**, **Tạo đề xuất hóa đơn** hoặc **Đề xuất hóa đơn**.  |
| Quản lý dự án và kế toán | [566348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566348) | Kiểm soát ngày giao hàng sai được cung cấp khi bạn tạo các yêu cầu về mặt hàng bằng cách sử dụng quản lý dữ liệu (**ProjSalesItemRequirementEntity**).                                              |
| Quản lý dự án và kế toán | [566544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566544) | Khi bạn chọn ID hợp đồng dự án trong Tài chính, môi trường tích hợp Project Operations sẽ mở trang để tạo bản ghi mới thay vì mở hợp đồng dự án hiện có.                                                                                                                 |
| Quản lý dự án và kế toán | [567300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567300) |  Nhãn, "@SYS4083080" ("Không thể tìm thấy bản ghi Nhân viên duy nhất tương ứng với các giá trị đã nhập") không được dịch sang tiếng Đan Mạch.                                |
| Quản lý dự án và kế toán | [569901](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569901) | Không thể chỉnh sửa trường **Nhóm thuế bán hàng** trên một đề xuất hóa đơn.                                                                               |
| Quản lý dự án và kế toán | [557049](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557049) | Chi phí cam kết bị phóng đại với số thuế không được khấu trừ.                                                                                                    |
| Quản lý dự án và kế toán | [565080](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565080) | Đăng một bảng chấm công liên công ty với nhiều dự án và các khía cạnh tài chính khác nhau tạo ra các giá trị không mong đợi trong sổ cái.                             |
| Quản lý dự án và kế toán | [567962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567962) | Các dòng đề xuất hóa đơn bị trùng lặp do có nhiều trường hợp của quy trình định kỳ, **Nhập từ tách chuyển** đang chạy cùng lúc.                                      |
| Quản lý dự án và kế toán | [571339](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571339) | Đã xảy ra lỗi khi đăng đề xuất hóa đơn ghi có, vì vậy các giao dịch trên chứng từ không có số dư.    |
| Quản lý dự án và kế toán | [573567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573567) | Các chi phí đã cam kết của dự án sẽ không chính xác sau khi các hóa đơn tạm dừng chờ xử lý được phát hành.                                                                             |
| Quản lý dự án và kế toán | [573886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573886) | Bạn không thể tạo giấy báo có cho đơn bán hàng trong dự án khi thuế bằng đơn vị tiền tệ khác với đơn vị tiền tệ của công ty.                                      |
| Quản lý dự án và kế toán | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | Xóa hợp đồng cũng xóa địa chỉ được liên kết với khách hàng.                                                                                     |
| Quản lý dự án và kế toán | [585811](https://fix.lcs.dynamics.com/Issue/Details/?bugId=585811) | Không thể đăng đề xuất hóa đơn do chỉnh sửa giao dịch theo thời gian âm.                                                                    |
| Đi lại và chi tiêu                  | [532075](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532075) | Thuế được tính khác nhau trong các báo cáo chi phí.                                                                                                                  |
| Đi lại và chi tiêu                  | [546450](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546450) | Cập nhật phát hành **DB72_Expense.updateTrvExpTransProjTransId()** không cho phép **trvExpTrans.ReferenceDataAreaId** tạo trình tự số mới.                    |
| Đi lại và chi tiêu                  | [568805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568805) | Số tiền đã nộp không hiển thị với trường bắt buộc.                                                                                                             |
| Đi lại và chi tiêu                  | [568831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568831) | Cải thiện hiệu suất của việc đính kèm một khoản chi phí vào báo cáo chi phí bằng cách sử dụng giao diện người dùng Expense Reimagined.                                                            |
| Đi lại và chi tiêu                  | [570790](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570790) | Bạn có thể xóa các báo cáo chi phí đã đăng.                                                                                           |
| Đi lại và chi tiêu                  | [571317](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571317) | Thông báo Chính sách chi phí được hiển thị nhiều lần.                                                                                                       |
| Đi lại và chi tiêu                  | [573969](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573969) | Trường **Phương thức thanh toán** có trên ngăn **Chi phí mới**.                                                                                                      |
| Đi lại và chi tiêu                  | [523557](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523557) | Công cụ **Đặt lại trạng thái tài liệu chi phí** sẽ đặt lại trạng thái báo cáo chi phí thành **Bản nháp** nếu không tìm thấy quy trình làm việc. 

### <a name="regulatory-updates"></a>Bản cập nhật theo quy định
Để biết thông tin về các bản cập nhật theo quy định cho ứng dụng Finance and Operations, hãy xem [Bản cập nhật theo quy định](/dynamics365/finance/localizations/regulatory-updates). Bạn cũng có thể đăng nhập vào Lifecycle Services (LCS) và xem các bản cập nhật quy định theo kế hoạch bằng cách sử dụng công cụ tìm kiếm Sự cố. Tìm kiếm vấn đề cho phép bạn tìm kiếm theo quốc gia, loại tính năng và bản phát hành.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
