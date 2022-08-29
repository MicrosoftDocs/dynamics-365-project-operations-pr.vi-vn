---
title: Nâng cấp từ Tự động hóa dịch vụ dự án lên Vận hành dự án
description: Bài viết này cung cấp tổng quan về quá trình nâng cấp từ Microsoft Dynamics 365 Project Service Automation đến Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/13/2022
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
ms.openlocfilehash: c7958c1474820361269f19ea8c9279b96f087d7a
ms.sourcegitcommit: 8edd24201cded2672cec16cd5dc84c6a3516b6c2
ms.translationtype: MT
ms.contentlocale: vi-VN
ms.lasthandoff: 08/06/2022
ms.locfileid: "9230295"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Nâng cấp từ Tự động hóa dịch vụ dự án lên Vận hành dự án

Chúng tôi vui mừng thông báo giai đoạn đầu tiên trong ba giai đoạn nâng cấp từ Microsoft Dynamics 365 Project Service Automation đến Dynamics 365 Project Operations. Bài viết này cung cấp một cái nhìn tổng quan cho những khách hàng đang dấn thân vào hành trình thú vị này. Các bài viết trong tương lai sẽ bao gồm các cân nhắc của nhà phát triển và thông tin chi tiết về các cải tiến của tính năng. Họ sẽ không chỉ cung cấp hướng dẫn để giúp bạn chuẩn bị cho việc nâng cấp lên Hoạt động dự án mà còn giải thích những gì bạn có thể mong đợi sau khi nâng cấp.

Chương trình nâng cấp sẽ được chia thành ba giai đoạn.

| Nâng cấp giao hàng | Giai đoạn 1 (tháng 1 năm 2022) | Giai đoạn 2 (Làn sóng tháng 4 năm 2022) | Giai đoạn 3  |
|------------------|------------------------|---------------------------|---------------------------|
| Không phụ thuộc vào cấu trúc phân tích công việc (WBS) cho các dự án | : heavy_check_mark: | : heavy_check_mark: | : heavy_check_mark: |
| WBS trong giới hạn được hỗ trợ hiện tại của Hoạt động dự án | | : heavy_check_mark: | : heavy_check_mark: |
| WBS nằm ngoài giới hạn được hỗ trợ hiện tại của Hoạt động dự án, bao gồm hỗ trợ cho máy khách Project trên máy tính | | | : heavy_check_mark: |

## <a name="upgrade-process-features"></a>Nâng cấp các tính năng của quy trình 

Là một phần của quá trình nâng cấp, chúng tôi đã thêm nhật ký nâng cấp vào sơ đồ trang web, để quản trị viên có thể chẩn đoán lỗi dễ dàng hơn. Ngoài giao diện mới, các quy tắc xác thực mới sẽ được thêm vào để đảm bảo tính toàn vẹn của dữ liệu sau khi nâng cấp. Các xác nhận sau sẽ được thêm vào quá trình nâng cấp.

| Xác thực | Giai đoạn 1 (tháng 1 năm 2022) | Giai đoạn 2 (Làn sóng tháng 4 năm 2022) | Giai đoạn 3  |
|-------------|------------------------|---------------------------|---------------------------|
| WBS sẽ được xác thực để chống lại các vi phạm toàn vẹn dữ liệu phổ biến (ví dụ: gán tài nguyên được liên kết với cùng một nhiệm vụ mẹ nhưng có các dự án mẹ khác nhau). | | : heavy_check_mark: | : heavy_check_mark: |
| WBS sẽ được xác nhận dựa trên [giới hạn đã biết của Dự án cho Web](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | : heavy_check_mark: | : heavy_check_mark: |
| WBS sẽ được xác nhận theo các giới hạn đã biết của máy khách Project desktop. | |  | : heavy_check_mark: |
| Các tài nguyên có thể đặt trước và lịch dự án sẽ được đánh giá dựa trên các ngoại lệ quy tắc lịch không tương thích phổ biến. | | : heavy_check_mark: | : heavy_check_mark: |

Trong giai đoạn 2, những khách hàng nâng cấp lên Hoạt động dự án sẽ được nâng cấp các dự án hiện có của họ lên trải nghiệm chỉ đọc để lập kế hoạch dự án. Trong trải nghiệm chỉ đọc này, WBS đầy đủ sẽ hiển thị trong lưới theo dõi. Để chỉnh sửa WBS, người quản lý dự án có thể chọn **Chuyển thành** trên chính **Dự án** trang. Sau đó, một quy trình nền sẽ cập nhật dự án để nó hỗ trợ trải nghiệm lập lịch dự án mới từ Project cho Web. Giai đoạn này thích hợp cho những khách hàng có dự án phù hợp với [các giới hạn đã biết của Dự án cho Web](/project-for-the-web/project-for-the-web-limits-and-boundaries).

Trong giai đoạn 3, hỗ trợ cho máy khách Project desktop sẽ được bổ sung, vì lợi ích của những khách hàng muốn tiếp tục chỉnh sửa dự án của họ từ ứng dụng đó. Tuy nhiên, nếu các dự án hiện có được chuyển đổi sang Dự án mới cho trải nghiệm Web, quyền truy cập vào phần bổ trợ sẽ bị vô hiệu hóa cho mỗi dự án được chuyển đổi.

## <a name="prerequisites"></a>Điều kiện tiên quyết

Để đủ điều kiện nhận nâng cấp giai đoạn 1, khách hàng phải đáp ứng các tiêu chí sau:

- Môi trường đích không được chứa bất kỳ bản ghi nào trong **msdyn_projecttask** thực thể.
- Giấy phép Hoạt động Dự án hợp lệ phải được chỉ định cho tất cả người dùng đang hoạt động của khách hàng. 
- Khách hàng phải xác thực quy trình nâng cấp trong ít nhất một môi trường phi sản xuất có tập dữ liệu đại diện phù hợp với dữ liệu sản xuất.
- Môi trường đích phải được cập nhật lên Bản phát hành cập nhật tự động hóa dịch vụ dự án 41 (3.10.62.162) hoặc mới hơn.

Các điều kiện tiên quyết cho giai đoạn 2 và giai đoạn 3 sẽ được cập nhật theo cách tiếp cận ngày khả dụng chung.

## <a name="licensing"></a>Cấp phép

Nếu bạn có giấy phép hoạt động cho Tự động hóa dịch vụ dự án, bạn có thể cài đặt và sử dụng Hoạt động dự án, bao gồm tất cả các khả năng của Tự động hóa dịch vụ dự án và hơn thế nữa. Bằng cách này, bạn có thể kiểm tra khả năng của Hoạt động dự án trong khi bạn tiếp tục sử dụng Tự động hóa dịch vụ dự án trong sản xuất. Sau khi giấy phép Tự động hóa Dịch vụ Dự án của bạn hết hạn, bạn sẽ phải chuyển sang Hoạt động Dự án. Khi lập kế hoạch chuyển đổi này, bạn phải tính đến thực tế là giấy phép Hoạt động Dự án không bao gồm giấy phép Tự động hóa Dịch vụ Dự án.

## <a name="testing-and-refactoring-customizations"></a>Kiểm tra và cấu trúc lại các tùy chỉnh

Khi bắt đầu, hãy nhập tất cả các tùy chỉnh vào môi trường Hoạt động Dự án (Lite) sạch để xác nhận rằng quá trình nhập thành công và các hoạt động kinh doanh hoạt động như mong đợi.

Dưới đây là một số điều cần chú ý:

- Nhập có thể không thành công vì thiếu phụ thuộc. Nói cách khác, các trường tham chiếu tùy chỉnh hoặc các thành phần khác đã bị loại bỏ trong Hoạt động dự án. Trong trường hợp này, hãy loại bỏ những phụ thuộc này khỏi môi trường phát triển.
- Nếu các giải pháp không được quản lý và quản lý của bạn bao gồm các thành phần không được tùy chỉnh, hãy xóa các thành phần đó khỏi giải pháp. Ví dụ: khi bạn tùy chỉnh **Dự án** thực thể, chỉ thêm tiêu đề thực thể vào giải pháp của bạn. Đừng thêm tất cả các trường. Nếu trước đó bạn đã thêm tất cả các thành phần con, bạn có thể phải tạo một giải pháp mới theo cách thủ công và thêm các thành phần có liên quan vào nó.
- Biểu mẫu và chế độ xem có thể không xuất hiện như mong đợi. Trong một số trường hợp, nếu bạn đã tùy chỉnh bất kỳ biểu mẫu hoặc dạng xem có sẵn nào, các tùy chỉnh có thể ngăn các cập nhật mới trong Hoạt động dự án có hiệu lực. Để xác định những vấn đề này, chúng tôi khuyên bạn nên thực hiện đánh giá song song việc cài đặt hoàn thiện Hoạt động dự án và cài đặt Hoạt động dự án bao gồm các tùy chỉnh của bạn. So sánh các biểu mẫu được sử dụng phổ biến nhất trong doanh nghiệp của bạn để xác nhận rằng phiên bản biểu mẫu của bạn vẫn có ý nghĩa và không thiếu điều gì đó từ phiên bản sạch của biểu mẫu. Thực hiện cùng một loại đánh giá song song cho bất kỳ chế độ xem nào mà bạn đã tùy chỉnh.
- Logic nghiệp vụ có thể không thành công trong thời gian chạy. Vì các tham chiếu đến các trường trong trình cắm của bạn không được xác thực tại thời điểm nhập, logic nghiệp vụ có thể không thành công do các tham chiếu đến các trường không còn tồn tại và bạn có thể nhận được thông báo lỗi tương tự như ví dụ sau: "'Dự án" thực thể không chứa thuộc tính Name = 'msdyn_plannedhours' và NameMapping = 'Logical'. " Trong trường hợp này, hãy sửa đổi các tùy chỉnh của bạn để chúng sử dụng các trường mới. Nếu bạn sử dụng các lớp proxy được tạo tự động và các tham chiếu kiểu mạnh trong logic trình cắm của mình, hãy xem xét việc tạo lại các proxy đó từ một bản cài đặt sạch. Bằng cách này, bạn có thể dễ dàng xác định tất cả các vị trí mà trình cắm của bạn phụ thuộc vào các trường không dùng nữa.

Sau khi bạn cập nhật các tùy chỉnh của mình để nhập Hoạt động dự án một cách rõ ràng, hãy chuyển sang các bước tiếp theo.

## <a name="end-to-end-testing-in-development-environments"></a>Kiểm tra đầu cuối trong môi trường phát triển

### <a name="initiate-upgrade"></a>Bắt đầu nâng cấp 

1. Bên trong Power Platform trung tâm quản trị, tìm và chọn môi trường của bạn. Sau đó, trong các ứng dụng, hãy tìm và chọn **Dynamics 365 Project Operations**.
2. Lựa chọn **Cài đặt** để bắt đầu nâng cấp. Các Power Platform trung tâm quản trị sẽ trình bày cài đặt này như một cài đặt mới. Tuy nhiên, sự hiện diện của phiên bản Project Service Automation trước đó sẽ được phát hiện và cài đặt hiện có sẽ được nâng cấp.

    Sau khi hoàn tất nâng cấp, môi trường sẽ hiển thị rằng Hoạt động dự án đã được cài đặt và Tự động hóa dịch vụ dự án chưa được cài đặt.

    > [!NOTE]
    > Tùy thuộc vào lượng dữ liệu trong môi trường, quá trình nâng cấp có thể mất vài giờ. Nhóm cốt lõi đang quản lý việc nâng cấp nên lập kế hoạch phù hợp và chạy nâng cấp trong giờ không phải làm việc. Trong một số trường hợp, nếu khối lượng dữ liệu lớn, bản nâng cấp nên được chạy vào cuối tuần. Quyết định về việc lên lịch phải dựa trên kết quả thử nghiệm trong môi trường thấp hơn.

3. Nâng cấp các giải pháp tùy chỉnh khi thích hợp. Tại thời điểm này, hãy triển khai bất kỳ thay đổi nào bạn đã thực hiện đối với các tùy chỉnh của mình trong [Kiểm tra và cấu trúc lại các tùy chỉnh](#testing-and-refactoring-customizations) phần của bài viết này.
4. Đi đến **Cài đặt** \> **Các giải pháp** và chọn gỡ cài đặt **Hoạt động dự án Các thành phần không được chấp nhận** dung dịch.

    Giải pháp này là giải pháp tạm thời giữ mô hình dữ liệu hiện có và các thành phần có trong quá trình nâng cấp. Bằng cách loại bỏ giải pháp này, bạn loại bỏ tất cả các trường và thành phần không còn được sử dụng. Bằng cách này, bạn sẽ giúp đơn giản hóa giao diện và làm cho việc tích hợp và mở rộng dễ dàng hơn.
    
### <a name="validate-common-scenarios"></a>Xác thực các tình huống phổ biến

Khi bạn xác thực các tùy chỉnh cụ thể của mình, chúng tôi khuyên bạn cũng nên xem xét các quy trình kinh doanh được hỗ trợ trên các ứng dụng. Các quy trình kinh doanh này bao gồm, nhưng không giới hạn, việc tạo ra các thực thể bán hàng như báo giá và hợp đồng cũng như tạo các dự án bao gồm WBS và phê duyệt các thực tế.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Những thay đổi lớn giữa Tự động hóa dịch vụ dự án và Vận hành dự án

Phần này cung cấp tóm tắt về những thay đổi chính mà bạn có thể mong đợi giữa Tự động hóa dịch vụ dự án và Hoạt động dự án.

### <a name="project-planning"></a>Lập kế hoạch dự án

Khả năng lập kế hoạch dự án trong Hoạt động dự án không còn dựa vào sự kết hợp logic phía máy khách và logic phía máy chủ. Thay vào đó, Hoạt động Dự án sử dụng Dự án cho Web làm công cụ lập lịch của nó. Sự thay đổi này trong khả năng lập lịch cho phép một số tính năng mới, chẳng hạn như chế độ xem Board và Gantt, lập kế hoạch theo hướng tài nguyên, [các mục trong danh sách kiểm tra nhiệm vụ](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) và các chế độ lập lịch dự án. Các khả năng lập lịch mới cũng được hỗ trợ bởi một loạt các [giao diện lập trình ứng dụng (API)](../project-management/schedule-api-preview.md). Các API này nhằm giúp đảm bảo rằng không có hoạt động lập trình nào để tạo, cập nhật hoặc xóa một thực thể trong WBS sẽ làm hỏng các trường được tính toán trong lịch biểu.

## <a name="billing-and-pricing"></a>Định giá và thanh toán

Là một phần của việc tiếp tục đầu tư vào Hoạt động Dự án, một số khả năng mới có sẵn trong Lập hóa đơn và định giá. Dưới đây là một số ví dụ:

- [Ghi lại việc sử dụng tài liệu cho các dự án và nhiệm vụ dự án](../material/material-usage-log.md)
- [Quản lý hợp đồng phụ](../pro/subcontracting/managing-subcontracts-overview.md)
- [Hợp đồng dựa trên tiền tạm ứng và giữ lại](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Hợp đồng không vượt quá trạng thái và xác nhận](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Thanh toán dựa trên công việc

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
- Triển khai Hoạt động Dự án một cách riêng biệt trên bất kỳ tổ chức bán hàng nào không có Tự động hóa Dịch vụ Dự án.

> [!NOTE]
> Nếu Tự động hóa dịch vụ dự án được cài đặt trên một tổ chức, nhưng nó không được sử dụng, nó có thể được gỡ cài đặt. Sau khi bạn loại bỏ hoàn toàn Tự động hóa dịch vụ dự án, Hoạt động dự án có thể được cài đặt trên cùng một tổ chức.
