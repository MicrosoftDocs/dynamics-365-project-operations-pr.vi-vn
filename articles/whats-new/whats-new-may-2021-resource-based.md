---
title: Tính năng mới từ tháng 5 năm 2021 – Project Operations cho các kịch bản dựa trên nguồn lực/hàng không nhập kho
description: Bài viết này cung cấp thông tin về các bản cập nhật chất lượng có trong bản phát hành Project Operations vào tháng 5 năm 2021 dành cho các kịch bản dựa trên nguồn lực/hàng không nhập kho.
author: sigitac
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: cc5e8104702951fd787d02407d26671e46d44f0c
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 06/18/2022
ms.locfileid: "9030015"
---
# <a name="whats-new-may-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Tính năng mới từ tháng 5 năm 2021 – Project Operations cho các kịch bản dựa trên nguồn lực/hàng không nhập kho

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Bài viết này áp dụng cho các phiên bản và thành phần sau của Dynamics 365 Project Operations:

- Project Operations trên môi trường Dynamics 365 Dataverse phiên bản 4.10.0.186
- Quản lý dự án và kế toán trong môi trường ứng dụng tài chính và hoạt động phiên bản 10.0.18

## <a name="features-included-in-this-release"></a>Các tính năng có trong bản phát hành này

Sau đây là các tính năng có trong bản phát hành này:

- [Chế độ lập lịch trình](../project-management/scheduling-modes.md): Người quản lý dự án có thể xác định xem một dự án sẽ được quản lý bằng chế độ lập lịch trình theo đơn vị cố định, công việc cố định hay khoảng thời gian cố định.
- [Thiết lập khoảng cách bằng các bậc tỷ lệ khoảng cách](../expense/set-up-mileage.md): Cập nhật các bậc tỷ lệ khoảng cách cho báo cáo chi phí của nhân viên.

## <a name="project-operations-dual-write-maps-updates"></a>Cập nhật về bản đồ ghi kép của Project Operations

Danh sách sau đây hiển thị các bản đồ ghi kép đã được sửa đổi hoặc bổ sung trong bản phát hành Project Operations vào tháng 5 năm 2021.

| Bản đồ thực thể | Phiên bản đã cập nhật | Nhận xét |
| --- | --- | --- |
| Nguồn tài trợ dự án (msdyn\_projectcontractsplitbillingrules) | 1.0.0.2 | Đồng bộ hóa các điều khoản thanh toán của khách hàng trong hợp đồng dự án. |
| Đề xuất hóa đơn dự án V2 (hóa đơn) | 1.0.0.3 | Đồng bộ hóa các điều khoản thanh toán của hóa đơn ước giá. |
| Thực thể xuất mô tả hóa đơn nhà cung cấp của Project Operations (msdyn\_projectvendorinvoicelines) | 1.0.0.1 | Bản cập nhật chất lượng |
| Dự án V2 (msdyn\_projects) | 1.0.0.2 | Bản cập nhật chất lượng |

Luôn chạy phiên bản bản đồ mới nhất trong môi trường của bạn và bật tất cả các bản đồ bảng liên quan khi bạn cập nhật phiên bản giải pháp Project Operations Dataverse và giải pháp ứng dụng tài chính và hoạt động. Một số tính năng và chức năng nhất định có thể không hoạt động chính xác nếu phiên bản mới nhất của bản đồ không được kích hoạt. Bạn có thể thấy phiên bản hiện hoạt của bản đồ ở cột **Phiên bản** trên trang **Ghi kép**. Để kích hoạt phiên bản mới của bản đồ, hãy chọn **Phiên bản bản đồ bảng**, chọn phiên bản mới nhất rồi lưu phiên bản đã chọn. Nếu đã tùy chỉnh sơ đồ bảng có sẵn, hãy áp dụng lại các thay đổi. Để biết thêm thông tin, hãy xem [Quản lý vòng đời áp dụng](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Nếu bạn gặp sự cố khi khởi động bản đồ, hãy làm theo hướng dẫn trong phần [Vấn đề thiếu cột trong bảng trên bản đồ](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) của hướng dẫn khắc phục sự cố Ghi kép.

## <a name="quality-updates"></a>Bản cập nhật chất lượng

### <a name="project-operations-on-dataverse"></a>Project Operations trên Dataverse

| **Lĩnh vực tính năng** | **Số tham chiếu** | **Cập nhật chất lượng** |
| --- | --- | --- |
| Định giá và thanh toán | 2227635 | Các giá trị ở trường **Nhóm đơn vị đo** và **Đơn vị** được lấy mặc định từ sản phẩm trong lưới **Ước tính vật liệu**. |
| Định giá và thanh toán | 2234127 | Trường **ID nhiệm vụ** hiện được tích hợp chính xác với giá trị thực tế của dự án Dataverse khi hóa đơn của nhà cung cấp được đăng. |
| Định giá và thanh toán | 2235564 | Thao tác lưu dòng nhật ký kế toán giúp bảo đảm rằng đơn vị tiền tệ được hiển thị trong mục nhập dòng nhật ký kế toán khớp với đơn vị tiền tệ mặc định của dòng sau khi lưu. |
| Định giá và thanh toán | 2246671 | Việc chuyển một giao dịch thành dạng không tính phí trong quá trình lập hóa đơn sẽ đảo ngược bản ghi bán hàng chưa lập hóa đơn ban đầu và tạo bản ghi bán hàng chưa lập hóa đơn mới dưới dạng không tính phí. |
| Định giá và thanh toán | 2264042 | Không được chặn mục chỉnh sửa hóa đơn hợp lệ nếu có chi tiết sửa hóa đơn không hợp lệ trong môi trường. |
| Định giá và thanh toán | 2146367 | Chức năng ánh xạ ghi kép thông tin cơ bản của hóa đơn dự án được mở rộng để bao gồm các điều khoản thanh toán. |
|   Quản lý cơ hội | 2086888 | Không thêm các vai trò và danh mục đã bị hủy kích hoạt trước khi bạn sao chép báo giá vào các vai trò và danh mục có thể tính phí của báo giá mới được sao chép. |
|   Quản lý cơ hội | 2234376 | Các trường chỉ đọc được chuyển thành màu xám trong lưới **Ước tính vật liệu**. |
|   Quản lý cơ hội | 2238337 | Báo giá dựa trên một người liên hệ có thể được lưu ngay cả khi mục này không được liên kết với bảng giá dự án. |
|   Quản lý cơ hội | 2239810 | Thao tác đóng một báo giá dưới dạng bị mất cũng sẽ đóng dự án được liên kết và hủy mọi mục đăng ký. |
| Hoạch định và theo dõi dự án | 2099559 | Đã thêm phần xác thực bổ sung đối với tình trạng hệ thống trước khi lưới **Nhiệm vụ dự án** mở ra. |
| Hoạch định và theo dõi dự án | 2178987 | Đã sửa một lỗi nhất thời xảy ra khi chọn **Giai đoạn tiếp theo** trên trang **Dự án**. |
| Quản lý nguồn lực | 2224817 | Chức năng mở rộng mục đăng ký lấy mặc định trạng thái đăng ký chính xác. |
| Mục nhập thời gian | 2202476 | Trang **Mục nhập thời gian** giờ sử dụng bộ điều khiển lưới phản ứng và khắc phục các vấn đề như lệch lưới. |
| Mục nhập thời gian | 2223377 | Mục nhập thời gian bị ẩn khỏi phần **Có liên quan** trên trang **Nguồn lực có thể đăng ký** để tránh nhầm lẫn với khả năng sử dụng. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Quản lý dự án và kế toán trong Dynamics 365 Finance

| Lĩnh vực tính năng | Số tham chiếu | Cập nhật chất lượng |
| --- | --- | --- |
| Quản lý dự án và kế toán | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | Project Operations dành cho các tình huống dựa trên Nguồn lực: Không thể chuyển báo giá sang trạng thái đã giành được do có lỗi tích hợp. |
| Quản lý dự án và kế toán | [546604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546604) | Project Operations: Lỗi xảy ra khi bạn cố gắng liên kết một mục mô tả hợp đồng với ID dự án do việc kiểm tra mục mô tả hợp đồng và loại giao dịch chồng chéo. |
| Quản lý dự án và kế toán | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** thiết lập địa chỉ hóa đơn nguồn tiền từ một khách hàng khác. |
| Đi lại và chi tiêu | [480451](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480451) | Có thể xảy ra lỗi đăng liên quan đến việc thiết lập khoảng cách. |
| Đi lại và chi tiêu | [522084](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522084) | Chức năng **Chia cho cá nhân** không hoạt động đối với các giao dịch chi phí ngoại tệ. |
| Đi lại và chi tiêu | [523938](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523938) | Các giá trị trong phần thả xuống danh mục chi phí hiển thị các danh mục không chính xác cho đại diện, bất kể họ có phải là nguồn lực hay không. |
| Đi lại và chi tiêu | [539266](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539266) | Bạn không thể lưu báo cáo chi phí liên công ty do lỗi **xác thực Nguồn lực/danh mục**. |
| Đi lại và chi tiêu | [532610](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532610) | Việc tính sai tỷ lệ khoảng cách trong việc đăng báo cáo chi phí có các mô tả chia nhỏ. |
| Đi lại và chi tiêu | [537404](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537404) | Bạn không thể đăng báo cáo chi phí liên công ty khi có thuế bán hàng được bao gồm và loại tài khoản bù trừ trên phương thức thanh toán là **Nhân viên**. |
| Đi lại và chi tiêu | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | Hoàn quy thực thể dữ liệu **TrvRequisitionLine** và chỉ mục duy nhất được liên kết. |
| Đi lại và chi tiêu | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | Báo cáo chi phí hỗ trợ thao tác tạo và cập nhật dòng tài liệu nguồn. |
| Đi lại và chi tiêu | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | Bút toán sổ cái chi tiết không chính xác sẽ được hiển thị trong tình huống liên công ty nếu thuế bán hàng được kết sổ cho pháp nhân đích. |
| Đi lại và chi tiêu | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | Project Operations: Giá trị ước tính chi phí không bị xóa khỏi mục Tài chính khi mục này bị xóa khỏi Dataverse. |
| Đi lại và chi tiêu | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | Khi danh mục chi phí là một danh mục phi dự án, các thứ nguyên tài chính đã chọn trên trang **Chi phí** sẽ không được sao chép vào báo cáo chi phí. |
