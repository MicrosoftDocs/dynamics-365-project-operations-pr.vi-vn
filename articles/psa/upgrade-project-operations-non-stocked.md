---
title: Nâng cấp từ Project Service Automation lên Project Operations
description: Bài viết này cung cấp tổng quan về quá trình nâng cấp từ Microsoft Dynamics 365 Project Service Automation đến Dynamics 365 Project Operations.
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
ms.openlocfilehash: 2d7b372cac391fab7a81ac6ac5d2ea6d12977b5c
ms.sourcegitcommit: 9de444ae0460c8d15c77d225d0c0ad7f8445d5fc
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 10/18/2022
ms.locfileid: "9687002"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Nâng cấp từ Project Service Automation lên Project Operations

Chúng tôi vui mừng thông báo giai đoạn thứ hai trong ba giai đoạn nâng cấp từ Microsoft Dynamics 365 Project Service Automation cho Microsoft Dynamics 365 Project Operations. Bài viết này cung cấp một cái nhìn tổng quan cho những khách hàng đang dấn thân vào hành trình thú vị này. 

Chương trình nâng cấp sẽ được chia thành ba giai đoạn.

| Nâng cấp giao hàng | Giai đoạn 1 (tháng 1 năm 2022) | Giai đoạn 2 (tháng 11 năm 2022) | Giai đoạn 3 (Làn sóng tháng 4 năm 2023)  |
|------------------|------------------------|---------------------------|---------------------------|
| Không phụ thuộc vào cấu trúc phân chia công việc (WBS) cho các dự án | : heavy_check_mark: | : heavy_check_mark: | : heavy_check_mark: |
| Một WBS trong giới hạn được hỗ trợ hiện tại của Hoạt động dự án | | : heavy_check_mark: | : heavy_check_mark: |
| Một WBS nằm ngoài giới hạn được hỗ trợ hiện tại của Hoạt động dự án, bao gồm hỗ trợ cho máy khách Project trên máy tính | | | : heavy_check_mark: |

## <a name="upgrade-process-features"></a>Nâng cấp các tính năng của quy trình 

Là một phần của quá trình nâng cấp, chúng tôi đã thêm nhật ký nâng cấp vào sơ đồ trang web để cho phép quản trị viên chẩn đoán lỗi dễ dàng hơn. Ngoài giao diện mới, các quy tắc xác thực mới sẽ được thêm vào để đảm bảo tính toàn vẹn của dữ liệu sau khi nâng cấp. Các xác nhận sau sẽ được thêm vào quá trình nâng cấp.

| Xác thực | Giai đoạn 1 (tháng 1 năm 2022) | Giai đoạn 2 (tháng 11 năm 2022) | Giai đoạn 3  |
|-------------|------------------------|---------------------------|---------------------------|
| WBS sẽ được xác thực để chống lại các vi phạm toàn vẹn dữ liệu phổ biến (ví dụ: gán tài nguyên được liên kết với cùng một nhiệm vụ mẹ nhưng có các dự án mẹ khác nhau). | | : heavy_check_mark: | : heavy_check_mark: |
| WBS sẽ được xác nhận dựa trên [giới hạn đã biết của Dự án cho Web](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | : heavy_check_mark: | : heavy_check_mark: |
| WBS sẽ được xác nhận theo các giới hạn đã biết của máy khách Project desktop. | |  | : heavy_check_mark: |
| Các tài nguyên có thể đặt trước và lịch dự án sẽ được đánh giá dựa trên các ngoại lệ quy tắc lịch không tương thích phổ biến. | | : heavy_check_mark: | : heavy_check_mark: |

Trong giai đoạn 2, những khách hàng nâng cấp lên Hoạt động dự án sẽ được nâng cấp các dự án hiện có của họ lên trải nghiệm chỉ đọc để lập kế hoạch dự án. Trong trải nghiệm chỉ đọc này, WBS đầy đủ sẽ hiển thị trong lưới theo dõi. Để chỉnh sửa WBS, người quản lý dự án có thể chọn [**Chuyển thành**](/PSA-Upgrade-Project-Conversion.md) trên trang chính của dự án. Sau đó, một quy trình nền sẽ cập nhật dự án để nó hỗ trợ trải nghiệm lập lịch dự án mới từ Project cho Web. Giai đoạn này thích hợp cho những khách hàng có dự án phù hợp với [các giới hạn đã biết của Dự án cho Web](/project-for-the-web/project-for-the-web-limits-and-boundaries).

Trong giai đoạn 3, hỗ trợ cho máy khách Project desktop sẽ được bổ sung, vì lợi ích của những khách hàng muốn tiếp tục chỉnh sửa dự án của họ từ ứng dụng đó. Tuy nhiên, nếu các dự án hiện có được chuyển đổi thành Dự án mới cho trải nghiệm Web, quyền truy cập vào phần bổ trợ sẽ bị vô hiệu hóa cho mỗi dự án được chuyển đổi.

## <a name="prerequisites"></a>Điều kiện tiên quyết

Để đủ điều kiện nâng cấp Giai đoạn 1, bạn phải đáp ứng các tiêu chí sau:

- Môi trường đích không được chứa bất kỳ bản ghi nào trong **msdyn_projecttask** thực thể.
- Giấy phép Hoạt động Dự án hợp lệ phải được chỉ định cho tất cả người dùng đang hoạt động. 
- Bạn phải xác thực quy trình nâng cấp trong ít nhất một môi trường phi sản xuất có chứa tập dữ liệu đại diện phù hợp với môi trường sản xuất của bạn.
- Môi trường đích phải được cập nhật lên Bản phát hành bản cập nhật tự động hóa dịch vụ dự án 37 (V3.10.58.120) trở lên.

Để đủ điều kiện nâng cấp Giai đoạn 2, bạn phải đáp ứng các tiêu chí sau:

- Giấy phép Hoạt động Dự án hợp lệ phải được chỉ định cho tất cả người dùng đang hoạt động. 
- Bạn phải xác thực quy trình nâng cấp trong ít nhất một môi trường phi sản xuất có chứa tập dữ liệu đại diện phù hợp với môi trường sản xuất của bạn.
- Môi trường đích phải được cập nhật lên Bản phát hành bản cập nhật tự động hóa dịch vụ dự án 37 (V3.10.58.120) trở lên.
- Môi trường chứa nhiệm vụ (msdyn_projecttask) chỉ được hỗ trợ nếu tổng số nhiệm vụ trên mỗi dự án là 500 hoặc ít hơn.

Các điều kiện tiên quyết cho Giai đoạn 3 sẽ được cập nhật khi ngày khả dụng chung sắp đến.

## <a name="licensing"></a>Cấp phép

Nếu bạn có giấy phép hoạt động cho Tự động hóa dịch vụ dự án, bạn có thể cài đặt và sử dụng Hoạt động dự án, bao gồm tất cả các khả năng của Tự động hóa dịch vụ dự án và hơn thế nữa. Sau đó, bạn có thể kiểm tra khả năng của Hoạt động dự án trong một môi trường riêng biệt trong khi bạn tiếp tục sử dụng Tự động hóa dịch vụ dự án trong sản xuất. Sau khi giấy phép Tự động hóa Dịch vụ Dự án của bạn hết hạn, bạn sẽ phải chuyển sang Hoạt động Dự án. Khi lập kế hoạch chuyển đổi này, bạn phải tính đến thực tế là giấy phép Hoạt động Dự án không bao gồm giấy phép Tự động hóa Dịch vụ Dự án.

## <a name="testing-and-refactoring-customizations"></a>Kiểm tra và cấu trúc lại các tùy chỉnh

Như một điểm khởi đầu, hãy nhập tất cả các tùy chỉnh vào môi trường Hoạt động Dự án (Lite) sạch để xác nhận rằng quá trình nhập thành công và các hoạt động kinh doanh hoạt động như mong đợi.

Dưới đây là một số điều cần chú ý:

- Nhập có thể không thành công vì thiếu phụ thuộc. Nói cách khác, các trường tham chiếu tùy chỉnh hoặc các thành phần khác đã bị loại bỏ trong Hoạt động dự án. Trong trường hợp này, hãy loại bỏ những phụ thuộc này khỏi môi trường phát triển.
- Nếu các giải pháp không được quản lý và quản lý của bạn bao gồm các thành phần không được tùy chỉnh, hãy xóa các thành phần đó khỏi giải pháp. Ví dụ: khi bạn tùy chỉnh **Dự án** thực thể, chỉ thêm tiêu đề thực thể vào giải pháp của bạn. Đừng thêm tất cả các trường. Nếu trước đây bạn đã thêm tất cả các thành phần con, bạn có thể phải tạo một giải pháp mới theo cách thủ công và thêm các thành phần có liên quan vào nó.
- Biểu mẫu và chế độ xem có thể không xuất hiện như mong đợi. Trong một số trường hợp, nếu bạn đã tùy chỉnh bất kỳ biểu mẫu hoặc chế độ xem có sẵn nào, các tùy chỉnh có thể ngăn các cập nhật mới trong Hoạt động dự án có hiệu lực. Để xác định những vấn đề này, chúng tôi khuyên bạn nên thực hiện đánh giá song song việc cài đặt hoàn thiện Hoạt động dự án và cài đặt Hoạt động dự án bao gồm các tùy chỉnh của bạn. So sánh các biểu mẫu được sử dụng phổ biến nhất trong doanh nghiệp của bạn để xác nhận rằng phiên bản biểu mẫu của bạn vẫn có ý nghĩa và không thiếu điều gì đó từ phiên bản sạch của biểu mẫu. Thực hiện cùng một loại đánh giá song song cho bất kỳ chế độ xem nào mà bạn đã tùy chỉnh.
- Logic nghiệp vụ có thể không thành công trong thời gian chạy. Vì các tham chiếu đến các trường trong trình cắm của bạn không được xác thực tại thời điểm nhập, logic nghiệp vụ có thể không thành công do các tham chiếu đến các trường không còn tồn tại và bạn có thể nhận được thông báo lỗi tương tự như ví dụ sau: "'Dự án' thực thể không chứa thuộc tính Name = 'msdyn_plannedhours' và NameMapping = 'Logical'. " Trong trường hợp này, hãy sửa đổi các tùy chỉnh của bạn để chúng sử dụng các trường mới. Nếu bạn sử dụng các lớp proxy được tạo tự động và các tham chiếu kiểu mạnh trong logic trình cắm của mình, hãy xem xét việc tạo lại các proxy đó từ một bản cài đặt sạch. Bằng cách này, bạn có thể dễ dàng xác định tất cả các vị trí mà trình cắm của bạn phụ thuộc vào các trường không dùng nữa.

Sau khi bạn cập nhật các tùy chỉnh của mình để nhập Hoạt động dự án một cách rõ ràng, hãy chuyển sang các bước tiếp theo.

## <a name="end-to-end-testing-in-development-environments"></a>Kiểm tra đầu cuối trong môi trường phát triển

### <a name="initiate-upgrade"></a>Bắt đầu nâng cấp 

1. Bên trong Power Platform trung tâm quản trị, tìm và chọn môi trường của bạn. Sau đó, trong các ứng dụng, hãy tìm và chọn **Dynamics 365 Project Operations**.
2. Lựa chọn **Cài đặt** để bắt đầu nâng cấp. Các Power Platform trung tâm quản trị sẽ trình bày cài đặt này như một cài đặt mới. Tuy nhiên, sự hiện diện của phiên bản Project Service Automation trước đó sẽ được phát hiện và cài đặt hiện có sẽ được nâng cấp.

    Sau khi hoàn tất nâng cấp, môi trường sẽ hiển thị rằng Hoạt động dự án đã được cài đặt và Tự động hóa dịch vụ dự án chưa được cài đặt.

    Tùy thuộc vào lượng dữ liệu trong môi trường, quá trình nâng cấp có thể mất vài giờ. Nhóm cốt lõi đang quản lý việc nâng cấp nên lập kế hoạch phù hợp và chạy nâng cấp trong giờ không phải làm việc. Trong một số trường hợp, nếu khối lượng dữ liệu lớn, bản nâng cấp nên được chạy vào cuối tuần. Quyết định về việc lên lịch phải dựa trên kết quả thử nghiệm trong môi trường thấp hơn.

3. Nâng cấp các giải pháp tùy chỉnh khi thích hợp. Tại thời điểm này, hãy triển khai bất kỳ thay đổi nào bạn đã thực hiện đối với các tùy chỉnh của mình trong [Kiểm tra và cấu trúc lại các tùy chỉnh](#testing-and-refactoring-customizations) phần của bài viết này.
4. Đi đến **Cài đặt** \> **Các giải pháp** và chọn gỡ cài đặt **Hoạt động dự án Các thành phần không được chấp nhận** dung dịch.

    Giải pháp này là giải pháp tạm thời giữ mô hình dữ liệu hiện có và các thành phần có trong quá trình nâng cấp. Bằng cách loại bỏ giải pháp này, bạn loại bỏ tất cả các trường và thành phần không còn được sử dụng. Bằng cách này, bạn sẽ giúp đơn giản hóa giao diện và làm cho việc tích hợp và mở rộng dễ dàng hơn.
    
### <a name="upgrade-to-project-operations-lite"></a>Nâng cấp lên Project Operations Lite

Các bước sau đây mô tả quá trình nâng cấp và ghi nhật ký lỗi liên quan:

1. **Kiểm tra phiên bản PSA:** Để cài đặt Hoạt động dự án, bạn phải có V3.10.58.120 trở lên.
1. **Xác thực trước:** Khi quản trị viên bắt đầu nâng cấp, hệ thống sẽ chạy hoạt động xác thực trước trên từng thực thể cốt lõi của giải pháp Hoạt động dự án. Bước này xác minh rằng tất cả các tham chiếu thực thể là hợp lệ và nó đảm bảo rằng dữ liệu liên quan đến WBS nằm trong giới hạn được công bố của Dự án cho Web.
1. **Nâng cấp siêu dữ liệu:** Sau khi xác thực trước thành công, hệ thống bắt đầu các thay đổi đối với lược đồ và tạo giải pháp thành phần không dùng nữa. Bạn có thể xóa giải pháp không dùng nữa này sau khi đã hoàn thành tất cả các tùy chỉnh được yêu cầu tái cấu trúc. Bước này là phần dài nhất của quá trình nâng cấp và có thể mất đến bốn giờ để hoàn thành.
1. **Nâng cấp dữ liệu:** Sau khi tất cả các thay đổi giản đồ bắt buộc đã được hoàn tất trong bước nâng cấp siêu dữ liệu, dữ liệu của bạn sẽ được di chuyển sang giản đồ mới và mọi thao tác tính toán và mặc định bắt buộc sẽ được thực hiện.
1. **Cập nhật công cụ lịch trình dự án:** Sau khi nâng cấp dữ liệu thành công, **Lịch trình** tab trên trang chính được gắn nhãn lại **Nhiệm vụ**. Khi người dùng chọn tab này sau khi nâng cấp, họ được chuyển hướng đến lưới theo dõi để xem phiên bản chỉ đọc của WBS. Để chỉnh sửa WBS, họ phải bắt đầu lịch trình [Quá trình chuyển đổi](/PSA-Upgrade-Project-Conversion.md). Tất cả các dự án không có WBS có sẵn đều có thể sử dụng trực tiếp trải nghiệm lập lịch mới mà không cần chuyển đổi.
 
### <a name="validate-common-scenarios"></a>Xác thực các tình huống phổ biến

Khi bạn xác thực các tùy chỉnh cụ thể của mình, chúng tôi khuyên bạn cũng nên xem xét các quy trình kinh doanh được hỗ trợ trên các ứng dụng. Các quy trình kinh doanh này bao gồm, nhưng không giới hạn, việc tạo ra các thực thể bán hàng như báo giá và hợp đồng cũng như tạo các dự án bao gồm WBS và phê duyệt các thực tế.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Những thay đổi lớn giữa Tự động hóa dịch vụ dự án và Vận hành dự án

Phần này cung cấp một bản tóm tắt về những thay đổi chính mà bạn có thể mong đợi giữa Tự động hóa dịch vụ dự án và Hoạt động dự án.

### <a name="project-planning"></a>Lập kế hoạch dự án

Khả năng lập kế hoạch dự án trong Hoạt động dự án không còn dựa vào sự kết hợp logic phía máy khách và logic phía máy chủ. Thay vào đó, Hoạt động Dự án sử dụng Dự án cho Web làm công cụ lập lịch của nó. Sự thay đổi này trong khả năng lập lịch cho phép một số tính năng mới, chẳng hạn như chế độ xem Board và Gantt, lập kế hoạch theo hướng tài nguyên, [các mục trong danh sách kiểm tra nhiệm vụ](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) và các chế độ lập lịch dự án. Các khả năng lập lịch mới cũng được hỗ trợ bởi một loạt các [giao diện lập trình ứng dụng (API)](../project-management/schedule-api-preview.md). Các API này nhằm giúp đảm bảo rằng không có hoạt động lập trình nào để tạo, cập nhật hoặc xóa một thực thể trong WBS sẽ làm hỏng các trường được tính toán trong lịch biểu.

### <a name="billing-and-pricing"></a>Định giá và thanh toán

Là một phần của việc tiếp tục đầu tư vào Hoạt động Dự án, một số khả năng mới có sẵn trong Lập hóa đơn và định giá. Dưới đây là một số ví dụ:

- [Ghi lại việc sử dụng tài liệu cho các dự án và nhiệm vụ dự án](../material/material-usage-log.md)
- [Quản lý hợp đồng phụ](../pro/subcontracting/managing-subcontracts-overview.md)
- [Hợp đồng dựa trên tiền tạm ứng và giữ lại](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Hợp đồng không vượt quá trạng thái và xác nhận](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Thanh toán dựa trên công việc

### <a name="resource-management"></a>Quản lý nguồn lực

Hoạt động dự án cung cấp hỗ trợ tùy chọn cho Universal Resource Scheduling (URS) hội đồng quản trị và trợ lý lập lịch trình. Trải nghiệm mới này sẽ trở thành bắt buộc trong làn sóng tháng 4 năm 2023.

## <a name="frequently-asked-questions"></a>Các câu hỏi thường gặp

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Những loại triển khai nào hiện được hỗ trợ để nâng cấp?

| Nguồn                                                 | Mục tiêu                                                    | Trạng thái                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | Triển khai Project Operations Lite                        | Hỗ trợ               |
| Dynamics 365 Finance Quản lý và Kế toán Dự án | Triển khai Project Operations Lite                        | Hiện không được hỗ trợ |
| Quản lý dự án tài chính và kế toán              | Project Operations dành cho tình huống dựa trên nguồn lực/hàng không trữ kho     | Hiện không được hỗ trợ |
| Tự động hóa dịch vụ dự án 3.x                         | Project Operations dành cho tình huống dựa trên nguồn lực/hàng không trữ kho     | Hiện không được hỗ trợ |
| Dự án cho Web (môi trường chuyên dụng)            | Triển khai Project Operations Lite                        | Hiện không được hỗ trợ |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Làm cách nào để cài đặt Hoạt động Dự án trước khi có công cụ nâng cấp?

Có hai tùy chọn để cài đặt Hoạt động Dự án trước khi có công cụ nâng cấp:

- Cung cấp một môi trường mới.
- Triển khai Hoạt động dự án một cách riêng biệt trên bất kỳ tổ chức bán hàng nào không có Tự động hóa dịch vụ dự án.

Nếu Tự động hóa dịch vụ dự án được cài đặt trên một tổ chức, nhưng nó không được sử dụng, nó có thể được gỡ cài đặt. Sau khi bạn loại bỏ hoàn toàn Tự động hóa dịch vụ dự án, Hoạt động dự án có thể được cài đặt trên cùng một tổ chức.
