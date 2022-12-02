---
title: Nâng cấp từ Project Service Automation lên Project Operations
description: Bài viết này cung cấp thông tin tổng quan về quá trình nâng cấp từ Microsoft Dynamics 365 Project Service Automation lên Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/11/2022
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: ac2435c99f3aa9b2a6cdb08d7ce5f6628e7f6ac4
ms.sourcegitcommit: bea5f9b4066277344add1da3a1567ed56a0cfd31
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 11/02/2022
ms.locfileid: "9736693"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Nâng cấp từ Project Service Automation lên Project Operations

Chúng tôi rất vui được thông báo giai đoạn thứ hai trong ba giai đoạn nâng cấp từ Microsoft Dynamics 365 Project Service Automation lên Microsoft Dynamics 365 Project Operations. Bài viết này cung cấp thông tin tổng quan cho những khách hàng đang bước vào hành trình thú vị này. 

Chương trình thực hiện nâng cấp sẽ được chia thành ba giai đoạn.

| Thực hiện nâng cấp | Giai đoạn 1 (tháng 1 năm 2022) | Giai đoạn 2 (tháng 11 năm 2022) | Giai đoạn 3 (Đợt tháng 4 năm 2023)  |
|------------------|------------------------|---------------------------|---------------------------|
| Không có sự phụ thuộc vào cấu trúc phân tích công việc (WBS) cho các dự án | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Một WBS nằm trong những giới hạn được hỗ trợ hiện tại của Project Operations | | :heavy_check_mark: | :heavy_check_mark: |
| Một WBS nằm ngoài những giới hạn được hỗ trợ hiện tại của Project Operations, bao gồm hỗ trợ cho Project desktop client | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Các tính năng trong quy trình nâng cấp 

Là một phần của quá trình nâng cấp, chúng tôi đã thêm nhật ký nâng cấp vào sơ đồ trang web để cho phép quản trị viên chẩn đoán lỗi dễ dàng hơn. Bên cạnh giao diện mới, các quy tắc xác thực mới sẽ được thêm vào để bảo đảm tính toàn vẹn của dữ liệu sau khi nâng cấp. Các xác thực sau sẽ được thêm vào quá trình nâng cấp.

| Xác thực | Giai đoạn 1 (tháng 1 năm 2022) | Giai đoạn 2 (tháng 11 năm 2022) | Giai đoạn 3  |
|-------------|------------------------|---------------------------|---------------------------|
| WBS sẽ được xác thực dựa trên các hành vi vi phạm tính toàn vẹn dữ liệu phổ biến (ví dụ: phân công nguồn lực được liên kết với cùng một nhiệm vụ gốc nhưng có các dự án gốc khác nhau). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS sẽ được xác thực dựa trên [các giới hạn đã xác định của Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS sẽ được xác thực dựa trên các giới hạn đã xác định của Project desktop client. | |  | :heavy_check_mark: |
| Các nguồn lực có thể đặt trước và lịch dự án sẽ được đánh giá dựa trên các ngoại lệ quy tắc lịch không tương thích phổ biến. | | :heavy_check_mark: | :heavy_check_mark: |

Trong giai đoạn 2, những khách hàng nâng cấp lên Project Operations sẽ được nâng cấp các dự án hiện có của mình lên trải nghiệm lập kế hoạch dự án chỉ đọc. Trong trải nghiệm chỉ đọc này, WBS đầy đủ sẽ hiển thị trong lưới theo dõi. Để chỉnh sửa WBS, người quản lý dự án có thể chọn [**Chuyển đổi**](/PSA-Upgrade-Project-Conversion.md) trên trang chính của dự án. Sau đó, một quy trình nền sẽ cập nhật dự án để có thể hỗ trợ trải nghiệm lập lịch dự án mới từ Project for the Web. Giai đoạn này thích hợp cho những khách hàng có dự án nằm trong phạm vi [các giới hạn đã xác định của Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries).

Trong giai đoạn 3, hỗ trợ cho Project desktop client sẽ được bổ sung, vì lợi ích của những khách hàng muốn tiếp tục chỉnh sửa dự án của họ từ ứng dụng đó. Tuy nhiên, nếu các dự án hiện có được chuyển đổi thành trải nghiệm Project for the Web, quyền truy cập vào phần bổ trợ sẽ bị vô hiệu hóa cho mỗi dự án được chuyển đổi.

## <a name="prerequisites"></a>Điều kiện tiên quyết

Để đủ điều kiện cho nâng cấp Giai đoạn 1, bạn phải đáp ứng các tiêu chí sau:

- Môi trường đích không được chứa bất kỳ bản ghi nào trong thực thể **msdyn_projecttask**.
- Giấy phép Project Operations hợp lệ phải được chỉ định cho tất cả người dùng đang hoạt động. 
- Bạn phải xác thực quy trình nâng cấp trong ít nhất một môi trường phi sản xuất có chứa tập dữ liệu đại diện phù hợp với môi trường sản xuất của bạn.
- Môi trường đích phải được cập nhật lên Project Service Automation Bản phát hành cập nhật 37 (V3.10.58.120) trở lên.

Để đủ điều kiện cho nâng cấp Giai đoạn 2, bạn phải đáp ứng các tiêu chí sau:

- Giấy phép Project Operations hợp lệ phải được chỉ định cho tất cả người dùng đang hoạt động. 
- Bạn phải xác thực quy trình nâng cấp trong ít nhất một môi trường phi sản xuất có chứa tập dữ liệu đại diện phù hợp với môi trường sản xuất của bạn.
- Môi trường đích phải được cập nhật lên Project Service Automation Bản phát hành cập nhật 37 (V3.10.58.120) trở lên.
- Môi trường chứa nhiệm vụ (msdyn_projecttask) chỉ được hỗ trợ nếu tổng số nhiệm vụ trên mỗi dự án là 500 trở xuống.

Các điều kiện tiên quyết cho Giai đoạn 3 sẽ được cập nhật khi ngày phát hành rộng rãi đến gần.

## <a name="licensing"></a>Cấp phép

Nếu bạn có giấy phép cho Project Service Automation, bạn có thể cài đặt và sử dụng Project Operations, bao gồm tất cả các tính năng của Project Service Automation và các tính năng khác. Bằng cách này, bạn có thể kiểm tra các tính năng của Project Operations trong khi bạn tiếp tục sử dụng Project Service Automation trong sản xuất. Sau khi giấy phép Project Service Automation của bạn hết hạn, bạn sẽ phải chuyển sang Project Operations. Khi lập kế hoạch chuyển đổi này, bạn phải tính đến thực tế là giấy phép Project Operations không bao gồm giấy phép Project Service Automation. Những khách hàng có tình huống mà họ đã triển khai Project Service Automation và cần tiếp tục sử dụng hoặc tăng giấy phép cho PSA trong khi họ định chuyển sang Project Operations, có thể yêu cầu giấy phép PSA tạm thời dựa trên giấy phép Project Operations đã mua. Một giấy phép Project Service Automation sẽ được cấp cho một giấy phép Project Operations. Giấy phép PSA tạm thời có thể được yêu cầu bằng cách sử dụng liên kết này: aka.ms/ineedpsa

## <a name="testing-and-refactoring-customizations"></a>Kiểm tra và cấu trúc lại các mục tùy chỉnh

Mở đầu, hãy nhập tất cả các mục tùy chỉnh vào môi trường Project Operations (Lite) sạch để xác nhận rằng quá trình nhập thành công và các hoạt động kinh doanh hoạt động như mong đợi.

Dưới đây là một số điều cần chú ý:

- Quá trình nhập có thể không thành công do thiếu các mục phụ thuộc. Nói cách khác, các trường tham chiếu của mục tùy chỉnh hoặc các thành phần khác đã bị loại bỏ trong Project Operations. Trong trường hợp này, hãy loại bỏ những mục phụ thuộc này khỏi môi trường phát triển.
- Nếu các giải pháp không được quản lý và được quản lý của bạn bao gồm các thành phần không được tùy chỉnh, hãy loại bỏ các thành phần đó khỏi giải pháp. Ví dụ: khi bạn tùy chỉnh thực thể **Dự án**, chỉ thêm tiêu đề thực thể vào giải pháp của bạn. Không thêm tất cả các trường. Nếu trước đây bạn đã thêm tất cả các thành phần con, bạn có thể phải tạo một giải pháp mới theo cách thủ công và thêm các thành phần có liên quan vào đó.
- Các biểu mẫu và dạng xem có thể không như mong đợi. Trong một số trường hợp, nếu bạn đã tùy chỉnh bất kỳ biểu mẫu hoặc dạng xem sẵn dùng nào, các mục tùy chỉnh có thể ngăn không cho những cập nhật mới trong Project Operations có hiệu lực. Để xác định những vấn đề này, chúng tôi khuyên bạn nên thực hiện đánh giá song song việc cài đặt hoàn thiện Project Operations và cài đặt Project Operations bao gồm các mục tùy chỉnh của bạn. So sánh các biểu mẫu được sử dụng phổ biến nhất trong doanh nghiệp của bạn để xác nhận rằng phiên bản biểu mẫu của bạn vẫn có ý nghĩa và không thiếu gì từ phiên bản hoàn thiện của biểu mẫu. Thực hiện đánh giá song song tương tự cho bất kỳ dạng xem nào mà bạn đã tùy chỉnh.
- Logic kinh doanh có thể bị lỗi tại thời gian chạy. Vì các tham chiếu đến các trường trong phần bổ trợ của bạn không được xác thực tại thời điểm nhập, logic kinh doanh có thể không thành công do các tham chiếu đến các trường không còn tồn tại và bạn có thể nhận được thông báo lỗi tương tự như ví dụ sau: "Thực thể 'Dự án" không chứa thuộc tính Tên = 'msdyn_plannedhours' và NameMapping = 'Logical'. " Trong trường hợp này, hãy sửa đổi các mục tùy chỉnh của bạn sao cho chúng sử dụng các trường mới. Nếu bạn sử dụng các lớp proxy được tạo tự động và các tham chiếu kiểu mạnh trong logic phần bổ trợ của mình, hãy xem xét việc tạo lại các proxy đó từ một bản cài đặt hoàn thiện. Bằng cách này, bạn có thể dễ dàng xác định tất cả các vị trí mà phần bổ trợ của bạn phụ thuộc trên các trường không dùng nữa.

Sau khi bạn cập nhật các mục tùy chỉnh của mình để nhập Project Operations một cách gọn gàng, hãy chuyển sang các bước tiếp theo.

## <a name="end-to-end-testing-in-development-environments"></a>Thử nghiệm đầu cuối trong môi trường phát triển

### <a name="initiate-upgrade"></a>Bắt đầu nâng cấp 

1. Trong trung tâm quản trị Power Platform, tìm và chọn môi trường của bạn. Sau đó, trong ứng dụng, tìm và chọn **Dynamics 365 Project Operations**.
2. Chọn **Cài đặt** để bắt đầu nâng cấp. Trung tâm quản trị Power Platform sẽ hiển thị cài đặt này như một cài đặt mới. Tuy nhiên, sự hiện diện của phiên bản Project Service Automation trước đó sẽ được phát hiện và cài đặt hiện có sẽ được nâng cấp.

    Sau khi hoàn tất nâng cấp, môi trường sẽ hiển thị là Project Operations đã được cài đặt và Project Service Automation chưa được cài đặt.

    Tùy thuộc vào lượng dữ liệu trong môi trường, quá trình nâng cấp có thể mất vài giờ. Nhóm cốt lõi đang quản lý việc nâng cấp nên lập kế hoạch phù hợp và chạy nâng cấp trong những khung giờ ngoài giờ làm việc. Trong một số trường hợp, nếu khối lượng dữ liệu lớn, quy trình nâng cấp nên được chạy vào cuối tuần. Quyết định về việc lên lịch phải dựa trên kết quả thử nghiệm trong các môi trường thấp hơn.

3. Nâng cấp các giải pháp tùy chỉnh khi thích hợp. Tại thời điểm này, hãy triển khai bất kỳ thay đổi nào bạn đã thực hiện đối với các tùy chỉnh của mình trong phần [Thử nghiệm và cấu trúc lại các mục tùy chỉnh](#testing-and-refactoring-customizations) của bài viết này.
4. Đi đến **make.powerapps.com**, chọn môi trường của bạn từ menu thả xuống ở trên cùng bên phải của cổng thông tin, chọn **Giải pháp** từ menu bên trái, chọn giải pháp **Các thành phần không dùng nữa của Project Operations** và **Gỡ cài đặt**.

    Giải pháp này là giải pháp tạm thời nhằm giữ mô hình dữ liệu hiện có và các thành phần có trong quá trình nâng cấp. Bằng cách loại bỏ giải pháp này, bạn loại bỏ tất cả các trường và thành phần không còn được sử dụng. Bằng cách này, bạn sẽ giúp đơn giản hóa giao diện và giúp quá trình tích hợp và mở rộng diễn ra dễ dàng hơn.
    
### <a name="upgrade-to-project-operations-lite"></a>Nâng cấp lên Project Operations Lite

Các bước sau đây mô tả quá trình nâng cấp và ghi nhật ký lỗi liên quan:

1. **Kiểm tra Phiên bản PSA:** Để cài đặt Project Operations, bạn phải có V3.10.58.120 trở lên.
1. **Trước khi xác thực:** Khi quản trị viên bắt đầu nâng cấp, hệ thống sẽ chạy thao tác trước khi xác thực trên từng thực thể cốt lõi của giải pháp Project Operations. Bước này xác minh rằng tất cả các tham chiếu thực thể là hợp lệ và nó đảm bảo rằng dữ liệu có liên quan đến WBS nằm trong giới hạn được công bố của Project for the Web.
1. **Nâng cấp siêu dữ liệu:** Sau khi bước trước khi xác thực thành công, hệ thống bắt đầu các thay đổi đối với sơ đồ và tạo một giải pháp thành phần không dùng nữa. Bạn có thể loại bỏ giải pháp không dùng nữa này sau khi đã hoàn thành tất cả các bước tái cấu trúc mục tùy chỉnh. Bước này là phần dài nhất của quá trình nâng cấp và có thể mất đến bốn giờ để hoàn thành.
1. **Nâng cấp dữ liệu:** Sau khi tất cả các thay đổi sơ đồ bắt buộc đã được hoàn tất trong bước nâng cấp siêu dữ liệu, dữ liệu của bạn sẽ được di chuyển sang sơ đồ mới và mọi thao tác mặc định và tính toán lại được hoàn tất.
1. **Cập nhật công cụ lịch trình dự án:** Sau khi nâng cấp dữ liệu thành công, tab **Lịch trình** trên trang chính được gắn nhãn **Nhiệm vụ**. Khi người dùng chọn tab này sau khi nâng cấp, họ được chuyển hướng đến lưới theo dõi để xem phiên bản chỉ đọc của WBS. Để chỉnh sửa WBS, họ phải bắt đầu [quá trình chuyển đổi](/PSA-Upgrade-Project-Conversion.md) theo lịch. Tất cả các dự án không có WBS có sẵn đều có thể sử dụng trực tiếp trải nghiệm lập lịch mới mà không cần chuyển đổi.
 
### <a name="validate-common-scenarios"></a>Xác thực các trường hợp phổ biến

Khi bạn xác thực các mục tùy chỉnh cụ thể của mình, chúng tôi khuyên bạn cũng nên xem xét các quy trình kinh doanh được hỗ trợ trên các ứng dụng. Các quy trình kinh doanh này bao gồm, nhưng không giới hạn, việc tạo ra các thực thể bán hàng như báo giá và hợp đồng cũng như quá trình tạo các dự án bao gồm WBS và phê duyệt số liệu thực tế.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Các thay đổi lớn giữa Project Service Automation và Project Operations

Phần này cung cấp một bản tóm tắt về những thay đổi lớn mà bạn có thể mong đợi giữa Project Service Automation và Project Operations.

### <a name="project-planning"></a>Lập kế hoạch dự án

Tính năng lập kế hoạch dự án trong Project Operations không còn phụ thuộc vào logic phía máy khách kết hợp và logic phía máy chủ. Thay vào đó, Project Operations sử dụng Project for the Web làm công cụ lập lịch của nó. Sự thay đổi này trong tính năng lập lịch cho phép một số tính năng mới, chẳng hạn như dạng xem Board và Gantt, lập kế hoạch dựa trên nguồn lực, [các mục trong danh sách kiểm tra nhiệm vụ](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) và các chế độ lập lịch dự án. Các tính năng lập lịch mới cũng được hỗ trợ bởi một loạt các [giao diện lập trình ứng dụng (API)](../project-management/schedule-api-preview.md). Các API này nhằm giúp đảm bảo rằng không có hoạt động lập trình nào nhằm tạo, cập nhật hoặc xóa một thực thể trong WBS sẽ làm hỏng các trường được tính toán trong lịch trình.

### <a name="billing-and-pricing"></a>Định giá và thanh toán

Là một phần của việc đầu tư liên tục vào Project Operations, một số tính năng mới sẽ khả dụng trong Lập hóa đơn và giá. Dưới đây là một số ví dụ:

- [Ghi lại hoạt động sử dụng vật tư của dự án và nhiệm vụ dự án](../material/material-usage-log.md)
- [Quản lý hợp đồng phụ](../pro/subcontracting/managing-subcontracts-overview.md)
- [Hợp đồng dựa trên tiền tạm ứng và giữ lại](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Trạng thái không được vượt quá của hợp đồng và các mục xác thực](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Lập hóa đơn dựa trên nhiệm vụ

### <a name="resource-management"></a>Quản lý nguồn lực

Project Operations cung cấp hỗ trợ tùy chọn cho trợ lý bảng lịch trình và lập lịch Universal Resource Scheduling (URS). Trải nghiệm mới này sẽ trở thành bắt buộc trong đợt tháng 4 năm 2023.

## <a name="frequently-asked-questions"></a>Các câu hỏi thường gặp

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Những loại triển khai nào hiện được hỗ trợ cho nâng cấp?

| Nguồn                                                 | Mục tiêu                                                    | Trạng thái                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | Triển khai Project Operations Lite                        | Hỗ trợ               |
| Quản lý dự án và kế toán Dynamics 365 Finance | Triển khai Project Operations Lite                        | Hiện không được hỗ trợ |
| Quản lý dự án và kế toán Finance              | Project Operations dành cho tình huống dựa trên nguồn lực/hàng không trữ kho     | Hiện không được hỗ trợ |
| Project Service Automation 3.x                         | Project Operations dành cho tình huống dựa trên nguồn lực/hàng không trữ kho     | Hiện không được hỗ trợ |
| Project for the Web (môi trường dành riêng)            | Triển khai Project Operations Lite                        | Hiện không được hỗ trợ |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Làm cách nào để cài đặt Project Operations trước khi công cụ nâng cấp khả dụng?

Có hai tùy chọn để cài đặt Project Operations trước khi công cụ nâng cấp khả dụng:

- Cung cấp môi trường mới.
- Triển khai Project Operations một cách riêng biệt trên bất kỳ tổ chức bán hàng nào không có Project Service Automation.

Nếu Project Service Automation được cài đặt trên một tổ chức nhưng không được sử dụng thì nó có thể đ=bị gỡ cài đặt. Sau khi bạn loại bỏ hoàn toàn Project Service Automation, Project Operations có thể được cài đặt trên cùng tổ chức.
