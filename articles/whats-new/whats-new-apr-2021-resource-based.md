---
title: Tính năng mới kể từ tháng 4 năm 2021 – Project Operations cho các kịch bản dựa trên nguồn lực/vật tư không tồn kho
description: Chủ đề này cung cấp thông tin về các bản cập nhật chất lượng có trong lần triển khai bản đơn giản của Project Operations phát hành vào tháng 4 năm 2021 cho các kịch bản dựa trên nguồn lực/vật tư không tồn kho.
author: sigitac
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: dbce86e88f8315ac4a4957c1128b5619d5328bdbbe27793e161f8f2691899481
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/06/2021
ms.locfileid: "7008162"
---
# <a name="whats-new-april-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Tính năng mới kể từ tháng 4 năm 2021 – Project Operations cho các kịch bản dựa trên nguồn lực/vật tư không tồn kho

_**Áp dụng cho:** Project Operations cho kịch bản dựa trên nguồn lực/hàng không nhập kho_

Chủ đề này áp dụng cho các phiên bản và thành phần sau của Dynamics 365 Project Operations:

- Project Operations trên môi trường Dataverse phiên bản 4.9.0.221
- Quản lý dự án và kế toán trong các môi trường Dynamics 365 Finance phiên bản 10.0.17

## <a name="features-included-in-this-release"></a>Các tính năng có trong bản phát hành này

Sau đây là các tính năng có trong bản phát hành này:

- Vật tư không tồn kho cho các dự án. Các tính năng chính bao gồm:
  - Ước tính và định giá vật tư không tồn kho trong chu kỳ bán hàng của một dự án. Để biết thêm thông tin, hãy xem phần [Thiết lập chi phí và tỷ lệ doanh số cho các sản phẩm trong danh mục - bản đơn giản](../pro/pricing-costing/set-up-cost-sales-rates-catalog-products.md).
  - Theo dõi việc sử dụng vật tư không tồn kho trong quá trình thực hiện dự án. Để biết thêm thông tin, hãy xem phần [Ghi mức sử dụng vật tư của dự án và nhiệm vụ dự án](../material/material-usage-log.md).
  - Lập hóa đơn chi phí vật tư không tồn kho đã qua sử dụng. Để biết thêm thông tin, hãy xem [Quản lý mục tồn đọng lập hóa đơn](../proforma-invoicing/manage-billing-backlog.md).
  - Để biết thông tin về cách đặt cấu hình tính năng này, hãy xem [Đặt cấu hình vật tư không tồn kho và hóa đơn của nhà cung cấp đang chờ xử lý](../procurement/configure-materials-nonstocked.md)
- Thanh toán theo nhiệm vụ: Đã thêm khả năng kết hợp các nhiệm vụ dự án với các mục mô tả hợp đồng dự án, nhờ đó có thể áp dụng cùng một phương thức thanh toán, tần suất hóa đơn và khách hàng cho các nhiệm vụ đó nhưng như những nhiệm vụ trên mục mô tả hợp đồng. Sự liên kết này đảm bảo việc lập hóa đơn, kế toán, ước tính doanh thu và ghi nhận chính xác hoạt động theo cách thiết lập này cho các nhiệm vụ dự án.
- API mới trong Dynamics 365 Dataverse cho phép thực hiện các thao tác tạo, cập nhật và xóa với **Thực thể lập lịch trình**. Để biết thêm thông tin, hãy xem [Sử dụng API lịch trình để thực hiện thao tác với các thực thể Lập lịch trình](../project-management/schedule-api-preview.md).

## <a name="project-operations-dual-write-maps-updates"></a>Cập nhật về bản đồ ghi kép của Project Operations

Danh sách sau đây hiển thị các bản đồ ghi kép đã được sửa đổi hoặc bổ sung trong bản phát hành Project Operations vào tháng 4 năm 2021.

| **Bản đồ thực thể** | **Phiên bản đã cập nhật** | **Nhận xét** |
| --- | --- | --- |
| Giá trị tích hợp thực tế của Project Operations (msdyn\_actuals) | 1.0.0.14 | Bản đồ được sửa đổi để đồng bộ hóa các giá trị thực tế của dự án vật tư. |
| Thực thể tích hợp Project Operations để ước tính chi phí (msdyn\_estimateslines) | 1.0.0.2 | Mô tả hợp đồng dự án được thêm đã đồng bộ hóa với ứng dụng Finance and Operations để hỗ trợ thanh toán dựa trên nhiệm vụ. |
| Thực thể tích hợp Project Operations để ước tính giờ (msdyn\_resourceassignments) | 1.0.0.5 | Mô tả hợp đồng dự án được thêm đã đồng bộ hóa với ứng dụng Finance and Operations để hỗ trợ thanh toán dựa trên nhiệm vụ. |
| Bảng tích hợp Project Operations để ước tính vật tư (msdyn\_estimatelines) | 1.0.0.0 | Bản đồ bảng mới để đồng bộ hóa các ước tính vật tư từ Dataverse đến ứng dụng Finance and Operations. |
| Thực thể xuất hóa đơn nhà cung cấp của Project Operations (msdyn\_projectvendorinvoices) | 1.0.0.0 | Bản đồ bảng mới để đồng bộ hóa tiêu đề hóa đơn của nhà cung cấp từ ứng dụng Finance and Operations đến Dataverse. |
| Thực thể xuất mô tả hóa đơn nhà cung cấp của Project Operations (msdyn\_projectvendorinvoicelines) | 1.0.0.0 | Bản đồ bảng mới để đồng bộ hóa mô tả hóa đơn của nhà cung cấp từ ứng dụng Finance and Operations đến Dataverse. |

Bạn phải luôn chạy phiên bản bản đồ mới nhất trong môi trường của mình và bật tất cả các bản đồ bảng liên quan khi cập nhật giải pháp Project Operations Dataverse và phiên bản giải pháp Finance and Operations. Một số tính năng và chức năng nhất định có thể không hoạt động chính xác nếu phiên bản mới nhất của bản đồ không được kích hoạt. Bạn có thể xem phiên bản hiện hoạt của bản đồ trong cột **Phiên bản** trên trang **Ghi kép**. Bạn có thể kích hoạt phiên bản mới của bản đồ bằng cách chọn **Phiên bản bản đồ bảng**, chọn phiên bản mới nhất rồi lưu phiên bản đã chọn. Nếu đã tùy chỉnh sơ đồ bảng có sẵn, hãy áp dụng lại các thay đổi. Để biết thêm thông tin, hãy xem [Quản lý vòng đời áp dụng](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Nếu bạn gặp sự cố khi khởi động bản đồ, hãy làm theo hướng dẫn trong phần [Vấn đề thiếu cột trong bảng trên bản đồ](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) của hướng dẫn khắc phục sự cố Ghi kép.

## <a name="quality-updates"></a>Bản cập nhật chất lượng

### <a name="project-operations-in-dynamics-365-dataverse"></a>Project Operations trong Dynamics 365 Dataverse

| **Lĩnh vực tính năng** | **Số tham chiếu** | **Cập nhật chất lượng** |
| --- | --- | --- |
| Định giá và thanh toán | 2124532 | Nút **Sửa hóa đơn** hiển thị trên hóa đơn ước giá khi số tiền đặt cọc hoặc số tiền đặt cọc đã áp dụng có trên hóa đơn gốc. Nút này chỉ hiển thị cho các môi trường có phiên bản Finance 10.0.19 trở lên. |
| Định giá và thanh toán | 2224568 | Đã thêm logic để bật các chế độ tùy chỉnh liên quan đến việc gọi ra phần bổ trợ xác nhận hóa đơn. |
| Định giá và thanh toán | 2101098 | Đã cải thiện logic của các trường mặc định cho hóa đơn ước giá: **Địa chỉ nhận hóa đơn**, **Tên nhận hóa đơn** và **Điều khoản thanh toán** bây giờ là các trường mặc định từ hồ sơ khách hàng của hợp đồng dự án tương ứng. |
| Định giá và thanh toán | 2021413 | Đã cập nhật các trường **Chi phí thực tế** và **Bán hàng** trên thực thể **Nhiệm vụ** để đưa vào các giá trị doanh số từ các chi phí chưa lập hóa đơn và đã lập hóa đơn cho các nhiệm vụ. |
| Định giá và thanh toán | 2182110 | Khi sao chép hợp đồng dự án, ID mô tả hợp đồng sẽ được tái tạo trong hợp đồng dự án đích để đảm bảo ID này là duy nhất. |
| Quản lý cơ hội | 2186741 | Đã thêm các bước xác thực để đảm bảo không thể cập nhật trường **Gốc** và **Loại giao dịch** trên phần chi tiết mô tả báo giá hiện có. |
| Quản lý cơ hội | 2191353 | Không được tạo các mốc trên một mục mô tả hợp đồng thời gian và vật tư. |
| Quản lý cơ hội | 2216956 | Đã khắc phục sự cố **Cập nhật giá**. |
| Hoạch định và theo dõi dự án | 2182979 | Đã cải tiến chức năng sao chép dự án để đảm bảo các dòng ước tính chi phí được sao chép từ dự án gốc. |
| Hoạch định và theo dõi dự án | 2184144 | Đã cải tiến chức năng sao chép dự án để đảm bảo tên vị trí nguồn lực được sao chép từ dự án gốc. |
| Hoạch định và theo dõi dự án | 2184799 | Sao chép dự án: Kiểm soát chặt chẽ để đảm bảo không thể thay đổi ngày bắt đầu ước tính khi đang sao chép. |
| Hoạch định và theo dõi dự án | 2185134 | Sao chép dự án: Ngày bắt đầu dự kiến của dự án đích được đặt thành ngày hôm nay. |
| Hoạch định và theo dõi dự án | 2196373 | Sao chép dự án: Đảm bảo hồ sơ của người quản lý dự án và thành viên trong nhóm không bị trùng lặp trong nhóm dự án. |
| Hoạch định và theo dõi dự án | 2211833 | Sao chép dự án: Các công việc giao cho nguồn lực được sao chép từ nhiệm vụ của dự án nguồn sang dự án đích. |
| Hoạch định và theo dõi dự án | 2186541 | Đã khắc phục sự cố trong lưới **Ước tính** khi nhóm theo nguồn lực. |
| Hoạch định và theo dõi dự án | 2166906 | Phải sao chép thể loại giao dịch từ một nhiệm vụ vào thực thể **Công việc giao cho nguồn lực**. |
| Quản lý nguồn lực | 2125362 | Đã khắc phục sự cố khi tạo một thành viên nhóm chung bằng phương pháp phân bổ theo giờ. |
| Thời gian và Chi phí | 2113603 | Đã khắc phục sự cố liên quan đến tùy chỉnh bằng cách xóa các thuộc tính khỏi trang **Mục nhập thời gian**. Giờ đây, hệ thống sẽ kiểm tra xem thuộc tính có tồn tại trên trang hay không trước khi truy cập chúng bằng cách sử dụng tập lệnh. |
| Thời gian và Chi phí | 2204377 | Bảng chấm công đã sao chép phải tự động hiển thị khi bạn chọn **Sao chép tuần** trong mục nhập thời gian. |
| Thời gian và Chi phí | 2209059 | Bạn có thể chỉnh sửa trường **Trạng thái** cho các mục nhập thời gian trên Dynamics 365 Field Service. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Quản lý dự án và kế toán trong Dynamics 365 Finance

| **Lĩnh vực tính năng** | **Số tham chiếu** | **Cập nhật chất lượng** |
| --- | --- | --- |
| Quản lý dự án và kế toán | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | Tính năng loại bỏ ước tính ngược không hoạt động trong phần **Định kỳ**.  |
| Quản lý dự án và kế toán | [509773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509773) | Tính năng **Điều chỉnh kế toán** gây ra sự cố với các tài khoản sổ cái đã chọn **Không cho phép nhập thủ công**. |
| Quản lý dự án và kế toán | [510728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=5109728) | Đã thêm logic nghiệp vụ để xử lý hóa đơn điều chỉnh bao gồm số tiền đặt cọc hoặc số tiền đặt cọc đã áp dụng. |
| Quản lý dự án và kế toán | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | WIP - giá trị bán hàng đăng trong hóa đơn dự án liên công ty chọn một tài khoản không mong muốn. |
| Quản lý dự án và kế toán | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | Khi làm việc với các khoản đặt cọc trong Project Operations, việc thay đổi dự án mặc định trên một hợp đồng sau khi các khoản trả trước được lập hóa đơn gây ra sự cố với các khoản khấu trừ trong tương lai. |
| Quản lý dự án và kế toán | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | Trong Project Operations, việc xóa một dự án khỏi hợp đồng sẽ đặt lại dự án mặc định của hợp đồng, nếu cần. |
| Quản lý dự án và kế toán | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | Trong Project Operations, các dòng chi phí không chính xác hiển thị trong danh sách **Thêm dòng** trên hóa đơn giữa các công ty. |
| Quản lý dự án và kế toán | [543968](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543968) | Trong Project Operations, trang **Thỏa thuận mua** không hiển thị trong các pháp nhân Tài chính được tích hợp với Project Operations. |
| Quản lý dự án và kế toán | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | Do có lỗi tích hợp Dataverse, bạn không thể chuyển đổi báo giá thành đã lấy được trong Project Operations. |
| Quản lý dự án và kế toán | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** có thể đặt địa chỉ hóa đơn nguồn tiền từ một khách hàng khác.  |
| Quản lý dự án và kế toán | [557376](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557376) | Trong Project Operations, không có thứ nguyên nào được chọn khi bạn tạo hóa đơn đăng cho một giao dịch. |
| Đi lại và chi phí | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | Số dư tạm ứng tiền mặt sẽ không được cập nhật cho báo cáo chi phí nếu nó được phê duyệt và đăng từng dòng. |
| Đi lại và chi tiêu | [482041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482041) | Thuế trên các báo cáo chi phí giữa các công ty đã ghi thành từng khoản không được tính toán chính xác. |
| Đi lại và chi tiêu | [483469](https://fix.lcs.dynamics.com/Issue/Details/?bugId=483469) | Các trường khác có liên quan đến dự án hiển thị trên trang **Báo cáo chi phí giữa các công ty** đã tái tạo. |
| Đi lại và chi tiêu | [486592](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486592) | Một thông báo lỗi không chính xác xuất hiện trên biên lai tiêu đề của các báo cáo chi phí. |
| Đi lại và chi tiêu | [487971](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487971) | Báo cáo chi phí sẽ được đăng không chính xác trong một kịch bản giữa các công ty nếu thuế bán hàng được gửi đến pháp nhân đích. |
| Đi lại và chi tiêu | [505696](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505696) | Ngày gửi báo cáo không được in trên báo cáo chi phí đã phê duyệt. |
| Đi lại và chi tiêu | [508726](https://fix.lcs.dynamics.com/Issue/Details/?bugId=508726) | Trường **Ngày được phê duyệt** và **Ngày bị từ chối** không được điền sau khi phê duyêt một khoản chi phí. |
| Đi lại và chi tiêu | [509913](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509913) | Bạn có thể sử dụng yêu cầu đi lại được tạo cho một nhân viên cho báo cáo chi phí của một nhân viên khác. |
| Đi lại và chi tiêu | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | Danh mục chi phí bị khóa khi thêm dòng chi phí mới. |
| Đi lại và chi tiêu | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | Việc ghi các dòng báo cáo chi phí đã phân chia thành từng khoản sẽ làm gián đoạn quá trình đăng phiếu Sổ cái chung\Khoản phải trả và Trình khám phá nguồn kế toán do **TRVEXPTRANS.SOURCEDOCUMENTLINE** bị trùng lặp. |
| Đi lại và chi tiêu | [521943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521943) | Chính sách yêu cầu đi lại không hoạt động như mong đợi. |
| Đi lại và chi tiêu | [522567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522567) | Tên tài khoản nhà cung cấp không hiển thị trên các giao dịch dự án đã đăng cho các báo cáo chi phí. |
| Đi lại và chi tiêu | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | Trong Project Operations, bạn không thể phê duyệt thời gian với một nhiệm vụ của một dự án giữa các công ty. |
| Đi lại và chi tiêu | [526336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526336) | Thể loại hoàn trả khoản ứng trước tiền mặt hiện không cập nhật số dư khoản ứng trước tiền mặt khi được đăng. |
| Đi lại và chi tiêu | [527218](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527218) | Giá bán được tính không chính xác trên các báo cáo chi phí được tạo bằng ngoại tệ (bằng cách sử dụng các giao dịch thẻ tín dụng đã nhập) và liên kết với một dự án. |
| Đi lại và chi tiêu | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | Đã khôi phục thực thể dữ liệu **TrvRequisitionLine** và chỉ mục duy nhất được liên kết. |
| Đi lại và chi tiêu | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | Đã thêm thiết bị vào quá trình tạo **SOURCEDOCUMENTLINE**. |
| Đi lại và chi tiêu | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | Nhật ký sổ cái không chính xác sẽ hiển thị trong kịch bản giữa các công ty nếu thuế bán hàng được gửi đến pháp nhân đích. |
| Đi lại và chi tiêu | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | Trong Project Operations, các ước tính chi phí không bị xóa khỏi mục Tài chính khi bị xóa khỏi Dataverse. |
| Đi lại và chi tiêu | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | Khi một thể loại chi phí là một thể loại phi dự án, các thứ nguyên tài chính được chọn trên trang **Chi phí** sẽ không được sao chép vào báo cáo chi phí. |
