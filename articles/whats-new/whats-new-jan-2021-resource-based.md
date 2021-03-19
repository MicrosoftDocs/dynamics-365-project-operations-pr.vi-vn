---
title: Có gì mới tháng 1 năm 2021 – Project Operations cho các kịch bản dựa trên nguồn lực/hàng không nhập kho
description: Chủ đề này cung cấp thông tin về các bản cập nhật chất lượng được cung cấp trong lần triển khai bản phát hành Project Operations tháng 1 năm 2021 cho tình huống dựa trên nguồn lực/hàng không trữ kho.
author: sigitac
manager: tfehr
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5e5bfd3c790dac51895cde04e08d1fa62f4457e8
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5292095"
---
# <a name="whats-new-january-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Có gì mới tháng 1 năm 2021 – Project Operations cho các kịch bản dựa trên nguồn lực/hàng không nhập kho

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_


Chủ đề này áp dụng cho các phiên bản và thành phần sau của Dynamics 365 Project Operations:

  - Project Operations trên môi trường Dataverse phiên bản 4.6.0.154
  - Quản lý dự án và kế toán trong các môi trường Dynamics 365 Finance phiên bản 10.0.16

## <a name="quality-updates"></a>Bản cập nhật chất lượng

### <a name="project-operations-on-dataverse"></a>Project Operations trên Dataverse

| **Lĩnh vực tính năng** | **Số tham chiếu** | **Cập nhật chất lượng** |
| --- | --- | --- |
| **Đợt triển khai và Cấu hình** | 2106818 | Đã sửa lỗi đặt lại tên nguồn tài nguyên web gây ra sự cố liên quan đến việc tùy chỉnh trang. |
| **Định giá và thanh toán** | 2091908 | Đã sửa lỗi hiển thị của tùy chọn **Khóa giá** và **Dùng giá hiện tại** trên trang **Hóa đơn** khi cài đặt Project Operations cùng với Dynamics 365 Field Service. |
| **Định giá và thanh toán** | 2103058 | Đã làm mới **Tổng dự án** để xử lý các giá trị rỗng cho chi phí thực tế của một nhiệm vụ. |
| **Định giá và thanh toán** | 2116100 | Đã cải thiện thông báo lỗi dùng với chức năng **Sửa mục nhập trên tab Thực tế**. |
| **Định giá và thanh toán** | 2116129 | Đã sửa lỗi hiển thị ước tính chi phí trên tab **Ước tính** của trang **Dự án**. |
| **Định giá và thanh toán** | 2119112 | Đã sửa lỗi tính tổng giá trị bán hàng thực tế và chi phí thực tế khi dùng tỷ giá hối đoái khác nhau. |
| **Định giá và thanh toán** | 2134705 | Đã sửa lỗi "Không thể đọc thuộc tính **getResourceString** không xác định" khi mở trang **Hóa đơn** và khi cài đặt Field Service. |
| **Quản lý cơ hội** | 2022195 | Lưới thanh toán theo nhiệm vụ trên trang **Dự án** bao gồm một biểu tượng cho biết có một dòng hợp đồng hoặc dòng báo giá liên kết với nhiệm vụ đó. |
| **Quản lý cơ hội** | 2029135 | Đã sửa lỗi quy trình kinh doanh xảy ra khi người dùng tìm cách mở một dòng hóa đơn trên hóa đơn đã xác nhận mà có khoản trả trước đã được lập hóa đơn. |
| **Quản lý cơ hội** | 2040713 | Đã sửa lỗi tập lệnh xảy ra khi tạo hóa đơn từ hợp đồng và khi cài đặt Field Service. |
| **Hoạch định và theo dõi dự án** | 2090202 | Đã đánh dấu các quy tắc công việc không còn dùng đến là **Không dùng nữa**. |
| **Thời gian và Chi phí** | 2091249 | Đã siết chặt các tùy chọn kiểm soát để người dùng không thể thay đổi nhiệm vụ trên mục nhập thời gian đã gửi hoặc đã phê duyệt. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Quản lý dự án và kế toán trong Dynamics 365 Finance

| **Lĩnh vực tính năng** | **Số tham chiếu** | **Cập nhật chất lượng** |
| --- | --- | --- |
| **Quản lý dự án và kế toán** | [478667](https://fix.lcs.dynamics.com/Issue/Details/?bugId=478667) | Số tiền trong hợp đồng trên trang **Trả dần** bị sai đối với dự án theo giá cố định có nhiều nguồn cấp vốn. |
| **Quản lý dự án và kế toán** | [480260](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480260) | Chỗ dành sẵn cho **Invoiceproposal.PSAnfRefProjId** không hiển thị ID dự án cho quy trình làm việc **Xem lại đề xuất hóa đơn dự án**. |
| **Quản lý dự án và kế toán** | [481227](https://fix.lcs.dynamics.com/Issue/Details/?bugId=481227) | Dùng ngày chiết khấu tiền mặt sai khi đăng bản đề xuất hóa đơn dự án. |
| **Quản lý dự án và kế toán** | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558) | Thao tác xóa và đọc phân công nguồn lực trong Project Operations sẽ nhân đôi số mục dự báo dự án trong phần Tài chính. |
| **Quản lý dự án và kế toán** | [484468](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484468) | Trong Project Operations, bạn không thể tạo ước tính dự án trong Dataverse khi không có dòng hợp đồng trên dự án. |
| **Quản lý dự án và kế toán** | [485871](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485871) | Thông số tài chính trên giao dịch chi tiêu dự án không đồng bộ hóa với phiếu giảm giá có liên quan về cách phân bổ kế toán của báo cáo chi tiêu khi chi phí được đăng lên Số dư. |
| **Quản lý dự án và kế toán** | [488382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488382) | Bộ lọc **Trạng thái hóa đơn** của các giao dịch dự án đã đăng đối với dự án theo giá cố định không hoạt động. |
| **Quản lý dự án và kế toán** | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | Tính năng loại bỏ ước tính ngược không hoạt động trong phần **Định kỳ**. |
| **Quản lý dự án và kế toán** | [509989](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509989) | Không thể xóa dòng đề xuất hóa đơn trong Project Operations khi được tích hợp với Dataverse. |
| **Quản lý dự án và kế toán** | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041) | Ngăn việc kích hoạt tính năng nhiều dòng hợp đồng khi không tích hợp Dataverse. |
| **Quản lý dự án và kế toán** | [510527](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510527) | Khi hóa đơn trả tạm bằng lợi nhuận và thua lỗ, thì doanh thu đã lập hóa đơn sẽ được liệt kê là 0 trên trang Ước tính. |
| **Quản lý dự án và kế toán** | [514167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514167) | Các chi tiết sửa lỗi trên hóa đơn không có tác dụng trong môi trường tích hợp. |
| **Quản lý dự án và kế toán** | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | Khi đăng WIP - giá trị bán hàng trong hóa đơn dự án liên công ty, hệ thống sẽ chọn một tài khoản sai. |
| **Quản lý dự án và kế toán** | [514385](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514385) | Trong Project Operations, không thể cập nhật các tác nhân phụ thuộc trên nhiệm vụ ước tính trong Dataverse. |
| **Quản lý dự án và kế toán** | [515258](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515258) | Việc xóa liên tục các hành trình tích hợp Project Operations trong phần Tài chính dẫn đến tình trạng mất dữ liệu. |
| **Quản lý dự án và kế toán** | [519716](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519716) | Lỗi sau đây xảy ra khi đăng bản đề xuất hóa đơn dự án "Giao dịch không cân bằng ở tiền tệ báo cáo khi thêm khoản khấu trừ trên hóa đơn tạm ứng". |
| **Quản lý dự án và kế toán** | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | ID dự án sai được thêm vào các khoản khấu trừ sau khi cập nhật hợp đồng dự án mặc định trong Project Operations. |
| **Quản lý dự án và kế toán** | [522799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522799) | Không thể hoàn tất ghi nhận ước tính và doanh thu khi bật Project Operations. |
| **Quản lý dự án và kế toán** | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | Trong Project Operations, thao tác xóa dự án khỏi hợp đồng không đặt lại dự án mặc định trên hợp đồng. |
| **Quản lý dự án và kế toán** | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | Trong Project Operations, trên hóa đơn liên công ty, dòng chi tiêu không chính xác hiển thị trong danh sách **Thêm dòng**. |
| **Đi lại và chi tiêu** | [515334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515334) | Không thể đăng dòng chi tiêu do thiếu thiết lập giờ trên dòng hợp đồng. |
| **Đi lại và chi tiêu** | [437673](https://fix.lcs.dynamics.com/Issue/Details/?bugId=437673) | Khi bắt buộc phải xác nhận dự án/hạng mục, các hạng mục chi tiêu liên kết với dự án không hiển thị trong báo cáo chi tiêu. |
| **Đi lại và chi tiêu** | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | Không cập nhật số dư tiền mặt tạm ứng khi báo cáo chi tiêu được đăng theo dòng. |
| **Đi lại và chi tiêu** | [465396](https://fix.lcs.dynamics.com/Issue/Details/?bugId=465396) | Tác vụ **Cập nhật thông tin thanh toán** thất bại sau khi đảo ngược các khoản trả góp trong đó hóa đơn được trả góp với hai giao dịch thanh toán trở lên. |
| **Đi lại và chi tiêu** | [472892](https://fix.lcs.dynamics.com/Issue/Details/?bugId=472892) | Xảy ra sự cố với việc tính toán khoản khấu trừ bữa ăn ngày cuối đối với hạng mục chi tiêu công tác phí. |
| **Đi lại và chi tiêu** | [477714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=477714) | Báo cáo **Loại chi tiêu mỗi nhân viên** không hiển thị chi phí theo mục nếu kết nối đầu tiên của người dùng là ở ngôn ngữ es-MX. |
| **Đi lại và chi tiêu** | [487516](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487516) | Khoản thanh toán của nhà cung cấp cho hóa đơn báo cáo chi tiêu sẽ dùng sai tài khoản tổng hợp để đăng khoản trả góp. |
| **Đi lại và chi tiêu** | [487531](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487531) | Nếu báo cáo chi tiêu được đăng khi bật tùy chọn **Cho phép nhóm giao dịch dựa trên tài khoản thanh toán bù trừ** và **Sửa ngày hạch toán lúc đăng**, ngày hạch toán sẽ không được nhóm trong bảng **Phân bổ kế toán**, làm ảnh hưởng đến bản ghi thuế bán hàng. |
| **Đi lại và chi tiêu** | [488292](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488292) | Ánh xạ hạng mục chi tiêu phụ bị xóa khi bỏ đánh dấu rồi chọn lại ô Dùng trong chi tiêu. |
| **Đi lại và chi tiêu** | [506175](https://fix.lcs.dynamics.com/Issue/Details/?bugId=506175) | Không thể tạo báo cáo chi tiêu liên công ty nếu ID dự án được thêm ở cấp tiêu đề. |
| **Đi lại và chi tiêu** | [509491](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509491) | Xảy ra sự cố thanh toán khoản chi tiêu khi số tiền chi tiêu lớn hơn số tiền mặt tạm ứng. |
| **Đi lại và chi tiêu** | [509556](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509556) | Trường **ID dự án** trên báo cáo chi tiêu liên công ty sẽ trống nếu như vai trò người dùng được gán cho một tổ chức cụ thể. |
| **Đi lại và chi tiêu** | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | Hạng mục chi tiêu bị khóa khi thêm dòng chi tiêu mới. |
| **Đi lại và chi tiêu** | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | Việc phân mục các dòng báo cáo chi tiêu có kết quả tách biệt sẵn sẽ khiến cho phiếu giảm giá Khoản phải trả/Sổ cái đã đăng không hoàn chỉnh. Do **TRVEXPTRANS.SOURCEDOCUMENTLINE** bị trùng lặp, Trình khám phá nguồn kế toán cũng không hoạt động. |
| **Đi lại và chi tiêu** | [521768](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521768) | Chỉ mục được thêm vào bảng **TRVREQUISITIONLINE** dành cho khách hàng có các trường hợp trùng lặp, dẫn đến lỗi khi nâng cấp. |
| **Đi lại và chi tiêu** | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | Trong Project Operations, không thể tạo hoặc phê duyệt thời gian với các nhiệm vụ liên công ty trong Dataverse. |

## <a name="regulatory-updates"></a>Bản cập nhật theo quy định

Để biết thông tin về các bản cập nhật theo quy định cho ứng dụng Finance and Operations, hãy xem [Bản cập nhật theo quy định](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates). Bạn cũng có thể đăng nhập vào LCS và xem các bản cập nhật theo quy định đã lên kế hoạch bằng cách sử dụng Công cụ tìm kiếm vấn đề. Tìm kiếm vấn đề cho phép bạn tìm kiếm theo quốc gia, loại tính năng và bản phát hành.


[!INCLUDE[footer-include](../includes/footer-banner.md)]